---
title: 'Designdetails: Durchschnittskosten | Microsoft Docs'
description: Die Durchschnittskosten eines Artikels werden mit einem periodischen gewichteten Durchschnitt berechnet, basierend auf der Durchschnittskostenperiode, die in Business Central eingerichtet wurde.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 917aab6c4062233ff5cedb32f8aa75b84687849b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779657"
---
# <a name="design-details-average-cost"></a>Designdetails: Durchschnittskosten
Die Durchschnittskosten eines Artikels werden mit einem periodischen gewichteten Durchschnitt berechnet, basierend auf der Durchschnittskostenperiode, die in [!INCLUDE[prod_short](includes/prod_short.md)] eingerichtet wurde.  

 Das Bewertungsdatum wird automatisch festgelegt.  

## <a name="setting-up-average-cost-calculation"></a>Einrichten der-Durchschnittskostenberechnung  
 In der folgenden Tabelle werden die beiden Felder auf der Seite **Lager einrichten** beschrieben, die ausgefüllt werden müssen, um die Durchschnittskostenberechnung zu aktivieren.  

|Feld|Beschreibung|  
|---------------------------------|---------------------------------------|  
|**Durchschnittskostenperiode**|Gibt an, in welcher Periode die Durchschnittskosten berechnet werden. Folgende Optionen sind verfügbar:<br /><br /> -   **Tag**<br />-   **Woche**<br />-   **Monat**<br />-   **Buchhaltungsperiode**<br /><br /> Für alle Lagerabgänge, die während der Durchschnittskostenperiode gebucht wurden, wird der durchschnittliche Einstandspreis verwendet, der für diese Periode berechnet wurde.|  
|**Durchschnittlicher Kostenberechnungstyp**|Gibt an, wie die durchschnittlichen Kosten eines Artikels berechnet werden. Folgende Optionen sind verfügbar:<br /><br /> -   **Artikel**<br />-   **Artikel, Variante und Lagerort**<br />     Wenn diese Option ausgewählt ist, berechnet die Anwendung den durchschnittlichen Einstandspreis pro Artikel für jeden Lagerort und für jede Variante des Artikels. Dies bedeutet, dass der durchschnittliche Einstandspreis des Artikels davon abhängt, wo er gelagert wird und welche Variante (z. B. welche Farbe) des Artikels Sie ausgewählt haben.|  

> [!NOTE]  
>  Sie können nur eine Durchschnittskostenperiode und eine Berechnungsart für den durchschnittlichen Einstandspreis pro Geschäftsjahr verwenden.  
>   
>  Die Seite **-Buchhaltungsperioden** zeigt, welche Durchschnittskostenperiode und welche Berechnungsart für diese Periode für jede Buchhaltungsperiode aktiv ist.  

## <a name="calculating-average-cost"></a>Durchschnittskosten berechnen  
 Wenn Sie eine Transaktion für einen Artikel buchen, für den die Lagerabgangsmethode "Durchschnitt" verwendet wird, erstellt die Anwendung einen Posten in der Tabelle **Einst.-Pr. (durchschn.) Regul. Startzeitpunkt**. Dieser Posten enthält die Artikelnummer, den Variantencode und den Lagerortcode der Transaktion. Darüber hinaus enthält der Posten das **Bewertungsdatum**, das das letzte Datum der Durchschnittskostenperiode ist, in der die Transaktion gebucht wurde.  

> [!NOTE]  
>  Dieses Feld sollte nicht mit dem Feld **Bewertungsdatum** in der Tabelle **Eintragswert** verwechselt werden, die das Datum anzeigt, an dem der Wert Gültigkeit hat und die verwendet wird, um die Durchschnittskostenperiode festzulegen, zu der der Wertposten gehört.  

 Die Durchschnittskosten einer Transaktion werden berechnet, wenn die Kosten des Artikels reguliert werden. Weitere Informationen finden Sie unter [Designdetails: Kostenanpassung](design-details-cost-adjustment.md) Eine Kostenregulierung verwendet die Posten in der Tabelle **Einst.-Pr. (durchschn.) Regul. Startzeitpunkt**, um zu ermitteln, für welche Artikel (oder Artikel, Lagerorte und Varianten) durchschnittliche Einstandspreise berechnet werden sollen. Für jeden Posten, der noch nicht reguliert wurde, geht die Einstandspreisregulierung wie folgt vor, um den durchschnittlichen Einstandspreis zu bestimmen:  

