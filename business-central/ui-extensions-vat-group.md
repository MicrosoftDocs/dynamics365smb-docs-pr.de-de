---
title: Die MwSt.-Gruppenverwaltungserweiterung für das Vereinigte Königreich
description: Sie können sich mit anderen Unternehmen zusammenschließen, um eine Mehrwertsteuergruppe zu bilden, in der alle Mitglieder die Mehrwertsteuer in einer einzigen Erklärung melden.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, value added tax, report
ms.search.forms: ''
ms.date: 05/24/2022
ms.author: bholtorf
ms.openlocfilehash: c5757a78a44e3cdc2f6100c42b5105734928837b
ms.sourcegitcommit: 7a6efcbae293c024ca4f6622c82886decf86c176
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/02/2022
ms.locfileid: "8841920"
---
# <a name="the-vat-group-management-extension-for-the-united-kingdom"></a>Die MwSt.-Gruppenverwaltungserweiterung für das Vereinigte Königreich

Sie können ein oder mehrere Unternehmen in Ihrem Land verbinden, um die Mehrwertsteuerberichterstattung unter einer einzigen Registrierungsnummer zu kombinieren. Diese Art der Anordnung ist bekannt als *Mehrwertsteuergruppe*. Sie können mit der Gruppe als Mitglied oder als Gruppenvertreter zusammenarbeiten.

## <a name="forming-a-vat-group"></a>Bildung einer Mehrwertsteuergruppe
Mehrwertsteuergruppenmitglieder und der Gruppenvertreter können die Anleitung zur unterstützten Einrichtung für die **Mehrwertsteuergruppen-Verwaltungseinrichtung** verwenden, um ihre Zusammenarbeit mit der Gruppe zu definieren und eine Verbindung zwischen ihren [!INCLUDE[prod_short](includes/prod_short.md)]-Mandanten zu erstellen. Die Gruppenmitglieder verwenden die Verbindung, um ihre Mehrwertsteuererklärung an den Gruppenvertreter zu senden. Der Vertreter verwendet eine einzelne MwSt.-Rückgabe, um die Mehrwertsteuer an die Steuerbehörden für die Gruppe zu übermitteln. 

## <a name="license-requirements"></a>Lizenzanforderungen
Die Teilnehmer der Gruppe müssen für die Verwendung von [!INCLUDE[prod_short](includes/prod_short.md)] lizenziert sein. Sie können Gastkonten nicht in Mehrwertsteuergruppen verwenden. 

* Um Mehrwertsteuererklärungen zu berechnen und einzureichen, muss ein Benutzer ein vollständiger Business Central-Benutzer sein.
* Sie können sich mit der Teammitglied-Lizenz für Dynamics 365 Business Central anmelden und grundlegende Aufgaben wie das Erstellen von Konten ausführen.

## <a name="vat-group-constellations"></a>Mehrwertsteuergruppenkonstellationen
Die Kommunikation erfolgt von den Gruppenmitgliedern mit dem Vertreter. Der Gruppenvertreter stellt eine API-URL zur Verfügung, mit der die Mitglieder ihre Mehrwertsteuererklärungen an den Vertreter der Mehrwertsteuergruppe übermitteln können. 
[!INCLUDE[prod_short](includes/prod_short.md)] unterstützt die Übermittlung von Mehrwertsteuererklärungen innerhalb der Gruppe bei Unternehmen, die [!INCLUDE[prod_short](includes/prod_short.md)] lokal oder online verwenden oder irgendeine Kombination davon. Die Einrichtung der Kommunikation hängt von der Konstellation ab. Dieser Artikel beschreibt verschiedene Gruppenkonstellationen.

Die folgende Liste zeigt die empfohlene Reihenfolge der Schritte zum Einrichten einer Mehrwertsteuergruppe:

1. Erstellen Sie die Einrichtung in Azure Active Directory. Weitere Informationen finden Sie unter [Anforderungen für die Authentifizierung](ui-extensions-vat-group.md#requirements-for-authentication).
2. Teilen Sie die technischen Informationen, die Mehrwertsteuergruppen-Mitglieder und die Vertreter benötigen, um ihre [!INCLUDE[prod_short](includes/prod_short.md)]-Mandanten zu verbinden. Normalerweise verfügt der Vertreter der Mehrwertsteuergruppe über diese Informationen, wie z. B. den Namen der Umgebung des Mehrwertsteuergruppenvertreters, an den die Mitglieder der Mehrwertsteuergruppe die Mehrwertsteuer übermitteln.
3. Erstellen Sie Benutzer, die Mehrwertsteuergruppenmitglieder verwenden können, um sich zu authentifizieren, wenn sie eine Verbindung im [!INCLUDE[prod_short](includes/prod_short.md)] des Vertreters der Mehrwertsteuergruppe herstellen. Die Benutzer müssen über eine Benutzerlizenz mit Vollzugriff auf [!INCLUDE[prod_short](includes/prod_short.md)] verfügen.
4. Führen Sie die Anleitung zur unterstützten Einrichtung **Mehrwertsteuergruppenverwaltung einrichten** aus, um die Mitglieder der Mehrwertsteuergruppe zu verbinden.

  Für die Anleitung sind einige Informationen vom Vertreter der Mehrwertsteuergruppe erforderlich. Weitere Informationen finden Sie unter [Mehrwertsteuergruppenmitglieder einrichten](#set-up-vat-group-members). Notieren Sie sich die **Gruppenmitglieds-ID** für jedes Mitglied der Mehrwertsteuergruppe. Der Vertreter benötigt diese IDs, um die Unternehmen der Mehrwertsteuergruppe hinzuzufügen.
5. Richten Sie die Erweiterung „Mehrwertsteuergruppenverwaltung“ im [!INCLUDE[prod_short](includes/prod_short.md)] des Mehrwertsteuergruppen-Vertreters ein, indem Sie die Anleitung zur unterstützten Einrichtung **Mehrwertsteuergruppenverwaltung einrichten** verwenden. 

> [!NOTE]
> Um eine Verbindung zum Vertreter der Mehrwertsteuergruppe herzustellen, müssen Gruppenmitglieder über ein Benutzerkonto mit Zugriff auf das [!INCLUDE[prod_short](includes/prod_short.md)] des Mehrwertsteuergruppenvertreters verfügen. Der Vertreter der Mehrwertsteuergruppe muss hierfür mindestens einen Benutzer erstellen. Aus Sicherheitsgründen empfehlen wir jedoch, für jedes Mitglied der Mehrwertsteuergruppe einen Benutzer zu erstellen. Stellen Sie sicher, dass Sie die Anmeldeinformationen für diese Benutzer auf sichere Weise an Mehrwertsteuergruppenmitglieder verteilen. Dies kann ein Systembenutzerkonto sein, das nicht mit einer tatsächlichen Person verbunden ist.

## <a name="about-the-vat-group-management-setup"></a>Info über die Einrichtung der Mehrwertsteuergruppenverwaltung

Der Vertreter der Mehrwertsteuergruppe stellt den Gruppenmitgliedern eine API zur Verfügung. Die Mitglieder verwenden die API, um sich mit dem [!INCLUDE[prod_short](includes/prod_short.md)]-Mandant zu verbinden und Mehrwertsteuererklärungen zu übermitteln. Mehrwertsteuergruppenmitglieder verwenden [!INCLUDE[prod_short](includes/prod_short.md)] häufig in separaten Azure Active Directory-Mandanten. Daher sind weitere Einrichtungsvorgänge erforderlich, um das Mehrwertsteuergruppenmitglied mit dem [!INCLUDE[prod_short](includes/prod_short.md)] des Vertreters zu verbinden. 
  
Mitglieder der Mehrwertsteuergruppe stellen eine Verbindung zum Vertreter her, indem sie einen Webdienst im Mandanten des Mehrwertsteuergruppen-Vertreters aufrufen. Der Aufrufer muss mithilfe von OAuth2 authentifiziert sein. Wenn die Erweiterung „Mehrwertsteuergruppenverwaltung“ eingerichtet ist, werden Sie aufgefordert, sich beim Vertreter der Mehrwertsteuergruppe zu authentifizieren, um einen Zugriffstoken abzurufen und zu speichern. Dieses Zugriffstoken wird verwendet, wenn Mehrwertsteuererklärungen an den Vertreter der Mehrwertsteuergruppe gesendet werden. 

## <a name="construct-the-api-url"></a>Die API-URL erstellen
1. Wählen Sie im Business Central Admin Center für den Mandanten des Vertreters die Registerkarte **Umgebungen** aus.
2. Kopieren Sie die **URL** im Abschnitt **Details**.
3. Öffnen Sie Notepad, und fügen Sie die URL ein. Ersetzen Sie **https://businesscentral.dynamics.com** durch **https://api.businesscentral.dynamics.com/v2.0**.

## <a name="requirements-for-authentication"></a>Voraussetzungen für die Authentifizierung 
> [!NOTE]
> Dazu sind die Anmeldeinformationen für ein Administratorbenutzerkonto mit Vollzugriff auf [!INCLUDE[prod_short](includes/prod_short.md)] erforderlich.

Wenn der Vertreter der Mehrwertsteuergruppe [!INCLUDE[prod_short](includes/prod_short.md)] online oder lokal verwendet, müssen Mehrwertsteuergruppenmitglieder Azure Active Directory verwenden, um Benutzer zu authentifizieren, wenn sie Mehrwertsteuererklärungen an den Vertreter der Mehrwertsteuergruppe übermitteln. Für [!INCLUDE[prod_short](includes/prod_short.md)]-On-premises müssen Mitglieder Single Sign-On konfigurieren. Weitere Informationen finden Sie unter [Azure Active Directory-Authentifizierung mit WS-Fedeation konfigurieren](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory?tabs=singletenant%2Cadmintool). Wenn die Mehrwertsteuergruppenmitglieder ebenfalls [!INCLUDE[prod_short](includes/prod_short.md)] online verwenden, kann sich das Mehrwertsteuergruppenmitglied mithilfe der angegebenen Benutzeranmeldeinformationen und der Endpunktinformationen authentifizieren. Weitere Informationen finden Sie unter [Mehrwertsteuergruppenmitglieder einrichten](ui-extensions-vat-group.md#set-up-vat-group-members).

Mehrwertsteuergruppenmitglieder, die [!INCLUDE[prod_short](includes/prod_short.md)] lokal haben, müssen eine App-Registrierung in Azure Active Directory für den [!INCLUDE[prod_short](includes/prod_short.md)]-Mandanten des Vertreters der Mehrwertsteuergruppe einrichten. Die App-Registrierung ermöglicht es, dass mit [!INCLUDE[prod_short](includes/prod_short.md)] online des Mehrwertsteuergruppenvertreters das Gruppenmitglied authentifiziert werden kann. Weitere Informationen finden Sie unter [Schnellstart: Registrieren einer Anwendung mit der Microsoft-Identitätsplattform](/azure/active-directory/develop/quickstart-register-app).

Wenn Sie die App-Registrierung in Azure Active Directory erstellen, müssen Sie die folgenden Informationen angeben.

* Im Abschnitt **Authentifizierung** fügen Sie **Web** als Plattform hinzu und verwenden die folgende **Umleitungs-URL**: https://businesscentral.dynamics.com/OAuthLanding.htm.
* Im Abschnitt **Authentifizierung** in der Option zur Auswahl **Unterstützte Kontoarten** wählen Sie **Konten in einem beliebigen Organisationsverzeichnis (Beliebiges Azure AD-Verzeichnis – mandantenfähig)**.
* Im Abschnitt **Zertifikate und Geheimschlüssel** erstellen Sie einen neuen geheimen Clientschlüssel und notieren den Wert. Die Mehrwertsteuergruppenmitglieder benötigen den Geheimschlüssel, wenn Sie die Verbindung zum Gruppenvertreter einrichten.
* Im Abschnitt **API-Berechtigungen** fügen Sie Berechtigungen zu [!INCLUDE[prod_short](includes/prod_short.md)] hinzu. Aktivieren Sie den stellvertretenden Zugriff auf **Financials.ReadWrite.All** und **user_impersonation**.
* Im Abschnitt **Übersicht** notieren Sie die **Anwendungs-(Client)-ID**. Die Mehrwertsteuergruppenmitglieder benötigen die ID, wenn Sie die Verbindung zum Gruppenvertreter einrichten. 

## <a name="set-up-vat-group-members"></a>Mehrwertsteuergruppenmitglieder einrichten
> [!IMPORTANT]
> Die Mitgliedsunternehmen in der Mehrwertsteuergruppe müssen sich nicht mit HMRC verbinden, da sie über den Vertreter der Gruppe berichten.

Bevor Sie beginnen, wenden Sie sich an den Vertreter der Mehrwertsteuergruppe für die folgenden Informationen über seinen [!INCLUDE[prod_short](includes/prod_short.md)]-Mandanten:

* Die API-URL
* Der Name seines Unternehmens 
* Client-ID
* Geheimer Clientschlüssel
* Anmeldeinformationen für den dedizierten Benutzer 

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **MwSt.-Gruppenverwaltung einrichten** ein, und wählen Sie dann den entsprechenden Link aus.
2. Geben Sie im Feld **MwSt.-Gruppenrolle** an, ob Sie ein Mitglied der Gruppe oder der Vertreter der Gruppe sind. Wählen Sie **Mitglied** aus, um als Gruppenmitglied zu fungieren und die Mehrwertsteuererklärungen an den Gruppenvertreter anstatt an die Steuerbehörde zu übermitteln, und wählen Sie dann **Weiter** aus.
3. Kopieren Sie den Wert des Felds **Gruppenmitglieds-ID**, und telen Sie ihn dann mit dem Vertreter der Mehrwertsteuergruppe, damit dieser Ihr Unternehmen als genehmigtes Mitglied der Gruppe hinzufügen kann.
4. Geben Sie im Feld **Produktversion des Gruppenvertreters** die Version von [!INCLUDE[prod_short](includes/prod_short.md)] an, die der Vertreter verwendet.
5. Geben Sie im Feld **Gruppenvertreterunternehmen** den Unternehmensnamen des Vertreters der Mehrwertsteuergruppe ein. Zum Beispiel **CRONUS UK Ltd**.
6. Wählen Sie im Feld **Authentifizierungstyp** die Option **OAuth2** aus. Wenn der Vertreter der Mehrwertsteuergruppe [!INCLUDE[prod_short](includes/prod_short.md)] Online verwendet, legen Sie die Option **Gruppenvertreter verwendet Business Central Online** fest, und wählen Sie dann aus **Weiter** aus. Je nachdem, ob der Vertreter [!INCLUDE[prod_short](includes/prod_short.md)] Online oder -On-premises verwendet, befolgen Sie die Schritte im Abschnitt [Vertreter der Mehrwertsteuergruppe verwendet Business Central Online](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-online) oder im Abschnitt [Vertreter der Mehrwertsteuergruppe verwendet Business Central-On-Premises](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-on-premesis).

### <a name="vat-group-representative-uses-business-central-online"></a>Vertreter der Mehrwertsteuergruppe verwendet Business Central Online
1. Geben Sie die Benutzeranmeldeinformationen ein, die vom Vertreter der Mehrwertsteuergruppe bereitgestellt wurden, und fügen Sie die erforderlichen Berechtigungen hinzu.
2. Wählen Sie die MwSt.-Berichtskonfiguration aus, die derzeit verwendet wird, um MwSt.-Erklärungen an die Steuerbehörden zu übermitteln. Nachdem Sie die Einrichtung abgeschlossen haben, erstellt [!INCLUDE[prod_short](includes/prod_short.md)] basierend auf dieser Auswahl eine neue Konfiguration und verwendet die Konfiguration, um Mehrwertsteuererklärungen an den Vertreter der Mehrwertsteuergruppe zu übermitteln.  
3. Fügen Sie die **API-URL** vom Vertreter der Mehrwertsteuergruppe hinzu. Normalerweise ist die URL wie folgt formatiert: `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Zum Beispiel, `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative`.

### <a name="vat-group-representative-uses-business-central-on-premesis"></a>Vertreter der Mehrwertsteuergruppe verwendet Business Central-On-Premises
1. Geben Sie im Feld **Client-ID** die Client-ID aus der App-Registrierung in Azure Active Directory ein.
2. Geben Sie im Feld **Geheimer Clientschlüssel** den geheimen Clientschlüssel aus der App-Registrierung in Azure Active Directory ein.
3. Geben Sie im Feld **OAuth 2.0-Autoritätsendpunkt** `https://login.microsoftonline.com/common/oauth2` ein.
4. Geben Sie im Feld **OAuth 2.0-Ressourcen-URL** `https://api.businesscentral.dynamics.com/` ein.
5. Geben Sie im Feld **OAuth 2.0-Umleitungs-URL** `https://businesscentral.dynamics.com/OAuthLanding.htm` ein.
6. Wenn Sie die verschiedenen Felder angegeben haben, wählen Sie **Weiter** und geben Sie dann die Benutzeranmeldeinformationen ein, die vom Vertreter der Mehrwertsteuergruppe bereitgestellt wurden.
7. Wählen Sie die MwSt.-Berichtskonfiguration aus, die Sie verwenden, um die Mehrwertsteuer den Behörden in Ihrem Land zu melden.

## <a name="set-up-the-vat-group-representative"></a>Vertreter der Mehrwertsteuergruppe einrichten
> [!NOTE]
> Für die lokale Version wird nur eine einzelne Mandanteninstanz des Gruppenvertreters unterstützt.

> [!IMPORTANT]
> Das Unternehmen des Vertreters muss die Serviceverbindung für **HMRC-VAT-Einrichtung** auf der Seite **Dienstverbindungen** aktivieren. Vertreter müssen auch die Perioden für die Umsatzsteuererklärung von HMRC herunterladen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **MwSt.-Gruppenverwaltung einrichten** ein, und wählen Sie dann den entsprechenden Link aus.
2. Geben Sie im Feld **MwSt.-Gruppenrolle** an, ob Sie ein Mitglied der Gruppe oder der Vertreter der Gruppe sind. Wählen Sie den **Vertreter** aus, der als Vertreter der Mehrwertsteuergruppe fungieren soll, übermitteln Sie die Mehrwertsteuererklärungen an die Steuerbehörde für diese Gruppe, und wählen Sie dann **Weiter** aus.
3. Geben Sie im Feld **MwSt.-Ausgleichskontos** das Konto an, das Sie für MwSt.-Abrechnungen verwenden.
4. Geben Sie im Feld **MwSt. fällig Feldnr.** das Feld an, das den gesamten fälligen MwSt.-Betrag aus einer MwSt.-Gruppenübermittlung darstellt.
5. Geben Sie im Feld **Fibu Buch.-Blattvorlage „Gruppenausgleich“** die Fibu Buch.-Blattvorlage an, die für den Beleg verwendet wird, um die Gruppenmehrwertsteuer auf das Ausgleichskonto zu buchen.
6. Das Feld **Genehmigte Mitglieder** Feld zeigt die Anzahl der Gruppenmitglieder, die eingerichtet werden, um Umsatzsteuererklärungen an den Vertreter zu übermitteln. Wählen Sie zum Hinzufügen neuer Mitglieder die Nummer aus, um die Seite **Genehmigte Mitglieder** zu öffnen.
7. Um neue Mitglieder hinzuzufügen, fügen Sie die folgenden Informationen auf der Seite **Genehmigte Mitglieder der MwSt.-Gruppe** aus:
    1. Geben Sie im Feld **Gruppenmitglieds-ID** einen Bezeichner für das Gruppenmitglied ein.
    2. Geben Sie im Feld **Gruppenmitgliedsname** den Namen des Gruppenmitglieds an. 
    3. Geben Sie im Feld **Unternehmen** an, das Unternehmen, von dem aus das Gruppenmitglied Mehrwertsteuererklärungen in [!INCLUDE[prod_short](includes/prod_short.md)] übermittelt. Zum Beispiel **CRONUS UK Ltd**.
    4. Gibt die Kontaktdetails für das Unternehmen an.

## <a name="use-the-vat-group-management-features"></a>Die Funktionen der Mehrwertsteuergruppenverwaltung verwenden
Mehrwertsteuergruppenmitglieder verwenden die Standardprozesse, um Mehrwertsteuererklärungen zu erstellen. Der einzige Unterschied ist die Auswahl der Berichtsversion **MEHRWERTSTEUERGRUPPE**, wodurch die Mehrwertsteuererklärung an den Vertreter der Mehrwertsteuergruppe und nicht an die Behörden übermittelt wird. Weitere Informationen finden Sie unter [Informationen zum MwSt.-Rückgabebericht](finance-how-report-vat.md#vatreturn).

In den folgenden Abschnitten werden die Aufgaben beschrieben, die Vertreter von Mehrwertsteuergruppen ausführen müssen.

### <a name="vat-group-submissions"></a>Übermittlungen der MwSt.-Gruppe

Auf der Seite **Übermittlungen der Mehrwertsteuergruppe** werden die von Mitgliedern übermittelten Mehrwertsteuererklärungen aufgelistet. Die Seite dient als Entwurfsspeicherort für die Übermittlungen, bis der Vertreter der Mehrwertsteuergruppe sie in eine Mehrwertsteuererklärung für die Gruppe einbezieht. Sie können die Übermittlungen öffnen, um die Mehrwertsteuer für die einzelnen vom Mehrwertsteuergruppenmitglied gemeldeten Felder zu überprüfen. 

> [!TIP]
> Auf der Seite **MwSt.-Rückgabezeitraum** wird im Feld **Gruppenmitglied-Übermittlungen** angezeigt, wie viele Mehrwertsteuererklärunge Mitglieder übermittelt haben. Um sicherzustellen, dass diese Zahl aktuell ist, wählen Sie die Aktion **MwSt.-Rückgabezeiträume abrufen** aus.

### <a name="creating-a-group-vat-return"></a>Erstellen einer Gruppenmehrwertsteuererklärung

Um die Mehrwertsteuer für die Gruppe zu melden, erstellen Sie auf der Seite **Mehrwertsteuererklärungen** eine Mehrwertsteuererklärung nur für Ihr Unternehmen. Fügen Sie anschließend die neuesten Mehrwertsteuerübermittlungen von Mehrwertsteuergruppenmitgliedern ein, indem Sie die Aktion **Gruppenmehrwertsteuer einschließen** wählen.  

Wenn die Mehrwertsteuererklärung des Vertreters der Mehrwertsteuergruppe den Behörden im Auftrag der gesamten Gruppe übermittelt wurde, führen Sie normalerweise die Aktion **MwSt.-Abrechnung berechnen und buchen** aus. Die Aktion schließt offene MwSt.-Posten und überträgt Beträge zum MwSt.-Abrechnungskonto. Derzeit werden bei dieser Aktion die Gruppenübermittlungen nicht berücksichtigt. <!--Has this changed?--> Es werden nur die MwSt.-Posten des Unternehmens des Vertreters der Mehrwertsteuergruppe gebucht. Die Übermittlungsbeträge der Mehrwertsteuergruppenmitglieder müssen manuell zum MwSt.-Abrechnungsetrag hinzugebucht werden, damit das MwSt.-Abrechnungskonto des Vertreters der Mehrwertsteuergruppe die Verbindlichkeit dessen, was an die Behörden gemeldet wurde, widerspiegelt. Dieses Verhalten wird sich in einem bevorstehenden Update von [!INCLUDE[prod_short](includes/prod_short.md)] ändern, sodass die gesamte Gruppenmehrwertsteuer (der Gesamtbetrag der Berichtszeilen in der Mehrwertsteuererklärung) ausgeglichen wird. <!--Has this behavior changed?-->

> [!NOTE]
> Mitglieder der Mehrwertsteuergruppe können übermittelte Mehrwertsteuererklärungen korrigieren, solange der Gruppenvertreter die Mehrwertsteuererklärung für die Gruppe noch nicht herausgegeben hat. Um eine Korrektur vorzunehmen, muss das Mitglied der Mehrwertsteuergruppe eine neue Mehrwertsteuererklärung für den Zeitraum der Mehrwertsteuererklärung erstellen und diese dem Vertreter der Mehrwertsteuergruppe übermitteln. Auf der Seite des Vertreters der Mehrwertsteuergruppe wird die aktuellste Mehrwertsteuererklärung auf der Seite **Mehrwertsteuererklärungen** eingefügt. 

> [!IMPORTANT]
> Die Mehrwertsteuergruppenfunktionalität wird nur in den Märkten unterstützt, in denen [!INCLUDE[prod_short](includes/prod_short.md)] einen Mehrwertsteuerrahmen verwendet, der aus Mehrwertsteuererklärungen und Umsatzsteuererklärungsperioden besteht. Sie können Mehrwertsteuergruppen nicht in anderen Märkten verwenden, in denen die lokale Mehrwertsteuerberichterstattung anders implementiert ist, z. B. in Österreich, Deutschland, Italien, Spanien und der Schweiz. 

## <a name="see-also"></a>Siehe auch
[Lokale Funktionalität für Großbritannien in der britischen Version](LocalFunctionality/unitedkingdom/united-kingdom-local-functionality.md)  
[Making Tax Digital im Vereinigten Königreich](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md)  
[Arbeiten mit MwSt im Verkauf und Einkauf](finance-work-with-vat.md)  
[Mehrwertsteuer einrichten](finance-setup-vat.md)  
[Arbeiten mit MwSt im Verkauf und Einkauf](finance-work-with-vat.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
