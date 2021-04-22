---
title: 'Designdetails: Artikelnachverfolgung im Lager | Microsoft Docs'
description: Der Umgang mit Serien- oder Chargennummern ist hauptsächlich eine Lageraufgabe; daher haben alle eingehenden und ausgehenden Lagerbelege Standardfunktionen für die Zuordnung und die Auswahl von Artikelverfolgungsnummern. Da das Reservierungssystem auf Artikelposten basiert, werden Lageraktivitätsbelege, die nur Lagerplatzposten erfassen, jedoch nicht vollständig unterstützt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, serial number, lot number, outbound documents
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: fdd76b21254fc40d2d02332f29c2e002900fdc8b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775140"
---
# <a name="design-details-item-tracking-in-the-warehouse"></a><span data-ttu-id="d34b9-104">Designdetails: Artikelverfolgung im Lager</span><span class="sxs-lookup"><span data-stu-id="d34b9-104">Design Details: Item Tracking in the Warehouse</span></span>
<span data-ttu-id="d34b9-105">Der Umgang mit Serien- oder Chargennummern ist hauptsächlich eine Lageraufgabe; daher haben alle eingehenden und ausgehenden Lagerbelege Standardfunktionen für die Zuordnung und die Auswahl von Artikelverfolgungsnummern.</span><span class="sxs-lookup"><span data-stu-id="d34b9-105">Serial number and lot number handling is primarily a warehouse task and therefore all inbound and outbound warehouse documents have standard functionality for assigning and selecting item tracking numbers.</span></span>  

<span data-ttu-id="d34b9-106">Da das Reservierungssystem auf Artikelposten basiert, werden Lageraktivitätsbelege, die nur Lagerplatzposten erfassen, jedoch nicht vollständig unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d34b9-106">However, because the reservation system is based on item ledger entries, warehouse activity documents that register only warehouse entries are not fully supported.</span></span> <span data-ttu-id="d34b9-107">Da Reservierungen und Artikelverfolgungsnummern nur auf Lagerort- (und nicht auf Lagerplatz- oder Zonen-) Ebene bearbeitet werden können, kann die Seite **Artikelverfolgungszeilen** nicht aus den Lageraktivitätsbelegen heraus geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="d34b9-107">Because reservations and item tracking numbers can be handled only at the location level, not at the bin and zone level, the **Item Tracking Lines** page cannot be opened from warehouse activity documents.</span></span> <span data-ttu-id="d34b9-108">Dies gilt auch für die Seite **Reservierung**.</span><span class="sxs-lookup"><span data-stu-id="d34b9-108">The same applies to the **Reservation** page.</span></span>  

<span data-ttu-id="d34b9-109">Nachdem eine Serien- oder eine Chargennummer dem Bestand an einem Lagerort hinzugefügt wurde, kann sie verschoben und frei im Lager neuklassifiziert werden, indem eine unabhängige Artikelnachverfolgungsstruktur, die keine Beziehung zum Reservierungssystem hat, verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d34b9-109">After a serial or lot number has been added to an item at a warehouse location, it can be moved and reclassified freely within the warehouse by using an independent item tracking structure that is unrelated to the reservation system.</span></span> <span data-ttu-id="d34b9-110">Auf die Felder **Seriennr.** und **Chargennr.** wird direkt auf Logistikbelegzeilen zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="d34b9-110">**Serial No.** and **Lot No.** fields are accessed directly on warehouse document lines.</span></span> <span data-ttu-id="d34b9-111">Wenn die Serien- oder Chargennummer später in der ausgehenden Buchung erscheint, wird sie mit dem Reservierungssystem als Teil einer gewöhnlichen Lagerplatzanpassung synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="d34b9-111">When the serial or lot number later partakes in outbound posting, it is synchronized with the reservation system as a part of ordinary bin adjustment.</span></span> <span data-ttu-id="d34b9-112">Weitere Informationen finden Sie unter [Designdetails: Bestandintegration](design-details-integration-with-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="d34b9-112">For more information, see [Design Details: Integration with Inventory](design-details-integration-with-inventory.md).</span></span>  

<span data-ttu-id="d34b9-113">Das Reservierungssystem berücksichtigt jedoch Lageraktivitäten, wenn es die Verfügbarkeit berechnet.</span><span class="sxs-lookup"><span data-stu-id="d34b9-113">However, the reservation system does take warehouse activities into consideration when it calculates availability.</span></span> <span data-ttu-id="d34b9-114">Beispielsweise können Artikel, die Kommissionierungen zugewiesen oder als kommissioniert registriert sind, nicht reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="d34b9-114">For example, items that are allocated to picks, or registered as picked, cannot be reserved.</span></span> <span data-ttu-id="d34b9-115">Weitere Informationen finden Sie unter [Designdetails: Verfügbarkeit im Lager](design-details-availability-in-the-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="d34b9-115">For more information, see [Design Details: Warehouse Availability](design-details-availability-in-the-warehouse.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d34b9-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d34b9-116">See Also</span></span>  
[<span data-ttu-id="d34b9-117">Designdetails: Artikelnachverfolgung</span><span class="sxs-lookup"><span data-stu-id="d34b9-117">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)  
[<span data-ttu-id="d34b9-118">Designdetails: Integration mit dem Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="d34b9-118">Design Details: Integration with Inventory</span></span>](design-details-integration-with-inventory.md)  
[<span data-ttu-id="d34b9-119">Designdetails: Verfügbarkeit im Lager</span><span class="sxs-lookup"><span data-stu-id="d34b9-119">Design Details: Warehouse Availability</span></span>](design-details-availability-in-the-warehouse.md)  
[<span data-ttu-id="d34b9-120">Designdetails: Artikelverfolgungsdesign</span><span class="sxs-lookup"><span data-stu-id="d34b9-120">Design Details: Item Tracking Design</span></span>](design-details-item-tracking-design.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]