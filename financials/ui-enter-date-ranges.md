---
title: Datenbereich in Finance and Operations, Business edition  | Microsoft Docs einrichten
description: "Erhalten von Informationen zum Anzeigen von Daten aus bestimmten Zeiträumen mithilfe von Finance and Operations, Business edition"
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 05/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: da2fea4e095c8211f30aaa7c570a84a005e7cbc8
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="entering-date-ranges-in-finance-and-operations-business-edition"></a><span data-ttu-id="42bd4-103">Änderungen von Datenbereichen in Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="42bd4-103">Entering Date Ranges in Finance and Operations, Business edition</span></span> 
<span data-ttu-id="42bd4-104">Sie können Filter mit einem Start- und Enddatum setzen, sodass lediglich die Daten angezeigt werden, die innerhalb eines bestimmten Datumsbereichs oder Zeitintervalls liegen.</span><span class="sxs-lookup"><span data-stu-id="42bd4-104">You can set filters containing a start date and an end date to display only the data contained in that date range or time interval.</span></span> <span data-ttu-id="42bd4-105">Für das Festlegen von Datumsbereichen gelten besondere Regeln.</span><span class="sxs-lookup"><span data-stu-id="42bd4-105">Special rules apply to the way you set date ranges.</span></span> <span data-ttu-id="42bd4-106">Als Beispiel nehmen wir die **Top 10 Debitoren**.</span><span class="sxs-lookup"><span data-stu-id="42bd4-106">Let's take the **Customer Top 10** as an example:</span></span>

![Einen Datumsbereich auf der Anforderungsseite der Top 10 Debitorenliste festlegen](./media/ui-enter-date-ranges/customer-top10-list.png)

<span data-ttu-id="42bd4-108">Hier können Sie den Bericht auf eine Gültigkeit wie den letzten 2 Wochen oder insgesamt 6 Wochen oder einen beliebigen Bereich einschränken.</span><span class="sxs-lookup"><span data-stu-id="42bd4-108">Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want.</span></span> <span data-ttu-id="42bd4-109">Um eine Gültigkeit festzulegen, geben Sie Daten ein und verwenden anschließend **..**</span><span class="sxs-lookup"><span data-stu-id="42bd4-109">To set date ranges, you enter dates and then use either **..**</span></span> <span data-ttu-id="42bd4-110">oder **|**, um den Bereich zu ändern.</span><span class="sxs-lookup"><span data-stu-id="42bd4-110">or **|** to set the range.</span></span> <span data-ttu-id="42bd4-111">Im vorliegenden Beispiel müssen Sie, um die ersten zwei Wochen des Mai für die Top 10 Debitoren anzuzeigen, den Datumsfilter auf *05 01 17..05 14 17* setzen.</span><span class="sxs-lookup"><span data-stu-id="42bd4-111">In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.</span></span>
<span data-ttu-id="42bd4-112">Hier finden Sie einige andere Beispiele:</span><span class="sxs-lookup"><span data-stu-id="42bd4-112">Here are a couple of other examples:</span></span>

