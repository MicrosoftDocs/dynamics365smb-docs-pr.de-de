---
title: So sperren Sie Verkäufe an Debitoren
description: Bei Bedarf können Sie verhindern, dass ein Debitor in Verkaufsbelege und andere Verkaufstransaktionen aufgenommen wird.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 720eb2d5899ba067dbcee8dc97492ebcd01b1abd
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3779172"
---
# <a name="block-customers"></a><span data-ttu-id="46799-103">Debitoren sperren</span><span class="sxs-lookup"><span data-stu-id="46799-103">Block Customers</span></span>
<span data-ttu-id="46799-104">Sie können Debitoren, zum Beispiel aufgrund von Zahlungsunfähigkeit sperren, so dass der Debitor nicht zu Verkaufsbelegen hinzugefügt werden kann, oder dass keine Transaktionen für den Debitor gebucht werden können.</span><span class="sxs-lookup"><span data-stu-id="46799-104">You can block a customer, for example because of insolvency, so that the customer cannot be added to sales documents or so that no transactions can be posted for the customer.</span></span>

<span data-ttu-id="46799-105">Zusätzlich zum Blockieren eines Debitors können Sie ausstehende Transaktionen festlegen, damit der Debitor in Verbindung mit Mahnungen ist.</span><span class="sxs-lookup"><span data-stu-id="46799-105">In addition to blocking a customer, you can set receivable transactions for the customer to be on hold in connection with reminders.</span></span> <span data-ttu-id="46799-106">Weitere Informationen finden Sie unter [Offene Salden eintreiben](receivables-collect-outstanding-balances.md)</span><span class="sxs-lookup"><span data-stu-id="46799-106">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>   

<span data-ttu-id="46799-107">Die drei Optionen zum Sperren von Debitoren werden in den folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="46799-107">The following table describes the options for blocking customers.</span></span>  

|<span data-ttu-id="46799-108">Option</span><span class="sxs-lookup"><span data-stu-id="46799-108">Option</span></span>|<span data-ttu-id="46799-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46799-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="46799-110">**"Leer"**</span><span class="sxs-lookup"><span data-stu-id="46799-110">**Blank**</span></span>|<span data-ttu-id="46799-111">Transaktionen sind für diesen Debitor zulässig.</span><span class="sxs-lookup"><span data-stu-id="46799-111">Transactions are allowed for this customer.</span></span>|
|<span data-ttu-id="46799-112">**Liefern**</span><span class="sxs-lookup"><span data-stu-id="46799-112">**Ship**</span></span>|<span data-ttu-id="46799-113">Für diesen Debitor können keine neuen Aufträge und Lieferungen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="46799-113">New orders and new shipments cannot be created for this customer.</span></span> <span data-ttu-id="46799-114">Vorhandene Lieferungen, die noch nicht fakturiert wurden, können fakturiert werden.</span><span class="sxs-lookup"><span data-stu-id="46799-114">Existing shipments not yet invoiced can be invoiced.</span></span>|  
|<span data-ttu-id="46799-115">**Fakturieren**</span><span class="sxs-lookup"><span data-stu-id="46799-115">**Invoice**</span></span>|<span data-ttu-id="46799-116">Für diesen Debitor können keine neuen Aufträge, Lieferungen und Rechnungen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="46799-116">New orders, new shipments, and new invoices cannot be created for this customer.</span></span> <span data-ttu-id="46799-117">Vorhandene Lieferungen, die noch nicht fakturiert wurden, können nicht fakturiert werden.</span><span class="sxs-lookup"><span data-stu-id="46799-117">Existing shipments not yet invoiced cannot be invoiced.</span></span> <span data-ttu-id="46799-118">Sie können dem Debitor weiterhin Erinnerungen und Zinsrechnungen senden.</span><span class="sxs-lookup"><span data-stu-id="46799-118">You can still send reminders and finance charge memos to the customer.</span></span>|  
|<span data-ttu-id="46799-119">**Alle**</span><span class="sxs-lookup"><span data-stu-id="46799-119">**All**</span></span>|<span data-ttu-id="46799-120">Für diesen Debitor ist keine Transaktion zulässig, wozu auch Zahlungen gehören.</span><span class="sxs-lookup"><span data-stu-id="46799-120">No transaction is allowed for this customer, including payments.</span></span>|  

## <a name="to-block-a-customer"></a><span data-ttu-id="46799-121">Einen Debitor sperren</span><span class="sxs-lookup"><span data-stu-id="46799-121">To block a customer</span></span>  
1. <span data-ttu-id="46799-122">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link.</span><span class="sxs-lookup"><span data-stu-id="46799-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="46799-123">Wählen Sie einen Debitoren und wählen Sie dann die Aktion **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="46799-123">Select a customer, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="46799-124">Wählen Sie im Feld **Gesperrt** aus, was gesperrt werden soll, wie in der obigen Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="46799-124">In the **Blocked** field, choose what to block, as described in the table above.</span></span>

## <a name="see-also"></a><span data-ttu-id="46799-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46799-125">See Also</span></span>  
[<span data-ttu-id="46799-126">Registriert einen neuen Debitor.</span><span class="sxs-lookup"><span data-stu-id="46799-126">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="46799-127">Einziehen von Restbeträgen</span><span class="sxs-lookup"><span data-stu-id="46799-127">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="46799-128">Verwalten von Forderungen</span><span class="sxs-lookup"><span data-stu-id="46799-128">Managing Receivables</span></span>](receivables-manage-receivables.md)  
