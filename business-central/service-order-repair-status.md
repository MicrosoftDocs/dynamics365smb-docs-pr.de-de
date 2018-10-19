---
title: "Einrichten von Status für Serviceaufträge und Reparaturen | Microsoft Docs"
description: "Sie müssen neun Reparaturstatusoptionen einrichten, die den Fortschritt von Reparatur- und Wartungsarbeiten in Serviceaufträgen widerspiegeln."
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
ms.openlocfilehash: 366bf200b78e4927b1c202340dd84af09d32c1a5
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a><span data-ttu-id="18154-103">Einrichten von Status für Serviceaufträge und Reparaturen</span><span class="sxs-lookup"><span data-stu-id="18154-103">Set Up Statuses for Service Orders and Repairs</span></span>
<span data-ttu-id="18154-104">Sie müssen Reparaturstatusoptionen einrichten, die den Fortschritt von Reparatur- und Wartungsarbeiten in Serviceaufträgen widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="18154-104">You must set up repair status options that identify the progress of repair and maintenance of service items in service orders.</span></span> <span data-ttu-id="18154-105">Sie müssen mindestens neun Reparaturstatusoptionen eingerichtet werden, die die Situation oder Aktionen von Servicearbeiten an Serviceartikeln kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="18154-105">You must set up at least nine repair status options that identify situations or actions taken when servicing service items.</span></span>  

<span data-ttu-id="18154-106">Sie können die Prioritätsstufe für die Optionen des Serviceauftragsstatus festlegen.</span><span class="sxs-lookup"><span data-stu-id="18154-106">You can set the priority level for service order status options.</span></span> <span data-ttu-id="18154-107">Die vier Prioritäten lauten: "Hoch" und "Sehr Hoch", "Sehr Gering" und "Gering".</span><span class="sxs-lookup"><span data-stu-id="18154-107">There four priorities are High, Medium High, Medium Low, and Low.</span></span>  

<span data-ttu-id="18154-108">Wenn Sie den Reparaturstatus eines Serviceartikels in einem Serviceauftrag ändern, wird der Serviceauftragsstatus aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="18154-108">When you change the repair status of a service item in a service order, the service order status is updated.</span></span> <span data-ttu-id="18154-109">Der Reparaturstatus jedes Serviceartikels ist mit dem Serviceauftragsstatus verknüpft.</span><span class="sxs-lookup"><span data-stu-id="18154-109">The repair status of each service item is linked to the service order status.</span></span> <span data-ttu-id="18154-110">Sind die Serviceartikel mit zwei oder mehr Serviceauftragsstatusoptionen verknüpft, wird der Serviceauftragsstatus mit der höchsten Priorität ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="18154-110">If the service items are linked to two or more service order status options, the service order status with the highest priority is selected.</span></span>  

## <a name="to-set-up-a-repair-status"></a><span data-ttu-id="18154-111">So richten Sie einen Reparaturstatus ein</span><span class="sxs-lookup"><span data-stu-id="18154-111">To set up a repair status</span></span>  
1. <span data-ttu-id="18154-112">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Reparaturstatus** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="18154-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Repair Status**, and then choose the related link.</span></span>
2. <span data-ttu-id="18154-113">Erstellen Sie einen neuen Reparaturstatus.</span><span class="sxs-lookup"><span data-stu-id="18154-113">Create a new repair status.</span></span>  
3. <span data-ttu-id="18154-114">Füllen Sie die Felder **Code** und **Beschreibung** aus.</span><span class="sxs-lookup"><span data-stu-id="18154-114">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="18154-115">Wählen Sie im **Serviceauftragsstatus** Feld den Auftragsstatus aus, mit dem der Reparaturstatus verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="18154-115">In the **Service Order Status** field, choose the order status to link the repair status to.</span></span> <span data-ttu-id="18154-116">Das Feld **Priorität** zeigt die Priorität des von Ihnen ausgewählten Serviceauftragsstatus.</span><span class="sxs-lookup"><span data-stu-id="18154-116">The **Priority** field displays the priority of the service order status you have chosen.</span></span>  
5. <span data-ttu-id="18154-117">Wählen Sie einen Reparaturstatus aus.</span><span class="sxs-lookup"><span data-stu-id="18154-117">Choose a repair status.</span></span> <span data-ttu-id="18154-118">Sie können nur einen auswählen.</span><span class="sxs-lookup"><span data-stu-id="18154-118">You can choose only one.</span></span>  
6. <span data-ttu-id="18154-119">Um Serviceverträge, einschließlich Serviceartikel, mit diesem Reparaturstatus buchen zu können, wählen Sie das Feld **Buchen zulassen** aus.</span><span class="sxs-lookup"><span data-stu-id="18154-119">To be able to post service orders, including service items, with this repair status, choose the **Posting Allowed** field.</span></span>  
7. <span data-ttu-id="18154-120">Um die Serviceauftragsstatusoption in Serviceaufträgen, die Serviceartikel mit diesem Reparaturstatus enthalten, manuell auf **Offen** ändern zu können, wählen Sie das Kontrollkästchen **Status Offen zulassen** aus.</span><span class="sxs-lookup"><span data-stu-id="18154-120">To be able to manually change the service order status option to **Pending** in service orders including service items with this repair status, choose the **Pending Status Allowed** check box.</span></span>  
8. <span data-ttu-id="18154-121">Wählen Sie die Kontrollkästchen **Status in Bearbeitung zulassen**, **Status Erledigt zulassen**und **Status Warten zulassen** auf die gleiche Weise aus.</span><span class="sxs-lookup"><span data-stu-id="18154-121">Choose the **In Process Status Allowed**, **Finished Status Allowed**, and **On Hold Status Allowed** check boxes in the same way.</span></span>
  
## <a name="to-set-up-service-status-priorities"></a><span data-ttu-id="18154-122">So richten Sie Servicestatusprioritäten ein</span><span class="sxs-lookup"><span data-stu-id="18154-122">To set up service status priorities</span></span>  
1. <span data-ttu-id="18154-123">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Serviceauftragsstatus** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="18154-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Order Status**, and then choose the related link.</span></span>  
2. <span data-ttu-id="18154-124">Wählen Sie den Serviceauftragsstatus aus, für den Sie eine Priorität festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="18154-124">Select the service order status you want to set a priority for.</span></span>  
3. <span data-ttu-id="18154-125">Wählen Sie im Feld **Priorität**die Priorität aus, die Sie diesem Serviceauftragsstatus zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="18154-125">In the **Priority** field, choose the priority you want for this service order status.</span></span> <span data-ttu-id="18154-126">Wiederholen Sie diesen Schritt für jeden Status.</span><span class="sxs-lookup"><span data-stu-id="18154-126">Repeat this step for each status.</span></span>  

## <a name="see-also"></a><span data-ttu-id="18154-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18154-127">See Also</span></span>  
[<span data-ttu-id="18154-128">Serviceauftragsstatus und Reparaturstatus</span><span class="sxs-lookup"><span data-stu-id="18154-128">Service Order Status and Repair Status</span></span>](service-service-order-status-and-repair-status.md)  
[<span data-ttu-id="18154-129">Einrichten der Serviceverwaltung</span><span class="sxs-lookup"><span data-stu-id="18154-129">Setting Up Service Management</span></span>](service-setup-service.md)  

