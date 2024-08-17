---
title: Neue Wertposten für Artikel im Lagerbestand erstellen| Microsoft Docs
description: 'Beschreibt, wie Sie die Werteinträge eines oder mehrerer Artikel im Bestand aufwerten oder abschreiben, indem Sie deren aktuellen, berechneten Wert buchen.'
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'costing, inventory cost, value entries'
ms.search.forms: '5803,'
ms.date: 07/29/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Lagerbestand neu bewerten
Wenn Sie den Lagerwert eines Artikels oder den eines bestimmten Artikelpostens nach oben oder unten verändern möchten, müssen Sie das Neubewertungs Buch.-Blatt verwenden.

## Neubewerten von Lagerbestand
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Neubewertungs Buch.-Blatt** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Lagerwert berechnen** aus.
3. Füllen Sie auf der Seite **Lagerwert berechnen** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wählen Sie die Schaltfläche **OK**.
5. Geben Sie in jeder Zeile auf der Seite  **Artikelneubewertungsjournale**  im Feld  **Stückpreis (Neubewertet)**  den neuen Stückpreis ein. Oder geben Sie den Gesamtbetrag im Feld **Lagerwert (neu bewertet)** ein.

    Die entsprechenden Felder werden automatisch aktualisiert. Im Feld  **Betrag**  wird die tatsächliche Bestandswertänderung für den ausgewählten Artikelposten angezeigt. Es berechnet die Differenz zwischen den Feldern **Lagerwert (berechnet)** und **Lagerwert (neu bewertet)**.
6. Wenn Sie das Einlagern der Artikel abgeschlossen haben, wählen Sie die Aktion **Buchen** aus.

Neue Wertposten werden nun erstellt, um die Neubewertungen abzubilden, die Sie gebucht haben. Sie können die neuen Werte in der entsprechenden Artikelkarten sehen.

## Siehe auch
[Designdetails: Neubewertung](design-details-revaluation.md)    
[Lagerbest](inventory-manage-inventory.md)    
[Verkauf](sales-manage-sales.md)    
[Einkauf](purchasing-manage-purchasing.md)    
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]