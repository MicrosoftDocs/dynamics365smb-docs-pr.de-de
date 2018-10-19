---
title: "Einrichten und Verwenden von Standardzeilen für Wiederverkäufe und -einkäufe| Microsoft Docs"
description: "Sie können Verkaufszeilen und Einkaufszeilen einrichten, die Sie häufig machen und diese dann in Verkaufs- und Einkaufsbelegen einfügen, um die Zeilen mit Standardinformationen schnell auszufüllen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: df4f093ded0a55d45c40be15c5888035d6e3b2df
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="create-recurring-sales-and-purchase-lines"></a><span data-ttu-id="ff188-103">Erstellen Sie wiederkehrende Verkaufs- und Einkaufszeilen</span><span class="sxs-lookup"><span data-stu-id="ff188-103">Create Recurring Sales and Purchase Lines</span></span>
<span data-ttu-id="ff188-104">Wenn Sie häufiger Verkaufs- und Einkaufszeilen mit ähnlichen Daten erstellen müssen, können Sie die Standardzeilen einrichten, die Sie in wiederkehrenden Verkaufs- und Einkaufsbelegen, z. B. für wiederkehrende Ersatzaufträge benötigen.</span><span class="sxs-lookup"><span data-stu-id="ff188-104">If you often need to create sales and purchase lines with similar information, you can set up standard lines that you can then insert on recurring sales and purchase documents, for example, for recurring replenishment orders.</span></span>  

<span data-ttu-id="ff188-105">Der folgende Ablauf zeigt, wie man Standardverkaufszeilen einrichtet.</span><span class="sxs-lookup"><span data-stu-id="ff188-105">The following procedure shows how to work with standard sales lines.</span></span> <span data-ttu-id="ff188-106">Es geht auf ähnliche Weise für Standardeinkaufszeilen.</span><span class="sxs-lookup"><span data-stu-id="ff188-106">It works in a similar way for standard purchase lines.</span></span>  

## <a name="to-set-up-standard-sales-lines"></a><span data-ttu-id="ff188-107">So richten Sie eine Standard-Verkaufszeile ein</span><span class="sxs-lookup"><span data-stu-id="ff188-107">To set up standard sales lines</span></span>  
1. <span data-ttu-id="ff188-108">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Standard-Verkaufszeilen** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="ff188-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Standard Sales Lines**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ff188-109">Wählen Sie im Fenster **Standardverkaufszeile** die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="ff188-109">In the **Standard Sales Lines** window, choose the **New** action.</span></span>  
3. <span data-ttu-id="ff188-110">Füllen Sie im Inforegister **Allgemein** die notwendigen Felder aus.</span><span class="sxs-lookup"><span data-stu-id="ff188-110">On the **General** FastTab, fill the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="ff188-111">Im Inforegister **Zeilen** können Sie Informationen in die Felder eingeben, um Verkaufszeilen vorzubereiten, die die Standardzeilen widerspiegeln, von der Sie erwarten, wiederkehrende Zeilen in Einkaufsbelegen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff188-111">On the **Lines** FastTab, enter information in the fields to prepare sales lines that reflect the standard lines that you expect to use as recurring lines on sales documents.</span></span>  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a><span data-ttu-id="ff188-112">Um auf einer Verkaufsrechnung Standardverkaufszeilen einfügen</span><span class="sxs-lookup"><span data-stu-id="ff188-112">To insert standard sales lines on a sales invoice</span></span>
1. <span data-ttu-id="ff188-113">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Rechnung** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="ff188-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="ff188-114">Öffnen Sie die Verkaufsrechnung, in die Sie eine oder mehrere Standard-Verkaufszeilen einfügen möchten.</span><span class="sxs-lookup"><span data-stu-id="ff188-114">Open the sales invoice that you want to insert one or more standard sales lines on.</span></span>
3. <span data-ttu-id="ff188-115">Wählen Sie die **Wiederkehrende Verkaufszeilen abrufen** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="ff188-115">Choose the **Get Recurring Sales Lines** action.</span></span>
4. <span data-ttu-id="ff188-116">Im Fenster **Wiederkehrende Verkaufszeilen** wählen Sie die Suchschaltfläche im Feld **Code**, und wählen einen Satz von Standardverkaufszeilen aus.</span><span class="sxs-lookup"><span data-stu-id="ff188-116">In the **Recurring Sales Lines** window, choose the lookup button in the **Code** field, and then select a set of standard sales lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ff188-117">Um wiederkehrenden die Verkaufszeilen zu verwenden, die bei der Stapelverarbeitung **Wiederkehrende Verkaufsrechnungen erstellen** festgelegt werden, müssen Sie die Felder **Gültig ab-Datum** und **Gültig bis-Datum** im Fenster **Wiederkehrende Verkaufszeilen** ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="ff188-117">To use the recurring sales lines set together with the **Create Recurring Sales Invoices** batch job, you must also fill in the **Valid From Date** and **Valid To Date** fields in the **Recurring Sales Lines** window.</span></span> <span data-ttu-id="ff188-118">Weitere Informationen finden Sie unter Vorgehensweise: Mehrere Verkaufsrechnungen auf der Grundlage von Standardverkaufscodes erstellen</span><span class="sxs-lookup"><span data-stu-id="ff188-118">For more information, see the "To create multiple sales invoices based on standard sales lines" section.</span></span>

