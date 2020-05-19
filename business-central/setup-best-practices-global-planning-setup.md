---
title: Bewährte Vorgehensweisen für globale Planung einrichten | Microsoft Docs
description: Das Inforegister "Planung" auf der Seite "Herstellung einrichten" enthält eine Reihe von Feldern, die globale Regeln für die Beschaffungsplanung definieren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 3897602d405f13b5de4a1bc401cc409cb5ef58ec
ms.sourcegitcommit: 99915b493a7e49d12c530f2f9fda1fcedb518b6e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "3271894"
---
# <a name="setup-best-practices-global-planning-setup"></a><span data-ttu-id="f775b-103">Bewährte Einrichtungsmethoden: Globale Planungseinrichtung</span><span class="sxs-lookup"><span data-stu-id="f775b-103">Setup Best Practices: Global Planning Setup</span></span>
<span data-ttu-id="f775b-104">Das Inforegister **Planung** auf der Seite **Herstellung einrichten** enthält eine Reihe von Feldern, die globale Regeln für die Beschaffungsplanung definieren.</span><span class="sxs-lookup"><span data-stu-id="f775b-104">The **Planning** FastTab on the **Manufacturing Setup** page contains several fields that define global rules for supply planning.</span></span>  

 <span data-ttu-id="f775b-105">Die folgende Tabelle enthält bewährte Methoden zum Einrichten von ausgewählten globalen Planungsparameterfeldern.</span><span class="sxs-lookup"><span data-stu-id="f775b-105">The following table provides best practices on how to set up selected global planning parameter fields.</span></span> <span data-ttu-id="f775b-106">Für weitere Informationen zu einem Feld klicken Sie auf den Link in der Spalte **Feldeinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="f775b-106">For more information about a field, choose the link in the **Setup field** column.</span></span>  

|<span data-ttu-id="f775b-107">Feldeinstellungen</span><span class="sxs-lookup"><span data-stu-id="f775b-107">Setup field</span></span>|<span data-ttu-id="f775b-108">Bewährte Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="f775b-108">Best practice</span></span>|<span data-ttu-id="f775b-109">Bemerkung</span><span class="sxs-lookup"><span data-stu-id="f775b-109">Comment</span></span>|  
|-----------------|-------------------|-------------|  
|<span data-ttu-id="f775b-110">Absatzpl. pro Lagerort verw.</span><span class="sxs-lookup"><span data-stu-id="f775b-110">Use Forecast on Locations</span></span>|<span data-ttu-id="f775b-111">Wählen Sie diese Option aus, wenn Sie für bestimmte Lagerorte eine Planung haben.</span><span class="sxs-lookup"><span data-stu-id="f775b-111">Select if you have forecasts for specific locations.</span></span>||  
|<span data-ttu-id="f775b-112">Komponenten von Lagerort</span><span class="sxs-lookup"><span data-stu-id="f775b-112">Components at Location</span></span>|<span data-ttu-id="f775b-113">Wenn Artikel nicht als Lagerhaltungsdaten definiert sind, wählen Sie den Lagerortcode Ihres Auffülllagerorts aus.</span><span class="sxs-lookup"><span data-stu-id="f775b-113">If items are not defined as SKUs, select the location code of your main warehouse.</span></span>|<span data-ttu-id="f775b-114">Dies gilt auch, wenn Sie nur den Bestellvorschlag verwenden.</span><span class="sxs-lookup"><span data-stu-id="f775b-114">This also applies if you only use the requisition worksheet.</span></span>|  
|<span data-ttu-id="f775b-115">Leerer Überlauflevel</span><span class="sxs-lookup"><span data-stu-id="f775b-115">Blank Overflow Level</span></span>|<span data-ttu-id="f775b-116">Wählen Sie **Standardberechnung zulassen** wenn Sie von Microsoft Dynamics NAV 5.0 oder frrüher migrieren.</span><span class="sxs-lookup"><span data-stu-id="f775b-116">Select **Allow Default Calculation** if you are migrating from Microsoft Dynamics NAV 5.0 or earlier.</span></span>|<span data-ttu-id="f775b-117">Verwenden Sie dies nur, wenn alle oder einige Artikel den Minimalbestand übersteigen dürfen.</span><span class="sxs-lookup"><span data-stu-id="f775b-117">Use only if you want to allow all or some of your items to overflow the reorder point.</span></span>|  
|<span data-ttu-id="f775b-118">Standardtoleranzperiode</span><span class="sxs-lookup"><span data-stu-id="f775b-118">Default Dampener Period</span></span>|<span data-ttu-id="f775b-119">Die Einstellung muss zwischen 1D und 5D liegen.</span><span class="sxs-lookup"><span data-stu-id="f775b-119">Set between 1D and 5D.</span></span><br /><br /> <span data-ttu-id="f775b-120">Bei Neulingen in der Planung in [!INCLUDE[d365fin](includes/d365fin_md.md)] legen Sie eine längere Periode fest.</span><span class="sxs-lookup"><span data-stu-id="f775b-120">If new to planning in [!INCLUDE[d365fin](includes/d365fin_md.md)], then set a longer period.</span></span>|<span data-ttu-id="f775b-121">Wenn Benutzer mit den verschiedenen Gründen für Ereignismeldungen vertraut sind, dann kürzen Sie die Toleranzperiode, um mehr Änderungsvorschläge zu erlauben.</span><span class="sxs-lookup"><span data-stu-id="f775b-121">When users are more familiar with the different reasons for action messages, then shorten the dampener period to allow more change suggestions.</span></span>|  
|<span data-ttu-id="f775b-122">Toleranzmenge %</span><span class="sxs-lookup"><span data-stu-id="f775b-122">Default Dampener Quantity %</span></span>|<span data-ttu-id="f775b-123">Legen Sie sie zwischen 5 und 20 Prozent der Losgröße des Artikels fest.</span><span class="sxs-lookup"><span data-stu-id="f775b-123">Set between 5 and 20 percent of the item’s lot size.</span></span>||  

## <a name="see-also"></a><span data-ttu-id="f775b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f775b-124">See Also</span></span>  
 <span data-ttu-id="f775b-125">[Bewährte Einrichtungsmethoden: Beschaffungsplanung](setup-best-practices-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="f775b-125">[Setup Best Practices: Supply Planning](setup-best-practices-supply-planning.md) </span></span>  
 <span data-ttu-id="f775b-126">[Designdetails: Vorratsplanung](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="f775b-126">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
 [<span data-ttu-id="f775b-127">Richten Sie komplexe Anwendungsbereiche mithilfe bewährter Methoden ein</span><span class="sxs-lookup"><span data-stu-id="f775b-127">Set Up Complex Application Areas Using Best Practices</span></span>](set-up-complex-application-areas-using-best-practices.md)  
 <span data-ttu-id="f775b-128">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f775b-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
