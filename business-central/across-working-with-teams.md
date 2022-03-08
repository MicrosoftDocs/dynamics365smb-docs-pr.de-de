---
title: Arbeiten mit Business Central-Daten in Microsoft Teams | Microsoft Docs
description: Erfahren Sie, wie Sie die Business Central-App für Microsoft Teams verwenden.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 01/20/2021
ms.author: jswymer
ms.openlocfilehash: 0f7c1e8016a1bc1915d7d6a54a183aa0e8cea2ea
ms.sourcegitcommit: 36a32c997b201ff32ed8c1cff8179b36e2468c47
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/22/2021
ms.locfileid: "5046454"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a>Arbeiten mit Business Central-Daten in Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]

[!INCLUDE [prod_short](includes/prod_short.md)] bietet eine App, die Microsoft Teams mit Ihren Geschäftsdaten in [!INCLUDE [prod_short](includes/prod_short.md)] verbindet. So können Sie schnell Daten zwischen Teammitgliedern austauschen und Anfragen schneller beantworten. In diesem Artikel erfahren Sie, wie Sie die App zum Teilen von [!INCLUDE [prod_short](includes/prod_short.md)]-Daten mit Mitarbeitern in einer Unterhaltung in Teams verwenden.

## <a name="overview"></a>Matrix

Mit der [!INCLUDE [prod_short](includes/prod_short.md)]-App können Sie Folgendes tun:

- Sie können einen Link zu einem beliebigen Business Central-Datensatz kopieren und ihn in eine Teams-Unterhaltung einfügen, um ihn dann mit Ihren Mitarbeitern zu teilen. Die App dann wird zu einem kompakten, interaktiven Link erweitert, auf dem Informationen zum Datensatz angezeigt werden.
- Wenn Sie sich in der Unterhaltung befinden, können Sie und Ihre Mitarbeiter weitere Details zum Datensatz anzeigen, Daten bearbeiten und Maßnahmen ergreifen&mdash;ohne Teams zu verlassen.

