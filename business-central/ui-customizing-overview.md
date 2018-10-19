---
title: Anpassen von Business Central | Microsoft Docs
description: "Mehr über das Hinzufügen von Funktionalitäten und Anpassungen in Business Central erfahren."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personalize, add-in, extend, customize
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 63ba198a761b0c79c51ac94d36314310e330fc58
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="customizing-business-central"></a><span data-ttu-id="39434-103">Business Central anpassen</span><span class="sxs-lookup"><span data-stu-id="39434-103">Customizing Business Central</span></span>
<span data-ttu-id="39434-104">Es gibt unterschiedliche Arten, die Anwendung anzupassen, um Ihnen und Ihren Kollegen Zugriff auf die Funktionen, die Funktionalität und die Daten zu geben, die Sie am häufigsten brauchen, uns so, dass es am besten in Ihre tägliche Arbeit passt.</span><span class="sxs-lookup"><span data-stu-id="39434-104">There are different ways to customize the application to give you and your colleagues access to the features, functionality, and data that you need most, in a manner that bests suits your daily work.</span></span> <span data-ttu-id="39434-105">Diejenigen, die Änderungen sehen, verlassen sich auf das, was Sie tun in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="39434-105">Those who see the changes will depend on what you do, as described in this table.</span></span>

| <span data-ttu-id="39434-106">Was können Sie tun</span><span class="sxs-lookup"><span data-stu-id="39434-106">What you can do</span></span>    |  <span data-ttu-id="39434-107">Description</span><span class="sxs-lookup"><span data-stu-id="39434-107">Description</span></span>  |  <span data-ttu-id="39434-108">Wer sieht die Änderungen</span><span class="sxs-lookup"><span data-stu-id="39434-108">Who sees the changes</span></span>  |  <span data-ttu-id="39434-109">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="39434-109">More information</span></span>  |
|-----|---------------|---------|-------|
|<span data-ttu-id="39434-110">Erweiterung installieren</span><span class="sxs-lookup"><span data-stu-id="39434-110">Install an extension</span></span>|<span data-ttu-id="39434-111">Erweiterung sind wie kleine Anwendungen, die Funktionalität hinzufügen, Verhalten ändern, Zugriff auf neuen Onlinediensten bereitstellen und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="39434-111">Extensions are like small applications that add functionality, change behavior, provide access to new online services, and more.</span></span> <span data-ttu-id="39434-112">Beispielsweise bietet Microsoft eine Erweiterung an, die die Integration mit PayPal Payments Standard ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="39434-112">For example, Microsoft provides an extension that provides integration with PayPal Payments Standard.</span></span>|<span data-ttu-id="39434-113">Alle Benutzer in allen Mandanten.</span><span class="sxs-lookup"><span data-stu-id="39434-113">All users in all companies.</span></span>|[<span data-ttu-id="39434-114">Erweiterungen nutzen anpassen</span><span class="sxs-lookup"><span data-stu-id="39434-114">Customizing Using Extensions</span></span>](ui-extensions.md)|
|<span data-ttu-id="39434-115">Ändern, welche Benutzeroberflächenelementen sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="39434-115">Change which UI elements are visible.</span></span>|<span data-ttu-id="39434-116">Die Einstellung **Erfahrung** bestimmt, wie viel der Funktionen der Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="39434-116">The **Experience** setting determines how much of the functionality is displayed in the user interface.</span></span> <span data-ttu-id="39434-117">Wählen Sie zwischen Essential und Premium aus.</span><span class="sxs-lookup"><span data-stu-id="39434-117">Choose between Essential and Premium.</span></span>|<span data-ttu-id="39434-118">Alle Benutzer in einem bestimmten Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="39434-118">All users in a specific company.</span></span>|[<span data-ttu-id="39434-119">Sie können auswählen, welche Funktionen angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="39434-119">Changing Which Features are Displayed</span></span>](ui-experiences.md)|
|<span data-ttu-id="39434-120">Personalisieren Ihres Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="39434-120">Personalize your workspace</span></span>|<span data-ttu-id="39434-121">Anpassen des Layouts und den Inhalt der Seiten.</span><span class="sxs-lookup"><span data-stu-id="39434-121">Change the layout and content of your pages.</span></span>|<span data-ttu-id="39434-122">Nur Sie.</span><span class="sxs-lookup"><span data-stu-id="39434-122">Only you.</span></span>|[<span data-ttu-id="39434-123">Personalisieren Ihres Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="39434-123">Personalizing Your Workspace</span></span>](ui-personalization-user.md)|

> [!NOTE]
> <span data-ttu-id="39434-124">Alle Funktionsbeschreibungen in der Dokumentation behandeln [!INCLUDE[d365fin](includes/d365fin_md.md)] die **Premium**-Umgebung, decken also den gesamten Umfang der Benutzeroberflächenelemente ab.</span><span class="sxs-lookup"><span data-stu-id="39434-124">All feature descriptions in user documentation for [!INCLUDE[d365fin](includes/d365fin_md.md)] assumes the **Premium** experience, meaning the descriptions cover the full scope of UI elements.</span></span> <span data-ttu-id="39434-125">Daher können Benutzer mit der **Essential**-Umgebung in einigen Themen Informationen zu Funktionen und Benutzeroberflächenelementen finden, die in der Benutzeroberfläche nicht sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="39434-125">Therefore, users with the **Essential** experience may in some topics read about functionality and UI elements that are not visible in their user interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="39434-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39434-126">See Also</span></span>
<span data-ttu-id="39434-127">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="39434-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

