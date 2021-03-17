---
title: QuickBooks Online-Migrationserweiterung | Microsoft Docs
description: Beschreibt, wie die Erweiterung verwendet wird, um Debitoren, Kreditoren, Artikel und Konten aus QuickBooks Online zu Business Central zu migrieren.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, QuickBooks, import
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 6eb05acc55c86ce8547c2b18b933d669787583d4
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386399"
---
# <a name="the-quickbooks-online-data-migration-extension"></a><span data-ttu-id="0eabb-103">Die QuickBooks Online-Datenmigrations-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="0eabb-103">The QuickBooks Online Data Migration Extension</span></span>

<span data-ttu-id="0eabb-104">Diese Erweiterung ist im unterstützten Einrichtungshandbuch **Datenmigration** enthalten, um Ihnen zu helfen, wichtige Geschäftsdaten von QuickBooks Online zu [!INCLUDE[prod_short](includes/prod_short.md)] zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="0eabb-104">This extension is included in the **Data Migration** assisted setup guide to help you migrate important business data from QuickBooks Online to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="0eabb-105">Dies ist beispielsweise dann nützlich, wenn Ihr Unternehmen wächst und Sie sich entschieden haben, Ihre Geschäftsführungs-App zu aktualisieren, indem Sie mit [!INCLUDE[prod_short](includes/prod_short.md)] verwenden.</span><span class="sxs-lookup"><span data-stu-id="0eabb-105">For example, this is useful when your business is growing, and you've decided to upgrade your business management app by starting to use [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

## <a name="what-data-can-i-import-from-quickbooks-online"></a><span data-ttu-id="0eabb-106">Welche Daten kann ich von QuickBooks Online importieren?</span><span class="sxs-lookup"><span data-stu-id="0eabb-106">What data can I import from QuickBooks Online?</span></span>

<span data-ttu-id="0eabb-107">Sie können die folgenden Daten von QuickBooks Online in [!INCLUDE[prod_short](includes/prod_short.md)] importieren:</span><span class="sxs-lookup"><span data-stu-id="0eabb-107">You can import the following data from QuickBooks Online to [!INCLUDE[prod_short](includes/prod_short.md)]:</span></span>  

* <span data-ttu-id="0eabb-108">Debitoren</span><span class="sxs-lookup"><span data-stu-id="0eabb-108">Customers</span></span>
* <span data-ttu-id="0eabb-109">Kreditoren</span><span class="sxs-lookup"><span data-stu-id="0eabb-109">Vendors</span></span>
* <span data-ttu-id="0eabb-110">Artikel</span><span class="sxs-lookup"><span data-stu-id="0eabb-110">Items</span></span>
* <span data-ttu-id="0eabb-111">Kontenplan</span><span class="sxs-lookup"><span data-stu-id="0eabb-111">Chart of accounts</span></span>
* <span data-ttu-id="0eabb-112">Saldovortragtransaktion in der Finanzbuchhaltung</span><span class="sxs-lookup"><span data-stu-id="0eabb-112">Beginning balance transaction in the general ledger</span></span>
* <span data-ttu-id="0eabb-113">Verfügbare Mengen für Lagerartikel</span><span class="sxs-lookup"><span data-stu-id="0eabb-113">On-hand quantities for inventory items</span></span>
* <span data-ttu-id="0eabb-114">Offene Dokumente für Debitoren und Kreditoren, wie beispielsweise Rechnungen, Gutschriften und Zahlungen</span><span class="sxs-lookup"><span data-stu-id="0eabb-114">Open documents for customers and vendors, such as invoices, credit memos, and payments</span></span>

<span data-ttu-id="0eabb-115">Es migrieren nur Gesamtbeträge auf Einkaufs- und Verkaufsbelegen.</span><span class="sxs-lookup"><span data-stu-id="0eabb-115">We migrate only full amounts on sales and purchase documents.</span></span> <span data-ttu-id="0eabb-116">Wir aktualisieren keine teilweise bezahlten Beträge.</span><span class="sxs-lookup"><span data-stu-id="0eabb-116">We do not update partially paid amounts.</span></span> <span data-ttu-id="0eabb-117">Wenn ein Debitor 300 von insgesamt 500 Dollar einer Verkaufsrechnung bezahlt hat, migrieren wir die vollständigen 500.</span><span class="sxs-lookup"><span data-stu-id="0eabb-117">For example, if a customer has paid 300 of a total of 500 dollars on a sales invoice, we migrate the full 500.</span></span> <span data-ttu-id="0eabb-118">Wenn Sie Teilzahlungen erhalten, müssen Sie diese manuell aktualisieren, entweder, vor oder nach dem Sie Daten migrieren.</span><span class="sxs-lookup"><span data-stu-id="0eabb-118">If you have received partial payments, you must update these manually, either before or after you migrate data.</span></span> <span data-ttu-id="0eabb-119">Es ist empfehlenswert, ausstehende Transaktionen anzuwenden, bevor Sie migrieren, das ist einfacher danach.</span><span class="sxs-lookup"><span data-stu-id="0eabb-119">We recommend that you apply outstanding transactions before you migrate, just to make things easier afterward.</span></span>

