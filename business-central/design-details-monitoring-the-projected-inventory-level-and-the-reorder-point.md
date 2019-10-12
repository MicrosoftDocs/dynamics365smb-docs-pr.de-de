---
title: 'Designdetails: Überwachen der Ebene des voraussichtlichen Lagerbestands und des Minimalbestands | Microsoft Docs'
description: Erfahren, wie Lagerplanung voraussichtlichem zwischen voraussichtlichen Lagerbestand und voraussichtlich verfügbaren Lagerbestandebenen unterscheidet.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, supply, inventory, planning
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 3ae50295fd77de376ac25f2f2e267b765e5de58e
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307012"
---
# <a name="design-details-monitoring-the-projected-inventory-level-and-the-reorder-point"></a>Designdetails: Überwachen der voraussichtlichen Lagerebene und des Minimalbestands
Der Bestand ist eine Art Vorrat, jedoch für Bestandsplanung unterscheidet das Planungssystem zwischen zwei Bestandsebenen:  

* Voraussichtlicher Lagerbestand  
* Voraussichtlich verfügbarer Lagerbestand  

## <a name="projected-inventory"></a>Voraussichtlicher Lagerbestand  
Zuerst ist der voraussichtliche Lagerbestand die Menge des Bruttobestands, einschließlich Vorrat und Bedarf in der Vergangenheit (selbst wenn nicht gebucht), wenn der Planungsprozess gestartet wird. Zukünftig wird dies eine bewegliche Ebene des voraussichtlichen Bestands sein, die durch Brutto-Mengen aus künftigem Vorrat und Bedarf verwaltet wird, da diese entlang der Zeitachse eingeführt werden (ob reserviert oder auf andere Weise zugewiesen).  

Der voraussichtliche Lagerbestand wird vom Planungssystem verwendet, um den Minimalbestand zu überwachen und um die Wiederbeschaffungsmenge zu bestimmen, wenn die Wiederbeschaffungsrichtlinie „Höchstmenge“ verwendet wird.  

## <a name="projected-available-inventory"></a>Voraussichtlich verfügbarer Lagerbestand  
Der voraussichtlich verfügbare Lagerbestand ist Teil des voraussichtlichen Bestands, der zu einem bestimmten Zeitpunkt verfügbar ist, um Bedarf zu erfüllen. Der voraussichtlich verfügbare Lagerbestand wird vom Planungsmodul verwendet, wenn die Sicherheitsbestandsebene überwacht wird.  

Der voraussichtlich verfügbare Lagerbestand wird vom Planungssystem verwendet, um die Sicherheitsbestandsebene zu überwachen, da der Sicherheitsbestand immer verfügbar sein muss, um unerwarteten Bedarf zu erfüllen.  

## <a name="time-buckets"></a>Zeitrahmen  
Eine strenge Kontrolle des voraussichtlichen Lagerbestands ist entscheidend, um zu ermitteln, wann der Minimalbestand erreicht ist oder unterschritten wurde, und wie die richtige Auftragsmenge berechnet wird, wenn das Wiederbeschaffungsverfahren „Höchstmenge“ verwendet wird.  

Wie zuvor angegeben, wird der voraussichtliche Lagerbestand am Anfang der Planungsperiode berechnet. Dies ist eine grobe Ebene, bei der Reservierungen und ähnliche Zuordnungen nicht berücksichtigt werden. Um dieses Lagerbestandsniveau während der Planungssequenz zu überwachen, überwacht das System die aggregierten Änderungen über eine Zeitperiode, einen Zeitrahmen hinweg. Die Anwendung stellt sicher, dass der Zeitrahmen mindestens ein Tag ist, da dies die präziseste Zeiteinheit für ein Bedarfs- oder ein Vorratsereignis ist.  

## <a name="determining-the-projected-inventory-level"></a>Bestimmen des voraussichtlichen Lagerbestands  
Die folgende Sequenz beschreibt, wie der voraussichtliche Lagerbestand bestimmt wird:  

* Wenn ein Vorratsereignis, wie eine Bestellung, vollständig geplant wurde, erhöht es den voraussichtlichen Lagerbestand am Fälligkeitsdatum.  
* Wenn ein Nachfrageereignis vollständig erfüllt wurde, verringert es nicht sofort den voraussichtlichen Lagerbestand. Stattdessen bucht es eine Minderungserinnerung, die ein interner Datensatz ist, der das Datum und die Menge des Beitrags zum voraussichtlichen Lagerbestand beinhaltet.  
* Wenn ein folgendes Vorratsereignis auf die Zeitachse geplant und auf die Zeitachse platziert wird, werden die gebuchten Abgangsmahnungen beim Aktualisieren des voraussichtlichen Lagerstatus einzeln bis zum geplanten Datum der Lieferung überprüft. Während dieses Prozesses kann der Minimalbestand der internen Zunahmeerinnerung erreicht oder unterschritten werden.  
* Wenn ein neuer Beschaffungsauftrag eingegeben wird, prüft die Anwendung, ob dieser vor dem aktuellen Vorrat eingegeben wird. Wenn dies der Fall ist, wird der neue Vorrat zum aktuellen Vorrat, und der Ausgleichsvorgang beginnt erneut.  

Nachfolgend wird eine graphische Illustration dieses Prinzips gezeigt:  

![Die voraussichtliche Lagerstatusebene bestimmen](media/nav_app_supply_planning_2_projected_inventory.png "Die voraussichtliche Lagerstatusebene bestimmen")  

1. Vorrat **Sa** von 4 (fest) schließt Bedarf **Da** von -3.  
2. CloseDemand: Erstellen Sie eine Minderungserinnerung von -3 (nicht angezeigt).  
3. Vorrat **Sa** wird mit einem Überschuss von 1 geschlossen (kein Bedarf mehr vorhanden).  

     Dadurch wird der voraussichtliche Lagerbestand auf +4 angehoben, während der voraussichtliche **verfügbare** Lagferbestand -1 wird.  

4. Der nächste Vorrat **Sb** von 2 (ein anderer Auftrag) wurdet bereits in die Zeitachse platziert.  
5. Das System prüft, ob es eine Minderungserinnerung gibt, die **Sb** vorangeht (dies ist nicht der Fall, daher keine Aktion).  
6. Das System schließt Vorrat **Sb** (kein Bedarf mehr vorhanden) - entweder A: durch Reduzierung auf 0 (Stornieren) oder B: durch unverändert lassen.  

     Dadurch wird der voraussichtliche Lagerbestand erhöht (A: +0 => +4 oder B: +2 = +6).  

7. Das System führt eine abschließende Prüfung durch: Gibt es eine Minderungserinnerung? Ja, es gibt eine am Datum **Da**  
8. Die Anwendung fügt die Minderungserinnerung -3 in der Ebene des voraussichtlichen Lagerbestands hinzu, entweder A: +4 -3 = 1 oder B: +6 -3 = +3.  
9. Im Falle von A erstellt das System eine vorausplanende Bestellung ab Datum **Da**.  

     Im Falle von B wird der Minimalbestand erreicht, und es wird ein neuer Auftrag erstellt.  

## <a name="see-also"></a>Siehe auch  
[Designdetails: Wiederbeschaffungsverfahren](design-details-reordering-policies.md)   
[Designdetails: Planungsparameter](design-details-planning-parameters.md)   
[Designdetails: Umgang mit Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md)   
[Designdetails: Vorratsplanung](design-details-supply-planning.md)
