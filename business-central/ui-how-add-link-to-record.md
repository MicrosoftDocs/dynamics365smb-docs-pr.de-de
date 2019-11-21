---
title: Anhänge, Links und Notizen zu Datensätzen hinzufügen| Microsoft Docs
description: Fügen Sie einem Dokument oder einer Website einen Link zu einem bestimmten Datensatz hinzu, beispielsweise zu einer Debitorenkarte oder einem Dokument.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/21/2019
ms.author: sgroespe
ms.openlocfilehash: 88e6a04a8e4a992b6a5df3fee87104eba7b5510e
ms.sourcegitcommit: be1e2c49a8434d3f440d5a201508af9c3c8cc87f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/22/2019
ms.locfileid: "2649788"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a><span data-ttu-id="4f841-103">Verwalten von Anhängen, Links und Notizen zu Karten und Dokumenten</span><span class="sxs-lookup"><span data-stu-id="4f841-103">Manage Attachments, Links, and Notes on Cards and Documents</span></span>

<span data-ttu-id="4f841-104">In der Infobox der meisten Karten und Dokumente können Sie Dateien anhängen, Links hinzufügen und Notizen schreiben.</span><span class="sxs-lookup"><span data-stu-id="4f841-104">In the FactBox on most cards and documents, you can attach files, add links, and write notes.</span></span> <span data-ttu-id="4f841-105">Bei Links und Notizen können Sie dies auch auf der Listenseite tun, indem Sie zuerst die entsprechende Zeile auswählen.</span><span class="sxs-lookup"><span data-stu-id="4f841-105">For links and notes, you can also do this on the list page by first selecting the related line.</span></span>

<span data-ttu-id="4f841-106">Um einen dieser angehängten Informationstypen anzuzeigen oder zu ändern, müssen Sie zuerst die Registerkarte **Anhänge** in der Infobox öffnen.</span><span class="sxs-lookup"><span data-stu-id="4f841-106">To view or change any of these attached information types, you must first open the **Attachments** tab in the FactBox.</span></span> <span data-ttu-id="4f841-107">Die Zahl hinter dem Titel der Registerkarte gibt an, wie viele angehängte Dateien, Links oder Notizen für die Karte oder das Dokument vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="4f841-107">The number behind the tab title indicates how many attached files, links, or notes exist for the card or document.</span></span>

<span data-ttu-id="4f841-108">Anhänge, Links und Notizen bleiben angehängt, wenn die Karte oder das Dokument in einen anderen Status verarbeitet wird, z. B. von einem laufenden Kundenauftrag zu einer gebuchten Kundenrechnung.</span><span class="sxs-lookup"><span data-stu-id="4f841-108">Attachments, links, and notes stay attached as the card or document is processed into other states, such as from an ongoing sales order to a posted sales invoice.</span></span> <span data-ttu-id="4f841-109">Beachten Sie jedoch, dass keiner der Anhangstypen vom System ausgegeben wird, z. B. beim Drucken oder beim Speichern in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="4f841-109">Note, however, that none of the attachment types are output from the system, for example, when printing or when saving to a file.</span></span>

## <a name="to-attach-a-file-to-a-purchase-invoice"></a><span data-ttu-id="4f841-110">So hängen Sie eine Datei an eine Eikaufsrechnung an</span><span class="sxs-lookup"><span data-stu-id="4f841-110">To attach a file to a purchase invoice</span></span>
<span data-ttu-id="4f841-111">Sie können jede Art von Datei, die Text, Bilder oder Videos enthält, an eine Karte oder ein Dokument anhängen.</span><span class="sxs-lookup"><span data-stu-id="4f841-111">You can attach any type of file, containing text, image, or video, to a card or document.</span></span> <span data-ttu-id="4f841-112">Dies ist beispielsweise nützlich, wenn Sie eine Lieferantenrechnung als PDF-Datei auf der zugehörigen Einkaufsrechnung in [!INCLUDE[d365fin](includes/d365fin_md.md)] speichern möchten.</span><span class="sxs-lookup"><span data-stu-id="4f841-112">This is useful, for example, when you want to store a vendor's invoice as a PDF file on the related purchase invoice in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

