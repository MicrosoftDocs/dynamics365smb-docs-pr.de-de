---
title: Öffnen von Business Central Dateien in OneDrive
description: 'Erfahren Sie, wie Sie Business Central-Daten über OneDrive for Business freigeben können.'
author: jswymer
ms.topic: conceptual
ms.workload: na
ms.search.keywords: null
ms.date: 08/03/2022
ms.author: jswymer
---
# <a name="opening-and-sharing-business-central-files-in-microsoft-onedrive"></a><a name="opening-and-sharing-business-central-files-in-microsoft-onedrive"></a><a name="opening-and-sharing-business-central-files-in-microsoft-onedrive"></a>Öffnen und Freigeben von Business Central Dateien in Microsoft OneDrive

[!INCLUDE[prod_short](includes/prod_short.md)] macht es Ihnen leicht, Dateien zu speichern, zu verwalten und mit anderen Personen über Microsoft OneDrive for Business auszutauschen. Auf den meisten Seiten mit verfügbaren Dateien, wie z.B. dem Posteingang für Berichte oder wenn Dateien an Datensätze angehängt sind, finden Sie die Aktionen **Öffnen in OneDrive** und **Freigeben**.


:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Die Aktionen „In OneDrive öffnen“ und „Freigeben“ für Berichte":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Die Aktionen „In OneDrive öffnen“ und „Freigeben“ für Anhänge":::


## <a name="open-in-onedrive"></a><a name="open-in-onedrive"></a><a name="open-in-onedrive"></a>In OneDrive öffnen

Die Aktion **Öffnen in OneDrive** kopiert die Datei in Ihr OneDrive und öffnet die Datei dann in einer Anwendung wie Microsoft Excel online, Microsoft Word online oder Microsoft PowerPoint online. 

<!--## Working with different types of files-->

Wenn Sie **Öffnen in OneDrive** wählen, identifiziert [!INCLUDE[prod_short](includes/prod_short.md)] Excel-, Word- und PowerPoint-Dateien und öffnet sie in den jeweiligen Online-Anwendungen, d.h. Excel online, Word online und PowerPoint online. 

Mit den Online-Versionen dieser Anwendungen können Sie Anmerkungen machen, bearbeiten und mit anderen zusammenarbeiten, ohne den Browser zu verlassen.

Für andere gängige Dateitypen wie PDFs, Textdateien und Bilder bietet OneDrive Dateibetrachter, die Funktionen zum Drucken, Teilen und mehr bieten. Wenn eine Datei nicht in OneDrive angezeigt werden kann, werden Sie möglicherweise aufgefordert, sie herunterzuladen.

## <a name="share"></a><a name="share"></a><a name="share"></a>Freigeben

Die Aktion **Freigeben** kopiert die Datei in Ihr OneDrive, so dass Sie sehen können, mit wem Sie sie bereits geteilt haben, und die Datei mit anderen Personen teilen können. Wenn Sie die Aktion **Freigeben** auswählen, wird die folgende Seite geöffnet.

:::image type="content" source="media/share-to-onedrive-dialog-v2.PNG" alt-text="Datei in OneDrive teilen":::

Wenn Sie mit OneDrive vertraut sind, erkennen Sie die oben erwähnte Seite vielleicht wieder. Sie sehen, dass Sie zwei Optionen zum Teilen der Datei haben: **Link senden** und **Link kopieren**.

- Mit **Link senden** können Sie die Dateien für bestimmte Personen freigeben. Die Personen, für die Sie die Datei freigeben, erhalten eine E-Mail mit einem Link zur Datei. Die Datei wird auch im Abschnitt **Freigegeben** von OneDrive angezeigt. Geben Sie zunächst die E-Mail-Adressen oder Kontaktnamen in das Feld **Name, Gruppe oder E-Mail** ein. Fügen Sie eine Nachricht unter dem Feld **Name, Gruppe oder E-Mail** ein, wenn Sie möchten.

  > [!TIP]
  > Wenn Sie Ihre Nachricht in Outlook verfassen möchten, wählen Sie die Schaltfläche **Outlook**. Der Link wird in einen E-Mail-Entwurf eingefügt und alle Personen, die Sie zum Teilen eingegeben haben, werden in der Liste **An** aufgeführt. Mit dieser Option können Sie E-Mails mit allen Funktionen von Outlook verfassen, z.B. Text formatieren, andere Anhänge hinzufügen, Bilder oder Tabellen einfügen und CC- oder BCC-Empfänger hinzufügen.

- **Link kopieren** kopiert einen Dateilink, den Sie verwenden können, um die Datei über Anwendungen wie Facebook, Twitter oder E-Mail weiterzugeben. 

Bevor Sie einen Dateilink senden oder kopieren, legen Sie die Berechtigungsstufe fest, die andere Personen haben sollen. Sie können die aktuelle Einstellung unter **Link senden** oder **Link kopieren** sehen. In den meisten Fällen wird es **Jeder, der den Link hat, kann ihn bearbeiten** sein, je nachdem, was Ihr Administrator festgelegt hat. Um die Berechtigungen zu ändern, wählen Sie den Link aus, und nehmen Sie Änderungen auf der Seite **Link-Einstellungen** vor.

