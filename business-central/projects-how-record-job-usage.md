---
title: Datensatz-Verbrauch oder -Verwendung von Job-Ressourcen und Elementen
description: Beschreibt, wie der Verbrauch oder die Verwendung von Artikeln oder Ressourcen erfasst wird, um das Projektmanagement zu vereinfachen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, consumption
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 65975621fff862b64333c87e70f34b75f8e2cbdb
ms.sourcegitcommit: 93c8681054b059cec38cb29b86de20be37980676
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938096"
---
# <a name="record-consumption-or-usage-for-jobs"></a>Datensatz-Verbrauch oder -Verwendung für Jobs aufzeichnen

Auf der Seite **Projektplanzeilen** können Sie Verbrauch für verschiedene Teile des Projekts überprüfen und erfassen; dieser wird automatisch aktualisiert, wenn Sie Informationen zu Projekten und Projektbuchungsblättern oder Projektrechnungen ändern und übertragen. Dies setzt voraus, dass Sie einen Job so festgelegt haben, dass die **Verbrauchsverknüpfung anwenden** eingeschaltet ist. Weitere Informationen finden Sie unter [Einrichten von Stellen](projects-how-setup-jobs.md).  

Zum Beispiel können Sie für Planungszeilen der Art **Plan** die Menge einer Ressource eingeben und festlegen, welche Menge in das Projektbuchungsblatt umgelagert wird. Wenn die Art der Planungszeile **Fakturierbar** ist, können Sie die Menge einer Ressource eingeben und festlegen, welche Menge in das Projektbuchungsblatt umgelagert wird. Weitere Informationen zur Rechnungsstellung an den Debitor finden Sie unter [Jobs fakturieren](projects-how-invoice-jobs.md). Durch den Vergleich der ursprünglichen Menge, der verbleibenden Menge oder der gebuchten Menge können Sie die Verbrauchsinformationen schnell überprüfen. Informationen zur Einschätzung der geplante Werte bei der Planung, siehe [Verwalten von Projektbudgets](projects-how-manage-budgets.md)  

Die folgenden Verfahren beschreiben, wie Sie tatsächliche (budgetierte) Mengen und Kosten mit dem Job-Journal erfassen. Alternativ können Sie auch Kaufbelege verwenden, um den Kauf für einen Job zu erfassen. Weitere Informationen finden Sie unter [Verwalten von Auftragsvorräten](projects-how-manage-project-supplies.md).

## <a name="to-record-usage-for-a-job-planning-line-of-type-budget"></a>Den Verbrauch in einer Projektplanungszeile der Art "Plan"erfassen

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Projekte** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die entsprechende Projekte und wählen Sie dann die Aktion **Projektplanzeilen** aus.
3. Wählen Sie eine Projektplanungszeile der Art **Plan** aus oder geben Sie **Plan und Fakturierbar** ein, für die Sie den Verbrauch buchen möchten.  

    > [!NOTE]
    > Sie können den Datensatz auch für eine Auftragsplanungszeile vom Typ **Abrechnungsfähig** verwenden. Normalerweise verwenden Sie diese Zeile, um Rechnungen zu erstellen, aber Sie können sie auch in eine Erfassung übertragen. Weitere Informationen finden Sie unter [Rechnungsaufträge](projects-how-invoice-jobs.md) <!--However, when you do that, a job planning line of type **Budget** is created to match the billable line. For more information, see [Manage Job Budgets](projects-how-manage-budgets.md).-->

4. Geben Sie im Feld **In das Journal zu übertragende Menge** die Anzahl ein, die Sie auf die Rechnung transferieren wollen. Der Standardwert ist der Wert, den Sie im Feld **Menge** angegeben haben.

    Das Feld **Restmenge** zeigt die Menge an, die verbleibt, um das Projekt abzuschließen und in das Buch.-Blatt zu übertragen.  
5. Wählen Sie die Aktion **Buch.-Blattzeilen erstellen** aus.

    > [!TIP]
    > Wenn Sie weitere Projektplanzeilen für dieses Projekt hinzufügen möchten, warten Sie mit diesem Schritt, bis Sie alle Projektplanzeilen hinzugefügt haben.
