---
title: Designdetails - Dimensionssatzposten | Microsoft Docs
description: Diese Dokumentation stellt einen detaillierten technischen Einblick in die Urheberrechtshinweise und Prinzipien bereit, die verwendet werden, um die Dimensionsposten-Einlagerungs- und Buchungsfunktion in  neu zu gestalten.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, dimensions, codeunit
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: c6b66ecee87e1fd128733f541d46b97f44af0453
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "935659"
---
# <a name="design-details-dimension-set-entries"></a><span data-ttu-id="0dc82-103">Designdetails: Dimensionssatzposten</span><span class="sxs-lookup"><span data-stu-id="0dc82-103">Design Details: Dimension Set Entries</span></span>
<span data-ttu-id="0dc82-104">Diese Dokumentation stellt einen detaillierten technischen Einblick in die Konzepte und Prinzipien der Dimensionsposten-Einlagerungs- und Buchungsfunktion in [!INCLUDE[d365fin](includes/d365fin_md.md)] dar.</span><span class="sxs-lookup"><span data-stu-id="0dc82-104">This documentation provides detailed technical insight into the concepts and principles of the dimension-entry storing and posting functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="0dc82-105">Die Dokumentation beginnt mit der Beschreibung der konzeptionellen Übersichten.</span><span class="sxs-lookup"><span data-stu-id="0dc82-105">The documentation starts by describing conceptual overviews.</span></span> <span data-ttu-id="0dc82-106">Dann wird die technische Architektur erklärt.</span><span class="sxs-lookup"><span data-stu-id="0dc82-106">Then it explains the technical architecture.</span></span> <span data-ttu-id="0dc82-107">Schließlich bietet sie Codebeispiele, die Sie für Dimensionscodemigration und -Upgrade von Versionen vor Dynamics NAV 2013R2 vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="0dc82-107">Finally, it provides code examples to prepare you for dimension code migration and upgrade from versions earlier than Dynamics NAV 2013R2.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="0dc82-108">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="0dc82-108">In This Section</span></span>  
[<span data-ttu-id="0dc82-109">Dimensionssatz-Eintrags-Übersicht</span><span class="sxs-lookup"><span data-stu-id="0dc82-109">Dimension Set Entries Overview</span></span>](design-details-dimension-set-entries-overview.md)  
[<span data-ttu-id="0dc82-110">Designdetails: Suche nach Dimensionskombinationen</span><span class="sxs-lookup"><span data-stu-id="0dc82-110">Design Details: Searching for Dimension Combinations</span></span>](design-details-searching-for-dimension-combinations.md)  
[<span data-ttu-id="0dc82-111">Designdetails: Tabellenstruktur</span><span class="sxs-lookup"><span data-stu-id="0dc82-111">Design Details: Table Structure</span></span>](design-details-table-structure.md)  
[<span data-ttu-id="0dc82-112">Designdetails: Codeunit 408 Dimension Management</span><span class="sxs-lookup"><span data-stu-id="0dc82-112">Design Details: Codeunit 408 Dimension Management</span></span>](design-details-codeunit-408-dimension-management.md)  
[<span data-ttu-id="0dc82-113">Designdetails: Codebeispiele von geänderten Mustern in Änderungen</span><span class="sxs-lookup"><span data-stu-id="0dc82-113">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)
