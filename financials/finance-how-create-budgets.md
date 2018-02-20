---
title: Erstellen von Sachkontenbudgets| Microsoft Docs
description: "Erstellen Sie Sachkonten-Budgets, um verschiedene Finanzaktivitäten zu prognostizieren und Dimensionen zu den einzelnen Intelligence-Zwecken zuzuordnen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f6969d05cfde9ba7ce5767a961d4af1c7b3bd983
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="create-gl-budgets"></a><span data-ttu-id="6d602-103">Sachkontenbudgets erstellen</span><span class="sxs-lookup"><span data-stu-id="6d602-103">Create G/L Budgets</span></span>
<span data-ttu-id="6d602-104">Sie können für dieselbe Periode mehrere Budgets verwalten, indem Sie Budgets mit verschiedenen Namen einrichten.</span><span class="sxs-lookup"><span data-stu-id="6d602-104">You can have multiple budgets for identical time periods by creating budgets with separate names.</span></span> <span data-ttu-id="6d602-105">Zuerst richten Sie den Budgetnamen ein und geben die Budgetzahlen ein.</span><span class="sxs-lookup"><span data-stu-id="6d602-105">First, you set up the budget name and enter the budget figures.</span></span> <span data-ttu-id="6d602-106">Der Budgetname wird dann allen Budgetposten zugewiesen, die Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="6d602-106">The budget name is then included on all the budget entries you create.</span></span>  

 <span data-ttu-id="6d602-107">Wenn Sie ein Budget erstellen, können Sie für jedes Budget vier Dimensionen festlegen.</span><span class="sxs-lookup"><span data-stu-id="6d602-107">When you create a budget, you can define four dimensions for each budget.</span></span> <span data-ttu-id="6d602-108">Diese bugetspezifischen Dimensionen werden Budgetdimensionen genannt.</span><span class="sxs-lookup"><span data-stu-id="6d602-108">These budget-specific dimensions are called budget dimensions.</span></span> <span data-ttu-id="6d602-109">Sie wählen die Budgetdimensionen für jedes Budget aus den Dimensionen, die Sie bereits eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="6d602-109">You select the budget dimensions for each budget from among the dimensions you have already set up.</span></span> <span data-ttu-id="6d602-110">Budgetdimensionen können Budgetposten hinzugefügt werden und als Filter für ein Budget verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6d602-110">Budget dimensions can be used to set filters on a budget and to add dimension information to budget entries.</span></span> <span data-ttu-id="6d602-111">Weitere Informationen finden Sie unter [Arbeiten mit Dimensionen](finance-dimensions.md)</span><span class="sxs-lookup"><span data-stu-id="6d602-111">For more information, see [Working with Dimensions](finance-dimensions.md).</span></span>

 <span data-ttu-id="6d602-112">Budgets spielen eine wichtige Rolle in der Business Intelligence wie Finanzauswertung auf Basis von Kontenschemata, die erneut den Budgetposten enthalten, oder beim geplant Analysieren von tatsächlichen Beträgen im Kontenplan.</span><span class="sxs-lookup"><span data-stu-id="6d602-112">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="6d602-113">Weitere Informationen finden Sie unter [Business Intelligence](bi.md).</span><span class="sxs-lookup"><span data-stu-id="6d602-113">For more information, see [Business Intelligence](bi.md).</span></span>

 <span data-ttu-id="6d602-114">Budgets spielen eine wichtige Rolle in der Business Intelligence wie Finanzauswertung auf Basis von Kontenschemata, die erneut den Budgetposten enthalten, oder beim geplant Analysieren von tatsächlichen Beträgen im Kontenplan.</span><span class="sxs-lookup"><span data-stu-id="6d602-114">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="6d602-115">Weitere Informationen finden Sie unter [Business Intelligence](bi.md).</span><span class="sxs-lookup"><span data-stu-id="6d602-115">For more information, see [Business Intelligence](bi.md).</span></span>

