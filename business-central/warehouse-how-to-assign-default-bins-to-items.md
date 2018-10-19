---
title: "Vorgehensweise: Zuordnen der Vorgabelagerplätze zu Artikeln | Microsoft Docs"
description: "Wenn Sie in einem Lagerort Lagerplätze verwenden, kann das Zuordnen von Vorgabelagerplätzen zu Ihren Artikeln den Warenausgangs-, Wareneingangs- und Umlagerungsprozess wesentlich vereinfachen. Wenn einem Artikel ein Vorgabelagerplatz zugeordnet wurde, wird diesen Lagerplatz jedes Mal vorgeschlagen, wenn Sie eine Transaktion mit diesem Artikel starten."
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
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e6c6c8a54ae638fa90bca94e43a38d120b5fd3f6
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="assign-default-bins-to-items"></a><span data-ttu-id="3185f-104">Zuordnen der Vorgabelagerplätze zu Artikeln</span><span class="sxs-lookup"><span data-stu-id="3185f-104">Assign Default Bins to Items</span></span>
<span data-ttu-id="3185f-105">Wenn Sie in einem Lagerort Lagerplätze verwenden, kann das Zuordnen von Vorgabelagerplätzen zu Ihren Artikeln den Warenausgangs-, Wareneingangs- und Umlagerungsprozess wesentlich vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="3185f-105">If you are using bins at a location, assigning default bins to your items can make the process of shipping, receiving, and moving your items much easier.</span></span> <span data-ttu-id="3185f-106">Wenn einem Artikel ein Vorgabelagerplatz zugeordnet wurde, wird diesen Lagerplatz jedes Mal vorgeschlagen, wenn Sie eine Transaktion mit diesem Artikel starten.</span><span class="sxs-lookup"><span data-stu-id="3185f-106">When a default bin is assigned to an item, this bin is suggested every time you initiate a transaction for this item.</span></span> <span data-ttu-id="3185f-107">Vorgabelagerplätze werden im Fenster **Lagerplatzinhalt** definiert.</span><span class="sxs-lookup"><span data-stu-id="3185f-107">Default bins are defined in the **Bin Content** window.</span></span>  

## <a name="to-assign-a-default-bin-to-an-item"></a><span data-ttu-id="3185f-108">So weisen Sie einen Standardlagerplatz einem Artikel zu</span><span class="sxs-lookup"><span data-stu-id="3185f-108">To assign a default bin to an item</span></span>
1.  <span data-ttu-id="3185f-109">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Lagerplatzinh. Erst.-Vorschlag** ein, und wählen den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="3185f-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bin Content Creation Worksheet**, and choose the related link.</span></span>  
2.  <span data-ttu-id="3185f-110">Geben Sie den Lagerplatzcode und die Artikelinformationen für jeden Lagerplatz ein, den Sie als Vorgabelagerplatz für einen Artikel einrichten möchten.</span><span class="sxs-lookup"><span data-stu-id="3185f-110">Fill in the bin code and item information for each bin that you would like to set up as a default for an item.</span></span> <span data-ttu-id="3185f-111">Stellen Sie sicher, das das Feld **Standard** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3185f-111">Make sure to select the **Default** field.</span></span>  
3.  <span data-ttu-id="3185f-112">Wählen Sie die **Lagerplatzinhalt erstellen** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="3185f-112">Choose the **Create Bin Content** action.</span></span> <span data-ttu-id="3185f-113">Jetzt werden Ihrem Artikel Vorgabelagerplätze zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="3185f-113">Default bins are now assigned for your item.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="3185f-114">Wenn ein Artikel eingelagert wird, dem noch kein Vorgabelagerplatz zugeordnet wurde, wird dem Artikel der Lagerplatz als Vorgabelagerplatz zugeordnet, in den der Artikel eingelagert wird.</span><span class="sxs-lookup"><span data-stu-id="3185f-114">When an item is put away, if the item does not have a default bin assigned, the bin where the item is put away is assigned as the default.</span></span>  

## <a name="to-change-the-default-bin-for-an-item"></a><span data-ttu-id="3185f-115">So ändern Sie den Standardlagerplatz für einen Artikel</span><span class="sxs-lookup"><span data-stu-id="3185f-115">To change the default bin for an item</span></span>  
<span data-ttu-id="3185f-116">Es kann sein, dass Sie die Zuordnung des Vorgabelagerplatzes für einen Artikel ändern oder einem neuen Artikel einen Vorgabelagerplatz zuordnen müssen.</span><span class="sxs-lookup"><span data-stu-id="3185f-116">You may need to change the default bin assignment for an item or assign a default bin to a new item.</span></span>    
1.  <span data-ttu-id="3185f-117">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Lagerplatzinhalt** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="3185f-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bin Contents**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="3185f-118">Wählen Sie im Feld **Lagerortfilter** den geeigneten Lagerortcode aus.</span><span class="sxs-lookup"><span data-stu-id="3185f-118">In the **Location Filter** field, select the appropriate location code.</span></span>  
3.  <span data-ttu-id="3185f-119">Suchen Sie die aktuelle Zeile mit dem Vorgabewert des Artikels und deaktivieren Sie das Kontrollkästchen **Vorgabewert**.</span><span class="sxs-lookup"><span data-stu-id="3185f-119">Find the current default bin content entry for the item and clear the **Default Bin** check box.</span></span>  
4.  <span data-ttu-id="3185f-120">Suchen Sie die Lagerplatzinhaltszeile des Lagerplatzes, den Sie als neuen Vorgabelagerplatz zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="3185f-120">Find the bin content line for the bin that you would like as the new default bin.</span></span> <span data-ttu-id="3185f-121">Aktivieren Sie das Kontrollkästchen **Standardlagerplatz**.</span><span class="sxs-lookup"><span data-stu-id="3185f-121">Select the **Default Bin** check box.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="3185f-122">Wenn ein Artikel erstmalig eingelagert wird, dem noch kein Vorgabelagerplatz zugeordnet wurde, ordnet die Anwendung dem Artikel den Lagerplatz als Vorgabelagerplatz zu, in den der Artikel eingelagert wird.</span><span class="sxs-lookup"><span data-stu-id="3185f-122">When an item is put away for the first time, and the item does not have a default bin assigned, the system will assign the bin where the item is put away as the default bin for the item.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3185f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3185f-123">See Also</span></span>  
[<span data-ttu-id="3185f-124">Logistik</span><span class="sxs-lookup"><span data-stu-id="3185f-124">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="3185f-125">Lagerbest</span><span class="sxs-lookup"><span data-stu-id="3185f-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="3185f-126">[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="3185f-126">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="3185f-127">[Montageverwaltung](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="3185f-127">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="3185f-128">Designdetails: Logistik</span><span class="sxs-lookup"><span data-stu-id="3185f-128">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="3185f-129">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3185f-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

