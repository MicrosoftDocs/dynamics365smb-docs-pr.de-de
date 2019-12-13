---
title: So sperren Sie Artikelverkäufe an den Debitoren vom Verkauf oder Einkauf
description: In Business Central kann ein Artikel für den Verkauf, den Einkauf oder alle Zwecke gesperrt werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: c1b055e5101b99f0b0e1b69169d5c9f2f7e21d09
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2882994"
---
# <a name="block-customers"></a><span data-ttu-id="0fb7e-103">Debitoren sperren</span><span class="sxs-lookup"><span data-stu-id="0fb7e-103">Block Customers</span></span>
<span data-ttu-id="0fb7e-104">Sie können Debitoren, zum Beispiel aufgrund von Zahlungsunfähigkeit sperren, so dass der Debitor nicht zu Verkaufsbelegen hinzugefügt werden kann, oder dass keine Transaktionen für den Debitor gebucht werden können.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-104">You can block a customer, for example because of insolvency, so that the customer cannot be added to sales documents or so that no transactions can be posted for the customer.</span></span>

<span data-ttu-id="0fb7e-105">Zusätzlich zum Blockieren eines Debitors können Sie ausstehende Transaktionen festlegen, damit der Debitor in Verbindung mit Mahnungen ist.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-105">In addition to blocking a customer, you can set receivable transactions for the customer to be on hold in connection with reminders.</span></span> <span data-ttu-id="0fb7e-106">Weitere Informationen finden Sie unter [Offene Salden eintreiben](receivables-collect-outstanding-balances.md)</span><span class="sxs-lookup"><span data-stu-id="0fb7e-106">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>   

<span data-ttu-id="0fb7e-107">Die drei Optionen werden in den folgenden Sperroptionen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-107">The following table describes the different blocking options.</span></span>  

|<span data-ttu-id="0fb7e-108">Option</span><span class="sxs-lookup"><span data-stu-id="0fb7e-108">Option</span></span>|<span data-ttu-id="0fb7e-109">Description</span><span class="sxs-lookup"><span data-stu-id="0fb7e-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="0fb7e-110">**"Leer"**</span><span class="sxs-lookup"><span data-stu-id="0fb7e-110">**Blank**</span></span>|<span data-ttu-id="0fb7e-111">Transaktionen sind für diesen Debitor zulässig.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-111">Transactions are allowed for this customer.</span></span>|
|<span data-ttu-id="0fb7e-112">**Liefern**</span><span class="sxs-lookup"><span data-stu-id="0fb7e-112">**Ship**</span></span>|<span data-ttu-id="0fb7e-113">Für diesen Debitor können keine neuen Aufträge und Lieferungen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-113">New orders and new shipments cannot be created for this customer.</span></span> <span data-ttu-id="0fb7e-114">Vorhandene Lieferungen, die noch nicht fakturiert wurden, können fakturiert werden.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-114">Existing shipments not yet invoiced can be invoiced.</span></span>|  
|<span data-ttu-id="0fb7e-115">**Fakturieren**</span><span class="sxs-lookup"><span data-stu-id="0fb7e-115">**Invoice**</span></span>|<span data-ttu-id="0fb7e-116">Für diesen Debitor können keine neuen Aufträge, Lieferungen und Rechnungen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-116">New orders, new shipments, and new invoices cannot be created for this customer.</span></span> <span data-ttu-id="0fb7e-117">Vorhandene Lieferungen, die noch nicht fakturiert wurden, können nicht fakturiert werden.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-117">Existing shipments not yet invoiced cannot be invoiced.</span></span>|  
|<span data-ttu-id="0fb7e-118">**Alle**</span><span class="sxs-lookup"><span data-stu-id="0fb7e-118">**All**</span></span>|<span data-ttu-id="0fb7e-119">Für diesen Debitor ist keine Transaktion zulässig, wozu auch Zahlungen gehören.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-119">No transaction is allowed for this customer, including payments.</span></span>|  

## <a name="to-block-a-customer"></a><span data-ttu-id="0fb7e-120">Einen Debitor sperren</span><span class="sxs-lookup"><span data-stu-id="0fb7e-120">To block a customer</span></span>  
1. <span data-ttu-id="0fb7e-121">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="0fb7e-122">Wählen Sie einen Debitoren und wählen Sie dann die Aktion **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-122">Select a customer, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="0fb7e-123">Füllen Sie das Feld **Blockiert** mit einer der Optionen aus, wie sie oben beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-123">Fill in the **Blocked** field with one of the options described above.</span></span>

## <a name="see-also"></a><span data-ttu-id="0fb7e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fb7e-124">See Also</span></span>  
[<span data-ttu-id="0fb7e-125">Registriert einen neuen Debitor.</span><span class="sxs-lookup"><span data-stu-id="0fb7e-125">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="0fb7e-126">Einziehen von Restbeträgen</span><span class="sxs-lookup"><span data-stu-id="0fb7e-126">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="0fb7e-127">Verwalten von Forderungen</span><span class="sxs-lookup"><span data-stu-id="0fb7e-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
