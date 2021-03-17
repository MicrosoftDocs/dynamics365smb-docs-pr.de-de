---
title: 'Gewusst wie: Vorauszahlungsrechnungen erstellen | Microsoft Docs'
description: Erfahren Sie, wie Sie Situationen bearbeiten, in denen Vorauszahlung gefordert wird, oder Ihr Kreditor dies fordert.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3a1f79f089ef8633ca51be35930c5de5c2401b29
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387399"
---
# <a name="create-prepayment-invoices"></a><span data-ttu-id="f7f00-103">Vorauszahlungsrechnungen erstellen</span><span class="sxs-lookup"><span data-stu-id="f7f00-103">Create Prepayment Invoices</span></span>

<span data-ttu-id="f7f00-104">Wenn Sie von Ihren Debitoren erwarten, dass diese vor der Lieferung eines Auftrags eine Vorauszahlung leisten, können Sie die Funktion „Vorauszahlung“ verwenden.</span><span class="sxs-lookup"><span data-stu-id="f7f00-104">If you require your customers to submit payment before you ship an order to them, you can use the prepayment functionality.</span></span> <span data-ttu-id="f7f00-105">Dies gilt auch, wenn Ihr Verkäufer erwartet, dass Sie die Zahlung übermitteln, bevor er eine Bestellung an Sie versendet.</span><span class="sxs-lookup"><span data-stu-id="f7f00-105">The same applies if your vendor requires you to submit payment before they ship an order to you.</span></span>  

<span data-ttu-id="f7f00-106">Sie können den Vorauszahlungsprozess starten, wenn Sie eine Einkaufsbestellung oder einen Verkaufsauftrag erstellen.</span><span class="sxs-lookup"><span data-stu-id="f7f00-106">You can start the prepayment process when you create a sales or purchase order.</span></span> <span data-ttu-id="f7f00-107">Wenn Sie für diesen Debitor oder Kreditor einen standardmäßigen Vorauszahlungsprozentsatz haben, wird dieser automatisch in die resultierende Vorauszahlungsrechnung aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="f7f00-107">If you have a default prepayment percentage for this customer or vendor, that will be included automatically in the resulting prepayment invoice.</span></span> <span data-ttu-id="f7f00-108">Sie können auch einen Vorauszahlungsprozentsatz für das gesamte Dokument angeben.</span><span class="sxs-lookup"><span data-stu-id="f7f00-108">You can also specify a prepayment percentage to the entire document.</span></span>

<span data-ttu-id="f7f00-109">Nachdem Sie einen Auftrag oder eine Bestellung angelegt haben, können Sie eine Vorauszahlungsrechnung erstellen.</span><span class="sxs-lookup"><span data-stu-id="f7f00-109">After you create a sales or purchase order, you can create a prepayment invoice.</span></span> <span data-ttu-id="f7f00-110">Sie können für Verkaufs- oder Einkaufszeile die Standardprozentsätze verwenden, oder Sie können den Betrag den Anforderungen entsprechend anpassen.</span><span class="sxs-lookup"><span data-stu-id="f7f00-110">You can use the default percentages for each sales or purchase line, or you can adjust the amount as necessary.</span></span> <span data-ttu-id="f7f00-111">So können Sie beispielsweise den Gesamtbetrag für den gesamten Auftrag angeben.</span><span class="sxs-lookup"><span data-stu-id="f7f00-111">For example, you can specify a total amount for the entire order.</span></span>  

<span data-ttu-id="f7f00-112">Im Folgenden wird beschrieben, wie eine Vorauszahlung für einen Verkaufsauftrag fakturiert wird.</span><span class="sxs-lookup"><span data-stu-id="f7f00-112">The following procedure describes how to invoice a prepayment for a sales order.</span></span> <span data-ttu-id="f7f00-113">Die Schritte sind für eine Bestellung ähnlich.</span><span class="sxs-lookup"><span data-stu-id="f7f00-113">The steps are similar for purchase orders.</span></span>  

## <a name="to-create-a-prepayment-invoice"></a><span data-ttu-id="f7f00-114">So erstellen Sie eine Vorauszahlungsrechnung</span><span class="sxs-lookup"><span data-stu-id="f7f00-114">To create a prepayment invoice</span></span>

