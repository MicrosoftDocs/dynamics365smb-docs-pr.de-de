---
title: Einkaufs- und Verkaufsbelege archivieren | Microsoft Docs
description: "Sie können auch Aufträge oder Bestellungen, Angebote, Reklamationen und Rahmenaufträge archivieren, und Sie können den archivierten Beleg verwenden, um den Beleg neu zu erstellen, dass er aus archiviert wurde."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 12/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 74460bfcff36d293006229f4a89719f8c05c2631
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="archive-documents"></a><span data-ttu-id="5991e-103">Beleg archivieren</span><span class="sxs-lookup"><span data-stu-id="5991e-103">Archive Documents</span></span>
<span data-ttu-id="5991e-104">Sie können auch Aufträge oder Bestellungen, Angebote, Reklamationen und Rahmenaufträge archivieren, und Sie können den archivierten Beleg verwenden, um den Beleg neu zu erstellen, dass er aus archiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="5991e-104">You can archive sales and purchase orders, quotes, return orders, and blanket orders, and you can use the archived document to recreate the document that it was archived from.</span></span>

## <a name="to-set-up-automatic-document-archiving"></a><span data-ttu-id="5991e-105">So richten Sie die automatische Archivierung von Belegen ein</span><span class="sxs-lookup"><span data-stu-id="5991e-105">To set up automatic document archiving</span></span>  
<span data-ttu-id="5991e-106">Sie können die automatische Archivierung von Verkaufs- und Einkaufsbelegen einrichten – beispielsweise Angebote, Rahmenbestellungen und Aufträge – bevor Sie Belege löschen.</span><span class="sxs-lookup"><span data-stu-id="5991e-106">You can set up automatic archiving of sales and purchase orders, quotes, blanket orders, and return orders, before you delete documents.</span></span>

<span data-ttu-id="5991e-107">Nachfolgend wird beschrieben, wie die automatische Archivierung von Verkaufsbelegen eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="5991e-107">The following procedure describes how to set up automatic archiving of sales documents.</span></span> <span data-ttu-id="5991e-108">Die Schritte sind für eine Einkaufsdokumente ähnlich.</span><span class="sxs-lookup"><span data-stu-id="5991e-108">The steps are similar for purchase documents.</span></span>
1.  <span data-ttu-id="5991e-109">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Debit&oren && Verkauf Einr.** ein und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="5991e-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="5991e-110">Füllen Sie im Feld **Debitoren & Verkauf Einr.** die folgenden Felder aus:</span><span class="sxs-lookup"><span data-stu-id="5991e-110">In the **Sales & Receivables Setup** window, fill in the fields as follows.</span></span>

|<span data-ttu-id="5991e-111">Feld</span><span class="sxs-lookup"><span data-stu-id="5991e-111">Field</span></span>|<span data-ttu-id="5991e-112">Description</span><span class="sxs-lookup"><span data-stu-id="5991e-112">Description</span></span>|
|-----|-----------|
|<span data-ttu-id="5991e-113">**Angebote archivieren**</span><span class="sxs-lookup"><span data-stu-id="5991e-113">**Archiving Sales Quotes**</span></span>|<span data-ttu-id="5991e-114">**Nie**, wenn die Verkaufsangebote beim Löschen niemals archiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5991e-114">**Never** to never archive sales quotes when they are deleted.</span></span> <span data-ttu-id="5991e-115">**Frage**, wenn der Benutzer aufgefordert werden soll, auszuwählen, ob Verkaufsangebote beim Löschen archiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5991e-115">**Question** to prompt the user to choose whether to archive sales quotes when they are deleted.</span></span> <span data-ttu-id="5991e-116">**Immer**, wenn Verkaufsangebote beim Löschen automatisch archiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5991e-116">**Always** to archive sales quotes automatically when they are deleted.</span></span>|
|<span data-ttu-id="5991e-117">**Info zu Rahmenaufträgen**</span><span class="sxs-lookup"><span data-stu-id="5991e-117">**Archiving Blanket Sales Orders**</span></span>|<span data-ttu-id="5991e-118">Wählen Sie diese Option aus, um Rahmenaufträge bei jedem Löschen automatisch zu archivieren.</span><span class="sxs-lookup"><span data-stu-id="5991e-118">Select to archive blanket sales orders automatically each time they are deleted.</span></span>|
|<span data-ttu-id="5991e-119">**Arch. Bestellungen und Reklamationen**</span><span class="sxs-lookup"><span data-stu-id="5991e-119">**Arch. Orders and Ret. Orders**</span></span>|<span data-ttu-id="5991e-120">Wählen Sie diese Option aus, um Verkaufsaufträge bei jedem Löschen automatisch zu archivieren.</span><span class="sxs-lookup"><span data-stu-id="5991e-120">Select to automatically archive sales orders each time they are deleted.</span></span>|

