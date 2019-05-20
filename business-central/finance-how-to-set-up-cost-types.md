---
title: 'Vorgehensweise: Einrichten eines Kostenartenplans | Microsoft Docs'
description: Kostenartenpläne ähneln Kontenpläne im Sachkonto.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger, accounts
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: e0bf6a8c7595155785949ed51c765fef0524173b
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1240487"
---
# <a name="set-up-cost-types"></a><span data-ttu-id="ee252-103">Einrichten von Kostenträgern</span><span class="sxs-lookup"><span data-stu-id="ee252-103">Set Up Cost Types</span></span>
<span data-ttu-id="ee252-104">Kostenartenpläne ähneln Kontenpläne im Sachkonto.</span><span class="sxs-lookup"><span data-stu-id="ee252-104">The chart of cost types is similar to the chart of accounts in the general ledger.</span></span> <span data-ttu-id="ee252-105">Sie können den Kostenartenplan auf die folgenden Weisen einrichten:</span><span class="sxs-lookup"><span data-stu-id="ee252-105">You can set up the chart of cost types in the following ways:</span></span>  

-   <span data-ttu-id="ee252-106">Strukturieren Sie den Kostenartenplan ähnlich wie GuV-Konten im Sachkontenplan.</span><span class="sxs-lookup"><span data-stu-id="ee252-106">Structure the chart of cost types similar to the income statement accounts in the general ledger chart of accounts.</span></span> <span data-ttu-id="ee252-107">Dann können Sie den Sachkontenplan in den Kostenartenplan übertragen.</span><span class="sxs-lookup"><span data-stu-id="ee252-107">Then, you can transfer the general ledger chart of accounts to the chart of cost types.</span></span> <span data-ttu-id="ee252-108">Sie können alle notwendigen Änderungen nach der Übertragung vornehmen.</span><span class="sxs-lookup"><span data-stu-id="ee252-108">You can make any necessary adjustments after the transfer.</span></span>  
-   <span data-ttu-id="ee252-109">Erstellen Sie einen neuen Kostenartenplan, oder fügen Sie einem vorhandenen Kostenartenplan neue Kostenarten hinzu.</span><span class="sxs-lookup"><span data-stu-id="ee252-109">Create new chart of cost types or add new cost types to existing chart of cost types.</span></span> <span data-ttu-id="ee252-110">Sie müssen jede neue Kostenart einzeln erstellen.</span><span class="sxs-lookup"><span data-stu-id="ee252-110">You must create each new cost type individually.</span></span>  

## <a name="to-transfer-the-general-ledger-chart-of-accounts-to-the-chart-of-cost-types"></a><span data-ttu-id="ee252-111">So übertragen Sie den Sachkontenplan in den Kostenartenplan.</span><span class="sxs-lookup"><span data-stu-id="ee252-111">To transfer the general ledger chart of accounts to the chart of cost types</span></span>  
1.  <span data-ttu-id="ee252-112">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontenplan Kontenarten** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="ee252-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Types**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ee252-113">Wählen Sie die Aktion **Kostenarten aus K&ontenplan abrufen**.</span><span class="sxs-lookup"><span data-stu-id="ee252-113">Choose the **Get Cost Types from Chart of Accounts** action.</span></span> <span data-ttu-id="ee252-114">Klicken Sie im Dialogfeld auf die Schaltfläche **Ja**, um die Übertragung zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="ee252-114">In the dialog box, choose the **Yes** button to confirm the transfer.</span></span> <span data-ttu-id="ee252-115">Die Funktion verwendet den Kontenplan, um einen Kostenartenplan zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ee252-115">The function uses the chart of accounts to create a chart of cost types.</span></span>  

    <span data-ttu-id="ee252-116">Der Kostenartenplan enthält jetzt alle GuV-Konten im Sachkonto und umfasst Überschriften und Zwischensummen.</span><span class="sxs-lookup"><span data-stu-id="ee252-116">The chart of cost types now contain all income statement accounts in the general ledger and include headings and subtotals.</span></span> <span data-ttu-id="ee252-117">Sie können den Kostenartenplan ändern, falls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ee252-117">You can change the chart of cost types, as necessary.</span></span> <span data-ttu-id="ee252-118">Beispielsweise können Sie doppelt vorhandene Kostenarten löschen.</span><span class="sxs-lookup"><span data-stu-id="ee252-118">For example, you can delete duplicate existing cost types.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="ee252-119">Die **Kostenarten in Kontenplan registrieren**-Funktion aktualisiert das Verhältnis zwischen dem Kontenplan und dem Kostenartenplan.</span><span class="sxs-lookup"><span data-stu-id="ee252-119">The **Register Cost Types in Chart of Accounts** function updates the relationship between the chart of accounts and the chart of cost types.</span></span> <span data-ttu-id="ee252-120">Das Feld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="ee252-120">The **No.**</span></span> <span data-ttu-id="ee252-121">wird ausgefüllt und geprüft, um sicherzustellen, dass jedes Sachkonto mit nur einer Kostenart verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="ee252-121">field is filled and verified to make sure that each general ledger account is related to only one cost type.</span></span> <span data-ttu-id="ee252-122">Die Funktion wird automatisch ausgeführt, bevor Sie Sachposten in die Kostenrechnung übertragen.</span><span class="sxs-lookup"><span data-stu-id="ee252-122">The function runs automatically before transferring general ledger entries to cost accounting.</span></span>  

