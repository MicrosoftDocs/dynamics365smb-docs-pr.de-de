---
title: Verbinden mit Common Data Service | Microsoft Docs
description: Sie können über Common Data Service andere Apps in Business Central integrieren.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 51f04f690483fd5b0c3f093ac5f8e2694ca3fdd9
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924628"
---
# <a name="connect-to-common-data-service"></a>Mit Common Data Service verbinden

In diesem Thema wird beschrieben, wie Sie eine Verbindung zwischen [!INCLUDE[d365fin](includes/d365fin_md.md)]und [!INCLUDE[cds_long_md](includes/cds_long_md.md)] einrichten. Typischerweise stellen Unternehmen die Verbindung her, um Daten mit einer anderen Dynamics 365-Geschäftsanwendung, z. B. [!INCLUDE[crm_md](includes/crm_md.md)], zu integrieren und zu synchronisieren.  

## <a name="before-you-start"></a>Bevor Sie beginnen

Sie müssen einige Informationen bereithalten, bevor Sie die Verbindung herstellen:  

* Die URL für die [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Umgebung, mit der Sie eine Verbindung herstellen möchten. Wenn Sie die Aktion **CDS Verbindungseinrichtung** unterstützte Einrichtungsanleitung verwenden, um die Verbindung herzustellen, werden wir Ihre Umgebungen ermitteln, aber Sie können auch die URL einer anderen Umgebung in Ihrem Mandant eingeben.  
* Der Benutzername und das Passwort eines Kontos, das über Administratorberechtigungen in [!INCLUDE[d365fin](includes/d365fin_md.md)] und [!INCLUDE[cds_long_md](includes/cds_long_md.md)] verfügt.  

> [!Note]
> Diese Schritte beschreiben das Verfahren der Onlineversion von [!INCLUDE[d365fin](includes/d365fin_md.md)].
> Wenn Sie Business Central vor Ort verwenden und die Verbindung mit [!INCLUDE [cds_long_md](includes/cds_long_md.md)] nicht mit dem Azure Active Directory-Konto herstellen, müssen Sie außerdem einen Benutzernamen und ein Kennwort eines Benutzerkontos für die Integration angeben. Dieses Konto wird als „Integrationsbenutzer“-Konto bezeichnet. Wenn Sie ein Azure Active Directory-Konto verwenden, ist das Integrationsbenutzerkonto weder erforderlich noch wird es angezeigt. Der Integrationsbenutzer wird automatisch eingerichtet und benötigt keine Lizenz.

## <a name="set-up-a-connection-to-cds_long_md"></a>Eine Verbindung mit [!INCLUDE[cds_long_md](includes/cds_long_md.md)] einrichten

Für alle anderen Authentifizierungstypen als die Microsoft 365-Authentifizierung richten Sie Ihre Verbindung mit [!INCLUDE[cds_long_md](includes/cds_long_md.md)] auf der Seite **CDS-Verbindungseinrichtung** ein. Für die Microsoft 365-Authentifizierung empfehlen wir die Anleitung zum unterstützten Setup **Common Data Service-Verbindung einrichten** . Der Leitfaden erleichtert die Einrichtung der Verbindung und die Festlegung erweiterter Funktionen, z. B. Personenbesitz und Erstsynchronisierung.  

> [!IMPORTANT]
> Während der Einrichtung der Verbindung mit [!INCLUDE[cds_long_md](includes/cds_long_md.md)] wird der Administrator aufgefordert, der registrierten Azure-Anwendung mit dem Namen [!INCLUDE[d365fin](includes/d365fin_md.md)] Integration für [!INCLUDE[cds_long_md](includes/cds_long_md.md)] zu erteilen:
>
> * Die Berechtigung **Auf [!INCLUDE[cds_long_md](includes/cds_long_md.md)] zugreifen** ist erforderlich, damit [!INCLUDE[d365fin](includes/d365fin_md.md)] im Namen des Administrators automatisch einen nicht lizenzierten, nicht interaktiven Benutzer der Anwendung [!INCLUDE[d365fin](includes/d365fin_md.md)] Integration erstellen, diesem Benutzer Sicherheitsrollen zuweisen und [!INCLUDE[d365fin](includes/d365fin_md.md)] Base CDS Integration Solution für [!INCLUDE[cds_long_md](includes/cds_long_md.md)] bereitstellen kann. Diese Berechtigung wird nur einmal beim Einrichten der Verbindung mit [!INCLUDE[cds_long_md](includes/cds_long_md.md)] verwendet.  
> * Die Berechtigung **Vollzugriff auf Dynamics 365 [!INCLUDE[d365fin](includes/d365fin_md.md)]** ist erforderlich, damit automatisch erstellte Benutzer der Anwendung [!INCLUDE[d365fin](includes/d365fin_md.md)] Integration auf [!INCLUDE[d365fin](includes/d365fin_md.md)]-Daten zugreifen können, die synchronisiert werden.  
> * Die Berechtigung **Anmelden und Ihr Profil lesen** ist erforderlich, um zu überprüfen, ob dem Benutzer, der sich anmeldet, tatsächlich die Sicherheitsrolle „Systemadministrator“ in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] zugewiesen ist.  
>
> Durch die Einwilligung im Namen der Organisation berechtigt der Administrator die registrierte Azure-Anwendung mit dem Namen [!INCLUDE[d365fin](includes/d365fin_md.md)] Integration für [!INCLUDE[cds_long_md](includes/cds_long_md.md)], Daten mit automatisch erstellten Anmeldeinformationen des Benutzers der Anwendung [!INCLUDE[d365fin](includes/d365fin_md.md)] zu synchronisieren.

