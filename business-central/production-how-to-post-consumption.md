---
title: Den Verbrauch über Stapelverarbeitung buchen
description: Wenn die Buchungsmethode **Manuell** ist, müssen Sie den Verbrauch manuell mit einem Verbrauchsprotokoll buchen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 66a19b624c74ec844806c27c490c300746b46704
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787902"
---
# <a name="batch-post-production-consumption"></a><span data-ttu-id="1453e-103">Produktionsverbrauch mit Stapelverarbeitung buchen</span><span class="sxs-lookup"><span data-stu-id="1453e-103">Batch Post Production Consumption</span></span>

<span data-ttu-id="1453e-104">Wenn die Buchungsmethode **Manuell** ist, müssen Sie den Verbrauch manuell mit einem Verbrauchsprotokoll buchen.</span><span class="sxs-lookup"><span data-stu-id="1453e-104">If the flushing method is **Manual**, you must post the components manually, using a consumption journal.</span></span>  

>[!NOTE]
> <span data-ttu-id="1453e-105">Wenn Sie auf der Lagerortkarte im Feld **Kommissionierung erforderlich** ein Häkchen gesetzt haben, um anzugeben, dass für den Lagerort die Bearbeitung der Kommissionierung erforderlich ist, müssen Sie diese Stapelvearbeitung nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="1453e-105">If you have placed a check mark in the **Require Pick** field on the location card to indicate that the location requires inventory pick processing, then you do not need to use this batch job.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="1453e-106">übernimmt den Verbrauch, wenn Sie die Lagerkommissionierung buchen.</span><span class="sxs-lookup"><span data-stu-id="1453e-106">will handle consumption when you post the inventory pick.</span></span> <span data-ttu-id="1453e-107">Weitere Informationen finden Sie unter [Kommissionierung für die Produktion oder Montage](warehouse-how-to-pick-for-production.md#to-pick-components-in-basic-warehouse-configurations).</span><span class="sxs-lookup"><span data-stu-id="1453e-107">For more information, see [Pick for Production or Assembly](warehouse-how-to-pick-for-production.md#to-pick-components-in-basic-warehouse-configurations).</span></span> 

<span data-ttu-id="1453e-108">Sie können [!INCLUDE[prod_short](includes/prod_short.md)] so einstellen, um automatisch (*flush*) Komponenten zu buchen, wenn Sie beginnen oder Fertigungsaufträge beenden.</span><span class="sxs-lookup"><span data-stu-id="1453e-108">You can also set up [!INCLUDE[prod_short](includes/prod_short.md)] to automatically post (*flush*) components when you start or finish production orders.</span></span> <span data-ttu-id="1453e-109">Weitere Informationen finden Sie unter [Vorgehensweise: Komponenten entsprechend dem Arbeitsgangs-Ausstoß leeren](production-how-to-flush-components-according-to-operation-output.md).</span><span class="sxs-lookup"><span data-stu-id="1453e-109">For more information, see [Enable Flushing of Components According to Operation Output](production-how-to-flush-components-according-to-operation-output.md).</span></span>

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a><span data-ttu-id="1453e-110">Die Laufzeit für eine oder mehrere Verbrauchszeile buchen</span><span class="sxs-lookup"><span data-stu-id="1453e-110">To post consumption for one or more production order lines</span></span>

1.  <span data-ttu-id="1453e-111">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **FA-Verbrauchs Buch.-Blatt** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="1453e-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Consumption Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1453e-112">Füllen Sie die Felder mit den Daten des Fertigungsauftrags und den Verbrauchsdaten aus.</span><span class="sxs-lookup"><span data-stu-id="1453e-112">Fill in the fields with the production order data and the consumption data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    <span data-ttu-id="1453e-113">Verwenden Sie die Aktion **Verbrauch berechnen**, um Buch.-Blattzeilen von Fertigungsaufträgen basierend auf der Berechnung der Verbrauchsmenge auf der Ist-Menge (der Menge der fertig gestellten Artikel, die Sie ausgewertet haben) oder der Soll-Menge (der Menge von Artikeln, die Sie fertigen möchten) basiert.</span><span class="sxs-lookup"><span data-stu-id="1453e-113">Use the **Calc. Consumption** action to generate journal lines from production orders based on the actual output (the quantity of finished goods that you have reported) or on the expected output (the quantity of finished goods that you expect to produce).</span></span>

    > [!NOTE]
    > <span data-ttu-id="1453e-114">Wenn Sie die Standortkarte so konfiguriert haben, dass eine Lagerentnahme erforderlich ist, können nur Mengen eingegeben werden, die bereits über eine Lageraktivität im Feld **Menge** auf der Seite **Verbrauchsjournal** kommissioniert wurden, keine berechnete Menge.</span><span class="sxs-lookup"><span data-stu-id="1453e-114">If you configured the location card to require warehouse pick processing, then only quantities that are already picked through a warehouse activity can be entered in the **Quantity** field in the **Consumption Journal** page, not any calculated quantity.</span></span> <span data-ttu-id="1453e-115">Weitere Informationen unter [Kommissionierung für Montage oder Produktion in erweiterter Lagerkonfiguration](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="1453e-115">For more information, see [Pick for Production or Assembly in Advanced Warehouse Configurations](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)</span></span>

3.  <span data-ttu-id="1453e-116">Um den Verbrauch zu buchen, wählen Sie die Aktion **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="1453e-116">Choose the **Post** action to post the consumption.</span></span> <span data-ttu-id="1453e-117">Die damit verbundenen Bestände werden reduziert.</span><span class="sxs-lookup"><span data-stu-id="1453e-117">The related inventories are reduced.</span></span>



## <a name="see-also"></a><span data-ttu-id="1453e-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1453e-118">See Also</span></span>

<span data-ttu-id="1453e-119">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="1453e-119">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="1453e-120">Produktion einrichten</span><span class="sxs-lookup"><span data-stu-id="1453e-120">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="1453e-121">[Planung](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="1453e-121">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="1453e-122">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="1453e-122">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="1453e-123">Einkauf</span><span class="sxs-lookup"><span data-stu-id="1453e-123">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="1453e-124">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1453e-124">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]
