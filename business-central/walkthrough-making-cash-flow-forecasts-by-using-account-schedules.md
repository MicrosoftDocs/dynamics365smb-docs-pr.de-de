---
title: Exemplarische Vorgehensweise - Erstellen von Cashflowplanungen mithilfe von Kontenschemata | Microsoft Docs
description: In dieser exemplarischen Vorgehensweise wird beschrieben, wie Sie mit Kontenschemata arbeiten können, um Cashflowplanungen zu erstellen. Kontenschemata führen Berechnungen aus, die nicht direkt im Kontenplan für Cashflowkonten vorgenommen werden können. In Kontenschemata können Sie Zwischensummen für Cashflow-Auftragseingänge und -Auszahlungen einrichten. Diese Zwischensummen können in neue Summen einbezogen werden, die dann für Cashflowplanungen verwendet werden können.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 415cabbb859bfc49477f69b19ad4a4daf1137837
ms.sourcegitcommit: 319023e53627dbe8e68643908aacc6fd594a4957
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2019
ms.locfileid: "2554692"
---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a><span data-ttu-id="9fccf-106">Exemplarische Vorgehensweise: Erstellen von Cashflowplanungen mithilfe von Kontenschemata</span><span class="sxs-lookup"><span data-stu-id="9fccf-106">Walkthrough: Making Cash Flow Forecasts by Using Account Schedules</span></span>
<span data-ttu-id="9fccf-107">In dieser exemplarischen Vorgehensweise wird beschrieben, wie Sie mit Kontenschemata arbeiten können, um Cashflowplanungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9fccf-107">This walkthrough describes how you can use account schedules to make cash flow forecasts.</span></span> <span data-ttu-id="9fccf-108">Kontenschemata führen Berechnungen aus, die nicht direkt im Kontenplan für Cashflowkonten vorgenommen werden können.</span><span class="sxs-lookup"><span data-stu-id="9fccf-108">Account schedules perform calculations that cannot be done directly in the chart of cash flow accounts.</span></span> <span data-ttu-id="9fccf-109">In Kontenschemata können Sie Zwischensummen für Cashflow-Auftragseingänge und -Auszahlungen einrichten.</span><span class="sxs-lookup"><span data-stu-id="9fccf-109">In the account schedules, you can set up subtotals for cash flow receipts and disbursements.</span></span> <span data-ttu-id="9fccf-110">Diese Zwischensummen können in neue Summen einbezogen werden, die dann für Cashflowplanungen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="9fccf-110">These subtotals can be included in new totals that can then be used in making cash flow forecasts.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="9fccf-111">Informationen zu dieser exemplarischen Vorgehensweise</span><span class="sxs-lookup"><span data-stu-id="9fccf-111">About This Walkthrough</span></span>  
<span data-ttu-id="9fccf-112">In dieser exemplarischen Vorgehensweise werden folgende Aufgaben erläutert:</span><span class="sxs-lookup"><span data-stu-id="9fccf-112">This walkthrough describes the following tasks:</span></span>  

- <span data-ttu-id="9fccf-113">Einrichten eines neuen Cashflowkonto-Zeitplannamens.</span><span class="sxs-lookup"><span data-stu-id="9fccf-113">Setting up a new cash flow account schedule name.</span></span>  
- <span data-ttu-id="9fccf-114">Einrichten von Kontenschemazeilen.</span><span class="sxs-lookup"><span data-stu-id="9fccf-114">Setting up account schedule lines.</span></span>  
- <span data-ttu-id="9fccf-115">Einrichten eines neuen Spaltenlayouts.</span><span class="sxs-lookup"><span data-stu-id="9fccf-115">Setting up a new column layout.</span></span>  
- <span data-ttu-id="9fccf-116">Zuweisen eines Spaltenlayouts zu einem Kontenschema.</span><span class="sxs-lookup"><span data-stu-id="9fccf-116">Assigning a column layout to an account schedule.</span></span>  
- <span data-ttu-id="9fccf-117">Anzeigen und Drucken der Cashflowplanung.</span><span class="sxs-lookup"><span data-stu-id="9fccf-117">Viewing and printing the cash flow forecast.</span></span>  

### <a name="prerequisites"></a><span data-ttu-id="9fccf-118">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="9fccf-118">Prerequisites</span></span>  
<span data-ttu-id="9fccf-119">Für diese exemplarische Vorgehensweise gelten folgende Voraussetzungen:</span><span class="sxs-lookup"><span data-stu-id="9fccf-119">To complete this walkthrough, you will need:</span></span>  

