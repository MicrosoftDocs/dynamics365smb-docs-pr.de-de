---
title: Info über Lagerkostenberechnung | Microsoft Docs
description: Die Verwaltung der Lagerkostenberechnung dient zum Erfassen und Melden der Betriebskosten eines Unternehmens. Sie umfasst das Melden von Fertigungskosten und Lagerkosten (also den Wert von Artikeln).
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 18d1a44fc3ed69793dffc70fe579749623a2dc56
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778036"
---
# <a name="about-inventory-costing"></a>Info über Lagerkostenberechnung
Die Verwaltung der Lagerkostenberechnung dient zum Erfassen und Melden der Betriebskosten eines Unternehmens. Sie umfasst das Melden von Fertigungskosten und Lagerkosten (also den Wert von Artikeln).  

 Wichtige Prinzipien: Mithilfe von Lagerabgangsmethoden werden die Bewertung von Artikeln sowie der Zeitpunkt definiert, zu dem sie das Lager verlassen. Durch eine Lagerregulierung werden die Kosten für verkaufte Waren mit zugehörigen, nach dem Verkauf gebuchten Einkaufskosten aktualisiert. Lagerwerte müssen in regelmäßigen Abständen auf dedizierte Sachkonten gebucht werden.  

 In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.   

|**Aufgabe**|**Siehe**|  
|------------|-------------|  
|Unterscheiden der fünf verschiedenen Lagerabgangsmethoden und deren Auswirkungen auf Kostenströme|[Designdetails: Kostenberechnungsmethoden](design-details-costing-methods.md)|  
|Erhalten von Informationen dazu, wie Verringerungen des Lagerbestands durch Artikelausgleichsposten dynamisch mit Zunahmen verknüpft werden, um Kostenströme zu steuern|[Designdetails: Artikelausgleich](design-details-item-application.md)|  
|Erhalten von Informationen dazu, wie der Einstandspreis eines Artikels – gemäß der Lagerabgangsmethode des Artikels – fortlaufend mit den Kosten der letzten Transaktion aktualisiert wird|[Designdetails: Kostenregulierung](design-details-cost-adjustment.md)|  
|Erhalten von Informationen dazu, wie der durchschnittliche Einstandspreis eines Artikels dynamisch gemäß der ausgewählten Durchschnittskostenperiode berechnet wird|[Designdetails: Durchschnittskosten](design-details-average-cost.md)|  
|Unterscheiden der Soll-Kosten (noch nicht fakturiert) und der tatsächlichen Kosten sowie Erhalten von Informationen dazu, warum diese in der Finanzbuchhaltung verwaltet werden|[Designdetails: Soll-Kosten-Buchen](design-details-expected-cost-posting.md)|  
|Entwickeln eines Verständnisses für den Kostenregulierungsmechanismus, durch den die Berücksichtigung von Kosten auch dann sichergestellt ist, wenn Lagertransaktionen auf unregelmäßige Weise erfolgen|[Designdetails: Kostenregulierung](design-details-cost-adjustment.md)|  
|Erhalten von Informationen dazu, warum feste Einstandspreise häufig von Fertigungsbetrieben als Bewertungsgrundlage für Komponenten und Endartikel verwendet werden|[Informationen zur Berechnung von festen Einstandspreisen](finance-about-calculating-standard-cost.md)|  
|Entwickeln eines Verständnisses dafür, wie der Wert von Lagerbestand in der Finanzbuchhaltung dargestellt wird|[Melden von Kosten und Abstimmen mit der Finanzbuchhaltung](finance-report-costs-and-reconcile-with-the-general-ledger.md)|  
|Erhalten von Informationen dazu, wie dem Einstandspreis eines Artikels durch Artikelzu-/-abschläge (wie Fracht und Versicherung) zusätzliche Kostenkomponenten zugeordnet werden können|[Verwenden von Artikelzuschlägen für zusätzliche Kosten](payables-how-assign-item-charges.md)|  
|Erhalten von Informationen dazu, wie Lagerbuchungsperioden in einem Unternehmen zur kontinuierlichen Steuerung des Lagerwerts beitragen können, indem kürzere Perioden definiert werden, die im Laufe des Geschäftsjahrs abgeschlossen werden können|[Arbeiten mit Lagerbuchungsperioden](finance-how-to-work-with-inventory-periods.md)|  
|Verstehen aller Mechanismen im Kalkulationsmodul, einschließlich dessen, was passiert, wenn Sie Montage- und Produktionstransaktionen buchen.|[Designdetails: Lagerkostenberechnung](design-details-inventory-costing.md)|  

## <a name="see-also"></a>Siehe auch
[Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)    
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
