---
title: Geben Sie das Layout eines Schecks an| Microsoft Docs
description: Sie können Ihre Checks entwerfen und srucken in unterschiedliche Formaten, um Standardwerten zu entsprechen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 04/24/2019
ms.author: edupont
ms.openlocfilehash: f2b7fa01cff36e3aab335f7d5921954343c69b74
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243595"
---
# <a name="define-check-layouts"></a><span data-ttu-id="6cc07-103">So definieren Sie Schecklayouts</span><span class="sxs-lookup"><span data-stu-id="6cc07-103">Define Check Layouts</span></span>
<span data-ttu-id="6cc07-104">Sie können Ihre Schecks entwerfen, um sie den Vorgaben anzupassen, die von den lokalen Behörden festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6cc07-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="6cc07-105">Scheckbilder können in Englisch, Französisch oder Spanisch gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="6cc07-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="6cc07-106">Schecks können sowohl im USA- als auch im Kanada-Schecklayout, entweder im Scheck/Formular/Scheck-Format oder im Formular/Formular/Scheck-Format gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="6cc07-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-define-check-layouts"></a><span data-ttu-id="6cc07-107">So definieren Sie Schecklayouts</span><span class="sxs-lookup"><span data-stu-id="6cc07-107">To define check layouts</span></span>
1. <span data-ttu-id="6cc07-108">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Berichtsauswahl Bankkonto** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="6cc07-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="6cc07-109">Auf der Seite **Berichts-Auswahl - Bankkonto** unter **Verwendung** wählen Sie **Scheck**.</span><span class="sxs-lookup"><span data-stu-id="6cc07-109">On the **Report Selection - Bank Acc.** page, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="6cc07-110">Wählen Sie eine der folgenden Berichts-IDs:</span><span class="sxs-lookup"><span data-stu-id="6cc07-110">Select one of the following report IDs.</span></span>

  | <span data-ttu-id="6cc07-111">Berichts-ID</span><span class="sxs-lookup"><span data-stu-id="6cc07-111">Report ID</span></span> | <span data-ttu-id="6cc07-112">Berichtsname</span><span class="sxs-lookup"><span data-stu-id="6cc07-112">Report Name</span></span> | <span data-ttu-id="6cc07-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6cc07-113">Description</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="6cc07-114">1401</span><span class="sxs-lookup"><span data-stu-id="6cc07-114">1401</span></span> |<span data-ttu-id="6cc07-115">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="6cc07-115">Check</span></span> |<span data-ttu-id="6cc07-116">Dieser Bericht wird standardmäßig verwendet.</span><span class="sxs-lookup"><span data-stu-id="6cc07-116">This is the default report.</span></span> |
  | <span data-ttu-id="6cc07-117">10411</span><span class="sxs-lookup"><span data-stu-id="6cc07-117">10411</span></span> |<span data-ttu-id="6cc07-118">Scheck (Formular/Formular/Scheck)</span><span class="sxs-lookup"><span data-stu-id="6cc07-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="6cc07-119">Dieser Bericht dient dazu, Schecks im Formular/Formular/Scheck-Format zu drucken.</span><span class="sxs-lookup"><span data-stu-id="6cc07-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
  | <span data-ttu-id="6cc07-120">10412</span><span class="sxs-lookup"><span data-stu-id="6cc07-120">10412</span></span> |<span data-ttu-id="6cc07-121">Scheck (Formular/Scheck/Formular)</span><span class="sxs-lookup"><span data-stu-id="6cc07-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="6cc07-122">Dieser Bericht dient dazu, Schecks im Formular/Scheck/Formular-Format zu drucken.</span><span class="sxs-lookup"><span data-stu-id="6cc07-122">This report is designed to print checks in a stub/check/stub format.</span></span> |
  | <span data-ttu-id="6cc07-123">10413</span><span class="sxs-lookup"><span data-stu-id="6cc07-123">10413</span></span> |<span data-ttu-id="6cc07-124">Drei Schecks pro Seite</span><span class="sxs-lookup"><span data-stu-id="6cc07-124">Three Checks per Page</span></span> |<span data-ttu-id="6cc07-125">Dieser Bericht ist dafür ausgelegt, drei Schecks auf jeder Seite zu drucken.</span><span class="sxs-lookup"><span data-stu-id="6cc07-125">This report is designed to print three checks on each page.</span></span> |

<span data-ttu-id="6cc07-126">Wenn Sie Schecklayouts eingerichtet haben, können Sie Schecks auf de Seite **Zahlung Buch.-Blatt** drucken.</span><span class="sxs-lookup"><span data-stu-id="6cc07-126">When you have set up check layouts, you can print checks from the **Payment Journal** page.</span></span> <span data-ttu-id="6cc07-127">Weitere Informationen finden Sie unter [Arbeiten mit Schecks](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="6cc07-127">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="6cc07-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6cc07-128">See Also</span></span>
[<span data-ttu-id="6cc07-129">Verwalten von Verbindlichkeiten</span><span class="sxs-lookup"><span data-stu-id="6cc07-129">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="6cc07-130">[Verwalten von Bankkonten](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="6cc07-130">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="6cc07-131">Abschließen von Periodenabschlüssen</span><span class="sxs-lookup"><span data-stu-id="6cc07-131">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="6cc07-132">[Arbeiten mit [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6cc07-132">[Working with [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="6cc07-133">Allgemeine Geschäftsfunktionen</span><span class="sxs-lookup"><span data-stu-id="6cc07-133">General Business Functionality</span></span>](ui-across-business-areas.md)
