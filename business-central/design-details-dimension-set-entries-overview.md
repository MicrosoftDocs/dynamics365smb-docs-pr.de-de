---
title: Dimensionssatzposten Übersicht | Microsoft Docs
description: In diesem Thema wird beschrieben, wie Dimensionssatzposten in Dynamics 365 gespeichert und gebucht werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 98916c0843d84c76529e7b6f475ba207b2590a08
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911180"
---
# <a name="dimension-set-entries-overview"></a><span data-ttu-id="4c9c9-103">Dimensionssatz-Eintrags-Übersicht</span><span class="sxs-lookup"><span data-stu-id="4c9c9-103">Dimension Set Entries Overview</span></span>
<span data-ttu-id="4c9c9-104">In diesem Thema wird beschrieben, wie Dimensionssatzposten in [!INCLUDE[d365fin](includes/d365fin_md.md)] gespeichert und gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="4c9c9-104">This topic describes how dimension set entries are stored and posted in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="dimension-sets"></a><span data-ttu-id="4c9c9-105">Dimensionssätze</span><span class="sxs-lookup"><span data-stu-id="4c9c9-105">Dimension Sets</span></span>  
<span data-ttu-id="4c9c9-106">Ein Dimensionssatz ist eine eindeutige Kombination von Dimensionswerten.</span><span class="sxs-lookup"><span data-stu-id="4c9c9-106">A dimension set is a unique combination of dimension values.</span></span> <span data-ttu-id="4c9c9-107">Er wird als Dimensionssatzposten in die Datenbank gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4c9c9-107">It is stored as dimension set entries in the database.</span></span> <span data-ttu-id="4c9c9-108">Jeder Dimensionssatzposten stellt einen einzelnen Dimensionswert dar.</span><span class="sxs-lookup"><span data-stu-id="4c9c9-108">Each dimension set entry represents a single dimension value.</span></span> <span data-ttu-id="4c9c9-109">Der Dimensionssatz wird durch eine allgemeine Dimensionssatz-ID identifiziert, die jedem Dimensionssatzposten zugewiesen wird, der zum Dimensionssatz gehört.</span><span class="sxs-lookup"><span data-stu-id="4c9c9-109">The dimension set is identified by a common dimension set ID that is assigned to each dimension set entry that belongs to the dimension set.</span></span>  

<span data-ttu-id="4c9c9-110">Im folgenden Beispiel wird ein Dimensionssatz gezeigt, der drei Dimensionssatzposten aufweist.</span><span class="sxs-lookup"><span data-stu-id="4c9c9-110">The following example shows a dimension set that has three dimension set entries.</span></span> <span data-ttu-id="4c9c9-111">Der Dimensionssatz wird durch eine Dimensionssatz-ID, nämlich 108, identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4c9c9-111">The dimension set is identified by a dimension set ID, which is 108.</span></span>  

|<span data-ttu-id="4c9c9-112">Dimensionssatz-ID</span><span class="sxs-lookup"><span data-stu-id="4c9c9-112">Dimension Set ID</span></span>|<span data-ttu-id="4c9c9-113">Dimensionscode</span><span class="sxs-lookup"><span data-stu-id="4c9c9-113">Dimension Code</span></span>|<span data-ttu-id="4c9c9-114">Dimensionswertcode</span><span class="sxs-lookup"><span data-stu-id="4c9c9-114">Dimension Value Code</span></span>|<span data-ttu-id="4c9c9-115">Dimensionswertname</span><span class="sxs-lookup"><span data-stu-id="4c9c9-115">Dimension Value Name</span></span>|  
|----------------------|--------------------|--------------------------|--------------------------|  
|<span data-ttu-id="4c9c9-116">108</span><span class="sxs-lookup"><span data-stu-id="4c9c9-116">108</span></span>|<span data-ttu-id="4c9c9-117">BEREICH</span><span class="sxs-lookup"><span data-stu-id="4c9c9-117">AREA</span></span>|<span data-ttu-id="4c9c9-118">70</span><span class="sxs-lookup"><span data-stu-id="4c9c9-118">70</span></span>|<span data-ttu-id="4c9c9-119">Nordamerika</span><span class="sxs-lookup"><span data-stu-id="4c9c9-119">America North</span></span>|  
|<span data-ttu-id="4c9c9-120">108</span><span class="sxs-lookup"><span data-stu-id="4c9c9-120">108</span></span>|<span data-ttu-id="4c9c9-121">UNTERNEHMENSGRUPPE</span><span class="sxs-lookup"><span data-stu-id="4c9c9-121">BUSINESSGROUP</span></span>|<span data-ttu-id="4c9c9-122">POS1</span><span class="sxs-lookup"><span data-stu-id="4c9c9-122">HOME</span></span>|<span data-ttu-id="4c9c9-123">Start</span><span class="sxs-lookup"><span data-stu-id="4c9c9-123">Home</span></span>|  
|<span data-ttu-id="4c9c9-124">108</span><span class="sxs-lookup"><span data-stu-id="4c9c9-124">108</span></span>|<span data-ttu-id="4c9c9-125">KOSTENSTELLE</span><span class="sxs-lookup"><span data-stu-id="4c9c9-125">DEPARTMENT</span></span>|<span data-ttu-id="4c9c9-126">VERKAUF</span><span class="sxs-lookup"><span data-stu-id="4c9c9-126">SALES</span></span>|<span data-ttu-id="4c9c9-127">Verkauf</span><span class="sxs-lookup"><span data-stu-id="4c9c9-127">Sales</span></span>|  