<span data-ttu-id="6d602-116">In der Kostenrechnung arbeiten Sie mit Kostenbudgets auf ähnliche Weise.</span><span class="sxs-lookup"><span data-stu-id="6d602-116">In cost accounting, you work with cost budgets in a similar way.</span></span> <span data-ttu-id="6d602-117">Weitere Informationen finden Sie unter [Gewusst wie: Budgets erstellen](finance-create-cost-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="6d602-117">For more information, see [Creating Cost Budgets](finance-create-cost-budgets.md).</span></span>    

## <a name="to-create-a-new-gl-budget"></a><span data-ttu-id="6d602-118">Einrichten eines neuen Sachkonten-Budgets</span><span class="sxs-lookup"><span data-stu-id="6d602-118">To create a new G/L budget</span></span>  
1. <span data-ttu-id="6d602-119">Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **G/L-Blatt Budgets** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="6d602-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **G/L Budgets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6d602-120">Wählen Sie die Aktion **Liste bearbeiten** aus, und füllen Sie die Felder nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="6d602-120">Choose the **Edit List** action, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="6d602-121">Wählen Sie die Aktion **Buch.-Blatt bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="6d602-121">Choose the **Edit Budget** action.</span></span>
4. <span data-ttu-id="6d602-122">Im Fenster oben von **Budget** füllen Sie die Felder aus, um anzuzeigen, was gezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6d602-122">At the top of the **Budget** window, fill in the fields as necessary to define what is displayed.</span></span>  

    <span data-ttu-id="6d602-123">Nur Posten, die diesen Budgetnamen enthalten, der im Feld **Artikelbudgetname** angezeigt wird, werden nun angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6d602-123">Only entries that contain the budget name that you entered in the **budget Name** field are shown.</span></span> <span data-ttu-id="6d602-124">Da der Budgetname gerade erstellt wurde, gibt es keine Posten, die dem Filter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6d602-124">Because the budget name has just been created, there are no entries that match the filter.</span></span> <span data-ttu-id="6d602-125">Daher ist das Fenster leer.</span><span class="sxs-lookup"><span data-stu-id="6d602-125">Therefore, the window is empty.</span></span>  
5. <span data-ttu-id="6d602-126">Wählen Sie zum Eingeben eines Betrags die entsprechende Zelle in der Matrix.</span><span class="sxs-lookup"><span data-stu-id="6d602-126">To enter an amount, choose the relevant cell in the matrix.</span></span> <span data-ttu-id="6d602-127">Das Fenster **Finanzbudgetposten** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="6d602-127">The **G/L Budget Entries** window opens.</span></span>  
6. <span data-ttu-id="6d602-128">Erstellen Sie eine neue Zeile, und füllen Sie das Feld **Betrag** aus.</span><span class="sxs-lookup"><span data-stu-id="6d602-128">Create a new line and fill in the **Amount** field.</span></span> <span data-ttu-id="6d602-129">Schließen Sie das Fenster **Finanzbudgetposten**.</span><span class="sxs-lookup"><span data-stu-id="6d602-129">Close the **G/L Budget Entries** window.</span></span>  
7. <span data-ttu-id="6d602-130">Wiederholen Sie die Schritte 5 bis 6, bis alle Budgetbeträge eingegeben sind.</span><span class="sxs-lookup"><span data-stu-id="6d602-130">Repeat steps 5 and 6 until you have entered all of the budget amounts.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="6d602-131">Im Inforegister **Filter** stehen zwischen vier und acht Filter zur Verfügung, abhängig davon, wie viele Budgetdimensionen für den Budgetnamen eingerichtet wurden.</span><span class="sxs-lookup"><span data-stu-id="6d602-131">On the **Filters** FastTab, you can filter the budget information by budget dimensions you have set up under the budget name.</span></span>   

## <a name="see-also"></a><span data-ttu-id="6d602-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d602-132">See Also</span></span>
[<span data-ttu-id="6d602-133">Finanzen</span><span class="sxs-lookup"><span data-stu-id="6d602-133">Finance</span></span>](finance.md)  
[<span data-ttu-id="6d602-134">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="6d602-134">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="6d602-135">Finance einrichten</span><span class="sxs-lookup"><span data-stu-id="6d602-135">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="6d602-136">Die Finanzbuchhaltung und der Kontenplan</span><span class="sxs-lookup"><span data-stu-id="6d602-136">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="6d602-137">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6d602-137">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

