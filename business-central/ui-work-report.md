---
title: Arbeiten mit Berichten, Stapelverarbeitungen und XMLports
description: Erfahren Sie mehr zum Eingeben eines Berichts in eine Aufgabenwarteschlange und das Planen der Verarbeitung an einem bestimmten Datum und Uhrzeit.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report, print, schedule, save, Excel, PDF, Word, dataset
ms.date: 02/09/2022
ms.author: jswymer
ms.openlocfilehash: 142a9f826e200f06172b741e72e54d49ff9caf47
ms.sourcegitcommit: 2c972dfc94d27245eaa99efcf638d030dedafb22
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2022
ms.locfileid: "8102603"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Arbeiten mit Berichten, Stapelverarbeitungen und XMLports

Ein Bericht sammelt Informationen, die auf einer festgelegten Anzahl von Kriterien basieren. Er organisiert und präsentiert die Informationen in einem leicht zu lesenden Format, das Sie ausdrucken oder als Datei speichern können. Es gibt viele Berichte, auf die Sie im Zuge der Anwendung zugreifen können. Die Berichte enthalten normalerweise Informationen, die sich auf den Kontext der Seite beziehen, auf der Sie sich befinden. Beispielsweise der **Debitor** für die Seite Berichte Top 10 Debitoren, die Verkaufsstatistik und mehr.

Batch-Aufträge und XMLports tun mehr oder weniger dasselbe wie Berichte, werden aber eher für die Verarbeitung oder den Export von Daten verwendet. Die Stapelverarbeitung **Mahnungen erstellen** erstellt beispielsweise Mahnungsbelege für Debitoren mit überfälligen Zahlungen.  

> [!NOTE]
> Dieses Thema bezieht sich hauptsächlich auf "Bericht", aber die gleichen Informationen gelten für Stapelverarbeitungen und XMLports.

## <a name="getting-started"></a>Erste Schritte

Sie finden Berichte in der Registerkarte **Berichte** auf ausgewählten Seiten, oder Sie können die Suche ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet“](media/ui-search/search_small.png "Was möchten Sie tun?") verwenden, um Berichte nach Namen zu finden.

Wenn Sie einen Bericht, einen Stapelverarbeitungsauftrag oder XMLport öffnen, wird in der Regel eine Seite dargestellt, mit der Sie bestimmte Informationen definieren können, die Sie im Bericht integrieren möchten. In den folgenden Abschnitten wird erläutert, wie Sie auf der Anforderungsseite einen Bericht erstellen, in der Vorschau anzeigen und drucken.

## <a name="using-default-values---predefined-settings"></a><a name="SavedSettings"></a>Standardwerte verwenden – vordefinierte Einstellungen

Die meisten Anforderungsseiten enthalten das Feld **Standardwerte verwenden von**. In diesem Feld können Sie vordefinierte Einstellungen für den Bericht auswählen, mit denen automatisch Optionen und Filter für den Bericht festgelegt werden. Wählen Sie einen Posten aus der Dropdownliste aus, und die Optionen und Filter auf der Anforderungsseite ändern sich entsprechend.

Der Posten mit der Bezeichnung **Zuletzt verwendete Optionen und Filter** ist immer verfügbar. Dieser Posten legt fest, dass der Bericht Optionen und Filter verwendet, die verwendet wurden, als Sie das letzte Mal den Bericht ausgeführt hatten.

Das Feld **Standardwerte verwenden von** bietet eine schnelle und zuverlässige Möglichkeit, konsistent Berichte zu generieren, die die richtigen Daten enthalten. Nachdem Sie einen Posten ausgewählt haben, können Sie alle Optionen und Filter ändern, bevor Sie den Bericht in der Vorschau anzeigen oder drucken. Die Änderungen, die Sie vornehmen, werden nicht auf dem vordefinierten Einstellungseintrag gespeichert, den Sie ausgewählt haben, sondern auf dem Eintrag **Zuletzt verwendete Optionen und Filter**.

