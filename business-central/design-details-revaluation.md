---
title: Designdetailsl- Neubewertung | Microsoft Docs
description: Sie können den Lagerbestand basierend auf der Bewertungsbasis, die den Lagerwert am genauesten wiedergibt, neu bewerten. Sie können eine Neubewertung auch zurückdatieren, damit der Wareneinsatz (COGS) ordnungsgemäß für Artikel aktualisiert wird, die bereits verkauft wurden. Artikel mit der Lagerabgangsmethode "Standard", die noch nicht vollständig fakturiert wurden, können ebenfalls neu bewertet werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: a052f726169fde9e09e83aeb690169580eaee948
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215778"
---
# <a name="design-details-revaluation"></a>Designdetails: Neubewertung
Sie können den Lagerbestand basierend auf der Bewertungsbasis, die den Lagerwert am genauesten wiedergibt, neu bewerten. Sie können eine Neubewertung auch zurückdatieren, damit der Wareneinsatz (COGS) ordnungsgemäß für Artikel aktualisiert wird, die bereits verkauft wurden. Artikel mit der Lagerabgangsmethode "Standard", die noch nicht vollständig fakturiert wurden, können ebenfalls neu bewertet werden.  

In [!INCLUDE[prod_short](includes/prod_short.md)] wird die folgende Flexibilität für die Neubewertung unterstützt:  

-   Die neu bewertbare Menge kann für jedes Datum berechnet werden, auch zeitlich rückwärts.  
-   Für Artikel mit der Kostenberechnungsmethode Standard sind Soll-Kosten-Posten in der Neubewertung enthalten.  
-   Bestandsminderungen, die von der Neubewertung betroffen sind, werden erkannt.  

## <a name="calculating-the-revaluable-quantity"></a>Berechnung der neubewertbaren Menge  
 Die neu bewertbare Menge ist die Restmenge im Bestand, die für die Neubewertung an einem vorgegebenen Datum verfügbar ist. Sie wird als die Gesamtsumme der Mengen vollständig fakturierter Artikelposten berechnet, die ein Buchungsdatum gleich oder vor dem Neubewertungsbuchungsdatum haben.  

> [!NOTE]  
>  Artikel mit der Lagerabgangsmethode "Standard" werden bei der Berechnung der neubewertbaren Menge pro Artikel, Menge, Lagerort und Variante unterschiedlich berechnet. Die Mengen und Werte von Artikelposten, die noch nicht vollständig fakturiert wurden, werden in der neu bewertbaren Menge eingeschlossen.  

Nachdem eine Neubewertung gebucht wurde, können Sie einen Lagerzugang oder einen Abgang mit einem Buchungsdatum buchen, das vor dem Neubewertungsbuchungsdatum liegt. Diese Menge wird jedoch nicht durch die Neubewertung beeinflusst. Um den Lagerbestand auszugleichen, wird nur die ursprüngliche neu bewertbare Menge berücksichtigt.  

Da die Neubewertung an jedem beliebigen Datum erstellt werden kann, müssen Sie Konventionen dafür haben, wann ein Artikel aus finanzieller Sicht als Teil des Lagerbestands gilt. Wenn beispielsweise der Artikel im Lager ist und der Artikel WIP (WIP) ist.  

### <a name="example"></a>Beispiel  
Im folgenden Beispiel wird gezeigt, wann ein WIP-Artikel Teil des Bestands wird. Das Beispiel basiert auf der Produktion einer Kette mit 150 Gliedern.  

![“RIF-Lagerbestand und Neubewertung](media/design_details_inventory_costing_10_revaluation_wip.png "“RIF-Lagerbestand und Neubewertung")  

**1Q**: Der Benutzer bucht die eingekauften Links als erhalten. Die folgende Tabelle zeigt den sich daraus ergebenden Artikelposten.  

|Buchungsdatum|Artikel|Postentyp|Menge|Eingabenr.|  
|------------------|----------|----------------|--------------|---------------|  
|01-01-20|LINK|Einkauf|150|1|  

> [!NOTE]  
>  Jetzt ist ein Artikel mit der Lagerabgangsmethode "Standard" für eine Neubewertung verfügbar.  

**1V**: Der Benutzer bucht die eingekauften Links als fakturiert und die Links werden aus finanzieller Sicht Teil des Lagerbestands. Die folgende Tabelle zeigt die sich daraus ergebenden Wertposten.  

