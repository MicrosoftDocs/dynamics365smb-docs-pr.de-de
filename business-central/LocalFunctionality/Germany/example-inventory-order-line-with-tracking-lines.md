---
title: Beispiel - Inventurauftragszeile mit Nachverfolgungszeilen
description: 'Eine Inventurauftragszeile muss die folgenden bestimmten Daten enthalten:'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/01/2017
ms.author: sgroespe
ms.openlocfilehash: fc3f4bca5a09ec4780bded9f5e87d37a4484e9e3
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241723"
---
# <a name="example---inventory-order-line-with-tracking-lines"></a><span data-ttu-id="d9e22-103">Beispiel - Inventurauftragszeile mit Nachverfolgungszeilen</span><span class="sxs-lookup"><span data-stu-id="d9e22-103">Example - Inventory Order Line with Tracking Lines</span></span>
<span data-ttu-id="d9e22-104">Eine Inventurauftragszeile enthält die folgenden buchungsrelevanten Daten:</span><span class="sxs-lookup"><span data-stu-id="d9e22-104">The physical inventory order line should contain the following data:</span></span>  

- <span data-ttu-id="d9e22-105">Artikelnr.: 80216-V</span><span class="sxs-lookup"><span data-stu-id="d9e22-105">Item No.: 80216-V</span></span>  
- <span data-ttu-id="d9e22-106">Lagerortcode: BLAU</span><span class="sxs-lookup"><span data-stu-id="d9e22-106">Location Code: BLUE</span></span>  
- <span data-ttu-id="d9e22-107">Die Felder "Variantencode" und "Lagerplatzcode" sind beide leer.</span><span class="sxs-lookup"><span data-stu-id="d9e22-107">The fields Variant Code and Bin Code may be blank.</span></span>  

<span data-ttu-id="d9e22-108">Das Kontrollkästchen Verfolgungszeilen verwenden der Inventurauftragszeile wurde aktiviert, und der Artikel 80216-V wird entsprechend seines Artikelverfolgungscodes stets unter Angabe der Chargennummern gebucht.</span><span class="sxs-lookup"><span data-stu-id="d9e22-108">There is a check mark in the field Use Tracking Lines on the physical inventory order line and the item 80216-V should be posted all time with lot nos. according to the item tracking code.</span></span>  

<span data-ttu-id="d9e22-109">Das Buchungsdatum des Inventurauftragskopfes ist der 31.12.2002.</span><span class="sxs-lookup"><span data-stu-id="d9e22-109">The posting date on the physical inventory order header should be 12/31/2002.</span></span>  

<span data-ttu-id="d9e22-110">Die erwartete Menge des Artikels 80216-V am Lagerort BLAU zum 31.12.2001 beträgt 120 Stück.</span><span class="sxs-lookup"><span data-stu-id="d9e22-110">The expected quantity of the item 80216-V at the location BLUE on 12/31/2001 should be 120 pieces.</span></span>  

<span data-ttu-id="d9e22-111">Der Lagerbestand setzt sich aus den folgenden Chargen zusammen:</span><span class="sxs-lookup"><span data-stu-id="d9e22-111">The quantity on stock consists of the following lots:</span></span>  

## <a name="the-expected-item-tracking-lines"></a><span data-ttu-id="d9e22-112">Die erwarteten Artikelverfolgungszeilen:</span><span class="sxs-lookup"><span data-stu-id="d9e22-112">The expected Item Tracking Lines:</span></span>  