| <span data-ttu-id="42bd4-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="42bd4-113">Meaning</span></span> | <span data-ttu-id="42bd4-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="42bd4-114">Example</span></span> | <span data-ttu-id="42bd4-115">Enthaltene Posten</span><span class="sxs-lookup"><span data-stu-id="42bd4-115">Entries included</span></span> |
|---|---|---|
|<span data-ttu-id="42bd4-116">Ist gleich</span><span class="sxs-lookup"><span data-stu-id="42bd4-116">Equal to</span></span>| <span data-ttu-id="42bd4-117">12 15 16</span><span class="sxs-lookup"><span data-stu-id="42bd4-117">12 15 16</span></span> |<span data-ttu-id="42bd4-118">Nur jene, die am 15. Deuzember 2016 gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="42bd4-118">Only those posted on December 15 2016.</span></span>|
|<span data-ttu-id="42bd4-119">Intervall</span><span class="sxs-lookup"><span data-stu-id="42bd4-119">Interval</span></span>| <span data-ttu-id="42bd4-120">12 15 16..01 15 17</span><span class="sxs-lookup"><span data-stu-id="42bd4-120">12 15 16..01 15 17</span></span><br /><br /><span data-ttu-id="42bd4-121">..12 15 16</span><span class="sxs-lookup"><span data-stu-id="42bd4-121">..12 15 16</span></span>|<span data-ttu-id="42bd4-122">Jene, die zwischen dem 15. Dezember 2016 und dem 15. Januar 2017 (einschließlich) gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="42bd4-122">Those posted on dates between and including December 15 2016 and January 15 2017.</span></span><br /><br /><span data-ttu-id="42bd4-123">Jene, die bis zum 15. Dezember 2016 oder früher gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="42bd4-123">Those posted on December 15 2016 or earlier.</span></span>|
|<span data-ttu-id="42bd4-124">Entweder/oder</span><span class="sxs-lookup"><span data-stu-id="42bd4-124">Either/or</span></span>|<span data-ttu-id="42bd4-125">12 15 16&#124;12 16 16</span><span class="sxs-lookup"><span data-stu-id="42bd4-125">12 15 16&#124;12 16 16</span></span>|<span data-ttu-id="42bd4-126">Entweder am 15. Dezember oder am 16. Dezember 2016 gebucht.</span><span class="sxs-lookup"><span data-stu-id="42bd4-126">Those posted on either December 15 or December 16 2016.</span></span> <span data-ttu-id="42bd4-127">Falls es Posten gibt, die an einem der beiden Tage gebucht wurden, werden diese angezeigt.</span><span class="sxs-lookup"><span data-stu-id="42bd4-127">If there are entries posted on both days, they will all be displayed.</span></span>|

<span data-ttu-id="42bd4-128">Sie können auch die verschiedenen Formattypen miteinander kombinieren.</span><span class="sxs-lookup"><span data-stu-id="42bd4-128">You can also combine the various format types.</span></span>

| <span data-ttu-id="42bd4-129">Beispiel</span><span class="sxs-lookup"><span data-stu-id="42bd4-129">Example</span></span> | <span data-ttu-id="42bd4-130">Enthaltene Posten</span><span class="sxs-lookup"><span data-stu-id="42bd4-130">Entries included</span></span> |
|---|---|
|<span data-ttu-id="42bd4-131">12 15 16&#124;12 01 16..05 31 17</span><span class="sxs-lookup"><span data-stu-id="42bd4-131">12 15 16&#124;12 01 16..05 31 17</span></span> | <span data-ttu-id="42bd4-132">Posten, die am 15. Dezember 2016 oder zwischen dem 01. Dezember 2016 und 31. Mai 2017 (einschließlich) gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="42bd4-132">Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017.</span></span> |
|<span data-ttu-id="42bd4-133">..12 14 16&#124;12 30 16..</span><span class="sxs-lookup"><span data-stu-id="42bd4-133">..12 14 16&#124;12 30 16..</span></span> | <span data-ttu-id="42bd4-134">Posten, die bis einschließlich zum 14. Dezember oder am bzw. nach dem 30. Dezember gebucht wurden. Mit diesem Filter können Sie alle Posten ausschließen, die zwischen den beiden angegebenen Tagen gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="42bd4-134">Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29.</span></span> |

<span data-ttu-id="42bd4-135">Beachten Sie, dass wir das US-Datumsformat MMDDYY hier verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="42bd4-135">Note that we have used the US date format MMDDYY here.</span></span> <span data-ttu-id="42bd4-136">[!INCLUDE[d365fin](includes/d365fin_md.md)] wird verfügbar in anderen Märkten, Sie haben die Möglichkeit, die Formaten zu verwenden, die möchten.</span><span class="sxs-lookup"><span data-stu-id="42bd4-136">As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.</span></span>

## <a name="see-also"></a><span data-ttu-id="42bd4-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42bd4-137">See Also</span></span>
<span data-ttu-id="42bd4-138">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="42bd4-138">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="42bd4-139">Eingeben von Kriterien in Filtern</span><span class="sxs-lookup"><span data-stu-id="42bd4-139">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  
[<span data-ttu-id="42bd4-140">Allgemeine Geschäftsfunktionen</span><span class="sxs-lookup"><span data-stu-id="42bd4-140">General Business Functionality</span></span>](ui-across-business-areas.md)

