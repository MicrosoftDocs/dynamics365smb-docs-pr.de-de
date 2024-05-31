---
title: Ad-hoc-Analysen von Finanzdaten
description: 'Erfahren Sie, wie Sie den Datenanalysemodus verwenden, um Finanzdaten zu analysieren.'
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 05/02/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Ad-hoc-Analysen von Finanzdaten

In diesem Artikel wird erklärt, wie Sie das Feature **Datenanalyse** zum Analysieren von Finanzdaten direkt von Listenseiten und Abfragen aus verwenden. Sie müssen keinen Bericht ausführen und nicht zu einer anderen Anwendung wie beispielsweise Excel wechseln. Das Feature bietet eine interaktive und vielseitige Möglichkeit, Daten zu berechnen, zusammenzufassen und zu untersuchen. Anstatt Berichte mit Optionen und Filtern auszuführen, können Sie mehrere Registerkarten hinzufügen, die unterschiedliche Aufgaben oder Ansichten der Daten darstellen. Einige Beispiele sind „Aktiva gesamt im Zeitverlauf“, „Kreditorenkonten“, „Debitorenkonten“ und jede andere Ansicht, die Sie sich vorstellen können. Weitere Informationen zur Verwendung des Features **Datenanalyse** finden Sie unter [Listen- und Abfragedaten mit dem Analysemodus analysieren](analysis-mode.md).

Nutzen Sie die folgenden Listenseiten um mit der Ad-hoc-Analyse von Finanzprozessen zu beginnen:

