---
title: "Erstellen eines Kreditors, Debitors oder Bankkontos über einen Kontakt | Microsoft Docs"
description: "Sie können einen bestehenden Kontakt als Debitor, Kreditor oder Bankkonto mithilfe der vorhandenen Daten und angeben Geschäftsbeziehung erfassen."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e1f1d9e89d4164f36fb90c027cd636da67bc40d9
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="create-a-customer-vendor-or-bank-account-from-a-contact"></a><span data-ttu-id="8c44d-103">Erstellen eines Kreditors, Debitors oder Bankkontos über einen Kontakt</span><span class="sxs-lookup"><span data-stu-id="8c44d-103">Create a Customer, Vendor, or Bank Account From a Contact</span></span>
<span data-ttu-id="8c44d-104">Sie können vorhandene Kontakte als Debitoren, Kreditoren oder als Bankkonten erfassen.</span><span class="sxs-lookup"><span data-stu-id="8c44d-104">You may want to record some of your existing contacts as customers, vendors, or bank accounts.</span></span> <span data-ttu-id="8c44d-105">Beim Erstellen eines Kreditors, Debitors oder Bankkontos aus einem Kontakt können Sie vorhandene Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="8c44d-105">Creating a customer, vendor, or bank account from a contact enables you use existing data.</span></span> <span data-ttu-id="8c44d-106">Wenn Sie einen Debitor, Kreditor oder ein Bankkonto auf diese Weise erstellen, wird es mit dem Kontakt synchronisiert</span><span class="sxs-lookup"><span data-stu-id="8c44d-106">When you create a customer, vendor, or bank account this way, it is synchronized with the contact.</span></span> <span data-ttu-id="8c44d-107">Die Synchronisierung macht Informationen, die zwischen Kontakten und Debitoren, Kreditoren oder Bankkonto gleich sind, identisch.</span><span class="sxs-lookup"><span data-stu-id="8c44d-107">Synchronization makes information that is common between contacts and customers, vendors, or bank account the same.</span></span>

<span data-ttu-id="8c44d-108">**Hinweis**: Bevor Sie auf diese Weise ein erfassen können, müssen Sie einen Geschäftsbeziehungscode für Debitoren, Kreditoren und Bankkonten im Fenster Marketingeinrichtung angeben.</span><span class="sxs-lookup"><span data-stu-id="8c44d-108">Before you can record contacts this way, you must specify a business relation code for customers, vendors, and bank accounts in the **Marketing Setup** window.</span></span> <span data-ttu-id="8c44d-109">Wenn Sie Kontakte als Bankkonten erfassen, müssen Sie Nummernserie für Bankkonten im **Finanzbuchhaltungseinrichtung**-Fenster angeben.</span><span class="sxs-lookup"><span data-stu-id="8c44d-109">If you will be recording contacts as bank accounts, you must also specify numbers series for bank accounts in the **General Ledger Setup** window.</span></span>

## <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a><span data-ttu-id="8c44d-110">So erstellen Sie einen Kontakt als Debitor, Kreditor oder Bankkonto</span><span class="sxs-lookup"><span data-stu-id="8c44d-110">To create a contact as a customer, vendor, or bank account</span></span>
1. <span data-ttu-id="8c44d-111">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Kontakte** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="8c44d-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Contacts**, and then choose the related link.</span></span>
2. <span data-ttu-id="8c44d-112">Wählen Sie den Kontakt aus, den Sie als Debitor, Kreditor oder Bankkonto erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="8c44d-112">Select the contact you want to create as a customer, vendor, or bank account.</span></span>
3. <span data-ttu-id="8c44d-113">Wählen Sie die Aktionen **Erstellen als**, und wählen Sie denn entweder **Debitor**, **Kreditor** oder **Bank**.</span><span class="sxs-lookup"><span data-stu-id="8c44d-113">Choose the **Create As** action, and then choose either **Customer**, **Vendor**, or **Bank**.</span></span>
4. <span data-ttu-id="8c44d-114">Bestätigen Sie die nachfolgende Meldung.</span><span class="sxs-lookup"><span data-stu-id="8c44d-114">Confirm the subsequent message.</span></span>

<span data-ttu-id="8c44d-115">Die Kontaktinformationen werden von der Karte **Kontakt** auf die Karte **Bankkonto**, die Karte **Debitor** oder die Karte **Kreditor** übertragen.</span><span class="sxs-lookup"><span data-stu-id="8c44d-115">The contact information is transferred from the **Contact** card to the **Bank Account** card, the **Customer** card, or the **Vendor** card.</span></span> <span data-ttu-id="8c44d-116">Sie können den einzelnen Karten spezifische Informationen, wie Fakturierungs- und Zahlungsdetails hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8c44d-116">You may want to add specific information to each of the cards, such as invoicing and payment details.</span></span>

## <a name="see-also"></a><span data-ttu-id="8c44d-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c44d-117">See Also</span></span>
[<span data-ttu-id="8c44d-118">Erstellen von Kontaktunternehmen</span><span class="sxs-lookup"><span data-stu-id="8c44d-118">Create Contact Companies</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="8c44d-119">Anlegen von Kontaktpersonen</span><span class="sxs-lookup"><span data-stu-id="8c44d-119">Create Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="8c44d-120">Marketing & Vertrieb einrichten</span><span class="sxs-lookup"><span data-stu-id="8c44d-120">Setting Up Relationship Management</span></span>](marketing-setup-marketing.md)  
[<span data-ttu-id="8c44d-121">Synchronisieren von Kontakten mit Debitoren, Kreditoren und Bankkonten</span><span class="sxs-lookup"><span data-stu-id="8c44d-121">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[<span data-ttu-id="8c44d-122">Kontakte mit vorhandenen Debitoren, Kreditoren und Bankkonten verknüpfen</span><span class="sxs-lookup"><span data-stu-id="8c44d-122">Link Contacts to Existing Customers, Vendors, or Bank Accounts</span></span>](marketing-how-link-contact.md)  
[<span data-ttu-id="8c44d-123">Kontakten Geschäftsbeziehungen zuordnen</span><span class="sxs-lookup"><span data-stu-id="8c44d-123">Assign Business Relations to a Contact</span></span>](marketing-business-relations.md#AssignBusRelContact)  
[<span data-ttu-id="8c44d-124">Arbeiten mit  Business Central</span><span class="sxs-lookup"><span data-stu-id="8c44d-124">Working with Business Central</span></span>](ui-work-product.md)

