---
title: Eingeben von Daten in Business Central | Microsoft Docs
description: Informationen zu allgemeinen Funktionen, die Ihnen dabei helfen, Daten in die Felder einzugeben.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/03/2020
ms.author: sgroespe
ms.openlocfilehash: f3af601f0de00445a42c88bb47053084b05fc14b
ms.sourcegitcommit: 8a4e66f7fc8f9ef8bdf34595e0d3983df4749376
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/15/2020
ms.locfileid: "3262142"
---
# <a name="entering-data"></a>Eingeben von Daten

Es gibt eine Vielzahl allgemeiner Funktionen, mit denen Sie Daten einfacher, schneller und genauer eingeben können. Die Grundprinzipien und erweiterten Funktionen für die Eingabe von Daten werden in diesem Artikel beschrieben.  

Die Beispiele in diesen Artikel verwendet die Demodaten.

## <a name="working-with-editable-fields"></a>Mit bearbeitbaren Feldern arbeiten
Felder in [!INCLUDE[d365fin](includes/d365fin_md.md)] können verschiedene bearbeitbare Daten enthalten, z. B. Text oder Währungsbeträge. Bearbeitbare Felder zeigen in der Regel ein Eingabefeld an, in das Sie einen Wert eingeben bzw. aus dem Sie einen Wert auswählen können. Nicht bearbeitbare Felder werden normalerweise mit einem grauem Hintergrund angezeigt.   

Einige bearbeitbare Felder bieten eine Auswahl, anhand derer Sie einen Wert festlegen können.  

<!-- TODO: Add illustrations or images of each picker -->
|**Kommissionierer**        |**So können Sie einen Wert festlegen**|
|------------------|------------------------------------|
|Datumsauswahl       |Diese Auswahl zeigt einen Kalender an, der auf Ihren aktuellen regionalen Einstellungen basiert. Dieser ermöglicht die Auswahl eines einzelnen Datums.|
|Dropdownliste          |Dropdownlisten bieten eine Auswahl an festen Werten oder Referenzdatensätzen aus einer anderen Tabelle.|
|Schalter oder Kontrollkästchen|Einige Felder bieten eine einfache Auswahl von *Ja*- oder *Nein*-Werten. Dieser Wert wird mit dem Schalter festgelegt und in Listen immer als Kontrollkästchen angezeigt.|
|AssistEdit       |Einige Felder bieten benutzerdefinierte Auswahlfelder zum Suchen und Auswählen des besten Werts für dieses Feld, z. B. ein Popup-Fenster.|


### <a name="modifying-a-field-value"></a>Ändern eines Feldwerts

Um den Wert eines Felds zu ändern, müssen Sie zuerst den Fokus auf dieses Feld legen. Führen Sie dazu die folgenden Aktionen aus:

- Verwenden Sie die **TAB**-Taste. Die Aktion wählt den gesamten Wert aus.
- Klicken Sie mit der linken Maustaste oder einem ähnlichen Eingabegerät. Diese Aktion wählt nur den gesamten Feldwert aus, wenn sich das Feld in einer Liste befindet.  

Wenn Sie mit Feldern in der Benutzeroberfläche interagieren, bevorzugt [!INCLUDE[d365fin](includes/d365fin_md.md)] in der Regel die Auswahl des gesamten Feldwerts, damit Sie diesen Wert leichter ersetzen können.

Gehen Sie wie folgt vor, wenn der gesamte Feldwert ausgewählt ist:
- Ersetzen Sie den Wert einfach durch die Eingabe eines neuen Werts, um diesen festzulegen. Wenn das Feld eine Auswahl bietet, können Sie diese mit der Tastenkombination **Alt + Pfeil nach unten** aktivieren.
- Verwenden Sie die Taste **Löschen** oder die **Rücktaste**, um den Wert zu löschen.

