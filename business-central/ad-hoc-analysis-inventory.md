---
title: Ad-hoc-Analyse von Bestandsdaten
description: 'Erfahren Sie, wie Sie den Datenanalysemodus verwenden, um Bestandsdaten zu analysieren.'
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

# Ad-hoc-Analyse von Bestandsdaten

In diesem Artikel wird erklärt, wie Sie das Feature **Datenanalyse** zum Analysieren von Bestandsdaten direkt von Listenseiten und Abfragen aus verwenden. Sie müssen keinen Bericht ausführen und nicht zu einer anderen Anwendung wie beispielsweise Excel wechseln. Das Feature bietet eine interaktive und vielseitige Möglichkeit, Daten zu berechnen, zusammenzufassen und zu untersuchen. Anstatt Berichte mit Optionen und Filtern auszuführen, können Sie mehrere Registerkarten hinzufügen, die unterschiedliche Aufgaben oder Ansichten der Daten darstellen. Einige Beispiele sind „Ablaufende Bestände“ oder „Top-Verkäufer“ oder jede andere Ansicht, die Sie sich vorstellen können. Weitere Informationen zur Verwendung des Features **Datenanalyse** finden Sie unter [Listen- und Abfragedaten mit dem Analysemodus analysieren](analysis-mode.md).

Nutzen Sie die folgenden Listenseiten zur Ad-hoc-Analyse von Bestandsprozessen:

- [Artikelposten](https://businesscentral.dynamics.com/?page=38)

## Ad-hoc-Analyseszenarien für Bestände

Nutzen Sie das Feature **Datenanalyse** zum schnellen Faktencheck und zur Ad-hoc-Analyse:

- Wenn Sie keinen Bericht ausführen möchten.
- Wenn für Ihren speziellen Bedarf kein Bericht vorhanden ist.
- Wenn Sie schnell iterieren möchten, um sich einen guten Überblick über einen Teil Ihres Unternehmens zu verschaffen.

Die folgenden Abschnitte enthalten Beispiele für Bestandsszenarien in [!INCLUDE [prod_short](includes/prod_short.md)].

| Region | An... | Öffnen Sie diese Seite im Analysemodus | Diese Felder verwenden |
| ---- | ----- | ------------------------------- |------------------- |
| [Verfügbarer Lagerbestand](#example-inventory-on-hand) | Erhalten Sie einen Überblick über die in Ihrem Lager verfügbaren Artikel. | [Artikelposten](https://businesscentral.dynamics.com/?page=38) | **Artikelnr.**, **Restmenge** |
|[Beispiel: Ablaufende oder alte Lagerbestände nachverfolgen](#example-track-expiring-or-old-stock) | Erhalten Sie einen Überblick über Artikel in Ihrem Bestand, die schon lange auf Lager sind und sich nicht gut verkaufen. | [Artikelposten](https://businesscentral.dynamics.com/?page=38) | **Buchungsdatum (Jahr)**, **Buchungsdatum (Monat)**, **Artikelnr.**, **Buchungsdatum**, **Buchungsart**, **Menge** und **Restmenge**. |
| [Zurückgesandte Artikel nach Retourengründen](#example-returned-items-by-return-reason) | Erhalten Sie einen Überblick über die von Debitoren zurückgesandte Waren, kategorisiert nach Retourengrund. Nutzen Sie dies für die Analyse zur Qualitätskontrolle. | [Artikelposten](https://businesscentral.dynamics.com/?page=38) | **Retourengrundcode**, **Buchungsdatum (Monat)**, **Menge**, **Einstandsbetrag**, **Buchungsdatum**, **Belegart**, **Artikelnr.** und **Belegnr.** |
| Lagerdurchsatz | Erhalten Sie einen Überblick über Käufe und Verkäufe in Ihrem Lagerbestand nach Monaten oder Quartalen. | [Artikelposten](https://businesscentral.dynamics.com/?page=38) | **Buchungsdatum (Jahr)**, **Buchungsdatum (Monat)**, **Artikelnr.**, **Menge**, **Verkaufsbetrag**, **Einstandsbetrag (Ist)** und **Buchungsdatum (Monat)** |
| [Lagerbestandsumlagerungen] | Erhalten Sie einen Überblick darüber, wie sich Waren in Ihrem Lager zwischen Lagerorten bewegen. | [Artikelposten](https://businesscentral.dynamics.com/?page=38) | **Lagerortcode**, **Menge**, **Buchungsdatum**, **Artikelnr.** |

## Beispiel: verfügbarer Lagerbestand

Um die vorrätigen Artikel in Ihrem Lagerbestand zu analysieren, gehen Sie wie folgt vor:

1. Öffnen Sie die Liste [Artikelposten](https://businesscentral.dynamics.com/?page=38) und wählen Sie :::image type="content" source="media/analysis-mode-icon.png" alt-text="Analysemodus eingeben."::: um den Analysemodus einzuschalten.
1. Gehen Sie zum Menü **Spalten** und entfernen Sie alle Spalten (wählen Sie das Kästchen neben dem Feld **Suchen** aus).
1. Ziehen Sie das Feld **Artikelnr.** in den Bereich **Zeilengruppen**. Ziehen Sie die Felder in dieser Reihenfolge.
1. Ziehen Sie **Restmenge** in die Bereiche **Werte**.
1. Legen Sie einen **Ungleich**-Filter auf **0** für **Restmenge** fest. Wenn Sie keine negativen Lagerbestände zulassen, legen Sie einen **Größer als**-Filter auf **0** fest.
1. Fügen Sie der Analyse optional weitere Felder hinzu und orientieren Sie sich möglicherweise am Lagerort oder anderen Feldern.
1. Benennen Sie Ihre Analyseregisterkarte in **Verfügbarer Lagerbestand** oder in etwas anderes um, das diese Analyse beschreibt.

Das folgende Bild zeigt das Ergebnis dieser Schritte.

:::image type="content" source="media/data-analysis-inventory-on-hand.png" alt-text="Beispiel für die Durchführung einer Datenanalyse zum verfügbaren Lagerbestand." lightbox="media/data-analysis-inventory-on-hand.png":::

## Beispiel: Ablaufende oder alte Lagerbestände nachverfolgen

Um zu analysieren, welche Artikel schon lange in Ihrem Bestand auf Lager sind und sich nicht gut verkaufen, gehen Sie wie folgt vor:

1. Öffnen Sie die Liste [Artikelposten](https://businesscentral.dynamics.com/?page=38) und wählen Sie :::image type="content" source="media/analysis-mode-icon.png" alt-text="Analysemodus eingeben."::: um den Analysemodus einzuschalten.
1. Gehen Sie zum Menü **Spalten** und entfernen Sie alle Spalten (wählen Sie das Kästchen rechts neben dem Feld **Suchen** aus).
1. Ziehen Sie die Felder **Buchungsdatum (Jahr)**, **Buchungsdatum (Monat)** und **Artikelnr.** in den Bereich **Zeilengruppen**. Ziehen Sie die Felder in dieser Reihenfolge.
1. Wählen Sie im Bereich **Säulen** die Felder **Buchungsdatum**, **Eintragstyp**, **Menge** und **Restmenge** aus.
1. Legen Sie einen **Kleiner als**-Filter auf **Buchungsdatum** fest, um zu bestimmen, was Sie mit „alt“ meinen.
1. Benennen Sie Ihre Analyseregisterkarte in **Alter Lagerbestand** oder in etwas anderes um, das diese Analyse beschreibt.

Das folgende Bild zeigt das Ergebnis dieser Schritte.

:::image type="content" source="media/data-analysis-inventory-dead-stock.png" alt-text="Beispiel für die Durchführung einer Datenanalyse zu unverkäuflichem Lagerbestand auf der Seite „Artikelposten“." lightbox="media/data-analysis-inventory-dead-stock.png":::

## Beispiel: zurückgesandte Artikel nach Retourengrund

Um Retouren sortiert nach Retourengründen zu analysieren, gehen Sie folgendermaßen vor:

1. Öffnen Sie die Liste [Artikelposten](https://businesscentral.dynamics.com/?page=38).
1. Fügen Sie das Feld **Retourengrundcode** hinzu, indem Sie die Seite personalisieren. Wählen Sie im Menü **Einstellungen** die Option **Personalisieren** aus.
1. Beenden Sie den Personalisierungsmodus.
1. Wählen Sie :::image type="content" source="media/analysis-mode-icon.png" alt-text="In den Analysemodus wechseln"::: aus. um den Analysemodus einzuschalten.
1. Gehen Sie zum Menü **Spalten** und entfernen Sie alle Spalten (wählen Sie das Kästchen rechts neben dem Feld **Suchen** aus).
1. Ziehen Sie die Felder **Retourengrundcode** und **Buchungsdatum (Monat)** in den Bereich **Zeilengruppen**. Ziehen Sie die Felder in dieser Reihenfolge.
1. Ziehen Sie die Felder **Menge** und **Kostenbetrag** in den Bereich **Werte**.
1. Fügen Sie alle weiteren Felder hinzu, die Sie in der Analyse haben möchten, und aktivieren Sie sie im Bereich **Spalten**. Sie können beispielsweise die Felder **Buchungsdatum**, **Belegart**, **Artikelnr.** und **Belegnr.** hinzufügen.
1. Benennen Sie Ihre Analyseregisterkarte in **Zurückgegebene Artikel nach Retourengrund** oder in etwas anderes um, das diese Analyse beschreibt.  

## Beispiel: Lagerdurchsatz

1. Öffnen Sie die Liste [Artikelposten](https://businesscentral.dynamics.com/?page=38) und wählen Sie :::image type="content" source="media/analysis-mode-icon.png" alt-text="Analysemodus eingeben."::: um den Analysemodus einzuschalten.
1. Gehen Sie zum Menü **Spalten** und entfernen Sie alle Spalten (wählen Sie das Kästchen rechts neben dem Feld **Suchen** aus).
1. Aktivieren Sie den Schalter **Pivot**-Modus (rechts über dem Feld **Suchen**).
1. Ziehen Sie die Felder **Buchungsdatum (Jahr)**, **Buchungsdatum (Monat)** und **Artikelnr.** in den Bereich **Zeilengruppen**.
1. Ziehen Sie die Felder **Menge**, **Verkaufsmenge** und **Einstandsbetrag (Ist)** in den Bereich **Werte**.
1. Ziehen Sie das Feld **Buchungsdatum (Monat)** auf den Bereich **Spaltengruppen**.
1. Benennen Sie Ihre Analyseregisterkarte in **Lagerdurchsatz nach Monat** oder in etwas anderes um, das diese Analyse beschreibt.  

## Lagerbestandsumlagerungen

Um Lagerbestandsumlagerungen zwischen Lagerorten zu verfolgen, gehen Sie wie folgt aus:

1. Öffnen Sie die Liste [Artikelposten](https://businesscentral.dynamics.com/?page=38) und wählen Sie :::image type="content" source="media/analysis-mode-icon.png" alt-text="Analysemodus eingeben."::: um den Analysemodus einzuschalten.
1. Gehen Sie zum Menü **Spalten** und entfernen Sie alle Spalten (wählen Sie das Kästchen rechts neben dem Feld **Suchen** aus).
1. Ziehen Sie das Feld **Lagerortcode** in den Bereich **Zeilengruppen**.
1. Ziehen Sie das Feld **Menge** in den Bereich **Werte**.
1. Fügen Sie alle weiteren Felder hinzu, die Sie in der Analyse haben möchten, und aktivieren Sie sie im Bereich **Spalten**. Sie könnten beispielsweise das Feld **Artikelnr.** hinzufügen.
1. Benennen Sie Ihre Analyseregisterkarte in **Lagerbestandsumlagerungen** oder in etwas anderes um, das diese Analyse beschreibt.  

   > [!TIP]
   > Wenn Sie das Feld „Buchungsdatum“ hinzufügen, können Sie Umlagerungen auch im Zeitverlauf nachverfolgen.

## Datengrundlage für Ad-hoc-Analysen zum Lager

Wenn Sie einen Verkaufsauftrag buchen, [!INCLUDE [prod_short](includes/prod_short.md)] werden das Debitorenkonto, die Finanzbuchhaltung und die Artikelposten aktualisiert.

- Für jede Verkaufsauftragszeile wird ein Artikelposten in der Tabelle **Artikelposten** erstellt (sofern die Verkaufszeilen Artikelnummern enthalten). Darüber hinaus werden Verkaufsaufträge immer in den Tabellen **Verkaufslieferkopf** und **Verkaufsrechnungskopf** gespeichert. Weitere Informationen zum Buchen von Verkäufen finden Sie unter [Buchen von Verkäufen](ui-post-sales.md).

Wenn Sie einen Einkaufsbeleg buchen, aktualisiert [!INCLUDE [prod_short](includes/prod_short.md)] das Kreditorenkonto, das Sachkonto, die Artikelposten und die Ressourcenposten.

- Für jede Einkaufszeile werden ggf. Einträge in der Tabelle **Artikelposten** erstellt (sofern die Einkaufszeile den Typ „Artikel“ hat). Darüber hinaus werden Einkaufsbelege immer im Feld **Einkaufslieferkopf** und **Einkaufsrechnungskopf** Tabellen erfasst. Weitere Informationen unter [Einkäufe buchen](purchasing-how-record-purchases.md#posting-purchases).

## Siehe auch

[Listen- und Abfragedaten mit dem Analysemodus analysieren](analysis-mode.md)  
[Übersicht über die Bestandsanalyse](inventory-analytics-overview.md)  
[Analysen, Business Intelligence und Berichterstellung – Übersicht](reports-bi-reporting.md)  
[Lagerbestand – Übersicht](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]