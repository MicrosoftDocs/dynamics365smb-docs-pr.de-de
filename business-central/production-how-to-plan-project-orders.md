---
title: Projekt nach Projekt planen | Microsoft Docs
description: Diese Planungsaufgabe beginnt mit einem Verkaufsauftrag auf der Seite **Verkaufsauftragsplanung** . Nachdem ein Projektfertigungsauftrag erstellt wurde, kann die Planung auf der Seite **Auftragsplanung** fortgeführt werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 09fea87bb1d8606390fe8c0ed5b2e3780dbc4978
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919188"
---
# <a name="plan-project-orders"></a><span data-ttu-id="41922-104">Projektaufträge planen</span><span class="sxs-lookup"><span data-stu-id="41922-104">Plan Project Orders</span></span>
<span data-ttu-id="41922-105">Diese Planungsaufgabe beginnt mit einem Verkaufsauftrag auf der Seite **Verkaufsauftragsplanung** .</span><span class="sxs-lookup"><span data-stu-id="41922-105">This planning task starts from a sales order and uses the **Sales Order Planning** page.</span></span> <span data-ttu-id="41922-106">Nachdem ein Projektfertigungsauftrag erstellt wurde, kann die Planung auf der Seite **Auftragsplanung** fortgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="41922-106">Once you have created a project production order, you can plan it further by using the **Order Planning** page.</span></span>  

## <a name="to-create-a-project-production-order"></a><span data-ttu-id="41922-107">Projektfertigungsaufträge erstellen</span><span class="sxs-lookup"><span data-stu-id="41922-107">To create a project production order</span></span>  

1.  <span data-ttu-id="41922-108">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Verkaufsaufträge** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="41922-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders** , and then choose the related link.</span></span>  
2.  <span data-ttu-id="41922-109">Wählen Sie den Verkaufsauftrag, der für das Produktionsprojekt steht, und wählen die Aktion **Planung** .</span><span class="sxs-lookup"><span data-stu-id="41922-109">Select the sales order that represents the production project, and then choose the **Planning** action.</span></span>  
4.  <span data-ttu-id="41922-110">Klicken Sie auf der Seite **Verkaufsauftragsplanung** auf **Produktionsauftrag erstellen** .</span><span class="sxs-lookup"><span data-stu-id="41922-110">On the **Sales Order Planning** page, choose  the **Create Prod. Order** action.</span></span>  
5.  <span data-ttu-id="41922-111">Wählen Sie auf der Seite **Auftrag aus Verkauf erstellen** im Feld **Auftragsart** die Option **Projektauftrag** aus.</span><span class="sxs-lookup"><span data-stu-id="41922-111">On the **Create Order from Sales** page, in the **Order Type** field, select **Project Order** .</span></span>  
6.  <span data-ttu-id="41922-112">Wählen Sie die Schaltfläche **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="41922-112">Choose the **Yes** button.</span></span>  
7.  <span data-ttu-id="41922-113">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Fertigungsaufträge** ein, und wählen Sie dann den zugehörigen Link.</span><span class="sxs-lookup"><span data-stu-id="41922-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Production Orders** , and then choose the related link.</span></span>
8. <span data-ttu-id="41922-114">Öffnen Sie den soeben erstellten Fertigungsauftrag.</span><span class="sxs-lookup"><span data-stu-id="41922-114">Open the production order just created.</span></span>  

    <span data-ttu-id="41922-115">Im Feld **Herkunftsart** des Fertigungsauftrags ist ein **Verkaufskopf** enthalten, und der Auftrag besteht aus mehreren Zeilen, eine pro zu fertigenden Verkaufszeilenartikel.</span><span class="sxs-lookup"><span data-stu-id="41922-115">Notice that the **Source Type** field of the production order contains **Sales Header** and the order has multiple lines, one for each sales line item that must be produced.</span></span>  
