---
title: Konfigurieren von API Vorlagen | Microsoft Docs
description: "Die Schritte, die Sie durchmachen, um API-Vorlagen für Dynamics 365 Business Central zu konfigurieren."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API templates, configuring templates
ms.date: 05/16/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 1695a6950dabc1b2f0a2f85ad9e0c565012c92e1
ms.contentlocale: de-de
ms.lasthandoff: 05/17/2018

---

# <a name="configuring-api-templates"></a>API Vorlagen konfigurieren
Die API-Bibliothek für [!INCLUDE[d365fin_md](includes/d365fin_md.md)] bietet eine vereinfachte Darstellung der zugrunde liegenden Einheiten. Alle Eigenschaften der Anwendung werden nicht durch die zugeordnete API bereitgestellt. Das Fenster **API Setup** ermöglicht Ihnen, Vorlagen festzulegen, die verwendet werden, um auf eine leere Eigenschaften Einheit zu füllen, wenn Sie eine Beitragsaktion durch die API erstellen. 

Wenn beispielsweise eine Konfigurationsvorlage für die Artikeleinheit definiert ist, wenn ein Datensatz des neuen Artikels um die API Artikel erstellt wird, werden Eigenschaften für den neuen Artikel, die nicht im API-Aufruf definiert sind, aus der ausgewählten Vorlage definiert. Wenn beispielsweise kein Wert für das Feld **Gen. Prod. Buchungsgruppe** durch die API definiert wird, aber ein Wert in der ausgewählten Vorlage definiert ist, wird der Wert, der in der Vorlage festgelegt wird, vom neuen Artikel übernommen. 

## <a name="setting-up-the-entity-template"></a>Einrichten der Einheiten-Vorlage
Um Vorlagen mit der API-Bibliothek zu verwenden, müssen Sie verschiedene Eigenschaften für die Vorlagen anlegen und definieren. Sie können diese Vorlagen im Fenster **Konfigurationsvorlagen** einrichten. Weitere Informationen finden Sie unter [Gewusst wie: Kundendaten zusammenführen](admin-use-templates-to-prepare-customer-data-for-migration.md). 

## <a name="assign-the-template-to-an-api"></a>Weisen Sie die Vorlage zu einer API zu

Um eine Vorlage zu einer API zuzuordnen, müssen Sie folgende Schritte durchführen.

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **API-Dienst einrichten** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie **Neu** und dann den Wert **Auftrag** für den Datensatztyp aus.  
Wenn es mehr als eine Vorlage gibt, die für eine API ausgewählt wird (Seiten-ID), werden die Vorlagen im Auftrag angewendet, der in der Spalte **Auftrag** definiert ist.   
Wenn jeder Vorlage übernommen wird, werden die Feldwerte, die in der Vorlage definiert werden, nur zu den Feldern, die nicht bereits einen explizit definierten Wert aufweisen, entweder explizit der API oder einer zuvor zugewiesenen Vorlage im Auftrag zugeordnent. 
3. Wählen Sie einen **PageID** Wert. aus.  
Dieses ist die Seite für die API, für die die Vorlage angewendet wird. Die **Seiten-ID**  Suche bietet eine Übersicht aller APIs, die in derselben Bibliothek verfügbar sind.
4. Wählen Sie im Feld **Vorlagencode** einen Wert aus.  
Der Vorlagencode ist der Code für die Vorlage, die im **Konfigurationsvorlagen** definiert wurde. Die definierten Vorlagenwerte werden auf die API übernommen. 
5. In dem Feld **Bedingungen** geben Sie an, welche Vorlage ausgeglichen werden soll.  
Die definierte Vorlage wird in einen neuen Datensatz angewendet, der durch die API erstellt wird, wenn die Bedingungen, die im **Bedingungen** Feld definiert werden, durch die Werte erfüllt sind, die bereits für die neue Instanz der Einheit definiert werden.

## <a name="see-also"></a>Siehe auch
[API-Dokumentation](/dynamics-nav/fin-graph)  
[Connect Apps entwicklen für [!INCLUDE[d365fin_md](includes/d365fin_md.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
[Aktivieren der APIs](/dynamics-nav/enabling-apis-for-dynamics-nav)  
[Endpunkte für die APIs](/dynamics-nav/endpoints-apis-for-dynamics)  
[Einrichten von Mandanten mit RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Verwaltung](admin-setup-and-administration.md)
