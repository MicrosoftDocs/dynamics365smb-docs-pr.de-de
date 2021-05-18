---
title: Erstellen Sie eine Projekt-Verkaufsrechnung, um ein Projekt zu fakturieren| Microsoft Docs
description: Beschreibt, wie Debitoren für Jobausgaben als Jobfortschritt Rechnung gestellt wird.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 873135d2fa6053b7101a999981fb3117ee8689ab
ms.sourcegitcommit: 93c8681054b059cec38cb29b86de20be37980676
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938146"
---
# <a name="invoice-jobs"></a><span data-ttu-id="347a8-103">Fakturieren von Projekten</span><span class="sxs-lookup"><span data-stu-id="347a8-103">Invoice Jobs</span></span>
<span data-ttu-id="347a8-104">Im Laufe des Projekts können Projektkosten wie Ressourcenverbrauch, Material oder projektbezogene Einkäufe anfallen.</span><span class="sxs-lookup"><span data-stu-id="347a8-104">During the project, job costs from resource usage, materials, and job-related purchases can accumulate.</span></span> <span data-ttu-id="347a8-105">Diese Transaktionen werden im weiteren Verlauf des Projekts auf das Projekt Buch.-Blatt gebucht.</span><span class="sxs-lookup"><span data-stu-id="347a8-105">As the job progresses, these transactions get posted to the job journal.</span></span> <span data-ttu-id="347a8-106">Dabei ist es wichtig, dass alle Kosten im Projekt Buch.-Blatt erfasst werden, bevor die Rechnung an den Debitor erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="347a8-106">It is important that all costs get recorded in the job journal before you invoice the customer.</span></span>

