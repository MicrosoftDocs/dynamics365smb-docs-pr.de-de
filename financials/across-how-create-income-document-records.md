---
title: Eingehende Dokumente aufzeichnen| Microsoft Docs
description: "Sie finden hier Datensätze aus eingehenden Belege, wie Erechnungen erstellen und verwalten OCRaufgaben, elektronische Geschäftsverkehr und Belegaustausch."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 8642f4d904c9a1e7c46846d790fcb2d0837c4cc2
ms.contentlocale: de-de
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-create-incoming-document-records"></a><span data-ttu-id="7021a-103">Vorgehensweise: Erstellen von Eingangsbelegen</span><span class="sxs-lookup"><span data-stu-id="7021a-103">How to: Create Incoming Document Records</span></span>
<span data-ttu-id="7021a-104">Im Fenster **Eingehende Dokumente** können Sie verschiedene Funktionen zum Überprüfen von Ausgabenbelegen, Verwalten von OCR-Aufgaben und Konvertieren eingehender Belege, manuell oder automatisch, in den entsprechenden Belegen oder Buch.-Blattzeilen verwenden.</span><span class="sxs-lookup"><span data-stu-id="7021a-104">In the **Incoming Documents** window, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="7021a-105">Die externen Dateien können jeder Prozessphase zugeordnet werden, auch gebuchten Belegen und den resultierenden Kreditoren-, Debitoren- und Sachposten.</span><span class="sxs-lookup"><span data-stu-id="7021a-105">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span>

