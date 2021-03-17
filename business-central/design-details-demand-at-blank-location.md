---
title: 'Designdetails: Bedarf und Vorrat | Microsoft Docs'
description: Dieses Thema erläutert das Konzept der Nachfrage, welches der allgemeine Begriff ist für jede Art Brutto-Bedarf, wie beispielsweise für Verkaufsauftrags und Komponentenbedarf aus einem Fertigungsauftrag.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: cbafba8d012244b10c142912b357188a1f7eece4
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386949"
---
# <a name="design-details-demand-at-blank-location"></a><span data-ttu-id="8c188-103">Designdetails: Bedarf an leerem Lagerort</span><span class="sxs-lookup"><span data-stu-id="8c188-103">Design Details: Demand at Blank Location</span></span>
<span data-ttu-id="8c188-104">Wenn ein Benutzer ein Bedarfsereignis erstellt, wie eine Verkaufsauftragszeile, erlaubt es das Programm dem Benutzer, manchmal einen Lagerortcode anzugeben und andere Male nicht, das heißt, es muss ein leerer Lagerort verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c188-104">When a user creates a demand event, such as a sales order line, the program allows the user to sometimes specify a location code and other times not, that is, use blank location.</span></span>

<span data-ttu-id="8c188-105">In der Bedarfsplanung mit oder ohne Lagerortcodes arbeitet das Planungssystem unter diesen Voraussetzungen in geradliniger Weise:</span><span class="sxs-lookup"><span data-stu-id="8c188-105">For demand with or without location codes, the planning system operates in a straight forward way when:</span></span>

- <span data-ttu-id="8c188-106">Bedarfszeilen enthalten immer Lagerortcodes, und das System verwendet in vollem Umfang Lagermengeneinheiten, einschließlich der betreffenden Lagerorteinrichtung.</span><span class="sxs-lookup"><span data-stu-id="8c188-106">Demand lines always carry location codes and the system fully uses SKUs, including the relevant location setup.</span></span>
- <span data-ttu-id="8c188-107">Bedarfszeilen enthalten nie Lagerortcodes, und das System verwendet keine Lagermengeneinheiten oder irgendeine Lagerorteinrichtung (siehe letztes Szenario im folgenden Abschnitt).</span><span class="sxs-lookup"><span data-stu-id="8c188-107">Demand lines never carry location codes, and the system does not use SKUs or any location setup (see the last scenario in the following section).</span></span>

<span data-ttu-id="8c188-108">Wenn jedoch Bedarfsereignisse manchmal Lagerortcodes aufweisen und manchmal nicht, folgt das Planungssystem je nach Einrichtung bestimmten Regeln.</span><span class="sxs-lookup"><span data-stu-id="8c188-108">However, if demand events sometimes have location codes and other times do not, the planning system will follow certain rules depending on setup.</span></span>

## <a name="demand-at-location"></a><span data-ttu-id="8c188-109">Bedarf am Lagerort</span><span class="sxs-lookup"><span data-stu-id="8c188-109">Demand at Location</span></span>
<span data-ttu-id="8c188-110">Wenn das Planungssystem Bedarf an einem Lagerort erkennt, verhält es sich in unterschiedlicher Weise, abhängig von drei kritischen Einrichtungswerten.</span><span class="sxs-lookup"><span data-stu-id="8c188-110">When the planning system detects demand at a location, it will behave in different ways depending on three critical setup values.</span></span> <span data-ttu-id="8c188-111">Während eines Planungslaufs führt das System der Reihe nach eine Überprüfung auf drei Konfigurationswerte durch und plant entsprechend.</span><span class="sxs-lookup"><span data-stu-id="8c188-111">During a planning run, the system checks for three setup values in sequence and plans accordingly.</span></span>

1. <span data-ttu-id="8c188-112">Ist das Feld **Lagerort notwendig** mit einem Häkchen markiert?</span><span class="sxs-lookup"><span data-stu-id="8c188-112">Is there a check mark in the **Location Mandatory** field?</span></span>

    <span data-ttu-id="8c188-113">Falls ja:</span><span class="sxs-lookup"><span data-stu-id="8c188-113">If yes, then:</span></span>

