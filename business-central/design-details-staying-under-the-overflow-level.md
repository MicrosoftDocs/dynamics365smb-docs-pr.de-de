---
title: 'Designdetails: Unter dem Überlauflevel bleiben  | Microsoft Docs'
description: Wenn die Funktionen Auffüllen auf Maximalbestand Feste Bestellmenge verwendet werden, konzentriert sich das Planungssystem nur auf den voraussichtlichen Lagerbestand in dem vorgegebenen Zeitrahmen. Dies bedeutet, dass das Planungssystem möglicherweise überflüssigen Vorrat vorschlägt, wenn negativer Bedarfs- oder positive Vorratsänderungen außerhalb gegebenen Zeitrahmens auftreten.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: bf602a0a7688c0459b4f7a3711e4f3d75bd8ef00
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306796"
---
# <a name="design-details-staying-under-the-overflow-level"></a><span data-ttu-id="0b136-104">Designdetails: Unter dem Überlauflevel bleiben</span><span class="sxs-lookup"><span data-stu-id="0b136-104">Design Details: Staying under the Overflow Level</span></span>
<span data-ttu-id="0b136-105">Wenn die Funktionen Auffüllen auf Maximalbestand Feste Bestellmenge verwendet werden, konzentriert sich das Planungssystem nur auf den voraussichtlichen Lagerbestand in dem vorgegebenen Zeitrahmen.</span><span class="sxs-lookup"><span data-stu-id="0b136-105">When using the Maximum Qty. and Fixed Reorder Qty. policies, the planning system focuses on the projected inventory in the given time-bucket only.</span></span> <span data-ttu-id="0b136-106">Dies bedeutet, dass das Planungssystem möglicherweise überflüssigen Vorrat vorschlägt, wenn negativer Bedarfs- oder positive Vorratsänderungen außerhalb gegebenen Zeitrahmens auftreten.</span><span class="sxs-lookup"><span data-stu-id="0b136-106">This means that the planning system may suggest superfluous supply when negative demand or positive supply changes occur outside of the given time bucket.</span></span> <span data-ttu-id="0b136-107">Wenn aus diesem Grund ein überflüssiger Vorrat vorgeschlagen wird, berechnet das Planungssystem die zu reduzierende oder zu löschende Vorratsmenge, um überflüssigen Vorrat zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="0b136-107">If, for this reason, a superfluous supply is suggested, the planning system calculates which quantity the supply should be decreased to (or deleted) to avoid the superfluous supply.</span></span> <span data-ttu-id="0b136-108">Diese Menge wird als "Überlauflevel" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0b136-108">This quantity is called the “overflow level.”</span></span> <span data-ttu-id="0b136-109">Diese Menge wird als "Überlauflevel" bezeichnet. Der Überlauf wird als Planungszeile mit einer **Menge ändern** oder **Abbrechen** Operation und der folgenden Warnmeldung mitgeteilt:</span><span class="sxs-lookup"><span data-stu-id="0b136-109">The overflow is communicated as a planning line with a **Change Qty. (Decrease)** or **Cancel** action and the following warning message:</span></span>  

<span data-ttu-id="0b136-110">*Achtung: Der voraussichtliche Lagerbestand [xx] ist höher als das Überlauflevel [xx] am Fälligkeitsdatum [xx].*</span><span class="sxs-lookup"><span data-stu-id="0b136-110">*Attention: The projected inventory [xx] is higher than the overflow level [xx] on the Due Date [xx].*</span></span>  

<span data-ttu-id="0b136-111">![Lagerüberlauflevel](media/supplyplanning_2_overflow1_new.png "Lagerüberlauflevel")</span><span class="sxs-lookup"><span data-stu-id="0b136-111">![Inventory overflow level](media/supplyplanning_2_overflow1_new.png "Inventory overflow level")</span></span>  

##  <a name="calculating-the-overflow-level"></a><span data-ttu-id="0b136-112">Berechnung des Überlauflevels</span><span class="sxs-lookup"><span data-stu-id="0b136-112">Calculating the Overflow Level</span></span>  
<span data-ttu-id="0b136-113">Das Überlauflevel wird auf verschiedene Arten abhängig vom Planungssetup berechnet.</span><span class="sxs-lookup"><span data-stu-id="0b136-113">The overflow level is calculated in different ways depending on planning setup.</span></span>  

