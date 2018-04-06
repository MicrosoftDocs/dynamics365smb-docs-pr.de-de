---
title: Beispiel - Inventurauftragszeile mit Nachverfolgungszeilen
description: 'Eine Inventurauftragszeile muss die folgenden bestimmten Daten enthalten:'
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
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 41ec6f018b604e5dddb7ac9da735c6e0623eed82
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="example---inventory-order-line-with-tracking-lines"></a><span data-ttu-id="27dff-103">Beispiel - Inventurauftragszeile mit Nachverfolgungszeilen</span><span class="sxs-lookup"><span data-stu-id="27dff-103">Example - Inventory Order Line with Tracking Lines</span></span>
<span data-ttu-id="27dff-104">Eine Inventurauftragszeile enthält die folgenden buchungsrelevanten Daten:</span><span class="sxs-lookup"><span data-stu-id="27dff-104">The physical inventory order line should contain the following data:</span></span>  

- <span data-ttu-id="27dff-105">Artikelnr.: 80216-V</span><span class="sxs-lookup"><span data-stu-id="27dff-105">Item No.: 80216-V</span></span>  
- <span data-ttu-id="27dff-106">Lagerortcode: BLAU</span><span class="sxs-lookup"><span data-stu-id="27dff-106">Location Code: BLUE</span></span>  
- <span data-ttu-id="27dff-107">Die Felder "Variantencode" und "Lagerplatzcode" sind beide leer.</span><span class="sxs-lookup"><span data-stu-id="27dff-107">The fields Variant Code and Bin Code may be blank.</span></span>  

<span data-ttu-id="27dff-108">Das Kontrollkästchen Verfolgungszeilen verwenden der Inventurauftragszeile wurde aktiviert, und der Artikel 80216-V wird entsprechend seines Artikelverfolgungscodes stets unter Angabe der Chargennummern gebucht.</span><span class="sxs-lookup"><span data-stu-id="27dff-108">There is a check mark in the field Use Tracking Lines on the physical inventory order line and the item 80216-V should be posted all time with lot nos. according to the item tracking code.</span></span>  

<span data-ttu-id="27dff-109">Das Buchungsdatum des Inventurauftragskopfes ist der 31.12.2002.</span><span class="sxs-lookup"><span data-stu-id="27dff-109">The posting date on the physical inventory order header should be 12/31/2002.</span></span>  

<span data-ttu-id="27dff-110">Die erwartete Menge des Artikels 80216-V am Lagerort BLAU zum 31.12.2001 beträgt 120 Stück.</span><span class="sxs-lookup"><span data-stu-id="27dff-110">The expected quantity of the item 80216-V at the location BLUE on 12/31/2001 should be 120 pieces.</span></span>  

<span data-ttu-id="27dff-111">Der Lagerbestand setzt sich aus den folgenden Chargen zusammen:</span><span class="sxs-lookup"><span data-stu-id="27dff-111">The quantity on stock consists of the following lots:</span></span>  

## <a name="the-expected-item-tracking-lines"></a><span data-ttu-id="27dff-112">Die erwarteten Artikelverfolgungszeilen:</span><span class="sxs-lookup"><span data-stu-id="27dff-112">The expected Item Tracking Lines:</span></span>  

|<span data-ttu-id="27dff-113">**Chargennr.**</span><span class="sxs-lookup"><span data-stu-id="27dff-113">**Lot No.**</span></span>|<span data-ttu-id="27dff-114">**Menge**</span><span class="sxs-lookup"><span data-stu-id="27dff-114">**Quantity**</span></span>|  
|-----------------|------------------|  
|<span data-ttu-id="27dff-115">CH1001</span><span class="sxs-lookup"><span data-stu-id="27dff-115">CH1001</span></span>|<span data-ttu-id="27dff-116">80</span><span class="sxs-lookup"><span data-stu-id="27dff-116">80</span></span>|  
|<span data-ttu-id="27dff-117">CH1003</span><span class="sxs-lookup"><span data-stu-id="27dff-117">CH1003</span></span>|<span data-ttu-id="27dff-118">30</span><span class="sxs-lookup"><span data-stu-id="27dff-118">30</span></span>|  
|<span data-ttu-id="27dff-119">CH1006</span><span class="sxs-lookup"><span data-stu-id="27dff-119">CH1006</span></span>|<span data-ttu-id="27dff-120">10</span><span class="sxs-lookup"><span data-stu-id="27dff-120">10</span></span>|  
|<span data-ttu-id="27dff-121">**Summe**</span><span class="sxs-lookup"><span data-stu-id="27dff-121">**Total**</span></span>|<span data-ttu-id="27dff-122">**120**</span><span class="sxs-lookup"><span data-stu-id="27dff-122">**120**</span></span>|  

