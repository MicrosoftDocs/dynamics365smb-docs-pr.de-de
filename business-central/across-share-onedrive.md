---
title: Öffnen von Business Central Dateien in OneDrive
description: Erfahren Sie, wie Sie Business Central-Daten über OneDrive for Business freigeben können.
author: jswymer
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 02/28/2022
ms.author: jswymer
ms.openlocfilehash: 2e1cc04d265541c87244dcd6c13b14327f07cc2f
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8516421"
---
# <a name="opening-and-sharing-business-central-files-in-onedrive"></a>Öffnen und Freigeben von Business Central-Dateien in OneDrive

[!INCLUDE[prod_short](includes/prod_short.md)] macht es Ihnen leicht, Dateien zu speichern, zu verwalten und mit anderen Personen über OneDrive for Business zu teilen. Auf den meisten Seiten, auf denen Dateien verfügbar sind, wie z. B. dem Berichtseingang oder Dateien, die an Datensätze angehängt sind, befindet sich die Aktion **In OneDrive öffnen** und **Freigeben**.


:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Die Aktionen „In OneDrive öffnen“ und „Freigeben“ für Berichte":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Die Aktionen „In OneDrive öffnen“ und „Freigeben“ für Anhänge":::

<!--
:::image type="content" source="media/Open in OneDrive.PNG" alt-text="The Open in OneDrive action":::

 
:::image type="content" source="media/OneDrive attachment.PNG" alt-text="Share file attachments in OneDrive":::
-->

## <a name="open-in-onedrive"></a>In OneDrive öffnen

Mit der Aktion **In OneDrive öffnen** wird die Datei in OneDrive kopiert und in Onlineanwendungen wie Excel Online, Word Online und PowerPoint Online geöffnet. 

<!--## Working with Different Types of Files-->

Wenn Sie **Öffnen in OneDrive** wählen, identifiziert [!INCLUDE[prod_short](includes/prod_short.md)] Excel-, Word- und PowerPoint-Dateien und öffnet sie in den jeweiligen Online-Anwendungen, d.h. Excel online, Word online und PowerPoint online. Sie können Anmerkungen machen, bearbeiten und mit anderen zusammenarbeiten, ohne den Browser zu verlassen.

Für andere gängige Dateitypen wie PDFs, Textdateien und Bilder bietet OneDrive Dateibetrachter, die Funktionen zum Drucken, Teilen und mehr bieten. Wenn eine Datei nicht in OneDrive angezeigt werden kann, werden Sie möglicherweise aufgefordert, sie herunterzuladen.

## <a name="share"></a>Anteil

Mit der Aktion **Freigeben** wird die Datei in OneDrive kopiert und Sie können sie für andere Personen freigeben und anzeigen, für wen Sie sie bereits freigegeben haben. Wenn Sie die Aktion **Freigeben** auswählen, wird die folgende Seite geöffnet.

:::image type="content" source="media/share-to-onedrive-dialog.PNG" alt-text="In OneDrive freigeben":::

Wenn Sie mit OneDrive vertraut sind, erkennen Sie die Seite möglicherweise. Sie haben zwei Möglichkeiten, die Datei freizugeben: **Link senden** und **Link kopieren**.

- Mit **Link senden** können Sie die Dateien für bestimmte Personen freigeben. Die Personen, für die Sie die Datei freigeben, erhalten eine E-Mail mit einem Link zur Datei. Die Datei wird auch im Abschnitt **Freigegeben** von OneDrive angezeigt. Geben Sie zunächst die E-Mail-Adressen oder Kontaktnamen in das Feld **Name, Gruppe oder E-Mail** ein.

- Mit **Link kopieren** wird ein Link zur Datei in OneDrive kopiert, sodass Sie den Link auch an anderen Orten wie Facebook, Twitter oder E-Mails verwenden können. 

Bevor Sie den Link senden oder kopieren, legen Sie die Berechtigung für die Datei fest, die Personen zugewiesen werden sollen. Die aktuelle Einstellung wird unter **Link senden** und **Link kopieren** angezeigt. In den meisten Fällen ist es **Jeder, der über den Link verfügt, kann Änderungen vornehmen, um den Link zu öffnen**, abhängig von den Einstellungen Ihres Administrators. Um die Berechtigungen zu ändern, wählen Sie den Link aus, und nehmen Sie Änderungen auf der Seite **Link-Einstellungen** vor.

