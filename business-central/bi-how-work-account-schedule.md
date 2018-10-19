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
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 8e63e507411f41c67caa94834f4d99861bd1ae77
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a><span data-ttu-id="f1e4b-103">Bereiten Sie Finanzberichte mit Kontenschemata und Kontengruppen vor</span><span class="sxs-lookup"><span data-stu-id="f1e4b-103">Prepare Financial Reporting with Account Schedules and Account Categories</span></span>
<span data-ttu-id="f1e4b-104">Verwenden von Kontenplan, um die Einblicke in die Finanzdaten zu kommen, die in Ihrem Kontenplan gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-104">Use account schedules to get insight into the financial data stored in your chart of accounts.</span></span> <span data-ttu-id="f1e4b-105">Verwenden von Kontenschemata zum Analysieren der Werte auf Sachkonten oder zum Vergleichen von Sachposten mit Finanzbudgetposten.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-105">Account schedules analyze figures in G/L accounts, and compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="f1e4b-106">Die Ergebnisse werden in den Diagrammen in Ihrem Rollencenter angezeigt, wie der Cashflowplan und Berichten, wie den GuV und den Bilanzberichten.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-106">The results display in charts on your Role Center, such as the Cash Flow chart, and in reports, such as the Income Statement and the Balance Sheet reports.</span></span>

<span data-ttu-id="f1e4b-107">Sie rufen diese beiden Berichte beispielsweise mit der Aktion **Finanzverhältnis-Abrechnungen** im Business Manager und Buchhalter Rollen-Centers ab.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-107">You access these two reports, for example, with the **Financials Statements** action on the Business Manager and Accountant Role Centers.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="f1e4b-108">enthält mehrere Beispielkontenschemata, die Sie verwenden können , oder Sie können eigene Zeilen und Spalten einrichten, um die Werte anzugeben und zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-108">provides a few sample account schedules that you can use right away, or you can set up your own rows and columns to specify the figures to compare.</span></span> <span data-ttu-id="f1e4b-109">So können beispielsweise Kontenschemata zur Berechnung von Gewinnmargen für Dimensionen wie beispielsweise Abteilungen oder Debitorengruppen erstellen.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-109">For example, you can create account schedules to calculate profit margins on dimensions like departments or customer groups.</span></span> <span data-ttu-id="f1e4b-110">Das bedeutet, dass Sie so viele maßgeschneiderte Finanzaufstellungen erstellen können, wie Sie möchten.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-110">You can create as many customized financial statements as you want.</span></span>  

<span data-ttu-id="f1e4b-111">Das Einrichten von Kontenschemata erfordert ein Verständnis für die Finanzdaten im Kontenplan.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-111">Setting up account schedules requires an understanding of the financial data in the chart of accounts.</span></span> <span data-ttu-id="f1e4b-112">Sie können beispielsweise die Sachposten als prozentualen Anteil der Budgetposten sehen.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-112">For example, you can view general ledger entries as percentages of budget entries.</span></span> <span data-ttu-id="f1e4b-113">Dazu ist es erforderlich, dass Budgets erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-113">This requires that budgets are created.</span></span> <span data-ttu-id="f1e4b-114">Weitere Informationen finden Sie unter [Sachkonto-Budgets erstellen](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="f1e4b-114">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

## <a name="account-categories-and-account-schedules"></a><span data-ttu-id="f1e4b-115">Kontengruppen und Kontenschemata</span><span class="sxs-lookup"><span data-stu-id="f1e4b-115">Account Categories and Account Schedules</span></span>
<span data-ttu-id="f1e4b-116">Sie können Kontengruppen dazu verwenden, das Layout Ihrer Finanzberichte zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-116">You can use account categories to change the layout of your financial statements.</span></span> <span data-ttu-id="f1e4b-117">Wenn Sie Ihre Kontengruppen im Fenster **Sachkontokategorien** eingerichtet haben und die Aktion **Kontenschemata generieren** auswählen, werden die zugrunde liegenden Kontenschemata für die Kernfinanzberichte aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-117">After you set up your account categories in the **G/L Account Categories** window, and you choose the **Generate Account Schedules** action, the underlying account schedules for the core financial reports are updated.</span></span> <span data-ttu-id="f1e4b-118">Wenn Sie das nächste Mal einen dieser Berichte wie die Saldoabrechnung ausführen, werden neue Summen und Untereinträge basierend auf Ihren Änderungen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-118">The next time you run one of these reports, such as the Balance Statement report, new totals and subentries are added, based on your changes.</span></span> <span data-ttu-id="f1e4b-119">Weitere Informationen finden Sie unter "Buchhaltungskategorien" unter [Die Finanzbuchhaltung und der Kontenplan verstehen](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="f1e4b-119">For more information, see The "Account Categories" section in [Understanding the General Ledger and the COA](finance-general-ledger.md).</span></span>  

