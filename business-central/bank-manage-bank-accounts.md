---
title: Verwalten von Bankkonten| Microsoft Docs
description: Sie müssen regelmäßig Bankposten mit den zugehörigen Banktransaktionen in Ihren Bankkonten abstimmen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 25e1242541e98cc47e2fcc4f016a860ad08c635d
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2019
ms.locfileid: "939129"
---
# <a name="managing-bank-accounts"></a><span data-ttu-id="8c9a5-103">Verwalten von Bankkonten</span><span class="sxs-lookup"><span data-stu-id="8c9a5-103">Managing Bank Accounts</span></span>
<span data-ttu-id="8c9a5-104">In regelmäßigen Abständen müssen Sie Ihre Bankposten in [!INCLUDE[d365fin](includes/d365fin_md.md)] mit den entsprechenden Banktransaktionen auf den Konten bei Ihrer Bank abstimmen, und dann den Saldo auf Ihrem Bankkonto buchen.</span><span class="sxs-lookup"><span data-stu-id="8c9a5-104">At regular intervals, you must reconcile your bank ledger entries in [!INCLUDE[d365fin](includes/d365fin_md.md)] with the related bank transactions in bank accounts at your bank, and then post the balance to your bank account.</span></span> <span data-ttu-id="8c9a5-105">Diese Aufgabe kann als Teil der Zahlungsverarbeitung auf einem Bankauszug im **Zahlungsabstimmungsbuch.-Blatt** dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8c9a5-105">You can perform this task either as part of processing the payments represented on a bank statement in the **Payment Reconciliation Journal**.</span></span> <span data-ttu-id="8c9a5-106">Alternativ können Sie die Aufgabe separat ausführen vom Zahlungsprozess, indem die Seite **Bankkonto Abstimmen**, in dem Sie die Bnkkontoauszugszeilen abstimmen (abgleichen) auf der linken Bereichsseite mit Ihrem internen Bankposten im rechten Fensterbereich.</span><span class="sxs-lookup"><span data-stu-id="8c9a5-106">Alternatively, you can perform the task separately from payment processing, on the **Bank Acc. Reconciliation** page where you match (reconcile) bank statement lines in the left-hand pane with your internal bank account ledger entries in the right-hand pane.</span></span> <span data-ttu-id="8c9a5-107">In beiden Seiten können Sie die Bankkontoauszugsinformationen ausfüllen, indem Sie eine Datei oder einen Feed importieren oder automatische entsprechende Vorschläge verwenden.</span><span class="sxs-lookup"><span data-stu-id="8c9a5-107">In both pages, you can fill in the bank statement information by importing a file or feed and you can use automatic matching suggestions.</span></span>

> [!NOTE]  
> <span data-ttu-id="8c9a5-108">In den nordamerikanischen Versionen können Sie auf der Seite **Bank Rec. Vorschlag** durchführen, das besser für Schecks und Einzahlungen-Vorgänge geeignet ist, jedoch keine Bankkontoauszugsdateien bietet.</span><span class="sxs-lookup"><span data-stu-id="8c9a5-108">In North American versions, you can also perform bank reconciliation on the **Bank Rec. Worksheet** page, which is better suited for checks and deposits but does not offer import of bank statement files.</span></span> <span data-ttu-id="8c9a5-109">Um diese Seite **Bankkonto Abstimmen** anstelle des Fensters zu verwenden, wählen Sie das Feld **Bank Recon. mit Auto. Entsprechung** auf der Seite **Finanzbuchhaltung Einrichtung**.</span><span class="sxs-lookup"><span data-stu-id="8c9a5-109">To use this page instead of the **Bank Acc. Reconciliation** page, deselect the **Bank Recon. with Auto. Match** field on the **General Ledger Setup** page.</span></span> <span data-ttu-id="8c9a5-110">Weitere Informationen finden Sie im Abschnitt "Bankkonten abstimmen" unter der der lokalen USA-Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="8c9a5-110">For more information, see the "Reconcile Bank Accounts" section under United States Local Functionality.</span></span>