Die Freigabefunktion in Business Central basiert auf OneDrive. Weitere Informationen zur Freigabefunktion und zu Berechtigungen finden Sie unter [OneDrive-Dateien und -Ordner freigeben](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

> [!NOTE]
> Die Aktion **Freigeben** ist in der Business Central-App für mobile Geräte nicht verfügbar.

## <a name="first-time-sign-in-from-business-central"></a>Erstmalige Anmeldung über Business Central

Wenn Sie die Aktion **In OneDrive öffnen** oder **Freigeben** zum ersten Mal verwenden, führt [!INCLUDE[prod_short](includes/prod_short.md)] die folgenden Schritte aus:

1. Öffnet die Seite **Allgemeine Geschäftsbedingungen lesen**. Lesen Sie die Seite, und wählen Sie, wenn Sie mit den Nutzungsbedingungen einverstanden sind, **Zustimmen** aus, um den Vorgang fortzusetzen.
2. Öffnet die Seite **Konto auswählen**. Wählen Sie Ihr Konto oder die Option **anderes Konto verwenden** aus, wenn Ihr eigenes nicht angezeigt wird, und geben Sie dann den Benutzernamen und das Kennwort ein, wenn Sie dazu aufgefordert werden.
3. Erstellt einen Ordner mit dem Namen [!INCLUDE[prod_short](includes/prod_short.md)] in OneDrive. 
4. In dem Ordner [!INCLUDE[prod_short](includes/prod_short.md)] erstellt es einen weiteren Ordner mit dem Namen der Firma, in der Sie arbeiten. Wenn Sie in mehreren Unternehmen beschäftigt sind, wird ein Ordner des Unternehmens erstellt, in dem Sie arbeiten, wenn Sie die Aktionen **In OneDrive öffnen** und **Freigeben** verwenden. 
5. Legt eine Kopie der von Ihnen ausgewählten Datei in dem Ordner ab und öffnet dann die Datei. Wenn Sie die Aktion das nächste Mal verwenden, wird die Datei nur kopiert und geöffnet. 

## <a name="managing-multiple-copies-of-a-file"></a>Verwalten mehrerer Kopien einer Datei

Wenn Sie **In OneDrive öffnen** oder **Freigeben** auswählen, wird die Datei von [!INCLUDE[prod_short](includes/prod_short.md)] in Ihren Ordner in OneDrive kopiert. Wenn Sie die Datei in OneDrive bearbeiten, werden die Kopien der Datei unterschiedlich sein. Um [!INCLUDE[prod_short](includes/prod_short.md)] mit der neuesten Datei zu aktualisieren, entfernen Sie die vorhandene Datei aus [!INCLUDE[prod_short](includes/prod_short.md)] und laden dann die neueste Kopie hoch.

Wenn eine Datei mit demselben Namen bereits in OneDrive vorhanden ist, bietet Ihnen [!INCLUDE[prod_short](includes/prod_short.md)] außerdem die Möglichkeit, die Datei zu ersetzen oder beide Dateien zu behalten. Wenn Sie beide Dateien behalten möchten, wird die neue Datei in OneDrive kopiert und erhält einen Dateinamen mit einer Suffixnummer, z. B. „Artikel (2).xlsx“. Die ursprügnliche Datei wird nicht verändert. 

Wenn Sie sich dafür entscheiden, die Datei zu ersetzen, wird die neue Datei dem Versionsverlauf für diese Datei hinzugefügt. Die Originaldatei geht dabei nicht verloren und Sie können frühere Versionen der Datei anzeigen oder wiederherstellen. 

## <a name="about-your-business-central-folder-on-onedrive"></a>Informationen zu Ihrem Business Central-Ordner auf OneDrive

Der Ordner und sein Inhalt sind privat, bis Sie sich entscheiden, sie mit anderen zu teilen. Sie könnten beispielsweise beschließen, Inhalte mit einem oder mehreren Ihrer Mitarbeiter oder sogar mit Personen außerhalb Ihres Unternehmens zu teilen. Sie können auf Ihre OneDrive von der Seite **Meine Einstellungen** aus zugreifen, indem Sie den Link im Feld **Cloud-Speicher** wählen. Weitere Informationen finden Sie unter [Freigeben von OneDrive Dateien und Ordnern](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

:::image type="content" source="media/my-settings-cloud-storage.PNG" alt-text="Das Feld Cloud-Speicher in Meine Einstellungen":::

<!--## Extending the Connection to OneDrive
You can create an extension and connect it to... For more information, see...-->

## <a name="see-also"></a>Weitere Informationen
[Business Central und OneDrive Integration](across-onedrive-overview.md)  
[Verwaltung der OneDrive Integration mit Business Central](admin-onedrive-integration.md)  
[OneDrive FAQ](admin-onedrive-faq.md)