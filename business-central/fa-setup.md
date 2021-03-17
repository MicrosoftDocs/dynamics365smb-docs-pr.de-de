---
title: Anlagen einrichten | Microsoft Docs
description: Kennenlernen der die Abfolge von Aufgaben, die Sie ausführen müssen, um Anlagen einzurichten, wie Arbeitsplätze oder Gebäude.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: machinery, buildings
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3044d878260dbab4e9d2423398b7654386671638
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5380077"
---
# <a name="setting-up-fixed-assets"></a><span data-ttu-id="823f8-103">Anlagen einrichten</span><span class="sxs-lookup"><span data-stu-id="823f8-103">Setting Up Fixed Assets</span></span>
<span data-ttu-id="823f8-104">Um mit Anlagen arbeiten können, müssen Sie einige Elemente festlegen:</span><span class="sxs-lookup"><span data-stu-id="823f8-104">Before you can work with Fixed Assets, you need to define a few things:</span></span>  

* <span data-ttu-id="823f8-105">Wie Sie Anlagen versichern, verwalten und abschreiben.</span><span class="sxs-lookup"><span data-stu-id="823f8-105">How you insure, maintain, and depreciate fixed assets.</span></span>  
* <span data-ttu-id="823f8-106">Wie Sie Kosten und andere Werte in der Finanzbuchhaltung erfassen.</span><span class="sxs-lookup"><span data-stu-id="823f8-106">How you record costs and other values in the general ledger.</span></span>  

