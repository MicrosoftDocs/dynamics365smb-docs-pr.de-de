---
title: 'Designdetails: Verfügbarkeit im Lager | Microsoft Docs'
description: Die Anwendung muss eine konstante Kontrolle der Artikelverfügbarkeit im Lager aufrechterhalten, sodass ausgehende Aufträge effizient verlaufen und optimale Lieferungen zur Verfügung stellen können.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 10eb4e51a90437d847d01fdbf577adba8c8275eb
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3185756"
---
# <a name="design-details-availability-in-the-warehouse"></a>Designdetails: Verfügbarkeit im Lager
Die Anwendung muss eine konstante Kontrolle der Artikelverfügbarkeit im Lager aufrechterhalten, sodass ausgehende Aufträge effizient verlaufen und optimale Lieferungen zur Verfügung stellen können.  

Die Verfügbarkeit variiert je nach Zuordnungen auf Lagerplatzebene, wenn Lageraktivitäten wie Kommissionierungen und Lagerplatzumlagerungen auftreten, und wenn das Bestandsreservierungssystem Einschränkungen erforderlich macht, die einzuhalten sind. Ein komplexer Algorithmus prüft, ob alle Bedingungen erfüllt sind, bevor Mengen auf Kommissionierungen für ausgehende Ströme zugewiesen werden.

Wenn eine oder mehrere Bedingungen nicht erfüllt werden, können verschiedene Fehlermeldungen, einschließlich der generischen Meldung "Nichts zu behandeln" angezeigt werden. Meldung. Die "Nichts zu behandeln" Meldung kann für viele verschiedenen Ursachen, in den eingehenden und ausgehenden Flüssen auftreten, in denen eine direkt oder indirekt betroffene Belegzeile das Feld **Menge. zu behandeln** enthält.

> [!NOTE]
> Informationen werden in Kürze hier über mögliche Ursachen und Lösungen veröffentlicht, dass das "nichts zu behandeln" umfasst. Nachricht

## <a name="bin-content-and-reservations"></a>Lagerplatzinhalt und Reservierungen  
 In jeder Installation von NAV-Logistik sind Artikelmengen als Lagerplatzposten, im Logistikbereich, und als Artikelposten, im Anwendungsbereich Lager, vorhanden. Diese beiden Postenarten enthalten verschiedene Informationen darüber, wo Artikel vorhanden sind und ob sie verfügbar sind. Lagerplatzposten definieren die Verfügbarkeit eines Artikels nach Lagerplatz und Lagerplatzart, was als Lagerplatzinhalt bezeichnet wird. Artikelposten definieren die Verfügbarkeit eines Artikels durch ihre Reservierung auf ausgehenden Belegen.  

 Spezielle Funktionen sind im Kommissionierungsalgorithmus vorhanden, um die Menge zu berechnen, die zur Kommissionierung verfügbar ist, wenn Lagerplatzinhalt mit Reservierungen verknüpft ist.  

## <a name="quantity-available-to-pick"></a>Verfügbare Menge für Kommissionierung  
 Wenn, zum Beispiel, der Entnahmealgorithmus nicht Artikelmengen berücksichtigt, die für eine offene Verkaufsauftragslieferung reserviert sind, dann werden diejenigen Artikel für einen anderen Verkaufsauftrag kommissioniert, der zuvor ausgeliefert wurde, wodurch der erste Verkauf verhindert wird. Um diese Situation zu vermeiden, zieht der Entnahmealgorithmus Mengen, die für andere ausgehende Belege reserviert sind, Mengen auf bestehenden Kommissionierbelegen und Mengen, die kommissioniert, aber noch nicht geliefert oder verbraucht wurden, ab.  

 Das Ergebnis wird im Feld **Verfügbare Menge** auf der Seite **Kommissioniervorschlag** angezeigt, in dem das Feld dynamisch berechnet wird. Der Wert wird auch berechnet, wenn Benutzer Kommissionierungen direkt für ausgehende Belege erstellen. Solche ausgehenden Belege können Verkaufsaufträge, Fertigungsverbrauch oder ausgehende Umlagerungen sein, bei denen das Ergebnis in den entsprechenden Mengenfeldern reflektiert wird, wie etwa **Verfügbare Menge.**  

