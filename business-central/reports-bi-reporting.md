---
title: 'Analysen, Business Intelligence und Berichterstellung – Übersicht'
description: 'Bietet einen Überblick über alle Funktionen für Analysen, Business Intelligence und Berichterstellung, die in Business Central unterstützt werden.'
author: KennieNP
ms.topic: get-started
ms.devlang: al
ms.search.keywords: feature overview
ms.reviewer: bholtorf
ms.date: 09/22/2022
ms.author: kepontop
ms.service: dynamics-365-business-central
---

# Analysen, Business Intelligence und Berichterstellung – Übersicht

Kleine und mittelständische Unternehmen setzen auf integrierte Analyse- und Berichtsfunktionen, die sie sofort nutzen können, um den Überblick über ihr Geschäft zu behalten. [!INCLUDE[prod_short](includes/prod_short.md)] bietet Berichte und Analysetools, die grundlegende und komplexe Geschäftsprozesse für solche Organisationen abdecken. Sie können auch Ad-hoc-Analysen direkt von Ihrer Homepage aus durchführen.  

## Analyseanforderungen in Organisationen

Wenn Sie über Analyseanforderungen in Organisationen nachdenken, kann es hilfreich sein, ein mentales Modell zu verwenden, das auf allgemein beschriebenen Personas und ihren unterschiedlichen Analyseanforderungen basiert.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Darstellung verschiedener Personas für die Analyse" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Das Modell basiert auf der Tatsache, dass verschiedene Rollen in einer Organisation unterschiedliche Anforderungen an Daten haben. Je höher eine Rolle im Organigramm platziert ist, desto mehr aggregierte Daten benötigt die Person in der Rolle, um ihre Arbeit zu erledigen.

Rollen verfügen häufig über bevorzugte Methoden zum Konsumieren und Analysieren von Daten, Methoden, die den Grad der Datenaggregation widerspiegeln, den sie benötigen.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Abbildung, die zeigt, das verschiedene Personas unterschiedliche Analyseanforderungen haben." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

In den folgenden Abschnitten erfahren Sie mehr über die Möglichkeiten zur Nutzung von Daten von [!INCLUDE[prod_short](includes/prod_short.md)]:

- Finanzberichte
- KPIs und Dashboards
- Ad-hoc-Analysen
- Berichte

## Verwendung von Finanzberichten für die Erstellung von Finanzauswertungen und KPIs

Die Finanzberichtsfunkion gibt Ihnen Einblick in die in Ihrem Kontenplan (COA) gespeicherten Finanzdaten. Sie können Finanzberichte einrichten, um die Zahlen in den Finanzbuchhaltungskonten zu analysieren und Sachposten mit Budgetposten zu vergleichen.

:::image type="content" source="media/acc_schedule_13_columns.jpg" alt-text="Screenshot eines Finanzberichts." lightbox="media/acc_schedule_13_columns.jpg":::

Dimensionen spielen eine wichtige Rolle bei Business Intelligence. Bei einer Dimension handelt es sich um Daten, die Sie einem Eintrag als Parameter hinzufügen können. Mithilfe von Dimensionen können Sie Einträge mit ähnlichen Merkmalen gruppieren. Gruppieren Sie zum Beispiel Debitoren, Regionen, Produkte und Verkaufende. Gruppen erleichtern das Abrufen von Daten zur Analyse. Sie verwenden Dimensionen u. a. bei der Definition von Analyseansichten und beim Erstellen von Finanzberichten. Unter [Arbeiten mit Dimensionen](finance-dimensions.md) erfahren Sie mehr.

Weitere Informationen zu Finanzberichten und KPIs finden Sie unter [Verwendung von Finanzberichten für die Erstellung von Finanzauswertungen und KPIs](bi.md).

## Ihre geschäftlichen Ziele mithilfe von Key Performance Indicators erreichen

Ein Key Performance Indicator (KPI) ist ein messbarer Wert, der zeigt, wie effektiv Sie Ihre Ziele erreichen. Betrachten Sie KPIs als Scorecard Ihres Unternehmens, mit der Sie erfassen können, ob Sie Ihre Ziele erreichen.

