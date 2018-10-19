---
title: Verwalten von Rollen und Benutzer | Microsoft Docs
description: Erfahren, wie Benutzer, Profile und Rollencenter in Finance and Operations, Business Central verwaltet werden.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: profiles, users
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 1a94d023424c6eceb93af6e9ca89a90a3a94e996
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="understanding-users-profiles-and-role-centers"></a><span data-ttu-id="9cc9f-103">Benutzer, Profile und Rollencenter verstehen</span><span class="sxs-lookup"><span data-stu-id="9cc9f-103">Understanding Users, Profiles, and Role Centers</span></span>

<span data-ttu-id="9cc9f-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], werden Benutzer von einem Administrator hinzugefügt, der auch Zugriff auf den Bereichen aus Feld [!INCLUDE[d365fin](includes/d365fin_md.md)] gibt, den sie, in ihrer Arbeit benötigen.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], users are added by an administrator who also gives users access to the areas of [!INCLUDE[d365fin](includes/d365fin_md.md)] that they need in their work.</span></span>  

<span data-ttu-id="9cc9f-105">Zugriff auf die Funktionalität wird durch *Benutzergruppen* und *Profile* verwaltet.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-105">Access to functionality is managed through *user groups* and *profiles*.</span></span> <span data-ttu-id="9cc9f-106">Als Administrator können Sie Profile zuordnen und ändern, und Sie können Benutzer als Teil des [!INCLUDE[d365fin](includes/d365fin_md.md)] Abonnements hinzufügen und  entfernen.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-106">As an administrator, you can add and remove users as part of your [!INCLUDE[d365fin](includes/d365fin_md.md)] subscription, and you can assign users permissions through user groups.</span></span>  

## <a name="adding-users"></a><span data-ttu-id="9cc9f-107">Hinzufügen von Benutzern</span><span class="sxs-lookup"><span data-stu-id="9cc9f-107">Adding Users</span></span>

<span data-ttu-id="9cc9f-108">Um Benutzer in [!INCLUDE[d365fin](includes/d365fin_md.md)] online hinzuzufügen, muss der Office 365-Administrator Ihres Unternehmens zuerst einen Benutzer im Office 365-Admin Center erstellen.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-108">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)] online, your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="9cc9f-109">Weitere Informationen sind hier verfügbar [Benutzer zu Office 365 for Business hinzufügen](https://aka.ms/CreateOffice365Users).</span><span class="sxs-lookup"><span data-stu-id="9cc9f-109">For more information, see [Add Users to Office 365 for business](https://aka.ms/CreateOffice365Users).</span></span>

<span data-ttu-id="9cc9f-110">Dann kann der Administrator Berechtigungen jedem Benutzerund Benutzergruppen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-110">Then, the administrator can assign permissions to each user and groups of users.</span></span> <span data-ttu-id="9cc9f-111">Weitere Informationen finden Sie unter [Verwalten von Benutzern und Berechtigungen](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="9cc9f-111">For more information, see [Managing Users and Permissions](ui-how-users-permissions.md).</span></span>  

### <a name="users-of-on-premises-deployments"></a><span data-ttu-id="9cc9f-112">Lokale Bereitstellungen von Benutzern</span><span class="sxs-lookup"><span data-stu-id="9cc9f-112">Users of on-premises deployments</span></span>

