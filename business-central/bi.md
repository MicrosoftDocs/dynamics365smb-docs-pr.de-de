---
title: Finanzielle Analysen
description: 'Business Central hilft Ihnen, Daten Ihres Unternehmens zu sammeln, zu analysieren und weiterzugeben, um Business Intelligence zu erhalten.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: kepontop
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '103, 108, 198, 490'
ms.date: 03/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Finanzielle Analysen

Unternehmen erfassen im Laufe ihrer täglichen Arbeit enorme Mengen an Daten, die wertvolle Business Intelligence (BI) für Entscheidungen liefern:

- Verkaufszahlen
- Einkauf
- Betriebsbedarf
- Gehälter der Mitarbeitenden
- Budgets

[!INCLUDE[prod_short](includes/prod_short.md)] enthält viele Features, die Ihnen helfen, Finanzdaten Ihrer Organisation zu sammeln, zu analysieren und weiterzugeben:

- Finanzberichte (für Finanzauswertungen und KPIs)
- Ad-hoc-Analyse von Listen
- Ad-hoc-Analyse von Daten in Excel (über „In Excel öffnen“)
- Integrierte Finanzberichte

Jedes dieser Features hat seine eigenen Vor- und Nachteile, die von der Art der Datenanalyse und der Rolle der Benutzenden abhängen. Weitere Informationen finden Sie unter [Analysen, Business Intelligence und Berichterstellung – Übersicht](reports-bi-reporting.md).

Dieser Artikel erklärt, wie Sie diese Analysefeatures nutzen können, um finanzielle Erkenntnisse zu gewinnen.

## Analyseanforderungen im Finanzbereich

Wenn Sie über Analyseanforderungen im Finanzbereich nachdenken, kann es hilfreich sein, ein mentales Modell zu verwenden, das auf allgemein beschriebenen Personas und ihren unterschiedlichen Analyseanforderungen basiert.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Darstellung verschiedener Personas für die Analyse" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Mitarbeitende in unterschiedlichen Rollen haben unterschiedliche Anforderungen an die Daten und nutzen die Daten auf unterschiedliche Weise. Beispielsweise interagieren Mitarbeitende im Finanzbereich anders mit Daten als im Vertrieb.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Abbildung, die zeigt, das verschiedene Personas unterschiedliche Analyseanforderungen haben." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Rolle              | Datenaggregation  | Übliche Arten zur Datennutzung                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|CFO/CEO          | Leistungsdaten  | KPIs <br> Dashboards <br> Finanzberichte           |
|Finanzmanagement | Trends, Zusammenfassungen | Integrierte Managementberichte <br> Ad-hoc-Analysen      | 
|Buchhalter         | Detaillierte Daten     | Integrierte betriebliche Berichte <br> Aufgabendaten am Bildschirm |

## Finanz-KPIs

Ein Key Performance Indicator (KPI) ist ein messbarer Wert, der zeigt, wie effektiv Sie Ihre Ziele erreichen. Im Finanzbereich werden häufig die folgenden KPIs verwendet, um die finanzielle Stärke eines Unternehmens zu überwachen:

- Bruttogewinnspanne
- Nettogewinnspanne
- Nettoumlaufvermögen
- Umsatzbedingte/Einzugsliquidität
- Finanzieller Hebel, auch bekannt als Eigenkapitalmultiplikator
- Verschuldungsgrad
- Gesamtkapitalumschlag
- Eigenkapitalrendite
- Vermögensrendite

<!-- Not ready to publish yet
For more information, see [Financial KPIs in Business Central](bi-finance-kpis.md) 
-->

## Verwendung von Finanzberichten für die Erstellung von Finanzauswertungen und KPIs

Das Feature **Finanzberichte** gibt Ihnen Einblick in die in Ihrem Kontenplan (COA) enthaltenen Finanzdaten. Sie können Finanzberichte einrichten, um die Zahlen in den Finanzbuchhaltungskonten zu analysieren und Sachposten mit Budgetposten zu vergleichen. Die Ergebnisse werden in Diagrammen und Berichten auf Ihrer Homepage angezeigt, darunter das Cashflowdiagramm sowie die GuV- und Bilanzberichte.

