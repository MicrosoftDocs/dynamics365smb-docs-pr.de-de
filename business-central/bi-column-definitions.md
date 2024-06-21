---
title: Spaltendefinitionen in Finanzberichten
description: 'Beschreibt, wie Spaltendefinitionen in Finanzberichten funktionieren.'
author: kennieNP
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 03/27/2024
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 488, 489, 490, 764, 765, 766'
ms.service: dynamics-365-business-central
---

# Spaltendefinitionen in Finanzberichten

Verwenden Sie Spaltendefinitionen, um die Spalten anzugeben, die in einen Bericht aufgenommen werden sollen. Zum Beispiel können Sie ein Berichtslayout gestalten, das Bewegung und Saldo für dieselbe Periode dieses und letzten Jahres vergleicht. Eine Spaltendefinition kann bis zu 15 Spalten umfassen. Zum Beispiel sind mehrere Spalten sinnvoll, wenn Sie Budgets für zwölf Monate mit einer Spalte für die Gesamtsumme anzeigen möchten.

## Eine Spaltendefinition erstellen oder bearbeiten

Gehen Sie wie folgt vor, um eine Spaltendefinition zu erstellen oder zu bearbeiten.

> [!NOTE]
> Eine gedruckte, Vorschau- und gespeicherte Version eines Finanzberichts zeigt maximal fünf Spalten an. Wenn ein Finanzbericht dagegen nur für die Analyse auf der Seite **Finanzbericht** gedacht ist, können Sie so viele Spalten erstellen, wie Sie möchten.

1. Wählen Sie auf der Seite **Finanzberichte** den entsprechenden Finanzbericht und dann die Aktion **Spaltendefinition bearbeiten** aus.
1. Erstellen Sie auf der Seite **Spaltendefinition** eine Zeile für jede Spalte mit Finanzdaten, die im Finanzbericht angezeigt wird. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. Wählen Sie **OK** aus.
1. Öffnen Sie die Seite **Finanzbericht** von Zeit zu Zeit, um zu überprüfen, ob die neue Spalte wie gewünscht funktioniert.

## Integrierte Spaltendefinitionen

[!INCLUDE[prod_short](includes/prod_short.md)] bietet Beispielspaltendefinitionen, die Ihnen dabei helfen können, schnell mit der Einrichtung von Finanzberichten zu beginnen, die Ihren Anforderungen entsprechen.

<!-- update this when we release the new templates in 24.1
| Column definition code | Description | How to use this column definition | 
| ------------------- | ----------- | ------------------------------ | 
| TBA 1 | TBA 1 | TBA 1 |
| TBA 2 | TBA 2 | TBA 2 |
| TBA 3 | TBA 3 | TBA 3 |
| TBA 4 | TBA 4 | TBA 4 |
-->

## Beispiel: Eine Spaltendefinition zur Berechnung von Prozentsätzen erstellen

Vielleicht möchten Sie eine Spalte in einen Finanzbericht einfügen, um Prozentsätze einer Summe zu berechnen. Wenn beispielsweise Zeilen vorhanden sind, die den Umsatz nach Dimensionen aufschlüsseln, empfiehlt sich die Einrichtung einer Spalte, die den prozentualen Anteil an den Gesamtverkäufen in jeder Zeile angibt.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 2.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") öffnet. Symbol, geben Sie **Finanzberichte** ein und wählen Sie dann den entsprechenden Link.
1. Wählen Sie auf der Seite **Finanzberichte** einen Finanzbericht aus.  
1. Wählen Sie die Aktion **Finanzbericht bearbeiten**, um eine Finanzberichtszeile festzulegen, um die Summe zu berechnen, auf der die Prozentsätze basieren.  
1. Fügen Sie eine Zeile unmittelbar über der ersten Zeile hinzu, für die Sie einen Prozentsatz anzeigen möchten.  
1. Füllen Sie die Felder in der Zeile wie folgt aus: 
    1. Geben Sie im Feld **Zusammenzählungsart** den Eintrag **Festgelegte Basis für Prozent** ein. 
    1. Geben Sie im Feld **Zusammenzählung** eine Formel für die Summe ein, auf welcher der Prozentsatz basiert. Wenn beispielsweise Zeile 11 die gesamten Verkäufe enthält, geben Sie **11** ein.  
1. Wählen Sie die Aktion **Spaltendefinition bearbeiten**, um eine Spalte festzulegen.  
1. Füllen Sie die Felder in der Zeile wie folgt aus. 
    1. Wählen Sie im Feld **Spaltenart** den Eintrag **Formel** aus. 
    1. Geben Sie in das Feld **Formel** eine Formel für den Betrag ein, für den Sie einen Prozentsatz berechnen möchten, gefolgt von dem Prozentzeichen (%). Wenn also die Spalte Nummer N die Nettoveränderung enthält, geben Sie **N%** ein.  
1. Wiederholen Sie die Schritte 4 bis 7 für jede Gruppe von Zeilen, die Sie nach Prozentsätzen aufschlüsseln möchten.

## Vergleich von Buchhaltungsperioden mit Hilfe von Periodenformeln

Ihr Finanzbericht kann die Ergebnisse verschiedener Buchhaltungsperioden vergleichen, z.B. den vergangenen Monat mit dem gleichen Monat des Vorjahres. Öffnen Sie dazu die Seite **Spaltendefinition** und personalisieren Sie sie, indem Sie das Feld **Vergleich Periodenformel** als Spalte hinzufügen. Erfahren Sie mehr unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md). Sie können dieses Feld dann auf eine Periodenformel setzen.  

