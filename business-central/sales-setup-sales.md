---
title: Überblick der Aufgaben zum konfigurieren von Verkaufsprozessen | Microsoft Docs
description: Gliedert die Aufgaben, um Regeln und Werte einzurichten, um Ihre Vertriebsrichtlinien und Arbeitsgänge zu definieren.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, configure
ms.date: 01/13/2020
ms.author: sgroespe
ms.openlocfilehash: d19d02cb770efb32441d4b1282789a92deea41a0
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/14/2020
ms.locfileid: "2953395"
---
# <a name="setting-up-sales"></a><span data-ttu-id="92e74-103">Einrichten von Verkäufen</span><span class="sxs-lookup"><span data-stu-id="92e74-103">Setting Up Sales</span></span>
<span data-ttu-id="92e74-104">Bevor Sie Verkaufsprozesse verwalten können, müssen die Regeln und Werte konfiguriert werden, die die Vertriebsrichtlinien des Mandanten definieren.</span><span class="sxs-lookup"><span data-stu-id="92e74-104">Before you can manage sales processes, you must configure the rules and values that define the company's sales policies.</span></span>

<span data-ttu-id="92e74-105">Zuerst muss die allgemeine Einrichtung definiert werden, z. B. welche Verkaufsbelege erforderlich sind und wie deren Werte gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="92e74-105">You must define the general setup, such as which sales documents are required and how their values are posted.</span></span> <span data-ttu-id="92e74-106">Diese allgemeine Einrichtung erfolgt in der Regel einmal bei der anfänglichen Implementierung.</span><span class="sxs-lookup"><span data-stu-id="92e74-106">This general setup is typically performed once during the initial implementation.</span></span>

<span data-ttu-id="92e74-107">Eine separate Reihe von Aufgaben, die mit der Erfassung neuer Kreditoren im Zusammenhang stehen, dient dazu, alle Sonderpreis oder Rabattvereinbarungen zu speichern, die Sie mit einzelnen Kreditoren haben.</span><span class="sxs-lookup"><span data-stu-id="92e74-107">A separate series of tasks related to registering new customers is to record any special price or discount agreements that you have with each customer.</span></span>

<span data-ttu-id="92e74-108">Einrichten von finanzbezogenen Verkäufen wie Zahlungsformen und Währungen werden im Finanzsetupabschnitt behandelt.</span><span class="sxs-lookup"><span data-stu-id="92e74-108">Finance-related sales setup, such as payment methods and currencies, are covered in the Finance Setup section.</span></span> <span data-ttu-id="92e74-109">Weitere Informationen finden Sie unter [Einrichten von Finanzen](finance-setup-finance.md).</span><span class="sxs-lookup"><span data-stu-id="92e74-109">For more information, see [Setting Up Finance](finance-setup-finance.md).</span></span>

