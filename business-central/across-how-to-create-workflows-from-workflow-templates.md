---
title: 'Vorgehensweise: Workflows von Workflowvorlagen erstellen | Microsoft Docs'
description: Um Zeit zu sparen, wenn Sie neue Workflows erstellen, können Sie Workflows aus Workflowvorlagen erstellen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: c5e3f26e45a4c990a3614011e21fe8d661973035
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3784734"
---
# <a name="create-workflows-from-workflow-templates"></a><span data-ttu-id="2e30d-103">Erstellen von Workflows aus Workflowvorlagen</span><span class="sxs-lookup"><span data-stu-id="2e30d-103">Create Workflows from Workflow Templates</span></span>
<span data-ttu-id="2e30d-104">Um Zeit zu sparen, wenn Sie neue Workflows erstellen, können Sie Workflows aus Workflowvorlagen erstellen.</span><span class="sxs-lookup"><span data-stu-id="2e30d-104">To save time when creating new workflows, you can create workflows from workflow templates.</span></span>  

 <span data-ttu-id="2e30d-105">Workflowvorlagen sind nicht-bearbeitbare Workflows, die Sie in der generischen Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] finden.</span><span class="sxs-lookup"><span data-stu-id="2e30d-105">Workflow templates are non-editable workflows that exist in the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="2e30d-106">Dem Code für von Microsoft hinzugefügte Workflowvorlagen ist „MS-“ vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="2e30d-106">The codes for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span>  

 <span data-ttu-id="2e30d-107">Eine andere Art, einen Workflow schnell zu erstellen ist es, einen vorhandenen Workflow zu importieren, den Sie in einer Datei außerhalb von [!INCLUDE[d365fin](includes/d365fin_md.md)] haben.</span><span class="sxs-lookup"><span data-stu-id="2e30d-107">Another way to quickly create a workflow is to import an existing workflow that you have on a file outside of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="2e30d-108">Weitere Informationen finden Sie in [Exportieren und Importieren von Workflows](across-how-to-export-and-import-workflows.md)</span><span class="sxs-lookup"><span data-stu-id="2e30d-108">For more information, see [Export and Import Workflows](across-how-to-export-and-import-workflows.md).</span></span>  

<span data-ttu-id="2e30d-109">Auf der Seite **Workflow** können Sie einen Workflow erstellen, indem Sie die entsprechenden Schritte in den Zeilen auflisten.</span><span class="sxs-lookup"><span data-stu-id="2e30d-109">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="2e30d-110">Jeder Schritt besteht aus einem durch Ereignisbedingungen moderiertem Workflowereignis und einer durch Antwortoptionen moderierten Workflowantwort.</span><span class="sxs-lookup"><span data-stu-id="2e30d-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="2e30d-111">Sie definieren Workflowschritte, indem Sie die Felder in Workflowzeilen mit Ereignis- und Antwortwerten aus festen Listen ausfüllen, die die Workflowszenarien darstellen, die durch den Anwendungscode unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="2e30d-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="2e30d-112">Weitere Informationen finden Sie unter [Workflows erstellen](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="2e30d-112">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-create-a-workflow-from-workflow-template"></a><span data-ttu-id="2e30d-113">Vorgehensweise: Workflows von Workflowvorlagen erstellen</span><span class="sxs-lookup"><span data-stu-id="2e30d-113">To create a workflow from workflow template</span></span>  
1.  <span data-ttu-id="2e30d-114">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Workflows** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="2e30d-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2e30d-115">Wählen Sie die Aktion **Workflow von Vorlage erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="2e30d-115">Choose the **Create Workflow from Template** action.</span></span> <span data-ttu-id="2e30d-116">Die Seite **Workflowvorlagen** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="2e30d-116">The **Workflow Templates** page opens.</span></span>  
3.  <span data-ttu-id="2e30d-117">Wählen Sie eine Workflowvorlage aus, und wählen Sie dann die Schaltfläche **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e30d-117">Select a workflow template, and then choose the **OK** button.</span></span>  

     <span data-ttu-id="2e30d-118">Die Seite **Workflow** wird für einen neuen Workflow geöffnet, der alle Informationen der ausgewählten Vorlage enthält.</span><span class="sxs-lookup"><span data-stu-id="2e30d-118">The **Workflow** page opens for a new workflow containing all the information of the selected template.</span></span> <span data-ttu-id="2e30d-119">Der Wert im Feld **Code** wird beispielweise mit "-01 " erweitert. Dies zeigt an, dass dies der erste Workflow ist, der von der Workflowvorlage erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="2e30d-119">The value in the **Code** field is extended with, for example, “-01” to indicate that this is the first workflow that is created from the workflow template.</span></span>  
4.  <span data-ttu-id="2e30d-120">Fahren Sie fort mit dem Erstellen des Workflows, indem Sie die Workflowschritte bearbeiten oder neue Schritte hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2e30d-120">Proceed to create the workflow by editing the workflow steps or add new steps.</span></span> <span data-ttu-id="2e30d-121">Weitere Informationen finden Sie unter [Workflows erstellen](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="2e30d-121">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="2e30d-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e30d-122">See Also</span></span>  
 <span data-ttu-id="2e30d-123">[Erstellen eines Workflows](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="2e30d-123">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="2e30d-124">[Exportieren und Importieren von Workflows](across-how-to-export-and-import-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="2e30d-124">[Export and Import Workflows](across-how-to-export-and-import-workflows.md) </span></span>  
 <span data-ttu-id="2e30d-125">[Anzeigen von archivierten Workflowschritt-Instanzen](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="2e30d-125">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="2e30d-126">[Löschen eines Workflows](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="2e30d-126">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="2e30d-127">[Exemplarische Vorgehensweise: Einrichten und Nutzen eines Einkaufsgenehmigungsworkflows](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="2e30d-127">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="2e30d-128">[Einrichten von Workflows](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="2e30d-128">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="2e30d-129">[Verwenden von Workflows](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="2e30d-129">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="2e30d-130">Workflow</span><span class="sxs-lookup"><span data-stu-id="2e30d-130">Workflow</span></span>](across-workflow.md)   
