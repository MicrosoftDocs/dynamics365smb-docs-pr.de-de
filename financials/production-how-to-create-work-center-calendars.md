---
title: 'Vorgehensweise: Einrichten von Betriebskalendern | Microsoft Docs'
description: "In einem Arbeitsplatzgruppenkalender werden die Arbeitstage und -stunden, Schichten, Feiertage und Fehlzeiten angegeben, die die verfügbare Bruttokapazität der Arbeitsplatzgruppe zeitlich gemessen entsprechend ihren definierten Effektivitäts- und Kapazitätswerten bestimmen. Um einen Arbeitsplatzgruppenkalender zu erstellen und zu aktivieren, sind verschiedene vorbereitende Aufgaben auszuführen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: cf54f63e94ab3249f30d2fcdbef2c35e323e4cd8
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-shop-calendars"></a><span data-ttu-id="e08d5-104">Betriebskalender einrichten</span><span class="sxs-lookup"><span data-stu-id="e08d5-104">Set Up Shop Calendars</span></span>
<span data-ttu-id="e08d5-105">In einem Arbeitsplatzgruppenkalender werden die Arbeitstage/-stunden, Schichten, Feiertage und Fehlzeiten angegeben, die die verfügbare Bruttokapazität der Arbeitsplatzgruppe (zeitlich gemessen) entsprechend ihren definierten Effektivitäts- und Kapazitätswerten bestimmen.</span><span class="sxs-lookup"><span data-stu-id="e08d5-105">A work center or machine calendar specifies the working days and hours, shifts, holidays, and absences that determine the center’s gross available capacity, measured in time, according to its defined efficiency and capacity values.</span></span>

<span data-ttu-id="e08d5-106">Ein grundlegender Schritt beim Berechnen eines spezifischen Arbeitsplatzgruppenkalenders ist das Einrichten eines oder mehrerer allgemeiner Betriebskalender.</span><span class="sxs-lookup"><span data-stu-id="e08d5-106">As a foundation for calculating a specific work or machine center calendar, you must first set up one or more general shop calendars.</span></span> <span data-ttu-id="e08d5-107">In einem Betriebskalender wird eine Standardarbeitswoche gemäß den Anfangs- und Endzeit der einzelnen Arbeitstage und dem Plan der einzelnen Schichten definiert.</span><span class="sxs-lookup"><span data-stu-id="e08d5-107">A shop calendar defines a standard work week according to start and end times of each working day and the work shift relation.</span></span> <span data-ttu-id="e08d5-108">Darüber hinaus werden im Betriebskalender die festen Feiertage im gesamten Jahr definiert.</span><span class="sxs-lookup"><span data-stu-id="e08d5-108">In addition, the shop calendar defines the fixed holidays during a year.</span></span>  

<span data-ttu-id="e08d5-109">Nachfolgend ist beschrieben, wie ein alternativer Arbeitsplatzkalender eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="e08d5-109">The following describes how to set up work center calendars.</span></span> <span data-ttu-id="e08d5-110">Die Schritte sind ähnlich, wenn Sie Arbeitsplatzkalender einrichten.</span><span class="sxs-lookup"><span data-stu-id="e08d5-110">The steps are similar when setting up machine center calendars.</span></span>  

## <a name="to-create-work-shifts"></a><span data-ttu-id="e08d5-111">Arbeitsschichten erstellen</span><span class="sxs-lookup"><span data-stu-id="e08d5-111">To create work shifts</span></span>  
1.  <span data-ttu-id="e08d5-112">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Schichten** ein und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="e08d5-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Work Shifts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e08d5-113">Geben Sie in einer leeren Zeile eine Zahl im Feld **Code** ein, um die Schicht zu bestimmen, z. B. **1**.</span><span class="sxs-lookup"><span data-stu-id="e08d5-113">On a blank line, enter a number in the **Code** field to identify the work shift, for example, **1**.</span></span>  
3.  <span data-ttu-id="e08d5-114">Geben Sie im Feld **Beschreibung** eine Beschreibung der Schicht ein, z. B. **1. Schicht**.</span><span class="sxs-lookup"><span data-stu-id="e08d5-114">Describe the work shift in the **Description** field, for example, **1st shift**.</span></span>  
4.  <span data-ttu-id="e08d5-115">Optional füllen Sie Zeilen für eine zweite oder dritte Schicht aus.</span><span class="sxs-lookup"><span data-stu-id="e08d5-115">Optionally, fill in lines for a second or third work shift.</span></span>  