Die Freigabefunktion in Business Central basiert auf OneDrive. Mehr über OneDrive Freigaben und Berechtigungen erfahren Sie unter [Freigeben von OneDrive Dateien und Ordnern](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

> [!NOTE]
> Die Aktion **Freigeben** ist in der Business Central-App für mobile Geräte nicht verfügbar.

## <a name="first-time-sign-in-from-business-central"></a><a name="first-time-sign-in-from-business-central"></a><a name="first-time-sign-in-from-business-central"></a>Erstmalige Anmeldung über Business Central

Wenn Sie die Aktion **In OneDrive öffnen** oder **Freigeben** zum ersten Mal verwenden, führt [!INCLUDE[prod_short](includes/prod_short.md)] die folgenden Schritte aus:

1. Öffnet die Seite **Allgemeine Geschäftsbedingungen lesen**. Lesen Sie die Seite, und wählen Sie, wenn Sie mit den Nutzungsbedingungen einverstanden sind, **Zustimmen** aus, um den Vorgang fortzusetzen.
2. Erstellt einen Ordner mit dem Namen [!INCLUDE[prod_short](includes/prod_short.md)] in OneDrive. 
3. Innerhalb des Ordners [!INCLUDE[prod_short](includes/prod_short.md)] erstellt es einen Ordner mit dem Namen der Firma, in der Sie arbeiten. Wenn Sie in mehr als einer Firma arbeiten, erstellt [!INCLUDE[prod_short](includes/prod_short.md)] einen Ordner für jede Firma, in der Sie arbeiten, wenn Sie die Aktion **Öffnen in OneDrive** oder **Freigeben** verwenden. 
4. Legt eine Kopie der von Ihnen ausgewählten Datei im Ordner mit dem Namen der Firma ab und öffnet die Datei dann. 

Wenn Sie dann das nächste Mal die Aktion **Öffnen in OneDrive** oder **Freigeben** verwenden, kopiert und öffnet [!INCLUDE[prod_short](includes/prod_short.md)] die Datei nur. 

## <a name="managing-multiple-copies-of-a-file"></a><a name="managing-multiple-copies-of-a-file"></a><a name="managing-multiple-copies-of-a-file"></a>Verwalten mehrerer Kopien einer Datei

Wenn Sie **In OneDrive öffnen** oder **Freigeben** auswählen, wird die Datei von [!INCLUDE[prod_short](includes/prod_short.md)] in Ihren Ordner in OneDrive kopiert. Wenn Sie die Datei in OneDrive bearbeiten, unterscheidet sich diese Datei von der Datei in [!INCLUDE[prod_short](includes/prod_short.md)]. Um [!INCLUDE[prod_short](includes/prod_short.md)] mit der neuesten Dateiversion zu aktualisieren, entfernen Sie die vorhandene Datei aus [!INCLUDE[prod_short](includes/prod_short.md)] und laden Sie die neueste Kopie hoch.

Wenn in OneDrive bereits eine Datei mit demselben Namen existiert, haben Sie die folgenden Möglichkeiten:

- **Vorhandenes verwenden**

  Mit dieser Option wird die Datei, die bereits in OneDrive gespeichert ist, geöffnet oder freigegeben, anstatt die Datei aus Business Central zu kopieren.
  
- **Ersetzen**
  
  Mit dieser Option wird die vorhandene Datei in OneDrive durch die Datei ersetzt, die Sie in Business Central ausgewählt haben. Die ursprüngliche Datei geht dabei nicht verloren &mdash;Sie können sie mit Hilfe des Versionsverlaufs in OneDrive sehen und wiederherstellen. Erfahren Sie mehr unter [Wiederherstellen einer früheren Version einer in OneDrive gespeicherten Datei“](https://support.microsoft.com/office/restore-a-previous-version-of-a-file-stored-in-onedrive).

- **Beides beibehalten**
 
  Mit dieser Option behalten Sie die vorhandene Datei bei und speichern die Datei, die Sie in Business Central ausgewählt haben, unter einem anderen Namen. Der neue Name ähnelt dem vorhandenen Namen, nur mit einer Zusatznummer wie „Elemente (2).xlsx“.

## <a name="about-your-business-central-folder-on-onedrive"></a><a name="about-your-business-central-folder-on-onedrive"></a><a name="about-your-business-central-folder-on-onedrive"></a>Informationen zu Ihrem Business Central-Ordner auf OneDrive

Der Ordner und sein Inhalt sind privat, bis Sie sich entscheiden, sie mit anderen zu teilen. Sie könnten also beschließen, Inhalte mit einem oder mehreren Ihrer Mitarbeiter oder sogar mit Personen außerhalb Ihres Unternehmens zu teilen. 

Sie können auf Ihre OneDrive von der Seite **Meine Einstellungen** aus zugreifen, indem Sie den Link im Feld **Cloud-Speicher** wählen. Erfahren Sie mehr unter [Freigeben von OneDrive Dateien und Ordnern](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

:::image type="content" source="media/my-settings-cloud-storage.PNG" alt-text="Das Feld Cloud-Speicher in Meine Einstellungen":::

<!--## Extending the Connection to OneDrive
You can create an extension and connect it to... For more information, see...-->

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Siehe auch

[Business Central und OneDrive Integration](across-onedrive-overview.md)  
[Verwaltung der OneDrive Integration mit Business Central](admin-onedrive-integration.md)  
[OneDrive FAQ](admin-onedrive-faq.md)
