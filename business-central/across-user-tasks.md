---
title: Zuweisen und Verwalten von Aufgaben | Microsoft Docs
description: Erfahren Sie, wie Benutzern, einschließlich Ihres Buchhalters, Aufgaben in Business Central zugewiesen werden
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: tasks, work
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c76751726f5cd680fafc0887fc57a1464d0ac3ca
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922617"
---
# <a name="define-user-tasks"></a><span data-ttu-id="90feb-103">Benutzeraufgaben definieren</span><span class="sxs-lookup"><span data-stu-id="90feb-103">Define User Tasks</span></span>

<span data-ttu-id="90feb-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)] können Sie Aufgaben erstellen, die Sie an Arbeit erinnern, die durchgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="90feb-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], you can create tasks to remind you of work to be done.</span></span> <span data-ttu-id="90feb-105">Sie können Aufgaben für sich selbst erstellen, aber Sie können auch Aufgaben an Andere zuweisen oder Ihnen kann von jemand anderem in Ihrer Organisation eine Aufgabe zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="90feb-105">You can create tasks for yourself, but you can also assign tasks to others or be assigned a task by someone else in your organization.</span></span>  

## <a name="managing-user-tasks"></a><span data-ttu-id="90feb-106">Benutzeraufgaben verwalten</span><span class="sxs-lookup"><span data-stu-id="90feb-106">Managing User Tasks</span></span>

<span data-ttu-id="90feb-107">Die Seite **Benutzeraufgaben** zeigt alle Aufgaben an, und Sie können einfach neue Aufgaben erstellen und zuweisen.</span><span class="sxs-lookup"><span data-stu-id="90feb-107">The **User Tasks** page shows all tasks, and you can easily create and assign new tasks.</span></span> <span data-ttu-id="90feb-108">Wenn Sie eine Aufgabe erstellen, können Sie das Startdatum und das Fälligkeitsdatum angeben, und Sie können einen Link auf der Seite oder dem Bericht in [!INCLUDE[d365fin](includes/d365fin_md.md)] hinzufügen, wo der Benutzer die Arbeit machen muss.</span><span class="sxs-lookup"><span data-stu-id="90feb-108">When you create a task, you can specify the start date and due date, and you can add a link to the page or report in [!INCLUDE[d365fin](includes/d365fin_md.md)] where the user must do the work.</span></span>  

<span data-ttu-id="90feb-109">Beispielsweise können Sie eine Aufgabe für sich selbst oder einen Mitarbeiter erstellen, sodass alle gebuchten Verkaufsrechnungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="90feb-109">For example, you can create a task for yourself or a coworker to view all posted sales invoices.</span></span> <span data-ttu-id="90feb-110">In diesem Fall können Sie die Aufgabe mit Seite 143, **„Gebuchte Verkaufsrechnungen“** , verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="90feb-110">In that case, you link the task to page 143, **Posted Sales Invoices** .</span></span> <span data-ttu-id="90feb-111">Im folgenden Screenshot erstellt jemand eine Aufgabe für MeganB, um die gebuchten Verkaufsrechnungen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="90feb-111">In the following screenshot, someone is creating a task for MeganB to review the posted sales invoices.</span></span>  

:::image type="content" source="media/across-user-tasks/sample-user-task.png" alt-text="Beispiel für eine Benutzeraufgabe":::

> [!TIP]  
> <span data-ttu-id="90feb-113">Verwenden Sie die Suche im Feld **Seite** , und verwenden Sie dann das Feld **Suche** , um die Seite zu finden, die Sie anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="90feb-113">Use the look-up in the **Page** field and then use the **Search** field to find the page that you want.</span></span>  
>
> <span data-ttu-id="90feb-114">Sie können auf jede Seite verlinken, aber nicht auf einzelne Einträge. Machen Sie die Beschreibung daher so explizit wie möglich, z. B. „Bitte werfen Sie einen Blick auf Kunden-Nr.</span><span class="sxs-lookup"><span data-stu-id="90feb-114">You can link to any page, but you cannot link to individual entries, so make the description as explicit as possible, such as writing "Please take a look at customer no.</span></span> <span data-ttu-id="90feb-115">10000 und stellen Sie sicher, dass keine überfälligen Zahlungen vorliegen.“</span><span class="sxs-lookup"><span data-stu-id="90feb-115">10000 and make sure they don't have overdue payments.".</span></span>

### <a name="picking-up-user-tasks"></a><span data-ttu-id="90feb-116">Benutzeraufgaben aufnehmen</span><span class="sxs-lookup"><span data-stu-id="90feb-116">Picking Up User Tasks</span></span>

<span data-ttu-id="90feb-117">In den Rollencentern Geschäftsführer, Bookkeeper und Buchhalter zeigt eine Kachel ausstehende Aufgaben an, die diesem Benutzer zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="90feb-117">In the Business Manager, Bookkeeper, and Accountant Role Centers, a tile shows pending tasks that are assigned to that user.</span></span> <span data-ttu-id="90feb-118">Um eine Aufgabe aufzunehmen, wählen Sie sie einfach aus der Liste der ausstehenden Benutzeraufgaben aus.</span><span class="sxs-lookup"><span data-stu-id="90feb-118">To pick up a task, simply choose it from the list of pending user tasks.</span></span> <span data-ttu-id="90feb-119">Im Menüband öffnet der Link **Zu Aufgabenelement wechseln** die Seite, in dem Sie die Arbeit ausführen können.</span><span class="sxs-lookup"><span data-stu-id="90feb-119">In the ribbon, the link **Go to Task Item** opens the page where you can do the work.</span></span>  

<span data-ttu-id="90feb-120">Wenn Sie eine Aufgabe abgeschlossen haben, kennzeichnen Sie sie einfach als abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="90feb-120">When you have completed a task, simply mark it as completed.</span></span>  

### <a name="deleting-user-tasks"></a><span data-ttu-id="90feb-121">Benutzeraufgaben löschen</span><span class="sxs-lookup"><span data-stu-id="90feb-121">Deleting User Tasks</span></span>

<span data-ttu-id="90feb-122">Wenn Sie eine Massenlöschung aller oder einiger Benutzeraufgaben vornehmen möchten, können Sie den Bericht **Benutzeraufgaben** löschen verwenden.</span><span class="sxs-lookup"><span data-stu-id="90feb-122">If you want to bulk delete all or some user tasks, you can use the **Delete User Tasks** report.</span></span> <span data-ttu-id="90feb-123">Auf der Anforderungsseite können Sie Filter festlegen, um zu bestimmen, welche Aufgaben gelöscht werden müssen.</span><span class="sxs-lookup"><span data-stu-id="90feb-123">In the request page, you can set filters to determine which tasks must be deleted.</span></span>  

## <a name="see-also"></a><span data-ttu-id="90feb-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90feb-124">See Also</span></span>

[<span data-ttu-id="90feb-125">Nach einer Seite oder einem Bericht suchen</span><span class="sxs-lookup"><span data-stu-id="90feb-125">Searching for a Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="90feb-126">[Buchhalter-Erfahrung in [!INCLUDE[d365fin](includes/d365fin_md.md)]](finance-accounting.md)</span><span class="sxs-lookup"><span data-stu-id="90feb-126">[Accountant Experiences in [!INCLUDE[d365fin](includes/d365fin_md.md)]](finance-accounting.md)</span></span>  
