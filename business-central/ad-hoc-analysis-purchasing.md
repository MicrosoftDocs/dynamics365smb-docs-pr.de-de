---
title: Ad-hoc-Analysen im Einkauf
description: 'Erfahren Sie, wie Sie den Datenanalysemodus im Einkauf verwenden, um Daten zu analysieren.'
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '9306, 9307, 518, 29'
ms.date: 04/29/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="ad-hoc-analyses-in-purchasing"></a>Ad-hoc-Analysen im Einkauf

In diesem Artikel wird erklärt, wie Sie Einkaufsdaten von Listenseiten und Abfragen mit dem Feature **Datenanalyse** analysieren. Mit dem Feature für die Datenanalyse können Sie, Daten direkt von der Seite aus analysieren, ohne einen Bericht ausführen oder eine andere Anwendung wie Excel öffnen zu müssen. Die Datenanalyse bietet eine interaktive und vielseitige Möglichkeit, Daten zu berechnen, zusammenzufassen und zu untersuchen. Anstatt Berichte mit Optionen und Filtern auszuführen, können Sie mehrere Registerkarten hinzufügen, die unterschiedliche Aufgaben oder Ansichten der Daten darstellen. Einige Beispiele sind „Meine Kreditoren“ oder „Einkaufsstatistiken“ oder jede andere Ansicht, die Sie sich vorstellen können. Weitere Informationen zur Verwendung des Features **Datenanalyse** finden Sie unter [Listen- und Abfragedaten mit dem Analysemodus analysieren](analysis-mode.md).

Nutzen Sie die folgenden Listenseiten zur Ad-hoc-Analyse von Einkaufsprozessen:

- [Bestellungen](https://businesscentral.dynamics.com/?page=9307)
- [Einkaufszeilen](https://businesscentral.dynamics.com/?page=518)
- [Gebuchte Einkaufsrechnungen](https://businesscentral.dynamics.com/?page=146)
- [Kreditorenposten](https://businesscentral.dynamics.com/?page=29)
- [Finanzbuchhaltungsposten](https://businesscentral.dynamics.com/?page=20)

## <a name="ad-hoc-analysis-scenarios-for-purchasing"></a>Ad-hoc-Analyseszenarien für den Einkauf

Nutzen Sie das Feature **Datenanalyse** zum schnellen Faktencheck und zur Ad-hoc-Analyse:

- Wenn Sie keinen Bericht ausführen möchten
- Wenn für Ihren speziellen Bedarf kein Bericht vorliegt
- Wenn Sie schnell iterieren möchten, um sich einen guten Überblick über einen Teil Ihres Unternehmens zu verschaffen.

Die folgenden Abschnitte enthalten Beispiele für Einkaufsszenarien in [!INCLUDE [prod_short](includes/prod_short.md)].

| Region | An... | Öffnen Sie diese Seite im Analysemodus | Diese Felder verwenden |
| ---- | ----- | ------------------------------- |------------------- |
| [GRNI-Übersicht](#example-goods-received-not-invoiced-grni-overview) | Erhalten Sie eine Übersicht über eingegangene, nicht in Rechnung gestellte Waren (GRNI) bei allen Kreditoren. | [Einkaufszeilen](https://businesscentral.dynamics.com/?page=518) | **Typ**, **Betrag – eingegangen, nicht fakturiert (LW)** (nach diesen Feldern filtern), **Kreditorennr.**, **Belegnr.**, **Nr.** und **Betrag – eingegangen, nicht fakturiert (LW)** <br><br> **HINWEIS:** Um diese Felder hinzuzufügen, müssen Sie die Seite personalisieren. Um mehr zu erfahren, gehen Sie zu [Arbeitsbereich personalisieren](ui-personalization-user.md). | 
| [Finanzen (Kreditorenkonten)](#example-finance-accounts-payable) | Sehen Sie beispielsweise, wie viel Sie Ihren Kreditoren schulden, eventuell aufgeschlüsselt nach Fälligkeitszeiträumen. | [Kreditorenposten](https://businesscentral.dynamics.com/?page=29) | **Kreditorenname**, **Belegart**, **Belegnr.**, **Fälligkeitsdatum (Jahr)**, **Fälligkeitsdatum (Monat)** und **Restbetrag**. |

## <a name="example-goods-received-not-invoiced-grni-overview"></a>Beispiel: Übersicht über eingegangene, nicht in Rechnung gestellte Waren (GRNI)

Um eine Übersicht über eingegangene, nicht in Rechnung gestellte Waren (GRNI) für alle Kreditoren zu erstellen, gehen Sie wie folgt vor:

1. Öffnen Sie die Listenseite [Einkaufszeilen](https://businesscentral.dynamics.com/?page=518).
1. Personalisieren Sie die Seite, um das Feld **Betrag – eingegangen, nicht fakturiert** hinzuzufügen. Um die Seite zu personalisieren, wählen Sie **Einstellungen** und dann **Personalisieren**.
1. Wählen Sie :::image type="content" source="media/analysis-mode-icon.png" alt-text="In den Analysemodus wechseln"::: aus. um den Analysemodus einzuschalten.
1. Gehen Sie zum Menü **Spalten** und entfernen Sie alle Spalten (wählen Sie das Kästchen rechts neben dem Feld **Suchen** aus).
1. Legen Sie im Menü **Weitere Filter** (rechts unter dem Menü **Spalten**) die folgenden Filter fest:
    - **Typ = Artikel**
    - **Betrag – eingegangen, nicht fakturiert (MW) > 0**. 
1. Ziehen Sie die Felder **Kreditorennr.**, **Belegnr.** und die **Nr.** in den Bereich **Zeilengruppen**. Ziehen Sie die Felder in dieser Reihenfolge.
1. Fügen Sie das Feld **Betrag – eingegangen, nicht fakturiert (LW)** hinzu, um es in die Übersicht aufzunehmen.
1. Um die Analyse für ein bestimmtes Jahr oder Quartal durchzuführen, wenden Sie einen Filter im Menü **Analysefilter** an. Das Menü befindet sich rechts auf der Seite, direkt unter dem Menü **Spalten**.
1. Benennen Sie Ihre Analyseregisterkarte in **Eingegangene, nicht fakturierte Waren (GRNI)** oder in etwas anderes um, das diese Analyse beschreibt.

## <a name="example-finance-accounts-payable"></a>Beispiele: Finanzen (Kreditorenkonten)

Gehen Sie wie folgt vor, um herauszufinden, wie viel Sie Ihren Kreditoren, eventuell aufgeschlüsselt nach Fälligkeitszeiträumen, schulden:

1. Öffnen Sie die Listenseite [Kreditorenposten](https://businesscentral.dynamics.com/?page=29) und aktivieren Sie den Analysemodus.
1. Gehen Sie zum Menü **Spalten** und entfernen Sie alle Spalten (wählen Sie das Kästchen rechts neben dem Feld **Suchen** aus).
1. Aktivieren Sie den Schalter **Pivot**-Modus (rechts über dem Feld **Suchen**).
1. Ziehen Sie die Felder **Kreditorenname**, **Belegart** und **Belegnr.** in den Bereich **Zeilengruppen** und ziehen Sie dann das Feld **Restbetrag** in den Bereich **Werte**.
1. Ziehen Sie die Felder **Fälligkeitsdatum (Jahr)** und **Fälligkeitsdatum (Monat)** in den Bereich **Spaltenbeschriftungen**. Ziehen Sie die Felder in dieser Reihenfolge.
1. Um die Analyse auf ein bestimmtes Jahr oder Quartal zu beschränken, wenden Sie im Menü **Analysefilter** (rechts unter dem Menü **Spalten**) einen Filter an.
1. Benennen Sie Ihre Analyseregisterkarte in **Kreditorenkontorückblick nach Monat** oder in etwas anderes um, das diese Analyse beschreibt.

Das folgende Bild zeigt das Ergebnis dieser Schritte.

:::image type="content" source="media/data-analysis-vendor-ledger-entries.png" alt-text="Beispiel für die Durchführung einer Datenanalyse auf der Seite „Debitorenposten“." lightbox="media/data-analysis-vendor-ledger-entries.png":::

## <a name="data-foundation-for-ad-hoc-analysis-on-purchasing"></a>Datengrundlage für Ad-hoc-Analysen zum Einkauf

Wenn Sie einen Einkaufsbeleg buchen, aktualisiert [!INCLUDE [prod_short](includes/prod_short.md)] das Kreditorenkonto, das Sachkonto, die Artikelkontoposten und die Ressourcenkontoposten:

- Für jeden Einkaufsbeleg wird ein Einkaufseintrag in der Tabelle **Sachposten** angelegt. Darüber hinaus wird ein Posten in der Tabelle **Lieferantenposten** erzeugt und ein Sachposten im entsprechenden Einkaufskonto. Darüber hinaus führt die Buchung des Einkaufs eventuell zu einer Mehrwertsteuerbuchung (MwSt.) und einem Sachposten für den Rabattbetrag.

- Für jede Einkaufszeile werden, falls anwendbar. die folgenden Einträge erstellt:
  - Tabelle **Artikelposten**, wenn die Einkaufszeile den Typ Artikel ist.
  - Tabelle **Sachposten**, wenn die Einkaufszeile vom Typ Sachkonto ist.
  - **Ressourcenposten**, wenn die Einkaufszeile vom Typ Ressourcen ist.
- Darüber hinaus werden Einkaufsbelege immer im Feld **Einkaufslieferkopf** und **Einkaufsrechnungskopf** Tabellen erfasst.

Weitere Informationen unter [Einkäufe buchen](purchasing-how-record-purchases.md#posting-purchases).

## <a name="see-also"></a>Siehe auch

[Einkäufe buchen](purchasing-how-record-purchases.md#posting-purchases)  
[Listen- und Abfragedaten mit dem Analysemodus analysieren](analysis-mode.md)  
[Analysen, Business Intelligence und Berichterstellung – Übersicht](reports-bi-reporting.md)  
[Einkauf – Übersicht](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
