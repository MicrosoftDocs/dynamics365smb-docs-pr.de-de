---
title: Sie können einen Bericht planen, sodass er an einem bestimmten Datum und zu einer festgelegten Uhrzeit ausgeführt wird | Microsoft Docs
description: Erfahren Sie mehr zum Eingeben eines Berichts in eine Aufgabenwarteschlange und das Planen der Verarbeitung an einem bestimmten Datum und Uhrzeit.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 06/10/2020
ms.author: sgroespe
ms.openlocfilehash: 19811dadb284ee9e629c9dc518df5cb989175fdb
ms.sourcegitcommit: 0b5f8f68b1c9526288bfcce1a3bdc988d2910040
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2020
ms.locfileid: "3454329"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Arbeiten mit Berichten, Stapelverarbeitungen und XMLports

Ein Bericht stellt Informationen auf Basis eines bestimmten Satz an Kriterien zusammen und unterteilt die Informationen in ein einfach zu lesendes, druckbares Format oder speichert es als Dateil Es gibt viele Berichte, auf die Sie im Zuge der Anwendung zugreifen können. Die Berichte stellen in der Regel Informationen proportional zu dem Kontext der Seite bereit, auf der Sie sich befinden. Beispielsweise der **Debitor** für die Seite Berichte Top 10 Debitoren, die Verkaufsstatistik und mehr.

Stapelverarbeitungen und XMLports machen mehr oder weniger das gleiche wie Berichte, aber mit dem Ziel der Durchführung eines Vorgangs. Die Stapelverarbeitung **Mahnungen erstellen** erstellt beispielsweise Mahnungsbelege für Debitoren mit überfälligen Zahlungen.  

> [!NOTE]
> Dieses Thema bezieht sich hauptsächlich auf "Bericht", aber die gleichen Informationen gelten für Stapelverarbeitungen und XMLports.

