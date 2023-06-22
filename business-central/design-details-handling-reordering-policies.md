---
title: Design-Details – Handhabung von Richtlinien für die Neuordnung
description: 'Dieser Artikel gibt einen Überblick über die Nachbestellungsrichtlinien, die Sie bei der Beschaffungsplanung verwenden können.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/24/2023
ms.custom: bap-template
---
# <a name="design-details-handling-reordering-policies" />Designdetails: Umgang mit Wiederbeschaffungsrichtlinien

Um einen Artikel in die Beschaffungsplanung aufzunehmen, müssen Sie auf der Seite **Artikelkarte** eine Nachbestellungsrichtlinie dafür festlegen. Die folgenden Wiederbeschaffungsrichtlinien sind verfügbar:  

* Feste Bestellmenge  
* Auffüllen auf Maximalbestand  
* Bestellung  
* Los-für-Los  

Die Richtlinien **Feste Bestellmenge** und **Höchstmenge** beziehen sich auf die Bestandsplanung. Diese Richtlinien koexistieren mit dem schrittweisen Ausgleich des Angebots und der Auftragsverfolgung.  

## <a name="the-role-of-the-reorder-point" />Die Rolle des Meldebestands

Ein Minimalbestand repräsentiert den Bedarf während der Beschaffungszeit. Wenn der Lagerstatus voraussichtlich unter den Lagerbestand gerät, der durch den Minimalbestand definiert ist, muss mehr bestellt werden. Der Bestand wird schrittweise verringert, bis der Nachschub eintrifft. Er kann Null oder den Sicherheitsbestand erreichen. Das Planungssystem schlägt einen vorwärtsgeplanten Beschaffungsauftrag an dem Zeitpunkt vor, an dem der Bestand unter den Minimalbestand sinkt.  

Lagerebenen können sich während des Zeitfensters erheblich verändern. Daher überwacht das Planungssystem ständig verfügbare Bestände.

## <a name="monitoring-the-projected-inventory-level-and-the-reorder-point" />Überwachen der voraussichtlichen Lagerebene und des Meldebestands

Der Bestand ist eine Art Vorrat, jedoch für Bestandsplanung unterscheidet das Planungssystem zwischen zwei Bestandsebenen:  

* Voraussichtlicher Lagerbestand  
* Voraussichtlich verfügbarer Lagerbestand  

### <a name="projected-inventory" />Voraussichtlicher Lagerbestand

Zu Beginn des Planungsprozesses ist der voraussichtliche Bestand die Bruttobestandsmenge. Die Bruttomenge umfasst gebuchtes und nicht gebuchtes Angebot und Nachfrage in der Vergangenheit. Diese Menge wird zu einer voraussichtlichen Lagerebene, die Bruttomengen aus zukünftigem Angebot und Nachfrage beibehalten. Zukünftiges Angebot und zukünftige Nachfrage werden entlang der Zeitlinie eingeführt, entweder reserviert oder auf andere Weise zugewiesen.  

Das Planungssystem verwendet voraussichtlichen Bestand, um den Minimalbestand zu überwachen und um die Wiederbeschaffungsmenge zu bestimmen, wenn die Wiederbeschaffungsrichtlinie **Höchstmenge** verwendet wird.  

### <a name="projected-available-inventory" />Voraussichtlich verfügbarer Lagerbestand

Der voraussichtlich verfügbare Lagerbestand ist Teil ist der voraussichtliche Bestand, der zum Erfüllen der Nachfrage zu einem bestimmten Zeitpunkt verfügbar ist. Das Planungssystem verwendet den voraussichtlich verfügbaren Lagerbestand, wenn die Sicherheitsbestandsebene überwacht wird. Für unerwarteten Bedarf muss immer ein Sicherheitsbestand verfügbar sein.  

### <a name="time-buckets" />Zeitrahmen

Der voraussichtliche Lagerbestands ist entscheidend, um zu ermitteln, wann der Minimalbestand erreicht ist oder unterschritten wurde, und wie die richtige Auftragsmenge berechnet wird, wenn das Wiederbeschaffungsverfahren **Höchstmenge** verwendet wird.  

