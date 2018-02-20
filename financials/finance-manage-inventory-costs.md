---
title: Verwalten der Lagerregulierung | Microsoft Docs
description: Die Kostenverwaltung, die auch als "Lagerabgang" bezeichnet wird, dient zum Erfassen und Melden der Betriebskosten eines Unternehmens. Sie umfasst das Melden von Fertigungskosten und Lagerkosten (also den Wert von Artikeln).
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e2443552440cae8a0d90753d9a56fdc82006a197
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="managing-inventory-costs"></a><span data-ttu-id="bf801-104">Verwalten der Lagerregulierung</span><span class="sxs-lookup"><span data-stu-id="bf801-104">Managing Inventory Costs</span></span>
<span data-ttu-id="bf801-105">Die Kostenverwaltung, die auch als "Lagerabgang" bezeichnet wird, dient zum Erfassen und Melden der Betriebskosten eines Unternehmens.</span><span class="sxs-lookup"><span data-stu-id="bf801-105">Cost management, also referred to as “costing”, is concerned with recording and reporting business operating costs.</span></span> <span data-ttu-id="bf801-106">Sie umfasst das Melden von Fertigungskosten und Lagerkosten (also den Wert von Artikeln).</span><span class="sxs-lookup"><span data-stu-id="bf801-106">It includes the reporting of manufacturing costs and inventory costs, that is, the value of items.</span></span>   

<span data-ttu-id="bf801-107">Wichtige Prinzipien: Mithilfe von Lagerabgangsmethoden werden die Bewertung von Artikeln sowie der Zeitpunkt definiert, zu dem sie das Lager verlassen. Durch eine Lagerregulierung werden die Kosten für verkaufte Waren mit zugehörigen, nach dem Verkauf gebuchten Einkaufskosten aktualisiert. Lagerwerte müssen in regelmäßigen Abständen auf dedizierte Sachkonten gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="bf801-107">Central principles to understand are that costing methods define how items are valued when they leave inventory, that cost adjustment updates the cost of goods sold with related purchase costs posted after the sale, and that inventory values must be posted to dedicated G/L accounts at regular intervals.</span></span>

