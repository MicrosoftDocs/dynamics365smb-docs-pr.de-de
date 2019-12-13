---
title: Zahlungsformen einrichten| Microsoft Docs
description: Sie können Zahlungsformen nutzen, z.B. Banküberweisung, Kasse oder Paypal, um festzulegen, wie eine Rechnung bezahlt wird.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, bank transfer, cash, PayPal
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 753b9f30648059a68c22b524008e21c6c866d19c
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2882542"
---
# <a name="defining-payment-methods"></a><span data-ttu-id="9f3c9-103">Zahlungsformen definieren</span><span class="sxs-lookup"><span data-stu-id="9f3c9-103">Defining Payment Methods</span></span>
<span data-ttu-id="9f3c9-104">Zahlungsformen definieren die Art, wie Sie es vorziehen, dass Debitoren Sie zahlen und wie Sie den Kreditoren bezahlen können.</span><span class="sxs-lookup"><span data-stu-id="9f3c9-104">Payment methods define the way you prefer for customers to pay you, and how you like to pay your vendors.</span></span> <span data-ttu-id="9f3c9-105">Die Methode kann für jeden Debitor oder Kreditor variieren.</span><span class="sxs-lookup"><span data-stu-id="9f3c9-105">The method can vary for each customer or vendor.</span></span> <span data-ttu-id="9f3c9-106">Beispiele für typische Zahlungsformen sind **Bankkonten**, **Bargeld**, **Check** oder **Konto**.</span><span class="sxs-lookup"><span data-stu-id="9f3c9-106">Examples of typical payment methods are **bank**, **cash**, **check**, or **account**.</span></span>

<span data-ttu-id="9f3c9-107">Sie können eine Zahlungsform Debitoren und Kreditoren zuweisen, sodass dasselbe Verfahren immer auf Verkaufs- und Einkaufsbelegen verwendet wird, die Sie für sie einrichten.</span><span class="sxs-lookup"><span data-stu-id="9f3c9-107">You can assign a payment method to customers and vendors so that the same method is always used on the sales and purchase documents you create for them.</span></span> <span data-ttu-id="9f3c9-108">Bei Bedarf können Sie die Methode im Einkaufs- und Verkaufsbeleg ändern.</span><span class="sxs-lookup"><span data-stu-id="9f3c9-108">If needed, you can change the method on the sales or purchase document.</span></span> <span data-ttu-id="9f3c9-109">Wenn Sie beispielsweise eine bestimmte Einkaufsrechnung in bar anstatt mit Scheck bezahlen möchten.</span><span class="sxs-lookup"><span data-stu-id="9f3c9-109">For example, if you want to pay a particular purchase invoice in cash rather than by check.</span></span> <span data-ttu-id="9f3c9-110">Dies verändert nicht die standardmäßige Zahlungsform, die dem Kreditor zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9f3c9-110">This does not change the default payment method assigned to the vendor.</span></span>

<span data-ttu-id="9f3c9-111">Die gleichen Zahlungsformen werden für Einkaufs- und Verkaufsbelegen verwendet.</span><span class="sxs-lookup"><span data-stu-id="9f3c9-111">The same payment methods are used for sales and purchase documents.</span></span> <span data-ttu-id="9f3c9-112">Beispielsweise wird eine _cash_ Zahlungsform verwendet, wenn Sie Zahlungen leisten und wenn Sie den Wareneingang erhalten.</span><span class="sxs-lookup"><span data-stu-id="9f3c9-112">For example, a _cash_ payment method is used both when you make payments and when you receive them.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="9f3c9-113">weiß, dass wenn Sie eine Verkaufsrechnung erstellen, Sie eine Zahlung erwarten und das Gegenteil der Einkaufsrechnungen ist.</span><span class="sxs-lookup"><span data-stu-id="9f3c9-113">knows that when you are creating a sales invoice you expect to receive payment, and the opposite for purchase invoices.</span></span>

<span data-ttu-id="9f3c9-114">Gutschriften für Reklamationen sind jedoch Ausnahmen, da Geld entgegengesetzt fließt, von Ihnen an Ihren Kunden und von Ihrem Lieferanten an Sie.</span><span class="sxs-lookup"><span data-stu-id="9f3c9-114">Credit memos for returns, however, are exceptions because money is flowing in the opposite directions, from you to your customer and from your vendor to you.</span></span> <span data-ttu-id="9f3c9-115">Daher wird eine standardmäßige Zahlungsform nicht den Gutschriften zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9f3c9-115">Therefore, a default payment method is not assigned to credit memos.</span></span> <span data-ttu-id="9f3c9-116">Es gibt eine Problemumgehung, wenn Sie Zahlungsfristen des Debitors oder Kreditors angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="9f3c9-116">There is, however, a workaround if you have specified terms of payment for the customer or vendor.</span></span> <span data-ttu-id="9f3c9-117">Auch wenn das **Rechnungsrab. Zahl. Verk. im Zinsrechnung** Feld nicht für dies beabsichtigt ist, wenn Sie das Feld **Zahlungsbedingungen** auswählen, wird eine standardmäßige Zahlungsform hinzugefügt, wenn Sie eine Gutschrift erstellen.</span><span class="sxs-lookup"><span data-stu-id="9f3c9-117">Though the **Calc. Pmt. Disc. on Cr. Memos** field is not intended for this, if you choose the check box on the **Payment Terms** page a default payment method will be added when you create a credit memo.</span></span> <br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE476Ys]

## <a name="to-set-up-a-payment-method"></a><span data-ttu-id="9f3c9-118">So richten Sie eine Zahlungsform ein</span><span class="sxs-lookup"><span data-stu-id="9f3c9-118">To set up a payment method</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="9f3c9-119">enthält mehrere Zahlungsformen, die Geschäfte häufig verwenden.</span><span class="sxs-lookup"><span data-stu-id="9f3c9-119">provides a few payment methods that businesses often use.</span></span> <span data-ttu-id="9f3c9-120">Sie können so viele Zeilen hinzufügen, wie Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="9f3c9-120">You can, however, add as many as you need.</span></span>

1. <span data-ttu-id="9f3c9-121">Wählen Sie die ![Glühbirne, die das Symbol Tell Me öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Zahlungsformen** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="9f3c9-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Methods**, and then choose the related link.</span></span>
2. <span data-ttu-id="9f3c9-122">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="9f3c9-122">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-a-payment-method-to-a-customer-or-vendor"></a><span data-ttu-id="9f3c9-123">So weisen Sie einem Kreditor eine Zahlungsform zu</span><span class="sxs-lookup"><span data-stu-id="9f3c9-123">To assign a payment method to a customer or vendor</span></span>
1. <span data-ttu-id="9f3c9-124">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Kunde** oder **Lieferant** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="9f3c9-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customer** or **Vendor**, and then choose the related link.</span></span>
2. <span data-ttu-id="9f3c9-125">Im **Zahlungsformcode** Feld wählen Sie die Methode, die Sie für den Debitor oder Kreditor standardmäßig verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="9f3c9-125">In the **Payment Method Code** field, choose the method to use by default for the customer or vendor.</span></span>

## <a name="see-also"></a><span data-ttu-id="9f3c9-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f3c9-126">See Also</span></span>
[<span data-ttu-id="9f3c9-127">Registriert einen neuen Debitor.</span><span class="sxs-lookup"><span data-stu-id="9f3c9-127">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="9f3c9-128">Finanzen</span><span class="sxs-lookup"><span data-stu-id="9f3c9-128">Finance</span></span>](finance.md)  
<span data-ttu-id="9f3c9-129">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9f3c9-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
