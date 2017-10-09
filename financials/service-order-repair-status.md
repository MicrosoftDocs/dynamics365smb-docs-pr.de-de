---
title: "Einrichten von Status für Serviceaufträge und Reparaturen | Microsoft Docs"
description: "Sie müssen neun Reparaturstatusoptionen einrichten, die den Fortschritt von Reparatur- und Wartungsarbeiten in Serviceaufträgen widerspiegeln."
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
ms.openlocfilehash: 36925a08f7fdfffedf13902a5c6feaaa8b0929a4
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-statuses-for-service-orders-and-repairs"></a><span data-ttu-id="0a6aa-103">Vorgehensweise: Einrichten von Status für Serviceaufträge und Reparaturen</span><span class="sxs-lookup"><span data-stu-id="0a6aa-103">How to: Set Up Statuses for Service Orders and Repairs</span></span>
<span data-ttu-id="0a6aa-104">Sie müssen Reparaturstatusoptionen einrichten, die den Fortschritt von Reparatur- und Wartungsarbeiten in Serviceaufträgen widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="0a6aa-104">You must set up repair status options that identify the progress of repair and maintenance of service items in service orders.</span></span> <span data-ttu-id="0a6aa-105">Sie müssen mindestens neun Reparaturstatusoptionen eingerichtet werden, die die Situation oder Aktionen von Servicearbeiten an Serviceartikeln kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="0a6aa-105">You must set up at least nine repair status options that identify situations or actions taken when servicing service items.</span></span>  

<span data-ttu-id="0a6aa-106">Sie können die Prioritätsstufe für die Optionen des Serviceauftragsstatus festlegen.</span><span class="sxs-lookup"><span data-stu-id="0a6aa-106">You can set the priority level for service order status options.</span></span> <span data-ttu-id="0a6aa-107">Die vier Prioritäten lauten: "Hoch" und "Sehr Hoch", "Sehr Gering" und "Gering".</span><span class="sxs-lookup"><span data-stu-id="0a6aa-107">There four priorities are High, Medium High, Medium Low, and Low.</span></span>  
  
<span data-ttu-id="0a6aa-108">Wenn Sie den Reparaturstatus eines Serviceartikels in einem Serviceauftrag ändern, wird der Serviceauftragsstatus aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0a6aa-108">When you change the repair status of a service item in a service order, the service order status is updated.</span></span> <span data-ttu-id="0a6aa-109">Der Reparaturstatus jedes Serviceartikels ist mit dem Serviceauftragsstatus verknüpft.</span><span class="sxs-lookup"><span data-stu-id="0a6aa-109">The repair status of each service item is linked to the service order status.</span></span> <span data-ttu-id="0a6aa-110">Sind die Serviceartikel mit zwei oder mehr Serviceauftragsstatusoptionen verknüpft, wird der Serviceauftragsstatus mit der höchsten Priorität ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="0a6aa-110">If the service items are linked to two or more service order status options, the service order status with the highest priority is selected.</span></span>  

