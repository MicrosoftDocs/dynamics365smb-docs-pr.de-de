---
title: Erstellen und führen Sie eine Stapelverarbeitung | Microsoft Docs
description: Sie führen Stapelverarbeitungen durch , um Daten zu verarbeiten und Informationen zu aktualisieren, um periodische Buchhaltungsaktivitäten oder Berechnungen durchzuführen.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 10/01/2019
ms.author: solsen
ms.openlocfilehash: 2387356fd3e80e5020b4d2e4857280dd4b99788a
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315204"
---
# <a name="run-batch-jobs-and-xmlports"></a><span data-ttu-id="b1f64-103">Führen Sie Stapeljobs und XMLports aus</span><span class="sxs-lookup"><span data-stu-id="b1f64-103">Run Batch Jobs and XMLports</span></span>
<span data-ttu-id="b1f64-104">Bei einer Stapelverarbeitung handelt es sich um einen Vorgang, bei dem Daten stapelweise verarbeitet werden, beispielsweise bei der Stapelverarbeitung **Wechselkurs regulieren**.</span><span class="sxs-lookup"><span data-stu-id="b1f64-104">A batch job is a routine that processes data in batches, for example the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="b1f64-105">Es stehen Stapelverarbeitungen für periodische Buchhaltungsaktivitäten zur Verfügung, beispielsweise zum Abschließen der GuV am Ende eines Geschäftsjahrs.</span><span class="sxs-lookup"><span data-stu-id="b1f64-105">There are batch jobs that perform periodic accounting activities, such as closing the income statement at the end of a fiscal year.</span></span> <span data-ttu-id="b1f64-106">Viele Stapelverarbeitungen dienen zum Ausführen von Berechnungsaufgaben – beispielsweise zum Berechnen von Zuschlägen, Wechselkursregulierungen oder VK-Preisen.</span><span class="sxs-lookup"><span data-stu-id="b1f64-106">Many batch jobs do calculation work, such as calculation of finance charges, exchange rate adjustment, and calculation of unit prices.</span></span>

<span data-ttu-id="b1f64-107">Eine Stapelverarbeitung gleicht einem Bericht, die Ergebnisse der Stapelverarbeitung werden jedoch zur direkten Aktualisierung der Informationen verwendet, anstatt diese lediglich auszugeben.</span><span class="sxs-lookup"><span data-stu-id="b1f64-107">A batch job is like a report, except the batch job uses the result of its work to update information directly, instead of printing the results.</span></span>

<span data-ttu-id="b1f64-108">Sie können planen, wann ein Stapeljob ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1f64-108">You can schedule when a batch job runs.</span></span> <span data-ttu-id="b1f64-109">Weitere Informationen finden Sie unter [Vorgehensweise: Projektwarteschlangen nutzen, um Aufgaben zu planen](admin-job-queues-schedule-tasks.md)</span><span class="sxs-lookup"><span data-stu-id="b1f64-109">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

## <a name="to-run-a-batch-job"></a><span data-ttu-id="b1f64-110">So führen Sie eine Stapelverarbeitung aus:</span><span class="sxs-lookup"><span data-stu-id="b1f64-110">To run a batch job</span></span>
1. <span data-ttu-id="b1f64-111">Zum Öffnen der Anforderungsseite für die relevanten Stapelverarbeitung wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie den Namen der Stapelverarbeitung ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="b1f64-111">To open the request page for the relevant batch job, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter the name of the batch job, and then choose the related link.</span></span>
2. <span data-ttu-id="b1f64-112">Ist für die Stapelverarbeitung ein Inforegister vom Typ **Optionen** verfügbar, füllen Sie die Felder aus, um die Stapelverarbeitung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b1f64-112">If there is an **Options** FastTab for the batch job, fill in the fields to determine what the batch job will do.</span></span>
3. <span data-ttu-id="b1f64-113">Die Seite kann mehrere Inforegister mit Filtern enthalten, mit denen sich die in die Stapelverarbeitung einzubeziehenden Daten einschränken lassen.</span><span class="sxs-lookup"><span data-stu-id="b1f64-113">The page may contain one or more FastTab with filters, which you can use to limit the data included in the batch job.</span></span> <span data-ttu-id="b1f64-114">Sie können Kriterien in die vorgeschlagenen Filter eingeben oder weitere Filter hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b1f64-114">You can enter criteria in the suggested filters or add more filters.</span></span>
4. <span data-ttu-id="b1f64-115">Klicken Sie auf die Schaltfläche **OK**, um den Batchauftrag zu starten.</span><span class="sxs-lookup"><span data-stu-id="b1f64-115">Choose the **OK** button to start the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="b1f64-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1f64-116">See Also</span></span>
[<span data-ttu-id="b1f64-117">Sortieren, Durchsuchen und Filtern von Listen</span><span class="sxs-lookup"><span data-stu-id="b1f64-117">Sorting, Searching, and Filtering Lists</span></span>](ui-enter-criteria-filters.md)  
[<span data-ttu-id="b1f64-118">Verwenden von Aufgabenwarteschlangen für die Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="b1f64-118">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
<span data-ttu-id="b1f64-119">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b1f64-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