6. Auf der Seite **Projekt auf Projektplanung übertragen** geben Sie die Felder wie nötig ein, und wählen Sie dann die Schaltfläche **OK**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Wählen Sie die Aktion **Buch.-Blatt öffnen** aus.  
8. Auf der Seite **Projekt Buch,-Blatt** wählen Sie die entsprechende Zeile und wählen die Aktion **Buchen** aus.
9. Auf der Seite **Projektplanungszeilen** überprüfen Sie den erfassten Verbrauch, indem Sie die Felder **Menge**, **Restmenge** und **Auf Buch.-Blatt zu übertragende Menge** kontrollieren.  
10. Um zusätzlichen Verbrauch zu erfassen, wiederholen Sie die Schritte 3 bis 8.  

## <a name="to-create-job-journal-lines-manually"></a>Projekt-Buchungsblattzeilen manuell erstellen

1. Wählen Sie das Symbol ![Glühbirne , das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") aus, geben Sie **Projekt Buch.-Blätter** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie im Feld **Stapelverarbeitungsname** einen entsprechenden Projekt-Buchungsblattnamen aus.  
3. Geben Sie in einer neuen Zeile die Belegnummer, Projektnummer, Projektaufgabennummer und die Art und Menge des verbrauchten Typs ein.  
4. Wenn die Projekt-Buch.-Blattzeilen vollständig sind, wählen Sie die Aktion **Buchen** aus.  

## <a name="to-view-job-usage-estimates-and-post-updates"></a>So zeigen Sie Projektverbrauchschätzungen und Buchungsaktualisierungen an.

Der Projektverbrauch kann bis zum Projektabschluss in einem einzigen Schritt angezeigt werden. Verwenden Sie hierzu die Stapelverarbeitung **Restverbrauch für Projekt berechnen** für alle Aufgaben bis zum Projektende (einschließlich).  

Auf diese Weise können Sie die ursprüngliche Planung mit den tatsächlichen Ergebnissen vergleichen und ggf. Änderungen vornehmen oder neue Posten hinzufügen. Beispiel: Sie haben für ein Projekt eine Dauer von zehn Stunden geplant, aktueller Stand sind jedoch 15 Stunden. Sie können die fünf zusätzlichen Stunden entweder der bestehenden Buch.-Blattzeile hinzufügen oder eine neue Buch.-Blattzeile erstellen, um die fünf Stunden als Überstunden (anderer Arbeitstyp) zu melden. Die angemessenen Kosten und der Preis werden berechnet und dann können Sie sie in das Protokoll buchen.  

> [!NOTE]  
>   Artikeleinträge erstellen Artikelposten und reduzieren die Lagerbestandmenge. Durch die Stapelverarbeitung **Lagerregulierung buchen** werden die Kosten aus dem Lagerbestand in die Finanzbuchhaltung gebucht. Aus Posten für Ressourcen werden Ressourcenposten erstellt.  

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion Tell Me](media/ui-search/search_small.png "Was möchten Sie tun?") öffnet, geben Sie **Job Journale** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie ein Buch.-Blatt des entsprechenden Projekts, und wählen Sie dann die Aktion **Verbleibender Verbrauch berechnen** aus.  
3. Geben Sie auf der Seite **Restverbrauch für Projekt berechnen** die Belegnummer und das Buchungsdatum ein, das in das Buch.-Blatt eingefügt werden soll und wählen Sie dann die Schaltfläche **OK**.  
4. Aktualisieren Sie das Buch.-Blatt mit sämtlichen Änderungen, die möglicherweise erforderlich sind.  
5. Wählen Sie die Aktion **Buchen** aus.



## <a name="to-review-planning-lines-for-a-job-ledger-entry"></a>Um Planungszeilen für einen Projektposten zu überprüfen

Nachdem Sie die Projekt-Planungszeilen gebucht haben, können Sie die gebuchten Projekt-Buchungszeilen sehen, die dem Projekt-Buchungsblatt zugeordnet sind.

> [!NOTE]  
> Dies setzt voraus, dass das Kontrollkästchen **Verwendungslink anwenden** für den Job aktiviert wurde. Weitere Informationen finden Sie unter [Jobs festlegen](projects-how-setup-jobs.md).  

1. Wählen Sie das Symbol ![Glühbirne , das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Projekt Buch.-Blätter** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie ein Buch.-Blatt des entsprechenden Projekts aus, und wählen Sie dann die Aktion **Projektposten** aus.  
3. Auf der Seite **Projektposteneinträge** wählen Sie die Aktion **Anzeigen verknüpfter Projektplanungszeilen** aus.

## <a name="see-also"></a>Siehe auch
[Projektmanagement](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)         
[Verkauf](sales-manage-sales.md)      
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
