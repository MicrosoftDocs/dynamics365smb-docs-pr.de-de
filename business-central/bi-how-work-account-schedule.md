---
title: Finanzberichte mithilfe von Kontenschemata bauen
description: "Beschreibt, wie Filter verwendet werden, um unterschiedliche Ansichten und Berichte zum Analysieren von Finanzverhältnisleistungsdaten zu erstellen."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 04/16/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 7c346455a9e27d7274b116754f1d594484b95d67
ms.openlocfilehash: f9f5b3a25a24d4d10c80d048153e68030733bf9e
ms.contentlocale: de-de
ms.lasthandoff: 04/18/2018

---
# <a name="work-with-account-schedules"></a><span data-ttu-id="7fbb5-103">Arbeiten mit Kontenschemata</span><span class="sxs-lookup"><span data-stu-id="7fbb5-103">Work with Account Schedules</span></span>
<span data-ttu-id="7fbb5-104">Verwenden von Kontenplan, um die Einblicke in die Finanzdaten zu kommen, die in Ihrem Kontenplan gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-104">Use account schedules to get insight into the financial data stored in your chart of accounts.</span></span> <span data-ttu-id="7fbb5-105">Verwenden von Kontenschemata zum Analysieren der Werte auf Sachkonten oder zum Vergleichen von Sachposten mit Finanzbudgetposten.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-105">Account schedules analyze figures in G/L accounts, and compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="7fbb5-106">Die Ergebnisanzeige in den Diagrammen in Ihrem Rollencenter, wie beispielsweise der Cashflowplan.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-106">The results display in charts on your Role Center, such as the Cash Flow chart.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="7fbb5-107"> enthält mehrere Beispielkontenschemata, die Sie verwenden können , oder Sie können eigene Zeilen und Spalten einrichten, um die Werte anzugeben und zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-107"> provides a few sample account schedules that you can use right away, or you can set up your own rows and columns to specify the figures to compare.</span></span> <span data-ttu-id="7fbb5-108">So können beispielsweise Kontenschemata zur Berechnung von Gewinnmargen für Dimensionen wie beispielsweise Abteilungen oder Debitorengruppen erstellen.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-108">For example, you can create account schedules to calculate profit margins on dimensions like departments or customer groups.</span></span> <span data-ttu-id="7fbb5-109">Das bedeutet, dass Sie so viele maßgeschneiderte Finanzaufstellungen erstellen können, wie Sie möchten.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-109">You can create as many customized financial statements as you want.</span></span>  

<span data-ttu-id="7fbb5-110">Das Einrichten von Kontenschemata erfordert ein Verständnis für die Finanzdaten im Kontenplan.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-110">Setting up account schedules requires an understanding of the financial data in the chart of accounts.</span></span> <span data-ttu-id="7fbb5-111">Sie können beispielsweise die Sachposten als prozentualen Anteil der Budgetposten sehen.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-111">For example, you can view general ledger entries as percentages of budget entries.</span></span> <span data-ttu-id="7fbb5-112">Dazu ist es erforderlich, dass Budgets erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-112">This requires that budgets are created.</span></span> <span data-ttu-id="7fbb5-113">Weitere Informationen finden Sie unter [Sachkonto-Budgets erstellen](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="7fbb5-113">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

