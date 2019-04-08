---
title: Terminberechnung für Verkäufe  | Microsoft Docs
description: Das Programm berechnet automatisch das Datum, an dem Sie einen Artikel bestellen müssen, damit er zu einem bestimmten Datum im Lagerbestand vorhanden ist. Dies ist das Datum, an dem Sie erwarten können, dass Artikel, die an einem bestimmten Datum bestellt wurden, zur Kommissionierung verfügbar sind.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 7de382530c1872155903bfa015866cf99a9f5566
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "798577"
---
# <a name="date-calculation-for-sales"></a><span data-ttu-id="ba1e9-104">Terminberechnung für Verkäufe</span><span class="sxs-lookup"><span data-stu-id="ba1e9-104">Date Calculation for Sales</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="ba1e9-105">berechnet automatisch das frühestmögliche Datum, an dem ein Artikel in einer Verkaufsauftragszeile geliefert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ba1e9-105">automatically calculates the earliest possible date that an item on a sales order line can be shipped.</span></span>

<span data-ttu-id="ba1e9-106">Wenn der Debitor ein bestimmtes Lieferdatum wünscht, wird das Datum berechnet, an dem die Artikel für die Kommissionierung zur Verfügung stehen müssen, damit dieser Liefertermin eingehalten werden kann.</span><span class="sxs-lookup"><span data-stu-id="ba1e9-106">If the customer has requested a specific delivery date, then the date on which the items must be available to pick to meet that delivery date is calculated.</span></span>

<span data-ttu-id="ba1e9-107">Falls der Debitor kein bestimmtes Lieferdatum wünscht, wird das Datum berechnet, an dem die Artikel geliefert werden können, ausgehend von dem Datum, an dem die Artikel für die Kommissionierung zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="ba1e9-107">If the customer does not request a specific delivery date, then the date on which the items can be delivered is calculated, starting from the date on which the items are available for picking.</span></span>

## <a name="calculating-a-requested-delivery-date"></a><span data-ttu-id="ba1e9-108">So berechnen Sie ein gewünschtes Wareneingangsdatum:</span><span class="sxs-lookup"><span data-stu-id="ba1e9-108">Calculating a Requested Delivery Date</span></span>
<span data-ttu-id="ba1e9-109">Wenn Sie in einer Verkaufszeile ein gewünschtes Lieferdatum eingeben, wird dieses Datum als Ausgangspunkt für die folgenden Berechnungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ba1e9-109">If you specify a requested delivery date on the sales order line, then that date is used as the starting point for the following calculations.</span></span>

- <span data-ttu-id="ba1e9-110">Gewünschtes Lieferdatum - Transportzeit = Geplantes Warenausgangsdatum</span><span class="sxs-lookup"><span data-stu-id="ba1e9-110">requested delivery date - shipping time = planned shipment date</span></span>
- <span data-ttu-id="ba1e9-111">Geplantes Warenausgangsdatum - Ausgeh. Lagerdurchlaufzeit = Warenausgangsdatum</span><span class="sxs-lookup"><span data-stu-id="ba1e9-111">planned shipment date - outbound whse. handling time = shipment date</span></span>

<span data-ttu-id="ba1e9-112">Falls die Artikel am Lieferdatum zur Kommissionierung zur Verfügung stehen, kann der Verkaufsvorgang fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="ba1e9-112">If the items are available to pick on the shipment date, then the sales process can continue.</span></span>

<span data-ttu-id="ba1e9-113">Falls die Artikel am Lieferdatum nicht zur Kommissionierung zur Verfügung stehen, erscheint eine Warnmeldung die auf diesen Umstand hinweist.</span><span class="sxs-lookup"><span data-stu-id="ba1e9-113">If the items are not available to be picked on the shipment date, then a stock-out warning is displayed.</span></span>

## <a name="calculating-the-earliest-possible-delivery-date"></a><span data-ttu-id="ba1e9-114">So berechnen Sie das frühestmögliche Lieferdatum:</span><span class="sxs-lookup"><span data-stu-id="ba1e9-114">Calculating the Earliest Possible Delivery Date</span></span>
<span data-ttu-id="ba1e9-115">Wenn Sie kein angefordertes Lieferdatum auf der Verkaufsauftragszeile angeben oder das angeforderte Lieferdatum nicht eingehalten werden kann, wird das früheste Datum, an dem die Artikel verfügbar sind, berechnet.</span><span class="sxs-lookup"><span data-stu-id="ba1e9-115">If you do not specify a requested delivery date on the sales order line, or if the requested delivery date cannot be met, then the earliest date on which that the items are available is calculated.</span></span> <span data-ttu-id="ba1e9-116">Dieses Datum wird dann im Feld Versanddatum auf der Zeile eingegeben, und das Datum, an dem Sie planen, die Artikel zu liefern, sowie das Datum, an dem Sie an den Kunden ausgeliefert werden, werden anhand der nachfolgenden Formeln berechnet.</span><span class="sxs-lookup"><span data-stu-id="ba1e9-116">That date is then entered in the Shipment Date field on the line, and the date on which you plan to ship the items as well as the date on which they will be delivered to the customer are calculated using the following formulas.</span></span>

- <span data-ttu-id="ba1e9-117">Warenausgangsdatum + Ausgeh. Lagerdurchlaufzeit = Geplantes Warenausgangsdatum</span><span class="sxs-lookup"><span data-stu-id="ba1e9-117">shipment date + outbound whse. handling time = planned shipment date</span></span>
- <span data-ttu-id="ba1e9-118">Geplantes Warenausgangsdatum + Transportzeit = Geplantes Lieferdatum</span><span class="sxs-lookup"><span data-stu-id="ba1e9-118">planned shipment date + shipping time = planned delivery date</span></span>


## <a name="see-also"></a><span data-ttu-id="ba1e9-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba1e9-119">See Also</span></span>  
 <span data-ttu-id="ba1e9-120">[Terminberechnung für Einkäufe](purchasing-date-calculation-for-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="ba1e9-120">[Date Calculation for Purchases](purchasing-date-calculation-for-purchases.md) </span></span>  
 [<span data-ttu-id="ba1e9-121">Lieferterminzusagen-Daten berechnen</span><span class="sxs-lookup"><span data-stu-id="ba1e9-121">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="ba1e9-122">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ba1e9-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