- [Finanzbuchhaltungsposten](https://businesscentral.dynamics.com/?page=20)
- [Debitorenposten](https://businesscentral.dynamics.com/?page=25)
- [Kreditorenposten](https://businesscentral.dynamics.com/?page=29)

## Ad-hoc-Analyseszenarien im Finanzwesen

Nutzen Sie das Feature **Datenanalyse** zum schnellen Faktencheck und zur Ad-hoc-Analyse:

- Wenn Sie keinen Bericht ausführen möchten.
- Wenn für Ihren speziellen Bedarf kein Bericht vorhanden ist.
- Wenn Sie schnell iterieren möchten, um sich einen guten Überblick über einen Teil Ihres Unternehmens zu verschaffen.

Die folgenden Abschnitte enthalten Beispiele für Finanzszenarien in [!INCLUDE [prod_short](includes/prod_short.md)].

| Region | Zweck ... | Öffnen Sie diese Seite im Analysemodus | Diese Felder verwenden |
| ---- | ----- | ------------------------------- |------------------- |
|[Beispiel: Finanzen (Debitorenbuchhaltung)](#example-finance-accounts-receivable) | Sehen Sie beispielsweise, wie viel Ihre Debitoren Ihnen schulden, aufgeschlüsselt nach Fälligkeitszeiträumen. | [Debitorenposten](https://businesscentral.dynamics.com/?page=25) | **Debitorenname**, **Fälligkeitsdatum** und **Restbetrag** |
| [Finanzen (Kreditorenkonten)](#example-finance-accounts-payable) | Sehen Sie beispielsweise, wie viel Sie Ihren Kreditoren schulden, eventuell aufgeschlüsselt nach Fälligkeitszeiträumen. | [Kreditorenposten](https://businesscentral.dynamics.com/?page=29) | **Kreditorenname**, **Belegart**, **Belegnr.**, **Fälligkeitsdatum (Jahr)**, **Fälligkeitsdatum (Monat)** und **Restbetrag**. |
| [Finanzen (Verkaufsrechnungen nach Sachkonto)](#example-finance-sales-invoices-by-gl-account) | Sehen Sie sich an, wie sich Ihre Verkaufsrechnungen auf die Sachkonten aus dem Kontenplan verteilen, beispielsweise aufgeschlüsselt nach Zeitintervallen, in denen die Beträge gebucht wurden. | [Finanzbuchhaltungsposten](https://businesscentral.dynamics.com/?page=20) | **Sachkontoname**, **Quellcode**, **Sachkontoname**, **Sachkontonr.**, **Sollbetrag**, **Habenbetrag**, **Buchungsdatum Jahr**, **Buchungsdatum Quartal** und **Buchungsdatum Monat** |
| [Finanzen (GuV)](#example-finance-income-statement) | Sehen Sie sich Ihre Einnahmen über die Ertragskonten aus dem Kontenplan an, beispielsweise aufgeschlüsselt nach Buchungszeiträumen der Beträge. | [Finanzbuchhaltungsposten](https://businesscentral.dynamics.com/?page=20) | **Sachkontonr.**, **Buchungsdatum** und **Betrag**. |
| [Finanzen (Aktiva gesamt)](#example-finance-total-assets) | Sehen Sie sich Ihre Aktiva über die Aktivakonten aus dem Kontenplan an, beispielsweise aufgeschlüsselt nach Buchungszeiträumen der Beträge. | [Finanzbuchhaltungsposten](https://businesscentral.dynamics.com/?page=20) | **Sachkontonr.**, **Buchungsdatum** und **Betrag**. |

### Beispiel: Finanzen (Debitorenbuchhaltung)

Gehen Sie wie folgt vor, um herauszufinden, wie viel Ihre Debitoren Ihnen, eventuell aufgeschlüsselt nach Fälligkeitszeiträumen, schulden:

1. Öffnen Sie die Liste [Debitorenposten](https://businesscentral.dynamics.com/?page=25) und wählen Sie :::image type="content" source="media/analysis-mode-icon.png" alt-text="Analysemodus eingeben":::, um den Analysemodus einzuschalten.
1. Gehen Sie zum Menü **Spalten** und entfernen Sie alle Spalten (wählen Sie das Kästchen rechts neben dem Feld *Suchen* aus).
1. Aktivieren Sie den Schalter **Pivot**-Modus (rechts über dem Feld **Suchen**).
1. Ziehen Sie das Feld **Debitorenname** zum Bereich **Zeilengruppen** und ziehen Sie **Restbetrag** zum Bereich **Werte**.
1. Ziehen Sie das Feld **Fälligkeitsdatum (Monat)** auf den Bereich **Spaltenbeschriftungen**.
1. Um die Analyse auf ein bestimmtes Jahr oder Quartal zu beschränken, wenden Sie im Menü **Analysefilter** (rechts unter dem Menü **Spalten**) einen Filter an.
1. Benennen Sie Ihre Analyseregisterkarte in **Kontorückblick nach Monat** oder in etwas anderes um, das diese Analyse beschreibt.

### Beispiele: Finanzen (Kreditorenkonten)

Gehen Sie wie folgt vor, um herauszufinden, wie viel Sie Ihren Kreditoren, eventuell aufgeschlüsselt nach Fälligkeitszeiträumen, schulden:

1. Öffnen Sie die Listenseite [Kreditorenposten](https://businesscentral.dynamics.com/?page=29) und wählen Sie :::image type="content" source="media/analysis-mode-icon.png" alt-text="Analysemodus eingeben":::, um den Analysemodus einzuschalten.
1. Gehen Sie zum Menü **Spalten** und entfernen Sie alle Spalten (wählen Sie das Kästchen neben dem Feld **Suchen** aus).
1. Aktivieren Sie den Schalter **Pivot**-Modus (rechts über dem Feld **Suchen**).
1. Ziehen Sie die Felder **Kreditorenname**, **Belegart** und **Belegnr.** in den Bereich **Zeilengruppen** und ziehen Sie dann das Feld **Restbetrag** in den Bereich **Werte**.
1. Ziehen Sie die Felder **Fälligkeitsdatum (Jahr)** und **Fälligkeitsdatum (Monat)** in den Bereich **Spaltenbeschriftungen**. Ziehen Sie die Felder in dieser Reihenfolge.
1. Um die Analyse auf ein bestimmtes Jahr oder Quartal zu beschränken, wenden Sie im Menü **Analysefilter** (rechts unter dem Menü **Spalten**) einen Filter an.
1. Benennen Sie Ihre Analyseregisterkarte in **Kreditorenkontorückblick nach Monat** oder in etwas anderes um, das diese Analyse beschreibt.

Das folgende Bild zeigt das Ergebnis dieser Schritte.

:::image type="content" source="media/data-analysis-vendor-ledger-entries.png" alt-text="Beispiel für die Durchführung einer Datenanalyse auf der Seite „Debitorenposten“." lightbox="media/data-analysis-vendor-ledger-entries.png":::

### Beispiel: Finanzen (Verkaufsrechnungen nach Sachkonto)

Um zu sehen, wie sich Ihre Verkaufsrechnungen auf die Sachkonten aus dem Kontenplan verteilen, z. B. aufgeschlüsselt nach Zeitintervallen für die Buchung von Beträgen, führen Sie die folgenden Schritte aus:

1. Öffnen Sie die Seite  [Hauptbucheinträge](https://businesscentral.dynamics.com/?page=20) .
1. Fügen Sie die Felder  **Sachkontoname**  und  **Quellcode**  hinzu, indem Sie die Seite personalisieren. Wählen Sie im Menü **Einstellungen** die Option **Personalisieren** aus.
1. Beenden Sie den Personalisierungsmodus.
1. Wählen Sie :::image type="content" source="media/analysis-mode-icon.png" alt-text="In den Analysemodus wechseln"::: aus. um den Analysemodus einzuschalten.
1. Legen Sie im Menü  **Analysefilter**  im Feld  **Quellcode**  einen Filter auf  **VERKAUF** fest. Wenn Sie Anpassungen haben, die andere Werte hinzufügen, können Sie diese auch hinzufügen.
1. Entfernen Sie auf dem Menü **Spalten** alle Spalten (wählen Sie das Kästchen neben dem Feld **Suchen** aus).
1. Aktivieren Sie den Schalter **Pivot**-Modus (rechts über dem Feld **Suchen**).
1. Ziehen Sie die Felder  **Sachkontoname**  und  **Sachkontonr.**  in den Bereich  **Zeilengruppen** .
1. Ziehen Sie die Felder  **Sollbetrag**  und  **Habenbetrag**  in den Bereich  **Werte** .
1. Ziehen Sie die Felder  **Buchungsdatum Jahr**,  **Buchungsdatum Quartal** und  **Buchungsdatum Monat**  in den Bereich  **Spaltenbeschriftungen** .
1. Benennen Sie Ihre Analyseregisterkarte in  **Rechnungsaufschlüsselung nach Konto** oder in etwas um, das diese Analyse beschreibt.

Das folgende Bild zeigt das Ergebnis dieser Schritte.

:::image type="content" source="media/data-analysis-gl-entries-invoices.png" alt-text="Beispiel für die Durchführung einer Datenanalyse auf der Seite „Sachbucheinträge“ (zum Verständnis von Verkaufsbuchungen)." lightbox="media/data-analysis-gl-entries-invoices.png":::

### Beispiel: Finanzen (GuV)

Gehen Sie wie folgt vor, um sich Ihre Einnahmen über die Ertragskonten aus dem Kontenplan aufgeschlüsselt nach Buchungszeiträumen der Beträge anzusehen:

1. Öffnen Sie die Liste [Sachposten](https://businesscentral.dynamics.com/?page=20) und wählen Sie :::image type="content" source="media/analysis-mode-icon.png" alt-text="Analysemodus eingeben":::, um den Analysemodus einzuschalten.
1. Gehen Sie zum Menü **Spalten** und entfernen Sie alle Spalten (wählen Sie das Kästchen rechts neben dem Feld **Suchen** aus).
1. Aktivieren Sie den Schalter **Pivot**-Modus (rechts über dem Feld **Suchen**).
1. Ziehen Sie das Feld **Sachkontonr.** zum Bereich **Zeilengruppen** und ziehen Sie **Betrag** zum Bereich **Werte**.
1. Ziehen Sie das Feld **Buchungsdatum (Monat)** auf den Bereich **Spaltenbeschriftungen**.
1. Filtern Sie für die Gewinn- und Verlustrechnung nach den von Ihnen verwendeten Konten. In den [!INCLUDE [prod_short](includes/prod_short.md)] Demodaten beginnen diese Konten mit einer „4“. In Ihrem Kontenplan ist dies jedoch eventuell anders. Legen Sie im Menü **Analysefilter** (rechts unter dem Menü **Spalten**) einen Filter für die Konten fest.

   > [!TIP]
   > Um zu sehen, welche Konten in Ihrer Konfiguration verwendet werden, führen Sie den Bericht [Rohbilanz nach Periode](https://businesscentral.dynamics.com/?report=38) aus.

1. Benennen Sie Ihre Analyseregisterkarte in **Erträge nach Monat** oder in etwas anderes um, das diese Analyse beschreibt.

### Beispiel: Finanzen (Aktiva gesamt)

Gehen Sie wie folgt vor, um sich Ihre Aktiva über die Aktivkonten aus dem Kontenplan aufgeschlüsselt nach Buchungszeiträumen der Beträge anzusehen:

1. Öffnen Sie die Liste [Sachposten](https://businesscentral.dynamics.com/?page=20) und wählen Sie :::image type="content" source="media/analysis-mode-icon.png" alt-text="Analysemodus eingeben":::, um den Analysemodus einzuschalten.
1. Gehen Sie zum Menü **Spalten** und entfernen Sie alle Spalten (wählen Sie das Kästchen rechts neben dem Feld **Suchen** aus).
1. Aktivieren Sie den Schalter **Pivot**-Modus (rechts über dem Feld **Suchen**).
1. Ziehen Sie das Feld **Sachkontonr.** zum Bereich **Zeilengruppen** und ziehen Sie **Betrag** zum Bereich **Werte**.
1. Ziehen Sie das Feld **Buchungsdatum (Monat)** auf den Bereich **Spaltenbeschriftungen**.
1. Filtern Sie für die Aufstellung der Gesamtaktiva nach den von Ihnen verwendeten Konten. In den [!INCLUDE [prod_short](includes/prod_short.md)] Demodaten beginnen diese Konten mit einer „10“. In Ihrem Kontenplan ist dies jedoch eventuell anders. Legen Sie im Menü **Weitere Filter** (rechts unter dem Menü **Spalten**) einen Filter für die entsprechenden Konten fest.

   > [!TIP]
   > Um zu sehen, welche Konten in Ihrer Konfiguration verwendet werden, führen Sie den Bericht [Rohbilanz nach Periode](https://businesscentral.dynamics.com/?report=38) aus.

1. Benennen Sie Ihre Analyseregisterkarte in **Erträge nach Monat** oder in etwas anderes um, das diese Analyse beschreibt.

## Datengrundlage für Ad-hoc-Finanzanalysen

Wenn Sie Buch.-Blätter buchen, erstellt [!INCLUDE [prod_short](includes/prod_short.md)] Posten in der Tabelle **Sachposten**. Deshalb werden allgemeine Ad-hoc-Finanzanalysen normalerweise auf der Seite [Sachposten](https://businesscentral.dynamics.com/?page=20) durchgeführt. Für Debitoren- und Kreditorenkonten können Sie [Debitorenposten](https://businesscentral.dynamics.com/?page=25) und [Kreditorenposten](https://businesscentral.dynamics.com/?page=29) analysieren.

Weitere Informationen finden Sie in den folgenden Artikeln:

- [Datengrundlage für Ad-hoc-Analysen zum Verkauf](ad-hoc-analysis-sales.md#data-foundation-for-ad-hoc-analysis-on-sales)
- [Datengrundlage für Ad-hoc-Analysen zum Einkauf](ad-hoc-analysis-purchasing.md#data-foundation-for-ad-hoc-analysis-on-purchasing)

## Siehe auch

[Listen- und Abfragedaten mit dem Analysemodus analysieren](analysis-mode.md)  
[Übersicht über finanzielle Analysen](bi.md)  
[Analysen, Business Intelligence und Berichterstellung – Übersicht](reports-bi-reporting.md)  
[Finanzen – Übersicht](finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]