### <a name="to-use-the-set-up-common-data-service-connection-assisted-setup-guide"></a>So verwenden Sie das unterstützte Setup zum Einrichten der Common Data Service-Verbindung

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Unterstützte Einrichtung** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie **Common Data Service-Verbindung einrichten** aus, um das unterstützte Setup zu starten.
3. Füllen Sie die Felder nach Bedarf aus.

### <a name="to-create-or-maintain-the-connection-manually"></a>So erstellen oder pflegen Sie den Link manuell

Die folgende Prozedur beschreibt, wie die Verbindung auf der Seite **CDS-Verbindungsaufbau** manuell eingerichtet wird. Dies ist auch die Seite, auf der Sie Einstellungen für die Integration verwalten.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **CDS-Verbindungsaufbau** ein, und wählen Sie dann den entsprechenden Link.
2. Geben Sie die folgenden Informationen über die Verbindung von [!INCLUDE[d365fin](includes/d365fin_md.md)] mit [!INCLUDE[cds_long_md](includes/cds_long_md.md)] ein.

    |Feld|Beschreibung|
    |-----|-----|
    |**Umgebungs-URL**|Wenn Sie Umgebungen in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] besitzen, werden wir diese für Sie finden, wenn Sie den Einrichtungsleitfaden ausführen. Wenn Sie eine Verbindung zu einer anderen Umgebung in einem anderen Mandanten herstellen möchten, können Sie die Administrator-Zugangsdaten für die Umgebung eingeben, und wir werden diese ermitteln. |
    |**Aktiviert**|Beginnen Sie mit der Verwendung der Integration. Wenn Sie die Verbindung nicht sofort aktivieren, werden die Verbindungseinstellungen gespeichert, aber Benutzer können nicht von [!INCLUDE[d365fin](includes/d365fin_md.md)] aus auf [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Daten zugreifen. Sie können zu dieser Seite zurückkehren und die Verbindung später aktivieren.  |

3. Wählen Sie im Feld **Eigentümermodell** aus, ob eine Team-Entität in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] neue Datensätze oder ein oder mehrere bestimmte Benutzer besitzen soll. Wenn Sie **Person** wählen, müssen Sie jeden Benutzer angeben. Wenn Sie **Team** wählen, wird die Standard-Geschäftseinheit BCI_Company im Feld **Gekoppelte Geschäftseinheit** angezeigt.

    <!--Need to verify the details in this table, are these specific to Sales maybe?-->
    Geben Sie die folgenden erweiterten Einstellungen ein.

    |Feld|Beschreibung|
    |-----|-----|
    |**[!INCLUDE[d365fin](includes/d365fin_md.md)] Benutzer müssen CDS-Benutzern zugeordnet sein**|Wenn Sie das Personenbesitzmodell verwenden, geben Sie an, ob [!INCLUDE[d365fin](includes/d365fin_md.md)]-Benutzerkonten über übereinstimmende Benutzerkonten in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] verfügen müssen. Die **Microsoft 365-Authentifizierungs-E-Mail** des [!INCLUDE[d365fin](includes/d365fin_md.md)]-Benutzers muss mit der **Primären E-Mail** des [!INCLUDE[crm_md](includes/crm_md.md)]-Benutzers identisch sein.<br /><br /> Wenn Sie den Wert auf **Ja** festlegen, werden [!INCLUDE[d365fin](includes/d365fin_md.md)]-Benutzer, die kein zugeordnetes [!INCLUDE[crm_md](includes/crm_md.md)]-Benutzerkonto haben, keine [!INCLUDE[d365fin](includes/d365fin_md.md)]-Integrationsfunktionen auf der Benutzeroberfläche haben. Der Zugriffs auf [!INCLUDE[crm_md](includes/crm_md.md)]-Daten direkt von [!INCLUDE[d365fin](includes/d365fin_md.md)] wird im Auftrag des [!INCLUDE[crm_md](includes/crm_md.md)]-Benutzerkontos ausgeführt.<br /><br /> Wenn Sie den Wert auf **Nein** festlegen, werden alle [!INCLUDE[d365fin](includes/d365fin_md.md)]-Benutzer [!INCLUDE[crm_md](includes/crm_md.md)]-Integrationsfunktionen auf der Benutzeroberfläche haben. Der Zugriffs auf [!INCLUDE[crm_md](includes/crm_md.md)]-Daten wird im Auftrag des [!INCLUDE[crm_md](includes/crm_md.md)]-Verbindungs-(Integrations-)Benutzers ausgeführt.|
    |**Der aktuelle Business Central-Verkäufer ist einem Benutzer zugeordnet**|Gibt an, ob Ihr Benutzerkonto einem Konto ist [!INCLUDE[crm_md](includes/crm_md.md)] zugeordnet ist <!--double check the name of this field-->|

