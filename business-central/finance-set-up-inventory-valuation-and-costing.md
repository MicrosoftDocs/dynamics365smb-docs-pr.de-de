---
title: Einrichten der Lagerwertberechnung und der Kostenrechnung | Microsoft Docs
description: "In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: af4c256b59739abce9ec22bce254fe8e2dff4e29
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-inventory-valuation-and-costing"></a>Einrichten der Lagerwertberechnung und der Kostenrechnung
Um sicherzustellen, dass Lagerregulierungen ordnungsgemäß aufgezeichnet werden, müssen Sie verschiedene Felder und Fenster einrichten, bevor Sie Artikeltransaktionen durchführen können.

In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.

|**Aufgabe**|**Siehe**|  
|------------|-------------|  
|Festlegen einer Lagerabgangsmethode für jeden Artikel, um zu steuern, wie dessen eingehende Kosten zum Ermitteln des Lagerwerts und der Kosten für verkaufte Waren verwendet werden sollen|[Neue Artikel registrieren](inventory-how-register-new-items.md)|  
|Sicherstellen, dass Kosten beim Buchen einer Lagertransaktion automatisch in die Finanzbuchhaltung gebucht werden|Wählen Sie im Fenster **Lagereinrichtung** das Feld **Automatische Lagerbuchung**.|  
|Sicherstellen, dass die Soll-Kosten in die Finanzbuchhaltung gebucht werden, um in den Interimssachkonten vor der eigentlichen Buchung eine Schätzung der fälligen Beträge und der Kosten der gehandelten Waren anzuzeigen|Wählen Sie im Fenster **Lagereinrichtung** das Feld **Soll-Kosten buchen**.|  
|Einrichten der automatischen Regulierung von Kostenänderungen beim Buchen von Lagertransaktionen|[Artikelpreise justieren](inventory-how-adjust-item-costs.md)|  
|Festlegen, ob der durchschnittliche Einstandspreis nur pro Artikel oder pro Artikel für alle Lagerhaltungsdaten sowie für jede Variante des Artikels berechnet werden soll|Wählen Sie im Fenster **Lagereinrichtung** das Feld **Einst.-Pr.(durchschn.)Ber.-Art**.|  
|Auswählen des gewünschten Zeitraums für die Berechnung der gewichteten Durchschnittskosten von Artikeln, für die die Durchschnittskostenmethode verwendet wird|Wählen Sie im Fenster **Lagereinrichtung** das Feld **Durchschnittskostenperiode**.|  
|Definieren der Lagerbuchungsperioden zum Steuern des Lagerwerts im Zeitverlauf durch Sperren der Buchung von Transaktionen in geschlossenen Lagerbuchungsperioden|[Arbeiten mit Lagerbuchungsperioden](finance-how-to-work-with-inventory-periods.md)|  
|Sicherstellen, dass Verkaufsreklamationen mit der ursprünglichen ausgehenden Transaktion ausgeglichen werden, um den Lagerwert zu erhalten.|Das Feld **Einst.-Pr.-Rückverfolg. notw.** im Fenster **Debitoren & Verkauf**|  
|Sicherstellen, dass Einkaufsreklamationen mit der ursprünglichen eingehenden Transaktion ausgeglichen werden, um den Lagerwert zu erhalten.|Das Feld **Einst.-Pr.-Rückverfolg. notw.** im Fenster **Kreditoren & Einkauf**|
|Einrichten der Rundungsregeln, die beim Regulieren oder Vorschlagen von Artikelpreisen sowie beim Regulieren oder Vorschlagen von Einstandspreisen angewendet werden|**Rundungsmethode**|  

## <a name="see-also"></a>Siehe auch  
[Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)  
[Arbeiten mit  Business Central](ui-work-product.md)  
[Finanzen](finance.md)  

