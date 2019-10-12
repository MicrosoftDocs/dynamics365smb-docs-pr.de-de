---
title: 'Vorgehensweise: Aufteilen von Lageraktivitätszeilen | Microsoft Docs'
description: In Einlagerungen, Lagerplatzumlagerungen oder Kommissionierungen und in Lagereinlagerungen und Lagerkommissionierungen werden Lagerplätze für das Kommissionieren oder Einlagern von Artikeln vorgeschlagen. Die tatsächliche Menge im Lagerplatz, die von der Anwendung vorgeschlagen wird, ist möglicherweise nicht ausreichend, oder in dem vorgeschlagenen Lagerplatz ist nicht genügend Platz, um die erforderliche Menge einzulagern. In diesen Fällen müssen Sie die Zeile aufteilen, so dass die Artikel für eine Zeile entweder aus mehr als einem Lagerplatz entnommen oder in mehr als einen Lagerplatz eingelagert werden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 55f0de5df8a9c4f2281af2456ffa4315560e9ea1
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2310084"
---
# <a name="split-warehouse-activity-lines"></a><span data-ttu-id="9c7bc-105">Lageraktivitätszeilen aufzuteilen</span><span class="sxs-lookup"><span data-stu-id="9c7bc-105">Split Warehouse Activity Lines</span></span>
<span data-ttu-id="9c7bc-106">In Einlagerungen, Lagerplatzumlagerungen oder Kommissionierungen und in Lagereinlagerungen und Lagerkommissionierungen werden Lagerplätze für das Kommissionieren oder Einlagern von Artikeln vorgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="9c7bc-106">In warehouse put-aways, movements, or picks, and in inventory put-aways and inventory picks, bins are suggested for the picking or putting away of items.</span></span> <span data-ttu-id="9c7bc-107">Die tatsächliche Menge im Lagerplatz, die von der Anwendung vorgeschlagen wird, ist möglicherweise nicht ausreichend, oder in dem vorgeschlagenen Lagerplatz ist nicht genügend Platz, um die erforderliche Menge einzulagern.</span><span class="sxs-lookup"><span data-stu-id="9c7bc-107">The actual quantity in the bin suggested may not be sufficient, or there is not enough room in the suggested bin to put away the required quantity.</span></span> <span data-ttu-id="9c7bc-108">In diesen Fällen müssen Sie die Zeile aufteilen, so dass die Artikel für eine Zeile entweder aus mehr als einem Lagerplatz entnommen oder in mehr als einen Lagerplatz eingelagert werden.</span><span class="sxs-lookup"><span data-stu-id="9c7bc-108">In these cases, you need to split the line, so that the items for one line are either taken from or placed into more than one bin.</span></span>  

<span data-ttu-id="9c7bc-109">Die folgende Vorgehensweise gilt für Logistikbelege, z. B. Einlagerungs-, Umlagerungs- und Kommissionierzeilen, oder Lagereinlagerungs-, Umlagerungs- und Kommissionierzeilen.</span><span class="sxs-lookup"><span data-stu-id="9c7bc-109">The following procedure applies to warehouse documents, such as warehouse put-away, movement, and pick lines, or inventory put-away, movement, and pick lines.</span></span>  

## <a name="to-split-warehouse-activity-lines"></a><span data-ttu-id="9c7bc-110">Um Lageraktivitätszeilen aufzuteilen</span><span class="sxs-lookup"><span data-stu-id="9c7bc-110">To split warehouse activity lines</span></span>  
1.  <span data-ttu-id="9c7bc-111">Öffnen Sie eine Lageraktivitätszeile, in der Sie versuchen, eine nicht ausreichende Menge zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="9c7bc-111">Open a warehouse activity line where you are trying to handle an insufficient quantity.</span></span>  
2.  <span data-ttu-id="9c7bc-112">Geben Sie im Feld **Bewegungsmenge** die reduzierte Menge ein, die Sie bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="9c7bc-112">In the **Qty. to Handle** field, enter the reduced quantity that you are able to handle.</span></span>  
3.  <span data-ttu-id="9c7bc-113">Wählen Sie im Inforegister **Zeilen** die Aktion **Aktionen**, dann die Aktion **Funktionen** und die Aktion **Zeile aufteilen** aus.</span><span class="sxs-lookup"><span data-stu-id="9c7bc-113">On the **Lines** FastTab, choose the **Actions** action, choose the **Functions** action, and then choose the **Split Line** action.</span></span> <span data-ttu-id="9c7bc-114">Eine neue Zeile wird angezeigt, bei der es sich um eine Kopie der Originalzeile handelt. Einziger Unterschied: Das Feld **Bewegungsmenge** enthält die Menge, die aus der ursprünglichen Zeile entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="9c7bc-114">A new line appears, which is a copy of the original line, except that the **Qty. to Handle** field contains the quantity that you removed from the original line.</span></span>  
4.  <span data-ttu-id="9c7bc-115">Ordnen Sie dieser neuen Zeile einen geeigneten Lagerplatz zu, und eine Zone, wenn Sie die gesteuerte Einlagerung und Kommissionierung verwenden, oder setzen Sie das Aufteilen der Zeile so lange fort, wie es erforderlich ist, um geeignete Lagerplätze für die gesamte Menge zu finden.</span><span class="sxs-lookup"><span data-stu-id="9c7bc-115">Assign an appropriate bin and, if you are using directed put-away and pick, a zone, to this new line, or continue splitting the line as necessary until you find appropriate bins for all of the quantity.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="9c7bc-116">Wenn der Lagerort die gesteuerte Einlagerung und Kommissionierung verwendet und Sie die Zeilen aufteilen, müssen Sie sich mit dem Lager auskennen und in der Lage sein, einen Lagerplatz auszuwählen, der den Lageranforderungen des Artikels und den allgemeinen Anforderungen des Logistikbelegs entspricht.</span><span class="sxs-lookup"><span data-stu-id="9c7bc-116">If the location uses directed put-away and pick and you split the lines, you must be familiar with the warehouse and be able to choose a bin that matches the storage requirements of the item and that fulfills the general requirements of the warehouse document.</span></span> <span data-ttu-id="9c7bc-117">Sie würden z. B. nicht eine Zeile eines Kommissionierbelegs aufteilen und einige der Artikel in den Palettenlagerplätzen einlagern.</span><span class="sxs-lookup"><span data-stu-id="9c7bc-117">For example, you would not split a line on a pick document and place some items in the bulk storage.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9c7bc-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c7bc-118">See Also</span></span>  
[<span data-ttu-id="9c7bc-119">Logistik</span><span class="sxs-lookup"><span data-stu-id="9c7bc-119">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="9c7bc-120">Lagerbest</span><span class="sxs-lookup"><span data-stu-id="9c7bc-120">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="9c7bc-121">[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="9c7bc-121">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="9c7bc-122">[Montageverwaltung](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="9c7bc-122">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="9c7bc-123">Designdetails: Logistik</span><span class="sxs-lookup"><span data-stu-id="9c7bc-123">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="9c7bc-124">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9c7bc-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
