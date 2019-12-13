---
title: Ausgleichen und ändern Sie Einstellungen in gespeicherten Berichten | Microsoft Docs
description: Beschreibt vordefinierte Optionen und filtert, um einen Bericht anzupassen und die richtigen Daten zu generieren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: a9bb72a85fb49b4316af2160e5823fbf77a18cbf
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2881401"
---
# <a name="manage-saved-settings-for-reports-and-batch-jobs"></a>Gespeicherte Einstellungen für Berichte und Stapelaufträge verwalten
Abhängig vom ausgeführten Bericht, erhalten Benutzer in der Regel eine Seite, für die Sie bestimmte Optionen wählen und Filter festlegen können, um Daten zu ändern, die im erstellten Bericht enthalten sind. Dies ist die Berichtanfordearungsseite. Ein Bericht kann eine oder mehrere *Gespeicherte Einstellungen* enthalten, die Benutzer auf den Bericht von der Anforderungsseite anwenden können. *Gespeicherte Einstellungen* sind grundsätzlich vordefinierte Optionen und Filter. Die Verwendung von gespeicherten Einstellungen ist eine schnelle und zuverlässige Art, Berichte zu erstellen, die die richtigen Daten enthalten. Weitere Informationen finden Sie unter [Gespeicherte Einstellungen verwenden](ui-work-report.md#SavedSettings).

> [!NOTE]
> Dieses Thema bezieht sich hauptsächlich auf "Bericht", aber die gleichen Informationen gelten für Stapelverarbeitungen.

Wenn Sie die richtigen Berechtigungen haben, können Sie die gespeicherten Einstellungen für alle Berichte für alle Benutzer in einem Unternehmen anzeigen, erstellen und bearbeiten. Sie können gespeicherte Einstellungen für einen Bericht entweder den einzelnen Benutzern oder allen Benutzern im Unternehmen zuweisen.

<!--
## Apply saved settings to a report
1. Open the report.

   The request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="to-create-and-modify-saved-settings-for-all-users"></a>Um gespeicherter Einstellungen für alle Benutzer zu erstellen oder zu ändern
Sie können gespeicherte Einstellungen auf der Seite **Berichteinstellungen** verwalten. Es gibt zwei Möglichkeiten, dies Seite zu öffnen:
-   Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Berichtseinstellungen** ein, und wählen Sie dann den zugehörigen Link.
-   Öffnen Sie einen Bericht, wählen die Suche neben dem Feld **Verwendete Standardwerte verwenden aus** aus und wählen Sie **Aus vollständiger Liste auswählen** aus.

Die Seitendarstellungen zeigt alle gespeicherten Einstellungseingaben für alle Anwender an. Wenn es einen Benutzernamen im Feld **Zugewiesen zu** hat, kann nur der Benutzer die gespeicherten Einstellungen für den entsprechenden Bericht verwenden. Wenn sich ein Häkchen im Feld **Mit allen Benutzern teilen** befindet, können alle Benutzer die gespeicherten Einstellungen für den Bericht verwenden.

Von der Seite **Berichts-Einstellungen** können Sie:
-   Die Aktion **Neu** auswählen, um neue gespeicherte Einstellungen von Grund auf neu zu erstellen.
-   Wählen Sie einen Einstellungsposten aus der Liste aus, und wählen Sie die Aktion **Kopieren**, um eine Kopie zu erstellen.
-   Wählen Sie einen Einstellungsposten aus der Liste aus, und wählen Sie die Aktion **Bearbeiten**, um einen gespeicherten Einstellungsposten zu ändern.

> [!Important]
> Berücksichtigt den Namen, den Sie einem gespeicherten Einstellungsposten geben. Wenn Sie einen gespeicherten Einstellungsartikel für alle Benutzer erstellen und er denselben Namen wie bestehende gespeicherte Einstellungen für einen bestimmten Benutzer hat, ist dieser Benutzer nicht dazu in der Lage, die gespeicherten Einstellungen zu verwenden, die jedem zugeordnet sind.  Im Abschnitt **Gespeicherte Einstellungen** auf der Berichtsanforderungsseite werden dem Benutzer auch zwei Optionen gespeicherter Einstellungen mit demselben Namen angezeigt. Jedoch gleichgültig welche Option sie auswählen, werden die benutzerspezifischen gespeicherten Einstellungen verwendet.

> [!NOTE]
> Die gespeicherte Einstellungsfunktion in Berichten ist nur relevant, wenn die [SaveValues-Eigenschaft](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) der Anforderungsseite mit **Ja** festgelegt ist. Die **SaveValues**-Eigenschaft wird in der Entwicklungsumgebung festgelegt.  

## <a name="see-also"></a>Siehe auch
[Arbeiten mit Berichten, Batchaufträgen und XMLports](ui-work-report.md)  