2. <span data-ttu-id="8c188-114">Sind Lagerhaltungsdaten für den Artikel vorhanden?</span><span class="sxs-lookup"><span data-stu-id="8c188-114">Does SKU exist for the item?</span></span>

    <span data-ttu-id="8c188-115">Falls ja:</span><span class="sxs-lookup"><span data-stu-id="8c188-115">If yes, then:</span></span>

    <span data-ttu-id="8c188-116">Der Artikel wird gemäß den Planungsparametern auf der Lagerhaltungsdatenkarte geplant.</span><span class="sxs-lookup"><span data-stu-id="8c188-116">The item is planned according to planning parameters on the SKU card.</span></span>

    <span data-ttu-id="8c188-117">Falls nein:</span><span class="sxs-lookup"><span data-stu-id="8c188-117">If no, then:</span></span>

3. <span data-ttu-id="8c188-118">Enthält das Feld Komponenten von Lagerort den angeforderen Lagerortcode?</span><span class="sxs-lookup"><span data-stu-id="8c188-118">Does the Components at Location field contain the demanded location code?</span></span>

  <span data-ttu-id="8c188-119">Falls ja:</span><span class="sxs-lookup"><span data-stu-id="8c188-119">If yes, then:</span></span>

  <span data-ttu-id="8c188-120">Der Artikel wird gemäß den Planungsparametern auf der Artikelkarte geplant.</span><span class="sxs-lookup"><span data-stu-id="8c188-120">The item is planned according to planning parameters on the item card.</span></span>

  <span data-ttu-id="8c188-121">Falls nein:</span><span class="sxs-lookup"><span data-stu-id="8c188-121">If no, then:</span></span>

  <span data-ttu-id="8c188-122">Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren = Los-für-Los, Lagerbestand berücksichtigen = Ja, alle anderen Planungsparameter = Leer, Artikel mit dem Wiederbeschaffungsverfahren = Bestellung verwendet weiterhin Auftrag zusammen mit den anderen Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="8c188-122">The item is planned according to: Reordering Policy = Lot-for-Lot, Include Inventory = Yes, all other planning parameters = Empty, items using Reordering Policy = Order will remain using Order along with the other settings.</span></span>

> [!NOTE]
> <span data-ttu-id="8c188-123">Die Ausnahmeplanungseinrichtung, die als letzte Reaktion in Schritt 3 ausgegeben wird, wird nachfolgend als „minimale Alternative“ bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8c188-123">The exceptional planning setup that is output as the last reaction in step 3 above is referred to in the following as the “minimal alternative”.</span></span> <span data-ttu-id="8c188-124">Diese Planungseinrichtung deckt nur den exakten Bedarf ab, und alle anderen Planungsparameter werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8c188-124">This planning setup only covers the exact demand, and all other planning parameters are ignored.</span></span>

<span data-ttu-id="8c188-125">Informationen zu Variationen dieser Planungslogik finden Sie unten im Szenarienabschnitt.</span><span class="sxs-lookup"><span data-stu-id="8c188-125">For information about variations of this planning logic, see the Scenarios section below.</span></span>

## <a name="demand-at-blank-location"></a><span data-ttu-id="8c188-126">Bedarf unter „Leerer Lagerort“</span><span class="sxs-lookup"><span data-stu-id="8c188-126">Demand at Blank Location</span></span>
<span data-ttu-id="8c188-127">Selbst bei ausgewähltem Feld **Lagerort notwendig** erlaubt das System die Erstellung von Bedarfszeilen ohne Lagerortcode, auch als „Leerer Lagerort“ bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8c188-127">Even if the **Location Mandatory** field is selected, the program will allow demand lines to be created without a location code, also referred to as blank location.</span></span> <span data-ttu-id="8c188-128">Dies stellt für das System eine Abweichung dar, weil mehrere Konfigurationswerte für die Behandlung von Lagerorten optimiert sind, und im Ergebnis erstellt das Planungsmodul für eine solche Bedarfszeile keine Planungszeile.</span><span class="sxs-lookup"><span data-stu-id="8c188-128">This is a deviation for the system because it has various setup values tuned to dealing with locations (see above) and as a result, the planning engine will not create a planning line for such a demand line.</span></span>

