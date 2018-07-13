---
title: Einrichten von Prozessen in Financials | Microsoft Docs
description: "Informationen zu Aufgaben, Finanzen in Ihrem Unternehmen einzurichten, um Ihrer Buchhaltung, oder Buchhaltungsanforderungen Prüfungen zu entsprechen."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 05/31/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: 025c00e6013e773204a12abc7d86c09b3dcef3dd
ms.contentlocale: de-de
ms.lasthandoff: 06/28/2018

---
# <a name="setting-up-finance"></a><span data-ttu-id="9b830-103">Finance einrichten</span><span class="sxs-lookup"><span data-stu-id="9b830-103">Setting Up Finance</span></span>
<span data-ttu-id="9b830-104">Damit Sie sich rasch zurechtfinden, enthält [!INCLUDE[d365fin](includes/d365fin_md.md)] Standardkonfigurationen für die meisten Finanzprozesse.</span><span class="sxs-lookup"><span data-stu-id="9b830-104">To help you get going quickly, [!INCLUDE[d365fin](includes/d365fin_md.md)] includes standard configurations for most financial processes.</span></span> <span data-ttu-id="9b830-105">Wenn Sie die Konfiguration ändern müssen, um Ihrem Geschäft zu entsprechen, tun Sie es.</span><span class="sxs-lookup"><span data-stu-id="9b830-105">If you need to change the configurations to suit your business, go right ahead.</span></span> <span data-ttu-id="9b830-106">Sei können vom Rollencenter auf eine unterstützte Einrichtung zugreifen, die Sie bespielsweise dabei unterstützt, Verkaufssteuer abhängig von Ihrem Standort einzurichten.</span><span class="sxs-lookup"><span data-stu-id="9b830-106">For example, from the Role Center, you can use an assisted setup guide to set up sales tax rate for your location.</span></span>  

<span data-ttu-id="9b830-107">Es gibt jedoch mehrere Elemente, die Sie selber einrichten müssen.</span><span class="sxs-lookup"><span data-stu-id="9b830-107">However, there are some things you need to set up yourself.</span></span> <span data-ttu-id="9b830-108">Wenn Sie Dimensionen als Grundlage für Business Intelligence verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="9b830-108">For example, if you want to use dimensions as a basis for business intelligence.</span></span>  

