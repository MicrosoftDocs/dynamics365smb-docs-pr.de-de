---
title: Ad-hoc-Analysen von Verkaufsdaten
description: 'Erfahren Sie, wie Sie den Datenanalysemodus verwenden, um Verkaufsdaten zu analysieren.'
author: brentholtorf
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 04/28/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="ad-hoc-analysis-of-sales-data"></a>Ad-hoc-Analysen von Verkaufsdaten

In diesem Artikel wird erklärt, wie Sie das Feature **Datenanalyse** zum Analysieren von Verkaufsdaten direkt von Listenseiten und Abfragen aus verwenden. Sie müssen keinen Bericht ausführen und nicht zu einer anderen Anwendung wie beispielsweise Excel wechseln. Das Feature bietet eine interaktive und vielseitige Möglichkeit, Daten zu berechnen, zusammenzufassen und zu untersuchen. Anstatt Berichte mit Optionen und Filtern auszuführen, können Sie mehrere Registerkarten hinzufügen, die unterschiedliche Aufgaben oder Ansichten der Daten darstellen. Einige Beispiele sind „Meine Debitoren“ oder „Verkaufsstatistiken“ oder jede andere Ansicht, die Sie sich vorstellen können. Weitere Informationen zur Verwendung des Features **Datenanalyse** finden Sie unter [Listen- und Abfragedaten mit dem Analysemodus analysieren](analysis-mode.md).

Nutzen Sie die folgenden Listenseiten zur Ad-hoc-Analyse von Verkaufsprozessen:

- [Aufträge](https://businesscentral.dynamics.com/?page=9305)
- Finanzbuchhaltungsposten
- [Debitorenposten](https://businesscentral.dynamics.com/?page=25)
- Artikelposten
- Gebuchte Verkaufsrechnungen
- Verkaufsreklamationen

## <a name="sales-ad-hoc-analysis-scenarios"></a>Ad-hoc-Analyseszenarien für den Verkauf

Nutzen Sie das Feature **Datenanalyse** zum schnellen Faktencheck und zur Ad-hoc-Analyse:

- Wenn Sie keinen Bericht ausführen möchten.
- Wenn für Ihren speziellen Bedarf kein Bericht vorhanden ist.
- Wenn Sie schnell iterieren möchten, um sich einen guten Überblick über einen Teil Ihres Unternehmens zu verschaffen.

Die folgenden Abschnitte enthalten Beispiele für Verkaufsszenarien in [!INCLUDE [prod_short](includes/prod_short.md)].

| Region | An... | Öffnen Sie diese Seite im Analysemodus | Diese Felder verwenden |
| ---- | ----- | ------------------------------- |------------------- |
| [Verkauf (voraussichtliches Verkaufsvolumen)](#example-sales-expected-sales-volume) | Analysieren Sie Ihr voraussichtliches Verkaufsvolumen. | [Aufträge](https://businesscentral.dynamics.com/?page=9305) | **Verkauf an Debitorname**, **Verkauf an Deb.-Nr.**, **Nr.** , **Menge**, **Belegdatum (Jahr)** und **Belegdatum (Monat)**. |
| [Verkauf (Debitorenverkäufe nach Volumen)](#example-sales-customer-sales-by-volume) | Verschaffen Sie sich einen schnellen Überblick über die Debitoren, die am meisten kaufen oder Ihnen am meisten schulden. | [Debitorenposten](https://businesscentral.dynamics.com/?page=25) | **Debitorenname**, **Beleg-Nr.**, **Menge** und **Restbetrag**. |
| [Finanzen (Debitorenkonten)](#example-finance-accounts-receivables) | Sehen Sie beispielsweise, wie viel Ihre Debitoren Ihnen schulden, aufgeschlüsselt nach Fälligkeitszeiträumen. | [Debitorenposten](https://businesscentral.dynamics.com/?page=25) | **Kundenname**, **Fälligkeitsdatum** und **Restbetrag**. |

## <a name="example-sales-expected-sales-volume"></a>Beispiel: Verkauf (voraussichtliches Verkaufsvolumen)

Um Ihr erwartetes Verkaufsvolumen und die Verkaufsbeträge für nicht gelieferte Aufträge für jeden Debitor nach Jahr oder Monat zu analysieren, gehen Sie wie folgt vor:

1. Öffnen Sie die Liste [Verkaufsaufträge](https://businesscentral.dynamics.com/?page=9305) und schalten Sie den Analysemodus ein.
1. Gehen Sie zum Menü **Spalten** und entfernen Sie alle Spalten (wählen Sie das Kästchen neben dem Feld **Suchen** aus).
1. Aktivieren Sie den **Pivot**-Modus (direkt über dem Feld **Suchen**).
1. Ziehen Sie die Felder **Verkauf an Debitorname**, **Verkauf an Deb.-Nr.** und **Nr.** in den Bereich **Zeilengruppen**. Ziehen Sie die Felder in dieser Reihenfolge.
1. Ziehen Sie das Feld **Menge** in den Bereich **Werte**.
1. Ziehen Sie die Felder **Belegdatum (Jahr)** und **Belegdatum (Monat)** in den Bereich **Spaltenbeschriftungen**. Ziehen Sie die Felder in dieser Reihenfolge.
1. Um die Analyse für ein bestimmtes Jahr oder Quartal durchzuführen, wenden Sie einen Filter im Menü **Zusätzliche Filter** an. Das Menü befindet sich rechts auf der Seite, direkt unter dem Menü **Spalten**.
1. Benennen Sie Ihre Analyseregisterkarte in **Voraussichtliches Verkaufsvolumen** oder in etwas anderes um, das diese Analyse für Sie beschreibt.

## <a name="example-sales-customer-sales-by-volume"></a>Beispiel: Verkauf (Debitorenverkäufe nach Volumen)

Gehen Sie wie folgt vor, um sich einen schnellen Überblick über die Debitoren, die am meisten kaufen oder die Ihnen am meisten schulden, zu verschaffen.

1. Öffnen Sie die Liste [Debitorenposten](https://businesscentral.dynamics.com/?page=25) und schalten Sie den Analysemodus ein.
1. Gehen Sie zum Menü **Spalten** und entfernen Sie alle Spalten (wählen Sie das Kästchen neben dem Feld **Suchen** aus).
1. Ziehen Sie das Feld **Debitorenname** zum Bereich **Zeilengruppen** und das Feld **Beleg-Nr.** darunter.
1. Wählen Sie die Felder **Menge** und **Restbetrag** aus.
1. Um die Analyse für ein bestimmtes Jahr oder Quartal durchzuführen, wenden Sie einen Filter im Menü **Zusätzliche Filter** an. Das Menü befindet sich rechts auf der Seite, direkt unter dem Menü **Spalten**.
1. Benennen Sie Ihre Analyseregisterkarte in **Debitoren nach Verkaufsvolumen** oder in etwas anderes um, das diese Analyse für Sie beschreibt.

Das folgende Bild zeigt das Ergebnis dieser Schritte.

:::image type="content" source="media/data-analysis-customer-ledger-entries.png" alt-text="Beispiel für die Durchführung einer Datenanalyse auf der Seite „Debitorenposten“." lightbox="media/data-analysis-customer-ledger-entries.png":::

## <a name="example-finance-accounts-receivables"></a>Beispiele: Finanzen (Debitorenkonten)

Gehen Sie wie folgt vor, um herauszufinden, wie viel Ihre Debitoren Ihnen, eventuell aufgeschlüsselt nach Fälligkeitszeiträumen, schulden:

1. Öffnen Sie die Liste [Debitorenposten](https://businesscentral.dynamics.com/?page=25) und aktivieren Sie den Analysemodus.
1. Entfernen Sie auf dem Menü **Spalten** alle Spalten (wählen Sie das Kästchen neben dem Feld **Suchen** aus).
1. Aktivieren Sie den **Pivot**-Modus (direkt über dem Feld **Suchen**).
1. Ziehen Sie das Feld **Debitorenname** zum Bereich **Zeilengruppen** und ziehen Sie das Feld **Restbetrag** zum Bereich **Werte**.
1. Ziehen Sie das Feld **Fälligkeitsdatum (Monat)** auf den Bereich **Spaltenbeschriftungen**.
1. Um die Analyse für ein bestimmtes Jahr oder Quartal durchzuführen, wenden Sie einen Filter im Menü **Zusätzliche Filter** an. Das Menü befindet sich rechts auf der Seite, direkt unter dem Menü **Spalten**.
1. Benennen Sie Ihre Analyseregisterkarte in **Kontorückblick nach Monat** oder in etwas anderes um, das diese Analyse für Sie beschreibt.

## <a name="data-foundation-for-ad-hoc-analysis-on-sales"></a>Datengrundlage für Ad-hoc-Analysen zum Verkauf

Nachdem Sie alle Informationen auf einem Verkaufsauftrag eingegeben und alle Verkaufsauftragszeilen hinzugefügt haben, können Sie den Auftrag buchen. Durch die Buchung werden eine Lieferung und eine Rechnung erstellt. [!INCLUDE [prod_short](includes/prod_short.md)] aktualisiert die Debitoren-, Sachposten- und Artikelposten:

- Für jeden Verkaufsauftrag wird ein Verkaufsposten in der Tabelle **Sachposten** erstellt. Darüber hinaus wird ein Posten in der Tabelle **Kreditorenposten** erzeugt und ein Sachposten im entsprechenden Einkaufskonto. Zusätzlich kann das Buchen in einem MwSt.-Posten und einem Sachposten für den Rabattbetrag resultieren.
- Für jede Zeile des Verkaufsauftrags wird ein Artikelposten in der Tabelle **Artikelposten** erstellt (wenn die Verkaufszeilen Artikelnummern enthalten) oder es wird ein Sachposten in der Tabelle **Sachposten** erstellt (wenn die Verkaufszeilen Sachkonten enthalten). Darüber hinaus werden Verkaufsaufträge immer in den Tabellen **Verkaufslieferkopf** und **Verkaufsrechnungskopf** gespeichert.

Weitere Informationen zum Buchen von Verkäufen finden Sie unter [Buchen von Verkäufen](ui-post-sales.md).

## <a name="see-also"></a>Siehe auch

[Buchen von Verkäufen](ui-post-sales.md)  
[Listen- und Abfragedaten mit dem Analysemodus analysieren](analysis-mode.md)  
[Überblick über Verkaufsanalysen](sales-analytics-overview.md)  
[Analysen, Business Intelligence und Berichterstellung – Übersicht](reports-bi-reporting.md)  
[Verkauf – Übersicht](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
