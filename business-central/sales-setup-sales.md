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
ms.date: 06/17/2019
ms.author: sgroespe
ms.openlocfilehash: 3ece1edb7ba18cb96099cba34065c96164390e82
ms.sourcegitcommit: 6dc83b27ac47f3b39a7b84cfb7446e7f48b8ce63
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2019
ms.locfileid: "1632706"
---
# <a name="setting-up-sales"></a><span data-ttu-id="a0dff-103">Einrichten von Verkäufen</span><span class="sxs-lookup"><span data-stu-id="a0dff-103">Setting Up Sales</span></span>
<span data-ttu-id="a0dff-104">Bevor Sie Verkaufsprozesse verwalten können, müssen die Regeln und Werte konfiguriert werden, die die Vertriebsrichtlinien des Mandanten definieren.</span><span class="sxs-lookup"><span data-stu-id="a0dff-104">Before you can manage sales processes, you must configure the rules and values that define the company's sales policies.</span></span>

<span data-ttu-id="a0dff-105">Zuerst muss die allgemeine Einrichtung definiert werden, z. B. welche Verkaufsbelege erforderlich sind und wie deren Werte gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="a0dff-105">You must define the general setup, such as which sales documents are required and how their values are posted.</span></span> <span data-ttu-id="a0dff-106">Diese allgemeine Einrichtung erfolgt in der Regel einmal bei der anfänglichen Implementierung.</span><span class="sxs-lookup"><span data-stu-id="a0dff-106">This general setup is typically performed once during the initial implementation.</span></span>

<span data-ttu-id="a0dff-107">Eine separate Reihe von Aufgaben, die mit der Erfassung neuer Kreditoren im Zusammenhang stehen, dient dazu, alle Sonderpreis oder Rabattvereinbarungen zu speichern, die Sie mit einzelnen Kreditoren haben.</span><span class="sxs-lookup"><span data-stu-id="a0dff-107">A separate series of tasks related to registering new customers is to record any special price or discount agreements that you have with each customer.</span></span>

<span data-ttu-id="a0dff-108">Einrichten von finanzbezogenen Verkäufen wie Zahlungsformen und Währungen werden im Finanzsetupabschnitt behandelt.</span><span class="sxs-lookup"><span data-stu-id="a0dff-108">Finance-related sales setup, such as payment methods and currencies, are covered in the Finance Setup section.</span></span> <span data-ttu-id="a0dff-109">Weitere Informationen finden Sie unter [Einrichten von Finanzen](finance-setup-finance.md).</span><span class="sxs-lookup"><span data-stu-id="a0dff-109">For more information, see [Setting Up Finance](finance-setup-finance.md).</span></span>

