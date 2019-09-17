---
title: Verkaufsdokumente buchen | Microsoft Docs
description: Erfahren Sie mehr über die verschiedenen Buchungsfunktionen zum Buchen von Verkaufsbelegen und wie Sie gebuchte Belege aktualisieren können.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 08/27/2019
ms.author: sgroespe
ms.openlocfilehash: a2eb27a541033b755b9ab9d4ea9156bf7de9cab4
ms.sourcegitcommit: f46793abdb3efd8384c10eb7992e076383251f2c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2019
ms.locfileid: "1921430"
---
# <a name="posting-sales"></a><span data-ttu-id="5b860-103">Verkäufe buchen</span><span class="sxs-lookup"><span data-stu-id="5b860-103">Posting Sales</span></span>
<span data-ttu-id="5b860-104">Unter dem Menü **Buchen** in einem Verkaufsbeleg auswählen können Sie zwischen den folgenden Buchungsfunktionen auswählen:</span><span class="sxs-lookup"><span data-stu-id="5b860-104">Under the **Posting** menu in a sales document, you can choose between the following posting functions:</span></span>

* <span data-ttu-id="5b860-105">**Veröffentlichen**</span><span class="sxs-lookup"><span data-stu-id="5b860-105">**Post**</span></span>
* <span data-ttu-id="5b860-106">**Buchen und neu**</span><span class="sxs-lookup"><span data-stu-id="5b860-106">**Post and New**</span></span>
* <span data-ttu-id="5b860-107">**Buchen und senden**</span><span class="sxs-lookup"><span data-stu-id="5b860-107">**Post and Send**</span></span>
* <span data-ttu-id="5b860-108">**Buchungsvorschau**</span><span class="sxs-lookup"><span data-stu-id="5b860-108">**Preview Posting**</span></span>
* <span data-ttu-id="5b860-109">**Rechnungsentwurf**</span><span class="sxs-lookup"><span data-stu-id="5b860-109">**Draft Invoice**</span></span>
* <span data-ttu-id="5b860-110">**Proforma-Rechnung**</span><span class="sxs-lookup"><span data-stu-id="5b860-110">**Pro Forma Invoice**</span></span>
* <span data-ttu-id="5b860-111">**Testbericht**</span><span class="sxs-lookup"><span data-stu-id="5b860-111">**Test Report**</span></span>

<span data-ttu-id="5b860-112">Wenn Sie alle Zeilen ausgefüllt und alle Daten des Verkaufsauftrags eingegeben haben, können Sie ihn buchen.</span><span class="sxs-lookup"><span data-stu-id="5b860-112">When you have completed all the lines and entered all the information on the sales order, you can post it.</span></span> <span data-ttu-id="5b860-113">Dies erstellt eine Lieferung und eine Rechnung.</span><span class="sxs-lookup"><span data-stu-id="5b860-113">This creates a shipment and an invoice.</span></span>

<span data-ttu-id="5b860-114">Wenn eine Verkaufsbestellung gebucht wird, wird das Debitorenkonto, die Finanzbuchhaltung und die Artikelposten aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5b860-114">When a sales order is posted, the customer's account, the general ledger, and the item ledger entries are updated.</span></span>

<span data-ttu-id="5b860-115">Für jeden Verkaufsauftrag wird ein Verkaufsposten in der Tabelle **Sachposten** erstellt.</span><span class="sxs-lookup"><span data-stu-id="5b860-115">For each sales order, a sales entry is created in the **G/L Entry** table.</span></span> <span data-ttu-id="5b860-116">Darüber hinaus wird ein Posten in der Tabelle **Kreditorenposten** erzeugt und ein Sachposten im entsprechenden Einkaufskonto.</span><span class="sxs-lookup"><span data-stu-id="5b860-116">An entry is also created in the customer's account in the **Cust. Ledger Entry** table and a general ledger entry is created in the relevant receivables account.</span></span> <span data-ttu-id="5b860-117">Zusätzlich kann das Buchen in einem MwSt.-Posten und einem Sachposten für den Rabattbetrag resultieren.</span><span class="sxs-lookup"><span data-stu-id="5b860-117">In addition, posting the order may result in a VAT entry and a general ledger entry for the discount amount.</span></span> <span data-ttu-id="5b860-118">Ob ein Posten für Rabatt gebucht wird, hängt von den Einstellungen im Feld **Rabattbuchung** auf der Seite **Debitoren & Verkauf Einr.** ab.</span><span class="sxs-lookup"><span data-stu-id="5b860-118">Whether an entry for the discount is posted depends on the contents of the **Discount Posting** field on the **Sales & Receivables Setup** page.</span></span>