<span data-ttu-id="8c188-129">Wenn das Feld **Lagerort notwendig** nicht aktiviert ist, jedoch einer der Standortsetupwerte vorhanden ist, gilt dies auch als eine Abweichung, und das Planungssystem reagiert, indem es die „Minimale Alternative“ verwendet: Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren = Los-für-Los (Auftrag bleibt Auftrag), Lagerbestand berücksichtigen = Ja, alle anderen Planungsparameter = Leer.</span><span class="sxs-lookup"><span data-stu-id="8c188-129">If the **Location Mandatory** field is not selected but any of the location setup values exist, it is also considered a deviation, and the planning system will react by using the “minimal alternative”: The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

## <a name="scenarios"></a><span data-ttu-id="8c188-130">Szenarien</span><span class="sxs-lookup"><span data-stu-id="8c188-130">Scenarios</span></span>
<span data-ttu-id="8c188-131">Die folgenden Szenarien beschreiben Variationen des Bedarfs am leeren Lagerort und wie das Planungssystem zur „minimale Alternative“ aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="8c188-131">The following scenarios describe variations of demand at blank location and how the planning system resolves to the “minimal alternative.”</span></span>

### <a name="setup-1"></a><span data-ttu-id="8c188-132">Konfiguration 1:</span><span class="sxs-lookup"><span data-stu-id="8c188-132">Setup 1:</span></span>
<span data-ttu-id="8c188-133">Lagerort notwendig = Ja</span><span class="sxs-lookup"><span data-stu-id="8c188-133">Location Mandatory = Yes</span></span>

<span data-ttu-id="8c188-134">Lagerhaltungsdaten sind für ROT eingerichtet</span><span class="sxs-lookup"><span data-stu-id="8c188-134">SKU is set up for RED</span></span>

<span data-ttu-id="8c188-135">Komponenten in Lagerort = BLAU</span><span class="sxs-lookup"><span data-stu-id="8c188-135">Components at Location = BLUE</span></span>

#### <a name="case-11-demand-is-at-red-location"></a><span data-ttu-id="8c188-136">Fall 1.1: Es besteht Bedarf am Lagerort ROT</span><span class="sxs-lookup"><span data-stu-id="8c188-136">Case 1.1: Demand is at RED location</span></span>
<span data-ttu-id="8c188-137">Der Artikel wird gemäß den Planungsparametern auf der Lagerhaltungsdatenkarte geplant.</span><span class="sxs-lookup"><span data-stu-id="8c188-137">The item is planned according to planning parameters on the SKU card.</span></span>

#### <a name="case-12-demand-is-at-blue-location"></a><span data-ttu-id="8c188-138">Fall 1.2: Es besteht Bedarf am Lagerort BLAU</span><span class="sxs-lookup"><span data-stu-id="8c188-138">Case 1.2: Demand is at BLUE location</span></span>
<span data-ttu-id="8c188-139">Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren = Los-für-Los (Auftrag bleibt Auftrag), Lagerbestand berücksichtigen = Ja, alle anderen Planungsparameter = Leer.</span><span class="sxs-lookup"><span data-stu-id="8c188-139">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-13-demand-is-at-green-location"></a><span data-ttu-id="8c188-140">Fall 1.3: Es besteht Bedarf am Lagerort GRÜN</span><span class="sxs-lookup"><span data-stu-id="8c188-140">Case 1.3: Demand is at GREEN location</span></span>
<span data-ttu-id="8c188-141">Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren = Los-für-Los (Auftrag bleibt Auftrag), Lagerbestand berücksichtigen = Ja, alle anderen Planungsparameter = Leer.</span><span class="sxs-lookup"><span data-stu-id="8c188-141">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-14-demand-is-at-blank-location"></a><span data-ttu-id="8c188-142">Fall 1.4: Es besteht Bedarf am Lagerort LEER</span><span class="sxs-lookup"><span data-stu-id="8c188-142">Case 1.4: Demand is at BLANK location</span></span>
<span data-ttu-id="8c188-143">Der Artikel wird nicht geplant, weil kein Lagerort in der Bedarfszeile definiert ist.</span><span class="sxs-lookup"><span data-stu-id="8c188-143">The item is not planned because no location is defined on the demand line.</span></span>

