---
title: Designdetails - Lagerhaus Übersicht | Microsoft Docs
description: Um die physische Bewegung der Artikel auf dieser Zonen- und Lagerplatzebene zu unterstützen, müssen alle Informationen für jede Transaktion oder Umlagerung im Lager nachverfolgt werden. Dies wird in der Tabelle **Lagerplatzposten** verwaltet. Jede Transaktion wird in einem Lagerplatzjournal gespeichert.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b265f8a910ba4d6e36856ce6d4485532b4e1337a
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3920822"
---
# <a name="design-details-warehouse-overview"></a><span data-ttu-id="c0049-105">Designdetails: Lagerübersicht</span><span class="sxs-lookup"><span data-stu-id="c0049-105">Design Details: Warehouse Overview</span></span>
<span data-ttu-id="c0049-106">Um die physische Bewegung der Artikel auf dieser Zonen- und Lagerplatzebene zu unterstützen, müssen alle Informationen für jede Transaktion oder Umlagerung im Lager nachverfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="c0049-106">To support the physical handling of items on the zone and bin level, all information must be traced for each transaction or movement in the warehouse.</span></span> <span data-ttu-id="c0049-107">Dies wird in der Tabelle **Lagerplatzposten** verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c0049-107">This is managed in the **Warehouse Entry** table.</span></span> <span data-ttu-id="c0049-108">Jede Transaktion wird in einem Lagerplatzjournal gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c0049-108">Each transaction is stored in a warehouse register.</span></span>  

<span data-ttu-id="c0049-109">Logistikbelege und ein Logistik Buch.-Blatt werden verwendet, um Artikelumlagerungen im Lager zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="c0049-109">Warehouse documents and a warehouse journal are used to register item movements in the warehouse.</span></span> <span data-ttu-id="c0049-110">Immer wenn ein Artikel im Lager umgelagert, erhalten, eingelagert, kommissioniert, geliefert oder angepasst wird, werden Lagerposten registriert, um die physischen Informationen zu Zone, Lagerplatz und Menge zu speichern.</span><span class="sxs-lookup"><span data-stu-id="c0049-110">Every time that an item in the warehouse is moved, received, put away, picked, shipped, or adjusted, warehouse entries are registered to store the physical information about zone, bin, and quantity.</span></span>

<span data-ttu-id="c0049-111">Die Tabelle **Lagerplatzinhalt** wird verwendet, um alle verschiedenen Dimensionen des Inhalts eines Lagerplatzes pro Artikel zu bearbeiten, wie etwa Mengeneinheit, Höchstmenge oder Mindestmenge.</span><span class="sxs-lookup"><span data-stu-id="c0049-111">The **Bin Content** table is used to handle all the different dimensions of the contents of a bin per item, such as unit of measure, maximum quantity, and minimum quantity.</span></span> <span data-ttu-id="c0049-112">Die Tabelle **Lagerplatzinhalt** enthält auch Flussfelder zu den Lagerplatzposten, Lageranweisungen und Logistik-Buch.-Blattzeilen, wodurch sichergestellt wird, dass die Verfügbarkeit eines Artikels pro Lagerplatz und eines Lagerplatzes für einen Artikel schnell berechnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c0049-112">The **Bin Content** table also contains flow fields to the warehouse entries, warehouse instructions, and warehouse journal lines, which ensures that the availability of an item per bin and a bin for an item can be calculated quickly.</span></span> <span data-ttu-id="c0049-113">Weitere Informationen finden Sie unter [Designdetails: Verfügbarkeit im Lager](design-details-availability-in-the-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="c0049-113">For more information, see [Design Details: Availability in the Warehouse](design-details-availability-in-the-warehouse.md).</span></span>  

