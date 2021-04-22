---
title: Verwalten von Bankkonten| Microsoft Docs
description: Sie müssen regelmäßig Bankposten mit den zugehörigen Banktransaktionen in Ihren Bankkonten abstimmen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: db4afccdd67e400f2effd34b2db3c449db10432a
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779707"
---
# <a name="reconciling-bank-accounts"></a><span data-ttu-id="48874-103">Abstimmen von Bankkonten</span><span class="sxs-lookup"><span data-stu-id="48874-103">Reconciling Bank Accounts</span></span>

<span data-ttu-id="48874-104">Eine Bankabstimmung sollte in regelmäßigen Abständen für alle Ihre Bankkonten durchgeführt werden, um sicherzustellen, dass die Kassenunterlagen des Unternehmens korrekt sind.</span><span class="sxs-lookup"><span data-stu-id="48874-104">A bank reconciliation should be completed at regular intervals for all your bank accounts to ensure that the company's cash records are correct.</span></span> <span data-ttu-id="48874-105">Sie tun dies, indem Sie die Einträge in Ihren internen Bankkonten mit den Banktransaktionen in Ihrer Bank vergleichen und abgleichen und dann die Salden auf Ihre internen Bankkonten buchen, um den Finanzmanagern Gesamtsummen zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="48874-105">You do this by comparing and matching entries in your internal bank accounts with bank transactions at your bank, and then posting the balances to your internal bank accounts to make totals available to finance managers.</span></span> <span data-ttu-id="48874-106">Der Bankabgleich ist auch eine praktische Methode, um fehlende Zahlungen und Buchhaltungsfehler zu ermitteln und zu beheben.</span><span class="sxs-lookup"><span data-stu-id="48874-106">Bank reconciliation is also a practical way to discover and resolve missing payments and bookkeeping errors.</span></span>

<span data-ttu-id="48874-107">Sie können die Aufgabe auf der Seite **Bankkonto Abstimmen** ausführen, auf der Sie die Bankkontoauszugszeilen auf der linken Bereichsseite mit Ihrem internen Bankposten im rechten Fensterbereich abstimmen (abgleichen).</span><span class="sxs-lookup"><span data-stu-id="48874-107">You can perform the task on the **Bank Acc. Reconciliation** page where you match (reconcile) bank statement lines in the left-hand pane with your internal bank account ledger entries in the right-hand pane.</span></span> <span data-ttu-id="48874-108">Alternativ können Sie diese Aufgabe auf der Seite **Zahlungsabstimmungsbuch.-Blatt** als Teil der Verarbeitung der Zahlungen durchgeführt werden, die auf einem Bankauszug dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="48874-108">Alternatively, you can perform this task on the **Payment Reconciliation Journal** page as part of processing the payments that are represented on a bank statement.</span></span> <span data-ttu-id="48874-109">Auf beiden Seiten können Sie die Bankkontoauszugsinformationen ausfüllen, indem Sie eine Datei oder einen Feed importieren oder automatische entsprechende Vorschläge verwenden.</span><span class="sxs-lookup"><span data-stu-id="48874-109">On both pages, you can fill in the bank statement information by importing a file or feed and you can use automatic matching suggestions.</span></span>

> [!NOTE]  
> <span data-ttu-id="48874-110">In den nordamerikanischen Versionen können Sie auf der Seite **Bank Rec. Arbeitsblatt** durchführen, das besser für Schecks und Einzahlungen-Vorgänge geeignet ist, jedoch keine Bankkontoauszugsdateien bietet.</span><span class="sxs-lookup"><span data-stu-id="48874-110">In the North American versions, you can also perform bank reconciliation on the **Bank Rec. Worksheet** page, which is better suited for checks and deposits but does not offer import of bank statement files.</span></span> <span data-ttu-id="48874-111">Um diese Seite **Bankkonto Abstimmen** anstelle des Fensters zu verwenden, wählen Sie das Feld **Bank Recon. mit Auto. Entsprechung** auf der Seite **Finanzbuchhaltung Einrichtung**.</span><span class="sxs-lookup"><span data-stu-id="48874-111">To use this page instead of the **Bank Acc. Reconciliation** page, deselect the **Bank Recon. with Auto. Match** field on the **General Ledger Setup** page.</span></span> <span data-ttu-id="48874-112">Weitere Informationen finden Sie im Abschnitt [Bankkonten abstimmen](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) unter der lokalen USA-Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="48874-112">For more information, see [Reconcile Bank Accounts](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) under United States Local Functionality.</span></span>

