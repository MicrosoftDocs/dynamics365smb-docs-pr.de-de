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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 447012a66e75e1acf03f2aff1ba6b6922164312f
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3918563"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a><span data-ttu-id="57669-103">Verwalten von Anhängen, Links und Notizen zu Karten und Dokumenten</span><span class="sxs-lookup"><span data-stu-id="57669-103">Manage Attachments, Links, and Notes on Cards and Documents</span></span>

<span data-ttu-id="57669-104">In der Infobox der meisten Karten und Dokumente können Sie Dateien anhängen, Links hinzufügen und Notizen schreiben.</span><span class="sxs-lookup"><span data-stu-id="57669-104">In the FactBox on most cards and documents, you can attach files, add links, and write notes.</span></span> <span data-ttu-id="57669-105">Bei Links und Notizen können Sie dies auch auf der Listenseite tun, indem Sie zuerst die entsprechende Zeile auswählen.</span><span class="sxs-lookup"><span data-stu-id="57669-105">For links and notes, you can also do this on the list page by first selecting the related line.</span></span>

<span data-ttu-id="57669-106">Um einen dieser angehängten Informationstypen anzuzeigen oder zu ändern, müssen Sie zuerst die Registerkarte **Anhänge** in der Infobox öffnen.</span><span class="sxs-lookup"><span data-stu-id="57669-106">To view or change any of these attached information types, you must first open the **Attachments** tab in the FactBox.</span></span> <span data-ttu-id="57669-107">Die Zahl hinter dem Titel der Registerkarte gibt an, wie viele angehängte Dateien, Links oder Notizen für die Karte oder das Dokument vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="57669-107">The number behind the tab title indicates how many attached files, links, or notes exist for the card or document.</span></span>

<span data-ttu-id="57669-108">Anhänge, Links und Notizen bleiben angehängt, wenn die Karte oder das Dokument in einen anderen Status verarbeitet wird, z. B. von einem laufenden Kundenauftrag zu einer gebuchten Kundenrechnung.</span><span class="sxs-lookup"><span data-stu-id="57669-108">Attachments, links, and notes stay attached as the card or document is processed into other states, such as from an ongoing sales order to a posted sales invoice.</span></span> <span data-ttu-id="57669-109">Allerdings wird keiner der Anhangstypen vom System ausgegeben, z. B. beim Drucken oder beim Speichern in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="57669-109">However, none of the attachment types are output from the system, for example, when printing or when saving to a file.</span></span>

> [!NOTE]
> <span data-ttu-id="57669-110">Wenn Sie einen Verkaufsauftrag oder eine Einkaufsbestellung teilweise versenden und in Rechnung stellen, wird der Anhang nur der endgültigen Rechnung dieser Bestellung beigefügt.</span><span class="sxs-lookup"><span data-stu-id="57669-110">When you partially ship and invoice a sales order or purchase order, the attachment will only be attached to the final invoice of that order.</span></span> <span data-ttu-id="57669-111">Wenn Sie mit der Funktion „Abgrenzungen“ abrechnen, wird der Anhang entsprechend nur an die Sachkontenbucheinträge für den Beleg angehängt, nicht jedoch an die Abgrenzungseinträge.</span><span class="sxs-lookup"><span data-stu-id="57669-111">Likewise, when you invoice using the Deferrals feature, the attachment is only attached to the G/L entries for the document but not for the deferral entries.</span></span>

## <a name="to-attach-a-file-to-a-purchase-invoice"></a><span data-ttu-id="57669-112">So hängen Sie eine Datei an eine Eikaufsrechnung an</span><span class="sxs-lookup"><span data-stu-id="57669-112">To attach a file to a purchase invoice</span></span>
<span data-ttu-id="57669-113">Sie können jede Art von Datei, die Text, Bilder oder Videos enthält, an eine Karte oder ein Dokument anhängen.</span><span class="sxs-lookup"><span data-stu-id="57669-113">You can attach any type of file, containing text, image, or video, to a card or document.</span></span> <span data-ttu-id="57669-114">Dies ist beispielsweise nützlich, wenn Sie eine Lieferantenrechnung als PDF-Datei auf der zugehörigen Einkaufsrechnung in [!INCLUDE[d365fin](includes/d365fin_md.md)] speichern möchten.</span><span class="sxs-lookup"><span data-stu-id="57669-114">This is useful, for example, when you want to store a vendor's invoice as a PDF file on the related purchase invoice in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

