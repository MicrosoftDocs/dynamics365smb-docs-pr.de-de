---
title: Verstehen, wie Verkaufsbelege gebucht werden | Microsoft Docs
description: Mehr zu den unterschiedlichen Buchungsfunktionen erfahren, um Verkaufsbelege zu buchen.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: solsen
ms.openlocfilehash: 7ada688f7946d7f857dc6d4a6518b8bcb4e5c707
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "798525"
---
# <a name="posting-sales"></a><span data-ttu-id="b4084-103">Verkäufe buchen</span><span class="sxs-lookup"><span data-stu-id="b4084-103">Posting Sales</span></span>
<span data-ttu-id="b4084-104">Wenn Sie die Schaltfläche **Gruppe Buchen** in einem Verkaufsbeleg auswählen, können Sie zwischen den folgenden Buchungsfunktionen auswählen:</span><span class="sxs-lookup"><span data-stu-id="b4084-104">In the **Posting group** on a sales document, you can choose between the following posting functions:</span></span>

* <span data-ttu-id="b4084-105">**Veröffentlichen**</span><span class="sxs-lookup"><span data-stu-id="b4084-105">**Post**</span></span>
* <span data-ttu-id="b4084-106">**Testbericht**</span><span class="sxs-lookup"><span data-stu-id="b4084-106">**Test Report**</span></span>
* <span data-ttu-id="b4084-107">**Buchen und senden**</span><span class="sxs-lookup"><span data-stu-id="b4084-107">**Post and Send**</span></span>
* <span data-ttu-id="b4084-108">**Buchen und Drucken**</span><span class="sxs-lookup"><span data-stu-id="b4084-108">**Post and Print**</span></span>
* <span data-ttu-id="b4084-109">**Buchen und per E-Mail senden**</span><span class="sxs-lookup"><span data-stu-id="b4084-109">**Post and Email**</span></span>
* <span data-ttu-id="b4084-110">**Stapelbuchung**</span><span class="sxs-lookup"><span data-stu-id="b4084-110">**Post Batch**</span></span>
* <span data-ttu-id="b4084-111">**Buchungsvorschau**</span><span class="sxs-lookup"><span data-stu-id="b4084-111">**Preview Posting**</span></span>

<span data-ttu-id="b4084-112">Wenn Sie alle Zeilen ausgefüllt und alle Daten des Verkaufsauftrags eingegeben haben, können Sie ihn buchen.</span><span class="sxs-lookup"><span data-stu-id="b4084-112">When you have completed all the lines and entered all the information on the sales order, you can post it.</span></span> <span data-ttu-id="b4084-113">Dies erstellt eine Lieferung und eine Rechnung.</span><span class="sxs-lookup"><span data-stu-id="b4084-113">This creates a shipment and an invoice.</span></span>

<span data-ttu-id="b4084-114">Wenn eine Verkaufsbestellung gebucht wird, wird das Debitorenkonto, die Finanzbuchhaltung und die Artikelposten aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b4084-114">When a sales order is posted, the customer's account, the general ledger, and the item ledger entries are updated.</span></span>

<span data-ttu-id="b4084-115">Für jeden Verkaufsauftrag wird ein Verkaufsposten in der Tabelle **Sachposten** erstellt.</span><span class="sxs-lookup"><span data-stu-id="b4084-115">For each sales order, a sales entry is created in the **G/L Entry** table.</span></span> <span data-ttu-id="b4084-116">Darüber hinaus wird ein Posten in der Tabelle **Kreditorenposten** erzeugt und ein Sachposten im entsprechenden Einkaufskonto.</span><span class="sxs-lookup"><span data-stu-id="b4084-116">An entry is also created in the customer's account in the **Cust. Ledger Entry** table and a general ledger entry is created in the relevant receivables account.</span></span> <span data-ttu-id="b4084-117">Zusätzlich kann das Buchen in einem MwSt.-Posten und einem Sachposten für den Rabattbetrag resultieren.</span><span class="sxs-lookup"><span data-stu-id="b4084-117">In addition, posting the order may result in a VAT entry and a general ledger entry for the discount amount.</span></span> <span data-ttu-id="b4084-118">Ob ein Posten für Rabatt gebucht wird, hängt von den Einstellungen im Feld **Rabattbuchung** auf der Seite **Debitoren & Verkauf Einr.** ab.</span><span class="sxs-lookup"><span data-stu-id="b4084-118">Whether an entry for the discount is posted depends on the contents of the **Discount Posting** field on the **Sales & Receivables Setup** page.</span></span>

