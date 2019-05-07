---
title: Überprüfen von Seiten in Business Central
description: Verwenden Sie die Seitenüberprüfungsfunktion, um Details zum Seitenentwurf und zur Datenquelle anzuzeigen. Der Seiteninspektor eignet sich ideal zum Beheben von Problemen mit Ihren Daten.
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: dynamics365-business-central
author: jswymer
ms.date: 04/01/2019
ms.openlocfilehash: eb9d4ec76c0dbbd59763f7622ca51137c9563a91
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2019
ms.locfileid: "969878"
---
# <a name="inspecting-pages-in-business-central"></a>Überprüfen von Seiten in Business Central

Die Überprüfungsfunktion der Seite ermöglicht es Ihnen, Details zu einer Seite abzurufen und bietet Einblick in den Seitenentwurf, die verschiedenen Elemente, aus denen die Seite besteht und die Quelle hinter den angezeigten Daten. Seitenüberprüfung ist besonders für Administratoren und Superuser, Support-Mitarbeiter und Entwickler gedacht. Es eignet sich ideal, um mehr über das Datenmodells hinter einer Seite zu erfahren, und für die Fehlerbehebung. Wenn Sie beispielsweise ein Problem mit einer Seite haben, können Sie mit der Seitenüberprüfung Informationen erhalten, die Sie an den Systemadministrator oder den Supportmitarbeiter weitergeben.

## <a name="working-with-page-inspection"></a>Arbeiten mit der Seitenüberprüfung

Zur Überprüfung einer Seite wählen Sie in der oberen rechten Ecke das ![Einstellungssymbol](media/ui-experience/settings_icon_small.png) und dann **Überprüfen** aus. Zudem besteht die Möglichkeit, die Tastenkombination **Strg+Alt+F1** zu verwenden.

Der Bereich **Seitenüberprüfung** wird auf der Seite geöffnet. Die folgende Abbildung zeigt den Bereich **Seitenüberprüfung** auf der Seite **Verkaufsauftrag**.

![Seitenüberprüfung](media/page-inspection-example.png)

Wenn der Bereich **Seitenüberprüfung** erstmaligen geöffnet wird, werden Informationen zum Hauptseitenobjekt angezeigt.

Verwenden Sie die Tastatur oder ein Zeigegerät, um den Fokus auf verschiedene Elemente der Seite zu verschieben. Wenn Sie eine Infobox oder einen Teil der Hauptseite auswählen, wird der umgebende Bereich von einen Rahmen markiert und der Bereich **Seitenüberprüfung** zeigt Informationen zum ausgewählten Element. Beispielsweise zeigt die vorherige Abbildung Informationen über den Listenanteil auf der Seite **Verkaufsauftrag** an. Wenn Sie zu anderen Seiten in der Anwendung navigieren, wird der Bereich **Seitenüberprüfung** dabei automatisch mit Seiteninformationen aktualisiert.

Weitere Informationen darüber, was in der Seitenüberprüfung angezeigt wird, finden Sie in [Überprüfung und Fehlerbehebung von Seiten](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-inspecting-pages) in der Hilfe für Business Central-Entwickler und IT-Profis.

Wenn die erwarteten Details im Bereich **Seitenüberprüfung** nicht angezeigt werden, verfügen Sie möglicherweise nicht über die erforderlichen Berechtigungen, wie im nächsten Abschnitt erläutert.

## <a name="controlling-access-to-page-inspection-details"></a>Steuern des Zugriffs auf Seitenüberprüfungsdetails

Als ein Administrator können Sie den Zugriff auf die gesamten Details steuern, die im Bereich **Seitenüberprüfung** angezeigt werden, indem Sie die Berechtigungen konfigurieren, die Benutzer haben. Um einem Benutzer Berechtigung für alle Details zu gewähren, geben Sie Benutzern die Berechtigung **Ausführen** im **System**-Objekt **5330**. Sie können diese Berechtigungen gewähren, indem Sie einen Berechtigungssatz (beispielsweise **D365 Troubleshoot**) oder eine Benutzergruppe (beispielsweise **D365 Troubleshoot**) verwenden. Weitere Informationen zu Berechtigungen finden Sie unter [Verwalten von Benutzern und Berechtigungen](ui-how-users-permissions.md).

Benutzer, die keine Berechtigungen in **Systemobjekt 5330** haben, können dennoch auf den Bereich **Seitenüberprüfung** zugreifen, sehen allerdings nur die Felder **Seite** und **Tabelle**, die grundlegende Details anzeigen, die sie an ihr Support Team weitergeben können.

## <a name="see-also"></a>Siehe auch

[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
