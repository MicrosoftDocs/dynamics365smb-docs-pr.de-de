---
title: "Designdetails -Priorisieren von Aufträgen | Microsoft Docs"
description: "Lesen, wie priorisiert wird, um Bedarf und Versorgungsbedarf zu erfüllen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, priority, prioritize, order, sku, demand, supply
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7af645f5a9dd7f34619d05cb2d4f0f7f8ad1921d
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-prioritizing-orders"></a><span data-ttu-id="5c33b-103">Designdetails: Priorisieren von Aufträgen</span><span class="sxs-lookup"><span data-stu-id="5c33b-103">Design Details: Prioritizing Orders</span></span>
<span data-ttu-id="5c33b-104">In bestimmten Lagerhaltungsdaten zeigt das angeforderte oder verfügbare Datum die höchste Priorität an; mit dem Bedarf des heutigen Tages soll vor dem Bedarf der nächsten Woche verfahren werden.</span><span class="sxs-lookup"><span data-stu-id="5c33b-104">Within a given SKU, the requested or available date represents the highest priority; the demand of today should be dealt with before the demand of next week.</span></span> <span data-ttu-id="5c33b-105">Zusätzlich zu dieser allgemeinen Priorität schlägt das Planungssystem jedoch auch vor, welche Art von Bedarf vor anderen Bedarfen erfüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c33b-105">But in addition to this overall priority, the planning system will also suggest which type of demand should be fulfilled before fulfilling another demand.</span></span> <span data-ttu-id="5c33b-106">Ebenso empfiehlt es eine auszugleichende Versorgungsquelle vor anderen Versorgungsquellen.</span><span class="sxs-lookup"><span data-stu-id="5c33b-106">Likewise, it will suggest what source of supply should be applied before applying other sources of supply.</span></span> <span data-ttu-id="5c33b-107">Dieses wird gemäß Auftragsprioritäten durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="5c33b-107">This is done according to order priorities.</span></span>  
  
<span data-ttu-id="5c33b-108">Geladener Bedarf und Vorrat tragen zu einem Profil für den voraussichtlichen Lagerbestand entsprechend den folgenden Prioritäten bei:</span><span class="sxs-lookup"><span data-stu-id="5c33b-108">Loaded demand and supply contribute to a profile for the projected inventory according to the following priorities:</span></span>  
  
## <a name="priorities-on-the-demand-side"></a><span data-ttu-id="5c33b-109">Prioritäten der Bedarfs-Seite</span><span class="sxs-lookup"><span data-stu-id="5c33b-109">Priorities on the Demand Side</span></span>  
1. <span data-ttu-id="5c33b-110">Bereits geliefert: Artikelposten</span><span class="sxs-lookup"><span data-stu-id="5c33b-110">Already shipped: Item Ledger Entry</span></span>  
2. <span data-ttu-id="5c33b-111">Einkaufsreklamation</span><span class="sxs-lookup"><span data-stu-id="5c33b-111">Purchase Return Order</span></span>  
3. <span data-ttu-id="5c33b-112">Verkaufsauftrag</span><span class="sxs-lookup"><span data-stu-id="5c33b-112">Sales Order</span></span>  
4. <span data-ttu-id="5c33b-113">Serviceauftrag</span><span class="sxs-lookup"><span data-stu-id="5c33b-113">Service Order</span></span>  
5. <span data-ttu-id="5c33b-114">Bedarf an Produktionskomponenten</span><span class="sxs-lookup"><span data-stu-id="5c33b-114">Production Component Need</span></span>  
6. <span data-ttu-id="5c33b-115">Montageauftragszeile</span><span class="sxs-lookup"><span data-stu-id="5c33b-115">Assembly Order Line</span></span>  
7. <span data-ttu-id="5c33b-116">Ausgehender Umlagerungsauftrag.</span><span class="sxs-lookup"><span data-stu-id="5c33b-116">Outbound Transfer Order</span></span>  
8. <span data-ttu-id="5c33b-117">Rahmenauftrag (der nicht bereits durch zugehörige Verkaufsaufträge verbraucht wurde)</span><span class="sxs-lookup"><span data-stu-id="5c33b-117">Blanket Order (that has not already been consumed by related sales orders)</span></span>  
9. <span data-ttu-id="5c33b-118">Planung (die nicht bereits durch andere Verkaufsaufträge verbraucht wurde)</span><span class="sxs-lookup"><span data-stu-id="5c33b-118">Forecast (that has not already been consumed by other sales orders)</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="5c33b-119">Einkaufsreklamationen sind normalerweise nicht Teil der Absatzplanung; sie sollten stets in der Charge reserviert sein, die zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5c33b-119">Purchase returns are usually not involved in supply planning; they should always be reserved from the lot that is going to be returned.</span></span> <span data-ttu-id="5c33b-120">Falls nicht reserviert, spielen Einkaufsreklamationen eine Rolle bei der Verfügbarkeit und werden hoch priorisiert, um zu vermeiden, dass das Planungssystem einen Beschaffungsauftrag vorschlägt, nur um eine Einkaufsreklamation zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="5c33b-120">If not reserved, purchase returns play a role in the availability and are highly prioritized to avoid that the planning system suggests a supply order just to serve a purchase return.</span></span>  
  
