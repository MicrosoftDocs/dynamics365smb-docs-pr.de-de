---
title: 'Designdetails: Umgang mit voraussichtlichem negativem Lagerbestand | Microsoft Docs'
description: "Der Minimalbestand drückt den voraussichtlichen Bedarf während der Beschaffungszeit des Artikels aus. Wenn der Minimalbestand überschritten wird, ist es an der Zeit, mehr zu bestellen. Der voraussichtliche Lagerbestand muss jedoch groß genug sein, um den Bedarf zu decken, bis der neue Auftrag eingegangen ist. Unterdessen gleicht der Sicherheitsbestand Schwankungen im Bedarf bis zu einem anvisierten Servicelevel aus."
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 3436e2a00858a1dbfcbb0a44cb9db32bd7665593
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-handling-projected-negative-inventory"></a><span data-ttu-id="4220a-106">Designdetails: Umgang mit voraussichtlichem negativem Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="4220a-106">Design Details: Handling Projected Negative Inventory</span></span>
<span data-ttu-id="4220a-107">Der Minimalbestand drückt den voraussichtlichen Bedarf während der Beschaffungszeit des Artikels aus.</span><span class="sxs-lookup"><span data-stu-id="4220a-107">The reorder point expresses the anticipated demand during the lead time of the item.</span></span> <span data-ttu-id="4220a-108">Wenn der Minimalbestand überschritten wird, ist es an der Zeit, mehr zu bestellen.</span><span class="sxs-lookup"><span data-stu-id="4220a-108">When the reorder point is passed, it is time to order more.</span></span> <span data-ttu-id="4220a-109">Der voraussichtliche Lagerbestand muss jedoch groß genug sein, um den Bedarf zu decken, bis der neue Auftrag eingegangen ist.</span><span class="sxs-lookup"><span data-stu-id="4220a-109">But the projected inventory must be large enough to cover the demand until the new order is received.</span></span> <span data-ttu-id="4220a-110">Unterdessen gleicht der Sicherheitsbestand Schwankungen im Bedarf bis zu einem anvisierten Servicelevel aus.</span><span class="sxs-lookup"><span data-stu-id="4220a-110">Meanwhile, the safety stock should take care of fluctuations in demand up to a targeted service level.</span></span>  

 <span data-ttu-id="4220a-111">Deshalb betrachtet das Planungssystem es als einen Notfall, wenn ein zukünftiger Bedarf nicht aus dem voraussichtlichen Lagerbestand abgedeckt werden kann, oder anders ausgedrückt: wenn der voraussichtliche Lagerbestand negativ wird.</span><span class="sxs-lookup"><span data-stu-id="4220a-111">Consequently, the planning system considers it an emergency if a future demand cannot be served from the projected inventory, or expressed in another way, that the projected inventory goes negative.</span></span> <span data-ttu-id="4220a-112">Die Anwendung behandelt eine solche Ausnahme, indem es einen neuen Beschaffungsauftrag vorschlägt, um den Teil des Bedarf einzuhalten, der nicht durch Lagerbestand oder anderen Vorrat befriedigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="4220a-112">The system deals with such an exception by suggesting a new supply order to meet the part of the demand that cannot be met by inventory or other supply.</span></span> <span data-ttu-id="4220a-113">Die Auftragsgröße des neuen Beschaffungsauftrags berücksichtigt nicht den Höchstbestand oder die Wiederbeschaffungsmenge, und auch nicht die Auftragsmodifikatoren maximale Auftragsmenge, minimale Auftragsmenge und Auftragsvielfaches.</span><span class="sxs-lookup"><span data-stu-id="4220a-113">The order size of the new supply order will not take the maximum inventory or the reorder quantity into consideration, nor will it take into consideration the order modifiers Maximum Order Quantity, Minimum Order Quantity, and Order Multiple.</span></span> <span data-ttu-id="4220a-114">Stattdessen spiegelt sie den genauen Mangel wider.</span><span class="sxs-lookup"><span data-stu-id="4220a-114">Instead, it will reflect the exact deficiency.</span></span>  

 <span data-ttu-id="4220a-115">Die Planungszeile für diese Art von Beschaffungsauftrag zeigt ein Notwarnsymbol an , und zusätzliche Informationen werden beim Lookup angezeigt, um den Benutzer über die Situation zu informieren..</span><span class="sxs-lookup"><span data-stu-id="4220a-115">The planning line for this type of supply order will display an Emergency warning icon, and additional information will be provided upon lookup to inform the user of the situation.</span></span>  

 <span data-ttu-id="4220a-116">In der folgenden Abbildung zeigt Vorrat D eine Notfallbestellung an, um negativen Bestand auszugleichen.</span><span class="sxs-lookup"><span data-stu-id="4220a-116">In the following illustration, supply D represents an emergency order to adjust for negative inventory.</span></span>  

 ![](media/nav_app_supply_planning_2_negative_inventory.png "NAV_APP_supply_planning_2_negative_inventory")  

