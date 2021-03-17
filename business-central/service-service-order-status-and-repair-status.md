---
title: Serviceauftragsstatus und Reparaturstatus
description: Das Feld "Status" auf der Seite "Serviceauftrag" und das Feld "Reparaturstatuscode" (der Serviceartikelreparaturstatus) auf der Seite "Serviceauftrag stellen" im Service eine bestimmte Beziehung zueinander dar. Der Serviceauftragsstatus spiegelt den Reparaturstatus aller Serviceartikel des Serviceauftrags wider.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/15/2020
ms.author: edupont
ms.openlocfilehash: b9095cbfd1b8a55f525f0a3c4dcfad6cf56fc449
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386824"
---
# <a name="service-order-status-and-repair-status"></a><span data-ttu-id="75864-104">Serviceauftragsstatus und Reparaturstatus</span><span class="sxs-lookup"><span data-stu-id="75864-104">Service Order Status and Repair Status</span></span>

<span data-ttu-id="75864-105">Das Feld **Status** auf der Seite **Serviceauftrag** und das Feld **Reparaturstatuscode** (der Serviceartikelreparaturstatus) auf der Seite **Serviceauftrag stellen** im Service eine bestimmte Beziehung zueinander dar.</span><span class="sxs-lookup"><span data-stu-id="75864-105">The **Status** field on the **Service Order** page and the service item repair status, which is represented by the **Repair Status Code** field on the **Service Order** page have a certain relationship in Service Management.</span></span> <span data-ttu-id="75864-106">Der Serviceauftragsstatus spiegelt den Reparaturstatus aller Serviceartikel des Serviceauftrags wider.</span><span class="sxs-lookup"><span data-stu-id="75864-106">The service order status reflects the repair status of all the service items in the service order.</span></span>  

> [!NOTE]  
> <span data-ttu-id="75864-107">Die beiden Felder sind nicht mit dem Feld **Freigabestatus** des Serviceauftragskopfs verbunden, der den Lagerdurchlauf von Serviceartikeln steuert.</span><span class="sxs-lookup"><span data-stu-id="75864-107">These two status field are not related to the **Release Status** field on the service order header, which determines how the warehouse handles service items.</span></span>  

<span data-ttu-id="75864-108">Wenn Sie den Reparaturstatus eines Serviceartikels in einem Serviceauftrag ändern, wird der Auftragsstatus aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="75864-108">Each time the repair status of a service item is changed in a service order, the status of the order is updated.</span></span> <span data-ttu-id="75864-109">Um den gesamten Reparaturstatus einzelner Serviceartikel anzuzeigen, müssen Sie Folgendes angeben:</span><span class="sxs-lookup"><span data-stu-id="75864-109">To display the status that reflects the overall repair status of the individual service items, you must specify the following:</span></span>  

* <span data-ttu-id="75864-110">Den Serviceauftragsstatus, mit dem jeder Reparaturstatus verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="75864-110">The service order status that each repair status is linked to.</span></span>  
* <span data-ttu-id="75864-111">Die Prioritätsstufe jeder Serviceauftragsstatus Option.</span><span class="sxs-lookup"><span data-stu-id="75864-111">The level of priority of each service order status option.</span></span>  

<span data-ttu-id="75864-112">Wenn Sie ein Serviceangebot in einen Serviceauftrag umwandeln, wird der Reparaturstatus der einzelnen Serviceartikel in dem Serviceauftrag in **Anfang** und der Serviceauftragsstatus in **Offen** geändert.</span><span class="sxs-lookup"><span data-stu-id="75864-112">When you convert a service quote to a service order, the repair status of each service item is changed in the order to **Initial** and the service order status is changed to **Pending**.</span></span>  

