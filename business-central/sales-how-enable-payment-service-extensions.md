---
title: 'Gewusst wie: Aktivieren von Debitoren-Zahlungen durch Zahlungsverkehr.| Microsoft Docs'
description: Macht es für Debitoren einfacher, die Rechnungen durch Aktivierung des Zahlungsverkehrs zu bezahlen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: eac58a651989fff8b1d2cc6b6dbed2a380ae8ef8
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "797930"
---
# <a name="enable-customer-payments-through-payment-services"></a><span data-ttu-id="a5466-103">Gewusst wie: Aktivieren von Debitoren-Zahlungen durch Zahlungsverkehr</span><span class="sxs-lookup"><span data-stu-id="a5466-103">Enable Customer Payments Through Payment Services</span></span>
<span data-ttu-id="a5466-104">Als Alternative zu Zahlungen per Banktransfer oder Kreditkarten können Sie Ihren Debitoren anbieten, über Microsoft Pay, Paypal oder WorldPay zu bezahlen.</span><span class="sxs-lookup"><span data-stu-id="a5466-104">As an alternative to collecting payments through bank transfer or credit cards, your customers can pay you through their account with payment services, such as Microsoft Pay, PayPal, or WorldPay.</span></span>  

<span data-ttu-id="a5466-105">Nachdem Sie einen Zahlungsverkehr in [!INCLUDE[d365fin](includes/d365fin_md.md)], wird ein Link zum Service auf Verkaufsbelegen verfügbar, den Sie per E-Mail an Ihren Geschäftspartner senden können.</span><span class="sxs-lookup"><span data-stu-id="a5466-105">After you enable a payment service in [!INCLUDE[d365fin](includes/d365fin_md.md)], a link to the service is available on sales documents that you send by email to your customers.</span></span> <span data-ttu-id="a5466-106">Debitoren können den Link verwenden, um zum Zahlungsverkehr zu wechseln und die Rechnung direkt über das Verkaufsdokument zu bezahlen.</span><span class="sxs-lookup"><span data-stu-id="a5466-106">Customers can use the link to go to the payment service and pay the bill, directly from the sales document.</span></span> <span data-ttu-id="a5466-107">Wenn Sie nicht den Link hinzufügen möchten, beispielsweise wenn ein Debitor in Bar bezahlt, können Sie den Zahlungsverkehr von der Rechnung entfernen, bevor Sie buchen.</span><span class="sxs-lookup"><span data-stu-id="a5466-107">If you don't want to include the link, for example, if a customer will pay with cash, you can remove the payment service from the invoice before posting.</span></span>  

<span data-ttu-id="a5466-108">Der Microsoft Pay, PayPal Payments Standard und die WorldPay Payments Standard-Erweiterungen werden installiert in [!INCLUDE[d365fin](includes/d365fin_md.md)] und stehen zur Aktivierung bereit.</span><span class="sxs-lookup"><span data-stu-id="a5466-108">The Microsoft Pay, PayPal Payments Standard, and WorldPay Payments Standard extensions are installed in [!INCLUDE[d365fin](includes/d365fin_md.md)], and are ready for you to enable.</span></span>  

## <a name="to-enable-a-payment-service-in-included365finincludesd365finmdmd"></a><span data-ttu-id="a5466-109">Einen Zahlungsverkehr in [!INCLUDE[d365fin](includes/d365fin_md.md)] aktivieren</span><span class="sxs-lookup"><span data-stu-id="a5466-109">To enable a payment service in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>
1. <span data-ttu-id="a5466-110">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Zahlungsverkehr** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="a5466-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="a5466-111">Wählen Sie auf der Seite **Zahlungsverkehr** die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="a5466-111">On the **Payment Services** page, choose the **New** action.</span></span>  
3. <span data-ttu-id="a5466-112">Wählen Sie die Zahlungsverkehr aus und schließen Sie dann die Seite.</span><span class="sxs-lookup"><span data-stu-id="a5466-112">Select the payment service, and then close the page.</span></span>  
4. <span data-ttu-id="a5466-113">Wählen Sie auf der Seite **Zahlungsverkehr** die Aktion **Einrichten** aus.</span><span class="sxs-lookup"><span data-stu-id="a5466-113">On the **Payment Services** page, choose the **Setup** action.</span></span>  
5. <span data-ttu-id="a5466-114">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="a5466-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. <span data-ttu-id="a5466-115">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="a5466-115">Close the page.</span></span>  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a><span data-ttu-id="a5466-116">Einen Zahlungsverkehr in einer Verkaufsrechnung auswählen</span><span class="sxs-lookup"><span data-stu-id="a5466-116">To select a payment service on a sales invoice</span></span>
1. <span data-ttu-id="a5466-117">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Verkaufsrechnung** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="a5466-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="a5466-118">Öffnen Sie die Verkaufsrechnung, die Sie zahlen möchten, indem Sie den Zahlungsverkehr verwenden.</span><span class="sxs-lookup"><span data-stu-id="a5466-118">Open the sales invoice that you want to pay by using the payment service.</span></span>  
3. <span data-ttu-id="a5466-119">Geben Sie im Feld **Zahlungsverkehr** den Zahlungsservice ein.</span><span class="sxs-lookup"><span data-stu-id="a5466-119">In the **Payment Service** field, choose the payment service.</span></span>  

    > [!NOTE]  
    > <span data-ttu-id="a5466-120">Das Feld **Zahlungsverkehr** ist verfügbar, wenn Sie den Zahlungsservice aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="a5466-120">The **Payment Service** field is available only if you've enabled the payment service.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a5466-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5466-121">See Also</span></span>  
[<span data-ttu-id="a5466-122">Einrichten von Verkäufen</span><span class="sxs-lookup"><span data-stu-id="a5466-122">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="a5466-123">Verkauf</span><span class="sxs-lookup"><span data-stu-id="a5466-123">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="a5466-124">[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="a5466-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="a5466-125">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a5466-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
