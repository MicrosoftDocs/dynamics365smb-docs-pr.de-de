---
title: Daten in Business Central eingeben
description: Es gibt viele allgemeine Funktionen, die Ihnen helfen, Daten einfacher, schneller und präziser einzugeben. Hier werden die grundlegenden Prinzipien und erweiterten Funktionen beschrieben.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: decimal separator, data entry, focus
ms.search.form: 9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017
ms.date: 03/23/2022
ms.author: jswymer
ms.openlocfilehash: ecf23184faea42895973d11115904606d715d31a
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9528619"
---
# <a name="entering-data" /><a name="entering-data"></a>Eingeben von Daten

Es gibt viele allgemeine Funktionen, die Ihnen helfen, Daten einfacher, schneller und präziser einzugeben. Die Grundprinzipien und erweiterten Funktionen für die Eingabe von Daten werden in diesem Artikel beschrieben.  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

Die Beispiele in diesen Artikel verwendet die Demodaten.

## <a name="work-with-editable-fields" /><a name="work-with-editable-fields"></a>Mit bearbeitbaren Feldern arbeiten

Felder in [!INCLUDE[prod_short](includes/prod_short.md)] können verschiedene bearbeitbare Daten enthalten, z. B. Text oder Währungsbeträge. Bearbeitbare Felder zeigen in der Regel ein Eingabefeld an, in das Sie einen Wert eingeben bzw. aus dem Sie einen Wert auswählen können. Nicht bearbeitbare Felder werden normalerweise mit einem grauem Hintergrund angezeigt.   

Einige bearbeitbare Felder bieten eine Auswahl, anhand derer Sie einen Wert festlegen können.  

<!-- TODO: Add illustrations or images of each picker -->
|**Kommissionierer**        |**So können Sie einen Wert festlegen**|
|------------------|------------------------------------|
|Datumsauswahl       |Diese Auswahl zeigt einen Kalender an, der auf Ihren aktuellen regionalen Einstellungen basiert. Dieser ermöglicht die Auswahl eines einzelnen Datums.|
|Dropdownliste          |Dropdownlisten bieten eine Auswahl an festen Werten oder Referenzdatensätzen aus einer anderen Tabelle.|
|Schalter oder Kontrollkästchen|Einige Felder bieten eine einfache Auswahl von *Ja*- oder *Nein*-Werten. Dieser Wert wird mit dem Schalter festgelegt und in Listen immer als Kontrollkästchen angezeigt.|
|AssistEdit       |Einige Felder bieten benutzerdefinierte Auswahlfelder zum Suchen und Auswählen des besten Werts für dieses Feld, z. B. ein Popup-Fenster.|

### <a name="modifying-a-field-value" /><a name="modifying-a-field-value"></a>Ändern eines Feldwerts

Um den Wert eines Felds zu ändern, müssen Sie zuerst den Fokus auf dieses Feld legen. Führen Sie dazu die folgenden Aktionen aus:

- Verwenden Sie die **TAB**-Taste. Die Aktion wählt den gesamten Wert aus.
- Klicken Sie mit der linken Maustaste oder einem ähnlichen Eingabegerät. Diese Aktion wählt nur den gesamten Feldwert aus, wenn sich das Feld in einer Liste befindet.  

Wenn Sie mit Feldern in der Benutzeroberfläche interagieren, bevorzugt [!INCLUDE[prod_short](includes/prod_short.md)] in der Regel die Auswahl des gesamten Feldwerts, damit Sie diesen Wert leichter ersetzen können.

Gehen Sie wie folgt vor, wenn der gesamte Feldwert ausgewählt ist:
- Ersetzen Sie den Wert einfach durch die Eingabe eines neuen Werts, um diesen festzulegen. Wenn das Feld eine Auswahl bietet, können Sie diese mit der Tastenkombination **Alt + Pfeil nach unten** aktivieren.
- Verwenden Sie die Taste **Löschen** oder die **Rücktaste**, um den Wert zu löschen.

Drücken Sie die Taste **F2**, um zwischen der Auswahl des gesamten Feldwerts oder der Platzierung des Cursors hinter dem Wert des Felds umzuschalten. Wenn Sie den Cursor am Ende des Werts platzieren, können Sie ihn leichter an den vorhandenen Wert anhängen.

