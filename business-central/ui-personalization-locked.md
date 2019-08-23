---
title: Warum ich eine Seite nicht personalisieren | Microsoft Docs
description: Erklärt, warum Sie eine Seite nicht personalisieren können und was Sie tun können, um sie zu entsperren, sodass Sie sie anpassen können.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 1a3edaca2e76388d82ea8991c3196410dd9c7288
ms.sourcegitcommit: a88d1e9c0ab647cb8d9d81d32c0bdc82843f4145
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/31/2019
ms.locfileid: "1796760"
---
# <a name="why-a-page-is-locked-from-personalization"></a><span data-ttu-id="97a2e-103">Warum eine Seite für Personalisierungen gesperrt ist</span><span class="sxs-lookup"><span data-stu-id="97a2e-103">Why a Page is Locked from Personalization</span></span>

<span data-ttu-id="97a2e-104">Es gibt zwei Bedingungen, die Sie am Personalisieren einer Seite hindern.</span><span class="sxs-lookup"><span data-stu-id="97a2e-104">There are two conditions that prevent you from personalizing a page.</span></span> <span data-ttu-id="97a2e-105">Entweder ist die Seite gesperrt (wie durch ![Personalisieren sperren](media/personalization-lock-icon.png "Personalisieren sperren") angegeben), oder sie ist blockiert (wie von ![Personalisieren blockiert](media/personalization-blocked-icon.png "Personalisieren blockiert")) angegeben.</span><span class="sxs-lookup"><span data-stu-id="97a2e-105">Either the page is locked (as indicated by ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock")) or it is blocked (as indicated by ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked")).</span></span>

## <a name="locked-from-personalizing"></a><span data-ttu-id="97a2e-106">Für Personalisierung gesperrt</span><span class="sxs-lookup"><span data-stu-id="97a2e-106">Locked from Personalizing</span></span>

<span data-ttu-id="97a2e-107">Wenn ein Symbol ![Personalisieren sperren](media/personalization-lock-icon.png "Personalisieren sperren") im Banner **Personalisieren** angezeigt wird, wenn Sie eine Seite öffnen (wie angezeigt), bedeutet dies, dass Sie zurzeit keine Personalisierungsänderungen an der Seite vornehmen können.</span><span class="sxs-lookup"><span data-stu-id="97a2e-107">If there is a ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon in the **Personalizing** banner when you open a page (as shown), this means that you are currently prevented from making any more personalization changes to the page.</span></span>

<span data-ttu-id="97a2e-108">![Personalisieren sperren](media/personalization-locked.png "Personalisieren sperren")</span><span class="sxs-lookup"><span data-stu-id="97a2e-108">![Personalize Lock](media/personalization-locked.png "Personalize lock")</span></span>


<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

<span data-ttu-id="97a2e-109">Hierfür gibt es zwei Gründe:</span><span class="sxs-lookup"><span data-stu-id="97a2e-109">There can be two reasons for this:</span></span>

1. <span data-ttu-id="97a2e-110">Sie haben die Seite zuvor personalisiert, aber dies erfolgte mithilfe einer früheren Version des Produkts.</span><span class="sxs-lookup"><span data-stu-id="97a2e-110">You have personalized the page before, but it was done using an earlier version of the product.</span></span> <span data-ttu-id="97a2e-111">Wir haben die Art für die Personalisierung geändert seit Sie das letzte Mal die Seite personalisiert haben.</span><span class="sxs-lookup"><span data-stu-id="97a2e-111">We changed the way personalization works behind the scenes since the last time that you personalized the page.</span></span> <span data-ttu-id="97a2e-112">Leider arbeiten die alte Art und die neue Art nicht zusammen.</span><span class="sxs-lookup"><span data-stu-id="97a2e-112">Unfortunately, the old way and new way of doing things do not work together.</span></span>

2. <span data-ttu-id="97a2e-113">Bis jetzt haben Sie nur [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] verwendet, um die Seite zu personalisieren.</span><span class="sxs-lookup"><span data-stu-id="97a2e-113">Until now, you have only used the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] to personalize the page.</span></span>

### <a name="unlocking-the-page"></a><span data-ttu-id="97a2e-114">Entsperren der Seite</span><span class="sxs-lookup"><span data-stu-id="97a2e-114">Unlocking the Page</span></span>

