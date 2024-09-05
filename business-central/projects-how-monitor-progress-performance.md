---
title: Projektfortschritt und -leistung überwachen
description: 'Beschreibt, wie Sie eine WIP-Methode (Work in Process) erstellen und WIP berechnen können, um den finanziellen Wert laufender Projekte zu schätzen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 08/19/2024
ms.custom: bap-template
ms.search.keywords: 'project management, KPI, work in process, work in progress'
ms.search.form: '89, 92, 1010'
ms.service: dynamics-365-business-central
---

# <a name="monitor-project-progress-and-performance"></a>Projektfortschritt und -leistung überwachen

Mit der Funktion Umlaufbestand (WIP) können Sie den finanziellen Wert laufender Projekte in der Finanzbuchhaltung schätzen.

Im Laufe eines Projekts werden Material sowie Ressourcen verbraucht und Aufwendungen erbracht, die auf das Projekt gebucht werden müssen. In vielen Fällen werden die Aufwendungen für ein Projekt vor der Fakturierung gebucht. Wenn Sie jedoch nur die Ausgaben verbuchen, ist Ihre Bilanz ungenau. Um den tatsächlichen Wert des Projekts zu verfolgen, berechnen Sie den WIP und buchen Sie ihn im Hauptbuch. Die folgenden WIP-Methoden sind sofort verfügbar:

* Einstandswert
* Verkaufswert
* Realisierbare Kosten
* Prozentsatz der Fertigung
* Abgeschl. Vertrag

Sie können auch eine WIP-Methode erstellen, die den Anforderungen Ihrer Organisation entspricht, und diese als Standard festlegen.  

Erfahren Sie mehr unter [WIP-Methoden verstehen](projects-understanding-wip.md).

Wenn Sie das Ergebnis mit einer anderen Methode anzeigen möchten, ändern Sie die Methode und berechnen Sie den WIP erneut. Sie können den WIP beliebig oft berechnen. Der Wert wird nicht automatisch im Hauptbuch gebucht. Nachdem Sie die WIP mit der von Ihnen bevorzugten Methode berechnet haben, können Sie in das Hauptbuch buchen.