Wenn der Cursor am Ende des Feldwerts angezeigt wird:
- Fügen Sie den Wert hinzu, indem Sie ihn einfach eingeben.
- Verwenden Sie die **POS1**-, **ENDE**-, **NACH-LINKS**- und **NACH-RECHTS**-Taste, um den Cursor innerhalb des Werts zu bewegen. Wenn Sie beim Bearbeiten eines Felds in einer Liste die **NACH-LINKS**-TASTE erneut drücken, wenn sich der Cursor am Anfang des Werts befindet, wird der Fokus wieder auf das vorherige Feld gelegt. Wenn Sie die **NACH-RECHTS**-TASTE erneut drücken, während sich der Cursor am Ende des Werts befindet, wird der Fokus entsprechend auf das nächste Feld gelegt.

> [!NOTE]
> Nachdem Sie einen Wert angegeben haben, überprüft Business Central dessen Gültigkeit erst, wenn Sie außerhalb des Felds klicken oder den Fokus auf ein anderes Element wie das nächste Feld legen.  

[!INCLUDE [background_doc_journal_check](includes/background_doc_journal_check.md)]

## <a name="keyboard-shortcuts" /><a name="keyboard-shortcuts"></a>Tastenkombinationen

Es gibt verschiedene Tastenkombinationen, mit denen Sie ohne Maus arbeiten und die Dateneingabe beschleunigen können. Diese Tastenkombinationen sind besonders hilfreich bei umfangreichen Einträgen und wiederkehrenden Eingabeaufgaben.

Weitere Informationen zu diesen Tastenkombinationen finden Sie unter [Tastenkombinationen](keyboard-shortcuts.md). Einige der Tastenkombinationen werden in diesem Artikel erläutert.

## <a name="a-namequickentryaaccelerating-data-entry-using-quick-entry" /><a name="accelerating-data-entry-using-quick-entry"></a><a name="QuickEntry"></a>Beschleunigende der Dateneingabe mithilfe der Schnelleingabe

Die Schnelleingabe ist eine Funktion für die Dateneingabe bei Verwendung der Tastatur. Schnelleingabe funktioniert bei Feldern (wie in Kartenseiten) und in Listen (Zeilen und Spalten). Dies ist hilfreich, wenn Sie sich wiederholende Eingabeaufgaben ausführen, bei denen mehrere Datensätze nacheinander erstellt werden müssen. Beispiele hierfür sind eine Gruppe von Kundenaufträgen oder die Registrierung neuer Artikel.

Mit der TAB-TASTE können Sie von einem Feld einer Seite zum nächsten bearbeitbaren Feld navigieren. Der Nachteil der Anwendung von TAB ist, dass sie stets fortlaufend zum nächsten Feld navigiert. <!-- even if the field is non-editable or seldom filled it in.-->Mit Schnelleintrag können Sie den Pfad ändern. Bei der Schnelleingabe können Sie die EINGABETASTE verwenden, um nur durch die Felder zu navigieren, die Sie interessieren. Die Schnelleingabe überspringt nicht bearbeitbare Felder sowie Felder, die Sie in der Regel nicht ausfüllen. Sie haben dieses Verhalten möglicherweise bereits auf einigen Seiten bemerkt. Der Grund für dieses Verhalten besteht darin, dass vordefiniert ist, welche Felder beim Drücken der EINGABETASTE einbezogen und welche übersprungen werden sollen. Sie können die Schnelleingabe anpassen, indem Sie den Arbeitsbereich personalisieren und optimieren, wie Sie Daten auf jeder Seite eingeben.

### <a name="how-quick-entry-works" /><a name="how-quick-entry-works"></a>So funktioniert die Schnelleingabe

Jedes Feld kann als *in Schnelleingabe enthalten* oder *aus Schnelleingabe ausgeschlossen* markiert werden. Felder, die in die Schnelleingabe eingeschlossen sind, werden in den Pfad aufgenommen, wenn Sie die EINGABETASTE drücken. Felder, die von der Schnelleingabe ausgeschlossen sind, hingegen nicht.

