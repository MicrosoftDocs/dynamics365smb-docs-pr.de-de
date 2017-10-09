---
title: Siehe Planung mit/ohne Lagerortcodes  | Microsoft Docs
description: Die Planung mit oder ohne Lagerortcodes unter diesen Voraussetzungen in geradliniger Weise ist wichtig zu verstehen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 964bcd38897e676baa993399fe772b8ccfdc9ea0
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="planning-with-or-without-locations"></a><span data-ttu-id="98f9c-103">Siehe Planung mit/ohne Lagerortcodes.</span><span class="sxs-lookup"><span data-stu-id="98f9c-103">Planning With or Without Locations</span></span>
<span data-ttu-id="98f9c-104">In der Planung mit oder ohne Lagerortcodes in Bedarfszeilen arbeitet das Planungssystem unter diesen Voraussetzungen in geradliniger Weise:</span><span class="sxs-lookup"><span data-stu-id="98f9c-104">Concerning planning with or without location codes on demand lines, the planning system operates in a straight forward way when:</span></span>  

-   <span data-ttu-id="98f9c-105">Die Bedarfszeilen enthalten immer Lagerortcodes, und das System verwendet in vollem Umfang Lagerhaltungsdaten, einschließlich der betreffenden Lagerorteinrichtung.</span><span class="sxs-lookup"><span data-stu-id="98f9c-105">demand lines always carry location codes and the system fully uses stockkeeping units, including the relevant location setup.</span></span>  
-   <span data-ttu-id="98f9c-106">Die Bedarfszeilen enthalten nie Lagerortcodes, und das System verwendet keine Lagerhaltungsdaten oder irgendeine Lagerorteinrichtung (siehe letztes Szenario unten).</span><span class="sxs-lookup"><span data-stu-id="98f9c-106">demand lines never carry location codes and the system does not use SKUs or any location setup (see last scenario below).</span></span>  

<span data-ttu-id="98f9c-107">Wenn jedoch die Bedarfszeilen manchmal Lagerortcodes aufweisen und manchmal nicht, folgt das Planungssystem je nach Einrichtung bestimmten Regeln.</span><span class="sxs-lookup"><span data-stu-id="98f9c-107">However, if demand lines sometimes have location codes and other times do not, the planning system will follow certain rules depending on setup.</span></span>  

## <a name="demand-at-location"></a><span data-ttu-id="98f9c-108">Bedarf am Lagerort</span><span class="sxs-lookup"><span data-stu-id="98f9c-108">Demand at Location</span></span>  
<span data-ttu-id="98f9c-109">Wenn das Planungssystem Bedarf an einem Lagerort (eine Zeile mit einem Lagerortcode) erkennt, verhält es sich in verschiedener Weise, abhängig von drei kritischen Konfigurationswerten.</span><span class="sxs-lookup"><span data-stu-id="98f9c-109">When the planning system detects demand at a location (a line with a location code), it will behave in different ways depending on 3 critical setup values.</span></span>  

<span data-ttu-id="98f9c-110">Während eines Planungslaufs führt das System der Reihe nach eine Überprüfung auf die drei Konfigurationswerte durch und plant entsprechend:</span><span class="sxs-lookup"><span data-stu-id="98f9c-110">During a planning run, the system checks for the 3 setup values in sequence and plans accordingly:</span></span>  

1.  <span data-ttu-id="98f9c-111">Ist das Feld **Lagerort notwendig** mit einem Häkchen markiert?</span><span class="sxs-lookup"><span data-stu-id="98f9c-111">Is there a check mark in the **Location Mandatory** field?</span></span>  

    <span data-ttu-id="98f9c-112">Falls ja:</span><span class="sxs-lookup"><span data-stu-id="98f9c-112">If yes, then:</span></span>  

