---
title: "Abschließen der Buchhaltungsperioden für ein Geschäftsjahr | Microsoft Docs"
description: "Beschreibt, wie Sie die Buchhaltungsperioden schließen, die das Geschäftsjahr ausmachen."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 859801a5e9d9b900aed6af5fe672f650932b2e79
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-close-accounting-periods"></a><span data-ttu-id="ca0cb-103">So geht's: Buchhaltungsperioden schließen</span><span class="sxs-lookup"><span data-stu-id="ca0cb-103">How to: Close Accounting Periods</span></span>
<span data-ttu-id="ca0cb-104">Wenn ein Geschäftsjahr vorbei ist, müssen die Perioden, aus denen es besteht, geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="ca0cb-104">When a fiscal year is over, you must close the periods that comprise it.</span></span>

## <a name="to-close-accounting-periods"></a><span data-ttu-id="ca0cb-105">Buchhaltungsperioden schließen:</span><span class="sxs-lookup"><span data-stu-id="ca0cb-105">To close accounting periods</span></span>
1. <span data-ttu-id="ca0cb-106">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Buchungsperioden** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="ca0cb-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Accounting Periods**, and then choose the related link.</span></span>
2. <span data-ttu-id="ca0cb-107">Im Fenster **Buchhaltungsperioden** wählen Sie die Aktion **Jahr abschließen**.</span><span class="sxs-lookup"><span data-stu-id="ca0cb-107">In the **Accounting Periods** window, choose the **Close Year** action.</span></span>

    <span data-ttu-id="ca0cb-108">Sind mehrere Geschäftsjahre offen, wird angenommen, dass das früheste automatisch abgeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ca0cb-108">If more than one fiscal year is open, the earliest one is automatically selected to be closed.</span></span> <span data-ttu-id="ca0cb-109">Ein Mitteilungsfenster wird angezeigt, in dem das zu schließende Jahr angegeben wird und die Konsequenzen erklärt werden.</span><span class="sxs-lookup"><span data-stu-id="ca0cb-109">A message displays identifying the year that will close and the consequences of closing the year.</span></span>
3. <span data-ttu-id="ca0cb-110">Wählen Sie die Schaltfläche **Ja** aus, um das Jahr zu schließen.</span><span class="sxs-lookup"><span data-stu-id="ca0cb-110">To close the year, choose the **Yes** button.</span></span>

<span data-ttu-id="ca0cb-111">Das Geschäftsjahr ist geschlossen und die Felder **Abgeschlossen** und **Datum gesperrt** werden für alle Perioden des Jahres aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ca0cb-111">The fiscal year is closed, and the **Closed** and **Date Locked** fields for all the periods in the year are selected.</span></span> <span data-ttu-id="ca0cb-112">Das Geschäftsjahr kann nicht erneut geöffnet werden und Sie können das Häkchen aus den Feldern **Abgeschlossen** oder **Datum gesperrt** nicht mehr entfernen.</span><span class="sxs-lookup"><span data-stu-id="ca0cb-112">The fiscal year cannot be opened again and you cannot remove the check mark from the **Closed** or **Date Locked** fields.</span></span>

> [!NOTE]  
>   <span data-ttu-id="ca0cb-113">Sie können ein Geschäftsjahr erst abschließen, wenn Sie ein neues erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="ca0cb-113">You cannot close a fiscal year before you create a new one.</span></span> <span data-ttu-id="ca0cb-114">Beachten Sie, dass Sie nach dem Abschluss eines Geschäftsjahres das Startdatum des folgenden Geschäftsjahres nicht mehr ändern können.</span><span class="sxs-lookup"><span data-stu-id="ca0cb-114">Notice that when a fiscal year has been closed, you cannot change the starting date of the following fiscal year.</span></span>

<span data-ttu-id="ca0cb-115">Auch wenn ein Geschäftsjahr abgeschlossen wurde, können hierfür noch Sachposten gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="ca0cb-115">Even though a fiscal year has been closed, you can still post general ledger entries to it.</span></span> <span data-ttu-id="ca0cb-116">In diesen Fällen wird in den Posten vermerkt, dass die Buchung in einem abgeschlossenen Geschäftsjahr erfolgte, d. h., das Feld **Nachbuchung** wird mit einem Häkchen versehen.</span><span class="sxs-lookup"><span data-stu-id="ca0cb-116">When you do this, the entries will be marked as posted to a closed fiscal year and the **Prior-Year Entry** field will be selected.</span></span>

<span data-ttu-id="ca0cb-117">Nachdem ein Geschäftsjahr abgeschlossen wurde, müssen Sie die GuV-Kontennullstellung durchführen und das Ergebnis auf ein Bilanzkonto übertragen lassen.</span><span class="sxs-lookup"><span data-stu-id="ca0cb-117">After a fiscal year is closed, you must close the income statement accounts and transfer the year's results to an account in the balance sheet.</span></span> <span data-ttu-id="ca0cb-118">Dies können das jedes Mal wiederholen, wenn Sie in ein abgeschlossenes Geschäftsjahr gebucht haben.</span><span class="sxs-lookup"><span data-stu-id="ca0cb-118">You can repeat this every time that you post to the closed fiscal year.</span></span>

## <a name="see-also"></a><span data-ttu-id="ca0cb-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca0cb-119">See Also</span></span>
[<span data-ttu-id="ca0cb-120">Schließen der Bücher</span><span class="sxs-lookup"><span data-stu-id="ca0cb-120">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="ca0cb-121">Vorgehensweise: Buchen des Jahresabschlusspostens</span><span class="sxs-lookup"><span data-stu-id="ca0cb-121">How to: Post the Year-End Closing Entry</span></span>](year-how-post-year-end-close-entry.md)  
[<span data-ttu-id="ca0cb-122">So geht's: Ein neues Geschäftsjahr eröffnen</span><span class="sxs-lookup"><span data-stu-id="ca0cb-122">How to: Open a New Fiscal Year</span></span>](finance-how-open-new-fiscal-year.md)  
<span data-ttu-id="ca0cb-123">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ca0cb-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