> [!NOTE]
> <span data-ttu-id="4f841-113">Dateien, die mit der Funktion Eingehende Belege angehängt sind, werden auf der Registerkarte **Anhänge** nicht eingeschlossen. Weitere Informationen finden Sie unter [Eingehende Belege](across-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="4f841-113">Files attached with the Incoming Documents feature are not included on the **Attachments** tab. For more information, see [Incoming Documents](across-income-documents.md).</span></span>

<span data-ttu-id="4f841-114">Das folgende Verfahren basiert auf einer Auftragsabwicklung.</span><span class="sxs-lookup"><span data-stu-id="4f841-114">The following procedure is based on a sales order.</span></span> <span data-ttu-id="4f841-115">Die Schritte sind für alle anderen unterstützten Belege und Karten ähnlich.</span><span class="sxs-lookup"><span data-stu-id="4f841-115">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="4f841-116">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Kaufrechnungen** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="4f841-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="4f841-117">Öffnen Sie den Verkaufsauftrag, den Sie einer Datei zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="4f841-117">Open the sales order that you want to attach a file to.</span></span>
3. <span data-ttu-id="4f841-118">Öffnen Sie in der Infobox die Registerkarte **Anhänge**.</span><span class="sxs-lookup"><span data-stu-id="4f841-118">In the FactBox, open the **Attachments** tab.</span></span>
4. <span data-ttu-id="4f841-119">Wählen Sie den Wert hinter dem Feld **Belege** z. B. "0".</span><span class="sxs-lookup"><span data-stu-id="4f841-119">Choose the value behind the **Documents** field, such as "0".</span></span>
5. <span data-ttu-id="4f841-120">Auf der Seite **Beleg anfügen** im Feld **Dateianhang**, wählen Sie die Schaltfläche **Wählen Sie die Datei aus** aus.</span><span class="sxs-lookup"><span data-stu-id="4f841-120">On the **Attached Documents** page, in the **Attachment** field, choose the **Select File** button.</span></span>
5. <span data-ttu-id="4f841-121">Wählen Sie eine Datei aus jedem Lagerort, und wählen Sie dann die Schaltfläche **Öffnen** aus.</span><span class="sxs-lookup"><span data-stu-id="4f841-121">Select a file from any location, and then choose the **Open** button.</span></span>

<span data-ttu-id="4f841-122">Die Datei wird nun der Einkaufsrechnung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="4f841-122">The file is now attached to the purchase invoice.</span></span>

## <a name="to-add-a-link-from-an-item-card"></a><span data-ttu-id="4f841-123">Um einen Link von einer Artikelkarte hinzuzufügen</span><span class="sxs-lookup"><span data-stu-id="4f841-123">To add a link from an item card</span></span>
<span data-ttu-id="4f841-124">Sie können jeder URL oder jedem Pfad einen Link von einer Karte oder einem Dokument hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4f841-124">You can add a link from a card or document to any URL or path.</span></span> <span data-ttu-id="4f841-125">Dies ist beispielsweise hilfreich, wenn Sie eine Artikelkarte mit dem Artikelkatalog des Lieferanten verknüpfen möchten.</span><span class="sxs-lookup"><span data-stu-id="4f841-125">This is useful, for example, when you want to link an item card with the supplier's item catalog.</span></span>

<span data-ttu-id="4f841-126">Das folgende Verfahren basiert auf einer Elementkarte.</span><span class="sxs-lookup"><span data-stu-id="4f841-126">The following procedure is based on an item card.</span></span> <span data-ttu-id="4f841-127">Die Schritte sind für alle anderen unterstützten Belege und Karten gleich.</span><span class="sxs-lookup"><span data-stu-id="4f841-127">The steps are similar for all other supported cards and documents.</span></span>

1. <span data-ttu-id="4f841-128">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Elemente** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="4f841-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="4f841-129">Wählen Sie das Element aus, zu dem Sie einen Link hinzufügen möchten, und wählen Sie dann die Registerkarte **Anhänge** in der Infobox.</span><span class="sxs-lookup"><span data-stu-id="4f841-129">Select the item that you want to add a link from, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="4f841-130">In dem **Link**, wählen Sie das **+** Symbol.</span><span class="sxs-lookup"><span data-stu-id="4f841-130">In the **Links**, choose the **+** icon.</span></span>
4. <span data-ttu-id="4f841-131">Geben Sie im Feld **Link Adresse** den Link ein.</span><span class="sxs-lookup"><span data-stu-id="4f841-131">In the **Link Address** field, enter the link.</span></span>

    <span data-ttu-id="4f841-132">Der Link muss eine gültige Internet- oder Intranet-URL sein.</span><span class="sxs-lookup"><span data-stu-id="4f841-132">The link must be a valid internet or intranet URL.</span></span>

5. <span data-ttu-id="4f841-133">Geben Sie im Feld **Beschreibung** die Informationen zu dem Link ein.</span><span class="sxs-lookup"><span data-stu-id="4f841-133">In the **Description** field, enter any information about the link.</span></span>  
6. <span data-ttu-id="4f841-134">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="4f841-134">Choose the **OK** button.</span></span>

<span data-ttu-id="4f841-135">Der Link ist jetzt an die Artikel-Karte angehängt.</span><span class="sxs-lookup"><span data-stu-id="4f841-135">The link is now attached to the item card.</span></span>  

## <a name="to-write-a-note-on-a-sales-order"></a><span data-ttu-id="4f841-136">So schreiben Sie eine Notiz zu einem Verkaufsauftrag</span><span class="sxs-lookup"><span data-stu-id="4f841-136">To write a note on a sales order</span></span>
<span data-ttu-id="4f841-137">Sie können eine Notiz auf ein Dokument oder eine Karte schreiben, um beispielsweise anderen Benutzern des Dokuments oder der Karte spezielle Anweisungen zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="4f841-137">You can write a note on a document or card, for example, to communicate special instructions to other users of the document or card.</span></span> <span data-ttu-id="4f841-138">Sie können Dateilinks und URLs in Notizen einfügen.</span><span class="sxs-lookup"><span data-stu-id="4f841-138">You can include file links and URLs in notes.</span></span>

> [!NOTE]
> <span data-ttu-id="4f841-139">Hinweise auf der Registerkarte **Anhänge** haben nichts mit der internen Notizfunktion zu tun, die hauptsächlich für die Kommunikation zwischen Workflowbenutzern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4f841-139">Notes on the **Attachments** tab are not related to internal notes functionality, which is mainly used to communicate between workflow users.</span></span> <span data-ttu-id="4f841-140">Weitere Informationen finden Sie unter [Einrichten von Workflowbenachrichtigungen](across-setting-up-workflow-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="4f841-140">For more information, see [Setting Up Workflow Notifications](across-setting-up-workflow-notifications.md).</span></span>

<span data-ttu-id="4f841-141">Das folgende Verfahren basiert auf einer Auftragsabwicklung.</span><span class="sxs-lookup"><span data-stu-id="4f841-141">The following procedure is based on a sales order.</span></span> <span data-ttu-id="4f841-142">Die Schritte sind für alle anderen unterstützten Dokumente und Karten ähnlich.</span><span class="sxs-lookup"><span data-stu-id="4f841-142">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="4f841-143">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Verkaufsaufträge** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="4f841-143">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="4f841-144">Wählen Sie den Verkaufsauftrag aus, zu dem Sie einen Link hinzufügen möchten, und wählen Sie dann die Registerkarte **Anhänge** in der Infobox.</span><span class="sxs-lookup"><span data-stu-id="4f841-144">Select the sales order that you want to write a note on, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="4f841-145">In dem Abschnitt **Notizen** wählen Sie das **+** Symbol.</span><span class="sxs-lookup"><span data-stu-id="4f841-145">In the **Notes** section, choose the **+** icon.</span></span>
4. <span data-ttu-id="4f841-146">In dem Feld **Hinweis** geben Sie in das Feld einen beliebigen Text ein, z. B. "Dies ist eine dringende Bestellung.".</span><span class="sxs-lookup"><span data-stu-id="4f841-146">In the **Note** field, write any text, such as "This is an urgent order.".</span></span>
5. <span data-ttu-id="4f841-147">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="4f841-147">Choose the **OK** button.</span></span>

<span data-ttu-id="4f841-148">Der Hinweis ist jetzt dem Verkaufsauftrag beigefügt.</span><span class="sxs-lookup"><span data-stu-id="4f841-148">The note is now attached to the sales order.</span></span>

## <a name="see-also"></a><span data-ttu-id="4f841-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f841-149">See Also</span></span>  
<span data-ttu-id="4f841-150">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4f841-150">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="4f841-151">Eingehende Belege</span><span class="sxs-lookup"><span data-stu-id="4f841-151">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="4f841-152">Einrichten von Workflowbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="4f841-152">Setting Up Workflow Notifications</span></span>](across-setting-up-workflow-notifications.md)  
