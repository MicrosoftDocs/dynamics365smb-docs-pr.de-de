---
title: Bestandsanalyse
description: 'Business Central enthält viele Features, mit denen Sie wertvolle Bestandsdaten für Business Intelligence und Entscheidungsfindung in Ihrer Organisation sammeln, analysieren und gemeinsam nutzen können.'
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 05/03/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="inventory-analytics"></a>Bestandsanalyse

Unternehmen erfassen im Laufe ihrer täglichen Arbeit eine Menge Daten, die wertvolle Business Intelligence (BI) für Bestandsführungskräfte liefern:

- Versand der Waren, wenn Verkaufsaufträge erfüllt werden.
- Eingang von Artikeln, wenn Bestellungen erfüllt werden.
- Umlagerungen von Artikeln zwischen Lagerorten.

[!INCLUDE[prod_short](includes/prod_short.md)] bietet viele Features, die Ihnen helfen, Bestandsdaten Ihrer Organisation zu erfassen, zu analysieren und weiterzugeben:

- Ad-hoc-Analyse von Listen
- Ad-hoc-Analyse von Daten in Excel (über „In Excel öffnen“)
- Integrierte Tools zur Bestandsanalyse
- Integrierte Bestandsberichte

Jedes dieser Features hat Vor- und Nachteile, die von der Art der Datenanalyse und der Rolle der Benutzenden abhängen. Weitere Informationen finden Sie unter [Analysen, Business Intelligence und Berichterstellung – Übersicht](reports-bi-reporting.md).

Dieser Artikel erklärt, wie Sie diese Analysefeatures nutzen können, um Erkenntnisse zu Ihrem Bestand zu gewinnen.

## <a name="analytics-needs-in-inventory"></a>Analyseanforderungen im Lager

Wenn Sie über Analyseanforderungen in der Lagerverwaltung nachdenken, kann es hilfreich sein, ein auf Personas basierendes Modell zu verwenden, das verschiedene Analyseanforderungen allgemein beschreibt.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Darstellung verschiedener Personas für die Analyse" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Mitarbeitende in unterschiedlichen Rollen haben unterschiedliche Anforderungen an die Daten und nutzen die Daten auf unterschiedliche Weise. Beispielsweise interagieren Mitarbeitende in der Anlagenverwaltung und im Finanzbereich anders mit Daten als im Vertrieb.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Abbildung, die zeigt, das verschiedene Personas unterschiedliche Analyseanforderungen haben." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Rolle              | Datenaggregation  | Übliche Arten zur Datennutzung                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|COO, CFO, CEO    | Leistungsdaten  | KPIs, Dashboards, Finanzberichte           |
|Lagerverwalter  | Trends, Zusammenfassungen | Integrierte Managementberichte, Ad-hoc-Analyse      | 
|Lagermitarbeitende   | Detaillierte Daten     | Integrierte betriebliche Berichte, Aufgabendaten auf dem Bildschirm |

<!-- 
## <a name="inventory-kpis"></a>Inventory KPIs

A key performance indicator (KPI) is a measurable value that shows how effectively you’re meeting your goals. In inventory management, people often use the following KPIs to monitor their organization's sales performance:

- TODO  
-->

## <a name="use-financial-reporting-to-produce-financial-statements-and-kpis-related-to-inventory"></a>Finanzberichte für die Erstellung von mit dem Bestand zusammenhängenden Finanzauswertungen und KPIs verwenden

Das Feature **Finanzberichterstattung** gibt Ihnen Einblick in die in Ihrem Kontenplan (COA) enthaltenen Finanzdaten. Sie können Finanzberichte einrichten, um die Zahlen in den Sachkonten zu analysieren und Sachposten mit Budgetposten zu vergleichen. Speziell für die Lagerverwaltung können Sie Finanzberichte zu den Sachkonten einrichten, die Sie zum Verfolgen von Bestandsbuchungen verwenden.

Dimensionen spielen eine wichtige Rolle bei Business Intelligence. Bei einer Dimension handelt es sich um Daten, die Sie einem Eintrag als Parameter hinzufügen. Mit Dimensionen können Sie Einträge mit ähnlichen Merkmalen gruppieren, z. B. Debitoren, Regionen, Produkte und Verkaufende. Sie verwenden Dimensionen u. a. bei der Festlegung von Analyseansichten und beim Erstellen von Finanzberichten. Unter [Arbeiten mit Dimensionen](finance-dimensions.md) erfahren Sie mehr.

