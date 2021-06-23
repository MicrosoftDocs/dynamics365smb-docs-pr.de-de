---
title: Outlook für Ihr Unternehmenspostfach optimieren
description: Erfahren Sie, wie Sie die Erfahrung mit dem Unternehmenspostfach in Microsoft Outlook verbessern können.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Outlook, Microsoft 365, inbox, business inbox, WebView2, Edge, addin, add-in
ms.date: 05/12/2021
ms.author: jswymer
ms.openlocfilehash: 2fee1782057d0f45319e4d12d715c2e1e0d3d4a6
ms.sourcegitcommit: 61e279b253370cdf87b7bc1ee0f927e4f0521344
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2021
ms.locfileid: "6064856"
---
# <a name="optimizing-outlook-for-your-business-inbox"></a><span data-ttu-id="0dcfe-103">Outlook für Ihr Unternehmenspostfach optimieren</span><span class="sxs-lookup"><span data-stu-id="0dcfe-103">Optimizing Outlook for Your Business Inbox</span></span> 

<span data-ttu-id="0dcfe-104">In diesem Artikel wird beschrieben, wie Sie die bestmögliche Erfahrung mit dem Unternehmenpostfach in Microsoft Outlook erzielen können.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-104">This article discusses things you can do to get the best possible experience with the Business Inbox in Microsoft Outlook.</span></span> 

## <a name="update-outlook"></a><span data-ttu-id="0dcfe-105">Outlook aktualisieren</span><span class="sxs-lookup"><span data-stu-id="0dcfe-105">Update Outlook</span></span>

<span data-ttu-id="0dcfe-106">Aktualisieren Sie auf Outlook-Version 2012 oder höher.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-106">Update to Outlook version 2012 or newer.</span></span>

> [!NOTE]
> <span data-ttu-id="0dcfe-107">Wenn Sie Outlook nicht auf Version 2012 oder höher aktualisieren können, stellen Sie sicher, dass Sie mindestens auf Version 1905 aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-107">If you are unable to update Outlook to version 2012 or later, make sure that you at least update to version 1905.</span></span> <span data-ttu-id="0dcfe-108">Dadurch wird verhindert, dass das Outlook-Add-In veraltete Internet Explorer-Komponenten verwendet.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-108">This prevents the Outlook Add-in from running using legacy Internet Explorer components</span></span>

### <a name="how-to-check-your-version-of-outlook"></a><span data-ttu-id="0dcfe-109">So überprüfen Sie Ihre Outlook-Version</span><span class="sxs-lookup"><span data-stu-id="0dcfe-109">How to check your version of Outlook</span></span>

<span data-ttu-id="0dcfe-110">Befolgen Sie, unabhängig davon, ob Sie Office 2019 oder Microsoft 365 verwenden, diese Microsoft-Support-Anleitung, um zu überprüfen, welche Version von Outlook Sie verwenden:</span><span class="sxs-lookup"><span data-stu-id="0dcfe-110">Whether you use Office 2019 or Microsoft 365, follow this Microsoft Support guide to check which version of Outlook you have:</span></span>  

