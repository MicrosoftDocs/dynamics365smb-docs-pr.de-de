---
title: Business Central und OneDrive für Business Integration
description: 'Sie können OneDrive for Business verwenden, um Dateien zu speichern, zu verwalten und freizugeben, z.B. Berichte oder Dateianhänge. Auch wenn Sie es One Drive buchstabieren.'
author: jswymer
ms.topic: overview
ms.search.keywords: null
ms.date: 02/28/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---

# Business Central und OneDrive für Business Integration

OneDrive for Business ist ein Cloud-Speicherdienst, der in Microsoft 365 enthalten ist. Mit [!INCLUDE[prod_short](includes/prod_short.md)] können Sie ganz einfach Dateien speichern, verwalten und mit anderen Personen über OneDrive teilen. Wenn sich eine Datei in Ihrer OneDrive befindet, profitieren Sie von den vielfältigen Möglichkeiten der Zusammenarbeit mit den Online-Versionen von Microsoft-Produkten, wie Word, Excel und PowerPoint. So können Sie zum Beispiel einen Word Beleg freigeben, den Sie dann gemeinsam mit Ihren Kollegen in Echtzeit bearbeiten können. Mit OneDrive können Sie auch andere Dateitypen öffnen, z. B. PDFs. 

## Einstieg in die Funktionen von OneDrive

Wenn Sie [!INCLUDE[prod_short](includes/prod_short.md)] online verwenden, haben wir bereits die Verbindung zwischen [!INCLUDE[prod_short](includes/prod_short.md)] online und OneDrive erstellt, so dass Sie ganz einfach loslegen können. Die einzige Voraussetzung ist, dass die Benutzer OneDrive mindestens einmal geöffnet haben. Bei [!INCLUDE[prod_short](includes/prod_short.md)] vor Ort muss ein Administrator die Verbindung konfigurieren, bevor Sie loslegen können. Weitere Informationen finden Sie unter [Verwaltung der Integration von OneDrive mit Business Central](admin-onedrive-integration.md).

<!-- We've created the connection between [!INCLUDE[prod_short](includes/prod_short.md)] online and OneDrive, so it's easy to get started. The only requirement is that users have opened OneDrive at least one time. -->

### Öffnen und freigeben in OneDrive

Auf den meisten Seiten, auf denen Dateien verfügbar sind, wie z. B. dem Berichtseingang oder Dateien, die an Datensätze angehängt sind, befinden sich die Aktionen **In OneDrive öffnen** und **Freigeben**.

:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Die Aktionen „In OneDrive öffnen“ und „Freigeben“ für Berichte":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Die Aktionen „In OneDrive öffnen“ und „Freigeben“ für Anhänge":::

|Wählen Sie...|An...|Weitere Informationen...|
|---------|-----|----------------|
|In OneDrive öffnen|Kopieren Sie die Datei in einen Business Central-Ordner in OneDrive, und öffnen Sie die Datei.|[In OneDrive öffnen](across-share-onedrive.md#open-in-onedrive) |
|Anteil|Kopieren Sie die Datei in OneDrive, und geben Sie sie für andere frei.|[In OneDrive freigeben](across-share-onedrive.md#share) |

### Speichern Sie Excel-Arbeitsmappen und Berichtsdateien in OneDrive

Wenn die OneDrive-Integration festgelegt ist, werden einige andere vertraute Funktionen automatisch OneDrive zum Speichern von Dateien verwenden, anstatt Dateien auf Ihrem Gerät zu speichern:

- Die Aktionen **Öffnen in Excel** und **Bearbeiten in Excel** auf Listenseiten kopieren die Excel-Datei automatisch nach OneDrive und öffnen sie dann in Excel Online. Weitere Informationen finden Sie unter [Betrachten und Bearbeiten in Excel](across-work-with-excel.md).
- Wenn Sie einen Bericht an eine Excel- oder Word-Datei senden, wird die Datei automatisch nach OneDrive kopiert und dann in Excel oder Word Online geöffnet. Weitere Informationen finden Sie unter [Speichern eines Berichts in einer Datei](ui-work-report.md#saving-a-report-to-a-file).

Diese Funktionen sind standardmäßig nicht aktiviert. Als Administrator können Sie sie jedoch mit Hilfe der Anleitung zur **OneDrive Einrichtung** ganz einfach einschalten.

<!--
When you use the **Open in OneDrive** action for the first time, [!INCLUDE[prod_short](includes/prod_short.md)] does the following in your OneDrive:

1. Creates a folder named [!INCLUDE[prod_short](includes/prod_short.md)]. 
2. In the [!INCLUDE[prod_short](includes/prod_short.md)] folder, it creates another folder with the same name as the company you're working in. If you work in more than one company, it will create a folder for the company you're working in when you use the **Open in OneDrive** action. 
3. Puts a copy of the file you selected in the folder, and then opens the file. The next time you use the action, it only copies and opens the file. 

The folder and its content are private until you decide to share them with others. For example, you might decide to share content with one or more of your coworkers, or even people outside of your organization. For more information, see [Share OneDrive files and folders](https://support.microsoft.com/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07) in the content for OneDrive.
-->

> [!NOTE]
> Sie können auch Ihr [!INCLUDE[prod_short](includes/prod_short.md)] on-premises mit OneDrive verbinden. Damit dies funktioniert, müssen Sie jedoch einige Dinge beachten. Weitere Informationen finden Sie unter [Konfiguration von Business Central vor Ort](admin-onedrive-integration-onpremises.md).

## Siehe auch

[Verwaltung der OneDrive Integration mit Business Central](admin-onedrive-integration.md)  
[Öffnen von Business Central Dateien in OneDrive](across-share-onedrive.md)  
[OneDrive FAQ](admin-onedrive-faq.md)  
