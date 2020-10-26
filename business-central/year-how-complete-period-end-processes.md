---
title: Optionale Aktivitäten beispielsweise für Abschlussperioden | Microsoft Docs
description: In diesem Thema werden die optionalen Vorgänge und Aktivitäten Abschlussbuchhaltungsperioden in  Business Central dargelegt.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 6526760c78cb11d8454b7f5390c6fefe713647d2
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3918238"
---
# <a name="overview-of-tasks-to-close-accounting-periods"></a><span data-ttu-id="1bab5-103">Überblick zu Aufgaben, Buchhaltungsperioden zu schließen</span><span class="sxs-lookup"><span data-stu-id="1bab5-103">Overview of Tasks to Close Accounting Periods</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="1bab5-104">zwingt Sie nicht, Perioden zu schließen, aber es gibt viele Aktivitäten am Periodenende (Monatsende), die Sie ausführen können.</span><span class="sxs-lookup"><span data-stu-id="1bab5-104">does not force you to close periods, however, there are many period-end (month-end) activities that you can do.</span></span> <span data-ttu-id="1bab5-105">Dieses Thema zeigt eine Übersicht von optionalen Vorgängen und Aktivitäten für Perioden, die bereitstehen.</span><span class="sxs-lookup"><span data-stu-id="1bab5-105">This topic provides an overview of optional processes and activities for closing periods.</span></span>  

## <a name="general-ledger"></a><span data-ttu-id="1bab5-106">Sachposten</span><span class="sxs-lookup"><span data-stu-id="1bab5-106">General Ledger</span></span>
* <span data-ttu-id="1bab5-107">Geben Sie systemweite und benutzerspezifische Buchungsperioden an.</span><span class="sxs-lookup"><span data-stu-id="1bab5-107">Specify system-wide and user-specific posting periods.</span></span>  

    <span data-ttu-id="1bab5-108">Dies gibt die Daten an, zwischen denen Buchungen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="1bab5-108">This specifies the dates between which you allow posting.</span></span> <span data-ttu-id="1bab5-109">Je nach Geschäftsanforderungen empfiehlt es sich, die Buchungsdatumsbereiche für Benutzer zu Beginn des Periodenabschlusses einzugrenzen.</span><span class="sxs-lookup"><span data-stu-id="1bab5-109">Depending on your business, you may want to allow posting at the start of the period, or toward the end.</span></span> <span data-ttu-id="1bab5-110">Weitere Informationen finden Sie unter [Abschließen von Buchhaltungsperioden](finance-how-specify-posting-periods.md).</span><span class="sxs-lookup"><span data-stu-id="1bab5-110">For more information, see [Specify Posting Periods](finance-how-specify-posting-periods.md).</span></span>  
* <span data-ttu-id="1bab5-111">Führen Sie alle notwendigen Sachpostenregulierungen durch.</span><span class="sxs-lookup"><span data-stu-id="1bab5-111">Make all necessary G/L adjustments.</span></span>  
* <span data-ttu-id="1bab5-112">Aktualisieren und buchen Sie wiederkehrende Buch.-Blätter.</span><span class="sxs-lookup"><span data-stu-id="1bab5-112">Update and post Recurring Journals.</span></span>  
  <!--* Process Consolidations-->
* <span data-ttu-id="1bab5-113">Führen Sie Kontenschemata wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="1bab5-113">Run account schedules as follows:</span></span>  
  * <span data-ttu-id="1bab5-114">Öffnen Sie die Seite **Kontenschema** und klicken Sie auf **Drucken** .</span><span class="sxs-lookup"><span data-stu-id="1bab5-114">Open the **Account Schedule** page, and then choose the **Print** action.</span></span>  

## <a name="sales-and-receivables"></a><span data-ttu-id="1bab5-115">Debitoren und Verkauf</span><span class="sxs-lookup"><span data-stu-id="1bab5-115">Sales and Receivables</span></span>
* <span data-ttu-id="1bab5-116">Alle Aufträge, Rechnungen, Gutschriften und Reklamationen werden gebucht.</span><span class="sxs-lookup"><span data-stu-id="1bab5-116">Post all sales orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="1bab5-117">Buchen Sie alle Barzahlungseingangs-Buch.-Blätter.</span><span class="sxs-lookup"><span data-stu-id="1bab5-117">Post all cash receipt journals.</span></span>  
* <span data-ttu-id="1bab5-118">Aktualisieren und buchen Sie wiederkehrende Buch.-Blätter, die sich auf Debitoren und Verkauf beziehen.</span><span class="sxs-lookup"><span data-stu-id="1bab5-118">Update and post recurring journals that are related to sales and receivables.</span></span>  
* <span data-ttu-id="1bab5-119">Stimmen Sie die Debitoren mit der Finanzbuchhaltung ab.</span><span class="sxs-lookup"><span data-stu-id="1bab5-119">Reconcile accounts receivable to the general ledger.</span></span>  
* <span data-ttu-id="1bab5-120">Führen Sie die Stapelverarbeitung **Fakturierte Aufträge löschen** aus.</span><span class="sxs-lookup"><span data-stu-id="1bab5-120">Run the **Delete Invoiced Sales Orders** batch job.</span></span>  

