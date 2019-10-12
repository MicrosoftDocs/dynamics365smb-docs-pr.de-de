---
title: Kontakte mit Debitoren, Kreditoren und Bankkonten synchronisieren| Microsoft Docs
description: Sie koppeln synchronisieren Kontaktinformationen der Kontakte, die auch Debitoren, Kreditoren oder Bankkonten sind, so aktualisieren Sie nur Informationen in einem Bereich.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, CRM, integration, couple
ms.date: 10/01/2019
ms.author: edupont
redirect_url: marketing-create-contact-companies
ms.openlocfilehash: f102b6dac47732d96aff8413697c172fbea3f687
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308644"
---
# <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a><span data-ttu-id="6899b-103">Synchronisieren von Kontakten mit Debitoren, Kreditoren und Bankkonten</span><span class="sxs-lookup"><span data-stu-id="6899b-103">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>
<span data-ttu-id="6899b-104">Wenn einige Ihrer Kontakte auch Debitoren, Kreditoren oder Bankkonten sind, können Sie deren Kontaktinformationen mit dem entsprechenden Debitor, Kreditor oder Bankkonto synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="6899b-104">If some of your contacts are also customers, vendors, or bank accounts, you can synchronize the contact information with the related customer, vendor, or bank account.</span></span> <span data-ttu-id="6899b-105">Die Synchronisierung macht Informationen, die zwischen Kontakten und Debitoren, Kreditoren oder Bankkonto gleich sind, identisch.</span><span class="sxs-lookup"><span data-stu-id="6899b-105">Synchronization makes information that is common between contacts and customers, vendors, or bank account the same.</span></span>  

## <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a><span data-ttu-id="6899b-106">Unterschiedliche Wege, um Kontakte mit Debitoren, Kreditoren und Bankkonten zu synchronisieren</span><span class="sxs-lookup"><span data-stu-id="6899b-106">Different Ways to Synchronize Contacts with Customers, Vendors and Bank Accounts</span></span>
<span data-ttu-id="6899b-107">Sie können Ihre Kontakte mit Debitoren, Kreditoren oder Bankkonten synchronisieren, indem Sie eine der folgenden drei Methoden verwenden:</span><span class="sxs-lookup"><span data-stu-id="6899b-107">You can synchronize your contacts with customers, vendors, or bank accounts by three methods:</span></span>