<span data-ttu-id="27dff-123">Es wurden folgende Inventurerfassungszeilen für Artikel 80216-V, Lagerortcode BLAU, erfasst:</span><span class="sxs-lookup"><span data-stu-id="27dff-123">There had been recorded the following physical inventory recording lines for the item 80216-V, location code BLUE:</span></span>  

## <a name="recorded-lot-nos-on-the-physical-inventory-recording-lines"></a><span data-ttu-id="27dff-124">Erfasste Chargennummern in den Inventurerfassungszeilen:</span><span class="sxs-lookup"><span data-stu-id="27dff-124">Recorded Lot Nos. on the Physical Inventory Recording Lines:</span></span>  

|<span data-ttu-id="27dff-125">**Chargennr.**</span><span class="sxs-lookup"><span data-stu-id="27dff-125">**Lot No.**</span></span>|<span data-ttu-id="27dff-126">**Menge**</span><span class="sxs-lookup"><span data-stu-id="27dff-126">**Quantity**</span></span>|  
|-----------------|------------------|  
|<span data-ttu-id="27dff-127">CH1001</span><span class="sxs-lookup"><span data-stu-id="27dff-127">CH1001</span></span>|<span data-ttu-id="27dff-128">80</span><span class="sxs-lookup"><span data-stu-id="27dff-128">80</span></span>|  
|<span data-ttu-id="27dff-129">CH1002</span><span class="sxs-lookup"><span data-stu-id="27dff-129">CH1002</span></span>|<span data-ttu-id="27dff-130">12</span><span class="sxs-lookup"><span data-stu-id="27dff-130">12</span></span>|  
|<span data-ttu-id="27dff-131">CH1003</span><span class="sxs-lookup"><span data-stu-id="27dff-131">CH1003</span></span>|<span data-ttu-id="27dff-132">20</span><span class="sxs-lookup"><span data-stu-id="27dff-132">20</span></span>|  
|<span data-ttu-id="27dff-133">**Summe**</span><span class="sxs-lookup"><span data-stu-id="27dff-133">**Total**</span></span>|<span data-ttu-id="27dff-134">**112**</span><span class="sxs-lookup"><span data-stu-id="27dff-134">**112**</span></span>|  

<span data-ttu-id="27dff-135">Bei Abschluss des Inventurauftrags berechnet die Anwendung für den Artikel 80216-V am Lagerort BLAU einen zu buchenden Abgang von 8 Stück und erstellt folgende Posten</span><span class="sxs-lookup"><span data-stu-id="27dff-135">When finishing the physical inventory order the program will calculate for the item 80216-V at the location BLUE a negative adjustment of 8 pieces and will create the following entries:</span></span>  

## <a name="item-tracking-lines-to-post"></a><span data-ttu-id="27dff-136">Zu buchende Artikelverfolgungszeilen:</span><span class="sxs-lookup"><span data-stu-id="27dff-136">Item Tracking lines to post:</span></span>  

