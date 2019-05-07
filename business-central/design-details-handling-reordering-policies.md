---
title: Designdetails - Abwicklung on Wiederbeschaffungsrichtlinien | Microsoft Docs
description: Übersicht über Aufgaben für das Definieren einer Wiederbestellungsrichtlinie in die Beschaffungsplanung.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 69f9f1f2f63e1d16ec1ef4980c00d21bada06166
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "928602"
---
# <a name="design-details-handling-reordering-policies"></a>Designdetails: Umgang mit Wiederbeschaffungsrichtlinien
Damit ein Artikel an der Beschaffungsplanung teilnehmen kann, muss eine Wiederbeschaffungsrichtlinie festgelegt werden. Die folgenden vier Wiederbeschaffungsrichtlinien sind verfügbar:  

* Feste Bestellmenge  
* Auffüllen auf Maximalbestand  
* Bestellung  
* Los-für-Los  

Feste Bestellmenge und Höchstmenge, Richtlinien für die Bestandsplanung. Obwohl die Bestandsplanung eigentlich einfacher als das Ausgleichsverfahren ist, müssen diese Richtlinien gemeinsam mit dem schrittweisen Ausgleich der Nachverfolgung von Vorrat und Bedarf bestehen. Um die Integration zwischen den beiden zu steuern, und Einsehbarkeit in die beteiligte Planungslogik bereitzustellen, steuern strenge Prinzipien, wie Wiederbeschaffungsverfahren angewendet werden.  

## <a name="the-role-of-the-reorder-point"></a>Die Rolle des Meldebestands
Zusätzlich zur allgemeinen Anpassung von Angebot und Nachfrage muss das Planungssystem auch Lagerbestände für die betroffenen Artikel überwachen, um die definierten Wiederbeschaffungsverfahren zu berücksichtigen.  

Ein Minimalbestand repräsentiert den Bedarf während der Beschaffungszeit. Wenn die Durchläufe des voraussichtlichen Lagerstatus unter den Lagerbestand gerät, der durch den Minimalbestand definiert ist, muss eine größere Menge bestellt werden. Unterdessen schrumpft der Lagerbestand erfahrungsgemäß schrittweise und erreicht wahrscheinlich den Punkt Null (oder den Sicherheitsbestand), bis der Vorrat aufgestockt wird.  

Entsprechend schlägt das Planungssystem einen vorwärtsgeplanten Beschaffungsauftrag an dem Zeitpunkt vor, an dem der geplante Bestand unter den Minimalbestand sinkt.  

Der Minimalbestand reflektiert einen bestimmten Lagerbestand. Allerdings können sich Lagerbestände während des Zeitrahmens erheblich ändern, daher muss das Planungssystem ständig den voraussichtlich verfügbaren Lagerbestand überwachen.

## <a name="monitoring-the-projected-inventory-level-and-the-reorder-point"></a>Überwachen der voraussichtliche Lagerebene und Meldebestand
Der Bestand ist eine Art Vorrat, jedoch für Bestandsplanung unterscheidet das Planungssystem zwischen zwei Bestandsebenen:  

* Voraussichtlicher Lagerbestand  
* Voraussichtlich verfügbarer Lagerbestand  

### <a name="projected-inventory"></a>Voraussichtlicher Lagerbestand  
Zuerst ist der voraussichtliche Lagerbestand die Menge des Bruttobestands, einschließlich Vorrat und Bedarf in der Vergangenheit (selbst wenn nicht gebucht), wenn der Planungsprozess gestartet wird. Zukünftig wird dies eine bewegliche Ebene des voraussichtlichen Bestands sein, die durch Brutto-Mengen aus künftigem Vorrat und Bedarf verwaltet wird, da diese entlang der Zeitachse eingeführt werden (ob reserviert oder auf andere Weise zugewiesen).  

Der voraussichtliche Lagerbestand wird vom Planungssystem verwendet, um den Minimalbestand zu überwachen und um die Wiederbeschaffungsmenge zu bestimmen, wenn die Wiederbeschaffungsrichtlinie „Höchstmenge“ verwendet wird.  

### <a name="projected-available-inventory"></a>Voraussichtlich verfügbarer Lagerbestand  
Der voraussichtlich verfügbare Lagerbestand ist Teil des voraussichtlichen Bestands, der zu einem bestimmten Zeitpunkt verfügbar ist, um Bedarf zu erfüllen. Der voraussichtlich verfügbare Lagerbestand wird vom Planungsmodul verwendet, wenn die Sicherheitsbestandsebene überwacht wird.  

