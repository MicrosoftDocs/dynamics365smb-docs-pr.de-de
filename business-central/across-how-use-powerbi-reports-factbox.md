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
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: a600b24e16172134d4f8e78cf47efa4e262cac09
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777516"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prod_short"></a><span data-ttu-id="5eb27-103">Erstellen von Power BI-Berichten zum Anzeigen von Listendaten in [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="5eb27-103">Creating Power BI Reports for Displaying List Data in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

[!INCLUDE[prod_long](includes/prod_long.md)] <span data-ttu-id="5eb27-104">umfasst ein Power BI-Infobox-Steuerelement auf mehreren Schlüssellistenseiten.</span><span class="sxs-lookup"><span data-stu-id="5eb27-104">includes a Power BI FactBox control element on many key list pages.</span></span> <span data-ttu-id="5eb27-105">Der Zweck dieser Infobox ist die Anzeige von Power BI-Berichten, die sich auf Datensätze in den Listen beziehen und zusätzlichen Einblick in die Daten bieten.</span><span class="sxs-lookup"><span data-stu-id="5eb27-105">The purpose of this FactBox is to display Power BI reports that are related to records in the lists, providing extra insight into the data.</span></span> <span data-ttu-id="5eb27-106">Die Idee ist, dass während Sie sich zwischen den Zeilen in der Liste bewegen, wird der Bericht für den Eintrag gefiltert und aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5eb27-106">The idea is that as you move between rows in the list, the report is updated and filtered for the selected entry.</span></span>

[!INCLUDE[prod_long](includes/prod_long.md)] <span data-ttu-id="5eb27-107">kommt mit einigen dieser Berichte.</span><span class="sxs-lookup"><span data-stu-id="5eb27-107">comes ready with some of these reports.</span></span> <span data-ttu-id="5eb27-108">Sie können auch eigene benutzerdefinierte Berichte erstellen, die in dieser Infobox angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5eb27-108">You can also create your own custom reports that display in this FactBox.</span></span> <span data-ttu-id="5eb27-109">Das Erstellen dieser Berichte ähnelt anderen Berichten.</span><span class="sxs-lookup"><span data-stu-id="5eb27-109">Creating these reports is similar to other reports.</span></span> <span data-ttu-id="5eb27-110">Es gibt jedoch einige Entwurfsregeln, die Sie befolgen müssen, um sicherzustellen, dass die Berichte wie erwartet angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5eb27-110">But there are a few design rules you'll have to follow to make sure the reports display as expected.</span></span> <span data-ttu-id="5eb27-111">Diese Regeln werden in diesem Artikel erläutert.</span><span class="sxs-lookup"><span data-stu-id="5eb27-111">These rules are explained in this article.</span></span>

> [!NOTE]
> <span data-ttu-id="5eb27-112">Allgemeine Informationen zum Erstellen und Veröffentlichen von Power BI-Berichten für Business Central finden Sie unter [Power BI-Berichte zum Anzeigen erstellen [!INCLUDE [prod_long](includes/prod_long.md)]-Daten](across-how-use-financials-data-source-powerbi.md).</span><span class="sxs-lookup"><span data-stu-id="5eb27-112">For general information about creating and publishing Power BI reports for Business Central, see [Building Power BI Reports to Display [!INCLUDE [prod_long](includes/prod_long.md)] Data](across-how-use-financials-data-source-powerbi.md).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="5eb27-113">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="5eb27-113">Prerequisites</span></span>

- <span data-ttu-id="5eb27-114">Ein Power BI-Konto.</span><span class="sxs-lookup"><span data-stu-id="5eb27-114">A Power BI account.</span></span>
- <span data-ttu-id="5eb27-115">Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="5eb27-115">Power BI Desktop.</span></span>

<!-- 
For more information about getting started, see [Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md).-->

## <a name="create-a-report-for-a-list-page"></a><span data-ttu-id="5eb27-116">Einen Bericht für eine Listenseite erstellen</span><span class="sxs-lookup"><span data-stu-id="5eb27-116">Create a report for a list page</span></span>

1. <span data-ttu-id="5eb27-117">Starten Sie Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="5eb27-117">Start Power BI Desktop.</span></span>
2. <span data-ttu-id="5eb27-118">Wählen Sie **Daten abrufen** aus, und beginnen Sie mit der Auswahl der Datenquelle für den Bericht.</span><span class="sxs-lookup"><span data-stu-id="5eb27-118">Select **Get Data**, and start choosing the data source for the report.</span></span>

    <span data-ttu-id="5eb27-119">In diesem Schritt geben Sie die Business Central-Listenseiten an, die die gewünschten Daten im Bericht enthalten.</span><span class="sxs-lookup"><span data-stu-id="5eb27-119">In this step, you specify the Business Central list pages that contain the data that you want in the report.</span></span> <span data-ttu-id="5eb27-120">Wenn Sie beispielsweise einen Bericht für die Verkaufsübersicht erstellen möchten, stellen Sie sicher, dass der Datensatz Informationen enthält, die mit Verkäufen verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="5eb27-120">For example, to create a report for the Sales List, ensure the data set contains information related to sales.</span></span>

    <span data-ttu-id="5eb27-121">Weitere Informationen finden Sie in den Anweisungen [[!INCLUDE[prod_short](includes/prod_short.md)] als Datenquelle in Power BI Desktop hinzufügen](across-how-use-financials-data-source-powerbi.md#getdata).</span><span class="sxs-lookup"><span data-stu-id="5eb27-121">For more information, follow the instructions [Add [!INCLUDE[prod_short](includes/prod_short.md)] as a data source in Power BI Desktop](across-how-use-financials-data-source-powerbi.md#getdata).</span></span>

3. <span data-ttu-id="5eb27-122">Definieren Sie den Berichtsfilter.</span><span class="sxs-lookup"><span data-stu-id="5eb27-122">Set the report filter.</span></span>

    <span data-ttu-id="5eb27-123">Um die Daten für den ausgewählten Datensatz in der Liste zu aktualisieren, fügen Sie dem Bericht einen Filter hinzu.</span><span class="sxs-lookup"><span data-stu-id="5eb27-123">To make the data update to the selected record in the list, you add a filter to the report.</span></span> <span data-ttu-id="5eb27-124">Der Filter muss ein Feld der Datenquelle enthalten, mit dem jeder Datensatz in der Liste eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="5eb27-124">The filter must include a field of the data source that's used to uniquely identify each record in the list.</span></span> <span data-ttu-id="5eb27-125">In Bezug auf Entwickler ist dieses Feld der *Primärschlüssel*.</span><span class="sxs-lookup"><span data-stu-id="5eb27-125">In developer terms, this field is the *primary key*.</span></span> <span data-ttu-id="5eb27-126">In den meisten Fällen ist der Primärschlüssel für eine Liste **Nr.**</span><span class="sxs-lookup"><span data-stu-id="5eb27-126">In most cases, the primary key for a list is the **No.**</span></span> <span data-ttu-id="5eb27-127">Feld eingetragen.</span><span class="sxs-lookup"><span data-stu-id="5eb27-127">field.</span></span>

    <span data-ttu-id="5eb27-128">Führen Sie die folgenden Schritte aus, um den Filter einzustellen:</span><span class="sxs-lookup"><span data-stu-id="5eb27-128">To set the filter, do the following steps:</span></span>

    1. <span data-ttu-id="5eb27-129">Wählen Sie unter **Filter** das Primärschlüsselfeld aus der Liste der verfügbaren Felder aus.</span><span class="sxs-lookup"><span data-stu-id="5eb27-129">In the **Filters**, select the primary key field from the list of available fields.</span></span>
    2. <span data-ttu-id="5eb27-130">Ziehen Sie den Bereich **Filter** und legen Sie ihn in der Box **Filter auf allen Seiten** ab.</span><span class="sxs-lookup"><span data-stu-id="5eb27-130">Drag the field to **Filters** pane and drop it in the **Filters on all pages** box.</span></span>
    3. <span data-ttu-id="5eb27-131">Stellen Sie den **Filtertyp** auf **Grundfilterung**.</span><span class="sxs-lookup"><span data-stu-id="5eb27-131">Set the **Filter type** to **Basic filtering**.</span></span> <span data-ttu-id="5eb27-132">Es darf sich nicht um einen Seiten-, visuellen oder erweiterten Filter handeln.</span><span class="sxs-lookup"><span data-stu-id="5eb27-132">It can't be page, visual, or advanced filter.</span></span>

    ![Den Berichtfilter für den Verkaufsrechnungs-Tätigkeitsbericht festlegen](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)
4. <span data-ttu-id="5eb27-134">Entwerfen Sie den Berichtslayout.</span><span class="sxs-lookup"><span data-stu-id="5eb27-134">Design the report layout.</span></span>

    <span data-ttu-id="5eb27-135">Erstellen Sie das Layout, indem Sie Felder ziehen und Visualisierungen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5eb27-135">Create the layout by dragging fields and adding visualizations.</span></span> <span data-ttu-id="5eb27-136">Weitere Informationen finden Sie unter [Mit der Berichtsansicht in Power BI Desktop arbeiten](/power-bi/create-reports/desktop-report-view) in der Power BI-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="5eb27-136">For more information, see, [Work with Report view in Power BI Desktop](/power-bi/create-reports/desktop-report-view) in the Power BI documentation.</span></span>

5. <span data-ttu-id="5eb27-137">In den nächsten Abschnitten erfahren Sie, wie Sie die Größe des Berichts ändern und mehrere Seiten verwenden.</span><span class="sxs-lookup"><span data-stu-id="5eb27-137">See the next sections about sizing the report and using multiple pages.</span></span>

6. <span data-ttu-id="5eb27-138">Speichern und benennen Sie den Bericht.</span><span class="sxs-lookup"><span data-stu-id="5eb27-138">Save and name the report.</span></span>

    <span data-ttu-id="5eb27-139">Es ist wichtig, dem Bericht einen Namen zu geben, der den Namen der dem Bericht zugeordneten Listenseite enthält.</span><span class="sxs-lookup"><span data-stu-id="5eb27-139">It's important to give the report a name that contains the name of the list page associated with the report.</span></span> <span data-ttu-id="5eb27-140">Wenn es sich beispielsweise um einen Bericht für die Listenseite **Artikel** handelt, sollte der Name das Wort *Artikel* enthalten.</span><span class="sxs-lookup"><span data-stu-id="5eb27-140">For example, if the report is for the **Items** list page, include the word *items* somewhere in the name.</span></span>  

    <span data-ttu-id="5eb27-141">Diese Namenskonvention ist nicht zwingend erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5eb27-141">This naming convention isn't a requirement.</span></span> <span data-ttu-id="5eb27-142">Sie beschleunigt jedoch das Auswählen von Berichten in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="5eb27-142">However, it makes selecting reports in [!INCLUDE[prod_short](includes/prod_short.md)] quicker.</span></span> <span data-ttu-id="5eb27-143">Wenn die Seite für die Berichtsauswahls von einer Listenseite aus geöffnet wird, wird sie automatisch anhand des Seitennamens gefiltert.</span><span class="sxs-lookup"><span data-stu-id="5eb27-143">When the report selection page opens from a list page, it's automatically filtered based on the page name.</span></span> <span data-ttu-id="5eb27-144">Diese Filterung wird durchgeführt, um die Anzahl der angezeigten Berichte zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="5eb27-144">This filtering is done to limit the reports that are displayed.</span></span> <span data-ttu-id="5eb27-145">Benutzer können den Filter entfernen, um eine vollständige Liste der in Power BI verfügbaren Berichte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5eb27-145">Users can clear the filter to get a full list of reports available in Power BI.</span></span>

7. <span data-ttu-id="5eb27-146">Wenn Sie fertig sind, veröffentlichen Sie den Bericht wie gewohnt.</span><span class="sxs-lookup"><span data-stu-id="5eb27-146">When you're done, publish the report as usual.</span></span>

    <span data-ttu-id="5eb27-147">Weitere Informationen finden Sie unter [Veröffentlichen eines Berichts](across-how-use-financials-data-source-powerbi.md#publish-reports).</span><span class="sxs-lookup"><span data-stu-id="5eb27-147">For more information, see [Publishing a Report](across-how-use-financials-data-source-powerbi.md#publish-reports).</span></span>

8. <span data-ttu-id="5eb27-148">Testen Sie den Bericht.</span><span class="sxs-lookup"><span data-stu-id="5eb27-148">Test the report.</span></span>

    <span data-ttu-id="5eb27-149">Sobald die Berichte in Ihrem Arbeitsbereich veröffentlicht wurden, sollten sie im Internet über die Power BI-Infobox auf der Listenseite in [!INCLUDE[prod_short](includes/prod_short.md)] verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="5eb27-149">Once the reports been published to your workspace, it should be available from the Power BI FactBox on the list page in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

    <span data-ttu-id="5eb27-150">Führen Sie die folgenden Schritte aus, um es zu testen.</span><span class="sxs-lookup"><span data-stu-id="5eb27-150">To test it, do the following steps.</span></span>

    1. <span data-ttu-id="5eb27-151">Öffnen Sie [!INCLUDE[prod_short](includes/prod_short.md)], und gehen Sie zur Listenseite.</span><span class="sxs-lookup"><span data-stu-id="5eb27-151">Open [!INCLUDE[prod_short](includes/prod_short.md)] and go to the list page.</span></span>
    2. <span data-ttu-id="5eb27-152">Wenn Sie die Power BI-Infobox nicht sehen, wechseln Sie zur Aktionsleiste und wählen Sie **Aktionen** > **Anzeigen** > **Power BI-Berichte anzeigen/ausblenden** aus.</span><span class="sxs-lookup"><span data-stu-id="5eb27-152">If you don't see the Power BI FactBox, go the action bar, then select **Actions** > **Display** > **Show/Hide Power BI Reports**.</span></span>
    3. <span data-ttu-id="5eb27-153">Wählen Sie in der Power BI-Infobox **Berichte auswählen**, dann das Feld **Aktivieren** für den Bericht und **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="5eb27-153">In the Power BI FactBox, select **Select Reports**, select the **Enable** box for the report, then select **OK**.</span></span>

    <span data-ttu-id="5eb27-154">Bei korrekter Gestaltung wird der Bericht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5eb27-154">If designed correctly, the report displays.</span></span>  

## <a name="set-the-report-size-and-color"></a><span data-ttu-id="5eb27-155">Berichtsgröße und ‑farbe festlegen</span><span class="sxs-lookup"><span data-stu-id="5eb27-155">Set the report size and color</span></span>

<span data-ttu-id="5eb27-156">Die Größe des Berichts muss auf 325 Pixel auf 310 Pixel festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5eb27-156">The size of the report must be set to 325 pixels by 310 pixels.</span></span> <span data-ttu-id="5eb27-157">Diese Größe gibt die richtige Skalierung des Berichts im verfügbaren Platz des Power BI-Infoboxreglers in [!INCLUDE[prod_short](includes/prod_short.md)] an.</span><span class="sxs-lookup"><span data-stu-id="5eb27-157">This size provides the proper scaling of the report in the available space of the Power BI FactBox control in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="5eb27-158">Um die Größe des Berichts zu definieren, den Fokus außerhalb des Berichts im Berichtslayoutbereich zu platzieren und um das Farbenrollensymbol zu wählen.</span><span class="sxs-lookup"><span data-stu-id="5eb27-158">To define the size of the report, place focus outside of the report layout area, and then choose the paint roller icon.</span></span>

![Den Berichtfilter für die Breite und die Höhe des Verkaufsrechnungs-Tätigkeitsbericht festlegen](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

<span data-ttu-id="5eb27-160">Sie können die Breite und die Tiefe des Berichts ändern, indem Sie im Feld **Benutzerdefiniert** **Art** auswählen.</span><span class="sxs-lookup"><span data-stu-id="5eb27-160">You can change the width and height of the report by choosing **Custom** in the **Type** field.</span></span>

<span data-ttu-id="5eb27-161">Wenn Sie möchten, dass sich der Hintergrund des Bericht an die Hintergrundfarbe des Power BI-Infoboxreglers anpasst, legen Sie die Berichtshintergrundfarbe auf *#FFFFFF* (weiß) fest.</span><span class="sxs-lookup"><span data-stu-id="5eb27-161">If you want the background of the report to blend with the background color of the Power BI FactBox control, set report background color to *#FFFFFF* (white).</span></span> 

> [!TIP]
> <span data-ttu-id="5eb27-162">Verwenden Sie die [!INCLUDE [prod_short](includes/prod_short.md)]-Themendatei zum Erstellen von Berichten mit dem gleichen Farbstil wie die [!INCLUDE [prod_short](includes/prod_short.md)]-Apps.</span><span class="sxs-lookup"><span data-stu-id="5eb27-162">Use the [!INCLUDE [prod_short](includes/prod_short.md)] theme file to build reports with the same color styling as the [!INCLUDE [prod_short](includes/prod_short.md)] apps.</span></span> <span data-ttu-id="5eb27-163">Weitere Informationen finden Sie unter [[!INCLUDE [prod_short](includes/prod_short.md)]-Berichtsthema verwenden](across-how-use-financials-data-source-powerbi.md#theme).</span><span class="sxs-lookup"><span data-stu-id="5eb27-163">For more information, see [Using the [!INCLUDE [prod_short](includes/prod_short.md)] report theme](across-how-use-financials-data-source-powerbi.md#theme).</span></span>

## <a name="reports-with-multiple-pages"></a><span data-ttu-id="5eb27-164">Berichte mit mehrere Seiten</span><span class="sxs-lookup"><span data-stu-id="5eb27-164">Reports with multiple pages</span></span>

<span data-ttu-id="5eb27-165">Mit Power BI können Sie einen einzelnen Bericht mit mehreren Seiten erstellen.</span><span class="sxs-lookup"><span data-stu-id="5eb27-165">With Power BI, you can create a single report with multiple pages.</span></span> <span data-ttu-id="5eb27-166">Für Berichte, die mit Listenseiten angezeigt werden, empfehlen wir jedoch nicht, dass sie mehr als eine Seite umfassen.</span><span class="sxs-lookup"><span data-stu-id="5eb27-166">However, for reports that will display with list pages, we don't recommend that they have more than one page.</span></span> <span data-ttu-id="5eb27-167">Die Power BI-Infobox zeigt nur die erste Seite Ihres Berichts an.</span><span class="sxs-lookup"><span data-stu-id="5eb27-167">The Power BI FactBox will only show the first page of your report.</span></span>

## <a name="fixing-problems"></a><span data-ttu-id="5eb27-168">Probleme beheben</span><span class="sxs-lookup"><span data-stu-id="5eb27-168">Fixing problems</span></span>

<span data-ttu-id="5eb27-169">Dieser Abschnitt enthält Anweisungen zum Beheben von Problemen, auf die Sie möglicherweise stoßen, wenn Sie versuchen, einen Power BI-Bericht für eine Listenseite in [!INCLUDE[prod_short](includes/prod_short.md)] anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5eb27-169">This section provides instructions about how to fix problems that you might run into when trying to view a Power BI report for a list page in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

### <a name="you-cant-see-the-power-bi-factbox-on-a-list-page"></a><span data-ttu-id="5eb27-170">Sie können die Power BI-Infobox auf einer Listenseite nicht sehen</span><span class="sxs-lookup"><span data-stu-id="5eb27-170">You can't see the Power BI FactBox on a list page</span></span>

<span data-ttu-id="5eb27-171">Standardmäßig ist die Power BI-Infobox nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="5eb27-171">By default, the Power BI FactBox is hidden from view.</span></span> <span data-ttu-id="5eb27-172">Um die Infobox auf einer Seite anzuzeigen, wählen Sie in der Aktionsleiste **Aktionen** > **Anzeigen** > **Power BI-Berichte anzeigen/ausblenden** aus.</span><span class="sxs-lookup"><span data-stu-id="5eb27-172">To show the FactBox on a page, from the action bar, select **Actions** > **Display** > **Show/Hide Power BI Reports**.</span></span>

### <a name="you-cant-see-the-report-in-the-select-report-pane"></a><span data-ttu-id="5eb27-173">Sie können den Bericht im Abschnitt „Bericht auswählen“ nicht sehen</span><span class="sxs-lookup"><span data-stu-id="5eb27-173">You can't see the report in the Select Report pane</span></span>

<span data-ttu-id="5eb27-174">Vermutlich enthält der Name des Berichts nicht den Namen der Listenseite, die angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5eb27-174">It's probably because the report's name doesn't contain the name of the list page that's being shown.</span></span> <span data-ttu-id="5eb27-175">Löschen Sie den Filter, um die vollständige Liste der verfügbaren Power BI-Berichte anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5eb27-175">Clear the filter to get a full list of Power BI reports available.</span></span>  

### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a><span data-ttu-id="5eb27-176">Der Bericht wird zwar geladen, ist jedoch leer, wird nicht gefiltert oder falsch gefiltert</span><span class="sxs-lookup"><span data-stu-id="5eb27-176">Report is loaded but blank, not filtered, or filtered incorrectly</span></span>

<span data-ttu-id="5eb27-177">Vergewissern Sie sich, dass der Berichtsfilter den richtigen Primärschlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="5eb27-177">Verify that the report filter contains the right primary key.</span></span> <span data-ttu-id="5eb27-178">In den meisten Fällen handelt es sich hierbei um das Feld **Nr.**.</span><span class="sxs-lookup"><span data-stu-id="5eb27-178">In most cases, this field is the **No.**</span></span> <span data-ttu-id="5eb27-179">In der Tabelle **Sachposten** beispielsweise müssen Sie jedoch das Feld **Postennr.** verwenden.</span><span class="sxs-lookup"><span data-stu-id="5eb27-179">field, but in the **G/L Entry** table, for example, you must use the **Entry No.** field.</span></span>

### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a><span data-ttu-id="5eb27-180">Der Bericht wird zwar geladen, zeigt jedoch nicht die erwartete Seite an</span><span class="sxs-lookup"><span data-stu-id="5eb27-180">Report is loaded, but it shows a page you didn't expect</span></span>

<span data-ttu-id="5eb27-181">Vergewissern Sie sich, dass die Seite, die angezeigt werden soll, die erste Seite im Bericht ist.</span><span class="sxs-lookup"><span data-stu-id="5eb27-181">Verify that the page you want displayed is the first page in your report.</span></span>  

### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a><span data-ttu-id="5eb27-182">Der Bericht wird mit einem unerwünschten grauen Rand angezeigt, ist zu klein oder zu umfangreich</span><span class="sxs-lookup"><span data-stu-id="5eb27-182">Report appears with an unwanted gray boarder, or it's too small or too large</span></span>

<span data-ttu-id="5eb27-183">Vergewissern Sie sich, dass die Berichtsgröße auf 325 Pixel x 310 Pixel festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="5eb27-183">Verify that the report size is set to 325 pixels x 310 pixels.</span></span> <span data-ttu-id="5eb27-184">Speichern Sie den Bericht, und aktualisieren Sie anschließend die Seite.</span><span class="sxs-lookup"><span data-stu-id="5eb27-184">Save the report, and then refresh the list page.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="5eb27-185">Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="5eb27-185">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="5eb27-186">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5eb27-186">See Also</span></span>

[<span data-ttu-id="5eb27-187">Aktivieren Sie Ihre Geschäftsdaten für Power BI</span><span class="sxs-lookup"><span data-stu-id="5eb27-187">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
<span data-ttu-id="5eb27-188">[Verwenden von [!INCLUDE[prod_short](includes/prod_short.md)] als Power BI-Datenquelle](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="5eb27-188">[Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
[<span data-ttu-id="5eb27-189">Vorbereitung für die Geschäftstätigkeit</span><span class="sxs-lookup"><span data-stu-id="5eb27-189">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
<span data-ttu-id="5eb27-190">[Einrichten [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="5eb27-190">[Setting Up [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span></span>  
[<span data-ttu-id="5eb27-191">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5eb27-191">Finance</span></span>](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]