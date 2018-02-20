---
title: 'Designdetails: Bedarf und Vorrat | Microsoft Docs'
description: "Wenn die Zubehör-Ausgleichsverfahren ausgeführt wurden, gibt es drei mögliche Schlusssituationen."
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
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: f682e2fdaa5be20ae8e6f3ff6ee2ff4769b48545
ms.contentlocale: de-de
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-closing-demand-and-supply"></a>Designdetails: Abschluss von Bedarf und Vorrat
Wenn die Zubehör-Ausgleichsverfahren ausgeführt wurden, gibt es drei mögliche Schlusssituationen:  

-   Die benötigte Menge und das Datum der Bedarfsereignisse wurden erfüllt, und die Planung für den Artikel kann geschlossen werden. Das Vorratsereignis ist noch offen und kann möglicherweise den nächsten Bedarf decken, der Ausgleichsvorgang kann daher erneut mit dem aktuellen Vorratsereignis und dem nächsten Bedarf starten.  

-   Der Beschaffungsauftrag kann nicht geändert werden, um den gesamten Bedarf zu decken. Das Bedarfsereignis ist noch offen, mit einigen nicht abgedeckten Mengen, die möglicherweise vom nächsten Bedarfsereignis abgedeckt werden. Daher wird das aktuelle Vorratsereignis geschlossen, sodass der Ausgleichsvorgang mit dem aktuellen Bedarfs- und dem nächsten Vorratsereignis erneut beginnen kann.  

-   Der gesamte Bedarf ist abgedeckt; es gibt keinen folgenden Bedarf (oder es gab überhaupt keinen Bedarf). Wenn überschüssiger Vorrat vorhanden ist, kann dieser vermindert (oder storniert) und dann geschlossen werden. Es ist möglich, dass zusätzliche Zubehörereignisse weiter entlang der Kette vorhanden sind, und diese sollten ebenfalls annulliert werden.  

 Schließlich erstellt das Planungssystem ein Auftragsnachverfolgungslink zwischen dem Vorrat und dem Bedarf.  

## <a name="creating-the-planning-line-suggested-action"></a>Die Planungszeile (vorgeschlagene Aktion) erstellen  
 Wenn eine Aktion – Neu, Menge ändern, Neuplanen, Neuplanen und Menge ändern oder Stornieren – für die Revision des Beschaffungsauftrags vorgeschlagen wird, erstellt das Planungssystem, eine Planung auf dem Planungsvorschlag. Aufgrund der Auftragsnachverfolgung wird die Planungszeile nicht nur erstellt, wenn das Vorratsereignis geschlossen wird, sondern auch, wenn das Nachfrageereignis geschlossen wird, auch wenn das Vorratsereignis möglicherweise noch offen und abhängig von zusätzlichen Änderungen ist, wenn das nächste Nachfrageereignis verarbeitet wird. Dies bedeutet, dass die Planungszeile, wenn sie zuerst erstellt wird, möglicherweise erneut geändert wird.  

 Um Datenbankzugriff zu minimieren, wenn Sie Fertigungsaufträge bearbeiten, können Sie die Planungszeile in drei Ebenen verwalten, mit dem Ziel, das am wenigsten anspruchsvolle Bestanderhaltungsniveau auszuführen:  

-   Erstellen Sie nur die Planungszeile mit dem aktuellen Fälligkeitsdatum und der Menge, aber ohne Arbeitsplan und Komponenten.  

-   Arbeitsplan einschließen: Der geplante Arbeitsplan wird einschließlich Berechnung des Start- und Enddatum und -Zeiten ausgebreitet. Dieses ist anspruchvoll in Bezug auf Datenbankzugriffe. Um das End- und die Fälligkeitsdatum zu bestimmen, kann es notwendig sein, dies zu berechnen, auch wenn das Vorratsereignis nicht abgeschlossen wurde (im Fall der Vorwärtsterminierung).  

-   Strukturstückliste einschließen: Dies kann warten bis kurz vor dem Abschluss des Vorratsereignisses.  

 Damit sind die Beschreibungen dazu, wie Bedarf und Vorrat vom Planungssystem geladen, priorisiert und ausgeglichen werden, abgeschlossen. In der Integration mit dieser Beschaffungsplanungsaktivität muss das System sicherstellen, dass der erforderliche Lagerbestand jedes geplanten Artikels entsprechend den jeweiligen Wiederbeschaffungsverfahren verwaltet wird.  

## <a name="see-also"></a>Siehe auch  
 [Designdetails: Ausgleich von Bedarf und Vorrat](design-details-balancing-demand-and-supply.md)   
 [Designdetails: Zentrale Konzepte des Planungssystems](design-details-central-concepts-of-the-planning-system.md)   
 [Designdetails: Vorratsplanung](design-details-supply-planning.md)