<span data-ttu-id="c0049-114">Wenn Artikelbuchungen außerhalb des Lagermoduls auftreten, wird ein Standard-Ausgleichslagerplatz pro Lagerort verwendet, um Lagerplatzposten mit Inventurposten zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="c0049-114">When item postings occur outside the warehouse module, a default adjustment bin per location is used to synchronize warehouse entries with inventory entries.</span></span> <span data-ttu-id="c0049-115">Während der Inventur des Lagers werden jegliche Abweichungen zwischen berechneten und gezählten Mengen am Regulierungslagerplatz erfasst und dann als korrigierende Artikelposten gebucht.</span><span class="sxs-lookup"><span data-stu-id="c0049-115">During physical inventory of the warehouse, any differences between the calculated and counted quantities are recorded in the adjustment bin and then posted as correcting item ledger entries.</span></span> <span data-ttu-id="c0049-116">Weitere Informationen finden Sie unter [Designdetails: Bestandintegration](design-details-integration-with-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="c0049-116">For more information, see [Design Details: Integration with Inventory](design-details-integration-with-inventory.md).</span></span>  

<span data-ttu-id="c0049-117">Die folgenden Abbildung zeigt typische Warenflüsse.</span><span class="sxs-lookup"><span data-stu-id="c0049-117">The following illustration outlines typical warehouse flows.</span></span>  

<span data-ttu-id="c0049-118">![Überblick über Lagerprozesse](media/design_details_warehouse_management_overview.png "Überblick über Lagerprozesse")</span><span class="sxs-lookup"><span data-stu-id="c0049-118">![Overview of warehouse processes](media/design_details_warehouse_management_overview.png "Overview of warehouse processes")</span></span>  

## <a name="basic-or-advanced-warehousing"></a><span data-ttu-id="c0049-119">Grundlegende oder erweiterte Lagerhaltung</span><span class="sxs-lookup"><span data-stu-id="c0049-119">Basic or Advanced Warehousing</span></span>  
<span data-ttu-id="c0049-120">Lagerfunktionen in [!INCLUDE[d365fin](includes/d365fin_md.md)] können in unterschiedlichen Komplexitätsebenen implementiert werden, abhängig von den Prozessen eines Unternehmens und dem Auftragsvolumen.</span><span class="sxs-lookup"><span data-stu-id="c0049-120">Warehouse functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)] can be implemented in different complexity levels, depending on a company’s processes and order volume.</span></span> <span data-ttu-id="c0049-121">Der wichtigste Unterschied besteht darin, dass Aktivitäten in der einfachen Logistik Auftrag für Auftrag durchgeführt werden, während sie in der erweiterten Logistik für mehrere Aufträge konsolidiert werden.</span><span class="sxs-lookup"><span data-stu-id="c0049-121">The main difference is that activities are performed order-by-order in basic warehousing when they are consolidated for multiple orders in advanced warehousing.</span></span>  

 <span data-ttu-id="c0049-122">Um zwischen den verschiedenen Komplexitätsebenen zu unterscheiden, verwendet diese Dokumentation zwei allgemeine Bezeichnungen, grundlegende und erweiterte Lagerhaltung.</span><span class="sxs-lookup"><span data-stu-id="c0049-122">To differentiate between the different complexity levels, this documentation refers to two general denominations, Basic and Advanced Warehousing.</span></span> <span data-ttu-id="c0049-123">Diese einfache Unterscheidung umfasst mehrere verschiedene Komplexitätsebenen, die durch definierte Produktdetails und Lagerorteinrichtung definiert sind, wobei jede durch unterschiedliche UI-Dokumente unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="c0049-123">This simple differentiation covers several different complexity levels as defined by product granules and location setup, each supported by different UI documents.</span></span> <span data-ttu-id="c0049-124">Weitere Informationen finden Sie unter [Designdetails: Lagerhaus einrichten](design-details-warehouse-setup.md).</span><span class="sxs-lookup"><span data-stu-id="c0049-124">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="c0049-125">Die höchstentwickelte Ebene der Logistik wird in dieser Dokumentation als „WMS-Installationen“ bezeichnet, da diese Methode die höchstentwickelten Elemente und Logistiksysteme erfordert.</span><span class="sxs-lookup"><span data-stu-id="c0049-125">The most advanced level of warehousing is referred to as “WMS installations” in this documentation, since this level requires the most advanced granule, Warehouse Management Systems.</span></span>  

 <span data-ttu-id="c0049-126">Die folgenden verschiedenen UI-Dokumente werden in der einfachen und der erweiterten Logistik verwendet.</span><span class="sxs-lookup"><span data-stu-id="c0049-126">The following different UI documents are used in basic and advanced warehousing.</span></span>  

