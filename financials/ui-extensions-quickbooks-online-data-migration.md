---
title: QuickBooks-Migrations-Erweiterung verwenden | Microsoft Docs
description: Beschreibt, wie die Erweiterung verwendet wird, um Debitoren, Kreditoren, Artikel und Konten aus QuickBooks-Online auf Dynamics 365 for Financials zu migrieren
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, QuickBooks, import
ms.date: 05/24/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: fe87a108d132ff25f0c93a51df58bb88fb12f421
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---

# <a name="the-quickbooks-online-data-migration-extension-for-dynamics-365-for-financials"></a><span data-ttu-id="05de6-103">Die QuickBooks-Online-Datenmigrations-Erweiterung für Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="05de6-103">The QuickBooks Online Data Migration Extension for Dynamics 365 for Financials</span></span>
<span data-ttu-id="05de6-104">Diese Erweiterung ist im unterstützten Einrichtungshandbuch **Datenmigration** enthalten, um Ihnen zu helfen, wichtige Geschäftsdaten von QuickBooks in Online zu [!INCLUDE[d365fin](includes/d365fin_md.md)]migrieren.</span><span class="sxs-lookup"><span data-stu-id="05de6-104">This extension is included in the **Data Migration** assisted setup guide to help you migrate important business data from QuickBooks Online to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="05de6-105">Dies ist beispielsweise dann nützlich, wenn Ihr Unternehmen wächst und Sie sich entschieden haben, Ihre Geschäftsführungs-App zu aktualisieren, indem Sie mit [!INCLUDE[d365fin](includes/d365fin_md.md)]  verwenden.</span><span class="sxs-lookup"><span data-stu-id="05de6-105">For example, this is useful when your business is growing, and you've decided to upgrade your business management app by starting to use [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="what-data-can-i-import-from-quickbooks-online"></a><span data-ttu-id="05de6-106">Welche Daten kann ich von QuickBooks online importieren?</span><span class="sxs-lookup"><span data-stu-id="05de6-106">What data can I import from QuickBooks Online?</span></span>
<span data-ttu-id="05de6-107">Sie können die folgenden Daten aus QuickBooks online importieren [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="05de6-107">You can import the following data from QuickBooks Online to [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

* <span data-ttu-id="05de6-108">Debitoren</span><span class="sxs-lookup"><span data-stu-id="05de6-108">Customers</span></span>
* <span data-ttu-id="05de6-109">Kreditoren</span><span class="sxs-lookup"><span data-stu-id="05de6-109">Vendors</span></span>
* <span data-ttu-id="05de6-110">Artikel</span><span class="sxs-lookup"><span data-stu-id="05de6-110">Items</span></span>
* <span data-ttu-id="05de6-111">Kontenplan</span><span class="sxs-lookup"><span data-stu-id="05de6-111">Chart of accounts</span></span> 
* <span data-ttu-id="05de6-112">Saldovortragtransaktion in der Finanzbuchhaltung</span><span class="sxs-lookup"><span data-stu-id="05de6-112">Beginning balance transaction in the general ledger</span></span>
* <span data-ttu-id="05de6-113">Verfügbare Mengen für Lagerartikel</span><span class="sxs-lookup"><span data-stu-id="05de6-113">On-hand quantities for inventory items</span></span>
* <span data-ttu-id="05de6-114">Offene Dokumente für Debitoren und Kreditoren, wie beispielsweise Rechnungen, Gutschriften und Zahlungen</span><span class="sxs-lookup"><span data-stu-id="05de6-114">Open documents for customers and vendors, such as invoices, credit memos, and payments</span></span>

<span data-ttu-id="05de6-115">Es migrieren nur Gesamtbeträge auf Einkaufs- und Verkaufsbelegen.</span><span class="sxs-lookup"><span data-stu-id="05de6-115">We migrate only full amounts on sales and purchase documents.</span></span> <span data-ttu-id="05de6-116">Wir aktualisieren keine teilweise bezahlten Beträge.</span><span class="sxs-lookup"><span data-stu-id="05de6-116">We do not update partially paid amounts.</span></span> <span data-ttu-id="05de6-117">Wenn ein Debitor 300 von insgesamt 500 Dollar einer Verkaufsrechnung bezahlt hat, migrieren wir die vollständigen 500.</span><span class="sxs-lookup"><span data-stu-id="05de6-117">For example, if a customer has paid 300 of a total of 500 dollars on a sales invoice, we migrate the full 500.</span></span> <span data-ttu-id="05de6-118">Wenn Sie Teilzahlungen erhalten, müssen Sie diese manuell aktualisieren, entweder, vor oder nach dem Sie Daten migrieren.</span><span class="sxs-lookup"><span data-stu-id="05de6-118">If you have received partial payments, you must update these manually, either before or after you migrate data.</span></span> <span data-ttu-id="05de6-119">Es ist empfehlenswert, ausstehende Transaktionen anzuwenden, bevor Sie migrieren, das ist einfacher danach.</span><span class="sxs-lookup"><span data-stu-id="05de6-119">We recommend that you apply outstanding transactions before you migrate, just to make things easier afterward.</span></span>

> [!NOTE]  
>   <span data-ttu-id="05de6-120">Wir migrieren keine Einkaufsbestellungen oder Verkaufsaufträge.</span><span class="sxs-lookup"><span data-stu-id="05de6-120">We do not migrate purchase orders or sales orders.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="05de6-121">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="05de6-121">Before you start</span></span>
<span data-ttu-id="05de6-122">Ein wichtiger Teil des Migrationsvorgangs ist es, Konten anzugeben, um Transaktionen zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="05de6-122">An important part of the migration process is to specify the accounts to migrate transactions to.</span></span> <span data-ttu-id="05de6-123">Es ist empfehlenswert, diese Zuordnung zu planen, bevor Sie Daten migrieren.</span><span class="sxs-lookup"><span data-stu-id="05de6-123">It's a good idea to plan this mapping before you migrate data.</span></span> <span data-ttu-id="05de6-124">Beispielsweise die Konten, die Sie für Transaktionen buchen:</span><span class="sxs-lookup"><span data-stu-id="05de6-124">For example, the accounts where you post transactions for:</span></span>  
  
* <span data-ttu-id="05de6-125">Der Verkauf von Artikeln oder Services an einen Kunden.</span><span class="sxs-lookup"><span data-stu-id="05de6-125">The sale of items or services to customers.</span></span>
* <span data-ttu-id="05de6-126">Der Kauf von Waren oder Dienste von einem Kreditor.</span><span class="sxs-lookup"><span data-stu-id="05de6-126">The purchase of items or services from vendors.</span></span>  
* <span data-ttu-id="05de6-127">Änderungen in der Finanzbuchhaltung.</span><span class="sxs-lookup"><span data-stu-id="05de6-127">Adjustments in the general ledger.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="05de6-128"> erfordert, dass Sachkonten die Kontonummern haben, die ihm zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="05de6-128"> requires that general ledger accounts have account numbers assigned to them.</span></span> <span data-ttu-id="05de6-129">Überprüfen Sie, ob Sie Kontonummern Ihren Konten in QuickBooks online zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="05de6-129">Make sure that account numbers are assigned to your accounts in QuickBooks Online.</span></span>

<span data-ttu-id="05de6-130">Wenn Transaktionen in QuickBooks online Steuerbeträge haben, müssen Sie eine MwSt einrichten für Ihre Steuerzuständigkeiten in, [!INCLUDE[d365fin](includes/d365fin_md.md)] bevor Sie Buchungen durchführen können.</span><span class="sxs-lookup"><span data-stu-id="05de6-130">If transactions in QuickBooks Online have tax amounts, you must set up a tax account for your tax jurisdictions in [!INCLUDE[d365fin](includes/d365fin_md.md)] before you can post transactions.</span></span>

## <a name="how-do-i-start-using-the-extension"></a><span data-ttu-id="05de6-131">Wie beginne ich, die Erweiterung zu nutzen?</span><span class="sxs-lookup"><span data-stu-id="05de6-131">How do I start using the extension?</span></span>
<span data-ttu-id="05de6-132">Erste Schritte sind einfach.</span><span class="sxs-lookup"><span data-stu-id="05de6-132">Getting started is easy.</span></span> <span data-ttu-id="05de6-133">Sie müssen nur das unterstütze Einrichtungshandbuch **Datenmigration** ausführen.</span><span class="sxs-lookup"><span data-stu-id="05de6-133">All you need to do is run the **Data Migration** assisted setup guide.</span></span> <span data-ttu-id="05de6-134">So geht es:</span><span class="sxs-lookup"><span data-stu-id="05de6-134">Here's how:</span></span>

1. <span data-ttu-id="05de6-135">Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "") Symbol **Unterstützte Einrichtung** und geben **Geschäftsdaten migrieren** ein.</span><span class="sxs-lookup"><span data-stu-id="05de6-135">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Assisted Setup**, and then choose **Migrate business data**.</span></span>
2. <span data-ttu-id="05de6-136">Befolgen Sie die Anweisungen für jeden Schritt im unterstützten Anleitungshandbuch.</span><span class="sxs-lookup"><span data-stu-id="05de6-136">Follow the instructions on each step in the assisted setup guide.</span></span>

## <a name="what-do-i-do-after-i-migrate-data"></a><span data-ttu-id="05de6-137">Was tue ich, nachdem ich Daten migriert habe?</span><span class="sxs-lookup"><span data-stu-id="05de6-137">What do I do after I migrate data?</span></span>
<span data-ttu-id="05de6-138">Nachdem Sie Daten migriert haben, haben die Transaktionen den Status **Nicht gebucht**, sodass Sie sie überprüfen und Korrekturen vornehmen können.</span><span class="sxs-lookup"><span data-stu-id="05de6-138">After you migrate data, transactions have the status **Unposted**, so you can review them and make adjustments.</span></span> <span data-ttu-id="05de6-139">Um die Transaktionen zu überprüfen, wechseln Sie zur Seite in der Sie normalerweise suchen müssen.</span><span class="sxs-lookup"><span data-stu-id="05de6-139">To review the transactions, go to the page where you would normally find them.</span></span> <span data-ttu-id="05de6-140">Beispielsweise um nicht gebuchten Verkaufsrechnungen zu überprüfen, gehen Sie zu der Seite **Verkaufsrechnungen**.</span><span class="sxs-lookup"><span data-stu-id="05de6-140">For example, to review unposted sales invoices, go to the **Sales Invoices** page.</span></span> <span data-ttu-id="05de6-141">Um Zahlungsausgangs Buch.-Blätter zu überprüfen, wechseln Sie zur Seite **Zlg.-Ausg. Buch.-Blätter**.</span><span class="sxs-lookup"><span data-stu-id="05de6-141">To review payment journals, go to the **Payment Journals** page.</span></span>   

<span data-ttu-id="05de6-142">Es gibt mehrere Dinge, die Sie durchführen sollten:</span><span class="sxs-lookup"><span data-stu-id="05de6-142">There are a few things in particular that you should do:</span></span>

* <span data-ttu-id="05de6-143">Wenn die Transaktionen in QuickBooks online Markup oder Rabattbeträge aufweisen, müssen Sie die Beträge zu den verwandten Transaktionen manuell hinzufügen, [!INCLUDE[d365fin](includes/d365fin_md.md)] bevor Sie diese buchen.</span><span class="sxs-lookup"><span data-stu-id="05de6-143">If the transactions in QuickBooks Online had markup or discount amounts, you must manually add the amounts to the related transactions in [!INCLUDE[d365fin](includes/d365fin_md.md)] before you post them.</span></span>
* <span data-ttu-id="05de6-144">Wenn Sie MwSt verwenden, können Sie eine Geschäftsbuchungsgruppe und eine Produktbuchungsgruppe "Buchungsmatrix Einrichtung" hinzufügen, sodass Sie MwSt.-Beträge buchen können.</span><span class="sxs-lookup"><span data-stu-id="05de6-144">If you are using value added tax (VAT), you may need to add a business posting group and a product posting group to the posting setup so that you can post VAT amounts.</span></span>
* <span data-ttu-id="05de6-145">Prüfen Sie die Startkapitale für Konten in der Finanzbuchhaltung.</span><span class="sxs-lookup"><span data-stu-id="05de6-145">Verify the beginning balances for accounts in the general ledger.</span></span> <span data-ttu-id="05de6-146">QuickBooks online speichert nicht den aktuellen Saldo für alle Konten, daher müssen Sie möglicherweise Startkapitale korrigieren.</span><span class="sxs-lookup"><span data-stu-id="05de6-146">QuickBooks Online does not store the current balance for all accounts, so you might need to correct beginning balances.</span></span>

## <a name="see-also"></a><span data-ttu-id="05de6-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05de6-147">See Also</span></span>
[<span data-ttu-id="05de6-148">Geschäftsdaten aus anderen Finanzsystemen importieren</span><span class="sxs-lookup"><span data-stu-id="05de6-148">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="05de6-149">[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="05de6-149">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  

