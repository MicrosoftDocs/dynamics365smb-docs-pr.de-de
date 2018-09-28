---
title: Designdetails - Bestandbewertung | Microsoft Docs
description: Die Lagerbewertung ist die Identifizierung der Kosten, die einem Lagerartikel zugewiesen sind, wie durch folgende Formel dargestellt.
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
ms.openlocfilehash: 8d186d3f104f152a4ad121d32e14ad2bc1e33c5d
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-inventory-valuation"></a><span data-ttu-id="61af0-103">Designdetails: Bestandsbewertung</span><span class="sxs-lookup"><span data-stu-id="61af0-103">Design Details: Inventory Valuation</span></span>
<span data-ttu-id="61af0-104">Die Lagerbewertung ist die Identifizierung der Kosten, die einem Lagerartikel zugewiesen sind, wie durch folgende Formel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="61af0-104">Inventory valuation XE "Inventory Valuation"  is the determination of the cost that is assigned to an inventory item, as expressed by the following equation.</span></span>  

<span data-ttu-id="61af0-105">Endbestand = Anfangsbestand + Nettoeinkäufe - Vertriebskosten</span><span class="sxs-lookup"><span data-stu-id="61af0-105">Ending inventory = beginning inventory + net purchases – cost of goods sold</span></span>  

<span data-ttu-id="61af0-106">Die Berechnung der Lagerbewertung verwendet das Feld **Kostenbetrag (Ist)** der Wertposten für den Artikel.</span><span class="sxs-lookup"><span data-stu-id="61af0-106">The calculation of inventory valuation uses the **Cost Amount (Actual)** field of the value entries for the item.</span></span> <span data-ttu-id="61af0-107">Die Posten werden nach der Postenart klassifiziert, die den "Kostenkomponenten", den direkten Kosten, den indirekten Kosten, der Abweichung, der Neubewertung und der Rundung entspricht.</span><span class="sxs-lookup"><span data-stu-id="61af0-107">The entries are classified according to the entry type XE "Entry Type"  that corresponds to the cost components, direct cost, indirect cost, variance, revaluation, and rounding.</span></span> <span data-ttu-id="61af0-108">Weitere Informationen finden Sie unter [Designdetails: Kostenkomponenten](design-details-cost-components.md)</span><span class="sxs-lookup"><span data-stu-id="61af0-108">For more information, see [Design Details: Cost Components](design-details-cost-components.md).</span></span>  

<span data-ttu-id="61af0-109">Posten werden gegeneinander ausgeglichen, entweder durch den "festen Ausgleich" XE oder entsprechend der allgemeinen Kostenfluss-Annahme, die von der Kostenberechnungsmethode XE "Methode; Kosten" XE "Kostenmethode definiert ist.</span><span class="sxs-lookup"><span data-stu-id="61af0-109">Entries are applied against each other, either by the fixed application XE "Application; Fixed" , or according to the general cost-flow assumption defined by the costing method XE "Method; Costing"  XE "Costing Method" .</span></span> <span data-ttu-id="61af0-110">Ein Posten des Lagerabgangs kann mit mehr als einem Zugangseintrag mit verschiedenen Buchungsdaten und ggfs. verschiedenen "Anschaffungskosten" ausgeglichen werden.</span><span class="sxs-lookup"><span data-stu-id="61af0-110">One entry of inventory decrease can be applied to more than one increase entry with different posting dates and possibly different acquisition cost XE "Acquisition Cost" s.</span></span> <span data-ttu-id="61af0-111">[Weitere Informationen finden Sie unter "Designdetails: Artikelverfolgung".](design-details-item-application.md)</span><span class="sxs-lookup"><span data-stu-id="61af0-111">For more information, see [Design Details: Item Application](design-details-item-application.md).</span></span> <span data-ttu-id="61af0-112">Daher basiert die Berechnung des "Lagerwerts" für ein gegebenes Datum auf dem Aufsummieren von positiven und negativen Wertposten.</span><span class="sxs-lookup"><span data-stu-id="61af0-112">Therefore, calculation of the inventory value XE "Inventory Value"  for a given date is based on summing up positive and negative value entries.</span></span>  

