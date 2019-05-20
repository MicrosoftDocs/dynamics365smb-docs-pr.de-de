---
title: Konfigurieren von API Vorlagen | Microsoft Docs
description: Beschreibung der Schritte, die Sie durchlaufen, um API-Vorlagen für Dynamics 365 Business Central zu konfigurieren.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API templates, configuring templates
ms.date: 04/01/2019
ms.author: solsen
ms.openlocfilehash: ef6b6d89ccea59de6a87c062cc6e29a27abe2c88
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245478"
---
# <a name="configuring-api-templates"></a>API Vorlagen konfigurieren
Die API-Bibliothek für [!INCLUDE[d365fin_md](includes/d365fin_md.md)] bietet eine vereinfachte Darstellung der zugrunde liegenden Einheiten. Alle Eigenschaften der Anwendung werden nicht durch die zugeordnete API bereitgestellt. Die Seite **API Einrichten** ermöglicht Ihnen, Vorlagen festzulegen, die verwendet werden, um leere Eigenschaften auf eine Einheit zu füllen, wenn Sie eine Beitragsaktion durch die API erstellen. 

Wenn beispielsweise eine Konfigurationsvorlage für die Artikeleinheit definiert ist, wenn ein Datensatz des neuen Artikels um die API Artikel erstellt wird, werden Eigenschaften für den neuen Artikel, die nicht im API-Aufruf definiert sind, aus der ausgewählten Vorlage definiert. Wenn beispielsweise kein Wert für das Feld **Gen. Prod. Buchungsgruppe** durch die API definiert wird, aber ein Wert in der ausgewählten Vorlage definiert ist, wird der Wert, der in der Vorlage festgelegt wird, vom neuen Artikel übernommen. 

## <a name="setting-up-the-entity-template"></a>Einrichten der Einheiten-Vorlage
Um Vorlagen mit der API-Bibliothek zu verwenden, müssen Sie verschiedene Eigenschaften für die Vorlagen anlegen und definieren. Sie können diese Vorlagen auf der Seite **Konfigurationsvorlagen** einrichten. Weitere Informationen finden Sie unter [Gewusst wie: Debitorendaten zusammenführen](admin-use-templates-to-prepare-customer-data-for-migration.md). 

## <a name="assign-the-template-to-an-api"></a>Weisen Sie die Vorlage zu einer API zu

Um eine Vorlage zu einer API zuzuordnen, müssen Sie folgende Schritte durchführen.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **API einrichten** ein, und wählen dann den zugehörigen Link aus.
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
[Connect Apps entwicklen für [!INCLUDE[d365fin_md](includes/d365fin_md.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
[Aktivieren der APIs](/dynamics-nav/enabling-apis-for-dynamics-nav)  
[Endpunkte für die APIs](/dynamics-nav/endpoints-apis-for-dynamics)  
[Mandanten mit RapidStart Services einrichten](admin-set-up-a-company-with-rapidstart.md)  
[Verwaltung](admin-setup-and-administration.md)