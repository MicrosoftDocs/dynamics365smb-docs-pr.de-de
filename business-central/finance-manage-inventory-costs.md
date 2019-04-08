---
title: Verwalten der Lagerregulierung | Microsoft Docs
description: Die Kostenverwaltung, die auch als "Lagerabgang" bezeichnet wird, dient zum Erfassen und Melden der Betriebskosten eines Unternehmens. Sie umfasst das Melden von Fertigungskosten und Lagerkosten (also den Wert von Artikeln).
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/27/2018
ms.author: sgroespe
ms.openlocfilehash: d5f5885055aa1094e4172d4a4e327ff1e940f799
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "798702"
---
# <a name="managing-inventory-costs"></a>Verwalten der Lagerregulierung
Die Kostenverwaltung, die auch als "Lagerabgang" bezeichnet wird, dient zum Erfassen und Melden der Betriebskosten eines Unternehmens. Sie umfasst das Melden von Fertigungskosten und Lagerkosten (also den Wert von Artikeln).   

Wichtige Prinzipien: Mithilfe von Lagerabgangsmethoden werden die Bewertung von Artikeln sowie der Zeitpunkt definiert, zu dem sie das Lager verlassen. Durch eine Lagerregulierung werden die Kosten für verkaufte Waren mit zugehörigen, nach dem Verkauf gebuchten Einkaufskosten aktualisiert. Lagerwerte müssen in regelmäßigen Abständen auf dedizierte Sachkonten gebucht werden.

In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.

|**Aufgabe**|**Siehe**|  
|------------|-------------|  
|Lesen verschiedener Konzeptinformationen, um ein Verständnis für die Prinzipien und Definitionen zu entwickeln, auf denen die Lagerkostenbuchungsfunktionalität in [!INCLUDE[d365fin](includes/d365fin_md.md)] beruht|[Info über Lagerkostenberechnung](finance-learn-about-costing.md)|  
|Erfahren Sie mehr über die Mechanismen im Kostenrechnungssystem.|[Designdetails: Lagerkostenberechnung](design-details-inventory-costing.md)|
|Erhalten von Informationen dazu, wie Lagerbuchungsperioden in einem Unternehmen zur kontinuierlichen Steuerung des Lagerwerts beitragen können, indem kürzere Perioden definiert werden, die im Laufe des Geschäftsjahrs abgeschlossen werden können|[Arbeiten mit Lagerbuchungsperioden](finance-how-to-work-with-inventory-periods.md)|
|Erhalten von Informationen dazu, warum feste Einstandspreise häufig von Fertigungsbetrieben als Bewertungsgrundlage für Komponenten und Endartikel verwendet werden|[Informationen zur Berechnung von festen Einstandspreisen](finance-about-calculating-standard-cost.md)|
|Einrichten von Lagerbuchungsperioden, Lagerabgangsmethoden und Rundungsmethoden.|[Einrichten der Lagerwertberechnung und der Kostenrechnung](finance-set-up-inventory-valuation-and-costing.md)|
|Schreiben sie den Wert eines oder mehrerer Artikel im Lager ab oder bewerten sie ihn neu, indem Sie den aktuellen, berechneten Wert buchen.|[Neubewerten von Lagerbestand](inventory-how-revalue-inventory.md)|
|Regulieren Sie Artikelkosten, entweder automatisch oder manuell, um Kostenänderungen aus eingehenden Posten an die entsprechenden ausgehenden Posten weiterzuleiten.|[Artikelpreise justieren](inventory-how-adjust-item-costs.md)|
|Verwendung spezieller Kostenberechnungsfunktionen für tägliche Artikeltransaktionen in den Artikeloperationen.|[Verarbeiten von Lager- und Fertigungskosten](finance-handle-inventory-and-manufacturing-costs.md)|  
|Regelmäßige Aktualisierung der festen Einstandspreise von Komponenten in Montage- oder Produktionsstücklisten und Übertragung der neuen Einstandspreise auf den übergeordneten Artikel.|[Standardkosten aktualisieren](finance-how-to-update-standard-costs.md)|
|Sie können bestimmte Artikelausgleichsposten, die bei Lagertransaktionen automatisch erstellt werden, anzeigen und manuell ändern.|[Entfernen und erneutes Ausgleichen von Artikelposten](finance-how-to-remove-and-reapply-item-entries.md)|
|Ausführen von Kontroll- und Berichterstellungsaufgaben am Periodenende – beispielsweise Berechnen des Werts von Lagerbestand und Buchen von Kosten in die Finanzbuchhaltung|[Melden von Kosten und Abstimmen mit der Finanzbuchhaltung](finance-report-costs-and-reconcile-with-the-general-ledger.md)|

## <a name="see-also"></a>Siehe auch  
 [Finanzen](finance.md)  
 [Lagerbest](inventory-manage-inventory.md)   
 [Verkauf](sales-manage-sales.md)   
 [Einkauf](purchasing-manage-purchasing.md)  
 [Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
