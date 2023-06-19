---
title: Design Details - Durchschnittliche Kalkulation
description: Die durchschnittlichen Kosten eines Artikels werden anhand eines periodischen gewichteten Durchschnitts berechnet.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '8645,'
ms.date: 06/06/2023
ms.author: bholtorf
---
# Designdetails: Einstandspreis

Die durchschnittlichen Kosten eines Artikels werden anhand eines periodischen gewichteten Durchschnitts berechnet. Der Durchschnitt basiert auf der Durchschnittskostenperiode, die in [!INCLUDE[prod_short](includes/prod_short.md)] eingerichtet ist.  

Das Bewertungsdatum wird automatisch festgelegt.  

## Einrichten der-Durchschnittskostenberechnung

In der folgenden Tabelle werden die beiden Felder auf der Seite **Lager einrichten** beschrieben, die ausgefüllt werden müssen, um die Durchschnittskostenberechnung zu aktivieren.  

|Feld|Beschreibung|  
|---------------------------------|---------------------------------------|  
|**Durchschnittskostenperiode**|Gibt an, in welcher Periode die Durchschnittskosten berechnet werden. Folgende Optionen sind verfügbar:<br /><br /> - **Tag**<br />- **Woche**<br />- **Monat**<br />- **Buchhaltungsperiode**<br /><br /> Für Lagerabgänge, die während der Durchschnittskostenperiode gebucht wurden, wird der durchschnittliche Einstandspreis verwendet, der für diese Periode berechnet wurde.|  
|**Einst.-Pr. (durchschn.) Ber.-Art**|Gibt an, wie die durchschnittlichen Kosten eines Artikels berechnet werden. Folgende Optionen sind verfügbar:<br /><br /> - **Artikel**<br />- **Artikel, Variante und Lagerort**<br /> Wenn diese Option ausgewählt ist, berechnet die Anwendung den durchschnittlichen Einstandspreis pro Artikel für jeden Lagerort und für jede Variante des Artikels. Der durchschnittliche Einstandspreis des Artikels davon abhängt, wo er gelagert wird und welche Variante (z. B. welche Farbe) Sie auswählen.|  

> [!NOTE]  
> Sie können nur eine Durchschnittskostenperiode und eine Berechnungsart für den durchschnittlichen Einstandspreis pro Geschäftsjahr verwenden.  
>
> Die Seite **-Buchhaltungsperioden** zeigt, welche Durchschnittskostenperiode und welche Berechnungsart für diese Periode für jede Buchhaltungsperiode aktiv ist.  

## Durchschnittskosten berechnen

 Wenn Sie eine Transaktion für einen Artikel buchen, für den die Lagerabgangsmethode "Durchschnitt" verwendet wird, erstellt die Anwendung einen Posten in der Tabelle **Einst.-Pr. (durchschn.) Regul. Startzeitpunkt**. Dieser Posten enthält die Artikelnummer, den Variantencode und den Lagerortcode der Transaktion. Darüber hinaus enthält der Posten das **Bewertungsdatum**, das das letzte Datum der Durchschnittskostenperiode ist, in der die Transaktion gebucht wurde.  

> [!NOTE]  
> Dieses Feld sollte nicht mit dem Feld **Bewertungsdatum** in der Tabelle **Eintragswert** verwechselt werden, die das Datum anzeigt, an dem der Wert Gültigkeit hat und die verwendet wird, um die Durchschnittskostenperiode festzulegen, zu der der Wertposten gehört.  

 Die Durchschnittskosten einer Transaktion werden berechnet, wenn die Kosten des Artikels reguliert werden. Weitere Informationen finden Sie unter [Designdetails: Kostenanpassung](design-details-cost-adjustment.md) Eine Kostenregulierung verwendet die Posten in der Tabelle **Einst.-Pr. (durchschn.) Regul. Startzeitpunkt**, um zu ermitteln, für welche Artikel (oder Artikel, Lagerorte und Varianten) durchschnittliche Einstandspreise berechnet werden sollen. Für jeden Posten, der noch nicht reguliert wurde, geht die Einstandspreisregulierung wie folgt vor, um den durchschnittlichen Einstandspreis zu bestimmen:  

