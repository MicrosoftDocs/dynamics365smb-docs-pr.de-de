---
title: Einrichten des Benutzerkontos für die Integration in Common Data Service | Microsoft Docs
description: Erfahren Sie, wie die Benutzerkonten eingerichtet werden, die die Apps zum Austausch von Daten verwenden, und die Mitarbeiter nutzen, um auf Daten in den Apps zuzugreifen und diese Daten zu synchronisieren.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: ad10aa53b4fe6a8b9b65ad798c206fa251e08a7a
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196495"
---
# <a name="setting-up-user-accounts-for-integrating-with-common-data-service"></a>Einrichten des Benutzerkontos für die Integration in Common Data Service
Dieser Artikel bietet eine Übersicht darüber, wie die Benutzerkonten eingerichtet werden, die erforderlich sind, um [!INCLUDE[d365fin](includes/d365fin_md.md)] in [!INCLUDE[d365fin](includes/cds_long_md.md)] zu integrieren.  

## <a name="setting-up-the-administrator-user-account"></a>Einrichten des Administrator-Benutzerkontos
Sie müssen Ihr Administrator-Benutzerkonto für [!INCLUDE[d365fin](includes/d365fin_md.md)] als Benutzer in [!INCLUDE[d365fin](includes/cds_long_md.md)] hinzufügen. Wenn Sie die Verbindung zwischen [!INCLUDE[d365fin](includes/d365fin_md.md)] und [!INCLUDE[d365fin](includes/cds_long_md.md)] einrichten, werden wir dieses Konto einmal zur Installation und Konfiguration einiger erforderlicher Komponenten verwenden. <!--Verify this-->

## <a name="setting-up-the-user-account-for-the-integration"></a>Einrichten des Benutzerkontos für die Integration
Sie müssen ein spezifisches Benutzerkonto in Ihrem Office 365-Abonnement erstellen, das sowohl [!INCLUDE[d365fin](includes/d365fin_md.md)] als auch [!INCLUDE[d365fin](includes/cds_long_md.md)] verwenden können, um Daten zu synchronisieren. Dieses Benutzerkonto muss in der Lage sein, sich bei [!INCLUDE[d365fin](includes/cds_long_md.md)] anzumelden, was bedeutet, dass dieser Benutzer eine Lizenz für [!INCLUDE[d365fin](includes/cds_long_md.md)] und mindestens eine ihm in [!INCLUDE[d365fin](includes/cds_long_md.md)] zugewiesene Sicherheitsrolle haben muss. <!--not sure that this applies as described [here](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-user-account). For more information about how to create users in [!INCLUDE[d365fin](includes/cds_long_md.md)], see [Manage security, users, and teams](https://go.microsoft.com/fwlink/?LinkID=616518). --> Nachdem die Verbindung eingerichtet ist, ordnet [!INCLUDE[d365fin](includes/d365fin_md.md)] dem Benutzerkonto Sicherheitsrollen zu, die es in [!INCLUDE[d365fin](includes/d365fin_md.md)] benötigt.

<!--![Assisted setup guide showing place to enter synchronization user credentials](media/sync-user-setup.png "Visualization assisted setup wizard page showing place to enter synchronization user credentials")-->

> [!IMPORTANT]  
> Verwenden Sie nicht das Administratorkonto für [!INCLUDE[d365fin](includes/cds_long_md.md)] für die Synchronisierung. Dadurch wird die Synchronisierung unterbrochen.

## <a name="permissions-and-security-roles-for-user-accounts-in-d365fin"></a>Berechtigungen und Sicherheitsrollen für Benutzerkonten in [!INCLUDE[d365fin](includes/cds_long_md.md)]
Wenn Sie die CDS-Basisintegrationslösung installieren, werden die Berechtigungen für das Integrationsbenutzerkonto konfiguriert. Wenn diese Berechtigungen geändert werden, müssen Sie sie möglicherweise zurücksetzen. Sie können dies tun, indem Sie die CDS-Basisintegrationslösung neu installieren, indem Sie die Option **Integrationslösung neu installieren** auf der Seite **Common Data Service Verbindungseinrichtung** wählen. Die Sicherheitsrolle der Business Central CDS Integration wird eingesetzt.


<!--
The following tables list the minimum permissions for the user accounts in [!INCLUDE[d365fin](includes/cds_long_md.md)].

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

#### Integration User
The following table displays the minimum permissions on each tab for each security role that is required for the integration user.

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

## <a name="see-also"></a>Siehe auch  
[Integrieren in Common Data Service](admin-common-data-service.md)  
[Integration mit Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
