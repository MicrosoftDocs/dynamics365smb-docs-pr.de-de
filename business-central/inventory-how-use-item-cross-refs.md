---
title: Artikelreferenzen verwenden
description: Richten Sie Referenzen zwischen den Beschreibungen ein, die Sie und Ihr Kreditor für einen Artikel verwenden, damit Sie die Artikelbeschreibung des Kreditors in Einkaufsbelege einfügen können.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0a9f84522598344435ad9c1263fe8cdea2e2a1e0
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785648"
---
# <a name="use-item-cross-references"></a><span data-ttu-id="5653a-103">Artikelreferenzen verwenden</span><span class="sxs-lookup"><span data-stu-id="5653a-103">Use Item Cross References</span></span>
<span data-ttu-id="5653a-104">Wenn Sie eine Artikelreferenzen zwischen der Artikelbeschreibung definieren, die Sie für den Artikel und die Beschreibung verwenden, die der Kreditor dieses Artikels verwendet, wird die Artikelbeschreibung des Kreditors automatisch auf Verkaufsbelegen für den Kreditor eingegeben, wenn Sie die **Referenznr.** ausfüllen</span><span class="sxs-lookup"><span data-stu-id="5653a-104">If you set up a cross reference between the item description that you use for an item and the description that the vendor of that item uses, then the vendor's item description is automatically inserted on purchase documents for the vendor when you fill in the **Cross-Reference No.**</span></span> <span data-ttu-id="5653a-105">Feld</span><span class="sxs-lookup"><span data-stu-id="5653a-105">field.</span></span> <span data-ttu-id="5653a-106">Dieselbe Funktionalität gilt für Debitorenartikelnummern in Verkaufsbelegen.</span><span class="sxs-lookup"><span data-stu-id="5653a-106">The same functionality applies for customer item numbers on sales documents.</span></span>

<span data-ttu-id="5653a-107">Die folgenden Verfahren beschreiben, wie Artikelreferenzen beim Einkauf verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5653a-107">The following procedures describe how to use item cross references on the purchase side.</span></span> <span data-ttu-id="5653a-108">Die Schritte sind für den Verkauf ähnlich.</span><span class="sxs-lookup"><span data-stu-id="5653a-108">The steps are similar for the sales side.</span></span>

> [!NOTE]
> <span data-ttu-id="5653a-109">Für Artikelbezeichner wie z. B. GTINs oder GUIDs wird es immer üblicher, dass sie mindestens 30 Zeichen enthalten, was mehr ist. als die aktuelle Funktion für Artikelquerverweise handhaben kann.</span><span class="sxs-lookup"><span data-stu-id="5653a-109">It's becoming more common for item identifiers such as GTINs or GUIDs to contain 30 or more characters, which is more than the current feature for item cross references can handle.</span></span> <span data-ttu-id="5653a-110">Wenn Sie Referenzen verwenden müssen, die mehr als 30 Zeichen enthalten, kann Ihr Administrator die Funktion **Längere Artikelreferenzen schreiben** auf der Seite [Funktionsverwaltung](https://businesscentral.dynamics.com/?page=2610) aktivieren (der Link erfordert, dass Sie einen [!INCLUDE[prod_short](includes/prod_short.md)]-Mandanten haben) aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5653a-110">If you need to use references that contain more than 30 characters, your administrator can turn on the **Write longer item references** feature on the [Feature Management](https://businesscentral.dynamics.com/?page=2610) page (link requires that you have a [!INCLUDE[prod_short](includes/prod_short.md)] tenant).</span></span> <span data-ttu-id="5653a-111">Die Verwendung von Referenzen ändert sich nicht, aber die Namen von Dingen wie Seiten und Schaltflächen ändern sich.</span><span class="sxs-lookup"><span data-stu-id="5653a-111">How you use references doesn't change, but the names of things like pages and buttons will.</span></span> <span data-ttu-id="5653a-112">Aus der Seite **Artikelquerverweisposten** wird beispielsweise die Seite **Artikelreferenzposten**.</span><span class="sxs-lookup"><span data-stu-id="5653a-112">For example, the **Item Cross-Reference Entries** page will become the **Item Reference Entries** page.</span></span>

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a><span data-ttu-id="5653a-113">Eine Artikelreferenz zur Artikelbeschreibung des Kreditor einrichten</span><span class="sxs-lookup"><span data-stu-id="5653a-113">To set up an item cross reference to a vendor's item description</span></span>