## <a name="to-create-new-account-schedules"></a><span data-ttu-id="f1e4b-120">Neue Kontenschemata erstellen:</span><span class="sxs-lookup"><span data-stu-id="f1e4b-120">To create new account schedules</span></span>  
 <span data-ttu-id="f1e4b-121">Sie benutzen Kontenschemata zum Analysieren der Werte auf Sachkonten oder zum Vergleichen von Sachposten mit Finanzbudgetposten.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-121">You use account schedules to analyze figures in general ledger accounts or to compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="f1e4b-122">Sie können beispielsweise die Sachposten als prozentualen Anteil der Finanzbudgetposten sehen.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-122">For example, you can view the general ledger entries as percentages of the budget entries.</span></span>

1. <span data-ttu-id="f1e4b-123">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontenplan** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f1e4b-124">Wählen Sie im Fenster **Kontoschemaname** auf der Registerkarte **Neu** die Option Neu aus, um einen neuen Kontenschemanamen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-124">In the **Account Schedule Names** window, choose the **New** action to create a new account schedule name.</span></span>
3. <span data-ttu-id="f1e4b-125">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-125">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="f1e4b-126">Wählen Sie die **Kontenschema bearbeiten** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-126">Choose the **Edit Account Schedule** action.</span></span>
5. <span data-ttu-id="f1e4b-127">Füllen Sie die Felder im Fenster **Kontenschema** aus.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-127">In the **Account Schedule** window, fill in the fields as necessary.</span></span>  

    <span data-ttu-id="f1e4b-128">Nachdem Sie ein neues Kontenschema erstellt haben und neue Zeilen in Ihrem Kontenschema eingerichtet haben, müssen Sie die Spalten einrichten.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-128">When you have created a new account schedule and set up the rows, you must set up columns.</span></span> <span data-ttu-id="f1e4b-129">Sie können diese entweder manuell einrichten oder Ihrem Kontenschema ein vordefiniertes Spaltenlayout zuweisen.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-129">You can either set them up manually or assign a predefined column layout to your account schedule.</span></span>
6. <span data-ttu-id="f1e4b-130">Wählen Sie die **Spaltenlayouteinrichtung bearbeiten** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-130">Choose the **Edit Column Layout Setup** action.</span></span>
7. <span data-ttu-id="f1e4b-131">Füllen Sie die Felder im Fenster **Spaltenlayout** aus.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-131">In the **Column Layout** window, fill in the fields as necessary.</span></span>

> [!NOTE]  
> <span data-ttu-id="f1e4b-132">Wurde dem Kontenschema kein Standardspaltenlayout zugeordnet, müssen Sie die Spalten manuell einrichten.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-132">If you did not assign a default column layout to the account schedule, you must set the columns up manually.</span></span>

### <a name="to-copy-an-existing-account-schedule"></a><span data-ttu-id="f1e4b-133">So kopieren Sie ein Kontenschema</span><span class="sxs-lookup"><span data-stu-id="f1e4b-133">To copy an existing account schedule</span></span>
<span data-ttu-id="f1e4b-134">Die Kontenschemata in der Standardeinstellung sind [!INCLUDE[d365fin](includes/d365fin_md.md)] die Basis der Standardfinanzberichte, die möglicherweise nicht den Anforderungen Ihres Unternehmens entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-134">The account schedules in the standard version of [!INCLUDE[d365fin](includes/d365fin_md.md)] are the basis of the standard financial reports, which may not suit the needs of your business.</span></span> <span data-ttu-id="f1e4b-135">Um Ihre eigenen Finanzberichte schnell erstellen zu können, beginnen Sie, indem Sie ein vorhandenes Kontenschema kopieren.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-135">To quickly create your own financial reports, you can start by copying an existing account schedule.</span></span>
1. <span data-ttu-id="f1e4b-136">Im Fenster **Kontenschemata** können Sie ein Kontenschema wählen und dann die **Kontenschema kopieren** Aktion auswählen.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-136">In the **Account Schedules** window, select an account schedule, and then choose the **Copy Account Schedule** action.</span></span>
2. <span data-ttu-id="f1e4b-137">Im Fenster **Kontenplan kopieren** geben Sie die Felder wie nötig ein, und wählen Sie dann die Schaltfläche **OK**.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-137">In the **Copy Account Schedule** window, fill in the fields as necessary, and then choose the **OK** button.</span></span>

