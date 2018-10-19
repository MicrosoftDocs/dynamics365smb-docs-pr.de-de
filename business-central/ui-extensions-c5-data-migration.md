---
title: C5-Datenmigrations-Erweiterung verwenden | Microsoft Docs
description: Verwenden Sie diese Erweiterung, um Debitoren, Kreditoren, Artikel und Sachkonten von Microsoft Dynamics C5 2012 zu  Business Central zu migrieren.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: a10c05116e97cdf000bd46258a9d67f4c9910c90
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---

# <a name="the-c5-data-migration-extension"></a><span data-ttu-id="1ab69-103">Die C5-Datenmigrations-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="1ab69-103">The C5 Data Migration Extension</span></span>
<span data-ttu-id="1ab69-104">Verwenden Sie diese Erweiterung, um Debitoren, Kreditoren, Artikel und Sachkonten von Microsoft Dynamics C5 2012 zu [!INCLUDE[d365fin](includes/d365fin_md.md)] zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="1ab69-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="1ab69-105">Sie können historische Posten für Sachkonten auch migrieren.</span><span class="sxs-lookup"><span data-stu-id="1ab69-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="1ab69-106">Der Mandant darf in [!INCLUDE[d365fin](includes/d365fin_md.md)] keine Daten in enthalten.</span><span class="sxs-lookup"><span data-stu-id="1ab69-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="1ab69-107">Nachdem Sie mit der Migration begonnen haben, erstellen Sie keine Debitoren, Kreditoren, Artikel oder Konten, bis die Migration beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="1ab69-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

## <a name="what-data-is-migrated"></a><span data-ttu-id="1ab69-108">Welche Daten migriert?</span><span class="sxs-lookup"><span data-stu-id="1ab69-108">What Data is Migrated?</span></span>
<span data-ttu-id="1ab69-109">Die folgenden Daten werden für jede Einheit migriert:</span><span class="sxs-lookup"><span data-stu-id="1ab69-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="1ab69-110">**Debitoren**</span><span class="sxs-lookup"><span data-stu-id="1ab69-110">**Customers**</span></span>
* <span data-ttu-id="1ab69-111">Kontakte</span><span class="sxs-lookup"><span data-stu-id="1ab69-111">Contacts</span></span>  
* <span data-ttu-id="1ab69-112">Ort</span><span class="sxs-lookup"><span data-stu-id="1ab69-112">Location</span></span>
* <span data-ttu-id="1ab69-113">Land</span><span class="sxs-lookup"><span data-stu-id="1ab69-113">Country</span></span>
* <span data-ttu-id="1ab69-114">Debitoren-Dimensionen (Abteilung, Kostenträger, Kostenstelle)</span><span class="sxs-lookup"><span data-stu-id="1ab69-114">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="1ab69-115">Lieferbedingungsmethode</span><span class="sxs-lookup"><span data-stu-id="1ab69-115">Shipment method</span></span>
* <span data-ttu-id="1ab69-116">Verkäufer</span><span class="sxs-lookup"><span data-stu-id="1ab69-116">Sales Person</span></span>
* <span data-ttu-id="1ab69-117">Zahlungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="1ab69-117">Payment terms</span></span>
* <span data-ttu-id="1ab69-118">Zahlungsform</span><span class="sxs-lookup"><span data-stu-id="1ab69-118">Payment method</span></span>
* <span data-ttu-id="1ab69-119">Debitorenpreisgruppe</span><span class="sxs-lookup"><span data-stu-id="1ab69-119">Customer price group</span></span>
* <span data-ttu-id="1ab69-120">Debitorenrechnungsrabatt</span><span class="sxs-lookup"><span data-stu-id="1ab69-120">Customer invoice discount</span></span>

