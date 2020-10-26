---
title: Sie können einen Bericht planen, sodass er an einem bestimmten Datum und zu einer festgelegten Uhrzeit ausgeführt wird | Microsoft Docs
description: Erfahren Sie mehr zum Eingeben eines Berichts in eine Aufgabenwarteschlange und das Planen der Verarbeitung an einem bestimmten Datum und Uhrzeit.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: cdb01a2d74dff2fef15c2207f98ba8893f081aca
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3920372"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Arbeiten mit Berichten, Stapelverarbeitungen und XMLports

Ein Bericht stellt Informationen auf Basis eines bestimmten Satz an Kriterien zusammen und unterteilt die Informationen in ein einfach zu lesendes, druckbares Format oder speichert es als Dateil Es gibt viele Berichte, auf die Sie im Zuge der Anwendung zugreifen können. Die Berichte stellen in der Regel Informationen proportional zu dem Kontext der Seite bereit, auf der Sie sich befinden. Beispielsweise der **Debitor** für die Seite Berichte Top 10 Debitoren, die Verkaufsstatistik und mehr.

Stapelverarbeitungen und XMLports machen mehr oder weniger das gleiche wie Berichte, aber mit dem Ziel der Durchführung eines Vorgangs. Die Stapelverarbeitung **Mahnungen erstellen** erstellt beispielsweise Mahnungsbelege für Debitoren mit überfälligen Zahlungen.  

> [!NOTE]
> Dieses Thema bezieht sich hauptsächlich auf "Bericht", aber die gleichen Informationen gelten für Stapelverarbeitungen und XMLports.

## <a name="getting-started"></a>Erste Schritte

Sie können Berichte in der Registerkarte **Berichte** auf ausgewählten Seiten finden, oder Sie können die Suche verwenden ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), um Berichte nach Namen zu finden.

Wenn Sie einen Bericht, einen Stapelverarbeitungsauftrag oder XMLport öffnen, wird in der Regel eine Seite dargestellt, mit der Sie bestimmte Informationen definieren können, die Sie im Bericht integrieren möchten. In den folgenden Abschnitten wird erläutert, wie Sie auf der Anforderungsseite einen Bericht erstellen, in der Vorschau anzeigen und drucken.

## <a name="using-default-values---predefined-settings"></a><a name="SavedSettings"></a>Standardwerte verwenden – vordefinierte Einstellungen 

Die meisten Anforderungsseiten enthalten das Feld **Standardwerte verwenden von** . In diesem Feld können Sie vordefinierte Einstellungen für den Bericht auswählen, mit denen automatisch Optionen und Filter für den Bericht festgelegt werden. Wählen Sie einen Posten aus der Dropdownliste aus, und die Optionen und Filter auf der Anforderungsseite ändern sich entsprechend.

Der Posten mit der Bezeichnung **Zuletzt verwendete Optionen und Filter** ist immer verfügbar. Dieser Posten legt fest, dass der Bericht Optionen und Filter verwendet, die verwendet wurden, als Sie das letzte Mal den Bericht ausgeführt hatten.

Das Feld **Standardwerte verwenden von** bietet eine schnelle und zuverlässige Möglichkeit, konsistent Berichte zu generieren, die die richtigen Daten enthalten. Nachdem Sie einen Posten ausgewählt haben, können Sie alle Optionen und Filter ändern, bevor Sie den Bericht in der Vorschau anzeigen oder drucken. Die Änderungen, die Sie vornehmen, werden nicht im vordefinierten Einstellungseintrag gespeichert, den Sie ausgewählt haben, sondern sie werden im Posten **Zuletzt verwendete Optionen und Filter** gespeichert.

