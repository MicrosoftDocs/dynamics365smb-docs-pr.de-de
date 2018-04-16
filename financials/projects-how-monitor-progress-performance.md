---
title: "Eine WIP-Methode definieren und den Projekt-Status überwachen | Microsoft Docs"
descrition: Describes how you can create a work in process (WIP) method and calculate WIP to estimate the financial value of jobs while they are ongoing.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, KPI, work in process, work in progress
ms.date: 07/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 22dc57e01941927dfc2077eb1e48645cfc7b56de
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

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

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen") und geben **Projekt-WIP-Methoden** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Neu** aus, und füllen Sie die Felder nach Bedarf aus. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Schließen Sie das Fenster.   
4. Um diese neue Methode als Standard zu definieren, wählen Sie in der rechten oberen Ecke ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen")aus und geben Sie **Projekteinrichtung** ein. Wählen Sie dann den zugehörigen Link aus.  
5. Wählen Sie im Feld **WIP-Standardmethode** die Methode aus der Liste aus.

## <a name="to-define-a-wip-method-for-a-job"></a>Eine WIP-Methode für ein Projekt definieren
Wenn Sie ein neues Projekt erstellen, müssen Sie auswählen, welche WIP-Methode angewendet werden soll. In einigen Fällen kann die WIP-Methode, die Sie verwenden können, bereits als Standard eingerichtet sein.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Projekt** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus. Weitere Informationen finden Sie unter  [Projekte erstellen](projects-how-create-jobs.md).  
3. Wählen Sie im Fenster **Projektkarte** im Feld **WIP-Methode** eine WIP-Methode aus der Liste aus. Wenn eine standardmäßige Methode festgelegt wurde, können Sie sofern erforderlich eine andere Option aktivieren.  

## <a name="to-calculate-wip"></a>So berechnen Sie die WIP
Bestimmen den WIP-Betrag, der im Rahmen der Berichterstellung am Periodenende auf Bilanzkonten gebucht werden muss Dazu verwenden Sie die Stapelverarbeitung **WIP berechnen Projekt**.  

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen") und geben **Projekt-WIP berechnen** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **WIP berechnen** aus.
3. Geben Sie im Fenster **WIP für Projekt berechnen** die notwendigen Felder ein.
4. Wählen Sie die Schaltfläche **OK** aus.  

> [!NOTE]  
>   Die Stapelverarbeitung berechnet nur den WIP. Er wird nicht auf das Sachkonto gebucht. Dazu müssen Sie die Stapelverarbeitung **WIP nach Sachposten Projekt** ausführen, nachdem Sie den WIP berechnet haben. Weitere Informationen finden Sie in der folgenden Prozedur.

## <a name="to-post-wip"></a>Zu buchender WIP
Wenn Sie den WIP berechnet haben, können Sie ihn zur Erstellung von Periodenendberichten auf Bilanzkonten buchen. Dazu verwenden Sie die Stapelverarbeitung **WIP nach Sachposten Projekt**.

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen") und geben **WIP auf G/L buchen** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Füllen Sie im Fenster **WIP nach Sachkonten Projekt buchen** aus und füllen Sie die Felder wie erforderlich aus.  
3. Wählen Sie die Schaltfläche **OK** aus.

## <a name="to-view-job-usage-estimates-and-post-updates"></a>So zeigen Sie Projektverbrauchschätzungen und Buchungsaktualisierungen an.
Der Projektverbrauch kann bis zum Projektabschluss in einem einzigen Schritt angezeigt werden. Verwenden Sie hierzu die Stapelverarbeitung **Restverbrauch für Projekt berechnen** für alle Aufgaben bis zum Projektende (einschließlich).  

Auf diese Weise können Sie die ursprüngliche Planung mit den tatsächlichen Ergebnissen vergleichen und ggf. Änderungen vornehmen oder neue Posten hinzufügen. Beispiel: Sie haben für ein Projekt eine Dauer von zehn Stunden geplant, aktueller Stand sind jedoch 15 Stunden. Sie können die fünf zusätzlichen Stunden entweder der bestehenden Buch.-Blattzeile hinzufügen oder eine neue Buch.-Blattzeile erstellen, um die fünf Stunden als Überstunden (anderer Arbeitstyp) zu melden. Die angemessenen Kosten und der Preis werden berechnet und dann können Sie sie in das Protokoll buchen.  

> [!NOTE]  
>   Artikeleinträge erstellen Artikelposten und reduzieren die Lagerbestandmenge. Durch die Stapelverarbeitung **Lagerregulierung buchen** werden die Kosten aus dem Lagerbestand in die Finanzbuchhaltung gebucht. Aus Posten für Ressourcen werden Ressourcenposten erstellt.  

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen") und geben **Projektbuch** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie ein Buch.-Blatt des entsprechenden Projekts, und wählen Sie dann die Aktion **Verbleibender Verbrauch berechnen** aus.  
3. Geben Sie im Fenster **Restverbrauch für Projekt berechnen** die Belegnummer und das Buchungsdatum ein, das in das Buch.-Blatt eingefügt werden soll und wählen Sie dann die Schaltfläche **OK**.  
4. Aktualisieren Sie das Buch.-Blatt mit sämtlichen Änderungen, die möglicherweise erforderlich sind.  
5. Wählen Sie die Aktion **Buchen** aus.

## <a name="to-view-job-ledger-entries"></a>Projektbuchungsposten anzeigen
Alle projektbezogenen Posten werden in Projektjournalen aufgezeichnet und fortlaufend nummeriert, beginnend mit 1. Aus den Projektjournalen können Sie eine Übersicht über alle Projektposten erhalten.    

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen") und geben **Projektregister** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die entsprechende Projekte und wählen Sie dann die Aktion **Projektposten** aus.

Im Fenster **Projektposten** können Sie die Posten überprüfen, die einem Projekt zugeordnet sind.  

## <a name="see-also"></a>Siehe auch
[Verwalten von Projekten](projects-manage-projects.md)
[Verwalten der Lagerkosten](finance-manage-inventory-costs.md)   
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)         
[Verkauf](sales-manage-sales.md)      
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

