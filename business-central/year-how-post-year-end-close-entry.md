---
title: So buchen Sie den Jahresabschlussposten
description: Beschreibt, wie Sie das Buchblatt öffnen, dass Sie in der Stapelverarbeitung "GuV-Konten Nullstellung" definier haben und dann den Jahresabschlusseintrag überprüfen und buchen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 02/23/2021
ms.author: edupont
ms.openlocfilehash: 728a3edc1ef2200d4f28130cad6653d6b26a5b3b
ms.sourcegitcommit: a9d48272ce61e5d512a30417412b5363e56abf30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5493353"
---
# <a name="post-the-year-end-closing-entry"></a><span data-ttu-id="a3e88-103">So buchen Sie den Jahresabschlussposten</span><span class="sxs-lookup"><span data-stu-id="a3e88-103">Post the Year-End Closing Entry</span></span>

<span data-ttu-id="a3e88-104">Nachdem Sie die Stapelverarbeitung **GuV-Konten Nullstellung** ausgeführt haben, um den bzw. die Ultimoposten für den Jahresabschluss zu generieren, müssen Sie das in der Stapelverarbeitung angegebene Buchungsblatt öffnen und die Posten überprüfen und buchen.</span><span class="sxs-lookup"><span data-stu-id="a3e88-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>  

> [!TIP]
> <span data-ttu-id="a3e88-105">Abhängig von den Arbeitsprozessen Ihres Unternehmens können Sie wählen, ob Abrechnungsperioden und Geschäftsjahre in [!INCLUDE [prod_short](includes/prod_short.md)] geschlossen werden sollen oder nicht.</span><span class="sxs-lookup"><span data-stu-id="a3e88-105">Depending on your organizations work processes, you can choose to close or not close accounting periods and fiscal years in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="a3e88-106">Das folgende Verfahren setzt voraus, dass Sie das Geschäftsjahr mit der Option *Buchhaltungsperioden* abgeschlossen haben, einen Jahresabschlusseintrag mit dem Batch-Job **Gewinn- und Verlustrechnung schließen** generiert haben und nun bereit sind, den Abschlusseintrag zum Jahresende zusammen mit den Gegenbuchungen des Eigenkapitalkontos zu buchen.</span><span class="sxs-lookup"><span data-stu-id="a3e88-106">The following procedure assumes that you have closed the fiscal year using the *Accounting Periods* option, generated a year-end closing entry using the **Close Income Statement** batch job, and are now ready to post the year-end closing entry along with the offsetting equity account entries.</span></span> <span data-ttu-id="a3e88-107">Ihre Organisation kann sich dafür entscheiden, anders zu arbeiten, z. B. den Abschluss zum Jahresende als Teil des Abschlusses des Geschäftsjahres zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="a3e88-107">Your organization can choose to work differently, such as post the year-end closing entry as part of closing the fiscal year.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="a3e88-108">So buchen Sie den Jahresabschlussposten</span><span class="sxs-lookup"><span data-stu-id="a3e88-108">To post the year end closing entry</span></span>

1. <span data-ttu-id="a3e88-109">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Fibu Buch.-Blatt** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="a3e88-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="a3e88-110">Wählen Sie auf der Seite **Fibu Buch.Blatt** im Feld **Buch.-Blattname** das Buch.-Blatt mit den Abschlussposten aus.</span><span class="sxs-lookup"><span data-stu-id="a3e88-110">On the **General Journal** page, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="a3e88-111">Überprüfen Sie die Posten.</span><span class="sxs-lookup"><span data-stu-id="a3e88-111">Review the entries.</span></span>
4. <span data-ttu-id="a3e88-112">Wählen Sie auf der Registerkarte **Start** die Option Buchen aus, um das Buch.-Blatt zu buchen.</span><span class="sxs-lookup"><span data-stu-id="a3e88-112">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
> <span data-ttu-id="a3e88-113">Wenn ein Fehler erkannt wird, wird eine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a3e88-113">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="a3e88-114">Wurde die Buchung ordnungsgemäß durchgeführt, werden die gebuchten Posten aus dem Buch.-Blatt entfernt.</span><span class="sxs-lookup"><span data-stu-id="a3e88-114">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="a3e88-115">Nachdem die Buchung abgeschlossen ist, wird ein Posten auf jedes GuV-Konto gebucht, sodass der Saldo des Kontos Null ist und das Jahresergebnis in die Bilanz übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="a3e88-115">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="a3e88-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3e88-116">See Also</span></span>

[<span data-ttu-id="a3e88-117">Schließen von Buchhaltungsperioden</span><span class="sxs-lookup"><span data-stu-id="a3e88-117">Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="a3e88-118">Schließen der Bücher</span><span class="sxs-lookup"><span data-stu-id="a3e88-118">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="a3e88-119">GuV-Konten Nullstellung</span><span class="sxs-lookup"><span data-stu-id="a3e88-119">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="a3e88-120">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a3e88-120">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]