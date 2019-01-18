---
title: "Definieren von Kostenstellen und Kostenträgern für Kontenpläne | Microsoft Docs"
description: "Sie können die Ausgaben- und Einnahmenposten aus dem Sachkonto in die Kostenrechnung entweder für jede Sachkontobuchung oder mit einem Batchauftrag übertragen. Wenn Sie die Übertragung ausführen, überträgt das System nur die Posten, die bereits mit einer Kostenstelle oder einem Kostenträger verknüpft sind. Um eine sinnvolle Übertragung herzustellen, müssen Sie sicherstellen, dass die Kostenstellen und die Kostenträger korrekt definiert sind."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: b3ca863a9f4969046695e0cec16fedf6f5ac7aec
ms.contentlocale: de-de
ms.lasthandoff: 11/22/2018

---
# <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a><span data-ttu-id="d21f4-105">Definieren von Kostenstellen und Kostenträgern für Kontenpläne</span><span class="sxs-lookup"><span data-stu-id="d21f4-105">Defining Cost Centers and Cost Objects for Chart of Accounts</span></span>
<span data-ttu-id="d21f4-106">Sie können die Ausgaben- und Einnahmenposten aus dem Sachkonto in die Kostenrechnung entweder für jede Sachkontobuchung oder mit einem Batchauftrag übertragen.</span><span class="sxs-lookup"><span data-stu-id="d21f4-106">You can automatically transfer the expense and income entries from the general ledger to cost accounting either for each general ledger posting or with a batch job.</span></span> <span data-ttu-id="d21f4-107">Wenn Sie die Übertragung ausführen, überträgt [!INCLUDE[d365fin](includes/d365fin_md.md)] nur die Posten, die bereits mit einer Kostenstelle oder einem Kostenträger verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="d21f4-107">When you do the transfer, [!INCLUDE[d365fin](includes/d365fin_md.md)] only transfers the entries that are already linked to a cost center or a cost object.</span></span> <span data-ttu-id="d21f4-108">Um eine sinnvolle Übertragung herzustellen, müssen Sie sicherstellen, dass die Kostenstellen und die Kostenträger korrekt definiert sind.</span><span class="sxs-lookup"><span data-stu-id="d21f4-108">To establish a meaningful transfer, you must ensure that the cost centers and cost objects are correctly defined.</span></span>  

## <a name="defining-default-dimension-values-for-general-ledger-accounts"></a><span data-ttu-id="d21f4-109">Definieren von Standarddimensionswerten für Sachkonten</span><span class="sxs-lookup"><span data-stu-id="d21f4-109">Defining Default Dimension Values for General Ledger Accounts</span></span>  
<span data-ttu-id="d21f4-110">Für jedes Sachkonto können Sie Standarddimensionswerte in der Tabelle **Standard-Dimensionen** definieren.</span><span class="sxs-lookup"><span data-stu-id="d21f4-110">For each general ledger account, you can define default dimension values in the **Default Dimension** table.</span></span> <span data-ttu-id="d21f4-111">Das folgende Beispiel zeigt, wie Sie definieren, dass es immer eine Kostenstelle ABTEILUNG, aber nie einen Kostenträger PROJEKT geben soll, wenn Sie auf ein Sachkonto buchen.</span><span class="sxs-lookup"><span data-stu-id="d21f4-111">The following example shows how to define that there should always be a DEPARTMENT cost center, but never be a PROJECT cost object when posting to a general ledger account.</span></span>  

|<span data-ttu-id="d21f4-112">**Dimensionscode**</span><span class="sxs-lookup"><span data-stu-id="d21f4-112">**Dimension Code**</span></span>|<span data-ttu-id="d21f4-113">**Dimensionswertbuchung**</span><span class="sxs-lookup"><span data-stu-id="d21f4-113">**Value Posting**</span></span>|  
|------------------------------------------|-----------------------------------------|  
|<span data-ttu-id="d21f4-114">Abteilung</span><span class="sxs-lookup"><span data-stu-id="d21f4-114">Department</span></span>|<span data-ttu-id="d21f4-115">Code notwendig</span><span class="sxs-lookup"><span data-stu-id="d21f4-115">Code Mandatory</span></span>|  
|<span data-ttu-id="d21f4-116">Kostenträger</span><span class="sxs-lookup"><span data-stu-id="d21f4-116">Project</span></span>|<span data-ttu-id="d21f4-117">Kein Code</span><span class="sxs-lookup"><span data-stu-id="d21f4-117">No Code</span></span>|  