Der voraussichtliche Lagerbestand wird am Anfang der Planungsperiode berechnet. Dies ist eine grobe Ebene, bei der Reservierungen und andere Zuordnungen nicht berücksichtigt werden. Um dieses Lagerbestandsniveau während der Planungssequenz zu überwachen, überwacht das Planungssystem die aggregierten Änderungen über eine Zeitperiode hinweg. Dieser Zeitraum wird als *Zeitrahmen* bezeichnet. Weitere Informationen zu Zeitrahmen finden Sie unter [Zeitrahmen](#time-buckets). Das Planungssystem stellt sicher, dass der Zeitrahmen mindestens einen Tag beträgt. Ein Tag ist die Mindestzeiteinheit für Nachfrage- oder Angebotsereignisse.  

### <a name="determining-the-projected-inventory-level" />Bestimmen des voraussichtlichen Lagerbestands

Die folgende Sequenz beschreibt, wie das Planungssystem den voraussichtlichen Lagerbestand bestimmt:  

* Wenn ein Vorratsereignis, wie eine Bestellung, vollständig geplant wird, erhöht es den voraussichtlichen Lagerbestand am Fälligkeitsdatum des Ereignisses.  
* Wenn ein Nachfrageereignis vollständig erfüllt wurde, verringert es nicht sofort den voraussichtlichen Lagerbestand. Stattdessen bucht es eine Minderungserinnerung, die ein interner Datensatz ist, der das Datum und die Menge der Ergänzung zum voraussichtlichen Lagerbestand beinhaltet.  
* Wenn ein späteres Lieferereignis geplant und der Zeitleiste hinzugefügt wird, untersucht das System nacheinander gebuchte Abnahmeerinnerungen bis zum geplanten Lieferdatum. Während dieses Prozesses kann der Minimalbestand der internen Zunahmeerinnerung erreicht oder unterschritten werden.  
* Wenn ein neuer Beschaffungsauftrag eingegeben wird, prüft es, ob dieser vor dem aktuellen Vorrat eingegeben wird. Wenn dies der Fall ist, wird der neue Vorrat zum aktuellen Vorrat, und der Ausgleichsvorgang beginnt erneut.  

Das folgende Bild zeigt dieses Prinzip.  

![Bestimmen des geplanten Bestandes.](media/nav_app_supply_planning_2_projected_inventory.png "Bestimmen des voraussichtlichen Lagerbestands")  

1. Vorrat **Sa** von 4 (fest) schließt Bedarf **Da** von -3.  
2. CloseDemand: Erstellen Sie eine Minderungserinnerung von -3 (nicht angezeigt).  
3. Vorrat **Sa** wird mit einem Überschuss von 1 geschlossen (kein Bedarf mehr vorhanden).  

     Der voraussichtliche Lagerbestand steigt auf +4, während der voraussichtliche **verfügbare** Lagferbestand -1 wird.  

4. Der nächste Vorrat **Sb** von 2 (ein anderer Auftrag) wurdet bereits in die Zeitachse platziert.  
5. Das Planungssystem prüft auf eine Minderungserinnerung vor **Sb** (in diesem Beispiel ist dies nicht der Fall, daher wird keine Aktion ergriffen).  
6. Das Planungssystem schließt Vorrat **Sb** (kein Bedarf mehr vorhanden), entweder A: durch Reduzierung auf 0 (Stornieren) oder B: durch unverändert lassen.  

     Der voraussichtliche Lagerbestand steigt (A: +0 => +4 oder B: +2 = +6).  

7. Das Planungssystem führt eine letzte Prüfung durch. Gibt es eine Abnahmeerinnerung? Ja, es gibt eine am Datum **Da**  
8. Das Planungssystem fügt die Minderungserinnerung -3 in der Ebene des voraussichtlichen Lagerbestands hinzu, entweder A: +4 -3 = 1 oder B: +6 -3 = +3.  
9. Bei A erstellt das Planungssystem eine vorausplanende Bestellung ab Datum **Da**. Bei B wird der Minimalbestand erreicht, und es wird ein neuer Auftrag erstellt.

## <a name="the-role-of-the-time-bucket" />Die Rolle des Zeitrahmens

Der Zweck dieses Zeitrahmens ist es, Bedarfsereignisse innerhalb des Zeitfensters zu erfassen, um einen gemeinsamen Beschaffungsauftrag zu erstellen.  

Für Wiederbeschaffungsverfahren, die einen Minimalbestand verwenden, können Sie einen Zeitrahmen definieren. Zeitrahmen helfen sicherzustellen, dass Bedarfe innerhalb des gleichen Zeitraums kumuliert werden. Das System prüft dann die Auswirkung auf den projizierten Bestand und ob der Meldebestand überschritten wurde.

Wenn Sie den Meldebestand überschreiten, Plant das System einen neuen Beschaffungsauftrag vom Ende der durch den Zeitrahmen definierten Periode vorwärts. Zeitrahmen beginnen am geplanten Startdatum.  

Das Zeitrahmenkonzept spiegelt den manuellen Vorgang des Überprüfens des Lagerbestands auf häufiger Basis anstatt für jede Transaktion. Sie müssen die Häufigkeit (den Zeitrahmen) festlegen. Beispielsweise erfassen Sie möglicherweise alle Artikelanforderungen von einem Kreditor, um einen wöchentlichen Auftrag zu platzieren.  

![Beispiel für Zeitrahmen in der Planung.](media/nav_app_supply_planning_2_reorder_cycle.png "Beispiel eines Zeitrahmens in der Planung")  

Zeitrahmen werden häufig verwendet, um einen Kaskadeneffekt zu vermeiden. Zum Beispiel eine eine ausgeglichene Zeile von Bedarf und Vorrat, bei der ein frühzeitiger Bedarf storniert oder ein neuer Bedarf erstellt wird. Das Ergebnis würde sein, dass jeder Beschaffungsauftrag (mit Ausnahme des letzten) umgeplant würde.

## <a name="stay-below-the-overflow-level" />Unter dem Überlauflevel bleiben

Wenn das Wiederbeschaffungsverfahren **Maximalbestand** und **Feste Bestellmenge** verwendet werden, konzentriert sich das Planungssystem nur auf den voraussichtlichen Lagerbestand in dem vorgegebenen Zeitrahmen. Es könnte auf ein zusätzliches Angebot hindeuten, wenn negative Nachfrage- oder positive Angebotsänderungen außerhalb des Zeitfensters auftreten. Bei einem zusätzlichen Vorrat berechnet das Planungssystem die Menge, um die Sie den Vorrat verringern sollten. Diese Menge wird als "Überlauflevel" bezeichnet. Der Überlauf ist als Planungszeile mit einer **Menge ändern** oder **Abbrechen** Operation und der folgenden Warnmeldung verfügbar:  

* Achtung: Der voraussichtliche Lagerbestand [xx] ist höher als das Überlauflevel [xx] am Fälligkeitsdatum [xx].*  

![Bestandsüberlaufebene.](media/supplyplanning_2_overflow1_new.png "Lagerbestand-Überlauflevel")  

### <a name="calculating-the-overflow-level" />Berechnung des Überlauflevels

Das Überlauflevel wird auf verschiedene Arten abhängig vom Wiederbeschaffungsverfahren berechnet.  

#### <a name="maximum-qty" />Auffüllen auf Maximalbestand

Überlauflevel = Maximalbestand  

> [!NOTE]  
> Wenn Sie eine Mindestbestellmenge verwenden, wird diese wie folgt hinzugefügt:
>
> Überlaufmenge = maximaler Lagerbestand + Mindestbestellmenge.  

#### <a name="fixed-reorder-qty" />Feste Bestellmenge

Überlauflevel = Nachbestellmenge + Meldebestand  

> [!NOTE]  
> Wenn die Mindestbestellmenge höher als der Meldebestand ist, wird sie wie folgt ersetzt:
>
> Überlauflevel = Nachbestellmenge + Mindestbestellmenge  

#### <a name="order-multiple" />Losgrößenrundungsfaktor

Wenn ein Auftragsvielfaches vorhanden ist, reguliert dieses den Überlauflevel für die Wiederbeschaffungsverfahren die Höchstmenge und die Feste Nachbestellmenge.  

### <a name="creating-the-planning-line-with-an-overflow-warning" />Erstellen der Planungszeile mit Überlaufwarnmeldung

Eine Planungszeile wird erstellt, wenn eine vorhandene Lieferung dazu führt, dass der voraussichtliche Lagerbestand höher ist, als das Überlauflevel am Ende eines Zeitrahmens. Um vor einem Extravorrat zu warnen, hat die Planungszeile eine Warnmeldung, das Feld **Ereignismeldung akzeptieren** ist nicht aktiviert, und die Ereignismeldung ist entweder **Abbrechen** oder **Menge ändern**.  

#### <a name="calculating-the-planning-line-quantity" />Berechnen der Planungszeilenmenge

Die Menge auf einer Planungszeile wird wie folgt berechnet:

Planungszeilen-Menge = Netzstrom-Menge - (voraussichtlicher Lagerbestand - Überlauflevel)  

> [!NOTE]  
> Bei sAs bei allen Hinweiszeilen werden die maximale und Mindestauftragsmengen und das Auftragsvielfache ignoriert.  

#### <a name="defining-the-action-message-type" />Definieren des Aktionsmeldungstyps

* Wenn die Planungszeilenmenge höher als 0 ist, ist die Aktionsmeldung **Menge ändern**.  
* Wenn die Planungszeilenmenge gleich oder weniger als 0 ist, ist die Aktionsmeldung **Stornieren**.  

#### <a name="composing-the-warning-message" />Verfassen der Warnmeldung

Bei einem Überlauf zeigt die Seite **Planungselement ohne Nachverfolgung** eine Warnmeldung mit den folgenden Informationen an:  

* Der voraussichtliche Lagerbestand, der die Warnung ausgelöst hat.  
* Der berechnete Überlauflevel  
* Das Fälligkeitsdatum des Vorratsereignisses  

Beispiel: „Der voraussichtliche Lagerbestand 120 übersteigt das Überlauflevel 60 am 28.01.23“  

### <a name="example-scenario" />Beispielszenario

In diesem Szenario ändert ein Debitor einen Verkaufsauftrag von 70 zu 40 Stück zwischen zwei Planungen. Die Überlauffunktion reduziert den Einkauf, der für die anfängliche Verkaufsmenge vorgeschlagen worden war.  

#### <a name="item-setup" />Artikeleinrichtung

|Wiederbeschaffungsverfahren|Auffüllen auf Maximalbestand|  
|-----------------------|------------------|  
|Maximale Losgröße|100|  
|Minimalbestand|50|  
|Lagerbest|80|  

#### <a name="situation-before-sales-decrease" />Situation vor Vertriebsabgang

|Ereignis|"Menge ändern"|Voraussichtlicher Lagerbestand|  
|-----------|-----------------|-------------------------|  
|Tag eins|Keine|80|  
|Verkauf|-70|10|  
|Ende des Zeitrahmens|Keine|10|  
|Neue Bestellung vorschlagen|+90|100|  

#### <a name="situation-after-sales-decrease" />Situation nach Vertriebsabgang

|Ändern|"Menge ändern"|Voraussichtlicher Lagerbestand|  
|------------|-----------------|-------------------------|  
|Tag eins|Keine|80|  
|Verkauf|-40|40|  
|Einkauf|+90|130|  
|Ende des Zeitrahmens|Keine|130|  
|Vorschlagen, den Einkauf zu vermindern<br><br> Auftrag von 90 bis 60|-30|100|  

#### <a name="resulting-planning-lines" />Planungszeilen erstellen

Das System erstellt eine Warnungsplanungszeile, um den Einkauf um 30 von 90 auf 60 zu verringern, um den voraussichtlichen Lagerstatus auf 100 entsprechend dem Überlauflevel festzuhalten.  

![Planen Sie nach dem Überlauflevel.](media/nav_app_supply_planning_2_overflow2.png "Plan gemäß Überlauflevel")  

> [!NOTE]  
> Ohne die Überlauffunktion werden keine Warnmeldungen erstellt, wenn die voraussichtliche Lagerebene über dem Maximum liegt, was einen Extravorrat von 30 verursachen könnte.

## <a name="handling-projected-negative-inventory" />Bestandvoraussichtlich negativ behandeln

Der Minimalbestand drückt den voraussichtlichen Bedarf während der Beschaffungszeit des Artikels aus. Der voraussichtliche Lagerbestand muss groß genug sein, um den Bedarf zu decken, bis der neue Auftrag eingegangen ist. Unterdessen gleicht der Sicherheitsbestand Schwankungen im Bedarf bis zu einem anvisierten Servicelevel aus.  

Das Planungssystem betrachtet es als Notfall, wenn ein zukünftiger Bedarf nicht aus dem prognostizierten Bestand gedeckt werden kann. Oder, anders ausgedrückt, dass der prognostizierte Lagerbestand negativ wird. Das System schlägt Ihnen vor, einen neuen Beschaffungsauftrag anzulegen, um den ungedeckten Teil des Bedarfs zu decken. Die Größe des neuen Beschaffungsauftrags berücksichtigt weder den maximalen Bestand oder die Nachbestellmenge noch die folgenden Auftragsmodifikatoren:

* Maximale Losgröße
* Minimale Losgröße
* Losgrößenrundungsfaktor 

Stattdessen spiegelt sie den genauen Mangel wider.  

In der Planungszeile für diesen Typ von Beschaffungsauftrag wird ein **Notfall**-Warnsymbol angezeigt, das zusätzliche Informationen zur Situation bereitstellt.  

In der folgenden Abbildung zeigt Vorrat D eine Notfallbestellung an, um negativen Bestand auszugleichen.  

![Notfallplanungsvorschlag zur Vermeidung von negativem Bestand.](media/nav_app_supply_planning_2_negative_inventory.png "NotfallPlanungsarbeitsblatt zur Vermeidung von negativem Lagerbestand")  

1. Vorrat **A** anfänglicher voraussichtlicher Lagerbestand, liegt unter Minimalbestand.  
2. Ein neuer voraus geplanter Vorrat wurde erstellt (**C**).  

     (Menge = Maximalbestand - Voraussichtlicher Lagerbestand)  
3. Vorrat **A** wird durch Bedarf **B** geschlossen, der nicht vollständig abgedeckt wird.  

     (Bedarf **B** könnte versuchen, Zubehör C einzuplanen, doch der zeitrahmen verhindert dies.)  
4. Neuer Vorrat (**D**) wird erstellt, um die Restmenge auf Anfordung **B** zu decken.  
5. Bedarf **B** ist geschlossen (eine Erinnerung für den voraussichtlichen Lagerbestand wird erstellt).  
6. Das neue Vorrat **D** wird geschlossen.  
7. Voraussichtlicher Lagerbestand wird überprüft. Der Meldebestand wurde nicht überschritten.  
8. Vorrat **C** ist geschlossen (es gibt keinen weiteren Bedarf).  
9. Letzte Prüfung. Es gibt keine ausstehenden Erinnerungen auf Lagerebene.  

Im nächsten Abschnitt werden die Eigenschaften der vier unterstützten Wiederbeschaffungsrichtlinien beschrieben.

## <a name="reordering-policies" />Wiederbeschaffungsverfahren

Wiederbeschaffungsrichtlinien definieren, wie viel zu bestellen ist, wenn der Artikel aufgefüllt werden muss. Es gibt verschiedene Wiederbeschaffungsverfahren.  

### <a name="fixed-reorder-quantity" />Feste Wiederbeschaffungsmenge

Die feste Richtlinie für die Wiederbeschaffungsmenge wird normalerweise für die Bestandsplanung für Artikel mit den folgenden Merkmalen verwendet:

* Geringe Bestandskosten
* Geringes Veralterungsrisiko
* Geringe Artikelanzahl

Verwenden Sie diese Methode normalerweise in Verbindung mit einem Minimalbestand, der den voraussichtlichen Bedarf während der Beschaffungszeit des Artikels angezeigt.  

#### <a name="calculated-per-time-bucket" />Berechnet pro Zeitrahmen

Wenn Sie den Meldebestand in einem Zeitrahmen (Meldezyklus) erreichen oder überschreiten, schlägt das System zwei Aktionen vor:

* Einen neuen Beschaffungsauftrag für die relevante Menge erstellen
* Die Bestellung ab dem ersten Datum nach dem Ende des Zeitfensters vorwärts planen  

Der Minimalbestand im Zeitrahmen reduziert die Anzahl der Beschaffungsvorschläge. Er spiegelt einen Prozess wider, bei dem der tatsächliche Inhalt der Plätze in Ihrem Lager manuell überprüft wird.  

#### <a name="creates-only-necessary-supply" />Erstellt nur erforderlichen Vorrat

Bevor es einen neuen Beschaffungsauftrag vorschlägt, um einen Meldebestand zu erfüllen, prüft das Planungssystem auf den folgenden Vorrat:

* Ob Vorrat bereits bestellt ist
* Ob Sie erwarten, den Vorrat innerhalb der Lieferzeit des Artikels zu erhalten

Das System schlägt keine neuen Beschaffungsauftrag vor, wenn ein Vorrat den voraussichtlichen Lagerbestand innerhalb der Beschaffungszeit auf den Minimalbestand bringt.  

Beschaffungsaufträge, die speziell erstellt werden, um einen Minimalbestand zu erfüllen, werden aus dem Vorratsausgleich ausgeschlossen und nicht geändert. Wenn Sie einen Artikel mit einem Meldebestand auslaufen lassen möchten, überprüfen Sie Ihre ausstehenden Lieferbestellungen manuell oder ändern Sie die Wiederbeschaffungsverfahren in **Charge für Charge**. Das System wird zusätzlichen Vorrat reduzieren oder stornieren.  

#### <a name="combines-with-order-modifiers" />Wird mit anderen Auftragsmodifizierern kombiniert

Die Auftragsmodifikatoren „Minimale Auftragsmenge“, „Maximale Auftragsmenge“ und „Auftragsvielfaches“ sollten keine bedeutende Rolle spielen, wenn Sie die feste Nachbestellungsmengenrichtlinie verwenden. Das Planungssystem berücksichtigt sie jedoch:

* Reduzieren Sie die Menge auf die angegebene maximale Bestellmenge (und erstellen Sie zwei oder mehr Lieferungen, um die Gesamtbestellmenge zu erreichen).
* Erhöhen Sie die Bestellung auf die angegebene Mindestbestellmenge
* Runden Sie die Bestellmenge auf ein bestimmtes Bestellvielfaches auf  

#### <a name="combines-with-calendars" />Zusammenfassen mit Kalendern

Bevor ein neuer Beschaffungsauftrag vorgeschlagen wird, um einen Meldebestand zu erfüllen, prüft das Planungssystem, ob der Auftrag für einen arbeitsfreien Tag geplant ist. Es verwendet die Kalender, die Sie im Feld **Basiskalendercode** in den Seiten **Unternehmensinformationen** und **Standortkarte** angegeben haben.  

Wenn das geplante Datum ein freier Tag ist, verschiebt das Planungssystem die Reihenfolge weiter zum nächsten Arbeitstag. Eine Verschiebung des Datums kann zu einem Verkaufsauftrag, der für einen Minimalbestand gilt, aber keinen bestimmten Bedarf abdeckt. Bei solcher Nachfrage ohne Bedarf erstellt das Planungssystem ein zusätzlicher Vorrat.  

#### <a name="shouldnt-be-used-with-forecasts" />Sollte nicht mit Planung verwendet werden

Da der erwartete Bedarf bereits in der Minimalbestandsebene angegeben wird, ist es nicht notwendig, eine Prognose in die Planung zu berücksichtigen. Wenn es wichtig ist, den Plan auf einer Planung zu basieren, verwenden Sie die **Charge-für-Charge**-Richtlinie.  

#### <a name="must-not-be-used-with-reservations" />Darf nicht mit Reservierungen verwendet werden

Wenn Sie eine Menge, etwa eine Menge im Bestand, für einen späteren Bedarf reserviert haben, stören Sie möglicherweise die Grundlage der Planung. Selbst wenn der voraussichtliche Lagerbestand im Hinblick auf den Minimalbestand akzeptabel ist, stehen die Mengen möglicherweise aufgrund der Reservierung nicht zur Verfügung. Das System versucht möglicherweise, dies zu kompensieren, indem Ausnahmeaufträge erstellt werden. Wir empfehlen jedoch, dass das Feld **Reservieren** für Artikel, die mit einem Meldebestand geplant werden, auf **Nie** eingestellt wird.

### <a name="maximum-quantity" />Höchstmenge

Die Richtlinie der maximalen Menge ist eine Möglichkeit zur Verwaltung des Bestands anhand eines Minimalbestands.  

Alles im Zusammenhang mit der festen Bestellmengenrichtlinie bezieht sich auch auf diese Richtlinie. Der einzige Unterschied ist die Menge des vorgeschlagenen Vorrats. Wenn Sie die Methode Auffüllen auf Maximalbestand verwenden, erfolgt die Definition der Bestellmenge dynamisch auf Basis der voraussichtlichen Lagerebene. Daher ist es in der Regel von Bestellung zu Bestellung unterschiedlich.  

#### <a name="calculate-per-time-bucket" />Berechnet pro Zeitrahmen

Wenn Sie den Meldebestand erreichen oder überschreiten, ermittelt das System die Meldemenge am Ende eines Zeitraums. Es misst die Lücke zwischen der aktuellen voraussichtlichen Lagerebene und dem angegebenen Maximalbestand, um die zu bestellende Menge zu bestimmen. Das System prüft dann:

* Ob Vorrat bereits bestellt ist
* Ob Sie erwarten, den Vorrat innerhalb der Lieferzeit des Artikels zu erhalten

Wenn dies der Fall ist, reduziert das System die Menge des neuen Beschaffungsauftrags um die bereits bestellten Mengen.  

Wenn Sie keine maximale Bestandsmenge angeben, stellt das Planungssystem sicher, dass der voraussichtliche Bestand die Nachbestellmenge erreicht.

#### <a name="combine-with-order-modifiers" />Mit anderen Auftragsmodifizierern kombinieren

Abhängig von Ihrer Einrichtung ist es möglicherweise am besten, die Maximalmengenrichtlinie mit Bestellmodifikatoren zu kombinieren: 

* So stellen Sie eine Mindestbestellmenge sicher
* Runden Sie die Menge auf eine ganze Zahl von Einkaufsmengeneinheiten
* Die Menge in Lose aufteilen, die von der maximalen Auftragsmenge definiert sind  

### <a name="combine-with-calendars" />Mit Kalendern kombinieren

Bevor ein neuer Beschaffungsauftrag vorgeschlagen wird, um einen Meldebestand zu erfüllen, prüft das Planungssystem, ob der Auftrag für einen arbeitsfreien Tag geplant ist. Es verwendet die Kalender, die Sie im Feld **Basiskalendercode** in den Seiten **Unternehmensinformationen** und **Standortkarte** angegeben haben.  

Wenn das geplante Datum ein freier Tag ist, verschiebt das Planungssystem die Reihenfolge weiter zum nächsten Arbeitstag. Eine Verschiebung des Datums kann zu einem Verkaufsauftrag, der für einen Minimalbestand gilt, aber keinen bestimmten Bedarf abdeckt. Bei solcher Nachfrage ohne Bedarf erstellt das Planungssystem ein zusätzlicher Vorrat.

### <a name="order" />Bestellung

In einer Auftragsfertigungsumgebung wird ein Artikel bezogen oder gefertigt, um einen speziellen Bedarf zu decken. Üblicherweise wird das Auftragswiederbeschaffungsverfahren für Artikel mit den folgenden Merkmalen verwendet

* Nachfrage ist selten
* Die Vorlaufzeit ist unerheblich
* Erforderliche Attribute variieren  

[!INCLUDE [prod_short](includes/prod_short.md)] erstellt einen Auftrag-zu-Auftrag-Link, der als vorläufige Verbindung zwischen dem Vorrat, (einem Beschaffungsauftrag oder dem Bestand) und dem Bedarf fungiert. Sie können die Auftrag-zu-Auftrag-Verknüpfung während der Planung auf folgende Weise anwenden:  

* Bei Verwendung der Produktionsart Auftragsfertigung, um mehrstufige oder projekttypbezogene Fertigungsaufträge (Herstellung benötigter Komponenten im selben Fertigungsauftrag) zu erstellen  
* Wenn die Verkaufsauftrags-Planungsfunktion verwendet wird, um einen Fertigungsauftrag aus einem Verkaufsauftrag zu erstellen  

> [!TIP]
> Wenn Artikelattribute nicht variieren, ist es möglicherweise am besten, eine Charge-für-Charge-Nachbestellungsrichtlinie zu verwenden. Deshalb verwendet das System nicht geplanten Lagerbestand und kumuliert nur Verkaufsaufträge mit demselben Lieferdatum oder in einem definierten Zeitrahmen.  

#### <a name="order-to-order-links-and-past-due-dates" />Auftrag-zu-Auftrag-Links und überfällige Datumsangaben

Anders als die meisten Angebot-Nachfrage Datensätze werden verknüpfte Aufträge vor dem Startdatum vollständig vom System geplant. Der Grund für diese Ausnahme ist, dass bestimmte Bedarf-Vorrat-Sätze synchronisiert werden müssen. Weitere Informationen zu der fixierten Zone, die für die meisten Bedarf-Vorrat-Typen gilt, finden Sie unter [Aufträge vor dem Planungsstartdatum verarbeiten](design-details-balancing-demand-and-supply.md#process-orders-before-the-planning-start-date).

### <a name="lot-for-lot" />Los-für-Los

Die Charge-für-Charge-Richtlinie ist am flexibelsten, da das System nur auf die tatsächliche Nachfrage reagiert. Es reagiert auf den erwarteten Bedarf aus Prognose- und Rahmenaufträgen und rechnet dann die Auftragsmenge basierend auf dem Bedarf ab. Die Charge-für-Charge-Richtlinie gilt für Artikel, bei denen der bestand angenommen werden kann, jedoch vermieden werden sollte.  

In mancher Hinsicht ähnelt die Charge-für-Charge-Richtlinie der Auftragsrichtlinie, hat aber einen generischen Ansatz für Artikel. Sie kann Bestandsmengen aufnehmen und Angebot und Nachfrage in den von Ihnen definierten Zeitrahmen bündeln.  

Sie geben den Zeitrahmen im Feld **Zeitrahmen** auf der Seite **Artikelkarte** an. Die Mindestgröße des Zeitrahmens ist ein Tag, da dies die kleinste Zeiteinheit für Bedarfs- und Versorgungsereignisse in [!INCLUDE [prod_short](includes/prod_short.md)] ist.  

Das Zeitrahmen legt auch Grenzen dafür fest, wann Sie einen Beschaffungsauftrag umplanen sollten, um einen angegebenen Bedarf zu erfüllen. Der Vorrat innerhalb des Zeitrahmens, wird ein- oder ausgeplant, um den Bedarf zu erfüllen. Eine frühere Lieferung führt zu zusätzlichem Lagerbestand, und Sie sollten sie stornieren. Für spätere Lieferungen erstellen Sie einen neuen Lieferauftrag.  

Mit dieser Richtlinie können Sie einen Sicherheitsbestand festlegen, um Angebotsänderungen auszugleichen oder einen plötzlichen Bedarf zu decken.  

Da die Beschaffungsauftragsmenge auf dem tatsächlichen Bedarf basiert, kann es sinnvoll sein, die Auftragsmodifikatoren zu verwenden:

* Aufrunden der Bestellmenge auf ein Bestellvielfaches (oder Einkaufsmengeneinheit)
* Erhöhen Sie die Bestellung auf eine angegebene Mindestbestellmenge
* Reduzieren Sie die Menge auf die angegebene Maximalmenge (und erstellen Sie damit zwei oder mehr Lieferungen, um die erforderliche Gesamtmenge zu erreichen)

## <a name="see-also" />Weitere Informationen

[Designdetails: Planungsparameter](design-details-planning-parameters.md)  
[Designdetails: Planungs-Zuordnungstabelle](design-details-planning-assignment-table.md)  
[Designdetails: Zentrale Konzepte des Planungssystems](design-details-central-concepts-of-the-planning-system.md)  
[Designdetails: Ausgleich von Bedarf und Vorrat](design-details-balancing-demand-and-supply.md)  
[Designdetails: Vorratsplanung](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
