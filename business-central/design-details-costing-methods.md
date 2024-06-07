---
title: 'Designdetails: Kostenberechnungsmethoden'
description: 'Dieses Thema beschreibt, wie sich die Kalkulationsmethode darauf auswirkt, wie Ist- und Planwerte kapitalisiert und in der Kostenkalkulation verwendet werden.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 05/12/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="design-details-costing-methods"></a>Designdetails: Kostenberechnungsmethoden

Die Lagerabgangsmethode legt fest, ob ein tatsächlicher oder ein budgetierter Wert gebucht und in der Berechnung des Einstandspreises verwendet werden soll. Zusammen mit dem Buchungsdatum und der -reihenfolge beeinflusst die Lagerabgangsmethode auch, wie der Kostenfluss aufgezeichnet wird.

> [!NOTE]
> Sie können die Lagerabgangsmethode eines Artikels nicht ändern, wenn Artikelposten für den Artikel vorhanden sind. Weitere Informationen finden Sie unter [Enwurfsdetails: Die Lagerabgangsmethode für Artikel ändern](design-details-changing-costing-methods.md).

Die folgenden Methoden werden in [!INCLUDE[prod_short](includes/prod_short.md)] unterstützt:  

| Lagerabgangsmethode | Beschreibung | Anwendungsbeispiele |
|--|--|--|
| FIFO | Der Einstandspreis eines Artikels ist der tatsächliche Wert jedes Eingangs des Artikels, nach der FIFO-Regel ausgewählt.<br /><br /> In der Lagerbewertung wird angenommen, dass die ersten Artikel, die im Lager platziert sind, zuerst verkauft werden. | In Unternehmensumgebungen, in denen die Produktkosten stabil sind.<br /><br /> Wenn Preise steigen, zeigt die Bilanz größeren Wert. Das bedeutet, dass Steuerverbindlichkeiten zunehmen, aber die Bonität und die Möglichkeit, Bargeld zu borgen verbessert sich.<br /><br /> Verwendung für Artikel mit einem begrenzten Haltbarkeitsdatum, da die ältesten Waren verkauft werden müssen, bevor sie ihr Mindesthaltbarkeitsdatum überschreiten. |
| LIFO | Der Einstandspreis eines Artikels ist der tatsächliche Wert jedes Eingangs des Artikels, nach der LIFO-Regel ausgewählt.<br /><br /> In der Lagerbewertung wird angenommen, dass die letzten Artikel, die im Lager platziert sind, zuerst verkauft werden. | Nicht zugelassen in vielen Ländern/Regionen, da es verwendet werden kann, um den Deckungsbeitrag zu drücken.<br /><br /> Wenn Preise steigen, reduziert sich der Wert in den GuV-Konten. Das bedeutet, dass Steuerverbindlichkeiten abnehmen, aber die Möglichkeit, Bargeld zu borgen verschlechtert sich. |
| Durchschnitt | Der Einstandspreis eines Artikels wird, wie der durchschnittliche Einstandspreis, an jedem Zeitpunkt nach einem Kauf berechnet.<br /><br /> Für Lagerbewertung setzt man voraus, dass alle Bestände gleichzeitig verkauft werden. | In Unternehmensumgebungen, in denen die Produktkosten nicht stabil sind.<br /><br /> Vorgehensweise bei gestapelten oder miteinander kombinierten Beständen, die nicht unterschieden werden können, wie z.B. bei Chemikalien. |
| Ausgewählt | Der Einstandspreis eines Artikels sind die exakten Kosten, zu denen die bestimmte Einheit empfangen wurden. | Verwendung in der Produktion oder Handel von einfach identifizierbaren Artikeln mit sehr hohen Einstandspreis.<br /><br /> Für Artikel, die Zu-/Abschlägen unterliegen.<br /><br /> Verwendung für Artikel mit Seriennummern. |
| Standard | Der Einstandspreis eines Artikels ist voreingestellt basierend auf vorkalkulierten Kosten.<br /><br /> Wenn die Ist-Kosten später realisiert werden, muss der Einstandspreis (fest) auf die Ist-Kosten durch Abweichungswerte reguliert werden. | Wird verwendet, wo Kostenkontrolle kritisch ist.<br /><br /> In der wiederholenden Produktion zu verwenden, um die Kosten des Fertigungsmaterials, direkte Arbeit und Produktionsgemeinkosten zu bewerten.<br /><br /> Wird verwendet, wo es Kategorie und Mitarbeiter gibt, um die Vorgaben beizubehalten. |

