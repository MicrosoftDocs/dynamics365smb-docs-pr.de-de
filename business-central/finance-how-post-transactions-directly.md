---
title: Erfassen von Aufwendungen oder Umsatz direkt in der Finanzbuchhaltung| Microsoft Docs
description: Für Geschäftsaktivitäten, die nicht in einem Beleg festgehlaten sind, wie kleinere Aufwendungen oder Zahlungseingänge, können Sie die entsprechenden Transaktionen erstellen, indem Sie die Buch.-Blattzeilen im Fibu Buch.-Blatt buchen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e0beff15352fb8e57f57c9d0ffdcd76bc28afbb9
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782379"
---
# <a name="post-transactions-directly-to-the-general-ledger"></a><span data-ttu-id="2c51c-103">Buchen von Transaktionen direkt in der Finanzbuchhaltung</span><span class="sxs-lookup"><span data-stu-id="2c51c-103">Post Transactions Directly to the General Ledger</span></span>

<span data-ttu-id="2c51c-104">Fibu Buch.-Blätter dienen zum Buchen auf Sachkonten sowie auf andere Konten wie Bank-, Debitoren-, Debitoren- oder Mitarbeiterkonten.</span><span class="sxs-lookup"><span data-stu-id="2c51c-104">You use general journals to post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, vendor, and employee accounts.</span></span>  

<span data-ttu-id="2c51c-105">Eine typische Verwendung des Fibu Buch.-Blatt gehört die Buchung der Kosten der Mitarbeiter während  Geschäftsaktivitäten zur späteren Rückvergütung.</span><span class="sxs-lookup"><span data-stu-id="2c51c-105">A typical use of the general journal is to post employees' expenditure of own money during business activities, for later reimbursement.</span></span> <span data-ttu-id="2c51c-106">Weitere Informationen finden Sie unter [Erstatten Sie die Ausgaben der Mitarbeiter zurück](finance-how-record-reimburse-employee-expenses.md).</span><span class="sxs-lookup"><span data-stu-id="2c51c-106">For more information, see [Record and Reimburse Employees' Expenses](finance-how-record-reimburse-employee-expenses.md).</span></span>

<span data-ttu-id="2c51c-107">Fibu Buch.-Blätter dienen zum Buchen auf Sachkonten sowie auf andere Konten wie Bank-, Debitoren-, Kreditoren- oder Mitarbeiterkonten.</span><span class="sxs-lookup"><span data-stu-id="2c51c-107">General journals post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, vendor, and employee accounts.</span></span> <span data-ttu-id="2c51c-108">Bei der Buchung mit einem Fibu Buch.-Blatt werden immer Posten für Sachkonten erstellt.</span><span class="sxs-lookup"><span data-stu-id="2c51c-108">Posting with a general journal always creates entries on general ledger accounts.</span></span> <span data-ttu-id="2c51c-109">Dies gilt auch, wenn beispielsweise eine Buch.-Blattzeile auf ein Debitorenkonto gebucht wird, da ein Posten im Rahmen einer Buchungsgruppe auf ein Fibu-Debitorenkonto gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="2c51c-109">This is true even when, for example, you post a journal line to a customer account, because an entry is posted to a general ledger receivables account through a posting group.</span></span> <span data-ttu-id="2c51c-110">Sie können Ihre Version eines Fibu Buch.-Blattes anpassen, indem Sie einen Buch.-Blattnamen oder eine Vorlage einrichten.</span><span class="sxs-lookup"><span data-stu-id="2c51c-110">You can personalize your version of a general journal by setting up a journal batch or template.</span></span> <span data-ttu-id="2c51c-111">Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)</span><span class="sxs-lookup"><span data-stu-id="2c51c-111">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>

