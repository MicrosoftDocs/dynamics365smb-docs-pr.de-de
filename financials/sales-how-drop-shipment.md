---
title: "Erstellen Sie einen Verkaufsauftrag, der mit einer Einkaufsbestellung für eine direkte Lieferung verknüpft ist| Microsoft Docs"
description: "Beschreibt, wie Sie einen Verkaufsauftrag erstellen, der mit einer Bestellung verknüpft ist, um sicherzustellen, dass die Artikel vom Kreditor direkt an den Debitor versendet werden"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 977debf7386ad1113ef54147b20fd24c7c285a78
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-make-drop-shipments"></a><span data-ttu-id="eabad-103">So geht's: Direktlieferungen erstellen</span><span class="sxs-lookup"><span data-stu-id="eabad-103">How to: Make Drop Shipments</span></span>
<span data-ttu-id="eabad-104">Eine Direktlieferung ist die Lieferung von Artikeln, von einem Ihrer Kreditoren direkt an einen Ihrer Debitoren.</span><span class="sxs-lookup"><span data-stu-id="eabad-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="eabad-105">Wenn ein Verkaufsauftrag für Direktlieferung markiert wird und Sie eine Bestellung erstellen, in der der Debitor im Feld **Verk. an Deb.-Nr.**</span><span class="sxs-lookup"><span data-stu-id="eabad-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Sell-to Customer No.**</span></span> <span data-ttu-id="eabad-106">angegeben wird, können Sie die beiden Belege verknüpfen und somit den Kreditor anweisen, direkt an den Kunden zu versenden.</span><span class="sxs-lookup"><span data-stu-id="eabad-106">field, you can link the two documents and thereby instruct the vendor to ship directly to the customer.</span></span>

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="eabad-107">So erstellen Sie einen Verkaufsauftrag für eine Direktlieferung</span><span class="sxs-lookup"><span data-stu-id="eabad-107">To create a sales order for drop shipment</span></span>
<span data-ttu-id="eabad-108">Um eine Direktlieferung vorzubereiten, erstellen Sie einen normalen Verkaufsauftrag für einen Artikel, außer dass Sie in der Verkaufsauftragszeile angeben müssen, dass für den Verkauf Direktlieferung benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="eabad-108">To prepare a drop shipment, you create a sales order for an item as normal, except you must indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="eabad-109">Legen Sie einen Verkaufsauftrag für einen Artikel an.</span><span class="sxs-lookup"><span data-stu-id="eabad-109">Create a sales order for an item.</span></span> <span data-ttu-id="eabad-110">Weitere Informationen finden Sie unter [So geht's: Produkte verkaufen](sales-how-sell-products.md)</span><span class="sxs-lookup"><span data-stu-id="eabad-110">For more information, see [How to: Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="eabad-111">Aktivieren Sie in der Verkaufsauftragszeile für den Direktlieferungsartikel das Kontrollkästchen **Direktlieferung**.</span><span class="sxs-lookup"><span data-stu-id="eabad-111">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="eabad-112">Verwenden Sie die Funktion **Spalten auswählen**, wenn das Feld nicht sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="eabad-112">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="eabad-113">Weitere Informationen finden Sie unter [Benutzer-Personalisierung](ui-user-personalization.md).</span><span class="sxs-lookup"><span data-stu-id="eabad-113">For more information, see [User Personalization](ui-user-personalization.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="eabad-114">Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="eabad-114">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="eabad-115">Weitere Informationen finden Sie unter [Anpassen Ihrer [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)Experience.</span><span class="sxs-lookup"><span data-stu-id="eabad-115">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="eabad-116">So erstellen Sie Bestellungen für Direktlieferungen:</span><span class="sxs-lookup"><span data-stu-id="eabad-116">To create the purchase order for drop shipment</span></span>
<span data-ttu-id="eabad-117">Um eine Direktlieferung für den Artikel, der verkauft werden soll, vorzubereiten, erstellen Sie eine normale Bestellung, außer dass Sie in der Bestellung angeben müssen, dass direkt an den Debitoren geliefert wird, nicht an Sie selbst.</span><span class="sxs-lookup"><span data-stu-id="eabad-117">To prepare a drop shipment for the item to be sold, you create a purchase order as normal, except you must indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="eabad-118">Erstellen Sie eine Bestellung.</span><span class="sxs-lookup"><span data-stu-id="eabad-118">Create a purchase order.</span></span> <span data-ttu-id="eabad-119">Füllen Sie keines dieser Felder in den Zeilen aus.</span><span class="sxs-lookup"><span data-stu-id="eabad-119">Do not fill any fields on the lines.</span></span> <span data-ttu-id="eabad-120">Weitere Informationen finden Sie unter [So gehts: Erfassen eines Einkaufs](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="eabad-120">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="eabad-121">Wählen Sie im Feld **Verk. an Deb.-Nr.**</span><span class="sxs-lookup"><span data-stu-id="eabad-121">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="eabad-122">den Debitor aus, an die Sie verkaufen.</span><span class="sxs-lookup"><span data-stu-id="eabad-122">field, select the customer that you are selling to.</span></span>
3. <span data-ttu-id="eabad-123">Wählen Sie die Aktion **Direktlieferungen** aus, und dann die Aktion **Auftrag holen**.</span><span class="sxs-lookup"><span data-stu-id="eabad-123">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
4. <span data-ttu-id="eabad-124">Im Fenster **Verkaufsübersicht** wählen Sie den Auftrag, den Sie im Abschnitt "So erstellen Sie einen Verkaufsauftrag für Direktlieferung" vorbereitet haben.</span><span class="sxs-lookup"><span data-stu-id="eabad-124">In the **Sales List** window, select the sales order that you prepared in the "To create a sales order for drop shipment" section.</span></span>
5. <span data-ttu-id="eabad-125">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="eabad-125">Choose the **OK** button.</span></span>

<span data-ttu-id="eabad-126">Die Zeileninformation aus dem Auftrag werden in die Bestellzeile eingetragen.</span><span class="sxs-lookup"><span data-stu-id="eabad-126">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="eabad-127">Sie können nun den Kreditor anweisen, die Artikel an Ihren Kunden zu versenden, indem Sie ihm beispielsweise die Bestellung als PDF-Datei senden.</span><span class="sxs-lookup"><span data-stu-id="eabad-127">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="eabad-128">So zeigen Sie den verknüpften Auftrag aus der Bestellung an</span><span class="sxs-lookup"><span data-stu-id="eabad-128">To view the linked purchase order from the sales order</span></span>
* <span data-ttu-id="eabad-129">Wählen Sie die Verkaufsauftragszeile der Direktlieferung aus, dann die Aktion **Bestellung**, die Aktion **Direktlieferung** und die Aktion **Bestellung**.</span><span class="sxs-lookup"><span data-stu-id="eabad-129">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="eabad-130">So buchen Sie eine Direktlieferung:</span><span class="sxs-lookup"><span data-stu-id="eabad-130">To post a drop shipment</span></span>
<span data-ttu-id="eabad-131">Wenn der Kreditor die Artikel geliefert hat, können Sie den Verkaufsauftrag als geliefert buchen.</span><span class="sxs-lookup"><span data-stu-id="eabad-131">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="eabad-132">Sie können auch die Bestellung buchen, aber nur mit der Option **Erhalten** bis der Verkaufsauftrag fakturiert wurde.</span><span class="sxs-lookup"><span data-stu-id="eabad-132">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="eabad-133">Alternativ wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Verkaufsauftrag** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="eabad-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="eabad-134">Öffnen Sie den Verkaufsauftrag, den Sie im Abschnitt "So erstellen Sie einen Verkaufsauftrag für Direktlieferung" erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="eabad-134">Open the sales order that you created in the "To create a sales order for a drop shipment" section.</span></span>
3. <span data-ttu-id="eabad-135">Geben Sie im Feld **Zu liefern** an, wieviele der Bestellmengen geliefert werden sollen, die gesamte Menge oder eine Teilmenge.</span><span class="sxs-lookup"><span data-stu-id="eabad-135">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="eabad-136">Wählen Sie die Aktion **Buchen** oder **Buchen und Senden** aus.</span><span class="sxs-lookup"><span data-stu-id="eabad-136">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="eabad-137">Wählen Sie dann entweder die Option **Liefern**, um zu einem späteren Zeitpunkt zu fakturieren oder **Liefern und Fakturieren**, um sofort zu fakturieren.</span><span class="sxs-lookup"><span data-stu-id="eabad-137">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="eabad-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eabad-138">See Also</span></span>
[<span data-ttu-id="eabad-139">Gewusst wie: Produkte verkaufen</span><span class="sxs-lookup"><span data-stu-id="eabad-139">How to: Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="eabad-140">Vorgehensweise: Erfassen eines Einkaufs</span><span class="sxs-lookup"><span data-stu-id="eabad-140">How to: Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="eabad-141">Verkauf</span><span class="sxs-lookup"><span data-stu-id="eabad-141">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="eabad-142">Lagerbest</span><span class="sxs-lookup"><span data-stu-id="eabad-142">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="eabad-143">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="eabad-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

