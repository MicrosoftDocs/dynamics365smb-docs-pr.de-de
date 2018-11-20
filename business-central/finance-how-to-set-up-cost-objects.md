---
title: "Vorgehensweise: Einrichten von Kostenträgern| Microsoft Docs"
description: "Erfahren Sie, wie Sie Kostenträger eingerichtet werden, die gleich sind wie Dimensionen in der Finanzbuchhaltung."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.translationtype: HT
ms.sourcegitcommit: 67400e424305cc705db5c1bd52a8e4de17ecc5a9
ms.openlocfilehash: 28ab54dea21385083eb61e5dc8a7df44aef0ea21
ms.contentlocale: de-de
ms.lasthandoff: 11/20/2018

---
# <a name="set-up-cost-objects"></a><span data-ttu-id="0ad43-103">Einrichten von Kostenträgern</span><span class="sxs-lookup"><span data-stu-id="0ad43-103">Set Up Cost Objects</span></span>
<span data-ttu-id="0ad43-104">Kostenträger sind Projekte, Produkte oder Services eines Unternehmens.</span><span class="sxs-lookup"><span data-stu-id="0ad43-104">Cost objects are projects, products, or services of a company.</span></span> <span data-ttu-id="0ad43-105">Der Kostenträgerplan ähnelt den Dimensionsinformationen für das Sachkonto.</span><span class="sxs-lookup"><span data-stu-id="0ad43-105">The chart of cost objects is similar to the dimension information for the general ledger.</span></span> <span data-ttu-id="0ad43-106">Sie können den Kostenträgerplan auf die folgenden Weisen einrichten:</span><span class="sxs-lookup"><span data-stu-id="0ad43-106">You can set up the chart of cost objects in the following ways:</span></span>  

* <span data-ttu-id="0ad43-107">Transferieren Sie Dimensionswerte im Sachkonto zum Kostenträgerplan.</span><span class="sxs-lookup"><span data-stu-id="0ad43-107">Transfer dimension values in the general ledger to the chart of cost objects.</span></span> <span data-ttu-id="0ad43-108">Sie können alle notwendigen Änderungen nach der Übertragung vornehmen.</span><span class="sxs-lookup"><span data-stu-id="0ad43-108">You can make any necessary adjustments after the transfer.</span></span>  
* <span data-ttu-id="0ad43-109">Erstellen Sie einen neuen Kostenträgerplan, der unabhängig vom Sachkonto ist, oder fügen Sie einem vorhandenen Kostenträgerplan einen neuen Kostenträger hinzu.</span><span class="sxs-lookup"><span data-stu-id="0ad43-109">Create a new chart of cost object that is independent of the general ledger or add a new cost object to an existing chart of cost objects.</span></span> <span data-ttu-id="0ad43-110">Sie müssen jeden Kostenträger einzeln erstellen.</span><span class="sxs-lookup"><span data-stu-id="0ad43-110">You must create each cost object individually.</span></span>  

