---
title: 'Vorgehensweise: Zusammenfassen von Lieferungen in einer einzelnen Rechnung | Microsoft Docs'
description: Wenn Sie mehr als eine Lieferung gleichzeitig fakturieren möchten, können Sie die Funktion zum Erstellen von Sammelrechnungen verwenden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: f6ce4c0c304fc8255789ec91fb3a00ba78170d6d
ms.sourcegitcommit: 6078bc9b2b571248d779722ce4125f250e7a3922
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/07/2020
ms.locfileid: "3666922"
---
# <a name="combine-shipments-on-a-single-invoice"></a><span data-ttu-id="cf141-103">Zusammenfassen von Lieferungen in einer einzelnen Rechnung</span><span class="sxs-lookup"><span data-stu-id="cf141-103">Combine Shipments on a Single Invoice</span></span>
<span data-ttu-id="cf141-104">Wenn Sie mehr als eine Lieferung gleichzeitig fakturieren möchten, können Sie die Funktion zum Erstellen von Sammelrechnungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="cf141-104">If you want to invoice more than one shipment at a time, you can use the combined shipments feature.</span></span>  

<span data-ttu-id="cf141-105">Bevor Sie eine Sammelrechnung erstellen können, müssen Sie mehr als eine Verkaufslieferung für den gleichen Debitor in der gleichen Währung gebucht haben.</span><span class="sxs-lookup"><span data-stu-id="cf141-105">Before you can create a combined shipment, more than one sales shipment for the same customer in the same currency must be posted.</span></span> <span data-ttu-id="cf141-106">Anders ausgedrückt, Sie müssen zwei oder mehr Verkaufsaufträge erstellt und als geliefert (aber nicht fakturiert) gebucht haben.</span><span class="sxs-lookup"><span data-stu-id="cf141-106">In other words, you must have create two or more sales orders and post them as shipped, but not invoiced.</span></span> 

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="cf141-107">So kombinieren Sie Lieferungen manuell auf einer einzigen Rechnung:</span><span class="sxs-lookup"><span data-stu-id="cf141-107">To manually combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="cf141-108">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Verkaufsrechnungen** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="cf141-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="cf141-109">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="cf141-109">Choose the **New** action.</span></span> <span data-ttu-id="cf141-110">Weitere Informationen finden Sie unter [Fakturieren eines Verkaufs](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="cf141-110">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span>
3. <span data-ttu-id="cf141-111">Wählen Sie im Feld **Verk. an Deb.-Nr.**</span><span class="sxs-lookup"><span data-stu-id="cf141-111">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="cf141-112">Feld, geben Sie den Debitor ein, der die Rechnung für die gelieferten Artikel erhält.</span><span class="sxs-lookup"><span data-stu-id="cf141-112">field, enter the customer who will receive the invoice for the shipped items.</span></span>  
4. <span data-ttu-id="cf141-113">Klicken Sie im Inforegister **Zeilen** und wählen die Aktionen **Warenverandszeilen holen**.</span><span class="sxs-lookup"><span data-stu-id="cf141-113">On the **Lines** FastTab, choose the **Get Shipment Lines** action.</span></span>  
5. <span data-ttu-id="cf141-114">Wählen Sie die Lieferzeile aus, die in die Rechnung aufgenommen werden soll:</span><span class="sxs-lookup"><span data-stu-id="cf141-114">Select the shipment line that you want to include in the invoice:</span></span>  

    - <span data-ttu-id="cf141-115">Um alle Zeilen einzufügen, wählen Sie alle Zeilen aus, und wählen Sie die Schaltfläche **OK**.</span><span class="sxs-lookup"><span data-stu-id="cf141-115">To insert all lines, select all lines and choose the **OK** button.</span></span>  
    - <span data-ttu-id="cf141-116">Um spezifische Zeilen einzufügen, wählen Sie die Zeilen aus, und wählen Sie die Schaltfläche **OK**.</span><span class="sxs-lookup"><span data-stu-id="cf141-116">To insert specific lines, select the lines and choose the **OK** button.</span></span> <span data-ttu-id="cf141-117">Sie können die STRG-Taste verwenden, um mehrere nicht unmittelbar aufeinander folgende Zeilen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="cf141-117">You can use the Ctrl key to select multiple nonsequential lines.</span></span>  

    <span data-ttu-id="cf141-118">Wenn Sie eine falsche Lieferzeile ausgewählt haben oder von vorn beginnen möchten, können Sie einfach die Zeilen in der Rechnung löschen und die Funktion **Lieferzeilen holen** erneut ausführen.</span><span class="sxs-lookup"><span data-stu-id="cf141-118">If an incorrect shipment line was selected or you want to start over, you can simply delete the lines on the invoice and re-run the **Get Shipment Lines** function.</span></span>  
