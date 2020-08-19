---
title: Erstellen Sie einen Verkaufsauftrag, der mit einer Einkaufsbestellung für eine direkte Lieferung verknüpft ist | Microsoft Docs
description: Beschreibt, wie Sie einen Verkaufsauftrag erstellen, der mit einer Bestellung verknüpft ist, um sicherzustellen, dass die Artikel vom Kreditor direkt an den Debitor versendet werden
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 7cc6101fbd63ed7bc4f92372acf651fe8868c7be
ms.sourcegitcommit: 6078bc9b2b571248d779722ce4125f250e7a3922
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/07/2020
ms.locfileid: "3666972"
---
# <a name="make-drop-shipments"></a><span data-ttu-id="5fc01-103">Direktlieferungen machen</span><span class="sxs-lookup"><span data-stu-id="5fc01-103">Make Drop Shipments</span></span>
<span data-ttu-id="5fc01-104">Eine Direktlieferung ist die Lieferung von Artikeln, von einem Ihrer Kreditoren direkt an einen Ihrer Debitoren.</span><span class="sxs-lookup"><span data-stu-id="5fc01-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="5fc01-105">Wenn ein Verkaufsauftrag für die Direktlieferung markiert ist und Sie einen Verkaufsauftrag erstellen, bei dem der Kunde im **Lief. an**-Feld, **Adresse Debitor** angegeben ist, können Sie die beiden Dokumente verknüpfen und so den Lieferanten anweisen, direkt an den Kunden zu senden.</span><span class="sxs-lookup"><span data-stu-id="5fc01-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Ship-to** field, **Customer Address**, you can link the two documents to instruct the vendor to ship directly to the customer.</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="5fc01-106">So erstellen Sie einen Verkaufsauftrag für eine Direktlieferung</span><span class="sxs-lookup"><span data-stu-id="5fc01-106">To create a sales order for drop shipment</span></span>
<span data-ttu-id="5fc01-107">Um eine Direktlieferung vorzubereiten, erstellen Sie einen normalen Verkaufsauftrag für einen Artikel und geben in der Verkaufsauftragszeile an, dass für den Verkauf Direktlieferung benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="5fc01-107">To prepare a drop shipment, you create a sales order for an item and indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="5fc01-108">Legen Sie einen Verkaufsauftrag für einen Artikel an.</span><span class="sxs-lookup"><span data-stu-id="5fc01-108">Create a sales order for an item.</span></span> <span data-ttu-id="5fc01-109">Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)</span><span class="sxs-lookup"><span data-stu-id="5fc01-109">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="5fc01-110">Aktivieren Sie in der Verkaufsauftragszeile für den Direktlieferungsartikel das Kontrollkästchen **Direktlieferung**.</span><span class="sxs-lookup"><span data-stu-id="5fc01-110">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="5fc01-111">Verwenden Sie die Funktion **Spalten auswählen**, wenn das Feld nicht sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="5fc01-111">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="5fc01-112">Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="5fc01-112">For more information, see [Personalize Your Workspace](ui-personalization-user.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="5fc01-113">So erstellen Sie Bestellungen für Direktlieferungen:</span><span class="sxs-lookup"><span data-stu-id="5fc01-113">To create the purchase order for drop shipment</span></span>
<span data-ttu-id="5fc01-114">Um eine Direktlieferung vorzubereiten, geben Sie auf der Bestellung an, dass sie an Ihren Kunden und nicht an Sie selbst versendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="5fc01-114">To prepare a drop shipment, you indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="5fc01-115">Erstellen Sie eine Bestellung.</span><span class="sxs-lookup"><span data-stu-id="5fc01-115">Create a purchase order.</span></span> <span data-ttu-id="5fc01-116">Füllen Sie keines dieser Felder in den Zeilen aus.</span><span class="sxs-lookup"><span data-stu-id="5fc01-116">Do not fill any fields on the lines.</span></span> <span data-ttu-id="5fc01-117">Weitere Informationen finden Sie unter [Erfassen eines Einkaufs](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="5fc01-117">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="5fc01-118">Wählen Sie im Feld **Lief. an** **Adresse Debitor** aus.</span><span class="sxs-lookup"><span data-stu-id="5fc01-118">In the **Ship-to** field, select **Customer Address**.</span></span>
3. <span data-ttu-id="5fc01-119">Wählen Sie im Feld **Debitor** den Debitor aus, an den Sie verkaufen.</span><span class="sxs-lookup"><span data-stu-id="5fc01-119">In the **Customer** field, select the customer that you are selling to.</span></span>
3. <span data-ttu-id="5fc01-120">Wählen Sie die Aktion **Direktlieferungen** aus, und dann die Aktion **Auftrag holen**.</span><span class="sxs-lookup"><span data-stu-id="5fc01-120">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
4. <span data-ttu-id="5fc01-121">Auf der Seite **Verkaufsübersicht** wählen Sie den Auftrag, den Sie im Abschnitt [So erstellen Sie einen Verkaufsauftrag für Direktlieferung](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment) vorbereitet haben.</span><span class="sxs-lookup"><span data-stu-id="5fc01-121">On the **Sales List** page, select the sales order that you prepared in [To create a sales order for drop shipment](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span></span>
5. <span data-ttu-id="5fc01-122">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="5fc01-122">Choose the **OK** button.</span></span>

<span data-ttu-id="5fc01-123">Die Zeileninformation aus dem Auftrag werden in die Bestellzeile eingetragen.</span><span class="sxs-lookup"><span data-stu-id="5fc01-123">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="5fc01-124">Sie können nun den Kreditor anweisen, die Artikel an Ihren Debitoren zu versenden, indem Sie ihm beispielsweise die Bestellung als PDF-Datei senden.</span><span class="sxs-lookup"><span data-stu-id="5fc01-124">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-create-multiple-purchase-orders-for-drop-shipments"></a><span data-ttu-id="5fc01-125">Um mehrere Bestellungen für Direktlieferungen zu erstellen</span><span class="sxs-lookup"><span data-stu-id="5fc01-125">To create multiple purchase orders for drop shipments</span></span>
<span data-ttu-id="5fc01-126">Sie können auch das Anforderungsarbeitsblatt verwenden, um die Bestellung für den Lieferanten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5fc01-126">You can also use the requisition worksheet to create the purchase order for the vendor.</span></span> <span data-ttu-id="5fc01-127">Der Vorteil der Verwendung des Anforderungsarbeitsblatts besteht darin, dass Bestellungen für alle ausstehenden Direktlieferungen erstellt werden können, sodass Sie nicht jede einzeln erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="5fc01-127">The advantage of using the requisition worksheet is that it can create purchase orders for all outstanding drop shipments, so you don't have to create each one individually.</span></span>

1. <span data-ttu-id="5fc01-128">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Anforderungsarbeitsblatt** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="5fc01-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Requistion Worksheets**, and then choose the related link.</span></span>
2. <span data-ttu-id="5fc01-129">Wählen Sie die Aktion **Direktlieferungen** aus, und dann die Aktion **Auftrag holen**.</span><span class="sxs-lookup"><span data-stu-id="5fc01-129">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
3. <span data-ttu-id="5fc01-130">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="5fc01-130">Choose the **OK** button.</span></span>
4. <span data-ttu-id="5fc01-131">Überprüfen Sie die Bestellpositionen und im Feld **Lieferanten-Nr.** wählen Sie den Lieferanten aus, der die erforderlichen Waren liefert.</span><span class="sxs-lookup"><span data-stu-id="5fc01-131">Review the purchase order lines, and in the **Vendor No.** field, select vendor that supplies required goods.</span></span> 
5. <span data-ttu-id="5fc01-132">Wählen Sie die Aktion **Ereignismeldung ausführen** \* zum Konvertieren überprüfter Zeilen in eine Bestellung.</span><span class="sxs-lookup"><span data-stu-id="5fc01-132">Choose the **Carry Out Action Message**\* action to convert reviewed lines to a purchase order.</span></span>

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="5fc01-133">So zeigen Sie den verknüpften Auftrag aus der Bestellung an</span><span class="sxs-lookup"><span data-stu-id="5fc01-133">To view the linked purchase order from the sales order</span></span>
* <span data-ttu-id="5fc01-134">Wählen Sie die Verkaufsauftragszeile der Direktlieferung aus, dann die Aktion **Bestellung**, die Aktion **Direktlieferung** und die Aktion **Bestellung**.</span><span class="sxs-lookup"><span data-stu-id="5fc01-134">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="5fc01-135">So buchen Sie eine Direktlieferung:</span><span class="sxs-lookup"><span data-stu-id="5fc01-135">To post a drop shipment</span></span>
<span data-ttu-id="5fc01-136">Wenn der Kreditor die Artikel geliefert hat, können Sie den Verkaufsauftrag als geliefert buchen.</span><span class="sxs-lookup"><span data-stu-id="5fc01-136">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="5fc01-137">Sie können auch die Bestellung buchen, aber nur mit der Option **Erhalten** bis der Verkaufsauftrag fakturiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5fc01-137">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="5fc01-138">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") Symbol öffnet, geben Sie **Verkaufsaufträge** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="5fc01-138">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="5fc01-139">Öffnen Sie den Verkaufsauftrag, den Sie in [So erstellen Sie einen Verkaufsauftrag für Direktlieferung](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment) erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="5fc01-139">Open the sales order that you created in [To create a sales order for drop shipment]().</span></span>
3. <span data-ttu-id="5fc01-140">Geben Sie im Feld **Zu liefern** an, wieviele der Bestellmengen geliefert werden sollen, die gesamte Menge oder eine Teilmenge.</span><span class="sxs-lookup"><span data-stu-id="5fc01-140">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="5fc01-141">Wählen Sie die Aktion **Buchen** oder **Buchen und Senden** aus.</span><span class="sxs-lookup"><span data-stu-id="5fc01-141">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="5fc01-142">Wählen Sie dann entweder die Option **Liefern**, um zu einem späteren Zeitpunkt zu fakturieren oder **Liefern und Fakturieren**, um sofort zu fakturieren.</span><span class="sxs-lookup"><span data-stu-id="5fc01-142">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="5fc01-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5fc01-143">See Also</span></span>
[<span data-ttu-id="5fc01-144">Spezialaufträge erstellen:</span><span class="sxs-lookup"><span data-stu-id="5fc01-144">Create Special Orders</span></span>](sales-how-to-create-special-orders.md)  
[<span data-ttu-id="5fc01-145">Einkauf von Artikeln für einen Verkauf</span><span class="sxs-lookup"><span data-stu-id="5fc01-145">Purchase Items for a Sale</span></span>](purchasing-how-purchase-products-sale.md)  
[<span data-ttu-id="5fc01-146">Produkte verkaufen</span><span class="sxs-lookup"><span data-stu-id="5fc01-146">Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="5fc01-147">Erfassen eines Einkaufs</span><span class="sxs-lookup"><span data-stu-id="5fc01-147">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="5fc01-148">Verkauf</span><span class="sxs-lookup"><span data-stu-id="5fc01-148">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="5fc01-149">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="5fc01-149">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="5fc01-150">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5fc01-150">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