## <a name="basic-ui-documents"></a><span data-ttu-id="c0049-127">Grundlegende UI-Dokumente</span><span class="sxs-lookup"><span data-stu-id="c0049-127">Basic UI Documents</span></span>  

-   <span data-ttu-id="c0049-128">**Lagereinlagerung**</span><span class="sxs-lookup"><span data-stu-id="c0049-128">**Inventory Put-away**</span></span>  
-   <span data-ttu-id="c0049-129">**Lagerkommissionierung**</span><span class="sxs-lookup"><span data-stu-id="c0049-129">**Inventory Pick**</span></span>  
-   <span data-ttu-id="c0049-130">**Lagerbestandsumlagerung**</span><span class="sxs-lookup"><span data-stu-id="c0049-130">**Inventory Movement**</span></span>  
-   <span data-ttu-id="c0049-131">**Artikel Buch.-Blatt**</span><span class="sxs-lookup"><span data-stu-id="c0049-131">**Item Journal**</span></span>  
-   <span data-ttu-id="c0049-132">**Artikel Umlag. Buch.-Blatt**</span><span class="sxs-lookup"><span data-stu-id="c0049-132">**Item Reclassification Journal**</span></span>  
-   <span data-ttu-id="c0049-133">(Verschiedene Berichte)</span><span class="sxs-lookup"><span data-stu-id="c0049-133">(Various reports)</span></span>  

## <a name="advanced-ui-documents"></a><span data-ttu-id="c0049-134">Erweiterte UI-Dokumente</span><span class="sxs-lookup"><span data-stu-id="c0049-134">Advanced UI Documents</span></span>  

-   <span data-ttu-id="c0049-135">**Wareneingang**</span><span class="sxs-lookup"><span data-stu-id="c0049-135">**Warehouse Receipt**</span></span>  
-   <span data-ttu-id="c0049-136">**Einlagerungsvorschlag**</span><span class="sxs-lookup"><span data-stu-id="c0049-136">**Put-away Worksheet**</span></span>  
-   <span data-ttu-id="c0049-137">**Einlagerung**</span><span class="sxs-lookup"><span data-stu-id="c0049-137">**Warehouse Put-away**</span></span>  
-   <span data-ttu-id="c0049-138">**Kommissioniervorschlag**</span><span class="sxs-lookup"><span data-stu-id="c0049-138">**Pick Worksheet**</span></span>  
-   <span data-ttu-id="c0049-139">**Kommissionierung**</span><span class="sxs-lookup"><span data-stu-id="c0049-139">**Warehouse Pick**</span></span>  
-   <span data-ttu-id="c0049-140">**Lagerplatzumlagerungsvorschlag**</span><span class="sxs-lookup"><span data-stu-id="c0049-140">**Movement Worksheet**</span></span>  
-   <span data-ttu-id="c0049-141">**Lagerplatzumlagerung**</span><span class="sxs-lookup"><span data-stu-id="c0049-141">**Warehouse Movement**</span></span>  
-   <span data-ttu-id="c0049-142">**Interne Kommissionierung**</span><span class="sxs-lookup"><span data-stu-id="c0049-142">**Internal Whse. Pick**</span></span>  
-   <span data-ttu-id="c0049-143">**Interne Einlag.-Anforderung**</span><span class="sxs-lookup"><span data-stu-id="c0049-143">**Internal Whse. Put-away**</span></span>  
-   <span data-ttu-id="c0049-144">**Lagerplatz Erst.-Vorschlag**</span><span class="sxs-lookup"><span data-stu-id="c0049-144">**Bin Creation Worksheet**</span></span>  
-   <span data-ttu-id="c0049-145">**Lagerplatzinh. Erst.-Vorschlag**</span><span class="sxs-lookup"><span data-stu-id="c0049-145">**Bin Content Creation Worksheet**</span></span>  
-   <span data-ttu-id="c0049-146">**Logistik Artikel Buch.-Blatt**</span><span class="sxs-lookup"><span data-stu-id="c0049-146">**Whse. Item Journal**</span></span>  
-   <span data-ttu-id="c0049-147">**Umlagerung Logistik Artikel Buch.-Blatt**</span><span class="sxs-lookup"><span data-stu-id="c0049-147">**Whse. Item Reclass. Journal**</span></span>  
-   <span data-ttu-id="c0049-148">(Verschiedene Berichte)</span><span class="sxs-lookup"><span data-stu-id="c0049-148">(Various reports)</span></span>  

