---
title: Ausgabe, Drucken, Stornieren und Annullieren von Schecks| Microsoft Docs
description: "Beschreibt, wie Schecks mithilfe des Zahlungsausgangs Buch.-Blattes, ausgegeben, gedruckt oder annulliert werden oder wie Check-Sachposteneinträge in Finance and Operations, Business edition angezeigt werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b3f8bece0d0d1de9a6fd17b84df73d466ccdf403
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-checks"></a><span data-ttu-id="3a38e-103">Arbeiten mit Checks</span><span class="sxs-lookup"><span data-stu-id="3a38e-103">Work With Checks</span></span>
<span data-ttu-id="3a38e-104">Sie können elektronischerund und manuelle Schecks ausgeben in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="3a38e-104">You can issue electronic and manual checks in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="3a38e-105">Bei beiden Verfahren erfolgt die Ausstellung von Schecks an Kreditoren über das Zahlungsausgangs-Buch.-Blatt.</span><span class="sxs-lookup"><span data-stu-id="3a38e-105">Both methods use the payment journal to issue checks to vendors.</span></span> <span data-ttu-id="3a38e-106">Sie können auch Schecks annullieren und Scheckposten anzeigen.</span><span class="sxs-lookup"><span data-stu-id="3a38e-106">You can also void checks and view check ledger entries.</span></span>

<span data-ttu-id="3a38e-107">Bei dem Verfahren zum Ausstellen von Schecks werden Zahlungsvorschläge gemacht, Scheckposten erstellt und die Computerschecks gedruckt.</span><span class="sxs-lookup"><span data-stu-id="3a38e-107">The process of issuing checks suggests payments, creates ledger entries, and prints the computer checks.</span></span>

> [!NOTE]  
>   <span data-ttu-id="3a38e-108">Um sicherzustellen, dass Ihre Bank nur Schecks und Beträge freigibt, können Sie ihr eine Datei senden, die die Daten für Kreditoren, Schecks und Zahlungsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="3a38e-108">To make sure that your bank only clears validated checks and amounts, you can send them a file that contains vendor, check, and payment information.</span></span> <span data-ttu-id="3a38e-109">Weitere Informationen finden Sie unter [Datei Positive Pay exportieren](finance-how-positive-pay.md).</span><span class="sxs-lookup"><span data-stu-id="3a38e-109">For more information, see [Export a Positive Pay file](finance-how-positive-pay.md).</span></span>

<span data-ttu-id="3a38e-110">Der Drucker muss für den Ausdruck von Scheckformularen eingerichtet werden, und Sie müssen festlegen welches Layout verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3a38e-110">Your printer must be correctly set up with the check forms, and you must define which check layout to use.</span></span> <span data-ttu-id="3a38e-111">Weitere Informationen zum Definieren von Attributen finden Sie unter [Definieren von Scheck-Layouts](finance-how-define-check-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="3a38e-111">For more information, see [Define Check Layouts](finance-how-define-check-layouts.md)</span></span>

## <a name="to-issue-checks"></a><span data-ttu-id="3a38e-112">Um Schecks auszustellen</span><span class="sxs-lookup"><span data-stu-id="3a38e-112">To issue checks</span></span>
1. <span data-ttu-id="3a38e-113">Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Zahlungs-Buchblatt** ein und wählen den zugehörenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="3a38e-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="3a38e-114">Füllen Sie das Buch.-Blatt mit den entsprechenden Zahlungen aus, z. B. indem Sie die Zahlungsvorschläge verwenden.</span><span class="sxs-lookup"><span data-stu-id="3a38e-114">Fill in the journal with relevant payments, for example by using the Suggest Vendor Payments function.</span></span> <span data-ttu-id="3a38e-115">Weitere Informationen finden Sie unter [Erstellen von Zahlungsvorschlägen für Kreditoren](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="3a38e-115">For more information, see [Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span>
3. <span data-ttu-id="3a38e-116">Im Feld **Bankkontozahlungsart** der Buch.-Blattzeilen zur Zahlung, die Sie mit Schecks vornehmen möchten, wählen Sie eine der folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="3a38e-116">In the **Bank Payment Type** field on journal lines for payment that you want to make with checks, select one of the following options:</span></span>

   * <span data-ttu-id="3a38e-117">**Computer Scheck**: Wählen Sie diese Option, wenn Sie einen Scheck über den in der Buch.-Blattzeile angezeigten Betrag drucken wollen.</span><span class="sxs-lookup"><span data-stu-id="3a38e-117">**Computer Check**: Select this option if you want to print a check for the amount on the payment journal line.</span></span> <span data-ttu-id="3a38e-118">Sie müssen die Schecks drucken, bevor Sie die Buch.-Blattzeilen buchen können.</span><span class="sxs-lookup"><span data-stu-id="3a38e-118">You must print the checks before you can post the journal lines.</span></span> <span data-ttu-id="3a38e-119">Sie können **Computer Scheck** nur auswählen, wenn **Gegenkontoart** oder **Kontoart** den Wert **Bankkonto** hat.</span><span class="sxs-lookup"><span data-stu-id="3a38e-119">You can only select **Computer Check** if the **Bal. Account Type** or the **Account Type** is **Bank Account**.</span></span>
   * <span data-ttu-id="3a38e-120">**Manueller Scheck**: Wählen Sie diese Option, wenn Sie einen Scheck manuell ausstellen und einen entsprechenden Scheckposten über diesen Betrag anlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="3a38e-120">**Manual Check**: Select this option if you have created a check manually and want to create a corresponding check ledger entry for this amount.</span></span> <span data-ttu-id="3a38e-121">Mit dieser Option ist das automatische Drucken von Schecks in [!INCLUDE[d365fin](includes/d365fin_md.md)]nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="3a38e-121">By using this option, you cannot print checks from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="3a38e-122">Sie können **Manueller Scheck** nur auswählen, wenn **Gegenkontoart** oder **Kontoart** den Wert **Bankkonto** hat.</span><span class="sxs-lookup"><span data-stu-id="3a38e-122">You can only select **Manual Check** if the **Bal. Account Type** or the **Account Type** is **Bank Account**.</span></span>

     > [!NOTE]  