4. Um die Verbindungseinstellungen zu testen, wählen Sie **Verbindung** , und dann **Verbindung testen** .  

    > [!NOTE]  
    > Wenn keine Datenverschlüsselung in [!INCLUDE[d365fin](includes/d365fin_md.md)] aktiviert ist, werden Sie gefragt, ob sie diese aktivieren möchten. Um Datenverschlüsselung zu aktivieren, wählen Sie **Ja** aus, und stellen Sie die erforderlichen Informationen bereit. Anderenfalls wählen Sie **Nein** aus. Sie können die Datenverschlüsselung später aktivieren. Weitere Informationen finden Sie unter [Verschlüsseln von Daten in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) in der Hilfe für Entwickler und die Verwaltung.  

5. Wenn die [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Synchronisierung nicht bereits eingerichtet ist, werden Sie gefragt, ob Sie die Standardsynchronisierungskonfiguration verwenden möchten. Abhängig davon, ob Sie Datensätze in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] und [!INCLUDE[d365fin](includes/d365fin_md.md)] angepasst bleiben sollen, wählen Sie **Ja** oder **Nein** aus.

## <a name="show-me-the-process"></a>Zeig mir den Prozess

Das folgende Video zeigt die Schritte zum Verbinden von [!INCLUDE[d365fin](includes/d365fin_md.md)] und [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. <br>
  
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ArlP]

## <a name="connecting-on-premises-versions"></a>Verbinden von Vor-Ort-Versionen

Sie müssen einige Informationen auf der Seite **Common Data Service-Verbindungseinrichtung** eingeben, um [!INCLUDE[d365fin](includes/d365fin_md.md)] vor Ort mit [!INCLUDE[cds_long_md](includes/cds_long_md.md)] zu verbinden.

