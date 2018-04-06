---
title: Anlagen einrichten | Microsoft Docs
description: "Kennenlernen der die Abfolge von Aufgaben, die Sie ausführen müssen, um Anlagen einzurichten, wie Arbeitsplätze oder Gebäude."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: machinery, buildings
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 6ca21ece631fdd07cb95ffdaaa350506b4a8c9e1
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-fixed-assets"></a><span data-ttu-id="7070c-103">Anlagen einrichten</span><span class="sxs-lookup"><span data-stu-id="7070c-103">Setting Up Fixed Assets</span></span>
<span data-ttu-id="7070c-104">Um mit Anlagen arbeiten können, müssen Sie einige Elemente festlegen:</span><span class="sxs-lookup"><span data-stu-id="7070c-104">Before you can work with Fixed Assets, you need to define a few things:</span></span>  

* <span data-ttu-id="7070c-105">Wie Sie Anlagen versichern, verwalten und abschreiben.</span><span class="sxs-lookup"><span data-stu-id="7070c-105">How you insure, maintain, and depreciate fixed assets.</span></span>  
* <span data-ttu-id="7070c-106">Wie Sie Kosten und andere Werte in der Finanzbuchhaltung erfassen.</span><span class="sxs-lookup"><span data-stu-id="7070c-106">How you record costs and other values in the general ledger.</span></span>  

<span data-ttu-id="7070c-107">Die folgende Tabelle enthält Verknüpfungen für weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="7070c-107">The table below has links to more information.</span></span> <span data-ttu-id="7070c-108">Nachdem Sie diese Dinge festgelegt haben, können Sie die verschiedene Aktivitäten beginnen.</span><span class="sxs-lookup"><span data-stu-id="7070c-108">After you set those things up, you can start various activities.</span></span> <span data-ttu-id="7070c-109">Weitere Informationen finden Siue unter [Anlagen](fa-manage.md).</span><span class="sxs-lookup"><span data-stu-id="7070c-109">For more information, see [Fixed Assets](fa-manage.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="7070c-110">Sie können Anlagentransaktionen im Fenster **Anlagen Fibu Buch.-Blatt** oder im Fenster **Anlagen Buch-Blatt** erfassen, abhängig davon, ob die Transaktionen für Finanzberichte oder zur internen Verwaltung bestimmt sind.</span><span class="sxs-lookup"><span data-stu-id="7070c-110">You can record fixed asset transactions in the **Fixed Asset G/L Journal** or **Fixed Asset Journal** windows, depending on whether the transactions are for financial reporting or for internal management.</span></span> <span data-ttu-id="7070c-111">Die Hilfe zu den Anlagen beschreibt lediglich, wie das Fenster **Anlagen Fibu Buch.-Blatt** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7070c-111">Help for Fixed Assets only describes how to use the **Fixed Asset G/L Journal** window.</span></span>  

<span data-ttu-id="7070c-112">Wenn Sie das Kontrollkästchen für eine Anlagenaktivität im Abschnitt **Fibu-Integration** im Fenster **AfA-Buch-Karte** aktiveren, wird das **Anlagen Fibu Buch.-Blatt** Fenster verwendet, um Transaktionen für die fragliche Aktivität zu buchen.</span><span class="sxs-lookup"><span data-stu-id="7070c-112">When you enable a fixed asset activity in the **G/L Integration** section in the **Depreciation Book Card** window, the **Fixed Asset G/L Journal** window is used to post transactions for the activity.</span></span>

<span data-ttu-id="7070c-113">In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.</span><span class="sxs-lookup"><span data-stu-id="7070c-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

| <span data-ttu-id="7070c-114">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="7070c-114">To</span></span> | <span data-ttu-id="7070c-115">Siehe</span><span class="sxs-lookup"><span data-stu-id="7070c-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="7070c-116">Richten Sie Standardsachkonten, Verteilungsschlüssel, Buch.-Blattvorlagen und - namen für Anlagebuchungen ein und erstellen feste Anlageklassen und Unterklassen, wie beispielsweise materielle und immaterielle.</span><span class="sxs-lookup"><span data-stu-id="7070c-116">Set up default G/L accounts, allocation keys, journal templates and batches for fixed asset posting, and set up fixed asset classes and subclasses, such as Tangible and Intangible.</span></span> |[<span data-ttu-id="7070c-117">Allgemeine Anlagen-Informationen einrichten</span><span class="sxs-lookup"><span data-stu-id="7070c-117">Set Up General Fixed Assets Information</span></span>](fa-how-setup-general.md) |
| <span data-ttu-id="7070c-118">Erstellen Sie AfA-Bücher, definieren verschiedene AfA-Methoden, integrieren in die Finanzbuchhaltung und aktiveren das Kopieren der Posten in mehrere AfA-Bücher.</span><span class="sxs-lookup"><span data-stu-id="7070c-118">Create depreciation books, define various depreciation methods, integrate with the general ledger, and enable duplication of entries in several depreciation books.</span></span> |[<span data-ttu-id="7070c-119">Richten Sie eine neue Anlagenkarte ein.</span><span class="sxs-lookup"><span data-stu-id="7070c-119">Set Up Fixed Asset Depreciation</span></span>](fa-how-setup-depreciation.md) |
| <span data-ttu-id="7070c-120">Aktivieren Sie Versicherungen von Anlagen, richten allgemeine Versicherungsinformationen und eine Versicherungskarte pro Versicherung ein und bereiten Buch.-Blätter vor, um Versicherungskosten zu buchen.</span><span class="sxs-lookup"><span data-stu-id="7070c-120">Enable insurance of fixed assets, set up general insurance information, an insurance card per policy, and prepare journals to post insurance costs.</span></span> |[<span data-ttu-id="7070c-121">Um Anlagenversicherung einzurichten:</span><span class="sxs-lookup"><span data-stu-id="7070c-121">Set Up Fixed Asset Insurance</span></span>](fa-how-setup-insurance.md) |
| <span data-ttu-id="7070c-122">Aktivieren Sie die Wartung von Anlagen, richten allgemeine Wartungsinformationen und Wartungs-Buchungskonten ein, und definieren Sie Arten von Wartungsarbeiten.</span><span class="sxs-lookup"><span data-stu-id="7070c-122">Enable maintenance of fixed assets, set up general maintenance information, set up maintenance posting accounts, and define types of maintenance work.</span></span> |[<span data-ttu-id="7070c-123">Um Anlagenwartung einzurichten:</span><span class="sxs-lookup"><span data-stu-id="7070c-123">Set Up Fixed Asset Maintenance</span></span>](fa-how-setup-maintenance.md) |
| <span data-ttu-id="7070c-124">Informieren Sie sich über verschiedene Anlagen-AfA-Methoden.</span><span class="sxs-lookup"><span data-stu-id="7070c-124">Learn about different fixed asset depreciation methods.</span></span> |[<span data-ttu-id="7070c-125">Abschreibungsmethoden</span><span class="sxs-lookup"><span data-stu-id="7070c-125">Depreciation Methods</span></span>](fa-depreciation-methods.md) |

## <a name="see-also"></a><span data-ttu-id="7070c-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7070c-126">See Also</span></span>
[<span data-ttu-id="7070c-127">Anlagen</span><span class="sxs-lookup"><span data-stu-id="7070c-127">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="7070c-128">Finanzen</span><span class="sxs-lookup"><span data-stu-id="7070c-128">Finance</span></span>](finance.md)  
<span data-ttu-id="7070c-129">[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="7070c-129">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="7070c-130">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7070c-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

