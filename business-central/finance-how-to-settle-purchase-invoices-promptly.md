---
title: Einkaufsrechnungen sofort ausgleichen
description: Wenn Sie den Kreditor bar oder per Scheck bezahlen, können Sie die notwendigen Buchungen gleichzeitig bei der Buchung der Rechnung vornehmen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 10/06/2020
ms.author: bholtorf
ms.openlocfilehash: fb442c7b1e9e7bdcb727ca6de157657e370e254f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746841"
---
# <a name="settle-purchase-invoices-promptly"></a><span data-ttu-id="c7887-103">Einkaufsrechnungen sofort ausgleichen</span><span class="sxs-lookup"><span data-stu-id="c7887-103">Settle Purchase Invoices Promptly</span></span>

<span data-ttu-id="c7887-104">Wenn Sie den Kreditor bar oder per Scheck bezahlen, können Sie die notwendigen Buchungen gleichzeitig bei der Buchung der Rechnung vornehmen.</span><span class="sxs-lookup"><span data-stu-id="c7887-104">If you need to pay the vendor by cash or check, you can post the payment when you post the invoice.</span></span>  

> [!NOTE]  
> <span data-ttu-id="c7887-105">Wenn Sie häufig Einkaufsrechnungen bar, per Scheck oder Banküberweisung bezahlen, ist es sinnvoll, eine bestimmte Zahlungsform mit einem Gegenkonto einzurichten und diese Methode im Feld **Zahlungsform** auf der Kreditorenkarte einzugeben.</span><span class="sxs-lookup"><span data-stu-id="c7887-105">If you frequently pay purchase invoices in cash, check, or bank transfer, it is a good idea to set up a specific payment method with a balancing account and enter this method in the **Payment Method** field on the vendor card.</span></span> <span data-ttu-id="c7887-106">Die entsprechende Gegenkontonummer wird automatisch auf dem Rechnungskopf eingefügt, wenn Sie eine neue Rechnung erstellen.</span><span class="sxs-lookup"><span data-stu-id="c7887-106">The balancing account number is inserted automatically on the invoice header every time you create a new invoice.</span></span> <span data-ttu-id="c7887-107">Weitere Informationen finden Sie unter [Zahlungsformen definieren](finance-payment-methods.md).</span><span class="sxs-lookup"><span data-stu-id="c7887-107">For more information, see [Defining Payment Methods](finance-payment-methods.md).</span></span>  

## <a name="to-settle-purchase-invoices-promptly"></a><span data-ttu-id="c7887-108">So gleichen Sie Einkaufsrechnungen sofort aus</span><span class="sxs-lookup"><span data-stu-id="c7887-108">To settle purchase invoices promptly</span></span>

1. <span data-ttu-id="c7887-109">Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Einkaufsrechnungen** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="c7887-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c7887-110">Wählen Sie die Aktion **Neu**.</span><span class="sxs-lookup"><span data-stu-id="c7887-110">Choose the **New** action.</span></span>  
3. <span data-ttu-id="c7887-111">Um entweder bar oder per Banktransfer zu bezahlen, geben Sie die Nummer des Sachkontos für Barzahlungen oder die des Bankkontos in dem Feld **Gegenkontonr.** an.</span><span class="sxs-lookup"><span data-stu-id="c7887-111">To pay either in cash or by bank transfer, enter the number of the general ledger cash account or the bank account in the **Bal. Account No.** field.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="c7887-112">Die Felder **Gegenkontoart** und **Gegenkontonr.** sind im Rechnungskopf nicht im Standard enthalten.</span><span class="sxs-lookup"><span data-stu-id="c7887-112">The **Bal. Account Type** and **Bal. Account No.** fields are not included in the standard layout of the invoice header.</span></span> <span data-ttu-id="c7887-113">Um die Zahlung einer Rechnung zu buchen, müssen Sie sich an einen Microsoft-Partner wenden, der die Felder per Code hinzufügen kann.</span><span class="sxs-lookup"><span data-stu-id="c7887-113">In order to post the payment of an invoice, you must contact a Microsoft partner who can add the fields through code.</span></span>  
>
> <span data-ttu-id="c7887-114">Diese Anpassung ist nur erforderlich, wenn Sie keine Gegenkonten zu den Zahlungsformen, wie oben beschrieben, angeben.</span><span class="sxs-lookup"><span data-stu-id="c7887-114">This customization is only required if you do not specify balancing accounts on the payment methods as describe above.</span></span>

## <a name="see-also"></a><span data-ttu-id="c7887-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7887-115">See Also</span></span>

[<span data-ttu-id="c7887-116">Verwalten von Verbindlichkeiten</span><span class="sxs-lookup"><span data-stu-id="c7887-116">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="c7887-117">Einkauf</span><span class="sxs-lookup"><span data-stu-id="c7887-117">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="c7887-118">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c7887-118">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