> [!NOTE]  
> <span data-ttu-id="0eabb-120">Wir migrieren keine Einkaufsbestellungen oder Verkaufsaufträge.</span><span class="sxs-lookup"><span data-stu-id="0eabb-120">We do not migrate purchase orders or sales orders.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="0eabb-121">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="0eabb-121">Before you start</span></span>

<span data-ttu-id="0eabb-122">Ein wichtiger Teil des Migrationsvorgangs ist es, Konten anzugeben, um Transaktionen zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="0eabb-122">An important part of the migration process is to specify the accounts to migrate transactions to.</span></span> <span data-ttu-id="0eabb-123">Es ist empfehlenswert, diese Zuordnung zu planen, bevor Sie Daten migrieren.</span><span class="sxs-lookup"><span data-stu-id="0eabb-123">It's a good idea to plan this mapping before you migrate data.</span></span> <span data-ttu-id="0eabb-124">Beispielsweise die Konten, die Sie für Transaktionen buchen:</span><span class="sxs-lookup"><span data-stu-id="0eabb-124">For example, the accounts where you post transactions for:</span></span>  

* <span data-ttu-id="0eabb-125">Der Verkauf von Artikeln oder Services an einen Debitoren.</span><span class="sxs-lookup"><span data-stu-id="0eabb-125">The sale of items or services to customers.</span></span>
* <span data-ttu-id="0eabb-126">Der Kauf von Waren oder Dienste von einem Kreditor.</span><span class="sxs-lookup"><span data-stu-id="0eabb-126">The purchase of items or services from vendors.</span></span>  
* <span data-ttu-id="0eabb-127">Änderungen in der Finanzbuchhaltung.</span><span class="sxs-lookup"><span data-stu-id="0eabb-127">Adjustments in the general ledger.</span></span>  

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="0eabb-128">erfordert, dass Sachkonten die Kontonummern haben, die ihm zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="0eabb-128">requires that general ledger accounts have account numbers assigned to them.</span></span> <span data-ttu-id="0eabb-129">Überprüfen Sie, ob Kontonummern Ihren Konten in QuickBooks Online zugeordnet wurden.</span><span class="sxs-lookup"><span data-stu-id="0eabb-129">Make sure that account numbers are assigned to your accounts in QuickBooks Online.</span></span>

<span data-ttu-id="0eabb-130">Wenn Transaktionen in QuickBooks Online Steuerbeträge haben, müssen Sie ein Steuerkonto für Ihre Steuerzuständigkeiten in [!INCLUDE[prod_short](includes/prod_short.md)] einrichten, bevor Sie Buchungen durchführen können.</span><span class="sxs-lookup"><span data-stu-id="0eabb-130">If transactions in QuickBooks Online have tax amounts, you must set up a tax account for your tax jurisdictions in [!INCLUDE[prod_short](includes/prod_short.md)] before you can post transactions.</span></span>

## <a name="how-do-i-start-using-the-extension"></a><span data-ttu-id="0eabb-131">Wie beginne ich, die Erweiterung zu nutzen?</span><span class="sxs-lookup"><span data-stu-id="0eabb-131">How do I start using the extension?</span></span>

<span data-ttu-id="0eabb-132">Erste Schritte sind einfach.</span><span class="sxs-lookup"><span data-stu-id="0eabb-132">Getting started is easy.</span></span> <span data-ttu-id="0eabb-133">Sie müssen nur das unterstütze Einrichtungshandbuch **Datenmigration** ausführen.</span><span class="sxs-lookup"><span data-stu-id="0eabb-133">All you need to do is run the **Data Migration** assisted setup guide.</span></span> <span data-ttu-id="0eabb-134">So geht es:</span><span class="sxs-lookup"><span data-stu-id="0eabb-134">Here's how:</span></span>

