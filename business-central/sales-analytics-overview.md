---
title: Verkaufsanalyse
description: 'Business Central enthält viele Features, mit denen Sie wertvolle Vertriebsdaten für Business Intelligence und Entscheidungsfindung im Verkauf sammeln, analysieren und gemeinsam nutzen können.'
author: kennienp
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 04/28/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Verkaufsanalyse

Unternehmen erfassen im Laufe ihrer täglichen Arbeit eine Menge Daten, die wertvolle Business Intelligence (BI) für Führungskräfte im Verkauf liefern:

- Verkaufschancen
- Angebote
- Verkaufsaufträge
- Verkaufsrechnungen

[!INCLUDE[prod_short](includes/prod_short.md)] bietet viele Features, die Ihnen helfen, Verkaufsdaten Ihrer Organisation zu erfassen, zu analysieren und weiterzugeben:

- Ad-hoc-Analyse von Listen
- Ad-hoc-Analyse von Daten in Excel (über „In Excel öffnen“)
- Integrierte Tools zur Verkaufsanalyse
- Integrierte Verkaufsberichte

Jedes dieser Features hat Vor- und Nachteile, die von der Art der Datenanalyse und der Rolle der Benutzenden abhängen. Weitere Informationen finden Sie unter [Analysen, Business Intelligence und Berichterstellung – Übersicht](reports-bi-reporting.md).

Dieser Artikel erklärt, wie Sie diese Analysefeatures nutzen können, um Erkenntnisse zum Verkauf zu gewinnen.

## Analyseanforderungen im Verkauf

Wenn Sie über Analyseanforderungen im Verkaufsmanagement nachdenken, kann es hilfreich sein, ein auf Personas basierendes Modell zu verwenden, das verschiedene Analyseanforderungen allgemein beschreibt.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Darstellung verschiedener Personas für die Analyse" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Mitarbeitende in unterschiedlichen Rollen haben unterschiedliche Anforderungen an die Daten und nutzen die Daten auf unterschiedliche Weise. Beispielsweise interagieren Mitarbeitende in der Anlagenverwaltung und im Finanzbereich anders mit Daten als im Vertrieb.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Abbildung, die zeigt, das verschiedene Personas unterschiedliche Analyseanforderungen haben." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Rolle              | Datenaggregation  | Übliche Arten zur Datennutzung                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|CCO, CFO, CEO    | Leistungsdaten  | KPIs <br> Dashboards <br> Finanzberichte           |
|Verkaufsleiter      | Trends, Zusammenfassungen | Integrierte Managementberichte <br> Ad-hoc-Analysen      | 
|Kundenbetreuung, Verkaufende | Detaillierte Daten     | Integrierte betriebliche Berichte <br> Aufgabendaten am Bildschirm |

<!-- 
## Sales KPIs

A key performance indicator (KPI) is a measurable value that shows how effectively you’re meeting your goals. In sales management, people often use the following KPIs to monitor their organization's sales performance:

- TODO  
-->

## Finanzberichte für die Erstellung von Finanzauswertungen und KPIs im Zusammenhang mit dem Verkauf verwenden

Das Feature **Finanzberichterstattung** gibt Ihnen Einblick in die in Ihrem Kontenplan (COA) enthaltenen Finanzdaten. Sie können Finanzberichte einrichten, um die Zahlen in den Finanzbuchhaltungskonten zu analysieren und Sachposten mit Budgetposten zu vergleichen. Speziell für das Verkaufsmanagement können Sie Finanzberichte zu den Sachkonten einrichten, die Sie zum Verfolgen von Verkaufsbuchungen verwenden.

Dimensionen spielen eine wichtige Rolle bei Business Intelligence. Bei einer Dimension handelt es sich um Daten, die Sie einem Eintrag als Parameter hinzufügen. Mit Dimensionen können Sie Einträge mit ähnlichen Merkmalen gruppieren, z. B. Debitoren, Regionen, Produkte und Verkaufende. Sie verwenden Dimensionen u. a. bei der Festlegung von Analyseansichten und beim Erstellen von Finanzberichten. Unter [Arbeiten mit Dimensionen](finance-dimensions.md) erfahren Sie mehr.

Erfahren Sie mehr unter Finanzberichte unter [Finanzberichte mit Finanzdaten und Kontenkategorien erstellen](bi-how-work-account-schedule.md).

