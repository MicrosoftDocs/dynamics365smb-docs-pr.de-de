---
title: 'Designdetails: Die Rolle des Minimalbestands | Microsoft Docs'
description: Dieses Thema hebt die Wichtigkeit der Einstellung Minimalbed hervor, damit Sie wissen, wann Sie den Bestand erneuern müssen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: desigh, reorder, demand, supply
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 760bc475be2606e9bc4d72f09ae76e794418d904
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306748"
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
