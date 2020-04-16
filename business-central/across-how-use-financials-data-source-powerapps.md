---
title: Verwenden Sie die Daten, um eine App zu erstellen| Microsoft Docs
description: Sie können Daten aus Business Central zur Verfügung stellen und eine OData URL Ihrer Webdienste festlegen, um eine Geschäfts-App mithilfe von Power Apps zu erstellen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OData, Power App, SOAP
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: f6b771b0107214702785d2b124983eb369741a84
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187916"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a><span data-ttu-id="53ecf-103">Verknüpfung mit Business Central, um eine Geschäfts-App mithilfe von Power Apps zu erstellen</span><span class="sxs-lookup"><span data-stu-id="53ecf-103">Connecting to Your Business Central Data to Build a Business App Using Power Apps</span></span>

<span data-ttu-id="53ecf-104">Sie können die [!INCLUDE[prodshort](includes/prodshort.md)] Daten als Datenquelle in Power Apps bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="53ecf-104">You can make your [!INCLUDE[prodshort](includes/prodshort.md)] data available as a data source in Power Apps.</span></span>  

> [!NOTE]  
> <span data-ttu-id="53ecf-105">Sie müssen ein gültiges Konto bei [!INCLUDE[prodshort](includes/prodshort.md)] und Power Apps haben.</span><span class="sxs-lookup"><span data-stu-id="53ecf-105">You must have a valid account with [!INCLUDE[prodshort](includes/prodshort.md)] and with Power Apps.</span></span>  

## <a name="to-add-prodshort-as-a-data-source-in-power-apps"></a><span data-ttu-id="53ecf-106">So fügen Sie [!INCLUDE[prodshort](includes/prodshort.md)] als Datenquelle in Power Apps hinzu</span><span class="sxs-lookup"><span data-stu-id="53ecf-106">To add [!INCLUDE[prodshort](includes/prodshort.md)] as a data source in Power Apps</span></span>

