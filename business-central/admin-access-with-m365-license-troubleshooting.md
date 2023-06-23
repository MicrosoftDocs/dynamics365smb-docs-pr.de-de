---
title: Fehlerbehebung beim Zugriff mit Microsoft 365-Lizenzen
description: 'Erfahren Sie, wie Sie Probleme beim Zugriff auf Business Central mit nur einer Microsoft 365-Lizenz beheben können.'
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.topic: troubleshooting
ms.date: 02/07/2023
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
---

# <a name="troubleshoot-access-with-microsoft-365-licenses" />Fehlerbehebung beim Zugriff mit Microsoft 365-Lizenzen

## <a name="this-page-uses-data-from-related-tables-that-you-do-not-have-access-to-error-message" />Diese Seite verwendet Daten aus verwandten Tabellen, auf die Sie keinen Zugriff haben, Fehlermeldung

### <a name="symptoms" />Symptome

Beim Zugriff auf einen Datensatz in Teams wird Ihnen eine Fehlermeldung in einer Registerkarte oder Kartendetails ähnlich der folgenden angezeigt:

Diese Seite verwendet Daten aus verwandten Tabellen, auf die Sie keinen Zugriff haben. Wenden Sie sich an Ihren Administrator, um mit allen Funktionen dieser Seite zu arbeiten.“

### <a name="cause" />Grund

Höchstwahrscheinlich fehlen Ihnen Objektberechtigungen für Tabellen, auf die die aktuelle Seite oder der aktuelle Datensatz verweist.

## <a name="microsoft-365-access-has-been-enabled-but-users-get-a-permission-error" />Microsoft 365 Zugriff wurde aktiviert, aber Benutzer erhalten beim Zugriff auf einen Datensatz einen Berechtigungsfehler

### <a name="symptoms" />Symptome

Der Zugriff mit Microsoft 365 wurde im Business Central Admin Center aktiviert, aber Benutzer erhalten beim Zugriff auf einen Datensatz einen Berechtigungsfehler.

### <a name="cause" />Grund

Wenn Sie den Zugriff im Business Central Admin Center aktivieren, aber keine Berechtigungen auf der **Lizenzkonfigurationsseite** zuweisen, wird jedem, der versucht, auf Business Central-Datensätze in Teams zuzugreifen, sein Benutzerdatensatz ohne Berechtigung für Objekte bereitgestellt. Business Central ist von Natur aus sicher: Administratoren müssen zunächst konfigurieren, auf welche Daten in Teams zugegriffen werden kann. 

### <a name="resolution" />Lösung

Das Anpassen von Berechtigungen auf der Lizenzkonfigurationsseite wirkt sich nur auf neu erstellte Benutzer aus. Sie müssen die fehlenden Berechtigungen auch Benutzern zuweisen, die bereits über die Benutzerlistenseite erstellt wurden. 

## <a name="you-shared-a-link-in-teams-but-users-get-a-message-that-they-can-only-view-data" />Sie haben einen Link in Teams geteilt, aber Benutzer erhalten eine Meldung, dass sie nur Daten anzeigen können

### <a name="symptoms" />Symptome

Wenn ich einen Link in Teams als Business Central Benutzer freigebe, erhalten andere die Fehlermeldung „Beim Zugriff auf Business Central mit einer Microsoft 365-Lizenz können Sie nur Daten in Microsoft Teams anzeigen“.

### <a name="cause" />Grund

Wenn Sie einen Business Central-Link für Teams-Chats oder -Kanäle freigeben, wird durch das Navigieren eines Links immer aus Microsoft Teams heraus navigiert, wo die Daten nicht mehr zugänglich für eine Person sind, die eine Microsoft 365-Lizenz hat.

### <a name="resolution" />Lösung

Fügen Sie beim Teilen von Seiten oder Datensätzen entweder die Linkvorschau als Karte hinzu oder teilen Sie Daten als Registerkarte im Chat oder Kanal.

## <a name="card-from-shared-link-is-minimal-and-doesnt-include-details-button" />Die Karte vom freigegebenen Link ist minimal und enthält keine Detail-Schaltfläche

### <a name="symptoms" />Symptome

Wenn ein Microsoft 365 Lizenzinhaber ohne Business Central-Lizenz einen Business Central-Link in Teams teilt, wird dieser automatisch zu einer Karte erweitert, die keine nützlichen Informationen enthält und nur Business Central ohne die Schaltfläche **Details** anzeigt.

### <a name="cause" />Grund

Benutzer, die eine Microsoft 365 Lizenz, aber keine Business Central-Lizenz haben, dürfen Links nicht als Karten freigeben. Wenn der Benutzer die Business Central-App für Teams installiert hat und einen Link in den Erstellungsbereich einfügt, wird nur eine minimale Karte angezeigt. 

## <a name="see-also" />Siehe auch

[Business Central-Zugriff mit Microsoft 365-Lizenzen](admin-access-with-m365-license.md#minimum-requirements)  
[Zugriff mit Microsoft 365-Lizenzen festlegen](admin-access-with-m365-license-setup.md)  
[Integration von Business Central und Microsoft Teams](across-teams-overview.md)
[Gemeinsame Nutzung von Business Central-Datensätzen und Seitenlinks in Microsoft Teams](across-working-with-teams.md)  
[Problembehandlung der Teams-Integration](admin-teams-troubleshooting.md)  