## <a name="to-transfer-dimension-values-from-the-general-ledger-to-the-chart-of-cost-objects"></a><span data-ttu-id="0ad43-111">So transferieren Sie Dimensionswerte aus dem Sachkonto zum Kostenträgerplan</span><span class="sxs-lookup"><span data-stu-id="0ad43-111">To transfer dimension values from the general ledger to the chart of cost objects</span></span>  
1.  <span data-ttu-id="0ad43-112">Legen Sie eine Dimension als Kostenträgerdimension im Fenster **Kostenträger-Dimensionen aktualisieren** fest.</span><span class="sxs-lookup"><span data-stu-id="0ad43-112">Set a dimension to be the cost object dimension in the **Update CA Dimensions** window.</span></span> <span data-ttu-id="0ad43-113">Nur die Werte aus dieser Dimension werden übertragen.</span><span class="sxs-lookup"><span data-stu-id="0ad43-113">Only the values from this dimension are transferred.</span></span>  
2.  <span data-ttu-id="0ad43-114">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontenplan Kostenobjekte** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="0ad43-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Objects**, and then choose the related link.</span></span>  
3.  <span data-ttu-id="0ad43-115">Wählen Sie die Aktion **Kostenträger aus Dimension abrufen**, um Dimensionswerte zum Kostenträgerplan zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="0ad43-115">Choose the **Get Cost Objects from Dimension** action to transfer dimension values to the chart of cost objects.</span></span> <span data-ttu-id="0ad43-116">Die Funktion überträgt die Dimensionswerte, die Sie in Schritt 1 definiert haben.</span><span class="sxs-lookup"><span data-stu-id="0ad43-116">The function transfers the dimension values that you defined in step 1.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="0ad43-117">Sie können das Feld **Kostenträgerdimension ausrichten** so einrichten, dass eine unidirektionale Synchronisierung von Dimensionswerten aus dem Sachkonto zum Kostenträgerplan definiert wird.</span><span class="sxs-lookup"><span data-stu-id="0ad43-117">You can set up the **Align Cost Object Dimension**  field to define a one-way synchronization of dimension values from the general ledger to the chart of cost objects.</span></span> <span data-ttu-id="0ad43-118">Sie können keine Synchronisierung des Kostenträgerplans mit Dimensionswerten aus dem Sachkonto definieren.</span><span class="sxs-lookup"><span data-stu-id="0ad43-118">You cannot define a synchronization of the chart of cost objects to dimension values from the general ledger.</span></span>  

<span data-ttu-id="0ad43-119">Der Kostenträgerplan enthält jetzt alle angegebenen Dimensionswerte aus dem Sachkonto und umfasst Titel und Zwischensummen.</span><span class="sxs-lookup"><span data-stu-id="0ad43-119">The chart of cost objects now contains all specified dimension values from the general ledger and includes titles and subtotals.</span></span>  

## <a name="to-create-new-cost-objects-in-the-chart-of-cost-objects-window"></a><span data-ttu-id="0ad43-120">So richten Sie im Fenster Kostenstellenträger neue Kostenträger ein</span><span class="sxs-lookup"><span data-stu-id="0ad43-120">To create new cost objects in the Chart of Cost Objects window</span></span>  
<span data-ttu-id="0ad43-121">Sie können Kostenkarten im Fenster **Kostenträger** oder im Fenster **Kostenträgerkarte** einrichten und verwalten.</span><span class="sxs-lookup"><span data-stu-id="0ad43-121">You can set up and maintain cost objects in either the **Cost Object Card** card or in the **Chart of Cost Objects** window.</span></span> <span data-ttu-id="0ad43-122">So richten Sie im Fenster **Kostenträger** neue Kostenstellenträger ein.</span><span class="sxs-lookup"><span data-stu-id="0ad43-122">In this procedure, you set up cost objects in the **Chart of Cost Objects** window.</span></span>  

