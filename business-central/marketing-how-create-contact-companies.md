---
title: Erstellen von Kontaktunternehmen| Microsoft Docs
description: "Beschreibt, wie einer Kontaktkarte für jede neue Unternehmung oder potentielle neuen Unternehmung erstellt wird, mit dem Sie eine Geschäftsbeziehung haben."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 64bef8820ec10bb293ccda88e7384d5d9e868e1f
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="create-contact-companies"></a><span data-ttu-id="902ae-103">Erstellen von Kontaktunternehmen</span><span class="sxs-lookup"><span data-stu-id="902ae-103">Create Contact Companies</span></span>
<span data-ttu-id="902ae-104">Sie können für jedes neue Unternehmen, mit dem Sie Geschäfte machen, eine Kontaktkarte anlegen. Das können z. B. Debitoren, Kreditoren, Interessenten, Banken, Rechtsanwälte, Berater usw. sein.</span><span class="sxs-lookup"><span data-stu-id="902ae-104">You can create a contact for each new company you interact with, for example, a customer, vendor, prospective customer, bank, law firm, consultant, and so on.</span></span>

<span data-ttu-id="902ae-105">Es gibt zwei Möglichkeiten, um einen Kontakt zu erstellen: von Grund auf neu oder aus einem bestehenden Debitor, Kreditor oder Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="902ae-105">There are two ways to create a contact: from scratch or from an existing customer, vendor, or bank account.</span></span>

<span data-ttu-id="902ae-106">Bevor Sie einen Kontakt anlegen, sollten Sie die Einstellungen im Fenster **Marketing & Vertrieb Einr.** überprüfen.</span><span class="sxs-lookup"><span data-stu-id="902ae-106">Before creating a contact, you may want to check the settings in the **Marketing Setup** window.</span></span> <span data-ttu-id="902ae-107">Weitere Informationen finden Sie unter [Einrichten von Relationship Management](marketing-setup-marketing.md)</span><span class="sxs-lookup"><span data-stu-id="902ae-107">For more information, see [Setting Up Relationship Management](marketing-setup-marketing.md).</span></span>

## <a name="create-a-company-contact-from-scratch"></a><span data-ttu-id="902ae-108">Neues eines Unternehmenskontakte von Grund auf</span><span class="sxs-lookup"><span data-stu-id="902ae-108">Create a company contact from scratch</span></span>
1. <span data-ttu-id="902ae-109">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontakte** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="902ae-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Contacts**, and then choose the related link.</span></span>
2. <span data-ttu-id="902ae-110">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="902ae-110">Choose the **New** action.</span></span>
3. <span data-ttu-id="902ae-111">Geben Sie im Feld **Nr.** eine Nummer für den Kontakt ein.</span><span class="sxs-lookup"><span data-stu-id="902ae-111">In the **No. field**, enter a number for the contact.</span></span>

    <span data-ttu-id="902ae-112">Wenn Sie im Fenster **Marketing & Vertrieb Einr.** eine Nummernserie für Kontakte eingegeben haben, können Sie alternativ auch die EINGABETASTE drücken, um die nächste verfügbare Kontaktnummer auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="902ae-112">Alternatively, if you have set up a number series for contacts in the **Marketing Setup** window, you can press the Enter key to select the next available contact number.</span></span>  
4. <span data-ttu-id="902ae-113">Legen Sie **Art** auf **Unternehmen** fest.</span><span class="sxs-lookup"><span data-stu-id="902ae-113">Set **Type** to **Company**.</span></span>
5. <span data-ttu-id="902ae-114">Füllen Sie die weiteren Felder wie erforderlich aus.</span><span class="sxs-lookup"><span data-stu-id="902ae-114">Fill in the other fields as required.</span></span>

## <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a><span data-ttu-id="902ae-115">Erstellen eines Unternehmenskontakts aus einem Debitor, Kreditor oder Bankkonto</span><span class="sxs-lookup"><span data-stu-id="902ae-115">To create a company contact from a customer, vendor, or bank account</span></span>
<span data-ttu-id="902ae-116">Wenn Sie bereits eine Anzahl von Debitoren, Kreditoren und Bankkonten eingerichtet haben, können Sie Kontakte auf der Basis von bestehenden Daten erstellen.</span><span class="sxs-lookup"><span data-stu-id="902ae-116">If you have already set up a number of customers, vendors, and bank accounts, you can create contacts on the basis of the existing data.</span></span> <span data-ttu-id="902ae-117">Wenn Sie einen Kontakt auf diese Weise erstellen, werden die Kontaktinformationen mit dem Debitoren-, Kreditoren- oder den Bankkontoinformationen synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="902ae-117">When you create a contact this way, the contact information is synchronized with the customer, vendor, or bank account information.</span></span>

