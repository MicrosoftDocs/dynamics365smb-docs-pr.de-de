---
title: Business Central und OneDrive für Business Integration
description: Sie können OneDrive for Business verwenden, um Dateien zu speichern, zu verwalten und freizugeben, z.B. Berichte oder Dateianhänge.
author: jswymer
ms.topic: overview
ms.workload: na
ms.search.keywords: ''
ms.date: 02/28/2022
ms.author: jswymer
ms.openlocfilehash: 371c090e321992ec2fdc0ee7cb218feaa6b16d9a
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8521228"
---
# <a name="business-central-and-onedrive-for-business-integration"></a>Business Central und OneDrive für Business Integration

OneDrive for Business ist ein Cloud-Speicherdienst, der in Microsoft 365 enthalten ist. Mit [!INCLUDE[prod_short](includes/prod_short.md)] können Sie ganz einfach Dateien speichern, verwalten und mit anderen Personen über OneDrive teilen. Wenn sich eine Datei in Ihrem OneDrive befindet, können Sie die vielfältigen Möglichkeiten der Zusammenarbeit mit den Online-Versionen von Microsoft-Produkten wie Word, Excel und PowerPoint nutzen. So können Sie zum Beispiel einen Word Beleg freigeben, den Sie dann gemeinsam mit Ihren Kollegen in Echtzeit bearbeiten können. Mit OneDrive können Sie auch andere Dateitypen öffnen, z. B. PDFs. 

## <a name="getting-started"></a>Erste Schritte

Wir haben die Verbindung zwischen [!INCLUDE[prod_short](includes/prod_short.md)] online und OneDrive erstellt, sodass Sie ganz einfach loslegen können. Die einzige Voraussetzung ist, dass die Benutzer OneDrive mindestens einmal geöffnet haben. 

Auf den meisten Seiten, auf denen Dateien verfügbar sind, wie z. B. dem Berichtseingang oder Dateien, die an Datensätze angehängt sind, befinden sich die Aktionen **In OneDrive öffnen** und **Freigeben**.

:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Die Aktionen „In OneDrive öffnen“ und „Freigeben“ für Berichte":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Die Aktionen „In OneDrive öffnen“ und „Freigeben“ für Anhänge":::

|Wählen Sie...|An...|Weitere Informationen...|
|---------|-----|----------------|
|In OneDrive öffnen|Kopieren Sie die Datei in einen Business Central-Ordner in OneDrive, und öffnen Sie die Datei.|[In OneDrive öffnen](across-share-onedrive.md#open-in-onedrive) |
|Anteil|Kopieren Sie die Datei in OneDrive, und geben Sie sie für andere frei.|[In OneDrive freigeben](across-share-onedrive.md#share) |

<!--
When you use the **Open in OneDrive** action for the first time, [!INCLUDE[prod_short](includes/prod_short.md)] does the following in your OneDrive:

1. Creates a folder named [!INCLUDE[prod_short](includes/prod_short.md)]. 
2. In the [!INCLUDE[prod_short](includes/prod_short.md)] folder, it creates another folder with the same name as the company you're working in. If you work in more than one company, it will create a folder for the company you're working in when you use the **Open in OneDrive** action. 
3. Puts a copy of the file you selected in the folder, and then opens the file. The next time you use the action, it only copies and opens the file. 

The folder and its content are private until you decide to share them with others. For example, you might decide to share content with one or more of your coworkers, or even people outside of your organization. For more information, see [Share OneDrive files and folders](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).
-->

> [!NOTE]
> Sie können auch Ihr [!INCLUDE[prod_short](includes/prod_short.md)] on-premises mit OneDrive verbinden. Damit dies funktioniert, müssen Sie jedoch einige Dinge beachten. Weitere Informationen finden Sie unter [Konfiguration von Business Central On-Premises](admin-onedrive-integration.md#configuring-business-central-on-premises).

## <a name="see-also"></a>Weitere Informationen
[Verwaltung der OneDrive Integration mit Business Central](admin-onedrive-integration.md)  
[Öffnen von Business Central Dateien in OneDrive](across-share-onedrive.md)  
[OneDrive FAQ](admin-onedrive-faq.md)