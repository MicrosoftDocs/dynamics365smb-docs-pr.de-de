---
title: Codes für Audit-Trails einrichten | Microsoft Docs
description: Erfahren Sie mehr über die Aufgaben zum Einrichten von Herkunftscodes und Ursachencodes ein, mit denen Sie Audit-Trails verfolgen können.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 05/12/2020
ms.author: edupont
ms.openlocfilehash: eac9b5268cda8671a7189a429dedd9eb3cbfbc53
ms.sourcegitcommit: b9264b4ed650feca18776892ec23f2aa7ec43e20
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2020
ms.locfileid: "3372687"
---
# <a name="setting-up-source-codes-and-reason-codes-for-audit-trails"></a><span data-ttu-id="b23d0-103">Herkunftscodes und Ursachencodes für Audit Trails einrichten</span><span class="sxs-lookup"><span data-stu-id="b23d0-103">Setting Up Source Codes and Reason Codes for Audit Trails</span></span>

<span data-ttu-id="b23d0-104">Allen gebuchten Posten werden automatisch einem Herkunftscode zugewiesen, sodass Transaktionen bis zu ihrem Ursprung nachverfolgt werden können.</span><span class="sxs-lookup"><span data-stu-id="b23d0-104">All posted entries are automatically assigned a source code so that transactions can be traced to their origin.</span></span> <span data-ttu-id="b23d0-105">Wenn Sie Posten einen zusätzlichen Herkunftscode zuordnen möchten, können Sie Ursachencodes verwenden.</span><span class="sxs-lookup"><span data-stu-id="b23d0-105">If you want to give entries a supplementary source code, you can use reason codes.</span></span> <span data-ttu-id="b23d0-106">Ursachencodes werden verwendet, um den Grund für eine Buchung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b23d0-106">Reason codes are used to indicate why an entry was created.</span></span> <span data-ttu-id="b23d0-107">Ursachencodes können gesamten Buch.-Blattvorlagen und Buch.-Blattnamen oder auch einzelnen Buch.-Blattzeilen und Belegen zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b23d0-107">When you set up reason codes, you can assign them to entire journal templates and journal batches, and you can assign them to individual journal lines and documents.</span></span>  

<span data-ttu-id="b23d0-108">Verwenden Sie als Herkunfstcodes und Ursachencodes aussagekräftige Codes, an die Sie sich leicht erinnern können.</span><span class="sxs-lookup"><span data-stu-id="b23d0-108">For both source codes and reason codes, use codes that are easy to remember and descriptive.</span></span> <span data-ttu-id="b23d0-109">Der Code muss eindeutig sein, und Sie können beliebig viele Codes einrichten.</span><span class="sxs-lookup"><span data-stu-id="b23d0-109">The code must be unique, and you can set up as many codes as you like.</span></span>

## <a name="define-source-codes"></a><span data-ttu-id="b23d0-110">Herkunftscodes definieren</span><span class="sxs-lookup"><span data-stu-id="b23d0-110">Define source codes</span></span>

<span data-ttu-id="b23d0-111">Gelegentlich möchten Sie nachvollziehen, wie ein bestimmter Posten entstanden ist, ob er z. B. beim Buchen eines Buch.-Blattes oder einer Einkaufsrechnung erzeugt wurde.</span><span class="sxs-lookup"><span data-stu-id="b23d0-111">Sometimes, you want see how a particular entry arose, such as whether it came from posting a general journal or a purchase invoice.</span></span> <span data-ttu-id="b23d0-112">Ein Herkunftscode gibt an, wo ein Posten erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b23d0-112">A source code indicates where an entry was created.</span></span> <span data-ttu-id="b23d0-113">Posten werden erstellt, wenn Buch.-Blätter und Rechnungen gebucht und bestimmte Stapelverarbeitungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b23d0-113">Entries are created when journals and invoices are posted and when certain batch jobs are executed.</span></span> <span data-ttu-id="b23d0-114">Jede Buchungsart hat einen bestimmten Herkunftscode, der zugewiesen wird, wenn Posten erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b23d0-114">Each posting type has a specific source code that is assigned when individual entries are created.</span></span>  

