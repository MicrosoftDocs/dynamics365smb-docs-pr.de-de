---
title: Workflow | Microsoft Docs
description: "Sie können Workflows einrichten und verwenden, die Geschäftsprozessaufgaben von verschiedenen Benutzern verbinden. Systemaufgaben, wie automatische Buchung, können als Schritte in Workflows berücksichtigt werden, vor oder nach Benutzeraufgaben. Die Anforderung oder Bewilligung von Genehmigungen zum Erstellen neuer Datensätze sind typische Workflowschritte."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 7a7782fcb51eb9078cb62c4892814cd178518332
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="workflow"></a><span data-ttu-id="73886-105">Workflow</span><span class="sxs-lookup"><span data-stu-id="73886-105">Workflow</span></span>
<span data-ttu-id="73886-106">Sie können Workflows einrichten und verwenden, die Geschäftsprozessaufgaben von verschiedenen Benutzern verbinden.</span><span class="sxs-lookup"><span data-stu-id="73886-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="73886-107">Systemaufgaben, wie automatische Buchung, können als Schritte in Workflows berücksichtigt werden, vor oder nach Benutzeraufgaben.</span><span class="sxs-lookup"><span data-stu-id="73886-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="73886-108">Die Anforderung oder Bewilligung von Genehmigungen zum Erstellen neuer Datensätze sind typische Workflowschritte.</span><span class="sxs-lookup"><span data-stu-id="73886-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="73886-109">Im Fenster **Workflow** können Sie einen Workflow erstellen, indem Sie die entsprechenden Schritte in den Zeilen auflisten.</span><span class="sxs-lookup"><span data-stu-id="73886-109">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="73886-110">Jeder Schritt besteht aus einem durch Ereignisbedingungen moderiertem Workflowereignis und einer durch Antwortoptionen moderierten Workflowantwort.</span><span class="sxs-lookup"><span data-stu-id="73886-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="73886-111">Sie definieren Workflowschritte, indem Sie die Felder in Workflowzeilen mit Ereignis- und Antwortwerten aus festen Listen ausfüllen, die die Workflowszenarien darstellen, die durch den Anwendungscode unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="73886-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span>  

 <span data-ttu-id="73886-112">Die generische Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] umfasst mehrere vorkonfigurierte Workflows, für die Workflowvorlagen vorliegen. Diese können Sie kopieren, um Workflows zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="73886-112">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] includes a number of preconfigured workflows represented by workflow templates that you can copy to create workflows.</span></span> <span data-ttu-id="73886-113">Dem Code für von Microsoft hinzugefügte Workflowvorlagen ist „MS-“ vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="73886-113">The code for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span> <span data-ttu-id="73886-114">Weitere Informationen finden Sie in der Liste mit Workflowvorlagen im Fenster Workflow-Vorlagen</span><span class="sxs-lookup"><span data-stu-id="73886-114">For more information, see the list of workflow templates in the Workflow Templates window.</span></span>  

 <span data-ttu-id="73886-115">Wenn ein Szenario ein Workflowereignis oder -antwort benötigt, die nicht unterstützt wird, muss ein Microsoft-Partner diese implementieren, indem er den Anwendungscode anpasst.</span><span class="sxs-lookup"><span data-stu-id="73886-115">If a business scenario requires a workflow event or response that is not supported, a Microsoft partner must implement them by customizing the application code.</span></span> <span data-ttu-id="73886-116">Weitere Informationen finden Sie unter [Exemplarische Vorgehensweise: Implementieren von neuen Workflowereignissen und von Kampagnenreaktionen](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) in der Entwickler- und IT-Pro-Hilfe.</span><span class="sxs-lookup"><span data-stu-id="73886-116">For more information, see [Walkthrough: Implementing New Workflow Events and Responses](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) in the developer and IT-pro help.</span></span>

> [!NOTE]  
> <span data-ttu-id="73886-117">Workflow können auch von Microsoft Flow initiert werden.</span><span class="sxs-lookup"><span data-stu-id="73886-117">Workflows can also be initiated from Microsoft Flow.</span></span> <span data-ttu-id="73886-118">Weitere Informationen finden Sie unter [Business Central in einem automatisierten Workflow nutzen](across-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="73886-118">For more information, see [Using Business Central in an Automated Workflow](across-how-use-financials-data-source-flow.md).</span></span>  

 <span data-ttu-id="73886-119">In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.</span><span class="sxs-lookup"><span data-stu-id="73886-119">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="73886-120">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="73886-120">**To**</span></span>|<span data-ttu-id="73886-121">**Informationen**</span><span class="sxs-lookup"><span data-stu-id="73886-121">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="73886-122">Richten Sie Workflowbenutzer ein, geben Sie an, wie Benutzer benachrichtigt werden, und erstellen Sie neue Workflows.</span><span class="sxs-lookup"><span data-stu-id="73886-122">Set up workflow users, specify how users get notified, and create new workflows.</span></span> <span data-ttu-id="73886-123">Implementieren Sie für neue Workflow für nicht unterstützte Szenarien die erforderlichen Workflowelemente, indem Sie den Anwendungscode anpassen.</span><span class="sxs-lookup"><span data-stu-id="73886-123">For new workflows for unsupported scenarios, implement the required workflow elements by customizing the application code.</span></span>|[<span data-ttu-id="73886-124">Einrichten von Workflows</span><span class="sxs-lookup"><span data-stu-id="73886-124">Setting Up Workflows</span></span>](across-set-up-workflows.md)|  
|<span data-ttu-id="73886-125">Aktivieren Sie Workflows, reagieren Sie auf Workflowbenachrichtigungen, einschließlich Anfragegenehmigungen und genehmigen Sie Anforderungen, um einen Workflowschritt auszuführen.</span><span class="sxs-lookup"><span data-stu-id="73886-125">Enable workflows, act on workflow notifications, including request approvals and approve requests to perform a workflow step.</span></span> <span data-ttu-id="73886-126">Archivieren und löschen Sie Workflows.</span><span class="sxs-lookup"><span data-stu-id="73886-126">Archive and delete workflows.</span></span>|[<span data-ttu-id="73886-127">Verwenden von Workflows</span><span class="sxs-lookup"><span data-stu-id="73886-127">Using Workflows</span></span>](across-use-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="73886-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73886-128">See Also</span></span>  
[<span data-ttu-id="73886-129">Verkauf</span><span class="sxs-lookup"><span data-stu-id="73886-129">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="73886-130">Einkauf</span><span class="sxs-lookup"><span data-stu-id="73886-130">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="73886-131">Projekte verwalten</span><span class="sxs-lookup"><span data-stu-id="73886-131">Managing Projects</span></span>](projects-manage-projects.md)  
<span data-ttu-id="73886-132">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="73886-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

