---
title: Anlagenanalyse
description: 'Erfahren Sie, wie Sie Daten zu Anlagen für Business Intelligence erfassen, analysieren und freigeben.'
author: brentholtorf
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '5601, 5600, 5615, 5616, 5617'
ms.date: 04/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="fixed-assets-analytics"></a>Anlagenanalyse

Unternehmen mit Anlagen erfassen im Laufe ihrer täglichen Arbeit eine Menge Daten über diese Anlagen. Diese Daten liefern wertvolle Business Intelligence (BI) für das Anlagenmanagement:

- Anschaffungen von Anlagen
- Abschreibungen von Anlagen
- Versicherung und Reparaturen
- Anlagenbudgets

[!INCLUDE[prod_short](includes/prod_short.md)] bietet viele Features, die Ihnen helfen, Daten über die Anlagen Ihrer Organisation zu erfassen, zu analysieren und weiterzugeben:

- Finanzberichte (für Finanzauswertungen und KPIs zu Anlagenkonten)
- Ad-hoc-Analyse von Listen
- Ad-hoc-Analyse von Daten in Excel (über „In Excel öffnen“)
- Integrierte Tools für die Anlagenanalyse
- Integrierte Anlagenberichte

> [!NOTE]
> Die Anlagenanalyse unterscheidet sich ein wenig von anderen Bereichen. Sie müssen bereits vorhandene Daten analysieren, etwa zu Anschaffungen, Abschreibungen und Versicherungen von Anlagen, aber auch zukünftige Daten, etwa zu Abschreibungen und zur Stilllegung von Anlagen. Für den letzteren Analysetyp bietet [!INCLUDE[prod_short](includes/prod_short.md)] integrierte Berichte, mit denen diese Zahlen berechnet werden können.

Jedes dieser Features hat Vor- und Nachteile, die von der Art der Datenanalyse und der Rolle der Benutzenden abhängen. Weitere Informationen finden Sie unter [Analysen, Business Intelligence und Berichterstellung – Übersicht](reports-bi-reporting.md).

In diesem Artikel werden Möglichkeiten beschrieben, diese Analysefeatures zu nutzen, um Einblicke in Ihre Anlagen zu erhalten.

## <a name="analytics-needs-in-asset-management"></a>Analysebedarf im Anlagenmanagement

Wenn Sie über Analyseanforderungen im Anlagenmanagement nachdenken, kann es hilfreich sein, ein auf Personas basierendes Modell zu verwenden, das die jeweiligen Analyseanforderungen allgemein beschreibt.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Darstellung verschiedener Personas für die Analyse" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Im Hinblick auf Daten haben Mitarbeitende in unterschiedlichen Rollen auch unterschiedliche Anforderungen an die Daten und nutzen die Daten auf unterschiedliche Weise. Beispielsweise interagieren Mitarbeitende in der Anlagenverwaltung und im Finanzbereich anders mit Daten als im Vertrieb.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Abbildung, die zeigt, das verschiedene Personas unterschiedliche Analyseanforderungen haben." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Rolle              | Datenaggregation  | Übliche Arten zur Datennutzung                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|CFO, COO, CEO                 | Leistungsdaten  | KPIs <br> Dashboards <br> Finanzberichte           |
|Anlagenbuchhaltung, Controlling   | Trends, Zusammenfassungen | Integrierte Managementberichte <br> Ad-hoc-Analysen      | 
|Buchhalter                      | Detaillierte Daten     | Integrierte betriebliche Berichte <br> Aufgabendaten am Bildschirm |

## <a name="asset-management-kpis"></a>Anlagenmanagement-KPIs

Ein Key Performance Indicator (KPI) ist ein messbarer Wert, der zeigt, wie effektiv Sie Ihre Ziele erreichen. Im Anlagenmanagement werden häufig die folgenden KPIs verwendet, um die Verwendung der Anlagen eines Unternehmens zu überwachen:

- Gesamtkapitalumschlag
- Vermögensrendite

## <a name="use-financial-reporting-to-produce-financial-statements-and-kpis-related-to-fixed-assets"></a>Finanzberichte für die Erstellung von Finanzauswertungen und KPIs im Zusammenhang Anlagen verwenden

Das Feature **Finanzberichterstattung** gibt Ihnen Einblick in die in Ihrem Kontenplan (COA) enthaltenen Finanzdaten. Sie können Finanzberichte einrichten, um die Zahlen in den Sachkonten zu analysieren und Sachposten mit Budgetposten zu vergleichen. Speziell für das Anlagenmanagement können Sie Finanzberichte zu den Sachkonten einrichten, die Sie zum Verfolgen von Anlagenbuchungen verwenden.

