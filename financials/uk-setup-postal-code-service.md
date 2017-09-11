---
title: Einrichten der britischen Postleitzahlerweiterung GetAddress.io| Microsoft Docs
description: "Beschreibt die allgemeine Funktionen, die Sie verwenden, um die Daten in den Finanzverhältnissen für Aktivitäten, wie Eingabe von Werten, Sortieren von Daten und Ändern von Ansichten auszuführen."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: getaddress.io, postcodes, extension
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c5a99f7a90b2f832bba3eb088d0faa7514c14708
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-set-up-the-getaddressio-uk-postcodes-extension"></a><span data-ttu-id="5736c-103">Vorgehensweise: Einrichten der britischen Postleitzahlerweiterung für Postleitzahlen, GetAddress.io</span><span class="sxs-lookup"><span data-stu-id="5736c-103">How to: Set Up the GetAddress.io UK Postcodes Extension</span></span>
<span data-ttu-id="5736c-104">Diese Erweiterung macht es einfach Adressen in Großbritannien für Entitäten beispielsweise Kunden, Kontakten, Mitarbeiter, Kreditoren, Bankkonten einzugeben, usw.</span><span class="sxs-lookup"><span data-stu-id="5736c-104">This extension makes it easy to enter addresses in the UK for entities like customers, contacts, employees, vendors, bank accounts, and so on.</span></span> 

<span data-ttu-id="5736c-105">Die britische Postleitzahlerweiterung GetAddress.io verwendet die getAddress API Adressen, um Postleitzahlen in Großbritannien zu finden.</span><span class="sxs-lookup"><span data-stu-id="5736c-105">The GetAddress.io UK Postcodes extension uses the getAddress API to find addresses in postcodes in the UK.</span></span> <span data-ttu-id="5736c-106">Um die Erweiterung zu verwenden, müssen Sie einen Plan und einen API Schlüssel für getAddress API haben.</span><span class="sxs-lookup"><span data-stu-id="5736c-106">To use the extension, you need to get a plan and an API Key for the getAddress API.</span></span> <span data-ttu-id="5736c-107">Das ist einfach und wir Ihnen helfen das tun, wenn Sie die britische Postleitzahlerweiterung GetAddress.io einrichten.</span><span class="sxs-lookup"><span data-stu-id="5736c-107">That's easy, and we help you do that when you set up the GetAddress.io UK Postcodes extension.</span></span> <span data-ttu-id="5736c-108">Pläne basieren auf der Nutzung, manchmal auch als Aufrufe bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="5736c-108">Plans are based on use, or what's sometimes referred to as calls.</span></span> <span data-ttu-id="5736c-109">Ein Aufruf ist in diesem Fall, wenn [!INCLUDE[d365fin](includes/d365fin_md.md)] eine Übersicht der Adressen für eine Postleitzahl anzeigt.</span><span class="sxs-lookup"><span data-stu-id="5736c-109">A call, in this case, is when [!INCLUDE[d365fin](includes/d365fin_md.md)] displays a list of addresses in a postcode.</span></span> <span data-ttu-id="5736c-110">Abhängig davon, wie oft Sie Adressen hinzufügen, wählen Sie den Plan aus, der für Sie sinnvoll ist.</span><span class="sxs-lookup"><span data-stu-id="5736c-110">Depending on how often you add addresses, choose the plan that is best for you.</span></span> <span data-ttu-id="5736c-111">Wenn Sie einfach auf der Seite **Abrufen von API Schlüsseln** auswählen, verwenden Sie den **Kostenlosen** Plan, mit dem Sie 20 Adressen pro hinzufügen können und der für 30 Tage gültig ist.</span><span class="sxs-lookup"><span data-stu-id="5736c-111">If you just choose **Get API Key** in the page, you'll use the **Free** plan, which lets you add 20 addresses per day, and is valid for 30 days.</span></span> 