2.  <span data-ttu-id="98f9c-113">Sind Lagerhaltungsdaten für den Artikel vorhanden?</span><span class="sxs-lookup"><span data-stu-id="98f9c-113">Does SKU exist for the item?</span></span>  

    <span data-ttu-id="98f9c-114">Falls ja:</span><span class="sxs-lookup"><span data-stu-id="98f9c-114">If yes, then:</span></span>  

    <span data-ttu-id="98f9c-115">Der Artikel wird gemäß den Planungsparametern auf der Lagerhaltungsdatenkarte geplant.</span><span class="sxs-lookup"><span data-stu-id="98f9c-115">The item is planned according to planning parameters on the SKU card.</span></span>  

    <span data-ttu-id="98f9c-116">Falls nein:</span><span class="sxs-lookup"><span data-stu-id="98f9c-116">If no, then:</span></span>  

3.  <span data-ttu-id="98f9c-117">Enthält das Feld **Komponenten von Lagerort** den angeforderen Lagerortcode?</span><span class="sxs-lookup"><span data-stu-id="98f9c-117">Does the **Components at Location** field contain the demanded location code?</span></span>  

    <span data-ttu-id="98f9c-118">Falls ja:</span><span class="sxs-lookup"><span data-stu-id="98f9c-118">If yes, then:</span></span>  

    <span data-ttu-id="98f9c-119">Der Artikel wird gemäß den Planungsparametern auf der Artikelkarte geplant.</span><span class="sxs-lookup"><span data-stu-id="98f9c-119">The item is planned according to planning parameters on the item card.</span></span>  

    <span data-ttu-id="98f9c-120">Falls nein:</span><span class="sxs-lookup"><span data-stu-id="98f9c-120">If no, then:</span></span>  

    <span data-ttu-id="98f9c-121">Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren =  *Los-für-Los*, Lagerbestand berücksichtigen =  *Ja*, alle anderen Planungsparameter = Leer.</span><span class="sxs-lookup"><span data-stu-id="98f9c-121">The item is planned according to: Reordering Policy =  *Lot-for-Lot*, Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span> <span data-ttu-id="98f9c-122">(Artikel mit dem Wiederbeschaffungsverfahren  *Bestellung* verbleiben auf  *Bestellung* sowie auf allen anderen für sie festgelegten Einstellungen.)</span><span class="sxs-lookup"><span data-stu-id="98f9c-122">(Items using reordering policy  *Order* remain using  *Order* as well as the other settings.)</span></span>  

> [!NOTE]  
>  <span data-ttu-id="98f9c-123">Diese Minimalalternative deckt nur den exakten Bedarf ab.</span><span class="sxs-lookup"><span data-stu-id="98f9c-123">This minimal alternative only covers the exact demand.</span></span> <span data-ttu-id="98f9c-124">Alle definierten Planungsparameter werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="98f9c-124">Any planning parameters defined are ignored.</span></span>  

<span data-ttu-id="98f9c-125">Siehe Abweichungen in den unten angeführten Szenarien.</span><span class="sxs-lookup"><span data-stu-id="98f9c-125">See variations in the scenarios below.</span></span>  

## <a name="demand-at-blank-location"></a><span data-ttu-id="98f9c-126">Bedarf an "leerer Lagerort"</span><span class="sxs-lookup"><span data-stu-id="98f9c-126">Demand at "Blank Location"</span></span>  
<span data-ttu-id="98f9c-127">Selbst bei markiertem Feld **Lagerort notwendig** erlaubt das System die Erstellung von Bedarfszeilen ohne Lagerortcode – auch als Lagerort *LEER* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="98f9c-127">Even if the **Location Mandatory** check box is selected, the system will allow demand lines to be created without a location code – also referred to as *BLANK* location.</span></span> <span data-ttu-id="98f9c-128">Dies stellt für das System eine Abweichung dar, weil mehrere Konfigurationswerte für die Behandlung von Lagerorten optimiert sind, und im Ergebnis erstellt das Planungsmodul für eine solche Bedarfszeile keine Planungszeile.</span><span class="sxs-lookup"><span data-stu-id="98f9c-128">This is a deviation for the system because it has various setup values tuned to dealing with locations (see above) and as a result, the planning engine will not create a planning line for such a demand line.</span></span> <span data-ttu-id="98f9c-129">Wenn das Feld **Lagerort notwendig** nicht markiert ist, jedoch andere Konfigurationswerte für den Lagerort vorhanden sind, wird auch dieser Fall als Abweichung betrachtet, und das Planungssystem reagiert mit der Ausgabe der "Minimalalternative":</span><span class="sxs-lookup"><span data-stu-id="98f9c-129">If the **Location Mandatory** field is not selected but any of the location setup values exist, then that is also considered a deviation and the planning system will react by outputting the "minimal alternative":</span></span>   
<span data-ttu-id="98f9c-130">Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren =  *Los-für-Los* ( *Bestellung* bleibt *Bestellung*), Lagerbestand berücksichtigen =  *Ja*, alle anderen Planungsparameter = Leer.</span><span class="sxs-lookup"><span data-stu-id="98f9c-130">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains *Order)*, Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