## <a name="account-categories-and-account-schedules"></a><span data-ttu-id="7fbb5-114">Kontengruppen und Kontenschemata</span><span class="sxs-lookup"><span data-stu-id="7fbb5-114">Account Categories and Account Schedules</span></span>
<span data-ttu-id="7fbb5-115">Sie können Kontengruppen dazu verwenden, das Layout Ihrer Finanzberichte zu ändern.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-115">You can use account categories to change the layout of your financial statements.</span></span> <span data-ttu-id="7fbb5-116">Wenn Sie Ihre Kontengruppen im Fenster **Sachkontokategorien** eingerichtet haben und die Aktion **Kontenschemata generieren** auswählen, werden die zugrunde liegenden Kontenschemata für die Kernfinanzberichte aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-116">After you set up your account categories in the **G/L Account Categories** window, and you choose the **Generate Account Schedules** action, the underlying account schedules for the core financial reports are updated.</span></span> <span data-ttu-id="7fbb5-117">Wenn Sie das nächste Mal einen dieser Berichte wie die Saldoabrechnung ausführen, werden neue Summen und Untereinträge basierend auf Ihren Änderungen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-117">The next time you run one of these reports, such as the balance statement, new totals and subentries are added, based on your changes.</span></span> <span data-ttu-id="7fbb5-118">Weitere Informationen finden Sie unter [Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="7fbb5-118">For more information, see [The General Ledger and the Chart of Accounts](finance-general-ledger.md).</span></span>  

## <a name="to-create-new-account-schedules"></a><span data-ttu-id="7fbb5-119">Neue Kontenschemata erstellen:</span><span class="sxs-lookup"><span data-stu-id="7fbb5-119">To create new account schedules</span></span>  
 <span data-ttu-id="7fbb5-120">Sie benutzen Kontenschemata zum Analysieren der Werte auf Sachkonten oder zum Vergleichen von Sachposten mit Finanzbudgetposten.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-120">You use account schedules to analyze figures in general ledger accounts or to compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="7fbb5-121">Sie können beispielsweise die Sachposten als prozentualen Anteil der Finanzbudgetposten sehen.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-121">For example, you can view the general ledger entries as percentages of the budget entries.</span></span>

1. <span data-ttu-id="7fbb5-122">Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Kontenplämne** ein und wählen den zugehörenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7fbb5-123">Wählen Sie im Fenster **Kontoschemaname** auf der Registerkarte **Neu** die Option Neu aus, um einen neuen Kontenschemanamen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-123">In the **Account Schedule Names** window, choose the **New** action to create a new account schedule name.</span></span>
3. <span data-ttu-id="7fbb5-124">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="7fbb5-125">Wählen Sie die **Kontenschema bearbeiten** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-125">Choose the **Edit Account Schedule** action.</span></span>
5. <span data-ttu-id="7fbb5-126">Füllen Sie die Felder im Fenster **Kontenschema** aus.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-126">In the **Account Schedule** window, fill in the fields as necessary.</span></span>  

    <span data-ttu-id="7fbb5-127">Nachdem Sie ein neues Kontenschema erstellt haben und neue Zeilen in Ihrem Kontenschema eingerichtet haben, müssen Sie die Spalten einrichten.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-127">When you have created a new account schedule and set up the rows, you must set up columns.</span></span> <span data-ttu-id="7fbb5-128">Sie können diese entweder manuell einrichten oder Ihrem Kontenschema ein vordefiniertes Spaltenlayout zuweisen.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-128">You can either set them up manually or assign a predefined column layout to your account schedule.</span></span>
6. <span data-ttu-id="7fbb5-129">Wählen Sie die **Spaltenlayouteinrichtung bearbeiten** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-129">Choose the **Edit Column Layout Setup** action.</span></span>
7. <span data-ttu-id="7fbb5-130">Füllen Sie die Felder im Fenster **Spaltenlayout** aus.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-130">In the **Column Layout** window, fill in the fields as necessary.</span></span>

> [!NOTE]  
>   <span data-ttu-id="7fbb5-131">Wurde dem Kontenschema kein Standardspaltenlayout zugeordnet, müssen Sie die Spalten manuell einrichten.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-131">If you did not assign a default column layout to the account schedule, you must set the columns up manually.</span></span>   

