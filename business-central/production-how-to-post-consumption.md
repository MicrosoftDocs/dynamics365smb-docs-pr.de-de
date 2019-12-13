---
title: 'Vorgehensweise: Verbrauch mit Stapelverarbeitung buchen | Microsoft Docs'
description: Wenn die Buchungsmethode **Manuell** ist, müssen Sie den Verbrauch manuell mit einem Verbrauchsprotokoll buchen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 9200256cec074e547bc594950b1eb2d975a8ad9b
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2877883"
---
# <a name="batch-post-production-consumption"></a><span data-ttu-id="f0927-103">Produktionsverbrauch mit Stapelverarbeitung buchen</span><span class="sxs-lookup"><span data-stu-id="f0927-103">Batch Post Production Consumption</span></span>
<span data-ttu-id="f0927-104">Wenn die Buchungsmethode **Manuell** ist, müssen Sie den Verbrauch manuell mit einem Verbrauchsprotokoll buchen.</span><span class="sxs-lookup"><span data-stu-id="f0927-104">If the flushing method is **Manual**, you must post the components manually, using a consumption journal.</span></span>

<span data-ttu-id="f0927-105">Sie können das System so einstellen, um automatisch (*flush*) Komponenten zu buchen, wenn Sie beginnen oder Fertigungsaufträge beenden.</span><span class="sxs-lookup"><span data-stu-id="f0927-105">You can also set the system up to automatically post (*flush*) components when you start or finish production orders.</span></span> <span data-ttu-id="f0927-106">Weitere Informationen finden Sie unter [Vorgehensweise: Komponenten entsprechend dem Arbeitsgangs-Ausstoß leeren](production-how-to-flush-components-according-to-operation-output.md).</span><span class="sxs-lookup"><span data-stu-id="f0927-106">For more information, see [Enable Flushing of Components According to Operation Output](production-how-to-flush-components-according-to-operation-output.md).</span></span>

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a><span data-ttu-id="f0927-107">Die Laufzeit für eine oder mehrere Verbrauchszeile buchen</span><span class="sxs-lookup"><span data-stu-id="f0927-107">To post consumption for one or more production order lines</span></span>  
1.  <span data-ttu-id="f0927-108">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **FA-Verbrauchs Buch.-Blatt** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="f0927-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Consumption Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f0927-109">Füllen Sie die Felder mit den Daten des Fertigungsauftrags und den Verbrauchsdaten aus.</span><span class="sxs-lookup"><span data-stu-id="f0927-109">Fill in the fields with the production order data and the consumption data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    <span data-ttu-id="f0927-110">Wenn der Lagerort, an dem sich die Komponenten befinden, so eingerichtet ist, dass Lagerplätze verwendet werden, die Bearbeitung der Kommissionierung jedoch nicht erforderlich ist, dann geben Sie in der Buch.-Blattzeile einen Lagerplatz ein, um festzulegen, von welchem Lagerplatz die Artikel aus dem Lager entnommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f0927-110">If the warehouse location where the components are stored is set up to use bins but does not require pick processing, assign a bin code to the journal line to indicate where the items should be taken from in the warehouse.</span></span> <span data-ttu-id="f0927-111">Weitere Informationen finden Sie unter [Kommissionierung für die Produktion oder Montage](warehouse-how-to-pick-for-production.md).</span><span class="sxs-lookup"><span data-stu-id="f0927-111">For more information, see [Pick for Production or Assembly](warehouse-how-to-pick-for-production.md).</span></span>  
3.  <span data-ttu-id="f0927-112">Um den Verbrauch zu buchen, wählen Sie die Aktion **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="f0927-112">Choose the **Post** action to post the consumption.</span></span> <span data-ttu-id="f0927-113">Die verknüpften Artikelposten werden verringert.</span><span class="sxs-lookup"><span data-stu-id="f0927-113">The related item ledger entries are reduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="f0927-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0927-114">See Also</span></span>  
<span data-ttu-id="f0927-115">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="f0927-115">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="f0927-116">Produktion einrichten</span><span class="sxs-lookup"><span data-stu-id="f0927-116">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="f0927-117">[Planung](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="f0927-117">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="f0927-118">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="f0927-118">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="f0927-119">Einkauf</span><span class="sxs-lookup"><span data-stu-id="f0927-119">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="f0927-120">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f0927-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
