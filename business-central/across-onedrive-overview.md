---
title: Business Central und OneDrive für Business Integration
description: Sie können OneDrive for Business verwenden, um Dateien zu speichern, zu verwalten und freizugeben, z.B. Berichte oder Dateianhänge.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: overview
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: bholtorf
ms.openlocfilehash: 8965fe1c0f04c3b12fef984e71b7f2643f7f11c2
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/19/2022
ms.locfileid: "8012575"
---
# <a name="business-central-and-onedrive-for-business-integration"></a>Business Central und OneDrive für Business Integration
OneDrive for Business ist ein Cloud-Speicherdienst, der in Microsoft 365 enthalten ist. Mit [!INCLUDE[prod_short](includes/prod_short.md)] können Sie ganz einfach Dateien speichern, verwalten und mit anderen Personen über OneDrive teilen. Wenn sich eine Datei in Ihrem OneDrive befindet, können Sie die vielfältigen Möglichkeiten der Zusammenarbeit mit den Online-Versionen von Microsoft-Produkten wie Word, Excel und PowerPoint nutzen. So können Sie zum Beispiel einen Word Beleg freigeben, den Sie dann gemeinsam mit Ihren Kollegen in Echtzeit bearbeiten können. Mit OneDrive können Sie auch andere Dateitypen öffnen, z. B. PDFs. 

## <a name="getting-started"></a>Erste Schritte
Wir haben die Verbindung zwischen [!INCLUDE[prod_short](includes/prod_short.md)] online und OneDrive erstellt, sodass Sie ganz einfach loslegen können. Die einzige Voraussetzung ist, dass die Benutzer OneDrive mindestens einmal geöffnet haben. 

Auf den meisten Seiten, auf denen Dateien verfügbar sind, wie z.B. dem Berichtseingang oder Dateien, die an Datensätze angehängt sind, finden Sie eine **Öffnen in OneDrive** Aktion.

:::image type="content" source="media/Open in OneDrive.PNG" alt-text="Die Aktion Öffnen in OneDrive":::

 
:::image type="content" source="media/OneDrive attachment.PNG" alt-text="Freigeben von Dateianhängen in OneDrive":::

Wenn Sie die Aktion **Öffnen in OneDrive** zum ersten Mal verwenden, führt [!INCLUDE[prod_short](includes/prod_short.md)] in Ihrem OneDrive Folgendes aus:

1. Er erstellt einen Ordner mit dem Namen [!INCLUDE[prod_short](includes/prod_short.md)]. 
2. In dem Ordner [!INCLUDE[prod_short](includes/prod_short.md)] erstellt es einen weiteren Ordner mit dem Namen der Firma, in der Sie arbeiten. Wenn Sie in mehr als einer Firma arbeiten, erstellt es einen Ordner für die Firma, in der Sie arbeiten, wenn Sie die Aktion **Öffnen in OneDrive** verwenden. 
3. Legt eine Kopie der von Ihnen ausgewählten Datei in dem Ordner ab und öffnet dann die Datei. Wenn Sie die Aktion das nächste Mal verwenden, wird die Datei nur kopiert und geöffnet. 

Der Ordner und sein Inhalt sind privat, bis Sie sich entscheiden, sie mit anderen zu teilen. Sie könnten beispielsweise beschließen, Inhalte mit einem oder mehreren Ihrer Mitarbeiter oder sogar mit Personen außerhalb Ihres Unternehmens zu teilen. Weitere Informationen finden Sie unter [Freigeben von OneDrive Dateien und Ordnern](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

> [!NOTE]
> Sie können auch Ihr [!INCLUDE[prod_short](includes/prod_short.md)] on-premises mit OneDrive verbinden. Damit dies funktioniert, müssen Sie jedoch einige Dinge beachten. Weitere Informationen finden Sie unter [Konfiguration von Business Central On-Premises](admin-onedrive-integration.md#configuring-business-central-on-premises).

## <a name="see-also"></a>Weitere Informationen
[Verwaltung der OneDrive Integration mit Business Central](admin-onedrive-integration.md)  
[Öffnen von Business Central Dateien in OneDrive](across-share-onedrive.md)  
[OneDrive FAQ](admin-onedrive-faq.md)