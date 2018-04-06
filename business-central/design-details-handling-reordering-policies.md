---
title: Designdetails - Abwicklung on Wiederbeschaffungsrichtlinien | Microsoft Docs
description: "Übersicht über Aufgaben für das Definieren einer Wiederbestellungsrichtlinie in die Beschaffungsplanung."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: b273dedd269d8b86ba4fa7a9d9540c44b701a97e
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

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
