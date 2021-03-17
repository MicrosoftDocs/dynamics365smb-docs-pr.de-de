---
title: 'Vorgehensweise: Angebot eines Auftragsmontageverkaufs | Microsoft Docs'
description: Sie können Montageverwaltung verwenden, um einen Montageartikel auf Anforderung eines Debitors während des Vertriebsprozesses anzupassen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 807c924e64764e7ac1932321603a415101e3bbf3
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386649"
---
# <a name="quote-an-assemble-to-order-sale"></a><span data-ttu-id="c0ba0-103">Angebot eines Auftragsmontageverkaufs</span><span class="sxs-lookup"><span data-stu-id="c0ba0-103">Quote an Assemble-to-Order Sale</span></span>
<span data-ttu-id="c0ba0-104">Sie können Montageverwaltung verwenden, um einen Montageartikel auf Anforderung eines Debitors während des Vertriebsprozesses anzupassen.</span><span class="sxs-lookup"><span data-stu-id="c0ba0-104">You can use assembly management to customize an assembly item to a customer’s request during the sales process.</span></span> <span data-ttu-id="c0ba0-105">Weitere Informationen finden Sie unter [Verkaufen von Auftragsmontageartikeln](assembly-how-to-sell-items-assembled-to-order.md).</span><span class="sxs-lookup"><span data-stu-id="c0ba0-105">For more information, see [Sell Items Assembled to Order](assembly-how-to-sell-items-assembled-to-order.md).</span></span>  

<span data-ttu-id="c0ba0-106">Wie beim Verkauf beliebiger Artikel können Sie auch eine Verkaufsangebot für einen angepassten Montageartikel erstellen, bevor Sie dieses in einen Verkaufsauftrag umwandeln.</span><span class="sxs-lookup"><span data-stu-id="c0ba0-106">As when you sell any other type of item, you can also create a sales quote for a customized assembly item before converting it to a sales order.</span></span> <span data-ttu-id="c0ba0-107">Dieser Prozess beinhaltet einige zusätzliche Schritte, wenn Sie ihn mit dem Erstellen eines regulären Verkaufsangebots vergleichen; er verwendet eine Variation eines verknüpften Montageauftrags, ein Montageangebot.</span><span class="sxs-lookup"><span data-stu-id="c0ba0-107">This process involves several extra steps when you compare it to creating a regular sales quote, and it uses a variation of a linked assembly order, which is an assembly quote.</span></span>

> [!NOTE]  
>  <span data-ttu-id="c0ba0-108">Wie alle Arten von Angeboten, werden die Mengen in Montageangeboten nicht für die Verfügbarkeit, in der Planung oder für Reservierungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="c0ba0-108">Like all types of quotes, the quantities on assembly quotes are not used in availability, planning, or reservations.</span></span>  

## <a name="to-create-a-sales-quote-for-an-assemble-to-order-item"></a><span data-ttu-id="c0ba0-109">So erstellen Sie ein Verkaufsangebot für einen Auftragsmontageartikel:</span><span class="sxs-lookup"><span data-stu-id="c0ba0-109">To create a sales quote for an assemble-to-order item</span></span>  
1.  <span data-ttu-id="c0ba0-110">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Verkaufsangebot** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="c0ba0-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Quote**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c0ba0-111">Erstellen Sie eine Verkaufsangebotzeile mit einer Zeile für einen Montageartikel.</span><span class="sxs-lookup"><span data-stu-id="c0ba0-111">Create a sales quote line with one line for an assembly item.</span></span> <span data-ttu-id="c0ba0-112">Weitere Informationen finden Sie unter [Verkaufsangebote machen](sales-how-make-offers.md).</span><span class="sxs-lookup"><span data-stu-id="c0ba0-112">For more information, see [Make Sales Quotes](sales-how-make-offers.md).</span></span>  
3.  <span data-ttu-id="c0ba0-113">Geben Sie im Feld **Menge für Auftragsmontage** die vollständige Menge ein.</span><span class="sxs-lookup"><span data-stu-id="c0ba0-113">In the **Qty. to Assemble to Order** field, enter the full quantity.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="c0ba0-114">Sie sollten keine Teilmenge eingeben.</span><span class="sxs-lookup"><span data-stu-id="c0ba0-114">You should not quote a partial quantity.</span></span> <span data-ttu-id="c0ba0-115">Daher müssen Sie die gleiche Menge eingeben, die Sie im Feld **Menge** auf der Verkaufsangebotzeile eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="c0ba0-115">Therefore, you must enter the same quantity that you entered in the **Quantity** field on the sales quote line.</span></span>  

