---
title: Verwenden von Workflows
description: Sie können Workflows einrichten und verwenden, die Geschäftsprozessaufgaben von verschiedenen Benutzern verbinden. Erfahren Sie mehr über die verschiedenen Schritte, die Sie ausführen müssen, um Workflows zu verwenden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 375d53975bca97d16b3857056d44b9eada5cca97
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753000"
---
# <a name="using-workflows"></a><span data-ttu-id="1e355-104">Verwenden von Workflows</span><span class="sxs-lookup"><span data-stu-id="1e355-104">Using Workflows</span></span>
<span data-ttu-id="1e355-105">Sie können Workflows einrichten und verwenden, die Geschäftsprozessaufgaben von verschiedenen Benutzern verbinden.</span><span class="sxs-lookup"><span data-stu-id="1e355-105">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="1e355-106">Systemaufgaben, wie automatische Buchung, können als Schritte in Workflows berücksichtigt werden, vor oder nach Benutzeraufgaben.</span><span class="sxs-lookup"><span data-stu-id="1e355-106">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="1e355-107">Die Anforderung oder Bewilligung von Genehmigungen zum Erstellen neuer Datensätze sind typische Workflowschritte.</span><span class="sxs-lookup"><span data-stu-id="1e355-107">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="1e355-108">Bevor Sie beginnen können, Workflows zu verwenden, müssen Sie Workflowbenutzer einrichten, die Workflows erstellen, möglicherweise Codeanpassung berücksichtigen und angeben, wie Benutzer Benachrichtigungen empfangen sollen.</span><span class="sxs-lookup"><span data-stu-id="1e355-108">Before you can begin to use workflows, you must set up workflow users, create the workflows, potentially preceded by code customization and specify how users receive notifications.</span></span> <span data-ttu-id="1e355-109">Weitere Informationen erhalten Sie unter [Workflows einrichten](across-set-up-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="1e355-109">For more information, see [Setting Up Workflows](across-set-up-workflows.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="1e355-110">Typische Workflowschritte drehen sich um Benutzer, die Genehmigungen für Aufgaben anfordern, und Genehmiger, die Genehmigungsanforderungen annehmen oder ablehen.</span><span class="sxs-lookup"><span data-stu-id="1e355-110">Typical workflow steps are about users who request approval of tasks and approvers accepting or rejecting approval requests.</span></span> <span data-ttu-id="1e355-111">Daher beschäftigen sich viele Themen in Bezug auf die Verwendung von Workflows mit Genehmigungen.</span><span class="sxs-lookup"><span data-stu-id="1e355-111">Therefore, many topics about how to use workflows refer to approvals.</span></span>  

 <span data-ttu-id="1e355-112">Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Themen, die sie beschreiben..</span><span class="sxs-lookup"><span data-stu-id="1e355-112">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="1e355-113">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="1e355-113">**To**</span></span>|<span data-ttu-id="1e355-114">**Informationen**</span><span class="sxs-lookup"><span data-stu-id="1e355-114">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="1e355-115">Richten Sie einen Workflow ein, der gestartet wird, wenn das erste Einstiegspunktereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="1e355-115">Set a workflow to start when the first entry-point event occurs.</span></span>|[<span data-ttu-id="1e355-116">Aktivieren von Workflows</span><span class="sxs-lookup"><span data-stu-id="1e355-116">Enable Workflows</span></span>](across-how-to-enable-workflows.md)|  
|<span data-ttu-id="1e355-117">Anforderung der Genehmigung einer Aufgabe, Akzeptieren oder Delegieren von Genehmigungen oder Ablehnen von Genehmigungen, und Senden oder Anzeigen von Genehmigungsbenachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="1e355-117">Request approval of a task, as an approver, accept, decline, or delegate approvals, and send or view approval notifications.</span></span>|[<span data-ttu-id="1e355-118">Artikelgenehmigungsworkflow verwenden</span><span class="sxs-lookup"><span data-stu-id="1e355-118">Use Approval Workflows</span></span>](across-how-use-approval-workflows.md)|  
|<span data-ttu-id="1e355-119">Erstellen Sie Workflowschritte, die einen bestimmten Datensatztyp für die Verwendung vor einem bestimmten Ereignis einschränken (beispielsweise, bevor der Datensatz genehmigt wird).</span><span class="sxs-lookup"><span data-stu-id="1e355-119">Create workflow steps that restrict a certain record type from being used before a certain event occurs, for example that the record is approved.</span></span>|[<span data-ttu-id="1e355-120"> Zulassen und Einschränken des Verbrauchs eines Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="1e355-120">Restrict and Allow Usage of a Record</span></span>](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|<span data-ttu-id="1e355-121">Zeigen Sie Workflowschrittinstanzen mit dem Status „Abgeschlossen“ an.</span><span class="sxs-lookup"><span data-stu-id="1e355-121">View workflow step instances of status Completed.</span></span>|[<span data-ttu-id="1e355-122">Anzeigen von archivierten Workflowschritt-Instanzen</span><span class="sxs-lookup"><span data-stu-id="1e355-122">View Archived Workflow Step Instances</span></span>](across-how-to-view-archived-workflow-step-instances.md)|  
|<span data-ttu-id="1e355-123">Löschen Sie einen Workflow, den Sie mit Gewissheit nicht mehr verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="1e355-123">Delete a workflow that you are sure will no longer be used.</span></span>|[<span data-ttu-id="1e355-124">Löschen eines Workflows</span><span class="sxs-lookup"><span data-stu-id="1e355-124">Delete Workflows</span></span>](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="1e355-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e355-125">See Also</span></span>  
<span data-ttu-id="1e355-126">[Einrichten von Workflows](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="1e355-126">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
<span data-ttu-id="1e355-127">[Workflow](across-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="1e355-127">[Workflow](across-workflow.md) </span></span>  
<span data-ttu-id="1e355-128">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1e355-128">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