## Mit dem Verkauf zusammenhängende Finanzberichte über Konzernmandanten oder juristische Personen hinweg

Einige Organisationen verwenden [!INCLUDE [prod_short](includes/prod_short.md)] in mehreren Konzernmandanten oder juristischen Personen. Andere verwenden [!INCLUDE [prod_short](includes/prod_short.md)] in Niederlassungen, die der Mutterorganisation unterstehen. [!INCLUDE [prod_short](includes/prod_short.md)] bietet Buchhaltern Tools, die ihnen helfen, Hauptbucheinträge von zwei oder mehr Unternehmen (Tochtergesellschaften) in ein konsolidiertes Unternehmen zu übertragen. Insbesondere für das Verkaufsmanagement möchten Sie möglicherweise Sachposten für Ihre Verkaufskonten konsolidieren, um Verkaufs-KPIs über Konzernmandanten oder juristische Personen hinweg nachverfolgen zu können.

Weitere Informationen finden Sie unter [Unternehmenskonsolidierung](finance-consolidated-company-reporting.md).

## Ad-hoc-Analysen von Verkaufsdaten

Manchmal wollen Sie nur prüfen, ob die Zahlen stimmen, oder schnell eine Zahl bestätigen. Die folgenden Features eignen sich hervorragend für Ad-hoc-Analysen:

- Datenanalysen auf Sachkontolistenseiten
- In Excel öffnen

Mit dem Feature für die Datenanalyse können Sie fast jede Listenseite öffnen, z. B. die Seiten **Sachposten**, **Debitorenposten**, **Artikelposten** oder **Gebuchte Rechnungen**, in den Analysemodus wechseln und dann Daten nach Belieben gruppieren, filtern und pivotieren.

:::image type="content" source="media/data-analysis-customer-ledger-entries.png" alt-text="Beispiel für die Durchführung einer Datenanalyse auf der Seite „Debitorenposten“." lightbox="media/data-analysis-customer-ledger-entries.png":::

Ebenso können Sie die Aktion **In Excel öffnen** verwenden, um eine Listenseite zu öffnen, die Liste optional nach einer Teilmenge der Daten zu filtern und dann Excel zum Arbeiten mit den Daten zu verwenden. Indem Sie zum Beispiel FEatures wie „Daten analysieren“, „Was-wäre-wenn-Analyse“ oder „Prognoseblatt“ verwenden.

:::image type="content" source="media/open-in-excel-customer-ledger-entries.png" alt-text="Beispiel für die Durchführung einer Datenanalyse von Debitorenposten mithilfe von Excel." lightbox="media/open-in-excel-customer-ledger-entries.png":::

> [!TIP]
> Wenn Sie OneDrive für Systemfeatures konfigurieren, wird die Excel-Arbeitsmappe in Ihrem Browser geöffnet.

Weitere Informationen zur Ad-hoc-Analyse von Verkaufsdaten finden Sie unter [Ad-hoc-Analyse von Verkaufsdaten](ad-hoc-analysis-sales.md). 

## Integrierte Berichte für den Verkauf

[!INCLUDE [prod_short](includes/prod_short.md)] enthält mehrere integrierte Berichte, Nachverfolgungsfunktionen und Tools, die Verkaufsorganisationen bei der Berichterstattung über ihre Daten unterstützen.

Um einen Überblick über die verfügbaren Berichte zu erhalten, wählen Sie im oberen Bereich Ihrer Homepage **Alle Berichte** aus. Dadurch öffnet sich der Rollen-Explorer, der nach den Features in der Option **Bericht und Analyse** gefiltert ist. Weitere Informationen finden Sie unter [Mit dem Rollen-Explorer nach Berichten suchen](ui-role-explorer.md). 

:::image type="content" source="media/report-explorer-sales.png" alt-text="Beispiel zu Berichten im Vertriebsrollencenter." lightbox="media/report-explorer-sales.png":::

Es gibt zwei Varianten integrierter Berichte:

- Für den Druck erstellt (pdf).
- Für die Analyse in Excel erstellt.

Weitere Informationen zu Berichten, die für den Verkauf relevant sind, finden Sie unter [Integrierte Berichte für den Verkauf](sales-reports.md).

## Verkaufsanalysen am Bildschirm

