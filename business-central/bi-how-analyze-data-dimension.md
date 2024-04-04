---
title: Analysieren von Daten nach Dimensionen
description: 'Dieser Artikel beschreibt, wie Sie Geschäftsdaten nach Dimensionen analysieren können, um einen besseren Einblick in Ihr Unternehmen zu erhalten.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '545, 555, 556, 557, 558, 9372, 9370, 9371'
ms.date: 09/22/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Analysieren von Daten nach Dimensionen

In der Finanzanalyse sind Dimensionen Daten, die Sie einem Eintrag als eine Art Markierung hinzufügen. Diese Daten dienen zum Gruppieren von Posten mit ähnlichen Merkmalen – beispielsweise Debitoren, Regionen, Produkte oder Verkäufer – sowie zum einfachen Abrufen dieser Gruppen zur Analyse. Dimensionen können für Posten in Buch.-Blättern, Belegen und Budgets verwendet werden. 

Jede „Dimension“ beschreibt den Schwerpunkt der Analyse. Eine zweidimensionale Analyse wäre z.B. der Umsatz pro Bereich. Wenn Sie beim Erstellen eines Eintrags mehr als zwei Dimensionen verwenden, können Sie eine komplexere Analyse durchführen, z. B. Umsatz pro Verkaufskampagne pro Kundengruppe pro Gebiet. So erhalten Sie einen besseren Einblick in Ihr Unternehmen, z.B. wie gut Ihr Geschäft läuft, wo es floriert und wo nicht, und wo mehr Ressourcen zugewiesen werden sollten, so dass Sie fundiertere Entscheidungen treffen können, wenn Sie vorankommen. Erfahren Sie mehr unter [Arbeiten mit Dimensionen](finance-dimensions.md).

> [!TIP]
> Um Transaktionsdaten schnell nach Dimensionen zu analysieren, können Sie die Summen im Kontenplan (CoA) und die Einträge auf allen **Buchungen**-Seiten nach Dimensionen filtern. Suchen Sie nach der Aktion **Dimensionsfilter festlegen**.

> [!NOTE]
> Wenn Sie feststellen, dass bei gebuchten Sachkonten ein falscher Dimensionswert verwendet wurde, können Sie ihn korrigieren und Ihre Analyseansichten aktualisieren. Mehr dazu erfahren Sie im Abschnitt [Problembehandlung und Korrektur von Dimensionen](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting).

## Eine Analysesicht festlegen

Eine Analyse nach Dimensionen verwendet eine ausgewählte Kombination von Dimensionen. Sie speichern, rufen diese Dimensionen-Kombination ab und aktualisieren sie, indem Sie eine **Analyseansicht**-Karte erstellen. 

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Analyseansichten** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie auf der Seite **Analyseansichtsliste** die Aktion **Neu** aus.
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Um zusätzlich zu den vier Codes auf dem Inforegister **Dimensionen** weitere Dimensionen hinzuzufügen, wählen Sie die Aktion **Filter**, füllen die Felder aus und wählen dann die Schaltfläche **OK**.  
5. Um die Ansicht zu aktualisieren, wählen Sie die **Aktualisieren** Aktion.

## Analysieren nach Dimensionen

Verwenden Sie die Analyseansichten, die Sie bereits mit der **Analyse nach Dimensionen** Matrix festgelegt haben, um die Beträge in Ihrem Hauptbuch zu betrachten.   

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Analyseansichten** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die entsprechende Analysesicht aus und wählen Sie dann die Aktion **Analyse nach Dimensionen**.
3. auf der Seite  **Verkaufsanalyse nach Dimension** füllen Sie die Felder aus, um zu definieren, welche Daten wie angezeigt werden.
4. Wählen Sie die **Matrix anzeigen** Aktion aus, um die für die jeweilige Matrixseite definierte Analyseansicht zu öffnen.
5. Um die Spezifikation eines Betrags auf der Matrixseite anzuzeigen, wählen Sie den Betrag aus.  

- Die Spalten ganz links enthalten Informationen, die auf dem basieren, was Sie im Feld **Als Zeilen anzeigen** in der Kopfzeile ausgewählt haben.  
- Die Spalten ganz rechts enthalten Informationen, die auf dem basieren, was Sie im Feld **Als Spalten anzeigen** in der Kopfzeile ausgewählt haben.

> [!IMPORTANT]  
> Die ausgewählte Periodenlänge muss mindestens der Länge der Periode entsprechen, die auf der Karte **Analyseansicht** für die Datumskomprimierung angegeben ist. Die Befehle **Nächster Satz** und **Vorheriger Satz** sind nicht aktiv, wenn Sie **Periodisch** entweder im Feld **Als Zeilen anzeigen** oder **Als Spalten anzeigen** festgelegt haben.  

> [!NOTE]  
> Sie können den Bericht **Dimensionen - Detail** verwenden, um genau anzeigen zu lassen, wie Dimensionen in einem bestimmten Zeitraum in Posten verwendet wurden. Mit dem Bericht **Dimensionen - Total** können Sie die Anzeige auf die Gesamtbeträge beschränken.  

> [!TIP]  
> Sie können die Ansicht auch ändern, indem Sie den Inhalt der Felder **Als Zeilen anzeigen** und **Als Spalten anzeigen** ändern. Um eine Ansichtseinstellung auszutauschen, wählen Sie die **Zeilen- und Spaltenansicht vertauschen**.

## Eine Analyseansicht aktualisieren

Die auf der Seite **Analyse nach Dimensionen** angezeigten Beträge vermitteln Ihnen ein Bild vom Status der Firma zum Zeitpunkt der letzten Aktualisierung. Um einen Eindruck über den aktuellen Zustand zu erhalten, müssen Sie die Analyseansicht mit der Aktualisierungsfunktion aktualisieren.

Gehen Sie wie folgt vor, um eine Analyseansicht auf der Seite **Analyse nach Dimensionen** zu aktualisieren. Die Schritte sind ähnlich wie bei der Aktualisierung der Seiten **Analyseansicht Karte** und **Analyseansicht Liste**.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Analyseansichten** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die entsprechende Analysesicht aus und wählen Sie dann die Aktion **Analyse nach Dimensionen**.
3. Auf der Seite **Analyse nach Dimensionen** wählen Sie das Feld **Analyseansichtscode**, um die Optionen anzuzeigen aus.  
4. Wählen Sie die Zeile mit der relevanten Analyseansicht aus.  
5. Auf der Seite **Analyseansichten** wählen Sie die Analyseansicht aus und wählen dann die Aktion **Aktualisieren**.  

> [!TIP]  
> Wenn Sie das Kontrollkästchen **Bei Buchung aktualisieren** auf einer Analyseansichtskarte aktivieren, wird die Ansicht automatisch aktualisiert, wenn eine zugehörige Transaktion gebucht wird.

> [!NOTE]  
> Um eine oder alle Analyseansichten gleichzeitig zu aktualisieren, müssen Sie die Stapelverarbeitung **Analyseansichten aktualisieren** verwenden.  

## Siehe auch

[Financial Business Intelligence](bi.md)  
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Das Hauptbuch und der Kontenplan](finance-general-ledger.md)  
[Arbeiten mit Dimensionen](finance-dimensions.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
