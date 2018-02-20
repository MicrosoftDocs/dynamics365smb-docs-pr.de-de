---
title: Einrichten von Bestand | Microsoft Docs
description: "Beschreibt, wie Lagervorgänge und Lagerorte eingerichtet werden, einschließlich Umlagerungsrouten und Standorte wie Lagerorte."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 01/12/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 5a667f28bd50bbd1149526e08e0d786da83bc8a6
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="setting-up-inventory"></a><span data-ttu-id="c3a84-103">Bestand einrichten</span><span class="sxs-lookup"><span data-stu-id="c3a84-103">Setting Up Inventory</span></span>
<span data-ttu-id="c3a84-104">Bevor Sie Lageraktivitäten und Lagerbewertung verwalten können, müssen die Regeln und Werte konfiguriert werden, die die Lagerbestandsrichtlinien des Unternehmens definieren.</span><span class="sxs-lookup"><span data-stu-id="c3a84-104">Before you can manage warehouse activities and inventory costing, you must configure the rules and values that define the company's inventory policies.</span></span>

<span data-ttu-id="c3a84-105">Sie können einen besseren Kundenservice bieten und Ihre Lieferkette optimieren, indem Sie Ihren Lagerbestand an verschiedenen Adressen organisieren.</span><span class="sxs-lookup"><span data-stu-id="c3a84-105">You can provide better customer service and optimize your supply chain by organizing your inventory at different addresses.</span></span> <span data-ttu-id="c3a84-106">Sie können dann Artikel an unterschiedlichen Lagerorten kaufen, lagern und verkaufen sowie Lagerbestände zwischen ihnen umlagern.</span><span class="sxs-lookup"><span data-stu-id="c3a84-106">You can then buy, store, or sell items at different locations and transfer inventory between them.</span></span>

<span data-ttu-id="c3a84-107">Wenn Sie Ihr Lager so eingerichtet haben, können Sie verschiedene Lagervorgänge verwalten.</span><span class="sxs-lookup"><span data-stu-id="c3a84-107">When you have set up your inventory, you can manage various processes related to item transactions.</span></span> <span data-ttu-id="c3a84-108">Weitere Informationen finden Sie unter [Verwalten von Lager-](inventory-manage-inventory.md) und [Lagerort-Verwaltung](warehouse-manage-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="c3a84-108">For more information, see [Manage Inventory](inventory-manage-inventory.md) and [Warehouse Management](warehouse-manage-warehouse.md).</span></span>

| <span data-ttu-id="c3a84-109">An</span><span class="sxs-lookup"><span data-stu-id="c3a84-109">To</span></span> | <span data-ttu-id="c3a84-110">Siehe</span><span class="sxs-lookup"><span data-stu-id="c3a84-110">See</span></span> |
| --- | --- |
| <span data-ttu-id="c3a84-111">Definieren Sie die allgemeinen Lagereinstellungen, wie Nummernserien und wie Lagerorte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3a84-111">Define the general inventory setup, such as number series and how to use locations.</span></span> |[<span data-ttu-id="c3a84-112">So richten Sie allgemeine Lagerbestandsinformationen ein</span><span class="sxs-lookup"><span data-stu-id="c3a84-112">Set Up General Inventory Information</span></span>](inventory-how-setup-general.md) |
|<span data-ttu-id="c3a84-113">Konfigurieren Sie ein effizientes Vertriebsmodell mit einer Kombination verschiedener Lagerorte und Zuständigkeitseinheiten, die Geschäftspartnern oder Mitarbeitern zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="c3a84-113">Configure an efficient distribution model with a combination of different locations and responsibility centers assigned to business partners or employees.</span></span>|[<span data-ttu-id="c3a84-114">Arbeiten mit Zuständigkeitseinheiten</span><span class="sxs-lookup"><span data-stu-id="c3a84-114">Work with Responsibility Centers</span></span>](inventory-responsibility-centers.md)|
| <span data-ttu-id="c3a84-115">Organisieren Sie Ihr Lager an mehreren Lagerorten, einschließlich Umlagerungsrouten.</span><span class="sxs-lookup"><span data-stu-id="c3a84-115">Organize your inventory at multiple locations, including transfer routes.</span></span> |[<span data-ttu-id="c3a84-116">Einrichten von Lagerorten</span><span class="sxs-lookup"><span data-stu-id="c3a84-116">Set Up Locations</span></span>](inventory-how-register-new-items.md) |
| <span data-ttu-id="c3a84-117">Erstellen Sie Artikelkarten für Lagerartikel, mit denen Sie handeln.</span><span class="sxs-lookup"><span data-stu-id="c3a84-117">Create item cards for inventory items that you trade in.</span></span> |[<span data-ttu-id="c3a84-118">Neue Artikel registrieren</span><span class="sxs-lookup"><span data-stu-id="c3a84-118">Register New Items</span></span>](inventory-how-register-new-items.md) |
|<span data-ttu-id="c3a84-119">Einrichten mehrerer Einheiten für einen Artikel, den Sie für Alternativvorrat, beispielsweise auf Verkauf, Einkauf oder Buchungen innerhalb der Fertigung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="c3a84-119">Set up multiple units of measure for an item that you can use as alternate UOMs, for example on sales, purchasing, or production transactions.</span></span>|[<span data-ttu-id="c3a84-120">Artikeleinheiten einrichten</span><span class="sxs-lookup"><span data-stu-id="c3a84-120">Set Up Item Units of Measure</span></span>](inventory-how-setup-units-of-measure.md)|
|<span data-ttu-id="c3a84-121">Sie können Lagerhaltungsdaten verwenden, um Informationen über Ihre Artikel für einen bestimmten Lagerortcode und/oder einen bestimmten Variantencode zu speichern.</span><span class="sxs-lookup"><span data-stu-id="c3a84-121">As a supplement to item cards, record information about your items in a specific location or of a specific variant.</span></span>|[<span data-ttu-id="c3a84-122">Lagerhaltungsdaten einrichten</span><span class="sxs-lookup"><span data-stu-id="c3a84-122">Set Up Stockkeeping Units</span></span>](inventory-how-to-set-up-stockkeeping-units.md)|
| <span data-ttu-id="c3a84-123">Artikel den Kategorien zuweisen und ihnen Attribute zuweisen, damit Sie und die Kunden die Artikel finden.</span><span class="sxs-lookup"><span data-stu-id="c3a84-123">Assign items to categories and give them attributes to help you and customers find items.</span></span> |[<span data-ttu-id="c3a84-124">Artikel kategorisieren</span><span class="sxs-lookup"><span data-stu-id="c3a84-124">Categorize Items</span></span>](inventory-how-categorize-items.md) |

## <a name="see-also"></a><span data-ttu-id="c3a84-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3a84-125">See Also</span></span>
[<span data-ttu-id="c3a84-126">Verwalten des Lagerbestands</span><span class="sxs-lookup"><span data-stu-id="c3a84-126">Managing Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="c3a84-127">Käufe verwalten</span><span class="sxs-lookup"><span data-stu-id="c3a84-127">Managing Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="c3a84-128">[Verkäufe verwalten](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="c3a84-128">[Managing Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="c3a84-129">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c3a84-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="c3a84-130">Allgemeine Geschäftsfunktionen</span><span class="sxs-lookup"><span data-stu-id="c3a84-130">General Business Functionality</span></span>](ui-across-business-areas.md)