Durch die Identifizierung und Verfolgung von KPIs erfahren Sie, ob Ihr Unternehmen auf dem richtigen Weg ist oder ob Sie den Kurs ändern sollten. Bei richtiger Anwendung sind KPIs leistungsstarke Tools, die Ihnen bei Folgendem helfen:

- Überwachen Sie die Finanzstärke des Unternehmens.
- Messen Sie den Fortschritt anhand strategischer Ziele.
- Erkennen Sie Probleme frühzeitig.
- Nehmen Sie rechtzeitig Anpassungen der Taktik vor.
- Motivieren Sie Teammitglieder.
- Treffen Sie schneller bessere Entscheidungen.

Mehr über KPIs erfahren Sie unter [Ihre geschäftlichen Ziele mithilfe von Key Performance Indicators erreichen](./analytics-about-kpis.md)

## Ad-hoc-Datenanalyse

Eventuell möchten Sie einfach nur überprüfen, ob die Zahlen das richtige Ergebnis liefern, schnell eine Hypothese über das Unternehmen bestätigen oder widerlegen oder vielleicht nach Anomalien in Ihren Finanzdaten suchen. Für Ad-hoc-Analysen verfügen Sie möglicherweise nicht über einen integrierten Bericht, der Ihnen bei der Beantwortung Ihrer Fragen hilft. Nutzen Sie für Ad-hoc-Analysen diese beiden Features:

- Datenanalysen auf Sachkontolistenseiten
- In Excel öffnen

Mit der Datenanalysefunktion können Sie fast jede Listenseite öffnen, z. B. die Seiten „Sachposten“ oder „Debitorenposten“, in den Analysemodus wechseln und dann Daten nach Belieben gruppieren, filtern und schwenken. 

:::image type="content" source="media/data-analysis-gl-entries.png" alt-text="Beispiel für die Durchführung einer Datenanalyse auf der Seite „Sachposten“." lightbox="media/data-analysis-gl-entries.png":::

Ebenso können Sie die Aktion **In Excel öffnen** verwenden, um eine Listenseite zu öffnen, die Liste optional nach einer Teilmenge der Daten zu filtern und dann Excel zum Arbeiten mit den Daten zu verwenden. Indem Sie zum Beispiel FEatures wie „Daten analysieren“, „Was-wäre-wenn-Analyse“ oder „Prognoseblatt“ verwenden.

:::image type="content" source="media/open-in-excel-gl-entries.png" alt-text="Beispiel für die Durchführung einer Datenanalyse von Sachposten mithilfe von Excel." lightbox="media/open-in-excel-gl-entries.png":::

> [!TIP]
> Wenn Sie OneDrive für Systemfeatures konfigurieren, wird die Excel-Arbeitsmappe in Ihrem Browser mithilfe von Excel für das Web geöffnet.

Weitere Informationen zu Ad-hoc-Analysen finden Sie unter [Ad-hoc-Datenanalyse](reports-adhoc-analysis.md).

## Berichte

Ein Bericht in [!INCLUDE[prod_short](includes/prod_short.md)] sammelt Informationen auf der Grundlage einer festgelegten Gruppe von Kriterien. Berichte organisieren und präsentieren die Informationen in einem leicht zu lesenden Format, das Sie in Excel nutzen, ausdrucken oder als Datei speichern können.  

Als Beispiel für einen interaktiven Bericht in Excel können Sie mit dem Bericht ***Debitor – Saldenrückblick** analysieren, was Ihre Debitoren Ihnen schulden und wann Zahlungen fällig sind.

:::image type="content" source="media/aged-accounts-receivables-excel.png" alt-text="Beispiel für den interaktiven Bericht über Debitor-Saldenrückblicke in Excel." lightbox="media/aged-accounts-receivables-excel.png":::

Für Debitor-Saldenrückblicke fügt [!INCLUDE[prod_short](includes/prod_short.md)] auch einen Bericht zum Ausdrucken ein. Die Möglichkeit zum Drucken ist praktisch, wenn Sie die Daten lieber in einer PDF-Datei haben möchten.

:::image type="content" source="media/aged-accounts-receivables-pdf.png" alt-text="Beispiel für den Bericht über Debitor-Saldenrückblicke im PDF-Format." lightbox="media/aged-accounts-receivables-pdf.png":::

