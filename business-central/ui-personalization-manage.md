---
title: Verwaltung von Personalisierung als Administrator in Business Central | Microsoft Docs
description: Erfahren Sie, wie Sie die Benutzeroberfläche anpassen, damit diese Ihren Bedürfnissen entspricht.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 08/16/2019
ms.author: jswymer
ms.openlocfilehash: 268d61e05f84643abe8eeeb283bd035e0247fe1c
ms.sourcegitcommit: 81b6062194bf04d8052a3cd394cc0b41e3f53e6d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2019
ms.locfileid: "1887737"
---
# <a name="managing-personalization-as-an-administrator"></a><span data-ttu-id="e2cd4-103">Personalisierung als Administrator verwalten</span><span class="sxs-lookup"><span data-stu-id="e2cd4-103">Managing Personalization as an Administrator</span></span>

<span data-ttu-id="e2cd4-104"> Benutzer können ihren Arbeitsbereich personalisieren, um ihren Bedürfnissen zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-104">Users can personalize their workspace to suit their own preferences.</span></span> <span data-ttu-id="e2cd4-105">Als Administrator steuern und verwalten Sie Personalisierungen nach:</span><span class="sxs-lookup"><span data-stu-id="e2cd4-105">As an administrator, you control and manage personalization by:</span></span>

-   <span data-ttu-id="e2cd4-106">Aktivieren oder Deaktivieren der Personalisierungsfunktion für die gesamte Anwendung (nur lokale Installation).</span><span class="sxs-lookup"><span data-stu-id="e2cd4-106">Enabling or disabling the personalization feature for the entire the application (on-premises installation only).</span></span>
-   <span data-ttu-id="e2cd4-107">Aktivieren oder Deaktivieren der Personalisierungsfunktion für Benutzer eines bestimmten Profils.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-107">Enabling or disabling the personalization feature for users of a specific profile.</span></span>
-   <span data-ttu-id="e2cd4-108">Löschen aller Seitenanpassungen, die Benutzer vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-108">Clearing any page personalizations that users have made.</span></span>

## <a name="EnablePersonalization"></a> <span data-ttu-id="e2cd4-109">So aktivieren oder deaktivieren Sie Personalisierung (nur lokal)</span><span class="sxs-lookup"><span data-stu-id="e2cd4-109">To enable or disable personalization (On-Premises Only)</span></span>

<span data-ttu-id="e2cd4-110">Standardmäßig ist die Personalisierung im Client nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-110">By default, personalization is not enabled in the client.</span></span> <span data-ttu-id="e2cd4-111">Sie aktivieren oder deaktivieren die Personalisierung, indem Sie die Konfigurationsdatei (navsettings.json) der Business Central-Web Server-Instanz ändern, die dem Clients dient.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-111">You enable or disable personalization by modifying the configuration file (navsettings.json) of the Business Central Web Server instance that serves the clients.</span></span>

1. <span data-ttu-id="e2cd4-112">Um die Personalisierung zu aktivieren, müssen Sie die folgende Zeile in der navsettings.json-Datei hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="e2cd4-112">To enable personalization, add the following line in the navsettings.json file:</span></span>

    ```
    "PersonalizationEnabled": "true"
    ```

    <span data-ttu-id="e2cd4-113">Um die Personalisierung zu deaktivieren, entfernen Sie diese Zeile oder bearbeiten sie folgendermaßen:</span><span class="sxs-lookup"><span data-stu-id="e2cd4-113">To disable personalization, remove this line or change it to:</span></span>

    ```
    "PersonalizationEnabled": "false"
    ```

    <span data-ttu-id="e2cd4-114">Weitere Informationen darüber, wie Sie die navsettings.json-Datei ändern, finden Sie unter [Direktes Ändern der navsettings.json-Datei](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings)</span><span class="sxs-lookup"><span data-stu-id="e2cd4-114">For more information about how to modify the navsettings.json file, see [Modify the navsettings.json file directly](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings).</span></span>