Der voraussichtlich verfügbare Lagerbestand wird vom Planungssystem verwendet, um die Sicherheitsbestandsebene zu überwachen, da der Sicherheitsbestand immer verfügbar sein muss, um unerwarteten Bedarf zu erfüllen.  

### <a name="time-buckets"></a>Zeitrahmen  
Eine strenge Kontrolle des voraussichtlichen Lagerbestands ist entscheidend, um zu ermitteln, wann der Minimalbestand erreicht ist oder unterschritten wurde, und wie die richtige Auftragsmenge berechnet wird, wenn das Wiederbeschaffungsverfahren „Höchstmenge“ verwendet wird.  

Wie zuvor angegeben, wird der voraussichtliche Lagerbestand am Anfang der Planungsperiode berechnet. Dies ist eine grobe Ebene, bei der Reservierungen und ähnliche Zuordnungen nicht berücksichtigt werden. Um dieses Lagerbestandsniveau während der Planungssequenz zu überwachen, überwacht das System die aggregierten Änderungen über eine Zeitperiode, einen Zeitrahmen hinweg. Die Anwendung stellt sicher, dass der Zeitrahmen mindestens ein Tag ist, da dies die präziseste Zeiteinheit für ein Bedarfs- oder ein Vorratsereignis ist.  

### <a name="determining-the-projected-inventory-level"></a>Bestimmen des voraussichtlichen Lagerbestands  
Die folgende Sequenz beschreibt, wie der voraussichtliche Lagerbestand bestimmt wird:  

* Wenn ein Vorratsereignis, wie eine Bestellung, vollständig geplant wurde, erhöht es den voraussichtlichen Lagerbestand am Fälligkeitsdatum.  
* Wenn ein Nachfrageereignis vollständig erfüllt wurde, verringert es nicht sofort den voraussichtlichen Lagerbestand. Stattdessen bucht es eine Minderungserinnerung, die ein interner Datensatz ist, der das Datum und die Menge des Beitrags zum voraussichtlichen Lagerbestand beinhaltet.  
* Wenn ein folgendes Vorratsereignis auf die Zeitachse geplant und auf die Zeitachse platziert wird, werden die gebuchten Abgangsmahnungen beim Aktualisieren des voraussichtlichen Lagerstatus einzeln bis zum geplanten Datum der Lieferung überprüft. Während dieses Prozesses kann der Minimalbestand der internen Zunahmeerinnerung erreicht oder unterschritten werden.  
* Wenn ein neuer Beschaffungsauftrag eingegeben wird, prüft die Anwendung, ob dieser vor dem aktuellen Vorrat eingegeben wird. Wenn dies der Fall ist, wird der neue Vorrat zum aktuellen Vorrat, und der Ausgleichsvorgang beginnt erneut.  

Nachfolgend wird eine graphische Illustration dieses Prinzips gezeigt:  

![Die voraussichtliche Lagerstatusebene bestimmen](media/nav_app_supply_planning_2_projected_inventory.png "Die voraussichtliche Lagerstatusebene bestimmen")  

1. Vorrat **Sa** von 4 (fest) schließt Bedarf **Da** von -3.  
2. CloseDemand: Erstellen Sie eine Minderungserinnerung von -3 (nicht angezeigt).  
3. Vorrat **Sa** wird mit einem Überschuss von 1 geschlossen (kein Bedarf mehr vorhanden).  

     Dadurch wird der voraussichtliche Lagerbestand auf +4 angehoben, während der voraussichtliche **verfügbare** Lagferbestand -1 wird.  

4. Der nächste Vorrat **Sb** von 2 (ein anderer Auftrag) wurdet bereits in die Zeitachse platziert.  
5. Das System prüft, ob es eine Minderungserinnerung gibt, die **Sb** vorangeht (dies ist nicht der Fall, daher keine Aktion).  
6. Das System schließt Vorrat **Sb** (kein Bedarf mehr vorhanden) - entweder A: durch Reduzierung auf 0 (Stornieren) oder B: durch unverändert lassen.  

     Dadurch wird der voraussichtliche Lagerbestand erhöht (A: +0 => +4 oder B: +2 = +6).  

7. Das System führt eine abschließende Prüfung durch: Gibt es eine Minderungserinnerung? Ja, es gibt eine am Datum **Da**  
8. Die Anwendung fügt die Minderungserinnerung -3 in der Ebene des voraussichtlichen Lagerbestands hinzu, entweder A: +4 -3 = 1 oder B: +6 -3 = +3.  
9. Im Falle von A erstellt das System eine vorausplanende Bestellung ab Datum **Da**.  

     Im Falle von B wird der Minimalbestand erreicht, und es wird ein neuer Auftrag erstellt.

