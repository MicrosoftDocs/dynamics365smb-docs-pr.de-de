---
title: E-Mail-Protokollierung einrichten | Microsoft Docs
description: Erfahren Sie, wie Sie E-Mail-Interaktionen zwischen Verkäufern und Kunden in echte Verkaufschancen verwandeln können.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: a431eba8881eb6bb32e01d67f25ea53981da445e
ms.sourcegitcommit: cb06aa973f5c767df774b0e1e199c6fbe0e85b88
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470337"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a>Verfolgen Sie den Austausch von E-Mail-Nachrichten zwischen Verkäufern und Kontakten

Machen Sie mehr aus der Kommunikation zwischen Verkäufern und Ihren bestehenden oder potenziellen Kunden, indem Sie den E-Mail-Austausch nachverfolgen und diese dann in umsetzbare Gelegenheiten umwandeln. [!INCLUDE[prod_short](includes/prod_short.md)] kann mit Exchange Online arbeiten, um ein Protokoll der eingehenden und ausgehenden Nachrichten zu erhalten. Sie können den Inhalt jeder Nachricht auf der Seite **Aktivitätenprotokollposten** anzeigen und analysieren.

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Öffentliche Ordner und Regeln für die E-Mail-Anmeldung in Exchange Online einrichten

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Als nächstes verbinden Sie [!INCLUDE[prod_short](includes/prod_short.md)] mit Exchange Online.

## <a name="setting-up-prod_short-to-log-email-messages"></a>Einrichten von [!INCLUDE[prod_short](includes/prod_short.md)], um E-Mail-Nachrichten zu protokollieren

Beginnen Sie mit der E-Mail-Protokollierung in zwei einfachen Schritten:

1. Stellen Sie eine Verbindung von [!INCLUDE[prod_short](includes/prod_short.md)] mit Exchange Online her für Ihr Microsoft 365-Abonnement. Exchange Online verarbeitet Ihre E-Mail-Nachrichten. Wir haben diesen Schritt vereinfacht, indem wir eine Anleitung für Unterstützte Einrichtung bereitgestellt haben. Sie benötigen lediglich Ihre Administratoranmeldeinformationen für Ihr Administratorkonto in Microsoft 365. Um die Anleitung zu starten, gehen Sie zu **Unterstützte Einrichtung**, und wählen Sie dann **E-Mail-Protokollierung einrichten** aus.  

2. Stellen Sie sicher, dass in [!INCLUDE[prod_short](includes/prod_short.md)] gültige E-Mail-Adressen für Ihre Verkäufer und Kontakte eingegeben wurden, je nachdem, ob es sich um potenzielle oder bestehende Kunden handelt. Öffnen Sie dazu für jeden Kunden oder Verkäufer die Karte **Kontakt** oder **Verkäufer/Käufer**, und überprüfen Sie das Feld **E-Mail**.

> [!Tip]
> Nachdem Sie die Schritte in der Anleitung ausgeführt haben, können Sie überprüfen, ob die Verbindung erfolgreich war. Suchen Sie nach **Marketingeinrichtung**, wählen Sie **Verarbeiten** aus, dann **Funktionen**, und dann **E-Mail-Protokollierungseinr. überprüfen** aus.

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a>Anzeigen des E-Mail-Nachrichtenaustauschs im Aktivitätenprotokoll
[!INCLUDE[prod_short](includes/prod_short.md)] erstellt einen Eintrag auf der Seite **Aktivitätenprotokoll**, jedes Mal, wenn ein Verkäufer und ein Kontakt eine E-Mail-Nachricht austauschen. Um das Interaktionsprotokoll anzuzeigen, öffnen Sie die Karte **Kontakt** oder **Verkäufer/Einkäufer** für die Person, und wählen Sie dann **Verkauf** und dann **Interaktionsprotokollposten** aus. Es gibt einige Dinge, die wir mit jedem Eintrag im Protokoll tun können, zum Beispiel:

- Zeigen Sie den Inhalt der E-Mail-Nachricht an, die ausgetauscht wurde, indem Sie auf die Aktion **Dateianhänge anzeigen** klicken.
- Verwandeln Sie einen E-Mail-Austausch in eine Verkaufschance: Wenn ein Eintrag vielversprechend aussieht, können Sie ihn in eine Verkaufschance verwandeln und dann den Fortschritt in Richtung Verkauf steuern. Wählen Sie hierzu den Eintrag aus, und wählen Sie dann die Aktion **Verkaufschance erstellen** aus. Weitere Informationen finden Sie unter [Verkaufschancen verwalten](marketing-manage-sales-opportunities.md).

## <a name="connecting-on-premises-versions-to-microsoft-exchange"></a>Verbinden von lokalen Versionen mit Microsoft Exchange
Sie können eine Verbindung mit [!INCLUDE[prod_short](includes/prod_short.md)] lokal zum Austausch lokal oder für die Exchange Online Protokollierung verbinden. Für beide Exchange-Versionen sind die Einstellungen für die Verbindung auf der Seite **Marketing-Einrichtung** verfügbar. Für Exchange Online können Sie auch eine unterstützte Einrichtungsanleitung verwenden. 

### <a name="connecting-to-exchange-on-premises"></a>Mit Exchange lokal verbinden
Verbinden Sie [!INCLUDE[prod_short](includes/prod_short.md)] lokal mit Exchange lokal auf der Seite **Marketing-Einrichtung**. Sie können **Basis** als die **Authentifizierungsart** verwenden. Geben Sie anschließend die Anmeldeinformationen für das Benutzerkonto für Exchange lokal ein. Dann schalten Sie die **aktiviert** Umschaltung ein, um die Protokollierung von E-Mails zu starten. 

