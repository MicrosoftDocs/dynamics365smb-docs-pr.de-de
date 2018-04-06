---
title: "Gewusst wie: Beschränken und Zulassen der Nutzung eines Datensatzes | Microsoft Docs"
description: "Wenn Sie verhindern möchten, dass ein Datensatz für bestimmte Aktivitäten verwendet wird (beispielsweise so lange, bis der Datensatz genehmigt wurde), können Sie zwei Workflowantworten in einen Workflow einbauen, der die Verwendung des Datensatzes steuert."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4636cdedc2c99d1aa7cfc2dc361f7135aa3c4199
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="restrict-and-allow-usage-of-a-record"></a><span data-ttu-id="6194a-103">Zulassen und Einschränken des Verbrauchs eines Datensatzes</span><span class="sxs-lookup"><span data-stu-id="6194a-103">Restrict and Allow Usage of a Record</span></span>
<span data-ttu-id="6194a-104">Wenn Sie verhindern möchten, dass ein Datensatz für bestimmte Aktivitäten verwendet wird (beispielsweise so lange, bis der Datensatz genehmigt wurde), können Sie zwei Workflowantworten in einen Workflow einbauen, der die Verwendung des Datensatzes steuert.</span><span class="sxs-lookup"><span data-stu-id="6194a-104">If you want to restrict a record from being used in certain activities, for example, until the record has been approved, you can incorporate two workflow responses in a workflow that controls the usage of the record.</span></span> <span data-ttu-id="6194a-105">Eine Workflowantwort schränkt die Nutzung des Datensatzes entsprechend des definierten Workflowereignis und die der Bedingungen ein.</span><span class="sxs-lookup"><span data-stu-id="6194a-105">One workflow response will restrict usage of the record as defined by the workflow event and conditions.</span></span> <span data-ttu-id="6194a-106">Eine weitere Workflowantwort läßt die Nutzung des Datensatzes entsprechend des definierten Workflowereignis und die der Bedingungen zu.</span><span class="sxs-lookup"><span data-stu-id="6194a-106">Another workflow response will allow usage of the record as defined by the workflow event and conditions.</span></span> <span data-ttu-id="6194a-107">In der generische Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] stehen zwei Antworten zu diesem Zweck zur Verfügung: **Nutzung eines Datensatzes einschränken** und Zulassen der Nutzung eines Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="6194a-107">Two responses exist in the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] for this purpose: **Restrict usage of a record.**</span></span> <span data-ttu-id="6194a-108">und **Zulassen Verbrauch eines Datensatzes**.</span><span class="sxs-lookup"><span data-stu-id="6194a-108">and **Allow usage of a record.**.</span></span>

> [!NOTE]  
>  <span data-ttu-id="6194a-109">Die generische Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt die Beschränkung der Buchung, des Exports als Zahlung und des Druckens als Scheck für einen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="6194a-109">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] offers support for restricting a record from being posted, from being exported as a payment, and from being printed as a check.</span></span> <span data-ttu-id="6194a-110">Um andere Einschränkungen zu unterstützen muss ein Microsoft-Partner den Anwendungscode anpassen.</span><span class="sxs-lookup"><span data-stu-id="6194a-110">To support other restrictions, a Microsoft partner must customize the application code.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="6194a-111">Die Workflowfunktionalität zur Einschränkung der Nutzung von Datensätzen ist nicht mit der Funktionalität zur Blockierung der Buchung von Artikel-, Debitor- und Kreditordatensätze verknüpft.</span><span class="sxs-lookup"><span data-stu-id="6194a-111">The workflow functionality to restrict and allow records from being used is not related to the functionality to block item, customer, and vendor records from being posted.</span></span>

