---
title: 'Vorgehensweise: Exportieren und Importieren von Workflows | Microsoft Docs'
description: "Um Workflows auf andere Dynamics 365-Datenbanken zu übertragen, beispielsweise um Zeit zu sparen, wenn Sie neue Workflows erstellen, können Workflows exportiert und importiert werden."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 520c81b9c550b4ef29b077685541a2e7ea30d4d7
ms.contentlocale: de-de
ms.lasthandoff: 12/14/2017

---
# <a name="how-to-export-and-import-workflows"></a><span data-ttu-id="1fb1b-103">Vorgehensweise: Exportieren und Importieren von Workflows</span><span class="sxs-lookup"><span data-stu-id="1fb1b-103">How to: Export and Import Workflows</span></span>
<span data-ttu-id="1fb1b-104">Um Workflows auf andere [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datenbanken zu übertragen, beispielsweise um Zeit zu sparen, wenn Sie neue Workflows erstellen, können Workflows exportiert und importiert werden.</span><span class="sxs-lookup"><span data-stu-id="1fb1b-104">To transfer workflows to other [!INCLUDE[d365fin](includes/d365fin_md.md)] databases, for example to save time when creating new workflows, you can export and import workflows.</span></span>  

 <span data-ttu-id="1fb1b-105">Eine andere Art, Workflows schnell zu erstellen, besteht darin, Workflows aus Workflow-Vorlagen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1fb1b-105">Another way to quickly create workflows is to create workflows from workflow templates.</span></span> <span data-ttu-id="1fb1b-106">Weitere Informationen finden Sie unter [Gewusst wie: Workflows von Workflow-Vorlagen erstellen](across-how-to-create-workflows-from-workflow-templates.md).</span><span class="sxs-lookup"><span data-stu-id="1fb1b-106">For more information, see [How to: Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md).</span></span>  

 <span data-ttu-id="1fb1b-107">Im Fenster **Workflow** können Sie einen Workflow erstellen, indem Sie die entsprechenden Schritte in den Zeilen auflisten.</span><span class="sxs-lookup"><span data-stu-id="1fb1b-107">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="1fb1b-108">Jeder Schritt besteht aus einem durch Ereignisbedingungen moderiertem Workflowereignis und einer durch Antwortoptionen moderierten Workflowantwort.</span><span class="sxs-lookup"><span data-stu-id="1fb1b-108">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="1fb1b-109">Sie definieren Workflowschritte, indem Sie die Felder in Workflowzeilen mit Ereignis- und Antwortwerten aus festen Listen ausfüllen, die die Workflowszenarien darstellen, die durch den Anwendungscode unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="1fb1b-109">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="1fb1b-110">Weitere Informationen finden Sie unter [Gewusst wie: Workflows erstellen](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="1fb1b-110">For more information, see [How to: Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-export-a-workflow"></a><span data-ttu-id="1fb1b-111">So exportieren Sie ein Workflow</span><span class="sxs-lookup"><span data-stu-id="1fb1b-111">To export a workflow</span></span>  
1.  <span data-ttu-id="1fb1b-112">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Workflows** ein und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="1fb1b-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1fb1b-113">Wählen Sie einen Workflow, und wählen die **In Datei exportieren** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="1fb1b-113">Select a workflow, and then choose the **Export to File** action.</span></span>  
3.  <span data-ttu-id="1fb1b-114">Klicken Sie im Fenster **Datei exportieren** auf die Schaltfläche **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="1fb1b-114">In the **Export File** window, choose the **Save** button.</span></span>  
4.  <span data-ttu-id="1fb1b-115">Wählen Sie im Fenster **Exportieren** einen Dateistandort aus, und wählen Sie dann die Schaltfläche **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="1fb1b-115">In the **Export** window, select a file location, and then choose the **Save** button.</span></span>  

## <a name="to-import-a-workflow"></a><span data-ttu-id="1fb1b-116">So importieren Sie einen Workflow</span><span class="sxs-lookup"><span data-stu-id="1fb1b-116">To import a workflow</span></span>  
1.  <span data-ttu-id="1fb1b-117">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Workflows** ein und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="1fb1b-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1fb1b-118">Wählen Sie die Aktion **Importieren aus Datei** aus.</span><span class="sxs-lookup"><span data-stu-id="1fb1b-118">Choose the **Import from File** action.</span></span>  
3.  <span data-ttu-id="1fb1b-119">Wählen Sie im Fenster **Importieren** die XML-Datei aus, die den Workflow enthält, und wählen Sie dann die Schaltfläche **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="1fb1b-119">In the **Import** window, choose the XML file that contains the workflow, and then choose the **Open** button.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="1fb1b-120">Wenn der Workflowcode bereits in der Datenbank vorhanden ist, werden die Workflowschritte mit den Schritten im importierten Workflow überschrieben.</span><span class="sxs-lookup"><span data-stu-id="1fb1b-120">If the workflow code already exists in the database, the workflow steps will be overwritten with the steps in the imported workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1fb1b-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1fb1b-121">See Also</span></span>  
 <span data-ttu-id="1fb1b-122">[So wird's gemacht: Erstellen von Workflows](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="1fb1b-122">[How to: Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="1fb1b-123">[Vorgehensweise: Workflows von Workflowvorlagen erstellen](across-how-to-create-workflows-from-workflow-templates.md) </span><span class="sxs-lookup"><span data-stu-id="1fb1b-123">[How to: Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md) </span></span>  
 <span data-ttu-id="1fb1b-124">[Gewusst wie: Anzeigen von archivierten Workflowschritt-Instanzen](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="1fb1b-124">[How to: View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="1fb1b-125">[So wird's gemacht: Löschen von Workflows](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="1fb1b-125">[How to: Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="1fb1b-126">[Exemplarische Vorgehensweise: Einrichten und Nutzen eines Einkaufsanfrage-Genehmigungsworkflows](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="1fb1b-126">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="1fb1b-127">[Einrichten von Workflows](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="1fb1b-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="1fb1b-128">[Verwenden von Workflows](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="1fb1b-128">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="1fb1b-129">Workflow</span><span class="sxs-lookup"><span data-stu-id="1fb1b-129">Workflow</span></span>](across-workflow.md)   

