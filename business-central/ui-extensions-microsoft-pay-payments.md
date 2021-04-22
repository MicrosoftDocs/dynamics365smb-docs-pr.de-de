---
title: Microsoft Pay Standard | Microsoft Docs
description: Enthält Informationen über die Microsoft Pay-Erweiterung
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 58c7ff08a7359b4f577b7ba40b23bc1f6310da4c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787327"
---
# <a name="the-microsoft-pay-extension"></a><span data-ttu-id="2c471-103">Die Microsoft Pay-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="2c471-103">The Microsoft Pay Extension</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2c471-104">Mit Wirkung zum 8. Februar 2020 wirken sich Änderungen im Microsoft Pay-Service auf die Microsoft Pay-Erweiterung in Microsoft [!INCLUDE[prod_short](includes/prod_long.md)] aus.</span><span class="sxs-lookup"><span data-stu-id="2c471-104">Effective February 8 2020, changes in the Microsoft Pay service will affect the Microsoft Pay extension in Microsoft [!INCLUDE[prod_short](includes/prod_long.md)].</span></span> <span data-ttu-id="2c471-105">Aufgrund der Änderungen öffnen die **Zahlen Sie jetzt**-Zahlungslinks, die die Microsoft Pay-Erweiterung für Rechnungen in [!INCLUDE[prod_short](includes/prod_short.md)] generiert, nach dem 8. Februar Microsoft Pay nicht.</span><span class="sxs-lookup"><span data-stu-id="2c471-105">Due to the changes, after February 8, the **Pay now** payment links that the Microsoft Pay extension generates for invoices in [!INCLUDE[prod_short](includes/prod_short.md)] will not open Microsoft Pay.</span></span> <span data-ttu-id="2c471-106">Kunden, die die Erweiterung verwenden, sollten ihre Zahlungsverkehrseinrichtung ändern, um stattdessen die PayPal-Erweiterung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="2c471-106">Customers who are using the extension should change their Payment Services setup to start using the PayPal extension instead.</span></span><br /></br>
>
> <span data-ttu-id="2c471-107">Ab dem 8. Januar wird in [!INCLUDE[prod_short](includes/prod_short.md)] eine Benachrichtigung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2c471-107">From January 8, we will display a notification in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="2c471-108">Die Benachrichtigung enthält einen Link zu den Einstellungen, die Sie ändern müssen, und zu weiteren Informationen.</span><span class="sxs-lookup"><span data-stu-id="2c471-108">The notification will contain a link to the settings that you need to change and to more information.</span></span> <span data-ttu-id="2c471-109">Nach dem 8. Februar ist die Microsoft Pay-Erweiterung nicht mehr in [!INCLUDE[prod_short](includes/prod_short.md)] verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2c471-109">After February 8, the Microsoft Pay extension will no longer be available in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span><br /></br>
>
> <span data-ttu-id="2c471-110">Die Änderungen wirken sich auf die folgenden Versionen von Business Central aus:</span><span class="sxs-lookup"><span data-stu-id="2c471-110">The changes impact the following versions of Business Central:</span></span>
> - <span data-ttu-id="2c471-111">Microsoft Dynamics 365 Business Central Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="2c471-111">Microsoft Dynamics 365 Business Central October 2018</span></span>
> - <span data-ttu-id="2c471-112">Microsoft Dynamics 365 Business Central April 2019</span><span class="sxs-lookup"><span data-stu-id="2c471-112">Microsoft Dynamics 365 Business Central April 2019</span></span>
> - <span data-ttu-id="2c471-113">Microsoft Dynamics 365 Business Central 2019 Veröffentlichunswelle 2</span><span class="sxs-lookup"><span data-stu-id="2c471-113">Microsoft Dynamics 365 Business Central 2019 Release Wave 2</span></span>

<span data-ttu-id="2c471-114">Debitoren erfordern regelmäßig höheren Debitorenservice, sowohl in Bezug auf Produktqualität wie auch in Bezug auf Lieferungs- und Zahlungsverkehr.</span><span class="sxs-lookup"><span data-stu-id="2c471-114">Customers continuously require higher customer service, both in terms of the quality of product but also in terms of delivery and payment services.</span></span> <span data-ttu-id="2c471-115">Mit dem Microsoft Pay-Service steigern Sie Ihren Kundenservice.</span><span class="sxs-lookup"><span data-stu-id="2c471-115">The Microsoft Pay service helps you increase your customer service.</span></span>

