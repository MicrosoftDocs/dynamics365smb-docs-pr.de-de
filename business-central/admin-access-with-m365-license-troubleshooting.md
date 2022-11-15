---
title: Fehlerbehebung beim Zugriff mit Microsoft 365-Lizenzen
description: Erfahren Sie, wie Sie Probleme beim Zugriff auf Business Central mit nur einer Microsoft 365-Lizenz beheben können.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: troubleshooting
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams
ms.openlocfilehash: 750a78eb32568bea07d6851ff69c0b2cfea3ab49
ms.sourcegitcommit: 61fdaded30310ba8bdf95f99e76335372f583642
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2022
ms.locfileid: "9744992"
---
# <a name="troubleshoot-access-with-microsoft-365-licenses"></a>Fehlerbehebung beim Zugriff mit Microsoft 365-Lizenzen

## <a name="symptoms"></a>Symptome

Beim Zugriff auf einen Datensatz in Teams wird Ihnen eine Fehlermeldung in einer Registerkarte oder Kartendetails ähnlich der folgenden angezeigt:

„Diese Seite verwendet Daten aus verwandten Tabellen, auf die Sie keinen Zugriff haben. Wenden Sie sich an Ihren Administrator, um mit allen Funktionen dieser Seite zu arbeiten.“

## <a name="cause"></a>Grund

Höchstwahrscheinlich fehlen Ihnen Objektberechtigungen für Tabellen, auf die die aktuelle Seite oder der aktuelle Datensatz verweist.

## <a name="symptoms"></a>Symptome

Der Zugriff wurde aktiviert, aber Benutzer erhalten beim Zugriff auf einen Datensatz einen Berechtigungsfehler.

## <a name="cause"></a>Grund

Wenn Sie den Zugriff im Business Central Admin Center aktivieren, aber keine Berechtigungen auf der Lizenzkonfigurationsseite zuweisen, wird jedem, der versucht, auf Business Central-Datensätze in Teams zuzugreifen, sein Benutzerdatensatz ohne Berechtigung für Objekte bereitgestellt. Business Central ist von Natur aus sicher: Administratoren müssen zunächst konfigurieren, auf welche Daten in Teams zugegriffen werden kann. 

## <a name="resolution"></a>Lösung

Das Anpassen von Berechtigungen auf der Lizenzkonfigurationsseite wirkt sich nur auf neu erstellte Benutzer aus. Sie müssen die fehlenden Berechtigungen auch Benutzern zuweisen, die bereits über die Benutzerlistenseite erstellt wurden. 

## <a name="symptoms"></a>Symptome

Wenn ich einen Link in Teams freigebe, erhalten andere die Fehlermeldung „Beim Zugriff auf Business Central mit einer Microsoft 365-Lizenz können Sie nur Daten in Microsoft Teams anzeigen“.

## <a name="cause"></a>Grund

Wenn Sie einen Business Central-Link für Teams-Chats oder -Kanäle freigeben, wird durch das Navigieren eines Links immer aus Microsoft Teams heraus navigiert, wo die Daten nicht mehr zugänglich für eine Person sind, die eine Microsoft 365-Lizenz hat.

## <a name="resolution"></a>Lösung

Fügen Sie beim Teilen von Seiten oder Datensätzen entweder die Linkvorschau als Karte hinzu oder teilen Sie Daten als Registerkarte im Chat oder Kanal.

## <a name="see-also"></a>Siehe auch

[Business Central-Zugriff mit Microsoft 365-Lizenzen](admin-access-with-m365-license.md#minimum-requirements)  
[Zugriff mit Microsoft 365-Lizenzen einrichten](admin-access-with-m365-license-setup.md)  
[Integration von Business Central und Microsoft Teams](across-teams-overview.md)
[Gemeinsame Nutzung von Business Central-Datensätzen und Seitenlinks in Microsoft Teams](across-working-with-teams.md)  
[Problembehandlung der Teams-Integration](admin-teams-troubleshooting.md)  