## <a name="the-role-of-the-time-bucket"></a>Die Rolle des Zeitrahmen
Der Zweck dieses Zeitrahmens ist es, Bedarfsereignisse innerhalb des Zeitfensters zu erfassen, um einen gemeinsamen Beschaffungsauftrag zu erstellen.  

Für Wiederbeschaffungsverfahren, die einen Minimalbestand verwenden, können Sie einen Zeitrahmen definieren. Dadurch ist sichergestellt, dass Bedarf innerhalb derselben Periode kumuliert wird, bevor die Auswirkungen auf den voraussichtlichen Lagerbestand geprüft werden, und ob der Minimalbestand unterschritten wurde. Wenn der Minimalbestand überschritten wird, wird ein neuer Beschaffungsauftrag vom Ende der durch den Zeitrahmen definierten Periode vorwärts geplant. Der Zeitrahmen beginnt am geplanten Startdatum.  

Der Zeitrahmenkonzept spiegelt den manuellen Vorgang des Überprüfens des Lagerbestands auf häufiger Basis anstatt für jede Transaktion. Die Anwender muss die Häufigkeit (den Zeitrahmen) festlegen. Beispielsweise erfasst der Benutzer alle Artikelanforderungen von einem Kreditor, um einen wöchentlichen Auftrag zu platzieren.  

![Beispiel des Zeitrahmens in der Planung](media/nav_app_supply_planning_2_reorder_cycle.png "Beispiel des Zeitrahmens in der Planung")  

Das Zeitrahmen wird im Allgemeinen verwendet, um einen Kaskadeneffekt zu vermeiden. Zum Beispiel eine eine ausgeglichene Zeile von Bedarf und Vorrat, bei der ein frühzeitiger Bedarf storniert oder ein neuer Bedarf erstellt wird. Das Ergebnis würde sein, dass jeder Beschaffungsauftrag (mit Ausnahme des letzten) umgeplant würde.

## <a name="staying-under-the-overflow-level"></a>Unter dem Überlauflevel bleiben
Wenn die Funktionen Auffüllen auf Maximalbestand Feste Bestellmenge verwendet werden, konzentriert sich das Planungssystem nur auf den voraussichtlichen Lagerbestand in dem vorgegebenen Zeitrahmen. Dies bedeutet, dass das Planungssystem möglicherweise überflüssigen Vorrat vorschlägt, wenn negativer Bedarfs- oder positive Vorratsänderungen außerhalb gegebenen Zeitrahmens auftreten. Wenn aus diesem Grund ein überflüssiger Vorrat vorgeschlagen wird, berechnet das Planungssystem die zu reduzierende oder zu löschende Vorratsmenge, um überflüssigen Vorrat zu vermeiden. Diese Menge wird als "Überlauflevel" bezeichnet. Diese Menge wird als "Überlauflevel" bezeichnet. Der Überlauf wird als Planungszeile mit einer **Menge ändern** oder **Abbrechen** Operation und der folgenden Warnmeldung mitgeteilt:  

*Achtung: Der voraussichtliche Lagerbestand [xx] ist höher als das Überlauflevel [xx] am Fälligkeitsdatum [xx].*  

![Lagerüberlauflevel](media/supplyplanning_2_overflow1_new.png "Lagerüberlauflevel")  

###  <a name="calculating-the-overflow-level"></a>Berechnung des Überlauflevels  
Das Überlauflevel wird auf verschiedene Arten abhängig vom Planungssetup berechnet.  

#### <a name="maximum-qty-reordering-policy"></a>Auffüllen auf Maximalbestand. Wiederbeschaffungsverfahren  
Überlauflevel = Maximalbestand  

> [!NOTE]  
>  Wenn eine Auftragsmindestmenge existiert, wird sie wie folgt hinzugefügt: Überlauflevel-= Maximalbestand-+ Auftragsmindestmenge.  

#### <a name="fixed-reorder-qty-reordering-policy"></a>Nachbestellungsrichtlinie Feste Bestellmenge  
Überlauflevel = Bestellmenge + Minimalbestand  

> [!NOTE]  
>  Wenn die Mindestauftragsgröße höher als der Minimalbestand ist, dann werden folgende Ersetzungen vorgenommen: Überlauflevel-= Bestellmenge + Mindestauftragsgröße  

