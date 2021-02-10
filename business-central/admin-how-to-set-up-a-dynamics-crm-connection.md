---
title: Verbinden mit Microsoft Dataverse | Microsoft Docs
description: Sie können über Microsoft Dataverse andere Apps in Business Central integrieren.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/20/2020
ms.author: bholtorf
ms.openlocfilehash: e0713de255aabc599fbc80cf29f1bfa618a29003
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753917"
---
# <a name="connect-to-microsoft-dataverse"></a>Mit Microsoft Dataverse verbinden
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

In diesem Thema wird beschrieben, wie Sie eine Verbindung zwischen [!INCLUDE[prod_short](includes/prod_short.md)]und [!INCLUDE[cds_long_md](includes/cds_long_md.md)] einrichten. Typischerweise stellen Unternehmen die Verbindung her, um Daten mit einer anderen Dynamics 365-Geschäftsanwendung, z. B. [!INCLUDE[crm_md](includes/crm_md.md)], zu integrieren und zu synchronisieren.  

## <a name="before-you-start"></a>Bevor Sie beginnen

Sie müssen einige Informationen bereithalten, bevor Sie die Verbindung herstellen:  

* Die URL für die [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Umgebung, mit der Sie eine Verbindung herstellen möchten. Wenn Sie die Aktion **Common Data Service Verbindungseinrichtung** unterstützte Einrichtungsanleitung verwenden, um die Verbindung herzustellen, werden wir Ihre Umgebungen ermitteln, aber Sie können auch die URL einer anderen Umgebung in Ihrem Mandant eingeben.  
* Der Benutzername und das Passwort eines Kontos, das über Administratorberechtigungen in [!INCLUDE[prod_short](includes/prod_short.md)] und [!INCLUDE[cds_long_md](includes/cds_long_md.md)] verfügt.  
* Wenn Sie eine lokale [!INCLUDE[prod_short](includes/prod_short.md)] 2020 Veröffentlichungszyklus 1, Version 16.5 haben, lesen Sie den Artikel zu [Einige bekannte Probleme](/dynamics365/business-central/dev-itpro/upgrade/known-issues#wrong-net-assemblies-for-external-connected-services). Sie müssen die beschriebene Problemumgehung ausführen, bevor Sie eine Verbindung zu [!INCLUDE[cds_long_md](includes/cds_long_md.md)] herstellen können.

> [!Note]
> Diese Schritte beschreiben das Verfahren in [!INCLUDE[prod_short](includes/prod_short.md)] online.
> Wenn Sie [!INCLUDE[prod_short](includes/prod_short.md)] lokal verwenden und nicht das Azure Active Directory Konto verwenden, um die Verbindung mit [!INCLUDE [cds_long_md](includes/cds_long_md.md)] herzustellen, müssen Sie außerdem einen Benutzernamen und ein Kennwort eines Benutzerkontos für die Integration angeben. Dieses Konto wird als „Integrationsbenutzer“-Konto bezeichnet. Wenn Sie ein Azure Active Directory-Konto verwenden, ist das Integrationsbenutzerkonto weder erforderlich noch wird es angezeigt. Der Integrationsbenutzer wird automatisch eingerichtet und benötigt keine Lizenz.

## <a name="set-up-a-connection-to-cds_long_md"></a>Eine Verbindung mit [!INCLUDE[cds_long_md](includes/cds_long_md.md)] einrichten

Für alle anderen Authentifizierungstypen als die Microsoft 365-Authentifizierung richten Sie Ihre Verbindung mit [!INCLUDE[cds_long_md](includes/cds_long_md.md)] auf der Seite **Common Data Service Verbindungseinrichtung** ein. Für die Microsoft 365-Authentifizierung empfehlen wir die Anleitung zur unterstützten Einrichtung für die **Common Data Service Verbindung**. Der Leitfaden erleichtert die Einrichtung der Verbindung und die Festlegung erweiterter Funktionen, wie z. B. Personenbesitz und Erstsynchronisierung.  

> [!IMPORTANT]
> Während der Einrichtung der Verbindung mit [!INCLUDE[cds_long_md](includes/cds_long_md.md)] wird der Administrator aufgefordert, der registrierten Azure-Anwendung mit dem Namen [!INCLUDE[prod_short](includes/prod_short.md)] Integration für [!INCLUDE[cds_long_md](includes/cds_long_md.md)] zu erteilen:
>
> * Die Berechtigung **Auf [!INCLUDE[cds_long_md](includes/cds_long_md.md)] zugreifen** ist erforderlich, damit [!INCLUDE[prod_short](includes/prod_short.md)] im Namen des Administrators automatisch einen nicht lizenzierten, nicht interaktiven Benutzer der Anwendung [!INCLUDE[prod_short](includes/prod_short.md)] Integration erstellen, diesem Benutzer Sicherheitsrollen zuweisen und [!INCLUDE[prod_short](includes/prod_short.md)] Base CDS Integration Solution für [!INCLUDE[cds_long_md](includes/cds_long_md.md)] bereitstellen kann. Diese Berechtigung wird nur einmal beim Einrichten der Verbindung mit [!INCLUDE[cds_long_md](includes/cds_long_md.md)] verwendet.  
> * Die Berechtigung **Vollzugriff auf Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]** ist erforderlich, damit automatisch erstellte Benutzer der Anwendung [!INCLUDE[prod_short](includes/prod_short.md)] Integration auf [!INCLUDE[prod_short](includes/prod_short.md)]-Daten zugreifen können, die synchronisiert werden.  
> * Die Berechtigung **Anmelden und Ihr Profil lesen** ist erforderlich, um zu überprüfen, ob dem Benutzer, der sich anmeldet, tatsächlich die Sicherheitsrolle „Systemadministrator“ in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] zugewiesen ist.  
>
> Durch die Einwilligung im Namen der Organisation berechtigt der Administrator die registrierte Azure-Anwendung mit dem Namen [!INCLUDE[prod_short](includes/prod_short.md)] Integration für [!INCLUDE[cds_long_md](includes/cds_long_md.md)], Daten mit automatisch erstellten Anmeldeinformationen des Benutzers der Anwendung [!INCLUDE[prod_short](includes/prod_short.md)] zu synchronisieren.

