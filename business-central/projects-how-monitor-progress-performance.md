---
title: Überwachen des Status und der Leistung
description: 'Beschreibt, wie Sie eine Umlaufbestand-Methode (WIP) erstellen und WIP berechnen können, um den finanziellen Wert von Projekten zu beurteilen, während sie ausgeführt werden.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 03/28/2023
ms.custom: bap-template
ms.search.keywords: 'project management, KPI, work in process, work in progress'
ms.search.form: '89, 92, 1010'
---
# <a name="monitor-job-progress-and-performance" />Überwachen des Status und der Leistung

Mit der Funktion Umlaufbestand (WIP) können Sie den finanziellen Wert laufender Projekte in der Finanzbuchhaltung schätzen.

Im Laufe eines Projekts werden Material sowie Ressourcen verbraucht und Aufwendungen erbracht, die auf das Projekt gebucht werden müssen. In vielen Fällen werden die Aufwendungen für ein Projekt vor der Fakturierung gebucht. Wenn ausschließlich Aufwendungen gebucht werden, ergibt sich eine inkorrekte Finanzauswertung. Um den tatsächlichen Wert des Auftrags zu verfolgen, berechnen Sie den WIP und buchen Sie ihn im Hauptbuch. Erfahren Sie mehr unter [WIP-Methoden verstehen](projects-understanding-wip.md).

Die WIP-Berechnung kann auf der Grundlage der folgenden Optionen erfolgen:

* Einstandswert
* Verkaufswert
* Realisierbare Kosten
* Prozentsatz der Fertigung
* Abgeschl. Vertrag

<!--If you want to view the result using a different method, change the method and calculate WIP again. There's no limit to the number of times you calculate WIP; it doesn't get automatically posted to the general ledger. After you've calculated WIP using the method you prefer, you can post to the general ledger.-->
<!--Unhide the above paragraph?-->

## <a name="create-a-job-wip-method" />WIP-Methode für ein Projekt erstellen

Erstellen Sie eine WIP-Methode, die den Bedarf Ihrer Organisation wiedergibt und legen Sie sie als Standard fest.  

> [!NOTE]
> Nachdem Sie Ihre neue Methode verwendet haben, um WIP-Posten zu erstellen, können Sie die Methode nicht löschen oder ändern.  

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Job WIP-Methoden für Projekte** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus, und füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Schließen Sie die Seite.   
4. Um diese neue Methode zur Standardmethode zu machen, wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Projekt Einrichtung** ein, wählen Sie den zugehörigen Link.  
5. Wählen Sie im Feld **WIP-Standardmethode** die Methode aus der Liste aus.

## <a name="define-a-wip-method-for-a-job" />Eine WIP-Methode für ein Projekt definieren

Wenn Sie ein neues Projekt erstellen, müssen Sie auswählen, welche WIP-Methode angewendet werden soll. In einigen Fällen ist die von Ihnen verwendete Job-WIP-Methode bereits als Standard festgelegt.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Aufträge** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Neu**. Erfahren Sie mehr unter [Arbeitsplätze schaffen](projects-how-create-jobs.md).  
3. Wählen Sie auf der Seite **Projektkarte** im Feld **WIP-Methode** eine WIP-Methode aus der Liste aus. Wenn eine standardmäßige Methode festgelegt wurde, können Sie sofern erforderlich eine andere Option aktivieren.  

### <a name="define-a-wip-method-for-a-job-task" />Eine WIP-Methode für eine Projektaufgabe definieren

Sie können eine WIP-Methode für eine Arbeitsaufgabe definieren, einige Arbeitsaufgaben von der WIP-Berechnung ausschließen oder Aufgaben gruppieren, die zusammen berechnet werden sollen. 

Wenn Sie den WIP für jede Projektaufgabe einzeln berechnen möchten, bietet die WIP-Buchung definierte Dimensionen für die spezifischen Aufgaben.

**WIP-Summe** legt Projektaufgaben fest, die sie zusammen gruppieren, wenn Sie WIP und Erkennung berechnen. In jeder Gruppe von Aufgaben muss eine Aufgabe vorhanden sein, die zwei Bedingungen erfüllt:
<!--But doesn't the parenthetical below contradict this -* if there is no total, the application sets the total for you, meaning the condition does not HAVE to be satisfied, right? Or am I missing something?-->

* Hat ein **WIP-Gesamt** einstellen auf *Gesamt*. (Falls es keine Projektaufgaben mit der **WIP-Summe** gibt, die auf *Summe* gesetzt ist, wird *Summe* automatisch in der letzten Projektaufgabenzeile festgelegt, wenn die WIP das erste Mal berechnet wird.)

* Hat eine **Projektauftrag**-Nummer, die die letzte in der Gruppe oder im Bereich von Projektaufgaben ist.

Die drei Optionen werden in der folgenden Tabelle beschrieben:

| Feld | Description |
|--|--|
| **\<blank\>** | Lassen Sie dieses Feld leer, wenn die Projektaufgabe ein Teil einer Gruppe von Aufgaben ist. |
| **Summe** | Definiert den Bereich oder die Gruppe von Aufgaben, die in der WIP- und Umsatzrealisierungsberechnung berücksichtigt sind. Innerhalb der Gruppe ist jede Projektaufgabe, deren **Projektaufgabenart** auf **Buchen** festgelegt ist, in der WIP-Summe enthalten, es sei denn, das Feld **WIP-Summe** der Aufgabe ist auf **Ausschließlich** festgelegt. |
| **Ausschließlich** | Gilt nur für eine Aufgabe mit **Projektaufgabentyp** von **Buchung**, in diesem Fall wird die Aufgabe bei der Berechnung von WIP und Erfassung nicht berücksichtigt. |

