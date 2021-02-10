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
ms.date: 10/01/2020
ms.author: solsen
ms.openlocfilehash: 04ae13561f44d544d38b04e3a881a0e707b441b4
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760517"
---
# <a name="run-batch-jobs-and-xmlports"></a><span data-ttu-id="eaeaa-103">Führen Sie Stapeljobs und XMLports aus</span><span class="sxs-lookup"><span data-stu-id="eaeaa-103">Run Batch Jobs and XMLports</span></span>
<span data-ttu-id="eaeaa-104">Bei einer Stapelverarbeitung handelt es sich um einen Vorgang, bei dem Daten stapelweise verarbeitet werden, beispielsweise bei der Stapelverarbeitung **Wechselkurs regulieren**.</span><span class="sxs-lookup"><span data-stu-id="eaeaa-104">A batch job is a routine that processes data in batches, for example the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="eaeaa-105">Es stehen Stapelverarbeitungen für periodische Buchhaltungsaktivitäten zur Verfügung, beispielsweise zum Abschließen der GuV am Ende eines Geschäftsjahrs.</span><span class="sxs-lookup"><span data-stu-id="eaeaa-105">There are batch jobs that perform periodic accounting activities, such as closing the income statement at the end of a fiscal year.</span></span> <span data-ttu-id="eaeaa-106">Viele Stapelverarbeitungen dienen zum Ausführen von Berechnungsaufgaben – beispielsweise zum Berechnen von Zuschlägen, Wechselkursregulierungen oder VK-Preisen.</span><span class="sxs-lookup"><span data-stu-id="eaeaa-106">Many batch jobs do calculation work, such as calculation of finance charges, exchange rate adjustment, and calculation of unit prices.</span></span>

<span data-ttu-id="eaeaa-107">Eine Stapelverarbeitung gleicht einem Bericht, die Ergebnisse der Stapelverarbeitung werden jedoch zur direkten Aktualisierung der Informationen verwendet, anstatt diese lediglich auszugeben.</span><span class="sxs-lookup"><span data-stu-id="eaeaa-107">A batch job is like a report, except the batch job uses the result of its work to update information directly, instead of printing the results.</span></span>

<span data-ttu-id="eaeaa-108">Sie können planen, wann ein Stapeljob ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eaeaa-108">You can schedule when a batch job runs.</span></span> <span data-ttu-id="eaeaa-109">Weitere Informationen finden Sie unter [Vorgehensweise: Projektwarteschlangen nutzen, um Aufgaben zu planen](admin-job-queues-schedule-tasks.md)</span><span class="sxs-lookup"><span data-stu-id="eaeaa-109">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

## <a name="to-run-a-batch-job"></a><span data-ttu-id="eaeaa-110">So führen Sie eine Stapelverarbeitung aus:</span><span class="sxs-lookup"><span data-stu-id="eaeaa-110">To run a batch job</span></span>
1. <span data-ttu-id="eaeaa-111">Um die Anforderungsseite für den entsprechenden Batch-Job zu öffnen, wählen Sie die Seite ![Glühbirne, die das Symbol Tell Me feature](media/ui-search/search_small.png "Was möchten Sie tun?") öffnet, geben Sie den Namen des Batch-Jobs ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="eaeaa-111">To open the request page for the relevant batch job, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter the name of the batch job, and then choose the related link.</span></span>
2. <span data-ttu-id="eaeaa-112">Ist für die Stapelverarbeitung ein Inforegister vom Typ **Optionen** verfügbar, füllen Sie die Felder aus, um die Stapelverarbeitung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="eaeaa-112">If there is an **Options** FastTab for the batch job, fill in the fields to determine what the batch job will do.</span></span>
3. <span data-ttu-id="eaeaa-113">Die Seite kann mehrere Inforegister mit Filtern enthalten, mit denen sich die in die Stapelverarbeitung einzubeziehenden Daten einschränken lassen.</span><span class="sxs-lookup"><span data-stu-id="eaeaa-113">The page may contain one or more FastTab with filters, which you can use to limit the data included in the batch job.</span></span> <span data-ttu-id="eaeaa-114">Sie können Kriterien in die vorgeschlagenen Filter eingeben oder weitere Filter hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="eaeaa-114">You can enter criteria in the suggested filters or add more filters.</span></span>
4. <span data-ttu-id="eaeaa-115">Klicken Sie auf die Schaltfläche **OK**, um den Batchauftrag zu starten.</span><span class="sxs-lookup"><span data-stu-id="eaeaa-115">Choose the **OK** button to start the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="eaeaa-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eaeaa-116">See Also</span></span>
[<span data-ttu-id="eaeaa-117">Sortieren, Durchsuchen und Filtern von Listen</span><span class="sxs-lookup"><span data-stu-id="eaeaa-117">Sorting, Searching, and Filtering Lists</span></span>](ui-enter-criteria-filters.md)  
[<span data-ttu-id="eaeaa-118">Verwenden von Aufgabenwarteschlangen für die Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="eaeaa-118">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
<span data-ttu-id="eaeaa-119">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="eaeaa-119">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
