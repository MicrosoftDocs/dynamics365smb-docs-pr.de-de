---
title: Designdetails - Dimensionssatzposten | Microsoft Docs
description: Diese Dokumentation stellt einen detaillierten technischen Einblick in die Urheberrechtshinweise und Prinzipien bereit, die verwendet werden, um die Dimensionsposten-Einlagerungs- und Buchungsfunktion in  neu zu gestalten.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, dimensions, codeunit
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 17fd783bd44faa914d473aae35ddc31145c181ef
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-dimension-set-entries"></a><span data-ttu-id="6b2a3-103">Designdetails: Dimensionssatzposten</span><span class="sxs-lookup"><span data-stu-id="6b2a3-103">Design Details: Dimension Set Entries</span></span>
<span data-ttu-id="6b2a3-104">Diese Dokumentation stellt einen detaillierten technischen Einblick in die Urheberrechtshinweise und Prinzipien bereit, die verwendet werden, um die Dimensionsposten-Einlagerungs- und Buchungsfunktion in [!INCLUDE[d365fin](includes/d365fin_md.md)] neu zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="6b2a3-104">This documentation provides detailed technical insight into the concepts and principles that are used to redesign the dimension entry storing and posting feature in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="6b2a3-105">Die Dokumentation beginnt mit der Beschreibung der konzeptionellen Übersichten der Neugestaltung.</span><span class="sxs-lookup"><span data-stu-id="6b2a3-105">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="6b2a3-106">Dann wird die technische Architektur erklärt, um zu zeigen, wie die Neugestaltung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="6b2a3-106">Then it explains the technical architecture to show how the redesign is made.</span></span> <span data-ttu-id="6b2a3-107">Schließlich bietet sie Codebeispiele, die Sie für Dimensionscodemigration und -Upgrade vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="6b2a3-107">Finally, it provides code examples to prepare you for dimension code migration and upgrade.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="6b2a3-108">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="6b2a3-108">In This Section</span></span>  
[<span data-ttu-id="6b2a3-109">Dimensionssatz-Eintrags-Übersicht</span><span class="sxs-lookup"><span data-stu-id="6b2a3-109">Dimension Set Entries Overview</span></span>](design-details-dimension-set-entries-overview.md)  
[<span data-ttu-id="6b2a3-110">Designdetails: Suche nach Dimensionskombinationen</span><span class="sxs-lookup"><span data-stu-id="6b2a3-110">Design Details: Searching for Dimension Combinations</span></span>](design-details-searching-for-dimension-combinations.md)  
[<span data-ttu-id="6b2a3-111">Designdetails: Tabellenstruktur</span><span class="sxs-lookup"><span data-stu-id="6b2a3-111">Design Details: Table Structure</span></span>](design-details-table-structure.md)  
[<span data-ttu-id="6b2a3-112">Designdetails: Codeunit 408 Dimension Management</span><span class="sxs-lookup"><span data-stu-id="6b2a3-112">Design Details: Codeunit 408 Dimension Management</span></span>](design-details-codeunit-408-dimension-management.md)  
[<span data-ttu-id="6b2a3-113">Designdetails: Codebeispiele von geänderten Mustern in Änderungen</span><span class="sxs-lookup"><span data-stu-id="6b2a3-113">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)

