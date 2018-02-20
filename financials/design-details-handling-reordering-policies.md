---
title: Designdetails - Abwicklung on Wiederbeschaffungsrichtlinien | Microsoft Docs
description: "Übersicht über Aufgaben für das Definieren einer Wiederbestellungsrichtlinie in die Beschaffungsplanung."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 2a6658508f8e12a11989d54da6d6c8e3a36631cc
ms.contentlocale: de-de
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-handling-reordering-policies"></a>Designdetails: Umgang mit Wiederbeschaffungsrichtlinien
Damit ein Artikel an der Beschaffungsplanung teilnehmen kann, muss eine Wiederbeschaffungsrichtlinie festgelegt werden. Die folgenden vier Wiederbeschaffungsrichtlinien sind verfügbar:  
  
* Feste Bestellmenge  
* Auffüllen auf Maximalbestand  
* Bestellung  
* Los-für-Los  
  
Feste Bestellmenge und Höchstmenge, Richtlinien für die Bestandsplanung. Obwohl die Bestandsplanung eigentlich einfacher als das Ausgleichsverfahren ist, müssen diese Richtlinien gemeinsam mit dem schrittweisen Ausgleich der Nachverfolgung von Vorrat und Bedarf bestehen. Um die Integration zwischen den beiden zu steuern, und Einsehbarkeit in die beteiligte Planungslogik bereitzustellen, steuern strenge Prinzipien, wie Wiederbeschaffungsverfahren angewendet werden.  
  
## <a name="in-this-section"></a>In diesem Abschnitt  
[Designdetails: Die Rolle des Minimalbestands](design-details-the-role-of-the-reorder-point.md)  
[Designdetails: Überwachen der Ebene des voraussichtlichen Lagerbestands und des Minimalbestands](design-details-monitoring-the-projected-inventory-level-and-the-reorder-point.md)  
[Designdetails: Die Rolle des Zeitrahmens](design-details-the-role-of-the-time-bucket.md)  
[Designdetails: Unter dem Überlauflevel bleiben](design-details-staying-under-the-overflow-level.md)  
[Designdetails: Umgang mit voraussichtlichem negativem Lagerbestand](design-details-handling-projected-negative-inventory.md)  
[Designdetails: Wiederbeschaffungsverfahren](design-details-reordering-policies.md)  
  
## <a name="see-also"></a>Siehe auch  
[Designdetails: Planungsparameter](design-details-planning-parameters.md)   
[Designdetails: Planungs-Zuordnungstabelle](design-details-planning-assignment-table.md)   
[Designdetails: Zentrale Konzepte des Planungssystems](design-details-central-concepts-of-the-planning-system.md)   
[Designdetails: Ausgleich von Bedarf und Vorrat](design-details-balancing-demand-and-supply.md)   
[Designdetails: Vorratsplanung](design-details-supply-planning.md)
