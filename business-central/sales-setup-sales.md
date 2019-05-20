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
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6903744c1be0492267c8dee307e4b012aed4ffa4
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251032"
---
# <a name="setting-up-sales"></a><span data-ttu-id="e3a28-103">Einrichten von Verkäufen</span><span class="sxs-lookup"><span data-stu-id="e3a28-103">Setting Up Sales</span></span>
<span data-ttu-id="e3a28-104">Bevor Sie Verkaufsprozesse verwalten können, müssen die Regeln und Werte konfiguriert werden, die die Vertriebsrichtlinien des Mandanten definieren.</span><span class="sxs-lookup"><span data-stu-id="e3a28-104">Before you can manage sales processes, you must configure the rules and values that define the company's sales policies.</span></span>

<span data-ttu-id="e3a28-105">Zuerst muss die allgemeine Einrichtung definiert werden, z. B. welche Verkaufsbelege erforderlich sind und wie deren Werte gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="e3a28-105">You must define the general setup, such as which sales documents are required and how their values are posted.</span></span> <span data-ttu-id="e3a28-106">Diese allgemeine Einrichtung erfolgt in der Regel einmal bei der anfänglichen Implementierung.</span><span class="sxs-lookup"><span data-stu-id="e3a28-106">This general setup is typically performed once during the initial implementation.</span></span>

<span data-ttu-id="e3a28-107">Eine separate Reihe von Aufgaben, die mit der Erfassung neuer Kreditoren im Zusammenhang stehen, dient dazu, alle Sonderpreis oder Rabattvereinbarungen zu speichern, die Sie mit einzelnen Kreditoren haben.</span><span class="sxs-lookup"><span data-stu-id="e3a28-107">A separate series of tasks related to registering new customers is to record any special price or discount agreements that you have with each customer.</span></span>

<span data-ttu-id="e3a28-108">Einrichten von finanzbezogenen Verkäufen wie Zahlungsformen und Währungen werden im Finanzsetupabschnitt behandelt.</span><span class="sxs-lookup"><span data-stu-id="e3a28-108">Finance-related sales setup, such as payment methods and currencies, are covered in the Finance Setup section.</span></span> <span data-ttu-id="e3a28-109">Weitere Informationen finden Sie unter [Einrichten von Finanzen](finance-setup-finance.md).</span><span class="sxs-lookup"><span data-stu-id="e3a28-109">For more information, see [Setting Up Finance](finance-setup-finance.md).</span></span>

| <span data-ttu-id="e3a28-110">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="e3a28-110">To</span></span> | <span data-ttu-id="e3a28-111">Siehe</span><span class="sxs-lookup"><span data-stu-id="e3a28-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="e3a28-112">Erstellen Sie eine Debitorenkarte für jeden Debitor, an den Sie verkaufen.</span><span class="sxs-lookup"><span data-stu-id="e3a28-112">Create a customer card for each customer that you sell to.</span></span> |[<span data-ttu-id="e3a28-113">Registriert einen neuen Debitor.</span><span class="sxs-lookup"><span data-stu-id="e3a28-113">Register New Customers</span></span>](sales-how-register-new-customers.md) |
| <span data-ttu-id="e3a28-114">Aktivieren Sie Debitoren, um über Paypal zu bezahlen, indem Sie das Paypal-Logo in Verkaufsbelegen auswählen.</span><span class="sxs-lookup"><span data-stu-id="e3a28-114">Enable customers to pay through PayPal by choosing the PayPal logo on sales documents.</span></span> |[<span data-ttu-id="e3a28-115">Aktivieren von Debitoren-Zahlungen durch Paypal</span><span class="sxs-lookup"><span data-stu-id="e3a28-115">Enable Customer Payment Through PayPal</span></span>](sales-how-enable-payment-service-extensions.md) |
| <span data-ttu-id="e3a28-116">Geben Sie die verschiedenen Rabatte und alternativen Preise ein, die Sie den Debitoren abhängig von Artikel, Mengen und/oder Datum gewähren.</span><span class="sxs-lookup"><span data-stu-id="e3a28-116">Enter the different discounts and special prices that you grant to customers depending on item, quantities, and/or date.</span></span> |[<span data-ttu-id="e3a28-117">Erfassen von Verkaufspreisen, Skonti und Zahlungsvereinbarungen</span><span class="sxs-lookup"><span data-stu-id="e3a28-117">Record Sales Price, Discount, and Payment Agreements</span></span>](sales-how-record-sales-price-discount-payment-agreements.md) |
| <span data-ttu-id="e3a28-118">Einrichten von Verkäufer, sodass Sie diese den Debitorenkontakten zuweisen können oder die Leistung des Verkaufspersonals messen können und als Basis für die Berechnung von Verkaufsprovisionen oder der Prämie zuweisen können.</span><span class="sxs-lookup"><span data-stu-id="e3a28-118">Set up salespeople so that you can assign them to customer contacts or measure salespeople's performance as a basis for calculating the sales commission or bonus.</span></span> |[<span data-ttu-id="e3a28-119">Verkäufer einrichten</span><span class="sxs-lookup"><span data-stu-id="e3a28-119">Set Up Salespeople</span></span>](sales-how-setup-salespeople.md) |
| <span data-ttu-id="e3a28-120">Geben Sie für einzelne Debitoren oder für alle Debitoren an, wie Verkaufsbelege standardmäßig gesendet werden, wenn Sie die Aktion **Buchen und senden** auswählen.</span><span class="sxs-lookup"><span data-stu-id="e3a28-120">Specify for individual customers or for all customers how sales documents are sent by default when you choose the **Post and Send** action.</span></span> |[<span data-ttu-id="e3a28-121">Belegsendeprofile einrichten</span><span class="sxs-lookup"><span data-stu-id="e3a28-121">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md) |
| <span data-ttu-id="e3a28-122">Legen Sie die E-Mail a, um eine Zusammenfassung der Informationen des Verkaufsbelegs zu erhalten, der gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="e3a28-122">Set your email up to contain a summary of information in the sales document that is being sent.</span></span> |<span data-ttu-id="e3a28-123">[Senden von Belegen über E-Mail](ui-how-send-documents-email.md).</span><span class="sxs-lookup"><span data-stu-id="e3a28-123">[Send Documents by Email](ui-how-send-documents-email.md).</span></span> |
|<span data-ttu-id="e3a28-124">Verwenden Sie einen EU-Webdienst, um die MwSt-IdNr. eines Debitors zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e3a28-124">Use an EU web service to verify a customer's VAT registration number.</span></span>|[<span data-ttu-id="e3a28-125">MwSt-IdNr. prüfen</span><span class="sxs-lookup"><span data-stu-id="e3a28-125">Verify VAT Registration Numbers</span></span>](finance-setup-vat.md)|
|<span data-ttu-id="e3a28-126">Geben Sie Informationen über die verschiedenen eingesetzten Transportkreditoren ein, einschließlich einer Verknüpfung zu ihrem Paketverfolgungsservice.</span><span class="sxs-lookup"><span data-stu-id="e3a28-126">Enter information about the different transportation vendors you use, including a link to their package tracking service.</span></span>|[<span data-ttu-id="e3a28-127">Zusteller einrichten</span><span class="sxs-lookup"><span data-stu-id="e3a28-127">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)|

## <a name="see-also"></a><span data-ttu-id="e3a28-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3a28-128">See Also</span></span>
[<span data-ttu-id="e3a28-129">Verkauf</span><span class="sxs-lookup"><span data-stu-id="e3a28-129">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="e3a28-130">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e3a28-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
