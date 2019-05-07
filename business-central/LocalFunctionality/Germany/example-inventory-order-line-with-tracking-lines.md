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
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: ../../inventory-how-count-inventory-with-documents
ms.openlocfilehash: fc3f4bca5a09ec4780bded9f5e87d37a4484e9e3
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "919628"
---
# <a name="example---inventory-order-line-with-tracking-lines"></a><span data-ttu-id="afef5-103">Beispiel - Inventurauftragszeile mit Nachverfolgungszeilen</span><span class="sxs-lookup"><span data-stu-id="afef5-103">Example - Inventory Order Line with Tracking Lines</span></span>
<span data-ttu-id="afef5-104">Eine Inventurauftragszeile enthält die folgenden buchungsrelevanten Daten:</span><span class="sxs-lookup"><span data-stu-id="afef5-104">The physical inventory order line should contain the following data:</span></span>  

- <span data-ttu-id="afef5-105">Artikelnr.: 80216-V</span><span class="sxs-lookup"><span data-stu-id="afef5-105">Item No.: 80216-V</span></span>  
- <span data-ttu-id="afef5-106">Lagerortcode: BLAU</span><span class="sxs-lookup"><span data-stu-id="afef5-106">Location Code: BLUE</span></span>  
- <span data-ttu-id="afef5-107">Die Felder "Variantencode" und "Lagerplatzcode" sind beide leer.</span><span class="sxs-lookup"><span data-stu-id="afef5-107">The fields Variant Code and Bin Code may be blank.</span></span>  

<span data-ttu-id="afef5-108">Das Kontrollkästchen Verfolgungszeilen verwenden der Inventurauftragszeile wurde aktiviert, und der Artikel 80216-V wird entsprechend seines Artikelverfolgungscodes stets unter Angabe der Chargennummern gebucht.</span><span class="sxs-lookup"><span data-stu-id="afef5-108">There is a check mark in the field Use Tracking Lines on the physical inventory order line and the item 80216-V should be posted all time with lot nos. according to the item tracking code.</span></span>  

<span data-ttu-id="afef5-109">Das Buchungsdatum des Inventurauftragskopfes ist der 31.12.2002.</span><span class="sxs-lookup"><span data-stu-id="afef5-109">The posting date on the physical inventory order header should be 12/31/2002.</span></span>  

<span data-ttu-id="afef5-110">Die erwartete Menge des Artikels 80216-V am Lagerort BLAU zum 31.12.2001 beträgt 120 Stück.</span><span class="sxs-lookup"><span data-stu-id="afef5-110">The expected quantity of the item 80216-V at the location BLUE on 12/31/2001 should be 120 pieces.</span></span>  

<span data-ttu-id="afef5-111">Der Lagerbestand setzt sich aus den folgenden Chargen zusammen:</span><span class="sxs-lookup"><span data-stu-id="afef5-111">The quantity on stock consists of the following lots:</span></span>  

## <a name="the-expected-item-tracking-lines"></a><span data-ttu-id="afef5-112">Die erwarteten Artikelverfolgungszeilen:</span><span class="sxs-lookup"><span data-stu-id="afef5-112">The expected Item Tracking Lines:</span></span>  

|<span data-ttu-id="afef5-113">**Chargennr.**</span><span class="sxs-lookup"><span data-stu-id="afef5-113">**Lot No.**</span></span>|<span data-ttu-id="afef5-114">**Menge**</span><span class="sxs-lookup"><span data-stu-id="afef5-114">**Quantity**</span></span>|  
|-----------------|------------------|  
|<span data-ttu-id="afef5-115">CH1001</span><span class="sxs-lookup"><span data-stu-id="afef5-115">CH1001</span></span>|<span data-ttu-id="afef5-116">80</span><span class="sxs-lookup"><span data-stu-id="afef5-116">80</span></span>|  
|<span data-ttu-id="afef5-117">CH1003</span><span class="sxs-lookup"><span data-stu-id="afef5-117">CH1003</span></span>|<span data-ttu-id="afef5-118">30</span><span class="sxs-lookup"><span data-stu-id="afef5-118">30</span></span>|  
|<span data-ttu-id="afef5-119">CH1006</span><span class="sxs-lookup"><span data-stu-id="afef5-119">CH1006</span></span>|<span data-ttu-id="afef5-120">10</span><span class="sxs-lookup"><span data-stu-id="afef5-120">10</span></span>|  
|<span data-ttu-id="afef5-121">**Summe**</span><span class="sxs-lookup"><span data-stu-id="afef5-121">**Total**</span></span>|<span data-ttu-id="afef5-122">**120**</span><span class="sxs-lookup"><span data-stu-id="afef5-122">**120**</span></span>|  

