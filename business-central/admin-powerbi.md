---
title: Einführung in Business Central und Power BI
description: 'Sie erhalten eine Übersicht der Verwendung von Power BI, um Erkenntnisse, Business Intelligence und KPIs aus Ihren Business Central-Daten zu erhalten.'
author: jswymer
ms.topic: overview
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.search.form: '6316, 6317'
ms.reviewer: jswymer
ms.date: 07/17/2023
ms.author: jswymer
ms.custom: bap-template
---
# <a name="introduction-to--and-power-bi"></a>Einführung in [!INCLUDE[prod_short](includes/prod_short.md)] und Power BI

Einblicke in Ihre [!INCLUDE[prod_short](includes/prod_short.md)]-Daten sind mit [Power BI](https://powerbi.microsoft.com), einem Datenvisualisierungssystem von Microsoft, kein Problem. Power BI ruft [!INCLUDE[prod_short](includes/prod_short.md)]-Daten ab, damit Sie mit diesen Daten Dashboards und Berichte erstellen können. Power BI stellt eine flexible Alternative zu den in [!INCLUDE[prod_short](includes/prod_short.md)] integrierten Berichten dar, mit der Sie einen Drilldown durchführen und die Visualisierung anpassen können. Sie können in [!INCLUDE[prod_short](includes/prod_short.md)] sogar die Daten verschiedener Unternehmen zusammenführen. Manche Power BI-Berichte können auch in Business Central eingebettet und angezeigt werden, ohne das System zu verlassen. Komplexere Dashboards bieten auf der Power BI-Webseite eine bessere Erfahrung.

![Power BI und Business Central.](media/power-bi-intro.png)

## <a name="what-you-can-do-with-power-bi-and-"></a>Möglichkeiten von Power BI und [!INCLUDE[prod_short](includes/prod_short.md)]

Bei der Arbeit mit [!INCLUDE[prod_short](includes/prod_short.md)] und Power BI stehen Ihnen verschiedene Funktionen zur Verfügung. Manche Dinge werden über Power BI ausgeführt, andere über [!INCLUDE[prod_short](includes/prod_short.md)]. Außerdem sind einige Funktionen nur mit [!INCLUDE[prod_short](includes/prod_short.md)] online verfügbar und nicht mit on-premises. Die folgende Tabelle verschafft Ihnen einen Überblick.

|Funktion|Description|Online|Lokal|Weitere Informationen|
|-------|-----------|--------------|-----------|----------------|
|Zeigen Sie [!INCLUDE[prod_short](includes/prod_short.md)]-Daten in Power BI an.|Sie können Ihre Daten aus [!INCLUDE[prod_short](includes/prod_short.md)] in Berichten in Power BI anzeigen. [!INCLUDE[prod_short](includes/prod_short.md)] online umfasst einige vordefinierte Power BI-Berichte. Oder möglicherweise hat Ihre Organisation einige benutzerdefinierte Berichte für Sie zur Verfügung gestellt.|![Funktioniert online.](media/check.png)|![Funktioniert lokal](media/check.png)|[Hier...](across-working-with-business-central-in-powerbi.md)|
|Zeigen Sie Power BI-Berichte im [!INCLUDE[prod_short](includes/prod_short.md)]-Client an.| Power BI-Berichte, die [!INCLUDE[prod_short](includes/prod_short.md)]-Daten anzeigen, können direkt in Teile von [!INCLUDE[prod_short](includes/prod_short.md)]-Seiten eingebettet werden. Sie können in diesem Teil jeden beliebigen Bericht anzeigen, der Ihnen zur Verfügung steht. |![Funktioniert online.](media/check.png)|![Funktioniert lokal](media/check.png)<sup>[*](#onprem)</sup>|[Hier...](across-working-with-powerbi.md).|
|Erstellen Sie Berichte und Dashboards in Power BI, die [!INCLUDE[prod_short](includes/prod_short.md)]-Daten anzeigen.|Verwenden Sie Power BI Desktop, um eigene Berichte und Dashboards zu erstellen. Sie können die Berichte in Ihrem eigenen Power BI-Dienst veröffentlichen oder sie mit anderen Personen innerhalb ihrer Organisation teilen.|![Funktioniert online.](media/check.png)|![Funktioniert lokal](media/check.png)|[Hier...](across-how-use-financials-data-source-powerbi.md)|
|[!INCLUDE[prod_short](includes/prod_short.md)]-Apps in Power BI| [!INCLUDE[prod_short](includes/prod_short.md)] veröffentlicht drei Apps für Power BI auf Microsoft AppSource. Diese Apps erstellen detaillierte Berichte und Dashboards in Ihrem Power BI-Dienst zum Anzeigen von [!INCLUDE[prod_short](includes/prod_short.md)]-Daten. Zu den verfügbaren Apps gehören: <ul><li>[!INCLUDE [prod_long](includes/prod_long.md)] – CRM </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] – Finance </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] – Sales </li></ul>  |![Funktioniert online.](media/check.png)||[Hier...](across-powerbi-business-central-apps.md)|
|Arbeiten mit [!INCLUDE [prod_short](includes/prod_short.md)] Daten in Datamarts und Dataflows|Ab Juli 2022 können Sie den Connector [!INCLUDE [prod_short](includes/prod_short.md)] in Power Query Online zu Datenflows verwenden, die Sie über verschiedene Berichte und Dashboards hinweg teilen.|![Funktioniert online.](media/check.png)||[Hier...](across-powerbi-business-central-apps.md)|

