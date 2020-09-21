---
title: Übersicht über die Power BI-Integrationskomponente und -Architektur für Business Central | Microsoft Docs
description: Insight, Business Intelligence und KPIs aus Ihren Business Central Daten einfach beziehen mit der Business Central Anwendung für Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 9514f0355932c1b1cbd30acfdb9f6dab46db8a0a
ms.sourcegitcommit: aeaa0dc64e54432a70c4b0e1faf325cd17d01389
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697762"
---
# <a name="power-bi-integration-component-and-architecture-overview-for-prodshort"></a><span data-ttu-id="23470-103">Übersicht über die Power BI-Integrationskomponente und -Architektur für [!INCLUDE[prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="23470-103">Power BI Integration Component and Architecture Overview for [!INCLUDE[prodshort](includes/prodshort.md)]</span></span>

<span data-ttu-id="23470-104">In diesem Artikel erfahren Sie etwas über die verschiedenen Aspekte der Power BI-Integration mit [!INCLUDE[prodshort](includes/prodshort.md)], damit Sie die Implementierung und Verwendung besser verstehen.</span><span class="sxs-lookup"><span data-stu-id="23470-104">In this article, you'll learn about the different aspects of Power BI integration with [!INCLUDE[prodshort](includes/prodshort.md)] to help you understand its implementation and use.</span></span>

## <a name="components"></a><span data-ttu-id="23470-105">Komponenten</span><span class="sxs-lookup"><span data-stu-id="23470-105">Components</span></span>

<span data-ttu-id="23470-106">In der folgenden Tabelle werden die wichtigsten Komponenten der Power BI-Integration beschrieben.</span><span class="sxs-lookup"><span data-stu-id="23470-106">The following table describes the major components involved with Power BI integration.</span></span>

|<span data-ttu-id="23470-107">Komponente</span><span class="sxs-lookup"><span data-stu-id="23470-107">Component</span></span>|<span data-ttu-id="23470-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23470-108">Description</span></span>|
|---------|-----------|
|<span data-ttu-id="23470-109">Power BI</span><span class="sxs-lookup"><span data-stu-id="23470-109">Power BI</span></span>|<span data-ttu-id="23470-110">Ein cloudbasierter Hosting- und Verwaltungsdienst für Berichte.</span><span class="sxs-lookup"><span data-stu-id="23470-110">A cloud-based report hosting and management service.</span></span>|
|<span data-ttu-id="23470-111">Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="23470-111">Power BI Desktop</span></span>|<span data-ttu-id="23470-112">Ein Erstellungstool für Berichte und Dashboard, mit dem Sie Berichte ausführen können.</span><span class="sxs-lookup"><span data-stu-id="23470-112">An authoring tool for building reports and dashboards, and allows you to run reports.</span></span> <span data-ttu-id="23470-113">Es ist als kostenloser Download im Microsoft Store erhältlich und wird lokal installiert.</span><span class="sxs-lookup"><span data-stu-id="23470-113">It's available as a free download on Microsoft Store and is installed locally.</span></span>|
|[!INCLUDE[prodshort](includes/prodshort.md)]|<span data-ttu-id="23470-114">Dieses Tool ist als online oder lokale Lösung mit Connectors für Power BI erhältlich und kann als Power BI-Teil eingebettet werden.</span><span class="sxs-lookup"><span data-stu-id="23470-114">Online or on-premises solution with connectors exposed to Power BI and the ability to embed a Power BI part.</span></span>|

## <a name="whats-available-from-the-start"></a><span data-ttu-id="23470-115">Von Beginn an verfügbar</span><span class="sxs-lookup"><span data-stu-id="23470-115">What's available from the start</span></span>

<span data-ttu-id="23470-116">Die verfügbaren Funktionen werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="23470-116">The following table describes available features.</span></span>