<span data-ttu-id="2c51c-112">Anders als für Posten, die mit Belegen gebucht werden, die einen Gutschriftsvorgang benötigen, können Sie Posten ordnungsgemäß stornieren, die mit dem Buch.-Blatt gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="2c51c-112">Unlike for entries that are posted with documents, which require a credit memo process, you can correctly reverse entries that are posted with the general journal.</span></span> <span data-ttu-id="2c51c-113">Weitere Informationen finden Sie unter [Buchungen stornieren und Belege/Lieferungen rückgängig machen](finance-how-reverse-journal-posting.md).</span><span class="sxs-lookup"><span data-stu-id="2c51c-113">For more information, see [Reverse Journal Postings and Undo Receipts/Shipments](finance-how-reverse-journal-posting.md).</span></span>

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a><span data-ttu-id="2c51c-114">Transaktionen direkt in die Finanzbuchhaltung buchen</span><span class="sxs-lookup"><span data-stu-id="2c51c-114">To post a transaction directly to a general ledger account</span></span>

1. <span data-ttu-id="2c51c-115">Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Buch.-Blätter** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="2c51c-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="2c51c-116">Öffnet das entsprechende Fibu Buch.-Blatt</span><span class="sxs-lookup"><span data-stu-id="2c51c-116">Open the relevant general journal batch.</span></span> <span data-ttu-id="2c51c-117">Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)</span><span class="sxs-lookup"><span data-stu-id="2c51c-117">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="2c51c-118">Füllen Sie die Felder in einer neuen Zeile wie erforderlich aus.</span><span class="sxs-lookup"><span data-stu-id="2c51c-118">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. <span data-ttu-id="2c51c-119">Wiederholen Sie Schritt 3 für jede separate Transaktion, die Sie buchen möchten.</span><span class="sxs-lookup"><span data-stu-id="2c51c-119">Repeat step 3 for all the separate transactions that you want to post.</span></span>

    > [!TIP]  
    > <span data-ttu-id="2c51c-120">Wenn Sie Zeilen mit mehreren Transaktion über eine Gegenkontozeile, beispielsweise für das Bankkonto eingeben möchten, wählen Sie das Kontrollkästchen **Ausgleichsbetrag vorschlagen** in der Zeile für Ihren Stapel im **Fibu Buch.-Blattnamen** aus.</span><span class="sxs-lookup"><span data-stu-id="2c51c-120">If you want to enter multiple transaction lines above one balance-account line, for example, for one bank account, then select the **Suggest Balancing Amount** check box on the line for your batch on the **General Journal Batches** page.</span></span> <span data-ttu-id="2c51c-121">Dann werden das Feld **Betrag** auf der Gegenkontozeile automatisch mit dem Wert ausgefüllt, der erforderlich ist, um Transaktionen auszugleichen.</span><span class="sxs-lookup"><span data-stu-id="2c51c-121">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the transactions.</span></span>
5. <span data-ttu-id="2c51c-122">Wählen Sie die **Buchen** Aktion aus, um die Transaktionen in den angegebenen Sachkonten zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="2c51c-122">Choose the **Post** action to record the transactions on the specified G/L accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="2c51c-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c51c-123">See Also</span></span>

[<span data-ttu-id="2c51c-124">Arbeiten mit Fibu Buch.-Blättern</span><span class="sxs-lookup"><span data-stu-id="2c51c-124">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="2c51c-125">Geschäftsverwandte Ausgaben der Beschäftigten aufzeichnen und zurückzahlen</span><span class="sxs-lookup"><span data-stu-id="2c51c-125">Record and Reimburse Employees' Expenses</span></span>](finance-how-record-reimburse-employee-expenses.md)  
[<span data-ttu-id="2c51c-126">Buchungen stornieren und Belege/Lieferungen rückgängig machen</span><span class="sxs-lookup"><span data-stu-id="2c51c-126">Reverse Journal Postings and Undo Receipts/Shipments</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="2c51c-127">Finanzen</span><span class="sxs-lookup"><span data-stu-id="2c51c-127">Finance</span></span>](finance.md)  
<span data-ttu-id="2c51c-128">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2c51c-128">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]