[![Teams-Integration in Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)

## <a name="prerequisites"></a>Voraussetzungen

- Sie haben Zugriff auf Microsoft Teams.
- Sie haben die [!INCLUDE [prod_short](includes/prod_short.md)]-App in Teams installiert. Weitere Informationen finden Sie unter [Die [!INCLUDE [prod_short](includes/prod_short.md)]-App für Microsoft Teams installieren](across-install-app-for-teams.md).

> [!NOTE]
> Alle Teilnehmer einer Teams-Unterhaltung können Karten für Business Central-Datensätze anzeigen, die Sie an die Unterhaltung senden. Um weitere Details zu Datensätzen anzuzeigen (durch Verwenden der Schaltflächen **Details** oder **Pop-out** auf einer Karte), benötigen diese jedoch Zugriff auf [!INCLUDE [prod_short](includes/prod_short.md)]. Weitere Informationen finden Sie unter [Verwalten der Microsoft Teams-Integration](admin-teams-integration.md#minimum-requirements-1).

## <a name="include-a-business-central-card-in-a-teams-conversation"></a>Eine Business Central-Karte in eine Teams-Unterhaltung einfügen

1. Verwenden Sie Ihren Browser, um sich bei [!INCLUDE [prod_short](includes/prod_short.md)] anzumelden.
2. Öffnen Sie den Datensatz, den Sie teilen möchten.

    Die App dient zum Anzeigen von Kartenseiten aus [!INCLUDE [prod_short](includes/prod_short.md)]. Öffnen Sie daher eine Seite, auf der ein einzelner Datensatz angezeigt wird, z. B. ein Artikel, ein Kunde oder ein Verkaufsauftrag. Sie können sie nicht für Rollencenter oder Seiten verwenden, auf denen mehrere Datensätze in einer Liste angezeigt werden.

3. Kopieren Sie die gesamte URL aus der Adressleiste des Browsers.

   ![Die Business Central-URL aus dem Browser kopieren](media/teams-url-v2.png)
4. Wechseln Sie zu Teams und beginnen Sie eine Unterhaltung, die mit einer Person, einer Personengruppe oder einem Teamkanal geführt werden kann.

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. Fügen Sie die URL in das Feld Nachrichten ein, in dem Sie die Nachricht erstellen.

   ![Business Central-URL in Teams einfügen](media/teams-paste-url-v2.png)
6. Wenn Sie zum ersten Mal einen Link in eine Unterhaltung einfügen, werden Sie aufgefordert, sich bei [!INCLUDE [prod_short](includes/prod_short.md)] anzumelden und der App die Zustimmung zum Datenabruf zu geben. Folgen Sie einfach den Anweisungen auf dem Bildschirm.

    > [!NOTE]
    > Sie müssen diesen Schritt nur einmal ausführen.

7. Warten Sie einen Moment, während eine Karte im Nachrichtenfeld generiert wird.

8. Wenn die Karte angezeigt wird, überprüfen Sie den Inhalt der Karte sorgfältig auf sensible Informationen, bevor Sie die Nachricht senden. Dieser Schritt ist wichtig, da nach dem Senden der Nachricht jeder Unterhaltungsteilnehmer die Karte sehen kann.

9. Wenn Sie mit der Karte zufrieden sind, wählen Sie **Senden** aus, um sie der Unterhaltung hinzuzufügen.

    > [!TIP]
    > Nachdem die Karte angezeigt wird und bevor Sie **Senden** auswählen, können Sie die eingefügte URL bei Bedarf löschen.

10. Um weitere Details anzuzeigen oder Änderungen an der Karte vorzunehmen, wählen Sie **Details** aus. Weitere Informationen finden Sie im nächsten Abschnitt.

## <a name="view-card-details"></a>Kartendetails anzeigen

Sobald eine Karte an ein Gespräch gesendet wurde, können alle Teilnehmer mit den [ordnungsgemäßen Berechtigungen](admin-teams-integration.md#permissions) **Einzelheiten** auswählen, um ein Fenster zu öffnen, in dem weitere Informationen zum Datensatz angezeigt werden&mdash; und möglicherweise Änderungen am Datensatz vornehmen. Es spielt keine Rolle, ob Sie die Karte senden oder die Karte empfangen. Die Funktion **Details** ist besonders für Empfänger nützlich, da sie ihnen schnell präzise und zielgerichtete Informationen über den Datensatz liefert, anstatt den gesamten Datensatz scannen zu müssen.

Das Detailfenster ähnelt der Seite, die im [!INCLUDE [prod_short](includes/prod_short.md)] Datensatz angezeigt wird. Sie ist für Teams jedoch ein wenig gekürzt. Wenn Sie mit dem Anzeigen und Vornehmen von Änderungen fertig sind, schließen Sie das Fenster, um zur Unterhaltung in Teams zurückzukehren.

Hier sind einige Dinge zu beachten, wenn Sie mit den Kartendetails arbeiten:

- Um weitere Details für eine Karte anzuzeigen oder den Datensatz in [!INCLUDE [prod_short](includes/prod_short.md)] zu öffnen, müssen Benutzer über Leseberechtigung für die Seite und ihre Daten verfügen.
- Karten in Team-Chats werden nicht automatisch auf Änderungen aktualisiert. Alle Änderungen, die Sie an einem Datensatz im Detailfenster speichern, werden in [!INCLUDE [prod_short](includes/prod_short.md)] gespeichert. Auf der Karte in Teams werden die Änderungen in der Konvertierung jedoch erst angezeigt, wenn Sie den Link erneut einfügen.

Weitere Informationen zum Arbeiten mit Karten und Kartendetails finden Sie unter [Teams FAQ](teams-faq.md).

## <a name="see-also"></a>Siehe auch

[Übersicht über die Integration von Business Central und Microsoft Teams](across-teams-overview.md)  
[Die [!INCLUDE [prod_short](includes/prod_short.md)]-App für Microsoft Teams installieren](across-install-app-for-teams.md)  
[Teams FAQ](teams-faq.md)  
[Teams Problembehebung](admin-teams-troubleshooting.md)  
[Entwicklung für die Teams-Integration](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  
