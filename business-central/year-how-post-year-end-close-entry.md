---
title: "Vorgehensweise: Buchen und überprüfen des Jahresabschlusspostens | Microsoft Docs"
description: "Beschreibt, wie Sie das Buchblatt öffnen, dass Sie in der Stapelverarbeitung \"GuV-Konten Nullstellung\" definier haben und dann den Jahresabschlusseintrag überprüfen und buchen."
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
ms.openlocfilehash: 0a5eaa15fdfbc1d578d755b246b0304030a82b1c
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="post-the-year-end-closing-entry"></a><span data-ttu-id="c3c89-103">So buchen Sie den Jahresabschlussposten</span><span class="sxs-lookup"><span data-stu-id="c3c89-103">Post the Year-End Closing Entry</span></span>
<span data-ttu-id="c3c89-104">Nachdem Sie die Stapelverarbeitung **GuV-Konten Nullstellung** ausgeführt haben, um den bzw. die Ultimoposten für den Jahresabschluss zu generieren, müssen Sie das in der Stapelverarbeitung angegebene Buchungsblatt öffnen und die Posten überprüfen und buchen.</span><span class="sxs-lookup"><span data-stu-id="c3c89-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="c3c89-105">So buchen Sie den Jahresabschlussposten</span><span class="sxs-lookup"><span data-stu-id="c3c89-105">To post the year end closing entry</span></span>
1. <span data-ttu-id="c3c89-106">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Allgemeine Buch.-Blätter** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="c3c89-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="c3c89-107">Wählen Sie im Fenster **Fibu Buch.Blatt** im Feld **Buch.-Blattname** das Buch.-Blatt mit den Abschlussposten aus.</span><span class="sxs-lookup"><span data-stu-id="c3c89-107">In the **General Journal** window, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="c3c89-108">Überprüfen Sie die Posten.</span><span class="sxs-lookup"><span data-stu-id="c3c89-108">Review the entries.</span></span>
4. <span data-ttu-id="c3c89-109">Wählen Sie auf der Registerkarte **Start** die Option Buchen aus, um das Buch.-Blatt zu buchen.</span><span class="sxs-lookup"><span data-stu-id="c3c89-109">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="c3c89-110">Wenn ein Fehler erkannt wird, wird eine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c3c89-110">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="c3c89-111">Wurde die Buchung ordnungsgemäß durchgeführt, werden die gebuchten Posten aus dem Buch.-Blatt entfernt.</span><span class="sxs-lookup"><span data-stu-id="c3c89-111">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="c3c89-112">Nachdem die Buchung abgeschlossen ist, wird ein Posten auf jedes GuV-Konto gebucht, sodass der Saldo des Kontos Null ist und das Jahresergebnis in die Bilanz übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="c3c89-112">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="c3c89-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3c89-113">See Also</span></span>
[<span data-ttu-id="c3c89-114">Schließen von Buchhaltungsperioden</span><span class="sxs-lookup"><span data-stu-id="c3c89-114">Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="c3c89-115">Schließen der Bücher</span><span class="sxs-lookup"><span data-stu-id="c3c89-115">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="c3c89-116">GuV-Konten Nullstellung</span><span class="sxs-lookup"><span data-stu-id="c3c89-116">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="c3c89-117">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c3c89-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

