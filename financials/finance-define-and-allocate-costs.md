---
title: Dfinieren und Zuweisen von Kosten | Microsoft Docs
description: "Kostenzuteilungen verschieben Kosten und Einnahmen zwischen Kostenarten, Kostenstellen und Kostenträgern. Sie können so viele Zuteilungen wie notwendig definieren."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 04e5a95b7a926528cc26c254390d08e3bce6ad8a
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="defining-and-allocating-costs"></a><span data-ttu-id="c42a3-104">Definieren und Zuweisen von Kosten</span><span class="sxs-lookup"><span data-stu-id="c42a3-104">Defining and Allocating Costs</span></span>
<span data-ttu-id="c42a3-105">Kostenzuteilungen verschieben Kosten und Einnahmen zwischen Kostenarten, Kostenstellen und Kostenträgern.</span><span class="sxs-lookup"><span data-stu-id="c42a3-105">Cost allocations move costs and revenues between cost types, cost centers, and cost objects.</span></span> <span data-ttu-id="c42a3-106">Sie können so viele Zuteilungen wie notwendig definieren.</span><span class="sxs-lookup"><span data-stu-id="c42a3-106">You can define as many allocations as you need.</span></span> <span data-ttu-id="c42a3-107">Jede Zuteilung besteht aus:</span><span class="sxs-lookup"><span data-stu-id="c42a3-107">Each allocation consists of:</span></span>  

-   <span data-ttu-id="c42a3-108">Eine Verteilungsquelle.</span><span class="sxs-lookup"><span data-stu-id="c42a3-108">An allocation source.</span></span>  
-   <span data-ttu-id="c42a3-109">Mindestens einem Zuteilungsziel.</span><span class="sxs-lookup"><span data-stu-id="c42a3-109">One or more allocation targets.</span></span>  

<span data-ttu-id="c42a3-110">Die Zuteilungsquelle gibt an, welche Kosten zugeordnet werden müssen, und die Zuteilungsziele bestimmen, wo die Kosten zugeordnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c42a3-110">The allocation source establishes which costs must be allocated, and the allocation targets determine where the costs must be allocated.</span></span> <span data-ttu-id="c42a3-111">Beispielsweise können die Kosten für die Kostenart Strom und Heizung eine Verteilungsquelle sein.</span><span class="sxs-lookup"><span data-stu-id="c42a3-111">For example, an allocation source can be the costs for the Electricity and Heating cost type.</span></span> <span data-ttu-id="c42a3-112">Sie ordnen alle Strom- und Heizkosten drei Kostenstellen zu: Werkstatt, Produktion und Verkauf.</span><span class="sxs-lookup"><span data-stu-id="c42a3-112">You allocate all electricity and heating costs to three cost centers: Workshop, Production, and Sales.</span></span> <span data-ttu-id="c42a3-113">Diese Kostenstellen sind Ihre Zuteilungsziele.</span><span class="sxs-lookup"><span data-stu-id="c42a3-113">These cost centers are your allocation targets.</span></span>  

<span data-ttu-id="c42a3-114">Für jede Zuteilungsquelle legen Sie eine Zuteilungsebene, eine Gültigkeitsdauer und eine Variante als Gruppen-ID fest.</span><span class="sxs-lookup"><span data-stu-id="c42a3-114">For each allocation source, you define an allocation level, a validity period, and a variant as grouping identifier.</span></span> <span data-ttu-id="c42a3-115">Sie können einen Batchauftrag verwenden, um Filter festzulegen und Zuteilungsdefinitionen auszuwählen und dann automatisch Kostenzuteilungen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c42a3-115">You can use a batch job to set filters to select allocation definitions and then run cost allocations automatically.</span></span>  

<span data-ttu-id="c42a3-116">Für jedes Zuteilungsziel definieren Sie eine Zuteilungsgrundlage.</span><span class="sxs-lookup"><span data-stu-id="c42a3-116">For each allocation target, you define an allocation base.</span></span> <span data-ttu-id="c42a3-117">Die Zuteilungsgrundlage kann entweder statisch oder dynamisch sein.</span><span class="sxs-lookup"><span data-stu-id="c42a3-117">The allocation base can be either static or dynamic.</span></span>  