> [!NOTE]
> <span data-ttu-id="75864-113">Bevor Sie einen Serviceauftrag einrichten können, müssen Sie die Prioritäten für den Reparaturstatus festlegen.</span><span class="sxs-lookup"><span data-stu-id="75864-113">Before you can create service orders, you must set up repair statuses and service status priorities.</span></span> <span data-ttu-id="75864-114">Weitere Informationen finden Sie unter [Serviceauftrag und Reparaturstatus einrichten](service-order-repair-status.md).</span><span class="sxs-lookup"><span data-stu-id="75864-114">For more information, see [Set Up Statuses for Service Orders and Repairs](service-order-repair-status.md).</span></span>

## <a name="specifying-service-order-status-for-repair-status"></a><span data-ttu-id="75864-115">Serviceauftragsstatus für Reparaturstatusoptionen festlegen</span><span class="sxs-lookup"><span data-stu-id="75864-115">Specifying Service Order Status for Repair Status</span></span>

<span data-ttu-id="75864-116">Jeder Reparaturstatus ist mit einem bestimmten Serviceauftragsstatus verknüpft.</span><span class="sxs-lookup"><span data-stu-id="75864-116">Each repair status is linked to a particular service order status.</span></span> <span data-ttu-id="75864-117">Folgende Optionen stehen für den Serviceauftragsstatus zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="75864-117">The options for the service order status are as follows:</span></span>

* <span data-ttu-id="75864-118">**"Offen"**</span><span class="sxs-lookup"><span data-stu-id="75864-118">**Pending**</span></span>
* <span data-ttu-id="75864-119">**In Bearbeitung**</span><span class="sxs-lookup"><span data-stu-id="75864-119">**In Process**</span></span>
* <span data-ttu-id="75864-120">**Abwarten**</span><span class="sxs-lookup"><span data-stu-id="75864-120">**On Hold**</span></span>
* <span data-ttu-id="75864-121">**Erledigt**</span><span class="sxs-lookup"><span data-stu-id="75864-121">**Finished**</span></span>

<span data-ttu-id="75864-122">Die Reparaturstatusoptionen sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="75864-122">The repair status options are as follows:</span></span>

* <span data-ttu-id="75864-123">**Anfang**</span><span class="sxs-lookup"><span data-stu-id="75864-123">**Initial**</span></span>
* <span data-ttu-id="75864-124">**In Bearbeitung**</span><span class="sxs-lookup"><span data-stu-id="75864-124">**In Process**</span></span>
* <span data-ttu-id="75864-125">**Weitergeleitet**</span><span class="sxs-lookup"><span data-stu-id="75864-125">**Referred**</span></span>
* <span data-ttu-id="75864-126">**Unvollständig bearbeitet**</span><span class="sxs-lookup"><span data-stu-id="75864-126">**Partly Serviced**</span></span>
* <span data-ttu-id="75864-127">**Angebot erstellt**</span><span class="sxs-lookup"><span data-stu-id="75864-127">**Quote Finished**</span></span>
* <span data-ttu-id="75864-128">**Warten auf Debitor**</span><span class="sxs-lookup"><span data-stu-id="75864-128">**Waiting for Customer**</span></span>
* <span data-ttu-id="75864-129">**Ersatzteil bestellt**</span><span class="sxs-lookup"><span data-stu-id="75864-129">**Spare Part Ordered**</span></span>
* <span data-ttu-id="75864-130">**Ersatzteil erhalten**</span><span class="sxs-lookup"><span data-stu-id="75864-130">**Spare Part Received**</span></span>
* <span data-ttu-id="75864-131">**Erledigt**</span><span class="sxs-lookup"><span data-stu-id="75864-131">**Finished**</span></span>  

### <a name="pending"></a><span data-ttu-id="75864-132">"Offen"</span><span class="sxs-lookup"><span data-stu-id="75864-132">Pending</span></span>