<span data-ttu-id="823f8-107">Die folgende Tabelle enthält Verknüpfungen für weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="823f8-107">The table below has links to more information.</span></span> <span data-ttu-id="823f8-108">Nachdem Sie diese Dinge festgelegt haben, können Sie die verschiedene Aktivitäten beginnen.</span><span class="sxs-lookup"><span data-stu-id="823f8-108">After you set those things up, you can start various activities.</span></span> <span data-ttu-id="823f8-109">Weitere Informationen finden Siue unter [Anlagen](fa-manage.md).</span><span class="sxs-lookup"><span data-stu-id="823f8-109">For more information, see [Fixed Assets](fa-manage.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="823f8-110">Sie können Anlagentransaktionen auf der Seite **Anlagen Fibu Buch.-Blatt** oder auf der Seite **Anlagen Buch-Blatt** erfassen, abhängig davon, ob die Transaktionen für Finanzberichte oder zur internen Verwaltung bestimmt sind.</span><span class="sxs-lookup"><span data-stu-id="823f8-110">You can record fixed asset transactions in the **Fixed Asset G/L Journal** or **Fixed Asset Journal** pages, depending on whether the transactions are for financial reporting or for internal management.</span></span> <span data-ttu-id="823f8-111">Die Hilfe zu den Anlagen beschreibt lediglich, wie das Fenster **Anlagen Fibu Buch.-Blatt** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="823f8-111">Help for Fixed Assets only describes how to use the **Fixed Asset G/L Journal** page.</span></span>  

<span data-ttu-id="823f8-112">Wenn Sie das Kontrollkästchen für eine Anlagenaktivität im Abschnitt **Fibu-Integration** im Fenster **AfA-Buch-Karte** aktiveren, wird die Seite **Anlagen Fibu Buch.-Blatt** verwendet, um Transaktionen für die fragliche Aktivität zu buchen.</span><span class="sxs-lookup"><span data-stu-id="823f8-112">When you enable a fixed asset activity in the **G/L Integration** section on the **Depreciation Book Card** page, the **Fixed Asset G/L Journal** page is used to post transactions for the activity.</span></span>

<span data-ttu-id="823f8-113">Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Themen, die sie beschreiben..</span><span class="sxs-lookup"><span data-stu-id="823f8-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

| <span data-ttu-id="823f8-114">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="823f8-114">To</span></span> | <span data-ttu-id="823f8-115">Siehe</span><span class="sxs-lookup"><span data-stu-id="823f8-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="823f8-116">Richten Sie Standardsachkonten, Verteilungsschlüssel, Buch.-Blattvorlagen und - namen für Anlagebuchungen ein und erstellen feste Anlageklassen und Unterklassen, wie beispielsweise materielle und immaterielle.</span><span class="sxs-lookup"><span data-stu-id="823f8-116">Set up default G/L accounts, allocation keys, journal templates and batches for fixed asset posting, and set up fixed asset classes and subclasses, such as Tangible and Intangible.</span></span> |[<span data-ttu-id="823f8-117">Allgemeine Anlagen-Informationen einrichten</span><span class="sxs-lookup"><span data-stu-id="823f8-117">Set Up General Fixed Assets Information</span></span>](fa-how-setup-general.md) |
| <span data-ttu-id="823f8-118">Erstellen Sie AfA-Bücher, definieren verschiedene AfA-Methoden, integrieren in die Finanzbuchhaltung und aktiveren das Kopieren der Posten in mehrere AfA-Bücher.</span><span class="sxs-lookup"><span data-stu-id="823f8-118">Create depreciation books, define various depreciation methods, integrate with the general ledger, and enable duplication of entries in several depreciation books.</span></span> |[<span data-ttu-id="823f8-119">Richten Sie eine neue Anlagenkarte ein.</span><span class="sxs-lookup"><span data-stu-id="823f8-119">Set Up Fixed Asset Depreciation</span></span>](fa-how-setup-depreciation.md) |
| <span data-ttu-id="823f8-120">Aktivieren Sie Versicherungen von Anlagen, richten allgemeine Versicherungsinformationen und eine Versicherungskarte pro Versicherung ein und bereiten Buch.-Blätter vor, um Versicherungskosten zu buchen.</span><span class="sxs-lookup"><span data-stu-id="823f8-120">Enable insurance of fixed assets, set up general insurance information, an insurance card per policy, and prepare journals to post insurance costs.</span></span> |[<span data-ttu-id="823f8-121">Um Anlagenversicherung einzurichten:</span><span class="sxs-lookup"><span data-stu-id="823f8-121">Set Up Fixed Asset Insurance</span></span>](fa-how-setup-insurance.md) |
| <span data-ttu-id="823f8-122">Aktivieren Sie die Wartung von Anlagen, richten allgemeine Wartungsinformationen und Wartungs-Buchungskonten ein, und definieren Sie Arten von Wartungsarbeiten.</span><span class="sxs-lookup"><span data-stu-id="823f8-122">Enable maintenance of fixed assets, set up general maintenance information, set up maintenance posting accounts, and define types of maintenance work.</span></span> |[<span data-ttu-id="823f8-123">Um Anlagenwartung einzurichten:</span><span class="sxs-lookup"><span data-stu-id="823f8-123">Set Up Fixed Asset Maintenance</span></span>](fa-how-setup-maintenance.md) |
| <span data-ttu-id="823f8-124">Informieren Sie sich über verschiedene Anlagen-AfA-Methoden.</span><span class="sxs-lookup"><span data-stu-id="823f8-124">Learn about different fixed asset depreciation methods.</span></span> |[<span data-ttu-id="823f8-125">Abschreibungsmethoden</span><span class="sxs-lookup"><span data-stu-id="823f8-125">Depreciation Methods</span></span>](fa-depreciation-methods.md) |

## <a name="see-also"></a><span data-ttu-id="823f8-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="823f8-126">See Also</span></span>
[<span data-ttu-id="823f8-127">Anlagen</span><span class="sxs-lookup"><span data-stu-id="823f8-127">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="823f8-128">Finanzen</span><span class="sxs-lookup"><span data-stu-id="823f8-128">Finance</span></span>](finance.md)  
[<span data-ttu-id="823f8-129">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="823f8-129">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="823f8-130">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="823f8-130">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]