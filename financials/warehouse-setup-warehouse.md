---
title: Konfigurieren von Lagerprozessen | Microsoft Docs
description: "Die Logistikstrategie eines Mandanten spiegelt sich in der Konfiguration seiner Lagerprozesse wider. Dazu gehört die Definition der Bearbeitung unterschiedlicher Artikel an verschiedenen Lagerorten, wie z. B. der Grad der Lagerplatzkontrolle und das Ausmaß des erforderlichen Workflows zwischen Lageraktivitäten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 130d266d5e9ff5a4d862dd9a03a781b57afd52be
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-warehouse-management"></a>Lagerortverwaltung einrichten
Die Logistikstrategie eines Mandanten spiegelt sich in der Konfiguration seiner Lagerprozesse wider. Dazu gehört die Definition der Bearbeitung unterschiedlicher Artikel an verschiedenen Lagerorten, wie z. B. der Grad der Lagerplatzkontrolle und das Ausmaß des erforderlichen Workflows zwischen Lageraktivitäten.  

 Die folgende Tabelle enthält eine Abfolge von Aufgaben sowie Links zu den entsprechenden Themen, in denen diese Aufgaben erläutert werden.   

|**Aufgabe**|**Siehe**|  
|------------|-------------|  
|Verschaffen Sie sich einen Überblick über die Kapazitäten der grundlegenden und erweiterten Lagerfunktionalität.|[Designdetails: Lagerübersicht](design-details-warehouse-overview.md)|  
|Richten Sie acht verschiedene Lagerplatzarten ein, wie z. B. Kommissionierungslagerplatz, um die Workflowaktivitäten zu definieren, die sich auf die einzelnen Lagerplatzarten beziehen.|[Vorgehensweise: Lagerplatzarten einrichten](warehouse-how-to-set-up-bin-types.md)|  
|Erstellen Sie Lagerplätze entweder manuell oder automatisch mit Informationen wie Name, Nummernserie und Kategorie entsprechend einer Lagerplatzvorlage.|[Vorgehensweise: Erstellen von Lagerplätzen](warehouse-how-to-create-individual-bins.md)|  
|Definieren Sie die Artikel, die Sie an einem bestimmten Lagerplatz aufbewahren möchten, und legen Sie die Regeln dafür fest, wann der Lagerplatz mit einem bestimmten Artikel aufgefüllt werden soll.|[Vorgehensweise: Erstellen von Lagerplatzinhalten](warehouse-how-to-set-up-bin-contents.md)|  
|Richten Sie ein, dass ein Artikel immer an einem spezifischen Lagerplatz eingelagert wird.|[Vorgehensweise: Zuordnen der Vorgabelagerplätze zu Artikeln](warehouse-how-to-assign-default-bins-to-items.md)|
|Erstellen Sie Regeln, um Ziel und Art der gesteuerten Einlagerung zu steuern.|[Vorgehensweise: Einlagerungsmethoden einrichten](warehouse-how-to-set-up-put-away-templates.md)|
|Richten Sie Benutzer als Lagermitarbeiter an bestimmten Lagerorten ein.|[Vorgehensweise: Lagermitarbeiter einrichten](warehouse-how-to-set-up-warehouse-employees.md)|
|Definieren Sie unterschiedliche Arten von Lagerplätzen in einem Lager zur Kontrolle der Platzierung von Artikeln gemäß ihrer Art, ihrem Rang oder ihrer Bearbeitungsstufe.|[Vorgehensweise: Lagerorte für die Verwendung von Lagerplätzen ein](warehouse-how-to-set-up-locations-to-use-bins.md)richten|
|Nehmen Sie an einem vorhandenen Lagerort zusätzliche Einstellungen vor, um Lageraktivitäten zu ermöglichen.|[Vorgehensweise: Konvertieren vorhandener Lagerorte in Lagerorte des Lagers](warehouse-how-to-convert-existing-locations-to-warehouse-locations.md)|
|Ermöglichen Sie die Kommissionierung und Einlagerung für Montage- oder Fertigungsaufträge in Basislagerkonfigurationen.|[Vorgehensweise: Einrichten von Basislagern mit Vorgangsbereichen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|  
|Richten Sie Artikel und Lagerorte für die höchste Logistikstufe ein, bei der alle Aktivitäten einem strikten Workflow entsprechen müssen.|[Vorgehensweise: Einrichten von Artikeln und Standorten für die gesteuerte Einlagerung und Kommissionierung](warehouse-how-to-set-up-items-for-directed-put-away-and-pick.md)|  
|Definieren Sie Zeitpunkt und Art der Zählung von Artikeln an Lagerorten zu Zwecken der Verwaltung oder für Finanzberichte.|[Vorgehensweise. Erfassen oder Regulieren von Lagerbestand](inventory-how-count-adjust-reclassify.md)|
|Ermöglichen Sie es Lagermitarbeitern, eine größere Einheit in kleinere Einheiten aufzubrechen, um die Anforderungen von Herkunftsbelegen zu erfüllen.|[Vorgehensweise: Automatisches Teilen von Gebindeeinheiten mit gesteuerter Einlagerung und Kommissionierung](warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md)|  
|Richten Sie ein, dass das Lager automatisch Artikel für die Kommissionierung vorschlägt, die zuerst ablaufen.|[Vorgehensweise: Aktiveren der Kommissionierung nach FEFO](warehouse-picking-by-fefo.md)|
|Integrieren Sie Barcodeleser in Ihrer Logistiklösung.|[Automatisierte Datenerfassung (MDE) verwenden](warehouse-use-automated-data-capture-systems-adcs.md)|  
|Sie erhalten Tipps zur Neuorganisation von Lagerorten, Lagerplätzen oder Zonen, um weitere effiziente Lageraktivitäten zu erhalten.|[Vorgehensweise: Umstrukturieren von Lagern](warehouse-how-to-restructure-warehouses.md)|  

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbest](inventory-manage-inventory.md)  
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