<span data-ttu-id="e08d5-116">Selbst wenn Ihre Arbeitsplatzgruppen nicht in verschiedenen Schichten arbeiten, geben Sie mindestens einen Schichtcode ein.</span><span class="sxs-lookup"><span data-stu-id="e08d5-116">Even if your work centers do not work in different work shifts, enter at least one work shift code.</span></span>  

## <a name="to-set-up-a-shop-calendar"></a><span data-ttu-id="e08d5-117">Einen Betriebskalender einrichten</span><span class="sxs-lookup"><span data-stu-id="e08d5-117">To set up a shop calendar</span></span>  
1.  <span data-ttu-id="e08d5-118">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Schichten** ein und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="e08d5-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Shop Calendars**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e08d5-119">Geben Sie in einer leeren Zeile eine Zahl im Feld **Code** ein, um den Betriebskalender zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="e08d5-119">On a blank line, enter a number in the **Code** field to identify the shop calendar.</span></span>  
3.  <span data-ttu-id="e08d5-120">Geben Sie im Feld **Beschreibung** eine Beschreibung für den Betriebskalender ein.</span><span class="sxs-lookup"><span data-stu-id="e08d5-120">Describe the shop calendar in the **Description** field.</span></span>  
4.  <span data-ttu-id="e08d5-121">Wählen Sie die **Arbeitstage** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="e08d5-121">Choose the **Working Days** action.</span></span>
5.  <span data-ttu-id="e08d5-122">Im Fenster **Betriebskalenderarbeitstage** bestimmen Sie eine ganze Arbeitswoche mit den Start- und Endzeiten für jeden Tag.</span><span class="sxs-lookup"><span data-stu-id="e08d5-122">In the **Shop Calendar Working Days** window, define a complete work week, with the start and end times for each day.</span></span>  

    <span data-ttu-id="e08d5-123">Wählen Sie im Feld **Schichtcode** eine der Schichten aus, die Sie zuvor definierten.</span><span class="sxs-lookup"><span data-stu-id="e08d5-123">In the **Work Shift Code** field, select one of the shifts that you previously defined.</span></span> <span data-ttu-id="e08d5-124">Fügen Sie eine Zeile für jeden Arbeitstag und jede Schicht hinzu.</span><span class="sxs-lookup"><span data-stu-id="e08d5-124">Add a line for every working day and every shift.</span></span> <span data-ttu-id="e08d5-125">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e08d5-125">For example:</span></span>  

    <span data-ttu-id="e08d5-126">Montag  07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="e08d5-126">Monday  07:00 15:00 1</span></span>   
    <span data-ttu-id="e08d5-127">Dienstag 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="e08d5-127">Tuesday 07:00 15:00 1</span></span>  

    <span data-ttu-id="e08d5-128">Wenn Sie einen Betriebskalender mit zwei Schichten benötigen, nehmen Sie eine Eingabe wie im folgt vor:</span><span class="sxs-lookup"><span data-stu-id="e08d5-128">If you need a shop calendar with two work shifts, you must fill it in in this manner:</span></span>  

    <span data-ttu-id="e08d5-129">Montag 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="e08d5-129">Monday 07:00 15:00 1</span></span>   
    <span data-ttu-id="e08d5-130">Montag 15:00 23:00 2</span><span class="sxs-lookup"><span data-stu-id="e08d5-130">Monday 15:00 23:00 2</span></span>  
    <span data-ttu-id="e08d5-131">Dienstag 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="e08d5-131">Tuesday 07:00 15:00 1</span></span>  
    <span data-ttu-id="e08d5-132">Dienstag 15:00 23:00 2</span><span class="sxs-lookup"><span data-stu-id="e08d5-132">Tuesday 15:00 23:00 2</span></span>  

    <span data-ttu-id="e08d5-133">Alle Wochentage, die nicht im Betriebskalender definiert sind, z. B. Samstag und Sonntag, werden einfach als Nicht-Werktage betrachtet, und sie weisen im Arbeitsplatzgruppenkalender keine verfügbare Kapazität auf.</span><span class="sxs-lookup"><span data-stu-id="e08d5-133">Any week days that you do not define in the shop calendar, such as Saturday and Sunday, are considered non-working days and will have zero available capacity in a work center calendar.</span></span>  

    <span data-ttu-id="e08d5-134">Wenn alle Arbeitstage einer Woche definiert sind, können Sie das Fenster **Betriebskalenderarbeitstage** schließen und mit der Eingabe von Feiertagen fortfahren.</span><span class="sxs-lookup"><span data-stu-id="e08d5-134">When all the working days of a week are defined, you can close the **Shop Calendar Working Days** window and proceed to enter holidays.</span></span>  

