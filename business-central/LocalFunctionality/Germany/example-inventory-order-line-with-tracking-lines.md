---
title: Beispiel - Inventurauftragszeile mit Nachverfolgungszeilen
description: 'Eine Inventurauftragszeile muss die folgenden bestimmten Daten enthalten:'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: d9bcf8b4a9483409a33d796d4f968be357e22670
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="example---inventory-order-line-with-tracking-lines"></a><span data-ttu-id="064f1-103">Beispiel - Inventurauftragszeile mit Nachverfolgungszeilen</span><span class="sxs-lookup"><span data-stu-id="064f1-103">Example - Inventory Order Line with Tracking Lines</span></span>
<span data-ttu-id="064f1-104">Eine Inventurauftragszeile enthält die folgenden buchungsrelevanten Daten:</span><span class="sxs-lookup"><span data-stu-id="064f1-104">The physical inventory order line should contain the following data:</span></span>  

- <span data-ttu-id="064f1-105">Artikelnr.: 80216-V</span><span class="sxs-lookup"><span data-stu-id="064f1-105">Item No.: 80216-V</span></span>  
- <span data-ttu-id="064f1-106">Lagerortcode: BLAU</span><span class="sxs-lookup"><span data-stu-id="064f1-106">Location Code: BLUE</span></span>  
- <span data-ttu-id="064f1-107">Die Felder "Variantencode" und "Lagerplatzcode" sind beide leer.</span><span class="sxs-lookup"><span data-stu-id="064f1-107">The fields Variant Code and Bin Code may be blank.</span></span>  

<span data-ttu-id="064f1-108">Das Kontrollkästchen Verfolgungszeilen verwenden der Inventurauftragszeile wurde aktiviert, und der Artikel 80216-V wird entsprechend seines Artikelverfolgungscodes stets unter Angabe der Chargennummern gebucht.</span><span class="sxs-lookup"><span data-stu-id="064f1-108">There is a check mark in the field Use Tracking Lines on the physical inventory order line and the item 80216-V should be posted all time with lot nos. according to the item tracking code.</span></span>  

<span data-ttu-id="064f1-109">Das Buchungsdatum des Inventurauftragskopfes ist der 31.12.2002.</span><span class="sxs-lookup"><span data-stu-id="064f1-109">The posting date on the physical inventory order header should be 12/31/2002.</span></span>  

<span data-ttu-id="064f1-110">Die erwartete Menge des Artikels 80216-V am Lagerort BLAU zum 31.12.2001 beträgt 120 Stück.</span><span class="sxs-lookup"><span data-stu-id="064f1-110">The expected quantity of the item 80216-V at the location BLUE on 12/31/2001 should be 120 pieces.</span></span>  

<span data-ttu-id="064f1-111">Der Lagerbestand setzt sich aus den folgenden Chargen zusammen:</span><span class="sxs-lookup"><span data-stu-id="064f1-111">The quantity on stock consists of the following lots:</span></span>  

## <a name="the-expected-item-tracking-lines"></a><span data-ttu-id="064f1-112">Die erwarteten Artikelverfolgungszeilen:</span><span class="sxs-lookup"><span data-stu-id="064f1-112">The expected Item Tracking Lines:</span></span>  

|<span data-ttu-id="064f1-113">**Chargennr.**</span><span class="sxs-lookup"><span data-stu-id="064f1-113">**Lot No.**</span></span>|<span data-ttu-id="064f1-114">**Menge**</span><span class="sxs-lookup"><span data-stu-id="064f1-114">**Quantity**</span></span>|  
|-----------------|------------------|  
|<span data-ttu-id="064f1-115">CH1001</span><span class="sxs-lookup"><span data-stu-id="064f1-115">CH1001</span></span>|<span data-ttu-id="064f1-116">80</span><span class="sxs-lookup"><span data-stu-id="064f1-116">80</span></span>|  
|<span data-ttu-id="064f1-117">CH1003</span><span class="sxs-lookup"><span data-stu-id="064f1-117">CH1003</span></span>|<span data-ttu-id="064f1-118">30</span><span class="sxs-lookup"><span data-stu-id="064f1-118">30</span></span>|  
|<span data-ttu-id="064f1-119">CH1006</span><span class="sxs-lookup"><span data-stu-id="064f1-119">CH1006</span></span>|<span data-ttu-id="064f1-120">10</span><span class="sxs-lookup"><span data-stu-id="064f1-120">10</span></span>|  
|<span data-ttu-id="064f1-121">**Summe**</span><span class="sxs-lookup"><span data-stu-id="064f1-121">**Total**</span></span>|<span data-ttu-id="064f1-122">**120**</span><span class="sxs-lookup"><span data-stu-id="064f1-122">**120**</span></span>|  

