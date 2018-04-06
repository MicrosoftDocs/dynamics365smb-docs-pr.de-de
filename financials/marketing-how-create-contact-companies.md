---
title: Erstellen von Kontaktunternehmen| Microsoft Docs
description: "Beschreibt, wie einer Kontaktkarte für jede neue Unternehmung oder potentielle neuen Unternehmung erstellt wird, mit dem Sie eine Geschäftsbeziehung haben."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ed0f75f1e0ee8a282b58458e4fed3b4eef7c46fb
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="create-contact-companies"></a><span data-ttu-id="856a2-103">Erstellen von Kontaktunternehmen</span><span class="sxs-lookup"><span data-stu-id="856a2-103">Create Contact Companies</span></span>
<span data-ttu-id="856a2-104">Sie können für jedes neue Unternehmen, mit dem Sie Geschäfte machen, eine Kontaktkarte anlegen. Das können z. B. Debitoren, Kreditoren, Interessenten, Banken, Rechtsanwälte, Berater usw. sein.</span><span class="sxs-lookup"><span data-stu-id="856a2-104">You can create a contact for each new company you interact with, for example, a customer, vendor, prospective customer, bank, law firm, consultant, and so on.</span></span>

<span data-ttu-id="856a2-105">Es gibt zwei Möglichkeiten, um einen Kontakt zu erstellen: von Grund auf neu oder aus einem bestehenden Debitor, Kreditor oder Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="856a2-105">There are two ways to create a contact: from scratch or from an existing customer, vendor, or bank account.</span></span>

<span data-ttu-id="856a2-106">Bevor Sie einen Kontakt anlegen, sollten Sie die Einstellungen im Fenster **Marketing & Vertrieb Einr.** überprüfen.</span><span class="sxs-lookup"><span data-stu-id="856a2-106">Before creating a contact, you may want to check the settings in the **Marketing Setup** window.</span></span> <span data-ttu-id="856a2-107">Weitere Informationen finden Sie unter [Einrichten von Relationship Management](marketing-setup-marketing.md)</span><span class="sxs-lookup"><span data-stu-id="856a2-107">For more information, see [Setting Up Relationship Management](marketing-setup-marketing.md).</span></span>

## <a name="create-a-company-contact-from-scratch"></a><span data-ttu-id="856a2-108">Neues eines Unternehmenskontakte von Grund auf</span><span class="sxs-lookup"><span data-stu-id="856a2-108">Create a company contact from scratch</span></span>
1. <span data-ttu-id="856a2-109">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Kontakte** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="856a2-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Contacts**, and then choose the related link.</span></span>
2. <span data-ttu-id="856a2-110">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="856a2-110">Choose the **New** action.</span></span>
3. <span data-ttu-id="856a2-111">Geben Sie im Feld **Nr.** eine Nummer für den Kontakt ein.</span><span class="sxs-lookup"><span data-stu-id="856a2-111">In the **No. field**, enter a number for the contact.</span></span>

    <span data-ttu-id="856a2-112">Wenn Sie im Fenster **Marketing & Vertrieb Einr.** eine Nummernserie für Kontakte eingegeben haben, können Sie alternativ auch die EINGABETASTE drücken, um die nächste verfügbare Kontaktnummer auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="856a2-112">Alternatively, if you have set up a number series for contacts in the **Marketing Setup** window, you can press the Enter key to select the next available contact number.</span></span>  
4. <span data-ttu-id="856a2-113">Legen Sie **Art** auf **Unternehmen** fest.</span><span class="sxs-lookup"><span data-stu-id="856a2-113">Set **Type** to **Company**.</span></span>
5. <span data-ttu-id="856a2-114">Füllen Sie die weiteren Felder wie erforderlich aus.</span><span class="sxs-lookup"><span data-stu-id="856a2-114">Fill in the other fields as required.</span></span>

## <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a><span data-ttu-id="856a2-115">Erstellen eines Unternehmenskontakts aus einem Debitor, Kreditor oder Bankkonto</span><span class="sxs-lookup"><span data-stu-id="856a2-115">To create a company contact from a customer, vendor, or bank account</span></span>
<span data-ttu-id="856a2-116">Wenn Sie bereits eine Anzahl von Debitoren, Kreditoren und Bankkonten eingerichtet haben, können Sie Kontakte auf der Basis von bestehenden Daten erstellen.</span><span class="sxs-lookup"><span data-stu-id="856a2-116">If you have already set up a number of customers, vendors, and bank accounts, you can create contacts on the basis of the existing data.</span></span> <span data-ttu-id="856a2-117">Wenn Sie einen Kontakt auf diese Weise erstellen, werden die Kontaktinformationen mit dem Debitoren-, Kreditoren- oder den Bankkontoinformationen synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="856a2-117">When you create a contact this way, the contact information is synchronized with the customer, vendor, or bank account information.</span></span>

