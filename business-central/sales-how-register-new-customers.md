---
title: Eine Debitorenkarte erstellen, um einen neuen Debitor zu erfassen | Microsoft Docs
description: Beschreibt, wie eine Debitorenkarte erstellt wird, um Informationen zu jedem neuen Debitor oder Clients zu erfassen, an die Sie verkaufen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 06/24/2020
ms.author: sgroespe
ms.openlocfilehash: cc48c7c55edac8af9333dd04661a828c528621b8
ms.sourcegitcommit: 63102669366eb26f9c32729848170bc2e5c4d6ae
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2020
ms.locfileid: "3503973"
---
# <a name="register-new-customers"></a><span data-ttu-id="4c02d-103">Neue Debitoren registrieren</span><span class="sxs-lookup"><span data-stu-id="4c02d-103">Register New Customers</span></span>

<span data-ttu-id="4c02d-104">Debitoren sind die Herkunft Ihres Einkommens.</span><span class="sxs-lookup"><span data-stu-id="4c02d-104">Customers are the source of your income.</span></span> <span data-ttu-id="4c02d-105">Sie müssen jeden Debitor, an den Sie verkaufen, als Debitorenkarte anlegen.</span><span class="sxs-lookup"><span data-stu-id="4c02d-105">You must register each customer you sell to as a customer card.</span></span> <span data-ttu-id="4c02d-106">Debitorenkarten enthalten die Informationen, die für den Verkauf von Produkten an Debitoren erforderlich sind."</span><span class="sxs-lookup"><span data-stu-id="4c02d-106">Customer cards hold the information that is required to sell products to the customer.</span></span> <span data-ttu-id="4c02d-107">Weitere Informationen finden Sie unter [Fakturieren eines Verkaufs](sales-how-invoice-sales.md) und [Neue Artikel registrieren](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="4c02d-107">For more information, see [Invoice Sales](sales-how-invoice-sales.md) and [Register New Items](inventory-how-register-new-items.md).</span></span>  

<span data-ttu-id="4c02d-108">Bevor Sie neue Debitoren erfassen können, müssen Sie verschiedene Verkaufscodes einrichten, aus denen Sie auswählen können, wenn Sie Debitorenkarten ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="4c02d-108">Before you can register new customers, you must set up various sales codes that you can select from when you fill in customer cards.</span></span> <span data-ttu-id="4c02d-109">Weitere Informationen finden Sie unter [Einrichten von Verkäufen](sales-setup-sales.md).</span><span class="sxs-lookup"><span data-stu-id="4c02d-109">For more information, see [Setting Up Sales](sales-setup-sales.md).</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## <a name="adding-new-customers"></a><span data-ttu-id="4c02d-110">Hinzufügen neuer Kunden</span><span class="sxs-lookup"><span data-stu-id="4c02d-110">Adding new customers</span></span>

<span data-ttu-id="4c02d-111">Sie müssen eine Debitorenkarte ausfüllen, um einen neuen Debitoren zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="4c02d-111">To register a new customer, you must fill in a customer card.</span></span> <span data-ttu-id="4c02d-112">Sie können Vorlagen für verschiedene Debitorenprofile erstellen oder Debitoren ohne Vorlagen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4c02d-112">You can establish templates for different customer profiles, or you can add customers without templates.</span></span>  

> [!NOTE]  
> <span data-ttu-id="4c02d-113">Wenn es Debitorenvorlagen für verschiedene Debitorenarten gibt, dann erscheint eine Seite automatisch, wenn Sie eine neue Debitorenkarte erstellen, von der aus Sie eine entsprechende Debitorenvorlage auswählen können.</span><span class="sxs-lookup"><span data-stu-id="4c02d-113">If customer templates exist for different customer types, then a page appears when you create a new customer card from where you can select an appropriate template.</span></span> <span data-ttu-id="4c02d-114">Wenn nur eine Debitorenvorlage vorhanden ist, verwenden neue Debitorenkarten immer diese Vorlage.</span><span class="sxs-lookup"><span data-stu-id="4c02d-114">If only one customer template exists, then new customer cards always use that template.</span></span>  

### <a name="to-create-a-new-customer-card"></a><span data-ttu-id="4c02d-115">Erstellen Sie eine neue Debitorenkarte</span><span class="sxs-lookup"><span data-stu-id="4c02d-115">To create a new customer card</span></span>