Sie können Berichte im Register **Berichte** auf ausgewählten Seiten finden, oder Sie können die Suche ![Glühbirne verwenden, die die Funktion „Tell Me“](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") öffnet, um Berichte nach Namen zu finden.

## <a name="specifying-the-data-to-include-in-reports"></a>Angeben der Daten, die in Berichten integriert werden sollen
Wenn Sie einen Bericht, einen Stapelverarbeitungsauftrag oder XMLport öffnen, wird in der Regel eine Seite dargestellt, mit der Sie bestimmte Informationen definieren können, die Sie im Bericht integrieren möchten.

Sie legen Filter in einem Bericht ungefähr so fest wie Filter in Listen. Weitere Informationen finden Sie unter [Filterung](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> Der Abschnitt **Filterlisten nach** auf der Anforderungsseite stellt eine generische Filterungsfunktion für Berichte bereit. Diese Filter sind optional.
>
> Manche Berichte ignorieren solche Filter, was bedeutet, dass, egal welcher Filter im Abschnitt **Filterliste nach** festgelegt ist, das Ergebnis des Berichts gleich ist. Es ist nicht möglich, eine Übersicht zu bieten, welche Felder in welchen Berichten ignoriert werden, daher müssen Sie mit den Filtern experimentieren, wenn Sie sie verwenden.
>
> **Beispiel**: Wenn Sie die Stapelverarbeitung **Mahnungen erstellen** verwenden, wird ein Filter für das Feld **Debitorenposten** aus **Letzte registrierte Mahnstufe** ignoriert, da Filter für diese Stapelverarbeitung fest sind.

## <a name="using-saved-settings"></a><a name="SavedSettings"></a>Gespeicherte Einstellungen nutzen
Die Anforderungsseite kann den Abschnitt **Gespeicherte Einstellungen**, der einen oder mehrere Einträge Kästchen **Standardwert von verwenden** enthält, einschließen. Eine gespeicherte Einstellung ist im Allgemeinen eine vordefinierte Gruppe von Optionen und Filter, die Sie z. B. für Berichte anwenden können, bevor Sie den Bericht auf eine Datei in der Vorschau sehen oder buchen. Der gespeicherte Einstellungseintrag mit der Bezeichnung **Zuletzt verwendete Optionen und Filter** ist immer verfügbar. Dieser Posten setzt den Bericht mit den Optionen und Filtern, die Sie beim letzten Mal verwendet haben, als Sie den Bericht betrachtet haben.

Die Verwendung von gespeicherten Einstellungen ist eine schnelle und zuverlässige Art, Berichte zu erstellen, die die richtigen Daten enthalten. Nachdem Sie das Feld **Verwendungsstandardwert nutzen ab** für eine gespeicherte Einstellung definiert haben, können Sie eine Optionen und die Filter ändern, bevor Sie die Berichtvorschau anzeigen oder speichern. Änderungen, die Sie machen, werden nicht in den gespeicherten Einstellungsposten gespeichert, die Sie auswählten, sie sind jedoch unter **Zuletzt verwendete Optionen und Filtereinträge** gespeichert.

>[!NOTE]
>Als Administrator können Sie die gespeicherten Einstellungen für Berichte für alle Benutzer erstellen und verwalten. Weitere Informationen finden Sie unter [Verwaltung von gespeicherten Einstellungen in Berichten und Stapelverarbeitungen](reports-saving-reusing-settings.md).

## <a name="previewing-a-report"></a>Einen Bericht anzeigen

Wählen Sie die Schaltfläche **Vorschau**, um den Bericht anzuzeigen. Verwenden Sie die Menüleiste in der Berichtsvorschau, um:

- Navigieren durch Seiten
- Ein- und Ausblenden
- An die Seite anpassen
- Text auswählen

    Sie können Text aus einem Bericht kopieren und diesen dann woanders einfügen, z. B. eine Seite in [!INCLUDE[d365fin](includes/d365fin_md.md)] oder Microsoft Word.  Mithilfe einer Maus beispielsweise drücken und halten Sie, wo Sie beginnen möchten, und fahren dann mit der Maus, um einen oder mehrere Begriffe, Sätze oder Absätze auszuwählen. Sie können die rechte Maustaste drücken dann **Kopieren** auswählen. Sie können dann den ausgewählten Text kopieren.
- Beleg verschieben

    Sie können den sichtbaren Bereich des Berichts in beliebiger Richtung verschieben, daher können Sie weitere Bereiche oder den Bericht anzeigen. Dies ist hilfreich, wenn Sie gezoomt haben, um Details anzuzeigen.  Mithilfe der Maus beispielsweise drücken und halten Sie die Maustaste an einem beliebigen Ort in der Berichtsvorschau und bewegen Sie dann Ihre Maus.

- Download in eine PDF-Datei auf Ihrem Computer oder Netzwerk.
- Drucken

## <a name="saving-a-report"></a>Speichern des Berichts
Sie können einen Bericht in ein PDF-Dokument, Microsoft Word Dokument oder Microsoft Excel Dokument speichern, indem Sie die Schaltfläche **Senden an** auswählen, und anschließend Ihre Auswahl treffen.

## <a name="scheduling-a-report-to-run"></a><a name="ScheduleReport"></a> Planen der Ausführung eines Berichts

Sie können einen Bericht oder einen Stapelverarbeitungsauftrag planen, sodass er an einem bestimmten Datum und zu einer festgelegten Uhrzeit ausgeführt wird. Geplante Berichte und Stapelverarbeitungsaufträge werden in der Projektwarteschlange eingegeben und zu der geplanten Zeit verarbeitet, wie vergleichbare andere Aufträge auch. Sie wählen die **Zeitplan** Option, nachdem Sie die Schaltfläche **Senden an** gewählt haben und geben Sie dann Informationen wie den Drucker sowie Uhrzeit und Datum ein. Der Bericht wird der Aufgabenwarteschlange hinzugefügt und zum angegebenen Zeitpunkt ausgeführt. Wenn der Bericht verarbeitet ist, wird das Element aus der Aufgabenwarteschlange entfernt. Weitere Informationen finden Sie unter [Job-Warteschlangen zur Einplanung von Aufgaben verwenden](admin-job-queues-schedule-tasks.md).  

Wenn Sie die Ausführung eines Berichts planen, können Sie festlegen, dass er jeden Donnerstag ausgeführt werden muss, indem Sie beispielsweise das Feld **Datumsformel für nächste Ausführung** auf *D4* festlegen. Weitere Informationen zu finden Sie unter [Verwenden von Datumsformeln](ui-enter-date-ranges.md#using-date-formulas).  

Sie können auswählen, ob Sie den verarbeiteten Bericht speichern möchten, beispielsweise als Excel-, Word- oder PDF-Datei, ihn auf einem ausgewählten Drucker auszugeben, oder ihn nur zu verarbeiten. Wenn Sie wählen, den Bericht in eine Datei zu speichern, wird der verarbeitete Bericht an den **Berichts-Eingang** an Ihr Rollencenter gesendet, wo Sie ihn anzeigen können.  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Berichte drucken
Sie können einen Bericht drucken, indem Sie die Schaltfläche **Drucken** auf der Berichtsanforderungsseite oder in der Menüleiste auf der Seite **Vorschau** wählen.

Da [!INCLUDE[prodshort](includes/prodshort.md)] ein Cloud-Service ist, kann er keine lokalen Drucker erreichen, die mit den Rechnern der Benutzer verbunden sind. Sie kann jedoch mit Cloud-fähigen Druckern verbunden werden. In der generischen Version von [!INCLUDE[prodshort](includes/prodshort.md)] wird ein Cloud-Drucker namens **E-Mail-Drucker** als Erweiterung installiert und ist nach der Ersteinrichtung einsatzbereit.

Wenn ein Cloud-Drucker nicht installiert und eingerichtet ist oder wenn ein installierter Drucker ausfällt, werden beim Drucken standardmäßig die Druckoptionen des Browsers verwendet. Dies wird durch diesen Wert im Feld **Drucker** auf der Berichtsanforderungsseite angezeigt: *(keines, wird vom Browser behandelt)*.

Auf der Seite **Druckerverwaltung** sehen Sie die Drucker, die eingerichtet sind. Weitere Informationen finden Sie unter [Drucker einrichten](ui-specify-printer-selection-reports.md).

> [!NOTE]
> Sie können das Feld **Drucker** auf der Berichtsanforderungsseite nicht ändern. Um einen anderen Drucker zu verwenden, müssen Sie ihn auf der Seite **Druckerverwaltung** auswählen.

### <a name="printing-reports-in-thai"></a>Drucken von Berichten in Thailändisch
Speziell für die thailändische Version von [!INCLUDE[prodshort](includes/prodshort.md)], kann die **Drucken** Schaltfläche keine Berichte korrekt drucken, weil der Service, der die druckbare PDF-Datei generiert, limitiert ist. Stattdessen können Sie den Bericht in Word öffnen und den Bericht als druckbare PDF-Dateien speichern.  

Alternativ können Sie den Administrator bitten, ein Word-Berichtslayout für Ihre verwendete Berichte zu erstellen. Weitere Informationen finden Sie unter [Berichte- und Dokumentenlayouts verwalten](ui-manage-report-layouts.md).  

## <a name="changing-report-layouts"></a>Ändern von Berichtslayouts
Ein Berichtslayout steuert, was in einem Bericht angezeigt wird, wie er angeordnet wird und wie er formatiert ist. Wenn Sie zu einem anderen Layout wechseln möchten, finden Sie Informationen unter [Ändern des aktuellen Berichtlayout](ui-how-change-layout-currently-used-report.md). Oder, wenn Sie Ihr eigenes Berichtslayout anpassen möchten gehen Sie zu [Erstellen und bearbeiten von benutzerdefinierten Berichtslayouts](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Siehe auch

[Drucker einrichten](ui-specify-printer-selection-reports.md)  
[Arbeiten mit Datumsangaben und Uhrzeiten in Kalendern](ui-enter-date-ranges.md)  
[Verwalten von Berichts- und Beleglayouts](ui-manage-report-layouts.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