### <a name="to-create-a-column-that-calculates-percentages"></a><span data-ttu-id="f1e4b-138">Eine Spalte zur Berechnung von Prozentsätzen erstellen:</span><span class="sxs-lookup"><span data-stu-id="f1e4b-138">To create a column that calculates percentages</span></span>  
<span data-ttu-id="f1e4b-139">Manchmal möchten Sie möglicherweise eine Spalte in ein Kontenschema einfügen, in der Prozentsätze einer Summe berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-139">Sometimes you may want to include a column in an account schedule to calculate percentages of a total.</span></span> <span data-ttu-id="f1e4b-140">Wenn beispielsweise mehrere Zeilen vorhanden sind, in denen die Verkäufe nach Dimension aufgeschlüsselt sind, empfiehlt sich die Einrichtung einer Spalte, in der für jede Zeile der prozentuale Anteil an den Gesamtverkäufen angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-140">For example, if you have a number of rows that break down sales by dimension, you may want a column to indicate the percentage of total sales that each row represents.</span></span>

1. <span data-ttu-id="f1e4b-141">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontenplan** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-141">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="f1e4b-142">Wählen Sie im Fenster **Kontenschemanamen** ein Kontenschema aus.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-142">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="f1e4b-143">Klicken Sie auf der Registerkarte **Kontoschema bearbeiten** in der Gruppe Prozess auf Kontenschema bearbeiten, um eine Kontenschemazeile einzurichten, um die Gesamtsumme zu berechnen, auf denen die Prozentsätze basieren.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-143">Choose the **Edit Account Schedule** action to set up an account schedule row to calculate the total on which the percentages will be based.</span></span>  
4. <span data-ttu-id="f1e4b-144">Fügen Sie eine Zeile unmittelbar über der ersten Zeile ein, für die Sie einen Prozentsatz anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-144">Insert a line immediately above the first row for which you want to display a percentage.</span></span>  
5. <span data-ttu-id="f1e4b-145">Füllen Sie die Felder in der Zeile wie folgt aus: In dem Feld **Zusammenzählungsart** geben Sie **Festgelegte Basis für Prozent** ein.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-145">Fill in the fields on the line as follows: In the **Totaling Type** field, enter **Set Base for Percent**.</span></span> <span data-ttu-id="f1e4b-146">Geben Sie im Feld **Zusammenzählung** eine Formel für die Summe ein, auf die der Prozentsatz basiert.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-146">In the **Totaling** field, enter a formula for the total that the percentage will be based on.</span></span> <span data-ttu-id="f1e4b-147">Wenn beispielsweise Zeile 11 die gesamten Verkäufe enthält, geben Sie **11** ein.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-147">For example, if row 11 contains the total sales, enter **11**.</span></span>  
6. <span data-ttu-id="f1e4b-148">Wählen Sie die **Spaltenlayouteinrichtung bearbeiten** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-148">Choose the **Edit Column Layout Setup** action to set up a column.</span></span>  
7. <span data-ttu-id="f1e4b-149">Füllen Sie die Felder in der Zeile wie folgt aus: Wählen Sie im Feld **Spaltenart** **Formel** aus.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-149">Fill in the fields on the line as follows: In the **Column Type** field, select **Formula**.</span></span> <span data-ttu-id="f1e4b-150">Geben Sie im Feld **Formel** eine Formel für den Betrag ein, für den ein Prozentsatz berechnet werden soll, gefolgt von %.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-150">In the **Formula** field, enter a formula for the amount that you want to calculate a percentage for, followed by %.</span></span> <span data-ttu-id="f1e4b-151">Wenn beispielsweise Spalte N die Bewegung enthält, geben Sie **N%** ein.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-151">For example, if column number N contains the net change, enter **N%**.</span></span>  
8. <span data-ttu-id="f1e4b-152">Wiederholen Sie Schritt 4 bis 7 für jede Zeilengruppe, die nach Prozentsätzen aufgeschlüsselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-152">Repeat steps 4 through 7 for each group of rows that you want to break down by percentage.</span></span>