1. <span data-ttu-id="0eabb-135">Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Unterstützte Einrichtung** ein, und wählen Sie dann **Geschäftsdaten migrieren**.</span><span class="sxs-lookup"><span data-stu-id="0eabb-135">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Assisted Setup**, and then choose **Migrate business data**.</span></span>
2. <span data-ttu-id="0eabb-136">Befolgen Sie die Anweisungen für jeden Schritt im unterstützten Anleitungshandbuch.</span><span class="sxs-lookup"><span data-stu-id="0eabb-136">Follow the instructions on each step in the assisted setup guide.</span></span>

## <a name="what-do-i-do-after-i-migrate-data"></a><span data-ttu-id="0eabb-137">Was tue ich, nachdem ich Daten migriert habe?</span><span class="sxs-lookup"><span data-stu-id="0eabb-137">What do I do after I migrate data?</span></span>

<span data-ttu-id="0eabb-138">Nachdem Sie Daten migriert haben, haben die Transaktionen den Status **Nicht gebucht**, sodass Sie sie überprüfen und Korrekturen vornehmen können.</span><span class="sxs-lookup"><span data-stu-id="0eabb-138">After you migrate data, transactions have the status **Unposted**, so you can review them and make adjustments.</span></span> <span data-ttu-id="0eabb-139">Um die Transaktionen zu überprüfen, wechseln Sie zur Seite in der Sie normalerweise suchen müssen.</span><span class="sxs-lookup"><span data-stu-id="0eabb-139">To review the transactions, go to the page where you would normally find them.</span></span> <span data-ttu-id="0eabb-140">Beispielsweise um nicht gebuchten Verkaufsrechnungen zu überprüfen, gehen Sie zu der Seite **Verkaufsrechnungen**.</span><span class="sxs-lookup"><span data-stu-id="0eabb-140">For example, to review unposted sales invoices, go to the **Sales Invoices** page.</span></span> <span data-ttu-id="0eabb-141">Um Zahlungsausgangs Buch.-Blätter zu überprüfen, wechseln Sie zur Seite **Zlg.-Ausg. Buch.-Blätter**.</span><span class="sxs-lookup"><span data-stu-id="0eabb-141">To review payment journals, go to the **Payment Journals** page.</span></span>  

<span data-ttu-id="0eabb-142">Es gibt mehrere Dinge, die Sie durchführen sollten:</span><span class="sxs-lookup"><span data-stu-id="0eabb-142">There are a few things in particular that you should do:</span></span>

* <span data-ttu-id="0eabb-143">Wenn die Transaktionen in QuickBooks Online Aufschläge oder Rabattbeträge aufweisen, müssen Sie die Beträge manuell zu den verwandten Transaktionen in [!INCLUDE[prod_short](includes/prod_short.md)] hinzufügen, bevor Sie diese buchen.</span><span class="sxs-lookup"><span data-stu-id="0eabb-143">If the transactions in QuickBooks Online had markup or discount amounts, you must manually add the amounts to the related transactions in [!INCLUDE[prod_short](includes/prod_short.md)] before you post them.</span></span>
* <span data-ttu-id="0eabb-144">Wenn Sie MwSt verwenden, können Sie eine Geschäftsbuchungsgruppe und eine Produktbuchungsgruppe "Buchungsmatrix Einrichtung" hinzufügen, sodass Sie MwSt.-Beträge buchen können.</span><span class="sxs-lookup"><span data-stu-id="0eabb-144">If you are using value added tax (VAT), you may need to add a business posting group and a product posting group to the posting setup so that you can post VAT amounts.</span></span>
* <span data-ttu-id="0eabb-145">Prüfen Sie die Startkapitale für Konten in der Finanzbuchhaltung.</span><span class="sxs-lookup"><span data-stu-id="0eabb-145">Verify the beginning balances for accounts in the general ledger.</span></span> <span data-ttu-id="0eabb-146">QuickBooks Online speichert nicht den aktuellen Saldo für alle Konten, daher müssen Sie möglicherweise Startkapitale korrigieren.</span><span class="sxs-lookup"><span data-stu-id="0eabb-146">QuickBooks Online does not store the current balance for all accounts, so you might need to correct beginning balances.</span></span>

## <a name="see-also"></a><span data-ttu-id="0eabb-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0eabb-147">See Also</span></span>

[<span data-ttu-id="0eabb-148">Importieren von Geschäftsdaten aus anderen Finanzsystemen</span><span class="sxs-lookup"><span data-stu-id="0eabb-148">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="0eabb-149">[Anpassen [!INCLUDE[prod_short](includes/prod_short.md)] über Erweiterungen](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="0eabb-149">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]