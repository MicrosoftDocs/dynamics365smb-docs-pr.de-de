---
title: Eingeben von Datumsangaben und Uhrzeiten in Business Central  | Microsoft Docs
description: "Erfahren Sie, wie Sie Datumsangaben und Uhrzeiten einschließlich verschiedener Produktivitätstipps wie Stenografie, Ausdrücke und Bereiche eingegeben. Filtern Sie Listen oder Berichte bis zu einem bestimmten Datum oder zu Zeiträumen."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter, calendar, shorthand, range
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 8717d60a8449ca300eaf9c1a5c4b137ea1a1a247
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---

# <a name="working-with-calendar-dates-and-times"></a><span data-ttu-id="0580d-104">Arbeiten mit Datumsangaben und Uhrzeiten in Kalendern</span><span class="sxs-lookup"><span data-stu-id="0580d-104">Working with Calendar Dates and Times</span></span>
[!INCLUDE[d365fin](includes/d365fin_long_md.md)] <span data-ttu-id="0580d-105">bietet mehrere Möglichkeiten, Datumsangaben und Uhrzeiten einzugeben, einschließlich leistungsstarker Funktionen, die die Dateneingabe beschleunigen oder Ihnen helfen, komplexe Kalenderausdrücke zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="0580d-105">offers multiple ways to enter dates and times, including powerful features that accelerate data entry, or help you write complex calendar expressions.</span></span> <span data-ttu-id="0580d-106">Es gibt verschiedene Bereiche in der Anwendung, in denen Sie Daten und Uhrzeiten in die Felder eingeben können.</span><span class="sxs-lookup"><span data-stu-id="0580d-106">There are various places throughout the application where you can enter dates and times in fields.</span></span> <span data-ttu-id="0580d-107">So können Sie beispielsweise das Warenausgangsdatum für einen Auftrag festlegen.</span><span class="sxs-lookup"><span data-stu-id="0580d-107">For example, on a sales order, you can set the shipment date.</span></span> <span data-ttu-id="0580d-108">Wenn Sie Listen oder Berichtsdaten filtern, können Sie Datumswerten und Uhrzeiten eingeben, um genau die Daten zu finden, an denen Sie interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="0580d-108">When filtering lists or report data, you can enter dates and times to pinpoint only the data that you are interested in.</span></span>