### <a name="maximum-qty-reordering-policy"></a><span data-ttu-id="0b136-114">Auffüllen auf Maximalbestand. Wiederbeschaffungsverfahren</span><span class="sxs-lookup"><span data-stu-id="0b136-114">Maximum Qty. reordering policy</span></span>  
<span data-ttu-id="0b136-115">Überlauflevel = Maximalbestand</span><span class="sxs-lookup"><span data-stu-id="0b136-115">Overflow level = Maximum Inventory</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0b136-116">Wenn eine Auftragsmindestmenge existiert, wird sie wie folgt hinzugefügt: Überlauflevel-= Maximalbestand-+ Auftragsmindestmenge.</span><span class="sxs-lookup"><span data-stu-id="0b136-116">If a minimum order quantity exists, then it will be added as follows: Overflow level = Maximum Inventory + Minimum Order Quantity.</span></span>  

### <a name="fixed-reorder-qty-reordering-policy"></a><span data-ttu-id="0b136-117">Nachbestellungsrichtlinie Feste Bestellmenge</span><span class="sxs-lookup"><span data-stu-id="0b136-117">Fixed Reorder Qty. reordering policy</span></span>  
<span data-ttu-id="0b136-118">Überlauflevel = Bestellmenge + Minimalbestand</span><span class="sxs-lookup"><span data-stu-id="0b136-118">Overflow level = Reorder Quantity + Reorder Point</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0b136-119">Wenn die Mindestauftragsgröße höher als der Minimalbestand ist, dann werden folgende Ersetzungen vorgenommen: Überlauflevel-= Bestellmenge + Mindestauftragsgröße</span><span class="sxs-lookup"><span data-stu-id="0b136-119">If the minimum order quantity is higher than the reorder point, then it will replace as follows: Overflow Level = Reorder Quantity + Minimum Order Quantity</span></span>  

### <a name="order-multiple"></a><span data-ttu-id="0b136-120">Losgrößenrundungsfaktor</span><span class="sxs-lookup"><span data-stu-id="0b136-120">Order Multiple</span></span>  
<span data-ttu-id="0b136-121">Wenn ein Auftragsvielfaches vorhanden ist, reguliert dieses den Überlauflevel für die Wiederbeschaffungsverfahren Höchstmenge und Feste Nachbestellmenge.</span><span class="sxs-lookup"><span data-stu-id="0b136-121">If an order multiple exists, then it will adjust the overflow level for both Maximum Qty. and Fixed Reorder Qty. reordering policies.</span></span>  

##  <a name="creating-the-planning-line-with-overflow-warning"></a><span data-ttu-id="0b136-122">Erstellen der Planungszeile mit Überlaufwarnmeldung</span><span class="sxs-lookup"><span data-stu-id="0b136-122">Creating the Planning Line with Overflow Warning</span></span>  
<span data-ttu-id="0b136-123">Wenn eine vorhandene Lieferung dazu führt, dass der voraussichtliche Lagerbestand höher ist, als das Überlauflevel am Ende eines Zeitrahmens höher, wird eine Planungszeile erstellt.</span><span class="sxs-lookup"><span data-stu-id="0b136-123">When an existing supply causes the projected inventory to be higher than the overflow level at the end of a time bucket, a planning line is created.</span></span> <span data-ttu-id="0b136-124">Um vor einem möglichen überflüssigen Vorrat zu warnen, hat die Planungszeile eine Warnmeldung, das Feld **Ereignismeldung akzeptieren** ist nicht aktiviert, und die Ereignismeldung ist entweder "Abbrechen" oder "Menge ändern".</span><span class="sxs-lookup"><span data-stu-id="0b136-124">To warn about the potential superfluous supply, the planning line has a warning message, the **Accept Action Message** field is not selected, and the action message is either Cancel or Change Qty.</span></span>  

### <a name="calculating-the-planning-line-quantity"></a><span data-ttu-id="0b136-125">Berechnen der Planungszeilenmenge</span><span class="sxs-lookup"><span data-stu-id="0b136-125">Calculating the Planning Line Quantity</span></span>  
<span data-ttu-id="0b136-126">Planungszeilen-Menge = Netzstrom-Menge - (voraussichtlicher Lagerbestand - Überlauflevel)</span><span class="sxs-lookup"><span data-stu-id="0b136-126">Planning Line Quantity = Current Supply Quantity – (Projected Inventory – Overflow Level)</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0b136-127">Wie bei allen Hinweiszeilen werden alle Max./Min.-Auftragsmengen oder Auftragsvielfache ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0b136-127">As with all warning lines, any maximum/minimum order quantity or order multiple will be ignored.</span></span>  

