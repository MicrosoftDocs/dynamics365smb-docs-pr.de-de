---
title: Projektkarte für ein Projekt erstellen und Aufgaben angeben
description: Für ein neues Projekt erstellen Sie eine Projektkarte, die Projektaufgaben und enthält Planungszeilen erstellt, um Ihnen zu helfen, Status und Budgets zu verwalten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.workload: na
ms.search.keywords: project management, task
ms.search.form: 88, 1001, 1002, 1003, 1004, 1005, 1006, 1007
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 88da1794619da0fce6001d70482a021d8efbe8cf
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/14/2022
ms.locfileid: "7973310"
---
# <a name="create-jobs"></a>Projekt erstellen
Wenn Sie mit einem neuen Projekt beginnen, müssen Sie eine Projektkarte mit integrierten Projektaufgaben und Projektplanungszeilen erstellen, strukturiert in zwei Ebenen.  

Die erste Ebene besteht aus Projektaufgaben. Sie müssen mindestens eine Projektaufgabe pro Projekt erstellen, da sich alle Buchungen auf eine Projektaufgabe beziehen. Ist für das Projekt mindestens eine Projektaufgabe vorhanden, haben Sie die Möglichkeit zum Einrichten von Planungszeilen sowie zum Buchen des Verbrauchs für das Projekt.

Die zweite Ebene besteht aus Projektplanungszeilen, die zum Angeben des genauen Verbrauchs von Ressourcen, Artikeln sowie von verschiedenen Aufwandssachposten dienen.

Durch die Ebenenstruktur lässt sich das Projekt in kleinere Aufgaben unterteilen, was wiederum eine detaillierte Budgetierung, Angebotserstellung und Erfassung ermöglicht. Außerdem gibt sie Ihnen Einblick in den Fortschritt eines Projekt. So können Sie beispielsweise nachverfolgen, ob Sie die Meilensteine erfüllen, oder ob Sie mit den erwarteten Haushaltsmitteln zurechtkommen.

> [!TIP]
> Wählen Sie die Aktion **Neues Projekt** im Rollencenter **Projektmanager** aus, um einen Leitfaden für das unterstütze Setup zu starten, der Sie durch die Schritte zur Erstellung eines Projekts mit integrierten Aufgaben und Planungszeilen führt. Nachfolgend wird beschrieben, wie Sie die Schritte manuell ausführen. Ein Beispiel dazu, wie Sie ein Projekt manuell erstellen, finden im [Video: So erstellen Sie ein Projekt in Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw).

## <a name="to-create-a-job-card"></a>So erstellen Sie eine Projektkarte
Sie erstellen eine Projektkarte und erstellen dann Projektaufgabenzeilen und Projektplanungszeilen dafür.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Aufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus, und füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Um das Projekt mit Informationen über andere Projekte anzugeben, wählen Sie die Aktion **Projekt kopieren** aus und ergänzen Sie die Felder wie nötig. Wählen Sie dann die Schaltfläche **OK** aus.

> [!NOTE]  
>   Wenn Sie Arbeitszeittabellen bei Ihrem Projekt verwenden, müssen Sie auch eine verantwortliche Person angeben. Diese Person kann Arbeitszeittabellen für die Mitarbeiteraufgaben genehmigen, die dem Projekt zugeordnet sind. Weitere Informationen finden Sie unter [Einrichten von Arbeitszeittabellen](projects-how-setup-time-sheets.md).

## <a name="to-create-tasks-for-a-job"></a>Aufgaben für ein Projekt erstellen
Beim Einrichten eines neuen Projekts ist es wichtig, auch die verschiedenen Aufgaben für das Projekt anzugeben. Dazu fügen Sie neue Zeilen im Inforegister **Aufgaben** auf der Seite **Projektkarten** hinzu, jeweils eine Aufgabe pro Zeile. Jedes Objekt muss mindestens eine Aufgabe haben.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Aufträge** ein, und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die Projektkarte für ein entsprechendes Projekt.
3. Füllen Sie im Inforegister **Aufgaben** die Felder nach Bedarf auf einer neuen Zeile aus.
4. Um Aufgaben einzurücken und eine Hierarchie zu erstellen, wählen Sie die Aktion **Aufgaben** und **Projektaufgaben einrücken**.
5. Wiederholen Sie die Schritte 3 und 4 für alle Aufgaben, die Sie für das Projekt benötigen.
6. Um die Projektaufgaben mit Informationen über andere Projektaufgaben anzugeben, wählen Sie die Aktion **Projektaufgaben kopieren von** aus und ergänzen Sie die Felder wie nötig. Wählen Sie dann die Schaltfläche **OK** aus.

## <a name="to-create-planning-lines-for-a-job"></a>So erstellen Sie eine Projektplanzeile für ein Projekt
Sie können Ihre neuen Projektaufgaben für Projektplanzeilen neu definieren. Mithilfe einer Planzeile lassen sich alle Informationen erfassen, die Sie für ein Projekt nachverfolgen möchten. Planzeilen können verwendet werden, um Informationen wie erforderliche Ressourcen hinzuzufügen oder um Elemente zu erfassen, die zum Ausführen des Projekts erforderlich sind. So können Sie beispielsweise eine Aufgabe zum Einholen der Zustimmung des Debitors von einem Projekt erstellen. Diese Aufgabe können Sie mit Planzeilen für Elemente verknüpfen, beispielsweise Treffen mit dem Debitor und Zuweisen von Ressourcen.  

Eine Projektplanungszeile kann von einer der folgenden Arten sein.  

| Typ | Beschreibung |
| --- | --- |
| **Budget** |Dient zum Angeben der geschätzten Verbrauchswerte und der Kosten für das Projekt, üblicherweise in einem Aufwandsvertrag. Planzeilen dieser Art können nicht fakturiert werden. |
| **Fakturierbar** |Dient zum Angeben der geschätzten Fakturierung für den Debitor, üblicherweise in einem Festpreisprojekt. |
| **Sowohl budgetiert und verrechenbar** |Dient zum Angeben des geplanten Verbrauchs, der dem zu fakturierenden Wert entspricht. |

**Hinweis**. Beim Hinzufügen von Informationen in der Projektplanungszeilen werden die Kosteninformationen automatisch ergänzt. Wenn Sie also beispielsweise eine neue Zeile eingeben, basieren Kosten, Preis und Skonto für Ressourcen und Artikel zunächst auf den Informationen, die auf den Ressourcen- und Artikelkarten angegeben sind.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Aufträge** ein, und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie eine entsprechende Jobkarte.
3. Wählen Sie eine Projektaufgabe aus, deren Wert für das Feld **Projektaufgabenart** **Buchen** enthält und klicken Sie anschließend auf die Aktion **Projektplanzeilen**.  
4. Auf einer neuen Zeile auf der Seite **Projektplanungszeilen** füllen Sie die Felder nach Bedarf aus.
5. Wiederholen Sie die Schritte 3 und 4 für alle Planungszeilen für diese Projektaufgabe.

## <a name="see-also"></a>Siehe auch

[Projektmanagement](projects-manage-projects.md)  
[Video: Wie man einen Auftrag in Dynamics 365 Business Central erstellt](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]