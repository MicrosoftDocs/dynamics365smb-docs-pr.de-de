---
title: 'Designdetails: Bedarf und Vorrat | Microsoft Docs'
description: Dieses Thema erläutert das Konzept der Nachfrage, welches der allgemeine Begriff ist für jede Art Brutto-Bedarf, wie beispielsweise für Verkaufsauftrags und Komponentenbedarf aus einem Fertigungsauftrag.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 23e941b3ab6fc8e2176268f38647630419453d23
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "933886"
---
# <a name="design-details-demand-and-supply"></a>Designdetails: Bedarf und Vorrat
Bedarf ist der Oberbegriff, der für jede Art Brutto-Bedarf verwendet wird, beispielsweise für Verkaufsauftrags und Komponentenbedarf aus einem Fertigungsauftrag. Darüber hinaus ermöglicht die Anwendung weitere technische Bedarfsarten, wie z.B. negative Lagerbestände und Einkaufsreklamationen.  
  
Vorrat ist der allgemeine Begriff für jede Art von positiver oder eingehender Menge, wie etwa Bestands-, Einkauf-, Montage-, Fertigungs- oder eingehende Umlagerungen. Darüber hinaus stellt möglicherweise eine Verkaufsreklamation ebenfalls einen Vorrat dar.  
  
Um die vielen Quellen von Nachfrage und Angebot zu sortieren, organisiert das Planungssystem sie auf zwei Zeitachsen, die Bestandsprofile genannt werden. Das eine Profil enthält Bedarfsereignisse und das andere enthält die entsprechenden Zubehörereignisse. Jedes Ereignis repräsentiert eine Auftragsnetzwerkeinheit, wie etwa eine Verkaufsauftragszeile, einen Artikelposten oder eine Fertigungsauftragszeile.  
  
Wenn Bestandsprofile geladen werden, werden die verschiedenen BBedarf-Vorrat-Sätze ausgeglichen, um einen Beschaffungsplan auszustellen, der die aufgeführten Ziele erfüllt.  
  
Planungsparameter und Lagerbestände sind andere Arten von Bedarf und Vorrat bzw. sind einem integrierten Ausgleich unterworfen, um den Lagerbestand wieder aufzufüllen. Weitere Informationen finden Sie unter [Designdetails: Behandlungs-Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md).  
  
## <a name="see-also"></a>Siehe auch  
[Designdetails: Ausgleich von Bedarf und Vorrat](design-details-balancing-demand-and-supply.md)   
[Designdetails: Zentrale Konzepte des Planungssystems](design-details-central-concepts-of-the-planning-system.md)   
[Designdetails: Vorratsplanung](design-details-supply-planning.md)