Dimensionen spielen eine wichtige Rolle bei Business Intelligence. Bei einer Dimension handelt es sich um Daten, die Sie einem Eintrag als Parameter hinzufügen können. Mithilfe von Dimensionen können Sie Einträge mit ähnlichen Merkmalen gruppieren, sodass sie leichter zu analysieren sind. Exportieren Sie Debitoren, Regionen, Produkte und Verkaufende. Sie verwenden Dimensionen u. a. bei der Festlegung von Analyseansichten und beim Erstellen von Finanzberichten. Unter [Arbeiten mit Dimensionen](finance-dimensions.md) erfahren Sie mehr.

> [!TIP]
> Um Transaktionsdaten schnell zu analysieren, können Sie die Summen im Kontenplan und alle Einträge auf den Seiten **Buchungen** nach Dimensionen filtern. Suchen Sie nach der Aktion **Dimensionsfilter festlegen**.  

Die folgende Tabelle beschreibt eine Reihe von Aufgaben in der Finanzberichterstattung mit Links zu den Artikeln, die sie beschreiben.  

| Bis | Siehe |
| --- | --- |
| Erstellen Sie neue Finanzberichte, um Bilanzen für die Berichterstattung zu definieren oder als Diagramme anzuzeigen.| [Bereiten Sie Finanzberichte mit Finanzdaten und Kontenkategorien vor](bi-how-work-account-schedule.md)|
| Verwenden Sie statistische Konten, um Informationen in Finanzberichten zu ergänzen. Mit Statistikkonten können Sie Metriken hinzufügen, die auf Nicht-Transaktionsdaten basieren. Sie können die nicht-transaktionsbezogenen Daten als zahlenbasierte Einheiten hinzufügen, z. B. Mitarbeiterzahl, Quadratmeterzahl oder Anzahl der Debitoren mit überfälligen Rechnungen. | [Daten mit statistischen Konten analysieren](bi-use-statistical-accounts.md) |
| Erfahren Sie anhand von Beispielen, wie Sie einen neuen Finanzbericht erstellen. | [Exemplarische Vorgehensweise: Eine Cashflowplanung mithilfe von Finanzberichten erstellen](walkthrough-making-cash-flow-forecasts-by-using-account-schedules.md) |
| Analysieren Sie Ihre finanzielle Performance, indem Sie Leistungskennzahlen (KPIs) auf der Grundlage von Finanzberichten festlegen, die Sie dann als Webdienste veröffentlichen. Die veröffentlichten Finanzberichte KPIs können auf einer Website angezeigt oder mit Hilfe von OData-Webdiensten in Microsoft Excel importiert werden. |[KPI-Webdienste auf der Grundlage von Finanzberichten festlegen und veröffentlichen](bi-how-to-set-up-and-publish-kpi-web-services-based-on-account-schedules.md) |
| Legen Sie Ansichten fest, um Daten anhand von Dimensionen zu analysieren.|[Analysieren Sie Daten nach Dimensionen](bi-how-analyze-data-dimension.md)|
| Erstellen neuer Analyseberichte für Verkauf, Einkauf und Lager sowie Einrichten von Analysevorlagen |[Analyseberichte erstellen](bi-how-create-analysis-views-reports.md)|

## Finanzberichte über Konzernmandanten oder juristische Personen hinweg

Einige Organisationen verwenden [!INCLUDE [prod_short](includes/prod_short.md)] in mehreren Konzernmandanten oder juristischen Personen. Andere verwenden [!INCLUDE [prod_short](includes/prod_short.md)] in Niederlassungen, die den übergeordneten Organisationen Bericht erstatten müssen. [!INCLUDE [prod_short](includes/prod_short.md)] bietet Buchhaltern Tools, die ihnen helfen, Hauptbucheinträge von zwei oder mehr Unternehmen (Tochtergesellschaften) in ein konsolidiertes Unternehmen zu übertragen.  

Weitere Informationen finden Sie unter [Unternehmenskonsolidierung](finance-consolidated-company-reporting.md).

## Ad-hoc-Analysen von Finanzdaten

Manchmal wollen Sie nur prüfen, ob die Zahlen stimmen, oder schnell eine Zahl bestätigen. Die folgenden Features eignen sich hervorragend für Ad-hoc-Analysen:

- Datenanalysen auf Sachkontolistenseiten
- In Excel öffnen

Mit dem Datenanalysefeature können Sie fast jede Listenseite öffnen, z. B. die Seiten „Sachposten“, „Anlagenposten“, „Scheckposten“ oder „Bankposten“, in den Analysemodus wechseln und dann Daten nach Belieben gruppieren, filtern und pivotieren.

