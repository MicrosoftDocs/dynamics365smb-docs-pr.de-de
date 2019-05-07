---
title: Designdetails - Lagerhaus Übersicht | Microsoft Docs
description: Um die physische Bewegung der Artikel auf dieser Zonen- und Lagerplatzebene zu unterstützen, müssen alle Informationen für jede Transaktion oder Umlagerung im Lager nachverfolgt werden. Dies wird in der Tabelle **Lagerplatzposten** verwaltet. Jede Transaktion wird in einem Lagerplatzjournal gespeichert.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: e174b56b8570f541ec10683fc8e44fb844da05c6
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "926016"
---
# <a name="design-details-warehouse-overview"></a><span data-ttu-id="13adc-105">Designdetails: Lagerübersicht</span><span class="sxs-lookup"><span data-stu-id="13adc-105">Design Details: Warehouse Overview</span></span>
<span data-ttu-id="13adc-106">Um die physische Bewegung der Artikel auf dieser Zonen- und Lagerplatzebene zu unterstützen, müssen alle Informationen für jede Transaktion oder Umlagerung im Lager nachverfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="13adc-106">To support the physical handling of items on the zone and bin level, all information must be traced for each transaction or movement in the warehouse.</span></span> <span data-ttu-id="13adc-107">Dies wird in der Tabelle **Lagerplatzposten** verwaltet.</span><span class="sxs-lookup"><span data-stu-id="13adc-107">This is managed in the **Warehouse Entry** table.</span></span> <span data-ttu-id="13adc-108">Jede Transaktion wird in einem Lagerplatzjournal gespeichert.</span><span class="sxs-lookup"><span data-stu-id="13adc-108">Each transaction is stored in a warehouse register.</span></span>  

<span data-ttu-id="13adc-109">Logistikbelege und ein Logistik Buch.-Blatt werden verwendet, um Artikelumlagerungen im Lager zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="13adc-109">Warehouse documents and a warehouse journal are used to register item movements in the warehouse.</span></span> <span data-ttu-id="13adc-110">Immer wenn ein Artikel im Lager umgelagert, erhalten, eingelagert, kommissioniert, geliefert oder angepasst wird, werden Lagerposten registriert, um die physischen Informationen zu Zone, Lagerplatz und Menge zu speichern.</span><span class="sxs-lookup"><span data-stu-id="13adc-110">Every time that an item in the warehouse is moved, received, put away, picked, shipped, or adjusted, warehouse entries are registered to store the physical information about zone, bin, and quantity.</span></span>

