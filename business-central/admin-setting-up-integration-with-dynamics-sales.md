---
title: Einrichten des Benutzerkontos für die Integration in Microsoft Dataverse | Microsoft Docs
description: 'Erfahren Sie, wie die Benutzerkonten eingerichtet werden, die die Apps zum Austausch von Daten verwenden, und die Mitarbeiter nutzen, um auf Daten in den Apps zuzugreifen und diese Daten zu synchronisieren.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="setting-up-user-accounts-for-integrating-with-microsoft-dataverse" />Einrichten des Benutzerkontos für die Integration in Microsoft Dataverse

Dieser Artikel bietet eine Übersicht darüber, wie die Benutzerkonten eingerichtet werden, die erforderlich sind, um [!INCLUDE[prod_short](includes/prod_short.md)] in [!INCLUDE[prod_short](includes/cds_long_md.md)] zu integrieren.

## <a name="set-up-the-administrator-user-account" />Das Administrator-Benutzerkonto festlegen

Um die Verbindung zwischen [!INCLUDE[prod_short](includes/prod_short.md)] und [!INCLUDE[prod_short](includes/cds_long_md.md)] einzurichten, müssen Sie sich bei [!INCLUDE[prod_short](includes/prod_short.md)] mit einem Benutzerkonto anmelden, das der [!INCLUDE[prod_short](includes/prod_short.md)] Essential- oder [!INCLUDE[prod_short](includes/prod_short.md)] Premium-Lizenz zugeordnet ist. Wir werden dieses Konto einmal verwenden, um einige erforderliche Komponenten zu installieren und zu konfigurieren.

> [!IMPORTANT]
> Während der Einrichtung werden Sie aufgefordert, Anmeldeinformationen für die [!INCLUDE[prod_short](includes/cds_long_md.md)] Umgebung anzugeben. Geben Sie die Anmeldeinformationen für ein Konto an, bei dem es sich um einen lizenzierten Benutzenden handelt und das der Sicherheitsrolle **Systemadministrator** in der [!INCLUDE[prod_short](includes/cds_long_md.md)] Umgebung und globaler Administrierender in dem Mandant zugeordnet ist, zu dem die Umgebung gehört. Dieses Konto benötigt keine Lizenz für [!INCLUDE[prod_short](includes/prod_short.md)], da es nur für die Einrichtung von Aufgaben in der [!INCLUDE[prod_short](includes/cds_long_md.md)] Umgebung verwendet wird.
>
> Nachdem die Einrichtung der Verbindung abgeschlossen ist, können Sie diesen [!INCLUDE[prod_short](includes/cds_long_md.md)]-Benutzenden entfernen. Die Integration wird mit dem Benutzerkonto fortgesetzt, das automatisch speziell für die Integration erstellt wird.

## <a name="permissions-and-security-roles-for-user-accounts-in-includeprodshortincludescdslongmdmd" />Berechtigungen und Sicherheitsrollen für Benutzerkonten in [!INCLUDE[prod_short](includes/cds_long_md.md)]

Die Basis-Integrationslösung erstellt die folgenden Rollen in [!INCLUDE[cds_long](includes/cds_long_md.md)] für die Integration:

* **Integrationsadministrator**: Lässt Benutzer zu, die Verbindung zwischen [!INCLUDE[prod_short](includes/prod_short.md)] und [!INCLUDE[cds_long](includes/cds_long_md.md)] zu verwalten. Normalerweise wird diese nur dem automatisch erstellten Benutzerkonto für die Synchronisierung zugewiesen.
* **Integrationsbenutzer**: Ermöglicht Benutzern den Zugriff auf synchronisierte Daten. In der Regel wird dies dem automatisch erstellten Benutzerkonto für die Synchronisierung und anderen Benutzern zugewiesen, die die synchronisierten Daten anzeigen oder auf sie zugreifen müssen.

> [!NOTE]
>
> Die Rollen **Integrationsadministrator** und **Integrationsbenutzer** sollten nur von dem Anwendungsbenutzer verwendet werden, der die Integration ausführt. Der Anwendungsbenutzer braucht die zugewiesene [!INCLUDE[prod_short](includes/prod_short.md)]- oder [!INCLUDE[cds_long](includes/cds_long_md.md)]-Lizenz nicht.

