---
title: Terminberechnung für Einkäufe  | Microsoft Docs
description: Die Anwendung berechnet automatisch das Datum, an dem Sie einen Artikel bestellen müssen, damit er zu einem bestimmten Datum im Lagerbestand vorhanden ist. Dies ist das Datum, an dem Sie erwarten können, dass Artikel, die an einem bestimmten Datum bestellt wurden, zur Kommissionierung verfügbar sind.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 03cdb942a088b27be5c89843da4a958d0e13f843
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388274"
---
# <a name="date-calculation-for-purchases"></a><span data-ttu-id="ea3d6-104">Terminberechnung für Einkäufe</span><span class="sxs-lookup"><span data-stu-id="ea3d6-104">Date Calculation for Purchases</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="ea3d6-105">berechnet automatisch das Datum, an dem Sie einen Artikel bestellen müssen, damit er zu einem bestimmten Datum im Lagerbestand vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ea3d6-105">automatically calculates the date on which you must order an item to have it in inventory on a certain date.</span></span> <span data-ttu-id="ea3d6-106">Dies ist das Datum, an dem Sie erwarten können, dass Artikel, die an einem bestimmten Datum bestellt wurden, zur Kommissionierung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ea3d6-106">This is the date on which you can expect items ordered on a particular date to be available for picking.</span></span>  

<span data-ttu-id="ea3d6-107">Wenn Sie ein gewünschtes Wareneingangsdatum in einem Einkaufsbestellkopf angeben, ist das berechnete Auftragsdatum das Datum, an dem die Bestellung erfolgen muss, um die Artikel an dem Datum zu erhalten, das Sie angefordert haben.</span><span class="sxs-lookup"><span data-stu-id="ea3d6-107">If you specify a requested receipt date on a purchase order header, then the calculated order date is the date on which the order must be placed to receive the items on the date that you requested.</span></span> <span data-ttu-id="ea3d6-108">Dann wird das Datum, an dem die Artikel für die Kommissionierung zur Verfügung stehen, im Feld **Erwartetes Eingangsdatum** berechnet und eingegeben.</span><span class="sxs-lookup"><span data-stu-id="ea3d6-108">Then, the date on which the items are available for picking is calculated and entered in the **Expected Receipt Date** field.</span></span>  

<span data-ttu-id="ea3d6-109">Wenn Sie kein gewünschtes Wareneingangsdatum angeben, wird das Bestelldatum in der Zeile als Ausgangspunkt zur Berechnung des Datums verwendet, an dem die Artikel eingehen sollen, und des Datums, an dem die Artikel für die Kommissionierung zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="ea3d6-109">If you do not specify a requested receipt date, then the order date on the line is used as the starting point for calculating the date on which you can expect to receive the items and the date on which the items are available for picking.</span></span>  

## <a name="calculating-with-a-requested-receipt-date"></a><span data-ttu-id="ea3d6-110">Berechnung mit einem gewünschten Wareneingangsdatum</span><span class="sxs-lookup"><span data-stu-id="ea3d6-110">Calculating with a requested receipt date</span></span>

<span data-ttu-id="ea3d6-111">Falls es ein gewünschtes Wareneingangsdatum in der Einkaufsbestellungszeile gibt, wird dieses Datum als Ausgangspunkt für die folgenden Berechnungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ea3d6-111">If there is a requested receipt date on the purchase order line, then that date is used as the starting point for the following calculations.</span></span>  

- <span data-ttu-id="ea3d6-112">Gewünschtes Wareneingangsdatum – Beschaffungszeit = Bestelldatum</span><span class="sxs-lookup"><span data-stu-id="ea3d6-112">requested receipt date - lead time calculation = order date</span></span>  
- <span data-ttu-id="ea3d6-113">Gewünschtes Wareneingangsdatum + Eingeh. Lagerdurchlaufzeit + Beschaffungszeit = Erwartetes Wareneingangsdatum</span><span class="sxs-lookup"><span data-stu-id="ea3d6-113">requested receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="ea3d6-114">Wenn Sie ein gewünschtes Wareneingangsdatum im Bestellkopf angegeben haben, wird dieses Datum in das entsprechende Feld in allen Zeilen kopiert.</span><span class="sxs-lookup"><span data-stu-id="ea3d6-114">If you entered a requested receipt date on the purchase order header, then that date is copied to the corresponding field on all the lines.</span></span> <span data-ttu-id="ea3d6-115">Sie können dieses Datum in den einzelnen Zeilen ändern oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="ea3d6-115">You can change this date on any of the lines, or you can remove the date on the line.</span></span>  

