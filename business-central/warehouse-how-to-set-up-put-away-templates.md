---
title: 'Vorgehensweise: Einlagerungsmethoden einrichten | Microsoft Docs'
description: Mit der Funktionalität der gesteuerten Einlagerung und Kommissionierung, wird jederzeit der geeignetsten Lagerplatz für Ihre Artikel vorgeschlagen, entsprechend der Einlagerungsvorlage, die Sie für dieses Lager eingerichtet haben, entsprechend den Lagerplatzprioritäten, die Sie den Lagerplätzen gegeben haben, und den minimalen und maximalen Mengen, die Sie für Standardlagerplätze eingerichtet haben.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2c8cd73e1dd47549cab57e9fd44fe52232437175
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3925297"
---
# <a name="set-up-put-away-templates"></a><span data-ttu-id="81d7b-103">Einlagerungsmethoden einzurichten</span><span class="sxs-lookup"><span data-stu-id="81d7b-103">Set Up Put-away Templates</span></span>

<span data-ttu-id="81d7b-104">Mit der Funktionalität der gesteuerten Einlagerung und Kommissionierung, wird jederzeit der geeignetsten Lagerplatz für Ihre Artikel vorgeschlagen, entsprechend der Einlagerungsvorlage, die Sie für dieses Lager eingerichtet haben, entsprechend den Lagerplatzprioritäten, die Sie den Lagerplätzen gegeben haben, und den minimalen und maximalen Mengen, die Sie für Standardlagerplätze eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="81d7b-104">With directed put-away and pick functionality, the most appropriate bin for your items at any given time is suggested, according to the put-away template that you have set up for the warehouse, the bin rankings you have given to the bins, and the minimum and maximum quantities that you have set up for fixed bins.</span></span>  

<span data-ttu-id="81d7b-105">Sie können eine Reihe von Einlagerungsmethoden einrichten und eine von diesen auswählen, mit der Sie im Allgemeinen Einlagerungen in Ihrem Lager steuern möchten.</span><span class="sxs-lookup"><span data-stu-id="81d7b-105">You can set up a number of put-away templates and select one of them to govern put-aways in general in your warehouse.</span></span> <span data-ttu-id="81d7b-106">Sie können ebenfalls für solche Artikel oder Lagerhaltungsdaten, für die besondere Einlagerungsmethoden nötig sind, eine Einlagerungsvorlage auswählen.</span><span class="sxs-lookup"><span data-stu-id="81d7b-106">You can also select a put-away template for any item or stockkeeping unit that might have special put-away requirements.</span></span>  

## <a name="to-set-up-put-away-templates"></a><span data-ttu-id="81d7b-107">So richten Sie Einlagerungsmethoden ein:</span><span class="sxs-lookup"><span data-stu-id="81d7b-107">To set up put-away templates</span></span>

