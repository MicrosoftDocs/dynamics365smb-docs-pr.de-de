---
title: GDPdU-Filterbeispiele
description: Das folgende Thema enthält Beispiele, wie Sie unterschiedliche Filtertypen verwenden und kombinieren können, wenn Sie Ihre GPDdU-Exporte einrichten. Wenn Sie Filter passend einsetzen, können Sie die Leistung verbessern.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: d0ac7e4408a0b013c0dbe4a72e6f933c42bf6082
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2300193"
---
# <a name="gdpdu-filter-examples"></a><span data-ttu-id="63933-104">GDPdU-Filterbeispiele</span><span class="sxs-lookup"><span data-stu-id="63933-104">GDPdU Filter Examples</span></span>
<span data-ttu-id="63933-105">Das folgende Thema enthält Beispiele, wie Sie unterschiedliche Filtertypen verwenden und kombinieren können, wenn Sie Ihre GPDdU-Exporte einrichten.</span><span class="sxs-lookup"><span data-stu-id="63933-105">The following topic provides examples of how you can use and combine different filter types when you set up your GPDdU exports.</span></span> <span data-ttu-id="63933-106">Wenn Sie Filter passend einsetzen, können Sie die Leistung verbessern.</span><span class="sxs-lookup"><span data-stu-id="63933-106">By setting filters appropriately, you can improve performance.</span></span>  

<span data-ttu-id="63933-107">In den folgenden Beispielen werden für Daten die Tabellen für Sachposten und Debitorenposten verwendet.</span><span class="sxs-lookup"><span data-stu-id="63933-107">The following examples use the G/L Entry and Cust. Ledger Entry tables for data.</span></span> <span data-ttu-id="63933-108">Sie gehen davon aus, dass Sie das nächste Datum in der Stapelverarbeitung **Geschäftsdaten exportieren** angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="63933-108">They assume that you have specified the following date in the **Export Business Data** batch job.</span></span>  

<span data-ttu-id="63933-109">Startdatum = 01.01.2013</span><span class="sxs-lookup"><span data-stu-id="63933-109">Start Date = 01/01/2013</span></span>  

<span data-ttu-id="63933-110">Enddatum = 31.12.2013</span><span class="sxs-lookup"><span data-stu-id="63933-110">End Date = 12/31/2013</span></span>  

## <a name="setting-up-export-record-source-examples"></a><span data-ttu-id="63933-111">Einrichten von Beispielen für Datensatzquellen für den Export</span><span class="sxs-lookup"><span data-stu-id="63933-111">Setting Up Export Record Source Examples</span></span>  

### <a name="period-field-no"></a><span data-ttu-id="63933-112">Periodenfeldnr.</span><span class="sxs-lookup"><span data-stu-id="63933-112">Period Field No.</span></span>  
<span data-ttu-id="63933-113">Auf der Seite **Datenexport – Datensatzherkunft** erfolgt die Einrichtung wie in folgender Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="63933-113">On the **Data Export Record Source** page, the set up is as described in the following table.</span></span>  

|<span data-ttu-id="63933-114">Tabellennr.</span><span class="sxs-lookup"><span data-stu-id="63933-114">Table No.</span></span>|<span data-ttu-id="63933-115">Tabellenname</span><span class="sxs-lookup"><span data-stu-id="63933-115">Table Name</span></span>|<span data-ttu-id="63933-116">Periodenfeldnr.</span><span class="sxs-lookup"><span data-stu-id="63933-116">Period Field No.</span></span>|<span data-ttu-id="63933-117">Periodenfeldname</span><span class="sxs-lookup"><span data-stu-id="63933-117">Period Field Name</span></span>|<span data-ttu-id="63933-118">Tabellenfilter</span><span class="sxs-lookup"><span data-stu-id="63933-118">Table Filter</span></span>|  
|---------------|----------------|----------------------|-----------------------|------------------|  
|<span data-ttu-id="63933-119">17</span><span class="sxs-lookup"><span data-stu-id="63933-119">17</span></span>|<span data-ttu-id="63933-120">Fibubuchung</span><span class="sxs-lookup"><span data-stu-id="63933-120">G/L Entry</span></span>|<span data-ttu-id="63933-121">4</span><span class="sxs-lookup"><span data-stu-id="63933-121">4</span></span>|<span data-ttu-id="63933-122">Buchungsdatum</span><span class="sxs-lookup"><span data-stu-id="63933-122">Posting Date</span></span>|<span data-ttu-id="63933-123">Kein Filter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="63933-123">No filter set.</span></span>|  
|<span data-ttu-id="63933-124">21</span><span class="sxs-lookup"><span data-stu-id="63933-124">21</span></span>|<span data-ttu-id="63933-125">Debitorenposten</span><span class="sxs-lookup"><span data-stu-id="63933-125">Cust. Ledger Entry</span></span>|<span data-ttu-id="63933-126">4</span><span class="sxs-lookup"><span data-stu-id="63933-126">4</span></span>|<span data-ttu-id="63933-127">Buchungsdatum</span><span class="sxs-lookup"><span data-stu-id="63933-127">Posting Date</span></span>|<span data-ttu-id="63933-128">Kein Filter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="63933-128">No filter set.</span></span>|  

