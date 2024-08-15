---
title: 'Entwurfsdetails: Reservierung, Auftragsverfolgung und Aktionsnachrichten | Microsoft Docs'
description: Das Reservierungssystem ist umfassend und enthält auch die zusammenhängenden und parallelen Features der Auftragsnachverfolgung und Aktionsmeldungen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'design, replenishment, reordering'
ms.date: 07/23/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Designdetails: Reservierung, Auftragsnachverfolgung und Aktionsmeldungen

Das Reservierungssystem ist umfassend und enthält auch die zusammenhängenden und parallelen Features der Auftragsnachverfolgung und Aktionsmeldungen.  

Der Kern des Reservierungssystems besteht in der Verknüpfung einer Bedarfsbuchung und einer entsprechenden Angebotsbuchung, entweder über eine Reservierung oder eine Auftragsverfolgung. Eine Reservierung ist ein vom Benutzer generierter Link, und ein Auftragsnachverfolgungsdatensatz ist ein vom System generierter Link. Eine Artikelmenge, die in das Reservierungssystem eingegeben wurde, ist entweder reserviert oder auftragsnachverfolgt, aber nicht beides gleichzeitig. Wie die Systeme mit einem Artikel umgehen, hängt davon ab, wie der Artikel eingerichtet ist.  

Das Reservierungssystem interagiert mit dem Planungssystem durch Erstellen von Aktionsmeldungen auf Planungszeilen während der Planungsausführung. Eine Ereignismeldung kann als Anhang zu einem Auftragsnachverfolgungsbeleg betrachtet werden. Ereignismeldungen, ob dynamisch erstellt in der Auftragsnachverfolgung oder während der Planung erstellt, sind nützliche Hilfsmittel für eine effiziente Beschaffungsplanung.  

> [!NOTE]  
> Reservierte Mengen werden vom Planungssystem ignoriert, d. h. die feste Verknüpfung zwischen Vorrat und Bedarf kann nicht durch die Planung geändert werden.  

 Das Reservierungssystem bildet auch die strukturelle Basis für das Artikelnachverfolgungssystem. Weitere Informationen finden Sie unter [Designdetails: Artikelverfolgung](design-details-item-tracking.md).  

 <!--For more detailed information about how the reservation system works, see the _Reservation Entry Table_ white paper on [PartnerSource](https://go.microsoft.com/fwlink/?LinkId=258348).  -->
<!--
> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]
-->

## Reservierung  

 Eine Reservierung ist ein fester Link, der einen speziellen Bedarf und einen bestimmten Vorrat miteinander verknüpft. Diese Verknüpfung beeinflusst dirket die nächste Lagertransaktion und sorgt für die richtigen Anwendung von Artikelposten für Bewertungszwecke. Eine Reservierung setzt die Standard-Kostenberechnungsmethode eines Artikels außer Kraft. Weitere Informationen finden Sie unter [Designdetails: Artikelverfolgung](design-details-item-tracking.md).  

 Die Seite **Reservierung** ist von allen Auftragszeilen des Typs Bedarf und Vorrat aus zugänglich. auf der Seite kann der Benutzer angeben, zu welchem Bedarfs- oder Vorratsposten eine Reservierungsverknüpfung erstellt werden soll. Die Reservierung besteht aus einem Paar von Datensätzen, die dieselbe Postennummer haben. Ein Datensatz hat ein negatives Vorzeichen und verweist auf den Bedarf. Der andere Datensatz hat ein positives Vorzeichen und verweist auf den Vorrat. Diese Datensätze werden in der Tabelle  *Reservierungseintrag*  mit dem Statuswert  *Reservierung gespeichert*. Der Benutzer kann alle Reservierungen auf der Seite **Reservierungsposten** anzeigen.  

### Ausgleichung für Reservierungen  

 Reservierungen werden gegen verfügbare Artikelmengen vorgenommen. Artikelverfügbarkeit wird wie folgt grundlegend berechnet:  

 `available quantity = inventory + scheduled receipts - gross requirements`

 Die folgende Tabelle zeigt die Details der Auftragsnetzwerkeinheiten an, die Teil der Verfügbarkeitsberechnung sind.  

