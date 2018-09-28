---
title: So aktivieren Sie die Kommissionierung nach FEFO | Microsoft Docs
description: "FEFO (First-Expired-First-Out) ist eine Sortiermethode, durch die sichergestellt ist, dass die ältesten Artikel mit den frühesten Ablaufdatumsangaben zuerst kommissioniert werden."
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
ms.openlocfilehash: 7e494ebc118b7c75ab565ae57259030987bbeee7
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="enable-picking-items-by-fefo"></a><span data-ttu-id="d1ed5-103">Aktiveren der Kommissionierung von Artikeln nach FEFO</span><span class="sxs-lookup"><span data-stu-id="d1ed5-103">Enable Picking Items by FEFO</span></span>
<span data-ttu-id="d1ed5-104">FEFO (First-Expired-First-Out) ist eine Sortiermethode, durch die sichergestellt ist, dass die ältesten Artikel mit den frühesten Ablaufdatumsangaben zuerst kommissioniert werden.</span><span class="sxs-lookup"><span data-stu-id="d1ed5-104">First-Expired-First-Out (FEFO) is a sorting method that ensures that the oldest items, those with the earliest expiration dates, are picked first.</span></span>  

 <span data-ttu-id="d1ed5-105">Diese Funktionen arbeiten nur, wenn die folgenden Kriterien erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="d1ed5-105">This functionality only works when the following criteria are met:</span></span>  

-   <span data-ttu-id="d1ed5-106">Der Artikel muss eine Serien-/Chargennummer haben.</span><span class="sxs-lookup"><span data-stu-id="d1ed5-106">The item must have a serial/lot number.</span></span>  
-   <span data-ttu-id="d1ed5-107">Bei der Einrichtung des Artikelverfolgungscodes des Artikels muss das Feld **Seriennr.-spezifische Verf.** oder das Feld **Chargennr.-spezifische Verf.** aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="d1ed5-107">On the item’s item tracking code setup, the **SN-Specific Warehouse Tracking** field or the **Lot-Specific Warehouse Tracking** field must be selected.</span></span>  
-   <span data-ttu-id="d1ed5-108">Der Artikel muss mit einem Ablaufdatum im Lager gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="d1ed5-108">The item must be posted to inventory with an expiration date.</span></span>  
-   <span data-ttu-id="d1ed5-109">Das Kontrollkästchen **Kommissionierung erforderlich** auf der Lagerortkarte muss aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="d1ed5-109">On the location card, the **Require Pick** check box must be selected.</span></span>  
-   <span data-ttu-id="d1ed5-110">Das Kontrollkästchen **Gemäß FEFO kommissionieren** auf der Lagerortkarte muss aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="d1ed5-110">On the location card, the **Pick According to FEFO** check box must be selected.</span></span>  
-   <span data-ttu-id="d1ed5-111">Das Kontrollkästchen **Kommissionierung erforderlich** muss auf der Lagerortkarte aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="d1ed5-111">On the location card, the **Bin Mandatory** check box must be selected.</span></span>  

 <span data-ttu-id="d1ed5-112">Wenn alle Kriterien erfüllt sein, werden zu kommissionierenden Artikel mit Serien-/Chargennummern bei allen in Kommissionierungen und Lagerplatzumlagerungen mit dem ältesten zuerst sortiert. Ausgenommen sind Artikel mit SN-spezifischer oder chargenspezifischer Verfolgung.</span><span class="sxs-lookup"><span data-stu-id="d1ed5-112">When all the criteria are met, then serial/lot-numbered items to be picked are sorted with the oldest first in all picks and movements, except for items that use SN-specific or lot-specific tracking.</span></span>  

> [!NOTE]  
> <span data-ttu-id="d1ed5-113">Wenn einige serien-/chargennummerierte Artikel eine spezifische Verfolgung verwenden, werden diese zuerst berücksichtigt und danach werden die verbleibenden unspezifischen Serien-/Chargennummern gemäß FEFO aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d1ed5-113">If some serial/lot-numbered items use specific tracking, then those are respected first and under them, the remaining, non-specific, serial/lot numbers are listed according to FEFO.</span></span>
<br /><br />
<span data-ttu-id="d1ed5-114">Weisen zwei Artikel mit Serien-/Chargennummer dasselbe Ablaufdatum aus, wählt die Anwendung den Artikel mit der niedrigeren Serien- oder Chargennummer aus.</span><span class="sxs-lookup"><span data-stu-id="d1ed5-114">If two serial/lot-numbered items have the same expiration date, then the program selects the item with the lowest serial or lot number.</span></span>
<br /><br />
<span data-ttu-id="d1ed5-115">Werden Artikel mit Serien-/Chargennummer an Lagerorten kommissioniert, die für die gesteuerte Einlagerung und Kommissionierung eingerichtet sind, werden bei der FEFO-Methode lediglich Mengen aus Lagerplätzen vom Typ *Kommissionierung* kommissioniert.</span><span class="sxs-lookup"><span data-stu-id="d1ed5-115">When picking serial/lot-numbered items in locations set up for directed put-away and pick, only quantities on bins of type *Pick* are picked according to FEFO.</span></span>  
<br /><br />
<span data-ttu-id="d1ed5-116">Die Aktivierung der Umlagerungen nach FEFO erfolgt entweder im Fenster **Lagerbestandsumlagerung** oder im Fenster **Lagerplatzumlagerungsvorschlag**, indem das Feld **Von Lagerplatz** leer gelassen wird.</span><span class="sxs-lookup"><span data-stu-id="d1ed5-116">To enable movements according to FEFO, either in the **Inventory Movement** window or the **Movement Worksheet** window, you must leave the **From Bin** field empty.</span></span>  
<br /><br />
<span data-ttu-id="d1ed5-117">Wenn das Feld **Fixes Ablaufdatum** ausgewählt ist, werden nur Artikel, die nicht abgelaufen sind, in die Kommissionierung einbezogen.</span><span class="sxs-lookup"><span data-stu-id="d1ed5-117">If the **Strict Expiration Posting** field is selected, then only items that are not expired will be included in the pick.</span></span> <span data-ttu-id="d1ed5-118">Dies gilt auch dann, wenn Sie die Kommissionierung gemäß FEFO nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="d1ed5-118">This applies even if you are not using Pick according to FEFO.</span></span>

## <a name="see-also"></a><span data-ttu-id="d1ed5-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1ed5-119">See Also</span></span>  
<span data-ttu-id="d1ed5-120">[Kommissionieren von Artikeln](warehouse-pick-items.md) </span><span class="sxs-lookup"><span data-stu-id="d1ed5-120">[Picking Items](warehouse-pick-items.md) </span></span>  
<span data-ttu-id="d1ed5-121">[Um Artikel für den Warenausgang zu kommissionieren](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="d1ed5-121">[Pick Items for Warehouse Shipment](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span></span>  
<span data-ttu-id="d1ed5-122">[Artikel mit der Lagerkommissionierung kommissionieren](warehouse-how-to-pick-items-with-inventory-picks.md) </span><span class="sxs-lookup"><span data-stu-id="d1ed5-122">[Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md) </span></span>  
[<span data-ttu-id="d1ed5-123">Designdetails: Logistik</span><span class="sxs-lookup"><span data-stu-id="d1ed5-123">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
[<span data-ttu-id="d1ed5-124">Lagerbest</span><span class="sxs-lookup"><span data-stu-id="d1ed5-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="d1ed5-125">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d1ed5-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

