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
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 4827e25d97127faf691b96df9868320bb47dee39
ms.contentlocale: de-de
ms.lasthandoff: 11/26/2018

---
# <a name="archive-documents"></a><span data-ttu-id="7bec1-103">Beleg archivieren</span><span class="sxs-lookup"><span data-stu-id="7bec1-103">Archive Documents</span></span>
<span data-ttu-id="7bec1-104">Sie können auch Aufträge oder Bestellungen, Angebote, Reklamationen und Rahmenaufträge archivieren, und Sie können den archivierten Beleg verwenden, um den Beleg neu zu erstellen, dass er aus archiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="7bec1-104">You can archive sales and purchase orders, quotes, return orders, and blanket orders, and you can use the archived document to recreate the document that it was archived from.</span></span>

## <a name="to-set-up-automatic-document-archiving"></a><span data-ttu-id="7bec1-105">So richten Sie die automatische Archivierung von Belegen ein</span><span class="sxs-lookup"><span data-stu-id="7bec1-105">To set up automatic document archiving</span></span>  
<span data-ttu-id="7bec1-106">Sie können die automatische Archivierung von Verkaufs- und Einkaufsbelegen einrichten – beispielsweise Angebote, Rahmenbestellungen und Aufträge – bevor Sie Belege löschen.</span><span class="sxs-lookup"><span data-stu-id="7bec1-106">You can set up automatic archiving of sales and purchase orders, quotes, blanket orders, and return orders, before you delete documents.</span></span>

<span data-ttu-id="7bec1-107">Nachfolgend wird beschrieben, wie die automatische Archivierung von Verkaufsbelegen eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="7bec1-107">The following procedure describes how to set up automatic archiving of sales documents.</span></span> <span data-ttu-id="7bec1-108">Die Schritte sind für eine Einkaufsdokumente ähnlich.</span><span class="sxs-lookup"><span data-stu-id="7bec1-108">The steps are similar for purchase documents.</span></span>
1.  <span data-ttu-id="7bec1-109">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Debitoren & Verkauf einrichten** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="7bec1-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="7bec1-110">Füllen Sie auf der Seite **Debitoren und Verkauf Einr.** die folgenden Felder aus:</span><span class="sxs-lookup"><span data-stu-id="7bec1-110">On the **Sales & Receivables Setup** page, fill in the fields as follows.</span></span>

|<span data-ttu-id="7bec1-111">Feld</span><span class="sxs-lookup"><span data-stu-id="7bec1-111">Field</span></span>|<span data-ttu-id="7bec1-112">Description</span><span class="sxs-lookup"><span data-stu-id="7bec1-112">Description</span></span>|
|-----|-----------|
|<span data-ttu-id="7bec1-113">**Angebote archivieren**</span><span class="sxs-lookup"><span data-stu-id="7bec1-113">**Archiving Sales Quotes**</span></span>|<span data-ttu-id="7bec1-114">**Nie**, wenn die Verkaufsangebote beim Löschen niemals archiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7bec1-114">**Never** to never archive sales quotes when they are deleted.</span></span> <span data-ttu-id="7bec1-115">**Frage**, wenn der Benutzer aufgefordert werden soll, auszuwählen, ob Verkaufsangebote beim Löschen archiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7bec1-115">**Question** to prompt the user to choose whether to archive sales quotes when they are deleted.</span></span> <span data-ttu-id="7bec1-116">**Immer**, wenn Verkaufsangebote beim Löschen automatisch archiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7bec1-116">**Always** to archive sales quotes automatically when they are deleted.</span></span>|
|<span data-ttu-id="7bec1-117">**Info zu Rahmenaufträgen**</span><span class="sxs-lookup"><span data-stu-id="7bec1-117">**Archiving Blanket Sales Orders**</span></span>|<span data-ttu-id="7bec1-118">Wählen Sie diese Option aus, um Rahmenaufträge bei jedem Löschen automatisch zu archivieren.</span><span class="sxs-lookup"><span data-stu-id="7bec1-118">Select to archive blanket sales orders automatically each time they are deleted.</span></span>|
|<span data-ttu-id="7bec1-119">**Arch. Bestellungen und Reklamationen**</span><span class="sxs-lookup"><span data-stu-id="7bec1-119">**Arch. Orders and Ret. Orders**</span></span>|<span data-ttu-id="7bec1-120">Wählen Sie diese Option aus, um Verkaufsaufträge bei jedem Löschen automatisch zu archivieren.</span><span class="sxs-lookup"><span data-stu-id="7bec1-120">Select to automatically archive sales orders each time they are deleted.</span></span>|