<a name="onprem"><sup>*</sup></a> Für diese Funktion ist eine registrierte Anwendung für Business Central in Microsoft Azure erforderlich. Weitere Informationen finden Sie unter [Registrieren von Business Central lokal in Azure AD zur Integration mit anderen Diensten](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

## <a name="get-ready-to-use-power-bi"></a>Vorbereitung auf die Verwendung von Power BI

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

## <a name="track-your-business-kpis-with-power-bi-metrics"></a>Verfolgen Sie Ihre Geschäfts-KPIs mit Power BI Metriken nach

Wenn Sie Power BI auf [!INCLUDE[prod_short](includes/prod_short.md)] Daten verwenden, können Sie wichtige KPIs oder Metriken ganz einfach nachverfolgen. 

Mit Metriken in Power BI können Sie Ihre eigenen Metriken zusammenstellen und sie in einem einzigen Bereich mit wichtigen Geschäftszielen vergleichen. Dieses Feature verbessert die Datenkultur, indem sie Verantwortlichkeit, Ausrichtung und Transparenz für Teams und Initiativen innerhalb von Organisationen fördert. 

Befolgen Sie diesen vierstufigen Prozess, um Power BI Metriken einzurichten:

1. Erstellen Sie eine Scorecard im Power BI Dienst. Weitere Informationen finden Sie unter [Scorecards in Power BI erstellen](/power-bi/create-reports/service-goals-create).  
2. Fügen Sie die _Metriken_ hinzu, die Sie nachverfolgen möchten, indem Sie eine Verbindung zu Ihrem Power BI Telemetriebericht herstellen. Weitere Informationen finden Sie unter [Verbundene Metriken erstellen](/power-bi/create-reports/service-goals-create-connected).  
3. Um Warnmeldungen hinzuzufügen, legen Sie Statusregeln für Ihre Metriken fest. Weitere Informationen finden Sie unter [Automatisierte Statusregeln für Metriken erstellen](/power-bi/create-reports/service-metrics-status-rules).  

    Dieser Schritt automatisiert Statusaktualisierungen basierend auf Regeln, die diese Metrik steuern. Regeln lösen Änderungen basierend auf dem Wert, dem Prozentsatz der Zielerreichung, den Datumsbedingungen oder einer Kombination der drei aus, wodurch die Regeln so vielseitig wie möglich werden. Für verbundene Metriken werden diese Statusregeln jedes Mal aktualisiert, wenn die Daten in Ihrer Scorecard aktualisiert werden.
4. Folgen Sie schließlich den Metriken, um Benachrichtigungen in Teams oder per E-Mail zu erhalten. Weitere Informationen finden Sie unter [Ihre Metriken nachverfolgen](/power-bi/create-reports/service-metrics-follow).  

Weitere Informationen zu Power BI-Metriken finden Sie unter [Erste Schritte mit Metriken in Power BI](/power-bi/create-reports/service-goals-introduction).

> [!NOTE]
> Es ist derzeit nicht möglich, Scorecards aus Power BI Metriken in [!INCLUDE[prod_short](includes/prod_short.md)] einzubetten.

## <a name="next-steps"></a>Nächste Schritte

- Wenn Sie ein Administrierender sind, der Power BI in [!INCLUDE[prod_short](includes/prod_short.md)] einrichten muss, gehen Sie zu [Power BI Integration aktivieren](admin-powerbi-setup.md).
- Wenn Power BI bereits eingerichtet ist und Sie die Features ausprobieren möchten, gehen Sie zu [Mit Power BI Berichten in Business Central arbeiten](across-working-with-powerbi.md).

## <a name="see-also"></a>Siehe auch

[Business Intelligence](bi.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] einrichten](setup.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] als Power BI-Datenquelle verwenden](across-how-use-financials-data-source-powerbi.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] als Power Apps-Datenquelle verwenden](across-how-use-financials-data-source-powerapps.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] in Power Automate verwenden](across-how-use-financials-data-source-flow.md)  
[Power BI Dokumentation](/power-bi/)  
[Was ist Power BI?](/power-bi/fundamentals/power-bi-overview)  
[Schnellstart: Stellen Sie eine Verbindung zu Daten her in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Einführung in Datamarts](/power-bi/transform-model/datamarts/datamarts-overview)  
[Einführung in Datenflows und Self-Service-Datenvorbereitung](/power-bi/transform-model/dataflows/dataflows-introduction-self-service)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
