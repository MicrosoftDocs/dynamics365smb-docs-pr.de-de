---
title: 'Wareneingang, Einlagerung, Umlagerung, Kommissionierung und Versand in der erweiterten Lagerkonfiguration mit gezielter Kommissionierung und Einlagerung'
description: 'Die ein- und ausgehenden Prozesse für das Empfangen und Einlagern auf vier Arten, mit den verschiedenen Funktionen, immer abhängig von der Lagerkomplexitätsebene, ausgeführt werden.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: null
ms.date: 04/01/2021
ms.author: bholtorf
---

# <a name="walkthrough-of-inbound-and-outbound-flow-in-advanced-warehouse-configuration"></a>Exemplarische Vorgehensweise des eingehenden und ausgehenden Flows in der erweiterten Lagerkonfiguration mit gesteuerter Einlagerung und Kommissionierung

Diese exemplarische Vorgehensweise zeigt, wie eingehende und ausgehende Flows in der Konfiguration Erweitert: Gezielte Einlagerung und Kommissionierung abgeschlossen werden. Weitere Informationen finden Sie unter [Übersicht über verschiedene Konfigurationsoptionen](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## <a name="prerequisites"></a>Voraussetzungen
Um diese exemplarische Vorgehensweise zu beenden, müssen Sie selber einen Lagermitarbeiter am Standort *WEISS* mit folgenden Schritten erstellen:  
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 1.](../../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Lagermitarbeiter** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie das Feld **Benutzer-ID** aus, und wählen Sie Ihr eigenes Benutzerkonto auf der Seite **Benutzer** aus.  
3. Geben Sie im Feld **Lagerortcode** WHITE ein.  
4. Aktivieren Sie die Umschaltung **Standard**.


## <a name="scenario"></a>Szenario
Ellen, die Lagerleiterin, nutzt Cross-Docking- und Behälternachschubfunktionen, um die Wareneingangs- und Versandzeit zu verkürzen.  

## <a name="steps"></a>Schritte

1. Warenausgang erstellen.  

    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 2.](../../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") öffnet. Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.  
    2. Auftrag für Kunde 10000 für den Standort WEISS auswählen. Die externe Bestellnummer lautet *W-1*.
    3. Wählen Sie im Herkunftsbeleg die Aktion **Warenausgang erstellen** aus, um einen Warenausgang für den ausgewählten Verkaufsauftrag zu erstellen.
    4. Wählen Sie die Aktion **Freigeben**, um das Lager zu informieren, dass der Versand im Lager bereit ist.  

2. Definieren Sie Lagerplätze für den Artikel, um zu steuern, wo er eingelagert wird 

    1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 3.](../../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") öffnet. Symbol einrichten möchten, geben Sie **Artikel** ein und wählen dann den entsprechenden Link.  
    2.  Wählen Sie *WBR-1000* und wählen Sie die Aktion **Behälter-Inhalte**.  
    3.  Wählen Sie die Aktion **Neu**. Zwei Zeilen hinzufügen.
    
    |Option|Lagerortcode|Lagerplatzcode|Behoben|Maßeinheit|
    |----------|----------|---------|---|------|  
    |WRB-1000|WEISS|W-05-0001|Ja|TASCHE|  
    |WRB-1000|WEISS|W-05-0002|Ja|TASCHE|

3. Wareneempfang erstellen.  

    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 4.](../../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol. Geben Sie **Einkaufsbestellungen** ein, und wählen Sie dann den zugehörigen Link.  
    2. Auftrag für Kunde 10000 für den Standort WEISS auswählen. Bestellnummer lautet *W-2*. Verwenden Sie die Personalisierungstools, wenn **Kreditor-Bestellnummer** Feld nicht sichtbar ist. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](../../ui-personalization-user.md).
    3. Wählen Sie im Herkunftsbeleg die Aktion **Warenausgang erstellen** aus, um einen Warenempfang für den ausgewählten Verkaufsauftrag zu erstellen.


