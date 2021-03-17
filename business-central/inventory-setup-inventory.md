---
title: Einrichten von Bestand | Microsoft Docs
description: Beschreibt, wie Lagervorgänge und Lagerorte eingerichtet werden, einschließlich Umlagerungsrouten und Standorte wie Lagerorte.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3d11e39e54d864db2eac0a1a2e1919a3cfd7a767
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5392999"
---
# <a name="setting-up-inventory"></a><span data-ttu-id="8c3f5-103">Bestand einrichten</span><span class="sxs-lookup"><span data-stu-id="8c3f5-103">Setting Up Inventory</span></span>
<span data-ttu-id="8c3f5-104">Bevor Sie Lageraktivitäten und Lagerbewertung verwalten können, müssen die Regeln und Werte konfiguriert werden, die die Lagerbestandsrichtlinien des Unternehmens definieren.</span><span class="sxs-lookup"><span data-stu-id="8c3f5-104">Before you can manage warehouse activities and inventory costing, you must configure the rules and values that define the company's inventory policies.</span></span>

<span data-ttu-id="8c3f5-105">Sie können einen besseren Debitorenservice bieten und Ihre Lieferkette optimieren, indem Sie Ihren Lagerbestand an verschiedenen Adressen organisieren.</span><span class="sxs-lookup"><span data-stu-id="8c3f5-105">You can provide better customer service and optimize your supply chain by organizing your inventory at different addresses.</span></span> <span data-ttu-id="8c3f5-106">Sie können dann Artikel an unterschiedlichen Lagerorten kaufen, lagern und verkaufen sowie Lagerbestände zwischen ihnen umlagern.</span><span class="sxs-lookup"><span data-stu-id="8c3f5-106">You can then buy, store, or sell items at different locations and transfer inventory between them.</span></span>

