---
title: Anpassen von Seiten für Rollen | Microsoft Docs
description: Erfahren Sie, wie Sie die Benutzeroberfläche für ein Profil (eine Rolle) anpassen, sodass allen Benutzern, die diese Rolle zugewiesen haben, ein benutzerdefinierter Arbeitsbereich angezeigt wird.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 470d2542864b8d0e0f16f89fd99e422807829404
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2310804"
---
# <a name="customize-pages-for-profiles"></a><span data-ttu-id="9f3bf-103">Seiten für Profile anpassen</span><span class="sxs-lookup"><span data-stu-id="9f3bf-103">Customize Pages for Profiles</span></span>
<span data-ttu-id="9f3bf-104">Benutzer können Seiten für ihren Arbeitsbereich personalisieren, um ihren Bedürfnissen zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-104">Users can personalize pages that make up their workspace to suit their own preferences.</span></span> <span data-ttu-id="9f3bf-105">Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="9f3bf-105">For more information, see [Personalize Your Workspace](ui-personalization-user.md).</span></span>

<span data-ttu-id="9f3bf-106">Administratoren können Seiten für ein Profil anpassen, z. B. entsprechend der jeweiligen Geschäftsrolle oder Abteilung, sodass allen Benutzern, denen das Profil zugewiesen ist, das angepasste Seitenlayout angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-106">Administrators can customize pages for a profile, according to the related business role or department, for example, so that all users that are assigned the profile will see the customized page layout.</span></span> <span data-ttu-id="9f3bf-107">Als Administrator passen Sie die Seiten an, indem Sie dieselben Funktionen verwenden wie Benutzer, wenn sie Personalisierungen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-107">The administrator customizes pages by using the same functionality as users do when they personalize pages.</span></span>

> [!NOTE]
> <span data-ttu-id="9f3bf-108">Die typische geschäftliche Verwendung eines Profils ist eine Rolle.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-108">The typical business use of a profile is a role.</span></span> <span data-ttu-id="9f3bf-109">Ein Profil wird daher *Profil (Rolle)* benannt in der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-109">A profile is therefore named *Profile (Role)* in the UI.</span></span>

<span data-ttu-id="9f3bf-110">Die Seitenanpassung beginnt mit **Profile (Rollen)** Seite, Ausgangspunkt des Administrators für die Verwaltung der Benutzerprofile auf einzelnen Profilkarten.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-110">Page customization starts from the **Profiles (Roles)** page, the administrator's starting point for managing users' profiles on individual profile cards.</span></span> <span data-ttu-id="9f3bf-111">Zusätzlich zum Anpassen des Seitenlayouts steuern Sie verschiedene andere Einstellungen für Profile in der **Profil (Rolle)** Seite für jedes Profil.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-111">In addition to customizing the page layout, you control various other settings for profiles on the **Profile (Role)** page for each profile.</span></span> <span data-ttu-id="9f3bf-112">Weitere Informationen finden Sie unter [Profile verwalten](admin-users-profiles-roles.md).</span><span class="sxs-lookup"><span data-stu-id="9f3bf-112">For more information, see [Manage Profiles](admin-users-profiles-roles.md).</span></span>

