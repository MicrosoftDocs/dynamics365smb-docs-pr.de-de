---
title: 'Vorgehensweise: Vorauszahlungen korrigieren | Microsoft Docs'
description: Sie können eine Korrektur an einem Auftrag vornehmen, nachdem Sie eine Vorauszahlungsrechnung für den Auftrag gebucht haben. Sie können einem Auftrag auch nach dem Versand einer Vorauszahlungsrechnung noch weitere Zeilen hinzufügen, und Sie können dann eine weitere Vorauszahlungsrechnung buchen, Sie können jedoch keine Zeile mehr aus einem Auftrag löschen, nachdem für die Zeile eine Vorauszahlung fakturiert wurde.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0934cfedb7fa2e387e7d1bdcfbabb3ad45b2133e
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2882734"
---
# <a name="correct-prepayments"></a><span data-ttu-id="94bee-104">So korrigieren Sie Vorauszahlungen</span><span class="sxs-lookup"><span data-stu-id="94bee-104">Correct Prepayments</span></span>
<span data-ttu-id="94bee-105">Sie können eine Korrektur an einem Auftrag vornehmen, nachdem Sie eine Vorauszahlungsrechnung für den Auftrag gebucht haben.</span><span class="sxs-lookup"><span data-stu-id="94bee-105">You can make a correction to an order after you have posted a prepayment invoice for the order.</span></span> <span data-ttu-id="94bee-106">Sie können einem Auftrag auch nach dem Versand einer Vorauszahlungsrechnung noch weitere Zeilen hinzufügen, und Sie können dann eine weitere Vorauszahlungsrechnung buchen, Sie können jedoch keine Zeile mehr aus einem Auftrag löschen, nachdem für die Zeile eine Vorauszahlung fakturiert wurde.</span><span class="sxs-lookup"><span data-stu-id="94bee-106">You can add new lines to an order after issuing a prepayment, and then you can post another prepayment invoice, but you cannot delete a line from an order after a prepayment has been invoiced for the line.</span></span>  

## <a name="to-correct-a-prepayment"></a><span data-ttu-id="94bee-107">So korrigieren Sie eine Vorauszahlung</span><span class="sxs-lookup"><span data-stu-id="94bee-107">To correct a prepayment</span></span>
<span data-ttu-id="94bee-108">Das folgende Verfahren zeigt, wie Sie eine Vorauszahlungsgutschrift ausstellen, um alle fakturierten Vorauszahlungen für einen Auftrag zu stornieren.</span><span class="sxs-lookup"><span data-stu-id="94bee-108">The following procedure shows how to issue a prepayment credit memo to cancel all invoiced prepayments for a sales order.</span></span>  
1. <span data-ttu-id="94bee-109">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Verkaufsaufträge** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="94bee-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="94bee-110">Öffnen Sie den entsprechenden Verkaufsauftrag.</span><span class="sxs-lookup"><span data-stu-id="94bee-110">Open the relevant sales order.</span></span>
3. <span data-ttu-id="94bee-111">Wählen Sie die Aktion **Vorauszahlung**, und dann die Aktion **Vorauszahlungsgutschrift buchen** oder **Vorauszahlungsgutschrift buchen und drucken**.</span><span class="sxs-lookup"><span data-stu-id="94bee-111">Choose the **Prepayment** action, and then choose the **Post Prepayment Credit Memo** action or the **Post and Print Prepmt. Cr. Memo** action.</span></span>  
4. <span data-ttu-id="94bee-112">Korrigieren Sie auf der Seite **Verkaufsgutschrift** alle relevanten Positionen für alle Verkaufsgutschriften.</span><span class="sxs-lookup"><span data-stu-id="94bee-112">On the **Sales Credit Memo** page, proceed to correct the relevant entries, as for any sales credit memo.</span></span> <span data-ttu-id="94bee-113">Weitere Informationen finden Sie unter [Retouren verarbeiten oder Stornieren](sales-how-process-sales-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="94bee-113">For more information, see [Process Sales Returns or Cancellations](sales-how-process-sales-returns-cancellations.md).</span></span>     

    > [!NOTE]  
    > <span data-ttu-id="94bee-114">Um den Betrag im Feld **Positionsbetrag** zu reduzieren, müssen Sie zuerst den Vorauszahlungsprozentsatz in der Zeile erhöhen, damit der Wert im Feld **Vorauszahlungszeilenbetrag** nicht unter den Wert im Feld **Fakt. Vorauszahlungsbetrag** fällt.</span><span class="sxs-lookup"><span data-stu-id="94bee-114">To Reduce the amount in the **Line Amount** field, you must first increase the prepayment percentage on the line so that the value in the **Prepmt. Line Amount** field is not decreased below the value in the **Prepmt. Amt. Inv.** field.</span></span>

5. <span data-ttu-id="94bee-115">Um eine Vorauszahlungsrechnung für neuen Zeilen in der Vorauszahlungsgutschrift zu erstellen, wählen Sie die Aktion **Vorauszahlung**, und dann die Aktion **Vorauszahlungsrechnung buchen** oder **Vorauszahlungsrechnung buchen und drucken**.</span><span class="sxs-lookup"><span data-stu-id="94bee-115">To make a prepayment invoice for any new lines in the sales credit memo, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action or the **Post and Print Prepmt. Invoice** action.</span></span>  
6. <span data-ttu-id="94bee-116">Um eine zusätzliche Vorauszahlungsrechnung zu erstellen, erhöhen Sie den Vorauszahlungsbetrag in einer oder mehreren Zeilen, und buchen die Vorauszahlungsrechnung.</span><span class="sxs-lookup"><span data-stu-id="94bee-116">To issue an additional prepayment invoice, increase the prepayment amount on one or more lines and post the prepayment invoice.</span></span> <span data-ttu-id="94bee-117">Für die Differenz zwischen dem fakturierten Vorauszahlungsbetrag und den neuen Vorauszahlungsbeträgen wird eine neue Rechnung erstellt.</span><span class="sxs-lookup"><span data-stu-id="94bee-117">A new invoice will be created for the difference between the prepayment amounts invoiced and the new prepayment amounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="94bee-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94bee-118">See Also</span></span>  
[<span data-ttu-id="94bee-119">Fakturieren von Vorauszahlungen</span><span class="sxs-lookup"><span data-stu-id="94bee-119">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="94bee-120">Exemplarische Vorgehensweise: Einrichten und Fakturieren von Verkaufsvorauszahlungen</span><span class="sxs-lookup"><span data-stu-id="94bee-120">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="94bee-121">Finanzen</span><span class="sxs-lookup"><span data-stu-id="94bee-121">Finance</span></span>](finance.md)  
<span data-ttu-id="94bee-122">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="94bee-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