## <a name="to-set-up-new-cost-types-in-the-chart-of-cost-types-page"></a><span data-ttu-id="ee252-123">So richten Sie auf der Seite "Liquiditätskontenplan" neue Liquiditätskonten ein</span><span class="sxs-lookup"><span data-stu-id="ee252-123">To set up new cost types in the Chart of Cost Types page</span></span>  
1.  <span data-ttu-id="ee252-124">Öffnen Sie die Seite **Kontenplan-Arten** im Bearbeitungsmodus.</span><span class="sxs-lookup"><span data-stu-id="ee252-124">Open the **Chart of Cost Types** page in edit mode.</span></span>  
2.  <span data-ttu-id="ee252-125">Füllen Sie je nach Bedarf die Felder aus.</span><span class="sxs-lookup"><span data-stu-id="ee252-125">Fill in the fields as described as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >  <span data-ttu-id="ee252-126">Sie können Kostenarten auf der Seite **Kostenartkarte** oder auf der Seite **Kostenartenplan** einrichten und verwalten.</span><span class="sxs-lookup"><span data-stu-id="ee252-126">You can set up and maintain cost types in either the **Cost Type Card** page or on the **Chart of Cost Types** page.</span></span> <span data-ttu-id="ee252-127">So richten Sie auf der Seite **Liquiditätskontenplan** neue Liquiditätskonten ein.</span><span class="sxs-lookup"><span data-stu-id="ee252-127">In this procedure, you set up cost types on the **Chart of Cost Types** page.</span></span>

3.  <span data-ttu-id="ee252-128">Nachdem Sie alle Kostenarten erstellt haben, wählen Sie die Aktion **Kostenarten einrücken** aus.</span><span class="sxs-lookup"><span data-stu-id="ee252-128">After you have created all cost types, choose the **Indent Cost Types** action.</span></span> <span data-ttu-id="ee252-129">Klicken Sie im Dialogfeld auf die Schaltfläche **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ee252-129">In the dialog box, choose the **Yes** button.</span></span>  
4.  <span data-ttu-id="ee252-130">Verknüpfen Sie die neue Kostenart mit dem entsprechenden Sachkonto.</span><span class="sxs-lookup"><span data-stu-id="ee252-130">Link the new cost type to the corresponding general ledger account.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="ee252-131">Wenn Sie in den Feldern **Zusammenzählung** Definitionen für die Zeilenart **Bis-Summe** eingetragen haben, bevor Sie die Funktion **Kostenarten einrücken** ausgeführt haben, müssen Sie diese Eintragungen wiederholen, da die Funktion die Werte in allen **Bis-Summe**-Feldern überschreibt.</span><span class="sxs-lookup"><span data-stu-id="ee252-131">If you have entered definitions in the **Totaling** fields for the line type of **End-Total** before you run the **Indent Cost Types** function, then you must enter the definitions again because the function overwrites the values in all **End-Total** fields.</span></span>  

## <a name="to-update-cost-types"></a><span data-ttu-id="ee252-132">So aktualisieren Sie Kostenarten</span><span class="sxs-lookup"><span data-stu-id="ee252-132">To update cost types</span></span>  
1.  <span data-ttu-id="ee252-133">Auf der Seite **Kostenrechnung einrichten**  wählen Sie aus, ob der Kostenartenplan automatisch aktualisiert werden soll, wenn der Kontenplan geändert wird.</span><span class="sxs-lookup"><span data-stu-id="ee252-133">On the **Cost Accounting Setup** page, select if you want the chart of cost types to be automatically updated when the chart of accounts is changed.</span></span>  
2.  <span data-ttu-id="ee252-134">Die folgenden Optionen stehen im Feld **Sachkonto ausrichten** zur Auswahl.</span><span class="sxs-lookup"><span data-stu-id="ee252-134">In the **Align G/L Account** field, you can choose from the following options.</span></span>  

- <span data-ttu-id="ee252-135">**Keine Ausrichtung** - Es gibt keine entsprechende Änderung im Kostenartenplan, wenn Sie den Kontenplan ändern.</span><span class="sxs-lookup"><span data-stu-id="ee252-135">**No Alignment** - There is no corresponding change in the chart of cost types when you change the chart of accounts.</span></span>  
- <span data-ttu-id="ee252-136">**Automatisch** - Es gibt eine entsprechende Änderung im Kostenartenplan, wenn Sie den Kontenplan ändern.</span><span class="sxs-lookup"><span data-stu-id="ee252-136">**Automatic** - A corresponding change is made in the chart of cost types when you change the chart of accounts.</span></span>  
- <span data-ttu-id="ee252-137">**Eingabeaufforderung** - Eine Meldung wird mit der Frage angezeigt, ob Sie die entsprechende Änderung auch im Kostenartenplan vornehmen möchten, wenn Sie den Kontenplan ändern.</span><span class="sxs-lookup"><span data-stu-id="ee252-137">**Prompt** - A message is displayed asking if you want to make a corresponding change in the chart of cost types when you change the chart of accounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ee252-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee252-138">See Also</span></span>  
[<span data-ttu-id="ee252-139">Kostenrechnung</span><span class="sxs-lookup"><span data-stu-id="ee252-139">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="ee252-140">[Definieren von Kostenstellen und Kostenträgern für Kontenpläne](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="ee252-140">[Defining Cost Centers and Cost Objects for Chart of Accounts](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span></span>  
<span data-ttu-id="ee252-141">[Salden zwischen Kostenart, Kostenstelle und Kostenträger](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span><span class="sxs-lookup"><span data-stu-id="ee252-141">[Balances Between Cost Type, Cost Center, and Cost Object](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span></span>  
<span data-ttu-id="ee252-142">[Einrichten der Kostenrechnung](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="ee252-142">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
<span data-ttu-id="ee252-143">[Terminologie der Kostenrechnung](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="ee252-143">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="ee252-144">Informationen zur Kostenrechnung</span><span class="sxs-lookup"><span data-stu-id="ee252-144">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="ee252-145">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ee252-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