-   Ermitteln des Einstandspreises des Artikels zu Beginn der Durchschnittskostenperiode.  
-   Hinzufügen der Summe der Wareneingangskosten, die während der Durchschnittskostenperiode gebucht wurden. Dazu gehören Einkäufe, Verkaufsreklamationen, Istmeldungen und Produktions- und Montageausstoß.  
-   Subtrahieren der Summe der Kosten von ausgehenden Transaktionen, die in der Durchschnittskostenperiode fest auf Wareneingänge angewendet wurden. Diese können typischerweise Einkaufsreklamationen und negative Istmeldungen beinhalten.  
-   Dividiert durch die gesamte Lagerbestandsmenge für das Ende der Durchschnittskostenperiode, ausschließlich der Bestandsreduzierungen, die bewertet werden.  

 Das Programm wendet diesen durchschnittlichen Einstandspreis dann mit den Buchungsdaten auf die Lagerabgänge für den Artikel (oder Artikel, Lagerort und Variante) an, die es in der Durchschnittskostenperiode gegeben hat. Wenn Bestandszunahmen vorhanden sind, die fest mit Bestandsminderungen in der Durchschnittskostenperiode verknüpft sind, werden die berechneten Durchschnittskosten von der Zunahme zur Minderung übertragen.  

### <a name="example-average-cost-period--day"></a>Beispiel: Durchschnittskostenperiode = Tag  
 Das folgende Beispiel zeigt die Auswirkungen der Berechnung der Durchschnittskosten auf der Grundlage einer Durchschnittskostenperiode von einem Tag. Das Feld **Durchschnittlicher Kostenberechnungstyp** auf der Seite **Lager Einrichtung** ist auf **Artikel** festgelegt.  

 Die folgende Tabelle zeigt Artikelposten für den Beispiel-Durchschnittkostenartikel, ITEM1, bevor die **Lagerreg. fakt. Einst. Preise**-Stapelverarbeitung ausgeführt wurde.  

|**Buchungsdatum**|**Artikelpostenart**|**Menge**|**Einstandsbetrag (tatsächl.)**|**Postennr.**|  
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
|01-01-20|Einkauf|1|20.00|1|  
|01-01-20|Einkauf|1|40.00|2|  
|01-01-20|Verkauf|-1|-20.00|3|  
|02-01-20|Verkauf|-1|-40.00|4|  
|02-02-20|Einkauf|1|100.00|5|  
|02-03-20|Verkauf|-1|-100.00|6|  

> [!NOTE]  
>  Da die Kostenregulierung noch nicht stattgefunden hat, werden Werte im **Einstandsbetrag (tatsächl.)**-Feld des Bestandes entsprechend den Lagerzugängen, auf die sie angewendet werden, vermindert.  

 In der folgenden Tabelle werden die Posten in der Tabelle **Einst.-Pr. (durchschn.) Regul. Startzeitpunkt** aufgeführt, die sich auf Wertposten beziehen, die aus den Artikelposten in der vorherigen Tabelle resultieren.  

|**Artikelnr.**|**Variantencode**|**Lagerortcode**|**Bewertungsdatum**|**Einstandspreis ist reguliert**|  
|-------------------------------------|-----------------------------------------|------------------------------------------|-------------------------------------------|---------------------------------------------|  
|ARTIKEL1||BLAU|01-01-20|Nr.|  
|ARTIKEL1||BLAU|02-01-20|Nr.|  
|ARTIKEL1||BLAU|02-02-20|Nein|  
|ARTIKEL1||BLAU|02-03-20|Nein|  

 Die folgende Tabelle zeigt dieselben Artikelposten für den Beispiel-Durchschnittkostenartikel, nachdem die **Lagerreg. fakt. Einst. Preise**-Stapelverarbeitung ausgeführt wurde. Der durchschnittliche Einstandspreis pro Tag wird auf die Lagerabgänge berechnet und angewendet.  

