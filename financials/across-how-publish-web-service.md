---
title: "Rückgängigmachen von Objekte als Web Services verfügbar | Microsoft Docs"
description: "Sie Veröffentlichen  [!INCLUDE[d365fin](includes/d365fin_md.md)] Objekte als Webdienste, und sind  sofort im Netzwerk verfügbar."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 278515fc479a72957fb52dad71ce2f98d354ee32
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-publish-a-web-service"></a><span data-ttu-id="5c6c0-103">Vorgehensweise: Veröffentlichen eines Webdiensts</span><span class="sxs-lookup"><span data-stu-id="5c6c0-103">How to: Publish a Web Service</span></span>
<span data-ttu-id="5c6c0-104">Webdienste sind eine einfache Art, Anwendungsfunktionen für eine Vielzahl von externen Systemen und Benutzern zugänglich zu machen.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-104">Web services are a lightweight way to make application functionality available to a variety of external systems and users.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="5c6c0-105"> enthält die Anzahl von Objekten, die als Webdienste standardmäßig gegenüber die Integration anderer Microsoft-Dienstleistungen bereitgestellt werden, Sie können weitere Web Services hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-105"> includes an number of objects that are exposed as web services by default due to integration with other Microsoft services, but you can also add other web services.</span></span>  

<span data-ttu-id="5c6c0-106">Sie können einen Webdienst im Windows-Client oder im Webclienten einrichten.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-106">You can set up a web service in the Windows client or in the Web client.</span></span> <span data-ttu-id="5c6c0-107">Sie müssen dann den Webdienst veröffentlichen, so dass er für Serviceanforderungen über das Netzwerk bereitsteht.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-107">You must then publish the web service so that it is available to service requests over the network.</span></span> <span data-ttu-id="5c6c0-108">Benutzer können Webdienste erkennen, indem Sie auf einen Browser auf den Computer verweisen, der  ausführt und eine Liste der verfügbaren Services anfordern.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-108">Users can discover web services by pointing a browser at the server location and requesting a list of available services.</span></span> <span data-ttu-id="5c6c0-109">Wenn Sie einen Webdienst veröffentlichen, ist er über das Netzwerk für authentifizierte Benutzer sofort verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-109">When you publish a web service, it is immediately available over the network for authenticated users.</span></span> <span data-ttu-id="5c6c0-110">Alle autorisierten Benutzer können auf Metadaten für Webdienste zugreifen, aber nur Benutzer mit ausreichenden -Berechtigungen können auf tatsächliche Daten zugreifen.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-110">All authorized users can access metadata for web services, but only users who have sufficient permissions can access actual data.</span></span>

## <a name="creating-and-publishing-a-web-service"></a><span data-ttu-id="5c6c0-111">Erstellen und Veröffentlichen eines Webdienstes</span><span class="sxs-lookup"><span data-stu-id="5c6c0-111">Creating and Publishing a Web Service</span></span>  
 <span data-ttu-id="5c6c0-112">Die folgenden Schritte erläutern, wie ein Webdienst erstellt und veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-112">The following steps explain how to create and publish a web service.</span></span>  

#### <a name="to-create-and-publish-a-web-service"></a><span data-ttu-id="5c6c0-113">So erstellen und veröffentlichen Sie einen Webdienst</span><span class="sxs-lookup"><span data-stu-id="5c6c0-113">To create and publish a web service</span></span>  

