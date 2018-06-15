---
title: "So geht's: Lagerbestand zwischen Lagerplätzen umlagern| Microsoft Docs"
description: "Beschreibt, wie vom Bestand von einem Bereich oder von einem Lager an einen anderen Ort umgebucht wird, entweder mit dem Umlagerungs Buch.-Blatt mit oder den Umlagerungsaufträgen."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 01/25/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 7c346455a9e27d7274b116754f1d594484b95d67
ms.openlocfilehash: 653fee8d327635f2e53a2f3c890f0b52649697f9
ms.contentlocale: de-de
ms.lasthandoff: 04/18/2018

---
# <a name="transfer-inventory-between-locations"></a><span data-ttu-id="e8955-103">Lagerbestand zwischen Lagerplätzen umlagern</span><span class="sxs-lookup"><span data-stu-id="e8955-103">Transfer Inventory Between Locations</span></span>
<span data-ttu-id="e8955-104">Sie können Bestandsartikel zwischen Lagerplätzen umlagern, indem Sie Umlagerungsaufträge erstellen.</span><span class="sxs-lookup"><span data-stu-id="e8955-104">You can transfer inventory items between locations by creating transfer orders.</span></span> <span data-ttu-id="e8955-105">Sie können auch das Einkaufs-Buch.-Blatt verwenden.</span><span class="sxs-lookup"><span data-stu-id="e8955-105">Alternatively, you can use the item reclassification journal.</span></span>

<span data-ttu-id="e8955-106">Bei Umlagerungsaufträgen senden Sie die ausgehende Umlagerung von einem Lagerplatz und empfangen die eingehende Umlagerung am anderen Lagerplatz.</span><span class="sxs-lookup"><span data-stu-id="e8955-106">With transfer orders, you ship the outbound transfer from one location and receive the inbound transfer at the other location.</span></span> <span data-ttu-id="e8955-107">Dies ermöglicht es Ihnen, die einbezogenen Lageraktivitäten zu verwalten und bietet mehr Sicherheit, dass Lagerbestandsmengen korrekt aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="e8955-107">This allows you to manage the involved warehouse activities and provides more certainty that inventory quantities are updated correctly.</span></span>

<span data-ttu-id="e8955-108">Mit dem Umlagerungs Buch.-Blatt füllen Sie einfach die Felder **Lagerortcode** und **Neuer Lagerortcode** aus.</span><span class="sxs-lookup"><span data-stu-id="e8955-108">With the reclassification journal, you simply fill in the **Location Code** and the **New Location Code** fields.</span></span> <span data-ttu-id="e8955-109">Wenn Sie das Buch.-Blatt buchen, werden die Artikelposten an den fraglichen Lagerplätzen reguliert.</span><span class="sxs-lookup"><span data-stu-id="e8955-109">When you post the journal, the item ledger entries are adjusted at the locations in question.</span></span> <span data-ttu-id="e8955-110">Mit dieser Methode werden Lageraktivitäten nicht verwaltet.</span><span class="sxs-lookup"><span data-stu-id="e8955-110">With this method, warehouse activities are not managed.</span></span>

> [!NOTE]  
>   <span data-ttu-id="e8955-111">Wenn Sie Artikel haben, die in Ihrem Lager ohne Lagerortcode erfasst sind, wie beispielsweise aus einer Zeit, als Sie nur ein Lager hatten, dann können Sie diejenigen Artikel nicht mithilfe von Umlagerungsaufträgen übertragen.</span><span class="sxs-lookup"><span data-stu-id="e8955-111">If you have items recorded in your inventory without a location code, for example from a time when you only had one warehouse, then you cannot transfer those items using transfer orders.</span></span> <span data-ttu-id="e8955-112">Stattdessen müssen Sie das Umlagerungs Buch.-Blatt verwenden, um die Artikel aus einem leeren Lagerortcode zu einem tatsächlichen Lagerortcode umzubuchen.</span><span class="sxs-lookup"><span data-stu-id="e8955-112">Instead, you must use the reclassification journal to reclassify the items from a blank location code to an actual location code.</span></span>  <span data-ttu-id="e8955-113">Weitere Informationen finden Sie Schritt 3 im "Artikel mit Abschnitt des Artikel Umlag. Buch.-Blattes übertragen".</span><span class="sxs-lookup"><span data-stu-id="e8955-113">For more information, see step 3 in the "To transfer items with the item reclassification journal" section.</span></span>

<span data-ttu-id="e8955-114">Um Artikel umzulagern, müssen Lagerplätze und Umlagerungsrouten eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="e8955-114">To transfer items, locations and transfer routes must be set up.</span></span> <span data-ttu-id="e8955-115">Weitere Informationen finden Sie unter [Einrichten von Lagerorten](inventory-how-setup-locations.md).</span><span class="sxs-lookup"><span data-stu-id="e8955-115">For more information, see [Set Up Locations](inventory-how-setup-locations.md).</span></span>