### <a name="defining-the-action-message-type"></a><span data-ttu-id="0b136-128">Definieren des Aktionsmeldungstyps</span><span class="sxs-lookup"><span data-stu-id="0b136-128">Defining the Action Message Type</span></span>  

-   <span data-ttu-id="0b136-129">Wenn die Planungszeilenmenge höher als 0 ist, ist die Aktionsmeldung „Menge ändern“.</span><span class="sxs-lookup"><span data-stu-id="0b136-129">If the planning line quantity is higher than 0, then the action message is Change Qty.</span></span>  
-   <span data-ttu-id="0b136-130">Wenn die Planungszeilenmenge gleich oder niedriger als 0 ist, ist die Aktionsmeldung „Stornieren“.</span><span class="sxs-lookup"><span data-stu-id="0b136-130">If the planning line quantity is equal to or lower than 0, then the action message is Cancel</span></span>  

### <a name="composing-the-warning-message"></a><span data-ttu-id="0b136-131">Verfassen der Warnmeldung</span><span class="sxs-lookup"><span data-stu-id="0b136-131">Composing the Warning Message</span></span>  
<span data-ttu-id="0b136-132">Im Falle eines Überlaufs zeigt die Seite  **Planungselement ohne Nachverfolgung** eine Warnmeldung mit den folgenden Informationen an:</span><span class="sxs-lookup"><span data-stu-id="0b136-132">In case of overflow, the **Untracked Planning Elements** page displays a warning message with the following information:</span></span>  

-   <span data-ttu-id="0b136-133">Der voraussichtliche Lagerbestand, der die Warnung ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="0b136-133">The projected inventory level that triggered the warning</span></span>  
-   <span data-ttu-id="0b136-134">Der berechnete Überlauflevel</span><span class="sxs-lookup"><span data-stu-id="0b136-134">The calculated overflow level</span></span>  
-   <span data-ttu-id="0b136-135">Das Fälligkeitsdatum des Vorratsereignisses.</span><span class="sxs-lookup"><span data-stu-id="0b136-135">The due date of the supply event.</span></span>  

<span data-ttu-id="0b136-136">Beispiel: "Der voraussichtliche Lagerbestand 120 übersteigt das Überlauflevel 60 am 28.01.11"</span><span class="sxs-lookup"><span data-stu-id="0b136-136">Example: “The projected inventory 120 is higher than the overflow level 60 on 28-01-11”</span></span>  

## <a name="scenario"></a><span data-ttu-id="0b136-137">Szenario</span><span class="sxs-lookup"><span data-stu-id="0b136-137">Scenario</span></span>  
<span data-ttu-id="0b136-138">In diesem Szenario ändert ein Debitor einen Verkaufsauftrag von 70 zu 40 Stück zwischen zwei Planungen.</span><span class="sxs-lookup"><span data-stu-id="0b136-138">In this scenario, a customer changes a sales order from 70 to 40 pieces between two planning runs.</span></span> <span data-ttu-id="0b136-139">Die Überlauffunktion reduziert den Einkauf, der für die anfängliche Verkaufsmenge vorgeschlagen worden war.</span><span class="sxs-lookup"><span data-stu-id="0b136-139">The overflow feature sets in to reduce the purchase that was suggested for the initial sales quantity.</span></span>  

### <a name="item-setup"></a><span data-ttu-id="0b136-140">Artikeleinrichtung</span><span class="sxs-lookup"><span data-stu-id="0b136-140">Item setup</span></span>  

