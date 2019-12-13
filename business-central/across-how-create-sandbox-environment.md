---
title: Erstellen Sie eine Sandkastenumgebung| Microsoft Docs
description: Erstellen Sie somit eine Umgebung für das Untersuchen, Lernen, Entwickeln und Testen.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 12/06/2019
ms.author: solsen
ms.openlocfilehash: 0f8f0f85df89c1d71fc3e114ebd902f2aa85f802
ms.sourcegitcommit: b6e506a45a1cd632294bafa1c959746cc3a144f6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896109"
---
# <a name="creating-a-sandbox-environment-in-include-prodshortincludesprodshortmd"></a><span data-ttu-id="5a496-103">Erstellen einer Sandkastenumgebung in [!INCLUDE [prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="5a496-103">Creating a Sandbox Environment in [!INCLUDE [prodshort](includes/prodshort.md)]</span></span>

<span data-ttu-id="5a496-104">Mit [!INCLUDE [prodshort](includes/prodshort.md)] können Sie auf einfache Weise eine sichere Umgebung schaffen, in der Sie testen, trainieren oder Fehler beheben können, ohne die Arbeitsprozesse oder Geschäftsdaten Ihres Unternehmens zu beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="5a496-104">With [!INCLUDE [prodshort](includes/prodshort.md)], you can easily create a safe environment where you can test, train, or troubleshoot without disturbing your company's work processes or business data.</span></span> <span data-ttu-id="5a496-105">Eine solche Nichtproduktionsumgebung heißt *Sandbox*.</span><span class="sxs-lookup"><span data-stu-id="5a496-105">Such a non-production environment is called a *sandbox*.</span></span> <span data-ttu-id="5a496-106">Isoliert von der Produktion ist eine Sandboxumgebung der Ort, um den Dienst sicher zu untersuchen, erfahren, testen und entwickeln, ohne das Risiko des Beeinflussens der Daten und Einstellungen Ihrer Fertigungsumgebungen zur riskieren.</span><span class="sxs-lookup"><span data-stu-id="5a496-106">Isolated from production, a sandbox environment is the place to safely explore, learn, demo, develop, and test the service without the risk of affecting the data and settings of your production environment.</span></span>  

