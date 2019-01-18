---
title: 'Vorgehensweise: Einrichten von Kostenstellen| Microsoft Docs'
description: "Kostenstellen sind Abteilungen, die für die Kosten und die Einnahmen zuständig sind. Der Kostenstellenplan ähnelt den Dimensionsinformationen für das Sachkonto."
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
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 252ebf514635ada8e07bfb1e950d0cff156d0bfc
ms.contentlocale: de-de
ms.lasthandoff: 11/26/2018

---
# <a name="set-up-cost-centers"></a><span data-ttu-id="c3dfb-104">Kostenstellen einrichten</span><span class="sxs-lookup"><span data-stu-id="c3dfb-104">Set Up Cost Centers</span></span>
<span data-ttu-id="c3dfb-105">Kostenstellen sind Abteilungen, die für die Kosten und die Einnahmen zuständig sind.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-105">Cost centers are departments that are responsible for costs and income.</span></span> <span data-ttu-id="c3dfb-106">Der Kostenstellenplan ähnelt den Dimensionsinformationen für das Sachkonto.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-106">The chart of cost centers is similar to the dimension information for the general ledger.</span></span> <span data-ttu-id="c3dfb-107">Sie können den Kostenstellenplan auf die folgenden Weisen einrichten:</span><span class="sxs-lookup"><span data-stu-id="c3dfb-107">You can set up the chart of cost centers in the following ways:</span></span>  

-   <span data-ttu-id="c3dfb-108">Transferieren Sie Dimensionswerte im Sachkonto zum Kostenstellenplan.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-108">Transfer dimension values in the general ledger to the chart of cost centers.</span></span> <span data-ttu-id="c3dfb-109">Sie können alle notwendigen Änderungen nach der Übertragung vornehmen.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-109">You can make any necessary adjustments after the transfer.</span></span>  
-   <span data-ttu-id="c3dfb-110">Erstellen Sie einen neuen Kostenstellenplan, der unabhängig vom Sachkonto ist, oder fügen Sie einem vorhandenen Kostenstellenplan eine neue Kostenstelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-110">Create a new chart of cost center that is independent of the general ledger or add a new cost center to an existing chart of cost center.</span></span> <span data-ttu-id="c3dfb-111">Sie müssen jede Kostenstelle einzeln erstellen.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-111">You must create each cost center individually.</span></span>  

## <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers"></a><span data-ttu-id="c3dfb-112">So transferieren Sie Dimensionswerte im Sachkonto zum Kostenstellenplan</span><span class="sxs-lookup"><span data-stu-id="c3dfb-112">To transfer dimension values in the general ledger to the chart of cost centers</span></span>  
1.  <span data-ttu-id="c3dfb-113">Richten Sie eine Dimension als Kostenstellendimension auf der Seite **Kostenstellendimension aktualisieren** ein.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-113">Set up a dimension to be the cost center dimension on the **Update Cost Acctg. Dimensions** page.</span></span> <span data-ttu-id="c3dfb-114">Nur die Werte aus dieser Dimension werden übertragen.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-114">Only the values from this dimension are transferred.</span></span>  
2.  <span data-ttu-id="c3dfb-115">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontenplan Kontenstelle** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Centers**, and then choose the related link.</span></span>  
3.  <span data-ttu-id="c3dfb-116">Klicken Sie auf der Registerkarte **Aktionen** in der Gruppe **Funktion** auf **Kostenstellen aus Dimension abrufen**, um Dimensionswerte zum Kostenstellenplan zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-116">On the **Actions** tab, in the **Functions** group, choose **Get Cost Centers from Dimension** to transfer dimension values to the chart of cost centers.</span></span> <span data-ttu-id="c3dfb-117">Die Funktion überträgt die Dimensionswerte, die Sie in Schritt 1 definiert haben.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-117">The function transfers the dimension values that you defined in step 1.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="c3dfb-118">Sie können das Feld **Kostenstellendimension ausrichten** so einrichten, dass eine unidirektionale Synchronisierung von Dimensionswerten aus dem Sachkonto zum Kostenstellenplan definiert wird.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-118">You can set up the **Align Cost Center Dimension**  field to define a one-way synchronization of dimension values from the general ledger to the chart of cost centers.</span></span> <span data-ttu-id="c3dfb-119">Sie können keine Synchronisierung des Kostenstellenplans mit Dimensionswerten aus dem Sachkonto definieren.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-119">You cannot define a synchronization of the chart of cost centers to dimension values from the general ledger.</span></span>  

<span data-ttu-id="c3dfb-120">Der Kostenstellenplan enthält jetzt alle angegebenen Dimensionswerte aus dem Sachkonto und umfasst Titel und Zwischensummen.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-120">The chart of cost centers now contains all specified dimension values from the general ledger and includes titles and subtotals.</span></span>  

