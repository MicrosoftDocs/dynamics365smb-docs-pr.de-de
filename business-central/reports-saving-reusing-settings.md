---
title: Gespeicherte Einstellungen für Berichte und Stapelaufträge verwalten
description: Beschreibt, wie der Admin vordefinierte Optionen und Filter für einen Bericht festlegen und diese Einstellungen für einen oder alle Benutzer freigeben kann.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 12/21/2021
ms.author: edupont
ms.openlocfilehash: 901f3899ef164d3d24dbc5c4e2226b840c97c945
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8522642"
---
# <a name="manage-saved-settings-for-reports-and-batch-jobs"></a>Gespeicherte Einstellungen für Berichte und Batch-Aufträge verwalten

Abhängig vom ausgeführten Bericht, erhalten Benutzer in der Regel eine Seite, für die Sie bestimmte Optionen wählen und Filter festlegen können, um Daten zu ändern, die im erstellten Bericht enthalten sind. Diese Seite wird als *Anforderungsseite* bezeichnet. Ein Bericht kann eine oder mehrere *Gespeicherte Einstellungen* enthalten, die Benutzer auf den Bericht von der Anforderungsseite anwenden können. *Gespeicherte Einstellungen* sind grundsätzlich vordefinierte Optionen und Filter. Die Verwendung von gespeicherten Einstellungen ist eine schnelle und zuverlässige Art, Berichte zu erstellen, die die richtigen Daten enthalten. Weitere Informationen finden Sie unter [Gespeicherte Einstellungen verwenden](ui-work-report.md#SavedSettings).

> [!NOTE]
> Dieses Thema bezieht sich auf *Berichte*, aber ähnliche Informationen gelten auch für *Batch-Aufträge*.

Wenn Sie die richtigen Berechtigungen haben, können Sie die gespeicherten Einstellungen für alle Berichte für alle Benutzer in einem Unternehmen anzeigen, erstellen und bearbeiten. Sie können gespeicherte Einstellungen für einen Bericht entweder den einzelnen Benutzern oder allen Benutzern im Unternehmen zuweisen.

## <a name="manage-saved-settings"></a>Gespeicherte Einstellungen verwalten

Sie können gespeicherte Einstellungen auf der Seite **Berichteinstellungen** verwalten. Es gibt zwei Möglichkeiten, dies Seite zu öffnen:

- Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Berichtseinstellungen** ein, und wählen Sie dann den entsprechenden Link.
- Wählen Sie auf der Anforderungsseite eines Berichts das Suchfeld im Feld **Standardwerte verwenden von** und wählen Sie dann die Aktion **Aus der vollständigen Liste auswählen**.

    Dieses Feld ist nur sichtbar, wenn Sie den Bericht zuvor mindestens einmal ausgeführt haben. In der Liste werden nur Einstellungen angezeigt, die Ihnen zur Verfügung stehen, entweder weil es sich um Ihre eigenen Einstellungen handelt oder weil die Einstellungen für Sie freigegeben sind.

Die Seite **Berichtseinstellungen** zeigt alle vorhandenen gespeicherten Einstellungseinträge für alle Benutzer an. Wenn es einen Benutzernamen im Feld **Zugewiesen zu** hat, kann nur der Benutzer die gespeicherten Einstellungen für den entsprechenden Bericht verwenden. Wenn sich ein Häkchen im Feld **Mit allen Benutzern teilen** befindet, können alle Benutzer die gespeicherten Einstellungen für den Bericht verwenden.  

> [!TIP]
> Wenn ein Benutzer einen Bericht ausgeführt hat, der gemeinsame Einstellungen unterstützt, werden seine Einstellungen gespeichert und zu dieser Liste hinzugefügt. In den meisten Fällen kann der Admin diese Einstellungen dann bearbeiten und festlegen, dass die Einstellungen für alle Benutzer freigegeben werden sollen.
>
> In einigen Fällen können die Einstellungen jedoch nicht gemeinsam genutzt werden, und der Admin kann sie auch nicht ändern. Die meisten Batchaufträge unterstützen keine gemeinsamen Einstellungen.  

## <a name="create-or-modify-saved-settings-for-all-users"></a>Gespeicherte Einstellungen für alle Benutzer erstellen oder ändern

Von der Seite **Berichts-Einstellungen** können Sie:

- Die Aktion **Neu** auswählen, um neue gespeicherte Einstellungen von Grund auf neu zu erstellen.
- Wählen Sie einen Einstellungsposten aus der Liste aus, und wählen Sie die Aktion **Kopieren**, um eine Kopie zu erstellen.
- Wählen Sie einen Einstellungsposten aus der Liste aus, und wählen Sie die Aktion **Bearbeiten**, um einen gespeicherten Einstellungsposten zu ändern.

> [!Important]
> Berücksichtigt den Namen, den Sie einem gespeicherten Einstellungsposten geben. Wenn Sie einen gespeicherten Einstellungsartikel für alle Benutzer erstellen und er denselben Namen wie bestehende gespeicherte Einstellungen für einen bestimmten Benutzer hat, ist dieser Benutzer nicht dazu in der Lage, die gespeicherten Einstellungen zu verwenden, die jedem zugeordnet sind.  Im Abschnitt **Gespeicherte Einstellungen** auf der Berichtsanforderungsseite werden dem Benutzer auch zwei Optionen gespeicherter Einstellungen mit demselben Namen angezeigt. Jedoch gleichgültig welche Option sie auswählen, werden die benutzerspezifischen gespeicherten Einstellungen verwendet.

> [!NOTE]
> Die Möglichkeit, Einstellungen zu speichern, ist nur bei Berichten verfügbar, bei denen die Eigenschaft [SaveValues](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) auf der Anforderungsseite des Berichts auf **Ja** festgelegt ist. Die Eigenschaft **SaveValues** wird vom Entwickler festgelegt.  

## <a name="see-also"></a>Weitere Informationen

[Arbeiten mit Berichten, Batchaufträgen und XMLports](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]