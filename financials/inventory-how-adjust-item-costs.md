---
title: Manuelles Anpassen von Artikelkosten| Microsoft Docs
description: "Sie können die Lagerbewertung eines Artikels anpassen, indem Sie die FIFO. oder \" Standard \"oder Durchschnittskostenmethode anwenden, z. B. wenn Artikelkosten für Gründe, die keine Transaktionen betreffen, ändern."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost adjustment, cost forwarding, costing method, inventory valuation, costing
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: a1f682b60b7b9ae402c27093f13aa3db2368ed5b
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-adjust-item-costs-manually"></a>So regulieren Sie Artikelpreise manuell
Die Kosten eines Artikels (Lagerwert), den Sie ein- und später verkaufen, ändert sich im Laufe der Nutzungsdauer, weil beispielsweise Frachtkosten dem Kaufpreis hinzugefügt werden, nachdem Sie den Artikel verkauft haben. Dies ist insbesondere dann wichtig, wenn Sie Waren verkaufen, bevor der Kauf dieser Waren in Rechnung gestellt wurde. Um immer den richtigen Lagerwert zu kennen, müssen Artikelkosten daher regelmäßig reguliert werden. Dadurch ist sichergestellt, dass die Verkaufs- und Gewinnstatistiken auf dem neuesten Stand sind und die finanziellen Kennziffern korrekt sind.

In [!INCLUDE[d365fin](includes/d365fin_md.md)], werden Artikelkosten automatisch jedes Mal reguliert, wenn eine Lagertransaktion auftritt, beispielsweise, wenn Sie eine Einkaufsrechnung für einen Artikel buchen.

Sie können eine Funktion verwenden, um die Kosten einer oder mehrerer Artikel manuell anzupassen. Dies ist beispielsweise dann nützlich, wenn Sie wissen, dass Sie die Artikelpreise aufgrund anderer Ursachen als Artikeltransaktionen geändert haben.

Artikelkosten werden durch die FIFO- oder Durchschnittskostenmethode, abhängig von Ihrer Auswahl in **Mein Unternehmen** reguliert. Weitere Informationen finden Sie unter [Vorbereitungen für das Ausführen von Geschäften](ui-get-ready-business.md).  

Wenn Sie die FIFO-Kostenmethode verwenden, dass ist der Einstandspreis eines Artikels der tatsächliche Wert jedes Eingangs des Artikels. Bestand wird mit der Annahme bewertet, dass dess erste Artikel im Lager zuerst verkauft wird.

Wenn Sie die Durchschnittskostenmethode verwenden, dass werden die Einstandskosten als Durchschnittskosten nach dem Kauf berechnet. Bestand wird mit der Annahme bewertet, dass aller Bestand gleichzeitig verkauft wird.

Die Kostenregulierungsfunktion verarbeitet nur Wertposten, die noch nicht reguliert wurden. Liegt eine Situation vor, in der geänderte eingehende Kosten an zugehörige ausgehende Posten weitergeleitet werden müssen, werden dafür neue Regulierungswertposten erstellt, die zwar auf den Informationen der ursprünglichen Wertposten basieren, aber den Regulierungsbetrag enthalten. Die Kostenregulierungsfunktion verwendet das Buchungsdatum des ursprünglichen Wertpostens in den Regulierungsposten, es sei denn, das Datum befindet sich in einer geschlossenen Lagerbuchungsperiode. In diesem Fall wird das Startdatum der nächsten offenen Lagerbuchungsperiode verwendet. Werden keine Lagerbuchungsperioden verwendet, definiert das Datum im Feld **Buchungen zugel. ab** im Fenster **Finanzbuchhaltung Einrichtung**, wann der Regulierungsposten gebucht wird.

Änderungen im Lagerwert vom Handel werden automatisch mit den Finanzbüchern Artikeltransaktionen ausgeglichen, wenn Sie buchen. Weitere Informationen finden Sie im "Abschnitt "Lagerabstimmung unter [Bestand](inventory-manage-inventory.md).

## <a name="to-adjust-item-costs-manually"></a>So regulieren Sie Artikelpreise manuell
1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Kosten anpassen - Artikeleinträge** ein. Wählen Sie dann den zugehörigen Link aus.
2. Im Fenster **Lagerreg. fakt. Einst. Preise** geben Sie an, für welche Artikel die Kosten anzupassen sind.
3. Wählen Sie die Schaltfläche **OK** aus.

## <a name="see-also"></a>Siehe auch
[Lagerbest](inventory-manage-inventory.md)  
[Verkauf](sales-manage-sales.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

