---
title: Rückgängigmachen von Objekte als Web Services verfügbar | Microsoft Docs
description: Veröffentlichen Sie Objekte als Web Services, um sie sofort für Ihre Business Central-Lösung bereitzustellen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 02/04/2020
ms.author: edupont
ms.openlocfilehash: 4e09df754895a8d0d3a1cc1ed84a7c8332e32880
ms.sourcegitcommit: 0cb8a646dcba8f6d6336ebd008587874d25f4629
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/07/2020
ms.locfileid: "3030244"
---
# <a name="publish-a-web-service"></a>Webdienst veröffentlichen

Webdienste sind eine einfache Art, Anwendungsfunktionen für eine Vielzahl von externen Systemen und Benutzern zugänglich zu machen. [!INCLUDE[d365fin](includes/d365fin_md.md)] enthält die Anzahl von Objekten, die als Webdienste standardmäßig gegenüber die Integration anderer Microsoft-Dienstleistungen bereitgestellt werden, Sie können weitere Web Services hinzufügen.  

Sie richten im Internet einen Webdienst ein im [!INCLUDE[d365fin](includes/d365fin_md.md)] Client. Sie müssen dann den Webdienst veröffentlichen, so dass er für Serviceanforderungen über das Netzwerk bereitsteht. Benutzer können Webdienste erkennen, indem Sie auf einen Browser auf den Computer verweisen, der ausführt und eine Liste der verfügbaren Services anfordern. Wenn Sie einen Webdienst veröffentlichen, ist er über das Netzwerk für authentifizierte Benutzer sofort verfügbar. Alle autorisierten Benutzer können auf Metadaten für Webdienste zugreifen, aber nur Benutzer mit ausreichenden -Berechtigungen können auf tatsächliche Daten zugreifen.

## <a name="creating-and-publishing-a-web-service"></a>Erstellen und Veröffentlichen eines Webdienstes  
Die folgenden Schritte erläutern, wie ein Webdienst erstellt und veröffentlicht wird.  

### <a name="to-create-and-publish-a-web-service"></a>So erstellen und veröffentlichen Sie einen Webdienst  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Webdienste** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie auf der Seite **Webdienste** **Neu** aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > **Codeunit** und **Seite** sind gültige Arten für SOAP-Webdienste. **Seite** und **Abfrage** sind gültige Arten für OData-Webdienste.  
    > Wenn die Datenbank mehrere Unternehmen enthält, können Sie eine Objekt-ID auswählen, die für eines der Unternehmen eindeutig ist.  
    > Der Dienstname ist für Nutzer Ihres Webdiensts sichtbar und wird zum Identifizieren und Unterscheiden von Webdiensten verwendet, Sie sollten daher einen aussagefähigen Namen wählen.

3. Aktivieren Sie das Kontrollkästchen in der Spalte **Veröffentlicht**.  

Wenn Sie den Webdienst veröffentlichen, sehen Sie in den Feldern **OData-URL** und **SOAP-URL** die URLs, die für den Webdienst erzeugt wurden. Sie können den Webdienst sofort testen, indem Sie die Links in den **OData-URL** und **SOAP-URL**-Feldern auswählen. Optional können Sie den Wert des Felds kopieren und ihn für die spätere Verwendung speichern.  

> [!IMPORTANT]
> Für Codeunits, die als SOAP-Webdienst veröffentlicht werden, müssen die Methoden, die in der Codeunit bereitgestellt werden, im Code als `[External]` markiert werden.

Nachdem Sie einen Webdienst veröffentlichen, ist er für externe Seiten verfügbar. Sie können die Verfügbarkeit dieses Webdienstes prüfen, indem Sie einen Browser verwenden, oder Sie können den Link in den **OData-URL** und **SOAP-URL** -Feldern auf der Seite **Webdienste** auswählen. Im folgenden Verfahren wird gezeigt, wie Sie die Verfügbarkeit des Webdienstes für die spätere Verwendung prüfen können.  

### <a name="to-verify-the-availability-of-a-web-service"></a>So prüfen Sie die Verfügbarkeit eines Webdienstes  

1. Geben Sie in Ihrem Browser die entsprechende URL ein. Die folgende Tabelle zeigt die Arten von URLs, die Sie für unterschiedliche Webservicearten eingeben können.  

    > [!div class="mx-tdBreakAll"]
    > |Typ|Syntax|Beispiel|
    > |----------------|------|-------|
    > |SOAP|https://api.businesscentral.dynamics.com/*Version*/*Mandant*/Produktion/WS/*CompanyName*/*Entität*/ |https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument|
    > |OData-V4|https://api.businesscentral.dynamics.com/*Version*/*Mandant*/Produktion/ODataV4/Unternehmen('*CompanyName*')/*Entität*|https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument<br/>    Das Feld „Unternehmensname“ berücksichtigt Groß-/Kleinschreibung.|

2. Überprüfen Sie die Informationen, die im Browser angezeigt werden. Vergewissern Sie sich, dass Sie den Namen des Webdienstes sehen, den Sie erstellt haben.  

Wenn Sie auf einen Webdienst zugreifen und Daten wieder auf [!INCLUDE[d365fin](includes/d365fin_md.md)] schreiben möchten, müssen Sie den Firmennamen angeben. Sie können den Mandanten als Teil des URI, wie in Beispielen angezeigt, angeben, oder Sie können den Mandanten als Teil der Abfrageparameter angeben. Beispielsweise verweisen die folgenden URIs auf denselben OData-Webdienst, und beide sind gültige URIs.  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a>Siehe auch

[Verwaltung](admin-setup-and-administration.md)  
[Business Central-Web Services für Entwickler](/dynamics365/business-central/dev-itpro/webservices/web-services)  
