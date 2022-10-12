---
title: Berichte ausführen und drucken
description: Erfahren Sie mehr zum Eingeben eines Berichts in eine Aufgabenwarteschlange und das Planen seiner Verarbeitung an einem bestimmten Datum und Uhrzeit.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report, print, schedule, save, Excel, PDF, Word, dataset
ms.search.form: ''
ms.date: 09/09/2022
ms.author: jswymer
ms.openlocfilehash: be4817ceac67674b82452b972c38dc316e274e8c
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607175"
---
# <a name="run-and-print-reports"></a>Berichte ausführen und drucken

Ein Bericht sammelt Informationen, die auf einer festgelegten Anzahl von Kriterien basieren. Er organisiert und präsentiert die Informationen in einem leicht zu lesenden Format, das Sie ausdrucken oder als Datei speichern können. Es gibt viele Berichte, auf die Sie im Zuge der Anwendung zugreifen können. Die Berichte enthalten normalerweise Informationen, die sich auf den Kontext der Seite beziehen, auf der Sie sich befinden. Beispielsweise der **Debitor** für die Seite Berichte Top 10 Debitoren, die Verkaufsstatistik und mehr.

> [!NOTE]
> Batch-Aufträge und XMLports tun mehr oder weniger dasselbe wie Berichte, werden aber eher für die Verarbeitung oder den Export von Daten verwendet. Die Stapelverarbeitung **Mahnungen erstellen** erstellt beispielsweise Mahnungsbelege zum Senden an Debitoren mit überfälligen Zahlungen. Dieser Artikel bezieht sich hauptsächlich auf "Berichte", aber die gleichen Informationen gelten für Stapelverarbeitungen und XMLports.

## <a name="get-started"></a>Erste Schritte

Sie können Berichte im Menü **Berichte** auf ausgewählten Seiten, Listen und Karten finden, oder Sie können die Suche verwenden ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?"), um Berichte nach Namen zu finden. verwenden, um Berichte nach Namen zu finden. Eine Übersicht über integrierte Berichte finden Sie in [!INCLUDE[prod_short](includes/prod_short.md)], sortiert nach Kategorien, siehe [Verfügbare Berichte in [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md).

Wenn Sie einen Bericht auswählen, wird in der Regel eine Seite&mdash;dargestellt, mit der Sie bestimmte Informationen definieren können,&mdash;die Sie im Bericht integrieren möchten. In den folgenden Abschnitten wird erläutert, wie Sie auf der Anforderungsseite einen Bericht erstellen, in der Vorschau anzeigen und drucken.

## <a name="using-default-valuesmdashpredefined-settings"></a><a name="SavedSettings"></a>Standardwerte verwenden&mdash;– vordefinierte Einstellungen

Die meisten Berichtsanforderungsseiten enthalten das Feld **Standardwerte verwenden von**. In diesem Feld können Sie vordefinierte Einstellungen für den Bericht auswählen, mit denen automatisch Optionen und Filter festgelegt werden. Wählen Sie einen Posten aus der Dropdownliste aus, und die Optionen und Filter auf der Berichtanforderungsseite ändern sich entsprechend.

Der Posten mit der Bezeichnung **Zuletzt verwendete Optionen und Filter** ist immer verfügbar. Dieser Posten legt fest, dass der Bericht die Optionen und Filter verwendet, die verwendet wurden, als Sie das letzte Mal den Bericht ausgeführt hatten.

Das Feld **Standardwerte verwenden von** bietet eine schnelle und zuverlässige Möglichkeit, konsistent Berichte zu generieren, die die richtigen Daten enthalten. Nachdem Sie einen Posten ausgewählt haben, können Sie alle Optionen und Filter ändern, bevor Sie den Bericht in der Vorschau anzeigen oder drucken. Die Änderungen, die Sie vornehmen, werden nicht auf dem vordefinierten Einstellungseintrag gespeichert, den Sie ausgewählt haben, sondern auf dem Eintrag **Zuletzt verwendete Optionen und Filter**.