Wenn Sie eine Verbindung mit einem Azure Active Directory (Azure AD)-Konto herstellen möchten, müssen Sie eine Anwendung in Azure AD registrieren, die Anwendungs-ID, die geheime Schlüsseltresor-ID und die zu verwendende Umleitungs-URL angeben. Die Umleitungs-URL ist bereits ausgefüllt und sollte für die meisten Installationen funktionieren. Sie müssen Ihre Installation für die Verwendung von HTTPS einrichten. Weitere Informationen finden Sie unter [Konfigurieren von SSL zum Sichern der Business Central Web Client-Verbindung ](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Wenn Sie Ihren Server für eine andere Startseite einrichten, können Sie die URL jederzeit ändern. Der geheime Clientschlüssel wird als verschlüsselte Zeichenfolge in Ihrer Datenbank gespeichert.  

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-common-data-service"></a>So registrieren Sie eine Anwendung in Azure AD, um eine Verbindung mit Common Data Service über Business Central herzustellen

Bei den folgenden Schritten wird davon ausgegangen, dass Sie Azure AD verwenden, um Identitäten und den Zugriff zu verwalten. Weitere Informationen zum Registrieren einer Anwendung in Azure AD finden Sie unter [Schnellstart: Anwendung bei der Microsoft-Identitätsplattform registrieren](/azure/active-directory/develop/quickstart-register-app). Wenn Sie Azure AD nicht verwenden, finden Sie weitere Informationen unter [Verwenden eines anderen Identitäts- und Zugriffsverwaltungsdienstes](admin-how-to-set-up-a-dynamics-crm-connection.md#using-another-identity-and-access-management-service).  

1. Wählen Sie im Navigationsbereich von Azure-Portal unter **Verwalten** die Option **Authentifizierung** aus.  
2. Fügen Sie unter **URLs umleiten** die Umleitungs-URL hinzu, die auf der Seite **Common Data Service-Verbindungseinrichtung** in [!INCLUDE[d365fin](includes/d365fin_md.md)] vorgeschlagen wird.
3. Wählen Sie unter **Verwalten** die Option **API-Berechtigungen** aus.
4. Wählen Sie unter **Konfigurierte Berechtigungen** die Option **Berechtigung hinzufügen** aus, und fügen Sie anschließen der Registerkarte **Microsoft APIs** delegierte Berechtigungen hinzu:
    * Fügen Sie für Business Central die **Financials.ReadWrite.All** -Berechtigungen hinzu.
    * Fügen Sie für Dynamics CRM die **user_impersonation** -Berechtigungen hinzu.  

    > [!NOTE]
    > Der Name der Dynamics CRM-API kann sich ändern.

5. Wählen Sie unter **Verwalten** die Option **Zertifikate & Geheimnisse** aus, und erstellen Sie dann einen neuen geheimen Schlüssel für Ihre App. Sie verwenden den geheimen Schlüssel in [!INCLUDE[d365fin](includes/d365fin_md.md)], im Feld **Geheimer Clientschlüssel** auf der Seite **Common Data Service-Verbindungseinrichtung** , oder Sie speichern ihn in einem sicheren Speicher und stellen ihn in einem Ereignisabonnenten bereit, wie weiter oben in diesem Thema beschrieben.
6. Wählen Sie **Übersicht** aus, und suchen Sie dann den Wert **Anwendungs-(Client-)ID** . Dies ist die Client-ID Ihrer Anwendung. Sie müssen sie auf der Seite **Common Data Service-Verbindungseinrichtung** im Feld **Client-ID** eingeben oder in einem sicheren Speicher speichern und in einem Ereignisabonnenten bereitstellen.
7. Geben Sie in [!INCLUDE[d365fin](includes/d365fin_md.md)] auf der Seite **Common Data Service-Verbindungseinrichtung** im Feld **Umgebungs-URL** die URL für Ihre [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Umgebung ein.
8. Aktivieren Sie das Kontrollkästchen **Aktiviert** , um die Verbindung mit [!INCLUDE[cds_long_md](includes/cds_long_md.md)] zu aktivieren.
9. Melden Sie sich mit Ihrem Administratorkonto für Azure Active Directory an (dieses Konto muss eine gültige Lizenz für [!INCLUDE[cds_long_md](includes/cds_long_md.md)] haben und ein Administrator in Ihrer [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Umgebung sein). Nachdem Sie sich angemeldet haben, werden Sie aufgefordert, Ihrer registrierten Anwendung zu erlauben, sich im Namen der Organisation bei [!INCLUDE[cds_long_md](includes/cds_long_md.md)] anzumelden. Sie müssen Ihre Zustimmung geben, um die Einrichtung abzuschließen.

   > [!NOTE]
   > Wenn Sie nicht aufgefordert werden, sich mit Ihrem Administratorkonto anzumelden, liegt dies wahrscheinlich daran, dass Popups blockiert sind. Erlauben Sie Popups von `https://login.microsoftonline.com`, um sich anzumelden.

#### <a name="using-another-identity-and-access-management-service"></a>Verwenden eines anderen Identitäts- und Zugriffsverwaltungsdienstes

Wenn Sie Azure Active Directory nicht verwenden, um Identitäten und den Zugriff zu verwalten, benötigen Sie die Hilfe eines Entwicklers. Wenn Sie die App-ID und den geheimen Schlüssel lieber an einem anderen Ort speichern möchten, können Sie die Felder „Client-ID“ und „Geheimer Clientschlüssel“ leer lassen und eine Erweiterung schreiben, um die ID und den geheimen Schlüssel von diesem Speicherort abzurufen. Sie können den geheimen Schlüssel zur Laufzeit bereitstellen, indem Sie die Ereignisse „OnGetCDSConnectionClientId“ und „OnGetCDSConnectionClientSecret“ in Codeunit 7201 „CDS Integration Impl“ abonnieren.

### <a name="to-disconnect-from-cds_long_md"></a>So trennen Sie [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **CDS-Verbindungsaufbau** ein, und wählen Sie dann den entsprechenden Link.
2. Schalten Sie auf der Seite **CDS Verbindungseinrichtung** den Schalter **Aktiviert** aus.  

## <a name="see-also"></a>Siehe auch

[Den Status einer Synchronisierung anzeigen](admin-how-to-view-synchronization-status.md)  
