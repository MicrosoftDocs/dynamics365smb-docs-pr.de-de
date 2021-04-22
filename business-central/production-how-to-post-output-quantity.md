---
title: Produktionsausgabe und Laufzeiten über Stapelverarbeitung buchen
description: Die fertig gestellte Menge repräsentiert den Arbeitsfortschritt in Form der fertigen Menge und der genutzten Kapazität der Arbeit oder des Arbeitsplatzes.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 923f68b13619013dd54062438c66192a682868bc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787877"
---
# <a name="batch-post-output-and-run-times"></a><span data-ttu-id="f9327-103">Ausgabe über Stapelverarbeitung buchen und Bearbeitungszeiten prüfen</span><span class="sxs-lookup"><span data-stu-id="f9327-103">Batch Post Output and Run Times</span></span>
<span data-ttu-id="f9327-104">Die fertig gestellte Menge repräsentiert den Arbeitsfortschritt in Form der fertigen Menge und der genutzten Kapazität der Arbeit oder des Arbeitsplatzes.</span><span class="sxs-lookup"><span data-stu-id="f9327-104">The output quantity represents the work progress in the form of the finished quantity and used capacity of work or machine center.</span></span>

<span data-ttu-id="f9327-105">Sie können das Ausgabejournal für Folgendes verwenden:</span><span class="sxs-lookup"><span data-stu-id="f9327-105">You can use the output journal to:</span></span>
*  <span data-ttu-id="f9327-106">Regulieren Sie Lagerbestand in Verbindung mit der Ausgabe fertiger Artikel aus der Produktion.</span><span class="sxs-lookup"><span data-stu-id="f9327-106">Adjust inventory in connection with output of finished items from production.</span></span>
*  <span data-ttu-id="f9327-107">Registrieren Sie Mengen und Ausschuss für jeden Vorgang im Fertigungsarbeitsgang.</span><span class="sxs-lookup"><span data-stu-id="f9327-107">Register quantities and scrap for each operation in production routing.</span></span>
*  <span data-ttu-id="f9327-108">Registrieren Sie Setup und Laufzeit für Arbeit und Arbeitsplätze.</span><span class="sxs-lookup"><span data-stu-id="f9327-108">Register setup and run time for work and machine centers.</span></span>

> [!NOTE]
> <span data-ttu-id="f9327-109">Wenn der Fertigungsarbeitsgang verwendet wird, aktualisiert die Anwendung automatisch den Lagerbestand nur wenn Sie die fertig gestellte Menge für den letzten Arbeitsgang buchen.</span><span class="sxs-lookup"><span data-stu-id="f9327-109">If production routing are used, the inventory is updated only when you post output quantity on the last operation.</span></span>

<span data-ttu-id="f9327-110">Im Fenster **Produktions Buch.-Blatt** können Sie die gleichen Aufgaben wie im Fenster **FA-Istmeldungs Buch.-Blatt** ausführen und gleichzeitig die entsprechenden Verbrauchsbuchungsaufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="f9327-110">With the **Production Journal** window, you can perform the same tasks as in the **Output Journal** window and at the same time perform the related consumption posting tasks.</span></span> <span data-ttu-id="f9327-111">Weitere Informationen finden Sie unter [Gemeinsames Erfassen und Buchen von Verbrauch und Istmeldungen für eine einzelne freigegebene Fertigungsauftragszeile](production-how-to-register-consumption-and-output.md).</span><span class="sxs-lookup"><span data-stu-id="f9327-111">For more information, see [Register Consumption and Output for One Released Production order line](production-how-to-register-consumption-and-output.md).</span></span>

## <a name="to-post-output-quantities-andor-register-run-times-for-one-or-more-production-order-lines"></a><span data-ttu-id="f9327-112">Die fertig gestellte Mengen und/oder Erfassungslaufzeiten für eine oder mehrere Fertigungsauftragszeilen buchen</span><span class="sxs-lookup"><span data-stu-id="f9327-112">To post output quantities and/or register run times for one or more production order lines</span></span>
1. <span data-ttu-id="f9327-113">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **FA-Istmeldungs Buch.-Blatt** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="f9327-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f9327-114">Füllen Sie die Felder mit den Daten des Fertigungsauftrags und den Ausgabedaten und/oder der Laufzeit aus.</span><span class="sxs-lookup"><span data-stu-id="f9327-114">Fill in the fields with the production order data and the output data and/or run time.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
  
    <span data-ttu-id="f9327-115">Sie können die Funktion **Arbeitsplan auflösen** Generieren von Journalzeilen aus Fertigungsaufträgen verwenden.</span><span class="sxs-lookup"><span data-stu-id="f9327-115">You can use the **Explode Routing** function to generate journal lines from production orders.</span></span>
  
4. <span data-ttu-id="f9327-116">Wenn der Arbeitsgang beendet ist, wählen Sie das Feld **Beendet** aus.</span><span class="sxs-lookup"><span data-stu-id="f9327-116">If the operation has been completed, select the **Finished** field.</span></span>  
5. <span data-ttu-id="f9327-117">Um die Vorgänge zu buchen, wählen Sie die Aktion **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="f9327-117">Choose the **Post** action to post the operations.</span></span> 
 
<span data-ttu-id="f9327-118">Kapazitätsposten werden für die verwendeten Arbeitsplätze mit Informationen zu Zeit und Menge der Ausgabe und des Ausschusses aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f9327-118">Capacity ledger entries are updated for the used work or machine centers with information about time and quantity of output and scrap.</span></span> <span data-ttu-id="f9327-119">Wenn Sie den letzten Vorgang gebucht haben, wird der Artikel dem Lager hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f9327-119">If you posted the last operation, the item will be added to the inventory.</span></span> 

## <a name="see-also"></a><span data-ttu-id="f9327-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9327-120">See Also</span></span>  
<span data-ttu-id="f9327-121">[Ausschuss manuell buchen](production-how-to-post-scrap.md)
[Gebuchte fertig gestellte Menge stornieren](production-how-to-reverse-output-posting.md)
[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="f9327-121">[Post Scrap Manually](production-how-to-post-scrap.md)
[Reverse Output Posting](production-how-to-reverse-output-posting.md)
[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="f9327-122">Produktion einrichten</span><span class="sxs-lookup"><span data-stu-id="f9327-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="f9327-123">[Planung](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="f9327-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="f9327-124">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="f9327-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="f9327-125">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f9327-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]
