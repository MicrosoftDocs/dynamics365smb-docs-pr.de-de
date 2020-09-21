---
title: 'Vorgehensweise: Komponenten entsprechend dem Arbeitsgangs-Ausstoß leeren | Microsoft Docs'
description: Für Artikel, die mit der Rückwärtsbuchungsmethode erstellt wurden, ist das Standardverhalten, Komponentenverbrauch zu berechnen und zu buchen, wenn Sie den Status eines freigegebenen Fertigungsauftrags in **Erledigt** ändern. Weitere Informationen finden Sie unter Entnahmemethoden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: d895ede7ec603b1f4892b1aacb2683f6ace11233
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3779762"
---
# <a name="flush-components-according-to-operation-output"></a><span data-ttu-id="cb1b5-104">Komponenten entsprechend dem Arbeitsgangs-Ausstoß leeren</span><span class="sxs-lookup"><span data-stu-id="cb1b5-104">Flush Components According to Operation Output</span></span>
<span data-ttu-id="cb1b5-105">Für Artikel, die mit der Rückwärtsbuchungsmethode erstellt wurden, ist das Standardverhalten, Komponentenverbrauch zu berechnen und zu buchen, wenn Sie den Status eines freigegebenen Fertigungsauftrags in **Erledigt** ändern.</span><span class="sxs-lookup"><span data-stu-id="cb1b5-105">For items that are set up with backward flushing method, the default behavior is to calculate and post component consumption when you change the status of a released production order to **Finished**.</span></span>  

<span data-ttu-id="cb1b5-106">Wenn Sie auch Verbindungscodes definieren, dann erfolgt die Berechnung und Buchung, wenn jeder Arbeitsgang beendet ist, und die Menge, die tatsächlich im Arbeitsgang verbraucht wurde, wird gebucht.</span><span class="sxs-lookup"><span data-stu-id="cb1b5-106">If you also define routing link codes, then calculation and posting occurs when each operation is finished, and the quantity that was actually consumed in the operation is posted.</span></span> <span data-ttu-id="cb1b5-107">Weitere Informationen finden Sie unter [Arbeitspläne erstellen](production-how-to-create-routings.md).</span><span class="sxs-lookup"><span data-stu-id="cb1b5-107">For more information, see [Create Routings](production-how-to-create-routings.md).</span></span>  

<span data-ttu-id="cb1b5-108">Wenn beispielsweise ein Fertigungsauftrag, 800 Meter zu produzieren, 8 Kilogramm einer Komponente benötigt, dann werden, wenn Sie 200 Meter buchen, wie ausgegeben, 2 Kilogramm automatisch als Verbrauch gebucht.</span><span class="sxs-lookup"><span data-stu-id="cb1b5-108">For example, if a production order to produce 800 meters requires 8 kg of a component, then when you post 200 meters as output, 2 kg are automatically posted as consumption.</span></span>  

<span data-ttu-id="cb1b5-109">Diese Funktionalität ist aus folgenden Ursachen nützlich:</span><span class="sxs-lookup"><span data-stu-id="cb1b5-109">This functionality is useful for the following reasons:</span></span>  

-   <span data-ttu-id="cb1b5-110">**Bestandsbewertung** - Wertposten für Istmeldungen und Verbräuche werden beim Fortschritt des Fertigungsauftrags erstellt.</span><span class="sxs-lookup"><span data-stu-id="cb1b5-110">**Inventory Valuation** - Value entries for output and consumption are created in parallel as the production order progresses.</span></span> <span data-ttu-id="cb1b5-111">Ohne Verbindungscodes erhöht sich der Lagerwert, wenn Ausstoß registriert wird, und vermindert sich später, wenn der Wert des Komponentenverbrauchs zusammen mit dem beendeten FA gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="cb1b5-111">Without routing link codes, the inventory value will increase as output is posted and then decrease at a later point in time when the value of component consumption is posted together with the finished production order.</span></span>  
-   <span data-ttu-id="cb1b5-112">**Bestandsverfügbarkeit** - mit allmählicher Verbrauchsbuchung, wird die Verfügbarkeit von Komponenten aktueller, was wichtig ist, um die interne Balance zwischen Bedarf und Vorrat aufrechtzuerhalten.</span><span class="sxs-lookup"><span data-stu-id="cb1b5-112">**Inventory Availability** - With gradual consumption posting, the availability of component items is more up-to-date, which is important to maintain the internal balance between demand and supply.</span></span> <span data-ttu-id="cb1b5-113">Ohne Verbindungscodenummern glauben möglicherweise andere, die Bedarf für die Komponente haben, dass sie verfügbar ist, solange eine verzögerte Verbrauchsbuchung dafür aussteht.</span><span class="sxs-lookup"><span data-stu-id="cb1b5-113">Without routing link codes, other demands for the component may believe that it is available as long as it is pending a delayed consumption posting.</span></span>  
-   <span data-ttu-id="cb1b5-114">**Just-In-Time** - mit der Möglichkeit, Produkte an Debitorenanfragen anzupassen, können Sie Abfall minimieren, indem Sie sicherstellen, dass Arbeits- und Systemänderungen nur eintreten, wenn es erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="cb1b5-114">**Just-in-Time** – With the ability to customize products to customer requests, you can minimize waste by making sure that work and system changes only occur when it is necessary.</span></span>  

