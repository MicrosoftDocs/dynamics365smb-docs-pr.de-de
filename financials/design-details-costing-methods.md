---
title: 'Designdetails: Kostenmethoden | Microsoft Docs'
description: "Die Lagerabgangsmethode legt fest, ob ein tatsächlicher oder ein budgetierter Wert gebucht und in der Berechnung des Einstandspreises verwendet werden soll. Zusammen mit dem Buchungsdatum und der -reihenfolge beeinflusst die Lagerabgangsmethode auch, wie der Kostenfluss aufgezeichnet wird."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a968ba404a3ff0bdee3aa98039a1f8c50a193c08
ms.contentlocale: de-de
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-costing-methods"></a>Designdetails: Kostenberechnungsmethoden
Die Lagerabgangsmethode legt fest, ob ein tatsächlicher oder ein budgetierter Wert gebucht und in der Berechnung des Einstandspreises verwendet werden soll. Zusammen mit dem Buchungsdatum und der -reihenfolge beeinflusst die Lagerabgangsmethode auch, wie der Kostenfluss aufgezeichnet wird. Die folgenden Methoden werden in [!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt:  

|Lagerabgangsmethode|Description|Anwendungsbeispiele|  
|--------------------|---------------------------------------|-----------------|  
|FIFO|Der Einstandspreis eines Artikels ist der tatsächliche Wert jedes Eingangs des Artikels, nach der FIFO-Regel ausgewählt.<br /><br /> In der Lagerbewertung wird angenommen, dass die ersten Artikel, die im Lager platziert sind, zuerst verkauft werden.|In Unternehmensumgebungen, in denen die Produktkosten stabil sind.<br /><br /> Wenn Preise steigen, zeigt die Bilanz größeren Wert. Das bedeutet, dass Steuerverbindlichkeiten zunehmen, aber die Bonität und die Möglichkeit, Bargeld zu borgen verbessert sich.<br /><br /> Verwendung für Artikel mit einem begrenzten Haltbarkeitsdatum, da die ältesten Waren verkauft werden müssen, bevor sie ihr Mindesthaltbarkeitsdatum überschreiten.|  
|LIFO|Der Einstandspreis eines Artikels ist der tatsächliche Wert jedes Eingangs des Artikels, nach der LIFO-Regel ausgewählt.<br /><br /> In der Lagerbewertung wird angenommen, dass die letzten Artikel, die im Lager platziert sind, zuerst verkauft werden.|Nicht zugelassen in vielen Ländern/Regionen, da es verwendet werden kann, um den Deckungsbeitrag zu drücken.<br /><br /> Wenn Preise steigen, reduziert sich der Wert in den GuV-Konten. Das bedeutet, dass Steuerverbindlichkeiten abnehmen, aber die Möglichkeit, Bargeld zu borgen verschlechtert sich.|  
|Durchschnitt|Der Einstandspreis eines Artikels wird, wie der durchschnittliche Einstandspreis, an jedem Zeitpunkt nach einem Kauf berechnet.<br /><br /> Für Lagerbewertung setzt man voraus, dass alle Bestände gleichzeitig verkauft werden.|In Unternehmensumgebungen, in denen die Produktkosten nicht stabil sind.<br /><br /> Vorgehensweise bei gestapelten oder miteinander kombinierten Beständen, die nicht unterschieden werden können, wie z.B. bei Chemikalien.|  
|Ausgewählt|Der Einstandspreis eines Artikels sind die exakten Kosten, an denen die bestimmte Einheit empfangen wurden.|Verwendung in der Produktion oder Handel von einfach identifizierbaren Artikeln mit sehr hohen Einstandspreis.<br /><br /> Für Artikel, die Zu-/Abschlägen unterliegen.<br /><br /> Verwendung für Artikel mit Seriennummern.|  
|Standard|Der Einstandspreis eines Artikels ist voreingestellt basierend auf vorkalkulierten Kosten.<br /><br /> Wenn die Ist-Kosten später realisiert werden, muss der Einstandspreis (fest) auf die Ist-Kosten durch Abweichungswerte reguliert werden.|Wird verwendet, wo Kostenkontrolle kritisch ist.<br /><br /> In der wiederholenden Produktion zu verwenden, um die Kosten des Fertigungsmaterials, direkte Arbeit und Produktionsgemeinkosten zu bewerten.<br /><br /> Wird verwendet, wo es Kategorie und Mitarbeiter gibt, um die Vorgaben beizubehalten.|  

 Die folgenden Bild zeigt, wie Kosten für jede Kostenbewertungsmethode den Bestand durchlaufen.  

 ![Kostenmethoden](media/design_details_inventory_costing_7_costing_methods.png "design_details_inventory_costing_7_costing_methods")  

 Kostenberechnungsmethoden unterscheiden sich in der Art, wie sie Lagerabgänge bewerten und dahingehend, ob sie Ist-Kosten oder Standardkosten als Bewertungsbasis verwenden. Die verschiedenen Eigenschaften werden in der folgenden Tabelle beschrieben. (Die LIFO-Methode ist ausgeschlossen, da diese der FIFO-Methode sehr ähnlich ist)  

||FIFO|Durchschnitt|Standard|Ausgewählt|  
|-|----------|-------------|--------------|--------------|  
|Allgemeine Eigenschaft|Einfach zu verstehen|Basierend auf Periodenoptionen: **Tag**/**Woche**/**Monat**/**Quartal**/**Buchhaltungsperiode**.<br /><br /> Kann pro Artikel oder pro Artikel/Lagerort/Variante berechnet werden.|Bedienungsfreundlich, benötigt jedoch qualifizierte Wartung.|Erfordert Artikelverfolgung auf der eingehenden und ausgehenden Transaktion.<br /><br /> Normalerweise verwendet für serialisierte Artikel.|  
|Anwendung/Regulierung|Anwendung verfolgt **die Restmenge**.<br /><br /> Die Regulierung überträgt Kosten je nach Mengenanwendung vorwärts.|Anwendung verfolgt die **Restmenge**.<br /><br /> Kosten werden nach **Bewertungsdatum** berechnet und weitergeleitet.|Anwendung verfolgt die **Restmenge**.<br /><br /> Anwendung basiert auf "FIFO".|Alle Augleiche sind fest.|  
|Neubewertung|Bewertet nur die fakturierte Menge neu.<br /><br /> Kann pro Artikel oder pro Artikelposten durchgeführt werden.<br /><br /> Kann rückwirkend geschehen.|Bewertet nur die fakturierte Menge neu.<br /><br /> Kann nur pro Artikel durchgeführt werden.<br /><br /> Kann rückwirkend geschehen.|Bewertet fakturierte und nicht fakturierte Mengen neu.<br /><br /> Kann pro Artikel oder pro Artikelposten durchgeführt werden.<br /><br /> Kann rückwirkend geschehen.|Bewertet nur die fakturierte Menge neu.<br /><br /> Kann pro Artikel oder pro Artikelposten durchgeführt werden.<br /><br /> Kann rückwirkend geschehen.|  
|Sonstiges|Wenn Sie eine Bestandsminderung zurückdatieren, werden bestehende Posten NICHT erneut ausgeglichen, um einen korrekten FIFO-Kostenfluss bereitzustellen.|Wenn Sie eine Bestandserhöhung oder -minderung zurückdatieren, werden die Durchschnittskosten erneut berechnet, und alle betroffenen Posten werden angepasst.<br /><br /> Wenn Sie die Periode oder Berechnungsart ändern, müssen alle betroffenen Posten reguliert werden.|Verwenden Sie das **Standardarbeitsblatt**-Fenster, um Einstandspreise (fest) in regelmäßigen Abständen zu aktualisieren und der zu ermitteln.<br /><br /> Wird NICHT pro SKU unterstützt.<br /><br /> Keine historischen Datensätze für Einstandspreise vorhanden.|Sie können eine bestimmte Artikelverfolgung verwenden, ohne die bestimmte Lagerabgangsmethode zu verwenden. Dann folgen die Kosten NICHT der Chargennummer, sondern der Kosten-Annahme der ausgewählten Bewertungsmethode.|  

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
>  Die resultierende Menge im Bestand ist Null. Aus diesem Grund muss der Lagerwert, unabhängig von der Kostenberechnungsmethode, auch Null sein.  

### <a name="effect-of-costing-methods-on-valuing-inventory-increases"></a>Auswirkungen der Kostenbewertungsmethoden auf die Bewertung von Lagerzugängen  
 **FIFO**/**LIFO**/**Durchschnitt**/**Spezifisch**  

 Für Artikel mit Kostenberechnungsmethoden, die die Ist-Kosten als Bewertungsbasis verwenden (**FIFO**, **LIFO**, **Durchschnitt** oder **Spezifisch**) werden Bestandserhöhungen anhand der Anschaffungskosten des Artikels bewertet.  

 Die nachstehende Tabelle zeigt, wie Bestandsminderungen für alle Kostenberechnungsmethoden, mit Ausnahme von **Standard**, bewertet werden.  

|Buchungsdatum|Menge|Einstandsbetrag (tatsächl.)|Lfd. Nr.|  
|------------------|--------------|----------------------------|---------------|  
|01-01-20|1|10,00|1|  
|01-01-20|1|20,00|2|  
|01-01-20|1|30,00|3|  

 **Standard**  

 Bei der Lagerabgangsmethode **Standard** werden Lagerzugänge mit den aktuellen Standardkosten des Artikels bewertet.  

 Die nachstehende Tabelle zeigt, wie Bestandserhöhungen für die Kostenberechnungsmethode **Standard** bewertet werden.  

|Buchungsdatum|Menge|Einstandsbetrag (tatsächl.)|Lfd. Nr.|  
|------------------|--------------|----------------------------|---------------|  
|01-01-20|1|15.00|1|  
|01-01-20|1|15.00|2|  
|01-01-20|1|15.00|3|  

### <a name="effect-of-costing-methods-on-valuing-inventory-decreases"></a>Auswirkungen der Kostenbewertungsmethoden auf die Bewertung von Lagerabgängen  
 **FIFO**  

 Für Artikel mit der Kostenberechnungsmethode **FIFO** werden Artikel, die zuerst eingekauft wurden, immer zuerst verkauft (in diesem Beispiel die Postennummern 3, 2 und 1). Entsprechend gilt: Lagerabgänge werden durch den Wert des ersten Lagerzugangs bewertet.  

 Lagerverbrauch wird mithilfe des Werts der ersten Bestandsdatenerfassungen berechnet.  

 Die nachstehende Tabelle zeigt, wie Bestandsminderungen für die Kostenberechnungsmethode **FIFO** bewertet werden.  

|Buchungsdatum|Menge|Einstandsbetrag (tatsächl.)|Lfd. Nr.|  
|------------------|--------------|----------------------------|---------------|  
|02-01-20|-1|-10.00|4|  
|03-01-20|-1|-20.00|5|  
|04-01-20|-1|-30.00|6|  

 **LIFO**  

 Für Artikel mit der Kostenberechnungsmethode **LIFO** werden Artikel, die zuletzt eingekauft wurden, immer zuerst verkauft (in diesem Beispiel die Postennummern 3, 2 und 1). Entsprechend gilt: Lagerabgänge werden durch den Wert des letzten Lagerzugangs bewertet.  

 Lagerverbrauch wird mithilfe des Werts der neuesten Bestandsdatenerfassungen berechnet.  

 Die nachstehende Tabelle zeigt, wie Bestandsminderungen für die Kostenberechnungsmethode **LIFO** bewertet werden.  

|Buchungsdatum|Menge|Einstandsbetrag (tatsächl.)|Lfd. Nr.|  
|------------------|--------------|----------------------------|---------------|  
|02-01-20|-1|-30.00|4|  
|03-01-20|-1|-20.00|5|  
|04-01-20|-1|-10.00|6|  

 **Durchschnitt**  

 Die Lagerabgangsmethode **Durchschnitt** bewertet einen Lagerabgang, indem sie den gewogenen Durchschnitt des verbleibenden Lagerbestandes zum Bewertungsdatum auf den Lagerabgang überträgt. Weitere Informationen finden Sie unter [Designdetails: Durchschnittliche Kosten](design-details-average-cost.md)  

 Die nachstehende Tabelle zeigt, wie Bestandsminderungen für die Kostenberechnungsmethode **Durchschnitt** bewertet werden.  

|Buchungsdatum|Menge|Einstandsbetrag (tatsächl.)|Lfd. Nr.|  
|------------------|--------------|----------------------------|---------------|  
|02-01-20|-1|-20.00|4|  
|03-01-20|-1|-20.00|5|  
|04-01-20|-1|-20.00|6|  

 **Standard**  

 Für Artikel mit der Kostenberechnungsmethode **Standard** werden Bestandserhöhungen ähnlich wie bei der Kostenberechnungsmethode **FIFO** bewertet, außer dass die Bewertung auf Standardkosten basiert, nicht auf den Ist-Kosten.  

 Die nachstehende Tabelle zeigt, wie Bestandsminderungen für die Kostenberechnungsmethode **Standard** bewertet werden.  

|Buchungsdatum|Menge|Einstandsbetrag (tatsächl.)|Lfd. Nr.|  
|------------------|--------------|----------------------------|---------------|  
|02-01-20|-1|-15.00|4|  
|03-01-20|-1|-15.00|5|  
|04-01-20|-1|-15.00|6|  

 **Ausgewählt**  

 Die Lagerabgangsmethoden bringen die Annahme zum Ausdruck, dass die Kosten von Lagerzugängen zu Lagerabgängen fließen. Wenn genauere Informationen über den Kostenfluss vorliegen, können Sie diese Annahme jedoch überschreiben, indem Sie einen festen Ausgleich zwischen Posten erstellen. Eine feste Anwendung erstellt eine Verknüpfung zwischen einem Lagerabgang und einem bestimmten Lagerzugang und leitet den Kostenfluss entsprechend.  

 Für Artikel mit der Kostenberechnungsmethode **Spezifisch** werden Bestandsminderungen entsprechend der Bestandserhöhung bewertet, mit der sie durch den festen Ausgleich verknüpft sind.  

 Die nachstehende Tabelle zeigt, wie Bestandsminderungen für die Kostenberechnungsmethode **Spezifisch** bewertet werden.  

|Buchungsdatum|Menge|Einstandsbetrag (tatsächl.)|Ausgleich mit Lfd. Nr.|Lfd. Nr.|  
|------------------|--------------|----------------------------|-----------------------|---------------|  
|02-01-20|-1|-20.00|**2**|4|  
|03-01-20|-1|-10.00|**1**|5|  
|04-01-20|-1|-30.00|**3**|6|  

## <a name="see-also"></a>Siehe auch  
 [Designdetails: Lagerkostenberechnung](design-details-inventory-costing.md)   
 [Designdetails: Abweichung](design-details-variance.md)   
 [Designdetails: Durchschnittskosten](design-details-average-cost.md)   
 [Designdetails: Artikelanwendung](design-details-item-application.md) [Verwalten der Lagerkosten](finance-manage-inventory-costs.md)  
 [Finanzen](finance.md)  
 [Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

