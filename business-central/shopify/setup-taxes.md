---
title: Steuern für Shopify Verbindung einrichten
description: So richten Sie Steuern in Shopify und Business Central ein.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: 0070d583752002cc34ebff74dee2906c289b7136
ms.sourcegitcommit: b353f06e0c91aa6e725d59600f90329774847ece
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2022
ms.locfileid: "9317490"
---
# <a name="set-up-taxes-for-the-shopify-connection"></a>Steuern für Shopify Verbindung einrichten

In diesem Artikel untersuchen wir, wie verschiedene Einstellungen in Shopify sich auf die Storefront-Preise und Steuern auswirken, die dem Kunden angezeigt werden. Wir werden uns auch ansehen, wie man [!INCLUDE[prod_short](../includes/prod_short.md)] zur Unterstützung der Einstellungen in Shopify konfiguriert. Dieser Artikel ist nicht als umfassende Steueranleitung gedacht. Um mehr zu erfahren, wenden Sie sich an Ihre örtliche Steuerbehörde oder einen Steuerexperten.  

Der Artikel geht davon aus, dass Sie beim Verkauf von Waren im In- oder Ausland steuerpflichtig sind.

## <a name="if-you-sell-domestically"></a>Wenn Sie im Inland verkaufen 

Sobald Sie Ihr Shopify konfiguriert haben, um Steuern in Ihrem Heimatland oder Ihrer Heimatregion zu erheben, können Sie entscheiden, wie Sie die Preise auf Ihrer Storefront anzeigen möchten. Sie steuern dies, indem Sie **Alle Preise verstehen sich inklusive Mehrwertsteuer** umschalten in den [**Steuern und Zölle**](https://www.shopify.com/admin/settings/taxes)-Einstellungen in Ihrem **Shopify Administrator**.

Es ist üblich, diesen Schalter für Länder wie Australien, Österreich, Belgien, die Tschechische Republik, Dänemark, Finnland, Frankreich, Deutschland, Island, Italien, die Niederlande, Neuseeland, Norwegen, Spanien, Schweden, die Schweiz und die Tschechische Republik und Vereinigtes Königreich zu aktivieren. In Märkten wie diesen enhält der Preis *100 EUR*, der auf der Produktkarte definiert ist, bereits die Mehrwertsteuer (MwSt.) und derselbe Preis wird dem Kunden im Geschäft und an der Kasse angezeigt.  

In den USA und Kanada erwarten Kunden Produktpreise ohne Steuern, die an der Kasse hinzugefügt werden. So ist das Feld **Alle Preise verstehen sich inklusive Mehrwertsteuer** normalerweise nicht ausgewählt. In diesem Fall ist der Preis *$100* in der Produktkarte ohne MwSt. An der Kasse werden Steuern zusätzlich zum Preis hinzugefügt, um die Kassensumme zu berechnen.

Um das Szenario zu unterstützen, wo **Alle Preise inklusive Mehrwertsteuer** auf der Seite [!INCLUDE[prod_short](../includes/prod_short.md)] ausgewählt ist, füllen Sie das Feld **Debitorenvorlagencode** auf der Seite **Shopify -Shop-Karte** aus für den Zugriff auf die Vorlage mit den folgenden definierten Feldern:  
<!--I changed that last part of the sentence above because it didn't track logically. Just wanted to let you know in case I introduced an inaccuracy.-->

1. **Allgemeine Geschäftsbuchungsgruppe**, für inländische Debitoren.  
2. **MwSt.-Geschäftsbuchungsgrp.**, für inländische Debitoren.  
3. **Preise inkl. MwSt** auf *Ja* gesetzt.  

Definieren Sie nun Artikelpreise im Feld **Artikelkarte** oder **Verkaufspreisliste**, mit oder ohne Steuer. Beim Export der Preise nach Shopify berechnet das System den Preis einschließlich der inländischen Steuern und zeigt diesen Preis dann auf der Produktkarte in Shopify.

> [!NOTE]
> Wenn Sie den Shopify Connector zum automatischen Erstellen von Debitoren konfiguriert haben, benötigen Sie möglicherweise mehr Felder in Ihrer Vorlage, z. B. **Debitorenbuchungsgruppe**. Wenn Sie den Standarddebitor für importierte Bestellungen verwenden, stellen Sie sicher, dass für den Debitor dieselben Felder ausgefüllt sind. Sie müssen immer noch den **Debitorenvorlagecode** wie oben angegeben, ausfüllen, da das Feld **Preise inkl. Steuer**/**Preise inkl. MwSt.** im erstellten Verkaufsdokument nicht vom Debitor abhängt, sondern von der **Debitorenvorlage** aus der Shopify Shop-Karte oder der Debitorenvorlage pro Land.

## <a name="if-you-sell-internationally"></a>Wenn Sie international verkaufen

In diesem Abschnitt untersuchen wir Einstellungen für Szenarien, in denen Sie Steuern erheben müssen, wenn Sie in ein anderes Land verkaufen, z. B. andere Länder in der EU. 

Derzeit unterstützt die Erweiterung **Shopify Connector** nur den Export eines Preises. Shopify wendet automatisch lokale Steuern, Währungen und Rundungen an. Der Schalter **Alle Preise verstehen sich inklusive Mehrwertsteuer** führt zu den Aktionen, die in den folgenden Unterabschnitten beschrieben werden.

### <a name="all-prices-include-tax-is-selected"></a>*Alle Preise verstehen sich inklusive Mehrwertsteuer* ist ausgewählt

||Inlandsverkäufe|Ausland, in dem Sie Steuern erheben|Ausland, in dem Sie keine Steuern erheben|
|------------------------|--------|--------|--------|
|Angezeigter Preis in der Storefront|1200|1200|1200|
|Steuersatzprozentsatz|20|25|0|
|Preis an der Kasse|1200|1200|1200|

Der Preis für den Kunden bleibt unabhängig von seinem Standort intakt, aber Ihre Marge wird aufgrund der von Land zu Land unterschiedlichen Steuersätze beeinflusst.

### <a name="all-prices-include-tax-is-not-selected"></a>*Alle Preise verstehen sich inklusive Mehrwertsteuer* ist nicht ausgewählt

||Inlandsverkäufe|Ausland, in dem Sie Steuern erheben|Ausland, in dem Sie keine Steuern erheben|
|------------------------|--------|--------|--------|
|Angezeigter Preis in der Storefront|1000|1000|1000|
|Steuersatzprozentsatz|20|25|0|
|Preis an der Kasse|1200|1250|1000|

Shopify fügt lokale Steuern zu dem auf der Produktkarte definierten Preis hinzu, je nachdem, wohin die Waren geliefert werden.

## <a name="dynamic-tax-inclusive-pricing"></a>Dynamische Preise inklusive Steuern

Da verschiedene Länder unterschiedliche Anforderungen haben, je nachdem, ob Sie Steuern in den angezeigten Preis einschließen oder nicht, können Sie [Dynamische Preise inklusive Steuern](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing) in Shopify aktivieren. Dies automatisiert die Steuereinschlussfunktion. 
<!--I added the last sentence to complete the thought. I hope that's okay.-->

Wählen Sie **Steuern basierend auf dem Land Ihres Debitors einschließen oder ausschließen** im Abschnitt **Andere Märkte – Präferenzen** der Einstellungen [**Märkte**](https://www.shopify.com/admin/settings/markets) in Ihrem **Shopify Administrator**.  

> [!NOTE]
> Diese Einstellung wirkt sich nicht auf die Darstellung von Preisen auf Inlandsmärkten aus, die vom Umschalter **Alle Preise verstehen sich inklusive Mehrwertsteuer** gesteuert wird.

### <a name="all-prices-include-tax-is-selected"></a>*Alle Preise verstehen sich inklusive Mehrwertsteuer* ist ausgewählt

||Inlandsverkäufe|Ausland, in dem die Steuer im Preis inbegriffen ist|Ausland, in dem die Steuer im Preis nicht inbegriffen ist|
|------------------------|--------|--------|--------|
|Angezeigter Preis in der Storefront|1200|1250|1000|
|Steuersatzprozentsatz|20|25|10|
|Preis an der Kasse|1200|1250|1100|

Der Preis für jeden Kunden ändert sich je nach Standort.

### <a name="all-prices-include-tax-is-not-selected"></a>*Alle Preise verstehen sich inklusive Mehrwertsteuer* ist nicht ausgewählt

||Inlandsverkäufe|Ausland, in dem die Steuer im Preis inbegriffen ist|Ausland, in dem die Steuer im Preis nicht inbegriffen ist|
|------------------------|--------|--------|--------|
|Angezeigter Preis in der Storefront|1000|1250|1000|
|Steuersatzprozentsatz|20|25|10|
|Preis an der Kasse|1200|1250|1100|

> [!NOTE]
> Der Schalter **Alle Preise verstehen sich inklusive Mehrwertsteuer** ändert nicht, wie Preise internationalen Debitoren angezeigt werden.

## <a name="if-you-sell-to-eu-customers"></a>Wenn Sie an EU-Debitoren verkaufen

Verschiedene EU-Länder haben unterschiedliche lokale Steuersätze. Wenn Sie jedoch in der EU ansässig sind und in andere EU-Länder verkaufen, können Sie in einigen Fällen Ihren lokalen Steuersatz verwenden.  

Aktivieren Sie die Option **Mehrwertsteuer einbehalten** im Abschnitt **Europäische Union** der Einstellungen [**Steuern und Zölle**](https://www.shopify.com/admin/settings/taxes) in Ihrem **Shopify Administrator**.

|MwSt. einbehalten|MwSt.-Satz|
|-|-|
|Ausnahmeregelung für Kleinstunternehmen|Verwenden Sie Ihren inländischen Steuersatz für alle Verkäufe innerhalb der EU|
|One-Stop-Shop oder länderspezifische Registrierung|Verwenden Sie den Mehrwertsteuersatz des Landes Ihres Debitors|


### <a name="collect-vat-set-to-one-stop-shop-registration"></a>Sammeln Sie die Mehrwertsteuer, die auf die One-Stop-Shop-Registrierung eingestellt ist

Im folgenden Beispiel ist der Schalter **Alle Preise verstehen sich inklusive Mehrwertsteuer** aktiviert. Der Preis auf der Produktkarte ist auf *1200* gesetzt. 
        
|-|Inlandsverkäufe|Ausland|
|------------------------|--------|--------|
|Angezeigter Preis in der Storefront|1200|1250|
|Steuersatzprozentsatz|20|25|
|Preis an der Kasse|1200|1250|       
        
### <a name="collect-vat-set-to-micro-business-exemption"></a>MwSt. erheben ist auf Ausnahmeregelung für Kleinstunternehmen eingestellt

Im folgenden Beispiel ist der Schalter **Alle Preise verstehen sich inklusive Mehrwertsteuer** aktiviert. Der Preis auf der Produktkarte ist auf *1200* gesetzt. 
        
|-|Inlandsverkäufe|Ausland mit lokalem Steuersatz von 25 Prozent.|
|------------------------|--------|--------|
|Angezeigter Preis in der Storefront|1200|1200|
|Steuersatzprozentsatz|20|20|
|Preis an der Kasse|1200|1200|           
    
Shopify ignoriert bei der Berechnung der Endpreise den Steuersatz im Ausland und verwendet den inländischen Steuersatz.

## <a name="importing-shopify-orders-sold-to-international-customers"></a>Importierender Shopify Bestellungen, die an internationale Debitoren verkauft wurden

Wenn Sie Steuern aus mehreren Ländern erheben, müssen Sie höchstwahrscheinlich eine länderspezifische Einstellung in [!INCLUDE[prod_short](../includes/prod_short.md)] definieren. Dies ist erforderlich, da beim Erstellen eines Verkaufsbelegs in [!INCLUDE[prod_short](../includes/prod_short.md)] das System Steuern berechnet, anstatt aus Shopify importierte wiederzuverwenden.

Länder-/regionsspezifische Einstellungen werden im Fenster **Shopify Debitorenvorlage** ausgewählt.
<!--Should this be "window" or "page"? I haven't been seeing "window" is use elsewhere, but I don't know what the interface looks like for this action.--> Dort können Sie **Standarddebitorennr.** definieren oder **Debitorenvorlagennr.** Stellen Sie in jedem Fall sicher, dass für den ausgewählten Debitoren oder die ausgewählte Vorlage die folgenden Felder definiert sind:

1. **Allgemeine Geschäftsbuchungsgruppe** (für ausländische Debitoren verwendet).
2. **MwSt.-Geschäftsbuchungsgrp.** (für ausländische Debitoren verwendet).
3. **Preise inkl. MwSt** (ausgerichtet auf die Einstellung auf der Shopify Seite):
* Wählen Sie *Ja* aus, wenn **Alle Preise verstehen sich inklusive Mehrwertsteuer** aktiviert ist und **Steuern basierend auf dem Land Ihres Debitoren einschließen oder ausschließen** deaktiviert ist.
* Wählen Sie *Nein* aus, wenn **Alle Preise verstehen sich inklusive Mehrwertsteuer** deaktiviert ist und **Steuern basierend auf dem Land Ihres Debitoren einschließen oder ausschließen** deaktiviert ist.
* Wählen Sie *Ja* aus, wenn **Steuern basierend auf dem Land Ihres Debitoren einschließen oder ausschließen** aktiviert ist und das Land oder die Region in [Steuerpflichtige Länder](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions) aufgeführt ist.
* Wählen Sie *Nein* aus, wenn **Steuern basierend auf dem Land Ihres Debitoren einschließen oder ausschließen** aktiviert ist und das Land oder die Region nicht in [Steuerpflichtige Länder](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions) aufgeführt ist.
<!--I changed "Set" to "Choose" since "Set" really isn't an instruction we use. if they're toggling, we then would say "Toggle" as in "Toggle *No* if...."-->
> 
[!Note]
> Die Einstellung des Feldes **Preise inkl. MwSt** stammt aus der Vorlage, nicht aus dem konkreten Debitoren. Deshalb ist es wichtig, dass die Debitorenvorlage definiert ist.

## <a name="other-tax-remarks"></a>Sonstige Anmerkungen zu Steuern

Während die importierte Shopify-Bestellung Informationen zu Steuern enthält, werden die Steuern neu berechnet, wenn Sie den Verkaufsbeleg erstellen. Diese Neuberechnung bedeutet, dass es wichtig ist, dass die Einstellungen für Mehrwertsteuer/Steuern in [!INCLUDE[prod_short](../includes/prod_short.md)] richtig sind.

- Mehrere Produktsteuer- oder MwSt.-Steuersätze. Beispielsweise unterliegen einige Produktkategorien ermäßigten Steuersätzen. Sie können die [Steuerüberschreitung](https://help.shopify.com/en/manual/taxes/tax-overrides#create-a-manual-collection-for-products-that-need-a-tax-override) Funktion in Shopify verwenden. Beim Importieren und Erstellen von Elementen in [!INCLUDE[prod_short](../includes/prod_short.md)] verwenden sie die Steuereinstellungen, die im Artikelvorlagencode in Shopify Shop ausgefüllt sind. Bevor Sie Bestellungen mit solchen Artikeln importieren, müssen Sie die Umsatzsteuer-Produktbuchungsgruppe aktualisieren.  

- Adressabhängige Steuersätze. Verwenden Sie das Feld **Steuergebiet Priorität** zusammen mit der Tabelle **Kundenvorlagen**, um die Standardlogik zu überschreiben, die den **Steuergebietscode** im Verkaufsdokument ausfüllt. Das Feld **Steuergebiet Priorität** gibt die Priorität an, aus der die Funktion die Informationen über das Land oder die Region und den Staat oder die Provinz übernehmen soll. Dann wird der entsprechende Datensatz in den Kundenvorlagen Shopify identifiziert und die **Steuerkennziffer**, **Steuerpflichtig** und **MwSt Bus. Buchungsgruppe** werden verwendet, wenn ein Verkaufsbeleg erstellt wird.  

## <a name="see-also"></a>Siehe auch

[Einstieg mit dem Konnektor für Shopify](get-started.md)  
