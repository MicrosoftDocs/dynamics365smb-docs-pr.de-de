---
title: Bank-Geldmittel überweisen
description: Sie können Überweisungsbeträge von einem Bankkonto auf ein anders übertragen, einschließlich verschiedene Währungen, indem Sie die Transaktion im Fibu Buch.-Blatt buchen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 04/29/2021
ms.author: edupont
ms.openlocfilehash: da9c8711751040cecb267a3b2209bad2534b618b
ms.sourcegitcommit: 08ca5798cf3f04fc3ea38fff40c1860196a70adf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/06/2021
ms.locfileid: "5985387"
---
# <a name="transfer-bank-funds"></a><span data-ttu-id="c7c7c-103">Bank-Geldmittel überweisen</span><span class="sxs-lookup"><span data-stu-id="c7c7c-103">Transfer Bank Funds</span></span>

<span data-ttu-id="c7c7c-104">Manchmal ist es erforderlich, einen Betrag von einem Bankkonto in [!INCLUDE[prod_short](includes/prod_short.md)] auf ein anderes Bankkonto zu überweisen.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-104">You may sometimes need to transfer an amount from one bank account in [!INCLUDE[prod_short](includes/prod_short.md)] to another.</span></span> <span data-ttu-id="c7c7c-105">Dazu müssen Sie die Transaktion auf der Seite **Allgemeines Journal** buchen.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-105">To do this, you must post the transaction on the **General Journal** page.</span></span> <span data-ttu-id="c7c7c-106">Die Aufgabe variiert abhängig davon, ob die Bankkonten dieselbe Währung oder unterschiedlichen Währungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-106">The task varies depending on whether the bank accounts use the same currency or different currencies.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a><span data-ttu-id="c7c7c-107">So buchen Sie Überweisungen zwischen Bankkonten mit demselben Währungscode:</span><span class="sxs-lookup"><span data-stu-id="c7c7c-107">To post a transfer between bank accounts with the same currency code</span></span>

1. <span data-ttu-id="c7c7c-108">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Fibu Buch.-Blatt** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="c7c7c-109">Füllen Sie in einer Buch.-Blattzeile die Felder **Buchungsdatum** und **Belegnr.** aus.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-109">On a journal line, fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="c7c7c-110">Wählen Sie im Feld **Kontoart** die Option **Bankkonto** aus.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-110">In the **Account Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="c7c7c-111">Im Feld **Kontonr.** wählen Sie das Bankkonto aus, von dem Sie die Beträge überweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-111">In the **Account No.** field, select the bank from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="c7c7c-112">Geben Sie im Feld **Betrag** den Betrag ein, der überwiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-112">In the **Amount** field, enter the amount to be transferred.</span></span>

    <span data-ttu-id="c7c7c-113">Als nächstes müssen Sie das Ausgleichskonto angeben.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-113">Next, you must specify the balancing account.</span></span> <span data-ttu-id="c7c7c-114">Wenn Sie die relevanten Felder nicht sehen können, dann wählen Sie die Aktion **Weitere Spalten anzeigen**, um alle verfügbaren Felder anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-114">If you can't see the relevant fields, then choose the **Show More Columns** action to view all available fields.</span></span>
6. <span data-ttu-id="c7c7c-115">Wählen Sie im Feld **Gegenkontoart** die Option **Bankkonto** aus.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-115">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="c7c7c-116">Im Feld **Gegenkontonr.** wählen Sie das Bankkonto aus, auf das Sie die Beträge überweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-116">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="c7c7c-117">Buchen Sie das Buch.-Blatt.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-117">Post the journal.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a><span data-ttu-id="c7c7c-118">Überweisungen zwischen Bankkonten mit verschiedenen Währungscodes buchen:</span><span class="sxs-lookup"><span data-stu-id="c7c7c-118">To post a transfer between bank accounts with different currency codes</span></span>

<span data-ttu-id="c7c7c-119">Um Beträge zwischen Bankkonten zu transferieren, die unterschiedliche Währungen verwenden, müssen Sie zwei Fibu Buch.-Blattzeilen buchen.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-119">To transfer funds between bank accounts that use different currencies, you must post two general journal lines.</span></span>

