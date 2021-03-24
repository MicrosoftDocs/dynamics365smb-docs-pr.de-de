---
title: 'Vorgehensweise: Titel-Beziehungen zwischen Bedarf und Vorrat | Microsoft Docs'
description: Verfolgen des Auftragsbedarfs (Menge mit Bedarfsverursacher), der Absatzplanung, des Rahmenauftrags oder der Planungsparameter (Menge ohne Bedarfsverursacher), auf den bzw. auf die die betreffende Planungszeile zurückzuführen ist
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7ba774a7f7ba93c132e10e19f61b7df9cf825e7a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383225"
---
# <a name="track-relations-between-demand-and-supply"></a>Nachverfolgen von Beziehungen zwischen Bedarf und Vorrat
Verfolgen des Auftragsbedarfs (Menge mit Bedarfsverursacher), der Absatzplanung, des Rahmenauftrags oder der Planungsparameter (Menge ohne Bedarfsverursacher), auf den bzw. auf die die betreffende Planungszeile zurückzuführen ist

Die Planungsarbeitsblätter beinhalten zusätzliche Planungsinformationen wie Nachverfolgung zu nicht auftragsbezogenen Entitäten und Warnungen, um den Planer bei der Erstellung eines optimalen Beschaffungsplans zu unterstützen. Weitere Informationen finden Sie unter [Planungselement ohne Bedarfsverursacher](production-how-track-demand-supply.md#untracked-planning-elements).

## <a name="to-track-linked-items"></a>Um verknüpfte Artikel zu verfolgen
Die Verfolgung zeigt, wie Verkaufsaufträge, Fertigungsaufträge und Bestellungen über Reservierungen mit einem Fertigungsauftrag verbunden sind.

Nachfolgend wird erläutert, wie Artikel für einen fest geplanten Fertigungsauftrag verfolgt werden. Die Schritte sind für alle anderen Auftragsarten und der Planungsarbeitsblattszeilen ähnlich.

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Fester geplanter Fertigungsauftrag** ein, und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie den relevanten fest geplanten Fertigungsauftrag in der Liste.
3. Wählen Sie im Inforegister **Zeilen** in Aktionen **Funktion** aus, und wählen Sie dann **Auftrag-Verfolgung**.

In den Zeilen im Fenster **Auftragsverfolgung** werden die Dokumente angezeigt, die sich auf die aktuelle Fertigungsauftragszeile beziehen.

## <a name="untracked-planning-elements"></a>Planungselemente ohne Bedarfsverursacher
Die Seite **Planungselemente ohne Bedarfsverursacher** öffnet sich, wenn Sie das Feld **Mge. ohne Bedarfsverursacher** auf der Seite **Auftragsplanung** auswählen. Er dient beiden Zwecken:

1. Sie enthält Informationen zu Mengen ohne Bedarfsverursacher, die angezeigt werden, wenn der Benutzer auf der Seite "Bedarfsverursacher" Mengen ohne Bedarfsverursacher aufruft.
2. Sie enthält Warnmeldungen, die angezeigt werden, wenn der Benutzer auf der Seite **Planungsarbeitsblatt** auf ein **Warnungs**-Symbol klickt.

Die Seite enthält Posten, die eine Überschussmenge ohne Bedarfsverursacher im Bedarfsverursachernetzwerk ausweisen. Diese Posten werden während der Planung erzeugt und zeigen die Herkunft der Überschussmenge ohne Bedarfsverursacher in den Bedarfsverursacherzeilen. Die folgende Herkunft ist für den Überschuss ohne Bedarfsverursacher möglich:

- Absatzplanung
- Rahmenbestellungen
- Sicherheitsbestand
- Minimalbestand
- Maximalbestand
- Bestellmenge
- Maximale Losgröße
- Minimale Losgröße
- Losgrößenrundungsfaktor
- Toleranz (% der Losgröße)

## <a name="see-also"></a>Siehe auch  
[Planung](production-planning.md)   
[Produktion einrichten](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagerbestand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Designdetails: Reservierung, Auftragsnachverfolgung und Aktionsmeldungen](design-details-reservation-order-tracking-and-action-messaging.md)  
[Designdetails: Vorratsplanung](design-details-supply-planning.md)   
[Bewährte Einrichtungsmethoden: Beschaffungsplanung](setup-best-practices-supply-planning.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]