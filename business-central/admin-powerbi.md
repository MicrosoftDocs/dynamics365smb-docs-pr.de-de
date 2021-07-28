---
title: Einführung in Business Central und Power BI | Microsoft Docs
description: Sie erhalten eine Übersicht der Verwendung von Power BI, um Erkenntnisse, Business Intelligence und KPIs aus Ihren Business Central-Daten zu erhalten.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 3c8ad52667ad8ff0a2cb399ac6354012d7ef9275
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6437912"
---
# <a name="prod_short-and-power-bi"></a>[!INCLUDE[prod_short](includes/prod_short.md)] und Power BI

Einblicke in Ihre [!INCLUDE[prod_short](includes/prod_short.md)]-Daten sind mit [Power BI](https://powerbi.microsoft.com), einem Datenvisualisierungssystem von Microsoft, kein Problem. Power BI ruft [!INCLUDE[prod_short](includes/prod_short.md)]-Daten ab, damit Sie mit diesen Daten Dashboards und Berichte erstellen können. Power BI stellt eine flexible Alternative zu den in [!INCLUDE[prod_short](includes/prod_short.md)] integrierten Berichten dar, mit der Sie einen Drilldown durchführen und die Visualisierung anpassen können. Sie können in [!INCLUDE[prod_short](includes/prod_short.md)] sogar die Daten verschiedener Unternehmen zusammenführen. Manche Power BI-Berichte können auch in Business Central eingebettet und angezeigt werden, ohne das System zu verlassen. Komplexere Dashboards bieten auf der Power BI-Webseite eine bessere Erfahrung.

![Power BI und Business Central.](media/power-bi-intro.png)

## <a name="what-you-can-do-with-power-bi-and-prod_short"></a>Möglichkeiten von Power BI und [!INCLUDE[prod_short](includes/prod_short.md)]

Bei der Arbeit mit [!INCLUDE[prod_short](includes/prod_short.md)] und Power BI stehen Ihnen verschiedene Funktionen zur Verfügung. Manche Dinge werden über Power BI ausgeführt, andere über [!INCLUDE[prod_short](includes/prod_short.md)]. Außerdem sind einige Funktionen nur mit [!INCLUDE[prod_short](includes/prod_short.md)] online verfügbar und nicht mit on-premises. Die folgende Tabelle verschafft Ihnen einen Überblick.

|Funktion|Beschreibung|Online|On-premises|Weitere Informationen|
|-------|-----------|--------------|-----------|----------------|
|Zeigen Sie [!INCLUDE[prod_short](includes/prod_short.md)]-Daten in Power BI an.|Sie können Ihre Daten aus [!INCLUDE[prod_short](includes/prod_short.md)] in Berichten in Power BI anzeigen. [!INCLUDE[prod_short](includes/prod_short.md)] online umfasst einige vordefinierte Power BI-Berichte. Oder möglicherweise hat Ihre Organisation einige benutzerdefinierte Berichte für Sie zur Verfügung gestellt.|![Funktioniert online.](media/check.png)|![Funktioniert lokal](media/check.png)|[Siehe ...](across-working-with-business-central-in-powerbi.md)|
|Zeigen Sie Power BI-Berichte im [!INCLUDE[prod_short](includes/prod_short.md)]-Client an.| Power BI-Berichte, die [!INCLUDE[prod_short](includes/prod_short.md)]-Daten anzeigen, können direkt in Teile von [!INCLUDE[prod_short](includes/prod_short.md)]-Seiten eingebettet werden. Sie können in diesem Teil jeden beliebigen Bericht anzeigen, der Ihnen zur Verfügung steht. |![Funktioniert online.](media/check.png)|![Funktioniert lokal](media/check.png)<sup>[*](#onprem)</sup>|[Siehe ...](across-working-with-powerbi.md).|
|Erstellen Sie Berichte und Dashboards in Power BI, die [!INCLUDE[prod_short](includes/prod_short.md)]-Daten anzeigen.|Verwenden Sie Power BI Desktop, um eigene Berichte und Dashboards zu erstellen. Sie können die Berichte in Ihrem eigenen Power BI-Dienst veröffentlichen oder sie mit anderen Personen innerhalb ihrer Organisation teilen.|![Funktioniert online.](media/check.png)|![Funktioniert lokal](media/check.png)|[Siehe ...](across-how-use-financials-data-source-powerbi.md)
|[!INCLUDE[prod_short](includes/prod_short.md)]-Apps in Power BI| [!INCLUDE[prod_short](includes/prod_short.md)] veröffentlicht drei Apps für Power BI auf Microsoft AppSource. Diese Apps erstellen detaillierte Berichte und Dashboards in Ihrem Power BI-Dienst zum Anzeigen von [!INCLUDE[prod_short](includes/prod_short.md)]-Daten. Zu den verfügbaren Apps gehören: <ul><li>[!INCLUDE [prod_long](includes/prod_long.md)] – CRM </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] – Finance </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] – Sales </li></ul>  |![Funktioniert online.](media/check.png)||[Siehe ...](across-powerbi-business-central-apps.md)

