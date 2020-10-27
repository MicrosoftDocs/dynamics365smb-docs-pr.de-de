---
title: Verwalten der Microsoft Teams-Integration in Business Central | Microsoft Docs
description: Verwalten Sie die Business Central-Integration in Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: 3c04dfb2f77eba906b2567ca9438849e1cc20861
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989358"
---
# <a name="managing-microsoft-teams-integration-with-business-central"></a>Verwalten der Microsoft Teams-Integration in Business Central

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

Dieser Artikel bietet einen Überblick darüber, was Sie als Administrator zur Steuerung der Microsoft Teams-Integration in [!INCLUDE [prodshort](includes/prodshort.md)] unternehmen können.

## <a name="in-microsoft-teams"></a>In Microsoft Teams

### <a name="minimum-requirements"></a>Mindestanforderungen

In diesem Abschnitt werden die Mindestanforderungen für die Verwendung der [!INCLUDE [prodshort](includes/prodshort.md)]-App-Funktionen in Teams beschrieben.

- Erforderliche Lizenzen

    Diese Tabelle gibt Ihnen einen Überblick über die Lizenzen, die für die Verwendung der [!INCLUDE [prodshort](includes/prodshort.md)]-App-Funktionen in Teams erforderlich sind.

    |Funktion|Teams-Lizenz|Business Central-Lizenz|
    |----|---|---|
    |Einen Link zu einem [!INCLUDE [prodshort](includes/prodshort.md)]-Datensatz in eine Unterhaltung einfügen und ihn als Karte versenden.|![Häkchen](media/check.png "Aktivieren")|![Häkchen](media/check.png "Aktivieren")|
    |Eine Karte eines [!INCLUDE [prodshort](includes/prodshort.md)]-Datensatzes in einer Unterhaltung anzeigen.|![Häkchen](media/check.png "Aktivieren")||
    |Weitere Details für eine Karte eines [!INCLUDE [prodshort](includes/prodshort.md)]-Datensatzes in einer Unterhaltung anzeigen.|![Häkchen](media/check.png "Aktivieren")|![Häkchen](media/check.png "Aktivieren")|

- URL-Vorschau zulassen

    Die Richtlinieneinstellung **URL-Vorschau zulassen** muss aktiviert sein. Andernfalls kann keine Karte für Business Central-Links generiert werden, die in eine Teams-Unterhaltung eingefügt werden. Weitere Informationen zu dieser Einstellung finden Sie unter [Nachrichtenrichtlinien in Teams verwalten](/microsoftteams/messaging-policies-in-teams).

### <a name="managing-the-business-central-app-optional"></a>Verwalten der Business Central-App (optional)

Als Teams-Administrator können Sie alle Apps für Ihre Organisation verwalten, einschließlich der [!INCLUDE [prodshort](includes/prodshort.md)]-App. Sie können die [!INCLUDE [prodshort](includes/prodshort.md)]-App für Ihr Unternehmen genehmigen oder installieren, die Installation der App durch Benutzer blockieren und vieles mehr.

Weitere Informationen finden Sie in den folgenden Artikeln in der Microsoft Teams-Dokumentation:

- [Ihre Apps im Microsoft Teams Admin Center verwalten](https://docs.microsoft.com/MicrosoftTeams/manage-apps)
- [App-Einrichtungsrichtlinien in Microsoft Teams verwalten](https://docs.microsoft.com/microsoftteams/teams-app-setup-policies)

## <a name="in-prodshort"></a>In [!INCLUDE [prodshort](includes/prodshort.md)]

### <a name="minimum-requirements"></a>Mindestanforderungen

- [!INCLUDE [prodshort](includes/prodshort.md)]-Version:

    [!INCLUDE [prodshort](includes/prodshort.md)] 2020 Veröffentlichungzyklus 2 (Version 17) oder höher. Die Teams-Integration wird nur für [!INCLUDE [prodshort](includes/prodshort.md)] Online unterstützt, nicht für On-Premises.

- Codeunit **2718 Seitenzusammenfassungsanbieter** wird als Webdienst veröffentlicht:

    Diese Codeunit wird standardmäßig als Webdienst veröffentlicht. Die Codeunit ist Teil der [!INCLUDE [prodshort](includes/prodshort.md)]-Systemanwendung. Sie wird verwendet, um die Felddaten für eine [!INCLUDE [prodshort](includes/prodshort.md)]-Seite abzurufen, die einer Teams-Unterhaltung hinzugefügt wurde. 

- Benutzerberechtigungen:

    Die Seiten und Daten, die Benutzer in einer Teams-Unterhaltung anzeigen und bearbeiten können, werden größtenteils durch deren Berechtigungen in [!INCLUDE [prodshort](includes/prodshort.md)] gesteuert.
    
    - Um einen [!INCLUDE [prodshort](includes/prodshort.md)]-Link in eine Teams-Unterhaltung einzufügen und diesen zu einer Karte zu erweitern, müssen Benutzer mindestens über die Leseberechtigung für die Seite und ihre Daten verfügen.
    - Sobald eine Karte in eine Unterhaltung übermittelt wurde, kann jeder Benutzer in dieser Unterhaltung diese Karte ohne Berechtigungen für Business Central anzeigen.
    - Um weitere Details für eine Karte anzuzeigen oder den Datensatz in [!INCLUDE [prodshort](includes/prodshort.md)] zu öffnen, müssen Benutzer über Leseberechtigung für die Seite und ihre Daten verfügen.
    - Um Daten zu ändern, benötigen Benutzer Änderungsberechtigungen.
    
    Weitere Informationen zu Berechtigungen finden Sie unter [Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md).

## <a name="see-also"></a>Siehe auch
[Übersicht über die Integration von Business Central und Microsoft Teams](across-teams-overview.md)  
[Die [!INCLUDE [prodshort](includes/prodshort.md)]-App für Microsoft Teams installieren](across-install-app-for-teams.md)  
[Entwicklung für die Teams-Integration](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[Erste Schritte](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
