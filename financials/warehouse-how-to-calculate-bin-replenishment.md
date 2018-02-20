---
title: "Wie Sie Lagerplatzauffüllung berechnen | Microsoft Docs"
description: "Wenn der Lagerort so eingerichtet wurde, dass er die gesteuerte Einlagerung und Kommissionierung verwendet, werden die Prioritäten der Einlagerungsvorlage für den Lagerplatz berücksichtigt, wenn Wareneingänge eingelagert werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e667ca56aa22fafc7fe6d0a4880c419a4272db26
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="calculate-bin-replenishment"></a><span data-ttu-id="df103-103">Lagerplatzauffüllung berechnen</span><span class="sxs-lookup"><span data-stu-id="df103-103">Calculate Bin Replenishment</span></span>
<span data-ttu-id="df103-104">Wenn der Lagerort so eingerichtet wurde, dass er die gesteuerte Einlagerung und Kommissionierung verwendet, werden die Prioritäten der Einlagerungsvorlage für den Lagerplatz berücksichtigt, wenn Wareneingänge eingelagert werden.</span><span class="sxs-lookup"><span data-stu-id="df103-104">When the location is set up to use directed put-away and pick, priorities of the put-away template for the location are taken into account when putting receipts away.</span></span> <span data-ttu-id="df103-105">Prioritäten umfassen die minimalen und maximalen Mengen des Lagerplatzinhalts, die für einen bestimmten Lagerplatz verknüpft wurden, und die Lagerplatzprioritäten.</span><span class="sxs-lookup"><span data-stu-id="df103-105">Priorities include the minimum and maximum quantities of bin content that have been fixed for a particular bin, and the bin rankings.</span></span> <span data-ttu-id="df103-106">Wenn daher gleichmäßig Artikel ankommen, werden die meistverwendeten Kommissionierlagerplätze nachgefüllt, während gleichzeitig Artikel aus ihnen entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="df103-106">Therefore, if items are arriving at a steady pace, the most-used pick bins will be filled up as they are emptied.</span></span>  

<span data-ttu-id="df103-107">Artikel treffen jedoch nicht immer gleichmäßig im Lager ein.</span><span class="sxs-lookup"><span data-stu-id="df103-107">But inventory does not always arrive in a steady trickle.</span></span> <span data-ttu-id="df103-108">Manchmal werden Artikel in großen Mengen gekauft, so dass das Unternehmen einen Rabatt erhalten kann, oder Ihre Fertigung produziert eine größere Menge eines Artikels, um geringe Stückkosten zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="df103-108">Sometimes, items are purchased in large quantities so that the company can obtain a rebate, or your production unit might produce a lot of one item to achieve a low unit cost.</span></span> <span data-ttu-id="df103-109">Dann wiederum erhält das Lager eine Zeit lang keine Artikel mehr und Lagermitarbeiter müssen regelmäßig Artikel aus Palettenlagerplätzen in Kommissionierlagerplätze umpacken.</span><span class="sxs-lookup"><span data-stu-id="df103-109">Then items will not be received in the warehouse again for some time, and the warehouse needs to periodically move items to pick bins from bulk storage areas.</span></span>  

<span data-ttu-id="df103-110">Es ist auch möglich, dass das Lager neue Lieferungen erwartet und daher die Palettenlagerplätze frei machen möchte, bevor die neue Ware eintrifft.</span><span class="sxs-lookup"><span data-stu-id="df103-110">It could also be that the warehouse is expecting new stock to arrive soon and wants to empty the bulk storage area of items before the new merchandise arrives.</span></span>  

<span data-ttu-id="df103-111">Wenn Sie Ihre Palettenlagerplätze mit einer Lagerplatzart definiert haben, die ausschließlich die Aktion **Einlagerung** vorsieht, d. h. die Lagerplatzart hat kein Häkchen bei der Aktion **Kommissionierung**, müssen Sie immer darauf achten, dass Ihre Kommissionierlagerplätze gefüllt sind, da keine Kommissionierung aus Einlagerungslagerplätzen vorgeschlagen wird.</span><span class="sxs-lookup"><span data-stu-id="df103-111">Finally, if you have defined your bulk storage bins with a bin type action **Put Away** only, that is, the bin type does not have the **Pick** action selected, you must always keep your pick bins replenished, since Put Away-type bins are not suggested for a pick of inventory.</span></span>  