<span data-ttu-id="13adc-111">Die Tabelle **Lagerplatzinhalt** wird verwendet, um alle verschiedenen Dimensionen des Inhalts eines Lagerplatzes pro Artikel zu bearbeiten, wie etwa Mengeneinheit, Höchstmenge oder Mindestmenge.</span><span class="sxs-lookup"><span data-stu-id="13adc-111">The **Bin Content** table is used to handle all the different dimensions of the contents of a bin per item, such as unit of measure, maximum quantity, and minimum quantity.</span></span> <span data-ttu-id="13adc-112">Die Tabelle **Lagerplatzinhalt** enthält auch Flussfelder zu den Lagerplatzposten, Lageranweisungen und Logistik-Buch.-Blattzeilen, wodurch sichergestellt wird, dass die Verfügbarkeit eines Artikels pro Lagerplatz und eines Lagerplatzes für einen Artikel schnell berechnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="13adc-112">The **Bin Content** table also contains flow fields to the warehouse entries, warehouse instructions, and warehouse journal lines, which ensures that the availability of an item per bin and a bin for an item can be calculated quickly.</span></span> <span data-ttu-id="13adc-113">Weitere Informationen finden Sie unter [Designdetails: Verfügbarkeit im Lager](design-details-availability-in-the-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="13adc-113">For more information, see [Design Details: Availability in the Warehouse](design-details-availability-in-the-warehouse.md).</span></span>  

<span data-ttu-id="13adc-114">Wenn Artikelbuchungen außerhalb des Lagermoduls auftreten, wird ein Standard-Ausgleichslagerplatz pro Lagerort verwendet, um Lagerplatzposten mit Inventurposten zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="13adc-114">When item postings occur outside the warehouse module, a default adjustment bin per location is used to synchronize warehouse entries with inventory entries.</span></span> <span data-ttu-id="13adc-115">Während der Inventur des Lagers werden jegliche Abweichungen zwischen berechneten und gezählten Mengen am Regulierungslagerplatz erfasst und dann als korrigierende Artikelposten gebucht.</span><span class="sxs-lookup"><span data-stu-id="13adc-115">During physical inventory of the warehouse, any differences between the calculated and counted quantities are recorded in the adjustment bin and then posted as correcting item ledger entries.</span></span> <span data-ttu-id="13adc-116">Weitere Informationen finden Sie unter [Designdetails: Bestandintegration](design-details-integration-with-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="13adc-116">For more information, see [Design Details: Integration with Inventory](design-details-integration-with-inventory.md).</span></span>  

<span data-ttu-id="13adc-117">Die folgenden Abbildung zeigt typische Warenflüsse.</span><span class="sxs-lookup"><span data-stu-id="13adc-117">The following illustration outlines typical warehouse flows.</span></span>  

<span data-ttu-id="13adc-118">![Übersicht Lagerprozesse](media/design_details_warehouse_management_overview.png "Übersicht Lagerprozesse")</span><span class="sxs-lookup"><span data-stu-id="13adc-118">![Overview of warehouse processes](media/design_details_warehouse_management_overview.png "Overview of warehouse processes")</span></span>  

## <a name="basic-or-advanced-warehousing"></a><span data-ttu-id="13adc-119">Grundlegende oder erweiterte Lagerhaltung</span><span class="sxs-lookup"><span data-stu-id="13adc-119">Basic or Advanced Warehousing</span></span>  
<span data-ttu-id="13adc-120">Lagerfunktionen in [!INCLUDE[d365fin](includes/d365fin_md.md)] können in unterschiedlichen Komplexitätsebenen implementiert werden, abhängig von den Prozessen eines Unternehmens und dem Auftragsvolumen.</span><span class="sxs-lookup"><span data-stu-id="13adc-120">Warehouse functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)] can be implemented in different complexity levels, depending on a company’s processes and order volume.</span></span> <span data-ttu-id="13adc-121">Der wichtigste Unterschied besteht darin, dass Aktivitäten in der einfachen Logistik Auftrag für Auftrag durchgeführt werden, während sie in der erweiterten Logistik für mehrere Aufträge konsolidiert werden.</span><span class="sxs-lookup"><span data-stu-id="13adc-121">The main difference is that activities are performed order-by-order in basic warehousing when they are consolidated for multiple orders in advanced warehousing.</span></span>  

 <span data-ttu-id="13adc-122">Um zwischen den verschiedenen Komplexitätsebenen zu unterscheiden, verwendet diese Dokumentation zwei allgemeine Bezeichnungen, grundlegende und erweiterte Lagerhaltung.</span><span class="sxs-lookup"><span data-stu-id="13adc-122">To differentiate between the different complexity levels, this documentation refers to two general denominations, Basic and Advanced Warehousing.</span></span> <span data-ttu-id="13adc-123">Diese einfache Unterscheidung umfasst mehrere verschiedene Komplexitätsebenen, die durch definierte Produktdetails und Lagerorteinrichtung definiert sind, wobei jede durch unterschiedliche UI-Dokumente unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="13adc-123">This simple differentiation covers several different complexity levels as defined by product granules and location setup, each supported by different UI documents.</span></span> <span data-ttu-id="13adc-124">Weitere Informationen finden Sie unter [Designdetails: Lagerhaus einrichten](design-details-warehouse-setup.md).</span><span class="sxs-lookup"><span data-stu-id="13adc-124">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="13adc-125">Die höchstentwickelte Ebene der Logistik wird in dieser Dokumentation als „WMS-Installationen“ bezeichnet, da diese Methode die höchstentwickelten Elemente und Logistiksysteme erfordert.</span><span class="sxs-lookup"><span data-stu-id="13adc-125">The most advanced level of warehousing is referred to as “WMS installations” in this documentation, since this level requires the most advanced granule, Warehouse Management Systems.</span></span>  

 <span data-ttu-id="13adc-126">Die folgenden verschiedenen UI-Dokumente werden in der einfachen und der erweiterten Logistik verwendet.</span><span class="sxs-lookup"><span data-stu-id="13adc-126">The following different UI documents are used in basic and advanced warehousing.</span></span>  

