---
title: Posten finden | Microsoft Docs
description: Dieser Artikel beschreibt, wie Dokumente und Posten verknüpft sind
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 437e0c076b664ad35d5819783e98d9e91abee982
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393974"
---
# <a name="finding-related-entries-for-posted-documents"></a><span data-ttu-id="7bded-103">Suchen verwandter Posten für gebuchte Belege</span><span class="sxs-lookup"><span data-stu-id="7bded-103">Finding Related Entries for Posted Documents</span></span> 

<span data-ttu-id="7bded-104">In diesem Artikel erfahren Sie, wie Sie Belege und Posten finden, die miteinander verwandt sind, basierend auf gemeinsamen Informationen, wie z. B.:</span><span class="sxs-lookup"><span data-stu-id="7bded-104">In this article, you learn how to find documents and entries that are related to each other based on a common information, like:</span></span>

- <span data-ttu-id="7bded-105">Belegnummer oder Buchungsdatum</span><span class="sxs-lookup"><span data-stu-id="7bded-105">Document number or posting date</span></span>
- <span data-ttu-id="7bded-106">Geschäftskontaktart, -nummer oder externe Belegnummer</span><span class="sxs-lookup"><span data-stu-id="7bded-106">Business contact type, number, or external document number</span></span>
- <span data-ttu-id="7bded-107">Seriennummer oder Chargennummer des Artikels</span><span class="sxs-lookup"><span data-stu-id="7bded-107">Item serial number or lot number</span></span>

<span data-ttu-id="7bded-108">Diese Funktion ist nützlich, wenn Sie Posten finden möchten, die aus bestimmten Transaktionen resultierten.</span><span class="sxs-lookup"><span data-stu-id="7bded-108">This feature is useful for finding the ledger entries that resulted from certain transactions.</span></span> <span data-ttu-id="7bded-109">Wenn Sie anhand von einer Belegnummer suchen, können Sie die Zusammenfassung über den Bericht „Belegposten“ ausdrucken.</span><span class="sxs-lookup"><span data-stu-id="7bded-109">When you search by document number, you can print the summary from the Document Entries report.</span></span>

## <a name="get-started"></a><span data-ttu-id="7bded-110">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="7bded-110">Get started</span></span>

<span data-ttu-id="7bded-111">Die Funktion zum Suchen von Posten ist auf den meisten Seiten verfügbar, auf denen gebuchte Belege oder gebuchte Belegposten angezeigt werden – sowohl für Listen als auch für Karten.</span><span class="sxs-lookup"><span data-stu-id="7bded-111">The find entries feature is readily available on most pages that display posted documents or posted documents entries - for both lists and cards.</span></span> <span data-ttu-id="7bded-112">Der erste Schritt ist also das Öffnen einer dieser Seiten.</span><span class="sxs-lookup"><span data-stu-id="7bded-112">So the first step is open one of these pages.</span></span> <span data-ttu-id="7bded-113">Dann wählen Sie entweder die Aktion **Posten suchen** aus oder drücken die Tasten ALT+G.</span><span class="sxs-lookup"><span data-stu-id="7bded-113">Then, either choose the **Find Entries** action or press the Alt+G keys.</span></span>

<span data-ttu-id="7bded-114">Die Seite **Posten suchen** enthält alle verknüpften Belege und Posten basierend auf der Belegnr. und dem Buchungsdatum.</span><span class="sxs-lookup"><span data-stu-id="7bded-114">The **Find Entries** page  includes all related documents and entries based on the document no. and posting date.</span></span> <span data-ttu-id="7bded-115">Die Seite ist in drei Abschnitte unterteilt:</span><span class="sxs-lookup"><span data-stu-id="7bded-115">The page is divided into three sections:</span></span>

- <span data-ttu-id="7bded-116">Im oberen Abschnitt werden Felder und Aktionen angezeigt, die Sie zum Filtern Ihrer Suche verwenden.</span><span class="sxs-lookup"><span data-stu-id="7bded-116">The top section displays fields and actions that you use for filtering your search.</span></span>
- <span data-ttu-id="7bded-117">Im mittleren Bereich werden verwandte Belege basierend auf der Suche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7bded-117">The middle section displays related documents based on the search.</span></span>
- <span data-ttu-id="7bded-118">Im unteren Abschnitt werden Informationen über den Herkunftsbeleg angezeigt, der durch die Suche gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="7bded-118">The bottom section displays information about the source document that was found by searching.</span></span>


<!--
 There are two ways to open this page:

- Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Find Entries**, and then choose the related link.

    With this way, the **Find Entries** page might be empty, and you'll have to start searching for entries from scratch.
    
- Open a page that displays posted documents or posted documents entries, either a list or a card. Then, locate and select the **Find Entries** action.

    With this way, the **Find Entries**, page will include all related documents and entries based on the document no. and posting date.


    > [!TIP]
    > If you are on a page that has the **Find Entries** action, press crtl+G to open the **Find Entries** page directly. 
-->

## <a name="search-for-entries"></a><span data-ttu-id="7bded-119">Suche nach Posten</span><span class="sxs-lookup"><span data-stu-id="7bded-119">Search for entries</span></span>

<span data-ttu-id="7bded-120">Sie können nach Posten suchen, basierend auf Informationen entweder über den Beleg, den Geschäftskontakt oder die Artikelreferenz.</span><span class="sxs-lookup"><span data-stu-id="7bded-120">You can search for entries based on information about either the document, business contact, or item reference.</span></span> <span data-ttu-id="7bded-121">Um die Suche zu ändern, wählen Sie **Aktionen**, **Suchen nach** und dann eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="7bded-121">To change the search, select **Actions**, **Find By**, then one of the following actions:</span></span>