| <span data-ttu-id="a0dff-110">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="a0dff-110">To</span></span> | <span data-ttu-id="a0dff-111">Siehe</span><span class="sxs-lookup"><span data-stu-id="a0dff-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="a0dff-112">Erstellen Sie eine Debitorenkarte für jeden Debitor, an den Sie verkaufen.</span><span class="sxs-lookup"><span data-stu-id="a0dff-112">Create a customer card for each customer that you sell to.</span></span> |[<span data-ttu-id="a0dff-113">Registriert einen neuen Debitor.</span><span class="sxs-lookup"><span data-stu-id="a0dff-113">Register New Customers</span></span>](sales-how-register-new-customers.md) |
| <span data-ttu-id="a0dff-114">Aktivieren Sie Debitoren, um über Paypal zu bezahlen, indem Sie das Paypal-Logo in Verkaufsbelegen auswählen.</span><span class="sxs-lookup"><span data-stu-id="a0dff-114">Enable customers to pay through PayPal by choosing the PayPal logo on sales documents.</span></span> |[<span data-ttu-id="a0dff-115">Aktivieren von Debitoren-Zahlungen durch Paypal</span><span class="sxs-lookup"><span data-stu-id="a0dff-115">Enable Customer Payment Through PayPal</span></span>](sales-how-enable-payment-service-extensions.md) |
| <span data-ttu-id="a0dff-116">Geben Sie die verschiedenen Rabatte und alternativen Preise ein, die Sie den Debitoren abhängig von Artikel, Mengen und/oder Datum gewähren.</span><span class="sxs-lookup"><span data-stu-id="a0dff-116">Enter the different discounts and special prices that you grant to customers depending on item, quantities, and/or date.</span></span> |[<span data-ttu-id="a0dff-117">Erfassen von Verkaufspreisen, Skonti und Zahlungsvereinbarungen</span><span class="sxs-lookup"><span data-stu-id="a0dff-117">Record Sales Price, Discount, and Payment Agreements</span></span>](sales-how-record-sales-price-discount-payment-agreements.md) |
| <span data-ttu-id="a0dff-118">Einrichten von Verkäufer, sodass Sie diese den Debitorenkontakten zuweisen können oder die Leistung des Verkaufspersonals messen können und als Basis für die Berechnung von Verkaufsprovisionen oder der Prämie zuweisen können.</span><span class="sxs-lookup"><span data-stu-id="a0dff-118">Set up salespeople so that you can assign them to customer contacts or measure salespeople's performance as a basis for calculating the sales commission or bonus.</span></span> |[<span data-ttu-id="a0dff-119">Verkäufer einrichten</span><span class="sxs-lookup"><span data-stu-id="a0dff-119">Set Up Salespeople</span></span>](sales-how-setup-salespeople.md) |
| <span data-ttu-id="a0dff-120">Geben Sie für einzelne Debitoren oder für alle Debitoren an, wie Verkaufsbelege standardmäßig gesendet werden, wenn Sie die Aktion **Buchen und senden** auswählen.</span><span class="sxs-lookup"><span data-stu-id="a0dff-120">Specify for individual customers or for all customers how sales documents are sent by default when you choose the **Post and Send** action.</span></span> |[<span data-ttu-id="a0dff-121">Belegsendeprofile einrichten</span><span class="sxs-lookup"><span data-stu-id="a0dff-121">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md) |
| <span data-ttu-id="a0dff-122">Legen Sie die E-Mail a, um eine Zusammenfassung der Informationen des Verkaufsbelegs zu erhalten, der gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="a0dff-122">Set your email up to contain a summary of information in the sales document that is being sent.</span></span> |<span data-ttu-id="a0dff-123">[Senden von Belegen über E-Mail](ui-how-send-documents-email.md).</span><span class="sxs-lookup"><span data-stu-id="a0dff-123">[Send Documents by Email](ui-how-send-documents-email.md).</span></span> |
|<span data-ttu-id="a0dff-124">Verwenden Sie einen EU-Webdienst, um die MwSt-IdNr. eines Debitors zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a0dff-124">Use an EU web service to verify a customer's VAT registration number.</span></span>|[<span data-ttu-id="a0dff-125">MwSt-IdNr. prüfen</span><span class="sxs-lookup"><span data-stu-id="a0dff-125">Verify VAT Registration Numbers</span></span>](finance-setup-vat.md)|
|<span data-ttu-id="a0dff-126">Definieren Sie die verschiedenen Incoterms, die Sie Debitoren oder Ihren Kreditoren anbieten.</span><span class="sxs-lookup"><span data-stu-id="a0dff-126">Define the different incoterms that you offer to customers or that your vendors offer you.</span></span>|[<span data-ttu-id="a0dff-127">Liefermethoden einrichten</span><span class="sxs-lookup"><span data-stu-id="a0dff-127">Set Up Shipment Methods</span></span>](sales-how-set-up-shipment-methods.md)|
|<span data-ttu-id="a0dff-128">Geben Sie Informationen über die verschiedenen eingesetzten Transportkreditoren ein, einschließlich einer Verknüpfung zu ihrem Paketverfolgungsservice.</span><span class="sxs-lookup"><span data-stu-id="a0dff-128">Enter information about the different transportation vendors you use, including a link to their package tracking service.</span></span>|[<span data-ttu-id="a0dff-129">Zusteller einrichten</span><span class="sxs-lookup"><span data-stu-id="a0dff-129">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)|

## <a name="see-also"></a><span data-ttu-id="a0dff-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0dff-130">See Also</span></span>
[<span data-ttu-id="a0dff-131">Verkauf</span><span class="sxs-lookup"><span data-stu-id="a0dff-131">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="a0dff-132">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a0dff-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