<span data-ttu-id="7021a-106">Um einen externen Beleg in [!INCLUDE[d365fin](includes/d365fin_md.md)] aufzuzeichnen, müssen Sie zuerst einen Datensatz des Eingangsbeleges anlegen oder ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="7021a-106">To record an external document in [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first create or complete an incoming document record.</span></span> <span data-ttu-id="7021a-107">Dies kann manuell erfolgen, oder Sie können ein Foto des externen Belegs machen und einen Eingangsbelegsdatensatz mit der angehängten Bilddatei erstellen.</span><span class="sxs-lookup"><span data-stu-id="7021a-107">You can do this manually, or you can take a photo of the external document and then create the incoming document record with the image file attached.</span></span>

<span data-ttu-id="7021a-108">Bevor Sie die Funktion für Eingangsbelege verwenden können, müssen Sie sie entsprechend einrichten.</span><span class="sxs-lookup"><span data-stu-id="7021a-108">Before you can use the Incoming Documents feature, you must perform the required setup.</span></span> <span data-ttu-id="7021a-109">Weitere Informationen finden Sie unter [So gehts: Einrichten von eingehenden Belegen](across-how-setup-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="7021a-109">For more information, see [How to: Set Up Incoming Documents](across-how-setup-income-documents.md).</span></span>

## <a name="to-approve-or-reject-an-incoming-document"></a><span data-ttu-id="7021a-110">So können Sie einen eingehenden Beleg genehmigen oder ablehnen</span><span class="sxs-lookup"><span data-stu-id="7021a-110">To approve or reject an incoming document</span></span>
<span data-ttu-id="7021a-111">Wenn Sie wünschen, dass Benutzer Rechnungen oder Hauptjournalzeilen aus Eingangsbelegen nur dann erstellen dürfen, wenn diese genehmigt sind, können Sie Genehmiger einrichten, die alle Belege genehmigen müssen, bevor sie verarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="7021a-111">If you do want to allow users to create invoices or general journal lines from incoming document records unless they are approved, you can set up approvers who must approve the records before they can be processed.</span></span>

1. <span data-ttu-id="7021a-112">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Gebuchte Einkaufsrechnungen** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="7021a-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Incoming Documents**, and then choose the related link.</span></span>
2. <span data-ttu-id="7021a-113">Wählen Sie die Zeile mit dem Beleg, den Sie genehmigen oder ablehnen möchten, und wählen Sie dann die Aktion **Genehmigen** oder **Ablehnen** aus.</span><span class="sxs-lookup"><span data-stu-id="7021a-113">Select the line with the document that you want to approve or reject, and then choose the **Approve** or **Reject** actions.</span></span>

<span data-ttu-id="7021a-114">Das Kontrollkästchen **Freigegeben** in der Zeile für den Eingangsbeleg ist aktiviert, wenn dieser genehmigt wurde.</span><span class="sxs-lookup"><span data-stu-id="7021a-114">If you approve the incoming document record, the **Released** check box on the incoming document line is selected.</span></span> <span data-ttu-id="7021a-115">Der jeweilige Benutzer, beispielsweise der für das Erstellen von Einkaufsrechnungen zuständige, kann dann fortfahren, den Datensatz zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="7021a-115">The user in charge of creating, for example, purchase invoices can proceed to process the record.</span></span>

## <a name="to-create-an-incoming-document-record-by-taking-a-photo"></a><span data-ttu-id="7021a-116">So erstellen Sie Eingangsbelegdatensätze indem Sie ein Foto machen</span><span class="sxs-lookup"><span data-stu-id="7021a-116">To create an incoming document record by taking a photo</span></span>
> [!NOTE]  
>   <span data-ttu-id="7021a-117">Der folgende Vorgang gilt nur für [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tablet- und Smartphone-Clients.</span><span class="sxs-lookup"><span data-stu-id="7021a-117">The following procedure only applies to the [!INCLUDE[d365fin](includes/d365fin_md.md)] Tablet and Phone clients.</span></span>

1. <span data-ttu-id="7021a-118">Wählen Sie auf der App-Leiste die Kachel **Erstellen von eingehendem Beleg von Kamera**, und wechseln Sie dann zu Schritt 4.</span><span class="sxs-lookup"><span data-stu-id="7021a-118">On the app bar, choose the **Create Incoming Document from Camera** tile, and then go to step 4.</span></span>
2. <span data-ttu-id="7021a-119">Wählen Sie alternativ in er Anwendungsleiste die Optionsschaltfläche aus, wählen Sie **Eingehende Belege** und wählen Sie dann **Alle** aus.</span><span class="sxs-lookup"><span data-stu-id="7021a-119">Alternatively, on the app bar, choose the options button, choose **Incoming Documents**, and then choose **All**.</span></span>
3. <span data-ttu-id="7021a-120">Verwenden Sie im Fenster **Eingehende Belege** die Auslassungspunkt-Schaltfläche, und wählen Sie dann **Von Kamera erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="7021a-120">In the **Incoming Documents** window, choose the ellipsis button, and then choose **Create from Camera**.</span></span> <span data-ttu-id="7021a-121">Die Kamera im Tablet oder dem Smartphone wird aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7021a-121">The camera on the tablet or phone is activated.</span></span>
4. <span data-ttu-id="7021a-122">Nehmen Sie ein Foto eines Belegs, wie einer Einkaufsquittung, die Sie als eingehender Beleg bearbeiten wollen, und wählen Sie dann die Schaltfläche **OK**.</span><span class="sxs-lookup"><span data-stu-id="7021a-122">Take a photo of a document, such as a purchase receipt, that you want to process as an incoming document, and then choose the **OK** button.</span></span>

    <span data-ttu-id="7021a-123">Ein neuer Datensatz für den eingehenden Beleg wird erstellt und das Bild wird angehängt.</span><span class="sxs-lookup"><span data-stu-id="7021a-123">A new incoming document record is created, with the image attached.</span></span>

## <a name="to-attach-an-image-to-an-incoming-document-record-by-taking-a-photo"></a><span data-ttu-id="7021a-124">So hängen Sie ein Bild an ein Eingangsbelegdatensatz an, indem Sie ein Foto machen</span><span class="sxs-lookup"><span data-stu-id="7021a-124">To attach an image to an incoming document record by taking a photo</span></span>
> [!NOTE]  
>   <span data-ttu-id="7021a-125">Der folgende Vorgang gilt nur für [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tablet- und Smartphone-Clients.</span><span class="sxs-lookup"><span data-stu-id="7021a-125">The following procedure only applies to the [!INCLUDE[d365fin](includes/d365fin_md.md)] Tablet and Phone clients.</span></span>

1. <span data-ttu-id="7021a-126">Wählen Sie auf der App-Leiste die Optionsschaltfläche aus, wählen Sie **Eingehende Belege** und wählen Sie dann **Alle** aus.</span><span class="sxs-lookup"><span data-stu-id="7021a-126">On the app bar, choose the options button, choose **Incoming Documents**, and then choose **All**.</span></span>
2. <span data-ttu-id="7021a-127">Öffnen Sie die Karte eines vorhandenen eingehenden Belegsdatensatzes.</span><span class="sxs-lookup"><span data-stu-id="7021a-127">Open the card for an existing incoming document record.</span></span>
3. <span data-ttu-id="7021a-128">Verwenden Sie im Fenster **Eingehende Belege** die Auslassungspunkt-Schaltfläche, und wählen Sie dann **Bild von Kamera anhängen** aus.</span><span class="sxs-lookup"><span data-stu-id="7021a-128">In the **Incoming Document** window, choose the ellipsis button, and then choose **Attach Image from Camera**.</span></span> <span data-ttu-id="7021a-129">Die Kamera im Tablet oder dem Smartphone wird aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7021a-129">The camera on the tablet or phone is activated.</span></span>
4. <span data-ttu-id="7021a-130">Nehmen Sie ein Foto eines Belegs, wie einer Einkaufsquittung, die Sie als eingehender Beleg bearbeiten wollen, und wählen Sie dann die Schaltfläche **OK**.</span><span class="sxs-lookup"><span data-stu-id="7021a-130">Take a photo of a document, such as a purchase receipt, that you want to process as an incoming document, and then choose the **OK** button.</span></span>

    <span data-ttu-id="7021a-131">Das Bild wurde dem Datensatz des eingehenden Beleges angehängt.</span><span class="sxs-lookup"><span data-stu-id="7021a-131">The image is attached to the incoming document record.</span></span>

## <a name="to-create-an-incoming-document-record-manually"></a><span data-ttu-id="7021a-132">Eingangsbelege manuell erstellen</span><span class="sxs-lookup"><span data-stu-id="7021a-132">To create an incoming document record manually</span></span>
1. <span data-ttu-id="7021a-133">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Gebuchte Einkaufsrechnungen** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="7021a-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Incoming Documents**, and then choose the related link.</span></span>
2. <span data-ttu-id="7021a-134">Wählen Sie die Aktion **Aus Datei erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="7021a-134">Choose the **Create from File** action.</span></span>  
3. <span data-ttu-id="7021a-135">Wählen Sie im Fenster **Datei einfügen** eine Datei aus und wählen Sie dann **Offen** aus.</span><span class="sxs-lookup"><span data-stu-id="7021a-135">In the **Insert File** window, select a file, and then choose **Open**.</span></span> <span data-ttu-id="7021a-136">Die Datei wird automatisch angehängt.</span><span class="sxs-lookup"><span data-stu-id="7021a-136">The file is automatically attached.</span></span>
4. <span data-ttu-id="7021a-137">Wählen Sie alternativ die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="7021a-137">Alternatively, choose the **New** action.</span></span>
5. <span data-ttu-id="7021a-138">Um eine Datei hinzuzufügen, wählen Sie die Aktion **Datei anhängen**.</span><span class="sxs-lookup"><span data-stu-id="7021a-138">To attach a file, choose the **Attach File** action.</span></span>
6. <span data-ttu-id="7021a-139">Im **Datei einfügen**-Fenster wählen Sie die Datei, die den jeweiligen Eingangsbeleg darstellt, und wählen Sie die Schaltfläche **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="7021a-139">In the **Insert File** window, select the file that represents the incoming document in question, and then choose the **Open** button.</span></span>
7. <span data-ttu-id="7021a-140">Füllen Sie im Fenster **Eingehende Belege** die Felder wie benötigt aus.</span><span class="sxs-lookup"><span data-stu-id="7021a-140">In the **Incoming Document** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><span data-ttu-id="7021a-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7021a-141">See Also</span></span>
[<span data-ttu-id="7021a-142">Eingehende Dokumente verarbeiten</span><span class="sxs-lookup"><span data-stu-id="7021a-142">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="7021a-143">Eingehende Belege</span><span class="sxs-lookup"><span data-stu-id="7021a-143">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="7021a-144">Einkauf</span><span class="sxs-lookup"><span data-stu-id="7021a-144">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="7021a-145">[Arbeiten mit [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7021a-145">[Working with [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>