Im folgenden Beispiel werden Auftragsaufgaben in zwei WIP-Gesamtgruppierungen unterteilt, um zu zeigen, wie die **WIP-Gesamt** Feld funktioniert:

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
|1399|Nachbesserung gesamt|Bis-Summe|**Summe**|

Sie werden feststellen:

* *1000* bis *1299*: Für diese Gruppe von Projektaufgaben werden WIP separat berechnet. Beachten Sie jedoch, dass zwei der Aufgaben, 1010 und 1110, von der WIP-Berechnung ausgeschlossen sind, da ihr Auftragsaufgabentyp ist **Buchung**.

* *1300* bis *1399*: Für diese Gruppe von Projektaufgaben werden WIP separat berechnet.

## <a name="calculate-wip" />WIP berechnen

Bestimmen den WIP-Betrag, der im Rahmen der Berichterstellung am Periodenende auf Bilanzkonten gebucht werden muss. Verwenden Sie dazu die Stapelverarbeitung **WIP berechnen Projekt**.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Job WIP berechnen Projekt** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **WIP berechnen** aus.
3. Geben Sie auf der Seite **WIP für Projekt berechnen** die notwendigen Felder ein.
4. Wählen Sie die Schaltfläche **OK**.  

> [!NOTE]  
>   Der Stapelauftrag berechnet lediglich die WIP, und es erfolgt keine Buchung in die Finanzbuchhaltung. Zum Buchen müssen Sie den Stapelauftrag **WIP nach Sachposten Projekt** ausführen, nachdem Sie den WIP berechnet haben. Erfahren Sie mehr im folgenden Verfahren.

## <a name="post-wip" />WIP buchen

Wenn Sie den WIP berechnet haben, können Sie ihn zur Erstellung von Periodenendberichten auf Bilanzkonten buchen. Dazu verwenden Sie die Stapelverarbeitung **WIP nach Sachposten Projekt**.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Job WIP auf Sachkonten buchen Projekt** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie auf der Seite **WIP nach Sachkonten Projekt buchen** aus und füllen Sie die Felder wie erforderlich aus.  
3. Wählen Sie die Schaltfläche **OK**.

## <a name="calculate-and-post-job-completion-entries" />Berechnen und Buchen von Projekt-Abschlussposten

Nachdem alle Aktivitäten für ein Projekt – einschließlich Buchung des Verbrauchs und Fakturierung – abgeschlossen wurden, muss das Projekt aktualisiert werden, damit es den **Status** **Abgeschlossen** erhält. Dann stornieren Sie alle WIPs, die in der Finanzbuchhaltung gebucht wurde.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Aufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie ein offenes Projekte und wählen Sie dann die Aktion **Bearbeiten** aus.
3. Wählen Sie im Feld **Status** **Abgeschlossen**.
4. Folgen Sie den Hilfeschritten, um den WIP zu berechnen und zu buchen. Oder folgen Sie den Schritten 5 und 6, um dies manuell zu tun.  
5. Wählen Sie die Aktion **WIP berechnen** aus.
6. Geben Sie auf der Seite **WIP für Projekt berechnen** die notwendigen Felder ein.  

     Die WIP-Projektposten, die beim Ausführen der Stapelverarbeitung erstellt wurden, weisen nun ein Häkchen im Feld **Auftrag abgeschlossen** auf, um anzugeben, dass es sich hierbei um Abschlussposten handelt.  
7. Wählen Sie die Aktion **WIP nach Sachkonten Projekt** aus.
8. Füllen Sie auf der Seite **WIP nach Sachkonten Projekt buchen** aus und füllen Sie die Felder wie erforderlich aus.  

     Die WIP-Hauptbuchungsposten, die beim Ausführen der Stapelverarbeitung erstellt wurden, weisen nun ein Häkchen im Feld **Auftrag abgeschlossen** auf, um anzugeben, dass es sich hierbei um Abschlussposten handelt.

## <a name="view-job-ledger-entries" />Projektbuchungsposten anzeigen

Alle projektbezogenen Posten werden in Projektjournalen aufgezeichnet und fortlaufend nummeriert, beginnend mit 1. Aus den Projektjournalen können Sie eine Übersicht über alle Projektposten erhalten.    

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Projektjournale** ein und wählen Sie den zugehörigen Link.
2. Wählen Sie die entsprechende Projekte und wählen Sie dann die Aktion **Projektposten** aus.

Auf der Seite **Projektposten** können Sie die Posten überprüfen, die einem Projekt zugeordnet sind.  

## <a name="find-related-microsoft-training" />Siehe verwandte [Microsoft Schulungen](/training/paths/calculate-post-job-wip/)

## <a name="see-also" />Siehe auch

[Exemplarische Vorgehensweise: Berechnen des Umlaufbestandes](walkthrough-calculating-work-in-process-for-a-job.md)
[Verwalten von Projekten](projects-manage-projects.md)  
[Verwalten der Bestandsregulierung](finance-manage-inventory-costs.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