<span data-ttu-id="63933-129">**Ergebnisse exportieren**</span><span class="sxs-lookup"><span data-stu-id="63933-129">**Export Results**</span></span>  

- <span data-ttu-id="63933-130">Sachposten mit Buchungsdatum zwischen 01.01.2013 und 31.12.2013.</span><span class="sxs-lookup"><span data-stu-id="63933-130">G/L Entries with Posting Date between 1/1/2013 and 12/31/2013.</span></span>  
- <span data-ttu-id="63933-131">Debitorenposten mit Buchungsdatum zwischen 01.01.2013 und 31.12.2013.</span><span class="sxs-lookup"><span data-stu-id="63933-131">Cust. Ledger Entries with Posting Date between 1/1/2013 and 12/31/2013.</span></span>  

### <a name="table-filter"></a><span data-ttu-id="63933-132">Tabellenfilter</span><span class="sxs-lookup"><span data-stu-id="63933-132">Table Filter</span></span>  
<span data-ttu-id="63933-133">In diesem Beispiel geben Sie, zusätzlich zu „Periodenfeldnr.”-Informationen auch einen Tabellenfilter an.</span><span class="sxs-lookup"><span data-stu-id="63933-133">In this example, in addition to Period Field No. information, you also specify a table filter.</span></span> <span data-ttu-id="63933-134">Dies ist hilfreich, wenn Sie nicht nur ein Start- und Enddatum für Ihren Export einbeziehen möchten, sondern auch einen zusätzlichen Filter, um weitere Kriterien anzugeben, wie beispielsweise Beträge.</span><span class="sxs-lookup"><span data-stu-id="63933-134">This is useful when you want to not only include a starting date and ending date for your export, but also include an additional filter to specify other criteria, for example, amounts.</span></span>  

|<span data-ttu-id="63933-135">Tabellennr.</span><span class="sxs-lookup"><span data-stu-id="63933-135">Table No.</span></span>|<span data-ttu-id="63933-136">Tabellenname</span><span class="sxs-lookup"><span data-stu-id="63933-136">Table Name</span></span>|<span data-ttu-id="63933-137">Periodenfeldnr.</span><span class="sxs-lookup"><span data-stu-id="63933-137">Period Field No.</span></span>|<span data-ttu-id="63933-138">Periodenfeldname</span><span class="sxs-lookup"><span data-stu-id="63933-138">Period Field Name</span></span>|<span data-ttu-id="63933-139">Tabellenfilter</span><span class="sxs-lookup"><span data-stu-id="63933-139">Table Filter</span></span>|  
|---------------|----------------|----------------------|-----------------------|------------------|  
|<span data-ttu-id="63933-140">17</span><span class="sxs-lookup"><span data-stu-id="63933-140">17</span></span>|<span data-ttu-id="63933-141">Fibubuchung</span><span class="sxs-lookup"><span data-stu-id="63933-141">G/L Entry</span></span>|<span data-ttu-id="63933-142">4</span><span class="sxs-lookup"><span data-stu-id="63933-142">4</span></span>|<span data-ttu-id="63933-143">Buchungsdatum</span><span class="sxs-lookup"><span data-stu-id="63933-143">Posting Date</span></span>||  
|<span data-ttu-id="63933-144">21</span><span class="sxs-lookup"><span data-stu-id="63933-144">21</span></span>|<span data-ttu-id="63933-145">Debitorenposten</span><span class="sxs-lookup"><span data-stu-id="63933-145">Cust. Ledger Entry</span></span>|||<span data-ttu-id="63933-146">Debitorenposten: **Buchungsdatum=..31-12-13**</span><span class="sxs-lookup"><span data-stu-id="63933-146">Cust. Ledger Entry: **Posting Date=..31-12-13**</span></span>|  

