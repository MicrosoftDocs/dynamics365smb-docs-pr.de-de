---
title: Löschen von Workflows | Microsoft Docs
description: Wenn Sie sicher sind, dass ein Workflow nicht mehr verwendet wird, können Sie ihn löschen. Alle Workflowschrittinstanzen, die im Workflow definiert wurden, müssen den Status **Abgeschlossen** haben.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e554b3118dbbef0f1235b27da5707b2d0bbd092f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775797"
---
# <a name="delete-workflows"></a><span data-ttu-id="a1403-104">Löschen eines Workflows</span><span class="sxs-lookup"><span data-stu-id="a1403-104">Delete Workflows</span></span>
<span data-ttu-id="a1403-105">Wenn Sie sicher sind, dass ein Workflow nicht mehr verwendet wird, können Sie ihn löschen.</span><span class="sxs-lookup"><span data-stu-id="a1403-105">If you are certain that a workflow is no longer being used, you can delete it.</span></span> <span data-ttu-id="a1403-106">Alle Workflowschrittinstanzen, die im Workflow definiert wurden, müssen den Status **Abgeschlossen** haben.</span><span class="sxs-lookup"><span data-stu-id="a1403-106">All workflow step instances that are defined in the workflow must have status **Completed**.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="a1403-107">Wenn Sie einen Workflow löschen, gehen alle Informationen im Workflow verloren.</span><span class="sxs-lookup"><span data-stu-id="a1403-107">When you delete a workflow, all information in the workflow will be lost.</span></span>  

 <span data-ttu-id="a1403-108">Auf der Seite **Workflow** können Sie einen Workflow erstellen, indem Sie die entsprechenden Schritte in den Zeilen auflisten.</span><span class="sxs-lookup"><span data-stu-id="a1403-108">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="a1403-109">Jeder Schritt besteht aus einem durch Ereignisbedingungen moderiertem Workflowereignis und einer durch Antwortoptionen moderierten Workflowantwort.</span><span class="sxs-lookup"><span data-stu-id="a1403-109">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="a1403-110">Sie definieren Workflowschritte, indem Sie die Felder in Workflowzeilen mit Ereignis- und Antwortwerten aus festen Listen ausfüllen, die die Workflowszenarien darstellen, die durch den Anwendungscode unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a1403-110">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="a1403-111">Weitere Informationen finden Sie unter [Workflows erstellen](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="a1403-111">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-delete-a-workflow"></a><span data-ttu-id="a1403-112">So löschen Sie einen Workflow</span><span class="sxs-lookup"><span data-stu-id="a1403-112">To delete a workflow</span></span>  
1.  <span data-ttu-id="a1403-113">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Workflows** ein und wählen Sie dann den zugehörigen Link.</span><span class="sxs-lookup"><span data-stu-id="a1403-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a1403-114">Wählen Sie den zu löschenden Workflow aus.</span><span class="sxs-lookup"><span data-stu-id="a1403-114">Select the workflow that you want to delete.</span></span>  
3.  <span data-ttu-id="a1403-115">Wählen Sie die Aktion **Löschen** aus.</span><span class="sxs-lookup"><span data-stu-id="a1403-115">Choose the **Delete** action.</span></span>  
4.  <span data-ttu-id="a1403-116">Öffnen Sie alternativ den Workflow, den Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="a1403-116">Alternatively, open the workflow that you want to delete.</span></span>  
5.  <span data-ttu-id="a1403-117">Wählen Sie im Fenster **Workflow** die Aktion **Löschen** aus.</span><span class="sxs-lookup"><span data-stu-id="a1403-117">On the **Workflow** page, choose the **Delete** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a1403-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1403-118">See Also</span></span>  
 <span data-ttu-id="a1403-119">[Erstellen eines Workflows](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="a1403-119">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="a1403-120">[Aktivieren von Workflows](across-how-to-enable-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="a1403-120">[Enable Workflows](across-how-to-enable-workflows.md) </span></span>  
 <span data-ttu-id="a1403-121">[Anzeigen von archivierten Workflowschritt-Instanzen](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="a1403-121">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="a1403-122">[Exemplarische Vorgehensweise: Einrichten und Nutzen eines Einkaufsgenehmigungsworkflows](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="a1403-122">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="a1403-123">[Einrichten von Workflows](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="a1403-123">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="a1403-124">[Verwenden von Workflows](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="a1403-124">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="a1403-125">Workflow</span><span class="sxs-lookup"><span data-stu-id="a1403-125">Workflow</span></span>](across-workflow.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]