---
title: 'Designdetails: Bedarf und Vorrat | Microsoft Docs'
description: Dieses Thema erläutert das Konzept der Nachfrage, welches der allgemeine Begriff ist für jede Art Brutto-Bedarf, wie beispielsweise für Verkaufsauftrags und Komponentenbedarf aus einem Fertigungsauftrag.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 23e941b3ab6fc8e2176268f38647630419453d23
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "933886"
---
# <a name="design-details-demand-and-supply"></a><span data-ttu-id="ae15a-103">Designdetails: Bedarf und Vorrat</span><span class="sxs-lookup"><span data-stu-id="ae15a-103">Design Details: Demand and Supply</span></span>
<span data-ttu-id="ae15a-104">Bedarf ist der Oberbegriff, der für jede Art Brutto-Bedarf verwendet wird, beispielsweise für Verkaufsauftrags und Komponentenbedarf aus einem Fertigungsauftrag.</span><span class="sxs-lookup"><span data-stu-id="ae15a-104">Demand is the common term used for any kind of gross demand, such as a sales order and component need from a production order.</span></span> <span data-ttu-id="ae15a-105">Darüber hinaus ermöglicht die Anwendung weitere technische Bedarfsarten, wie z.B. negative Lagerbestände und Einkaufsreklamationen.</span><span class="sxs-lookup"><span data-stu-id="ae15a-105">In addition, the program allows more technical types of demand, such as negative inventory and purchase returns.</span></span>  
  
<span data-ttu-id="ae15a-106">Vorrat ist der allgemeine Begriff für jede Art von positiver oder eingehender Menge, wie etwa Bestands-, Einkauf-, Montage-, Fertigungs- oder eingehende Umlagerungen.</span><span class="sxs-lookup"><span data-stu-id="ae15a-106">Supply is the common term used for any kind of positive or inbound quantity, such as inventory, purchases, assembly, production, or inbound transfers.</span></span> <span data-ttu-id="ae15a-107">Darüber hinaus stellt möglicherweise eine Verkaufsreklamation ebenfalls einen Vorrat dar.</span><span class="sxs-lookup"><span data-stu-id="ae15a-107">In addition, a sales return may also represent supply.</span></span>  
  
<span data-ttu-id="ae15a-108">Um die vielen Quellen von Nachfrage und Angebot zu sortieren, organisiert das Planungssystem sie auf zwei Zeitachsen, die Bestandsprofile genannt werden.</span><span class="sxs-lookup"><span data-stu-id="ae15a-108">To sort out the many sources of demand and supply, the planning system organizes them on two time lines called inventory profiles.</span></span> <span data-ttu-id="ae15a-109">Das eine Profil enthält Bedarfsereignisse und das andere enthält die entsprechenden Zubehörereignisse.</span><span class="sxs-lookup"><span data-stu-id="ae15a-109">One profile holds demand events, and the other holds the corresponding supply events.</span></span> <span data-ttu-id="ae15a-110">Jedes Ereignis repräsentiert eine Auftragsnetzwerkeinheit, wie etwa eine Verkaufsauftragszeile, einen Artikelposten oder eine Fertigungsauftragszeile.</span><span class="sxs-lookup"><span data-stu-id="ae15a-110">Each event represents one order network entity, such as a sales order line, an item ledger entry, or a production order line.</span></span>  
  
<span data-ttu-id="ae15a-111">Wenn Bestandsprofile geladen werden, werden die verschiedenen BBedarf-Vorrat-Sätze ausgeglichen, um einen Beschaffungsplan auszustellen, der die aufgeführten Ziele erfüllt.</span><span class="sxs-lookup"><span data-stu-id="ae15a-111">When inventory profiles are loaded, the different demand-supply sets are balanced to output a supply plan that fulfills the listed goals.</span></span>  
  
<span data-ttu-id="ae15a-112">Planungsparameter und Lagerbestände sind andere Arten von Bedarf und Vorrat bzw. sind einem integrierten Ausgleich unterworfen, um den Lagerbestand wieder aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="ae15a-112">Planning parameters and inventory levels are other types of demand and supply respectively, which undergo integrated balancing to replenish stock items.</span></span> <span data-ttu-id="ae15a-113">Weitere Informationen finden Sie unter [Designdetails: Behandlungs-Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md).</span><span class="sxs-lookup"><span data-stu-id="ae15a-113">For more information, see [Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ae15a-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae15a-114">See Also</span></span>  
<span data-ttu-id="ae15a-115">[Designdetails: Ausgleich von Bedarf und Vorrat](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="ae15a-115">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="ae15a-116">[Designdetails: Zentrale Konzepte des Planungssystems](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="ae15a-116">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="ae15a-117">Designdetails: Vorratsplanung</span><span class="sxs-lookup"><span data-stu-id="ae15a-117">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)