#### <a name="order-multiple"></a>Losgrößenrundungsfaktor  
Wenn ein Auftragsvielfaches vorhanden ist, reguliert dieses den Überlauflevel für die Wiederbeschaffungsverfahren Höchstmenge und Feste Nachbestellmenge.  

###  <a name="creating-the-planning-line-with-overflow-warning"></a>Erstellen der Planungszeile mit Überlaufwarnmeldung  
Wenn eine vorhandene Lieferung dazu führt, dass der voraussichtliche Lagerbestand höher ist, als das Überlauflevel am Ende eines Zeitrahmens höher, wird eine Planungszeile erstellt. Um vor einem möglichen überflüssigen Vorrat zu warnen, hat die Planungszeile eine Warnmeldung, das Feld **Ereignismeldung akzeptieren** ist nicht aktiviert, und die Ereignismeldung ist entweder "Abbrechen" oder "Menge ändern".  

#### <a name="calculating-the-planning-line-quantity"></a>Berechnen der Planungszeilenmenge  
Planungszeilen-Menge = Netzstrom-Menge - (voraussichtlicher Lagerbestand - Überlauflevel)  

> [!NOTE]  
>  Wie bei allen Hinweiszeilen werden alle Max./Min.-Auftragsmengen oder Auftragsvielfache ignoriert.  

#### <a name="defining-the-action-message-type"></a>Definieren des Aktionsmeldungstyps  

-   Wenn die Planungszeilenmenge höher als 0 ist, ist die Aktionsmeldung „Menge ändern“.  
-   Wenn die Planungszeilenmenge gleich oder niedriger als 0 ist, ist die Aktionsmeldung „Stornieren“.  

#### <a name="composing-the-warning-message"></a>Verfassen der Warnmeldung  
Im Falle eines Überlaufs zeigt die Seite  **Planungselement ohne Nachverfolgung** eine Warnmeldung mit den folgenden Informationen an:  

-   Der voraussichtliche Lagerbestand, der die Warnung ausgelöst hat.  
-   Der berechnete Überlauflevel  
-   Das Fälligkeitsdatum des Vorratsereignisses.  

Beispiel: "Der voraussichtliche Lagerbestand 120 übersteigt das Überlauflevel 60 am 28.01.11"  

### <a name="scenario"></a>Szenario  
In diesem Szenario ändert ein Debitor einen Verkaufsauftrag von 70 zu 40 Stück zwischen zwei Planungen. Die Überlauffunktion reduziert den Einkauf, der für die anfängliche Verkaufsmenge vorgeschlagen worden war.  

#### <a name="item-setup"></a>Artikeleinrichtung  

|Wiederbeschaffungsverfahren|Auffüllen auf Maximalbestand|  
|-----------------------|------------------|  
|Maximale Losgröße|100|  
|Meldebestand|50|  
|Lagerbest|80|  

#### <a name="situation-before-sales-decrease"></a>Situation vor Vertriebsabgang  

|Veranstaltung|"Menge ändern"|Voraussichtlicher Lagerbestand|  
|-----------|-----------------|-------------------------|  
|Tag eins|Keine|80|  
|Verkauf|-70|10|  
|Ende des Zeitrahmens|Keine|10|  
|Neue Bestellung vorschlagen|+90|100|  

#### <a name="situation-after-sales-ddecrease"></a>Situation nach Vertriebsabgang  

|Ändern|"Menge ändern"|Voraussichtlicher Lagerbestand|  
|------------|-----------------|-------------------------|  
|Tag eins|Keine|80|  
|Verkauf|-40|40|  
|Einkauf|+90|130|  
|Ende des Zeitrahmens|Keine|130|  
|Vorschlagen, den Einkauf zu vermindern<br /><br /> Auftrag von 90 bis 60|-30|100|  

#### <a name="resulting-planning-lines"></a>Planzeilen erstellen  
 Eine Planungszeile (Warnen) wird erstellt, um den Einkauf mit 30 von 90 auf 60 zu verringern, um den voraussichtlichen Lagerstatus auf 100 entsprechend dem Überlauflevel festzuhalten.  

![Planung entsprechender Überlauflevel](media/nav_app_supply_planning_2_overflow2.png "Planung entsprechender Überlauflevel")  

> [!NOTE]  
>  Ohne die Sammelfunktion werden keine Warnmeldungen erstellt, wenn der voraussichtliche Lagerbestand über Maximalbestand ist. Dies kann einen überflüssigen Vorrat von 30 verursachen.

