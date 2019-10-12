---
title: 'Designdetails: Umgang mit Aufträgen vor dem Planungs-Startdatum | Microsoft Docs'
description: In diesem Thema werden die Regeln beschrieben, die Planung für Aufträge in der fixierten Zone anwendet.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: planning, frozen, design serial, lot
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: bc594a93987bf8740964b082fed25dc8d7e269fe
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307300"
---
# <a name="design-details-dealing-with-orders-before-the-planning-starting-date"></a>Designdetails: Umgang mit Aufträgen vor dem Planungs-Startdatum
Um zu vermeiden, dass ein Beschaffungsplan unmöglichen und daher unbrauchbare Vorschläge anzeigt, berücksichtigt das Planungssystem die Periode bis zum Startdatum als fixierte Zone, für die nichts geplant wird. Die folgende Regel gilt für die fixierte Zone:  

Alle Vorräte und Bedarfe vor dem Startdatum der Planungsperiode gelten als Teil des Lagerbestands oder als geliefert.  

Entsprechend schlägt das Planungssystem, mit wenigen Ausnahmen, keine Änderungen an Beschaffungsaufträgen in der fixierten Zone vor, und keine Auftragsnachverfolgungsverknüpfungen werden für diese Periode erstellt oder gespeichert.  

Die Ausnahmen dieser Regel sind die folgenden:  

* Wenn der voraussichtlich verfügbare Lagerbestand, einschließlich die Summe von Bedarf und Vorrat in der fixierten Zone, geringer als Null ist.  
* Wenn Serien-/Chargennummern auf den zurückdatierten Aufträgen erforderlich sind.  
* Wenn der Vorrat-Bedarf-Satz durch eine Auftrag-zu-Auftrag-Richtlinie verknüpft ist.  

Wenn der anfänglich verfügbare Lagerbestand geringer als Null ist, schlägt das Planungssystem einen Notfallbeschaffungsauftrag am Tag vor der Planperiode vor, um die fehlende Menge zu decken. Deshalb ist der voraussichtliche und der verfügbare Lagerbestand immer mindestens Null, wenn die Planung für die zukünftige Periode beginnt. Die Planungszeile für diesen Beschaffungsauftrag zeigt ein Notwarnsymbol an , und zusätzliche Informationen werden beim Lookup angezeigt.  

## <a name="seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone"></a>Serien-/Chargennummern und Auftrag-zu-Auftrag-Links sind von der fixierten Zone ausgenommen  
Wenn Serien-/Chargennummern erforderlich sind, oder ein Auftrag-zu-Auftrag-Link vorhanden ist, beachtet das Planungssystem die fixierte Zone nicht und berücksichtigt solche Mengen, die vom dem Startdatum zurückdatiert sind und möglicherweise Korrekturmaßnahmen erfordern, wenn bedarf und Vorrat nicht synchronisiert sind. Der Geschäftsgrund für dieses Prinzip ist, dass solche bestimmten bedarf-Vorrat-Sätze übereinstimmen müssen, um sicherzustellen, dass dieser bestimmte Bedarf erfüllt wird.  

## <a name="see-also"></a>Siehe auch  
[Designdetails: Ausgleich von Bedarf und Vorrat](design-details-balancing-demand-and-supply.md)   
[Designdetails: Zentrale Konzepte des Planungssystems](design-details-central-concepts-of-the-planning-system.md)   
[Designdetails: Vorratsplanung](design-details-supply-planning.md)
