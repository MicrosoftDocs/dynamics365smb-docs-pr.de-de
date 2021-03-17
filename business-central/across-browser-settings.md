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
ms.openlocfilehash: b5083735be31b635cb3fc3ce404e7f182d04640f
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384974"
---
# <a name="setting-up-and-troubleshooting-your-browser-to-work-with-business-central-web-client"></a><span data-ttu-id="6d732-103">Einrichten und Beheben von Problemen mit Ihrem Browser für die Arbeit mit Business Central Web Client</span><span class="sxs-lookup"><span data-stu-id="6d732-103">Setting Up and Troubleshooting Your Browser to Work With Business Central Web Client</span></span>

<span data-ttu-id="6d732-104">In diesem Artikel wird erläutert, wie Sie Ihren Browser so einrichten, dass [!INCLUDE[web_client](includes/web_client.md)] und alle seine Funktionen ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="6d732-104">This article explains how to set up your browser so that the [!INCLUDE[web_client](includes/web_client.md)] and all its features work properly.</span></span> <span data-ttu-id="6d732-105">Lesen Sie diesen Artikel, wenn Sie Probleme beim Öffnen von [!INCLUDE[web_client](includes/web_client.md)] haben, da einige Probleme durch die Einstellungen Ihres Browsers verursacht werden können.</span><span class="sxs-lookup"><span data-stu-id="6d732-105">Read this article if you're having problems opening the [!INCLUDE[web_client](includes/web_client.md)], because some problems may be caused by your browser's settings.</span></span>

<span data-ttu-id="6d732-106">Der Artikel enthält Details zum Einrichten von Microsoft Edge, aber die Anforderungen für JavaScript, Cookies und Popups sind jedoch für alle unterstützten Browser gleich.</span><span class="sxs-lookup"><span data-stu-id="6d732-106">The article provides details for setting up Microsoft Edge, but the requirements for JavaScript, cookies, and pop-ups are the same for all supported browsers.</span></span> <span data-ttu-id="6d732-107">Informationen zu anderen Browsern finden Sie in den Anweisungen des Herstellers.</span><span class="sxs-lookup"><span data-stu-id="6d732-107">For other browsers, refer to the instructions provided by the manufacturer.</span></span>  

## <a name="use-a-supported-browser"></a><span data-ttu-id="6d732-108">Einen unterstützten Browser verwenden</span><span class="sxs-lookup"><span data-stu-id="6d732-108">Use a supported browser</span></span>