### <a name="to-create-a-column-that-calculates-percentages"></a><span data-ttu-id="7fbb5-132">Eine Spalte zur Berechnung von Prozentsätzen erstellen:</span><span class="sxs-lookup"><span data-stu-id="7fbb5-132">To create a column that calculates percentages</span></span>  
<span data-ttu-id="7fbb5-133">Manchmal möchten Sie möglicherweise eine Spalte in ein Kontenschema einfügen, in der Prozentsätze einer Summe berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-133">Sometimes you may want to include a column in an account schedule to calculate percentages of a total.</span></span> <span data-ttu-id="7fbb5-134">Wenn beispielsweise mehrere Zeilen vorhanden sind, in denen die Verkäufe nach Dimension aufgeschlüsselt sind, empfiehlt sich die Einrichtung einer Spalte, in der für jede Zeile der prozentuale Anteil an den Gesamtverkäufen angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-134">For example, if you have a number of rows that break down sales by dimension, you may want a column to indicate the percentage of total sales that each row represents.</span></span>

1. <span data-ttu-id="7fbb5-135">Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Kontenplämne** ein und wählen den zugehörenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-135">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="7fbb5-136">Wählen Sie im Fenster **Kontenschemanamen** ein Kontenschema aus.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-136">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="7fbb5-137">Klicken Sie auf der Registerkarte **Kontoschema bearbeiten** in der Gruppe Prozess auf Kontenschema bearbeiten, um eine Kontenschemazeile einzurichten, um die Gesamtsumme zu berechnen, auf denen die Prozentsätze basieren.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-137">Choose the **Edit Account Schedule** action to set up an account schedule row to calculate the total on which the percentages will be based.</span></span>  
4. <span data-ttu-id="7fbb5-138">Fügen Sie eine Zeile unmittelbar über der ersten Zeile ein, für die Sie einen Prozentsatz anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-138">Insert a line immediately above the first row for which you want to display a percentage.</span></span>  
5. <span data-ttu-id="7fbb5-139">Füllen Sie die Felder in der Zeile wie folgt aus: In dem Feld **Zusammenzählungsart** geben Sie **Festgelegte Basis für Prozent** ein.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-139">Fill in the fields on the line as follows: In the **Totaling Type** field, enter **Set Base for Percent**.</span></span> <span data-ttu-id="7fbb5-140">Geben Sie im Feld **Zusammenzählung** eine Formel für die Summe ein, auf die der Prozentsatz basiert.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-140">In the **Totaling** field, enter a formula for the total that the percentage will be based on.</span></span> <span data-ttu-id="7fbb5-141">Wenn beispielsweise Zeile 11 die gesamten Verkäufe enthält, geben Sie **11** ein.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-141">For example, if row 11 contains the total sales, enter **11**.</span></span>  
6. <span data-ttu-id="7fbb5-142">Wählen Sie die **Spaltenlayouteinrichtung bearbeiten** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-142">Choose the **Edit Column Layout Setup** action to set up a column.</span></span>  
7. <span data-ttu-id="7fbb5-143">Füllen Sie die Felder in der Zeile wie folgt aus: Wählen Sie im Feld **Spaltenart** **Formel** aus.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-143">Fill in the fields on the line as follows: In the **Column Type** field, select **Formula**.</span></span> <span data-ttu-id="7fbb5-144">Geben Sie im Feld **Formel** eine Formel für den Betrag ein, für den ein Prozentsatz berechnet werden soll, gefolgt von %.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-144">In the **Formula** field, enter a formula for the amount that you want to calculate a percentage for, followed by %.</span></span> <span data-ttu-id="7fbb5-145">Wenn beispielsweise Spalte N die Bewegung enthält, geben Sie **N%** ein.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-145">For example, if column number N contains the net change, enter **N%**.</span></span>  
8. <span data-ttu-id="7fbb5-146">Wiederholen Sie Schritt 4 bis 7 für jede Zeilengruppe, die nach Prozentsätzen aufgeschlüsselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-146">Repeat steps 4 through 7 for each group of rows that you want to break down by percentage.</span></span>

## <a name="to-set-up-account-schedules-with-overviews"></a><span data-ttu-id="7fbb5-147">Kontenschemata mit Matrizen einrichten:</span><span class="sxs-lookup"><span data-stu-id="7fbb5-147">To set up account schedules with overviews</span></span>  
<span data-ttu-id="7fbb5-148">Sie können eine Kontenschema zum Erstellen eines Vergleichs der in der Finanzbuchhaltung gebuchten Werte mit den Finanzbudgetwerten benutzen.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-148">You can use an account schedule to create a statement comparing general ledger figures and general leger budget figures.</span></span>