Dimensionen spielen eine wichtige Rolle bei Business Intelligence. Bei einer Dimension handelt es sich um Daten, die Sie einem Eintrag als Parameter hinzufügen können. Mit Dimensionen können Sie Posten mit ähnlichen Merkmalen gruppieren, z. B. Debitoren, Regionen, Produkte und Verkaufende, und diese Gruppen leicht für Analysen abrufen. Sie verwenden Dimensionen u. a. bei der Definition von Analyseansichten und beim Erstellen von Finanzberichten. Unter [Arbeiten mit Dimensionen](finance-dimensions.md) erfahren Sie mehr.

Mehr über Finanzberichte erfahren Sie unter [Finanzberichte mit Finanzdaten und Kontenkategorien erstellen](bi-how-work-account-schedule.md).

## <a name="finance-reporting-across-business-units-or-legal-entities-related-to-fixed-assets"></a>Finanzberichte über Konzernmandanten oder juristische Personen hinweg (im Zusammenhang mit Anlagen)

Manche Organisationen verwenden [!INCLUDE [prod_short](includes/prod_short.md)] in mehreren Konzernmandanten oder juristischen Personen. Andere verwenden [!INCLUDE [prod_short](includes/prod_short.md)] in Niederlassungen, die der Mutterorganisation unterstehen. [!INCLUDE [prod_short](includes/prod_short.md)] bietet der Buchhaltung Tools, die ihr helfen, Sachposten von zwei oder mehr Unternehmen (Tochtergesellschaften) in ein konsolidiertes Unternehmen zu übertragen. Insbesondere für das Anlagenmanagement möchten Sie möglicherweise Sachposten für Ihre Anlagenkonten konsolidieren, um Anlagen-KPIs über Konzernmandanten oder juristische Personen hinweg nachverfolgen zu können.

Weitere Informationen finden Sie unter [Unternehmenskonsolidierung](finance-consolidated-company-reporting.md).

## <a name="ad-hoc-analysis-of-fixed-assets-data"></a>Ad-hoc-Analysen von Anlagendaten

Manchmal wollen Sie nur prüfen, ob die Zahlen stimmen, oder schnell eine Zahl bestätigen. Die folgenden Features eignen sich hervorragend für Ad-hoc-Analysen:

- Datenanalysen auf Sachkontolistenseiten
- In Excel öffnen

Mit dem Feature für die Datenanalyse können Sie fast jede Listenseite öffnen, z. B. **Sachposten** oder **Anlagenposten**, in den Analysemodus wechseln und dann Daten nach Belieben gruppieren, filtern und pivotieren.

:::image type="content" source="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png" alt-text="Beispiel für die Durchführung einer Datenanalyse auf der Seite „Anlagenposten“, um sich den Anlagenwert anzeigen zu lassen." lightbox="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png":::

Ebenso können Sie die Aktion **In Excel öffnen** verwenden, um eine Listenseite für Sachposten zu öffnen, die Liste optional nach einer Teilmenge der Daten zu filtern und dann Excel zum Arbeiten mit den Daten zu verwenden. Indem Sie zum Beispiel FEatures wie „Daten analysieren“, „Was-wäre-wenn-Analyse“ oder „Prognoseblatt“ verwenden.

<!-- :::image type="content" source="media/open-in-excel-gl-entries.png" alt-text="Example of how to do data analysis on the G/L entries data using Excel." lightbox="media/open-in-excel-gl-entries.png"::: -->

> [!TIP]
> Wenn Sie OneDrive für Systemfeatures konfigurieren, wird die Excel-Arbeitsmappe in Ihrem Browser mithilfe von Excel für das Web geöffnet. 

Weitere Informationen zur Durchführung von Ad-hoc-Analysen von Anlagenposten finden Sie unter [Ad-hoc-Analysen von Anlagendaten](ad-hoc-analysis-fa.md).


## <a name="built-in-reports-for-fixed-assets"></a>Integrierte Berichte für Anlagen

[!INCLUDE [prod_short](includes/prod_short.md)] enthält mehrere integrierte Berichte, Nachverfolgungsfunktionen und Tools, die Überwachungs- und Controllingfachkräften, die Berichte zu Anlagen erstellen, unterstützen.

