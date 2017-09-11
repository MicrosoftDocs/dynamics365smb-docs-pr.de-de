---
title: 'Gewusst wie: Aktivieren von Debitoren-Zahlungen durch Zahlungsverkehr.| Microsoft Docs'
description: "Macht es für Debitoren einfacher, die Rechnungen durch Aktivierung des Zahlungsverkehrs zu bezahlen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 49e75c5f43b495bfc053c58b27e06feace62971c
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-enable-customer-payments-through-payment-services"></a><span data-ttu-id="a1ff9-103">Gewusst wie: Aktivieren von Debitoren-Zahlungen durch Zahlungsverkehr</span><span class="sxs-lookup"><span data-stu-id="a1ff9-103">How to: Enable Customer Payments Through Payment Services</span></span>
<span data-ttu-id="a1ff9-104">Als Alternative zu Zahlungen per Banktransfer oder Kreditkarten können Sie Ihren Debitoren anbieten, über Paypal oder WorldPay zu bezahlen.</span><span class="sxs-lookup"><span data-stu-id="a1ff9-104">As an alternative to collecting payments through bank transfer or credit cards, your customers can pay you through their account with payment services, such as PayPal or WorldPay.</span></span>  

<span data-ttu-id="a1ff9-105">Nachdem Sie einen Zahlungsverkehr in [!INCLUDE[d365fin](includes/d365fin_md.md)], wird ein Link zum Service auf Verkaufsbelegen verfügbar, den Sie per E-Mail an Ihren Geschäftspartner senden können.</span><span class="sxs-lookup"><span data-stu-id="a1ff9-105">After you enable a payment service in [!INCLUDE[d365fin](includes/d365fin_md.md)], a link to the service is available on sales documents that you send by email to your customers.</span></span> <span data-ttu-id="a1ff9-106">Debitoren können den Link verwenden, um zum Zahlungsverkehr zu wechseln und die Rechnung direkt über das Verkaufsdokument zu bezahlen.</span><span class="sxs-lookup"><span data-stu-id="a1ff9-106">Customers can use the link to go to the payment service and pay the bill, directly from the sales document.</span></span> <span data-ttu-id="a1ff9-107">Wenn Sie nicht den Link hinzufügen möchten, beispielsweise wenn ein Kunde in Bar bezahlt, können Sie den Zahlungsverkehr von der Rechnung entfernen, bevor Sie buchen.</span><span class="sxs-lookup"><span data-stu-id="a1ff9-107">If you don't want to include the link, for example, if a customer will pay with cash, you can remove the payment service from the invoice before posting.</span></span>  

<span data-ttu-id="a1ff9-108">Der Paypal-Zahlungs-Standard und die WorldPay-Zahlungsstandarderweiterungen werden erfasst in [!INCLUDE[d365fin](includes/d365fin_md.md)] und stehen zur Aktivierung bereit.</span><span class="sxs-lookup"><span data-stu-id="a1ff9-108">The PayPal Payments Standard and WorldPay Payments Standard extensions are installed in [!INCLUDE[d365fin](includes/d365fin_md.md)], and are ready for you to enable.</span></span>  

## <a name="to-enable-a-payment-service-in-included365finincludesd365finmdmd"></a><span data-ttu-id="a1ff9-109">Einen Zahlungsverkehr in [!INCLUDE[d365fin](includes/d365fin_md.md)] aktivieren</span><span class="sxs-lookup"><span data-stu-id="a1ff9-109">To enable a payment service in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>
1. <span data-ttu-id="a1ff9-110">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Zahlungsverkehr** ein und wählen den zugehörenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="a1ff9-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="a1ff9-111">Wählen Sie im Fenster **Zahlungsverkehr** die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="a1ff9-111">In the **Payment Services** window, choose the **New** action.</span></span>  
3. <span data-ttu-id="a1ff9-112">Wählen Sie die Zahlungsverkehr aus und schließen Sie dann das Fenster.</span><span class="sxs-lookup"><span data-stu-id="a1ff9-112">Select the payment service, and then close the window.</span></span>  
4. <span data-ttu-id="a1ff9-113">Wählen Sie im Fenster **Zahlungsverkehr** die Aktion **Einrichten** aus.</span><span class="sxs-lookup"><span data-stu-id="a1ff9-113">In the **Payment Services** window, choose the **Setup** action.</span></span>  
5. <span data-ttu-id="a1ff9-114">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="a1ff9-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. <span data-ttu-id="a1ff9-115">Schließen Sie das Fenster.</span><span class="sxs-lookup"><span data-stu-id="a1ff9-115">Close the window.</span></span>  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a><span data-ttu-id="a1ff9-116">Einen Zahlungsverkehr in einer Verkaufsrechnung auswählen</span><span class="sxs-lookup"><span data-stu-id="a1ff9-116">To select a payment service on a sales invoice</span></span>
1. <span data-ttu-id="a1ff9-117">Auf der Startseite wählen Sie **Verkaufsrechnung** aus.</span><span class="sxs-lookup"><span data-stu-id="a1ff9-117">On the Home page, choose **Sales Invoices**.</span></span>  
2. <span data-ttu-id="a1ff9-118">Öffnen Sie die Verkaufsrechnung, die Sie zahlen möchten, indem Sie den Zahlungsverkehr verwenden.</span><span class="sxs-lookup"><span data-stu-id="a1ff9-118">Open the sales invoice that you want to pay by using the payment service.</span></span>  
3. <span data-ttu-id="a1ff9-119">Geben Sie im Feld **Zahlungsverkehr** den Zahlungsservice ein.</span><span class="sxs-lookup"><span data-stu-id="a1ff9-119">In the **Payment Service** field, choose the payment service.</span></span>  
  
    > [!NOTE]  
>   <span data-ttu-id="a1ff9-120">Das Feld **Zahlungsverkehr** ist verfügbar, wenn Sie den Zahlungsservice aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="a1ff9-120">The **Payment Service** field is available only if you've enabled the payment service.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a1ff9-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1ff9-121">See Also</span></span>  
[<span data-ttu-id="a1ff9-122">Einrichten von Verkäufen</span><span class="sxs-lookup"><span data-stu-id="a1ff9-122">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="a1ff9-123">Verkauf</span><span class="sxs-lookup"><span data-stu-id="a1ff9-123">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="a1ff9-124">[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="a1ff9-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="a1ff9-125">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a1ff9-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

