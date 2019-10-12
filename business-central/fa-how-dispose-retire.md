---
title: Anlagen zurücksziehen| Microsoft Docs
description: Sie müssen einen Verkaufswert buchen, wenn Sie eine Anlage verkaufen oder ausrangieren, die storniert werden sollten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: c91015877b661f9939dddc891f601e50c8299557
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306628"
---
# <a name="dispose-of-or-retire-fixed-assets"></a><span data-ttu-id="536d1-103">Anlagen entsorgen oder außer Dienst stellen</span><span class="sxs-lookup"><span data-stu-id="536d1-103">Dispose of or Retire Fixed Assets</span></span>
<span data-ttu-id="536d1-104">Wenn Sie eine Anlage verkaufen oder anderweitig entfernen, muss der Verkaufswert gebucht werden, um den Gewinn oder Verlust zu berechnen und zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="536d1-104">When you sell or otherwise dispose of a fixed asset, the disposal value must be posted to calculate and record the gain or loss.</span></span> <span data-ttu-id="536d1-105">Ein Verkaufsposten muss der letzte gebuchte Posten einer Anlage sein.</span><span class="sxs-lookup"><span data-stu-id="536d1-105">A disposal entry must be the last entry posted for a fixed asset.</span></span> <span data-ttu-id="536d1-106">Für teilweise verkaufte Anlagen können Sie mehrere Verkaufsposten buchen.</span><span class="sxs-lookup"><span data-stu-id="536d1-106">For partially disposed fixed assets, you can post more than one disposal entry.</span></span> <span data-ttu-id="536d1-107">Die Summe aller gebuchten Verkaufsbeträge muss ein Habenposten sein.</span><span class="sxs-lookup"><span data-stu-id="536d1-107">The total of all posted disposal amounts must be a credit amount.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="536d1-108">Falls Sie für den Verkauf einer Anlage eine andere Anlage in Zahlung nehmen, müssen Sie sowohl den Verkauf der alten Anlage als auch die Anschaffung der neuen Anlage buchen.</span><span class="sxs-lookup"><span data-stu-id="536d1-108">If you trade-in a fixed asset for another one, you must record both the sale of the old asset (disposal) and the purchase of the new one (acquisition).</span></span> <span data-ttu-id="536d1-109">Weitere Informationen finden Sie unter [Anschaffen von Anlagen](fa-how-acquire.md).</span><span class="sxs-lookup"><span data-stu-id="536d1-109">For more information, see [Acquire Fixed Assets](fa-how-acquire.md).</span></span>  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a><span data-ttu-id="536d1-110">So buchen Sie einen Verkauf aus dem Anlagen Fibu Buch.-Blatt</span><span class="sxs-lookup"><span data-stu-id="536d1-110">To post a disposal from the fixed asset G/L journal</span></span>
1. <span data-ttu-id="536d1-111">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **FA Buch.-Blätter** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="536d1-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **FA G/L Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="536d1-112">Erstellen Sie eine ursprüngliche Buch.-Blattzeile und füllen Sie die notwendigen Felder aus.</span><span class="sxs-lookup"><span data-stu-id="536d1-112">Create an initial journal line and fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="536d1-113">Wählen Sie im Feld **Anlagenbuchungsart** den **Verkauf**.</span><span class="sxs-lookup"><span data-stu-id="536d1-113">In the **FA Posting Type** field, select **Disposal**.</span></span>  
4. <span data-ttu-id="536d1-114">Wählen Sie die Aktion **Anlagengegenkonto einfügen**.</span><span class="sxs-lookup"><span data-stu-id="536d1-114">Choose the **Insert FA Bal. Account** action.</span></span> <span data-ttu-id="536d1-115">Eine zweite Buch.-Blattzeile wird für das Gegenkonto erstellt, das für die Buchung eines Verkaufs eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="536d1-115">A second journal line is created for the balancing account that is set up for disposal posting.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="536d1-116">Schritt 4 funktioniert nur, wenn Sie Folgendes eingerichtet haben: Auf der Seite **Anlagenbuchungsgruppenkarte** der Buchungsgruppe der Anlage enthält das Feld **Kto. Verkauf** das Sollkonto im Sachkonto und das Feld **Gegenkto Verkauf** enthält das Sachkonto, auf das die Gegenposten für Zuschreibungen gebucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="536d1-116">Step 4 only works if you have set up the following: On the **FA Posting Group Card** page for the posting group of the fixed asset, the **Disposal Account** field contains the general ledger debit account and the **Disposal Bal. Account** field contains the general ledger account to which you want to post balancing entries for appreciation.</span></span> <span data-ttu-id="536d1-117">Weitere Informationen finden Sie unter [So richten Sie Anlagenbuchungsgruppen ein](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span><span class="sxs-lookup"><span data-stu-id="536d1-117">For more information, see [To set up fixed asset posting groups](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span></span>  
5. <span data-ttu-id="536d1-118">Wählen Sie die Aktion **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="536d1-118">Choose the **Post** action.</span></span>  

<span data-ttu-id="536d1-119">Wenn Sie eine Anlage zum Teil verkaufen, müssen Sie die Anlage aufteilen, bevor Sie die Verkaufstransaktion buchen können.</span><span class="sxs-lookup"><span data-stu-id="536d1-119">If you sell or dispose of part of a fixed asset, you must split up the asset before you can record the disposal transaction.</span></span> <span data-ttu-id="536d1-120">Weitere Informationen finden Sie unter [Übertragen, Teilen oder Kombinieren von Anlagen.](fa-how-trans-split-combine.md).</span><span class="sxs-lookup"><span data-stu-id="536d1-120">For more information, see [Transfer, Split, or Combine Fixed Assets](fa-how-trans-split-combine.md).</span></span>  

## <a name="to-view-disposal-ledger-entries"></a><span data-ttu-id="536d1-121">So zeigen Sie Verkaufsposten an</span><span class="sxs-lookup"><span data-stu-id="536d1-121">To view disposal ledger entries</span></span>
<span data-ttu-id="536d1-122">Wenn Sie eine Anlage verkaufen, wird der Verkaufswert in den Sachposten gebucht, wo Sie die Ergebnisse anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="536d1-122">When you sell or dispose of a fixed asset, the disposal value is posted to the general ledger where you can view the result.</span></span>  

1. <span data-ttu-id="536d1-123">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Anlagen** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="536d1-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="536d1-124">Wählen Sie die Anlage aus, für die Sie die Posten anzeigen möchten und wählen Sie dann die Aktion **AfA-Bücher** aus.</span><span class="sxs-lookup"><span data-stu-id="536d1-124">Select the fixed asset that you want to view entries for, and then choose the **Depreciation Books** action.</span></span>  
3. <span data-ttu-id="536d1-125">Wählen Sie das AfA-Buch aus, für das Sie die Posten anzeigen möchten und wählen Sie dann die Aktion **Posten** aus.</span><span class="sxs-lookup"><span data-stu-id="536d1-125">Select the depreciation book that you want to view entries for, and then choose the **Ledger Entries** action.</span></span>  
4. <span data-ttu-id="536d1-126">Wählen Sie im Feld **Anlagebuchungskategorie** die Zeile mit **Verkauf** aus, und klicken Sie auf die Aktion **Navigieren**.</span><span class="sxs-lookup"><span data-stu-id="536d1-126">Select a line with **Disposal** in the **FA Posting Category** field, and then choose the **Navigate** action.</span></span>  
5. <span data-ttu-id="536d1-127">Wählen Sie auf der Seite **Navigieren** die Sachpostenzeile aus, und klicken Sie auf die Aktion **Anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="536d1-127">On the **Navigate** page, select the general ledger entry line, and then choose the **Show** action.</span></span>  

<span data-ttu-id="536d1-128">Die Seite **Sachposten** wird geöffnet, in dem Sie die Posten sehen können, die aus der Verkaufsbuchung resultieren.</span><span class="sxs-lookup"><span data-stu-id="536d1-128">The **General Ledger Entries** page opens where you can see the entries that the disposal posting resulted in.</span></span>  

## <a name="see-also"></a><span data-ttu-id="536d1-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="536d1-129">See Also</span></span>
[<span data-ttu-id="536d1-130">Anlagen</span><span class="sxs-lookup"><span data-stu-id="536d1-130">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="536d1-131">Anlagen einrichten</span><span class="sxs-lookup"><span data-stu-id="536d1-131">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="536d1-132">Finanzen</span><span class="sxs-lookup"><span data-stu-id="536d1-132">Finance</span></span>](finance.md)  
[<span data-ttu-id="536d1-133">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="536d1-133">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="536d1-134">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="536d1-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
