---
title: 'Vorgehensweise: Artikel-Familien in der Produktion verwenden | Microsoft Docs'
description: Die Hauptaufgabe beim Anpassen eines Basiskalenders für Ihre Firma oder einen Ihrer Geschäftspartner ist, alle Änderungen am Status der Daten als freie Tage oder Arbeitstage einzugeben.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8d773c1c12bd170801b178c1627dc0b3dc718bdb
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2883142"
---
# <a name="work-with-production-families"></a><span data-ttu-id="24007-103">Arbeiten mit Fertigungsfamilien</span><span class="sxs-lookup"><span data-stu-id="24007-103">Work with Production Families</span></span>
<span data-ttu-id="24007-104">Eine Fertigungsfamilie ist eine Gruppe einzelner Artikel, deren Zusammenhang in der Ähnlichkeit ihres Fertigungsprozesses liegt.</span><span class="sxs-lookup"><span data-stu-id="24007-104">A production family is a group of individual items whose relationship is based on the similarity of their manufacturing processes.</span></span> <span data-ttu-id="24007-105">Wenn Sie Fertigungsfamilien zusammenstellen, können einzelne Artikel mehrfach, in einem Arbeitsschritt, gefertigt werden, womit Sie den Materialverbrauch optimieren können.</span><span class="sxs-lookup"><span data-stu-id="24007-105">By forming production families, some items can be manufactured twice or more in one production, which will optimize material consumption.</span></span>

<span data-ttu-id="24007-106">Geben Sie auf der **Menge**-Seite im **Familien**-Fenster die Menge ein, die gefertigt werden soll, wenn die gesamte Fertigungsfamilie einmal gefertigt wird.</span><span class="sxs-lookup"><span data-stu-id="24007-106">In the **Quantity** field on the **Family** page, you enter the quantity that will be produced when the whole family has been manufactured once.</span></span>

## <a name="example"></a><span data-ttu-id="24007-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="24007-107">Example</span></span>
<span data-ttu-id="24007-108">Beim Stanzen können vier Teile eines Artikels und 10 Teile eines anderen Artikels aus einem Blech zur gleichen Zeit gestanzt werden.</span><span class="sxs-lookup"><span data-stu-id="24007-108">In punching processes, four pieces of the same item can be produced from one sheet and 10 pieces of another, different, item at the same time.</span></span> <span data-ttu-id="24007-109">Die Stanzmaschine stanzt die kompletten 14 Teile in einem Arbeitsschritt.</span><span class="sxs-lookup"><span data-stu-id="24007-109">The punching machine will punch all 14 pieces in one step.</span></span>

<span data-ttu-id="24007-110">Fertigungsfamilien verringern die Ausschussmenge, da der normalerweise bei der Fertigung großer Teile entstehende Ausschuss zur Fertigung kleiner Teile verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="24007-110">Forming production families reduces the scrap quantity because what would normally be leftover scrap, when producing big pieces, will be used instead to produce small items.</span></span>

## <a name="to-set-up-a-production-family"></a><span data-ttu-id="24007-111">Fertigungsfamilien einrichten</span><span class="sxs-lookup"><span data-stu-id="24007-111">To set up a production family</span></span>
1. <span data-ttu-id="24007-112">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Fertigungsfamilien** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="24007-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Families**, and then choose the related link.</span></span>
2. <span data-ttu-id="24007-113">Füllen Sie die Felder bei Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="24007-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-produce-based-on-a-production-family"></a><span data-ttu-id="24007-114">Um auf Grundlage eine Produktionsfamilie erzeugen</span><span class="sxs-lookup"><span data-stu-id="24007-114">To produce based on a production family</span></span>
1. <span data-ttu-id="24007-115">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Feste geplante Fertigungsaufträge** ein, und wählen Sie dann den zugehörigen Link.</span><span class="sxs-lookup"><span data-stu-id="24007-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="24007-116">Dient zum Erstellen eines neuen Produktionsauftrags.</span><span class="sxs-lookup"><span data-stu-id="24007-116">Create a new production order.</span></span> <span data-ttu-id="24007-117">Weitere Informationen finden Sie unter [Erstellen von Montageaufträgen](production-how-to-create-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="24007-117">For more information, see [Create Production orders](production-how-to-create-production-orders.md).</span></span>
3. <span data-ttu-id="24007-118">Wählen Sie im Feld **Quelltyp** **Familie** aus.</span><span class="sxs-lookup"><span data-stu-id="24007-118">In the **Source Type** field, select **Family**.</span></span>  
4. <span data-ttu-id="24007-119">Wählen Sie im Feld **Quelle** die entsprechende Produktionsfamilien aus.</span><span class="sxs-lookup"><span data-stu-id="24007-119">In the **Source No.** field, select the relevant production family.</span></span>

## <a name="see-also"></a><span data-ttu-id="24007-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24007-120">See Also</span></span>
[<span data-ttu-id="24007-121">Fertigungsauftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="24007-121">Create Production BOMs</span></span>](production-how-to-create-production-boms.md)  
[<span data-ttu-id="24007-122">Produktion einrichten</span><span class="sxs-lookup"><span data-stu-id="24007-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="24007-123">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="24007-123">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="24007-124">[Planung](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="24007-124">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="24007-125">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="24007-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="24007-126">Einkauf</span><span class="sxs-lookup"><span data-stu-id="24007-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="24007-127">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="24007-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