### <a name="connecting-to-exchange-online"></a>Verbinden mit Exchange Online
Zum Verbinden mit Exchange Online müssen Sie **OAuth2** als **Authentifizierungsart** verwenden. Wenn Sie eine Verbindung mit einer Anwendung in Azure Active Directory herstellen möchten, müssen Sie eine Anwendungs-ID mit dem geheimen Schlüssel eingeben und die zu verwendende Umleitungs-URL angeben. Die Umleitungs-URL ist bereits ausgefüllt und sollte für die meisten Installationen funktionieren. Weitere Informationen finden Sie unter [So registrieren Sie eine Anwendung in Azure AD für die Verbindung von Business Central mit Exchange Online](marketing-set-up-email-logging.md#to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online). 

Sie müssen Ihre Installation für die Verwendung von HTTPS einrichten. Weitere Informationen finden Sie unter [Konfigurieren von SSL zum Sichern der Business Central Web Client-Verbindung ](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Wenn Sie Ihren Server für eine andere Homepage einrichten, können Sie die URL jederzeit ändern. Der geheime Clientschlüssel wird als verschlüsselte Zeichenfolge in Ihrer Datenbank gespeichert.

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online"></a>So registrieren Sie eine Anwendung in Azure AD, um eine Verbindung mit Exchange Online über Business Central herzustellen
Bei den folgenden Schritten wird davon ausgegangen, dass Sie Azure Active Directory verwenden, um Identitäten und den Zugriff zu verwalten. Weitere Informationen finden Sie unter [Schnellstart: Registrieren einer Anwendung mit der Microsoft-Identitätsplattform](/azure/active-directory/develop/quickstart-register-app). Wenn Sie Azure Active Directory nicht verwenden, finden Sie weitere Informationen unter [Verwenden eines anderen Identitäts- und Zugriffsverwaltungsdienstes](marketing-set-up-email-logging.md#using-another-identity-and-access-management-service). 

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
8. Wählen Sie **Übersicht** aus, und suchen Sie dann den Wert **Anwendungs-(Client-)ID**. Dies ist die Client-ID Ihrer Anwendung. Sie müssen sie auf der Seite **Marketing Einrichtungsseite** im Feld **Client-ID** eingeben oder in einem sicheren Speicher speichern und in einem Ereignisabonnenten bereitstellen.
9. Unter [!INCLUDE[prod_short](includes/prod_short.md)] richten Sie die E-Mail-Protokollierung auf der Seite **Marketing-Eirnichtung** ein oder verwenden Sie die **Unterstützte Einrichtung für die E-Mail-Protokollierung** für Unterstützung bei diesem Prozess.
    * Geben Sie das E-Mail-Konto des Benutzers an, für den der geplante Auftrag eine Verbindung mit Exchange Online herstellen und E-Mails verarbeiten soll. Der Benutzer muss eine gültige Lizenz für Exchange Online haben.
    * Geben Sie die URL für Exchange Online an. In der Regel ist dies die Domäne, die Sie in der E-Mail-Adresse des Benutzers angegeben haben.
    * Geben Sie den **Warteschlangenordnerpfad** und den **Speicherordnerpfad** an.
10. Um die E-Mail-Protokollierung zu starten, schalten Sie die **aktiviert** Umschaltung ein.
11. Melden Sie sich mit Ihrem Administratorkonto für Azure Active Directory an (dieses Konto muss eine gültige Lizenz für Exchange haben und ein Administrator in Ihrer Exchange Online-Umgebung sein). Nachdem Sie sich angemeldet haben, werden Sie aufgefordert, Ihrer registrierten Anwendung zu erlauben, sich im Namen der Organisation bei Exchange Online anzumelden. Sie müssen Ihre Zustimmung geben, um die Einrichtung abzuschließen.

   > [!NOTE]
   > Wenn Sie nicht aufgefordert werden, sich mit Ihrem Administratorkonto anzumelden, liegt dies wahrscheinlich daran, dass Popups blockiert sind. Erlauben Sie Popups von https://login.microsoftonline.com, um sich anzumelden.

### <a name="using-another-identity-and-access-management-service"></a>Verwenden eines anderen Identitäts- und Zugriffsverwaltungsdienstes
Wenn Sie Azure Active Directory nicht verwenden, um Identitäten und den Zugriff zu verwalten, benötigen Sie die Hilfe eines Entwicklers. Wenn Sie die App-ID und den geheimen Schlüssel lieber an einem anderen Ort speichern möchten, können Sie die Felder „Client-ID“ und „Geheimer Clientschlüssel“ leer lassen und eine Erweiterung schreiben, um die ID und den geheimen Schlüssel von diesem Speicherort abzurufen. Sie können den geheimen Clientschlüssel zur Laufzeit bereitstellen, indem Sie die Ereignisse OnGetEmailLoggingClientId und OnGetEmailLoggingClientSecret in Codeunit 1641 E-Mail-Protokollierung einrichten abonnieren.

### <a name="to-stop-logging-email"></a>E-Mail-Protokollierung beenden
1. Wählen Sie die ![Glühbirne, die das Symbol Wie möchten Sie weiter verfahren](media/ui-search/search_small.png "Was möchten Sie tun") öffnet, geben Sie **Benutzereinrichtung** ein und wählen Sie dann den entsprechenden Link.
2. Umschaltung **Aktiviert** ausschalten.

## <a name="see-also"></a>Siehe auch
[Verwalten von Beziehungen](marketing-relationship-management.md)



[!INCLUDE[footer-include](includes/footer-banner.md)]