> [!NOTE]
> <span data-ttu-id="57669-115">Dateien, die mit der Funktion Eingehende Belege angehängt sind, werden auf der Registerkarte **Anhänge** nicht eingeschlossen. Weitere Informationen finden Sie unter [Eingehende Belege](across-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="57669-115">Files attached with the Incoming Documents feature are not included on the **Attachments** tab. For more information, see [Incoming Documents](across-income-documents.md).</span></span>

<span data-ttu-id="57669-116">Das folgende Verfahren basiert auf einer Einkaufsrechnung.</span><span class="sxs-lookup"><span data-stu-id="57669-116">The following procedure is based on a purchase invoice.</span></span> <span data-ttu-id="57669-117">Die Schritte sind für alle anderen unterstützten Dokumente und Karten ähnlich.</span><span class="sxs-lookup"><span data-stu-id="57669-117">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="57669-118">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Kaufrechnungen** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="57669-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices** , and then choose the related link.</span></span>
2. <span data-ttu-id="57669-119">Öffnen Sie den Verkaufsauftrag, den Sie einer Datei zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="57669-119">Open the sales order that you want to attach a file to.</span></span>
3. <span data-ttu-id="57669-120">Öffnen Sie in der Infobox die Registerkarte **Anhänge** .</span><span class="sxs-lookup"><span data-stu-id="57669-120">In the FactBox, open the **Attachments** tab.</span></span>
4. <span data-ttu-id="57669-121">Wählen Sie den Wert hinter dem Feld **Belege** z. B. "0".</span><span class="sxs-lookup"><span data-stu-id="57669-121">Choose the value behind the **Documents** field, such as "0".</span></span>
5. <span data-ttu-id="57669-122">Wählen Sie auf der Seite **Angefügte Dokumente** im Feld **Anhang** die Aktion **Datei auswählen** aus.</span><span class="sxs-lookup"><span data-stu-id="57669-122">On the **Attached Documents** page, in the **Attachment** field, choose the **Select File** action.</span></span>
5. <span data-ttu-id="57669-123">Wählen Sie eine Datei aus jedem Lagerort, und wählen Sie dann die Schaltfläche **Öffnen** aus.</span><span class="sxs-lookup"><span data-stu-id="57669-123">Select a file from any location, and then choose the **Open** button.</span></span>

<span data-ttu-id="57669-124">Die Datei wird nun der Einkaufsrechnung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="57669-124">The file is now attached to the purchase invoice.</span></span>

## <a name="to-view-an-attached-file"></a><span data-ttu-id="57669-125">So zeigen Sie eine angehängte Datei an</span><span class="sxs-lookup"><span data-stu-id="57669-125">To view an attached file</span></span>
1. <span data-ttu-id="57669-126">Öffnen Sie in der Infobox die Registerkarte **Anhänge** .</span><span class="sxs-lookup"><span data-stu-id="57669-126">In the FactBox, open the **Attachments** tab.</span></span>
2. <span data-ttu-id="57669-127">Wählen Sie den Wert hinter dem Feld **Belege** z. B. "1".</span><span class="sxs-lookup"><span data-stu-id="57669-127">Choose the value behind the **Documents** field, such as "1".</span></span>
3. <span data-ttu-id="57669-128">Wählen Sie auf der Seite **Angefügte Dokumente** die Aktion **Vorschau** aus.</span><span class="sxs-lookup"><span data-stu-id="57669-128">On the **Attached Documents** page, choose the **Preview** action.</span></span>
4. <span data-ttu-id="57669-129">Öffnen Sie die heruntergeladene Datei.</span><span class="sxs-lookup"><span data-stu-id="57669-129">Open the downloaded file.</span></span>

## <a name="to-save-a-document-as-a-pdf-attachment"></a><span data-ttu-id="57669-130">So speichern Sie ein Dokument als PDF-Anhang</span><span class="sxs-lookup"><span data-stu-id="57669-130">To save a document as a PDF attachment</span></span>
<span data-ttu-id="57669-131">Wann immer Sie ein Dokument als Datei speichern müssen, können Sie die Aktion **Anhängen als PDF** verwenden, um den aktuellen Dokumentinhalt als PDF-Datei zu erfassen, die an die FactBox des Dokuments angehängt wird.</span><span class="sxs-lookup"><span data-stu-id="57669-131">Whenever you need to save a document as a file, you can use the **Attach as PDF** action to capture the current document content as a PDF file attached to the FactBox of the document.</span></span> <span data-ttu-id="57669-132">Dies ist z.B. nützlich, wenn Dokumente mehreren Schritten in einem Prozess folgen, wie z.B. einem Verkaufsprozess oder einem Genehmigungs-Workflow, und Sie sich auf einen Ausdruck des vorherigen Schritts beziehen möchten.</span><span class="sxs-lookup"><span data-stu-id="57669-132">This is useful, for example, when documents follow multiple steps in a process, such as a sales process or an approval workflow, and you want to refer to a printout of the previous step.</span></span>

<span data-ttu-id="57669-133">Das folgende Verfahren basiert auf einer Auftragsabwicklung.</span><span class="sxs-lookup"><span data-stu-id="57669-133">The following procedure is based on a sales order.</span></span> <span data-ttu-id="57669-134">Die Schritte sind für alle unterstützten Dokumente ähnlich.</span><span class="sxs-lookup"><span data-stu-id="57669-134">The steps are similar for all supported documents.</span></span>

1. <span data-ttu-id="57669-135">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Verkaufsaufträge** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="57669-135">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders** , and then choose the related link.</span></span>
2. <span data-ttu-id="57669-136">Markieren Sie einen Debitorenauftrag, und wählen Sie dann die Aktion **Anhängen als PDF** .</span><span class="sxs-lookup"><span data-stu-id="57669-136">Select a sales order, and then choose the **Attach as PDF** action.</span></span>

<span data-ttu-id="57669-137">Eine PDF-Datei mit dem aktuellen Inhalt des Kundenauftrags wird der Registerkarte **Anlagen** im Infoboxbereich hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="57669-137">A PDF file with the current content of the sales order is added to the **Attachments** tab in the FactBox.</span></span>

## <a name="to-add-a-link-from-an-item-card"></a><span data-ttu-id="57669-138">Um einen Link von einer Artikelkarte hinzuzufügen</span><span class="sxs-lookup"><span data-stu-id="57669-138">To add a link from an item card</span></span>
<span data-ttu-id="57669-139">Sie können jeder URL oder jedem Pfad einen Link von einer Karte oder einem Dokument hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="57669-139">You can add a link from a card or document to any URL or path.</span></span> <span data-ttu-id="57669-140">Dies ist beispielsweise hilfreich, wenn Sie eine Artikelkarte mit dem Artikelkatalog des Lieferanten verknüpfen möchten.</span><span class="sxs-lookup"><span data-stu-id="57669-140">This is useful, for example, when you want to link an item card with the supplier's item catalog.</span></span>

<span data-ttu-id="57669-141">Das folgende Verfahren basiert auf einer Elementkarte.</span><span class="sxs-lookup"><span data-stu-id="57669-141">The following procedure is based on an item card.</span></span> <span data-ttu-id="57669-142">Die Schritte sind für alle anderen unterstützten Belege und Karten gleich.</span><span class="sxs-lookup"><span data-stu-id="57669-142">The steps are similar for all other supported cards and documents.</span></span>

1. <span data-ttu-id="57669-143">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Elemente** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="57669-143">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items** , and then choose the related link.</span></span>
2. <span data-ttu-id="57669-144">Wählen Sie das Element aus, zu dem Sie einen Link hinzufügen möchten, und wählen Sie dann die Registerkarte **Anhänge** in der Infobox.</span><span class="sxs-lookup"><span data-stu-id="57669-144">Select the item that you want to add a link from, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="57669-145">In dem **Link** , wählen Sie das **+** Symbol.</span><span class="sxs-lookup"><span data-stu-id="57669-145">In the **Links** , choose the **+** icon.</span></span>
4. <span data-ttu-id="57669-146">Geben Sie im Feld **Link Adresse** den Link ein.</span><span class="sxs-lookup"><span data-stu-id="57669-146">In the **Link Address** field, enter the link.</span></span>

    <span data-ttu-id="57669-147">Der Link muss eine gültige Internet- oder Intranet-URL sein.</span><span class="sxs-lookup"><span data-stu-id="57669-147">The link must be a valid internet or intranet URL.</span></span>

5. <span data-ttu-id="57669-148">Geben Sie im Feld **Beschreibung** die Informationen zu dem Link ein.</span><span class="sxs-lookup"><span data-stu-id="57669-148">In the **Description** field, enter any information about the link.</span></span>  
6. <span data-ttu-id="57669-149">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="57669-149">Choose the **OK** button.</span></span>

<span data-ttu-id="57669-150">Der Link ist jetzt an die Artikel-Karte angehängt.</span><span class="sxs-lookup"><span data-stu-id="57669-150">The link is now attached to the item card.</span></span>  

## <a name="to-write-a-note-on-a-sales-order"></a><span data-ttu-id="57669-151">So schreiben Sie eine Notiz zu einem Verkaufsauftrag</span><span class="sxs-lookup"><span data-stu-id="57669-151">To write a note on a sales order</span></span>
<span data-ttu-id="57669-152">Sie können eine Notiz auf ein Dokument oder eine Karte schreiben, um beispielsweise anderen Benutzern des Dokuments oder der Karte spezielle Anweisungen zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="57669-152">You can write a note on a document or card, for example, to communicate special instructions to other users of the document or card.</span></span> <span data-ttu-id="57669-153">Sie können Dateilinks und URLs in Notizen einfügen.</span><span class="sxs-lookup"><span data-stu-id="57669-153">You can include file links and URLs in notes.</span></span>

> [!NOTE]
> <span data-ttu-id="57669-154">Hinweise auf der Registerkarte **Anhänge** haben nichts mit der internen Notizfunktion zu tun, die hauptsächlich für die Kommunikation zwischen Workflowbenutzern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="57669-154">Notes on the **Attachments** tab are not related to internal notes functionality, which is mainly used to communicate between workflow users.</span></span> <span data-ttu-id="57669-155">Weitere Informationen finden Sie unter [Einrichten von Workflowbenachrichtigungen](across-setting-up-workflow-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="57669-155">For more information, see [Setting Up Workflow Notifications](across-setting-up-workflow-notifications.md).</span></span>

<span data-ttu-id="57669-156">Das folgende Verfahren basiert auf einer Auftragsabwicklung.</span><span class="sxs-lookup"><span data-stu-id="57669-156">The following procedure is based on a sales order.</span></span> <span data-ttu-id="57669-157">Die Schritte sind für alle anderen unterstützten Dokumente und Karten ähnlich.</span><span class="sxs-lookup"><span data-stu-id="57669-157">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="57669-158">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Verkaufsaufträge** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="57669-158">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders** , and then choose the related link.</span></span>
2. <span data-ttu-id="57669-159">Wählen Sie den Verkaufsauftrag aus, zu dem Sie einen Link hinzufügen möchten, und wählen Sie dann die Registerkarte **Anhänge** in der Infobox.</span><span class="sxs-lookup"><span data-stu-id="57669-159">Select the sales order that you want to write a note on, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="57669-160">In dem Abschnitt **Notizen** wählen Sie das **+** Symbol.</span><span class="sxs-lookup"><span data-stu-id="57669-160">In the **Notes** section, choose the **+** icon.</span></span>
4. <span data-ttu-id="57669-161">In dem Feld **Hinweis** geben Sie in das Feld einen beliebigen Text ein, z. B. "Dies ist eine dringende Bestellung.".</span><span class="sxs-lookup"><span data-stu-id="57669-161">In the **Note** field, write any text, such as "This is an urgent order.".</span></span>
5. <span data-ttu-id="57669-162">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="57669-162">Choose the **OK** button.</span></span>

<span data-ttu-id="57669-163">Der Hinweis ist jetzt dem Verkaufsauftrag beigefügt.</span><span class="sxs-lookup"><span data-stu-id="57669-163">The note is now attached to the sales order.</span></span>

## <a name="see-also"></a><span data-ttu-id="57669-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57669-164">See Also</span></span>  
<span data-ttu-id="57669-165">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="57669-165">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="57669-166">Eingehende Belege</span><span class="sxs-lookup"><span data-stu-id="57669-166">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="57669-167">Einrichten von Workflowbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="57669-167">Setting Up Workflow Notifications</span></span>](across-setting-up-workflow-notifications.md)  
