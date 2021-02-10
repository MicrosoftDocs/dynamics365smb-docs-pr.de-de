---
title: Einrichten Ihres Browsers
description: Beschreibt das Einrichten von Browsern für die Arbeit mit Business Central und den darin integrierten Produkten.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, web client, troubleshooting, errors
ms.date: 01/08/2021
ms.author: jswymer
ms.openlocfilehash: 17b41653b1b5934e98c82ce8a35430e7b6a5c0d0
ms.sourcegitcommit: 1aac2c5f6773151c011dc1e4069c84d79fe5bda8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "4839946"
---
# <a name="setting-up-and-troubleshooting-your-browser-to-work-with-business-central-web-client"></a><span data-ttu-id="17624-103">Einrichten und Beheben von Problemen mit Ihrem Browser für die Arbeit mit Business Central Web Client</span><span class="sxs-lookup"><span data-stu-id="17624-103">Setting Up and Troubleshooting Your Browser to Work With Business Central Web Client</span></span>

<span data-ttu-id="17624-104">In diesem Artikel wird erläutert, wie Sie Ihren Browser so einrichten, dass [!INCLUDE[web_client](includes/web_client.md)] und alle seine Funktionen ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="17624-104">This article explains how to set up your browser so that the [!INCLUDE[web_client](includes/web_client.md)] and all its features work properly.</span></span> <span data-ttu-id="17624-105">Lesen Sie diesen Artikel, wenn Sie Probleme beim Öffnen von [!INCLUDE[web_client](includes/web_client.md)] haben, da einige Probleme durch die Einstellungen Ihres Browsers verursacht werden können.</span><span class="sxs-lookup"><span data-stu-id="17624-105">Read this article if you're having problems opening the [!INCLUDE[web_client](includes/web_client.md)], because some problems may be caused by your browser's settings.</span></span>

<span data-ttu-id="17624-106">Der Artikel enthält Details zum Einrichten von Microsoft Edge, aber die Anforderungen für JavaScript, Cookies und Popups sind jedoch für alle unterstützten Browser gleich.</span><span class="sxs-lookup"><span data-stu-id="17624-106">The article provides details for setting up Microsoft Edge, but the requirements for JavaScript, cookies, and pop-ups are the same for all supported browsers.</span></span> <span data-ttu-id="17624-107">Informationen zu anderen Browsern finden Sie in den Anweisungen des Herstellers.</span><span class="sxs-lookup"><span data-stu-id="17624-107">For other browsers, refer to the instructions provided by the manufacturer.</span></span>  

## <a name="use-a-supported-browser"></a><span data-ttu-id="17624-108">Einen unterstützten Browser verwenden</span><span class="sxs-lookup"><span data-stu-id="17624-108">Use a supported browser</span></span>