[!INCLUDE [prod_short](includes/prod_short.md)] verfügt über mehrere Seiten, die Ihnen einen Überblick über den Verkauf und die zu erledigenden Aufgaben bieten. Hier sind einige Beispiele, mit denen Sie anfangen können:

- [Öffnen Sie die Liste **Verkaufsangebote**](https://businesscentral.dynamics.com/?page=9300)
- [Öffnen Sie die Liste **Verkaufsaufträge**](https://businesscentral.dynamics.com/?page=9305)
- [Öffnen Sie die Liste **Gebuchte Verkaufsrechnungen**](https://businesscentral.dynamics.com/?page=143)
- [Öffnen Sie die Liste **Verkaufsretouren**](https://businesscentral.dynamics.com/?page=9304)
- [Datumsangaben für Lieferterminzusagen berechnen](sales-how-to-calculate-order-promising-dates.md)
- [Lieferdaten für Verkaufsaufträge berechnen](sales-date-calculation-for-sales.md)
- [Paketverfolgung](sales-how-track-packages.md)
- [Die Verfügbarkeit von Elementen anzeigen](inventory-how-availability-overview.md)
- [Rahmenauftragsstatus](sales-how-to-create-blanket-sales-orders.md#to-view-the-status-of-a-blanket-sales-order)
- [Lassen Sie sich ungebuchte und gebuchte Zeilen des Verkaufsrahmenauftrags anzeigen](sales-how-to-create-blanket-sales-orders.md#to-view-unposted-and-posted-blanket-sales-order-lines)


### Mit dem Verkauf zusammenhängende Sachposten und Salden auf der Seite „Kontenplan“ anzeigen

Auf der Seite „Kontenplan“ werden alle Sachkonten mit aggregierten Zahlen zu den in der Finanzbuchhaltung gebuchten Beträgen angezeigt. Von dieser Seite aus können Sie beispielsweise Folgendes tun:  

- Berichte ansehen, die die Sachkonteneinträge und -Salden zeigen.  
- Eine Liste der Buchungsgruppen für dieses Konto überprüfen.
- Zeigen Sie separate Soll- und Habensalden für ein einzelnes Konto an.

Speziell für den Verkauf können Sie auf der Seite „Kontenplan“ eine Ansicht erstellen, in der nur die Konten angezeigt werden, die Sie zum Buchen von Verkaufsposten verwenden.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Beispiel dafür, wie die Seite „Kontenplan“ Finanzinformationen anzeigt" lightbox="media/chart-of-accounts-page.png":::

Weitere Informationen finden Sie unter [Den Kontenplan verstehen](finance-general-ledger.md#the-chart-of-accounts).

### Daten nach (mit dem Verkauf zusammenhängenden) Dimensionen analysieren

Dimensionen sind Attribute und Werte, die Posten kategorisieren, sodass Sie sie auf Dokumenten wie Verkaufsaufträgen verfolgen und analysieren können. Dimensionen können beispielsweise angegeben, aus welchem Projekt oder aus welcher Abteilung ein Posten stammt.  

Anstatt also separate Finanzbuchhaltungskonten für jede Abteilung und jeden Standort einzurichten, können Sie Dimensionen als Grundlage für die Analyse verwenden und vermeiden, dass Sie eine komplizierte Kontenplanstruktur erstellen müssen.

Mehr erfahren Sie unter [Daten nach Dimensionen analysieren](bi-how-analyze-data-dimension.md).

## Siehe auch

[Unternehmenskonsolidierung](finance-consolidated-company-reporting.md)   
[Finanzberichte mit Finanzdaten und Kontenkategorien erstellen](bi-how-work-account-schedule.md)  
[Finanzberichte über Konzernmandanten oder juristische Personen hinweg verarbeiten](finance-consolidated-company-reporting.md)  
[Ad-hoc-Analysen von Verkaufsdaten](ad-hoc-analysis-sales.md)   
[Integrierte Verkaufsberichte](sales-reports.md)   
[Den Kontenplan verstehen](finance-general-ledger.md#the-chart-of-accounts)  
[Daten nach Dimensionen analysieren](bi-how-analyze-data-dimension.md)  
[Analysen, Business Intelligence und Berichterstellung – Übersicht](reports-bi-reporting.md)   
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