|<span data-ttu-id="27dff-137">**Chargennr.**</span><span class="sxs-lookup"><span data-stu-id="27dff-137">**Lot No.**</span></span>|<span data-ttu-id="27dff-138">**Erwartete Menge**</span><span class="sxs-lookup"><span data-stu-id="27dff-138">**Expected Quantity**</span></span>|<span data-ttu-id="27dff-139">**Erfasste Menge**</span><span class="sxs-lookup"><span data-stu-id="27dff-139">**Recorded Quantity**</span></span>|<span data-ttu-id="27dff-140">**Zu buchende Menge**</span><span class="sxs-lookup"><span data-stu-id="27dff-140">**Quantity to post**</span></span>|  
|-----------------|---------------------------|---------------------------|--------------------------|  
|<span data-ttu-id="27dff-141">CH1001</span><span class="sxs-lookup"><span data-stu-id="27dff-141">CH1001</span></span>|<span data-ttu-id="27dff-142">80</span><span class="sxs-lookup"><span data-stu-id="27dff-142">80</span></span>|<span data-ttu-id="27dff-143">80</span><span class="sxs-lookup"><span data-stu-id="27dff-143">80</span></span>|<span data-ttu-id="27dff-144">0</span><span class="sxs-lookup"><span data-stu-id="27dff-144">0</span></span>|  
|<span data-ttu-id="27dff-145">CH1002</span><span class="sxs-lookup"><span data-stu-id="27dff-145">CH1002</span></span>|<span data-ttu-id="27dff-146">0</span><span class="sxs-lookup"><span data-stu-id="27dff-146">0</span></span>|<span data-ttu-id="27dff-147">12</span><span class="sxs-lookup"><span data-stu-id="27dff-147">12</span></span>|<span data-ttu-id="27dff-148">+12</span><span class="sxs-lookup"><span data-stu-id="27dff-148">+ 12</span></span>|  
|<span data-ttu-id="27dff-149">CH1003</span><span class="sxs-lookup"><span data-stu-id="27dff-149">CH1003</span></span>|<span data-ttu-id="27dff-150">30</span><span class="sxs-lookup"><span data-stu-id="27dff-150">30</span></span>|<span data-ttu-id="27dff-151">20</span><span class="sxs-lookup"><span data-stu-id="27dff-151">20</span></span>|<span data-ttu-id="27dff-152">-10</span><span class="sxs-lookup"><span data-stu-id="27dff-152">- 10</span></span>|  
|<span data-ttu-id="27dff-153">CH1006</span><span class="sxs-lookup"><span data-stu-id="27dff-153">CH1006</span></span>|<span data-ttu-id="27dff-154">10</span><span class="sxs-lookup"><span data-stu-id="27dff-154">10</span></span>|<span data-ttu-id="27dff-155">0</span><span class="sxs-lookup"><span data-stu-id="27dff-155">0</span></span>|<span data-ttu-id="27dff-156">-10</span><span class="sxs-lookup"><span data-stu-id="27dff-156">- 10</span></span>|  
|<span data-ttu-id="27dff-157">**Summe**</span><span class="sxs-lookup"><span data-stu-id="27dff-157">**Total**</span></span>|<span data-ttu-id="27dff-158">**120**</span><span class="sxs-lookup"><span data-stu-id="27dff-158">**120**</span></span>|<span data-ttu-id="27dff-159">**112**</span><span class="sxs-lookup"><span data-stu-id="27dff-159">**112**</span></span>|<span data-ttu-id="27dff-160">**-8**</span><span class="sxs-lookup"><span data-stu-id="27dff-160">**- 8**</span></span>|  

## <a name="see-also"></a><span data-ttu-id="27dff-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27dff-161">See Also</span></span>  
 [<span data-ttu-id="27dff-162">Inventurauftragszeilen mit Artikelverfolgungszeilen</span><span class="sxs-lookup"><span data-stu-id="27dff-162">Physical Inventory Order Lines With Item Tracking Lines</span></span>](physical-inventory-order-lines-with-item-tracking-lines.md)  
 [<span data-ttu-id="27dff-163">Arbeiten mit Chargennummern und Seriennummern</span><span class="sxs-lookup"><span data-stu-id="27dff-163">Work with Serial and Lot Numbers</span></span>](../../inventory-how-work-item-tracking.md)

