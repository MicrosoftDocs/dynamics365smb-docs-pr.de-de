---
title: 'Designdetails: Die Rolle des Minimalbestands | Microsoft Docs'
description: "Dieses Thema hebt die Wichtigkeit der Einstellung Minimalbed hervor, damit Sie wissen, wann Sie den Bestand erneuern müssen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: desigh, reorder, demand, supply
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5b5e3cec4bc5af8188470ea1d711422c0130677e
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-the-role-of-the-reorder-point"></a><span data-ttu-id="9d41b-103">Designdetails: Die Rolle des Minimalbestands</span><span class="sxs-lookup"><span data-stu-id="9d41b-103">Design Details: The Role of the Reorder Point</span></span>
<span data-ttu-id="9d41b-104">Zusätzlich zur allgemeinen Anpassung von Angebot und Nachfrage muss das Planungssystem auch Lagerbestände für die betroffenen Artikel überwachen, um die definierten Wiederbeschaffungsverfahren zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="9d41b-104">In addition to the general balancing of supply and demand, the planning system must also monitor inventory levels for the affected items to respect the defined reordering policies.</span></span>  
  
<span data-ttu-id="9d41b-105">Ein Minimalbestand repräsentiert den Bedarf während der Beschaffungszeit.</span><span class="sxs-lookup"><span data-stu-id="9d41b-105">A reorder point represents demand during lead time.</span></span> <span data-ttu-id="9d41b-106">Wenn die Durchläufe des voraussichtlichen Lagerstatus unter den Lagerbestand gerät, der durch den Minimalbestand definiert ist, muss eine größere Menge bestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9d41b-106">When the projected inventory passes below the inventory level defined by the reorder point, it is time to order more quantity.</span></span> <span data-ttu-id="9d41b-107">Unterdessen schrumpft der Lagerbestand erfahrungsgemäß schrittweise und erreicht wahrscheinlich den Punkt Null (oder den Sicherheitsbestand), bis der Vorrat aufgestockt wird.</span><span class="sxs-lookup"><span data-stu-id="9d41b-107">Meanwhile, the inventory is expected to decrease gradually and possibly reach zero (or the safety stock level), until the replenishment arrives.</span></span>  
  
<span data-ttu-id="9d41b-108">Entsprechend schlägt das Planungssystem einen vorwärtsgeplanten Beschaffungsauftrag an dem Zeitpunkt vor, an dem der geplante Bestand unter den Minimalbestand sinkt.</span><span class="sxs-lookup"><span data-stu-id="9d41b-108">Accordingly, the planning system will suggest a forward-scheduled supply order at the point when the projected inventory passes below the reorder point.</span></span>  
  
<span data-ttu-id="9d41b-109">Der Minimalbestand reflektiert einen bestimmten Lagerbestand.</span><span class="sxs-lookup"><span data-stu-id="9d41b-109">The reorder point reflects a certain inventory level.</span></span> <span data-ttu-id="9d41b-110">Allerdings können sich Lagerbestände während des Zeitrahmens erheblich ändern, daher muss das Planungssystem ständig den voraussichtlich verfügbaren Lagerbestand überwachen.</span><span class="sxs-lookup"><span data-stu-id="9d41b-110">However, inventory levels can move significantly during the time bucket and, therefore, the planning system must constantly monitor the projected available inventory.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9d41b-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d41b-111">See Also</span></span>  
<span data-ttu-id="9d41b-112">[Designdetails: Wiederbeschaffungsverfahren](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="9d41b-112">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="9d41b-113">[Designdetails: Planungsparameter](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="9d41b-113">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="9d41b-114">[Designdetails: Umgang mit Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="9d41b-114">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="9d41b-115">Designdetails: Vorratsplanung</span><span class="sxs-lookup"><span data-stu-id="9d41b-115">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