##<a name="to-set-up-the-getaddressio-uk-postcodes-extension"></a><span data-ttu-id="5736c-112">Einrichten der britischen Postleitzahlerweiterung für Postleitzahlen, GetAddress.io</span><span class="sxs-lookup"><span data-stu-id="5736c-112">To set up the GetAddress.io UK Postcodes extension</span></span> 
1. <span data-ttu-id="5736c-113">Alternativ wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Erweiterung** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="5736c-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Connections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="5736c-114">Im Fenster **Dienstverbindungen** wählen Sie **Britischer Postleitzahl-Dienst** aus.</span><span class="sxs-lookup"><span data-stu-id="5736c-114">In the **Service Connections** window, choose **UK Postcode Service**.</span></span>
3. <span data-ttu-id="5736c-115">Auf der Seite **Postleitzahlanbieterkonfiguration** wählen Sie **Deaktiviert** aus.</span><span class="sxs-lookup"><span data-stu-id="5736c-115">In the **Postcode provider configuration** page, choose **Disabled**.</span></span>
4. <span data-ttu-id="5736c-116">Im Fenster **Postleitzahldienst-Auswahl** wählen Sie **GetAddress.io** aus.</span><span class="sxs-lookup"><span data-stu-id="5736c-116">In the **Postal code service selection** window, choose **GetAddress.io**.</span></span>
5. <span data-ttu-id="5736c-117">Im Fenster **GetAddress.io-Config** wählen Sie **API Schlüssel abrufen**, um die Seite **Pläne** auf der Website getAddress API zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5736c-117">In the **GetAddress.io Config** window, choose **Get API Key** to open the **Plans** page on the website for the getAddress API.</span></span>  

    > [!NOTE]  
>   <span data-ttu-id="5736c-118">Sie müssen möglicherweise Popups in Ihrem Browser ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="5736c-118">You might need to allow pop-ups in your browser.</span></span>
6. <span data-ttu-id="5736c-119">Kaufen einen Plan oder wählen Sie einfach **API Schlüssel abrufen** aus und erstellen Sie dann Ihre E-Mail-Adresse bereit.</span><span class="sxs-lookup"><span data-stu-id="5736c-119">Purchase a plan, or just choose **Get API Key**, and then provide your email address.</span></span>
7. <span data-ttu-id="5736c-120">Öffnen Sie die E-Mail aus getAddress.io und kopieren Sie den API-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="5736c-120">Open the email from getAddress.io, and copy the API key.</span></span> <span data-ttu-id="5736c-121">Der Schlüssel ist unter der Überschrift **Ihr API Schlüssel**.</span><span class="sxs-lookup"><span data-stu-id="5736c-121">The key is under the **Your API Key** heading.</span></span>
8. <span data-ttu-id="5736c-122">Im Fenster **GetAddress.io-Config** geben Sie den API-Schlüssel im Feld **API Schlüssel** ein, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="5736c-122">In the **GetAddress.io Config** window, paste the API key in the **API Key** field, and then choose **OK**.</span></span>
9. <span data-ttu-id="5736c-123">Auf der Seite **Dienstverbindungen** prüfen Sie, dass das Feld **Adressen-Anbieter** Feld **GetAddress.io** anzeigt.</span><span class="sxs-lookup"><span data-stu-id="5736c-123">In the **Service Connections** page, verify that the **Address Provider** field shows **GetAddress.io**.</span></span> <span data-ttu-id="5736c-124">Wenn dies so ist, ist der Dienst aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5736c-124">If it does, the service is enabled.</span></span>

## <a name="see-also"></a><span data-ttu-id="5736c-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5736c-125">See Also</span></span>
<span data-ttu-id="5736c-126">[" GetAddress.io Großbritannien](ui-extensions-getaddressio.md)
[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Mittels der Erweiterungen](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="5736c-126">[GetAddress.io UK Postcodes](ui-extensions-getaddressio.md)
[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="5736c-127">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5736c-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
