---
title: 'So geht es: Ein neues Unternehmen erstellen | Microsoft Docs'
description: Um RapidStart Services zu verwenden, werden Tabellen und Seiten erstellt, aber sie enthalten keine Daten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 1f176fb0e9d72d948d26d041f417554949087b68
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783662"
---
# <a name="create-a-new-company"></a><span data-ttu-id="c1dcb-103">Erstellen eines neuen Mandanten.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-103">Create a New Company</span></span>
<span data-ttu-id="c1dcb-104">Um RapidStart Services für [!INCLUDE[d365fin](includes/d365fin_md.md)] zu verwenden, müssen Sie zunächst einen neuen Mandanten erstellen, für den Sie eine Debitoren-Implementierung durchführen wollen.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-104">To use RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], you first create a new company for which you want to perform a customer implementation.</span></span> <span data-ttu-id="c1dcb-105">Bei der Erstellung eines neuen Mandanten werden die [!INCLUDE[d365fin](includes/d365fin_md.md)]-Standardtabellen und -seiten erstellt, aber sie enthalten keine Daten.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-105">When you create a new company, the standard [!INCLUDE[d365fin](includes/d365fin_md.md)] tables and pages are created, but there is no data in them.</span></span>

<span data-ttu-id="c1dcb-106">Darüber hinaus können Sie bestimmte Einrichtungsdaten bei Ihrem Unternehmen anwenden, nachdem Sie es initialisiert haben.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-106">In addition, you can apply specific setup data to your company after you initialize it.</span></span> <span data-ttu-id="c1dcb-107">Die Informationen werden in einem Konfigurationspaket, eine .rapidstart-Datei bereitgestellt, die Inhalt in einem komprimierten Format bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-107">The information is provided in a configuration package, a .rapidstart file, which delivers content in a compressed format.</span></span>  

<span data-ttu-id="c1dcb-108">Beispielkonfigurationspakete, einschließlich landes-/regionspezifischer Dateien, sind im CRONUS-Demounternehmen enthalten.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-108">Example configuration packages, including country/region-specific files, are included with the CRONUS demonstration company.</span></span> <span data-ttu-id="c1dcb-109">Verwenden Sie die folgende Vorgehensweisen, um das Beispielkonfigurationspaket mit einem neuen Mandanten zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-109">Use the following procedures to use the example configuration package with a new company.</span></span>  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a><span data-ttu-id="c1dcb-110">Beispielskonfigurationspaket BASICCONFIG verwenden</span><span class="sxs-lookup"><span data-stu-id="c1dcb-110">To use the sample BASICCONFIG configuration package</span></span>  
1. <span data-ttu-id="c1dcb-111">Öffnen Sie das Unternehmen „CRONUS International Ltd.“.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-111">Open the CRONUS International Ltd. company.</span></span> <span data-ttu-id="c1dcb-112">Weitere Informationen finden Sie unter [Ändern der Grundeinstellungen](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="c1dcb-112">For more information, see [Change Basic Settings](ui-change-basic-settings.md).</span></span>
2. <span data-ttu-id="c1dcb-113">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Konfigurationspakete** ein, und wählen Sie dann den zugehörigen Link.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Configuration Packages**, and then choose the related link.</span></span>  
3. <span data-ttu-id="c1dcb-114">Wählen Sie das BASICCONFIG-Paket von der Liste aus, und wählen **Exportpaket**.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-114">Choose the BASICCONFIG package from the list, and then choose the **Export Package** action.</span></span>  

<span data-ttu-id="c1dcb-115">Verwenden Sie das folgende Vorgehen, um einen neuen Mandanten zu erstellen, und verwenden Sie das BASICCONFIG-Paket als Teil des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-115">Use the following procedure to create a new company, and use the BASICCONFIG package as part of the process.</span></span>  

## <a name="to-create-a-new-company"></a><span data-ttu-id="c1dcb-116">So erstellen Sie einen neuen Mandanten:</span><span class="sxs-lookup"><span data-stu-id="c1dcb-116">To create a new company</span></span>  
1. <span data-ttu-id="c1dcb-117">Erstellen eines neuen Mandanten.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-117">Create a new company.</span></span> <span data-ttu-id="c1dcb-118">Weitere Informationen finden Sie unter [Neue Mandanten erstellen in [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="c1dcb-118">For more information, see [Creating New Companies in [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).</span></span>
2. <span data-ttu-id="c1dcb-119">Vom RapidStart Services-Implementierungs-Rollencenter können Sie das Konfigurationspaket jetzt importieren, das Sie aus CRONUS International Ltd. exportierten.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-119">From the RapidStart Services Implementer Role Center, you can now import the configuration package that you exported from the CRONUS International Ltd. company.</span></span>

