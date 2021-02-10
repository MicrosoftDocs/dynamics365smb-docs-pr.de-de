---
title: Erstellen Sie Neuwert-Posten für Artikel im Lagerbestand| Microsoft Docs
description: Beschreiben Sie, wie der Wert eines oder mehrerer Artikel im Lager abgeschrieben oder neu bewertet wird, indem Sie den aktuellen, berechneten Wert buchen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2bcd09876f18bb948e060b06199d3d36facaa83f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750055"
---
# <a name="revalue-inventory"></a>Neubewerten von Lagerbestand
Wenn Sie den Lagerwert eines Artikels oder den eines bestimmten Artikelpostens nach oben oder unten verändern möchten, müssen Sie das Neubewertungs Buch.-Blatt verwenden.

## <a name="to-revalue-inventory"></a>Neubewerten von Lagerbestand
1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Bewertungs Buch.-Blatt** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Lagerwert berechnen** aus.
3. Füllen Sie auf der Seite **Lagerwert berechnen** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wählen Sie die Schaltfläche **OK** aus.
5. In jeder Zeile auf der Seite **Neubewertungs-Blatt-Blatt** im Feld **Einheitskosten (neu bewertet)** geben Sie den neuen Einstandspreis ein. Oder geben Sie den Gesamtbetrag im Feld **Lagerwert (neu bewertet)** ein.

    Die entsprechenden Felder werden automatisch aktualisiert. Beachten Sie, dass das Feld **Betrag** die tatsächliche Änderung des Lagerwertes für den ausgewählten Artikelposten zeigt. Es berechnet die Differenz zwischen den Feldern **Lagerwert (berechnet)** und **Lagerwert (neu bewertet)**.
6. Wenn Sie das Einlagern der Artikel abgeschlossen haben, wählen Sie die Aktion **Buchen** aus.

Neue Wertposten werden nun erstellt, um die Neubewertungen abzubilden, die Sie gebucht haben. Sie können die neuen Werte in der entsprechenden Artikelkarten sehen.

## <a name="see-also"></a>Siehe auch
[Designdetails: Neubewertung](design-details-revaluation.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Verkauf](sales-manage-sales.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