<span data-ttu-id="75864-133">Der Serviceauftragsstatus **Offen** gibt an, dass der Service jederzeit beginnen oder fortgesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="75864-133">The service order status **Pending** indicates that the service can start or continue at any time.</span></span> <span data-ttu-id="75864-134">Aus diesem Grunde können die vier Reparaturstatusoptionen **Anfang**, **Weitergeleitet**, **Unvollständig bearbeitet** und **Ersatzteil erhalten** mit diesem Serviceauftragsstatus verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="75864-134">Therefore, the repair status options of **Initial**, **Referred**, **Partly Serviced**, and **Spare Part Received** can be linked to this service order status.</span></span>  

### <a name="in-process"></a><span data-ttu-id="75864-135">"In Bearbeitung"</span><span class="sxs-lookup"><span data-stu-id="75864-135">In Process</span></span>

<span data-ttu-id="75864-136">Der Serviceauftragsstatus **In Bearbeitung** gibt an, dass der Service in Bearbeitung ist.</span><span class="sxs-lookup"><span data-stu-id="75864-136">The service order status **In Process** indicates that the service is in process.</span></span> <span data-ttu-id="75864-137">Aus diesem Grunde können die zwei Reparaturstatusoptionen **In Bearbeitung** und **Ersatzteil bestellt** mit diesem Serviceauftragsstatus verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="75864-137">Therefore, the repair status options **In Process** and **Spare Part Ordered** can both be linked to this service order status.</span></span> <span data-ttu-id="75864-138">Wenn Sie den Status **Ersatzteil bestellt** mit dem Serviceauftragsstatus **In Bearbeitung** verknüpfen, müssen Sie auch den Status **Ersatzteil erhalten** mit diesem Serviceauftragsstatus verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="75864-138">If you link the **Spare Part Ordered** status to an **In Process** service order status, you must also link the **Spare Part Received** status to this service order status.</span></span>  

### <a name="on-hold"></a><span data-ttu-id="75864-139">Warten</span><span class="sxs-lookup"><span data-stu-id="75864-139">On Hold</span></span>

<span data-ttu-id="75864-140">Der Serviceauftragsstatus **Warten** gibt an, dass der Service zeitweilig gesperrt ist, da Sie auf die Antwort eines Debitors oder auf Ersatzteile warten, bevor der Service gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="75864-140">The service order status **On Hold** indicates that the service is temporarily on hold because you are waiting for a customer response or spare parts before the service can start.</span></span> <span data-ttu-id="75864-141">Aus diesem Grunde können die drei Reparaturstatusoptionen **Angebot erstellt**, **Ersatzteil bestellt** und **Warten auf Debitor** mit diesem Serviceauftragsstatus verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="75864-141">Therefore, the repair status options of **Quote Finished**, **Spare Part Ordered**, and **Waiting for Customer** can be linked to this service order status.</span></span>  

### <a name="finished"></a><span data-ttu-id="75864-142">"Erledigt"</span><span class="sxs-lookup"><span data-stu-id="75864-142">Finished</span></span>

<span data-ttu-id="75864-143">Der Serviceauftragsstatus **Erledigt** gibt an, dass der Service abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="75864-143">The service order status **Finished** indicates that the service has been completed.</span></span> <span data-ttu-id="75864-144">Deshalb wird der Reparaturstatus **Erledigt** mit diesem Status verknüpft.</span><span class="sxs-lookup"><span data-stu-id="75864-144">Therefore, the **Finished** repair status is linked to this status.</span></span>  

## <a name="assigning-priority-to-service-order-status"></a><span data-ttu-id="75864-145">Einem Serviceauftragsstatus eine Priorität zuordnen</span><span class="sxs-lookup"><span data-stu-id="75864-145">Assigning Priority to Service Order Status</span></span>