Ein Buchhaltungszeitraum muss nicht mit dem Kalender übereinstimmen. Jedes Geschäftsjahr muss jedoch dieselbe Anzahl von Buchhaltungsperioden aufweisen, wobei jede Periode eine andere Länge haben kann.  

[!INCLUDE[prod_short](includes/prod_short.md)] verwendet die Periodenformel, um die Dauer der Vergleichsperiode im Verhältnis zu der Periode zu berechnen, die durch den Datumsfilter im Bericht dargestellt wird. Die Vergleichsperiode basiert auf der Periode des Startdatums des Datumsfilters. In der nachfolgenden Tabelle sind die Abkürzungen für die Periodenangaben aufgeführt.

| Abkürzung | Beschreibung                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| P            | Periode.                                                                                |
| EP           | Endperiode eines Geschäftsjahres, eines Halbjahres oder eines Vierteljahres.                                   |
| CP           | Laufende Periode eines Geschäftsjahres, eines Halbjahres oder eines Vierteljahres. Verwenden Sie CP in Formeln, um den Zeitraum festzulegen, in dem die Formel beginnt oder endet. Zum Beispiel FY\[1..CP\] bezeichnet die Zeit vom Beginn des laufenden Geschäftsjahres bis zur laufenden Periode.|
| GJ           | Geschäftsjahr. Zum Beispiel bezeichnet FY\[1..3\] das erste Quartal des aktuellen Geschäftsjahres. |

Beispiele für Formeln:

| Formel | Beschreibung |
|-----|-----|
| \<Blank\>       | Aktueller Zeitraum. |
| \-1P            | Vorherige Periode.            |
| \-1GJ\[1..EP\]  | Gesamtes vorheriges Geschäftsjahr.                  |
| \-1GJ           | Aktuelle Periode im vorherigen Geschäftsjahr.       |
| \-1GJ\[1..3\]   | Erstes Quartal des vorangegangenen Geschäftsjahres.        |
| \-1GJ\[1..LP\]  | Vom Beginn des vorherigen Geschäftsjahres bis zur aktuellen Periode im vorherigen Geschäftsjahr, einschließlich beider Perioden. |
| \-1GJ\[LP..EP\] | Von der aktuellen Periode im vorigen Geschäftsjahr bis zur letzten Periode des vorigen Geschäftsjahres, einschließlich beider Perioden.   |

Geben Sie für die Berechnung gemäß regulärer Zeitperioden eine Formel in das Feld **Vergleichsdatumsformel** ein. Wenn das Feld z. B. auf -1Y festgelegt ist, bezieht sich [!INCLUDE [prod_short](includes/prod_short.md)] auf die gleiche Periode im Vorjahr.

> [!NOTE]
> Es ist nicht immer offensichtlich, welche Perioden Sie vergleichen, denn Sie können in einem Bericht einen Datumsfilter festlegen, die sich von den Buchhaltungsperioden in Ihrem Kontenplan unterscheiden. Wenn Sie also einen Finanzbericht erstellen, in dem Sie diese Periode mit der gleichen Periode des Vorjahrs vergleichen möchten, legen Sie das Feld **Vergleichsdatum Formel** auf **-1FY** fest. Dann führen Sie den Bericht am **28. Februar** aus und legen die Datumsfilter auf **Januar und Februar** fest. Infolgedessen vergleicht der Finanzbericht den Januar und Februar dieses Jahres mit dem Januar des letzten Jahres, der die einzige abgeschlossene Buchhaltungsperiode des letzten Jahres ist.  

Erfahren Sie mehr unter [Arbeiten mit Kalenderdaten und -zeiten](ui-enter-date-ranges.md).

[!INCLUDE [report-best-practices-column-defs](includes/report-best-practices-column-defs.md)]

## Finanzberichtsspaltendefinitionen importieren oder exportieren

Ab dem 1. Veröffentlichungszyklus 2024 (Version 24.1) können Sie Finanzberichtsspaltendefinitionen als RapidStart-Konfigurationspakete importieren und exportieren. Konfigurationspakete sind beispielsweise hilfreich, um Informationen für andere Unternehmen freizugeben. Das Paket wird in einer .rapidstart-Datei erstellt, die den Inhalt komprimiert.

> [!NOTE]
> Wenn Sie Finanzberichtsspaltendefinitionen importieren, werden bestehende Datensätze mit dem gleichen Namen wie die zu importierenden durch die neuen Definitionen ersetzt. Das Konfigurationspaket für eine Berichtsdefinition überschreibt keine vorhandenen Zeilen- oder Spaltendefinitionen, die in der Berichtsdefinition verwendet werden.

Um Finanzberichtsspaltendefinitionen zu importieren oder zu exportieren, gehen Sie wie folgt vor:

1. Wählen Sie das ![Glühbirne, die das „Sie wünschen ...“-Feature 4 öffnen.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Spaltendefinition** ein, und wählen Sie dann den zugehörigen Link.
1. Wählen Sie die Spaltendefinition und dann die Aktion **Spaltendefinition importieren** oder **Spaltendefinition exportieren** aus, je nachdem, was Sie tun möchten.

## Siehe auch

[Zeilendefinitionen in Finanzberichten](bi-row-definitions.md)  
[Finanzberichte erstellen](bi-how-work-account-schedule.md)  
[Financial Business Intelligence](bi.md)  
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