<span data-ttu-id="8c3f5-107">Wenn Sie Ihr Lager so eingerichtet haben, können Sie verschiedene Lagervorgänge verwalten.</span><span class="sxs-lookup"><span data-stu-id="8c3f5-107">When you have set up your inventory, you can manage various processes related to item transactions.</span></span> <span data-ttu-id="8c3f5-108">Weitere Informationen finden Sie unter [Verwalten von Lager-](inventory-manage-inventory.md) und [Lagerort-Verwaltung](warehouse-manage-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="8c3f5-108">For more information, see [Manage Inventory](inventory-manage-inventory.md) and [Warehouse Management](warehouse-manage-warehouse.md).</span></span>

| <span data-ttu-id="8c3f5-109">An</span><span class="sxs-lookup"><span data-stu-id="8c3f5-109">To</span></span> | <span data-ttu-id="8c3f5-110">Siehe</span><span class="sxs-lookup"><span data-stu-id="8c3f5-110">See</span></span> |
| --- | --- |
| <span data-ttu-id="8c3f5-111">Definieren Sie die allgemeinen Lagereinstellungen, wie Nummernserien und wie Lagerorte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c3f5-111">Define the general inventory setup, such as number series and how to use locations.</span></span> |[<span data-ttu-id="8c3f5-112">So richten Sie allgemeine Lagerbestandsinformationen ein</span><span class="sxs-lookup"><span data-stu-id="8c3f5-112">Set Up General Inventory Information</span></span>](inventory-how-setup-general.md) |
|<span data-ttu-id="8c3f5-113">Konfigurieren Sie ein effizientes Vertriebsmodell mit einer Kombination verschiedener Lagerorte und Zuständigkeitseinheiten, die Geschäftspartnern oder Mitarbeitern zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="8c3f5-113">Configure an efficient distribution model with a combination of different locations and responsibility centers assigned to business partners or employees.</span></span>|[<span data-ttu-id="8c3f5-114">Arbeiten mit Zuständigkeitseinheiten</span><span class="sxs-lookup"><span data-stu-id="8c3f5-114">Work with Responsibility Centers</span></span>](inventory-responsibility-centers.md)|
| <span data-ttu-id="8c3f5-115">Organisieren Sie Ihr Lager an mehreren Lagerorten, einschließlich Umlagerungsrouten.</span><span class="sxs-lookup"><span data-stu-id="8c3f5-115">Organize your inventory at multiple locations, including transfer routes.</span></span> |[<span data-ttu-id="8c3f5-116">Einrichten von Lagerorten</span><span class="sxs-lookup"><span data-stu-id="8c3f5-116">Set Up Locations</span></span>](inventory-how-register-new-items.md) |
| <span data-ttu-id="8c3f5-117">Erstellen einer Artikelkarte für Lager-, Nicht-Lager- oder Serviceeinheiten, mit denen Sie gerade handeln.</span><span class="sxs-lookup"><span data-stu-id="8c3f5-117">Create item cards for inventory, non-inventory, or service items that you trade in.</span></span> |[<span data-ttu-id="8c3f5-118">Neue Artikel registrieren</span><span class="sxs-lookup"><span data-stu-id="8c3f5-118">Register New Items</span></span>](inventory-how-register-new-items.md) |
|<span data-ttu-id="8c3f5-119">Verwenden Sie die **Element kopieren** Funktion zum schnellen Erstellen einer neuen Artikelkarte basierend auf einer vorhandenen.</span><span class="sxs-lookup"><span data-stu-id="8c3f5-119">Use the **Copy Item** function to quickly create a new item card based on an existing one.</span></span>|[<span data-ttu-id="8c3f5-120">Kopieren von vorhandenen Artikeln um neue Artikel zu erstellen</span><span class="sxs-lookup"><span data-stu-id="8c3f5-120">Copy Existing Items to Create New Items</span></span>](inventory-how-copy-items.md)|
|<span data-ttu-id="8c3f5-121">Erfahren Sie, wie Sie das Feld **Art** entsprechend dem Geschäftszweck auf der Artikelkarte ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="8c3f5-121">Learn how to fill in the **Type** field on item cards according to the business purpose.</span></span>|[<span data-ttu-id="8c3f5-122">Info zu Elementtypen</span><span class="sxs-lookup"><span data-stu-id="8c3f5-122">About Item Types</span></span>](inventory-about-item-types.md)|
|<span data-ttu-id="8c3f5-123">Einrichten mehrerer Einheiten für einen Artikel, den Sie für Alternativvorrat, beispielsweise auf Verkauf, Einkauf oder Buchungen innerhalb der Fertigung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="8c3f5-123">Set up multiple units of measure for an item that you can use as alternate UOMs, for example on sales, purchasing, or production transactions.</span></span>|[<span data-ttu-id="8c3f5-124">Artikeleinheiten einrichten</span><span class="sxs-lookup"><span data-stu-id="8c3f5-124">Set Up Item Units of Measure</span></span>](inventory-how-setup-units-of-measure.md)|
|<span data-ttu-id="8c3f5-125">Sie können Lagerhaltungsdaten verwenden, um Informationen über Ihre Artikel für einen bestimmten Lagerortcode und/oder einen bestimmten Variantencode zu speichern.</span><span class="sxs-lookup"><span data-stu-id="8c3f5-125">As a supplement to item cards, record information about your items in a specific location or of a specific variant.</span></span>|[<span data-ttu-id="8c3f5-126">Lagerhaltungsdaten einrichten</span><span class="sxs-lookup"><span data-stu-id="8c3f5-126">Set Up Stockkeeping Units</span></span>](inventory-how-to-set-up-stockkeeping-units.md)|
| <span data-ttu-id="8c3f5-127">Artikel den Kategorien zuweisen und ihnen Attribute zuweisen, damit Sie und die Debitoren die Artikel finden.</span><span class="sxs-lookup"><span data-stu-id="8c3f5-127">Assign items to categories and give them attributes to help you and customers find items.</span></span> |[<span data-ttu-id="8c3f5-128">Artikel kategorisieren</span><span class="sxs-lookup"><span data-stu-id="8c3f5-128">Categorize Items</span></span>](inventory-how-categorize-items.md) |
|<span data-ttu-id="8c3f5-129">Importieren Sie mehrere Artikelbilder auf einmal aus einer ZIP-Datei, in der die Dateien entsprechend der Artikelnummern benannt sind.</span><span class="sxs-lookup"><span data-stu-id="8c3f5-129">Import multiple item pictures in one go from a zip file where the files are named according to item numbers.</span></span>|[<span data-ttu-id="8c3f5-130">Mehrere Artikelbilder importieren</span><span class="sxs-lookup"><span data-stu-id="8c3f5-130">Import Multiple Item Pictures</span></span>](inventory-how-import-item-pictures.md)|
|<span data-ttu-id="8c3f5-131">Geben Sie Standardberichte an, die für verschiedene Dokumenttypen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8c3f5-131">Specify default reports to be used for different document types.</span></span>|[<span data-ttu-id="8c3f5-132">Berichtsauswahl in Business Central</span><span class="sxs-lookup"><span data-stu-id="8c3f5-132">Report Selection in Business Central</span></span>](across-report-selections.md)|

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="8c3f5-133">Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="8c3f5-133">See Related Training at [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="8c3f5-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c3f5-134">See Also</span></span>

[<span data-ttu-id="8c3f5-135">Verwalten des Lagerbestands</span><span class="sxs-lookup"><span data-stu-id="8c3f5-135">Managing Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="8c3f5-136">Käufe verwalten</span><span class="sxs-lookup"><span data-stu-id="8c3f5-136">Managing Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="8c3f5-137">[Verkäufe verwalten](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="8c3f5-137">[Managing Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="8c3f5-138">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8c3f5-138">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="8c3f5-139">Allgemeine Geschäftsfunktionen</span><span class="sxs-lookup"><span data-stu-id="8c3f5-139">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]