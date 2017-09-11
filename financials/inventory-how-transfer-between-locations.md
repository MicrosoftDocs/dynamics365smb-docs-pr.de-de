---
title: "So geht's: Lagerbestand zwischen Lagerplätzen umlagern| Microsoft Docs"
description: "Beschreibt, wie vom Bestand von einem Bereich oder von einem Lager an einen anderen Ort umgebucht wird, entweder mit dem Umlagerungs Buch.-Blatt mit oder den Umlagerungsaufträgen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d54b75240cb0a2dddcfabc488a18e0bf9635f82c
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-transfer-inventory-between-locations"></a><span data-ttu-id="c4216-103">So geht's: Lagerbestand zwischen Lagerplätzen umlagern</span><span class="sxs-lookup"><span data-stu-id="c4216-103">How to: Transfer Inventory Between Locations</span></span>
<span data-ttu-id="c4216-104">Sie können Bestandsartikel zwischen Lagerplätzen umlagern, indem Sie Umlagerungsaufträge erstellen.</span><span class="sxs-lookup"><span data-stu-id="c4216-104">You can transfer inventory items between locations by creating transfer orders.</span></span> <span data-ttu-id="c4216-105">Sie können auch das Einkaufs-Buch.-Blatt verwenden.</span><span class="sxs-lookup"><span data-stu-id="c4216-105">Alternatively, you can use the item reclassification journal.</span></span>

<span data-ttu-id="c4216-106">Bei Umlagerungsaufträgen senden Sie die ausgehende Umlagerung von einem Lagerplatz und empfangen die eingehende Umlagerung am anderen Lagerplatz.</span><span class="sxs-lookup"><span data-stu-id="c4216-106">With transfer orders, you ship the outbound transfer from one location and receive the inbound transfer at the other location.</span></span> <span data-ttu-id="c4216-107">Dies ermöglicht es Ihnen, die einbezogenen Lageraktivitäten zu verwalten und bietet mehr Sicherheit, dass Lagerbestandsmengen korrekt aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c4216-107">This allows you to manage the involved warehouse activities and provides more certainty that inventory quantities are updated correctly.</span></span>

<span data-ttu-id="c4216-108">Mit dem Umlagerungs Buch.-Blatt füllen Sie einfach die Felder **Lagerortcode** und **Neuer Lagerortcode** aus.</span><span class="sxs-lookup"><span data-stu-id="c4216-108">With the reclassification journal, you simply fill in the **Location Code** and the **New Location Code** fields.</span></span> <span data-ttu-id="c4216-109">Wenn Sie das Buch.-Blatt buchen, werden die Artikelposten an den fraglichen Lagerplätzen reguliert.</span><span class="sxs-lookup"><span data-stu-id="c4216-109">When you post the journal, the item ledger entries are adjusted at the locations in question.</span></span> <span data-ttu-id="c4216-110">Mit dieser Methode werden Lageraktivitäten nicht verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c4216-110">With this method, warehouse activities are not managed.</span></span>

> [!NOTE]  
>   <span data-ttu-id="c4216-111">Wenn Sie Artikel haben, die in Ihrem Lager ohne Lagerortcode erfasst sind, wie beispielsweise aus einer Zeit, als Sie nur ein Lager hatten, dann können Sie diejenigen Artikel nicht mithilfe von Umlagerungsaufträgen übertragen.</span><span class="sxs-lookup"><span data-stu-id="c4216-111">If you have items recorded in your inventory without a location code, for example from a time when you only had one warehouse, then you cannot transfer those items using transfer orders.</span></span> <span data-ttu-id="c4216-112">Stattdessen müssen Sie das Umlagerungs Buch.-Blatt verwenden, um die Artikel aus einem leeren Lagerortcode zu einem tatsächlichen Lagerortcode umzubuchen.</span><span class="sxs-lookup"><span data-stu-id="c4216-112">Instead, you must use the reclassification journal to reclassify the items from a blank location code to an actual location code.</span></span>  <span data-ttu-id="c4216-113">Weitere Informationen finden Sie Schritt 3 im "Artikel mit Abschnitt des Artikel Umlag. Buch.-Blattes übertragen".</span><span class="sxs-lookup"><span data-stu-id="c4216-113">For more information, see step 3 in the "To transfer items with the item reclassification journal" section.</span></span>

