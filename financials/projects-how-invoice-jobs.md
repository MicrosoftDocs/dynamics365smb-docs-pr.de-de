---
title: Erstellen Sie eine Projekt-Verkaufsrechnung, um ein Projekt zu fakturieren| Microsoft Docs
description: "Beschreibt, wie Kunden für Jobausgaben als Jobfortschritt Rechnung gestellt wird."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4c00ce50f70cbae3ad0557f0703e80f6b115995a
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="invoice-jobs"></a><span data-ttu-id="24ac4-103">Fakturieren von Projekten</span><span class="sxs-lookup"><span data-stu-id="24ac4-103">Invoice Jobs</span></span>
<span data-ttu-id="24ac4-104">Im Laufe des Projekts können Projektkosten wie Ressourcenverbrauch, Material oder projektbezogene Einkäufe anfallen.</span><span class="sxs-lookup"><span data-stu-id="24ac4-104">During the project, job costs from resource usage, materials, and job-related purchases can accumulate.</span></span> <span data-ttu-id="24ac4-105">Diese Transaktionen werden im weiteren Verlauf des Projekts auf das Projekt Buch.-Blatt gebucht.</span><span class="sxs-lookup"><span data-stu-id="24ac4-105">As the job progresses, these transactions get posted to the job journal.</span></span> <span data-ttu-id="24ac4-106">Dabei ist es wichtig, dass alle Kosten im Projekt Buch.-Blatt erfasst werden, bevor die Rechnung an den Debitor erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="24ac4-106">It is important that all costs get recorded in the job journal before you invoice the customer.</span></span>

<span data-ttu-id="24ac4-107">Sie können das gesamte Projekt im Fenster **Projektaufgabenzeilen** fakturieren, oder Sie fakturieren lediglich ausgewählte Vertragszeilen im Fenster **Projektplanzeilen**.</span><span class="sxs-lookup"><span data-stu-id="24ac4-107">You can invoice the whole job from the **Job Task Lines** window or only invoice selected billable lines from the **Planning Lines** window.</span></span> <span data-ttu-id="24ac4-108">Die Fakturierung kann erfolgen, wenn das Projekt abgeschlossen ist, oder in bestimmten Intervallen während der Projektlaufzeit gemäß eines Fakturierungsplans.</span><span class="sxs-lookup"><span data-stu-id="24ac4-108">Invoicing can be done after the job is finished or at certain intervals during the job's progress based on an invoicing schedule.</span></span>

> [!NOTE]  
>   <span data-ttu-id="24ac4-109">Wenn Sie **Verrechenbar** im Feld **Projekt-Zeilenart** auf den Verkaufsbelegen für projektbezogene Einkäufe auswählen, werden Projektplanzeilen, die bereit sind, an den Kunden zu fakturieren, erstellt.</span><span class="sxs-lookup"><span data-stu-id="24ac4-109">If you select **Billable** in the **Job Line Type** field on the purchase documents for job-related purchases, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="24ac4-110">Weitere Informationen finden Sie unter [Verwalten von Projekt-Material](projects-how-manage-project-supplies.md).</span><span class="sxs-lookup"><span data-stu-id="24ac4-110">For more information, see [Manage Project Supplies](projects-how-manage-project-supplies.md).</span></span>

## <a name="to-create-and-post-a-job-sales-invoice"></a><span data-ttu-id="24ac4-111">Verkaufsrechnung für ein Projekt erstellen und buchen</span><span class="sxs-lookup"><span data-stu-id="24ac4-111">To create and post a job sales invoice</span></span>
<span data-ttu-id="24ac4-112">Sie können eine Rechnung für ein Projekt oder für eine oder mehrere Projektunteraktivitäten für einen Debitor erstellen, wenn entweder die zu fakturierende Arbeit abgeschlossen ist oder das Datum für die Fakturierung basierend auf einem Fakturierungsplan erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="24ac4-112">You can create an invoice for a job or for one or more job tasks for a customer when either the work to be invoiced is complete or the date for invoicing based on an invoicing schedule has been reached.</span></span>

<span data-ttu-id="24ac4-113">Vom Fenster **Projekte** können Sie keinen Debitor fakturieren, indem Sie das Projekt auswählen, und dann die Aktion **Projekt-Verkaufsrechnung erstellen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="24ac4-113">From the **Jobs** window, you can invoice a customer by selecting the job, and then choosing the **Create Job Sales Invoice** action.</span></span> <span data-ttu-id="24ac4-114">Der folgende Ablauf zeigt, wie eine Stapelverarbeitung verwendet wird, um mehrere Projekte zu fakturieren.</span><span class="sxs-lookup"><span data-stu-id="24ac4-114">The following procedure shows how to use a batch job to invoice multiple jobs.</span></span>  