## <a name="check-your-region-and-language-settings"></a><span data-ttu-id="0580d-109">Überprüfen Ihrer Bereichs- und Spracheneinstellungen</span><span class="sxs-lookup"><span data-stu-id="0580d-109">Check your region and language settings</span></span>
<span data-ttu-id="0580d-110">Die Seite [**Meine Einstellungen**](https://businesscentral.dynamics.com?page=9176 "Direkt zur Benutzereinstellungsseite in Business Central zurückkehren") gibt die **Region** und die **Sprache** an, die Sie in der Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="0580d-110">The [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central") page specifies the **Region** and **Language** that you are using in the application.</span></span> <span data-ttu-id="0580d-111">Diese Einstellungen beeinflussen, wie Sie Datumswerte und Uhrzeiten eingeben.</span><span class="sxs-lookup"><span data-stu-id="0580d-111">These settings influence how you enter dates and times.</span></span> 

-   <span data-ttu-id="0580d-112">Die Einstellung **Region** bestimmt, wie Daten, Uhrzeiten, Ziffern und Währungen angezeigt oder formatiert werden.</span><span class="sxs-lookup"><span data-stu-id="0580d-112">The **Region** setting determines how dates, times, numbers, and currencies are shown or formatted.</span></span>

-   <span data-ttu-id="0580d-113">Bei Datumsmustern, die Begriffe enthalten, muss die Sprache der Begriffe, die Sie verwenden, der **Sprache**-Einstellung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0580d-113">For date patterns that involve words, the language of the words that you use must correspond to the **Language** setting.</span></span>

> [!NOTE]
> [!INCLUDE[d365fin](includes/d365fin_long_md.md)] <span data-ttu-id="0580d-114">verwendet das gregorianische Kalendersystem.</span><span class="sxs-lookup"><span data-stu-id="0580d-114">uses the Gregorian calendar system.</span></span>

<!-- 
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->
## <a name="entering-dates"></a><span data-ttu-id="0580d-115">Eingeben von Datumswerten</span><span class="sxs-lookup"><span data-stu-id="0580d-115">Entering Dates</span></span>
<span data-ttu-id="0580d-116">In einem Datumsfeld können Sie unter Verwendung des Standardformats ein Datum für Ihre Bereichseinstellung eingeben.</span><span class="sxs-lookup"><span data-stu-id="0580d-116">In a date field, you can enter a date using the standard format for your region setting.</span></span> <span data-ttu-id="0580d-117">Verschiedene Regionen können verschiedene Trennzeichen zwischen Tagen, Monaten und Jahren verwenden.</span><span class="sxs-lookup"><span data-stu-id="0580d-117">Different regions can use different separators between the days, months and years.</span></span> <span data-ttu-id="0580d-118">Beispielsweise werden in einigen Regionen Bindestriche verwendet (mm-tt-jjjj) und in anderen werden Schrägstriche verwenden (mm/tt/jjjj).</span><span class="sxs-lookup"><span data-stu-id="0580d-118">For example, some regions use dashes (mm-dd-yyyy) and others use forward slashes (mm/dd/yyyy).</span></span> <span data-ttu-id="0580d-119">Sie können allerdings sämtliche Trennzeichen verwenden, sogar einen Leerzeichen, und das Datum wird automatisch zu den Trennzeichen geändert, die Ihrer Region entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0580d-119">However, you can use any separators, even a space, and the date will automatically be changed to use separators that match your region.</span></span>

<span data-ttu-id="0580d-120">Beachten Sie, dass, das Format, in dem Datumswerte in gedruckten Berichten oder per E-Mail gesendeten Dokumenten von Ihrer persönlichen Regionseinstellung nicht beeinflusst wird.</span><span class="sxs-lookup"><span data-stu-id="0580d-120">Note that the format in which dates are displayed on printed reports or emailed documents is not influenced by your personal choice of region setting.</span></span>

<span data-ttu-id="0580d-121">Um produktiver mit Datumswerten und Uhrzeiten zu arbeiten, können Sie alle Methoden oder Formate verwenden, die in den folgenden Abschnitten beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="0580d-121">To work more productively with dates and times, you can use any of the methods or formats that are described in the following sections.</span></span> 

### <a name="picking-dates-from-the-calendar"></a><span data-ttu-id="0580d-122">Datumsangaben aus dem Kalender auswählen</span><span class="sxs-lookup"><span data-stu-id="0580d-122">Picking dates from the calendar</span></span>
<span data-ttu-id="0580d-123">Alle Felder, die ein Kalendersymbol anzeigen, können mithilfe der Kalendertagauswahl festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0580d-123">Any field displaying a calendar icon can be set using the calendar date picker.</span></span> <span data-ttu-id="0580d-124">Um die Kalendertagauswahl anzuzeigen, aktivieren Sie das Kalendersymbol oder drücken Sie die Tastenkombination STRG+POS1 im Feld.</span><span class="sxs-lookup"><span data-stu-id="0580d-124">To display the calendar date picker, activate the calendar icon or press the Ctrl + Home keyboard shortcut in the field.</span></span>

<span data-ttu-id="0580d-125">![Datumsfelder](media/ui-date-field.png "Beispiel eines Datumsfeldes")</span><span class="sxs-lookup"><span data-stu-id="0580d-125">![Date fields](media/ui-date-field.png "Example of a date field")</span></span>

<span data-ttu-id="0580d-126">Weitere Informationen unter [Tastenkombinationen in der Kalenderdatumsauswahl](keyboard-shortcuts.md#calendarshortcuts)</span><span class="sxs-lookup"><span data-stu-id="0580d-126">See also [Keyboard Shortcuts in the calendar date picker](keyboard-shortcuts.md#calendarshortcuts)</span></span>

### <a name="today"></a><span data-ttu-id="0580d-127">Heute</span><span class="sxs-lookup"><span data-stu-id="0580d-127">Today</span></span>
<span data-ttu-id="0580d-128">Geben Sie das Wort für `today` in der Sprache ein, die von der **Sprach**-Einstellung festgelegt wird. Dadurch wird das Datum auf das aktuelle Datum festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0580d-128">Enter the word for `today`, in the language set by **Language** setting, that will set the date to the current date.</span></span> <span data-ttu-id="0580d-129">Anstatt den gesamten Begriff einzugeben, können Sie einen Teil des Begriffs eingeben. Beginnen Sie mit `t` oder `tod`, sofern dies nicht auch der Beginn eines anderen Begriffs ist.</span><span class="sxs-lookup"><span data-stu-id="0580d-129">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as `t` or `tod`, as long as it is not also the start of another word.</span></span>

### <a name="day-week-year-pattern"></a><span data-ttu-id="0580d-130">Tag\-Woche\-Jahr-Muster</span><span class="sxs-lookup"><span data-stu-id="0580d-130">Day\-week\-year pattern</span></span>
<span data-ttu-id="0580d-131">Sie können ein Datum als Wochentag gefolgt von einer Wochennummer und optional einem Jahr eingeben.</span><span class="sxs-lookup"><span data-stu-id="0580d-131">You can enter a date as a weekday followed by a week number and, optionally, a year.</span></span> <span data-ttu-id="0580d-132">Beispielsweise bedeutet `Mon25` oder `mon25` Montag in der 25. Woche</span><span class="sxs-lookup"><span data-stu-id="0580d-132">For example, `Mon25` or `mon25` means Monday in week 25.</span></span> <span data-ttu-id="0580d-133">Wenn Sie kein Jahr eingeben, wird das Jahr des Arbeitsdatums verwendet.</span><span class="sxs-lookup"><span data-stu-id="0580d-133">If you do not enter a year, the year of the work date is used.</span></span>

<span data-ttu-id="0580d-134">Anstatt das gesamte Wort für den Wochentag einzugeben, können Sie vom Anfang an einen Teil des Begriffs eingeben.</span><span class="sxs-lookup"><span data-stu-id="0580d-134">Instead of entering the entire word for the day of the week, you can enter part of the word, starting from the beginning.</span></span> <span data-ttu-id="0580d-135">Bei Konflikten (wie bei `s` für Samstag oder Sonntag) werden die Tage entsprechend der Bereichseinstellung ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="0580d-135">In case of conflicts (such as with `s` which could be Saturday or Sunday), the days are evaluated according to the region setting.</span></span> <span data-ttu-id="0580d-136">Die Eingabe wird zuerst nach `workdate` auch `today` ausgewertet, beachten Sie dies bei der Abkürzung.</span><span class="sxs-lookup"><span data-stu-id="0580d-136">The input is first evaluated against `workdate` and `today` as well, so keep this in mind when abbreviating.</span></span> <span data-ttu-id="0580d-137">Beispielsweise bedeutet `t` heute, daher kann es nicht "Dienstag" oder "Donnerstag" bedeuten.</span><span class="sxs-lookup"><span data-stu-id="0580d-137">For example, `t` already means today, so it cannot mean Tuesday or Thursday.</span></span>

<span data-ttu-id="0580d-138">Das Kalenderwocheschema folgt immer ISO 8601. Dabei ist Woche 1, in die der 4. Januar fällt, oder die Woche mit dem ersten Donnerstag des Jahres.</span><span class="sxs-lookup"><span data-stu-id="0580d-138">The week number scheme is always ISO 8601, where week 1 is the week with 4 January in it, or the week with the first Thursday of the year.</span></span>

### <a name="digit-patterns"></a><span data-ttu-id="0580d-139">Ziffernmuster</span><span class="sxs-lookup"><span data-stu-id="0580d-139">Digit patterns</span></span>
<span data-ttu-id="0580d-140">In einem Datumsfeld können zwei-, vier-, sechs- oder achtstellige Werte eingegeben werden:</span><span class="sxs-lookup"><span data-stu-id="0580d-140">In a date field you can enter two, four, six, or eight digits:</span></span>

-   <span data-ttu-id="0580d-141">Wenn Sie nur zwei Ziffern eingeben, wird dies als Tagesangabe interpretiert, es gilt also der Monat und das Jahr des Arbeitsdatums.</span><span class="sxs-lookup"><span data-stu-id="0580d-141">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>

-   <span data-ttu-id="0580d-142">Wenn Sie vier Ziffern eingeben, wird dies als Tages- und Monatsangabe interpretiert, es gilt also das Jahr des Arbeitsdatums.</span><span class="sxs-lookup"><span data-stu-id="0580d-142">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span> <span data-ttu-id="0580d-143">Die Reihenfolge von Tag und Monat wird durch Ihre Regionseinstellungen bestimmt.</span><span class="sxs-lookup"><span data-stu-id="0580d-143">The order of the day and month is determined by your region settings.</span></span> <span data-ttu-id="0580d-144">Selbst wenn Ihre Regionseinstellungen das Jahr vor den Tag und Monat stellen, werden vier Ziffern als Tag und Monat interpretiert.</span><span class="sxs-lookup"><span data-stu-id="0580d-144">Even if your region settings have the year before the day and month, four digits are interpreted as the day and month.</span></span>

-   <span data-ttu-id="0580d-145">Wenn Sie ein Datum zwischen dem 01.01.1930 und dem 31.12.2029 eingeben wollen, können Sie das Jahr zweistellig eingeben; ansonsten muss das Jahr vierstellig angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0580d-145">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>

### <a name="current-work-date"></a><span data-ttu-id="0580d-146">Aktuelles Arbeitsdatum</span><span class="sxs-lookup"><span data-stu-id="0580d-146">Current work date</span></span>
<span data-ttu-id="0580d-147">Die Arbeitsdatumsfunktion ermöglicht es Ihnen Übergänge mithilfe eines Datums aufzuzeichnen, das sich vom aktuellen Datum unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="0580d-147">The work date feature allows you to record transations using a date that is different from the current date.</span></span>

<span data-ttu-id="0580d-148">Das für Wort "Arbeitsdatum" in der Sprache, die in der **Spracheinstellung** festgelegt ist, legt das Datum auf das aktuell festgelegte Arbeitsdatum fest, das auf der Seite [**Meine Einstellungen**](https://businesscentral.dynamics.com?page=9176 "Direkt zur Benutzereinstellungsseite in Business Central") angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0580d-148">The word for 'workdate', in the language set by **Language** setting, will set the date to the currently set work date that is specified on the [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central") page.</span></span> <span data-ttu-id="0580d-149">Anstatt das gesamte Wort einzugeben, können Sie vom Anfang an einen Teil des Begriffs eingeben, z. B. 'A' oder 'Arbeit'.</span><span class="sxs-lookup"><span data-stu-id="0580d-149">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as 'w' or 'work'.</span></span>

<span data-ttu-id="0580d-150">Wenn Sie kein Arbeitsdatum definiert haben, wird das aktuelle Datum als Arbeitsdatum verwendet.</span><span class="sxs-lookup"><span data-stu-id="0580d-150">If you have not defined a work date, the current date will be used as the work date.</span></span> <span data-ttu-id="0580d-151">Die Verwendung des Arbeitsdatums ist hilfreich, wenn eine Vielzahl von Transaktionen zu einem Datum ausgeführt werden müssen, das vom Systemdatum abweicht.</span><span class="sxs-lookup"><span data-stu-id="0580d-151">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>

<span data-ttu-id="0580d-152">Weitere Informationen finden Sie unter [Ändern von grundlegenden Einstellungen, wie dem Arbeitsdatum](ui-change-basic-settings.md#work-date).</span><span class="sxs-lookup"><span data-stu-id="0580d-152">See also [Changing Basic Settings, such as the Work Date](ui-change-basic-settings.md#work-date)</span></span>

### <a name="closing-date"></a><span data-ttu-id="0580d-153">Ultimodatum</span><span class="sxs-lookup"><span data-stu-id="0580d-153">Closing Date</span></span>
<span data-ttu-id="0580d-154">Wenn Sie ein Geschäftsjahr abschließen, können Sie mithilfe des Ultimodatums angeben, dass es sich bei einem Posten um einen Abschlussposten handelt.</span><span class="sxs-lookup"><span data-stu-id="0580d-154">When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry.</span></span> <span data-ttu-id="0580d-155">Technisch gesehen liegt ein Ultimodatum zwischen zwei Datumswerten, beispielsweise zwischen dem 31. Dezember und dem 1. Januar.</span><span class="sxs-lookup"><span data-stu-id="0580d-155">A closing date technically is between two dates, for example between Dec 31 and Jan 1.</span></span>

<span data-ttu-id="0580d-156">Setzen Sie ein `C` vor eine Datumsangabe, um anzugeben, dass es sich bei diesem Datum um ein Ultimodatum handelt, z. B. `C123101`.</span><span class="sxs-lookup"><span data-stu-id="0580d-156">To specify that a date is a closing date, put `C` just before the date, such as `C123101`.</span></span> <span data-ttu-id="0580d-157">Dies kann in Verbindung mit allen Datumsmustern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0580d-157">This can be used in combination with all the date patterns.</span></span>

### <a name="examples"></a><span data-ttu-id="0580d-158">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0580d-158">Examples</span></span>
<span data-ttu-id="0580d-159">Die folgende Tabelle enthält Beispiele von Datumsangaben, die alle diese Formate verwenden.</span><span class="sxs-lookup"><span data-stu-id="0580d-159">The following table contains examples of dates using all the formats.</span></span> <span data-ttu-id="0580d-160">Es nimmt Regionseinstellungen an, die Datumsangaben laut **year.month.day.** festlegen; eine Woche, die mit Montag beginnt und die englische Sprache.</span><span class="sxs-lookup"><span data-stu-id="0580d-160">It assumes region settings that format dates according to: **year.month.day.**, a week starting on Monday, and the English language.</span></span>

|<span data-ttu-id="0580d-161">**Eingabe**</span><span class="sxs-lookup"><span data-stu-id="0580d-161">**Entry**</span></span>      |<span data-ttu-id="0580d-162">**Interpretation**</span><span class="sxs-lookup"><span data-stu-id="0580d-162">**Interpretation**</span></span>      |
|---------------|------------------------|
|`2018.12.31.`|<span data-ttu-id="0580d-163">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="0580d-163">2018.12.31.</span></span>|
|`181231`|<span data-ttu-id="0580d-164">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="0580d-164">2018.12.31.</span></span>|
|`18.12.31.`|<span data-ttu-id="0580d-165">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="0580d-165">2018.12.31.</span></span>|
|`18.12.31.`|<span data-ttu-id="0580d-166">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="0580d-166">2018.12.31.</span></span>|
|`20181231`|<span data-ttu-id="0580d-167">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="0580d-167">2018.12.31.</span></span>|
|`18/12,31`|<span data-ttu-id="0580d-168">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="0580d-168">2018.12.31.</span></span>|
|`11`|<span data-ttu-id="0580d-169">Arbeitsdatum Jahr.Arbeitsdatum Monat.11</span><span class="sxs-lookup"><span data-stu-id="0580d-169">work date year.work date month.11.</span></span>|
|`1112`|<span data-ttu-id="0580d-170">Arbeitsdatum Jahr.11.12.</span><span class="sxs-lookup"><span data-stu-id="0580d-170">work date year.11.12.</span></span>|
|<span data-ttu-id="0580d-171">`t` oder `today`</span><span class="sxs-lookup"><span data-stu-id="0580d-171">`t` or `today`</span></span>|<span data-ttu-id="0580d-172">heutiges Datum</span><span class="sxs-lookup"><span data-stu-id="0580d-172">today's date</span></span>|
|<span data-ttu-id="0580d-173">`w` oder `workdate`</span><span class="sxs-lookup"><span data-stu-id="0580d-173">`w` or `workdate`</span></span>|<span data-ttu-id="0580d-174">das Arbeitsdatum</span><span class="sxs-lookup"><span data-stu-id="0580d-174">the working date</span></span>|
|<span data-ttu-id="0580d-175">`m` oder `Monday`</span><span class="sxs-lookup"><span data-stu-id="0580d-175">`m` or `Monday`</span></span>|<span data-ttu-id="0580d-176">Montag der Woche des Arbeitsdatums</span><span class="sxs-lookup"><span data-stu-id="0580d-176">Monday of the work date week</span></span>|
|<span data-ttu-id="0580d-177">`tu` oder `Tuesday`</span><span class="sxs-lookup"><span data-stu-id="0580d-177">`tu` or `Tuesday`</span></span>|<span data-ttu-id="0580d-178">Dienstag der Woche des Arbeitsdatums</span><span class="sxs-lookup"><span data-stu-id="0580d-178">Tuesday of the work date week</span></span>|
|<span data-ttu-id="0580d-179">`sa` oder `Saturday`</span><span class="sxs-lookup"><span data-stu-id="0580d-179">`sa` or `Saturday`</span></span>|<span data-ttu-id="0580d-180">Samstag der Woche des Arbeitsdatums</span><span class="sxs-lookup"><span data-stu-id="0580d-180">Saturday of the work date week</span></span>|
|<span data-ttu-id="0580d-181">`s` oder `Sunday`</span><span class="sxs-lookup"><span data-stu-id="0580d-181">`s` or `Sunday`</span></span>|<span data-ttu-id="0580d-182">Sonntag der Woche des Arbeitsdatums</span><span class="sxs-lookup"><span data-stu-id="0580d-182">Sunday of the work date week</span></span>|
|`t23`|<span data-ttu-id="0580d-183">Dienstag von Woche 23 des Arbeitsjahres</span><span class="sxs-lookup"><span data-stu-id="0580d-183">Tuesday of week 23 of the work date year</span></span>|
|`t 23`|<span data-ttu-id="0580d-184">Dienstag von Woche 23 des Arbeitsjahres</span><span class="sxs-lookup"><span data-stu-id="0580d-184">Tuesday of week 23 of the work date year</span></span>|
|`t-1`|<span data-ttu-id="0580d-185">Dienstag von Woche 1 des Arbeitsjahres</span><span class="sxs-lookup"><span data-stu-id="0580d-185">Tuesday of week 1 of the work date year</span></span>|

##  <a name="BKMK_SettingDateRanges"></a> <span data-ttu-id="0580d-186">Festlegen von Breichen</span><span class="sxs-lookup"><span data-stu-id="0580d-186">Setting Ranges</span></span>
<span data-ttu-id="0580d-187">In Listen, Summen und Berichten können Sie Filter für Datumsangaben, Uhrzeiten, Datums-/Uhrzeitangaben einrichten, die einen Startwert und optional einen Endwert haben, um nur die Datumsangaben anzuzeigen, die in diesem Bereich enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="0580d-187">On lists, totals and reports, you can set filters on dates, times and datetimes containing a start value and optionally an end value to display only the data contained in that range.</span></span> <span data-ttu-id="0580d-188">Die Standardregeln gelten für die Methode, auf die Sie Datumsbereiche festlegen.</span><span class="sxs-lookup"><span data-stu-id="0580d-188">The standard rules apply to the way you set date ranges.</span></span>

|<span data-ttu-id="0580d-189">**Bedeutung**</span><span class="sxs-lookup"><span data-stu-id="0580d-189">**Meaning**</span></span>|<span data-ttu-id="0580d-190">**Beispielausdruck (Datum)**</span><span class="sxs-lookup"><span data-stu-id="0580d-190">**Sample expression (Date)**</span></span>|<span data-ttu-id="0580d-191">**Im Filter enthaltene Daten**</span><span class="sxs-lookup"><span data-stu-id="0580d-191">**Data included in the filter**</span></span>|
|-----------|---------------------|--------------------|
|<span data-ttu-id="0580d-192">Intervall</span><span class="sxs-lookup"><span data-stu-id="0580d-192">Interval</span></span>|<span data-ttu-id="0580d-193">`12 15 00..01 15 01`  \n`..12 15 00`</span><span class="sxs-lookup"><span data-stu-id="0580d-193">`12 15 00..01 15 01`  \n`..12 15 00`</span></span>|<span data-ttu-id="0580d-194">Datensätze mit Datumsangaben zwischen und einschließlich dem 15.12.00 und dem 15.01.01.</span><span class="sxs-lookup"><span data-stu-id="0580d-194">Records with dates between and including 12 15 00 and 01 15 01.</span></span>  <span data-ttu-id="0580d-195">\nDatensätze mit Datumsangaben vom 12 15 00 oder früher.</span><span class="sxs-lookup"><span data-stu-id="0580d-195">\nRecords with dates of 12 15 00 or earlier.</span></span>|
|<span data-ttu-id="0580d-196">Entweder/oder</span><span class="sxs-lookup"><span data-stu-id="0580d-196">Either/or</span></span>|<span data-ttu-id="0580d-197">\`12 15 00</span><span class="sxs-lookup"><span data-stu-id="0580d-197">\`12 15 00</span></span>|<span data-ttu-id="0580d-198">12 16 00\`</span><span class="sxs-lookup"><span data-stu-id="0580d-198">12 16 00\`</span></span>|<span data-ttu-id="0580d-199">Datensätze mit den Datumsangaben 12 15 00 oder 12 16 00.</span><span class="sxs-lookup"><span data-stu-id="0580d-199">Records with dates of either 12 15 00 or 12 16 00.</span></span> <span data-ttu-id="0580d-200">Wenn es sowohl Datensätze mit Datumsangaben für beide Tage gibt, werden alle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0580d-200">If there are records with dates on both days, they will all be displayed.</span></span>|
|<span data-ttu-id="0580d-201">Kombination</span><span class="sxs-lookup"><span data-stu-id="0580d-201">Combination</span></span>|<span data-ttu-id="0580d-202">\`12 15 00</span><span class="sxs-lookup"><span data-stu-id="0580d-202">\`12 15 00</span></span>|<span data-ttu-id="0580d-203">12 01 00..12 10 00`  \n`..12 14 00</span><span class="sxs-lookup"><span data-stu-id="0580d-203">12 01 00..12 10 00`  \n`..12 14 00</span></span>|<span data-ttu-id="0580d-204">12 30 00..\`</span><span class="sxs-lookup"><span data-stu-id="0580d-204">12 30 00..\`</span></span>|<span data-ttu-id="0580d-205">Datensätze mit Datumsangaben vom 15.12.00 oder zwischen dem 01.12.00 und dem 10.12.00 einschließlich.</span><span class="sxs-lookup"><span data-stu-id="0580d-205">Records with dates of 12 15 00 or on dates between and including 12 01 00 and 12 10 00.</span></span>  <span data-ttu-id="0580d-206">\nDatensätze mit einem Datum von 14.12.00 oder früher, oder mit einem Datum von 30.12.00 und später, d. h. alle Datensätze außer solchen mit Datumsangaben zwischen dem 15.12.00 und dem 29.12.00 (jeweils einschließlich).</span><span class="sxs-lookup"><span data-stu-id="0580d-206">\nRecords with dates of 12 14 00 or earlier, or dates of 12 30 00 or later, that is, all records except those with dates between and including 12 15 00 and 12 29 00.</span></span>|

<span data-ttu-id="0580d-207">Sie können jedes der gültigen Formate in den Datumsbereichsfiltern verwenden.</span><span class="sxs-lookup"><span data-stu-id="0580d-207">You can use any of the valid formats in date range filters.</span></span> <span data-ttu-id="0580d-208">Beispielsweise ergibt `mon14 3..t 4p` bei einem Datums-/Zeitangabenfeld einen Filter von 3 Uhr morgens am Montag in der Woche 14 des Jahr des aktuellen Arbeitsdatums bis heute um 4 Uhr nachmittags.</span><span class="sxs-lookup"><span data-stu-id="0580d-208">For example, `mon14 3..t 4p` applied on a datetime field results in a filter from 3 AM on Monday in week 14 of the current work date year, inclusive, until today at 4PM, inclusive.</span></span>


## <a name="using-date-formulas"></a><span data-ttu-id="0580d-209">Verwenden von Datumsformeln</span><span class="sxs-lookup"><span data-stu-id="0580d-209">Using Date Formulas</span></span>
<span data-ttu-id="0580d-210">Bei einer Datumsformel handelt es sich um eine verkürzte Kombination aus Buchstaben und Zahlen, die zum Berechnen von Datumswerten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0580d-210">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="0580d-211">Sie können Datumsformeln in verschiedenen Datumsberechnungsfeldern oder -filtern eingeben.</span><span class="sxs-lookup"><span data-stu-id="0580d-211">You can enter date formulas in various date calculation fields or filters.</span></span>

> [!NOTE]
>  <span data-ttu-id="0580d-212">In allen Formelfeldern wird automatisch ein Tag aufgenommen, um den heutigen Tag als den Tag abzudecken, an dem die Periode beginnt.</span><span class="sxs-lookup"><span data-stu-id="0580d-212">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="0580d-213">Wenn Sie beispielsweise `1W` eingeben, ist der Zeitraum tatsächlich acht Tage, da der aktuelle Tag (heute) eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="0580d-213">Accordingly, for example, if you enter `1W`, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="0580d-214">Um eine Periode von sieben Tagen \(tatsächlich eine Woche\) einschließlich des Periodenstartdatums anzugeben, müssen Sie `6D` oder `1W-1D` eingeben.</span><span class="sxs-lookup"><span data-stu-id="0580d-214">To specify a period of seven days \(one true week\) including the period starting date, then you must enter `6D` or `1W-1D`.</span></span>

<span data-ttu-id="0580d-215">Nachfolgend finden Sie einige Verwendungsbeispiele für Datumsformeln:</span><span class="sxs-lookup"><span data-stu-id="0580d-215">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="0580d-216">In wiederkehrenden Buch.-Blättern wird anhand der Datumsformel im Feld "Wiederholungsrate" bestimmt, wie oft der Posten in der Buch.-Blattzeile gebucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="0580d-216">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="0580d-217">Anhand der Datumsformel im Feld **Toleranzperiode** für eine Mahnstufe wird die Zeit bestimmt, die vom Fälligkeitsdatum \(oder vom Datum der letzten Mahnung\) an vergehen muss, bevor eine Mahnung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0580d-217">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date \(or from the date of the previous reminder\) before a reminder will be created.</span></span>

-   <span data-ttu-id="0580d-218">Das Datumsformat im Feld **Berechnung des Fälligkeitsdatums** bestimmt, wie das Fälligkeitsdatum auf der Erinnerung berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="0580d-218">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="0580d-219">Die Datumsformel kann maximal 20 Zeichen (Buchstaben und Zahlen) enthalten.</span><span class="sxs-lookup"><span data-stu-id="0580d-219">The date formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="0580d-220">Für die Kalendereinheiten können die folgenden Abkürzungen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="0580d-220">You can use the following letters, which are abbreviations for calendar units.</span></span>

|  <span data-ttu-id="0580d-221">Brief</span><span class="sxs-lookup"><span data-stu-id="0580d-221">Letter</span></span>  |  <span data-ttu-id="0580d-222">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0580d-222">Meaning</span></span>  |
|----------|----------------------|
|`C`|<span data-ttu-id="0580d-223">Aktuell</span><span class="sxs-lookup"><span data-stu-id="0580d-223">Current</span></span>|
|`D`|<span data-ttu-id="0580d-224">Tag\(e\)</span><span class="sxs-lookup"><span data-stu-id="0580d-224">Day\(s\)</span></span>|
|`W`|<span data-ttu-id="0580d-225">Woche\(n\)</span><span class="sxs-lookup"><span data-stu-id="0580d-225">Week\(s\)</span></span>|
|`M`|<span data-ttu-id="0580d-226">Monat\(e\)</span><span class="sxs-lookup"><span data-stu-id="0580d-226">Month\(s\)</span></span>|
|`Q`|<span data-ttu-id="0580d-227">Quartal\(e\)</span><span class="sxs-lookup"><span data-stu-id="0580d-227">Quarter\(s\)</span></span>|
|`Y`|<span data-ttu-id="0580d-228">Jahr\(e\)</span><span class="sxs-lookup"><span data-stu-id="0580d-228">Year\(s\)</span></span>|

<span data-ttu-id="0580d-229">Datumsformeln können auf drei Arten erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0580d-229">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="0580d-230">Im folgenden Beispiel wird veranschaulicht, wie Sie `C`, für aktuell und eine Zeiteinheit verwenden.</span><span class="sxs-lookup"><span data-stu-id="0580d-230">The following example shows how to use `C`, for current, and a time unit.</span></span>

|  <span data-ttu-id="0580d-231">Ausdruck</span><span class="sxs-lookup"><span data-stu-id="0580d-231">Expression</span></span>  |  <span data-ttu-id="0580d-232">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0580d-232">Meaning</span></span>  |
|--------------|-----------|
|`CW`|<span data-ttu-id="0580d-233">Laufende Woche</span><span class="sxs-lookup"><span data-stu-id="0580d-233">Current week</span></span>|
|`CM`|<span data-ttu-id="0580d-234">Laufender Monat</span><span class="sxs-lookup"><span data-stu-id="0580d-234">Current month</span></span>|

<span data-ttu-id="0580d-235">Im folgenden Beispiel wird veranschaulicht, wie Sie eine Zahl und eine Zeiteinheit verwenden.</span><span class="sxs-lookup"><span data-stu-id="0580d-235">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="0580d-236">Eine Zahl darf nicht größer sein als 9999.</span><span class="sxs-lookup"><span data-stu-id="0580d-236">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="0580d-237">Ausdruck</span><span class="sxs-lookup"><span data-stu-id="0580d-237">Expression</span></span>  |  <span data-ttu-id="0580d-238">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0580d-238">Meaning</span></span>  |
|--------------|-----------|
|`10D`|<span data-ttu-id="0580d-239">10 Tage ab heute</span><span class="sxs-lookup"><span data-stu-id="0580d-239">10 days from today</span></span>|
|`2W`|<span data-ttu-id="0580d-240">2 Wochen ab heute</span><span class="sxs-lookup"><span data-stu-id="0580d-240">2 weeks from today</span></span>|

<span data-ttu-id="0580d-241">Im folgenden Beispiel wird veranschaulicht, wie Sie eine Zeiteinheit und eine Zahl verwenden.</span><span class="sxs-lookup"><span data-stu-id="0580d-241">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="0580d-242">Ausdruck</span><span class="sxs-lookup"><span data-stu-id="0580d-242">Expression</span></span>  |  <span data-ttu-id="0580d-243">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0580d-243">Meaning</span></span>  |
|--------------|-----------|
|`D10`|<span data-ttu-id="0580d-244">Der nächste 10. eines Monats</span><span class="sxs-lookup"><span data-stu-id="0580d-244">The next 10th day of a month</span></span>|
|`WD4`|<span data-ttu-id="0580d-245">Der nächste 4. einer Woche \(Donnerstag\)</span><span class="sxs-lookup"><span data-stu-id="0580d-245">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="0580d-246">Das folgende Beispiel zeigt, wie Sie diese drei Formulare nach Bedarf kombinieren können.</span><span class="sxs-lookup"><span data-stu-id="0580d-246">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="0580d-247">Ausdruck</span><span class="sxs-lookup"><span data-stu-id="0580d-247">Expression</span></span>  |  <span data-ttu-id="0580d-248">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0580d-248">Meaning</span></span>  |
|--------------|-----------|
|`CM+10D`|<span data-ttu-id="0580d-249">Aktueller Monat\+ 10 Tage</span><span class="sxs-lookup"><span data-stu-id="0580d-249">Current month \+ 10 days</span></span>|

<span data-ttu-id="0580d-250">Das folgende Beispiel zeigt, wie Sie ein Minuszeichen verwenden können, um anzugeben, dass es sich um ein Datum in der Vergangenheit handelt.</span><span class="sxs-lookup"><span data-stu-id="0580d-250">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="0580d-251">Ausdruck</span><span class="sxs-lookup"><span data-stu-id="0580d-251">Expression</span></span>  |  <span data-ttu-id="0580d-252">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0580d-252">Meaning</span></span>  |
|--------------|-----------|
|`-1Y`|<span data-ttu-id="0580d-253">Heute vor einem Jahr</span><span class="sxs-lookup"><span data-stu-id="0580d-253">1 year ago from today</span></span>|

> [!IMPORTANT]
>  <span data-ttu-id="0580d-254">Wenn für den Lagerort einen Grundkalender verwendet, wird das Datumsformular, das Sie eingeben, zum Beispiel das Feld **Transportzeit**, entsprechend der Kalenderarbeitstage interpretiert.</span><span class="sxs-lookup"><span data-stu-id="0580d-254">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="0580d-255">Zum Beispiel entspricht `1W` sieben Arbeitstagen.</span><span class="sxs-lookup"><span data-stu-id="0580d-255">For example, `1W`  means seven working days.</span></span>
<!--
# Entering Date Ranges
You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges. Let's take the **Customer Top 10** as an example:

![Setting a date range in the request page for the Customer Top 10 list](./media/ui-enter-date-ranges/customer-top10-list.png)

Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want. To set date ranges, you enter dates and then use either **..** or **|** to set the range. In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.
Here are a couple of other examples:

| Meaning | Example | Entries included |
|---|---|---|
|Equal to| 12 15 16 |Only those posted on December 15 2016.|
|Interval| 12 15 16..01 15 17<br /><br />..12 15 16|Those posted on dates between and including December 15 2016 and January 15 2017.<br /><br />Those posted on December 15 2016 or earlier.|
|Either/or|12 15 16&#124;12 16 16|Those posted on either December 15 or December 16 2016. If there are entries posted on both days, they will all be displayed.|

You can also combine the various format types.

| Example | Entries included |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017. |
|..12 14 16&#124;12 30 16.. | Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29. |

Note that we have used the US date format MMDDYY here. As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.

## Using Date Formulas
A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.

> [!NOTE]
>  In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, for example, if you enter **1W**, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter **6D** or **1W\-1D**.

Here are some examples of how date formulas can be used:

-   The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.

-   The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date (or from the due date of the previous reminder) before a reminder will be created.

-   The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.

The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.

|  Letter  |  Time specification  |
|----------|----------------------|
|C|Current|
|D|Day\(s\)|
|W|Week\(s\)|
|M|Month\(s\)|
|Q|Quarter\(s\)|
|Y|Year\(s\)|

You can construct a date formula in three ways.

The following example shows how to use **C**, for current, and a time unit.

|  Expression  |  Meaning  |
|--------------|-----------|
|CW|Current week|
|CM|Current month|

The following example shows how to use a number and a time unit. A number cannot be larger than 9999.

|  Expression  |  Meaning  |
|--------------|-----------|
|10D|10 days from today|
|2W|2 weeks from today|

The following example shows how to use a time unit and a number.

|  Expression  |  Meaning  |
|--------------|-----------|
|D10|The next 10th day of a month|
|WD4|The next 4th day of a week \(Thursday\)|

The following example shows how you can combine these three forms as needed.

|  Expression  |  Meaning  |
|--------------|-----------|
|CM\+10D|Current month \+ 10 days|

The following example shows how you can use a minus sign to indicate a date in the past.

|  Expression  |  Meaning  |
|--------------|-----------|
|-1Y|1 year ago from today|

> [!IMPORTANT]
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, **1W**  means seven working days.

-->

## <a name="entering-times"></a><span data-ttu-id="0580d-256">Eingeben von Uhrzeiten</span><span class="sxs-lookup"><span data-stu-id="0580d-256">Entering Times</span></span>
<span data-ttu-id="0580d-257">Beim der Eingabe von Uhrzeiten können Sie alle Trennzeichen außer Leerzeichen einfügen, die zwischen den Einheiten angegeben werden sollen. Bei der Verwendung von zweistelligen Zahlen für jede Einheit bis zu MilliseDebitoren ist dies nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0580d-257">When you enter times, you can insert any non-space separators that you want between the units, but if you use double digits for each unit up to milliseconds, then it is not required.</span></span>

<span data-ttu-id="0580d-258">Sie müssen lediglich die größten Einheiten schreiben, die Sie benötigen; der Rest wird auf null gesetzt.</span><span class="sxs-lookup"><span data-stu-id="0580d-258">You only have to write the largest units that you require; the rest will be set to zero.</span></span> <span data-ttu-id="0580d-259">Sie können auch alle Tageszeitangaben (AM/PM) auslassen.</span><span class="sxs-lookup"><span data-stu-id="0580d-259">You can also leave out any AM/PM indicator.</span></span>

<span data-ttu-id="0580d-260">In der folgenden Tabelle finden Sie eine Übersicht über die Möglichkeiten zum Angeben von Uhrzeiten sowie die Interpretation der jeweiligen Angabe.</span><span class="sxs-lookup"><span data-stu-id="0580d-260">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span> <span data-ttu-id="0580d-261">Es werden Regionseinstellungen angenommen, mit der die Uhrzeit wie folgt formatiert wird: **Stunden:Minuten: SeDebitoren:MilliseDebitoren.**</span><span class="sxs-lookup"><span data-stu-id="0580d-261">It assumes region settings that format times according to: **Hours:Minutes:Seconds.Milliseconds.**</span></span> <span data-ttu-id="0580d-262">und verwenden die jeweiligen Tageszeitangaben (AM/PM).</span><span class="sxs-lookup"><span data-stu-id="0580d-262">and use the AM and PM indicators of 'AM' and 'PM', respectively.</span></span>

|<span data-ttu-id="0580d-263">**Eingabe**</span><span class="sxs-lookup"><span data-stu-id="0580d-263">**Entry**</span></span>      |<span data-ttu-id="0580d-264">**Interpretation**</span><span class="sxs-lookup"><span data-stu-id="0580d-264">**Interpretation**</span></span>      |
|---------------|------------------------|
|`05:23:17`|<span data-ttu-id="0580d-265">05:23:17</span><span class="sxs-lookup"><span data-stu-id="0580d-265">05:23:17</span></span>|
|`5`|<span data-ttu-id="0580d-266">05:00:00</span><span class="sxs-lookup"><span data-stu-id="0580d-266">05:00:00</span></span>|
|`5AM`|<span data-ttu-id="0580d-267">05:00:00</span><span class="sxs-lookup"><span data-stu-id="0580d-267">05:00:00</span></span>|
|`5P`|<span data-ttu-id="0580d-268">17:00:00</span><span class="sxs-lookup"><span data-stu-id="0580d-268">17:00:00</span></span>|
|`12`|<span data-ttu-id="0580d-269">12:00:00</span><span class="sxs-lookup"><span data-stu-id="0580d-269">12:00:00</span></span>|
|`12A`|<span data-ttu-id="0580d-270">00:00:00</span><span class="sxs-lookup"><span data-stu-id="0580d-270">00:00:00</span></span>|
|`12P`|<span data-ttu-id="0580d-271">12:00:00</span><span class="sxs-lookup"><span data-stu-id="0580d-271">12:00:00</span></span>|
|`17`|<span data-ttu-id="0580d-272">17:00:00</span><span class="sxs-lookup"><span data-stu-id="0580d-272">17:00:00</span></span>|
|`5:30`|<span data-ttu-id="0580d-273">05:30:00</span><span class="sxs-lookup"><span data-stu-id="0580d-273">05:30:00</span></span>|
|`0530`|<span data-ttu-id="0580d-274">05:30:00</span><span class="sxs-lookup"><span data-stu-id="0580d-274">05:30:00</span></span>|
|`5:30:5`|<span data-ttu-id="0580d-275">05:30:05</span><span class="sxs-lookup"><span data-stu-id="0580d-275">05:30:05</span></span>|
|`053005`|<span data-ttu-id="0580d-276">05:30:05</span><span class="sxs-lookup"><span data-stu-id="0580d-276">05:30:05</span></span>|
|`5:30:5,50`|<span data-ttu-id="0580d-277">05:30:05,5</span><span class="sxs-lookup"><span data-stu-id="0580d-277">05:30:05.5</span></span>|
|`053005050`|<span data-ttu-id="0580d-278">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="0580d-278">05:30:05.05</span></span>|

<span data-ttu-id="0580d-279">Beachten Sie, dass MilliseDebitoren in Dezimalnotation angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0580d-279">You should be aware that milliseconds are interpreted as decimal notation.</span></span> <span data-ttu-id="0580d-280">`3`, `30` und `300` bedeuten beispielsweise alle 300 MilliseDebitoren, während `03` `30` und `003` zum 3 MilliseDebitoren bedeuten.</span><span class="sxs-lookup"><span data-stu-id="0580d-280">So, for example, `3`, `30`, and `300` all mean 300 milliseconds, while `03` means `30` and `003` means 3 milliseconds.</span></span>

<span data-ttu-id="0580d-281">Sie können `24:00` nicht verwenden, um Mitternacht anzugeben oder einen Wert angeben, der größer als 24:00 ist.</span><span class="sxs-lookup"><span data-stu-id="0580d-281">You cannot use `24:00` to mean midnight, or use any value greater than 24:00.</span></span>

<span data-ttu-id="0580d-282">Das für Wort für "Zeit" in der Sprache, die von [!INCLUDE[d365fin](includes/d365fin_long_md.md)] verwendet wird, wird in die aktuelle Uhrzeit auf Ihrem Computer oder mobilen Gerät umgerechnet.</span><span class="sxs-lookup"><span data-stu-id="0580d-282">The word for 'time' in the language used by [!INCLUDE[d365fin](includes/d365fin_long_md.md)] will be evaluated to the current time on your computer or mobile device.</span></span> <span data-ttu-id="0580d-283">Sie können vom Anfang einem Teil des Begriffs eingeben, z. B. `t` oder `TIM`.</span><span class="sxs-lookup"><span data-stu-id="0580d-283">You can enter any part of the word, starting from the beginning, such as `t` or `TIM`.</span></span>

## <a name="entering-combined-dates-and-times"></a><span data-ttu-id="0580d-284">Eingeben kombinierter Datums- und Zeitangaben</span><span class="sxs-lookup"><span data-stu-id="0580d-284">Entering combined Dates and Times</span></span>
<span data-ttu-id="0580d-285">Wenn Sie Datums-/Uhrzeitangaben eingeben, die aus einem kombinierten Datum und einer Uhrzeit in einem Feld bestehen, müssen Sie ein Leerzeichen zwischen dem Datum und der Uhrzeit eingeben.</span><span class="sxs-lookup"><span data-stu-id="0580d-285">When you enter datetimes, which are a date and time combined into one field, you must enter a space between the date and the time.</span></span> <span data-ttu-id="0580d-286">Der Datumsteil kann nur Stellen in Form von den offiziellen Datumstrennzeichen Ihrer Regionseinstellung enthalten.</span><span class="sxs-lookup"><span data-stu-id="0580d-286">The date part can only contain spaces in the form of the official date separator of your region settings.</span></span> <span data-ttu-id="0580d-287">Die Uhrzeit kann Stellen um die AM/AM-Angabe enthalten.</span><span class="sxs-lookup"><span data-stu-id="0580d-287">The time can contain spaces around the AM/PM indicator.</span></span>

<span data-ttu-id="0580d-288">Sie können auch nur ein Datum in einem Datums-/Uhrzeitangabefeld eingeben, aber Sie können nicht bloß eine Uhrzeit angeben.</span><span class="sxs-lookup"><span data-stu-id="0580d-288">It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.</span></span>

<span data-ttu-id="0580d-289">Die folgende Tabelle führt einige Beispiele von Datum-/Uhrzeitkombinationen auf.</span><span class="sxs-lookup"><span data-stu-id="0580d-289">The following table lists some examples of date/time combinations.</span></span> <span data-ttu-id="0580d-290">Die Regionseinstellungen in den Beispielen zeigen Datumsangaben im Tag\-Monat\-Jahr-Format mit den AM/PM-Angaben, der englischen Sprache und Sonntag als Start der Woche an.</span><span class="sxs-lookup"><span data-stu-id="0580d-290">The region settings in the examples displays dates in the day\-month\-year format, using AM/PM designators, English language, and Sunday as the start of the week.</span></span>

|<span data-ttu-id="0580d-291">**Eingabe**</span><span class="sxs-lookup"><span data-stu-id="0580d-291">**Entry**</span></span>      |<span data-ttu-id="0580d-292">**Interpretation**</span><span class="sxs-lookup"><span data-stu-id="0580d-292">**Interpretation**</span></span>      |
|---------------|------------------------|
|`08-01-2016 05:48:12 PM`|<span data-ttu-id="0580d-293">08\-01\-2016 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="0580d-293">08\-01\-2016 05:48:12 PM</span></span>|
|`131202 132455`|<span data-ttu-id="0580d-294">13\-12\-2002 13:24:55</span><span class="sxs-lookup"><span data-stu-id="0580d-294">13\-12\-2002 13:24:55</span></span>|
|`1-12-02 10`|<span data-ttu-id="0580d-295">01\-12\-2002 10:00:00</span><span class="sxs-lookup"><span data-stu-id="0580d-295">01\-12\-2002 10:00:00</span></span>|
|`1.12.02 5`|<span data-ttu-id="0580d-296">01\-12\-2002 05:00:00</span><span class="sxs-lookup"><span data-stu-id="0580d-296">01\-12\-2002 05:00:00</span></span>|
|`1.12.02`|<span data-ttu-id="0580d-297">01\-12\-2002 00:00:00</span><span class="sxs-lookup"><span data-stu-id="0580d-297">01\-12\-2002 00:00:00</span></span>|
|`11 12`|<span data-ttu-id="0580d-298">11\-Arbeitsdatum Monat\-Arbeitsdatum Jahr 12:00:00</span><span class="sxs-lookup"><span data-stu-id="0580d-298">11\-work date month\-work date year 12:00:00</span></span>|
|`1112 12`|<span data-ttu-id="0580d-299">11\-12\-Arbeitsdatum Jahr 12:00:00</span><span class="sxs-lookup"><span data-stu-id="0580d-299">11\-12\-work date year 12:00:00</span></span>|
|<span data-ttu-id="0580d-300">`t` oder `today`</span><span class="sxs-lookup"><span data-stu-id="0580d-300">`t` or `today`</span></span>|<span data-ttu-id="0580d-301">heutiges Datum 00:00:00</span><span class="sxs-lookup"><span data-stu-id="0580d-301">today's date 00:00:00</span></span>|
|`t 10:30`|<span data-ttu-id="0580d-302">heutiges Datum 10:30:00</span><span class="sxs-lookup"><span data-stu-id="0580d-302">today's date 10:30:00</span></span>|
|`t 3:3:3`|<span data-ttu-id="0580d-303">heutiges Datum 03:03:03</span><span class="sxs-lookup"><span data-stu-id="0580d-303">today's date 03:03:03</span></span>|
|<span data-ttu-id="0580d-304">`w` oder `workdate`</span><span class="sxs-lookup"><span data-stu-id="0580d-304">`w` or `workdate`</span></span>|<span data-ttu-id="0580d-305">das Arbeitsdatum 00:00:00</span><span class="sxs-lookup"><span data-stu-id="0580d-305">the working date 00:00:00</span></span>|
|<span data-ttu-id="0580d-306">`m` oder `Monday`</span><span class="sxs-lookup"><span data-stu-id="0580d-306">`m` or `Monday`</span></span>|<span data-ttu-id="0580d-307">Montag der Woche des Arbeitsdatums 00:00:00</span><span class="sxs-lookup"><span data-stu-id="0580d-307">Monday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="0580d-308">`tu` oder `Tuesday`</span><span class="sxs-lookup"><span data-stu-id="0580d-308">`tu` or `Tuesday`</span></span>|<span data-ttu-id="0580d-309">Dienstag der Woche des Arbeitsdatums 00:00:00</span><span class="sxs-lookup"><span data-stu-id="0580d-309">Tuesday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="0580d-310">`sa` oder `Saturday`</span><span class="sxs-lookup"><span data-stu-id="0580d-310">`sa` or `Saturday`</span></span>|<span data-ttu-id="0580d-311">Samstag der Woche des Arbeitsdatums 00:00:00</span><span class="sxs-lookup"><span data-stu-id="0580d-311">Saturday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="0580d-312">`s` oder `Sunday`</span><span class="sxs-lookup"><span data-stu-id="0580d-312">`s` or `Sunday`</span></span>|<span data-ttu-id="0580d-313">Sonntag der Woche des Arbeitsdatums 00:00:00</span><span class="sxs-lookup"><span data-stu-id="0580d-313">Sunday of the work date week 00:00:00</span></span>|
|`tu 10:30`|<span data-ttu-id="0580d-314">Dienstag der Woche des Arbeitsdatums 10:30:00</span><span class="sxs-lookup"><span data-stu-id="0580d-314">Tuesday of the work date week 10:30:00</span></span>|
|`tu 3:3:3`|<span data-ttu-id="0580d-315">Dienstag der Woche des Arbeitsdatums 03:03:03</span><span class="sxs-lookup"><span data-stu-id="0580d-315">Tuesday of the work date week 03:03:03</span></span>|
|`t23 t`|<span data-ttu-id="0580d-316">Dienstag der Woche 23 des Jahres des Arbeitsdatums, aktuelle Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="0580d-316">Tuesday of week 23 of the work date year, current time of day</span></span>|
|`t23`|<span data-ttu-id="0580d-317">Dienstag von Woche 23 des Arbeitsjahres</span><span class="sxs-lookup"><span data-stu-id="0580d-317">Tuesday of week 23 of the work date year</span></span>|
|`t 23`|<span data-ttu-id="0580d-318">Heute 23:00:00</span><span class="sxs-lookup"><span data-stu-id="0580d-318">Today 23:00:00</span></span>|
|`t-1`|<span data-ttu-id="0580d-319">Dienstag von Woche 1 des Arbeitsjahres</span><span class="sxs-lookup"><span data-stu-id="0580d-319">Tuesday of week 1 of the work date year</span></span>|

## <a name="entering-duration"></a><span data-ttu-id="0580d-320">Eingeben von Terminen</span><span class="sxs-lookup"><span data-stu-id="0580d-320">Entering Duration</span></span>
<span data-ttu-id="0580d-321">Einige Felder in der Anwendung stellen eine Dauer oder Betrag der verstrichenen Uhrzeit, anstatt einer bestimmten Datums- oder Uhrzeitangabe dar.</span><span class="sxs-lookup"><span data-stu-id="0580d-321">Some fields in the application represent a duration, or amount of elapsed time, instead of a specific date or time.</span></span> <span data-ttu-id="0580d-322">Zeiträume können als Zahl gefolgt von der entsprechenden Einheit eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0580d-322">You enter a duration as a number followed by its unit of measure.</span></span>

<span data-ttu-id="0580d-323">Hier folgen einige Beispiele.</span><span class="sxs-lookup"><span data-stu-id="0580d-323">Here are some examples.</span></span>

|<span data-ttu-id="0580d-324">**Termine**</span><span class="sxs-lookup"><span data-stu-id="0580d-324">**Duration**</span></span>|<span data-ttu-id="0580d-325">**Einheit**</span><span class="sxs-lookup"><span data-stu-id="0580d-325">**Unit of measure**</span></span>|
|------------|-------------------|
|`2h`|<span data-ttu-id="0580d-326">2 Stunden</span><span class="sxs-lookup"><span data-stu-id="0580d-326">2 hrs</span></span>|
|`6h 30 m`|<span data-ttu-id="0580d-327">6 Stunden 30 Minuten</span><span class="sxs-lookup"><span data-stu-id="0580d-327">6 hrs 30 mins</span></span>|
|`6.5h`|<span data-ttu-id="0580d-328">6 Stunden 30 Minuten</span><span class="sxs-lookup"><span data-stu-id="0580d-328">6 hrs 30 mins</span></span>|
|`90m`|<span data-ttu-id="0580d-329">1 Stunde 30 Minuten</span><span class="sxs-lookup"><span data-stu-id="0580d-329">1 hr 30 mins</span></span>|
|`2d 6h 30m`|<span data-ttu-id="0580d-330">2 Tage 6 Stunden 30 Minuten</span><span class="sxs-lookup"><span data-stu-id="0580d-330">2 days 6 hrs 30 mins</span></span>|
|`2d 6h 30m 56s 600ms`|<span data-ttu-id="0580d-331">2 Tage 6 Stunden 30 Minuten 56 SeDebitoren 600 MilliseDebitoren</span><span class="sxs-lookup"><span data-stu-id="0580d-331">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|

<span data-ttu-id="0580d-332">Sie haben auch die Möglichkeit, eine Zahl einzugeben, die automatisch in einen Zeitraum umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="0580d-332">You can also enter a number, which will be automatically converted to a duration.</span></span> <span data-ttu-id="0580d-333">Die eingegebene Zahl wird entsprechend der Standardeinheit konvertiert, die im Feld "Dauer" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="0580d-333">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>

<span data-ttu-id="0580d-334">Geben Sie zum Ermitteln der Einheit, die für ein Feld vom Typ "Dauer" verwendet wird, eine Zahl ein. Am Ergebnis können Sie ablesen, in welche Einheit diese konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="0580d-334">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>

<span data-ttu-id="0580d-335">Wenn die Maßeinheit beispielsweise Stunden ist, wird die Zahl `5` in 5 h konvertiert.</span><span class="sxs-lookup"><span data-stu-id="0580d-335">For example, if the unit of measure is hours, the number `5` is converted to 5 hrs.</span></span>


## <a name="see-also"></a><span data-ttu-id="0580d-336">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0580d-336">See Also</span></span>
<span data-ttu-id="0580d-337">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0580d-337">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="0580d-338">Terminberechnung für Einkäufe</span><span class="sxs-lookup"><span data-stu-id="0580d-338">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="0580d-339">Eingeben von Kriterien in Filtern</span><span class="sxs-lookup"><span data-stu-id="0580d-339">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  

