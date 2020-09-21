---
title: Ermöglichen der Power BI-Integration mit Business Central | Microsoft Docs
description: Insight, Business Intelligence und KPIs aus Ihren Business Central Daten einfach beziehen mit der Business Central Anwendung für Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 92b3bb1d04c58332db20c978928fe1b04ed2ab37
ms.sourcegitcommit: aeaa0dc64e54432a70c4b0e1faf325cd17d01389
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697765"
---
# <a name="enabling-power-bi-integration-with-prodshort"></a>Ermöglichen der Power BI-Integration mit [!INCLUDE[prodshort](includes/prodshort.md)]

Dieser Artikel beschreibt, wie man [!INCLUDE[prodshort](includes/prodshort.md)] für die Integration mit Power BI vorbereitet. [!INCLUDE[prodshort](includes/prodshort.md)] online ist bereits für die Integration vorbereitet, obwohl Sie eventuell einige Informationen zur Lizenzierung lesen möchten. Für [!INCLUDE[prodshort](includes/prodshort.md)] on-premises müssen Sie Ihre Umgebung für die Verbindung mit Power BI einrichten, bevor Benutzer damit arbeiten können.

## <a name="power-bi-licensing"></a><a name="license"></a>Power BI-Lizenzierung

Mit [!INCLUDE[prodshort](includes/prodshort.md)] erhalten Benutzer eine kostenlose Power BI-Lizenz, die Zugriff auf die gängigsten Funktionen von [!INCLUDE[prodshort](includes/prodshort.md)] und Power BI bietet. Sie können auch eine Power BI Pro-Lizenz kaufen, die Zugriff auf zusätzliche Funktionen bietet. Die folgende Tabelle bietet einen Überblick über die Funktionen, die mit jeder Lizenz verfügbar sind.

|Power-Lizenz|Berichte anzeigen|Berichte erstellen|Berichte teilen|Berichte aktualisieren| [!INCLUDE[prodshort](includes/prodshort.md)]-Apps|
|-------------|--------||
|Power BI kostenlos|![Aktivieren](media/check.png)|![Aktivieren](media/check.png)|(eingeschränkt)|(eingeschränkt)||
|Power BI Pro|![Aktivieren](media/check.png)|![Aktivieren](media/check.png)|![Aktivieren](media/check.png)|(umfangreich)|![Aktivieren](media/check.png)|

Weitere Informationen finden Sie unter [Lizenzierung des Power BI-Dienstes für Benutzer in Ihrer Organisation](/power-bi/admin/service-admin-licensing-organization) oder unter [Als Einzelperson für den Power BI-Dienst anmelden](/power-bi/fundamentals/service-self-service-signup-for-power-bi).

## <a name="set-up-prodshort-on-premises-for-power-bi-integration"></a><a name="setup"></a>[!INCLUDE[prodshort](includes/prodshort.md)] on-premises für die Power BI-Integration einrichten

In diesem Abschnitt werden die Anforderungen für eine Bereitstellung von [!INCLUDE[prodshort](includes/prodshort.md)] on-premises zur Integration mit Power BI erläutert.

1. OData-Webdienste und der ODataV4-Endpunkt sind aktiviert.

    Der OData-Webdienst muss auf dem [!INCLUDE[server](includes/server.md)] aktiviert sein und der OData-Port in der Firewall muss offen sein. Weitere Informationen finden Sie unter [Konfigurieren von Business Central Server – OData-Webdienste](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).
    
    Der lokale Server muss über das Internet erreichbar sein.

2. [!INCLUDE[prodshort](includes/prodshort.md)]-Benutzerkonten verfügen über einen Webdienst-Zugriffsschlüssel.

    Zur Anzeige von [!INCLUDE[prodshort](includes/prodshort.md)]-Daten in Power BI wird ein Webdienst-Zugriffsschlüssel benötigt. Sie können jedem Benutzerkonto einen Webdienst-Zugriffsschlüssel zuweisen. Oder erstellen Sie stattdessen ein bestimmtes Konto mit einem Webdienst-Zugriffsschlüssel, der von allen Benutzern verwendet werden kann. Weitere Informationen finden Sie unter [Webdienst-Authentifizierung](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

3. NavUserPassword- oder Azure Active Directory-Authentifizierung ist konfiguriert.

4. Um Power BI-Berichte anzuzeigen, die in [!INCLUDE[prodshort](includes/prodshort.md)]-Seiten eingebettet sind, muss für [!INCLUDE[prodshort](includes/prodshort.md)] in Microsoft Azure eine Anwendung registriert werden.

    Die registrierte Anwendung benötigt Berechtigungen für Power BI-Dienste. Weitere Informationen finden Sie unter [Registrieren von [!INCLUDE[prodshort](includes/prodshort.md)] On-Premises in Azure AD zur Integration mit anderen Diensten](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > Wenn Ihre Bereitstellung die NavUserPassword-Authentifizierung verwendet, stellt [!INCLUDE[prodshort](includes/prodshort.md)] für alle Benutzer eine Verbindung mit demselben Power BI-Dienst her. Sie geben dieses Dienstkonto bei der Registrierung der Anwendung an. Wenn Sie die Azure AD-Authentifizierung verwenden, verbindet sich [!INCLUDE[prodshort](includes/prodshort.md)] mit dem Power BI-Dienst, der den einzelnen Benutzerkonten zugeordnet ist.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->

## <a name="publish-data-as-web-services"></a>Daten als Webdienste veröffentlichen

Codeunits, Seiten und Abfragen, die Sie als Datenquelle in Power BI-Berichten verwenden möchten, müssen als Webdienste veröffentlicht werden. Viele Webdienste werden standardmäßig veröffentlicht. Eine einfache Methode, die Webdienste zu finden ist, in *Webdiensten* in [!INCLUDE[prodshort](includes/prodshort.md)] zu suchen. Vergewissern Sie sich, dass auf der Seite **Webdienste** das Feld **Veröffentlichen** für die oben aufgeführten Webdienste ausgewählt ist. Hierbei handelt es sich üblicherweise um eine Aufgabe für einen Administrator.

Weitere Informationen zum Veröffentlichen von Webdiensten finden Sie unter [Webdienst veröffentlichen](across-how-publish-web-service.md).

> [!TIP]
> Um zu erfahren, wie Sie vom Business Central Server (Endpunkt) und vom Verbaucher (dem Client) aus gesehen die optimale Leistung von Webdiensten erzielen, lesen Sie [Effiziente Webdienste schreiben](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-web-services).




## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/Configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Business Central und Power BI](admin-powerbi.md)  
[Übersicht über die Power BI-Integrationskomponente und -Architektur für [!INCLUDE[prodshort](includes/prodshort.md)]](admin-powerbi-overview.md)  
[Power BI für Verbraucher](/power-bi/consumer/end-user-consumer)  
[Der „neue Look“ des Power BI Service](/power-bi/service-new-look)  
[Schnellstart: Stellen Sie eine Verbindung zu Daten her in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI Dokumentation](/power-bi/)  
[Business Intelligence](bi.md)  
[Erste Schritte](product-get-started.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Verwenden von [!INCLUDE[d365fin](includes/d365fin_md.md)] als Power BI-Datenquelle](across-how-use-financials-data-source-powerbi.md)  
[Verwenden von [!INCLUDE[d365fin](includes/d365fin_md.md)] als Power Apps-Datenquelle](across-how-use-financials-data-source-powerapps.md)  
[Verwenden von [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power Automate](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
