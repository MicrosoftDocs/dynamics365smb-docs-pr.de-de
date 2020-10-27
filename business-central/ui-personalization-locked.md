---
title: Warum ich eine Seite nicht personalisieren | Microsoft Docs
description: Erklärt, warum Sie eine Seite nicht personalisieren können und was Sie tun können, um sie zu entsperren, sodass Sie sie anpassen können.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0bd24833f37fe70f8e642685be4d28dbb593a16d
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923395"
---
# <a name="why-a-page-is-locked-from-personalization"></a><span data-ttu-id="98f3e-103">Warum eine Seite für Personalisierungen gesperrt ist</span><span class="sxs-lookup"><span data-stu-id="98f3e-103">Why a Page is Locked from Personalization</span></span>

<span data-ttu-id="98f3e-104">Es gibt zwei Bedingungen, die Sie am Personalisieren einer Seite hindern.</span><span class="sxs-lookup"><span data-stu-id="98f3e-104">There are two conditions that prevent you from personalizing a page.</span></span> <span data-ttu-id="98f3e-105">Entweder ist die Seite gesperrt (wie durch das Symbol ![Personalisierungssperre](media/personalization-lock-icon.png "Personalisieren sperren") angezeigt) oder sie ist blockiert (wie durch das Symbol ![Personalisierung blockiert](media/personalization-blocked-icon.png "Personalisierung blockiert") angezeigt).</span><span class="sxs-lookup"><span data-stu-id="98f3e-105">Either the page is locked (as indicated by the ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock")) icon or it is blocked (as indicated by the ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon).</span></span>

## <a name="locked-from-personalizing"></a><span data-ttu-id="98f3e-106">Für Personalisierung gesperrt</span><span class="sxs-lookup"><span data-stu-id="98f3e-106">Locked from Personalizing</span></span>

<span data-ttu-id="98f3e-107">Wenn beim Öffnen einer Seite das Symbol ![Personalisierungssperre](media/personalization-lock-icon.png "Personalisieren sperren") im Banner **Personalisierung** zu sehen ist, bedeutet dies, dass Sie derzeit keine weiteren Personalisierungsänderungen an der Seite vornehmen können.</span><span class="sxs-lookup"><span data-stu-id="98f3e-107">If there is a ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon in the **Personalizing** banner when you open a page, this means that you are currently prevented from making any more personalization changes to the page.</span></span>

<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

<span data-ttu-id="98f3e-108">Hierfür gibt es zwei Gründe:</span><span class="sxs-lookup"><span data-stu-id="98f3e-108">There can be two reasons for this:</span></span>

1. <span data-ttu-id="98f3e-109">Sie haben die Seite zuvor personalisiert, aber dies erfolgte mithilfe einer früheren Version des Produkts.</span><span class="sxs-lookup"><span data-stu-id="98f3e-109">You have personalized the page before, but it was done using an earlier version of the product.</span></span> <span data-ttu-id="98f3e-110">Wir haben die Art für die Personalisierung geändert seit Sie das letzte Mal die Seite personalisiert haben.</span><span class="sxs-lookup"><span data-stu-id="98f3e-110">We changed the way personalization works behind the scenes since the last time that you personalized the page.</span></span> <span data-ttu-id="98f3e-111">Leider arbeiten die alte Art und die neue Art nicht zusammen.</span><span class="sxs-lookup"><span data-stu-id="98f3e-111">Unfortunately, the old way and new way of doing things do not work together.</span></span>

2. <span data-ttu-id="98f3e-112">Bis jetzt haben Sie nur [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] verwendet, um die Seite zu personalisieren.</span><span class="sxs-lookup"><span data-stu-id="98f3e-112">Until now, you have only used the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] to personalize the page.</span></span>

### <a name="unlocking-the-page"></a><span data-ttu-id="98f3e-113">Entsperren der Seite</span><span class="sxs-lookup"><span data-stu-id="98f3e-113">Unlocking the Page</span></span>

<span data-ttu-id="98f3e-114">Wenn Sie eine Seite entsperren und weiter personalisieren möchten, wählen Sie das Symbol ![Personalisieren Sperre](media/personalization-lock-icon.png "Personalisieren sperren") und dann die Aktion **Entsperren** .</span><span class="sxs-lookup"><span data-stu-id="98f3e-114">If you want to unlock a page and continue personalizing it, choose the ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon, and then choose the **Unlock** action.</span></span>  

