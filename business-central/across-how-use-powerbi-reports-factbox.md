---
title: Anzeigen benutzerdefinierter Power BI-Berichte für Business Central-Daten | Microsoft Docs
description: Sie können Power BI-Berichte verwenden, um einen zusätzlichen Einblick in Daten in Listen zu gewinnen.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 6c818940357ed21a994e7553517989a0c16accec
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379273"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prod_short"></a><span data-ttu-id="fb9bb-103">Erstellen von Power BI-Berichten zum Anzeigen von Listendaten in [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="fb9bb-103">Creating Power BI Reports for Displaying List Data in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

[!INCLUDE[prod_long](includes/prod_long.md)] <span data-ttu-id="fb9bb-104">enthält einen Infoboxregler in mehreren Schlüssellistenseiten, der zusätzliche Einblicke in die Daten in dieser Liste bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-104">includes a FactBox control element on a number of key list pages that provide additional insight into the data in the list.</span></span> <span data-ttu-id="fb9bb-105">Während Sie sich zwischen den Zeilen in der Liste bewegen, wird der Bericht für den Eintrag gefiltert und aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-105">As you move between rows in the list, the report is updated and filtered for the selected entry.</span></span> <span data-ttu-id="fb9bb-106">Sie können benutzerdefinierte Berichte erstellen, die in diesem Steuerelement angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-106">You can create custom reports to display in this control.</span></span> <span data-ttu-id="fb9bb-107">Dabei sind jedoch einige Regeln zu beachten, um sicherzustellen, dass die Berichte wie erwartet funktionieren.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-107">However, there are a few rules to follow to ensure that reports work as expected.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="fb9bb-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="fb9bb-108">Prerequisites</span></span>

- <span data-ttu-id="fb9bb-109">Ein Power BI-Konto.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-109">A Power BI account.</span></span>
- <span data-ttu-id="fb9bb-110">Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-110">Power BI Desktop.</span></span>

<span data-ttu-id="fb9bb-111">Weitere Informationen zu den ersten Schritten finden Sie unter [[!INCLUDE[prod_short](includes/prod_short.md)] als Power BI-Datenquelle nutzen](across-how-use-financials-data-source-powerbi.md).</span><span class="sxs-lookup"><span data-stu-id="fb9bb-111">For more information about getting started, see [Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md).</span></span>

## <a name="defining-the-report-data-set"></a><span data-ttu-id="fb9bb-112">Definieren des Berichtsdatensatzes</span><span class="sxs-lookup"><span data-stu-id="fb9bb-112">Defining the report data set</span></span>

<span data-ttu-id="fb9bb-113">Geben Sie die Datenquelle an, die die Daten enthält, die sich auf die Liste beziehen.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-113">Specify the data source that contains the data related to the list.</span></span> <span data-ttu-id="fb9bb-114">Wenn Sie beispielsweise einen Bericht für die Verkaufsübersicht erstellen möchten, stellen Sie sicher, dass der Datensatz Informationen enthält, die mit Verkäufen verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-114">For example, to create a report for the Sales List, ensure the data set contains information related to sales.</span></span>  

## <a name="defining-the-report-filter"></a><span data-ttu-id="fb9bb-115">Definieren des Berichtsfilters</span><span class="sxs-lookup"><span data-stu-id="fb9bb-115">Defining the report filter</span></span>

<span data-ttu-id="fb9bb-116">Um die Daten für den ausgewählten Datensatz in der Liste zu aktualisieren, fügen Sie dem Bericht einen Filter hinzu.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-116">To make the data update to the selected record in the list, you add a filter to the report.</span></span> <span data-ttu-id="fb9bb-117">Der Filter muss ein Feld der Datenquelle enthalten, die als *Primärschlüssel* verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-117">The filter must include a field of the data source that's used as the *primary key*.</span></span> <span data-ttu-id="fb9bb-118">In den meisten Fällen ist der Primärschlüssel für eine Liste **Nr.**</span><span class="sxs-lookup"><span data-stu-id="fb9bb-118">In most cases, the primary key for a list is the **No.**</span></span> <span data-ttu-id="fb9bb-119">Feld eingetragen.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-119">field.</span></span>

<span data-ttu-id="fb9bb-120">Um einen Filter für den Bericht zu definieren, wählen Sie den Primärschlüssel aus der Liste der verfügbaren Felder und ziehen dann das Feld in den Abschnitt **Berichts-Filter**.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-120">To define a filter for the report, select the primary key from the list of available fields, and then drag and drop that field into the **Report Filter** section.</span></span> <span data-ttu-id="fb9bb-121">Der Filter muss ein grundlegender Berichtsfilter sein, der für alle Seiten definiert ist.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-121">The filter must be a basic report filter that's defined for all pages.</span></span> <span data-ttu-id="fb9bb-122">Es darf sich nicht um einen Seiten-, visuellen oder erweiterten Filter handeln.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-122">It can't be page, visual, or advanced filter.</span></span>

![Den Berichtfilter für den Verkaufsrechnungs-Tätigkeitsbericht festlegen](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)

## <a name="setting-the-report-size-and-color"></a><span data-ttu-id="fb9bb-124">Festlegen von Berichtsgröße und -farbe</span><span class="sxs-lookup"><span data-stu-id="fb9bb-124">Setting the report size and color</span></span>

<span data-ttu-id="fb9bb-125">Die Größe des Berichts muss auf 325 Pixel auf 310 Pixel festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-125">The size of the report must be set to 325 pixels by 310 pixels.</span></span> <span data-ttu-id="fb9bb-126">Diese Größe gibt die richtige Skalierung des Berichts im verfügbaren Platz des Power BI-Infoboxreglers in [!INCLUDE[prod_short](includes/prod_short.md)] an.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-126">This size provides the proper scaling of the report in the available space of the Power BI FactBox control in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="fb9bb-127">Um die Größe des Berichts zu definieren, den Fokus außerhalb des Berichts im Berichtslayoutbereich zu platzieren und um das Farbenrollensymbol zu wählen.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-127">To define the size of the report, place focus outside of the report layout area, and then choose the paint roller icon.</span></span>

![Den Berichtfilter für die Breite und die Höhe des Verkaufsrechnungs-Tätigkeitsbericht festlegen](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

<span data-ttu-id="fb9bb-129">Sie können die Breite und die Tiefe des Berichts ändern, indem Sie im Feld **Benutzerdefiniert** **Art** auswählen.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-129">You can change the width and height of the report by choosing **Custom** in the **Type** field.</span></span>

<span data-ttu-id="fb9bb-130">Wenn Sie möchten, dass sich der Hintergrund des Bericht an die Hintergrundfarbe des Power BI-Infoboxreglers anpasst, legen Sie die Berichtshintergrundfarbe auf *#FFFFFF* fest.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-130">If you want the background of the report to blend with the background color of the Power BI FactBox control, set report background color to *#FFFFFF*.</span></span> 

## <a name="using-reports-with-multiple-pages"></a><span data-ttu-id="fb9bb-131">Verwenden von Berichten mit mehreren Seiten</span><span class="sxs-lookup"><span data-stu-id="fb9bb-131">Using reports with multiple pages</span></span>

<span data-ttu-id="fb9bb-132">Mit Power BI können Sie einen einzelnen Bericht mit mehreren Seiten erstellen.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-132">With Power BI, you can create a single report with multiple pages.</span></span> <span data-ttu-id="fb9bb-133">Für Berichte, die mit Listenseiten angezeigt werden, empfehlen wir jedoch nicht, dass sie mehr als eine Seite umfassen.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-133">However, for reports that will display with list pages, we don't recommend that they have more than one page.</span></span> <span data-ttu-id="fb9bb-134">Die Power BI-Infobox zeigt nur die erste Seite Ihres Berichts an.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-134">The Power BI FactBox will only show the first page of your report.</span></span>

## <a name="naming-the-report"></a><span data-ttu-id="fb9bb-135">Benennen des Berichts</span><span class="sxs-lookup"><span data-stu-id="fb9bb-135">Naming the report</span></span>

<span data-ttu-id="fb9bb-136">Geben Sie dem Bericht einen Namen, der den Namen der dem Bericht zugeordneten Listenseite enthält.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-136">Give the report a name that contains the name of the list page associated with the report.</span></span> <span data-ttu-id="fb9bb-137">Wenn es sich beispielsweise um einen Bericht für die Listenseite **Verkäufer** handelt, sollte der Name das Wort *Verkäufer* enthalten.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-137">For example, if the report is for the **Vendor** list page, include the word *vendor* somewhere in the name.</span></span>  

<span data-ttu-id="fb9bb-138">Diese Namenskonvention ist nicht zwingend erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-138">This naming convention isn't a requirement.</span></span> <span data-ttu-id="fb9bb-139">Sie beschleunigt jedoch das Auswählen von Berichten in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="fb9bb-139">However, it makes selecting reports in [!INCLUDE[prod_short](includes/prod_short.md)] quicker.</span></span> <span data-ttu-id="fb9bb-140">Wenn die Seite für die Berichtsauswahls von einer Listenseite aus geöffnet wird, wird sie automatisch anhand des Seitennamens gefiltert.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-140">When the report selection page opens from a list page, it's automatically filtered based on the page name.</span></span> <span data-ttu-id="fb9bb-141">Diese Filterung wird durchgeführt, um die Anzahl der angezeigten Berichte zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-141">This filtering is done to limit the reports that are displayed.</span></span> <span data-ttu-id="fb9bb-142">Benutzer können den Filter entfernen, um eine vollständige Liste der in Power BI verfügbaren Berichte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-142">Users can clear the filter to get a full list of reports available in Power BI.</span></span>  

## <a name="fixing-problems"></a><span data-ttu-id="fb9bb-143">Probleme beheben</span><span class="sxs-lookup"><span data-stu-id="fb9bb-143">Fixing problems</span></span>

<span data-ttu-id="fb9bb-144">Dieser Abschnitt bietet eine Problemumgehung für die gängigsten Probleme, die beim Erstellen des Power BI-Berichts auftreten können.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-144">This section provides a workaround for the most typical problems that can occur when you create the Power BI report.</span></span>  

#### <a name="you-cant-see-a-report-on-the-select-report-page"></a><span data-ttu-id="fb9bb-145">Ein Bericht ist auf der Seite „Bericht auswählen“ nicht sichtbar</span><span class="sxs-lookup"><span data-stu-id="fb9bb-145">You can't see a report on the Select Report page</span></span>

<span data-ttu-id="fb9bb-146">Vermutlich enthält der Name des Berichts nicht den Namen der Listenseite.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-146">It's probably because the report's name doesn't contain the name of the list page.</span></span> <span data-ttu-id="fb9bb-147">Löschen Sie den Filter, um die vollständige Liste der verfügbaren Power BI-Berichte anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-147">Clear the filter to get a full list of Power BI reports available.</span></span>  

#### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a><span data-ttu-id="fb9bb-148">Der Bericht wird zwar geladen, ist jedoch leer, wird nicht gefiltert oder falsch gefiltert</span><span class="sxs-lookup"><span data-stu-id="fb9bb-148">Report is loaded but blank, not filtered or filtered incorrectly</span></span>

<span data-ttu-id="fb9bb-149">Vergewissern Sie sich, dass der Berichtsfilter den richtigen Primärschlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-149">Verify that the report filter contains the right primary key.</span></span> <span data-ttu-id="fb9bb-150">In den meisten Fällen handelt es sich hierbei um das Feld **Nr.**.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-150">In most cases, this field is the **No.**</span></span> <span data-ttu-id="fb9bb-151">In der Tabelle **Sachposten** beispielsweise müssen Sie jedoch das Feld **Postennr.** verwenden.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-151">field, but in the **G/L Entry** table, for example, you must use the **Entry No.** field.</span></span>

#### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a><span data-ttu-id="fb9bb-152">Der Bericht wird zwar geladen, zeigt jedoch nicht die erwartete Seite an</span><span class="sxs-lookup"><span data-stu-id="fb9bb-152">Report is loaded, but it shows a page you didn't expect</span></span>

<span data-ttu-id="fb9bb-153">Vergewissern Sie sich, dass die Seite, die angezeigt werden soll, die erste Seite im Bericht ist.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-153">Verify that the page you want displayed is the first page in your report.</span></span>  

#### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a><span data-ttu-id="fb9bb-154">Der Bericht wird mit einem unerwünschten grauen Rand angezeigt, ist zu klein oder zu umfangreich</span><span class="sxs-lookup"><span data-stu-id="fb9bb-154">Report appears with an unwanted gray boarder, or it's too small or too large</span></span>

<span data-ttu-id="fb9bb-155">Vergewissern Sie sich, dass die Berichtsgröße auf 325 Pixel x 310 Pixel festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-155">Verify that the report size is set to 325 pixels x 310 pixels.</span></span> <span data-ttu-id="fb9bb-156">Speichern Sie den Bericht, und aktualisieren Sie anschließend die Seite.</span><span class="sxs-lookup"><span data-stu-id="fb9bb-156">Save the report, and then refresh the list page.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="fb9bb-157">Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="fb9bb-157">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="fb9bb-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb9bb-158">See Also</span></span>

[<span data-ttu-id="fb9bb-159">Aktivieren Sie Ihre Geschäftsdaten für Power BI</span><span class="sxs-lookup"><span data-stu-id="fb9bb-159">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
<span data-ttu-id="fb9bb-160">[Verwenden von [!INCLUDE[prod_short](includes/prod_short.md)] als Power BI-Datenquelle](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="fb9bb-160">[Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
[<span data-ttu-id="fb9bb-161">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="fb9bb-161">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="fb9bb-162">[Einrichten [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="fb9bb-162">[Setting Up [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span></span>  
[<span data-ttu-id="fb9bb-163">Finanzen</span><span class="sxs-lookup"><span data-stu-id="fb9bb-163">Finance</span></span>](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]