4. Überprüfen Sie, ob es ausgehende Bestellungen gibt, die empfangene Artikel benötigen, und buchen Sie die Quittung
    1. Wählen Sie die Aktion **Zuordnung berechnen** aus. Dadurch wird eine Spalte **Menge zum Cross-Dock** ausgefüllt.
    2. Geben Sie 0 in das Feld **Menge zu Cross Dock** in der Zeile mit Artikel *WRB-1000* ein, da Sie nicht vorhaben, im Wareneingangsbereich umzupacken.
    3. Wählen Sie die Aktion **Beleg Buchen**.

5. So registrieren Sie eine Wareneinlagerung
    1. Verwenden Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 5.](../../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Geben Sie **Lagereinlagerungen** ein, und wählen Sie dann die zugehörige Verknüpfung aus.
    2. Suchen Sie das Lagereinlagerungsdokument, das aus Ihrem Wareneingang erstellt wurde, und öffnen Sie es
    3. Überprüfen Sie auf der Seite **Lagereinlagerung** den Abschnitt **Positionen**

    In diesem Stadium wird die Lagerplatz-Kapazitätslogik offenbart. Die Lagereinlagerungszeilen haben drei Zeilen für Artikel *WRB-1000*:
    - A Entnahmeleitung zum Abtransport der eingegangenen Mengen am Lagerplatz (W-08-0001)
    - Eine Platzierungslinie, die einen Beutel in einen der konfigurierten festen Behälter bewegt (W-05-0001)
    - Eine Platzierungslinie, die einen anderen BAG in einen anderen festen Behälter bewegt (W-05-0002). Dies liegt daran, dass ein einzelner fester Lagerplatz nicht die vollständige Wareneingangsmenge enthalten kann.

    Da diese Einlagerung Zuordnungspositionen enthält, sehen Sie drei Zeilen für Artikel *WRB-1001*:
    -  A Entnahmeleitung zum Abtransport der eingegangenen Mengen am Lagerplatz (W-08-0001)
    -  A Platzieren Sie die Linie für die 2 in den Cross-Dock-Behälter
    -  A Platzieren Sie die Restmenge am Lagerplatz

    4. Wählen Sie die Aktion **Einlagerung erstellen** aus.


6. Definieren Sie Lagerplätze für den Artikel, um zu steuern, wo er entnommen wird 

    1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 6.](../../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol. Geben Sie **Lagerorte** ein, und wählen Sie dann den entsprechenden Link.  
    2.  Öffnen Sie die *WHITE* Lagerortkarte.  
    3.  Wählen Sie die Aktion **Behälter** in der **Standortkarte**
    4.  Wählen Sie Lagerplatz *W-02-0001* und wählen Sie die Aktion **Inhalte**.  
    5.  Wählen Sie die Aktion **Neu**.  
    6.  Aktivieren Sie die Umschaltung **Fest**.  
    7.  Geben Sie im Feld **Belegnr.** den Wert *RB-1000* ein. 
    8.  Geben Sie im Feld **Mindestmenge** den Wert *2* ein. 
    9.  Geben Sie im Feld **Maximale Menge** den Wert *10* ein. 

    Verwenden Sie die Personalisierungstools, wenn die Felder **Min. Menge** und **Max. Menge** nicht sichtbar sind. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](../../ui-personalization-user.md). 