- [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="9fccf-120">installiert.</span><span class="sxs-lookup"><span data-stu-id="9fccf-120">installed.</span></span>  
- <span data-ttu-id="9fccf-121">Die Cashflowvorschlagszeilen werden erfasst.</span><span class="sxs-lookup"><span data-stu-id="9fccf-121">The cash flow worksheet lines are registered.</span></span>  

## <a name="roles"></a><span data-ttu-id="9fccf-122">Rollen</span><span class="sxs-lookup"><span data-stu-id="9fccf-122">Roles</span></span>  
<span data-ttu-id="9fccf-123">Die Aufgaben in dieser exemplarischen Vorgehensweise werden von den folgenden Benutzern ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="9fccf-123">This walkthrough demonstrates tasks that are performed by the following user role:</span></span>  

- <span data-ttu-id="9fccf-124">CONTROLLER</span><span class="sxs-lookup"><span data-stu-id="9fccf-124">Controller</span></span>  

## <a name="story"></a><span data-ttu-id="9fccf-125">Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9fccf-125">Story</span></span>  
<span data-ttu-id="9fccf-126">Ken ist ein Controller bei CRONUS , der Monatscashflowplanungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="9fccf-126">Ken is a controller at CRONUS who makes monthly cash flow forecasts.</span></span> <span data-ttu-id="9fccf-127">Es schließt Finanzen, Verkauf, Einkauf und Anlagen in die Planung ein und zeigt sie dann CFO Sara für den Geschäfteseinblick.</span><span class="sxs-lookup"><span data-stu-id="9fccf-127">He includes finance, sales, purchase, and fixed assets in the forecast, and then he presents it to CFO Sara for business insight.</span></span>  

## <a name="setting-up-a-new-account-schedule-name"></a><span data-ttu-id="9fccf-128">Einrichten eines neuen Kontenschemanamens</span><span class="sxs-lookup"><span data-stu-id="9fccf-128">Setting Up a New Account Schedule Name</span></span>  
<span data-ttu-id="9fccf-129">Ein Kontenschema besteht aus einem Cashflow-Kontenschemanamen mit einer Reihe von Zeilen und einem Spaltenlayout.</span><span class="sxs-lookup"><span data-stu-id="9fccf-129">An account schedule consists of a cash flow account schedule name with a series of lines and a column layout.</span></span>  

### <a name="to-set-up-a-new-account-schedule-name"></a><span data-ttu-id="9fccf-130">Einen neuen Kontenschemanamen einrichten:</span><span class="sxs-lookup"><span data-stu-id="9fccf-130">To set up a new account schedule name</span></span>  

1.  <span data-ttu-id="9fccf-131">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion Wie möchten Sie weiter verfahren geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontenplan** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="9fccf-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="9fccf-132">Wählen Sie auf der Seite **Kontoschemaname** auf der Registerkarte **Neu** die Option Neu aus, um einen neuen Cashflow zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9fccf-132">On the **Account Schedule Names** page, choose the **New** to create a new cash flow account schedule name.</span></span>  
3.  <span data-ttu-id="9fccf-133">Geben Sie im Feld **Namen** **Planung** ein.</span><span class="sxs-lookup"><span data-stu-id="9fccf-133">In the **Name** field, enter **Forecast**.</span></span>  
4.  <span data-ttu-id="9fccf-134">Geben Sie im Feld **Beschreibung** eine Beschreibung für die **Cashflowplanung** ein.</span><span class="sxs-lookup"><span data-stu-id="9fccf-134">In the **Description** field, enter **Cash Flow Forecast**.</span></span>  
5.  <span data-ttu-id="9fccf-135">Lassen Sie die Felder **Standard Spaltenlayout** und **Analyseansichtsname** leer.</span><span class="sxs-lookup"><span data-stu-id="9fccf-135">Leave the **Default Column Layout** and **Analysis View Name** fields blank.</span></span>  

## <a name="setting-up-account-schedule-lines"></a><span data-ttu-id="9fccf-136">Einrichten von Kontenschemazeilen</span><span class="sxs-lookup"><span data-stu-id="9fccf-136">Setting Up Account Schedule Lines</span></span>  
<span data-ttu-id="9fccf-137">Nachdem ein Kontenschemaname eingerichtet wurde, definiert Ken jede Zeile, die im Cashflow-Kontenschema angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9fccf-137">After an account schedule name is set up, Ken defines each line that appears in the cash flow account schedule.</span></span> <span data-ttu-id="9fccf-138">Ken definiert Zeilen, die in Berichten zusätzlich zu den Zeilen angezeigt werden können, die nur Berechnungszwecken dienen.</span><span class="sxs-lookup"><span data-stu-id="9fccf-138">Ken defines lines that can be shown in reports in addition to lines that are only for calculation purposes.</span></span>  

### <a name="to-set-up-account-schedule-lines"></a><span data-ttu-id="9fccf-139">So richten Sie Kontenschemazeilen ein</span><span class="sxs-lookup"><span data-stu-id="9fccf-139">To set up account schedule lines</span></span>  

1.  <span data-ttu-id="9fccf-140">Wählen Sie auf der Seite **Kontenplannamen** den neuen **Prognose**Kontenplannamen, den Sie erstellt haben, und wählen Sie dann die Aktion **Kontenplan bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="9fccf-140">On the **Account Schedule Names** page, select the new **Forecast** account schedule name that you have created, and then choose the **Edit Account Schedule** action.</span></span>  
2.  <span data-ttu-id="9fccf-141">Auf der Seite **Kontoplan** geben Sie jede Zeile genau wie in der folgenden Tabelle ein.</span><span class="sxs-lookup"><span data-stu-id="9fccf-141">On the **Account Schedule** page, enter each line exactly as shown in the following table.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="9fccf-142">Mithilfe der Funktion **CF-Konten einfügen** können Sie die Cashflowkonten aus dem Kontenplan für Cashflowkontos schnell markieren und sie in Kontenschemazeilen kopieren.</span><span class="sxs-lookup"><span data-stu-id="9fccf-142">Using the **Insert CF Accounts** function, you can quickly mark the cash flow accounts from the chart of cash flow accounts and copy them to account schedule lines.</span></span>  

    |<span data-ttu-id="9fccf-143">Rubrikennr.</span><span class="sxs-lookup"><span data-stu-id="9fccf-143">Row No.</span></span>|<span data-ttu-id="9fccf-144">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9fccf-144">Description</span></span>|<span data-ttu-id="9fccf-145">Zusammenzählungsart</span><span class="sxs-lookup"><span data-stu-id="9fccf-145">Totaling Type</span></span>|<span data-ttu-id="9fccf-146">Zusammenzählung</span><span class="sxs-lookup"><span data-stu-id="9fccf-146">Totaling</span></span>|<span data-ttu-id="9fccf-147">Zeilenart</span><span class="sxs-lookup"><span data-stu-id="9fccf-147">Row Type</span></span>|<span data-ttu-id="9fccf-148">Betragsart</span><span class="sxs-lookup"><span data-stu-id="9fccf-148">Amount Type</span></span>|<span data-ttu-id="9fccf-149">Anzeigen</span><span class="sxs-lookup"><span data-stu-id="9fccf-149">Show</span></span>|  
    |-------|-----------|-------------|--------|--------|-----------|----|
    |<span data-ttu-id="9fccf-150">C10</span><span class="sxs-lookup"><span data-stu-id="9fccf-150">C10</span></span>|<span data-ttu-id="9fccf-151">Betrag</span><span class="sxs-lookup"><span data-stu-id="9fccf-151">Amount</span></span>|<span data-ttu-id="9fccf-152">Bewegung</span><span class="sxs-lookup"><span data-stu-id="9fccf-152">Net Change</span></span>|<span data-ttu-id="9fccf-153">Posten</span><span class="sxs-lookup"><span data-stu-id="9fccf-153">Entries</span></span>|<span data-ttu-id="9fccf-154">Nettobetrag</span><span class="sxs-lookup"><span data-stu-id="9fccf-154">Net Amount</span></span>|<span data-ttu-id="9fccf-155">Immer</span><span class="sxs-lookup"><span data-stu-id="9fccf-155">Always</span></span>|  
    |<span data-ttu-id="9fccf-156">C20</span><span class="sxs-lookup"><span data-stu-id="9fccf-156">C20</span></span>|<span data-ttu-id="9fccf-157">Betrag bis Datum</span><span class="sxs-lookup"><span data-stu-id="9fccf-157">Amount until Date</span></span>|<span data-ttu-id="9fccf-158">Saldo bis Datum</span><span class="sxs-lookup"><span data-stu-id="9fccf-158">Balance at Date</span></span>|<span data-ttu-id="9fccf-159">Posten</span><span class="sxs-lookup"><span data-stu-id="9fccf-159">Entries</span></span>|<span data-ttu-id="9fccf-160">Nettobetrag</span><span class="sxs-lookup"><span data-stu-id="9fccf-160">Net Amount</span></span>|<span data-ttu-id="9fccf-161">Immer</span><span class="sxs-lookup"><span data-stu-id="9fccf-161">Always</span></span>|  
    |<span data-ttu-id="9fccf-162">C30</span><span class="sxs-lookup"><span data-stu-id="9fccf-162">C30</span></span>|<span data-ttu-id="9fccf-163">Gesamtes Geschäftsjahr</span><span class="sxs-lookup"><span data-stu-id="9fccf-163">Entire Fiscal Year</span></span>|<span data-ttu-id="9fccf-164">Gesamtes Geschäftsjahr</span><span class="sxs-lookup"><span data-stu-id="9fccf-164">Entire Fiscal Year</span></span>|<span data-ttu-id="9fccf-165">Posten</span><span class="sxs-lookup"><span data-stu-id="9fccf-165">Entries</span></span>|<span data-ttu-id="9fccf-166">Nettobetrag</span><span class="sxs-lookup"><span data-stu-id="9fccf-166">Net Amount</span></span>|<span data-ttu-id="9fccf-167">Immer</span><span class="sxs-lookup"><span data-stu-id="9fccf-167">Always</span></span>|  

4.  <span data-ttu-id="9fccf-168">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="9fccf-168">Choose the **OK** button.</span></span>  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="9fccf-169">Das Spaltenlayout dem Kontenschemanamen zuweisen</span><span class="sxs-lookup"><span data-stu-id="9fccf-169">Assigning the Column Layout to the Account Schedule Name</span></span>  
<span data-ttu-id="9fccf-170">Ken kann das Spaltenlayout jetzt dem Kontenschemanamen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="9fccf-170">Ken is now ready to assign the column layout to the account schedule name.</span></span>  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="9fccf-171">Das Spaltenlayout dem Kontenschemanamen zuweisen:</span><span class="sxs-lookup"><span data-stu-id="9fccf-171">To assign the column layout to the account schedule name</span></span>  

1.  <span data-ttu-id="9fccf-172">Wählen Sie auf der Seite **Kontoschemanamen** die **Planung**  im Feld **Name** aus.</span><span class="sxs-lookup"><span data-stu-id="9fccf-172">On the **Account Schedule Names** page, select **Forecast** in the **Name** field.</span></span>  
2.  <span data-ttu-id="9fccf-173">Wählen Sie im Feld **Standardspaltenlayout** das Spaltenlayout **Cashflow** aus, um es als Standard-Spaltenlayout zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="9fccf-173">In the **Default Column Layout** field, choose the column layout **Cash Flow** to assign as the default column layout.</span></span>  

### <a name="to-view-and-print-the-cash-flow-forecast"></a><span data-ttu-id="9fccf-174">So können Sie die Cashflowplanung anzeigen und drucken</span><span class="sxs-lookup"><span data-stu-id="9fccf-174">To view and print the cash flow forecast</span></span>  
1.  <span data-ttu-id="9fccf-175">Wählen Sie auf der Seite **Kontoschemanamen** auf der Registerkarte **Übersicht** in der Gruppe Prozess die Option Übersicht aus, um die Cashflowplanung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9fccf-175">On the **Account Schedule Names** page, choose the **Overview** action to view the cash flow forecast.</span></span>  
2.  <span data-ttu-id="9fccf-176">Auf der Seite **Kontoschemaübersicht** können Sie einen Betrag auswählen und die Cashflowplanungs Posten dann anzeigen, aus denen sich der Betrag zusammensetzt.</span><span class="sxs-lookup"><span data-stu-id="9fccf-176">On the **Acc. Schedule Overview** page, you can select an amount and then view the cash flow forecast entries that make up the amount.</span></span> <span data-ttu-id="9fccf-177">Darüber hinaus können Sie die Formel anzeigen, die verwendet wird, um den Betrag zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="9fccf-177">In addition, you can view the formula that is used to calculate the amount.</span></span> <span data-ttu-id="9fccf-178">Sie können die Beträge auch nach Datum und Dimension filtern.</span><span class="sxs-lookup"><span data-stu-id="9fccf-178">You can also filter the amounts by date and dimension.</span></span>  
3.  <span data-ttu-id="9fccf-179">Wählen Sie die Aktion **Drucken** aus, um die Cashflowplanung zu drucken.</span><span class="sxs-lookup"><span data-stu-id="9fccf-179">Choose the **Print** action to print the cash flow forecast.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9fccf-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fccf-180">See Also</span></span>  
 <span data-ttu-id="9fccf-181">[Arbeiten mit Kontenschemata](bi-how-work-account-schedule.md) </span><span class="sxs-lookup"><span data-stu-id="9fccf-181">[Work with Account Schedules](bi-how-work-account-schedule.md) </span></span>  
 [<span data-ttu-id="9fccf-182">Exemplarische Vorgehensweisen für Geschäftsprozesse</span><span class="sxs-lookup"><span data-stu-id="9fccf-182">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="9fccf-183">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9fccf-183">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
