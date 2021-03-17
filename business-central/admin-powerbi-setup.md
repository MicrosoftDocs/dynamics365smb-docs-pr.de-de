---
title: Ermöglichen der Power BI-Integration in Business Central
description: Erfahren Sie, wie Sie die Verbindung zu Power BI einrichten, damit Sie mit den Business Central-Apps für Power BI Einblicke, Business Intelligence und KPIs aus Ihren Business Central-Daten erhalten.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 17e41dd44dd4f7f99eabd4904d5ebd7c48d9964d
ms.sourcegitcommit: a9d48272ce61e5d512a30417412b5363e56abf30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5492981"
---
# <a name="enabling-power-bi-integration-with-prod_short"></a>Ermöglichen der Power BI-Integration mit [!INCLUDE[prod_short](includes/prod_short.md)]

Dieser Artikel beschreibt, wie man [!INCLUDE[prod_short](includes/prod_short.md)] für die Integration mit Power BI vorbereitet. [!INCLUDE[prod_short](includes/prod_short.md)] online ist bereits für die Integration vorbereitet, obwohl Sie eventuell einige Informationen zur Lizenzierung lesen möchten. Für [!INCLUDE[prod_short](includes/prod_short.md)] on-premises müssen Sie Ihre Umgebung für die Verbindung mit Power BI einrichten, bevor Benutzer damit arbeiten können.

## <a name="power-bi-licensing"></a><a name="license"></a>Power BI-Lizenzierung

Mit [!INCLUDE[prod_short](includes/prod_short.md)] erhalten Benutzer eine kostenlose Power BI-Lizenz, die Zugriff auf die gängigsten Funktionen von [!INCLUDE[prod_short](includes/prod_short.md)] und Power BI bietet. Sie können auch eine Power BI Pro-Lizenz kaufen, die Zugriff auf zusätzliche Funktionen bietet. Die folgende Tabelle bietet einen Überblick über die Funktionen, die mit jeder Lizenz verfügbar sind.

|Power-Lizenz|Berichte anzeigen|Berichte erstellen|Berichte teilen|Berichte aktualisieren| [!INCLUDE[prod_short](includes/prod_short.md)]-Apps|
|-------------|--------||
|Power BI kostenlos|![ein Häkchen](media/check.png)|![ein weiteres Häkchen](media/check.png)|(eingeschränkt)|(eingeschränkt)||
|Power BI Pro|![und ein weiteres Häkchen](media/check.png)|![noch ein Häkchen](media/check.png)|![wieder ein Häkchen](media/check.png)|(umfangreich)|![letztes Häkchen](media/check.png)|

Weitere Informationen finden Sie unter [Lizenzierung des Power BI-Dienstes für Benutzer in Ihrer Organisation](/power-bi/admin/service-admin-licensing-organization) oder unter [Als Einzelperson für den Power BI-Dienst anmelden](/power-bi/fundamentals/service-self-service-signup-for-power-bi).

## <a name="set-up-prod_short-on-premises-for-power-bi-integration"></a><a name="setup"></a>[!INCLUDE[prod_short](includes/prod_short.md)] on-premises für die Power BI-Integration einrichten

In diesem Abschnitt werden die Anforderungen für eine Bereitstellung von [!INCLUDE[prod_short](includes/prod_short.md)] on-premises zur Integration mit Power BI erläutert.

1. Konfigurieren Sie die Authentifizierung für die Bereitstellung entweder mit NavUserPassword oder Azure Active Directory.

    Die Power BI-Integration unterstützt keine Windows-Authentifizierung.  

2. OData-Webdienste und ODataV4-Endpunkt aktivieren.

    Der OData-Webdienst muss auf dem [!INCLUDE[server](includes/server.md)] aktiviert sein und der OData-Port in der Firewall muss offen sein. Weitere Informationen finden Sie unter [Konfigurieren von Business Central Server – OData-Webdienste](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).

    Der lokale Server muss über das Internet erreichbar sein.