<span data-ttu-id="afef5-123">Es wurden folgende Inventurerfassungszeilen für Artikel 80216-V, Lagerortcode BLAU, erfasst:</span><span class="sxs-lookup"><span data-stu-id="afef5-123">There had been recorded the following physical inventory recording lines for the item 80216-V, location code BLUE:</span></span>  

## <a name="recorded-lot-nos-on-the-physical-inventory-recording-lines"></a><span data-ttu-id="afef5-124">Erfasste Chargennummern in den Inventurerfassungszeilen:</span><span class="sxs-lookup"><span data-stu-id="afef5-124">Recorded Lot Nos. on the Physical Inventory Recording Lines:</span></span>  

|<span data-ttu-id="afef5-125">**Chargennr.**</span><span class="sxs-lookup"><span data-stu-id="afef5-125">**Lot No.**</span></span>|<span data-ttu-id="afef5-126">**Menge**</span><span class="sxs-lookup"><span data-stu-id="afef5-126">**Quantity**</span></span>|  
|-----------------|------------------|  
|<span data-ttu-id="afef5-127">CH1001</span><span class="sxs-lookup"><span data-stu-id="afef5-127">CH1001</span></span>|<span data-ttu-id="afef5-128">80</span><span class="sxs-lookup"><span data-stu-id="afef5-128">80</span></span>|  
|<span data-ttu-id="afef5-129">CH1002</span><span class="sxs-lookup"><span data-stu-id="afef5-129">CH1002</span></span>|<span data-ttu-id="afef5-130">12</span><span class="sxs-lookup"><span data-stu-id="afef5-130">12</span></span>|  
|<span data-ttu-id="afef5-131">CH1003</span><span class="sxs-lookup"><span data-stu-id="afef5-131">CH1003</span></span>|<span data-ttu-id="afef5-132">20</span><span class="sxs-lookup"><span data-stu-id="afef5-132">20</span></span>|  
|<span data-ttu-id="afef5-133">**Summe**</span><span class="sxs-lookup"><span data-stu-id="afef5-133">**Total**</span></span>|<span data-ttu-id="afef5-134">**112**</span><span class="sxs-lookup"><span data-stu-id="afef5-134">**112**</span></span>|  

<span data-ttu-id="afef5-135">Bei Abschluss des Inventurauftrags berechnet die Anwendung für den Artikel 80216-V am Lagerort BLAU einen zu buchenden Abgang von 8 Stück und erstellt folgende Posten</span><span class="sxs-lookup"><span data-stu-id="afef5-135">When finishing the physical inventory order the program will calculate for the item 80216-V at the location BLUE a negative adjustment of 8 pieces and will create the following entries:</span></span>  

## <a name="item-tracking-lines-to-post"></a><span data-ttu-id="afef5-136">Zu buchende Artikelverfolgungszeilen:</span><span class="sxs-lookup"><span data-stu-id="afef5-136">Item Tracking lines to post:</span></span>  

