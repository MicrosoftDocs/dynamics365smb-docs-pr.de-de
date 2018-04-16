---
title: So aktivieren Sie die Kommissionierung nach FEFO | Microsoft Docs
description: "FEFO (First-Expired-First-Out) ist eine Sortiermethode, durch die sichergestellt ist, dass die ältesten Artikel mit den frühesten Ablaufdatumsangaben zuerst kommissioniert werden."
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
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: e21ff28a472391ea19bc393ecfee017e7aa668f1
ms.contentlocale: de-de
ms.lasthandoff: 04/16/2018

---
# <a name="enable-picking-items-by-fefo"></a><span data-ttu-id="a19e9-103">Aktiveren der Kommissionierung von Artikeln nach FEFO</span><span class="sxs-lookup"><span data-stu-id="a19e9-103">Enable Picking Items by FEFO</span></span>
<span data-ttu-id="a19e9-104">FEFO (First-Expired-First-Out) ist eine Sortiermethode, durch die sichergestellt ist, dass die ältesten Artikel mit den frühesten Ablaufdatumsangaben zuerst kommissioniert werden.</span><span class="sxs-lookup"><span data-stu-id="a19e9-104">First-Expired-First-Out (FEFO) is a sorting method that ensures that the oldest items, those with the earliest expiration dates, are picked first.</span></span>  

 <span data-ttu-id="a19e9-105">Diese Funktionen arbeiten nur, wenn die folgenden Kriterien erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="a19e9-105">This functionality only works when the following criteria are met:</span></span>  

- <span data-ttu-id="a19e9-106">Der Artikel muss eine Serien-/Chargennummer haben.</span><span class="sxs-lookup"><span data-stu-id="a19e9-106">The item must have a serial/lot number.</span></span>  
- <span data-ttu-id="a19e9-107">Bei der Einrichtung des Artikelverfolgungscodes des Artikels muss das Feld **Seriennr.-spezifische Verf.** oder das Feld **Chargennr.-spezifische Verf.** aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="a19e9-107">On the item’s item tracking code setup, the **SN-Specific Warehouse Tracking** field or the **Lot-Specific Warehouse Tracking** field must be selected.</span></span>  
- <span data-ttu-id="a19e9-108">Der Artikel muss mit einem Ablaufdatum im Lager gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="a19e9-108">The item must be posted to inventory with an expiration date.</span></span>  
- <span data-ttu-id="a19e9-109">Das Kontrollkästchen **Kommissionierung erforderlich** auf der Lagerortkarte muss aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="a19e9-109">On the location card, the **Require Pick** check box must be selected.</span></span>  
- <span data-ttu-id="a19e9-110">Das Kontrollkästchen **Gemäß FEFO kommissionieren** auf der Lagerortkarte muss aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="a19e9-110">On the location card, the **Pick According to FEFO** check box must be selected.</span></span>  
- <span data-ttu-id="a19e9-111">Das Kontrollkästchen **Kommissionierung erforderlich** muss auf der Lagerortkarte aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="a19e9-111">On the location card, the **Bin Mandatory** check box must be selected.</span></span>  

  <span data-ttu-id="a19e9-112">Wenn alle Kriterien erfüllt sein, werden zu kommissionierenden Artikel mit Serien-/Chargennummern bei allen in Kommissionierungen und Lagerplatzumlagerungen mit dem ältesten zuerst sortiert. Ausgenommen sind Artikel mit SN-spezifischer oder chargenspezifischer Verfolgung.</span><span class="sxs-lookup"><span data-stu-id="a19e9-112">When all the criteria are met, then serial/lot-numbered items to be picked are sorted with the oldest first in all picks and movements, except for items that use SN-specific or lot-specific tracking.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="a19e9-113">Wenn einige serien-/chargennummerierte Artikel eine spezifische Verfolgung verwenden, werden diese zuerst berücksichtigt und danach werden die verbleibenden unspezifischen Serien-/Chargennummern gemäß FEFO aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a19e9-113">If some serial/lot-numbered items use specific tracking, then those are respected first and under them, the remaining, non-specific, serial/lot numbers are listed according to FEFO.</span></span>  

 <span data-ttu-id="a19e9-114">Weisen zwei Artikel mit Serien-/Chargennummer dasselbe Ablaufdatum aus, wählt die Anwendung den Artikel mit der niedrigeren Serien- oder Chargennummer aus.</span><span class="sxs-lookup"><span data-stu-id="a19e9-114">If two serial/lot-numbered items have the same expiration date, then the program selects the item with the lowest serial or lot number.</span></span> <span data-ttu-id="a19e9-115">Sind die Serien- oder Chargennummern identisch, wählt die Anwendung den Artikel aus, der zuerst registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="a19e9-115">If the serial or lot numbers are the same, then the program selects the item that was registered first.</span></span>  

> [!NOTE]
> - <span data-ttu-id="a19e9-116">Werden Artikel mit Serien-/Chargennummer an Lagerorten kommissioniert, die für die gesteuerte Einlagerung und Kommissionierung eingerichtet sind, werden bei der FEFO-Methode lediglich Mengen aus Lagerplätzen vom Typ *Kommissionierung* kommissioniert.</span><span class="sxs-lookup"><span data-stu-id="a19e9-116">When picking serial/lot-numbered items in locations set up for directed put-away and pick, only quantities on bins of type *Pick* are picked according to FEFO.</span></span>  
>   -   <span data-ttu-id="a19e9-117">Die Aktivierung der Umlagerungen nach FEFO erfolgt entweder im Fenster **Lagerbestandsumlagerung** oder im Fenster **Lagerplatzumlagerungsvorschlag**, indem das Feld **Von Lagerplatz** leer gelassen wird.</span><span class="sxs-lookup"><span data-stu-id="a19e9-117">To enable movements according to FEFO, either in the **Inventory Movement** window or the **Movement Worksheet** window, you must leave the **From Bin** field empty.</span></span>  
>   -   <span data-ttu-id="a19e9-118">Wenn das Feld **Fixes Ablaufdatum** ausgewählt ist, werden nur Artikel, die nicht abgelaufen sind, in die Kommissionierung einbezogen.</span><span class="sxs-lookup"><span data-stu-id="a19e9-118">If the **Strict Expiration Posting** field is selected, then only items that are not expired will be included in the pick.</span></span> <span data-ttu-id="a19e9-119">Dies gilt auch dann, wenn Sie die Kommissionierung gemäß FEFO nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="a19e9-119">This applies even if you are not using Pick according to FEFO.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a19e9-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a19e9-120">See Also</span></span>  
<span data-ttu-id="a19e9-121">[Kommissionieren von Artikeln](warehouse-pick-items.md) </span><span class="sxs-lookup"><span data-stu-id="a19e9-121">[Picking Items](warehouse-pick-items.md) </span></span>  
<span data-ttu-id="a19e9-122">[Um Artikel für den Warenausgang zu kommissionieren](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="a19e9-122">[Pick Items for Warehouse Shipment](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span></span>  
<span data-ttu-id="a19e9-123">[Artikel mit der Lagerkommissionierung kommissionieren](warehouse-how-to-pick-items-with-inventory-picks.md) </span><span class="sxs-lookup"><span data-stu-id="a19e9-123">[Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md) </span></span>  
[<span data-ttu-id="a19e9-124">Designdetails: Logistik</span><span class="sxs-lookup"><span data-stu-id="a19e9-124">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
[<span data-ttu-id="a19e9-125">Lagerbest</span><span class="sxs-lookup"><span data-stu-id="a19e9-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="a19e9-126">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a19e9-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

