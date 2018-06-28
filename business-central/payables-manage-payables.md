---
title: "Überblick der Aufgaben zum Verwalten von Debitoren | Microsoft Docs"
description: "Gliedert Aufgaben, um Debitoren zu verwalten, beispielsweise zahlende Gläubiger oder ausgehende Zahlungen an Buch-Posten, um Rechnungen oder Gutschriften zu schließen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: 730596534df93b7aa16f7975b5c5b1307a7f571a
ms.contentlocale: de-de
ms.lasthandoff: 06/28/2018

---
# <a name="managing-payables"></a><span data-ttu-id="70a46-103">Verwalten von Verbindlichkeiten</span><span class="sxs-lookup"><span data-stu-id="70a46-103">Managing Payables</span></span>
<span data-ttu-id="70a46-104">Ein Teil der Verwaltung großer aus das Wareneinkaufskonto zahlt Ihre Kreditoren oder erstattet Mitarbeiter für Ausgaben zurück.</span><span class="sxs-lookup"><span data-stu-id="70a46-104">A big part of managing accounts payable is paying your vendors, or reimbursing your employees for expenses.</span></span> <span data-ttu-id="70a46-105">Sie können Funktionalität verwenden, um das Fenster **Zahlung Buch.-Blatt** automatisch mit Zahlungszeilen für fällige Einkaufsrechnungen auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="70a46-105">You can use functions to add payments lines for purchase invoices that are due in the **Payment Journal** window.</span></span> <span data-ttu-id="70a46-106">Um die entsprechenden Banktransaktionen schnell auszuführen, können Sie mehrere Zahlungsausgangs Buch.-Blattzeilen in eine Datei exportieren, die Sie dann für Ihre Bank für die Verarbeitung hochladen.</span><span class="sxs-lookup"><span data-stu-id="70a46-106">To send transactions to your bank, you can export multiple payment journal lines to a file, and then upload the file to your bank.</span></span> <span data-ttu-id="70a46-107">Sie können Zahlungen auch mit Scheck leisten inkl. der Möglichkeit, Schecks als elektronisches Zahlungsmittel zu senden.</span><span class="sxs-lookup"><span data-stu-id="70a46-107">You can also make payments by check, including transmitting checks as electronic payments.</span></span>

<span data-ttu-id="70a46-108">Eine weitere typische Aufgabe ist es, ausgehenden Zahlungen dem zugehörigen Debitor bzw. einem Kreditorenposten zuzuordnen, um die entsprechenden Einkaufsrechnungen oder Einkaufsgutschriften zu schließen, wenn sie bezahlt sind.</span><span class="sxs-lookup"><span data-stu-id="70a46-108">Another typical task is to apply outgoing payments to their related vendor or employee ledger entries in order to close purchase invoices, purchase credit memos, or employee accounts as paid.</span></span> <span data-ttu-id="70a46-109">Diese Aufgabe können Sie dann im Fenster **Zahlungs-Abstimmungs-Buch.-Blatt** ausführen, indem Sie eine Bankkontoauszugsdatei importieren, um die Zahlungen schnell zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="70a46-109">You can do this in the **Payment Reconciliation Journal** window by importing a bank statement file to register the payments.</span></span> <span data-ttu-id="70a46-110">Die Zahlungen werden angewendet, um Debitoren- oder Kreditorenposten zu öffnen, indem passender Zahlungstext und Zahlungsinformationen verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="70a46-110">The payments are applied to open vendor, customer, or employee ledger entries by matching payment text and entry information.</span></span> <span data-ttu-id="70a46-111">Es gibt verschiedene Arten, die Übereinstimmungen zu prüfen und zu ändern, bevor Sie das Buch.-Blatt buchen.</span><span class="sxs-lookup"><span data-stu-id="70a46-111">There are various ways to review and change the matches before you post the journal.</span></span> <span data-ttu-id="70a46-112">Sie können die offenen Bankkontoposten für ausgeglichenen Posten schließen, wenn Sie das Buch.-Blatt buchen.</span><span class="sxs-lookup"><span data-stu-id="70a46-112">You can choose to close any open bank account ledger entries related to the applied ledger entries when you post the journal.</span></span> <span data-ttu-id="70a46-113">Das bedeutet, dass das Bankkonto automatisch abgestimmt wird, wenn alle Zahlungen ausgeglichen werden.</span><span class="sxs-lookup"><span data-stu-id="70a46-113">The bank account is automatically reconciled when all payments are applied.</span></span>

