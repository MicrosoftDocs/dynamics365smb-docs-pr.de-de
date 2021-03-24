---
title: Ressourcenverbrauch und Preise aufzeichnen und anpassen | Microsoft Docs
description: Beschreibt, wie Sie den Ressourcenverbrauch oder den Verbrauch erfassen können, die einem Projekt zugeordnet sind, um Kosten, Preisen und Arbeitstypen zu verwalten.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 48d7615ec32424400133c9dbf6b63c46d450f019
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388374"
---
# <a name="use-resources-for-jobs"></a><span data-ttu-id="197db-103">Verwenden von Ressourcen für Projekte</span><span class="sxs-lookup"><span data-stu-id="197db-103">Use Resources for Jobs</span></span>
<span data-ttu-id="197db-104">Wenn Sie den Verbrauch von Ressourcen im Projekt Buch.-Blatt buchen, können Sie die Einstands- und Verkaufspreise, die Arbeitstypen und die damit verknüpften Projekte verfolgen.</span><span class="sxs-lookup"><span data-stu-id="197db-104">You record the usage of resources in the job journal to keep track of costs, prices, and the work types that are linked to jobs.</span></span> <span data-ttu-id="197db-105">Weitere Informationen finden Sie unter [Verwendung von Datensätzen für Projekte](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="197db-105">For more information, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

> [!NOTE]
> <span data-ttu-id="197db-106">Sie können auch externe Ressourcen einkaufen, z.B. um einem Kreditor die gelieferte Arbeit in Rechnung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="197db-106">You can also purchase external resources, for example, to invoice a vendor for work delivered.</span></span> <span data-ttu-id="197db-107">Weitere Informationen finden Sie unter [Käufe erfassen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="197db-107">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

<span data-ttu-id="197db-108">Sie können auch den Verbrauch einer Ressource in einem Ressourcen Buch.-Blatt buchen.</span><span class="sxs-lookup"><span data-stu-id="197db-108">You can also post the usage of a resource in a resource journal.</span></span> <span data-ttu-id="197db-109">Posten, die in einem Ressourcen Buch.-Blatt gebucht werden, haben keinen Einfluss auf die Finanzbuchhaltung.</span><span class="sxs-lookup"><span data-stu-id="197db-109">Entries posted in a resource journal have no effect on the general ledger.</span></span>

## <a name="to-assign-resources-to-jobs"></a><span data-ttu-id="197db-110">So weisen Sie Projekten Ressourcen zu</span><span class="sxs-lookup"><span data-stu-id="197db-110">To assign resources to jobs</span></span>
<span data-ttu-id="197db-111">Sie weisen Projekten Ressourcen zu, indem Sie Projektplanungszeilen für das Projekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="197db-111">You assign resources to jobs by creating job planning lines for the job.</span></span> <span data-ttu-id="197db-112">Weitere Informationen finden Sie unter  [Projekte erstellen](projects-how-create-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="197db-112">For more information, see [Create Jobs](projects-how-create-jobs.md).</span></span>

## <a name="to-record-resource-usage-for-a-job"></a><span data-ttu-id="197db-113">Um Ressourcenverbrauch für ein Projekt buchen</span><span class="sxs-lookup"><span data-stu-id="197db-113">To record resource usage for a job</span></span>
1. <span data-ttu-id="197db-114">Wählen Sie das Symbol ![Glühbirne , das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Projekt Buch.-Blätter** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="197db-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="197db-115">Öffnen Sie das relevante Projekt-Buch.-Blatt und füllen Sie die Felder nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="197db-115">Open a relevant job journal batch, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="197db-116">Wenn der Verkaufsauftrag ausgeführt wurde, wählen Sie die Aktion **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="197db-116">When the journal is complete, choose the **Post** action.</span></span>

## <a name="to-adjust-resource-prices"></a><span data-ttu-id="197db-117">Um Ressourcenpreise zu justieren:</span><span class="sxs-lookup"><span data-stu-id="197db-117">To adjust resource prices</span></span>
<span data-ttu-id="197db-118">Wenn Sie die Einstands- und Verkaufspreise für eine große Anzahl von Ressourcen ändern möchten, können Sie den Batchauftrag verwenden.</span><span class="sxs-lookup"><span data-stu-id="197db-118">If you want to change costs or prices for a large number of resources, you can use a batch job.</span></span>  

1. <span data-ttu-id="197db-119">Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Ressourcenkosten/Preise anpassen** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="197db-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Adjust Resource Costs/Prices**, and then choose the related link.</span></span>
2. <span data-ttu-id="197db-120">Füllen Sie die anderen relevanten Felder wie erforderlich aus, und wählen Sie dann die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="197db-120">Fill in the fields on a line as necessary, and then choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="197db-121">Diese Stapelverarbeitung erzeugt oder aktualisiert keine alternativen Einkaufs- oder Verkaufspreise für Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="197db-121">This batch job does not create or adjust alternate costs or prices for resources.</span></span> <span data-ttu-id="197db-122">Sie ändert lediglich den Inhalt des Feldes auf der Ressourcenkarte für das Feld **Feld korrigieren**, das Sie in der Stapelverarbeitung ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="197db-122">It only changes the contents of the field on the resource card for the **Adjust Field** field that you selected in the batch job.</span></span> <span data-ttu-id="197db-123">Die Änderung tritt für die Ressourcen sofort in Kraft, überprüfen Sie daher Ihre Korrekturfaktoren, bevor Sie die Stapelverarbeitung ausführen.</span><span class="sxs-lookup"><span data-stu-id="197db-123">The adjustment will take effect immediately for resources, so check your adjustment factors before you run the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a><span data-ttu-id="197db-124">Um Ressourcen-Preisänderungsvorschläge auf Basis bestehender alternativer Preise zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="197db-124">To get resource price change suggestions based on existing alternate prices</span></span>
<span data-ttu-id="197db-125">Wenn Sie bereits alternative Ressourcenpreise für mehrere Ressourcen eingerichtet haben, können Sie den Batchauftrag verwenden, um alternative Ressourcenpreise einzurichten.</span><span class="sxs-lookup"><span data-stu-id="197db-125">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="197db-126">Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Ressourcenpreisänderungen** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="197db-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="197db-127">Wählen Sie die Aktion **Res. Preisänderung (Preis) vorschlagen** aus. Füllen Sie dann die Felder wie notwendig aus.</span><span class="sxs-lookup"><span data-stu-id="197db-127">Choose the **Suggest Res. Price Chg. (Price)** action, and then fill in the fields as necessary.</span></span>
3. <span data-ttu-id="197db-128">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="197db-128">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="197db-129">Wenn die Stapelverarbeitung beendet ist, öffnen Sie die Seite **Ressourcen-Preisänderungen**, um die Ergebnisse der Stapelverarbeitung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="197db-129">When the batch job is finished, the **Resource Price Changes** page shows the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a><span data-ttu-id="197db-130">So erstellen Sie Ressourcenpreisvorschläge auf Basis bestehender Standard-VK-Preise</span><span class="sxs-lookup"><span data-stu-id="197db-130">To get resource price change suggestions based on standard prices</span></span>
<span data-ttu-id="197db-131">Wenn Sie einen oder mehrere alternative Ressourcenpreise basierend auf den Standardpreisen auf den Ressourcenkarten festlegen möchten, dann können Sie den Batchauftrag verwenden.</span><span class="sxs-lookup"><span data-stu-id="197db-131">If you want to set up multiple alternate resource prices based on the standard prices on the resource cards, you can use a batch job.</span></span>  

1. <span data-ttu-id="197db-132">Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Ressourcenpreisänderungen** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="197db-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="197db-133">Wählen Sie die Aktion **Res. Preisänderung (Res) vorschlagen** aus. Füllen Sie dann die Felder wie notwendig aus.</span><span class="sxs-lookup"><span data-stu-id="197db-133">Choose the **Suggest Res. Price Chg. (Res.)** action, and then fill in the fields as necessary.</span></span>  
3. <span data-ttu-id="197db-134">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="197db-134">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="197db-135">Wenn die Stapelverarbeitung beendet ist, öffnen Sie die Seite **Ressourcen-VK-Preisarbeitsblätter**, um die Ergebnisse der Stapelverarbeitung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="197db-135">When the batch job is finished, open the **Resource Price Changes** page to see the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a><span data-ttu-id="197db-136">Um Ressourcenpreisvorschläge auf Basis alternierender Preise zu erhalten</span><span class="sxs-lookup"><span data-stu-id="197db-136">To get resource price change suggestions based on alternate prices</span></span>
<span data-ttu-id="197db-137">Wenn Sie bereits einen alternativen Ressourcenpreis für einige Ressourcen eingerichtet haben, können Sie einen Batch-Job verwenden, um mehrere alternative Ressourcenpreise einzurichten.</span><span class="sxs-lookup"><span data-stu-id="197db-137">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="197db-138">Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Res. Preisänderung (Preis) vorschlagen.** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="197db-138">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Suggest Res. Price Chg. (Price)**, and then choose the related link.</span></span>  
2. <span data-ttu-id="197db-139">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="197db-139">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="197db-140">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="197db-140">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="197db-141">Wenn die Stapelverarbeitung beendet ist, öffnen Sie die Seite **Ressourcen-VK-Preisarbeitsblätter**, um die Ergebnisse der Stapelverarbeitung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="197db-141">When the batch job is finished, open the **Resource Price Changes** page to see the results of the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="197db-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="197db-142">See Also</span></span>
[<span data-ttu-id="197db-143">Projektmanagement</span><span class="sxs-lookup"><span data-stu-id="197db-143">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="197db-144">Finanzen</span><span class="sxs-lookup"><span data-stu-id="197db-144">Finance</span></span>](finance.md)  
<span data-ttu-id="197db-145">[Einkauf](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="197db-145">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="197db-146">[Verkauf](sales-manage-sales.md)   </span><span class="sxs-lookup"><span data-stu-id="197db-146">[Sales](sales-manage-sales.md)   </span></span>  
<span data-ttu-id="197db-147">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="197db-147">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]