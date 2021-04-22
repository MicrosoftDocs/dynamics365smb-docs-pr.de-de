---
title: 'Problembehebung: Auf Kamera und Standort zugreifen'
description: In diesem Artikel wird beschrieben, wie Fehler beim Zugriff auf Kamera- und Standortinformationen in Business Central behoben werden.
author: blrobl
ms.author: t-blrobl
ms.date: 04/01/2021
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: conceptual
ms.service: dynamics365-business-central
ms.openlocfilehash: d6323ef6ce1a278d0dfd5fc0ecb4c7f8e9632aa1
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783084"
---
# <a name="troubleshooting-accessing-camera-and-location"></a><span data-ttu-id="e7000-103">Problembehebung: Auf Kamera und Standort zugreifen</span><span class="sxs-lookup"><span data-stu-id="e7000-103">Troubleshooting: Accessing Camera and Location</span></span>

<span data-ttu-id="e7000-104">Wenn Sie versuchen, die Kamera- und Standortinformationen eines Geräts über [!INCLUDE[prod_short](includes/prod_short.md)] aufzurufen, können Probleme auftreten.</span><span class="sxs-lookup"><span data-stu-id="e7000-104">You might come across some issues when trying to access the camera and location information of a device from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="e7000-105">Nachfolgend sind die möglichen Ursachen für diese Probleme und deren Umgehung aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7000-105">You can find the possible causes behind these problems and how to work around them listed below.</span></span>

## <a name="device-must-have-camera-and-location-capabilities"></a><span data-ttu-id="e7000-106">Das Gerät muss über Kamera- und Standortfunktionen verfügen</span><span class="sxs-lookup"><span data-stu-id="e7000-106">Device must have Camera and Location Capabilities</span></span>

<span data-ttu-id="e7000-107">Das Gerät muss über eine physische Kamera bzw. die Fähigkeit verfügen, Standortinformationen abzurufen, um von einem Gerät aus auf die Kamera oder den Standort eines Benutzers zugreifen zu können.</span><span class="sxs-lookup"><span data-stu-id="e7000-107">In order to access the camera or a user's location from a device, the device must have a physical camera or the capability to retrieve location information, respectively.</span></span>

<span data-ttu-id="e7000-108">Wenn Ihr Gerät über Kamera- und Standortfunktionen verfügt, jedoch weiterhin Probleme auftreten, müssen möglicherweise einige Treiber aktualisiert oder neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="e7000-108">If your device has camera and location capabilities but you still encounter problems, it is possible that some drivers need updating or reinstalling.</span></span> <span data-ttu-id="e7000-109">Auch wenn Sie nicht sicher sind, empfehlen wir immer, das Betriebssystem, die Treiber und den Browser Ihres Geräts auf die neueste Version zu aktualisieren, um eine optimale Nutzung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="e7000-109">Even if you are unsure, we always recommend you update your device operating system, drivers, and browser to the latest version for the best experience.</span></span>

## <a name="access-permissions-not-enabled"></a><span data-ttu-id="e7000-110">Zugriffsberechtigungen sind nicht aktiviert</span><span class="sxs-lookup"><span data-stu-id="e7000-110">Access Permissions not Enabled</span></span>

<span data-ttu-id="e7000-111">Sie müssen den allgemeinen Zugriff auf die Kamera und den Standort über die Datenschutzeinstellungen Ihres Geräts aktivieren und [!INCLUDE[prod_short](includes/prod_short.md)] ausdrücklich die Erlaubnis erteilen, darauf zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="e7000-111">You must enable general access to camera and location from your device's privacy settings and explicitly give permission to  [!INCLUDE[prod_short](includes/prod_short.md)] to access them.</span></span> <span data-ttu-id="e7000-112">Wechseln Sie zu **Einstellungen**, und wählen Sie **Datenschutz** und dann **App-Berechtigungen** aus, wenn Sie beispielsweise die Berechtigungen für ein unter Windows ausgeführtes Gerät anzeigen oder ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="e7000-112">For example, to see or change permissions for a device running on Windows, go to **Settings**, choose **Privacy**, and then **App permissions**.</span></span> 

<span data-ttu-id="e7000-113">Bei mobilen Geräten müssen Sie der mobilen [!INCLUDE[prod_short](includes/prod_short.md)]-App Zugriffsberechtigungen für die Kamera und den Standort gewähren.</span><span class="sxs-lookup"><span data-stu-id="e7000-113">For mobile devices, you must give camera and location access permissions to the [!INCLUDE[prod_short](includes/prod_short.md)] Mobile App.</span></span> <span data-ttu-id="e7000-114">Wechseln Sie dazu bei einem iOS-Gerät zu **Einstellungen**, und wählen Sie **Datenschutz** und dann **Kamera** oder **Standort** aus.</span><span class="sxs-lookup"><span data-stu-id="e7000-114">To do so for an iOS device, go to **Settings**, choose **Privacy**, and then **Camera** or **Location**.</span></span> <span data-ttu-id="e7000-115">Gehen Sie bei Android-Geräten zu **Einstellungen**, und wählen Sie **Apps & Benachrichtigungen**, **Erweitert**, **Berechtigungsmanager** und dann **Kamera** oder **Standort** aus.</span><span class="sxs-lookup"><span data-stu-id="e7000-115">For Android devices go to **Settings**, choose **Apps & Notifications**, **Advanced**, **Permission Manager**, and then **Camera** or **Location**.</span></span>

