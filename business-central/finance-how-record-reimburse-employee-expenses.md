---
title: Gschäftsrelevante Ausgaben der Mitarbeiter aufzeichnen und zurückzahlen
description: Buchen Sie die Kosten der Mitarbeiter mit dem Fibu Buch.-Blatt zu dem Konto und buchen Sie später die Zahlung an das Bankkonto des Mitarbeiters, dem die geschäftsverwandten Ausgaben zurückzuerstatten sind.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: dd4ce755e3414f19ae501c1d437f3e1d78d565a1
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184399"
---
# <a name="record-and-reimburse-employees-expenses"></a><span data-ttu-id="08b25-103">Geschäftsverwandte Ausgaben der Beschäftigten aufzeichnen und zurückzahlen</span><span class="sxs-lookup"><span data-stu-id="08b25-103">Record and Reimburse Employees' Expenses</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="08b25-104">unterstützt Transaktionen für Mitarbeiter auf ähnliche Weise wie für Kreditoren.</span><span class="sxs-lookup"><span data-stu-id="08b25-104">supports transactions for employees in a similar way as for vendors.</span></span> <span data-ttu-id="08b25-105">Entsprechend bestehen Mitarbeiterbuchungsgruppen, um sicherzustellen, dass Mitarbeiterposten auf den entsprechenden Konten in der Finanzbuchhaltung gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="08b25-105">Accordingly, employee posting groups exist to make sure that employee ledger entries are posted to the relevant accounts in the general ledger.</span></span>

> [!NOTE]  
> <span data-ttu-id="08b25-106">Mitarbeitertransaktionen können nur in der lokalen Währung gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="08b25-106">Employee transactions can be posted in the local currency only.</span></span> <span data-ttu-id="08b25-107">Vergütungszahlungen für Mitarbeiter unterstützen keine Skonti und Zahlungstoleranzen.</span><span class="sxs-lookup"><span data-stu-id="08b25-107">Reimbursement payments to employees do not support discounts and payment tolerances.</span></span>

<span data-ttu-id="08b25-108">Wenn die Mitarbeiter ihr eigenes Geld für die Geschäftsaktivitäten ausgeben, können Sie die Kosten auf das Konto des Mitarbeiters buchen.</span><span class="sxs-lookup"><span data-stu-id="08b25-108">If employees spend their own money during business activities, you can post the expense to the employee's account.</span></span> <span data-ttu-id="08b25-109">Dann können Sie die Kosten den Mitarbeiter zurückerstatten, indem Sie eine Zahlung auf das Bankkonto des Mitarbeiters leisten, ähnlich wie Sie Kreditoren bezahlen.</span><span class="sxs-lookup"><span data-stu-id="08b25-109">Then you can reimburse the employee by making a payment to the employee's bank account, similarly to how you pay vendors.</span></span>  

> [!TIP]
> <span data-ttu-id="08b25-110">In diesem Artikel wird erläutert, wie Sie die Ausgaben in den Büchern erfassen und die Kosten dem Mitarbeiter zurückerstatten.</span><span class="sxs-lookup"><span data-stu-id="08b25-110">This article explains how to record the expense in the books and how to reimburse the employee.</span></span> <span data-ttu-id="08b25-111">Ihre Organisation verfügt möglicherweise über ein Portal oder eine App, über die Mitarbeiter ihre Spesenabrechnungen einreichen können.</span><span class="sxs-lookup"><span data-stu-id="08b25-111">Your organization may have a portal or app where employees can submit their expense reports.</span></span>

<span data-ttu-id="08b25-112">[!INCLUDE [prod_short](includes/prod_short.md)] ist flexibel genug, um vielen verschiedenen Praktiken gerecht zu werden.</span><span class="sxs-lookup"><span data-stu-id="08b25-112">[!INCLUDE [prod_short](includes/prod_short.md)] is flexible enough to suit many different practices.</span></span> <span data-ttu-id="08b25-113">Die genauen zu verwendenden Kontonummern hängen von der Konfiguration und den Prozessen Ihrer Organisation ab.</span><span class="sxs-lookup"><span data-stu-id="08b25-113">The exact account numbers to use depends on your organization's configuration and processes.</span></span>  

## <a name="to-record-an-employees-expense"></a><span data-ttu-id="08b25-114">Um die Ausgaben eines Mitarbeiters tz erfassen</span><span class="sxs-lookup"><span data-stu-id="08b25-114">To record an employee's expense</span></span>

<span data-ttu-id="08b25-115">Sie buchen die Ausgaben der Mitarbeiter auf der Seite **Fibu Buch.-Blatt**.</span><span class="sxs-lookup"><span data-stu-id="08b25-115">You post employees' expenses on the **General Journal** page.</span></span>

1. <span data-ttu-id="08b25-116">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Buch.-Blätter** ein, und wählen Sie dann den entsprechenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="08b25-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="08b25-117">Öffnet das entsprechende Fibu Buch.-Blatt</span><span class="sxs-lookup"><span data-stu-id="08b25-117">Open the relevant general journal batch.</span></span> <span data-ttu-id="08b25-118">Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)</span><span class="sxs-lookup"><span data-stu-id="08b25-118">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="08b25-119">Füllen Sie die Felder in einer neuen Zeile wie erforderlich aus.</span><span class="sxs-lookup"><span data-stu-id="08b25-119">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. <span data-ttu-id="08b25-120">Wiederholen Sie Schritt 3 für alle Ausgaben, die der Beschäftigte hatte.</span><span class="sxs-lookup"><span data-stu-id="08b25-120">Repeat step 3 for all the expenses that the employee has incurred.</span></span>

    > [!TIP]  
    > <span data-ttu-id="08b25-121">Wenn Sie Zeilen mit mehreren Transaktion über eine Gegenkontozeile, beispielsweise für das Bankkonto des Mitarbeiters eingeben möchten, wählen Sie das Kontrollkästchen **Ausgleichsbetrag vorschlagen** auf der Seite für Ihren Stapel im **Fibu Buch.-Blattnamen** aus.</span><span class="sxs-lookup"><span data-stu-id="08b25-121">If you want to enter multiple expense lines above one balance-account line for the employee's bank account, then select the **Suggest Balancing Amount** check box on the line for your batch on the **General Journal Batches** page.</span></span> <span data-ttu-id="08b25-122">Dann werden das Feld **Betrag** auf der Gegenkontozeile automatisch mit dem Wert ausgefüllt, der erforderlich ist, um Transaktionen auszugleichen.</span><span class="sxs-lookup"><span data-stu-id="08b25-122">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the expenses.</span></span>
