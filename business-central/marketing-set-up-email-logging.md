---
title: E-Mail-Protokollierung einr.
description: 'Erfahren Sie, wie Sie E-Mail-Interaktionen zwischen Verkäufern und Kunden in echte Verkaufschancen verwandeln können.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'relationship, prospect, opportunity, email'
ms.date: 03/22/2022
ms.search.form: '1680, 1811, 5076'
ms.author: bholtorf
---
# Verfolgen Sie den Austausch von E-Mail-Nachrichten zwischen Verkäufern und Kontakten
Machen Sie mehr aus der Kommunikation zwischen Ihren Verkäufern und Kunden, indem Sie den E-Mail-Verkehr in umsetzbare Verkaufsmöglichkeiten verwandeln. [!INCLUDE[prod_short](includes/prod_short.md)] kann mit Exchange Online arbeiten, um ein Protokoll der eingehenden und ausgehenden Nachrichten zu erhalten. Sie können den Inhalt jeder Nachricht auf der Seite **Aktivitätenprotokollposten** anzeigen und analysieren.

> [!NOTE]
> Im 1. Veröffentlichungszyklus 2022 haben wir die Prozesse zur Einrichtung der E-Mail-Protokollierung optimiert, um die Flexibilität und Sicherheit zu erhöhen. Wenn Sie ein neuer Kunde mit dieser Version sind, nutzen Sie die neue Erfahrung. Wenn Sie bereits Kunde sind, hängt es davon ab, ob Sie die neue Erfahrung verwenden, ob Ihr Administrator die Funktionsaktualisierung **E-Mail-Protokollierung mit der Microsoft Graph API** auf der Seite **Funktionsverwaltung** aktiviert hat. Weitere Informationen finden Sie unter [Bevorstehende Funktionen im Voraus aktivieren](/dynamics365/business-central/dev-itpro/administration/feature-management).

> [!IMPORTANT]
> Für [!INCLUDE[prod_short](includes/prod_short.md)] online erfordert die neue Erfahrung, dass [!INCLUDE[prod_short](includes/prod_short.md)] und Exchange Online beim selben Tenant sind.

## So richten Sie E-Mail-Protokollierung ein
Diese Schritte unterscheiden sich je nachdem, ob Ihr Administrator das Feature-Update **E-Mail-Protokollierung mit der Microsoft Graph API** aktiviert hat. Wenn das Funktionsupdate nicht aktiviert ist, befolgen Sie die Schritte auf der Registerkarte **Aktuelle Erfahrung**.

## [Aktuelle Erfahrung](#tab/current-experience)

### Öffentliche Ordner und Regeln für die E-Mail-Anmeldung in Exchange Online einrichten

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Als nächstes verbinden Sie [!INCLUDE[prod_short](includes/prod_short.md)] mit Exchange Online.

## [Neue Erfahrung](#tab/new-experience)
### Einrichten eines freigegebenen Postfachs und Regeln für die E-Mail-Protokollierung in Exchange Online

> [!NOTE]
> Für diese Schritte ist Administratorzugriff für Exchange Online erforderlich.