> [!NOTE]
> <span data-ttu-id="ea3d6-116">Wenn Ihr Prozess auf einer Rückwärtsberechnung basiert, wenn Sie beispielsweise das angeforderte Wareneingangsdatum verwenden, um das geplante Auftragsdatum zu erhalten, empfehlen wir, Datumsformeln mit fester Dauer zu verwenden, z. B. 5D für fünf Tage oder 1W für eine Woche.</span><span class="sxs-lookup"><span data-stu-id="ea3d6-116">If your process is based on backward calculation, for example, if you use the requested receipt date to get the order date, we recommend that you use date formulas that have fixed durations, such as "5D" for five days or "1W" for one week.</span></span> <span data-ttu-id="ea3d6-117">Datumsformeln ohne feste Dauer, wie „CW“ für die aktuelle Woche oder CM für den aktuellen Monat, können zu falschen Datumsberechnungen führen.</span><span class="sxs-lookup"><span data-stu-id="ea3d6-117">Date formulas without fixed durations, such as "CW" for current week or CM for current month, can result in incorrect date calculations.</span></span> <span data-ttu-id="ea3d6-118">Weitere Informationen zu Datumsformeln finden Sie unter [Arbeiten mit Kalenderdaten und -zeiten](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="ea3d6-118">For more information about date formulas, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

## <a name="calculating-without-a-requested-delivery-date"></a><span data-ttu-id="ea3d6-119">Berechnung ohne ein gewünschtes Wareneingangsdatum</span><span class="sxs-lookup"><span data-stu-id="ea3d6-119">Calculating without a requested delivery date</span></span>

<span data-ttu-id="ea3d6-120">Wenn Sie eine Bestellzeile ohne ein gewünschtes Lieferdatum eingeben, füllt die Anwendung das Feld **Bestelldatum** in der Zeile mit dem **Bestelldatum** im Bestellkopf.</span><span class="sxs-lookup"><span data-stu-id="ea3d6-120">If you enter a purchase order line without a requested delivery date, then the **Order Date** field on the line is filled with the date in the **Order Date** field on the purchase order header.</span></span> <span data-ttu-id="ea3d6-121">Hierbei handelt es sich entweder um das Datum, das Sie eingegeben haben, oder um das Arbeitsdatum.</span><span class="sxs-lookup"><span data-stu-id="ea3d6-121">This is either the date that you entered or the work date.</span></span> <span data-ttu-id="ea3d6-122">Die folgenden Datumsangaben werden dann in der Einkaufsbestellungszeile berechnet, mit dem Bestelldatum als Ausgangspunkt.</span><span class="sxs-lookup"><span data-stu-id="ea3d6-122">The following dates are then calculated for the purchase order line, with the order date as the starting point.</span></span>  

- <span data-ttu-id="ea3d6-123">Bestelldatum + Beschaffungszeit = Geplantes Wareneingangsdatum</span><span class="sxs-lookup"><span data-stu-id="ea3d6-123">order date + lead time calculation = planned receipt date</span></span>  
- <span data-ttu-id="ea3d6-124">Geplantes Wareneingangsdatum + Eingeh. Lagerdurchlaufzeit + Beschaffungszeit = Erwartetes Wareneingangsdatum</span><span class="sxs-lookup"><span data-stu-id="ea3d6-124">planned receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="ea3d6-125">Falls Sie das Bestelldatum in der Zeile ändern (z. B. weil die Artikel bei dem Kreditor erst zu einem späteren Datum verfügbar sind), werden die entsprechenden Datumsangaben in der Zeile automatisch neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="ea3d6-125">If you change the order date on the line, such as when items are not available at your vendor until a later date, then the relevant dates on the line are automatically recalculated.</span></span>  

<span data-ttu-id="ea3d6-126">Wenn Sie das Bestelldatum im Kopf ändern, wird das Datum in allen Zeilen in das Feld  kopiert, und alle zugehörigen **Datumsfelder** werden neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="ea3d6-126">If you change the order date on the header, then that date is copied to the **Order Date** field on all the lines, and all the related date fields are then recalculated.</span></span>  

## <a name="default-values-for-lead-time-calculation"></a><span data-ttu-id="ea3d6-127">Standardwerte für die Vorlaufzeitberechnung</span><span class="sxs-lookup"><span data-stu-id="ea3d6-127">Default values for lead time calculation</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="ea3d6-128">verwendet den Wert aus dem Feld **Vorlaufzeitberechnung** in der Bestellzeile, um die Bestellung und die erwarteten Eingangsdaten zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="ea3d6-128">uses the value from the **Lead Time Calculation** field on the purchase order line to calculate the order and the expected receipt dates.</span></span>  

<span data-ttu-id="ea3d6-129">Sie können den Wert in der Zeile manuell angeben oder das Programm Werte verwenden lassen, die auf der Lieferantenkarte, der Artikelkarte, der Lagereinheitskarte oder dem Artikellieferantenkatalog definiert sind.</span><span class="sxs-lookup"><span data-stu-id="ea3d6-129">You can manually specify the value on the line or let the program use values that are defined on the vendor card, item card, stockkeeping unit card, or the item vendor catalog.</span></span>
<span data-ttu-id="ea3d6-130">Der Wert für die Vorlaufzeit auf der Lieferantenkarte wird jedoch nur verwendet, wenn auf der Artikelkarte, der Karte der Lagereinheit oder dem Artikellieferantenkatalog für den Artikel keine Vorlaufzeit angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ea3d6-130">However, the lead time value on the vendor card is used only if a lead time is not specified on the item card, stockkeeping unit card, or the item vendor catalog for the item.</span></span> <span data-ttu-id="ea3d6-131">Dies ist auch die eskalierende Prioritätsreihenfolge für diese Werte.</span><span class="sxs-lookup"><span data-stu-id="ea3d6-131">This is also the escalating order of priority for these values.</span></span> <span data-ttu-id="ea3d6-132">Wenn alle angegeben sind, hat die Vorlaufzeit von der Lieferantenkarte die niedrigste Priorität, und die Vorlaufzeit aus dem Lieferantenkatalog des Artikels hat die höchste Priorität.</span><span class="sxs-lookup"><span data-stu-id="ea3d6-132">If they are all provided, the lead time from the vendor card has the lowest priority, and the lead time from the item vendor catalog has the highest priority.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ea3d6-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea3d6-133">See Also</span></span>

<span data-ttu-id="ea3d6-134">[Terminberechnung für Verkäufe](sales-date-calculation-for-sales.md) </span><span class="sxs-lookup"><span data-stu-id="ea3d6-134">[Date Calculation for Sales](sales-date-calculation-for-sales.md) </span></span>  
[<span data-ttu-id="ea3d6-135">Lieferterminzusagen-Daten berechnen</span><span class="sxs-lookup"><span data-stu-id="ea3d6-135">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
<span data-ttu-id="ea3d6-136">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ea3d6-136">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]