Erfahren Sie mehr unter Finanzberichte unter [Finanzberichte mit Finanzdaten und Kontenkategorien erstellen](bi-how-work-account-schedule.md).

## <a name="finance-reporting-across-business-units-or-legal-entities-related-to-inventory"></a>Finanzberichte über Konzernmandanten oder juristische Personen hinweg (im Zusammenhang mit dem Bestand)

Manche Organisationen verwenden [!INCLUDE [prod_short](includes/prod_short.md)] in mehreren Konzernmandanten oder juristischen Personen. Andere verwenden [!INCLUDE [prod_short](includes/prod_short.md)] in Niederlassungen, die der Mutterorganisation unterstehen. [!INCLUDE [prod_short](includes/prod_short.md)] bietet der Buchhaltung Tools, die ihr helfen, Sachposten von zwei oder mehr Unternehmen (Tochtergesellschaften) in ein konsolidiertes Unternehmen zu übertragen. Insbesondere für die Lagerverwaltung möchten Sie möglicherweise Sachposten für Ihre Bestandskonten konsolidieren, um Verkaufs-KPIs über Konzernmandanten oder juristische Personen hinweg nachverfolgen zu können.

Weitere Informationen finden Sie unter [Unternehmenskonsolidierung](finance-consolidated-company-reporting.md).

## <a name="ad-hoc-analysis-of-inventory-data"></a>Ad-hoc-Analyse von Bestandsdaten

Manchmal wollen Sie nur prüfen, ob die Zahlen stimmen, oder schnell eine Zahl bestätigen. Die folgenden Features eignen sich hervorragend für Ad-hoc-Analysen:

- Datenanalysen auf Sachkontolistenseiten
- In Excel öffnen

Mit dem Feature für die Datenanalyse können Sie fast jede Listenseite öffnen, z. B. **Artikelposten**, in den Analysemodus wechseln und dann Daten nach Belieben gruppieren, filtern und pivotieren.

:::image type="content" source="media/data-analysis-inventory-dead-stock.png" alt-text="Beispiel für die Durchführung einer Datenanalyse zu altem Lagerbestand auf der Seite „Artikelposten“." lightbox="media/data-analysis-inventory-dead-stock.png":::

Ebenso können Sie die Aktion **In Excel öffnen** verwenden, um eine Listenseite zu öffnen, die Liste optional nach einer Teilmenge der Daten zu filtern und dann Excel zum Arbeiten mit den Daten zu verwenden. Indem Sie zum Beispiel Features wie „Daten analysieren“, „Was-wäre-wenn-Analyse“ oder „Prognoseblatt“ verwenden.

<!-- :::image type="content" source="media/open-in-excel-item-ledger-entries.png" alt-text="Example of how to do data analysis on the Item Ledger Entries data using Excel." lightbox="media/open-in-excel-item-ledger-entries.png"::: -->

> [!TIP]
> Wenn Sie OneDrive für Systemfeatures konfigurieren, wird die Excel-Arbeitsmappe in Ihrem Browser geöffnet.

Weitere Informationen zur Ad-hoc-Analyse von Bestandsdaten finden Sie unter [Ad-hoc-Analyse von Bestandsdaten](ad-hoc-analysis-inventory.md).

## <a name="built-in-reports-for-inventory"></a>Integrierte Bestandsberichte

[!INCLUDE [prod_short](includes/prod_short.md)] enthält mehrere integrierte Berichte, Nachverfolgungsfunktionen und Tools, die Bestandsorganisationen bei der Berichterstattung über ihre Daten unterstützen.

