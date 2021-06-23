---
title: Kommissionierung und Lieferung in Basis-Lagerkonfigurationen
description: In Business Central können die ausgehenden Prozesse für die Komissionierung und Lieferung auf vier Arten, mit den verschiedenen Funktionen, abhängig von der Lagerkomplexitätsebene, ausgeführt werden.
author: jill-kotel-andersson
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: e1763e6288c8b8218955049ba7ef4c461ee5164e
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214653"
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a><span data-ttu-id="e01b3-103">Exemplarische Vorgehensweise: Kommissionierung und Lieferung in Basis-Lagerkonfigurationen</span><span class="sxs-lookup"><span data-stu-id="e01b3-103">Walkthrough: Picking and Shipping in Basic Warehouse Configurations</span></span>

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)] -->

<span data-ttu-id="e01b3-104">In [!INCLUDE[prod_short](includes/prod_short.md)] können die ausgehenden Prozesse für die Komissionierung und Lieferung auf vier Arten, mit den verschiedenen Funktionen, abhängig von der Lagerkomplexitätsebene, ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e01b3-104">In [!INCLUDE[prod_short](includes/prod_short.md)], the outbound processes for picking and shipping can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="e01b3-105">Art</span><span class="sxs-lookup"><span data-stu-id="e01b3-105">Method</span></span>|<span data-ttu-id="e01b3-106">Eingangsprozess</span><span class="sxs-lookup"><span data-stu-id="e01b3-106">Inbound process</span></span>|<span data-ttu-id="e01b3-107">Lagerplätze</span><span class="sxs-lookup"><span data-stu-id="e01b3-107">Bins</span></span>|<span data-ttu-id="e01b3-108">Kommissionierungen</span><span class="sxs-lookup"><span data-stu-id="e01b3-108">Picks</span></span>|<span data-ttu-id="e01b3-109">Lieferungen</span><span class="sxs-lookup"><span data-stu-id="e01b3-109">Shipments</span></span>|<span data-ttu-id="e01b3-110">Komplexitätsebene anzeigen (siehe [Designdetails: Lagerhaus-Einrichtung](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="e01b3-110">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="e01b3-111">A</span><span class="sxs-lookup"><span data-stu-id="e01b3-111">A</span></span>|<span data-ttu-id="e01b3-112">Beitragsentnahme und -Lieferung aus der Auftragszeile</span><span class="sxs-lookup"><span data-stu-id="e01b3-112">Post pick and shipment from the order line</span></span>|<span data-ttu-id="e01b3-113">X</span><span class="sxs-lookup"><span data-stu-id="e01b3-113">X</span></span>|||<span data-ttu-id="e01b3-114">2</span><span class="sxs-lookup"><span data-stu-id="e01b3-114">2</span></span>|  
|<span data-ttu-id="e01b3-115">F</span><span class="sxs-lookup"><span data-stu-id="e01b3-115">B</span></span>|<span data-ttu-id="e01b3-116">Buchen Sie die Kommissionierung und den Warenausgang aus einem Lagerkommissionierungsbeleg</span><span class="sxs-lookup"><span data-stu-id="e01b3-116">Post pick and shipment from an inventory pick document</span></span>||<span data-ttu-id="e01b3-117">X</span><span class="sxs-lookup"><span data-stu-id="e01b3-117">X</span></span>||<span data-ttu-id="e01b3-118">3</span><span class="sxs-lookup"><span data-stu-id="e01b3-118">3</span></span>|  
|<span data-ttu-id="e01b3-119">L</span><span class="sxs-lookup"><span data-stu-id="e01b3-119">C</span></span>|<span data-ttu-id="e01b3-120">Buchen Sie die Kommissionierung und den Warenausgang aus einem Warenausgangsbeleg</span><span class="sxs-lookup"><span data-stu-id="e01b3-120">Post pick and shipment from a warehouse shipment document</span></span>|||<span data-ttu-id="e01b3-121">X</span><span class="sxs-lookup"><span data-stu-id="e01b3-121">X</span></span>|<span data-ttu-id="e01b3-122">4/5/6</span><span class="sxs-lookup"><span data-stu-id="e01b3-122">4/5/6</span></span>|  
|<span data-ttu-id="e01b3-123">T</span><span class="sxs-lookup"><span data-stu-id="e01b3-123">D</span></span>|<span data-ttu-id="e01b3-124">Buchen Sie die Kommissionierung von einem Kommissionierbeleg und buchen Sie den Warenausgang aus einem Warenausgangsbeleg</span><span class="sxs-lookup"><span data-stu-id="e01b3-124">Post pick from a warehouse pick document and post shipment from a warehouse shipment document</span></span>||<span data-ttu-id="e01b3-125">X</span><span class="sxs-lookup"><span data-stu-id="e01b3-125">X</span></span>|<span data-ttu-id="e01b3-126">X</span><span class="sxs-lookup"><span data-stu-id="e01b3-126">X</span></span>|<span data-ttu-id="e01b3-127">4/5/6</span><span class="sxs-lookup"><span data-stu-id="e01b3-127">4/5/6</span></span>|  

