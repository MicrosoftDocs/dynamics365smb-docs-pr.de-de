---
title: 'Vorgehensweise: Buchen von Kapazitäten | Microsoft Docs'
description: 'Im Kapazitäts Buch.-Blatt buchen Sie verbrauchte Kapazität, die keinem Fertigungsauftrag zugeordnet ist. Zum Beispiel: Wartungsarbeit muss einem Arbeitsplatz oder einer Arbeitsplatzgruppe zugeordnet werden, aber nicht einem Fertigungsauftrag.'
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2fa0038745664c269d6d471c6d9373a9174df201
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4759192"
---
# <a name="post-capacities"></a><span data-ttu-id="b91d2-104">Kapazität buchen</span><span class="sxs-lookup"><span data-stu-id="b91d2-104">Post Capacities</span></span>
<span data-ttu-id="b91d2-105">Im Kapazitäts Buch.-Blatt buchen Sie verbrauchte Kapazität, die keinem Fertigungsauftrag zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b91d2-105">In the capacity journal, you post consumed capacities that are not assigned to the production order.</span></span> <span data-ttu-id="b91d2-106">Zum Beispiel: Wartungsarbeit muss einem Arbeitsplatz oder einer Arbeitsplatzgruppe zugeordnet werden, aber nicht einem Fertigungsauftrag.</span><span class="sxs-lookup"><span data-stu-id="b91d2-106">For example, maintenance work must be assigned to capacity, but not to a production order.</span></span>  

## <a name="to-post-capacities"></a><span data-ttu-id="b91d2-107">Kapazitäten buchen</span><span class="sxs-lookup"><span data-stu-id="b91d2-107">To post capacities</span></span>  
1.  <span data-ttu-id="b91d2-108">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Kapazitäts Buch.-Blätter** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="b91d2-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Capacity Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b91d2-109">Füllen Sie die Felder **Buchungsdatum** und **Belegnr.** aus.</span><span class="sxs-lookup"><span data-stu-id="b91d2-109">Fill in the **Posting Date** and **Document No.** fields.</span></span>  
3.  <span data-ttu-id="b91d2-110">Geben Sie in das Feld **Art** die Art der Kapazität entweder **Arbeitsplatz** oder **Arbeitsplatzgruppe** ein, die Sie buchen möchten.</span><span class="sxs-lookup"><span data-stu-id="b91d2-110">In the **Type** field, enter the type of the capacity, either **Machine Center** or **Work Center**, that you are posting.</span></span>  
4.  <span data-ttu-id="b91d2-111">Geben Sie im Feld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="b91d2-111">In the **No.**</span></span> <span data-ttu-id="b91d2-112">Geben Sie die Nummer des Arbeitsplatzes oder der Arbeitsplatzgruppe ein.</span><span class="sxs-lookup"><span data-stu-id="b91d2-112">field, enter the number of the machine center or work center.</span></span>  
5.  <span data-ttu-id="b91d2-113">Geben Sie in den anderen Feldern die entsprechenden Daten, wie zum Beispiel **Startzeit**, **Endzeit**, **Menge** und **Ausschuss** ein.</span><span class="sxs-lookup"><span data-stu-id="b91d2-113">Enter the relevant data in the other fields, such as **Starting Time**, **Ending Time**, **Quantity**, and **Scrap**.</span></span>  
6.  <span data-ttu-id="b91d2-114">Um die Rechnung zu buchen, wählen Sie die Aktion **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="b91d2-114">Choose the **Post** action to post the capacities.</span></span>  

## <a name="to-view-work-center-ledger-entries"></a><span data-ttu-id="b91d2-115">Um sich die Arbeitsplatzgruppeneinträge anzeigen zu lassen:</span><span class="sxs-lookup"><span data-stu-id="b91d2-115">To view work center ledger entries</span></span>  
<span data-ttu-id="b91d2-116">Auf den Seiten **Arbeitsplatzgruppenkarte** und **Arbeitsplatzkarte** können Sie gebuchte Kapazität aufgrund der Informationen zu beendeten Fertigungsaufträgen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="b91d2-116">In the **Work Center Card** and **Machine Center Card** pages, you can view the posted capacities as a result of finished production orders.</span></span>    
1.  <span data-ttu-id="b91d2-117">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Arbeitsplatzgruppen** ein und wählen Sie dann den zugehörigen Link.</span><span class="sxs-lookup"><span data-stu-id="b91d2-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Work Centers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b91d2-118">Öffnen Sie die relevante Karte **Arbeitsplatzgruppe** aus der Liste, und wählen Sie die **Kapazitätsposten** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="b91d2-118">Open the relevant **Work Center** card from the list, and then choose the **Capacity Ledger Entries** action.</span></span>  

<span data-ttu-id="b91d2-119">Auf der Seite **Kapazitätsposten** werden die gebuchten Posten der Arbeitsplatzgruppe in der Reihenfolge der Buchungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b91d2-119">The **Capacity Ledger Entries** page displays the posted entries from the work center in the order they were posted.</span></span>   

## <a name="see-also"></a><span data-ttu-id="b91d2-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b91d2-120">See Also</span></span>  
<span data-ttu-id="b91d2-121">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="b91d2-121">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="b91d2-122">Produktion einrichten</span><span class="sxs-lookup"><span data-stu-id="b91d2-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="b91d2-123">[Planung](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="b91d2-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="b91d2-124">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="b91d2-124">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="b91d2-125">Einkauf</span><span class="sxs-lookup"><span data-stu-id="b91d2-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="b91d2-126">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b91d2-126">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
