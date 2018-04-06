---
title: Verwenden Sie Excel, um in Financials Stammdaten zu importieren | Microsoft Docs
description: "Verwenden Sie das Standardkonfigurationspaket, um Debitorendaten in Excel hinzuzufügen und Daten nach Business Central zu importieren."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 03/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4526e8b11c9cbae36c7db58259499fbfa1b0c243
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="importing-data-from-legacy-accounting-software-using-a-configuration-package"></a><span data-ttu-id="85e82-103">Importieren von Daten aus der Vorgänger-Buchhaltungs-Software unter Verwendung eines Konfigurations-Pakets.</span><span class="sxs-lookup"><span data-stu-id="85e82-103">Importing Data from Legacy Accounting Software using a Configuration Package</span></span>
<span data-ttu-id="85e82-104">Sie können Transaktions-Masterdaten und die Daten aus anderen Finanzsysteme basierend auf dem Standardkonfigurationspaket in [!INCLUDE[d365fin](includes/d365fin_md.md)] importieren.</span><span class="sxs-lookup"><span data-stu-id="85e82-104">You can import master data and some transactional data from other finance systems based on the default configuration package in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="85e82-105">Im Fenster **Konfigurationspakete** können Sie mit einem Paket arbeiten, um die Daten zu importieren und zu prüfen, bevor Sie die Paketnummer anwenden.</span><span class="sxs-lookup"><span data-stu-id="85e82-105">In the **Configuration Packages** window, you can work with the package to import and validate the data before you apply the package.</span></span>  

> [!NOTE]  
> <span data-ttu-id="85e82-106">Konfigurationspakete sind Teil von RapidStart-Services, [!INCLUDE[d365fin](includes/d365fin_md.md)]für der umfangreichen Toolkit für das Einrichten von neuen Lösungen auf Grundlage Geschäftsanforderungen und -Einrichtungsdaten der Debitoren.</span><span class="sxs-lookup"><span data-stu-id="85e82-106">Configuration packages are part of RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], an extensive toolkit for setting up new solutions based on customers' business requirements and setup data.</span></span> <span data-ttu-id="85e82-107">RapidStart enthält auch Funktionalität für Stammdaten Importieren von Artikeln.</span><span class="sxs-lookup"><span data-stu-id="85e82-107">RapidStart Services also offers functionality for import of legacy data.</span></span> <span data-ttu-id="85e82-108">Weitere Informationen finden Sie unter [Einrichten eines Unternehmens mit RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span><span class="sxs-lookup"><span data-stu-id="85e82-108">For more information, see [Setting Up a Company With RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span></span>

> [!TIP]  
>   <span data-ttu-id="85e82-109">Alternativ verwenden Sie den Datenmigrationsassistenten, um die Daten aus QuickBooks oder von Dynamics GP zu importieren.</span><span class="sxs-lookup"><span data-stu-id="85e82-109">Alternatively, use data migration wizards to import data from QuickBooks or Dynamics GP.</span></span> <span data-ttu-id="85e82-110">Weitere Informationen finden Sie unter [QuickBooks-Datenmigration](ui-extensions-quickbooks-data-migration.md) oder [Dynamics GP-Datenmigration](ui-extensions-dynamicsgp-data-migration.md).</span><span class="sxs-lookup"><span data-stu-id="85e82-110">For more information, see [QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md) or [Dynamics GP Data Migration](ui-extensions-dynamicsgp-data-migration.md).</span></span>  

