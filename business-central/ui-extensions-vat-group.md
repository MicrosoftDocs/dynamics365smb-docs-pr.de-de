---
title: Die MwSt.-Gruppenverwaltungserweiterung für das Vereinigte Königreich
description: 'Sie können sich mit anderen Unternehmen zusammenschließen, um eine Mehrwertsteuergruppe zu bilden, in der alle Mitglieder die Mehrwertsteuer in einer einzigen Erklärung melden.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'VAT, value added tax, report'
ms.search.form: '4700, 4701, 4703, 4704, 4705, 4706, 4707, 4708, 4709,'
ms.date: 07/08/2022
ms.author: bholtorf
---

# <a name="the-vat-group-management-extension-for-the-united-kingdom"></a><a name="the-vat-group-management-extension-for-the-united-kingdom"></a><a name="the-vat-group-management-extension-for-the-united-kingdom"></a>Die MwSt.-Gruppenverwaltungserweiterung für das Vereinigte Königreich

Sie können ein oder mehrere Unternehmen in Großbritannien verbinden, um die Mehrwertsteuerberichterstattung unter einer einzigen Registrierungsnummer zu kombinieren. Diese Art der Anordnung ist bekannt als *Mehrwertsteuergruppe*. Sie können mit der Gruppe als Mitglied oder als Gruppenvertreter zusammenarbeiten.

## <a name="forming-a-vat-group"></a><a name="forming-a-vat-group"></a><a name="forming-a-vat-group"></a>Bildung einer Mehrwertsteuergruppe

Mehrwertsteuergruppenmitglieder und der Gruppenvertreter können die Anleitung zur unterstützten Einrichtung für die **Mehrwertsteuergruppenverwaltung einrichten** verwenden, um ihre Zusammenarbeit mit der Gruppe zu definieren und eine Verbindung zwischen ihren [!INCLUDE[prod_short](includes/prod_short.md)]-Mandanten zu erstellen. Die Gruppenmitglieder verwenden diese Verbindung, um ihre Mehrwertsteuererklärung an den Gruppenvertreter zu senden. Der Gruppenvertreter verwendet dann eine einzelne MwSt.-Rückgabe, um die Mehrwertsteuer der Gruppe an die Steuerbehörden zu übermitteln.

[!INCLUDE[prod_short](includes/prod_short.md)] unterstützt konzerninterne Umsatzsteuererklärungen für Unternehmen, die [!INCLUDE[prod_short](includes/prod_short.md)] vor Ort oder online verwenden, in beliebiger Kombination, was die Kommunikationseinrichtung zwischen Unternehmen beeinflusst. Dieser Artikel beschreibt verschiedene Gruppeneinrichtungen.

### <a name="license-requirements"></a><a name="license-requirements"></a><a name="license-requirements"></a>Lizenzanforderungen

Die Teilnehmer der Gruppe müssen für die Verwendung von [!INCLUDE[prod_short](includes/prod_short.md)] lizenziert sein. Sie können Gastkonten nicht in Mehrwertsteuergruppen verwenden.

* Um Mehrwertsteuererklärungen zu berechnen und einzureichen, muss ein Benutzer ein vollständiger [!INCLUDE[prod_short](includes/prod_short.md)]-Benutzer sein.
* Sie können sich mit der Teammitglied-Lizenz für [!INCLUDE[prod_long](includes/prod_long.md)] anmelden und grundlegende Aufgaben wie das Erstellen von Konten ausführen.

## <a name="set-up-a-vat-group"></a><a name="set-up-a-vat-group"></a><a name="set-up-a-vat-group"></a>Mehrwertsteuergruppe einrichten

Die folgende ist die empfohlene Reihenfolge der Schritte für einen Administrator zum Einrichten einer Mehrwertsteuergruppe:

1. Erstellen Sie das Setup in [Azure Active Directory für die Gruppenmitglieder](#azure-active-directory-setup-for-group-members).
2. Teilen Sie die technischen Informationen, die Mehrwertsteuergruppen-Mitglieder und die Gruppenvertreter benötigen, um ihre [!INCLUDE[prod_short](includes/prod_short.md)]-Mandanten zu verbinden. Normalerweise verfügt der Gruppenvertreter über diese Informationen, wie z. B. [API URL](#group-api-setup) und den Namen der Umgebung des Mehrwertsteuergruppenvertreters, an den die Mitglieder der Mehrwertsteuergruppe die Mehrwertsteuer übermitteln.
3. Erstellen Sie Benutzer, die Mehrwertsteuergruppenmitglieder verwenden, um sich zu authentifizieren, wenn sie eine Verbindung im [!INCLUDE[prod_short](includes/prod_short.md)] des Vertreters der Mehrwertsteuergruppe herstellen. Die Benutzer müssen über eine Benutzerlizenz mit Vollzugriff auf [!INCLUDE[prod_short](includes/prod_short.md)] verfügen.
4. Führen Sie die Anleitung zur unterstützten Einrichtung **Mehrwertsteuergruppenverwaltung einrichten** aus, um die Mitglieder der Mehrwertsteuergruppe zu verbinden.

   Der Vertreter der MwSt.-Gruppe muss den Gruppenmitgliedern bestimmte Informationen zur Verfügung stellen, um deren Einrichtung abzuschließen. (Erfahren Sie mehr im [Richten Sie MwSt.-Gruppenmitglieder ein](#set-up-vat-group-members) Abschnitt unten.) Notieren Sie sich die **Gruppenmitglieds-ID** für jedes Mitglied der MwSt.-Gruppe. Der Gruppenvertreter benötigt diese IDs, um die Unternehmen der Mehrwertsteuergruppe hinzuzufügen.
5. Richten Sie die Erweiterung „Mehrwertsteuergruppenverwaltung“ im [!INCLUDE[prod_short](includes/prod_short.md)] des Mehrwertsteuergruppen-Vertreters ein, indem Sie die Anleitung zur unterstützten Einrichtung **Mehrwertsteuergruppenverwaltung einrichten** verwenden.

> [!NOTE]
> Um eine Verbindung zum Vertreter der Mehrwertsteuergruppe herzustellen, müssen Gruppenmitglieder über ein Benutzerkonto mit Zugriff auf das [!INCLUDE[prod_short](includes/prod_short.md)] des Mehrwertsteuergruppenvertreters verfügen. Der Umsatzsteuer-Gruppenvertreter muss dafür mindestens einen Benutzer anlegen. Aus Sicherheitsgründen empfehlen wir jedoch, dass sie für jedes Mitglied der Mehrwertsteuergruppe einen Benutzer erstellen, der ein Systembenutzerkonto sein kann, das nicht mit einer tatsächlichen Person verbunden ist. Stellen Sie sicher, dass Sie die Anmeldeinformationen der Benutzer auf sichere Weise an Mehrwertsteuergruppenmitglieder verteilen.

### <a name="azure-active-directory-setup-for-group-members"></a><a name="azure-active-directory-setup-for-group-members"></a><a name="azure-active-directory-setup-for-group-members"></a>Azure Active Directory Einrichtung für Gruppenmitglieder

Wenn der Vertreter der Mehrwertsteuergruppe [!INCLUDE[prod_short](includes/prod_short.md)] online oder lokal verwendet, müssen Mehrwertsteuergruppenmitglieder Azure Active Directory verwenden, um Benutzer zu authentifizieren, wenn sie Mehrwertsteuererklärungen an den Vertreter der Mehrwertsteuergruppe übermitteln. Für [!INCLUDE[prod_short](includes/prod_short.md)]-On-premises müssen Mitglieder Single Sign-On konfigurieren. Erfahren Sie mehr unter [Azure Active Directory-Authentifizierung mit WS-Fedeation konfigurieren](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory?tabs=singletenant%2Cadmintool).

Wenn die Mehrwertsteuergruppenmitglieder ebenfalls [!INCLUDE[prod_short](includes/prod_short.md)] online verwenden, kann sich das Mitglied mit den angegebenen Benutzeranmeldeinformationen und der Anmeldeinformationen authentifizieren, die vom Gruppensprecher bereitgestellt werden. Erfahren Sie mehr im [Richten Sie MwSt.-Gruppenmitglieder ein](#set-up-vat-group-members) Abschnitt unten.

Mehrwertsteuergruppenmitglieder, die [!INCLUDE[prod_short](includes/prod_short.md)] lokal haben, müssen eine App-Registrierung in Azure Active Directory für den [!INCLUDE[prod_short](includes/prod_short.md)]-Mandanten des Vertreters der Mehrwertsteuergruppe einrichten. Die App-Registrierung ermöglicht es, dass mit [!INCLUDE[prod_short](includes/prod_short.md)] online des Mehrwertsteuergruppenvertreters das Gruppenmitglied authentifiziert werden kann. Erfahren Sie mehr unter [Schnellstart: Registrieren einer Anwendung mit der Microsoft-Identitätsplattform](/azure/active-directory/develop/quickstart-register-app).

Wenn der Administrator des Mitglieds der Mehrwertsteuergruppe die App-Registrierung in Azure Active Directory erstellt, müssen sie die folgenden Informationen angeben.

* Im Abschnitt **Authentifizierung** fügen Sie **Web** als Plattform hinzu und verwenden die folgende **Umleitungs-URL**: `https://businesscentral.dynamics.com/OAuthLanding.htm`.
* Im Abschnitt **Authentifizierung** in der Option zur Auswahl **Unterstützte Kontoarten** wählen Sie **Konten in einem beliebigen Organisationsverzeichnis (Beliebiges Azure AD-Verzeichnis – mandantenfähig)**.
* Im Abschnitt **Zertifikate und Geheimschlüssel** erstellen Sie einen neuen geheimen Clientschlüssel und notieren den Wert. Die Mehrwertsteuergruppenmitglieder benötigen den Geheimschlüssel, wenn Sie die Verbindung zum Gruppenvertreter einrichten.
* Im Abschnitt **API-Berechtigungen** fügen Sie Berechtigungen zu [!INCLUDE[prod_short](includes/prod_short.md)] hinzu. Aktivieren Sie den stellvertretenden Zugriff auf **Financials.ReadWrite.All** und **user_impersonation**.
* Im Abschnitt **Übersicht** notieren Sie die **Anwendungs-(Client)-ID**. Die Mehrwertsteuergruppenmitglieder benötigen die ID, wenn Sie die Verbindung zum Gruppenvertreter einrichten.

### <a name="group-api-setup"></a><a name="group-api-setup"></a><a name="group-api-setup"></a>Einrichtung der Gruppen API

Der Vertreter der Mehrwertsteuergruppe erstellt eine API und stellt sie den Gruppenmitgliedern zur Verfügung. Die Mitglieder verwenden diese API, um sich mit dem [!INCLUDE[prod_short](includes/prod_short.md)]-Mandant zu verbinden und Mehrwertsteuererklärungen zu übermitteln. Mehrwertsteuergruppenmitglieder verwenden [!INCLUDE[prod_short](includes/prod_short.md)] häufig in separaten Azure Active Directory-Mandanten. Deshalb sind weitere Einrichtungsvorgänge erforderlich, um das Mehrwertsteuergruppenmitglied mit dem [!INCLUDE[prod_short](includes/prod_short.md)] des Vertreters zu verbinden.

> [!NOTE]
> Für diese Einrichtung sind die Anmeldeinformationen für ein Administratorbenutzerkonto mit Vollzugriff auf [!INCLUDE[prod_short](includes/prod_short.md)] erforderlich.

1. Wählen Sie im Business Central Admin Center für den Mandanten des Vertreters die Registerkarte **Umgebungen** aus.
1. Wählen Sie die Umgebung des Vertreters aus.
1. Kopieren Sie die **URL** im Abschnitt **Details**.
1. Öffnen Sie Notepad, und fügen Sie die URL ein. Ersetzen `https://businesscentral.dynamics.com` mit `https://api.businesscentral.dynamics.com/v2.0`.

## <a name="set-up-vat-group-members"></a><a name="set-up-vat-group-members"></a><a name="set-up-vat-group-members"></a>Mehrwertsteuergruppenmitglieder einrichten

Mitglieder der Mehrwertsteuergruppe stellen eine Verbindung zum Vertreter her, indem sie einen Webdienst im Mandanten des Mehrwertsteuergruppen-Vertreters aufrufen. Der Aufrufer muss mithilfe von OAuth2 authentifiziert sein. Wenn die Erweiterung „Mehrwertsteuergruppenverwaltung“ eingerichtet ist, werden Mitglieder aufgefordert, sich beim Vertreter der Mehrwertsteuergruppe zu authentifizieren, während ein Zugriffstoken abgerufen und zu gespeichert wird. Dieses Zugriffstoken wird verwendet, wenn Mehrwertsteuererklärungen an den Vertreter der Mehrwertsteuergruppe gesendet werden.

> [!IMPORTANT]
> Die Mitgliedsunternehmen in der Mehrwertsteuergruppe müssen sich nicht mit HMRC verbinden, da sie über den Vertreter der Gruppe berichten.

Bevor die Mitglieder der MwSt.-Gruppe ihre Einrichtung beginnen (unten aufgeführt), müssen sie sich an den Vertreter der MwSt.-Gruppe wenden, um die folgenden Informationen zu ihrem [!INCLUDE[prod_short](includes/prod_short.md)] Mandanten zu erhalten:

* Die API-URL
* Der Name seines Unternehmens
* Anmeldeinformationen für den dedizierten Benutzer

1. Wählen Sie in der oberen rechten Ecke **Einstellungen** ![Einstellungen.](media/ui-experience/settings_icon_small.png "Einstellungssymbol für Rollenzentrum") Symbol, und dann wählen Sie die Aktion **Unterstützte Einrichtung**.
2. Wählen Sie die **Mehrwertsteuergruppenverwaltung einrichten**-Aktion aus.
3. In dem Feld **Rolle der Mehrwertsteuergruppe** wählen **Mitglied** dann **Nächste**.
4. Kopieren Sie den Wert des Felds **Gruppenmitglieds-ID**, und telen Sie ihn dann mit dem Vertreter der Mehrwertsteuergruppe, damit dieser Ihr Unternehmen als genehmigtes Mitglied der Gruppe hinzufügen kann.
5. Geben Sie im Feld **Produktversion des Gruppenvertreters** die Version von [!INCLUDE[prod_short](includes/prod_short.md)] an, die der Vertreter verwendet.
6. Im Feld **API URL** geben Sie die vom Vertreter der Mehrwertsteuergruppe angegebene API URL ein. Normalerweise ist die URL wie folgt formatiert: `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Zum Beispiel, `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative`.
7. Geben Sie im Feld **Gruppenvertreterunternehmen** den Unternehmensnamen des Vertreters der Mehrwertsteuergruppe ein, z. B. **CRONUS UK Ltd**.
8. Wählen Sie im Feld **Authentifizierungstyp** die Option **OAuth2** aus. Wenn der Vertreter der Mehrwertsteuergruppe [!INCLUDE[prod_short](includes/prod_short.md)] Online verwendet, aktivieren Sie die Option **Gruppenvertreter verwendet Business Central Online** fest, und wählen Sie dann aus **Weiter** aus.

   Befolgen Sie dann die Schritte entweder im [Vertreter der Mehrwertsteuergruppe verwendet Business Central Online](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-online) oder im Abschnitt [Vertreter der Mehrwertsteuergruppe verwendet Business Central-On-Premises](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-on-premises).

### <a name="vat-group-representative-uses-business-central-online"></a><a name="vat-group-representative-uses-business-central-online"></a><a name="vat-group-representative-uses-business-central-online"></a>Vertreter der Mehrwertsteuergruppe verwendet Business Central Online

1. Geben Sie die Benutzeranmeldeinformationen ein, die vom Vertreter der Mehrwertsteuergruppe bereitgestellt wurden, und fügen Sie die erforderlichen Berechtigungen hinzu, um das Zugriffstoken zu generieren.
2. Wählen Sie die MwSt.-Berichtskonfiguration aus, die Sie verwenden, um MwSt.-Erklärungen an die Steuerbehörden in Großbritannien zu übermitteln. 

Nachdem Sie die Einrichtung abgeschlossen haben, erstellt [!INCLUDE[prod_short](includes/prod_short.md)] basierend auf dieser Auswahl, mit der Sie die Mehrwertsteuererklärungen an den Vertreter der Mehrwertsteuergruppe übermitteln können.

### <a name="vat-group-representative-uses-business-central-on-premises"></a><a name="vat-group-representative-uses-business-central-on-premises"></a><a name="vat-group-representative-uses-business-central-on-premises"></a>Vertreter der Mehrwertsteuergruppe verwendet Business Central-On-Premises

1. Geben Sie die vom Vertreter der MwSt.-Gruppe bereitgestellten Benutzerdaten ein und wählen Sie **Nächste**.
2. Geben Sie im Feld **Client ID** die Client-ID aus der App-Registrierung in [Azure Active Directory](#azure-active-directory-setup-for-group-members) ein.
3. Geben Sie im Feld **Geheimer Clientschlüssel** den geheimen Clientschlüssel aus der App-Registrierung in Azure Active Directory ein.
4. Geben Sie im Feld **OAuth 2.0-Autoritätsendpunkt** `https://login.microsoftonline.com/common/oauth2` ein.
5. Geben Sie im Feld **OAuth 2.0-Ressourcen-URL** `https://api.businesscentral.dynamics.com/` ein.
6. Geben Sie im Feld **OAuth 2.0-Umleitungs-URL** `https://businesscentral.dynamics.com/OAuthLanding.htm` ein.
7. Wenn Sie die verschiedenen Felder festgelegt haben, wählen Sie **Nächste**, und bestätigen Sie dann die Authentifizierungsverbindung, um das Zugriffstoken zu generieren.
8. Wählen Sie die MwSt.-Berichtskonfiguration aus, die Sie verwenden, um MwSt.-Erklärungen an die Steuerbehörden in Großbritannien zu übermitteln.

## <a name="set-up-the-vat-group-representative"></a><a name="set-up-the-vat-group-representative"></a><a name="set-up-the-vat-group-representative"></a>Vertreter der Mehrwertsteuergruppe einrichten

> [!NOTE]
> Für die lokale Version [!INCLUDE[prod_short](includes/prod_short.md)] wird nur eine einzelne Mandanteninstanz des Gruppenvertreters unterstützt.

> [!IMPORTANT]
> Das Unternehmen des Vertreters muss die Serviceverbindung für **HMRC-VAT-Einrichtung** auf der Seite **Dienstverbindungen** aktivieren. Vertreter müssen auch die Perioden für die Umsatzsteuererklärung von HMRC herunterladen.

1. Wählen Sie in der oberen rechten Ecke das Symbol **Einstellungen** ![Einstellungen.](media/ui-experience/settings_icon_small.png "Einstellungssymbol für Rollenzentrum") und dann die Aktion **Unterstützte Einrichtung**.
2. Wählen Sie die **Mehrwertsteuergruppenverwaltung einrichten**-Aktion aus.
3. In dem **Rolle der Mehrwertsteuergruppe** Feld, wählen **Vertreter** als Vertreter der MwSt.-Gruppe fungieren möchten, und wählen Sie dann **Nächste**.
4. Geben Sie im Feld **Gruppenabrechnungskonto** das Abrechnungskonto an, das für die Mehrwertsteuerbeträge der Gruppenmitglieder verwendet wird. Dieses Konto sollte **Anlagen** als **Kontokategorie** haben.
5. Geben Sie im Feld **MwSt.-Ausgleichskontos** das Konto an, das Sie für MwSt.-Abrechnungen verwenden. Dieses Konto sollte **Verbindlichkeiten** als **Kontokategorie** haben.
6. Geben Sie im Feld **MwSt. fällig Feldnr.** das Feld an, das den gesamten fälligen MwSt.-Betrag aus einer MwSt.-Gruppenübermittlung darstellt.
7. Geben Sie im Feld **Fibu Buch.-Blattvorlage „Gruppenausgleich“** die Fibu Buch.-Blattvorlage an, die für die Erstellung des Belegs verwendet wird, mit dem der Gruppenvertreter die Gruppenmehrwertsteuer auf das Ausgleichskonto buchen kann.
8. Das Feld **Genehmigte Mitglieder** Feld zeigt die Anzahl der Gruppenmitglieder, die eingerichtet werden, um Umsatzsteuererklärungen an den Gruppenvertreter zu übermitteln. Um neue Mitglieder hinzuzufügen, wählen Sie die Nummer zum Öffnen der Seite **VGenehmigte Mitglieder der MwSt.-Gruppe** aus:
    1. Geben Sie im Feld **Gruppenmitglieds-ID** eine Kennung für das Gruppenmitglied ein, wie sie während der Einrichtung des Gruppenmitglieds angezeigt wird (weitere Informationen finden Sie in der [Einrichtung von MwSt.-Gruppenmitgliedern](#set-up-vat-group-members) Abschnitt oben).
    2. Geben Sie im Feld **Gruppenmitgliedsname** den Namen des Gruppenmitglieds an.
    3. Geben Sie im Feld **Unternehmen** an, das Unternehmen, von dem aus das Gruppenmitglied Mehrwertsteuererklärungen in [!INCLUDE[prod_short](includes/prod_short.md)], z. B., **CRONUS UK Ltd**.
    4. Gibt die Kontaktdetails für das Unternehmen an.

## <a name="use-the-vat-group-management-features"></a><a name="use-the-vat-group-management-features"></a><a name="use-the-vat-group-management-features"></a>Die Funktionen der Mehrwertsteuergruppenverwaltung verwenden

Mehrwertsteuergruppenmitglieder verwenden die Standardprozesse, um Mehrwertsteuererklärungen zu erstellen. Der einzige Unterschied besteht darin, dass Mitglieder die **VATGROUP** Berichtversion, wodurch die Seite **Mehrwertsteuererklärung** an den Vertreter der Mehrwertsteuergruppe und nicht an die Behörden übermittelt wird. Erfahren Sie mehr unter [Über den Umsatzsteuererklärungsbericht](finance-how-report-vat.md#vatreturn).

> [!NOTE]
> Mitglieder der Mehrwertsteuergruppe können übermittelte Mehrwertsteuererklärungen korrigieren, solange der Gruppenvertreter die Mehrwertsteuererklärung für die Gruppe noch nicht herausgegeben hat. Um eine Korrektur vorzunehmen, muss das Mitglied der Mehrwertsteuergruppe eine neue Mehrwertsteuererklärung für den Zeitraum der Mehrwertsteuererklärung erstellen und diese dem Vertreter der Mehrwertsteuergruppe übermitteln. Auf der Seite des Vertreters der Mehrwertsteuergruppe wird die vorherige Mehrwertsteuererklärung des Mitgliedes durch die vorherige ersetzt und auf der Seite **Mehrwertsteuererklärungen** eingefügt.

In den folgenden Abschnitten werden die Aufgaben beschrieben, die Vertreter von Mehrwertsteuergruppen ausführen müssen, um eine Mehrwertsteuererklärung des Gruppe einzureichen.

### <a name="review-vat-member-submissions"></a><a name="review-vat-member-submissions"></a><a name="review-vat-member-submissions"></a>Mehrwertsteuergruppenmitglied-Übermittlungen prüfen

Auf der Seite **Übermittlungen der Mehrwertsteuergruppe** werden die von Mitgliedern übermittelten Mehrwertsteuererklärungen aufgelistet. Die Seite dient als Entwurfsspeicherort für die Übermittlungen, bis der Vertreter der Mehrwertsteuergruppe sie in eine Mehrwertsteuererklärung für die Gruppe einbezieht. Der Vertreter kann die Übermittlungen öffnen, um die Mehrwertsteuer für die einzelnen von jedem Mehrwertsteuergruppenmitglied gemeldeten Felder zu überprüfen.

> [!TIP]
> Auf der Seite **MwSt.-Rückgabezeitraum** wird im Feld **Gruppenmitglied-Übermittlungen** angezeigt, wie viele Mehrwertsteuererklärunge Mitglieder übermittelt haben. Um sicherzustellen, dass diese Zahl aktuell ist, wählen Sie die Aktion **MwSt.-Rückgabezeiträume abrufen** aus.

### <a name="create-a-group-vat-return"></a><a name="create-a-group-vat-return"></a><a name="create-a-group-vat-return"></a>Erstellen einer Gruppenmehrwertsteuererklärung

Um die Mehrwertsteuer für die Gruppe zu melden, erstellen Sie auf der Seite **Mehrwertsteuererklärungen** eine Mehrwertsteuererklärung nur für Ihr Unternehmen. Fügen Sie anschließend die neuesten Mehrwertsteuerübermittlungen von Mehrwertsteuergruppenmitgliedern ein, indem Sie die Aktion **Gruppenmehrwertsteuer einschließen** wählen.  

Wenn die Mehrwertsteuererklärung des Vertreters der Gruppe den Behörden übermittelt wurde, führt der Verteter normalerweise die Aktion **MwSt.-Abrechnung berechnen und buchen** aus. Die Aktion schließt offene MwSt.-Posten und überträgt Beträge zum MwSt.-Abrechnungskonto. Derzeit werden bei dieser Aktion die Gruppenübermittlungen nicht berücksichtigt. Es werden nur die MwSt.-Posten des Unternehmens des Vertreters der Mehrwertsteuergruppe gebucht. Die Übermittlungsbeträge der Mehrwertsteuergruppenmitglieder müssen manuell zum MwSt.-Abrechnungsetrag hinzugebucht werden, damit das MwSt.-Abrechnungskonto des Vertreters der Mehrwertsteuergruppe die Verbindlichkeit dessen, was an die Behörden gemeldet wurde, widerspiegelt. Dieses Verhalten wird sich in einem bevorstehenden Update von [!INCLUDE[prod_short](includes/prod_short.md)] ändern, sodass die gesamte Gruppenmehrwertsteuer (der Gesamtbetrag der Berichtszeilen in der Mehrwertsteuererklärung) ausgeglichen wird.

> [!IMPORTANT]
> Die Mehrwertsteuergruppenfunktionalität wird nur in den Märkten unterstützt, in denen [!INCLUDE[prod_short](includes/prod_short.md)] einen Mehrwertsteuerrahmen verwendet, der aus Mehrwertsteuererklärungen und Umsatzsteuererklärungsperioden besteht. Sie können Mehrwertsteuergruppen nicht in anderen Märkten verwenden, in denen die lokale Mehrwertsteuerberichterstattung anders implementiert ist, z. B. in Österreich, Deutschland, Italien, Spanien und der Schweiz.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Siehe auch

[Lokale Funktionalität für Großbritannien in der britischen Version](LocalFunctionality/unitedkingdom/united-kingdom-local-functionality.md)  
[Making Tax Digital im Vereinigten Königreich](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md)  
[Arbeiten mit MwSt im Verkauf und Einkauf](finance-work-with-vat.md)  
[Mehrwertsteuer einrichten](finance-setup-vat.md)  
[Arbeiten mit MwSt im Verkauf und Einkauf](finance-work-with-vat.md)  
[Konsolidieren von Finanzdaten aus mehreren Unternehmen](finance-consolidated-company-reporting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
