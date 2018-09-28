---
title: 'Designdetails: Die Rolle des Minimalbestands | Microsoft Docs'
description: "Dieses Thema hebt die Wichtigkeit der Einstellung Minimalbed hervor, damit Sie wissen, wann Sie den Bestand erneuern müssen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: desigh, reorder, demand, supply
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a64d71ca9f163793c959126da09ffa4ef281b5e0
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-the-role-of-the-reorder-point"></a>Designdetails: Die Rolle des Minimalbestands
Zusätzlich zur allgemeinen Anpassung von Angebot und Nachfrage muss das Planungssystem auch Lagerbestände für die betroffenen Artikel überwachen, um die definierten Wiederbeschaffungsverfahren zu berücksichtigen.  
  
Ein Minimalbestand repräsentiert den Bedarf während der Beschaffungszeit. Wenn die Durchläufe des voraussichtlichen Lagerstatus unter den Lagerbestand gerät, der durch den Minimalbestand definiert ist, muss eine größere Menge bestellt werden. Unterdessen schrumpft der Lagerbestand erfahrungsgemäß schrittweise und erreicht wahrscheinlich den Punkt Null (oder den Sicherheitsbestand), bis der Vorrat aufgestockt wird.  
  
Entsprechend schlägt das Planungssystem einen vorwärtsgeplanten Beschaffungsauftrag an dem Zeitpunkt vor, an dem der geplante Bestand unter den Minimalbestand sinkt.  
  
Der Minimalbestand reflektiert einen bestimmten Lagerbestand. Allerdings können sich Lagerbestände während des Zeitrahmens erheblich ändern, daher muss das Planungssystem ständig den voraussichtlich verfügbaren Lagerbestand überwachen.  
  
## <a name="see-also"></a>Siehe auch  
[Designdetails: Wiederbeschaffungsverfahren](design-details-reordering-policies.md)   
[Designdetails: Planungsparameter](design-details-planning-parameters.md)   
[Designdetails: Umgang mit Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md)   
[Designdetails: Vorratsplanung](design-details-supply-planning.md)