1. <span data-ttu-id="7fbb5-149">Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Kontenplämne** ein und wählen den zugehörenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-149">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="7fbb5-150">Wählen Sie im Fenster **Kontenschemanamen** ein Kontenschema aus.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-150">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="7fbb5-151">Wählen Sie die **Kontenschema bearbeiten** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-151">Choose the **Edit Account Schedule** action</span></span>  
4. <span data-ttu-id="7fbb5-152">Wählen Sie im Fenster **Kontenplan** den gewünschten Kontenschemanamen im Feld **Name** aus.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-152">In the **Account Schedule** window, in the **Name** field, select the default account schedule name.</span></span>
5. <span data-ttu-id="7fbb5-153">Wählen Sie die **Konten einfügen** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-153">Choose the **Insert Accounts** action.</span></span>  
6. <span data-ttu-id="7fbb5-154">Wählen Sie die Konten, die Sie in Ihrer Aufstellung berücksichtigen möchten, und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-154">Select the accounts that you want to include in your statement, and then choose the **OK** button.</span></span>

    <span data-ttu-id="7fbb5-155">Die Konten sind damit in Ihr Kontenschema eingefügt.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-155">The accounts are now inserted into your account schedule.</span></span> <span data-ttu-id="7fbb5-156">Wenn Sie möchten, können Sie auch das Spaltenlayout ändern.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-156">If you want you can also change the column layout.</span></span>  
7. <span data-ttu-id="7fbb5-157">Wählen Sie die Aktion **Übersicht** aus.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-157">Choose the **Overview** action.</span></span>  
8. <span data-ttu-id="7fbb5-158">Im Inforegister **Dimensionsfilter** legen Sie den gewünschten Budgetfilter fest.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-158">On the **Dimension Filters** FastTab, set the budget filter to the desired filter name.</span></span>  
9. <span data-ttu-id="7fbb5-159">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-159">Choose the **OK** button.</span></span>  

<span data-ttu-id="7fbb5-160">Die Budgetaufstellung kann nun kopiert und in ein Arbeitsblatt eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-160">Now you can copy and paste your budget statement into a spreadsheet.</span></span>  

## <a name="comparing-accounting-periods-using-period-formulas"></a><span data-ttu-id="7fbb5-161">Vergleichen von Buchhaltungsperioden mithilfe der Periodenformulare</span><span class="sxs-lookup"><span data-stu-id="7fbb5-161">Comparing Accounting Periods using Period Formulas</span></span>
<span data-ttu-id="7fbb5-162">Ihr Kontenschema kann sich die Ergebnisse von verschiedenen Buchhaltungsperioden, wie diesen Monat mit jenem des Vorjahresmonat vergleichen.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-162">Your account schedule can compare the results of different accounting periods, such as this month versus same month last year.</span></span> <span data-ttu-id="7fbb5-163">Um das zu tun, fügen Sie eine Spalte mit dem Feld **Vergleichsperiodendatumsformel** hinzu und legen Sie dann dieses Feld auf eine Periodenformel fest.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-163">To do that, you add a column with the **Comparison Period Formula** field, and then set that field to a period formula.</span></span>  

