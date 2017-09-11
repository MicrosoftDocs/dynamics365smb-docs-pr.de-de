---
title: "Einrichten und Verwalten eines Budget für ein Projekt| Microsoft Docs"
description: "Beschreibt, wie Sie Ressourcen planen und die Kosten für ein Projekt durch das Einrichten eines Budgets für jedes Projekt prognostizieren und steuern."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project budget, forecast
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 0e480c67ddb2acd5e98799c98cb1cd9d972889df
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-manage-job-budgets"></a><span data-ttu-id="edec2-103">Vorgehensweise: Verwalten von Projektbudgets</span><span class="sxs-lookup"><span data-stu-id="edec2-103">How to: Manage Job Budgets</span></span>
<span data-ttu-id="edec2-104">Jedes Projekt kann mit einem Budget versehen werden.</span><span class="sxs-lookup"><span data-stu-id="edec2-104">You can set up a budget for each job.</span></span> <span data-ttu-id="edec2-105">Das Budget dient zum Planen der Ressourcen, die einem Projekt zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="edec2-105">The budget is used to plan the resources that you allocate to a job.</span></span> <span data-ttu-id="edec2-106">Dabei kann es sich entweder um ein allgemeines Budget mit nur wenigen Posten oder um ein komplexeres Budget mit einer Vielzahl von Posten handeln, die in verschiedene Aktivitätsstufen unterteilt sind.</span><span class="sxs-lookup"><span data-stu-id="edec2-106">The budget can be either general with few entries or it can contain more entries that are divided into activity levels.</span></span> <span data-ttu-id="edec2-107">Mithilfe eines Budgets können die geplanten Beträge mit dem tatsächlichen Verbrauch verglichen werden, der im Buch.-Blatt des Projekts erfasst ist.</span><span class="sxs-lookup"><span data-stu-id="edec2-107">You can then compare the budgeted amounts with the actual usage as recorded in the job journal.</span></span> <span data-ttu-id="edec2-108">Durch Überwachung des tatsächlichen Verbrauchs im Vergleich zu einem Budget können sie ein laufendes Projekt kontrollieren und bei späteren Projekten zu einer höheren Qualität beitragen, da sich dadurch die Gefahr unterschätzter Kosten verringert.</span><span class="sxs-lookup"><span data-stu-id="edec2-108">By monitoring differences between actual usage and budgeted usage, you can control an ongoing project and improve the quality of future jobs by reducing the risk of underestimating costs.</span></span>

<span data-ttu-id="edec2-109">Nachfolgend wird beschrieben, wie Sie budgetierte Kosten während der Planung schätzen.</span><span class="sxs-lookup"><span data-stu-id="edec2-109">The following procedure describes how to estimate budgeted costs during planning.</span></span> <span data-ttu-id="edec2-110">Informationen zur Erfassung der budgetierten versus aktueller Preise und Kosten im Projekt finden Sie unter [Vorgehensweise: Erfassen des Verbrauchs für Projekte](projects-how-record-job-usage.md)</span><span class="sxs-lookup"><span data-stu-id="edec2-110">For information about recording budgeted versus actual job prices and costs, see [How to: Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>  

## <span data-ttu-id="edec2-111"><a name="JobBudgetCosts"></a> Die budgetierten Kosten für ein Projekt schätzen</span><span class="sxs-lookup"><span data-stu-id="edec2-111"><a name="JobBudgetCosts"></a> To estimate the budgeted costs for a job</span></span>
<span data-ttu-id="edec2-112">Wenn ein Debitor den Preis eines Projekts erfahren möchte, das auf Grundlage des Verbrauchs fakturiert wird, müssen Sie die budgetierten Einstandspreise für das Projekt ermitteln.</span><span class="sxs-lookup"><span data-stu-id="edec2-112">When a customer wants to know the price of a job that will be invoiced based on usage, you must have to determine the budgeted costs for the job.</span></span> <span data-ttu-id="edec2-113">Dazu verwenden Sie das Fenster **Projektaufgabenzeilen**.</span><span class="sxs-lookup"><span data-stu-id="edec2-113">You use the **Job Task Lines** window to do this.</span></span>

1. <span data-ttu-id="edec2-114">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Projekt** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="edec2-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="edec2-115">Ein relevantes Projekt öffnen.</span><span class="sxs-lookup"><span data-stu-id="edec2-115">Open a relevant job.</span></span>
3. <span data-ttu-id="edec2-116">Wählen Sie eine Aufgabenzeile unter Buchung aus und wählen Sie dann die Aktion **Projektplanungszeile**</span><span class="sxs-lookup"><span data-stu-id="edec2-116">Select a task line of type Posting, and then choose the **Job Planning Lines** action.</span></span>
4. <span data-ttu-id="edec2-117">Füllen Sie die Felder in einer neuen Zeile wie erforderlich aus.</span><span class="sxs-lookup"><span data-stu-id="edec2-117">On a new line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]   

<span data-ttu-id="edec2-118">Für das Feld **Linienart** geben Sie die folgenden Informationen in die Felder ein:</span><span class="sxs-lookup"><span data-stu-id="edec2-118">For the **Line Type** field, refer to the following information.</span></span>  