1. <span data-ttu-id="24ac4-115">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Projektverkaufsrechnungen** erstellen ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="24ac4-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Job Create Sales Invoice**, and then choose the related link.</span></span>  
2. <span data-ttu-id="24ac4-116">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="24ac4-116">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="24ac4-117">Legt Filter fest, wenn Sie die Projekte einschränken möchten, die die Stapelverarbeitung verarbeiten soll.</span><span class="sxs-lookup"><span data-stu-id="24ac4-117">Set filters if you want to limit the jobs that the batch job will process.</span></span>
4. <span data-ttu-id="24ac4-118">Wählen Sie die Schaltfläche **OK**, um die Rechnung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="24ac4-118">Choose the **OK** button to create the invoices.</span></span>  

## <a name="to-create-multiple-job-sales-invoices-from-job-planning-lines"></a><span data-ttu-id="24ac4-119">Mehrere Projektverkaufsrechnungen aus Projektplanungszeilen erstellen</span><span class="sxs-lookup"><span data-stu-id="24ac4-119">To create multiple job sales invoices from job planning lines</span></span>
<span data-ttu-id="24ac4-120">Sie können eine Rechnung aus Projektplanungszeilen erstellen, und dabei die Menge des Artikels, der Ressource oder des Sachkontos angeben, die Sie fakturieren möchten.</span><span class="sxs-lookup"><span data-stu-id="24ac4-120">You can create an invoice from a job planning lines, and indicate at that time the quantity of the item, resource, or general ledger account that you want to invoice.</span></span>

1. <span data-ttu-id="24ac4-121">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Projekt** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="24ac4-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="24ac4-122">Ein relevantes Projekt öffnen.</span><span class="sxs-lookup"><span data-stu-id="24ac4-122">Open a relevant job.</span></span>
3. <span data-ttu-id="24ac4-123">Wählen Sie eine Projektaufgabe aus, deren Wert für das Feld **Projektaufgabenart** **Buchen** enthält und klicken Sie anschließend auf die Aktion **Projektplanzeilen**.</span><span class="sxs-lookup"><span data-stu-id="24ac4-123">Select a job task for which the **Job Task Type** field contains **Posting**, and then choose the **Job Planning Lines** action.</span></span>  
4. <span data-ttu-id="24ac4-124">In einer Projektplanungszeile im Feld **In Rechnung zu übertragende Menge** geben Sie die Menge des Artikels, der Ressource, Sachkontoart ein, die fakturiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="24ac4-124">On a job planning line, in the **Qty. To Transfer to Invoice** field, enter the quantity of the item, resource, general ledger account type that you want to invoice.</span></span>  
5. <span data-ttu-id="24ac4-125">Wählen Sie die Aktion **Verkaufsrechnung erstellen**.</span><span class="sxs-lookup"><span data-stu-id="24ac4-125">Choose the **Create Sales Invoice** action.</span></span>
6. <span data-ttu-id="24ac4-126">Im Fenster **Projekt-Verkaufsrechnung erstellen** geben Sie das Buchungsdatum an und ob Sie eine neue Rechnung erstellen oder diese Rechnung einer bestehenden Rechnung hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="24ac4-126">In the **Job Create Sales Invoice** window, enter the posting date and whether you want to create a new invoice or append this invoice to an existing one.</span></span>
7. <span data-ttu-id="24ac4-127">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="24ac4-127">Choose the **OK** button.</span></span>  

    <span data-ttu-id="24ac4-128">In der Projektplanungszeile im Feld **In Rechnung übertragene Menge** können Sie die Menge anzeigen.</span><span class="sxs-lookup"><span data-stu-id="24ac4-128">On the job planning line, in the **Qty. Transferred to Invoice** field, you can see the quantity.</span></span>
8. <span data-ttu-id="24ac4-129">Im Fenster **Projektplanungszeilen** wählen Sie Die Aktion **Verkaufsrechnungen/Gutschrift** aus.</span><span class="sxs-lookup"><span data-stu-id="24ac4-129">In the **Job Planning Lines** window, choose the **Sales Invoices/Credit Memos** action.</span></span>

    <span data-ttu-id="24ac4-130">Das Fenster **Verkaufsrechnung** wird geöffnet und zeigt die Menge an, die Sie zum Fakturieren in die Rechnung übertragen haben.</span><span class="sxs-lookup"><span data-stu-id="24ac4-130">The **Sales Invoice** window opens, showing the quantity that you have transferred to the invoice.</span></span>  
9. <span data-ttu-id="24ac4-131">Nehmen Sie die zusätzlichen Änderungen vor, und wählen Sie dann die Aktion **Buchen**.</span><span class="sxs-lookup"><span data-stu-id="24ac4-131">Make any additional changes, and then choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="24ac4-132">Das obige Verfahren dient zum Erstellen, Prüfen und Buchen einer projektbezogenen Verkaufsgutschrift.</span><span class="sxs-lookup"><span data-stu-id="24ac4-132">The above procedure is similar for creating, reviewing, and posting a job-related sales credit memo.</span></span>