<span data-ttu-id="c1dcb-120">Nachdem Sie ein neues Unternehmen erstellt haben, werden einige Tabellen automatisch ausgefüllt, auch wenn keine Unternehmensvorlage angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-120">After you create a new company, some tables are automatically filled in, even if no company template is applied.</span></span> <span data-ttu-id="c1dcb-121">Beispielsweise können Sie die Standardcodes für Buchungen und Stapeltransaktionen auf der Seite **Quellencode** prüfen.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-121">For example, you can review the standard codes for posting and batch transactions on the **Source Code** page.</span></span> <span data-ttu-id="c1dcb-122">Wenn Sie eine lokale Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] zur Verfügung stellen, sollten Sie diese Tabelle prüfen und auf sämtliche lokale sprachliche Aspekte achten.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-122">If you provide a local version of [!INCLUDE[d365fin](includes/d365fin_md.md)], you should review this table and consider any local language issues.</span></span>

## <a name="about-data-tables"></a><span data-ttu-id="c1dcb-123">Info zu Datentabellen</span><span class="sxs-lookup"><span data-stu-id="c1dcb-123">About Data Tables</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]  <span data-ttu-id="c1dcb-124">Datentabellen liegen in zwei Haupttypen vor: Master und Einrichtung.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-124">, data tables come in two basic types: Master and Setup.</span></span> <span data-ttu-id="c1dcb-125">Wenn Sie eine Mandantkonfiguration erstellen, können Sie diese Arten verwenden, um Ihre Konfigurationsstrategie zu konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-125">When you are setting up a company configuration, you can use these types to focus your configuration strategy.</span></span>  

### <a name="master-data-tables"></a><span data-ttu-id="c1dcb-126">Stammdatentabellen</span><span class="sxs-lookup"><span data-stu-id="c1dcb-126">Master Data Tables</span></span>  
<span data-ttu-id="c1dcb-127">In der folgenden Tabelle sind einige Bespiele für -Stammdatentabellen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-127">The following table lists some of the master data tables.</span></span> <span data-ttu-id="c1dcb-128">Wenn Sie einen neuen Mandanten initialisieren, sind diese Tabellen leer.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-128">When you initialize a new company, these tables are empty.</span></span>  

|<span data-ttu-id="c1dcb-129">Tabellennr.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-129">Table No.</span></span>|<span data-ttu-id="c1dcb-130">Tabellenname</span><span class="sxs-lookup"><span data-stu-id="c1dcb-130">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="c1dcb-131">15</span><span class="sxs-lookup"><span data-stu-id="c1dcb-131">15</span></span>|<span data-ttu-id="c1dcb-132">Sachkonto</span><span class="sxs-lookup"><span data-stu-id="c1dcb-132">G/L Account</span></span>|  
|<span data-ttu-id="c1dcb-133">18</span><span class="sxs-lookup"><span data-stu-id="c1dcb-133">18</span></span>|<span data-ttu-id="c1dcb-134">Debitor</span><span class="sxs-lookup"><span data-stu-id="c1dcb-134">Customer</span></span>|  
|<span data-ttu-id="c1dcb-135">23</span><span class="sxs-lookup"><span data-stu-id="c1dcb-135">23</span></span>|<span data-ttu-id="c1dcb-136">Kreditor</span><span class="sxs-lookup"><span data-stu-id="c1dcb-136">Vendor</span></span>|  
|<span data-ttu-id="c1dcb-137">27</span><span class="sxs-lookup"><span data-stu-id="c1dcb-137">27</span></span>|<span data-ttu-id="c1dcb-138">Option</span><span class="sxs-lookup"><span data-stu-id="c1dcb-138">Item</span></span>|  
|<span data-ttu-id="c1dcb-139">5050</span><span class="sxs-lookup"><span data-stu-id="c1dcb-139">5050</span></span>|<span data-ttu-id="c1dcb-140">Kontakt</span><span class="sxs-lookup"><span data-stu-id="c1dcb-140">Contact</span></span>|  

