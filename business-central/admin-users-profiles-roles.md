---
title: Verwalten von Rollen und Benutzer | Microsoft Docs
description: Erfahren, wie Benutzer, Profile und Rollencenter in Finanzen and Operations, Business Central verwaltet werden.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: profiles, users
ms.date: 08/02/2019
ms.author: edupont
ms.openlocfilehash: 27a57490101195f8dc05cc39538260e7db5e46af
ms.sourcegitcommit: 5bcc5f95e450ee9a3d9f7a380e592a5e75c4185b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2019
ms.locfileid: "1858220"
---
# <a name="understanding-users-roles-and-profiles"></a><span data-ttu-id="7c822-103">Benutzer, Rollen und  Profile verstehen</span><span class="sxs-lookup"><span data-stu-id="7c822-103">Understanding Users, Roles, and Profiles</span></span>

<span data-ttu-id="7c822-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], werden Benutzer von einem Administrator hinzugefügt, der auch Zugriff auf den Bereichen aus Feld [!INCLUDE[d365fin](includes/d365fin_md.md)] gibt, den sie, in ihrer Arbeit benötigen.</span><span class="sxs-lookup"><span data-stu-id="7c822-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], users are added by an administrator who also gives users access to the areas of [!INCLUDE[d365fin](includes/d365fin_md.md)] that they need in their work.</span></span>  

<span data-ttu-id="7c822-105">Zugriff auf die Funktionalität wird durch *Benutzergruppen* und *Profile (Rollen)* verwaltet.</span><span class="sxs-lookup"><span data-stu-id="7c822-105">Access to functionality is managed through *user groups* and *profiles (roles)*.</span></span> <span data-ttu-id="7c822-106">Als Administrator können Sie Profile zuordnen und ändern, und Sie können Benutzer als Teil des [!INCLUDE[d365fin](includes/d365fin_md.md)] Abonnements hinzufügen und  entfernen.</span><span class="sxs-lookup"><span data-stu-id="7c822-106">As an administrator, you can add and remove users as part of your [!INCLUDE[d365fin](includes/d365fin_md.md)] subscription, and you can assign users permissions through user groups.</span></span>  

## <a name="adding-users"></a><span data-ttu-id="7c822-107">Hinzufügen von Benutzern</span><span class="sxs-lookup"><span data-stu-id="7c822-107">Adding Users</span></span>