6.  <span data-ttu-id="e08d5-135">Im Fenster **Betriebskalender** wählen Sie den Betriebskalender, und wählen die **Feiertage** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="e08d5-135">In the **Shop Calendars** window, select the shop calendar, and then choose the **Holidays** action.</span></span>
7. <span data-ttu-id="e08d5-136">Im Fenster **Betriebskalender-Feiertage**definieren Sie nun die Feiertage des Jahres, indem Sie Anfangsdatum und -uhrzeit sowie Enddatum und -uhrzeit sowie eine Beschreibung des jeweiligen Feiertags in einzelnen Zeilen eingeben. Beispiel.</span><span class="sxs-lookup"><span data-stu-id="e08d5-136">In the **Shop Calendar Holidays** window, define the holidays of the year by entering the start date and time, the end time, and description of each holiday on individual lines.</span></span> <span data-ttu-id="e08d5-137">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e08d5-137">For example:</span></span>  

    <span data-ttu-id="e08d5-138">04.07.14 0:00:00 23:59:00 Sommerurlaub</span><span class="sxs-lookup"><span data-stu-id="e08d5-138">04/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  
    <span data-ttu-id="e08d5-139">05.07.14 0:00:00 23:59:00 Sommerurlaub</span><span class="sxs-lookup"><span data-stu-id="e08d5-139">05/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  
    <span data-ttu-id="e08d5-140">06.07.14 0:00:00 23:59:00 Sommerurlaub</span><span class="sxs-lookup"><span data-stu-id="e08d5-140">06/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  

<span data-ttu-id="e08d5-141">Die definierten Feiertage weisen im Arbeitsgruppenkalender eine verfügbare Kapazität von Null auf.</span><span class="sxs-lookup"><span data-stu-id="e08d5-141">The defined holidays will have zero available capacity in a work center calendar.</span></span>  

<span data-ttu-id="e08d5-142">Der Betriebskalender kann nun einer Arbeitsplatzgruppe zugewiesen werden, um einen Arbeitsplatzgruppenkalender zu berechnen, anhand dessen die gesamte Arbeitsgangplanung für die Zeit dieser Arbeitsplatzgruppe erfolgt.</span><span class="sxs-lookup"><span data-stu-id="e08d5-142">The shop calendar can now be assigned to a work center to calculate the work shop calendar that will govern all operation scheduling at that work center.</span></span>  

## <a name="to-calculate-a-work-center-calendar"></a><span data-ttu-id="e08d5-143">Einen Arbeitsplatzgruppenkalender berechnen</span><span class="sxs-lookup"><span data-stu-id="e08d5-143">To calculate a work center calendar</span></span>  