<span data-ttu-id="5b860-119">Für jede Zeile des Verkaufsauftrags wird ein Artikelposten in der Tabelle **Artikelposten** erzeugt (wenn die Verkaufszeilen Artikelnummern enthalten) oder es wird ein Sachposten in der Tabelle **Sachposten** erzeugt (wenn die Verkaufszeilen Sachkonten enthalten).</span><span class="sxs-lookup"><span data-stu-id="5b860-119">For each sales order line, an item ledger entry will be created in the **Item Ledger Entry** table (if the sales lines contain item numbers) or a general ledger entry will be created in the **G/L Entry** table (if the sales lines contain a general ledger account).</span></span> <span data-ttu-id="5b860-120">Zusätzlich dazu werden Verkaufsaufträge immer in den Tabellen **Verkaufslieferkopf** und **Verkaufsrechnungskopf** gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5b860-120">In addition to this, sales orders are always recorded in the **Sales Shipment Header** and **Sales Invoice Header** tables.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="5b860-121">Wenn Sie einen Auftrag buchen, können Sie sowohl einen Lieferschein als auch eine Rechnung erzeugen.</span><span class="sxs-lookup"><span data-stu-id="5b860-121">When you post an order, you can create both a shipment and an invoice.</span></span> <span data-ttu-id="5b860-122">Dies kann gleichzeitig oder unabhängig voneinander getan werden.</span><span class="sxs-lookup"><span data-stu-id="5b860-122">These can be done at the same time or independently.</span></span> <span data-ttu-id="5b860-123">Sie können auch eine Teillieferung und eine Teilrechnung erzeugen, indem Sie die Felder **Menge zu liefern** und/oder **Menge zu fakturieren** in den jeweiligen Zeilen des Verkaufsauftrags ausfüllen, bevor Sie buchen.</span><span class="sxs-lookup"><span data-stu-id="5b860-123">You can also create a partial shipment and a partial invoice by completing the **Qty. to Ship** and **Qty. to Invoice** fields on the individual sales order lines before you post.</span></span> <span data-ttu-id="5b860-124">Beachten Sie, dass Sie keine Rechnung ausstellen können, solange die entsprechende Lieferung nicht erfolgt ist.</span><span class="sxs-lookup"><span data-stu-id="5b860-124">Note that you cannot create an invoice for something that is not shipped.</span></span> <span data-ttu-id="5b860-125">Bevor Sie also die Fakturierung durchführen können, müssen Sie einen Lieferschein erstellt oder die Funktion zur gleichzeitigen Lieferung und Fakturierung gewählt haben.</span><span class="sxs-lookup"><span data-stu-id="5b860-125">That is, before you can invoice, you must have recorded a shipment, or you must choose to ship and invoice at the same time.</span></span>

<span data-ttu-id="5b860-126">Wenn die Buchung vollständig ist, werden die gebuchten Verkaufszeilen aus der Bestellung entfernt.</span><span class="sxs-lookup"><span data-stu-id="5b860-126">When the posting is completed, the posted sales lines are removed from the order.</span></span> <span data-ttu-id="5b860-127">Eine Meldung erscheint, die Ihnen mitteilt, dass die Buchung vollständig ist.</span><span class="sxs-lookup"><span data-stu-id="5b860-127">A message tells you when the posting is completed.</span></span> <span data-ttu-id="5b860-128">Im Anschluss können Sie die gebuchten Posten auf den verschiedenen Seiten einsehen, die gebuchte Posten enthalten, einschließlich **Debitorenposten**, **Sachposten**, **Artikelposten**, **Lagerplatzposten**, **Geb. Verkaufsrechnung**.</span><span class="sxs-lookup"><span data-stu-id="5b860-128">After this, you will be able to see the posted entries in the various pages that contain posted entries, such as the **Cust. Ledger Entries**, **G/L Entries**, **Item Ledger Entries**, **Posted Sales Shipments**, and **Posted Sales Invoices** pages.</span></span>  

<span data-ttu-id="5b860-129">Sie können bestimmte Felder in gebuchten Verkaufsbelegen bearbeiten, z. B. die **Paketverfolgungsnr.**</span><span class="sxs-lookup"><span data-stu-id="5b860-129">You can edit certain fields on posted sales documents, such as the **Package Tracking No.**</span></span> <span data-ttu-id="5b860-130">Feld eingetragen.</span><span class="sxs-lookup"><span data-stu-id="5b860-130">field.</span></span> <span data-ttu-id="5b860-131">Weitere Informationen finden Sie unter [Gebuchte Belege bearbeiten](across-edit-posted-document.md).</span><span class="sxs-lookup"><span data-stu-id="5b860-131">For more information, see [Edit Posted Documents](across-edit-posted-document.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5b860-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b860-132">See Also</span></span>
[<span data-ttu-id="5b860-133">Verkauf</span><span class="sxs-lookup"><span data-stu-id="5b860-133">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="5b860-134">Gebuchte Belege bearbeiten</span><span class="sxs-lookup"><span data-stu-id="5b860-134">Edit Posted Documents</span></span>](across-edit-posted-document.md)  
[<span data-ttu-id="5b860-135">Senden von Belegen über E-Mail</span><span class="sxs-lookup"><span data-stu-id="5b860-135">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
[<span data-ttu-id="5b860-136">Ändern oder Löschen einer unbezahlten Verkaufsrechnung</span><span class="sxs-lookup"><span data-stu-id="5b860-136">Correct or Cancel Unpaid Sales Invoices</span></span>](sales-how-correct-cancel-sales-invoice.md)  
[<span data-ttu-id="5b860-137">Verwenden von „Wie möchten Sie weiter verfahren“ bei der Suche nach Funktionen und Informationen</span><span class="sxs-lookup"><span data-stu-id="5b860-137">Using Tell Me to Find Features and Information</span></span>](ui-search.md)  
<span data-ttu-id="5b860-138">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5b860-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
