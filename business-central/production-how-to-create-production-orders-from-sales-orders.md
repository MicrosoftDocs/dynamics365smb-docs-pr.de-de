---
title: 'Fertigungsaufträge aus Verkaufsaufträgen zu erstellen:'
description: Sie können Fertigungsaufträge aus Verkaufsaufträgen erstellen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/28/2021
ms.author: edupont
ms.openlocfilehash: 438f4d4e1833ba607ceedb9f5d9450c0a4dbb680
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115236"
---
# <a name="create-production-orders-from-sales-orders"></a><span data-ttu-id="6e91e-103">Fertigungsaufträge aus Verkaufsaufträgen zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="6e91e-103">Create Production Orders from Sales Orders</span></span>
<span data-ttu-id="6e91e-104">In diesem Fenster können Sie direkt zum aktuellen Verkaufsauftrag einen Fertigungsauftrag erstellen.</span><span class="sxs-lookup"><span data-stu-id="6e91e-104">You can create production orders for produced items directly from sales orders.</span></span>  

## <a name="to-create-a-production-order-from-a-sales-order"></a><span data-ttu-id="6e91e-105">Fertigungsaufträge aus Verkaufsaufträgen erstellen</span><span class="sxs-lookup"><span data-stu-id="6e91e-105">To create a production order from a sales order</span></span>  

1.  <span data-ttu-id="6e91e-106">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den entsprechenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="6e91e-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="6e91e-107">Wählen Sie den Verkaufsauftrag, für den Sie einen Fertigungsauftrag erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="6e91e-107">Select the sales order you want to create a production order for.</span></span>  
3.  <span data-ttu-id="6e91e-108">Wählen Sie die Aktion **Planung** aus.</span><span class="sxs-lookup"><span data-stu-id="6e91e-108">Choose the **Planning** action.</span></span> <span data-ttu-id="6e91e-109">Auf der Seite **Verkaufsauftragsplanung** können Sie die Verfügbarkeit des Verkaufsauftragsartikels anzeigen.</span><span class="sxs-lookup"><span data-stu-id="6e91e-109">On the **Sales Order Planning** page, you can view the availability of the sales order item.</span></span>  
4.  <span data-ttu-id="6e91e-110">Wählen Sie die Aktion **Produktionsauftrag erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="6e91e-110">Choose the **Create Prod. Order** action.</span></span>  
5.  <span data-ttu-id="6e91e-111">Wählen Sie den Status und die Auftragsart aus.</span><span class="sxs-lookup"><span data-stu-id="6e91e-111">Select the status and order type.</span></span>  
6.  <span data-ttu-id="6e91e-112">Wählen Sie die Schaltfläche **Ja** aus, um einen oder mehrere Produktionsaufträge für die Zeilen zu erstellen, die **Fertigungsauftrag** im Feld **Beschaffungsmethode** haben.</span><span class="sxs-lookup"><span data-stu-id="6e91e-112">Choose the **Yes** button to create one or more production orders for the lines that have **Prod. Order** in their **Replenishment System** field.</span></span>


> [!NOTE]  
> <span data-ttu-id="6e91e-113">Bedarfszeilen im erstellten Produktionsauftrag, die **Prod. Auftrag** im Feld **Beschaffungsmethode** haben, stellen zugrunde liegende Fertigungsaufträge dar.</span><span class="sxs-lookup"><span data-stu-id="6e91e-113">Demand lines in the created production order that have **Prod. Order** in their **Replenishment System** field represent underlying production orders.</span></span> <span data-ttu-id="6e91e-114">Denken Sie daran, dass Sie nach der Erstellung dieser Fertigungsaufträge sämtliche nicht befriedigte Nachfrage nach Komponenten für diese auf der Seite **Auftragsplanung** oder mit der Funktion **Neu planen** aus erstellten Bestellungen identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6e91e-114">After you have generated these production orders, remember to identify any unfulfilled component demand for them using the **Order Planning** page or the **Replan** function from created orders.</span></span> 

## <a name="order-type"></a><span data-ttu-id="6e91e-115">Auftragsart</span><span class="sxs-lookup"><span data-stu-id="6e91e-115">Order type</span></span>  
<span data-ttu-id="6e91e-116">Sie können zwischen zwei Methoden zur Erstellung von Produktionsaufträgen auswählen, wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6e91e-116">You can choose between two ways to create the production orders as outlined in the following table.</span></span>

|<span data-ttu-id="6e91e-117">Option</span><span class="sxs-lookup"><span data-stu-id="6e91e-117">Option</span></span>|<span data-ttu-id="6e91e-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e91e-118">Description</span></span>|
|------|-----------|
|<span data-ttu-id="6e91e-119">Artikelauftrag</span><span class="sxs-lookup"><span data-stu-id="6e91e-119">Item Order</span></span>|<span data-ttu-id="6e91e-120">Ein Fertigungsauftrag wird für jeden erforderlichen Fertigungsauftrag erstellt, der durch eine Zeile im Fenster **Verkaufsauftragsplanung** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6e91e-120">One production order is created for each needed production order that is represented by a line in the **Sales Order Planning** window.</span></span>|
|<span data-ttu-id="6e91e-121">Projektauftrag</span><span class="sxs-lookup"><span data-stu-id="6e91e-121">Project Order</span></span>|<span data-ttu-id="6e91e-122">Ein Fertigungsauftrag wird für alle erforderlichen Fertigungsaufträge erstellt, die durch Zeilen im Fenster **Verkaufsauftragsplanung** angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6e91e-122">One production order is created for all needed production orders order that are represented by lines in the **Sales Order Planning** window.</span></span> |

<span data-ttu-id="6e91e-123">Wenn Sie Projektaufträge verwenden, enthält das Feld **Herkunftsart** des Fertigungsauftrags einen **Verkaufskopf** und der Auftrag besteht aus mehreren Zeilen, eine pro zu fertigenden Verkaufszeilenartikel.</span><span class="sxs-lookup"><span data-stu-id="6e91e-123">When you use project orders, the **Source Type** field of the production order contains **Sales Header** and the order has multiple lines, one for each sales line item that must be produced.</span></span>  


## <a name="see-also"></a><span data-ttu-id="6e91e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e91e-124">See Also</span></span>  
[<span data-ttu-id="6e91e-125">Produktion einrichten</span><span class="sxs-lookup"><span data-stu-id="6e91e-125">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="6e91e-126">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="6e91e-126">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="6e91e-127">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="6e91e-127">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="6e91e-128">Einkauf</span><span class="sxs-lookup"><span data-stu-id="6e91e-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="6e91e-129">[Designdetails: Beschaffungsplanung](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="6e91e-129">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="6e91e-130">Bewährte Einrichtungsmethoden: Beschaffungsplanung</span><span class="sxs-lookup"><span data-stu-id="6e91e-130">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="6e91e-131">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6e91e-131">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]