1.  <span data-ttu-id="e08d5-144">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Schichten** ein und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="e08d5-144">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Work Centers**, and then choose the related link.</span></span>
2. <span data-ttu-id="e08d5-145">öffnen Sie den Arbeitsplatz, den Sie aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="e08d5-145">Open the work center that you want to update.</span></span>  
3. <span data-ttu-id="e08d5-146">Wählen Sie im Inforegister Planung im Feld **Betriebskalendercode** den Kalender aus, der in dieser Arbeitsplatzgruppe als Grundlage für einen Arbeitsplatzgruppenkalender verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e08d5-146">In the **Shop Calendar Code** field, select which shop calendar to use as the foundation for a work center calendar.</span></span>  
4. <span data-ttu-id="e08d5-147">Wählen Sie die Aktion **Kalender** aus.</span><span class="sxs-lookup"><span data-stu-id="e08d5-147">Choose the **Calendar** action.</span></span>  
5. <span data-ttu-id="e08d5-148">Klicken Sie im Fenster **Arbeitsplatzgruppenkalender** auf **Aktionen, Matrix anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="e08d5-148">In the **Work Center Calendar** window, choose the **Show Matrix** action.</span></span>  

    <span data-ttu-id="e08d5-149">Links im Matrixfenster werden die eingerichteten Arbeitsplatzgruppen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e08d5-149">The left side of the matrix window lists the work centers that are set up.</span></span> <span data-ttu-id="e08d5-150">Rechts befindet sich ein Kalender, in dem die verfügbaren Kapazitäten pro Arbeitstag in der definierten Maßeinheit angegeben werden, z. B. **480** Minuten.</span><span class="sxs-lookup"><span data-stu-id="e08d5-150">The right side shows a calendar displaying the available capacity values for each working day in the defined unit of measure, for example, **480** minutes.</span></span> <span data-ttu-id="e08d5-151">Jede Zeile stellt den Kalender einer Arbeitsplatzgruppe dar.</span><span class="sxs-lookup"><span data-stu-id="e08d5-151">Each line represents the calendar of one work center.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="e08d5-152">Sie können die Kapazitätswerte auch pro Woche oder Monat anzeigen, indem Sie die Auswahl im Feld **Anzeigen nach** auf dem Inforegister Matrixoptionen im Fenster **Arbeitsplatzgruppenkalender** ändern.</span><span class="sxs-lookup"><span data-stu-id="e08d5-152">You can also select to view the capacity values for each week or month by changing the selection in the **View By** field in the **Work Center Calendar** window.</span></span>  

    <span data-ttu-id="e08d5-153">Um den neuen Betriebskalender als eine Zeile in der ausgewählten Arbeitsgruppe widerzuspiegeln, muss er zunächst berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="e08d5-153">To reflect the new shop calendar as a line on the selected work center, it must first be calculated.</span></span>  

6.  <span data-ttu-id="e08d5-154">Wählen Sie die Aktion **berechnen** aus.</span><span class="sxs-lookup"><span data-stu-id="e08d5-154">Choose the **Calculate** action.</span></span>  
7.  <span data-ttu-id="e08d5-155">Auf dem Inforegister **Arbeitsplatzgruppe** können Sie einen Filter festlegen, sodass nur die Berechnung für eine Arbeitsplatzgruppe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e08d5-155">On the **Work Center** FastTab, you can set a filter to only calculate for one work center.</span></span> <span data-ttu-id="e08d5-156">Wenn kein Filter festgelegt wird, werden alle vorhandenen Arbeitsplatzgruppenkalender berechnet.</span><span class="sxs-lookup"><span data-stu-id="e08d5-156">If you do not set a filter, all existing work center calendars will be calculated.</span></span>  
8.  <span data-ttu-id="e08d5-157">Legen Sie das Anfangs- und das Enddatum des zu berechnenden Kalenderzeitraums fest, z. B. ein Jahr vom 01.01.14 bis zum 31.12.14.</span><span class="sxs-lookup"><span data-stu-id="e08d5-157">Define the starting and ending dates of the calendar period that should be calculated, for example, one year from 01/01/14 to 31/12/14.</span></span>
9. <span data-ttu-id="e08d5-158">Klicken Sie auf die Schaltfläche **OK**, um die Kapazität zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="e08d5-158">Choose the **OK** button to calculate capacity.</span></span>  

<span data-ttu-id="e08d5-159">Kalenderposten werden nun erstellt bzw. aktualisiert und zeigen die verfügbare Kapazität pro Tag oder sonstiger Periode an, entsprechend den folgenden drei Sätzen von Stammdaten:</span><span class="sxs-lookup"><span data-stu-id="e08d5-159">Calendar entries are now created or updated displaying the available capacity for each period according to the following three sets of master data:</span></span>  

- <span data-ttu-id="e08d5-160">Die im zugewiesenen Betriebskalender definierten Arbeitstage und Schichten.</span><span class="sxs-lookup"><span data-stu-id="e08d5-160">The working days and shift defined in the assigned shop calendar.</span></span>  
- <span data-ttu-id="e08d5-161">Der Wert im Feld **Kapazität** auf der Arbeitsplatzgruppenkarte.</span><span class="sxs-lookup"><span data-stu-id="e08d5-161">The value in the **Capacity** field on the work center card.</span></span>  
- <span data-ttu-id="e08d5-162">Der Wert im Feld **Effektivität** auf der Arbeitsplatzgruppenkarte</span><span class="sxs-lookup"><span data-stu-id="e08d5-162">The value in the **Efficiency** field on the work center card.</span></span>  

