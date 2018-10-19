---
title: 'Designdetails: Umgang mit voraussichtlichem negativem Lagerbestand | Microsoft Docs'
description: "Der Minimalbestand drückt den voraussichtlichen Bedarf während der Beschaffungszeit des Artikels aus. Wenn der Minimalbestand überschritten wird, ist es an der Zeit, mehr zu bestellen. Der voraussichtliche Lagerbestand muss jedoch groß genug sein, um den Bedarf zu decken, bis der neue Auftrag eingegangen ist. Unterdessen gleicht der Sicherheitsbestand Schwankungen im Bedarf bis zu einem anvisierten Servicelevel aus."
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
ms.openlocfilehash: 25a2017fd91f09a9d7725c68ffaa0df48a041294
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-handling-projected-negative-inventory"></a><span data-ttu-id="be35a-106">Designdetails: Umgang mit voraussichtlichem negativem Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="be35a-106">Design Details: Handling Projected Negative Inventory</span></span>
<span data-ttu-id="be35a-107">Der Minimalbestand drückt den voraussichtlichen Bedarf während der Beschaffungszeit des Artikels aus.</span><span class="sxs-lookup"><span data-stu-id="be35a-107">The reorder point expresses the anticipated demand during the lead time of the item.</span></span> <span data-ttu-id="be35a-108">Wenn der Minimalbestand überschritten wird, ist es an der Zeit, mehr zu bestellen.</span><span class="sxs-lookup"><span data-stu-id="be35a-108">When the reorder point is passed, it is time to order more.</span></span> <span data-ttu-id="be35a-109">Der voraussichtliche Lagerbestand muss jedoch groß genug sein, um den Bedarf zu decken, bis der neue Auftrag eingegangen ist.</span><span class="sxs-lookup"><span data-stu-id="be35a-109">But the projected inventory must be large enough to cover the demand until the new order is received.</span></span> <span data-ttu-id="be35a-110">Unterdessen gleicht der Sicherheitsbestand Schwankungen im Bedarf bis zu einem anvisierten Servicelevel aus.</span><span class="sxs-lookup"><span data-stu-id="be35a-110">Meanwhile, the safety stock should take care of fluctuations in demand up to a targeted service level.</span></span>  

 <span data-ttu-id="be35a-111">Deshalb betrachtet das Planungssystem es als einen Notfall, wenn ein zukünftiger Bedarf nicht aus dem voraussichtlichen Lagerbestand abgedeckt werden kann, oder anders ausgedrückt: wenn der voraussichtliche Lagerbestand negativ wird.</span><span class="sxs-lookup"><span data-stu-id="be35a-111">Consequently, the planning system considers it an emergency if a future demand cannot be served from the projected inventory, or expressed in another way, that the projected inventory goes negative.</span></span> <span data-ttu-id="be35a-112">Die Anwendung behandelt eine solche Ausnahme, indem es einen neuen Beschaffungsauftrag vorschlägt, um den Teil des Bedarf einzuhalten, der nicht durch Lagerbestand oder anderen Vorrat befriedigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="be35a-112">The system deals with such an exception by suggesting a new supply order to meet the part of the demand that cannot be met by inventory or other supply.</span></span> <span data-ttu-id="be35a-113">Die Auftragsgröße des neuen Beschaffungsauftrags berücksichtigt nicht den Höchstbestand oder die Wiederbeschaffungsmenge, und auch nicht die Auftragsmodifikatoren maximale Auftragsmenge, minimale Auftragsmenge und Auftragsvielfaches.</span><span class="sxs-lookup"><span data-stu-id="be35a-113">The order size of the new supply order will not take the maximum inventory or the reorder quantity into consideration, nor will it take into consideration the order modifiers Maximum Order Quantity, Minimum Order Quantity, and Order Multiple.</span></span> <span data-ttu-id="be35a-114">Stattdessen spiegelt sie den genauen Mangel wider.</span><span class="sxs-lookup"><span data-stu-id="be35a-114">Instead, it will reflect the exact deficiency.</span></span>  

 <span data-ttu-id="be35a-115">Die Planungszeile für diese Art von Beschaffungsauftrag zeigt ein Notwarnsymbol an , und zusätzliche Informationen werden beim Lookup angezeigt, um den Benutzer über die Situation zu informieren..</span><span class="sxs-lookup"><span data-stu-id="be35a-115">The planning line for this type of supply order will display an Emergency warning icon, and additional information will be provided upon lookup to inform the user of the situation.</span></span>  

 <span data-ttu-id="be35a-116">In der folgenden Abbildung zeigt Vorrat D eine Notfallbestellung an, um negativen Bestand auszugleichen.</span><span class="sxs-lookup"><span data-stu-id="be35a-116">In the following illustration, supply D represents an emergency order to adjust for negative inventory.</span></span>  

 <span data-ttu-id="be35a-117">![Notfallplanungsvorschlag, verhindern von negativem Lagerbestand](media/nav_app_supply_planning_2_negative_inventory.png "Notfallplanungsvorschlag, verhindern von negativem Lagerbestand")</span><span class="sxs-lookup"><span data-stu-id="be35a-117">![Emergency planning suggestion to avoid negative inventory](media/nav_app_supply_planning_2_negative_inventory.png "Emergency planning suggestion to avoid negative inventory")</span></span>  