|**Buchungsdatum**|**Artikelpostenart**|**Menge**|**Einstandsbetrag (tatsächl.)**|**Postennr.**|  
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
|01-01-20|Einkauf|1|20.00|1|  
|01-01-20|Einkauf|1|40.00|2|  
|01-01-20|Verkauf|-1|-30.00|3|  
|02-01-20|Verkauf|-1|-30.00|4|  
|02-02-20|Einkauf|1|100.00|5|  
|02-03-20|Verkauf|-1|-100.00|6|  

### <a name="example-average-cost-period--month"></a>Beispiel: für eine Durchschnittskostenperiode = Monat  
 Das folgende Beispiel zeigt die Auswirkungen der Berechnung der Durchschnittskosten auf der Grundlage einer Durchschnittskostenperiode von einem Monat. Das Feld **Durchschnittlicher Kostenberechnungstyp** auf der Seite **Lager Einrichtung** ist auf **Artikel** festgelegt.  

 Wenn die Durchschnittskostenperiode ein Monat ist, wird nur ein Posten für jede Kombination von Artikelnummer, Variantencode, Lagerortcode und Bewertungsdatum erstellt.  

 Die folgende Tabelle zeigt Artikelposten für den Beispiel-Durchschnittkostenartikel, ITEM1, bevor die **Lagerreg. fakt. Einst. Preise**-Stapelverarbeitung ausgeführt wurde.  

|**Buchungsdatum**|**Artikelpostenart**|**Menge**|**Einstandsbetrag (tatsächl.)**|**Postennr.**|  
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
|01-01-20|Einkauf|1|20.00|1|  
|01-01-20|Einkauf|1|40.00|2|  
|01-01-20|Verkauf|-1|-20.00|3|  
|02-01-20|Verkauf|-1|-40.00|4|  
|02-02-20|Einkauf|1|100.00|5|  
|02-03-20|Verkauf|-1|-100.00|6|  

> [!NOTE]  
>  Da die Kostenregulierung noch nicht stattgefunden hat, werden Werte im **Einstandsbetrag (tatsächl.)**-Feld des Bestandes entsprechend den Lagerzugängen, auf die sie angewendet werden, vermindert.  

 In der folgenden Tabelle werden die Posten in der Tabelle **Einst.-Pr. (durchschn.) Regul. Startzeitpunkt** aufgeführt, die sich auf Wertposten beziehen, die aus den Artikelposten in der vorherigen Tabelle resultieren.  

|**Artikelnr.**|**Variantencode**|**Lagerortcode**|**Bewertungsdatum**|**Einstandspreis ist reguliert**|  
|-------------------------------------|-----------------------------------------|------------------------------------------|-------------------------------------------|---------------------------------------------|  
|ARTIKEL1||BLAU|01-31-20|Nr.|  
|ARTIKEL1||BLAU|02-28-20|Nr.|  

> [!NOTE]  
>  Das Bewertungsdatum wird auf das das letzte Datum der Durchschnittskostenperiode festgelegt, in diesem Fall den letzten Tag des Monats.  

 Die folgende Tabelle zeigt dieselben Artikelposten für den Beispiel-Durchschnittkostenartikel, nachdem die **Lagerreg. fakt. Einst. Preise**-Stapelverarbeitung ausgeführt wurde. Der durchschnittliche Einstandspreis pro Monat wird auf die Lagerabgänge berechnet und angewendet.  

|**Buchungsdatum**|**Artikelpostenart**|**Menge**|**Einstandsbetrag (tatsächl.)**|**Postennr.**|  
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
|01-01-20|Einkauf|1|20.00|1|  
|01-01-20|Einkauf|1|40.00|2|  
|01-01-20|Verkauf|-1|-30.00|3|  
|02-01-20|Verkauf|-1|-65.00|4|  
|02-02-20|Einkauf|1|100.00|5|  
|02-03-20|Verkauf|-1|-65.00|6|  

 Die Durchschnittskosten von Nummer 3 werden in der Durchschnittskostenperiode für Januar und die Durchschnittskosten für die Posten 4 und 6 in der Durchschnittskostenperiode für Februar berechnet.  

 Um den durchschnittlichen Einstandspreis für Februar zu erhalten, wird der durchschnittliche Einstandspreis des Artikels, der im Lagerbestand empfangen wird (100,00) zu dem durchschnittlichen Einstandpreis am Anfang der Periode (30,00) addiert. Die Summe der beiden (130,00) wird dann durch die Gesamtmenge im Bestand (2) geteilt. Dies ergibt die resultierenden Durchschnittskosten des Artikels im Februar (65,00). Diesen durchschnittlichen Einstandspreis weist das Programm dann den Lagerabgängen in dieser Periode zu (Posten 4 und 6).  