<span data-ttu-id="70a46-114">Alternativ können Sie ausgehende Zahlungen im **Zahlungsausgangs Buch.-Blatt**-Fenster oder aus den zugehörigen Kreditorenposten manuell ausgleichen.</span><span class="sxs-lookup"><span data-stu-id="70a46-114">Alternatively, you can apply outgoing payments manually in the **Payment Journal** window or from the related vendor or employee ledger entries.</span></span>

<span data-ttu-id="70a46-115">Die folgende Tabelle enthält eine Abfolge von Aufgaben sowie Links zu den Kreditoren, in denen diese Aufgaben erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="70a46-115">The following table describes a sequence of tasks within accounts payable, with links to the topics that describe them.</span></span>

| <span data-ttu-id="70a46-116">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="70a46-116">To</span></span> | <span data-ttu-id="70a46-117">Siehe</span><span class="sxs-lookup"><span data-stu-id="70a46-117">See</span></span> |
| --- | --- |
| <span data-ttu-id="70a46-118">Generieren von Fälligkeitsdatum oder Kreditorenzahlungen oder Mitarbeitervergütungen, bereiten Sie Scheckzahlungen vor und exportieren sie Zahlungen beim Buchen an eine Bank.</span><span class="sxs-lookup"><span data-stu-id="70a46-118">Generate due vendor payments or employee reimbursements, prepare check payments, and export payments to a bank file when posting.</span></span> |[<span data-ttu-id="70a46-119">Zahlungen vornehmen</span><span class="sxs-lookup"><span data-stu-id="70a46-119">Making Payments</span></span>](payables-make-payments.md) |
| <span data-ttu-id="70a46-120">Gleichen Sie Kreditorenzahlungen automatisch für unbezahlte Einkaufsrechnungen aus, indem Sie eine Bankkontoauszugsdatei importieren.</span><span class="sxs-lookup"><span data-stu-id="70a46-120">Apply vendor payments automatically to unpaid purchase invoices by importing a bank statement file.</span></span> |[<span data-ttu-id="70a46-121">Zahlungen automatisch vornehmen und Bankkonten abstimmen</span><span class="sxs-lookup"><span data-stu-id="70a46-121">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="70a46-122">Gleichen Sie Kreditorenzahlungen für unbezahlten Einkaufsrechnungen manuell aus.</span><span class="sxs-lookup"><span data-stu-id="70a46-122">Apply vendor payments to unpaid purchase invoices manually.</span></span> |[<span data-ttu-id="70a46-123">Manuelle Abstimmung von Debitorenzahlungen</span><span class="sxs-lookup"><span data-stu-id="70a46-123">Reconcile Vendor Payments Manually</span></span>](payables-how-apply-purchase-transactions-manually.md) |
|<span data-ttu-id="70a46-124">Um eine korrekte Bewertung sicherzustellen, müssen Ihre Lagerartikel Kosten wie Fracht, Versicherung, Umlagerung und Transport enthalten, die beim Kauf oder Verkauf entstehen.</span><span class="sxs-lookup"><span data-stu-id="70a46-124">Ensure correct inventory valuation by assigning added item costs, such as freight, physical handling, insurance, and transportation that you incur when purchasing.</span></span>|[<span data-ttu-id="70a46-125">Verwenden von Artikelzuschlägen für zusätzliche Kosten</span><span class="sxs-lookup"><span data-stu-id="70a46-125">Use Item Charges to Account for Additional Trade Costs</span></span>](payables-how-assign-item-charges.md)|

## <a name="see-also"></a><span data-ttu-id="70a46-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70a46-126">See Also</span></span>
[<span data-ttu-id="70a46-127">Einkauf</span><span class="sxs-lookup"><span data-stu-id="70a46-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="70a46-128">Verwalten von Forderungen</span><span class="sxs-lookup"><span data-stu-id="70a46-128">Managing Receivables</span></span>](receivables-manage-receivables.md)  
[<span data-ttu-id="70a46-129">Verwenden von Artikelzuschlägen für zusätzliche Kosten</span><span class="sxs-lookup"><span data-stu-id="70a46-129">Use Item Charges to Account for Additional Trade Costs</span></span>](payables-how-assign-item-charges.md)  
[<span data-ttu-id="70a46-130">Allgemeine Geschäftsfunktionen</span><span class="sxs-lookup"><span data-stu-id="70a46-130">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="70a46-131">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="70a46-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

