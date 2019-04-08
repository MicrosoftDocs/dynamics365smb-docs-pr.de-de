---
title: 'Vorgehensweise: Planen von Lagerplatzumlagerungen in Vorschlägen | Microsoft Docs'
description: Planen Sie Lagerplatzumlagerungen im Vorschlag, indem Sie eine Wiederauffüllfunktion nutzen oder manuell die Zeilen planen, die Sie als Umlagerungsanweisungen erstellen möchten.
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
ms.openlocfilehash: 7184143303dd1a8b04d8d740d83f35f1fa19485a
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "798848"
---
# <a name="plan-warehouse-movements-in-worksheets"></a><span data-ttu-id="04459-103">Planen von Umlagerungen in Arbeitsblättern</span><span class="sxs-lookup"><span data-stu-id="04459-103">Plan Warehouse Movements in Worksheets</span></span>
<span data-ttu-id="04459-104">Planen Sie Lagerplatzumlagerungen im Vorschlag, indem Sie eine Wiederauffüllfunktion nutzen oder manuell die Zeilen planen, die Sie als Umlagerungsanweisungen erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="04459-104">Plan movements in the worksheet using a bin replenishment function or manually planning the lines that you want to create as movement instructions.</span></span>  

## <a name="to-calculate-a-replenishment-movement"></a><span data-ttu-id="04459-105">So berechnen Sie Lagerplatzauffüllungen:</span><span class="sxs-lookup"><span data-stu-id="04459-105">To calculate a replenishment movement</span></span>  
<span data-ttu-id="04459-106">Wenn aus dem Lager Artikel an Debitoren geliefert werden, enthalten die Lagerplätze mit den höchsten Prioritäten (höchstwahrscheinlich die, die am dichtesten am Warenausgangsbereich liegen) kontinuierlich weniger Artikel.</span><span class="sxs-lookup"><span data-stu-id="04459-106">As the warehouse ships items out to customers, the bins with the highest bin rankings contain fewer and fewer items.</span></span> <span data-ttu-id="04459-107">Um diese Lagerplätze mit den höchsten Prioritäten mit Artikeln aus anderen Lagerplätzen wiederaufzufüllen, können Sie die Funktion **Lagerplatz-Auffüllung berechnen** auf der Seite **Lagerplatzumlagerungsvorschlag** verwenden.</span><span class="sxs-lookup"><span data-stu-id="04459-107">To fill up these high-ranking pick bins with items from other bins, run the **Calculate Bin Replenishment** function on the **Movement Worksheet** page</span></span>

