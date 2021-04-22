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
ms.date: 04/12/2021
ms.author: jswymer
ms.openlocfilehash: ecb3f88bf14c74f026f10fd49efe28f189036589
ms.sourcegitcommit: e13b80d4e5141f414109e660e0918eae561acb36
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882205"
---
# <a name="managing-microsoft-teams-integration-with-prod_short"></a>Verwalten der Microsoft Teams-Integration mit [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Dieser Artikel bietet einen Überblick darüber, was Sie als Administrator zur Steuerung der Microsoft Teams-Integration in [!INCLUDE [prod_short](includes/prod_short.md)] unternehmen können.

## <a name="in-microsoft-teams"></a>In Microsoft Teams

### <a name="minimum-requirements"></a>Mindestanforderungen

In diesem Abschnitt werden die Mindestanforderungen für die Verwendung der [!INCLUDE [prod_short](includes/prod_short.md)]-App-Funktionen in Teams beschrieben.

- Erforderliche Lizenzen

    Diese Tabelle gibt Ihnen einen Überblick über die Lizenzen, die für die Verwendung der [!INCLUDE [prod_short](includes/prod_short.md)]-App-Funktionen in Teams erforderlich sind.

    |Funktion|Teams-Lizenz|[!INCLUDE [prod_short](includes/prod_short.md)] Lizenz|
    |----|---|---|
    |Suchen Sie nach [!INCLUDE [prod_short](includes/prod_short.md)]-Kontakten.|![Häkchen](media/check.png "Aktivieren")|![Häkchen](media/check.png "Aktivieren")|
    |Einen Link zu einem [!INCLUDE [prod_short](includes/prod_short.md)]-Datensatz in eine Unterhaltung einfügen und ihn als Karte versenden.|![Häkchen](media/check.png "Aktivieren")|![Häkchen](media/check.png "Aktivieren")|
    |Eine Karte eines [!INCLUDE [prod_short](includes/prod_short.md)]-Datensatzes in einer Unterhaltung anzeigen.|![Häkchen](media/check.png "Aktivieren")||
    |Weitere Details für eine Karte eines [!INCLUDE [prod_short](includes/prod_short.md)]-Datensatzes in einer Unterhaltung anzeigen.|![Häkchen](media/check.png "Aktivieren")|![Häkchen](media/check.png "Aktivieren")|

- URL-Vorschau zulassen

    Die Richtlinieneinstellung **URL-Vorschau zulassen** muss aktiviert sein. Andernfalls kann keine Karte für [!INCLUDE [prod_short](includes/prod_short.md)] Links generiert werden, die in eine Teams-Unterhaltung eingefügt werden. Weitere Informationen zu dieser Einstellung finden Sie unter [Nachrichtenrichtlinien in Teams verwalten](/microsoftteams/messaging-policies-in-teams).

### <a name="managing-the-prod_short-app-optional"></a>Verwalten der [!INCLUDE [prod_short](includes/prod_short.md)] App (optional)

Als Teams-Administrator können Sie alle Apps für Ihre Organisation verwalten, einschließlich der [!INCLUDE [prod_short](includes/prod_short.md)]-App. Sie können die [!INCLUDE [prod_short](includes/prod_short.md)]-App für Ihr Unternehmen genehmigen oder installieren, die Installation der App durch Benutzer blockieren und vieles mehr.

Weitere Informationen finden Sie in den folgenden Artikeln in der Microsoft Teams-Dokumentation:

- [Ihre Apps im Microsoft Teams Admin Center verwalten](/MicrosoftTeams/manage-apps)
- [App-Einrichtungsrichtlinien in Microsoft Teams verwalten](/microsoftteams/teams-app-setup-policies)

## <a name="in-prod_short"></a>In [!INCLUDE [prod_short](includes/prod_short.md)]

### <a name="minimum-requirements"></a>Mindestanforderungen

- [!INCLUDE [prod_short](includes/prod_short.md)]-Version:

    [!INCLUDE [prod_short](includes/prod_short.md)] 2021 Veröffentlichungszyklus 1 oder höher. Die Teams-Integration wird nur für [!INCLUDE [prod_short](includes/prod_short.md)] Online unterstützt, nicht für On-Premises.

- Codeunit **2718 Seitenzusammenfassungsanbieter** wird als Webdienst veröffentlicht:

    Diese Codeunit wird standardmäßig als Webdienst veröffentlicht. Die Codeunit ist Teil der [!INCLUDE [prod_short](includes/prod_short.md)]-Systemanwendung. Sie wird verwendet, um die Felddaten für eine [!INCLUDE [prod_short](includes/prod_short.md)]-Seite abzurufen, die einer Teams-Unterhaltung hinzugefügt wurde. Weitere Informationen zum Veröffentlichen von Webdiensten finden Sie unter [Webdienst veröffentlichen](across-how-publish-web-service.md).

