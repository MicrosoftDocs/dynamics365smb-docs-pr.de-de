---
title: Konfigurieren von API Vorlagen | Microsoft Docs
description: Beschreibung der Schritte, die Sie durchlaufen, um API-Vorlagen für Dynamics 365 Business Central zu konfigurieren.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API templates, configuring templates
ms.date: 04/01/2021
ms.author: solsen
ms.openlocfilehash: 7d39262993a173fec1eae68bcb44a85332a9866a
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5773104"
---
# <a name="configuring-api-templates"></a>API Vorlagen konfigurieren
Die API-Bibliothek für [!INCLUDE[prod_short_md](includes/prod_short.md)] bietet eine vereinfachte Darstellung der zugrunde liegenden Einheiten. Alle Eigenschaften der Anwendung werden nicht durch die zugeordnete API bereitgestellt. Die Seite **API Einrichten** ermöglicht Ihnen, Vorlagen festzulegen, die verwendet werden, um leere Eigenschaften auf eine Einheit zu füllen, wenn Sie eine Beitragsaktion durch die API erstellen. 

Wenn beispielsweise eine Konfigurationsvorlage für die Artikeleinheit definiert ist, wenn ein Datensatz des neuen Artikels um die API Artikel erstellt wird, werden Eigenschaften für den neuen Artikel, die nicht im API-Aufruf definiert sind, aus der ausgewählten Vorlage definiert. Wenn beispielsweise kein Wert für das Feld **Gen. Prod. Buchungsgruppe** durch die API definiert wird, aber ein Wert in der ausgewählten Vorlage definiert ist, wird der Wert, der in der Vorlage festgelegt wird, vom neuen Artikel übernommen. 

## <a name="setting-up-the-entity-template"></a>Einrichten der Einheiten-Vorlage
Um Vorlagen mit der API-Bibliothek zu verwenden, müssen Sie verschiedene Eigenschaften für die Vorlagen anlegen und definieren. Sie können diese Vorlagen auf der Seite **Konfigurationsvorlagen** einrichten. Weitere Informationen finden Sie unter [Gewusst wie: Debitorendaten zusammenführen](admin-use-templates-to-prepare-customer-data-for-migration.md). 

## <a name="assign-the-template-to-an-api"></a>Weisen Sie die Vorlage zu einer API zu

Um eine Vorlage zu einer API zuzuordnen, müssen Sie folgende Schritte durchführen.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **API-Einrichtung** ein und wählen Sie den entsprechenden Link.
2. Wählen Sie **Neu** und dann den Wert **Auftrag** für den Datensatztyp aus.  
Wenn es mehr als eine Vorlage gibt, die für eine API ausgewählt wird (Seiten-ID), werden die Vorlagen im Auftrag angewendet, der in der Spalte **Auftrag** definiert ist.   
Wenn jeder Vorlage übernommen wird, werden die Feldwerte, die in der Vorlage definiert werden, nur zu den Feldern, die nicht bereits einen explizit definierten Wert aufweisen, entweder explizit der API oder einer zuvor zugewiesenen Vorlage im Auftrag zugeordnent. 
3. Wählen Sie einen **PageID** Wert. aus.  
Dieses ist die Seite für die API, für die die Vorlage angewendet wird. Die **Seiten-ID** Suche bietet eine Übersicht aller APIs, die in derselben Bibliothek verfügbar sind.
4. Wählen Sie im Feld **Vorlagencode** einen Wert aus.  
Der Vorlagencode ist der Code für die Vorlage, die auf der Seite **Konfigurationsvorlagen** definiert wurde. Die definierten Vorlagenwerte werden auf die API übernommen. 
5. In dem Feld **Bedingungen** geben Sie an, welche Vorlage ausgeglichen werden soll.  
Die definierte Vorlage wird in einen neuen Datensatz angewendet, der durch die API erstellt wird, wenn die Bedingungen, die im **Bedingungen** Feld definiert werden, durch die Werte erfüllt sind, die bereits für die neue Instanz der Einheit definiert werden.

## <a name="see-also"></a>Siehe auch
[API-Dokumentation](/dynamics-nav/fin-graph)  
[Connect Apps entwicklen für [!INCLUDE[prod_short_md](includes/prod_short.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
[Aktivieren der APIs](/dynamics-nav/enabling-apis-for-dynamics-nav)  
[Endpunkte für die APIs](/dynamics-nav/endpoints-apis-for-dynamics)  
[Mandanten mit RapidStart Services einrichten](admin-set-up-a-company-with-rapidstart.md)  
[Verwaltung](admin-setup-and-administration.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]