<span data-ttu-id="064f1-123">Es wurden folgende Inventurerfassungszeilen für Artikel 80216-V, Lagerortcode BLAU, erfasst:</span><span class="sxs-lookup"><span data-stu-id="064f1-123">There had been recorded the following physical inventory recording lines for the item 80216-V, location code BLUE:</span></span>  

## <a name="recorded-lot-nos-on-the-physical-inventory-recording-lines"></a><span data-ttu-id="064f1-124">Erfasste Chargennummern in den Inventurerfassungszeilen:</span><span class="sxs-lookup"><span data-stu-id="064f1-124">Recorded Lot Nos. on the Physical Inventory Recording Lines:</span></span>  

|<span data-ttu-id="064f1-125">**Chargennr.**</span><span class="sxs-lookup"><span data-stu-id="064f1-125">**Lot No.**</span></span>|<span data-ttu-id="064f1-126">**Menge**</span><span class="sxs-lookup"><span data-stu-id="064f1-126">**Quantity**</span></span>|  
|-----------------|------------------|  
|<span data-ttu-id="064f1-127">CH1001</span><span class="sxs-lookup"><span data-stu-id="064f1-127">CH1001</span></span>|<span data-ttu-id="064f1-128">80</span><span class="sxs-lookup"><span data-stu-id="064f1-128">80</span></span>|  
|<span data-ttu-id="064f1-129">CH1002</span><span class="sxs-lookup"><span data-stu-id="064f1-129">CH1002</span></span>|<span data-ttu-id="064f1-130">12</span><span class="sxs-lookup"><span data-stu-id="064f1-130">12</span></span>|  
|<span data-ttu-id="064f1-131">CH1003</span><span class="sxs-lookup"><span data-stu-id="064f1-131">CH1003</span></span>|<span data-ttu-id="064f1-132">20</span><span class="sxs-lookup"><span data-stu-id="064f1-132">20</span></span>|  
|<span data-ttu-id="064f1-133">**Summe**</span><span class="sxs-lookup"><span data-stu-id="064f1-133">**Total**</span></span>|<span data-ttu-id="064f1-134">**112**</span><span class="sxs-lookup"><span data-stu-id="064f1-134">**112**</span></span>|  

<span data-ttu-id="064f1-135">Bei Abschluss des Inventurauftrags berechnet die Anwendung für den Artikel 80216-V am Lagerort BLAU einen zu buchenden Abgang von 8 Stück und erstellt folgende Posten</span><span class="sxs-lookup"><span data-stu-id="064f1-135">When finishing the physical inventory order the program will calculate for the item 80216-V at the location BLUE a negative adjustment of 8 pieces and will create the following entries:</span></span>  

## <a name="item-tracking-lines-to-post"></a><span data-ttu-id="064f1-136">Zu buchende Artikelverfolgungszeilen:</span><span class="sxs-lookup"><span data-stu-id="064f1-136">Item Tracking lines to post:</span></span>  

