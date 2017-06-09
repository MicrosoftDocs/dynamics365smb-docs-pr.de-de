---
title: 'Vorgehensweise: Verwalten von Projektbudgets | Microsoft Docs'
description: Beschreibt, wie Projekte budgetiert werden.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project budget, forecast
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 9a351b581e0312d21b04db43a85243b8a5afb0e3
ms.contentlocale: de-de
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-manage-job-budgets"></a>Vorgehensweise: Verwalten von Projektbudgets
Jedes Projekt kann mit einem Budget versehen werden. Das Budget dient zum Planen der Ressourcen, die einem Projekt zugeordnet werden. Dabei kann es sich entweder um ein allgemeines Budget mit nur wenigen Posten oder um ein komplexeres Budget mit einer Vielzahl von Posten handeln, die in verschiedene Aktivitätsstufen unterteilt sind. Mithilfe eines Budgets können die geplanten Beträge mit dem tatsächlichen Verbrauch verglichen werden, der im Buch.-Blatt des Projekts erfasst ist. Durch Überwachung des tatsächlichen Verbrauchs im Vergleich zu einem Budget können sie ein laufendes Projekt kontrollieren und bei späteren Projekten zu einer höheren Qualität beitragen, da sich dadurch die Gefahr unterschätzter Kosten verringert.

Nachfolgend wird beschrieben, wie Sie budgetierte Kosten während der Planung schätzen. Informationen zur Erfassung der budgetierten versus aktueller Preise und Kosten im Projekt finden Sie unter [Vorgehensweise: Erfassen des Verbrauchs für Projekte](projects-how-record-job-usage.md)  

## <a name="JobBudgetCosts"></a> Die budgetierten Kosten für ein Projekt schätzen
Wenn ein Debitor den Preis eines Projekts erfahren möchte, das auf Grundlage des Verbrauchs fakturiert wird, müssen Sie die budgetierten Einstandspreise für das Projekt ermitteln. Dazu verwenden Sie das Fenster **Projektaufgabenzeilen**.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus **![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "")Symbol nach Seite oder Bericht suchen. Geben Sie **Jobs** ein und wählen Sie dann den entsprechenden Link aus.  
2. Ein relevantes Projekt öffnen.
3. Wählen Sie eine Aufgabenzeile unter Buchung aus und wählen Sie dann die Aktion **Projektplanungszeile**
4. Füllen Sie die Felder in einer neuen Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]   

Für das Feld **Linienart** geben Sie die folgenden Informationen in die Felder ein:  

| Zeilenart | Beschreibung |
| --- | --- |
| **Sowohl budgetiert und verrechenbar** |Bei den in der Planungszeile eingegebenen Beträgen für Kosten und Preise handelt es sich um den budgetierten Einstandspreis für diese bestimmte Planungszeile. Der Preisbetrag wird fakturiert. |
| **Budget** |Die Nutzung wird dem Kunden nicht in Rechnung gestellt. Der Verbrauch kann nicht in eine Rechnung übertragen werden, wird jedoch weiterhin in der WIP-Berechnung verwendet. |
| **Fakturierbar** |Die Nutzung wird dem Kunden in Rechnung gestellt. Der Verbrauch wird auf die Rechnung übertragen, und basiert auf der Menge, die in dem In Rechnung zu übertrag. Menge angegeben ist. Auf Rechnungsfeld übertragen |

**Hinweis** Das Feld **Planungsdatum** für die Planungszeile enthält das Datum, wann der Verbrauch, der mit der Planungszeile verknüpft wird, erwartungsgemäß abgeschlossen. Es ist ebenfalls das Datum, an dem die Planungszeile in eine Verkaufsrechnung übertragen und gebucht wird.  

**Hinweis**: Geben Sie die Menge für das Feld **Planungszeile** ein. Alle Angaben zu Einstands- und Verkaufsbeträgen werden nun berechnet und für diese Planungszeile eingetragen. Sie können nun jederzeit bearbeitet werden.

Im Fenster **Projektkarte** können Sie nun eine Zusammenfassung mit budgetiertem Einstandsbetrag, budgetiertem Verkaufsbetrag, Einstandsbetrag (Vertrag) und Verkaufsbetrag für jede Aufgabe anzeigen.

Informationen zur Erfassung der budgetierten versus aktueller Preise und Kosten im Projekt finden Sie unter [Vorgehensweise: Erfassen des Verbrauchs für Projekte](projects-how-record-job-usage.md)

## <a name="see-also"></a>Siehe auch
[Projektmanagement](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)         
[Verkauf](sales-manage-sales.md)      
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md]  