### <a name="setup-data-tables"></a><span data-ttu-id="c1dcb-141">Einrichtungsdatentabellen</span><span class="sxs-lookup"><span data-stu-id="c1dcb-141">Setup Data Tables</span></span>  
<span data-ttu-id="c1dcb-142">Die folgende Tabelle enthält Beispiele für Einrichtungsdatentabellen, in denen Sie Einrichtungsinformationen im Konfigurationsfragebogen erfassen.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-142">The following table lists some of the setup data tables, in which you capture setup information in the configuration questionnaire.</span></span> <span data-ttu-id="c1dcb-143">Diese Tabellen enthalten Basisinformationen, wenn der Mandant erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-143">These tables contain baseline information when the company is created.</span></span>  

|<span data-ttu-id="c1dcb-144">Tabellennr.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-144">Table No.</span></span>|<span data-ttu-id="c1dcb-145">Tabellenname</span><span class="sxs-lookup"><span data-stu-id="c1dcb-145">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="c1dcb-146">98</span><span class="sxs-lookup"><span data-stu-id="c1dcb-146">98</span></span>|<span data-ttu-id="c1dcb-147">Finanzbuchhaltungs-Einrichtung:</span><span class="sxs-lookup"><span data-stu-id="c1dcb-147">General Ledger Setup</span></span>|  
|<span data-ttu-id="c1dcb-148">311</span><span class="sxs-lookup"><span data-stu-id="c1dcb-148">311</span></span>|<span data-ttu-id="c1dcb-149">Debitoren & Verkauf Einr.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-149">Sales & Receivables Setup</span></span>|  
|<span data-ttu-id="c1dcb-150">312</span><span class="sxs-lookup"><span data-stu-id="c1dcb-150">312</span></span>|<span data-ttu-id="c1dcb-151">Kreditoren & Einkauf Einr.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-151">Purchases & Payables Setup</span></span>|  
|<span data-ttu-id="c1dcb-152">313</span><span class="sxs-lookup"><span data-stu-id="c1dcb-152">313</span></span>|<span data-ttu-id="c1dcb-153">Lagereinrichtung</span><span class="sxs-lookup"><span data-stu-id="c1dcb-153">Inventory Setup</span></span>|  

<span data-ttu-id="c1dcb-154">Zusätzlich zu den Einrichtungsdatentabellen hat [!INCLUDE[d365fin](includes/d365fin_md.md)] auch Datentabellen, die Kernangaben zu dem Unternehmen und seinen Geschäftsprozesse enthalten.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-154">In addition to setup data tables, [!INCLUDE[d365fin](includes/d365fin_md.md)] also has setup-type data tables that specify core information about the company and its business processes.</span></span> <span data-ttu-id="c1dcb-155">In der folgenden Tabelle werden einige dieser Felder aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="c1dcb-155">The following table lists some of them.</span></span>  

|<span data-ttu-id="c1dcb-156">Tabellennr.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-156">Table No.</span></span>|<span data-ttu-id="c1dcb-157">Tabellenname</span><span class="sxs-lookup"><span data-stu-id="c1dcb-157">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="c1dcb-158">3</span><span class="sxs-lookup"><span data-stu-id="c1dcb-158">3</span></span>|<span data-ttu-id="c1dcb-159">Zahlungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="c1dcb-159">Payment Terms</span></span>|  
|<span data-ttu-id="c1dcb-160">4</span><span class="sxs-lookup"><span data-stu-id="c1dcb-160">4</span></span>|<span data-ttu-id="c1dcb-161">Währung</span><span class="sxs-lookup"><span data-stu-id="c1dcb-161">Currency</span></span>|  
|<span data-ttu-id="c1dcb-162">6</span><span class="sxs-lookup"><span data-stu-id="c1dcb-162">6</span></span>|<span data-ttu-id="c1dcb-163">Debitorenpreisgruppen</span><span class="sxs-lookup"><span data-stu-id="c1dcb-163">Customer Price Groups</span></span>|  
|<span data-ttu-id="c1dcb-164">5700</span><span class="sxs-lookup"><span data-stu-id="c1dcb-164">5700</span></span>|<span data-ttu-id="c1dcb-165">Lagerhaltungsdaten</span><span class="sxs-lookup"><span data-stu-id="c1dcb-165">Stockkeeping Unit</span></span>|

  

## <a name="see-also"></a><span data-ttu-id="c1dcb-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1dcb-166">See Also</span></span>  
[<span data-ttu-id="c1dcb-167">Konfigurationen für neue Unternehmen übernehmen</span><span class="sxs-lookup"><span data-stu-id="c1dcb-167">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="c1dcb-168">Einrichten eines Unternehmens mit RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="c1dcb-168">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="c1dcb-169">Verwaltung</span><span class="sxs-lookup"><span data-stu-id="c1dcb-169">Administration</span></span>](admin-setup-and-administration.md)
