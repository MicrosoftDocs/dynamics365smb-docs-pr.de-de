---
title: 'Vorgehensweise: Titel-Beziehungen zwischen Bedarf und Vorrat | Microsoft Docs'
description: Verfolgen des Auftragsbedarfs (Menge mit Bedarfsverursacher), der Absatzplanung, des Rahmenauftrags oder der Planungsparameter (Menge ohne Bedarfsverursacher), auf den bzw. auf die die betreffende Planungszeile zurückzuführen ist
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: beb438be379cfc6e3f239ebb0ae270a2e957651c
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1252803"
---
# <a name="track-relations-between-demand-and-supply"></a>Nachverfolgen von Beziehungen zwischen Bedarf und Vorrat
Verfolgen des Auftragsbedarfs (Menge mit Bedarfsverursacher), der Absatzplanung, des Rahmenauftrags oder der Planungsparameter (Menge ohne Bedarfsverursacher), auf den bzw. auf die die betreffende Planungszeile zurückzuführen ist

Die Planungsvorschläge beinhalten zusätzliche Planungsinformationen wie  Nachverfolgung zu nicht auftragsbezogenen Entitäten und  Warnungen, um den Planer bei der Erstellung eines optimalen Beschaffungsplans zu unterstützen. Weitere Informationen finden Sie unter [Planungselement ohne Bedarfsverursacher](production-how-track-demand-supply.md#untracked-planning-elements).

## <a name="to-track-linked-items"></a>Um verknüpfte Artikel zu verfolgen
Die Verfolgung zeigt, wie Verkaufsaufträge, Fertigungsaufträge und Bestellungen über Reservierungen mit einem Fertigungsauftrag verbunden sind.

Nachfolgend wird erläutert, wie Artikel für einen fest geplanten Fertigungsauftrag verfolgt werden. Die Schritte sind für alle anderen Auftragsarten und der Planungsvorschlagszeilen ähnlich.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Fest geplante Produktionsauftrag** ein, und wählen dann den zugehörigen Link aus.
2. Öffnen Sie den relevanten fest geplanten Fertigungsauftrag in der Liste.
3. Wählen Sie im Inforegister **Zeilen** in Aktionen **Funktion** aus, und wählen Sie dann **Auftrag-Verfolgung**.

In den Zeilen im Fenster  **Auftragsverfolgung**werden die Dokumente angezeigt, die sich auf die aktuelle Fertigungsauftragszeile beziehen.

## <a name="untracked-planning-elements"></a>Planungselemente ohne Bedarfsverursacher
Die Seite**Planungselemente ohne Bedarfsverursacher** öffnet sich, wenn Sie das Feld **Mge. ohne Bedarfsverursacher** auf der Seite **Auftragsplanung** auswählen. Er dient beiden Zwecken:

1. Sie enthält Informationen zu Mengen ohne Bedarfsverursacher, die angezeigt werden, wenn der Benutzer auf der Seite "Bedarfsverursacher" Mengen ohne Bedarfsverursacher aufruft.
2. Sie enthält Warnmeldungen, die angezeigt werden, wenn der Benutzer auf der Seite **Planungsvorschlag** auf ein **Warnungs**-Symbol klickt.

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
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
