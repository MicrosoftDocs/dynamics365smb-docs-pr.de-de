---
title: 'Vorgehensweise: Titel-Beziehungen zwischen Bedarf und Vorrat | Microsoft Docs'
description: Verfolgen des Auftragsbedarfs (Menge mit Bedarfsverursacher), der Absatzplanung, des Rahmenauftrags oder der Planungsparameter (Menge ohne Bedarfsverursacher), auf den bzw. auf die die betreffende Planungszeile zurückzuführen ist
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 25eed1edd8aeb92c875e093a177e59c40d3c3a12
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758918"
---
# <a name="track-relations-between-demand-and-supply"></a><span data-ttu-id="6ee3e-103">Nachverfolgen von Beziehungen zwischen Bedarf und Vorrat</span><span class="sxs-lookup"><span data-stu-id="6ee3e-103">Track Relations Between Demand and Supply</span></span>
<span data-ttu-id="6ee3e-104">Verfolgen des Auftragsbedarfs (Menge mit Bedarfsverursacher), der Absatzplanung, des Rahmenauftrags oder der Planungsparameter (Menge ohne Bedarfsverursacher), auf den bzw. auf die die betreffende Planungszeile zurückzuführen ist</span><span class="sxs-lookup"><span data-stu-id="6ee3e-104">From any supply or demand document in the so-called order network, you can track the order demand (tracked quantity), forecast, blanket sales order, or planning parameter (untracked quantity) that has given rise to the planning line in question.</span></span>

<span data-ttu-id="6ee3e-105">Die Planungsvorschläge beinhalten zusätzliche Planungsinformationen wie Nachverfolgung zu nicht auftragsbezogenen Entitäten und Warnungen, um den Planer bei der Erstellung eines optimalen Beschaffungsplans zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6ee3e-105">The planning worksheets also offers supporting planning information about non-order entities to help the planner obtain an optimal supply plan.</span></span> <span data-ttu-id="6ee3e-106">Weitere Informationen finden Sie unter [Planungselement ohne Bedarfsverursacher](production-how-track-demand-supply.md#untracked-planning-elements).</span><span class="sxs-lookup"><span data-stu-id="6ee3e-106">For more information, see [Untracked Planning Elements](production-how-track-demand-supply.md#untracked-planning-elements).</span></span>

## <a name="to-track-linked-items"></a><span data-ttu-id="6ee3e-107">Um verknüpfte Artikel zu verfolgen</span><span class="sxs-lookup"><span data-stu-id="6ee3e-107">To track linked items</span></span>
<span data-ttu-id="6ee3e-108">Die Verfolgung zeigt, wie Verkaufsaufträge, Fertigungsaufträge und Bestellungen über Reservierungen mit einem Fertigungsauftrag verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="6ee3e-108">Order tracking shows how sales orders, production orders, and purchase orders are related to the manufacturing order through the planning and reservation systems.</span></span>

<span data-ttu-id="6ee3e-109">Nachfolgend wird erläutert, wie Artikel für einen fest geplanten Fertigungsauftrag verfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="6ee3e-109">The following describes how to track linked items on a firm planned production order.</span></span> <span data-ttu-id="6ee3e-110">Die Schritte sind für alle anderen Auftragsarten und der Planungsvorschlagszeilen ähnlich.</span><span class="sxs-lookup"><span data-stu-id="6ee3e-110">The steps are similar for all other order types, and from planning worksheet lines.</span></span>

1. <span data-ttu-id="6ee3e-111">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Fester geplanter Fertigungsauftrag** ein, und wählen Sie dann den zugehörigen Link.</span><span class="sxs-lookup"><span data-stu-id="6ee3e-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Order**, and then choose the related link.</span></span>
2. <span data-ttu-id="6ee3e-112">Öffnen Sie den relevanten fest geplanten Fertigungsauftrag in der Liste.</span><span class="sxs-lookup"><span data-stu-id="6ee3e-112">Open the relevant firm planned production order from the list.</span></span>
3. <span data-ttu-id="6ee3e-113">Wählen Sie im Inforegister **Zeilen** in Aktionen **Funktion** aus, und wählen Sie dann **Auftrag-Verfolgung**.</span><span class="sxs-lookup"><span data-stu-id="6ee3e-113">On the **Lines** FastTab, choose the **Functions** action, and then choose the **Order Tracking** action.</span></span>

<span data-ttu-id="6ee3e-114">In den Zeilen im Fenster **Auftragsverfolgung** werden die Dokumente angezeigt, die sich auf die aktuelle Fertigungsauftragszeile beziehen.</span><span class="sxs-lookup"><span data-stu-id="6ee3e-114">The lines in the **Order Tracking** display the documents that are related to the current production order line.</span></span>

## <a name="untracked-planning-elements"></a><span data-ttu-id="6ee3e-115">Planungselemente ohne Bedarfsverursacher</span><span class="sxs-lookup"><span data-stu-id="6ee3e-115">Untracked Planning Elements</span></span>
<span data-ttu-id="6ee3e-116">Die Seite **Planungselemente ohne Bedarfsverursacher** öffnet sich, wenn Sie das Feld **Mge. ohne Bedarfsverursacher** auf der Seite **Auftragsplanung** auswählen.</span><span class="sxs-lookup"><span data-stu-id="6ee3e-116">The **Untracked Planning Elements** page opens when you choose the **Untracked Qty.** field on the **order Planning** page.</span></span> <span data-ttu-id="6ee3e-117">Er dient beiden Zwecken:</span><span class="sxs-lookup"><span data-stu-id="6ee3e-117">It serves two purposes:</span></span>