1. <span data-ttu-id="4c02d-116">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link.</span><span class="sxs-lookup"><span data-stu-id="4c02d-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4c02d-117">Wählen Sie auf der Seite **Debitoren** die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="4c02d-117">On the **Customers** page, choose the **New** action.</span></span>

    <span data-ttu-id="4c02d-118">Wenn nur eine Debitorenvorlage vorhanden ist, dann öffnet sich eine neue Debitorenkarte mit den Feldern, die mit Daten aus der Vorlage ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="4c02d-118">If only one customer template exists, then a new customer card opens with some fields filled with information from the template.</span></span>

    <span data-ttu-id="4c02d-119">Wenn mehr als eine Debitorenvorlage vorhanden ist, dann öffnet sich eine Seite mit verfügbaren Debitorenvorlagen automatisch.</span><span class="sxs-lookup"><span data-stu-id="4c02d-119">If more than one customer template exists, then a page opens from which you can select a customer template.</span></span> <span data-ttu-id="4c02d-120">In diesem Fall, folgen Sie den nächsten zwei Schritten.</span><span class="sxs-lookup"><span data-stu-id="4c02d-120">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="4c02d-121">Auf der Seite **Eine Vorlage für einen neuen Debitor auswählen** wählen Sie die Vorlage, die Sie für die neue Debitorenkarte verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="4c02d-121">On the **Select a template for a new customer** page, choose the template that you want to use for the new customer card.</span></span>
4. <span data-ttu-id="4c02d-122">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="4c02d-122">Choose the **OK** button.</span></span> <span data-ttu-id="4c02d-123">Eine neue Debitorenkarte wird geöffnet mit den Feldern, die mit Daten aus der Vorlage ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="4c02d-123">A new customer card opens with some fields filled with information from the template.</span></span>  
5. <span data-ttu-id="4c02d-124">Fahren Sie fort, um Felder auf der Debitorenkarte bei Bedarf auszufüllen und zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4c02d-124">Proceed to fill or change fields on the customer card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="4c02d-125">Definieren Sie im Inforegister **Verkaufspreise** spezielle Preise oder Rabatte, die Sie dem Debitor gewähren, wenn bestimmte Kriterien, wie z.B. Artikel, Mindestbestellmenge oder Enddatum erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="4c02d-125">On the **Sales Prices** FastTab, you can view special prices or discounts that you grant for the customer if certain criteria are met, such as item, minimum order quantity, or ending date.</span></span> <span data-ttu-id="4c02d-126">Jede Zeile stellt einen Sonderpreis oder einen Zeilenrabatt dar.</span><span class="sxs-lookup"><span data-stu-id="4c02d-126">Each row represents a special price or line discount.</span></span> <span data-ttu-id="4c02d-127">Jede Spalte stellt ein Kriterium an, das gelten muss, um den Sonderpreis, den Sie im **VK-Preis**-Feld eingeben, oder den Zeilenrabatt, den Sie im **Zeilenrabatt**-Feld eingeben, zu rechtfertigen.</span><span class="sxs-lookup"><span data-stu-id="4c02d-127">Each column represents a criterion that must apply to warrant the special price that you enter in the **Unit Price** field, or the line discount that you enter in the **Line Discount %** field.</span></span> <span data-ttu-id="4c02d-128">Weitere Informationen finden Sie unter [Erfassen von Verkaufspreisen, Rabatt und Zahlungsvereinbarungen](sales-how-record-sales-price-discount-payment-agreements.md)</span><span class="sxs-lookup"><span data-stu-id="4c02d-128">For more information, see [Record Sales Price, Discount, and Payment Agreements](sales-how-record-sales-price-discount-payment-agreements.md).</span></span>

<span data-ttu-id="4c02d-129">Der Debitor ist nun erfasst und die Debitorenkarte ist bereit, in Geschäftsbelegen verwendet zu werden, in denen Sie mit dem Debitor handeln.</span><span class="sxs-lookup"><span data-stu-id="4c02d-129">The customer is now registered, and the customer card is ready to be used on sales documents.</span></span>

