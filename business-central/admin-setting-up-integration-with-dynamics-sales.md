---
title: Einrichten des Benutzerkontos für die Integration in Microsoft Dataverse | Microsoft Docs
description: Erfahren Sie, wie die Benutzerkonten eingerichtet werden, die die Apps zum Austausch von Daten verwenden, und die Mitarbeiter nutzen, um auf Daten in den Apps zuzugreifen und diese Daten zu synchronisieren.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 2717196a170aede43bfb56d796b1da9307ff8d3f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777191"
---
# <a name="setting-up-user-accounts-for-integrating-with-microsoft-dataverse"></a><span data-ttu-id="a9a88-103">Einrichten des Benutzerkontos für die Integration in Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="a9a88-103">Setting Up User Accounts for Integrating with Microsoft Dataverse</span></span>
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

<span data-ttu-id="a9a88-104">Dieser Artikel bietet eine Übersicht darüber, wie die Benutzerkonten eingerichtet werden, die erforderlich sind, um [!INCLUDE[prod_short](includes/prod_short.md)] in [!INCLUDE[prod_short](includes/cds_long_md.md)] zu integrieren.</span><span class="sxs-lookup"><span data-stu-id="a9a88-104">This article provides an overview of how to set up the user accounts that are required to integrate [!INCLUDE[prod_short](includes/cds_long_md.md)] with [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

## <a name="setting-up-the-administrator-user-account"></a><span data-ttu-id="a9a88-105">Einrichten des Administrator-Benutzerkontos</span><span class="sxs-lookup"><span data-stu-id="a9a88-105">Setting Up the Administrator User Account</span></span>
<span data-ttu-id="a9a88-106">Sie müssen Ihr Administrator-Benutzerkonto für [!INCLUDE[prod_short](includes/prod_short.md)] als Benutzer in [!INCLUDE[prod_short](includes/cds_long_md.md)] hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a9a88-106">You must add your administrator user account for [!INCLUDE[prod_short](includes/prod_short.md)] as a user in [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span> <span data-ttu-id="a9a88-107">Wenn Sie die Verbindung zwischen [!INCLUDE[prod_short](includes/prod_short.md)] und [!INCLUDE[prod_short](includes/cds_long_md.md)] einrichten, werden wir dieses Konto einmal zur Installation und Konfiguration einiger erforderlicher Komponenten verwenden.</span><span class="sxs-lookup"><span data-stu-id="a9a88-107">When you set up the connection between [!INCLUDE[prod_short](includes/prod_short.md)] and [!INCLUDE[prod_short](includes/cds_long_md.md)] we will use this account one time to install and configure some required components.</span></span> 

## <a name="permissions-and-security-roles-for-user-accounts-in-prod_short"></a><span data-ttu-id="a9a88-108">Berechtigungen und Sicherheitsrollen für Benutzerkonten in [!INCLUDE[prod_short](includes/cds_long_md.md)]</span><span class="sxs-lookup"><span data-stu-id="a9a88-108">Permissions and Security Roles for User Accounts in [!INCLUDE[prod_short](includes/cds_long_md.md)]</span></span>
<span data-ttu-id="a9a88-109">Wenn Sie die CDS-Basisintegrationslösung installieren, werden die Berechtigungen für das Integrationsbenutzerkonto konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="a9a88-109">When you install the CDS Base Integration Solution, permissions for the integration user account are configured.</span></span> <span data-ttu-id="a9a88-110">Wenn diese Berechtigungen manuell geändert werden, können Sie sie zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="a9a88-110">If those permissions are changed manually you can reset them.</span></span> <span data-ttu-id="a9a88-111">Sie können dies tun, indem Sie die CDS-Basisintegrationslösung neu installieren, indem Sie die Option **Integrationslösung neu installieren** auf der Seite **Common Data Service Verbindungseinrichtung** wählen.</span><span class="sxs-lookup"><span data-stu-id="a9a88-111">You can do that by reinstalling the CDS Base Integration Solution by choosing **Redeploy Integration Solution** on the **Common Data Service Connection Setup** page.</span></span> <span data-ttu-id="a9a88-112">Die Sicherheitsrolle der Business Central CDS Integration wird eingesetzt.</span><span class="sxs-lookup"><span data-stu-id="a9a88-112">The Business Central CDS Integration security role is deployed.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="a9a88-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9a88-113">See Also</span></span>  
[<span data-ttu-id="a9a88-114">Integrieren in Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="a9a88-114">Integrating with Microsoft Dataverse</span></span>](admin-common-data-service.md)  
[<span data-ttu-id="a9a88-115">Integration mit Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="a9a88-115">Integrating with Dynamics 365 Sales</span></span>](admin-prepare-dynamics-365-for-sales-for-integration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]