> [!NOTE]
> <span data-ttu-id="347a8-107">Sie können auch externe Ressourcen erwerben, die nicht mit einem Auftrag verbunden sind, z.B. um einem Kreditor die gelieferte Arbeit in Rechnung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="347a8-107">You can also purchase external resources unrelated to a job, for example, to invoice a vendor for work delivered.</span></span> <span data-ttu-id="347a8-108">Weitere Informationen finden Sie unter [Käufe erfassen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="347a8-108">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

<span data-ttu-id="347a8-109">Sie können das gesamte Projekt auf der Seite **Projektaufgabenzeilen** fakturieren, oder Sie fakturieren lediglich ausgewählte Vertragszeilen auf der Seite **Projektplanzeilen**.</span><span class="sxs-lookup"><span data-stu-id="347a8-109">You can invoice the whole job from the **Job Task Lines** page or only invoice selected billable lines from the **Planning Lines** page.</span></span> <span data-ttu-id="347a8-110">Die Fakturierung kann erfolgen, wenn das Projekt abgeschlossen ist, oder in bestimmten Intervallen während der Projektlaufzeit gemäß eines Fakturierungsplans.</span><span class="sxs-lookup"><span data-stu-id="347a8-110">Invoicing can be done after the job is finished or at certain intervals during the job's progress based on an invoicing schedule.</span></span>

> [!NOTE]  
> <span data-ttu-id="347a8-111">Wenn Sie **Verrechenbar** im Feld **Projekt-Zeilenart** auf den Verkaufsbelegen für projektbezogene Einkäufe auswählen, werden Projektplanzeilen, die bereit sind, an den Debitoren zu fakturieren, erstellt.</span><span class="sxs-lookup"><span data-stu-id="347a8-111">If you select **Billable** in the **Job Line Type** field on the purchase documents for job-related purchases, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="347a8-112">Weitere Informationen finden Sie unter [Verwalten von Projekt-Material](projects-how-manage-project-supplies.md).</span><span class="sxs-lookup"><span data-stu-id="347a8-112">For more information, see [Manage Project Supplies](projects-how-manage-project-supplies.md).</span></span>

## <a name="to-create-multiple-job-sales-invoices"></a><span data-ttu-id="347a8-113">So erstellen Sie mehrere Projektverkaufsrechnungen</span><span class="sxs-lookup"><span data-stu-id="347a8-113">To create multiple job sales invoices</span></span>
<span data-ttu-id="347a8-114">Sie können eine Rechnung für ein Projekt oder für eine oder mehrere Projektunteraktivitäten für einen Debitor erstellen, wenn entweder die zu fakturierende Arbeit abgeschlossen ist oder das Datum für die Fakturierung basierend auf einem Fakturierungsplan erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="347a8-114">You can create an invoice for a job or for one or more job tasks for a customer when either the work to be invoiced is complete or the date for invoicing based on an invoicing schedule has been reached.</span></span>

<span data-ttu-id="347a8-115">Der folgende Ablauf zeigt, wie eine Stapelverarbeitung verwendet wird, um mehrere Projekte zu fakturieren.</span><span class="sxs-lookup"><span data-stu-id="347a8-115">The following procedure shows how to use a batch job to invoice multiple jobs.</span></span>  

1. <span data-ttu-id="347a8-116">Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun"), geben Sie **Job Verkaufsrechnung erstellen** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="347a8-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Create Sales Invoice**, and then choose the related link.</span></span>  
2. <span data-ttu-id="347a8-117">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="347a8-117">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="347a8-118">Legt Filter fest, wenn Sie die Projekte einschränken möchten, die die Stapelverarbeitung verarbeiten soll.</span><span class="sxs-lookup"><span data-stu-id="347a8-118">Set filters if you want to limit the jobs that the batch job will process.</span></span>
4. <span data-ttu-id="347a8-119">Wählen Sie die Schaltfläche **OK**, um die Rechnung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="347a8-119">Choose the **OK** button to create the invoices.</span></span>  

<span data-ttu-id="347a8-120">Sie können erstellte Rechnungen im Fenster **Verkaufsrechnungen** überprüfen und buchen.</span><span class="sxs-lookup"><span data-stu-id="347a8-120">You can review and post created invoices in the **Sales Invoices** window.</span></span>

> [!NOTE]
> <span data-ttu-id="347a8-121">Alternativ können Sie einen Debitor fakturieren, indem Sie das Projekt auswählen und anschließend die Aktion **Projektverkaufsrechnung erstellen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="347a8-121">Alternatively, invoice a customer by selecting the job, and then choosing the **Create Job Sales Invoice** action.</span></span> 

## <a name="to-create-and-post-job-sales-invoice-from-job-planning-lines"></a><span data-ttu-id="347a8-122">So erstellen und buchen Sie eine Projektverkaufsrechnung aus Projektplanzeilen</span><span class="sxs-lookup"><span data-stu-id="347a8-122">To create and post job sales invoice from job planning lines</span></span>
<span data-ttu-id="347a8-123">Sie können eine Rechnung aus Projektplanungszeilen erstellen, und dabei die Menge des Artikels, der Ressource oder des Sachkontos angeben, die Sie fakturieren möchten.</span><span class="sxs-lookup"><span data-stu-id="347a8-123">You can create an invoice from a job planning lines, and indicate at that time the quantity of the item, resource, or general ledger account that you want to invoice.</span></span>

1. <span data-ttu-id="347a8-124">Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten"), geben Sie **Projekte** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="347a8-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="347a8-125">Öffnen Sie eine relevante Jobkarte.</span><span class="sxs-lookup"><span data-stu-id="347a8-125">Open a relevant job.</span></span>
3. <span data-ttu-id="347a8-126">Wählen Sie eine Projektaufgabe aus, deren Wert für das Feld **Projektaufgabenart** **Buchen** enthält und klicken Sie anschließend auf die Aktion **Projektplanzeilen**.</span><span class="sxs-lookup"><span data-stu-id="347a8-126">Select a job task for which the **Job Task Type** field contains **Posting**, and then choose the **Job Planning Lines** action.</span></span>  
4. <span data-ttu-id="347a8-127">In einer Projektplanungszeile im Feld **In Rechnung zu übertragende Menge** geben Sie die Menge des Artikels, der Ressource, Sachkontoart ein, die fakturiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="347a8-127">On a job planning line, in the **Qty. To Transfer to Invoice** field, enter the quantity of the item, resource, general ledger account type that you want to invoice.</span></span>  
5. <span data-ttu-id="347a8-128">Wählen Sie die Aktion **Verkaufsrechnung erstellen**.</span><span class="sxs-lookup"><span data-stu-id="347a8-128">Choose the **Create Sales Invoice** action.</span></span>
6. <span data-ttu-id="347a8-129">Auf der Seite **Projekt-Verkaufsrechnung erstellen** geben Sie das Buchungsdatum an und ob Sie eine neue Rechnung erstellen oder diese Rechnung einer bestehenden Rechnung hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="347a8-129">On the **Job Create Sales Invoice** page, enter the posting date and whether you want to create a new invoice or append this invoice to an existing one.</span></span>
7. <span data-ttu-id="347a8-130">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="347a8-130">Choose the **OK** button.</span></span>  
8. <span data-ttu-id="347a8-131">Auf der Seite **Projektplanungszeilen** wählen Sie Die Aktion **Verkaufsrechnungen/Gutschrift** aus.</span><span class="sxs-lookup"><span data-stu-id="347a8-131">On the **Job Planning Lines** page, choose the **Sales Invoices/Credit Memos** action.</span></span>

    <span data-ttu-id="347a8-132">Die Seite **Verkaufsrechnung** wird geöffnet und zeigt die Menge an, die Sie zum Fakturieren in die Rechnung übertragen haben.</span><span class="sxs-lookup"><span data-stu-id="347a8-132">The **Sales Invoice** page opens, showing the quantity that you have transferred to the invoice.</span></span>
9. <span data-ttu-id="347a8-133">Nehmen Sie die zusätzlichen Änderungen vor, und wählen Sie dann die Aktion **Buchen**.</span><span class="sxs-lookup"><span data-stu-id="347a8-133">Make any additional changes, and then choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="347a8-134">Das obige Verfahren dient zum Erstellen, Prüfen und Buchen einer projektbezogenen Verkaufsgutschrift.</span><span class="sxs-lookup"><span data-stu-id="347a8-134">The above procedure is similar for creating, reviewing, and posting a job-related sales credit memo.</span></span>


## <a name="see-also"></a><span data-ttu-id="347a8-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="347a8-135">See Also</span></span>
[<span data-ttu-id="347a8-136">Projekte verwalten</span><span class="sxs-lookup"><span data-stu-id="347a8-136">Managing Projects</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="347a8-137">Finanzen</span><span class="sxs-lookup"><span data-stu-id="347a8-137">Finance</span></span>](finance.md)  
<span data-ttu-id="347a8-138">[Einkauf](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="347a8-138">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="347a8-139">[Verkauf](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="347a8-139">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="347a8-140">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="347a8-140">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]