* <span data-ttu-id="6899b-108">Verknüpfen Sie Kontakte auf der Kontaktkarte mit bestehenden Debitoren, Kreditoren oder Bankkonten.</span><span class="sxs-lookup"><span data-stu-id="6899b-108">Link contacts with existing customers, vendors, or bank accounts from the contact card.</span></span> <span data-ttu-id="6899b-109">Weitere Informationen finden Sie unter [Kontakte mit Debitoren, Kreditoren und Bankkonten synchronisieren](marketing-how-link-contact.md).</span><span class="sxs-lookup"><span data-stu-id="6899b-109">For more information, see [Link Contacts With Customers, Vendors, and Bank Accounts](marketing-how-link-contact.md).</span></span>
* <span data-ttu-id="6899b-110">Erstellen Sie Debitoren, Kreditoren oder Bankkonten über den Kontakt.</span><span class="sxs-lookup"><span data-stu-id="6899b-110">Create customers, vendors, or bank accounts from the contact.</span></span> <span data-ttu-id="6899b-111">Weitere Informationen finden Sie unter [Debitor, Kreditor oder Bankkonto über einen Kontakt erstellen](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="6899b-111">For more information, see [Create a Customer, Vendor, or Bank Account From a Contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span></span>
* <span data-ttu-id="6899b-112">Erstellen Sie Kontakte aus Debitoren, Kreditoren oder Bankkonten.</span><span class="sxs-lookup"><span data-stu-id="6899b-112">Create contacts from customers, vendors or bank accounts.</span></span> <span data-ttu-id="6899b-113">Weitere Informationen finden Sie unter [Erstellen eines Unternehmenskontakts aus einem Debitor, Kreditor oder Bankkonto](marketing-how-create-contact-companies.md).</span><span class="sxs-lookup"><span data-stu-id="6899b-113">For more information, see [Create a company contact from a customer, vendor, or bank account](marketing-how-create-contact-companies.md).</span></span>

## <a name="consequences-of-synchronization"></a><span data-ttu-id="6899b-114">Ergebnisse der Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="6899b-114">Consequences of Synchronization</span></span>
<span data-ttu-id="6899b-115">Wenn der Kontakt mit dem Debitor, Kreditor oder Bankkonto synchronisiert ist:</span><span class="sxs-lookup"><span data-stu-id="6899b-115">When the contact is synchronized with the customer, vendor, bank account:</span></span>

* <span data-ttu-id="6899b-116">Sie müssen die Informationen nur an einer Stelle aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6899b-116">You only have to update information in one place.</span></span> <span data-ttu-id="6899b-117">Wenn Sie z. B. die Telefonnummer auf des Kontakts ändern, wird die Telefonnummer auf des Debitors-, Kreditors oder Bankkontos automatisch mit der gleichen Änderung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6899b-117">For example, if you modify the phone number on the contact, the phone number is automatically updated with the same modification on the customer, the vendor, or the bank account.</span></span>
* <span data-ttu-id="6899b-118">Wenn Sie beim Erstellen einer Debitoren-, Kreditoren- oder Bankkontokarte eine Nummernserie für Kontakte angegeben haben, wird automatisch eine Kontaktkarte für den Debitor, den Kreditor bzw. das Bankkonto erstellt.</span><span class="sxs-lookup"><span data-stu-id="6899b-118">If you have specified a number series for contacts, when you create a customer card, a vendor card, or a bank account card, a contact card is automatically created for the customer, vendor or bank account.</span></span>
* <span data-ttu-id="6899b-119">Über den Kontakt können Sie Verkaufsangebote und -Aufträge, Einkaufsanfragen und –Aufträge erstellen.</span><span class="sxs-lookup"><span data-stu-id="6899b-119">You can create sales quotes and orders, and purchase quotes and orders from the contact.</span></span>
* <span data-ttu-id="6899b-120">Sie können Ihre Aktivitäten beim Durchführen von Aktionen erfassen lassen, z. B. das Drucken von Aufträgen oder Rahmenbestellungen, Erstellen von Verkaufsserviceaufträgen, Senden von E-Mails usw.</span><span class="sxs-lookup"><span data-stu-id="6899b-120">You can have your interactions recorded when you perform actions such as printing orders, blanket orders, creating sales service orders, sending e-mails, and so on.</span></span>
* <span data-ttu-id="6899b-121">Wenn Sie einen Kontakt löschen, der mit einem Debitor, Kreditor oder Bankkonto verknüpft ist, wird nur der Kontakt entfernt.</span><span class="sxs-lookup"><span data-stu-id="6899b-121">If you delete a contact linked to a customer, vendor or bank account, only the contact is removed.</span></span> <span data-ttu-id="6899b-122">Der Debitor, Kreditor oder das Bankkonto bleibt erhalten.</span><span class="sxs-lookup"><span data-stu-id="6899b-122">The customer, vendor, or bank account remains.</span></span>
* <span data-ttu-id="6899b-123">Wenn Sie einen Debitor, einen Kreditor oder ein Bankkonto löschen, der bzw. das mit einem Kontakt verknüpft ist, bleibt der Kontakt erhalten.</span><span class="sxs-lookup"><span data-stu-id="6899b-123">If you delete a customer, vendor, bank account linked to a contact, the contact remains.</span></span>

> [!NOTE]  
>   <span data-ttu-id="6899b-124">Einige Informationen, wie Fakturierungs- und Buchungsdetails, erscheinen nicht auf der Kontaktkarte.</span><span class="sxs-lookup"><span data-stu-id="6899b-124">Some details, such as invoicing and posting details, do not appear on the contact card.</span></span> <span data-ttu-id="6899b-125">Sie können sie manuell auf der Debitoren-, Kreditoren- und/oder Bankkontenkarte hinzufügen, wenn Sie Kontakte als Debitoren, Kreditoren oder Bankkonten erstellen.</span><span class="sxs-lookup"><span data-stu-id="6899b-125">Therefore, you may want to add them manually on the customer card, vendor card, or bank account card when you create contacts as customers, vendors or bank accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="6899b-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6899b-126">See Also</span></span>
[<span data-ttu-id="6899b-127">Kontakte verwalten</span><span class="sxs-lookup"><span data-stu-id="6899b-127">Managing Contacts</span></span>](marketing-contacts.md)  
<span data-ttu-id="6899b-128">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6899b-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
