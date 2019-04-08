---
title: Sie können einen Bericht planen, sodass er an einem bestimmten Datum und zu einer festgelegten Uhrzeit ausgeführt wird | Microsoft Docs
description: Erfahren Sie mehr zum Eingeben eines Berichts in eine Aufgabenwarteschlange und das Planen der Verarbeitung an einem bestimmten Datum und Uhrzeit.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 10/01/2018
ms.author: jswymer
ms.openlocfilehash: 98d51b10d3ca415a463b58405cb3c4f2449b75ad
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "852424"
---
# <a name="working-with-reports-and-batch-jobs"></a>Arbeiten mit Berichten und Stapelverarbeitungen
Ein Bericht stellt Informationen auf Basis eines bestimmten Satz an Kriterien zusammen und unterteilt die Informationen in ein einfach zu lesendes, druckbares Format. Es gibt viele Berichte, auf die Sie im Zuge der Anwendung zugreifen können. Die Berichte stellen in der Regel Informationen proportional zu dem Kontext der Seite bereit, auf der Sie sich befinden. Beispielsweise der **Debitor** für die Seite Berichte Top 10 Debitoren und die Verkaufsstatistik und mehr.

Stapelverarbeitungen machen mehr oder weniger das gleiche wie Berichte, aber mit dem Ziel der Durchführung eines Vorgangs. Die Stapelverarbeitung **Mahnungen erstellen** erstellt beispielsweise Mahnungsbelege für Debitoren mit überfälligen Zahlungen.  

> [!NOTE]
> Dieses Thema bezieht sich hauptsächlich auf "Bericht", aber die gleichen Informationen gelten für Stapelverarbeitungen.

Auf der Registerkarte **Berichte** finden Sie Berichte über ausgewählte Seiten, oder Sie können die Suche ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "„Wie möchten Sie weiter verfahren“") verwenden, um Berichte nach Name zu suchen.


## <a name="specifying-the-data-to-include-in-the-report"></a>Angeben der Daten, die im Bericht integriert werden sollen
Wenn Sie einen Bericht öffnen, wird in der Regel eine Seite dargestellt, mit der Sie bestimmte Informationen definieren können, die Sie im Bericht integrieren möchten. Diese Seite ist die Berichtanfordearungsseite. Beispielsweise können mit der Seite Bericht anfordern einen Bericht für einen bestimmten Debitor oder eine bestimmte Gültigkeit erstellen oder die Anordnung der Informationen im Bericht sortieren. Hier ist ein Beispiel einer Berichtsanforderungsseite:

![Berichtsoptionen](media/report_options.png "Berichtsoptionen")

> [!Caution]
> Der Abschnitt **Ergebnisse anzeigen** auf der Anforderungsseite stellt eine generische Filterungsfunktion für Berichte bereit. Diese Filter sind optional.<br /><br /> Manche Berichte ignorieren solche Filter, was bedeutet, dass, egal welcher Filter im Abschnitt **Ergebnisse anzeigen** festgelegt ist, das Ergebnis des Berichts gleich ist. Es ist nicht möglich, eine Übersicht zu bieten, welche Felder in welchen Berichten ignoriert werden, daher müssen Sie mit den Filtern experimentieren, wenn Sie sie verwenden.<br /><br />
**Beispiel**: Wenn Sie die Stapelverarbeitung **Mahnungen erstellen** verwenden, wird ein Filter für das Feld **Debitorenposten** aus **Letzte registrierte Mahnstufe** ignoriert, da Filter für diese Stapelverarbeitung fest sind.

### <a name="SavedSettings"></a>Gespeicherte Einstellungen nutzen
Bei gewissen Berichten, abhängig davon, wie sie eingerichtet sind, umfasst die Berichtsseite möglicherweise einen Bereich **Gespeicherte Einstellungen**, der ein oder mehrere Posten im Kästchen **Standardwert nutzen** enthält. Die Posten in diesem Feld wird *gespeicherte Einstellungen* genannt. Eine gespeicherte Einstellung ist im Allgemeinen eine vordefinierte Gruppe von Optionen und Filter, die Sie z. B. für Berichte anwenden können, bevor Sie den Bericht auf eine Datei in der Vorschau sehen oder buchen. Der gespeicherte Einstellungseintrag mit der Bezeichnung **Zuletzt verwendete Optionen und Filter** ist immer verfügbar. Dieser Posten setzt den Bericht mit den Optionen und Filtern, die Sie beim letzten Mal verwendet haben, als Sie den Bericht betrachteten.

Die Verwendung von gespeicherten Einstellungen ist eine schnelle und zuverlässige Art, Berichte zu erstellen, die die richtigen Daten enthalten. Nachdem Sie das Feld **Verwendungsstandardwert nutzen ab** für eine gespeicherte Einstellung definiert haben, können Sie eine Optionen und die Filter ändern, bevor Sie die Berichtvorschau anzeigen oder speichern. Änderungen, die Sie machen, werden nicht in den gespeicherten Einstellungsposten gespeichert, die Sie auswählten, sie sind jedoch unter **Zuletzt verwendete Optionen und Filter** gespeichert.

>[!NOTE]
>Als Administrator können Sie die gespeicherten Einstellungen für Berichte für alle Benutzer erstellen und verwalten. Weitere Informationen finden Sie unter [Verwaltung von gespeicherten Einstellungen in Berichten](reports-saving-reusing-settings.md).

### <a name="setting-options-and-filters"></a>Optionen und Filter einstellen
Wenn Sie die Daten weiter einschränken oder festlegen möchten, die in einem Bericht enthalten sind, können Sie Zusatzfunktionen und Filter festlegen.