<a name="onprem"><sup>*</sup></a> Für diese Funktion ist eine registrierte Anwendung für Business Central in Microsoft Azure erforderlich. Weitere Informationen finden Sie unter [Registrieren von Business Central On-Premises in Azure AD zur Integration mit anderen Diensten](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

## <a name="getting-ready-to-use-power-bi"></a>Vorbereitung auf die Verwendung von Power BI

Es gibt einige Aufgaben, die vor der Verwendung von Power BI mit [!INCLUDE[prod_short](includes/prod_short.md)] erledigt werden müssen. <!-- Some of the tasks are typically only done by administrators or super users.--> Die Aufgaben hängen von Ihrer Rolle in Ihrer Organisation ab und davon, was Sie mit Power BI machen wollen:

- Als *Business-Benutzer* möchten Sie Power BI-Berichte anzeigen, entweder im Power BI-Dienst oder in Business Central
- Als *Administrator* sind Sie für die Verwaltung der organisationsweiten Einstellungen verantwortlich, die festlegen, wie Business Central und Power BI arbeiten.
- Als *Berichtersteller* möchten Sie angepasste Power BI-Berichte erstellen, die Sie mit anderen Benutzern teilen können.

|Aufgabe|Geschäftsbenutzer|Administrator|Berichtsersteller|Weitere Informationen|
|----|-------------|-------------|-----------------------|----------------|
|Erstellen Sie ein Power BI-Konto.|![noch ein Häkchen.](media/check.png)|![noch ein Häkchen](media/check.png)|![wieder ein Häkchen](media/check.png)|Gehen Sie zu [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Verwenden Sie bei der Registrierung für ein Konto Ihre geschäftliche E-Mail-Adresse und Ihr zugehöriges Kennwort. <br /><br/>Für die Anmeldung benötigen Sie eine Lizenz, aber in den meisten Fällen sollten Sie bereits eine kostenlose Lizenz besitzen. Weitere Informationen finden Sie unter [Power BI Lizenzierung](admin-powerbi-setup.md#license).|
|GET Power BI Desktop|||![wieder ein Häkchen.](media/check.png)|Zum Herunterladen gehen Sie zu [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Weitere Informationen finden Sie unter [Power BI Desktop beziehen](/power-bi/fundamentals/desktop-get-the-desktop).
|Stellen Sie Business Central-Daten auf Power BI||![ein Häkchen.](media/check.png)|![wieder ein Häkchen](media/check.png)|[Daten über API-Seiten oder OData-Webdienste exponieren](admin-powerbi-setup.md#exposedata)
|Aktivieren Sie die Power BI-Integration<br />(nur vor Ort)||![ein Häkchen.](media/check.png)||[Business Central lokal für die Power BI-Integration festlegen](admin-powerbi-setup.md#setup)|


<!--



1. If you're using [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, make sure your deployment meets the requirements outlined in [Set up [!INCLUDE[prod_short](includes/prod_short.md)] on-premises for Power BI integration](admin-powerbi-setup.md#setup). This task is typically an administrative task.

2. Expose Business Central data through API pages or published web services.

    Business Central online automatically included several pages as APIs. For more information, see [Business Central API V2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/). Application developers for Business Central online can create custom API pages that you can then consume in reports. For more information, see [Developing a Custom API](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api).

   Codeunit, page, and query objects can be published as OData web services. There are many web services published by default. An easy way to find the web services is to search for *web services* in [!INCLUDE[prod_short](includes/prod_short.md)]. For more information about publishing web services, see [Publish a Web Service](across-how-publish-web-service.md).

3. Get a Power BI account.

   To do anything with Power BI and [!INCLUDE[prod_short](includes/prod_short.md)], whether you're an administrator or just a consumer, you'll need Power BI service account. To get an account, go to [https://powerbi.microsoft.com](https://powerbi.microsoft.com). To sign up for an account, use your work email address and password. Sign-up requires that you have a license, but in most cases you should already have a free license. For more information, see [Power BI Licensing](admin-powerbi-setup.md#license).

4. If you want to create your own Power BI reports, get Power BI Desktop.

   You can download [Power BI Desktop](https://powerbi.microsoft.com/desktop/). For more information, see [Get Power BI Desktop](/power-bi/fundamentals/desktop-get-the-desktop).

-->

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Weitere Informationen

[Power BI für Verbraucher](/power-bi/consumer/end-user-consumer)  
[Der „neue Look“ des Power BI Service](/power-bi/service-new-look)  
[Schnellstart: Stellen Sie eine Verbindung zu Daten her in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI Dokumentation](/power-bi/)  
[Business Intelligence](bi.md)  
[Vorbereitung für die Geschäftstätigkeit](ui-get-ready-business.md)  
[Importieren von Geschäftsdaten aus anderen Finanzsystemen](across-import-data-configuration-packages.md)  
[Einrichten [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Verwenden von [!INCLUDE[prod_short](includes/prod_short.md)] als Power BI-Datenquelle](across-how-use-financials-data-source-powerbi.md)  
[Verwenden von [!INCLUDE[prod_short](includes/prod_short.md)] als Power Apps-Datenquelle](across-how-use-financials-data-source-powerapps.md)  
[Verwenden von [!INCLUDE[prod_short](includes/prod_short.md)] in Power Automate](across-how-use-financials-data-source-flow.md)  




[!INCLUDE[footer-include](includes/footer-banner.md)]