---
title: Export von Positive Pay-Dateien| Microsoft Docs
description: Um sicherzustellen, dass Ihre Bank nur überprüfte Schecks und Beträge freigibt, können Sie ihr eine Positive Pay Datei senden, die die Daten für Kreditoren, Schecks und Zahlungsinformationen enthält.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, clearing
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 73d871e43490fba817db8f9dfad5fbdaf456c3c8
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306268"
---
# <a name="export-a-positive-pay-file"></a><span data-ttu-id="26166-103">Eine Positive Pay-Datei exportieren</span><span class="sxs-lookup"><span data-stu-id="26166-103">Export a Positive Pay File</span></span>
<span data-ttu-id="26166-104">Um sicherzustellen, dass eine Bank nur validierte Schecks und Beträge freigibt, können Sie eine Positive Pay-Datei exportieren, die die relevanten Zahlungsinformationen enthält wie Schecknummer und Zahlungsbetrag, die Sie als Referenz an die Bank senden, wenn Sie Zahlungen verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="26166-104">To make sure that your bank only clears validated checks and amounts, you can export a Positive Pay file that contains vendor information, check number, and payment amount, which you send to the bank for reference when you process payments.</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="26166-105">wird vorkonfiguriert, um Positive Pay-Dateien an die Bank of America und City Bank zu senden.</span><span class="sxs-lookup"><span data-stu-id="26166-105">is preconfigured to support Positive Pay files for Bank of America and City Bank.</span></span>

## <a name="to-set-up-a-bank-account-for-positive-pay"></a><span data-ttu-id="26166-106">Um ein Bankkkonto für Positive Pay einzurichten</span><span class="sxs-lookup"><span data-stu-id="26166-106">To set up a bank account for Positive Pay</span></span>
1. <span data-ttu-id="26166-107">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Bankkonten** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="26166-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="26166-108">Öffnen Sie die Karte des Bankkontos, für das Sie Positive Pay nutzen möchten.</span><span class="sxs-lookup"><span data-stu-id="26166-108">Open the card for the bank that you want to use Positive Pay for.</span></span>
3. <span data-ttu-id="26166-109">In dem Feld **Positive Pay-Exportcode** geben Sie POSPAYBANK ein.</span><span class="sxs-lookup"><span data-stu-id="26166-109">In the **Positive Pay Export Code** field, enter POSPAYBANK.</span></span>
4. <span data-ttu-id="26166-110">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="26166-110">Close the page.</span></span>

## <a name="to-export-a-positive-pay-file"></a><span data-ttu-id="26166-111">Um eine Positive Pay-Datei zu exportieren</span><span class="sxs-lookup"><span data-stu-id="26166-111">To export a Positive Pay file</span></span>
1. <span data-ttu-id="26166-112">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Bankkonten** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="26166-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="26166-113">Wählen Sie das Bankkonto aus, für das Sie eine Positive Pay-Datei exportieren möchten.</span><span class="sxs-lookup"><span data-stu-id="26166-113">Select the bank account that you want to export a Positive Pay file for.</span></span>
3. <span data-ttu-id="26166-114">Wählen Sie die Aktion **Positive Pay-Export** aus.</span><span class="sxs-lookup"><span data-stu-id="26166-114">Choose **Positive Pay Export** action.</span></span>

    <span data-ttu-id="26166-115">Die Seite **Positive Pay-Export** wird geöffnet und zeigt Zahlungen an, die über das Bankkonto seit dem letzten Uploaddatum, wie in den Felder **Letztes Upload-Datum** **Letzte Upload-Zeit** angezeigt, geleistet wurden.</span><span class="sxs-lookup"><span data-stu-id="26166-115">The **Positive Pay Export** page opens displaying payments that have been made for the bank account since the last upload date, as shown in the **Last Upload Date** and **Last Upload Time** fields.</span></span>
