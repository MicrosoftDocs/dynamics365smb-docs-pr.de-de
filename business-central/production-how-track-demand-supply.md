---
title: 'Vorgehensweise: Titel-Beziehungen zwischen Bedarf und Vorrat | Microsoft Docs'
description: "Verfolgen des Auftragsbedarfs (Menge mit Bedarfsverursacher), der Absatzplanung, des Rahmenauftrags oder der Planungsparameter (Menge ohne Bedarfsverursacher), auf den bzw. auf die die betreffende Planungszeile zurückzuführen ist"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 2300cc6e3f4c429cd73a17939420a44b846a3b13
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="track-relations-between-demand-and-supply"></a>Nachverfolgen von Beziehungen zwischen Bedarf und Vorrat
Verfolgen des Auftragsbedarfs (Menge mit Bedarfsverursacher), der Absatzplanung, des Rahmenauftrags oder der Planungsparameter (Menge ohne Bedarfsverursacher), auf den bzw. auf die die betreffende Planungszeile zurückzuführen ist

Die Planungsvorschläge beinhalten zusätzliche Planungsinformationen wie  Nachverfolgung zu nicht auftragsbezogenen Entitäten und  Warnungen, um den Planer bei der Erstellung eines optimalen Beschaffungsplans zu unterstützen. Weitere Informationen zu Planungsüberschuss ohne Bedarfsverursacher finden Sie unter  Planungselement ohne Bedarfsverursacher.

## <a name="to-track-linked-items"></a>Um verknüpfte Artikel zu verfolgen
Die Verfolgung zeigt, wie Verkaufsaufträge, Fertigungsaufträge und Bestellungen über Reservierungen mit einem Fertigungsauftrag verbunden sind.

Nachfolgend wird erläutert, wie Artikel für einen fest geplanten Fertigungsauftrag verfolgt werden. Die Schritte sind für alle anderen Auftragsarten und der Planungsvorschlagszeilen ähnlich.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Fest geplante Produktionsauftrag** ein, und wählen dann den zugehörigen Link aus.
2. Öffnen Sie den relevanten fest geplanten Fertigungsauftrag in der Liste.
3. Wählen Sie im Inforegister **Zeilen** in Aktionen **Funktion** aus, und wählen Sie dann **Auftrag-Verfolgung**.

In den Zeilen im Fenster  **Auftragsverfolgung**werden die Dokumente angezeigt, die sich auf die aktuelle Fertigungsauftragszeile beziehen.

## <a name="untracked-planning-elements"></a>Planungselemente ohne Bedarfsverursacher
Das Fenster **Planungselemente ohne Bedarfsverursacher** öffnet sich, wenn Sie das Feld **Mge. ohne Bedarfsverursacher** im Fenster **Auftragsplanung** auswählen. Er dient beiden Zwecken:

1. Sie enthält Informationen zu Mengen ohne Bedarfsverursacher, die angezeigt werden, wenn der Benutzer im Fenster "Bedarfsverursacher" Mengen ohne Bedarfsverursacher aufruft.
2. Sie enthält Warnmeldungen, die angezeigt werden, wenn der Benutzer im **Planungsvorschlag** auf ein **Warnungs**symbol klickt.

Die Tabelle enthält Posten, die eine Überschussmenge ohne Bedarfsverursacher im Bedarfsverursachernetzwerk ausweisen. Diese Posten werden während der Planung erzeugt und zeigen die Herkunft der Überschussmenge ohne Bedarfsverursacher in den Bedarfsverursacherzeilen. Die folgende Herkunft ist für den Überschuss ohne Bedarfsverursacher möglich:

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
[Lagerbest](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Designdetails: Reservierung, Auftragsnachverfolgung und Aktionsmeldungen](design-details-reservation-order-tracking-and-action-messaging.md)  
[Designdetails: Vorratsplanung](design-details-supply-planning.md)   
[Bewährte Einrichtungsmethoden: Beschaffungsplanung](setup-best-practices-supply-planning.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