<span data-ttu-id="b23d0-115">Beim Buchen von Buch.-Blättern, Aufträgen, Rechnungen oder Gutschriften sowie beim Ausführen bestimmter Stapelverarbeitungen werden Posten in der Finanzaufstellungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="b23d0-115">Posting journals, orders, invoices, or credit memos, and running various batch jobs, creates entries in the financial statements.</span></span> <span data-ttu-id="b23d0-116">Die Seite **Herkunftscode Einrichtung** enthält für jeden Anwendungsbereich mehrere Inforegister.</span><span class="sxs-lookup"><span data-stu-id="b23d0-116">The **Source Code Setup** page contains several FastTabs, one for each application area.</span></span> <span data-ttu-id="b23d0-117">Jedes Inforegister enthält die Herkunftscodes, die für diesen Anwendungsbereich anwendbar sind.</span><span class="sxs-lookup"><span data-stu-id="b23d0-117">Each FastTab contains the source codes that are applicable for that application area.</span></span>

<span data-ttu-id="b23d0-118">Beim Buchen oder Ausführen einer Stapelverarbeitung wird dem Posten automatisch der richtige Herkunftscode zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b23d0-118">When you post or run a batch job, the correct source code is automatically attached to the entry.</span></span> <span data-ttu-id="b23d0-119">Wenn Sie z. B. von einem Fibu Buch.-Blatt aus buchen, erhält der Posten den Code *FIBUBUCHBL*.</span><span class="sxs-lookup"><span data-stu-id="b23d0-119">For example, when you post from the general journal, the entry is coded as *GENJNL*.</span></span> <span data-ttu-id="b23d0-120">Sie können dann die Seite **Sachposten** filtern, um anzuzeigen, welche Einträge beispielsweise aus dem Fibu Buch.-Blatt oder aus Verkaufsbelegen gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="b23d0-120">You can then filter the **General Ledger Entries** page to show which entries were posted from the general journal or from sales documents, for example</span></span>

### <a name="to-define-source-codes"></a><span data-ttu-id="b23d0-121">So definieren Sie Herkunftscodes</span><span class="sxs-lookup"><span data-stu-id="b23d0-121">To define source codes</span></span>

1. <span data-ttu-id="b23d0-122">Wählen Sie das Symbol ![Seite suchen oder Bericht](media/ui-search/search_small.png "Nach dem Symbol für „Seite“ oder „Bericht“ suchen"), geben Sie **Herkunftscode Einrichtung** ein und wählen Sie dann den entsprechenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="b23d0-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Source Code Setup**, and then choose the related link.</span></span>  

2. <span data-ttu-id="b23d0-123">Geben Sie im Fenster **Herkunftscode Einrichtung** für jede Buchungsart und jede Stapelverarbeitung den entsprechenden Herkunftscode ein.</span><span class="sxs-lookup"><span data-stu-id="b23d0-123">In the **Source Code Setup** window, for each each posting type and batch job, specify the relevant source code.</span></span>  

<span data-ttu-id="b23d0-124">Sie können den Inhalt eines Felds später ändern. Diese Änderung wirkt sich dann auf zukünftige Buchungen aus.</span><span class="sxs-lookup"><span data-stu-id="b23d0-124">You can change the contents of a field later, and that change will then impact future postings.</span></span>

## <a name="change-source-codes"></a><span data-ttu-id="b23d0-125">Herkunftscodes ändern</span><span class="sxs-lookup"><span data-stu-id="b23d0-125">Change source codes</span></span>

<span data-ttu-id="b23d0-126">Sie können einen Herkunftscode ändern.</span><span class="sxs-lookup"><span data-stu-id="b23d0-126">You may want to change a source code.</span></span> <span data-ttu-id="b23d0-127">Sie können den Herkunftscode *FIBUBUCHBL* beispielsweise in *FIBUBL* ändern.</span><span class="sxs-lookup"><span data-stu-id="b23d0-127">For example, you want to change the source code *GENJNL* to *GNJ*.</span></span>

### <a name="to-change-source-codes"></a><span data-ttu-id="b23d0-128">So ändern Sie Herkunftscodes</span><span class="sxs-lookup"><span data-stu-id="b23d0-128">To change source codes</span></span>

1. <span data-ttu-id="b23d0-129">Wählen Sie das Symbol ![Seite oder Bericht suchen](media/ui-search/search_small.png "Nach dem Symbol für „Seite“ oder „Bericht“ suchen") aus, geben Sie **Herkunftscode Einrichtung** ein, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="b23d0-129">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Source Codes**, and then choose the related link.</span></span>

