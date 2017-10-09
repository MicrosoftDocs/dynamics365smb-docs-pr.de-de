---
title: Erstellen von Budgets| Microsoft Docs
description: "Erstellen Sie Budgets, um verschiedene Finanzaktivitäten zu prognostizieren und Dimensionen zu den einzelnen Intelligence-Zwecken zuzuordnen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 06/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: cda69d70ece090a149a13e5e1f4ed02fa70c49f7
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create--budgets"></a><span data-ttu-id="549d6-103">So wird's gemacht: neue Budgets erzeugen</span><span class="sxs-lookup"><span data-stu-id="549d6-103">How to: Create  Budgets</span></span>
<span data-ttu-id="549d6-104">Sie können für dieselbe Periode mehrere Budgets verwalten, indem Sie Budgets mit verschiedenen Namen einrichten.</span><span class="sxs-lookup"><span data-stu-id="549d6-104">You can have multiple budgets for identical time periods by creating budgets with separate names.</span></span> <span data-ttu-id="549d6-105">Zuerst richten Sie den Budgetnamen ein und geben die Budgetzahlen ein.</span><span class="sxs-lookup"><span data-stu-id="549d6-105">First, you set up the budget name and enter the budget figures.</span></span> <span data-ttu-id="549d6-106">Der Budgetname wird dann allen Budgetposten zugewiesen, die Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="549d6-106">The budget name is then included on all the budget entries you create.</span></span>  

 <span data-ttu-id="549d6-107">Wenn Sie ein Budget erstellen, können Sie für jedes Budget vier Dimensionen festlegen.</span><span class="sxs-lookup"><span data-stu-id="549d6-107">When you create a budget, you can define four dimensions for each budget.</span></span> <span data-ttu-id="549d6-108">Diese bugetspezifischen Dimensionen werden Budgetdimensionen genannt.</span><span class="sxs-lookup"><span data-stu-id="549d6-108">These budget-specific dimensions are called budget dimensions.</span></span> <span data-ttu-id="549d6-109">Sie wählen die Budgetdimensionen für jedes Budget aus den Dimensionen, die Sie bereits eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="549d6-109">You select the budget dimensions for each budget from among the dimensions you have already set up.</span></span> <span data-ttu-id="549d6-110">Budgetdimensionen können Budgetposten hinzugefügt werden und als Filter für ein Budget verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="549d6-110">Budget dimensions can be used to set filters on a budget and to add dimension information to budget entries.</span></span> <span data-ttu-id="549d6-111">Weitere Informationen finden Sie unter [Arbeiten mit Dimensionen](finance-dimensions.md)</span><span class="sxs-lookup"><span data-stu-id="549d6-111">For more information, see [Working with Dimensions](finance-dimensions.md).</span></span>

 <span data-ttu-id="549d6-112">Budgets spielen eine wichtige Rolle in der Business Intelligence wie Finanzauswertung auf Basis von Kontenschemata, die erneut den Budgetposten enthalten, oder beim geplant Analysieren von tatsächlichen Beträgen im Kontenplan.</span><span class="sxs-lookup"><span data-stu-id="549d6-112">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="549d6-113">Weitere Informationen finden Sie unter [Business Intelligence](bi.md).</span><span class="sxs-lookup"><span data-stu-id="549d6-113">For more information, see [Business Intelligence](bi.md).</span></span>

 <span data-ttu-id="549d6-114">Budgets spielen eine wichtige Rolle in der Business Intelligence wie Finanzauswertung auf Basis von Kontenschemata, die erneut den Budgetposten enthalten, oder beim geplant Analysieren von tatsächlichen Beträgen im Kontenplan.</span><span class="sxs-lookup"><span data-stu-id="549d6-114">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="549d6-115">Weitere Informationen finden Sie unter [Business Intelligence](bi.md).</span><span class="sxs-lookup"><span data-stu-id="549d6-115">For more information, see [Business Intelligence](bi.md).</span></span>