<span data-ttu-id="9cc9f-113">Für lokale Bereitstellungen von [!INCLUDE[d365fin](includes/d365fin_md.md)] kann der Administrator zwischen verschiedenen Autorisierungsmechanismen für Benutzer auswählen.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-113">For on-premises deployments of [!INCLUDE[d365fin](includes/d365fin_md.md)], the administrator can choose between different credential authorization mechanisms for users.</span></span> <span data-ttu-id="9cc9f-114">Wenn Sie einen Benutzer erstellen, stellen Sie je nach Anmeldeinformationstyp in der aktuellen [!INCLUDE[server](includes/server.md)]-Instanz verschiedene Informationen bereit.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-114">Then, when you create a user, you provide different information depending on the credential type that you are using in the specific [!INCLUDE[server](includes/server.md)] instance.</span></span> <span data-ttu-id="9cc9f-115">Weitere Informationen finden Sie unter [Authentifizierungs- und Anmeldeinformationstypen](/dynamics365/business-central/dev-itpro/administration/users-credential-types) im Abschnitt Verwaltung des Entwicklers und des ITPro-Inhalts für. [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="9cc9f-115">For more information, see the [Authentication and Credential Types](/dynamics365/business-central/dev-itpro/administration/users-credential-types) in the Administration section of the developer and ITPro content for [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="profiles"></a><span data-ttu-id="9cc9f-116">Profile</span><span class="sxs-lookup"><span data-stu-id="9cc9f-116">Profiles</span></span>

<span data-ttu-id="9cc9f-117">Alle Mitarbeiter in Ihrem Mandanten, die Zugriff haben auf[!INCLUDE[d365fin](includes/d365fin_md.md)] sind einem *Profil* zugewiesen, das Zugriff  auf das *Rollencenter* gibt.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-117">The people in your company who have access to [!INCLUDE[d365fin](includes/d365fin_md.md)] are all assigned a *profile* that gives them access to a *Role Center*.</span></span>

<span data-ttu-id="9cc9f-118">Profile sind Sammlungen von [!INCLUDE[d365fin](includes/d365fin_md.md)]-Benutzern, die dasselbe Rollencenter nutzen.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-118">Profiles are collections of [!INCLUDE[d365fin](includes/d365fin_md.md)] users who share the same Role Center.</span></span> <span data-ttu-id="9cc9f-119">Ein Rollencenter ist der Einstiegspunkt und die Homepage für [!INCLUDE[d365fin](includes/d365fin_md.md)] und gibt Ihnen Zugriff zu den wichtigsten Aufgaben und zeigt verschiedene Einblicke und Schlüsselleistungsindikatoren (KPIs) über Ihre Arbeit an.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-119">A Role Center is the entry point and home page for [!INCLUDE[d365fin](includes/d365fin_md.md)] that gives you quick access to your most important tasks and displays various insights and key performance indicators (KPIs) about your work.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="9cc9f-120">In der aktuellen Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] online können Sie keine Profile einfügen, ändern oder löschen.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-120">In the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] online, you cannot add, edit, or delete profiles.</span></span>  

## <a name="configuration-and-personalization"></a><span data-ttu-id="9cc9f-121">Konfiguration und Anpassung</span><span class="sxs-lookup"><span data-stu-id="9cc9f-121">Configuration and Personalization</span></span>
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->
<span data-ttu-id="9cc9f-122">Benutzer personalisieren die Benutzeroberfläche ihrer persönlichen Version, indem sie die Benutzeroberfläche unter ihrer eigenen Benutzeranmeldung anpassen.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-122">Users personalize the user interface of their personal version by customizing the user interface under their own user logon.</span></span> <span data-ttu-id="9cc9f-123">Diese Anpassung kann vom Administrator gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-123">This personalization can be deleted by the administrator.</span></span> <span data-ttu-id="9cc9f-124">Weitere Informationen finden Sie unter [Personalisieren Ihres Arbeitsbereichs](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="9cc9f-124">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="9cc9f-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9cc9f-125">See Also</span></span>  
[<span data-ttu-id="9cc9f-126">Benutzer und ihre Berechtigungen verwalten</span><span class="sxs-lookup"><span data-stu-id="9cc9f-126">Managing Users and Permissions</span></span>](ui-how-users-permissions.md)  
[<span data-ttu-id="9cc9f-127">Personalisierung als Administrator verwalten</span><span class="sxs-lookup"><span data-stu-id="9cc9f-127">Managing Personalization as an Administrator</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="9cc9f-128">Personalisieren Ihres Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="9cc9f-128">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  

