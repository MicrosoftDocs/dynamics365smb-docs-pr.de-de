---
title: Ausgleichen von Posten in unterschiedlichen Währungen| Microsoft Docs
description: Wenn Sie an einen Debitor in einer Währung verkaufen, die Zahlung jedoch in einer anderen Währung erfolgt, kann die Rechnung mit der Zahlung ausgeglichen werden.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 83b054b09f1015b988aed55acf9e75d93ab99f4e
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386474"
---
# <a name="enable-application-of-ledger-entries-in-different-currencies"></a><span data-ttu-id="717a7-103">Anwendung von Kreditorenposten in unterschiedlichen Währungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="717a7-103">Enable Application of Ledger Entries in Different Currencies</span></span>
<span data-ttu-id="717a7-104">Falls Sie Einkäufe von einem Kreditor in einer Währung tätigen und die Zahlung in einer anderen Währung leisten, können Sie die Zahlung mit dem Einkauf ausgleichen.</span><span class="sxs-lookup"><span data-stu-id="717a7-104">If you purchase from a vendor in one currency and submit payment in another currency, you can apply the payment to the purchase.</span></span>

<span data-ttu-id="717a7-105">Wenn Sie entsprechend an einen Debitor in einer Währung verkaufen und die Zahlung in einer anderen Währung erhalten, können Sie die Zahlung mit der Verkaufsrechnung ausgleichen.</span><span class="sxs-lookup"><span data-stu-id="717a7-105">Likewise, if you sell to a customer in one currency and receive payment in another currency, you can apply the payment to the sales invoice.</span></span>

<span data-ttu-id="717a7-106">Im Folgenden wird beschrieben, wie dies für Kreditorenposten auf der Seite **Kreditoren & Einkauf Einrichtung** eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="717a7-106">The following procedure describes how to set this up for vendor ledger entries on the **Purchases & Payables Setup** page.</span></span> <span data-ttu-id="717a7-107">Die Einrichtung für Debitorenposten auf der Seite **Debitoren & Verkauf Einrichtung** ist ähnlich.</span><span class="sxs-lookup"><span data-stu-id="717a7-107">The setup is similar for customer ledger entries on the **Sales & Receivables Setup** page.</span></span>

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a><span data-ttu-id="717a7-108">So aktivieren Sie den Ausgleich von Kreditorenposten in unterschiedlichen Währungen</span><span class="sxs-lookup"><span data-stu-id="717a7-108">To enable application of vendor ledger entries in different currencies</span></span>
1. <span data-ttu-id="717a7-109">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Einrichten von Einkäufen und Verbindlichkeiten** ein, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="717a7-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="717a7-110">Wählen Sie im Feld **Währungsausgleich** eine der folgenden Optionen.</span><span class="sxs-lookup"><span data-stu-id="717a7-110">In the **Appln. between Currencies** field, select one of the following options.</span></span>

| <span data-ttu-id="717a7-111">Option</span><span class="sxs-lookup"><span data-stu-id="717a7-111">Option</span></span> | <span data-ttu-id="717a7-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="717a7-112">Description</span></span> |
| --- | --- |
| <span data-ttu-id="717a7-113">Keine</span><span class="sxs-lookup"><span data-stu-id="717a7-113">None</span></span> |<span data-ttu-id="717a7-114">Ausgleich zwischen Währungen ist nicht zugelassen.</span><span class="sxs-lookup"><span data-stu-id="717a7-114">Application between currencies is not allowed.</span></span> |
| <span data-ttu-id="717a7-115">EWU</span><span class="sxs-lookup"><span data-stu-id="717a7-115">EMU</span></span> |<span data-ttu-id="717a7-116">Ausgleich zwischen EWU-Währungen ist zugelassen.</span><span class="sxs-lookup"><span data-stu-id="717a7-116">Application between EMU currencies is allowed.</span></span> |
| <span data-ttu-id="717a7-117">Alle</span><span class="sxs-lookup"><span data-stu-id="717a7-117">All</span></span> |<span data-ttu-id="717a7-118">Ausgleich zwischen allen Währungen ist zugelassen.</span><span class="sxs-lookup"><span data-stu-id="717a7-118">Application between all currencies is allowed.</span></span> |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a><span data-ttu-id="717a7-119">So richten Sie Sachkonten für Rundungsdifferenzen beim Währungsausgleich ein</span><span class="sxs-lookup"><span data-stu-id="717a7-119">To set up G/L accounts for currency application rounding differences</span></span>  
<span data-ttu-id="717a7-120">Wenn Sie Posten in unterschiedlichen Währungen ausgleichen, müssen Sie die Sachkonten einrichten, auf die Sie die Rundungsdifferenzen buchen möchten.</span><span class="sxs-lookup"><span data-stu-id="717a7-120">If you apply entries in different currencies, you must set up the general ledger accounts to which you want to post rounding differences.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="717a7-121">Sie müssen die Sachkonten einrichten, bevor Sie die Aufgabe abschließen.</span><span class="sxs-lookup"><span data-stu-id="717a7-121">You must set up the general ledger accounts before you complete the task.</span></span> <span data-ttu-id="717a7-122">Weitere Informationen finden Sie unter [Die Finanzbuchhaltung und der Kontenplan verstehen](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="717a7-122">For more information, see [Understanding the General Ledger and the Chart of Accounts](finance-general-ledger.md).</span></span>

1. <span data-ttu-id="717a7-123">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") aus, geben Sie **Debitorenbuchungsgruppen** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="717a7-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customer Posting Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="717a7-124">Geben Sie in die Felder **Währungsausgl. Rund.-Sollkto.** und **Währungsausgl. Rund.-Habenkto.** die entsprechenden Sachkonten ein, um Rundungsdifferenzen zu buchen.</span><span class="sxs-lookup"><span data-stu-id="717a7-124">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  
3. <span data-ttu-id="717a7-125">Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Kreditorenbuchungsgruppen** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="717a7-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendor Posting Groups**, and then choose the related link.</span></span>  
4. <span data-ttu-id="717a7-126">Geben Sie in die Felder **Währungsausgl. Rund.-Sollkto.** und **Währungsausgl. Rund.-Habenkto.** die entsprechenden Sachkonten ein, um Rundungsdifferenzen zu buchen.</span><span class="sxs-lookup"><span data-stu-id="717a7-126">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  

## <a name="see-also"></a><span data-ttu-id="717a7-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="717a7-127">See Also</span></span>
[<span data-ttu-id="717a7-128">Verwalten von Verbindlichkeiten</span><span class="sxs-lookup"><span data-stu-id="717a7-128">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="717a7-129">Verwalten von Forderungen</span><span class="sxs-lookup"><span data-stu-id="717a7-129">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="717a7-130">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="717a7-130">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]