1.  <span data-ttu-id="be35a-118">Vorrat **A** anfänglicher voraussichtlicher Lagerbestand, liegt unter Minimalbestand.</span><span class="sxs-lookup"><span data-stu-id="be35a-118">Supply **A**, initial projected inventory, is below reorder point.</span></span>  
2.  <span data-ttu-id="be35a-119">Ein neuer voraus geplanter Vorrat wurde erstellt (**C**).</span><span class="sxs-lookup"><span data-stu-id="be35a-119">A new forward-scheduled supply is created (**C**).</span></span>  

     <span data-ttu-id="be35a-120">(Menge = Maximalbestand - Voraussichtlicher Lagerbestand)</span><span class="sxs-lookup"><span data-stu-id="be35a-120">(Quantity = Maximum Inventory – Projected Inventory Level)</span></span>  
3.  <span data-ttu-id="be35a-121">Vorrat **A** wird durch Bedarf **B** geschlossen, der nicht vollständig abgedeckt wird.</span><span class="sxs-lookup"><span data-stu-id="be35a-121">Supply **A** is closed by demand **B**, which is not fully covered.</span></span>  

     <span data-ttu-id="be35a-122">(Bedarf **B** könnte versuchen, Zubehör C einzuplanen, dies erfolgt jedoch nicht aufgrund des Zeitrahmenkonzepts.)</span><span class="sxs-lookup"><span data-stu-id="be35a-122">(Demand **B** could try to schedule Supply C in but that will not happen according to the time-bucket concept.)</span></span>  
4.  <span data-ttu-id="be35a-123">Neuer Vorrat (**D**) wird erstellt, um die Restmenge auf Anfordung **B** zu decken.</span><span class="sxs-lookup"><span data-stu-id="be35a-123">New supply (**D**) is created to cover the remaining quantity on Demand **B**.</span></span>  
5.  <span data-ttu-id="be35a-124">Bedarf **B** ist geschlossen (eine Erinnerung für den voraussichtlichen Lagerbestand wird erstellt).</span><span class="sxs-lookup"><span data-stu-id="be35a-124">Demand **B** is closed (creating a reminder to the projected inventory).</span></span>  
6.  <span data-ttu-id="be35a-125">Das neue Vorrat **D** wird geschlossen.</span><span class="sxs-lookup"><span data-stu-id="be35a-125">The new supply **D** is closed.</span></span>  
7.  <span data-ttu-id="be35a-126">Voraussichtlicher Lagerbestand wird geprüft; Minimalbestand wurde nicht überschritten.</span><span class="sxs-lookup"><span data-stu-id="be35a-126">Projected Inventory is checked; reorder point has not been crossed.</span></span>  
8.  <span data-ttu-id="be35a-127">Vorrat **C** ist geschlossen (kein Bedarf mehr vorhanden).</span><span class="sxs-lookup"><span data-stu-id="be35a-127">Supply **C** is closed (no more demand exists).</span></span>  
9. <span data-ttu-id="be35a-128">Abschließende Prüfung: Keine ausstehenden Erinnerungen auf Bestandsebene sind vorhanden.</span><span class="sxs-lookup"><span data-stu-id="be35a-128">Final check: No outstanding inventory level reminders exist.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="be35a-129">Schritt 4 zeigt, wie das System in Versionen vor Microsoft Dynamics NAV 2009 SP1 reagiert.</span><span class="sxs-lookup"><span data-stu-id="be35a-129">Step 4 reflects how the system reacts in versions earlier than Microsoft Dynamics NAV 2009 SP1.</span></span>  

 <span data-ttu-id="be35a-130">Damit ist die Beschreibung der zentralen Prinzipien in Bezug auf Bestandsplanung basierend auf Wiederbeschaffungsverfahren abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="be35a-130">This concludes the description of central principles relating to inventory planning based on reordering policies.</span></span> <span data-ttu-id="be35a-131">Im nächsten Abschnitt werden die Eigenschaften der vier unterstützten Wiederbeschaffungsrichtlinien beschrieben.</span><span class="sxs-lookup"><span data-stu-id="be35a-131">The following section describes the characteristics of the four supported reordering policies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="be35a-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be35a-132">See Also</span></span>  
 <span data-ttu-id="be35a-133">[Designdetails: Wiederbeschaffungsverfahren](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="be35a-133">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="be35a-134">[Designdetails: Planungsparameter](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="be35a-134">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="be35a-135">[Designdetails: Umgang mit Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="be35a-135">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="be35a-136">Designdetails: Vorratsplanung</span><span class="sxs-lookup"><span data-stu-id="be35a-136">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