[<span data-ttu-id="0dcfe-111">Über Office: Welche Office-Version verwende ich?</span><span class="sxs-lookup"><span data-stu-id="0dcfe-111">About Office: What version of Office am I using?</span></span>](https://support.microsoft.com/office/about-office-what-version-of-office-am-i-using-932788b8-a3ce-44bf-bb09-e334518b8b19)

### <a name="how-to-update-outlook"></a><span data-ttu-id="0dcfe-112">So aktualisieren Sie Outlook</span><span class="sxs-lookup"><span data-stu-id="0dcfe-112">How to update Outlook</span></span>

<span data-ttu-id="0dcfe-113">Um Outlook auf die neueste Version zu aktualisieren, befolgen Sie diese Microsoft-Support-Anleitung, oder wenden Sie sich an Ihren Administrator:</span><span class="sxs-lookup"><span data-stu-id="0dcfe-113">To update Outlook to the latest version, follow this Microsoft Support guide or contact your administrator:</span></span>

[<span data-ttu-id="0dcfe-114">Office-Updates installieren</span><span class="sxs-lookup"><span data-stu-id="0dcfe-114">Install Office updates</span></span>](https://support.microsoft.com/office/install-office-updates-2ab296f3-7f03-43a2-8e50-46de917611c5)

## <a name="install-microsoft-edge-webview2"></a><span data-ttu-id="0dcfe-115">Microsoft Edge WebView2 installieren</span><span class="sxs-lookup"><span data-stu-id="0dcfe-115">Install Microsoft Edge WebView2</span></span>

<span data-ttu-id="0dcfe-116">Stellen Sie sicher, dass Microsoft Edge WebView2 auf Ihrem Gerät installiert ist.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-116">Ensure that Microsoft Edge WebView2 is installed on your device.</span></span>

### <a name="how-to-check-if-microsoft-edge-webview2-is-installed"></a><span data-ttu-id="0dcfe-117">So überprüfen Sie, ob Microsoft Edge WebView2 installiert ist</span><span class="sxs-lookup"><span data-stu-id="0dcfe-117">How to check if Microsoft Edge WebView2 is installed</span></span> 

<span data-ttu-id="0dcfe-118">Führen Sie die folgenden Schritte aus, um zu überprüfen, ob Microsoft Edge WebView2 auf einem Computer installiert ist:</span><span class="sxs-lookup"><span data-stu-id="0dcfe-118">To check if you have Microsoft Edge WebView2 installed on a computer, do the following steps:</span></span>

<span data-ttu-id="0dcfe-119">Über das Startmenü:</span><span class="sxs-lookup"><span data-stu-id="0dcfe-119">From Start menu:</span></span>

1. <span data-ttu-id="0dcfe-120">Wählen Sie **Start** ![Windows-Start](media/windows-start-icon.png "Symbol für Windows-Start") > **Einstellungen** ![Windows-Einstellungen](media/windows-settings-icon.png "Symbol für Windows-Einstellungen") > **Apps und Funktionen** aus.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-120">Choose **Start** ![Windows Start](media/windows-start-icon.png "Windows Start icon") > **Settings** ![Windows Settings](media/windows-settings-icon.png "Windows Settings icon") > **Apps & Features**.</span></span>
2. <span data-ttu-id="0dcfe-121">Geben Sie **WebView2** in das Suchfeld ein.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-121">In the search box, type **WebView2**.</span></span> <span data-ttu-id="0dcfe-122">Wenn Microsoft Edge WebView2 installiert ist, wird der Eintrag **Microsoft Edge WebView2 Runtime** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-122">If Microsoft Edge WebView2 is installed, you'll see an entry called **Microsoft Edge WebView2 Runtime**.</span></span>

<span data-ttu-id="0dcfe-123">Über die Systemsteuerung:</span><span class="sxs-lookup"><span data-stu-id="0dcfe-123">From Control Panel:</span></span>

1. <span data-ttu-id="0dcfe-124">Geben Sie im Suchfeld neben **Start** ![Windows-Start](media/windows-start-icon.png "Symbol für Windows-Start") **Systemsteuerung** ein, und wählen Sie dann das Ergebnis aus.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-124">In the search box next to **Start** ![Windows Start](media/windows-start-icon.png "Windows Start icon"), type **Control Panel**, and then select the result.</span></span>
2. <span data-ttu-id="0dcfe-125">Wählen Sie **Programme** > **Programme und Features** aus.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-125">Choose **Programs** > **Programs and Features**.</span></span>
3. <span data-ttu-id="0dcfe-126">Geben Sie **WebView2** in das Suchfeld ein.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-126">In the search box, type **WebView2**.</span></span> <span data-ttu-id="0dcfe-127">Wenn Microsoft Edge WebView2 installiert ist, wird der Eintrag **Microsoft Edge WebView2 Runtime** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-127">If Microsoft Edge WebView2 is installed, you'll see an entry called **Microsoft Edge WebView2 Runtime**.</span></span>

### <a name="how-to-install-microsoft-edge-webview2"></a><span data-ttu-id="0dcfe-128">So installieren Sie Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="0dcfe-128">How to install Microsoft Edge WebView2</span></span> 

1. <span data-ttu-id="0dcfe-129">Wechseln Sie über Ihren Browser zu [https://developer.microsoft.com/microsoft-edge/webview2/](https://developer.microsoft.com/microsoft-edge/webview2/).</span><span class="sxs-lookup"><span data-stu-id="0dcfe-129">Using your browser, go to [https://developer.microsoft.com/microsoft-edge/webview2/](https://developer.microsoft.com/microsoft-edge/webview2/).</span></span>
2. <span data-ttu-id="0dcfe-130">Wählen Sie **Herunterladen** aus.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-130">Choose **Download**.</span></span>
3. <span data-ttu-id="0dcfe-131">Legen Sie **Architektur auswählen** Ihrem System entsprechend fest.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-131">Set **Select Architecture** to match your system.</span></span>
4. <span data-ttu-id="0dcfe-132">Wählen Sie **Herunterladen** aus.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-132">Choose **Download**.</span></span>

> [!NOTE]
> <span data-ttu-id="0dcfe-133">Ihre Organisation unterliegt möglicherweise Beschränkungen in Bezug darauf, welche Komponenten auf Ihrem Gerät installiert werden können.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-133">Your organization may have restriction on which components can be installed on your device.</span></span> <span data-ttu-id="0dcfe-134">Wenden Sie sich an Ihren Administrator, um Unterstützung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-134">Contact your administrator for assistance.</span></span>

## <a name="use-a-supported-browser"></a><span data-ttu-id="0dcfe-135">Einen unterstützten Browser verwenden</span><span class="sxs-lookup"><span data-stu-id="0dcfe-135">Use a supported browser</span></span>

<span data-ttu-id="0dcfe-136">Sie können Outlook für das Web in einem der von Business Central unterstützten Browser verwenden.</span><span class="sxs-lookup"><span data-stu-id="0dcfe-136">Consider using Outlook for the Web in one of the browsers supported by Business Central.</span></span> <span data-ttu-id="0dcfe-137">Eine Liste der unterstützten Browser finden Sie unter [Mindestanforderungen für die Verwendung von Business Central](product-requirements.md#browsers).</span><span class="sxs-lookup"><span data-stu-id="0dcfe-137">For a list of supported browsers, see [Minimum Requirements for Using Business Central](product-requirements.md#browsers).</span></span>

## <a name="see-also"></a><span data-ttu-id="0dcfe-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0dcfe-138">See Also</span></span>

[<span data-ttu-id="0dcfe-139">Vorbereitung für die Geschäftstätigkeit</span><span class="sxs-lookup"><span data-stu-id="0dcfe-139">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
[<span data-ttu-id="0dcfe-140">Abrufen von Business Central auf meinem mobilen Gerät</span><span class="sxs-lookup"><span data-stu-id="0dcfe-140">Getting Business Central on my Mobile Device</span></span>](install-mobile-app.md)  
[<span data-ttu-id="0dcfe-141">Dokumente per E-Mail versenden</span><span class="sxs-lookup"><span data-stu-id="0dcfe-141">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
[<span data-ttu-id="0dcfe-142">Finanzen</span><span class="sxs-lookup"><span data-stu-id="0dcfe-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="0dcfe-143">Verkauf</span><span class="sxs-lookup"><span data-stu-id="0dcfe-143">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="0dcfe-144">Einkauf</span><span class="sxs-lookup"><span data-stu-id="0dcfe-144">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="0dcfe-145">Mindestanforderungen für die Verwendung von Outlook</span><span class="sxs-lookup"><span data-stu-id="0dcfe-145">Minimum Requirements for Outlook</span></span>](product-requirements.md#outlook)  
[<span data-ttu-id="0dcfe-146">Add-Ins in Outlook im Internet nutzen</span><span class="sxs-lookup"><span data-stu-id="0dcfe-146">Using add-ins in Outlook on the web</span></span>](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]