## <a name="setting-the-valuation-date"></a>Geben Sie das Bewertungsdatum ein  
 Das Feld **Bewertungsdatum** in der Tabelle **Werteintrag** wird verwendet, um festzustellen, in welche Durchschnittskostenperiode ein Bestandsminderungsposten gehört. Dies trifft zu auch Umlaufbestands (WIP)-Lagerbestand zu.  

 Die folgende Tabelle zeigt die Kriterien an, die verwendet werden, um das Bewertungsdatum festzulegen.  

|Szenario|Buchungsdatum|Bewertete Menge|Neubewertung|Bewertungsdatum|  
|--------------|-------------------------------------|-----------------------------------------|-----------------|-----------------------------------------|  
|1||Positiv|Nr.|Buchungsdatum des Artikelpostens|  
|2|Später als das letzte Bewertungsdatum von ausgeglichenen Wertposten|Negativ|Nein|Buchungsdatum des Artikelpostens|  
|3|Früher als das letzte Bewertungsdatum von ausgeglichenen Wertposten|Positiv|Nein|Neuestes Bewertungsdatum der ausgeglichenen Wertposten|  
|4||Negativ|Ja|Zeigt das Buchungsdatum des Neubewertungseintrags an.|  

### <a name="example"></a>Beispiel  
 Die folgende Tabelle von Wertposten stellt die verschiedenen Szenarien dar.  

|Szenario|Buchungsdatum|Artikelpostenart|Bewertungsdatum|Bewertete Menge|Einstandsbetrag (tatsächl.)|Artikelposten Lfd. Nr.|Postennr.|  
|--------------|-------------------------------------|-----------------------------------------------|-----------------------------------------|-----------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|1|01-01-20|Einkauf|01-01-20|2|20.00|1|1|  
|2|01-15-20|(Artikel &Zu-/Abschlag)|01-01-20|2|8.00|1|2|  
|3|02-01-20|Verkauf|02-01-20|-1|-14.00|2|3|  
|4|03-01-20|(Neubewertung)|03-01-20|1|-.4.00|1|4|  
|5|02-01-20|Verkauf|03-01-20|-1|-10.00|3|5|  

> [!NOTE]  
>  In Postennummer 5 in der vorangehenden Tabelle hat der der Benutzer einen Verkaufsauftrag mit einem Buchungsdatum (02-01-20) eingegeben, das vor dem spätesten Bewertungsdatum ausgeglichener Wertposten (03-01-20) liegt. Wenn der entsprechende Wert im Feld **Einstandsbetrag (tatsächl.)** für dieses Datum (02-01-20) für diesen Posten verwendet würde, dann würde er 14,00 sein. Dies führte zu einer Situation, in der der Lagerbestand Null ist, aber der Lagerwert - 4,00 ist.  
>   
>  Um einen solchen Menge-Wert-Konflikt zu vermeiden, wird das Bewertungsdatum festgelegt, um dem spätesten Bewertungsdatum der ausgeglichenen Wertposten (03-01-20) zu entsprechen. Der Wert im **Einstandsbetrag (tatsächl.)**-Feld wird 10,00 (nach Neubewertung), d. h., dass der Lagerbestand Null ist, und dass der Lagerwert ebenfalls Null ist.  

> [!CAUTION]  
>  Da der Bericht **Lagerwert berechnen** auf dem Buchungsdatum basiert, spiegelt der Bericht sämtliche Menge-Wert-Konflikte in den Szenarien wie im oben stehenden Beispiel wider. Weitere Informationen finden Sie unter [Designdetails: Planungsparameter](design-details-inventory-valuation.md).  

 Wenn der Lagerbestand kleiner als Null ist, nachdem die Bestandsminderung gebucht wurde, wird das Bewertungsdatum zuerst auf das Buchungsdatum der Bestandsminderung gesetzt. Dieses Datum kann später entsprechend den Regeln geändert werden, die im Hinweis zuvor in diesem Abschnitt beschriebenen wurden, wenn der Lagerzugang angewendet wird.  