## <a name="inventory-valuation-report"></a><span data-ttu-id="61af0-113">Bericht "Aktuellen Lagerwert ermitteln"</span><span class="sxs-lookup"><span data-stu-id="61af0-113">Inventory Valuation report</span></span>  
<span data-ttu-id="61af0-114">Um den Lagerwert im Bericht **Lagerwert berechnen** zu berechnen, beginnt der Bericht, den Lagerbestand des Artikels zu einem bestimmten Startdatum zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="61af0-114">To calculate the inventory value in the **Inventory Valuation** report, the report begins by calculating the value of the item’s inventory at a given starting date.</span></span> <span data-ttu-id="61af0-115">Er fügt den Wert von Lagerzugängen hinzu nd subtrahiert den Wert von Lagerabgängen bis zu einem bestimmten Enddatum.</span><span class="sxs-lookup"><span data-stu-id="61af0-115">It then adds the value of inventory increases and subtracts the value of inventory decreases up to a given ending date.</span></span> <span data-ttu-id="61af0-116">Das Endergebnis ist der Lagerwert am Enddatum.</span><span class="sxs-lookup"><span data-stu-id="61af0-116">The end result is the inventory value on the ending date.</span></span> <span data-ttu-id="61af0-117">Der Bericht berechnet diese Werte, indem er die Werte im Feld **Kostenbetrag (ist)** in den Wertposten summiert, wobei die Buchungsdaten als Filter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61af0-117">The report calculates these values by summing the values in the **Cost Amount (Actual)** field in the value entries, using the posting dates as filters.</span></span>  

<span data-ttu-id="61af0-118">Der gedruckte Bericht zeigt immer tatsächliche (fakturierte) Beträge an, d. h. Einstandspreise von Posten, die als fakturiert gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="61af0-118">The printed report always shows actual amounts, that is, the cost of entries that have been posted as invoiced.</span></span> <span data-ttu-id="61af0-119">Der Bericht enthält darüber hinaus die Soll-Kosten von Posten, die als geliefert gebucht wurden, wenn Sie auf dem Inforegister Optionen das Feld Inklusive Soll-Kosten durch ein Häkchen aktivieren.</span><span class="sxs-lookup"><span data-stu-id="61af0-119">The report will also print the expected cost of entries that have posted as received or shipped, if you select the Include Expected Cost field on the Options FastTab.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="61af0-120">Werte im Bericht **Lagerwert berechnen** wird mit dem Lagerkonto im Sachkonto abgestimmt, was bedeutet, dass die betreffenden Wertposten in der Finanzbuchhaltung gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="61af0-120">Values in the **Inventory Valuation** report is reconciled with the Inventory account in the general ledger, meaning the value entries in question have been posted to the general ledger.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="61af0-121">Beträge in den **Wert**-Spalten des Berichts basieren auf dem Buchungsdatum der Transaktionen für einen Artikel.</span><span class="sxs-lookup"><span data-stu-id="61af0-121">Amounts in the **Value** columns of the report are based on the posting date of transactions for an item.</span></span>  

## <a name="inventory-valuation---wip-report"></a><span data-ttu-id="61af0-122">Bericht "Aktuellen Lagerwert ermitteln"</span><span class="sxs-lookup"><span data-stu-id="61af0-122">Inventory Valuation - WIP report</span></span>  
<span data-ttu-id="61af0-123">Ein Produktionsbetrieb muss den Wert von drei Arten von Lagerbestand bestimmen:</span><span class="sxs-lookup"><span data-stu-id="61af0-123">A manufacturing company needs to determine the value of three types of inventory:</span></span>  

* <span data-ttu-id="61af0-124">Rohmaterialbestand</span><span class="sxs-lookup"><span data-stu-id="61af0-124">Raw Materials inventory</span></span>  
* <span data-ttu-id="61af0-125">Produktionslager</span><span class="sxs-lookup"><span data-stu-id="61af0-125">WIP inventory</span></span>  
* <span data-ttu-id="61af0-126">Fertigerzeugnisse (Bestand)</span><span class="sxs-lookup"><span data-stu-id="61af0-126">Finished Goods inventory</span></span>  

