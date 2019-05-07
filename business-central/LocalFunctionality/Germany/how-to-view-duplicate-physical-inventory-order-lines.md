---
title: So zeigen Sie doppelte Inventurauftragszeilen an
description: Werden Inventurauftragszeilen manuell erstellt oder automatisch erstellte Zeilen später geändert, müssen Sie darauf achten, dass keine doppelten Zeilen vorkommen. Sie haben die Möglichkeit, doppelte Inventurauftragszeilen durch die Anwendung anzeigen zu lassen.
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
redirect_url: ../../inventory-how-count-inventory-with-documents
ms.openlocfilehash: f13283f219f5913add0a267db27f44f6dfb8eba8
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "927303"
---
# <a name="view-duplicate-physical-inventory-order-lines"></a><span data-ttu-id="28bae-104">So zeigen Sie doppelte Inventurauftragszeilen an</span><span class="sxs-lookup"><span data-stu-id="28bae-104">View Duplicate Physical Inventory Order Lines</span></span>
<span data-ttu-id="28bae-105">Werden Inventurauftragszeilen manuell erstellt oder automatisch erstellte Zeilen später geändert, müssen Sie darauf achten, dass keine doppelten Zeilen vorkommen.</span><span class="sxs-lookup"><span data-stu-id="28bae-105">If you create physical inventory order lines manually, or if you change automatically created lines, you must make sure that there are no duplicate lines.</span></span> <span data-ttu-id="28bae-106">Sie haben die Möglichkeit, doppelte Inventurauftragszeilen durch die Anwendung anzeigen zu lassen.</span><span class="sxs-lookup"><span data-stu-id="28bae-106">You can create a list of duplicate physical inventory order lines.</span></span>  

<span data-ttu-id="28bae-107">Die Arbeitsweise der Anwendung basiert darauf, dass die Kombination der 4 Felder  Artikelnr.,  Variantencode,  Lagerortcode und  Lagerplatzcode in den Inventurauftragszeilen in jedem Inventurauftrag nur einmal vorkommt.</span><span class="sxs-lookup"><span data-stu-id="28bae-107">The combination of the Item No., Variant Code, Location Code, and Bin Code fields in the inventory order lines should exist only one time for a physical inventory order.</span></span> <span data-ttu-id="28bae-108">Aus diesem Grund führt die Anwendung beim Zuweisen von Inventurerfassungszeilen zu Inventurauftragszeilen eine entsprechende Prüfung durch.</span><span class="sxs-lookup"><span data-stu-id="28bae-108">This is verified when assigning physical inventory recording lines to physical inventory order lines.</span></span>  

## <a name="to-view-duplicate-physical-inventory-order-lines"></a><span data-ttu-id="28bae-109">So zeigen Sie doppelte Inventurauftragszeilen an</span><span class="sxs-lookup"><span data-stu-id="28bae-109">To view duplicate physical inventory order lines</span></span>  

1.  <span data-ttu-id="28bae-110">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Symbol „Nach Seite oder Bericht suchen”"), geben Sie **Bestandsauftrag** ein, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="28bae-110">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Phys. Inventory Order**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="28bae-111">Öffnen Sie den Inventurauftrag, dessen duplizierten Zeilen Sie anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="28bae-111">Open the physical inventory order that you want to view to duplicate lines of.</span></span>  
3.  <span data-ttu-id="28bae-112">Wählen Sie die **Doppelte Zeilen anzeigen** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="28bae-112">Choose the **Show Duplicate Lines** action.</span></span>  

<span data-ttu-id="28bae-113">Alle doppelten Inventurauftragszeilen werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="28bae-113">Any duplicate physical inventory order lines are displayed.</span></span>  

## <a name="see-also"></a><span data-ttu-id="28bae-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28bae-114">See Also</span></span>  
 <span data-ttu-id="28bae-115">[Physische Inventuraufträge eingeben](how-to-enter-physical-inventory-orders.md) </span><span class="sxs-lookup"><span data-stu-id="28bae-115">[Enter Physical Inventory Orders](how-to-enter-physical-inventory-orders.md) </span></span>  
 <span data-ttu-id="28bae-116">[So schließen Sie eine Inventurerfassung ab](how-to-finish-a-physical-inventory-recording.md) </span><span class="sxs-lookup"><span data-stu-id="28bae-116">[Finish a Physical Inventory Recording](how-to-finish-a-physical-inventory-recording.md) </span></span>  
 [<span data-ttu-id="28bae-117">Inventurerfassung – Inventurzählung</span><span class="sxs-lookup"><span data-stu-id="28bae-117">Physical Inventory Recording - Counting Physical Inventory</span></span>](physical-inventory-recording-counting-physical-inventory.md)
