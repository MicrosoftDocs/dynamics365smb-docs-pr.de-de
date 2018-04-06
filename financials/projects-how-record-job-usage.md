---
title: Verrechenbarer und geplanter Verbrauch von Projekt-Ressourcen| Microsoft Docs
description: Beschreibt, wie der Verbrauch oder die Verwendung von Artikeln oder Ressourcen erfasst wird, um das Projektmanagement zu vereinfachen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, consumption
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b0bd4f9a4c0963520631e1571fd182adce85fdd9
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="record-usage-for-jobs"></a>Verbrauch bei Projekten aufzeichnen
Im Fenster **Projektplanzeilen** können Sie Verbrauch für verschiedene Teile des Projekts überprüfen und erfassen; dieser wird automatisch aktualisiert, wenn Sie Informationen zu Projekten und Projektbuchungsblättern oder Projektrechnungen ändern und übertragen. Dazu ist es erforderlich, dass Sie ein Projekt eingerichtet haben, sodass der **Link Verbrauch anwenden** eingeschaltet ist. Weitere Informationen finden Sie unter [Einrichten von Stellen](projects-how-setup-jobs.md).  

Zum Beispiel können Sie für Planungszeilen der Art **Plan** die Menge einer Ressource eingeben und festlegen, welche Menge in das Projektbuchungsblatt umgelagert wird. Wenn die Art der Planungszeile **Fakturierbar** ist, können Sie die Menge einer Ressource eingeben und festlegen, welche Menge in das Projektbuchungsblatt umgelagert wird. Indem Sie die Menge vergleichen, die in das Buchungsblatt oder in die Rechnung mit der Restmenge übernommen wurde, können Sie Verbrauchsdaten schnell überprüfen.

Die folgenden Verfahren beschreiben, wie die tatsächlichen (verrechenbaren) oder geplanten Projektverkaufspreise und Kosten gespeichert werden. Informationen zur Einschätzung der geplante Werte bei der Planung, siehe [Verwalten von Projektbudgets](projects-how-manage-budgets.md)

## <a name="to-record-usage-for-a-job-planning-line-of-type-budget"></a>Den Verbrauch in einer Projektplanungszeile der Art "Plan"erfassen
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Projekt** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die entsprechende Projekte und wählen Sie dann die Aktion **Projektplanzeilen** aus.
3. Wählen Sie eine Projektplanungszeile der Art **Plan** aus oder geben Sie **Plan und Fakturierbar** ein, für die Sie den Verbrauch buchen möchten.
4. Geben Sie im Feld **In das Journal zu übertragende Menge** die Anzahl ein, die Sie auf die Rechnung transferieren wollen. Der Standardwert ist der Wert, den Sie im Feld **Menge** angegeben haben.

    Das Feld **Restmenge** zeigt die Menge an, die verbleibt, um das Projekt abzuschließen und in das Buch.-Blatt zu übertragen.  
5. Wählen Sie die Aktion **Buch.-Blattzeilen erstellen** aus.
6. Im Fenster **Projekt auf Projektplanung übertragen** geben Sie die Felder wie nötig ein, und wählen Sie dann die Schaltfläche **OK**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Wählen Sie die Aktion **Buch.-Blatt öffnen** aus.  
8. Im **Projekt Buch,-Blatt** wählen Sie die entsprechende Zeile und wählen die Aktion **Buchen** aus.
9. Im Fenster **Projektplanungszeilen** überprüfen Sie den erfassten Verbrauch, indem Sie die Felder **Menge**, **Restmenge** und **Auf Buch.-Blatt zu übertragende Menge** kontrollieren.  
10. Um zusätzlichen Verbrauch zu erfassen, wiederholen Sie die Schritte 3 bis 8.  

## <a name="to-record-usage-for-a-job-planning-line-of-type-billable"></a>Den Verbrauch in einer Projektplanungszeile der Art "Fakturierbar" erfassen
In der nächsten Aufgabe erfassen Sie ebenfalls den Verbrauch, jedoch für eine Projektplanungszeile der Art **Fakturierbar**. In diesem Fall fakturieren Sie normalerweise Ihren Verbrauch, Sie können ihn aber auch in ein Buchungsblatt übertragen. Wenn Sie dies tun, wird eine Projektplanungszeile der Art **Plan** erstellt, die der Zeile "Fakturierbar" entspricht. Weitere Informationen finden Sie unter [Budgets verwalten](projects-how-manage-budgets.md).

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Projekt** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die entsprechende Projekte und wählen Sie dann die Aktion **Projektplanzeilen** aus.  
3. Wählen Sie eine Projektplanungszeile der Art **Fakturierbar** aus, für die Sie den Verbrauch aufzeichnen möchten.
4. Geben Sie im Feld **In das Journal zu übertragende Rechnung** die Anzahl ein, die Sie transferieren wollen. Der Standardwert ist der Wert, den Sie im Feld **Menge** angegeben haben.

    Das Feld **Zu fakturierende Menge** zeigt die Menge an, die verbleibt, um das Projekt abzuschließen und zu fakturieren.  