## <a name="to-set-up-account-schedules-with-overviews"></a><span data-ttu-id="f1e4b-153">Kontenschemata mit Matrizen einrichten:</span><span class="sxs-lookup"><span data-stu-id="f1e4b-153">To set up account schedules with overviews</span></span>  
<span data-ttu-id="f1e4b-154">Sie können eine Kontenschema zum Erstellen eines Vergleichs der in der Finanzbuchhaltung gebuchten Werte mit den Finanzbudgetwerten benutzen.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-154">You can use an account schedule to create a statement comparing general ledger figures and general leger budget figures.</span></span>

1. <span data-ttu-id="f1e4b-155">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontenplan** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-155">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="f1e4b-156">Wählen Sie im Fenster **Kontenschemanamen** ein Kontenschema aus.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-156">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="f1e4b-157">Wählen Sie die **Kontenschema bearbeiten** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-157">Choose the **Edit Account Schedule** action</span></span>  
4. <span data-ttu-id="f1e4b-158">Wählen Sie im Fenster **Kontenplan** den gewünschten Kontenschemanamen im Feld **Name** aus.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-158">In the **Account Schedule** window, in the **Name** field, select the default account schedule name.</span></span>
5. <span data-ttu-id="f1e4b-159">Wählen Sie die **Konten einfügen** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-159">Choose the **Insert Accounts** action.</span></span>  
6. <span data-ttu-id="f1e4b-160">Wählen Sie die Konten, die Sie in Ihrer Aufstellung berücksichtigen möchten, und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-160">Select the accounts that you want to include in your statement, and then choose the **OK** button.</span></span>

    <span data-ttu-id="f1e4b-161">Die Konten sind damit in Ihr Kontenschema eingefügt.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-161">The accounts are now inserted into your account schedule.</span></span> <span data-ttu-id="f1e4b-162">Wenn Sie möchten, können Sie auch das Spaltenlayout ändern.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-162">If you want you can also change the column layout.</span></span>  
7. <span data-ttu-id="f1e4b-163">Wählen Sie die Aktion **Übersicht** aus.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-163">Choose the **Overview** action.</span></span>  
8. <span data-ttu-id="f1e4b-164">Im Inforegister **Dimensionsfilter** legen Sie den gewünschten Budgetfilter fest.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-164">On the **Dimension Filters** FastTab, set the budget filter to the desired filter name.</span></span>  
9. <span data-ttu-id="f1e4b-165">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-165">Choose the **OK** button.</span></span>  

<span data-ttu-id="f1e4b-166">Die Budgetaufstellung kann nun kopiert und in ein Arbeitsblatt eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-166">Now you can copy and paste your budget statement into a spreadsheet.</span></span>  

## <a name="comparing-accounting-periods-using-period-formulas"></a><span data-ttu-id="f1e4b-167">Vergleichen von Buchhaltungsperioden mithilfe der Periodenformulare</span><span class="sxs-lookup"><span data-stu-id="f1e4b-167">Comparing Accounting Periods using Period Formulas</span></span>
<span data-ttu-id="f1e4b-168">Ihr Kontenschema kann sich die Ergebnisse von verschiedenen Buchhaltungsperioden, wie diesen Monat mit jenem des Vorjahresmonat vergleichen.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-168">Your account schedule can compare the results of different accounting periods, such as this month versus same month last year.</span></span> <span data-ttu-id="f1e4b-169">Um das zu tun, fügen Sie eine Spalte mit dem Feld **Vergleichsperiodendatumsformel** hinzu und legen Sie dann dieses Feld auf eine Periodenformel fest.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-169">To do that, you add a column with the **Comparison Period Formula** field, and then set that field to a period formula.</span></span>  

