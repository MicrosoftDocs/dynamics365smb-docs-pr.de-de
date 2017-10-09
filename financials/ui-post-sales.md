---
title: Verstehen, wie Verkaufsbelege gebucht werden | Microsoft Docs
description: Mehr zu den unterschiedlichen Buchungsfunktionen erfahren, um Verkaufsbelege zu buchen.
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/02/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 106102d07761673461bc28bbf6452ed05f926112
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="posting-sales"></a><span data-ttu-id="968f5-103">Verkäufe buchen</span><span class="sxs-lookup"><span data-stu-id="968f5-103">Posting Sales</span></span>
<span data-ttu-id="968f5-104">Wenn Sie die Schaltfläche **Gruppe Buchen** in einem Verkaufsbeleg auswählen, können Sie zwischen den folgenden Buchungsfunktionen auswählen:</span><span class="sxs-lookup"><span data-stu-id="968f5-104">In the **Posting group** on a sales document, you can choose between the following posting functions:</span></span>

* <span data-ttu-id="968f5-105">**Veröffentlichen**</span><span class="sxs-lookup"><span data-stu-id="968f5-105">**Post**</span></span>
* <span data-ttu-id="968f5-106">**Testbericht**</span><span class="sxs-lookup"><span data-stu-id="968f5-106">**Test Report**</span></span>
* <span data-ttu-id="968f5-107">**Buchen und senden**</span><span class="sxs-lookup"><span data-stu-id="968f5-107">**Post and Send**</span></span>
* <span data-ttu-id="968f5-108">**Buchen und Drucken**</span><span class="sxs-lookup"><span data-stu-id="968f5-108">**Post and Print**</span></span>
* <span data-ttu-id="968f5-109">**Buchen und per E-Mail senden**</span><span class="sxs-lookup"><span data-stu-id="968f5-109">**Post and Email**</span></span>
* <span data-ttu-id="968f5-110">**Stapelbuchung**</span><span class="sxs-lookup"><span data-stu-id="968f5-110">**Post Batch**</span></span>
* <span data-ttu-id="968f5-111">**Buchungsvorschau**</span><span class="sxs-lookup"><span data-stu-id="968f5-111">**Preview Posting**</span></span>

<span data-ttu-id="968f5-112">Wenn Sie alle Zeilen ausgefüllt und alle Daten des Verkaufsauftrags eingegeben haben, können Sie ihn buchen.</span><span class="sxs-lookup"><span data-stu-id="968f5-112">When you have completed all the lines and entered all the information on the sales order, you can post it.</span></span> <span data-ttu-id="968f5-113">Dies erstellt eine Lieferung und eine Rechnung.</span><span class="sxs-lookup"><span data-stu-id="968f5-113">This creates a shipment and an invoice.</span></span>

<span data-ttu-id="968f5-114">Wenn eine Verkaufsbestellung gebucht wird, wird das Debitorenkonto, die Finanzbuchhaltung und die Artikelposten aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="968f5-114">When a sales order is posted, the customer's account, the general ledger, and the item ledger entries are updated.</span></span>

<span data-ttu-id="968f5-115">Für jeden Verkaufsauftrag wird ein Verkaufsposten in der Tabelle **Sachposten** erstellt.</span><span class="sxs-lookup"><span data-stu-id="968f5-115">For each sales order, a sales entry is created in the **G/L Entry** table.</span></span> <span data-ttu-id="968f5-116">Darüber hinaus wird ein Posten in der Tabelle **Kreditorenposten** erzeugt und ein Sachposten im entsprechenden Einkaufskonto.</span><span class="sxs-lookup"><span data-stu-id="968f5-116">An entry is also created in the customer's account in the **Cust. Ledger Entry** table and a general ledger entry is created in the relevant receivables account.</span></span> <span data-ttu-id="968f5-117">Zusätzlich kann das Buchen in einem MwSt.-Posten und einem Sachposten für den Rabattbetrag resultieren.</span><span class="sxs-lookup"><span data-stu-id="968f5-117">In addition, posting the order may result in a VAT entry and a general ledger entry for the discount amount.</span></span> <span data-ttu-id="968f5-118">Ob ein Posten für Rabatt gebucht wird, hängt von den Einstellungen im Feld **Rabattbuchung** im Fenster **Debitoren & Verkauf Einr.** ab.</span><span class="sxs-lookup"><span data-stu-id="968f5-118">Whether an entry for the discount is posted depends on the contents of the **Discount Posting** field in the **Sales & Receivables Setup** window.</span></span>