5. Wählen Sie die Aktion **Verkaufsrechnung erstellen**.
6. Im Fenster **Projekt auf Verkaufsrechnung übertragen** geben Sie die Felder wie nötig ein, und wählen Sie dann die Schaltfläche **OK**.
7. Im Fenster **Projekt Buch,-Blatt** wählen Sie die entsprechende Zeile und wählen die Aktion **Buchen** aus.
8. Überprüfen Sie den erfassten Verbrauch, indem Sie die Felder **Menge**, **Zu fakturierende Menge**, **Menge auf Rechnung übertragen** und wenn die Verkaufsrechnungen gebucht werden **Fakturierte Menge** kontrollieren.
9. Um zusätzlichen Verbrauch zu erfassen, wiederholen Sie die Schritte 3 bis 8.  
10. Um eine zugehörige gebuchte Verkaufsrechnung zu überprüfen, wählen Sie die Aktion **Verkaufsrechnungen/Gutschriften** aus.  
11. Im Fenster **Projektrechnungen** wählen Sie die entsprechende Rechnung aus, und wählen Sie die Aktion **Verkaufsrechnung/Gutschrift öffnen** aus.         

## <a name="to-create-job-journal-lines-from-job-planning-lines"></a>Projekt-Buchungsblattzeilen aus Projektplanungszeilen erstellen
Wenn Sie bereit sind, Finanzdaten für Projekte zu buchen, müssen Sie Projekt Buch.-Blattzeilen erstellen, die Sie buchen können.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Projekt** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie ein entsprechendes offenes Projekt und wählen Sie dann die Aktion **Projektplanzeilen** aus.  
3. Wählen Sie im Fenster **Projektplanungszeilen** eine relevante Projektplanungszeile aus und geben Sie im Feld **In Buch.-Blatt zu übertragende Menge** die Menge ein, die Sie in ein Projekt-Buchungsblatt übertragen möchten.  
4. Wählen Sie die Aktion **Buch.-Blattzeilen erstellen** aus.
5. Auf einer neuen Zeile im Fenster **Projektplanungszeilen übertragen** füllen Sie die Felder nach Bedarf aus.  
6. Wählen Sie die Schaltfläche **OK** aus. Projekt-Buch.-Blattzeilen werden erstellt.
7. Um die Übertragung zu prüfen, öffnen Sie das Buch.-Blatt des entsprechenden Projekts und überprüfen Sie die Posten in der Stapelverarbeitung des entsprechenden Projekts.  
8. Wenn die Projekt-Buch.-Blattzeilen vollständig sind, wählen Sie die Aktion **Buchen** aus.  

## <a name="to-create-job-journal-lines-manually"></a>Projekt-Buchungsblattzeilen manuell erstellen
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen") und geben **Projektbuch** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie im Feld **Stapelverarbeitungsname** einen entsprechenden Projekt-Buchungsblattnamen aus.  
3. Geben Sie in einer neuen Zeile die Belegnummer, Projektnummer, Projektaufgabennummer und die Art und Menge des verbrauchten Typs ein.  
4. Wenn die Projekt-Buch.-Blattzeilen vollständig sind, wählen Sie die Aktion **Buchen** aus.  

## <a name="to-review-planning-lines-for-a-job-ledger-entry"></a>Um Planungszeilen für einen Projektposten zu überprüfen
Nachdem Sie die Projekt-Planungszeilen gebucht haben, können Sie die gebuchten Projekt-Buchungszeilen sehen, die dem Projekt-Buchungsblatt zugeordnet sind.

> [!NOTE]  
>   Dazu ist es erforderlich, dass das Kontrollkästchen **Verbrauchslink anwenden** für das Projekt ausgewählt wurde, oder dass es die Standardeinstellung für alle Projekte in Ihrer Organisation ist. Weitere Informationen finden Sie unter [Einrichten von Stellen](projects-how-setup-jobs.md).  

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen") und geben **Projektbuch** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie ein Buch.-Blatt des entsprechenden Projekts aus, und wählen Sie dann die Aktion **Projektposten** aus.  
3. Im Fenster **Projektposteneinträge** wählen Sie die Aktion **Anzeigen verknüpfter Projektplanungszeilen** aus.

## <a name="see-also"></a>Siehe auch
[Projektmanagement](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)         
[Verkauf](sales-manage-sales.md)      
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