2. <span data-ttu-id="e2cd4-115">Generieren Sie die Anwendungssymbole und laden Sie diese herunter.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-115">Generate and download the application symbols.</span></span>

    <span data-ttu-id="e2cd4-116">Dieser Schritt ist optional und nicht erforderlich, um die Personalisierung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-116">This step is optional, and not required to enable personalization.</span></span> <span data-ttu-id="e2cd4-117">Er stellt jedoch sicher, dass neue Seiten, die von den Entwicklern erstellt werden, angepasst werden können.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-117">However, it ensures that new pages that are created by developers can be personalized.</span></span>

    1. <span data-ttu-id="e2cd4-118">Zuerst generieren Sie die Symbole, indem Sie die finsql.exe mit dem Befehl `generatesymbolreference` ausführen.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-118">First, you generate the symbols by running finsql.exe with `generatesymbolreference` command.</span></span> <span data-ttu-id="e2cd4-119">Die finsql.exe-Datei befindet sich im Installationsordner für die [!INCLUDE[server](includes/server.md)]- und Dynamics NAV-Entwicklungsumgebung (CSIDE).</span><span class="sxs-lookup"><span data-stu-id="e2cd4-119">The finsql.exe file is located in the installation folder for the [!INCLUDE[server](includes/server.md)] and Dynamics NAV Development Environment (CSIDE).</span></span> <span data-ttu-id="e2cd4-120">Um die Symbole zu erstellen, öffnen Sie eine Eingabeaufforderung, navigieren zum Verzeichnis, in dem die Datei gespeichert ist, und führen folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="e2cd4-120">To generate the symbols, open a command prompt, change to the directory where the file is store, and the run the following command:</span></span>

        ```
        finsql.exe Command=generatesymbolreference, Database="<Database Name>", ServerName=<SQL Server Name\<Server Instance>
        ```
    <span data-ttu-id="e2cd4-121">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e2cd4-121">For example:</span></span>

        ```
        finsql.exe Command=generatesymbolreference, Database="Demo Database BC", ServerName=MySQLServer\BCDEMO
        ```

    <span data-ttu-id="e2cd4-122">Weitere Informationen finden Sie unter [Gleichzeitiges Ausführen von C/SIDE und AL](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).</span><span class="sxs-lookup"><span data-stu-id="e2cd4-122">For more information, see [Running C/SIDE and AL Side-by-Side](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).</span></span>

    2. <span data-ttu-id="e2cd4-123">Konfigurieren Sie die [!INCLUDE[nav_server_md](includes/nav_server_md.md)]-Instanz zu: **Laden der Anwendungssymbolverweise bei Serverstart aktivieren** (EnableSymbolLoadingAtServerStartup).</span><span class="sxs-lookup"><span data-stu-id="e2cd4-123">Configure [!INCLUDE[nav_server_md](includes/nav_server_md.md)] instance to **Enable loading application symbol references at server startup** (EnableSymbolLoadingAtServerStartup).</span></span> <span data-ttu-id="e2cd4-124">Weitere Informationen finden Sie unter [Konfigurieren von Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings).</span><span class="sxs-lookup"><span data-stu-id="e2cd4-124">For more information, see [Configuring Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings).</span></span>

## <a name="to-disable-personalization-for-a-profile"></a><span data-ttu-id="e2cd4-125">So deaktivieren Sie die Personalisierung für ein Profil</span><span class="sxs-lookup"><span data-stu-id="e2cd4-125">To disable personalization for a profile</span></span>

<span data-ttu-id="e2cd4-126">Sie können verhindern, dass alle Benutzer, die zu einem bestimmten Profil gehören, ihre Seiten personalisieren können.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-126">You can prevent all users that belong to a specific profile from being able to personalize their pages.</span></span>

1. <span data-ttu-id="e2cd4-127">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Profile** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Profiles**, and then choose the related link.</span></span>
2. <span data-ttu-id="e2cd4-128">Wählen Sie das Profil aus, das Sie ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-128">Select the profile in the list that you want to modify.</span></span>
3. <span data-ttu-id="e2cd4-129">Aktivieren Sie das Kontrollkästchen **Anpassung deaktivieren**, und klicken Sie dann auf die Schaltfläche **OK**.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-129">Select the **Disable personalization** check box, and then choose the **OK** button.</span></span>

> [!NOTE]  
> <span data-ttu-id="e2cd4-130">In Business Central Online können Sie die Personalisierung nur für ein Mandantenprofil deaktivieren, nicht für Systemprofile.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-130">In Business Central online, you can only disable personalization for a tenant profile, not for system profiles.</span></span> 

## <a name="to-clear-user-personalizations"></a><span data-ttu-id="e2cd4-131">So löschen Sie Benutzeranpassungen</span><span class="sxs-lookup"><span data-stu-id="e2cd4-131">To clear user personalizations</span></span>

<span data-ttu-id="e2cd4-132">Die Löschung der Seitenanpassung ändert die Seite oder erstellt das ursprüngliche Layout wieder.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-132">Clearing page personalization changes the page back to its original layout before any personalization was made.</span></span> <span data-ttu-id="e2cd4-133">Es gibt zwei Möglichkeiten, die Anpassungen zu löschen, die Benutzer auf Seiten vorgenommen haben: mit der Seite **Benutzeranpassung löschen** und mithilfe der Anwendung der Seite **Benutzeranpassungskarte**.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-133">There are two ways to clear the personalizations that users have made to pages: using the **Delete User Personalization** page and using the **User Personalization Card** page.</span></span>

### <a name="to-clear-user-personalizations-by-using-the-delete-user-personalization-page"></a><span data-ttu-id="e2cd4-134">So löschen Sie Benutzeranpassungen mithilfe der Seite "Benutzeranpassungen löschen"</span><span class="sxs-lookup"><span data-stu-id="e2cd4-134">To clear user personalizations by using the Delete User Personalization page</span></span>

