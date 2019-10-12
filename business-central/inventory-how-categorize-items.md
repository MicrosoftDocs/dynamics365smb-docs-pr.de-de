---
title: Kategorisieren Sie Artikel| Microsoft Docs
description: Um Artikel zu finden, können Sie Artikelattribute zuweisen und Artikel nach den definierten Kategorien organisieren.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: bf4ae1f000afcae3026b3c35a8097f2fb73a9a4a
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2309988"
---
# <a name="categorize-items"></a><span data-ttu-id="e21cf-103">Artikel kategorisieren</span><span class="sxs-lookup"><span data-stu-id="e21cf-103">Categorize Items</span></span>
<span data-ttu-id="e21cf-104">Um eine Übersicht über Ihre Artikel zu verwalten und das Sortieren und Finden von Artikeln zu erleichtern, ist es nützlich, Ihre Artikel in Artikelkategorien zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="e21cf-104">To maintain an overview of your items and to help you sort and find items, it is useful to organize your items in item categories.</span></span>

<span data-ttu-id="e21cf-105">Um Artikel nach Eigenschaften zu finden, können Sie Artikelattribute Artikeln und auch Artikelkategorien zuordnen.</span><span class="sxs-lookup"><span data-stu-id="e21cf-105">To find items by characteristics, you can assign item attributes to items and also to item categories.</span></span> <span data-ttu-id="e21cf-106">Weitere Informationen finden Sie unter [Arbeiten mit Artikelattributen](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="e21cf-106">For more information, see [Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>

## <a name="to-create-an-item-category"></a><span data-ttu-id="e21cf-107">So erstellen Sie eine Artikelkategorie</span><span class="sxs-lookup"><span data-stu-id="e21cf-107">To create an item category</span></span>
1. <span data-ttu-id="e21cf-108">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Logistik Artikelkategorien** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="e21cf-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Categories**, and then choose the related link.</span></span>
2. <span data-ttu-id="e21cf-109">Wählen Sie auf der Seite **Artikelkategorien** die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="e21cf-109">On the **Item Categories** page, choose the **New** action.</span></span>
3. <span data-ttu-id="e21cf-110">Füllen Sie auf der Seite **Artikelkategorienkarte** im Inforegister **Allgemein** die notwendigen Felder aus.</span><span class="sxs-lookup"><span data-stu-id="e21cf-110">On the **Item Category Card** page, on the **General** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="e21cf-111">Geben Sie im Inforegister **Attribute** alle Artikelattribute für die Artikelkategorie an.</span><span class="sxs-lookup"><span data-stu-id="e21cf-111">On the **Attributes** FastTab, specify any item attributes for the item category.</span></span> <span data-ttu-id="e21cf-112">Weitere Informationen finden Sie unter [So ordnen Sie ein Artikelattribut einer Artikelkategorie zu](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).</span><span class="sxs-lookup"><span data-stu-id="e21cf-112">For more information, see [To assign item attributes to item categories](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).</span></span>

> [!NOTE]  
>   <span data-ttu-id="e21cf-113">Hinweis: Wenn die Artikelkategorie eine übergeordnete Artikelkategorie besitzt, wie durch das Feld **Übergeordnete Kategorie** angegeben, werden alle Artikelattribute, die dieser übergeordneten Artikelkategorie zugewiesen sind, im Inforegister **Attribute** bereits eingetragen.</span><span class="sxs-lookup"><span data-stu-id="e21cf-113">If the item category has a parent item category, as indicated by the **Parent Category** field, then any item attributes that are assigned to that parent item category are prefilled on the **Attributes** FastTab.</span></span>

> [!NOTE]  
>   <span data-ttu-id="e21cf-114">Artikelattribute, die Sie einer Artikelkategorie zuordnen, werden automatisch auf den Artikel angewendet, der der Artikelkategorie zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e21cf-114">Item attributes that you assign to an item category will automatically apply to the item that the item category is assigned to.</span></span>

## <a name="to-assign-an-item-category-to-an-item"></a><span data-ttu-id="e21cf-115">So ordnen Sie eine Artikelkategorie einem Artikel zu</span><span class="sxs-lookup"><span data-stu-id="e21cf-115">To assign an item category to an item</span></span>
1. <span data-ttu-id="e21cf-116">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Katalogartikel** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="e21cf-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="e21cf-117">Öffnen Sie die Karte des Artikels, den Sie einer Artikelkategorie zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="e21cf-117">Open the card for the item that you want to assign to an item category.</span></span>
3. <span data-ttu-id="e21cf-118">Klicken Sie im Feld **Artikelkategoriencode** auf die Schaltfläche suchen und wählen Sie eine bereits vorhandene Artikelkategorie aus.</span><span class="sxs-lookup"><span data-stu-id="e21cf-118">Choose the lookup button in the **Item Category Code** field and select an existing item category.</span></span> <span data-ttu-id="e21cf-119">Alternativ wählen Sie die Aktion **Neu**, um zuerst eine neue Artikelkategorie so zu erstellen, wie es unter [So erstellen Sie eine Artikelkategorie](inventory-how-categorize-items.md#to-create-an-item-category) erklärt wird.</span><span class="sxs-lookup"><span data-stu-id="e21cf-119">Alternatively, choose the **New** action to first create a new item category as explained in [To create an item category](inventory-how-categorize-items.md#to-create-an-item-category).</span></span>

## <a name="see-also"></a><span data-ttu-id="e21cf-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e21cf-120">See Also</span></span>
[<span data-ttu-id="e21cf-121">Arbeiten mit Artikelattributen</span><span class="sxs-lookup"><span data-stu-id="e21cf-121">Work with Item Attributes</span></span>](inventory-how-work-item-attributes.md)  
[<span data-ttu-id="e21cf-122">Neue Artikel registrieren</span><span class="sxs-lookup"><span data-stu-id="e21cf-122">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="e21cf-123">Lagerbest</span><span class="sxs-lookup"><span data-stu-id="e21cf-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="e21cf-124">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e21cf-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