|Buchungsdatum|Postentyp|Bewertungsdatum|Einstandsbetrag (tatsächl.)|Artikelposten Lfd. Nr.|Lfd. Nr.|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|01-15-20|EK-Preis|01-01-20|150.00|1|1|  

 **2Q + 2V**: Der Benutzer bucht die eingekauften Links als verbraucht für die Produktion der Eisenkette. Aus finanziellen Gesichtspunkten werden die Links Teil des WIP-Bestands.  Die folgende Tabelle zeigt den sich daraus ergebenden Artikelposten.  

|Buchungsdatum|Artikel|Postentyp|Menge|Lfd. Nr.|  
|------------------|----------|----------------|--------------|---------------|  
|02-01-20|LINK|Verbrauch|-150|1|  

Die folgende Tabelle zeigt den sich daraus ergebenden Wertposten.  

|Buchungsdatum|Postentyp|Bewertungsdatum|Einstandsbetrag (tatsächl.)|Artikelposten Lfd. Nr.|Lfd. Nr.|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|02-01-20|EK-Preis|02-01-20|-150.00|2|2|  

Das Bewertungsdatum wird auf das Datum der Verbrauchsbuchung (02-01-20) als regelmäßiger Lagerabgang festgelegt.  

**3Q**: Der Benutzer bucht die Kette als fertig gestellt und schließt den Fertigungsauftrag ab. Die folgende Tabelle zeigt den sich daraus ergebenden Artikelposten.  

|Buchungsdatum|Artikel|Postentyp|Menge|Postennr.|  
|------------------|----------|----------------|--------------|---------------|  
|02-15-20|Kette|Istmeldung|1|3|  

**3V**: Der Benutzer führt die **Kosten anpassen - Artikeleingabe**-Stapelverarbeitung aus, die die Kette als fakturiert bucht, um anzugeben, dass aller Materialverbrauch vollständig fakturiert wurde. Aus finanziellen Gesichtspunkten sind die Links nicht mehr Teil des WIP-Bestands, wenn die Ausgabe vollständig fakturiert und angepasst ist. Die folgende Tabelle zeigt die sich daraus ergebenden Wertposten.  

|Buchungsdatum|Postentyp|Bewertungsdatum|Einstandsbetrag (tatsächl.)|Artikelposten Lfd. Nr.|Lfd. Nr.|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|01-15-20|EK-Preis|01-01-20|150.00|2|2|  
|02-01-20|EK-Preis|02-01-20|-150.00|2|2|  
|02-15-20|EK-Preis|02-15-20|150.00|3|3|  

## <a name="expected-cost-in-revaluation"></a>Soll-Kosten in der Neubewertung  
Die neu bewertbare Menge wird als die Gesamtsumme der Mengen vollständig fakturierter Artikelposten berechnet, die ein Buchungsdatum gleich oder vor dem Neubewertungsbuchungsdatum haben. Das bedeutet, dass, wenn mehrere Artikel eingegangen/geliefert, aber noch nicht fakturiert sind, deren Lagerwert nicht berechnet werden kann. Artikel mit der Lagerabgangsmethode Standard werden nicht in dieser Hinsicht begrenzt.  

