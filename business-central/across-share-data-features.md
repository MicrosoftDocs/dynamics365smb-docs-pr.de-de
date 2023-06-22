---
title: Freigeben von Daten
description: 'Erfahren Sie mehr über die verschiedenen Möglichkeiten, Geschäftsdaten aus Business Central freizugeben.'
author: jswymer
ms.topic: conceptual
ms.workload: na
ms.search.keywords: null
ms.date: 09/21/2022
ms.author: jswymer
---
# <a name="sharing-business-data-from-business-central" />Freigeben von Geschäftsdaten aus Business Central

Die Zusammenarbeit zwischen Personen innerhalb und außerhalb einer Organisation ist ein integraler Bestandteil der meisten Unternehmen. [!INCLUDE[prod_short](includes/prod_short.md)] bietet mehrere Funktionen zum Freigeben von Geschäftsdaten, wie eine Liste von Datensätzen, bestimmte Datensätze oder Dokumente. <!--, with others&mdash;even those people who don't have a Business Central license in some cases.-->

Bei all diesen Funktionen ist der Zugriff auf Daten durch die Lizenz und Berechtigungen von Business Central geschützt.

## <a name="copying-a-link" />Kopieren eines Links

![Unterstützt](media/check.png) Business Central Online ![Unterstützt](media/check.png) Business Central On-Premises

Sie können die URL der Seite von jeder Seite aus kopieren, dann einfügen und in anderen Medienformen wie E-Mails, Teams-Chats oder Textnachrichten verteilen. Am einfachsten kopieren Sie einen Link, indem Sie oben auf der Seite **Freigeben** > **Link kopieren** auswählen. Eine andere Möglichkeit besteht darin, die URL direkt aus dem Adressfeld des Browsers zu kopieren.

### <a name="modify-the-page-link" />Seitenlink ändern

Nachdem Sie einen Link kopiert haben, können Sie vor dem Senden die URL ändern, um die Anzeige beim Öffnen der Seite zu ändern. Sie können beispielsweise Filter hinzufügen oder ein anderes Unternehmen angeben.

Weitere Informationen finden Sie unter [Webclient-URL](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls).

### <a name="about-filtered-lists" />Informationen zu gefilterten Listen

Mithilfe des Filterbereichs auf Listenseiten können Sie Filter anwenden, um die in der Liste angezeigten Datensätze einzugrenzen. Wenn Sie die Aktion **Link kopieren** verwenden oder die URL aus dem Browser kopieren, enthält der Seitenlink Ihre Filteränderungen nicht. Benutzern, die den Link öffnen, wird die vollständige Sammlung angezeigt. Um die Filterung für einen Sammlungsseiten-Link beizubehalten, speichern Sie die gefilterte Seite zunächst als **Ansicht**. Dann öffnen Sie die Ansicht, und kopieren Sie den Link von dort.

Weitere Informationen finden Sie unter [Sortieren, Durchsuchen und Filtern](ui-enter-criteria-filters.md).

## <a name="sharing-to-teams" />Freigeben für Teams

![Unterstützt](media/check.png) Business Central Online ![Nicht unterstützt](media/x-icon.png) Business Central On-Premises

Von den meisten Sammlungsseiten und Detailseiten aus können Sie direkt einen Link zur Seite an Personen, Gruppenchats oder Kanäle senden. Geben Sie beispielsweise einen Link zu einer gefilterten Ansicht Ihrer Datensätze frei. Wenn Sie die [!INCLUDE[prod_short](includes/prod_short.md)] App für Teams installiert haben, wird der Link automatisch zu einer kompakten Karte erweitert, die Sie Ihrer Nachricht beifügen können. Die Empfänger wählen dann den Link oder die Karte aus, um die Seite in Business Central zu öffnen.

Weitere Informationen finden Sie unter [Freigeben von Datensätzen und Seitenlinks teilen in Teams](across-working-with-teams.md).

## <a name="sharing-through-onedrive" />Freigeben durch OneDrive

![Unterstützt](media/check.png) Business Central Online ![Unterstützt](media/check.png) Business Central On-Premises

Business Central macht es Ihnen leicht, Dateien zu speichern, zu verwalten und für andere Personen über OneDrive for Business freizugeben. Auf den meisten Seiten, auf denen Dateien verfügbar sind, wie z. B. dem Berichtseingang oder Dateien, die an Datensätze angehängt sind, finden Sie die Aktionen **In OneDrive öffnen** und **Freigeben**. Beide Aktionen speichern eine Kopie einer Datei in OneDrive. Wenn Sie sich in OneDrive befinden, können Sie dessen Freigabe- und Beitragsfunktionen für die Datei verwenden. Der Unterschied in den Aktionen besteht darin, dass **In OneDrive öffnen** die Datei in OneDrive öffnet. **Freigeben** öffnet eine Seite, auf der Sie auswählen können, für wen Sie die Datei freigeben möchten. Die Empfänger erhalten eine Benachrichtigungs-E-Mail für den Zugriff auf die Datei von Ihrem OneDrive.

Weitere Informationen finden Sie unter [Freigeben von Dateien in OneDrive](across-share-onedrive.md).

## <a name="opening-in-excel" />Öffnen in Excel

![Unterstützt](media/check.png) Business Central Online ![Unterstützt](media/check.png) Business Central On-Premises

Für Listenseiten und Listen, die in eine Seite eingebettet sind, können Sie die Aktion **In Excel öffnen** verwenden. Diese Aktion exportiert die Liste der Datensätze in eine Excel-Arbeitsmappe (.xlsx-Datei), die Sie für andere freigeben können. In der Arbeitsmappe können Sie auch die in Excel enthaltene Freigabefunktion verwenden.

Weitere Informationen finden Sie unter [Anzeigen und Bearbeiten in Excel](across-work-with-excel.md).

## <a name="sharing-rows-or-tables" />Freigeben von Zeilen oder Tabellen

![Unterstützt](media/check.png) Business Central Online ![Unterstützt](media/check.png) Business Central On-Premises

Sie können einen oder mehrere Datensätze in einer Liste freigeben. Wählen Sie einfach die Tastenkombination <kbd>Strg</kbd>+<kbd>C</kbd>, um sie in Ihre Zwischenablage zu kopieren. Fügen Sie dann die kopierten Elemente in eine andere Anwendung ein, indem Sie <kbd>Strg</kbd>+<kbd>V</kbd> drücken. Wenn Sie beispielsweise drei Verkaufsaufträge kopieren und in eine E-Mail einfügen, werden die Aufträge in einer formatierten Tabelle angezeigt.

Weitere Informationen finden Sie unter [FAQ zum Kopieren und Einfügen](faq-copy-paste.yml).

## <a name="see-also" />Weitere Informationen

[Business Central und OneDrive Integration](across-onedrive-overview.md)  
[Verwaltung der OneDrive Integration mit Business Central](admin-onedrive-integration.md)  
[OneDrive FAQ](admin-onedrive-faq.md)
