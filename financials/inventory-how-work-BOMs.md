---
title: "Vorgehensweise: Arbeiten mit Stücklisten| Microsoft Docs"
description: "Sie erstellen eine Montagestückliste, um die Komponenten und Ressourcen an, die benötigt werden, um den Artikel zusammenzufügen, den die Montagestückliste darstellt, und die Komponenten eines Montageartikels an."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: e6aef60ee5b206b0ae978f72b92e6f8778290509
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-work-with-bills-of-material"></a><span data-ttu-id="fcdf4-103">Vorgehensweise: Arbeiten mit Stücklisten</span><span class="sxs-lookup"><span data-stu-id="fcdf4-103">How to: Work with Bills of Material</span></span>
> [!NOTE]  
>   <span data-ttu-id="fcdf4-104">Die aktuelle Version aus [!INCLUDE[d365fin](includes/d365fin_md.md)] enthält nur den ersten Teil der Montageverwaltungsfunktion.</span><span class="sxs-lookup"><span data-stu-id="fcdf4-104">The current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] only contains the first part of the Assembly Management feature.</span></span> <span data-ttu-id="fcdf4-105">Für den Moment können Sie nur Montagestücklisten erstellen und die zugehörigen übergeordneten Artikel als normale Artikel dann bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="fcdf4-105">For now, you can only create assembly BOMs and then handle the related parent items as normal inventory items.</span></span> <span data-ttu-id="fcdf4-106">In einem zukünftigen Update können Sie die tatsächliche Montage von Artikeln von den Komponenten, entweder im Lagermontage- als auch in Auftragsmontageprozessen verwenden und Sie können Komponenten als Kit verkaufen.</span><span class="sxs-lookup"><span data-stu-id="fcdf4-106">In a future update, you can manage the actual assembly of items from components, either in assemble-to-stock or assemble-to-order flows, and you can sell components as kits.</span></span>

<span data-ttu-id="fcdf4-107">Sie verwenden Stücklisten (BOMs), um übergeordnete Artikel zu strukturieren, die Sie als Sets verkaufen, die aus den Komponenten des übergeordneten Artikels bestehen oder für die Sie die Auftragsmontage oder das Lager haben.</span><span class="sxs-lookup"><span data-stu-id="fcdf4-107">You use bills of materials (BOMs) to structure parent items that you sell as kits consisting of the parent's components or that you assemble to order or to stock.</span></span>

<span data-ttu-id="fcdf4-108">In [!INCLUDE[d365fin](includes/d365fin_md.md)], bezeichnet eine Stückliste eine "Montagestückliste".</span><span class="sxs-lookup"><span data-stu-id="fcdf4-108">In [!INCLUDE[d365fin](includes/d365fin_md.md)], a bill of materials is referred to as an "assembly BOM".</span></span> <span data-ttu-id="fcdf4-109">Die Montagestückliste gibt an, welche Komponentenartikel im übergeordneten Artikel enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="fcdf4-109">Assembly BOMs specify which components are contained in parent items.</span></span> <span data-ttu-id="fcdf4-110">In dieser Dokumentation wird ein übergeordneter Artikel als "ein Montageartikel" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="fcdf4-110">In this documentation, a parent item is referred to as an "assembly item".</span></span>

<span data-ttu-id="fcdf4-111">Montagestücklisten enthalten normalerweise Artikel, können jedoch auch eine oder mehrere Ressourcen enthalten, die die Montageartikel ausführen.</span><span class="sxs-lookup"><span data-stu-id="fcdf4-111">Assembly BOMs usually contain items but can also contain one or more resources that are required to put the assembly item together.</span></span>

<span data-ttu-id="fcdf4-112">Montagestücklisten können mehrstufig sein, was bedeutet, dass eine Komponente in der Montagestückliste selbst ein Montageartikel sein kann.</span><span class="sxs-lookup"><span data-stu-id="fcdf4-112">Assembly BOMs can have multiple levels, which means that a component on the assembly BOM can be an assembly item itself.</span></span> <span data-ttu-id="fcdf4-113">In diesem Fall lautet das Feld **Montagestückliste** in der Montagestücklistenzeile **Ja**.</span><span class="sxs-lookup"><span data-stu-id="fcdf4-113">In that case, the **Assembly BOM** field on the assembly BOM line contains **Yes**.</span></span>

