---
title: Tabelleninformationen anzeigen
description: Erfahren Sie, wie Sie Informationen über Datenbanktabellen direkt über die Clientschnittstelle in Business Central anzeigen können.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: a4695594573056ec492bc15c29d1b6fca3100e97
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388674"
---
# <a name="viewing-table-information"></a><span data-ttu-id="1ae75-103">Tabelleninformationen anzeigen</span><span class="sxs-lookup"><span data-stu-id="1ae75-103">Viewing Table Information</span></span>

<span data-ttu-id="1ae75-104">Die Seite **8700 Tabelleninformationen** enthält Informationen zu allen System- und Geschäftstabellen in einer Business Central-Lösung.</span><span class="sxs-lookup"><span data-stu-id="1ae75-104">The page **8700 Table Information** provides information about all system and business tables in a Business Central solution.</span></span> <span data-ttu-id="1ae75-105">Auf der Seite werden insbesondere Informationen zur Datenmenge angezeigt, die die Tabellen enthalten.</span><span class="sxs-lookup"><span data-stu-id="1ae75-105">In particular, the page displays information about the amount of data the tables contain.</span></span>

<span data-ttu-id="1ae75-106">Diese Informationen sind hilfreich bei der Behebung von Leistungsproblemen, da Sie die Verteilung der Datengröße auf Tabellen anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="1ae75-106">This information is useful for troubleshooting performance problems, because let's you see the distribution of data size across tables.</span></span>

## <a name="viewing-table-information"></a><span data-ttu-id="1ae75-107">Tabelleninformationen anzeigen</span><span class="sxs-lookup"><span data-stu-id="1ae75-107">Viewing table information</span></span>

<span data-ttu-id="1ae75-108">Wählen Sie zum Öffnen dieser Seite das Symbol ![Suche nach Seite oder Bericht](media/ui-search/search_small.png "Suchen Sie nach dem Symbol Seite oder Bericht") aus, geben Sie **Tabelleninformationen** ein, und wählen Sie dann den entsprechenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="1ae75-108">To open this page, select the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Table Information**, and then choose the related link.</span></span>

<span data-ttu-id="1ae75-109">In der folgenden Tabelle werden die für jede Tabelle bereitgestellten Informationen beschrieben:</span><span class="sxs-lookup"><span data-stu-id="1ae75-109">The following table describes the information provided for each table:</span></span>

|<span data-ttu-id="1ae75-110">Spalte</span><span class="sxs-lookup"><span data-stu-id="1ae75-110">Column</span></span>|<span data-ttu-id="1ae75-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1ae75-111">Description</span></span>|
|------|-----------|
|<span data-ttu-id="1ae75-112">Unternehmensname</span><span class="sxs-lookup"><span data-stu-id="1ae75-112">Company Name</span></span>|<span data-ttu-id="1ae75-113">Name des Unternehmens (sofern zutreffend), zu dem die Tabelle gehört.</span><span class="sxs-lookup"><span data-stu-id="1ae75-113">The name of the company, if any, that the table belongs to.</span></span>|
|<span data-ttu-id="1ae75-114">Tabellenname</span><span class="sxs-lookup"><span data-stu-id="1ae75-114">Table Name</span></span>|<span data-ttu-id="1ae75-115">Der Name der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1ae75-115">The name of the table.</span></span>|
|<span data-ttu-id="1ae75-116">Tabellennr.</span><span class="sxs-lookup"><span data-stu-id="1ae75-116">Table No.</span></span>|<span data-ttu-id="1ae75-117">Die ID der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1ae75-117">The ID of the table</span></span>|
|<span data-ttu-id="1ae75-118">Anzahl</span><span class="sxs-lookup"><span data-stu-id="1ae75-118">No.</span></span> <span data-ttu-id="1ae75-119">der Datensätze</span><span class="sxs-lookup"><span data-stu-id="1ae75-119">of Records</span></span>|<span data-ttu-id="1ae75-120">Die Gesamtzahl der in der Tabelle gespeicherten Datensätze.</span><span class="sxs-lookup"><span data-stu-id="1ae75-120">The total number of records stored in the table.</span></span>|
|<span data-ttu-id="1ae75-121">Datensatzgröße</span><span class="sxs-lookup"><span data-stu-id="1ae75-121">Record Size</span></span>|<span data-ttu-id="1ae75-122">Die durchschnittliche Datensatzgröße in KB/Datensatz.</span><span class="sxs-lookup"><span data-stu-id="1ae75-122">The average record size in KB/record.</span></span> <span data-ttu-id="1ae75-123">Der Wert wird nach folgender Formel berechnet: 1024 (Größe)/(Anzahl</span><span class="sxs-lookup"><span data-stu-id="1ae75-123">The value is calculated using the following formula: 1024(Size)/(No.</span></span> <span data-ttu-id="1ae75-124">der Datensätze).</span><span class="sxs-lookup"><span data-stu-id="1ae75-124">of Records)\`.</span></span> |

## <a name="see-also"></a><span data-ttu-id="1ae75-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ae75-125">See Also</span></span>

[<span data-ttu-id="1ae75-126">Überprüfen von Seiten</span><span class="sxs-lookup"><span data-stu-id="1ae75-126">Inspecting Pages</span></span>](across-inspect-page.md)  
[<span data-ttu-id="1ae75-127">Artikel zur Leistung für Entwickler</span><span class="sxs-lookup"><span data-stu-id="1ae75-127">Performance Articles For Developers</span></span>](/dynamics365/business-central/dev-itpro/performance/performance-developer)  


[!INCLUDE[footer-include](includes/footer-banner.md)]