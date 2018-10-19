---
title: "Einrichten und Verwalten eines Budget für ein Projekt| Microsoft Docs"
description: "Beschreibt, wie Sie Ressourcen planen und die Kosten für ein Projekt durch das Einrichten eines Budgets für jedes Projekt prognostizieren und steuern."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project budget, forecast
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 995d181496dc1827f21c0b3edd9e52dd6c15c297
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="manage-job-budgets"></a><span data-ttu-id="5f126-103">Verwalten von Projektbudgets</span><span class="sxs-lookup"><span data-stu-id="5f126-103">Manage Job Budgets</span></span>
<span data-ttu-id="5f126-104">Jedes Projekt kann mit einem Budget versehen werden.</span><span class="sxs-lookup"><span data-stu-id="5f126-104">You can set up a budget for each job.</span></span> <span data-ttu-id="5f126-105">Das Budget dient zum Planen der Ressourcen, die einem Projekt zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="5f126-105">The budget is used to plan the resources that you allocate to a job.</span></span> <span data-ttu-id="5f126-106">Dabei kann es sich entweder um ein allgemeines Budget mit nur wenigen Posten oder um ein komplexeres Budget mit einer Vielzahl von Posten handeln, die in verschiedene Aktivitätsstufen unterteilt sind.</span><span class="sxs-lookup"><span data-stu-id="5f126-106">The budget can be either general with few entries or it can contain more entries that are divided into activity levels.</span></span> <span data-ttu-id="5f126-107">Mithilfe eines Budgets können die geplanten Beträge mit dem tatsächlichen Verbrauch verglichen werden, der im Buch.-Blatt des Projekts erfasst ist.</span><span class="sxs-lookup"><span data-stu-id="5f126-107">You can then compare the budgeted amounts with the actual usage as recorded in the job journal.</span></span> <span data-ttu-id="5f126-108">Durch Überwachung des tatsächlichen Verbrauchs im Vergleich zu einem Budget können sie ein laufendes Projekt kontrollieren und bei späteren Projekten zu einer höheren Qualität beitragen, da sich dadurch die Gefahr unterschätzter Kosten verringert.</span><span class="sxs-lookup"><span data-stu-id="5f126-108">By monitoring differences between actual usage and budgeted usage, you can control an ongoing project and improve the quality of future jobs by reducing the risk of underestimating costs.</span></span>

<span data-ttu-id="5f126-109">Nachfolgend wird beschrieben, wie Sie budgetierte Kosten während der Planung schätzen.</span><span class="sxs-lookup"><span data-stu-id="5f126-109">The following procedure describes how to estimate budgeted costs during planning.</span></span> <span data-ttu-id="5f126-110">Informationen zur Erfassung der budgetierten versus aktueller Preise und Kosten im Projekt finden Sie unter [Erfassen des Verbrauchs für Projekte](projects-how-record-job-usage.md)</span><span class="sxs-lookup"><span data-stu-id="5f126-110">For information about recording budgeted versus actual job prices and costs, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>  

## <a name="JobBudgetCosts"></a> <span data-ttu-id="5f126-111">Die budgetierten Kosten für ein Projekt schätzen</span><span class="sxs-lookup"><span data-stu-id="5f126-111">To estimate the budgeted costs for a job</span></span>
<span data-ttu-id="5f126-112">Wenn ein Debitor den Preis eines Projekts erfahren möchte, das auf Grundlage des Verbrauchs fakturiert wird, müssen Sie die budgetierten Einstandspreise für das Projekt ermitteln.</span><span class="sxs-lookup"><span data-stu-id="5f126-112">When a customer wants to know the price of a job that will be invoiced based on usage, you must have to determine the budgeted costs for the job.</span></span> <span data-ttu-id="5f126-113">Dazu verwenden Sie das Fenster **Projektaufgabenzeilen**.</span><span class="sxs-lookup"><span data-stu-id="5f126-113">You use the **Job Task Lines** window to do this.</span></span>

1. <span data-ttu-id="5f126-114">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Aufträge** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="5f126-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="5f126-115">Ein relevantes Projekt öffnen.</span><span class="sxs-lookup"><span data-stu-id="5f126-115">Open a relevant job.</span></span>
3. <span data-ttu-id="5f126-116">Wählen Sie eine Aufgabenzeile unter Buchung aus und wählen Sie dann die Aktion **Projektplanungszeile**</span><span class="sxs-lookup"><span data-stu-id="5f126-116">Select a task line of type Posting, and then choose the **Job Planning Lines** action.</span></span>
4. <span data-ttu-id="5f126-117">Füllen Sie die Felder in einer neuen Zeile wie erforderlich aus.</span><span class="sxs-lookup"><span data-stu-id="5f126-117">On a new line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]   

