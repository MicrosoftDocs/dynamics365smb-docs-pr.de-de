---
title: Business Central und Power BI Inhaltspakete verbinden | Microsoft Docs
description: Nutzen Sie Einblicke in Business Central mit Power BI und dem Business Central-Inhaltspaket.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 03/16/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 315d4b188cdd834e82676a0c5ef77272ad873eb7
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="connecting-power-bi-to-business-central-content-packs"></a><span data-ttu-id="953d3-103">Power BI mit den Business Central Inhaltspakenten verbinden</span><span class="sxs-lookup"><span data-stu-id="953d3-103">Connecting Power BI to Business Central Content Packs</span></span>
<span data-ttu-id="953d3-104">Einblicke in Ihre Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Daten zu erhalten ist mit Power BI und dem Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Inhaltspaket sehr einfach.</span><span class="sxs-lookup"><span data-stu-id="953d3-104">Getting insights into your Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data is easy with Power BI and the Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] content packs.</span></span> <span data-ttu-id="953d3-105">Power BI ruft die Daten ab und erstellt ein Standarddashboard und Berichte auf Grundlage der Daten.</span><span class="sxs-lookup"><span data-stu-id="953d3-105">Power BI retrieves your data then builds an out-of-the-box dashboard and reports based on that data.</span></span>

> [!NOTE]  
>  <span data-ttu-id="953d3-106">Sie müssen ein gültiges Konto mit [!INCLUDE[d365fin](includes/d365fin_md.md)] mit Power BI haben.</span><span class="sxs-lookup"><span data-stu-id="953d3-106">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Power BI.</span></span> <span data-ttu-id="953d3-107">Zudem müssen Sie [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) herunterladen.</span><span class="sxs-lookup"><span data-stu-id="953d3-107">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span></span>  
>  <span data-ttu-id="953d3-108">Power BI Inhaltpakete benötigen Berechtigungen für die Tabellen, aus denen Daten abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="953d3-108">Power BI content packs require permissions to the tables where data is retrieved from.</span></span> <span data-ttu-id="953d3-109">Weitere Einzelheiten auf den Anforderungen werden im Folgenden beschrieben.</span><span class="sxs-lookup"><span data-stu-id="953d3-109">More details on the requirements are described below.</span></span>  

