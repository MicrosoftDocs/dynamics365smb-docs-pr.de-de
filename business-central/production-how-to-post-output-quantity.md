---
title: 'Vorgehensweise: Produktionsausgabe und Laufzeiten über Stapelverarbeitung buchen| Microsoft Docs'
description: Die fertig gestellte Menge stellt den Arbeitsfortschritt in Form der gefertigten Menge dar.
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
ms.openlocfilehash: 28ad7aee70329251ffb6e4fbd187b183c8417f73
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "932384"
---
# <a name="batch-post-output-and-run-times"></a><span data-ttu-id="a9376-103">Ausgabe über Stapelverarbeitung buchen und Bearbeitungszeiten prüfen</span><span class="sxs-lookup"><span data-stu-id="a9376-103">Batch Post Output and Run Times</span></span>
<span data-ttu-id="a9376-104">Die fertig gestellte Menge stellt den Arbeitsfortschritt in Form der gefertigten Menge dar.</span><span class="sxs-lookup"><span data-stu-id="a9376-104">The output quantity represents the work progress in the form of the finished quantity.</span></span>  

> [!NOTE]
> <span data-ttu-id="a9376-105">Nur wenn Sie die fertig gestellte Menge für den letzten Arbeitsgang buchen, dann aktualisiert die Anwendung automatisch den Lagerbestand.</span><span class="sxs-lookup"><span data-stu-id="a9376-105">Only when you post output quantity on the last operation, the inventory is updated automatically.</span></span>  

## <a name="to-post-output-quantities-for-one-or-more-production-order-lines"></a><span data-ttu-id="a9376-106">Die fertig gestellte Mengen für eine oder mehrere Fertigungsauftragszeilen buchen</span><span class="sxs-lookup"><span data-stu-id="a9376-106">To post output quantities for one or more production order lines</span></span>
1. <span data-ttu-id="a9376-107">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Artikel Ausgabe-Buch.-Blätter** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="a9376-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="a9376-108">Füllen Sie die Felder mit den Daten des Fertigungsauftrags und den Ausgabedaten aus.</span><span class="sxs-lookup"><span data-stu-id="a9376-108">Fill in the fields with the production order data and the output data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="a9376-109">Wenn der Arbeitsgang beendet ist, wählen Sie das Feld **Beendet** aus.</span><span class="sxs-lookup"><span data-stu-id="a9376-109">If the operation has been completed, select the **Finished** field.</span></span>  

    <span data-ttu-id="a9376-110">Wenn der Lagerort, in den die Artikel eingelagert werden sollen, Lagerplätze verwendet, die Bearbeitung der Einlagerung jedoch nicht erforderlich ist,  weisen Sie der Buch.-Blattzeile einen Lagerplatzcode zu, um festzulegen, wo die Artikel im Lagerort eingelagert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a9376-110">If the warehouse location where the items should be put away uses bins but does not require put-away processing,  assign a bin code to the journal line to specify where the items should be placed in the warehouse.</span></span> <span data-ttu-id="a9376-111">Weitere Informationen finden Sie unter [Produktionseinlagerung oder Montageausgabe](warehouse-how-to-put-away-production-output.md).</span><span class="sxs-lookup"><span data-stu-id="a9376-111">For more information, see [Put Away Production or Assembly Output](warehouse-how-to-put-away-production-output.md).</span></span>  

4. <span data-ttu-id="a9376-112">Wählen Sie **Buchen** aus, um die Vorgänge zu buchen.</span><span class="sxs-lookup"><span data-stu-id="a9376-112">Choose the **Post** acto post the operations.</span></span> <span data-ttu-id="a9376-113">Die fertig gestellte Menge wird gebucht.</span><span class="sxs-lookup"><span data-stu-id="a9376-113">The output quantity will be posted.</span></span> <span data-ttu-id="a9376-114">Der Artikel ist jetzt versandbereit.</span><span class="sxs-lookup"><span data-stu-id="a9376-114">The item is now available for shipping.</span></span>  

## <a name="to-post-run-times-for-one-or-more-production-order-lines"></a><span data-ttu-id="a9376-115">Die Laufzeit für eine oder mehrere Fertigungsauftragszeilen buchen</span><span class="sxs-lookup"><span data-stu-id="a9376-115">To post run times for one or more production order lines</span></span>
<span data-ttu-id="a9376-116">Die Bearbeitungszeit stellt den Arbeitsfortschritt in Form der benötigten Arbeitszeit dar.</span><span class="sxs-lookup"><span data-stu-id="a9376-116">The run time represents work progress in the form of the necessary working time.</span></span>    

1.  <span data-ttu-id="a9376-117">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Artikel Ausgabe-Buch.-Blätter** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="a9376-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="a9376-118">Füllen Sie die Felder mit den Daten des Fertigungsauftrags und den Ausgabedaten aus.</span><span class="sxs-lookup"><span data-stu-id="a9376-118">Fill in the fields with the production order data and the output data.</span></span>  
3.  <span data-ttu-id="a9376-119">Wenn der Arbeitsgang beendet ist, wählen Sie das Feld **Beendet** aus.</span><span class="sxs-lookup"><span data-stu-id="a9376-119">If the operation is completed, select the **Finished** field.</span></span>  
4. <span data-ttu-id="a9376-120">Wählen Sie die **Buchen** Aktion aus, um die Zeit zu buchen, die je Arbeitsgang aufgewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="a9376-120">Choose the **Post** action to post the time spent per operation.</span></span> <span data-ttu-id="a9376-121">Kapazitätsposten werden für die benötigte Arbeitsplätzen oder Arbeitsplatzgruppen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a9376-121">Capacity ledger entries are updated for the used work or machine centers.</span></span>

## <a name="see-also"></a><span data-ttu-id="a9376-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9376-122">See Also</span></span>  
<span data-ttu-id="a9376-123">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="a9376-123">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="a9376-124">Produktion einrichten</span><span class="sxs-lookup"><span data-stu-id="a9376-124">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="a9376-125">[Planung](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="a9376-125">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="a9376-126">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="a9376-126">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="a9376-127">Einkauf</span><span class="sxs-lookup"><span data-stu-id="a9376-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="a9376-128">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a9376-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