1.  <span data-ttu-id="0ad43-123">Öffnen Sie das Fenster **Kostenstellenträger** im Bearbeitungsmodus.</span><span class="sxs-lookup"><span data-stu-id="0ad43-123">Open the **Chart of Cost Objects** window in edit mode.</span></span>  
2.  <span data-ttu-id="0ad43-124">Geben Sie im Feld **Code** den Kostenträgercode ein.</span><span class="sxs-lookup"><span data-stu-id="0ad43-124">In the **Code** field, enter the cost object code.</span></span> <span data-ttu-id="0ad43-125">Alle Kostenträger müssen einen Code aufweisen.</span><span class="sxs-lookup"><span data-stu-id="0ad43-125">All cost objects must have a code.</span></span>  
3.  <span data-ttu-id="0ad43-126">Geben Sie im Feld **Namen** den Kostenträgernamen ein.</span><span class="sxs-lookup"><span data-stu-id="0ad43-126">In the **Name** field, enter the cost object name.</span></span>  
4.  <span data-ttu-id="0ad43-127">Wählen Sie den Dropdownpfeil im Feld **Positionstyp** aus, um den Zweck des Kostenträgers anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0ad43-127">Choose the drop-down arrow in the **Line Type** field to specify the purpose of the cost object.</span></span>  

    * <span data-ttu-id="0ad43-128">Für Kostenträger der **Summe**-Zeilenart müssen Sie das Feld **Summe Von/Bis** ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="0ad43-128">For cost objects of the **Total** line type, fill in the **Total From/To** field.</span></span> <span data-ttu-id="0ad43-129">Verwenden Sie den **Oder**-Operator, der eine vertikale Zeile (**&#124;**) ist, um Bereiche von Kostenträgern festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0ad43-129">Use the **or** operator, which is a vertical line (**&#124;**), to set ranges of cost objects.</span></span>  
    * <span data-ttu-id="0ad43-130">Für Kostenträger der **Bis-Summe**-Zeilenart wird dieses Feld automatisch ausgefüllt, wenn Sie die Einzugsfunktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="0ad43-130">For cost objects of the **End-Total** line type, this field is filled in automatically when you use  the indent function.</span></span>  
5.  <span data-ttu-id="0ad43-131">Füllen Sie das Feld **Sortierungsauftrag** aus.</span><span class="sxs-lookup"><span data-stu-id="0ad43-131">Fill in the **Sorting Order** field.</span></span>  
6.  <span data-ttu-id="0ad43-132">Wählen Sie die nächste leere Zeile aus, um einen neuen Kostenträger zu erstellen. Wiederholen Sie dann die Schritte 2 bis 5.</span><span class="sxs-lookup"><span data-stu-id="0ad43-132">Chose the next empty line to create a new cost object, and then repeat steps 2 through 5.</span></span>  
7.  <span data-ttu-id="0ad43-133">Nachdem Sie alle Kostenträger eingerichtet haben, wählen Sie die Aktion **Kostenträger einrücken** aus.</span><span class="sxs-lookup"><span data-stu-id="0ad43-133">After you have set up all the cost objects, choose the **Indent Cost Objects** action.</span></span> <span data-ttu-id="0ad43-134">Wählen Sie die Schaltfläche **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="0ad43-134">Choose the **Yes** button.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="0ad43-135">Wenn Sie Definitionen in den **Summe Von/Bis**-Feldern für **Bis-Summe**-Kostenträger eingegeben haben, bevor Sie die Einzugsfunktion ausführen, müssen Sie sie noch einmal eingeben.</span><span class="sxs-lookup"><span data-stu-id="0ad43-135">If you have entered definitions in the **Total From/To** fields for **End-Total** cost objects before you run the indent function, then you must enter them again.</span></span> <span data-ttu-id="0ad43-136">Die Funktion überschreibt die Werte in allen **Bis-Summe**-Feldern.</span><span class="sxs-lookup"><span data-stu-id="0ad43-136">The function overwrites the values in all **End-Total** fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0ad43-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ad43-137">See Also</span></span>  
[<span data-ttu-id="0ad43-138">Kostenrechnung</span><span class="sxs-lookup"><span data-stu-id="0ad43-138">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="0ad43-139">[Definieren von Kostenstellen und Kostenträgern für Kontenpläne](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="0ad43-139">[Defining Cost Centers and Cost Objects for Chart of Accounts](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span></span>  
<span data-ttu-id="0ad43-140">[Salden zwischen Kostenart, Kostenstelle und Kostenträger](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span><span class="sxs-lookup"><span data-stu-id="0ad43-140">[Balances Between Cost Type, Cost Center, and Cost Object](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span></span>  
<span data-ttu-id="0ad43-141">[Einrichten der Kostenrechnung](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="0ad43-141">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
<span data-ttu-id="0ad43-142">[Terminologie der Kostenrechnung](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="0ad43-142">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="0ad43-143">Informationen zur Kostenrechnung</span><span class="sxs-lookup"><span data-stu-id="0ad43-143">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="0ad43-144">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0ad43-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