> [!NOTE]  
>  Eine weitere Art von erwarteten Kosten, die neubewertet werden können, ist der WIP-Bestand, für den bestimmte Regeln gelten. Weitere Informationen finden Sie unter [WIP Neubewerten von Lagerbestand](design-details-revaluation.md#wip-inventory-revaluation).  

Wenn Sie die neu bewertbare Menge für Artikel mit der Lagerabgangsmethode Standard wird, werden Artikelposten, die noch nicht vollständig fakturiert wurden, in die Berechnung einbezogen. Diese Posten werden dann neu bewertet, wenn Sie die Neubewertung buchen. Wenn Sie den neu bewerteten Posten fakturieren, werden die folgenden Wertposten erzeugt:  

-   Der übliche fakturierte Wertposten mit dem Postentyp **Direkte Kosten**. Der Kostenbetrag für diesen Posten entspricht den direkten Kosten aus der Herkunftszeile.  
-   Ein Wertposten mit dem Postentyp **Abweichung**. Dieser Eintrag erfasst die Differenz zwischen den fakturierten Kosten und dem neu bewerteten Einstandspreis.  
-   Ein Wertposten mit dem Postentyp **Neubewertung**. Dieser Posten erfasst die Stornierung der Neubewertung der Soll-Kosten.  

### <a name="example"></a>Beispiel  
Im folgenden Beispiel, das auf der Produktion der Kette im vorherigen Beispiel basiert, stellt dar, wie die drei Arten von Posten erstellt werden. Die basiert auf dem folgenden Szenario:  

1.  Der Benutzer bucht die eingekauften Glieder als mit einem Einstandspreis von MW 2,00 erhalten.  
2.  Der Benutzer bucht dann eine Neubewertung der Links durch einen neuen Einstandspreis von MW 3,00 und aktualisiert den Einstandspreis (fest) auf MW 3,00.  
3.  Der Benutzer bucht den ursprünglichen Einkauf der Glieder als fakturiert, wodurch Folgendes erzeugt wird:  

    1.  Ein fakturierter Wertposten mit dem Postentyp **Direkte Kosten**.  
    2.  Ein Wertposten mit dem Postentyp **Neubewertung** zur Erfassung der Umkehrung der Neubewertung der erwarteten Kosten.  
    3.  Ein Wertposten mit dem Postentyp Abweichung, der die Differenz zwischen den fakturierten Kosten und den neu bewerteten Standardkosten aufzeichnet.  
Die folgende Tabelle zeigt die sich daraus ergebenden Wertposten.  

|Schritt|Buchungsdatum|Postentyp|Bewertungsdatum|Einstandsbetrag (erwartet)|Einstandsbetrag (tatsächl.)|Artikelposten Lfd. Nr.|Lfd. Nr.|  
|----------|------------------|----------------|--------------------|------------------------------|----------------------------|---------------------------|---------------|  
|1.|01-15-20|EK-Preis|01-15-20|300.00|0.00|1|1|  
|2.|01-20-20|Neubewertung|01-20-20|150.00|0.00|1|2|  
|3.a.|01-15-20|EK-Preis|01-15-20|-300.00|0.00|1|3|  
|3.b.|01-15-20|Neubewertung|01-20-20|-150.00|0.00|1|4|  
|3.c.|01-15-20|Abweichung|01-15-20|0.00|450.00|1|5|  

## <a name="determining-whether-an-inventory-decrease-is-affected-by-revaluation"></a>Bestimmen Sie, ob eine Bestandsreduzierung von der Neubewertung betroffen ist  
Das Datum der Buchung oder der Neubewertung wird verwendet, um zu ermitteln, ob eine Bestandsminderung von einer Neubewertung beeinflusst wird.  

Die folgende Tabelle zeigt die Kriterien an, die für einen Artikel verwendet werden, der nicht das Durchschnittskostenbewertungsverfahren verwendet.  

|Szenario|Lfd. Nr.|Zeitablauf|Beeinflusst durch Neubewertung|  
|--------------|---------------|------------|-----------------------------|  
|A|Früher als die Neubewertungsposten-Nummer|Früher als das Neubewertungsbuchungsdatum|Nein|  
|B|Früher als die Neubewertungsposten-Nr.|Gleich Neubewertungsbuchungsdatum|Nein|  
|L|Früher als die Neubewertungsposten-Nr.|Später als das Neubewertungsbuchungsdatum|Ja|  
|T|Später als die Neubewertungsposten-Nr.|Früher als das Neubewertungsbuchungsdatum|Ja|  
|O|Später als die Neubewertungsposten-Nr.|Gleich Neubewertungsbuchungsdatum|Ja|  
|W|Später als die Neubewertungsposten-Nr.|Später als das Neubewertungsbuchungsdatum|Ja|  

### <a name="example"></a>Beispiel  
Das folgende Beispiel, das die Neubewertung eines Artikels zeigt, der die FIFO-Kostenbewertungsmethode verwendet, basiert auf dem folgenden Szenario:  

1.  In 01-01-20 bucht der Benutzer einen Einkauf von 6 Einheiten.  
2.  In 02-01-20 bucht der Benutzer einen Verkauf von 1 Einheit.  
3.  In 03-01-20 bucht der Benutzer einen Verkauf von 1 Einheit.  
4.  In 04-01-20 bucht der Benutzer einen Verkauf von 1 Einheit.  
5.  In 03-01-20 berechnet der Benutzer den Lagerwert für den Artikel und bucht eine Neubewertung des Einstandspreises des Artikels von MW 10,00 auf MW 8,00.  
6.  In 02-01-20 bucht der Benutzer einen Verkauf von 1 Einheit.  
7.  In 03-01-20 bucht der Benutzer einen Verkauf von 1 Einheit.  
8.  In 04-01-20 bucht der Benutzer einen Verkauf von 1 Einheit.  
9. Der Benutzer führt die Stapelverarbeitung **Kosten anpassen - Artikeleingänge** aus.  

Die folgende Tabelle zeigt die sich daraus ergebenden Wertposten.  

|Szenario|Buchungsdatum|Postentyp|Bewertungsdatum|Bewertete Menge|Einstandsbetrag (tatsächl.)|Artikelposten Lfd. Nr.|Lfd. Nr.|  
|--------------|------------------|----------------|--------------------|---------------------|----------------------------|---------------------------|---------------|  
||01-01-20|Einkauf|01-01-20|6|60.00|1|1|  
||03-01-20|Neubewertung|03-01-20|4|-8.00|1|5|  
|A|02-01-20|Verkauf|02-01-20|-1|-10.00|2|2|  
|B|03-01-20|Verkauf|03-01-20|-1|-10.00|3|3|  
|L|04-01-20|Verkauf|04-01-20|-1|-10.00|4|4|  
||04-01-20|Verkauf|04-01-20|-1|2.00|4|9|  
|T|02-01-20|Verkauf|03-01-20|-1|-10.00|5|6|  
||02-01-20|Verkauf|03-01-20|-1|2.00|5|10|  
|O|03-01-20|Verkauf|03-01-20|-1|-10.00|6|7|  
||03-01-20|Verkauf|03-01-20|-1|2.00|6|11|  
|W|04-01-20|Verkauf|04-01-20|-1|-10.00|7|8|  
||04-01-20|Verkauf|04-01-20|-1|2.00|7|12|  

## <a name="wip-inventory-revaluation"></a>"Lagerbewertung - Aktiviert"  
Die Neubewertung des WIP-Bestands impliziert die Neubewertung von Komponenten, die als Teil des WIP-Bestands zum Zeitpunkt der Neubewertung erfasst sind.  

In diesem Sinne ist es wichtig, Konventionen dahingehend zu schaffen, wenn ein Artikel als Teil des Produktionslagers aus finanzieller Sicht betrachtet wird. In [!INCLUDE[prod_short](includes/prod_short.md)] bestehen die folgenden Konventionen:  

-   Mit dem Buchen eines fakturierten Einkaufs wird eine eingekaufte Komponente Teil des Rohmaterialbestands.  
-   Eine eingekaufte/als Untermontage verbaute Komponente wird Teil des WIP-Lagerbestands seit dem Buchen ihres Verbrauchs in Verbindung mit einem Fertigungsauftrag.  
-   Eine eingekaufte/als Untermontage verbaute Komponente bleibt Teil des WIP-Lagerbestands bis zu dem Zeitpunkt, an dem ein Fertigungsauftrag (Produktionsartikel) fakturiert wird.  

Die Art, wie das Bewertungsdatum des Wertpostens von Verbrauch festgelegt wird, folgt denselben Regeln wie für Nicht-WIP-Bestand. Weitere Informationen finden Sie im Abschnitt [Feststellen, ob eine Bestandsminderung von der Neubewertung beeinflusst wird](design-details-revaluation.md#determining-whether-an-inventory-decrease-is-affected-by-revaluation).  

Das Produktionslager kann neubewertet werden, solange das Neubewertungsdatum nicht hinter dem Buchungsdatum des entsprechenden Artikelposten des Typs Verbrauch liegt und solange der entsprechende Fertigungsauftrag noch nicht fakturiert wurde.  

> [!CAUTION]  
>  Der Bericht **Bestandsbewertung - WIP** zeigt den Wert der gebuchten Fertigungsauftragsposten und kann daher für WIP-Artikel, die neu bewertet wurden, etwas irreführend sein.  

## <a name="see-also"></a>Siehe auch  
 [Designdetails: Lagerkostenberechnung](design-details-inventory-costing.md)   
 [Designdetails: Kostenberechnungsmethoden](design-details-costing-methods.md)   
 [Designdetails: Lagerkosten Bewerten](design-details-inventory-valuation.md) [Verwalten der Lagerkosten](finance-manage-inventory-costs.md)  
 [Finanzen](finance.md)  
 [Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]