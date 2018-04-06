---
title: Erweiterte Belegverwaltung
description: "In Finance and Operations, Business edition können Belege archiviert und die Arbeit über archivierte und nicht archivierte Belege nachverfolgt werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 66b688a1a437fd369b41fa05da4557a7cb96e29c
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="enhanced-document-management"></a><span data-ttu-id="bd9bc-103">Erweiterte Belegverwaltung</span><span class="sxs-lookup"><span data-stu-id="bd9bc-103">Enhanced Document Management</span></span>
<span data-ttu-id="bd9bc-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] können Belege archiviert und die Arbeit über archivierte und nicht archivierte Belege nachverfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="bd9bc-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can archive documents and track work across archived and non-archived documents.</span></span>  

## <a name="archiving-documents"></a><span data-ttu-id="bd9bc-105">Archivieren von Belegen</span><span class="sxs-lookup"><span data-stu-id="bd9bc-105">Archiving Documents</span></span>  
 <span data-ttu-id="bd9bc-106">Die erweiterte Archivbelegverwaltung kann für folgende Zwecke verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="bd9bc-106">You can use enhanced archive document management to:</span></span>  

- <span data-ttu-id="bd9bc-107">Archivieren von Rahmenaufträgen</span><span class="sxs-lookup"><span data-stu-id="bd9bc-107">Archive blanket orders</span></span>  
- <span data-ttu-id="bd9bc-108">Kopieren von Belegen</span><span class="sxs-lookup"><span data-stu-id="bd9bc-108">Copy documents</span></span>  
- <span data-ttu-id="bd9bc-109">Nachverfolgen von Belegzeilen</span><span class="sxs-lookup"><span data-stu-id="bd9bc-109">Track document lines</span></span>  

## <a name="archiving-blanket-orders"></a><span data-ttu-id="bd9bc-110">Archivieren von Rahmenaufträgen</span><span class="sxs-lookup"><span data-stu-id="bd9bc-110">Archiving Blanket Orders</span></span>  
<span data-ttu-id="bd9bc-111">Sie können Rahmenaufträge und -bestellungen archivieren und mithilfe von archivierten Rahmenaufträgen und -bestellungen standardmäßige Verkaufsaufträge und Bestellungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="bd9bc-111">You can archive blanket sales and purchase orders, and use archived blanket sales and purchase orders to create standard sales and purchase orders.</span></span>  

<span data-ttu-id="bd9bc-112">Folgende Dokumente können bei jedem Löschen eines Angebots oder Auftrags automatisch archiviert werden:</span><span class="sxs-lookup"><span data-stu-id="bd9bc-112">You can automatically archive the following each time a quote or order is deleted:</span></span>  

- <span data-ttu-id="bd9bc-113">Verkaufs- und Einkaufsanfragen</span><span class="sxs-lookup"><span data-stu-id="bd9bc-113">Sales and purchase quotes</span></span>  
- <span data-ttu-id="bd9bc-114">Rahmenaufträge und -bestellungen</span><span class="sxs-lookup"><span data-stu-id="bd9bc-114">Blanket sales and blanket purchase orders</span></span>  
- <span data-ttu-id="bd9bc-115">Verkaufsaufträge und Bestellungen</span><span class="sxs-lookup"><span data-stu-id="bd9bc-115">Sales and purchase orders</span></span>  

<span data-ttu-id="bd9bc-116">Sie können die archivierte Version der Rahmenbestellungen oder Rahmenaufträge löschen, die mit dem Stapelverarbeitungsauftrag **Archivierte Rahmenbestellungsversionen löschen** oder **Archivierte Rahmenauftragsversion löschen** gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="bd9bc-116">You can delete the archived version of the blanket purchase orders or blanket sales orders that have been deleted using the **Delete Archived Blanket Purchase Order Version** batch job or **Delete Archived Blanket Sales Order Version** batch job.</span></span> <span data-ttu-id="bd9bc-117">Zudem können auch Details aus einem archivierten Rahmenauftrag in einen Auftrag kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="bd9bc-117">Also, you can copy details from an archived blanket order to an order.</span></span>  

## <a name="tracking-document-lines"></a><span data-ttu-id="bd9bc-118">Nachverfolgen von Belegzeilen</span><span class="sxs-lookup"><span data-stu-id="bd9bc-118">Tracking Document Lines</span></span>  
<span data-ttu-id="bd9bc-119">Sie können eine Belegzeile in einer Belegart auswählen und die zugehörigen Belege anzeigen und abrufen.</span><span class="sxs-lookup"><span data-stu-id="bd9bc-119">You can select a document line within a document type, and view and retrieve the related documents.</span></span> <span data-ttu-id="bd9bc-120">Belegzeilen können in folgenden Dokumenten nachverfolgt werden:</span><span class="sxs-lookup"><span data-stu-id="bd9bc-120">You can track document lines from:</span></span>  

- <span data-ttu-id="bd9bc-121">Aufträge</span><span class="sxs-lookup"><span data-stu-id="bd9bc-121">Orders</span></span>  
- <span data-ttu-id="bd9bc-122">Archivierte Aufträge</span><span class="sxs-lookup"><span data-stu-id="bd9bc-122">Archived orders</span></span>  
- <span data-ttu-id="bd9bc-123">Rahmenbestellungen</span><span class="sxs-lookup"><span data-stu-id="bd9bc-123">Blanket orders</span></span>  
- <span data-ttu-id="bd9bc-124">Archivierte Rahmenaufträge</span><span class="sxs-lookup"><span data-stu-id="bd9bc-124">Archived blanket orders</span></span>  
- <span data-ttu-id="bd9bc-125">Angebote</span><span class="sxs-lookup"><span data-stu-id="bd9bc-125">Quotes</span></span>  
- <span data-ttu-id="bd9bc-126">Mit archivierten Angeboten</span><span class="sxs-lookup"><span data-stu-id="bd9bc-126">Archived quotes</span></span>  
- <span data-ttu-id="bd9bc-127">Mit gebuchten Lieferungen</span><span class="sxs-lookup"><span data-stu-id="bd9bc-127">Posted shipments</span></span>  
- <span data-ttu-id="bd9bc-128">Mit gebuchten Rechnungen</span><span class="sxs-lookup"><span data-stu-id="bd9bc-128">Posted invoices</span></span>  

## <a name="see-also"></a><span data-ttu-id="bd9bc-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd9bc-129">See Also</span></span>  
 <span data-ttu-id="bd9bc-130">[Erstellen von Rahmenaufträgen](../../sales-how-to-create-blanket-sales-orders.md) </span><span class="sxs-lookup"><span data-stu-id="bd9bc-130">[Create Blanket Sales Orders](../../sales-how-to-create-blanket-sales-orders.md) </span></span>  
 [<span data-ttu-id="bd9bc-131">Nachverfolgen von Belegzeilen</span><span class="sxs-lookup"><span data-stu-id="bd9bc-131">Track Document Lines</span></span>](how-to-track-document-lines.md)