5. <span data-ttu-id="08b25-123">Wählen Sie die **Buchen** Aktion aus, um die Ausgaben des Kontos des Mitarbeiters zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="08b25-123">Choose the **Post** action to record the expenses on the employee's account.</span></span>

## <a name="to-reimburse-an-employee"></a><span data-ttu-id="08b25-124">Rückerstattung für Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="08b25-124">To reimburse an employee</span></span>

<span data-ttu-id="08b25-125">Sie zahlen die Kosten dem Mitarbeiter zurück, indem Sie Zahlungen zu dem Bankkonto auf der Seite **Zahlungsausgangs Buch.-Blatt** buchen.</span><span class="sxs-lookup"><span data-stu-id="08b25-125">You reimburse employees by posting payments to their bank account on the **Payment Journal** page.</span></span>  

1. <span data-ttu-id="08b25-126">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Zahlungsjournale** ein, und wählen Sie dann den entsprechenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="08b25-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="08b25-127">Öffnet das entsprechende Zahlungs-Fibu Buch.-Blatt</span><span class="sxs-lookup"><span data-stu-id="08b25-127">Open the relevant payment journal batch.</span></span> <span data-ttu-id="08b25-128">Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)</span><span class="sxs-lookup"><span data-stu-id="08b25-128">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="08b25-129">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="08b25-129">Fill in the fields as necessary.</span></span> <span data-ttu-id="08b25-130">Weitere Informationen finden Sie unter [Zahlungen durchführen](payables-make-payments.md).</span><span class="sxs-lookup"><span data-stu-id="08b25-130">For more information, see [Making Payments](payables-make-payments.md).</span></span>
4. <span data-ttu-id="08b25-131">Wählen Sie alternativ die **Mitarbeiter-Zahlung vorschlagen** Aktion aus, um automatisch Buch.-Blattzeilen für offene Mitarbeitervergütungen einzufügen.</span><span class="sxs-lookup"><span data-stu-id="08b25-131">Alternatively, choose the **Suggest Employee Payment** action to automatically insert journal lines for pending employee reimbursements.</span></span>
5. <span data-ttu-id="08b25-132">Wählen Sie die Aktion **Buchen**, um die Rückerstattung zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="08b25-132">Choose the **Post** action to register the reimbursement.</span></span>  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a><span data-ttu-id="08b25-133">Um Vergütungen mit Mitarbeiterposten ausgleichen</span><span class="sxs-lookup"><span data-stu-id="08b25-133">To reconcile reimbursements with employee ledger entries</span></span>

<span data-ttu-id="08b25-134">Sie gleichen Mitarbeiterzahlungen in den entsprechenden offenen Mitarbeiterposten gleich aus, wie Sie dies für Kreditorenzahlungen tun, zum Beispiel auf der Seite **Zahlungsabstimmungsbuch.-Blatt** in den entsprechenden Bankkontoauszugsposten.</span><span class="sxs-lookup"><span data-stu-id="08b25-134">You apply employee payments to their related open employee ledger entries in the same way as you do for vendor payments, for example on the **Payment Reconciliation Journal** page, based on the related bank statement entries.</span></span> <span data-ttu-id="08b25-135">Weitere Informationen finden Sie unter [Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="08b25-135">For more information, see [Applying Payments Automatically and Reconciling Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span> <span data-ttu-id="08b25-136">Alternativ können Sie auf der Seite **Mitarbeiter-Posten** den Eintrag manuell eingeben.</span><span class="sxs-lookup"><span data-stu-id="08b25-136">Alternatively, you can apply manually on the **Employee Ledger Entries** page.</span></span> <span data-ttu-id="08b25-137">Weitere Informationen finden Sie im dazugehörigen Artikel [Abstimmen von Kreditorenzahlungen mit dem Zahlungsjournal oder aus Kreditorenposten](payables-how-apply-purchase-transactions-manually.md).</span><span class="sxs-lookup"><span data-stu-id="08b25-137">For more information, see the related [Reconcile Vendor Payments with the Payment Journal or from Vendor Ledger Entries](payables-how-apply-purchase-transactions-manually.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="08b25-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08b25-138">See Also</span></span>

[<span data-ttu-id="08b25-139">Buchen von Transaktionen direkt in der Finanzbuchhaltung</span><span class="sxs-lookup"><span data-stu-id="08b25-139">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="08b25-140">Arbeiten mit Fibu Buch.-Blättern</span><span class="sxs-lookup"><span data-stu-id="08b25-140">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="08b25-141">Buch.-Blatt-Buchungen stornieren und Rückgängigmachung von Eingängen/Versendungen</span><span class="sxs-lookup"><span data-stu-id="08b25-141">Reverse Journal Postings and Undo Receipts/Shipments</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="08b25-142">Finanzen</span><span class="sxs-lookup"><span data-stu-id="08b25-142">Finance</span></span>](finance.md)  
<span data-ttu-id="08b25-143">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="08b25-143">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]