## <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-page"></a><span data-ttu-id="c3dfb-121">So richten Sie auf der Seite Kostenstellenplan neue Kostenstellen ein</span><span class="sxs-lookup"><span data-stu-id="c3dfb-121">To create new cost centers in the Chart of Cost Centers page</span></span>  
<span data-ttu-id="c3dfb-122">Sie können Kostenkarten auf der Seite **Kostenstellen** oder auf der Seite **Kostenstellenkarte** einrichten und verwalten.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-122">You can set up and maintain cost centers in either the **Cost Center Card** card or on the **Chart of Cost Centers** page.</span></span> <span data-ttu-id="c3dfb-123">So richten Sie auf der Seite **Kostenstellenplan** neue Kostenstellen ein.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-123">In this procedure, you set up cost centers on the **Chart of Cost Centers** page.</span></span>  

1. <span data-ttu-id="c3dfb-124">Öffnen Sie die Seite **Kontenplan-Kostenstellen** im Bearbeitungsmodus.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-124">Open the **Chart of Cost Centers** page in edit mode.</span></span>  
2. <span data-ttu-id="c3dfb-125">Geben Sie im Feld **Code** den Kostenstellencode ein.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-125">In the **Code** field, enter the cost center code.</span></span> <span data-ttu-id="c3dfb-126">Alle Kostenstellen müssen einen Code aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-126">All cost centers must have a code.</span></span>  
3. <span data-ttu-id="c3dfb-127">Geben Sie im Feld **Namen** den Kostenstellennamen ein.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-127">In the **Name** field, enter the cost center name.</span></span>  
4. <span data-ttu-id="c3dfb-128">Wählen Sie den Dropdownpfeil im Feld **Positionstyp** aus, um den Zweck der Kostenstelle anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-128">Choose the drop-down arrow in the **Line Type** field to specify the purpose of the cost center.</span></span>  

    - <span data-ttu-id="c3dfb-129">Für Kostenstellen der Art **Summe** müssen Sie das Feld **Zusammenzählung** ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-129">For cost centers of the **Total** type, you must fill in the **Totaling** field.</span></span> <span data-ttu-id="c3dfb-130">Verwenden Sie den **Oder**-Operator, der eine vertikale Zeile (**&#124;**) ist, um Bereiche von Kostenstellen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-130">Use the **or** operator, which is a vertical line (**&#124;**) to set ranges of cost centers.</span></span>  
    - <span data-ttu-id="c3dfb-131">Für Kostenstellen der **Bis-Summe**-Zeilenart wird dieses Feld automatisch ausgefüllt, wenn Sie die Einzugsfunktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-131">For cost centers of the **End-Total** line type, this field is filled in automatically when you use the indent function.</span></span>  
5.  <span data-ttu-id="c3dfb-132">Füllen Sie die Felder **Sortierreihenfolge** und **Kostenunterart** aus.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-132">Fill in the **Sorting Order** and **Cost Subtype** fields.</span></span>  
6.  <span data-ttu-id="c3dfb-133">Wählen Sie die nächste leere Zeile aus, um eine neue Kostenstelle zu erstellen. Wiederholen Sie dann die Schritte 2 bis 5.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-133">Choose the next empty line to create a new cost center, and then repeat steps 2 through 5.</span></span>  
7.  <span data-ttu-id="c3dfb-134">Nachdem Sie alle Kostenstellen eingerichtet haben, wählen Sie die Aktion **Kostenstellen einrücken** aus.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-134">After you have set up all the cost centers, choose the **Indent Cost Centers** action.</span></span> <span data-ttu-id="c3dfb-135">Wählen Sie die Schaltfläche **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-135">Choose the **Yes** button.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="c3dfb-136">Wenn Sie Definitionen in den **Zusammenzählung**-Feldern für **Bis-Summe**-Kostenstellen eingegeben haben, bevor Sie die Einzugsfunktion ausführen, müssen Sie sie noch einmal eingeben.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-136">If you have entered definitions in the **Totaling** fields for **End-Total** cost centers before you run the indent function, then you must enter them again.</span></span> <span data-ttu-id="c3dfb-137">Die Funktion überschreibt die Werte in allen **Bis-Summe**-Feldern.</span><span class="sxs-lookup"><span data-stu-id="c3dfb-137">The function overwrites the values in all **End-Total** fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c3dfb-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3dfb-138">See Also</span></span>  
[<span data-ttu-id="c3dfb-139">Kostenrechnung</span><span class="sxs-lookup"><span data-stu-id="c3dfb-139">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="c3dfb-140">[Einrichten der Kostenrechnung](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="c3dfb-140">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
<span data-ttu-id="c3dfb-141">[Terminologie der Kostenrechnung](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="c3dfb-141">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="c3dfb-142">Informationen zur Kostenrechnung</span><span class="sxs-lookup"><span data-stu-id="c3dfb-142">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="c3dfb-143">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c3dfb-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