## <a name="to-customize-pages-for-a-profile"></a><span data-ttu-id="9f3bf-113">Um Seiten für ein Profil anzupassen</span><span class="sxs-lookup"><span data-stu-id="9f3bf-113">To customize pages for a profile</span></span>
1. <span data-ttu-id="9f3bf-114">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Profile (Rollen)** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Profiles (Roles)**, and then choose the related link.</span></span>
2. <span data-ttu-id="9f3bf-115">Wählen Sie dir Zeile für die Personalisierungsseite, die Sie löschen möchten, und wählen die Aktion **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-115">Select the line for the profile that you want to customize pages for, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="9f3bf-116">Wählen Sie die Aktion **Seiten anpassen**.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-116">Choose the **Customize pages** action.</span></span>

    [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="9f3bf-117">öffnet eine neue Browser-Registerkarte für das ausgewählte Profil mit dem Banner **Anpanssen** Banner aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-117">opens on a new browser tab for the selected profile with the **Customizing** banner activated.</span></span> <span data-ttu-id="9f3bf-118">Das **Anpassen** Banner bietet die gleiche Funktionalität wie das **Personalisierung** Banner, das den Benutzern zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-118">The **Customizing** banner offers the same functionality as the **Personalizing** banner that is available to users.</span></span>

4. <span data-ttu-id="9f3bf-119">Passen Sie die Seiten an die Anforderungen der jeweiligen Rolle oder Abteilung an, so wie es ein Benutzer bei der Personalisierung tun würde.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-119">Customize pages according to the needs of the role or department in question in the same way as a user would do when personalizing.</span></span> <span data-ttu-id="9f3bf-120">Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="9f3bf-120">For more information, see [Personalize Your Workspace](ui-personalization-user.md).</span></span>

    > [!NOTE]
    > <span data-ttu-id="9f3bf-121">Um während der Personalisierung zu navigieren, drücken Sie Strg + Klicken auf eine Aktion, wenn diese durch die Pfeilspitze hervorgehoben ist.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-121">To navigate during personalization, use Ctrl + Click on an action if it is highlighted by the arrowhead.</span></span>

5. <span data-ttu-id="9f3bf-122">Wenn Sie das Layout einer oder mehrerer Seiten geändert haben, wählen Sie die Schaltfläche **Fertig** im Banner **Anpassung**.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-122">When you have finished changing the layout on one or more pages, choose the **Done** button on the **Customizing** banner.</span></span>
6. <span data-ttu-id="9f3bf-123">Schließen Sie die Browser-Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-123">Close the browser tab.</span></span>

<span data-ttu-id="9f3bf-124">Die Anpassung von Seiten wird jetzt für das Profil aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-124">The customization of pages is now recorded for the profile.</span></span>

## <a name="to-view-all-customized-pages-for-a-profile"></a><span data-ttu-id="9f3bf-125">Um angepasste Seiten für ein Profil anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="9f3bf-125">To view all customized pages for a profile</span></span>
<span data-ttu-id="9f3bf-126">Sie können sich einen Überblick darüber verschaffen, welche Seiten für ein Profil angepasst wurden, um beispielsweise zu planen, welche Seiten weiter angepasst oder gelöscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-126">You can get an overview of which pages are customized for a profile, for example to plan which to customize further or delete.</span></span>

- <span data-ttu-id="9f3bf-127">Auf der **Profil (Rolle)** Seite, wählen Sie die **Angepasste Seiten** Aktion.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-127">On the **Profile (Role)** page, choose the **Customized Pages** action.</span></span>

## <a name="to-delete-all-customizations-for-a-profile"></a><span data-ttu-id="9f3bf-128">Löschen aller Anpassungen für ein Profil</span><span class="sxs-lookup"><span data-stu-id="9f3bf-128">To delete all customizations for a profile</span></span>
<span data-ttu-id="9f3bf-129">Sie können alle Anpassunge, die Sie für ein Profil vorgenommen haben, stornieren.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-129">You can cancel all customizations that you have made for a profile.</span></span> <span data-ttu-id="9f3bf-130">Mit einer Erweiterung eingeführte Anpassungen und von einem Benutzer vorgenommene Personalisierungen werden nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-130">Customizations introduced with an extension and personalizations made by a user will not be deleted.</span></span> <span data-ttu-id="9f3bf-131">Sie können alle Personalisierungen mit einer anderen Aktion löschen.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-131">You can delete all personalizations with another action.</span></span> <span data-ttu-id="9f3bf-132">Weitere Informationen finden Sie unter [Löscht alle von einem Benutzer vorgenommenen Personalisierungen](admin-users-profiles-roles.md#to-delete-all-personalizations-made-by-a-user).</span><span class="sxs-lookup"><span data-stu-id="9f3bf-132">For more information, see [To delete all personalizations made by a user](admin-users-profiles-roles.md#to-delete-all-personalizations-made-by-a-user).</span></span>

- <span data-ttu-id="9f3bf-133">Auf der **Profil (Rolle)** Seite wählen Sie auf der Seite für ein benutzerdefiniertes Profil die Option **Löschen Sie benutzerdefinierte Seiten** Aktion.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-133">On the **Profile (Role)** page for a customized profile, choose the **Clear customized pages** action.</span></span>

<span data-ttu-id="9f3bf-134">Das Seitenlayout für das Profil wird auf das Standardlayout zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-134">The layout on pages for the profile is reset to the default layout.</span></span>  

## <a name="to-delete-customization-for-specific-pages-for-a-profile"></a><span data-ttu-id="9f3bf-135">So löschen Sie die Anpassung für bestimmte Seiten eines Profils</span><span class="sxs-lookup"><span data-stu-id="9f3bf-135">To delete customization for specific pages for a profile</span></span>
<span data-ttu-id="9f3bf-136">Sie können auch alle individuellen Seitenanpassungen löschen, die Sie für ein gemacht haben.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-136">You can delete individual page customizations that you have made for a profile.</span></span> <span data-ttu-id="9f3bf-137">Mit einer Erweiterung eingeführte Anpassungen und von einem Benutzer vorgenommene Personalisierungen werden nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-137">Customizations introduced with an extension and personalizations made by a user will not be deleted.</span></span> <span data-ttu-id="9f3bf-138">Sie können eine bestimmte Seitenpersonalisierung mit einer anderen Aktion löschen.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-138">You can delete specific page personalizations with another action.</span></span> <span data-ttu-id="9f3bf-139">Weitere Informationen finden Sie unter [So löschen Sie alle Personalisierungen für bestimmte Seiten](admin-users-profiles-roles.md#to-delete-personalizations-for-specific-pages).</span><span class="sxs-lookup"><span data-stu-id="9f3bf-139">For more information, see [To delete personalizations for specific pages](admin-users-profiles-roles.md#to-delete-personalizations-for-specific-pages).</span></span>

1. <span data-ttu-id="9f3bf-140">Auf der **Profil (Rolle)** Seite, wählen Sie die **Angepasste Seiten** Aktion.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-140">On the **Profile (Role)** page, choose the **Customized Pages** action.</span></span>
2. <span data-ttu-id="9f3bf-141">Auf der Seite **Profilanpassungen** wählen Sie mindestens eine Zeile für die Seitenanpassungen aus, die Sie löschen möchten, und wählen Sie dann die Aktion **Löschen** aus.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-141">On the **Profile Customizations** page, select on or more lines for page customizations that you want to delete, and then choose the **Delete** action.</span></span>

<span data-ttu-id="9f3bf-142">Das Layout der ausgewählten Seiten wird an die von Ihnen vorgenommenen Änderungen angepasst.</span><span class="sxs-lookup"><span data-stu-id="9f3bf-142">The layout on the selected pages is adjusted to the changes you made.</span></span>

## <a name="see-also"></a><span data-ttu-id="9f3bf-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f3bf-143">See Also</span></span>
[<span data-ttu-id="9f3bf-144">Ihren Arbeitsbereich personalisieren</span><span class="sxs-lookup"><span data-stu-id="9f3bf-144">Personalize Your Workspace</span></span>](ui-personalization-user.md)  
[<span data-ttu-id="9f3bf-145">Profile verwalten</span><span class="sxs-lookup"><span data-stu-id="9f3bf-145">Manage Profiles</span></span>](admin-users-profiles-roles.md)  
[<span data-ttu-id="9f3bf-146">Ändern von grundlegenden Einstellungen</span><span class="sxs-lookup"><span data-stu-id="9f3bf-146">Change Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="9f3bf-147">Funktionen, die angezeigt werden ändern</span><span class="sxs-lookup"><span data-stu-id="9f3bf-147">Change Which Features are Displayed</span></span>](ui-experiences.md)  
<span data-ttu-id="9f3bf-148">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9f3bf-148">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