## <a name="basic-ui-documents"></a><span data-ttu-id="13adc-127">Grundlegende UI-Dokumente</span><span class="sxs-lookup"><span data-stu-id="13adc-127">Basic UI Documents</span></span>  

-   <span data-ttu-id="13adc-128">**Lagereinlagerung**</span><span class="sxs-lookup"><span data-stu-id="13adc-128">**Inventory Put-away**</span></span>  
-   <span data-ttu-id="13adc-129">**Lagerkommissionierung**</span><span class="sxs-lookup"><span data-stu-id="13adc-129">**Inventory Pick**</span></span>  
-   <span data-ttu-id="13adc-130">**Lagerbestandsumlagerung**</span><span class="sxs-lookup"><span data-stu-id="13adc-130">**Inventory Movement**</span></span>  
-   <span data-ttu-id="13adc-131">**Artikel Buch.-Blatt**</span><span class="sxs-lookup"><span data-stu-id="13adc-131">**Item Journal**</span></span>  
-   <span data-ttu-id="13adc-132">**Artikel Umlag. Buch.-Blatt**</span><span class="sxs-lookup"><span data-stu-id="13adc-132">**Item Reclassification Journal**</span></span>  
-   <span data-ttu-id="13adc-133">(Verschiedene Berichte)</span><span class="sxs-lookup"><span data-stu-id="13adc-133">(Various reports)</span></span>  

## <a name="advanced-ui-documents"></a><span data-ttu-id="13adc-134">Erweiterte UI-Dokumente</span><span class="sxs-lookup"><span data-stu-id="13adc-134">Advanced UI Documents</span></span>  

-   <span data-ttu-id="13adc-135">**Wareneingang**</span><span class="sxs-lookup"><span data-stu-id="13adc-135">**Warehouse Receipt**</span></span>  
-   <span data-ttu-id="13adc-136">**Einlagerungsvorschlag**</span><span class="sxs-lookup"><span data-stu-id="13adc-136">**Put-away Worksheet**</span></span>  
-   <span data-ttu-id="13adc-137">**Einlagerung**</span><span class="sxs-lookup"><span data-stu-id="13adc-137">**Warehouse Put-away**</span></span>  
-   <span data-ttu-id="13adc-138">**Kommissioniervorschlag**</span><span class="sxs-lookup"><span data-stu-id="13adc-138">**Pick Worksheet**</span></span>  
-   <span data-ttu-id="13adc-139">**Kommissionierung**</span><span class="sxs-lookup"><span data-stu-id="13adc-139">**Warehouse Pick**</span></span>  
-   <span data-ttu-id="13adc-140">**Lagerplatzumlagerungsvorschlag**</span><span class="sxs-lookup"><span data-stu-id="13adc-140">**Movement Worksheet**</span></span>  
-   <span data-ttu-id="13adc-141">**Lagerplatzumlagerung**</span><span class="sxs-lookup"><span data-stu-id="13adc-141">**Warehouse Movement**</span></span>  
-   <span data-ttu-id="13adc-142">**Interne Kommissionierung**</span><span class="sxs-lookup"><span data-stu-id="13adc-142">**Internal Whse. Pick**</span></span>  
-   <span data-ttu-id="13adc-143">**Interne Einlag.-Anforderung**</span><span class="sxs-lookup"><span data-stu-id="13adc-143">**Internal Whse. Put-away**</span></span>  
-   <span data-ttu-id="13adc-144">**Lagerplatz Erst.-Vorschlag**</span><span class="sxs-lookup"><span data-stu-id="13adc-144">**Bin Creation Worksheet**</span></span>  
-   <span data-ttu-id="13adc-145">**Lagerplatzinh. Erst.-Vorschlag**</span><span class="sxs-lookup"><span data-stu-id="13adc-145">**Bin Content Creation Worksheet**</span></span>  
-   <span data-ttu-id="13adc-146">**Logistik Artikel Buch.-Blatt**</span><span class="sxs-lookup"><span data-stu-id="13adc-146">**Whse. Item Journal**</span></span>  
-   <span data-ttu-id="13adc-147">**Umlagerung Logistik Artikel Buch.-Blatt**</span><span class="sxs-lookup"><span data-stu-id="13adc-147">**Whse. Item Reclass. Journal**</span></span>  
-   <span data-ttu-id="13adc-148">(Verschiedene Berichte)</span><span class="sxs-lookup"><span data-stu-id="13adc-148">(Various reports)</span></span>  