## <a name="to-calculate-and-post-job-completion-entries"></a><span data-ttu-id="24ac4-133">Berechnen und Buchen von Projekt-Abschlussposten</span><span class="sxs-lookup"><span data-stu-id="24ac4-133">To calculate and post job completion entries</span></span>
<span data-ttu-id="24ac4-134">Nachdem alle Aktivitäten für ein Projekt – einschließlich Buchung des Verbrauchs und Fakturierung – abgeschlossen wurden, muss das Projekt aktualisiert werden, damit es den **Status** **Abgeschlossen** erhält.</span><span class="sxs-lookup"><span data-stu-id="24ac4-134">When you have completed all activities for a job, including usage posting and invoicing, you must update the job to have a **Status** of **Completed**.</span></span> <span data-ttu-id="24ac4-135">Dann stornieren Sie alle WIPs, die in der Finanzbuchhaltung gebucht wurde.</span><span class="sxs-lookup"><span data-stu-id="24ac4-135">Then, you must reverse any WIP that has been posted to the general ledger.</span></span>

1. <span data-ttu-id="24ac4-136">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Projekt** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="24ac4-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="24ac4-137">Wählen Sie ein offenes Projekte und wählen Sie dann die Aktion **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="24ac4-137">Select an open job, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="24ac4-138">Wählen Sie im Feld **Status** **Abgeschlossen**.</span><span class="sxs-lookup"><span data-stu-id="24ac4-138">In the **Status** field, select **Completed**.</span></span>
4. <span data-ttu-id="24ac4-139">Folgen Sie den Hilfeschritten, um WIP zu berechnen und zu buchen.</span><span class="sxs-lookup"><span data-stu-id="24ac4-139">Follow the assistance steps to calculate and post WIP.</span></span> <span data-ttu-id="24ac4-140">Alternativ folgen Sie den Schritten 5 und 6, um dies manuell zu tun.</span><span class="sxs-lookup"><span data-stu-id="24ac4-140">Alternatively, follows steps 5 and 6 to do so manually.</span></span>  
5. <span data-ttu-id="24ac4-141">Wählen Sie die Aktion **WIP berechnen** aus.</span><span class="sxs-lookup"><span data-stu-id="24ac4-141">Choose the **Calculate WIP** action.</span></span>
6. <span data-ttu-id="24ac4-142">Geben Sie im Fenster **WIP für Projekt berechnen** die notwendigen Felder ein.</span><span class="sxs-lookup"><span data-stu-id="24ac4-142">In the **Job Calculate WIP** window, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="24ac4-143">Die WIP-Projektposten, die beim Ausführen der Stapelverarbeitung erstellt wurden, weisen nun ein Häkchen im Feld **Auftrag abgeschlossen** auf, um anzugeben, dass es sich hierbei um Abschlussposten handelt.</span><span class="sxs-lookup"><span data-stu-id="24ac4-143">The job WIP entries created by running the batch job will have the **Job Complete** check box selected to show that they are completion entries.</span></span>  
7. <span data-ttu-id="24ac4-144">Wählen Sie die Aktion **WIP nach Sachkonten Projekt** aus.</span><span class="sxs-lookup"><span data-stu-id="24ac4-144">Choose the **Job Post WIP to G/L** action.</span></span>
8. <span data-ttu-id="24ac4-145">Füllen Sie im Fenster **WIP nach Sachkonten Projekt buchen** aus und füllen Sie die Felder wie erforderlich aus.</span><span class="sxs-lookup"><span data-stu-id="24ac4-145">In the **Job Post WIP to G/L** window, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="24ac4-146">Die WIP-Hauptbuchungsposten, die beim Ausführen der Stapelverarbeitung erstellt wurden, weisen nun ein Häkchen im Feld **Auftrag abgeschlossen** auf, um anzugeben, dass es sich hierbei um Abschlussposten handelt.</span><span class="sxs-lookup"><span data-stu-id="24ac4-146">The job WIP general ledger entries created by running the batch job will have the **Job Complete** check box selected to show they are completion entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="24ac4-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24ac4-147">See Also</span></span>
[<span data-ttu-id="24ac4-148">Projekte verwalten</span><span class="sxs-lookup"><span data-stu-id="24ac4-148">Managing Projects</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="24ac4-149">Finanzen</span><span class="sxs-lookup"><span data-stu-id="24ac4-149">Finance</span></span>](finance.md)  
<span data-ttu-id="24ac4-150">[Einkauf](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="24ac4-150">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="24ac4-151">[Verkauf](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="24ac4-151">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="24ac4-152">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="24ac4-152">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