<span data-ttu-id="63933-147">**Ergebnisse exportieren**</span><span class="sxs-lookup"><span data-stu-id="63933-147">**Export Results**</span></span>  

- <span data-ttu-id="63933-148">Sachposten mit Buchungsdatum zwischen 01.01.2013 und 31.12.2013.</span><span class="sxs-lookup"><span data-stu-id="63933-148">G/L Entries with Posting Date between 1/1/2013 and 12/31/2013.</span></span>  
- <span data-ttu-id="63933-149">Debitorenposten mit Buchungsdatum vor 01.01.2014.</span><span class="sxs-lookup"><span data-stu-id="63933-149">Cust. Ledger Entries with Posting Date earlier than 01/01/2014.</span></span>  

### <a name="date-filter-field-no-and-date-filter-handling"></a><span data-ttu-id="63933-150">Datumsfilter-Feldnummer und Behandlung von Datumsfiltern</span><span class="sxs-lookup"><span data-stu-id="63933-150">Date Filter Field No. and Date Filter Handling</span></span>  
<span data-ttu-id="63933-151">Im folgenden Beispiel wird die Einstellung von Datumstyp-FlowFilters veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="63933-151">The following example demonstrates setting Date type FlowFilters.</span></span> <span data-ttu-id="63933-152">Wenn eine Tabelle mehr als einen Datums-FlowFilter hat, können Sie keinen zur Benutzung angeben, aber Sie können angeben, wie der Datumsfilter behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="63933-152">If a table has more than one date FlowFilter, you cannot specify one to use, but you can specify how the date filter should be handled.</span></span>  

|<span data-ttu-id="63933-153">Tabellennr.</span><span class="sxs-lookup"><span data-stu-id="63933-153">Table No.</span></span>|<span data-ttu-id="63933-154">Tabellenname</span><span class="sxs-lookup"><span data-stu-id="63933-154">Table Name</span></span>|<span data-ttu-id="63933-155">Periodenfeldnr.</span><span class="sxs-lookup"><span data-stu-id="63933-155">Period Field No.</span></span>|<span data-ttu-id="63933-156">Periodenfeldname</span><span class="sxs-lookup"><span data-stu-id="63933-156">Period Field Name</span></span>|<span data-ttu-id="63933-157">Tabellenfilter</span><span class="sxs-lookup"><span data-stu-id="63933-157">Table Filter</span></span>|<span data-ttu-id="63933-158">Behandlung von Datumsfiltern</span><span class="sxs-lookup"><span data-stu-id="63933-158">Date Filter Handling</span></span>|  
|---------------|----------------|----------------------|-----------------------|------------------|--------------------------|  
|<span data-ttu-id="63933-159">18</span><span class="sxs-lookup"><span data-stu-id="63933-159">18</span></span>|<span data-ttu-id="63933-160">Debitor</span><span class="sxs-lookup"><span data-stu-id="63933-160">Customer</span></span>|||<span data-ttu-id="63933-161">Debitor: **Bewegung (MW)**=<>0</span><span class="sxs-lookup"><span data-stu-id="63933-161">Customer: **Net Change (LCY)**=<>0</span></span>|<span data-ttu-id="63933-162">**Periode**</span><span class="sxs-lookup"><span data-stu-id="63933-162">**Period**</span></span>|  
|<span data-ttu-id="63933-163">21</span><span class="sxs-lookup"><span data-stu-id="63933-163">21</span></span>|<span data-ttu-id="63933-164">Debitorenposten</span><span class="sxs-lookup"><span data-stu-id="63933-164">Cust. Ledger Entry</span></span>|<span data-ttu-id="63933-165">4</span><span class="sxs-lookup"><span data-stu-id="63933-165">4</span></span>|<span data-ttu-id="63933-166">Buchungsdatum</span><span class="sxs-lookup"><span data-stu-id="63933-166">Posting Date</span></span>|<span data-ttu-id="63933-167">Debitorenposten: **Restbetrag (MW)**=<>0</span><span class="sxs-lookup"><span data-stu-id="63933-167">Cust. Ledger Entry: **Remaining Amt. (LCY)**=<>0</span></span>|<span data-ttu-id="63933-168">**Nur Enddatum**</span><span class="sxs-lookup"><span data-stu-id="63933-168">**End Date Only**</span></span>|  

<span data-ttu-id="63933-169">**Ergebnisse exportieren**</span><span class="sxs-lookup"><span data-stu-id="63933-169">**Export Results**</span></span>  