<span data-ttu-id="7fbb5-164">Eine Buchhaltungsperiode muss nicht dem Kalender entsprechen, aber jedes Geschäftsjahr muss dieselbe Anzahl von Buchhaltungsperioden haben, selbst wenn jede Periode eine andere Länge haben kann.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-164">An accounting period does not have to match the calendar, but each fiscal year must have the same number of accounting periods, even though each period can be different in length.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="7fbb5-165"> verwendet diese Periodenformel, um den Betrag der Vergleichsperiode in Bezug auf die Periode zu berechnen, die Sie im Datumsfilter des Anforderungsfensters im Bericht angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-165"> uses the period formula to calculate the amount from the comparison period in relation to the period represented by the date filter on the report request.</span></span> <span data-ttu-id="7fbb5-166">Die Vergleichsperiode basiert auf der Periode des Startdatums des Datumsfilters.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-166">The comparison period is based on the period of the start date of the date filter.</span></span> <span data-ttu-id="7fbb5-167">Für Periodenspezifikationen stehen folgende Abkürzungen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="7fbb5-167">The abbreviations for period specifications are:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7fbb5-168">Abkürzung</span><span class="sxs-lookup"><span data-stu-id="7fbb5-168">Abbreviation</span></span></th>
<th><span data-ttu-id="7fbb5-169">Description</span><span class="sxs-lookup"><span data-stu-id="7fbb5-169">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7fbb5-170">P</span><span class="sxs-lookup"><span data-stu-id="7fbb5-170">P</span></span></p></td>
<td><p><span data-ttu-id="7fbb5-171">Periode</span><span class="sxs-lookup"><span data-stu-id="7fbb5-171">Period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7fbb5-172">EP</span><span class="sxs-lookup"><span data-stu-id="7fbb5-172">LP</span></span></p></td>
<td><p><span data-ttu-id="7fbb5-173">Endperiode eines Geschäftsjahres, eines Halbjahres oder eines Vierteljahres.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-173">Last period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7fbb5-174">LP</span><span class="sxs-lookup"><span data-stu-id="7fbb5-174">CP</span></span></p></td>
<td><p><span data-ttu-id="7fbb5-175">Laufende Periode eines Geschäftsjahres, eines Halbjahres oder eines Vierteljahres.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-175">Current period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7fbb5-176">GJ</span><span class="sxs-lookup"><span data-stu-id="7fbb5-176">FY</span></span></p></td>
<td><p><span data-ttu-id="7fbb5-177">Geschäftsjahr.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-177">Fiscal year.</span></span> <span data-ttu-id="7fbb5-178">GJ[1..3] bezeichnet beispielsweise das erste Quartal des laufenden Geschäftsjahres.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-178">For example, FY[1..3] denotes first quarter of the current fiscal year</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7fbb5-179">Beispiele für Formeln:</span><span class="sxs-lookup"><span data-stu-id="7fbb5-179">Examples of formulas:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7fbb5-180">Formel</span><span class="sxs-lookup"><span data-stu-id="7fbb5-180">Formula</span></span></th>
<th><span data-ttu-id="7fbb5-181">Description</span><span class="sxs-lookup"><span data-stu-id="7fbb5-181">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7fbb5-182">&lt;"Leer"&gt;</span><span class="sxs-lookup"><span data-stu-id="7fbb5-182">&lt;Blank&gt;</span></span></p></td>
<td><p><span data-ttu-id="7fbb5-183">Laufende Periode</span><span class="sxs-lookup"><span data-stu-id="7fbb5-183">Current period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7fbb5-184">-1P</span><span class="sxs-lookup"><span data-stu-id="7fbb5-184">-1P</span></span></p></td>
<td><p><span data-ttu-id="7fbb5-185">Vorperiode</span><span class="sxs-lookup"><span data-stu-id="7fbb5-185">Previous period</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7fbb5-186">-1GJ[1..EP]</span><span class="sxs-lookup"><span data-stu-id="7fbb5-186">-1FY[1..LP]</span></span></p></td>
<td><p><span data-ttu-id="7fbb5-187">Das gesamte vorige Geschäftsjahr</span><span class="sxs-lookup"><span data-stu-id="7fbb5-187">Entire previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7fbb5-188">-1GJ</span><span class="sxs-lookup"><span data-stu-id="7fbb5-188">-1FY</span></span></p></td>
<td><p><span data-ttu-id="7fbb5-189">Laufende Periode des vorigen Geschäftsjahrs</span><span class="sxs-lookup"><span data-stu-id="7fbb5-189">Current period in previous fiscal year</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7fbb5-190">-1GJ[1..3]</span><span class="sxs-lookup"><span data-stu-id="7fbb5-190">-1FY[1..3]</span></span></p></td>
<td><p><span data-ttu-id="7fbb5-191">Das erste Quartal des vorigen Geschäftsjahres</span><span class="sxs-lookup"><span data-stu-id="7fbb5-191">First quarter of previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7fbb5-192">-1GJ[1..LP]</span><span class="sxs-lookup"><span data-stu-id="7fbb5-192">-1FY[1..CP]</span></span></p></td>
<td><p><span data-ttu-id="7fbb5-193">Vom Anfang des vorigen Geschäftsjahres bis zur laufenden Periode des vorigen Geschäftsjahres einschließlich.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-193">From the beginning of previous fiscal year to current period in previous fiscal year, inclusive</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7fbb5-194">-1GJ[LP..EP]</span><span class="sxs-lookup"><span data-stu-id="7fbb5-194">-1FY[CP..LP]</span></span></p></td>
<td><p><span data-ttu-id="7fbb5-195">Von der laufenden Periode des vorigen Geschäftsjahres bis zur Endperiode des vorigen Geschäftsjahres einschließlich.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-195">From current period in previous fiscal year to last period of previous fiscal year, inclusive</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7fbb5-196">Wenn die Berechnung gemäß regulärer Zeitperioden erfolgen soll, muss eine Formel in das Feld **Vergleichsdatumsformel** eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-196">If you want to calculate by regular time periods, you must enter a formula in the **Comparison Date Formula** field instead.</span></span>