<span data-ttu-id="98f9c-131">Siehe Abweichungen in den unten angeführte Setup-Szenarien.</span><span class="sxs-lookup"><span data-stu-id="98f9c-131">See variations in the setup scenarios below.</span></span>  

### <a name="setup-1"></a><span data-ttu-id="98f9c-132">Konfiguration 1:</span><span class="sxs-lookup"><span data-stu-id="98f9c-132">Setup 1:</span></span>  

-   <span data-ttu-id="98f9c-133">Lagerort notwendig = *Ja*</span><span class="sxs-lookup"><span data-stu-id="98f9c-133">Location Mandatory = *Yes*</span></span>  
-   <span data-ttu-id="98f9c-134">Lagerhaltungsdaten sind für  *ROT* eingerichtet</span><span class="sxs-lookup"><span data-stu-id="98f9c-134">SKU is set up for  *RED*</span></span>  
-   <span data-ttu-id="98f9c-135">Komponente an Lagerort =  *BLAU*</span><span class="sxs-lookup"><span data-stu-id="98f9c-135">Component at Location =  *BLUE*</span></span>  

#### <a name="case-11-demand-is-at--red-location"></a><span data-ttu-id="98f9c-136">Fall 1.1: Es besteht Bedarf am Lagerort  *ROT*</span><span class="sxs-lookup"><span data-stu-id="98f9c-136">Case 1.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="98f9c-137">Der Artikel wird gemäß den Planungsparametern auf der Lagerhaltungsdatenkarte geplant (einschließlich möglicher Umlagerungen).</span><span class="sxs-lookup"><span data-stu-id="98f9c-137">The item is planned according to planning parameters on the SKU card (including possible transfer).</span></span>  

#### <a name="case-12-demand-is-at--blue-location"></a><span data-ttu-id="98f9c-138">Fall 1.2: Es besteht Bedarf am Lagerort *BLAU*</span><span class="sxs-lookup"><span data-stu-id="98f9c-138">Case 1.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="98f9c-139">Der Artikel wird gemäß den Planungsparametern auf der Artikelkarte geplant.</span><span class="sxs-lookup"><span data-stu-id="98f9c-139">The item is planned according to planning parameters on the item card.</span></span>  

#### <a name="case-13-demand-is-at--green-location"></a><span data-ttu-id="98f9c-140">Fall 1.3: Es besteht Bedarf am Lagerort  *GRÜN*</span><span class="sxs-lookup"><span data-stu-id="98f9c-140">Case 1.3: Demand is at  *GREEN* location</span></span>  

<span data-ttu-id="98f9c-141">Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren =  *Los-für-Los* ( *Bestellung* bleibt  *Bestellung*), Lagerbestand berücksichtigen =  *Ja*, alle anderen Planungsparameter = Leer.</span><span class="sxs-lookup"><span data-stu-id="98f9c-141">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-14-demand-is-at--blank-location"></a><span data-ttu-id="98f9c-142">Fall 1.4: Es besteht Bedarf am Lagerort *LEER*</span><span class="sxs-lookup"><span data-stu-id="98f9c-142">Case 1.4: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="98f9c-143">Der Artikel wird nicht geplant, weil kein Lagerort in der Bedarfszeile definiert ist.</span><span class="sxs-lookup"><span data-stu-id="98f9c-143">The item is not planned because no location is defined on the demand line.</span></span>  

### <a name="setup-2"></a><span data-ttu-id="98f9c-144">Konfiguration 2:</span><span class="sxs-lookup"><span data-stu-id="98f9c-144">Setup 2:</span></span>  