3. [!INCLUDE[prod_short](includes/prod_short.md)]-Benutzerkonten erhalten einen Webdienst-Zugriffsschlüssel.

    Zur Anzeige von [!INCLUDE[prod_short](includes/prod_short.md)]-Daten in Power BI wird nur ein Webdienst-Zugriffsschlüssel benötigt. Sie können jedem Benutzerkonto einen Webdienst-Zugriffsschlüssel zuweisen. Oder erstellen Sie stattdessen ein bestimmtes Konto mit einem Webdienst-Zugriffsschlüssel, der von allen Benutzern verwendet werden kann. Weitere Informationen finden Sie unter [Webdienst-Authentifizierung](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

4. Erstellen Sie eine Anwendungsregistrierung für [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft Azure.

    Um Power BI-Berichte anzuzeigen, die in [!INCLUDE[prod_short](includes/prod_short.md)]-Seiten eingebettet sind, muss eine Anwendung für [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft Azure registriert sein. Die registrierte Anwendung benötigt die Erlaubnis für Power BI-Dienstleistungen. Weitere Informationen finden Sie unter [Registrieren von [!INCLUDE[prod_short](includes/prod_short.md)] On-Premises in Azure AD zur Integration mit anderen Diensten](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > Wenn Ihre Bereitstellung die NavUserPassword-Authentifizierung verwendet, stellt [!INCLUDE[prod_short](includes/prod_short.md)] für alle Benutzer eine Verbindung mit demselben Power BI-Dienst her. Sie geben dieses Dienstkonto bei der Registrierung der Anwendung an. Wenn Sie die Azure AD-Authentifizierung verwenden, verbindet sich [!INCLUDE[prod_short](includes/prod_short.md)] mit dem Power BI-Dienst, der den einzelnen Benutzerkonten zugeordnet ist.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->
5. Stellen Sie die erste Verbindung von Business Central zu Power BI her.

    Bevor Endbenutzer Power BI in [!INCLUDE[prod_short](includes/prod_short.md)] verwenden können, muss ein Azure-Anwendungsadministrator dem Power BI-Service zustimmen.

    Um die erste Verbindung herzustellen, öffnen Sie [!INCLUDE[prod_short](includes/prod_short.md)], und führen Sie **Erste Schritte mit Power BI** über das Rollenzentrum aus. Diese Aktion führt Sie durch den Einwilligungsprozess und überprüft Ihre Power BI-Lizenz. Wenn Sie dazu aufgefordert werden, melden Sie sich mit einem Azure-Administratorkonto an. Weitere Informationen finden Sie unter [Mit Power BI verbinden – nur ein Mal](across-working-with-powerbi.md#connect).

## <a name="publish-data-as-web-services"></a>Daten als Webdienste veröffentlichen

Codeunits, Seiten und Abfragen, die Sie als Datenquelle in Power BI-Berichten verwenden möchten, müssen als Webdienste veröffentlicht werden. Viele Webdienste werden standardmäßig veröffentlicht. Eine einfache Methode, die Webdienste zu finden ist, in *Webdiensten* in [!INCLUDE[prod_short](includes/prod_short.md)] zu suchen. Vergewissern Sie sich, dass auf der Seite **Webdienste** das Feld **Veröffentlichen** für die oben aufgeführten Webdienste ausgewählt ist. Hierbei handelt es sich üblicherweise um eine Aufgabe für einen Administrator.

Weitere Informationen zum Veröffentlichen von Webdiensten finden Sie unter [Webdienst veröffentlichen](across-how-publish-web-service.md).

> [!TIP]
> Um zu erfahren, wie Sie vom Business Central Server (Endpunkt) und vom Verbaucher (dem Client) aus gesehen die optimale Leistung von Webdiensten erzielen, lesen Sie [Effiziente Webdienste schreiben](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-web-services).

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/Configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Business Central und Power BI](admin-powerbi.md)  
[Übersicht über die Power BI-Integrationskomponente und -Architektur für [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Power BI für Verbraucher](/power-bi/consumer/end-user-consumer)  
[Der „neue Look“ des Power BI Service](/power-bi/service-new-look)  
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


[!INCLUDE[footer-include](includes/footer-banner.md)]