|<span data-ttu-id="7bded-122">Aktion</span><span class="sxs-lookup"><span data-stu-id="7bded-122">Action</span></span>|<span data-ttu-id="7bded-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7bded-123">Description</span></span>|
|------|-----------|
|<span data-ttu-id="7bded-124">Nach Beleg suchen</span><span class="sxs-lookup"><span data-stu-id="7bded-124">Find by Document</span></span>|<span data-ttu-id="7bded-125">Zeigen Sie Posten basierend auf einer bestimmten Belegnummer oder einem bestimmten Buchungsdatum an.</span><span class="sxs-lookup"><span data-stu-id="7bded-125">View entries based on a specific document number or posting date.</span></span>|
|<span data-ttu-id="7bded-126">Geschäftskontakt</span><span class="sxs-lookup"><span data-stu-id="7bded-126">Business Contact</span></span> |<span data-ttu-id="7bded-127">Zeigen Sie Posten basierend auf einer bestimmten Kontaktart, Kontaktnummer und/oder externer Belegnummer an.</span><span class="sxs-lookup"><span data-stu-id="7bded-127">View entries based on a specific contact type, contact number, anr/or external document number.</span></span> <span data-ttu-id="7bded-128">Sie können Beleginformationen eingeben, die von einem Kreditor oder einem Debitor zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="7bded-128">You can enter document information that was assigned by a vendor or a customer.</span></span> <span data-ttu-id="7bded-129">Verwenden Sie die verfügbaren Felder, um nach Kreditorenbelegen zu suchen, indem Sie die Nummern verwenden, die der Kreditor den Belegen zugewiesen hat.</span><span class="sxs-lookup"><span data-stu-id="7bded-129">Use the available fields to search for vendor documents by using the numbers that the vendor has assigned the documents.</span></span>|
|<span data-ttu-id="7bded-130">Artikelreferenz</span><span class="sxs-lookup"><span data-stu-id="7bded-130">Item reference</span></span>|<span data-ttu-id="7bded-131">Zeigen Sie Posten basierend auf einer Seriennummer oder Chargennummer an.</span><span class="sxs-lookup"><span data-stu-id="7bded-131">View entires based on a serial number or lot number.</span></span> <span data-ttu-id="7bded-132">Sie können die Chargennummer oder Seriennummer eingeben oder nach der Chargennummer oder Seriennummer filtern, nach der Sie suchen möchten.</span><span class="sxs-lookup"><span data-stu-id="7bded-132">You can enter the lot number or serial number, or filter on the lot number or serial number that you want to search for.</span></span> <span data-ttu-id="7bded-133">Mithilfe dieser Aktion kann festgestellt werden, ob eine bestimmte Artikelverfolgungsnummer verwendet wurde, von welchem Kreditor sie stammt oder an welchen Debitor der Artikel verkauft wurde.</span><span class="sxs-lookup"><span data-stu-id="7bded-133">This action is useful to see where a specific item tracking number was used, what vendor it came from, or what customer it was sold to.</span></span>|

<span data-ttu-id="7bded-134">Nachdem Sie eine Auswahl getroffen haben, geben Sie die relevanten Suchinformationen in die Felder oben ein.</span><span class="sxs-lookup"><span data-stu-id="7bded-134">After you make a selection, enter the relevant search information in the fields at the top.</span></span> <span data-ttu-id="7bded-135">Verwenden Sie die QuickInfos in den Feldern zur Hilfe.</span><span class="sxs-lookup"><span data-stu-id="7bded-135">Use the tooltips on the fields to help.</span></span> <span data-ttu-id="7bded-136">Wenn Sie fertig sind, wählen Sie **Suchen**, um die Suche zu starten.</span><span class="sxs-lookup"><span data-stu-id="7bded-136">When you're finished, choose **Find** to start the search.</span></span> <span data-ttu-id="7bded-137">Wenn Sie eine der Filter ändern, müssen Sie **Suchen** erneut wählen.</span><span class="sxs-lookup"><span data-stu-id="7bded-137">If you change any of the filters, you have to choose **Find** again.</span></span>

> [!TIP]
> <span data-ttu-id="7bded-138">Ein paar Beispiele zur Verwendung von **Posten suchen** sehen Sie hier: [Artikel mit Artikelverfolgung nachverfolgen](inventory-how-to-trace-item-tracked-items.md) und [Exemplarische Vorgehensweise: Nachverfolgen von Serienchargennummern](walkthrough-tracing-serial-lot-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="7bded-138">For a couple examples about using **Find Entries**, see [Trace Item-Tracked Items](inventory-how-to-trace-item-tracked-items.md) and [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md).</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="7bded-139">Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="7bded-139">See Related Training at [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="7bded-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7bded-140">See Also</span></span>

[<span data-ttu-id="7bded-141">Arbeiten mit Business Central</span><span class="sxs-lookup"><span data-stu-id="7bded-141">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="7bded-142">Fügen Sie Ihrem Rollencenter eine Seitenaktion hinzu</span><span class="sxs-lookup"><span data-stu-id="7bded-142">Add a Page Action to Your Role Center</span></span>](ui-bookmarks.md)  
[<span data-ttu-id="7bded-143">Verfolgen von Artikeln mit Artikelverfolgung</span><span class="sxs-lookup"><span data-stu-id="7bded-143">Trace Item-Tracked Items</span></span>](inventory-how-to-trace-item-tracked-items.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]