<span data-ttu-id="1ab69-121">Wenn Sie Konten migrieren, werden auch die folgenden Daten migriert:</span><span class="sxs-lookup"><span data-stu-id="1ab69-121">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="1ab69-122">Debitorenbuchungsgruppe</span><span class="sxs-lookup"><span data-stu-id="1ab69-122">Customer posting setup</span></span>
* <span data-ttu-id="1ab69-123">Fibu Buch.-Blattname</span><span class="sxs-lookup"><span data-stu-id="1ab69-123">General journal batch</span></span>
* <span data-ttu-id="1ab69-124">Migrieren Sie offene Debitorenposten (Debitorenbucheinträge)</span><span class="sxs-lookup"><span data-stu-id="1ab69-124">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="1ab69-125">**Kreditoren**</span><span class="sxs-lookup"><span data-stu-id="1ab69-125">**Vendors**</span></span>
* <span data-ttu-id="1ab69-126">Kontakte</span><span class="sxs-lookup"><span data-stu-id="1ab69-126">Contacts</span></span>
* <span data-ttu-id="1ab69-127">Ort</span><span class="sxs-lookup"><span data-stu-id="1ab69-127">Location</span></span>
* <span data-ttu-id="1ab69-128">Land</span><span class="sxs-lookup"><span data-stu-id="1ab69-128">Country</span></span>
* <span data-ttu-id="1ab69-129">Debitoren-Dimensionen (Abteilung, Kostenträger, Kostenstelle)</span><span class="sxs-lookup"><span data-stu-id="1ab69-129">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="1ab69-130">Rechnungsrabatt</span><span class="sxs-lookup"><span data-stu-id="1ab69-130">Invoice discount</span></span>
* <span data-ttu-id="1ab69-131">Lieferbedingungsmethode</span><span class="sxs-lookup"><span data-stu-id="1ab69-131">Shipment method</span></span>
* <span data-ttu-id="1ab69-132">Einkäufer</span><span class="sxs-lookup"><span data-stu-id="1ab69-132">Purchaser</span></span>
* <span data-ttu-id="1ab69-133">Zahlungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="1ab69-133">Payment terms</span></span>
* <span data-ttu-id="1ab69-134">Zahlungsform</span><span class="sxs-lookup"><span data-stu-id="1ab69-134">Payment method</span></span>
* <span data-ttu-id="1ab69-135">Kreditorenrechnungsrabatte</span><span class="sxs-lookup"><span data-stu-id="1ab69-135">Vendor invoice discount</span></span>

<span data-ttu-id="1ab69-136">Wenn Sie Konten migrieren, werden auch die folgenden Daten migriert:</span><span class="sxs-lookup"><span data-stu-id="1ab69-136">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="1ab69-137">Kreditorenbuchungsgruppe</span><span class="sxs-lookup"><span data-stu-id="1ab69-137">Vendor posting setup</span></span>
* <span data-ttu-id="1ab69-138">Fibu Buch.-Blattname</span><span class="sxs-lookup"><span data-stu-id="1ab69-138">General journal batch</span></span>
* <span data-ttu-id="1ab69-139">Öffnen Sie das Fenster Transaktionen (Kreditorenposten)</span><span class="sxs-lookup"><span data-stu-id="1ab69-139">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="1ab69-140">**Artikel**</span><span class="sxs-lookup"><span data-stu-id="1ab69-140">**Items**</span></span>
* <span data-ttu-id="1ab69-141">Ort</span><span class="sxs-lookup"><span data-stu-id="1ab69-141">Location</span></span>
* <span data-ttu-id="1ab69-142">Land</span><span class="sxs-lookup"><span data-stu-id="1ab69-142">Country</span></span>
* <span data-ttu-id="1ab69-143">Element-Dimensionen (Abteilung, Kostenträger, Kostenstelle)</span><span class="sxs-lookup"><span data-stu-id="1ab69-143">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="1ab69-144">VK-Zeilenrabatte</span><span class="sxs-lookup"><span data-stu-id="1ab69-144">Sales line discounts</span></span>
* <span data-ttu-id="1ab69-145">Debitorenrabattgruppen</span><span class="sxs-lookup"><span data-stu-id="1ab69-145">Customer discount groups</span></span>
* <span data-ttu-id="1ab69-146">Artikelrabattgruppen</span><span class="sxs-lookup"><span data-stu-id="1ab69-146">Item discount groups</span></span>
* <span data-ttu-id="1ab69-147">Verkaufspreis</span><span class="sxs-lookup"><span data-stu-id="1ab69-147">Sales price</span></span>
* <span data-ttu-id="1ab69-148">Zollposition</span><span class="sxs-lookup"><span data-stu-id="1ab69-148">Tariff number</span></span>
* <span data-ttu-id="1ab69-149">Einheiten</span><span class="sxs-lookup"><span data-stu-id="1ab69-149">Units of measure</span></span>
* <span data-ttu-id="1ab69-150">Artikelverfolgungscode</span><span class="sxs-lookup"><span data-stu-id="1ab69-150">Item tracking code</span></span>
* <span data-ttu-id="1ab69-151">Debitorenpreisgruppe</span><span class="sxs-lookup"><span data-stu-id="1ab69-151">Customer price group</span></span>
* <span data-ttu-id="1ab69-152">Montagestücklisten</span><span class="sxs-lookup"><span data-stu-id="1ab69-152">Assembly BOMs</span></span>