1. <span data-ttu-id="6ee3e-118">Sie enthält Informationen zu Mengen ohne Bedarfsverursacher, die angezeigt werden, wenn der Benutzer auf der Seite "Bedarfsverursacher" Mengen ohne Bedarfsverursacher aufruft.</span><span class="sxs-lookup"><span data-stu-id="6ee3e-118">To hold information about untracked quantities displayed when the user looks up from the Order Tracking page to see untracked quantities.</span></span>
2. <span data-ttu-id="6ee3e-119">Sie enthält Warnmeldungen, die angezeigt werden, wenn der Benutzer auf der Seite **Planungsvorschlag** auf ein **Warnungs**-Symbol klickt.</span><span class="sxs-lookup"><span data-stu-id="6ee3e-119">To hold warning messages displayed when the user chooses the **Warning** icon on the **Planning Worksheet** page.</span></span>

<span data-ttu-id="6ee3e-120">Die Seite enthält Posten, die eine Überschussmenge ohne Bedarfsverursacher im Bedarfsverursachernetzwerk ausweisen.</span><span class="sxs-lookup"><span data-stu-id="6ee3e-120">The page contains entries which account for an untracked surplus quantity in order tracking network.</span></span> <span data-ttu-id="6ee3e-121">Diese Posten werden während der Planung erzeugt und zeigen die Herkunft der Überschussmenge ohne Bedarfsverursacher in den Bedarfsverursacherzeilen.</span><span class="sxs-lookup"><span data-stu-id="6ee3e-121">These entries are generated during the planning run and explain where the untracked surplus quantity in the order tracking lines came from.</span></span> <span data-ttu-id="6ee3e-122">Die folgende Herkunft ist für den Überschuss ohne Bedarfsverursacher möglich:</span><span class="sxs-lookup"><span data-stu-id="6ee3e-122">This untracked surplus can come from:</span></span>

- <span data-ttu-id="6ee3e-123">Absatzplanung</span><span class="sxs-lookup"><span data-stu-id="6ee3e-123">Production forecast</span></span>
- <span data-ttu-id="6ee3e-124">Rahmenbestellungen</span><span class="sxs-lookup"><span data-stu-id="6ee3e-124">Blanket orders</span></span>
- <span data-ttu-id="6ee3e-125">Sicherheitsbestand</span><span class="sxs-lookup"><span data-stu-id="6ee3e-125">Safety stock quantity</span></span>
- <span data-ttu-id="6ee3e-126">Minimalbestand</span><span class="sxs-lookup"><span data-stu-id="6ee3e-126">Reorder point</span></span>
- <span data-ttu-id="6ee3e-127">Maximalbestand</span><span class="sxs-lookup"><span data-stu-id="6ee3e-127">Maximum inventory</span></span>
- <span data-ttu-id="6ee3e-128">Bestellmenge</span><span class="sxs-lookup"><span data-stu-id="6ee3e-128">Reorder quantity</span></span>
- <span data-ttu-id="6ee3e-129">Maximale Losgröße</span><span class="sxs-lookup"><span data-stu-id="6ee3e-129">Maximum order quantity</span></span>
- <span data-ttu-id="6ee3e-130">Minimale Losgröße</span><span class="sxs-lookup"><span data-stu-id="6ee3e-130">Minimum order quantity</span></span>
- <span data-ttu-id="6ee3e-131">Losgrößenrundungsfaktor</span><span class="sxs-lookup"><span data-stu-id="6ee3e-131">Order multiple</span></span>
- <span data-ttu-id="6ee3e-132">Toleranz (% der Losgröße)</span><span class="sxs-lookup"><span data-stu-id="6ee3e-132">Dampener (% of lot size)</span></span>

## <a name="see-also"></a><span data-ttu-id="6ee3e-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ee3e-133">See Also</span></span>  
<span data-ttu-id="6ee3e-134">[Planung](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="6ee3e-134">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="6ee3e-135">Produktion einrichten</span><span class="sxs-lookup"><span data-stu-id="6ee3e-135">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="6ee3e-136">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="6ee3e-136">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="6ee3e-137">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="6ee3e-137">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="6ee3e-138">Einkauf</span><span class="sxs-lookup"><span data-stu-id="6ee3e-138">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="6ee3e-139">Designdetails: Reservierung, Auftragsnachverfolgung und Aktionsmeldungen</span><span class="sxs-lookup"><span data-stu-id="6ee3e-139">Design Details: Reservation, Tracking, and Action Messaging</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
<span data-ttu-id="6ee3e-140">[Designdetails: Vorratsplanung](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="6ee3e-140">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="6ee3e-141">Bewährte Einrichtungsmethoden: Beschaffungsplanung</span><span class="sxs-lookup"><span data-stu-id="6ee3e-141">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="6ee3e-142">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6ee3e-142">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
