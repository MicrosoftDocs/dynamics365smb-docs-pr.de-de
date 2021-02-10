---
title: Erstellen von Kostenbudgets| Microsoft Docs
description: Dieses Thema enthält eine Übersicht, wo Kostenbudgets erstellt und analysiert werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2a8b8e88e296f36b8f4eb9bb41b05d5fc529b23b
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750955"
---
# <a name="creating-cost-budgets"></a><span data-ttu-id="eb679-103">Erstellen von Kostenbudgets</span><span class="sxs-lookup"><span data-stu-id="eb679-103">Creating Cost Budgets</span></span>
<span data-ttu-id="eb679-104">Die Budgetierung in der Kostenrechnung entspricht der Budgetierung im Sachkonto.</span><span class="sxs-lookup"><span data-stu-id="eb679-104">Budgeting in cost accounting resembles budgeting in the general ledger.</span></span> <span data-ttu-id="eb679-105">Ein Kostenbudget wird ausgehend von Kostenarten erstellt, wie ein Budget für das Sachkonto basierend auf Sachkonten erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="eb679-105">A cost budget is created based on cost types just as a budget for the general ledger is created based on general ledger accounts.</span></span>  

<span data-ttu-id="eb679-106">Ein Kostenbudget wird für eine bestimmten Zeitraum erstellt, zum Beispiel für ein Geschäftsjahr.</span><span class="sxs-lookup"><span data-stu-id="eb679-106">A cost budget is created for a certain period of time, for example, a fiscal year.</span></span> <span data-ttu-id="eb679-107">Sie können beliebig viele Kostenbudgets erstellen.</span><span class="sxs-lookup"><span data-stu-id="eb679-107">You can create as many cost budgets as needed.</span></span> <span data-ttu-id="eb679-108">Sie können ein neues Kostenbudget manuell erstellen, indem Sie ein Kostenbudget importieren oder indem Sie ein vorhandenes Kostenbudget als Budgetbasis kopieren.</span><span class="sxs-lookup"><span data-stu-id="eb679-108">You can create a new cost budget manually, or by importing a cost budget, or by copying an existing cost budget as the budget base.</span></span> <span data-ttu-id="eb679-109">Weitere Informationen finden Sie unter [Sachkonto-Budgets erstellen](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="eb679-109">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

<span data-ttu-id="eb679-110">Sie verwenden die folgenden Seiten, um Kostenbudgets zu erstellen und zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="eb679-110">You use the following pages to create and analyze cost budgets.</span></span> <span data-ttu-id="eb679-111">Wählen Sie das Symbol ![Glühlampe, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, um eine Seite zu finden, und lesen Sie dann die jeweilige QuickInfo.</span><span class="sxs-lookup"><span data-stu-id="eb679-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon to find a page, and then read the tooltip for each.</span></span>

|<span data-ttu-id="eb679-112">Aktion</span><span class="sxs-lookup"><span data-stu-id="eb679-112">To</span></span>|<span data-ttu-id="eb679-113">Siehe</span><span class="sxs-lookup"><span data-stu-id="eb679-113">See</span></span>|  
|--------|---------|  
|<span data-ttu-id="eb679-114">Übertragen Sie Budgets aus dem Sachkonto.</span><span class="sxs-lookup"><span data-stu-id="eb679-114">Transfer budgets from the general ledger.</span></span>|<span data-ttu-id="eb679-115">Stapelverarbeitung **Finanzbudget in Kostenrechnung kopieren**</span><span class="sxs-lookup"><span data-stu-id="eb679-115">**Copy G-L Budget to Cost Acctg.** batch job</span></span>|  
|<span data-ttu-id="eb679-116">Kostenbudgets kopieren.</span><span class="sxs-lookup"><span data-stu-id="eb679-116">Copy cost budgets.</span></span>|<span data-ttu-id="eb679-117">Stapelverarbeitung **Kostenbudget kopieren**</span><span class="sxs-lookup"><span data-stu-id="eb679-117">**Copy Cost Budget** batch job</span></span>|  
|<span data-ttu-id="eb679-118">Budgets zuteilen.</span><span class="sxs-lookup"><span data-stu-id="eb679-118">Allocate budgets.</span></span>|<span data-ttu-id="eb679-119">**Kostenzuteilung**</span><span class="sxs-lookup"><span data-stu-id="eb679-119">**Cost Allocation** page</span></span>|  
|<span data-ttu-id="eb679-120">Sehen Sie sich die Kostenbudgeterfassungen und Kostenbudgetposten an.</span><span class="sxs-lookup"><span data-stu-id="eb679-120">See cost budget registers and cost budget entries.</span></span>|<span data-ttu-id="eb679-121">**<Kostenbudgeterfassungen**</span><span class="sxs-lookup"><span data-stu-id="eb679-121">**Cost Budget Registers** page</span></span>|  
|<span data-ttu-id="eb679-122">Drucken Sie Kostenbudgetvergleiche unter Verwendung der verschiedenen Berichte.</span><span class="sxs-lookup"><span data-stu-id="eb679-122">Print cost budget comparisons using various reports.</span></span>|<span data-ttu-id="eb679-123">Bericht **Kostenrechnungsbilanz/Budget**</span><span class="sxs-lookup"><span data-stu-id="eb679-123">**Cost Acctg. Balance-Budget** report</span></span><br /><br /> <span data-ttu-id="eb679-124">Bericht **Kostenrechnungsauszug/Budget**</span><span class="sxs-lookup"><span data-stu-id="eb679-124">**Cost Acctg. Statement-Budget** report</span></span><br /><br /> <span data-ttu-id="eb679-125">Bericht **Kostenbudget nach Kostenstelle**</span><span class="sxs-lookup"><span data-stu-id="eb679-125">**Cost Budget by Cost Center** report</span></span><br /><br /> <span data-ttu-id="eb679-126">Bericht **Kostenbudget nach Kostenträger**</span><span class="sxs-lookup"><span data-stu-id="eb679-126">**Cost Budget by Cost Object** report</span></span>|  

## <a name="see-also"></a><span data-ttu-id="eb679-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb679-127">See Also</span></span>  
[<span data-ttu-id="eb679-128">Kostenrechnung</span><span class="sxs-lookup"><span data-stu-id="eb679-128">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
[<span data-ttu-id="eb679-129">Sachkontenbudgets erstellen</span><span class="sxs-lookup"><span data-stu-id="eb679-129">Create G/L Budgets</span></span>](finance-how-create-budgets.md)  
<span data-ttu-id="eb679-130">[Terminologie der Kostenrechnung](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="eb679-130">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="eb679-131">Definieren und Zuweisen von Kosten</span><span class="sxs-lookup"><span data-stu-id="eb679-131">Defining and Allocating Costs</span></span>](finance-define-and-allocate-costs.md)  
<span data-ttu-id="eb679-132">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="eb679-132">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
