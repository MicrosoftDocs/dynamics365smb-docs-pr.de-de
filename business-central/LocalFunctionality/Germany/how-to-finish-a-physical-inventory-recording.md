---
title: 'Gewusst wie: So schließen Sie eine Inventurerfassung ab'
description: Nachdem alle Daten einer Inventurerfassung vollständig eingegeben wurden, können Sie die Erfassung abschließen, indem Sie das Feld Status auf Beendet setzen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: fd06fb266f387bbe26c67673017b0515f7f66397
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "826685"
---
# <a name="finish-a-physical-inventory-recording"></a><span data-ttu-id="45b09-103">So schließen Sie eine Inventurerfassung ab</span><span class="sxs-lookup"><span data-stu-id="45b09-103">Finish a Physical Inventory Recording</span></span>
<span data-ttu-id="45b09-104">Nachdem alle Daten einer Inventurerfassung vollständig eingegeben wurden, können Sie die Erfassung abschließen, indem Sie das Feld **Status** auf **Beendet** setzen.</span><span class="sxs-lookup"><span data-stu-id="45b09-104">After you have entered all data for a physical inventory recording, you can finish the recording by setting the **Status** field to **Finished**.</span></span>  

<span data-ttu-id="45b09-105">Dies ist nur möglich, wenn das Kontrollkästchen **Erfasst** für alle Inventurerfassungszeilen der aktuellen Inventurerfassung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="45b09-105">You can only do this, if the **Recorded** field is selected for all physical inventory recording lines for the current physical inventory recording.</span></span>  

## <a name="to-finish-a-physical-inventory-recording"></a><span data-ttu-id="45b09-106">So schließen Sie eine Inventurerfassung ab</span><span class="sxs-lookup"><span data-stu-id="45b09-106">To finish a physical inventory recording</span></span>  

1.  <span data-ttu-id="45b09-107">Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Physische Inventurliste** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="45b09-107">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Phys. Inventory Recording List**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="45b09-108">Öffnen Sie den Inventurauftrag, den Sie abschließen möchten, und wählen Sie die **Fertig stellen** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="45b09-108">Open the physical inventory recording that you want to finish, and then choose the **Finish** action.</span></span>  

    <span data-ttu-id="45b09-109">Das Feld Status wird auf **Beendet** gesetzt.</span><span class="sxs-lookup"><span data-stu-id="45b09-109">The status is set to **Finished**.</span></span> <span data-ttu-id="45b09-110">Sie können den Inventurerfassungskopf oder die Inventurerfassungszeilen nun nicht mehr ändern.</span><span class="sxs-lookup"><span data-stu-id="45b09-110">You can no longer change the physical inventory header or the physical inventory lines.</span></span>  

<span data-ttu-id="45b09-111">Beim Abschluss der aktuellen Inventurerfassung weist die Anwendung jeder Inventurerfassungszeile eine Zeile des zugehörigen Inventurauftrags zu.</span><span class="sxs-lookup"><span data-stu-id="45b09-111">When you finish the current physical inventory recording, every physical inventory recording line is assigned to one line of the related physical inventory order.</span></span> <span data-ttu-id="45b09-112">Die Anwendung weist jeweils Inventurauftragszeilen mit den gleichen Werten in den 4 Feldern  **Artikelnr.**,  **Variantencode**, **Lagerortcode** und **Lagerplatzcode** wie in der Inventurerfassungszeile zu.</span><span class="sxs-lookup"><span data-stu-id="45b09-112">The physical inventory order lines are assigned with the same values in the **Item No.**, **Variant Code**, **Location Code**, and **Bin Code** fields as the physical inventory recording line has.</span></span>  

<span data-ttu-id="45b09-113">Wenn keine entsprechende Inventurauftragszeile vorhanden ist und wenn das Feld **Erfassung ohne Auftrag erlaubt** im Inventurerfassungskopf aktiviert ist, wird automatisch eine neue Zeile eingefügt und das **Ohne Auftrag erfasst** der Inventurauftragszeile aktiviert.</span><span class="sxs-lookup"><span data-stu-id="45b09-113">If no such physical inventory order line exists, and if the **Recording without order permit** field is selected on the physical inventory recording header, a new line is inserted automatically and the **Recorded without Order** field on the physical inventory order line is selected.</span></span> <span data-ttu-id="45b09-114">Andernfalls wird eine Fehlermeldung angezeigt, und der Prozess wird abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="45b09-114">Otherwise, an error message is displayed and the process is canceled.</span></span> <span data-ttu-id="45b09-115">Auch wenn es mehr als eine zugehörige Inventurauftragszeile gibt, wird eine Fehlermeldung angezeigt und die Verarbeitung gestoppt.</span><span class="sxs-lookup"><span data-stu-id="45b09-115">If there are more than one such physical inventory order lines, an error message is displayed and the process is canceled.</span></span>  

## <a name="see-also"></a><span data-ttu-id="45b09-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45b09-116">See Also</span></span>  
 <span data-ttu-id="45b09-117">[So erstellen Sie eine physische Inventurerfassung](how-to-create-a-physical-inventory-recording.md) </span><span class="sxs-lookup"><span data-stu-id="45b09-117">[Create a Physical Inventory Recording](how-to-create-a-physical-inventory-recording.md) </span></span>  
 <span data-ttu-id="45b09-118">[So erstellen Sie eine physische Inventurerfassung](how-to-create-a-physical-inventory-recording.md) </span><span class="sxs-lookup"><span data-stu-id="45b09-118">[Create a Physical Inventory Recording](how-to-create-a-physical-inventory-recording.md) </span></span>  
 <span data-ttu-id="45b09-119">[So zeigen Sie doppelte Inventurauftragszeilen an](how-to-view-duplicate-physical-inventory-order-lines.md) </span><span class="sxs-lookup"><span data-stu-id="45b09-119">[View Duplicate Physical Inventory Order Lines](how-to-view-duplicate-physical-inventory-order-lines.md) </span></span>  
 <span data-ttu-id="45b09-120">[Vorgehensweise beim Analysieren von Inventurdifferenzen](how-to-analyze-physical-inventory-differences.md) </span><span class="sxs-lookup"><span data-stu-id="45b09-120">[Analyze Physical Inventory Differences](how-to-analyze-physical-inventory-differences.md) </span></span>  
 [<span data-ttu-id="45b09-121">Inventurauftragszeilen mit Artikelverfolgungszeilen</span><span class="sxs-lookup"><span data-stu-id="45b09-121">Physical Inventory Order Lines With Item Tracking Lines</span></span>](physical-inventory-order-lines-with-item-tracking-lines.md)
