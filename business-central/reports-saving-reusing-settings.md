---
title: "Ausgleichen und ändern Sie Einstellungen in gespeicherten Berichten | Microsoft Docs"
description: Beschreibt vordefinierte Optionen und filtert, um einen Bericht anzupassen und die richtigen Daten zu generieren.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 9fd086831c0d145570d87c33c62a003c166aca87
ms.contentlocale: de-de
ms.lasthandoff: 11/22/2018

---
# <a name="managing-saved-settings-on-reports"></a>Gespeicherte Einstellungen in Berichtenn verwalten
Abhängig vom ausgeführten Bericht, erhalten Benutzer in der Regel eine Seite, für die Sie bestimmte Optionen festlegen und filtern können, um Daten zu ändern, die im erstellten Bericht enthalten sind. Diese Seite ist die Berichtanfordearungsseite. Ein Bericht kann eine oder mehrere *Gespeicherte Einstellungen* enthalten, die Benutzer auf den Bericht von der Anforderungsseite anwenden können. *Gespeicherte Einstellungen* sind grundsätzlich vordefinierte Optionen und Filter. Die Verwendung von gespeicherten Einstellungen ist eine schnelle und zuverlässige Art, Berichte zu erstellen, die die richtigen Daten enthalten. Weitere Informationen darüber, wie gespeicherte Einstellungen verwendet werden können, erfahren Sie unter [Gespeicherte Einstellungen nutzen](ui-work-report.md#SavedSettings).

Wenn Sie die richtigen Berechtigungen haben, können Sie die gespeicherten Einstellungen für alle Berichte für alle Benutzer im Unternehmen anzeigen, erstellen und bearbeiten. Sie können gespeicherte Einstellungen für einen Bericht den einzelnen Benutzern oder allen Benutzern im Unternehmen zuweisen.

<!-- 
## Apply saved settings to a report
1. Open the report.

   The report request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="create-and-modify-saved-settings-for-all-users"></a>Erstellen und Ändern gespeicherter Einstellungen für alle Benutzer
Sie können gespeicherte Einstellungen der Seite **1560 Berichteinstellungen** verwalten. Es gibt zwei Möglichkeiten, dies Seite zu öffnen:
-   Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Berichtseinstellungen** ein, und wählen dann den zugehörigen Link aus.
-   Öffnen Sie einen Bericht, wählen die Suche neben dem Feld **Verwendete Standardwerte aus:** aus, wählen Sie **Aus vollständiger Liste auswählen** aus.

Die Seitendarstellungen zeigt alle vorhandenen Abwehreinstellungsposten für alle Anwender an. Wenn es einen Benutzernamen in der Spalte **Zugewiesen zu** hat, kann nur der Benutzer die gespeicherten Einstellungen für den entsprechenden Bericht verwenden. Wenn sich ein Häkchen im Feld **Anteil mit allen Benutzern** befindet, können alle Benutzer die  gespeicherten Einstellungen für den Bericht verwenden.

Von der Seite **Berichts-Einstellungen** können Sie:
-   **Neu** auswählen, um neue gespeicherte Einstellungen von Grund auf neu zu erstellen.
-   Wählen Sie einen Einstellungsposten aus der Liste aus, und wählen Sie **Kopieren**, um eine Kopie zu erstellen.
-   Wählen Sie einen Einstellungsposten aus der Liste aus, und wählen Sie **Bearbeiten**, um einen gespeicherten Einstellungsposten zu ändern.


> [!Important]
> Berücksichtigt den Namen, den Sie einem gespeicherten Einstellungsposten geben. Wenn Sie einen gespeicherten Einstellungsartikel für alle Benutzer erstellen und er denselben Namen wie bestehende gespeicherte Einstellungen für einen bestimmten Benutzer hat, ist dieser Benutzer nicht dazu in der Lage, die gespeicherten Einstellungen zu verwenden, die jedem zugeordnet sind.  Im Feld **Gespeicherte Einstellungen** auf der Berichtsanforderungsseite werden dem Benutzer auch zwei Optionen gespeicherter Einstellungen mit demselben Namen angezeigt. Jedoch gleichgültig welche Option er auswählt, werden die benutzerspezifischen gespeicherten Einstellungen verwendet.

> [!NOTE]
> Die gespeicherte Einstellungsfunktion in Berichten ist nur relevant, wenn die [SaveValues-Eigenschaft](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property) der Anforderungsseite mit `Yes` festgelegt ist. Die **SaveValues**-Eigenschaft wird in der Entwicklungsumgebung festgelegt.  

## <a name="see-also"></a>Siehe auch
[Arbeiten mit Berichten](ui-work-report.md)  

