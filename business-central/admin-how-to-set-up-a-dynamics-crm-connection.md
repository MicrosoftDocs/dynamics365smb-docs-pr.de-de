---
title: Mit Microsoft Dynamics 365 Sales verbinden | Microsoft Docs
description: Sie können über Common Data Service andere Apps in Business Central integrieren.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 3375db0208d1a0275011f0efbfce4a13102c522e
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196639"
---
# <a name="connect-to-common-data-service"></a>Mit Common Data Service verbinden
In diesem Thema wird beschrieben, wie Sie eine Verbindung zwischen [!INCLUDE[d365fin](includes/d365fin_md.md)]und [!INCLUDE[d365fin](includes/cds_long_md.md)] einrichten. Typischerweise stellen Unternehmen die Verbindung her, um Daten mit einer anderen Dynamics 365-Geschäftsanwendung, z. B. [!INCLUDE[crm_md](includes/crm_md.md)], zu integrieren und zu synchronisieren.  

## <a name="before-you-start"></a>Bevor Sie beginnen
Sie müssen einige Informationen bereithalten, bevor Sie die Verbindung herstellen:  

* Die URL für die [!INCLUDE[d365fin](includes/cds_long_md.md)]-Umgebung, mit der Sie eine Verbindung herstellen möchten. Wenn Sie die Aktion **CDS Verbindungseinrichtung** unterstützte Einrichtungsanleitung verwenden, um die Verbindung herzustellen, werden wir Ihre Umgebungen ermitteln, aber Sie können auch die URL einer anderen Umgebung in Ihrem Mandant eingeben.  
* Ein Benutzername und ein Kennwort eines Benutzerkontos, die nur für die Integration verwendet werden. Dieses Konto wird als „Integrationsbenutzer“-Konto bezeichnet. 
* Der Benutzername und das Passwort eines Kontos, das über Administratorberechtigungen in [!INCLUDE[d365fin](includes/d365fin_md.md)] und [!INCLUDE[d365fin](includes/cds_long_md.md)] verfügt.  

