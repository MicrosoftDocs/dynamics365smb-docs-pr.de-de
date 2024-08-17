---
title: Projektfortschritt und -leistung überwachen
description: 'Beschreibt, wie Sie eine WIP-Methode (Work in Process) erstellen und WIP berechnen können, um den finanziellen Wert laufender Projekte zu schätzen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 07/31/2024
ms.custom: bap-template
ms.search.keywords: 'project management, KPI, work in process, work in progress'
ms.search.form: '89, 92, 1010'
ms.service: dynamics-365-business-central
---

# Projektfortschritt und -leistung überwachen

Mit der Funktion Umlaufbestand (WIP) können Sie den finanziellen Wert laufender Projekte in der Finanzbuchhaltung schätzen.

Im Laufe eines Projekts werden Material sowie Ressourcen verbraucht und Aufwendungen erbracht, die auf das Projekt gebucht werden müssen. In vielen Fällen werden die Aufwendungen für ein Projekt vor der Fakturierung gebucht. Wenn ausschließlich Aufwendungen gebucht werden, ergibt sich eine inkorrekte Finanzauswertung. Um den tatsächlichen Wert des Projekts zu verfolgen, berechnen Sie den WIP und buchen Sie ihn im Hauptbuch. Erfahren Sie mehr unter [WIP-Methoden verstehen](projects-understanding-wip.md).

Die WIP-Berechnung kann auf der Grundlage der folgenden Optionen erfolgen:

* Einstandswert
* Verkaufswert
* Realisierbare Kosten
* Prozentsatz der Fertigung
* Abgeschl. Vertrag

<!--If you want to view the result using a different method, change the method and calculate WIP again. There's no limit to the number of times you calculate WIP; it doesn't get automatically posted to the general ledger. After you've calculated WIP using the method you prefer, you can post to the general ledger.-->
<!--Unhide the above paragraph?-->

## WIP-Methode für ein Projekt erstellen

Erstellen Sie eine Projekt-WIP-Methode, die den Bedarf Ihrer Organisation wiedergibt und legen Sie sie als Standard fest.  

> [!NOTE]
> Nachdem Sie Ihre neue Methode verwendet haben, um WIP-Posten zu erstellen, können Sie die Methode nicht löschen oder ändern.  