## <a name="recalculating-average-cost"></a>Durchschnittskosten erneut berechnen  
 Das Bewerten von Lagerabgängen als gewichteter Durchschnitt würde einfach sein, wenn Einkäufe immer fakturiert würden, bevor Verkäufe fakturiert werden, Buchungen nie zurückdatiert würden, und Sie niemals Fehler machen würden. Die Realität weicht jedoch von diesem Ideal etwas ab.  

 Wie in den Beispielen in diesem Thema erläutert, wird das Bewertungsdatum als das Datum festlegt, ab dem der Wertposten in der Berechnung der durchschnittlichen Kosten berücksichtigt wird. Dies gibt Ihnen die Flexibilität, Folgendes für Artikel mit der Lagerabgangsmethode "Durchschnitt" zu tun:  

-   Fakturieren des Verkaufs eines Artikels, bevor der Kauf des Artikels fakturiert wurde.  
-   Eine Buchung zurückdatieren.  
-   Inkorrekte Buchung wiederherstellen.  

> [!NOTE]  
>  Eine weiterer Ursache für diese Flexibilität ist der feste Ausgleich. Weitere Informationen über feste Anwendung, siehe [Unter Designdetails: Artikelanwendung](design-details-item-application.md).  

 Aufgrund dieser Flexibilität müssen Sie möglicherweise die durchschnittlichen Kosten neu berechnen, nachdem die entsprechende Buchung stattgefunden hat. Wenn Sie beispielsweise eine Bestandszunahme oder -minderung mit einem Bewertungsdatum buchen, das vor einem oder mehreren Bestandsminderungen liegt. Die erneute Berechnung der Durchschnittskosten geschieht automatisch, wenn Sie die **Lagerreg. fakt. Einst.-Preise**-Stapelverarbeitung ausführen, manuell oder automatisch.  

 Es ist möglich, die Bestandsbewertungsbasis innerhalb einer Buchhaltungsperiode zu ändern, indem Sie das Feld **Durchschnittskostenperiode** und das Feld **Einst.-Pr.(durchschn.)Ber.-Art** ändern. Dies sollte jedoch vorsichtig und in Abstimmung mit einem Prüfer durchgeführt werden.  

### <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie die Durchschnittskosten berechnet werden, wenn eine späte Buchung an einem Datum eingegeben wird, das vor einem oder mehreren Bestandsminderungen liegt. Das Beispiel basiert auf einer Durchschnittskostenperiode **Tag**.  

 Die folgende Tabelle zeigt die Wertposten, die für den Artikel vorhanden sind, bevor die Buchung eingegeben wurde.  

|Bewertungsdatum|Menge|Einstandsbetrag (tatsächl.)|Postennr.|  
|-----------------------------------------|--------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|1|10.00|1|  
|01-02-20|1|20.00|2|  
|02-15-20|-1|-15.00|3|  
|02-16-20|-1|-15.00|4|  

 Der Benutzer erzeugt einen Lagerzugang (Postennummer 5) mit einem Bewertungsdatum (01-03-20), das vor einem oder mehreren Lagerabgängen ermittelt wird. Um den Lagerbestand auszugleichen, muss der durchschnittliche Einstandspreis neu berechnet und auf 17,00 angepasst werden.  

 Die folgende Tabelle zeigt die Wertposten, die für den Artikel vorhanden sind, nachdem Postennummer 5 eingegeben wurde.  

|Bewertungsdatum|Menge|Einstandsbetrag (tatsächl.)|Postennr.|  
|-----------------------------------------|--------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|1|10.00|1|  
|01-02-20|1|20.00|2|  
|01-03-20|1|21.00|5|  
|02-15-20|-1|-17.00|3|  
|02-16-20|-1|-17.00|4|  

## <a name="see-also"></a>Siehe auch  
 [Designdetails: Lagerkostenberechnung](design-details-inventory-costing.md)   
 [Designdetails: Kostenberechnungsmethoden](design-details-costing-methods.md)   
 [Designdetails: Kostenregulierung](design-details-cost-adjustment.md)   
 [Designdetails: Artikelausgleich](design-details-item-application.md)  
 [Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)  
 [Finanzen](finance.md)  
 [Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]