<span data-ttu-id="6194a-112">Nachfolgend wird beschrieben, wie das Buchen von Bestellungen bis zu deren Genehmigung eingeschränkt werden kann.</span><span class="sxs-lookup"><span data-stu-id="6194a-112">The following procedure describes how to restrict purchase orders from being posted until they have been approved.</span></span> <span data-ttu-id="6194a-113">Der neue Workflow basiert auf der vorhandene Workflowvorlage "Einkaufsrechnungs-Genehmigungsworkflow".</span><span class="sxs-lookup"><span data-stu-id="6194a-113">The new workflow will be based on the existing Purchase Invoice Approval Workflow workflow template.</span></span>  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a><span data-ttu-id="6194a-114">So erstellen Sie einen Workflowschritt, der die Buchung von nicht genehmigten Einkaufsbestellungen einschränkt</span><span class="sxs-lookup"><span data-stu-id="6194a-114">To create a workflow step that restricts posting of unapproved purchase orders</span></span>  
1. <span data-ttu-id="6194a-115">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Workflows** ein und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="6194a-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6194a-116">Im Fenster **Workflo** erstellen Sie einen neuen Workflow mit dem Namen "Einkaufsbestellungs-Genehmigungsworkflow".</span><span class="sxs-lookup"><span data-stu-id="6194a-116">In the **Workflows** window, create a new workflow named Purchase Order Approval Workflow.</span></span> <span data-ttu-id="6194a-117">Weitere Informationen finden Sie unter [Workflows erstellen](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="6194a-117">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  
3. <span data-ttu-id="6194a-118">Wählen Sie die Aktion **Von Workflowvorlage kopieren** aus.</span><span class="sxs-lookup"><span data-stu-id="6194a-118">Choose the **Copy From Workflow Template** action.</span></span>  
4. <span data-ttu-id="6194a-119">Wählen Sie das **Quellworkflow-Code**-Feld aus und wählen Sie dann im Fenster die **Workflowvorlage** "Einkaufsrechnungs-Genehmigungsworkflow" aus.</span><span class="sxs-lookup"><span data-stu-id="6194a-119">Choose the **Source Workflow Code** field, and then, in the **Workflow Templates** window, choose the Purchase Invoice Approval Workflow workflow template.</span></span>  

     <span data-ttu-id="6194a-120">Beachten Sie, dass die ersten beiden Workflowschritte zur Einschränkung und Zulassung der Nutzung von Einkaufsrechnungen dienen.</span><span class="sxs-lookup"><span data-stu-id="6194a-120">Notice that the first two workflow steps are about restricting and then allowing usage of purchase invoices.</span></span> <span data-ttu-id="6194a-121">Bearbeiten Sie die Ereignisbedingung des ersten Schritts des neuen Workflows. Legen Sie fest, dass er auf Einkaufsbestellungen angewandt wird.</span><span class="sxs-lookup"><span data-stu-id="6194a-121">Proceed to change the event condition on the first step of the new workflow to specify that it applies to purchase orders.</span></span>  
5. <span data-ttu-id="6194a-122">Wählen Sie im **Workflow-Schritte**-Inforegister das Feld **Ereigniskonditionen** , und wählen Sie dann für den Filter **Dokumentart** die Option **Auftrag** aus.</span><span class="sxs-lookup"><span data-stu-id="6194a-122">On the **Workflow Steps** FastTab, choose the **Event Conditions** field, and then, for the **Document Type** filter, select **Order**.</span></span>  
6. <span data-ttu-id="6194a-123">Lösen, bearbeiten oder erstellen Sie andere Workflowschritte, um einen Geschäftsprozess abzudecken der mit der Einschränkung der Buchung von nicht genehmigten Einkaufsbestellungen beginnt.</span><span class="sxs-lookup"><span data-stu-id="6194a-123">Proceed to edit, delete, or add other workflow steps to fit a business process that begins by restricting unapproved purchase orders from being posted.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6194a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6194a-124">See Also</span></span>  
<span data-ttu-id="6194a-125">[Erstellen eines Workflows](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="6194a-125">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
[<span data-ttu-id="6194a-126">Workflow</span><span class="sxs-lookup"><span data-stu-id="6194a-126">Workflow</span></span>](across-workflow.md)   