Wenn Sie die Dateneingabe in einem Feld beendet haben, drücken Sie einfach die EINGABETASTE, um die Änderungen zu bestätigen und zum nächsten Feld zu wechseln. Wenn Sie die Richtung umkehren und zum vorherigen Feld gehen möchten, drücken UMSCHALTTASTE+EINGABETASTE. Weitere Informationen zu diesen Tastenkombinationen unter [Tastenkombinationen der Schnelleingabe für Felder](keyboard-shortcuts.md#QuickEntry).

#### <a name="tips-and-tricks" /><a name="tips-and-tricks"></a>Tipps und Tricks

Nachfolgend sind einige nützliche Informationen zur Anwendung der Schnelleingabe aufgeführt.

- Sie ist für alle bearbeitbaren Felder verfügbar.
- Sie funktioniert auch über Spalten und Zeilen hinweg.
- Sie verhindert nicht den Zugriff auf andere Elemente einer Seite wie Aktionen. Auf diese Elemente kann noch mit TAB und UMSCHALT+TAB zugegriffen werden.  
- Es ist nicht erforderlich, dass Inforegister erweitert werden, damit die Schnelleingabe funktioniert. Wenn sich das nächste Feld der Schnelleingabe in einem reduzierten Inforegister befindet, wird das Inforegister automatisch mit Fokus auf dem ausgewählten Feld erweitert. [!INCLUDE[prod_short](includes/prod_short.md)] erweitert das Inforegister automatisch beim nächsten Besuch der Seite.  
- Schnelleingabe funktioniert unabhängig davon, ob Felder erforderlich sind. Daher ist es vorteilhaft, sicherzustellen, dass erforderliche Felder in der Schnelleingabe enthalten sind.
- Standardmäßig sind die meisten Felder automatisch im der Schnelleingabe enthalten. Daher wird die Aufgabe höchstwahrscheinlich zunächst darin bestehen, Felder aus der Schnelleingabe auszuschließen.

### <a name="to-change-quick-entry-fields" /><a name="to-change-quick-entry-fields"></a>Um Felder der Schnelleingabe zu ändern

Verwenden Sie die Personalisierung, um die Schnelleingabe für Felder einzurichten.

1. Starten Sie die Personalisierung, indem Sie das Symbol ![Einstellungen.](media/ui-experience/settings_icon_small.png "Einstellungssymbol für Rollenzentrum") Symbol und dann die Aktion **Personalisieren**.
2. Wählen Sie ein Feld aus, das Sie ändern möchten. Wählen Sie in Listen die entsprechende Spaltenüberschrift aus. Wählen Sie dann **In Schnelleingabe einschließen** oder **Von der Schnelleingabe ausschließen** aus.

Weitere Informationen zur Personalisierung finden Sie unter [Personalisieren Ihres Arbeitsbereichs](ui-personalization-user.md).

## <a name="mandatory-fields" /><a name="mandatory-fields"></a>Pflichtfelder

Wenn Sie Daten auf Seiten in eingeben, werden bestimmte Felder mit einem roten Sternchen markiert. Das rote Sternchen bedeutet, dass das Feld ausgefüllt werden muss, um einen bestimmten Vorgang abzuschließen. Ein Beispiel wäre, wenn Sie eine Transaktion buchen, die den Wert in dem Feld verwendet.  

Auch wenn ein Feld obligatorisch ist, sind Sie nicht gezwungen, das Feld auszufüllen, bevor Sie mit anderen Feldern fortfahren oder die Seite schließen. Das rote Sternchen dient nur als Erinnerung, dass Sie daran gehindert wurden, einen bestimmten Prozess zu beenden.  

## <a name="finding-data-as-you-type" /><a name="finding-data-as-you-type"></a>Suchen von Daten bei der Eingabe

 Wenn Sie mit der Eingabe von Zeichen in einem Feld beginnen, wird eine Dropdownliste mit möglichen Feldwerten angezeigt. Die Anzeige der Dropdownliste ändert sich bei Eingabe weiterer Zeichen, und Sie können den korrekten Wert auswählen, wenn dieser angezeigt wird.  

 Viele Felder haben eine Schaltfläche mit einem nach unten zeigenden Pfeil, den Sie auswählen können. Durch Klicken auf diesen Pfeil wird eine Liste der Daten angezeigt, die in das Feld eingegeben werden können. Die Schaltfläche bietet abhängig vom Feldtyp zwei Funktionen:  

- Lookup – Zeigt Informationen aus einer anderen Tabelle an, die im Feld eingegeben werden können. Es kann jeweils ein Datenelement ausgewählt werden.  

- Dropdown – Zeigt die Optionen an, die für das Feld verfügbar sind. Sie können nur eine der Optionen auswählen.  

## <a name="copying-and-pasting-faq-fields-and-lines" /><a name="copying-and-pasting-faq-fields-and-lines"></a>FAQ Felder und Zeilen kopieren und einfügen

Sie können eine oder mehrere Zeilen aus einer Liste oder einem einzelnen Feld auf einer Seite kopieren. Fügen Sie dann die kopierten Daten in dieselbe Seite, in eine andere Seite oder in ein externes Dokument ein. Sie können Daten beispielsweise in Microsoft Excel oder in eine Outlook-E-Mail einfügen. Drücken Sie zum Kopieren STRG+C (cmd+C in Mac Os) auf Ihrer Tastatur. Zum Einfügen drücken Sie STRG+V oder cmd+V in Mac Os.

Um das Feld in einer Liste in der gleichen Spalte der Zeile darüber zu kopieren, und es in die aktuelle Zeile einzufügen, drücken Sie einfach F8.

Weitere Informationen finden Sie unter [FAQ zum Kopieren und Einfügen](faq-copy-paste.yml).

## <a name="filtering-line-items" /><a name="filtering-line-items"></a>Filtern von Positionsartikel

Um mit dem Filtern zu beginnen, wählen Sie ![Filterbereichssymbol](media/open-filter-pane-icon.png "Filterbereichssymbol") in der Liste oben aus, oder drücken Sie auf UMSCHALT+F3, um den Filterbereich zu öffnen. Sie arbeiten mit Filterbereich, wie in jeder anderen Liste. Weitere Informationen finden Sie unter [Filterung](ui-enter-criteria-filters.md#filtering).

Die Filterung ist besonders dann hilfreich, wenn längere Belege angezeigt und analysiert werden. Stellen Sie sich vor, Sie öffnen eine gebuchte Verkaufsrechnung. Anschließend filtern Sie die Positionen, um alle Positionen mit einem individuellen Rabatt von mehr als 5 % anzuzeigen. Oder Sie filtern die Positionen, sodass nur Fahrradzubehör, dessen Name „Pro“ enthält, angezeigt wird.

## <a name="a-namefocusafocusing-on-line-items" /><a name="focusing-on-line-items"></a><a name="Focus"></a>Fokussieren auf Positionsartikel

Wenn Sie an Dokumenten arbeiten, die einen Positionsartikelteil enthalten, können Sie die Ansicht so ändern, dass der Fokus nur auf die Positionsartikel gelegt wird. Beispieldokumente sind Verkaufsauftrags- oder Rechnungsseite. Der Positionsartikelteil wird erweitert, sodass er fast den gesamten Arbeitsbereich einnimmt. Es verdeckt andere Teile der Seite, mit Ausnahme des Aktionsbereichs am oberen Rand. Dieses Layout ermöglicht Ihnen einen besseren Überblick über die Positionsartikel und bietet mehr Platz, um daran zu arbeiten.

Dies ist besonders hilfreich, wenn Sie mit großen Positionsartikellisten arbeiten und Daten schnell eingeben möchten. Diese Funktion bietet auch erweiterte Filterfunktionen. Wie bei anderen Listen wird das Durchsuchen von Positionsartikeln noch einfacher.

### <a name="switching-the-focus-on-and-off" /><a name="switching-the-focus-on-and-off"></a>Den Fokus zwischen An- und Ausschalten wechseln

Um den Fokus auf die Elemente der Zeile zu setzen, wählen Sie eine beliebige Stelle im Teil der Zeile aus und wählen dann das Symbol ![Fokusmodus.](media/focus-mode.png "Fokusmodus-Symbol") in der oberen rechten Ecke, oder drücken Sie Strg+Umschalt+F12.

Um wieder in die normale Ansicht zu wechseln, wählen Sie ![Fokusmodus Symbol.](media/focus-mode.png "Fokusmodus-Symbol") oder drücken Sie erneut Strg+Umschalt+F12.

## <a name="multitasking-across-multiple-pages" /><a name="multitasking-across-multiple-pages"></a>Multitasking über mehrere Seiten

Sie können eine Karten- oder Dokumentseite in einem neuen Fenster öffnen. Wenn Sie ein neues Fenster öffnen, können Sie:

- an mehreren Aufgaben gleichzeitig arbeiten
- Unterbrechungen der aktuellen Aufgabe verwalten, z. B. einen eingehenden Anruf annehmen
- ein Fenster für eine laufende Aufgabe geöffnet lassen, während Sie eine andere Aufgabe in Fenstern starten oder abschließen

Um die aktuelle Karte oder den aktuellen Beleg in einem neuen Fenster zu öffnen, wählen Sie ![Neues Fenster öffnen.](media/open-new-window-icon.png "Symbol „Neues Fenster öffnen“") in der oberen rechten Ecke, oder drücken Sie Alt+Umschalt+W.

<!--
When working on multiple tasks at a time or when managing interruptions to the current task, such as taking an incoming call, you can open a card or document page in a new window. This allows you to keep a window open for an ongoing task while you start or complete another task in one or more other windows.
-->
Um die aktuelle Karte oder den aktuellen Beleg in einem neuen Fenster zu öffnen, wählen Sie ![Neues Fenster öffnen.](media/open-new-window-icon.png "Symbol „Neues Fenster öffnen“") in der oberen rechten Ecke, oder drücken Sie Alt+Umschalt+W.

> [!NOTE]
> Wenn Sie andere Seiten von einer Karte oder einem Beleg öffnen, der in einem neuen Fenster geöffnet ist, werden diese Seiten in einem neuen Fenster geöffnet, auch wenn Sie nicht ![Neues Fenster öffnen.](media/open-new-window-icon.png "Symbol „Neues Fenster öffnen“") wählen.

> [!NOTE]
> Wenn Sie im Safari-Browser arbeiten, kann ein Popupblocker dazu führen, dass das neue Fenster nicht geöffnet wird. In diesem Fall geben Sie die Produkt-URL als zulässige Website an. Weitere Informationen finden Sie unter [Ändern Sie die Einstellungen in Safari](https://go.microsoft.com/fwlink/?LinkId=2102965).<br /><br />
> Das Gleiche kann auch in anderen Browsern wie Firefox passieren. Weitere Informationen finden Sie unter [Popupblocker-Einstellungen in Firefox](https://go.microsoft.com/fwlink/?LinkId=2116400).  

Eine andere Möglichkeit, Multitasking zu betreiben, besteht darin, die [!INCLUDE[prod_short](includes/prod_short.md)] auf zwei oder mehr Browser-Registerkarten zu öffnen. Wenn Sie dies tun, sollten Sie eine neue Registerkarte erstellen und dann die URL der ursprünglichen Registerkarte in die neue Registerkarte kopieren/einfügen. Dadurch wird eine neue Sitzung erstellt.   

> [!NOTE]
> Verwenden Sie nicht die Funktion **Duplizieren** des Browsers, um die neue Registerkarte zu erstellen, da dies dazu führen kann, dass Aktionen auf einer Registerkarte Aktionen auf anderen Registern blockieren, weil sie Teil derselben Sitzung sind.

## <a name="entering-quantities-by-calculation" /><a name="entering-quantities-by-calculation"></a>Eingeben von Mengen durch Berechnung

Beim Eingeben von Zahlen in die Mengenfelder, beispielsweise in das Feld **Menge** in einer Artikel Buch.-Blattzeile, kann anstelle der Summenmenge die Formel eingegeben werden.  

### <a name="examples" /><a name="examples"></a>Beispiele

- Bei Eingabe von 19+19 wird im Feld als Wert 38 angezeigt.  

- Bei Eingabe von 41-9 wird im Feld als Wert 32 angezeigt.  

- Bei Eingabe von 12*4 wird im Feld als Wert 48 angezeigt.  

- Bei Eingabe von 12/4 wird im Feld als Wert 3 angezeigt.  

## <a name="entering-negative-numbers" /><a name="entering-negative-numbers"></a>Eingeben von negativen Zahlen

Sie können negative Zahlen auf zwei Arten eingeben. Die Zahl. -20,5 kann so eingegeben werden:  

- -20.5  

  Oder
- 20.5-  

In beiden Fällen wird der Betrag als -20,5 erfasst.  

Wenn das letzte Zeichen des Ausdrucks **+** oder **-** ist, wird der gesamte Ausdruck mit diesem Vorzeichen erfasst. Ein Beispiel, **10-20+** ergibt 10 und nicht -10.  

## <a name="entering-dates-and-times" /><a name="entering-dates-and-times"></a>Daten und Zeit eingeben

Datums- und Uhrzeitwerte können in alle Felder eingegeben werden, die für Datumswerte vorgesehen sind (Datumsfelder). Datumswerte können mit oder ohne Trennzeichen eingegeben werden.

> [!NOTE]  
> Wie Sie Daten und Uhrzeiten eingeben, hängt von Ihren Einstellungen in Ihrer **Region** ab. Weitere Informationen finden Sie unter [Ändern der Grundeinstellungen](ui-change-basic-settings.md).  

### <a name="entering-dates" /><a name="entering-dates"></a>Eingeben von Datumswerten

Sie können entweder die Datenauswahl verwenden, um ein Datum aus einem Kalender auszuwählen, oder Sie können Daten manuell eingeben. Dieser Abschnitt bietet eine kurze Übersicht über die Dateneingabe. Weitere Informationen finden Sie unter [Mit Datumsangaben und Uhrzeiten in Kalendern arbeiten](ui-enter-date-ranges.md).

Für manuelle Eingabe von Datumsangaben können zwei-, vier-, sechs- oder achtstellige Werte eingegeben werden:  

- Zwei Ziffern werden als Tag interpretiert. Der Monat und das Jahr des Arbeitsdatums werden hinzugefügt.  

- Vier Ziffern werden als Tag und Monat interpretiert. Das Jahr des Arbeitsdatums wird hinzugefügt.  

- Wenn das gewünschte Datum im Bereich vom 01.01.1950 bis zum 31.12.2049 liegt, geben Sie das Jahr zweistellig ein. Andernfalls geben Sie das Jahr vierstellig ein.

  > [!NOTE]
  > Wenn Sie [!INCLUDE[prod_short](includes/prod_short.md)] lokal verwenden, kann der zweistellige Jahresbereich abweichen. Administratoren können den Bereich ändern, indem sie die **CalendarTwoDigitYearMax**-Einstellung des [!INCLUDE[prod_short](includes/prod_short.md)]-Servers ändern. Weitere Informationen finden Sie unter [Konfigurieren von Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General).

Sie können auch ein Datum als Wochentag gefolgt von einer Wochennummer eingeben. Oder Sie können ein Jahr eingeben. Beispielsweise bedeutet Mo25 oder mo25 Montag in der 25. Woche  

Anstatt ein bestimmtes Datum direkt einzugeben, können Sie auch einen dieser Codes verwenden.  

|Code|Ergebnis|  
|--------------|----------------|  
|h|Gibt das heutige Datum (das Systemdatum des Computers) an.|  
|p|Gibt eine Buchhaltungsperiode an, wobei p die erste Buchhaltungsperiode bezeichnet, p2 die zweite Buchhaltungsperiode angibt usw. |
|a|Gibt das Arbeitsdatum an, das in der Anwendung eingerichtet wird. Um das Arbeitsdatum zu ändern, siehe [Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md). Die Verwendung des Arbeitsdatums ist hilfreich, wenn eine Vielzahl von Transaktionen zu einem Datum ausgeführt werden müssen, das vom Systemdatum abweicht.|
|a|Gibt an, dass das Datum nach a ein Abschlussdatum ist, beispielsweise A31.12.01.|  

## <a name="entering-times" /><a name="entering-times"></a>Eingeben von Uhrzeiten

Beim Eingeben von Uhrzeiten kann zwischen den Zeiteinheiten ein beliebiges Trennzeichen (oder auch kein Trennzeichen) verwendet werden. Die Angabe von Minuten, Sekunden oder AM/PM ist nicht erforderlich.  

In der folgenden Tabelle finden Sie eine Übersicht über die Möglichkeiten zum Angeben von Uhrzeiten sowie die Interpretation der jeweiligen Angabe.  

|Eingabe|Interpretation|  
|---------------|------------------------|  
|5|05:00:00|  
|5:30|05:30:00|  
|0530|05:30:00|  
|5:30:5|05:30:05|  
|053005|05:30:05|  
|5:30:05:50|05:30:05:50|  
|053005050|05:30:05.05|  

 Wird kein Trennzeichen verwendet, müssen für jede Zeiteinheit zwei Zeichen eingegeben werden.  

## <a name="entering-combined-datetimes" /><a name="entering-combined-datetimes"></a>Eingeben kombinierter Datums‑ und Zeitangaben

[!INCLUDE [datetimes](includes/datetimes.md)]

## <a name="entering-duration" /><a name="entering-duration"></a>Eingeben von Terminen

Zeiträume können als Zahl gefolgt von der entsprechenden Einheit eingegeben werden.  

Hier folgen einige Beispiele.  

|Termine|Einheit**|  
|------------------|-------------------------|  
|2h|2 Stunden|  
|6 Std. 30 Min.|6 Stunden 30 Minuten|  
|6,5 Std.|6 Stunden 30 Minuten|  
|90 Min.|1 Stunde 30 Minuten|  
|2 T 6 Std. 30 Min.|2 Tage 6 Stunden 30 Minuten|  
|2d 6h 30m 56s 600ms|2 Tage 6 Stunden 30 Minuten 56 SeDebitoren 600 MilliseDebitoren|  

 Sie haben auch die Möglichkeit, eine Zahl einzugeben, die dann automatisch in einen Zeitraum umgewandelt wird. Die eingegebene Zahl wird entsprechend der Standardeinheit konvertiert, die im Feld "Dauer" definiert ist.  

 Geben Sie zum Anzeigen der Einheit, die für ein Feld vom Typ „Dauer“ verwendet wird, eine Zahl ein. Am Ergebnis können Sie ablesen, in welche Einheit diese konvertiert wird.  

 Die Zahl 5 wird in 5 Std. konvertiert, wenn Stunden als Einheit angegeben wurden.  

## <a name="a-namedecimalasetting-the-decimal-separator-used-by-numeric-keyboards" /><a name="setting-the-decimal-separator-used-by-numeric-keyboards"></a><a name="decimal"></a>Festlegen des Dezimaltrennzeichens, das von numerischen Tastaturen verwendet wird

Wenn Sie bei der Eingabe von Daten die Dezimaltrennzeichen-Taste auf einem Ziffernblock verwenden, wird das tatsächliche Dezimaltrennzeichen, das in das Feld eingegeben wird, durch die Regionseinstellung in Business Central bestimmt. Die meisten Regionen verwenden das Symbol Punkt (.) oder Komma (,) als Trennzeichen für Dezimalwerte, wie Sie es normalerweise in Währungsbeträgen sehen würden. Die Dezimaltaste auf Ihrer Tastatur passt sich Ihrer Region an. Sie unterscheidet sich oft von den Punkt- oder Kommatasten auf dem Rest Ihrer Tastatur. Sie legen die Region in Business Central auf der Seite **Meine Einstellungen** fest.

Nehmen wir zum Beispiel an, Sie verwenden eine numerische Tastatur, die einen Punkt (.) als Dezimaltrennzeichen verwendet. Sie geben aber Daten für eine regionale Sprache ein, die ein Komma (**,**) als Dezimaltrennzeichen verwendet, wie z.B. Französisch (Frankreich). Sie möchten also, dass Dezimalzahlen wie „1.23“ als „1,23“ eingegeben werden. In diesem Fall können Sie auf die Seite **Meine Einstellungen** gehen und die **Region** auf die regionale Zielsprache festlegen, wie **Französisch (Frankreich)**. Weitere Informationen finden Sie unter [Grundeinstellungen ändern](ui-change-basic-settings.md#region).

> [!TIP]
> Es kann vorkommen, dass Sie das Dezimaltrennzeichen verwenden möchten, um einen Punkt (.) einzugeben. Angenommen, Sie geben einen Datumsbereich in einen Filter ein, z. B. `01/01/2022..04/01/2022` oder irgendetwas, das einen Punkt erfordert. Um diesen Fall zu berücksichtigen, drücken Sie die Tasten „Alt+Dezimaltrennzeichen“ auf der numerischen Tastatur. Diese Tastenkombination schaltet das Dezimaltrennzeichen zwischen der Ausgabe eines Punktes und dem durch die **Region**-Einstellung festgelegten Dezimaltrennzeichen um.

## <a name="see-related-microsoft-trainingtrainingmodulesexplore-modify-info-dynamics-365-business-central" /><a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/explore-modify-info-dynamics-365-business-central/)

## <a name="see-also" /><a name="see-also"></a>Siehe auch

[Sortieren, Durchsuchen und Filtern von Listen](ui-enter-criteria-filters.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