Um einen Überblick über die verfügbaren Berichte zu erhalten, wählen Sie oben auf Ihrer Homepage **Alle Berichte** aus. Dadurch öffnet sich die Rollen-Explorer-Seite, die nach den Features in der Option **Bericht und Analyse** gefiltert ist. Um Berichte zu Anlagen zu finden, geben Sie im Feld **Suchen** **Anlagen** ein. Weitere Informationen finden Sie unter [Mit dem Rollen-Explorer nach Berichten suchen](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-fixed-assets.png" alt-text="Beispiel zu Berichten im Finanzrollencenter." lightbox="media/report-explorer-fixed-assets.png":::

<!-- Built-in reports come in two flavors:

- Designed for print (pdf).
- Designed for analysis in Excel. -->

Weitere Informationen zu Berichten, die für Anlagen relevant sind, finden Sie unter [Integrierte Anlagenberichte](fa-reports.md).

## <a name="on-screen-fixed-assets-analytics"></a>Anlagenanalyse auf dem Bildschirm

[!INCLUDE [prod_short](includes/prod_short.md)] verfügt über mehrere Seiten, die Ihnen einen Überblick über die Anlagen und die zu erledigenden Aufgaben bieten. Hier sind einige Beispiele, mit denen Sie anfangen können:

- [Berechnen und Buchen der AfA und Analysieren der AfA.](fa-how-depreciate-amortize.md)
- [Wartungskosten überwachen](fa-how-maintain.md#to-monitor-maintenance-costs)
- [Versicherungsdeckung überwachen](fa-how-insure.md#to-monitor-insurance-coverage)
- [Geänderte AfA-Buchwerte anzeigen](fa-how-trans-split-combine.md#to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification)
- [Verkaufsposten anzeigen](fa-how-dispose-retire.md#to-view-disposal-ledger-entries)
- [Geschätzte Verkaufswerte anzeigen](fa-how-manage-budgets.md#to-view-projected-disposal-values)

### <a name="show-fixed-asset-general-ledger-entries-and-balances-from-the-chart-of-accounts-page"></a>Anlagensachposten und -salden auf der Seite „Kontenplan“ anzeigen

Auf der Seite „Kontenplan“ werden alle Sachkonten mit aggregierten Zahlen zu den Beträgen in der Finanzbuchhaltung angezeigt. Von dieser Seite aus können Sie beispielsweise Folgendes tun:  

- Berichte ansehen, welche die Sachkonteneinträge und -salden zeigen.  
- Eine Liste der Buchungsgruppen für dieses Konto überprüfen.
- Zeigen Sie separate Soll- und Habensalden für ein einzelnes Konto an.

Speziell für Anlagen können Sie auf der Seite „Kontenplan“ eine Ansicht erstellen, in der nur die Konten angezeigt werden, die Sie zum Buchen von Anlagenposten verwenden.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Beispiel dafür, wie die Seite „Kontenplan“ Finanzinformationen anzeigt" lightbox="media/chart-of-accounts-page.png":::

Weitere Informationen finden Sie unter [Den Kontenplan verstehen](finance-general-ledger.md#the-chart-of-accounts).

### <a name="analyze-data-by-dimensions-related-to-fixed-assets"></a>Daten nach (mit Anlagen zusammenhängenden) Dimensionen analysieren

Dimensionen sind Attribute und Werte, die Posten kategorisieren, sodass Sie sie auf Dokumenten wie Anlagen-Buch.-Blättern verfolgen und analysieren können. Dimensionen können beispielsweise angegeben, aus welcher Abteilung oder aus welchem Standort ein Posten kommt.  

Anstatt also separate Finanzbuchhaltungskonten für jede Abteilung und jeden Standort einzurichten, können Sie Dimensionen als Grundlage für die Analyse verwenden und vermeiden, dass Sie eine komplizierte Kontenplanstruktur erstellen müssen.

Mehr erfahren Sie unter [Daten nach Dimensionen analysieren](bi-how-analyze-data-dimension.md)

## <a name="see-also"></a>Siehe auch

[Finanzberichte über Konzernmandanten oder juristische Personen hinweg verarbeiten](finance-consolidated-company-reporting.md)  
[Finanzberichte mit Finanzdaten und Kontenkategorien erstellen](bi-how-work-account-schedule.md)  
[Den Kontenplan verstehen](finance-general-ledger.md#the-chart-of-accounts)  
[Ad-hoc-Analysen von Anlagendaten](ad-hoc-analysis-fa.md)   
[Integrierte Anlagenberichte](fa-reports.md)  
[Analysen, Business Intelligence und Berichterstellung – Übersicht](reports-bi-reporting.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