[!INCLUDE[prod_short](includes/prod_short.md)] verfügt über mehr als 300 integrierte Berichte, mit denen Sie Ihre Geschäftsprozesse mit datengesteuerten Erkenntnissen unterstützen können. Um einen schnellen Überblick über alle Berichte zu erhalten, die für Ihre Rolle verfügbar sind, können Sie den Berichts-Explorer vom Rollencenter und allen Listenseiten sowie von **Wie möchten Sie weiter verfahren** aus öffnen.

:::image type="content" source="media/report-explorer-finance.png" alt-text="Beispiel dafür, wie der Berichts-Explorer alle Berichte für eine Rolle anzeigt." lightbox="media/report-explorer-finance.png":::

Weitere Informationen zur Verwendung des Berichts-Explorers zum Anzeigen aller integrierten Berichte finden Sie unter [Berichte nach Rolle erkunden](ui-role-explorer.md).

In der folgenden Tabelle sind Artikel zur Verwendung integrierter Berichte in [!INCLUDE[prod_short](includes/prod_short.md)] aufgeführt.

| Bis  | Siehe |
| --- | --- |
| Erfahren Sie, wie Sie Berichten verwenden (Lesezeichen setzen, ausführen, drucken, planen und das Layout ändern). | [Berichte in der täglichen Arbeit verwenden](reports-use-reports.md) |
| Erfahren Sie mehr darüber, welche integrierten Berichte in [!INCLUDE[prod_short](includes/prod_short.md)] verfügbar sind. |[Bericht – Übersicht](reports-available-reports.md)| 
| Verwenden Sie den Berichts-Explorer, um alle integrierten Berichte anzuzeigen. | [Berichte nach Rolle erkunden](ui-role-explorer.md) |

## Externe Business Intelligence- und Berichterstellungstools

Wenn Sie möchten, können Sie Business Intelligence-Tools verwenden, die nicht in [!INCLUDE[prod_short](includes/prod_short.md)] eingebettet sind. Die folgende Tabelle enthält Links zu Anleitungen und Möglichkeiten zur Verwendung externer Tools.

| Bis  | Siehe |
| --- | --- |
| Power BI mit Business Central-Daten verwenden | [Power BI mit Business Central verwenden](admin-powerbi.md) |
| Integrieren Sie externe Business Intelligence Tools mit [!INCLUDE[prod_short](includes/prod_short.md)].| [Externe Business Intelligence Tools](reports-external-analysis.md) |
| Daten in Data-Warehouses oder Data Lakes extrahieren| [So extrahieren Sie Daten in Data-Warehouses oder Data-Lakes](/dynamics365/business-central/dev-itpro/performance/performance-developer#efficient-extracts-to-data-lakes-or-data-warehouses) |
| Business Central-Daten mit Microsoft Fabric analysieren| [Einführung in Microsoft Fabric und Business Central](admin-fabric.md) |
| Daten mithilfe von APIs aus Business Central lesen | [Business Central API v2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/) |

## Analyse nach Funktionsbereich

Der Inhalt dieses allgemeinen Artikels steht Ihnen für viele Funktionsbereiche auch in speziellen Versionen in [!INCLUDE[prod_short](includes/prod_short.md)] zur Verfügung.

| Bei der Arbeit mit ... | Siehe |
| --- | --- |
| Finanzen | [Finanzielle Analysen](bi.md) |
| Vertrieb | [Vertriebsanalyse](sales-analytics-overview.md) |
| Einkauf | [Einkaufsanalysen](purchasing-analytics-overview.md) |
| Anlagenmanagement | [Anlagenanalysen](fa-analytics-overview.md) |


## Siehe auch

[Verwendung von Finanzberichten für die Erstellung von Finanzauswertungen und KPIs](bi.md)  
[Ihre geschäftlichen Ziele mithilfe von Key Performance Indicators (KPIs) erreichen](analytics-about-kpis.md)  
[Durchführen der Ad-hoc-Datenanalyse](reports-adhoc-analysis.md)  
[Berichte in der täglichen Arbeit verwenden](reports-use-reports.md)  
[Übersicht über integrierte Berichte](reports-available-reports.md)  
[Berichte nach Rolle erkunden](ui-role-explorer.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