## <a name="handling-projected-negative-inventory"></a>Bestandvoraussichtlich negativ behandeln
Der Minimalbestand drückt den voraussichtlichen Bedarf während der Beschaffungszeit des Artikels aus. Wenn der Minimalbestand überschritten wird, ist es an der Zeit, mehr zu bestellen. Der voraussichtliche Lagerbestand muss jedoch groß genug sein, um den Bedarf zu decken, bis der neue Auftrag eingegangen ist. Unterdessen gleicht der Sicherheitsbestand Schwankungen im Bedarf bis zu einem anvisierten Servicelevel aus.  

 Deshalb betrachtet das Planungssystem es als einen Notfall, wenn ein zukünftiger Bedarf nicht aus dem voraussichtlichen Lagerbestand abgedeckt werden kann, oder anders ausgedrückt: wenn der voraussichtliche Lagerbestand negativ wird. Die Anwendung behandelt eine solche Ausnahme, indem es einen neuen Beschaffungsauftrag vorschlägt, um den Teil des Bedarf einzuhalten, der nicht durch Lagerbestand oder anderen Vorrat befriedigt werden kann. Die Auftragsgröße des neuen Beschaffungsauftrags berücksichtigt nicht den Höchstbestand oder die Wiederbeschaffungsmenge, und auch nicht die Auftragsmodifikatoren maximale Auftragsmenge, minimale Auftragsmenge und Auftragsvielfaches. Stattdessen spiegelt sie den genauen Mangel wider.  

 Die Planungszeile für diese Art von Beschaffungsauftrag zeigt ein Notwarnsymbol an , und zusätzliche Informationen werden beim Lookup angezeigt, um den Benutzer über die Situation zu informieren..  

 In der folgenden Abbildung zeigt Vorrat D eine Notfallbestellung an, um negativen Bestand auszugleichen.  

 ![Notfallplanungsvorschlag, verhindern von negativem Lagerbestand](media/nav_app_supply_planning_2_negative_inventory.png "Notfallplanungsvorschlag, verhindern von negativem Lagerbestand")  

1.  Vorrat **A** anfänglicher voraussichtlicher Lagerbestand, liegt unter Minimalbestand.  
2.  Ein neuer voraus geplanter Vorrat wurde erstellt (**C**).  

     (Menge = Maximalbestand - Voraussichtlicher Lagerbestand)  
3.  Vorrat **A** wird durch Bedarf **B** geschlossen, der nicht vollständig abgedeckt wird.  

     (Bedarf **B** könnte versuchen, Zubehör C einzuplanen, dies erfolgt jedoch nicht aufgrund des Zeitrahmenkonzepts.)  
4.  Neuer Vorrat (**D**) wird erstellt, um die Restmenge auf Anfordung **B** zu decken.  
5.  Bedarf **B** ist geschlossen (eine Erinnerung für den voraussichtlichen Lagerbestand wird erstellt).  
6.  Das neue Vorrat **D** wird geschlossen.  
7.  Voraussichtlicher Lagerbestand wird geprüft; Minimalbestand wurde nicht überschritten.  
8.  Vorrat **C** ist geschlossen (kein Bedarf mehr vorhanden).  
9. Abschließende Prüfung: Keine ausstehenden Erinnerungen auf Bestandsebene sind vorhanden.  

> [!NOTE]  
>  Schritt 4 zeigt, wie das System in Versionen vor Microsoft Dynamics NAV 2009 SP1 reagiert.  

Damit ist die Beschreibung der zentralen Prinzipien in Bezug auf Bestandsplanung basierend auf Wiederbeschaffungsverfahren abgeschlossen. Im nächsten Abschnitt werden die Eigenschaften der vier unterstützten Wiederbeschaffungsrichtlinien beschrieben.

## <a name="reordering-policies"></a>Wiederbeschaffungsverfahren
Wiederbeschaffungsrichtlinien definieren, wie viel zu bestellen ist, wenn der Artikel aufgefüllt werden muss. Es gibt verschiedene Wiederbeschaffungsverfahren.  

### <a name="fixed-reorder-qty"></a>Feste Bestellmenge
Das Richtlinie „Feste Bestellmenge“ bezieht sich auf die Bestandsplanung typischer C-Artikel (niedrige Bestandskosten, geringes Veraltungsrisiko und/oder zahlreiche Artikel). Diese Methode wird normalerweise in Verbindung mit einem Minimalbestand verwendet, der den voraussichtlichen Bedarf während der Beschaffungszeit des Artikels angezeigt.  