1. <span data-ttu-id="f7f00-115">Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Verkaufsaufträge** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="f7f00-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f7f00-116">Erstellen Sie einen neuen Verkaufsauftrag für den relevanten Debitor.</span><span class="sxs-lookup"><span data-stu-id="f7f00-116">Create a new sales order for the relevant customer.</span></span> <span data-ttu-id="f7f00-117">Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)</span><span class="sxs-lookup"><span data-stu-id="f7f00-117">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>  

    <span data-ttu-id="f7f00-118">Auf dem Inforegister **Vorauszahlung** gibt das Feld **Vorauszahlung %** den Prozentsatz an, der zur Berechnung des Vorauszahlungsbetrags verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f7f00-118">On the **Prepayment** FastTab, the **Prepayment %** field specifies the percentage to use to calculate the prepayment amount.</span></span> <span data-ttu-id="f7f00-119">Wenn auf der Debitorenkarte ein standardmäßiger Vorauszahlungsprozentsatz angegeben ist, wird das Feld automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="f7f00-119">If there is a default prepayment percentage on the customer card, the field is filled in automatically.</span></span> <span data-ttu-id="f7f00-120">Sie können den Prozentsatz ändern.</span><span class="sxs-lookup"><span data-stu-id="f7f00-120">You can change the percentage.</span></span> <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    <span data-ttu-id="f7f00-121">Wählen Sie das Feld **Vorauszahlung komprimieren** aus, falls Sie auf der Vorauszahlungsrechnung Zeilen erstellen möchten, die Zeilen aus dem Kundenauftrag zusammenfassen, wenn folgende Bedingungen zutreffen:</span><span class="sxs-lookup"><span data-stu-id="f7f00-121">Choose the **Compress Prepayment** field if you want to create lines on the prepayment invoice that combine lines from the sales order if:</span></span>  

    - <span data-ttu-id="f7f00-122">Es wird das gleiche Sachkonto für Vorauszahlungen verwendet, wie unter "Buchungsmatrix Einrichtung" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f7f00-122">They have the same general ledger account for prepayments as determined by the general posting setup.</span></span>  
    - <span data-ttu-id="f7f00-123">Es werden die gleichen Dimensionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="f7f00-123">They have the same dimensions.</span></span>  

    <span data-ttu-id="f7f00-124">Wenn Sie eine Vorauszahlungsrechnung angeben möchten, die für jede Auftragszeile mit einem Vorauszahlungsprozentsatz eine Zeile enthält, wählen Sie nicht das Feld **Vorauszahlung komprimieren** aus.</span><span class="sxs-lookup"><span data-stu-id="f7f00-124">If you want to specify a prepayment invoice with one line for each sales order line that has a prepayment percentage, then do not choose the **Compress Prepayment** field.</span></span>  

    <span data-ttu-id="f7f00-125">Das Fälligkeitsdatum für die Vorauszahlung wird automatisch basierend auf dem Wert für **Zlg.-Bedingungscode Vorauszahlung** berechnet.</span><span class="sxs-lookup"><span data-stu-id="f7f00-125">The due date for the prepayment is calculated automatically based on the value of the **Prepmt. Payment Terms Code**.</span></span>

3. <span data-ttu-id="f7f00-126">Füllen Sie die Verkaufszeilen aus.</span><span class="sxs-lookup"><span data-stu-id="f7f00-126">Fill in the sales lines.</span></span>  

    <span data-ttu-id="f7f00-127">Wenn Sie einen standardmäßigen Vorauszahlungsprozentsatz für den Debitor oder auf dem Inforegister **Vorauszahlung** in diesem Dokument festgelegt haben, wird dieser Wert in jede Zeile kopiert.</span><span class="sxs-lookup"><span data-stu-id="f7f00-127">If you have specified a default prepayment percentage either for the customer or on the **Prepayment** FastTab on this document, this value is copied to each line.</span></span> <span data-ttu-id="f7f00-128">Sie können den Inhalt des Felds  in der Zeile **Vorauszahlung %** ändern.</span><span class="sxs-lookup"><span data-stu-id="f7f00-128">You can change the contents of the **Prepayment %** field on the line.</span></span>  

4. <span data-ttu-id="f7f00-129">Um den gesamten Vorauszahlungsbetrag anzuzeigen, wählen Sie die Aktion **Statistik**.</span><span class="sxs-lookup"><span data-stu-id="f7f00-129">To view the total prepayment amount, choose the **Statistics** action.</span></span>

    <span data-ttu-id="f7f00-130">Wenn Sie den gesamten Vorauszahlungsbetrag für den Auftrag anpassen möchten, können Sie den Inhalt des Feldes **Vorauszahlungsbetrag** auf der Seite **Verkaufsauftragsstatistik** ändern.</span><span class="sxs-lookup"><span data-stu-id="f7f00-130">If you want to adjust the total prepayment amount for the order, you can change the contents of the **Prepayment Amount** field on the **Sales Order Statistics** page.</span></span>  

    <span data-ttu-id="f7f00-131">Wenn das Feld **Preise inkl. MwSt** aktiviert ist, kann das Feld **Vorauszahlungsbetrag einschl. MwSt**. geändert werden.</span><span class="sxs-lookup"><span data-stu-id="f7f00-131">If the **Prices Including VAT** field is selected, the **Prepayment Amount Incl. VAT** field is editable.</span></span>  

    <span data-ttu-id="f7f00-132">Wenn Sie den Inhalt des Felds **Vorauszahlungsbetrag** ändern, wird der Betrag proportional auf alle Zeilen aufgeteilt, mit Ausnahme der Felder, bei denen im Feld **Vorauszahlung** der Wert **0** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="f7f00-132">If you change the contents of the **Prepayment Amount** field, the amount will be distributed proportionately between all lines, except those that have **0** in the **Prepayment %** field.</span></span>  

