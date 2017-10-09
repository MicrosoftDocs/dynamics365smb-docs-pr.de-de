---
title: 'Vorgehensweise: Versandagenten  Microsoft Docs'
description: "Sie können einen Code für jeden Zusteller anlegen und Informationen dazu eingeben."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 84a5d9eb8757dc82834c17327ffbb510cd15fa1a
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-shipping-agents"></a><span data-ttu-id="6f996-103">Vorgehensweise: Zusteller einrichten</span><span class="sxs-lookup"><span data-stu-id="6f996-103">How to: Set Up Shipping Agents</span></span>
<span data-ttu-id="6f996-104">Sie können einen Code für jeden Zusteller anlegen und Informationen dazu eingeben.</span><span class="sxs-lookup"><span data-stu-id="6f996-104">You can set up a code for each of your shipping agents and enter information about them.</span></span>  

<span data-ttu-id="6f996-105">Wenn Sie eine Internetadresse des Zustellers eingeben und der Zusteller die Paketverfolgung im Internet anbietet, können Sie die Funktion zur automatischen Paketverfolgung nutzen.</span><span class="sxs-lookup"><span data-stu-id="6f996-105">If you enter an Internet address for the shipping agent, and the agent provides package tracking services on the Internet, you can use the automatic package tracking feature.</span></span> <span data-ttu-id="6f996-106">Weitere Informationen finden Sie unter [Gewusst wie: Pakete nachverfolgen](sales-how-track-packages.md)</span><span class="sxs-lookup"><span data-stu-id="6f996-106">For more information, see [How to: Track Packages](sales-how-track-packages.md).</span></span>

<span data-ttu-id="6f996-107">Wenn Sie Zusteller in Ihren Verkaufsaufträgen eingeben, können Sie auch die Transportarten bestimmen, die jeder Zusteller anbietet.</span><span class="sxs-lookup"><span data-stu-id="6f996-107">When you set up shipping agents on your sales orders, you can also specify the services that each shipping agent offers.</span></span>  
<span data-ttu-id="6f996-108">Für jeden Zusteller können Sie eine unbegrenzte Anzahl von Transportarten anlegen und Sie können für jede Transportart eine Transportzeit festlegen.</span><span class="sxs-lookup"><span data-stu-id="6f996-108">For each shipping agent, you can set up an unlimited number of services, and you can specify a shipping time for each service.</span></span>  

<span data-ttu-id="6f996-109">Wenn Sie einer Verkaufsauftragszeile eine Zusteller Transportart zugeordnet haben, wird die Transportzeit für diese Zeile in den Lieferterminzusagen berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="6f996-109">When you have assigned a shipping agent service to a sales order line, the shipping time of the service will be included in the order promising calculation, for that line.</span></span> <span data-ttu-id="6f996-110">Weitere Informationen finden Sie unter [Gewusst wie: Berechnen von Lieferterminzusagen](sales-how-to-calculate-order-promising-dates.md).</span><span class="sxs-lookup"><span data-stu-id="6f996-110">For more information, see [How to: Calculate Order Promising Dates](sales-how-to-calculate-order-promising-dates.md).</span></span>

## <a name="to-set-up-a-shipping-agent"></a><span data-ttu-id="6f996-111">So richten Sie einen Zusteller ein</span><span class="sxs-lookup"><span data-stu-id="6f996-111">To set up a shipping agent</span></span>  
1.  <span data-ttu-id="6f996-112">Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Versandagenten** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="6f996-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Shipping Agents**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="6f996-113">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="6f996-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="6f996-114">.</span><span class="sxs-lookup"><span data-stu-id="6f996-114">.</span></span>  
3.  <span data-ttu-id="6f996-115">Wählen Sie die Aktion **Zustellertransportarten**.</span><span class="sxs-lookup"><span data-stu-id="6f996-115">Choose the **Shipping Agent Services** action.</span></span>
4. <span data-ttu-id="6f996-116">In **Zustellertransportarten** füllen Sie die Felder wie notwendig aus.</span><span class="sxs-lookup"><span data-stu-id="6f996-116">In the **Shipping Agent Services**, fill in the fields as necessary.</span></span>

> [!NOTE]  
>  <span data-ttu-id="6f996-117">Wenn Sie den Zusteller in der Auftragszeile löschen, wird auch der Zusteller Transportartcode gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6f996-117">If you delete the shipping agent on the order line, the shipping agent service code is also deleted.</span></span> <span data-ttu-id="6f996-118">Der Inhalt der Felder, die zum Teil auf der Zustellertransportart basierten, wird neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="6f996-118">The contents of fields that were based in part on the shipping agent service are recalculated.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6f996-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f996-119">See Also</span></span>
<span data-ttu-id="6f996-120">[Vorgehensweise: Pakete verfolgen](sales-how-track-packages.md)  </span><span class="sxs-lookup"><span data-stu-id="6f996-120">[How to: Track Packages](sales-how-track-packages.md)  </span></span>  
[<span data-ttu-id="6f996-121">Logistik</span><span class="sxs-lookup"><span data-stu-id="6f996-121">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="6f996-122">Lagerbest</span><span class="sxs-lookup"><span data-stu-id="6f996-122">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="6f996-123">[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="6f996-123">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="6f996-124">[Montageverwaltung](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="6f996-124">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="6f996-125">Designdetails: Logistik</span><span class="sxs-lookup"><span data-stu-id="6f996-125">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="6f996-126">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6f996-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

