---
title: GDPdU-Filterbeispiele
description: Das folgende Thema enthält Beispiele, wie Sie unterschiedliche Filtertypen verwenden und kombinieren können, wenn Sie Ihre GPDdU-Exporte einrichten. Wenn Sie Filter passend einsetzen, können Sie die Leistung verbessern.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e2180ee7dab96fd0c27ca49a92f94d298298282b
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3920092"
---
# <a name="gdpdu-filter-examples"></a><span data-ttu-id="27695-104">GDPdU-Filterbeispiele</span><span class="sxs-lookup"><span data-stu-id="27695-104">GDPdU Filter Examples</span></span>

<span data-ttu-id="27695-105">Das folgende Thema enthält Beispiele, wie Sie unterschiedliche Filtertypen verwenden und kombinieren können, wenn Sie Ihre GPDdU-Exporte einrichten.</span><span class="sxs-lookup"><span data-stu-id="27695-105">The following topic provides examples of how you can use and combine different filter types when you set up your GPDdU exports.</span></span> <span data-ttu-id="27695-106">Wenn Sie Filter passend einsetzen, können Sie die Leistung verbessern.</span><span class="sxs-lookup"><span data-stu-id="27695-106">By setting filters appropriately, you can improve performance.</span></span>  

<span data-ttu-id="27695-107">In den folgenden Beispielen werden für Daten die Tabellen für Sachposten und Debitorenposten verwendet.</span><span class="sxs-lookup"><span data-stu-id="27695-107">The following examples use the G/L Entry and Cust. Ledger Entry tables for data.</span></span> <span data-ttu-id="27695-108">Sie gehen davon aus, dass Sie das nächste Datum in der Stapelverarbeitung **Geschäftsdaten exportieren** angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="27695-108">They assume that you have specified the following date in the **Export Business Data** batch job.</span></span>  

<span data-ttu-id="27695-109">Startdatum = 01.01.2013</span><span class="sxs-lookup"><span data-stu-id="27695-109">Start Date = 01/01/2013</span></span>  

<span data-ttu-id="27695-110">Enddatum = 31.12.2013</span><span class="sxs-lookup"><span data-stu-id="27695-110">End Date = 12/31/2013</span></span>  

## <a name="setting-up-export-record-source-examples"></a><span data-ttu-id="27695-111">Einrichten von Beispielen für Datensatzquellen für den Export</span><span class="sxs-lookup"><span data-stu-id="27695-111">Setting Up Export Record Source Examples</span></span>  

### <a name="period-field-no"></a><span data-ttu-id="27695-112">Periodenfeldnr.</span><span class="sxs-lookup"><span data-stu-id="27695-112">Period Field No.</span></span>

<span data-ttu-id="27695-113">Auf der Seite **Datenexport – Datensatzherkunft** erfolgt die Einrichtung wie in folgender Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="27695-113">On the **Data Export Record Source** page, the set up is as described in the following table.</span></span>  

|<span data-ttu-id="27695-114">Tabellennr.</span><span class="sxs-lookup"><span data-stu-id="27695-114">Table No.</span></span>|<span data-ttu-id="27695-115">Tabellenname</span><span class="sxs-lookup"><span data-stu-id="27695-115">Table Name</span></span>|<span data-ttu-id="27695-116">Periodenfeldnr.</span><span class="sxs-lookup"><span data-stu-id="27695-116">Period Field No.</span></span>|<span data-ttu-id="27695-117">Periodenfeldname</span><span class="sxs-lookup"><span data-stu-id="27695-117">Period Field Name</span></span>|<span data-ttu-id="27695-118">Tabellenfilter</span><span class="sxs-lookup"><span data-stu-id="27695-118">Table Filter</span></span>|  
|---------------|----------------|----------------------|-----------------------|------------------|  
|<span data-ttu-id="27695-119">17</span><span class="sxs-lookup"><span data-stu-id="27695-119">17</span></span>|<span data-ttu-id="27695-120">Fibubuchung</span><span class="sxs-lookup"><span data-stu-id="27695-120">G/L Entry</span></span>|<span data-ttu-id="27695-121">4</span><span class="sxs-lookup"><span data-stu-id="27695-121">4</span></span>|<span data-ttu-id="27695-122">Buchungsdatum</span><span class="sxs-lookup"><span data-stu-id="27695-122">Posting Date</span></span>|<span data-ttu-id="27695-123">Kein Filter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="27695-123">No filter set.</span></span>|  
|<span data-ttu-id="27695-124">21</span><span class="sxs-lookup"><span data-stu-id="27695-124">21</span></span>|<span data-ttu-id="27695-125">Debitorenposten</span><span class="sxs-lookup"><span data-stu-id="27695-125">Cust. Ledger Entry</span></span>|<span data-ttu-id="27695-126">4</span><span class="sxs-lookup"><span data-stu-id="27695-126">4</span></span>|<span data-ttu-id="27695-127">Buchungsdatum</span><span class="sxs-lookup"><span data-stu-id="27695-127">Posting Date</span></span>|<span data-ttu-id="27695-128">Kein Filter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="27695-128">No filter set.</span></span>|  