|<span data-ttu-id="afef5-137">**Chargennr.**</span><span class="sxs-lookup"><span data-stu-id="afef5-137">**Lot No.**</span></span>|<span data-ttu-id="afef5-138">**Erwartete Menge**</span><span class="sxs-lookup"><span data-stu-id="afef5-138">**Expected Quantity**</span></span>|<span data-ttu-id="afef5-139">**Erfasste Menge**</span><span class="sxs-lookup"><span data-stu-id="afef5-139">**Recorded Quantity**</span></span>|<span data-ttu-id="afef5-140">**Zu buchende Menge**</span><span class="sxs-lookup"><span data-stu-id="afef5-140">**Quantity to post**</span></span>|  
|-----------------|---------------------------|---------------------------|--------------------------|  
|<span data-ttu-id="afef5-141">CH1001</span><span class="sxs-lookup"><span data-stu-id="afef5-141">CH1001</span></span>|<span data-ttu-id="afef5-142">80</span><span class="sxs-lookup"><span data-stu-id="afef5-142">80</span></span>|<span data-ttu-id="afef5-143">80</span><span class="sxs-lookup"><span data-stu-id="afef5-143">80</span></span>|<span data-ttu-id="afef5-144">0</span><span class="sxs-lookup"><span data-stu-id="afef5-144">0</span></span>|  
|<span data-ttu-id="afef5-145">CH1002</span><span class="sxs-lookup"><span data-stu-id="afef5-145">CH1002</span></span>|<span data-ttu-id="afef5-146">0</span><span class="sxs-lookup"><span data-stu-id="afef5-146">0</span></span>|<span data-ttu-id="afef5-147">12</span><span class="sxs-lookup"><span data-stu-id="afef5-147">12</span></span>|<span data-ttu-id="afef5-148">+12</span><span class="sxs-lookup"><span data-stu-id="afef5-148">+ 12</span></span>|  
|<span data-ttu-id="afef5-149">CH1003</span><span class="sxs-lookup"><span data-stu-id="afef5-149">CH1003</span></span>|<span data-ttu-id="afef5-150">30</span><span class="sxs-lookup"><span data-stu-id="afef5-150">30</span></span>|<span data-ttu-id="afef5-151">20</span><span class="sxs-lookup"><span data-stu-id="afef5-151">20</span></span>|<span data-ttu-id="afef5-152">-10</span><span class="sxs-lookup"><span data-stu-id="afef5-152">- 10</span></span>|  
|<span data-ttu-id="afef5-153">CH1006</span><span class="sxs-lookup"><span data-stu-id="afef5-153">CH1006</span></span>|<span data-ttu-id="afef5-154">10</span><span class="sxs-lookup"><span data-stu-id="afef5-154">10</span></span>|<span data-ttu-id="afef5-155">0</span><span class="sxs-lookup"><span data-stu-id="afef5-155">0</span></span>|<span data-ttu-id="afef5-156">-10</span><span class="sxs-lookup"><span data-stu-id="afef5-156">- 10</span></span>|  
|<span data-ttu-id="afef5-157">**Summe**</span><span class="sxs-lookup"><span data-stu-id="afef5-157">**Total**</span></span>|<span data-ttu-id="afef5-158">**120**</span><span class="sxs-lookup"><span data-stu-id="afef5-158">**120**</span></span>|<span data-ttu-id="afef5-159">**112**</span><span class="sxs-lookup"><span data-stu-id="afef5-159">**112**</span></span>|<span data-ttu-id="afef5-160">**-8**</span><span class="sxs-lookup"><span data-stu-id="afef5-160">**- 8**</span></span>|  

## <a name="see-also"></a><span data-ttu-id="afef5-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="afef5-161">See Also</span></span>  
 [<span data-ttu-id="afef5-162">Inventurauftragszeilen mit Artikelverfolgungszeilen</span><span class="sxs-lookup"><span data-stu-id="afef5-162">Physical Inventory Order Lines With Item Tracking Lines</span></span>](physical-inventory-order-lines-with-item-tracking-lines.md)  
 [<span data-ttu-id="afef5-163">Arbeiten mit Chargennummern und Seriennummern</span><span class="sxs-lookup"><span data-stu-id="afef5-163">Work with Serial and Lot Numbers</span></span>](../../inventory-how-work-item-tracking.md)