## <a name="priorities-on-the-supply-side"></a><span data-ttu-id="5c33b-121">Prioritäten der Bedarfs-Seite</span><span class="sxs-lookup"><span data-stu-id="5c33b-121">Priorities on the Supply Side</span></span>  
1. <span data-ttu-id="5c33b-122">Bereits im Bestand: Artikelposten (Planungs-Flexibilität = keine)</span><span class="sxs-lookup"><span data-stu-id="5c33b-122">Already in inventory: Item Ledger Entry (Planning Flexibility = None)</span></span>  
2. <span data-ttu-id="5c33b-123">Verkaufsreklamation (Planungs-Flexibilität = keine)</span><span class="sxs-lookup"><span data-stu-id="5c33b-123">Sales Return Order (Planning Flexibility = None)</span></span>  
3. <span data-ttu-id="5c33b-124">Ausgehende Umlagerungsaufträge</span><span class="sxs-lookup"><span data-stu-id="5c33b-124">Inbound Transfer Order</span></span>  
4. <span data-ttu-id="5c33b-125">Fertigungsauftrag</span><span class="sxs-lookup"><span data-stu-id="5c33b-125">Production Order</span></span>  
5. <span data-ttu-id="5c33b-126">Montageauftrag</span><span class="sxs-lookup"><span data-stu-id="5c33b-126">Assembly Order</span></span>  
6. <span data-ttu-id="5c33b-127">Bestellung</span><span class="sxs-lookup"><span data-stu-id="5c33b-127">Purchase Order</span></span>  
  
## <a name="priority-related-to-the-state-of-demand-and-supply"></a><span data-ttu-id="5c33b-128">Priorität in Bezug auf Status des Bedarfs und des Angebotes</span><span class="sxs-lookup"><span data-stu-id="5c33b-128">Priority Related to the State of Demand and Supply</span></span>  
<span data-ttu-id="5c33b-129">Abgesehen von den Prioritäten, die von dem Typ des Bedarfs oder des Vorrats vorgegeben werden, definiert der aktuelle Zustand der Aufträge im Ausführungsprozess ebenfalls eine Priorität.</span><span class="sxs-lookup"><span data-stu-id="5c33b-129">Apart from priorities given by the type of demand and supply, the present state of the orders in the execution process also defines a priority.</span></span> <span data-ttu-id="5c33b-130">Beispielsweise haben Lageraktivitäten Auswirkungen, und der Status von Verkaufs-, Einkaufs-, Umlagerungs-, Montage- und Fertigunksaufträgen wird berücksichtigt:</span><span class="sxs-lookup"><span data-stu-id="5c33b-130">For example, warehouse activities have an impact, and the status of sales, purchase, transfer, assembly, and production orders is taken into account:</span></span>  
  
1. <span data-ttu-id="5c33b-131">Teilweise bearbeitet (Planungs-Flexibilität = Nein)</span><span class="sxs-lookup"><span data-stu-id="5c33b-131">Partly handled (Planning Flexibility = None)</span></span>  
2. <span data-ttu-id="5c33b-132">Bereits in Bearbeitung im Lager (Planungs-Flexibilität = keine)</span><span class="sxs-lookup"><span data-stu-id="5c33b-132">Already in process in the warehouse (Planning Flexibility = None)</span></span>  
3. <span data-ttu-id="5c33b-133">Freigegeben - alle Auftragsarten (Planungs-Flexibilität = unbegrenzt)</span><span class="sxs-lookup"><span data-stu-id="5c33b-133">Released – all order types (Planning Flexibility = Unlimited)</span></span>  
4. <span data-ttu-id="5c33b-134">Fest geplanter Fertigungsauftrag (Planungs-Flexibilität = unbegrenzt)</span><span class="sxs-lookup"><span data-stu-id="5c33b-134">Firm Planned Production Order (Planning Flexibility = Unlimited)</span></span>  
5. <span data-ttu-id="5c33b-135">Geplant/Offen – alle Ordnertypen (Planungs-Flexibilität = unbegrenzt)</span><span class="sxs-lookup"><span data-stu-id="5c33b-135">Planned/Open – all order types (Planning Flexibility = Unlimited)</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5c33b-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c33b-136">See Also</span></span>  
<span data-ttu-id="5c33b-137">[Designdetails: Ausgleich von Bedarf und Vorrat](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="5c33b-137">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="5c33b-138">[Designdetails: Zentrale Konzepte des Planungssystems](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="5c33b-138">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="5c33b-139">Designdetails: Vorratsplanung</span><span class="sxs-lookup"><span data-stu-id="5c33b-139">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