:::image type="content" source="media/data-analysis-gl-entries.png" alt-text="Beispiel für die Durchführung einer Datenanalyse auf der Seite „Sachposten“." lightbox="media/data-analysis-gl-entries.png":::

Ebenso können Sie die Aktion **In Excel öffnen** verwenden, um eine Listenseite für Sachposten zu öffnen, die Liste optional nach einer Teilmenge der Daten zu filtern und dann Excel zum Arbeiten mit den Daten zu verwenden. Indem Sie zum Beispiel FEatures wie „Daten analysieren“, „Was-wäre-wenn-Analyse“ oder „Prognoseblatt“ verwenden.

:::image type="content" source="media/open-in-excel-gl-entries.png" alt-text="Beispiel für die Durchführung einer Datenanalyse von Sachposten mithilfe von Excel." lightbox="media/open-in-excel-gl-entries.png":::

> [!TIP]
> Wenn Sie OneDrive für Systemfeatures konfigurieren, wird die Excel-Arbeitsmappe in Ihrem Browser mithilfe von Excel für das Web geöffnet. 


Weitere Informationen zur Durchführung von Ad-hoc-Analysen finden Sie unter [Ad-hoc-Analysen von Finanzdaten](ad-hoc-analysis-finance.md). 

## Integrierte Berichte für den Finanzbereich

[!INCLUDE [prod_short](includes/prod_short.md)] enthält mehrere integrierte Berichte, Nachverfolgungsfunktionen und Tools, die Wirtschaftsprüfern oder Controllern helfen, die für die Berichterstattung an die Finanzabteilung verantwortlich sind.