<span data-ttu-id="549d6-116">In der Kostenrechnung arbeiten Sie mit Kostenbudgets auf ähnliche Weise.</span><span class="sxs-lookup"><span data-stu-id="549d6-116">In cost accounting, you work with cost budgets in a similar way.</span></span> <span data-ttu-id="549d6-117">Weitere Informationen finden Sie unter [Gewusst wie: Budgets erstellen](finance-create-cost-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="549d6-117">For more information, see [Creating Cost Budgets](finance-create-cost-budgets.md).</span></span>    

 > [!NOTE]  
>   <span data-ttu-id="549d6-118">Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="549d6-118">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="549d6-119">Weitere Informationen finden Sie unter [Anpassen Ihrer [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)Experience.</span><span class="sxs-lookup"><span data-stu-id="549d6-119">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>  

### <a name="to-create-a-new-budget"></a><span data-ttu-id="549d6-120">Einrichten eines neuen Budgets</span><span class="sxs-lookup"><span data-stu-id="549d6-120">To create a new budget</span></span>  

1. <span data-ttu-id="549d6-121">Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen] Symbol (media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **G/L-Blatt Budgets** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="549d6-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **G/L Budgets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="549d6-122">Wählen Sie die Aktion **Liste bearbeiten** aus, und füllen Sie die Felder nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="549d6-122">Choose the **Edit List** action, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="549d6-123">Wählen Sie die Aktion **Buch.-Blatt bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="549d6-123">Choose the **Edit Budget** action.</span></span>
4. <span data-ttu-id="549d6-124">Im Fenster oben von **Budget** füllen Sie die Felder aus, um anzuzeigen, was gezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="549d6-124">At the top of the **Budget** window, fill in the fields as necessary to define what is displayed.</span></span>  

    <span data-ttu-id="549d6-125">Nur Posten, die diesen Budgetnamen enthalten, der im Feld **Artikelbudgetname** angezeigt wird, werden nun angezeigt.</span><span class="sxs-lookup"><span data-stu-id="549d6-125">Only entries that contain the budget name that you entered in the **budget Name** field are shown.</span></span> <span data-ttu-id="549d6-126">Da der Budgetname gerade erstellt wurde, gibt es keine Posten, die dem Filter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="549d6-126">Because the budget name has just been created, there are no entries that match the filter.</span></span> <span data-ttu-id="549d6-127">Daher ist das Fenster leer.</span><span class="sxs-lookup"><span data-stu-id="549d6-127">Therefore, the window is empty.</span></span>  
5. <span data-ttu-id="549d6-128">Wählen Sie zum Eingeben eines Betrags die entsprechende Zelle in der Matrix.</span><span class="sxs-lookup"><span data-stu-id="549d6-128">To enter an amount, choose the relevant cell in the matrix.</span></span> <span data-ttu-id="549d6-129">Das Fenster **Finanzbudgetposten** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="549d6-129">The **G/L Budget Entries** window opens.</span></span>  
6. <span data-ttu-id="549d6-130">Erstellen Sie eine neue Zeile, und füllen Sie das Feld **Betrag** aus.</span><span class="sxs-lookup"><span data-stu-id="549d6-130">Create a new line and fill in the **Amount** field.</span></span> <span data-ttu-id="549d6-131">Schließen Sie das Fenster **Finanzbudgetposten**.</span><span class="sxs-lookup"><span data-stu-id="549d6-131">Close the **G/L Budget Entries** window.</span></span>  
7. <span data-ttu-id="549d6-132">Wiederholen Sie die Schritte 5 bis 6, bis alle Budgetbeträge eingegeben sind.</span><span class="sxs-lookup"><span data-stu-id="549d6-132">Repeat steps 5 and 6 until you have entered all of the budget amounts.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="549d6-133">Im Inforegister  **Filter** stehen zwischen vier und acht Filter zur Verfügung, abhängig davon, wie viele  Budgetdimensionen für den Budgetnamen eingerichtet wurden.</span><span class="sxs-lookup"><span data-stu-id="549d6-133">On the **Filters** FastTab, you can filter the budget information by budget dimensions you have set up under the budget name.</span></span>   

## <a name="see-also"></a><span data-ttu-id="549d6-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="549d6-134">See Also</span></span>
[<span data-ttu-id="549d6-135">Finanzen</span><span class="sxs-lookup"><span data-stu-id="549d6-135">Finance</span></span>](finance.md)  
[<span data-ttu-id="549d6-136">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="549d6-136">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="549d6-137">Finance einrichten</span><span class="sxs-lookup"><span data-stu-id="549d6-137">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="549d6-138">Die Finanzbuchhaltung und der Kontenplan</span><span class="sxs-lookup"><span data-stu-id="549d6-138">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="549d6-139">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="549d6-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

