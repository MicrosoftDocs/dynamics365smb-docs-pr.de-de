---
title: Kommissionierung und Lieferung in Basis-Lagerkonfigurationen | Microsoft Docs
description: In Business Central können die ausgehenden Prozesse für die Komissionierung und Lieferung auf vier Arten, mit den verschiedenen Funktionen, abhängig von der Lagerkomplexitätsebene, ausgeführt werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c05456ca45b4508be0ba44acedf81997a92b56bb
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3918488"
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a><span data-ttu-id="cf420-103">Exemplarische Vorgehensweise: Kommissionierung und Lieferung in Basis-Lagerkonfigurationen</span><span class="sxs-lookup"><span data-stu-id="cf420-103">Walkthrough: Picking and Shipping in Basic Warehouse Configurations</span></span>

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]

<span data-ttu-id="cf420-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)] können die ausgehenden Prozesse für die Komissionierung und Lieferung auf vier Arten, mit den verschiedenen Funktionen, abhängig von der Lagerkomplexitätsebene, ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cf420-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the outbound processes for picking and shipping can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="cf420-105">Art</span><span class="sxs-lookup"><span data-stu-id="cf420-105">Method</span></span>|<span data-ttu-id="cf420-106">Eingangsprozess</span><span class="sxs-lookup"><span data-stu-id="cf420-106">Inbound process</span></span>|<span data-ttu-id="cf420-107">Lagerplätze</span><span class="sxs-lookup"><span data-stu-id="cf420-107">Bins</span></span>|<span data-ttu-id="cf420-108">Kommissionierungen</span><span class="sxs-lookup"><span data-stu-id="cf420-108">Picks</span></span>|<span data-ttu-id="cf420-109">Lieferungen</span><span class="sxs-lookup"><span data-stu-id="cf420-109">Shipments</span></span>|<span data-ttu-id="cf420-110">Komplexitätsebene anzeigen (siehe [Designdetails: Lagerhaus-Einrichtung](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="cf420-110">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="cf420-111">A</span><span class="sxs-lookup"><span data-stu-id="cf420-111">A</span></span>|<span data-ttu-id="cf420-112">Beitragsentnahme und -Lieferung aus der Auftragszeile</span><span class="sxs-lookup"><span data-stu-id="cf420-112">Post pick and shipment from the order line</span></span>|<span data-ttu-id="cf420-113">X</span><span class="sxs-lookup"><span data-stu-id="cf420-113">X</span></span>|||<span data-ttu-id="cf420-114">2</span><span class="sxs-lookup"><span data-stu-id="cf420-114">2</span></span>|  
|<span data-ttu-id="cf420-115">F</span><span class="sxs-lookup"><span data-stu-id="cf420-115">B</span></span>|<span data-ttu-id="cf420-116">Buchen Sie die Kommissionierung und den Warenausgang aus einem Lagerkommissionierungsbeleg</span><span class="sxs-lookup"><span data-stu-id="cf420-116">Post pick and shipment from an inventory pick document</span></span>||<span data-ttu-id="cf420-117">X</span><span class="sxs-lookup"><span data-stu-id="cf420-117">X</span></span>||<span data-ttu-id="cf420-118">3</span><span class="sxs-lookup"><span data-stu-id="cf420-118">3</span></span>|  
|<span data-ttu-id="cf420-119">L</span><span class="sxs-lookup"><span data-stu-id="cf420-119">C</span></span>|<span data-ttu-id="cf420-120">Buchen Sie die Kommissionierung und den Warenausgang aus einem Warenausgangsbeleg</span><span class="sxs-lookup"><span data-stu-id="cf420-120">Post pick and shipment from a warehouse shipment document</span></span>|||<span data-ttu-id="cf420-121">X</span><span class="sxs-lookup"><span data-stu-id="cf420-121">X</span></span>|<span data-ttu-id="cf420-122">4/5/6</span><span class="sxs-lookup"><span data-stu-id="cf420-122">4/5/6</span></span>|  
|<span data-ttu-id="cf420-123">T</span><span class="sxs-lookup"><span data-stu-id="cf420-123">D</span></span>|<span data-ttu-id="cf420-124">Buchen Sie die Kommissionierung von einem Kommissionierbeleg und buchen Sie den Warenausgang aus einem Warenausgangsbeleg</span><span class="sxs-lookup"><span data-stu-id="cf420-124">Post pick from a warehouse pick document and post shipment from a warehouse shipment document</span></span>||<span data-ttu-id="cf420-125">X</span><span class="sxs-lookup"><span data-stu-id="cf420-125">X</span></span>|<span data-ttu-id="cf420-126">X</span><span class="sxs-lookup"><span data-stu-id="cf420-126">X</span></span>|<span data-ttu-id="cf420-127">4/5/6</span><span class="sxs-lookup"><span data-stu-id="cf420-127">4/5/6</span></span>|  