>[!NOTE]
> Die vordefinierten Einstellungen werden normalerweise von einem Administrator eingerichtet und verwaltet. Wenn Sie weitere Informationen erhalten möchten, finden Sie diese unter [Gespeicherten Einstellungen für Berichte und Stapelverarbeitungsaufträge verwalten](reports-saving-reusing-settings.md).

## <a name="specifying-the-data-to-include-in-reports"></a>Angeben der Daten, die in Berichten integriert werden sollen

Verwenden Sie die Felder unter **Optionen** und **Filter** zum Ändern der Begrenzung der Informationen, die Sie im Bericht haben möchten. Sie legen Filter in einem Bericht ungefähr so fest wie Filter in Listen. Weitere Informationen finden Sie unter [Filterung](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> Der Abschnitt **Filterlisten nach** auf der Anforderungsseite stellt eine generische Filterungsfunktion für Berichte bereit. Diese Filter sind optional.
>
> Manche Berichte ignorieren solche Filter, was bedeutet, dass, egal welcher Filter im Abschnitt **Filterliste nach** festgelegt ist, das Ergebnis des Berichts gleich ist. Es ist nicht möglich, eine Übersicht zu bieten, welche Felder in welchen Berichten ignoriert werden, daher müssen Sie mit den Filtern experimentieren, wenn Sie sie verwenden.
>
> **Beispiel**: Wenn Sie die Stapelverarbeitung **Mahnungen erstellen** verwenden, wird ein Filter für das Feld **Debitorenposten** aus **Letzte registrierte Mahnstufe** ignoriert, da Filter für diese Stapelverarbeitung fest sind.

## <a name="previewing-a-report"></a>Einen Bericht anzeigen

In der Vorschau eines Berichts können Sie sehen, wie der Bericht aussehen wird, bevor Sie ihn drucken. Die Vorschau basiert nicht auf dem Drucker, der im Feld **Drucker** auf der Anforderungsseite ausgewählt wurde. Das wird vom Browser gesteuert. Nach der Vorschau können Sie zur Anforderungsseite zurückkehren und bei Bedarf Änderungen an Optionen und Filtern vornehmen.

Um eine Vorschau eines Berichts anzuzeigen, wählen Sie die Schaltfläche **Vorschau** oder **Vorschau und Schließen** auf der Berichtsanforderungsseite aus. Die angezeigte Schaltfläche hängt vom Bericht ab, daher haben einige Berichte die Schaltfläche **Vorschau**, während andere die Schaltfläche **Vorschau und Schließen** haben. Beide Schaltflächen öffnen eine Vorschau des Berichts. Der Unterschied ist, das **Vorschau** die Anforderungsseite geöffnet lässt, sodass Sie dorthin zurückkehren können, um Änderungen vornehmen, sie erneut in der Vorschau anzuzeigen oder zu drucken. Mit **Vorschau und Schließen** wird die Anforderungsseite geschlossen, sodass Sie den Bericht erneut öffnen müssen, um Änderungen vorzunehmen oder zu drucken.

> [!NOTE]
> Wenn Sie Business Central 2020 Veröffentlichungszyklus 1 oder früher verwenden, gibt es nur eine Schaltfläche **Vorschau**, die die Anforderungsseite in der Vorschau schließt, wie für **Vorschau und Schließen** beschrieben.

### <a name="working-with-the-preview"></a>Arbeiten mit der Vorschau

Verwenden Sie in der Vorschau die Menüleiste in der Berichtsvorschau, um:

- Navigieren durch Seiten
- Ein- und Ausblenden
- An die Seite anpassen
- Text auswählen

    Sie können Text aus einem Bericht kopieren und diesen dann woanders einfügen, z. B. eine Seite in [!INCLUDE[prod_short](includes/prod_short.md)] oder Microsoft Word.  Mit der Maus halten Sie z. B. die Stelle gedrückt, an der Sie beginnen möchten. Dann bewegen Sie die Maus, um ein oder mehrere Wörter, Sätze oder Absätze auszuwählen. Drücken Sie die rechte Maustaste und wählen Sie **Kopieren** aus. Fügen Sie dann den ausgewählten Text dort ein, wo Sie möchten.
- Beleg verschieben

    Sie können den sichtbaren Bereich des Berichts in beliebiger Richtung verschieben, daher können Sie weitere Bereiche oder den Bericht anzeigen. Das Schwenken ist hilfreich, wenn Sie die Ansicht vergrößert haben, um Details zu sehen.  Mithilfe der Maus beispielsweise drücken und halten Sie die Maustaste an einem beliebigen Ort in der Berichtsvorschau und bewegen Sie dann Ihre Maus.

- Download in eine PDF-Datei auf Ihrem Computer oder Netzwerk.
- Drucken

## <a name="saving-a-report-to-a-file"></a>Speichern eines Berichts in einer Datei

Sie können einen Bericht in einem PDF-Dokument, einem Beleg Microsoft Word oder einem Arbeitsblatt Microsoft Excel speichern, indem Sie die Schaltfläche **Senden an** wählen und dann Ihre Auswahl treffen.

### <a name="about-sending-to-excel"></a>Über das Senden an Excel

Sie können mit [!INCLUDE [prod_short](includes/prod_short.md)]-Daten in Excel arbeiten, um sie weiter zu analysieren. Weitere Informationen finden Sie unter [Analysieren von Berichtsdaten mit Excel](report-analyze-excel.md).  
<!--
### About sending to Word

Use the **Microsoft Word Document** option to generate a report as a Word document.  

> [!NOTE]
> You can specify the layout to use for each report on the **Report Selection** page in the **Selected Layout** field. The default setting for reports is **RDLC (built-in)**, which produces reports in the same, or similar, layout as the **Microsoft Word Document** layout. However, the key difference is whether you want to generate a single or multiple report documents. For single documents, you can use the RDLC (built-in) option. For multiple documents, set the **Microsoft Word Document** as the default layout for the report. For more information, see [Managing Report and Document Layouts](ui-manage-report-layouts.md).

-->

## <a name="scheduling-a-report-to-run"></a><a name="ScheduleReport"></a> Planen der Ausführung eines Berichts

Sie können einen Bericht oder einen Stapelverarbeitungsauftrag planen, sodass er an einem bestimmten Datum und zu einer festgelegten Uhrzeit ausgeführt wird. Geplante Berichte und Stapelverarbeitungsaufträge werden in der Projektwarteschlange eingegeben und zu der geplanten Zeit verarbeitet, wie vergleichbare andere Aufträge auch. Sie wählen die **Zeitplan** Option, nachdem Sie die Schaltfläche **Senden an** gewählt haben und geben Sie dann Informationen wie den Drucker sowie Uhrzeit und Datum ein. Der Bericht wird der Aufgabenwarteschlange hinzugefügt und zum angegebenen Zeitpunkt ausgeführt. Wenn der Bericht verarbeitet ist, wird das Element aus der Aufgabenwarteschlange entfernt. Weitere Informationen finden Sie unter [Job-Warteschlangen zur Einplanung von Aufgaben verwenden](admin-job-queues-schedule-tasks.md).  

Wenn Sie die Ausführung eines Berichts planen, können Sie festlegen, dass er jeden Donnerstag ausgeführt werden muss, indem Sie beispielsweise das Feld **Datumsformel für nächste Ausführung** auf *D4* festlegen. Weitere Informationen zu finden Sie unter [Verwenden von Datumsformeln](ui-enter-date-ranges.md#using-date-formulas).  

Sie können wählen, ob Sie den Bericht in einer Datei (wie Excel, Word oder PDF) speichern, ausdrucken oder nur den Bericht generieren wollen. Wenn Sie wählen, den Bericht in eine Datei zu speichern, wird der verarbeitete Bericht an den **Berichts-Eingang** an Ihr Rollencenter gesendet, wo Sie ihn anzeigen können.  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Berichte drucken

Um den Bericht zu drucken, wählen Sie die Schaltfläche **Drucken** auf der Anforderungsseite oder in der Menüleiste der Seite **Vorschau** aus.

### <a name="printer"></a><a name="Printer"></a>Drucker

Das Feld **Drucker** auf der Anforderungsseite zeigt den Name des Druckers an, zu dem der Bericht gesendet wird. Um einen Drucker zu wechseln, wählen Sie einfach den Drucker aus der Liste aus.

> [!NOTE]
> **(Vom Browser gehandhabt)** zeigt an, dass es für den Bericht keinen vorgesehenen Drucker gibt. In diesem Fall handhabt der Browser den Ausdruck und zeigt eine Standardumgebung an, in dem Sie einen lokalen Drucker auswählen können, der mit Ihrem Gerät verbunden ist. **(Vom Browser gehandhabt)** ist nicht verfügbar in der mobilen App von [!INCLUDE[prod_short](includes/prod_short.md)] oder der App für Microsoft Teams.

> [!TIP]
> Der Drucker, der standardmäßig für Sie ausgewählt wurde, ist auf der Seite **Druckerauswahl** eingerichtet. Informationen zum Ändern des Standarddruckers finden Sie unter [So wählen Sie aus, welche Drucker welche Berichte drucken](ui-specify-printer-selection-reports.md#default).

### <a name="printing-reports-in-thai"></a>Drucken von Berichten in Thailändisch

Speziell für die thailändische Version von [!INCLUDE[prod_short](includes/prod_short.md)] kann die Schaltfläche **Drucken** keine Berichte korrekt drucken, weil der Dienst, der die druckbare PDF-Datei generiert, eingeschränkt ist. Stattdessen können Sie den Bericht in Word öffnen und den Bericht als druckbare PDF-Dateien speichern.  

Oder Sie können Ihren Administrator bitten, ein Word-Berichtslayout für Ihre am häufigsten verwendeten Berichte zu erstellen. Weitere Informationen finden Sie unter [Berichte- und Dokumentenlayouts verwalten](ui-manage-report-layouts.md).  

## <a name="changing-report-layouts"></a>Ändern von Berichtslayouts

Ein Berichtslayout steuert, was in einem Bericht angezeigt wird, wie er angeordnet wird und wie er formatiert ist. Wenn Sie zu einem anderen Layout wechseln möchten, finden Sie Informationen unter [Ändern des aktuellen Berichtlayout](ui-how-change-layout-currently-used-report.md). Oder, wenn Sie Ihr eigenes Berichtslayout anpassen möchten gehen Sie zu [Erstellen und bearbeiten von benutzerdefinierten Berichtslayouts](ui-how-create-custom-report-layout.md).

## <a name="advanced-options"></a>Erweiterte Optionen

Die Felder unter **Erweitert** legen Einschränkungen für den generierten Bericht fest, um Druckerressourcen zu steuern. Normalerweise müssen Sie diese Einstellungen nicht ändern, es sei denn, Sie haben einen umfangreichen Bericht. Wenn ein Bericht diese Einschränkungen überschreitet, wenn Sie versuchen, eine Vorschau anzuzeigen oder zu drucken, wird eine Meldung angezeigt, die Sie darüber informiert, welche Einschränkung überschritten wurde. Sie können die Einstellungen dann gemäß den Erfordernissen für Ihren Bericht ändern. Jedes Feld hat jedoch einen Maximalwert, den Sie beachten sollten:

|Feld|Maximalwert|
|-----|-------------|
|Maximale Rendering-Zeit|12:00:00|
|Maximale Zeilenanzahl|1000000|
|Maximale Beleganzahl|500|

> [!NOTE]
> Die Maximalwerte können sich für [!INCLUDE[prod_short](includes/prod_short.md)] lokal unterscheiden, und ein Administrator kann sie ändern. Weitere Informationen finden Sie unter [Konfigurieren von Business Central Server – Berichte](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Reports). Für eine Übersicht über Berichtseinschränkungen [!INCLUDE[prod_short](includes/prod_short.md)] online sehen Sie [Einschränkungen im Betrieb](/dynamics365/business-central/dev-itpro/administration/operational-limits-online).

## <a name="see-also"></a>Siehe auch

[Drucker einrichten](ui-specify-printer-selection-reports.md)  
[Arbeiten mit Datumsangaben und Uhrzeiten in Kalendern](ui-enter-date-ranges.md)  
[Verwalten von Berichts- und Beleglayouts](ui-manage-report-layouts.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]