#### <a name="calculated-per-time-bucket"></a>Berechnet pro Zeitrahmen  
Wenn das Planungssystem erkennt, dass der Minimalbestand einen bestimmten Zeitrahmen (Nachbestellungszyklus) erreicht oder unterschritten hat – oberhalb oder am Minimalbestand am Beginn der Periode bzw. unter oder am Minimalbestand am Ende der Periode –, schlägt es vor, einen neuen Beschaffungsauftrag mit der angegebenen Bestellmenge zu erstellen und ihn vorwärts vom ersten Datum des Endes des Zeitrahmens an zu planen.  

Das Konzept des Minimalbestands im Zeitrahmen reduziert reduziert die Anzahl der Beschaffungsvorschläge. Dieses spiegelt einen manuellen Vorgang des häufigen Durchgangs durch das Lager wirder, um die tatsächlichen Inhalte in den unterschiedlichen Lagerplätzen zu prüfen.  

#### <a name="creates-only-necessary-supply"></a>Erstellt nur erforderlichen Vorrat  
Bevor ein neuer Beschaffungsauftrag gemacht wird, um einen Minimalbestand einzuhalten, prüft das Planungssystem, ob Vorrat bereits bestellt wurde, um innerhalb der Vorlaufzeit des Artikels einzugehen. Wenn ein vorhandener Beschaffungsauftrag das Problem löst, indem er den voraussichtlichen Lagerbestand auf oder über den Minimalbestand innerhalb der Beschaffungszeit bringt, schlägt die Anwendung keinen neuen Beschaffungsauftrag vor.  

Beschaffungsaufträge, die speziell erstellt werden, um einen Minimalbestand zu erfüllen, werden aus dem normalen Vorratsausgleich ausgeschlossen und werden auch nachher in keiner Weise geändert. Deshalb gilt: Wenn ein Artikel mithilfe des Minimalbestands abgewickelt werden soll (d.h. nicht mehr aufgefüllt wird), sollten Sie ausstehende Beschaffungsaufträge manuell überprüfen oder die Wiederbeschaffungsrichtlinie Charge für Charge ändern, wodurch das System überflüssigen Vorrat reduziert oder storniert.  

#### <a name="combines-with-order-modifiers"></a>Wird mit anderen Auftragsmodifizierern kombiniert  
Die Auftragsmodifikatoren minimale Auftragsmenge, maximale Auftragsmenge und Auftragsvielfaches sollten keine große Rolle spielen, wenn die feste Nachbestellungsmengenrichtlinie verwendet wird. Das Planungssystem berücksichtigt jedoch diese Modifizierer und vermindert die Menge auf die angegebene Auftragshöchstmenge (und erstellt zwei oder mehr Vorräte, um die Gesamtauftragsmenge zu erreichen), erhöht den Auftrag auf die angegebene Auftragsmindestmenge oder rundet die Auftragsmenge auf, um ein angegebenes Auftragsvielfaches zu erreichen.  

#### <a name="combines-with-calendars"></a>Zusammenfassen mit Kalendern  
Bevor ein neuer Beschaffungsauftrag vorgeschlagen wird, einen Minimalbestand einzuhalten, überprüft das Planungssystem, ob der Auftrag für einen nicht freien Tag entsprechend dem Kalender geplant ist, die im Feld **Basiskalendercode** auf den Seiten **Firmendaten** und **Lagerortkarten** festgelegt werden.  

Wenn das geplante Datum ein freier Tag ist, verschiebt das Planungssystem die Reihenfolge weiter zum nächsten Arbeitsdatum. Dadurch ergeben sich möglicherweise ein Verkaufsauftrag, der für einen Minimalbestand gilt, aber keinen bestimmten Bedarf abdeckt. Bei solcher Nachfrage ohne Bedarf erstellt das Planungssystem ein zusätzlicher Vorrat.  

#### <a name="should-not-be-used-with-forecast"></a>Sollte nicht mit Planung verwendet werden  
Da der erwartete Bedarf bereits in der Minimalbestandsebene angegeben wird, ist es nicht notwendig, eine Prognose in die Planung eines Artikels mit einem Minimalbestand zu berücksichtigen. Wenn es wichtig ist, den Plan auf einer Planung zu basieren, verwenden Sie die Charge-für-Charge-Richtlinie.  

#### <a name="must-not-be-used-with-reservations"></a>Darf nicht mit Reservierungen verwendet werden  
Wenn der Benutzer eine Menge, etwa eine Menge im Bestand, für einen späteren Bedarf reserviert hat, ist die Grundlage der Planung gestört. Selbst wenn der voraussichtliche Lagerbestand im Hinblick auf den Minimalbestand akzeptabel ist, stehen die Mengen möglicherweise aufgrund der Reservierung nicht zur Verfügung. Die Anwendung versucht möglicherweise, dies auszugleichen, indem es Ausnahmeaufträge erstellt; jedoch empfiehlt es sich, dass das Reservefeld für Artikel, die unter Verwendung eines Minimalbestands geplant werden, auf Nie festgelegt wird.

