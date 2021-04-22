---
title: So aktivieren Sie die Kommissionierung nach FEFO | Microsoft Docs
description: FEFO (First-Expired-First-Out) ist eine Sortiermethode, durch die sichergestellt ist, dass die ältesten Artikel mit den frühesten Ablaufdatumsangaben zuerst kommissioniert werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3a47c9daeeab036055a0644e1b389735f7440106
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784067"
---
# <a name="enable-picking-items-by-fefo"></a><span data-ttu-id="6a2e7-103">Aktiveren der Kommissionierung von Artikeln nach FEFO</span><span class="sxs-lookup"><span data-stu-id="6a2e7-103">Enable Picking Items by FEFO</span></span>
<span data-ttu-id="6a2e7-104">FEFO (First-Expired-First-Out) ist eine Sortiermethode, durch die sichergestellt ist, dass die ältesten Artikel mit den frühesten Ablaufdatumsangaben zuerst kommissioniert werden.</span><span class="sxs-lookup"><span data-stu-id="6a2e7-104">First-Expired-First-Out (FEFO) is a sorting method that ensures that the oldest items, those with the earliest expiration dates, are picked first.</span></span>  

 <span data-ttu-id="6a2e7-105">Diese Funktionen arbeiten nur, wenn die folgenden Kriterien erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="6a2e7-105">This functionality only works when the following criteria are met:</span></span>  

-   <span data-ttu-id="6a2e7-106">Der Artikel muss eine Serien-/Chargennummer haben.</span><span class="sxs-lookup"><span data-stu-id="6a2e7-106">The item must have a serial/lot number.</span></span>  
-   <span data-ttu-id="6a2e7-107">Bei der Einrichtung des Artikelverfolgungscodes des Artikels muss das Feld **Seriennr.-Verf. Lager** oder das Feld **Chargennr.-Verf. Lager** ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="6a2e7-107">On the item’s item tracking code setup, the **SN Warehouse Tracking** field or the **Lot Warehouse Tracking** field must be selected.</span></span>  
-   <span data-ttu-id="6a2e7-108">Der Artikel muss mit einem Ablaufdatum im Lager gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="6a2e7-108">The item must be posted to inventory with an expiration date.</span></span>  
-   <span data-ttu-id="6a2e7-109">Für den Standort müssen die Schalter **Kommissionierung erforderlich**, **Gemäß FEFO kommissionieren** und **Lagerplatz notwendig** eingeschaltet sein.</span><span class="sxs-lookup"><span data-stu-id="6a2e7-109">On the location, the **Require Pick**, **Pick According to FEFO**, and **Bin Mandatory** toggles must be turned on.</span></span>  

 <span data-ttu-id="6a2e7-110">Wenn alle Kriterien erfüllt sein, werden zu kommissionierenden Artikel mit Serien-/Chargennummern bei allen in Kommissionierungen und Lagerplatzumlagerungen mit dem ältesten zuerst sortiert. Ausgenommen sind Artikel mit SN-spezifischer oder chargenspezifischer Verfolgung.</span><span class="sxs-lookup"><span data-stu-id="6a2e7-110">When all the criteria are met, then serial/lot-numbered items to be picked are sorted with the oldest first in all picks and movements, except for items that use SN-specific or lot-specific tracking.</span></span>  

> [!NOTE]  
> <span data-ttu-id="6a2e7-111">Wenn einige serien- oder chargennummerierte Artikel eine spezifische Verfolgung verwenden, werden diese zuerst berücksichtigt und danach werden die verbleibenden unspezifischen Serien-/Chargennummern gemäß FEFO aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6a2e7-111">If some serial or lot-numbered items use specific tracking, then those are respected first and under them, the remaining, non-specific, serial/lot numbers are listed according to FEFO.</span></span>
<br /><br />
<span data-ttu-id="6a2e7-112">Weisen zwei Artikel mit Serien- oder Chargennummer dasselbe Ablaufdatum aufweisen, wählt die Anwendung den Artikel mit der niedrigeren Serien- oder Chargennummer aus.</span><span class="sxs-lookup"><span data-stu-id="6a2e7-112">If two serial or lot-numbered items have the same expiration date, then the application selects the item with the lowest serial or lot number.</span></span>
<br /><br />
<span data-ttu-id="6a2e7-113">Werden Artikel mit Serien- oder Chargennummer an Lagerorten kommissioniert, die für die gesteuerte Einlagerung und Kommissionierung eingerichtet sind, werden bei der FEFO-Methode lediglich Mengen aus Lagerplätzen vom Typ *Kommissionierung* kommissioniert.</span><span class="sxs-lookup"><span data-stu-id="6a2e7-113">When picking serial or lot-numbered items in locations set up for directed put-away and pick, only quantities on bins of type *Pick* are picked according to FEFO.</span></span>  
<br /><br />
<span data-ttu-id="6a2e7-114">Die Aktivierung der Umlagerungen nach FEFO erfolgt entweder auf dem Feld **Von Lagerplatz** auf der Seite **Lagerbestandsumlagerung** oder der Seite **Lagerplatzumlagerungsarbeitsblatt**.</span><span class="sxs-lookup"><span data-stu-id="6a2e7-114">To enable movements according to FEFO, leave the **From Bin** field empty on the **Inventory Movement** page or the **Movement Worksheet** pages.</span></span>  
<br /><br />
<span data-ttu-id="6a2e7-115">Wenn das Feld **Fixes Ablaufdatum** auf der **Artikelnachverfolgungscodekarte** ausgewählt, werden nur Artikel, die nicht abgelaufen sind, in die Auswahl aufgenommen, und die Zeilen werden nach dem FEFO-Prinzip sortiert.</span><span class="sxs-lookup"><span data-stu-id="6a2e7-115">If the **Strict Expiration Posting** field is selected on the **Item Tracking Code Card**, only items that are not expired will be included in the pick, and the lines are sorted according to the FEFO principle.</span></span>

## <a name="see-also"></a><span data-ttu-id="6a2e7-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a2e7-116">See Also</span></span>  
<span data-ttu-id="6a2e7-117">[Kommissionieren von Artikeln](warehouse-pick-items.md) </span><span class="sxs-lookup"><span data-stu-id="6a2e7-117">[Picking Items](warehouse-pick-items.md) </span></span>  
<span data-ttu-id="6a2e7-118">[Um Artikel für den Warenausgang zu kommissionieren](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="6a2e7-118">[Pick Items for Warehouse Shipment](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span></span>  
<span data-ttu-id="6a2e7-119">[Artikel mit der Lagerkommissionierung kommissionieren](warehouse-how-to-pick-items-with-inventory-picks.md) </span><span class="sxs-lookup"><span data-stu-id="6a2e7-119">[Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md) </span></span>  
[<span data-ttu-id="6a2e7-120">Designdetails: Logistik</span><span class="sxs-lookup"><span data-stu-id="6a2e7-120">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
[<span data-ttu-id="6a2e7-121">Lagerbest</span><span class="sxs-lookup"><span data-stu-id="6a2e7-121">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="6a2e7-122">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6a2e7-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]