---
title: Einrichten einer Lagerortkarte und definieren von Umlagerungsrouten| Microsoft Docs
description: Sie stellen eine Lagerortkarte für jedes Bundesland, den von Lagerartikel speichern, beispielsweise, ein Lager oder eine Vertriebsstelle und Einrichtungsrouten, um Artikel zwischen Lagerorten umlagern erstellen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 10/01/2019
ms.author: SorenGP
ms.openlocfilehash: 5554bb1576705cd1f3cbcddc7ef33da7b5db3796
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2878314"
---
# <a name="set-up-locations"></a><span data-ttu-id="b867a-103">Einrichten von Lagerorten</span><span class="sxs-lookup"><span data-stu-id="b867a-103">Set Up Locations</span></span>
<span data-ttu-id="b867a-104">Wenn Sie Artikel a mehr als einem Ort oder Lagerort kaufen, lagern oder verkaufen, müssen Sie jeden Lagerplatz mit einer Lagerortkarte einrichten und Umlagerungsrouten definieren.</span><span class="sxs-lookup"><span data-stu-id="b867a-104">If you buy, store, or sell items at more than one place or warehouse, you must set each location up with a location card and define transfer routes.</span></span>

<span data-ttu-id="b867a-105">Sie können dann Belegzeilen für einen bestimmten Lagerplatz erstellen, Verfügbarkeit nach Lagerplatz anzeigen und Lagerbestand zwischen Lagerplätzen umlagern.</span><span class="sxs-lookup"><span data-stu-id="b867a-105">You can then create document lines for a specific location, view availability by location, and transfer inventory between locations.</span></span> <span data-ttu-id="b867a-106">Weitere Informationen finden Sie unter [Lagerbestand verwalten](inventory-manage-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="b867a-106">For more information, see [Manage Inventory](inventory-manage-inventory.md).</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq]

## <a name="to-create-a-location-card"></a><span data-ttu-id="b867a-107">So erstellen Sie eine Lagerortkarte</span><span class="sxs-lookup"><span data-stu-id="b867a-107">To create a location card</span></span>
1. <span data-ttu-id="b867a-108">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Lagerorte** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="b867a-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="b867a-109">Wählen Sie die Aktion **Neu**.</span><span class="sxs-lookup"><span data-stu-id="b867a-109">Choose the **New** action.</span></span>
3. <span data-ttu-id="b867a-110">Füllen Sie auf der Seite **Lagerortkarte** die Felder nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="b867a-110">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="b867a-111">Wiederholen Sie die Schritte 2 und 3 für jeden Lagerplatz, an dem Sie Lagerbestand aufbewahren möchten.</span><span class="sxs-lookup"><span data-stu-id="b867a-111">Repeat steps 2 and 3 for every location where you want to keep inventory.</span></span>

> [!NOTE]  
> <span data-ttu-id="b867a-112">Viele Felder auf der Lagerortkarte beziehen sich auf Auftragsabwicklung von Artikel in eingehenden und ausgehenden Lagerprozessen.</span><span class="sxs-lookup"><span data-stu-id="b867a-112">Many fields on the location card refer to the handling of items in inbound and outbound warehouse processes.</span></span> <span data-ttu-id="b867a-113">Weitere Informationen finden Sie unter [Lagerortverwaltung einrichten](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="b867a-113">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

## <a name="to-create-a-transfer-route"></a><span data-ttu-id="b867a-114">So erstellen Sie eine Umlagerungsroute</span><span class="sxs-lookup"><span data-stu-id="b867a-114">To create a transfer route</span></span>
1. <span data-ttu-id="b867a-115">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Umlagerungsrouten** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="b867a-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer Routes**, and then choose the related link.</span></span>
2. <span data-ttu-id="b867a-116">Wählen Sie von jedem beliebigen Fenster **Standortkarten** die Aktion **Umlagerungsrouten** aus.</span><span class="sxs-lookup"><span data-stu-id="b867a-116">Alternatively, from any **Location Card** page, choose the **Transfer Routes** action.</span></span>
3. <span data-ttu-id="b867a-117">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="b867a-117">Choose the **New** action.</span></span>
4. <span data-ttu-id="b867a-118">Füllen Sie auf der Seite **Lagerortkarte** die Felder nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="b867a-118">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="b867a-119">Sie können jetzt die Lagerartikel zwischen zwei Lagerplätzen umlagern.</span><span class="sxs-lookup"><span data-stu-id="b867a-119">You can now transfer inventory items between two locations.</span></span> <span data-ttu-id="b867a-120">Weitere Informationen finden Sie unter [Lagerbestand zwischen Lagerplätzen umlagern](inventory-how-transfer-between-locations.md).</span><span class="sxs-lookup"><span data-stu-id="b867a-120">For more information, see [Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md).</span></span>    

## <a name="see-also"></a><span data-ttu-id="b867a-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b867a-121">See Also</span></span>
[<span data-ttu-id="b867a-122">Verwalten des Lagerbestands</span><span class="sxs-lookup"><span data-stu-id="b867a-122">Manage Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="b867a-123">[Lagerbestand zwischen Lagerplätzen umlagern](inventory-how-transfer-between-locations.md)  </span><span class="sxs-lookup"><span data-stu-id="b867a-123">[Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md)  </span></span>  
<span data-ttu-id="b867a-124">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b867a-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="b867a-125">Ändern, welche Merkmale angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="b867a-125">Change Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="b867a-126">Allgemeine Geschäftsfunktionen</span><span class="sxs-lookup"><span data-stu-id="b867a-126">General Business Functionality</span></span>](ui-across-business-areas.md)