>   <span data-ttu-id="3a38e-123">Sie müssen die Computer Schecks drucken, bevor Sie die entsprechenden Buch.-Blattzeilen buchen können.</span><span class="sxs-lookup"><span data-stu-id="3a38e-123">You must print computer checks before you post the related journal lines.</span></span>
4. <span data-ttu-id="3a38e-124">Im Falle von Computer Schecks wählen Sie **Scheck drucken** aus.</span><span class="sxs-lookup"><span data-stu-id="3a38e-124">In case of computer checks, choose **Print Check**.</span></span>
5. <span data-ttu-id="3a38e-125">Füllen Sie im Fenster **Check** die Felder wie benötigt aus.</span><span class="sxs-lookup"><span data-stu-id="3a38e-125">In the **Check** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. <span data-ttu-id="3a38e-126">Wählen Sie die Schaltfläche **Drucken** aus.</span><span class="sxs-lookup"><span data-stu-id="3a38e-126">Choose the **Print** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="3a38e-127">Wenn Sie Schecks in mehreren Währungen von mehreren Bankkonten aus ausdrucken möchten, muss der Batchauftrag **Scheck drucken** für jede einzelne Währung ausgeführt und das entsprechende Bankkonto angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3a38e-127">If you want to print checks in more than one currency from different bank accounts, you must run the **Print Check** batch job separately for each currency and specify the appropriate bank account.</span></span>

## <a name="to-cancel-printed-checks-that-are-not-posted"></a><span data-ttu-id="3a38e-128">Um gedruckte Scheck die nicht gebucht wurden zu stornieren</span><span class="sxs-lookup"><span data-stu-id="3a38e-128">To cancel printed checks that are not posted</span></span>
<span data-ttu-id="3a38e-129">Sie können nicht gebuchte Schecks stornieren, nachdem sie gedruckt wurden, indem Sie die Aktion **Scheck annullieren** im Fenster **Zahlungsausgangs Buch.-Blatt** verwenden.</span><span class="sxs-lookup"><span data-stu-id="3a38e-129">You can cancel non-posted checks after they have been printed by using the **Void Check** action in the **Payment Journal** window.</span></span>

1. <span data-ttu-id="3a38e-130">Wählen Sie im Fenster **Zahlungsausgangs Buch.-Blatt** **Scheck annullieren** aus, und wählen Sie aus, welche Prüfungen durchgeführt zum stornieren mit den Schecks durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3a38e-130">In the **Payment Journal** window, choose the **Void Check**, and then choose which checks to cancel.</span></span>

## <a name="to-void-checks"></a><span data-ttu-id="3a38e-131">Annullieren von Schecks</span><span class="sxs-lookup"><span data-stu-id="3a38e-131">To void checks</span></span>
<span data-ttu-id="3a38e-132">Wenn Scheckzahlung gebucht wurden, können Sie Schecks aus den resultierenden Bankposten nur stornieren (annulieren).</span><span class="sxs-lookup"><span data-stu-id="3a38e-132">When check payment have been posted, you can only cancel (void) checks from the resulting bank ledger entries.</span></span>

1. <span data-ttu-id="3a38e-133">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Bankkonten** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="3a38e-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="3a38e-134">Wählen Sie das entsprechende Bankkonto aus, wählen Sie die **Bearbeiten**-Aktion aus, und wählen Sie dann die **Scheckposten**-Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="3a38e-134">Select the relevant bank account, choose the **Edit** action, and then choose the **Check Ledger Entries** action.</span></span>
3. <span data-ttu-id="3a38e-135">Im **Scheckposten**-Fenster wählen Sie die **Scheck annullieren**-Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="3a38e-135">In the **Check Ledger Entries** window, choose the **Void Check** action.</span></span>
4. <span data-ttu-id="3a38e-136">Wählen das Kontrollkästchen **Scheck nur annullieren**.</span><span class="sxs-lookup"><span data-stu-id="3a38e-136">Select the **Void Check Only** check box.</span></span>
5. <span data-ttu-id="3a38e-137">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="3a38e-137">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="3a38e-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a38e-138">See Also</span></span>
[<span data-ttu-id="3a38e-139">Verwalten von Verbindlichkeiten</span><span class="sxs-lookup"><span data-stu-id="3a38e-139">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="3a38e-140">Einrichten von Banken</span><span class="sxs-lookup"><span data-stu-id="3a38e-140">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="3a38e-141">Um eine Positive Pay-Datei zu exportieren</span><span class="sxs-lookup"><span data-stu-id="3a38e-141">Export a Positive Pay file</span></span>](finance-how-positive-pay.md)  
<span data-ttu-id="3a38e-142">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3a38e-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