Bereiten Sie ein freigegebenes Postfach im Exchange Admin Center vor. Alternativ können Sie auch Exchange Online PowerShell verwenden. Weitere Informationen finden Sie unter [Ein freigegebenes Postfach erstellen](/microsoft-365/admin/email/create-a-shared-mailbox) oder [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

> [!NOTE]
> Wenn Sie Exchange Management PowerShell verwenden, sind Ihre Änderungen mit einer Verzögerung im Exchange Admin Center verfügbar. Die Verzögerung kann mehrere Stunden betragen.

### Fügen Sie ein Benutzerkonto für Mitglieder des freigegebenen Postfachs hinzu
Das Konto, das Sie für die E-Mail-Protokollierung verwenden, ist ein Exchange Online-Konto. Der geplante Auftrag verwendet das Konto, um eine Verbindung mit dem freigegebenen Postfach herzustellen und E-Mails zu verarbeiten. Dieses Konto sollte keiner bestimmten Person zugeordnet werden. Fügen Sie das E-Mail-Konto den Mitgliedern für das freigegebene Postfach hinzu. Weitere Informationen finden Sie unter [Exchange Admin Center verwenden, um die Delegierung freigegebener Postfächer zu bearbeiten](/exchange/collaboration-exo/shared-mailboxes#use-the-eac-to-edit-shared-mailbox-delegation).

### Erlauben Sie anderen Benutzern, protokollierte E-Mails zu sehen
Sie können einem anderen Benutzer erlauben, eine E-Mail-Nachricht in Exchange zu öffnen, die sich auf einen Interaktionsprotokolleintrag von [!INCLUDE[prod_short](includes/prod_short.md)] bezieht. Geben Sie dazu dem Benutzer ``Read``-Rechte für den **Archiv**-Ordner im freigegebenen Postfach. Weitere Informationen finden Sie unter [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

### E-Mail-Fluss-Regeln erstellen
Nachrichtenflussregeln suchen nach bestimmten Bedingungen für Nachrichten und ergreifen entsprechende Maßnahmen. Erstellen Sie zwei neue E-Mail-Fluss-Regeln für öffentliche Ordner basierend auf den Informationen in der folgenden Tabelle. Weitere Informationen finden Sie unter [E-Mail-Fluss-Regeln in Exchange Online verwalten](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules?preserve-view=true) und [Aktionen für E-Mail-Fluss-Regeln in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions?preserve-view=true).

|Zweck  |Name  |Diese Regel anwenden, wenn...  |Führen Sie die folgenden Schritte aus...  |
|---------|---------|---------|---------|
|Regel für eingehende E-Mails     |An diese Organisation gesendete E-Mails protokollieren|Der Absender befindet sich außerhalb der Organisation und der Empfänger befindet sich innerhalb der Organisation|Das für das freigegebene Postfach festgelegte E-Mail-Konto mit Bcc senden.|
|Regel für ausgehende E-Mails     |Von dieser Organisation gesendete E-Mails protokollieren|Der Absender befindet sich innerhalb der Organisation und der Empfänger befindet sich außerhalb der Organisation.|Das für das freigegebene Postfach festgelegte E-Mail-Konto mit Bcc senden.|

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] verarbeitet nur Nachrichten im Posteingangsordner im freigegebenen Postfach. Wenn eine Regel Nachrichten aus dem Posteingang in einen anderen Ordner verschiebt, werden diese Nachrichten nicht verarbeitet. Außerdem werden Nachrichten im Junk-E-Mail-Ordner ebenfalls ignoriert. 

---

## [!INCLUDE[prod_short](includes/prod_short.md)] zum Protokollieren von E-Mail-Nachrichten einrichten
Diese Schritte sind für die aktuellen und neuen Erfahrungen gleich.

Beginnen Sie mit der E-Mail-Protokollierung in zwei einfachen Schritten:

1. Verbinden Sie [!INCLUDE[prod_short](includes/prod_short.md)] mit Exchange Online für Ihr Microsoft 365-Abonnement. Exchange Online verarbeitet Ihre E-Mail-Nachrichten. Wir haben diesen Schritt vereinfacht, indem wir eine Anleitung für Unterstützte Einrichtung bereitgestellt haben. Sie benötigen lediglich Ihre Administratoranmeldeinformationen für Ihr Administratorkonto in Microsoft 365. Um die Anleitung zu starten, wechseln Sie zu **Unterstützte Einrichtung**, und wählen Sie dann die Anleitung **E-Mail-Protokollierung einrichten** aus.  

2. Stellen Sie sicher, dass die E-Mail-Adressen Ihrer Vertriebsmitarbeiter und Kontakte in [!INCLUDE[prod_short](includes/prod_short.md)] gültig sind. Öffnen Sie dazu für jeden Kunden oder Verkäufer die Karte **Kontakt**oder **Verkäufer/Käufer**, und überprüfen Sie das Feld **E-Mail**.

> [!Tip]
> Nachdem Sie die Schritte in der Anleitung ausgeführt haben, können Sie überprüfen, ob die Verbindung erfolgreich war. Führen Sie je nachdem, ob Sie die aktuelle oder die neue Erfahrung verwenden, einen der folgenden Schritte aus: 
>
> * **Aktuelle Erfahrung**: Suchen Sie nach **Marketingeinrichtung**, wählen Sie **Zugriff**, dann **Funktionen** und dann die Option **E-Mail-Protokollierungseinr. überprüfen** aus.
> * **Neue Erfahrung**: Suchen Sie nach **E-Mail-Protokollierung**, wählen Sie **Aktionen** und dann **Einrichtung überprüfen** aus.

## Anzeigen des E-Mail-Nachrichtenaustauschs im Aktivitätenprotokoll

[!INCLUDE[prod_short](includes/prod_short.md)] erstellt einen Eintrag auf der Seite **Aktivitätenprotokoll**, jedes Mal, wenn ein Verkäufer und ein Kontakt eine E-Mail-Nachricht austauschen. Um das Interaktionsprotokoll anzuzeigen, öffnen Sie die Karte **Kontakt** für die Person, und wählen Sie **Zugehörig**, dann **Verlauf** und anschließend **Interaktionsprotokollposten** aus. Es gibt einige Dinge, die Sie mit jedem Eintrag im Protokoll tun können, zum Beispiel:

- Zeigen Sie den Inhalt der E-Mail-Nachricht an, die ausgetauscht wurde, indem Sie **Verarbeiten** und dann **Dateianhänge anzeigen** auswählen.
- Verwandeln Sie einen E-Mail-Austausch in eine Verkaufsmöglichkeit. Wenn ein Eintrag vielversprechend aussieht, können Sie ihn in eine Verkaufschance verwandeln und dann den Fortschritt in Richtung Verkauf steuern. Um einen E-Mail-Austausch in eine Chance zu verwandeln, wählen Sie den Eintrag, dann **Prozess** und dann **Gelegenheit schaffen** aus. Weitere Informationen finden Sie unter [Verkaufschancen verwalten](marketing-manage-sales-opportunities.md).

## Postfach- und Ordnerbeschränkungen in Exchange Online
Es gibt Postfach- und Ordnerbeschränkungen in Exchange Online, darunter Beschränkungen für Ordnergrößen und Anzahl der Nachrichten. Weitere Informationen finden Sie unter [Exchange Online-Beschränkungen](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#storage-limits) und [Einschränkungen für öffentliche Ordner in Exchange Server](/Exchange/collaboration/public-folders/limits?view=exchserver-2019).

[!INCLUDE[prod_short](includes/prod_short.md)] speichert protokollierte E-Mail-Nachrichten in einem Ordner in Exchange Online. [!INCLUDE[prod_short](includes/prod_short.md)] speichert auch einen Link zu jeder protokollierten Nachricht. Die Links öffnen die protokollierten Nachrichten in Exchange Online auf den Seiten „Interaktionsprotokollposten“, „Kontaktkarte“ und „Verkäuferkarte“ in [!INCLUDE[prod_short](includes/prod_short.md)]. Wenn eine protokollierte Nachricht in einen anderen Ordner verschoben wird, wird der Link beschädigt. Beispielsweise kann eine Nachricht manuell verschoben werden, oder Exchange Online kann AutoSplit automatisch starten, wenn ein Speicherlimit erreicht ist.

Anhand der folgenden Schritte können Sie verhindern, dass Links zu Nachrichten in Exchange Online beschädigt werden.

1. Verschieben Sie vorhandene Nachrichten nicht in einen anderen Ordner, nachdem Sie die Einstellungen für Ihre E-Mail-Protokollierung geändert haben. Wenn Sie vorhandene Nachrichten dort belassen, wo sie sind, bleiben die Links erhalten. Links zu Nachrichten im neuen Ordner sind gültig.
2. Vermeiden Sie das Erreichen der Postfach- und Ordnerbeschränkungen. Wenn Sie kurz davor sind, eine Beschränkung zu erreichen, führen Sie die folgenden Schritte aus:
    1. Richten Sie ein neues freigegebenes Postfach (neue Erfahrung) oder einen neuen freigegebenen Ordner (aktuelle Erfahrung) in Exchange Online ein.
    2. Aktualisieren Sie Ihre E-Mail-Flow-Regeln in Exchange Online.
    3. Aktualisieren Sie die Einrichtung der E-Mail-Protokollierung in Business Central entsprechend.

## Lokale Versionen mit Microsoft Exchange verbinden

Sie können eine Verbindung mit [!INCLUDE[prod_short](includes/prod_short.md)] lokal zum Austausch lokal oder für die Exchange Online Protokollierung verbinden. Für beide Exchange-Versionen sind die Einstellungen für die Verbindung auf der Seite **Marketing-Einrichtung** verfügbar. Für Exchange Online können Sie auch eine unterstützte Einrichtungsanleitung verwenden.

> [!IMPORTANT]
> Die neue Erfahrung unterstützt keine Verbindung mit Exchange lokal. Wenn Sie Exchange lokal verwenden müssen, aktivieren Sie das Funktionsupdate nicht für die neue Erfahrung.

## Mit lokaler Version von Exchange verbinden
## [Aktuelle Erfahrung](#tab/current-experience)
Verbinden Sie [!INCLUDE[prod_short](includes/prod_short.md)] lokal mit Exchange lokal auf der Seite **Marketing-Einrichtung**. Sie können **Basis** als die **Authentifizierungsart** verwenden. Geben Sie anschließend die Anmeldeinformationen für das Benutzerkonto für Exchange lokal ein. Dann schalten Sie die **aktiviert** Umschaltung ein, um die Protokollierung von E-Mails zu starten.

## [Neue Erfahrung](#tab/new-experience)
Die neue Erfahrung unterstützt keine Verbindungen mit Exchange lokal.

---

## Mit Exchange Online verbinden
Um Exchange Online zu verbinden, müssen Sie eine Anwendung in Azure Active Directory registrieren. Geben Sie die Anwendungs-ID, das Geheimnis des Schlüsseltresors und die Umleitungs-URL an, die für die Registrierung verwendet werden soll. Die Umleitungs-URL ist bereits festgelegt und sollte für die meisten Installationen funktionieren. Weitere Informationen finden Sie unter [So registrieren Sie eine Anwendung in Azure AD für die Verbindung von Business Central mit Exchange Online](marketing-set-up-email-logging.md#to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online). 

Sie müssen auch **OAuth2** als **Authentifizierungstyp** verwenden. Sie müssen auch eine Anwendung in registrieren Azure Active Directory. Geben Sie die Anwendungs-ID, das Geheimnis des Schlüsseltresors und die Umleitungs-URL an, die für die Registrierung verwendet werden soll. Die Umleitungs-URL ist bereits ausgefüllt und sollte für die meisten Installationen funktionieren. Weitere Informationen finden Sie weiter unten unter „So registrieren Sie eine Anwendung in Azure AD für die Verbindung von Business Central mit Exchange Online“.

Sie müssen Ihre Installation für die Verwendung von HTTPS einrichten. Weitere Informationen finden Sie unter [Konfigurieren von SSL zum Sichern der Business Central Web Client-Verbindung ](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Wenn Sie Ihren Server für eine andere Homepage einrichten, können Sie die URL jederzeit ändern. Der geheime Clientschlüssel wird als verschlüsselte Zeichenfolge in Ihrer Datenbank gespeichert.

### So registrieren Sie eine Anwendung in Azure AD, um eine Verbindung mit Exchange Online über Business Central herzustellen
Bei den folgenden Schritten wird davon ausgegangen, dass Sie Azure Active Directory verwenden, um Identitäten und den Zugriff zu verwalten. Weitere Informationen finden Sie unter [Schnellstart: Registrieren einer Anwendung mit der Microsoft-Identitätsplattform](/azure/active-directory/develop/quickstart-register-app). 

## [Aktuelle Erfahrung](#tab/current-experience) 
Bei den folgenden Schritten wird davon ausgegangen, dass Sie Azure Active Directory verwenden, um Identitäten und den Zugriff zu verwalten. Weitere Informationen finden Sie unter [Schnellstart: Registrieren einer Anwendung mit der Microsoft-Identitätsplattform](/azure/active-directory/develop/quickstart-register-app). Wenn Sie Azure Active Directory nicht verwenden, finden Sie weitere Informationen unter [Verwenden eines anderen Identitäts- und Zugriffsverwaltungsdienstes](marketing-set-up-email-logging.md#use-another-identity-and-access-management-service). 

1. Wählen Sie im Navigationsbereich von Azure-Portal unter **Verwalten** die Option **Authentifizierung** aus.
2. Fügen Sie unter **URL umleiten** die Umleitungs-URL hinzu, die auf der Seite **Marketing Einrichten** in [!INCLUDE[prod_short](includes/prod_short.md)] vorgeschlagen wird. Wenn die Weiterleitungs-URL auf der Seite Marketing-Einrichtung leer ist, finden Sie die vorgeschlagene Weiterleitungs-URL auf der Seite **Unterstützung Einrichtung fjür die E-Mail-Protokollierung**.

    > [!NOTE]
    > Wenn Sie die Umleitungs-URL nicht angeben, können Sie dies später durch Auswahl von **Fügen Sie eine Plattform hinzu** tun und dann **Internet** wählen, um die Webanwendung und die Weiterleitungs-URL hinzuzufügen. 

3. Wählen Sie unter **Verwalten** die Option **Manifest** aus.
4. Suchen Sie die **requiredResourceAccess** Eigenschaft im Manifest, und fügen Sie den folgenden Code in die Klammern ([]) ein, um die erforderlichen Berechtigungen hinzuzufügen. Weitere Informationen finden Sie unter [Anwendung anmelden](/exchange/client-developer/exchange-web-services/how-to-authenticate-an-ews-application-by-using-oauth#register-your-application).

```
{
    "resourceAppId": "00000002-0000-0ff1-ce00-000000000000",
    "resourceAccess": [
        {
            "id": "3b5f3d61-589b-4a3c-a359-5dd4b5ee5bd5",
            "type": "Scope"
        },
        {
            "id": "dc890d15-9560-4a4c-9b7f-a736ec74ec40",
            "type": "Role"
        }
    ]
}
```

5. Wählen Sie **Speichern** aus.
6. Unter **Verwalten** wählen Sie **API-Berechtigungen** und bestätigen Sie anschließend, dass die folgenden Berechtigungen aufgeführt sind:  

    * EWS.AccessAsUser.All
    * full_access_as_app

7. Wählen Sie unter **Verwalten** die Option **Zertifikate & Geheimnisse** aus, und erstellen Sie dann einen neuen geheimen Schlüssel für Ihre App. Sie müssen den geheimen Clientschlüssel entweider in [!INCLUDE[prod_short](includes/prod_short.md)] im Feld **Geheimer Clientschlüsse** auf der Seite **Marketing-Einrichtung** eingeben oder in einem sicheren Speicher speichern und in einem Ereignisabonnenten bereitstellen.
8. Wählen Sie **Übersicht** aus, und suchen Sie dann den Wert **Anwendungs-(Client-)ID**. Der Wert **Anwendungs-(Client-)ID** ist die Client-ID Ihrer Anwendung. Sie müssen die Client-ID auf der Seite **Marketing Einrichtungsseite** im Feld **Client-ID** eingeben oder in einem sicheren Speicher speichern und in einem Ereignisabonnenten bereitstellen.
9. Unter [!INCLUDE[prod_short](includes/prod_short.md)] richten Sie die E-Mail-Protokollierung auf der Seite **Marketing-Eirnichtung** ein oder verwenden Sie die **Unterstützte Einrichtung für die E-Mail-Protokollierung** für Unterstützung bei diesem Prozess.
    * Geben Sie das E-Mail-Konto des Benutzers an, für den der geplante Auftrag eine Verbindung mit Exchange Online herstellen und E-Mails verarbeiten soll. Der Benutzer muss eine gültige Lizenz für Exchange Online haben.
    * Geben Sie die URL für Exchange Online an. In der Regel ist diese URL die Domäne, die Sie in der E-Mail-Adresse des Benutzers angegeben haben.
    * Geben Sie den **Warteschlangenordnerpfad** und den **Speicherordnerpfad** an.
10. Um die E-Mail-Protokollierung zu starten, schalten Sie die **aktiviert** Umschaltung ein.
11. Melden Sie sich mit Ihrem Administratorkonto für Azure Active Directory an (dieses Konto muss eine gültige Lizenz für Exchange haben und ein Administrator in Ihrer Exchange Online-Umgebung sein). Nachdem Sie sich angemeldet haben, müssen Sie Ihrer registrierten Anwendung erlauben, sich im Namen der Organisation bei Exchange Online anzumelden. Sie müssen Ihre Zustimmung geben, um die Einrichtung abzuschließen.

   > [!NOTE]
   > Wenn Sie nicht aufgefordert werden, sich mit Ihrem Administratorkonto anzumelden, liegt dies wahrscheinlich daran, dass Popups blockiert sind. Erlauben Sie Popups von https://login.microsoftonline.com, um sich anzumelden.

## [Neue Erfahrung](#tab/new-experience)
1. Wählen Sie im Navigationsbereich von Azure-Portal unter **Verwalten** die Option **Authentifizierung** aus.
2. Fügen Sie unter **URL umleiten** die Umleitungs-URL hinzu, die auf der Seite **E-Mail-Protokollierung** in [!INCLUDE[prod_short](includes/prod_short.md)] vorgeschlagen wird. Wenn das URL-Feld auf der Seite E-Mail-Protokollierung leer ist, finden Sie die vorgeschlagene Weiterleitungs-URL auf der Seite **Unterstützung Einrichtung**. Um die Seite zu öffnen, wählen Sie auf der **E-Mail-Protokollierung**-Seite **Aktionen** und dann **Unterstützte Einrichtung** aus.

    > [!NOTE]
    > Wenn Sie die Umleitungs-URL nicht angeben, können Sie dies später durch Auswahl von **Fügen Sie eine Plattform hinzu** tun und dann **Internet** wählen, um die Webanwendung und die Weiterleitungs-URL hinzuzufügen.

3. Unter **Verwalten** wählen Sie **API-Berechtigungen** und dann **Microsoft Graph** und dann aus **Delegierte Berechtigungen**.
4. Verwenden Sie das Suchfeld, um **Mail** zu suchen und auszuwählen, und fügen Sie dann die **Mail.ReadWrite.Shared**-Berechtigung hinzu. 
5. Wählen Sie unter **Verwalten** die Option **Zertifikate & Geheimnisse** aus, und erstellen Sie dann einen neuen geheimen Schlüssel für Ihre App. Sie verwenden das Geheimnis entweder im **Client-Geheimnis**-Feld auf der **E-Mail-Protokollierung**-Seite in [!INCLUDE[prod_short](includes/prod_short.md)].
6. Wählen Sie **Übersicht** aus, und suchen Sie dann den Wert **Anwendungs-(Client-)ID**. Dies ist die Client-ID Ihrer Anwendung. Sie müssen es entweder im **Client-ID**-Feld auf der **E-Mail-Protokollierung**-Seite eingeben.
7. Unter [!INCLUDE[prod_short](includes/prod_short.md)] richten Sie die E-Mail-Protokollierung auf der Seite **E-Mail-Protokollierung** ein oder verwenden Sie die **Unterstützte Einrichtung** für Unterstützung bei diesem Prozess.

### Verwenden eines anderen Identitäts- und Zugriffsverwaltungsdienstes
Wenn Sie Azure Active Directory nicht verwenden, um Identitäten und den Zugriff zu verwalten, benötigen Sie die Hilfe eines Entwicklers. Wenn Sie die App-ID und den geheimen Schlüssel lieber an einem anderen Ort speichern möchten, können Sie die Felder „Client-ID“ und „Geheimer Clientschlüssel“ leer lassen und eine Erweiterung schreiben, um die ID und den geheimen Schlüssel von diesem Speicherort abzurufen. Sie können den geheimen Clientschlüssel zur Laufzeit bereitstellen, indem Sie die Ereignisse OnGetEmailLoggingClientId und OnGetEmailLoggingClientSecret in Codeunit 1641 E-Mail-Protokollierung einrichten abonnieren.

---

## E-Mail-Protokollierung starten
1. Um die E-Mail-Protokollierung zu starten, aktivieren Sie auf der Seite **E-Mail-Protokollierung** den Schalter **Aktiviert**.
2. Melden Sie sich mit dem Exchange Online-Konto an, das der geplante Auftrag für die Verbindung mit dem freigegebenen Postfach und die Verarbeitung von E-Mails verwenden soll.

    > [!NOTE]
    > Wenn Sie nicht aufgefordert werden, sich bei Ihrem Exchange Online-Konto anzumelden, liegt das möglicherweise daran, dass Ihr Browser Popups blockiert. Erlauben Sie Popups von https://login.microsoftonline.com, um sich anzumelden.

## E-Mail-Protokollierung beenden
## [Aktuelle Erfahrung](#tab/current-experience)
1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Marketing Einrichtung** ein, und wählen Sie dann den zugehörigen Link.
1. Umschaltung **Aktiviert** ausschalten.

## [Neue Erfahrung](#tab/new-experience)
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **E-Mail-Protokollierung** ein und wählen Sie dann den zugehörigen Link.
2. Umschaltung **Aktiviert** ausschalten.

---

## Zum Ändern des für die E-Mail-Protokollierung verwendeten Benutzerkontos
Wenn Sie die neue Erfahrung verwenden, können Sie das für die E-Mail-Protokollierung verwendete Benutzerkonto ändern. Die aktuelle Erfahrung unterstützt dies nicht.

## [Aktuelle Erfahrung](#tab/current-experience) 
Deaktivieren Sie Ihr aktuelles Setup, ändern Sie den Benutzer auf der **E-Mail-Protokollierung** Seite und aktivieren Sie dann die E-Mail-Protokollierung erneut. Sie können auch die Anleitung zur unterstützten Einrichtung erneut ausführen.

## [Neue Erfahrung](#tab/new-experience)
### [!INCLUDE[prod_short](includes/prod_short.md)] Online
1. Melden Sie sich mit dem [!INCLUDE[prod_short](includes/prod_short.md)]-Konto an, das der geplante Auftrag für die Verbindung mit dem freigegebenen Postfach und die Verarbeitung von E-Mails verwenden soll. Dieses Konto muss Zugriff auf [!INCLUDE[prod_short](includes/prod_short.md)] und Exchange Online haben.
2. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **E-Mail-Protokollierung** ein und wählen Sie dann den zugehörigen Link. 
3. Wählen Sie **Verwandt** und dann **Aufgabenwarteschlangenposten**.
4. Starten Sie die **E-Mail-Protokollierung**-Aufgabe neu.

### [!INCLUDE[prod_short](includes/prod_short.md)] On-Premises
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **E-Mail-Protokollierung** ein und wählen Sie dann den zugehörigen Link. 
2. Wählen Sie **Aktionen** und dann **Token erneuern**.
3. Melden Sie sich mit dem Exchange Online-Konto an, das der geplante Auftrag für die Verbindung mit dem freigegebenen Postfach und die Verarbeitung von E-Mails verwenden soll.



## Weitere Informationen
[Verwalten von Beziehungen](marketing-relationship-management.md)



[!INCLUDE[footer-include](includes/footer-banner.md)]