Drücken Sie die Taste **F2**, um zwischen der Auswahl des gesamten Feldwerts oder der Platzierung des Cursors hinter dem Wert des Felds umzuschalten. Wenn Sie den Cursor am Ende des Werts platzieren, können Sie ihn leichter an den vorhandenen Wert anhängen.

Wenn der Cursor am Ende des Feldwerts angezeigt wird:
- Fügen Sie den Wert hinzu, indem Sie ihn einfach eingeben.
- Verwenden Sie die **POS1**-, **ENDE**-, **NACH-LINKS**- und **NACH-RECHTS**-Taste, um den Cursor innerhalb des Werts zu bewegen. Wenn Sie beim Bearbeiten eines Felds in einer Liste die **NACH-LINKS**-TASTE erneut drücken, wenn sich der Cursor am Anfang des Werts befindet, wird der Fokus wieder auf das vorherige Feld gelegt. Wenn Sie die **NACH-RECHTS**-TASTE erneut drücken, während sich der Cursor am Ende des Werts befindet, wird der Fokus entsprechend auf das nächste Feld gelegt.

> [!NOTE]
> Nachdem Sie einen Wert angegeben haben, überprüft Business Central dessen Gültigkeit erst, wenn Sie außerhalb des Felds klicken oder den Fokus auf ein anderes Element wie das nächste Feld legen.  


## <a name="keyboard-shortcuts"></a>Tastenkombinationen

Es gibt verschiedene Tastenkombinationen, mit denen Sie ohne Maus arbeiten und die Dateneingabe beschleunigen können. Diese Tastenkombinationen sind besonders hilfreich bei umfangreichen Einträgen und wiederkehrenden Eingabeaufgaben.

Weitere Informationen zu diesen Tastenkombinationen finden Sie unter [Tastenkombinationen](keyboard-shortcuts.md). Einige der Tastenkombinationen werden in diesem Artikel erläutert.

## <a name="accelerating-data-entry-using-quick-entry"></a><a name="QuickEntry"></a>Beschleunigende der Dateneingabe mithilfe der Schnelleingabe

Die Schnelleingabe ist eine Funktion für die Dateneingabe bei Verwendung der Tastatur. Schnelleingabe funktioniert bei Feldern (wie in Kartenseiten) und in Listen (Zeilen und Spalten). Dies ist hilfreich, wenn Sie sich wiederholende Eingabeaufgaben ausführen, bei denen mehrere Datensätze nacheinander erstellt werden müssen. Beispiele hierfür sind eine Gruppe von Kundenaufträgen oder die Registrierung neuer Artikel.

Mit der TAB-TASTE können Sie von einem Feld einer Seite zum nächsten bearbeitbaren Feld navigieren. Der Nachteil der Anwendung von TAB ist, dass sie stets fortlaufend zum nächsten Feld navigiert. <!-- even if the field is non-editable or seldom filled it in.-->Mit Schnelleintrag können Sie den Pfad ändern. Bei der Schnelleingabe können Sie die EINGABETASTE verwenden, um nur durch die Felder zu navigieren, die Sie interessieren. Die Schnelleingabe überspringt nicht bearbeitbare Felder sowie Felder, die Sie in der Regel nicht ausfüllen. Sie haben dieses Verhalten möglicherweise bereits auf einigen Seiten bemerkt. Der Grund für dieses Verhalten besteht darin, dass vordefiniert ist, welche Felder beim Drücken der EINGABETASTE einbezogen und welche übersprungen werden sollen. Sie können die Schnelleingabe anpassen, indem Sie den Arbeitsbereich personalisieren und optimieren, wie Sie Daten auf jeder Seite eingeben.

### <a name="how-quick-entry-works"></a>So funktioniert die Schnelleingabe

Jedes Feld kann als *in Schnelleingabe enthalten* oder *aus Schnelleingabe ausgeschlossen* markiert werden. Felder, die in die Schnelleingabe eingeschlossen sind, werden in den Pfad aufgenommen, wenn Sie die EINGABETASTE drücken. Felder, die von der Schnelleingabe ausgeschlossen sind, hingegen nicht.

