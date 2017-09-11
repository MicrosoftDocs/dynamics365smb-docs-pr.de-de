---
title: "Vorgehensweise: Buchen und überprüfen des Jahresabschlusspostens | Microsoft Docs"
description: "Beschreibt, wie Sie das Buchblatt öffnen, dass Sie in der Stapelverarbeitung \"GuV-Konten Nullstellung\" definier haben und dann den Jahresabschlusseintrag überprüfen und buchen."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 68017b8b031ee4bd368936b6fb4de157328d7030
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-post-the-year-end-closing-entry"></a><span data-ttu-id="c88a1-103">Vorgehensweise: Buchen des Jahresabschlusspostens</span><span class="sxs-lookup"><span data-stu-id="c88a1-103">How to: Post the Year-End Closing Entry</span></span>
<span data-ttu-id="c88a1-104">Nachdem Sie die Stapelverarbeitung **GuV-Konten Nullstellung** ausgeführt haben, um den bzw. die Ultimoposten für den Jahresabschluss zu generieren, müssen Sie das in der Stapelverarbeitung angegebene Buchungsblatt öffnen und die Posten überprüfen und buchen.</span><span class="sxs-lookup"><span data-stu-id="c88a1-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="c88a1-105">So buchen Sie den Jahresabschlussposten</span><span class="sxs-lookup"><span data-stu-id="c88a1-105">To post the year end closing entry</span></span>
1. <span data-ttu-id="c88a1-106">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite ober Bericht suchen") und geben **Fibu Buch.-Blatt** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="c88a1-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="c88a1-107">Wählen Sie im Fenster **Fibu Buch.Blatt** im Feld **Buch.-Blattname** das Buch.-Blatt mit den Abschlussposten aus.</span><span class="sxs-lookup"><span data-stu-id="c88a1-107">In the **General Journal** window, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="c88a1-108">Überprüfen Sie die Posten.</span><span class="sxs-lookup"><span data-stu-id="c88a1-108">Review the entries.</span></span>
4. <span data-ttu-id="c88a1-109">Wählen Sie auf der Registerkarte **Start** die Option Buchen aus, um das Buch.-Blatt zu buchen.</span><span class="sxs-lookup"><span data-stu-id="c88a1-109">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="c88a1-110">Wenn ein Fehler erkannt wird, wird eine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c88a1-110">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="c88a1-111">Wurde die Buchung ordnungsgemäß durchgeführt, werden die gebuchten Posten aus dem Buch.-Blatt entfernt.</span><span class="sxs-lookup"><span data-stu-id="c88a1-111">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="c88a1-112">Nachdem die Buchung abgeschlossen ist, wird ein Posten auf jedes GuV-Konto gebucht, sodass der Saldo des Kontos Null ist und das Jahresergebnis in die Bilanz übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="c88a1-112">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="c88a1-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c88a1-113">See Also</span></span>
[<span data-ttu-id="c88a1-114">So geht's: Buchhaltungsperioden schließen</span><span class="sxs-lookup"><span data-stu-id="c88a1-114">How to: Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="c88a1-115">Schließen der Bücher</span><span class="sxs-lookup"><span data-stu-id="c88a1-115">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="c88a1-116">GuV-Konten Nullstellung</span><span class="sxs-lookup"><span data-stu-id="c88a1-116">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="c88a1-117">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c88a1-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