<span data-ttu-id="48874-113">Bevor Sie Ihre Bankkonten in [!INCLUDE[prod_short](includes/prod_short.md)] verwalten können, müssen Sie jedes Bankkonto als Bankkontokarte einrichten.</span><span class="sxs-lookup"><span data-stu-id="48874-113">Before you can manage your bank accounts within [!INCLUDE[prod_short](includes/prod_short.md)], you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="48874-114">Darüber hinaus müssen Sie elektronische Dienste einrichten, die Sie ggf. für den Bankauszugsimport und Zahlungsdateiexport verwenden.</span><span class="sxs-lookup"><span data-stu-id="48874-114">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="48874-115">Weitere Informationen finden Sie unter [Einrichten von Banken](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="48874-115">For more information, see [Setting Up Banking](bank-setup-banking.md).</span></span>

<span data-ttu-id="48874-116">Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Themen, die sie beschreiben.</span><span class="sxs-lookup"><span data-stu-id="48874-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="48874-117">Aktion</span><span class="sxs-lookup"><span data-stu-id="48874-117">To</span></span> | <span data-ttu-id="48874-118">Siehe</span><span class="sxs-lookup"><span data-stu-id="48874-118">See</span></span> |
| --- | --- |
| <span data-ttu-id="48874-119">Stimmen Sie Bankkonten als separate Aufgabe auf der Seite **Bankkontoabstimmung** ab.</span><span class="sxs-lookup"><span data-stu-id="48874-119">Reconcile bank accounts as a separate task on the **Bank Acc. Reconciliation** page.</span></span> |[<span data-ttu-id="48874-120">Bankkonten abstimmen</span><span class="sxs-lookup"><span data-stu-id="48874-120">Reconcile Bank Accounts</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="48874-121">Abstimmen von Bankkonten in Verbindung mit der Zahlungsverarbeitung auf der Seite **Zahlungsabstimmungsbuch.-Blatt**.</span><span class="sxs-lookup"><span data-stu-id="48874-121">Reconcile bank accounts in connection with payment processing on the **Payment Reconciliation Journal** page.</span></span> |[<span data-ttu-id="48874-122">Zahlungen automatisch vornehmen und Bankkonten abstimmen</span><span class="sxs-lookup"><span data-stu-id="48874-122">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |

> [!TIP]
> <span data-ttu-id="48874-123">Verwenden Sie die Bankabstimmung, um zu überprüfen, ob Ihre Bücher auf dem neuesten Stand sind, und veröffentlichen Sie die Abstimmung erst, wenn Sie mit der Abstimmung zufrieden sind.</span><span class="sxs-lookup"><span data-stu-id="48874-123">Use bank reconciliation to help verify that your books are up-to-date, and do not post the reconciliation until you are satisfied with the reconciliation.</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="48874-124">Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="48874-124">See Related Training at [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="48874-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48874-125">See Also</span></span>

[<span data-ttu-id="48874-126">Einrichten von Banken</span><span class="sxs-lookup"><span data-stu-id="48874-126">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="48874-127">Bankkonten abstimmen</span><span class="sxs-lookup"><span data-stu-id="48874-127">Reconcile Bank Accounts</span></span>](bank-how-reconcile-bank-accounts-separately.md)  
[<span data-ttu-id="48874-128">Zahlungen automatisch vornehmen und Bankkonten abstimmen</span><span class="sxs-lookup"><span data-stu-id="48874-128">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[<span data-ttu-id="48874-129">Bank-Geldmittel überweisen</span><span class="sxs-lookup"><span data-stu-id="48874-129">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md)  
[<span data-ttu-id="48874-130">Verwalten von Forderungen</span><span class="sxs-lookup"><span data-stu-id="48874-130">Managing Receivables</span></span>](receivables-manage-receivables.md)  
[<span data-ttu-id="48874-131">Verwalten von Verbindlichkeiten</span><span class="sxs-lookup"><span data-stu-id="48874-131">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="48874-132">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="48874-132">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="48874-133">Allgemeine Geschäftsfunktionen</span><span class="sxs-lookup"><span data-stu-id="48874-133">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]