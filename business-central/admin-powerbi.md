---
title: Einführung in Business Central und Power BI | Microsoft Docs
description: Insight, Business Intelligence und KPIs aus Ihren Business Central Daten einfach beziehen mit der Business Central Anwendung für Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 51c9e2cd05deba5fd8ace46382ebeb4eb41d13ba
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753742"
---
# <a name="prod_short-and-power-bi"></a>[!INCLUDE[prod_short](includes/prod_short.md)] und Power BI

Einblicke in Ihre [!INCLUDE[prod_short](includes/prod_short.md)]-Daten sind mit [Power BI](https://powerbi.microsoft.com), einem Datenvisualisierungssystem von Microsoft, kein Problem. Power BI ruft [!INCLUDE[prod_short](includes/prod_short.md)]-Daten ab, damit Sie mit diesen Daten Dashboards und Berichte erstellen können. Power BI stellt eine flexible Alternative zu den in [!INCLUDE[prod_short](includes/prod_short.md)] integrierten Berichten dar, mit der Sie einen Drilldown durchführen und die Visualisierung anpassen können. Sie können in [!INCLUDE[prod_short](includes/prod_short.md)] sogar die Daten verschiedener Unternehmen zusammenführen. Manche Power BI-Berichte können auch in Business Central eingebettet und angezeigt werden, ohne das System zu verlassen. Komplexere Dashboards bieten auf der Power BI-Webseite eine bessere Erfahrung.

![Power BI und Business Central](media/power-bi-intro.png)


## <a name="what-you-can-do-with-power-bi-and-prod_short"></a>Möglichkeiten von Power BI und [!INCLUDE[prod_short](includes/prod_short.md)]

Bei der Arbeit mit [!INCLUDE[prod_short](includes/prod_short.md)] und Power BI stehen Ihnen verschiedene Funktionen zur Verfügung. Manche Dinge werden über Power BI ausgeführt, andere über [!INCLUDE[prod_short](includes/prod_short.md)]. Außerdem sind einige Funktionen nur mit [!INCLUDE[prod_short](includes/prod_short.md)] online verfügbar und nicht mit on-premises. Die folgende Tabelle verschafft Ihnen einen Überblick.

|Funktion|Beschreibung|Online|On-premises|Weitere Informationen|
|-------|-----------|--------------|-----------|----------------|
|Zeigen Sie [!INCLUDE[prod_short](includes/prod_short.md)]-Daten in Power BI an.|Sie können Ihre Daten aus [!INCLUDE[prod_short](includes/prod_short.md)] in Berichten in Power BI anzeigen. [!INCLUDE[prod_short](includes/prod_short.md)] online umfasst einige vordefinierte Power BI-Berichte. Oder möglicherweise hat Ihre Organisation einige benutzerdefinierte Berichte für Sie zur Verfügung gestellt.|![Funktioniert online](media/check.png)|![Funktioniert lokal](media/check.png)|[Siehe ...](across-working-with-powerbi.md)|
|Zeigen Sie Power BI-Berichte im [!INCLUDE[prod_short](includes/prod_short.md)]-Client an.| Power BI-Berichte, die [!INCLUDE[prod_short](includes/prod_short.md)]-Daten anzeigen, können direkt in Teile von [!INCLUDE[prod_short](includes/prod_short.md)]-Seiten eingebettet werden. Sie können in diesem Teil jeden beliebigen Bericht anzeigen, der Ihnen zur Verfügung steht. |![Funktioniert online](media/check.png)|![Funktioniert lokal](media/check.png)<sup>[*](#onprem)</sup>|[Siehe ...](across-working-with-business-central-in-powerbi.md).|
|Erstellen Sie Berichte und Dashboards in Power BI, die [!INCLUDE[prod_short](includes/prod_short.md)]-Daten anzeigen.|Verwenden Sie Power BI Desktop, um eigene Berichte und Dashboards zu erstellen. Sie können die Berichte in Ihrem eigenen Power BI-Dienst veröffentlichen oder sie mit anderen Personen innerhalb ihrer Organisation teilen.|![Funktioniert online](media/check.png)|![Funktioniert lokal](media/check.png)|[Siehe ...](across-how-use-financials-data-source-powerbi.md)
|[!INCLUDE[prod_short](includes/prod_short.md)]-Apps in Power BI| [!INCLUDE[prod_short](includes/prod_short.md)] veröffentlicht drei Apps für Power BI auf Microsoft AppSource. Diese Apps erstellen detaillierte Berichte und Dashboards in Ihrem Power BI-Dienst zum Anzeigen von [!INCLUDE[prod_short](includes/prod_short.md)]-Daten. Zu den verfügbaren Apps gehören: <ul><li>[!INCLUDE [prod_long](includes/prod_long.md)] – CRM </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] – Finance </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] – Sales </li></ul>  |![Funktioniert online](media/check.png)||[Siehe ...](across-powerbi-business-central-apps.md)