- <a name="permissions"></a>Benutzerberechtigungen:

    Die Kontaktsuche, Seiten und Daten, die Benutzer in einer Teams-Unterhaltung anzeigen und bearbeiten können, werden größtenteils durch deren Berechtigungen in [!INCLUDE [prod_short](includes/prod_short.md)] gesteuert.
    
    - Um nach Kontakten zu suchen, müssen Benutzer mindestens über Leseberechtigung zur Tabelle **Kontakte** verfügen. 
    - Um einen [!INCLUDE [prod_short](includes/prod_short.md)]-Link in eine Teams-Unterhaltung einzufügen und diesen zu einer Karte zu erweitern, müssen Benutzer mindestens über die Leseberechtigung für die Seite und ihre Daten verfügen.
    - Sobald eine Karte in eine Unterhaltung übermittelt wurde, kann jeder Benutzer in dieser Unterhaltung diese Karte ohne Berechtigungen für [!INCLUDE [prod_short](includes/prod_short.md)] anzeigen.
    - Um weitere Details für eine Karte anzuzeigen oder den Datensatz in [!INCLUDE [prod_short](includes/prod_short.md)] zu öffnen, müssen Benutzer über Leseberechtigung für die Seite und ihre Daten verfügen.
    - Um Daten zu ändern, benötigen Benutzer Änderungsberechtigungen.
    
    Weitere Informationen zu Berechtigungen finden Sie unter [Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md).

## <a name="managing-privacy-and-compliance"></a>Datenschutz und Compliance verwalten 

Microsoft Teams bietet umfassende Kontrollen für die Einhaltung und Verwaltung sensibler oder persönlich identifizierbarer Daten&mdash;einschließlich Daten, die von der [!INCLUDE [prod_short](includes/prod_short.md)] App zu Chats und Kanälen hinzugefügt wurde.

### <a name="understanding-where-prod_short-cards-are-stored"></a>Verstehen wo [!INCLUDE [prod_short](includes/prod_short.md)] Karten gespeichert werden 

Nachdem eine Karte an einen Chat gesendet wurde, werden die Karte und die auf der Karte angezeigten Felder in Teams kopiert. Diese Informationen unterliegen den Teamrichtlinien für Ihr Unternehmen, z. B. Richtlinien zur Aufbewahrung von Daten. Bei der Anzeige von Kartendetails werden keine Daten im Detailfenster in Teams gespeichert. Die Daten bleiben in [!INCLUDE [prod_short](includes/prod_short.md)] gespeichert und wird nur von Teams abgerufen, wenn der Benutzer die Details anzeigen möchte. 

- Weitere Informationen darüber, wo Teams diese Daten speichern, finden Sie unter [Speicherort der Daten in Microsoft Teams](/microsoftteams/location-of-data-in-teams).
- Weitere Informationen zu Aufbewahrungsrichtlinien in Teams finden Sie unter [Aufbewahrungsrichtlinien in Microsoft Teams](/microsoftteams/retention-policies).

### <a name="restricting-sharing-of-cards"></a>Beschränken des Kartenaustauschs 

Sie verhindern, dass bestimmte Benutzer oder Gruppen Karten an Chats oder Kanäle senden, indem Sie Nahrichten-Richtlinien einrichten, die die Einstellung **URL-Vorschau** deaktivieren. Weitere Informationen zu dieser Einstellung finden Sie unter [Nachrichtenrichtlinien in Teams verwalten](/microsoftteams/messaging-policies-in-teams). 

Sie können auch Informationssperren verwenden, um zu verhindern, dass Einzelpersonen oder Gruppen miteinander kommunizieren. Weitere Informationen finden Sie unter [Informationssperren in Microsoft Teams](/microsoftteams/information-barriers-in-teams).

Funktionen zur Verhinderung von Datenverlust im Microsoft 365 Security & Compliance Center können nicht speziell auf Karten angewendet werden. Sie können jedoch auf die Chat-Nachrichten angewendet werden, die die Karten enthalten. <!-- To track upcoming advanced features that include enabling DLP for cards, see [https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093](https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093).-->

### <a name="responding-to-data-requests"></a>Antworten auf Datenenanforderungen

Sie ermöglichen Teammitgliedern und Teambesitzern, Nachrichten mit vertraulichen Karten zu löschen, indem Sie Nachrichtenrichtlinien einrichten, wie **Besitzer können gesendete Nachrichten löschen** und **Benutzer können gesendete Nachrichten löschen**. Weitere Informationen zu dieser Einstellung finden Sie unter [Nachrichtenrichtlinien in Teams verwalten](/microsoftteams/messaging-policies-in-teams).

Inhaltssuche und eDiscovery Compliance-Funktinen im Microsoft 365 Security & Compliance Center können nicht auch auf Karten angewendet werden.

Weil Kartendaten in Teams eine Kopie der Daten in [!INCLUDE [prod_short](includes/prod_short.md)] sind, können Sie auch [!INCLUDE [prod_short](includes/prod_short.md)] Funktionen zum Exportieren der Kundendaten sofern erforderlich verwenden. Weitere Informationen zum Datenschutz in [!INCLUDE [prod_short](includes/prod_short.md)] finden Sie unter [FAQ zu Datenschutz für Business Central Debitoren](/dynamics365/business-central/dev-itpro/security/privacyfaq).

## <a name="see-also"></a>Siehe auch
[[!INCLUDE [prod_short](includes/prod_short.md)] und Microsoft Teams Integration Übersicht](across-teams-overview.md)  
[Die [!INCLUDE [prod_short](includes/prod_short.md)]-App für Microsoft Teams installieren](across-install-app-for-teams.md)  
[Teams FAQ](teams-faq.md)  
[Teams Problembehebung](admin-teams-troubleshooting.md)  
[Entwicklung für die Teams-Integration](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]