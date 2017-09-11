---
title: Einrichten einer Lagerortkarte und definieren von Umlagerungsrouten| Microsoft Docs
description: "Sie stellen eine Lagerortkarte für jedes Bundesland, den von Lagerartikel speichern, beispielsweise, ein Lager oder eine Vertriebsstelle und Einrichtungsrouten, um Artikel zwischen Lagerorten umlagern erstellen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 146fc08f389a5c068044358c59b7d8911f0b3343
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-set-up-locations"></a><span data-ttu-id="b0237-103">So wird's gemacht: Standorte einrichten</span><span class="sxs-lookup"><span data-stu-id="b0237-103">How to: Set Up Locations</span></span>
<span data-ttu-id="b0237-104">Wenn Sie Artikel a mehr als einem Ort oder Lagerort kaufen, lagern oder verkaufen, müssen Sie jeden Lagerplatz mit einer Lagerortkarte einrichten und Umlagerungsrouten definieren.</span><span class="sxs-lookup"><span data-stu-id="b0237-104">If you buy, store, or sell items at more than one place or warehouse, you must set each location up with a location card and define transfer routes.</span></span>

<span data-ttu-id="b0237-105">Sie können dann Belegzeilen für einen bestimmten Lagerplatz erstellen, Verfügbarkeit nach Lagerplatz anzeigen und Lagerbestand zwischen Lagerplätzen umlagern.</span><span class="sxs-lookup"><span data-stu-id="b0237-105">You can then create document lines for a specific location, view availability by location, and transfer inventory between locations.</span></span> <span data-ttu-id="b0237-106">Weitere Informationen finden Sie unter [Lagerbestand verwalten](inventory-manage-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="b0237-106">For more information, see [Manage Inventory](inventory-manage-inventory.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="b0237-107">Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="b0237-107">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="b0237-108">Weitere Informationen finden Sie unter [Anpassen Ihrer [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)Experience.</span><span class="sxs-lookup"><span data-stu-id="b0237-108">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-create-a-location-card"></a><span data-ttu-id="b0237-109">So erstellen Sie eine Lagerortkarte</span><span class="sxs-lookup"><span data-stu-id="b0237-109">To create a location card</span></span>
1. <span data-ttu-id="b0237-110">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Lagerplätze** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="b0237-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="b0237-111">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="b0237-111">Choose the **New** action.</span></span>
3. <span data-ttu-id="b0237-112">Füllen Sie im Fenster **Lagerortkarte** die Felder nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="b0237-112">In the **Location Card** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="b0237-113">Wiederholen Sie die Schritte 2 und 3 für jeden Lagerplatz, an dem Sie Lagerbestand aufbewahren möchten.</span><span class="sxs-lookup"><span data-stu-id="b0237-113">Repeat steps 2 and 3 for every location where you want to keep inventory.</span></span>

## <a name="to-create-a-transfer-route"></a><span data-ttu-id="b0237-114">So erstellen Sie eine Umlagerungsroute</span><span class="sxs-lookup"><span data-stu-id="b0237-114">To create a transfer route</span></span>
1. <span data-ttu-id="b0237-115">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Lagerplätze** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="b0237-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Transfer Routes**, and then choose the related link.</span></span>
2. <span data-ttu-id="b0237-116">Alternativ wählen Sie von jedem beliebigen Fenster **Standortkarten** die Aktion **Umlagerungsrouten** aus.</span><span class="sxs-lookup"><span data-stu-id="b0237-116">Alternatively, from any **Location Card** window, choose the **Transfer Routes** action.</span></span>
3. <span data-ttu-id="b0237-117">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="b0237-117">Choose the **New** action.</span></span>
4. <span data-ttu-id="b0237-118">Füllen Sie im Fenster **Lagerortkarte** die Felder nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="b0237-118">In the **Location Card** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="b0237-119">Sie können jetzt die Lagerartikel zwischen zwei Lagerplätzen umlagern.</span><span class="sxs-lookup"><span data-stu-id="b0237-119">You can now transfer inventory items between two locations.</span></span> <span data-ttu-id="b0237-120">Weitere Informationen finden Sie unter [So geht's: Lagerbestand zwischen Lagerplätzen umlagern](inventory-how-transfer-between-locations.md).</span><span class="sxs-lookup"><span data-stu-id="b0237-120">For more information, see [How to: Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md).</span></span>    

## <a name="see-also"></a><span data-ttu-id="b0237-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0237-121">See Also</span></span>
[<span data-ttu-id="b0237-122">Verwalten des Lagerbestands</span><span class="sxs-lookup"><span data-stu-id="b0237-122">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="b0237-123">Lieferkette</span><span class="sxs-lookup"><span data-stu-id="b0237-123">Supply Chain</span></span>](madeira-supply-chain.md)  
<span data-ttu-id="b0237-124">[So geht's: Lagerbestand zwischen Lagerplätzen umlagern](inventory-how-transfer-between-locations.md)  </span><span class="sxs-lookup"><span data-stu-id="b0237-124">[How to: Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md)  </span></span>  
<span data-ttu-id="b0237-125">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b0237-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="b0237-126">[Anpassen der[!INCLUDE[d365fin](includes/d365fin_md.md)]Erfahrung](ui-experiences.md)</span><span class="sxs-lookup"><span data-stu-id="b0237-126">[Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md)</span></span>  
[<span data-ttu-id="b0237-127">Allgemeine Geschäftsfunktionen</span><span class="sxs-lookup"><span data-stu-id="b0237-127">General Business Functionality</span></span>](ui-across-business-areas.md)

