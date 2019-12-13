---
title: 'Vorgehensweise: Ausgangsbuchung stornieren | Microsoft Docs'
description: Es kann vorkommen, dass die Buchung einer fertig gestellten Menge storniert werden muss. Dies ist z. B. der Fall, wenn eine fehlerhafte Dateneingabe passiert ist und eine falsche fertiggestellte Menge in einem Fertigungsauftrag gebucht wurde.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 2cdda8a01d6391f97bfae5600ce35d2ab989ae54
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2877844"
---
# <a name="reverse-output-posting"></a><span data-ttu-id="3cfdf-104">Gebuchte fertig gestellte Menge stornieren</span><span class="sxs-lookup"><span data-stu-id="3cfdf-104">Reverse Output Posting</span></span>
<span data-ttu-id="3cfdf-105">Es kann vorkommen, dass die Buchung einer fertig gestellten Menge storniert werden muss.</span><span class="sxs-lookup"><span data-stu-id="3cfdf-105">There are times when output posting must be reversed.</span></span> <span data-ttu-id="3cfdf-106">Dies ist z. B. der Fall, wenn eine fehlerhafte Dateneingabe passiert ist und eine falsche fertiggestellte Menge in einem Fertigungsauftrag gebucht wurde.</span><span class="sxs-lookup"><span data-stu-id="3cfdf-106">An example of this would be if a data entry error occurred and an incorrect amount of output is posted to a production order.</span></span>  

## <a name="to-reverse-an-output-posting"></a><span data-ttu-id="3cfdf-107">Eine Ausgangsbuchung stornieren</span><span class="sxs-lookup"><span data-stu-id="3cfdf-107">To reverse an output posting</span></span>  
1.  <span data-ttu-id="3cfdf-108">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **FA-Istmeldungs Buch.-Blatt** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="3cfdf-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span> <span data-ttu-id="3cfdf-109">Wählen Sie Ihren Stapel aus.</span><span class="sxs-lookup"><span data-stu-id="3cfdf-109">Select your batch.</span></span>  
2. <span data-ttu-id="3cfdf-110">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="3cfdf-110">Fill in the fields as necessary.</span></span> <span data-ttu-id="3cfdf-111">Weitere Informationen finden Sie unter [Produktionsausgabe und Laufzeiten über Stapelverarbeitung buchen](production-how-to-post-output-quantity.md)</span><span class="sxs-lookup"><span data-stu-id="3cfdf-111">For more information, see [Batch Post Output and Run Times](production-how-to-post-output-quantity.md).</span></span>
3.  <span data-ttu-id="3cfdf-112">Wählen Sie im Feld **Ausgleich mit Lfd. Nr.** den zugeordneten Artikelposten aus.</span><span class="sxs-lookup"><span data-stu-id="3cfdf-112">In the **Applies-To Entry** field, select the associated item ledger entry.</span></span> <span data-ttu-id="3cfdf-113">Dadurch werden der Kapazitäts- und der Artikelposten storniert.</span><span class="sxs-lookup"><span data-stu-id="3cfdf-113">This reverses the capacity and item ledger entries.</span></span>  
4. <span data-ttu-id="3cfdf-114">Buchen Sie die Stornierung, indem Sie das Buch.-Blatt buchen.</span><span class="sxs-lookup"><span data-stu-id="3cfdf-114">Post the reversal by posting the journal.</span></span>  

<span data-ttu-id="3cfdf-115">Die Posten im FA-Istmeldungsprotokoll werden im Hauptartikelposten als positiver Ausgleich gebucht.</span><span class="sxs-lookup"><span data-stu-id="3cfdf-115">The output journal entries are posted to the item ledger as a positive adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3cfdf-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3cfdf-116">See Also</span></span>  
 <span data-ttu-id="3cfdf-117">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="3cfdf-117">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
 [<span data-ttu-id="3cfdf-118">Produktion einrichten</span><span class="sxs-lookup"><span data-stu-id="3cfdf-118">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
 <span data-ttu-id="3cfdf-119">[Planung](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="3cfdf-119">[Planning](production-planning.md)    </span></span>  
 [<span data-ttu-id="3cfdf-120">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="3cfdf-120">Inventory</span></span>](inventory-manage-inventory.md)  
 [<span data-ttu-id="3cfdf-121">Einkauf</span><span class="sxs-lookup"><span data-stu-id="3cfdf-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="3cfdf-122">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3cfdf-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
