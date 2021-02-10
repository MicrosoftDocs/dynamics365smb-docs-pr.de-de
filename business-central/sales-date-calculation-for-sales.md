---
title: Terminberechnung für Verkäufe | Microsoft Docs
description: Die Anwendung berechnet automatisch das Datum, an dem Sie einen Artikel bestellen müssen, damit er zu einem bestimmten Datum im Lagerbestand vorhanden ist. Dies ist das Datum, an dem Sie erwarten können, dass Artikel, die an einem bestimmten Datum bestellt wurden, zur Kommissionierung verfügbar sind.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 26782d211d205bb5414c5bd423ccf240f70f197e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748468"
---
# <a name="date-calculation-for-sales"></a><span data-ttu-id="a9b88-104">Terminberechnung für Verkäufe</span><span class="sxs-lookup"><span data-stu-id="a9b88-104">Date Calculation for Sales</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="a9b88-105">berechnet automatisch das frühestmögliche Datum, an dem ein Artikel in einer Verkaufsauftragszeile geliefert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a9b88-105">automatically calculates the earliest possible date that an item on a sales order line can be shipped.</span></span>

<span data-ttu-id="a9b88-106">Wenn der Debitor ein bestimmtes Lieferdatum wünscht, wird das Datum berechnet, an dem die Artikel für die Kommissionierung zur Verfügung stehen müssen, damit dieser Liefertermin eingehalten werden kann.</span><span class="sxs-lookup"><span data-stu-id="a9b88-106">If the customer has requested a specific delivery date, then the date on which the items must be available to pick to meet that delivery date is calculated.</span></span>

<span data-ttu-id="a9b88-107">Falls der Debitor kein bestimmtes Lieferdatum wünscht, wird das Datum berechnet, an dem die Artikel geliefert werden können, ausgehend von dem Datum, an dem die Artikel für die Kommissionierung zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="a9b88-107">If the customer does not request a specific delivery date, then the date on which the items can be delivered is calculated, starting from the date on which the items are available for picking.</span></span>

## <a name="calculating-a-requested-delivery-date"></a><span data-ttu-id="a9b88-108">So berechnen Sie ein gewünschtes Wareneingangsdatum:</span><span class="sxs-lookup"><span data-stu-id="a9b88-108">Calculating a Requested Delivery Date</span></span>
<span data-ttu-id="a9b88-109">Wenn Sie in einer Verkaufszeile ein gewünschtes Lieferdatum eingeben, wird dieses Datum dann als Ausgangspunkt für die folgenden Berechnungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="a9b88-109">If you specify a requested delivery date on the sales order line, that date becomes the starting point for the following calculations.</span></span>

- <span data-ttu-id="a9b88-110">Gewünschtes Lieferdatum - Transportzeit = Geplantes Warenausgangsdatum</span><span class="sxs-lookup"><span data-stu-id="a9b88-110">requested delivery date - shipping time = planned shipment date</span></span>
- <span data-ttu-id="a9b88-111">Geplantes Warenausgangsdatum - Ausgeh. Lagerdurchlaufzeit = Warenausgangsdatum</span><span class="sxs-lookup"><span data-stu-id="a9b88-111">planned shipment date - outbound whse. handling time = shipment date</span></span>

<span data-ttu-id="a9b88-112">Falls die Artikel am Lieferdatum zur Kommissionierung zur Verfügung stehen, kann der Verkaufsvorgang fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="a9b88-112">If the items are available to pick on the shipment date, then the sales process can continue.</span></span> <span data-ttu-id="a9b88-113">Andernfalls wird eine Bestandswarnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a9b88-113">Otherwise, a stock-out warning is displayed.</span></span>

> [!Note]
> <span data-ttu-id="a9b88-114">Wenn Ihr Prozess auf einer Rückwärtsberechnung basiert, wenn Sie beispielsweise das angeforderte Lieferdatum verwenden, um das geplante Versanddatum zu erhalten, empfehlen wir, Datumsformeln mit fester Dauer zu verwenden, z. B. 5D für fünf Tage oder 1W für eine Woche.</span><span class="sxs-lookup"><span data-stu-id="a9b88-114">If your process is based on backward calculation, for example, if you use the requested delivery date to get the planned shipment date, we recommend that you use date formulas that have fixed durations, such as "5D" for five days or "1W" for one week.</span></span> <span data-ttu-id="a9b88-115">Datumsformeln ohne feste Dauer, wie „CW“ für die aktuelle Woche oder CM für den aktuellen Monat, können zu falschen Datumsberechnungen führen.</span><span class="sxs-lookup"><span data-stu-id="a9b88-115">Date formulas without fixed durations, such as "CW" for current week or CM for current month, can result in incorrect date calculations.</span></span> <span data-ttu-id="a9b88-116">Weitere Informationen zu Datumsformeln finden Sie unter [Arbeiten mit Kalenderdaten und -zeiten](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="a9b88-116">For more information about date formulas, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

## <a name="calculating-the-earliest-possible-delivery-date"></a><span data-ttu-id="a9b88-117">So berechnen Sie das frühestmögliche Lieferdatum:</span><span class="sxs-lookup"><span data-stu-id="a9b88-117">Calculating the Earliest Possible Delivery Date</span></span>
<span data-ttu-id="a9b88-118">Wenn Sie kein angefordertes Lieferdatum auf der Verkaufsauftragszeile angeben oder das angeforderte Lieferdatum nicht eingehalten werden kann, wird das früheste Datum, an dem die Artikel verfügbar sind, berechnet.</span><span class="sxs-lookup"><span data-stu-id="a9b88-118">If you do not specify a requested delivery date on the sales order line, or if the requested delivery date cannot be met, then the earliest date on which that the items are available is calculated.</span></span> <span data-ttu-id="a9b88-119">Dieses Datum wird dann im Feld Versanddatum auf der Zeile eingegeben, und das Datum, an dem Sie planen, die Artikel zu liefern, sowie das Datum, an dem Sie an den Kunden ausgeliefert werden, werden anhand der nachfolgenden Formeln berechnet.</span><span class="sxs-lookup"><span data-stu-id="a9b88-119">That date is then entered in the Shipment Date field on the line, and the date on which you plan to ship the items as well as the date on which they will be delivered to the customer are calculated using the following formulas.</span></span>

- <span data-ttu-id="a9b88-120">Warenausgangsdatum + Ausgeh. Lagerdurchlaufzeit = Geplantes Warenausgangsdatum</span><span class="sxs-lookup"><span data-stu-id="a9b88-120">shipment date + outbound whse. handling time = planned shipment date</span></span>
- <span data-ttu-id="a9b88-121">Geplantes Warenausgangsdatum + Transportzeit = Geplantes Lieferdatum</span><span class="sxs-lookup"><span data-stu-id="a9b88-121">planned shipment date + shipping time = planned delivery date</span></span>


## <a name="see-also"></a><span data-ttu-id="a9b88-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9b88-122">See Also</span></span>  
 <span data-ttu-id="a9b88-123">[Terminberechnung für Einkäufe](purchasing-date-calculation-for-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="a9b88-123">[Date Calculation for Purchases](purchasing-date-calculation-for-purchases.md) </span></span>  
 [<span data-ttu-id="a9b88-124">Lieferterminzusagen-Daten berechnen</span><span class="sxs-lookup"><span data-stu-id="a9b88-124">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="a9b88-125">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a9b88-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