<span data-ttu-id="b4084-119">Für jede Zeile des Verkaufsauftrags wird ein Artikelposten in der Tabelle **Artikelposten** erzeugt (wenn die Verkaufszeilen Artikelnummern enthalten) oder es wird ein Sachposten in der Tabelle **Sachposten** erzeugt (wenn die Verkaufszeilen Sachkonten enthalten).</span><span class="sxs-lookup"><span data-stu-id="b4084-119">For each sales order line, an item ledger entry will be created in the **Item Ledger Entry** table (if the sales lines contain item numbers) or a general ledger entry will be created in the **G/L Entry** table (if the sales lines contain a general ledger account).</span></span> <span data-ttu-id="b4084-120">Zusätzlich dazu werden Verkaufsaufträge immer in den Tabellen **Verkaufslieferkopf** und **Verkaufsrechnungskopf** gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b4084-120">In addition to this, sales orders are always recorded in the **Sales Shipment Header** and **Sales Invoice Header** tables.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="b4084-121">Wenn Sie einen Auftrag buchen, können Sie sowohl einen Lieferschein als auch eine Rechnung erzeugen.</span><span class="sxs-lookup"><span data-stu-id="b4084-121">When you post an order, you can create both a shipment and an invoice.</span></span> <span data-ttu-id="b4084-122">Dies kann gleichzeitig oder unabhängig voneinander getan werden.</span><span class="sxs-lookup"><span data-stu-id="b4084-122">These can be done at the same time or independently.</span></span> <span data-ttu-id="b4084-123">Sie können auch eine Teillieferung und eine Teilrechnung erzeugen, indem Sie die Felder **Menge zu liefern** und/oder **Menge zu fakturieren** in den jeweiligen Zeilen des Verkaufsauftrags ausfüllen, bevor Sie buchen.</span><span class="sxs-lookup"><span data-stu-id="b4084-123">You can also create a partial shipment and a partial invoice by completing the **Qty. to Ship** and **Qty. to Invoice** fields on the individual sales order lines before you post.</span></span> <span data-ttu-id="b4084-124">Beachten Sie, dass Sie keine Rechnung ausstellen können, solange die entsprechende Lieferung nicht erfolgt ist.</span><span class="sxs-lookup"><span data-stu-id="b4084-124">Note that you cannot create an invoice for something that is not shipped.</span></span> <span data-ttu-id="b4084-125">Bevor Sie also die Fakturierung durchführen können, müssen Sie einen Lieferschein erstellt oder die Funktion zur gleichzeitigen Lieferung und Fakturierung gewählt haben.</span><span class="sxs-lookup"><span data-stu-id="b4084-125">That is, before you can invoice, you must have recorded a shipment, or you must choose to ship and invoice at the same time.</span></span>

<span data-ttu-id="b4084-126">Wenn die Buchung vollständig ist, werden die gebuchten Verkaufszeilen aus der Bestellung entfernt.</span><span class="sxs-lookup"><span data-stu-id="b4084-126">When the posting is completed, the posted sales lines are removed from the order.</span></span> <span data-ttu-id="b4084-127">Eine Meldung erscheint, die Ihnen mitteilt, dass die Buchung vollständig ist.</span><span class="sxs-lookup"><span data-stu-id="b4084-127">A message tells you when the posting is completed.</span></span> <span data-ttu-id="b4084-128">Im Anschluss können Sie die gebuchten Posten auf den verschiedenen Seiten einsehen, die gebuchte Posten enthalten, einschließlich **Debitorenposten**, **Sachposten**, **Artikelposten**, **Lagerplatzposten**, **Geb. Verkaufsrechnung**.</span><span class="sxs-lookup"><span data-stu-id="b4084-128">After this, you will be able to see the posted entries in the various pages that contain posted entries, such as the **Cust. Ledger Entries**, **G/L Entries**, **Item Ledger Entries**, **Posted Sales Shipments**, and **Posted Sales Invoices** pages.</span></span>

## <a name="see-also"></a><span data-ttu-id="b4084-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4084-129">See Also</span></span>
[<span data-ttu-id="b4084-130">Verkauf</span><span class="sxs-lookup"><span data-stu-id="b4084-130">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="b4084-131">Senden von Belegen über E-Mail</span><span class="sxs-lookup"><span data-stu-id="b4084-131">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="b4084-132">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b4084-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