Die folgenden Bild zeigt, wie Kosten für jede Kostenbewertungsmethode den Bestand durchlaufen.  

![Kalkulationsmethoden visualisiert.](media/design_details_inventory_costing_7_costing_methods.png "Kalkulationsmethoden visualisiert")  

Kostenberechnungsmethoden unterscheiden sich in der Art, wie sie Lagerabgänge bewerten und dahingehend, ob sie Ist-Kosten oder Standardkosten als Bewertungsbasis verwenden. Die verschiedenen Eigenschaften werden in der folgenden Tabelle beschrieben. (Die LIFO-Methode ist ausgeschlossen, da diese der FIFO-Methode sehr ähnlich ist)  
<!--Old  table
|Category|FIFO|Average|Standard|Specific|  
|-|----------|-------------|--------------|--------------|  
|General characteristic|Easy to understand|Based on period options: **Day**/**Week**/**Month**/**Quarter**/**Accounting Period**.<br /><br /> Can be calculated per item or per item/location/variant.|Easy to use, but requires qualified maintenance.|Requires item tracking on both inbound and outbound transaction.<br /><br /> Typically used for serialized items.|  
|Application/Adjustment|Application keeps track of **the remaining quantity**.<br /><br /> Adjustment forwards costs according to quantity application.|Application keeps track of the **remaining quantity**.<br /><br /> Costs are calculated and forwarded per the **valuation date**.|Application keeps track of the **remaining quantity**.<br /><br /> Application is based on FIFO.|All applications are fixed.|  
|Revaluation|Revalues invoiced quantity only.<br /><br /> Can be done per item or per item ledger entry.<br /><br /> Can be done backward in time.|Revalues invoiced quantity only.<br /><br /> Can be done per item only.<br /><br /> Can be done backward in time.|Revalues invoiced and un-invoiced quantities.<br /><br /> Can be done per item or per item ledger entry.<br /><br /> Can be done backward in time.|Revalues invoiced quantity only.<br /><br /> Can be done per item or per item ledger entry.<br /><br /> Can be done backward in time.|  
|Miscellaneous|If you back-date an inventory decrease, then existing entries are NOT reapplied to provide a correct FIFO cost flow.|If you back-date an inventory increase or decrease, then the average cost is recalculated, and all affected entries are adjusted.<br /><br /> If you change the period or calculation type, then all affected entries must be adjusted.|Use the **Standard Worksheet** page to periodically update and roll up standard costs.<br /><br /> Is NOT supported per SKU.<br /><br /> No historic records exist for standard costs.|You can use specific item tracking without using the Specific costing method. Then the cost will NOT follow the lot number, but the cost assumption of the selected costing method.|  
-->
<!--Table flipped for slightly better readability -->

||Allgemeine Eigenschaft|Anwendung/Regulierung |Neubewertung|Sonstiges |
|-|---------|---------|---------|---------|
|**FIFO**     |Einfach zu verstehen|Anwendung verfolgt **die Restmenge**.<br /><br /> Die Regulierung überträgt Kosten je nach Mengenanwendung vorwärts. |Bewertet nur die fakturierte Menge neu.<br /><br /> Kann pro Artikel oder pro Artikelposten durchgeführt werden.<br /><br /> Kann rückwirkend geschehen.|Wenn Sie eine Bestandsminderung zurückdatieren, werden bestehende Posten NICHT erneut ausgeglichen, um einen korrekten FIFO-Kostenfluss bereitzustellen.|
|**Durchschnitt**     |Basierend auf Periodenoptionen: **Tag**/**Woche**/**Monat**/**Quartal**/**Buchhaltungsperiode**.<br /><br /> Kann pro Artikel oder pro Artikel/Lagerort/Variante berechnet werden.|Anwendung verfolgt die **Restmenge**.<br /><br /> Kosten werden nach **Bewertungsdatum** berechnet und weitergeleitet. |Bewertet nur die fakturierte Menge neu.<br /><br /> Kann nur pro Artikel durchgeführt werden.<br /><br /> Kann rückwirkend geschehen. |Wenn Sie eine Bestandserhöhung oder -minderung zurückdatieren, werden die Durchschnittskosten erneut berechnet, und alle betroffenen Posten werden angepasst.<br /><br /> Wenn Sie die Periode oder Berechnungsart ändern, müssen alle betroffenen Posten reguliert werden.|
|**Standard**     |Bedienungsfreundlich, benötigt jedoch qualifizierte Wartung.|Anwendung verfolgt die **Restmenge**.<br /><br /> Anwendung basiert auf "FIFO".|Bewertet fakturierte und nicht fakturierte Mengen neu.<br /><br /> Kann pro Artikel oder pro Artikelposten durchgeführt werden.<br /><br /> Kann rückwirkend geschehen.|Verwenden Sie das **Standardarbeitsblatt**-Fenster, um Einstandspreise (fest) in regelmäßigen Abständen zu aktualisieren und der zu ermitteln.<br /><br /> Wird NICHT pro SKU unterstützt.<br /><br /> Keine historischen Datensätze für Einstandspreise vorhanden.|
|**Spezifisch**     |Erfordert Artikelverfolgung auf der eingehenden und ausgehenden Transaktion.<br /><br /> Normalerweise verwendet für serialisierte Artikel.|Alle Augleiche sind fest.|Bewertet nur die fakturierte Menge neu.<br /><br /> Kann pro Artikel oder pro Artikelposten durchgeführt werden.<br /><br /> Kann rückwirkend geschehen.|Sie können eine bestimmte Artikelverfolgung verwenden, ohne die bestimmte Lagerabgangsmethode zu verwenden. Dann folgen die Kosten NICHT der Chargennummer, sondern der Kosten-Annahme der ausgewählten Bewertungsmethode.|