<span data-ttu-id="4c02d-130">Wenn Sie diese Debitorenkarte als Vorlage verwenden möchten, fahren Sie fort, um sie als Debitorenvorlage zu speichern.</span><span class="sxs-lookup"><span data-stu-id="4c02d-130">If you want to use this customer card as a template when you create new customer cards, you can save it as a template.</span></span> <span data-ttu-id="4c02d-131">Weitere Informationen finden Sie im folgenden Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="4c02d-131">For more information, see the following section.</span></span>  

### <a name="to-save-the-customer-card-as-a-template"></a><span data-ttu-id="4c02d-132">Um die Debitorenkarte als Vorlage zu speichern</span><span class="sxs-lookup"><span data-stu-id="4c02d-132">To save the customer card as a template</span></span>

1. <span data-ttu-id="4c02d-133">Wählen Sie auf der Seite **Debitorenkarte** die Aktion **Als Vorlage speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="4c02d-133">On the **Customer Card** page, choose the **Save as Template** action.</span></span> <span data-ttu-id="4c02d-134">Die Seite **Debitorenvorlage** wird geöffnet und zeigt die Debitorenkarte als Vorlage.</span><span class="sxs-lookup"><span data-stu-id="4c02d-134">The **Customer Template** page opens showing the customer card as a template.</span></span>
2. <span data-ttu-id="4c02d-135">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="4c02d-135">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="4c02d-136">Um Dimensionen in den Vorlagen wiederzuverwenden, wählen Sie die Aktion **Dimensionen**.</span><span class="sxs-lookup"><span data-stu-id="4c02d-136">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="4c02d-137">Die Seite **Dimensionen Vorlagen** wird geöffnet und zeigt alle Dimensionscodes, die für den Debitor eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="4c02d-137">The **Dimension Templates** page opens showing any dimension codes that are set up for the customer.</span></span>
4. <span data-ttu-id="4c02d-138">Bearbeiten Sie oder geben Sie Dimensionscodes ein, die für die neuen Debitorenkarten gelten, die mit der Vorlage erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="4c02d-138">Edit or enter dimension codes that will apply to new customer cards created by using the template.</span></span>  
5. <span data-ttu-id="4c02d-139">Wenn Sie die neue Debitorenvorlage abgeschlossen haben, wählen Sie die Schaltfläche **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c02d-139">When you have completed the new customer template, choose the **OK** button.</span></span>

<span data-ttu-id="4c02d-140">Die Debitorenvorlage wird der Liste von Debitorenvorlagen hinzugefügt, damit Sie diese verwenden können, um neue Debitorenkarten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4c02d-140">The customer template is added to the list of customer templates, so that you can use it to create new customer cards.</span></span>

## <a name="deleting-customer-cards"></a><span data-ttu-id="4c02d-141">Löschen von Debitorenkarten</span><span class="sxs-lookup"><span data-stu-id="4c02d-141">Deleting customer cards</span></span>

<span data-ttu-id="4c02d-142">Wenn Sie eine Transaktion für einen Debitor gebucht haben, können Sie die Karte nicht löschen, da die Posten möglicherweise für die Prüfung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="4c02d-142">If you have posted a transaction for a customer, you cannot delete the card because the ledger entries may be needed for auditing.</span></span> <span data-ttu-id="4c02d-143">Um Debitorenkarten mit Posten zu löschen, wenden Sie sich an einen Microsoft-Partner, um dies über einen Code durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="4c02d-143">To delete customer cards with ledger entries, contact to Microsoft partner to do so through code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4c02d-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c02d-144">See Also</span></span>

[<span data-ttu-id="4c02d-145">Zahlungsformen definieren</span><span class="sxs-lookup"><span data-stu-id="4c02d-145">Defining Payment Methods</span></span>](finance-payment-methods.md)  
[<span data-ttu-id="4c02d-146">Doppelt Datensätze zusammenführen</span><span class="sxs-lookup"><span data-stu-id="4c02d-146">Merge Duplicate Records</span></span>](sales-how-merge-duplicate-records.md)  
[<span data-ttu-id="4c02d-147">Erstellen von Nummernkreisen</span><span class="sxs-lookup"><span data-stu-id="4c02d-147">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="4c02d-148">Verkauf</span><span class="sxs-lookup"><span data-stu-id="4c02d-148">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="4c02d-149">Einrichten von Verkäufen</span><span class="sxs-lookup"><span data-stu-id="4c02d-149">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="4c02d-150">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4c02d-150">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
