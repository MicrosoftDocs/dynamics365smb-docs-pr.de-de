---
title: Erfassen von Aufwendungen oder Umsatz direkt in der Finanzbuchhaltung| Microsoft Docs
description: "Für Geschäftsaktivitäten, die nicht in einem Beleg festgehlaten sind, wie kleinere Aufwendungen oder Zahlungseingänge, können Sie die entsprechenden Transaktionen erstellen, indem Sie die Buch.-Blattzeilen im Fibu Buch.-Blatt buchen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 06/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7fa0d6b604a60e000208287546d831690a914931
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-post-transactions-directly-to-the-general-ledger"></a><span data-ttu-id="9f8b4-103">Vorgehensweise: Transaktionen direkt in die Finanzbuchhaltung buchen</span><span class="sxs-lookup"><span data-stu-id="9f8b4-103">How to: Post Transactions Directly to the General Ledger</span></span>
<span data-ttu-id="9f8b4-104">Die meisten Finanztransaktionen werden in der Finanzbuchhaltung von Geschäftsbelegen wie Einkaufsrechnungen und Verkaufsaufträge gebucht.</span><span class="sxs-lookup"><span data-stu-id="9f8b4-104">Most financial transactions are posted to the general ledger through dedicated business documents, such as purchase invoices and sales orders.</span></span> <span data-ttu-id="9f8b4-105">Für Geschäftsaktivitäten, die nicht in einem Beleg in[!INCLUDE[d365fin](includes/d365fin_md.md)] festgehlaten sind, wie kleinere Aufwendungen oder Zahlungseingänge, können Sie die entsprechenden Transaktionen erstellen, indem Sie die Buch.-Blattzeilen im **Fibu Buch.-Blatt** buchen.</span><span class="sxs-lookup"><span data-stu-id="9f8b4-105">For business activities that are not represented by a document in [!INCLUDE[d365fin](includes/d365fin_md.md)], such as smaller expenses or cash receipts, you can create the related transactions by posting journal lines in the **General Journal** window.</span></span>

<span data-ttu-id="9f8b4-106">Fibu Buch.-Blätter dienen zum Buchen auf Sachkonten sowie auf andere Konten wie Bank-, Debitoren-, Kreditoren- oder Anlagekonten.</span><span class="sxs-lookup"><span data-stu-id="9f8b4-106">General journals post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, and vendor accounts.</span></span> <span data-ttu-id="9f8b4-107">Bei der Buchung mit einem Fibu Buch.-Blatt werden immer Posten für Sachkonten erstellt.</span><span class="sxs-lookup"><span data-stu-id="9f8b4-107">Posting with a general journal always creates entries on general ledger accounts.</span></span> <span data-ttu-id="9f8b4-108">Dies gilt auch, wenn beispielsweise eine Buch.-Blattzeile auf ein Debitorenkonto gebucht wird, da ein Posten im Rahmen einer Buchungsgruppe auf ein Fibu-Debitorenkonto gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="9f8b4-108">This is true even when, for example, you post a journal line to a customer account, because an entry is posted to a general ledger receivables account through a posting group.</span></span> <span data-ttu-id="9f8b4-109">Sie können Ihre Version eines Fibu Buch.-Blattes anpassen, indem Sie einen Buch.-Blattnamen oder eine Vorlage einrichten.</span><span class="sxs-lookup"><span data-stu-id="9f8b4-109">You can personalize your version of a general journal by setting up a journal batch or template.</span></span> <span data-ttu-id="9f8b4-110">Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)</span><span class="sxs-lookup"><span data-stu-id="9f8b4-110">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>

<span data-ttu-id="9f8b4-111">Anders als für Posten, die mit Belegen gebucht werden, die einen Gutschriftsvorgang benötigen, können Sie Posten ordnungsgemäß stornieren, die mit dem Buch.-Blatt gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="9f8b4-111">Unlike for entries that are posted with documents, which require a credit memo process, you can correctly reverse entries that are posted with the general journal.</span></span> <span data-ttu-id="9f8b4-112">Weitere Informationen finden Sie unter [Stornieren von Buch.-Blattbuchungen](finance-how-reverse-journal-posting.md).</span><span class="sxs-lookup"><span data-stu-id="9f8b4-112">For more information, see [How to: Reverse Journal Posting](finance-how-reverse-journal-posting.md).</span></span>

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a><span data-ttu-id="9f8b4-113">Transaktionen direkt in die Finanzbuchhaltung buchen</span><span class="sxs-lookup"><span data-stu-id="9f8b4-113">To post a transaction directly to a general ledger account</span></span>
1. <span data-ttu-id="9f8b4-114">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Fibu Buch.-Blatt** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="9f8b4-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="9f8b4-115">Öffnet das entsprechende Fibu Buch.-Blatt</span><span class="sxs-lookup"><span data-stu-id="9f8b4-115">Open the relevant general journal batch.</span></span> <span data-ttu-id="9f8b4-116">Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)</span><span class="sxs-lookup"><span data-stu-id="9f8b4-116">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="9f8b4-117">Füllen Sie die Felder in einer neuen Zeile wie erforderlich aus.</span><span class="sxs-lookup"><span data-stu-id="9f8b4-117">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    
4. <span data-ttu-id="9f8b4-118">Wiederholen Sie Schritt 3 für jede separate Transaktion, die Sie buchen möchten.</span><span class="sxs-lookup"><span data-stu-id="9f8b4-118">Repeat step 3 for all the separate transactions that you want to post.</span></span>

    > [!TIP]  
    > <span data-ttu-id="9f8b4-119">Wenn Sie Zeilen mit mehreren Transaktion über eine Gegenkontozeile, beispielsweise für das Bankkonto eingeben möchten, wählen Sie das Kontrollkästchen **Ausgleichsbetrag vorschlagen** in der Zeile für Ihren Stapel im **Fibu Buch.-Blattnamen** aus.</span><span class="sxs-lookup"><span data-stu-id="9f8b4-119">If you want to enter multiple transaction lines above one balance-account line, for example, for one bank account, then select the **Suggest Balancing Amount** check box on the line for your batch in the **General Journal Batches** window.</span></span> <span data-ttu-id="9f8b4-120">Dann werden das Feld **Betrag** auf der Gegenkontozeile automatisch mit dem Wert ausgefüllt, der erforderlich ist, um Transaktionen auszugleichen.</span><span class="sxs-lookup"><span data-stu-id="9f8b4-120">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the transactions.</span></span>
5. <span data-ttu-id="9f8b4-121">Wählen Sie die **Buchen** Aktion aus, um die Transaktionen in den angegebenen Sachkonten zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="9f8b4-121">Choose the **Post** action to record the transactions on the specified G/L accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="9f8b4-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f8b4-122">See Also</span></span>
[<span data-ttu-id="9f8b4-123">Arbeiten mit Fibu Buch.-Blättern</span><span class="sxs-lookup"><span data-stu-id="9f8b4-123">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="9f8b4-124">So geht's: Buch.-Blatt-Buchungen stornieren</span><span class="sxs-lookup"><span data-stu-id="9f8b4-124">How to: Reverse Journal Posting</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="9f8b4-125">Finanzen</span><span class="sxs-lookup"><span data-stu-id="9f8b4-125">Finance</span></span>](finance.md)  
<span data-ttu-id="9f8b4-126">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9f8b4-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