<span data-ttu-id="8c9a5-111">Manchmal müssen Sie Beträge zwischen Bankkonten im [!INCLUDE[d365fin](includes/d365fin_md.md)] transferieren, um Überweisungen bei Ihrer Bank widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="8c9a5-111">Sometimes, you need to transfer amounts between bank account in [!INCLUDE[d365fin](includes/d365fin_md.md)] to reflect transfers at your bank.</span></span> <span data-ttu-id="8c9a5-112">Diese Aufgabe wird auf der Seite **Fibu Buch.-Blatt** auf unterschiedliche Arten, abhängig von der Währung der Geldmittel ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8c9a5-112">You perform this task on the **General Journal** page, in different ways depending on the currency of the funds.</span></span>

<span data-ttu-id="8c9a5-113">Bevor Sie Bankkonten verwalten können, müssen Sie jedes Bankkonto als Bankkontokarte einrichten.</span><span class="sxs-lookup"><span data-stu-id="8c9a5-113">Before you can manage bank accounts, you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="8c9a5-114">Darüber hinaus müssen Sie elektronische Dienste einrichten, die Sie ggf. für den Bankauszugsimport und Zahlungsdateiexport verwenden.</span><span class="sxs-lookup"><span data-stu-id="8c9a5-114">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="8c9a5-115">Weitere Informationen finden Sie unter [So gehts: Einrichten von Bankkonten](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="8c9a5-115">For more information, see [Set Up Bank Accounts](bank-setup-banking.md).</span></span>

<span data-ttu-id="8c9a5-116">In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.</span><span class="sxs-lookup"><span data-stu-id="8c9a5-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="8c9a5-117">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="8c9a5-117">To</span></span> | <span data-ttu-id="8c9a5-118">Siehe</span><span class="sxs-lookup"><span data-stu-id="8c9a5-118">See</span></span> |
| --- | --- |
| <span data-ttu-id="8c9a5-119">Abstimmen von Bankkonten in Verbindung mit der Zahlungsverarbeitung auf der Seite **Zahlungsabstimmungsbuch.-Blatt**.</span><span class="sxs-lookup"><span data-stu-id="8c9a5-119">Reconcile bank accounts in connection with payment processing on the **Payment Reconciliation Journal** page.</span></span> |[<span data-ttu-id="8c9a5-120">Zahlungen automatisch vornehmen und Bankkonten abstimmen</span><span class="sxs-lookup"><span data-stu-id="8c9a5-120">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="8c9a5-121">Abstimmen von Bankkonten, inklusive Scheckposten, als separate Aufgabe auf der Seite **Bankkontoabstimmung**.</span><span class="sxs-lookup"><span data-stu-id="8c9a5-121">Reconcile bank accounts, including check ledger entries, as a separate task on the **Bank Acc. Reconciliation** page.</span></span> |[<span data-ttu-id="8c9a5-122">Bankkonten separat abstimmen</span><span class="sxs-lookup"><span data-stu-id="8c9a5-122">Reconcile Bank Accounts Separately</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="8c9a5-123">Buchen von Überweisungen zwischen Bankkonten in der gleichen oder in unterschiedlichen Währungen.</span><span class="sxs-lookup"><span data-stu-id="8c9a5-123">Post transfers between bank accounts in the same currency or in different currencies.</span></span> |[<span data-ttu-id="8c9a5-124">Bank-Geldmittel überweisen</span><span class="sxs-lookup"><span data-stu-id="8c9a5-124">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a><span data-ttu-id="8c9a5-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c9a5-125">See Also</span></span>
[<span data-ttu-id="8c9a5-126">Einrichten von Banken</span><span class="sxs-lookup"><span data-stu-id="8c9a5-126">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="8c9a5-127">Verwalten von Forderungen</span><span class="sxs-lookup"><span data-stu-id="8c9a5-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="8c9a5-128">[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="8c9a5-128">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="8c9a5-129">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8c9a5-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="8c9a5-130">Allgemeine Geschäftsfunktionen</span><span class="sxs-lookup"><span data-stu-id="8c9a5-130">General Business Functionality</span></span>](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 