<span data-ttu-id="e01b3-128">Weitere Informationen finden Sie unter [Designdetails: Ausgehender Lagerfluss](design-details-outbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="e01b3-128">For more information, see [Design Details: Outbound Warehouse Flow](design-details-outbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="e01b3-129">In der folgenden Vorgehensweise wird Methode B in der vorhergegangenen Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e01b3-129">The following walkthrough demonstrates method B in the previous table.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="e01b3-130">Informationen zu dieser exemplarischen Vorgehensweise</span><span class="sxs-lookup"><span data-stu-id="e01b3-130">About This Walkthrough</span></span>

<span data-ttu-id="e01b3-131">Bei Basis-Lagerkonfigurationen gilt Folgendes: Wenn ein Lagerort so eingerichtet wurde, dass Kommissionierung erforderlich ist, jedoch Warenausgang nicht erforderlich ist, verwenden Sie die Seite **Lagerkommissionierung**, um Kommissionier- und Warenausgangsinformationen für Ihre Herkunftsbelege zu erfassen und zu buchen.</span><span class="sxs-lookup"><span data-stu-id="e01b3-131">In basic warehouse configurations where your location is set up to require pick processing but not ship processing, you use the **Inventory Pick** page to record and post pick and ship information for your outbound source documents.</span></span> <span data-ttu-id="e01b3-132">Der ausgehende Herkunftsbeleg kann ein Verkaufsauftrag, eine Einkaufsreklamation, ein ausgehender Umlagerungsauftrag, ein Fertigungsauftrag oder ein Komponentenbedarf sein.</span><span class="sxs-lookup"><span data-stu-id="e01b3-132">The outbound source document can be a sales order, purchase return order, outbound transfer order, or a production order with component need.</span></span>  

<span data-ttu-id="e01b3-133">In dieser exemplarischen Vorgehensweise werden folgende Aufgaben erläutert:</span><span class="sxs-lookup"><span data-stu-id="e01b3-133">This walkthrough demonstrates the following tasks:</span></span>  

- <span data-ttu-id="e01b3-134">Einrichten des SÜD-Lagerorts für die Lagerkommissionierung.</span><span class="sxs-lookup"><span data-stu-id="e01b3-134">Setting up SOUTH location for inventory picks.</span></span>  
- <span data-ttu-id="e01b3-135">Erstellen eines Verkaufsauftrags für den Debitor 10000 für 30 AMSTERDAM Lampen.</span><span class="sxs-lookup"><span data-stu-id="e01b3-135">Creating a sales order for customer 10000 for 30 Amsterdam Lamps.</span></span>  
- <span data-ttu-id="e01b3-136">Freigeben des Verkaufsauftrags für Lagerdurchlaufzeit.</span><span class="sxs-lookup"><span data-stu-id="e01b3-136">Releasing the sales order for warehouse handling.</span></span>  
- <span data-ttu-id="e01b3-137">Erstellen einer Lagerkommissionierung basierend auf einem freigegebenen Herkunftsbeleg.</span><span class="sxs-lookup"><span data-stu-id="e01b3-137">Creating an inventory pick based on a released source document.</span></span>  
- <span data-ttu-id="e01b3-138">Erfassen der Lagerplatzumlagerung aus dem Lager und gleichzeitig Buchen der Verkaufslieferung für den ursprünglichen Verkaufsauftrag.</span><span class="sxs-lookup"><span data-stu-id="e01b3-138">Registering the warehouse movement from the warehouse and at the same time posting the sales shipment for the source sales order.</span></span>  

## <a name="roles"></a><span data-ttu-id="e01b3-139">Rollen</span><span class="sxs-lookup"><span data-stu-id="e01b3-139">Roles</span></span>

<span data-ttu-id="e01b3-140">Die Aufgaben in dieser Demonstration werden von den folgenden Benutzerrollen ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="e01b3-140">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

- <span data-ttu-id="e01b3-141">Lagerortleiter</span><span class="sxs-lookup"><span data-stu-id="e01b3-141">Warehouse Manager</span></span>  
- <span data-ttu-id="e01b3-142">Auftragsverarbeitung</span><span class="sxs-lookup"><span data-stu-id="e01b3-142">Order Processor</span></span>  
- <span data-ttu-id="e01b3-143">Lagermitarbeiter</span><span class="sxs-lookup"><span data-stu-id="e01b3-143">Warehouse Worker</span></span>  

<!-- ## Prerequisites

To complete this walkthrough, you will need:  

- For [!INCLUDE[prod_short](includes/prod_short.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment. For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, CRONUS installed.
 -->

## <a name="story"></a><span data-ttu-id="e01b3-144">Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e01b3-144">Story</span></span>

<span data-ttu-id="e01b3-145">Ellen, die Lagermanagerin bei CRONUS, richtet das SÜD-Lager für grundlegende Komissionierungshandlung ein, in dem Lagermitarbeiter ausgehende Aufträge einzeln verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="e01b3-145">Ellen, the warehouse manager at CRONUS, sets up SOUTH warehouse for basic pick handling where warehouse workers process outbound orders individually.</span></span> <span data-ttu-id="e01b3-146">Martha, die Verkaufsauftragsbearbeiterin, erstellt einen Verkaufsauftrag für 30 Einheiten des Artikels 1928-S, die dem Debitor 10000 aus dem SÜD-Lager geliefert werden.</span><span class="sxs-lookup"><span data-stu-id="e01b3-146">Susan, the order processor, creates a sales order for 30 units of item 1928-S to be shipped to customer 10000 from the SOUTH Warehouse.</span></span> <span data-ttu-id="e01b3-147">John, der Lagermitarbeiter muss sicherstellen, dass die Lieferung an den Debitor vorbereitet und geliefert wird.</span><span class="sxs-lookup"><span data-stu-id="e01b3-147">John, the warehouse worker must make sure that the shipment is prepared and delivered to the customer.</span></span> <span data-ttu-id="e01b3-148">John verwaltet alle beteiligten Aufgaben auf der Seite **Lagerkommissionierung**, das automatisch auf die Lagerplätze verweist, in denen 1928-S gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="e01b3-148">John manages all involved tasks on the **Inventory Pick** page, which automatically points to the bins where 1928-S is stored.</span></span>

[!INCLUDE[set_up_location.md](includes/set_up_location.md)]

### <a name="setting-up-the-bin-codes"></a><span data-ttu-id="e01b3-149">Einrichten der Lagerplatzcodes</span><span class="sxs-lookup"><span data-stu-id="e01b3-149">Setting Up the Bin Codes</span></span>
<span data-ttu-id="e01b3-150">Nachdem Sie den Standort eingerichtet haben, müssen Sie zwei Lagerplätze hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e01b3-150">Once you have the location set up, you must add two bins.</span></span>

#### <a name="to-setup-the-bin-codes"></a><span data-ttu-id="e01b3-151">So richten Sie die Lagerplatzcodes ein</span><span class="sxs-lookup"><span data-stu-id="e01b3-151">To setup the bin codes</span></span>

1. <span data-ttu-id="e01b3-152">Wählen Sie die Aktion **Lagerplätze** aus.</span><span class="sxs-lookup"><span data-stu-id="e01b3-152">Select the **Bins** action.</span></span>
2. <span data-ttu-id="e01b3-153">Erstellen Sie zwei Lagerplätze mit den Codes *S-01-0001* und *S-01-0002*.</span><span class="sxs-lookup"><span data-stu-id="e01b3-153">Create two bins, with the codes *S-01-0001* and *S-01-0002*.</span></span>

### <a name="making-yourself-a-warehouse-employee-at-location-south"></a><span data-ttu-id="e01b3-154">Machen Sie sich selbst zum Lagermitarbeiter am Standort SÜD</span><span class="sxs-lookup"><span data-stu-id="e01b3-154">Making Yourself a Warehouse Employee at Location SOUTH</span></span>

<span data-ttu-id="e01b3-155">Um diese Funktion nutzen zu können, müssen Sie sich selbst dem Lagerort als Lagermitarbeiter hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e01b3-155">In order to use this functionality, you must add yourself to the location as a warehouse worker.</span></span> 

#### <a name="to-make-yourself-a-warehouse-employee"></a><span data-ttu-id="e01b3-156">So machen Sie sich selbst zum Lagermitarbeiter</span><span class="sxs-lookup"><span data-stu-id="e01b3-156">To make yourself a warehouse employee</span></span>

  1. <span data-ttu-id="e01b3-157">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ zum ersten Mal öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Lagermitarbeiter** ein, und wählen Sie dann den entsprechenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="e01b3-157">Choose the ![Lightbulb that opens the Tell Me feature first](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="e01b3-158">Wählen Sie das Feld **Benutzer-ID** und dann Ihr eigenes Benutzerkonto auf der Seite **Lagermitarbeiter** aus.</span><span class="sxs-lookup"><span data-stu-id="e01b3-158">Choose the **User ID** field, and select your own user account on the **Warehouse Employees** page.</span></span>
  3. <span data-ttu-id="e01b3-159">Wählen Sie im Feld **Lagerortcode** „SÜD“ aus.</span><span class="sxs-lookup"><span data-stu-id="e01b3-159">In the **Location Code** field, choose SOUTH.</span></span>  
  4. <span data-ttu-id="e01b3-160">Wählen Sie das Feld **Standard** und dann die Schaltfläche **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="e01b3-160">Select the **Default** field, and then select the **Yes** button.</span></span>  

### <a name="making-item-1928-s-available"></a><span data-ttu-id="e01b3-161">Artikel 1928-S verfügbar machen</span><span class="sxs-lookup"><span data-stu-id="e01b3-161">Making Item 1928-S Available</span></span>

<span data-ttu-id="e01b3-162">Führen Sie die folgenden Schritte aus, um den Artikel LS-1928 SÜD-Standort verfügbar zu machen:</span><span class="sxs-lookup"><span data-stu-id="e01b3-162">To make item 1928-S available at the SOUTH location follow these steps:</span></span>  

  1. <span data-ttu-id="e01b3-163">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ zum zweiten Mal öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Artikel Buch.-Blätter** ein, und wählen Sie dann den entsprechenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="e01b3-163">Choose the ![Lightbulb that opens the Tell Me feature second](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Journals**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="e01b3-164">Öffnen Sie das Standardjournal, und erstellen Sie dann zwei Artikel Buch.-Blattzeilen mit den folgenden Informationen über das Arbeitsdatum (23. Januar).</span><span class="sxs-lookup"><span data-stu-id="e01b3-164">Open the default journal, and then create two item journal lines with the following information about the work date (January 23).</span></span>  

        |<span data-ttu-id="e01b3-165">Postentyp</span><span class="sxs-lookup"><span data-stu-id="e01b3-165">Entry Type</span></span>|<span data-ttu-id="e01b3-166">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="e01b3-166">Item Number</span></span>|<span data-ttu-id="e01b3-167">Lagerortcode</span><span class="sxs-lookup"><span data-stu-id="e01b3-167">Location Code</span></span>|<span data-ttu-id="e01b3-168">Lagerplatzcode</span><span class="sxs-lookup"><span data-stu-id="e01b3-168">Bin Code</span></span>|<span data-ttu-id="e01b3-169">Menge</span><span class="sxs-lookup"><span data-stu-id="e01b3-169">Quantity</span></span>|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |<span data-ttu-id="e01b3-170">Zugang</span><span class="sxs-lookup"><span data-stu-id="e01b3-170">Positive Adjmt.</span></span>|<span data-ttu-id="e01b3-171">1928-S</span><span class="sxs-lookup"><span data-stu-id="e01b3-171">1928-S</span></span>|<span data-ttu-id="e01b3-172">SÜD</span><span class="sxs-lookup"><span data-stu-id="e01b3-172">SOUTH</span></span>|<span data-ttu-id="e01b3-173">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="e01b3-173">S-01-0001</span></span>|<span data-ttu-id="e01b3-174">20</span><span class="sxs-lookup"><span data-stu-id="e01b3-174">20</span></span>|  
        |<span data-ttu-id="e01b3-175">Zugang</span><span class="sxs-lookup"><span data-stu-id="e01b3-175">Positive Adjmt.</span></span>|<span data-ttu-id="e01b3-176">1928-S</span><span class="sxs-lookup"><span data-stu-id="e01b3-176">1928-S</span></span>|<span data-ttu-id="e01b3-177">SÜD</span><span class="sxs-lookup"><span data-stu-id="e01b3-177">SOUTH</span></span>|<span data-ttu-id="e01b3-178">S-01-0002</span><span class="sxs-lookup"><span data-stu-id="e01b3-178">S-01-0002</span></span>|<span data-ttu-id="e01b3-179">20</span><span class="sxs-lookup"><span data-stu-id="e01b3-179">20</span></span>|  

        <span data-ttu-id="e01b3-180">Das Feld **Lagerplatzcode** in den Verkaufszeilen ist standardmäßig ausgeblendet, daher müssen Sie es anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e01b3-180">By default, the **Bin Code** field on the sales lines are hidden, so you must display it.</span></span> <span data-ttu-id="e01b3-181">Dazu müssen Sie die Seite personalisieren.</span><span class="sxs-lookup"><span data-stu-id="e01b3-181">To do this you need to personalize the page.</span></span> <span data-ttu-id="e01b3-182">Weitere Informationen finden Sie unter [So starten Sie die Personalisierung einer Seite über das Banner Personalisierung](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).</span><span class="sxs-lookup"><span data-stu-id="e01b3-182">For more information, see [To start personalizing a page through the Personalizing banner](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).</span></span>

  3. <span data-ttu-id="e01b3-183">Wählen Sie **Aktionen**, dann **Buchung** und anschließend die Option **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="e01b3-183">Choose **Actions**, then **Posting**, and then choose **Post**.</span></span>  
  4. <span data-ttu-id="e01b3-184">Wählen Sie die Schaltfläche **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="e01b3-184">Select the **Yes** button.</span></span>  

## <a name="creating-the-sales-order"></a><span data-ttu-id="e01b3-185">Erstellen des Verkaufsauftrags</span><span class="sxs-lookup"><span data-stu-id="e01b3-185">Creating the Sales Order</span></span>

<span data-ttu-id="e01b3-186">Verkaufsaufträge sind die häufigste Art des ausgehenden Herkunftsbelegs.</span><span class="sxs-lookup"><span data-stu-id="e01b3-186">Sales orders are the most common type of outbound source document.</span></span>  

### <a name="to-create-the-sales-order"></a><span data-ttu-id="e01b3-187">Den Verkaufsauftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="e01b3-187">To create the sales order</span></span>

1. <span data-ttu-id="e01b3-188">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ zum dritten Mal öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den entsprechenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="e01b3-188">Choose the ![Lightbulb that opens the Tell Me feature third](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e01b3-189">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="e01b3-189">Choose the **New** action.</span></span>  
3. <span data-ttu-id="e01b3-190">Erstellen Sie einen Verkaufsauftrag für den Debitor 10000 auf das Arbeitsdatum (23. Januar) mit den folgenden Verkaufszeilen.</span><span class="sxs-lookup"><span data-stu-id="e01b3-190">Create a sales order for customer 10000 on the work date (January 23) with the following sales order line.</span></span>  

    |<span data-ttu-id="e01b3-191">Artikel</span><span class="sxs-lookup"><span data-stu-id="e01b3-191">Item</span></span>|<span data-ttu-id="e01b3-192">Lagerortcode</span><span class="sxs-lookup"><span data-stu-id="e01b3-192">Location Code</span></span>|<span data-ttu-id="e01b3-193">Menge</span><span class="sxs-lookup"><span data-stu-id="e01b3-193">Quantity</span></span>|  
    |----|-------------|--------|  
    |<span data-ttu-id="e01b3-194">1928-S</span><span class="sxs-lookup"><span data-stu-id="e01b3-194">1928-S</span></span>|<span data-ttu-id="e01b3-195">SÜD</span><span class="sxs-lookup"><span data-stu-id="e01b3-195">SOUTH</span></span>|<span data-ttu-id="e01b3-196">30</span><span class="sxs-lookup"><span data-stu-id="e01b3-196">30</span></span>|  

     <span data-ttu-id="e01b3-197">Fahren Sie fort, das Lager zu informieren, dass die Verkaufsbestellung in Lagerdurchlaufzeit bereit ist, wenn die Lieferung eingeht.</span><span class="sxs-lookup"><span data-stu-id="e01b3-197">Proceed to notify the warehouse that the sales order is ready for warehouse handling.</span></span>  

4. <span data-ttu-id="e01b3-198">Wählen Sie die Aktion **Freigabe** aus.</span><span class="sxs-lookup"><span data-stu-id="e01b3-198">Choose the **Release** action.</span></span>  

    <span data-ttu-id="e01b3-199">John fährt fort, die Verkaufsartikel zu kommissionieren und zu liefern.</span><span class="sxs-lookup"><span data-stu-id="e01b3-199">John proceeds to pick and ship the sold items.</span></span>  

## <a name="picking-and-shipping-items"></a><span data-ttu-id="e01b3-200">Kommissionierung und Versand von Artikeln</span><span class="sxs-lookup"><span data-stu-id="e01b3-200">Picking and Shipping Items</span></span>

<span data-ttu-id="e01b3-201">Auf der Seite **Lagerkommissionierung** können Sie alle ausgehenden Lageraktivitäten für einen bestimmten Herkunftsbeleg, wie einen Verkauf, verwalten.</span><span class="sxs-lookup"><span data-stu-id="e01b3-201">On the **Inventory Pick** page, you can manage all outbound warehouse activities for a specific source document, such as a sales order.</span></span> [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a><span data-ttu-id="e01b3-202">So kommissionieren Sie Artikel und liefern diese aus</span><span class="sxs-lookup"><span data-stu-id="e01b3-202">To pick and ship items</span></span>

1. <span data-ttu-id="e01b3-203">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ zum vierten Mal öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Lagerkommissionierungen** ein, und wählen Sie dann den entsprechenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="e01b3-203">Choose the ![Lightbulb that opens the Tell Me feature fourth](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Picks**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e01b3-204">Wählen Sie die Aktion **Neu**.</span><span class="sxs-lookup"><span data-stu-id="e01b3-204">Choose the **New** action.</span></span>  

    <span data-ttu-id="e01b3-205">Stellen Sie sicher, dass das Feld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="e01b3-205">Make sure that the **No.**</span></span> <span data-ttu-id="e01b3-206">auf dem Inforegister **Allgemein** ausgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="e01b3-206">field on the **General** FastTab is filled in.</span></span>
3. <span data-ttu-id="e01b3-207">Wählen Sie das Feld **Quellendokument** , und wählen Sie **Verkaufsauftrag** aus.</span><span class="sxs-lookup"><span data-stu-id="e01b3-207">Select the **Source Document** field, and then select **Sales Order**.</span></span>  
4. <span data-ttu-id="e01b3-208">Wählen Sie das Feld **Herkunftsnr.** aus, wählen Sie die Zeile für den Verkauf an Debitor 10000 aus, und wählen Sie dann die Schaltfläche **OK**.</span><span class="sxs-lookup"><span data-stu-id="e01b3-208">Select the **Source No.** field, select the line for the sale to customer 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="e01b3-209">Alternativ auf der Registerkarte Aktionen, in der Gruppe Funktion, wählen Sie **Herkunftsbeleg holen** und wählen Sie die Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="e01b3-209">Alternatively, choose the **Get Source Document** action, and then select the sales order.</span></span>  
5. <span data-ttu-id="e01b3-210">Wählen Sie die Aktion **Die zu verarbeitende Menge automatisch ausfüllen**.</span><span class="sxs-lookup"><span data-stu-id="e01b3-210">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="e01b3-211">Alternativ im Feld **Menge zu verarbeiten** geben Sie 10 und 20 jeweils auf den zwei Lagerkommissionierzeilen ein.</span><span class="sxs-lookup"><span data-stu-id="e01b3-211">Alternatively, in the **Qty. to Handle** field, enter 10 and 20 respectively on the two inventory pick lines.</span></span>  
6. <span data-ttu-id="e01b3-212">Wählen Sie die Aktion **Buchen** und **Versand** und klicken Sie anschließend auf die Schaltfläche **OK**.</span><span class="sxs-lookup"><span data-stu-id="e01b3-212">Choose the **Post** action, select **Ship**, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="e01b3-213">Die 30 Lautsprecher werden nun erfasst, wie von den Lagerplätzen S-01-0001 und S-01-0002 kommissioniert, und es wird ein negativer Artikelposten erstellt, der gebuchte Verkaufslieferung anzeigt.</span><span class="sxs-lookup"><span data-stu-id="e01b3-213">The 30 Amsterdam Lamps are now registered as picked from bins S-01-0001 and S-01-0002, and a negative item ledger entry is created reflecting the posted sales shipment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e01b3-214">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e01b3-214">See Also</span></span>

[<span data-ttu-id="e01b3-215">Artikel mit der Lagerkommissionierung kommissionieren</span><span class="sxs-lookup"><span data-stu-id="e01b3-215">Pick Items with Inventory Picks</span></span>](warehouse-how-to-pick-items-with-inventory-picks.md)  
[<span data-ttu-id="e01b3-216">Um Artikel für den Warenausgang zu kommissionieren</span><span class="sxs-lookup"><span data-stu-id="e01b3-216">Pick Items for Warehouse Shipment</span></span>](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[<span data-ttu-id="e01b3-217">Einrichten von Basislagern mit Vorgangsbereichen</span><span class="sxs-lookup"><span data-stu-id="e01b3-217">Set Up Basic Warehouses with Operations Areas</span></span>](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[<span data-ttu-id="e01b3-218">So verschieben Sie Komponenten in einen Arbeitsgangbereich in Basis-Lagerkonfigurationen</span><span class="sxs-lookup"><span data-stu-id="e01b3-218">Move Components to an Operation Area in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  
[<span data-ttu-id="e01b3-219">Kommissionierung für die Produktion oder Montage</span><span class="sxs-lookup"><span data-stu-id="e01b3-219">Pick for Production or Assembly</span></span>](warehouse-how-to-pick-for-production.md)  
[<span data-ttu-id="e01b3-220">Ad-hoc-Umlagerung von Artikeln in Basis-Lagerkonfigurationen</span><span class="sxs-lookup"><span data-stu-id="e01b3-220">Move Items Ad Hoc in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[<span data-ttu-id="e01b3-221">Designdetails: Ausgehender Lagerfluss</span><span class="sxs-lookup"><span data-stu-id="e01b3-221">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="e01b3-222">Exemplarische Vorgehensweisen für Geschäftsprozesse</span><span class="sxs-lookup"><span data-stu-id="e01b3-222">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
<span data-ttu-id="e01b3-223">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e01b3-223">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]
