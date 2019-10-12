---
title: Löschen von Workflows | Microsoft Docs
description: Wenn Sie sicher sind, dass ein Workflow nicht mehr verwendet wird, können Sie ihn löschen. Alle Workflowschrittinstanzen, die im Workflow definiert wurden, müssen den Status **Abgeschlossen** haben.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0cdec04115ebfe089ee89cdc5db8cf28e3963eb8
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305428"
---
# <a name="delete-workflows"></a><span data-ttu-id="55a90-104">Löschen eines Workflows</span><span class="sxs-lookup"><span data-stu-id="55a90-104">Delete Workflows</span></span>
<span data-ttu-id="55a90-105">Wenn Sie sicher sind, dass ein Workflow nicht mehr verwendet wird, können Sie ihn löschen.</span><span class="sxs-lookup"><span data-stu-id="55a90-105">If you are certain that a workflow is no longer being used, you can delete it.</span></span> <span data-ttu-id="55a90-106">Alle Workflowschrittinstanzen, die im Workflow definiert wurden, müssen den Status **Abgeschlossen** haben.</span><span class="sxs-lookup"><span data-stu-id="55a90-106">All workflow step instances that are defined in the workflow must have status **Completed**.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="55a90-107">Wenn Sie einen Workflow löschen, gehen alle Informationen im Workflow verloren.</span><span class="sxs-lookup"><span data-stu-id="55a90-107">When you delete a workflow, all information in the workflow will be lost.</span></span>  

 <span data-ttu-id="55a90-108">Auf der Seite **Workflow** können Sie einen Workflow erstellen, indem Sie die entsprechenden Schritte in den Zeilen auflisten.</span><span class="sxs-lookup"><span data-stu-id="55a90-108">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="55a90-109">Jeder Schritt besteht aus einem durch Ereignisbedingungen moderiertem Workflowereignis und einer durch Antwortoptionen moderierten Workflowantwort.</span><span class="sxs-lookup"><span data-stu-id="55a90-109">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="55a90-110">Sie definieren Workflowschritte, indem Sie die Felder in Workflowzeilen mit Ereignis- und Antwortwerten aus festen Listen ausfüllen, die die Workflowszenarien darstellen, die durch den Anwendungscode unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="55a90-110">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="55a90-111">Weitere Informationen finden Sie unter [Workflows erstellen](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="55a90-111">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-delete-a-workflow"></a><span data-ttu-id="55a90-112">So löschen Sie einen Workflow</span><span class="sxs-lookup"><span data-stu-id="55a90-112">To delete a workflow</span></span>  
1.  <span data-ttu-id="55a90-113">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Workflows** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="55a90-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="55a90-114">Wählen Sie den zu löschenden Workflow aus.</span><span class="sxs-lookup"><span data-stu-id="55a90-114">Select the workflow that you want to delete.</span></span>  
3.  <span data-ttu-id="55a90-115">Wählen Sie die Aktion **Löschen** aus.</span><span class="sxs-lookup"><span data-stu-id="55a90-115">Choose the **Delete** action.</span></span>  
4.  <span data-ttu-id="55a90-116">Öffnen Sie alternativ den Workflow, den Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="55a90-116">Alternatively, open the workflow that you want to delete.</span></span>  
5.  <span data-ttu-id="55a90-117">Wählen Sie im Fenster **Workflow** die Aktion **Löschen** aus.</span><span class="sxs-lookup"><span data-stu-id="55a90-117">On the **Workflow** page, choose the **Delete** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="55a90-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55a90-118">See Also</span></span>  
 <span data-ttu-id="55a90-119">[Erstellen eines Workflows](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="55a90-119">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="55a90-120">[Aktivieren von Workflows](across-how-to-enable-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="55a90-120">[Enable Workflows](across-how-to-enable-workflows.md) </span></span>  
 <span data-ttu-id="55a90-121">[Anzeigen von archivierten Workflowschritt-Instanzen](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="55a90-121">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="55a90-122">[Exemplarische Vorgehensweise: Einrichten und Nutzen eines Einkaufsanfrage-Genehmigungsworkflows](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="55a90-122">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="55a90-123">[Einrichten von Workflows](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="55a90-123">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="55a90-124">[Verwenden von Workflows](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="55a90-124">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="55a90-125">Workflow</span><span class="sxs-lookup"><span data-stu-id="55a90-125">Workflow</span></span>](across-workflow.md)   