1.  <span data-ttu-id="4220a-117">Vorrat **A** anfänglicher voraussichtlicher Lagerbestand, liegt unter Minimalbestand.</span><span class="sxs-lookup"><span data-stu-id="4220a-117">Supply **A**, initial projected inventory, is below reorder point.</span></span>  

2.  <span data-ttu-id="4220a-118">Ein neuer voraus geplanter Vorrat wurde erstellt (**C**).</span><span class="sxs-lookup"><span data-stu-id="4220a-118">A new forward-scheduled supply is created (**C**).</span></span>  

     <span data-ttu-id="4220a-119">(Menge = Maximalbestand - Voraussichtlicher Lagerbestand)</span><span class="sxs-lookup"><span data-stu-id="4220a-119">(Quantity = Maximum Inventory – Projected Inventory Level)</span></span>  

3.  <span data-ttu-id="4220a-120">Vorrat **A** wird durch Bedarf **B** geschlossen, der nicht vollständig abgedeckt wird.</span><span class="sxs-lookup"><span data-stu-id="4220a-120">Supply **A** is closed by demand **B**, which is not fully covered.</span></span>  

     <span data-ttu-id="4220a-121">(Bedarf **B** könnte versuchen, Zubehör C einzuplanen, dies erfolgt jedoch nicht aufgrund des Zeitrahmenkonzepts.)</span><span class="sxs-lookup"><span data-stu-id="4220a-121">(Demand **B** could try to schedule Supply C in but that will not happen according to the time-bucket concept.)</span></span>  

4.  <span data-ttu-id="4220a-122">Neuer Vorrat (**D**) wird erstellt, um die Restmenge auf Anfordung **B** zu decken.</span><span class="sxs-lookup"><span data-stu-id="4220a-122">New supply (**D**) is created to cover the remaining quantity on Demand **B**.</span></span>  

5.  <span data-ttu-id="4220a-123">Bedarf **B** ist geschlossen (eine Erinnerung für den voraussichtlichen Lagerbestand wird erstellt).</span><span class="sxs-lookup"><span data-stu-id="4220a-123">Demand **B** is closed (creating a reminder to the projected inventory).</span></span>  

6.  <span data-ttu-id="4220a-124">Das neue Vorrat **D** wird geschlossen.</span><span class="sxs-lookup"><span data-stu-id="4220a-124">The new supply **D** is closed.</span></span>  

7.  <span data-ttu-id="4220a-125">Voraussichtlicher Lagerbestand wird geprüft; Minimalbestand wurde nicht überschritten.</span><span class="sxs-lookup"><span data-stu-id="4220a-125">Projected Inventory is checked; reorder point has not been crossed.</span></span>  

8.  <span data-ttu-id="4220a-126">Vorrat **C** ist geschlossen (kein Bedarf mehr vorhanden).</span><span class="sxs-lookup"><span data-stu-id="4220a-126">Supply **C** is closed (no more demand exists).</span></span>  

9. <span data-ttu-id="4220a-127">Abschließende Prüfung: Keine ausstehenden Erinnerungen auf Bestandsebene sind vorhanden.</span><span class="sxs-lookup"><span data-stu-id="4220a-127">Final check: No outstanding inventory level reminders exist.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="4220a-128">Schritt 4 zeigt, wie das System in Versionen vor Microsoft Dynamics NAV 2009 SP1 reagiert.</span><span class="sxs-lookup"><span data-stu-id="4220a-128">Step 4 reflects how the system reacts in versions earlier than Microsoft Dynamics NAV 2009 SP1.</span></span>  

 <span data-ttu-id="4220a-129">Damit ist die Beschreibung der zentralen Prinzipien in Bezug auf Bestandsplanung basierend auf Wiederbeschaffungsverfahren abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="4220a-129">This concludes the description of central principles relating to inventory planning based on reordering policies.</span></span> <span data-ttu-id="4220a-130">Im nächsten Abschnitt werden die Eigenschaften der vier unterstützten Wiederbeschaffungsrichtlinien beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4220a-130">The following section describes the characteristics of the four supported reordering policies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4220a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4220a-131">See Also</span></span>  
 <span data-ttu-id="4220a-132">[Designdetails: Wiederbeschaffungsverfahren](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="4220a-132">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="4220a-133">[Designdetails: Planungsparameter](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="4220a-133">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="4220a-134">[Designdetails: Umgang mit Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="4220a-134">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="4220a-135">Designdetails: Vorratsplanung</span><span class="sxs-lookup"><span data-stu-id="4220a-135">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