<span data-ttu-id="cb1b5-115">Im folgenden Verfahren wird gezeigt, wie Rückwärtsbuchen und die Verbindungscodes kombiniert werden, sodass die Menge, die je Arbeitsgang geleert wird, zur aktuellen Isteffektivität des abgeschlossenen Arbeitsgangs proportional ist.</span><span class="sxs-lookup"><span data-stu-id="cb1b5-115">The following procedure shows how to combine backward flushing and routing link codes so that the quantity that is flushed for each operation is proportional to the actual output of the finished operation.</span></span>  

## <a name="to-flush-components-according-to-operation-output"></a><span data-ttu-id="cb1b5-116">Komponenten entsprechend dem Arbeitsgangs-Ausstoß leeren</span><span class="sxs-lookup"><span data-stu-id="cb1b5-116">To flush components according to operation output</span></span>  
1.  <span data-ttu-id="cb1b5-117">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Elemente** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="cb1b5-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="cb1b5-118">Wählen Sie die Aktion **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="cb1b5-118">Choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="cb1b5-119">Wählen Sie im Inforegister **Beschaffung** im Feld **Buchungsmethode** die Option **Vorwärts** aus.</span><span class="sxs-lookup"><span data-stu-id="cb1b5-119">On the **Replenishment** FastTab, in the **Flushing Method** field, select **Forward**.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="cb1b5-120">Wählen Sie **Kommiss. + Vorwärts** aus, wenn die Komponente in einem Lagerplatz verwendet wird, der für die gesteuerte Einlagerung und Kommissionierung eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="cb1b5-120">Select **Pick+ Forward** if the component is used in a location that is set up for directed put-away and pick.</span></span>  

4.  <span data-ttu-id="cb1b5-121">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Routings** ein, und wählen Sie dann den zugehörigen Link.</span><span class="sxs-lookup"><span data-stu-id="cb1b5-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Routings**, and then choose the related link.</span></span>  
5.  <span data-ttu-id="cb1b5-122">Definieren Sie Verbindungscodes für jeden Arbeitsgang, der die Komponente verbraucht.</span><span class="sxs-lookup"><span data-stu-id="cb1b5-122">Define routing link codes for every operation that consumes the component.</span></span> <span data-ttu-id="cb1b5-123">Weitere Informationen finden Sie unter [Arbeitspläne erstellen ](production-how-to-create-routings.md).</span><span class="sxs-lookup"><span data-stu-id="cb1b5-123">For more information, see [Create Routings ](production-how-to-create-routings.md).</span></span>  
6.  <span data-ttu-id="cb1b5-124">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Fertigungsstückliste** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="cb1b5-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Production BOM**, and then choose the related link.</span></span>  
7.  <span data-ttu-id="cb1b5-125">Definieren Sie Verbindungscodes von jeder Instanz der Komponente zu dem Arbeitsgang, in dem sie verbraucht wird.</span><span class="sxs-lookup"><span data-stu-id="cb1b5-125">Define routing link codes from each instance of the component to the operation where it is consumed.</span></span>

    > [!IMPORTANT]  
    >  <span data-ttu-id="cb1b5-126">Die Komponente muss eine Verbindung zum letzten Arbeitsgang im Arbeitsplan haben.</span><span class="sxs-lookup"><span data-stu-id="cb1b5-126">The component must have a routing link to the last operation in the routing.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cb1b5-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb1b5-127">See Also</span></span>  
[<span data-ttu-id="cb1b5-128">Fertigungsauftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="cb1b5-128">Create Production BOMs</span></span>](production-how-to-create-production-boms.md)  
[<span data-ttu-id="cb1b5-129">Produktion einrichten</span><span class="sxs-lookup"><span data-stu-id="cb1b5-129">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="cb1b5-130">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="cb1b5-130">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="cb1b5-131">[Planung](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="cb1b5-131">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="cb1b5-132">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="cb1b5-132">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="cb1b5-133">Einkauf</span><span class="sxs-lookup"><span data-stu-id="cb1b5-133">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="cb1b5-134">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cb1b5-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
