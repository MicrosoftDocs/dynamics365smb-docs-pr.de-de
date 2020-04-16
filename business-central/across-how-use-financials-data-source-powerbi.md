---
title: Berichte für Business Central in Power BI verwenden | Microsoft Docs
description: Sie können Ihre Daten zur Verfügung stellen als Datenquelle in Power BI und leistungsstarke Berichte über den Zustand Ihres Geschäftes erstellen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 4f140303f037ea4a914cba1ded44fd453bcdfabb
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187892"
---
# <a name="using-prodlong-as-power-bi-data-source-for-building-reports"></a><span data-ttu-id="4f690-103">[!INCLUDE [prodlong](includes/prodlong.md)] als Power BI-Datenquelle für das Erstellen von Berichten nutzen</span><span class="sxs-lookup"><span data-stu-id="4f690-103">Using [!INCLUDE [prodlong](includes/prodlong.md)] as Power BI Data Source for Building Reports</span></span>

<span data-ttu-id="4f690-104">Sie können Ihre [!INCLUDE[prodlong](includes/prodlong.md)]-Daten zur Verfügung stellen als Datenquelle in Power BI und leistungsstarke Berichte über den Zustand Ihres Geschäftes erstellen.</span><span class="sxs-lookup"><span data-stu-id="4f690-104">You can make your [!INCLUDE[prodlong](includes/prodlong.md)] data available as a data source in Power BI and build powerful reports of the state of your business.</span></span>  