<span data-ttu-id="968f5-119">Für jede Zeile des Verkaufsauftrags wird ein Artikelposten in der Tabelle **Artikelposten** erzeugt (wenn die Verkaufszeilen Artikelnummern enthalten) oder es wird ein Sachposten in der Tabelle **Sachposten** erzeugt (wenn die Verkaufszeilen Sachkonten enthalten).</span><span class="sxs-lookup"><span data-stu-id="968f5-119">For each sales order line, an item ledger entry will be created in the **Item Ledger Entry** table (if the sales lines contain item numbers) or a general ledger entry will be created in the **G/L Entry** table (if the sales lines contain a general ledger account).</span></span> <span data-ttu-id="968f5-120">Zusätzlich dazu werden Verkaufsaufträge immer in den Tabellen **Verkaufslieferkopf** und **Verkaufsrechnungskopf** gespeichert.</span><span class="sxs-lookup"><span data-stu-id="968f5-120">In addition to this, sales orders are always recorded in the **Sales Shipment Header** and **Sales Invoice Header** tables.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="968f5-121">Wenn Sie einen Auftrag buchen, können Sie sowohl einen Lieferschein als auch eine Rechnung erzeugen.</span><span class="sxs-lookup"><span data-stu-id="968f5-121">When you post an order, you can create both a shipment and an invoice.</span></span> <span data-ttu-id="968f5-122">Dies kann gleichzeitig oder unabhängig voneinander getan werden.</span><span class="sxs-lookup"><span data-stu-id="968f5-122">These can be done at the same time or independently.</span></span> <span data-ttu-id="968f5-123">Sie können auch eine Teillieferung und eine Teilrechnung erzeugen, indem Sie die Felder **Menge zu liefern** und/oder **Menge zu fakturieren** in den jeweiligen Zeilen des Verkaufsauftrags ausfüllen, bevor Sie buchen.</span><span class="sxs-lookup"><span data-stu-id="968f5-123">You can also create a partial shipment and a partial invoice by completing the **Qty. to Ship** and **Qty. to Invoice** fields on the individual sales order lines before you post.</span></span> <span data-ttu-id="968f5-124">Beachten Sie, dass Sie keine Rechnung ausstellen können, solange die entsprechende Lieferung nicht erfolgt ist.</span><span class="sxs-lookup"><span data-stu-id="968f5-124">Note that you cannot create an invoice for something that is not shipped.</span></span> <span data-ttu-id="968f5-125">Bevor Sie also die Fakturierung durchführen können, müssen Sie einen Lieferschein erstellt oder die Funktion zur gleichzeitigen Lieferung und Fakturierung gewählt haben.</span><span class="sxs-lookup"><span data-stu-id="968f5-125">That is, before you can invoice, you must have recorded a shipment, or you must choose to ship and invoice at the same time.</span></span>

<span data-ttu-id="968f5-126">Wenn die Buchung vollständig ist, werden die gebuchten Verkaufszeilen aus der Bestellung entfernt.</span><span class="sxs-lookup"><span data-stu-id="968f5-126">When the posting is completed, the posted sales lines are removed from the order.</span></span> <span data-ttu-id="968f5-127">Eine Meldung erscheint, die Ihnen mitteilt, dass die Buchung vollständig ist.</span><span class="sxs-lookup"><span data-stu-id="968f5-127">A message tells you when the posting is completed.</span></span> <span data-ttu-id="968f5-128">Im Anschluss können Sie die gebuchten Posten in den verschiedenen Fenstern einsehen, die gebuchte Posten enthalten, einschließlich **Debitorenposten**, **Sachposten**, **Artikelposten**, **Lagerplatzposten**, **Geb. Verkaufsrechnung**.</span><span class="sxs-lookup"><span data-stu-id="968f5-128">After this, you will be able to see the posted entries in the various windows that contain posted entries, such as the **Cust. Ledger Entries**, **G/L Entries**, **Item Ledger Entries**, **Posted Sales Shipments**, and **Posted Sales Invoices** windows.</span></span>

## <a name="see-also"></a><span data-ttu-id="968f5-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="968f5-129">See Also</span></span>
[<span data-ttu-id="968f5-130">Verkauf</span><span class="sxs-lookup"><span data-stu-id="968f5-130">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="968f5-131">Gewusst wie: Senden von Belegen über E-Mail</span><span class="sxs-lookup"><span data-stu-id="968f5-131">How to: Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="968f5-132">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="968f5-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


