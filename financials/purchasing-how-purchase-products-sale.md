---
title: "Erstellen Sie eine Einkaufsrechnung aus einer Verkaufsrechnung, um Artikel für einen Verkauf zu kaufen | Microsoft Docs"
description: "Von einer Verkaufsrechnung um Produkte einzukaufen, können Sie eine Einkaufsrechnung für einen Kreditor oder Lieferanten einen erstellen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supply planning, sales demand, replenish
ms.date: 05/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 2d7eb238395a0b1060668996fbbc3e13d9dd8a94
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-purchase-items-for-a-sale"></a><span data-ttu-id="651f1-103">Vorgehensweise: Einkauf von Produkten für einen Verkauf</span><span class="sxs-lookup"><span data-stu-id="651f1-103">How to: Purchase Items for a Sale</span></span>
<span data-ttu-id="651f1-104">Bei Verkaufsaufträgen aus der Verkaufsrechnungen können Sie Funktionen verwenden, um für Einkaufsbelege Mengen des fehlenden Stücks schneller zu erstellen, die im Verkauf benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="651f1-104">From sales orders and sales invoices, you can use functions to quickly create purchase documents for missing item quantities that are required by the sale.</span></span> <span data-ttu-id="651f1-105">Sie können zwei verschiedene Funktionen nutzen, abhängig von der Belegart, die verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="651f1-105">You can use two different functions depending on the document type.</span></span>
|<span data-ttu-id="651f1-106">Funktion</span><span class="sxs-lookup"><span data-stu-id="651f1-106">Function</span></span>|<span data-ttu-id="651f1-107">Description</span><span class="sxs-lookup"><span data-stu-id="651f1-107">Description</span></span>|
|--------|-----------|
|<span data-ttu-id="651f1-108">**Einkaufsbestellungen erstellen**</span><span class="sxs-lookup"><span data-stu-id="651f1-108">**Create Purchase Orders**</span></span>|<span data-ttu-id="651f1-109">Bei einem Verkaufsauftrag erstellt diese Funktion eine Einkaufsbestellung für jeden Kreditor aus Artikeln des Verkaufsauftrags.</span><span class="sxs-lookup"><span data-stu-id="651f1-109">From a sales order, this function creates a purchase order for each vendor of items on the sales order.</span></span> <span data-ttu-id="651f1-110">Sie können die Abnahmemenge bearbeiten, bevor Sie die Bestellungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="651f1-110">You can edit the purchase quantity before you create the purchase orders.</span></span> <span data-ttu-id="651f1-111">Nur nicht verfügbare Verkaufsmengen werden vorgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="651f1-111">Only unavailable sales quantities are suggested.</span></span>
|<span data-ttu-id="651f1-112">**Einkaufsrechnung erstellen**</span><span class="sxs-lookup"><span data-stu-id="651f1-112">**Create Purchase Invoice**</span></span>|<span data-ttu-id="651f1-113">Bei einem Verkaufsauftrag und einer Verkaufsrechnung, erstellt diese Funktion eine Einkaufsrechnung für einen ausgewählten Kreditor für alle Zeilen oder nur ausgewählte Zeilen des Verkaufsbelegs.</span><span class="sxs-lookup"><span data-stu-id="651f1-113">From a sales order and from a sales invoice, this function creates a purchase invoice for a selected vendor for all lines or selected lines on the sales document.</span></span> <span data-ttu-id="651f1-114">Die verfügbare Verkaufsmenge wird vorgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="651f1-114">The full sales quantity is suggested.</span></span>|

## <a name="to-create-one-or-more-purchase-orders-from-a-sales-order"></a><span data-ttu-id="651f1-115">Um eine oder mehrere Einkaufsbestellungen aus Verkaufsaufträgen zu erstellen</span><span class="sxs-lookup"><span data-stu-id="651f1-115">To create one or more purchase orders from a sales order</span></span>
<span data-ttu-id="651f1-116">Um eine Bestellung für jede Artikelmenge von nichtverfügbaren Artikeln im Verkaufsauftrag zu erstellen, verwenden Sie die Funktion **Einkaufsbestellungen**.</span><span class="sxs-lookup"><span data-stu-id="651f1-116">To create a purchase order for each unavailable item quantity on the sales order, you use the **Create Purchase Orders** function.</span></span> 