<span data-ttu-id="75864-146">Wenn der Reparaturstatus eines Serviceartikels geändert wird, werden die Serviceauftragsstatusoptionen, die mit den verschiedenen Reparaturstatusoptionen aller Serviceartikel des Auftrags verknüpft sind, identifiziert.</span><span class="sxs-lookup"><span data-stu-id="75864-146">When a repair status of a service item is changed, the service order status options linked to the different repair status options of all the service items in the order are identified.</span></span> <span data-ttu-id="75864-147">Sind die Serviceartikel mit zwei oder mehr Serviceauftragsstatusoptionen verknüpft, wird der Serviceauftragsstatus mit der höchsten Priorität ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="75864-147">If the service items are linked to two or more service order status options, the service order status option with the highest priority is selected.</span></span>  

<span data-ttu-id="75864-148">Sie müssen entscheiden, welcher Serviceauftragsstatus die wichtigsten Informationen über den Status des Serviceauftrages enthält und diesen Status mit der höchsten Priorität verbinden usw.</span><span class="sxs-lookup"><span data-stu-id="75864-148">You must decide which service order status contains the most important information about the status of the service order and assign that status the highest priority, and so on.</span></span>  

<span data-ttu-id="75864-149">Wenn Sie dann einen neuen Serviceauftrag erstellen und Serviceartikel hinzufügen, wird das Feld **Priorität** im Serviceauftragskopf basierend auf den Prioritäten der Serviceartikel aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="75864-149">Then, when you create a new service order and you add service items to it, the **Priority** field on the service order header is updated based on the priorities on the service items.</span></span>  

### <a name="example"></a><span data-ttu-id="75864-150">Beispiel</span><span class="sxs-lookup"><span data-stu-id="75864-150">Example</span></span>

<span data-ttu-id="75864-151">Eine typische Zuordnung von Prioritätsstufen könnte folgendermaßen aussehen:</span><span class="sxs-lookup"><span data-stu-id="75864-151">A typical priority level assignment could be as follows:</span></span>  

* <span data-ttu-id="75864-152">"In Bearbeitung" - Sehr hoch</span><span class="sxs-lookup"><span data-stu-id="75864-152">In Process - High</span></span>  
* <span data-ttu-id="75864-153">"Offen" - Hoch</span><span class="sxs-lookup"><span data-stu-id="75864-153">Pending - Medium high</span></span>  
* <span data-ttu-id="75864-154">"Warten" - Niedrig</span><span class="sxs-lookup"><span data-stu-id="75864-154">On Hold - Medium low</span></span>  
* <span data-ttu-id="75864-155">"Erledigt" - Sehr niedrig</span><span class="sxs-lookup"><span data-stu-id="75864-155">Finished - Low</span></span>  

<span data-ttu-id="75864-156">Wenn ein Serviceartikel z. B. den Status **Anfang** hat (verbunden mit dem Serviceauftragsstatus **Warten**), einer den Reparaturstatus **In Bearbeitung** (verbunden mit dem Serviceauftragsstatus **In Bearbeitung**) und ein dritter den Reparaturstatus **Ersatzteil bestellt** (verbunden mit dem Serviceauftragsstatus **Warten**), ist der Auftragsstatus dann **In Bearbeitung**, weil er die höchste Priorität hat.</span><span class="sxs-lookup"><span data-stu-id="75864-156">For example, if one service item has the repair status **Initial**, linked to the service order status **Pending**, another has the repair status **In Process**, linked to the service order status **In Process**, and a third has the repair status **Spare Part Ordered**, linked to the service order status **On Hold**, the resulting service order status will be **In Process** because this has the highest priority.</span></span>  

## <a name="see-also"></a><span data-ttu-id="75864-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75864-157">See Also</span></span>

[<span data-ttu-id="75864-158">Einrichten von Status für Serviceaufträge und Reparaturen</span><span class="sxs-lookup"><span data-stu-id="75864-158">Set Up Statuses for Service Orders and Repairs</span></span>](service-order-repair-status.md)  
[<span data-ttu-id="75864-159">Einrichten der Serviceverwaltung</span><span class="sxs-lookup"><span data-stu-id="75864-159">Setting Up Service Management</span></span>](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]