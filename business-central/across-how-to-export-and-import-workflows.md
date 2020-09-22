---
title: 'Vorgehensweise: Exportieren und Importieren von Workflows | Microsoft Docs'
description: Um Workflows auf andere Business Central-Datenbanken zu übertragen, beispielsweise um Zeit zu sparen, wenn Sie neue Workflows erstellen, können Workflows exportiert und importiert werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: e38ffe59525ca1ef8c124028365bbb597a54a350
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3785146"
---
# <a name="export-and-import-workflows"></a><span data-ttu-id="b7d14-103">Exportieren und Importieren von Workflows</span><span class="sxs-lookup"><span data-stu-id="b7d14-103">Export and Import Workflows</span></span>
<span data-ttu-id="b7d14-104">Um Workflows auf andere [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datenbanken zu übertragen, beispielsweise um Zeit zu sparen, wenn Sie neue Workflows erstellen, können Workflows exportiert und importiert werden.</span><span class="sxs-lookup"><span data-stu-id="b7d14-104">To transfer workflows to other [!INCLUDE[d365fin](includes/d365fin_md.md)] databases, for example to save time when creating new workflows, you can export and import workflows.</span></span>  

 <span data-ttu-id="b7d14-105">Eine andere Art, Workflows schnell zu erstellen, besteht darin, Workflows aus Workflow-Vorlagen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b7d14-105">Another way to quickly create workflows is to create workflows from workflow templates.</span></span> <span data-ttu-id="b7d14-106">Weitere Informationen finden Sie unter [Workflows von Workflow-Vorlagen erstellen](across-how-to-create-workflows-from-workflow-templates.md).</span><span class="sxs-lookup"><span data-stu-id="b7d14-106">For more information, see [Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md).</span></span>  

 <span data-ttu-id="b7d14-107">Auf der Seite **Workflow** können Sie einen Workflow erstellen, indem Sie die entsprechenden Schritte in den Zeilen auflisten.</span><span class="sxs-lookup"><span data-stu-id="b7d14-107">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="b7d14-108">Jeder Schritt besteht aus einem durch Ereignisbedingungen moderiertem Workflowereignis und einer durch Antwortoptionen moderierten Workflowantwort.</span><span class="sxs-lookup"><span data-stu-id="b7d14-108">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="b7d14-109">Sie definieren Workflowschritte, indem Sie die Felder in Workflowzeilen mit Ereignis- und Antwortwerten aus festen Listen ausfüllen, die die Workflowszenarien darstellen, die durch den Anwendungscode unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b7d14-109">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="b7d14-110">Weitere Informationen finden Sie unter [Workflows erstellen](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="b7d14-110">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-export-a-workflow"></a><span data-ttu-id="b7d14-111">So exportieren Sie ein Workflow</span><span class="sxs-lookup"><span data-stu-id="b7d14-111">To export a workflow</span></span>  
1.  <span data-ttu-id="b7d14-112">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Workflows** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="b7d14-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b7d14-113">Wählen Sie einen Workflow, und wählen die **In Datei exportieren** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="b7d14-113">Select a workflow, and then choose the **Export to File** action.</span></span>  
3.  <span data-ttu-id="b7d14-114">Klicken Sie auf der Seite **Datei exportieren** auf die Schaltfläche **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="b7d14-114">On the **Export File** page, choose the **Save** button.</span></span>  
4.  <span data-ttu-id="b7d14-115">Wählen Sie auf der Seite **Exportieren** einen Dateistandort aus, und wählen Sie dann die Schaltfläche **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="b7d14-115">On the **Export** page, select a file location, and then choose the **Save** button.</span></span>  

## <a name="to-import-a-workflow"></a><span data-ttu-id="b7d14-116">So importieren Sie einen Workflow</span><span class="sxs-lookup"><span data-stu-id="b7d14-116">To import a workflow</span></span>  
1.  <span data-ttu-id="b7d14-117">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Workflows** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="b7d14-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b7d14-118">Wählen Sie die Aktion **Importieren aus Datei** aus.</span><span class="sxs-lookup"><span data-stu-id="b7d14-118">Choose the **Import from File** action.</span></span>  
3.  <span data-ttu-id="b7d14-119">Wählen Sie auf der Seite **Importieren** die XML-Datei aus, die den Workflow enthält, und wählen Sie dann die Schaltfläche **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="b7d14-119">On the **Import** page, choose the XML file that contains the workflow, and then choose the **Open** button.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="b7d14-120">Wenn der Workflowcode bereits in der Datenbank vorhanden ist, werden die Workflowschritte mit den Schritten im importierten Workflow überschrieben.</span><span class="sxs-lookup"><span data-stu-id="b7d14-120">If the workflow code already exists in the database, the workflow steps will be overwritten with the steps in the imported workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b7d14-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7d14-121">See Also</span></span>  
 <span data-ttu-id="b7d14-122">[Erstellen eines Workflows](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="b7d14-122">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="b7d14-123">[Erstellen von Workflows aus Workflowvorlagen](across-how-to-create-workflows-from-workflow-templates.md) </span><span class="sxs-lookup"><span data-stu-id="b7d14-123">[Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md) </span></span>  
 <span data-ttu-id="b7d14-124">[Anzeigen von archivierten Workflowschritt-Instanzen](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="b7d14-124">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="b7d14-125">[Löschen eines Workflows](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="b7d14-125">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="b7d14-126">[Exemplarische Vorgehensweise: Einrichten und Nutzen eines Einkaufsgenehmigungsworkflows](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="b7d14-126">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="b7d14-127">[Einrichten von Workflows](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="b7d14-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="b7d14-128">[Verwenden von Workflows](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="b7d14-128">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="b7d14-129">Workflow</span><span class="sxs-lookup"><span data-stu-id="b7d14-129">Workflow</span></span>](across-workflow.md)   