||Feld in T27-Element|Herkunftstabelle|Tabellenfilter|Quellfeld|  
|-|------------------|------------------|------------------|------------------|  
|**Lager**|Bestand|Artikelposten|N/Z|Menge|  
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

### Manuelle Reservierung  

Wenn ein Benutzer absichtlich eine Reservierung erstellt, erhält er vollen Besitz von und Zuständigkeit für diese Artikel. Dies bedeutet, dass der Benutzer eine Reservierung auch manuell ändern oder stornieren muss. Solche manuellen Änderungen können eine automatische Änderung der betroffenen Reservierungen zur Folge haben.  

Die folgende Tabelle zeigt, wann welche Änderungen auftreten können:  

|Benutzeraktion|Systemreaktion|  
|-----------------|---------------------|  
|Reduzieren der reservierten Menge|Die verknüpften Mengenfelder werden entsprechend aktualisiert.|  
|Ändern von Datumsfeldern|Die verknüpften Datumsfelder werden entsprechend aktualisiert.<br /><br /> **Hinweis**: Wenn das Fälligkeitsdatum auf einem Bedarf so geändert wird, dass es dem Lieferdatum oder dem Fälligkeitsdatum des Vorrats vorangeht, wird die Reservierung storniert.|  
|Löschen des Auftrags|Die Reservierung wird abgebrochen.|  
|Ändern des Lagerorts, des Lagerplatzes, der Variante, der Seriennummer oder der Chargennummer|Die Reservierung wird abgebrochen.|  

> [!NOTE]  
> Die Funktionalität der späten Bindung kann auch Reservierungen ändern, ohne den Benutzer zu informieren, indem sie nicht-spezifische Reservierungen von Serien- oder Chargennummern neu anordnet. Weitere Informationen finden Sie unter [Designdetails: Artikelverfolgung und Reservierungen](design-details-item-tracking-and-reservations.md).  

### Automatische Reservierungen  

 Die Artikelkarte kann so eingerichtet werden, dass immer eine Reservierung vom Bedarf stattfindet, etwa bei Verkaufsaufträgen. In diesem Fall wird eine Reservierung gegen den Bestand, Kaufaufträge, Montageaufträge und Fertigungsaufträge vorgenommen. Eine Warnung wird ausgegeben, wenn der Vorrat nicht ausreicht.  

 Darüber hinaus werden Artikel automatisch nach verschiedenen Planungsfunktionen reserviert, um einen mit einer bestimmten Bedarfssicherung verknüpften Bedarf beizubehalten. Die Auftragstrackingeinträge für solche Planungsverknüpfungen enthalten im Feld  **Reservierungsstatus**  der Tabelle  **Reservierungseintrag**  den Eintrag  *Reservierung* . Automatische Reservierungen werden in den folgenden Situationen erstellt:  

- Ein mehrstufiger Fertigungsauftrag, in dem das Feld **Produktionsart** der betreffenden übergeordneten und untergeordneten Artikel auf **Auftragsfertigung** festgelegt wurde. Das Planungssystem erstellt Reservierungen zwischen dem Produktionsauftrag zeigen und den zugrunde liegenden Produktionsaufträgen, um sicherzustellen, dass sie zusammen verarbeitet werden. Eine solche Reservierungsbindung überschreibt die Standard-Kostenberechnungs- und -ausgleichsmethode des Artikels.  