7. <span data-ttu-id="cf141-119">Um die Rechnung zu buchen, wählen Sie die Aktion **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="cf141-119">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="cf141-120">So kombinieren Sie Lieferungen automatisch in einer einzigen Rechnung:</span><span class="sxs-lookup"><span data-stu-id="cf141-120">To automatically combine shipments on a single invoice</span></span>  
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="cf141-121">wählt nur Verkaufsaufträge aus, bei denen **Sendungen kombinieren** gewählt ist.</span><span class="sxs-lookup"><span data-stu-id="cf141-121">will select only sales orders where **Combine Shipments** is chosen.</span></span> 

1. <span data-ttu-id="cf141-122">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Lieferungen kombinieren** ein, und wählen Sie dann den zugehörigen Link.</span><span class="sxs-lookup"><span data-stu-id="cf141-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Combine Shipments**, and then choose the related link.</span></span> <span data-ttu-id="cf141-123">Die Anforderungsseite für die Stapelverarbeitung wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="cf141-123">The batch job request page opens.</span></span>  
2. <span data-ttu-id="cf141-124">Füllen Sie die Felder nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="cf141-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="cf141-125">Wählen Sie das Kontrollkästchen **Rechnungen buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="cf141-125">Choose the **Post Invoices** check box.</span></span>  
4. <span data-ttu-id="cf141-126">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="cf141-126">Choose the **OK** button.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="cf141-127">Die Rechnungen müssen manuell gebucht werden, wenn das Kontrollkästchen **Rechnungen buchen** für die Stapelverarbeitung nicht aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="cf141-127">You will need to manually post the invoices if the **Post Invoices** check box was not selected on the batch job.</span></span>  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a><span data-ttu-id="cf141-128">Offene Verkaufsaufträge nach kombinierter Lieferungsbuchung entfernen</span><span class="sxs-lookup"><span data-stu-id="cf141-128">To remove open sales orders after combined shipment posting</span></span> 
<span data-ttu-id="cf141-129">Wenn Lieferungen in einer Rechnung zusammengefasst und gebucht werden, wird für die fakturierten Zeilen eine gebuchte Verkaufsrechnung erstellt.</span><span class="sxs-lookup"><span data-stu-id="cf141-129">When shipments are combined on an invoice and posted, a posted sales invoice is created for the invoiced lines.</span></span> <span data-ttu-id="cf141-130">Das Feld **Menge fakturiert** auf dem Ursprungsrahmenauftrag oder dem Auftrag wird ausgehend von der fakturierten Menge aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cf141-130">The **Quantity Invoiced** field on the originating blanket sales order or sales order is updated based on the invoiced quantity.</span></span>  

<span data-ttu-id="cf141-131">Werden Lieferungen auf diese Weise fakturiert, bleiben die Aufträge, aus denen die Lieferungen gebucht werden, weiterhin bestehen, auch wenn sie vollständig geliefert und fakturiert wurden.</span><span class="sxs-lookup"><span data-stu-id="cf141-131">When you invoice shipments in this way, the orders from which the shipments were posted still exist, even if they have been fully shipped and invoiced.</span></span>   

1. <span data-ttu-id="cf141-132">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Fakturierte Verkaufsaufträge löschen** ein und wählen Sie dann den entsprechenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="cf141-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Invoiced Sales Orders**, and then select the link.</span></span>  
2. <span data-ttu-id="cf141-133">Wählen Sie im Feld **Kontonummer**</span><span class="sxs-lookup"><span data-stu-id="cf141-133">Specify in the **No.**</span></span> <span data-ttu-id="cf141-134">Filterfeld an, welche Verkaufsaufträge zu löschen sind.</span><span class="sxs-lookup"><span data-stu-id="cf141-134">filter field which sales orders to delete.</span></span>  
3. <span data-ttu-id="cf141-135">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="cf141-135">Choose the **OK** button.</span></span>  

<span data-ttu-id="cf141-136">Sie können die einzelnen Verkaufsaufträge auch manuell löschen.</span><span class="sxs-lookup"><span data-stu-id="cf141-136">Alternatively, delete individual sales orders manually.</span></span>  

<span data-ttu-id="cf141-137">Wiederholen Sie die Schritte 1 bis 3 für alle betroffenen anderen Belege, wie z. B. leere Verkaufsaufträge.</span><span class="sxs-lookup"><span data-stu-id="cf141-137">Repeat steps 1 through 3 for any other affected documents, such as blanket sales orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="cf141-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf141-138">See Also</span></span>  
[<span data-ttu-id="cf141-139">Verkauf</span><span class="sxs-lookup"><span data-stu-id="cf141-139">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="cf141-140">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cf141-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
