---
title: 'Designdetails - Reservierung, Auftragsnachverfolgung und Aktionsmeldungen | Microsoft Docs'
description: Das Reservierungssystem ist umfassend und enthält auch die zusammenhängenden und parallelen Funktionen der Auftragsnachverfolgung und des Aktionsmessagings.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, replenishment, reordering'
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-reservation-order-tracking-and-action-messaging" />Designdetails: Reservierung, Auftragsnachverfolgung und Aktionsmeldungen
Das Reservierungssystem ist umfassend und enthält auch die zusammenhängenden und parallelen Funktionen der Auftragsnachverfolgung und des Aktionsmessagings.  

 Im Zentrum des Reservierungssystems steht die Verknüpfung eines Bedarfspostens und eines entsprechenden Vorratspostens, entweder durch Reservierung oder durch Bestandsnachverfolgung. Eine Reservierung ist ein vom Benutzer generierter Link, und ein Auftragsnachverfolgungsdatensatz ist ein vom System generierter Link. Eine Artikelmenge, die in das Reservierungssystem eingegeben wurde, ist entweder reserviert oder auftragsnachverfolgt, aber nicht beides gleichzeitig. Wie das System mit einem Artikel umgeht, hängt davon ab, wie es eingerichtet ist.  

 Das Reservierungssystem interagiert mit dem Planungssystem durch Erstellen von Aktionsmeldungen auf Planungszeilen während der Planungsausführung. Eine Ereignismeldung kann als Anhang zu einem Auftragsnachverfolgungsbeleg betrachtet werden. Ereignismeldungen, ob dynamisch erstellt in der Auftragsnachverfolgung oder während der Planung erstellt, sind nützliche Hilfsmittel für eine effiziente Beschaffungsplanung.  