- Ein Produktions-, Montage- oder ein Einkaufsauftrag, in dem das Feld **Wiederbeschaffungsverfahren** des betreffenden Artikels auf **Auftrag** festgelegt wurde. Das Planungssystem erstellt Reservierungen zwischen dem Bedarf und dem geplanten Vorrat, um sicherzustellen, dass der bestimmte Vorrat erstellt wird. Weitere Informationen finden Sie unter [Auftrag](design-details-handling-reordering-policies.md#order).  

- Ein Fertigungsauftrag, der aus einem Verkaufsauftrag mit der Funktion **Verkaufsauftragsplanung** erstellt wird, wird mit dem Verkaufsauftrag mit einer automatischen Reservierung verknüpft.  

- Ein automatisch für eine Verkaufsauftragszeile erstellter Montageauftrag, um die Menge im Feld  **Menge für Auftragsmontage**  zu erfüllen. Diese automatische Reservierung verknüpft den Verkaufsbedarf mit dem Montagezubehör, sodass Verkaufsauftragsbearbeiter den Montageartikel für den Debitor direkt anpassen und zusagen können. Darüber hinaus verknüpft die Reservierung den Montageausstoß der Verkaufsauftragszeile mit der Versandaktivität, die den Debitorenauftrag erfüllt.  

Bei nicht zugeteiltem Angebot oder Bedarf weist das Planungssystem automatisch einen Reservierungsstatus vom Typ  **Überschuss** zu. Dies kann sich aus Bedarf ergeben, der aufgrund von Planungsmengen oder der vom Benutzer eingegebenen Planungsparameter resultiert. Dabei handelt es sich um einen legitimen Überschuss, der vom System erkannt wird und nicht zu Aktionsmeldungen führt. Der Überschuss kann auch echter überschüssiger Vorrat oder nicht nachverfolgter Bedarf sein. Dies ist eine Angabe einer Ereignismeldung im Bestellungsbestand, das die Anwendung dazu veranlasst, Ereignismeldungen zu auszugeben. Beachten Sie, dass eine Ereignismeldung, die eine Änderung in der Menge vorschlägt, sich immer auf den Typ **Überschuss** bezieht. Weitere Informationen finden Sie im Abschnitt  [Beispiel: Auftragsverfolgung in Verkauf, Produktion und Transfers](#example-order-tracking-in-sales-production-and-transfers) in diesem Artikel.  

Automatische Reservierungen, die bei der Planungsausführung erstellt werden, werden in der folgenden Weise behandelt:  

- Sie werden auf Artikelmengen angewendet, die Teil der Verfügbarkeitsberechnung sind, ebenso wie manuelle Reservierungen. Weitere Informationen finden Sie im Abschnitt „Ausgleich bei Reservierungen“ in diesem Artikel.  

- Sie werden im Gegensatz zu manuell reservierten Artikeln bei nachfolgenden Planungsläufen berücksichtigt und ggf. geändert.  

## Auftragsnachverfolgung  

Bedarfsverursacher hilft dem Planer, einen gültigen Beschaffungsplan zu gewährleisten, indem er eine Übersicht zwischen Bedarf und Vorrat im Bestellungsbestand bereitstellt. Die Auftragsnachverfolgungsdatensätze dienen als Grundlage für die Erstellung von dynamischen Aktionsmeldungen und von Planungszeilenvorschlägen im Rahmen der Planungsausführungen.  

> [!NOTE]  
> Das Auftragsnachverfolgungssystem gleicht verfügbaren Bestand aus, wenn Aufträge in das Auftragsnetzwerk eingegeben werden. Dies bedeutet, dass die Anwendung Aufträge nicht priorisiert, die in Bezug auf ihr Fälligkeitsdatum dringender sind. Es ist daher auf die Logik des Planungssystems oder der Klugheit des Terminplaners angewiesen, um diese Prioritäten auf eine sinnvolle Art neu anzuordnen.  

> [!NOTE]  
> Die Auftragsverfolgungsrichtlinie und die Funktion „Aktionsmeldungen abrufen“ sind nicht in Projekte integriert. Das bedeutet, dass der Bedarf, der mit einem Projekt verknüpft ist, nicht automatisch verfolgt wird. Da dies nicht nachverfolgt wird, könnte es dazu führen, dass eine vorhandene Auffüllung mit Projektinformationen zu einem anderen Bedarf, beispielsweise ein Auftrag, verfolgt wird. Deshalb treffen Sie möglicherweise die Situation an, in der Ihre Informationen über verfügbaren Lagerbestand nicht synchron sind.  

### Das Auftragsnetzwerk  

Das Auftragsnachverfolgungssystem basiert auf dem Prinzip, das das Auftragsnetzwerk immer in einem Zustand des Gleichgewichts sein muss, in dem jeder Bedarf, der in das System eingeht, durch einen entsprechenden Vorrat ausgeglichen wird und umgekehrt. Die Anwendung stelt dies zu Verfügung, indem sie logische Verknüpfungen zwischen allen Bedarfs- und Vorratsposten im Bestellungsbestand bereitstellt.  

Dieses Prinzip impliziert, dass eine Nachfrageänderung zu einer entsprechenden Unausgeglichenheit auf der Zugangsseite des Auftragsnetzwerks führt. Andererseits resultiert eine Angebotsänderung in einer entsprechenden Unausgeglichenheit auf der Bedarfsseite des Auftragsnetzwerks. In der Realität ist das Auftragsnetzwerk in einem Zustand konstanten Flusses, da Benutzer Aufträge eingeben, ergänzen und löschen. Bedarfsverursacher verarbeitet Aufträge dynamisch, reagiert auf jede Änderung zum Zeitpunkt ihrer Eingabe in das System ein und wird ein Teil des Auftragsnetzwerks. Sobald neue Auftragsnachverfolgungsdatensätze erstellt wurden, ist das Auftragsnetzwerk ausgeglichen, aber nur bis zur nächsten Änderung.  

Um die Transparenz der Berechnungen im Planungssystem zu erhöhen, zeigt die Seite **Unverfolgte Planungselemente** nicht verfolgte Mengen an, die die Mengendifferenz zwischen bekanntem Bedarf und vorgeschlagenem Vorrat darstellen. Jede Zeile auf der Seite bezieht sich auf den Grund des Überschusses, wie **Rahmenauftrag**, **Sicherheitsbestands-Ebene**, **Feste Bestellmenge**, **Mindestauftragsmenge**, **Rundung** oder **Toleranz**.  

### Ausgleichung in der Auftragsverfolgung  

Im Gegensatz zu Reservierungen, die nur gegen verfügbare Artikelmengen vorgenommen werden können, ist die Auftragsnachverfolgung gegen alle Auftragsnetzwerkeinheiten möglich, die Teil der Nettobedarfsrechnung des Planungssystems sind. Der Nettobedarf wird wie folgt berechnet:  

`net requirements = gross requirements + reorder point - scheduled receipts - planned receipts - projected available balance`  

> [!NOTE]  
> Bedarf, der mit Planungen oder Planungsparametern verbunden ist, wird nicht nach Auftrag nachverfolgt.  

### Beispiel: Auftragsnachverfolgung im Verkauf, in der Produktion und bei Umlagerungen  

Das folgende Szenario zeigt, welche Auftragstrackingeinträge in der Tabelle  *Reservierungseintrag*  als Ergebnis verschiedener Auftragsnetzwerkänderungen erstellt werden.  

Gehen wir von den folgenden Daten für zwei Artikel aus, die für die Auftragsnachverfolgung eingerichtet wurden.  

|Option|Parameter|Detail|
|-|-|-|
|Artikel 1|Name|Komponente|
||Verfügbarkeit|100 Einheiten am Lagerort EAST<br /><br />- 30 Einheiten LOTA<br />- 70 Einheiten LOTB|  
|Artikel 2|Name|Produziertes Produkt|
||Fertigungsstückliste|1 Menge pro Komponente|  
||Bedarf|Verkauf für 100 Einheiten am Standort WEST|  
||Vorrat|Freigegebener Fertigungsauftrag (generiert mit der Funktion  *Verkaufsauftragsplanung*  für den Verkauf von 100 Einheiten)|  

Auf der Seite  **Fertigungseinrichtung**  ist das Feld  **Komponenten am Standort**  auf  *OST* eingestellt.

Basierend auf den Daten in der Tabelle sind in der Tabelle  *Reservierungseintrag*  die folgenden Auftragstrackingeinträge vorhanden.  

<!--![First example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_1.png "supply_planning_RTAM_1")  -->
**Reservierungseinträge**

|Postennummer|Positiv|Artikelnummer|Lagerortcode|Menge|Reservierungsstatus|Description|Chargennr.|Herkunftsart|Herkunfts-ID|Verknüpfung|  
|--------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|8|-|KOMPONENTE|OST|-70|Nachverfolgung|Komponente|-|5407|101004|-|
|8|Ja|KOMPONENTE|OST|70|Nachverfolgung|Komponente|LOTB|32|-|-| 
|9|-|KOMPONENTE|OST|-30|Nachverfolgung|Komponente|-|5407|1001004|-| 
|9|Ja|KOMPONENTE|OST|30|Nachverfolgung|Komponente|Lotta|32|-|-| 
|10|-|PRODUKTIERTES PRODUKT|WEST|-100|Reservierung|Produziertes Produkt|-|37|1001|Eins-zu-Eins|
|10|Ja|PRODUKTIERTES PRODUKT|WEST|100|Reservierung|Produziertes Produkt|-|5406|101004|Eins-zu-Eins|


#### Postennummern 8 und 9  

Für den Komponentenbedarf für LOTA bzw. LOTB werden Auftragsverfolgungsverknüpfungen vom Bedarf in Tabelle 5407,  *Fertigungsauftragskomponente*, zum Vorrat in Tabelle 32,  *Artikelposten*, erstellt. Das Feld  **Reservierungsstatus**  enthält  *Tracking*, um anzuzeigen, dass es sich bei diesen Einträgen um dynamische Bestelltracking-Links zwischen übergeordnetes Element handelt.  

> [!NOTE]  
> Das Feld **Chargennr.** ist auf den Bedarfszeilen leer, da die Chargennummern nicht auf den Komponentenzeilen des freigegebenen Fertigungsauftrags angegeben sind.  

#### Postennummer 10  

Aus dem Verkaufsbedarf in Tabelle 37,  *Verkaufszeilen*, wird eine Auftragsverfolgung verknüpfen für den Vorrat in Tabelle 5406,  *Produktionsauftragszeile*, erstellt. Das Feld  **Reservierungsstatus**  enthält  *Reservierung* und das Feld  **Bindung**  enthält  *Bestellung-zu-Bestellung*. Dies liegt daran, dass der freigegebene Fertigungsauftrag speziell für den Verkaufsauftrag generiert wurde und verknüpft bleiben muss, im Gegensatz zu Auftragstrackingverknüpfungen mit dem Reservierungsstatus „Tracking“, der dynamisch erstellt und geändert wird. Weitere Informationen finden Sie im Abschnitt  [Automatische Reservierungen](#automatic-reservations)  in diesem Artikel.  

 An dieser Stelle im Szenario zeigen werden die 100 Einheiten von LOTA und LOTB per Transferauftrag an den Standort WEST übertragen.  

> [!NOTE]  
> Nur die Umlagerungsauftragslieferung, nicht der Wareneingang, wird an diesem Zeitpunkt gebucht.  

 Nun sind in der Tabelle  *Reservierungseintrag*  folgende Auftragstrackingeinträge vorhanden.  

<!-- ![Second example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_2.png "supply_planning_RTAM_2")  -->
**Reservierungseinträge**

|Postennummer|Positiv|Artikelnummer|Lagerortcode|Menge|Reservierungsstatus|Description|Chargennr.|Herkunftsart|Herkunfts-ID|Verknüpfung|  
|---------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|9|-|KOMPONENTE|OST|-30|Überschuss|Komponente|-|5407|1001004|-| 
|10|-|PRODUKTIERTES PRODUKT|WEST|-100|Reservierung|Produziertes Produkt|-|37|1001|Eins-zu-Eins|
|10|Ja|PRODUKTIERTES PRODUKT|WEST|100|Reservierung|Produziertes Produkt|-|5406|101004|Eins-zu-Eins|
|12|Ja|KOMPONENTE|WEST|70|Überschuss|Komponente|LOTB|5741|1011|-| 
|14|Ja|KOMPONENTE|WEST|30|Überschuss|Komponente|Lotta|5741|1011|-| 
|15|Ja|KOMPONENTE|OUT.LOG.|70|Überschuss|Komponente|LOTB|32|-|-| 
|16|Ja|KOMPONENTE|OUT.LOG.|30|Überschuss|Komponente|Lotta|32|-|-| 

#### Postennummern 8 und 9  

Die Auftragsverfolgungseinträge für die beiden Chargen der Komponente, die den Bedarf in Tabelle 5407 widerspiegeln, werden von einem Reservierungsstatus von  *Verfolgung*  in  *Überschuss* geändert. Der Grund besteht darin, dass Vorräte, mit denen vorher eine Verknüpfung hergestellt wurde (in Tabelle 32), von der Lieferung des Umlagerungsauftrags verwendet wurden.  

Echter Überschuss, wie in diesem Fall, spiegelt überschüssigen Vorrat oder Bedarf wider, der nicht nachverfolgt wird. Es handelt sich um einen Hinweis auf ein Ungleichgewicht im Auftragsnetzwerk, das, sofern es nicht dynamisch behoben wird, eine Aktionsmeldung durch das Planungssystem generiert.  

#### Postennummern 12 bis 16  

Da die beiden Chargen der Komponente im Umlagerungsauftrag als geliefert, aber nicht als empfangen gebucht sind, sind alle zugehörigen positiven Auftragstrackingeinträge vom Reservierungstyp  *Überschuss*, was bedeutet, dass sie keinen Bedarfen zugeordnet sind. Für jede Chargennummer bezieht sich ein Eintrag auf Tabelle 5741,  *Transferzeile*, und ein Eintrag bezieht sich auf den Artikelposten am Transitort, an dem sich die Artikel jetzt befinden.  

An dieser Stelle im Szenario wird die Reihenfolge der Übertragung der Komponenten von *OST*  Zu *WESTEN*  Standort wird als empfangen gebucht.  

Nun sind in der Tabelle  *Reservierungseintrag*  folgende Auftragstrackingeinträge vorhanden.  

<!-- ![Third example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_3.png "supply_planning_RTAM_3") -->
 **Reservierungseinträge**

|Postennummer|Positiv|Artikelnummer|Lagerortcode|Menge|Reservierungsstatus|Description|Chargennr.|Herkunftsart|Herkunfts-ID|Verknüpfung|  
|---------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|8|-|KOMPONENTE|OST|-70|Überschuss|Komponente|-|5407|101004|-| 
|9|-|KOMPONENTE|OST|-30|Überschuss|Komponente|-|5407|1001004|-|
|10|-|PRODUKTIERTES PRODUKT|WEST|-100|Reservierung|Produziertes Produkt|-|37|1001|Eins-zu-Eins|
|10|Ja|PRODUKTIERTES PRODUKT|WEST|100|Reservierung|Produziertes Produkt|-|5406|101004|Eins-zu-Eins|
|17|Ja|KOMPONENTE|WEST|70|Überschuss|Komponente|LOTB|32|-|-| 
|18|Ja|KOMPONENTE|WEST|30|Überschuss|Komponente|Lotta|32|-|-| 

Die Auftragstrackingeinträge ähneln nun den ersten zeigen im Szenario, bevor der Transferauftrag nur als versendet gebucht wurde, außer dass Einträge für die Komponente nun den Status „Reservierung“ haben. *Überschuss*. Dies liegt daran, dass der Komponentenbedarf immer noch am Standort  *OST*  besteht, was bedeutet, dass das Feld  **Standortcode**  in der Komponentenzeile des Fertigungsauftrags den Wert  *OST*  enthält, wie im Feld  **Komponenten am Standort**  eingerichtet. Der Vorrat, der diesem Bedarf zuvor zugewiesen wurde, wurde an den Standort  *WEST*  übertragen und kann jetzt nicht mehr vollständig nachverfolgt werden, es sei denn, der Komponentenbedarf in der Fertigungsauftragszeile wird an den Standort  *WEST*  geändert.  

An dieser Stelle im Szenario zeigen wird der  **Standortcode**  in der Komponentenzeile des Fertigungsauftrags auf  *WEST* gesetzt. Darüber hinaus werden auf der Seite  **Artikelverfolgungszeilen**  die 30 Einheiten LOTA und die 70 Einheiten LOTB der Komponentenzeile des Fertigungsauftrags zugewiesen.  

Nun sind in der Tabelle  *Reservierungseintrag*  folgende Auftragstrackingeinträge vorhanden.  

<!-- ![Fourth example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_4.png "supply_planning_RTAM_4")   -->
 **Reservierungseinträge**

|Postennummer|Positiv|Artikelnummer|Lagerortcode|Menge|Reservierungsstatus|Description|Chargennr.|Herkunftsart|Herkunfts-ID|Verknüpfung|  
|---------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|10|-|PRODUKTIERTES PRODUKT|WEST|-100|Reservierung|Produziertes Produkt|-|37|1001|Eins-zu-Eins|
|10|Ja|PRODUKTIERTES PRODUKT|WEST|100|Reservierung|Produziertes Produkt|-|5406|101004|Eins-zu-Eins|
|21|-|KOMPONENTE|WEST|-70|Nachverfolgung|Komponente|LOTB|5407|101004|-| 
|21|Ja|KOMPONENTE|WEST|70|Nachverfolgung|Komponente|LOTB|32|-|-| 
|22|-|KOMPONENTE|WEST|-30|Nachverfolgung|Komponente|Lotta|5407|1001004|-| 
|22|Ja|KOMPONENTE|WEST|30|Nachverfolgung|Komponente|Lotta|32|-|-| 

#### Postennummern 21 und 22  

Da der Komponentenbedarf auf den Standort  *WEST*  geändert wurde und die Lieferung als Artikelposten am Standort  *WEST*  verfügbar ist, werden alle Auftragstrackingeinträge für die beiden Chargennummern nun vollständig verfolgt, was durch den Reservierungsstatus  *Verfolgung* angezeigt wird.  

Das Feld **Chargennr.** ist jetzt auf dem Auftragsnachverfolgungsposten für Tabelle 5407 ausgefüllt, da die Chargennummern zu den Fertigungsauftragskomponentenzeilen zugeordnet wurden.  

## Aktionsmeldungen  

Wenn Bedarfsverursachersystem eine Ereignismeldung im Bestellungsbestand erkennt, erstellt sie automatisch eine Ereignismeldung, um den Benutzer zu benachrichtigen. Ereignismeldungen sind vom System generierte Aufrufe zu Benutzeraktionen, die die Details der Unausgeglichenheit und Vorschläge zur Wiederherstellung der Balance im Auftragsnetzwerk enthalten. Sie werden als Planungszeilen auf der Seite  **Planungsarbeitsblätter**  angezeigt, wenn Sie die Aktion  **Aktionsmeldungen abrufen**  auswählen. Darüber hinaus werden Ereignismeldungen für Planungszeilen angezeigt, die durch die Planung generiert werden, um die Vorschläge des Planungssystems darüber widerzuspiegeln, wie der Saldo zum Auftragsnetzwerk wiederherzustellen ist. In beiden Fällen werden die Vorschläge im Auftragsnetzwerk ausgeführt, wenn Sie die Aktion  **Aktionsmeldung ausführen**  wählen.  

Eine Ereignismeldung bezieht sich auf jeweils eine Stücklistenebene. Wenn der Benutzer die Aktionsmeldung akzeptiert, kann dies zu weiteren Aktionsmeldungen auf der nächsten Stücklistenebene führen.  

Die folgende Tabelle zeigt die Aktionsmeldungen an, die vorhanden sind.  

|Ereignismeldung|Description|  
|--------------------|---------------------------------------|  
|**"Menge ändern"**|Ändert die Menge eines vorhandenen Beschaffungsauftrags, um einen geänderten oder neuen Bedarf zu decken.|  
|**Neu planen**|Plant Fälligkeitsdatum eines bestehenden Fertigungsauftrags oder einer Bestellung neu.|  
|**Neu berechnen & Menge ändern**|Plant Fälligkeitsdatum neu und ändert Menge eines bestehenden Fertigungsauftrags oder einer Bestellung.|  
|**Neu**|Erstellt eine neue Bestellung, wenn der Bedarf durch keine der vorherigen Aktionsmeldungen gedeckt werden kann.|  
|**Abbrechen**|Stornieren eines bestehenden Auftrags.|  

Das Auftragsnachverfolgungssystem versucht immer, eine Unausgeglichenheit im bestehenden Auftragsnetzwerk auszugleichen. Wenn dies nicht möglich ist, wird eine Aktionsmeldung zum Anlegen einer neuen Bestellung ausgegeben. Es folgt die nach Priorität sortierte Liste, die das Auftragsnachverfolgungssystem verwendet, wenn es festlegt, wie der Saldo hergestellt werden soll. Wenn ein zusätzlicher Bedarf in das Auftragsnetzwerk eingegeben wurde, versucht das System ihn anhand der folgenden Prüfungen nachzuverfolgen:  

1. Prüfung auf überschüssigen Vorrat im vorhandenen Auftragsnachverfolgungsdatensatz für diesen Bedarf.  
2. Prüfung auf geplante und zeitlich geplante Zugänge in der Reihenfolge des Eingangsdatums. Das letzte mögliche Datum ist ausgewählt.  
3. Prüfung auf verfügbaren Lagerbestand.  
4. Prüfung, ob ein Beschaffungsauftrag im aktuellen Auftragsnachverfolgungsdatensatz vorhanden ist. Wenn dies der Fall ist, gibt das System eine Aktionsnachricht vom Typ  *Ändern*  aus, um die Bestellung zu erhöhen.  
5. Prüfung, ob kein Beschaffungsauftrag im aktuellen Auftragsnachverfolgungsdatensatz vorhanden ist. Wenn dies der Fall ist, gibt das System eine Aktionsnachricht vom Typ  *Neu*  aus, um eine neue Bestellung zu erstellen.  

Ein offener Bedarf läuft durch die Liste und verschiebt an jedem Punkt den verfügbaren Vorrat. Jeder verbleibende Bedarf wird immer von Scheck 4 oder Scheck 5 abgedeckt.  

Wenn eine Verminderung der Bedarfsmenge auftritt, versucht das Auftragsnachverfolgungssystem, die Unausgeglichenheit zu beheben, indem es in umgekehrter Reihenfolge die vorherigen Prüfungen ausführt. Das bedeutet, dass vorhandene Ereignismeldungen geändert oder sogar gelöscht werden können, falls notwendig. Das Auftragsnachverfolgungssystem zeigt dem Benutzer immer das Nettoergebnis seiner Berechnungen an.  

## Auftragsverfolgung und -planning  

Wenn das Planungssystem ausgeführt wird, löscht es alle Nachverfolgungsdatensätze des bestehenden Auftrags sowie Ereignismeldungen und erstellt sie im Zuge Planungszeilenvorschläge entsprechend Angebot- und Nachfragepaaren und -Prioritäten neu. Wenn der Planungslauf beendet ist, ist das Auftragsnetzwerk im Saldo.  

### Planungssystem mit Auftragsverfolgung und Aktionsmeldung  

 Der folgende Vergleich zeigt die Unterschiede zwischen den Methoden, die vom Planungssystem verwendet werden, um Planungszeilenvorschläge zu erstellen, sowie die Methoden, die das Auftragsnachverfolgungssystem verwendet, um Auftragsnachverfolgungsdatensätze und Aktionsmeldungen zu erstellen.  

- Das Planungssystem behandelt das gesamte Vorrats- und Bedarfsmuster eines bestimmten Artikels, während die Auftragsnachverfolgung den Auftrag behandelt, der sie aktiviert hat.  

- Das Planungssystem behandelt alle Ebenen der Stücklistenhierarchie, während die Auftragsnachverfolgung nur jeweils eine Stücklistenebene gleichzeitig behandelt.  

- Das Planungssystem richtet Verknüpfungen zwischen Bedarf und Vorrat entsprechend dem priorisierten Fälligkeitsdatum ein. Bedarfsverursacher enthält Verknüpfungen zwischen Bedarf und Vorrat entsprechend der Reihenfolge der eingehenden Aufträge.  

- Das Planungssystem berücksichtigt Planungsparameter, die Auftragsverfolgung hingegen nicht.  

- Das Planungssystem erstellt Verknüpfungen in einem benutzeraktivierten Batchmodus, wenn es Bedarf und Vorrat ausgleicht, während die Auftragsnachverfolgung die Verknüpfungen automatisch und dynamisch erstellt, wenn der Benutzer Aufträge eingibt.  

## Siehe auch  

[Designdetails: Zentrale Konzepte des Planungssystems](design-details-central-concepts-of-the-planning-system.md)  
[Designdetails: Vorratsplanung](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