<span data-ttu-id="13adc-149">Weitere Informationen über jeden Beleg finden Sie den entsprechenden Fensterthemen.</span><span class="sxs-lookup"><span data-stu-id="13adc-149">For more information about each document, see the respective page topics.</span></span>  

### <a name="terminology"></a><span data-ttu-id="13adc-150">Terminologie</span><span class="sxs-lookup"><span data-stu-id="13adc-150">Terminology</span></span>  
<span data-ttu-id="13adc-151">Um mit den Finanzbegriffen Einkauf und von Verkauf zu entsprechen, verwendet [!INCLUDE[d365fin](includes/d365fin_md.md)] Lagerdokumentation die folgenden Begriffe für Warenfluss im Lager.</span><span class="sxs-lookup"><span data-stu-id="13adc-151">To align with the financial concepts of purchases and sales, [!INCLUDE[d365fin](includes/d365fin_md.md)] warehouse documentation refers to the following terms for item flow in the warehouse.</span></span>  

|<span data-ttu-id="13adc-152">Begriff</span><span class="sxs-lookup"><span data-stu-id="13adc-152">Term</span></span>|<span data-ttu-id="13adc-153">Description</span><span class="sxs-lookup"><span data-stu-id="13adc-153">Description</span></span>|  
|----------|---------------------------------------|  
|<span data-ttu-id="13adc-154">Eingehender Fluss</span><span class="sxs-lookup"><span data-stu-id="13adc-154">Inbound flow</span></span>|<span data-ttu-id="13adc-155">Artikel, die in den Lagerort eingehen, z.B. Einkäufe und eingehende Umlagerungen.</span><span class="sxs-lookup"><span data-stu-id="13adc-155">Items moving into the warehouse location, such as purchases and inbound transfers.</span></span>|  
|<span data-ttu-id="13adc-156">Interne Flüsse</span><span class="sxs-lookup"><span data-stu-id="13adc-156">Internal flow</span></span>|<span data-ttu-id="13adc-157">Artikel, die innerhalb des Lagerorts verschoben werden, wie z.B. Produktionskomponenten und fertiggestellte Artikel.</span><span class="sxs-lookup"><span data-stu-id="13adc-157">Items moving inside the warehouse location, such as production components and output.</span></span>|  
|<span data-ttu-id="13adc-158">Ausgehender Warenfluss</span><span class="sxs-lookup"><span data-stu-id="13adc-158">Outbound flow</span></span>|<span data-ttu-id="13adc-159">Artikel, die aus dem Lagerort ausgehen, z.B. Verkäufe und ausgehende Umlagerungen.</span><span class="sxs-lookup"><span data-stu-id="13adc-159">Items moving out of the warehouse location, such as sales and outbound transfers.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="13adc-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13adc-160">See Also</span></span>  
 [<span data-ttu-id="13adc-161">Designdetails: Logistik</span><span class="sxs-lookup"><span data-stu-id="13adc-161">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)