<span data-ttu-id="97a2e-115">Wenn Sie eine Seite entsperren und weiter Personalisieren möchten, wählen Sie ![Personalisieren sperren](media/personalization-lock-icon.png "Personalisieren sperren") und dann **Sperre aufheben** aus.</span><span class="sxs-lookup"><span data-stu-id="97a2e-115">If you want to unlock a page and continue personalizing it, choose ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock"), and then **Unlock**.</span></span>  

<span data-ttu-id="97a2e-116">Bevor Sie die Seite entsperren, beachten Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="97a2e-116">Before you unlock the page, be aware of the following:</span></span>

- <span data-ttu-id="97a2e-117">Die aktuelle Personalisierung der Seite wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="97a2e-117">The current personalization of the page will be cleared.</span></span> <span data-ttu-id="97a2e-118">Die Seite kehrt zum ursprünglichen Layout zurück, und Sie müssen neu beginnen.</span><span class="sxs-lookup"><span data-stu-id="97a2e-118">The page will go back to its original layout, and you will have to start from scratch.</span></span>

- <span data-ttu-id="97a2e-119">In [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] bleibt die Seite wie sie ist und wird von den Änderungen der neuen im Business Central-Central vorgenommenen Personalisierung nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="97a2e-119">In the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], the page will remain as-is and will not be affected by the new personalization changes made in the Business Central client.</span></span> <span data-ttu-id="97a2e-120">Ab da sind die Personalisierungen in [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] und im Business Central-Client völlig voneinander getrennt.</span><span class="sxs-lookup"><span data-stu-id="97a2e-120">Going forward, the personalization in the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] and Business Central client will be completely separate from each other.</span></span>

## <a name="blocked-from-personalizing"></a><span data-ttu-id="97a2e-121">Für Personalisierung blockiert</span><span class="sxs-lookup"><span data-stu-id="97a2e-121">Blocked from Personalizing</span></span>

<span data-ttu-id="97a2e-122">Ein Symbol ![Personalisierung blockiert](media/personalization-blocked-icon.png "Personalisierung blockiert") im Personalisierungsbanner bedeutet, dass jegliche Personalisierung der Seite blockiert ist.</span><span class="sxs-lookup"><span data-stu-id="97a2e-122">If there is a ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon in the Personalizing banner, this means that you are blocked from doing any personalization to the page.</span></span>

<span data-ttu-id="97a2e-123">![Personalisieren blockiert](media/personalization-blocked.png "Personalisieren sperren")</span><span class="sxs-lookup"><span data-stu-id="97a2e-123">![Personalize blocked](media/personalization-blocked.png "Personalize lock")</span></span>

<span data-ttu-id="97a2e-124">Der Grund dafür ist, dass das Rollencenter oder die Rolle, die derzeit mit dem Benutzerkonto verknüpft ist, diese Seite speziell für Ihre Rolle ändert.</span><span class="sxs-lookup"><span data-stu-id="97a2e-124">The reason for this is that the Role Center or role that is currently associated with your user account modifies this page specifically for your role.</span></span> <span data-ttu-id="97a2e-125">Bitten Sie Ihren Administrator um Hilfe oder versuchen Sie, wenn es sinnvoll ist, zu einem Rollencenter (in [**Meine Einstellungen**](https://businesscentral.dynamics.com?page=9176 "Navigieren Sie direkt zu Ihrer Einstellungsseite in Business Central")) zu wechseln, das Rollenanpassung für diese Seite umfasst.</span><span class="sxs-lookup"><span data-stu-id="97a2e-125">Please contact your administrator for assistance or, if it makes sense, try switching to a Role Center (from  [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central")) that does include role-tailoring for this page.</span></span>

## <a name="see-also"></a><span data-ttu-id="97a2e-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97a2e-126">See Also</span></span>
[<span data-ttu-id="97a2e-127">Personalisieren Ihres Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="97a2e-127">Personalizing Your Workspace</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="97a2e-128">Verwalten der Personalisierung</span><span class="sxs-lookup"><span data-stu-id="97a2e-128">Managing Personalization</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="97a2e-129">Ändern von grundlegenden Einstellungen</span><span class="sxs-lookup"><span data-stu-id="97a2e-129">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="97a2e-130">Sie können auswählen, welche Funktionen angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="97a2e-130">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