<span data-ttu-id="c4216-114">Um Artikel umzulagern, müssen Lagerplätze und Umlagerungsrouten eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="c4216-114">To transfer items, locations and transfer routes must be set up.</span></span> <span data-ttu-id="c4216-115">Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Lagerplätzen](inventory-how-setup-locations.md).</span><span class="sxs-lookup"><span data-stu-id="c4216-115">For more information, see [How to: Set Up Locations](inventory-how-setup-locations.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="c4216-116">Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="c4216-116">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="c4216-117">Weitere Informationen finden Sie unter [Anpassen Ihrer [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)Experience.</span><span class="sxs-lookup"><span data-stu-id="c4216-117">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-transfer-items-with-a-transfer-order"></a><span data-ttu-id="c4216-118">So lagern Sie Artikel mit einem Umlagerungsauftrag um</span><span class="sxs-lookup"><span data-stu-id="c4216-118">To transfer items with a transfer order</span></span>
1. <span data-ttu-id="c4216-119">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen ")aus und geben Sie **Umlagerungsaufträge** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="c4216-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Transfer orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="c4216-120">Füllen Sie im Fenster **Umlagerungsauftrag** die Felder nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="c4216-120">In the **Transfer Order** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
>   <span data-ttu-id="c4216-121">Wenn Sie die Felder **In Transit Code**, **Zustellercode** und **Zustellertransportart** im Fenster **Umlagerungsroutenspezifikation** ausgefüllt haben,</span><span class="sxs-lookup"><span data-stu-id="c4216-121">If you have filled in the **In-Transit Code**, **Shipping Agent Code**, and **Shipping Agent Service** fields in the **Trans. Route Spec.**</span></span> <span data-ttu-id="c4216-122">wenn Sie die Umlagerungsroute einrichten, werden die entsprechenden Felder im Umlagerungsauftrag automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="c4216-122">window when you set up the transfer route, then the corresponding fields on the transfer order are filled in automatically.</span></span>

    <span data-ttu-id="c4216-123">Wenn Sie das Feld **Zustellertransportarten** ausfüllen, wird das Zugangsdatum am Ziellagerplatz berechnet, indem Sie die Transportzeit der Zustellertransportart zum Lieferdatum hinzuaddieren.</span><span class="sxs-lookup"><span data-stu-id="c4216-123">When you fill in the **Shipping Agent Service** field, the receipt date at the transfer-to location is calculated by adding the shipping time of the shipping agent service to the shipment date.</span></span>

    <span data-ttu-id="c4216-124">Als Lagermitarbeiter am vom Umlagerungsort fahren sie fort, die Artikel auszuliefern.</span><span class="sxs-lookup"><span data-stu-id="c4216-124">As a warehouse worker at the transfer-from location, proceed to ship the items.</span></span>
3. <span data-ttu-id="c4216-125">Wählen Sie die Aktion **Buchen** aus, wählen Sie die Option **Warenausgang**, und wählen Sie dann die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="c4216-125">Choose the **Post** action, choose the **Ship** option, and then choose the **OK** button.</span></span>

    <span data-ttu-id="c4216-126">Die Artikel befinden sich jetzt in der Umlagerung zwischen den angegebenen Lagerplätzen, entsprechend der angegebenen Umlagerungsroute.</span><span class="sxs-lookup"><span data-stu-id="c4216-126">The items are now in transit between the specified locations, according to the specifies transfer route.</span></span>

    <span data-ttu-id="c4216-127">Als Lagermitarbeiter am vom Umlagerungsort fahren sie fort, die Artikel zu empfangen</span><span class="sxs-lookup"><span data-stu-id="c4216-127">As a warehouse worker at the transfer-from location, proceed to receive the items.</span></span>
4. <span data-ttu-id="c4216-128">Wählen Sie die Aktion **Buchen** aus, wählen Sie die Option **Eingang**, und wählen Sie dann die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="c4216-128">Choose the **Post** action, choose the **Receive** option, and then choose the **OK** button.</span></span>

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a><span data-ttu-id="c4216-129">So lagern Sie Artikel mit dem Artikel Umlag. Buch.-Blatt um</span><span class="sxs-lookup"><span data-stu-id="c4216-129">To transfer items with the item reclassification journal</span></span>
1. <span data-ttu-id="c4216-130">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Artikel Buchblatt neu klassieren** ein und wählen den zugehörenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="c4216-130">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Reclass. Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="c4216-131">Füllen Sie im Fenster **Umlagerungs Buch.-Blatt** die notwendigen Felder aus.</span><span class="sxs-lookup"><span data-stu-id="c4216-131">In the **Item Reclass. Journal** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="c4216-132">Geben Sie im Feld **Lagerortcode** den Lagerplatz ein, an dem die Artikel aktuell gelagert sind.</span><span class="sxs-lookup"><span data-stu-id="c4216-132">In the **Location Code** field, enter the location where the items are currently stored.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="c4216-133">Um Artikel umzulagern die keinen Lagerortcode haben, belassen Sie das Feld **Lagerortcode** leer.</span><span class="sxs-lookup"><span data-stu-id="c4216-133">To transfer items that have no location code, leave the **Location Code** field blank.</span></span>
4. <span data-ttu-id="c4216-134">Im Feld **Neuer Lagerortcode** geben Sie den Lagerplatz ein, an den Sie die Artikel umlagern möchten.</span><span class="sxs-lookup"><span data-stu-id="c4216-134">In the **New Location Code** field, enter the location that you want to transfer the items to.</span></span>
5. <span data-ttu-id="c4216-135">Wählen Sie die Aktion **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="c4216-135">Choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="c4216-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4216-136">See Also</span></span>
[<span data-ttu-id="c4216-137">Verwalten des Lagerbestands</span><span class="sxs-lookup"><span data-stu-id="c4216-137">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="c4216-138">So wird's gemacht: Standorte einrichten</span><span class="sxs-lookup"><span data-stu-id="c4216-138">How to: Set Up Locations</span></span>](inventory-how-setup-locations.md)  
[<span data-ttu-id="c4216-139">Lieferkette</span><span class="sxs-lookup"><span data-stu-id="c4216-139">Supply Chain</span></span>](madeira-supply-chain.md)  
<span data-ttu-id="c4216-140">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c4216-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="c4216-141">[Anpassen der[!INCLUDE[d365fin](includes/d365fin_md.md)]Erfahrung](ui-experiences.md)</span><span class="sxs-lookup"><span data-stu-id="c4216-141">[Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md)</span></span>  
[<span data-ttu-id="c4216-142">Allgemeine Geschäftsfunktionen</span><span class="sxs-lookup"><span data-stu-id="c4216-142">General Business Functionality</span></span>](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