1. <span data-ttu-id="5653a-114">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Artikel** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="5653a-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="5653a-115">Öffnen Sie die Karte eines Artikels, für den Sie eine Referenz zur Artikelbeschreibung erstellen möchten, die der Kreditor für diesen Artikel verwendet.</span><span class="sxs-lookup"><span data-stu-id="5653a-115">Open the card for an item for which you want to create a cross reference to the item description that the vendor uses for that item.</span></span>
3. <span data-ttu-id="5653a-116">Wählen Sie die **Referenzen**-Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="5653a-116">Choose the **Cross References** action.</span></span>

     <span data-ttu-id="5653a-117">Wenn Sie die Aktion **Querverweise** nicht finden können, wählen Sie die Anzeige weiterer Optionen aus, und suchen Sie diese unter **Verknüpft** > **Artikel**.</span><span class="sxs-lookup"><span data-stu-id="5653a-117">If you cannot find the **Cross References** action, choose to view more options, and then find it under **Related** > **Item**.</span></span>
  
4. <span data-ttu-id="5653a-118">In einer neuen Zeile auf der Seite **Artikelreferenzposten** füllen Sie die Felder wie notwendig aus.</span><span class="sxs-lookup"><span data-stu-id="5653a-118">On a new line on the **Item Cross-Reference Entries** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="5653a-119">.</span><span class="sxs-lookup"><span data-stu-id="5653a-119">.</span></span>

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a><span data-ttu-id="5653a-120">So geben Sie die Artikelbeschreibung eines Kreditors auf einer Einkaufsbestellung ein</span><span class="sxs-lookup"><span data-stu-id="5653a-120">To enter a vendor's item description on a purchase order</span></span>

1. <span data-ttu-id="5653a-121">Wählen Sie die ![Glühbirne, die das Tell Me Feature öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Bestellungen** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="5653a-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="5653a-122">Erstellen Sie eine Bestellung für den Kreditor, für den Sie im vorherigen Verfahren eine Artikelreferenz eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="5653a-122">Create a purchase order for the vendor that you set up an item cross reference for in the previous procedure.</span></span>
3. <span data-ttu-id="5653a-123">Erstellen Sie eine Einkaufszeile für den Artikel, für den Sie im vorherigen Verfahren eine Artikelreferenz eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="5653a-123">Create a purchase line for the item that you set up an item cross reference for in the previous procedure.</span></span>
4. <span data-ttu-id="5653a-124">Wählen Sie im Feld **Referenznr.**</span><span class="sxs-lookup"><span data-stu-id="5653a-124">In the **Cross-Reference No.**</span></span> <span data-ttu-id="5653a-125">die Artikelreferenz aus, die Sie erstellt haben, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="5653a-125">field, select the item cross reference that you have created, and then choose the **OK** button.</span></span>

<span data-ttu-id="5653a-126">Das Feld **Beschreibung** in der Zeile wird mit der Artikelbeschreibung des Kreditors überschrieben, wie im Artikelreferenzposten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5653a-126">The **Description** field on the line is overwritten with the vendor's item description, as set up on the item cross-reference entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="5653a-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5653a-127">See Also</span></span>
[<span data-ttu-id="5653a-128">Neue Artikel registrieren</span><span class="sxs-lookup"><span data-stu-id="5653a-128">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="5653a-129">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="5653a-129">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="5653a-130">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5653a-130">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]