<a name="onprem"><sup>*</sup></a> Für diese Funktion ist eine registrierte Anwendung für Business Central in Microsoft Azure erforderlich. Weitere Informationen finden Sie unter [Registrieren von Business Central On-Premises in Azure AD zur Integration mit anderen Diensten](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

## <a name="getting-ready-to-use-power-bi"></a>Vorbereitung auf die Verwendung von Power BI

Es gibt einige Aufgaben, die vor der Verwendung von Power BI mit [!INCLUDE[prod_short](includes/prod_short.md)] erledigt werden müssen. Manche davon werden normalerweise nur von Administratoren oder Superusern ausgeführt.

1. Wenn Sie [!INCLUDE[prod_short](includes/prod_short.md)] on-premises verwenden, achten Sie darauf, dass Ihre Bereitstellung die in [[!INCLUDE[prod_short](includes/prod_short.md)] on-premises für die Power BI-Integration einrichten](admin-powerbi-setup.md#setup) beschriebenen Anforderungen erfüllt. Hierbei handelt es sich üblicherweise um eine Aufgabe für einen Administrator.

2. Veröffentlichen Sie Daten als Webdienste.

    Codeunits, Seiten und Abfragen, die Sie als Datenquelle in Power BI-Berichten verwenden möchten, müssen als Webdienste veröffentlicht werden. Viele Webdienste werden standardmäßig veröffentlicht. Eine einfache Methode, die Webdienste zu finden ist, in *Webdiensten* in [!INCLUDE[prod_short](includes/prod_short.md)] zu suchen.
    
    Weitere Informationen zum Veröffentlichen von Webdiensten finden Sie unter [Webdienst veröffentlichen](across-how-publish-web-service.md).

3. Erstellen Sie ein Power BI-Konto.

    Um überhaupt mit Power BI und [!INCLUDE[prod_short](includes/prod_short.md)] arbeiten zu können, ob als Administrator oder lediglich als Verbraucher, wird ein Power BI-Dienstkonto benötigt. Um ein Konto zu erstellen, wechseln Sie zu [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Verwenden Sie bei der Registrierung für ein Konto Ihre geschäftliche E-Mail-Adresse und Ihr zugehöriges Kennwort. Für die Anmeldung ist eine Lizenz erforderlich. In den meisten Fällen sollten Sie jedoch bereits über eine kostenlose Lizenz verfügen. Weitere Informationen finden Sie unter [Power BI-Lizenzierung](admin-powerbi-setup.md#license).

4. Wenn Sie eigene Power BI-Berichte erstellen möchten, benötigen Sie Power BI Desktop.

    Sie können [Power BI Desktop](https://powerbi.microsoft.com/desktop/) herunterladen. Weitere Informationen finden Sie unter [Power BI Desktop beziehen](/power-bi/fundamentals/desktop-get-the-desktop).

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Power BI für Verbraucher](/power-bi/consumer/end-user-consumer)  
[Der "neue Look" des Power BI Service](/power-bi/service-new-look)  
[Schnellstart: Stellen Sie eine Verbindung zu Daten her in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI Dokumentation](/power-bi/)  
[Business Intelligence](bi.md)  
[Erste Schritte](product-get-started.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Einrichten [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Verwenden von [!INCLUDE[prod_short](includes/prod_short.md)] als Power BI-Datenquelle](across-how-use-financials-data-source-powerbi.md)  
[Verwenden von [!INCLUDE[prod_short](includes/prod_short.md)] als Power Apps-Datenquelle](across-how-use-financials-data-source-powerapps.md)  
[Verwenden von [!INCLUDE[prod_short](includes/prod_short.md)] in Power Automate](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  