| <span data-ttu-id="92e74-110">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="92e74-110">To</span></span> | <span data-ttu-id="92e74-111">Siehe</span><span class="sxs-lookup"><span data-stu-id="92e74-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="92e74-112">Erstellen Sie eine Debitorenkarte für jeden Debitor, an den Sie verkaufen.</span><span class="sxs-lookup"><span data-stu-id="92e74-112">Create a customer card for each customer that you sell to.</span></span> |[<span data-ttu-id="92e74-113">Registriert einen neuen Debitor.</span><span class="sxs-lookup"><span data-stu-id="92e74-113">Register New Customers</span></span>](sales-how-register-new-customers.md) |
| <span data-ttu-id="92e74-114">Aktivieren Sie Debitoren, um über Paypal zu bezahlen, indem Sie das Paypal-Logo in Verkaufsbelegen auswählen.</span><span class="sxs-lookup"><span data-stu-id="92e74-114">Enable customers to pay through PayPal by choosing the PayPal logo on sales documents.</span></span> |[<span data-ttu-id="92e74-115">Aktivieren von Debitoren-Zahlungen durch Paypal</span><span class="sxs-lookup"><span data-stu-id="92e74-115">Enable Customer Payment Through PayPal</span></span>](sales-how-enable-payment-service-extensions.md) |
| <span data-ttu-id="92e74-116">Geben Sie die verschiedenen Rabatte und alternativen Preise ein, die Sie den Debitoren abhängig von Artikel, Mengen und/oder Datum gewähren.</span><span class="sxs-lookup"><span data-stu-id="92e74-116">Enter the different discounts and special prices that you grant to customers depending on item, quantities, and/or date.</span></span> |[<span data-ttu-id="92e74-117">Erfassen von Verkaufspreisen, Skonti und Zahlungsvereinbarungen</span><span class="sxs-lookup"><span data-stu-id="92e74-117">Record Sales Price, Discount, and Payment Agreements</span></span>](sales-how-record-sales-price-discount-payment-agreements.md) |
| <span data-ttu-id="92e74-118">Einrichten von Verkäufer, sodass Sie diese den Debitorenkontakten zuweisen können oder die Leistung des Verkaufspersonals messen können und als Basis für die Berechnung von Verkaufsprovisionen oder der Prämie zuweisen können.</span><span class="sxs-lookup"><span data-stu-id="92e74-118">Set up salespeople so that you can assign them to customer contacts or measure salespeople's performance as a basis for calculating the sales commission or bonus.</span></span> |[<span data-ttu-id="92e74-119">Verkäufer einrichten</span><span class="sxs-lookup"><span data-stu-id="92e74-119">Set Up Salespeople</span></span>](sales-how-setup-salespeople.md) |
| <span data-ttu-id="92e74-120">Geben Sie für einzelne Debitoren oder für alle Debitoren an, wie Verkaufsbelege standardmäßig gesendet werden, wenn Sie die Aktion **Buchen und senden** auswählen.</span><span class="sxs-lookup"><span data-stu-id="92e74-120">Specify for individual customers or for all customers how sales documents are sent by default when you choose the **Post and Send** action.</span></span> |[<span data-ttu-id="92e74-121">Belegsendeprofile einrichten</span><span class="sxs-lookup"><span data-stu-id="92e74-121">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md) |
| <span data-ttu-id="92e74-122">Legen Sie die E-Mail a, um eine Zusammenfassung der Informationen des Verkaufsbelegs zu erhalten, der gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="92e74-122">Set your email up to contain a summary of information in the sales document that is being sent.</span></span> |<span data-ttu-id="92e74-123">[Senden von Belegen über E-Mail](ui-how-send-documents-email.md).</span><span class="sxs-lookup"><span data-stu-id="92e74-123">[Send Documents by Email](ui-how-send-documents-email.md).</span></span> |
|<span data-ttu-id="92e74-124">Verwenden Sie einen EU-Webdienst, um die MwSt-IdNr. eines Debitors zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="92e74-124">Use an EU web service to verify a customer's VAT registration number.</span></span>|[<span data-ttu-id="92e74-125">MwSt-IdNr. prüfen</span><span class="sxs-lookup"><span data-stu-id="92e74-125">Verify VAT Registration Numbers</span></span>](finance-setup-vat.md)|
|<span data-ttu-id="92e74-126">Definieren Sie die verschiedenen Incoterms, die Sie Debitoren oder Ihren Kreditoren anbieten.</span><span class="sxs-lookup"><span data-stu-id="92e74-126">Define the different incoterms that you offer to customers or that your vendors offer you.</span></span>|[<span data-ttu-id="92e74-127">Liefermethoden einrichten</span><span class="sxs-lookup"><span data-stu-id="92e74-127">Set Up Shipment Methods</span></span>](sales-how-set-up-shipment-methods.md)|
|<span data-ttu-id="92e74-128">Geben Sie Informationen über die verschiedenen eingesetzten Transportkreditoren ein, einschließlich einer Verknüpfung zu ihrem Paketverfolgungsservice.</span><span class="sxs-lookup"><span data-stu-id="92e74-128">Enter information about the different transportation vendors you use, including a link to their package tracking service.</span></span>|[<span data-ttu-id="92e74-129">Zusteller einrichten</span><span class="sxs-lookup"><span data-stu-id="92e74-129">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)|

## <a name="see-related-training-at-microsoft-learnlearnmodulestrade-get-started-dynamics-365-business-central"></a><span data-ttu-id="92e74-130">Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/trade-get-started-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="92e74-130">See Related Training at [Microsoft Learn](/learn/modules/trade-get-started-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="92e74-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92e74-131">See Also</span></span>
[<span data-ttu-id="92e74-132">Verkauf</span><span class="sxs-lookup"><span data-stu-id="92e74-132">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="92e74-133">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="92e74-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