- Ermitteln des Einstandspreises des Artikels zu Beginn der Durchschnittskostenperiode.  
- Hinzufügen der Summe der Wareneingangskosten, die während der Durchschnittskostenperiode gebucht wurden. Dazu gehören Einkäufe, Verkaufsreklamationen, Istmeldungen und Produktions- und Montageausstoß.  
- Subtrahieren der Summe der Kosten von ausgehenden Transaktionen, die in der Durchschnittskostenperiode fest auf Wareneingänge angewendet wurden. Diese können typischerweise Einkaufsreklamationen und negative Istmeldungen beinhalten.  
- Aufteilen der Gesamtlagermenge für das Ende der Durchschnittskostenperiode. Ausgenommen sind Lagerabgänge, die bewertet werden.  

 Das Programm wendet diesen durchschnittlichen Einstandspreis dann mit den Buchungsdaten auf die Lagerabgänge für den Artikel (oder Artikel, Lagerort und Variante) an, die es in der Durchschnittskostenperiode gegeben hat. Wenn Lagerzugänge vorhanden sind, die fest mit Lagerabgängen in der Durchschnittskostenperiode verknüpft sind, überträgt [!INCLUDE [prod_short](includes/prod_short.md)] den berechneten durchschnittlichen Einstandspreis von dem Zugang an den Abgang.  

### Beispiel: Durchschnittskostenperiode = Tag

Das folgende Beispiel zeigt die Auswirkungen der Berechnung des durchschnittlichen Einstandpreises auf der Grundlage einer Durchschnittskostenperiode von einem Tag. Das Feld **Durchschnittlicher Kostenberechnungstyp** auf der Seite **Lager Einrichtung** ist auf **Artikel** festgelegt.  

Die folgende Tabelle zeigt Artikelposten für den Beispiel-Durchschnittkostenartikel, ITEM1, bevor die **Lagerreg. fakt. Einst. Preise**-Stapelverarbeitung ausgeführt wurde.  

| **Buchungsdatum** | **Artikelpostenart** | **Menge** | **Einstandsbetrag (tatsächl.)** | **Postennummer** |
|--|--|--|--|--|
| 01-01-23 |   Einkauf | 0 | 20.00 | 0 |
| 01-01-23 |   Einkauf | 0 | 40.00 | 2 |
| 01-01-23 |   Verkauf | -1 | -20.00 | 3 |
| 02-01-23 |   Verkauf | -1 | -40.00 | 4 |
| 02-02-23 |   Einkauf | 0 | 100.00 | 5 |
| 02-03-23 |   Verkauf | -1 | -100.00 | 6 |

> [!NOTE]  
> Da die Kostenregulierung noch nicht stattgefunden hat, werden Werte im **Einstandsbetrag (tatsächl.)**-Feld des Bestandes entsprechend den Lagerzugängen, auf die sie angewendet werden, vermindert.  

 In der folgenden Tabelle werden die Posten in der Tabelle **Einst.-Pr. (durchschn.) Regul. Startzeitpunkt** aufgeführt, die sich auf Wertposten beziehen, die sich aus den Artikelposten in der vorherigen Tabelle ergeben.  

| **Artikelnr.** | **Variantencode** | **Lagerortcode** | **Bewertungsdatum** | **Einstandspreis ist reguliert** |
|--|--|--|--|--|
| ARTIKEL1 |  | BLAU | 01-01-23 |   Nein |
| ARTIKEL1 |  | BLAU | 02-01-23 |   Nein |
| ARTIKEL1 |  | BLAU | 02-02-23 |   Nein |
| ARTIKEL1 |  | BLAU | 02-03-23 |   Nein |

 Die folgende Tabelle zeigt dieselben Artikelposten für den Beispiel-Durchschnittkostenartikel, nachdem die **Lagerreg. fakt. Einst. Preise**-Stapelverarbeitung ausgeführt wurde. Der durchschnittliche Einstandspreis pro Tag wird auf die Lagerabgänge berechnet und angewendet.  

| **Buchungsdatum** | **Artikelpostenart** | **Menge** | **Einstandsbetrag (tatsächl.)** | **Postennummer** |
|--|--|--|--|--|--|
| 01-01-23 |   Einkauf | 0 | 20.00 | 0 |
| 01-01-23 |   Einkauf | 0 | 40.00 | 2 |
| 01-01-23 |   Verkauf | -1 | -30.00 | 3 |
| 02-01-23 |   Verkauf | -1 | -30.00 | 4 |
| 02-02-23 |   Einkauf | 0 | 100.00 | 5 |
| 02-03-23 |   Verkauf | -1 | -100.00 | 6 |