## <a name="to-transfer-items-with-a-transfer-order"></a><span data-ttu-id="e8955-116">So lagern Sie Artikel mit einem Umlagerungsauftrag um</span><span class="sxs-lookup"><span data-stu-id="e8955-116">To transfer items with a transfer order</span></span>
1. <span data-ttu-id="e8955-117">Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen ") aus und geben Sie **Umlagerungsaufträge** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="e8955-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Transfer orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="e8955-118">Füllen Sie im Fenster **Umlagerungsauftrag** die Felder nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="e8955-118">In the **Transfer Order** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   <span data-ttu-id="e8955-119">Wenn Sie die Felder **Umlag. in Code**, **Zustellercode** und **Zustellertransportartencode** im Fenster **Umlagerungsroutenspezifikation** ausgefüllt haben, als Sie die Umlagerungsrouten zwischen diesen Lagerorten eingerichtet haben, werden die entsprechenden Felder im Umlagerungsauftrag automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="e8955-119">If you have filled in the **In-Transit Code**, **Shipping Agent Code**, and **Shipping Agent Service** fields in the **Trans. Route Spec.** window when you set up the transfer route, then the corresponding fields on the transfer order are filled in automatically.</span></span>

    <span data-ttu-id="e8955-120">Wenn Sie das Feld **Zustellertransportarten** ausfüllen, wird das Zugangsdatum am Ziellagerplatz berechnet, indem Sie die Transportzeit der Zustellertransportart zum Lieferdatum hinzuaddieren.</span><span class="sxs-lookup"><span data-stu-id="e8955-120">When you fill in the **Shipping Agent Service** field, the receipt date at the transfer-to location is calculated by adding the shipping time of the shipping agent service to the shipment date.</span></span>

    <span data-ttu-id="e8955-121">Als Lagermitarbeiter am vom Umlagerungsort fahren sie fort, die Artikel auszuliefern.</span><span class="sxs-lookup"><span data-stu-id="e8955-121">As a warehouse worker at the transfer-from location, proceed to ship the items.</span></span>
3. <span data-ttu-id="e8955-122">Wählen Sie die Aktion **Buchen** aus, wählen Sie die Option **Warenausgang**, und wählen Sie dann die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="e8955-122">Choose the **Post** action, choose the **Ship** option, and then choose the **OK** button.</span></span>

    <span data-ttu-id="e8955-123">Die Artikel befinden sich jetzt in der Umlagerung zwischen den angegebenen Lagerplätzen, entsprechend der angegebenen Umlagerungsroute.</span><span class="sxs-lookup"><span data-stu-id="e8955-123">The items are now in transit between the specified locations, according to the specifies transfer route.</span></span>

    <span data-ttu-id="e8955-124">Als Lagermitarbeiter am vom Umlagerungsort fahren sie fort, die Artikel zu empfangen</span><span class="sxs-lookup"><span data-stu-id="e8955-124">As a warehouse worker at the transfer-from location, proceed to receive the items.</span></span>
4. <span data-ttu-id="e8955-125">Wählen Sie die Aktion **Buchen** aus, wählen Sie die Option **Eingang**, und wählen Sie dann die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="e8955-125">Choose the **Post** action, choose the **Receive** option, and then choose the **OK** button.</span></span>

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a><span data-ttu-id="e8955-126">So lagern Sie Artikel mit dem Artikel Umlag. Buch.-Blatt um</span><span class="sxs-lookup"><span data-stu-id="e8955-126">To transfer items with the item reclassification journal</span></span>
1. <span data-ttu-id="e8955-127">Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Artikel Buchblatt neu klassieren** ein und wählen den zugehörenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="e8955-127">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Reclass. Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="e8955-128">Füllen Sie im Fenster **Umlagerungs Buch.-Blatt** die notwendigen Felder aus.</span><span class="sxs-lookup"><span data-stu-id="e8955-128">In the **Item Reclass. Journal** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="e8955-129">Geben Sie im Feld **Lagerortcode** den Lagerplatz ein, an dem die Artikel aktuell gelagert sind.</span><span class="sxs-lookup"><span data-stu-id="e8955-129">In the **Location Code** field, enter the location where the items are currently stored.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="e8955-130">Um Artikel umzulagern die keinen Lagerortcode haben, belassen Sie das Feld **Lagerortcode** leer.</span><span class="sxs-lookup"><span data-stu-id="e8955-130">To transfer items that have no location code, leave the **Location Code** field blank.</span></span>
4. <span data-ttu-id="e8955-131">Im Feld **Neuer Lagerortcode** geben Sie den Lagerplatz ein, an den Sie die Artikel umlagern möchten.</span><span class="sxs-lookup"><span data-stu-id="e8955-131">In the **New Location Code** field, enter the location that you want to transfer the items to.</span></span>
5. <span data-ttu-id="e8955-132">Wählen Sie die Aktion **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="e8955-132">Choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8955-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8955-133">See Also</span></span>
[<span data-ttu-id="e8955-134">Verwalten des Lagerbestands</span><span class="sxs-lookup"><span data-stu-id="e8955-134">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="e8955-135">Einrichten von Lagerorten</span><span class="sxs-lookup"><span data-stu-id="e8955-135">Set Up Locations</span></span>](inventory-how-setup-locations.md)  
<span data-ttu-id="e8955-136">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e8955-136">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="e8955-137">Sie können auswählen, welche Funktionen angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="e8955-137">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="e8955-138">Allgemeine Geschäftsfunktionen</span><span class="sxs-lookup"><span data-stu-id="e8955-138">General Business Functionality</span></span>](ui-across-business-areas.md)