-   <span data-ttu-id="98f9c-145">Lagerort notwendig = *Ja*</span><span class="sxs-lookup"><span data-stu-id="98f9c-145">Location Mandatory = *Yes*</span></span>  
-   <span data-ttu-id="98f9c-146">Es sind keine Lagerhaltungsdaten vorhanden.</span><span class="sxs-lookup"><span data-stu-id="98f9c-146">No SKU exists</span></span>  
-   <span data-ttu-id="98f9c-147">Komponente an Lagerort =  *BLAU*</span><span class="sxs-lookup"><span data-stu-id="98f9c-147">Component at Location =  *BLUE*</span></span>  

#### <a name="case-21-demand-is-at--red-location"></a><span data-ttu-id="98f9c-148">Fall 2.1: Es besteht Bedarf am Lagerort  *ROT*</span><span class="sxs-lookup"><span data-stu-id="98f9c-148">Case 2.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="98f9c-149">Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren =  *Los-für-Los* ( *Bestellung* bleibt  *Bestellung*), Lagerbestand berücksichtigen =  *Ja*, alle anderen Planungsparameter = Leer.</span><span class="sxs-lookup"><span data-stu-id="98f9c-149">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-22-demand-is-at--blue-location"></a><span data-ttu-id="98f9c-150">Fall 2.2: Es besteht Bedarf am Lagerort *BLAU*</span><span class="sxs-lookup"><span data-stu-id="98f9c-150">Case 2.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="98f9c-151">Der Artikel wird gemäß den Planungsparametern auf der Artikelkarte geplant.</span><span class="sxs-lookup"><span data-stu-id="98f9c-151">The item is planned according to planning parameters on the item card.</span></span>  

### <a name="setup-3"></a><span data-ttu-id="98f9c-152">Konfiguration 3:</span><span class="sxs-lookup"><span data-stu-id="98f9c-152">Setup 3:</span></span>  

-   <span data-ttu-id="98f9c-153">Lagerort notwendig = *Nein*</span><span class="sxs-lookup"><span data-stu-id="98f9c-153">Location Mandatory = *No*</span></span>  
-   <span data-ttu-id="98f9c-154">Es sind keine Lagerhaltungsdaten vorhanden.</span><span class="sxs-lookup"><span data-stu-id="98f9c-154">No SKU exists</span></span>  
-   <span data-ttu-id="98f9c-155">Komponente an Lagerort =  *BLAU*</span><span class="sxs-lookup"><span data-stu-id="98f9c-155">Component at Location =  *BLUE*</span></span>  

#### <a name="case-31-demand-is-at--red-location"></a><span data-ttu-id="98f9c-156">Fall 3.1: Es besteht Bedarf am Lagerort  *ROT*</span><span class="sxs-lookup"><span data-stu-id="98f9c-156">Case 3.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="98f9c-157">Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren =  *Los-für-Los* ( *Bestellung* bleibt  *Bestellung*), Lagerbestand berücksichtigen =  *Ja*, alle anderen Planungsparameter = Leer.</span><span class="sxs-lookup"><span data-stu-id="98f9c-157">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-32-demand-is-at--blue-location"></a><span data-ttu-id="98f9c-158">Fall 3.2: Es besteht Bedarf am Lagerort *BLAU*</span><span class="sxs-lookup"><span data-stu-id="98f9c-158">Case 3.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="98f9c-159">Der Artikel wird gemäß den Planungsparametern auf der Artikelkarte geplant.</span><span class="sxs-lookup"><span data-stu-id="98f9c-159">The item is planned according to planning parameters on the item card.</span></span>  

#### <a name="case-33-demand-is-at--blank-location"></a><span data-ttu-id="98f9c-160">Fall 3.3: Es besteht Bedarf am Lagerort  *LEER*</span><span class="sxs-lookup"><span data-stu-id="98f9c-160">Case 3.3: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="98f9c-161">Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren =  *Los-für-Los* ( *Bestellung* bleibt  *Bestellung*), Lagerbestand berücksichtigen =  *Ja*, alle anderen Planungsparameter = Leer.</span><span class="sxs-lookup"><span data-stu-id="98f9c-161">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