2. <span data-ttu-id="b23d0-130">Wählen Sie in der Zeile mit dem zu ändernden den Code im Feld **Code** aus.</span><span class="sxs-lookup"><span data-stu-id="b23d0-130">On the line with the code to be changed, select the code in the **Code** field.</span></span>

3. <span data-ttu-id="b23d0-131">Geben Sie den neuen Code ein, und klicken Sie dann auf die Schaltfläche **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b23d0-131">Enter the new code, and then choose the **Yes** button.</span></span> <span data-ttu-id="b23d0-132">Sie können auch den Inhalt des Feldes **Beschreibung** ändern.</span><span class="sxs-lookup"><span data-stu-id="b23d0-132">You can also change the contents of the **Description** field.</span></span>

<span data-ttu-id="b23d0-133">Alle neuen Posten, die über das Fibu Buch.-Blatt gebucht werden, weisen den neuen Herkunftscode auf.</span><span class="sxs-lookup"><span data-stu-id="b23d0-133">All new entries that are posted from the general journal will have the new source code.</span></span>

## <a name="define-reason-codes"></a><span data-ttu-id="b23d0-134">Ursachencodes definieren</span><span class="sxs-lookup"><span data-stu-id="b23d0-134">Define reason codes</span></span>

<span data-ttu-id="b23d0-135">Ursachencodes ergänzen die Quellcodes und geben an, warum ein Eintrag erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b23d0-135">Reason codes supplement the source codes and are used to indicate why an entry was created.</span></span> <span data-ttu-id="b23d0-136">Sie können Ursachencodes für einzelne Posten und permanente Codes bestimmten Buch.-Blattvorlagen und Buch.-Blattnamen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="b23d0-136">You can assign reason codes on individual entries, and you can assign permanent codes to specific journal templates and journal batches.</span></span> <span data-ttu-id="b23d0-137">Wenn ein Ursachencodes mit einer Buch.-Blattzeile bzw. einem Einkaufs- oder Verkaufskopf verknüpft ist, werden beim Buchen alle Posten mit dem entsprechenden Ursachencode markiert.</span><span class="sxs-lookup"><span data-stu-id="b23d0-137">When a reason code is linked to a journal line or a sales or purchase header, all entries are marked with the reason code when they are posted.</span></span>  

### <a name="to-set-up-reason-codes"></a><span data-ttu-id="b23d0-138">So richten Sie Ursachencodes ein</span><span class="sxs-lookup"><span data-stu-id="b23d0-138">To set up reason codes</span></span>

1. <span data-ttu-id="b23d0-139">Wählen Sie das Symbol ![Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol „Suche nach Seite oder Bericht“") aus, geben Sie **Ursachencodes** ein, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="b23d0-139">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon")  icon, enter **Reason Codes**, and then choose the related link.</span></span>

2. <span data-ttu-id="b23d0-140">Geben Sie im Fenster **Ursachencodes** den ersten Code im Feld **Code** ein.</span><span class="sxs-lookup"><span data-stu-id="b23d0-140">In the **Reason Codes** window, enter the first code in the **Code** field.</span></span> <span data-ttu-id="b23d0-141">Geben Sie im Feld **Beschreibung** einen erklärenden Text ein.</span><span class="sxs-lookup"><span data-stu-id="b23d0-141">In the **Description** field, enter an explanatory text.</span></span>

<span data-ttu-id="b23d0-142">Wiederholen Sie den Ablauf für jeden Code, den Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="b23d0-142">Repeat the procedure for each code you want to use.</span></span> <span data-ttu-id="b23d0-143">Sie können eine beliebige Anzahl von Codes einrichten.</span><span class="sxs-lookup"><span data-stu-id="b23d0-143">You can set up any number of codes.</span></span>

<span data-ttu-id="b23d0-144">Nachfolgend wird beschrieben, wie Sie einer Buch.-Blattvorlage einen Ursachencodes hinzufügen. Ähnliche Schritte gelten jedoch für das Hinzufügen eines Ursachencodes zu einer Buch.-Blattzeile oder einer Stapelverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="b23d0-144">The following procedure describes how to add a reason code to a journal template, but similar steps apply to adding a reason code to a journal line or journal batch.</span></span>  