Um einen Überblick über die verfügbaren Berichte zu erhalten, wählen Sie auf Ihrer Homepage **Alle Berichte** aus. Dadurch öffnet sich der Berichts-Explorer, der nach den Features in der Option **Bericht und Analyse** gefiltert ist. Wählen Sie unter der Überschrift **Verkauf und Marketing** die Option **Erkunden** aus. Weitere Informationen finden Sie unter [Mit dem Rollen-Explorer nach Berichten suchen](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-sales.png" alt-text="Beispiel zu Berichten im Vertriebsrollencenter." lightbox="media/report-explorer-sales.png":::

<!-- The built-in reports come in two flavors:

- Designed for print (pdf).
- Designed for analysis in Excel. -->

Weitere Informationen zu Berichten, die für den Bestand relevant sind, finden Sie unter [Integrierte Bestands- und Lagerberichte](inventory-WMS-reports.md).

## <a name="on-screen-inventory-analytics"></a>Bestandsanalyse am Bildschirm

[!INCLUDE [prod_short](includes/prod_short.md)] verfügt über mehrere Seiten, die Ihnen einen Überblick über den Bestand und die zu erledigenden Aufgaben bieten. Hier sind einige Beispiele, mit denen Sie anfangen können:

- [Die Verfügbarkeit von Elementen anzeigen](inventory-how-availability-overview.md)
- [Artikel mit Serien-, Chargen- und Paketnummern verfolgen](inventory-how-work-item-tracking.md)
- [Ablaufverfolgung der Artikel mit Artikelverfolgung](inventory-how-to-trace-item-tracked-items.md)
- [Abstimmung zwischen den Lagerbestandsposten und der Finanzbuchhaltung prüfen](finance-how-to-post-inventory-costs-to-the-general-ledger.md#to-audit-the-reconciliation-between-the-inventory-ledger-and-the-general-ledger)
- [Zugeordnete Artikel in einem Warenausgangs- oder Kommissionierarbeitsblatt anzeigen](warehouse-how-to-cross-dock-items.md#to-view-cross-docked-items-in-a-shipment-or-pick-worksheet)

Das Verkaufsmodul umfasst auch Analyseseiten zum Bestand:

- [Datumsangaben für Lieferterminzusagen berechnen](sales-how-to-calculate-order-promising-dates.md)
- [Lieferdaten für Verkaufsaufträge berechnen](sales-date-calculation-for-sales.md)
- [Paketverfolgung](sales-how-track-packages.md)

### <a name="show-inventory-related-general-ledger-entries-and-balances-from-the-chart-of-accounts-page"></a>Mit dem Bestand zusammenhängende Sachposten und Salden auf der Seite „Kontenplan“ anzeigen

Auf der Seite **Kontenplan** werden alle Sachkonten mit aggregierten Zahlen zu den in der Finanzbuchhaltung gebuchten Beträgen angezeigt. Von dieser Seite aus können Sie beispielsweise Folgendes tun:  

- Berichte ansehen, die die Sachkonteneinträge und -Salden zeigen.  
- Eine Liste der Buchungsgruppen für dieses Konto überprüfen.
- Zeigen Sie separate Soll- und Habensalden für ein einzelnes Konto an.

Speziell für die Lagerverwaltung können Sie auf der Seite „Kontenplan“ eine Ansicht erstellen, in der nur die Konten angezeigt werden, die Sie zum Buchen von Bestandsposten verwenden.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Beispiel dafür, wie die Seite „Kontenplan“ Finanzinformationen anzeigt" lightbox="media/chart-of-accounts-page.png":::

Weitere Informationen finden Sie unter [Den Kontenplan verstehen](finance-general-ledger.md#the-chart-of-accounts).

### <a name="analyze-inventory-data-by-dimensions"></a>Bestandsdaten nach Dimensionen analysieren

Dimensionen sind Attribute und Werte, die Posten kategorisieren, sodass Sie sie auf Dokumenten wie Verkaufsaufträgen verfolgen und analysieren können. Dimensionen können beispielsweise angegeben, aus welchem Projekt oder aus welcher Abteilung ein Posten stammt.  

Anstatt also separate Finanzbuchhaltungskonten für jede Abteilung und jeden Standort einzurichten, können Sie Dimensionen als Grundlage für die Analyse verwenden und vermeiden, dass Sie eine komplizierte Kontenplanstruktur erstellen müssen.

Mehr erfahren Sie unter [Daten nach Dimensionen analysieren](bi-how-analyze-data-dimension.md).

## <a name="see-also"></a>Siehe auch

[Unternehmenskonsolidierung](finance-consolidated-company-reporting.md)   
[Finanzberichte mit Finanzdaten und Kontenkategorien erstellen](bi-how-work-account-schedule.md)  
[Finanzberichte über Konzernmandanten oder juristische Personen hinweg verarbeiten](finance-consolidated-company-reporting.md)  
[Ad-hoc-Analyse von Bestandsdaten](ad-hoc-analysis-inventory.md)  
[Integrierte Bestands- und Lagerberichte](inventory-WMS-reports.md)  
[Den Kontenplan verstehen](finance-general-ledger.md#the-chart-of-accounts)  
[Daten nach Dimensionen analysieren](bi-how-analyze-data-dimension.md)  
[Analysen, Business Intelligence und Berichterstellung – Übersicht](reports-bi-reporting.md)   
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