>[!NOTE]
> Die vordefinierten Einstellungen werden normalerweise von einem Administrator eingerichtet und verwaltet. Wenn Sie weitere Informationen erhalten möchten, finden Sie diese unter [Gespeicherten Einstellungen für Berichte und Stapelverarbeitungsaufträge verwalten](reports-saving-reusing-settings.md).
<!--
Depending on the report, the request page might include the **Use default values from** field. This field lets you select a predefined set of can include the **Saved Settings** section that contains one or more entries in the **Use default value from** box. A saved setting is basically a predefined group of options and filters that you can apply to the report before previewing or sending the report to a file. The saved settings entry called **Last used options and filters** is always available. This entry sets the report to use options and filters that were used the last time you used the report.

Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data. After you set the **Use default value from** box to a saved settings entry, you can change any of the options and filters before previewing or saving the report. The changes that you make will not be saved to the saved settings entry you selected, but they will be saved to the **Last used options and filters** entry.

>[!NOTE]
>If you are an administrator, you can create and manage the saved settings for reports for all users. For more information, see [Manage Saved Settings for Reports and Batch Jobs](reports-saving-reusing-settings.md).
-->
## <a name="specifying-the-data-to-include-in-reports"></a>Angeben der Daten, die in Berichte eingeschlossen werden sollen

