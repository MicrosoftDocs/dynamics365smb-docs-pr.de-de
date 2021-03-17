---
title: Verwenden von Verteilungsschlüsseln in Fibu Buch.-Blättern | Microsoft Docs
description: Erfahren Sie, wie Sie Verteilungsschlüssel in Buch.-Blättern verwenden können.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost accounting
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 00d6fef612dd5fa1f3c38cef9fb97c08d10c752d
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388774"
---
# <a name="use-allocation-keys-in-general-journals"></a><span data-ttu-id="1320d-103">Verwenden von Verteilungsschlüsseln in Fibu Buch.-Blättern</span><span class="sxs-lookup"><span data-stu-id="1320d-103">Use Allocation Keys in General Journals</span></span>
<span data-ttu-id="1320d-104">Die Posten einer Fibu Buch.-Blattzeile lassen sich beim Buchen des Buch.-Blatts auf verschiedene Konten verteilen.</span><span class="sxs-lookup"><span data-stu-id="1320d-104">You can allocate an entry in a general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="1320d-105">Die Verteilung kann nach Anzahl, Prozent oder Betrag vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="1320d-105">The allocation can be made by quantity, percentage, or amount.</span></span>

## <a name="to-set-up-allocation-keys"></a><span data-ttu-id="1320d-106">Einrichten von Verteilungsschlüsseln</span><span class="sxs-lookup"><span data-stu-id="1320d-106">To set up allocation keys</span></span>
1. <span data-ttu-id="1320d-107">Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Wiederk. Fibu Buch.-Blatt** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="1320d-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="1320d-108">Wählen Sie auf der Seite **Fibu Buch.-Blattnamen** den **Buch.-Blattnamen**.</span><span class="sxs-lookup"><span data-stu-id="1320d-108">Choose the **Batch Name** field to open the **General Journal Batches** page.</span></span>
3. <span data-ttu-id="1320d-109">Sie können entweder Zuordnungen in einer vorhandene Charge in der Liste ändern oder eine neue Charge mit Zuordnungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="1320d-109">You can either modify allocations on an existing batch in the list or create a new batch with allocations.</span></span>
   * <span data-ttu-id="1320d-110">Um eine neue Chargennummer zu erstellen, wählen Sie die Aktion **Neu** und gehen Sie zum nächsten Schritt.</span><span class="sxs-lookup"><span data-stu-id="1320d-110">To create a new batch, choose the **New** action, and go to the next step.</span></span>
   * <span data-ttu-id="1320d-111">Um die Zuordnungen eines vorhandenen Buch.-Blattes zu ändern, wählen Sie das Buch.-Blatt und gehen Sie zum Schritt 7.</span><span class="sxs-lookup"><span data-stu-id="1320d-111">To change the allocations of an existing journal, select the journal and go to step 7.</span></span>    