> [!NOTE]  
>   <span data-ttu-id="902ae-118">Bevor Sie auf diese Weise ein Kontaktunternehmen erstellen können, müssen Sie einen Geschäftsbeziehungscode für Debitoren, Kreditoren und Bankkonten im Fenster **Marketingeinrichtung** angeben.</span><span class="sxs-lookup"><span data-stu-id="902ae-118">Before you can create contact companies this way, you must specify a business relation code for customers, vendors, and bank accounts in the **Marketing Setup** window.</span></span> <span data-ttu-id="902ae-119">Wenn Sie Kontakte aus Bankkonten erstellen, müssen Sie Nummernserie für Bankkonten im **Finanzbuchhaltungseinrichtung**-Fenster angeben.</span><span class="sxs-lookup"><span data-stu-id="902ae-119">If you will be creating contacts from a bank accounts, you must also specify numbers series for bank accounts in the **General Ledger Setup** window.</span></span>

1. <span data-ttu-id="902ae-120">Wählen Sie ![Glühlampe, die die Funktion "Teilen Sie mir mit, was Sie tun wollen"](media/ui-search/search_small.png "\"Teilen Sie mir mit, was Sie tun wollen\"") und Folgendes ein, je nachdem, von wo aus Sie Kontakte erstellen möchten, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="902ae-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter one of the following, depending on from where you want to create contacts, and then choose the related link.</span></span>
   * <span data-ttu-id="902ae-121">**Kontakte aus Debitoren erstellen**</span><span class="sxs-lookup"><span data-stu-id="902ae-121">**Create Contacts from Customers**</span></span>
   * <span data-ttu-id="902ae-122">**Kontakte aus Kreditoren erstellen**</span><span class="sxs-lookup"><span data-stu-id="902ae-122">**Create Contacts from Vendors**</span></span>
   * <span data-ttu-id="902ae-123">**Kontakte aus Bankkonten erstellen**</span><span class="sxs-lookup"><span data-stu-id="902ae-123">**Create Contacts from Bank Accounts**</span></span>
2. <span data-ttu-id="902ae-124">Legen Sie im Abschnitt **Debitor**, **Kreditor** oder **Bankkonto** des Stapelverarbeitungsfenstert Filter fest, wenn Sie Kontakte aus bestimmten Debitoren, Kreditoren oder Bankkonten erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="902ae-124">In the batch job window that opens, in the **Customer**, **Vendor**, or **Bank Account** section, set filters if you want to create contacts from specific customers, vendors, or bank accounts.</span></span>
3. <span data-ttu-id="902ae-125">Klicken Sie auf die Schaltfläche **OK**, um mit dem Erstellen von Kontakten zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="902ae-125">Choose the **OK** button to start creating contacts.</span></span>

    <span data-ttu-id="902ae-126">Den neuen Kontakten werden die nächsten Kontaktnummern aus der Nummernserie zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="902ae-126">The next contact numbers in the number series are assigned to the new contacts.</span></span> <span data-ttu-id="902ae-127">Den neu erstellten Kontakten wird automatisch die Geschäftsbeziehung für Kreditoren zugewiesen, die im Fenster **Marketing & Vertrieb Einr.** festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="902ae-127">The business relation for vendors that is specified in the **Marketing Setup** window is assigned to the newly created contacts.</span></span>

> [!TIP]  
>   <span data-ttu-id="902ae-128">Sie können auch einen Debitor, Kreditor oder Bankkonto über einen Kontakt erstellen.</span><span class="sxs-lookup"><span data-stu-id="902ae-128">You can also create a customer, vendor, or bank account from a contact.</span></span> <span data-ttu-id="902ae-129">Weitere Informationen finden Sie unter [Debitor, Kreditor oder Bankkonto über einen Kontakt erstellen](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="902ae-129">For more information, see [Create a Customer, Vendor, or Bank Account From a Contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="902ae-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="902ae-130">See Also</span></span>
[<span data-ttu-id="902ae-131">Synchronisieren von Kontakten mit Debitoren, Kreditoren und Bankkonten</span><span class="sxs-lookup"><span data-stu-id="902ae-131">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[<span data-ttu-id="902ae-132">Kontakten Geschäftsbeziehungen zuordnen</span><span class="sxs-lookup"><span data-stu-id="902ae-132">Assign Business Relations to a Contact</span></span>](marketing-business-relations.md#AssignBusRelContact)  
[<span data-ttu-id="902ae-133">Kontakt eine Branche zuordnen</span><span class="sxs-lookup"><span data-stu-id="902ae-133">Assign Industry Groups to a Contact</span></span>](marketing-industry-groups.md#AssignIndustryGroupContact)  
[<span data-ttu-id="902ae-134">Zuordnen von Verteiler zu einem Kontakt</span><span class="sxs-lookup"><span data-stu-id="902ae-134">Assign Mailing Groups to a Contact</span></span>](marketing-mailing-groups.md#AssignMailGroupContact)  
[<span data-ttu-id="902ae-135">Anlegen von Kontaktpersonen</span><span class="sxs-lookup"><span data-stu-id="902ae-135">Create Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="902ae-136">Arbeiten mit  Business Central</span><span class="sxs-lookup"><span data-stu-id="902ae-136">Working with Business Central</span></span>](ui-work-product.md)

