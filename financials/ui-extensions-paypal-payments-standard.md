---
title: Nutzung der Paypal-Zahlungs-Standard-Erweiterung| Microsoft Docs
description: Beschreibt, wie die Erweiterung verwendet wird, um Debitoren zu aktivieren, um Zahlungen mit Paypal zu leisten.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 43511c3c509c495555f4583fdbe982d8b98aa648
ms.contentlocale: de-de
ms.lasthandoff: 11/10/2017

---
# <a name="the-paypal-payments-standard-extension-to-dynamics-365-business-edition"></a><span data-ttu-id="76a06-103">Die Paypal-Zahlungs-Standarderweiterung für Dynamics 365 Business edition</span><span class="sxs-lookup"><span data-stu-id="76a06-103">The PayPal Payments Standard Extension to Dynamics 365 Business edition</span></span> 
<span data-ttu-id="76a06-104">Debitoren erfordern regelmäßig höheren Kundenservice, sowohl in Bezug auf Produktqualität wie auch in Bezug auf Lieferungs- und Zahlungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="76a06-104">Customers continuously require higher customer service, both in terms of product quality but also in terms of delivery and payment options.</span></span> <span data-ttu-id="76a06-105">Mit dem Paypal-Zahlungsstandard-Service erhöhen Sie Ihren Kundenservice.</span><span class="sxs-lookup"><span data-stu-id="76a06-105">The PayPal Payments Standard service helps you increase your customer service.</span></span>

<span data-ttu-id="76a06-106">Als Alternative zu Zahlungen per Banktransfer oder Kreditkarten können Sie Ihren Debitoren anbieten, über Paypal zu bezahlen.</span><span class="sxs-lookup"><span data-stu-id="76a06-106">As an alternative to collecting payments through bank transfer or credit cards, you can offer your customers to pay you through their PayPal account.</span></span> <span data-ttu-id="76a06-107">Wenn Sie eine Verkaufsrechnung oder einen Verkaufsauftrag per E-Mail versenden, hat es einen Paypal-Link im E-Mail-Text und im angefügten PDF-Dokument.</span><span class="sxs-lookup"><span data-stu-id="76a06-107">When you send a sales invoice or sales order by email, there is a PayPal link in the email body and in the attached PDF document.</span></span> <span data-ttu-id="76a06-108">Wenn der Debitor den Link auswählt, erscheint die Service-Seite für Ihr Paypal-Konto mit den Zahlungsdetails für den Verkauf.</span><span class="sxs-lookup"><span data-stu-id="76a06-108">When the customer chooses the link, the service page for their PayPal account appears showing the payment details for the sale.</span></span> <span data-ttu-id="76a06-109">Der Kunde kann die Rechnung wie jede andere PayPal-Zahlung bezahlen.</span><span class="sxs-lookup"><span data-stu-id="76a06-109">The customer can then pay the invoice as any other PayPal payment.</span></span>

<span data-ttu-id="76a06-110">Der Paypal-Zahlungsstandard-Service hat folgende Vorteile:</span><span class="sxs-lookup"><span data-stu-id="76a06-110">The PayPal Payments Standard service provides the following benefits:</span></span>

* <span data-ttu-id="76a06-111">Debitorenzahlungen sind schneller auf Ihrem Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="76a06-111">Customer payments arrive faster in your bank account.</span></span>
* <span data-ttu-id="76a06-112">Debitoren haben mehr Arten, Rechnungen zu bezahlen.</span><span class="sxs-lookup"><span data-stu-id="76a06-112">Customers have more ways to pay invoices.</span></span>
* <span data-ttu-id="76a06-113">Paypal bietet einen vertrauenswürdigen Zahlungsservice an, den Debitoren gegenüber der Eingabe von Kreditkarteninformationen auf der Websites bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="76a06-113">PayPal offers a trustworthy payment service, which customers prefer to entering credit card information on web sites.</span></span>
* <span data-ttu-id="76a06-114">Paypal bietet mehrere Arten zur Zahlungsabwicklung an, einschließlich Kreditkartenverarbeitung, Paypal-Konten und andere Quellen.</span><span class="sxs-lookup"><span data-stu-id="76a06-114">PayPal offers multiple ways of handling payments, including credit card processing, PayPal accounts, and other sources.</span></span>
* <span data-ttu-id="76a06-115">Der Paypal-Link kann automatisch allen Verkaufsdokumenten oder manuell vom Benutzer hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="76a06-115">The PayPal link can be added automatically to sales documents or manually by the user.</span></span>
* <span data-ttu-id="76a06-116">Der Paypal-Zahlungsstandard-Service kostet keine Monatsgebühren oder Gebühren für die Einrichtung.</span><span class="sxs-lookup"><span data-stu-id="76a06-116">The PayPal Payments Standard service does not involve monthly fees or setup fees.</span></span>
* <span data-ttu-id="76a06-117">Da dies eine Erweiterung ist, können Sie den Paypal-Zahlungsstandard-Service einfach aktivieren wenn und wenn Ihr Geschäft sie benötigt.</span><span class="sxs-lookup"><span data-stu-id="76a06-117">Because it is an extension, you can easily enable the PayPal Payment Standard service when and if your business requires it.</span></span>  

<span data-ttu-id="76a06-118">Weitere Informationen finden Sie unter [Vorgehensweise: Aktivieren Sie Debitoren-Zahlung durch Paypal](sales-how-enable-payment-service-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="76a06-118">For more information, see [How to: Enable Customer Payment Through PayPal](sales-how-enable-payment-service-extensions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="76a06-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76a06-119">See Also</span></span>
<span data-ttu-id="76a06-120">[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="76a06-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="76a06-121">Einrichten von Verkäufen</span><span class="sxs-lookup"><span data-stu-id="76a06-121">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="76a06-122">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="76a06-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