### <a name="to-assign-reason-codes-to-journal-templates"></a><span data-ttu-id="b23d0-145">So weisen Sie Buch.-Blattvorlagen Ursachencodes zu</span><span class="sxs-lookup"><span data-stu-id="b23d0-145">To assign reason codes to journal templates</span></span>

1. <span data-ttu-id="b23d0-146">Wählen Sie das Symbol ![Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol „Suche nach Seite oder Bericht“") aus, geben Sie **Allgemeine Buch.-Blatt Vorlage** ein, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="b23d0-146">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon")  icon, enter **General Journal Templates**, and then choose the related link.</span></span>

2. <span data-ttu-id="b23d0-147">Geben Sie in der Zeile mit der ausgewählten Buch.-Blattvorlage den entsprechenden Code in das Feld **Ursachencode** ein.</span><span class="sxs-lookup"><span data-stu-id="b23d0-147">On the line with the selected journal template, in the **Reason Code** field, specify the relevant code.</span></span>

3. <span data-ttu-id="b23d0-148">Schließen Sie die Buch.-Blattvorlage.</span><span class="sxs-lookup"><span data-stu-id="b23d0-148">Close the journal template.</span></span>

<span data-ttu-id="b23d0-149">Der ausgewählte Ursachencode wird in neue Buch.-Blätter eingefügt, die unter dieser Buch.-Blattvorlage erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b23d0-149">The selected reason code will be copied to new journal batches created under this journal template.</span></span> <span data-ttu-id="b23d0-150">In anderen Anwendungsbereichen weisen Sie auf dieselbe Art und Weise Buch.-Blattvorlagen Ursachencodes zu.</span><span class="sxs-lookup"><span data-stu-id="b23d0-150">You assign reason codes to journal templates in the other application areas in the same way.</span></span>

### <a name="to-use-reason-codes-on-sales-and-purchase-documents"></a><span data-ttu-id="b23d0-151">So verwenden Sie Ursachencodes in Verkaufs- und Einkaufsbelegen</span><span class="sxs-lookup"><span data-stu-id="b23d0-151">To use reason codes on sales and purchase documents</span></span>

1. <span data-ttu-id="b23d0-152">Öffnen Sie den gewünschten Verkaufs- oder Einkaufsbeleg.</span><span class="sxs-lookup"><span data-stu-id="b23d0-152">Open the relevant sales or purchase document.</span></span>

2. <span data-ttu-id="b23d0-153">Geben Sie im Einkaufskopf im Feld **Ursachencode** den Code ein.</span><span class="sxs-lookup"><span data-stu-id="b23d0-153">On the sales or purchase header, enter the code in the **Reason Code** field.</span></span>

<span data-ttu-id="b23d0-154">Wenn die Rechnung gebucht wird, wird der Ursachencode in jeden Sach-, Debitor- und Kreditorposten kopiert.</span><span class="sxs-lookup"><span data-stu-id="b23d0-154">When the invoice is posted, the reason code is copied to each general ledger, customer, and vendor entry.</span></span> <span data-ttu-id="b23d0-155">Sie können einzelnen Einkaufs- oder Verkaufszeilen nicht unterschiedliche Ursachencodes zuordnen, da alle Zeilen als ein Posten gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="b23d0-155">You cannot assign different reason codes to the individual purchase and sales lines because all lines are posted as one entry.</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="b23d0-156">Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="b23d0-156">See Related Training at [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="b23d0-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b23d0-157">See Also</span></span>

[<span data-ttu-id="b23d0-158">Finanzen</span><span class="sxs-lookup"><span data-stu-id="b23d0-158">Finance</span></span>](finance.md)  
[<span data-ttu-id="b23d0-159">Abstimmen von Bankkonten</span><span class="sxs-lookup"><span data-stu-id="b23d0-159">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="b23d0-160">Arbeiten mit Dimensionen</span><span class="sxs-lookup"><span data-stu-id="b23d0-160">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="b23d0-161">Importieren von Geschäftsdaten aus anderen Finanzsystemen</span><span class="sxs-lookup"><span data-stu-id="b23d0-161">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="b23d0-162">Analysieren von Cashflow in Ihren Mandanten</span><span class="sxs-lookup"><span data-stu-id="b23d0-162">Analyzing Cash Flow in Your Company</span></span>](finance-analyze-cash-flow.md)  
<span data-ttu-id="b23d0-163">[Arbeiten mit [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b23d0-163">[Working with [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