1. Wählen Sie das ![Glühbirne, die das „Sie wünschen ...“-Feature öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie  **Projekt-WIP-Methoden** ein und wählen Sie dann das zugehörige verknüpfen aus.  
2. Wählen Sie die Aktion **Neu** aus, und füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Schließen Sie die Seite.   
4. Um diese neue Methode zur Standardmethode zu machen, wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol, geben Sie  **Projekt-Setup** ein und wählen Sie dann das zugehörige verknüpfen.  
5. Wählen Sie im Feld **WIP-Standardmethode** die Methode aus der Liste aus.

## <a name="define-a-wip-method-for-a-project"></a>Eine WIP-Methode für ein Projekt definieren

Wenn Sie ein neues Projekt erstellen, müssen Sie auswählen, welche Projekt-WIP-Methode angewendet werden soll. In einigen Fällen ist die von Ihnen verwendete Projekt-WIP-Methode bereits als Standard festgelegt.

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Projekte** ein und wählen Sie den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu**. Erfahren Sie mehr unter [Projekte erstellen](projects-how-create-jobs.md).  
3. Wählen Sie auf der Seite  **Projekt Karte**  im Feld  **WIP-Methode**  auf der Registerkarte  **Buchen**  eine WIP-Methode aus der Liste aus. Wenn eine Standardmethode definiert ist, können Sie bei Bedarf eine andere Option Auswählen verwenden.  

### <a name="define-a-wip-method-for-a-project-task"></a>Eine WIP-Methode für eine Projektaufgabe definieren

Sie können eine WIP-Methode für ein Projekt Aufgabe definieren, Projektaufgaben von der WIP-Berechnung ausschließen oder Aufgaben gruppieren, die gemeinsam berechnet werden sollen.

Wenn Sie den WIP für jede Projektaufgabe einzeln berechnen möchten, bietet die WIP-Buchung definierte Dimensionen für die spezifischen Aufgaben.

**WIP-Summe** legt Projektaufgaben fest, die sie zusammen gruppieren, wenn Sie WIP und Erkennung berechnen. In jeder Gruppe von Aufgaben muss eine Aufgabe vorhanden sein, die zwei Bedingungen erfüllt:
<!--But doesn't the parenthetical below contradict this -* if there is no total, the application sets the total for you, meaning the condition does not HAVE to be satisfied, right? Or am I missing something?-->

* **WIP-Total** wird auf  **Gesamt** gesetzt. Wenn es keine Projektaufgaben gibt, bei denen  **WIP-Total** auf „Gesamt“ gesetzt ist, wird „Gesamt“ automatisch in der letzten Zeile des Projekts Aufgabe gesetzt, wenn WIP zum ersten Mal berechnet wird.
* Die Nummer im Feld  **Projekt-Nr. Aufgabe**  ist die letzte in der Gruppe oder dem Bereich der Projektaufgaben.

In der folgenden Tabelle werden die Optionen beschrieben:

| Feld | Description |
|--|--|
| **\<blank\>** | Lassen Sie dieses Feld leer, wenn die Projektaufgabe ein Teil einer Gruppe von Aufgaben ist. |
| **Total** | Definiert den Bereich oder die Gruppe von Aufgaben, die in der WIP- und Umsatzrealisierungsberechnung berücksichtigt sind. Innerhalb der Gruppe ist jede Projektaufgabe, deren **Projektaufgabenart** auf **Buchen** festgelegt ist, in der WIP-Summe enthalten, es sei denn, das Feld **WIP-Summe** der Aufgabe ist auf **Ausschließlich** festgelegt. |
| **Ausschließlich** | Gilt nur für eine Aufgabe mit **Projektaufgabentyp** von **Buchung**, in diesem Fall wird die Aufgabe bei der Berechnung von WIP und Erfassung nicht berücksichtigt. |

Im folgenden Beispiel werden Projektaufgaben in zwei WIP-Gesamtgruppierungen unterteilt, um zu zeigen, wie das Feld **WIP-Gesamt** funktioniert:

|Projektaufgabennr.|Description|Projektaufgabentyp|**WIP-Summe** Feld|  
|------------------|----------------------|----------------------|----------------------|  
|1000|Vorbereitung|Von-Summe|\<blank\>|
|1010|.    Reinigung|Buchen|**Ausschließlich**|
|1099|Gesamtvorbereitung|Bis-Summe|\<blank\>|
|1100|Teppich verlegen|Von-Summe|\<blank\>|
|1110|.    Kleber auftragen|Buchen|**Ausschließlich**|
|1120|.    Teppich auslegen|Buchen|\<blank\>|
|1199|Teppich-Gesamtarbeiten|Bis-Summe|\<blank\>|
|1200|Beenden|Von-Summe|\<blank\>|
|1210|.    Teppich saugen|Buchen|\<blank\>|
|1299|Gesamtfertigstellung|Bis-Summe|**Summe**|
|1300|Nachbesserung|Von-Summe|\<blank\>|
|1310|.    Nachbesserung|Buchen|\<blank\>|
|1399|Nachbesserung gesamt|Bis-Summe|**Total**|

Sie bemerken:

* Für  *1000* bis *1299* wird der WIP für diese Gruppe von Projektaufgaben separat berechnet. Beachten Sie jedoch, dass zwei der Aufgaben, 1010 und 1110, von der WIP-Berechnung ausgeschlossen sind, da ihr Projekttyp Aufgabe  **Buchung** ist.
* Von *1300* bis *1399* wird der WIP für diese Gruppe von Projektaufgaben separat berechnet.

## <a name="calculate-wip"></a>WIP berechnen

Mithilfe der Stapelverarbeitung  **Projekt-WIP-Betrag berechnen**  können Sie den WIP-Betrag ermitteln, der für die Berichterstattung zum Periodenende auf die Bilanzkonten gebucht werden soll.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie  **Projekt „WIP berechnen“** ein und wählen Sie dann das zugehörige verknüpfen aus.  
2. Wählen Sie die Aktion **WIP berechnen** aus.
3. Geben Sie auf der Seite **WIP berechnen Projekt** die notwendigen Felder ein.
4. Wählen Sie die Schaltfläche **OK**.  

> [!NOTE]  
> Der Batchauftrag berechnet lediglich den WIP, bucht ihn aber nicht ins Hauptbuch. Um WIP zu buchen, führen Sie den Stapelverarbeitungsauftrag  **WIP ins Hauptbuch buchen**  aus, nachdem Sie den WIP berechnet haben. Erfahren Sie mehr im folgenden Verfahren.

### <a name="review-warnings"></a>Warnungen überprüfen

Wenn Ihre WIP-Berechnung die Meldung  *WIP wurde mit Warnungen berechnet*  ergibt, sollten Sie die Warnungen überprüfen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Projekt – WIP-Cockpit** ein, und wählen Sie dann den entsprechenden Link aus.  
2. Auswählen das Projekt, für das Sie Warnungen überprüfen möchten. Der Schalter  **WIP-Warnungen**  ist für Projekte aktiviert, die WIP-Warnungen haben.
3. Wählen Sie die Aktion  **Warnung anzeigen** .

### <a name="delete-wip-entries"></a>WIP-Einträge löschen

Wenn Sie verschiedene WIP-Methoden ausprobieren möchten, erhalten Sie möglicherweise die Fehlermeldung  *Das Projekt Aufgabe kann nicht geändert werden, da dem Projekt WIP-Projekteinträge zugeordnet sind* . Um die WIP-Methode prüfen zu können, löschen Sie vorhandene WIP-Einträge.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Projekt – WIP-Cockpit** ein, und wählen Sie dann den entsprechenden Link aus.  
2. Auswählen das Projekt, für das Sie WIP-Einträge löschen möchten.
3. Wählen Sie die Aktion  **WIP-Einträge löschen** .

## <a name="post-wip"></a>WIP buchen

Wenn Sie die WIP berechnen, können Sie diese für die Berichterstattung zum Periodenende auf Bilanzkonten buchen. Verwenden Sie den Stapelverarbeitungsauftrag  **Projekt WIP ins Hauptbuch buchen** .

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie  **Projekt „WIP in Hauptbuch buchen“** ein und wählen Sie dann die zugehörige Nummer verknüpfen aus.  
2. Füllen Sie auf der Seite **WIP nach Sachkonten Projekt** aus und füllen Sie die Felder wie erforderlich aus.  
3. Wählen Sie die Schaltfläche **OK**.

## <a name="calculate-and-post-project-completion-entries"></a>Berechnen und Buchen von Projekt-Abschlussposten

Nachdem Sie alle Aktivitäten für ein Projekt abgeschlossen haben, einschließlich der Nutzungsbuchung und Rechnungsstellung, müssen Sie den Status des Projekts auf  **Abgeschlossen** aktualisieren. Anschließend müssen Sie sämtliche im Hauptbuch gebuchten WIP stornieren.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Projekte** ein und wählen Sie den zugehörigen Link aus.  
2. Wählen Sie ein offenes Projekt und dann die Aktion **Bearbeiten** aus.
3. Geben Sie auf der Registerkarte  **Buchung**  im Feld  **Status**  Auswählen **Abgeschlossen** ein.
4. Befolgen Sie die Hilfsschritte, um den WIP zu berechnen und zu buchen, oder befolgen Sie die Schritte 5 und 6, um dies manuell zu tun.  
5. Wählen Sie die Aktion **WIP berechnen** aus.
6. Geben Sie auf der Seite **WIP berechnen Projekt** die notwendigen Felder ein.  

     Bei den durch Ausführen des Stapelauftrags erstellten WIP-Projekteinträgen ist das Kontrollkästchen  **Projekt abgeschlossen**  aktiviert, um anzuzeigen, dass es sich um Abschlusseinträge handelt.  
7. Wählen Sie die Aktion **WIP nach Sachkonten** aus.
8. Füllen Sie auf der Seite **WIP nach Sachkonten Projekt** aus und füllen Sie die Felder wie erforderlich aus.  

     Bei den durch Ausführen des Batchprojekts erstellten WIP-Hauptbucheinträgen des Projekts ist das Kontrollkästchen  **Projekt abgeschlossen**  aktiviert, um anzuzeigen, dass es sich um Abschlusseinträge handelt.

## <a name="view-project-ledger-entries"></a>Projektposten anzeigen

Alle projektbezogenen Posten werden in Projektjournalen aufgezeichnet und fortlaufend nummeriert, beginnend mit 1. Aus den Projektjournalen können Sie eine Übersicht über alle Projektposten erhalten.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Projektjournale** ein und wählen Sie den zugehörigen Link aus.
2. Wählen Sie ein entsprechendes Journal und dann die Aktion **Projektposten** aus.

Auf der Seite  **Projektbucheinträge**  können Sie die Einträge überprüfen, die einem Projekt zugeordnet sind.  

## <a name="see-also"></a>Siehe auch

[exemplarische Vorgehensweise: Berechnen der laufenden Arbeit für ein Projekt](walkthrough-calculating-work-in-process-for-a-job.md)    
[Projekte verwalten](projects-manage-projects.md)    
[Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)    
[Finanzen](finance.md)    
[Einkauf](purchasing-manage-purchasing.md)    
[Verkauf](sales-manage-sales.md)    
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