<span data-ttu-id="1ab69-153">Wenn Sie Konten migrieren, werden auch die folgenden Daten migriert:</span><span class="sxs-lookup"><span data-stu-id="1ab69-153">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="1ab69-154">Lagerbuchungseinrichtung</span><span class="sxs-lookup"><span data-stu-id="1ab69-154">Inventory posting setup</span></span>
* <span data-ttu-id="1ab69-155">Buchungsmatrix Einrichtung</span><span class="sxs-lookup"><span data-stu-id="1ab69-155">General posting setup</span></span>
* <span data-ttu-id="1ab69-156">Artikel Buch.-Blattname</span><span class="sxs-lookup"><span data-stu-id="1ab69-156">Item journal batch</span></span>
* <span data-ttu-id="1ab69-157">Öffnen Sie das Fenster Transaktionen (Artikel Kreditorenposten)</span><span class="sxs-lookup"><span data-stu-id="1ab69-157">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="1ab69-158">Wenn es offene Transaktionen gibt, die Fremdwährungen verwenden, werden die Wechselkurse für alle Währungen auch migriert.</span><span class="sxs-lookup"><span data-stu-id="1ab69-158">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="1ab69-159">Andere Wechselkurse werden nicht migriert.</span><span class="sxs-lookup"><span data-stu-id="1ab69-159">Other exchange rates are not migrated.</span></span>

<span data-ttu-id="1ab69-160">**Kontenplan**</span><span class="sxs-lookup"><span data-stu-id="1ab69-160">**Chart of Accounts**</span></span>  
* <span data-ttu-id="1ab69-161">Standard-Dimensionen (Abteilung, Kostenträger, Kostenstelle)</span><span class="sxs-lookup"><span data-stu-id="1ab69-161">Standard dimensions: Department, Cost Center, Purpose</span></span>  
* <span data-ttu-id="1ab69-162">Historische Transaktionen</span><span class="sxs-lookup"><span data-stu-id="1ab69-162">Historical G/L transactions</span></span>  

