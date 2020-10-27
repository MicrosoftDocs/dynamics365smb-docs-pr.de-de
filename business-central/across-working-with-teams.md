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
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: fbe024f724f018aae6d3aeb5251281bf4c3bfbde
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989421"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a>Arbeiten mit Business Central-Daten in Microsoft Teams

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

[!INCLUDE [prodshort](includes/prodshort.md)] bietet eine App, die Microsoft Teams mit Ihren Geschäftsdaten in [!INCLUDE [prodshort](includes/prodshort.md)] verbindet. So können Sie schnell Daten zwischen Teammitgliedern austauschen und Anfragen schneller beantworten. In diesem Artikel erfahren Sie, wie Sie die App zum Teilen von [!INCLUDE [prodshort](includes/prodshort.md)]-Daten mit Mitarbeitern in einer Unterhaltung in Teams verwenden.

## <a name="overview"></a>Matrix

Mit der [!INCLUDE [prodshort](includes/prodshort.md)]-App können Sie Folgendes tun:

- Sie können einen Link zu einem beliebigen Business Central-Datensatz kopieren und ihn in eine Teams-Unterhaltung einfügen, um ihn mit Ihren Mitarbeitern zu teilen. Der Link wird zu einer kompakten, interaktiven Karte erweitert, auf der Informationen zum Datensatz angezeigt werden.
- Wenn Sie sich in der Unterhaltung befinden, können Sie und Ihre Mitarbeiter weitere Details zum Datensatz anzeigen, Daten bearbeiten und Maßnahmen ergreifen – ohne Teams zu verlassen.

[![Teams-Integration in Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)

## <a name="prerequisites"></a>Voraussetzungen

- Sie haben Zugriff auf Microsoft Teams.
- Sie haben die [!INCLUDE [prodshort](includes/prodshort.md)]-App in Teams installiert. Weitere Informationen finden Sie unter [Die [!INCLUDE [prodshort](includes/prodshort.md)]-App für Microsoft Teams installieren](across-install-app-for-teams.md).

> [!NOTE]
> Alle Teilnehmer einer Teams-Unterhaltung können Karten für Business Central-Datensätze anzeigen, die Sie an die Unterhaltung senden. Um weitere Details zu Datensätzen anzuzeigen (durch Verwenden der Schaltflächen **Details** oder **Pop-out** auf einer Karte), benötigen diese jedoch Zugriff auf [!INCLUDE [prodshort](includes/prodshort.md)]. Weitere Informationen finden Sie unter [Verwalten der Microsoft Teams-Integration](admin-teams-integration.md#minimum-requirements-1).
<!--
- People You and your coworkers have the following permissions in [!INCLUDE [prodshort](includes/prodshort.md)]
  - To paste a [!INCLUDE [prodshort](includes/prodshort.md)] link into a Teams conversation and have it expand into a card, you have to have at least permission to view the page and its data.
  - Once a card is submitted into a conversation, any user in that conversation can view that card without having permission to Business Central.
  - For other users to view more details from card, they must also have view permission, as a minimum, to the page and its data. If they want to change data, they'll need modify permissions.

  Setting up permissions is typically done by an administrator. For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md).-->

## <a name="include-a-business-central-card-in-a-teams-conversation"></a>Eine Business Central-Karte in eine Teams-Unterhaltung einfügen

1. Verwenden Sie Ihren Browser, um sich bei [!INCLUDE [prodshort](includes/prodshort.md)] anzumelden.
2. Öffnen Sie den Datensatz, den Sie teilen möchten.

    Die App dient zum Anzeigen von Kartenseiten aus [!INCLUDE [prodshort](includes/prodshort.md)]. Öffnen Sie daher eine Seite, auf der ein einzelner Datensatz angezeigt wird, z. B. ein Artikel, ein Kunde oder ein Verkaufsauftrag. Sie können sie nicht für Rollencenter oder Seiten verwenden, auf denen mehrere Datensätze in einer Liste angezeigt werden.

3. Kopieren Sie die gesamte URL aus der Adressleiste des Browsers.

   ![Die Business Central-URL aus dem Browser kopieren](media/teams-url.png)
4. Wechseln Sie zu Teams und beginnen Sie eine Unterhaltung, die mit einer Person, einer Personengruppe oder einem Teamkanal geführt werden kann.

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. Fügen Sie die URL in das Feld ein, in das Sie Nachrichten einfügen.

   ![Business Central-URL in Teams einfügen](media/teams-paste-url.png)
6. Wenn Sie zum ersten Mal einen Link in eine Unterhaltung einfügen, werden Sie aufgefordert, sich bei [!INCLUDE [prodshort](includes/prodshort.md)] anzumelden und der App die Zustimmung zum Datenabruf zu geben. Folgen Sie einfach den Anweisungen auf dem Bildschirm.

    > [!NOTE]
    > Sie müssen diesen Schritt nur einmal ausführen.

7. Warten Sie einen Moment, während eine Karte im Nachrichtenfeld generiert wird.

8. Wenn die Karte angezeigt wird, überprüfen Sie den Inhalt der Karte sorgfältig auf sensible Informationen, bevor Sie die Nachricht senden. Dieser Schritt ist wichtig, da nach dem Senden der Nachricht jeder Unterhaltungsteilnehmer die Karte sehen kann.

9. Wenn Sie mit der Karte zufrieden sind, wählen Sie **Senden** aus, um sie der Unterhaltung hinzuzufügen.

    > [!TIP]
    > Nachdem die Karte angezeigt wird und bevor Sie **Senden** auswählen, können Sie die eingefügte URL bei Bedarf löschen.

10. Um weitere Details anzuzeigen oder Änderungen am Datensatz vorzunehmen, wählen Sie **Details** aus.

    Die Detailseite ähnelt der Seite, die in [!INCLUDE [prodshort](includes/prodshort.md)] angezeigt wird. Sie ist für Teams jedoch ein wenig gekürzt. Wenn Sie mit dem Anzeigen und Vornehmen von Änderungen fertig sind, schließen Sie das Fenster, um zur Unterhaltung in Teams zurückzukehren.

    > [!NOTE]
    > Alle von Ihnen vorgenommenen Änderungen werden erst dann auf der Karte angezeigt, wenn Sie ihren Link beim nächsten Mal in eine Unterhaltung einfügen.

## <a name="see-also"></a>Siehe auch

[Übersicht über die Integration von Business Central und Microsoft Teams](across-teams-overview.md)  
[Die [!INCLUDE [prodshort](includes/prodshort.md)]-App für Microsoft Teams installieren](across-install-app-for-teams.md)  
[Entwicklung für die Teams-Integration](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[Erste Schritte](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