### Beispiel: für eine Durchschnittskostenperiode = Monat

 Dieses Beispiel zeigt die Auswirkungen der Berechnung des durchschnittlichen Einstandspreises auf der Grundlage einer Durchschnittskostenperiode von einem Monat. Das Feld **Durchschnittlicher Kostenberechnungstyp** auf der Seite **Lager Einrichtung** ist auf **Artikel** festgelegt.  

 Wenn die Durchschnittskostenperiode ein Monat ist, erstellt [!INCLUDE [prod_short](includes/prod_short.md)] nur einen Posten für jede Kombination aus Artikelnummer, Variantencode, Lagerortcode und Bewertungsdatum.  

 Die folgende Tabelle zeigt Artikelposten für den Beispiel-Durchschnittkostenartikel, ITEM1, bevor die **Lagerreg. fakt. Einst. Preise**-Stapelverarbeitung ausgeführt wurde.  

| **Buchungsdatum** | **Artikelpostenart** | **Menge** | **Einstandsbetrag (tatsächl.)** | **Postennummer** |
|--|--|--|--|--|
| 01-01-23 |   Einkauf | 0 | 20.00 | 0 |
| 01-01-23 |   Einkauf | 0 | 40.00 | 2 |
| 01-01-23 |   Verkauf | -1 | -20.00 | 3 |
| 02-01-23 |   Verkauf | -1 | -40.00 | 4 |
| 02-02-23 |   Einkauf | 0 | 100.00 | 5 |
| 02-03-23 |   Verkauf | -1 | -100.00 | 6 |

> [!NOTE]  
> Da die Kostenregulierung noch nicht stattgefunden hat, werden Werte im **Einstandsbetrag (tatsächl.)**-Feld des Bestandes entsprechend den Lagerzugängen, auf die sie angewendet werden, vermindert.  

In der folgenden Tabelle werden die Posten in der Tabelle **Einst.-Pr. (durchschn.) Regul. Startzeitpunkt** aufgeführt, die sich auf die Wertposten beziehen, die sich aus den Artikelposten in der vorherigen Tabelle ergeben.  

| **Artikelnr.** | **Variantencode** | **Lagerortcode** | **Bewertungsdatum** | **Einstandspreis ist reguliert** |
|--|--|--|--|--|
| ARTIKEL1 |  | BLAU | 01-31-23 |   Nein |
| ARTIKEL1 |  | BLAU | 02-28-23 |   Nein |

> [!NOTE]  
> Das Bewertungsdatum wird auf das das letzte Datum der Durchschnittskostenperiode festgelegt, in diesem Fall den letzten Tag des Monats.  

Die folgende Tabelle zeigt dieselben Artikelposten für den Beispiel-Durchschnittkostenartikel, nachdem die **Lagerreg. fakt. Einst. Preise**-Stapelverarbeitung ausgeführt wurde. Der durchschnittliche Einstandspreis pro Monat wird auf die Lagerabgänge berechnet und angewendet.  

|**Buchungsdatum** | **Artikelpostenart** | **Menge** | **Einstandsbetrag (tatsächl.)** | **Postennummer** |
|--|--|--|--|--|
| 01-01-23 | Einkauf | 0 | 20.00 | 0 |
| 01-01-23 | Einkauf | 0 | 40.00 | 2 |
| 01-01-23 | Verkauf | -1 | -30.00 | 3 |
| 02-01-23 | Verkauf | -1 | -65.00 | 4 |
| 02-02-23 | Einkauf | 0 | 100.00 | 5 |
| 02-03-23 | Verkauf | -1 | -65.00 | 6 |

Der durchschnittliche Einstandspreis für Posten Nummer 3 wird in der Durchschnittskostenperiode für Januar berechnet. Der durchschnittliche Einstandspreis für Posten Nummer 4 und 6 wird in der Durchschnittskostenperiode für Februar berechnet.  

Um den durchschnittlichen Einstandspreis für Februar zu erhalten, addiert [!INCLUDE [prod_short](includes/prod_short.md)] den durchschnittlichen Einstandspreis des Artikels, der im Lagerbestand empfangen wird (100,00) zu dem durchschnittlichen Einstandpreis am Anfang der Periode (30,00). Die Summe (130,00) wird dann durch die Gesamtmenge im Lagerbestand (2) dividiert. Aus der Berechnung ergibt sich der durchschnittliche Einstandspreis des Artikels in der Periode Februar (65,00). Diesen durchschnittlichen Einstandspreis weist das Programm dann den Lagerabgängen in dieser Periode zu (Posten 4 und 6).  

