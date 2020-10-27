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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 718d4378a897b187ba3073449869184fef5cec98
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924828"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a><span data-ttu-id="7cb46-103">Verknüpfung mit Business Central, um eine Geschäfts-App mithilfe von Power Apps zu erstellen</span><span class="sxs-lookup"><span data-stu-id="7cb46-103">Connecting to Your Business Central Data to Build a Business App Using Power Apps</span></span>

<span data-ttu-id="7cb46-104">Sie können die [!INCLUDE[prodshort](includes/prodshort.md)] Daten als Datenquelle in Power Apps bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7cb46-104">You can make your [!INCLUDE[prodshort](includes/prodshort.md)] data available as a data source in Power Apps.</span></span>  

> [!NOTE]  
> <span data-ttu-id="7cb46-105">Sie müssen ein gültiges Konto bei [!INCLUDE[prodshort](includes/prodshort.md)] und Power Apps haben.</span><span class="sxs-lookup"><span data-stu-id="7cb46-105">You must have a valid account with [!INCLUDE[prodshort](includes/prodshort.md)] and with Power Apps.</span></span>  

## <a name="to-add-prodshort-as-a-data-source-in-power-apps"></a><span data-ttu-id="7cb46-106">So fügen Sie [!INCLUDE[prodshort](includes/prodshort.md)] als Datenquelle in Power Apps hinzu</span><span class="sxs-lookup"><span data-stu-id="7cb46-106">To add [!INCLUDE[prodshort](includes/prodshort.md)] as a data source in Power Apps</span></span>

