---
title: so fassen Sie Wareneingänge zusammen | Microsoft Docs
description: Wenn Sie mehrere Einkaufslieferungen gleichzeitig fakturieren möchten, können Sie die Funktion Sammelgutschrift verwenden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 86617934ecdb0ac2f14f6cf717f8091ba96caf95
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772579"
---
# <a name="combine-receipts-on-a-single-invoice"></a><span data-ttu-id="3c691-103">Zusammenfassen von Lieferungen in einer einzelnen Rechnung</span><span class="sxs-lookup"><span data-stu-id="3c691-103">Combine Receipts on a Single Invoice</span></span>

<span data-ttu-id="3c691-104">Wenn Sie mehrere Einkaufslieferungen gleichzeitig fakturieren möchten, können Sie die Funktion **Sammelgutschrift** verwenden.</span><span class="sxs-lookup"><span data-stu-id="3c691-104">If you want to invoice more than one purchase receipt at a time, you can use the **Combine Receipts** function.</span></span>  

<span data-ttu-id="3c691-105">Bevor Sie eine zusammengefassten Einkaufslieferung erstellen können, müssen Sie mehrere Einkaufslieferungen für den gleichen Debitor in der gleichen Währung gebucht haben.</span><span class="sxs-lookup"><span data-stu-id="3c691-105">Before you can create a combined purchase receipt, more than one receipt from the same vendor in the same currency must be posted.</span></span> <span data-ttu-id="3c691-106">Anders ausgedrückt: Sie müssen mindestens zwei Einkaufsbestellungen ausgefüllt und als geliefert (aber nicht fakturiert) gebucht haben.</span><span class="sxs-lookup"><span data-stu-id="3c691-106">In other words, you must have filled in two or more purchase orders and posted them as received, but not invoiced.</span></span>  

<span data-ttu-id="3c691-107">Wenn Einkaufslieferungen in einer Rechnung zusammengefasst und gebucht werden, wird für die fakturierten Zeilen eine gebuchte Einkaufsrechnung erstellt.</span><span class="sxs-lookup"><span data-stu-id="3c691-107">When purchase receipts are combined on an invoice and posted, then a posted purchase invoice is created for the invoiced lines.</span></span> <span data-ttu-id="3c691-108">Das Feld **Menge fakturiert** auf der Ursprungseinkaufsbestellung oder der Rahmenbestellung wird ausgehend von der fakturierten Menge aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3c691-108">The **Quantity Invoiced** field on the originating purchase order, or blanket purchase order, is updated based on the invoiced quantity.</span></span> <span data-ttu-id="3c691-109">Der ursprüngliche Beleg wird jedoch nicht gelöscht, auch wenn er vollständig geliefert und fakturiert wurde, und Sie müssen daher den Einkaufsbeleg löschen.</span><span class="sxs-lookup"><span data-stu-id="3c691-109">However, this original purchase document is not deleted, even if it has been fully received and invoiced, and you must therefore delete the purchase document.</span></span>  

> [!NOTE]
> <span data-ttu-id="3c691-110">Die resultierende Einkaufsrechnung kann später nicht mehr korrigiert oder storniert werden.</span><span class="sxs-lookup"><span data-stu-id="3c691-110">The resulting purchase invoice cannot later be corrected or canceled.</span></span> <span data-ttu-id="3c691-111">Wenn Sie eine auf diese Weise erstellte Einkaufsrechnung ändern möchten, müssen Sie Einkaufgutschriften verwenden.</span><span class="sxs-lookup"><span data-stu-id="3c691-111">If you want to modify a purchase invoice that is created in this way, you must use purchase credit memos.</span></span> <span data-ttu-id="3c691-112">Weitere Informationen finden Sie unter [Ändern oder löschen von unbezahlten Einkaufsrechnungen](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="3c691-112">For more information, see [Correct or Cancel Unpaid Purchase Invoices](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).</span></span>

## <a name="to-combine-receipts"></a><span data-ttu-id="3c691-113">So fassen Sie Wareneingänge zusammen</span><span class="sxs-lookup"><span data-stu-id="3c691-113">To combine receipts</span></span>

1. <span data-ttu-id="3c691-114">Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Einkaufsrechnungen** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="3c691-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3c691-115">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="3c691-115">Choose the **New** action.</span></span> <span data-ttu-id="3c691-116">Weitere Informationen finden Sie unter [Erfassen eines Einkaufs](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="3c691-116">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>  
3. <span data-ttu-id="3c691-117">Klicken Sie im Inforegister **Zeilen** und wählen die  Aktionen **Wareneingangszeilen holen**.</span><span class="sxs-lookup"><span data-stu-id="3c691-117">On the **Lines** FastTab, choose the **Get Receipt Lines** action.</span></span>  
4. <span data-ttu-id="3c691-118">Wählen Sie die Wareneingangszeilen aus, die in der Rechnung enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="3c691-118">Select multiple receipt lines that you want to include in the invoice.</span></span>  

    <span data-ttu-id="3c691-119">Wenn Sie eine falsche Wareneingangszeile ausgewählt haben oder von vorn beginnen möchten, können Sie einfach die Zeilen in der Einkaufsrechnung löschen und die Funktion **Wareneingangszeilen holen** erneut ausführen.</span><span class="sxs-lookup"><span data-stu-id="3c691-119">If an incorrect receipt line was selected or you want to start over, you can just delete the lines on the purchase invoice and then use the **Get Receipt Lines** function again.</span></span>  
5. <span data-ttu-id="3c691-120">Um die Rechnung zu buchen, wählen Sie die Aktion **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="3c691-120">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a><span data-ttu-id="3c691-121">Offene Einkaufsreklamationen nach kombinierter Lieferungsbuchung entfernen</span><span class="sxs-lookup"><span data-stu-id="3c691-121">To remove open purchase orders after combined receipt posting</span></span>

1. <span data-ttu-id="3c691-122">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Fakturierte Einkaufsbestellungen löschen** ein und wählen Sie den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="3c691-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Invoiced Purchase Orders**, and select the related link.</span></span>  
2. <span data-ttu-id="3c691-123">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="3c691-123">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="3c691-124">.</span><span class="sxs-lookup"><span data-stu-id="3c691-124">.</span></span>
3. <span data-ttu-id="3c691-125">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="3c691-125">Choose the **OK** button.</span></span>  

<span data-ttu-id="3c691-126">Alternativ löschen Sie die jeweiligen Aufträge manuell.</span><span class="sxs-lookup"><span data-stu-id="3c691-126">Alternatively, delete the individual orders manually.</span></span>

<span data-ttu-id="3c691-127">Wiederholen Sie die Schritte 1 bis 3 für alle betroffenen anderen Belege, wie z. B. Rahmenbestellungen.</span><span class="sxs-lookup"><span data-stu-id="3c691-127">Repeat steps 1 through 3 for any other affected documents, such as blanket purchase orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="3c691-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c691-128">See Also</span></span>

[<span data-ttu-id="3c691-129">Einkauf</span><span class="sxs-lookup"><span data-stu-id="3c691-129">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="3c691-130">Ändern oder Löschen einer unbezahlten Einkaufsrechnung</span><span class="sxs-lookup"><span data-stu-id="3c691-130">Correct or Cancel Unpaid Purchase Invoices</span></span>](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
<span data-ttu-id="3c691-131">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3c691-131">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]