Um einen Überblick über die verfügbaren Berichte zu erhalten, wählen Sie im oberen Bereich Ihrer Homepage auf **Alle Berichte**. Dadurch öffnet sich der Rollen-Explorer, der nach den Features in der Option **Bericht und Analyse** gefiltert ist. Weitere Informationen finden Sie unter [Mit dem Rollen-Explorer nach Berichten suchen](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-finance.png" alt-text="Beispiel zu Berichten im Finanzrollencenter." lightbox="media/report-explorer-finance.png":::

Es in zwei Varianten integrierter Berichte:

- Für den Druck erstellt (pdf).
- Für die Analyse in Excel erstellt.

Weitere Informationen zu für den Finanzbereich relevanten Berichten finden Sie in diesen Übersichten.

- [Integrierte Excel-Finanzberichte](finance-analyze-excel.md)
- [Wichtigste integrierte Finanzberichte](finance-reports.md)
- [Integrierte Anlagenberichte](fa-reports.md)
- [Integrierte Debitorenberichte](receivables-reports.md)
- [Integrierte Kreditorenberichte](payables-reports.md)

<!-- TODO: add when we have these articles
* [Built-in Cost Accounting reports](cost-accounting-reports.md) 
* [Built-in Cash Management reports](cost-accounting-reports.md) 
* [Built-in Tax and VAT reports](tax-and-vat-reports.md) 
-->

## Finanzaufgabenseiten am Bildschirm

[!INCLUDE [prod_short](includes/prod_short.md)] verfügt über mehrere Seiten, die Ihnen einen Überblick über Finanzen und die zu erledigenden Aufgaben bieten.

### Sachposten und Salden auf der Seite „Kontenplan“ anzeigen

Auf der Seite „Kontenplan“ werden alle Sachkonten mit aggregierten Zahlen zu den in der Finanzbuchhaltung gebuchten Beträgen angezeigt. Von dieser Seite aus können Sie beispielsweise Folgendes tun:  

- Berichte ansehen, die die Sachkonteneinträge und -Salden zeigen.  
- Eine Liste der Buchungsgruppen für dieses Konto überprüfen.
- Zeigen Sie separate Soll- und Habensalden für ein einzelnes Konto an.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Beispiel dafür, wie die Seite „Kontenplan“ Finanzinformationen anzeigt" lightbox="media/chart-of-accounts-page.png":::

Weitere Informationen finden Sie unter [Den Kontenplan verstehen](finance-general-ledger.md#the-chart-of-accounts).

### Anzeigen eines Vergleichs von tatsächlichen und budgetierten Beträgen für alle Konten sowie für mehrere Perioden

Im Rahmen des Erfassens, Analysierens und Weitergebens der Firmendaten möchten Sie sich vielleicht aktuelle Beträge verglichen mit den budgetierten Beträgen für alle Konten sowie für mehrere Perioden anzeigen lassen. Sie können den Vergleich von der Seite **Kontenplan** aus über die Aktion **Saldo/Budget** vornehmen.

Weitere Informationen finden Sie unter [Tatsächliche Beträge im Vergleich zu budgetierten Beträgen analysieren](bi-how-analyze-actual-versus-budget.md).

### Daten nach Dimensionen analysieren

Dimensionen sind Attribute und Werte, die Posten kategorisieren, sodass Sie sie auf Dokumenten wie Verkaufsaufträgen verfolgen und analysieren können. Dimensionen können beispielsweise angegeben, aus welchem Projekt oder aus welcher Abteilung ein Posten stammt.  

Anstatt also separate Finanzbuchhaltungskonten für jede Abteilung und jedes Projekt einzurichten, können Sie Dimensionen als Grundlage für die Analyse verwenden und vermeiden, dass Sie eine komplizierte Kontenplanstruktur erstellen müssen.

In der Finanzanalyse sind Dimensionen Daten, die Sie einem Sachposten als eine Art Markierung hinzufügen. Diese Daten dienen zum Gruppieren von Sachposten mit ähnlichen Merkmalen – beispielsweise Debitoren, Regionen, Produkte oder Verkäufer – sowie zum einfachen Abrufen dieser Gruppen zur Analyse. Sie können Dimensionen für Posten in Buch.-Blättern, Belegen und Budgets verwenden. Weitere Informationen finden Sie unter [Daten nach Dimensionen analysieren](bi-how-analyze-data-dimension.md)

### Cashflow analysieren

Auf der Buchhalter-Homepage unter **Finanzleistung** bieten die Diagramme „Bargeldumlauf“, „Cashflow“ und „Einnahmen und Ausgaben“ verschiedene Möglichkeiten, den Cashflow zu analysieren:

- Überprüfen Sie die Zahlen für eine Periode, indem Sie den Zeitachsenschieberegler verwenden.
- Filtern Sie ein Diagramm, indem Sie die Quelle in der Legende auswählen.
- Ändern Sie die Länge der Periode oder gehen Sie zur vorherigen oder nächsten Periode, indem Sie die Optionen Finanzleistung auswählen.

:::image type="content" source="media/cashflow-accountant-rolecentre.png" alt-text="Beispiel dafür, wie die Cashflow-Visualisierungen im Buchhalter-Rollencenter aussehen" lightbox="media/cashflow-accountant-rolecentre.png":::

Um die Planung zusätzlich zu den Absatzplanungsposten zu prüfen, können Sie auch das Cashflowarbeitsblatt berücksichtigen. Beispielsweise wird angezeigt, wie die Planungs:

- Verarbeitet bestätigte Verkäufe und Einkäufe.
- Subtrahiert Verbindlichkeiten und fügt Forderungen hinzu.
- Überspringt duplizierte Verkaufsaufträge und Bestellungen.

Weitere Informationen finden Sie unter [Analysieren von Cashflow in Ihren Mandanten](finance-analyze-cash-flow.md).

## Siehe auch

[Finanzberichte über Konzernmandanten oder juristische Personen hinweg verarbeiten](finance-consolidated-company-reporting.md)  
<!-- [Financial KPIs in Business Central](bi-finance-kpis.md)    -->
[Finanzberichte mit Finanzdaten und Kontenkategorien erstellen](bi-how-work-account-schedule.md)  
[Ad-hoc-Analysen der Finanzdaten](ad-hoc-analysis-finance.md)   
[Den Kontenplan verstehen](finance-general-ledger.md#the-chart-of-accounts)  
[Integrierte Excel-Finanzberichte](finance-analyze-excel.md)  
[Wichtigste integrierte Finanzberichte](finance-reports.md)  
[Integrierte Anlagenberichte](fa-reports.md)  
[Integrierte Debitorenberichte](receivables-reports.md)  
[Integrierte Kreditorenberichte](payables-reports.md)  
[Finanzen – Übersicht](finance.md)  
[Analysen, Business Intelligence und Berichterstellung – Übersicht](reports-bi-reporting.md)   
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