1.  <span data-ttu-id="5c6c0-114">Wählen Sie das Symbol ![Nach Seite oder Bericht] (media/ui-search/search_small.png "Nach Seite oder Bericht suche") und geben **Internetquellen** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Web Services**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="5c6c0-115">Wählen Sie auf der Seite **Webdienste** **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-115">In the **Web Services** page, choose **New**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    >  <span data-ttu-id="5c6c0-116">**Codeunit** und **Seite** sind gültige Arten für SOAP-Webdienste.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-116">**Codeunit** and **Page** are valid types for SOAP web services.</span></span> <span data-ttu-id="5c6c0-117">**Seite** und **Abfrage** sind gültige Arten für OData-Webdienste.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-117">**Page** and **Query** are valid types for OData web services.</span></span>  
    <span data-ttu-id="5c6c0-118">Wenn die Datenbank mehrere Unternehmen enthält, können Sie eine Objekt-ID auswählen, die für eines der Unternehmen eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-118">Also, if the database contains multiple companies, you can choose an object ID that is specific to one of the companies.</span></span>  
    <span data-ttu-id="5c6c0-119">Der Dienstname ist für Nutzer Ihres Webdiensts sichtbar und wird zum Identifizieren und Unterscheiden von Webdiensten verwendet, Sie sollten daher einen aussagefähigen Namen wählen.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-119">Finally, the service name is visible to consumers of your web service and is the basis for identifying and distinguishing web services, so you should make the name meaningful.</span></span>

3.  <span data-ttu-id="5c6c0-120">Aktivieren Sie das Kontrollkästchen in der Spalte **Veröffentlicht**.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-120">Select the check box in the **Published** column.</span></span>  

     <span data-ttu-id="5c6c0-121">Wenn Sie den Webdienst veröffentlichen, sehen Sie in den Feldern **OData-URL** und **SOAP-URL** die URLs, die für den Webdienst erzeugt wurden.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-121">When you publish the web service, in the **OData URL** and **SOAP URL** fields, you can see the URLs that are generated for the web service.</span></span> <span data-ttu-id="5c6c0-122">Sie können den Webdienst sofort testen, indem Sie die Links in den **OData-URL** und **SOAP-URL**-Feldern auswählen.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-122">You can test the web service immediately by choosing the links in the **OData URL** and **SOAP URL** fields.</span></span> <span data-ttu-id="5c6c0-123">Optional können Sie den Wert des Felds kopieren und ihn für die spätere Verwendung speichern.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-123">Optionally, you can copy the value of the field and save it for later use.</span></span>  

<span data-ttu-id="5c6c0-124">Nachdem Sie einen Webdienst veröffentlichen, ist er für externe Seiten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-124">After you publish a web service, it is available to external parties.</span></span> <span data-ttu-id="5c6c0-125">Sie können die Verfügbarkeit dieses Webdienstes prüfen, indem Sie einen Browser verwenden, oder Sie können den Link in den **OData-URL** und **SOAP-URL** -Feldern im Fenster **Webdienste** auswählen.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-125">You can verify the availability of that web service by using a browser, or you can choose the link in the **OData URL** and **SOAP URL** fields in the **Web Services** window.</span></span> <span data-ttu-id="5c6c0-126">Im folgenden Verfahren wird gezeigt, wie Sie die Verfügbarkeit des Webdienstes für die spätere Verwendung prüfen können.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-126">The following procedure illustrates how you can verify the availability of the web service for later use.</span></span>  

#### <a name="to-verify-the-availability-of-a-web-service"></a><span data-ttu-id="5c6c0-127">So prüfen Sie die Verfügbarkeit eines Webdienstes</span><span class="sxs-lookup"><span data-stu-id="5c6c0-127">To verify the availability of a web service</span></span>  

