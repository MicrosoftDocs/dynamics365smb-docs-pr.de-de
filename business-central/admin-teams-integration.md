---
title: Verwalten der Microsoft Teams-Integration in Business Central | Microsoft Docs
description: Verwalten Sie die Business Central-Integration in Microsoft Teams.
author: jswymer
ms.topic: overview
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork'
ms.date: 02/03/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="managing-microsoft-teams-integration-with-"></a>Verwalten der Microsoft Teams-Integration mit [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Dieser Artikel bietet einen Überblick darüber, was Sie als Administrator zur Steuerung der Microsoft Teams-Integration in [!INCLUDE [prod_short](includes/prod_short.md)] unternehmen können.

## <a name="in-microsoft-teams"></a>In Microsoft Teams

### <a name="minimum-requirements"></a>Mindestanforderungen

In diesem Abschnitt werden die Mindestanforderungen für die Verwendung der [!INCLUDE [prod_short](includes/prod_short.md)]-App-Funktionen in Teams beschrieben.

- Erforderliche Lizenzen

    Die [!INCLUDE[prod_short](includes/prod_short.md)]-App erfordert eine Teams-Lizenz über ein Microsoft 365 Business- oder Enterprise-Abonnement. Eigenständige Teams-Abonnements wie Microsoft Teams (kostenlos) oder Microsoft Teams Essentials werden nicht unterstützt.

    Die meisten Funktionen der [!INCLUDE[prod_short](includes/prod_short.md)]-App für Teams erfordern außerdem eine [!INCLUDE [prod_short](includes/prod_short.md)]-Lizenz, wie in der folgenden Tabelle gezeigt.

    |Funktion|[!INCLUDE [prod_short](includes/prod_short.md)] Lizenz|
    |----|---|
    |Suchen Sie nach [!INCLUDE [prod_short](includes/prod_short.md)]-Kontakten.|![Häkchen](media/check.png "Aktivieren")|
    |Einen Link zu einem [!INCLUDE [prod_short](includes/prod_short.md)]-Datensatz in eine Unterhaltung einfügen und ihn als Karte versenden.|![Häkchen](media/check.png "Aktivieren")|
    |Geben Sie einen Link von einer Seite in [!INCLUDE [prod_short](includes/prod_short.md)] an die Teams Unterhaltung weiter.|![Häkchen](media/check.png "Aktivieren")|
    |Eine Karte eines [!INCLUDE [prod_short](includes/prod_short.md)]-Datensatzes in einer Unterhaltung anzeigen.||
    |Weitere Details für eine Karte eines [!INCLUDE [prod_short](includes/prod_short.md)]-Datensatzes in einer Unterhaltung anzeigen.|![Häkchen](media/check.png "Aktivieren")|
    |Öffnen Sie einen Seitenlink in [!INCLUDE [prod_short](includes/prod_short.md)] aus einer Unterhaltung heraus.|![Häkchen](media/check.png "Aktivieren")|

- URL-Vorschau zulassen

    Die Richtlinieneinstellung **URL-Vorschau zulassen** muss aktiviert sein. Andernfalls kann keine Karte für [!INCLUDE [prod_short](includes/prod_short.md)] Links generiert werden, die in eine Teams-Unterhaltung eingefügt werden. Weitere Informationen zu dieser Einstellung finden Sie unter [Nachrichtenrichtlinien in Teams verwalten](/microsoftteams/messaging-policies-in-teams).

### <a name="managing-the--app-optional"></a>Verwalten der [!INCLUDE [prod_short](includes/prod_short.md)] App (optional)

Als Teams-Administrator können Sie alle Apps für Ihre Organisation verwalten, einschließlich der [!INCLUDE [prod_short](includes/prod_short.md)]-App. Sie können die [!INCLUDE [prod_short](includes/prod_short.md)]-App für Ihr Unternehmen genehmigen oder installieren, die Installation der App durch Benutzer blockieren und vieles mehr.

Weitere Informationen finden Sie in den folgenden Artikeln in der Microsoft Teams-Dokumentation:

- [Ihre Apps im Microsoft Teams Admin Center verwalten](/MicrosoftTeams/manage-apps)
- [App-Einrichtungsrichtlinien in Microsoft Teams verwalten](/microsoftteams/teams-app-setup-policies)

## <a name="in-"></a>In [!INCLUDE [prod_short](includes/prod_short.md)]

### <a name="minimum-requirements-1"></a>Mindestanforderungen

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

## <a name="installing-the-business-central-app-by-using-centralized-deployment"></a>Installieren der Business Central-App mit Hilfe der zentralen Bereitstellung

Im Admin Center Microsoft Teams konfigurieren Sie die Richtlinien für die Einrichtung der Apps von Teams für das Unternehmen. Im Admin Center von Teams können Sie die Funktion Zentrale Bereitstellung verwenden, um die Business Central-App in Teams automatisch für alle Benutzer in Ihrem Unternehmen, für bestimmte Gruppen oder für einzelne Benutzer bereitzustellen.

> [!NOTE]
> Um die zentralisierte Bereitstellung einzurichten, muss Ihr Teams-Konto mindestens über die Rolle [Teams-Administrator](/entra/identity/role-based-access-control/permissions-reference#teams-Administrator] verfügen.

1. Wählen Sie in Business Central die ![Lupe, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?"). Symbol, geben Sie **Teams App Zentrale Bereitstellung** ein und wählen Sie dann den entsprechenden Link. Oder wählen Sie [hier](https://businesscentral.dynamics.com/?page=1833), um die Seite direkt zu öffnen.
2. Lesen Sie die Informationen auf der Seite **Einrichten der Business Central-App für Teams** und wählen Sie dann **Weiter**, wenn Sie bereit sind.
3. Öffnen Sie das [Teams Admin Center](https://go.microsoft.com/fwlink/?linkid=2163970) und führen Sie die folgenden Schritte aus.
    1. Gehen Sie zu **Teams Apps** > **Richtlinien einrichten**.
    2. Erstellen Sie eine neue Richtlinie oder wählen Sie die Richtlinie aus, die Sie für die Installation der Business Central-App verwenden möchten, und wählen Sie dann **Apps hinzufügen**.
    3. Suchen Sie auf der Seite **Installierte Apps hinzufügen** nach **Business Central** und wählen Sie diese aus.
    4. Wählen Sie **Hinzufügen**.

       Business Central sollte nun unter **Installierte Apps** für die Richtlinie erscheinen.
    5. Konfigurieren Sie weitere Einstellungen und wählen Sie dann **Speichern**.

    Weitere Informationen über Richtlinien zur Einrichtung von Apps in Teams finden Sie unter [Verwalten von Richtlinien zur Einrichtung von Apps in Microsoft Teams](/MicrosoftTeams/teams-app-setup-policies) in der Dokumentation zu Teams.
4. Gehen Sie zurück zu **Teams App Zentrale Bereitstellung** in Business Central und wählen Sie **Fertig**.

> [!IMPORTANT]
> Es kann bis zu 24 Stunden dauern, bis die Richtlinie für die Einrichtung der App festgelegt ist und die App den Benutzern bereitgestellt wird.

## <a name="managing-privacy-and-compliance"></a>Datenschutz und Compliance verwalten

Microsoft Teams bietet umfassende Kontrollen für die Einhaltung und Verwaltung sensibler oder persönlich identifizierbarer Daten&mdash;einschließlich Daten, die von der [!INCLUDE [prod_short](includes/prod_short.md)] App zu Chats und Kanälen hinzugefügt wurde.

### <a name="understanding-where--cards-are-stored"></a>Verstehen wo [!INCLUDE [prod_short](includes/prod_short.md)] Karten gespeichert werden

Nachdem eine Karte an einen Chat gesendet wurde, werden die Karte und die auf der Karte angezeigten Felder in Teams kopiert. Diese Informationen unterliegen den Teamrichtlinien für Ihr Unternehmen, z. B. Richtlinien zur Aufbewahrung von Daten. Bei der Anzeige von Kartendetails werden keine Daten im Detailfenster in Teams gespeichert. Die Daten bleiben in [!INCLUDE [prod_short](includes/prod_short.md)] gespeichert und wird nur von Teams abgerufen, wenn der Benutzer die Details anzeigen möchte. 

- Weitere Informationen darüber, wo Teams diese Daten speichern, finden Sie unter [Speicherort der Daten in Microsoft Teams](/microsoftteams/location-of-data-in-teams).
- Weitere Informationen zu Aufbewahrungsrichtlinien in Teams finden Sie unter [Aufbewahrungsrichtlinien in Microsoft Teams](/microsoftteams/retention-policies).

### <a name="restricting-sharing-of-cards"></a>Beschränken des Kartenaustauschs

Sie verhindern, dass bestimmte Benutzer oder Gruppen Karten an Chats oder Kanäle senden, indem Sie Nahrichten-Richtlinien einrichten, die die Einstellung **URL-Vorschau** deaktivieren. Weitere Informationen zu dieser Einstellung finden Sie unter [Nachrichtenrichtlinien in Teams verwalten](/microsoftteams/messaging-policies-in-teams). 

Sie können auch Informationssperren verwenden, um zu verhindern, dass Einzelpersonen oder Gruppen miteinander kommunizieren. Weitere Informationen finden Sie unter [Informationssperren in Microsoft Teams](/microsoftteams/information-barriers-in-teams).

Funktionen zur Verhinderung von Datenverlust im Microsoft 365 Security & Compliance Center können nicht speziell auf Karten angewendet werden. Sie können jedoch auf die Chat-Nachrichten angewendet werden, die die Karten enthalten. <!-- To track upcoming advanced features that include enabling DLP for cards, see [https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093](https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093).-->

### <a name="responding-to-data-requests"></a>Antworten auf Datenenanforderungen

Sie ermöglichen Teammitgliedern und Teambesitzern, Nachrichten mit vertraulichen Karten zu löschen, indem Sie Nachrichtenrichtlinien einrichten, wie **Besitzer können gesendete Nachrichten löschen** und **Benutzer können gesendete Nachrichten löschen**. Weitere Informationen zu dieser Einstellung finden Sie unter [Nachrichtenrichtlinien in Teams verwalten](/microsoftteams/messaging-policies-in-teams).

Inhaltssuche und eDiscovery Compliance-Funktionen im Microsoft 365 Security & Compliance Center können nicht auch auf Karten angewendet werden.

Weil Kartendaten in Teams eine Kopie der Daten in [!INCLUDE [prod_short](includes/prod_short.md)] sind, können Sie auch [!INCLUDE [prod_short](includes/prod_short.md)] Funktionen zum Exportieren der Kundendaten sofern erforderlich verwenden. Weitere Informationen zum Datenschutz in [!INCLUDE [prod_short](includes/prod_short.md)] finden Sie unter [FAQ zu Datenschutz für Business Central Debitoren](/dynamics365/business-central/dev-itpro/security/privacyfaq).

## <a name="show-or-hide-record-data-on-cards"></a>Datensatzdaten auf Karten ein- oder ausblenden

Wenn ein Datensatz mit anderen in einem Teams-Chat oder -Kanal geteilt wird, wird eine Karte mit Feldern angezeigt, die Daten über den Datensatz enthalten. Alle Empfänger können diese Daten (oder die Datensatzzusammenfassung) standardmäßig anzeigen, unabhängig von ihrer Lizenz oder ihren Berechtigungen in Business Central. Wenn Sie ein Administrator sind, können Sie die **Karteneinstellungen** unterstützte Einrichtungsanleitung verwenden, um zu verhindern, dass die Datensatzzusammenfassung auf Karten in Teams angezeigt wird. Durch das Ausblenden der Datensatzzusammenfassung werden alle Felder und Bilder entfernt, die Schaltfläche **Details** und andere Nicht-Datensatzinformationen werden jedoch weiterhin auf der Karte angezeigt.

|Zusammenfassung aktivieren|Zusammenfassung deaktivieren|
|-|-|
|![Bild, das eine Karte in Teams zeigt, wenn die Datensatzzusammenfassung aktiviert ist.](media/card-settings-example-on.png)|![Bild, das eine Karte in Teams zeigt, wenn die Datensatzzusammenfassung deaktiviert ist.](media/card-settings-example-off.png)|

Sie konfigurieren die Einstellung pro Umgebung. Wenn Sie also die Datensatzzusammenfassung ein- oder ausschalten, wirkt sich dies auf alle Unternehmen in der Umgebung aus.

1. Öffnen Sie in Business Central die Umgebung, die Sie ändern möchten.

   > [!TIP]
   > Wählen Sie zum Wechseln der Umgebung <kbd>Strg</kbd>+<kbd>O</kbd>.
2. Wählen Sie die ![Lupe, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol, geben Sie **Karteneinstellungen** ein, und wählen Sie dann den entsprechenden Link. <!--Or, select [here](https://businesscentral.dynamics.com/?page=1833) to open the page directly.-->
3. Lesen Sie die Informationen zu den **Karteneinstellungen** und wählen Sie dann **Weiter**, wenn Sie fertig sind.
4. Auf der **Datensichtbarkeit**-Seite, schalten Sie die **Datensatzzusammenfassung anzeigen** an, um Daten auf den Karten anzuzeigen, oder aus, um die Daten auszublenden.
5. Wählen Sie **Nächste** und befolgen Sie die Anweisungen, um die Einrichtungsanleitung abzuschließen.

## <a name="related-information"></a>Weitere Informationen

[[!INCLUDE [prod_short](includes/prod_short.md)] und Microsoft Teams Integration Übersicht](across-teams-overview.md)  
[Die App [!INCLUDE [prod_short](includes/prod_short.md)] für Microsoft Teams installieren](across-install-app-for-teams.md)  
[Teams FAQ](teams-faq.md)  
[Teams Problembehebung](admin-teams-troubleshooting.md)  
[Entwickeln für Teams Integration](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