<span data-ttu-id="27695-129">Exportergebnisse:</span><span class="sxs-lookup"><span data-stu-id="27695-129">Results of the export:</span></span>

- <span data-ttu-id="27695-130">Sachposten mit Buchungsdatum zwischen 01.01.2013 und 31.12.2013.</span><span class="sxs-lookup"><span data-stu-id="27695-130">G/L Entries with Posting Date between 1/1/2013 and 12/31/2013.</span></span>  
- <span data-ttu-id="27695-131">Debitorenposten mit Buchungsdatum zwischen 01.01.2013 und 31.12.2013.</span><span class="sxs-lookup"><span data-stu-id="27695-131">Cust. Ledger Entries with Posting Date between 1/1/2013 and 12/31/2013.</span></span>  

### <a name="table-filter"></a><span data-ttu-id="27695-132">Tabellenfilter</span><span class="sxs-lookup"><span data-stu-id="27695-132">Table Filter</span></span>

<span data-ttu-id="27695-133">In diesem Beispiel geben Sie, zusätzlich zu „Periodenfeldnr.“-Informationen auch einen Tabellenfilter an.</span><span class="sxs-lookup"><span data-stu-id="27695-133">In this example, in addition to Period Field No. information, you also specify a table filter.</span></span> <span data-ttu-id="27695-134">Dies ist hilfreich, wenn Sie nicht nur ein Start- und Enddatum für Ihren Export einbeziehen möchten, sondern auch einen zusätzlichen Filter, um weitere Kriterien anzugeben, wie beispielsweise Beträge.</span><span class="sxs-lookup"><span data-stu-id="27695-134">This is useful when you want to not only include a starting date and ending date for your export, but also include an additional filter to specify other criteria, for example, amounts.</span></span>  

|<span data-ttu-id="27695-135">Tabellennr.</span><span class="sxs-lookup"><span data-stu-id="27695-135">Table No.</span></span>|<span data-ttu-id="27695-136">Tabellenname</span><span class="sxs-lookup"><span data-stu-id="27695-136">Table Name</span></span>|<span data-ttu-id="27695-137">Periodenfeldnr.</span><span class="sxs-lookup"><span data-stu-id="27695-137">Period Field No.</span></span>|<span data-ttu-id="27695-138">Periodenfeldname</span><span class="sxs-lookup"><span data-stu-id="27695-138">Period Field Name</span></span>|<span data-ttu-id="27695-139">Tabellenfilter</span><span class="sxs-lookup"><span data-stu-id="27695-139">Table Filter</span></span>|  
|---------------|----------------|----------------------|-----------------------|------------------|  
|<span data-ttu-id="27695-140">17</span><span class="sxs-lookup"><span data-stu-id="27695-140">17</span></span>|<span data-ttu-id="27695-141">Fibubuchung</span><span class="sxs-lookup"><span data-stu-id="27695-141">G/L Entry</span></span>|<span data-ttu-id="27695-142">4</span><span class="sxs-lookup"><span data-stu-id="27695-142">4</span></span>|<span data-ttu-id="27695-143">Buchungsdatum</span><span class="sxs-lookup"><span data-stu-id="27695-143">Posting Date</span></span>||  
|<span data-ttu-id="27695-144">21</span><span class="sxs-lookup"><span data-stu-id="27695-144">21</span></span>|<span data-ttu-id="27695-145">Debitorenposten</span><span class="sxs-lookup"><span data-stu-id="27695-145">Cust. Ledger Entry</span></span>|||<span data-ttu-id="27695-146">Debitorenposten: **Buchungsdatum=..31-12-13**</span><span class="sxs-lookup"><span data-stu-id="27695-146">Cust. Ledger Entry: **Posting Date=..31-12-13**</span></span>|  

<span data-ttu-id="27695-147">Exportergebnisse:</span><span class="sxs-lookup"><span data-stu-id="27695-147">Results of the export:</span></span>