## <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a><span data-ttu-id="d21f4-118">Definieren von Dimensionswerten für Gemeinkosten und direkte Kosten</span><span class="sxs-lookup"><span data-stu-id="d21f4-118">Defining Dimension Values for Overhead Costs and Direct Costs</span></span>  
 <span data-ttu-id="d21f4-119">Sie können Gemeinkosten an eine Kostenstelle und direkte Kosten an einen Kostenträger übertragen.</span><span class="sxs-lookup"><span data-stu-id="d21f4-119">You can transfer overhead costs to a cost center and direct costs to a cost object.</span></span> <span data-ttu-id="d21f4-120">In der folgenden Tabelle wird die optimale Kombination aus Dimensionseinrichtungswerten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d21f4-120">The following table shows the optimal combination of the dimension setup values.</span></span>  

|<span data-ttu-id="d21f4-121">Übertragen in</span><span class="sxs-lookup"><span data-stu-id="d21f4-121">Transfer To</span></span>|<span data-ttu-id="d21f4-122">Kostenstellenbuchung</span><span class="sxs-lookup"><span data-stu-id="d21f4-122">Cost Center Posting</span></span>|<span data-ttu-id="d21f4-123">Kostenträgerbuchung</span><span class="sxs-lookup"><span data-stu-id="d21f4-123">Cost Object Posting</span></span>|  
|-----------------|-------------------------|-------------------------|  
|<span data-ttu-id="d21f4-124">Kostenstelle</span><span class="sxs-lookup"><span data-stu-id="d21f4-124">Cost Center</span></span>|<span data-ttu-id="d21f4-125">Code notwendig</span><span class="sxs-lookup"><span data-stu-id="d21f4-125">Code Mandatory</span></span>|<span data-ttu-id="d21f4-126">Kein Code</span><span class="sxs-lookup"><span data-stu-id="d21f4-126">No Code</span></span>|  
|<span data-ttu-id="d21f4-127">Kostenträger</span><span class="sxs-lookup"><span data-stu-id="d21f4-127">Cost Object</span></span>|<span data-ttu-id="d21f4-128">Kein Code</span><span class="sxs-lookup"><span data-stu-id="d21f4-128">No Code</span></span>|<span data-ttu-id="d21f4-129">Code notwendig</span><span class="sxs-lookup"><span data-stu-id="d21f4-129">Code Mandatory</span></span>|  

> [!NOTE]  
>  <span data-ttu-id="d21f4-130">Um sicherzustellen, dass die vordefinierte Kostenstelle und der vordefinierte Kostenträger, die bzw. den Sie im Sachkonto eingerichtet haben, automatisch in die Kostenrechnung übertragen werden, aktivieren Sie das Kontrollkästchen **Fibu-Buchung prüfen** auf der Seite Kosenbuchungseinrichtung.</span><span class="sxs-lookup"><span data-stu-id="d21f4-130">To make sure that the predefined cost center and cost object that you set up in the general ledger are automatically carried over to cost accounting, select the **Check G/L Postings** check box in the Cost Accounting Setup page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d21f4-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d21f4-131">See Also</span></span>  
[<span data-ttu-id="d21f4-132">Kostenrechnung</span><span class="sxs-lookup"><span data-stu-id="d21f4-132">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
[<span data-ttu-id="d21f4-133">Einrichten der Kostenrechnung</span><span class="sxs-lookup"><span data-stu-id="d21f4-133">Setting Up Cost Accounting</span></span>](finance-set-up-cost-accounting.md)  
<span data-ttu-id="d21f4-134">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d21f4-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