Filter ermöglichen Ihnen, Datenanzeigen basierend auf bestimmten Kriterien anzuzeigen. Filter werden durch die Einheit, der sie angehören, wie in der Abbildung **Debitor** oben gruppiert. Sie definieren einen Filter, indem Sie das Kästchen **Wo** in das Feld setzen, das Sie filtern möchten, und dann die Kriterien im Feld **ist:** hinzufügen. Zum Beispiel in der Abbildung oben,gibt es einen individuellen Filter, der Berichte für den Debitor erstellt, deren **Nr.** gleich **01121212** ist.

Sie können weitere Filter hinzufügen, indem Sie die Felder **Hinzufügen** festlegen. Wenn Sie mehr als einen Filter haben, werden nur Ergebnisse, die die Kriterien für alle Filter erfüllen, im Bericht berücksichtigt werden.

Abhängig davon, in welchem Feld Sie filtern, können Sie die gewünschten Filterkriterien festlegen, um nach einer exakten Sprachgruppe, einer teilweisen Übereinstimmung, einem Datenbereich und mehr suchen. Informationen zur Einrichtung von Filtern finden Sie unter:
-   [Filterung](ui-enter-criteria-filters.md#FilterCriteria)
-   [Arbeiten mit Datumsangaben und Uhrzeiten in Kalendern](ui-enter-date-ranges.md)

## <a name="previewing-a-report"></a>Einen Bericht anzeigen
Wählen Sie **Vorschau**, um den Bericht im Internetbrowser anzuzeigen. Anzeigen auf einem Bereich des Berichts, um ihn auf der Menüleiste anzuzeigen.  

![Berichtsvorschausymbolleiste](media/report_viewer.png "Berichtsvorschausymbolleiste")

Verwenden der Menüleiste:

-   Navigieren durch Seiten
-   Ein- und Ausblenden
-   An die Seite anpassen
-   Text auswählen

    Sie können Text aus einem Bericht kopieren und diesen dann woanders einfügen, z. B. eine Seite in [!INCLUDE[d365fin](includes/d365fin_md.md)] oder Microsoft Word.  Mithilfe einer Maus beispielsweise drücken und halten Sie, wo Sie beginnen möchten, und fahren dann mit der Maus, um einen oder mehrere Begriffe, Sätze oder Absätze auszuwählen. Sie können die rechte Maustaste drücken dann **Kopieren** auswählen. Sie können dann den ausgewählten Text kopieren.
-   Beleg verschieben

    Sie können den sichtbaren Bereich des Berichts in beliebiger Richtung verschieben, daher können Sie weitere Bereiche oder den Bericht anzeigen. Dies ist hilfreich, wenn Sie gezoomt haben, um Details anzuzeigen.  Mithilfe der Maus beispielsweise drücken und halten Sie die Maustaste an einem beliebigen Ort in der Berichtsvorschau und bewegen Sie dann Ihre Maus.

-   Download in eine PDF-Datei auf Ihrem Computer oder Netzwerk.
-   Drucken


## <a name="saving-a-report"></a>Speichern des Berichts
Sie können einen Bericht in ein PDF-Dokument, Microsoft Word-Dokument oder Microsoft Excel-Dokument speichern, indem Sie **Senden an** auswählen, und anschließend Ihre Auswahl treffen.

## <a name="ScheduleReport"></a> Planen der Ausführung eines Berichts
Sie können einen Bericht planen, sodass er an einem bestimmten Datum und zu einer festgelegten Uhrzeit ausgeführt wird. Geplante Berichte werden in der Projektwarteschlange eingegeben und zu der geplanten Zeit verarbeitet, wie vergleichbare andere Aufträge auch. Sie können auswählen, ob Sie den verarbeiteten Bericht speichern möchten, beispielsweise als Excel-, Word- oder PDF-Datei, ihn auf einem ausgewählten Drucker auszugeben, oder ihn nur zu verarbeiten. Wenn Sie wählen, den Bericht in eine Datei zu speichern, wird der verarbeitete Bericht an den **Berichts-Eingang** an Ihr Rollencenter gesendet, wo Sie ihn anzeigen können.

Sie können einen Bericht planen, wenn Sie einen Bericht öffnen. Sie wählen **Plan** aus und Sie geben die Informationen wie Drucker und Zeit und Datum ein. Der Bericht wird der Aufgabenwarteschlange hinzugefügt und zum angegebenen Zeitpunkt ausgeführt. Wenn der Bericht verarbeitet ist, wird das Element aus der Aufgabenwarteschlange entfernt. Wenn Sie den verarbeiteten Bericht in einer Datei gespeichert haben, ist er im **Berichts-Eingang** verfügbar.

## <a name="PrintReport"></a>Berichte drucken
Sie können einen Bericht über die Schaltfläche **Drucken** auf der Optionsseite ausdrucken, die erscheint, wenn Sie den Bericht öffnen, oder von der Menüleiste unter "Vorschau".

## <a name="changing-the-layout-and-look-of-a-report"></a>Ändern des Layouts und des Layouts eines Berichts
Ein Berichtslayout steuert, was in einem Bericht angezeigt wird, wie er angeordnet wird und wie er formatiert ist. Wenn Sie zu einem anderen Layout wechseln möchten, finden Sie Informationen unter [Ändern Sie, das Layout derzeit auf einem Bericht verwendet wird](ui-how-change-layout-currently-used-report.md). Oder, wenn Sie Ihr eigenes Berichtslayout anpassen möchten gehen Sie zu [Erstellen und bearbeiten von benutzerdefinierten Berichtslayouts](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Siehe auch
[Angeben der Druckerauswahl für Berichte](ui-specify-printer-selection-reports.md)  
[Verwaltung von Berichts- und Beleg-Layouts](ui-manage-report-layouts.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