## <a name="example"></a>Beispiel

Dieser Abschnitt nennt Beispiele, wie unterschiedliche Lagerabgangsmethoden sich auf den Lagerwert auswirken.  

Die folgende Tabelle zeigt die Bestandserhöhungen und -minderungen, auf denen die Beispiele basieren.  

|Buchungsdatum|Menge|Lfd. Nr.|  
|------------------|--------------|---------------|  
|01-01-20|1|1|  
|01-01-20|1|2|  
|01-01-20|1|3|  
|02-01-20|-1|4|  
|03-01-20|-1|5|  
|04-01-20|-1|6|  

> [!NOTE]  
> Die resultierende Menge im Bestand ist Null. Aus diesem Grund muss der Lagerwert, unabhängig von der Kostenberechnungsmethode, auch Null sein.  

### <a name="effect-of-costing-methods-on-valuing-inventory-increases"></a>Auswirkungen der Kostenbewertungsmethoden auf die Bewertung von Lagerzugängen

Für Artikel mit Kostenberechnungsmethoden, die die Ist-Kosten als Bewertungsbasis verwenden (**FIFO**, **LIFO**, **Durchschnitt** oder **Spezifisch**) werden Bestandserhöhungen anhand der Anschaffungskosten des Artikels bewertet.  

- **Standard**  

    Bei der Lagerabgangsmethode **Standard** werden Lagerzugänge mit den aktuellen Standardkosten des Artikels bewertet.  

#### <a name="standard"></a>Standard

Bei der Lagerabgangsmethode **Standard** werden Lagerzugänge mit den aktuellen Standardkosten des Artikels bewertet.  

### <a name="effect-of-costing-methods-on-valuing-inventory-decreases"></a>Auswirkungen der Kostenbewertungsmethoden auf die Bewertung von Lagerabgängen

- **FIFO**  

    Für Artikel mit der Kostenberechnungsmethode **FIFO** werden Artikel, die zuerst eingekauft wurden, immer zuerst verkauft (in diesem Beispiel die Postennummern 3, 2 und 1). Entsprechend gilt: Lagerabgänge werden durch den Wert des ersten Lagerzugangs bewertet.  

     Lagerverbrauch wird mithilfe des Werts der ersten Bestandsdatenerfassungen berechnet.  

     Die nachstehende Tabelle zeigt, wie Bestandsminderungen für die Kostenberechnungsmethode **FIFO** bewertet werden.  

    |Buchungsdatum|Menge|Einstandsbetrag (tatsächl.)|Lfd. Nr.|  
    |------------------|--------------|----------------------------|---------------|  
    |02-01-20|-1|-10.00|4|  
    |03-01-20|-1|-20.00|5|  
    |04-01-20|-1|-30.00|6|  