- <span data-ttu-id="63933-170">Debitoren, die eine Bewegung (MW) <> 0 in die Periode von 01.01.2013 bis 31.12.2013 haben.</span><span class="sxs-lookup"><span data-stu-id="63933-170">Customers that have Net Change (LCY) <> 0 in the period from 1/1/2013 and 12/31/2013.</span></span>  
- <span data-ttu-id="63933-171">Debitorenposten mit Buchungsdatum zwischen 01.01.2013 und 31.12.2013, die einen Restbetrag (MW) <> 0 am 31.12.2013 haben.</span><span class="sxs-lookup"><span data-stu-id="63933-171">Cust. Ledger Entries with Posting Date between 01/01/2013 and 12/31/2013 that have Remaining Amt. (LCY) <> 0 at 12/31/2013.</span></span>  

### <a name="date-filter-handling-for-the-same-table"></a><span data-ttu-id="63933-172">Datumsfilterbehandlung für dieselbe Tabelle</span><span class="sxs-lookup"><span data-stu-id="63933-172">Date Filter Handling for the Same Table</span></span>  
<span data-ttu-id="63933-173">In diesem Beispiel legen Sie mehrere Filterdefinitionen für dieselbe Tabelle fest.</span><span class="sxs-lookup"><span data-stu-id="63933-173">In this example, you set multiple filter definitions for the same table.</span></span>  

|<span data-ttu-id="63933-174">Tabellennr.</span><span class="sxs-lookup"><span data-stu-id="63933-174">Table No.</span></span>|<span data-ttu-id="63933-175">Tabellenname</span><span class="sxs-lookup"><span data-stu-id="63933-175">Table Name</span></span>|<span data-ttu-id="63933-176">Tabellenfilter</span><span class="sxs-lookup"><span data-stu-id="63933-176">Table Filter</span></span>|<span data-ttu-id="63933-177">Behandlung von Datumsfiltern</span><span class="sxs-lookup"><span data-stu-id="63933-177">Date Filter Handling</span></span>|  
|---------------|----------------|------------------|--------------------------|  
|<span data-ttu-id="63933-178">18</span><span class="sxs-lookup"><span data-stu-id="63933-178">18</span></span>|<span data-ttu-id="63933-179">Debitor</span><span class="sxs-lookup"><span data-stu-id="63933-179">Customer</span></span>|<span data-ttu-id="63933-180">Debitor: **Bewegung (MW)**=<>0</span><span class="sxs-lookup"><span data-stu-id="63933-180">Customer: **Net Change (LCY)**=<>0</span></span>|<span data-ttu-id="63933-181">**Periode**</span><span class="sxs-lookup"><span data-stu-id="63933-181">**Period**</span></span>|  
|<span data-ttu-id="63933-182">18</span><span class="sxs-lookup"><span data-stu-id="63933-182">18</span></span>|<span data-ttu-id="63933-183">Debitor</span><span class="sxs-lookup"><span data-stu-id="63933-183">Customer</span></span>|<span data-ttu-id="63933-184">Debitor: **Bewegung (MW)**=<>0</span><span class="sxs-lookup"><span data-stu-id="63933-184">Customer: **Net Change (LCY)**=<>0</span></span>|<span data-ttu-id="63933-185">**Nur Startdatum**</span><span class="sxs-lookup"><span data-stu-id="63933-185">**Start Date Only**</span></span>|  

<span data-ttu-id="63933-186">**Ergebnisse exportieren**</span><span class="sxs-lookup"><span data-stu-id="63933-186">**Export Results**</span></span>  

- <span data-ttu-id="63933-187">Debitoren, die eine Bewegung (MW) <> 0 in die Periode von 01.01.2013 bis 31.12.2013 haben.</span><span class="sxs-lookup"><span data-stu-id="63933-187">Customers that have Net Change (LCY) <> 0 in the period from 1/1/2013 and 12/31/2013.</span></span>  
- <span data-ttu-id="63933-188">Debitoren, die Bewegung (MW) <> 0 am Tag vor dem Startdatum versehen haben.</span><span class="sxs-lookup"><span data-stu-id="63933-188">Customers that have Net Change (LCY) <> 0 on the day before the start date.</span></span>  

## <a name="see-also"></a><span data-ttu-id="63933-189">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63933-189">See Also</span></span>  
 [<span data-ttu-id="63933-190">Gewusst wie: Einrichten von Datenexporten für GDPdU</span><span class="sxs-lookup"><span data-stu-id="63933-190">Set Up Data Exports for GDPdU</span></span>](how-to-set-up-data-exports-for-gdpdu.md)
