---
title: "So geht's: Eingehende Lagerhaltungseinheiten einrichten| Microsoft Docs"
description: Sie können Lagerhaltungsdaten verwenden, um Informationen über Ihre Artikel für einen bestimmten Lagerortcode und/oder einen bestimmten Variantencode zu speichern.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4136cdb7dd89e2998a3fe0e8107dd82b3ab40619
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393049"
---
# <a name="set-up-stockkeeping-units"></a><span data-ttu-id="1e20a-103">Lagerhaltungsdaten einrichten</span><span class="sxs-lookup"><span data-stu-id="1e20a-103">Set Up Stockkeeping Units</span></span>
<span data-ttu-id="1e20a-104">Sie können Lagerhaltungsdaten verwenden, um Informationen über Ihre Artikel für einen bestimmten Lagerortcode und/oder einen bestimmten Variantencode zu speichern.</span><span class="sxs-lookup"><span data-stu-id="1e20a-104">You can use stockkeeping units to record information about your items for a specific location or a specific variant code.</span></span>  

 <span data-ttu-id="1e20a-105">Lagerhaltungsdaten sind eine Ergänzung zu Artikelkarten.</span><span class="sxs-lookup"><span data-stu-id="1e20a-105">Stockkeeping units are a supplement to item cards.</span></span> <span data-ttu-id="1e20a-106">Sie ersetzen sie nicht, obwohl sie mit ihnen verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="1e20a-106">They do not replace them, although they are related to them.</span></span> <span data-ttu-id="1e20a-107">Lagerhaltungsdaten ermöglichen Ihnen, Informationen über Artikel nach Lagerorten (wie z. B. Lagerhäuser und Vertriebsstellen) oder Varianten (wie z. B. unterschiedliche Regalnummern oder Informationen zur Wiederbestellung) zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="1e20a-107">Stockkeeping units allow you to differentiate information about an item for a specific location, such as a warehouse or distribution center, or a specific variant, such as different shelf numbers and different replenishment information, for the same item.</span></span>  

## <a name="to-set-up-a-stockkeeping-unit"></a><span data-ttu-id="1e20a-108">Lagerhaltungsdaten einrichten:</span><span class="sxs-lookup"><span data-stu-id="1e20a-108">To set up a stockkeeping unit</span></span>  

1.  <span data-ttu-id="1e20a-109">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Lagermengeneinheiten** ein, und wählen Sie dann den zugehörigen Link.</span><span class="sxs-lookup"><span data-stu-id="1e20a-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Stockkeeping Units**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1e20a-110">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="1e20a-110">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="1e20a-111">Füllen Sie die Felder der Karte aus.</span><span class="sxs-lookup"><span data-stu-id="1e20a-111">Fill in the fields on the card.</span></span> <span data-ttu-id="1e20a-112">Die folgenden Felder sind obligatorisch: **Artikelnr.**, **Lagerortcode** und/oder **Variantencode**.</span><span class="sxs-lookup"><span data-stu-id="1e20a-112">The following fields are required: **Item No.**, **Location Code**, and/or **Variant Code**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

<span data-ttu-id="1e20a-113">Nachdem Sie die ersten Lagerhaltungsdaten für einen Artikel eingerichtet haben, ist das Feld **Lagerhaltungsdaten vorhanden** auf der **Artikel**-Karte ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="1e20a-113">When you have set up the first stockkeeping unit for an item, the **Stockkeeping Unit Exists** check box on the **Item** card is selected.</span></span>  

<span data-ttu-id="1e20a-114">Um mehrere Lagerhaltungsdaten für einen Artikel anzulegen, verwenden Sie die Stapelverarbeitung **Lagerhaltungsdaten erstellen**.</span><span class="sxs-lookup"><span data-stu-id="1e20a-114">To create several stockkeeping units for an item, use the **Create Stockkeeping Unit** batch job.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="1e20a-115">Die Informationen auf der **Lagerhaltungsdatenkarte** haben eine höhere Priorität als die auf der **Artikelkarte**.</span><span class="sxs-lookup"><span data-stu-id="1e20a-115">The information on the **Stockkeeping Unit** card has priority over the **Item** card.</span></span>

> [!Warning]
> <span data-ttu-id="1e20a-116">Wenn die Lagerhaltungsdaten nach Produktion angegeben sind, wird dieses Feld **Standardkosten** nicht verwendet, wenn die Ist-Kosten des gefertigten Artikels fakturiert und reguliert werden.</span><span class="sxs-lookup"><span data-stu-id="1e20a-116">If the SKU is supplied through production, then the **Standard Cost** field is not used when invoicing and adjusting the actual cost of the produced item.</span></span> <span data-ttu-id="1e20a-117">Stattdessen wird das Feld **Standardkosten** in der zugrunde liegenden Artikelkarte verwendet, und auftretende Abweichungen werden anhand der Kostenanteile dieses Artikels berechnet.</span><span class="sxs-lookup"><span data-stu-id="1e20a-117">Instead, the **Standard Cost** field on the underlying item card is used, and any variances are calculated against the cost shares of that item.</span></span><br /><br />
> <span data-ttu-id="1e20a-118">Da Fertigungsstücklisten und Arbeitspläne nicht Lagerhaltungsdaten zugeordnet werden können, sind der Einstandspreis-Roll-up und die entsprechende Berechnung von Kosten für Lagerhaltungsdaten ebenfalls nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1e20a-118">Because production BOMs and routing cannot be assigned to SKUs, then the unit cost roll-up and the related calculation of cost shares are also not available on SKUs.</span></span> <span data-ttu-id="1e20a-119">Weitere Informationen finden Sie unter [Über das Berechnen von festen Einstandspreisen](finance-about-calculating-standard-cost.md).</span><span class="sxs-lookup"><span data-stu-id="1e20a-119">For more information, see [About Calculating Standard Cost](finance-about-calculating-standard-cost.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="1e20a-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e20a-120">See Also</span></span>  
[<span data-ttu-id="1e20a-121">Neue Artikel registrieren</span><span class="sxs-lookup"><span data-stu-id="1e20a-121">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="1e20a-122">Lagerortverwaltung einrichten</span><span class="sxs-lookup"><span data-stu-id="1e20a-122">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="1e20a-123">Logistik</span><span class="sxs-lookup"><span data-stu-id="1e20a-123">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="1e20a-124">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="1e20a-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="1e20a-125">[Montageverwaltung](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="1e20a-125">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="1e20a-126">Designdetails: Lagerverwaltung</span><span class="sxs-lookup"><span data-stu-id="1e20a-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="1e20a-127">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1e20a-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]