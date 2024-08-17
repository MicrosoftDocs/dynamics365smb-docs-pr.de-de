---
title: Einrichten der Bestandsbewertung und -kalkulation
description: 'Um sicherzustellen, dass Lagerregulierungen ordnungsgemäß aufgezeichnet werden, müssen Sie verschiedene Felder und Seiten einrichten, bevor Sie Artikeltransaktionen durchführen können.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 07/29/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="set-up-inventory-valuation-and-costing"></a>Einrichten der Bestandsbewertung und -kalkulation

Um sicherzustellen, dass Lagerregulierungen ordnungsgemäß aufgezeichnet werden, müssen Sie verschiedene Felder und Seiten einrichten, bevor Sie Artikeltransaktionen durchführen können. In der Regel wählen Unternehmen eine bestimmte Lagerabgangsmethode und wenden diese auf Lagerartikel an, beispielsweise um den Wert von auf Lager befindlichen Artikel besser nachzuverfolgen.  

> [!TIP]
> Für eine Einführung in die Nachkalkulation in [!INCLUDE [prod_short](includes/prod_short.md)] betrachten Sie [Informationen zur Bestandskalkulation](finance-learn-about-costing.md).

Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Artikeln, die sie beschreiben.

|**Bis**|**Siehe**|  
|------------|-------------|
|Geben Sie eine standardmäßige Lagerabgangsmethode für das Unternehmen an, um zu steuern, wie eingehende Kosten zum Ermitteln des Lagerwerts und der Kosten für verkaufte Waren verwendet werden.|[So richten Sie allgemeine Lagerbestandsinformationen ein](inventory-how-setup-general.md)|  
|Geben Sie eine Lagerabgangsmethode für einzelne Artikel an, wenn für sie eine andere Lagerabgangsmethode erforderlich ist.|[Neue Artikel registrieren](inventory-how-register-new-items.md)|  
|Sicherstellen, dass Kosten beim Buchen einer Lagertransaktion automatisch in die Finanzbuchhaltung gebucht werden|Wählen Sie auf der Seite **Lagereinrichtung** das Feld **Automatische Lagerbuchung**.|  
|Stellen Sie sicher, dass die erwarteten Kosten im Hauptbuch gebucht werden, um anhand der vorläufigen Sachkonten eine Schätzung der fälligen Beträge und der Kosten der gehandelten Artikel zu erhalten, bevor diese in Rechnung gestellt werden.|Wählen Sie auf der Seite **Lagereinrichtung** das Feld **Soll-Kosten buchen**.|  
|Einrichten der automatischen Regulierung von Kostenänderungen beim Buchen von Lagertransaktionen|[Artikelpreise justieren](inventory-how-adjust-item-costs.md)|  
|Definieren Sie, ob der Einstandspreis (durchschn.) nur pro Artikel oder pro Artikel für jede Lagermengeneinheit und für jede Variante des Artikels berechnet werden soll.|Wählen Sie auf der Seite **Lagereinrichtung** das Feld **Einst.-Pr.(durchschn.)Ber.-Art**.|  
|Auswählen des gewünschten Zeitraums für die Berechnung der gewichteten Durchschnittskosten von Artikeln, für die die Durchschnittskostenmethode verwendet wird, angewendet werden soll.|Wählen Sie auf der Seite **Lagereinrichtung** das Feld **Durchschnittskostenperiode**.|  
|Definieren der Lagerbuchungsperioden zum Steuern des Lagerwerts im Zeitverlauf durch Sperren der Buchung von Transaktionen in geschlossenen Lagerbuchungsperioden|[Arbeiten mit Lagerbuchungsperioden](finance-how-to-work-with-inventory-periods.md)|  
|Sicherstellen, dass Verkaufsreklamationen mit der ursprünglichen ausgehenden Transaktion ausgeglichen werden, um den Lagerwert zu erhalten.|Das Feld **Einst.-Pr.-Rückverfolg. notw.** auf der Seite **Debitoren & Verkauf**|  
|Sicherstellen, dass Einkaufsreklamationen mit der ursprünglichen eingehenden Transaktion ausgeglichen werden, um den Lagerwert zu erhalten.|Das Feld **Exakte Einstandspreisstornierung notwendig** auf der Seite **Kreditoren und Einkauf**|
|Einrichten der Rundungsregeln, die beim Regulieren oder Vorschlagen von Artikelpreisen sowie beim Regulieren oder Vorschlagen von Einstandspreisen angewendet werden|**Rundungsmethode**|  

## <a name="see-also"></a>Siehe auch

[Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)    
[Allgemeine Bestandsinformationen einrichten](inventory-how-setup-general.md)    
[Abgleich der Lagerkosten mit dem Hauptbuch](finance-how-to-post-inventory-costs-to-the-general-ledger.md)    
[Best Practices für die Einrichtung: Kostenrechnungsmethode](setup-best-practices-costing-method.md)    
[Designdetails: Bestandskalkulation](design-details-inventory-costing.md)    
[Designdetails: Ändern der Kostenmethode für Artikel](design-details-changing-costing-methods.md)    
[Arbeiten mit Business Central](ui-work-product.md)    
[Finanzen](finance.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]
