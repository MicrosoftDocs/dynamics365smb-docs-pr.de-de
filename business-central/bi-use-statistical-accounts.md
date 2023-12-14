---
title: Verwenden Sie statistische Konten zum Analysieren von nicht transaktionalen Daten
description: 'Beschreibt, wie Sie statistische Konten als weitere Datenquelle für Ihre Analysen verwenden.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/07/2023
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, financial report'
ms.search.form: '2632, 2631, 2633, 2623, 2634'
---
# Analysieren Sie Daten mit statistischen Konten

Verwenden Sie statistische Konten, um Informationen in Finanzberichten zu ergänzen. Mit Statistikkonten können Sie Metriken hinzufügen, die auf Nicht-Transaktionsdaten basieren. Sie fügen die nicht transaktionalen Daten als zahlenbasierte Einheiten hinzu, z. B.:

* Mitarbeiterzahl
* Quadratmeterzahl
* Die Anzahl der Kunden mit überfälligen Konten

Beispielsweise können Sie Einnahmen oder Kosten anhand der Anzahl der Personen in einer Abteilung messen. Der Personalbestand der Abteilung ist die Einheit für die statistische Abrechnung. Die folgende Abbildung zeigt ein Beispiel eines Berichts, der ein statistisches Konto verwendet, um den Umsatz pro Mitarbeiter anzuzeigen.

:::image type="content" source="media/statistical account report example.png" alt-text="Ein Beispiel für einen Bericht, der Daten aus einem statistischen Konto enthält.":::

Statistische Konten ähneln in ihrer Funktionsweise den Buchungskonten. Sie speichern Transaktionen, die Sie mit statistischen Kontenjournalen buchen, damit Sie die Transaktionen als Daten für Finanzberichte verwenden können. Erfahren Sie mehr unter Finanzberichte unter [Bereiten Sie Financial Reporting mit Finanzdaten und Kontengruppen vor](bi-how-work-account-schedule.md). 

Es gibt einige wichtige Unterschiede zwischen statistischen Konten und Buchungskonten. Statistische Konten sind separate Entitäten und nicht in den Berichten über die Testbilanz enthalten. Außerdem müssen Sie Soll- und Habenbeträge nicht ausgleichen, wenn Sie Buchungen für statistische Konten verwenden, um Buchungen auf einem statistischen Konto zu buchen. Sie buchen einfach den Betrag.

## Statistische Konten einrichten

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Statistische Konten** ein und wählen Sie dann den zugehörigen Link.
1. Füllen Sie auf der Registerkarte **Allgemein** die Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Beträge auf ein statistisches Konto buchen

1. Um die Beträge zu buchen, die Sie verfolgen möchten, auf der Seite **Statistische Konten** wählen Sie die Aktion **Journal für statistische Konten** aus.
1. Geben Sie in das Feld **Buchungsdatum** das letzte Datum der Lagerbuchungsperiode ein, für die Sie die Beträge buchen möchten.
1. Optional: Wenn Sie Beträge für ein bestimmtes Dokument nachverfolgen möchten, geben Sie im Feld **Dokument Nr.** die ID des Dokuments ein.
1. Im Feld **Statistische Konto-Nr.** wählen Sie das statistische Konto aus, auf das Sie die Beträge buchen möchten.
1. Geben Sie in dem Feld **Beschreibung** eine kurze Beschreibung ein, was Sie messen.  
1. Geben Sie im Feld **Betrag** den zu buchenden Betrag ein. 
1. Optional: Wenn Sie das statistische Konto in erweiterte Analysen einbeziehen möchten, geben Sie Dimensionen in den Feldern **Abteilungscode** und **Kundengruppencode** ein. Um mehr über Dimensionen zu erfahren, gehen Sie zu [Analysieren Sie Daten nach Dimensionen](bi-how-analyze-data-dimension.md).

## Statistische Kontenbeträge prüfen

Verwenden Sie auf der Seite **Statistische Konten** die Aktion **Statistische Kontensaldo**, um zu überprüfen, ob die registrierten Beträge für jeden Zeitraum korrekt sind.  

## Nehmen Sie das statistische Konto in einen Finanzbericht auf

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol, geben Sie **Finanzberichte** ein und wählen Sie dann den entsprechenden Link.
1. Erstellen Sie auf eine der folgenden Arten einen neuen Finanzbericht:
    1. Um von vorne zu beginnen, wählen Sie **Neu**. Weitere Informationen zum Erstellen von Finanzberichten finden Sie unter [Neuen Finanzbericht erstellen](bi-how-work-account-schedule.md#create-a-new-financial-report).
    1. Um Einstellungen aus einem ähnlichen Bericht zu verwenden, den Sie bereits haben, wählen Sie den zu kopierenden Bericht und dann die Aktion **Finanzbericht kopieren** aus. Sie können die kopierten Einstellungen in Ihrem neuen Bericht bearbeiten.
1. Statistisches Konto hinzufügen:
    1. Wenn Sie bei Null anfangen, wählen Sie die Aktion **Zeilendefinition bearbeiten** .
    1. Um eine Zeilendefinition aus einem bestehenden Bericht zu verwenden, den Sie bereits haben, wählen Sie den zu kopierenden Bericht und dann die Aktion **Zeilendefinitionen kopieren** aus.
1. Auf der Seite **Zeilendefinition** in der **Zeile Nr.** definieren Sie, wo die Zeile in der Zeilenfolge des Berichts erscheinen soll.
1. Geben Sie in dem Feld **Beschreibung** eine kurze Textbeschreibung ein, um zu beschreiben, was Sie messen.
1. Wählen Sie im Feld **Summentyp** **Statistische Konten** aus.
1. Wählen Sie im Feld **Summe** ein statistisches Konto aus.
1. Wählen Sie im Feld **Zeilentyp** aus, ob der Saldo am Buchungsdatum oder am Beginn der Buchungsperiode oder die Änderung des Betrags während der Periode angezeigt werden soll.
1. Füllen Sie die restlichen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Weitere Informationen

[Financial Business Intelligence](bi.md)  
[Finanzberichte und Analysen in Business Central](finance-reports.md)