| <span data-ttu-id="edec2-119">Zeilenart</span><span class="sxs-lookup"><span data-stu-id="edec2-119">Line Type</span></span> | <span data-ttu-id="edec2-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="edec2-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="edec2-121">**Sowohl budgetiert und verrechenbar**</span><span class="sxs-lookup"><span data-stu-id="edec2-121">**Both Budget and Billable**</span></span> |<span data-ttu-id="edec2-122">Bei den in der Planungszeile eingegebenen Beträgen für Kosten und Preise handelt es sich um den budgetierten Einstandspreis für diese bestimmte Planungszeile.</span><span class="sxs-lookup"><span data-stu-id="edec2-122">The cost and price amounts entered on the planning line are the budgeted costs for the particular planning line.</span></span> <span data-ttu-id="edec2-123">Der Preisbetrag wird fakturiert.</span><span class="sxs-lookup"><span data-stu-id="edec2-123">The price amount will be invoiced.</span></span> |
| <span data-ttu-id="edec2-124">**Budget**</span><span class="sxs-lookup"><span data-stu-id="edec2-124">**Budget**</span></span> |<span data-ttu-id="edec2-125">Die Nutzung wird dem Kunden nicht in Rechnung gestellt.</span><span class="sxs-lookup"><span data-stu-id="edec2-125">The customer is not charged for usage.</span></span> <span data-ttu-id="edec2-126">Der Verbrauch kann nicht in eine Rechnung übertragen werden, wird jedoch weiterhin in der WIP-Berechnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="edec2-126">Usage is not transferred to an invoice, but will still be used in the calculation of WIP.</span></span> |
| <span data-ttu-id="edec2-127">**Fakturierbar**</span><span class="sxs-lookup"><span data-stu-id="edec2-127">**Billable**</span></span> |<span data-ttu-id="edec2-128">Die Nutzung wird dem Kunden in Rechnung gestellt.</span><span class="sxs-lookup"><span data-stu-id="edec2-128">The customer is charged for usage.</span></span> <span data-ttu-id="edec2-129">Der Verbrauch wird auf die Rechnung übertragen, und basiert auf der Menge, die in dem In Rechnung zu übertrag. Menge angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="edec2-129">Usage is transferred to the invoice, based on the quantity specified in the Qty.</span></span> <span data-ttu-id="edec2-130">Auf Rechnungsfeld übertragen</span><span class="sxs-lookup"><span data-stu-id="edec2-130">to Transfer to Invoice field.</span></span> |

> [!NOTE]  
>   <span data-ttu-id="edec2-131">Das Feld **Planungsdatum** für die Planungszeile enthält das Datum, wann der Verbrauch, der mit der Planungszeile verknüpft wird, erwartungsgemäß abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="edec2-131">The **Planning Date** field for the planning line contains the date when usage related to the planning line is expected to be completed.</span></span> <span data-ttu-id="edec2-132">Es ist ebenfalls das Datum, an dem die Planungszeile in eine Verkaufsrechnung übertragen und gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="edec2-132">It is also the date when the planning line may be transferred to a sales invoice and posted.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="edec2-133">Geben Sie die Menge für das Feld **Planungszeile** ein. Alle Angaben zu Einstands- und Verkaufsbeträgen werden nun berechnet und für diese Planungszeile eingetragen.</span><span class="sxs-lookup"><span data-stu-id="edec2-133">When you fill in the **Quantity** field, all total price and total cost information will be calculated and filled in for that planning line.</span></span> <span data-ttu-id="edec2-134">Sie können nun jederzeit bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="edec2-134">You can edit them at any time.</span></span>

<span data-ttu-id="edec2-135">Im Fenster **Projektkarte** können Sie nun eine Zusammenfassung mit budgetiertem Einstandsbetrag, budgetiertem Verkaufsbetrag, Einstandsbetrag (Vertrag) und Verkaufsbetrag für jede Aufgabe anzeigen.</span><span class="sxs-lookup"><span data-stu-id="edec2-135">In the **Job Card** window, you can now see a summary of the total budgeted costs, budgeted price, billable cost and billable price for each task.</span></span>

<span data-ttu-id="edec2-136">Informationen zur Erfassung der budgetierten versus aktueller Preise und Kosten im Projekt finden Sie unter [Vorgehensweise: Erfassen des Verbrauchs für Projekte](projects-how-record-job-usage.md)</span><span class="sxs-lookup"><span data-stu-id="edec2-136">For information about recording budgeted versus actual job prices and costs, see [How to: Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="edec2-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="edec2-137">See Also</span></span>
[<span data-ttu-id="edec2-138">Projektmanagement</span><span class="sxs-lookup"><span data-stu-id="edec2-138">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="edec2-139">Finanzen</span><span class="sxs-lookup"><span data-stu-id="edec2-139">Finance</span></span>](finance.md)  
<span data-ttu-id="edec2-140">[Einkauf](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="edec2-140">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="edec2-141">[Verkauf](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="edec2-141">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="edec2-142">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="edec2-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