-   <span data-ttu-id="c42a3-118">Die statische Zuteilungsgrundlagen basieren auf einem definierten Wert, zum Beispiel Quadratmeter oder ein eingerichtetes Verteilungsverhältnis, wie 5:2:4.</span><span class="sxs-lookup"><span data-stu-id="c42a3-118">Static allocation bases are based on a definite value, such as square footage or an established allocation ratio, such as 5:2:4.</span></span>  
-   <span data-ttu-id="c42a3-119">Die dynamische Zuteilung basiert auf veränderbaren Werten, wie z. B. die Anzahl der Mitarbeiter in einer Kostenstelle oder die Verkaufseinnahmen eines Kostenträgers in einem bestimmten Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="c42a3-119">Dynamic allocation bases depend on changeable values, such as the number of employees in a cost center or sales revenue of a cost object throughout a certain time period.</span></span>  

<span data-ttu-id="c42a3-120">Die folgende Tabelle enthält eine Abfolge von Aufgaben sowie Links zu den entsprechenden Themen, in denen diese Aufgaben erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="c42a3-120">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="c42a3-121">An</span><span class="sxs-lookup"><span data-stu-id="c42a3-121">To</span></span>|<span data-ttu-id="c42a3-122">Siehe</span><span class="sxs-lookup"><span data-stu-id="c42a3-122">See</span></span>|  
|--------|---------|  
|<span data-ttu-id="c42a3-123">Richten Sie die Zuteilungsquelle und ihre Ziele ein.</span><span class="sxs-lookup"><span data-stu-id="c42a3-123">Set up allocation source and its targets.</span></span>|[<span data-ttu-id="c42a3-124">Richten Sie die Zuteilungsquelle und Ziele ein</span><span class="sxs-lookup"><span data-stu-id="c42a3-124">Set Up Allocation Source and Targets</span></span>](finance-how-to-set-up-allocation-source-and-targets.md)|  
|<span data-ttu-id="c42a3-125">Richten Sie verschiedene Filter für dynamische Zuteilungsgrundlagen ein.</span><span class="sxs-lookup"><span data-stu-id="c42a3-125">Set up various filters for dynamic allocation bases.</span></span>|[<span data-ttu-id="c42a3-126">Setzen von Filtern für dynamische Zuteilungsgrundlagen</span><span class="sxs-lookup"><span data-stu-id="c42a3-126">Setting Filters for Dynamic Allocation Bases</span></span>](finance-setting-filters-for-dynamic-allocation-bases.md)|  
|<span data-ttu-id="c42a3-127">Sehen Sie sich ein Beispiel für das Definieren einer statischen Verteilung an.</span><span class="sxs-lookup"><span data-stu-id="c42a3-127">See an example of how to define a static allocation.</span></span>|[<span data-ttu-id="c42a3-128">Szenario-Beispiel: Definieren von statischen Verteilungen basierend auf dem Verteilungsverhältnis</span><span class="sxs-lookup"><span data-stu-id="c42a3-128">Scenario Example: Defining Static Allocations Based on Allocation Ratio</span></span>](finance-scenario-example-defining-static-allocations-based-on-allocation-ratio.md)|  
|<span data-ttu-id="c42a3-129">Sehen Sie sich ein Beispiel für das Definieren einer dynamischen Zuteilung an.</span><span class="sxs-lookup"><span data-stu-id="c42a3-129">See an example of how to define a dynamic allocation.</span></span>|[<span data-ttu-id="c42a3-130">Szenario-Beispiel: Definieren von dynamischen Zuteilungen auf der Basis der verkauften Artikel</span><span class="sxs-lookup"><span data-stu-id="c42a3-130">Scenario Example: Defining Dynamic Allocations Based on Items Sold</span></span>](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)|  

## <a name="see-also"></a><span data-ttu-id="c42a3-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c42a3-131">See Also</span></span>  
 <span data-ttu-id="c42a3-132">[Einrichten der Kostenrechnung](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="c42a3-132">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
 <span data-ttu-id="c42a3-133">[Übertragung und Buchung von Kostenzuteilungen](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="c42a3-133">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 <span data-ttu-id="c42a3-134">[Kostenrechnung](finance-manage-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="c42a3-134">[Accounting for Costs](finance-manage-cost-accounting.md) </span></span>  
 <span data-ttu-id="c42a3-135">[Terminologie der Kostenrechnung](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="c42a3-135">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
 [<span data-ttu-id="c42a3-136">Informationen zur Kostenrechnung</span><span class="sxs-lookup"><span data-stu-id="c42a3-136">About Cost Accounting</span></span>](finance-about-cost-accounting.md)