> [!NOTE]
> <span data-ttu-id="7fbb5-197">Es ist jedoch nicht immer transparent, welche Perioden Sie vergleichen, da Sie einen Datumsfilter in einem Bericht festlegen können, die verschiedene Daten als die Buchhaltungsperioden umfasst, die Daten im Kontenplan angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-197">It is not always transparent which periods you are comparing because you can set a date filter on a report that spans different dates than the accounting periods that are reflected in the data in the chart of accounts.</span></span> <span data-ttu-id="7fbb5-198">Beispielsweise können Sie ein Kontenschema erstellen, in dem Sie diese Periode mit derselben Periode des Vorjahrs vergleichen möchten, damit Sie den **Vergleichs-Datums-Perioden-Filter** im Feld *1GJ* festlegen.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-198">For example, you create an account schedule where you want to compare this period with the same period last year, so you set the **Comparison Date Period Filter** field to *-1FY*.</span></span> <span data-ttu-id="7fbb5-199">Dann führen Sie den Bericht am 28. Februar aus und legen die Datumsfilter des Januar und Februar fest.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-199">Then, you run the report on February 28th and set the date filter to January and February.</span></span> <span data-ttu-id="7fbb5-200">Deshalb vergleicht das Kontenschema Januar und Februar dieses Jahr mit dem Januar des Vorjahrs, die die einzige abgeschlossene Buchhaltungsperiode der zwei für das Vorjahr ist.</span><span class="sxs-lookup"><span data-stu-id="7fbb5-200">As a result, the account schedule compares January and February this year to January last year, which is the only completed accounting period of the two for last year.</span></span>  


## <a name="see-also"></a><span data-ttu-id="7fbb5-201">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7fbb5-201">See Also</span></span>
[<span data-ttu-id="7fbb5-202">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="7fbb5-202">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="7fbb5-203">Finanzen</span><span class="sxs-lookup"><span data-stu-id="7fbb5-203">Finance</span></span>](finance.md)  
[<span data-ttu-id="7fbb5-204">Finance einrichten</span><span class="sxs-lookup"><span data-stu-id="7fbb5-204">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="7fbb5-205">Die Finanzbuchhaltung und der Kontenplan</span><span class="sxs-lookup"><span data-stu-id="7fbb5-205">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="7fbb5-206">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7fbb5-206">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