4. <span data-ttu-id="1320d-112">Geben Sie im Feld **Name** einen Namen für das Buch.-Blatt ein, wie beispielsweise REINIGUNG.</span><span class="sxs-lookup"><span data-stu-id="1320d-112">In the **Name** field, enter a name for the batch, such as CLEANING.</span></span> <span data-ttu-id="1320d-113">Geben Sie im Feld **Beschreibung** eine Beschreibung ein, wie z. B. Reinigungsausgaben Buch.-Blatt.</span><span class="sxs-lookup"><span data-stu-id="1320d-113">In the **Description** field, enter a description, such as Cleaning Expenses Journal.</span></span>
5. <span data-ttu-id="1320d-114">Wenn Sie fertig sind, schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1320d-114">When you are done, close the page.</span></span> <span data-ttu-id="1320d-115">Ein neues, leeres wiederkehrendes Buchungsblatt wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="1320d-115">A new, empty recurring journal opens.</span></span>
6. <span data-ttu-id="1320d-116">Füllen Sie die Felder in der Zeile aus.</span><span class="sxs-lookup"><span data-stu-id="1320d-116">Fill in the fields on the line.</span></span>
7. <span data-ttu-id="1320d-117">Wählen Sie die Aktion **Verteilung** aus.</span><span class="sxs-lookup"><span data-stu-id="1320d-117">Choose the **Allocations** action.</span></span>
8. <span data-ttu-id="1320d-118">Erstellen Sie für jede Verteilung eine Zeile.</span><span class="sxs-lookup"><span data-stu-id="1320d-118">Add a line for each allocation.</span></span> <span data-ttu-id="1320d-119">Sie müssen entweder das Feld **Verteilung %**, **Anzahl Verteilungen** oder **Betrag** ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="1320d-119">You must fill in either the **Allocation %**, **Allocation Quantity**, or **Amount** field.</span></span> <span data-ttu-id="1320d-120">Sie müssen ebenfalls das Feld **Kontonr.** ausfüllen und, wenn Sie auf globale Dimensionen verteilen, auch die Felder "globale Dimensionen".</span><span class="sxs-lookup"><span data-stu-id="1320d-120">You must also fill in the **Account No.** field and, if you are allocating the transaction among global dimensions, the global dimension fields.</span></span>
9. <span data-ttu-id="1320d-121">Wenn Sie in einer Zeile einen Prozentsatz eingeben, wird der Betrag im Feld **Betrag** automatisch berechnet.</span><span class="sxs-lookup"><span data-stu-id="1320d-121">If you enter a percentage on a line, the amount in the **Amount** field is calculated automatically.</span></span> <span data-ttu-id="1320d-122">Diese Beträge haben das gegenteilige Vorzeichen wie der Gesamtbetrag im Feld **Betrag** des wiederkehrenden Buch.-Blattes.</span><span class="sxs-lookup"><span data-stu-id="1320d-122">These amounts have the opposite sign from the total amount in the **Amount** field in the recurring journal.</span></span>
10. <span data-ttu-id="1320d-123">Nachdem Sie die Zuteilungszeilen eingegeben haben, wählen Sie **OK** aus, um zur Seite **Wiederk. Fibu Buch.-Blätter** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="1320d-123">After entering the allocations lines, choose **OK** to return to the **Recurring General Journal** page.</span></span> <span data-ttu-id="1320d-124">Das Feld **Zugewiesener Betrag (USD)** ist ausgefüllt und entspricht dem Feld **Betrag**.</span><span class="sxs-lookup"><span data-stu-id="1320d-124">The **Allocated Amt. (USD)** field is filled in and matches the **Amount** field.</span></span>
11. <span data-ttu-id="1320d-125">Buchen Sie die Buch.-Blattzeile.</span><span class="sxs-lookup"><span data-stu-id="1320d-125">Post the journal.</span></span>

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a><span data-ttu-id="1320d-126">So ändern Sie einen bereits eingerichteten Zuordnungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="1320d-126">To change an allocation key that has already been set up</span></span>
1. <span data-ttu-id="1320d-127">Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Wiederk. Fibu Buch.-Blatt** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="1320d-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="1320d-128">Wählen Sie auf der Seite **Wiederk. Fibu Buch.-Blatt** das Buch.-Blatt mit der Verteilung aus.</span><span class="sxs-lookup"><span data-stu-id="1320d-128">On the **Recurring General Journal** page, select the journal with the allocation.</span></span>
3. <span data-ttu-id="1320d-129">Wählen Sie die Zeile mit der Verteilung, und wählen Sie dann die Aktion **Zuweisungen** aus.</span><span class="sxs-lookup"><span data-stu-id="1320d-129">Choose the line with the allocation, and then choose **Allocations** action.</span></span>
4. <span data-ttu-id="1320d-130">Ändern Sie die relevanten Felder und wählen Sie dann die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="1320d-130">Change the relevant fields, and then choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="1320d-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1320d-131">See Also</span></span>
[<span data-ttu-id="1320d-132">Arbeiten mit allgemeinen Buch.-Blättern</span><span class="sxs-lookup"><span data-stu-id="1320d-132">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="1320d-133">Dokumente und Buch.-Blatt verbuchen</span><span class="sxs-lookup"><span data-stu-id="1320d-133">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="1320d-134">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1320d-134">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]