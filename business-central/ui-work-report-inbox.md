---
title: Berichte mit dem Berichtseingang teilen und exportieren
description: 'Verwenden Sie die Seite „Berichtseingang“, um Berichte in Business Central herunterzuladen, freizugeben und zu exportieren.'
author: rubenseishima
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'task, process, report, print, schedule, save, Excel, PDF, dataset, export, report inbox, onedrive,'
ms.search.form: 680
ms.date: 08/08/2022
ms.author: a-reishima
---
# <a name="share-and-export-reports-with-the-report-inbox"></a>Berichte mit dem Berichtseingang teilen und exportieren

Die Seite **Berichtseingang** listet geplante Berichte auf, die vom Benutzer in [!INCLUDE[prod_short](includes/prod_short.md)] erstellt wurden, und kann verwendet werden, um nicht nur auf die generierten Berichte zuzugreifen, sondern auch um die Dateien in OneDrive for Business zu teilen und zu öffnen.

> [!TIP]
> Die folgenden Aktionen sind auch im Bereich **Berichtseingang** im Rollencenter verfügbar. Wenn dieser Bereich nicht in Ihrer Benutzeroberfläche angezeigt wird, erfahren Sie hier, wie Sie Ihr Rollencenter anpassen können: [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).

## <a name="download-generated-reports"></a>Generierte Berichte herunterladen

Um frühere Berichte zu speichern, öffnen Sie die Seite **Berichtseingang**, indem Sie diesen Schritten folgen:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?"). Symbol. Geben Sie **Berichtseingang** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Berichtseingang** den gewünschten Bericht aus.

> [!NOTE]
> Die Seite listet keine früheren Berichte auf, die mit der Aktion **Drucken** erstellt oder als Datei im Menü **Berichte** gespeichert wurden.
>
> Die generierten Dateien werden in dem beim Planen des Berichts definierten Format gespeichert und können auf der Seite **Einträge in der Auftragswarteschlange** zusammen mit der Wiederholung und anderen Einstellungen geändert werden. Erfahren Sie unter, wie Sie das Berichtsdateiformat ändern und zusätzliche Optionen festlegen [Verwalten Sie geplante wiederkehrende Berichte](ui-work-report.md#manage-scheduled-recurring-reports).

## <a name="open-generated-reports-in-onedrive"></a>Öffnen Sie generierte Berichte in OneDrive

So exportieren Sie die Berichtsdatei nach Microsoft OneDrive for Business: Wählen Sie den Bericht über die Seite **Berichtseingang** und wählen Sie **In OneDrive öffnen**. Der Bericht wird dann in den [!INCLUDE[prod_short](includes/prod_short.md)] Ordner in OneDrive kopiert und in einem neuen Browserfenster geöffnet, wo Sie die Dokumentdatei drucken und verwalten können.

> [!IMPORTANT]
>
> Berichte, deren Gültigkeitsdauer auf der Seite **Planen Sie einen Bericht** festgelegt und in OneDrive kopiert wurde, werden nicht automatisch aus dem freigegebenen Ordner entfernt.

## <a name="share-scheduled-reports"></a>Geplante Berichte freigeben

Das Teilen von Berichten mit Mitarbeitern ist auch auf der Seite **Berichtseingang** möglich. Wählsen Sie den Bericht und dann **Freigeben** Aktion aus. Auf der Seite **Link senden** wählen Sie aus, wer die Datei öffnen darf, definieren Bearbeitungsberechtigungen und wählen Sie dann **Senden** um einen Link für den Zugriff auf den gespeicherten Bericht zu senden.

> [!NOTE]
> Mehr über die OneDrive Integration und Funktionen für [!INCLUDE[prod_short](includes/prod_short.md)], einschließlich erstmaliger Einrichtung und Optionen zum Umgang mit Dateinamenskonflikten, finden Sie unter [Öffnen und Freigeben von Dateien inOneDrive](across-share-onedrive.md).
>
> Mit der Aktion **Freigeben** wird die generierte Berichtsdatei für andere Benutzer nur auf OneDrive for Business verfügbar gemacht und listet den geplanten Bericht in ihrem **Berichtseingang** nicht auf.

## <a name="see-related-training-at-microsoft-learn"></a>Siehe verwandte Schulungen unter [Microsoft Learn](/learn/paths/build-reports/).

## <a name="see-also"></a>Siehe auch

[Berichte ausführen und drucken](ui-work-report.md)  
[Verfügbare Berichte in [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md)  
[Berichte in der täglichen Arbeit verwenden](reports-use-reports.md)  
[Übersicht über Business Intelligence und Reporting](reports-bi-reporting.md)  
[Drucker einrichten](ui-specify-printer-selection-reports.md)  
[Mit Datumsangaben und Uhrzeiten in Kalendern arbeiten](ui-enter-date-ranges.md)  
[Verwaltung von Berichts- und Dokumentlayouts](ui-manage-report-layouts.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]- und OneDrive-Integration](across-onedrive-overview.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
