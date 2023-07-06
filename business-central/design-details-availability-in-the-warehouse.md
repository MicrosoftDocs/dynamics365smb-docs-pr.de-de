---
title: Designdetails - Verfügbarkeit im Lager
description: 'Erfahren Sie mehr über die verschiedenen Faktoren, die die Artikelverfügbarkeit in Ihrem Lager beeinflussen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
---
# <a name="design-details-availability-in-the-warehouse"></a><a name="design-details-availability-in-the-warehouse"></a><a name="design-details-availability-in-the-warehouse"></a>Designdetails: Verfügbarkeit im Lager

Behalten Sie die Artikelverfügbarkeit im Auge, um sicherzustellen, dass ausgehende Bestellungen effizient ablaufen und Ihre Lieferzeiten optimal sind.  

Verfügbarkeit kann abhängig von verschiedenen Faktoren variieren. Beispiel:

* Zuordnungen auf Lagerplatzebene, wenn Lageraktivitäten wie Kommissionierungen und Umlagerungen stattfinden.
* Wenn das Bestandsreservierungssystem Beschränkungen auferlegt, die eingehalten werden müssen.

Bevor Mengen auf Kommissionierungen für ausgehende Ströme zugewiesen werden, prüft [!INCLUDE [prod_short](includes/prod_short.md)], dass alle Bedingungen erfüllt sind.

Wenn die Bedingungen nicht erfüllt sind, werden Fehlermeldungen angezeigt. Eine typische Meldung ist das generische „Nichts zu behandeln“. Meldung. Die Meldung kann für viele verschiedenen Ursachen, in den eingehenden und ausgehenden Flüssen angezeigt werden, in denen eine Belegzeile das Feld **Menge. zu behandeln** enthält.

## <a name="bin-content-and-reservations"></a><a name="bin-content-and-reservations"></a><a name="bin-content-and-reservations"></a>Lagerplatzinhalt und Reservierungen

Artikelmengen existieren sowohl als Lagerposten als auch als Artikelposten im Bestand. Diese beiden Postenarten enthalten verschiedene Informationen darüber, wo Artikel vorhanden sind und ob sie verfügbar sind. Lagerplatzposten definieren die Verfügbarkeit eines Artikels nach Lagerplatz und Lagerplatzart, was als Lagerplatzinhalt bezeichnet wird. Artikelposten definieren die Verfügbarkeit eines Artikels durch ihre Reservierung für ausgehenden Belegen.  

[!INCLUDE [prod_short](includes/prod_short.md)] berechnet die zur Kommissinierung verfügbare Menge, wenn der Lagerplatzinhalt mit Reservierungen gekoppelt ist.  

## <a name="quantity-available-to-pick"></a><a name="quantity-available-to-pick"></a><a name="quantity-available-to-pick"></a>Verfügbare Menge für Kommissionierung

[!INCLUDE [prod_short](includes/prod_short.md)] Reserviert Artikel für ausstehende Verkaufsauftragslieferungen, sodass sie nicht für andere Kundenaufträge kommissioniert werden, die früher versendet werden. [!INCLUDE [prod_short](includes/prod_short.md)] subtrahiert Artikelmengen, die bereits in Bearbeitung sind, wie folgt:

* Mengen, die für andere ausgehende Belege reserviert sind.
* Mengen auf vorhandenen Kommissionierungsbelegen.
* Kommissionierte, aber noch nicht versendete oder verbrauchte Mengen.  

Das Ergebnis wird im Feld **Verfügbare Menge** auf der Seite **Kommissionierarbeitsblatt** dynamisch berechnet und angezeigt. Der Wert wird auch berechnet, wenn Benutzer Kommissionierungen direkt für ausgehende Belege erstellen. Es folgen Beispiele für ausgehende Belege:

* Verkaufsaufträge
* Produktionsverbrauch
* Ausgehende Umlagerungen

Das Ergebnis steht in diesen Belegen in den Mengenfeldern, wie z. B. dem Feld **Bewegungsmge**.  

