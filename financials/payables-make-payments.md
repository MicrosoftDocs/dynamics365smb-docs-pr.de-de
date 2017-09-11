---
title: "Überblick der Aufgaben zum Verwalten von Zahlungen an Debitoren | Microsoft Docs"
description: "Gliederungen ihm eine Arbeit, um Zahlungen an Kreditoren oder zu den Gläubigern, einschließlich Buchungszahlungszeilen und das Anzeigen einer Übersicht über den fälligen Saldo zu verwalten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d0b9020596484a8910db2f5720adfe159ad96fe7
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017


---
# <a name="make-payments"></a><span data-ttu-id="7d32b-103">Zahlungen vornehmen</span><span class="sxs-lookup"><span data-stu-id="7d32b-103">Make Payments</span></span>
<span data-ttu-id="7d32b-104">Wenn Sie Zahlungen an Kreditoren leisten, buchen Sie die jeweiligen Zahlungszeilen im **Zahlungsausgangs Buch.-Blatt**-Fenster.</span><span class="sxs-lookup"><span data-stu-id="7d32b-104">When you make payments to vendors, you post the related payment lines in the **Payment Journal** window.</span></span> <span data-ttu-id="7d32b-105">Verwenden Sie zum Suchen fälliger Zahlungen im Zahlungsausgangs Buch.-Blatt die Funktion **Zahlungsvorschlag**.</span><span class="sxs-lookup"><span data-stu-id="7d32b-105">You can use the **Suggest Vendor Payments** function to find payments that are due.</span></span> <span data-ttu-id="7d32b-106">Darüber hinaus können Sie sich mithilfe des Berichts **Kreditor - Saldo nach Perioden** einen Überblick über die fälligen Zahlungen verschaffen.</span><span class="sxs-lookup"><span data-stu-id="7d32b-106">You can also use the **Vendor - Summary Aging** report to get an overview of due payments.</span></span>

<span data-ttu-id="7d32b-107">Im Zahlungsausgangs Buch.-Blatt können Sie Computerschecks drucken sowie ausgestellte Schecks erfassen.</span><span class="sxs-lookup"><span data-stu-id="7d32b-107">From the payment journal, you can print computer checks or record when checks are written.</span></span> <span data-ttu-id="7d32b-108">Wenn Sie **Computer Scheck** im Feld **Bankkontozahlungsart** wählen, dann müssen alle Posten für Schecks gedruckt werden, damit die Buch.-Blattzeilen gebucht werden können.</span><span class="sxs-lookup"><span data-stu-id="7d32b-108">If you select **Computer Check** in the **Bank Payment Type** field, then any lines representing checks must be printed before the payment journal can be posted.</span></span>

<span data-ttu-id="7d32b-109">Wenn Zahlungen gebucht werden, exportieren Sie sie in eine Bankdatei für den Upload zu Ihrer Bank zur Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="7d32b-109">When the payments are posted, you can export them to a bank file for upload to your bank for processing.</span></span>

<span data-ttu-id="7d32b-110">Nachdem die Zahlungen in Ihrer Bank getätigt wurden, müssen Sie diese in ihre entsprechenden offenen Kreditorenposten ausgleichen.</span><span class="sxs-lookup"><span data-stu-id="7d32b-110">After the payments are made at your bank, you must apply them to their related open vendor ledger entries.</span></span> <span data-ttu-id="7d32b-111">Sie können dies manuell oder über den Import in eine Bankkontoauszugsdatei und das Automatische Ausgleichen der Zahlungen durchführen.</span><span class="sxs-lookup"><span data-stu-id="7d32b-111">You can do this manually or by importing a bank statement file and applying the payments automatically.</span></span> <span data-ttu-id="7d32b-112">Weitere Informationen finden Sie unter [Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="7d32b-112">For more information, see [Apply Payments Automatically and Reconcile Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span>

<span data-ttu-id="7d32b-113">Die folgende Tabelle enthält eine Abfolge von Aufgaben sowie Links zu den entsprechenden Themen, in denen diese Aufgaben erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="7d32b-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="7d32b-114">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="7d32b-114">To</span></span> | <span data-ttu-id="7d32b-115">Siehe</span><span class="sxs-lookup"><span data-stu-id="7d32b-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="7d32b-116">Verwenden Sie die Funktion, um Kreditorenzahlungen entsprechend gewählten Kriterien, wie Fälligkeitsdatum, Skontoeignung und Ihrer Liquidität vorzuschlagen.</span><span class="sxs-lookup"><span data-stu-id="7d32b-116">Use a function to suggest vendor payments according to selected criteria, such as due date, discount eligibility, and your liquidity.</span></span> |[<span data-ttu-id="7d32b-117">Vorgehensweise: Erstellen von Zahlungsvorschlägen für Kreditoren</span><span class="sxs-lookup"><span data-stu-id="7d32b-117">How to: Suggest Vendor Payments</span></span>](payables-how-suggest-vendor-payments.md) |
| <span data-ttu-id="7d32b-118">Stellen Sie Schecks für Zahlungen entweder als Ausdruck oder als Computer Schecks aus.</span><span class="sxs-lookup"><span data-stu-id="7d32b-118">Issue checks for payments, either as print-outs or as computer checks.</span></span> <span data-ttu-id="7d32b-119">Annullieren Sie Schecks vor oder nach dem Buchen.</span><span class="sxs-lookup"><span data-stu-id="7d32b-119">Void checks before or after posting.</span></span> |[<span data-ttu-id="7d32b-120">So gehts: Arbeiten mit Schecks</span><span class="sxs-lookup"><span data-stu-id="7d32b-120">How to: Work with Checks</span></span>](payables-how-work-checks.md) |
| <span data-ttu-id="7d32b-121">Um sicherzustellen, dass Ihre Bank nur Schecks und Beträge freigibt, können Sie ihr eine Datei senden, die die Daten für Kreditoren, Schecks und Zahlungsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="7d32b-121">Make sure that your bank only clears validated checks and amounts by sending them a file that contains vendor, check, and payment information.</span></span> |[<span data-ttu-id="7d32b-122">Erneuter Positive Pay-Export in Datei</span><span class="sxs-lookup"><span data-stu-id="7d32b-122">How to: Export a Positive Pay file</span></span>](finance-how-positive-pay.md) |
|<span data-ttu-id="7d32b-123">Exportzahlungen aus dem **Zahlungsausgangs Buch.-Blatt** in eine Bank archivieren, das Sie für Ihre Bank für das Verarbeiten hochladen, einschließlich EFT (elektronischer Geldtransfer) in Nordamerika.</span><span class="sxs-lookup"><span data-stu-id="7d32b-123">Export payments from the **Payment Journal** window to a bank file that you upload to your bank for processing, including EFT (electronic funds transfer) in North America.</span></span> |[<span data-ttu-id="7d32b-124">Vorgehensweise: Zahlungen in eine Bankdatei exportieren</span><span class="sxs-lookup"><span data-stu-id="7d32b-124">How to: Export Payments to a Bank File</span></span>](payables-how-export-payments-bank-file.md)|  

## <a name="see-also"></a><span data-ttu-id="7d32b-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d32b-125">See Also</span></span>
[<span data-ttu-id="7d32b-126">Verwalten von Verbindlichkeiten|</span><span class="sxs-lookup"><span data-stu-id="7d32b-126">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="7d32b-127">Einkauf</span><span class="sxs-lookup"><span data-stu-id="7d32b-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="7d32b-128">Verwalten von Forderungen</span><span class="sxs-lookup"><span data-stu-id="7d32b-128">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="7d32b-129">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7d32b-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