<span data-ttu-id="9b830-109">In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.</span><span class="sxs-lookup"><span data-stu-id="9b830-109">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="9b830-110">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="9b830-110">To</span></span> | <span data-ttu-id="9b830-111">Siehe</span><span class="sxs-lookup"><span data-stu-id="9b830-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="9b830-112">Wählen Sie aus, wie Sie Ihre Kreditoren bezahlen.</span><span class="sxs-lookup"><span data-stu-id="9b830-112">Choose how you pay your vendors.</span></span> |[<span data-ttu-id="9b830-113">Zahlungsformen definieren</span><span class="sxs-lookup"><span data-stu-id="9b830-113">Defining Payment Methods</span></span>](finance-payment-methods.md) |
| <span data-ttu-id="9b830-114">Buchungsgruppenzuordnungseinheiten nach Debitoren, Kreditoren, Artikel, Ressourcen und Einkaufs- und Verkaufsbelegen mit Sachkonten.</span><span class="sxs-lookup"><span data-stu-id="9b830-114">Specify the posting groups that map entities like customers, vendors, items, resources, and sales and purchase documents to general ledger accounts.</span></span> |[<span data-ttu-id="9b830-115">Buchungsgruppen einrichten</span><span class="sxs-lookup"><span data-stu-id="9b830-115">Setting Up Posting Groups</span></span>](finance-posting-groups.md)|
|<span data-ttu-id="9b830-116">Erstellen Sie Kontenschemata und definieren hiermit Kontengruppen, um den Inhalt aus Finanzdiagrammen und Berichte, wie den Bilanz- und GuV-Berichten zu definieren.</span><span class="sxs-lookup"><span data-stu-id="9b830-116">Create account schedules and define account categories to define the contents of financial charts and reports, such as the Balance Sheet and Income Statement reports.</span></span>|[<span data-ttu-id="9b830-117">Bereiten Sie Finanzberichte mit Kontenschemata und Kontengruppen vor</span><span class="sxs-lookup"><span data-stu-id="9b830-117">Prepare Financial Reporting with Account Schedules and Account Categories</span></span>](bi-how-work-account-schedule.md)|
|<span data-ttu-id="9b830-118">Einrichtung einer Toleranz, mit der das System eine Rechnung schließt, selbst wenn die Zahlung einschließlich aller Rabatte nicht vollständig den Betrag der Rechnung abdeckt.</span><span class="sxs-lookup"><span data-stu-id="9b830-118">Set up a tolerance by which the system closes an invoice even though the payment, including any discount, does not fully cover the amount on the invoice.</span></span>|[<span data-ttu-id="9b830-119">Mit Zahlungstoleranzen und Skontotoleranzen arbeiten</span><span class="sxs-lookup"><span data-stu-id="9b830-119">Work with Payment Tolerances and Payment Discount Tolerances</span></span>](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| <span data-ttu-id="9b830-120">Einrichten von Finanzzeiträumen</span><span class="sxs-lookup"><span data-stu-id="9b830-120">Set up fiscal periods.</span></span> |[<span data-ttu-id="9b830-121">Ein neues Geschäftsjahres eröffnen</span><span class="sxs-lookup"><span data-stu-id="9b830-121">Open a New Fiscal Year</span></span>](finance-how-open-new-fiscal-year.md) |
| <span data-ttu-id="9b830-122">Definieren Sie, wie Sie Dienstleistungssteuerbeträge erstellen, die Sie für Verkäufe an das Finanzamt eingetrieben haben.</span><span class="sxs-lookup"><span data-stu-id="9b830-122">Define how you report value-added tax amounts that you have collected for sales to the tax authorities.</span></span> |[<span data-ttu-id="9b830-123">So gehts: Melden von MwSt. an die Steuerbehörden</span><span class="sxs-lookup"><span data-stu-id="9b830-123">How To: Report VAT to Tax Authorities</span></span>](finance-how-report-vat.md)|
| <span data-ttu-id="9b830-124">Einrichten Ihrer Verkaufs- und Einkaufsfunktionen, um Zahlungen in Fremdwährungen abzuwickeln.</span><span class="sxs-lookup"><span data-stu-id="9b830-124">Set your Sales and Purchases features up to handle payments in foreign currencies.</span></span>|[<span data-ttu-id="9b830-125">Anwendung von Kreditorenposten in unterschiedlichen Währungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="9b830-125">Enable Application of Ledger Entries in Different Currencies</span></span>](finance-how-enable-application-ledger-entries-different-currencies.md)
| <span data-ttu-id="9b830-126">Fügen Sie dem bestehenden Kontenplan neue Konten hinzu.</span><span class="sxs-lookup"><span data-stu-id="9b830-126">Add new accounts to the existing chart of accounts.</span></span> |[<span data-ttu-id="9b830-127">Einrichten des Kontenplans</span><span class="sxs-lookup"><span data-stu-id="9b830-127">Setting Up the Chart of Accounts</span></span>](finance-setup-chart-accounts.md) |
| <span data-ttu-id="9b830-128">Einrichten Business Intelligence (BI)- Diagrammen, um Cashflow zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="9b830-128">Set up business intelligence (BI) charts to analyze cash flow.</span></span> |[<span data-ttu-id="9b830-129">Einrichten der Cashflowanalyse</span><span class="sxs-lookup"><span data-stu-id="9b830-129">Setting Up Cash Flow Analysis</span></span>](finance-setup-cash-flow-analyses.md) |
|<span data-ttu-id="9b830-130">Aktivierung der Rechnungstellung für einen Kunden, der nicht im System eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="9b830-130">Enable invoicing of a customer who is not set up in the system.</span></span>|[<span data-ttu-id="9b830-131">Barkunden einrichten</span><span class="sxs-lookup"><span data-stu-id="9b830-131">Set Up Cash Customers</span></span>](finance-how-to-set-up-cash-customers.md)|
| <span data-ttu-id="9b830-132">Einrichtung von Intrastat-Berichten und Übermitteln des Berichts an eine Behörde</span><span class="sxs-lookup"><span data-stu-id="9b830-132">Set up Intrastat reporting, and submit the report to an authority</span></span> | [<span data-ttu-id="9b830-133">Einrichten und Berichten von Intrastat</span><span class="sxs-lookup"><span data-stu-id="9b830-133">Set Up and Report Intrastat</span></span>](finance-how-setup-report-intrastat.md)|

## <a name="see-also"></a><span data-ttu-id="9b830-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b830-134">See Also</span></span>
[<span data-ttu-id="9b830-135">Finanzen</span><span class="sxs-lookup"><span data-stu-id="9b830-135">Finance</span></span>](finance.md)  
[<span data-ttu-id="9b830-136">Verwalten von Bankkonten</span><span class="sxs-lookup"><span data-stu-id="9b830-136">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="9b830-137">Arbeiten mit Dimensionen</span><span class="sxs-lookup"><span data-stu-id="9b830-137">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="9b830-138">Geschäftsdaten aus anderen Finanzsystemen importieren</span><span class="sxs-lookup"><span data-stu-id="9b830-138">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="9b830-139">Analysieren von Cashflow in Ihren Mandanten</span><span class="sxs-lookup"><span data-stu-id="9b830-139">Analyzing Cash Flow in Your Company</span></span>](finance-analyze-cash-flow.md)  
<span data-ttu-id="9b830-140">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9b830-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

