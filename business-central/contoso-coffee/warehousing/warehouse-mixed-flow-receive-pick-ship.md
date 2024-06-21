---
title: 'Eingang, Einlagerung, Kommissionierung und Versand in gemischten Lagerkonfigurationen'
description: 'In Business Central können die ein- und ausgehenden Prozesse für das Empfangen und Einlagern auf vier Arten, mit den verschiedenen Funktionen, immer abhängig von der Lagerkomplexitätsebene, ausgeführt werden.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Exemplarische Vorgehensweise für ein- und ausgehende Flows in gemischten Lagerkonfigurationen

Diese exemplarische Vorgehensweise zeigt, wie Sie eingehende und ausgehende Flows in einer gemischten Konfiguration vervollständigen, wobei das Warenlager für den eingehenden Flow als Basic: Auftrag-für-Auftrag konfiguriert ist und für den ausgehenden Flow die erweiterte Konfiguration verwendet wird. Weitere Informationen finden Sie unter [Übersicht über verschiedene Konfigurationsoptionen](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## Voraussetzungen  
Um diese exemplarische Vorgehensweise zu beenden, müssen Sie selber einen Lagermitarbeiter am Standort *YELLOW* mit folgenden Schritten erstellen:  
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 1.](../../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Lagermitarbeiter** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie das Feld **Benutzer-ID** aus, und wählen Sie Ihr eigenes Benutzerkonto auf der Seite **Benutzer** aus.  
3. Geben Sie im Feld **Lagerortcode** *YELLOW* ein.  

## Eingeheder Flow: Eingang und Einlagerung in Basis-Lagerkonfigurationen

In [!INCLUDE[prod_short](../../includes/prod_short.md)] können die eingehenden Prozesse für das Empfangen und Einlagern auf vier Arten, mit den verschiedenen Funktionen, abhängig von der Lagerkomplexitätsebene, ausgeführt werden.  

|Art|Eingangsprozess|Lagerplätze|Geb. Umlag.-Eingänge|Einlagerungen|Komplexitätsebene anzeigen (siehe [Designdetails: Lagerhaus-Einrichtung](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Posteinlieferungsschein und die Einlagerung der Auftragszeile|X|||2|  
|F|Posteinlieferungsschein und Einlagerung aus dem Beleg "Lagereinlagerung"|||X|3|  
|L|Posteinlieferungsschein und Einlagerung aus einem Wareneingangsbeleg||X||4/5/6|  
|T|Posteinlieferungsschein aus einem Wareneingangsbeleg und Posteinlagerung aus einem Einlagerungsbeleg||X|X|4/5/6|  

Weitere Informationen finden Sie unter [Designdetails: Eingehender Lagerfluss](../../design-details-inbound-warehouse-flow.md).  

In der folgenden Vorgehensweise wird Methode C in der vorhergegangenen Tabelle beschrieben.  

### Szenario  
Alicia, die Einkäuferin, erstellt eine Bestellung für verschiedene geröstete Bohnen je nach Bedarf. Wenn die kombinierte Lieferung im Lager eingeht, lagert John, der Lagermitarbeiter, die Artikel in die Standardlagerplätze ein, die für die Artikel eingerichtet sind. Wenn John die Belege bucht, werden die Artikel gebucht als im Lager erhalten und verfügbar zum Verkauf oder anderen Bedarf.  

### Schritte
1. Einstellungen auf der Seite **Lagerortkarte**, um die eingehenden Warenflüsse des Unternehmens anzugeben.  

    1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 2.](../../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") öffnet. Symbol. Geben Sie **Lagerorte** ein, und wählen Sie dann den entsprechenden Link.  
    2.  Öffnen Sie die Lagerort-Karte *YELLOW*.  
    3.  Dektivieren Sie den Schalter **Einlagerung erforderlich**.  

2. Bestellung(en) für Wareneingang freigeben.  

    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 3.](../../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") öffnet. Symbol. Geben Sie **Einkaufsbestellungen** ein, und wählen Sie dann den zugehörigen Link.  
    2. Auftrag für Kunde 10000 für den Standort YELLOW auswählen. Lieferantenbestellnummern sind *Y-1* und *Y-2*. Verwenden Sie die Personalisierungstools, wenn **Kreditor-Bestellnummer** Feld nicht sichtbar ist. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](../../ui-personalization-user.md).
    3. Wählen Sie die Aktion **Freigabe**, um das Lager zu informieren, dass die Bestellungen in der Lagerdurchlaufzeit bereit ist, wenn die Lieferung eingeht.  

3. Erstellen Sie den Lagerbeleg, um die gelieferten Artikel entgegenzunehmen und einzulagern
    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 4.](../../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol. Geben Sie **Wareneingänge** ein und wählen Sie dann den entsprechenden Link.
    2. Wählen Sie die Aktion **Neu** aus
    3. Drücken Sie auf der Lagerscheinseite die Eingabetaste, damit automatisch eine Lagerscheinnummer ausgewählt wird
    4. Geben Sie im Feld **Lagerortcode** *YELLOW* ein.
    5. Wählen Sie die **Herkunftsbelege abrufen...** Aktion aus
    6. Wählen Sie zuvor freigegebene Bestellungen von Lieferant 10000 aus und wählen Sie die Schaltfläche **OK**.
        Die Zeilen enthalten einen neuen Eintrag für jede Bestellposition.

4. Passen Sie die Menge an den Eingang basierend auf der erhaltenen Menge an und buchen Sie den Beleg
    1. Zeile mit Artikel *WRB-1000* auswählen.
    2. Wählen Sie *OVERRCPT10* im Feld **Eingangsüberschusscode** aus und ändern Sie den Wert im Feld **Zu empfangende Menge** von *100* bis *110*.
    3. Zeile mit Artikel *WRB-1001* auswählen und 
    4. Ändern Sie in der zweiten Zeile den Wert im Feld **Zu erhaltende Menge** von *200* in *190*.
    5. Wählen Sie die Aktion **Beleg Buchen**.

### Ergebnisse 
 - die gerösteten Bohnen werden jetzt als in bestimmten Behältern eingelagert registriert
 - die Seite **Gebuchte Lagerbelege** wird geöffnet
 - die Seite **Gebuchte Eingangsbelege** wird geöffnet
 - Die Bestellung hat die **erhaltene Menge** für die eingegangenen Positionen aktualisiert
 - Der Artikel **Inventar** wird um die gewählte Menge erhöht
    

## Ausgehender Flow: Komissionierung und Lieferung in erweiterten Lagerkonfigurationen

In [!INCLUDE[prod_short](../../includes/prod_short.md)] können die ausgehenden Prozesse für die Komissionierung und Lieferung auf vier Arten, mit den verschiedenen Funktionen, abhängig von der Lagerkomplexitätsebene, ausgeführt werden.  

|Art|Eingangsprozess|Lagerplätze|Kommissionierungen|Lieferungen|Komplexitätsebene anzeigen (siehe [Designdetails: Lagerhaus-Einrichtung](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Beitragsentnahme und -Lieferung aus der Auftragszeile|X|||2|  
|F|Buchen Sie die Kommissionierung und den Warenausgang aus einem Lagerkommissionierungsbeleg||X||3|  
|L|Buchen Sie die Kommissionierung und den Warenausgang aus einem Warenausgangsbeleg|||X|4/5/6|  
|T|Buchen Sie die Kommissionierung von einem Kommissionierbeleg und buchen Sie den Warenausgang aus einem Warenausgangsbeleg||X|X|4/5/6|  

Weitere Informationen finden Sie unter [Designdetails: Ausgehender Lagerfluss](../../design-details-outbound-warehouse-flow.md).  

In der folgenden Vorgehensweise wird Methode D in der vorhergegangenen Tabelle beschrieben.

### Szenario  
Susan, die Auftragsbearbeiterin, erstellt einen Verkaufsauftrag für verschiedene geröstete Bohnen und übergibt ihn an das Lager. Da alle Bestellungen vom selben Kunden kommen, beschließt die Lagerleiterin Ellen, sie zusammen zu versenden. John, der Lagermitarbeiter muss sicherstellen, dass die Lieferung an den Debitor vorbereitet und geliefert wird.

### Schritte
Das ist eine Fortsetzung von [Eingeheder Flow: Eingang und Einlagerung in Basis-Lagerkonfigurationen](#inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations).

1. Bestellung(en) für Wareneingang freigeben.  

    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 5.](../../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.  
    2. Auftrag für Kunde 10000 für den Standort YELLOW auswählen. Externe Bestellnummern sind *Y-3*, *Y-4* und *Y- 5*.
    3. Wählen Sie die Aktion **Freigeben**, um das Lager zu informieren, dass der ausgewählte Verkaufsauftrag im Lager bereit ist.  

2. Zu versendende Artikel  
    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 6.](../../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol. Geben Sie **Warenausgänge** ein und wählen Sie dann den entsprechenden Link.  
    2. Wählen Sie die Aktion **Neu**.  
    3. Geben Sie im Feld **Lagerortcode** *YELLOW* ein.  
    4. Wählen Sie die **Filter zum Holen von Herk.-Belegen verwenden** Aktion aus.  
    5. Geben Sie in das Feld **Code** **CUST10000** ein.  
    6. Geben Sie in das Feld **Beschreibung** **Kunde 10000** ein.  
    7. Wählen Sie die Aktion **Bearbeiten** aus.  
    8. Geben Sie im Inforegister **Verkauf** im Feld **Verkauf an Kunden-Nr. Filter** den Wert *10000* ein.  
    9. Wählen Sie die Aktion **Ausführen** aus. 
    
    Der Warenversand wird mit vier Zeilen gefüllt, die Verkaufszeilen für die angegebenen Kreditoren darstellen. Das Feld **Menge. für Versand** ist leer, da Artikel zuerst kommissioniert werden müssen.

3. Erstellen Sie die Lagerkommissionierung aus der Lagerlieferung
    1. Wählen Sie auf der Seite Warenausgang die Aktionen **Kommissionierung erstellen** aus.
    2. Bestätigen Sie alle erforderlichen Auswahleinstellungen, wählen Sie beispielsweise *Element* im Feld **Sortiermethode für Aktivitätszeile** aus, um gleiche Elemente zusammen zu gruppieren. Wählen Sie die Schaltfläche **OK**.
    3. Sie erhalten eine Bestätigungsnachricht mit der Auswahlnummer. 

4. Öffnen Sie die Lagerkommissionierung
    1. Verwenden Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 7.](../../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **Lager-Kommissionierungen** ein und wählen Sie dann den zugehörigen Link.
    2. Suchen Sie die Auswahl, die Sie erstellt haben, und öffnen Sie sie.
    3. Aktualisieren Sie die **Zu handhabende Menge** falls erforderlich.
    4. Wählen Sie die Aktion **Auswahl registrieren**.
    5. Die Lagerkommissionierung wird geschlossen und entfernt, wenn alle Mengen bearbeitet wurden.

5. Den Lagerversand buchen
   1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 8.](../../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol. Geben Sie **Warenausgänge** ein und wählen Sie dann den entsprechenden Link.  
   2. Suchen Sie den Versand, den Sie zuvor erstellt haben, und öffnen Sie ihn.
    Achten Sie darauf, dass **Menge. zum Versand** ausgefüllt ist.
    3. Sie können **Buchungsdatum**, **Externe Dokumentnummer**, **Versandagentcode**, **Versandmethode** nach Bedarf aktualisieren. Nicht leere Werte werden an Quelldokumente weitergegeben.
    4. Wählen Sie dann die Aktion **Versand buchen** aus.
    5. Bestätigen Sie die Option **Versenden** .

### Ergebnisse
 - die gerösteten Bohnen werden jetzt als aus bestimmten Behältern entnommen registriert 
 - die **Registrierte Lager-Kommissionierung** wird erstellt
 - die Seite **Gebuchter Lagerversand** wird geöffnet
 - die drei **Gebuchte Verkaufslieferungen** werden erstellt
 - der Verkaufsauftrag hat die **versandte Menge** für die versandten Positionen aktualisiert
 - Der Artikel **Bestand** wird um die gewählte Menge reduziert


## Weitere Informationen
[Empfangene Artikel](../../warehouse-how-receive-items.md)
[Basic-Lagerl mit Arbeitsbereich einrichten](../../warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)
[Details festelgen: Eingehender Lager-Flow](../../design-details-inbound-warehouse-flow.md)
[Versandartikel](../../warehouse-how-ship-items.md)
[Artikel für Lagerversand entnehmen](../../warehouse-how-to-pick-items-for-warehouse-shipment.md)
[Details entwerfen: Ausgehender Lagerflow](../../design-details-outbound-warehouse-flow.md)
[Verfügbarkeit von Artikeln anzeigen](../../inventory-how-availability-overview.md)