<span data-ttu-id="2c471-116">Die Microsoft Pay-Erweiterung fügt einen Microsoft Pay-Link zu Verkaufsbelegen hinzu, sodass Debitoren einfach mithilfe von Microsoft Pay bezahlen können.</span><span class="sxs-lookup"><span data-stu-id="2c471-116">The Microsoft Pay extension adds a Microsoft Pay link to your sales documents so customers can easily pay using Microsoft Pay.</span></span> <span data-ttu-id="2c471-117">Dann können Sie die Dokumente per E-Mail versenden, um besseren Debitorenservice bereitzustellen und die Zeit zu verkürzen, die benötigt wird, damit die Zahlungsausgleichsposten der Debitoren auf dem Bankkonto ankommen.</span><span class="sxs-lookup"><span data-stu-id="2c471-117">Then you can send the documents by email to provide higher customer service and shorten the time it takes for customers’ payments to arrive on your bank account.</span></span>

<span data-ttu-id="2c471-118">Die Microsoft Pay-Erweiterung bietet die folgenden Vorteile:</span><span class="sxs-lookup"><span data-stu-id="2c471-118">The Microsoft Pay extension provides the following benefits:</span></span>
- <span data-ttu-id="2c471-119">Debitorenzahlungen sind schneller auf Ihrem Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="2c471-119">Customer payments appear faster on your bank account.</span></span>
- <span data-ttu-id="2c471-120">Debitoren haben mehr Arten, Rechnungen zu bezahlen.</span><span class="sxs-lookup"><span data-stu-id="2c471-120">Customers have more ways to pay invoices.</span></span>
- <span data-ttu-id="2c471-121">Microsoft Pay bietet einen vertrauenswürdigen Zahlungsservice an, den Debitoren gegenüber der Eingabe von Kreditkarteninformationen auf unbekannten Websites bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="2c471-121">Microsoft Pay offers a trustworthy payment service, which customers prefer to entering credit card information on unknown web sites.</span></span>
- <span data-ttu-id="2c471-122">Microsoft Pay bietet mehrere Arten zur Zahlungsabwicklung an, einschließlich Kreditkartenverarbeitung, wie Paypal-Konten und andere Quellen.</span><span class="sxs-lookup"><span data-stu-id="2c471-122">Microsoft Pay offers multiple ways of handling payments, including credit card processing, such as PayPal and Stripe.</span></span>
- <span data-ttu-id="2c471-123">Der Microsoft Pay-Link kann jedem Rechnungsbeleg oder vom Benutzer automatisch eingebettet werden.</span><span class="sxs-lookup"><span data-stu-id="2c471-123">The Microsoft Pay link can be embedded automatically on every invoice document or by the user.</span></span>
- <span data-ttu-id="2c471-124">Da diese Funktionalität als Erweiterung aufgebaut ist, gibt sie Ihnen Kontrolle, um sie zu aktivieren und wenn die Geschäftsvorgänge sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="2c471-124">Because this functionality is built as an extension, it gives you full control to enable it when and if your business processes require it.</span></span>

<span data-ttu-id="2c471-125">Das Aktivieren der Zahlungsverkehrerweiterungen ist frei in [!INCLUDE[prod_short](includes/prod_short.md)]jedoch müssen Sie den Zahlungsservice kontaktieren, um ein Konto auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="2c471-125">Enabling payment service extensions is free in [!INCLUDE[prod_short](includes/prod_short.md)], however, you will need to contact the payment service to get an account.</span></span> <span data-ttu-id="2c471-126">Weitere Informationen finden Sie unter [Aktivieren Sie Zahlungen durch Zahlungsverkehr](sales-how-enable-payment-service-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="2c471-126">For more information, see [Enable Customer Payment Through Payment Services](sales-how-enable-payment-service-extensions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="2c471-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c471-127">See Also</span></span>
<span data-ttu-id="2c471-128">[Anpassen [!INCLUDE[prod_short](includes/prod_short.md)] Erweiterungen nutzen](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="2c471-128">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="2c471-129">Einrichten von Verkäufen</span><span class="sxs-lookup"><span data-stu-id="2c471-129">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="2c471-130">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2c471-130">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]