- **LIFO**  

    Für Artikel mit der Kostenberechnungsmethode **LIFO** werden Artikel, die zuletzt eingekauft wurden, immer zuerst verkauft (in diesem Beispiel die Postennummern 3, 2 und 1). Entsprechend gilt: Lagerabgänge werden durch den Wert des letzten Lagerzugangs bewertet.  

     Lagerverbrauch wird mithilfe des Werts der neuesten Bestandsdatenerfassungen berechnet.  

     Die nachstehende Tabelle zeigt, wie Bestandsminderungen für die Kostenberechnungsmethode **LIFO** bewertet werden.  

    |Buchungsdatum|Menge|Einstandsbetrag (tatsächl.)|Lfd. Nr.|  
    |------------|--------|--------------------|---------|  
    |02-01-20|-1|-30.00|4|  
    |03-01-20|-1|-20.00|5|  
    |04-01-20|-1|-10.00|6|  

- **Durchschnitt**  

    Die Lagerabgangsmethode **Durchschnitt** bewertet einen Lagerabgang, indem sie den gewogenen Durchschnitt des verbleibenden Lagerbestandes zum Bewertungsdatum auf den Lagerabgang überträgt. Weitere Informationen finden Sie unter [Designdetails: Durchschnittliche Kosten](design-details-average-cost.md)  

     Die nachstehende Tabelle zeigt, wie Bestandsminderungen für die Kostenberechnungsmethode **Durchschnitt** bewertet werden.  

    | Buchungsdatum | Menge | Einstandsbetrag (tatsächl.) | Lfd. Nr. |
    |--|--|--|--|
    | 02-01-20 | -1 | -20.00 | 4 |
    | 03-01-20 | -1 | -20.00 | 5 |
    | 04-01-20 | -1 | -20.00 | 6 |

- **Standard**  

    Für Artikel mit der Kostenberechnungsmethode **Standard** werden Bestandserhöhungen ähnlich wie bei der Kostenberechnungsmethode **FIFO** bewertet, außer dass die Bewertung auf Standardkosten basiert, nicht auf den Ist-Kosten.  

    Die nachstehende Tabelle zeigt, wie Bestandsminderungen für die Kostenberechnungsmethode **Standard** bewertet werden.  

    |Buchungsdatum|Menge|Einstandsbetrag (tatsächl.)|Lfd. Nr.|  
    |------------------|--------------|----------------------------|---------------|  
    |02-01-20|-1|-15.00|4|  
    |03-01-20|-1|-15.00|5|  
    |04-01-20|-1|-15.00|6|  

- **Ausgewählt**  

    Die Lagerabgangsmethoden bringen die Annahme zum Ausdruck, dass die Kosten von Lagerzugängen zu Lagerabgängen fließen. Wenn genauere Informationen über den Kostenfluss vorliegen, können Sie diese Annahme jedoch überschreiben, indem Sie einen festen Ausgleich zwischen Posten erstellen. Eine feste Anwendung erstellt eine Verknüpfung zwischen einem Lagerabgang und einem bestimmten Lagerzugang und leitet den Kostenfluss entsprechend.  

    Für Artikel mit der Kostenberechnungsmethode **Spezifisch** werden Bestandsminderungen entsprechend der Bestandserhöhung bewertet, mit der sie durch den festen Ausgleich verknüpft sind.  

    Die nachstehende Tabelle zeigt, wie Bestandsminderungen für die Kostenberechnungsmethode **Spezifisch** bewertet werden.  

    |Buchungsdatum|Menge|Einstandsbetrag (tatsächl.)|Ausgleich mit Lfd. Nr.|Lfd. Nr.|
    |------------|--------|--------------------|----------------|---------|  
    |02-01-20|-1|-20.00|**2**|4|  
    |03-01-20|-1|-10.00|**1**|5|  
    |04-01-20|-1|-30.00|**3**|6|  

## <a name="see-also"></a>Siehe auch

[Designdetails: Lagerbewertung](design-details-inventory-costing.md)  
[Designdetails: Abweichung](design-details-variance.md)  
[Designdetails: Einstandspreis](design-details-average-cost.md)  
[Designdetails: Artikelausgleich](design-details-item-application.md)  
[Verwalten der Bestandsregulierung](finance-manage-inventory-costs.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Glossar der Begriffe in Dynamics 365-Geschäftsprozessen](/dynamics365/guidance/business-processes/glossary)  
[Einen Überblick Nachkalkulation für Produkte und Dienstleistungen festlegen](/dynamics365/guidance/business-processes/product-service-define-cost-overview)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
