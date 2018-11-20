---
title: 'Designdetails: Die Rolle des Zeitrahmens | Microsoft Docs'
description: Der Zweck dieses Zeitrahmens ist, Bedarfsereignisse innerhalb des Zeitfensters zu erfassen, um einen gemeinsamen Beschaffungsauftrag zu erstellen.
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
redirect_url: design-details-handling-reordering-policies
ms.translationtype: HT
ms.sourcegitcommit: 67400e424305cc705db5c1bd52a8e4de17ecc5a9
ms.openlocfilehash: 2edbbb5caa74216ece64f093f6323446f04fa1d7
ms.contentlocale: de-de
ms.lasthandoff: 11/20/2018

---
# <a name="design-details-the-role-of-the-time-bucket"></a><span data-ttu-id="2497a-103">Designdetails: Die Rolle des Zeitrahmens</span><span class="sxs-lookup"><span data-stu-id="2497a-103">Design Details: The Role of the Time Bucket</span></span>
<span data-ttu-id="2497a-104">Der Zweck dieses Zeitrahmens ist, Bedarfsereignisse innerhalb des Zeitfensters zu erfassen, um einen gemeinsamen Beschaffungsauftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2497a-104">The purpose of the time bucket is to collect demand events within the time window in order to make a joint supply order.</span></span>  

 <span data-ttu-id="2497a-105">Für Wiederbeschaffungsverfahren, die einen Minimalbestand verwenden, können Sie einen Zeitrahmen definieren.</span><span class="sxs-lookup"><span data-stu-id="2497a-105">For reordering policies that use a reorder point, you can define a time bucket.</span></span> <span data-ttu-id="2497a-106">Dadurch ist sichergestellt, dass Bedarf innerhalb derselben Periode kumuliert wird, bevor die Auswirkungen auf den voraussichtlichen Lagerbestand geprüft werden, und ob der Minimalbestand unterschritten wurde.</span><span class="sxs-lookup"><span data-stu-id="2497a-106">This ensures that demand within the same time period is accumulated before checking the impact on the projected inventory and whether the reorder point has been passed.</span></span> <span data-ttu-id="2497a-107">Wenn der Minimalbestand überschritten wird, wird ein neuer Beschaffungsauftrag vom Ende der durch den Zeitrahmen definierten Periode vorwärts geplant.</span><span class="sxs-lookup"><span data-stu-id="2497a-107">If the reorder point is passed, a new supply order is scheduled forward from the end of the period defined by the time bucket.</span></span> <span data-ttu-id="2497a-108">Der Zeitrahmen beginnt am geplanten Startdatum.</span><span class="sxs-lookup"><span data-stu-id="2497a-108">The time buckets begin on the planning starting date.</span></span>  

 <span data-ttu-id="2497a-109">Der Zeitrahmenkonzept spiegelt den manuellen Vorgang des Überprüfens des Lagerbestands auf häufiger Basis anstatt für jede Transaktion.</span><span class="sxs-lookup"><span data-stu-id="2497a-109">The time-bucketed concept reflects the manual process of checking the inventory level on a frequent basis rather than for each transaction.</span></span> <span data-ttu-id="2497a-110">Die Anwender muss die Häufigkeit (den Zeitrahmen) festlegen.</span><span class="sxs-lookup"><span data-stu-id="2497a-110">The user needs to define the frequency (the time bucket).</span></span> <span data-ttu-id="2497a-111">Beispielsweise erfasst der Benutzer alle Artikelanforderungen von einem Kreditor, um einen wöchentlichen Auftrag zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="2497a-111">For example, the user gathers all item needs from one vendor to place a weekly order.</span></span>  

 <span data-ttu-id="2497a-112">![Beispiel des Zeitrahmens in der Planung](media/nav_app_supply_planning_2_reorder_cycle.png "Beispiel des Zeitrahmens in der Planung")</span><span class="sxs-lookup"><span data-stu-id="2497a-112">![Example of time bucket in planning](media/nav_app_supply_planning_2_reorder_cycle.png "Example of time bucket in planning")</span></span>  

 <span data-ttu-id="2497a-113">Das Zeitrahmen wird im Allgemeinen verwendet, um einen Kaskadeneffekt zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="2497a-113">The time bucket is generally used to avoid a cascade effect.</span></span> <span data-ttu-id="2497a-114">Zum Beispiel eine eine ausgeglichene Zeile von Bedarf und Vorrat, bei der ein frühzeitiger Bedarf storniert oder ein neuer Bedarf erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2497a-114">For example, a balanced row of demand and supply where an early demand is canceled, or a new one is created.</span></span> <span data-ttu-id="2497a-115">Das Ergebnis würde sein, dass jeder Beschaffungsauftrag (mit Ausnahme des letzten) umgeplant würde.</span><span class="sxs-lookup"><span data-stu-id="2497a-115">The result would be that every supply order (except the last one) is rescheduled.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2497a-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2497a-116">See Also</span></span>  
 <span data-ttu-id="2497a-117">[Designdetails: Wiederbeschaffungsverfahren](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="2497a-117">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="2497a-118">[Designdetails: Planungsparameter](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="2497a-118">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="2497a-119">[Designdetails: Umgang mit Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="2497a-119">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="2497a-120">Designdetails: Vorratsplanung</span><span class="sxs-lookup"><span data-stu-id="2497a-120">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

