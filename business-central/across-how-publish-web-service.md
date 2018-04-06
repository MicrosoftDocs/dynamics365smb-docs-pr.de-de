---
title: "Rückgängigmachen von Objekte als Web Services verfügbar | Microsoft Docs"
description: "Wenn Sie Objekte als Webdienste veröffentlichen, stehen sie sofort auf dem Netzwerk zur Verfügung."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/22/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 3b2e2dcd7e52aaf9d347f5d20210bc4cf18cd864
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="publish-a-web-service"></a>Webdienst veröffentlichen
Webdienste sind eine einfache Art, Anwendungsfunktionen für eine Vielzahl von externen Systemen und Benutzern zugänglich zu machen. [!INCLUDE[d365fin](includes/d365fin_md.md)] enthält die Anzahl von Objekten, die als Webdienste standardmäßig gegenüber die Integration anderer Microsoft-Dienstleistungen bereitgestellt werden, Sie können weitere Web Services hinzufügen.  

Sie können einen Webdienst im Windows-Client oder im Webclienten einrichten. Sie müssen dann den Webdienst veröffentlichen, so dass er für Serviceanforderungen über das Netzwerk bereitsteht. Benutzer können Webdienste erkennen, indem Sie auf einen Browser auf den Computer verweisen, der ausführt und eine Liste der verfügbaren Services anfordern. Wenn Sie einen Webdienst veröffentlichen, ist er über das Netzwerk für authentifizierte Benutzer sofort verfügbar. Alle autorisierten Benutzer können auf Metadaten für Webdienste zugreifen, aber nur Benutzer mit ausreichenden -Berechtigungen können auf tatsächliche Daten zugreifen.

## <a name="creating-and-publishing-a-web-service"></a>Erstellen und Veröffentlichen eines Webdienstes  
Die folgenden Schritte erläutern, wie ein Webdienst erstellt und veröffentlicht wird.  

### <a name="to-create-and-publish-a-web-service"></a>So erstellen und veröffentlichen Sie einen Webdienst  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht](media/ui-search/search_small.png "Nach Seite oder Bericht suche") und geben **Internetquellen** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie auf der Seite **Webdienste** **Neu** aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    >  **Codeunit** und **Seite** sind gültige Arten für SOAP-Webdienste. **Seite** und **Abfrage** sind gültige Arten für OData-Webdienste.  
    Wenn die Datenbank mehrere Unternehmen enthält, können Sie eine Objekt-ID auswählen, die für eines der Unternehmen eindeutig ist.  
    Der Dienstname ist für Nutzer Ihres Webdiensts sichtbar und wird zum Identifizieren und Unterscheiden von Webdiensten verwendet, Sie sollten daher einen aussagefähigen Namen wählen.

3.  Aktivieren Sie das Kontrollkästchen in der Spalte **Veröffentlicht**.  

Wenn Sie den Webdienst veröffentlichen, sehen Sie in den Feldern **OData-URL** und **SOAP-URL** die URLs, die für den Webdienst erzeugt wurden. Sie können den Webdienst sofort testen, indem Sie die Links in den **OData-URL** und **SOAP-URL**-Feldern auswählen. Optional können Sie den Wert des Felds kopieren und ihn für die spätere Verwendung speichern.  

Nachdem Sie einen Webdienst veröffentlichen, ist er für externe Seiten verfügbar. Sie können die Verfügbarkeit dieses Webdienstes prüfen, indem Sie einen Browser verwenden, oder Sie können den Link in den **OData-URL** und **SOAP-URL** -Feldern im Fenster **Webdienste** auswählen. Im folgenden Verfahren wird gezeigt, wie Sie die Verfügbarkeit des Webdienstes für die spätere Verwendung prüfen können.  

### <a name="to-verify-the-availability-of-a-web-service"></a>So prüfen Sie die Verfügbarkeit eines Webdienstes  

1.  Geben Sie in Ihrem Browser die entsprechende URL ein. Die folgende Tabelle zeigt die Arten von URLs, die Sie für unterschiedliche Webservicearten eingeben können.  
> [!div class="mx-tdBreakAll"]
> |Typ|Syntax|Beispiel|
> |----------------|------|-------|
> |SOAP |https://*Server*:*SOAPWebServicePort*/*ServerInstance*/WS/*CompanyName*/salesDocuments/ |https://mycompany.financials.dynamics.com:7047/MS/WS/MyCompany/Page/salesDocuments?tenant=mycompany.financials.dynamics.com |
> |OData |https://*Server*:*ODataWebServicePort*/*ServerInstance*/OData/Company('*CompanyName*')|[https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com](https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com) <br />    Das Feld „Unternehmensname“ berücksichtigt Groß-/Kleinschreibung.|

2.  Überprüfen Sie die Informationen, die im Browser angezeigt werden. Vergewissern Sie sich, dass Sie den Namen des Webdienstes sehen, den Sie erstellt haben.  

Wenn Sie auf einen Webdienst zugreifen und Daten wieder auf [!INCLUDE[d365fin](includes/d365fin_md.md)] schreiben möchten, müssen Sie den Firmennamen angeben. Sie können den Mandanten als Teil des URI, wie in Beispielen angezeigt, angeben, oder Sie können den Mandanten als Teil der Abfrageparameter angeben. Beispielsweise verweisen die folgenden URIs auf denselben OData-Webdienst, und beide sind gültige URIs.  

```  
https://localhost:7048/server/OData/Company('CRONUS International Ltd.')/Customer  
```  

```  
https://localhost:7048/server/OData/Customer?company='CRONUS International Ltd.'  
```  

## <a name="see-also"></a>Siehe auch  
[Einrichtung und Verwaltung](admin-setup-and-administration.md)  