- <span data-ttu-id="27695-148">Sachposten mit Buchungsdatum zwischen 01.01.2013 und 31.12.2013.</span><span class="sxs-lookup"><span data-stu-id="27695-148">G/L Entries with Posting Date between 1/1/2013 and 12/31/2013.</span></span>  
- <span data-ttu-id="27695-149">Debitorenposten mit Buchungsdatum vor 01.01.2014.</span><span class="sxs-lookup"><span data-stu-id="27695-149">Cust. Ledger Entries with Posting Date earlier than 01/01/2014.</span></span>  

### <a name="date-filter-field-no-and-date-filter-handling"></a><span data-ttu-id="27695-150">Datumsfilter-Feldnummer und Behandlung von Datumsfiltern</span><span class="sxs-lookup"><span data-stu-id="27695-150">Date Filter Field No. and Date Filter Handling</span></span>

<span data-ttu-id="27695-151">Im folgenden Beispiel wird die Einstellung von Datumstyp-FlowFilters veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="27695-151">The following example demonstrates setting Date type FlowFilters.</span></span> <span data-ttu-id="27695-152">Wenn eine Tabelle mehr als einen Datums-FlowFilter hat, können Sie keinen zur Benutzung angeben, aber Sie können angeben, wie der Datumsfilter behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="27695-152">If a table has more than one date FlowFilter, you cannot specify one to use, but you can specify how the date filter should be handled.</span></span>  

|<span data-ttu-id="27695-153">Tabellennr.</span><span class="sxs-lookup"><span data-stu-id="27695-153">Table No.</span></span>|<span data-ttu-id="27695-154">Tabellenname</span><span class="sxs-lookup"><span data-stu-id="27695-154">Table Name</span></span>|<span data-ttu-id="27695-155">Periodenfeldnr.</span><span class="sxs-lookup"><span data-stu-id="27695-155">Period Field No.</span></span>|<span data-ttu-id="27695-156">Periodenfeldname</span><span class="sxs-lookup"><span data-stu-id="27695-156">Period Field Name</span></span>|<span data-ttu-id="27695-157">Tabellenfilter</span><span class="sxs-lookup"><span data-stu-id="27695-157">Table Filter</span></span>|<span data-ttu-id="27695-158">Behandlung von Datumsfiltern</span><span class="sxs-lookup"><span data-stu-id="27695-158">Date Filter Handling</span></span>|  
|---------------|----------------|----------------------|-----------------------|------------------|--------------------------|  
|<span data-ttu-id="27695-159">18</span><span class="sxs-lookup"><span data-stu-id="27695-159">18</span></span>|<span data-ttu-id="27695-160">Debitor</span><span class="sxs-lookup"><span data-stu-id="27695-160">Customer</span></span>|||<span data-ttu-id="27695-161">Debitor: **Bewegung (MW)**=<>0</span><span class="sxs-lookup"><span data-stu-id="27695-161">Customer: **Net Change (LCY)**=<>0</span></span>|<span data-ttu-id="27695-162">**Periode**</span><span class="sxs-lookup"><span data-stu-id="27695-162">**Period**</span></span>|  
|<span data-ttu-id="27695-163">21</span><span class="sxs-lookup"><span data-stu-id="27695-163">21</span></span>|<span data-ttu-id="27695-164">Debitorenposten</span><span class="sxs-lookup"><span data-stu-id="27695-164">Cust. Ledger Entry</span></span>|<span data-ttu-id="27695-165">4</span><span class="sxs-lookup"><span data-stu-id="27695-165">4</span></span>|<span data-ttu-id="27695-166">Buchungsdatum</span><span class="sxs-lookup"><span data-stu-id="27695-166">Posting Date</span></span>|<span data-ttu-id="27695-167">Debitorenposten: **Restbetrag (MW)**=<>0</span><span class="sxs-lookup"><span data-stu-id="27695-167">Cust. Ledger Entry: **Remaining Amt. (LCY)**=<>0</span></span>|<span data-ttu-id="27695-168">**Nur Enddatum**</span><span class="sxs-lookup"><span data-stu-id="27695-168">**End Date Only**</span></span>|  

<span data-ttu-id="27695-169">Exportergebnisse:</span><span class="sxs-lookup"><span data-stu-id="27695-169">Results of the export:</span></span>

