---
title: Einrichten der Lagerwertberechnung und der Kostenrechnung | Microsoft Docs
description: "Die folgende Tabelle enthält eine Abfolge von Aufgaben sowie Links zu den entsprechenden Themen, in denen diese Aufgaben erläutert werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: aa5ee6d9942390a2b4ad0aa8787172b0f7b141d0
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-inventory-valuation-and-costing"></a>Einrichten der Lagerwertberechnung und der Kostenrechnung
Um sicherzustellen, dass Lagerregulierungen ordnungsgemäß aufgezeichnet werden, müssen Sie verschiedene Felder und Fenster einrichten, bevor Sie Artikeltransaktionen durchführen können.

Die folgende Tabelle enthält eine Abfolge von Aufgaben sowie Links zu den entsprechenden Themen, in denen diese Aufgaben erläutert werden.

|**Aufgabe**|**Siehe**|  
|------------|-------------|  
|Festlegen einer Lagerabgangsmethode für jeden Artikel, um zu steuern, wie dessen eingehende Kosten zum Ermitteln des Lagerwerts und der Kosten für verkaufte Waren verwendet werden sollen|[Vorgehensweise: Neue Artikel registrieren](inventory-how-register-new-items.md)|  
|Sicherstellen, dass Kosten beim Buchen einer Lagertransaktion automatisch in die Finanzbuchhaltung gebucht werden|Wählen Sie im Fenster **Lagereinrichtung** das Feld **Automatische Lagerbuchung**.|  
|Sicherstellen, dass die Soll-Kosten in die Finanzbuchhaltung gebucht werden, um in den Interimssachkonten vor der eigentlichen Buchung eine Schätzung der fälligen Beträge und der Kosten der gehandelten Waren anzuzeigen|Wählen Sie im Fenster **Lagereinrichtung** das Feld **Soll-Kosten buchen**.|  
|Einrichten der automatischen Regulierung von Kostenänderungen beim Buchen von Lagertransaktionen|[Gewusst wie: Artikelpreise anpassen](inventory-how-adjust-item-costs.md)|  
|Festlegen, ob der durchschnittliche Einstandspreis nur pro Artikel oder pro Artikel für alle Lagerhaltungsdaten sowie für jede Variante des Artikels berechnet werden soll|Wählen Sie im Fenster **Lagereinrichtung** das Feld **Einst.-Pr.(durchschn.)Ber.-Art**.|  
|Auswählen des gewünschten Zeitraums für die Berechnung der gewichteten Durchschnittskosten von Artikeln, für die die Durchschnittskostenmethode verwendet wird|Wählen Sie im Fenster **Lagereinrichtung** das Feld **Durchschnittskostenperiode**.|  
|Definieren der Lagerbuchungsperioden zum Steuern des Lagerwerts im Zeitverlauf durch Sperren der Buchung von Transaktionen in geschlossenen Lagerbuchungsperioden|[Vorgehensweise: Arbeiten mit Lagerbuchungsperioden](finance-how-to-work-with-inventory-periods.md)|  
|Sicherstellen, dass Verkaufsreklamationen mit der ursprünglichen ausgehenden Transaktion ausgeglichen werden, um den Lagerwert zu erhalten.|Das Feld **Einst.-Pr.-Rückverfolg. notw.** im Fenster **Debitoren & Verkauf**|  
|Sicherstellen, dass Einkaufsreklamationen mit der ursprünglichen eingehenden Transaktion ausgeglichen werden, um den Lagerwert zu erhalten.|Das Feld **Einst.-Pr.-Rückverfolg. notw.** im Fenster **Kreditoren & Einkauf**|
|Einrichten der Rundungsregeln, die beim Regulieren oder Vorschlagen von Artikelpreisen sowie beim Regulieren oder Vorschlagen von Einstandspreisen angewendet werden|**Rundungsmethode**|  

## <a name="see-also"></a>Siehe auch  
[Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)  
[Arbeiten mit Financials](ui-work-product.md)  
[Finanzen](finance.md)  