<span data-ttu-id="17624-109">Stellen Sie sicher, dass Sie einen der unterstützten Browser verwenden.</span><span class="sxs-lookup"><span data-stu-id="17624-109">Make sure to use a one of the supported browsers.</span></span> <span data-ttu-id="17624-110">Siehe [Mindestanforderungen für die Nutzung von Business Central](product-requirements.md#recommended-browsers).</span><span class="sxs-lookup"><span data-stu-id="17624-110">See [Minimum Requirements for Using Business Central](product-requirements.md#recommended-browsers).</span></span>  

## <a name="allow-javascript-from-business-central"></a><span data-ttu-id="17624-111">JavaScript von Business Central aus zulassen</span><span class="sxs-lookup"><span data-stu-id="17624-111">Allow JavaScript from Business Central</span></span>

<span data-ttu-id="17624-112">*Problem:*</span><span class="sxs-lookup"><span data-stu-id="17624-112">*Problem:*</span></span>

<span data-ttu-id="17624-113">Wenn der Browser kein JavaScript zulässt, werden Sie **NotSupported/DisabledJavaScript** in der Adressleiste und **HTTP-Fehler 404.0 – Nicht gefunden** Nachricht sehen, wenn Sie versuchen [!INCLUDE[prod_short](includes/prod_short.md)] zu öffnen, und die</span><span class="sxs-lookup"><span data-stu-id="17624-113">If the browser doesn't allow JavaScript, you'll see **NotSupported/DisabledJavaScript** in the address bar and an **HTTP Error 404.0 - Not Found** message when you try to open [!INCLUDE[prod_short](includes/prod_short.md)], and the</span></span> 

<!-- http://localhost:8080/NotSupported/DisabledJavaScript HTTP Error 404.0 - Not Found
The resource you are looking for has been removed, had its name changed, or is temporarily unavailable. -->

<span data-ttu-id="17624-114">*Fix:*</span><span class="sxs-lookup"><span data-stu-id="17624-114">*Fix:*</span></span>

1. <span data-ttu-id="17624-115">Im Microsoft Edge gehen Sie zu **Einstellungen** > **Cookies und Site-Berechtigungen** > **JavaScript**.</span><span class="sxs-lookup"><span data-stu-id="17624-115">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **JavaScript**.</span></span>
2. <span data-ttu-id="17624-116">Führen Sie einen der folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="17624-116">Do one of the following steps.</span></span> <span data-ttu-id="17624-117">Wählen Sie den von Ihrer Organisation empfohlenen Schritt aus:</span><span class="sxs-lookup"><span data-stu-id="17624-117">Choose the step that is recommended by your organization:</span></span>

    - <span data-ttu-id="17624-118">Bewegen Sie die Umschaltung **Zulassen** nach links (Aus).</span><span class="sxs-lookup"><span data-stu-id="17624-118">Move the **Allowed** toggle to the left (Off).</span></span> <span data-ttu-id="17624-119">Wählen Sie dann **Hinzufügen** und geben Sie die Adresse (URL) ein für [!INCLUDE[prod_short](includes/prod_short.md)] im Kästchen **Seite**.</span><span class="sxs-lookup"><span data-stu-id="17624-119">Then, select **Add** and type the address (URL) for [!INCLUDE[prod_short](includes/prod_short.md)] in the **Site** box.</span></span> <span data-ttu-id="17624-120">Wählen Sie **Hinzufügen**, wenn fertig.</span><span class="sxs-lookup"><span data-stu-id="17624-120">Select **Add** when done.</span></span>
    - <span data-ttu-id="17624-121">Bewegen Sie die Umschaltung **Zulassen** nach rechts (Ein).</span><span class="sxs-lookup"><span data-stu-id="17624-121">Move the **Allowed** toggle to the right (On).</span></span>

## <a name="allow-cookies-from-business-central"></a><span data-ttu-id="17624-122">Cookies für Business Central zulassen</span><span class="sxs-lookup"><span data-stu-id="17624-122">Allow cookies from Business Central</span></span>

<span data-ttu-id="17624-123">*Problem:*</span><span class="sxs-lookup"><span data-stu-id="17624-123">*Problem:*</span></span>

<span data-ttu-id="17624-124">Wenn der Browser keine Cookies zulässt, wird folgende Fehlermeldung angezeigt:</span><span class="sxs-lookup"><span data-stu-id="17624-124">If the browser doesn't allow cookies, you'll get the following error:</span></span>

<span data-ttu-id="17624-125">**Die Seite wurde leider nicht gefunden. Bitte überprüfen Sie die Adresse und versuchen Sie es erneut.**</span><span class="sxs-lookup"><span data-stu-id="17624-125">**Sorry, the page could not be found. Please check the address and try again.**</span></span> 

<span data-ttu-id="17624-126">*Fix:*</span><span class="sxs-lookup"><span data-stu-id="17624-126">*Fix:*</span></span>

1. <span data-ttu-id="17624-127">In Microsoft Edge gehen Sie zu **Einstellungen** > **Cookies und Site-Berechtigungen** > **Cookies und Site-Daten**.</span><span class="sxs-lookup"><span data-stu-id="17624-127">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **Cookies and site data**.</span></span>
2. <span data-ttu-id="17624-128">Bewegen Sie die Umschaltung **Ermöglichen Sie Websites das Speichern und Lesen von Cookie-Daten** nach rechts (Ein).</span><span class="sxs-lookup"><span data-stu-id="17624-128">Move the **Allow sites to save and read cookie data** toggle to the right (On).</span></span>  

## <a name="allow-pop-ups-from-business-central"></a><a name="popup"></a><span data-ttu-id="17624-129">Pup-Ups von Business Central zulassen</span><span class="sxs-lookup"><span data-stu-id="17624-129">Allow pop-ups from Business Central</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="17624-130">lässt sich in mehrere Produkte integrieren.</span><span class="sxs-lookup"><span data-stu-id="17624-130">integrates with several products.</span></span> <span data-ttu-id="17624-131">In einigen Fällen wird, wie bei Microsoft Teams, [!INCLUDE[prod_short](includes/prod_short.md)] oder Popups innerhalb des Produkts geöffnet.</span><span class="sxs-lookup"><span data-stu-id="17624-131">In some cases, like with Microsoft Teams, [!INCLUDE[prod_short](includes/prod_short.md)] opens, or "pop-ups", within the product.</span></span> <span data-ttu-id="17624-132">Diese Funktion erfordert, dass Ihr Browser Popups zulässt von [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="17624-132">This capability requires that your browser allows pop-ups from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

<span data-ttu-id="17624-133">*Problem:*</span><span class="sxs-lookup"><span data-stu-id="17624-133">*Problem:*</span></span>

<span data-ttu-id="17624-134">Wenn Popups für [!INCLUDE[prod_short](includes/prod_short.md)] blockiert werden, erhalten Sie eine Nachricht ähnlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="17624-134">If pop-ups for [!INCLUDE[prod_short](includes/prod_short.md)] are being blocked, you get a message similar to the following message:</span></span>

<span data-ttu-id="17624-135">**Etwas ist schief gelaufen. Ihr Browser blockiert möglicherweise Popups, die von Business Central benötigt werden.**</span><span class="sxs-lookup"><span data-stu-id="17624-135">**Something went wrong. Your browser may be blocking pop-ups needed by Business Central.**</span></span>

<!--
Something went wrong
Your browser may be blocking pop-ups needed by Business Central.

Change your browser settings to allow pop-ups or allow this for trusted domains, then try again.
If these settings are managed for your organization, you should contact your administrator for assistance.

Try again
-->
<span data-ttu-id="17624-136">*Fix:*</span><span class="sxs-lookup"><span data-stu-id="17624-136">*Fix:*</span></span>

1. <span data-ttu-id="17624-137">In Microsoft Edge gehen Sie zu **Einstellungen** > **Cookies und Site-Berechtigungen** > **Popups und Umleitung**.</span><span class="sxs-lookup"><span data-stu-id="17624-137">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **Pop-ups and redirects**.</span></span>
2. <span data-ttu-id="17624-138">Bewegen Sie die Umschaltung **Blockiert** nach rechts (Ein).</span><span class="sxs-lookup"><span data-stu-id="17624-138">Move the **Blocked** toggle to the right (On).</span></span>
3. <span data-ttu-id="17624-139">Wählen Sie **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="17624-139">Select **Add**.</span></span> <span data-ttu-id="17624-140">In dem Kästchen **Seite** geben Sie `https://businesscentral.dynamics.com` ein und wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="17624-140">In the **Site** box, type `https://businesscentral.dynamics.com`, then select **Add**.</span></span>

## <a name="see-also"></a><span data-ttu-id="17624-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17624-141">See Also</span></span>

[<span data-ttu-id="17624-142">Teams Problembehebung</span><span class="sxs-lookup"><span data-stu-id="17624-142">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  