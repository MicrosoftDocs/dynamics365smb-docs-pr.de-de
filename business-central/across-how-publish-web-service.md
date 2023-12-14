---
title: Objekte als Webdienste verfügbar machen
description: 'Veröffentlichen Sie Objekte als Web Services, um sie sofort für Ihre Business Central-Lösung bereitzustellen.'
author: brentholtorf
ms.topic: conceptual
ms.search.form: 810
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="publish-a-web-service"></a>Webdienst veröffentlichen

Webdienste sind eine einfache Art, Anwendungsfunktionen für verschiedene externe Systeme und Benutzer zugänglich zu machen. Standardmäßig stellt [!INCLUDE[prod_short](includes/prod_short.md)] eine Reihe von Objekten als Webdienste bereit, um eine bessere Integration in andere Microsoft-Dienste zu ermöglichen. Sie können bei Bedarf weitere Webdienste hinzufügen.  

Richten Sie einen Webdienst in [!INCLUDE[prod_short](includes/prod_short.md)] ein, und veröffentlichen Sie den Webdienst anschließend, damit er authentifizierten Benutzern zur Verfügung steht. Alle autorisierten Benutzer können auf Metadaten für Webdienste zugreifen, aber nur Benutzer mit ausreichenden -Berechtigungen können auf tatsächliche Daten zugreifen.  

## <a name="creating-and-publishing-a-web-service"></a>Erstellen und Veröffentlichen eines Webdienstes

Die folgenden Schritte erläutern, wie ein Webdienst erstellt und veröffentlicht wird.  

### <a name="to-create-and-publish-a-web-service"></a>So erstellen und veröffentlichen Sie einen Webdienst

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Webdienste** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie auf der Seite **Webdienste** **Neu** aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > **Codeunit** und **Seite** sind gültige Arten für SOAP-Webdienste. **Seite** und **Abfrage** sind gültige Arten für OData-Webdienste. Ab Version 16.3 ist **Codeunit** ebenfalls ein gültiger Typ für OData v4-Webdienste, es wird jedoch keine URL in der Benutzeroberfläche angezeigt. Wenn die Datenbank mehrere Unternehmen enthält, können Sie eine Objekt-ID auswählen, die für eines der Unternehmen eindeutig ist.  
    > Der Dienstname ist für Nutzer Ihres Webdiensts sichtbar und wird zum Identifizieren und Unterscheiden von Webdiensten verwendet, Sie sollten daher einen aussagefähigen Namen wählen.

3. Aktivieren Sie das Kontrollkästchen in der Spalte **Veröffentlicht**.  

Wenn Sie den Webdienst veröffentlichen, werden die neuen URLs in den Feldern **OData-URL** und **SOAP-URL** angezeigt. Bei Codeunits, die als ungebundene OData v4-Aktionen verfügbar gemacht werden, werden die URL-Felder jedoch nicht angezeigt.  

Sie können den Webdienst sofort testen, indem Sie die Links in den **OData-URL** und **SOAP-URL**-Feldern auswählen. Optional können Sie den Wert des Felds kopieren und ihn für die spätere Verwendung speichern. Befolgen Sie die Anweisungen im Abschnitt [Überprüfen der Verfügbarkeit eines Webdiensts](/dynamics365/business-central/dev-itpro/developer/devenv-creating-and-interacting-with-odatav4-unbound-action#verifying-web-service-availability) im Inhalt für Entwickler, um Codeunits zu testen, die als ungebundene OData v4-Aktionen verfügbar gemacht werden.

> [!NOTE]
> Wenn die als Webdienste bereitgestellten Objekt nicht online über [!INCLUDE[prod_short](includes/prod_short.md)] aufgerufen werden dürfen, müssen Sie die im Code verfügbaren Methoden als `[Scope('OnPrem')]` markieren. Weitere Informationen finden Sie unter [Bereichsattribut ](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).

Nachdem Sie einen Webdienst veröffentlichen, ist er für externe Seiten verfügbar. Sie können die Verfügbarkeit dieses Webdiensts prüfen, indem Sie einen Browser verwenden, oder Sie können den Link in den Feldern **OData-URL** und **SOAP-URL** auf der Seite **Webdienste** auswählen. Im folgenden Verfahren wird gezeigt, wie Sie die Verfügbarkeit des Webdienstes für die spätere Verwendung prüfen können.  

### <a name="to-verify-the-availability-of-a-web-service"></a>So prüfen Sie die Verfügbarkeit eines Webdienstes

1. Geben Sie in Ihrem Browser die entsprechende URL ein. Die folgende Tabelle zeigt die Arten von URLs, die Sie für unterschiedliche Webservicearten eingeben können.  

    > [!div class="mx-tdBreakAll"]
    > |Typ|Syntax|Beispiel|
    > |----------------|------|-------|
    > |SOAP|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/` |`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument`|
    > |OData-V4|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*`|`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument`<br/>    Das Feld „Unternehmensname“ berücksichtigt Groß-/Kleinschreibung.|

2. Überprüfen Sie die Informationen, die im Browser angezeigt werden. Vergewissern Sie sich, dass Sie den Namen des Webdienstes sehen, den Sie erstellt haben.  

Wenn Sie auf einen Webdienst zugreifen und Daten wieder auf [!INCLUDE[prod_short](includes/prod_short.md)] schreiben möchten, müssen Sie den Firmennamen angeben. Sie können das Unternehmen als Teil des URI, wie in Beispielen angezeigt, angeben, oder Sie können das Unternehmen als Teil der Abfrageparameter angeben. Beispielsweise verweisen die folgenden URIs auf denselben OData-Webdienst, und beide sind gültige URIs.  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a>Siehe auch

[Verwaltung](admin-setup-and-administration.md)  
[Business Central-Web Services für Entwickler](/dynamics365/business-central/dev-itpro/webservices/web-services)  
[OData-Anforderungslimits](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#ODataServices)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