Wenn Sie die Dateneingabe in einem Feld beendet haben, drücken Sie einfach die EINGABETASTE, um die Änderungen zu bestätigen und zum nächsten Feld zu wechseln. Wenn Sie die Richtung umkehren und zum vorherigen Feld gehen möchten, drücken UMSCHALTTASTE+EINGABETASTE. Weitere Informationen zu diesen Tastenkombinationen unter [Tastenkombinationen der Schnelleingabe für Felder](keyboard-shortcuts.md#QuickEntry).

#### <a name="tips-and-tricks"></a>Tipps und Tricks

Nachfolgend sind einige nützliche Informationen zur Anwendung der Schnelleingabe aufgeführt.

- Sie ist für alle bearbeitbaren Felder verfügbar.
- Sie funktioniert auch über Spalten und Zeilen hinweg.
- Sie verhindert nicht den Zugriff auf andere Elemente einer Seite wie Aktionen. Auf diese Elemente kann noch mit TAB und UMSCHALT+TAB zugegriffen werden.  
- Es ist nicht erforderlich, dass Inforegister erweitert werden, damit die Schnelleingabe funktioniert. Wenn sich das nächste Feld der Schnelleingabe in einem reduzierten Inforegister befindet, wird das Inforegister automatisch mit Fokus auf dem ausgewählten Feld erweitert. [!INCLUDE[d365fin](includes/d365fin_md.md)] erweitert das Inforegister automatisch beim nächsten Besuch der Seite.  
- Schnelleingabe funktioniert unabhängig davon, ob Felder erforderlich sind. Daher ist es vorteilhaft, sicherzustellen, dass erforderliche Felder in der Schnelleingabe enthalten sind.
- Standardmäßig sind die meisten Felder automatisch im der Schnelleingabe enthalten. Daher wird die Aufgabe höchstwahrscheinlich zunächst darin bestehen, Felder aus der Schnelleingabe auszuschließen.

### <a name="to-change-quick-entry-fields"></a>Um Felder der Schnelleingabe zu ändern

Verwenden Sie die Personalisierung, um die Schnelleingabe für Felder einzurichten.

1. Beginnen Sie mit der Personalisierung, indem Sie das Symbol ![Einstellungen](media/ui-experience/settings_icon_small.png "Einstellungssymbol für Rollencenter") und dann die Aktion **Personalisieren** auswählen.
2. Wählen Sie ein Feld aus, das Sie ändern möchten. Wählen Sie in Listen die entsprechende Spaltenüberschrift aus. Wählen Sie dann **In Schnelleingabe einschließen** oder **Von der Schnelleingabe ausschließen** aus.

Weitere Informationen zur Personalisierung finden Sie unter [Personalisieren Ihres Arbeitsbereichs](ui-personalization-user.md).

## <a name="mandatory-fields"></a>Pflichtfelder

Wenn Sie Daten auf Seiten in eingeben, werden bestimmte Felder mit einem roten Sternchen markiert. Das rote Sternchen bedeutet, dass das Feld ausgefüllt werden muss, um einen bestimmten Vorgang abzuschließen. Ein Beispiel wäre, wenn Sie eine Transaktion buchen, die den Wert in dem Feld verwendet.  

Auch wenn ein Feld obligatorisch ist, sind Sie nicht gezwungen, das Feld auszufüllen, bevor Sie mit anderen Feldern fortfahren oder die Seite schließen. Das rote Sternchen dient nur als Erinnerung, dass Sie daran gehindert wurden, einen bestimmten Prozess zu beenden.  

## <a name="finding-data-as-you-type"></a>Suchen von Daten bei der Eingabe

 Wenn Sie mit der Eingabe von Zeichen in einem Feld beginnen, wird eine Dropdownliste mit möglichen Feldwerten angezeigt. Die Anzeige der Dropdownliste ändert sich bei Eingabe weiterer Zeichen, und Sie können den korrekten Wert auswählen, wenn dieser angezeigt wird.  

 Viele Felder haben eine Schaltfläche mit einem nach unten zeigenden Pfeil, den Sie auswählen können. Durch Klicken auf diesen Pfeil wird eine Liste der Daten angezeigt, die in das Feld eingegeben werden können. Die Schaltfläche bietet abhängig vom Feldtyp zwei Funktionen:  

-   Lookup – Zeigt Informationen aus einer anderen Tabelle an, die im Feld eingegeben werden können. Es kann jeweils ein Datenelement ausgewählt werden.  

-   Dropdown – Zeigt die Optionen an, die für das Feld verfügbar sind. Sie können nur eine der Optionen auswählen.  

## <a name="copying-and-pasting-faq-fields-and-lines"></a>FAQ Felder und Zeilen kopieren und einfügen

Sie können eine oder mehrere Zeilen aus einer Liste oder einem einzelnen Feld auf einer Seite kopieren. Fügen Sie dann die kopierten Daten in dieselbe Seite, in eine andere Seite oder in ein externes Dokument ein. Sie können Daten beispielsweise in Microsoft Excel oder in eine Outlook-E-Mail einfügen. Drücken Sie zum Kopieren STRG+C (cmd+C in Mac Os) auf Ihrer Tastatur. Zum Einfügen drücken Sie STRG+V oder cmd+V in Mac Os.

Um das Feld in einer Liste in der gleichen Spalte der Zeile darüber zu kopieren, und es in die aktuelle Zeile einzufügen, drücken Sie einfach F8.

Weitere Informationen finden Sie unter [FAQ zum Kopieren und Einfügen](ui-copy-paste.md).

## <a name="filtering-line-items"></a>Filtern von Positionsartikel

Um mit dem Filtern zu beginnen, wählen Sie ![Filterbereichssymbol](media/open-filter-pane-icon.png "Filterbereichssymbol") in der Liste oben aus, oder drücken Sie auf UMSCHALT+F3, um den Filterbereich zu öffnen. Sie arbeiten mit Filterbereich, wie in jeder anderen Liste. Weitere Informationen finden Sie unter [Filterung](ui-enter-criteria-filters.md#filtering).

Die Filterung ist besonders dann hilfreich, wenn längere Belege angezeigt und analysiert werden. Stellen Sie sich vor, Sie öffnen eine gebuchte Verkaufsrechnung. Anschließend filtern Sie die Positionen, um alle Positionen mit einem individuellen Rabatt von mehr als 5 % anzuzeigen. Oder Sie filtern die Positionen, sodass nur Fahrradzubehör, dessen Name „Pro“ enthält, angezeigt wird.

## <a name="focusing-on-line-items"></a><a name="Focus"></a>Fokussieren auf Positionsartikel

Wenn Sie an Dokumenten arbeiten, die einen Positionsartikelteil enthalten, können Sie die Ansicht so ändern, dass der Fokus nur auf die Positionsartikel gelegt wird. Beispieldokumente sind Verkaufsauftrags- oder Rechnungsseite. Der Positionsartikelteil wird erweitert, sodass er fast den gesamten Arbeitsbereich einnimmt. Es verdeckt andere Teile der Seite, mit Ausnahme des Aktionsbereichs am oberen Rand. Dieses Layout ermöglicht Ihnen einen besseren Überblick über die Positionsartikel und bietet mehr Platz, um daran zu arbeiten.

Dies ist besonders hilfreich, wenn Sie mit großen Positionsartikellisten arbeiten und Daten schnell eingeben möchten. Diese Funktion bietet auch erweiterte Filterfunktionen. Wie bei anderen Listen wird das Durchsuchen von Positionsartikeln noch einfacher.

### <a name="switching-the-focus-on-and-off"></a>Den Fokus zwischen An- und Ausschalten wechseln

Um sich auf Zeilenartikel zu konzentrieren, wählen irgendeine Stelle im Bereich des Zeilenartikelteils aus und wählen Sie dann das ![Fokusmodussymbol](media/focus-mode.png "Fokusmodus-Symbol") in der oberen rechten Ecke aus, oder drücken Sie STRG+UMSCHALT+F12.

Um zur Normalansicht zurückzukehren, wählen Sie das ![Fokusmodussymbol](media/focus-mode.png "Fokusmodus-Symbol") aus, oder drücken Sie STRG+UMSCHALT+F12 erneut.

## <a name="multitasking-across-multiple-pages"></a>Multitasking über mehrere Seiten

Sie können eine Karten- oder Dokumentseite in einem neuen Fenster öffnen. Wenn Sie ein neues Fenster öffnen, können Sie:

- an mehreren Aufgaben gleichzeitig arbeiten
- Unterbrechungen der aktuellen Aufgabe verwalten, z. B. einen eingehenden Anruf annehmen
- ein Fenster für eine laufende Aufgabe geöffnet lassen, während Sie eine andere Aufgabe in Fenstern starten oder abschließen

Um die aktuelle Karte oder den aktuellen Beleg in einem neuen Fenster zu öffnen, wählen Sie ![Neues Fenster öffnen](media/open-new-window-icon.png "Symbol „Neues Fenster öffnen“") öffnen in der oberen rechten Ecke, oder drücken Sie Alt + UMSCHALT+W.

<!--
When working on multiple tasks at a time or when managing interruptions to the current task, such as taking an incoming call, you can open a card or document page in a new window. This allows you to keep a window open for an ongoing task while you start or complete another task in one or more other windows.
-->
Um die aktuelle Karte oder den aktuellen Beleg in einem neuen Fenster zu öffnen, wählen Sie ![Neues Fenster öffnen](media/open-new-window-icon.png "Symbol „Neues Fenster öffnen“") öffnen in der oberen rechten Ecke, oder drücken Sie Alt + UMSCHALT+W.

> [!NOTE]
> Wenn Sie andere Seiten über eine Karte oder einen Beleg öffnen, die bzw. der in einem neuen Fenster geöffnet wird, werden diese Seiten auch dann in einem neuen Fenster geöffnet, wenn Sie ![Neues Fenster öffnen](media/open-new-window-icon.png "Symbol „Neues Fenster öffnen“") nicht auswählen.

> [!NOTE]
> Wenn Sie im Safari-Browser arbeiten, kann ein Popupblocker dazu führen, dass das neue Fenster nicht geöffnet wird. In diesem Fall geben Sie die Produkt-URL als zulässige Website an. Weitere Informationen finden Sie unter [Ändern Sie die Einstellungen in Safari](https://go.microsoft.com/fwlink/?LinkId=2102965).<br /><br />
> Das Gleiche kann in anderen Browsern wie Firefox passieren. Weitere Informationen finden Sie unter [Popupblocker-Einstellungen in Firefox](https://go.microsoft.com/fwlink/?LinkId=2116400).  

Eine andere Möglichkeit, Multitasking zu betreiben, besteht darin, die [!INCLUDE[d365fin](includes/d365fin_md.md)] auf zwei oder mehr Browser-Registerkarten zu öffnen. Wenn Sie dies tun, sollten Sie eine neue Registerkarte erstellen und dann die URL der ursprünglichen Registerkarte in die neue Registerkarte kopieren/einfügen. Dadurch wird eine neue Sitzung erstellt.   

> [!NOTE]
> Verwenden Sie nicht die Funktion **Duplizieren** des Browsers, um die neue Registerkarte zu erstellen, da dies dazu führen kann, dass Aktionen auf einer Registerkarte Aktionen auf anderen Registern blockieren, weil sie Teil derselben Sitzung sind.

## <a name="entering-quantities-by-calculation"></a>Eingeben von Mengen durch Berechnung

Beim Eingeben von Zahlen in die Mengenfelder, beispielsweise in das Feld **Menge** in einer Artikel Buch.-Blattzeile, kann anstelle der Summenmenge die Formel eingegeben werden.  

### <a name="examples"></a>Beispiele  

-   Bei Eingabe von 19+19 wird im Feld als Wert 38 angezeigt.  

-   Bei Eingabe von 41-9 wird im Feld als Wert 32 angezeigt.  

-   Bei Eingabe von 12*4 wird im Feld als Wert 48 angezeigt.  

-   Bei Eingabe von 12/4 wird im Feld als Wert 3 angezeigt.  

## <a name="entering-negative-numbers"></a>Eingeben von negativen Zahlen

Sie können negative Zahlen auf zwei Arten eingeben. Die Zahl. -20,5 kann so eingegeben werden:  

-   -20.5  

    Oder
-   20.5-  

 In beiden Fällen wird der Betrag als -20,5 erfasst.  

 Wenn das letzte Zeichen des Ausdrucks **+** oder **-** ist, wird der gesamte Ausdruck mit diesem Vorzeichen erfasst. Ein Beispiel, **10-20+** ergibt 10 und nicht -10.  

## <a name="entering-dates-and-times"></a>Daten und Zeit eingeben

Datums- und Uhrzeitwerte können in alle Felder eingegeben werden, die für Datumswerte vorgesehen sind (Datumsfelder). Datumswerte können mit oder ohne Trennzeichen eingegeben werden.

> [!NOTE]  
> Wie Sie Daten und Uhrzeiten eingeben, hängt von Ihren Einstellungen in Ihrer **Region** ab. Weitere Informationen finden Sie unter [Ändern der Grundeinstellungen](ui-change-basic-settings.md).  

### <a name="entering-dates"></a>Eingeben von Datumswerten

Sie können entweder die Datumsauswahl verwenden, um ein Datum aus einem Kalender auszuwählen, oder Sie können Daten manuell eingeben. Dieser Abschnitt bietet eine kurze Übersicht über die Dateneingabe. Weitere Informationen finden Sie unter [Arbeiten mit Datumsangaben und Uhrzeiten in Kalendern](ui-enter-date-ranges.md).

Für manuelle Eingabe von Datumsangaben können zwei-, vier-, sechs- oder achtstellige Werte eingegeben werden:  

-   Zwei Ziffern werden als Tag interpretiert. Der Monat und das Jahr des Arbeitsdatums werden hinzugefügt.  

-   Vier Ziffern werden als Tag und Monat interpretiert. Das Jahr des Arbeitsdatums wird hinzugefügt.  

-   Wenn das gewünschte Datum im Bereich vom 01.01.1930 bis zum 31.12.2029 liegt, geben Sie das Jahr zweistellig ein. Andernfalls geben Sie das Jahr vierstellig ein.  

Sie können auch ein Datum als Wochentag gefolgt von einer Wochennummer eingeben. Oder Sie können ein Jahr eingeben. Beispielsweise bedeutet Mo25 oder mo25 Montag in der 25. Woche  

Anstatt ein bestimmtes Datum direkt einzugeben, können Sie auch einen dieser Codes verwenden.  

|Code|Ergebnis|  
|--------------|----------------|  
|h|Gibt das heutige Datum (das Systemdatum des Computers) an.|  
|p|Gibt eine Buchhaltungsperiode an, wobei p die erste Buchhaltungsperiode bezeichnet, p2 die zweite Buchhaltungsperiode angibt usw. |
|a|Gibt das Arbeitsdatum an, das in der Anwendung eingerichtet wird. Um das Arbeitsdatum zu ändern, siehe [Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md). Die Verwendung des Arbeitsdatums ist hilfreich, wenn eine Vielzahl von Transaktionen zu einem Datum ausgeführt werden müssen, das vom Systemdatum abweicht.|
|a|Gibt an, dass das Datum nach a ein Abschlussdatum ist, beispielsweise A31.12.01.|  

## <a name="entering-times"></a>Eingeben von Uhrzeiten

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

## <a name="entering-datetimes"></a>Eingeben von Datums-/Uhrzeitangaben

Beim Eingeben einer Datums-/Uhrzeitangabe muss zwischen dem Datum und der Zeiteingabe ein Leerzeichen eingefügt werden.  

In der folgenden Tabelle finden Sie eine Übersicht über die Möglichkeiten zum Eingeben von Datums-/Uhrzeitangaben sowie die Interpretation der jeweiligen Angabe.  

|Eingabe|Interpretation|  
|---------------|------------------------|  
|`131202` 132455|13.12.2002 13:24:55|  
|1-12-02 10|01.12.2002 10:00:00|  
|1.12.02 5|01.12.2002 05:00:00|  
|1.12.02|01.12.2002 00:00:00|  
|11 12|11.aktueller Monat.aktuelles Jahr 12:00:00|  
|1112 12|11.12.aktuelles Jahr 12:00:00|  
|"h" für heute|heutiges Datum 00:00:00|  
|Z… Zeit|heutiges Datum aktuelle Zeit|  
|h 10:30|heutiges Datum 10:30:00|  
|h 3:3:3|heutiges Datum 03:03:03|  
|"a" oder "Arbeitsdatum"|das Arbeitsdatum 00:00:00|  
|"mo" oder "Montag"|Montag der aktuellen Woche 00:00:00|  
|"di" oder "Dienstag"|Dienstag der aktuellen Woche 00:00:00|  
|"mi" oder "Mittwoch"|Mittwoch der aktuellen Woche 00:00:00|  
|"do" oder "Donnerstag"|Donnerstag der aktuellen Woche 00:00:00|  
|"fr" oder "Freitag"|Freitag der aktuellen Woche 00:00:00|  
|"s" oder "Sonnabend"|Samstag der aktuellen Woche 00:00:00|  
|"so" oder "Sonntag"|Sonntag der aktuellen Woche 00:00:00|  
|di 10:30|Dienstag der aktuellen Woche 10:30:00|  
|di 3:3:3|Dienstag der aktuellen Woche 03:03:03|  

## <a name="entering-duration"></a>Eingeben von Terminen

Zeiträume können als Zahl gefolgt von der entsprechenden Einheit eingegeben werden.  

Hier folgen einige Beispiele.  

|Termine|Maßeinheit**|  
|------------------|-------------------------|  
|2h|2 Stunden|  
|6 Std. 30 Min.|6 Stunden 30 Minuten|  
|6,5 Std.|6 Stunden 30 Minuten|  
|90 Min.|1 Stunde 30 Minuten|  
|2 T 6 Std. 30 Min.|2 Tage 6 Stunden 30 Minuten|  
|2 T 6 Std. 30 Min. 56 Sek. 600 Milisek.|2 Tage 6 Stunden 30 Minuten 56 SeDebitoren 600 MilliseDebitoren|  

 Sie haben auch die Möglichkeit, eine Zahl einzugeben, die dann automatisch in einen Zeitraum umgewandelt wird. Die eingegebene Zahl wird entsprechend der Standardeinheit konvertiert, die im Feld "Dauer" definiert ist.  

 Geben Sie zum Anzeigen der Einheit, die für ein Feld vom Typ „Dauer“ verwendet wird, eine Zahl ein. Am Ergebnis können Sie ablesen, in welche Einheit diese konvertiert wird.  

 Die Zahl 5 wird in 5 Std. konvertiert, wenn Stunden als Einheit angegeben wurden.  

## <a name="see-also"></a>Siehe auch  
 [Sortieren, Durchsuchen und Filtern von Listen](ui-enter-criteria-filters.md)  
 [Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