1.  <span data-ttu-id="5c6c0-128">Geben Sie in Ihrem Browser die entsprechende URL ein.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-128">In your browser, enter the relevant URL.</span></span> <span data-ttu-id="5c6c0-129">Die folgende Tabelle zeigt die Arten von URLs, die Sie eingeben können.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-129">The following table illustrates the types of URLs that you can enter.</span></span> <span data-ttu-id="5c6c0-130">Für SOAP-Webdienste verwenden Sie das folgende Format für Ihr URI.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-130">For SOAP web services, use the following format for your URI.</span></span>  

    <table>
    <tr>
    <th><span data-ttu-id="5c6c0-131">Webdiensttyp</span><span class="sxs-lookup"><span data-stu-id="5c6c0-131">Web service type</span></span></th>
    <th><span data-ttu-id="5c6c0-132">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c6c0-132">Syntax</span></span></th>
    <th><span data-ttu-id="5c6c0-133">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5c6c0-133">Example</span></span></th>
    </tr>
    <tr>
    <td><span data-ttu-id="5c6c0-134">SOAP</span><span class="sxs-lookup"><span data-stu-id="5c6c0-134">SOAP</span></span></td>
    <td><span data-ttu-id="5c6c0-135">https://*Server*:*SOAPWebServicePort*/*ServerInstance*/WS/*CompanyName*/salesDocuments/</span><span class="sxs-lookup"><span data-stu-id="5c6c0-135">https://*Server*:*SOAPWebServicePort*/*ServerInstance*/WS/*CompanyName*/salesDocuments/</span></span></td>
    <td><span data-ttu-id="5c6c0-136">https://mycompany.financials.dynamics.com:7047/MS/WS/MyCompany/Page/salesDocuments?tenant=mycompany.financials.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="5c6c0-136">https://mycompany.financials.dynamics.com:7047/MS/WS/MyCompany/Page/salesDocuments?tenant=mycompany.financials.dynamics.com</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="5c6c0-137">OData</span><span class="sxs-lookup"><span data-stu-id="5c6c0-137">OData</span></span></td>
    <td><span data-ttu-id="5c6c0-138">https://*Server*:*ODataWebServicePort*/*ServerInstance*/OData/Company('*CompanyName*')</span><span class="sxs-lookup"><span data-stu-id="5c6c0-138">https://*Server*:*ODataWebServicePort*/*ServerInstance*/OData/Company('*CompanyName*')</span></span></td>
    <td><span data-ttu-id="5c6c0-139">https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="5c6c0-139">https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com</span></span>

         The company name is case-sensitive.</td>
    </tr>
    </table>

2.  <span data-ttu-id="5c6c0-140">Überprüfen Sie die Informationen, die im Browser angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-140">Review the information that is displayed in the browser.</span></span> <span data-ttu-id="5c6c0-141">Vergewissern Sie sich, dass Sie den Namen des Webdienstes sehen, den Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-141">Verify that you can see the name of the web service that you have created.</span></span>  

 <span data-ttu-id="5c6c0-142">Wenn Sie auf einen Webdienst zugreifen und Daten wieder auf [!INCLUDE[d365fin](includes/d365fin_md.md)] schreiben möchten, müssen Sie den Firmennamen angeben.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-142">When you access a web service, and you want to write data back to [!INCLUDE[d365fin](includes/d365fin_md.md)], you must specify the company name.</span></span> <span data-ttu-id="5c6c0-143">Sie können den Mandanten als Teil des URI, wie in Beispielen angezeigt, angeben, oder Sie können den Mandanten als Teil der Abfrageparameter angeben.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-143">You can specify the company as part of the URI as shown in the examples, or you can specify the company as part of the query parameters.</span></span> <span data-ttu-id="5c6c0-144">Beispielsweise verweisen die folgenden URIs auf denselben OData-Webdienst, und beide sind gültige URIs.</span><span class="sxs-lookup"><span data-stu-id="5c6c0-144">For example, the following URIs point to the same OData web service and are both valid URIs.</span></span>  

```  
https://localhost:7048/server/OData/Company('CRONUS International Ltd.')/Customer  
```  

```  
https://localhost:7048/server/OData/Customer?company='CRONUS International Ltd.'  
```  

## <a name="see-also"></a><span data-ttu-id="5c6c0-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c6c0-145">See Also</span></span>  
[<span data-ttu-id="5c6c0-146">Verwaltung in Dynamics 365 for Financials einrichten</span><span class="sxs-lookup"><span data-stu-id="5c6c0-146">Setup and Administration in Dynamics 365 for Financials</span></span>](admin-setup-and-administration.md)  