1. <span data-ttu-id="81d7b-108">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Einlagerungsvorlagen** ein, und wählen Sie dann den zugehörigen Link.</span><span class="sxs-lookup"><span data-stu-id="81d7b-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Put-away Templates** , and then choose the related link.</span></span>  
2. <span data-ttu-id="81d7b-109">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="81d7b-109">Choose the **New** action.</span></span>  
3. <span data-ttu-id="81d7b-110">Geben Sie einen Code ein, bei dem es sich um die eindeutige Kennung der neu zu erstellenden Vorlage handelt.</span><span class="sxs-lookup"><span data-stu-id="81d7b-110">Enter a code that is the unique identifier of the template you are about to create.</span></span>  
4. <span data-ttu-id="81d7b-111">Geben Sie, wenn Sie möchten, eine kurze Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="81d7b-111">Enter a short description, if you wish.</span></span>  
5. <span data-ttu-id="81d7b-112">Füllen Sie die erste Zeile mit den Lagerplatzanforderungen aus, die vor allem erfüllt sein sollen, wenn eine Einlagerung vorgeschlagen wird.</span><span class="sxs-lookup"><span data-stu-id="81d7b-112">Fill in the first line with the bin requirements that you want fulfilled first and foremost when suggesting a put-away.</span></span>

    <span data-ttu-id="81d7b-113">Wenn die Standard-Einlagerungsmethode beispielsweise auf festen Lagerplätzen basieren soll, wählen Sie das Feld **Festen Lagerplatz finden** aus.</span><span class="sxs-lookup"><span data-stu-id="81d7b-113">For example, if want the default put-away method to be based on fixed bins, then choose the **Find Fixed Bin** field.</span></span> [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
6. <span data-ttu-id="81d7b-114">Füllen Sie eine zweite Zeile mit den Lagerplatzanforderungen aus, die Ihre zweite Wahl bei der Auswahl eines Lagerplatzes für die Einlagerung sein soll.</span><span class="sxs-lookup"><span data-stu-id="81d7b-114">Fill in the second line with the bin requirements that would be your second choice to fulfill in finding a bin for put-away.</span></span> <span data-ttu-id="81d7b-115">Die zweite Zeile wird nur berücksichtigt, wenn kein Lagerplatz gefunden wird, der die Anforderungen der ersten Zeile erfüllt.</span><span class="sxs-lookup"><span data-stu-id="81d7b-115">The second line is used only if a bin that meets the requirements of the first line cannot be found.</span></span>  
7. <span data-ttu-id="81d7b-116">Fahren Sie fort, die Zeilen auszufüllen, bis Sie alle gewünschten Lagerplatzeinlagerungen beschrieben haben, die im Einlagerungsprozess verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="81d7b-116">Continue to fill in the lines until you have described all the acceptable bin placements that you want to use in the put-away process.</span></span>  
8. <span data-ttu-id="81d7b-117">Wählen Sie in der letzten Zeile der Einlagerungsvorlage das Kontrollkästchen **Chaot. Lagerplatz finden** .</span><span class="sxs-lookup"><span data-stu-id="81d7b-117">On the last line in the put-away template, select the **Find Floating Bin** check box.</span></span>  

<span data-ttu-id="81d7b-118">Sie können verschiedene Einlagerungsmethoden erstellen und diese dann anwenden, wie Sie es für richtig halten.</span><span class="sxs-lookup"><span data-stu-id="81d7b-118">You can create various put-away templates and then apply them as you see fit.</span></span> <span data-ttu-id="81d7b-119">Als Erstes wird die Einlagerungsmethode berücksichtigt, die Sie für den Artikel oder die Lagerhaltungsdaten ausgewählt haben (falls Sie dies getan haben).</span><span class="sxs-lookup"><span data-stu-id="81d7b-119">The put-away template that you selected for the item or stockkeeping unit, if any is used first.</span></span> <span data-ttu-id="81d7b-120">Wenn diese Felder nicht ausgefüllt sind, wird die Einlagerungsmethode berücksichtigt, die Sie für das Lager im Inforegister **Lagerplatzprüfung** auf der Lagerortkarte ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="81d7b-120">If these fields are not filled in, then the put-away template that you selected for the warehouse on the **Bin Policies** FastTab on the location card is used.</span></span>  

## <a name="see-also"></a><span data-ttu-id="81d7b-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81d7b-121">See Also</span></span>

[<span data-ttu-id="81d7b-122">Logistik</span><span class="sxs-lookup"><span data-stu-id="81d7b-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="81d7b-123">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="81d7b-123">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="81d7b-124">Lagerortverwaltung einrichten</span><span class="sxs-lookup"><span data-stu-id="81d7b-124">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="81d7b-125">Montageverwaltung</span><span class="sxs-lookup"><span data-stu-id="81d7b-125">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="81d7b-126">Designdetails: Lagerverwaltung</span><span class="sxs-lookup"><span data-stu-id="81d7b-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="81d7b-127">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="81d7b-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
