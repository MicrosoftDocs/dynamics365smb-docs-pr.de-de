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
ms.date: 04/01/2020
ms.author: solsen
ms.openlocfilehash: c54edd1e907c27aca719898319f69f98c0a0a068
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3195603"
---
# <a name="run-batch-jobs-and-xmlports"></a><span data-ttu-id="d5012-103">Führen Sie Stapeljobs und XMLports aus</span><span class="sxs-lookup"><span data-stu-id="d5012-103">Run Batch Jobs and XMLports</span></span>
<span data-ttu-id="d5012-104">Bei einer Stapelverarbeitung handelt es sich um einen Vorgang, bei dem Daten stapelweise verarbeitet werden, beispielsweise bei der Stapelverarbeitung **Wechselkurs regulieren**.</span><span class="sxs-lookup"><span data-stu-id="d5012-104">A batch job is a routine that processes data in batches, for example the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="d5012-105">Es stehen Stapelverarbeitungen für periodische Buchhaltungsaktivitäten zur Verfügung, beispielsweise zum Abschließen der GuV am Ende eines Geschäftsjahrs.</span><span class="sxs-lookup"><span data-stu-id="d5012-105">There are batch jobs that perform periodic accounting activities, such as closing the income statement at the end of a fiscal year.</span></span> <span data-ttu-id="d5012-106">Viele Stapelverarbeitungen dienen zum Ausführen von Berechnungsaufgaben – beispielsweise zum Berechnen von Zuschlägen, Wechselkursregulierungen oder VK-Preisen.</span><span class="sxs-lookup"><span data-stu-id="d5012-106">Many batch jobs do calculation work, such as calculation of finance charges, exchange rate adjustment, and calculation of unit prices.</span></span>

<span data-ttu-id="d5012-107">Eine Stapelverarbeitung gleicht einem Bericht, die Ergebnisse der Stapelverarbeitung werden jedoch zur direkten Aktualisierung der Informationen verwendet, anstatt diese lediglich auszugeben.</span><span class="sxs-lookup"><span data-stu-id="d5012-107">A batch job is like a report, except the batch job uses the result of its work to update information directly, instead of printing the results.</span></span>

<span data-ttu-id="d5012-108">Sie können planen, wann ein Stapeljob ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5012-108">You can schedule when a batch job runs.</span></span> <span data-ttu-id="d5012-109">Weitere Informationen finden Sie unter [Vorgehensweise: Projektwarteschlangen nutzen, um Aufgaben zu planen](admin-job-queues-schedule-tasks.md)</span><span class="sxs-lookup"><span data-stu-id="d5012-109">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

## <a name="to-run-a-batch-job"></a><span data-ttu-id="d5012-110">So führen Sie eine Stapelverarbeitung aus:</span><span class="sxs-lookup"><span data-stu-id="d5012-110">To run a batch job</span></span>
1. <span data-ttu-id="d5012-111">Um die Anforderungsseite für den entsprechenden Batch-Job zu öffnen, wählen Sie die Seite ![Glühbirne, die das Symbol Tell Me feature](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") öffnet, geben Sie den Namen des Batch-Jobs ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="d5012-111">To open the request page for the relevant batch job, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter the name of the batch job, and then choose the related link.</span></span>
2. <span data-ttu-id="d5012-112">Ist für die Stapelverarbeitung ein Inforegister vom Typ **Optionen** verfügbar, füllen Sie die Felder aus, um die Stapelverarbeitung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d5012-112">If there is an **Options** FastTab for the batch job, fill in the fields to determine what the batch job will do.</span></span>
3. <span data-ttu-id="d5012-113">Die Seite kann mehrere Inforegister mit Filtern enthalten, mit denen sich die in die Stapelverarbeitung einzubeziehenden Daten einschränken lassen.</span><span class="sxs-lookup"><span data-stu-id="d5012-113">The page may contain one or more FastTab with filters, which you can use to limit the data included in the batch job.</span></span> <span data-ttu-id="d5012-114">Sie können Kriterien in die vorgeschlagenen Filter eingeben oder weitere Filter hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d5012-114">You can enter criteria in the suggested filters or add more filters.</span></span>
4. <span data-ttu-id="d5012-115">Klicken Sie auf die Schaltfläche **OK**, um den Batchauftrag zu starten.</span><span class="sxs-lookup"><span data-stu-id="d5012-115">Choose the **OK** button to start the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="d5012-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5012-116">See Also</span></span>
[<span data-ttu-id="d5012-117">Sortieren, Durchsuchen und Filtern von Listen</span><span class="sxs-lookup"><span data-stu-id="d5012-117">Sorting, Searching, and Filtering Lists</span></span>](ui-enter-criteria-filters.md)  
[<span data-ttu-id="d5012-118">Verwenden von Aufgabenwarteschlangen für die Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="d5012-118">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
<span data-ttu-id="d5012-119">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d5012-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