## <a name="working-with-data-in-excel"></a><span data-ttu-id="85e82-111">Arbeiten mit Daten in Excel</span><span class="sxs-lookup"><span data-stu-id="85e82-111">Working with Data in Excel</span></span>
<span data-ttu-id="85e82-112">Wenn Sie das Standardkonfigurationspaket in Excel exportieren, enthält die generierte Arbeitsmappe einen Vorschlag für jede Tabelle im Paket.</span><span class="sxs-lookup"><span data-stu-id="85e82-112">When you export the default configuration package to Excel, the generated workbook contains a worksheet for each table in the package.</span></span> <span data-ttu-id="85e82-113">Um Ihre Aufgaben zu vereinfachen, können Sie die in Excel integrierten XML-Änderungswerkzeuge nutzen.</span><span class="sxs-lookup"><span data-stu-id="85e82-113">To simplify your tasks, you can take advantage of the XML manipulation tools that are built into Excel.</span></span> <span data-ttu-id="85e82-114">Sie können die in Excel integrierten Funktionen auch für die Datenformatierung und zum Verschieben von Daten in die richtige Zelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="85e82-114">You can also use Excel built-in functions to help with data formatting and to put data in the correct cell.</span></span> <span data-ttu-id="85e82-115">Beispielsweise fügen Sie einen leeren Vorschlag hinzu und kopieren Sie die Stammdaten dazu.</span><span class="sxs-lookup"><span data-stu-id="85e82-115">For example, add a blank worksheet and copy the legacy data to it.</span></span> <span data-ttu-id="85e82-116">Verwenden Sie eine Excel-Formel, um Daten im Arbeitsblatt für die Datenumwandlung zwischen den Feldern im exportierten Datenblatt und in den Debitorenstammdaten zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="85e82-116">Then make an Excel formula to map data in the transformation worksheet between the fields in the exported worksheet and customer legacy data.</span></span> <span data-ttu-id="85e82-117">Sobald Sie alle Daten zugeordnet haben, kopieren Sie den Bereich der Daten in das Arbeitsblatt mit der Migrationstabelle.</span><span class="sxs-lookup"><span data-stu-id="85e82-117">After you have mapped all of the data, copy the range of data onto the table worksheet.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="85e82-118">Ändern Sie nicht die Spalten in den Arbeitsblättern.</span><span class="sxs-lookup"><span data-stu-id="85e82-118">Do not change the columns in the worksheets.</span></span> <span data-ttu-id="85e82-119">Wenn sie verschoben, geändert oder gelöscht werden, kann das Arbeitsblatt nicht in [!INCLUDE[d365fin](includes/d365fin_md.md)] importiert werden.</span><span class="sxs-lookup"><span data-stu-id="85e82-119">If they are moved, changed, or deleted, the worksheet cannot be imported into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="tables-in-the-default-configuration-package"></a><span data-ttu-id="85e82-120">Tabellen im Standard-Konfigurations-Paket</span><span class="sxs-lookup"><span data-stu-id="85e82-120">Tables in the Default Configuration Package</span></span>
<span data-ttu-id="85e82-121">Das Standardkonfigurationspaket unterstützt die folgenden Tabellen:</span><span class="sxs-lookup"><span data-stu-id="85e82-121">The default configuration package supports the following tables:</span></span>