<span data-ttu-id="5f126-118">Für das Feld **Linienart** geben Sie die folgenden Informationen in die Felder ein:</span><span class="sxs-lookup"><span data-stu-id="5f126-118">For the **Line Type** field, refer to the following information.</span></span>  

| <span data-ttu-id="5f126-119">Zeilenart</span><span class="sxs-lookup"><span data-stu-id="5f126-119">Line Type</span></span> | <span data-ttu-id="5f126-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f126-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="5f126-121">**Sowohl budgetiert und verrechenbar**</span><span class="sxs-lookup"><span data-stu-id="5f126-121">**Both Budget and Billable**</span></span> |<span data-ttu-id="5f126-122">Bei den in der Planungszeile eingegebenen Beträgen für Kosten und Preise handelt es sich um den budgetierten Einstandspreis für diese bestimmte Planungszeile.</span><span class="sxs-lookup"><span data-stu-id="5f126-122">The cost and price amounts entered on the planning line are the budgeted costs for the particular planning line.</span></span> <span data-ttu-id="5f126-123">Der Preisbetrag wird fakturiert.</span><span class="sxs-lookup"><span data-stu-id="5f126-123">The price amount will be invoiced.</span></span> |
| <span data-ttu-id="5f126-124">**Budget**</span><span class="sxs-lookup"><span data-stu-id="5f126-124">**Budget**</span></span> |<span data-ttu-id="5f126-125">Die Nutzung wird dem Debitoren nicht in Rechnung gestellt.</span><span class="sxs-lookup"><span data-stu-id="5f126-125">The customer is not charged for usage.</span></span> <span data-ttu-id="5f126-126">Der Verbrauch kann nicht in eine Rechnung übertragen werden, wird jedoch weiterhin in der WIP-Berechnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="5f126-126">Usage is not transferred to an invoice, but will still be used in the calculation of WIP.</span></span> |
| <span data-ttu-id="5f126-127">**Fakturierbar**</span><span class="sxs-lookup"><span data-stu-id="5f126-127">**Billable**</span></span> |<span data-ttu-id="5f126-128">Die Nutzung wird dem Debitoren in Rechnung gestellt.</span><span class="sxs-lookup"><span data-stu-id="5f126-128">The customer is charged for usage.</span></span> <span data-ttu-id="5f126-129">Der Verbrauch wird auf die Rechnung übertragen, und basiert auf der Menge, die in dem In Rechnung zu übertrag. Menge angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="5f126-129">Usage is transferred to the invoice, based on the quantity specified in the Qty. to Transfer to Invoice field.</span></span> |

> [!NOTE]  
>   <span data-ttu-id="5f126-130">Das Feld **Planungsdatum** für die Planungszeile enthält das Datum, wann der Verbrauch, der mit der Planungszeile verknüpft wird, erwartungsgemäß abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="5f126-130">The **Planning Date** field for the planning line contains the date when usage related to the planning line is expected to be completed.</span></span> <span data-ttu-id="5f126-131">Es ist ebenfalls das Datum, an dem die Planungszeile in eine Verkaufsrechnung übertragen und gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="5f126-131">It is also the date when the planning line may be transferred to a sales invoice and posted.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="5f126-132">Geben Sie die Menge für das Feld **Planungszeile** ein. Alle Angaben zu Einstands- und Verkaufsbeträgen werden nun berechnet und für diese Planungszeile eingetragen.</span><span class="sxs-lookup"><span data-stu-id="5f126-132">When you fill in the **Quantity** field, all total price and total cost information will be calculated and filled in for that planning line.</span></span> <span data-ttu-id="5f126-133">Sie können nun jederzeit bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="5f126-133">You can edit them at any time.</span></span>

<span data-ttu-id="5f126-134">Im Fenster **Projektkarte** können Sie nun eine Zusammenfassung mit budgetiertem Einstandsbetrag, budgetiertem Verkaufsbetrag, Einstandsbetrag (Vertrag) und Verkaufsbetrag für jede Aufgabe anzeigen.</span><span class="sxs-lookup"><span data-stu-id="5f126-134">In the **Job Card** window, you can now see a summary of the total budgeted costs, budgeted price, billable cost and billable price for each task.</span></span>

<span data-ttu-id="5f126-135">Informationen zur Erfassung der budgetierten versus aktueller Preise und Kosten im Projekt finden Sie unter [Erfassen des Verbrauchs für Projekte](projects-how-record-job-usage.md)</span><span class="sxs-lookup"><span data-stu-id="5f126-135">For information about recording budgeted versus actual job prices and costs, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5f126-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f126-136">See Also</span></span>
[<span data-ttu-id="5f126-137">Projektmanagement</span><span class="sxs-lookup"><span data-stu-id="5f126-137">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="5f126-138">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5f126-138">Finance</span></span>](finance.md)  
<span data-ttu-id="5f126-139">[Einkauf](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="5f126-139">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="5f126-140">[Verkauf](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="5f126-140">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="5f126-141">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5f126-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