1. <span data-ttu-id="7cb46-107">In Ihrem Browser navigieren und zu [powerapps.microsoft.com](https://powerapps.microsoft.com/) gehen und sich dann anmelden.</span><span class="sxs-lookup"><span data-stu-id="7cb46-107">In your browser, navigate to [powerapps.microsoft.com](https://powerapps.microsoft.com/), and then sign in.</span></span>
2. <span data-ttu-id="7cb46-108">Wählen Sie auf der Homepage im Abschnitt **Beginn von Daten** die Kachel **Andere Datenquellen** aus.</span><span class="sxs-lookup"><span data-stu-id="7cb46-108">On the Home page, in the **Start from data** section, choose the **Other data sources** tile.</span></span>  

    <span data-ttu-id="7cb46-109">Dadurch wird Power Apps Studio geöffnet.</span><span class="sxs-lookup"><span data-stu-id="7cb46-109">This opens Power Apps Studio.</span></span> <span data-ttu-id="7cb46-110">Bei der ersten Anmeldung müssen Sie das Land/die Region angeben.</span><span class="sxs-lookup"><span data-stu-id="7cb46-110">On first login, you must specify the country/region.</span></span>  
3. <span data-ttu-id="7cb46-111">In der Liste der verfügbaren Verbindungscodes wählen Sie **Business Central** und dann die Schaltfläche **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="7cb46-111">In the list of available connections, choose **Business Central** , and then choose the **Create** button.</span></span>

    <span data-ttu-id="7cb46-112">Power Apps PowerApps verbinden sich mit Ihrem [!INCLUDE[prodshort](includes/prodshort.md)] mithilfe der Anmeldeinformationen, mit denen Sie sich anmelden.</span><span class="sxs-lookup"><span data-stu-id="7cb46-112">Power Apps will connect to your [!INCLUDE[prodshort](includes/prodshort.md)] using the credentials that you are signed in with.</span></span> <span data-ttu-id="7cb46-113">Wenn Sie KEIN Administrator Ihrer [!INCLUDE[prodshort](includes/prodshort.md)] sind, müssen Sie sich möglicherweise bei einem anderen Konto anmelden.</span><span class="sxs-lookup"><span data-stu-id="7cb46-113">If you are not an administrator of your [!INCLUDE[prodshort](includes/prodshort.md)], you may have to sign in with another account.</span></span>  

4. <span data-ttu-id="7cb46-114">Power Apps zeigt eine Liste der *Umgebungen und Unternehmungen* an, die in [!INCLUDE[prodshort](includes/prodshort.md)] verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="7cb46-114">Power Apps will display a list of *Environments and companies* that are available from [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="7cb46-115">Wählen Sie die Umgebung und das Unternehmen aus, in der sich die Daten befinden, zu denen Sie eine Verbindung herstellen möchten, z. B. *PRODUKTION - Mein Unternehmen* .</span><span class="sxs-lookup"><span data-stu-id="7cb46-115">Choose the environment and company that contains the data you want to connect to, such as *PRODUCTION - My Company* .</span></span>  

5. <span data-ttu-id="7cb46-116">Als Nächstes wird eine Liste der Tabellen angezeigt, die als Teil der API für Ihre Umgebung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="7cb46-116">Next, you will be presented with a list of tables that are exposed as part of the API for your environment.</span></span> <span data-ttu-id="7cb46-117">Wählen Sie die Tabelle aus, zu der Sie eine Verbindung herstellen möchten, und wählen Sie dann **Verbinden** aus.</span><span class="sxs-lookup"><span data-stu-id="7cb46-117">Select the table that you want to connect to, and then choose **Connect** .</span></span>

<span data-ttu-id="7cb46-118">Diese sogenannten Tabellen werden von [!INCLUDE[prodshort](includes/prodshort.md)] Connector für Power Apps als Endpunkte bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="7cb46-118">These so-called tables are exposed as endpoints by the [!INCLUDE[prodshort](includes/prodshort.md)] connector for Power Apps.</span></span>  

> [!NOTE]
> <span data-ttu-id="7cb46-119">Wenn Sie Daten aus anderen Tabellen in [!INCLUDE[prodshort](includes/prodshort.md)] in Ihre Anwendung aufnehmen möchten, müssen Sie mit einem Entwickler zusammenarbeiten, um eine benutzerdefinierte API in [!INCLUDE[prodshort](includes/prodshort.md)] zu definieren und diese benutzerdefinierte API dann über einen benutzerdefinierten Konnektor in Power Apps zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7cb46-119">If you want to include data from other tables in [!INCLUDE[prodshort](includes/prodshort.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE[prodshort](includes/prodshort.md)] and then consume that custom API through a custom connector in Power Apps.</span></span> <span data-ttu-id="7cb46-120">Weitere Informationen finden Sie unter [Erstellen Sie einen benutzerdefinierten Connector von Grund auf neu](/connectors/custom-connectors/define-blank).</span><span class="sxs-lookup"><span data-stu-id="7cb46-120">For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).</span></span>  

<span data-ttu-id="7cb46-121">Zu diesem Zeitpunkt haben Sie erfolgreich Ihre [!INCLUDE[prodshort](includes/prodshort.md)]-Daten verbunden und sind bereit, Ihre Power App zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7cb46-121">At this point, you have successfully connected to your [!INCLUDE[prodshort](includes/prodshort.md)] data and are ready to begin building your PowerApp.</span></span> <span data-ttu-id="7cb46-122">Sie können zusätzliche Bildschirme hinzufügen und an weitere Daten von Ihrem [!INCLUDE[prodshort](includes/prodshort.md)] anschließen.</span><span class="sxs-lookup"><span data-stu-id="7cb46-122">You can add additional screens and connect to additional data from your [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="7cb46-123">Weitere Informationen finden Sie unter [Erstellen einer Canvas-App aus einem Beispiel in Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).</span><span class="sxs-lookup"><span data-stu-id="7cb46-123">For more information, see [Create a canvas app from a sample in Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).</span></span>  

<span data-ttu-id="7cb46-124">Wenn Sie Ihre App entworfen und erstellt haben, können Sie diese mit Ihre Kollegen teilen.</span><span class="sxs-lookup"><span data-stu-id="7cb46-124">When you have designed and built your app, you can share it with your colleagues.</span></span> <span data-ttu-id="7cb46-125">Weitere Informationen finden Sie unter [Speichern und veröffentlichen Sie eine Canvas-App in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span><span class="sxs-lookup"><span data-stu-id="7cb46-125">For more information, see [Save and publish a canvas app in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span></span>  

> [!NOTE]
> <span data-ttu-id="7cb46-126">Wenn Sie [!INCLUDE[prodshort](includes/prodshort.md)] lokal verbinden möchten, müssen Sie den **Business Central (lokal)** Connector in Schritt 3 auswählen.</span><span class="sxs-lookup"><span data-stu-id="7cb46-126">If you want to connect to [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, then you must choose the **Business Central (on-premises)** connector in step 3.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7cb46-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7cb46-127">See Also</span></span>

[<span data-ttu-id="7cb46-128">Erstellen Sie eine Canvas-App aus einer Vorlage in Power Apps</span><span class="sxs-lookup"><span data-stu-id="7cb46-128">Create a canvas app from a template in Power Apps</span></span>](/powerapps/maker/canvas-apps/get-started-test-drive)  
[<span data-ttu-id="7cb46-129">Importieren von Geschäftsdaten aus anderen Finanzsystemen</span><span class="sxs-lookup"><span data-stu-id="7cb46-129">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="7cb46-130">[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="7cb46-130">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="7cb46-131">Erste Schritte mit dem Entwickeln von Verbindungs-Apps für Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="7cb46-131">Getting Started Developing Connect Apps for Dynamics 365 Business Central</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
