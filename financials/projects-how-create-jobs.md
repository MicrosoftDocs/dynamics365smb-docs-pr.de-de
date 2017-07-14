---
title: 'Vorgehensweise: Erstellen von Jobs | Microsoft Docs'
description: 'So wird''s gemacht: Jobs erstellen'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, task
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: c9dcf1c235f3d510cde85502ac6ec40af748893b
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# So wird's gemacht: Projekt erstellen
<a id="how-to-create-jobs" class="xliff"></a>
Wenn Sie mit einem neuen Projekt beginnen, müssen Sie eine Projektkarte mit integrierten Projektaufgaben und Projektplanungszeilen erstellen, strukturiert in zwei Ebenen.  

Die erste Ebene besteht aus Projektaufgaben. Sie müssen mindestens eine Projektaufgabe pro Projekt erstellen, da sich alle Buchungen auf eine Projektaufgabe beziehen. Ist für das Projekt mindestens eine Projektaufgabe vorhanden, haben Sie die Möglichkeit zum Einrichten von Planungszeilen sowie zum Buchen des Verbrauchs für das Projekt.

Die zweite Ebene besteht aus Projektplanungszeilen, die zum Angeben des genauen Verbrauchs von Ressourcen, Artikeln sowie von verschiedenen Aufwandssachposten dienen.

Durch die Ebenenstruktur lässt sich das Projekt in kleinere Aufgaben unterteilen, was wiederum eine detaillierte Budgetierung, Angebotserstellung und Erfassung ermöglicht. Außerdem gibt sie Ihnen Einblick in den Fortschritt eines Projekt. So können Sie beispielsweise nachverfolgen, ob Sie die Meilensteine erfüllen, oder ob Sie mit den erwarteten Haushaltsmitteln zurechtkommen.

**Hinweis**: Die Aktion **Neues Projekt** im Rollencenter **Projektmanager** öffnet eine unterstütze Einrichtung, die Sie durch die Schritte zur Erstellung eines Projekts mit integrierten Aufgaben und Planungszeilen führt. Nachfolgend wird beschrieben, wie Sie die Schritte manuell ausführen.

**Hinweis**: Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird. Weitere Informationen finden Sie unter [Benutzeroberfläche [!INCLUDE[d365fin](includes/d365fin_md.md)] (ui-experiences.md) anpassen].

## So erstellen Sie eine Projektkarte
<a id="to-create-a-job-card" class="xliff"></a>
Sie erstellen eine Projektkarte und erstellen dann Projektaufgabenzeilen und Projektplanungszeilen dafür.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Jobs** ein und wählen Sie dann den entsprechenden Link aus.  
2. Wählen Sie die Aktion **Neu** aus, und füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Um das Projekt mit Informationen über andere Projekte anzugeben, wählen Sie die Aktion **Projekt kopieren** aus und ergänzen Sie die Felder wie nötig. Wählen Sie dann die Schaltfläche **OK** aus.

**HINWEIS**: Wenn Sie Arbeitszeittabellen bei Ihrem Projekt verwenden, müssen Sie auch ein verantwortliche Person angeben. Diese Person kann Arbeitszeittabellen für die Mitarbeiteraufgaben genehmigen, die dem Projekt zugeordnet sind. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Arbeitszeittabellen](projects-how-setup-time-sheets.md).

## Aufgaben für ein Projekt erstellen
<a id="to-create-tasks-for-a-job" class="xliff"></a>
Beim Einrichten eines neuen Projekts ist es wichtig, auch die verschiedenen Aufgaben für das Projekt anzugeben. Dazu fügen Sie neue Zeilen im Inforegister **Aufgaben** im Fenster **Projektkarten** hinzu, jeweils eine Aufgabe pro Zeile. Jedes Objekt muss mindestens eine Aufgabe haben.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Jobs** ein und wählen Sie dann den entsprechenden Link aus.
2. Öffnen Sie die Projektkarte für ein entsprechendes Projekt.
3. Füllen Sie im Inforegister **Aufgaben** die Felder nach Bedarf auf einer neuen Zeile aus.
4. Um Aufgaben einzurücken und eine Hierarchie zu erstellen, wählen Sie die Aktion **Aufgaben** und **Projektaufgaben einrücken**.
5. Wiederholen Sie die Schritte 3 und 4 für alle Aufgaben, die Sie für das Projekt benötigen.
6. Um die Projektaufgaben mit Informationen über andere Projektaufgaben anzugeben, wählen Sie die Aktion **Projektaufgaben kopieren von** aus und ergänzen Sie die Felder wie nötig. Wählen Sie dann die Schaltfläche **OK** aus.

## So erstellen Sie eine Projektplanzeile für ein Projekt
<a id="to-create-planning-lines-for-a-job" class="xliff"></a>
Sie können Ihre neuen Projektaufgaben für Projektplanzeilen neu definieren. Mithilfe einer Planzeile lassen sich alle Informationen erfassen, die Sie für ein Projekt nachverfolgen möchten. Planzeilen können verwendet werden, um Informationen wie erforderliche Ressourcen hinzuzufügen oder um Elemente zu erfassen, die zum Ausführen des Projekts erforderlich sind. So können Sie beispielsweise eine Aufgabe zum Einholen der Zustimmung des Debitors von einem Projekt erstellen. Diese Aufgabe können Sie mit Planzeilen für Elemente verknüpfen, beispielsweise Treffen mit dem Debitor und Zuweisen von Ressourcen.  

Eine Projektplanungszeile kann von einer der folgenden Arten sein.  

| Typ | Beschreibung |
| --- | --- |
| **Budget** |Dient zum Angeben der geschätzten Verbrauchswerte und der Kosten für das Projekt, üblicherweise in einem Aufwandsvertrag. Planzeilen dieser Art können nicht fakturiert werden. |
| **Fakturierbar** |Dient zum Angeben der geschätzten Fakturierung für den Debitor, üblicherweise in einem Festpreisprojekt. |
| **Sowohl budgetiert und verrechenbar** |Dient zum Angeben des geplanten Verbrauchs, der dem zu fakturierenden Wert entspricht. |

**Hinweis**. Beim Hinzufügen von Informationen in der Projektplanungszeilen werden die Kosteninformationen automatisch ergänzt. Wenn Sie also beispielsweise eine neue Zeile eingeben, basieren Kosten, Preis und Skonto für Ressourcen und Artikel zunächst auf den Informationen, die auf den Ressourcen- und Artikelkarten angegeben sind.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Jobs** ein und wählen Sie dann den entsprechenden Link aus.
2. Eine relevante Projektkarte öffnen.
3. Wählen Sie eine Projektaufgabe aus, deren Wert für das Feld **Projektaufgabenart** **Buchen** enthält und klicken Sie anschließend auf die Aktion **Projektplanzeilen**.  
4. Auf einer neuen Zeile im Fenster **Projektplanungszeilen** füllen Sie die Felder nach Bedarf aus.
5. Wiederholen Sie die Schritte 3 und 4 für alle Planungszeilen für diese Projektaufgabe.

## Siehe auch
<a id="see-also" class="xliff"></a>
[Projektmanagement](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)         
[Verkauf](sales-manage-sales.md)      
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