## Geben Sie das Bewertungsdatum ein

 Das Feld **Bewertungsdatum** in der Tabelle **Wertposten** bestimmt, in welche Durchschnittskostenperiode ein Bestandsabgangsposten gehört. Diese Einstellung gilt auch für Lagerbestände des Umlaufbestands (WIP).  

 Die folgende Tabelle zeigt die Kriterien an, die verwendet werden, um das Bewertungsdatum festzulegen.  

| Szenario | Buchungsdatum | Bewertete Menge | Neubewertung | Bewertungsdatum |
|--|--|--|--|--|
| 1 |  | Positiv | Nein | Buchungsdatum des Artikelpostens |
| 2 | Später als das letzte Bewertungsdatum von ausgeglichenen Wertposten | Negativ | Nein | Buchungsdatum des Artikelpostens |
| 3 | Früher als das letzte Bewertungsdatum von ausgeglichenen Wertposten | Positiv | Nein | Neuestes Bewertungsdatum der ausgeglichenen Wertposten |
| 4 |  | Negativ | Ja | Zeigt das Buchungsdatum des Neubewertungseintrags an. |

### Beispiel

Die folgende Tabelle von Wertposten stellt die verschiedenen Szenarien dar.  

| Szenario | Buchungsdatum | Artikelpostenart | Bewertungsdatum | Bewertete Menge | Einstandsbetrag (tatsächl.) | Artikelposten Lfd. Nr. | Postennr. |
|--|--|--|--|--|--|--|--|
| 1 | 01-01-20 | Einkauf | 01-01-20 | 2 | 20.00 | 1 | 1 |
| 2 | 01-15-20 | (Artikel Zu-/Abschlag) | 01-01-20 | 2 | 8.00 | 1 | 2 |
| 3 | 02-01-20 | Verkauf | 02-01-20 | -1 | -14.00 | 2 | 3 |
| 4 | 03-01-20 | (Neubewertung) | 03-01-20 | 1 | -.4.00 | 1 | 4 |
| 5 | 02-01-20 | Verkauf | 03-01-20 | -1 | -10.00 | 3 | 5 |

> [!NOTE]  
> In Postennummer 5 in der vorangehenden Tabelle hat der der Benutzer einen Verkaufsauftrag mit einem Buchungsdatum (02-01-20) eingegeben, das vor dem spätesten Bewertungsdatum ausgeglichener Wertposten (03-01-20) liegt. Wenn der entsprechende Wert im Feld **Einstandsbetrag (tatsächl.)** für dieses Datum (02-01-20) für diesen Posten verwendet würde, dann würde er 14,00 sein. Dies führte zu einer Situation, in der der Lagerbestand Null ist, aber der Lagerwert - 4,00 ist.  
>
> Um einen solchen Menge-Wert-Konflikt zu vermeiden, wird das Bewertungsdatum festgelegt, um dem spätesten Bewertungsdatum der ausgeglichenen Wertposten (03-01-20) zu entsprechen. Der Wert im **Einstandsbetrag (tatsächl.)**-Feld wird 10,00 (nach Neubewertung), d. h., dass der Lagerbestand Null ist, und dass der Lagerwert ebenfalls Null ist.  

> [!CAUTION]  
> Da der Bericht **Lagerwert berechnen** auf dem Buchungsdatum basiert, spiegelt der Bericht sämtliche Menge-Wert-Konflikte in den Szenarien wie im oben stehenden Beispiel wider. Weitere Informationen finden Sie unter [Designdetails: Planungsparameter](design-details-inventory-valuation.md).  

Wenn der Lagerbestand kleiner als Null ist, nachdem Sie den Lagerabgang gebucht haben, wird das Bewertungsdatum zuerst auf das Buchungsdatum des Lagerabgangs gesetzt. Sie können dieses Datum wenn der Lagerzugang angewendet wird entsprechend den Regeln ändern, die im Hinweis zuvor in diesem Abschnitt beschriebenen wurden.  

## Durchschnittskosten erneut berechnen

Die Bewertung von Lagerabgängen als gewichteter Durchschnitt wäre in mehreren Szenarien unkompliziert:

- Einkäufe werden immer vor Verkäufen in Rechnung gestellt.
- Buchungen werden niemals rückdatiert.
- Sie haben niemals Fehler gemacht.

Die Realität sieht jedoch anders aus.  

Wie die Beispiele in diesem Artikel zeigen, wird das Bewertungsdatum als das Datum festlegt, ab dem der Wertposten in der Berechnung der durchschnittlichen Kosten berücksichtigt wird. Mit dieser Einstellung können Sie verschiedene Dinge für Artikel mit der Durchschnittslagerabgangsmethode tun:  

- Fakturieren des Verkaufs eines Artikels, bevor Sie den Kauf fakturieren.  
- Eine Buchung zurückdatieren.  
- Inkorrekte Buchung wiederherstellen.  

> [!NOTE]  
> Eine weiterer Ursache für diese Flexibilität ist der feste Ausgleich. Weitere Informationen über feste Anwendung, siehe [Unter Designdetails: Artikelanwendung](design-details-item-application.md).  

Aufgrund dieser Flexibilität müssen Sie möglicherweise den durchschnittlichen Einstandspreis nach der Buchung neu berechnen. Wenn Sie beispielsweise einen Lagerzugang oder -abgang mit einem Bewertungsdatum buchen, das vor einem Lagerabgang liegt. Die erneute Berechnung der Durchschnittskosten geschieht automatisch, wenn Sie die **Lagerreg. fakt. Einst.-Preise**-Stapelverarbeitung ausführen, manuell oder automatisch.  

Sie können Bestandsbewertungsbasis innerhalb einer Buchhaltungsperiode zu ändern, indem Sie die Werte in den Feldern **Durchschnittskostenperiode** und **Einst.-Pr. (durchschn.) Ber.-Art** ändern. Sie sollten jedoch vorsichtig sein und Ihren Wirtschaftsprüfer konsultieren.  

### Beispiel für neu berechnete durchschnittliche Einstandspreise

Dieses Beispiel zeigt, wie [!INCLUDE [prod_short](includes/prod_short.md)] den durchschnittlichen Einstandspreis neu berechnet, wenn Sie an einem Datum buchen, das vor einem Lagerabgang liegt. Das Beispiel basiert auf einer Durchschnittskostenperiode **Tag**.  

Die folgende Tabelle zeigt die Wertposten, die für den Artikel vorhanden sind, bevor die Buchung eingegeben wurde.  

| Bewertungsdatum | Menge | Einstandsbetrag (tatsächl.) | Postennr. |
|--|--|--|--|
| 01-01-20 | 1 | 10.00 | 1 |
| 01-02-20 | 1 | 20.00 | 2 |
| 02-15-20 | -1 | -15.00 | 3 |
| 02-16-20 | -1 | -15.00 | 4 |

Der Benutzer erzeugt einen Lagerzugang (Postennummer 5) mit einem Bewertungsdatum (01-03-20), das vor einem Lagerabgang liegt. Um den Lagerbestand auszugleichen, muss der durchschnittliche Einstandspreis neu berechnet und auf 17,00 angepasst werden.  

Die folgende Tabelle zeigt die Wertposten, die für den Artikel vorhanden sind, nachdem Postennummer 5 eingegeben wurde.  

| Bewertungsdatum | Menge | Einstandsbetrag (tatsächl.) | Postennr. |
|--|--|--|--|
| 01-01-20 | 1 | 10.00 | 1 |
| 01-02-20 | 1 | 20.00 | 2 |
| 01-03-20 | 1 | 21.00 | 5 |
| 02-15-20 | -1 | -17.00 | 3 |
| 02-16-20 | -1 | -17.00 | 4 |

## Siehe auch

[Designdetails: Lagerbewertung](design-details-inventory-costing.md)  
[Designdetails: Lagerabgangsmethoden](design-details-costing-methods.md)  
[Designdetails: Lagerregulierung](design-details-cost-adjustment.md)  
[Designdetails: Artikelausgleich](design-details-item-application.md)  
[Verwalten der Bestandsregulierung](finance-manage-inventory-costs.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Glossar der Begriffe in Dynamics 365-Geschäftsprozessen](/dynamics365/guidance/business-processes/glossary)  
[Einen Überblick Nachkalkulation für Produkte und Dienstleistungen festlegen](/dynamics365/guidance/business-processes/product-service-define-cost-overview)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