<span data-ttu-id="5a496-107">Ihr Administrator kann Sandboxumgebungen im [Admin Center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json) erstellen, aber wenn Sie schnell etwas testen möchten, können Sie eine Sandboxumgebung aus [!INCLUDE [prodshort](includes/prodshort.md)] heraus erstellen.</span><span class="sxs-lookup"><span data-stu-id="5a496-107">Your administrator can create sandbox environments in the [administration center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), but if you want to quickly test something, you can create a sandbox environment from inside [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>  

> [!NOTE]
> <span data-ttu-id="5a496-108">Technisch gesehen unterscheiden sich Sandboxumgebungen stark von Produktionsumgebungen, selbst wenn Ihr Administrator eine Sandbox erstellt, die Produktionsdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="5a496-108">Technically, sandbox environments are very different from production environments, even if your administrator creates a sandbox that includes production data.</span></span> <span data-ttu-id="5a496-109">Sie können keine Sandbox für das Benchmarking verwenden und beispielsweise keinen Datenbankexport anfordern.</span><span class="sxs-lookup"><span data-stu-id="5a496-109">You cannot use a sandbox for benchmarking, and you cannot request a database export, for example.</span></span> <span data-ttu-id="5a496-110">Wenn Sie eine Sandbox für das Benchmarking erstellen möchten, kann Ihr Administrator im Admin Center eine dedizierte Produktionsumgebung erstellen.</span><span class="sxs-lookup"><span data-stu-id="5a496-110">If you want to create a sandbox for benchmarking, your administrator can create a dedicated production environment in the administration center.</span></span> <span data-ttu-id="5a496-111">Weitere Informationen finden Sie unter [Umgebungstypen](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments).</span><span class="sxs-lookup"><span data-stu-id="5a496-111">For more information, see [Types of environments](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments).</span></span>

## <a name="to-create-a-sandbox-environment-in-your-include-prodshortincludesprodshortmd"></a><span data-ttu-id="5a496-112">So erstellen Sie eine Umgebung in Ihrer [!INCLUDE [prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="5a496-112">To create a sandbox environment in your [!INCLUDE [prodshort](includes/prodshort.md)]</span></span>

1. <span data-ttu-id="5a496-113">Melden Sie sich bei Ihrer Produktionsinstanz von [!INCLUDE[d365fin](includes/d365fin_md.md)] an.</span><span class="sxs-lookup"><span data-stu-id="5a496-113">Sign in to your production instance of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

2. <span data-ttu-id="5a496-114">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Sandboxumgebung** ein und wählen Sie dann den verknüpften Link.</span><span class="sxs-lookup"><span data-stu-id="5a496-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sandbox Environment**, and then choose the related link.</span></span>
    <!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. <span data-ttu-id="5a496-115">Klicken Sie auf die Schaltfläche **Erstellen**.</span><span class="sxs-lookup"><span data-stu-id="5a496-115">Choose the **Create** button.</span></span>  

    <span data-ttu-id="5a496-116">Eine weitere Registerkarte mit [!INCLUDE[d365fin](includes/d365fin_md.md)] wird geöffnet, in der Sie die Einrichtung Ihrer Sandbox-Umgebung abschließen können.</span><span class="sxs-lookup"><span data-stu-id="5a496-116">Another tab with [!INCLUDE[d365fin](includes/d365fin_md.md)] opens where you can finish the setup of your sandbox environment.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="5a496-117">Wenn Sie Popupblocker aktiviert haben in Ihrem Browser, bearbeiten sie diese, um URLs der \*.businesscentral.dynamics.com-Adresse zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="5a496-117">If you have pop-up blocker enabled in your browser, change it to allow URLs from the \*.businesscentral.dynamics.com address.</span></span>

<span data-ttu-id="5a496-118">Wenn die Sandkastenumgebung bereitsteht, werden Sie zum Begrüßung-Assistenten der Sandkastenumgebung umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="5a496-118">When the sandbox environment is ready, you will be redirected to sandbox environment's Welcome wizard.</span></span>
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

<span data-ttu-id="5a496-119">Sie können die Schaltfläche **Mehr erfahren** wählen, um Informationen zu Entwicklerszenarien zu erhalten, die Sie in einer Sandboxumgebung ausprobieren können oder wählen Sie die Schaltfläche **Schließen**, um zum Rollencenter Ihrer [!INCLUDE[d365fin](includes/d365fin_md.md)] Sandboxinstanz zu gelangen.</span><span class="sxs-lookup"><span data-stu-id="5a496-119">You can choose the **Learn more** button to read about developer scenarios that you can try in a sandbox environment or choose the **Close** button to continue to the Role Center of your [!INCLUDE[d365fin](includes/d365fin_md.md)] sandbox instance.</span></span>

<span data-ttu-id="5a496-120">Oben im Rollencenters wird eine Benachrichtigung angezeigt, die bestätigt, dass dies eine Sandkastenumgebung ist.</span><span class="sxs-lookup"><span data-stu-id="5a496-120">At the top of the Role Center, a notification appears to inform you that this is a sandbox environment.</span></span> <span data-ttu-id="5a496-121">Der Typ dieser Umgebung wird in der Titelleiste des Clients anzeigen.</span><span class="sxs-lookup"><span data-stu-id="5a496-121">You can also see the type of the environment in the title bar of the client.</span></span>
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> <span data-ttu-id="5a496-122">Eine auf diese Weise erstellte Sandbox-Umgebung enthält nur die Standarddemonstrationsdaten für das CRONUS Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="5a496-122">A sandbox environment created in this way only contains the default demonstration data for the CRONUS company.</span></span> <span data-ttu-id="5a496-123">Keine Daten werden kopiert oder anderswie von der Fertigungsumgebungen während der Sandkastenerstellung transferiert.</span><span class="sxs-lookup"><span data-stu-id="5a496-123">No data is copied or otherwise transferred from the production environment.</span></span><br /><br />
> <span data-ttu-id="5a496-124">Sie können auch eine Sandbox-Umgebung erstellen, die die Produktionsdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="5a496-124">You can also create a sandbox environment containing the production data.</span></span> <span data-ttu-id="5a496-125">Sie müssen dies über die Verwaltungszentrale tun.</span><span class="sxs-lookup"><span data-stu-id="5a496-125">You must do this through the administration center.</span></span> <span data-ttu-id="5a496-126">Weitere Informationen finden Sie unter [Umgebung verwalten](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) in der Entwickler- und IT-Profi-Hilfe.</span><span class="sxs-lookup"><span data-stu-id="5a496-126">For more information, see [Managing Environments](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) in the Developer and IT-Pro help.</span></span>

<span data-ttu-id="5a496-127">Jederzeit können Sie zur Seite **Sandkastenumgebung** zurückkehren und die Sandkastenumgebung zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="5a496-127">At any time, you can return to the **Sandbox Environment** page, and reset the sandbox environment.</span></span>

> [!NOTE]  
> <span data-ttu-id="5a496-128">Das Zurücksetzen der Sandkastenmgebung, wird sie komplett entfernen und dann wieder erstellt mit den Vorgabe-Demodaten.</span><span class="sxs-lookup"><span data-stu-id="5a496-128">Resetting the sandbox environment will remove it completely, and then create it again with the default demonstration data.</span></span>  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

<span data-ttu-id="5a496-129">Ein Administrator kann den Zugriff für einige Benutzer zur Sandboxumgebung begrenzen oder sogar sperren.</span><span class="sxs-lookup"><span data-stu-id="5a496-129">An administrator can limit or even block access for some users to the sandbox environment.</span></span> <span data-ttu-id="5a496-130">Dies kann geschehen, indem die Standardsicherheitsfunktionen des Produkts, wie die Benutzerkarte, die Benutzergruppen und die Berechtigungssätze verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5a496-130">This can be done by using the standard security features of the product, such as the User card, user groups, and permission sets.</span></span> <span data-ttu-id="5a496-131">Weitere Informationen finden Sie unter [Berechtigungen für Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="5a496-131">For more information, see [Assign Permissions to Users and Groups](ui-define-granular-permissions.md).</span></span>  

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a><span data-ttu-id="5a496-132">Erweiterte Funktionen der Sandkastenumgebung</span><span class="sxs-lookup"><span data-stu-id="5a496-132">Advanced Functionality in the Sandbox Environment</span></span>

<span data-ttu-id="5a496-133">Die Sandboxumgebung ist nicht zuletzt deshalb nützlich, weil sie einige nützliche Funktionen enthält.</span><span class="sxs-lookup"><span data-stu-id="5a496-133">The sandbox environment is not least useful because it includes a couple of handy features.</span></span>

### <a name="designer"></a><span data-ttu-id="5a496-134">Designerin</span><span class="sxs-lookup"><span data-stu-id="5a496-134">Designer</span></span>

<span data-ttu-id="5a496-135">In einer Sandboxumgebung finden Sie den **Designer** aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5a496-135">In a sandbox environment, you will find the **Designer** enabled.</span></span> <span data-ttu-id="5a496-136">Sie können Designer aktivieren, indem Sie das Entwurfssymbol ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) auf einer Seite auswählen oder durch Auswahl des Menüelements **Entwurf** im Einstellungsmenü ![Einstellungen](media/ui-experience/settings_icon_small.png).</span><span class="sxs-lookup"><span data-stu-id="5a496-136">You can activate Designer by selecting the design icon ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) on a page, or by choosing the **Design** menu item in the ![Settings](media/ui-experience/settings_icon_small.png) Settings menu.</span></span>

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

### <a name="to-enable-the-advanced-user-experience"></a><span data-ttu-id="5a496-137">Aktivieren Sie die erweiterte Benutzererfahrung</span><span class="sxs-lookup"><span data-stu-id="5a496-137">To enable the advanced user experience</span></span>
<span data-ttu-id="5a496-138">Es ist möglich, die erweiterte (vollständige) Funktion eines Sandkastentenants in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu aktivieren, indem Sie das Feld **Erfahrung** auf der Seite **Firmendaten** einrichten.</span><span class="sxs-lookup"><span data-stu-id="5a496-138">It is possible to enable and try the advanced (full) functionality of [!INCLUDE[d365fin](includes/d365fin_md.md)] in a sandbox tenant by setting the **Experience** field on the **Company Information** page.</span></span>

<!-- ![Sandbox Environment Advanced](./media/across-sandbox/sandbox-advanced.png) -->

<!-- ![Sandbox Production](./media/across-sandbox/sandbox-production.png) -->

<span data-ttu-id="5a496-139">Nachdem Sie die Funktion erweiterter Funktionalität in einem Sandkastentenant aktiviert haben, erhalten Sie Zugriff auf alle Standardprofile (Rollen) und Rollencenter.</span><span class="sxs-lookup"><span data-stu-id="5a496-139">After you have enabled the advanced functionality in a sandbox tenant, you get access to all the standard profiles (roles) and Role Centers.</span></span> <span data-ttu-id="5a496-140">Sie können einen Auswertungsmandanten erstellen, der vollständig eingerichtet wird, einschließlich Demodaten und Zugriff in den erweiterten Bereichen des Produkts.</span><span class="sxs-lookup"><span data-stu-id="5a496-140">You can also create an evaluation company that is fully set up, including demonstration data and access to the advanced areas of the product.</span></span>

<!-- ![Sandbox New Company](./media/across-sandbox/sandbox-newcompany.png) -->

## <a name="see-also"></a><span data-ttu-id="5a496-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a496-141">See Also</span></span>

<span data-ttu-id="5a496-142">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5a496-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="5a496-143">[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]-Testversionen und Abonnements](across-preview.md)</span><span class="sxs-lookup"><span data-stu-id="5a496-143">[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] Trials and Subscriptions](across-preview.md)</span></span>  
[<span data-ttu-id="5a496-144">Verwalten von Umgebungen im Business Central Admin Center</span><span class="sxs-lookup"><span data-stu-id="5a496-144">Managing Environments in the Business Central administration center</span></span>](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  