4.  <span data-ttu-id="c0ba0-116">Wählen Sie auf dem Inforegister **Zeilen** **Zeile** aus, wählen Sie **Auftragsmontage**, und klicken Sie anschließend auf **Auftragsmontagezeilen**.</span><span class="sxs-lookup"><span data-stu-id="c0ba0-116">On the **Lines** FastTab, choose **Line**, choose **Assemble to Order**, and then choose **Assemble-to-Order Lines**.</span></span> <span data-ttu-id="c0ba0-117">Wählen Sie das Feld **Menge für Auftragsmontage** aus.</span><span class="sxs-lookup"><span data-stu-id="c0ba0-117">Alternatively, choose the **Qty. to Assemble to Order** field on the line.</span></span>  
5.  <span data-ttu-id="c0ba0-118">Prüfen und ändern Sie bei Bedarf auf der Seite **Auftragsmontagezeilen** die Auftragsmontagezeilen anhand des Angebots, das der Debitor anfragt.</span><span class="sxs-lookup"><span data-stu-id="c0ba0-118">On the **Assemble-to-Order Lines** page, review or modify the assembly order lines according to the quote that the customer is requesting.</span></span> <span data-ttu-id="c0ba0-119">Wenn Sie weitere Informationen wünschen, wählen Sie die Aktion **Dokument anzeigen**, um den vollständigen Rahmenangebotsauftrag zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c0ba0-119">If you want to view more information, choose the **Show Document** action to open the complete blanket quote order.</span></span> <span data-ttu-id="c0ba0-120">Sie können den Inhalt der meisten Felder nicht ändern, und Sie können nicht buchen.</span><span class="sxs-lookup"><span data-stu-id="c0ba0-120">You cannot change the contents of most fields, and you cannot post.</span></span>  
6.  <span data-ttu-id="c0ba0-121">Wenn Sie die Montageauftragszeilen entsprechend dem Angebot angepasst haben, schließen Sie die Seite **Auftragsmontagezeilen**, um zur Seite **Verkaufsangebot** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="c0ba0-121">When you have adjusted the assembly order lines according to the quote, close the **Assemble-to-Order Lines** page to return to the **Sales Quote** page.</span></span>  
7.  <span data-ttu-id="c0ba0-122">Wenn der Debitor das Angebot annimmt, erstellen Sie einen Verkaufsauftrag für den angebotenen Montageartikel.</span><span class="sxs-lookup"><span data-stu-id="c0ba0-122">If the customer accepts the quote, then create a sales order for the quoted assembly item.</span></span> <span data-ttu-id="c0ba0-123">Weitere Informationen finden Sie unter [Verkaufsangebote machen](sales-how-make-offers.md).</span><span class="sxs-lookup"><span data-stu-id="c0ba0-123">For more information, see [Make Sales Quotes](sales-how-make-offers.md).</span></span> <span data-ttu-id="c0ba0-124">Das verknüpfte Montageangebot und alle eventuellen Anpassungen werden mit dem neuen Verkaufsauftrag verknüpft, um die Montage des/der zu verkaufenden Artikel vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="c0ba0-124">The linked assembly quote and any customizations are linked to that new sales order to prepare for assembly of the item or items to be sold.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c0ba0-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0ba0-125">See Also</span></span>  
[<span data-ttu-id="c0ba0-126">Montageverwaltung</span><span class="sxs-lookup"><span data-stu-id="c0ba0-126">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="c0ba0-127">Mit Fertigungsstücklisten arbeiten</span><span class="sxs-lookup"><span data-stu-id="c0ba0-127">Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)  
[<span data-ttu-id="c0ba0-128">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="c0ba0-128">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="c0ba0-129">Designdetails: Lagerverwaltung</span><span class="sxs-lookup"><span data-stu-id="c0ba0-129">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="c0ba0-130">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c0ba0-130">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]