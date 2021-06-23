---
title: 'Designdetails: Fibu-Buchungszeile - Überblick | Microsoft Docs'
description: Diese Dokumentation stellt einen detaillierten technischen Einblick in die Urheberrechtshinweise und Prinzipien bereit, die verwendet werden, um die Finanzbuchhaltungs-Buchungsfunktion in Business Central neu zu gestalten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general journal, posting, codeunit 12
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 8492c83437be4cd850bafdaaa5dc70d00a075674
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215228"
---
# <a name="design-details-general-journal-post-line"></a><span data-ttu-id="bb503-103">Designdetails: Fibu Buch.-Blatt-Buchungsposition</span><span class="sxs-lookup"><span data-stu-id="bb503-103">Design Details: General Journal Post Line</span></span>

<span data-ttu-id="bb503-104">Diese Dokumentation stellt einen detaillierten technischen Einblick in die Urheberrechtshinweise und Prinzipien bereit, die verwendet wurden, um die Finanzbuchhaltungs-Buchungsfunktion in [!INCLUDE[prod_short](includes/prod_short.md)] neu zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="bb503-104">This documentation provides detailed technical insight into the concepts and principles that were used to redesign the general journal posting line feature in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="bb503-105">Durch die Neugestaltung wurde Codeunit 12 vereinfacht und leichter zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="bb503-105">The redesign made codeunit 12 simpler and more maintainable.</span></span> <span data-ttu-id="bb503-106">Die Dokumentation beginnt mit der Beschreibung der konzeptionellen Übersichten der Neugestaltung.</span><span class="sxs-lookup"><span data-stu-id="bb503-106">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="bb503-107">Dann wird die technische Architektur erklärt, um die Änderungen zu zeigen, die sich aus der Neugestaltung ergeben.</span><span class="sxs-lookup"><span data-stu-id="bb503-107">Then it explains the technical architecture to show the changes that result from the redesign.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="bb503-108">Die Informationen in diesem Abschnitt gelten für die Neugestaltung in einer früheren Version des Produkts, Microsoft Dynamics NAV 2013 R2.</span><span class="sxs-lookup"><span data-stu-id="bb503-108">The information in this section applies to the redesign in an earlier version of the product, Microsoft Dynamics NAV 2013 R2.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bb503-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="bb503-109">In This Section</span></span>

[<span data-ttu-id="bb503-110">Fibu-Buchungszeile - Überblick</span><span class="sxs-lookup"><span data-stu-id="bb503-110">General Journal Post Line Overview</span></span>](design-details-general-journal-post-line-overview.md)  
[<span data-ttu-id="bb503-111">Designdetails: Buchungs-Schnittstellenstruktur</span><span class="sxs-lookup"><span data-stu-id="bb503-111">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="bb503-112">Designdetails: Buchungs-Modul-Struktur</span><span class="sxs-lookup"><span data-stu-id="bb503-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  

## <a name="see-also"></a><span data-ttu-id="bb503-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb503-113">See Also</span></span>

<span data-ttu-id="bb503-114">[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)
[Designdetails: Fibu Buch.-Blatt-Buchungszeilen (Dynamics NAV)](/dynamics-nav-app/design-details-general-journal-post-line)</span><span class="sxs-lookup"><span data-stu-id="bb503-114">[Working with General Journals](ui-work-general-journals.md)
[Design Details: General Journal Post Line (Dynamics NAV)](/dynamics-nav-app/design-details-general-journal-post-line)</span></span>  

[!INCLUDE[footer-include](includes/footer-banner.md)]