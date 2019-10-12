---
title: Beispiel - Inventurauftragszeile mit Nachverfolgungszeilen
description: 'Eine Inventurauftragszeile muss die folgenden bestimmten Daten enthalten:'
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
redirect_url: ../../inventory-how-count-inventory-with-documents
ms.openlocfilehash: 8d663849e34f0e5a6a69cf19b17e8cd9d3ab89c7
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2301334"
---
# <a name="example---inventory-order-line-with-tracking-lines"></a><span data-ttu-id="eec37-103">Beispiel - Inventurauftragszeile mit Nachverfolgungszeilen</span><span class="sxs-lookup"><span data-stu-id="eec37-103">Example - Inventory Order Line with Tracking Lines</span></span>
<span data-ttu-id="eec37-104">Eine Inventurauftragszeile enthält die folgenden buchungsrelevanten Daten:</span><span class="sxs-lookup"><span data-stu-id="eec37-104">The physical inventory order line should contain the following data:</span></span>  

- <span data-ttu-id="eec37-105">Artikelnr.: 80216-V</span><span class="sxs-lookup"><span data-stu-id="eec37-105">Item No.: 80216-V</span></span>  
- <span data-ttu-id="eec37-106">Lagerortcode: BLAU</span><span class="sxs-lookup"><span data-stu-id="eec37-106">Location Code: BLUE</span></span>  
- <span data-ttu-id="eec37-107">Die Felder "Variantencode" und "Lagerplatzcode" sind beide leer.</span><span class="sxs-lookup"><span data-stu-id="eec37-107">The fields Variant Code and Bin Code may be blank.</span></span>  

<span data-ttu-id="eec37-108">Das Kontrollkästchen Verfolgungszeilen verwenden der Inventurauftragszeile wurde aktiviert, und der Artikel 80216-V wird entsprechend seines Artikelverfolgungscodes stets unter Angabe der Chargennummern gebucht.</span><span class="sxs-lookup"><span data-stu-id="eec37-108">There is a check mark in the field Use Tracking Lines on the physical inventory order line and the item 80216-V should be posted all time with lot nos. according to the item tracking code.</span></span>  

<span data-ttu-id="eec37-109">Das Buchungsdatum des Inventurauftragskopfes ist der 31.12.2002.</span><span class="sxs-lookup"><span data-stu-id="eec37-109">The posting date on the physical inventory order header should be 12/31/2002.</span></span>  

<span data-ttu-id="eec37-110">Die erwartete Menge des Artikels 80216-V am Lagerort BLAU zum 31.12.2001 beträgt 120 Stück.</span><span class="sxs-lookup"><span data-stu-id="eec37-110">The expected quantity of the item 80216-V at the location BLUE on 12/31/2001 should be 120 pieces.</span></span>  

<span data-ttu-id="eec37-111">Der Lagerbestand setzt sich aus den folgenden Chargen zusammen:</span><span class="sxs-lookup"><span data-stu-id="eec37-111">The quantity on stock consists of the following lots:</span></span>  

## <a name="the-expected-item-tracking-lines"></a><span data-ttu-id="eec37-112">Die erwarteten Artikelverfolgungszeilen:</span><span class="sxs-lookup"><span data-stu-id="eec37-112">The expected Item Tracking Lines:</span></span>  