### <a name="to-use-the-common-data-service-connection-setup-assisted-setup-guide"></a>So verwenden Sie die Common Data Service Anleitung zur unterstützten Einrichtung
Die Anleitung zur unterstützten Einrichtung für die Verbindung von Common Data Service kann Ihnen helfen, die Verbindung einfacher herzustelle und Sie kann Ihnen sogar beim Ausführen einer ersten Synchronisierung helfen. Wenn Sie die anfängliche Synchronisierung ausführen möchten, überprüft [!INCLUDE[prod_short](includes/prod_short.md)] die Daten in beiden Anwendungen und gibt Empfehlungen für die anfängliche Synchronisierung. Die folgende Tabelle beschreibt die Empfehlungen.

|Empfehlung  |Beschreibung  |
|---------|---------|
|**Vollständige Synchronisierung**|Daten existieren nur in [!INCLUDE[prod_short](includes/prod_short.md)] oder nur in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Die Empfehlung lautet, alle Daten des Dienstes, der sie hat, mit dem anderen Dienst zu synchronisieren.|
|**Keine Synchronisation**|Daten sind in beiden Anwendungen vorhanden, und eine vollständige Synchronisierung würde die Daten duplizieren. Die Empfehlung ist, Datensätze zu koppeln.|
|**Abhängigkeit nicht erfüllt**|Daten sind in beiden Anwendungen vorhanden, aber die Zeile oder Tabelle kann nicht synchronisiert werden, da dies von einer Zeile oder Tabelle abhängt, für die die Empfehlung Keine Synchronisierung gilt. Wenn beispielsweise Kunden nicht synchronisiert werden können, können auch Daten für Kontakte, die von den Kundendaten abhängen, nicht synchronisiert werden.|

