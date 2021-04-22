---
title: Lieferbedingungen einrichten
description: Sie können eine Code für jede einzelne angebotene Lieferbedingungen einrichten, wie auch die Informationen dazu angeben und die Informationen dazu eingeben.e können Sie einen Code für jeden Zusteller anlegen und Informationen dazu eingeben.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8390c95083eb02c208e97f0309a725e8ec4d7730
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778572"
---
# <a name="set-up-shipment-methods"></a><span data-ttu-id="44ae5-103">Lieferbedingungen einrichten</span><span class="sxs-lookup"><span data-stu-id="44ae5-103">Set Up Shipment Methods</span></span>

<span data-ttu-id="44ae5-104">Lieferbedingungen hängen häufig von den Debitoren, Kreditoren und den Artikeln ab.</span><span class="sxs-lookup"><span data-stu-id="44ae5-104">Shipment methods often depend on the items, the customers, and the vendors.</span></span> <span data-ttu-id="44ae5-105">Wenn der Debitor beispielsweise auf einer Insel lebt, kann er entscheiden, die Artikel immer auf dem Luftweg oder immer auf dem Seeweg geliefert zu bekommen.</span><span class="sxs-lookup"><span data-stu-id="44ae5-105">For example, if the customer lives on an island, they can choose to have items always shipped by air or always by sea.</span></span> <span data-ttu-id="44ae5-106">Einige Debitoren möglicherweise eine Lieferung am nächsten Tag.</span><span class="sxs-lookup"><span data-stu-id="44ae5-106">Some customers may require next day delivery.</span></span> <span data-ttu-id="44ae5-107">Einige möchten vielleicht den Auftrag abholen.</span><span class="sxs-lookup"><span data-stu-id="44ae5-107">Some may want to pick up the order.</span></span> <span data-ttu-id="44ae5-108">Sie können auf den Debitoren- und Kreditorenkarten angeben, welche Lieferart gewünscht ist.</span><span class="sxs-lookup"><span data-stu-id="44ae5-108">On the customer and vendor cards, you can specify what sort of delivery is desired.</span></span>

<span data-ttu-id="44ae5-109">In der Tabelle **Lieferbedingungen** richten Sie die Beschreibung und den Code für jede Lieferbedingung ein.</span><span class="sxs-lookup"><span data-stu-id="44ae5-109">You set up the description and code for each shipment method on the **Shipment Methods** page.</span></span> <span data-ttu-id="44ae5-110">Sie können z. B. den Code "FOB" einrichten und im Feld **Beschreibung** können Sie "Frei an Bord" eingeben.</span><span class="sxs-lookup"><span data-stu-id="44ae5-110">For example, you can set up the code FOB, and enter Free on Board in the **Description** field.</span></span> <span data-ttu-id="44ae5-111">Sie können dann den Code im Feld **Lieferbedingungscode** an anderer Stelle in der Anwendung eingeben, z. B. auf der Debitorenkarte.</span><span class="sxs-lookup"><span data-stu-id="44ae5-111">You can then enter the code in **Shipment Method Code** fields elsewhere in the system, such as on a customer card.</span></span> <span data-ttu-id="44ae5-112">Wenn Sie dann neue Aufträge, Bestellungen, Rechnungen oder Gutschriften erstellen oder buchen, wird das System die Beschreibung einfügen, die zu dem Code gehört.</span><span class="sxs-lookup"><span data-stu-id="44ae5-112">Then when you create new orders, invoices, credit memos, and so on, the system will enter the description represented by the code.</span></span> <span data-ttu-id="44ae5-113">Sie können die Standardbeträge auf dem Beleg je nach Anforderung ändern.</span><span class="sxs-lookup"><span data-stu-id="44ae5-113">You can change it on the document as needed.</span></span>

## <a name="to-set-up-a-shipment-method"></a><span data-ttu-id="44ae5-114">So richten Sie eine Lieferbedingung ein</span><span class="sxs-lookup"><span data-stu-id="44ae5-114">To set up a shipment method</span></span>

1. <span data-ttu-id="44ae5-115">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Lieferbedingungen** ein, und wählen Sie dann den zugehörigen Link.</span><span class="sxs-lookup"><span data-stu-id="44ae5-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shipment Methods**, and then choose the related link.</span></span>
2. <span data-ttu-id="44ae5-116">Wählen Sie auf der Seite **Lieferbedingungen** die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="44ae5-116">On the **Shipment Methods** page, choose the **New** action.</span></span>
3. <span data-ttu-id="44ae5-117">Geben Sie in der neuen Zeile einen Code und eine Beschreibung für die Lieferbedingung an.</span><span class="sxs-lookup"><span data-stu-id="44ae5-117">On the new line, specify a code and description for the shipment method.</span></span>

> [!TIP]
> <span data-ttu-id="44ae5-118">Wenn Sie Incoterms verwenden, richten Sie Versandmethoden ein, um die relevanten Incoterms-Regeln darzustellen.</span><span class="sxs-lookup"><span data-stu-id="44ae5-118">If you use Incoterms, set up shipment methods to represent the relevant Incoterms rules.</span></span>  

## <a name="see-also"></a><span data-ttu-id="44ae5-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44ae5-119">See Also</span></span>

[<span data-ttu-id="44ae5-120">Zusteller einrichten</span><span class="sxs-lookup"><span data-stu-id="44ae5-120">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)  
[<span data-ttu-id="44ae5-121">Um Pakete zu verfolgen</span><span class="sxs-lookup"><span data-stu-id="44ae5-121">Track Packages</span></span>](sales-how-track-packages.md)  
[<span data-ttu-id="44ae5-122">Logistik</span><span class="sxs-lookup"><span data-stu-id="44ae5-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="44ae5-123">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="44ae5-123">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="44ae5-124">Lagerortverwaltung einrichten</span><span class="sxs-lookup"><span data-stu-id="44ae5-124">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="44ae5-125">Montageverwaltung</span><span class="sxs-lookup"><span data-stu-id="44ae5-125">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="44ae5-126">Designdetails: Lagerverwaltung</span><span class="sxs-lookup"><span data-stu-id="44ae5-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="44ae5-127">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="44ae5-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="44ae5-128">Incoterms auf iccwbo.org</span><span class="sxs-lookup"><span data-stu-id="44ae5-128">Incoterms on iccwbo.org</span></span>](https://iccwbo.org/resources-for-business/incoterms-rules)  

[!INCLUDE[footer-include](includes/footer-banner.md)]