|<span data-ttu-id="0b136-141">Wiederbeschaffungsverfahren</span><span class="sxs-lookup"><span data-stu-id="0b136-141">Reordering Policy</span></span>|<span data-ttu-id="0b136-142">Auffüllen auf Maximalbestand</span><span class="sxs-lookup"><span data-stu-id="0b136-142">Maximum Qty.</span></span>|  
|-----------------------|------------------|  
|<span data-ttu-id="0b136-143">Maximale Losgröße</span><span class="sxs-lookup"><span data-stu-id="0b136-143">Maximum Order Quantity</span></span>|<span data-ttu-id="0b136-144">100</span><span class="sxs-lookup"><span data-stu-id="0b136-144">100</span></span>|  
|<span data-ttu-id="0b136-145">Minimalbestand</span><span class="sxs-lookup"><span data-stu-id="0b136-145">Reorder Point</span></span>|<span data-ttu-id="0b136-146">50</span><span class="sxs-lookup"><span data-stu-id="0b136-146">50</span></span>|  
|<span data-ttu-id="0b136-147">Lagerbest</span><span class="sxs-lookup"><span data-stu-id="0b136-147">Inventory</span></span>|<span data-ttu-id="0b136-148">80</span><span class="sxs-lookup"><span data-stu-id="0b136-148">80</span></span>|  

### <a name="situation-before-sales-decrease"></a><span data-ttu-id="0b136-149">Situation vor Vertriebsabgang</span><span class="sxs-lookup"><span data-stu-id="0b136-149">Situation before sales decrease</span></span>  

|<span data-ttu-id="0b136-150">Ereignis</span><span class="sxs-lookup"><span data-stu-id="0b136-150">Event</span></span>|<span data-ttu-id="0b136-151">"Menge ändern"</span><span class="sxs-lookup"><span data-stu-id="0b136-151">Change Qty.</span></span>|<span data-ttu-id="0b136-152">Voraussichtlicher Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="0b136-152">Projected Inventory</span></span>|  
|-----------|-----------------|-------------------------|  
|<span data-ttu-id="0b136-153">Tag eins</span><span class="sxs-lookup"><span data-stu-id="0b136-153">Day one</span></span>|<span data-ttu-id="0b136-154">Keine</span><span class="sxs-lookup"><span data-stu-id="0b136-154">None</span></span>|<span data-ttu-id="0b136-155">80</span><span class="sxs-lookup"><span data-stu-id="0b136-155">80</span></span>|  
|<span data-ttu-id="0b136-156">Verkauf</span><span class="sxs-lookup"><span data-stu-id="0b136-156">Sale</span></span>|<span data-ttu-id="0b136-157">-70</span><span class="sxs-lookup"><span data-stu-id="0b136-157">-70</span></span>|<span data-ttu-id="0b136-158">10</span><span class="sxs-lookup"><span data-stu-id="0b136-158">10</span></span>|  
|<span data-ttu-id="0b136-159">Ende des Zeitrahmens</span><span class="sxs-lookup"><span data-stu-id="0b136-159">End of time bucket</span></span>|<span data-ttu-id="0b136-160">Keine</span><span class="sxs-lookup"><span data-stu-id="0b136-160">None</span></span>|<span data-ttu-id="0b136-161">10</span><span class="sxs-lookup"><span data-stu-id="0b136-161">10</span></span>|  
|<span data-ttu-id="0b136-162">Neue Bestellung vorschlagen</span><span class="sxs-lookup"><span data-stu-id="0b136-162">Suggest new purchase order</span></span>|<span data-ttu-id="0b136-163">+90</span><span class="sxs-lookup"><span data-stu-id="0b136-163">+90</span></span>|<span data-ttu-id="0b136-164">100</span><span class="sxs-lookup"><span data-stu-id="0b136-164">100</span></span>|  

### <a name="situation-after-sales-decrease"></a><span data-ttu-id="0b136-165">Situation nach Vertriebsabgang</span><span class="sxs-lookup"><span data-stu-id="0b136-165">Situation after sales decrease</span></span>  

