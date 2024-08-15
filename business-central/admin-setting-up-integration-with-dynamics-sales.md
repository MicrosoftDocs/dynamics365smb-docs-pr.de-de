---
title: Einrichten des Benutzerkontos für die Integration in Microsoft Dataverse | Microsoft Docs
description: 'Erfahren Sie, wie die Benutzerkonten eingerichtet werden, die die Apps zum Austausch von Daten verwenden, und die Mitarbeiter nutzen, um auf Daten in den Apps zuzugreifen und diese Daten zu synchronisieren.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 01/12/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Einrichten des Benutzerkontos für die Integration in Microsoft Dataverse über die Datensynchronisierung

Dieser Artikel bietet eine Übersicht darüber, wie die Benutzerkonten eingerichtet werden, die erforderlich sind, um [!INCLUDE[prod_short](includes/prod_short.md)] in [!INCLUDE[prod_short](includes/cds_long_md.md)] zu integrieren.

## Das Administrator-Benutzerkonto festlegen

Um die Verbindung zwischen [!INCLUDE[prod_short](includes/prod_short.md)] und [!INCLUDE[prod_short](includes/cds_long_md.md)] einzurichten, müssen Sie sich bei [!INCLUDE[prod_short](includes/prod_short.md)] mit einem Benutzerkonto anmelden, das der [!INCLUDE[prod_short](includes/prod_short.md)] Essential- oder [!INCLUDE[prod_short](includes/prod_short.md)] Premium-Lizenz zugeordnet ist. Wir werden dieses Konto einmal verwenden, um einige erforderliche Komponenten zu installieren und zu konfigurieren.

> [!IMPORTANT]
> Während der Einrichtung werden Sie aufgefordert, Anmeldeinformationen für die [!INCLUDE[prod_short](includes/cds_long_md.md)] Umgebung anzugeben. Geben Sie die Anmeldeinformationen eines Kontos ein, bei dem es sich um einen lizenzierten Benutzer handelt und dem die Sicherheitsrolle  **Systemadministrator**  für  [!INCLUDE[prod_short](includes/cds_long_md.md)] Umgebung und die Rolle  [Benutzeradministrator](/entra/identity/role-based-access-control/permissions-reference#user-administrator)  für den Mandanten zugewiesen ist, zu dem Umgebung gehört. Dieses Konto benötigt keine Lizenz für [!INCLUDE[prod_short](includes/prod_short.md)], da es nur für die Einrichtung von Aufgaben in der [!INCLUDE[prod_short](includes/cds_long_md.md)] Umgebung verwendet wird.
>
> Nachdem die Einrichtung der Verbindung abgeschlossen ist, können Sie diesen [!INCLUDE[prod_short](includes/cds_long_md.md)]-Benutzenden entfernen. Die Integration wird mit dem Benutzerkonto fortgesetzt, das automatisch speziell für die Integration erstellt wird.

## Berechtigungen und Sicherheitsrollen für Benutzerkonten in [!INCLUDE[prod_short](includes/cds_long_md.md)]

Die Basis-Integrationslösung erstellt in [!INCLUDE [cds_long_md](includes/cds_long_md.md)] die folgende Rolle für die Integration:

* **Business Central Dataverse-Integration**: Ermöglicht Ihnen das Verwalten der Verbindung zwischen [!INCLUDE [prod_short](includes/prod_short.md)] und [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Normalerweise wird diese nur dem automatisch erstellten Benutzerkonto für die Synchronisierung zugewiesen.

> [!NOTE]
> Nur der Anwendungsbenutzende, der die Integration ausführt, sollte die Rolle **Business Central Dataverse-Integration** haben. Der Anwendungsbenutzende braucht die zugewiesenen [!INCLUDE [prod_short](includes/prod_short.md)]- oder [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-Lizenzen nicht.

Wenn Sie die Basis-Integrationslösung installieren, werden die Berechtigungen für das Benutzerkonto des Integrationsbenutzers konfiguriert. Wenn diese Berechtigungen manuell geändert werden, können Sie sie zurücksetzen. Wählen Sie **Integrationslösung neu bereitstellen** auf der Seite **Dataverse Verbindungseinrichtung**, um die Basis-Integrationslösung neu zu installieren. Mit diesem Schritt wird die Sicherheitsrolle Business Central Integration bereitgestellt.

<!--
The following tables list the minimum permissions for the user accounts in [!INCLUDE[prod_short](includes/cds_long_md.md)].

### Minimum Permissions for the Administrator
The following table displays the minimum permissions on each tab for each security role that is required for the administrator user.

##### Customization
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

##### Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2020|
|----|----|-----|----|----|
|Business Central Account Statistics|Global|Read|Read|Read|
|Business Central Connection|Global|Create, Read, Write, Delete|Create, Read, Write, Delete|Create, Read, Write, Delete|
|Post Configuration|Global|||Write|

### Minimum Permissions for automatically created [!INCLUDE[prod_short](includes/prod_short.md)] Integration application user
The following table displays the minimum permissions on each tab for each security role that is required for the automatically created [!INCLUDE[prod_short](includes/prod_short.md)] Integration application user.

##### Core Records
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

##### Sales
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Invoice|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Order|Global|Read, Write, Append To|Read, Write, Append To|Read, Write, Append, Append To, Assign|
|Product|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Property|Global|Read|Read|Read|
|Property Association|Global|Read|Read|Read|
|Property Option Set Item|Global|Read|Read|Read|
|Quote|Global|Read|Read|Read|

##### Service
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Case|Global|Read|Read|Read|

##### Business Management
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Currency|Global|Create, Read, Write|Create, Read, Write|Create, Read, Write|
|Organization|Global|Read, Write|Read, Write|Read, Write|
|Security Role|Global|||Read|
|User|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|User Settings|Global|Create, Read, Write, Delete, Append To|Create, Read, Write, Delete, Append To|Create, Read, Write, Delete, Append To|
|Act on Behalf of Another User|Global|Yes|Yes|Yes|

##### Customization
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Field|Global||Read|Read|
|Plug-in Assembly|Global|Read|Read|Read|
|Plug-in Type|Global|Read|Read|Read|
|SDK Message|Global|Read|Read|Read|
|SDK Message Processing Step|Global|Read|Read|Read|
|Web Resource|Global|Read|Read|Read|

##### Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Account Statistics|Global|Create, Read, Write, Append To|Create, Read, Write, Append To|Create, Read, Write, Append To|
|Dynamics 365 Business Central Connection|Global|Read|Read|Read|

### Product Availability User
You can allow sales people to view inventory levels for the items they sell by granting them the permissions described in the following table.

##### Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Account Statistics|Global|Create, Read, Write, Append To|Create, Read, Write, Append To|Create, Read, Write, Append To|
|Dynamics 365 Business Central Connection|Global|Read|Read|Read|

-->

## Siehe auch

[Integrieren in Microsoft Dataverse](admin-common-data-service.md)  
[Integration mit Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
