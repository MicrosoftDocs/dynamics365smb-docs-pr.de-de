---
title: Dynamics 365 for Financials anpassen | Microsoft Docs
description: "Dynamics 365 for Financials Erweiterungen bauen, anzeigen und fördern."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: cc355c7b4cd51412ec0b5c95398c2d7b50a13f94
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017


---
# <a name="extending-included365finlongincludesd365finlongmdmd"></a><span data-ttu-id="42f2d-103">Erweitern [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]</span><span class="sxs-lookup"><span data-stu-id="42f2d-103">Extending [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]</span></span>
<span data-ttu-id="42f2d-104">Es gibt viele Vorteile, [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] als Plattform für das Bauen von Apps zu nutzen:</span><span class="sxs-lookup"><span data-stu-id="42f2d-104">There are plenty of benefits of using [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] as a platform for App builders:</span></span>

* <span data-ttu-id="42f2d-105">[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]ergänzt die bewährte Microsoft Online Lösung mit Ihren Kenntnissen</span><span class="sxs-lookup"><span data-stu-id="42f2d-105">Enrich [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], a proven Microsoft online solution, with your expertise</span></span>  
* <span data-ttu-id="42f2d-106">Nutzen Sie die Marke Dynamics 365 – eine Marke, dir Millionen von Benutzern kennen und vertrauen</span><span class="sxs-lookup"><span data-stu-id="42f2d-106">Leverage the Dynamics 365 brand – a brand that millions of users know and trust</span></span>  
* <span data-ttu-id="42f2d-107">Erreichen Sie mehr Debitoren für Ihre Geschäfts-Apps mit [Microsoft AppSource](https://appsource.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="42f2d-107">Reach more customers for your business apps with [Microsoft AppSource](https://appsource.microsoft.com/)</span></span>  
* <span data-ttu-id="42f2d-108">Erzielen Sie mehr mit eine Plattform, die eine moderne Benutzeroberfläche und eine Angebotsskala bietet</span><span class="sxs-lookup"><span data-stu-id="42f2d-108">Achieve more with a platform that delivers a modern experience and offers scale</span></span>  
* <span data-ttu-id="42f2d-109">Sie bündeln Sie mit intelligenten Geschäfts-Apps wie PowerApps, Flow, Power BI und Cortana-Intelligence und vielen mehr</span><span class="sxs-lookup"><span data-stu-id="42f2d-109">Bundle with intelligent business apps such as PowerApps, Flow, Power BI, Cortana Intelligence, and many more</span></span>  

## <a name="to-bring-your-included365finincludesd365finmdmd-app-into-appsource"></a><span data-ttu-id="42f2d-110">Um Ihre [!INCLUDE[d365fin](includes/d365fin_md.md)] in AppSource zu transferieren:</span><span class="sxs-lookup"><span data-stu-id="42f2d-110">To bring your [!INCLUDE[d365fin](includes/d365fin_md.md)] app into AppSource:</span></span>
+ <span data-ttu-id="42f2d-111">Erstellen Sie Ihre Konten</span><span class="sxs-lookup"><span data-stu-id="42f2d-111">Create your accounts</span></span>  
<span data-ttu-id="42f2d-112">Wir möchten, dass Sie Zugriff auf alle erforderlichen Tools haben!</span><span class="sxs-lookup"><span data-stu-id="42f2d-112">We want you to have access to all the necessary tools!</span></span> <span data-ttu-id="42f2d-113">Sie müssen eine Microsoft-Partners-Netzwerk ID, ein Entwicklerkonto und ein PSBC-Konto haben.</span><span class="sxs-lookup"><span data-stu-id="42f2d-113">You must have a Microsoft Partner Network ID, a Developer account, and a PSBC account.</span></span>
<span data-ttu-id="42f2d-114">Weitere Informationen darüber, wie Sie die Konten an einem Ort zusammenfassen, finden Sie im Dokument [Create your accounts.pdf](https://go.microsoft.com/fwlink/?linkid=841514) im Download Center.</span><span class="sxs-lookup"><span data-stu-id="42f2d-114">For more information about how you can get your accounts in place, get the [Create your accounts.pdf](https://go.microsoft.com/fwlink/?linkid=841514) document from the Download Center.</span></span>

+ <span data-ttu-id="42f2d-115">Kontaktieren Sie uns zu Ihren App-Ideen</span><span class="sxs-lookup"><span data-stu-id="42f2d-115">Engage with us about your app idea</span></span>  
<span data-ttu-id="42f2d-116">Teilen Sie Ihre [!INCLUDE[d365fin](includes/d365fin_md.md)] App-Idee mit uns in Microsoft AppSource!</span><span class="sxs-lookup"><span data-stu-id="42f2d-116">Share your [!INCLUDE[d365fin](includes/d365fin_md.md)] app idea with us on Microsoft AppSource!</span></span> <span data-ttu-id="42f2d-117">Nachdem Sie Ihre Idee übermittelt haben, binden wir Sie ein und stellen Ihnen alles Notwendige bereit, damit Sie mit der Arbeit an Ihrer App beginnen können.</span><span class="sxs-lookup"><span data-stu-id="42f2d-117">After submitting your idea, we will engage with you and provide you with everything you need to start working on your app.</span></span>
<span data-ttu-id="42f2d-118">Weitere Informationen über alle Schritte finden Sie im Dokument [Engage with us about your app idea document.pdf](https://go.microsoft.com/fwlink/?linkid=841515) im Download Center.</span><span class="sxs-lookup"><span data-stu-id="42f2d-118">For more information about all the steps, get the [Engage with us about your app idea document.pdf](https://go.microsoft.com/fwlink/?linkid=841515) document from the Download Center.</span></span>

+ <span data-ttu-id="42f2d-119">Entwickeln Sie die technischen Aspekte Ihrer App</span><span class="sxs-lookup"><span data-stu-id="42f2d-119">Develop the technical aspects of your app</span></span>    
<span data-ttu-id="42f2d-120">Nachdem Sie Ihre eigene App-Entwicklungsumgebung eingerichtet haben, können Sie Ihre App entwickeln.</span><span class="sxs-lookup"><span data-stu-id="42f2d-120">After you have set up your own app development environment, you can develop your app.</span></span>
<span data-ttu-id="42f2d-121">Weitere Informationen über alles, was Sie wissen müssen und wie Sie die technischen Aspekte Ihrer App Ihrer [!INCLUDE[d365fin](includes/d365fin_md.md)] entwickeln, finden Sie im [Develop the technical aspects of your app.pdf](https://go.microsoft.com/fwlink/?linkid=841516) im Download Center.</span><span class="sxs-lookup"><span data-stu-id="42f2d-121">For more information about everything you need to know about how to develop the technical aspects of your [!INCLUDE[d365fin](includes/d365fin_md.md)] app, get the [Develop the technical aspects of your app.pdf](https://go.microsoft.com/fwlink/?linkid=841516) document from the Download Center.</span></span>

+ <span data-ttu-id="42f2d-122">Entwickeln Sie die Marketing-Aspekte Ihrer App</span><span class="sxs-lookup"><span data-stu-id="42f2d-122">Develop the marketing aspects of your app</span></span>  
<span data-ttu-id="42f2d-123">Die Funktionen und die Funktionalität Ihrer App reicht nicht, mögliche Käufer zu finden.</span><span class="sxs-lookup"><span data-stu-id="42f2d-123">Simply listing your app's features and functionality will not convert prospects to buyers.</span></span> <span data-ttu-id="42f2d-124">Weitere Informationen darüber, wie Sie Ihre App im AppSource-Marktplatz am besten vermarkten, finden Sie im Dokument [Develop the marketing aspects of your app.pdf](https://go.microsoft.com/fwlink/?linkid=841518) im Download Center.</span><span class="sxs-lookup"><span data-stu-id="42f2d-124">For more information about how to best market your app in the AppSource marketplace, get the [Develop the marketing aspects of your app.pdf](https://go.microsoft.com/fwlink/?linkid=841518) from the Download Center.</span></span>

+ <span data-ttu-id="42f2d-125">Veröffentlichen Sie Ihre App</span><span class="sxs-lookup"><span data-stu-id="42f2d-125">Publish your app</span></span>  
<span data-ttu-id="42f2d-126">Bevor wir veröffentlichen, arbeiten wir mit Ihnen zusammen, um sicherzustellen, dass Ihre App auf Microsoft AppSource und in Ihrer persönlichen Zugangsseite steht!</span><span class="sxs-lookup"><span data-stu-id="42f2d-126">Before we publish, we will collaborate with you to ensure that your app stands out on Microsoft AppSource and on your own landing page!</span></span> <span data-ttu-id="42f2d-127">Wir müssen Ihre App prüfen, um sicherzustellen, dass sei gut vermarktet, vertrauenswürdig und auf dem neuesten Stand ist.</span><span class="sxs-lookup"><span data-stu-id="42f2d-127">We need to validate your app to ensure it is marketed well, trustworthy, and up to date.</span></span>
<span data-ttu-id="42f2d-128">Weitere Informationen über den Prüfungsprozess und wie Ihre App publiziert wird finden Sie im Dokument [Publish your app.pdf](https://go.microsoft.com/fwlink/?linkid=841517) im Download Center.</span><span class="sxs-lookup"><span data-stu-id="42f2d-128">For more information about the validation process and how to publish your app, get the [Publish your app.pdf](https://go.microsoft.com/fwlink/?linkid=841517) document from the Download Center.</span></span>

## <a name="need-help"></a><span data-ttu-id="42f2d-129">Benötigen Sie Hilfe?</span><span class="sxs-lookup"><span data-stu-id="42f2d-129">Need help?</span></span>
<span data-ttu-id="42f2d-130">Wenn Sie etwas Unterstützung möchten, können Sie einen App-Experten aus der folgenden Liste kontaktieren:</span><span class="sxs-lookup"><span data-stu-id="42f2d-130">If you would like some coaching, you can contact an app subject matter expert from the following list:</span></span>

* <span data-ttu-id="42f2d-131">Cloud Ready Software, [http://cloud-ready-software.com](http://cloud-ready-software.com/)</span><span class="sxs-lookup"><span data-stu-id="42f2d-131">Cloud Ready Software, [http://cloud-ready-software.com](http://cloud-ready-software.com/)</span></span>  
* <span data-ttu-id="42f2d-132">Dynamics App Alliance, [http://dynamicsappalliance.com](http://dynamicsappalliance.com/)</span><span class="sxs-lookup"><span data-stu-id="42f2d-132">Dynamics App Alliance, [http://dynamicsappalliance.com](http://dynamicsappalliance.com/)</span></span>

<span data-ttu-id="42f2d-133">Partner auf der Liste:</span><span class="sxs-lookup"><span data-stu-id="42f2d-133">Partners in this list:</span></span>

* <span data-ttu-id="42f2d-134">Werden alphabetisch aufgeführt</span><span class="sxs-lookup"><span data-stu-id="42f2d-134">Are listed alphabetically</span></span>  
* <span data-ttu-id="42f2d-135">Helfen oder haben mindestens drei Partnern beim Vermarkten von Apps in Microsoft AppSource geholfen</span><span class="sxs-lookup"><span data-stu-id="42f2d-135">Are assisting or have assisted a minimum of three partners with bringing apps into Microsoft AppSource</span></span>  
* <span data-ttu-id="42f2d-136">Bieten einen Paketservice an (und ist auf der Website aufgeführt) zur App-Anleitung, die sie anbieten</span><span class="sxs-lookup"><span data-stu-id="42f2d-136">Have a packaged service available (and listed on their website) about the app guidance that they provide</span></span>  

<span data-ttu-id="42f2d-137">Wenn Sie glauben, Sie müssten als App-Dienstpartner aufgeführt sein, zögern Sie nicht, [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com) zu kontaktieren.</span><span class="sxs-lookup"><span data-stu-id="42f2d-137">If you believe you should be listed as an app service partner, don't hesitate to reach out to [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span></span>

## <a name="questions"></a><span data-ttu-id="42f2d-138">Fragen?</span><span class="sxs-lookup"><span data-stu-id="42f2d-138">Questions?</span></span>
<span data-ttu-id="42f2d-139">Diese [FAQ](https://go.microsoft.com/fwlink/?linkid=841520) antworten auf der die meisten allgemeinen Fragen, die Sie möglicherweise zu Apps haben [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="42f2d-139">This [FAQ](https://go.microsoft.com/fwlink/?linkid=841520) responds to the most common questions you might have about apps for [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="42f2d-140">Wenn Sie weitere Fragen haben, zögern Sie nicht, Ihren lokalen Microsoft-Vertreter zu kontaktieren, bei dem sich der Serviceartikel befindet oder eine E-Mail zu senden an [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="42f2d-140">If you have further questions, don't hesitate to contact your local Microsoft representative or email [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span></span>

## <a name="further-resources"></a><span data-ttu-id="42f2d-141">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="42f2d-141">Further Resources</span></span>
<span data-ttu-id="42f2d-142">Auf der [DLP-Themenseite](https://mbspartner.microsoft.com/BFI/Topic/76) DLP-Themenseite finden Sie weitere Ressourcen für die App-Entwicklung.</span><span class="sxs-lookup"><span data-stu-id="42f2d-142">Please find further resources for app development on our [DLP topic page](https://mbspartner.microsoft.com/BFI/Topic/76) DLP topic page.</span></span> <span data-ttu-id="42f2d-143">Einige wählten jene, die unten verfügbar sind:</span><span class="sxs-lookup"><span data-stu-id="42f2d-143">Some selected ones are available below:</span></span>
-   [<span data-ttu-id="42f2d-144">Benutzer-Registrierung und daraus folgende Fakturierung</span><span class="sxs-lookup"><span data-stu-id="42f2d-144">User Registration and Subsequent Billing </span></span>](http://download.microsoft.com/download/3/2/0/320D0286-8810-4A8F-B7DD-523ED87D441B/FAQ on apps for Dynamics 365 for Financials.pdf)



## <a name="see-also"></a><span data-ttu-id="42f2d-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42f2d-145">See Also</span></span>
<span data-ttu-id="42f2d-146">[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="42f2d-146">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="42f2d-147">[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="42f2d-147">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="42f2d-148">https://appsource.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="42f2d-148">https://appsource.microsoft.com</span></span>](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365-for-financials&page=1)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