<span data-ttu-id="4f690-105">Sie müssen ein gültiges Konto bei [!INCLUDE[prodshort](includes/prodshort.md)] und Power BI haben.</span><span class="sxs-lookup"><span data-stu-id="4f690-105">You must have a valid account with [!INCLUDE[prodshort](includes/prodshort.md)] and with Power BI.</span></span> <span data-ttu-id="4f690-106">Sie müssen auch [Power BI Desktop](https://powerbi.microsoft.com/desktop/) herunterladen.</span><span class="sxs-lookup"><span data-stu-id="4f690-106">You must also download [Power BI Desktop](https://powerbi.microsoft.com/desktop/).</span></span> <span data-ttu-id="4f690-107">Weitere Informationen finden Sie unter [Schnellstart: Stellen Sie eine Verbindung zu Daten her in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).</span><span class="sxs-lookup"><span data-stu-id="4f690-107">For more information, see [Quickstart: Connect to data in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).</span></span>  

## <a name="to-add-prodshort-as-a-data-source-in-power-bi-desktop"></a><span data-ttu-id="4f690-108">So fügen Sie [!INCLUDE[prodshort](includes/prodshort.md)] als Datenquelle in Power BI Desktop hinzu</span><span class="sxs-lookup"><span data-stu-id="4f690-108">To add [!INCLUDE[prodshort](includes/prodshort.md)] as a data source in Power BI Desktop</span></span>

1. <span data-ttu-id="4f690-109">In Power BI Desktop im linken Navigationsbereich, wählen Sie **Daten abrufen** aus.</span><span class="sxs-lookup"><span data-stu-id="4f690-109">In Power BI Desktop, in the left navigation pane, choose **Get Data**.</span></span>
2. <span data-ttu-id="4f690-110">Auf der Seite **Daten abrufen** wählen Sie **Onlinedienste** aus, wählen Sie **Microsoft Dynamics 365 Business Central** und dann die Schaltfläche **Verbinden** aus.</span><span class="sxs-lookup"><span data-stu-id="4f690-110">On the **Get Data** page, choose **Online Services**, choose **Microsoft Dynamics 365 Business Central**, and then choose the **Connect** button.</span></span>
3. <span data-ttu-id="4f690-111">Power BI zeigt einen Assistenten an, der Sie durch den Verbindungsprozess führt, einschließlich der Anmeldung bei [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="4f690-111">Power BI displays a wizard that will guide you through the connection process, including signing into [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="4f690-112">Wählen Sie **Anmelden**, und wählen Sie dann das entsprechende Konto.</span><span class="sxs-lookup"><span data-stu-id="4f690-112">Choose **Sign in**, and then choose the relevant account.</span></span> <span data-ttu-id="4f690-113">Verwenden Sie dasselbe Konto, mit dem Sie sich bei [!INCLUDE [prodshort](includes/prodshort.md)] anmelden.</span><span class="sxs-lookup"><span data-stu-id="4f690-113">Use the same account that you sign into [!INCLUDE [prodshort](includes/prodshort.md)] with.</span></span>
4. <span data-ttu-id="4f690-114">Klicken Sie auf die Schaltfläche **Verbinden** zum Fortfahren.</span><span class="sxs-lookup"><span data-stu-id="4f690-114">Choose the **Connect** button to continue.</span></span> <span data-ttu-id="4f690-115">Der Power BI-Assistent zeigt eine Liste von Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]-Umgebungen, Unternehmen und Datenquellen an.</span><span class="sxs-lookup"><span data-stu-id="4f690-115">The Power BI wizard shows a list of Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)] environments, companies, and data sources.</span></span> <span data-ttu-id="4f690-116">Diese Datenquellen repräsentieren alle Webdienste, die Sie ab [!INCLUDE [prodshort](includes/prodshort.md)] veröffentlicht haben.</span><span class="sxs-lookup"><span data-stu-id="4f690-116">These data sources represent all the web services that you have published from [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>

    <span data-ttu-id="4f690-117">Sie können stattdessen auch eine neue Webdienst-URL in [!INCLUDE [prodshort](includes/prodshort.md)] erstellen.</span><span class="sxs-lookup"><span data-stu-id="4f690-117">You can also create a new web service URL in [!INCLUDE [prodshort](includes/prodshort.md)] instead.</span></span> <span data-ttu-id="4f690-118">Wählen Sie eine der folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="4f690-118">Choose one of the following methods:</span></span>

      - <span data-ttu-id="4f690-119">Verwenden Sie die Aktion **Datensatz erstellen** auf der Seite **Webdienste**</span><span class="sxs-lookup"><span data-stu-id="4f690-119">Use the **Create Data Set** action on the **Web Services** page</span></span>
      - <span data-ttu-id="4f690-120">Verwenden Sie den Leitfaden **Berichte einrichten** Unterstützte Einrichtung</span><span class="sxs-lookup"><span data-stu-id="4f690-120">Use the **Set Up Reporting** Assisted Setup guide</span></span>
      - <span data-ttu-id="4f690-121">Wählen Sie in einer beliebigen Liste die Aktion **Bearbeiten in Excel**</span><span class="sxs-lookup"><span data-stu-id="4f690-121">Choose the **Edit in Excel** action in any lists</span></span>

5. <span data-ttu-id="4f690-122">Geben Sie die Daten an, die Sie Ihrem Datenmodell hinzufügen möchten, und wählen Sie dann die Schaltfläche **Laden** aus.</span><span class="sxs-lookup"><span data-stu-id="4f690-122">Specify the data you want to add to your data model, and then choose the **Load** button.</span></span>
6. <span data-ttu-id="4f690-123">Wiederholen Sie die vorherigen Schritte, um zusätzliche [!INCLUDE [prodshort](includes/prodshort.md)] oder andere Daten Ihrem Power BI Datenmodell hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4f690-123">Repeat the previous steps to add additional [!INCLUDE [prodshort](includes/prodshort.md)], or other data, to your Power BI data model.</span></span>

> [!NOTE]  
> <span data-ttu-id="4f690-124">Sobald Sie sich erfolgreich verbunden haben mit [!INCLUDE [prodshort](includes/prodshort.md)] werden Sie nicht mehr aufgefordert, sich anzumelden.</span><span class="sxs-lookup"><span data-stu-id="4f690-124">Once you have successfully connected to [!INCLUDE [prodshort](includes/prodshort.md)], you will not be prompted again to sign in.</span></span>

<span data-ttu-id="4f690-125">Sobald die Daten geladen sind, können Sie sie in der rechten Navigation auf der Seite sehen.</span><span class="sxs-lookup"><span data-stu-id="4f690-125">Once the data is loaded, you can see it in the right navigation on the page.</span></span> <span data-ttu-id="4f690-126">Sie haben die Verbindung zu Ihren [!INCLUDE [prodshort](includes/prodshort.md)]-Daten erfolgreich hergestellt, und Sie können mit dem Aufbau Ihres Power BI-Berichts beginnen.</span><span class="sxs-lookup"><span data-stu-id="4f690-126">You have successfully connected to your [!INCLUDE [prodshort](includes/prodshort.md)] data, and you can begin building your Power BI report.</span></span>  

<span data-ttu-id="4f690-127">Bevor Sie Ihren Bericht erstellen, empfiehlt es sich, die Microsoft [!INCLUDE [prodshort](includes/prodshort.md)] Designndatei zu importieren.</span><span class="sxs-lookup"><span data-stu-id="4f690-127">Before building your report, we recommend that you import the [!INCLUDE [prodshort](includes/prodshort.md)] theme file.</span></span>  <span data-ttu-id="4f690-128">Die Designdatei erstellt eine Farbpalette, damit Sie Berichte im selben Farbstil erstellen können, wie bei den Microsoft [!INCLUDE [prodshort](includes/prodshort.md)] Anwendungen, ohne benutzerdefinierte Farben für jede Grafik definieren zu müssen.</span><span class="sxs-lookup"><span data-stu-id="4f690-128">The theme file will create a color palette so that you can build reports with the same color styling as the [!INCLUDE [prodshort](includes/prodshort.md)] apps without requiring you to define custom colors for each visual.</span></span>

<span data-ttu-id="4f690-129">Weitere Informationen finden Sie in der [Power BI-Dokumentation](/power-bi/consumer/).</span><span class="sxs-lookup"><span data-stu-id="4f690-129">For more information, see the [Power BI documentation](/power-bi/consumer/).</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="4f690-130">Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="4f690-130">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="4f690-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f690-131">See Also</span></span>

[<span data-ttu-id="4f690-132">Aktivieren Sie Ihre Geschäftsdaten für Power BI</span><span class="sxs-lookup"><span data-stu-id="4f690-132">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
[<span data-ttu-id="4f690-133">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="4f690-133">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="4f690-134">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="4f690-134">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="4f690-135">Geschäftsdaten aus anderen Finanzsystemen importieren</span><span class="sxs-lookup"><span data-stu-id="4f690-135">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="4f690-136">[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="4f690-136">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="4f690-137">Finanzen</span><span class="sxs-lookup"><span data-stu-id="4f690-137">Finance</span></span>](finance.md)  
[<span data-ttu-id="4f690-138">Schnellstart: Stellen Sie eine Verbindung zu Daten her in Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="4f690-138">Quickstart: Connect to data in Power BI Desktop</span></span>](/power-bi/desktop-quickstart-connect-to-data)  