|<span data-ttu-id="064f1-137">**Chargennr.**</span><span class="sxs-lookup"><span data-stu-id="064f1-137">**Lot No.**</span></span>|<span data-ttu-id="064f1-138">**Erwartete Menge**</span><span class="sxs-lookup"><span data-stu-id="064f1-138">**Expected Quantity**</span></span>|<span data-ttu-id="064f1-139">**Erfasste Menge**</span><span class="sxs-lookup"><span data-stu-id="064f1-139">**Recorded Quantity**</span></span>|<span data-ttu-id="064f1-140">**Zu buchende Menge**</span><span class="sxs-lookup"><span data-stu-id="064f1-140">**Quantity to post**</span></span>|  
|-----------------|---------------------------|---------------------------|--------------------------|  
|<span data-ttu-id="064f1-141">CH1001</span><span class="sxs-lookup"><span data-stu-id="064f1-141">CH1001</span></span>|<span data-ttu-id="064f1-142">80</span><span class="sxs-lookup"><span data-stu-id="064f1-142">80</span></span>|<span data-ttu-id="064f1-143">80</span><span class="sxs-lookup"><span data-stu-id="064f1-143">80</span></span>|<span data-ttu-id="064f1-144">0</span><span class="sxs-lookup"><span data-stu-id="064f1-144">0</span></span>|  
|<span data-ttu-id="064f1-145">CH1002</span><span class="sxs-lookup"><span data-stu-id="064f1-145">CH1002</span></span>|<span data-ttu-id="064f1-146">0</span><span class="sxs-lookup"><span data-stu-id="064f1-146">0</span></span>|<span data-ttu-id="064f1-147">12</span><span class="sxs-lookup"><span data-stu-id="064f1-147">12</span></span>|<span data-ttu-id="064f1-148">+12</span><span class="sxs-lookup"><span data-stu-id="064f1-148">+ 12</span></span>|  
|<span data-ttu-id="064f1-149">CH1003</span><span class="sxs-lookup"><span data-stu-id="064f1-149">CH1003</span></span>|<span data-ttu-id="064f1-150">30</span><span class="sxs-lookup"><span data-stu-id="064f1-150">30</span></span>|<span data-ttu-id="064f1-151">20</span><span class="sxs-lookup"><span data-stu-id="064f1-151">20</span></span>|<span data-ttu-id="064f1-152">-10</span><span class="sxs-lookup"><span data-stu-id="064f1-152">- 10</span></span>|  
|<span data-ttu-id="064f1-153">CH1006</span><span class="sxs-lookup"><span data-stu-id="064f1-153">CH1006</span></span>|<span data-ttu-id="064f1-154">10</span><span class="sxs-lookup"><span data-stu-id="064f1-154">10</span></span>|<span data-ttu-id="064f1-155">0</span><span class="sxs-lookup"><span data-stu-id="064f1-155">0</span></span>|<span data-ttu-id="064f1-156">-10</span><span class="sxs-lookup"><span data-stu-id="064f1-156">- 10</span></span>|  
|<span data-ttu-id="064f1-157">**Summe**</span><span class="sxs-lookup"><span data-stu-id="064f1-157">**Total**</span></span>|<span data-ttu-id="064f1-158">**120**</span><span class="sxs-lookup"><span data-stu-id="064f1-158">**120**</span></span>|<span data-ttu-id="064f1-159">**112**</span><span class="sxs-lookup"><span data-stu-id="064f1-159">**112**</span></span>|<span data-ttu-id="064f1-160">**-8**</span><span class="sxs-lookup"><span data-stu-id="064f1-160">**- 8**</span></span>|  

## <a name="see-also"></a><span data-ttu-id="064f1-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="064f1-161">See Also</span></span>  
 [<span data-ttu-id="064f1-162">Inventurauftragszeilen mit Artikelverfolgungszeilen</span><span class="sxs-lookup"><span data-stu-id="064f1-162">Physical Inventory Order Lines With Item Tracking Lines</span></span>](physical-inventory-order-lines-with-item-tracking-lines.md)  
 [<span data-ttu-id="064f1-163">Arbeiten mit Chargennummern und Seriennummern</span><span class="sxs-lookup"><span data-stu-id="064f1-163">Work with Serial and Lot Numbers</span></span>](../../inventory-how-work-item-tracking.md)

