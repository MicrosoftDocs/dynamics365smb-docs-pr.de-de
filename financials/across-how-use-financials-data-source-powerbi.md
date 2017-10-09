---
title: Eine Power BI Datenquelle mit Financials erstellen| Microsoft Docs
description: "Sie können Ihre Daten in Financials als Datenquelle in Power BI bereitstellen und leistungsstarke Berichte über den Zustand des Geschäftes erstellen."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 06/06/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 3f98a08415a896c37868bf0ed5efd9314d5ab07a
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="using-included365finincludesd365finmdmd-as-a-power-bi-data-source"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)] als Power BI Datenquelle nutzen
Sie können Ihre [!INCLUDE[d365fin](includes/d365fin_md.md)] Daten zur Verfügung stellen als Datenquelle in Power BI und leistungsstarke Berichte über den Zustand des Geschäftes erstellen.  

> [!NOTE]  
>   Sie müssen ein gültiges Konto mit  [!INCLUDE[d365fin](includes/d365fin_md.md)]mit Power BI haben. Zudem müssen Sie [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) herunterladen.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-power-bi-desktop"></a>Um [!INCLUDE[d365fin](includes/d365fin_md.md)] als Datenquelle in Power BI Desktop hinzufügen
1. In Power BI Desktop im linken Navigationsbereich, wählen Sie **Daten abrufen** aus.
2. Im Fenster **Daten abrufen** wählen Sie **Onlinedienste** aus, wählen Sie **Dynamics 365 for Financials** und dann die Schaltfläche **Verbinden** aus.

   Power Bi zeigt einen Assistenten an, der Sie durch den Verbindungsvorgang führt. Der erste Schritt besteht darin, OData URL und den Mandanten einzugeben, der mit dem Sachkonto [!INCLUDE[d365fin](includes/d365fin_md.md)] verknüpft ist.  

   Für *OData-URL* können Sie das OData V4 URL eines der Web Services, der in **Webdienste** auf der Seite angezeigt wird in [!INCLUDE[d365fin](includes/d365fin_md.md)] kopieren, beispielsweise `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.  

   Für den *Unternehmensname* verwenden Sie den Namen, der im Feld **Name** im Fenster **Firmendaten** in [!INCLUDE[d365fin](includes/d365fin_md.md)] angezeigt wird. Wenn Ihr [!INCLUDE[d365fin](includes/d365fin_md.md)] mehrere Unternehmen enthält, wählen Sie den entsprechenden Namen aus der Liste im Fenster **Unternehmen** aus. In beiden Fällen prüfen Sie, ob dem Namen, den Sie im Power BI Assistenten angeben, genau dem Text entspricht, der angezeigt wird in [!INCLUDE[d365fin](includes/d365fin_md.md)], wie z. B. `My Company`
3. Nachdem Sie die Informationen eingegeben haben, wählen Sie die Schaltfläche OK. Der nächste Schritt im Assistenten ist es, den Benutzernamen und das Kennwort einzugeben.

   > [!NOTE]  
>    Wenn es andere Authentifizierungsoptionen gibt, die in der linken Handnavigation verfügbar sind, wählen Sie *Standard* aus.
4. Geben Sie den Benutzernamen und da Kennwort an. Sie finden diese Informationen im Fenster **Benutzer** in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Verwenden Sie **Internet-Tastenkombination** als Ihr Kennwort.

   Beispielsweise ist der Benutzername *ADMINISTRATOR* und die Webdiensttastenkombination, die als Passwort dient *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*.
5. Klicken Sie auf die Schaltfläche **Verbinden** zum Fortfahren. Der Power BI Assistent zeigt eine Liste der [!INCLUDE[d365fin](includes/d365fin_md.md)] Datenquellen an. Diese Datenquelle ist für alle Webdienste, die Sie von [!INCLUDE[d365fin](includes/d365fin_md.md)] veröffentlicht haben.

   Sie können einen neuen Webdienst URL in [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellen, indem Sie die **Erstellen Dataset** Aktion der Seite **Webdienste** nutzen, indem Sie die unterstütze Hilfe **Bericht einrichten** verwenden oder die Aktion **Bearbeiten in Excel** in einer beliebigen Liste wählen.

6. Geben Sie die Daten an, die Sie Ihrem Datenmodell hinzufügen möchten, und wählen Sie dann die Schaltfläche **Laden** aus.
7. Wiederholen Sie die vorherigen Schritte, um zusätzliche [!INCLUDE[d365fin](includes/d365fin_md.md)] Daten Ihrem Power BI Datenmodell hinzuzufügen.

   > [!NOTE]  
>    Sobald Sie sich erfolgreich verbunden haben mit [!INCLUDE[d365fin](includes/d365fin_md.md)] werden Sie nicht erneut nach OData URL, Benutzername oder Kennwort gefragt.

Sobald die Daten geladen sind, erscheinen Sie in der rechten Navigation auf der Seite. Zu diesem Zeitpunkt haben Sie erfolgreich Ihre Dynamics 365 Daten verbunden und sind bereit, Ihren Power BI Bericht zu erstellen. Weitere Informationen finden Sie in der [Power BI Dokumentation](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).

## <a name="see-also"></a>Siehe auch
[Business Intelligence](bi.md)  
[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](upload-data.md)  
[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzen](finance.md)  