<span data-ttu-id="e08d5-163">Der berechneten Arbeitsplatzgruppenkalender legt jetzt fest, wann und wie viel Kapazität in dieser Arbeitsplatzgruppe verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e08d5-163">The calculated work center calendar will now define when and how much capacity is available at this work center.</span></span> <span data-ttu-id="e08d5-164">Dieses steuert die detaillierte Planung von Arbeitsgängen, die in der Arbeitsplatzgruppe ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e08d5-164">This controls the detailed scheduling of operations performed at the work center.</span></span>  

## <a name="to-record-work-center-absence"></a><span data-ttu-id="e08d5-165">Fehlzeiten für Arbeitsplatzgruppen erfassen</span><span class="sxs-lookup"><span data-stu-id="e08d5-165">To record work center absence</span></span>  
1.  <span data-ttu-id="e08d5-166">Klicken Sie im Fenster **Arbeitsplatzgruppenkalender** auf **Aktionen, Matrix anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="e08d5-166">In the **Work Center Calendar** window, choose the **Show Matrix** action.</span></span>
2. <span data-ttu-id="e08d5-167">Wählen Sie im Fenster **Arbeitsplatzgruppenkalendermatrix** die Arbeitsplatzgruppe und den Kalendertag aus, an dem die Fehlzeit aufgezeichnet werden soll, und klicken Sie anschließend auf **Verknüpfte Informationen, Planung, Fehlzeiten**.</span><span class="sxs-lookup"><span data-stu-id="e08d5-167">In the **Work Center Calendar Matrix** window, select the work center and calendar day when the absence time should be recorded, and then choose the **Absence** action.</span></span>  
3.  <span data-ttu-id="e08d5-168">Legen Sie im Fenster **Fehlzeiten** die Anfangs- und die Endzeit für die Fehlzeiten an diesem Tag fest, und geben Sie eine Begründung an.</span><span class="sxs-lookup"><span data-stu-id="e08d5-168">In the **Absence** window, define the starting time, ending time, and description of that day’s absence.</span></span> <span data-ttu-id="e08d5-169">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e08d5-169">For example:</span></span>  

    <span data-ttu-id="e08d5-170">25.01.01 08:00 10:00 Wartung</span><span class="sxs-lookup"><span data-stu-id="e08d5-170">25/01/01 08:00 10:00 Maintenance</span></span>  

4.  <span data-ttu-id="e08d5-171">Wählen Sie die **Aktualisieren** Aktion aus, und schließen Sie dann das Fenster **Fehlzeiten**.</span><span class="sxs-lookup"><span data-stu-id="e08d5-171">Choose the **Update** action, and then close the **Absence** window.</span></span>  

<span data-ttu-id="e08d5-172">Die Kapazität des ausgewählten Tages hat sich nun um die aufgezeichnete Fehlzeit verringert.</span><span class="sxs-lookup"><span data-stu-id="e08d5-172">The capacity of the selected day has now decreased by the recorded absence time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e08d5-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e08d5-173">See Also</span></span>  
[<span data-ttu-id="e08d5-174">Basiskalender einrichten</span><span class="sxs-lookup"><span data-stu-id="e08d5-174">Set Up Base Calendars</span></span>](across-how-to-assign-base-calendars.md)  
[<span data-ttu-id="e08d5-175">Arbeitsplätze und Arbeitsplatzgruppen einrichten</span><span class="sxs-lookup"><span data-stu-id="e08d5-175">Set Up Work Centers and Machine Centers</span></span>](production-how-to-set-up-work-and-machine-centers.md)  
[<span data-ttu-id="e08d5-176">Produktion einrichten</span><span class="sxs-lookup"><span data-stu-id="e08d5-176">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
[<span data-ttu-id="e08d5-177">Produktion</span><span class="sxs-lookup"><span data-stu-id="e08d5-177">Manufacturing</span></span>](production-manage-manufacturing.md)  
<span data-ttu-id="e08d5-178">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e08d5-178">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

