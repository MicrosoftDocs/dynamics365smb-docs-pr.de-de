---
title: Ad-hoc-Analysen von Nachhaltigkeitsdaten
description: 'Erfahren Sie, wie Sie den Datenanalysemodus zum Analysieren von Nachhaltigkeitsdaten verwenden.'
author: brentholtorf
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI, sustainability, ESG'
ms.search.form: '6220,'
ms.date: 06/12/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="ad-hoc-analysis-of-sustainability-data"></a>Ad-hoc-Analysen von Nachhaltigkeitsdaten

In diesem Artikel wird erklärt, wie Sie die Funktion **Datenanalyse** zum Analysieren von Nachhaltigkeitsdaten direkt über Listenseiten und Abfragen verwenden. Sie müssen keinen Bericht ausführen und nicht zu einer anderen Anwendung wie beispielsweise Excel wechseln. Das Feature bietet eine interaktive und vielseitige Möglichkeit, Daten zu berechnen, zusammenzufassen und zu untersuchen. Anstatt Berichte mit Optionen und Filtern auszuführen, können Sie mehrere Registerkarten hinzufügen, die unterschiedliche Aufgaben oder Ansichten der Daten darstellen. Einige Beispiele sind „Emissionsübersicht“ oder „Emission nach Umfang“ oder jede andere Ansicht, die Sie sich vorstellen können. Weitere Informationen zur Verwendung des Features **Datenanalyse** finden Sie unter [Listen- und Abfragedaten mit dem Analysemodus analysieren](analysis-mode.md).

Nutzen Sie die folgenden Listenseiten zur Ad-hoc-Analyse von Nachhaltigkeitsdaten:

- [Nachhaltigkeitsposten](https://businesscentral.dynamics.com/?page=6220)

## <a name="sustainability-ad-hoc-analysis-scenarios"></a>Ad-hoc-Analyseszenarien zur Nachhaltigkeit

Nutzen Sie das Feature **Datenanalyse** zum schnellen Faktencheck und zur Ad-hoc-Analyse:

- Wenn Sie keinen Bericht ausführen möchten.
- Wenn für Ihren speziellen Bedarf kein Bericht vorhanden ist.
- Wenn Sie schnell iterieren möchten, um sich einen guten Überblick über einen Teil Ihres Unternehmens zu verschaffen.

Die folgenden Abschnitte enthalten Beispiele für Nachhaltigkeitsszenarien in [!INCLUDE [prod_short](includes/prod_short.md)].

| Region | Zweck ... | Öffnen Sie diese Seite im Analysemodus | Diese Felder verwenden |
| ---- | ----- | ------------------------------- |------------------- |
| [Emissionsübersicht (Summe nach Kategorie)](#example-emission-overview-sum-by-category) | Analysieren Sie Ihre Emissionen nach Kategorie. | [Nachhaltigkeitsposten](https://businesscentral.dynamics.com/?page=6220) | **Kontokategorie**, **Kontoname**, **NH4-Emission**, **CO2-Emission** und **N2O-Emission**.|
| [Durchschnittliche Emissionen nach Kategorie](#example-average-emissions-by-category) | Analysieren Sie Ihre durchschnittlichen Emissionen nach Kategorie. | [Nachhaltigkeitsposten](https://businesscentral.dynamics.com/?page=6220) | **Kontokategorie**, **Kontoname**, **NH4-Emission**, **CO2-Emission** und **N2O-Emission**.|
| [Emissionen nach Umfang](#example-emissions-by-scope) | Analysieren Sie Ihre Emissionen nach Umfang. | [Nachhaltigkeitsposten](https://businesscentral.dynamics.com/?page=6220) | **Emissionsumfang**, **Kontokategorie**, **NH4-Emission**, **CO2-Emission** und **N2O-Emission**.|

## <a name="example-emission-overview-sum-by-category"></a>Beispiel: Emissionsübersicht (Summe nach Kategorie)

Um Ihre Emissionen nach Kategorie zu analysieren, gehen Sie wie folgt vor:

1. Öffnen Sie die Seite [Nachhaltigkeitsposten](https://businesscentral.dynamics.com/?page=6220), und aktivieren Sie den Analysemodus.
1. Gehen Sie zum Menü **Spalten** und entfernen Sie alle Spalten (wählen Sie das Kästchen neben dem Feld **Suchen** aus).
1. Aktivieren Sie den **Pivot**-Modus (direkt über dem Feld **Suchen**).
1. Ziehen Sie die Felder **Kontokategore** und **Kontoname** in den Bereich **Zeilengruppen**. Ziehen Sie die Felder in dieser Reihenfolge.
1. Ziehen Sie die Felder **NH4-Emission**, **CO2-Emission** und **N2O-Emission** in den Bereich **Werte**.
1. Benennen Sie Ihre Analyseregisterkarte in **Emissionsübersicht (Summe)** oder in etwas anderes um, das diese Analyse für Sie beschreibt.

Das folgende Bild zeigt das Ergebnis dieser Schritte.

:::image type="content" source="media/data-analysis-sustainability-entries.png" alt-text="Beispiel 1 für die Durchführung einer Datenanalyse auf der Seite „Nachhaltigkeitsposten“." lightbox="media/data-analysis-sustainability-entries.png":::

## <a name="example-average-emissions-by-category"></a>Beispiel: Durchschnittliche Emissionen nach Kategorie

Um Ihre durchschnittlichen Emissionen nach Kategorie zu analysieren, gehen Sie wie folgt vor:

1. Öffnen Sie die Seite [Nachhaltigkeitsposten](https://businesscentral.dynamics.com/?page=6220), und aktivieren Sie den Analysemodus.
1. Gehen Sie zum Menü **Spalten** und entfernen Sie alle Spalten (wählen Sie das Kästchen neben dem Feld **Suchen** aus).
1. Aktivieren Sie den **Pivot**-Modus (direkt über dem Feld **Suchen**).
1. Ziehen Sie die Felder **Kontokategore** und **Kontoname** in den Bereich **Zeilengruppen**. Ziehen Sie die Felder in dieser Reihenfolge.
1. Ziehen Sie die Felder **NH4-Emission**, **CO2-Emission** und **N2O-Emission** in den Bereich **Werte**.
1. Wählen Sie jedes Feld im Bereich **Werte** aus, und ändern Sie die Aggregatfunktion in `Average`.
1. Benennen Sie Ihre Analyseregisterkarte in **Emissionsübersicht (Durchschnitt)** oder in etwas anderes um, das diese Analyse für Sie beschreibt.

Das folgende Bild zeigt das Ergebnis dieser Schritte.

:::image type="content" source="media/data-analysis-sustainability-entries-avg.png" alt-text="Beispiel 2 für die Durchführung einer Datenanalyse auf der Seite „Nachhaltigkeitsposten“." lightbox="media/data-analysis-sustainability-entries-avg.png":::

## <a name="example-emissions-by-scope"></a>Beispiel: Emissionen nach Umfang

Um Ihre Emissionen nach Umfang zu analysieren, gehen Sie wie folgt vor:

1. Öffnen Sie die Seite [Nachhaltigkeitsposten](https://businesscentral.dynamics.com/?page=6220), und aktivieren Sie den Analysemodus.
1. Gehen Sie zum Menü **Spalten** und entfernen Sie alle Spalten (wählen Sie das Kästchen neben dem Feld **Suchen** aus).
1. Aktivieren Sie den **Pivot**-Modus (direkt über dem Feld **Suchen**).
1. Ziehen Sie die Felder **Emissionsumfang** und **Kontokategorie** in den Bereich **Zeilengruppen**. Ziehen Sie die Felder in dieser Reihenfolge.
1. Ziehen Sie die Felder **NH4-Emission**, **CO2-Emission** und **N2O-Emission** in den Bereich **Werte**.
1. Benennen Sie Ihre Analyseregisterkarte in **Emissionsübersicht nach Umfang** oder in etwas anderes um, das diese Analyse für Sie beschreibt.

Das folgende Bild zeigt das Ergebnis dieser Schritte.

:::image type="content" source="media/data-analysis-sustainability-entries-scope.png" alt-text="Beispiel 3 für die Durchführung einer Datenanalyse auf der Seite „Nachhaltigkeitsposten“." lightbox="media/data-analysis-sustainability-entries-scope.png":::

## <a name="data-foundation-for-ad-hoc-analysis-on-sustainability"></a>Datengrundlage für Ad-hoc-Analysen zur Nachhaltigkeit

Die in ein Nachhaltigkeits-Buch.-Blatt eingegebenen Informationen sind temporär und können geändert werden, solange sie sich im Buch.-Blatt befinden. Wenn Sie ein Nachhaltigkeits-Buch.-Blatt buchen, werden die Informationen in Nachhaltigkeitsposten auf einzelnen Nachhaltigkeitskonten übertragen, wo sie nicht geändert werden können. Sie können jedoch Storno- oder Korrekturbuchungen vornehmen. Die Listenseite [Nachhaltigkeitsposten](https://businesscentral.dynamics.com/?page=6220) ist die wichtigste Datenquelle für die Ad-hoc-Analyse von Nachhaltigkeitsdaten.

Weitere Informationen zum Buchen von Nachhaltigkeitsposten finden Sie unter [Nachhaltigkeitsposten erfassen](finance-sustainability-journal.md).

## <a name="see-also"></a>Siehe auch

[Nachhaltigkeitsposten erfassen](finance-sustainability-journal.md)  
[Integrierte Nachhaltigkeitsberichte](sustainability-reports.md)   
[Analysen, Business Intelligence und Berichterstellung – Übersicht](reports-bi-reporting.md)  
[Nachhaltigkeitsverwaltung – Übersicht](finance-manage-sustainability.md)   
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