-   <span data-ttu-id="85e82-122">Zahlungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="85e82-122">Payment Terms</span></span>
-   <span data-ttu-id="85e82-123">Debitorenpreisgruppe</span><span class="sxs-lookup"><span data-stu-id="85e82-123">Customer Price Group</span></span>
-   <span data-ttu-id="85e82-124">Lieferbedingungsmethode</span><span class="sxs-lookup"><span data-stu-id="85e82-124">Shipment Method</span></span>
-   <span data-ttu-id="85e82-125">Verkäufer/Einkäufer</span><span class="sxs-lookup"><span data-stu-id="85e82-125">Salesperson/Purchaser</span></span>
-   <span data-ttu-id="85e82-126">Ort</span><span class="sxs-lookup"><span data-stu-id="85e82-126">Location</span></span>
-   <span data-ttu-id="85e82-127">Gegenkonto</span><span class="sxs-lookup"><span data-stu-id="85e82-127">GL Account</span></span>
-   <span data-ttu-id="85e82-128">Debitor</span><span class="sxs-lookup"><span data-stu-id="85e82-128">Customer</span></span>
-   <span data-ttu-id="85e82-129">Kreditor</span><span class="sxs-lookup"><span data-stu-id="85e82-129">Vendor</span></span>
-   <span data-ttu-id="85e82-130">Option</span><span class="sxs-lookup"><span data-stu-id="85e82-130">Item</span></span>
-   <span data-ttu-id="85e82-131">Verkaufskopf</span><span class="sxs-lookup"><span data-stu-id="85e82-131">Sales Header</span></span>
-   <span data-ttu-id="85e82-132">Verkaufszeile</span><span class="sxs-lookup"><span data-stu-id="85e82-132">Sales Line</span></span>
-   <span data-ttu-id="85e82-133">Einkaufskopf</span><span class="sxs-lookup"><span data-stu-id="85e82-133">Purchase Header</span></span>
-   <span data-ttu-id="85e82-134">Einkaufszeile</span><span class="sxs-lookup"><span data-stu-id="85e82-134">Purchase Line</span></span>
-   <span data-ttu-id="85e82-135">Fibu Buch.-Blattzeile</span><span class="sxs-lookup"><span data-stu-id="85e82-135">Gen. Journal Line</span></span>
-   <span data-ttu-id="85e82-136">Artikel Buch.-Blattzeile</span><span class="sxs-lookup"><span data-stu-id="85e82-136">Item Journal Line</span></span>
-   <span data-ttu-id="85e82-137">Debitorenbuchungsgruppe</span><span class="sxs-lookup"><span data-stu-id="85e82-137">Customer Posting Group</span></span>
-   <span data-ttu-id="85e82-138">Kreditorenbuchungsgruppe</span><span class="sxs-lookup"><span data-stu-id="85e82-138">Vendor Posting Group</span></span>
-   <span data-ttu-id="85e82-139">Lagerbuchungsgruppe</span><span class="sxs-lookup"><span data-stu-id="85e82-139">Inventory Posting Group</span></span>
-   <span data-ttu-id="85e82-140">Maßeinheit</span><span class="sxs-lookup"><span data-stu-id="85e82-140">Unit of Measure</span></span>
-   <span data-ttu-id="85e82-141">Geschäftsbuchungsgrp.</span><span class="sxs-lookup"><span data-stu-id="85e82-141">Gen. Business Posting Group</span></span>
-   <span data-ttu-id="85e82-142">Produktbuchungsgrp.</span><span class="sxs-lookup"><span data-stu-id="85e82-142">Gen. Product Posting Group</span></span>
-   <span data-ttu-id="85e82-143">Buchungsmatrix Einrichtung</span><span class="sxs-lookup"><span data-stu-id="85e82-143">General Posting Setup</span></span>
-   <span data-ttu-id="85e82-144">Gebiet</span><span class="sxs-lookup"><span data-stu-id="85e82-144">Territory</span></span>
-   <span data-ttu-id="85e82-145">Artikelkategorie</span><span class="sxs-lookup"><span data-stu-id="85e82-145">Item Category</span></span>
-   <span data-ttu-id="85e82-146">Verkaufspreis</span><span class="sxs-lookup"><span data-stu-id="85e82-146">Sales Price</span></span>
-   <span data-ttu-id="85e82-147">Einkaufspreis</span><span class="sxs-lookup"><span data-stu-id="85e82-147">Purchase Price</span></span>

## <a name="importing-customer-data"></a><span data-ttu-id="85e82-148">So importieren Sie Debitorendaten</span><span class="sxs-lookup"><span data-stu-id="85e82-148">Importing Customer Data</span></span>
<span data-ttu-id="85e82-149">Nachdem die Debitorendaten in die Excel-Dateien für die Datenmigration eingegeben wurden, importieren Sie die Dateien in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="85e82-149">After the customer data has been entered in Excel, you import the data into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="85e82-150">Im Fenster **Konfigurationspakete** importieren Sie die Excel-Datei aus den Daten, und Sie können prüfen, ob die Daten mit [!INCLUDE[d365fin](includes/d365fin_md.md)] übereinstimmen, bevor Sie das Paket anwenden.</span><span class="sxs-lookup"><span data-stu-id="85e82-150">In the **Configuration Packages** window, you import the data from the Excel file, and you can validate that the data is consistent with [!INCLUDE[d365fin](includes/d365fin_md.md)] before you apply the package.</span></span>

## <a name="see-also"></a><span data-ttu-id="85e82-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85e82-151">See Also</span></span>
[<span data-ttu-id="85e82-152">Geschäftsdaten aus anderen Finanzsystemen importieren</span><span class="sxs-lookup"><span data-stu-id="85e82-152">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
[<span data-ttu-id="85e82-153">Einrichten von Mandanten mit RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="85e82-153">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="85e82-154">QuickBooks Datenmigration</span><span class="sxs-lookup"><span data-stu-id="85e82-154">QuickBooks Data Migration</span></span>](ui-extensions-quickbooks-data-migration.md)  
[<span data-ttu-id="85e82-155">Dynamics GP Datenmigration</span><span class="sxs-lookup"><span data-stu-id="85e82-155">Dynamics GP Data Migration</span></span>](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