<span data-ttu-id="98f3e-115">Bevor Sie die Seite entsperren, beachten Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="98f3e-115">Before you unlock the page, be aware of the following:</span></span>

- <span data-ttu-id="98f3e-116">Die aktuelle Personalisierung der Seite wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="98f3e-116">The current personalization of the page will be cleared.</span></span> <span data-ttu-id="98f3e-117">Die Seite kehrt zum ursprünglichen Layout zurück, und Sie müssen neu beginnen.</span><span class="sxs-lookup"><span data-stu-id="98f3e-117">The page will go back to its original layout, and you will have to start from scratch.</span></span>

- <span data-ttu-id="98f3e-118">In [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] bleibt die Seite wie sie ist und wird von den Änderungen der neuen im Business Central-Central vorgenommenen Personalisierung nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="98f3e-118">In the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], the page will remain as-is and will not be affected by the new personalization changes made in the Business Central client.</span></span> <span data-ttu-id="98f3e-119">Ab da sind die Personalisierungen in [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] und im Business Central-Client völlig voneinander getrennt.</span><span class="sxs-lookup"><span data-stu-id="98f3e-119">Going forward, the personalization in the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] and Business Central client will be completely separate from each other.</span></span>

## <a name="blocked-from-personalizing"></a><span data-ttu-id="98f3e-120">Für Personalisierung blockiert</span><span class="sxs-lookup"><span data-stu-id="98f3e-120">Blocked from Personalizing</span></span>

<span data-ttu-id="98f3e-121">Wenn das Symbol ![Personalisierung blockiert](media/personalization-blocked-icon.png "Personalisierung blockiert") im Banner **Personalisierung** erscheint, bedeutet dies, dass Sie an der Personalisierung der Seite gehindert werden.</span><span class="sxs-lookup"><span data-stu-id="98f3e-121">If there is a ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon in the **Personalizing** banner, this means that you are blocked from doing any personalization to the page.</span></span>

<!-- Only text is translated, so removing this image for non-English UX reasons.  ![Personalize blocked](media/personalization-blocked.png "Personalize lock") -->

<span data-ttu-id="98f3e-122">Der Grund dafür ist, dass das Rollencenter oder die Rolle, die derzeit mit dem Benutzerkonto verknüpft ist, diese Seite speziell für Ihre Rolle ändert.</span><span class="sxs-lookup"><span data-stu-id="98f3e-122">The reason for this is that the Role Center or role that is currently associated with your user account modifies this page specifically for your role.</span></span> <span data-ttu-id="98f3e-123">Wenden Sie sich an Ihren Administrator, um Unterstützung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="98f3e-123">Contact your administrator for assistance.</span></span> <span data-ttu-id="98f3e-124">Versuchen Sie alternativ, zu einem Rollencenter zu wechseln, das die Rollenanpassung für diese Seite enthält.</span><span class="sxs-lookup"><span data-stu-id="98f3e-124">Alternatively, try switching to a Role Center that does include role-tailoring for this page.</span></span> <span data-ttu-id="98f3e-125">Weitere Informationen finden Sie unter [Ändern der Grundeinstellungen](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="98f3e-125">For more information, see [Change Basic Settings](ui-change-basic-settings.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="98f3e-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98f3e-126">See Also</span></span>
[<span data-ttu-id="98f3e-127">Ihren Arbeitsbereich personalisieren</span><span class="sxs-lookup"><span data-stu-id="98f3e-127">Personalize Your Workspace</span></span>](ui-personalization-user.md)  
[<span data-ttu-id="98f3e-128">Seiten für Profile anpassen</span><span class="sxs-lookup"><span data-stu-id="98f3e-128">Customize Pages for Profiles</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="98f3e-129">Ändern von grundlegenden Einstellungen</span><span class="sxs-lookup"><span data-stu-id="98f3e-129">Change Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="98f3e-130">Ändern, welche Funktionen angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="98f3e-130">Change Which Features are Displayed</span></span>](ui-experiences.md)  