|<span data-ttu-id="0b136-166">Ändern</span><span class="sxs-lookup"><span data-stu-id="0b136-166">Change</span></span>|<span data-ttu-id="0b136-167">"Menge ändern"</span><span class="sxs-lookup"><span data-stu-id="0b136-167">Change Qty.</span></span>|<span data-ttu-id="0b136-168">Voraussichtlicher Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="0b136-168">Projected Inventory</span></span>|  
|------------|-----------------|-------------------------|  
|<span data-ttu-id="0b136-169">Tag eins</span><span class="sxs-lookup"><span data-stu-id="0b136-169">Day one</span></span>|<span data-ttu-id="0b136-170">Keine</span><span class="sxs-lookup"><span data-stu-id="0b136-170">None</span></span>|<span data-ttu-id="0b136-171">80</span><span class="sxs-lookup"><span data-stu-id="0b136-171">80</span></span>|  
|<span data-ttu-id="0b136-172">Verkauf</span><span class="sxs-lookup"><span data-stu-id="0b136-172">Sale</span></span>|<span data-ttu-id="0b136-173">-40</span><span class="sxs-lookup"><span data-stu-id="0b136-173">-40</span></span>|<span data-ttu-id="0b136-174">40</span><span class="sxs-lookup"><span data-stu-id="0b136-174">40</span></span>|  
|<span data-ttu-id="0b136-175">Einkauf</span><span class="sxs-lookup"><span data-stu-id="0b136-175">Purchase</span></span>|<span data-ttu-id="0b136-176">+90</span><span class="sxs-lookup"><span data-stu-id="0b136-176">+90</span></span>|<span data-ttu-id="0b136-177">130</span><span class="sxs-lookup"><span data-stu-id="0b136-177">130</span></span>|  
|<span data-ttu-id="0b136-178">Ende des Zeitrahmens</span><span class="sxs-lookup"><span data-stu-id="0b136-178">End of time bucket</span></span>|<span data-ttu-id="0b136-179">Keine</span><span class="sxs-lookup"><span data-stu-id="0b136-179">None</span></span>|<span data-ttu-id="0b136-180">130</span><span class="sxs-lookup"><span data-stu-id="0b136-180">130</span></span>|  
|<span data-ttu-id="0b136-181">Vorschlagen, den Einkauf zu vermindern</span><span class="sxs-lookup"><span data-stu-id="0b136-181">Suggest to decrease purchase</span></span><br /><br /> <span data-ttu-id="0b136-182">Auftrag von 90 bis 60</span><span class="sxs-lookup"><span data-stu-id="0b136-182">order from 90 to 60</span></span>|<span data-ttu-id="0b136-183">-30</span><span class="sxs-lookup"><span data-stu-id="0b136-183">-30</span></span>|<span data-ttu-id="0b136-184">100</span><span class="sxs-lookup"><span data-stu-id="0b136-184">100</span></span>|  

### <a name="resulting-planning-lines"></a><span data-ttu-id="0b136-185">Planzeilen erstellen</span><span class="sxs-lookup"><span data-stu-id="0b136-185">Resulting Planning Lines</span></span>  
 <span data-ttu-id="0b136-186">Eine Planungszeile (Warnen) wird erstellt, um den Einkauf mit 30 von 90 auf 60 zu verringern, um den voraussichtlichen Lagerstatus auf 100 entsprechend dem Überlauflevel festzuhalten.</span><span class="sxs-lookup"><span data-stu-id="0b136-186">One planning line (warning) is created to reduce the purchase with 30 from 90 to 60 to keep the projected inventory on 100 according to the overflow level.</span></span>  

<span data-ttu-id="0b136-187">![Planung entsprechender Überlauflevel](media/nav_app_supply_planning_2_overflow2.png "Planung entsprechender Überlauflevel")</span><span class="sxs-lookup"><span data-stu-id="0b136-187">![Plan according to overflow level](media/nav_app_supply_planning_2_overflow2.png "Plan according to overflow level")</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0b136-188">Ohne die Sammelfunktion werden keine Warnmeldungen erstellt, wenn der voraussichtliche Lagerbestand über Maximalbestand ist.</span><span class="sxs-lookup"><span data-stu-id="0b136-188">Without the Overflow feature, no warning is created if the projected inventory level is above maximum inventory.</span></span> <span data-ttu-id="0b136-189">Dies kann einen überflüssigen Vorrat von 30 verursachen.</span><span class="sxs-lookup"><span data-stu-id="0b136-189">This could cause a superfluous supply of 30.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0b136-190">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b136-190">See Also</span></span>  
<span data-ttu-id="0b136-191">[Designdetails: Wiederbeschaffungsverfahren](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="0b136-191">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="0b136-192">[Designdetails: Planungsparameter](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="0b136-192">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="0b136-193">[Designdetails: Umgang mit Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="0b136-193">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="0b136-194">Designdetails: Vorratsplanung</span><span class="sxs-lookup"><span data-stu-id="0b136-194">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