## <a name="dimension-set-entries"></a><span data-ttu-id="4c9c9-128">Dimensionssatzposten</span><span class="sxs-lookup"><span data-stu-id="4c9c9-128">Dimension Set Entries</span></span>  
<span data-ttu-id="4c9c9-129">Dimensionssätze werden in der Tabelle als **Dimensionssatzposten** mit derselben Dimensionssatz-ID gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4c9c9-129">Dimension sets are stored in the **Dimension Set Entry** table as dimension set entries with the same dimension set ID.</span></span>  

<span data-ttu-id="4c9c9-130">![Fluss von Dimensionssatzeinträgen](media/dimensionentrynav7.png "Fluss der Dimensionssatzeinträge")</span><span class="sxs-lookup"><span data-stu-id="4c9c9-130">![Flow of dimension set entries](media/dimensionentrynav7.png "Flow of dimension set entries")</span></span>  

<span data-ttu-id="4c9c9-131">Wenn Sie eine neue Buch.-Blattzeile, einen Belegkopf oder eine Belegzeile erstellen, können Sie eine Kombination von Dimensionswerten angeben.</span><span class="sxs-lookup"><span data-stu-id="4c9c9-131">When you create a new journal line, document header, or document line, you can specify a combination of dimension values.</span></span> <span data-ttu-id="4c9c9-132">Anstatt jeden Dimensionswert explizit in der Datenbank zu speichern, wird eine Dimensionssatz-ID der Buch.-Blattzeile, dem Belegkopf oder der Belegzeile zugewiesen, um den Dimensionssatz anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4c9c9-132">Instead of explicitly storing each dimension value in the database, a dimension set ID is assigned to the journal line, document header, or document line to specify the dimension set.</span></span>  

<span data-ttu-id="4c9c9-133">Wenn Sie die Seite **Dimensionssatzeinträge bearbeiten** bearbeiten und schließen, wird eine Prüfung ausgeführt, um festzustellen, ob die Kombination aus Dimensionswerten als Dimensionssatz in der Tabelle existiert.</span><span class="sxs-lookup"><span data-stu-id="4c9c9-133">When you edit and close the **Edit Dimension Set Entries** page, a check is performed to see whether the combination of dimension values exists as a dimension set in the table.</span></span> <span data-ttu-id="4c9c9-134">Wenn die Kombination in der Tabelle auftritt, wird die entsprechende Dimensionssatz-ID der Buch.-Blattzeile, dem Belegkopf oder der Belegzeile zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="4c9c9-134">If the combination occurs in the table, then the corresponding dimension set ID is assigned to the journal line, document header, or document line.</span></span> <span data-ttu-id="4c9c9-135">Andernfalls wird ein neuer Dimensionssatz der Tabelle hinzugefügt, und die neue Dimensionssatz-ID wird der Buch.-Blattzeile, dem Belegkopf oder der Belegzeile zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="4c9c9-135">Otherwise, a new dimension set is added to the table, and the new dimension set ID is assigned to the journal line, document header, or document line.</span></span>

## <a name="codeunit-408-dimension-management"></a><span data-ttu-id="4c9c9-136">Codeunit 408 Dimension Management</span><span class="sxs-lookup"><span data-stu-id="4c9c9-136">Codeunit 408 Dimension Management</span></span>
<span data-ttu-id="4c9c9-137">Codeunit 408 Dimension Management ist eine Funktionsbibliothek, die häufige Aufgaben im Zusammenhang mit Dimensionen behandelt, wie etwa das Kopieren von einer Tabelle zu einer anderen oder von einem Beleg zu einem anderen.</span><span class="sxs-lookup"><span data-stu-id="4c9c9-137">Codeunit 408, Dimension Management, is a function library that handles common tasks that are related to dimensions, such as copying from one table to another or from one document to another.</span></span>

## <a name="performance-improvement"></a><span data-ttu-id="4c9c9-138">Leistungsverbesserung</span><span class="sxs-lookup"><span data-stu-id="4c9c9-138">Performance Improvement</span></span>  
<span data-ttu-id="4c9c9-139">Durch das einmalige Speichern von Dimensionssätzen in der Datenbank wird Datenbankplatz beibehalten und die Gesamtleistung verbessert.</span><span class="sxs-lookup"><span data-stu-id="4c9c9-139">By storing dimension sets once in the database, database space is preserved and overall performance is improved.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4c9c9-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c9c9-140">See Also</span></span>  
<span data-ttu-id="4c9c9-141">[Designdetails: Suche nach Dimensionskombinationen](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="4c9c9-141">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
<span data-ttu-id="4c9c9-142">[Designdetails: Tabellenstruktur](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="4c9c9-142">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
[<span data-ttu-id="4c9c9-143">Designdetails: Dimensionssatzeinträge</span><span class="sxs-lookup"><span data-stu-id="4c9c9-143">Design Details: Dimension Set Entries</span></span>](design-details-dimension-set-entries.md)   