<span data-ttu-id="e7000-116">Wenn Sie [!INCLUDE[prod_short](includes/prod_short.md)] in einem Browser verwenden, müssen Sie [!INCLUDE[prod_short](includes/prod_short.md)] außerdem die Websiteberechtigung zum Zugriff auf die Kamera oder Standortinformationen gewähren.</span><span class="sxs-lookup"><span data-stu-id="e7000-116">In addition, if you are using [!INCLUDE[prod_short](includes/prod_short.md)] in a browser, you must also grant the [!INCLUDE[prod_short](includes/prod_short.md)] site permission to access the camera or location information.</span></span> <span data-ttu-id="e7000-117">Zum Anzeigen oder Ändern der Berechtigungen einer Website im Microsoft Edge-Browser wechseln Sie zu **Einstellungen**, wählen Sie **Websiteberechtigungen** und dann **Kamera** oder **Standort** aus.</span><span class="sxs-lookup"><span data-stu-id="e7000-117">To see or change a site's permissions in the Microsoft Edge browser, go to **Settings**, choose **Site Permissions**, and then **Camera** or **Location**.</span></span> <span data-ttu-id="e7000-118">Beachten Sie, dass dies bei anderen Browsern möglicherweise anders ist.</span><span class="sxs-lookup"><span data-stu-id="e7000-118">Note that this might be different for other browsers.</span></span>

<span data-ttu-id="e7000-119">Das Gerät oder der Browser zeigt standardmäßig eine Anforderung für den Zugriff auf diese Funktionen an, wenn der Benutzer sie zum ersten Mal aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e7000-119">By default, the device or browser will pop up a request to access these capabilities when the user activates them for the first time.</span></span>

> [!NOTE]  
> <span data-ttu-id="e7000-120">Einige alte Browser gewähren keinen Zugriff auf die Kamera und den Standort.</span><span class="sxs-lookup"><span data-stu-id="e7000-120">Some old browsers do not grant access to camera and location.</span></span> <span data-ttu-id="e7000-121">In Internet Explorer oder in der Vorversion des Edge-Browsers ist beispielsweise keine Kamerafunktion verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e7000-121">For example, camera is not available in Internet Explorer or the legacy Edge browser.</span></span>

## <a name="web-client-connection-not-secure"></a><span data-ttu-id="e7000-122">Webclient-Verbindung ist nicht sicher</span><span class="sxs-lookup"><span data-stu-id="e7000-122">Web Client Connection not Secure</span></span>

<span data-ttu-id="e7000-123">Die Kamera- und Standortfunktionen sind nur verfügbar, wenn der Zugriff auf den Webclient über SSL-gesicherte HTTP-Verbindungen unter Verwendung des `https://` URI-Schemas erfolgt.</span><span class="sxs-lookup"><span data-stu-id="e7000-123">The camera and location capabilities are only available when accessing the Web Client through SSL secured HTTP connections, using the `https://` URI scheme.</span></span> 

<span data-ttu-id="e7000-124">Die einzige Ausnahme ist die Verbindung zu `http://localhost`, die für Entwicklungs- und Testzwecke verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e7000-124">The only exception is connecting to `http://localhost`, used for development and test purposes.</span></span>


## <a name="working-with-virtualization-technologies"></a><span data-ttu-id="e7000-125">Mit Virtualisierungstechnologien arbeiten</span><span class="sxs-lookup"><span data-stu-id="e7000-125">Working with Virtualization Technologies</span></span>

<span data-ttu-id="e7000-126">Wenn eine Verbindung mit [!INCLUDE[prod_short](includes/prod_short.md)] über Remotedesktop oder eine andere Virtualisierung hergestellt wird, ist der Zugriff auf die Kamera oder den Standort möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e7000-126">When connecting to [!INCLUDE[prod_short](includes/prod_short.md)] through Remote Desktop or another virtualization, the access to camera or location might not be available.</span></span> <span data-ttu-id="e7000-127">Verwenden Sie in diesem Fall stattdessen das physische System.</span><span class="sxs-lookup"><span data-stu-id="e7000-127">If this is the case, use the physical system instead.</span></span>

## <a name="antivirus-software"></a><span data-ttu-id="e7000-128">Antivirensoftware</span><span class="sxs-lookup"><span data-stu-id="e7000-128">Antivirus Software</span></span>
<span data-ttu-id="e7000-129">Es gibt Antivirensoftware, die den Zugriff auf die Kamera und den Standort standardmäßig blockiert.</span><span class="sxs-lookup"><span data-stu-id="e7000-129">Some antivirus software block access to camera and location by default.</span></span> <span data-ttu-id="e7000-130">Denken Sie daran, die Einstellungen Ihrer Antivirensoftware zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e7000-130">Remember to check your antivirus software settings.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7000-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7000-131">See Also</span></span>
[<span data-ttu-id="e7000-132">Kamera in AL implementieren</span><span class="sxs-lookup"><span data-stu-id="e7000-132">Implementing the Camera in AL</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-implement-camera-al)  
[<span data-ttu-id="e7000-133">Standort in AL implementieren</span><span class="sxs-lookup"><span data-stu-id="e7000-133">Implementing the Location in AL</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-implement-location-al)


[!INCLUDE[footer-include](includes/footer-banner.md)]