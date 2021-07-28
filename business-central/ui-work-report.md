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
ms.date: 06/21/2021
ms.author: jswymer
ms.openlocfilehash: 9deb7e30e05da74e6ea263a0262680d2e99b8b4b
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6439950"
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

In der Vorschau eines Berichts können Sie sehen, wie der Bericht aussehen wird, bevor Sie ihn drucken. Die Vorschau basiert nicht auf dem ausgewählten Feld **Drucker** auf der Anforderungsseite. Das wird vom Browser gesteuert. Nach der Vorschau können Sie zur Anforderungsseite zurückkehren und bei Bedarf Änderungen an Optionen und Filtern vornehmen.

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

### <a name="send-to-excel"></a>An Excel senden

<!-- The following table describes the options for saving the report results as a worksheet in an Excel workbook.

|Option  |Description  |
|---------|---------|
|Microsoft Excel Document (data and layout)|Export the report results with the RDLC layout applied. Use this option if you want to export the data one time, and only want to make minor changes to its appearance, such as font and color scheme. <br><br>**Note**: Some reports might export numbers as text, so it's a good idea to verify the numbers. |
|Microsoft Excel Document (data only)|Export the report results and the criteria that was used to generate them, such as the parameters you specified on the request page, metadata, and the fields that control the layout of the printed report. Use this option when you want to do ad hoc analysis of the data or diagnose data issues in reports. For example, you can filter the data and use Power Pivot to display it.<br><br>This option exports all columns, including columns that hold formatting instructions for other values and filters. In columns that hold binary data like images, instead of actually values, fields will include the text **Binary data ({0} bytes)**, where **{0}** indicates the number of bytes.<br><br>**NOTE** With Business Central on-premises, the Business Central Server includes a configurations setting, called **Max Data Rows Allowed to Send to Excel**. This setting limits the number of rows that can be exported to Excel. If you don't see the expected number of rows, it might be because of this setting. For more information, see [Configuring Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General) or contact your administrator.|-->

Es gibt zwei Optionen zum Speichern der Reportergebnisse als Arbeitsblatt in einer Excel-Arbeitsmappe: **Microsoft Excel Dokument (Daten und Layout)** und **Microsoft Excel Dokument (nur Daten)**

#### <a name="microsoft-excel-document-data-and-layout"></a>[Microsoft Excel Dokument (Daten und Layout)](#tab/data-and-layout)

Diese Option ist nur für Berichte verfügbar, die ein RDLC-Layout verwenden. Sie exportiert die Berichtsergebnisse mit dem angewendeten RDLC-Layout. Verwenden Sie diese Option, wenn Sie die Daten einmalig exportieren und nur geringfügige Änderungen am Erscheinungsbild vornehmen wollen, z. B. an der Schriftart und dem Farbschema.

#### <a name="microsoft-excel-document-data-only"></a><a name="exportdataonly"></a>[Microsoft Excel Beleg (nur Daten)](#tab/data-only)

Die Option **Microsoft Excel Dokument (nur Daten)** exportiert die Berichtsergebnisse und die Kriterien, die zu ihrer Erzeugung verwendet wurden&mdash;, aber sie enthält nicht das Berichtslayout. Die Excel-Datei enthält das komplette Dataset, als Rohdaten, angeordnet in Zeilen und Spalten. Alle Datenspalten des Datasets des Berichts sind enthalten, unabhängig davon, ob sie im Berichtslayout verwendet werden.  Verwenden Sie diese Option, wenn Sie:

- Ad-hoc-Analysen der Daten durchführen wollen. Sie können z. B. die Daten filtern und Power Pivot verwenden, um sie anzuzeigen.

  Jedes Mal, wenn Sie Ergebnisse exportieren, wird ein neues Arbeitsblatt erstellt. Mit der Option **Microsoft Excel Beleg (nur Daten)** können Sie denselben Bericht ausführen und Formatierungsänderungen wiederverwenden. Zum Beispiel können Sie für Power Pivot den Bericht für einen anderen Zeitraum erneut ausführen, die Ergebnisse in das Arbeitsblatt kopieren und dann das Arbeitsblatt aktualisieren. Eine App für Berichte finden Sie auch auf [AppSource](https://appsource.microsoft.com/).
- Überprüfen Sie das Dataset des Berichts, wenn Sie angepasste Berichtslayouts erstellen oder ändern.

  Informationen zum Erstellen von angepassten Berichtslayouts finden Sie unter [Erstellen oder Ändern von angepassten Berichtslayouts](ui-how-create-custom-report-layout.md)
- Diagnose von Datenproblemen in Berichten.

##### <a name="for-administrators"></a>Für Administratoren

- **Microsoft Excel Beleg (nur Daten)** wurde als optionale Funktion in der 2021er Release-Welle 1, Update 18.3 eingeführt. Um Benutzern Zugriff auf diese Funktion zu geben, aktivieren Sie die Funktion **Berichts-Dataset in Microsoft Excel Dokument speichern** in **Funktionsverwaltung**. Weitere Informationen finden Sie unter [Bevorstehende Funktionen im Voraus aktivieren](/dynamics365/business-central/dev-itpro/administration/feature-management). In der Release-Welle 2 im Jahr 2021 wird diese Funktion dauerhaft, sodass Sie sie nicht mehr aktivieren müssen.

- Benutzerkonten benötigen die Berechtigung **<!--Export Report Dataset To Excel-->Aktion „Berichtsdataset in Excel exportieren“ zulassen**, die Sie über die auf **Tools zur Problembehandlung** oder **Berichtsdataset in Excel exportieren** festgelegte Berechtigung anwenden können.  

- Sie können keinen Bericht exportieren, der mehr als 1.048.576 Zeilen oder 16.384 Spalten hat.

    > [!NOTE]
    > Bei Business Central lokal kann die maximale Anzahl der exportierten Zeilen sogar noch geringer sein. Business Central Server enthält eine Konfigurationseinstellung mit der Bezeichnung **Maximal zulässige Anzahl der an Excel zu sendenden Datenzeilen**, mit der Sie die Grenze vom Maximalwert herabsetzen können. Weitere Informationen finden Sie unter [Konfiguration von Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General) oder wenden Sie sich an Ihren Administrator.

##### <a name="for-developers-and-advanced-users"></a>Für Entwickler und fortgeschrittene Benutzer

Die Option **Microsoft Excel Dokument (nur Daten)** exportiert alle Spalten, einschließlich Spalten, die Filter und Formatierungsanweisungen für andere Werte enthalten. Hier sind einige Punkte von Interesse:

- Binäre Daten in einem Feld, wie ein Bild, werden nicht exportiert.

  In Spalten, die binäre Daten enthalten, enthalten Felder den Text **Binäre Daten ({0} Bytes)**, wobei **{0}** die Anzahl der Bytes angibt.
- Ab Business Central 2021 Release Wave 2 enthält die Excel-Datei auch das Arbeitsblatt **Berichts-Metadaten**.

  Dieses Arbeitsblatt zeigt die auf den Bericht angewendeten Filter und allgemeine Berichtseigenschaften, wie Name, ID und Erweiterungsdetails. Die Filter werden in der Spalte **Filter (DataItem ::Table ::FilterGroupNo ::FieldName)** angezeigt. Die Filter in dieser Spalte enthalten Filter, die auf der Anforderungsseite des Berichts festgelegt wurden. Sie enthält auch Filter, die im AL-Code definiert sind, zum Beispiel durch die [DataItemLink-Eigenschaft](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemlink-reports-property) und [DataItemTableView-Eigenschaft](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemtableview-property).

Weitere Informationen zur Berichtsgestaltung finden Sie unter [Berichtsübersicht](/dynamics365/business-central/dev-itpro/developer/devenv-reports).

---

> [!NOTE]
> Einige Berichte exportieren Zahlen als Text, was Sie daran hindert, Berechnungen durchzuführen oder Power Pivot auf den Zellen im Excel-Arbeitsblatt zu verwenden. Nach dem Export ist es eine gute Idee, die Zahlen im Arbeitsblatt zu überprüfen. Wenn Sie mit den Zahlen Analysen und Diagramme erstellen wollen, ändern Sie das Format der betreffenden Zellen von **Text** auf **Zahl**. Weitere Informationen zum Formatieren von Zahlen in Zellen finden Sie in diesem Video [Zahlen in Zellen in Microsoft Excel formatieren](https://www.youtube.com/watch?v=2suE4YmZu_Q).

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