### <a name="maximum-qty"></a>Auffüllen auf Maximalbestand
Die Richtlinie der maximalen Menge ist eine Möglichkeit zur Verwaltung des Bestands anhand eines Minimalbestands.  

Alles im Zusammenhang mit der festen Bestellmengenrichtlinie bezieht sich auch auf diese Richtlinie. Der einzige Unterschied ist die Menge des vorgeschlagenen Vorrats. Wenn Sie die Methode Auffüllen auf Maximalbestand verwenden, erfolgt die Definition der Bestellmenge dynamisch auf Basis des voraussichtlichen Lagerbestandes und unterscheidet sich daher normalerweise von Auftrag zu Auftrag.  

#### <a name="calculated-per-time-bucket"></a>Berechnet pro Zeitrahmen  
Die Nachbestellungsmenge wird zu dem Zeitpunkt bestimmt (am Ende eines Zeitrahmens), wenn das Planungssystem erkennt, dass der Minimalbestand überschritten wurde. Zu diesem Zeitpunkt misst das System die Lücke von der aktuellen Stufe des voraussichtlichen Lagerbestands bis zum angegebenen Maximalbestand. Dies bildet die Menge, die wiederbestellt werden soll. Die Anwendung überprüft dann, ob Vorrat bereits anderswo bestellt worden, um innerhalb der Beschaffungszeit erhalten zu werden, und falls ja, reduziert es die Menge des neuen Beschaffungsauftrags um bereits bestellte Mengen.  

Die Anwendung stellt sicher, dass der voraussichtliche Lagerbestand mindestens die Minimalbestandsebene erreicht - falls der Benutzer vergessen hat, eine maximale Lagerbestandsmenge anzugeben.  

#### <a name="combines-with-order-modifiers"></a>Wird mit anderen Auftragsmodifizierern kombiniert  
Abhängig von den Einstellungen kann es am besten sein, die Methode „Maximale Menge“ mit Auftragsmodifikationen zu kombinieren, um eine Mindestauftragsmenge sicherzustellen, oder sie auf eine ganze Zahl von Einkaufsmengeneinheiten zu runden, bzw. sie in mehrere Chargen aufzuteilen, wie von der maximalen Auftragsmenge definiert.  

### <a name="combines-with-calendars"></a>Zusammenfassen mit Kalendern  
Bevor ein neuer Beschaffungsauftrag vorgeschlagen wird, einen Minimalbestand einzuhalten, überprüft das Planungssystem, ob der Auftrag für einen nicht freien Tag entsprechend dem Kalender geplant ist, die im Feld **Basiskalendercode** auf den Seiten **Firmendaten** und **Lagerortkarten** festgelegt werden.  

Wenn das geplante Datum ein freier Tag ist, verschiebt das Planungssystem die Reihenfolge weiter zum nächsten Arbeitsdatum. Dadurch ergeben sich möglicherweise ein Verkaufsauftrag, der für einen Minimalbestand gilt, aber keinen bestimmten Bedarf abdeckt. Bei solcher Nachfrage ohne Bedarf erstellt das Planungssystem ein zusätzlicher Vorrat.

### <a name="order"></a>Bestellung
In einer Auftragsfertigungsumgebung wird ein Artikel bezogen oder gefertigt, um einen speziellen Bedarf zu decken. Normalerweise bezieht sich dies auf A-Artikel, und die Motivation für die Auswahl des Auftragswiederbeschaffungsverfahrens kann es sein, dass der Bedarf selten ist, die Vorbereitungszeit unbedeutend ist, oder die erforderlichen Attribute variieren können.  

Das Programm erstellt einen Auftrag-zu-Auftrag-Link, der als vorläufige Verbindung zwischen dem Vorrat, einem Beschaffungsauftrag oder dem Bestand und dem bedarf, der erfüllt werden soll, fungiert.  

Abgesehen von der Verwendung der Auftragsrichtlinie, kann die Auftrag-zu-Auftragverknüpfung in folgender Weise verwendet werden:  

* Bei Verwendung der Produktionsart "Auftragsfertigung", um mehrstufige oder projekttypbezogene Fertigungsaufträge (Herstellung benötigter Komponenten im selben Fertigungsauftrag) zu erstellen.  
* Wenn die Verkaufsauftrags-Planungsfunktion verwendet wird, um einen Fertigungsauftrag aus einem Verkaufsauftrag zu erstellen.  