> [!NOTE]  
>   <span data-ttu-id="856a2-118">Bevor Sie auf diese Weise ein Kontaktunternehmen erstellen können, müssen Sie einen Geschäftsbeziehungscode für Debitoren, Kreditoren und Bankkonten im Fenster **Marketingeinrichtung** angeben.</span><span class="sxs-lookup"><span data-stu-id="856a2-118">Before you can create contact companies this way, you must specify a business relation code for customers, vendors, and bank accounts in the **Marketing Setup** window.</span></span> <span data-ttu-id="856a2-119">Wenn Sie Kontakte aus Bankkonten erstellen, müssen Sie Nummernserie für Bankkonten im **Finanzbuchhaltungseinrichtung**-Fenster angeben.</span><span class="sxs-lookup"><span data-stu-id="856a2-119">If you will be creating contacts from a bank accounts, you must also specify numbers series for bank accounts in the **General Ledger Setup** window.</span></span>

1. <span data-ttu-id="856a2-120">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben Sie einen der folgenden Begriffe ein (abhängig davon, was wo sie die Kontakte erstellen möchten), und klicken Sie auf den zugehörigen Link.</span><span class="sxs-lookup"><span data-stu-id="856a2-120">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter one of the following, depending on from where you want to create contacts, and then choose the related link.</span></span>
   * <span data-ttu-id="856a2-121">**Kontakte aus Debitoren erstellen**</span><span class="sxs-lookup"><span data-stu-id="856a2-121">**Create Contacts from Customers**</span></span>
   * <span data-ttu-id="856a2-122">**Kontakte aus Kreditoren erstellen**</span><span class="sxs-lookup"><span data-stu-id="856a2-122">**Create Contacts from Vendors**</span></span>
   * <span data-ttu-id="856a2-123">**Kontakte aus Bankkonten erstellen**</span><span class="sxs-lookup"><span data-stu-id="856a2-123">**Create Contacts from Bank Accounts**</span></span>
2. <span data-ttu-id="856a2-124">Legen Sie im Abschnitt **Debitor**, **Kreditor** oder **Bankkonto** des Stapelverarbeitungsfenstert Filter fest, wenn Sie Kontakte aus bestimmten Debitoren, Kreditoren oder Bankkonten erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="856a2-124">In the batch job window that opens, in the **Customer**, **Vendor**, or **Bank Account** section, set filters if you want to create contacts from specific customers, vendors, or bank accounts.</span></span>
3. <span data-ttu-id="856a2-125">Klicken Sie auf die Schaltfläche **OK**, um mit dem Erstellen von Kontakten zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="856a2-125">Choose the **OK** button to start creating contacts.</span></span>

    <span data-ttu-id="856a2-126">Den neuen Kontakten werden die nächsten Kontaktnummern aus der Nummernserie zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="856a2-126">The next contact numbers in the number series are assigned to the new contacts.</span></span> <span data-ttu-id="856a2-127">Den neu erstellten Kontakten wird automatisch die Geschäftsbeziehung für Kreditoren zugewiesen, die im Fenster **Marketing & Vertrieb Einr.** festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="856a2-127">The business relation for vendors that is specified in the **Marketing Setup** window is assigned to the newly created contacts.</span></span>

> [!TIP]  
>   <span data-ttu-id="856a2-128">Sie können auch einen Debitor, Kreditor oder Bankkonto über einen Kontakt erstellen.</span><span class="sxs-lookup"><span data-stu-id="856a2-128">You can also create a customer, vendor, or bank account from a contact.</span></span> <span data-ttu-id="856a2-129">Weitere Informationen finden Sie unter [Debitor, Kreditor oder Bankkonto über einen Kontakt erstellen](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="856a2-129">For more information, see [Create a Customer, Vendor, or Bank Account From a Contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="856a2-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="856a2-130">See Also</span></span>
[<span data-ttu-id="856a2-131">Synchronisieren von Kontakten mit Debitoren, Kreditoren und Bankkonten</span><span class="sxs-lookup"><span data-stu-id="856a2-131">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[<span data-ttu-id="856a2-132">Kontakten Geschäftsbeziehungen zuordnen</span><span class="sxs-lookup"><span data-stu-id="856a2-132">Assign Business Relations to a Contact</span></span>](marketing-business-relations.md#AssignBusRelContact)  
[<span data-ttu-id="856a2-133">Kontakt eine Branche zuordnen</span><span class="sxs-lookup"><span data-stu-id="856a2-133">Assign Industry Groups to a Contact</span></span>](marketing-industry-groups.md#AssignIndustryGroupContact)  
[<span data-ttu-id="856a2-134">Zuordnen von Verteiler zu einem Kontakt</span><span class="sxs-lookup"><span data-stu-id="856a2-134">Assign Mailing Groups to a Contact</span></span>](marketing-mailing-groups.md#AssignMailGroupContact)  
[<span data-ttu-id="856a2-135">Anlegen von Kontaktpersonen</span><span class="sxs-lookup"><span data-stu-id="856a2-135">Create Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="856a2-136">Arbeiten mit Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="856a2-136">Working with Finance and Operations, Business edition</span></span>](ui-work-product.md)