Verwenden Sie die Felder unter **Optionen** und **Filter** zum Ändern der Begrenzung der Informationen, die Sie im Bericht haben möchten. Sie legen Filter in einem Bericht ungefähr so fest wie Filter in Listen. Weitere Informationen finden Sie unter [Filterung](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> Der Abschnitt **Filterlisten nach** auf der Anforderungsseite stellt eine generische Filterungsfunktion für Berichte bereit. Diese Filter sind optional.
>
> Manche Berichte ignorieren solche Filter, was bedeutet, dass, egal welcher Filter im Abschnitt **Filterliste nach** festgelegt ist, das Ergebnis des Berichts gleich ist. Es ist nicht möglich, eine Übersicht zu bieten, welche Felder in welchen Berichten ignoriert werden, daher müssen Sie mit den Filtern experimentieren, wenn Sie sie verwenden.
>
> **Beispiel** : Wenn Sie die Stapelverarbeitung **Mahnungen erstellen** verwenden, wird ein Filter für das Feld **Debitorenposten** aus **Letzte registrierte Mahnstufe** ignoriert, da Filter für diese Stapelverarbeitung fest sind.

## <a name="previewing-a-report"></a>Einen Bericht anzeigen

In der Vorschau eines Berichts können Sie sehen, wie der Bericht aussehen wird, bevor Sie ihn drucken. In der Vorschau wird das Layout des Bericht basierend auf dem [Drucker](#Printer) ausgerichtet, der im Feld **Drucker** auf der Anforderungsseite angezeigt wird. Nach der Vorschau können Sie zur Anforderungsseite zurückkehren und bei Bedarf Änderungen an Optionen und Filtern vornehmen.

Um eine Vorschau eines Berichts anzuzeigen, wählen Sie die Schaltfläche **Vorschau** oder **Vorschau und Schließen** auf der Berichtsanforderungsseite aus. Die angezeigte Schaltfläche hängt vom Bericht ab, daher haben einige Berichte die Schaltfläche **Vorschau** , während andere die Schaltfläche **Vorschau und Schließen** haben. Beide Schaltflächen öffnen eine Vorschau des Berichts. Der Unterschied ist, das **Vorschau** die Anforderungsseite geöffnet lässt, sodass Sie dorthin zurückkehren können, um Änderungen vornehmen, sie erneut in der Vorschau anzuzeigen oder zu drucken. Mit **Vorschau und Schließen** wird die Anforderungsseite geschlossen, sodass Sie den Bericht erneut öffnen müssen, um Änderungen vorzunehmen oder zu drucken.

> [!NOTE]
> Wenn Sie Business Central 2020 Veröffentlichungzyklus 1 oder früher verwenden, gibt es nur eine Schaltfläche **Vorschau** , die die Anforderungsseite in der Vorschau schließt, wie für **Vorschau und Schließen** beschrieben.

### <a name="working-with-the-preview"></a>Arbeiten mit der Vorschau

Verwenden Sie in der Vorschau die Menüleiste in der Berichtsvorschau, um:

- Navigieren durch Seiten
- Ein- und Ausblenden
- An die Seite anpassen
- Text auswählen

    Sie können Text aus einem Bericht kopieren und diesen dann woanders einfügen, z. B. eine Seite in [!INCLUDE[d365fin](includes/d365fin_md.md)] oder Microsoft Word.  Mithilfe einer Maus beispielsweise drücken und halten Sie, wo Sie beginnen möchten, dann bewegen Sie die Maus, um einen oder mehrere Begriffe, Sätze oder Absätze auszuwählen. Drücken Sie die rechte Maustaste und wählen Sie **Kopieren** aus. Fügen Sie dann den ausgewählten Text dort ein, wo Sie möchten.
- Beleg verschieben

    Sie können den sichtbaren Bereich des Berichts in beliebiger Richtung verschieben, daher können Sie weitere Bereiche oder den Bericht anzeigen. Verschieben ist hilfreich, wenn Sie gezoomt haben, um Details anzuzeigen.  Mithilfe der Maus beispielsweise drücken und halten Sie die Maustaste an einem beliebigen Ort in der Berichtsvorschau und bewegen Sie dann Ihre Maus.

- Download in eine PDF-Datei auf Ihrem Computer oder Netzwerk.
- Drucken

## <a name="saving-a-report"></a>Speichern des Berichts

Sie können einen Bericht in ein PDF-Dokument, Microsoft Word Dokument oder Microsoft Excel Dokument speichern, indem Sie die Schaltfläche **Senden an** auswählen, und anschließend Ihre Auswahl treffen.

## <a name="scheduling-a-report-to-run"></a><a name="ScheduleReport"></a> Planen der Ausführung eines Berichts

Sie können einen Bericht oder einen Stapelverarbeitungsauftrag planen, sodass er an einem bestimmten Datum und zu einer festgelegten Uhrzeit ausgeführt wird. Geplante Berichte und Stapelverarbeitungsaufträge werden in der Projektwarteschlange eingegeben und zu der geplanten Zeit verarbeitet, wie vergleichbare andere Aufträge auch. Sie wählen die **Zeitplan** Option, nachdem Sie die Schaltfläche **Senden an** gewählt haben und geben Sie dann Informationen wie den Drucker sowie Uhrzeit und Datum ein. Der Bericht wird der Aufgabenwarteschlange hinzugefügt und zum angegebenen Zeitpunkt ausgeführt. Wenn der Bericht verarbeitet ist, wird das Element aus der Aufgabenwarteschlange entfernt. Weitere Informationen finden Sie unter [Job-Warteschlangen zur Einplanung von Aufgaben verwenden](admin-job-queues-schedule-tasks.md).  

Wenn Sie die Ausführung eines Berichts planen, können Sie festlegen, dass er jeden Donnerstag ausgeführt werden muss, indem Sie beispielsweise das Feld **Datumsformel für nächste Ausführung** auf *D4* festlegen. Weitere Informationen zu finden Sie unter [Verwenden von Datumsformeln](ui-enter-date-ranges.md#using-date-formulas).  

Sie können auswählen, den Bericht in einer Datei zu speichern, beispielsweise als Excel-, Word- oder PDF-Datei, ihn auf einem ausgewählten Drucker auszugeben, oder nur den Bericht zu generieren. Wenn Sie wählen, den Bericht in eine Datei zu speichern, wird der verarbeitete Bericht an den **Berichts-Eingang** an Ihr Rollencenter gesendet, wo Sie ihn anzeigen können.  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Berichte drucken

Um den Bericht zu drucken, wählen Sie die Schaltfläche **Drucken** auf der Anforderungsseite oder in der Menüleiste der Seite **Vorschau** aus.

<!--
### Printer selection

The report prints to the printer shown in the **Selected printer** field on the report request page. You can't change the printer from this page.

The selected printer is either set on the **Printer Selections** page or it's the default printer set up on the **Printer Management** page. If you want to use another printer, see  [Set Up Printers](ui-specify-printer-selection-reports.md).

If no printer is specified on the **Printer Selections** page or set as default on the **Printer Management** page, the browser printing feature is used. In this case, **Browser** appears in the **Selected printer** field on the report request page.
-->
### <a name="printer"></a><a name="Printer"></a>Drucker

Das Feld **Drucker** auf der Anforderungsseite zeigt den Name des Druckers an, zu dem der Bericht gesendet wird. **(Vom Browser gehandhabt)** zeigt an, dass es für den Bericht keinen vorgesehenen Drucker gibt. In diesem Fall handhabt der Browser den Ausdruck und zeigt eine Standardumgebung an, in dem Sie einen lokalen Drucker auswählen können, der mit Ihrem Gerät verbunden ist.

Sie können den Drucker nicht mithilfe des Felds **Drucker** ändern. Um den Drucker zu ändern, müssen Sie zu den Seiten **Druckerauswahlen** oder **Druckerverwaltung** wechseln. Das Festlegen des Druckers ist normalerweise eine Administratoraufgabe. Weitere Informationen finden Sie unter [Drucker einrichten](ui-specify-printer-selection-reports.md).

<!--
### Browser printing

Because [!INCLUDE[prodshort](includes/prodshort.md)] is a cloud service, it can't reach local printers connected to your computer. However, it can connect to cloud-enabled printers. In the generic version of [!INCLUDE[prodshort](includes/prodshort.md)], a cloud printer named **Email Printer** is installed as an extension and is ready to use after initial setup.

If a cloud printer is not installed and set up, or if an installed printer fails, then printing will default to the printing options for the browser.

> [!NOTE]
> The browser printing options work independently of [!INCLUDE[prodshort](includes/prodshort.md)]. So any printer settings that might have been set up from printers in [!INCLUDE[prodshort](includes/prodshort.md)] aren't carried over to the browser print options.

<!-- 
On the **Printer Management** page, you can see the printers that are set up. For more information, see [Set Up Printers](ui-specify-printer-selection-reports.md).

> [!NOTE]
> You can't change the **Printer** field on the report request page. To use another printer, you must select it from the **Printer Management** page.
-->
### <a name="printing-reports-in-thai"></a>Drucken von Berichten in Thailändisch

Speziell für die thailändische Version von [!INCLUDE[prodshort](includes/prodshort.md)] kann die Schaltfläche **Drucken** keine Berichte korrekt drucken, weil der Dienst, der die druckbare PDF-Datei generiert, eingeschränkt ist. Stattdessen können Sie den Bericht in Word öffnen und den Bericht als druckbare PDF-Dateien speichern.  

Alternativ können Sie den Administrator bitten, ein Word-Berichtslayout für Ihre verwendete Berichte zu erstellen. Weitere Informationen finden Sie unter [Berichte- und Dokumentenlayouts verwalten](ui-manage-report-layouts.md).  

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
> Die Maximalwerte können sich für [!INCLUDE[d365fin](includes/d365fin_md.md)] lokal unterscheiden, und ein Administrator kann sie ändern. Weitere Informationen finden Sie unter [Konfigurieren von Business Central Server – Berichte](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Reports). Für eine Übersicht über Berichtseinschränkungen [!INCLUDE[d365fin](includes/d365fin_md.md)] online sehen Sie [Einschränkungen im Betrieb](/dynamics365/business-central/dev-itpro/administration/operational-limits-online).

## <a name="see-also"></a>Siehe auch

[Drucker einrichten](ui-specify-printer-selection-reports.md)  
[Arbeiten mit Datumsangaben und Uhrzeiten in Kalendern](ui-enter-date-ranges.md)  
[Verwalten von Berichts- und Beleglayouts](ui-manage-report-layouts.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
