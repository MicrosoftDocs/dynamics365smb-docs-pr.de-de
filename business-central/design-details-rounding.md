---
title: Designdetails – Rundung
description: 'Rundungsreste können auftreten, wenn Sie die Kosten einer Bestandsminderung, die in einer anderen Menge gemessen wurde, als die entsprechende Bestandszunahme bewerten.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Designdetails: Rundung
Rundungsreste können auftreten, wenn Sie die Kosten einer Bestandsminderung bewerten, die in einer anderen Menge als die entsprechende Bestandszunahme registriert wurde. Rundungsreste werden für alle Kostenberechnungsmethoden berechnet, wenn Sie die **Kosten anpassen - Artikeleintrag**-Stapelverarbeitung ausführen.  

 Wenn Sie die Lagerabgangsmethode "Durchschnitt" verwenn, wird der Rundungsfunktionen Rückstand in einer kumulierten Posten-durch-Posten-Basis berechnet und erfasst.  

 Wenn Sie eine andere Lagerabgangsmethode als die Lagerabgangsmethode "Durchschnitt" verwenden, wird der Rundungsfunktionen Rückstand berechnet, wenn der Lagerzugang vollständig ausgeglichen wurde, d.h. wenn die Restmenge für den Lagerzugang gleich Null ist. Dann wird ein separater Posten für den ein Rundungsrest, und das Buchungsdatum dieses Rundungspostens ist das Buchungsdatum des zuletzt fakturierten Werts.  

## Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie unterschiedliche Rundungsreste für die Durchschnittskostenbewertung und die Nicht-Durchschnittskostenbewertung behandelt werden. In beiden Fällen ist die **Kosten anpassen Artikeleingänge**-Stapelverarbeitung durchgeführt worden.  

 Die folgende Tabelle zeigt die Artikelposten, auf denen das Beispiel basiert.  

|Buchungsdatum|Menge|Lfd. Nr.|  
|------------------|--------------|---------------|  
|01-01-20|3|1|  
|02-01-20|-1|2|  
|03-01-20|-1|3|  
|04-01-20|-1|4|  

 Für einen Artikel, der die Durchschnittskostenmethode verwendet, wird die Rundungsfunktion Rückstand (1/300) mit der ersten Abgangspostennummer (Eingangsnummer 2) berechnet und auf die Postennummer 3 übertragen. Deshalb wird Postennummer 3 mit  3,34 bewertet.  

 Die folgende Tabelle zeigt die sich daraus ergebenden Wertposten.  

|Buchungsdatum|Menge|Einstandsbetrag (tatsächl.)|Artikelposten Lfd. Nr.|Lfd. Nr.|  
|------------------|--------------|----------------------------|---------------------------|---------------|  
|01-01-20|3|10|1|1|  
|02-01-20|-1|-3.33|2|2|  
|03-01-20|-1|-3.34|3|3|  
|04-01-20|-1|-3.33|4|4|  

 Für einen Artikel, der eine andere Kostenberechnungsmethode als Durchschnitt verwendet, wird der Rundungsrest (0,01) berechnet, wenn die Restmenge für die Bestandszunahme Null ist. Der Rundungsrest hat einen separaten Posten (Nummer 5).  

 Die folgende Tabelle zeigt die sich daraus ergebenden Wertposten.  

|Buchungsdatum|Menge|Einstandsbetrag (tatsächl.)|Artikelposten Lfd. Nr.|Lfd. Nr.|  
|------------------|--------------|----------------------------|---------------------------|---------------|  
|01-01-20|3|10|1|1|  
|02-01-20|-1|-3.33|2|2|  
|03-01-20|-1|-3.33|3|3|  
|04-01-20|-1|-3.33|4|4|  
|01-01-20|0|-0.01|1|5|  

## Siehe auch  
 [Designdetails: Lagerkostenberechnung](design-details-inventory-costing.md)   
 [Designdetails: Kostenregulierung](design-details-cost-adjustment.md)   
 [Designdetails: Kostenmethoden](design-details-costing-methods.md) [Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)  
 [Finanzen](finance.md)  
 [Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]