5. <span data-ttu-id="f7f00-133">Wählen Sie zum Drucken eines Testberichtes vor der Buchung der Vorauszahlungsrechnung die Aktion **Vorauszahlung** und dann die Aktion **Vorauszahlungstestbericht**.</span><span class="sxs-lookup"><span data-stu-id="f7f00-133">To print a test report before posting the prepayment invoice, choose the **Prepayment** action, and then choose the **Prepayment Test Report** action.</span></span>  
6. <span data-ttu-id="f7f00-134">Wählen Sie zum Buchen der Vorauszahlungsrechnung die Aktion **Vorauszahlung**, und dann die Aktion **Vorauszahlungsrechnung**.</span><span class="sxs-lookup"><span data-stu-id="f7f00-134">To post the prepayment invoice, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action.</span></span>  

    <span data-ttu-id="f7f00-135">Klicken Sie zum Buchen und Drucken der Vorauszahlungsrechnung die Aktion **Vorauszahlungsrechnung buchen und drucken**.</span><span class="sxs-lookup"><span data-stu-id="f7f00-135">To post and print the prepayment invoice, choose the **Post and Print Prepmt. Invoice** action.</span></span>  

<span data-ttu-id="f7f00-136">Es können weitere Vorauszahlungsrechnungen für den Auftrag ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f7f00-136">You can issue additional prepayment invoices for the order.</span></span> <span data-ttu-id="f7f00-137">Erhöhen Sie hierzu den Vorauszahlungsbetrag für eine oder mehrere Zeilen, passen Sie im Bedarfsfall das Belegdatum an, und buchen Sie die Vorauszahlungsrechnung.</span><span class="sxs-lookup"><span data-stu-id="f7f00-137">To do this, increase the prepayment amount on one or more lines, adjust the document date if necessary, and post the prepayment invoice.</span></span> <span data-ttu-id="f7f00-138">Für die Differenz zwischen den bisher fakturierten Vorauszahlungsbeträgen und dem neuen Vorauszahlungsbetrag wird eine neue Rechnung erstellt.</span><span class="sxs-lookup"><span data-stu-id="f7f00-138">A new invoice will be created for the difference between the prepayment amounts invoiced so far and the new prepayment amount.</span></span>  

> [!NOTE]  
> <span data-ttu-id="f7f00-139">Wenn Sie in Nordamerika sind, können Sie den Prozentsatz nicht ändern, nachdem die Vorauszahlungsrechnung gebucht wurde.</span><span class="sxs-lookup"><span data-stu-id="f7f00-139">If you are located in North America, you cannot change the prepayment percentage after the prepayment invoice has been posted.</span></span> <span data-ttu-id="f7f00-140">Dieses wird in der nordamerikanischen Version von [!INCLUDE[prod_short](includes/prod_short.md)] verhindert, da die Berechnung der Verkaufssteuer ansonsten falsch ist.</span><span class="sxs-lookup"><span data-stu-id="f7f00-140">This is prevented in the North American version of [!INCLUDE[prod_short](includes/prod_short.md)] because the calculation of sales tax will otherwise be incorrect.</span></span>  

 <span data-ttu-id="f7f00-141">Wenn Sie bereit zum Buchen des verbleibenden Rechnungsbetrags sind, buchen Sie diesen auf die gleiche Weise, wie Sie jede andere Rechnung buchen. Der Vorauszahlungsbetrag wird automatisch vom fälligen Betrag abgezogen.</span><span class="sxs-lookup"><span data-stu-id="f7f00-141">When you are ready to post the rest of the invoice, post it as you would post any invoice, and the prepayment amount will automatically be deducted from the amount due.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f7f00-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7f00-142">See Also</span></span>

[<span data-ttu-id="f7f00-143">Fakturieren von Vorauszahlungen</span><span class="sxs-lookup"><span data-stu-id="f7f00-143">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="f7f00-144">Exemplarische Vorgehensweise: Einrichten und Fakturieren von Verkaufsvorauszahlungen</span><span class="sxs-lookup"><span data-stu-id="f7f00-144">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="f7f00-145">Finanzen</span><span class="sxs-lookup"><span data-stu-id="f7f00-145">Finance</span></span>](finance.md)  
<span data-ttu-id="f7f00-146">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f7f00-146">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]