> [!Note]
> <span data-ttu-id="1ab69-163">Historische Transaktionen werden so gut unterschiedlich behandelt.</span><span class="sxs-lookup"><span data-stu-id="1ab69-163">Historical G/L transactions are treated a little differently.</span></span> <span data-ttu-id="1ab69-164">Wenn Sie Daten migrieren, setzen Sie einen **Aktuelle Periode** Parameter.</span><span class="sxs-lookup"><span data-stu-id="1ab69-164">When you migrate data you set a **Current Period** parameter.</span></span> <span data-ttu-id="1ab69-165">Dieser Parameter gibt an, wie Ihre Transaktionen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="1ab69-165">This parameter specifies how to process G/L transactions.</span></span> <span data-ttu-id="1ab69-166">Transaktionen nach diesem Datum werden einzeln migriert.</span><span class="sxs-lookup"><span data-stu-id="1ab69-166">Transactions after this date are migrated individually.</span></span> <span data-ttu-id="1ab69-167">Transaktionen vor diesem Zeitpunkt werden pro Konto aggregiert und migriert als einzelner Betrag.</span><span class="sxs-lookup"><span data-stu-id="1ab69-167">Transactions before this date are aggregated per account and migrated as a single amount.</span></span> <span data-ttu-id="1ab69-168">Nehmen wir an, es gibt Transaktionen 2015, 2016, 2017 und 2018 und Sie definieren 1. Januar 2017 im aktuellen Periodenfeld.</span><span class="sxs-lookup"><span data-stu-id="1ab69-168">For example, let's say there are transactions in 2015, 2016, 2017, 2018, and you specify January 01, 2017 in the Current Period field.</span></span> <span data-ttu-id="1ab69-169">Für jedes Konto sind Beträge für Transaktionen an oder vor dem 31. Dezember 2106, in einer eigenen Fibu Buch.-Blattzeile für jedes Sachkonto aggregiert.</span><span class="sxs-lookup"><span data-stu-id="1ab69-169">For each account, amounts for transactions on or before December 31, 2106, will be aggregated in a single general journal line for each G/L account.</span></span> <span data-ttu-id="1ab69-170">Transaktionen nach diesem Datum werden einzeln migriert.</span><span class="sxs-lookup"><span data-stu-id="1ab69-170">All trascations after this date will be migrated individually.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="1ab69-171">Um Daten zu migrieren</span><span class="sxs-lookup"><span data-stu-id="1ab69-171">To migrate data</span></span>
<span data-ttu-id="1ab69-172">Es gibt nur einige wenige Schritte, um die Daten aus C5 zu exportieren und sie in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu importieren:</span><span class="sxs-lookup"><span data-stu-id="1ab69-172">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="1ab69-173">In C5 verwenden Sie die Funktion **Datenbank exportieren**, um die Daten zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="1ab69-173">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="1ab69-174">Senden Sie dann den Exportordner an einen komprimierten (gezippten) Ordner.</span><span class="sxs-lookup"><span data-stu-id="1ab69-174">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="1ab69-175">Wählen Sie in [!INCLUDE[d365fin](includes/d365fin_md.md)] das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Datenmigration** ein, und wählen Sie dann **Datenmigration** aus.</span><span class="sxs-lookup"><span data-stu-id="1ab69-175">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="1ab69-176">Schliessen Sie die Schritte im unterstützten Setup ab.</span><span class="sxs-lookup"><span data-stu-id="1ab69-176">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="1ab69-177">Stellen Sie sicher, dass Sie**Importieren aus Microsoft Dynamcis C5 2012** als die Datenquelle auswählen.</span><span class="sxs-lookup"><span data-stu-id="1ab69-177">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note]
> <span data-ttu-id="1ab69-178">Mandanten fügen häufig Felder hinzu, um C5 für ihren jeweiligen Geschäftsbereich anzupassen.</span><span class="sxs-lookup"><span data-stu-id="1ab69-178">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="1ab69-179">migriert nicht Daten vom benutzerdefinierten Feldern.</span><span class="sxs-lookup"><span data-stu-id="1ab69-179">does not migrate data from custom fields.</span></span> <span data-ttu-id="1ab69-180">Die Migration schlägt fehl, wenn Sie mehr als 10 benutzerdefinierte Felder haben.</span><span class="sxs-lookup"><span data-stu-id="1ab69-180">Also, migration will fail if you have more than 10 custom fields.</span></span>

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="1ab69-181">Zeigt den Status der Datenmigration an</span><span class="sxs-lookup"><span data-stu-id="1ab69-181">Viewing the Status of the Migration</span></span>
<span data-ttu-id="1ab69-182">Verwenden Sie das Fenster **Datenmigrations-Übersicht**, um den Erfolg der Migration zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="1ab69-182">Use the **Data Migration Overview** window to monitor the success of the migration.</span></span> <span data-ttu-id="1ab69-183">Die Seite zeigt Informationen wie die Anzahl von Einheiten, die migriert wurde, den Status der Migration und die Anzahl von Artikeln an, die migriert wurden und ob sie erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="1ab69-183">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="1ab69-184">Sie zeigt auch die Anzahl von Fehlern, Sie können überprüfen, was schief ging und macht es wenn möglich einfach, zur Einheit zu gehen und das Problem zu lösen.</span><span class="sxs-lookup"><span data-stu-id="1ab69-184">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="1ab69-185">Weitere Informationen finden Sie im nächsten Abschnitt dieses Themas.</span><span class="sxs-lookup"><span data-stu-id="1ab69-185">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="1ab69-186">Während Sie auf die Ergebnisse der Migration warten, müssen Sie die Seite aktualisieren, um die Ergebnisse anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1ab69-186">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="how-to-avoid-double-posting"></a><span data-ttu-id="1ab69-187">Wie Sie Doppel-Buchung vermeiden</span><span class="sxs-lookup"><span data-stu-id="1ab69-187">How to Avoid Double-Posting</span></span>
<span data-ttu-id="1ab69-188">Um Doppelbuchungen in der Finanzbuchhaltung zu vermeiden, werden folgende Gegenkonten für offene Transaktionen verwendet:</span><span class="sxs-lookup"><span data-stu-id="1ab69-188">To help avoid double-posting to the general ledger, the following balance accounts are used for open transactions:</span></span>  

