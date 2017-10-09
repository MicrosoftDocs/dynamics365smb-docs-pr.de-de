---
title: 'Vorgehensweise: Ausgangsbuchung stornieren | Microsoft Docs'
description: Es kann vorkommen, dass die Buchung einer fertig gestellten Menge storniert werden muss. Dies ist z. B. der Fall, wenn eine fehlerhafte Dateneingabe passiert ist und eine falsche fertiggestellte Menge in einem Fertigungsauftrag gebucht wurde.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7ac453ff87d78e6be0567ba93b58c0f8938f4052
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-reverse-output-posting"></a><span data-ttu-id="d94af-104">Vorgehensweise: Eine Ausgangsbuchung stornieren</span><span class="sxs-lookup"><span data-stu-id="d94af-104">How to: Reverse Output Posting</span></span>
<span data-ttu-id="d94af-105">Es kann vorkommen, dass die Buchung einer fertig gestellten Menge storniert werden muss.</span><span class="sxs-lookup"><span data-stu-id="d94af-105">There are times when output posting must be reversed.</span></span> <span data-ttu-id="d94af-106">Dies ist z. B. der Fall, wenn eine fehlerhafte Dateneingabe passiert ist und eine falsche fertiggestellte Menge in einem Fertigungsauftrag gebucht wurde.</span><span class="sxs-lookup"><span data-stu-id="d94af-106">An example of this would be if a data entry error occurred and an incorrect amount of output is posted to a production order.</span></span>  

## <a name="to-reverse-an-output-posting"></a><span data-ttu-id="d94af-107">Eine Ausgangsbuchung stornieren</span><span class="sxs-lookup"><span data-stu-id="d94af-107">To reverse an output posting</span></span>  
1.  <span data-ttu-id="d94af-108">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Ausgabe-Buchblatt** ein und wählen den zugehörenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="d94af-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Output Journal**, and then choose the related link.</span></span> <span data-ttu-id="d94af-109">Wählen Sie Ihren Stapel aus.</span><span class="sxs-lookup"><span data-stu-id="d94af-109">Select your batch.</span></span>  
2. <span data-ttu-id="d94af-110">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="d94af-110">Fill in the fields as necessary.</span></span> <span data-ttu-id="d94af-111">Weitere Informationen finden Sie unter [Vorgehensweise: Produktionsausgabe und Laufzeiten über Stapelverarbeitung buchen](production-how-to-post-output-quantity.md)</span><span class="sxs-lookup"><span data-stu-id="d94af-111">For more information, see [How to: Batch Post Output and Run Times](production-how-to-post-output-quantity.md).</span></span>
3.  <span data-ttu-id="d94af-112">Wählen Sie im Feld **Ausgleich mit Lfd. Nr.** den zugeordneten Artikelposten aus.</span><span class="sxs-lookup"><span data-stu-id="d94af-112">In the **Applies-To Entry** field, select the associated item ledger entry.</span></span> <span data-ttu-id="d94af-113">Dadurch werden der Kapazitäts- und der Artikelposten storniert.</span><span class="sxs-lookup"><span data-stu-id="d94af-113">This reverses the capacity and item ledger entries.</span></span>  
4. <span data-ttu-id="d94af-114">Buchen Sie die Stornierung, indem Sie das Buch.-Blatt buchen.</span><span class="sxs-lookup"><span data-stu-id="d94af-114">Post the reversal by posting the journal.</span></span>  

<span data-ttu-id="d94af-115">Die Posten im FA-Istmeldungsprotokoll werden im Hauptartikelposten als positiver Ausgleich gebucht.</span><span class="sxs-lookup"><span data-stu-id="d94af-115">The output journal entries are posted to the item ledger as a positive adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d94af-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d94af-116">See Also</span></span>  
 <span data-ttu-id="d94af-117">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="d94af-117">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
 [<span data-ttu-id="d94af-118">Produktion einrichten</span><span class="sxs-lookup"><span data-stu-id="d94af-118">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
 <span data-ttu-id="d94af-119">[Planung](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="d94af-119">[Planning](production-planning.md)    </span></span>  
 [<span data-ttu-id="d94af-120">Lagerbest</span><span class="sxs-lookup"><span data-stu-id="d94af-120">Inventory</span></span>](inventory-manage-inventory.md)  
 [<span data-ttu-id="d94af-121">Einkauf</span><span class="sxs-lookup"><span data-stu-id="d94af-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="d94af-122">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d94af-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