> [!NOTE]  
>   <span data-ttu-id="651f1-117">Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="651f1-117">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="651f1-118">Weitere Informationen finden Sie unter [Anpassen Ihrer [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)Experience.</span><span class="sxs-lookup"><span data-stu-id="651f1-118">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

1. <span data-ttu-id="651f1-119">Auf der Seite Startseite wählen Sie die den Titel **Laufende Verkaufsaufträge** aus.</span><span class="sxs-lookup"><span data-stu-id="651f1-119">On the Home page, choose the **Ongoing Sales Orders** tile.</span></span>
2. <span data-ttu-id="651f1-120">Öffnen Sie einen Verkaufsauftrag für Artikel, die Sie kaufen möchten.</span><span class="sxs-lookup"><span data-stu-id="651f1-120">Open a sales order that you want to purchase items for.</span></span>
3. <span data-ttu-id="651f1-121">Wählen Sie die Aktion **Einkaufsbestellung erstellen**.</span><span class="sxs-lookup"><span data-stu-id="651f1-121">Choose the **Create Purchase Orders** action.</span></span>

    <span data-ttu-id="651f1-122">Das Fenster **Einkaufsbestellungen** wird geöffnet und zeigt eine Zeile für jeden anderen Artikel im Verkaufsauftrag.</span><span class="sxs-lookup"><span data-stu-id="651f1-122">The **Create Purchase Orders** window opens showing a line for each different item on the sales order.</span></span> <span data-ttu-id="651f1-123">Zeilen für verfügbare und nicht verfügbare (abgeblendet) Verkaufsmengen werden standardmäßig angezeigt.</span><span class="sxs-lookup"><span data-stu-id="651f1-123">Lines for both fully available sales quantities and unavailable sales quantities (grayed) are shown by default.</span></span> <span data-ttu-id="651f1-124">Sie können die Funktionen **Anzeigen nicht verfügbar** Aktion auswählen, um Zeilen für nicht verfügbare Verkaufsmengen nur anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="651f1-124">You can choose the **Show Unavailable** action to only see lines for unavailable sales quantities.</span></span>

    <span data-ttu-id="651f1-125">Das Feld **Einzukaufen Menge** enthält standardmäßig die nichtverfügbare Verkaufsmenge.</span><span class="sxs-lookup"><span data-stu-id="651f1-125">The **Quantity to Purchase** field contains the unavailable sales quantity by default.</span></span>
4. <span data-ttu-id="651f1-126">Um eine andere Menge als die nichtverfügbare Verkaufsmenge einzukaufen, ändern Sie den Wert im Feld **Einzukaufende Menge**.</span><span class="sxs-lookup"><span data-stu-id="651f1-126">To purchase another quantity than the unavailable sales quantity, edit the value in the **Quantity to Purchase** field.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="651f1-127">Sie können das Feld **Einzukaufen Menge** in abgeblendeten Zeilen auch ändern, obwohl sie vollständig verfügbare Verkaufsmengen darstellen.</span><span class="sxs-lookup"><span data-stu-id="651f1-127">You can also change the **Quantity to Purchase** field on grayed lines even though they represent fully available sales quantities.</span></span>
5. <span data-ttu-id="651f1-128">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="651f1-128">Choose the **OK** button.</span></span> 
    
    <span data-ttu-id="651f1-129">Eine Bestellung ist für jeden Kreditor der Artikel im Verkaufsauftrag, einschließlich alle Mengenänderungen erstellt, die Sie im **Einkaufsbestellungen** durchgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="651f1-129">A purchase order is created for each vendor of items on the sales order, including any quantity changes that you made in the **Create Purchase Orders** window.</span></span>
7. <span data-ttu-id="651f1-130">Fahren Sie fort, die Einkaufsbestellungen zu verarbeiten, indem Sie beispielsweise Einkaufsbestellungszeilen bearbeiten oder hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="651f1-130">Proceed to process the purchase order or orders, for example, by editing or adding purchase order lines.</span></span> <span data-ttu-id="651f1-131">Weitere Informationen finden Sie unter [So gehts: Erfassen eines Einkaufs](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="651f1-131">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>


## <a name="to-create-a-purchase-invoice-from-a-sales-order-or-sales-invoice"></a><span data-ttu-id="651f1-132">Eine Einkaufsrechnung aus einer Verkaufsbestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="651f1-132">To create a purchase invoice from a sales order or sales invoice</span></span>
<span data-ttu-id="651f1-133">Eine einzelne Einkaufsrechnung für eine oder mehrere Zeilen in einem Verkaufsbeleg erstellen, indem Sie zuerst auswählen, von welchem Kreditor Sie die Funktion **Einkaufsr""echnung erstellen** verwenden.</span><span class="sxs-lookup"><span data-stu-id="651f1-133">To create a single purchase invoice for one or more lines on a sales document by first selecting which vendor to buy from, you use the **Create Purchase Invoice** function.</span></span> 

> [!NOTE]  
>   <span data-ttu-id="651f1-134">Diese Funktion erstellt eine Einkaufsrechnung für die exakte Artikelmenge audf dem ausgewählten Verkaufsbeleg.</span><span class="sxs-lookup"><span data-stu-id="651f1-134">This function creates a purchase invoice for the exact item quantity on the selected sales document.</span></span> <span data-ttu-id="651f1-135">Um die Abnahmemenge zu ändern, müssen Sie die Einkaufsrechnung bearbeiten nachdem sie erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="651f1-135">To change the purchase quantity, you must edit the purchase invoice after it is created.</span></span>  

1. <span data-ttu-id="651f1-136">Auf der Seite Startseite wählen Sie die den Titel **Laufende Verkaufsrechnungen** aus.</span><span class="sxs-lookup"><span data-stu-id="651f1-136">On the Home page, choose the **Ongoing Sales Invoices** tile.</span></span>
2. <span data-ttu-id="651f1-137">Öffnen Sie einen Verkaufsrechnunung für Artikel, die Sie kaufen möchten.</span><span class="sxs-lookup"><span data-stu-id="651f1-137">Open a sales invoice that you want to purchase items for.</span></span>
3. <span data-ttu-id="651f1-138">Wählen Sie eine oder mehrere Rechnungszeilen aus, die Sie auf der Einkaufsrechnung verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="651f1-138">Select one or more sales invoice lines that you want to use on the purchase invoice.</span></span> <span data-ttu-id="651f1-139">Um alle Verkaufsrechnungszeilen zu verwenden, wählen Sie entweder alle oder keine Zeilen aus.</span><span class="sxs-lookup"><span data-stu-id="651f1-139">To use all the sales invoice lines, select either all of them or do not select any lines.</span></span>
4. <span data-ttu-id="651f1-140">Wählen Sie die Aktion **Einkaufsrechnung erstellen**.</span><span class="sxs-lookup"><span data-stu-id="651f1-140">Choose the **Create Purchase Invoice** action.</span></span>
5. <span data-ttu-id="651f1-141">Wählen Sie entweder **Alle Posten** oder **Ausgewählte Posten**, und wählen Sie die **OK**-Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="651f1-141">Select either **All Lines** or **Selected Lines**, and then choose the **OK** button.</span></span>  
6. <span data-ttu-id="651f1-142">In der Kreditorenliste, die erscheint, wählen Sie den Kreditor, der die Artikel oder Dienstleistung liefert, und wählen Sie die Schaltfläche **OK**.</span><span class="sxs-lookup"><span data-stu-id="651f1-142">In the list of vendors that appears, select the vendor that you want to buy all the items from, and then choose the **OK** button.</span></span>

    <span data-ttu-id="651f1-143">Eine Einkaufsrechnung wird erstellt, die eine, mehrere oder alle Zeilen auf der Verkaufsrechnung enthält.</span><span class="sxs-lookup"><span data-stu-id="651f1-143">A purchase invoice is created that contains one, more, or all the lines on the sales invoice.</span></span>
7. <span data-ttu-id="651f1-144">Fahren Sie fort, die Einkaufsrechnung zu verarbeiten, indem Sie beispielsweise Einkaufsrechnungszeilen bearbeiten oder hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="651f1-144">Proceed to process the purchase invoice, for example, by editing or adding purchase invoice lines.</span></span> <span data-ttu-id="651f1-145">Weitere Informationen finden Sie unter [So gehts: Erfassen eines Einkaufs](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="651f1-145">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="651f1-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="651f1-146">See Also</span></span>
[<span data-ttu-id="651f1-147">Einkauf</span><span class="sxs-lookup"><span data-stu-id="651f1-147">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="651f1-148">Vorgehensweise: Erfassen eines Einkaufs</span><span class="sxs-lookup"><span data-stu-id="651f1-148">How to: Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="651f1-149">Vorgehensweise: Fakturieren</span><span class="sxs-lookup"><span data-stu-id="651f1-149">How to: Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="651f1-150">Vorgehensweise: Einen neuen Kreditor registrieren</span><span class="sxs-lookup"><span data-stu-id="651f1-150">How to: Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
<span data-ttu-id="651f1-151">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="651f1-151">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