## <a name="to-set-up-a-repair-status"></a><span data-ttu-id="0a6aa-111">So richten Sie einen Reparaturstatus ein</span><span class="sxs-lookup"><span data-stu-id="0a6aa-111">To set up a repair status</span></span>  
1. <span data-ttu-id="0a6aa-112">Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Reparaturstatus** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="0a6aa-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Repair Status**, and then choose the related link.</span></span> <span data-ttu-id="0a6aa-113">2.</span><span class="sxs-lookup"><span data-stu-id="0a6aa-113">2.</span></span> <span data-ttu-id="0a6aa-114">Erstellen Sie einen neuen Reparaturstatus.</span><span class="sxs-lookup"><span data-stu-id="0a6aa-114">Create a new repair status.</span></span>  
3. <span data-ttu-id="0a6aa-115">Füllen Sie die Felder **Code** und **Beschreibung** aus.</span><span class="sxs-lookup"><span data-stu-id="0a6aa-115">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="0a6aa-116">Wählen Sie im **Serviceauftragsstatus** Feld den Auftragsstatus aus, mit dem der Reparaturstatus verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="0a6aa-116">In the **Service Order Status** field, choose the order status to link the repair status to.</span></span> <span data-ttu-id="0a6aa-117">Das Feld **Priorität** zeigt die Priorität des von Ihnen ausgewählten Serviceauftragsstatus.</span><span class="sxs-lookup"><span data-stu-id="0a6aa-117">The **Priority** field displays the priority of the service order status you have chosen.</span></span>  
5. <span data-ttu-id="0a6aa-118">Wählen Sie einen Reparaturstatus aus.</span><span class="sxs-lookup"><span data-stu-id="0a6aa-118">Choose a repair status.</span></span> <span data-ttu-id="0a6aa-119">Sie können nur einen auswählen.</span><span class="sxs-lookup"><span data-stu-id="0a6aa-119">You can choose only one.</span></span>  
6. <span data-ttu-id="0a6aa-120">Um Serviceverträge, einschließlich Serviceartikel, mit diesem Reparaturstatus buchen zu können, wählen Sie das Feld **Buchen zulassen** aus.</span><span class="sxs-lookup"><span data-stu-id="0a6aa-120">To be able to post service orders, including service items, with this repair status, choose the **Posting Allowed** field.</span></span>  
7. <span data-ttu-id="0a6aa-121">Um die Serviceauftragsstatusoption in Serviceaufträgen, die Serviceartikel mit diesem Reparaturstatus enthalten, manuell auf **Offen** ändern zu können, wählen Sie das Kontrollkästchen **Status Offen zulassen** aus.</span><span class="sxs-lookup"><span data-stu-id="0a6aa-121">To be able to manually change the service order status option to **Pending** in service orders including service items with this repair status, choose the **Pending Status Allowed** check box.</span></span>  
8. <span data-ttu-id="0a6aa-122">Wählen Sie die Kontrollkästchen **Status in Bearbeitung zulassen**, **Status Erledigt zulassen**und **Status Warten zulassen** auf die gleiche Weise aus.</span><span class="sxs-lookup"><span data-stu-id="0a6aa-122">Choose the **In Process Status Allowed**, **Finished Status Allowed**, and **On Hold Status Allowed** check boxes in the same way.</span></span>
  
## <a name="to-set-up-service-status-priorities"></a><span data-ttu-id="0a6aa-123">So richten Sie Servicestatusprioritäten ein</span><span class="sxs-lookup"><span data-stu-id="0a6aa-123">To set up service status priorities</span></span>  
1. <span data-ttu-id="0a6aa-124">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Serviceauftragsstatus** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="0a6aa-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Order Status**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0a6aa-125">Wählen Sie den Serviceauftragsstatus aus, für den Sie eine Priorität festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="0a6aa-125">Select the service order status you want to set a priority for.</span></span>  
3. <span data-ttu-id="0a6aa-126">Wählen Sie im Feld **Priorität**die Priorität aus, die Sie diesem Serviceauftragsstatus zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="0a6aa-126">In the **Priority** field, choose the priority you want for this service order status.</span></span> <span data-ttu-id="0a6aa-127">Wiederholen Sie diesen Schritt für jeden Status.</span><span class="sxs-lookup"><span data-stu-id="0a6aa-127">Repeat this step for each status.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0a6aa-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a6aa-128">See Also</span></span>  
[<span data-ttu-id="0a6aa-129">Serviceauftragsstatus und Reparaturstatus</span><span class="sxs-lookup"><span data-stu-id="0a6aa-129">Understanding Service Order Status and Repair Status</span></span>]()  
[<span data-ttu-id="0a6aa-130">Einrichten der Serviceverwaltung</span><span class="sxs-lookup"><span data-stu-id="0a6aa-130">Setting Up Service Management</span></span>](service-setup-service.md)  

