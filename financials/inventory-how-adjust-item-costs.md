---
title: 'Vorgehensweise: Manuelles Anpassen von Artikelkosten| Microsoft Docs'
description: 'Gewusst wie: Artikelpreise anpassen'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost adjustment, cost forwarding, costing method, inventory valuation, costing
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 00b5ac40bd0d3df346618b57173df67daba6c7fc
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# So regulieren Sie Artikelpreise manuell
<a id="how-to-adjust-item-costs-manually" class="xliff"></a>
Die Kosten eines Artikels (Lagerwert), den Sie ein- und später verkaufen, ändert sich im Laufe der Nutzungsdauer, weil beispielsweise Frachtkosten dem Kaufpreis hinzugefügt werden, nachdem Sie den Artikel verkauft haben. Dies ist insbesondere dann wichtig, wenn Sie Waren verkaufen, bevor der Kauf dieser Waren in Rechnung gestellt wurde. Um immer den richtigen Lagerwert zu kennen, müssen Artikelkosten daher regelmäßig reguliert werden. Dadurch ist sichergestellt, dass die Verkaufs- und Gewinnstatistiken auf dem neuesten Stand sind und die finanziellen Kennziffern korrekt sind.

In [!INCLUDE[d365fin](includes/d365fin_md.md)], werden Artikelkosten automatisch jedes Mal reguliert, wenn eine Lagertransaktion auftritt, beispielsweise, wenn Sie eine Einkaufsrechnung für einen Artikel buchen.

Sie können eine Funktion verwenden, um die Kosten einer oder mehrerer Artikel manuell anzupassen. Dies ist beispielsweise dann nützlich, wenn Sie wissen, dass Sie die Artikelpreise aufgrund anderer Ursachen als Artikeltransaktionen geändert haben.

**Hinweis**: Artikelkosten werden nur durch die FIFO-Lagerabgangsmethode reguliert. Das bedeutet, dass der Einstandspreis eines Artikels der tatsächliche Wert jedes möglichen Eingangs des Artikels ist und dass das Lager mit der Annahme validiert wird, dass die ersten Artikel im Bestand zuerst verkauft werden.

Die Kostenregulierungsfunktion verarbeitet nur Wertposten, die noch nicht reguliert wurden. Liegt eine Situation vor, in der geänderte eingehende Kosten an zugehörige ausgehende Posten weitergeleitet werden müssen, werden dafür neue Regulierungswertposten erstellt, die zwar auf den Informationen der ursprünglichen Wertposten basieren, aber den Regulierungsbetrag enthalten. Die Kostenregulierungsfunktion verwendet das Buchungsdatum des ursprünglichen Wertpostens in den Regulierungsposten, es sei denn, das Datum befindet sich in einer geschlossenen Lagerbuchungsperiode. In diesem Fall wird das Startdatum der nächsten offenen Lagerbuchungsperiode verwendet. Werden keine Lagerbuchungsperioden verwendet, definiert das Datum im Feld **Buchungen zugel. ab** im Fenster **Finanzbuchhaltung Einrichtung**, wann der Regulierungsposten gebucht wird.

Änderungen im Lagerwert vom Handel werden automatisch mit den Finanzbüchern Artikeltransaktionen ausgeglichen, wenn Sie buchen. Weitere Informationen finden Sie unter [Erweiterte Lagerabstimmung](advanced-inventory-reconciliation.md).

## So regulieren Sie Artikelpreise manuell
<a id="to-adjust-item-costs-manually" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das **Symbol Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Kostenartikeleingaben anpassen** ein und wählen Sie dann den entsprechenden Link aus.
2. Im Fenster **Lagerreg. fakt. Einst. Preise** geben Sie an, für welche Artikel die Kosten anzupassen sind.
3. Wählen Sie die Schaltfläche **OK** aus.

## Siehe auch
<a id="see-also" class="xliff"></a>
[Erweiterte: Bestandabgleich](advanced-inventory-reconciliation.md)  
[Lagerbesttand](inventory-manage-inventory.md)  
[Verkauf](sales-manage-sales.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