> [!IMPORTANT]
> In der Regel verwenden Sie die vollständige Synchronisierung nur, wenn Sie die Anwendungen zum ersten Mal integrieren, und nur eine Anwendung enthält Daten. Eine vollständige Synchronisierung kann in einer Demonstrationsumgebung hilfreich sein, da in jeder Anwendung automatisch Datensätze erstellt und gekoppelt werden, wodurch die Arbeit mit synchronisierten Daten beschleunigt wird. Sie sollten die vollständige Synchronisierung jedoch nur ausführen, wenn Sie eine Zeile in [!INCLUDE[prod_short](includes/prod_short.md)] für jede Zeile in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] für die Tabellenzuordnungen möchten. Andernfalls kann das Ergebnis doppelte Datensätze sein.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Unterstützte Einrichtung** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie **Dataverse-Verbindung einrichten** aus, um das unterstützte Setup zu starten.
3. Füllen Sie die Felder nach Bedarf aus.

> [!NOTE]
> Wenn Sie nicht aufgefordert werden, sich mit Ihrem Administratorkonto anzumelden, liegt dies wahrscheinlich daran, dass die Popups blockiert sind. Erlauben Sie Popups von `https://login.microsoftonline.com`, um sich anzumelden.

### <a name="to-create-or-maintain-the-connection-manually"></a>So erstellen oder pflegen Sie den Link manuell