1.  <span data-ttu-id="04459-108">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Lagerplatzumlagerungsvorschlag** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="04459-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="04459-109">Wählen Sie die Aktion **Lagerplatzauffüllung berechnen**.</span><span class="sxs-lookup"><span data-stu-id="04459-109">Choose the **Calculate Bin Replenishment** action.</span></span>  

    [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="04459-110">erstellt Zeilen, die genau angeben, wie Artikel von den Lagerplätzen mit niedriger Priorität in die mit höherer Priorität umgelagert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="04459-110">creates lines that indicate precisely how you should move items from the low-ranking bins to the higher-ranking bins.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="04459-111">Eine Umlagerung wird gemäß FEFO vorgeschlagen, wenn Sie die Funktion **Lagerplatzumlagerung erstellen** aktivieren und wenn die folgenden Bedingungen für einen Artikel erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="04459-111">A movement is suggested according to FEFO when you activate the **Create Movement** function if the following conditions are met for an item:</span></span>  
    >   
    >  -   <span data-ttu-id="04459-112">Der Artikel weist ein Ablaufdatum auf.</span><span class="sxs-lookup"><span data-stu-id="04459-112">The item has an expiration date.</span></span>  
    > -   <span data-ttu-id="04459-113">Das Feld **Gemäß FEFO kommissionieren** ist auf der Lagerortkarte aktiviert, und</span><span class="sxs-lookup"><span data-stu-id="04459-113">The **Pick According to FEFO** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="04459-114">Das Kontrollkästchen **Kommissionierung erforderlich** muss auf der Lagerortkarte aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="04459-114">The **Bin Mandatory** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="04459-115">Die Felder **Von Zone** und **Von Lagerplatz** sind leer.</span><span class="sxs-lookup"><span data-stu-id="04459-115">The **From Zone** and **From Bin** fields are blank.</span></span>  

    <span data-ttu-id="04459-116">Weitere Informationen finden Sie unter[ Korrigieren der FEFO..](warehouse-picking-by-fefo.md)</span><span class="sxs-lookup"><span data-stu-id="04459-116">For more information, see [Picking by FEFO](warehouse-picking-by-fefo.md).</span></span>  

3.  <span data-ttu-id="04459-117">Sehen Sie sich die Zeilen an und ändern Sie sie – falls notwendig – oder löschen Sie einige von ihnen, wenn Sie nicht genug Zeit haben, alle auszuführen.</span><span class="sxs-lookup"><span data-stu-id="04459-117">Look through the lines and change them if necessary, or delete some of them if there is not enough time to perform them all.</span></span>  
4.  <span data-ttu-id="04459-118">Wählen Sie die Aktion **Lagerplatzumlagerung erstellen** aus, um eine Anweisung zu erstellen, die die Lagermitarbeiter ausführen sollen.</span><span class="sxs-lookup"><span data-stu-id="04459-118">Choose the **Create Movement** action to make a warehouse instruction for action by warehouse employees.</span></span>  

## <a name="to-move-the-entire-contents-of-one-or-more-bins-by-using-the-get-bin-content-function"></a><span data-ttu-id="04459-119">Den gesamten Inhalt eines oder mehrerer Lagerplätze umlagern, indem Sie die Funktion "Lagerplatzinhalt holen" verwenden</span><span class="sxs-lookup"><span data-stu-id="04459-119">To move the entire contents of one or more bins by using the Get Bin Content function</span></span>  
<span data-ttu-id="04459-120">Sie können den Lagerplatzumlagerungsvorschlag auch nutzen, um andere Umlagerungen von Artikeln innerhalb des Lagers zu planen.</span><span class="sxs-lookup"><span data-stu-id="04459-120">You can also use the movement worksheet to plan other movement of inventory within the warehouse.</span></span> <span data-ttu-id="04459-121">Wenn Sie z. B. Artikel für die Qualitätskontrolle in einen Lagerplatz einlagern möchten, können Sie den Lagerplatzumlagerungsvorschlag verwenden, um diese Aktion zu planen, und dann eine Lagerplatzumlagerung erstellen, die eine Anweisung für einen Mitarbeiter darstellt.</span><span class="sxs-lookup"><span data-stu-id="04459-121">For example, when you want to place items in a bin for quality control, you can use the movement worksheet to plan this action and then create a movement to make instructions for an employee.</span></span>  

1.  <span data-ttu-id="04459-122">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Lagerplatzumlagerungsvorschlag** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="04459-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="04459-123">Wählen Sie die **Lagerplatzinhalt holen** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="04459-123">Choose the **Get Bin Content** action.</span></span> <span data-ttu-id="04459-124">Sie verwenden die Anforderungsseite, um Filter auf die Lagerplätze und Artikel zu setzen, die in den Lagerplatzumlagerungsvorschlagszeilen erscheinen sollen.</span><span class="sxs-lookup"><span data-stu-id="04459-124">Use the request page to filter which bins and items you want to appear on the movement worksheet lines.</span></span>  
3.  <span data-ttu-id="04459-125">Füllen Sie die entsprechenden Felder in der Anforderungsseite der Stapelverarbeitung aus.</span><span class="sxs-lookup"><span data-stu-id="04459-125">Fill in the relevant fields in the batch job request page.</span></span> <span data-ttu-id="04459-126">Wenn Sie z. B. den Lagerplatzinhalt aller Lagerplätze in einer bestimmten Zone des Lagerorts sehen möchten, füllen Sie das Feld **Zonencode** aus.</span><span class="sxs-lookup"><span data-stu-id="04459-126">For example, if you want to see the bin content of all the bins in a certain zone at the location, fill in the **Zone Code** field.</span></span> <span data-ttu-id="04459-127">Wenn Sie Zeilen für alle Lagerplätze holen möchten, die einen bestimmten Artikel enthalten, füllen Sie das Feld **Artikelnr.** aus.</span><span class="sxs-lookup"><span data-stu-id="04459-127">If you want to retrieve lines for each bin that contains a particular item, fill in the **Item No.** field.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="04459-128">Sie können Artikel aus einem Lagerplatz der Lagerplatzart "Wareneingang" nicht manuell ein- oder auslagern, da Artikel in Lagerplätzen der Art "Wareneingang" als eingelagert registriert sein müssen, bevor sie ein Teil des verfügbaren Lagerbestands sind.</span><span class="sxs-lookup"><span data-stu-id="04459-128">You cannot manually move items in or out of a bin of bin type RECEIVE, because items that are in a RECEIVE-type bin must be registered as being put away before they are part of available inventory.</span></span>  

4.  <span data-ttu-id="04459-129">Wenn Sie viele Zeilen abrufen, wählen Sie **Sortierung**, um eine Sortiermethode zum Festlegen der Reihenfolge auszuwählen, in der die Zeilen im Vorschlag erscheinen sollen, und wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="04459-129">If you are retrieving many lines, choose **Sort** to select a sorting method to determine the order the lines will appear in the worksheet, and then choose the **OK** button.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="04459-130">Umlagerungszeilen werden gemäß FEFO übernommen, wenn Sie die Funktion **Lagerplatzumlagerung erstellen** aktivieren und wenn die folgenden Bedingungen für einen Artikel erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="04459-130">Movement lines are retrieved according to FEFO when you activate the **Get Bin Content** function if the following conditions are met for an item:</span></span>  
    >   
    >  -   <span data-ttu-id="04459-131">Der Artikel weist ein Ablaufdatum auf.</span><span class="sxs-lookup"><span data-stu-id="04459-131">The item has an expiration date.</span></span>  
    > -   <span data-ttu-id="04459-132">Das Feld **Gemäß FEFO kommissionieren** ist auf der Lagerortkarte aktiviert, und</span><span class="sxs-lookup"><span data-stu-id="04459-132">The **Pick According to FEFO** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="04459-133">Das Kontrollkästchen **Kommissionierung erforderlich** muss auf der Lagerortkarte aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="04459-133">The **Bin Mandatory** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="04459-134">Die Felder **Von Zone** und **Von Lagerplatz** sind leer.</span><span class="sxs-lookup"><span data-stu-id="04459-134">The **From Zone** and **From Bin** fields are blank.</span></span>  

5.  <span data-ttu-id="04459-135">Vervollständigen Sie einige der geholten Zeilen, um die Änderungen abzubilden, die Sie durchführen möchten.</span><span class="sxs-lookup"><span data-stu-id="04459-135">Complete some of the retrieved lines to reflect the changes you want to make.</span></span> <span data-ttu-id="04459-136">Für jeden Artikel, den Sie umlagern möchten, müssen Sie die Felder **Artikelnr.**, **Von Lagerplatzcode**, **Nach Lagerplatzcode** und **Menge** ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="04459-136">For each item that you want to move, you must fill in the **Item No.**, **From Bin Code**, **To Bin Code**, and **Quantity** fields.</span></span>  
6.  <span data-ttu-id="04459-137">Löschen Sie alle unvollständigen Zeilen, die Sie nur zu Informationszwecken verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="04459-137">Delete the incomplete lines that you used for information.</span></span>  
7.  <span data-ttu-id="04459-138">Sobald die Lagerplatzumlagerungsvorschlagszeilen genau die Umlagerungen darstellen, die von dem Lagermitarbeiter ausgeführt werden sollen, wählen Sie die Aktionen **Lagerplatzumlagerung erstellen**, um die Anweisungen für den Mitarbeiter zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="04459-138">Once the movement worksheet lines accurately reflect how the movement action should be carried out by the warehouse employee, choose the **Create Movement** action to create the instructions for the employee.</span></span>  

## <a name="see-also"></a><span data-ttu-id="04459-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04459-139">See Also</span></span>  
[<span data-ttu-id="04459-140">Logistik</span><span class="sxs-lookup"><span data-stu-id="04459-140">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="04459-141">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="04459-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="04459-142">[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="04459-142">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="04459-143">[Montageverwaltung](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="04459-143">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="04459-144">Designdetails: Logistik</span><span class="sxs-lookup"><span data-stu-id="04459-144">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="04459-145">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="04459-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
