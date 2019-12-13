---
title: 'Vorgehensweise: Versandagentenmethoden einrichten in | Microsoft Docs'
description: Sie können eine Code für jede einzelne angebotene Versandmethode einrichten, wie auch die Informationen dazu angeben und die Informationen dazu eingeben.e können Sie einen Code für jeden Zusteller anlegen und Informationen dazu eingeben.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 75a3e689083e64f446e84b2bc3b1d26961e3d898
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2877543"
---
# <a name="set-up-shipment-methods"></a><span data-ttu-id="36afe-103">Liefermethoden einrichten</span><span class="sxs-lookup"><span data-stu-id="36afe-103">Set Up Shipment Methods</span></span>
<span data-ttu-id="36afe-104">Versandmethoden nennt man auch Incoterms; sie hängen oft ab vom Artikel, den Debitoren und den Kreditoren</span><span class="sxs-lookup"><span data-stu-id="36afe-104">Shipment methods, also called incoterms, often depend on the items, the customers, and the vendors.</span></span> <span data-ttu-id="36afe-105">Wenn der Debitor beispielsweise auf einer Insel lebt, kann er entscheiden, die Artikel immer auf dem Luftweg oder immer auf dem Seeweg geliefert zu bekommen.</span><span class="sxs-lookup"><span data-stu-id="36afe-105">For example, if the customer lives on an island, they can choose to have items always shipped by air or always by sea.</span></span> <span data-ttu-id="36afe-106">Einige Debitoren möglicherweise eine Lieferung am nächsten Tag.</span><span class="sxs-lookup"><span data-stu-id="36afe-106">Some customers may require next day delivery.</span></span> <span data-ttu-id="36afe-107">Einige möchten vielleicht den Auftrag abholen.</span><span class="sxs-lookup"><span data-stu-id="36afe-107">Some may want to pick up the order.</span></span> <span data-ttu-id="36afe-108">Sie können auf den Debitoren- und Kreditorenkarten angeben, welche Lieferart gewünscht ist.</span><span class="sxs-lookup"><span data-stu-id="36afe-108">On the customer and vendor cards, you can specify what sort of delivery is desired.</span></span>

<span data-ttu-id="36afe-109">In der Tabelle **Lieferbedingung** richten Sie die Beschreibung und den Code für jede Lieferbedingung ein.</span><span class="sxs-lookup"><span data-stu-id="36afe-109">You set up the description and code for each shipment method on the **Shipment Methods** page.</span></span> <span data-ttu-id="36afe-110">Sie können z. B. den Code "FOB" einrichten und im Feld **Beschreibung** können Sie "Frei an Bord" eingeben.</span><span class="sxs-lookup"><span data-stu-id="36afe-110">For example, you can set up the code FOB, and enter Free on Board in the **Description** field.</span></span> <span data-ttu-id="36afe-111">Sie können dann den Code im Feld **Versandmethodencode** an anderer Stelle in der Anwendung eingeben, z. B. auf der Debitorenkarte.</span><span class="sxs-lookup"><span data-stu-id="36afe-111">You can then enter the code in **Shipment Method Code** fields elsewhere in the system, such as on a customer card.</span></span> <span data-ttu-id="36afe-112">Wenn Sie dann neue Aufträge, Bestellungen, Rechnungen oder Gutschriften erstellen oder buchen, wird das System die Beschreibung einfügen, die zu dem Code gehört.</span><span class="sxs-lookup"><span data-stu-id="36afe-112">Then when you create new orders, invoices, credit memos, and so on, the system will enter the description represented by the code.</span></span> <span data-ttu-id="36afe-113">Sie können die Standardbeträge auf dem Beleg je nach Anforderung ändern.</span><span class="sxs-lookup"><span data-stu-id="36afe-113">You can change it on the document as needed.</span></span>

## <a name="to-set-up-a-shipment-code"></a><span data-ttu-id="36afe-114">So richten Sie einen Verandcode ein</span><span class="sxs-lookup"><span data-stu-id="36afe-114">To set up a shipment code</span></span>
1. <span data-ttu-id="36afe-115">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Lieferbedingungen** ein, und wählen Sie dann den zugehörigen Link.</span><span class="sxs-lookup"><span data-stu-id="36afe-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shipment Methods**, and then choose the related link.</span></span>
2. <span data-ttu-id="36afe-116">Wählen Sie auf der Seite **Versandmethode** die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="36afe-116">On the **Shipment Methods** page, choose the **New** action.</span></span>
3. <span data-ttu-id="36afe-117">Geben Sie in der neuen Zeile einen Code und eine Beschreibung für die Lieferbedingung an.</span><span class="sxs-lookup"><span data-stu-id="36afe-117">On the new line, specify a code and description for the shipment method.</span></span>

## <a name="see-also"></a><span data-ttu-id="36afe-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36afe-118">See Also</span></span>
[<span data-ttu-id="36afe-119">Incoterms</span><span class="sxs-lookup"><span data-stu-id="36afe-119">Incoterms</span></span>](https://iccwbo.org/resources-for-business/incoterms-rules)  
[<span data-ttu-id="36afe-120">Zusteller einrichten</span><span class="sxs-lookup"><span data-stu-id="36afe-120">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)  
<span data-ttu-id="36afe-121">[Um Pakete zu verfolgen](sales-how-track-packages.md)  </span><span class="sxs-lookup"><span data-stu-id="36afe-121">[Track Packages](sales-how-track-packages.md)  </span></span>  
[<span data-ttu-id="36afe-122">Logistik</span><span class="sxs-lookup"><span data-stu-id="36afe-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="36afe-123">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="36afe-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="36afe-124">[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="36afe-124">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="36afe-125">[Montageverwaltung](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="36afe-125">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="36afe-126">Designdetails: Lagerverwaltung</span><span class="sxs-lookup"><span data-stu-id="36afe-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="36afe-127">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="36afe-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
