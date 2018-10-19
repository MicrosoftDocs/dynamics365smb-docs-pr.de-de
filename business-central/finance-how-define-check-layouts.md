---
title: Geben Sie das Layout eines Schecks an| Microsoft Docs
description: "Sie können Ihre Checks entwerfen und srucken in unterschiedliche Formaten, um Standardwerten zu entsprechen."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: d8546cd2f713416e50474848e783d61b4b1dc810
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="define-check-layouts"></a><span data-ttu-id="b1c6d-103">So definieren Sie Schecklayouts</span><span class="sxs-lookup"><span data-stu-id="b1c6d-103">Define Check Layouts</span></span>
<span data-ttu-id="b1c6d-104">Sie können Ihre Schecks entwerfen, um sie den Vorgaben anzupassen, die von den lokalen Behörden festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b1c6d-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="b1c6d-105">Scheckbilder können in Englisch, Französisch oder Spanisch gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="b1c6d-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="b1c6d-106">Schecks können sowohl im USA- als auch im Kanada-Schecklayout, entweder im Scheck/Formular/Scheck-Format oder im Formular/Formular/Scheck-Format gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="b1c6d-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-define-check-layouts"></a><span data-ttu-id="b1c6d-107">So definieren Sie Schecklayouts</span><span class="sxs-lookup"><span data-stu-id="b1c6d-107">To define check layouts</span></span>
1. <span data-ttu-id="b1c6d-108">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Berichtsauswahl Bankkonto** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="b1c6d-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="b1c6d-109">Im Fenster **Berichts-Auswahl - Bankkonto** unter **Verwendung** wählen Sie **Scheck**.</span><span class="sxs-lookup"><span data-stu-id="b1c6d-109">In the **Report Selection - Bank Acc.** window, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="b1c6d-110">Wählen Sie eine der folgenden Berichts-IDs:</span><span class="sxs-lookup"><span data-stu-id="b1c6d-110">Select one of the following report IDs.</span></span>

| <span data-ttu-id="b1c6d-111">Berichts-ID</span><span class="sxs-lookup"><span data-stu-id="b1c6d-111">Report ID</span></span> | <span data-ttu-id="b1c6d-112">Berichtsname</span><span class="sxs-lookup"><span data-stu-id="b1c6d-112">Report Name</span></span> | <span data-ttu-id="b1c6d-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1c6d-113">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="b1c6d-114">1401</span><span class="sxs-lookup"><span data-stu-id="b1c6d-114">1401</span></span> |<span data-ttu-id="b1c6d-115">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="b1c6d-115">Check</span></span> |<span data-ttu-id="b1c6d-116">Dieser Bericht wird standardmäßig verwendet.</span><span class="sxs-lookup"><span data-stu-id="b1c6d-116">This is the default report.</span></span> |
| <span data-ttu-id="b1c6d-117">10401</span><span class="sxs-lookup"><span data-stu-id="b1c6d-117">10401</span></span> |<span data-ttu-id="b1c6d-118">Scheck (Formular/Formular/Scheck)</span><span class="sxs-lookup"><span data-stu-id="b1c6d-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="b1c6d-119">Dieser Bericht dient dazu, Schecks im Formular/Formular/Scheck-Format zu drucken.</span><span class="sxs-lookup"><span data-stu-id="b1c6d-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="b1c6d-120">10411</span><span class="sxs-lookup"><span data-stu-id="b1c6d-120">10411</span></span> |<span data-ttu-id="b1c6d-121">Scheck (Formular/Scheck/Formular)</span><span class="sxs-lookup"><span data-stu-id="b1c6d-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="b1c6d-122">Dieser Bericht dient dazu, Schecks im Scheck/Formular/Scheck-Format zu drucken.</span><span class="sxs-lookup"><span data-stu-id="b1c6d-122">This report is designed to print checks in a check/stub/check format.</span></span> |

<span data-ttu-id="b1c6d-123">Wenn Sie Schecklayouts eingerichtet haben, können Sie Schecks aus dem Fenster **Zahlung Buch.-Blatt** drucken.</span><span class="sxs-lookup"><span data-stu-id="b1c6d-123">When you have set up check layouts, you can print checks from the **Payment Journal** window.</span></span> <span data-ttu-id="b1c6d-124">Weitere Informationen finden Sie unter [Arbeiten mit Schecks](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="b1c6d-124">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b1c6d-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1c6d-125">See Also</span></span>
[<span data-ttu-id="b1c6d-126">Verwalten von Verbindlichkeiten</span><span class="sxs-lookup"><span data-stu-id="b1c6d-126">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="b1c6d-127">[Verwalten von Bankkonten](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="b1c6d-127">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="b1c6d-128">Abschließen von Periodenabschlüssen</span><span class="sxs-lookup"><span data-stu-id="b1c6d-128">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="b1c6d-129">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b1c6d-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="b1c6d-130">Allgemeine Geschäftsfunktionen</span><span class="sxs-lookup"><span data-stu-id="b1c6d-130">General Business Functionality</span></span>](ui-across-business-areas.md)