1. Wählen Sie das ![Glühbirne, die das „Sie wünschen ...“-Feature öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie  **Projekt-WIP-Methoden** ein und wählen Sie dann das zugehörige verknüpfen aus.  
2. Wählen Sie die Aktion **Neu** aus, und füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Schließen Sie die Seite.   
4. Um diese neue Methode zur Standardmethode zu machen, wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol, geben Sie  **Projekt-Setup** ein und wählen Sie dann das zugehörige verknüpfen.  
5. Wählen Sie im Feld **WIP-Standardmethode** die Methode aus der Liste aus.

## Eine WIP-Methode für ein Projekt definieren

Wenn Sie ein neues Projekt erstellen, müssen Sie auswählen, welche Projekt-WIP-Methode angewendet werden soll. In einigen Fällen ist die von Ihnen verwendete Projekt-WIP-Methode bereits als Standard festgelegt.

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Projekte** ein und wählen Sie den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu**. Erfahren Sie mehr unter [Projekte erstellen](projects-how-create-jobs.md).  
3. Wählen Sie auf der Seite  **Projekt Karte**  im Feld  **WIP-Methode**  auf der Registerkarte  **Buchen**  eine WIP-Methode aus der Liste aus. Wenn eine standardmäßige Methode festgelegt wurde, können Sie sofern erforderlich eine andere Option aktivieren.  

### Eine WIP-Methode für eine Projektaufgabe definieren

Sie können eine WIP-Methode für eine Projektaufgabe definieren, einige Projektaufgaben von der WIP-Berechnung ausschließen oder Aufgaben gruppieren, die zusammen berechnet werden sollen. 

Wenn Sie den WIP für jede Projektaufgabe einzeln berechnen möchten, bietet die WIP-Buchung definierte Dimensionen für die spezifischen Aufgaben.

**WIP-Summe** legt Projektaufgaben fest, die sie zusammen gruppieren, wenn Sie WIP und Erkennung berechnen. In jeder Gruppe von Aufgaben muss eine Aufgabe vorhanden sein, die zwei Bedingungen erfüllt:
<!--But doesn't the parenthetical below contradict this -* if there is no total, the application sets the total for you, meaning the condition does not HAVE to be satisfied, right? Or am I missing something?-->

* Hat ein **WIP-Gesamt** einstellen auf *Gesamt*. (Falls es keine Projektaufgaben mit der **WIP-Summe** gibt, die auf *Summe* gesetzt ist, wird *Summe* automatisch in der letzten Projektaufgabenzeile festgelegt, wenn die WIP das erste Mal berechnet wird.)

* Hat eine **Projektaufgabennr.**, die die letzte in der Gruppe oder im Bereich von Projektaufgaben ist.

Die drei Optionen werden in der folgenden Tabelle beschrieben:

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

Sie werden feststellen:

* *1000* bis *1299*: WIP wird für diese Gruppe von Projektaufgaben separat berechnet. Beachten Sie jedoch, dass zwei der Aufgaben, 1010 und 1110, von der WIP-Berechnung ausgeschlossen sind, da ihr Projektaufgabentyp **Buchung** ist.

* *1300* bis *1399*: WIP wird für diese Gruppe von Projektaufgaben separat berechnet.

## WIP berechnen

Bestimmen den WIP-Betrag, der im Rahmen der Berichterstellung am Periodenende auf Bilanzkonten gebucht werden muss. Dazu verwenden Sie das Stapelprojekt **WIP berechnen Projekt**.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie  **Projekt „WIP berechnen“** ein und wählen Sie dann das zugehörige verknüpfen aus.  
2. Wählen Sie die Aktion **WIP berechnen** aus.
3. Geben Sie auf der Seite **WIP berechnen Projekt** die notwendigen Felder ein.
4. Wählen Sie die Schaltfläche **OK** aus.  

> [!NOTE]  
> Das Stapelprojekt berechnet lediglich die WIP, und es erfolgt keine Buchung in die Finanzbuchhaltung. Zum Buchen müssen Sie das Stapelprojekt **WIP nach Sachposten Projekt** ausführen, nachdem Sie den WIP berechnet haben. Erfahren Sie mehr im folgenden Verfahren.

## WIP buchen

Wenn Sie den WIP berechnet haben, können Sie ihn zur Erstellung von Periodenendberichten auf Bilanzkonten buchen. Dazu verwenden Sie das Stapelprojekt **WIP nach Sachkonten Projekt**.

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus Symbol. Geben Sie **WIP nach Sachkonten Projekt** ein und wählen Sie dann den zugehörigen Link aus.  
2. Füllen Sie auf der Seite **WIP nach Sachkonten Projekt** aus und füllen Sie die Felder wie erforderlich aus.  
3. Wählen Sie die Schaltfläche **OK** aus.

## Berechnen und Buchen von Projekt-Abschlussposten

Nachdem alle Aktivitäten für ein Projekt – einschließlich Buchung des Verbrauchs und Fakturierung – abgeschlossen wurden, müssen Sie den Status des Projekts auf **Abgeschlossen** aktualisieren. Dann stornieren Sie alle WIPs, die in der Finanzbuchhaltung gebucht wurde.

1. Wählen Sie das Symbol ![Glühbirne, welche die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Projekte** ein und wählen Sie den zugehörigen Link aus.  
2. Wählen Sie ein offenes Projekt und dann die Aktion **Bearbeiten** aus.
3. Geben Sie auf der Registerkarte  **Buchung**  im Feld  **Status**  Auswählen **Abgeschlossen** ein.
4. Befolgen Sie die Hilfsschritte, um den WIP zu berechnen und zu buchen, oder befolgen Sie die Schritte 5 und 6, um dies manuell zu tun.  
5. Wählen Sie die Aktion **WIP berechnen** aus.
6. Geben Sie auf der Seite **WIP berechnen Projekt** die notwendigen Felder ein.  

     Bei den durch Ausführen des Stapelauftrags erstellten WIP-Projekteinträgen ist das Kontrollkästchen  **Projekt abgeschlossen**  aktiviert, um anzuzeigen, dass es sich um Abschlusseinträge handelt.  
7. Wählen Sie die Aktion **WIP nach Sachkonten** aus.
8. Füllen Sie auf der Seite **WIP nach Sachkonten Projekt** aus und füllen Sie die Felder wie erforderlich aus.  

     Bei den durch Ausführen des Batchprojekts erstellten WIP-Hauptbucheinträgen des Projekts ist das Kontrollkästchen  **Projekt abgeschlossen**  aktiviert, um anzuzeigen, dass es sich um Abschlusseinträge handelt.

## Projektposten anzeigen

Alle projektbezogenen Posten werden in Projektjournalen aufgezeichnet und fortlaufend nummeriert, beginnend mit 1. Aus den Projektjournalen können Sie eine Übersicht über alle Projektposten erhalten.    

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Projektjournale** ein und wählen Sie den zugehörigen Link aus.
2. Wählen Sie ein entsprechendes Journal und dann die Aktion **Projektposten** aus.

Auf der Seite **Projektposten** können Sie die Posten überprüfen, die einem Projekt zugeordnet sind.  

## Siehe auch

[exemplarische Vorgehensweise: Berechnen der laufenden Arbeit für ein Projekt](walkthrough-calculating-work-in-process-for-a-job.md)    
[Projekte verwalten](projects-manage-projects.md)    
[Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)    
[Finanzen](finance.md)    
[Einkauf](purchasing-manage-purchasing.md)    
[Verkauf](sales-manage-sales.md)    
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]
