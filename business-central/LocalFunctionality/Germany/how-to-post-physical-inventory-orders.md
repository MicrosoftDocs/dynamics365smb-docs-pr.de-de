---
title: "Gewusst wie: Buchen von Inventuraufträgen"
description: "Nach Fertigstellen eines Inventurauftrags und Ändern des Status in Beendet kann er gebucht werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 1acac32a417f794801da50c866db2643ea0a4c2d
ms.openlocfilehash: 9aa3d69d41a4f8667499908d5a8b3a48f7e1cb44
ms.contentlocale: de-de
ms.lasthandoff: 01/22/2019

---
# <a name="post-physical-inventory-orders"></a><span data-ttu-id="6d727-103">So buchen Sie Inventuraufträge</span><span class="sxs-lookup"><span data-stu-id="6d727-103">Post Physical Inventory Orders</span></span>
<span data-ttu-id="6d727-104">Nach Fertigstellen eines Inventurauftrags und Ändern des Status in **Beendet** kann er gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="6d727-104">After completing a physical inventory order and changing its status to **Finished**, you can post it.</span></span>  

<span data-ttu-id="6d727-105">Der Status eines Inventurauftrags kann unter folgenden Voraussetzungen auf **Beendet** festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="6d727-105">You can set the status of a physical inventory order to **Finished** if the following is true:</span></span>  

- <span data-ttu-id="6d727-106">Alle zugehörigen Inventurerfassungen weisen den Status **Beendet** auf.</span><span class="sxs-lookup"><span data-stu-id="6d727-106">All related physical inventory recordings have a status of **Finished**.</span></span>  
- <span data-ttu-id="6d727-107">Jede Inventurauftragszeile wurde in mindestens einer Inventurerfassungszeile erfasst.</span><span class="sxs-lookup"><span data-stu-id="6d727-107">Each physical inventory order line has been counted by at least one inventory recording line.</span></span>  
- <span data-ttu-id="6d727-108">Die Kontrollkästchen **In Erfassungszeilen enthalten** und **Berechnete erw. Menge** wurden für alle Inventurauftragszeilen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6d727-108">The **In Recording Lines** and the **Qty. Exp. Calculated** check boxes have been selected for all of the physical inventory order lines.</span></span>  

<span data-ttu-id="6d727-109">Nach dem Buchen des Auftrags können die gebuchten Inventuraufträge angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6d727-109">After posting the order, you can view the posted physical inventory orders.</span></span> <span data-ttu-id="6d727-110">Gebuchte Lagerbelege bieten einen vollständigen Überblick über den Inventurprozess.</span><span class="sxs-lookup"><span data-stu-id="6d727-110">Posted inventory documents provide a complete overview of the physical inventory process.</span></span>  

## <a name="to-post-a-physical-inventory-order"></a><span data-ttu-id="6d727-111">So buchen Sie einen Inventurauftrag</span><span class="sxs-lookup"><span data-stu-id="6d727-111">To post a physical inventory order</span></span>  

1.  <span data-ttu-id="6d727-112">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Symbol „Nach Seite oder Bericht suchen”"), geben Sie **Bestandsauftrag** ein, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="6d727-112">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Phys. Inventory Order**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="6d727-113">Wählen Sie den Inventurauftrag aus, den Sie fertig stellen möchten, klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="6d727-113">Select the physical inventory order that you want to complete, and then choose the **Edit** action.</span></span>  

    <span data-ttu-id="6d727-114">Auf der Seite **Inventurauftrag** kann die Menge angezeigt werden, die nach Ausführung der Inventur im Feld **Erfasste Menge (Basis)** erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="6d727-114">On the **Phys. Inventory Order** page, you can view the quantity recorded after taking physical inventory in the **Qty. Recorded (Base)** field.</span></span>  

3.  <span data-ttu-id="6d727-115">Wählen Sie die Schaltfläche **Fertigstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="6d727-115">Choose the **Finish** action.</span></span>  
4.  <span data-ttu-id="6d727-116">Wählen Sie die Schaltfläche **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="6d727-116">Choose the **Yes** button.</span></span> <span data-ttu-id="6d727-117">Der Wert im Feld **Status** wird in **Beendet** geändert.</span><span class="sxs-lookup"><span data-stu-id="6d727-117">The value in the **Status** field is changed to **Finished**.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="6d727-118">Eine Änderung des Inventurauftragskopfs oder der Inventurauftragszeilen ist nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="6d727-118">You cannot change the physical inventory order header or the physical inventory order lines.</span></span>  

5.  <span data-ttu-id="6d727-119">Wählen Sie die zu buchenden Zeilen aus, und wählen Sie dann die Aktion **Buchen** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="6d727-119">To post the order, choose **Post**, and then choose the **OK** button.</span></span>  

## <a name="to-view-posted-physical-inventory-orders"></a><span data-ttu-id="6d727-120">So zeigen Sie gebuchte Inventuraufträge an</span><span class="sxs-lookup"><span data-stu-id="6d727-120">To view posted physical inventory orders</span></span>  

1.  <span data-ttu-id="6d727-121">Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Physische Inventur durchführen** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="6d727-121">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Phys. Invt. Order**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="6d727-122">Wählen Sie auf der Seite **Gebuchter Inventurauftrag** den gebuchten Inventurauftrag aus, den Sie anzeigen möchten, klicken Sie auf Aktionen und anschließend auf **Ansicht**.</span><span class="sxs-lookup"><span data-stu-id="6d727-122">On the **Posted Phys. Invt. Order** page, select the posted inventory order that you want to view, and then choose the **View** action.</span></span>  
3.  <span data-ttu-id="6d727-123">Um einer Liste zugehörige Inventurerfassungen anzuzeigen, wählen Sie die Aktion **Erfassungen** aus.</span><span class="sxs-lookup"><span data-stu-id="6d727-123">To view a list of related physical inventory recordings, choose the **Recordings** action.</span></span>  

    <span data-ttu-id="6d727-124">Sie können auch einen Bericht ausführen, in dem die Differenz zwischen der erwarteten Menge und der erfassten Menge zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6d727-124">You can also run a report that returns the difference between the expected quantity and the physical (recorded) quantity.</span></span>  

4.  <span data-ttu-id="6d727-125">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6d727-125">Close the page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6d727-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d727-126">See Also</span></span>  
 <span data-ttu-id="6d727-127">[Inventurbelege](physical-inventory-documents.md) </span><span class="sxs-lookup"><span data-stu-id="6d727-127">[Physical Inventory Documents](physical-inventory-documents.md) </span></span>  
 [<span data-ttu-id="6d727-128">Physische Inventuraufträge eingeben</span><span class="sxs-lookup"><span data-stu-id="6d727-128">Enter Physical Inventory Orders</span></span>](how-to-enter-physical-inventory-orders.md)