> [!NOTE]
> Die vordefinierten Einstellungen werden normalerweise von einem Administrator eingerichtet und verwaltet. Weitere Informationen finden Sie unter [Gespeicherte Einstellungen für Berichte und Stapelaufträge verwalten](reports-saving-reusing-settings.md).

## <a name="specifying-the-data-to-include-in-a-report"></a>Angeben der Daten, die in Berichten integriert werden sollen

Verwenden Sie die Felder unter **Optionen** und **Filter** zum Ändern oder Einschränken der Informationen, die Sie im Bericht haben möchten. Sie können Filter in einem Bericht ungefähr so fest wie Filter in Listen festlegen. Erfahren Sie mehr im Abschnitt [Filtern](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> Das Inforegister **Filter** auf der Berichtanforderungsseite stellt eine generische Filterungsfunktion für Berichte bereit. Diese Filter sind optional.
>
> Manche Berichte ignorieren solche Filter, was bedeutet, dass, egal welcher Filter im Inforegister **filter** festgelegt ist, das Ergebnis des Berichts gleich ist. Es ist nicht möglich, eine Übersicht zu bieten, welche Felder in welchen Berichten ignoriert werden, daher müssen Sie mit den Filtern experimentieren, wenn Sie sie verwenden.
>
> **Beispiel**: Wenn Sie die Stapelverarbeitung **Mahnungen erstellen** verwenden, wird ein Filter für das Feld **Debitorenposten** aus **Letzte registrierte Mahnstufe** ignoriert, da Filter für diese Stapelverarbeitung fest sind.

## <a name="previewing-a-report"></a>Einen Bericht anzeigen

In der Vorschau eines Berichts können Sie sehen, wie der Bericht aussehen wird, bevor Sie ihn drucken. Die Vorschau basiert nicht auf dem Drucker, der im Feld **Drucker** auf der Anforderungsseite ausgewählt wurde. Das wird vom Browser gesteuert. Nach der Vorschau können Sie zur Anforderungsseite zurückkehren und bei Bedarf Änderungen an Optionen und Filtern vornehmen.

Die Vorschauoptionen auf der Seite **Berichtsanforderung** hängen vom Bericht ab. Bei einigen Berichten können Sie also **Vorschau** wählen, während für andere die Option **Vorschau & schließen** lautet. Beide Optionen öffnen eine Vorschau des Berichts. Der Unterschied ist, das **Vorschau** die Anforderungsseite geöffnet lässt, sodass Sie dorthin zurückkehren können, um Änderungen vornehmen, sie erneut in der Vorschau anzuzeigen oder zu drucken. Im Gegensatz dazu wird mit **Vorschau und Schließen** die Anforderungsseite geschlossen, sodass Sie den Bericht erneut öffnen müssen, um Änderungen vorzunehmen oder zu drucken.

> [!NOTE]
> Wenn Sie Business Central 2020 Veröffentlichungszyklus 1 oder früher verwenden, gibt es nur die Option **Vorschau**, die die Anforderungsseite in der Vorschau schließt, wie für **Vorschau und Schließen** oben beschrieben.

### <a name="work-with-the-preview"></a>Mit der Vorschau arbeiten

Verwenden Sie in der Vorschau die Menüleiste in der Berichtsvorschau, um:

- Navigieren durch Seiten
- Ein- und Ausblenden
- An die Seite anpassen
- Text auswählen

    Sie können Text aus einem Bericht kopieren und diesen dann woanders einfügen, z. B. eine Seite in [!INCLUDE[prod_short](includes/prod_short.md)] oder Microsoft Word. Mit der linken Maustaste halten Sie z. B. die Stelle gedrückt, an der Sie beginnen möchten. Dann bewegen Sie die Maus, um ein oder mehrere Wörter, Sätze oder Absätze auszuwählen. Drücken Sie die rechte Maustaste und wählen Sie **Kopieren** aus. Nun können Sie dann den ausgewählten Text kopieren.
- Beleg verschieben

    Sie können den sichtbaren Bereich des Berichts in beliebiger Richtung verschieben, daher können Sie weitere Bereiche oder den Bericht anzeigen. Das Schwenken ist hilfreich, wenn Sie die Ansicht vergrößert haben, um Details zu sehen. Mithilfe der Maus beispielsweise drücken und halten Sie die linke Maustaste an einem beliebigen Ort in der Berichtsvorschau und bewegen Sie dann Ihre Maus, um einen Abschnitt des Berichts auszuwählen.

- Download in eine PDF-Datei auf Ihrem Computer oder Netzwerk.
- Drucken

## <a name="saving-a-report-to-a-file"></a>Speichern eines Berichts in einer Datei

Sie können einen Bericht in ein PDF-Dokument, Microsoft Word-Dokument, Microsoft Excel-Arbeitsmappe, oder ein XML-Dokument speichern, indem Sie **Senden an** auswählen, und anschließend Ihre Auswahl treffen. Eine Datei wird auf Ihr Gerät heruntergeladen.

Wenn Ihre Organisation OneDrive für Systemfeatures konfiguriert hat, werden Excel-Arbeitsmappen und Word-Dokumente nicht heruntergeladen, sondern in Ihrem Browser mit Excel oder Word für das Web geöffnet.

> [!TIP]
> Die **Microsoft Excel-Dokument (nur Daten)**- und **XML-Dokument**-Optionen dienen hauptsächlich fortgeschrittenen Zwecken. Normalerweise verwenden Sie diese Optionen für eine detaillierte Datenanalyse. Weitere Informationen finden Sie unter [Analysieren von Berichtsdaten mit Excel und XML](report-analyze-excel.md).
>
> Sie können auch **Microsoft Excel-Dokument (nur Daten)** verwenden, um neue Excel-Layouts für einen bestimmten Bericht erstellen. Weitere Informationen finden Sie unter [Arbeiten mit Excel-Layouts](ui-excel-report-layouts.md).  

## <a name="scheduling-a-report-to-run-later-or-periodically"></a><a name="ScheduleReport"></a> Planen der späteren oder regelmäßigen Ausführung eines Berichts

Sie können einen einzelnen oder Serienbericht planen, sodass er an einem bestimmten Datum und zu einer festgelegten Uhrzeit ausgeführt wird. Geplante Berichte werden in der Projektwarteschlange eingegeben und zu der geplanten Zeit verarbeitet, wie vergleichbare andere Aufträge auch. Sie wählen die **Zeitplan** Option, nachdem Sie **Senden an** gewählt haben und geben Sie dann Informationen wie den Drucker sowie Uhrzeit und Datum ein. Der Bericht wird der Aufgabenwarteschlange hinzugefügt und zum angegebenen Zeitpunkt ausgeführt. Wenn der Bericht verarbeitet ist, wird das Element aus der Aufgabenwarteschlange entfernt. Weitere Informationen finden Sie unter [Aufgabenwarteschlangen zum Planen von Aufgaben verwenden](admin-job-queues-schedule-tasks.md).  

Wenn Sie die Ausführung eines Berichts planen, können Sie festlegen, dass er beispielsweise jeden Donnerstag ausgeführt werden muss, indem Sie das Feld **Datumsformel für nächste Ausführung** auf *D4* festlegen. Weitere Informationen finden Sie unter [Verwenden von Datumsformeln](ui-enter-date-ranges.md#use-date-formulas).  

Sie können wählen, ob Sie den Bericht in einer Datei (wie Excel, Word oder PDF) speichern, ausdrucken oder nur den Bericht generieren wollen. Wenn Sie wählen, den Bericht in eine Datei zu speichern, wird der verarbeitete Bericht an die Seite **Berichts-Eingang** an Ihr Rollencenter gesendet, wo Sie ihn anzeigen können. Erfahren Sie mehr unter [Berichte mit dem Berichtseingang teilen und exportieren](ui-work-report-inbox.md)

### <a name="manage-scheduled-recurring-reports"></a>Verwalten Sie geplante wiederkehrende Berichte

Geplante Berichte werden durch Batch-Jobs generiert, die auf der Seite **Einträge in der Auftragswarteschlange** verwaltet werden. Sie können den Status und andere Informationen für jeden Bericht auf der Seite anzeigen, den Berichts-Batch-Job anhalten/fortsetzen und den Bericht bei Bedarf generieren.

Auf der Seite **Einträge in der Auftragswarteschlange** können Sie auch einige Berichtsparameter ändern, z. B. Ausgabedateityp, Wiederholung, Ausführungsdatum sowie Start- und Endzeit. Vor dem Bearbeiten eines vorhandenen geplanten Berichts ist es jedoch erforderlich, die Berichtsauftragswarteschlange anzuhalten:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 1.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Auftragswarteschlangenposten** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Projektwarteschlangeneinträge** den gewünschten Bericht aus.
3. Wählen Sie die **Auf „Abwarten“ setzen**-Aktion aus.
4. Öffnen und bearbeiten Sie den geplanten Bericht, indem Sie seinen Status auswählen (*Abwarten*).

Wiederholen Sie nach dem Bearbeiten der Berichtsoptionen die ersten beiden Schritte und wählen Sie dann **Status auf 'Bereit' festlegen**, um die Generierung des Berichts fortzusetzen.

Erfahren Sie mehr über die Verwaltung von Auftragswarteschlangen unter [Verwenden Sie Auftragswarteschlangen, um Aufgaben zu planen](admin-job-queues-schedule-tasks.md).  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Berichte drucken

Um den Bericht zu drucken, wählen Sie **Drucken** auf der Berichtsanforderungsseite oder in der Menüleiste der Seite **Vorschau** aus.

Wenn ein Bericht ein Excel-Layout verwendet, wird das Feld **Drucker**, die Schalftläche **Drucken** oder die Schalfläche **Vorschau** nicht angezeigt. Stattdessen gibt es eine **Herunterladen**-Option. Wählen Sie zum Drucken **Herunterladen** aus, öffnen Sie dann die heruntergeladene Datei in Excel und drucken Sie sie von dort aus.

### <a name="printer"></a><a name="Printer"></a>Drucker

Das Feld **Drucker** auf der Anforderungsseite zeigt den Name des Druckers an, zu dem der Bericht gesendet wird. Um einen Drucker zu wechseln, wählen Sie einfach den Drucker aus der Liste aus.

> [!NOTE]
> Die Option **(Vom Browser gehandhabt)** zeigt an, dass es für den Bericht keinen vorgesehenen Drucker gibt. In diesem Fall handhabt der Browser den Ausdruck und zeigt die Standarddruckschritte an, in denen Sie einen lokalen Drucker auswählen können, der mit Ihrem Gerät verbunden ist. Die Option **(Vom Browser gehandhabt)** ist nicht verfügbar in der mobilen App von [!INCLUDE[prod_short](includes/prod_short.md)] oder der App für Microsoft Teams.

> [!TIP]
> Der Drucker, der standardmäßig für Sie ausgewählt wurde, ist auf der Seite **Druckerauswahl** eingerichtet. Erfahren Sie mehr über das Ändern des Standarddruckers im Abschnitt [Standarddrucker einrichten](ui-specify-printer-selection-reports.md#default).

### <a name="printing-reports-in-thai"></a>Drucken von Berichten in Thailändisch

Speziell für die thailändische Version von [!INCLUDE[prod_short](includes/prod_short.md)] kann die Schaltfläche **Drucken** keine Berichte korrekt drucken, weil der Dienst, der die druckbare PDF-Datei generiert, eingeschränkt ist. Stattdessen können Sie den Bericht in Word öffnen und den Bericht als druckbare PDF-Dateien speichern.  

Oder Sie können Ihren Administrator bitten, ein Word-Berichtslayout für Ihre am häufigsten verwendeten Berichte zu erstellen. Weitere Informationen finden Sie unter [Berichte- und Dokumentenlayouts verwalten](ui-manage-report-layouts.md).  

## <a name="switching-the-report-layout"></a>Wechseln des Berichtslayouts

Ein Berichtslayout steuert, was in einem Bericht angezeigt wird, wie er angeordnet wird und wie er formatiert ist. Es gibt einige Möglichkeiten das Layout zu ändern:

- Wenn Sie die Ausführung eines Berichts einrichten, sehen Sie das aktuelle Layout im Feld **Berichtslayout** auf der Anforderungsseite. Um vorübergehend ein anderes Layout zu verwenden, wählen Sie das Feld **Berichslayout** und wählen Sie dann ein Layout aus einer Liste der verfügbaren Layouts für diesen Bericht aus.
- Um das von einem Bericht verwendete Standardlayout zu ändern, gehen Sie entweder zu **Berichtslayouts** oder **Auswahl des Berichtslayouts**.

Weitere Informationen finden Sie unter [Die von einem Bericht verwendeten Layouts festlegen](ui-set-report-layout.md). Wenn Sie Ihr eigenes Berichtslayout anpassen möchten, gehen Sie zu [Erste Schritte bei der Erstellung von Layouts](ui-get-started-layouts.md).

## <a name="advanced-options"></a>Erweiterte Optionen

Die Felder unter dem Inforegister **Erweitert** legen Einschränkungen für den generierten Bericht fest, um Druckerressourcen zu steuern. Normalerweise müssen Sie diese Einstellungen nicht ändern, es sei denn, Sie haben einen umfangreichen Bericht. Wenn ein Bericht diese Einschränkungen überschreitet, wenn Sie versuchen, eine Vorschau anzuzeigen oder zu drucken, wird eine Meldung angezeigt, die Sie darüber informiert, welche Einschränkung überschritten wurde. Sie können die Einstellungen dann gemäß den Erfordernissen für Ihren Bericht ändern. Jedes Feld hat jedoch einen Maximalwert, den Sie beachten sollten:

|Feld|Maximalwert|
|-----|-------------|
|Maximale Rendering-Zeit|12:00:00|
|Maximale Zeilenanzahl|1000000|
|Maximale Beleganzahl|500|

> [!NOTE]
> Die Maximalwerte können sich für [!INCLUDE[prod_short](includes/prod_short.md)] lokal unterscheiden, und ein Administrator kann sie ändern. Weitere Informationen finden Sie unter [Konfigurieren von Business Central Server – Berichte](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Reports). Für eine Übersicht über Berichtseinschränkungen [!INCLUDE[prod_short](includes/prod_short.md)] online sehen Sie [Einschränkungen im Betrieb](/dynamics365/business-central/dev-itpro/administration/operational-limits-online).

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/paths/setup-reporting-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch

[Verfügbare Berichte in [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md)  
[Berichte in der täglichen Arbeit verwenden](reports-use-reports.md)  
[Übersicht über Business Intelligence und Reporting](reports-bi-reporting.md)  
[Drucker einrichten](ui-specify-printer-selection-reports.md)  
[Führen Sie Stapeljobs und XMLports aus](ui-how-run-batch-jobs.md)  
[Mit Datumsangaben und Uhrzeiten in Kalendern arbeiten](ui-enter-date-ranges.md)  
[Verwaltung von Berichts- und Dokumentlayouts](ui-manage-report-layouts.md)  
[Financial Business Intelligence](bi.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
