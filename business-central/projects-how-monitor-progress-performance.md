---
title: Überwachen des Status und der Leistung
description: Beschreibt, wie Sie eine Umlaufbestand-Methode (WIP) erstellen und WIP berechnen können, um den finanziellen Wert von Projekten zu beurteilen, während sie ausgeführt werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, KPI, work in process, work in progress
ms.search.form: 89, 92, 1010
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7c816ea6d4fa8f1653000f94e15b74f9b78db8c6
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/14/2022
ms.locfileid: "7971810"
---
# <a name="monitor-job-progress-and-performance"></a>Überwachen des Status und der Leistung
Im Laufe eines Projekts werden Material sowie Ressourcen und andere Aufwendungen verbraucht und müssen auf das Projekt gebucht werden. Umlaufbestand (WIP) ist eine Funktion, mit der Sie den finanziellen Wert in der Finanzbuchhaltung schätzen können, solange die Projekte noch nicht abgeschlossen sind. In vielen Fällen werden die Aufwendungen für ein Projekt vor der Fakturierung des Projekts gebucht. Wurden ausschließlich Aufwendungen gebucht, ergibt sich eine inkorrekte Finanzauswertung. Weitere Informationen finden Sie unter [WIP-Methode verstehen](projects-understanding-wip.md).

Zum Überwachen des Werts in der Finanzbuchhaltung können Sie die WIP berechnen und den Wert in der Finanzbuchhaltung buchen.

Die WIP-Berechnung kann auf der Grundlage der folgenden Optionen erfolgen:

* Einstandswert
* Verkaufswert
* Realisierbare Kosten
* Prozentsatz der Fertigung
* Bei Abschluss

Soll das Ergebnis unter Verwendung einer anderen Methode angezeigt werden, können Sie die Methode ändern und die WIP-Berechnung erneut ausführen. Dieser Schritt lässt sich beliebig oft wiederholen. Die WIP wird lediglich berechnet; sie wird nicht in der Finanzbuchhaltung gebucht. Nach Ausführung der WIP-Berechnung kann das Ergebnis in die Finanzbuchhaltung gebucht werden.

## <a name="to-create-a-job-wip-method"></a>WIP-Methode für Projekt erstellen
Sie können eine WIP-Methode für das Projekt erstellen, die den Bedarf Ihrer Organisation wiedergibt. Nachdem Sie diese erstellt haben, können Sie diese als die standardmäßige Projekt-WIP-Berechnungsmethode festlegen, die in Ihrer Organisation verwendet wird.  

> [!NOTE]
> Nachdem Sie Ihre neue Methode verwendet haben, um WIP-Posten zu erstellen, können Sie die Methode nicht löschen oder ändern.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Job WIP-Methoden für Projekte** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus, und füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Schließen Sie die Seite.   
4. Um diese neue Methode zur Standardmethode zu machen, wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Projekt Einrichtung** ein und wählen Sie den zugehörigen Link.  
5. Wählen Sie im Feld **WIP-Standardmethode** die Methode aus der Liste aus.

## <a name="to-define-a-wip-method-for-a-job"></a>Eine WIP-Methode für ein Projekt definieren
Wenn Sie ein neues Projekt erstellen, müssen Sie auswählen, welche WIP-Methode angewendet werden soll. In einigen Fällen kann die WIP-Methode, die Sie verwenden können, bereits als Standard eingerichtet sein.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Aufträge** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Neu**. Weitere Informationen finden Sie unter  [Projekte erstellen](projects-how-create-jobs.md).  
3. Wählen Sie auf der Seite **Projektkarte** im Feld **WIP-Methode** eine WIP-Methode aus der Liste aus. Wenn eine standardmäßige Methode festgelegt wurde, können Sie sofern erforderlich eine andere Option aktivieren.  

