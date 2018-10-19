---
title: "Abschließen der Buchhaltungsperioden für ein Geschäftsjahr | Microsoft Docs"
description: "Beschreibt, wie Sie die Buchhaltungsperioden schließen, die das Geschäftsjahr ausmachen."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: f0bdc88cb2d52ed8e1558fb140f904f792e539ff
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="close-accounting-periods"></a><span data-ttu-id="2f965-103">Schließen von Buchhaltungsperioden</span><span class="sxs-lookup"><span data-stu-id="2f965-103">Close Accounting Periods</span></span>
<span data-ttu-id="2f965-104">Wenn ein Geschäftsjahr vorbei ist, müssen die Perioden, aus denen es besteht, geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="2f965-104">When a fiscal year is over, you must close the periods that comprise it.</span></span>

## <a name="to-close-accounting-periods"></a><span data-ttu-id="2f965-105">Buchhaltungsperioden schließen:</span><span class="sxs-lookup"><span data-stu-id="2f965-105">To close accounting periods</span></span>
1. <span data-ttu-id="2f965-106">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Buchungsperioden** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="2f965-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Accounting Periods**, and then choose the related link.</span></span>
2. <span data-ttu-id="2f965-107">Im Fenster **Buchhaltungsperioden** wählen Sie die Aktion **Jahr abschließen**.</span><span class="sxs-lookup"><span data-stu-id="2f965-107">In the **Accounting Periods** window, choose the **Close Year** action.</span></span>

    <span data-ttu-id="2f965-108">Sind mehrere Geschäftsjahre offen, wird angenommen, dass das früheste automatisch abgeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2f965-108">If more than one fiscal year is open, the earliest one is automatically selected to be closed.</span></span> <span data-ttu-id="2f965-109">Ein Mitteilungsfenster wird angezeigt, in dem das zu schließende Jahr angegeben wird und die Konsequenzen erklärt werden.</span><span class="sxs-lookup"><span data-stu-id="2f965-109">A message displays identifying the year that will close and the consequences of closing the year.</span></span>
3. <span data-ttu-id="2f965-110">Wählen Sie die Schaltfläche **Ja** aus, um das Jahr zu schließen.</span><span class="sxs-lookup"><span data-stu-id="2f965-110">To close the year, choose the **Yes** button.</span></span>

<span data-ttu-id="2f965-111">Das Geschäftsjahr ist geschlossen und die Felder **Abgeschlossen** und **Datum gesperrt** werden für alle Perioden des Jahres aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2f965-111">The fiscal year is closed, and the **Closed** and **Date Locked** fields for all the periods in the year are selected.</span></span> <span data-ttu-id="2f965-112">Das Geschäftsjahr kann nicht erneut geöffnet werden und Sie können das Häkchen aus den Feldern **Abgeschlossen** oder **Datum gesperrt** nicht mehr entfernen.</span><span class="sxs-lookup"><span data-stu-id="2f965-112">The fiscal year cannot be opened again and you cannot remove the check mark from the **Closed** or **Date Locked** fields.</span></span>

> [!NOTE]  
>   <span data-ttu-id="2f965-113">Sie können ein Geschäftsjahr erst abschließen, wenn Sie ein neues erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="2f965-113">You cannot close a fiscal year before you create a new one.</span></span> <span data-ttu-id="2f965-114">Beachten Sie, dass Sie nach dem Abschluss eines Geschäftsjahres das Startdatum des folgenden Geschäftsjahres nicht mehr ändern können.</span><span class="sxs-lookup"><span data-stu-id="2f965-114">Notice that when a fiscal year has been closed, you cannot change the starting date of the following fiscal year.</span></span>

<span data-ttu-id="2f965-115">Auch wenn ein Geschäftsjahr abgeschlossen wurde, können hierfür noch Sachposten gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="2f965-115">Even though a fiscal year has been closed, you can still post general ledger entries to it.</span></span> <span data-ttu-id="2f965-116">In diesen Fällen wird in den Posten vermerkt, dass die Buchung in einem abgeschlossenen Geschäftsjahr erfolgte, d. h., das Feld **Nachbuchung** wird mit einem Häkchen versehen.</span><span class="sxs-lookup"><span data-stu-id="2f965-116">When you do this, the entries will be marked as posted to a closed fiscal year and the **Prior-Year Entry** field will be selected.</span></span>

<span data-ttu-id="2f965-117">Nachdem ein Geschäftsjahr abgeschlossen wurde, müssen Sie die GuV-Kontennullstellung durchführen und das Ergebnis auf ein Bilanzkonto übertragen lassen.</span><span class="sxs-lookup"><span data-stu-id="2f965-117">After a fiscal year is closed, you must close the income statement accounts and transfer the year's results to an account in the balance sheet.</span></span> <span data-ttu-id="2f965-118">Dies können das jedes Mal wiederholen, wenn Sie in ein abgeschlossenes Geschäftsjahr gebucht haben.</span><span class="sxs-lookup"><span data-stu-id="2f965-118">You can repeat this every time that you post to the closed fiscal year.</span></span>

## <a name="see-also"></a><span data-ttu-id="2f965-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f965-119">See Also</span></span>
[<span data-ttu-id="2f965-120">Schließen der Bücher</span><span class="sxs-lookup"><span data-stu-id="2f965-120">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="2f965-121">So buchen Sie den Jahresabschlussposten</span><span class="sxs-lookup"><span data-stu-id="2f965-121">Post the Year-End Closing Entry</span></span>](year-how-post-year-end-close-entry.md)  
[<span data-ttu-id="2f965-122">Ein neues Geschäftsjahres eröffnen</span><span class="sxs-lookup"><span data-stu-id="2f965-122">Open a New Fiscal Year</span></span>](finance-how-open-new-fiscal-year.md)  
<span data-ttu-id="2f965-123">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2f965-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