<span data-ttu-id="bf801-108">Die folgende Tabelle enthält eine Abfolge von Aufgaben sowie Links zu den entsprechenden Themen, in denen diese Aufgaben erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="bf801-108">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="bf801-109">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="bf801-109">**To**</span></span>|<span data-ttu-id="bf801-110">**Siehe**</span><span class="sxs-lookup"><span data-stu-id="bf801-110">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="bf801-111">Lesen verschiedener Konzeptinformationen, um ein Verständnis für die Prinzipien und Definitionen zu entwickeln, auf denen die Lagerkostenbuchungsfunktionalität in [!INCLUDE[d365fin](includes/d365fin_md.md)] beruht</span><span class="sxs-lookup"><span data-stu-id="bf801-111">Read various conceptual information to understand the principles and definitions that govern the inventory costing accounting functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>|[<span data-ttu-id="bf801-112">Info über Lagerkostenberechnung</span><span class="sxs-lookup"><span data-stu-id="bf801-112">About Inventory Costing</span></span>](finance-learn-about-costing.md)|  
|<span data-ttu-id="bf801-113">Einrichten von Lagerbuchungsperioden, Lagerabgangsmethoden und Rundungsmethoden.</span><span class="sxs-lookup"><span data-stu-id="bf801-113">Set up inventory periods, costing methods, and rounding methods.</span></span>|[<span data-ttu-id="bf801-114">Einrichten der Lagerwertberechnung und der Kostenrechnung</span><span class="sxs-lookup"><span data-stu-id="bf801-114">Setting Up Inventory Valuation and Costing</span></span>](finance-set-up-inventory-valuation-and-costing.md)|
|<span data-ttu-id="bf801-115">Schreiben sie den Wert eines oder mehrerer Artikel im Lager ab oder bewerten sie ihn neu, indem Sie den aktuellen, berechneten Wert buchen.</span><span class="sxs-lookup"><span data-stu-id="bf801-115">Appreciate or depreciate the value of one or more items in inventory by posting their current, calculated value.</span></span>|[<span data-ttu-id="bf801-116">Neubewerten von Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="bf801-116">Revalue Inventory</span></span>](inventory-how-revalue-inventory.md)|
|<span data-ttu-id="bf801-117">Regulieren Sie Artikelkosten, entweder automatisch oder manuell, um Kostenänderungen aus eingehenden Posten an die entsprechenden ausgehenden Posten weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="bf801-117">Adjust item costs, either automatically or manually, to forward cost changes from inbound entries to their related outbound entries.</span></span>|[<span data-ttu-id="bf801-118">Artikelpreise justieren</span><span class="sxs-lookup"><span data-stu-id="bf801-118">Adjust Item Costs</span></span>](inventory-how-adjust-item-costs.md)|
|<span data-ttu-id="bf801-119">Verwendung spezieller Kostenberechnungsfunktionen für tägliche Artikeltransaktionen in den Artikeloperationen.</span><span class="sxs-lookup"><span data-stu-id="bf801-119">Use special costing functions for every-day item transactions in the item operations.</span></span>|[<span data-ttu-id="bf801-120">Verarbeiten von Lager- und Fertigungskosten</span><span class="sxs-lookup"><span data-stu-id="bf801-120">Handling Inventory and Manufacturing Costs</span></span>](finance-handle-inventory-and-manufacturing-costs.md)|  
|<span data-ttu-id="bf801-121">Regelmäßige Aktualisierung der festen Einstandspreise von Komponenten in Montage- oder Produktionsstücklisten und Übertragung der neuen Einstandspreise auf den übergeordneten Artikel.</span><span class="sxs-lookup"><span data-stu-id="bf801-121">Periodically update the standard costs of components, in assembly or production BOMs, and roll the new costs up to the parent item.</span></span>|[<span data-ttu-id="bf801-122">Standardkosten aktualisieren</span><span class="sxs-lookup"><span data-stu-id="bf801-122">Update Standard Costs</span></span>](finance-how-to-update-standard-costs.md)|
|<span data-ttu-id="bf801-123">Ausführen von Kontroll- und Berichterstellungsaufgaben am Periodenende – beispielsweise Berechnen des Werts von Lagerbestand und Buchen von Kosten in die Finanzbuchhaltung</span><span class="sxs-lookup"><span data-stu-id="bf801-123">Perform period-end control and reporting tasks, such calculate the value of inventory and post costs to the general ledger.</span></span>|[<span data-ttu-id="bf801-124">Melden von Kosten und Abstimmen mit der Finanzbuchhaltung</span><span class="sxs-lookup"><span data-stu-id="bf801-124">Reporting Costs and Reconciling with the General Ledger</span></span>](finance-report-costs-and-reconcile-with-the-general-ledger.md)|  
|<span data-ttu-id="bf801-125">Erfahren Sie mehr über die Mechanismen im Kostenrechnungssystem.</span><span class="sxs-lookup"><span data-stu-id="bf801-125">Learn about all mechanisms in the costing system.</span></span>|[<span data-ttu-id="bf801-126">Designdetails: Lagerkostenberechnung</span><span class="sxs-lookup"><span data-stu-id="bf801-126">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)|  

## <a name="see-also"></a><span data-ttu-id="bf801-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf801-127">See Also</span></span>  
 [<span data-ttu-id="bf801-128">Finanzen</span><span class="sxs-lookup"><span data-stu-id="bf801-128">Finance</span></span>](finance.md)  
 <span data-ttu-id="bf801-129">[Lagerbest](inventory-manage-inventory.md) </span><span class="sxs-lookup"><span data-stu-id="bf801-129">[Inventory](inventory-manage-inventory.md) </span></span>  
 <span data-ttu-id="bf801-130">[Verkauf](sales-manage-sales.md) </span><span class="sxs-lookup"><span data-stu-id="bf801-130">[Sales](sales-manage-sales.md) </span></span>  
 [<span data-ttu-id="bf801-131">Einkauf</span><span class="sxs-lookup"><span data-stu-id="bf801-131">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="bf801-132">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bf801-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