Selbst wenn ein Produktionsbetrieb sich als Auftragsfertigungsumgebung sieht, kann es am besten sein, ein Charge-für-Charge-Wiederbeschaffungsverfahren zu verwenden, wenn der Artikel reiner Standard ohne Variation der Attribute ist. Deshalb verwendet das System nicht geplanten Lagerbestand und kumuliert nur Verkaufsaufträge mit demselben Lieferdatum oder in einem definierten Zeitrahmen.  

#### <a name="order-to-order-links-and-past-due-dates"></a>Auftrag-zu-Auftrag-Links und überfällige Datumsangaben  
Anders als die meisten Angebot-Nachfrage Datensätze werden verknüpfte Aufträge vor dem Startdatum vollständig vom System geplant. Der Geschäftsgrund für diese Ausnahme ist, dass bestimmte Bedarf-Vorrat-Sätze bis zur Ausführung synchronisiert werden müssen. Weitere Informationen zu der fixierten Zone, die für die meisten Bedarf-Vorrat-Typen gilt, finden Sie unter [Designdetails: Abwicklung von Aufträgen vor dem Planungs-Startdatum](design-details-dealing-with-orders-before-the-planning-starting-date.md).

### <a name="lot-for-lot"></a>Los-für-Los
Die Charge-für-Charge-Richtlinie ist die flexibelste, da das System nur auf tatsächlichen Bedarf reagiert; dazu reagiert sie auf voraussichtlichen Bedarf aus der Planung und auf Rahmenaufträge und gleicht die Auftragsmenge auf der Grundlage des Bedarfs ab. Die Charge-für-Charge-Richtlinie bezieht sich auf A- und B-Artikel, bei denen der bestand angenommen werden kann, jedoch vermieden werden sollte.  

In mancher Hinsicht sieht die Charge-für-Charge-Richtlinie wie die Auftragsrichtlinie aus, sie verfolgt jedoch einen generischen Ansatz für Artikel; sie kann Mengen im Bestand akzeptieren und bündelt Bedarf und den entsprechenden Vorrat in Zeitrahmen, die vom Benutzer definiert werden.  

Das Zeitrahmen wird im Feld **Zeitrahmen** definiert. Die Anwendung arbeitet mit einem minimale Zeitrahmen von einem Tag, da dies die kleinste Zeiteinheit bei Bedarfs- und Vorratsereignissen im System ist (obwohl in der Praxis die Zeiteinheit in Fertigungsaufträgen und Komponentenbedarfen Sekunden sein kann).  

Das Zeitrahmen legt auch Grenzen dafür fest, wann ein vorhandener Beschaffungsauftrag umgeplant werden soll, um einen angegebenen Bedarf zu erfüllen. Wenn der Vorrat innerhalb des Zeitrahmens liegt, wird dieser ein- oder ausgeplant, um den Bedarf zu erfüllen. Wenn er jedoch vor dem Zeitrahmen liegt, verursacht er eine unnötige Anhäufung des Lagerbestandes und sollte storniert werden. Wenn es später liegt, wird stattdessen ein neuer Beschaffungsauftrag erstellt.  

Mit dieser Methode ist es möglich, einen Sicherheitsbestand festzulegen, um mögliche Schwankungen im Vorrat auszugleichen oder plötzlichen Bedarf zu decken.  

Da die Beschaffungsauftragsmenge auf dem tatsächlichen Bedarf basiert, kann es sinnvoll sein, die Auftragsmodifikationen zu verwenden: Aufrunden der Auftragsmenge, um ein angegebenes Auftragsvielfaches zu erreichen (oder eine Einkaufsmengeneinheit), Erhöhen der Auftragsmenge auf eine angegebene Mindestauftragsmenge oder Vermindern der Menge auf die angegebene Auftragshöchstmenge (wodurch zwei oder mehr Vorräte zum Erreichen der insgesamt benötigten Menge erstellt werden).

## <a name="see-also"></a>Siehe auch  
[Designdetails: Planungsparameter](design-details-planning-parameters.md)   
[Designdetails: Planungs-Zuordnungstabelle](design-details-planning-assignment-table.md)   
[Designdetails: Zentrale Konzepte des Planungssystems](design-details-central-concepts-of-the-planning-system.md)   
[Designdetails: Ausgleich von Bedarf und Vorrat](design-details-balancing-demand-and-supply.md)   
[Designdetails: Vorratsplanung](design-details-supply-planning.md)
