---
title: Designdetails - Bestandbewertung | Microsoft Docs
description: Die Bestandsbewertung ist die Ermittlung der Kosten eines Lagerartikels.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5bc09374f1e72c56f5f3fbb392b2253a60437738
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781681"
---
# <a name="design-details-inventory-valuation"></a>Designdetails: Bestandsbewertung
Die Lagerbewertung ist die Identifizierung der Kosten, die einem Lagerartikel zugewiesen sind, wie durch folgende Formel dargestellt.  

Endbestand = Anfangsbestand + Nettoeinkäufe - Vertriebskosten  

Die Berechnung der Lagerbewertung verwendet das Feld **Kostenbetrag (Ist)** der Wertposten für den Artikel. Die Posten werden nach der Postenart klassifiziert, die den Kostenkomponenten, den direkten Kosten, den indirekten Kosten, der Abweichung, der Neubewertung und der Rundung entspricht. Weitere Informationen finden Sie unter [Designdetails: Kostenkomponenten](design-details-cost-components.md)  

Posten werden gegeneinander ausgeglichen, entweder durch den festen Ausgleich oder entsprechend der allgemeinen Kostenfluss-Annahme, die von der Kostenberechnungsmethode definiert ist. Ein Posten des Lagerabgangs kann mit mehr als einem Zugangseintrag mit verschiedenen Buchungsdaten und ggfs. verschiedenen Anschaffungskosten ausgeglichen werden. [Weitere Informationen finden Sie unter "Designdetails: Artikelverfolgung".](design-details-item-application.md) Daher basiert die Berechnung des Lagerbestandwerts für ein gegebenes Datum auf dem Aufsummieren von positiven und negativen Wertposten.  

## <a name="inventory-valuation-report"></a>Bericht "Aktuellen Lagerwert ermitteln"  
Um den Lagerwert im Bericht **Lagerwert berechnen** zu berechnen, beginnt der Bericht, den Lagerbestand des Artikels zu einem bestimmten Startdatum zu berechnen. Er fügt den Wert von Lagerzugängen hinzu nd subtrahiert den Wert von Lagerabgängen bis zu einem bestimmten Enddatum. Das Endergebnis ist der Lagerwert am Enddatum. Der Bericht berechnet diese Werte, indem er die Werte im Feld **Kostenbetrag (ist)** in den Wertposten summiert, wobei die Buchungsdaten als Filter verwendet werden.  

Der gedruckte Bericht zeigt immer tatsächliche (fakturierte) Beträge an, d. h. Einstandspreise von Posten, die als fakturiert gebucht wurden. Der Bericht enthält darüber hinaus die Soll-Kosten von Posten, die als geliefert gebucht wurden, wenn Sie auf dem Inforegister Optionen das Feld Inklusive Soll-Kosten durch ein Häkchen aktivieren.  

> [!IMPORTANT]  
>  Werte im Bericht **Lagerwert berechnen** wird mit dem Lagerkonto im Sachkonto abgestimmt, was bedeutet, dass die betreffenden Wertposten in der Finanzbuchhaltung gebucht wurden.  

> [!IMPORTANT]  
>  Beträge in den **Wert**-Spalten des Berichts basieren auf dem Buchungsdatum der Transaktionen für einen Artikel.  

## <a name="inventory-valuation---wip-report"></a>Bericht "Aktuellen Lagerwert ermitteln"  
Ein Produktionsbetrieb muss den Wert von drei Arten von Lagerbestand bestimmen:  

* Rohmaterialbestand  
* Produktionslager  
* Fertigerzeugnisse (Bestand)  

Der Wert des WIP-Lagers wird durch folgende Formel bestimmt:  

* End-WIP-Bestand = Anfangs-WIP-Bestand + Fertigungskosten - Fertigungskosten  

Wie bei eingekauftem Lagerbestand sind die Werteinträge die Grundlage der Bestandsbewertung. Die Berechnung erfolgt anhand der Werte in dem Feld **Kostenbetrag (Ist)** der Artikel- und Kapazitätswertposten, die mit einem Fertigungsauftrag verbunden sind.  

Der Zweck der WIP-Bestandsbewertung besteht darin, den Wert der Artikel zu ermitteln, deren Produktion an einem vorgegebenen Datum noch nicht abgeschlossen wurde. Daher ist der den Lagerwert der unfertigen Arbeit auf den Wertposten basiert, die sich auf die Verbrauchs- und Kapazitätsposten beziehen. Verbrauchsposten müssen am Datum der Bewertung vollständig fakturiert sein. Deshalb zeigt der Bericht **Lagerbewertung - Aktiviert** die Kosten an, die den den Lagerwert der unfertigen Arbeit in zwei Kategorien darstellen: Verbrauch und Kapazität.  

## <a name="see-also"></a>Siehe auch  
[Designdetails: Abgleich mit der Finanzbuchhaltung](design-details-reconciliation-with-the-general-ledger.md)   
[Designdetails: Neubewertung](design-details-revaluation.md)   
[Designdetails: Fertigungsauftrags-Buchung](design-details-production-order-posting.md)
[Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]