7. Reorganisieren Sie das Lager, indem Sie Artikel aus dem Massenlagerbereich in den Kommissionierbereich verschieben, um die Kommissionierzeit zu optimieren.

    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 7.](../../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **Arbeitsblätter für Lagerplatzumlagerungen** ein und wählen Sie dann den zugehörigen Link
    2. Wählen Sie die Aktion **Lagerplatzauffüllung berechnen**. 

    Das Lagerarbeitsblatt mit Vorschlag zum Bewegen des Artikels *WRB-1000* vom Blocklager zum Kommissionierbereich wird erstellt.

    3. Wählen Sie die Aktion **Umlagerung erstellen**, um das Dokument zu erstellen und zu bestätigen.
    4.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 8.](../../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **Warenausgänge** ein und wählen Sie dann den entsprechenden Link
    5.  Öffnen Sie die von Ihnen erstellte Warenlagerbewegung und überprüfen Sie den Abschnitt **Positionen**

     In dieser Phase wird die Break-Bulk-Funktionalität offenbart. Es wird vier Zeilen geben:
    - Eine Zeile, um den einen BEUTEL dem Massenlagerplatz zu entnehmen
    - Eine Linie, um die 48 PCS wieder in denselben Behälter einzulagern. 
    - Eine Zeile, um die 10 STK. dem Massenlagerplatz zu entnehmen
    - Eine Zeile, um die 10 STK an den Lagerplatz zu legen

    6.  Wählen Sie die Aktion **Lagerbestandsumlagerung registrieren** aus.

8. Lagerentnahme erstellen

    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 9.](../../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **Arbeitsblätter** ein, und wählen Sie dann den zugehörigen Link
    2. Wählen Sie die Aktion **Lagerdokumente abrufen**, markieren Sie die Zeile für den Verkaufsauftrag für Kunde 10000 und wählen Sie dann die **OK** Schaltfläche, um die Arbeitsblattzeilen gemäß dem ausgewählten Dokument zu füllen.

    3. Überprüfen Sie die **Menge. auf dem Feld Cross-Dock Bin** . 

    4. Wählen Sie die Aktion **Kommissionierung erstellen** aus.
    5. Bestätigen Sie alle erforderlichen Auswahleinstellungen, aktivieren Sie beispielsweise die Umschaltung **Pro von Zone**. Wählen Sie die Schaltfläche **OK**.
    
    Sie erhalten eine Bestätigungsnachricht mit den Auswahlnummern. Es gibt zwei Kommissionierungen, da sich einige Artikel in der Cross-Dock-Zone in der Nähe des Versandbereichs befinden und es sinnvoll wäre, sie getrennt zu bearbeiten.

9.  So registrieren Sie die Lagerkommissionierung
    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 10.](../../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **Lager-Kommissionierungen** ein und wählen Sie dann den zugehörigen Link.
    2. Suchen Sie die Auswahl, die Sie erstellt haben, und öffnen Sie sie.
    3. Wählen Sie die Aktion **Auswahl registrieren**.
    4. Wiederholen Sie dies für die zweite Auswahl

10. Den Lagerversand buchen
    
    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 11.](../../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol. Geben Sie **Warenausgang** ein und wählen Sie dann den zugehörigen Link.
    2. Überprüfen Sie auf der Seite Lagerversand den Abschnitt **Positionen**. Nachdem die Lagerentnahme registriert wurde, wird die Lagerlieferung mit der **Menge aktualisiert. zum Versand** ausgefüllt.
    3. Wählen Sie dann die Aktion **Versand buchen** aus.
    4. Bestätigen Sie die Option **Versenden** .


## <a name="results"></a>Ergebnisse
- die Seite **Gebuchte Lagerbelege** wird geöffnet
- die **Registrierte Lager-Einlagerung** wird erstellt    
- die Seite **Gebuchte Eingangsbelege** wird geöffnet    
- Die **Bestellung** hat die **erhaltene Menge** für die eingegangenen Positionen aktualisiert
- die **Registrierte Lager-Bewegung** wird erstellt
- die **Registrierte Lager-Kommissionierung** wird erstellt
- die Seite **Gebuchter Lagerversand** wird geöffnet
- die **Gebuchte Verkaufslieferung** wird erstellt
- der **Verkaufsauftrag** hat die **versandte Menge** für die versandten Positionen aktualisiert
- Der Artikel **Lagerbestand** wird um alle nicht versendeten Reste erhöht



## <a name="see-also"></a>Weitere Informationen
[Artikel empfangen](../../warehouse-how-receive-items.md) 
[Design Details: Eingehender Lagerflow](../../design-details-inbound-warehouse-flow.md) 
[Versandartikel](../../warehouse-how-ship-items.md) 
[Artikel für den Lagerversand entnehmen](../../warehouse-how-to-pick-items-for-warehouse-shipment.md) 
[Design Details: Ausgehende Lagerflow](../../design-details-outbound-warehouse-flow.md) 
[Verfügbarkeit von Artikel anzeigen](../../inventory-how-availability-overview.md) 
