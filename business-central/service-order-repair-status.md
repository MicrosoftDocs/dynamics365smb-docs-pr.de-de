---
title: Einrichten von Status für Serviceaufträge und Reparaturen | Microsoft Docs
description: Sie müssen neun Reparaturstatusoptionen einrichten, die den Fortschritt von Reparatur- und Wartungsarbeiten in Serviceaufträgen widerspiegeln.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1cb6ba334d4584d6e3ead25606a612686258eae9
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776816"
---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a><span data-ttu-id="ea3cf-103">Einrichten von Status für Serviceaufträge und Reparaturen</span><span class="sxs-lookup"><span data-stu-id="ea3cf-103">Set Up Statuses for Service Orders and Repairs</span></span>

<span data-ttu-id="ea3cf-104">Sie müssen Reparaturstatusoptionen einrichten, die den Fortschritt von Reparatur- und Wartungsarbeiten in Serviceaufträgen widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-104">You must set up repair status options that identify the progress of repair and maintenance of service items in service orders.</span></span> <span data-ttu-id="ea3cf-105">Sie müssen mindestens neun Reparaturstatusoptionen eingerichtet werden, die die Situation oder Aktionen von Servicearbeiten an Serviceartikeln kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-105">You must set up at least nine repair status options that identify situations or actions taken when servicing service items.</span></span>  

<span data-ttu-id="ea3cf-106">Sie können die Prioritätsstufe für die Optionen des Serviceauftragsstatus festlegen.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-106">You can set the priority level for service order status options.</span></span> <span data-ttu-id="ea3cf-107">Die vier Prioritäten lauten: **Hoch** und **Sehr Hoch**, **Sehr Gering** und **Gering**.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-107">The four priorities are **High**, **Medium High**, **Medium Low**, and **Low**.</span></span>  

<span data-ttu-id="ea3cf-108">Wenn Sie den Reparaturstatus eines Serviceartikels in einem Serviceauftrag ändern, wird der Serviceauftragsstatus aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-108">When you change the repair status of a service item in a service order, the service order status is updated.</span></span> <span data-ttu-id="ea3cf-109">Der Reparaturstatus jedes Serviceartikels ist mit dem Serviceauftragsstatus verknüpft.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-109">The repair status of each service item is linked to the service order status.</span></span> <span data-ttu-id="ea3cf-110">Sind die Serviceartikel mit zwei oder mehr Serviceauftragsstatusoptionen verknüpft, wird der Serviceauftragsstatus mit der höchsten Priorität ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-110">If the service items are linked to two or more service order status options, the service order status with the highest priority is selected.</span></span>  

<span data-ttu-id="ea3cf-111">Bevor Sie einen Reparaturstatus einrichten können, müssen Sie die Prioritäten für den Servicestatus festlegen.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-111">Before you can set up a repair status, you must set up service status priorities.</span></span>

## <a name="to-set-up-service-status-priorities"></a><span data-ttu-id="ea3cf-112">So richten Sie Servicestatusprioritäten ein</span><span class="sxs-lookup"><span data-stu-id="ea3cf-112">To set up service status priorities</span></span>

1. <span data-ttu-id="ea3cf-113">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Serviceauftragsstatus** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Order Status**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ea3cf-114">Wählen Sie den Serviceauftragsstatus aus, für den Sie eine Priorität festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-114">Select the service order status you want to set a priority for.</span></span>  
3. <span data-ttu-id="ea3cf-115">Wählen Sie im Feld **Priorität** die Priorität aus, die Sie diesem Serviceauftragsstatus zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-115">In the **Priority** field, choose the priority you want for this service order status.</span></span>  

<span data-ttu-id="ea3cf-116">Wiederholen Sie die Schritte 2 und 3, bis Sie für jede der vier Statusoptionen eine Priorität festgelegt haben:  **Offen**, **In Bearbeitung**, **Erledigt** und **Warten** .</span><span class="sxs-lookup"><span data-stu-id="ea3cf-116">Repeat steps 2 and 3 until you have set the priority for each of the four status options: **Pending**, **In Process**, **Finished**, and **On Hold**.</span></span>  

## <a name="to-set-up-a-repair-status"></a><span data-ttu-id="ea3cf-117">So richten Sie einen Reparaturstatus ein</span><span class="sxs-lookup"><span data-stu-id="ea3cf-117">To set up a repair status</span></span>

1. <span data-ttu-id="ea3cf-118">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Reparaturstatus** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Repair Status**, and then choose the related link.</span></span>
2. <span data-ttu-id="ea3cf-119">Erstellen Sie einen neuen Reparaturstatus.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-119">Create a new repair status.</span></span>  
3. <span data-ttu-id="ea3cf-120">Füllen Sie die Felder **Code** und **Beschreibung** aus.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-120">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="ea3cf-121">Wählen Sie im **Serviceauftragsstatus** Feld den Auftragsstatus aus, mit dem der Reparaturstatus verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-121">In the **Service Order Status** field, choose the order status to link the repair status to.</span></span> <span data-ttu-id="ea3cf-122">Das Feld **Priorität** zeigt die Priorität des von Ihnen ausgewählten Serviceauftragsstatus.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-122">The **Priority** field displays the priority of the service order status you have chosen.</span></span>  
5. <span data-ttu-id="ea3cf-123">Wählen Sie einen Reparaturstatus aus.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-123">Choose a repair status.</span></span> <span data-ttu-id="ea3cf-124">Sie können nur einen auswählen.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-124">You can choose only one.</span></span> <span data-ttu-id="ea3cf-125">Ein Reparaturstatus kann nicht mit mehr als einer Reparaturstatusoption verknüpft sein.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-125">A repair status cannot be linked more than one repair status option.</span></span>  
6. <span data-ttu-id="ea3cf-126">Um Serviceverträge, einschließlich Serviceartikel, mit diesem Reparaturstatus buchen zu können, wählen Sie das Feld **Buchen zulassen** aus.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-126">To be able to post service orders, including service items, with this repair status, choose the **Posting Allowed** field.</span></span>  
7. <span data-ttu-id="ea3cf-127">Um die Serviceauftragsstatusoption in Serviceaufträgen, die Serviceartikel mit diesem Reparaturstatus enthalten, manuell auf **Offen** ändern zu können, wählen Sie das Kontrollkästchen **Status Offen zulassen** aus.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-127">To be able to manually change the service order status option to **Pending** in service orders including service items with this repair status, choose the **Pending Status Allowed** check box.</span></span>  
8. <span data-ttu-id="ea3cf-128">Wählen Sie die Kontrollkästchen **Status in Bearbeitung zulassen**, **Status Erledigt zulassen** und **Status Warten zulassen** auf die gleiche Weise aus.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-128">Choose the **In Process Status Allowed**, **Finished Status Allowed**, and **On Hold Status Allowed** check boxes in the same way.</span></span>

<span data-ttu-id="ea3cf-129">Wiederholen Sie diese Schritte für jede Reparaturstatusoption, die Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="ea3cf-129">Repeat these steps for each of the repair status options you want to create.</span></span>

## <a name="see-also"></a><span data-ttu-id="ea3cf-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea3cf-130">See Also</span></span>

[<span data-ttu-id="ea3cf-131">Serviceauftragsstatus und Reparaturstatus</span><span class="sxs-lookup"><span data-stu-id="ea3cf-131">Service Order Status and Repair Status</span></span>](service-service-order-status-and-repair-status.md)  
[<span data-ttu-id="ea3cf-132">Einrichten der Serviceverwaltung</span><span class="sxs-lookup"><span data-stu-id="ea3cf-132">Setting Up Service Management</span></span>](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]