## <a name="to-replenish-pick-bins"></a><span data-ttu-id="df103-112">So füllen Sie Kommissionierlagerplätze auf:</span><span class="sxs-lookup"><span data-stu-id="df103-112">To replenish pick bins</span></span>  
1.  <span data-ttu-id="df103-113">Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen") aus und geben Sie **Lagerplatzumlagerungsvorschlag** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="df103-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="df103-114">Wählen Sie die Aktion **Lagerplatzauffüllung berechnen** aus, um die Berichtanforderungsseite zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="df103-114">Choose the **Calculate Bin Replenishment** action to open the report request page.</span></span>  
3.  <span data-ttu-id="df103-115">Füllen Sie das Anforderungsfenster der Stapelverarbeitung aus, um den Umfang der Auffüllvorschläge zu begrenzen, die berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="df103-115">Fill in the batch job request window to limit the scope of the replenishment suggestions that will be calculated.</span></span> <span data-ttu-id="df103-116">Beispielsweise könnten Sie nur für bestimmte Artikel, Zonen oder Lagerplätze zuständig sein.</span><span class="sxs-lookup"><span data-stu-id="df103-116">For example, you might be concerned with particular items, zones, or bins.</span></span>  
4.  <span data-ttu-id="df103-117">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="df103-117">Choose the **OK** button.</span></span> <span data-ttu-id="df103-118">Es werden Zeilen für die Auffüllumlagerungen erstellt, die ausgeführt werden müssen, entsprechend den Regeln, die für Lagerplätze und Lagerplatzinhalte (Artikel in Lagerplätzen) festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="df103-118">Lines are created for the replenishment movements that need to be performed according to the rules that have been set up for the bins and bin contents, that is, items in bins.</span></span>  
5.  <span data-ttu-id="df103-119">Wenn Sie alle vorgeschlagenen Auffüllungen vornehmen möchten, wählen Sie die Aktionen **Lagerplatzumlagerung erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="df103-119">If you want to perform all the suggested replenishments, choose the **Create Movement** action.</span></span> <span data-ttu-id="df103-120">Die Lagermitarbeiter finden jetzt Anweisungen unter dem Menüpunkt **Lagerplatzumlagerungen**, können diese ausführen und sie registrieren.</span><span class="sxs-lookup"><span data-stu-id="df103-120">Employees can now find instructions in the **Movements** menu item, carry them out and register them.</span></span>  
6.  <span data-ttu-id="df103-121">Wenn Sie nur einige der Vorschläge ausführen möchten, löschen Sie die weniger wichtigen Zeilen und erzeugen Sie dann eine Lagerplatzumlagerung.</span><span class="sxs-lookup"><span data-stu-id="df103-121">If you only want some of the suggestions to be performed, delete the lines that are less important and then create a movement.</span></span>  

<span data-ttu-id="df103-122">Wenn Sie das nächste Mal eine Lagerplatzauffüllung berechnen lassen, werden Ihnen wieder die Zeilen vorgeschlagen, die Sie gelöscht haben, wenn diese dann immer noch gültig sind.</span><span class="sxs-lookup"><span data-stu-id="df103-122">The next time you calculate bin replenishment, the suggestions that you have deleted will be recreated, if they are still valid at that time.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="df103-123">Angenommen, die folgenden Bedingungen werden für einen Artikel erfüllt:</span><span class="sxs-lookup"><span data-stu-id="df103-123">If the following conditions are met for an item:</span></span>  
>   
>  -   <span data-ttu-id="df103-124">Der Artikel weist ein Ablaufdatum auf, und</span><span class="sxs-lookup"><span data-stu-id="df103-124">The item has an expiration date, and</span></span>  
> -   <span data-ttu-id="df103-125">Das Feld **Gemäß FEFO kommissionieren** ist auf der Lagerortkarte aktiviert, und</span><span class="sxs-lookup"><span data-stu-id="df103-125">The **Pick According to FEFO** field on the location card is selected, and</span></span>  
> -   <span data-ttu-id="df103-126">Sie verwenden die Funktionalität **Lagerplatzauffüllung berechnen**.</span><span class="sxs-lookup"><span data-stu-id="df103-126">You use the **Calculate Bin Replenishment** functionality</span></span>  
>   
>  <span data-ttu-id="df103-127">In diesem Fall bleiben die Felder **Von Zone** und **Von Lagerplatz** leer, da der Algorithmus zur Berechnung des Ausgangsortes der Umlagerung nur ausgelöst wird, wenn Sie die Funktion **Lagerplatzumlagerung erstellen** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="df103-127">then the **From Zone** and **From Bin** fields will be blank because the algorithm to calculate from where to move the items is triggered only when you activate the **Create Movement** function.</span></span>  

## <a name="see-also"></a><span data-ttu-id="df103-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df103-128">See Also</span></span>  
[<span data-ttu-id="df103-129">Logistik</span><span class="sxs-lookup"><span data-stu-id="df103-129">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="df103-130">Kommissionierung nach FEFO</span><span class="sxs-lookup"><span data-stu-id="df103-130">Picking by FEFO</span></span>](warehouse-picking-by-fefo.md)  
[<span data-ttu-id="df103-131">Lagerbest</span><span class="sxs-lookup"><span data-stu-id="df103-131">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="df103-132">[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="df103-132">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="df103-133">[Montageverwaltung](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="df103-133">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="df103-134">Designdetails: Logistik</span><span class="sxs-lookup"><span data-stu-id="df103-134">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="df103-135">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="df103-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

