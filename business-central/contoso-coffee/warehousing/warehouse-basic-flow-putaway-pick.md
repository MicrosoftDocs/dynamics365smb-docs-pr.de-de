---
title: 'Eingang, Einlagerung, Kommissionierung und Versand in Basis-Lagerkonfigurationen'
description: 'In Business Central können die ein- und ausgehenden Prozesse für das Empfangen und Einlagern auf vier Arten, mit den verschiedenen Funktionen, immer abhängig von der Lagerkomplexitätsebene, ausgeführt werden.'
author: andreipanko
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: null
ms.date: 04/01/2021
ms.author: andreipa
---

# <a name="walkthrough-of-inbound-and-outbound-flow-in-basic-warehouse-configurations" />Exemplarische Vorgehensweise für ein- und ausgehende Flows in Basis-Lagerkonfigurationen

Diese exemplarische Vorgehensweise zeigt, wie eingehende und ausgehende Flows in der Basis-Auftrag-für-Auftrag-Konfiguration abgeschlossen werden. Weitere Informationen finden Sie unter [Übersicht über verschiedene Konfigurationsoptionen](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## <a name="prerequisites" />Voraussetzungen
Um diese exemplarische Vorgehensweise zu beenden, müssen Sie selber einen Lagermitarbeiter am Standort *SILBER* mit folgenden Schritten erstellen:  
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 1.](../../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Lagermitarbeiter** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie das Feld **Benutzer-ID** aus, und wählen Sie Ihr eigenes Benutzerkonto auf der Seite **Benutzer** aus.  
3. Geben Sie im Feld **Lagerortcode** *SILBER* ein.  

## <a name="inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations" />Eingeheder Flow: Eingang und Einlagerung in Basis-Lagerkonfigurationen

In [!INCLUDE[prod_short](../../includes/prod_short.md)] können die eingehenden Prozesse für das Empfangen und Einlagern auf vier Arten, mit den verschiedenen Funktionen, abhängig von der Lagerkomplexitätsebene, ausgeführt werden.  

|Art|Eingangsprozess|Lagerplätze|Geb. Umlag.-Eingänge|Einlagerungen|Komplexitätsebene anzeigen (siehe [Designdetails: Lagerhaus-Einrichtung](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Posteinlieferungsschein und die Einlagerung der Auftragszeile|X|||2|  
|F|Posteinlieferungsschein und Einlagerung aus dem Beleg "Lagereinlagerung"|||X|3|  
|L|Posteinlieferungsschein und Einlagerung aus einem Wareneingangsbeleg||X||4/5/6|  
|T|Posteinlieferungsschein aus einem Wareneingangsbeleg und Posteinlagerung aus einem Einlagerungsbeleg||X|X|4/5/6|  

Weitere Informationen finden Sie unter [Designdetails: Eingehender Lagerfluss](../../design-details-inbound-warehouse-flow.md).  

In der folgenden Vorgehensweise wird Methode B in der vorhergegangenen Tabelle beschrieben.  

### <a name="scenario" />Szenario
Alicia, die Einkäuferin, erstellt eine Bestellung für verschiedene geröstete Bohnen. Wenn die Lieferung im Lager ankommt, räumt John, der Lagerarbeiter, die Artikel in geeignete Behälter. Wenn John die Einlagerung bucht, werden die Artikel wie erhalten in den Bestand gebucht und stehen zum Verkauf oder für andere Nachfrage zur Verfügung.  

### <a name="steps" />Schritte
1. Einstellungen auf der Seite **Lagerortkarte**, um die eingehenden Warenflüsse des Unternehmens anzugeben.  

    1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 2.](../../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") öffnet. Symbol. Geben Sie **Lagerorte** ein, und wählen Sie dann den entsprechenden Link.  
    2.  Öffnen Sie die Karte für den Standort *SILVER*.  
    3.  Aktivieren Sie das Kontrollkästchen **Einlagerung erforderlich**  

2. Definieren Sie einen Standard-Lagerplätze für den Artikel, um zu steuern, wo er eingelagert wird

    1.  Wählen Sie die Aktion **Behälter** in der **Standortkarte**
    2.  Wählen Sie die erste Zeile, für den Lagerplatz *S-1-01*, und wählen die **Inhalt**-Aktion aus.  
    3.  Wählen Sie die Aktion **Neu**.  
    4.  Wählen Sie die Felder **Fest** und **Standard** .  
    5.  Geben Sie im Feld **Belegnr.** den Wert *RB-1000* ein.  

3. Bestellungen sind die häufigste Art des eingehenden Herkunftsbelegs.  

    1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 3.](../../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") öffnet. Symbol. Geben Sie **Einkaufsbestellungen** ein, und wählen Sie dann den zugehörigen Link.  
    2.  Wählen Sie die Aktion **Neu**.  
    3.  Erstellen Sie eine Bestellung für den Kreditor 10000 auf das Arbeitsdatum mit den folgenden Einkaufszeilen. Verwenden Sie die Personalisierungstools, wenn ein **Behältercode** nicht sichtbar ist. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](../../ui-personalization-user.md). 

    |Artikel|Lagerortcode|Lagerplatzcode|Menge|  
    |----------|----------|---------|--------------|  
    |WRB-1000|SILBER|S-1-01|20|  
    |WRB-1001|SILBER||30|

    Der Bin-Code im ersten wird entsprechend zum Einrichten ausgefüllt. Der Lagerplatzcode für den zweiten Artikel ist leer, da er keine Standardwerte hat. Lassen Sie dies so.  

    4.  Wählen Sie die Aktion **Freigabe**, um das Lager zu informieren, dass die Einkaufsbestellung in Lagerdurchlaufzeit bereit ist, wenn die Lieferung eingeht.  

4. Erstellen Sie **Bestandseinlagerung**, um die gelieferten Artikel entgegenzunehmen und einzulagern  

    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 4.](../../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol. Geben Sie **Lagereinlagerungen** ein und wählen Sie dann den zugehörigen Link.  
    2. Wählen Sie die Aktion **Neu**. 
    3. Wählen Sie im Feld *Lagerortcode* **SILVER** aus.
    4. Wählen Sie das Feld **Herkunftsdokument** , und wählen Sie **Einkaufsauftrag** aus.  
    5. Wählen Sie das Feld **Quellennummer**, markieren Sie die Zeile für den Einkauf bei Lieferant 10000 und wählen Sie dann die **OK** Schaltfläche, um die Einlagerungszeilen gemäß dem ausgewählten Quelldokument zu füllen.

        Alternativ können Sie auch die Aktion **Quellbeleg holen** wählen und dann die Bestellung auswählen.  

5. Ändern Sie die Bestandseinlagerung basierend auf der tatsächlichen Platzierung von Artikeln und buchen Sie Belege

    Als er Artikel in Behälter legte, bemerkte John, dass der Standardbehälter bereits einige Elemente enthält, also entschied er sich, einen anderen Behälter zu verwenden. John legt auch andere Artikel in die nächsten Behälter, da die empfangene Menge nicht der Kapazität entspricht.

    1. Ändern Sie in der ersten Zeile **Behälter-Code** von *S-1-01*, der aus der Bestellung kopiert wurde, bis *S-1-02*. 
    2.  Geben Sie 20 im Feld **Bewegungsmenge** in der Zeile Lagereinlagerung mit Artikel WBR-1000 ein.  
    3. Geben Sie in der zweiten Zeile 20 in das Feld **Zu bearbeitende Menge** ein und wählen Sie die Aktion **Zeilen teilen** . Eine neue Zeile wird angezeigt, bei der es sich um eine Kopie der Originalzeile handelt. Einziger Unterschied: Das Feld **Bewegungsmenge** enthält die Menge, die aus der ursprünglichen Zeile entfernt wurde. 
    4. Geben Sie die Behältercodes für Artikel WBR-1001 ein:

    |Artikel|Lagerplatzcode|Menge|  
    |----------|-------------------|--------------|  
    |WRB-1001|S-1-03|20|  
    |WRB-1001|S-1-04|10|

    5.  Wählen Sie die Aktion **Buchen** aus, wählen Sie die Option **Lieferung und Rechnung**, und wählen Sie dann die Schaltfläche **OK** aus.  

### <a name="results" />Ergebnisse
 - Die gerösteten Bohnen werden jetzt als in bestimmten Behältern eingelagert registriert
 - die **Posted Invt. Einlagerung** wird erstellt
 - die Seite **Gebuchte Eingangsbelege** wird geöffnet
 - Die Bestellung hat die **erhaltene Menge** für die eingegangenen Positionen aktualisiert
 - Der Artikel **Inventar** wird um die gewählte Menge erhöht
    

## <a name="outbound-flow-picking-and-shipping-in-basic-warehouse-configurations" />Ausgehender Flow: Komissionierung und Lieferung in Basis-Lagerkonfigurationen

In [!INCLUDE[prod_short](../../includes/prod_short.md)] können die ausgehenden Prozesse für die Komissionierung und Lieferung auf vier Arten, mit den verschiedenen Funktionen, abhängig von der Lagerkomplexitätsebene, ausgeführt werden.  

|Art|Eingangsprozess|Lagerplätze|Kommissionierungen|Lieferungen|Komplexitätsebene anzeigen (siehe [Designdetails: Lagerhaus-Einrichtung](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Beitragsentnahme und -Lieferung aus der Auftragszeile|X|||2|  
|F|Buchen Sie die Kommissionierung und den Warenausgang aus einem Lagerkommissionierungsbeleg||X||3|  
|L|Buchen Sie die Kommissionierung und den Warenausgang aus einem Warenausgangsbeleg|||X|4/5/6|  
|T|Buchen Sie die Kommissionierung von einem Kommissionierbeleg und buchen Sie den Warenausgang aus einem Warenausgangsbeleg||X|X|4/5/6|  

Weitere Informationen finden Sie unter [Designdetails: Ausgehender Lagerfluss](../../design-details-outbound-warehouse-flow.md).  

In der folgenden Vorgehensweise wird Methode B in der vorhergegangenen Tabelle beschrieben.

### <a name="scenario-1" />Szenario
Susan, die Auftragsbearbeiterin, erstellt einen Verkaufsauftrag für verschiedene geröstete Bohnen und übergibt ihn an das Lager. John, der Lagermitarbeiter muss sicherstellen, dass die Lieferung an den Debitor vorbereitet und geliefert wird. John verwaltet alle beteiligten Aufgaben auf der Seite **Lagerkommissionierung**, das automatisch auf die Lagerplätze verweist, in denen geröstete Bohnen gespeichert wird.

### <a name="steps-1" />Schritte
Das ist eine Fortsetzung von [Eingeheder Flow: Eingang und Einlagerung in Basis-Lagerkonfigurationen](#inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations).

1. Einstellungen auf der Seite **Lagerortkarte**, um die eingehenden Warenflüsse des Unternehmens anzugeben.  

    1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 5.](../../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol. Geben Sie **Lagerorte** ein, und wählen Sie dann den entsprechenden Link.  
    2.  Öffnen Sie die Karte für den Standort *SILVER*.  
    3.  Aktivieren Sie das Kontrollkästchen **Kommissionierung erforderlich**  

2. Das Erstellen von Bestellungen ist die häufigste Art von ausgehenden Herkunftsbelegen.  

    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 6.](../../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.  
    2. Wählen Sie die Aktion **Neu**.  
    3. Erstellen Sie einen Verkaufsauftrag für Kunde 10000 mit der folgenden Verkaufsauftragsposition.  

    |Artikel|Lagerortcode|Menge|  
    |----|-------------|--------|  
    |WRB-1000|SILBER|20|  
    |WRB-1001|SILBER|30|  

    Die Behältercodes werden automatisch mit Standardbehältern ausgefüllt.

    4. Wählen Sie die Aktion **Lagereinlagerung/Auswahl**.
    5. Aktivieren Sie das Kontrollkästchen **Lagerkomm. erst.**  
    6. Wählen Sie die Schaltfläche **OK**. Eine neue Lagerkommissionierung wird erstellt.

3. ommissionieren Sie Artikel und liefern diese aus

    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 7.](../../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol. Geben Sie **Lagerkommissionierungen** ein und wählen Sie dann den zugehörigen Link.  
    2. Wählen Sie die Bestandskommissionierung für die Verkäufe an Kunde 10000 aus
    
    Die erstellte Bestandskommissionierung ignorierte den für den Artikel *WRB-1000* definierten Lagerplatz, da er keinen Bestand enthält und einen anderen Lagerplatz verwendet hat. Die zweite Zeile mit Artikel *WRB-1001* wurde automatisch aufgeteilt, um aus mehreren Lagerplätzen zu entnehmen.
    
4. Wählen Sie die Aktion **Die zu verarbeitende Menge automatisch ausfüllen**.  

5. Wählen Sie die Aktion **Buchen** und **Versand** und klicken Sie anschließend auf die Schaltfläche **OK**.  

### <a name="results-1" />Ergebnisse
 - Die gerösteten Bohnen werden jetzt als aus bestimmten Behältern entnommen registriert
 - die **Posted Invt. Entnahme** wird erstellt
 - die **Gebuchte Verkaufslieferung** wird erstellt
 - der Verkaufsauftrag hat die **versandte Menge** für die versandten Positionen aktualisiert
 - Der Artikel **Bestand** wird um die gewählte Menge reduziert


## <a name="see-also" />Weitere Informationen
[Eingelagerte Artikel mit Bestandeinlagerung](../../warehouse-how-to-put-items-away-with-inventory-put-aways.md) 
[Grundlager mit Verarbeitungsbereich](../../warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) 
[Details gestalten: Eingehender Lagerflow](../../design-details-inbound-warehouse-flow.md) 
[Artikel entneme mit Bestandentnahme](../../warehouse-how-to-pick-items-with-inventory-picks.md) 
[Details gestalten: Ausgehender Lagerflow](../../design-details-outbound-warehouse-flow.md) 
[Verfügbarkeit von Artikeln anzeigen](../../inventory-how-availability-overview.md) 
