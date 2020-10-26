---
title: So aktivieren Sie die Kommissionierung nach FEFO | Microsoft Docs
description: FEFO (First-Expired-First-Out) ist eine Sortiermethode, durch die sichergestellt ist, dass die ältesten Artikel mit den frühesten Ablaufdatumsangaben zuerst kommissioniert werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a34af93c4aae2d87d17fcad4f0526783a01e8b64
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915943"
---
# <a name="enable-picking-items-by-fefo"></a><span data-ttu-id="463f6-103">Aktiveren der Kommissionierung von Artikeln nach FEFO</span><span class="sxs-lookup"><span data-stu-id="463f6-103">Enable Picking Items by FEFO</span></span>
<span data-ttu-id="463f6-104">FEFO (First-Expired-First-Out) ist eine Sortiermethode, durch die sichergestellt ist, dass die ältesten Artikel mit den frühesten Ablaufdatumsangaben zuerst kommissioniert werden.</span><span class="sxs-lookup"><span data-stu-id="463f6-104">First-Expired-First-Out (FEFO) is a sorting method that ensures that the oldest items, those with the earliest expiration dates, are picked first.</span></span>  

 <span data-ttu-id="463f6-105">Diese Funktionen arbeiten nur, wenn die folgenden Kriterien erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="463f6-105">This functionality only works when the following criteria are met:</span></span>  

-   <span data-ttu-id="463f6-106">Der Artikel muss eine Serien-/Chargennummer haben.</span><span class="sxs-lookup"><span data-stu-id="463f6-106">The item must have a serial/lot number.</span></span>  
-   <span data-ttu-id="463f6-107">Bei der Einrichtung des Artikelverfolgungscodes des Artikels muss das Feld **Seriennr.-Verf. Lager** oder das Feld **Chargennr.-Verf. Lager** ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="463f6-107">On the item’s item tracking code setup, the **SN Warehouse Tracking** field or the **Lot Warehouse Tracking** field must be selected.</span></span>  
-   <span data-ttu-id="463f6-108">Der Artikel muss mit einem Ablaufdatum im Lager gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="463f6-108">The item must be posted to inventory with an expiration date.</span></span>  
-   <span data-ttu-id="463f6-109">Das Kontrollkästchen **Kommissionierung erforderlich** auf der Lagerortkarte muss aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="463f6-109">On the location card, the **Require Pick** check box must be selected.</span></span>  
-   <span data-ttu-id="463f6-110">Das Kontrollkästchen **Gemäß FEFO kommissionieren** auf der Lagerortkarte muss aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="463f6-110">On the location card, the **Pick According to FEFO** check box must be selected.</span></span>  
-   <span data-ttu-id="463f6-111">Das Kontrollkästchen **Kommissionierung erforderlich** muss auf der Lagerortkarte aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="463f6-111">On the location card, the **Bin Mandatory** check box must be selected.</span></span>  

 <span data-ttu-id="463f6-112">Wenn alle Kriterien erfüllt sein, werden zu kommissionierenden Artikel mit Serien-/Chargennummern bei allen in Kommissionierungen und Lagerplatzumlagerungen mit dem ältesten zuerst sortiert. Ausgenommen sind Artikel mit SN-spezifischer oder chargenspezifischer Verfolgung.</span><span class="sxs-lookup"><span data-stu-id="463f6-112">When all the criteria are met, then serial/lot-numbered items to be picked are sorted with the oldest first in all picks and movements, except for items that use SN-specific or lot-specific tracking.</span></span>  

> [!NOTE]  
> <span data-ttu-id="463f6-113">Wenn einige serien-/chargennummerierte Artikel eine spezifische Verfolgung verwenden, werden diese zuerst berücksichtigt und danach werden die verbleibenden unspezifischen Serien-/Chargennummern gemäß FEFO aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="463f6-113">If some serial/lot-numbered items use specific tracking, then those are respected first and under them, the remaining, non-specific, serial/lot numbers are listed according to FEFO.</span></span>
<br /><br />
<span data-ttu-id="463f6-114">Weisen zwei Artikel mit Serien-/Chargennummer dasselbe Ablaufdatum aufweisen, wählt die Anwendung den Artikel mit der niedrigeren Serien- oder Chargennummer aus.</span><span class="sxs-lookup"><span data-stu-id="463f6-114">If two serial/lot-numbered items have the same expiration date, then application selects the item with the lowest serial or lot number.</span></span>
<br /><br />
<span data-ttu-id="463f6-115">Werden Artikel mit Serien-/Chargennummer an Lagerorten kommissioniert, die für die gesteuerte Einlagerung und Kommissionierung eingerichtet sind, werden bei der FEFO-Methode lediglich Mengen aus Lagerplätzen vom Typ *Kommissionierung* kommissioniert.</span><span class="sxs-lookup"><span data-stu-id="463f6-115">When picking serial/lot-numbered items in locations set up for directed put-away and pick, only quantities on bins of type *Pick* are picked according to FEFO.</span></span>  
<br /><br />
<span data-ttu-id="463f6-116">Die Aktivierung der Umlagerungen nach FEFO erfolgt entweder auf der Seite **Lagerbestandsumlagerung** oder auf der Seite **Lagerplatzumlagerungsvorschlag** , indem das Feld **Von Lagerplatz** leer gelassen wird.</span><span class="sxs-lookup"><span data-stu-id="463f6-116">To enable movements according to FEFO, either on the **Inventory Movement** page or the **Movement Worksheet** page, you must leave the **From Bin** field empty.</span></span>  
<br /><br />
<span data-ttu-id="463f6-117">Wenn das Feld **Fixes Ablaufdatum** ausgewählt ist, werden nur Artikel, die nicht abgelaufen sind, in die Kommissionierung einbezogen.</span><span class="sxs-lookup"><span data-stu-id="463f6-117">If the **Strict Expiration Posting** field is selected, then only items that are not expired will be included in the pick.</span></span> <span data-ttu-id="463f6-118">Dies gilt auch dann, wenn Sie die Kommissionierung gemäß FEFO nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="463f6-118">This applies even if you are not using Pick according to FEFO.</span></span>

## <a name="see-also"></a><span data-ttu-id="463f6-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="463f6-119">See Also</span></span>  
<span data-ttu-id="463f6-120">[Kommissionieren von Artikeln](warehouse-pick-items.md) </span><span class="sxs-lookup"><span data-stu-id="463f6-120">[Picking Items](warehouse-pick-items.md) </span></span>  
<span data-ttu-id="463f6-121">[Um Artikel für den Warenausgang zu kommissionieren](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="463f6-121">[Pick Items for Warehouse Shipment](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span></span>  
<span data-ttu-id="463f6-122">[Artikel mit der Lagerkommissionierung kommissionieren](warehouse-how-to-pick-items-with-inventory-picks.md) </span><span class="sxs-lookup"><span data-stu-id="463f6-122">[Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md) </span></span>  
[<span data-ttu-id="463f6-123">Designdetails: Logistik</span><span class="sxs-lookup"><span data-stu-id="463f6-123">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
[<span data-ttu-id="463f6-124">Lagerbest</span><span class="sxs-lookup"><span data-stu-id="463f6-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="463f6-125">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="463f6-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