### <a name="setup-4"></a><span data-ttu-id="98f9c-162">Konfiguration 4:</span><span class="sxs-lookup"><span data-stu-id="98f9c-162">Setup 4:</span></span>  

-   <span data-ttu-id="98f9c-163">Lagerort notwendig = *Nein*</span><span class="sxs-lookup"><span data-stu-id="98f9c-163">Location Mandatory = *No*</span></span>  
-   <span data-ttu-id="98f9c-164">Es sind keine Lagerhaltungsdaten vorhanden.</span><span class="sxs-lookup"><span data-stu-id="98f9c-164">No SKU exists</span></span>  
-   <span data-ttu-id="98f9c-165">Komponente an Lagerort =  *LEER*</span><span class="sxs-lookup"><span data-stu-id="98f9c-165">Component at Location =  *BLANK*</span></span>  

#### <a name="case-41-demand-is-at--blue-location"></a><span data-ttu-id="98f9c-166">Fall 4.1: Es besteht Bedarf am Lagerort  *BLAU*</span><span class="sxs-lookup"><span data-stu-id="98f9c-166">Case 4.1: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="98f9c-167">Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren =  *Los-für-Los* ( *Bestellung* bleibt  *Bestellung*), Lagerbestand berücksichtigen =  *Ja*, alle anderen Planungsparameter = Leer.</span><span class="sxs-lookup"><span data-stu-id="98f9c-167">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-42-demand-is-at--blank-location"></a><span data-ttu-id="98f9c-168">Fall 4.2: Es besteht Bedarf am Lagerort  *LEER*</span><span class="sxs-lookup"><span data-stu-id="98f9c-168">Case 4.2: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="98f9c-169">Der Artikel wird gemäß den Planungsparametern auf der Artikelkarte geplant.</span><span class="sxs-lookup"><span data-stu-id="98f9c-169">The item is planned according to planning parameters on the item card.</span></span>  

<span data-ttu-id="98f9c-170">Wie aus dem letzten Szenario ersehen werden kann, besteht die einzige Möglichkeit, ein richtiges Ergebnis für eine Bedarfszeile ohne Lagerortcode zu erhalten, im Deaktivieren aller konfigurierten Werte, die sich auf Lagerorte beziehen.</span><span class="sxs-lookup"><span data-stu-id="98f9c-170">As you can see from the last scenario, the only way to get a correct result for a demand line without a location code is to disable all setup values relating to locations.</span></span> <span data-ttu-id="98f9c-171">Analog besteht die einzige Möglichkeit, stabile Planungsergebnisse für den Bedarf an den Lagerorten zu erhalten, in der Verwendung von Lagerhaltungsdaten.</span><span class="sxs-lookup"><span data-stu-id="98f9c-171">Similarly, the only way to get stable planning results for demand at locations is to use stockkeeping units.</span></span>  

<span data-ttu-id="98f9c-172">Wenn Sie häufig den Bedarf an Lagerorten planen müssen, empfiehlt sich daher dringend die Verwendung der Funktion Lagerhaltungsdaten.</span><span class="sxs-lookup"><span data-stu-id="98f9c-172">Therefore, if you often plan for demand at locations, it is strongly advised to use the Stockkeeping Units feature.</span></span>  

## <a name="see-also"></a><span data-ttu-id="98f9c-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98f9c-173">See Also</span></span>
<span data-ttu-id="98f9c-174">[Planung](production-planning.md)  </span><span class="sxs-lookup"><span data-stu-id="98f9c-174">[Planning](production-planning.md)  </span></span>  
[<span data-ttu-id="98f9c-175">Produktion einrichten</span><span class="sxs-lookup"><span data-stu-id="98f9c-175">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="98f9c-176">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="98f9c-176">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="98f9c-177">Lagerbest</span><span class="sxs-lookup"><span data-stu-id="98f9c-177">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="98f9c-178">Einkauf</span><span class="sxs-lookup"><span data-stu-id="98f9c-178">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="98f9c-179">[Designdetails: Vorratsplanung](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="98f9c-179">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="98f9c-180">Bewährte Einrichtungsmethoden: Beschaffungsplanung</span><span class="sxs-lookup"><span data-stu-id="98f9c-180">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="98f9c-181">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="98f9c-181">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

