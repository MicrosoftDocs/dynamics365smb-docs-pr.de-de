---
title: Designdetails - Maximale Menge | Microsoft Docs
description: Die Richtlinie der maximalen Menge ist eine Möglichkeit zur Verwaltung des Bestands anhand eines Minimalbestands.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 857a01bac28d85a35668f3aa01e8807a6f6dc845
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "936647"
---
# <a name="design-details-maximum-qty"></a><span data-ttu-id="4effe-103">Designdetails: Höchstmenge</span><span class="sxs-lookup"><span data-stu-id="4effe-103">Design Details: Maximum Qty.</span></span>
<span data-ttu-id="4effe-104">Die Richtlinie der maximalen Menge ist eine Möglichkeit zur Verwaltung des Bestands anhand eines Minimalbestands.</span><span class="sxs-lookup"><span data-stu-id="4effe-104">The Maximum Quantity policy is a way to maintain inventory using a reorder point.</span></span>  

 <span data-ttu-id="4effe-105">Alles im Zusammenhang mit der festen Bestellmengenrichtlinie bezieht sich auch auf diese Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="4effe-105">Everything regarding the Fixed Reorder Qty. policy also applies to this policy.</span></span> <span data-ttu-id="4effe-106">Der einzige Unterschied ist die Menge des vorgeschlagenen Vorrats.</span><span class="sxs-lookup"><span data-stu-id="4effe-106">The only difference is the quantity of the suggested supply.</span></span> <span data-ttu-id="4effe-107">Wenn Sie die Methode Auffüllen auf Maximalbestand verwenden, erfolgt die Definition der Bestellmenge dynamisch auf Basis des voraussichtlichen Lagerbestandes und unterscheidet sich daher normalerweise von Auftrag zu Auftrag.</span><span class="sxs-lookup"><span data-stu-id="4effe-107">When using the maximum quantity policy, the reorder quantity will be defined dynamically based on the projected inventory level and will therefore usually differ from order to order.</span></span>  

## <a name="calculated-per-time-bucket"></a><span data-ttu-id="4effe-108">Berechnet pro Zeitrahmen</span><span class="sxs-lookup"><span data-stu-id="4effe-108">Calculated per Time Bucket</span></span>  
 <span data-ttu-id="4effe-109">Die Nachbestellungsmenge wird zu dem Zeitpunkt bestimmt (am Ende eines Zeitrahmens), wenn das Planungssystem erkennt, dass der Minimalbestand überschritten wurde.</span><span class="sxs-lookup"><span data-stu-id="4effe-109">The reorder quantity is determined at the point of time (the end of a time bucket) when the planning system detects that the reorder point has been crossed.</span></span> <span data-ttu-id="4effe-110">Zu diesem Zeitpunkt misst das System die Lücke von der aktuellen Stufe des voraussichtlichen Lagerbestands bis zum angegebenen Maximalbestand.</span><span class="sxs-lookup"><span data-stu-id="4effe-110">At this time, the system measures the gap from the current projected inventory level up to the specified maximum inventory.</span></span> <span data-ttu-id="4effe-111">Dies bildet die Menge, die wiederbestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4effe-111">This constitutes the quantity that should be reordered.</span></span> <span data-ttu-id="4effe-112">Die Anwendung überprüft dann, ob Vorrat bereits anderswo bestellt worden, um innerhalb der Beschaffungszeit erhalten zu werden, und falls ja, reduziert es die Menge des neuen Beschaffungsauftrags um bereits bestellte Mengen.</span><span class="sxs-lookup"><span data-stu-id="4effe-112">The system then checks if supply has already been ordered elsewhere to be received within the lead time and, if so, reduces the quantity of the new supply order by already ordered quantities.</span></span>  

 <span data-ttu-id="4effe-113">Die Anwendung stellt sicher, dass der voraussichtliche Lagerbestand mindestens die Minimalbestandsebene erreicht - falls der Benutzer vergessen hat, eine maximale Lagerbestandsmenge anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4effe-113">The system will ensure that the projected inventory at least reaches the reorder point level – in case the user has forgotten to specify a maximum inventory quantity.</span></span>  

## <a name="combines-with-order-modifiers"></a><span data-ttu-id="4effe-114">Wird mit anderen Auftragsmodifizierern kombiniert</span><span class="sxs-lookup"><span data-stu-id="4effe-114">Combines with Order Modifiers</span></span>  
 <span data-ttu-id="4effe-115">Abhängig von den Einstellungen kann es am besten sein, die Methode „Maximale Menge“ mit Auftragsmodifikationen zu kombinieren, um eine Mindestauftragsmenge sicherzustellen, oder sie auf eine ganze Zahl von Einkaufsmengeneinheiten zu runden, bzw. sie in mehrere Chargen aufzuteilen, wie von der maximalen Auftragsmenge definiert.</span><span class="sxs-lookup"><span data-stu-id="4effe-115">Depending on the setup, it may be best to combine the Maximum Quantity policy with order modifiers to ensure a minimum order quantity or round it to an integer number of purchase units of measure, or split it into more lots as defined by the maximum order quantity.</span></span>  

## <a name="combines-with-calendars"></a><span data-ttu-id="4effe-116">Zusammenfassen mit Kalendern</span><span class="sxs-lookup"><span data-stu-id="4effe-116">Combines with Calendars</span></span>  
 <span data-ttu-id="4effe-117">Bevor ein neuer Beschaffungsauftrag vorgeschlagen wird, einen Minimalbestand einzuhalten, überprüft das Planungssystem, ob der Auftrag für einen nicht freien Tag entsprechend dem Kalender geplant ist, die im Feld **Basiskalendercode** auf den Seiten **Firmendaten** und **Lagerortkarten** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4effe-117">Before suggesting a new supply order to meet a reorder point, the planning system checks if the order is scheduled for a non-working day, according to any calendars that are  defined in the **Base Calendar Code** field in the **Company Information** and **Location Card** pages.</span></span>  

 <span data-ttu-id="4effe-118">Wenn das geplante Datum ein freier Tag ist, verschiebt das Planungssystem die Reihenfolge weiter zum nächsten Arbeitsdatum.</span><span class="sxs-lookup"><span data-stu-id="4effe-118">If the scheduled date is a non-working day, the planning system moves the order forward to the nearest working date.</span></span> <span data-ttu-id="4effe-119">Dadurch ergeben sich möglicherweise ein Verkaufsauftrag, der für einen Minimalbestand gilt, aber keinen bestimmten Bedarf abdeckt.</span><span class="sxs-lookup"><span data-stu-id="4effe-119">This may result in an order that meets a reorder point but does not meet some specific demand.</span></span> <span data-ttu-id="4effe-120">Bei solcher Nachfrage ohne Bedarf erstellt das Planungssystem ein zusätzlicher Vorrat.</span><span class="sxs-lookup"><span data-stu-id="4effe-120">For such unbalanced demand, the planning system creates an extra supply.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4effe-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4effe-121">See Also</span></span>  
 <span data-ttu-id="4effe-122">[Designdetails: Wiederbeschaffungsverfahren](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="4effe-122">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="4effe-123">[Designdetails: Planungsparameter](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="4effe-123">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="4effe-124">[Designdetails: Umgang mit Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="4effe-124">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="4effe-125">Designdetails: Vorratsplanung</span><span class="sxs-lookup"><span data-stu-id="4effe-125">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