<span data-ttu-id="fcdf4-114">Spezielle Anforderungen gelten für Artikel auf Montagestücklisten in Bezug auf die Verfügbarkeit.</span><span class="sxs-lookup"><span data-stu-id="fcdf4-114">Special requirements apply to items on assembly BOMs with regards to availability.</span></span> <span data-ttu-id="fcdf4-115">Weitere Informationen finden Sie im Abschnitt "Verfügbarkeit eines Artikels nach dessen Verwendung in den Montagestücklisten anzeigen [Vorgehensweise: Verschaffen Sie sich eine Übersicht zur Verfügbarkeit](inventory-how-availability-overview.md)".</span><span class="sxs-lookup"><span data-stu-id="fcdf4-115">For more information, see the "To see the availability of an item by its use in assembly BOMs" section in [How to: View the Availability of Items](inventory-how-availability-overview.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="fcdf4-116">Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="fcdf4-116">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="fcdf4-117">Weitere Informationen finden Sie unter [Anpassen Ihrer Financials Experience](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="fcdf4-117">For more information, see [Customizing Your Financials Experience](ui-experiences.md).</span></span>

## <a name="to-create-an-assembly-bom"></a><span data-ttu-id="fcdf4-118">So erstellen Sie eine Montagestückliste</span><span class="sxs-lookup"><span data-stu-id="fcdf4-118">To create an assembly BOM</span></span>
<span data-ttu-id="fcdf4-119">Um einen übergeordneten Artikel zu definieren, der aus anderen Artikeln und möglicherweise Ressourcen besteht die benötigt werden, um die übergeordnete Baugruppe zusammenzufügen, müssen Sie eine Montagestückliste erstellen.</span><span class="sxs-lookup"><span data-stu-id="fcdf4-119">To define a parent item that consists of other items, and potentially of resources required to put the parent together, you must create an assembly BOM.</span></span>  

<span data-ttu-id="fcdf4-120">Es gibt zwei Schritte zum Erstellen einer Montagestückliste:</span><span class="sxs-lookup"><span data-stu-id="fcdf4-120">There are two parts to creating an assembly BOM:</span></span>
- <span data-ttu-id="fcdf4-121">Einrichten einer neuen Artikelkarte</span><span class="sxs-lookup"><span data-stu-id="fcdf4-121">Setting up a new item</span></span>
- <span data-ttu-id="fcdf4-122">Gibt die Beschreibung des Montageartikels an.</span><span class="sxs-lookup"><span data-stu-id="fcdf4-122">Defining the BOM structure of the assembly item.</span></span>

1. <span data-ttu-id="fcdf4-123">Richten Sie einen neuen Artikel ein.</span><span class="sxs-lookup"><span data-stu-id="fcdf4-123">Set up a new item.</span></span> <span data-ttu-id="fcdf4-124">Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten neuer Artikel](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="fcdf4-124">For more information, see [How to: Register New Items](inventory-how-register-new-items.md).</span></span>

    <span data-ttu-id="fcdf4-125">Fahren Sie fort, um Komponenten oder Ressourcen in der Montagestückliste einzugeben.</span><span class="sxs-lookup"><span data-stu-id="fcdf4-125">Proceed to enter components or resources on the assembly BOM.</span></span>  
2. <span data-ttu-id="fcdf4-126">Im Fenster **Artikelkarte** für einen Montageartikel wählen Sie die **Montage** Aktion aus, und wählen Sie die **Montagestückliste** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="fcdf4-126">In the **Item Card** window for an assembly item, choose the **Assembly** action, and then choose the **Assembly BOM** action.</span></span>
3. <span data-ttu-id="fcdf4-127">Füllen Sie im Fenster **Montagestückliste** die Felder wie benötigt aus.</span><span class="sxs-lookup"><span data-stu-id="fcdf4-127">In the **Assembly BOM** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-the-components-of-an-assembly-item-indented-according-to-the-bom-structure"></a><span data-ttu-id="fcdf4-128">Um die Komponenten eines Montageartikels anzuzeigen gemäß der Stücklistenstruktur</span><span class="sxs-lookup"><span data-stu-id="fcdf4-128">To view the components of an assembly item indented according to the BOM structure</span></span>
<span data-ttu-id="fcdf4-129">Im Fenster **Montagestückliste** können Sie ein separates Fenster öffnen, in dem die Komponenten sowie jegliche Ressourcen angezeigt werden, die gemäß ihrer Stücklistenposition unter den Montageartikel eingerückt werden.</span><span class="sxs-lookup"><span data-stu-id="fcdf4-129">From the **Assembly BOM** window, you can open a separate window that shows the components and any resources indented according to their BOM position under the assembly item.</span></span>

1. <span data-ttu-id="fcdf4-130">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen")aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="fcdf4-130">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="fcdf4-131">Öffnen Sie das Kartenfenster für den Montageartikel.</span><span class="sxs-lookup"><span data-stu-id="fcdf4-131">Open the card for an assembly item.</span></span> <span data-ttu-id="fcdf4-132">(Das Feld **Montagestückliste** im Fenster **Artikel** enthält **Ja**.)</span><span class="sxs-lookup"><span data-stu-id="fcdf4-132">(The **Assembly BOM** field in the **Items** window contains **Yes**.)</span></span>
3. <span data-ttu-id="fcdf4-133">Im Fenster **Artikelkarte** für einen Montageartikel wählen Sie die **Montage** Aktion aus, und wählen Sie die **Montagestückliste** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="fcdf4-133">In the **Item Card** window, choose the **Assembly** action, and then choose the **Assembly BOM** action.</span></span>
4. <span data-ttu-id="fcdf4-134">Wählen Sie im Fenster **Montagestückliste** die Aktion **Stückliste anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="fcdf4-134">In the **Assembly BOM** window, choose the **Show BOM** action.</span></span>

## <a name="to-buy-sell-or-transfer-assembly-items"></a><span data-ttu-id="fcdf4-135">Montageartikel kaufen, verkaufen oder übertragen</span><span class="sxs-lookup"><span data-stu-id="fcdf4-135">To buy, sell, or transfer assembly items</span></span>
<span data-ttu-id="fcdf4-136">Da die aktuelle Version aus [!INCLUDE[d365fin](includes/d365fin_md.md)] nur die Möglichkeit enthält, Montagestücklisten für Artikel festzulegen und zuzuweisen, können Sie Montageartikel in Belegzeilen nur als Normalpositionen bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="fcdf4-136">Because the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] only contains the ability to define and assign assembly BOMs to items, you can handle assembly items on document lines as normal items only.</span></span>

<span data-ttu-id="fcdf4-137">**Vorsicht**: Die Komponenten der Lagermenge werden nicht geändert, wenn Sie das tun.</span><span class="sxs-lookup"><span data-stu-id="fcdf4-137">**Caution**: The inventory quantity of BOM components will not be adjusted if you do so.</span></span>

## <a name="see-also"></a><span data-ttu-id="fcdf4-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fcdf4-138">See Also</span></span>
[<span data-ttu-id="fcdf4-139">Vorgehensweise: Einen neuen Artikel registrieren</span><span class="sxs-lookup"><span data-stu-id="fcdf4-139">How to: Register New Items</span></span>](inventory-how-register-new-items.md)  
<span data-ttu-id="fcdf4-140">[Vorgehensweise: Artikelverfügbarkeit anzeigen](inventory-how-availability-overview.md)   </span><span class="sxs-lookup"><span data-stu-id="fcdf4-140">[How to: View the Availability of Items](inventory-how-availability-overview.md)   </span></span>  
[<span data-ttu-id="fcdf4-141">Lagerbest</span><span class="sxs-lookup"><span data-stu-id="fcdf4-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="fcdf4-142">[Arbeiten mit [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fcdf4-142">[Working with [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>

