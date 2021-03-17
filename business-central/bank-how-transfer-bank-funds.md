---
title: Bank-Geldmittel überweisen| Microsoft Docs
description: Sie können Überweisungsbeträge von einem Bankkonto auf ein anders übertragen, einschließlich verschiedene Währungen, indem Sie die Transaktion im Fibu Buch.-Blatt buchen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1a0ab7c2a96c278740c07ff243ad785be1d72dd4
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388099"
---
# <a name="transfer-bank-funds"></a><span data-ttu-id="6956e-103">Bank-Geldmittel überweisen</span><span class="sxs-lookup"><span data-stu-id="6956e-103">Transfer Bank Funds</span></span>
<span data-ttu-id="6956e-104">Manchmal ist es erforderlich, einen Betrag von einem Bankkonto in [!INCLUDE[prod_short](includes/prod_short.md)] auf ein anderes Bankkonto zu überweisen.</span><span class="sxs-lookup"><span data-stu-id="6956e-104">You may sometimes need to transfer an amount from one bank account in [!INCLUDE[prod_short](includes/prod_short.md)] to another.</span></span> <span data-ttu-id="6956e-105">Dafür müssen Sie eine Transaktion auf der Seite **Fibu Buch.-Blatt** buchen.</span><span class="sxs-lookup"><span data-stu-id="6956e-105">To do this, you must post the a transaction on the **General Journal** page.</span></span> <span data-ttu-id="6956e-106">Die Aufgabe variiert abhängig davon, ob die Bankkonten dieselbe Währung oder unterschiedlichen Währungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="6956e-106">The task varies depending on whether the bank accounts use the same currency or different currencies.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a><span data-ttu-id="6956e-107">So buchen Sie Überweisungen zwischen Bankkonten mit demselben Währungscode:</span><span class="sxs-lookup"><span data-stu-id="6956e-107">To post a transfer between bank accounts with the same currency code</span></span>
1. <span data-ttu-id="6956e-108">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Fibu Buch.-Blatt** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="6956e-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="6956e-109">Füllen Sie in einer Buch.-Blattzeile die Felder **Buchungsdatum** und **Belegnr.** aus.</span><span class="sxs-lookup"><span data-stu-id="6956e-109">On a journal line, fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="6956e-110">Wählen Sie im Feld **Kontoart** die Option **Bankkonto** aus.</span><span class="sxs-lookup"><span data-stu-id="6956e-110">In the **Account Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="6956e-111">Im Feld **Kontonr.** wählen Sie das Bankkonto aus, von dem Sie die Beträge überweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="6956e-111">In the **Account No.** field, select the bank from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="6956e-112">Geben Sie im Feld **Betrag** den Betrag ein, der überwiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6956e-112">In the **Amount** field, enter the amount to be transferred.</span></span>
6. <span data-ttu-id="6956e-113">Wählen Sie die **Zeigen Sie mehrere Spalten an** Aktion aus, um alle verfügbaren Felder anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6956e-113">Choose the **Show More Columns** action to view all available fields.</span></span>
7. <span data-ttu-id="6956e-114">Wählen Sie im Feld **Gegenkontoart** die Option **Bankkonto** aus.</span><span class="sxs-lookup"><span data-stu-id="6956e-114">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
8. <span data-ttu-id="6956e-115">Im Feld **Gegenkontonr.** wählen Sie das Bankkonto aus, auf das Sie die Beträge überweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="6956e-115">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
9. <span data-ttu-id="6956e-116">Buchen Sie das Buch.-Blatt.</span><span class="sxs-lookup"><span data-stu-id="6956e-116">Post the journal.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a><span data-ttu-id="6956e-117">Überweisungen zwischen Bankkonten mit verschiedenen Währungscodes buchen:</span><span class="sxs-lookup"><span data-stu-id="6956e-117">To post a transfer between bank accounts with different currency codes</span></span>
<span data-ttu-id="6956e-118">Um Beträge zwischen Bankkonten zu transferieren, die unterschiedliche Währungen verwenden, müssen Sie zwei Fibu Buch.-Blattzeilen buchen.</span><span class="sxs-lookup"><span data-stu-id="6956e-118">To transfer funds between bank accounts that use different currencies, you must post two general journal lines.</span></span>