## <a name="purchases-and-payables"></a><span data-ttu-id="1bab5-121">Kreditoren und Einkauf</span><span class="sxs-lookup"><span data-stu-id="1bab5-121">Purchases and Payables</span></span>
* <span data-ttu-id="1bab5-122">Alle Aufträge, Rechnungen, Gutschriften und Reklamationen für Kreditoren werden gebucht.</span><span class="sxs-lookup"><span data-stu-id="1bab5-122">Post all purchase orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="1bab5-123">Buchen Sie das Zahlungsausgangs Buch.-Blatt.</span><span class="sxs-lookup"><span data-stu-id="1bab5-123">Post all payment journals.</span></span>  
* <span data-ttu-id="1bab5-124">Aktualisieren und buchen Sie wiederkehrende Buch.-Blätter, die sich auf Kreditoren und Einkäufe beziehen.</span><span class="sxs-lookup"><span data-stu-id="1bab5-124">Update and post recurring journals that are related to purchases & payables.</span></span>  
* <span data-ttu-id="1bab5-125">Führen Sie den Bericht **Kreditor - Saldenrückblick** aus, und stimmen Sie die Kreditoren mit der Finanzbuchhaltung ab.</span><span class="sxs-lookup"><span data-stu-id="1bab5-125">Run the **Aged Accounts Payable** report and reconcile accounts payable to the general ledger.</span></span>  
* <span data-ttu-id="1bab5-126">Führen Sie die Stapelverarbeitung **Erledigte fakturierte Bestellungen löschen** aus.</span><span class="sxs-lookup"><span data-stu-id="1bab5-126">Run the **Delete Invoiced Purchase Orders** batch job.</span></span>  

<span data-ttu-id="1bab5-127">Anlagen</span><span class="sxs-lookup"><span data-stu-id="1bab5-127">Fixed Assets</span></span>
* <span data-ttu-id="1bab5-128">Alle Wartungskosten wurden über die Anlagen-Buch.-Blätter oder Rechnungen gebucht.</span><span class="sxs-lookup"><span data-stu-id="1bab5-128">Post all maintenance costs have been posted through the fixed asset journals or invoices.</span></span>
* <span data-ttu-id="1bab5-129">Buchen Sie Regulierungen.</span><span class="sxs-lookup"><span data-stu-id="1bab5-129">Post adjustments.</span></span>
* <span data-ttu-id="1bab5-130">Buchen Sie die Zuschreibung.</span><span class="sxs-lookup"><span data-stu-id="1bab5-130">Post appreciation.</span></span>
* <span data-ttu-id="1bab5-131">Buchen Sie die Abschreibung.</span><span class="sxs-lookup"><span data-stu-id="1bab5-131">Post depreciation.</span></span>
* <span data-ttu-id="1bab5-132">Aktualisieren und buchen Sie das Buch.-Blatt für wiederkehrende Anlagen</span><span class="sxs-lookup"><span data-stu-id="1bab5-132">Update and post the recurring fixed asset journal.</span></span>

<span data-ttu-id="1bab5-133">Intercompany</span><span class="sxs-lookup"><span data-stu-id="1bab5-133">Intercompany</span></span>
* <span data-ttu-id="1bab5-134">Verarbeiten von Intercompanytransaktionen</span><span class="sxs-lookup"><span data-stu-id="1bab5-134">Process Intercompany Transactions</span></span>

## <a name="calculate-and-process-sales-tax"></a><span data-ttu-id="1bab5-135">Berechnen und erfassen Sie die MwSt.</span><span class="sxs-lookup"><span data-stu-id="1bab5-135">Calculate and Process Sales Tax</span></span>
* <span data-ttu-id="1bab5-136">Schließen Sie Steuer-Abrechnungen ab.</span><span class="sxs-lookup"><span data-stu-id="1bab5-136">Complete Tax Statements.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1bab5-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1bab5-137">See Also</span></span>
[<span data-ttu-id="1bab5-138">Beenden von Jahresabschluss und Perioden</span><span class="sxs-lookup"><span data-stu-id="1bab5-138">Closing Years and Periods</span></span>](year-close-years-periods.md)  
[<span data-ttu-id="1bab5-139">Schließen der Bücher</span><span class="sxs-lookup"><span data-stu-id="1bab5-139">Closing Books</span></span>](year-close-books.md)  
<span data-ttu-id="1bab5-140">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1bab5-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