1. <span data-ttu-id="53ecf-107">In Ihrem Browser navigieren und zu [powerapps.microsoft.com](https://powerapps.microsoft.com/) gehen und sich dann anmelden.</span><span class="sxs-lookup"><span data-stu-id="53ecf-107">In your browser, navigate to [powerapps.microsoft.com](https://powerapps.microsoft.com/), and then sign in.</span></span>
2. <span data-ttu-id="53ecf-108">Wählen Sie auf der Startseite die **Apps**, **Erstelle eine App** und **Canvas** um eine neue Canvas-App zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="53ecf-108">On the Home page, choose the **Apps**, **Create an app** and **Canvas** to create a new canvas app.</span></span> <span data-ttu-id="53ecf-109">Die App ist zur Verwendung auf einem mobilen Gerät vorgesehen, aber Sie können auch wählen, eine eigene Vorlage zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="53ecf-109">This app will be designed for use on a mobile device, but you can also choose to use another template.</span></span>

    <span data-ttu-id="53ecf-110">Der nächste Schritt, um ein Power App zu erstellen ist die Auswahl der Daten.</span><span class="sxs-lookup"><span data-stu-id="53ecf-110">The next step to create a Power App is to select your data.</span></span> <span data-ttu-id="53ecf-111">Wählen Sie das Pfeilsymbol aus und wählen Sie dann die Option **Neue Verbindung** in der oberen linken Seite der Seite aus.</span><span class="sxs-lookup"><span data-stu-id="53ecf-111">Choose the Arrow icon then choose the **New connection** option in the upper left side of the page.</span></span>
3. <span data-ttu-id="53ecf-112">In der Liste der verfügbaren Verbindungscodes wählen Sie **Business Central** und dann die Schaltfläche **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="53ecf-112">In the list of available connections, choose **Business Central**, and then choose the **Create** button.</span></span>

    <span data-ttu-id="53ecf-113">Power Apps PowerApps verbinden sich mit Ihrem [!INCLUDE [prodshort](includes/prodshort.md)] mithilfe der Anmeldeinformationen, mit denen Sie sich anmelden.</span><span class="sxs-lookup"><span data-stu-id="53ecf-113">Power Apps will connect to your [!INCLUDE [prodshort](includes/prodshort.md)] using the credentials that you are signed in with.</span></span> <span data-ttu-id="53ecf-114">Wenn Sie KEIN Administrator Ihrer [!INCLUDE [prodshort](includes/prodshort.md)] sind, müssen Sie sich möglicherweise bei einem anderen Konto anmelden.</span><span class="sxs-lookup"><span data-stu-id="53ecf-114">If you are not an administrator of your [!INCLUDE [prodshort](includes/prodshort.md)], you may have to sign in with another account.</span></span>  

4. <span data-ttu-id="53ecf-115">Power Apps zeigt eine Liste der *Umgebungen und Unternehmungen* an, die in [!INCLUDE [prodshort](includes/prodshort.md)] verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="53ecf-115">Power Apps will display a list of *Environments and companies* that are available from [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="53ecf-116">Wählen Sie die Umgebung und das Unternehmen aus, in der sich die Daten be finden, zu denen Sie eine Verbindung herstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="53ecf-116">Choose the environment and company that contains the data you want to connect to.</span></span> <span data-ttu-id="53ecf-117">Als Nächstes wird eine Liste der APIs angezeigt.</span><span class="sxs-lookup"><span data-stu-id="53ecf-117">Next, you will be presented with a list of APIs.</span></span> <span data-ttu-id="53ecf-118">Wählen Sie die **API**, die Sie verbinden möchten.</span><span class="sxs-lookup"><span data-stu-id="53ecf-118">Select the **API** you want to connect to.</span></span>

<span data-ttu-id="53ecf-119">Diese so genannten Tabellen sind Teil der [!INCLUDE [prodshort](includes/prodshort.md)] API.</span><span class="sxs-lookup"><span data-stu-id="53ecf-119">These so-called tables are part of the [!INCLUDE [prodshort](includes/prodshort.md)] API.</span></span> <span data-ttu-id="53ecf-120">Sie müssen die Endpunkte nicht selber konfigurieren, der [!INCLUDE [prodshort](includes/prodshort.md)] Connector für Power Apps macht dies für Sie.</span><span class="sxs-lookup"><span data-stu-id="53ecf-120">You do not have to configure the end points yourself - the [!INCLUDE [prodshort](includes/prodshort.md)] connector for Power Apps does it for you.</span></span>  

> [!NOTE]
> <span data-ttu-id="53ecf-121">Wenn Sie Daten aus anderen Tabellen in [!INCLUDE [prodshort](includes/prodshort.md)] in Ihre Anwendung aufnehmen möchten, müssen Sie mit einem Entwickler zusammenarbeiten, um eine benutzerdefinierte API in [!INCLUDE [prodshort](includes/prodshort.md)] zu definieren und diese benutzerdefinierte API dann über einen benutzerdefinierten Konnektor in Power Apps zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="53ecf-121">If you want to include data from other tables in [!INCLUDE [prodshort](includes/prodshort.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE [prodshort](includes/prodshort.md)] and then consume that custom API through a custom connector in Power Apps.</span></span> <span data-ttu-id="53ecf-122">Weitere Informationen finden Sie unter [Erstellen Sie einen benutzerdefinierten Connector von Grund auf neu](/connectors/custom-connectors/define-blank).</span><span class="sxs-lookup"><span data-stu-id="53ecf-122">For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).</span></span>  

<span data-ttu-id="53ecf-123">Zu diesem Zeitpunkt haben Sie erfolgreich Ihre [!INCLUDE [prodshort](includes/prodshort.md)]-Daten verbunden und sind bereit, Ihre Power App zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="53ecf-123">At this point, you have successfully connected to your [!INCLUDE [prodshort](includes/prodshort.md)] data and are ready to begin building your PowerApp.</span></span> <span data-ttu-id="53ecf-124">Sie können zusätzliche Bildschirme hinzufügen und an weitere Daten von Ihrem [!INCLUDE [prodshort](includes/prodshort.md)] anschließen.</span><span class="sxs-lookup"><span data-stu-id="53ecf-124">You can add additional screens and connect to additional data from your [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="53ecf-125">Weitere Informationen finden Sie unter [Erstellen Sie eine Canvas-App aus einer Vorlage in Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive).</span><span class="sxs-lookup"><span data-stu-id="53ecf-125">For more information, see [Create a canvas app from a template in Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive).</span></span>  

<span data-ttu-id="53ecf-126">Wenn Sie Ihre App entworfen und erstellt haben, können Sie diese mit Ihre Kollegen teilen.</span><span class="sxs-lookup"><span data-stu-id="53ecf-126">When you have designed and built your app, you can share it with your colleagues.</span></span> <span data-ttu-id="53ecf-127">Weitere Informationen finden Sie unter [Speichern und veröffentlichen Sie eine Canvas-App in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span><span class="sxs-lookup"><span data-stu-id="53ecf-127">For more information, see [Save and publish a canvas app in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span></span>  

> [!NOTE]
> <span data-ttu-id="53ecf-128">Wenn Sie [!INCLUDE [prodshort](includes/prodshort.md)] lokal verbinden möchten, müssen Sie den **Business Central (lokal)** Connector in Schritt 3 auswählen.</span><span class="sxs-lookup"><span data-stu-id="53ecf-128">If you want to connect to [!INCLUDE [prodshort](includes/prodshort.md)] on-premises, then you must choose the **Business Central (on-premises)** connector in step 3.</span></span>  

## <a name="see-also"></a><span data-ttu-id="53ecf-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53ecf-129">See Also</span></span>

[<span data-ttu-id="53ecf-130">Erstellen Sie eine Canvas-App aus einer Vorlage in Power Apps</span><span class="sxs-lookup"><span data-stu-id="53ecf-130">Create a canvas app from a template in Power Apps</span></span>](/powerapps/maker/canvas-apps/get-started-test-drive)  
[<span data-ttu-id="53ecf-131">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="53ecf-131">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="53ecf-132">Geschäftsdaten aus anderen Finanzsystemen importieren</span><span class="sxs-lookup"><span data-stu-id="53ecf-132">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="53ecf-133">[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="53ecf-133">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="53ecf-134">Finanzen</span><span class="sxs-lookup"><span data-stu-id="53ecf-134">Finance</span></span>](finance.md)  
[<span data-ttu-id="53ecf-135">Erste Schritte mit dem Entwickeln von Verbindungs-Apps für Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="53ecf-135">Getting Started Developing Connect Apps for Dynamics 365 Business Central</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
