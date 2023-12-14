---
title: Einführung in Microsoft Fabric und Business Central
description: 'Hier erhalten Sie eine Übersicht über die Verwendung von Microsoft Fabric, um Erkenntnisse, Business Intelligence und KPIs aus Ihren Business Central-Daten zu erhalten.'
author: kennienp
ms.topic: overview
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.search.form: '6316, 6317'
ms.reviewer: jswymer
ms.date: 10/10/2023
ms.author: kepontop
ms.custom: bap-template
---
# <a name="introduction-to-microsoft-fabric-and-business-central"></a>Einführung in Microsoft Fabric und Business Central

[!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] ist eine End-to-End-Analyselösung mit Full-Service-Funktionen, einschließlich Datenverschiebung, Data Lakes, Datentechnik, Datenintegration, Data Science, Echtzeitanalysen und Business Intelligence, die alle von einer gemeinsamen Plattform unterstützt werden, die robuste Datensicherheit, Governance und Compliance bietet. Ihr Unternehmen muss nicht mehr einzelne Analysedienste mehrerer Anbieter zusammenbasteln. Nutzen Sie stattdessen eine optimierte Lösung, die sich einfach verbinden, integrieren und bedienen lässt.

> [!NOTE]
> [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] befindet sich derzeit in der Vorschau. Weitere Informationen über den Veröffentlichungsplan von Microsoft Fabric finden Sie unter [aka.ms/FabricRoadmap](https://aka.ms/FabricRoadmap)
> 
> Durch die regelmäßige Veröffentlichung dieser Roadmap bleiben Sie darüber auf dem Laufenden, wie [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] auf Ihre Bedürfnisse eingehen wird.

## <a name="where-does--fit-into-includeprod_short-analytics"></a>Wie passt [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] zur [!INCLUDE[prod_short](includes/prod_short.md)] Analyse

[!INCLUDE[prod_short](includes/prod_short.md)] verfügt über viele sofort einsatzbereite Berichte und Datenanalysefunktionen wie Finanzberichterstattung, Öffnen in Excel und Analysemodus für Listen und Abfragen. Darüber hinaus ist es einfach Power BI-Berichte festzulegen, die Daten von Standard- und benutzerdefinierten APIs lesen, Power BI Metrik-Scorecards festzulegen und diese direkt in den [!INCLUDE[prod_short](includes/prod_short.md)]-Client einzubetten. Aber für Debitoren mit fortgeschritteneren Data-Science- oder Business-Intelligence-Szenarien, die eine umfassendere Datentechnik oder Datenintegration erfordern, könnte [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] eine gute Option sein. 

## <a name="onelake"></a>OneLake

Ein wichtiger Teil des [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)]-Angebots ist OneLake. OneLake ist ein einziger, einheitlicher, logischer Datensee für Ihre gesamte Organisation. Sie können sich OneLake als OneDrive für Daten vorstellen. Es stellt Ihnen einen Data Lake as a Service zur Verfügung, ohne dass Sie ihn selbst erstellen müssen. OneLake wird automatisch mit jedem [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] Mandanten ohne zu verwaltende Infrastruktur geliefert. Alle Daten, die in OneLake landen, nehmen automatisch an der sofort einsatzbereiten Data Governance teil, darunter Datenherkunft, Datenschutz, Zertifizierung und Katalogintegration. Es bricht Datensilos auf, indem es verschiedenen Teilen der Organisation erlaubt, unabhängig zu arbeiten und gleichzeitig zum selben Data Lake beizutragen.

[!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] Elemente speichern Ihre Daten in OneLake in einem offenen Dateiformat. Für strukturierte Tabellendaten ist das Format hier *Delta Parquet*. Das Delta-Parquet-Format ermöglicht die Integration jedes Analysemoduls in [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)], um auf die Daten anderer Analysemodule zuzugreifen. So können Datenfachkräfte flexibel die Tools ihrer Wahl nutzen.

> [!NOTE]
> Wir gehen davon aus, dass ab einer zukünftigen Veröffentlichungen [!INCLUDE[prod_short](includes/prod_short.md)] Daten auch in OneLake für die Debitoren verfügbar gemacht werden, die sowohl [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] als auch [!INCLUDE[prod_short](includes/prod_short.md)] nutzen und in den Bereichen, die [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] unterstützt, einzigartige Anforderungen hat. Der Zeitplan hängt vom Zeitplan der allgemeinen Verfügbarkeit von [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] und seinen Komponenten ab, die erforderlich sind, um diese Umgebung zu aktivieren. Sobald wir mehr wissen, aktualisieren wir diesen Artikel mit einem genaueren Zeitplan.

## <a name="see-also"></a>Siehe auch
[Power BI mit Business Central verwenden](admin-powerbi.md)   

[!INCLUDE[footer-include](includes/footer-banner.md)]