## <a name="how-to-connect"></a><span data-ttu-id="953d3-110">So stellen Sie die Verbindung her</span><span class="sxs-lookup"><span data-stu-id="953d3-110">How to Connect</span></span>
1. <span data-ttu-id="953d3-111">Wählen Sie **Daten abrufen** am unteren Rand des linken Navigationsbereich aus.</span><span class="sxs-lookup"><span data-stu-id="953d3-111">Select **Get Data** at the bottom of the left navigation pane.</span></span>  
<span data-ttu-id="953d3-112">![Navigieren, um die Daten zu erhalten](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span><span class="sxs-lookup"><span data-stu-id="953d3-112">![Navigating to Get Data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span></span>
2. <span data-ttu-id="953d3-113">Im Feld **Dienste** wählen Sie **Abrufen** aus.</span><span class="sxs-lookup"><span data-stu-id="953d3-113">In the **Services** box, select **Get**.</span></span> <span data-ttu-id="953d3-114">Dadurch wird ein Fenster mit **AppSource** und **Apps für Power BI Apps** geöffnet.</span><span class="sxs-lookup"><span data-stu-id="953d3-114">This will open a window with the **AppSource** and **Apps for Power BI apps**.</span></span>  
<span data-ttu-id="953d3-115">![Wählen Sie Inhaltspakete von Onlinediensten aus](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span><span class="sxs-lookup"><span data-stu-id="953d3-115">![Choose content packs from online services](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span></span>
3. <span data-ttu-id="953d3-116">Wählen Sie **Apps** auf der Registerkarte **Apps für Power BI Apps**, und wählen Sie das Feld **Microsoft Dynamics 365 Business Central** Inhaltspakete, die Sie verwenden möchten, und wählen Sie dann **jetzt abrufen**.</span><span class="sxs-lookup"><span data-stu-id="953d3-116">Select **Apps** from the **Apps for Power BI apps** tab, and choose the **Microsoft Dynamics 365 Business Central** content pack that you want to use, and then select **Get it now**.</span></span>  
<span data-ttu-id="953d3-117">![Wählen Sie Dynamics 365 Business Central und wählen Sie "Jetzt abrufen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span><span class="sxs-lookup"><span data-stu-id="953d3-117">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span></span>
4. <span data-ttu-id="953d3-118">Wenn Sie dazu aufgefordert werden, geben Sie in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] den Namen des *Unternehmens* ein.</span><span class="sxs-lookup"><span data-stu-id="953d3-118">When prompted, enter the name of *your company* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="953d3-119">Dies ist nicht der Anzeigename.</span><span class="sxs-lookup"><span data-stu-id="953d3-119">This is not the display name.</span></span>  
<span data-ttu-id="953d3-120">![Wählen Sie Dynamics 365 Business Central und wählen Sie jetzt abrufen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span><span class="sxs-lookup"><span data-stu-id="953d3-120">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span></span>
5. <span data-ttu-id="953d3-121">Sobald verbunden, werden ein Dashboard, ein Bericht und ein Datensatz automatisch in Ihren Power BI Arbeitsbereich geladen.</span><span class="sxs-lookup"><span data-stu-id="953d3-121">Once connected, a dashboard, report and dataset will automatically be loaded into your Power BI workspace.</span></span> <span data-ttu-id="953d3-122">Wenn abgeschlossen werden die Kacheln die Daten aus dem Konto aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="953d3-122">When completed, the tiles will update with data from your account.</span></span>
<span data-ttu-id="953d3-123">![Wählen Sie Dynamics 365 Business Central und wählen Sie jetzt abrufen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span><span class="sxs-lookup"><span data-stu-id="953d3-123">![Select Dynamics 365 Business Central  and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span></span>

## <a name="what-now"></a><span data-ttu-id="953d3-124">Was jetzt?</span><span class="sxs-lookup"><span data-stu-id="953d3-124">What Now?</span></span>

- <span data-ttu-id="953d3-125">[Ändern Sie die Kacheln](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) im Dashboard.</span><span class="sxs-lookup"><span data-stu-id="953d3-125">[Change the tiles](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) in the dashboard.</span></span>  
- <span data-ttu-id="953d3-126">[Wählen Sie eine Kachel aus](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles), um den zu Grunde liegenden Bericht zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="953d3-126">[Select a tile](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) to open the underlying report.</span></span>  
- <span data-ttu-id="953d3-127">Während Ihr Dataset täglich aktualisiert wird, können Sie den Aktualisierungsplan ändern oder ihn mithilfe von **jetzt aktualisieren** bei Bedarf aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="953d3-127">While your dataset will be scheduled to refreshed daily, you can change the refresh schedule or try refreshing it on demand using **Refresh Now**.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="953d3-128">Systemanforderungen</span><span class="sxs-lookup"><span data-stu-id="953d3-128">System Requirements</span></span>
<span data-ttu-id="953d3-129">Um die Daten [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] in Power BI zu importieren, müssen Sie Berechtigungen für den Webdiensten haben, um die Daten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="953d3-129">To import your [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data into Power BI, you need to have permissions to the web services used to retrieve data.</span></span> <span data-ttu-id="953d3-130">Die Web Services, die für jedes Inhaltspakete erforderlich sind:</span><span class="sxs-lookup"><span data-stu-id="953d3-130">The web services required for each content pack include:</span></span>

<span data-ttu-id="953d3-131">**Microsoft Dynamics 365 Business Central – CRM**</span><span class="sxs-lookup"><span data-stu-id="953d3-131">**Microsoft Dynamics 365 Business Central – CRM**</span></span>
- <span data-ttu-id="953d3-132">SalesOpportunities</span><span class="sxs-lookup"><span data-stu-id="953d3-132">SalesOpportunities</span></span>
- <span data-ttu-id="953d3-133">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="953d3-133">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="953d3-134">**Microsoft Dynamics 365 Business Central – Sales**</span><span class="sxs-lookup"><span data-stu-id="953d3-134">**Microsoft Dynamics 365 Business Central – Sales**</span></span>
- <span data-ttu-id="953d3-135">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="953d3-135">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="953d3-136">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="953d3-136">SalesDashboard</span></span>
- <span data-ttu-id="953d3-137">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="953d3-137">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="953d3-138">**Microsoft Dynamics 365 Business Central – Finance**</span><span class="sxs-lookup"><span data-stu-id="953d3-138">**Microsoft Dynamics 365 Business Central – Finance**</span></span>
- <span data-ttu-id="953d3-139">PowerBIFinance</span><span class="sxs-lookup"><span data-stu-id="953d3-139">PowerBIFinance</span></span>
- <span data-ttu-id="953d3-140">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="953d3-140">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="953d3-141">**Microsoft Dynamics 365 Business Central – Jobs**</span><span class="sxs-lookup"><span data-stu-id="953d3-141">**Microsoft Dynamics 365 Business Central – Jobs**</span></span>
- <span data-ttu-id="953d3-142">Projektübersicht</span><span class="sxs-lookup"><span data-stu-id="953d3-142">Job List</span></span>
- <span data-ttu-id="953d3-143">Projektplanzeilen</span><span class="sxs-lookup"><span data-stu-id="953d3-143">Job Planning Lines</span></span>
- <span data-ttu-id="953d3-144">Projektaufgabenzeilen</span><span class="sxs-lookup"><span data-stu-id="953d3-144">Job Task Lines</span></span>

<span data-ttu-id="953d3-145">**Microsoft Dynamics 365 Business Central – Customers List**</span><span class="sxs-lookup"><span data-stu-id="953d3-145">**Microsoft Dynamics 365 Business Central – Customers List**</span></span>
- <span data-ttu-id="953d3-146">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="953d3-146">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="953d3-147">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="953d3-147">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="953d3-148">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="953d3-148">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="953d3-149">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="953d3-149">SalesDashboard</span></span>
- <span data-ttu-id="953d3-150">Power_BI_Customer_List</span><span class="sxs-lookup"><span data-stu-id="953d3-150">Power_BI_Customer_List</span></span>
- <span data-ttu-id="953d3-151">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="953d3-151">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="953d3-152">**Microsoft Dynamics 365 Business Central – Items List**</span><span class="sxs-lookup"><span data-stu-id="953d3-152">**Microsoft Dynamics 365 Business Central – Items List**</span></span>
- <span data-ttu-id="953d3-153">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="953d3-153">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="953d3-154">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="953d3-154">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="953d3-155">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="953d3-155">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="953d3-156">Artikel</span><span class="sxs-lookup"><span data-stu-id="953d3-156">Items</span></span>
- <span data-ttu-id="953d3-157">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="953d3-157">SalesDashboard</span></span>
- <span data-ttu-id="953d3-158">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="953d3-158">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="953d3-159">**Microsoft Dynamics 365 Business Central – Vendors List**</span><span class="sxs-lookup"><span data-stu-id="953d3-159">**Microsoft Dynamics 365 Business Central – Vendors List**</span></span>
- <span data-ttu-id="953d3-160">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="953d3-160">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="953d3-161">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="953d3-161">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="953d3-162">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="953d3-162">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="953d3-163">Artikel</span><span class="sxs-lookup"><span data-stu-id="953d3-163">Items</span></span>
- <span data-ttu-id="953d3-164">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="953d3-164">SalesDashboard</span></span>
- <span data-ttu-id="953d3-165">Power_BI_Customer_List</span><span class="sxs-lookup"><span data-stu-id="953d3-165">Power_BI_Customer_List</span></span>
- <span data-ttu-id="953d3-166">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="953d3-166">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="953d3-167">Power_BI_Vendor_List</span><span class="sxs-lookup"><span data-stu-id="953d3-167">Power_BI_Vendor_List</span></span>
- <span data-ttu-id="953d3-168">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="953d3-168">ExcelTemplateViewCompany</span></span>

## <a name="web-services"></a><span data-ttu-id="953d3-169">Webdienste</span><span class="sxs-lookup"><span data-stu-id="953d3-169">Web Services</span></span>
<span data-ttu-id="953d3-170">Eine einfache Methode, die Webdienste zu finden ist, in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] nach Webdiensten zu suchen.</span><span class="sxs-lookup"><span data-stu-id="953d3-170">An easy way to find the web services is to search for web services in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="953d3-171">In der Übersicht stellen Sie sicher, dass das Veröffentlichungsfeld für die oben aufgeführten Webdienste markiert wird.</span><span class="sxs-lookup"><span data-stu-id="953d3-171">In the list make sure the Publish box is marked for the web services listed above.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="953d3-172">Problembehebung</span><span class="sxs-lookup"><span data-stu-id="953d3-172">Troubleshooting</span></span>
<span data-ttu-id="953d3-173">Das Power BI-Dashboard beruht auf den veröffentlichten Webdiensten, die oben erwähnten werden. Es enthält Daten vom Demomandanten oder von Ihrem eigenen Unternehmen wenn Sie Daten aus der aktuellen Finanzlösung importieren.</span><span class="sxs-lookup"><span data-stu-id="953d3-173">The Power BI dashboard relies on the published web services that are listed above, and it will show data from the demonstration company or your own company if you import data from your current finance solution.</span></span> <span data-ttu-id="953d3-174">Wenn etwas schief geht, stellt dieser Abschnitt eine Problemumgehung für die häufigsten Probleme bereit.</span><span class="sxs-lookup"><span data-stu-id="953d3-174">However, if something goes wrong, this section provides a workaround for the most typical issues.</span></span>

### <a name="incorrect-company-name"></a><span data-ttu-id="953d3-175">Ungültiger Unternehmensnamen</span><span class="sxs-lookup"><span data-stu-id="953d3-175">Incorrect Company Name</span></span>  
<span data-ttu-id="953d3-176">Ein häufiger Fehler ist, den Unternehmensanzeigenamen anstelle des Unternehmensnamens einzugeben.</span><span class="sxs-lookup"><span data-stu-id="953d3-176">A common mistake is to enter the company display name instead of the company name.</span></span> <span data-ttu-id="953d3-177">Unternehmensnamensuche für **Unternehmen** zu suchen.</span><span class="sxs-lookup"><span data-stu-id="953d3-177">To find the company name search for **Companies**.</span></span> <span data-ttu-id="953d3-178">Verwenden Sie das Feld **Name**, wenn Sie den Unternehmensnamen eingeben.</span><span class="sxs-lookup"><span data-stu-id="953d3-178">Then use the **Name** field when entering your company name.</span></span>

### <a name="incorrect-user-name-and-password"></a><span data-ttu-id="953d3-179">Falscher Benutzername und Kennwort</span><span class="sxs-lookup"><span data-stu-id="953d3-179">Incorrect User Name and Password</span></span>  
<span data-ttu-id="953d3-180">Der Benutzername und das Kennwort, die zum Verbinden verwendet werden, sind dieselben, die verwendet werden, um die Verbindung mit Ihrem  Microsoft Office 365 Konto herzustellen.</span><span class="sxs-lookup"><span data-stu-id="953d3-180">The user name and password used to connect will be the same as what is used to connect to your Microsoft Office 365 account.</span></span>  

<span data-ttu-id="953d3-181">Die Inhaltspakete erfordern, dass Sie ein Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Konto haben.</span><span class="sxs-lookup"><span data-stu-id="953d3-181">The content packs also require that you have a Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account.</span></span> <span data-ttu-id="953d3-182">Nachdem Sie Ihre Anmeldeinformationen eingeben haben, erkennen wir sämtliche Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Tenants, auf die Sie Zugriff haben.</span><span class="sxs-lookup"><span data-stu-id="953d3-182">Once you enter your credentials, we will auto discover any Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] tenants you have access to.</span></span> <span data-ttu-id="953d3-183">Wenn Sie kein lizenziertes oder Probe-Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Konto haben, erhalten Sie eine Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="953d3-183">If you do not have a licensed or trial Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account, you will receive an error message.</span></span>

### <a name="the-key-didnt-match-any-rows-in-the-table"></a><span data-ttu-id="953d3-184">Der Schlüssel glich keinen Zeilen in der Tabelle</span><span class="sxs-lookup"><span data-stu-id="953d3-184">The Key Didn't Match Any Rows in the Table</span></span>
<span data-ttu-id="953d3-185">Wenn Sie einen nicht gültigen Unternehmensnamen während des Verbindungsvorgangs eingeben, erhalten Sie möglicherweise die Fehlermeldung, "der Schlüssel entsprach keinen Zeilen in der Tabelle".</span><span class="sxs-lookup"><span data-stu-id="953d3-185">If you enter a non valid company name during the connection process, you may get the error message "The key didn't match any rows in the table".</span></span> <span data-ttu-id="953d3-186">Geben Sie den korrekten Unternehmensnamen an und versuchen Sie die Verbindung erneut.</span><span class="sxs-lookup"><span data-stu-id="953d3-186">Provide the correct company name and try connecting again.</span></span>

## <a name="see-also"></a><span data-ttu-id="953d3-187">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="953d3-187">See Also</span></span>
[<span data-ttu-id="953d3-188">Erste Schritte mit Power BI</span><span class="sxs-lookup"><span data-stu-id="953d3-188">Get started with Power BI</span></span>](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
<span data-ttu-id="953d3-189">[Power BI - Grundmodelle](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Business Intelligence](bi.md)</span><span class="sxs-lookup"><span data-stu-id="953d3-189">[Power BI - Basic Concepts](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Business Intelligence](bi.md)</span></span>  
<span data-ttu-id="953d3-190">[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="953d3-190">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="953d3-191">Geschäftsdaten aus anderen Finanzsystemen importieren</span><span class="sxs-lookup"><span data-stu-id="953d3-191">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="953d3-192">[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="953d3-192">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="953d3-193">Finanzen</span><span class="sxs-lookup"><span data-stu-id="953d3-193">Finance</span></span>](finance.md)  
<span data-ttu-id="953d3-194">[Einrichtungs-Berichterstellugn für [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="953d3-194">[Setup Reporting for [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)</span></span>  