5. <span data-ttu-id="ff188-119">Wählen Sie die Schaltfläche **OK**, um die Standardverkaufszeilen in die Rechnung einzufügen, in die Sie Informationen verwenden ist beim oder bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="ff188-119">Choose the **OK** button to insert the standard sales lines on the invoice where you can reuse them as is or edit the information.</span></span>

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a><span data-ttu-id="ff188-120">Vorgehensweise: Mehrere Verkaufsrechnungen auf der Grundlage von Standardverkaufscodes erstellen</span><span class="sxs-lookup"><span data-stu-id="ff188-120">To create multiple sales invoices based on standard sales lines</span></span>
<span data-ttu-id="ff188-121">Sie können mit der Stapelverarbeitung **Wiederkehrende Verkaufsrechnungen erstellen** die Verkaufsrechnungen gemäß Standardverkaufscodes erstellen, die den Debitoren zugeordnet sind und Buchungsdaten enthalten, die innerhalb der Gültigkeitszeiträume liegen, die Sie im Standardverkaufscode festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="ff188-121">You can use the **Create Recurring Sales Invoices** batch job to create sales invoices according to standard sales lines that are assigned to the customers and with posting dates within the valid-from and valid-to dates that you specify on the standard sales lines.</span></span>

> [!NOTE]
> <span data-ttu-id="ff188-122">Im Fenster **Wiederkehrende Verkaufszeilen** können Sie auch eine Einzugsmethode und ein Lastschrift-Mandat angeben.</span><span class="sxs-lookup"><span data-stu-id="ff188-122">In the **Recurring Sales Lines** window, you can also specify a direct-debit payment method and a direct-debit mandate.</span></span> <span data-ttu-id="ff188-123">Die Verkaufsrechnungen, die mit der Stapelverarbeitung **Wiederkehrende Verkaufsrechnungen** erstellt werden, enthalten dann Informationen, die für den Einzug der Zahlungen für die Verkaufsrechnungen per SEPA-Lastschrift benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="ff188-123">The sales invoices that are created with the **Create Recurring Sales Inv.** batch job will then include information required to collect payment for the sales invoices with SEPA direct debit.</span></span> <span data-ttu-id="ff188-124">Weitere Informationen finden Sie unter [Einziehen von Zahlungen mit Abbuchung SEPA](finance-collect-payments-with-sepa-direct-debit.md).</span><span class="sxs-lookup"><span data-stu-id="ff188-124">For more information, see [Collecting Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md).</span></span>

1. <span data-ttu-id="ff188-125">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Wiederk. Verkaufsrechnungen** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="ff188-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Create Recurring Sales Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="ff188-126">Füllen Sie im Fenster **Wiederkehrende Verkaufsrechnung** die Felder wie benötigt aus.</span><span class="sxs-lookup"><span data-stu-id="ff188-126">In the **Create Recurring Sales Invoices** window, fill in the fields as necessary.</span></span>
3. <span data-ttu-id="ff188-127">In dem Feld **Code** geben Sie den Code der Standardverkaufscode ein, die einem Debitor zugewiesen sind, für den Verkaufsrechnungen erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="ff188-127">In the **Code** filter field, enter the code for standard sales lines that are assigned to a customer that you want to create sales invoices for.</span></span>
4. <span data-ttu-id="ff188-128">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="ff188-128">Choose the **OK** button.</span></span>

<span data-ttu-id="ff188-129">Verkaufsrechnungen werden für die Debitoren mit dem angegebenen Standard-Debitorenvertriebscode und allen angegebenen Direkteinzugsinformationen zur Buchung am angegebenen Datum erstellt.</span><span class="sxs-lookup"><span data-stu-id="ff188-129">Sales invoices are created for the customers with the specified standard customer sales code, and any specified direct-debit information, for posting on the specified date.</span></span>

## <a name="see-also"></a><span data-ttu-id="ff188-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff188-130">See Also</span></span>  
[<span data-ttu-id="ff188-131">Verkauf</span><span class="sxs-lookup"><span data-stu-id="ff188-131">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="ff188-132">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ff188-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