|<span data-ttu-id="d9e22-113">**Chargennr.**</span><span class="sxs-lookup"><span data-stu-id="d9e22-113">**Lot No.**</span></span>|<span data-ttu-id="d9e22-114">**Menge**</span><span class="sxs-lookup"><span data-stu-id="d9e22-114">**Quantity**</span></span>|  
|-----------------|------------------|  
|<span data-ttu-id="d9e22-115">CH1001</span><span class="sxs-lookup"><span data-stu-id="d9e22-115">CH1001</span></span>|<span data-ttu-id="d9e22-116">80</span><span class="sxs-lookup"><span data-stu-id="d9e22-116">80</span></span>|  
|<span data-ttu-id="d9e22-117">CH1003</span><span class="sxs-lookup"><span data-stu-id="d9e22-117">CH1003</span></span>|<span data-ttu-id="d9e22-118">30</span><span class="sxs-lookup"><span data-stu-id="d9e22-118">30</span></span>|  
|<span data-ttu-id="d9e22-119">CH1006</span><span class="sxs-lookup"><span data-stu-id="d9e22-119">CH1006</span></span>|<span data-ttu-id="d9e22-120">10</span><span class="sxs-lookup"><span data-stu-id="d9e22-120">10</span></span>|  
|<span data-ttu-id="d9e22-121">**Summe**</span><span class="sxs-lookup"><span data-stu-id="d9e22-121">**Total**</span></span>|<span data-ttu-id="d9e22-122">**120**</span><span class="sxs-lookup"><span data-stu-id="d9e22-122">**120**</span></span>|  

<span data-ttu-id="d9e22-123">Es wurden folgende Inventurerfassungszeilen für Artikel 80216-V, Lagerortcode BLAU, erfasst:</span><span class="sxs-lookup"><span data-stu-id="d9e22-123">There had been recorded the following physical inventory recording lines for the item 80216-V, location code BLUE:</span></span>  

## <a name="recorded-lot-nos-on-the-physical-inventory-recording-lines"></a><span data-ttu-id="d9e22-124">Erfasste Chargennummern in den Inventurerfassungszeilen:</span><span class="sxs-lookup"><span data-stu-id="d9e22-124">Recorded Lot Nos. on the Physical Inventory Recording Lines:</span></span>  

|<span data-ttu-id="d9e22-125">**Chargennr.**</span><span class="sxs-lookup"><span data-stu-id="d9e22-125">**Lot No.**</span></span>|<span data-ttu-id="d9e22-126">**Menge**</span><span class="sxs-lookup"><span data-stu-id="d9e22-126">**Quantity**</span></span>|  
|-----------------|------------------|  
|<span data-ttu-id="d9e22-127">CH1001</span><span class="sxs-lookup"><span data-stu-id="d9e22-127">CH1001</span></span>|<span data-ttu-id="d9e22-128">80</span><span class="sxs-lookup"><span data-stu-id="d9e22-128">80</span></span>|  
|<span data-ttu-id="d9e22-129">CH1002</span><span class="sxs-lookup"><span data-stu-id="d9e22-129">CH1002</span></span>|<span data-ttu-id="d9e22-130">12</span><span class="sxs-lookup"><span data-stu-id="d9e22-130">12</span></span>|  
|<span data-ttu-id="d9e22-131">CH1003</span><span class="sxs-lookup"><span data-stu-id="d9e22-131">CH1003</span></span>|<span data-ttu-id="d9e22-132">20</span><span class="sxs-lookup"><span data-stu-id="d9e22-132">20</span></span>|  
|<span data-ttu-id="d9e22-133">**Summe**</span><span class="sxs-lookup"><span data-stu-id="d9e22-133">**Total**</span></span>|<span data-ttu-id="d9e22-134">**112**</span><span class="sxs-lookup"><span data-stu-id="d9e22-134">**112**</span></span>|  

<span data-ttu-id="d9e22-135">Bei Abschluss des Inventurauftrags berechnet die Anwendung für den Artikel 80216-V am Lagerort BLAU einen zu buchenden Abgang von 8 Stück und erstellt folgende Posten</span><span class="sxs-lookup"><span data-stu-id="d9e22-135">When finishing the physical inventory order the program will calculate for the item 80216-V at the location BLUE a negative adjustment of 8 pieces and will create the following entries:</span></span>  

## <a name="item-tracking-lines-to-post"></a><span data-ttu-id="d9e22-136">Zu buchende Artikelverfolgungszeilen:</span><span class="sxs-lookup"><span data-stu-id="d9e22-136">Item Tracking lines to post:</span></span>  