<span data-ttu-id="f1e4b-170">Eine Buchhaltungsperiode muss nicht dem Kalender entsprechen, aber jedes Geschäftsjahr muss dieselbe Anzahl von Buchhaltungsperioden haben, selbst wenn jede Periode eine andere Länge haben kann.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-170">An accounting period does not have to match the calendar, but each fiscal year must have the same number of accounting periods, even though each period can be different in length.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="f1e4b-171">verwendet diese Periodenformel, um den Betrag der Vergleichsperiode in Bezug auf die Periode zu berechnen, die Sie im Datumsfilter des Anforderungsfensters im Bericht angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-171">uses the period formula to calculate the amount from the comparison period in relation to the period represented by the date filter on the report request.</span></span> <span data-ttu-id="f1e4b-172">Die Vergleichsperiode basiert auf der Periode des Startdatums des Datumsfilters.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-172">The comparison period is based on the period of the start date of the date filter.</span></span> <span data-ttu-id="f1e4b-173">Für Periodenspezifikationen stehen folgende Abkürzungen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="f1e4b-173">The abbreviations for period specifications are:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f1e4b-174">Abkürzung</span><span class="sxs-lookup"><span data-stu-id="f1e4b-174">Abbreviation</span></span></th>
<th><span data-ttu-id="f1e4b-175">Description</span><span class="sxs-lookup"><span data-stu-id="f1e4b-175">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1e4b-176">P</span><span class="sxs-lookup"><span data-stu-id="f1e4b-176">P</span></span></p></td>
<td><p><span data-ttu-id="f1e4b-177">Periode</span><span class="sxs-lookup"><span data-stu-id="f1e4b-177">Period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1e4b-178">EP</span><span class="sxs-lookup"><span data-stu-id="f1e4b-178">LP</span></span></p></td>
<td><p><span data-ttu-id="f1e4b-179">Endperiode eines Geschäftsjahres, eines Halbjahres oder eines Vierteljahres.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-179">Last period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1e4b-180">LP</span><span class="sxs-lookup"><span data-stu-id="f1e4b-180">CP</span></span></p></td>
<td><p><span data-ttu-id="f1e4b-181">Laufende Periode eines Geschäftsjahres, eines Halbjahres oder eines Vierteljahres.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-181">Current period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1e4b-182">GJ</span><span class="sxs-lookup"><span data-stu-id="f1e4b-182">FY</span></span></p></td>
<td><p><span data-ttu-id="f1e4b-183">Geschäftsjahr.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-183">Fiscal year.</span></span> <span data-ttu-id="f1e4b-184">GJ[1..3] bezeichnet beispielsweise das erste Quartal des laufenden Geschäftsjahres.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-184">For example, FY[1..3] denotes first quarter of the current fiscal year</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f1e4b-185">Beispiele für Formeln:</span><span class="sxs-lookup"><span data-stu-id="f1e4b-185">Examples of formulas:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f1e4b-186">Formel</span><span class="sxs-lookup"><span data-stu-id="f1e4b-186">Formula</span></span></th>
<th><span data-ttu-id="f1e4b-187">Description</span><span class="sxs-lookup"><span data-stu-id="f1e4b-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1e4b-188">&lt;"Leer"&gt;</span><span class="sxs-lookup"><span data-stu-id="f1e4b-188">&lt;Blank&gt;</span></span></p></td>
<td><p><span data-ttu-id="f1e4b-189">Laufende Periode</span><span class="sxs-lookup"><span data-stu-id="f1e4b-189">Current period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1e4b-190">-1P</span><span class="sxs-lookup"><span data-stu-id="f1e4b-190">-1P</span></span></p></td>
<td><p><span data-ttu-id="f1e4b-191">Vorperiode</span><span class="sxs-lookup"><span data-stu-id="f1e4b-191">Previous period</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1e4b-192">-1GJ[1..EP]</span><span class="sxs-lookup"><span data-stu-id="f1e4b-192">-1FY[1..LP]</span></span></p></td>
<td><p><span data-ttu-id="f1e4b-193">Das gesamte vorige Geschäftsjahr</span><span class="sxs-lookup"><span data-stu-id="f1e4b-193">Entire previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1e4b-194">-1GJ</span><span class="sxs-lookup"><span data-stu-id="f1e4b-194">-1FY</span></span></p></td>
<td><p><span data-ttu-id="f1e4b-195">Laufende Periode des vorigen Geschäftsjahrs</span><span class="sxs-lookup"><span data-stu-id="f1e4b-195">Current period in previous fiscal year</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1e4b-196">-1GJ[1..3]</span><span class="sxs-lookup"><span data-stu-id="f1e4b-196">-1FY[1..3]</span></span></p></td>
<td><p><span data-ttu-id="f1e4b-197">Das erste Quartal des vorigen Geschäftsjahres</span><span class="sxs-lookup"><span data-stu-id="f1e4b-197">First quarter of previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1e4b-198">-1GJ[1..LP]</span><span class="sxs-lookup"><span data-stu-id="f1e4b-198">-1FY[1..CP]</span></span></p></td>
<td><p><span data-ttu-id="f1e4b-199">Vom Anfang des vorigen Geschäftsjahres bis zur laufenden Periode des vorigen Geschäftsjahres einschließlich.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-199">From the beginning of previous fiscal year to current period in previous fiscal year, inclusive</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1e4b-200">-1GJ[LP..EP]</span><span class="sxs-lookup"><span data-stu-id="f1e4b-200">-1FY[CP..LP]</span></span></p></td>
<td><p><span data-ttu-id="f1e4b-201">Von der laufenden Periode des vorigen Geschäftsjahres bis zur Endperiode des vorigen Geschäftsjahres einschließlich.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-201">From current period in previous fiscal year to last period of previous fiscal year, inclusive</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f1e4b-202">Wenn die Berechnung gemäß regulärer Zeitperioden erfolgen soll, muss eine Formel in das Feld **Vergleichsdatumsformel** eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-202">If you want to calculate by regular time periods, you must enter a formula in the **Comparison Date Formula** field instead.</span></span>