Die folgende Prozedur beschreibt, wie die Verbindung auf der Seite **Common Data Service Verbindungs-Einrichtung** manuell eingerichtet wird. Dies ist auch die Seite, auf der Sie Einstellungen für die Integration verwalten.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Common Data Service Verbindungseinrichtung** ein und wählen Sie dann den entsprechenden Link.
2. Geben Sie die folgenden Informationen über die Verbindung von [!INCLUDE[prod_short](includes/prod_short.md)] mit [!INCLUDE[cds_long_md](includes/cds_long_md.md)] ein.

    |Feld|Beschreibung|
    |-----|-----|
    |**Umgebungs-URL**|Wenn Sie Umgebungen in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] besitzen, werden wir diese für Sie finden, wenn Sie den Einrichtungsleitfaden ausführen. Wenn Sie eine Verbindung zu einer anderen Umgebung in einem anderen Mandanten herstellen möchten, können Sie die Administrator-Zugangsdaten für die Umgebung eingeben, und wir werden diese ermitteln. |
    |**Aktiviert**|Beginnen Sie mit der Verwendung der Integration. Wenn Sie die Verbindung nicht sofort aktivieren, werden die Verbindungseinstellungen gespeichert, aber Benutzer können nicht von [!INCLUDE[prod_short](includes/prod_short.md)] aus auf [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Daten zugreifen. Sie können zu dieser Seite zurückkehren und die Verbindung später aktivieren.  |

3. Wählen Sie im Feld **Eigentümermodell** aus, ob Sie möchten, dass eine Team-Tabelle in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] neue Datensätze oder ein oder mehrere bestimmte Benutzer besitzen soll. Wenn Sie **Person** wählen, müssen Sie jeden Benutzer angeben. Wenn Sie **Team** wählen, wird die Standard-Geschäftseinheit im Feld **Gekoppelte Geschäftseinheit** angezeigt.

    <!--Need to verify the details in this table, are these specific to Sales maybe?  IK: No they are not and no longer relevant 
    Enter the following advanced settings.-->

   <!-- |Field|Description|
    |-----|-----|
    |**[!INCLUDE[prod_short](includes/prod_short.md)] Users Must Map to CDS Users**|If you are using the Person ownership model, specify whether [!INCLUDE[prod_short](includes/prod_short.md)] user accounts must have a matching user accounts in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. The **Microsoft 365 Authentication Email** of the [!INCLUDE[prod_short](includes/prod_short.md)] user must be the same as the **Primary Email** of the [!INCLUDE[crm_md](includes/crm_md.md)] user.<br /><br /> If you set the value to **Yes**, [!INCLUDE[prod_short](includes/prod_short.md)] users who do not have a matching [!INCLUDE[crm_md](includes/crm_md.md)] user account will not have [!INCLUDE[prod_short](includes/prod_short.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data directly from [!INCLUDE[prod_short](includes/prod_short.md)] is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] user account.<br /><br /> If you set the value to **No**, all [!INCLUDE[prod_short](includes/prod_short.md)] users will have [!INCLUDE[crm_md](includes/crm_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] connection (integration) user.|
    |**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] double check the name of this field-->|

4. Um die Verbindungseinstellungen zu testen, wählen Sie **Verbindung**, und dann **Verbindung testen**.  

    > [!NOTE]  
    > Wenn keine Datenverschlüsselung in [!INCLUDE[prod_short](includes/prod_short.md)] aktiviert ist, werden Sie gefragt, ob sie diese aktivieren möchten. Um Datenverschlüsselung zu aktivieren, wählen Sie **Ja** aus, und stellen Sie die erforderlichen Informationen bereit. Anderenfalls wählen Sie **Nein** aus. Sie können die Datenverschlüsselung später aktivieren. Weitere Informationen finden Sie unter [Verschlüsseln von Daten in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) in der Hilfe für Entwickler und die Verwaltung.  

5. Wenn die [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Synchronisierung nicht bereits eingerichtet ist, werden Sie gefragt, ob Sie die Standardsynchronisierungskonfiguration verwenden möchten. Abhängig davon, ob Sie Datensätze in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] und [!INCLUDE[prod_short](includes/prod_short.md)] angepasst bleiben sollen, wählen Sie **Ja** oder **Nein** aus.
<!--
## Show Me the Process

The following video shows the steps to connect [!INCLUDE[prod_short](includes/prod_short.md)] and [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. <br>
  
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ArlP]

-->

## <a name="connecting-on-premises-versions"></a>Verbinden von Vor-Ort-Versionen

Sie müssen einige Informationen auf der Seite **Common Data Service-Verbindungseinrichtung** eingeben, um [!INCLUDE[prod_short](includes/prod_short.md)] vor Ort mit [!INCLUDE[cds_long_md](includes/cds_long_md.md)] zu verbinden.

Wenn Sie eine Verbindung mit einem Azure Active Directory (Azure AD)-Konto herstellen möchten, müssen Sie eine Anwendung in Azure AD registrieren, die Anwendungs-ID, die geheime Schlüsseltresor-ID und die zu verwendende Umleitungs-URL angeben. Die Umleitungs-URL ist bereits ausgefüllt und sollte für die meisten Installationen funktionieren. Sie müssen Ihre Installation für die Verwendung von HTTPS einrichten. Weitere Informationen finden Sie unter [Konfigurieren von SSL zum Sichern der Business Central Web Client-Verbindung ](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Wenn Sie Ihren Server für eine andere Startseite einrichten, können Sie die URL jederzeit ändern. Der geheime Clientschlüssel wird als verschlüsselte Zeichenfolge in Ihrer Datenbank gespeichert.  

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-dataverse"></a>So registrieren Sie eine Anwendung in Azure AD, um eine Verbindung mit Dataverse über Business Central herzustellen

Bei den folgenden Schritten wird davon ausgegangen, dass Sie Azure AD verwenden, um Identitäten und den Zugriff zu verwalten. Weitere Informationen zum Registrieren einer Anwendung in Azure AD finden Sie unter [Schnellstart: Anwendung bei der Microsoft-Identitätsplattform registrieren](/azure/active-directory/develop/quickstart-register-app). Wenn Sie Azure AD nicht verwenden, finden Sie weitere Informationen unter [Verwenden eines anderen Identitäts- und Zugriffsverwaltungsdienstes](admin-how-to-set-up-a-dynamics-crm-connection.md#using-another-idtable-and-access-management-service).  

1. Wählen Sie im Navigationsbereich von Azure-Portal unter **Verwalten** die Option **Authentifizierung** aus.  
2. Fügen Sie unter **URLs umleiten** die Umleitungs-URL hinzu, die auf der Seite **Common Data Service-Verbindungseinrichtung** in [!INCLUDE[prod_short](includes/prod_short.md)] vorgeschlagen wird.
3. Wählen Sie unter **Verwalten** die Option **API-Berechtigungen** aus.
4. Wählen Sie unter **Konfigurierte Berechtigungen** die Option **Berechtigung hinzufügen** aus, und fügen Sie anschließen der Registerkarte **Microsoft APIs** delegierte Berechtigungen hinzu:
    * Fügen Sie für Business Central die **Financials.ReadWrite.All**-Berechtigungen hinzu.
    * Fügen Sie für Dynamics CRM die **user_impersonation**-Berechtigungen hinzu.  

    > [!NOTE]
    > Der Name der Dynamics CRM-API kann sich ändern.

5. Wählen Sie unter **Verwalten** die Option **Zertifikate & Geheimnisse** aus, und erstellen Sie dann einen neuen geheimen Schlüssel für Ihre App. Sie verwenden den geheimen Schlüssel in [!INCLUDE[prod_short](includes/prod_short.md)], im Feld **Geheimer Clientschlüssel** auf der Seite **Common Data Service-Verbindungseinrichtung**, oder Sie speichern ihn in einem sicheren Speicher und stellen ihn in einem Ereignisabonnenten bereit, wie weiter oben in diesem Thema beschrieben.
6. Wählen Sie **Übersicht** aus, und suchen Sie dann den Wert **Anwendungs-(Client-)ID**. Dies ist die Client-ID Ihrer Anwendung. Sie müssen sie auf der Seite **Common Data Service-Verbindungseinrichtung** im Feld **Client-ID** eingeben oder in einem sicheren Speicher speichern und in einem Ereignisabonnenten bereitstellen.
7. Geben Sie in [!INCLUDE[prod_short](includes/prod_short.md)] auf der Seite **Common Data Service-Verbindungseinrichtung** im Feld **Umgebungs-URL** die URL für Ihre [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Umgebung ein.
8. Aktivieren Sie das Kontrollkästchen **Aktiviert**, um die Verbindung mit [!INCLUDE[cds_long_md](includes/cds_long_md.md)] zu aktivieren.
9. Melden Sie sich mit Ihrem Administratorkonto für Azure Active Directory an (dieses Konto muss eine gültige Lizenz für [!INCLUDE[cds_long_md](includes/cds_long_md.md)] haben und ein Administrator in Ihrer [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Umgebung sein). Nachdem Sie sich angemeldet haben, werden Sie aufgefordert, Ihrer registrierten Anwendung zu erlauben, sich im Namen der Organisation bei [!INCLUDE[cds_long_md](includes/cds_long_md.md)] anzumelden. Sie müssen Ihre Zustimmung geben, um die Einrichtung abzuschließen.

   > [!NOTE]
   > Wenn Sie nicht aufgefordert werden, sich mit Ihrem Administratorkonto anzumelden, liegt dies wahrscheinlich daran, dass Popups blockiert sind. Erlauben Sie Popups von `https://login.microsoftonline.com`, um sich anzumelden.

#### <a name="using-another-idtable-and-access-management-service"></a>Verwenden eines anderen Identitäts- und Zugriffsverwaltungsdienstes

Wenn Sie Azure Active Directory nicht verwenden, um Identitäten und den Zugriff zu verwalten, benötigen Sie die Hilfe eines Entwicklers. Wenn Sie die App-ID und den geheimen Schlüssel lieber an einem anderen Ort speichern möchten, können Sie die Felder „Client-ID“ und „Geheimer Clientschlüssel“ leer lassen und eine Erweiterung schreiben, um die ID und den geheimen Schlüssel von diesem Speicherort abzurufen. Sie können den geheimen Schlüssel zur Laufzeit bereitstellen, indem Sie die Ereignisse „OnGetCDSConnectionClientId“ und „OnGetCDSConnectionClientSecret“ in Codeunit 7201 „CDS Integration Impl“ abonnieren.

### <a name="to-disconnect-from-cds_long_md"></a>So trennen Sie [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Common Data Service Verbindungseinrichtung** ein und wählen Sie dann den entsprechenden Link.
2. Schalten Sie auf der Seite **Common Data Service Verbindungseinrichtung** die Umschaltung auf **Aktiviert**.  

## <a name="see-also"></a>Siehe auch

[Den Status einer Synchronisierung anzeigen](admin-how-to-view-synchronization-status.md)  