<span data-ttu-id="6d732-109">Stellen Sie sicher, dass Sie einen der unterstützten Browser verwenden.</span><span class="sxs-lookup"><span data-stu-id="6d732-109">Make sure to use a one of the supported browsers.</span></span> <span data-ttu-id="6d732-110">Siehe [Mindestanforderungen für die Nutzung von Business Central](product-requirements.md#recommended-browsers).</span><span class="sxs-lookup"><span data-stu-id="6d732-110">See [Minimum Requirements for Using Business Central](product-requirements.md#recommended-browsers).</span></span>  

## <a name="allow-javascript-from-business-central"></a><span data-ttu-id="6d732-111">JavaScript von Business Central aus zulassen</span><span class="sxs-lookup"><span data-stu-id="6d732-111">Allow JavaScript from Business Central</span></span>

<span data-ttu-id="6d732-112">*Problem:*</span><span class="sxs-lookup"><span data-stu-id="6d732-112">*Problem:*</span></span>

<span data-ttu-id="6d732-113">Wenn der Browser kein JavaScript zulässt, werden Sie **NotSupported/DisabledJavaScript** in der Adressleiste und **HTTP-Fehler 404.0 – Nicht gefunden** Nachricht sehen, wenn Sie versuchen [!INCLUDE[prod_short](includes/prod_short.md)] zu öffnen, und die</span><span class="sxs-lookup"><span data-stu-id="6d732-113">If the browser doesn't allow JavaScript, you'll see **NotSupported/DisabledJavaScript** in the address bar and an **HTTP Error 404.0 - Not Found** message when you try to open [!INCLUDE[prod_short](includes/prod_short.md)], and the</span></span> 

<!-- http://localhost:8080/NotSupported/DisabledJavaScript HTTP Error 404.0 - Not Found
The resource you are looking for has been removed, had its name changed, or is temporarily unavailable. -->

<span data-ttu-id="6d732-114">*Fix:*</span><span class="sxs-lookup"><span data-stu-id="6d732-114">*Fix:*</span></span>

1. <span data-ttu-id="6d732-115">Im Microsoft Edge gehen Sie zu **Einstellungen** > **Cookies und Site-Berechtigungen** > **JavaScript**.</span><span class="sxs-lookup"><span data-stu-id="6d732-115">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **JavaScript**.</span></span>
2. <span data-ttu-id="6d732-116">Führen Sie einen der folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="6d732-116">Do one of the following steps.</span></span> <span data-ttu-id="6d732-117">Wählen Sie den von Ihrer Organisation empfohlenen Schritt aus:</span><span class="sxs-lookup"><span data-stu-id="6d732-117">Choose the step that is recommended by your organization:</span></span>

    - <span data-ttu-id="6d732-118">Bewegen Sie die Umschaltung **Zulassen** nach links (Aus).</span><span class="sxs-lookup"><span data-stu-id="6d732-118">Move the **Allowed** toggle to the left (Off).</span></span> <span data-ttu-id="6d732-119">Wählen Sie dann **Hinzufügen** und geben Sie die Adresse (URL) ein für [!INCLUDE[prod_short](includes/prod_short.md)] im Kästchen **Seite**.</span><span class="sxs-lookup"><span data-stu-id="6d732-119">Then, select **Add** and type the address (URL) for [!INCLUDE[prod_short](includes/prod_short.md)] in the **Site** box.</span></span> <span data-ttu-id="6d732-120">Wählen Sie **Hinzufügen**, wenn fertig.</span><span class="sxs-lookup"><span data-stu-id="6d732-120">Select **Add** when done.</span></span>
    - <span data-ttu-id="6d732-121">Bewegen Sie die Umschaltung **Zulassen** nach rechts (Ein).</span><span class="sxs-lookup"><span data-stu-id="6d732-121">Move the **Allowed** toggle to the right (On).</span></span>

## <a name="allow-cookies-from-business-central"></a><span data-ttu-id="6d732-122">Cookies für Business Central zulassen</span><span class="sxs-lookup"><span data-stu-id="6d732-122">Allow cookies from Business Central</span></span>

<span data-ttu-id="6d732-123">*Problem:*</span><span class="sxs-lookup"><span data-stu-id="6d732-123">*Problem:*</span></span>

<span data-ttu-id="6d732-124">Wenn der Browser keine Cookies zulässt, wird folgende Fehlermeldung angezeigt:</span><span class="sxs-lookup"><span data-stu-id="6d732-124">If the browser doesn't allow cookies, you'll get the following error:</span></span>

<span data-ttu-id="6d732-125">**Die Seite wurde leider nicht gefunden. Bitte überprüfen Sie die Adresse und versuchen Sie es erneut.**</span><span class="sxs-lookup"><span data-stu-id="6d732-125">**Sorry, the page could not be found. Please check the address and try again.**</span></span> 

<span data-ttu-id="6d732-126">*Fix:*</span><span class="sxs-lookup"><span data-stu-id="6d732-126">*Fix:*</span></span>

1. <span data-ttu-id="6d732-127">In Microsoft Edge gehen Sie zu **Einstellungen** > **Cookies und Site-Berechtigungen** > **Cookies und Site-Daten**.</span><span class="sxs-lookup"><span data-stu-id="6d732-127">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **Cookies and site data**.</span></span>
2. <span data-ttu-id="6d732-128">Bewegen Sie die Umschaltung **Ermöglichen Sie Websites das Speichern und Lesen von Cookie-Daten** nach rechts (Ein).</span><span class="sxs-lookup"><span data-stu-id="6d732-128">Move the **Allow sites to save and read cookie data** toggle to the right (On).</span></span>  

## <a name="allow-pop-ups-from-business-central"></a><a name="popup"></a><span data-ttu-id="6d732-129">Pup-Ups von Business Central zulassen</span><span class="sxs-lookup"><span data-stu-id="6d732-129">Allow pop-ups from Business Central</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="6d732-130">lässt sich in mehrere Produkte integrieren.</span><span class="sxs-lookup"><span data-stu-id="6d732-130">integrates with several products.</span></span> <span data-ttu-id="6d732-131">In einigen Fällen wird, wie bei Microsoft Teams, [!INCLUDE[prod_short](includes/prod_short.md)] oder Popups innerhalb des Produkts geöffnet.</span><span class="sxs-lookup"><span data-stu-id="6d732-131">In some cases, like with Microsoft Teams, [!INCLUDE[prod_short](includes/prod_short.md)] opens, or "pop-ups", within the product.</span></span> <span data-ttu-id="6d732-132">Diese Funktion erfordert, dass Ihr Browser Popups zulässt von [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="6d732-132">This capability requires that your browser allows pop-ups from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

<span data-ttu-id="6d732-133">*Problem:*</span><span class="sxs-lookup"><span data-stu-id="6d732-133">*Problem:*</span></span>

<span data-ttu-id="6d732-134">Wenn Popups für [!INCLUDE[prod_short](includes/prod_short.md)] blockiert werden, erhalten Sie eine Nachricht ähnlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="6d732-134">If pop-ups for [!INCLUDE[prod_short](includes/prod_short.md)] are being blocked, you get a message similar to the following message:</span></span>

<span data-ttu-id="6d732-135">**Etwas ist schief gelaufen. Ihr Browser blockiert möglicherweise Popups, die von Business Central benötigt werden.**</span><span class="sxs-lookup"><span data-stu-id="6d732-135">**Something went wrong. Your browser may be blocking pop-ups needed by Business Central.**</span></span>

<!--
Something went wrong
Your browser may be blocking pop-ups needed by Business Central.

Change your browser settings to allow pop-ups or allow this for trusted domains, then try again.
If these settings are managed for your organization, you should contact your administrator for assistance.

Try again
-->
<span data-ttu-id="6d732-136">*Fix:*</span><span class="sxs-lookup"><span data-stu-id="6d732-136">*Fix:*</span></span>

1. <span data-ttu-id="6d732-137">In Microsoft Edge gehen Sie zu **Einstellungen** > **Cookies und Site-Berechtigungen** > **Popups und Umleitung**.</span><span class="sxs-lookup"><span data-stu-id="6d732-137">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **Pop-ups and redirects**.</span></span>
2. <span data-ttu-id="6d732-138">Bewegen Sie die Umschaltung **Blockiert** nach rechts (Ein).</span><span class="sxs-lookup"><span data-stu-id="6d732-138">Move the **Blocked** toggle to the right (On).</span></span>
3. <span data-ttu-id="6d732-139">Wählen Sie **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="6d732-139">Select **Add**.</span></span> <span data-ttu-id="6d732-140">In dem Kästchen **Seite** geben Sie `https://businesscentral.dynamics.com` ein und wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="6d732-140">In the **Site** box, type `https://businesscentral.dynamics.com`, then select **Add**.</span></span>

## <a name="see-also"></a><span data-ttu-id="6d732-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d732-141">See Also</span></span>

[<span data-ttu-id="6d732-142">Teams Problembehebung</span><span class="sxs-lookup"><span data-stu-id="6d732-142">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]