---
title: "Vorgehensweise: Verwenden von Verteilungsschlüsseln in Fibu Buch.-Blättern | Microsoft Docs"
description: "Erfahren Sie, wie Sie Verteilungsschlüssel in Buch.-Blättern verwenden können."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost accounting
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: bbacf9b5634d51478dd4d54ac4b587ea9bfaaf99
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-use-allocation-keys-in-general-journals"></a><span data-ttu-id="fc7d9-103">Vorgehensweise: Verwenden von Verteilungsschlüsseln in Fibu Buch.-Blättern</span><span class="sxs-lookup"><span data-stu-id="fc7d9-103">How to: Use Allocation Keys in General Journals</span></span>
<span data-ttu-id="fc7d9-104">Die Posten einer Fibu Buch.-Blattzeile lassen sich beim Buchen des Buch.-Blatts auf verschiedene Konten verteilen.</span><span class="sxs-lookup"><span data-stu-id="fc7d9-104">You can allocate an entry in a general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="fc7d9-105">Die Verteilung kann nach Anzahl, Prozent oder Betrag vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="fc7d9-105">The allocation can be made by quantity, percentage, or amount.</span></span>

## <a name="to-set-up-allocation-keys"></a><span data-ttu-id="fc7d9-106">Einrichten von Verteilungsschlüsseln</span><span class="sxs-lookup"><span data-stu-id="fc7d9-106">To set up allocation keys</span></span>
1. <span data-ttu-id="fc7d9-107">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Wiederkehrendes Buch-Blatt** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="fc7d9-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="fc7d9-108">Wählen Sie im Fenster **Fibu Buch.-Blattnamen** den **Buch.-Blattnamen**.</span><span class="sxs-lookup"><span data-stu-id="fc7d9-108">Choose the **Batch Name** field to open the **General Journal Batches** window.</span></span>
3. <span data-ttu-id="fc7d9-109">Sie können entweder Zuordnungen in einer vorhandene Charge in der Liste ändern oder eine neue Charge mit Zuordnungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="fc7d9-109">You can either modify allocations on an existing batch in the list or create a new batch with allocations.</span></span>
   * <span data-ttu-id="fc7d9-110">Um eine neue Chargennummer zu erstellen, wählen Sie die Aktion **Neu** und gehen Sie zum nächsten Schritt.</span><span class="sxs-lookup"><span data-stu-id="fc7d9-110">To create a new batch, choose the **New** action, and go to the next step.</span></span>
   * <span data-ttu-id="fc7d9-111">Um die Zuordnungen eines vorhandenen Buch.-Blattes zu ändern, wählen Sie das Buch.-Blatt und gehen Sie zum Schritt 7.</span><span class="sxs-lookup"><span data-stu-id="fc7d9-111">To change the allocations of an existing journal, select the journal and go to step 7.</span></span>    