- <span data-ttu-id="27695-170">Debitoren, die eine Bewegung (MW) <> 0 in die Periode von 01.01.2013 bis 31.12.2013 haben.</span><span class="sxs-lookup"><span data-stu-id="27695-170">Customers that have Net Change (LCY) <> 0 in the period from 1/1/2013 and 12/31/2013.</span></span>  
- <span data-ttu-id="27695-171">Debitorenposten mit Buchungsdatum zwischen 01.01.2013 und 31.12.2013, die einen Restbetrag (MW) <> 0 am 31.12.2013 haben.</span><span class="sxs-lookup"><span data-stu-id="27695-171">Cust. Ledger Entries with Posting Date between 01/01/2013 and 12/31/2013 that have Remaining Amt. (LCY) <> 0 at 12/31/2013.</span></span>  

### <a name="date-filter-handling-for-the-same-table"></a><span data-ttu-id="27695-172">Datumsfilterbehandlung für dieselbe Tabelle</span><span class="sxs-lookup"><span data-stu-id="27695-172">Date Filter Handling for the Same Table</span></span>

<span data-ttu-id="27695-173">In diesem Beispiel legen Sie mehrere Filterdefinitionen für dieselbe Tabelle fest.</span><span class="sxs-lookup"><span data-stu-id="27695-173">In this example, you set multiple filter definitions for the same table.</span></span>  

|<span data-ttu-id="27695-174">Tabellennr.</span><span class="sxs-lookup"><span data-stu-id="27695-174">Table No.</span></span>|<span data-ttu-id="27695-175">Tabellenname</span><span class="sxs-lookup"><span data-stu-id="27695-175">Table Name</span></span>|<span data-ttu-id="27695-176">Tabellenfilter</span><span class="sxs-lookup"><span data-stu-id="27695-176">Table Filter</span></span>|<span data-ttu-id="27695-177">Behandlung von Datumsfiltern</span><span class="sxs-lookup"><span data-stu-id="27695-177">Date Filter Handling</span></span>|  
|---------------|----------------|------------------|--------------------------|  
|<span data-ttu-id="27695-178">18</span><span class="sxs-lookup"><span data-stu-id="27695-178">18</span></span>|<span data-ttu-id="27695-179">Debitor</span><span class="sxs-lookup"><span data-stu-id="27695-179">Customer</span></span>|<span data-ttu-id="27695-180">Debitor: **Bewegung (MW)**=<>0</span><span class="sxs-lookup"><span data-stu-id="27695-180">Customer: **Net Change (LCY)**=<>0</span></span>|<span data-ttu-id="27695-181">**Periode**</span><span class="sxs-lookup"><span data-stu-id="27695-181">**Period**</span></span>|  
|<span data-ttu-id="27695-182">18</span><span class="sxs-lookup"><span data-stu-id="27695-182">18</span></span>|<span data-ttu-id="27695-183">Debitor</span><span class="sxs-lookup"><span data-stu-id="27695-183">Customer</span></span>|<span data-ttu-id="27695-184">Debitor: **Bewegung (MW)**=<>0</span><span class="sxs-lookup"><span data-stu-id="27695-184">Customer: **Net Change (LCY)**=<>0</span></span>|<span data-ttu-id="27695-185">**Nur Startdatum**</span><span class="sxs-lookup"><span data-stu-id="27695-185">**Start Date Only**</span></span>|  

<span data-ttu-id="27695-186">Exportergebnisse:</span><span class="sxs-lookup"><span data-stu-id="27695-186">Results of the export:</span></span>

- <span data-ttu-id="27695-187">Debitoren, die eine Bewegung (MW) <> 0 in der Periode vom 01.01.2013 bis 31.12.2013 haben.</span><span class="sxs-lookup"><span data-stu-id="27695-187">Customers that have Net Change (LCY) <> 0 in the period from 1/1/2013 and 12/31/2013.</span></span>  
- <span data-ttu-id="27695-188">Debitoren, die Bewegung (MW) <> 0 am Tag vor dem Startdatum versehen haben.</span><span class="sxs-lookup"><span data-stu-id="27695-188">Customers that have Net Change (LCY) <> 0 on the day before the start date.</span></span>  

## <a name="see-also"></a><span data-ttu-id="27695-189">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27695-189">See Also</span></span>

[<span data-ttu-id="27695-190">Daten für eine digitale Prüfung (GoBD/GDPdU) einrichten</span><span class="sxs-lookup"><span data-stu-id="27695-190">Set Up Data Exports for a Digital Audit (GoBD/GDPdU)</span></span>](how-to-set-up-data-exports-for-digital-audits.md)  