### <a name="setup-2"></a><span data-ttu-id="8c188-144">Konfiguration 2:</span><span class="sxs-lookup"><span data-stu-id="8c188-144">Setup 2:</span></span>
<span data-ttu-id="8c188-145">Lagerort notwendig = Ja</span><span class="sxs-lookup"><span data-stu-id="8c188-145">Location Mandatory = Yes</span></span>

<span data-ttu-id="8c188-146">Es sind keine Lagerhaltungsdaten vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8c188-146">No SKU exists</span></span>

<span data-ttu-id="8c188-147">Komponenten in Lagerort = BLAU</span><span class="sxs-lookup"><span data-stu-id="8c188-147">Components at Location = BLUE</span></span>

#### <a name="case-21-demand-is-at-red-location"></a><span data-ttu-id="8c188-148">Fall 2.1: Es besteht Bedarf am Lagerort ROT</span><span class="sxs-lookup"><span data-stu-id="8c188-148">Case 2.1: Demand is at RED location</span></span>
<span data-ttu-id="8c188-149">Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren = Los-für-Los (Auftrag bleibt Auftrag), Lagerbestand berücksichtigen = Ja, alle anderen Planungsparameter = Leer.</span><span class="sxs-lookup"><span data-stu-id="8c188-149">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-22-demand-is-at-blue-location"></a><span data-ttu-id="8c188-150">Fall 2.2: Es besteht Bedarf am Lagerort BLAU</span><span class="sxs-lookup"><span data-stu-id="8c188-150">Case 2.2: Demand is at BLUE location</span></span>
<span data-ttu-id="8c188-151">Der Artikel wird gemäß den Planungsparametern auf der Artikelkarte geplant.</span><span class="sxs-lookup"><span data-stu-id="8c188-151">The item is planned according to planning parameters on the item card.</span></span>

### <a name="setup-3"></a><span data-ttu-id="8c188-152">Konfiguration 3:</span><span class="sxs-lookup"><span data-stu-id="8c188-152">Setup 3:</span></span>
<span data-ttu-id="8c188-153">Lagerort notwendig = Nein</span><span class="sxs-lookup"><span data-stu-id="8c188-153">Location Mandatory = No</span></span>

<span data-ttu-id="8c188-154">Es sind keine Lagerhaltungsdaten vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8c188-154">No SKU exists</span></span>

<span data-ttu-id="8c188-155">Komponenten in Lagerort = BLAU</span><span class="sxs-lookup"><span data-stu-id="8c188-155">Components at Location = BLUE</span></span>

#### <a name="case-31-demand-is-at-red-location"></a><span data-ttu-id="8c188-156">Fall 3.1: Es besteht Bedarf am Lagerort ROT</span><span class="sxs-lookup"><span data-stu-id="8c188-156">Case 3.1: Demand is at RED location</span></span>
<span data-ttu-id="8c188-157">Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren = Los-für-Los (Auftrag bleibt Auftrag), Lagerbestand berücksichtigen = Ja, alle anderen Planungsparameter = Leer.</span><span class="sxs-lookup"><span data-stu-id="8c188-157">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-32-demand-is-at-blue-location"></a><span data-ttu-id="8c188-158">Fall 3.2: Es besteht Bedarf am Lagerort BLAU</span><span class="sxs-lookup"><span data-stu-id="8c188-158">Case 3.2: Demand is at BLUE location</span></span>
<span data-ttu-id="8c188-159">Der Artikel wird gemäß den Planungsparametern auf der Artikelkarte geplant.</span><span class="sxs-lookup"><span data-stu-id="8c188-159">The item is planned according to planning parameters on the item card.</span></span>