<span data-ttu-id="e2cd4-135">Die Seite **Benutzeranpassung löschen** gibt Ihnen die Möglichkeit, die Personalisierung für eine Seite oder pro Benutzer zu löschen.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-135">The **Delete User Personalization** page enables you to clear personalizations on a per-page basis for each user individually.</span></span>

1. <span data-ttu-id="e2cd4-136">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Benutzeranpassung löschen** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-136">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="e2cd4-137">Die Seite führt alle Seiten auf, die angepasst wurden und den Benutzer, denen sie gehören.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-137">The page lists all the pages that have been personalized and the user it belongs to.</span></span>

    >[!NOTE]
    > <span data-ttu-id="e2cd4-138">Ein Häkchen in den Spalten **Vorgänger-Anpassung** bedeutet, dass die Personalisierung in einem vorherigen Version von, die erforderlich war [!INCLUDE[d365fin](includes/d365fin_md.md)]die Anpassung, Bearb die unterscheidet, als sie jetzt zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-138">A check mark in the **Legacy Personalization** columns indicates that the personalization was done in an older version of [!INCLUDE[d365fin](includes/d365fin_md.md)], which handled personalization different than it does now.</span></span> <span data-ttu-id="e2cd4-139">Benutzer, die versuchen, diese Seiten zu personalisieren, können dies nicht tun, es sei denn, sie entsperren die Seite.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-139">Users who try to personalize these pages are locked from doing so unless they choose to unlock the page.</span></span> <span data-ttu-id="e2cd4-140">Weitere Informationen finden Sie unter [Warum eine Seite zum Personalisieren gesperrt ist](ui-personalization-locked.md).</span><span class="sxs-lookup"><span data-stu-id="e2cd4-140">For more information, see [Why a page is locked from personalizing](ui-personalization-locked.md).</span></span>

2. <span data-ttu-id="e2cd4-141">Wählen Sie den Posten, den Sie löschen möchten, und wählen die Aktion **Löschen** aus.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-141">Select the entry that you want to delete, and then choose the **Delete** action.</span></span>

    <span data-ttu-id="e2cd4-142">Der Benutzer sieht die Änderungen das nächste Mal bei der Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-142">The user will see the changes the next time they sign-in.</span></span>

### <a name="to-clear-user-personalizations-by-using-the-user-personalization-card-page"></a><span data-ttu-id="e2cd4-143">So löschen Sie Benutzeranpassungen mithilfe der Seite "Benutzeranpassungskarte".</span><span class="sxs-lookup"><span data-stu-id="e2cd4-143">To clear user personalizations by using the User Personalization Card page</span></span>

<span data-ttu-id="e2cd4-144">Die Seite **Benutzeranpassungskarte** gibt Ihnen die Möglichkeit, die Personalisierung für alle Seiten für eijnen bestimmten Benutzer zu löschen.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-144">The **User Personalization Card** page enables you to clear the personalization on all pages for specific user.</span></span> <span data-ttu-id="e2cd4-145">Dazu müssen Sie die Schreibberechtigung für Tabelle 2000000072 **Profil** haben.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-145">This requires write permission to Table 2000000072 **Profile**.</span></span>

1. <span data-ttu-id="e2cd4-146">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Benutzeranpassung** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-146">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="e2cd4-147">Die Seite **Benutzeranpassung** führt alle Benutzer auf, die möglicherweise eine personalisierte Seite haben.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-147">The **User Personalization** page lists all users who potentially have personalized pages.</span></span> <span data-ttu-id="e2cd4-148">Wenn Sie einen Benutzer in der Übersicht nicht finden können, bedeutet dies, dass sie keine personalisierten Seiten haben.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-148">If you cannot find a user in the list, this means that they do not have any personalized pages.</span></span>

2. <span data-ttu-id="e2cd4-149">Wählen den Benutzer aus der Liste aus und wählen Sie dann die Aktion **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-149">Select the user from the list, and then choose the **Edit** action.</span></span>

3. <span data-ttu-id="e2cd4-150">Wählen Sie auf der Registerkarte **Aktionen** **Personalisierte Seiten löschen** aus.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-150">On the **Actions** tab, choose **Clear Personalized Pages**.</span></span>

    <span data-ttu-id="e2cd4-151">Der Benutzer sieht die Änderungen das nächste Mal bei der Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="e2cd4-151">The user will see the changes the next time they sign-in.</span></span>

## <a name="see-also"></a><span data-ttu-id="e2cd4-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2cd4-152">See Also</span></span>
[<span data-ttu-id="e2cd4-153">Personalisieren Ihres Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="e2cd4-153">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  
<span data-ttu-id="e2cd4-154">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e2cd4-154">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="e2cd4-155">Ändern von grundlegenden Einstellungen</span><span class="sxs-lookup"><span data-stu-id="e2cd4-155">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="e2cd4-156">Sie können auswählen, welche Funktionen angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="e2cd4-156">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
