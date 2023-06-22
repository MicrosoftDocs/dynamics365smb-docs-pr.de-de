---
title: Steuern für Shopify Verbindung einrichten
description: So richten Sie Steuern in Shopify und Business Central ein.
ms.date: 08/19/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
---

# <a name="set-up-taxes-for-the-shopify-connection" />Steuern für Shopify Verbindung einrichten

In diesem Artikel untersuchen wir, wie verschiedene Einstellungen in Shopify sich auf die Storefront-Preise und Steuern auswirken, die dem Kunden angezeigt werden. Wir werden uns auch ansehen, wie man [!INCLUDE[prod_short](../includes/prod_short.md)] zur Unterstützung der Einstellungen in Shopify konfiguriert. Dieser Artikel ist nicht als umfassende Steueranleitung gedacht. Um mehr zu erfahren, wenden Sie sich an Ihre örtliche Steuerbehörde oder einen Steuerexperten.  

Der Artikel geht davon aus, dass Sie beim Verkauf von Waren im In- oder Ausland steuerpflichtig sind.

## <a name="if-you-sell-domestically" />Wenn Sie im Inland verkaufen

Nachdem Sie Ihr Shopify konfiguriert haben, um Steuern in Ihrem Heimatland oder Ihrer Heimatregion zu erheben, können Sie entscheiden, wie Sie die Preise auf Ihrer Storefront anzeigen möchten.

Sie geben an, ob die Steuern im Preis enthalten sind, indem Sie **Alle Preise verstehen sich inklusive Mehrwertsteuer** umschalten in den [**Steuern und Zölle**](https://www.shopify.com/admin/settings/taxes)-Einstellungen in Ihrem **Shopify Administrator**.

Der Umschalter ist normalerweise für die folgenden Länder aktiviert:

* Australien
* Österreich
* Belgien
* Tschechische Republik
* Dänemark
* Finnland
* Frankreich
* Deutschland
* Island
* Italien
* Niederlande
* Neuseeland
* Norwegen
* Spanien
* Schweden
* Schweiz
* Vereinigtes Königreich. 

In solchen Märkten enthält ein auf der Produktkarte definierter Preis von 100 EUR bereits die Mehrwertsteuer (MwSt.). Der Preis, einschließlich Mehrwertsteuer, wird dem Kunden im Geschäft und an der Kasse angezeigt.  

In den USA und Kanada erwarten die Kunden keine Steuern im Preis. Tak wird an der Kasse hinzugefügt, daher ist die Option **Alle Preise inklusive Steuern** normalerweise deaktiviert. In diesem Fall ist der Preis $100 in der Produktkarte ohne MwSt. An der Kasse werden Steuern zum Preis hinzugefügt.

Um das Szenario zu unterstützen, in dem **Alle Preise inklusive Steuern** ausgewählt ist, füllen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] die folgenden Felder im **Shopify Shop aus Karte** Seite:  

1. Aktivieren Sie den Regelschalter **Preise inklusive Mehrwertsteuer** .  
2. Geben Sie im Feld **Umsatzsteuer-Geschäftsbuchungsgruppe** die Buchungsgruppe an, die Sie für inländische Kunden verwenden.  

Definieren Sie nun Artikelpreise im Feld **Artikelkarte** oder **Verkaufspreisliste**, mit oder ohne Steuer. Beim Export der Preise nach Shopify, [!INCLUDE [prod_short](../includes/prod_short.md)] ist die inländische Steuer im berechneten Preis enthalten und zeigt diesen Preis dann auf der Produktkarte in Shopify.

[!Note]
> Diese Einstellungen wirken sich auf den Export von Preisen aus. Wenn Sie Bestellungen aus Shopify importieren, stammt die Einstellung für das Feld **Preise inkl. MwSt.** aus der **Kundenvorlage** auf der Shopify Geschäftskarte oder der Kundenvorlage pro Land. Auch wenn Sie den Standardkunden für importierte Bestellungen verwenden, müssen Sie den **Kundenvorlagencode** eingeben.

## <a name="if-you-sell-internationally" />Wenn Sie international verkaufen

In diesem Abschnitt untersuchen wir Einstellungen für Szenarien, in denen Sie Steuern erheben müssen, wenn Sie in ein anderes Land verkaufen, z. B. andere Länder in der EU.

Derzeit unterstützt die Erweiterung Shopify Connector nur den Export eines Preises. Shopify wendet automatisch lokale Steuern, Währungen und Rundungen an. Der Schalter **Alle Preise verstehen sich inklusive Mehrwertsteuer** führt zu den Aktionen, die in den folgenden Unterabschnitten beschrieben werden.

### <a name="all-prices-include-tax-is-selected" />Alle Preise verstehen sich inklusive Mehrwertsteuer ist ausgewählt

|-|Inlandsverkäufe|Ausland, in dem Sie Steuern erheben|Ausland, in dem Sie keine Steuern erheben|
|------------------------|--------|--------|--------|
|Angezeigter Preis in der Storefront|1200|1200|1200|
|Steuersatzprozentsatz|20|25|0|
|Preis an der Kasse|1200|1200|1200|