<span data-ttu-id="c0049-149">Weitere Informationen über jeden Beleg finden Sie den entsprechenden Fensterthemen.</span><span class="sxs-lookup"><span data-stu-id="c0049-149">For more information about each document, see the respective page topics.</span></span>  

### <a name="terminology"></a><span data-ttu-id="c0049-150">Terminologie</span><span class="sxs-lookup"><span data-stu-id="c0049-150">Terminology</span></span>  
<span data-ttu-id="c0049-151">Um mit den Finanzbegriffen Einkauf und von Verkauf zu entsprechen, verwendet [!INCLUDE[d365fin](includes/d365fin_md.md)] Lagerdokumentation die folgenden Begriffe für Warenfluss im Lager.</span><span class="sxs-lookup"><span data-stu-id="c0049-151">To align with the financial concepts of purchases and sales, [!INCLUDE[d365fin](includes/d365fin_md.md)] warehouse documentation refers to the following terms for item flow in the warehouse.</span></span>  

|<span data-ttu-id="c0049-152">Begriff</span><span class="sxs-lookup"><span data-stu-id="c0049-152">Term</span></span>|<span data-ttu-id="c0049-153">Description</span><span class="sxs-lookup"><span data-stu-id="c0049-153">Description</span></span>|  
|----------|---------------------------------------|  
|<span data-ttu-id="c0049-154">Eingehender Fluss</span><span class="sxs-lookup"><span data-stu-id="c0049-154">Inbound flow</span></span>|<span data-ttu-id="c0049-155">Artikel, die in den Lagerort eingehen, z.B. Einkäufe und eingehende Umlagerungen.</span><span class="sxs-lookup"><span data-stu-id="c0049-155">Items moving into the warehouse location, such as purchases and inbound transfers.</span></span>|  
|<span data-ttu-id="c0049-156">Interne Flüsse</span><span class="sxs-lookup"><span data-stu-id="c0049-156">Internal flow</span></span>|<span data-ttu-id="c0049-157">Artikel, die innerhalb des Lagerorts verschoben werden, wie z.B. Produktionskomponenten und fertiggestellte Artikel.</span><span class="sxs-lookup"><span data-stu-id="c0049-157">Items moving inside the warehouse location, such as production components and output.</span></span>|  
|<span data-ttu-id="c0049-158">Ausgehender Warenfluss</span><span class="sxs-lookup"><span data-stu-id="c0049-158">Outbound flow</span></span>|<span data-ttu-id="c0049-159">Artikel, die aus dem Lagerort ausgehen, z.B. Verkäufe und ausgehende Umlagerungen.</span><span class="sxs-lookup"><span data-stu-id="c0049-159">Items moving out of the warehouse location, such as sales and outbound transfers.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="c0049-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0049-160">See Also</span></span>  
 [<span data-ttu-id="c0049-161">Designdetails: Logistik</span><span class="sxs-lookup"><span data-stu-id="c0049-161">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)