4. <span data-ttu-id="26166-116">Im Feld **Upload-Datum trennen** definieren Sie ein Datum, vor dem Zahlungen nicht in der exportierten Datei enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="26166-116">In the **Cutoff Upload Date** field, specify a date before which payments are not included in the exported file.</span></span>
5. <span data-ttu-id="26166-117">Wählen Sie die Aktion **Exportieren** aus.</span><span class="sxs-lookup"><span data-stu-id="26166-117">Choose the **Export** action.</span></span>
6. <span data-ttu-id="26166-118">Klicken Sie auf der Seite **Datei exportieren** auf die Schaltfläche **Speichern** und speichern Sie die Datei am gewünschten Speicherort.</span><span class="sxs-lookup"><span data-stu-id="26166-118">On the **Export File** page, choose the **Save** button, and then save the file to a convenient location.</span></span>
7. <span data-ttu-id="26166-119">Laden Sie die Datei in Ihre elektronische Bankseite hoch.</span><span class="sxs-lookup"><span data-stu-id="26166-119">Upload the file to your electronic bank site.</span></span>
8. <span data-ttu-id="26166-120">Schreiben oder kopieren Sie die Bestätigungsnummer, die angezeigt wird, wenn Sie die Datei erfolgreich hochgeladen haben.</span><span class="sxs-lookup"><span data-stu-id="26166-120">Write down or copy the confirmation number that is displayed when the file upload is successful.</span></span>

<span data-ttu-id="26166-121">Um exportierte Positive Pay-Datensätze anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="26166-121">To view exported Positive Pay records</span></span>

1. <span data-ttu-id="26166-122">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Bankkonten** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="26166-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="26166-123">Wählen Sie das Bankkonto aus, für das Sie einen Positive Pay-Datei-Export anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="26166-123">Select the bank account that you want to view Positive Pay export records for.</span></span>
3. <span data-ttu-id="26166-124">Wählen Sie die Aktion **Positive Pay-Einträge** aus.</span><span class="sxs-lookup"><span data-stu-id="26166-124">Choose the **Positive Pay Entries** action.</span></span>

    <span data-ttu-id="26166-125">Auf der Seite **Positive Pay-Posten** können Sie alle Positive Pay-Exportdatensätze für das Bankkonto anzeigen.</span><span class="sxs-lookup"><span data-stu-id="26166-125">On the **Positive Pay Entries** page, you can see all the Positive Pay export records for the bank account.</span></span>
4. <span data-ttu-id="26166-126">Geben Sie im Feld **Bestätigungsnummer** für jeden Exportdatensatz die Bestätigungsnummer ein, die Sie gerade erhalten, wann der Dateiupload zur Bank ordnungsgemäß durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="26166-126">In the **Confirmation Number** field, enter, for each export record, the confirmation number that you receive when the file upload to the bank is successful.</span></span>
5. <span data-ttu-id="26166-127">Um die entsprechenden Zahlungszeilen anzuzeigen, wählen Sie die **Positive Pay-Postendetails** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="26166-127">To view the related payment lines, choose the **Positive Pay Entry Details** action.</span></span>

<span data-ttu-id="26166-128">Um Positive Pay-Dateien erneut zu exportieren</span><span class="sxs-lookup"><span data-stu-id="26166-128">To reexport Positive Pay files</span></span>

1. <span data-ttu-id="26166-129">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Bankkonten** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="26166-129">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="26166-130">Wählen Sie das Bankkonto aus, für die Sie Positive Pay-Dateien erneut exportieren möchten.</span><span class="sxs-lookup"><span data-stu-id="26166-130">Select the bank account that you want to reexport Positive Pay files for.</span></span>
3. <span data-ttu-id="26166-131">Wählen Sie die Aktion **Positive Pay-Einträge** aus.</span><span class="sxs-lookup"><span data-stu-id="26166-131">Choose the **Positive Pay Entries** action.</span></span>
4. <span data-ttu-id="26166-132">Wählen Sie die Zeile für die Positive Pay Exportdatei aus, die Sie erneut exportieren möchten.</span><span class="sxs-lookup"><span data-stu-id="26166-132">Select the line for the Positive Pay export file that you want to reexport.</span></span>
5. <span data-ttu-id="26166-133">Auf der Seite **Positive Pay-Posten** wählen Sie die Aktion **Erneuter Positive Pay-Export in Datei** aus.</span><span class="sxs-lookup"><span data-stu-id="26166-133">On the **Positive Pay Entries** page, choose the **Reexport Positive Pay to File** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="26166-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26166-134">See Also</span></span>
[<span data-ttu-id="26166-135">Finanzen</span><span class="sxs-lookup"><span data-stu-id="26166-135">Finance</span></span>](finance.md)  
[<span data-ttu-id="26166-136">Finanzen einrichten</span><span class="sxs-lookup"><span data-stu-id="26166-136">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="26166-137">Arbeiten mit Fibu Buch.-Blättern</span><span class="sxs-lookup"><span data-stu-id="26166-137">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="26166-138">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="26166-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