|<span data-ttu-id="eec37-113">**Chargennr.**</span><span class="sxs-lookup"><span data-stu-id="eec37-113">**Lot No.**</span></span>|<span data-ttu-id="eec37-114">**Menge**</span><span class="sxs-lookup"><span data-stu-id="eec37-114">**Quantity**</span></span>|  
|-----------------|------------------|  
|<span data-ttu-id="eec37-115">CH1001</span><span class="sxs-lookup"><span data-stu-id="eec37-115">CH1001</span></span>|<span data-ttu-id="eec37-116">80</span><span class="sxs-lookup"><span data-stu-id="eec37-116">80</span></span>|  
|<span data-ttu-id="eec37-117">CH1003</span><span class="sxs-lookup"><span data-stu-id="eec37-117">CH1003</span></span>|<span data-ttu-id="eec37-118">30</span><span class="sxs-lookup"><span data-stu-id="eec37-118">30</span></span>|  
|<span data-ttu-id="eec37-119">CH1006</span><span class="sxs-lookup"><span data-stu-id="eec37-119">CH1006</span></span>|<span data-ttu-id="eec37-120">10</span><span class="sxs-lookup"><span data-stu-id="eec37-120">10</span></span>|  
|<span data-ttu-id="eec37-121">**Summe**</span><span class="sxs-lookup"><span data-stu-id="eec37-121">**Total**</span></span>|<span data-ttu-id="eec37-122">**120**</span><span class="sxs-lookup"><span data-stu-id="eec37-122">**120**</span></span>|  

<span data-ttu-id="eec37-123">Es wurden folgende Inventurerfassungszeilen für Artikel 80216-V, Lagerortcode BLAU, erfasst:</span><span class="sxs-lookup"><span data-stu-id="eec37-123">There had been recorded the following physical inventory recording lines for the item 80216-V, location code BLUE:</span></span>  

## <a name="recorded-lot-nos-on-the-physical-inventory-recording-lines"></a><span data-ttu-id="eec37-124">Erfasste Chargennummern in den Inventurerfassungszeilen:</span><span class="sxs-lookup"><span data-stu-id="eec37-124">Recorded Lot Nos. on the Physical Inventory Recording Lines:</span></span>  

|<span data-ttu-id="eec37-125">**Chargennr.**</span><span class="sxs-lookup"><span data-stu-id="eec37-125">**Lot No.**</span></span>|<span data-ttu-id="eec37-126">**Menge**</span><span class="sxs-lookup"><span data-stu-id="eec37-126">**Quantity**</span></span>|  
|-----------------|------------------|  
|<span data-ttu-id="eec37-127">CH1001</span><span class="sxs-lookup"><span data-stu-id="eec37-127">CH1001</span></span>|<span data-ttu-id="eec37-128">80</span><span class="sxs-lookup"><span data-stu-id="eec37-128">80</span></span>|  
|<span data-ttu-id="eec37-129">CH1002</span><span class="sxs-lookup"><span data-stu-id="eec37-129">CH1002</span></span>|<span data-ttu-id="eec37-130">12</span><span class="sxs-lookup"><span data-stu-id="eec37-130">12</span></span>|  
|<span data-ttu-id="eec37-131">CH1003</span><span class="sxs-lookup"><span data-stu-id="eec37-131">CH1003</span></span>|<span data-ttu-id="eec37-132">20</span><span class="sxs-lookup"><span data-stu-id="eec37-132">20</span></span>|  
|<span data-ttu-id="eec37-133">**Summe**</span><span class="sxs-lookup"><span data-stu-id="eec37-133">**Total**</span></span>|<span data-ttu-id="eec37-134">**112**</span><span class="sxs-lookup"><span data-stu-id="eec37-134">**112**</span></span>|  

<span data-ttu-id="eec37-135">Bei Abschluss des Inventurauftrags berechnet die Anwendung für den Artikel 80216-V am Lagerort BLAU einen zu buchenden Abgang von 8 Stück und erstellt folgende Posten</span><span class="sxs-lookup"><span data-stu-id="eec37-135">When finishing the physical inventory order application will calculate for the item 80216-V at the location BLUE a negative adjustment of 8 pieces and will create the following entries:</span></span>  

## <a name="item-tracking-lines-to-post"></a><span data-ttu-id="eec37-136">Zu buchende Artikelverfolgungszeilen:</span><span class="sxs-lookup"><span data-stu-id="eec37-136">Item Tracking lines to post:</span></span>  

