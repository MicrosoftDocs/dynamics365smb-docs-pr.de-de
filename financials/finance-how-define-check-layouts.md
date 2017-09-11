---
title: Geben Sie das Layout eines Schecks an| Microsoft Docs
description: "Sie können Ihre Checks entwerfen und srucken in unterschiedliche Formaten, um Standardwerten zu entsprechen."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 06/15/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: a2db2860846cd9b8010222faf580f0c9889e39a4
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-define-check-layouts"></a><span data-ttu-id="fdc95-103">Gewusst wie: Definieren von Scheck-Layouts</span><span class="sxs-lookup"><span data-stu-id="fdc95-103">How to: Define Check Layouts</span></span>
<span data-ttu-id="fdc95-104">Sie können Ihre Schecks entwerfen, um sie den Vorgaben anzupassen, die von den lokalen Behörden festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="fdc95-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="fdc95-105">Scheckbilder können in Englisch, Französisch oder Spanisch gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="fdc95-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="fdc95-106">Schecks können sowohl im USA- als auch im Kanada-Schecklayout, entweder im Scheck/Formular/Scheck-Format oder im Formular/Formular/Scheck-Format gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="fdc95-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-define-check-layouts"></a><span data-ttu-id="fdc95-107">So definieren Sie Schecklayouts</span><span class="sxs-lookup"><span data-stu-id="fdc95-107">To define check layouts</span></span>
1. <span data-ttu-id="fdc95-108">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "") Nach Seite oder Bericht suchen und geben **Berichtsauswahl Bankkonto** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="fdc95-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="fdc95-109">Wählen Sie im Fenster **Berichtsauswahl - Bankkonto**</span><span class="sxs-lookup"><span data-stu-id="fdc95-109">In the **Report Selection - Bank Acc.**</span></span> <span data-ttu-id="fdc95-110">im Feld **Verwendung** **Scheck**aus.</span><span class="sxs-lookup"><span data-stu-id="fdc95-110">window, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="fdc95-111">Wählen Sie eine der folgenden Berichts-IDs:</span><span class="sxs-lookup"><span data-stu-id="fdc95-111">Select one of the following report IDs.</span></span>

| <span data-ttu-id="fdc95-112">Berichts-ID</span><span class="sxs-lookup"><span data-stu-id="fdc95-112">Report ID</span></span> | <span data-ttu-id="fdc95-113">Berichtsname</span><span class="sxs-lookup"><span data-stu-id="fdc95-113">Report Name</span></span> | <span data-ttu-id="fdc95-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fdc95-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="fdc95-115">1401</span><span class="sxs-lookup"><span data-stu-id="fdc95-115">1401</span></span> |<span data-ttu-id="fdc95-116">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="fdc95-116">Check</span></span> |<span data-ttu-id="fdc95-117">Dieser Bericht wird standardmäßig verwendet.</span><span class="sxs-lookup"><span data-stu-id="fdc95-117">This is the default report.</span></span> |
| <span data-ttu-id="fdc95-118">10401</span><span class="sxs-lookup"><span data-stu-id="fdc95-118">10401</span></span> |<span data-ttu-id="fdc95-119">Scheck (Formular/Formular/Scheck)</span><span class="sxs-lookup"><span data-stu-id="fdc95-119">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="fdc95-120">Dieser Bericht dient dazu, Schecks im Formular/Formular/Scheck-Format zu drucken.</span><span class="sxs-lookup"><span data-stu-id="fdc95-120">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="fdc95-121">10411</span><span class="sxs-lookup"><span data-stu-id="fdc95-121">10411</span></span> |<span data-ttu-id="fdc95-122">Scheck (Formular/Scheck/Formular)</span><span class="sxs-lookup"><span data-stu-id="fdc95-122">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="fdc95-123">Dieser Bericht dient dazu, Schecks im Scheck/Formular/Scheck-Format zu drucken.</span><span class="sxs-lookup"><span data-stu-id="fdc95-123">This report is designed to print checks in a check/stub/check format.</span></span> |

<span data-ttu-id="fdc95-124">Wenn Sie Schecklayouts eingerichtet haben, können Sie Schecks aus dem Fenster **Zahlung Buch.-Blatt** drucken.</span><span class="sxs-lookup"><span data-stu-id="fdc95-124">When you have set up check layouts, you can print checks from the **Payment Journal** window.</span></span> <span data-ttu-id="fdc95-125">Weitere Informationen finden Sie unter [Vorgehensweise: Arbeiten mit Schecks](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="fdc95-125">For more information, see [How to: Work with Checks](payables-how-work-checks.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="fdc95-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fdc95-126">See Also</span></span>
[<span data-ttu-id="fdc95-127">Verwalten von Verbindlichkeiten|</span><span class="sxs-lookup"><span data-stu-id="fdc95-127">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="fdc95-128">[Verwalten von Bankkonten](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="fdc95-128">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="fdc95-129">Abschließen von Periodenabschlüssen</span><span class="sxs-lookup"><span data-stu-id="fdc95-129">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="fdc95-130">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fdc95-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="fdc95-131">Allgemeine Geschäftsfunktionen</span><span class="sxs-lookup"><span data-stu-id="fdc95-131">General Business Functionality</span></span>](ui-across-business-areas.md)