<span data-ttu-id="cf420-128">Weitere Informationen finden Sie unter [Designdetails: Ausgehender Lagerfluss](design-details-outbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="cf420-128">For more information, see [Design Details: Outbound Warehouse Flow](design-details-outbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="cf420-129">In der folgenden Vorgehensweise wird Methode B in der vorhergegangenen Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cf420-129">The following walkthrough demonstrates method B in the previous table.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="cf420-130">Informationen zu dieser exemplarischen Vorgehensweise</span><span class="sxs-lookup"><span data-stu-id="cf420-130">About This Walkthrough</span></span>

<span data-ttu-id="cf420-131">Bei Basis-Lagerkonfigurationen gilt Folgendes: Wenn ein Lagerort so eingerichtet wurde, dass Kommissionierung erforderlich ist, jedoch Warenausgang nicht erforderlich ist, verwenden Sie die Seite **Lagerkommissionierung** , um Kommissionier- und Warenausgangsinformationen für Ihre Herkunftsbelege zu erfassen und zu buchen.</span><span class="sxs-lookup"><span data-stu-id="cf420-131">In basic warehouse configurations where your location is set up to require pick processing but not ship processing, you use the **Inventory Pick** page to record and post pick and ship information for your outbound source documents.</span></span> <span data-ttu-id="cf420-132">Der ausgehende Herkunftsbeleg kann ein Verkaufsauftrag, eine Einkaufsreklamation, ein ausgehender Umlagerungsauftrag, ein Fertigungsauftrag oder ein Komponentenbedarf sein.</span><span class="sxs-lookup"><span data-stu-id="cf420-132">The outbound source document can be a sales order, purchase return order, outbound transfer order, or a production order with component need.</span></span>  

<span data-ttu-id="cf420-133">In dieser exemplarischen Vorgehensweise werden folgende Aufgaben erläutert:</span><span class="sxs-lookup"><span data-stu-id="cf420-133">This walkthrough demonstrates the following tasks:</span></span>  

- <span data-ttu-id="cf420-134">Einrichtung des SILBERNEN Lagerorts für Lagerkommissionierung.</span><span class="sxs-lookup"><span data-stu-id="cf420-134">Setting up SILVER location for inventory picks.</span></span>  
- <span data-ttu-id="cf420-135">Erstellen eines Verkaufsauftrags für den Debitor 10000 für 30 Lautsprecher.</span><span class="sxs-lookup"><span data-stu-id="cf420-135">Creating a sales order for customer 10000 for 30 loudspeakers.</span></span>  
- <span data-ttu-id="cf420-136">Freigeben des Verkaufsauftrags für Lagerdurchlaufzeit.</span><span class="sxs-lookup"><span data-stu-id="cf420-136">Releasing the sales order for warehouse handling.</span></span>  
- <span data-ttu-id="cf420-137">Erstellen einer Lagerkommissionierung basierend auf einem freigegebenen Herkunftsbeleg.</span><span class="sxs-lookup"><span data-stu-id="cf420-137">Creating an inventory pick based on a released source document.</span></span>  
- <span data-ttu-id="cf420-138">Erfassen der Lagerplatzumlagerung aus dem Lager und gleichzeitig Buchen der Verkaufslieferung für den ursprünglichen Verkaufsauftrag.</span><span class="sxs-lookup"><span data-stu-id="cf420-138">Registering the warehouse movement from the warehouse and at the same time posting the sales shipment for the source sales order.</span></span>  

## <a name="roles"></a><span data-ttu-id="cf420-139">Rollen</span><span class="sxs-lookup"><span data-stu-id="cf420-139">Roles</span></span>

<span data-ttu-id="cf420-140">Die Aufgaben in dieser Demonstration werden von den folgenden Benutzerrollen ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="cf420-140">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

- <span data-ttu-id="cf420-141">Lagerortleiter</span><span class="sxs-lookup"><span data-stu-id="cf420-141">Warehouse Manager</span></span>  
- <span data-ttu-id="cf420-142">Auftragsverarbeitung</span><span class="sxs-lookup"><span data-stu-id="cf420-142">Order Processor</span></span>  
- <span data-ttu-id="cf420-143">Lagermitarbeiter</span><span class="sxs-lookup"><span data-stu-id="cf420-143">Warehouse Worker</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="cf420-144">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="cf420-144">Prerequisites</span></span>

<span data-ttu-id="cf420-145">Für diese exemplarische Vorgehensweise gelten folgende Voraussetzungen:</span><span class="sxs-lookup"><span data-stu-id="cf420-145">To complete this walkthrough, you will need:</span></span>  

- <span data-ttu-id="cf420-146">Für [!INCLUDE[prodshort](includes/prodshort.md)] Online ein Unternehmen basierend auf der Option **Erweiterte Bewertung – Vollständige Beispieldaten** in einer Sandbox-Umgebung</span><span class="sxs-lookup"><span data-stu-id="cf420-146">For [!INCLUDE[prodshort](includes/prodshort.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment.</span></span> <span data-ttu-id="cf420-147">Für [!INCLUDE[prodshort](includes/prodshort.md)] (lokal) CRONUS International Ltd. installiert</span><span class="sxs-lookup"><span data-stu-id="cf420-147">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, CRONUS International Ltd. installed.</span></span>  
- <span data-ttu-id="cf420-148">Machen Sie sich selbst zum Lagerarbeiter am Standort SILVER, indem Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="cf420-148">To make yourself a warehouse employee at the location SILVER by following these steps:</span></span>  

  1. <span data-ttu-id="cf420-149">Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Lagermitarbeiter** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="cf420-149">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees** , and then choose the related link.</span></span>  
  2. <span data-ttu-id="cf420-150">Wählen Sie das Feld **Benutzer-ID** aus, und wählen Sie Ihr eigenes Benutzerkonto auf der Seite **Benutzer** aus.</span><span class="sxs-lookup"><span data-stu-id="cf420-150">Choose the **User ID** field, and select your own user account on the **Users** page.</span></span>  
  3. <span data-ttu-id="cf420-151">Geben Sie im Feld **Lagerortcode** SILVER ein.</span><span class="sxs-lookup"><span data-stu-id="cf420-151">In the **Location Code** field, enter SILVER.</span></span>  
  4. <span data-ttu-id="cf420-152">Wählen Sie das Feld **Standard** aus.</span><span class="sxs-lookup"><span data-stu-id="cf420-152">Select the **Default** field.</span></span>  

- <span data-ttu-id="cf420-153">Stellen Sie Artikel LS-81 am SILBERNEN Lagerort bereit, indem Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="cf420-153">Make item LS-81 available at SILVER location by following these steps:</span></span>  

  1. <span data-ttu-id="cf420-154">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Artikel Buch.-Blätter** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="cf420-154">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Journals** , and then choose the related link.</span></span>  
  2. <span data-ttu-id="cf420-155">Öffnen Sie das Standardjournal, und erstellen Sie dann zwei Artikel Buch.-Blattzeilen mit den folgenden Informationen über das Arbeitsdatum (23. Januar).</span><span class="sxs-lookup"><span data-stu-id="cf420-155">Open the default journal, and then create two item journal lines with the following information about the work date (January 23).</span></span>  

        |<span data-ttu-id="cf420-156">Postentyp</span><span class="sxs-lookup"><span data-stu-id="cf420-156">Entry Type</span></span>|<span data-ttu-id="cf420-157">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="cf420-157">Item Number</span></span>|<span data-ttu-id="cf420-158">Lagerortcode</span><span class="sxs-lookup"><span data-stu-id="cf420-158">Location Code</span></span>|<span data-ttu-id="cf420-159">Lagerplatzcode</span><span class="sxs-lookup"><span data-stu-id="cf420-159">Bin Code</span></span>|<span data-ttu-id="cf420-160">Menge</span><span class="sxs-lookup"><span data-stu-id="cf420-160">Quantity</span></span>|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |<span data-ttu-id="cf420-161">Zugang</span><span class="sxs-lookup"><span data-stu-id="cf420-161">Positive Adjmt.</span></span>|<span data-ttu-id="cf420-162">LS-81</span><span class="sxs-lookup"><span data-stu-id="cf420-162">LS-81</span></span>|<span data-ttu-id="cf420-163">SILBER</span><span class="sxs-lookup"><span data-stu-id="cf420-163">SILVER</span></span>|<span data-ttu-id="cf420-164">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="cf420-164">S-01-0001</span></span>|<span data-ttu-id="cf420-165">20</span><span class="sxs-lookup"><span data-stu-id="cf420-165">20</span></span>|  
        |<span data-ttu-id="cf420-166">Zugang</span><span class="sxs-lookup"><span data-stu-id="cf420-166">Positive Adjmt.</span></span>|<span data-ttu-id="cf420-167">LS-81</span><span class="sxs-lookup"><span data-stu-id="cf420-167">LS-81</span></span>|<span data-ttu-id="cf420-168">SILBER</span><span class="sxs-lookup"><span data-stu-id="cf420-168">SILVER</span></span>|<span data-ttu-id="cf420-169">S-01-0002</span><span class="sxs-lookup"><span data-stu-id="cf420-169">S-01-0002</span></span>|<span data-ttu-id="cf420-170">20</span><span class="sxs-lookup"><span data-stu-id="cf420-170">20</span></span>|  

  3. <span data-ttu-id="cf420-171">Wählen Sie die Aktion **Beleg buchen** aus und wählen Sie dann die Schaltfläche **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="cf420-171">Choose the **Post** action, and then select the **Yes** button.</span></span>  

## <a name="story"></a><span data-ttu-id="cf420-172">Hintergrund</span><span class="sxs-lookup"><span data-stu-id="cf420-172">Story</span></span>

<span data-ttu-id="cf420-173">Ellen, die Lagermanagerin bei CRONUS, richtet das SILBER-Lager für grundlegende Komissionierungshandlung ein, in dem Lagermitarbeiter ausgehende Aufträge einzeln verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="cf420-173">Ellen, the warehouse manager at CRONUS, sets up SILVER warehouse for basic pick handling where warehouse workers process outbound orders individually.</span></span> <span data-ttu-id="cf420-174">Martha, die Verkaufsauftragsbearbeiterin, erstellt einen Verkaufsauftrag für 30 Einheiten des Artikels LS-81, die dem Debitor 10000 aus dem SILBERNEN Lager geliefert werden.</span><span class="sxs-lookup"><span data-stu-id="cf420-174">Susan, the order processor, creates a sales order for 30 units of item LS-81 to be shipped to customer 10000 from the SILVER Warehouse.</span></span> <span data-ttu-id="cf420-175">John, der Lagermitarbeiter muss sicherstellen, dass die Lieferung an den Debitor vorbereitet und geliefert wird.</span><span class="sxs-lookup"><span data-stu-id="cf420-175">John, the warehouse worker must make sure that the shipment is prepared and delivered to the customer.</span></span> <span data-ttu-id="cf420-176">John verwaltet alle beteiligten Aufgaben auf der Seite **Lagerkommissionierung** , das automatisch auf die Lagerplätze verweist, in denen LS-81 gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="cf420-176">John manages all involved tasks on the **Inventory Pick** page, which automatically points to the bins where LS-81 is stored.</span></span>  

## <a name="setting-up-the-location"></a><span data-ttu-id="cf420-177">Einrichten des Lagerorts</span><span class="sxs-lookup"><span data-stu-id="cf420-177">Setting Up the Location</span></span>

<span data-ttu-id="cf420-178">Das Einrichten der Seite **Standortkarte** definiert die Warenflüsse des Unternehmens.</span><span class="sxs-lookup"><span data-stu-id="cf420-178">The setup of the **Location Card** page defines the company’s warehouse flows.</span></span>  

### <a name="to-set-up-the-location"></a><span data-ttu-id="cf420-179">So richten Sie den Standort ein</span><span class="sxs-lookup"><span data-stu-id="cf420-179">To set up the location</span></span>

1. <span data-ttu-id="cf420-180">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Lagerorte** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="cf420-180">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations** , and then choose the related link.</span></span>  
2. <span data-ttu-id="cf420-181">Öffnen Sie die Karte für den Standort SILVER.</span><span class="sxs-lookup"><span data-stu-id="cf420-181">Open the SILVER location card.</span></span>  
3. <span data-ttu-id="cf420-182">Aktivieren Sie im Inforegister **Lager** das Kontrollkästchen **Kommissionierung erforderlich** .</span><span class="sxs-lookup"><span data-stu-id="cf420-182">On the **Warehouse** FastTab, choose the **Require Pick** check box.</span></span>  

## <a name="creating-the-sales-order"></a><span data-ttu-id="cf420-183">Erstellen des Verkaufsauftrags</span><span class="sxs-lookup"><span data-stu-id="cf420-183">Creating the Sales Order</span></span>

<span data-ttu-id="cf420-184">Verkaufsaufträge sind die häufigste Art des ausgehenden Herkunftsbelegs.</span><span class="sxs-lookup"><span data-stu-id="cf420-184">Sales orders are the most common type of outbound source document.</span></span>  

### <a name="to-create-the-sales-order"></a><span data-ttu-id="cf420-185">Den Verkaufsauftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="cf420-185">To create the sales order</span></span>

1. <span data-ttu-id="cf420-186">Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Verkaufsaufträge** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="cf420-186">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders** , and then choose the related link.</span></span>  
2. <span data-ttu-id="cf420-187">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="cf420-187">Choose the **New** action.</span></span>  
3. <span data-ttu-id="cf420-188">Erstellen Sie einen Verkaufsauftrag für den Debitor 10000 auf das Arbeitsdatum (23. Januar) mit den folgenden Verkaufszeilen.</span><span class="sxs-lookup"><span data-stu-id="cf420-188">Create a sales order for customer 10000 on the work date (January 23) with the following sales order line.</span></span>  

    |<span data-ttu-id="cf420-189">Artikel</span><span class="sxs-lookup"><span data-stu-id="cf420-189">Item</span></span>|<span data-ttu-id="cf420-190">Lagerortcode</span><span class="sxs-lookup"><span data-stu-id="cf420-190">Location Code</span></span>|<span data-ttu-id="cf420-191">Menge</span><span class="sxs-lookup"><span data-stu-id="cf420-191">Quantity</span></span>|  
    |----|-------------|--------|  
    |<span data-ttu-id="cf420-192">LS_81</span><span class="sxs-lookup"><span data-stu-id="cf420-192">LS_81</span></span>|<span data-ttu-id="cf420-193">SILBER</span><span class="sxs-lookup"><span data-stu-id="cf420-193">SILVER</span></span>|<span data-ttu-id="cf420-194">30</span><span class="sxs-lookup"><span data-stu-id="cf420-194">30</span></span>|  

     <span data-ttu-id="cf420-195">Fahren Sie fort, das Lager zu informieren, dass die Verkaufsbestellung in Lagerdurchlaufzeit bereit ist, wenn die Lieferung eingeht.</span><span class="sxs-lookup"><span data-stu-id="cf420-195">Proceed to notify the warehouse that the sales order is ready for warehouse handling.</span></span>  

4. <span data-ttu-id="cf420-196">Wählen Sie die Aktion **Freigabe** aus.</span><span class="sxs-lookup"><span data-stu-id="cf420-196">Choose the **Release** action.</span></span>  

    <span data-ttu-id="cf420-197">John fährt fort, die Verkaufsartikel zu kommissionieren und zu liefern.</span><span class="sxs-lookup"><span data-stu-id="cf420-197">John proceeds to pick and ship the sold items.</span></span>  

## <a name="picking-and-shipping-items"></a><span data-ttu-id="cf420-198">Kommissionierung und Versand von Artikeln</span><span class="sxs-lookup"><span data-stu-id="cf420-198">Picking and Shipping Items</span></span>

<span data-ttu-id="cf420-199">Auf der Seite **Lagerkommissionierung** können Sie alle ausgehenden Lageraktivitäten für einen bestimmten Herkunftsbeleg, wie einen Verkauf, verwalten.</span><span class="sxs-lookup"><span data-stu-id="cf420-199">On the **Inventory Pick** page, you can manage all outbound warehouse activities for a specific source document, such as a sales order.</span></span> [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a><span data-ttu-id="cf420-200">So kommissionieren Sie Artikel und liefern diese aus</span><span class="sxs-lookup"><span data-stu-id="cf420-200">To pick and ship items</span></span>

1. <span data-ttu-id="cf420-201">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Lagerkommissionierungen** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="cf420-201">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Picks** , and then choose the related link.</span></span>  
2. <span data-ttu-id="cf420-202">Wählen Sie die Aktion **Neu** .</span><span class="sxs-lookup"><span data-stu-id="cf420-202">Choose the **New** action.</span></span>  

    <span data-ttu-id="cf420-203">Stellen Sie sicher, dass das Feld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="cf420-203">Make sure that the **No.**</span></span> <span data-ttu-id="cf420-204">auf dem Inforegister **Allgemein** ausgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="cf420-204">field on the **General** FastTab is filled in.</span></span>
3. <span data-ttu-id="cf420-205">Wählen Sie das Feld **Quellendokument** , und wählen Sie **Verkaufsauftrag** aus.</span><span class="sxs-lookup"><span data-stu-id="cf420-205">Select the **Source Document** field, and then select **Sales Order** .</span></span>  
4. <span data-ttu-id="cf420-206">Wählen Sie das Feld **Herkunftsnr.** aus, wählen Sie die Zeile für den Verkauf an Debitor 10000 aus, und wählen Sie dann die Schaltfläche **OK** .</span><span class="sxs-lookup"><span data-stu-id="cf420-206">Select the **Source No.** field, select the line for the sale to customer 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="cf420-207">Alternativ auf der Registerkarte Aktionen, in der Gruppe Funktion, wählen Sie **Herkunftsbeleg holen** und wählen Sie die Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="cf420-207">Alternatively, choose the **Get Source Document** action, and then select the sales order.</span></span>  
5. <span data-ttu-id="cf420-208">Wählen Sie die Aktion **Die zu verarbeitende Menge automatisch ausfüllen** .</span><span class="sxs-lookup"><span data-stu-id="cf420-208">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="cf420-209">Alternativ im Feld **Menge zu verarbeiten** geben Sie 10 und 20 jeweils auf den zwei Lagerkommissionierzeilen ein.</span><span class="sxs-lookup"><span data-stu-id="cf420-209">Alternatively, in the **Qty. to Handle** field, enter 10 and 20 respectively on the two inventory pick lines.</span></span>  
6. <span data-ttu-id="cf420-210">Wählen Sie die Aktion **Buchen** und **Versand** und klicken Sie anschließend auf die Schaltfläche **OK** .</span><span class="sxs-lookup"><span data-stu-id="cf420-210">Choose the **Post** action, select **Ship** , and then choose the **OK** button.</span></span>  

    <span data-ttu-id="cf420-211">Die 30 Lautsprecher werden nun erfasst, wie von den Lagerplätzen S-01-0001 und S-01-0002 kommissioniert, und ein negativer Artikelposten wird, die gebuchte Verkaufslieferung reflektierend, erstellt.</span><span class="sxs-lookup"><span data-stu-id="cf420-211">The 30 loudspeakers are now registered as picked from bins S-01-0001 and S-01-0002, and a negative item ledger entry is created reflecting the posted sales shipment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cf420-212">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf420-212">See Also</span></span>

[<span data-ttu-id="cf420-213">Artikel mit der Lagerkommissionierung kommissionieren</span><span class="sxs-lookup"><span data-stu-id="cf420-213">Pick Items with Inventory Picks</span></span>](warehouse-how-to-pick-items-with-inventory-picks.md)  
[<span data-ttu-id="cf420-214">Um Artikel für den Warenausgang zu kommissionieren</span><span class="sxs-lookup"><span data-stu-id="cf420-214">Pick Items for Warehouse Shipment</span></span>](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[<span data-ttu-id="cf420-215">Einrichten von Basislagern mit Vorgangsbereichen</span><span class="sxs-lookup"><span data-stu-id="cf420-215">Set Up Basic Warehouses with Operations Areas</span></span>](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[<span data-ttu-id="cf420-216">So verschieben Sie Komponenten in einen Arbeitsgangbereich in Basis-Lagerkonfigurationen</span><span class="sxs-lookup"><span data-stu-id="cf420-216">Move Components to an Operation Area in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  
[<span data-ttu-id="cf420-217">Kommissionierung für die Produktion oder Montage</span><span class="sxs-lookup"><span data-stu-id="cf420-217">Pick for Production or Assembly</span></span>](warehouse-how-to-pick-for-production.md)  
[<span data-ttu-id="cf420-218">Ad-hoc-Umlagerung von Artikeln in Basis-Lagerkonfigurationen</span><span class="sxs-lookup"><span data-stu-id="cf420-218">Move Items Ad Hoc in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[<span data-ttu-id="cf420-219">Designdetails: Ausgehender Lagerfluss</span><span class="sxs-lookup"><span data-stu-id="cf420-219">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="cf420-220">Exemplarische Vorgehensweisen für Geschäftsprozesse</span><span class="sxs-lookup"><span data-stu-id="cf420-220">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
<span data-ttu-id="cf420-221">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cf420-221">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
