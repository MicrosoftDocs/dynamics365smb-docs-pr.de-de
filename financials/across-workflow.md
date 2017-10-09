---
title: Workflow | Microsoft Docs
description: "Sie können Workflows einrichten und verwenden, die Geschäftsprozessaufgaben von verschiedenen Benutzern verbinden. Systemaufgaben, wie automatische Buchung, können als Schritte in Workflows berücksichtigt werden, vor oder nach Benutzeraufgaben. Die Anforderung oder Bewilligung von Genehmigungen zum Erstellen neuer Datensätze sind typische Workflowschritte."
services: project-madeira
documentationcenter: 
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: f65c0e577e839928809f7afda3dbdb4c9b7702c8
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="workflow"></a><span data-ttu-id="0a9fc-105">Workflow</span><span class="sxs-lookup"><span data-stu-id="0a9fc-105">Workflow</span></span>
<span data-ttu-id="0a9fc-106">Sie können Workflows einrichten und verwenden, die Geschäftsprozessaufgaben von verschiedenen Benutzern verbinden.</span><span class="sxs-lookup"><span data-stu-id="0a9fc-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="0a9fc-107">Systemaufgaben, wie automatische Buchung, können als Schritte in Workflows berücksichtigt werden, vor oder nach Benutzeraufgaben.</span><span class="sxs-lookup"><span data-stu-id="0a9fc-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="0a9fc-108">Die Anforderung oder Bewilligung von Genehmigungen zum Erstellen neuer Datensätze sind typische Workflowschritte.</span><span class="sxs-lookup"><span data-stu-id="0a9fc-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="0a9fc-109">Im Fenster **Workflow** können Sie einen Workflow erstellen, indem Sie die entsprechenden Schritte in den Zeilen auflisten.</span><span class="sxs-lookup"><span data-stu-id="0a9fc-109">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="0a9fc-110">Jeder Schritt besteht aus einem durch Ereignisbedingungen moderiertem Workflowereignis und einer durch Antwortoptionen moderierten Workflowantwort.</span><span class="sxs-lookup"><span data-stu-id="0a9fc-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="0a9fc-111">Sie definieren Workflowschritte, indem Sie die Felder in Workflowzeilen mit Ereignis- und Antwortwerten aus festen Listen ausfüllen, die die Workflowszenarien darstellen, die durch den Anwendungscode unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="0a9fc-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span>  

 <span data-ttu-id="0a9fc-112">Die generische Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] umfasst mehrere vorkonfigurierte Workflows, für die Workflowvorlagen vorliegen. Diese können Sie kopieren, um Workflows zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0a9fc-112">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] includes a number of preconfigured workflows represented by workflow templates that you can copy to create workflows.</span></span> <span data-ttu-id="0a9fc-113">Dem Code für von Microsoft hinzugefügte Workflowvorlagen ist „MS-“ vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="0a9fc-113">The code for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span> <span data-ttu-id="0a9fc-114">Weitere Informationen finden Sie in der Liste mit Workflowvorlagen im Fenster Workflow-Vorlagen</span><span class="sxs-lookup"><span data-stu-id="0a9fc-114">For more information, see the list of workflow templates in the Workflow Templates window.</span></span>  

 <span data-ttu-id="0a9fc-115">Wenn ein Szenario ein Workflowereignis oder -antwort benötigt, die nicht unterstützt wird, muss ein Microsoft-Partner diese implementieren, indem er den Anwendungscode anpasst.</span><span class="sxs-lookup"><span data-stu-id="0a9fc-115">If a business scenario requires a workflow event or response that is not supported, a Microsoft partner must implement them by customizing the application code.</span></span> <span data-ttu-id="0a9fc-116">Weitere Informationen finden Sie unter [Exemplarische Vorgehensweise: Implementieren von neuen Workflowereignissen und von Kampagnenreaktionen](https://msdn.microsoft.com/en-us/library/mt574349.aspx) in MSDN</span><span class="sxs-lookup"><span data-stu-id="0a9fc-116">For more information, see [Walkthrough: Implementing New Workflow Events and Responses](https://msdn.microsoft.com/en-us/library/mt574349.aspx) on MSDN.</span></span>  

 <span data-ttu-id="0a9fc-117">Die folgende Tabelle enthält eine Abfolge von Aufgaben sowie Links zu den entsprechenden Themen, in denen diese Aufgaben erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="0a9fc-117">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="0a9fc-118">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="0a9fc-118">**To**</span></span>|<span data-ttu-id="0a9fc-119">**Informationen**</span><span class="sxs-lookup"><span data-stu-id="0a9fc-119">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="0a9fc-120">Richten Sie Workflowbenutzer ein, geben Sie an, wie Benutzer benachrichtigt werden, und erstellen Sie neue Workflows.</span><span class="sxs-lookup"><span data-stu-id="0a9fc-120">Set up workflow users, specify how users get notified, and create new workflows.</span></span> <span data-ttu-id="0a9fc-121">Implementieren Sie für neue Workflow für nicht unterstützte Szenarien die erforderlichen Workflowelemente, indem Sie den Anwendungscode anpassen.</span><span class="sxs-lookup"><span data-stu-id="0a9fc-121">For new workflows for unsupported scenarios, implement the required workflow elements by customizing the application code.</span></span>|[<span data-ttu-id="0a9fc-122">Einrichten von Workflows</span><span class="sxs-lookup"><span data-stu-id="0a9fc-122">Setting Up Workflows</span></span>](across-set-up-workflows.md)|  
|<span data-ttu-id="0a9fc-123">Aktivieren Sie Workflows, reagieren Sie auf Workflowbenachrichtigungen, einschließlich Anfragegenehmigungen und genehmigen Sie Anforderungen, um einen Workflowschritt auszuführen.</span><span class="sxs-lookup"><span data-stu-id="0a9fc-123">Enable workflows, act on workflow notifications, including request approvals and approve requests to perform a workflow step.</span></span> <span data-ttu-id="0a9fc-124">Archivieren und löschen Sie Workflows.</span><span class="sxs-lookup"><span data-stu-id="0a9fc-124">Archive and delete workflows.</span></span>|[<span data-ttu-id="0a9fc-125">Verwenden von Workflows</span><span class="sxs-lookup"><span data-stu-id="0a9fc-125">Using Workflows</span></span>](across-use-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="0a9fc-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a9fc-126">See Also</span></span>  
[<span data-ttu-id="0a9fc-127">Verkauf</span><span class="sxs-lookup"><span data-stu-id="0a9fc-127">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="0a9fc-128">Einkauf</span><span class="sxs-lookup"><span data-stu-id="0a9fc-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="0a9fc-129">Projekte verwalten</span><span class="sxs-lookup"><span data-stu-id="0a9fc-129">Managing Projects</span></span>](projects-manage-projects.md)  
<span data-ttu-id="0a9fc-130">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0a9fc-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