* <span data-ttu-id="1ab69-189">Für Kreditoren verwenden wir das A-/P-Konto in der Kreditorenbuchungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="1ab69-189">For vendors, we use the A/P account from the vendor posting group.</span></span>  
* <span data-ttu-id="1ab69-190">Für Debitore verwenden wir das A-/P-Konto in der Debitorenbuchungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="1ab69-190">For customers, we use the A/R account from the customer posting group.</span></span>  
* <span data-ttu-id="1ab69-191">Für Artikel erstellen wir eine Buchungsmatrix, bei der im Korrekturkonto das Konto jenes ist, das als Lagerkonto in der Lagerbuchungseinrichtung angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="1ab69-191">For items, we create a general posting setup where the adjustment account is the account specified as the inventory account on the inventory posting setup.</span></span>  

## <a name="correcting-errors"></a><span data-ttu-id="1ab69-192">Nachbesserung</span><span class="sxs-lookup"><span data-stu-id="1ab69-192">Correcting Errors</span></span>
<span data-ttu-id="1ab69-193">Falls etwas schief geht und ein Fehler auftritt, wird das **Status** Feld **Abgeschlossen mit Fehlern** angezeigt und das Feld **Fehlerzahl** zeigt an, wie viele es sind.</span><span class="sxs-lookup"><span data-stu-id="1ab69-193">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="1ab69-194">Um eine Liste der Fehler anzuzeigen, können Sie das Fenster öffnen indem Sie **Datenmigrations-Fehler** auswählen:</span><span class="sxs-lookup"><span data-stu-id="1ab69-194">To view a list of the errors, you can open the **Data Migration Errors** window by choosing:</span></span>  

* <span data-ttu-id="1ab69-195">Die Nummer im Feld **Fehlerzahl** für die Einheit.</span><span class="sxs-lookup"><span data-stu-id="1ab69-195">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="1ab69-196">Die Einheit und dann die Aktion **Fehler anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="1ab69-196">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="1ab69-197">Um im Fenster **Datenmigrations-Fehler** einen Fehler zu korrigieren, können Sie eine Fehlermeldung auswählen, und dann **Datensatz bearbeiten** auswählen, um die Daten für die migrierte Einheit anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1ab69-197">In the **Data Migration Errors** window, to fix an error you can choose an error message, and then choose **Edit Record** to view the migrated data for the entity.</span></span> <span data-ttu-id="1ab69-198">Wenn Sie mehrere Fehler beheben müssen, können Sie **Stapelfehlerkorrektur** auswählen, um auf die Einheiten in einer Liste zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="1ab69-198">If you have several errors to fix, you can choose **Bulk-Fix Errors** to edit the entities in a list.</span></span> <span data-ttu-id="1ab69-199">Sie müssen immer noch einzelne Datensätze öffnen, wenn der Fehler durch einen entsprechenden Posten verursacht wurde.</span><span class="sxs-lookup"><span data-stu-id="1ab69-199">You still need to open individual records if the error was caused by a related entry though.</span></span> <span data-ttu-id="1ab69-200">Beispielsweise wird ein Kreditor nicht migriert, wenn die E-Mail-Adresse einer Kontaktperson ein ungültiges Format hat.</span><span class="sxs-lookup"><span data-stu-id="1ab69-200">For example, a vendor will not be migrated if an email address one of their contacts has an invalid format.</span></span>