<span data-ttu-id="61af0-127">Der Wert des WIP-Lagers wird durch folgende Formel bestimmt:</span><span class="sxs-lookup"><span data-stu-id="61af0-127">The value of WIP inventory is determined by the following equation:</span></span>  

* <span data-ttu-id="61af0-128">End-WIP-Bestand = Anfangs-WIP-Bestand + Fertigungskosten - Fertigungskosten</span><span class="sxs-lookup"><span data-stu-id="61af0-128">Ending WIP inventory = Beginning WIP inventory + manufacturing costs – cost of goods manufactured</span></span>  

<span data-ttu-id="61af0-129">Wie bei eingekauftem Lagerbestand sind die Werteinträge die Grundlage der Bestandsbewertung.</span><span class="sxs-lookup"><span data-stu-id="61af0-129">As for purchased inventory, the value entries provide the basis of the inventory valuation.</span></span> <span data-ttu-id="61af0-130">Die Berechnung erfolgt anhand der Werte in dem Feld **Kostenbetrag (Ist)** der Artikel- und Kapazitätswertposten, die mit einem Fertigungsauftrag verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="61af0-130">The calculation is made using the values in the **Cost Amount (Actual)** field of the item and capacity value entries associated with a production order.</span></span>  

<span data-ttu-id="61af0-131">Der Zweck der WIP-Bestandsbewertung besteht darin, den Wert der Artikel zu ermitteln, deren Produktion an einem vorgegebenen Datum noch nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="61af0-131">The purpose of WIP inventory valuation is to determine the value of the items whose manufacturing has not yet been completed on a given date.</span></span> <span data-ttu-id="61af0-132">Daher ist der den Lagerwert der unfertigen Arbeit auf den Wertposten basiert, die sich auf die Verbrauchs- und Kapazitätsposten beziehen.</span><span class="sxs-lookup"><span data-stu-id="61af0-132">Therefore the WIP inventory value is based on the value entries related to the consumption and capacity ledger entries.</span></span> <span data-ttu-id="61af0-133">Verbrauchsposten müssen am Datum der Bewertung vollständig fakturiert sein.</span><span class="sxs-lookup"><span data-stu-id="61af0-133">Consumption ledger entries must be completely invoiced at the date of the valuation.</span></span> <span data-ttu-id="61af0-134">Deshalb zeigt der Bericht **Lagerbewertung - Aktiviert** die Kosten an, die den den Lagerwert der unfertigen Arbeit in zwei Kategorien darstellen: Verbrauch und Kapazität.</span><span class="sxs-lookup"><span data-stu-id="61af0-134">Therefore, the **Inventory Valuation – WIP** report shows the costs representing the WIP inventory value in two categories: consumption and capacity.</span></span>  

## <a name="see-also"></a><span data-ttu-id="61af0-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61af0-135">See Also</span></span>  
<span data-ttu-id="61af0-136">[Designdetails: Abgleich mit der Finanzbuchhaltung](design-details-reconciliation-with-the-general-ledger.md) </span><span class="sxs-lookup"><span data-stu-id="61af0-136">[Design Details: Reconciliation with the General Ledger](design-details-reconciliation-with-the-general-ledger.md) </span></span>  
<span data-ttu-id="61af0-137">[Designdetails: Neubewertung](design-details-revaluation.md) </span><span class="sxs-lookup"><span data-stu-id="61af0-137">[Design Details: Revaluation](design-details-revaluation.md) </span></span>  
<span data-ttu-id="61af0-138">[Designdetails: Fertigungsauftrags-Buchung](design-details-production-order-posting.md)
[Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)</span><span class="sxs-lookup"><span data-stu-id="61af0-138">[Design Details: Production Order Posting](design-details-production-order-posting.md)
[Managing Inventory Costs](finance-manage-inventory-costs.md)</span></span>  
[<span data-ttu-id="61af0-139">Finanzen</span><span class="sxs-lookup"><span data-stu-id="61af0-139">Finance</span></span>](finance.md)  
<span data-ttu-id="61af0-140">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="61af0-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