> [!NOTE]  
>  Reservierte Mengen werden vom Planungssystem ignoriert, d. h. die feste Verknüpfung zwischen Vorrat und Bedarf kann nicht durch die Planung geändert werden.  

 Das Reservierungssystem bildet auch die strukturelle Basis für das Artikelnachverfolgungssystem. Weitere Informationen finden Sie unter [Designdetails: Artikelverfolgung](design-details-item-tracking.md).  

 <!--For more detailed information about how the reservation system works, see the _Reservation Entry Table_ white paper on [PartnerSource](https://go.microsoft.com/fwlink/?LinkId=258348).  -->

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="reservation" />Reservierung
 Eine Reservierung ist ein fester Link, der einen speziellen Bedarf und einen bestimmten Vorrat miteinander verknüpft. Diese Verknüpfung beeinflusst dirket die nächste Lagertransaktion und sorgt für die richtigen Anwendung von Artikelposten für Bewertungszwecke. Eine Reservierung setzt die Standard-Kostenberechnungsmethode eines Artikels außer Kraft. Weitere Informationen finden Sie unter [Designdetails: Artikelverfolgung](design-details-item-tracking.md).  

 Die Seite **Reservierung** ist von allen Auftragszeilen des Typs Bedarf und Vorrat aus zugänglich. auf der Seite kann der Benutzer angeben, zu welchem Bedarfs- oder Vorratsposten eine Reservierungsverknüpfung erstellt werden soll. Die Reservierung besteht aus einem Paar von Datensätzen, die dieselbe Postennummer haben. Ein Datensatz hat ein negatives Vorzeichen und verweist auf den Bedarf. Der andere Datensatz hat ein positives Vorzeichen und verweist auf den Vorrat. Diese Datensätze werden in der Tabelle **Reservierungsposten** mit Statuswert **Reservierung** gespeichert. Der Benutzer kann alle Reservierungen auf der Seite **Reservierungsposten** anzeigen.  

### <a name="offsetting-in-reservations" />Ausgleichung für Reservierungen
 Reservierungen werden gegen verfügbare Artikelmengen vorgenommen. Artikelverfügbarkeit wird wie folgt grundlegend berechnet:  

 verfügbare Menge = Bestand + geplante Zugänge - Bruttobedarf  

 Die folgende Tabelle zeigt die Details der Auftragsnetzwerkeinheiten an, die Teil der Verfügbarkeitsberechnung sind.  

||Feld in T27|Herkunftstabelle|Tabellenfilter|Quellfeld|  
|-|------------------|------------------|------------------|------------------|  
|**Lager**|Lagerbest|Artikelposten|N/Z|Menge|  
|**Geplante Zugänge**|Fest geplanter Zugang (Menge)|FA-Zeile|=Fest geplant|Restmenge (Basis)|  
|**Geplante Zugänge**|Freigegeb. FA Zugang (Menge)|FA-Zeile|=Freigegeben|Restmenge (Basis)|  
|**Geplante Zugänge**|Menge in Montageauftrag|Montagekopf|=Reihenfolge|Restmenge (Basis)|  
|**Geplante Zugänge**|Menge in Bestellung|Einkaufszeile|=Reihenfolge|Restbestellungsmenge (Basis)|  
|**Geplante Zugänge**|Umlag.-Auftrag Eingang (Menge)|Umlagerungszeile|N/Z|Restbestellungsmenge|  
|**Bruttobedarf**|Menge in Auftrag|Verkaufszeile|=Reihenfolge|Restbestellungsmenge (Basis)|  
|**Bruttobedarf**|Geplanter Bedarf (Menge)|FA-Komponente|<>Simuliert|Restmenge (Basis)|  
|**Bruttobedarf**|Menge in Montagekomponente|Montagezeile|=Reihenfolge|Restmenge (Basis)|  
|**Bruttobedarf**|Umlag.-Auftrag Ausgang (Menge)|Umlagerungszeile|N/Z|Restbestellungsmenge|  

 Weitere Informationen finden Sie unter [Designdetails: Verfügbarkeit im Lager](design-details-availability-in-the-warehouse.md).  

### <a name="manual-reservation" />manuelle Reservierung
 Wenn ein Benutzer absichtlich eine Reservierung erstellt, erhält er vollen Besitz von und Zuständigkeit für diese Artikel. Dies bedeutet, dass der Benutzer eine Reservierung auch manuell ändern oder stornieren muss. Derartige manuelle Änderungen verursachen möglicherweise automatische Änderungen der einbezogenen Reservierungen.  

 Die nachstehende Tabelle zeigt, welche Änderungen möglicherweise auftreten und wann dies der Fall sein kann:  

|Benutzeraktion|Systemreaktion|  
|-----------------|---------------------|  
|Reduzieren der reservierten Menge|Die verknüpften Mengenfelder werden entsprechend aktualisiert.|  
|Ändern von Datumsfeldern|Die verknüpften Datumsfelder werden entsprechend aktualisiert.<br /><br /> **Hinweis**: Wenn das Fälligkeitsdatum auf einem Bedarf so geändert wird, dass es dem Lieferdatum oder dem Fälligkeitsdatum des Vorrats vorangeht, wird die Reservierung storniert.|  
|Löschen des Auftrags|Die Reservierung wird abgebrochen.|  
|Ändern des Lagerorts, des Lagerplatzes, der Variante, der Seriennummer oder der Chargennummer|Die Reservierung wird abgebrochen.|  

> [!NOTE]  
>  Die Funktionalität der späten Bindung kann auch Reservierungen ändern, ohne den Benutzer zu informieren, indem sie nicht-spezifische Reservierungen von Serien- oder Chargennummern neu anordnet. Weitere Informationen finden Sie unter Designdetails: Artikelverfolgung und Reservierungen.  

### <a name="automatic-reservations" />Automatische Reservierungen
 Die Artikelkarte kann so eingerichtet werden, dass immer eine Reservierung vom Bedarf stattfindet, etwa bei Verkaufsaufträgen. In diesem Fall wird eine Reservierung gegen den Bestand, Kaufaufträge, Montageaufträge und Fertigungsaufträge vorgenommen. Eine Warnung wird ausgegeben, wenn der Vorrat nicht ausreicht.  

 Darüber hinaus werden Artikel automatisch nach verschiedenen Planungsfunktionen reserviert, um einen mit einer bestimmten Bedarfssicherung verknüpften Bedarf beizubehalten. Die Auftragsnachverfolgungsposten für solche Planungslinks enthalten **Reservierung** im Feld **Reservierungsstatus** in der Tabelle **Reservierungsposten**. Automatische Reservierungen werden in den folgenden Situationen erstellt:  

-   Ein mehrstufiger Fertigungsauftrag, in dem das Feld **Produktionsart** der betreffenden übergeordneten und untergeordneten Artikel auf **Auftragsfertigung** festgelegt wurde. Das Planungssystem erstellt Reservierungen zwischen dem übergeordneten Fertigungsauftrag und den zugrunde liegenden Fertigungsaufträgen, um sicherzustellen, dass sie zusammen verarbeitet werden. Eine solche Reservierungsbindung überschreibt die Standard-Kostenberechnungs- und -ausgleichsmethode des Artikels.  

-   Ein Produktions-, Montage- oder ein Einkaufsauftrag, in dem das Feld **Wiederbeschaffungsverfahren** des betreffenden Artikels auf **Auftrag** festgelegt wurde. Das Planungssystem erstellt Reservierungen zwischen dem Bedarf und dem geplanten Vorrat, um sicherzustellen, dass der bestimmte Vorrat erstellt wird. Weitere Informationen finden Sie unter [Auftrag](design-details-handling-reordering-policies.md#order).  

-   Ein Fertigungsauftrag, der aus einem Verkaufsauftrag mit der Funktion **Verkaufsauftragsplanung** erstellt wird, wird mit dem Verkaufsauftrag mit einer automatischen Reservierung verknüpft.  

-   Ein Montageauftrag, der automatisch für eine Verkaufsauftragszeile erstellt wurde, um die Menge im **($ T_37_900 Qty. to Assemble to Order $)** Feld abzudecken. Diese automatische Reservierung verknüpft den Verkaufsbedarf mit dem Montagezubehör, sodass Verkaufsauftragsbearbeiter den Montageartikel für den Debitor direkt anpassen und zusagen können. Darüber hinaus verknüpft die Reservierung den Montageausstoß der Verkaufsauftragszeile mit der Versandaktivität, die den Debitorenauftrag erfüllt.  

 Im Falle von nicht zugeordnetem Vorrat oder Bedarf weist das Planungssystem automatisch einen Reservierungsstatus der Art **Überschuss** zu. Dies kann sich aus Bedarf ergeben, der aufgrund von Planungsmengen oder der vom Benutzer eingegebenen Planungsparameter resultiert. Dies ist legitimer Überschuss, den das System anerkennt, und er verursacht keine Ereignismeldungen. Der Überschuss kann auch echter überschüssiger Vorrat oder nicht nachverfolgter Bedarf sein. Dies ist eine Angabe einer Ereignismeldung im Bestellungsbestand, das die Anwendung dazu veranlasst, Ereignismeldungen zu auszugeben. Beachten Sie, dass eine Ereignismeldung, die eine Änderung in der Menge vorschlägt, sich immer auf den Typ **Überschuss** bezieht. Weitere Informationen finden Sie im Abschnitt Auftragsnachverfolgung in Verkauf, Produktion und Umlagerung in diesem Thema.  

 Automatische Reservierungen, die bei der Planungsausführung erstellt werden, werden in der folgenden Weise behandelt:  

-   Sie werden auf Artikelmengen angewendet, die Teil der Verfügbarkeitsberechnung sind, wie sind manuelle Reservierungen. Weitere Informationen finden Sie im Abschnitt Ausgleich für Reservierungen dieses Themas.  

-   Sie sind in den folgenden Planungen enthalten und werden hier möglicherweise geändert, im Gegensatz zu manuell reservierten Artikeln.  

## <a name="order-tracking" />Bedarfsverursacher
 Bedarfsverursacher hilft dem Planer, einen gültigen Beschaffungsplan zu gewährleisten, indem er eine Übersicht zwischen Bedarf und Vorrat im Bestellungsbestand bereitstellt. Die Auftragsnachverfolgungsdatensätze dienen als Grundlage für die Erstellung von dynamischen Aktionsmeldungen und von Planungszeilenvorschlägen im Rahmen der Planungsausführungen.  

> [!NOTE]  
>  Das Auftragsnachverfolgungssystem gleicht verfügbaren Bestand aus, wenn Aufträge in das Auftragsnetzwerk eingegeben werden. Dies bedeutet, dass die Anwendung Aufträge nicht priorisiert, die in Bezug auf ihr Fälligkeitsdatum dringender sind. Es ist daher auf die Logik des Planungssystems oder der Klugheit des Terminplaners angewiesen, um diese Prioritäten auf eine sinnvolle Art neu anzuordnen.  

> [!NOTE]  
>  Bedarfsverursacherrichtlinie und die Funktion "Aktionsmeldungen abrufen" sind nicht mit Projekten integriert. Das bedeutet, dass der Bedarf, der mit einem Projekt verknüpft ist, nicht automatisch verfolgt wird. Da dies nicht nachverfolgt wird, könnte es dazu führen, dass eine vorhandene Auffüllung mit Projektinformationen zu einem anderen Bedarf, beispielsweise ein Auftrag, verfolgt wird. Deshalb treffen Sie möglicherweise die Situation an, in der Ihre Informationen über verfügbaren Lagerbestand nicht synchron sind.  

### <a name="the-order-network" />Das Auftragsnetzwerk
 Das Auftragsnachverfolgungssystem basiert auf dem Prinzip, das das Auftragsnetzwerk immer in einem Zustand des Gleichgewichts sein muss, in dem jeder Bedarf, der in das System eingeht, durch einen entsprechenden Vorrat ausgeglichen wird und umgekehrt. Die Anwendung stelt dies zu Verfügung, indem sie logische Verknüpfungen zwischen allen Bedarfs- und Vorratsposten im Bestellungsbestand bereitstellt.  

 Dieses Prinzip impliziert, dass eine Nachfrageänderung zu einer entsprechenden Unausgeglichenheit auf der Zugangsseite des Auftragsnetzwerks führt. Andererseits resultiert eine Angebotsänderung in einer entsprechenden Unausgeglichenheit auf der Bedarfsseite des Auftragsnetzwerks. In der Realität ist das Auftragsnetzwerk in einem Zustand konstanten Flusses, da Benutzer Aufträge eingeben, ergänzen und löschen. Bedarfsverursacher verarbeitet Aufträge dynamisch, reagiert auf jede Änderung zum Zeitpunkt ihrer Eingabe in das System ein und wird ein Teil des Auftragsnetzwerks. Sobald neue Auftragsnachverfolgungsdatensätze erstellt wurden, ist das Auftragsnetzwerk ausgeglichen, aber nur bis zur nächsten Änderung.  

 Um die Transparenz der Berechnungen im Planungssystem zu erhöhen, zeigt die Seite **Unverfolgte Planungselemente** nicht verfolgte Mengen an, die die Mengendifferenz zwischen bekanntem Bedarf und vorgeschlagenem Vorrat darstellen. Jede Zeile auf der Seite bezieht sich auf den Grund des Überschusses, wie **Rahmenauftrag**, **Sicherheitsbestands-Ebene**, **Feste Bestellmenge**, **Mindestauftragsmenge**, **Rundung** oder **Toleranz**.  

### <a name="offsetting-in-order-tracking" />Ausgleichung im Bedarfsverursacher
 Im Gegensatz zu Reservierungen, die nur gegen verfügbare Artikelmengen vorgenommen werden können, ist die Auftragsnachverfolgung gegen alle Auftragsnetzwerkeinheiten möglich, die Teil der Nettobedarfsrechnung des Planungssystems sind. Der Nettobedarf wird wie folgt berechnet:  

 Nettobedarf = Bruttobedarf + Minimalbestand - Geplante Zugänge - voraussichtliche Zugänge - Verfügbarkeitssaldo  

> [!NOTE]  
>  Bedarf, der mit Planungen oder Planungsparametern verbunden ist, wird nicht nach Auftrag nachverfolgt.  

### <a name="example-order-tracking-in-sales-production-and-transfers" />Beispiel: Auftragsnachverfolgung im Verkauf, in der Produktion und bei Umlagerungen
 Das folgende Szenario zeigt, welche Auftragsnachverfolgungsposten in der Tabelle **Reservierungsposten** als Ergebnis verschiedener Auftragsnetzwerkänderungen erstellt werden.  

 Gehen wir von den folgenden Daten für zwei Artikel aus, die für die Auftragsnachverfolgung eingerichtet wurden.  

|Artikel 1|Name|Komponente|
|-|-|-|
||Verfügbarkeit|100 Einheiten am Lagerort WEST<br /><br />- 30 Einheiten LOTA<br />- 70 Einheiten LOTB|  
|Artikel 2|Name|Fertigungsartikel|
||Fertigungsstückliste|1 Menge pro v. Komponente|  
||Bedarf|Verkauf für 100 Einheiten am Lagerort OST|  
||Vorrat|Freigegebener Fertigungsauftrag (generiert mit der Funktion **Verkaufsauftragsplanung** für den Verkauf von 100 Stück)|  

Auf der Seite **Produktion Einrichtung** wird das Feld **Komponenten von Lagerort** auf **ROT** festgelegt.

 Die folgenden Auftragsnachverfolgungsposten sind in der Tabelle **Reservierungsposten** enthalten, basierend auf den Daten in der Tabelle.  

 ![Erstes Beispiel für Auftragsverfolgungseinträge in der Tabelle Reservierungseintrag.](media/supply_planning_RTAM_1.png "supply_planning_RTAM_1")  

### <a name="entry-numbers-8-and-9" />Eintragsnummern 8 und 9
 Für den Komponentenbedarf für LOTA und LOTB werden Auftragsnachverfolgungslinks aus dem Bedarf in Tabelle 5407, **Fert. Auftrags-Komponente**, für den Vorrat in Tabelle 32, **Artikelposten**, erstellt. Das Feld **Reservierungsstatus** enthält **Nachverfolgung**, um anzugeben, dass diese Posten dynamische Auftragsnachverfolgungslinks zwischen Vorrat und Bedarf sind.  

> [!NOTE]  
>  Das Feld **Chargennr.** ist auf den Bedarfszeilen leer, da die Chargennummern nicht auf den Komponentenzeilen des freigegebenen Fertigungsauftrags angegeben sind.  

### <a name="entry-numbers-10" />Postennummern 10
 Vom Verkaufsbedarf in Tabelle 37, **Verkaufszeile**, wird ein Auftragsnachverfolgungslink zum Vorrat in Tabelle 5406, **Fert. Auftragszeile**, erstellt. Das Feld **Reservierungsstatus** enthält **Reservierung**, und das Feld **Verknüpfung** enthält **Eins-zu-Eins**. Dies liegt daran, dass der freigegebene Fertigungsauftrag speziell für den Verkaufsauftrag generiert wurde und anders als Bedarfsverursacherverknüpfungen in einem Reservierungsstatus **Bedarfsverursacher** bleiben muss, der dynamisch erstellt und geändert wird. Weitere Informationen finden Sie im Abschnitt Automatische Reservierungen dieses Themas.  

 An diesem Punkt im Szenario werden die 100 Stück von LOTA und LOTB zum Lagerort OST durch einen Umlagerungsauftrag übertragen.  

> [!NOTE]  
>  Nur die Umlagerungsauftragslieferung, nicht der Wareneingang, wird an diesem Zeitpunkt gebucht.  

 Jetzt sind die folgenden Auftragsverfolgungseinträge in der Tabelle **Reservierungseintrag** vorhanden.  

 ![Zweites Beispiel für Auftragsverfolgungseinträge in der Tabelle „Reservierungseingang“.](media/supply_planning_RTAM_2.png "supply_planning_RTAM_2")  

### <a name="entry-numbers-8-and-9-1" />Eintragsnummern 8 und 9
 Bedarfsverursacherposten für die zwei Chargen der den Bedarf widerspiegelnden Komponente in Tabelle 5407 werden von einem Reservierungsstatus von **Bedarfsverursacher** zu **Überschuss** geändert. Der Grund besteht darin, dass Vorräte, mit denen vorher eine Verknüpfung hergestellt wurde (in Tabelle 32), von der Lieferung des Umlagerungsauftrags verwendet wurden.  

 Echter Überschuss, wie in diesem Fall, spiegelt überschüssigen Vorrat oder Bedarf wider, der nicht nachverfolgt wird. Dies zeigt eine Unausgeglichenheit im Auftragsnetzwerk an, durch die eine Aktionsmeldung vom Planungssystem generiert wird, sofern sie nicht dynamisch gelöst wird.  

### <a name="entry-numbers-12-to-16" />Postennummern 12 bis 16
 Da die beiden Chargen der Komponente auf dem Umlagerungsauftrag als geliefert aber nicht empfangen gebucht werden, haben alle verknüpften positiven Auftragsnachverfolgungsposten den Reservierungstyp **Überschuss**, was angibt, dass sie nicht einem Bedarf zugeordnet sind. Für jede Chargennummer bezieht sich ein Posten auf Tabelle 5741, **Umlagerungszeile**, und ein Posten bezieht sich auf den Artikelposten am I-Transit-Lagerort, an dem sich die Artikel gerade befinden.  

 An diesem Punkt im Szenario wird der Umlagerungsauftrag der Komponenten vom Lagerort OST zu Lagerort WEST als erhalten gebucht.  

 Jetzt sind die folgenden Auftragsverfolgungseinträge in der Tabelle **Reservierungseintrag** vorhanden.  

 ![Drittes Beispiel für Einträge zur Auftragsverfolgung in der Tabelle Reservation Entry.](media/supply_planning_RTAM_3.png "supply_planning_RTAM_3")  

 Die Auftragsnachverfolgungsposten sind jetzt ähnlich dem ersten Punkt im Szenario, bevor der Umlagerungsauftrag als nur geliefert gebucht wurde, ausgenommen, dass die Posten für die Komponenten jetzt den Reservierungsstatus **Überschuss** haben. Dies liegt daran, dass der Komponentenbedarf noch am Lagerort WEST ist und gibt wieder, dass das Feld **Lagerortcode** in der FA-Komponentenzeile **WEST** enthält, wie im **Komponenten von Lagerort**-Einrichtungsfeld festgelegt. Das Lieferung, die diesem zuvor Bedarf zugeordnet wurde, wurde zum Lagerort OST übertragen und kann jetzt nicht vollständig zurückverfolgt werden, es sei denn, der Komponentenbedarf auf der Fertigungsauftragszeile wurd zum Lagerort OST geändert.  

 An diesem Punkt im Szenario wird **Lagerortcode** auf der Fertigungsauftragszeile auf **OST** festgelegt. Darüber hinaus werden auf der Seite **Artikelverfolgungszeilen** die 30 Stück aus LOTA und die 70 Stück aus LOTB der Fertigungsauftragszeile zugeordnet.  

 Jetzt sind die folgenden Auftragsverfolgungseinträge in der Tabelle **Reservierungseintrag** vorhanden.  

 ![Viertes Beispiel für Einträge zur Auftragsverfolgung in der Tabelle „Reservierungseingang“.](media/supply_planning_RTAM_4.png "supply_planning_RTAM_4")  

### <a name="entry-numbers-21-and-22" />Postennummern 21 und 22
 Da der Komponentenbedarf zum Lagerort OST geändert wurde und der Vorrat als Artikelposten am Lagerort OST verfügbar ist, werden alle Auftragsnachverfolgungsposten für die beiden Chargennummern jetzt vollständig verfolgt, angezeigt durch den Reservierungsstatus von **Nachverfolgung**.  

 Das Feld **Chargennr.** ist jetzt auf dem Auftragsnachverfolgungsposten für Tabelle 5407 ausgefüllt, da die Chargennummern zu den Fertigungsauftragskomponentenzeilen zugeordnet wurden.  

 Für mehr Beispiele zu Auftragsnachverfolgungsposten in der Tabelle **Reservierungsposten** vgl. das Whitepaper „Tabelle Reservierungsposten“ auf [PartnerSource](https://go.microsoft.com/fwlink/?LinkId=258348).

## <a name="action-messaging" />Ereignismeldungen
 Wenn Bedarfsverursachersystem eine Ereignismeldung im Bestellungsbestand erkennt, erstellt sie automatisch eine Ereignismeldung, um den Benutzer zu benachrichtigen. Ereignismeldungen sind vom System generierte Aufrufe zu Benutzeraktionen, die die Details der Unausgeglichenheit und Vorschläge zur Wiederherstellung der Balance im Auftragsnetzwerk enthalten. Sie werden als Planungszeilen auf der Seite **Planungsarbeitsblatt** angezeigt, wenn Sie **Aktionsmeldungen abrufen** auswählen. Darüber hinaus werden Ereignismeldungen für Planungszeilen angezeigt, die durch die Planung generiert werden, um die Vorschläge des Planungssystems darüber widerzuspiegeln, wie der Saldo zum Auftragsnetzwerk wiederherzustellen ist. In beiden Fällen werden die Vorschläge auf das Auftragsnetzwerk ausgeführt, wenn Sie **Aktionsmeldungen durchführen** auswählen.  

 Eine Ereignismeldung bezieht sich auf jeweils eine Stücklistenebene. Wenn der Benutzer die Aktionsmeldung akzeptiert, kann dies zu weiteren Aktionsmeldungen auf der nächsten Stücklistenebene führen.  

 Die folgende Tabelle zeigt die Aktionsmeldungen an, die vorhanden sind.  

|Ereignismeldung|Description|  
|--------------------|---------------------------------------|  
|**"Menge ändern"**|Ändert die Menge eines vorhandenen Beschaffungsauftrags, um einen geänderten oder neuen Bedarf zu decken.|  
|**Neu planen**|Plant Fälligkeitsdatum eines bestehenden Fertigungsauftrags oder einer Bestellung neu.|  
|**Neu berechnen & Menge ändern**|Plant Fälligkeitsdatum neu und ändert Menge eines bestehenden Fertigungsauftrags oder einer Bestellung.|  
|**Neu**|Erstellt einen neuen Auftrag, wenn der Bedarf nicht durch eine der vorherigen Aktionsmeldungen gedeckt werden kann.|  
|**Stornieren**|Stornieren eines bestehenden Auftrags.|  

 Das Auftragsnachverfolgungssystem versucht immer, eine Unausgeglichenheit im bestehenden Auftragsnetzwerk auszugleichen. Wenn dies nicht möglich ist, wird es eine Aktionsmeldung ausgegeben, um einem neuen Auftrag zu erstellen. Es folgt die nach Priorität sortierte Liste, die das Auftragsnachverfolgungssystem verwendet, wenn es festlegt, wie der Saldo hergestellt werden soll. Wenn ein zusätzlicher Bedarf in das Auftragsnetzwerk eingegeben wurde, versucht das System ihn anhand der folgenden Prüfungen nachzuverfolgen:  

1.  Prüfung auf überschüssigen Vorrat im vorhandenen Auftragsnachverfolgungsdatensatz für diesen Bedarf.  
2.  Prüfung auf geplante und zeitlich geplante Zugänge in der Reihenfolge des Eingangsdatums. Das letzte mögliche Datum ist ausgewählt.  
3.  Prüfung auf verfügbaren Lagerbestand.  
4.  Prüfung, ob ein Beschaffungsauftrag im aktuellen Auftragsnachverfolgungsdatensatz vorhanden ist. Ist dies der Fall, gibt das System eine Aktionsmeldung der Art **Ändern** aus, um den Auftrag zu erhöhen.  
5.  Prüfung, ob kein Beschaffungsauftrag im aktuellen Auftragsnachverfolgungsdatensatz vorhanden ist. Ist dies der Fall, gibt das System eine Aktionsmeldung der Art **Neu** aus, um einen neuen Auftrag zu erstellen.  

 Ein offener Bedarf läuft durch die Liste und verschiebt an jedem Punkt den verfügbaren Vorrat. Jeder verbleibende Bedarf wird immer von Scheck 4 oder Scheck 5 abgedeckt.  

 Wenn eine Verminderung der Bedarfsmenge auftritt, versucht das Auftragsnachverfolgungssystem, die Unausgeglichenheit zu beheben, indem es in umgekehrter Reihenfolge die vorherigen Prüfungen ausführt. Das bedeutet, dass vorhandene Ereignismeldungen geändert oder sogar gelöscht werden können, falls notwendig. Das Auftragsnachverfolgungssystem zeigt dem Benutzer immer das Nettoergebnis seiner Berechnungen an.  

## <a name="order-tracking-and-planning" />Bedarfsverursacher und Planung
 Wenn das Planungssystem ausgeführt wird, löscht es alle Nachverfolgungsdatensätze des bestehenden Auftrags sowie Ereignismeldungen und erstellt sie im Zuge Planungszeilenvorschläge entsprechend Angebot- und Nachfragepaaren und -Prioritäten neu. Wenn der Planungslauf beendet ist, ist das Auftragsnetzwerk im Saldo.  

### <a name="planning-system-versus-order-tracking-and-action-messaging" />Planungssystem mit Bedarfsverursacher- und Aktions-Messaging
 Der folgende Vergleich zeigt die Unterschiede zwischen den Methoden, die vom Planungssystem verwendet werden, um Planungszeilenvorschläge zu erstellen, sowie die Methoden, die das Auftragsnachverfolgungssystem verwendet, um Auftragsnachverfolgungsdatensätze und Aktionsmeldungen zu erstellen.  

-   Das Planungssystem behandelt das gesamte Vorrats- und Bedarfsmuster eines bestimmten Artikels, während die Auftragsnachverfolgung den Auftrag behandelt, der sie aktiviert hat.  

-   Das Planungssystem behandelt alle Ebenen der Stücklistenhierarchie, während die Auftragsnachverfolgung nur jeweils eine Stücklistenebene gleichzeitig behandelt.  

-   Das Planungssystem richtet Verknüpfungen zwischen Bedarf und Vorrat entsprechend dem priorisierten Fälligkeitsdatum ein. Bedarfsverursacher enthält Verknüpfungen zwischen Bedarf und Vorrat entsprechend der Reihenfolge der eingehenden Aufträge.  

-   Das Planungssystem berücksichtigt Planungsparameter, während die Auftragsnachverfolgung dies nicht tut.  

-   Das Planungssystem erstellt Verknüpfungen in einem benutzeraktivierten Batchmodus, wenn es Bedarf und Vorrat ausgleicht, während die Auftragsnachverfolgung die Verknüpfungen automatisch und dynamisch erstellt, wenn der Benutzer Aufträge eingibt.  

## <a name="see-also" />Siehe auch
[Designdetails: Zentrale Konzepte des Planungssystems](design-details-central-concepts-of-the-planning-system.md)   
[Designdetails: Vorratsplanung](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