## <a name="to-archive-a-sales-order"></a><span data-ttu-id="5991e-121">Verkaufsauftrag archivieren</span><span class="sxs-lookup"><span data-stu-id="5991e-121">To archive a sales order</span></span>
<span data-ttu-id="5991e-122">Nachfolgend wird beschrieben, wie Sie einen Auftrag archivieren</span><span class="sxs-lookup"><span data-stu-id="5991e-122">The following procedure describes how to archive a sales order.</span></span> <span data-ttu-id="5991e-123">Die Schritte für Einkaufsreklamationen, Serviceaufträge und ausgehende Umlagerungsaufträge sind ähnlich.</span><span class="sxs-lookup"><span data-stu-id="5991e-123">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="5991e-124">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Verkaufsauftrag** ein, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="5991e-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5991e-125">Öffnen Sie einen Verkaufsauftrag für Artikel, die Sie archivierne möchten.</span><span class="sxs-lookup"><span data-stu-id="5991e-125">Open a sales order that you want to archive.</span></span>  
3.  <span data-ttu-id="5991e-126">Wählen Sie die **Beleg archivieren**-Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="5991e-126">Choose the **Archive Document** action.</span></span>

<span data-ttu-id="5991e-127">Der Auftrag ist archiviert.</span><span class="sxs-lookup"><span data-stu-id="5991e-127">The sales order is archived.</span></span> <span data-ttu-id="5991e-128">Sie können sie im Fenster **Archivierte Aufträge** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="5991e-128">You can view it in the **Archived Sales orders** window.</span></span> <span data-ttu-id="5991e-129">Von hier aus können Sie es verwenden, um den Verkaufsauftrag neu zu erstellen, der archiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="5991e-129">From here, you can also use it to recreate the sales order that it was archived from.</span></span>

## <a name="to-recreate-a-sales-order-from-the-archive"></a><span data-ttu-id="5991e-130">Einen Auftrag aus Posten neu erstellen</span><span class="sxs-lookup"><span data-stu-id="5991e-130">To recreate a sales order from the archive</span></span>
<span data-ttu-id="5991e-131">Nachfolgend wird beschrieben, wie Sie einen Auftrag neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5991e-131">The following procedure describes how to recreate a sales order.</span></span> <span data-ttu-id="5991e-132">Die Schritte für Einkaufsreklamationen, Serviceaufträge und ausgehende Umlagerungsaufträge sind ähnlich.</span><span class="sxs-lookup"><span data-stu-id="5991e-132">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="5991e-133">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Auftrag archivieren** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="5991e-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Archived Sales Orders**, and then choose the related link.</span></span>
2.  <span data-ttu-id="5991e-134">Wählen Sie den zu archivierenden Verkaufsauftrag aus, klicken Sie auf Aktionen und anschließend auf **Wiederherstellen**.</span><span class="sxs-lookup"><span data-stu-id="5991e-134">Select the archived sales order that you want to recreate, and then choose the **Restore** action.</span></span>  

<span data-ttu-id="5991e-135">Der Verkaufsauftrag wird im  **Verkaufsaufträge** Fenster erstellt und hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5991e-135">The sales order is created and added to the **Sales Orders** window.</span></span>

## <a name="to-delete-archived-sales-orders"></a><span data-ttu-id="5991e-136">Archivierte Auftragsversionen löschen</span><span class="sxs-lookup"><span data-stu-id="5991e-136">To delete archived sales orders</span></span>
<span data-ttu-id="5991e-137">Nachfolgend wird beschrieben, wie Sie einen archivierten Auftrag löschen.</span><span class="sxs-lookup"><span data-stu-id="5991e-137">The following procedure describes how to delete archived sales orders.</span></span> <span data-ttu-id="5991e-138">Die Schritte sind für alle anderen archivierten Einkaufs- und Verkaufsbelege ähnlich.</span><span class="sxs-lookup"><span data-stu-id="5991e-138">The steps are similar for other archived sales and purchase documents.</span></span>

1.  <span data-ttu-id="5991e-139">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Archivierte Rahmenbestellungen löschen** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="5991e-139">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Archived Sales Order Versions**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5991e-140">Im Fenster **Archivierte Auftragsversionen löschen** wählen Sie den entsprechenden Filter aus.</span><span class="sxs-lookup"><span data-stu-id="5991e-140">In the **Delete Archived Sales Order Versions** window, select the appropriate filters.</span></span>  
3.  <span data-ttu-id="5991e-141">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="5991e-141">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="5991e-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5991e-142">See Also</span></span>
[<span data-ttu-id="5991e-143">Nachverfolgen von Belegzeilen</span><span class="sxs-lookup"><span data-stu-id="5991e-143">Track Document Lines</span></span>](across-how-to-track-document-lines.md)  
[<span data-ttu-id="5991e-144">Verkauf</span><span class="sxs-lookup"><span data-stu-id="5991e-144">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="5991e-145">Allgemeine Geschäftsfunktionen</span><span class="sxs-lookup"><span data-stu-id="5991e-145">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="5991e-146">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5991e-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

