---
title: Verwalten von Rollen und Benutzer | Microsoft Docs
description: Erfahren, wie Benutzer, Profile und Rollencenter in Finance and Operations, Business Central verwaltet werden.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/02/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e5efc3536203495dcec1be2f1dc680b35c39d4db
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="understanding-users-profiles-and-role-centers"></a><span data-ttu-id="ce57d-103">Benutzer, Profile und Rollencenter verstehen</span><span class="sxs-lookup"><span data-stu-id="ce57d-103">Understanding Users, Profiles, and Role Centers</span></span>
<span data-ttu-id="ce57d-104">Alle Mitarbeiter in Ihrem Mandanten, die Zugriff haben auf[!INCLUDE[d365fin](includes/d365fin_md.md)] sind einem *Profil* zugewiesen, das Zugriff  auf das *Rollencenter* gibt.</span><span class="sxs-lookup"><span data-stu-id="ce57d-104">The people in your company who have access to [!INCLUDE[d365fin](includes/d365fin_md.md)] are all assigned a *profile* that gives them access to a *Role Center*.</span></span> <span data-ttu-id="ce57d-105">Als Administrator können Sie Profile in [!INCLUDE[d365fin](includes/d365fin_md.md)] zuordnen und ändern, und Sie können Benutzer als Teil des [!INCLUDE[d365fin](includes/d365fin_md.md)] Abonnements hinzufügen und  entfernen.</span><span class="sxs-lookup"><span data-stu-id="ce57d-105">As an administrator, you can assign and change profiles in [!INCLUDE[d365fin](includes/d365fin_md.md)], and you can add and remove users as part of your [!INCLUDE[d365fin](includes/d365fin_md.md)] subscription.</span></span>  

## <a name="adding-users"></a><span data-ttu-id="ce57d-106">Hinzufügen von Benutzern</span><span class="sxs-lookup"><span data-stu-id="ce57d-106">Adding Users</span></span>
<span data-ttu-id="ce57d-107">Um Benutzer in [!INCLUDE[d365fin](includes/d365fin_md.md)] hinzuzufügen, muss der Office 365-Administrator Ihres Unternehmens zuerst einen Benutzer im Office 365-Admin Center erstellen.</span><span class="sxs-lookup"><span data-stu-id="ce57d-107">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)], your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="ce57d-108">Weitere Informationen finden Sie unter [Verwalten von Benutzern und Berechtigungen](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="ce57d-108">For more information, see [Managing Users and Permissions](ui-how-users-permissions.md).</span></span>  

## <a name="profiles"></a><span data-ttu-id="ce57d-109">Profile</span><span class="sxs-lookup"><span data-stu-id="ce57d-109">Profiles</span></span>
<span data-ttu-id="ce57d-110">Profile sind Sammlungen von [!INCLUDE[d365fin](includes/d365fin_md.md)]-Benutzern, die dasselbe Rollencenter nutzen.</span><span class="sxs-lookup"><span data-stu-id="ce57d-110">Profiles are collections of [!INCLUDE[d365fin](includes/d365fin_md.md)] users who share the same Role Center.</span></span> <span data-ttu-id="ce57d-111">Ein Rollencenter ist eine Art Seite, auf die Sie verschiedene Teile setzen können.</span><span class="sxs-lookup"><span data-stu-id="ce57d-111">A Role Center is a type of page on which you can place different parts.</span></span> <span data-ttu-id="ce57d-112">Jeder Teil ist ein Container, in dem Sie andere Seiten oder vordefinierte Systemteilen hosten können, wie etwa ein Outlook-Teil oder Teile für das Hinzufügen von Aufgaben, von Benachrichtigungen oder von Notizen.</span><span class="sxs-lookup"><span data-stu-id="ce57d-112">Each part is a container in which you can host other pages or pre-defined system parts, such as an Outlook part or parts for adding tasks, notifications, or notes.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ce57d-113">In der aktuellen Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] können Sie keine Profile einfügen, ändern oder löschen.</span><span class="sxs-lookup"><span data-stu-id="ce57d-113">In the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)], you cannot add, edit, or delete profiles.</span></span>  

## <a name="configuration-and-personalization"></a><span data-ttu-id="ce57d-114">Konfiguration und Anpassung</span><span class="sxs-lookup"><span data-stu-id="ce57d-114">Configuration and Personalization</span></span>
<span data-ttu-id="ce57d-115">Das Konzept der UI-Anpassung in [!INCLUDE[d365fin](includes/d365fin_md.md)] wird in zwei Teile untergliedert</span><span class="sxs-lookup"><span data-stu-id="ce57d-115">The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:</span></span>  

-   <span data-ttu-id="ce57d-116">Konfiguration, ausgeführt vom Administrator</span><span class="sxs-lookup"><span data-stu-id="ce57d-116">Configuration, performed by the administrator</span></span>  

-   <span data-ttu-id="ce57d-117">Anpassung, ausgeführt von Benutzern</span><span class="sxs-lookup"><span data-stu-id="ce57d-117">Personalization, performed by users</span></span>  

<span data-ttu-id="ce57d-118">Der Administrator konfiguriert die Benutzeroberfläche für mehrere Benutzer, indem er die Benutzeroberfläche für ein Profil anpasst, dem die Benutzer zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="ce57d-118">The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.</span></span>  

<span data-ttu-id="ce57d-119">Benutzer personalisieren die Benutzeroberfläche ihrer persönlichen Version, indem sie die Benutzeroberfläche unter ihrer eigenen Benutzeranmeldung anpassen.</span><span class="sxs-lookup"><span data-stu-id="ce57d-119">Users personalize the user interface of their personal version by customizing the user interface under their own user logon.</span></span> <span data-ttu-id="ce57d-120">Diese Anpassung kann vom Administrator gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="ce57d-120">This personalization can be deleted by the administrator.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ce57d-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce57d-121">See Also</span></span>  
[<span data-ttu-id="ce57d-122">Benutzer und ihre Berechtigungen verwalten</span><span class="sxs-lookup"><span data-stu-id="ce57d-122">Managing Users and Permissions</span></span>](ui-how-users-permissions.md)  
<!-- [Customize the User Interface](../customize-the-user-interface.md)   
 [Security Overview](../Security%20Overview.md)-->