Wenn Sie die Basis-Integrationslösung installieren, werden die Berechtigungen für das Benutzerkonto des Integrationsbenutzers konfiguriert. Wenn diese Berechtigungen manuell geändert werden, können Sie sie zurücksetzen. Wählen Sie **Integrationslösung neu bereitstellen** auf der Seite **Dataverse Verbindungseinrichtung**, um die Basis-Integrationslösung neu zu installieren. Mit diesem Schritt wird die Sicherheitsrolle Business Central Integration bereitgestellt.

<!--
The following tables list the minimum permissions for the user accounts in [!INCLUDE[prod_short](includes/cds_long_md.md)].

### <a name="minimum-permissions-for-the-administrator" />Minimum Permissions for the Administrator
The following table displays the minimum permissions on each tab for each security role that is required for the administrator user.

##### <a name="customization" />Customization
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Model Driven App|Global|||Read|
|Plugin Assembly|Global|Read|Read|Read|
|Plugin Type|Global|Read|Read|Read|
|Relationship|Global|||Read|
|SDK Message|Global|Read|Read|Read|
|SDK Message Proessing Step|Global|Read|Read|Read|
|SDK Message Proessing Step Image|Global|Read|Read|Read|
|System From|Global|||Write|

##### <a name="custom-entities" />Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2020|
|----|----|-----|----|----|
|Business Central Account Statistics|Global|Read|Read|Read|
|Business Central Connection|Global|Create, Read, Write, Delete|Create, Read, Write, Delete|Create, Read, Write, Delete|
|Post Configuration|Global|||Write|

### <a name="minimum-permissions-for-automatically-created-includeprodshortincludesprodshortmd-integration-application-user" />Minimum Permissions for automatically created [!INCLUDE[prod_short](includes/prod_short.md)] Integration application user
The following table displays the minimum permissions on each tab for each security role that is required for the automatically created [!INCLUDE[prod_short](includes/prod_short.md)] Integration application user.

##### <a name="core-records" />Core Records
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Account|Global|Create, Read, Write, Append, Append To, Assign|Create, Read, Write, Append, Append To, Assign|Create, Read, Write, Append, Append To, Assign|
|Action Card|Global||Read|Read|
|Connection|Global|Read|Read|Read|
|Contact|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Note|Global|||Create, Read, Write, Delete Append, Assign|
|Opportunity|Global||Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Post|Global|||Create, Read, Append To|
|User Entity UI|User|Create, Read, Write|Create, Read, Write|Create, Read, Write|

##### <a name="sales" />Sales
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Invoice|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Order|Global|Read, Write, Append To|Read, Write, Append To|Read, Write, Append, Append To, Assign|
|Product|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Property|Global|Read|Read|Read|
|Property Association|Global|Read|Read|Read|
|Property Option Set Item|Global|Read|Read|Read|
|Quote|Global|Read|Read|Read|

##### <a name="service" />Service
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Case|Global|Read|Read|Read|

##### <a name="business-management" />Business Management
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Currency|Global|Create, Read, Write|Create, Read, Write|Create, Read, Write|
|Organization|Global|Read, Write|Read, Write|Read, Write|
|Security Role|Global|||Read|
|User|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|User Settings|Global|Create, Read, Write, Delete, Append To|Create, Read, Write, Delete, Append To|Create, Read, Write, Delete, Append To|
|Act on Behalf of Another User|Global|Yes|Yes|Yes|

##### <a name="customization" />Customization
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Field|Global||Read|Read|
|Plug-in Assembly|Global|Read|Read|Read|
|Plug-in Type|Global|Read|Read|Read|
|SDK Message|Global|Read|Read|Read|
|SDK Message Processing Step|Global|Read|Read|Read|
|Web Resource|Global|Read|Read|Read|

##### <a name="custom-entities" />Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Account Statistics|Global|Create, Read, Write, Append To|Create, Read, Write, Append To|Create, Read, Write, Append To|
|Dynamics 365 Business Central Connection|Global|Read|Read|Read|

### <a name="product-availability-user" />Product Availability User
You can allow sales people to view inventory levels for the items they sell by granting them the permissions described in the following table.

##### <a name="custom-entities" />Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Account Statistics|Global|Create, Read, Write, Append To|Create, Read, Write, Append To|Create, Read, Write, Append To|
|Dynamics 365 Business Central Connection|Global|Read|Read|Read|

-->

## <a name="see-also" />Siehe auch

[Integrieren in Microsoft Dataverse](admin-common-data-service.md)  
[Integration mit Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