1. <span data-ttu-id="c7c7c-120">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Fibu Buch.-Blatt** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="c7c7c-121">Erstellen Sie zwei Buch.-Bl.-Zeilen und füllen Sie die Felder **Buchungsdatum** und **Belegnr.** aus.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-121">Create two journal lines, and fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="c7c7c-122">Wählen Sie in der ersten Buch.-Blattzeile des Feldes **Art** **Bankkonto** aus.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-122">On the first journal line, in the **Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="c7c7c-123">Im Feld **Kontonr.** wählen Sie das Bankkonto aus, von dem Sie die Beträge überweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-123">In the **Account No.** field, select the bank account from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="c7c7c-124">Geben Sie im Feld **Betrag** den Betrag in der Währung des Bankkontos mit oder ohne Minuszeichen ein.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-124">In the **Amount** field, enter the amount in the currency of the bank account with or without a minus sign.</span></span>

    > [!TIP]
    > <span data-ttu-id="c7c7c-125">Ein Betrag ohne Vorzeichen ist eine Belastung, ein Betrag mit Minuszeichen ist eine Gutschrift.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-125">An amount without a sign is a debit, and an amount with a minus sign is a credit.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c7c7c-126">Einige Firmen ziehen es vor, Umlagerungen zwischen Konten in separaten Zeilen zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-126">Some companies prefer to transfer between accounts on separate journal lines.</span></span> <span data-ttu-id="c7c7c-127">Andere Firmen bevorzugen es, alles in einer Zeile zu erfassen, indem sie ein Ausgleichskonto verwenden.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-127">Other companies prefer to post everything on one journal line by using a balancing account.</span></span> <span data-ttu-id="c7c7c-128">Fragen Sie Ihren Experten, wenn Sie sich nicht sicher sind, was Sie tun sollen.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-128">Check with your local expert if you're not sure what to do.</span></span>
    >
    > <span data-ttu-id="c7c7c-129">Wenn Ihre Firma es vorzieht, ein Ausgleichskonto zu verwenden, legen Sie das Feld **Saldokontotyp** auf **Bankkonto**, und legen Sie das Feld **Saldokontonr.** auf das Bankkonto, auf das Sie das Geld überweisen wollen.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-129">If your company prefers to use a balancing account, then set the **Bal. Account Type** field to **Bank Account**, and set the **Bal. Account No.** field to the bank account to which you want to transfer the funds.</span></span> <span data-ttu-id="c7c7c-130">Fahren Sie dann mit Schritt 9 oder 10 fort.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-130">Then proceed to step 9 or 10.</span></span>
    >
    > <span data-ttu-id="c7c7c-131">Wenn Ihre Firma es vorzieht, eine separate Zeile für die Erfassung zu verwenden, dann fahren Sie mit dem nächsten Schritt fort.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-131">If your company prefers to use a separate journal line, then move on to the next step.</span></span>
6. <span data-ttu-id="c7c7c-132">Wählen Sie in der zweiten Buch.-Blattzeile des Feldes **Art** **Bankkonto** aus.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-132">On the second journal line, in the **Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="c7c7c-133">Im Feld **Kontonr.** wählen Sie das Bankkonto aus, auf das Sie die Beträge überweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-133">In the **Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="c7c7c-134">Geben Sie im Feld **Betrag** den Betrag in der Währung des Bankkontos mit oder ohne Minuszeichen ein.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-134">In the **Amount** field, enter the amount in the currency of the bank account with or without a minus sign.</span></span>

    > [!TIP]
    > <span data-ttu-id="c7c7c-135">Ein Betrag ohne Vorzeichen ist eine Belastung, ein Betrag mit Minuszeichen ist eine Gutschrift.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-135">An amount without a sign is a debit, and an amount with a minus sign is a credit.</span></span>
9. <span data-ttu-id="c7c7c-136">Wenn die im Journal verwendeten Wechselkurse von den Sätzen auf der Seite **Wechselkursrate** abweichen, geben Sie eine neue Journalzeile für den Wechselkursgewinn oder -verlust ein.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-136">If the exchange rates used in the journal are different than the exchange rates on the **Currency Exchange Rates** page, enter a new journal line for the exchange rate gain or loss.</span></span>  

    1. <span data-ttu-id="c7c7c-137">Geben Sie **Sachkonto** im Feld **Kontoart** ein.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-137">Enter **G/L Account** in the **Account Type** field.</span></span>  

    2. <span data-ttu-id="c7c7c-138">Geben Sie die Sachkontonummer für Wechselkursgewinn oder -verlust im Feld **Kontonr.** ein.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-138">Enter the G/L account number for exchange rate gain or loss in the **Account No.** field.</span></span>  

    3. <span data-ttu-id="c7c7c-139">Geben Sie den Wechselkursgewinn oder -verlust in das Feld **Betrag** mit oder ohne Minuszeichen ein.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-139">Enter the exchange rate gain or loss in the **Amount** field with or without a minus sign.</span></span>

    > [!TIP]
    > <span data-ttu-id="c7c7c-140">Ein Betrag ohne Vorzeichen ist eine Belastung, ein Betrag mit Minuszeichen ist eine Gutschrift.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-140">An amount without a sign is a debit, and an amount with a minus sign is a credit.</span></span>
10. <span data-ttu-id="c7c7c-141">Buchen Sie das Buch.-Blatt.</span><span class="sxs-lookup"><span data-stu-id="c7c7c-141">Post the journal.</span></span>

## <a name="see-also"></a><span data-ttu-id="c7c7c-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7c7c-142">See Also</span></span>

[<span data-ttu-id="c7c7c-143">Abstimmen von Bankkonten</span><span class="sxs-lookup"><span data-stu-id="c7c7c-143">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="c7c7c-144">Einrichten von Banken</span><span class="sxs-lookup"><span data-stu-id="c7c7c-144">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="c7c7c-145">Arbeiten mit Fibu Buch.-Blättern</span><span class="sxs-lookup"><span data-stu-id="c7c7c-145">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="c7c7c-146">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c7c7c-146">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]