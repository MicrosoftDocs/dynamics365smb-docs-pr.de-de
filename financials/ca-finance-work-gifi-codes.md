---
title: GIFI-Codes in Kanada | Microsoft Docs
Description: "In Kanada können Sie den Gesamtindex der Codes der Finanzdaten (GIFI) einrichten und diese den Sachkonten zuweisen"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d5211f5c8265e572ff1d1a809b1046ce89f8c1e6
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-work-with-gifi-codes-in-canada"></a><span data-ttu-id="92c1c-103">So gehts: Arbeiten mit GIFI-Codes in Kanada</span><span class="sxs-lookup"><span data-stu-id="92c1c-103">How to: Work With GIFI Codes in Canada</span></span>
<span data-ttu-id="92c1c-104">Steuerinformationen können Sachkonten, Berichte, GuV, Bilanzen und Auszüge nicht ausgeschütteter Gewinne beinhalten.</span><span class="sxs-lookup"><span data-stu-id="92c1c-104">Fiscal information can include general ledger accounts, reports, income statements, balance sheets, and statements of retained earnings.</span></span> <span data-ttu-id="92c1c-105">Steuerinformationen werden mithilfe von Codes klassifiziert.</span><span class="sxs-lookup"><span data-stu-id="92c1c-105">Fiscal information is classified using codes.</span></span> <span data-ttu-id="92c1c-106">Die Verwendung von Codes hilft den Behörden, Daten zu bearbeiten, sie für die elektronische Speicherung vorzubereiten und Steuerdaten elektronisch zu überprüfen .</span><span class="sxs-lookup"><span data-stu-id="92c1c-106">The use of codes helps the government to process information, prepare for electronic filing, and validate tax information electronically.</span></span> <span data-ttu-id="92c1c-107">Außerdem hilft die Verwendung von Codes statistischen Organisationen, effizienter zu arbeiten, da Finanzdaten zeitnah zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="92c1c-107">The use of codes also helps statistical organizations to work more efficiently, as financial information is more readily available.</span></span> <span data-ttu-id="92c1c-108">Weitere Informationen finden Sie auf der [Webseite der Canada Revenue Agency](http://www.cra-arc.gc.ca/).</span><span class="sxs-lookup"><span data-stu-id="92c1c-108">For more information, see the [Canada Revenue Agency website](http://www.cra-arc.gc.ca/).</span></span>

<span data-ttu-id="92c1c-109">Die Canada Revenue Agency verwendet den General Index of Financial Information (GIFI), um Finanz- und Steuerdaten zu erfassen, zu überprüfen und elektronisch zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="92c1c-109">The Canada Revenue Agency uses General Index of Financial Information (GIFI) codes to collect, validate, and process financial and tax information electronically.</span></span> <span data-ttu-id="92c1c-110">Üblicher Weise werden GIFI-Codes nur für die Buchungskonten zugewiesen, sodass jede Zusammenzählung durch die Steuervorbereitungs-Software ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="92c1c-110">It is a best practice to assign GIFI codes only to posting accounts, so that all totaling is done by your tax preparation software.</span></span>

<span data-ttu-id="92c1c-111">Wenn ein Konto einem GIFI-Code zugeordnet ist, wird es der Einnahmenenagentur unter diesem Code gemeldet.</span><span class="sxs-lookup"><span data-stu-id="92c1c-111">When an account is associated with a GIFI code, it is reported to the revenue agency under that code.</span></span> <span data-ttu-id="92c1c-112">Mehrere Konten können alle denselben GIFI-Code haben, aber jedes Konto kann nur einen GIFI-Code haben.</span><span class="sxs-lookup"><span data-stu-id="92c1c-112">Multiple accounts can all have the same GIFI code, but each account can have only one GIFI code.</span></span>

<span data-ttu-id="92c1c-113">Sie können Saldoinformationen mit dem GIFI-Code exportieren und die exportierte Datei in Excel speichern. Dies ist nützlich, wenn Sie Informationen an Ihre Steuervorbereitungs-Software übertragen wollen.</span><span class="sxs-lookup"><span data-stu-id="92c1c-113">You can export balance information by GIFI code and save the exported file in Excel, which is useful for transferring information to your tax preparation software.</span></span>

## <a name="to-set-up-gifi-codes"></a><span data-ttu-id="92c1c-114">So richten Sie GIFI-Codes ein:</span><span class="sxs-lookup"><span data-stu-id="92c1c-114">To set up GIFI codes</span></span>
<span data-ttu-id="92c1c-115">In Dynamics NAV müssen Sie GIFI-Codes für Sachkonten, Berichte, Bilanzen, Einkommensblätter und Auszüge nicht ausgeschütteter Gewinne einrichten.</span><span class="sxs-lookup"><span data-stu-id="92c1c-115">In Dynamics NAV, you must set up GIFI codes for general ledger accounts, reports, balance sheets, income sheets, and statements of retained earnings.</span></span>

1. <span data-ttu-id="92c1c-116">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **GIFI Codes** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="92c1c-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **GIFI Codes**, and then choose the related link.</span></span>
2. <span data-ttu-id="92c1c-117">Wählen Sie im Fenster **GIFI Codes** die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="92c1c-117">In the **GIFI Codes** window, choose the **New** action.</span></span>
3. <span data-ttu-id="92c1c-118">Richten Sie GIFI-Codes ein, indem Sie die Felder ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="92c1c-118">Set up GIFI codes by filling the fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-associate-gifi-codes-with-gl-accounts"></a><span data-ttu-id="92c1c-119">So ordnen Sie GIFI-Codes Sachkonten zu</span><span class="sxs-lookup"><span data-stu-id="92c1c-119">To associate GIFI codes with G/L accounts</span></span>
<span data-ttu-id="92c1c-120">Um Finanzdaten mit GIFI-Code zu übermitteln, muss jeder GIFI-Code den entsprechenden Konten im Kontenplan zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="92c1c-120">To report financial information by GIFI code, each GIFI code must be associated with the appropriate accounts in the chart of accounts.</span></span>

1. <span data-ttu-id="92c1c-121">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben **Kontenplan** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="92c1c-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="92c1c-122">Wählen Sie ein entsprechendes Sachkonto, und wählen Sie dann die Aktion **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="92c1c-122">Select a relevant general ledger account, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="92c1c-123">Wählen Sie im Inforegister **Kostenrechnung** im Feld **GIFI Code** den entsprechenden GIFI-Code aus.</span><span class="sxs-lookup"><span data-stu-id="92c1c-123">On the **Cost Accounting** FastTab, in the **GIFI Code** field, select an appropriate GIFI code.</span></span>

## <a name="to-view-account-balances-using-the-gifi-code-report"></a><span data-ttu-id="92c1c-124">So verwenden Sie den GIFI-Code-Bericht, um Kontosalden anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="92c1c-124">To view account balances using the GIFI code report</span></span>
<span data-ttu-id="92c1c-125">Sie können Ihre Kontosalden mit dem GIFI-Code überprüfen, indem Sie den **Kontosalden durch GIFI-Code**-Bericht verwenden.</span><span class="sxs-lookup"><span data-stu-id="92c1c-125">You can review your account balances by GIFI code by using the **Account Balances by GIFI Code** report.</span></span>

1. <span data-ttu-id="92c1c-126">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Kontensalden nach GIFI Codes** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="92c1c-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Balances by GIFI Code**, and then choose the related link.</span></span>
2. <span data-ttu-id="92c1c-127">Legen Sie fest, was in den Bericht einbezogen werden soll, indem Sie die Felder ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="92c1c-127">Specify what to include in the report by filling the fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="92c1c-128">Wählen Sie die **Druck** oder **Vorschau** Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="92c1c-128">Choose the **Print** or the **Preview** button.</span></span>

## <a name="to-export-balance-information-using-gifi-codes"></a><span data-ttu-id="92c1c-129">So exportieren Sie Saldoinformationen mithilfe von GIFI-Codes</span><span class="sxs-lookup"><span data-stu-id="92c1c-129">To export balance information using GIFI codes</span></span>
<span data-ttu-id="92c1c-130">Sie können Saldoinformationen mithilfe von GIFI-Codes exportieren und die exportierte Datei in Excel speichern.</span><span class="sxs-lookup"><span data-stu-id="92c1c-130">You can export balance information using GIFI codes and save the exported file in Excel.</span></span> <span data-ttu-id="92c1c-131">Sie können die Datei ändern, speichern oder löschen.</span><span class="sxs-lookup"><span data-stu-id="92c1c-131">You can modify, save, or delete the file.</span></span> <span data-ttu-id="92c1c-132">Sie können die Datei verwenden, um Informationen an Ihre Steuervorbereitungs-Software zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="92c1c-132">You can use the file to transfer information to your tax preparation software.</span></span>

1. <span data-ttu-id="92c1c-133">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **GIFI Codes in Excel kopieren** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="92c1c-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Export GIFI Info. to Excel**, and then choose the related link.</span></span>
2. <span data-ttu-id="92c1c-134">Geben Sie an, was Sie in Excel exportieren wollen, indem Sie die Felder ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="92c1c-134">Specify what to export to Excel by filling the fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="92c1c-135">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="92c1c-135">Choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="92c1c-136">Die Excel-Datei hat folgende Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="92c1c-136">The Excel file has the following characteristics:</span></span>

* <span data-ttu-id="92c1c-137">Der Saldo wird auf den nächsten Prozentsatz gerundet, aber der Zellenwert behält den gleichen Prozentsatz bei, den er auch in der Finanzbuchhaltung hat.</span><span class="sxs-lookup"><span data-stu-id="92c1c-137">The balance is rounded to the nearest percentage, but the cell value maintains the same percentage as it does in the general ledger.</span></span>
* <span data-ttu-id="92c1c-138">Negative Zahlen werden als positive Zahl in Klammern dargestellt.</span><span class="sxs-lookup"><span data-stu-id="92c1c-138">Negative numbers are represented as positive number in brackets.</span></span> <span data-ttu-id="92c1c-139">Dementsprechend wird -123 als (123) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="92c1c-139">Accordingly, -123 is represented as (123).</span></span>

## <a name="see-also"></a><span data-ttu-id="92c1c-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92c1c-140">See Also</span></span>
<span data-ttu-id="92c1c-141">[Finanzen](finance.md) </span><span class="sxs-lookup"><span data-stu-id="92c1c-141">[Finance](finance.md) </span></span>  
[<span data-ttu-id="92c1c-142">Finance einrichten</span><span class="sxs-lookup"><span data-stu-id="92c1c-142">Setting Up Finance</span></span>](finance-setup-finance.md)

