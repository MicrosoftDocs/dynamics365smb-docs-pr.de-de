---
title: "Designdetails: Verfügbarkeit im Lager | Microsoft Docs"
description: "Die Anwendung muss eine konstante Kontrolle der Artikelverfügbarkeit im Lager aufrechterhalten, sodass ausgehende Aufträge effizient verlaufen und optimale Lieferungen zur Verfügung stellen können."
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
ms.openlocfilehash: 698404dab1b3888d073eb3c23268d3b009a4f577
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-availability-in-the-warehouse"></a>Designdetails: Verfügbarkeit im Lager
Die Anwendung muss eine konstante Kontrolle der Artikelverfügbarkeit im Lager aufrechterhalten, sodass ausgehende Aufträge effizient verlaufen und optimale Lieferungen zur Verfügung stellen können.  

 Die Verfügbarkeit variiert je nach Zuordnungen auf Lagerplatzebene, wenn Lageraktivitäten wie Kommissionierungen und Lagerplatzumlagerungen auftreten, und wenn das Bestandsreservierungssystem Einschränkungen erforderlich macht, die einzuhalten sind. Ein komplexer Algorithmus prüft, ob alle Bedingungen erfüllt sind, bevor Mengen auf Kommissionierungen für ausgehende Ströme zugewiesen werden.  

## <a name="bin-content-and-reservations"></a>Lagerplatzinhalt und Reservierungen  
 In jeder Installation von NAV-Logistik sind Artikelmengen als Lagerplatzposten, im Logistikbereich, und als Artikelposten, im Anwendungsbereich Lager, vorhanden. Diese beiden Postenarten enthalten verschiedene Informationen darüber, wo Artikel vorhanden sind und ob sie verfügbar sind. Lagerplatzposten definieren die Verfügbarkeit eines Artikels nach Lagerplatz und Lagerplatzart, was als Lagerplatzinhalt bezeichnet wird. Artikelposten definieren die Verfügbarkeit eines Artikels durch ihre Reservierung auf ausgehenden Belegen.  

 Spezielle Funktionen sind im Kommissionierungsalgorithmus vorhanden, um die Menge zu berechnen, die zur Kommissionierung verfügbar ist, wenn Lagerplatzinhalt mit Reservierungen verknüpft ist.  

## <a name="quantity-available-to-pick"></a>Verfügbare Menge für Kommissionierung  
 Wenn, zum Beispiel, der Entnahmealgorithmus nicht Artikelmengen berücksichtigt, die für eine offene Verkaufsauftragslieferung reserviert sind, dann werden diejenigen Artikel für einen anderen Verkaufsauftrag kommissioniert, der zuvor ausgeliefert wurde, wodurch der erste Verkauf verhindert wird. Um diese Situation zu vermeiden, zieht der Entnahmealgorithmus Mengen, die für andere ausgehende Belege reserviert sind, Mengen auf bestehenden Kommissionierbelegen und Mengen, die kommissioniert, aber noch nicht geliefert oder verbraucht wurden, ab.  

 Das Ergebnis wird im Feld **Verfügbare Menge** im Fenster **Kommissioniervorschlag** angezeigt, in dem das Feld dynamisch berechnet wird. Der Wert wird auch berechnet, wenn Benutzer Kommissionierungen direkt für ausgehende Belege erstellen. Solche ausgehenden Belege können Verkaufsaufträge, Fertigungsverbrauch oder ausgehende Umlagerungen sein, bei denen das Ergebnis in den entsprechenden Mengenfeldern reflektiert wird, wie etwa **Verfügbare Menge.**  

> [!NOTE]  
>  Hinsichtlich der Priorität von Reservierungen wird die zu reserviere Menge von der Menge abgezogen, die für die Kommissionierung verfügbar ist. Wenn beispielsweise die Menge, die an den Kommissionierlagerplätzen verfügbar ist, 5 Einheiten ist,sich jedoch 100 Einheiten an Einlagerungslagerplätzen befinden, wird, wenn Sie versuchen, mehr als 5 Einheiten für einen anderen Auftrag zu reservieren, eine Fehlermeldung angezeigt, da die zusätzliche Menge an den Kommissionierlagerplätzen verfügbar sein muss.  

### <a name="calculating-the-quantity-available-to-pick"></a>Berechnen der zur Kommissionierung verfügbaren Menge  
 Die zur Kommissionierung verfügbare Menge wird wie folgt berechnet:  

 Verfügbare Menge für Kommissionierung = Menge in Kommissionierlagerplätzen - Menge in Kommissionierungen und Lagerplatzumlagerungen - (reservierte Menge in Kommissionierlagerplätzen + reservierte Menge in Kommissionierungen und Lagerplatzumlagerungen)  

 Das folgende Diagramm zeigt die verschiedenen Elemente der Berechnung an.  

 ![Verfügbar, mit Reservierungsüberschneidung auswählen](media/design_details_warehouse_management_availability_2.png "design_details_warehouse_management_availability_2")  

## <a name="quantity-available-to-reserve"></a>&Menge Verfügbar für Reservierung  
 Da die Konzepte des Lagerplatzinhaltes und der Reservierung gleichzeitig existieren, muss die Menge der Artikel, die zur Reservierung verfügbar sind, an die Zuordnung zu ausgehenden Lagerbelegen angepasst sein.  

 Eine Reservierung aller Artikel im Lager sollte mögich sein außer bei jenen, deren ausgehende Verabeitung bereits begonnen hat. Entsprechend wird die Menge, die reservierbar ist, als die Menge auf allen Belegen und an allen Lagerplatzarten definiert, ausgenommen die folgenden ausgehenden Mengen:  

-   Menge für nicht registrierte Kommissionierbelege  
-   Menge der in Lieferung enthaltenen Lagerplätze  
-   Menge in Fert.-Bereitst.-Lagerplatzcodes  
-   Menge in Off. Fert.-Ber.-Lagerpl.  
-   Menge in Mont.-Bereitst.-Lagerplätzen  
-   Menge in Ausgleichslagerplätzen  

 Das Ergebnis wird im Feld **Verfügbare Gesamtmenge** im Fenster **Reservierungen** angezeigt.  

 In einer Reservierungszeile wird die Menge, die nicht reserviert werden kann, da sie im Lager zugeordnet wird, im Feld **Zugewiesene Menge im Lager** im Fenster **Reservierungen** angezeigt.  

### <a name="calculating-the-quantity-available-to-reserve"></a>Berechnen der zur Reservierung verfügbaren Menge  
 Die zur Reservierung verfügbare Menge wird wie folgt berechnet:  

 Zur Reservierung verfügbare Menge = Gesamtmenge im Lagerbestand - Menge in Kommissionierungen und Lagerplatzumlagerungen für Herkunftsbelege - Reservierte menge - Menge in Ausgangslagerplätzen  

 Das folgende Diagramm zeigt die verschiedenen Elemente der Berechnung an.  

 ![Für Reservierung pro Lagerhauszuweisung verfügbar](media/design_details_warehouse_management_availability_3.png "design_details_warehouse_management_availability_3")  

## <a name="see-also"></a>Siehe auch  
 [Designdetails: Logistik](design-details-warehouse-management.md)