Der Preis für den Kunden bleibt unabhängig von seinem Standort intakt, aber Ihre Marge wird dann aufgrund der von Land zu Land unterschiedlichen Steuersätze beeinflusst.

### <a name="all-prices-include-tax-is-not-selected" />Alle Preise verstehen sich inklusive Mehrwertsteuer ist nicht ausgewählt

|-|Inlandsverkäufe|Ausland, in dem Sie Steuern erheben|Ausland, in dem Sie keine Steuern erheben|
|------------------------|--------|--------|--------|
|Angezeigter Preis in der Storefront|1000|1000|1000|
|Steuersatzprozentsatz|20|25|0|
|Preis an der Kasse|1200|1250|1000|

Shopify fügt lokale Steuern zu dem auf der Produktkarte definierten Preis hinzu, je nachdem, wohin die Waren geliefert werden.

## <a name="dynamic-tax-inclusive-pricing" />Dynamische Preise inklusive Steuern

Länder haben unterschiedliche Anforderungen für die Einbeziehung von Steuern in die Preise. Wenn Sie möchten, dass die Preise automatisch Steuern enthalten, können Sie [Dynamische Preise inklusive Steuern](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing) in Shopify aktivieren.

Wählen Sie in Ihrem **Shopify Admin** **Steuern basierend auf dem Land Ihres Debitors einschließen oder ausschließen** im Abschnitt **Andere Märkte – Präferenzen** der Einstellungen **[Märkte](https://www.shopify.com/admin/settings/markets)**.  

> [!NOTE]
> Diese Einstellung wirkt sich nicht auf die Darstellung von Preisen auf Inlandsmärkten aus, die vom Umschalter **Alle Preise verstehen sich inklusive Mehrwertsteuer** gesteuert wird.

### <a name="all-prices-include-tax-is-selected" />Alle Preise verstehen sich inklusive Mehrwertsteuer ist ausgewählt

|-|Inlandsverkäufe|Ausland, in dem die Steuer im Preis inbegriffen ist|Ausland, in dem die Steuer im Preis nicht inbegriffen ist|
|------------------------|--------|--------|--------|
|Angezeigter Preis in der Storefront|1200|1250|1000|
|Steuersatzprozentsatz|20|25|10|
|Preis an der Kasse|1200|1250|1100|

Der Preis für jeden Kunden ändert sich je nach Standort.

### <a name="all-prices-include-tax-is-not-selected" />Alle Preise verstehen sich inklusive Mehrwertsteuer ist nicht ausgewählt

|-|Inlandsverkäufe|Ausland, in dem die Steuer im Preis inbegriffen ist|Ausland, in dem die Steuer im Preis nicht inbegriffen ist|
|------------------------|--------|--------|--------|
|Angezeigter Preis in der Storefront|1000|1250|1000|
|Steuersatzprozentsatz|20|25|10|
|Preis an der Kasse|1200|1250|1100|

> [!NOTE]
> Der Schalter **Alle Preise verstehen sich inklusive Mehrwertsteuer** ändert nicht, wie Preise internationalen Debitoren angezeigt werden.

## <a name="if-you-sell-to-eu-customers" />Wenn Sie an EU-Debitoren verkaufen

Verschiedene EU-Länder haben unterschiedliche lokale Steuersätze. Wenn Sie jedoch in der EU ansässig sind und in andere EU-Länder verkaufen, können Sie in einigen Fällen Ihren lokalen Steuersatz verwenden.  

In Ihrem **Shopify Admin** aktivieren Sie das Kontrollkästchen **Mehrwertsteuer einbehalten** im Abschnitt **Europäische Union** in den Einstellungen [**Steuern und Zölle**](https://www.shopify.com/admin/settings/taxes).

|MwSt. einbehalten|MwSt.-Satz|
|-|-|
|Ausnahmeregelung für Kleinstunternehmen|Verwenden Sie Ihren inländischen Steuersatz für alle Verkäufe innerhalb der EU|
|One-Stop-Shop oder länderspezifische Registrierung|Verwenden Sie den Mehrwertsteuersatz des Landes Ihres Debitors|

### <a name="collect-vat-set-to-one-stop-shop-registration" />Sammeln Sie die Mehrwertsteuer, die auf die One-Stop-Shop-Registrierung eingestellt ist

Im folgenden Beispiel ist der Schalter **Alle Preise verstehen sich inklusive Mehrwertsteuer** aktiviert. Der Preis auf der Produktkarte ist auf *1200* gesetzt.

|-|Inlandsverkäufe|Ausland|
|------------------------|--------|--------|
|Angezeigter Preis in der Storefront|1200|1250|
|Steuersatzprozentsatz|20|25|
|Preis an der Kasse|1200|1250|

### <a name="collect-vat-set-to-micro-business-exemption" />MwSt. erheben ist auf Ausnahmeregelung für Kleinstunternehmen eingestellt

Im folgenden Beispiel ist der Schalter **Alle Preise verstehen sich inklusive Mehrwertsteuer** aktiviert. Der Preis auf der Produktkarte ist auf *1200* gesetzt.

|-|Inlandsverkäufe|Ausland mit lokalem Steuersatz von 25 Prozent.|
|------------------------|--------|--------|
|Angezeigter Preis in der Storefront|1200|1200|
|Steuersatzprozentsatz|20|20|
|Preis an der Kasse|1200|1200|

Shopify ignoriert bei der Berechnung der Endpreise den Steuersatz im Ausland und verwendet dafür den inländischen Steuersatz.

## <a name="importing-shopify-orders-sold-to-international-customers" />Importierender Shopify Bestellungen, die an internationale Debitoren verkauft wurden

Wenn Sie Steuern aus mehreren Ländern erheben, müssen Sie höchstwahrscheinlich eine länderspezifische Einstellung in [!INCLUDE[prod_short](../includes/prod_short.md)] definieren. Es gibt einen Grund, warum diese Einstellung erforderlich ist. Wenn ein Verkaufsbelegs in [!INCLUDE[prod_short](../includes/prod_short.md)], erstellt wird, berchnet [!INCLUDE [prod_short](../includes/prod_short.md)] Steuern, anstatt aus Shopify importierte Steuern wiederzuverwenden.

Länder-/regionsspezifische Einstellungen werden auf der Seite **Shopify Debitorenvorlage** ausgewählt. Dort können Sie die **Standarddebitorennr.** definieren oder **Debitorenvorlagennr.** Stellen Sie in jedem Fall sicher, dass für den ausgewählten Debitoren oder die ausgewählte Vorlage die folgenden Felder ausgefüllt sind:

1. **Allgemeine Geschäftsbuchungsgruppe** (für ausländische Debitoren verwendet).
2. **MwSt.-Geschäftsbuchungsgrp.** (für ausländische Debitoren verwendet).
3. **Preise inkl. MwSt** (ausgerichtet auf die Einstellung auf der Shopify Seite):

* Wählen Sie **Ja** aus, wenn **Alle Preise verstehen sich inklusive Mehrwertsteuer** aktiviert ist und **Steuern basierend auf dem Land Ihres Debitoren einschließen oder ausschließen** deaktiviert ist.
* Wählen Sie **Nein** aus, wenn **Alle Preise verstehen sich inklusive Mehrwertsteuer** deaktiviert ist und **Steuern basierend auf dem Land Ihres Debitoren einschließen oder ausschließen** deaktiviert ist.
* Wählen Sie **Ja** aus, wenn **Steuern basierend auf dem Land Ihres Debitoren einschließen oder ausschließen** aktiviert ist und das Land oder die Region in [Steuerpflichtige Länder](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions) aufgeführt ist.
* Wählen Sie **Nein** aus, wenn **Steuern basierend auf dem Land Ihres Debitoren einschließen oder ausschließen** aktiviert ist und das Land oder die Region nicht unter [Steuerpflichtige Länder](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions) aufgeführt ist.

> [!NOTE]
> Die Einstellung des Feldes **Preise inkl. MwSt** stammt aus der Vorlage, nicht aus dem konkreten Debitoren. Deshalb ist es wichtig, dass die Debitorenvorlage definiert ist.

## <a name="other-tax-remarks" />Sonstige Anmerkungen zu Steuern

Während die importierte Shopify-Bestellung Informationen zu Steuern enthält, werden die Steuern neu berechnet, wenn Sie den Verkaufsbeleg erstellen. Diese Neuberechnung bedeutet, dass es wichtig ist, dass die Einstellungen für Mehrwertsteuer/Steuern in [!INCLUDE[prod_short](../includes/prod_short.md)] richtig sind.

* Mehrere Produktsteuer- oder MwSt.-Steuersätze. Beispielsweise unterliegen einige Produktkategorien ermäßigten Steuersätzen. Sie können die [Steuerüberschreitung](https://help.shopify.com/en/manual/taxes/tax-overrides#create-a-manual-collection-for-products-that-need-a-tax-override) Funktion in Shopify verwenden. Beim Importieren und Erstellen von Elementen in [!INCLUDE[prod_short](../includes/prod_short.md)] verwenden sie die Steuereinstellungen, die im Artikelvorlagencode in Shopify Shop eingegeben wurden. Bevor Sie Bestellungen mit solchen Artikeln importieren, müssen Sie die Umsatzsteuer-Produktbuchungsgruppe aktualisieren.  
* Adressabhängige Steuersätze. Verwenden Sie das Feld **Steuergebiet Priorität** zusammen mit der Tabelle **Kundenvorlagen**, um die Standardlogik zu überschreiben, die den **Steuergebietscode** im Verkaufsdokument ausfüllt. Das Feld **Steuergebiet Priorität** gibt die Priorität an, aus der die Funktion die Informationen über das Land oder die Region und den Staat oder die Provinz übernehmen soll. Dann wird der entsprechende Datensatz in den Kundenvorlagen Shopify identifiziert und die **Steuerkennziffer**, **Steuerpflichtig** und **MwSt Bus. Buchungsgruppe** werden verwendet, wenn ein Verkaufsbeleg erstellt wird.  

## <a name="see-also" />Siehe auch

[Einstieg mit dem Konnektor für Shopify](get-started.md)  