4. <span data-ttu-id="fc7d9-112">Geben Sie im Feld **Name** einen Namen für das Buch.-Blatt ein, wie beispielsweise REINIGUNG.</span><span class="sxs-lookup"><span data-stu-id="fc7d9-112">In the **Name** field, enter a name for the batch, such as CLEANING.</span></span> <span data-ttu-id="fc7d9-113">Geben Sie im Feld **Beschreibung** eine Beschreibung ein, wie z. B. Reinigungsausgaben Buch.-Blatt.</span><span class="sxs-lookup"><span data-stu-id="fc7d9-113">In the **Description** field, enter a description, such as Cleaning Expenses Journal.</span></span>
5. <span data-ttu-id="fc7d9-114">Wenn Sie fertig sind, schließen Sie das Fenster.</span><span class="sxs-lookup"><span data-stu-id="fc7d9-114">When you are done, close the window.</span></span> <span data-ttu-id="fc7d9-115">Ein neues, leeres wiederkehrendes Buchungsblatt wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="fc7d9-115">A new, empty recurring journal opens.</span></span>
6. <span data-ttu-id="fc7d9-116">Füllen Sie die Felder in der Zeile aus.</span><span class="sxs-lookup"><span data-stu-id="fc7d9-116">Fill in the fields on the line.</span></span>
7. <span data-ttu-id="fc7d9-117">Wählen Sie die Aktion **Verteilung** aus.</span><span class="sxs-lookup"><span data-stu-id="fc7d9-117">Choose the **Allocations** action.</span></span>
8. <span data-ttu-id="fc7d9-118">Erstellen Sie für jede Verteilung eine Zeile.</span><span class="sxs-lookup"><span data-stu-id="fc7d9-118">Add a line for each allocation.</span></span> <span data-ttu-id="fc7d9-119">Sie müssen entweder das Feld **Verteilung %**, **Anzahl Verteilungen** oder **Betrag** ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="fc7d9-119">You must fill in either the **Allocation %**, **Allocation Quantity**, or **Amount** field.</span></span> <span data-ttu-id="fc7d9-120">Sie müssen auch das Feld **Kontonr.**ausfüllen,</span><span class="sxs-lookup"><span data-stu-id="fc7d9-120">You must also fill in the **Account No.**</span></span> <span data-ttu-id="fc7d9-121">wenn Sie auf globale Dimensionen verteilen, auch die Felder "globale Dimensionen".</span><span class="sxs-lookup"><span data-stu-id="fc7d9-121">field and, if you are allocating the transaction among global dimensions, the global dimension fields.</span></span>
9. <span data-ttu-id="fc7d9-122">Wenn Sie in einer Zeile einen Prozentsatz eingeben, wird der Betrag im Feld **Betrag** automatisch berechnet.</span><span class="sxs-lookup"><span data-stu-id="fc7d9-122">If you enter a percentage on a line, the amount in the **Amount** field is calculated automatically.</span></span> <span data-ttu-id="fc7d9-123">Diese Beträge haben das gegenteilige Vorzeichen wie der Gesamtbetrag im Feld **Betrag** des wiederkehrenden Buch.-Blattes.</span><span class="sxs-lookup"><span data-stu-id="fc7d9-123">These amounts have the opposite sign from the total amount in the **Amount** field in the recurring journal.</span></span>
10. <span data-ttu-id="fc7d9-124">Nachdem Sie die Zuteilungszeilen eingegeben haben, wählen Sie **OK** aus, um zum Fenster **Wiederk. Fibu Buch.-Blätter** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="fc7d9-124">After entering the allocations lines, choose **OK** to return to the **Recurring General Journal** window.</span></span> <span data-ttu-id="fc7d9-125">Das Feld **Zugewiesener Betrag (USD)** ist ausgefüllt und entspricht dem Feld **Betrag**.</span><span class="sxs-lookup"><span data-stu-id="fc7d9-125">The **Allocated Amt. (USD)** field is filled in and matches the **Amount** field.</span></span>
11. <span data-ttu-id="fc7d9-126">Buchen Sie die Buch.-Blattzeile.</span><span class="sxs-lookup"><span data-stu-id="fc7d9-126">Post the journal.</span></span>

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a><span data-ttu-id="fc7d9-127">Ändern eines bereits eingerichteten Verteilungsschlüssels</span><span class="sxs-lookup"><span data-stu-id="fc7d9-127">To change an allocation key that has already been set up</span></span>
1. <span data-ttu-id="fc7d9-128">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Wiederkehrendes Buch-Blatt** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="fc7d9-128">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="fc7d9-129">Wählen Sie im Fenster **Wiederk. Fibu Buch.-Blatt** das Buch.-Blatt mit der Verteilung aus.</span><span class="sxs-lookup"><span data-stu-id="fc7d9-129">In the **Recurring General Journal** window, select the journal with the allocation.</span></span>
3. <span data-ttu-id="fc7d9-130">Wählen Sie die Zeile mit der Verteilung, und wählen Sie dann die Aktion **Zuweisungen** aus.</span><span class="sxs-lookup"><span data-stu-id="fc7d9-130">Choose the line with the allocation, and then choose **Allocations** action.</span></span>
4. <span data-ttu-id="fc7d9-131">Ändern Sie die relevanten Felder und wählen Sie dann die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="fc7d9-131">Change the relevant fields, and then choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="fc7d9-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc7d9-132">See Also</span></span>
[<span data-ttu-id="fc7d9-133">Arbeiten mit Fibu Buch.-Blättern</span><span class="sxs-lookup"><span data-stu-id="fc7d9-133">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="fc7d9-134">Journale und Dokumente buchen</span><span class="sxs-lookup"><span data-stu-id="fc7d9-134">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="fc7d9-135">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fc7d9-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