|<span data-ttu-id="d9e22-137">**Chargennr.**</span><span class="sxs-lookup"><span data-stu-id="d9e22-137">**Lot No.**</span></span>|<span data-ttu-id="d9e22-138">**Erwartete Menge**</span><span class="sxs-lookup"><span data-stu-id="d9e22-138">**Expected Quantity**</span></span>|<span data-ttu-id="d9e22-139">**Erfasste Menge**</span><span class="sxs-lookup"><span data-stu-id="d9e22-139">**Recorded Quantity**</span></span>|<span data-ttu-id="d9e22-140">**Zu buchende Menge**</span><span class="sxs-lookup"><span data-stu-id="d9e22-140">**Quantity to post**</span></span>|  
|-----------------|---------------------------|---------------------------|--------------------------|  
|<span data-ttu-id="d9e22-141">CH1001</span><span class="sxs-lookup"><span data-stu-id="d9e22-141">CH1001</span></span>|<span data-ttu-id="d9e22-142">80</span><span class="sxs-lookup"><span data-stu-id="d9e22-142">80</span></span>|<span data-ttu-id="d9e22-143">80</span><span class="sxs-lookup"><span data-stu-id="d9e22-143">80</span></span>|<span data-ttu-id="d9e22-144">0</span><span class="sxs-lookup"><span data-stu-id="d9e22-144">0</span></span>|  
|<span data-ttu-id="d9e22-145">CH1002</span><span class="sxs-lookup"><span data-stu-id="d9e22-145">CH1002</span></span>|<span data-ttu-id="d9e22-146">0</span><span class="sxs-lookup"><span data-stu-id="d9e22-146">0</span></span>|<span data-ttu-id="d9e22-147">12</span><span class="sxs-lookup"><span data-stu-id="d9e22-147">12</span></span>|<span data-ttu-id="d9e22-148">+12</span><span class="sxs-lookup"><span data-stu-id="d9e22-148">+ 12</span></span>|  
|<span data-ttu-id="d9e22-149">CH1003</span><span class="sxs-lookup"><span data-stu-id="d9e22-149">CH1003</span></span>|<span data-ttu-id="d9e22-150">30</span><span class="sxs-lookup"><span data-stu-id="d9e22-150">30</span></span>|<span data-ttu-id="d9e22-151">20</span><span class="sxs-lookup"><span data-stu-id="d9e22-151">20</span></span>|<span data-ttu-id="d9e22-152">-10</span><span class="sxs-lookup"><span data-stu-id="d9e22-152">- 10</span></span>|  
|<span data-ttu-id="d9e22-153">CH1006</span><span class="sxs-lookup"><span data-stu-id="d9e22-153">CH1006</span></span>|<span data-ttu-id="d9e22-154">10</span><span class="sxs-lookup"><span data-stu-id="d9e22-154">10</span></span>|<span data-ttu-id="d9e22-155">0</span><span class="sxs-lookup"><span data-stu-id="d9e22-155">0</span></span>|<span data-ttu-id="d9e22-156">-10</span><span class="sxs-lookup"><span data-stu-id="d9e22-156">- 10</span></span>|  
|<span data-ttu-id="d9e22-157">**Summe**</span><span class="sxs-lookup"><span data-stu-id="d9e22-157">**Total**</span></span>|<span data-ttu-id="d9e22-158">**120**</span><span class="sxs-lookup"><span data-stu-id="d9e22-158">**120**</span></span>|<span data-ttu-id="d9e22-159">**112**</span><span class="sxs-lookup"><span data-stu-id="d9e22-159">**112**</span></span>|<span data-ttu-id="d9e22-160">**-8**</span><span class="sxs-lookup"><span data-stu-id="d9e22-160">**- 8**</span></span>|  

## <a name="see-also"></a><span data-ttu-id="d9e22-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9e22-161">See Also</span></span>  
 [<span data-ttu-id="d9e22-162">Inventurauftragszeilen mit Artikelverfolgungszeilen</span><span class="sxs-lookup"><span data-stu-id="d9e22-162">Physical Inventory Order Lines With Item Tracking Lines</span></span>](physical-inventory-order-lines-with-item-tracking-lines.md)  
 [<span data-ttu-id="d9e22-163">Arbeiten mit Chargennummern und Seriennummern</span><span class="sxs-lookup"><span data-stu-id="d9e22-163">Work with Serial and Lot Numbers</span></span>](../../inventory-how-work-item-tracking.md)