## <a name="to-calculate-wip"></a>So berechnen Sie die WIP
Bestimmen den WIP-Betrag, der im Rahmen der Berichterstellung am Periodenende auf Bilanzkonten gebucht werden muss Dazu verwenden Sie die Stapelverarbeitung **WIP berechnen Projekt**.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Job WIP berechnen Projekt** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **WIP berechnen** aus.
3. Geben Sie auf der Seite **WIP für Projekt berechnen** die notwendigen Felder ein.
4. Wählen Sie die Schaltfläche **OK** aus.  

> [!NOTE]  
>   Die Stapelverarbeitung berechnet nur den WIP. Er wird nicht auf das Sachkonto gebucht. Dazu müssen Sie die Stapelverarbeitung **WIP nach Sachposten Projekt** ausführen, nachdem Sie den WIP berechnet haben. Weitere Informationen finden Sie in der folgenden Prozedur.

## <a name="to-post-wip"></a>Zu buchender WIP
Wenn Sie den WIP berechnet haben, können Sie ihn zur Erstellung von Periodenendberichten auf Bilanzkonten buchen. Dazu verwenden Sie die Stapelverarbeitung **WIP nach Sachposten Projekt**.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Job WIP auf Sachkonten buchen Projekt** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie auf der Seite **WIP nach Sachkonten Projekt buchen** aus und füllen Sie die Felder wie erforderlich aus.  
3. Wählen Sie die Schaltfläche **OK**.

## <a name="to-calculate-and-post-job-completion-entries"></a>Berechnen und Buchen von Projekt-Abschlussposten
Nachdem alle Aktivitäten für ein Projekt – einschließlich Buchung des Verbrauchs und Fakturierung – abgeschlossen wurden, muss das Projekt aktualisiert werden, damit es den **Status** **Abgeschlossen** erhält. Dann stornieren Sie alle WIPs, die in der Finanzbuchhaltung gebucht wurde.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Aufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie ein offenes Projekte und wählen Sie dann die Aktion **Bearbeiten** aus.
3. Wählen Sie im Feld **Status** **Abgeschlossen**.
4. Folgen Sie den Hilfeschritten, um WIP zu berechnen und zu buchen. Alternativ folgen Sie den Schritten 5 und 6, um dies manuell zu tun.  
5. Wählen Sie die Aktion **WIP berechnen** aus.
6. Geben Sie auf der Seite **WIP für Projekt berechnen** die notwendigen Felder ein.  

     Die WIP-Projektposten, die beim Ausführen der Stapelverarbeitung erstellt wurden, weisen nun ein Häkchen im Feld **Auftrag abgeschlossen** auf, um anzugeben, dass es sich hierbei um Abschlussposten handelt.  
7. Wählen Sie die Aktion **WIP nach Sachkonten Projekt** aus.
8. Füllen Sie auf der Seite **WIP nach Sachkonten Projekt buchen** aus und füllen Sie die Felder wie erforderlich aus.  

     Die WIP-Hauptbuchungsposten, die beim Ausführen der Stapelverarbeitung erstellt wurden, weisen nun ein Häkchen im Feld **Auftrag abgeschlossen** auf, um anzugeben, dass es sich hierbei um Abschlussposten handelt.

## <a name="to-view-job-ledger-entries"></a>Projektbuchungsposten anzeigen
Alle projektbezogenen Posten werden in Projektjournalen aufgezeichnet und fortlaufend nummeriert, beginnend mit 1. Aus den Projektjournalen können Sie eine Übersicht über alle Projektposten erhalten.    

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Projektjournale** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die entsprechende Projekte und wählen Sie dann die Aktion **Projektposten** aus.

Auf der Seite **Projektposten** können Sie die Posten überprüfen, die einem Projekt zugeordnet sind.  

## <a name="see-also"></a>Siehe auch
[Verwalten von Projekten](projects-manage-projects.md)
[Verwalten der Lagerkosten](finance-manage-inventory-costs.md)   
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)         
[Verkauf](sales-manage-sales.md)      
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