9. <span data-ttu-id="41922-116">Wählen Sie die Aktion **Planung** aus.</span><span class="sxs-lookup"><span data-stu-id="41922-116">Choose the **Planning** action.</span></span>
10. <span data-ttu-id="41922-117">Klicken Sie auf der Seite **Auftragsplanung** auf Funktionen und dann auf **Aktualisieren** , um den neuen Bedarf zu kalkulieren.</span><span class="sxs-lookup"><span data-stu-id="41922-117">On the **Order Planning** page, choose the **Refresh** action to calculate new demand.</span></span>  

<span data-ttu-id="41922-118">Die Auftragskopfzeile für das Projekt wird angezeigt, wobei alle Zeilen für nicht erfüllten Bedarf darunter erweitert sind.</span><span class="sxs-lookup"><span data-stu-id="41922-118">The order header line for the project order is displayed with all unfulfilled demand lines expanded under it.</span></span> <span data-ttu-id="41922-119">Obwohl der Fertigungsauftrag Zeilen für mehrere gefertigte Artikel enthält, wird der Gesamtbedarf für alle Fertigungsauftragszeilen unter einer Auftragskopfzeile auf der Seite **Auftragsplanung** aufgeführt, und der ursprüngliche Debitorenname wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="41922-119">Although the production order contains lines for several produced items, the total demand for all production order lines is listed under one order header line on the **Order Planning** page, and the original customer name is displayed.</span></span> <span data-ttu-id="41922-120">Setzen Sie die Planung für den Bedarf so fort wie unter [Bedarf für neuen Auftrag nach Auftrag planen](production-how-to-plan-for-new-demand.md) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="41922-120">You can now proceed to plan for the demand as described in [Plan for New Demand Order by Order](production-how-to-plan-for-new-demand.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="41922-121">Bedarfszeilen im projektbezogenen Produktionsauftrag, die **Prod. Auftrag** im Feld **Beschaffungsmethode** haben, stellen zugrunde liegende Fertigungsaufträge dar.</span><span class="sxs-lookup"><span data-stu-id="41922-121">Demand lines in the project production order that have **Prod. Order** in their **Replenishment System** field represent underlying production orders.</span></span> <span data-ttu-id="41922-122">Nachdem Sie diese Fertigungsaufträge erstellt haben, müssen Sie nochmals den Plan auf der Seite **Auftragsplanung** berechnen, um sämtliche nicht befriedigte Nachfrage nach Komponenten für diese zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="41922-122">After you have generated these production orders, you must again calculate a plan on the **Order Planning** page to identify any unfulfilled component demand for them.</span></span> <span data-ttu-id="41922-123">Dies bedeutet, dass die Projektbeziehung nicht mehr auf der Seite sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="41922-123">In that case, they are displayed as demand lines under a normal production order header line, meaning, the project relation is no longer visible on the page.</span></span> <span data-ttu-id="41922-124">Wenn Sie jedoch die Option "Auftragsverfolgung" verwenden, können Sie für alle Beschaffungsaufträge, die unter dem ursprünglichen Verkaufsauftrag erstellt wurden, eine Rück- und Vorschau ausführen.</span><span class="sxs-lookup"><span data-stu-id="41922-124">However, if you are using the Order Tracking feature, then you can look back and forth to all supply orders made under the original sales order.</span></span>  

## <a name="see-also"></a><span data-ttu-id="41922-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41922-125">See Also</span></span>
<span data-ttu-id="41922-126">[Planung](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="41922-126">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="41922-127">Produktion einrichten</span><span class="sxs-lookup"><span data-stu-id="41922-127">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="41922-128">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="41922-128">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="41922-129">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="41922-129">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="41922-130">Einkauf</span><span class="sxs-lookup"><span data-stu-id="41922-130">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="41922-131">[Designdetails: Beschaffungsplanung](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="41922-131">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="41922-132">Bewährte Einrichtungsmethoden: Beschaffungsplanung</span><span class="sxs-lookup"><span data-stu-id="41922-132">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="41922-133">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="41922-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