<span data-ttu-id="7c822-108">Um Benutzer in [!INCLUDE[d365fin](includes/d365fin_md.md)] online hinzuzufügen, muss der Office 365-Administrator Ihres Unternehmens zuerst einen Benutzer im Office 365-Admin Center erstellen.</span><span class="sxs-lookup"><span data-stu-id="7c822-108">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)] online, your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="7c822-109">Weitere Informationen sind hier verfügbar [Benutzer zu Office 365 for Business hinzufügen](https://aka.ms/CreateOffice365Users).</span><span class="sxs-lookup"><span data-stu-id="7c822-109">For more information, see [Add Users to Office 365 for business](https://aka.ms/CreateOffice365Users).</span></span>

<span data-ttu-id="7c822-110">Dann kann der Administrator Berechtigungen jedem Benutzerund Benutzergruppen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="7c822-110">Then, the administrator can assign permissions to each user and groups of users.</span></span> <span data-ttu-id="7c822-111">Weitere Informationen finden Sie unter [Verwalten von Benutzern und Berechtigungen](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="7c822-111">For more information, see [Managing Users and Permissions](ui-how-users-permissions.md).</span></span>  

<span data-ttu-id="7c822-112">Die leistungsstarksten Berechtigungen, die ein Benutzer haben kann, ist der SUPER-Berechtigungssatz.</span><span class="sxs-lookup"><span data-stu-id="7c822-112">The most powerful permissions that a user can have is the SUPER permission set.</span></span> <span data-ttu-id="7c822-113">Jeder Mandant muss mindestens einen Benutzer mit diesem Berechtigungssatz haben, aber es ist ein Verfahren, jedem Benutzer Berechtigungen zu geben, die ihren Arbeitsanforderungen in [!INCLUDE[prodshort](includes/prodshort.md)] entsprechen und nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="7c822-113">Each company must have at least one user with this permission set, but it is a best practice to give each user permissions that match their work needs in [!INCLUDE[prodshort](includes/prodshort.md)] and not more than that.</span></span> <span data-ttu-id="7c822-114">Dies ist hilfreich, um sicherzustellen, dass Benutzer nur Zugriff auf Daten haben, die für ihre Arbeit wichtig sind.</span><span class="sxs-lookup"><span data-stu-id="7c822-114">This helps ensure that users only have access to data that is relevant to their work, for example.</span></span>  

> [!TIP]
> <span data-ttu-id="7c822-115">Es ist eine Verfahren, sicherzustellen, dass auch der Office 365 Administrator den SUPER-Berechtigungssatz hat in [!INCLUDE[prodshort](includes/prodshort.md)], weil dies Verwaltungsaufgaben viele einfacher macht, einschließlich Aufstellungsintegration mit anderen Apps.</span><span class="sxs-lookup"><span data-stu-id="7c822-115">It's a best practice to make sure that the Office 365 administrator also has the SUPER permission set in [!INCLUDE[prodshort](includes/prodshort.md)] because that makes many administrative tasks easier, including setting up integration with other apps.</span></span>

### <a name="users-of-on-premises-deployments"></a><span data-ttu-id="7c822-116">Lokale Bereitstellungen von Benutzern</span><span class="sxs-lookup"><span data-stu-id="7c822-116">Users of on-premises deployments</span></span>

<span data-ttu-id="7c822-117">Für lokale Bereitstellungen von [!INCLUDE[d365fin](includes/d365fin_md.md)] kann der Administrator zwischen verschiedenen Autorisierungsmechanismen für Benutzer auswählen.</span><span class="sxs-lookup"><span data-stu-id="7c822-117">For on-premises deployments of [!INCLUDE[d365fin](includes/d365fin_md.md)], the administrator can choose between different credential authorization mechanisms for users.</span></span> <span data-ttu-id="7c822-118">Wenn Sie einen Benutzer erstellen, stellen Sie je nach Anmeldeinformationstyp in der aktuellen [!INCLUDE[server](includes/server.md)]-Instanz verschiedene Informationen bereit.</span><span class="sxs-lookup"><span data-stu-id="7c822-118">Then, when you create a user, you provide different information depending on the credential type that you are using in the specific [!INCLUDE[server](includes/server.md)] instance.</span></span> <span data-ttu-id="7c822-119">Weitere Informationen finden Sie unter [Authentifizierungs- und Anmeldeinformationstypen](/dynamics365/business-central/dev-itpro/administration/users-credential-types) im Abschnitt Verwaltung des Entwicklers und des ITPro-Inhalts für. [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="7c822-119">For more information, see the [Authentication and Credential Types](/dynamics365/business-central/dev-itpro/administration/users-credential-types) in the Administration section of the developer and ITPro content for [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="profiles-roles"></a><span data-ttu-id="7c822-120">Rollenprofile (Rollen)</span><span class="sxs-lookup"><span data-stu-id="7c822-120">Profiles (Roles)</span></span>

<span data-ttu-id="7c822-121">Alle Mitarbeiter in Ihrem Mandanten, die Zugriff haben auf [!INCLUDE[d365fin](includes/d365fin_md.md)] sind einer Rolle zugewiesen, das Zugriff auf das *Rollencenter* gibt.</span><span class="sxs-lookup"><span data-stu-id="7c822-121">The people in your company who have access to [!INCLUDE[d365fin](includes/d365fin_md.md)] are all assigned a role that gives them access to a *Role Center*.</span></span>

<span data-ttu-id="7c822-122">Profile sind Sammlungen von [!INCLUDE[d365fin](includes/d365fin_md.md)] Benutzern, die dasselbe Rollencenter nutzen.</span><span class="sxs-lookup"><span data-stu-id="7c822-122">Profiles are collections of [!INCLUDE[d365fin](includes/d365fin_md.md)] users who share the same role.</span></span> <span data-ttu-id="7c822-123">Ein Rollencenter ist der Einstiegspunkt und die Homepage für [!INCLUDE[d365fin](includes/d365fin_md.md)] und gibt Ihnen Zugriff zu den wichtigsten Aufgaben und zeigt verschiedene Einblicke und Schlüsselleistungsindikatoren (KPIs) über Ihre Arbeit an.</span><span class="sxs-lookup"><span data-stu-id="7c822-123">A Role Center is the entry point and home page for [!INCLUDE[d365fin](includes/d365fin_md.md)] that gives you quick access to your most important tasks and displays various insights and key performance indicators (KPIs) about your work.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="7c822-124">In der aktuellen Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] online können Sie keine Profile einfügen, ändern oder löschen.</span><span class="sxs-lookup"><span data-stu-id="7c822-124">In the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] online, you cannot add, edit, or delete profiles.</span></span>  

### <a name="CreateProfile"></a><span data-ttu-id="7c822-125">So erstellen Sie ein Profil</span><span class="sxs-lookup"><span data-stu-id="7c822-125">To create a profile</span></span>

1.  <span data-ttu-id="7c822-126">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen") aus, geben Sie **Profile** ein, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="7c822-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Profiles**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="7c822-127">Auf der Seite **Profile** wählen Sie die **Neu** Aktion aus, um die Seite **Neue Profil-Karte** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7c822-127">On the **Profiles** page, choose the **New** action to open the **New Profile Card** page.</span></span>  

3.  <span data-ttu-id="7c822-128">Geben Sie im Feld **Profil-ID** einen Namen ein, der die gewünschte Rolle des Benutzers beschreibt.</span><span class="sxs-lookup"><span data-stu-id="7c822-128">In the **Profile ID** field, enter a name that describes the intended role of the users.</span></span>  

4.  <span data-ttu-id="7c822-129">Geben Sie im Feld **Beschreibung** eine Beschreibung der Profil-ID, beispielsweise **Auftragsverarbeitung** ein.</span><span class="sxs-lookup"><span data-stu-id="7c822-129">In the **Description** field, enter a description of the Profile ID, for example, **Order Processor**.</span></span>  

5.  <span data-ttu-id="7c822-130">Legen Sie das Feld **Rollencenter-ID** auf das Rollencenter fest, das Sie dem Profil zuweisen wollen.</span><span class="sxs-lookup"><span data-stu-id="7c822-130">Set the **Role Center ID** field to the Role Center that you want to assign to the profile.</span></span>  

<span data-ttu-id="7c822-131">Das Verfahren zum Ändern eines vorhandenen Profils ist dasselbe, außer dass Sie ein vorhandenes Profil auf der Seite **Profile** auswählen, anstatt auf **Neu** zu klicken.</span><span class="sxs-lookup"><span data-stu-id="7c822-131">The procedure for modifying an existing profile is the same, except you select an existing profile on the **Profiles** page instead of choosing the **New** action.</span></span>  


### <a name="copy-a-profile"></a><span data-ttu-id="7c822-132">So kopieren Sie ein Profil</span><span class="sxs-lookup"><span data-stu-id="7c822-132">Copy a profile</span></span>
<span data-ttu-id="7c822-133">Durch Kopieren eines Profils sparen Sie Zeit, wenn Sie ähnlichen Einstellungen in einem Profil verwenden möchten und nur einige wenige Einstellungen ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="7c822-133">Copying a profile can save you time if you want to use similar settings on a profile and you only want to change a few settings.</span></span>

1.  <span data-ttu-id="7c822-134">Öffnen Sie das Profil, das Sie kopieren möchten, und wählen Sie dann die Aktion **Profil kopieren** aus.</span><span class="sxs-lookup"><span data-stu-id="7c822-134">Open the profile that you want to copy, and then choose the **Copy Profile** action.</span></span>

2.  <span data-ttu-id="7c822-135">Geben Sie im Feld **Neue Profil-ID** einen Namen für das zu kopierende Profil ein.</span><span class="sxs-lookup"><span data-stu-id="7c822-135">In **New Profile ID** field, enter a name for the profile that you want to copy.</span></span>

3.  <span data-ttu-id="7c822-136">Legen Sie das Feld **Neuer Profilbereich** auf eines der Folgenden fest:</span><span class="sxs-lookup"><span data-stu-id="7c822-136">Set the **New Profile Scope** field to one of the following:</span></span>

    - <span data-ttu-id="7c822-137">**System**, damit das neue Profil für alle Tenantdatenbanken verfügbar ist, die die Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="7c822-137">**System** to make the new profile available to all tenant databases that use the application.</span></span>
    - <span data-ttu-id="7c822-138">**Tenant**, damit das neue Profil nur der aktuellen Tenantdatenbank zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="7c822-138">**Tenant** to make the new profile available to just the current tenant database.</span></span>
4. <span data-ttu-id="7c822-139">Wenn Sie fertig sind, wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="7c822-139">Choose the **OK** button when done.</span></span>

### <a name="ExportImportProfile"></a><span data-ttu-id="7c822-140">Exportieren und Importieren von Profilen</span><span class="sxs-lookup"><span data-stu-id="7c822-140">Export and import profiles</span></span>

<span data-ttu-id="7c822-141">Sie können Profile als XML-Dateien aus und nach einer [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datenbank exportieren, bzw. importieren.</span><span class="sxs-lookup"><span data-stu-id="7c822-141">You can export and import profiles as XML files to and from the a [!INCLUDE[d365fin](includes/d365fin_md.md)] database.</span></span> <span data-ttu-id="7c822-142">Durch das Exportieren und das Importieren eines Profils können Sie Zeit speichern, wenn Sie die Benutzeroberfläche konfigurieren, da Sie eine vorhandene Profilkonfiguration wieder verwenden, statt ein Profil von Grund auf neu konfigurieren zu müssen.</span><span class="sxs-lookup"><span data-stu-id="7c822-142">Exporting and importing a profile can save you time when configuring the user interface because you reuse an existing profile configuration instead of having to configure a profile from scratch.</span></span> <span data-ttu-id="7c822-143">Wenn Sie ein Profil haben, das in einer [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datenbank konfiguriert ist und Sie alle oder einige derselben Profilkonfigurationen in einer anderen Datenbank erneut verwenden möchten, können Sie das Profil in eine XML-Datei exportieren.</span><span class="sxs-lookup"><span data-stu-id="7c822-143">If you have a profile that is configured in a [!INCLUDE[d365fin](includes/d365fin_md.md)] database and you would like to reuse all or some of the same profile configurations in another database, you can export the profile to an XML file.</span></span> <span data-ttu-id="7c822-144">Anschließend können Sie die XML-Profildatei in die andere Datenbank importieren.</span><span class="sxs-lookup"><span data-stu-id="7c822-144">Then, you can import the profile XML file into the other database.</span></span>

-   <span data-ttu-id="7c822-145">Um ein Profil zu exportieren, können Sie die **Profile exportieren** Aktion aus **Profilübersicht** oder **Profilkarte** auswählen oder Sie können **Profile exportieren** suchen.</span><span class="sxs-lookup"><span data-stu-id="7c822-145">To export a profile, you can either choose the **Export Profiles** action from the **Profile List** or **Profile Card** page or you can search for and open the **Export Profiles** page.</span></span> <span data-ttu-id="7c822-146">Speichern Sie die XML-Datei an einem Speicherort auf Ihrem Computer oder Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="7c822-146">Save the XML file to a location on your computer or network.</span></span>

-   <span data-ttu-id="7c822-147">Um ein Profil zu importieren, können Sie die **Profile importieren** Aktion aus Profilübersicht oder **Profilliste** auswählen oder Sie können **Profile importieren** suchen.</span><span class="sxs-lookup"><span data-stu-id="7c822-147">To import a profile, you can either choose the **Import Profile** action from the **Profile List** page, or you can search for and open the **Import Profiles** page.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="7c822-148">Sie können kein Profil importieren, das bereits in der Datenbank vorhanden ist, auch wenn die XML-Datei einen anderen Namen oder unterschiedlichen Inhalt hat.</span><span class="sxs-lookup"><span data-stu-id="7c822-148">You cannot import a profile that already exists in the database, even though the XML file is named differently or has different content.</span></span> <span data-ttu-id="7c822-149">Sie müssen das vorhandene Profil löschen, bevor Sie das neue Profil importieren können.</span><span class="sxs-lookup"><span data-stu-id="7c822-149">You must delete the existing profile before you can import the new profile.</span></span>


## <a name="configuration-and-personalization"></a><span data-ttu-id="7c822-150">Konfiguration und Anpassung</span><span class="sxs-lookup"><span data-stu-id="7c822-150">Configuration and Personalization</span></span>
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->

<span data-ttu-id="7c822-151">Benutzer personalisieren die Benutzeroberfläche ihrer persönlichen Version, indem sie die Benutzeroberfläche unter ihrer eigenen Benutzeranmeldung anpassen.</span><span class="sxs-lookup"><span data-stu-id="7c822-151">Users personalize the user interface of their personal version by customizing the user interface under their own user logon.</span></span> <span data-ttu-id="7c822-152">Diese Anpassung kann vom Administrator gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="7c822-152">This personalization can be deleted by the administrator.</span></span> <span data-ttu-id="7c822-153">Weitere Informationen finden Sie unter [Personalisieren Ihres Arbeitsbereichs](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="7c822-153">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="7c822-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c822-154">See Also</span></span>  
[<span data-ttu-id="7c822-155">Benutzer und ihre Berechtigungen verwalten</span><span class="sxs-lookup"><span data-stu-id="7c822-155">Managing Users and Permissions</span></span>](ui-how-users-permissions.md)  
[<span data-ttu-id="7c822-156">Personalisierung als Administrator verwalten</span><span class="sxs-lookup"><span data-stu-id="7c822-156">Managing Personalization as an Administrator</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="7c822-157">Personalisieren Ihres Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="7c822-157">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  