> [!NOTE]  
>  Hinsichtlich der Priorität von Reservierungen wird die zu reserviere Menge von der Menge abgezogen, die für die Kommissionierung verfügbar ist. Wenn beispielsweise die Menge, die an den Kommissionierlagerplätzen verfügbar ist, 5 Einheiten ist,sich jedoch 100 Einheiten an Einlagerungslagerplätzen befinden, wird, wenn Sie versuchen, mehr als 5 Einheiten für einen anderen Auftrag zu reservieren, eine Fehlermeldung angezeigt, da die zusätzliche Menge an den Kommissionierlagerplätzen verfügbar sein muss.  

### <a name="calculating-the-quantity-available-to-pick"></a>Berechnen der zur Kommissionierung verfügbaren Menge  
 Die zur Kommissionierung verfügbare Menge wird wie folgt berechnet:  

 Verfügbare Menge für Kommissionierung = Menge in Kommissionierlagerplätzen - Menge in Kommissionierungen und Lagerplatzumlagerungen - (reservierte Menge in Kommissionierlagerplätzen + reservierte Menge in Kommissionierungen und Lagerplatzumlagerungen)  

 Das folgende Diagramm zeigt die verschiedenen Elemente der Berechnung an.  

 ![Verfügbar zur Entnahme mit Reservierungsüberschneidung](media/design_details_warehouse_management_availability_2.png "Verfügbar zur Entnahme mit Reservierungsüberschneidung")  

## <a name="quantity-available-to-reserve"></a>&Menge Verfügbar für Reservierung  
 Da die Konzepte des Lagerplatzinhaltes und der Reservierung gleichzeitig existieren, muss die Menge der Artikel, die zur Reservierung verfügbar sind, an die Zuordnung zu ausgehenden Lagerbelegen angepasst sein.  

 Eine Reservierung aller Artikel im Lager sollte mögich sein außer bei jenen, deren ausgehende Verabeitung bereits begonnen hat. Entsprechend wird die Menge, die reservierbar ist, als die Menge auf allen Belegen und an allen Lagerplatzarten definiert, ausgenommen die folgenden ausgehenden Mengen:  

-   Menge für nicht registrierte Kommissionierbelege  
-   Menge der in Lieferung enthaltenen Lagerplätze  
-   Menge in Fert.-Bereitst.-Lagerplatzcodes  
-   Menge in Off. Fert.-Ber.-Lagerpl.  
-   Menge in Mont.-Bereitst.-Lagerplätzen  
-   Menge in Ausgleichslagerplätzen  

 Das Ergebnis wird im Feld **Verfügbare Gesamtmenge** auf der Seite **Reservierungen** angezeigt.  

 In einer Reservierungszeile wird die Menge, die nicht reserviert werden kann, da sie im Lager zugeordnet wird, im Feld **Zugewiesene Menge im Lager** auf der Seite **Reservierungen** angezeigt.  

### <a name="calculating-the-quantity-available-to-reserve"></a>Berechnen der zur Reservierung verfügbaren Menge  
 Die zur Reservierung verfügbare Menge wird wie folgt berechnet:  

 Zur Reservierung verfügbare Menge = Gesamtmenge im Lagerbestand - Menge in Kommissionierungen und Lagerplatzumlagerungen für Herkunftsbelege - Reservierte menge - Menge in Ausgangslagerplätzen  

 Das folgende Diagramm zeigt die verschiedenen Elemente der Berechnung an.  

 ![Verfügbar, um pro Lagerzuordnung zu reservieren](media/design_details_warehouse_management_availability_3.png "Verfügbar, um pro Lagerzuordnung zu reservieren")  

## <a name="see-also"></a>Siehe auch  
 [Designdetails: Lagerverwaltung](design-details-warehouse-management.md)  
 [Artikelverfügbarkeit anzeigen](inventory-how-availability-overview.md)