|<span data-ttu-id="23470-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="23470-117">Feature</span></span>|<span data-ttu-id="23470-118">Support für [!INCLUDE[prodshort](includes/prodshort.md)] online oder on-premises</span><span class="sxs-lookup"><span data-stu-id="23470-118">[!INCLUDE[prodshort](includes/prodshort.md)] online or on-premises support</span></span>|
|-------|---------------------|
|<span data-ttu-id="23470-119">Power BI-Connectors</span><span class="sxs-lookup"><span data-stu-id="23470-119">Power BI connectors</span></span>|<span data-ttu-id="23470-120">Beide.</span><span class="sxs-lookup"><span data-stu-id="23470-120">Both.</span></span> <span data-ttu-id="23470-121">Verschiedene Connectors für online und on-premises.</span><span class="sxs-lookup"><span data-stu-id="23470-121">Different connectors for online and on-premises.</span></span> <span data-ttu-id="23470-122">Gleicher Connector für Power BI Desktop und Power BI-Dienst</span><span class="sxs-lookup"><span data-stu-id="23470-122">Same connector used for Power BI Desktop and Power BI Service</span></span> |
|<span data-ttu-id="23470-123">Eingebettete Erfahrung zum Anzeigen eines bestimmten Berichts in einer Infobox in [!INCLUDE[prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="23470-123">Embedded experience for viewing a given report inside a FactBox in [!INCLUDE[prodshort](includes/prodshort.md)]</span></span>|<span data-ttu-id="23470-124">Beide.</span><span class="sxs-lookup"><span data-stu-id="23470-124">Both.</span></span> <span data-ttu-id="23470-125">Erfordert eine Konfiguration zum Anzeigen von Berichten für lokale Version.</span><span class="sxs-lookup"><span data-stu-id="23470-125">Requires configuration to display reports for on-premises.</span></span>|
|<span data-ttu-id="23470-126">Power BI-Berichtsverwaltung über [!INCLUDE[prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="23470-126">Power BI report management from [!INCLUDE[prodshort](includes/prodshort.md)]</span></span>|<span data-ttu-id="23470-127">Online</span><span class="sxs-lookup"><span data-stu-id="23470-127">Online</span></span>|
|<span data-ttu-id="23470-128">Power BI-Standardberichte in Rollencentern bereitgestellt für Power BI</span><span class="sxs-lookup"><span data-stu-id="23470-128">Default Power BI reports on role centers deployed to Power BI</span></span>|<span data-ttu-id="23470-129">Online</span><span class="sxs-lookup"><span data-stu-id="23470-129">Online</span></span>|
|<span data-ttu-id="23470-130">Power BI-Apps auf Microsoft AppSource</span><span class="sxs-lookup"><span data-stu-id="23470-130">Power BI Apps on Microsoft AppSource</span></span>|<span data-ttu-id="23470-131">Online.</span><span class="sxs-lookup"><span data-stu-id="23470-131">Online.</span></span>|

## <a name="architecture"></a><span data-ttu-id="23470-132">Architektur</span><span class="sxs-lookup"><span data-stu-id="23470-132">Architecture</span></span>

[!INCLUDE[prodshort](includes/prodshort.md)] <span data-ttu-id="23470-133">wird über einen Connector mithilfe von OData mit Power BI integriert.</span><span class="sxs-lookup"><span data-stu-id="23470-133">integrates with Power BI through a connector using OData.</span></span> <span data-ttu-id="23470-134">Die Datenquelle für Power BI-Berichte wird in der Form von OData-Webdiensten zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="23470-134">The data source for Power BI reports is exposed as OData web services.</span></span>

![Power BI-Architektur für die Integration mit Business Central](./media/power-bi-architecture.png)

## <a name="general-flow"></a><span data-ttu-id="23470-136">Allgemeiner Ablauf</span><span class="sxs-lookup"><span data-stu-id="23470-136">General Flow</span></span>

<span data-ttu-id="23470-137">Das folgende Diagramm zeigt den grundlegenden Workflow für Benutzer beim Herstellen einer Verbindung zwischen [!INCLUDE[prodshort](includes/prodshort.md)] und Power BI.</span><span class="sxs-lookup"><span data-stu-id="23470-137">The following diagram illustrates the basic workflow for users when connecting [!INCLUDE[prodshort](includes/prodshort.md)] to Power BI.</span></span>

![Power BI-Workflow für die Integration mit Business Central](./media/power-bi-flow.png)

1. <span data-ttu-id="23470-139">Der Benutzer registriert sich für ein Power BI-Konto.</span><span class="sxs-lookup"><span data-stu-id="23470-139">User signs up for a Power BI account.</span></span>
2. <span data-ttu-id="23470-140">Der Benutzer stellt eine Verbindung zwischen Power BI und [!INCLUDE[prodshort](includes/prodshort.md)] her.</span><span class="sxs-lookup"><span data-stu-id="23470-140">User connects to Power BI from [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>
3. [!INCLUDE[prodshort](includes/prodshort.md)] <span data-ttu-id="23470-141">überprüft die Lizenz.</span><span class="sxs-lookup"><span data-stu-id="23470-141">verifies the license.</span></span>
4. [!INCLUDE[prodshort](includes/prodshort.md)] <span data-ttu-id="23470-142">stellt Standardberichte für den Power BI-Dienst.</span><span class="sxs-lookup"><span data-stu-id="23470-142">deploys default reports to the Power BI service.</span></span> <span data-ttu-id="23470-143">Dieser Schritt ist nur für [!INCLUDE[prodshort](includes/prodshort.md)] online relevant.</span><span class="sxs-lookup"><span data-stu-id="23470-143">This step only happens for [!INCLUDE[prodshort](includes/prodshort.md)] online.</span></span>
5. [!INCLUDE[prodshort](includes/prodshort.md)] <span data-ttu-id="23470-144">stellt Berichte in Power BI zur Auswahl in [!INCLUDE[prodshort](includes/prodshort.md)] zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="23470-144">makes reports in Power BI available for selection in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="23470-145">Standardberichte werden automatisch in Power BI-Teilen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="23470-145">Default reports are automatically displayed in Power BI parts.</span></span>
6. <span data-ttu-id="23470-146">Der Benutzer erstellt einen Bericht in Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="23470-146">User creates a report in Power BI Desktop.</span></span>
7. <span data-ttu-id="23470-147">Der Benutzer veröffentlicht den Bericht für den Power BI-Dienst.</span><span class="sxs-lookup"><span data-stu-id="23470-147">User publishes the report to the Power BI service.</span></span> <span data-ttu-id="23470-148">Die Berichte können dann in [!INCLUDE[prodshort](includes/prodshort.md)] ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="23470-148">The reports are then available for selection in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="23470-149">Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="23470-149">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="23470-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23470-150">See Also</span></span>

[<span data-ttu-id="23470-151">Business Central und Power BI</span><span class="sxs-lookup"><span data-stu-id="23470-151">Business Central and Power BI</span></span>](admin-powerbi.md)  
[<span data-ttu-id="23470-152">Power BI für Verbraucher</span><span class="sxs-lookup"><span data-stu-id="23470-152">Power BI for consumers</span></span>](/power-bi/consumer/end-user-consumer)  
[<span data-ttu-id="23470-153">Der „neue Look“ des Power BI Service</span><span class="sxs-lookup"><span data-stu-id="23470-153">The 'new look' of the Power BI service</span></span>](/power-bi/service-new-look)  
[<span data-ttu-id="23470-154">Schnellstart: Stellen Sie eine Verbindung zu Daten her in Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="23470-154">Quickstart: Connect to data in Power BI Desktop</span></span>](/power-bi/desktop-quickstart-connect-to-data)  
[<span data-ttu-id="23470-155">Power BI Dokumentation</span><span class="sxs-lookup"><span data-stu-id="23470-155">Power BI documentation</span></span>](/power-bi/)  
[<span data-ttu-id="23470-156">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="23470-156">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="23470-157">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="23470-157">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="23470-158">Geschäftsdaten aus anderen Finanzsystemen importieren</span><span class="sxs-lookup"><span data-stu-id="23470-158">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="23470-159">[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="23470-159">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
<span data-ttu-id="23470-160">[Verwenden von [!INCLUDE[d365fin](includes/d365fin_md.md)] als Power BI-Datenquelle](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="23470-160">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
<span data-ttu-id="23470-161">[Verwenden von [!INCLUDE[d365fin](includes/d365fin_md.md)] als Power Apps-Datenquelle](across-how-use-financials-data-source-powerapps.md)</span><span class="sxs-lookup"><span data-stu-id="23470-161">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] as a Power Apps Data Source](across-how-use-financials-data-source-powerapps.md)</span></span>  
<span data-ttu-id="23470-162">[Verwenden von [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power Automate](across-how-use-financials-data-source-flow.md)</span><span class="sxs-lookup"><span data-stu-id="23470-162">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power Automate](across-how-use-financials-data-source-flow.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
