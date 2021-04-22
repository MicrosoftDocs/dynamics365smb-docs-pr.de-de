---
title: Kategorisieren Sie Artikel| Microsoft Docs
description: Um Artikel zu finden, können Sie Artikelattribute zuweisen und Artikel nach den definierten Kategorien organisieren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 55196b8026e5efc5a79ce1a547e2ff594fae231c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786023"
---
# <a name="categorize-items"></a><span data-ttu-id="24d76-103">Artikel kategorisieren</span><span class="sxs-lookup"><span data-stu-id="24d76-103">Categorize Items</span></span>

<span data-ttu-id="24d76-104">Um eine Übersicht über Ihre Artikel zu verwalten und das Sortieren und Finden von Artikeln zu erleichtern, ist es nützlich, Ihre Artikel in Artikelkategorien zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="24d76-104">To maintain an overview of your items and to help you sort and find items, it is useful to organize your items in item categories.</span></span>

<span data-ttu-id="24d76-105">Um Artikel nach Eigenschaften zu finden, können Sie Artikelattribute Artikeln und auch Artikelkategorien zuordnen.</span><span class="sxs-lookup"><span data-stu-id="24d76-105">To find items by characteristics, you can assign item attributes to items and also to item categories.</span></span> <span data-ttu-id="24d76-106">Weitere Informationen finden Sie unter [Arbeiten mit Artikelattributen](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="24d76-106">For more information, see [Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4j4mo?rel=0]

## <a name="to-create-an-item-category"></a><span data-ttu-id="24d76-107">So erstellen Sie eine Artikelkategorie</span><span class="sxs-lookup"><span data-stu-id="24d76-107">To create an item category</span></span>
1. <span data-ttu-id="24d76-108">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Artikelkategorien** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="24d76-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Categories**, and then choose the related link.</span></span>
2. <span data-ttu-id="24d76-109">Wählen Sie auf der Seite **Artikelkategorien** die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="24d76-109">On the **Item Categories** page, choose the **New** action.</span></span>
3. <span data-ttu-id="24d76-110">Füllen Sie auf der Seite **Artikelkategorienkarte** im Inforegister **Allgemein** die notwendigen Felder aus.</span><span class="sxs-lookup"><span data-stu-id="24d76-110">On the **Item Category Card** page, on the **General** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="24d76-111">Geben Sie im Inforegister **Attribute** alle Artikelattribute für die Artikelkategorie an.</span><span class="sxs-lookup"><span data-stu-id="24d76-111">On the **Attributes** FastTab, specify any item attributes for the item category.</span></span> <span data-ttu-id="24d76-112">Weitere Informationen finden Sie unter [So ordnen Sie ein Artikelattribut einer Artikelkategorie zu](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).</span><span class="sxs-lookup"><span data-stu-id="24d76-112">For more information, see [To assign item attributes to item categories](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).</span></span>

> [!NOTE]  
> <span data-ttu-id="24d76-113">Hinweis: Wenn die Artikelkategorie eine übergeordnete Artikelkategorie besitzt, wie durch das Feld **Übergeordnete Kategorie** angegeben, werden alle Artikelattribute, die dieser übergeordneten Artikelkategorie zugewiesen sind, im Inforegister **Attribute** bereits eingetragen.</span><span class="sxs-lookup"><span data-stu-id="24d76-113">If the item category has a parent item category, as indicated by the **Parent Category** field, then any item attributes that are assigned to that parent item category are prefilled on the **Attributes** FastTab.</span></span>

> [!NOTE]  
> <span data-ttu-id="24d76-114">Artikelattribute, die Sie einer Artikelkategorie zuordnen, werden automatisch auf den Artikel angewendet, der der Artikelkategorie zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="24d76-114">Item attributes that you assign to an item category will automatically apply to the item that the item category is assigned to.</span></span>

<span data-ttu-id="24d76-115">Wenn Sie Ihre Meinung zu einer Artikelkategorie ändern, können Sie sie löschen.</span><span class="sxs-lookup"><span data-stu-id="24d76-115">If you change your mind about an item category, you can delete it.</span></span> <span data-ttu-id="24d76-116">Wenn sie jedoch bereits einem Artikel zugewiesen wurde, müssen Sie diese Zuweisung entfernen, bevor Sie die Artikelkategorie löschen können.</span><span class="sxs-lookup"><span data-stu-id="24d76-116">However, if it has already been assigned to an item, you must remove that assignment before you can delete the item category.</span></span>

## <a name="to-assign-an-item-category-to-an-item"></a><span data-ttu-id="24d76-117">So ordnen Sie eine Artikelkategorie einem Artikel zu</span><span class="sxs-lookup"><span data-stu-id="24d76-117">To assign an item category to an item</span></span>

1. <span data-ttu-id="24d76-118">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Artikel** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="24d76-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="24d76-119">Öffnen Sie die Karte des Artikels, den Sie einer Artikelkategorie zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="24d76-119">Open the card for the item that you want to assign to an item category.</span></span>
3. <span data-ttu-id="24d76-120">Klicken Sie im Feld **Artikelkategoriencode** auf die Schaltfläche suchen und wählen Sie eine bereits vorhandene Artikelkategorie aus.</span><span class="sxs-lookup"><span data-stu-id="24d76-120">Choose the lookup button in the **Item Category Code** field and select an existing item category.</span></span> <span data-ttu-id="24d76-121">Alternativ wählen Sie die Aktion **Neu**, um zuerst eine neue Artikelkategorie so zu erstellen, wie es unter [So erstellen Sie eine Artikelkategorie](inventory-how-categorize-items.md#to-create-an-item-category) erklärt wird.</span><span class="sxs-lookup"><span data-stu-id="24d76-121">Alternatively, choose the **New** action to first create a new item category as explained in [To create an item category](inventory-how-categorize-items.md#to-create-an-item-category).</span></span>

## <a name="categories-attributes-and-variants"></a><span data-ttu-id="24d76-122">Kategorien, Attribute und Varianten</span><span class="sxs-lookup"><span data-stu-id="24d76-122">Categories, attributes, and variants</span></span>

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-also"></a><span data-ttu-id="24d76-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24d76-123">See Also</span></span>

[<span data-ttu-id="24d76-124">Arbeiten mit Artikelattributen</span><span class="sxs-lookup"><span data-stu-id="24d76-124">Work with Item Attributes</span></span>](inventory-how-work-item-attributes.md)  
[<span data-ttu-id="24d76-125">Neue Artikel registrieren</span><span class="sxs-lookup"><span data-stu-id="24d76-125">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="24d76-126">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="24d76-126">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="24d76-127">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="24d76-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]