## <a name="to-archive-a-sales-order"></a><span data-ttu-id="7bec1-121">Verkaufsauftrag archivieren</span><span class="sxs-lookup"><span data-stu-id="7bec1-121">To archive a sales order</span></span>
<span data-ttu-id="7bec1-122">Nachfolgend wird beschrieben, wie Sie einen Auftrag archivieren</span><span class="sxs-lookup"><span data-stu-id="7bec1-122">The following procedure describes how to archive a sales order.</span></span> <span data-ttu-id="7bec1-123">Die Schritte für Einkaufsreklamationen, Serviceaufträge und ausgehende Umlagerungsaufträge sind ähnlich.</span><span class="sxs-lookup"><span data-stu-id="7bec1-123">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="7bec1-124">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Aufträge** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="7bec1-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="7bec1-125">Öffnen Sie einen Verkaufsauftrag für Artikel, die Sie archivierne möchten.</span><span class="sxs-lookup"><span data-stu-id="7bec1-125">Open a sales order that you want to archive.</span></span>  
3.  <span data-ttu-id="7bec1-126">Wählen Sie die **Beleg archivieren**-Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="7bec1-126">Choose the **Archive Document** action.</span></span>

<span data-ttu-id="7bec1-127">Der Auftrag ist archiviert.</span><span class="sxs-lookup"><span data-stu-id="7bec1-127">The sales order is archived.</span></span> <span data-ttu-id="7bec1-128">Sie können sie auf der Seite **Archivierte Aufträge** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7bec1-128">You can view it on the **Archived Sales orders** page.</span></span> <span data-ttu-id="7bec1-129">Von hier aus können Sie es verwenden, um den Verkaufsauftrag neu zu erstellen, der archiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="7bec1-129">From here, you can also use it to recreate the sales order that it was archived from.</span></span>

## <a name="to-recreate-a-sales-order-from-the-archive"></a><span data-ttu-id="7bec1-130">Einen Auftrag aus Posten neu erstellen</span><span class="sxs-lookup"><span data-stu-id="7bec1-130">To recreate a sales order from the archive</span></span>
<span data-ttu-id="7bec1-131">Nachfolgend wird beschrieben, wie Sie einen Auftrag neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7bec1-131">The following procedure describes how to recreate a sales order.</span></span> <span data-ttu-id="7bec1-132">Die Schritte für Einkaufsreklamationen, Serviceaufträge und ausgehende Umlagerungsaufträge sind ähnlich.</span><span class="sxs-lookup"><span data-stu-id="7bec1-132">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="7bec1-133">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Archivierte Verkaufsaufträge** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="7bec1-133">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Archived Sales Orders**, and then choose the related link.</span></span>
2.  <span data-ttu-id="7bec1-134">Wählen Sie den zu archivierenden Verkaufsauftrag aus, klicken Sie auf Aktionen und anschließend auf **Wiederherstellen**.</span><span class="sxs-lookup"><span data-stu-id="7bec1-134">Select the archived sales order that you want to recreate, and then choose the **Restore** action.</span></span>  

<span data-ttu-id="7bec1-135">Der Verkaufsauftrag wird auf der Seite **Verkaufsaufträge** erstellt und hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7bec1-135">The sales order is created and added to the **Sales Orders** page.</span></span>

## <a name="to-delete-archived-sales-orders"></a><span data-ttu-id="7bec1-136">Archivierte Auftragsversionen löschen</span><span class="sxs-lookup"><span data-stu-id="7bec1-136">To delete archived sales orders</span></span>
<span data-ttu-id="7bec1-137">Nachfolgend wird beschrieben, wie Sie einen archivierten Auftrag löschen.</span><span class="sxs-lookup"><span data-stu-id="7bec1-137">The following procedure describes how to delete archived sales orders.</span></span> <span data-ttu-id="7bec1-138">Die Schritte sind für alle anderen archivierten Einkaufs- und Verkaufsbelege ähnlich.</span><span class="sxs-lookup"><span data-stu-id="7bec1-138">The steps are similar for other archived sales and purchase documents.</span></span>

1.  <span data-ttu-id="7bec1-139">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Archivierte Verkaufsauftragsversionen löschen** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="7bec1-139">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Archived Sales Order Versions**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="7bec1-140">auf der Seite **Archivierte Auftragsversionen löschen** wählen Sie den entsprechenden Filter aus.</span><span class="sxs-lookup"><span data-stu-id="7bec1-140">On the **Delete Archived Sales Order Versions** page, select the appropriate filters.</span></span>  
3.  <span data-ttu-id="7bec1-141">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="7bec1-141">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="7bec1-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7bec1-142">See Also</span></span>
[<span data-ttu-id="7bec1-143">Nachverfolgen von Belegzeilen</span><span class="sxs-lookup"><span data-stu-id="7bec1-143">Track Document Lines</span></span>](across-how-to-track-document-lines.md)  
[<span data-ttu-id="7bec1-144">Verkauf</span><span class="sxs-lookup"><span data-stu-id="7bec1-144">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="7bec1-145">Allgemeine Geschäftsfunktionen</span><span class="sxs-lookup"><span data-stu-id="7bec1-145">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="7bec1-146">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7bec1-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

