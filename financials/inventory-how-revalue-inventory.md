---
title: "Erstellen Sie Neuwert-Posten für Artikel im Lagerbestand| Microsoft Docs"
description: Beschreiben Sie, wie der Wert eines oder mehrerer Artikel im Lager abgeschrieben oder neu bewertet wird, indem Sie den aktuellen, berechneten Wert buchen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 1935f53db068047921e44109cd4b23bbb51f0890
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-revalue-inventory"></a>Vorgehensweise: Neubewerten von Lagerbestand
Wenn Sie den Lagerwert eines Artikels oder den eines bestimmten Artikelpostens nach oben oder unten verändern möchten, müssen Sie das Neubewertungs Buch.-Blatt verwenden.

## <a name="to-revalue-inventory"></a>Neubewerten von Lagerbestand
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen")und geben **Neubewertung Buch.-Blatt** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Lagerwert berechnen** aus.
3. Füllen Sie im Fenster **Lagerwert berechnen** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wählen Sie die Schaltfläche **OK** aus.
5. In jeder Zeile im Fenster **Neubewertungs-Blatt-Blatt** im Feld **Einheitskosten (neu bewertet)** geben Sie den neuen Einstandspreis ein. Oder geben Sie den Gesamtbetrag im Feld **Lagerwert (neu bewertet)** ein.

    Die entsprechenden Felder werden automatisch aktualisiert. Beachten Sie, dass das Feld **Betrag** die tatsächliche Änderung des Lagerwertes für den ausgewählten Artikelposten zeigt. Es berechnet die Differenz zwischen den Feldern **Lagerwert (berechnet)** und **Lagerwert (neu bewertet)**.
6. Wenn Sie das Einlagern der Artikel abgeschlossen haben, wählen Sie die Aktion **Buchen** aus.

Neue Wertposten werden nun erstellt, um die Neubewertungen abzubilden, die Sie gebucht haben. Sie können die neuen Werte in der entsprechenden Artikelkarten sehen.

## <a name="see-also"></a>Siehe auch
[Lagerbest](inventory-manage-inventory.md)  
[Verkauf](sales-manage-sales.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