|<span data-ttu-id="eec37-137">**Chargennr.**</span><span class="sxs-lookup"><span data-stu-id="eec37-137">**Lot No.**</span></span>|<span data-ttu-id="eec37-138">**Erwartete Menge**</span><span class="sxs-lookup"><span data-stu-id="eec37-138">**Expected Quantity**</span></span>|<span data-ttu-id="eec37-139">**Erfasste Menge**</span><span class="sxs-lookup"><span data-stu-id="eec37-139">**Recorded Quantity**</span></span>|<span data-ttu-id="eec37-140">**Zu buchende Menge**</span><span class="sxs-lookup"><span data-stu-id="eec37-140">**Quantity to post**</span></span>|  
|-----------------|---------------------------|---------------------------|--------------------------|  
|<span data-ttu-id="eec37-141">CH1001</span><span class="sxs-lookup"><span data-stu-id="eec37-141">CH1001</span></span>|<span data-ttu-id="eec37-142">80</span><span class="sxs-lookup"><span data-stu-id="eec37-142">80</span></span>|<span data-ttu-id="eec37-143">80</span><span class="sxs-lookup"><span data-stu-id="eec37-143">80</span></span>|<span data-ttu-id="eec37-144">0</span><span class="sxs-lookup"><span data-stu-id="eec37-144">0</span></span>|  
|<span data-ttu-id="eec37-145">CH1002</span><span class="sxs-lookup"><span data-stu-id="eec37-145">CH1002</span></span>|<span data-ttu-id="eec37-146">0</span><span class="sxs-lookup"><span data-stu-id="eec37-146">0</span></span>|<span data-ttu-id="eec37-147">12</span><span class="sxs-lookup"><span data-stu-id="eec37-147">12</span></span>|<span data-ttu-id="eec37-148">+12</span><span class="sxs-lookup"><span data-stu-id="eec37-148">+ 12</span></span>|  
|<span data-ttu-id="eec37-149">CH1003</span><span class="sxs-lookup"><span data-stu-id="eec37-149">CH1003</span></span>|<span data-ttu-id="eec37-150">30</span><span class="sxs-lookup"><span data-stu-id="eec37-150">30</span></span>|<span data-ttu-id="eec37-151">20</span><span class="sxs-lookup"><span data-stu-id="eec37-151">20</span></span>|<span data-ttu-id="eec37-152">-10</span><span class="sxs-lookup"><span data-stu-id="eec37-152">- 10</span></span>|  
|<span data-ttu-id="eec37-153">CH1006</span><span class="sxs-lookup"><span data-stu-id="eec37-153">CH1006</span></span>|<span data-ttu-id="eec37-154">10</span><span class="sxs-lookup"><span data-stu-id="eec37-154">10</span></span>|<span data-ttu-id="eec37-155">0</span><span class="sxs-lookup"><span data-stu-id="eec37-155">0</span></span>|<span data-ttu-id="eec37-156">-10</span><span class="sxs-lookup"><span data-stu-id="eec37-156">- 10</span></span>|  
|<span data-ttu-id="eec37-157">**Summe**</span><span class="sxs-lookup"><span data-stu-id="eec37-157">**Total**</span></span>|<span data-ttu-id="eec37-158">**120**</span><span class="sxs-lookup"><span data-stu-id="eec37-158">**120**</span></span>|<span data-ttu-id="eec37-159">**112**</span><span class="sxs-lookup"><span data-stu-id="eec37-159">**112**</span></span>|<span data-ttu-id="eec37-160">**-8**</span><span class="sxs-lookup"><span data-stu-id="eec37-160">**- 8**</span></span>|  

## <a name="see-also"></a><span data-ttu-id="eec37-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eec37-161">See Also</span></span>  
 [<span data-ttu-id="eec37-162">Inventurauftragszeilen mit Artikelverfolgungszeilen</span><span class="sxs-lookup"><span data-stu-id="eec37-162">Physical Inventory Order Lines With Item Tracking Lines</span></span>](physical-inventory-order-lines-with-item-tracking-lines.md)  
 [<span data-ttu-id="eec37-163">Arbeiten mit Chargennummern und Seriennummern</span><span class="sxs-lookup"><span data-stu-id="eec37-163">Work with Serial and Lot Numbers</span></span>](../../inventory-how-work-item-tracking.md)