> [!Note]
> Diese Schritte beschreiben das Verfahren der Onlineversion von [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="set-up-a-connection-to-d365fin"></a>Eine Verbindung mit [!INCLUDE[d365fin](includes/cds_long_md.md)] einrichten  
Für alle anderen Authentifizierungstypen als die Office 365-Authentifizierung richten Sie Ihre Verbindung zu [!INCLUDE[d365fin](includes/cds_long_md.md)] auf der Seite **CDS-Verbindungseinrichtung** ein. Für die Office 365-Authentifizierung empfehlen wir die Verwendung des **CDS-Verbindungseinrichtung** Assistenten zur Einrichtung. Der Leitfaden erleichtert die Einrichtung der Verbindung und die Spezifizierung erweiterter Funktionen, wie z.B. die Kopplung zwischen Datensätzen.  

### <a name="to-use-the-cds-connection-setup-assisted-setup-guide"></a>So verwenden Sie die Anleitung zur Einrichtung der CDS-Verbindung 
1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Unterstützte Einrichtung** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie **CDS-CDS Base Integration Verbindung einrichten**, um den Leitfaden zur unterstützten Einrichtung zu starten.
3. Füllen Sie die Felder nach Bedarf aus.

> [!Note]
> Die Spalte **CDS Verbindungseinrichtung** unterstützter Einrichtungsleitfaden weist dem für die Integration verwendeten Benutzerkonto automatisch die Sicherheitsrollen **Integrationsadministrator** und **Integrationsbenutzer** zu und setzt den Zugriffsmodus für das Konto auf **nicht interaktiv**.

### <a name="to-create-or-maintain-the-connection-manually"></a>So erstellen oder pflegen Sie den Link manuell
Die folgende Prozedur beschreibt, wie die Verbindung auf der Seite **CDS-Verbindungsaufbau** manuell eingerichtet wird. Dies ist auch die Seite, auf der Sie Einstellungen für die Integration verwalten.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **CDS-Verbindungsaufbau** ein, und wählen Sie dann den entsprechenden Link.
2. Geben Sie die folgenden Informationen über die Verbindung von [!INCLUDE[d365fin](includes/d365fin_md.md)] mit [!INCLUDE[d365fin](includes/cds_long_md.md)] ein.

|Feld|Beschreibung|
|-----|-----|
|**Umgebungs-URL**|Wenn Sie Umgebungen in [!INCLUDE[d365fin](includes/cds_long_md.md)] besitzen, werden wir diese für Sie finden, wenn Sie den Einrichtungsleitfaden ausführen. Wenn Sie eine Verbindung zu einer anderen Umgebung in einem anderen Mandanten herstellen möchten, können Sie die Administrator-Zugangsdaten für die Umgebung eingeben, und wir werden diese ermitteln. |
|**Benutzername** und **Kennwort**|Die Anmeldeinformationen des Benutzerkontos, das für die Integration dediziert ist. Weitere Informationen finden Sie unter [Einrichten des Benutzerkontos für die Integration in [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).|
|**Aktiviert**|Beginnen Sie mit der Verwendung der Integration. Wenn Sie die Verbindung nicht sofort aktivieren, werden die Verbindungseinstellungen gespeichert, aber Benutzer können nicht von [!INCLUDE[d365fin](includes/d365fin_md.md)] aus auf [!INCLUDE[d365fin](includes/cds_long_md.md)]-Daten zugreifen. Sie können zu dieser Seite zurückkehren und die Verbindung später aktivieren.  |

3. Wählen Sie im Feld **Eigentümermodell** aus, ob eine Team-Entität in [!INCLUDE[d365fin](includes/cds_long_md.md)] neue Datensätze oder ein oder mehrere bestimmte Benutzer besitzen soll. Wenn Sie **Person** wählen, müssen Sie jeden Benutzer angeben. Wenn Sie **Team** wählen, wird die Standard-Geschäftseinheit BCI_Company im Feld **Gekoppelte Geschäftseinheit** angezeigt.

<!--Need to verify the details in this table, are these specific to Sales maybe?
Enter the following advanced settings.

|Field|Description|
|-----|-----|
|**[!INCLUDE[d365fin](includes/d365fin_md.md)] Users Must Map to CDS Users**|If you are using the Person ownership model, specify whether [!INCLUDE[d365fin](includes/d365fin_md.md)] user accounts must have a matching user accounts in [!INCLUDE[d365fin](includes/cds_long_md.md)]. The **Office 365 Authentication Email** of the [!INCLUDE[d365fin](includes/d365fin_md.md)] user must be the same as the **Primary Email** of the [!INCLUDE[crm_md](includes/crm_md.md)] user.<br /><br /> If you set the value to **Yes**, [!INCLUDE[d365fin](includes/d365fin_md.md)] users who do not have a matching [!INCLUDE[crm_md](includes/crm_md.md)] user account will not have [!INCLUDE[d365fin](includes/d365fin_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data directly from [!INCLUDE[d365fin](includes/d365fin_md.md)] is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] user account.<br /><br /> If you set the value to **No**, all [!INCLUDE[d365fin](includes/d365fin_md.md)] users will have [!INCLUDE[crm_md](includes/crm_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] connection (integration) user.|
|**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] <!--double check the name of this field|-->

4. Um die Verbindungseinstellungen zu testen, wählen Sie **Verbindung**, und dann **Verbindung testen**.  

    > [!NOTE]  
    >  Wenn keine Datenverschlüsselung in [!INCLUDE[d365fin](includes/d365fin_md.md)] aktiviert ist, werden Sie gefragt, ob sie diese aktivieren möchten. Um Datenverschlüsselung zu aktivieren, wählen Sie **Ja** aus, und stellen Sie die erforderlichen Informationen bereit. Anderenfalls wählen Sie **Nein** aus. Sie können die Datenverschlüsselung später aktivieren. Weitere Informationen finden Sie unter [Verschlüsseln von Daten in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data.md) in der Entwickler- und IT-Pro-Hilfe.  

5. Wenn die [!INCLUDE[d365fin](includes/cds_long_md.md)]-Synchronisierung nicht bereits eingerichtet ist, werden Sie gefragt, ob Sie die Standardsynchronisierungskonfiguration verwenden möchten. Abhängig davon, ob Sie Datensätze in [!INCLUDE[d365fin](includes/cds_long_md.md)] und [!INCLUDE[d365fin](includes/d365fin_md.md)] angepasst bleiben sollen, wählen Sie **Ja** oder **Nein** aus.

> [!Note]
> Wenn Sie sich über die Seite **CDS-Verbindungsaufbau** mit [!INCLUDE[d365fin](includes/cds_long_md.md)] verbinden, kann es erforderlich sein, dass Sie dem für die Integration in Dynamics 365 Sales verwendeten Konto die Sicherheitsrollen Integrationsadministrator und Integrationsbenutzer zuweisen. Weitere Informationen finden Sie unter [Weisen Sie einem Benutzer eine Sicherheitsrolle zu](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user.md).

### <a name="to-disconnect-from-d365fin"></a>So trennen Sie [!INCLUDE[d365fin](includes/cds_long_md.md)]  
1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **CDS-Verbindungsaufbau** ein, und wählen Sie dann den entsprechenden Link.
2. Schalten Sie auf der Seite **CDS Verbindungseinrichtung** den Schalter **Aktiviert** aus.  

## <a name="see-also"></a>Siehe auch  
[Den Status einer Synchronisierung anzeigen](admin-how-to-view-synchronization-status.md)  