1. <span data-ttu-id="6956e-119">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Fibu Buch.-Blatt** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="6956e-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="6956e-120">Erstellen Sie zwei Buch.-Bl.-Zeilen und füllen Sie die Felder **Buchungsdatum** und **Belegnr.** aus.</span><span class="sxs-lookup"><span data-stu-id="6956e-120">Create two journal lines, and fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="6956e-121">Wählen Sie in der ersten Buch.-Blattzeile des Feldes **Art** **Bankkonto** aus.</span><span class="sxs-lookup"><span data-stu-id="6956e-121">On the first journal line, in the **Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="6956e-122">Im Feld **Kontonr.** wählen Sie das Bankkonto aus, von dem Sie die Beträge überweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="6956e-122">In the **Account No.** field, select the bank account from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="6956e-123">Geben Sie im Feld **Betrag** den Betrag in der Währung des Bankkontos ein.</span><span class="sxs-lookup"><span data-stu-id="6956e-123">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="6956e-124">Geben Sie die Habenbeträge mit einem Minuszeichen ein.</span><span class="sxs-lookup"><span data-stu-id="6956e-124">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="6956e-125">Geben Sie die Sollbeträge ohne ein Minuszeichen ein.</span><span class="sxs-lookup"><span data-stu-id="6956e-125">Enter debit amounts without a minus sign.</span></span>
6. <span data-ttu-id="6956e-126">Wählen Sie im Feld **Gegenkontoart** die Option **Bankkonto** aus.</span><span class="sxs-lookup"><span data-stu-id="6956e-126">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="6956e-127">Im Feld **Gegenkontonr.** wählen Sie das Bankkonto aus, auf das Sie die Beträge überweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="6956e-127">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="6956e-128">Wählen Sie in der zweiten Buch.-Blattzeile des Feldes **Art** **Bankkonto** aus.</span><span class="sxs-lookup"><span data-stu-id="6956e-128">On the second journal line, in the **Type** field, select **Bank Account**.</span></span>
9. <span data-ttu-id="6956e-129">Im Feld **Kontonr.** wählen Sie das Bankkonto aus, auf das Sie die Beträge überweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="6956e-129">In the **Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
10. <span data-ttu-id="6956e-130">Geben Sie im Feld **Betrag** den Betrag in der Währung des Bankkontos ein.</span><span class="sxs-lookup"><span data-stu-id="6956e-130">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="6956e-131">Geben Sie die Habenbeträge mit einem Minuszeichen ein.</span><span class="sxs-lookup"><span data-stu-id="6956e-131">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="6956e-132">Geben Sie die Sollbeträge ohne ein Minuszeichen ein.</span><span class="sxs-lookup"><span data-stu-id="6956e-132">Enter debit amounts without a minus sign.</span></span>
11. <span data-ttu-id="6956e-133">Wählen Sie im Feld **Gegenkontoart** die Option **Bankkonto** aus.</span><span class="sxs-lookup"><span data-stu-id="6956e-133">In the **Bal. Account Type** field, select **Bank Account**.</span></span>  
12. <span data-ttu-id="6956e-134">Im Feld **Gegenkontonr.** wählen Sie das Bankkonto aus, von dem Sie die Beträge überweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="6956e-134">In the **Bal. Account No.** field, select the bank account from which you want to transfer the funds.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="6956e-135">Wenn die im Buch.-Blatt verwendeten Wechselkurse von den Wechselkursen auf der Seite **Währungswechselkurse** abweichen, geben Sie eine dritte Zeile für den Wechselkursgewinn oder -verlust ein.</span><span class="sxs-lookup"><span data-stu-id="6956e-135">If the exchange rates used in the journal are different than the exchange rates on the **Currency Exchange Rates** page, enter a third line for the exchange rate gain or loss.</span></span> <span data-ttu-id="6956e-136">Geben Sie **Sachkonto** im Feld **Kontoart** ein.</span><span class="sxs-lookup"><span data-stu-id="6956e-136">Enter **G/L Account** in the **Account Type** field.</span></span> <span data-ttu-id="6956e-137">Geben Sie die Sachkontonummer für Wechselkursgewinn oder -verlust im Feld **Kontonr.** ein.</span><span class="sxs-lookup"><span data-stu-id="6956e-137">Enter the G/L account number for exchange rate gain or loss in the **Account No.** field.</span></span> <span data-ttu-id="6956e-138">Geben Sie den Wechselkursgewinn oder - verlust im Feld **Amount** mit oder ohne Minuszeichen jeweils für Soll- und Habenbeträge ein.</span><span class="sxs-lookup"><span data-stu-id="6956e-138">Enter the exchange rate gain or loss in the **Amount** field with or without a minus sign for credits and debits respectively.</span></span>
13. <span data-ttu-id="6956e-139">Buchen Sie das Buch.-Blatt.</span><span class="sxs-lookup"><span data-stu-id="6956e-139">Post the journal.</span></span>

## <a name="see-also"></a><span data-ttu-id="6956e-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6956e-140">See Also</span></span>
[<span data-ttu-id="6956e-141">Abstimmen von Bankkonten</span><span class="sxs-lookup"><span data-stu-id="6956e-141">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="6956e-142">Einrichten von Banken</span><span class="sxs-lookup"><span data-stu-id="6956e-142">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="6956e-143">Arbeiten mit Fibu Buch.-Blättern</span><span class="sxs-lookup"><span data-stu-id="6956e-143">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="6956e-144">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6956e-144">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]