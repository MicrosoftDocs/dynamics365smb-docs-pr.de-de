---
title: Konfigurieren von Lagerprozessen | Microsoft Docs
description: Die Logistikstrategie eines Mandanten spiegelt sich in der Konfiguration seiner Lagerprozesse wider. Dazu gehört die Definition der Bearbeitung unterschiedlicher Artikel an verschiedenen Lagerorten, wie z. B. der Grad der Lagerplatzkontrolle und das Ausmaß des erforderlichen Workflows zwischen Lageraktivitäten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c96691ada97f0ee91b53d9cde303c2413e99025e
ms.sourcegitcommit: 32bfc2acaaf3693afc9aeb86feea505fd328caa1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/19/2021
ms.locfileid: "5024387"
---
# <a name="setting-up-warehouse-management"></a>Lagerortverwaltung einrichten
Die Logistikstrategie eines Mandanten spiegelt sich in der Konfiguration seiner Lagerprozesse wider. Dazu gehört die Definition der Bearbeitung unterschiedlicher Artikel an verschiedenen Lagerorten, wie z. B. der Grad der Lagerplatzkontrolle und das Ausmaß des erforderlichen Workflows zwischen Lageraktivitäten.  

 Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Themen, die sie beschreiben..   

|**Aufgabe**|**Siehe**|  
|------------|-------------|  
|Verschaffen Sie sich einen Überblick über die Kapazitäten der grundlegenden und erweiterten Lagerfunktionalität.|[Designdetails: Lagerübersicht](design-details-warehouse-overview.md)|  
|Richten Sie acht verschiedene Lagerplatzarten ein, wie z. B. Kommissionierungslagerplatz, um die Workflowaktivitäten zu definieren, die sich auf die einzelnen Lagerplatzarten beziehen.|[Lagerplatzarten einrichten](warehouse-how-to-set-up-bin-types.md)|  
|Erstellen Sie Lagerplätze entweder manuell oder automatisch mit Informationen wie Name, Nummernserie und Kategorie entsprechend einer Lagerplatzvorlage.|[Lagerplätze erstellen](warehouse-how-to-create-individual-bins.md)|  
|Definieren Sie die Artikel, die Sie an einem bestimmten Lagerplatz aufbewahren möchten, und legen Sie die Regeln dafür fest, wann der Lagerplatz mit einem bestimmten Artikel aufgefüllt werden soll.|[Lagerplatzinhalt erstellen](warehouse-how-to-set-up-bin-contents.md)|  
|Richten Sie ein, dass ein Artikel immer an einem spezifischen Lagerplatz eingelagert wird.|[Zuordnen der Vorgabelagerplätze zu Artikeln](warehouse-how-to-assign-default-bins-to-items.md)|
|Erstellen Sie Regeln, um Ziel und Art der gesteuerten Einlagerung zu steuern.|[Einlagerungsmethoden einzurichten:](warehouse-how-to-set-up-put-away-templates.md)|
|Richten Sie Benutzer als Lagermitarbeiter an bestimmten Lagerorten ein.|[So richten Sie die Lagermitarbeiter ein](warehouse-how-to-set-up-warehouse-employees.md)|
|Definieren Sie unterschiedliche Arten von Lagerplätzen in einem Lager zur Kontrolle der Platzierung von Artikeln gemäß ihrer Art, ihrem Rang oder ihrer Bearbeitungsstufe.|[Lagerorte für die Verwendung von Lagerplätzen einrichten](warehouse-how-to-set-up-locations-to-use-bins.md)|
|Nehmen Sie an einem vorhandenen Lagerort zusätzliche Einstellungen vor, um Lageraktivitäten zu ermöglichen.|[Konvertieren vorhandener Lagerorte in Lagerorte des Lagers](warehouse-how-to-convert-existing-locations-to-warehouse-locations.md)|
|Ermöglichen Sie die Kommissionierung und Einlagerung für Montage- oder Fertigungsaufträge in Basislagerkonfigurationen.|[Einrichten von Basislagern mit Vorgangsbereichen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|  
|Richten Sie Artikel und Lagerorte für die höchste Logistikstufe ein, bei der alle Aktivitäten einem strikten Workflow entsprechen müssen.|[Einrichten von Artikeln und Standorten für die gesteuerte Einlagerung und Kommissionierung](warehouse-how-to-set-up-items-for-directed-put-away-and-pick.md)|  
|Definieren Sie Zeitpunkt und Art der Zählung von Artikeln an Lagerorten zu Zwecken der Verwaltung oder für Finanzberichte.|[Erfassen, Regulieren und Umbuchen von Lagerbestand](inventory-how-count-adjust-reclassify.md)|
|Ermöglichen Sie es Lagermitarbeitern, eine größere Einheit in kleinere Einheiten aufzubrechen, um die Anforderungen von Herkunftsbelegen zu erfüllen.|[Automatisches Teilen von Gebindeeinheiten mit gesteuerter Einlagerung und Kommissionierung aktivieren](warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md)|  
|Richten Sie ein, dass das Lager automatisch Artikel für die Kommissionierung vorschlägt, die zuerst ablaufen.|[Aktiveren der Kommissionierung nach FEFO](warehouse-picking-by-fefo.md)|
|Sie erhalten Tipps zur Neuorganisation von Lagerorten, Lagerplätzen oder Zonen, um weitere effiziente Lageraktivitäten zu erhalten.|[Lager umstrukturieren](warehouse-how-to-restructure-warehouses.md)|
|Integrieren Sie Barcodeleser in Ihrer Logistiklösung. Nur für lokale Bereitstellung.|[Automatisierte Datenerfassung (MDE) verwenden](warehouse-use-automated-data-capture-systems-adcs.md)|
|Geben Sie Standardberichte an, die für verschiedene Dokumenttypen verwendet werden sollen.|[Berichtsauswahl in Business Central](across-report-selections.md)|

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]