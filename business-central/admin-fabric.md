---
title: Einführung in Microsoft Fabric und Business Central
description: 'Sie erhalten eine Übersicht der Verwendung von Microsoft Fabric, um Erkenntnisse, Business Intelligence und KPIs aus Ihren Business Central-Daten zu erhalten.'
author: kennienp
ms.topic: overview
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.search.form: '6316, 6317'
ms.reviewer: bholtorf
ms.date: 04/24/2024
ms.author: kepontop
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Einführung in Microsoft Fabric und Business Central

[!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] ist eine End-to-End-Analyselösung mit Full-Service-Funktionen, einschließlich Datenverschiebung, Data Lakes, Datentechnik, Datenintegration, Data Science, Echtzeitanalysen und Business Intelligence, die alle von einer gemeinsamen Plattform unterstützt werden, die robuste Datensicherheit, Governance und Compliance bietet. Ihr Unternehmen muss nicht mehr einzelne Analysedienste mehrerer Anbieter zusammenbasteln. Nutzen Sie stattdessen eine optimierte Lösung, die sich einfach verbinden, integrieren und bedienen lässt.

> [!NOTE]
> Weitere Informationen über den Veröffentlichungsplan von Microsoft Fabric finden Sie unter [aka.ms/FabricRoadmap](https://aka.ms/FabricRoadmap)
> 
> Durch die regelmäßige Veröffentlichung dieser Roadmap bleiben Sie darüber auf dem Laufenden, wie [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] auf Ihre Bedürfnisse eingehen wird.

## Wie passt [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] zur [!INCLUDE[prod_short](includes/prod_short.md)] Analyse

[!INCLUDE[prod_short](includes/prod_short.md)] verfügt über viele sofort einsatzbereite Berichte und Datenanalysefunktionen wie Finanzberichterstattung, Öffnen in Excel und Analysemodus für Listen und Abfragen. Darüber hinaus ist es einfach Power BI-Berichte festzulegen, die Daten von Standard- und benutzerdefinierten APIs lesen, Power BI Metrik-Scorecards festzulegen und diese direkt in den [!INCLUDE[prod_short](includes/prod_short.md)]-Client einzubetten. Aber für Debitoren mit fortgeschritteneren Data-Science- oder Business-Intelligence-Szenarien, die eine umfassendere Datentechnik oder Datenintegration erfordern, könnte [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] eine gute Option sein. 

## OneLake

Ein wichtiger Teil des [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)]-Angebots ist OneLake. OneLake ist ein einziger, einheitlicher, logischer Datensee für Ihre gesamte Organisation. Sie können sich OneLake als OneDrive für Daten vorstellen. Es stellt Ihnen einen Data Lake as a Service zur Verfügung, ohne dass Sie ihn selbst erstellen müssen. OneLake wird automatisch mit jedem [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] Mandanten ohne zu verwaltende Infrastruktur geliefert. Alle Daten, die in OneLake landen, nehmen automatisch an der sofort einsatzbereiten Data Governance teil, darunter Datenherkunft, Datenschutz, Zertifizierung und Katalogintegration. Es bricht Datensilos auf, indem es verschiedenen Teilen der Organisation erlaubt, unabhängig zu arbeiten und gleichzeitig zum selben Data Lake beizutragen.

[!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] Elemente speichern Ihre Daten in OneLake in einem offenen Dateiformat. Für strukturierte Tabellendaten ist das Format hier *Delta Parquet*. Das Delta-Parquet-Format ermöglicht die Integration jedes Analysemoduls in [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)], um auf die Daten anderer Analysemodule zuzugreifen. So können Datenfachkräfte flexibel die Tools ihrer Wahl nutzen.


## Siehe auch
[Power BI mit Business Central verwenden](admin-powerbi.md)   

[!INCLUDE[footer-include](includes/footer-banner.md)]
