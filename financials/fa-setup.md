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
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 9dea8be0f5b0200f97082dc25dbaa2483ad6c735
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-fixed-assets"></a><span data-ttu-id="b7a86-103">Anlagen einrichten</span><span class="sxs-lookup"><span data-stu-id="b7a86-103">Setting Up Fixed Assets</span></span>
<span data-ttu-id="b7a86-104">Um mit Anlagen arbeiten können, müssen Sie einige Elemente festlegen:</span><span class="sxs-lookup"><span data-stu-id="b7a86-104">Before you can work with Fixed Assets, you need to define a few things:</span></span>  

* <span data-ttu-id="b7a86-105">Wie Sie Anlagen versichern, verwalten und abschreiben.</span><span class="sxs-lookup"><span data-stu-id="b7a86-105">How you insure, maintain, and depreciate fixed assets.</span></span>  
* <span data-ttu-id="b7a86-106">Wie Sie Kosten und andere Werte in der Finanzbuchhaltung erfassen.</span><span class="sxs-lookup"><span data-stu-id="b7a86-106">How you record costs and other values in the general ledger.</span></span>  

<span data-ttu-id="b7a86-107">Die folgende Tabelle enthält Verknüpfungen für weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="b7a86-107">The table below has links to more information.</span></span> <span data-ttu-id="b7a86-108">Nachdem Sie diese Dinge festgelegt haben, können Sie die verschiedene Aktivitäten beginnen.</span><span class="sxs-lookup"><span data-stu-id="b7a86-108">After you set those things up, you can start various activities.</span></span> <span data-ttu-id="b7a86-109">Weitere Informationen finden Siue unter [Anlagen](fa-manage.md).</span><span class="sxs-lookup"><span data-stu-id="b7a86-109">For more information, see [Fixed Assets](fa-manage.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="b7a86-110">Sie können Anlagentransaktionen im Fenster **Anlagen Fibu Buch.-Blatt** oder im Fenster **Anlagen Buch-Blatt** erfassen, abhängig davon, ob die Transaktionen für Finanzberichte oder zur internen Verwaltung bestimmt sind.</span><span class="sxs-lookup"><span data-stu-id="b7a86-110">You can record fixed asset transactions in the **Fixed Asset G/L Journal** or **Fixed Asset Journal** windows, depending on whether the transactions are for financial reporting or for internal management.</span></span> <span data-ttu-id="b7a86-111">Die Hilfe zu den Anlagen beschreibt lediglich, wie das Fenster **Anlagen Fibu Buch.-Blatt** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b7a86-111">Help for Fixed Assets only describes how to use the **Fixed Asset G/L Journal** window.</span></span>  

<span data-ttu-id="b7a86-112">Wenn Sie das Kontrollkästchen für eine Anlagenaktivität im Abschnitt **Fibu-Integration** im Fenster **AfA-Buch-Karte** aktiveren, wird das **Anlagen Fibu Buch.-Blatt** Fenster verwendet, um Transaktionen für die fragliche Aktivität zu buchen.</span><span class="sxs-lookup"><span data-stu-id="b7a86-112">When you enable a fixed asset activity in the **G/L Integration** section in the **Depreciation Book Card** window, the **Fixed Asset G/L Journal** window is used to post transactions for the activity.</span></span>

> [!NOTE]  
>  <span data-ttu-id="b7a86-113">Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="b7a86-113">This functionality requires that the experience is set to **Suite**.</span></span> <span data-ttu-id="b7a86-114">Weitere Informationen finden Sie unter [Anpassen Ihrer Financials Experience](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="b7a86-114">For more information, see [Customizing Your Financials Experience](ui-experiences.md).</span></span>  

<span data-ttu-id="b7a86-115">Die folgende Tabelle enthält eine Abfolge von Aufgaben sowie Links zu den entsprechenden Themen, in denen diese Aufgaben erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="b7a86-115">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

| <span data-ttu-id="b7a86-116">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="b7a86-116">To</span></span> | <span data-ttu-id="b7a86-117">Siehe</span><span class="sxs-lookup"><span data-stu-id="b7a86-117">See</span></span> |
| --- | --- |
| <span data-ttu-id="b7a86-118">Richten Sie Standardsachkonten, Verteilungsschlüssel, Buch.-Blattvorlagen und - namen für Anlagebuchungen ein und erstellen feste Anlageklassen und Unterklassen, wie beispielsweise materielle und immaterielle.</span><span class="sxs-lookup"><span data-stu-id="b7a86-118">Set up default G/L accounts, allocation keys, journal templates and batches for fixed asset posting, and set up fixed asset classes and subclasses, such as Tangible and Intangible.</span></span> |[<span data-ttu-id="b7a86-119">So geht's: Allgemeine Anlagen-Informationen einrichten</span><span class="sxs-lookup"><span data-stu-id="b7a86-119">How to: Set Up General Fixed Assets Information</span></span>](fa-how-setup-general.md) |
| <span data-ttu-id="b7a86-120">Erstellen Sie AfA-Bücher, definieren verschiedene AfA-Methoden, integrieren in die Finanzbuchhaltung und aktiveren das Kopieren der Posten in mehrere AfA-Bücher.</span><span class="sxs-lookup"><span data-stu-id="b7a86-120">Create depreciation books, define various depreciation methods, integrate with the general ledger, and enable duplication of entries in several depreciation books.</span></span> |[<span data-ttu-id="b7a86-121">So geht's: Einrichten der Anlagen-AfA</span><span class="sxs-lookup"><span data-stu-id="b7a86-121">How to: Set Up Fixed Asset Depreciation</span></span>](fa-how-setup-depreciation.md) |
| <span data-ttu-id="b7a86-122">Aktivieren Sie Versicherungen von Anlagen, richten allgemeine Versicherungsinformationen und eine Versicherungskarte pro Versicherung ein und bereiten Buch.-Blätter vor, um Versicherungskosten zu buchen.</span><span class="sxs-lookup"><span data-stu-id="b7a86-122">Enable insurance of fixed assets, set up general insurance information, an insurance card per policy, and prepare journals to post insurance costs.</span></span> |[<span data-ttu-id="b7a86-123">So geht's: Einrichten der Anlagenversicherung</span><span class="sxs-lookup"><span data-stu-id="b7a86-123">How to: Set Up Fixed Asset Insurance</span></span>](fa-how-setup-insurance.md) |
| <span data-ttu-id="b7a86-124">Aktivieren Sie die Wartung von Anlagen, richten allgemeine Wartungsinformationen und Wartungs-Buchungskonten ein, und definieren Sie Arten von Wartungsarbeiten.</span><span class="sxs-lookup"><span data-stu-id="b7a86-124">Enable maintenance of fixed assets, set up general maintenance information, set up maintenance posting accounts, and define types of maintenance work.</span></span> |[<span data-ttu-id="b7a86-125">So geht's: Einrichten der Anlagenwartung</span><span class="sxs-lookup"><span data-stu-id="b7a86-125">How to: Set Up Fixed Asset Maintenance</span></span>](fa-how-setup-maintenance.md) |
| <span data-ttu-id="b7a86-126">Informieren Sie sich über verschiedene Anlagen-AfA-Methoden.</span><span class="sxs-lookup"><span data-stu-id="b7a86-126">Learn about different fixed asset depreciation methods.</span></span> |[<span data-ttu-id="b7a86-127">Abschreibungsmethoden</span><span class="sxs-lookup"><span data-stu-id="b7a86-127">Depreciation Methods</span></span>](fa-depreciation-methods.md) |

## <a name="see-also"></a><span data-ttu-id="b7a86-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7a86-128">See Also</span></span>
[<span data-ttu-id="b7a86-129">Anlagen</span><span class="sxs-lookup"><span data-stu-id="b7a86-129">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="b7a86-130">Finanzen</span><span class="sxs-lookup"><span data-stu-id="b7a86-130">Finance</span></span>](finance.md)  
<span data-ttu-id="b7a86-131">[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="b7a86-131">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="b7a86-132">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b7a86-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

