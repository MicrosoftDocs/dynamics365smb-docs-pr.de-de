---
title: "Ausgleichen von Posten in unterschiedlichen Währungen| Microsoft Docs"
description: "Wenn Sie an einen Debitor in einer Währung verkaufen, die Zahlung jedoch in einer anderen Währung erfolgt, kann die Rechnung mit der Zahlung ausgeglichen werden."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 035f4c0e98e3b7ba308319c2017568de832e26c5
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-enable-application-of-ledger-entries-in-different-currencies"></a><span data-ttu-id="8f7bc-103">So gehts: Anwendung von Kreditorenposten in unterschiedlichen Währungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="8f7bc-103">How to: Enable Application of Ledger Entries in Different Currencies</span></span>
<span data-ttu-id="8f7bc-104">Falls Sie Einkäufe von einem Kreditor in einer Währung tätigen und die Zahlung in einer anderen Währung leisten, können Sie die Zahlung mit dem Einkauf ausgleichen.</span><span class="sxs-lookup"><span data-stu-id="8f7bc-104">If you purchase from a vendor in one currency and submit payment in another currency, you can apply the payment to the purchase.</span></span>

<span data-ttu-id="8f7bc-105">Wenn Sie entsprechend an einen Debitor in einer Währung verkaufen und die Zahlung in einer anderen Währung erhalten, können Sie die Zahlung mit der Verkaufsrechnung ausgleichen.</span><span class="sxs-lookup"><span data-stu-id="8f7bc-105">Likewise, if you sell to a customer in one currency and receive payment in another currency, you can apply the payment to the sales invoice.</span></span>

<span data-ttu-id="8f7bc-106">Im Folgenden wird beschrieben, wie dies für Kreditorenposten im Fenster **Kreditoren & Einkauf Einrichtung** eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="8f7bc-106">The following procedure describes how to set this up for vendor ledger entries in the **Purchases & Payables Setup** window.</span></span> <span data-ttu-id="8f7bc-107">Die Einrichtung für Debitorenposten im Fenster **Debitoren & Verkauf Einrichtung** ist ähnlich.</span><span class="sxs-lookup"><span data-stu-id="8f7bc-107">The setup is similar for customer ledger entries in the **Sales & Receivables Setup** window.</span></span>

> [!NOTE]  
>   <span data-ttu-id="8f7bc-108">Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8f7bc-108">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="8f7bc-109">Weitere Informationen finden Sie unter [Anpassen Ihrer [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)Experience.</span><span class="sxs-lookup"><span data-stu-id="8f7bc-109">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a><span data-ttu-id="8f7bc-110">So aktivieren Sie den Ausgleich von Kreditorenposten in unterschiedlichen Währungen</span><span class="sxs-lookup"><span data-stu-id="8f7bc-110">To enable application of vendor ledger entries in different currencies</span></span>
1. <span data-ttu-id="8f7bc-111">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht  suchen")und geben **Kreditoren- und Debitoren-Einrichtung** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="8f7bc-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="8f7bc-112">Wählen Sie im Feld **Währungsausgleich** eine der folgenden Optionen.</span><span class="sxs-lookup"><span data-stu-id="8f7bc-112">In the **Appln. between Currencies** field, select one of the following options.</span></span>

| <span data-ttu-id="8f7bc-113">Option</span><span class="sxs-lookup"><span data-stu-id="8f7bc-113">Option</span></span> | <span data-ttu-id="8f7bc-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8f7bc-114">Description</span></span> |
| --- | --- |
| <span data-ttu-id="8f7bc-115">Keine</span><span class="sxs-lookup"><span data-stu-id="8f7bc-115">None</span></span> |<span data-ttu-id="8f7bc-116">Ausgleich zwischen Währungen ist nicht zugelassen.</span><span class="sxs-lookup"><span data-stu-id="8f7bc-116">Application between currencies is not allowed.</span></span> |
| <span data-ttu-id="8f7bc-117">EWU</span><span class="sxs-lookup"><span data-stu-id="8f7bc-117">EMU</span></span> |<span data-ttu-id="8f7bc-118">Ausgleich zwischen EWU-Währungen ist zugelassen.</span><span class="sxs-lookup"><span data-stu-id="8f7bc-118">Application between EMU currencies is allowed.</span></span> |
| <span data-ttu-id="8f7bc-119">Alle</span><span class="sxs-lookup"><span data-stu-id="8f7bc-119">All</span></span> |<span data-ttu-id="8f7bc-120">Ausgleich zwischen allen Währungen ist zugelassen.</span><span class="sxs-lookup"><span data-stu-id="8f7bc-120">Application between all currencies is allowed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="8f7bc-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f7bc-121">See Also</span></span>
[<span data-ttu-id="8f7bc-122">Verwalten von Verbindlichkeiten|</span><span class="sxs-lookup"><span data-stu-id="8f7bc-122">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="8f7bc-123">Verwalten von Forderungen</span><span class="sxs-lookup"><span data-stu-id="8f7bc-123">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="8f7bc-124">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8f7bc-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