<span data-ttu-id="1ab69-201">Nachdem Sie eines oder mehrere Fehler korrigiert haben, können Sie **Migrieren von** wählen, um nur die Einheiten zu migrieren, die Sie korrigierten, ohne die Migration vollständig erneut durchführen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="1ab69-201">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="1ab69-202">Wenn Sie mehr als einen Fehler korrigiert haben, können Sie die Funktion **Weitere auswählen** verwenden, um mehrere Zeilen auszuwählen, um diese zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="1ab69-202">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="1ab69-203">Wenn es Fehler gibt, die nicht zur Korrektur wichtig sind, können Sie diese auswählen und dann **Auswahl überspringen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="1ab69-203">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="1ab69-204">Wenn Sie Artikel haben, die in der Stückliste enthalten sind, müssen Sie diese mehrmals migrieren, wenn der ursprüngliche Artikel nicht vor den Varianten erstellt wird, auf die sie verweist.</span><span class="sxs-lookup"><span data-stu-id="1ab69-204">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="1ab69-205">Wenn eine Artikelvariante zuerst erzeugt wird, kann die Referenz zum ursprünglichen Artikel eine Fehlermeldung verursachen.</span><span class="sxs-lookup"><span data-stu-id="1ab69-205">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="1ab69-206">Prüfen von Daten nach dem Migrieren</span><span class="sxs-lookup"><span data-stu-id="1ab69-206">Verifying Data After Migrating</span></span>
<span data-ttu-id="1ab69-207">Wenn Sie sicherstellen möchten, dass Ihre Daten ordnungsgemäß migriert werden, können Sie die nächste Seiten in C5 und in [!INCLUDE[d365fin](includes/d365fin_md.md)]anzeigen.</span><span class="sxs-lookup"><span data-stu-id="1ab69-207">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="1ab69-208">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="1ab69-208">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]| <span data-ttu-id="1ab69-209">Zu verwendender Batchauftrag</span><span class="sxs-lookup"><span data-stu-id="1ab69-209">Batch Job to Use</span></span> |
|-----|-----|-----|
|<span data-ttu-id="1ab69-210">Debitoreneinträge</span><span class="sxs-lookup"><span data-stu-id="1ab69-210">Customer Entries</span></span>| <span data-ttu-id="1ab69-211">Fibu Buch.-Blätter</span><span class="sxs-lookup"><span data-stu-id="1ab69-211">General Journals</span></span>| <span data-ttu-id="1ab69-212">CUSTMIGR</span><span class="sxs-lookup"><span data-stu-id="1ab69-212">CUSTMIGR</span></span> |
|<span data-ttu-id="1ab69-213">Kreditoreneinträge</span><span class="sxs-lookup"><span data-stu-id="1ab69-213">Vendor Entries</span></span>| <span data-ttu-id="1ab69-214">Fibu Buch.-Blätter</span><span class="sxs-lookup"><span data-stu-id="1ab69-214">General Journals</span></span>| <span data-ttu-id="1ab69-215">VENDMIGR</span><span class="sxs-lookup"><span data-stu-id="1ab69-215">VENDMIGR</span></span>|
|<span data-ttu-id="1ab69-216">Artikelposten</span><span class="sxs-lookup"><span data-stu-id="1ab69-216">Item Entries</span></span>| <span data-ttu-id="1ab69-217">Artikel Buch.-Blätter</span><span class="sxs-lookup"><span data-stu-id="1ab69-217">Item Journals</span></span>| <span data-ttu-id="1ab69-218">ITEMMIGR</span><span class="sxs-lookup"><span data-stu-id="1ab69-218">ITEMMIGR</span></span> |
|<span data-ttu-id="1ab69-219">Sachposten</span><span class="sxs-lookup"><span data-stu-id="1ab69-219">G/L Entries</span></span>| <span data-ttu-id="1ab69-220">Fibu Buch.-Blätter</span><span class="sxs-lookup"><span data-stu-id="1ab69-220">General Journals</span></span>| <span data-ttu-id="1ab69-221">GLACMIGR</span><span class="sxs-lookup"><span data-stu-id="1ab69-221">GLACMIGR</span></span> |

## <a name="stopping-data-migration"></a><span data-ttu-id="1ab69-222">Datenmigration anhalten</span><span class="sxs-lookup"><span data-stu-id="1ab69-222">Stopping Data Migration</span></span>
<span data-ttu-id="1ab69-223">Sie können Datenmigration unterbrechen, indem Sie **Automatisches Beenden alle Migrationen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="1ab69-223">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="1ab69-224">Wenn Sie dies tun, werden alle offenen Migrationen beendet.</span><span class="sxs-lookup"><span data-stu-id="1ab69-224">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="1ab69-225">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ab69-225">See Also</span></span>
<span data-ttu-id="1ab69-226">[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="1ab69-226">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="1ab69-227">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="1ab69-227">Getting Started</span></span>](product-get-started.md)