> [!NOTE]
> <span data-ttu-id="f1e4b-203">Es ist jedoch nicht immer transparent, welche Perioden Sie vergleichen, da Sie einen Datumsfilter in einem Bericht festlegen können, die verschiedene Daten als die Buchhaltungsperioden umfasst, die Daten im Kontenplan angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-203">It is not always transparent which periods you are comparing because you can set a date filter on a report that spans different dates than the accounting periods that are reflected in the data in the chart of accounts.</span></span> <span data-ttu-id="f1e4b-204">Beispielsweise können Sie ein Kontenschema erstellen, in dem Sie diese Periode mit derselben Periode des Vorjahrs vergleichen möchten, damit Sie den **Vergleichs-Datums-Perioden-Filter** im Feld *1GJ* festlegen.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-204">For example, you create an account schedule where you want to compare this period with the same period last year, so you set the **Comparison Date Period Filter** field to *-1FY*.</span></span> <span data-ttu-id="f1e4b-205">Dann führen Sie den Bericht am 28. Februar aus und legen die Datumsfilter des Januar und Februar fest.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-205">Then, you run the report on February 28th and set the date filter to January and February.</span></span> <span data-ttu-id="f1e4b-206">Deshalb vergleicht das Kontenschema Januar und Februar dieses Jahr mit dem Januar des Vorjahrs, die die einzige abgeschlossene Buchhaltungsperiode der zwei für das Vorjahr ist.</span><span class="sxs-lookup"><span data-stu-id="f1e4b-206">As a result, the account schedule compares January and February this year to January last year, which is the only completed accounting period of the two for last year.</span></span>  


## <a name="see-also"></a><span data-ttu-id="f1e4b-207">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1e4b-207">See Also</span></span>
[<span data-ttu-id="f1e4b-208">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="f1e4b-208">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="f1e4b-209">Finanzen</span><span class="sxs-lookup"><span data-stu-id="f1e4b-209">Finance</span></span>](finance.md)  
[<span data-ttu-id="f1e4b-210">Finance einrichten</span><span class="sxs-lookup"><span data-stu-id="f1e4b-210">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="f1e4b-211">Die Finanzbuchhaltung und der Kontenplan</span><span class="sxs-lookup"><span data-stu-id="f1e4b-211">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="f1e4b-212">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f1e4b-212">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

