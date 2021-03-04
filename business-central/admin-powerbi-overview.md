---
title: Übersicht über die Power BI-Integrationskomponente und -Architektur für Business Central | Microsoft Docs
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
ms.openlocfilehash: 23a0c72775dbddc89a81105de3b2ed79d1f09432
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753770"
---
# <a name="power-bi-integration-component-and-architecture-overview-for-prod_short"></a>Übersicht über die Power BI-Integrationskomponente und -Architektur für [!INCLUDE[prod_short](includes/prod_short.md)]

In diesem Artikel erfahren Sie etwas über die verschiedenen Aspekte der Power BI-Integration mit [!INCLUDE[prod_short](includes/prod_short.md)], damit Sie die Implementierung und Verwendung besser verstehen.

## <a name="components"></a>Komponenten

In der folgenden Tabelle werden die wichtigsten Komponenten der Power BI-Integration beschrieben.

|Komponente|Beschreibung|
|---------|-----------|
|Power BI|Ein cloudbasierter Hosting- und Verwaltungsdienst für Berichte.|
|Power BI Desktop|Ein Erstellungstool für Berichte und Dashboard, mit dem Sie Berichte ausführen können. Es ist als kostenloser Download im Microsoft Store erhältlich und wird lokal installiert.|
|[!INCLUDE[prod_short](includes/prod_short.md)]|Dieses Tool ist als online oder lokale Lösung mit Connectors für Power BI erhältlich und kann als Power BI-Teil eingebettet werden.|

## <a name="whats-available-from-the-start"></a>Von Beginn an verfügbar

Die verfügbaren Funktionen werden in der folgenden Tabelle beschrieben.

|Funktion|Support für [!INCLUDE[prod_short](includes/prod_short.md)] online oder on-premises|
|-------|---------------------|
|Power BI-Connectors|Beide. Verschiedene Connectors für online und on-premises. Gleicher Connector für Power BI Desktop und Power BI-Dienst |
|Eingebettete Erfahrung zum Anzeigen eines bestimmten Berichts in einer Infobox in [!INCLUDE[prod_short](includes/prod_short.md)]|Beide. Erfordert eine Konfiguration zum Anzeigen von Berichten für lokale Version.|
|Power BI-Berichtsverwaltung über [!INCLUDE[prod_short](includes/prod_short.md)]|Online|
|Power BI-Standardberichte in Rollencentern bereitgestellt für Power BI|Online|
|Power BI-Apps auf Microsoft AppSource|Online.|

## <a name="architecture"></a>Architektur

[!INCLUDE[prod_short](includes/prod_short.md)] wird über einen Connector mithilfe von OData mit Power BI integriert. Die Datenquelle für Power BI-Berichte wird in der Form von OData-Webdiensten zur Verfügung gestellt.

![Power BI-Architektur für die Integration mit Business Central](./media/power-bi-architecture.png)

## <a name="general-flow"></a>Allgemeiner Ablauf

Das folgende Diagramm zeigt den grundlegenden Workflow für Benutzer beim Herstellen einer Verbindung zwischen [!INCLUDE[prod_short](includes/prod_short.md)] und Power BI.

![Power BI-Workflow für die Integration mit Business Central](./media/power-bi-flow.png)

1. Der Benutzer registriert sich für ein Power BI-Konto.
2. Der Benutzer stellt eine Verbindung zwischen Power BI und [!INCLUDE[prod_short](includes/prod_short.md)] her.
3. [!INCLUDE[prod_short](includes/prod_short.md)] überprüft die Lizenz.
4. [!INCLUDE[prod_short](includes/prod_short.md)] stellt Standardberichte für den Power BI-Dienst. Dieser Schritt ist nur für [!INCLUDE[prod_short](includes/prod_short.md)] online relevant.
5. [!INCLUDE[prod_short](includes/prod_short.md)] stellt Berichte in Power BI zur Auswahl in [!INCLUDE[prod_short](includes/prod_short.md)] zur Verfügung. Standardberichte werden automatisch in Power BI-Teilen angezeigt.
6. Der Benutzer erstellt einen Bericht in Power BI Desktop.
7. Der Benutzer veröffentlicht den Bericht für den Power BI-Dienst. Die Berichte können dann in [!INCLUDE[prod_short](includes/prod_short.md)] ausgewählt werden.

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Business Central und Power BI](admin-powerbi.md)  
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