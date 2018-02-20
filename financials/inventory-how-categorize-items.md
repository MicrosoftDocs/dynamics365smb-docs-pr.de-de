---
title: Kategorisieren Sie Artikel| Microsoft Docs
description: "Um Artikel zu finden, können Sie Artikelattribute zuweisen und Artikel nach den definierten Kategorien organisieren."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 64511e0979671d13740bd18d95d53e8e37564583
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="categorize-items"></a><span data-ttu-id="71f47-103">Artikel kategorisieren</span><span class="sxs-lookup"><span data-stu-id="71f47-103">Categorize Items</span></span>
<span data-ttu-id="71f47-104">Um eine Übersicht über Ihre Artikel zu verwalten und das Sortieren und Finden von Artikeln zu erleichtern, ist es nützlich, Ihre Artikel in Artikelkategorien zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="71f47-104">To maintain an overview of your items and to help you sort and find items, it is useful to organize your items in item categories.</span></span>

<span data-ttu-id="71f47-105">Um Artikel nach Eigenschaften zu finden, können Sie Artikelattribute Artikeln und auch Artikelkategorien zuordnen.</span><span class="sxs-lookup"><span data-stu-id="71f47-105">To find items by characteristics, you can assign item attributes to items and also to item categories.</span></span> <span data-ttu-id="71f47-106">Weitere Informationen finden Sie unter [Arbeiten mit Artikelattributen](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="71f47-106">For more information, see [Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>

## <a name="to-create-an-item-category"></a><span data-ttu-id="71f47-107">So erstellen Sie eine Artikelkategorie</span><span class="sxs-lookup"><span data-stu-id="71f47-107">To create an item category</span></span>
1. <span data-ttu-id="71f47-108">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Artikelkategorien** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="71f47-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Categories**, and then choose the related link.</span></span>
2. <span data-ttu-id="71f47-109">Wählen Sie im Fenster **Artikelkategorie** die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="71f47-109">In the **Item Categories** window, choose the **New** action.</span></span>
3. <span data-ttu-id="71f47-110">Füllen Sie im Fenster **Artikelkategorienkarte** im Inforegister **Allgemein** die notwendigen Felder aus.</span><span class="sxs-lookup"><span data-stu-id="71f47-110">In the **Item Category Card** window, on the **General** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="71f47-111">Geben Sie im Inforegister **Attribute** alle Artikelattribute für die Artikelkategorie an.</span><span class="sxs-lookup"><span data-stu-id="71f47-111">On the **Attributes** FastTab, specify any item attributes for the item category.</span></span> <span data-ttu-id="71f47-112">Weitere Informationen finden Sie im Abschnitt "So weisen Sie Artikelattribute Artikelkategorien zu" in [Arbeiten mit Artikelattributen](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="71f47-112">For more information, see the "To assign item attributes to an item category" section in [Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="71f47-113">Hinweis: Wenn die Artikelkategorie eine übergeordnete Artikelkategorie besitzt, wie durch das Feld **Übergeordnete Kategorie** angegeben, werden alle Artikelattribute, die dieser übergeordneten Artikelkategorie zugewiesen sind, im Inforegister **Attribute** bereits eingetragen.</span><span class="sxs-lookup"><span data-stu-id="71f47-113">If the item category has a parent item category, as indicated by the **Parent Category** field, then any item attributes that are assigned to that parent item category are prefilled on the **Attributes** FastTab.</span></span>

> [!NOTE]  
>   <span data-ttu-id="71f47-114">Artikelattribute, die Sie einer Artikelkategorie zuordnen, werden automatisch auf den Artikel angewendet, der der Artikelkategorie zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="71f47-114">Item attributes that you assign to an item category will automatically apply to the item that the item category is assigned to.</span></span>

## <a name="to-assign-an-item-category-to-an-item"></a><span data-ttu-id="71f47-115">So ordnen Sie eine Artikelkategorie einem Artikel zu</span><span class="sxs-lookup"><span data-stu-id="71f47-115">To assign an item category to an item</span></span>
1. <span data-ttu-id="71f47-116">Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen") aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="71f47-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="71f47-117">Öffnen Sie die Karte des Artikels, den Sie einer Artikelkategorie zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="71f47-117">Open the card for the item that you want to assign to an item category.</span></span>
3. <span data-ttu-id="71f47-118">Klicken Sie im Feld **Artikelkategoriencode** auf die Schaltfläche suchen und wählen Sie eine bereits vorhandene Artikelkategorie aus.</span><span class="sxs-lookup"><span data-stu-id="71f47-118">Choose the lookup button in the **Item Category Code** field and select an existing item category.</span></span> <span data-ttu-id="71f47-119">Wählen Sie die Aktion **Neu**, um zuerst eine neue Artikelkategorie so zu erstellen, wie es im Abschnitt "So erstellen Sie eine Artikelkategorie" erklärt wird.</span><span class="sxs-lookup"><span data-stu-id="71f47-119">Alternatively, choose the **New** action to first create a new item category as explained in the "To create an item category" section.</span></span>

## <a name="see-also"></a><span data-ttu-id="71f47-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71f47-120">See Also</span></span>
[<span data-ttu-id="71f47-121">Arbeiten mit Artikelattributen</span><span class="sxs-lookup"><span data-stu-id="71f47-121">Work with Item Attributes</span></span>](inventory-how-work-item-attributes.md)  
[<span data-ttu-id="71f47-122">Neue Artikel registrieren</span><span class="sxs-lookup"><span data-stu-id="71f47-122">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="71f47-123">Lagerbest</span><span class="sxs-lookup"><span data-stu-id="71f47-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="71f47-124">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="71f47-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

