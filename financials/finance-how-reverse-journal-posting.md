---
title: "Eine Buch.-Blatt-Buchung rückgängig machen, indem ein Rückbuchung gemacht wird| Microsoft Docs"
description: "Wenn Sie fehlerhafte Buchungen im Fibu Buch.-Blatt vorgenommen haben, können Sie die Funktion verwenden, um die korrekte Buchung mit einem Protokoll zu stornieren."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 06/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 8126a53d59e72276eb1558fd65fe3c0cd53600cc
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-reverse-journal-posting"></a><span data-ttu-id="ecc6e-103">So geht's: Buch.-Blatt-Buchungen stornieren</span><span class="sxs-lookup"><span data-stu-id="ecc6e-103">How to: Reverse Journal Posting</span></span>
<span data-ttu-id="ecc6e-104">Zum Stornieren (Rückgängig machen) fehlerhafter Buch.-Blattbuchungen wählen Sie einen Posten und erstellen einen Korrekturposten (ein Posten, die mit dem ursprünglichen Posten identisch ist, jedoch im Betragsfeld ein umgekehrtes Vorzeichen aufweist) mit derselben Belegnummer und demselben Belegdatum wie der ursprüngliche Posten.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-104">To undo an erroneous journal posting, you select the entry and create a reverse entry (entries identical to the original entry but with opposite sign in the amount field) with the same document number and posting date as the original entry.</span></span> <span data-ttu-id="ecc6e-105">Nachdem Sie einen Posten storniert haben, müssen Sie den Korrekturposten erstellen.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-105">After reversing an entry, you must make the correct entry.</span></span>

<span data-ttu-id="ecc6e-106">Storniert werden können nur Posten, die in eine Zeile eines Fibu Buch.-Blattes gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-106">You can only reverse entries that are posted from a general journal line.</span></span> <span data-ttu-id="ecc6e-107">Ein Posten kann nur einmal storniert werden.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-107">An entry can only be reversed once.</span></span>

<span data-ttu-id="ecc6e-108">Weitere Informationen zum Buchen eines Fibu Buch.-Blatt, siehe [Vorgehensweise: Beitrags-Transaktionen in die Finanzbuchhaltung](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="ecc6e-108">For more information about posting from a general journal, see [How to: Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>

<span data-ttu-id="ecc6e-109">Posten können in allen **Posten** storniert werden.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-109">You can reverse entries from all **Ledger Entries** windows.</span></span> <span data-ttu-id="ecc6e-110">Das folgende Verfahren basiert auf dem **Sachposten** Fenster.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-110">The following procedure is based on the **General Ledger Entries** window.</span></span>

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a><span data-ttu-id="ecc6e-111">Um die Buch.-Blatt-Buchung eines Sachpostens zu stornieren</span><span class="sxs-lookup"><span data-stu-id="ecc6e-111">To reverse the journal posting of a general ledger entry</span></span>
1. <span data-ttu-id="ecc6e-112">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Finanzbuchhaltung einrichten** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Ledger Entries**, and then choose the related link.</span></span>
2. <span data-ttu-id="ecc6e-113">Wählen Sie den Posten, den Sie stornieren möchten, und wählen die **Transaktion stornieren** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-113">Select the entry that you want to reverse, and then choose the **Reverse Transaction** action.</span></span> <span data-ttu-id="ecc6e-114">Beachten Sie, das sie aus einer Buch.-Blatt-Buchung stammen muss.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-114">Note that is must originate from a journal posting.</span></span>
3. <span data-ttu-id="ecc6e-115">Im Fenster **Transaktionsposten stornieren** wählen Sie den entsprechenden Posten, und wählen die **Stornieren** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-115">In the **Reverse Transaction Entries** window, select the relevant entry, and then choose the **Reverse** action.</span></span>
4. <span data-ttu-id="ecc6e-116">Klicken Sie auf die Schaltfläche **Ja** auf der Bestätigungsnachricht.</span><span class="sxs-lookup"><span data-stu-id="ecc6e-116">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="see-also"></a><span data-ttu-id="ecc6e-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ecc6e-117">See Also</span></span>
[<span data-ttu-id="ecc6e-118">Vorgehensweise: Transaktionen direkt in die Finanzbuchhaltung buchen</span><span class="sxs-lookup"><span data-stu-id="ecc6e-118">How to: Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="ecc6e-119">Arbeiten mit Fibu Buch.-Blättern</span><span class="sxs-lookup"><span data-stu-id="ecc6e-119">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="ecc6e-120">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ecc6e-120">Finance</span></span>](finance.md)  
<span data-ttu-id="ecc6e-121">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ecc6e-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