> [!NOTE]  
> Für die Priorität von Reservierungen wird die zu reserviere Menge von der Menge abgezogen, die für die Kommissionierung verfügbar ist. Wenn beispielsweise die Menge, die an den Kommissionierlagerplätzen verfügbar ist, 5 Einheiten ist, sich jedoch 100 Einheiten an Einlagerungslagerplätzen befinden, wird, wenn Sie mehr als 5 Einheiten für einen anderen Auftrag reservieren, eine Fehlermeldung angezeigt, da die zusätzliche Menge an den Kommissionierlagerplätzen verfügbar sein muss.  

### <a name="calculating-the-quantity-available-to-pick"></a><a name="calculating-the-quantity-available-to-pick"></a><a name="calculating-the-quantity-available-to-pick"></a>Berechnen der zur Kommissionierung verfügbaren Menge

[!INCLUDE [prod_short](includes/prod_short.md)] berechnet die zur Kommissionierung verfügbare Menge wird wie folgt:  

Verfügbare Menge für Kommissionierung = Menge in Kommissionierlagerplätzen - Menge in Kommissionierungen und Lagerplatzumlagerungen - (reservierte Menge in Kommissionierlagerplätzen + reservierte Menge in Kommissionierungen und Lagerplatzumlagerungen)  

Das folgende Diagramm zeigt die verschiedenen Elemente der Berechnung.  

![Verfügbar zum Kommissionieren mit Reservierungsüberschneidung.](media/design_details_warehouse_management_availability_2.png "Verfügbar zur Entnahme mit Reservierungsüberschneidung")  

## <a name="quantity-available-to-reserve"></a><a name="quantity-available-to-reserve"></a><a name="quantity-available-to-reserve"></a>Für Reservierung verfügbare Menge

Da die Konzepte des Lagerplatzinhaltes und der Reservierung gleichzeitig existieren, muss die Menge der Artikel, die zur Reservierung verfügbar sind, an die Zuordnung zu ausgehenden Lagerbelegen angepasst sein.  

Sie können alle Bestandsartikel reservieren, mit Ausnahme von Artikeln, für die die Ausgangsverarbeitung begonnen hat. Die Menge, die reservierbar ist, ist als die Menge auf allen Belegen und an allen Lagerplatzarten definiert. Die folgende Ausgangsmengen sind Ausnahmen:  

* Menge für nicht registrierte Kommissionierbelege  
* Menge der in Lieferung enthaltenen Lagerplätze  
* Menge in Fert.-Bereitst.-Lagerplatzcodes  
* Menge in Off. Fert.-Ber.-Lagerpl.  
* Menge in Mont.-Bereitst.-Lagerplätzen  
* Menge in Ausgleichslagerplätzen  

Das Ergebnis wird im Feld **Verfügbare Gesamtmenge** auf der Seite **Reservierungen** angezeigt.  

In einer Reservierungszeile wird die Menge, die nicht reserviert werden kann, da sie im Lager zugeordnet wird, im Feld **Zugewiesene Menge im Lager** auf der Seite **Reservierungen** angezeigt.  

### <a name="calculating-the-quantity-available-to-reserve"></a><a name="calculating-the-quantity-available-to-reserve"></a><a name="calculating-the-quantity-available-to-reserve"></a>Berechnen der zur Reservierung verfügbaren Menge

[!INCLUDE [prod_short](includes/prod_short.md)] berechnet die zur Reservierung verfügbare Menge wird wie folgt:  

Zur Reservierung verfügbare Menge = Gesamtmenge im Lagerbestand - Menge in Kommissionierungen und Lagerplatzumlagerungen für Herkunftsbelege - Reservierte menge - Menge in Ausgangslagerplätzen  

Das folgende Diagramm zeigt die verschiedenen Elemente der Berechnung.  

![Verfügbar zum Reservieren pro Lager-Zuordnung.](media/design_details_warehouse_management_availability_3.png "Verfügbar, um pro Lagerzuordnung zu reservieren")  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Weitere Informationen

[Überblick über die Lagerverwaltung](design-details-warehouse-management.md)
[Anzeigen der Verfügbarkeit von Artikeln](inventory-how-availability-overview.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