#### <a name="case-33-demand-is-at-blank-location"></a><span data-ttu-id="8c188-160">Fall 3.3: Es besteht Bedarf am Lagerort LEER</span><span class="sxs-lookup"><span data-stu-id="8c188-160">Case 3.3: Demand is at BLANK location</span></span>
<span data-ttu-id="8c188-161">Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren = Los-für-Los (Auftrag bleibt Auftrag), Lagerbestand berücksichtigen = Ja, alle anderen Planungsparameter = Leer.</span><span class="sxs-lookup"><span data-stu-id="8c188-161">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

### <a name="setup-4"></a><span data-ttu-id="8c188-162">Konfiguration 4:</span><span class="sxs-lookup"><span data-stu-id="8c188-162">Setup 4:</span></span>
<span data-ttu-id="8c188-163">Lagerort notwendig = Nein</span><span class="sxs-lookup"><span data-stu-id="8c188-163">Location Mandatory = No</span></span>

<span data-ttu-id="8c188-164">Es sind keine Lagerhaltungsdaten vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8c188-164">No SKU exists</span></span>

<span data-ttu-id="8c188-165">Komponente an Lagerort = LEER</span><span class="sxs-lookup"><span data-stu-id="8c188-165">Components at Location = BLANK</span></span>

#### <a name="case-41-demand-is-at-blue-location"></a><span data-ttu-id="8c188-166">Fall 4.1: Es besteht Bedarf am Lagerort BLAU</span><span class="sxs-lookup"><span data-stu-id="8c188-166">Case 4.1: Demand is at BLUE location</span></span>
<span data-ttu-id="8c188-167">Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren = Los-für-Los (Auftrag bleibt Auftrag), Lagerbestand berücksichtigen = Ja, alle anderen Planungsparameter = Leer.</span><span class="sxs-lookup"><span data-stu-id="8c188-167">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-42-demand-is-at-blank-location"></a><span data-ttu-id="8c188-168">Fall 4.2: Es besteht Bedarf am Lagerort LEER</span><span class="sxs-lookup"><span data-stu-id="8c188-168">Case 4.2: Demand is at BLANK location</span></span>
<span data-ttu-id="8c188-169">Der Artikel wird gemäß den Planungsparametern auf der Artikelkarte geplant.</span><span class="sxs-lookup"><span data-stu-id="8c188-169">The item is planned according to planning parameters on the item card.</span></span>

<span data-ttu-id="8c188-170">Wie aus dem letzten Szenario ersehen werden kann, besteht die einzige Möglichkeit, ein richtiges Ergebnis für eine Bedarfszeile ohne Lagerortcode zu erhalten, im Deaktivieren aller Einrichtungswerte, die sich auf Lagerorte beziehen.</span><span class="sxs-lookup"><span data-stu-id="8c188-170">As illustrated in the last scenario, the only way to get a correct result for a demand line without a location code is to disable all setup values relating to locations.</span></span> <span data-ttu-id="8c188-171">Analog besteht die einzige Möglichkeit, stabile Planungsergebnisse für den Bedarf an den Lagerorten zu erhalten, in der Verwendung von Lagerhaltungsdaten.</span><span class="sxs-lookup"><span data-stu-id="8c188-171">Similarly, the only way to get stable planning results for demand at locations is to use SKUs.</span></span> <span data-ttu-id="8c188-172">Wenn Unternehmen häufig den Bedarf an Lagerorten planen müssen, empfiehlt sich daher dringend die Verwendung des Moduls Lagerhaltungsdaten.</span><span class="sxs-lookup"><span data-stu-id="8c188-172">Therefore, if companies often plan for demand at locations, they are strongly advised to use the Stockkeeping Units granule.</span></span>

## <a name="see-also"></a><span data-ttu-id="8c188-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c188-173">See Also</span></span>  
<span data-ttu-id="8c188-174">[Designdetails: Ausgleich von Bedarf und Vorrat](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="8c188-174">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="8c188-175">[Designdetails: Zentrale Konzepte des Planungssystems](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="8c188-175">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="8c188-176">Designdetails: Vorratsplanung</span><span class="sxs-lookup"><span data-stu-id="8c188-176">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]