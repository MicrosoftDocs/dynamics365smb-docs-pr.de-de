---
title: 'Gewusst wie: Besondere Einkaufspreise und Rabatte aufzeichnen| Microsoft Docs'
description: 'Gewusst wie: Verkaufspreise und Rabatte aufzeichnen'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 67625231d62a72bb0a62ab362bce92aa16b8956e
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# Gewusst wie: Besondere Verkaufspreise und Rabatte aufzeichnen
<a id="how-to-record-special-purchase-prices-and-discounts" class="xliff"></a>
Definieren Sie die verschiedenen Preis- und Rabattvereinbarungen, die beim Artikeleinkauf von unterschiedlichen Kreditoren gelten, damit die vereinbarten Regeln und Werte auf die für den Kreditor erstellten Einkaufsbelege angewendet werden.

Falls Sie spezielle Preise und Zeilenrabatte für Verkäufe und Einkäufe erfasst haben, stellt [!INCLUDE[d365fin](includes/d365fin_md.md)] sicher, dass der Deckungsbeitrag im Artikelhandel immer optimal ist, indem er die besten Preise automatisch in Einkaufs- und Verkaufsbelegen und auf Projekt und Artikel Buch.-Blattzeilen berechnet. Weitere Informationen finden Sie unter [Erweitert: Beste Preise berechnen](advanced-best-price-calculation.md).

Für die Preise können Sie besondere auf den Einkaufszeilen verschiedene Einkaufspreise einfügen, wenn eine bestimmte Kombination aus Kreditor, Artikel, Mindestmenge, Einheit oder des Start-/Enddatum vorhanden ist.

Für die Rabatte können Sie zwei Arten von Einkaufsrabatten einrichten und verwenden:

| Rabattart | Beschreibung |
| --- | --- |
| **Einkaufszeilenrabatt** |Ein Betrag mit Rabatt wird auf den Einkaufszeilen eingefügt, wenn eine bestimmte Kombination aus Kreditor, Artikel, Mindestmenge, Einheit oder des Start-/Enddatum vorhanden ist. Diese Funktionalität gilt auf gleiche Weise für Einkaufsbelege. |
| **Rechnungsrabatt** |Ein prozentualer Rabatt, der gewährt wird, wenn der Wertbetrag aller Zeilen eines Einkaufsbelegs einen bestimmten Mindestwert übersteigt. |

Da Einkaufszeilenrabatte und Einkaufspreise auf einer Kombination aus Artikel und Kreditor basieren, kann diese Konfiguration auch auf der Artikelkarte erfolgen, auf der die Regeln und Werte definiert sind. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten neuer Artikel](inventory-how-register-new-items.md).

## Einen Speziellen Einkaufspreis für einen Kreditor einrichten
<a id="to-set-up-a-special-purchase-price-for-a-vendor" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Kreditoren** ein und wählen Sie dann den entsprechenden Link aus.
2. Öffnen Sie die relevante Kreditorenkarte, und klicken Sie dann auf die Aktion **Preise**.

    Das **Einkaufstyp**-Feld ist mit **Kreditor** vorausgefüllt und das Feld **Einkaufscode** ist mit der Kreditorennummer vorausgefüllt.
3. Füllen Sie die Felder in der Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Füllen Sie eine Zeile für jede Kombination aus, für die Sie dem Kreditor einen Einkaufszeilenrabatt gewähren.

## Um einen Zeilenrabatt für einen Kreditor einzurichten
<a id="to-set-up-a-line-discount-for-a-vendor" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Kreditoren** ein und wählen Sie dann den entsprechenden Link aus.
2. Öffnen Sie die relevante Kreditorenkarte, und klicken Sie dann auf die Aktion **Zeilenrabatte**.

    Das **Einkaufstyp**-Feld ist mit **Kreditor** vorausgefüllt und das Feld **Einkaufscode** ist mit der Kreditorennummer vorausgefüllt.
3. Füllen Sie die Felder in der Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Füllen Sie eine Zeile für jede Kombination aus, für die Sie dem Kreditor einen Einkaufszeilenrabatt gewähren.

## Um einen Rechnungsrabatt für einen Kreditor einzurichten
<a id="to-set-up-an-invoice-discount-for-a-vendor" class="xliff"></a>
Wenn Ihre Kreditoren Sie informiert haben, welche Rechnungsrabatte sie gewähren, können Sie den Rechnungsrabattcode auf den Kreditorenkarten eingeben und Bedingungen für jeden Code einrichten.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Kreditoren** ein und wählen Sie dann den entsprechenden Link aus.
2. Öffnen Sie die Kreditorenkarte für einen Kreditor, der für Rechnungsrabatte in Frage kommt.
3. Geben Sie im Feld **Rechnungsrabattcode** einen Code für die jeweilige Rechnungsrabattbedingungen ein, die zur Berechnung der Rabatte für den Kreditor verwendet werden sollen.

    **Hinweis**: Rechnungsrabattcodes werden durch vorhandene Kreditorenkarten dargestellt. Dies ermöglicht es Ihnen, Rechnungsrabattbedingungen schnell einem Kreditor zuzuweisen, indem es den Namen eines anderen Kreditors mit den selben Konditionen auswählt.

    Fahren Sie fort, um neue Einkaufssrechnungsrabatt-Bedingungen einzurichten.
4. Im Fenster **Kreditorenkarte** wählen Sie die Aktion **Rechnungsrabatt** aus. Das Fenster **Kreditorenrechnungsrabatte** wird geöffnet.
5. Geben Sie in dem Feld **Währungscode** den Code für die Währung ein, für die die Rechnungsrabattkonditionen gelten sollen. Wenn Sie Rechnungsrabattbedingungen in EUR einrichten möchten, dann lassen Sie das Feld leer.
6. Geben Sie im Feld **Minimalbetrag** den Mindestbetrag ein, den eine Rechnung aufweisen muss, um für einen Rabatt in Frage zu kommen.
7. Geben Sie im Feld **Rabatt** den Rechnungsrabatt als Prozentsatz des Rechnungsbetrages ein.
8. Wiederholen Sie die Schritte 5 bis 7 für jede Währung, für die der Kreditor einen Rechnungsrabatt erhält.

Der Rechnungsrabatt wird jetzt eingerichtet und dem fraglichen Kreditor zugewiesen. Wenn Sie den Kreditorencode im Feld **Rechnungs-Rabattcode** für andere Kreditorenkarten auswählen, wird derselbe Rechnungsrabatt diesen Kreditor zugewiesen.

## Siehe auch
<a id="see-also" class="xliff"></a>
[Erweitert: Beste Preiskalkulation](advanced-best-price-calculation.md)  
[Einkaufeinrichten](purchasing-setup-purchasing.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

