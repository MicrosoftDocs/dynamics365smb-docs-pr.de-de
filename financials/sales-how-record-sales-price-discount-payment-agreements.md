---
title: 'Gewusst wie: Besondere Verkaufspreise und Rabatte aufzeichnen| Microsoft Docs'
description: 'Gewusst wie: Besondere Verkaufspreise und Rabatte aufzeichnen'
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
ms.openlocfilehash: 5ceddded2f95e15a6a7449bf2776b7776ce8a55c
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# Gewusst wie: Besondere Verkaufspreise und Rabatte aufzeichnen
<a id="how-to-record-special-sales-prices-and-discounts" class="xliff"></a>
Die unterschiedlichen Preis- und Zahlungsrichtlinien, die beim Verkauf an verschiedene Debitoren gelten, müssen so definiert werden, dass die vereinbarten Regeln und Werte für Verkaufsbelege übernommen werden, die für den Debitor erstellt werden.

Falls Sie spezielle Preise und Zeilenrabatte für Verkäufe und Einkäufe erfasst haben, stellt [!INCLUDE[d365fin](includes/d365fin_md.md)] sicher, dass der Deckungsbeitrag im Artikelhandel immer optimal ist, indem er die besten Preise automatisch in Einkaufs- und Verkaufsbelegen und auf Projekt und Artikel Buch.-Blattzeilen berechnet. Weitere Informationen finden Sie unter [Erweitert: Beste Preise berechnen](advanced-best-price-calculation.md).

Für die Preise können Sie besondere auf den Verkaufszeilen verschiedene Verkaufspreise einfügen, wenn eine bestimmte Kombination aus Debitor, Artikel, Mindestmenge, Einheit oder des Start-/Enddatum vorhanden ist.

Für die Rabatte können Sie zwei Arten von Verkaufsrabatten einrichten und verwenden:

| Rabattart | Beschreibung |
| --- | --- |
| **Verkaufszeilenrabatt** |Ein Betrag mit Rabatt wird auf den Verkaufszeilen eingefügt, wenn eine bestimmte Kombination aus Debitor, Artikel, Mindestmenge, Einheit oder des Start-/Enddatum vorhanden ist. Diese Funktionalität gilt auf gleiche Weise für Verkaufsbelege. |
| **Rechnungsrabatt** |Ein prozentualer Rabatt, der gewährt wird, wenn der Wertbetrag aller Zeilen eines Einkaufsbelegs einen bestimmten Mindestwert übersteigt. |

Da Verkaufszeilenrabatte und Verkaufspreise auf einer Kombination aus Artikel und Debitor bestehen, können Sie diese Konfiguration auch auf der Artikelkarte des Artikels eingerichtet werden, für den die Regeln und Werte gelten.

## Um Verkaufspreise für einen Debitor zu erstellen:
<a id="to-set-up-a-sales-price-for-a-customer" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Kreditoren** ein und wählen Sie dann den entsprechenden Link aus.
2. Öffnen Sie die entsprechende Debitorenkarte und klicken dann auf **Preise**.

    Das Feld **Verkaufsart** ist mit dem Code **Debitor** ausgefüllt und das Feld **Verkaufscode** enthält die Nummer des Debitoren.
3. Füllen Sie die Felder in der Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Füllen Sie eine Zeile für jede Kombination aus, die dem Debitor einen besonderen Preis gewährt.

## So erstellen Sie Verkaufszeilenrabatte für einen Debitor:
<a id="to-set-up-a-sales-line-discount-for-a-customer" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen") . Geben Sie **Kreditoren** ein und wählen Sie dann den entsprechenden Link aus.
2. Öffnen Sie die entsprechende Debitorenkarte und klicken dann auf **Zeilenpreise**.

    Das Feld **Verkaufsart** ist mit dem Code **Debitor** ausgefüllt und das Feld **Verkaufscode** enthält die Nummer des Debitoren.
3. Füllen Sie die Felder in der Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Füllen Sie eine Zeile für jede Kombination aus, die dem Debitor einen besonderen Preis gewährt.

## Um Rechnungsrabattkonditionen für Einkäufe einzurichten:
<a id="to-set-up-an-invoice-discount-for-a-customer" class="xliff"></a>
Nachdem Sie sich entschieden haben, welche Debitoren für Rechnungsrabatte in Frage kommen, geben Sie die Rechnungsrabattcodes auf den Debitorenkarten ein, und richten Sie die Bedingungen für die einzelnen Codes ein.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen") . Geben Sie **Kreditoren** ein und wählen Sie dann den entsprechenden Link aus.
2. Öffnen Sie die Debitorenkarte für einen Debitor, der für Rechnungsrabatte in Frage kommt.
3. Geben Sie im Feld **Rechnungsrabattcode** einen Code für das jeweilige Rechnungsrabattfenster ein, das die Anwendung verwenden soll, um Rechnungsrabatte für den Debitor zu berechnen.

    **Hinweis**: Rechnungsrabattcodes werden durch Bestandskundenkarten dargestellt. Dies ermöglicht es Ihnen, Rechnungsrabattbedingungen schnell einem Debitor zuzuweisen, indem es den Namen eines anderen Debitors mit den selben Konditionen auswählt.

    Fahren Sie fort, um neue Verkaufsrechnungsrabatt-Bedingungen einzurichten.
4. Im Fenster **Debitorenkarte** wählen Sie die Aktion **Rechnungsrabatt** aus. Das Fenster **Debitorenrechnungsrabatte** wird geöffnet.
5. Geben Sie in dem Feld **Währungscode** den Code für die Währung ein, für die die Rechnungsrabattkonditionen gelten sollen. Wenn Sie Rechnungsrabattbedingungen in EUR einrichten möchten, dann lassen Sie das Feld leer.
6. Geben Sie im Feld **Minimalbetrag** den Mindestbetrag ein, den eine Rechnung aufweisen muss, um für einen Rabatt in Frage zu kommen.
7. Geben Sie im Feld **Rabatt** den Rechnungsrabatt als Prozentsatz des Rechnungsbetrages ein.
8. Wiederholen Sie die Schritte 5 bis 7 für jede Währung, für die der Debitor einen Rechnungsrabatt erhält.

Der Rechnungsrabatt wird jetzt eingerichtet und dem fraglichen Debitor zugewiesen. Wenn Sie den Debitorencode im Feld **Rechnungs-Rabattcode** für andere Debitorenkarten auswählen, wird derselbe Rechnungsrabatt diesen Kunden zugewiesen.

## Siehe auch
<a id="see-also" class="xliff"></a>
[Erweitert: Beste Preiskalkulation](advanced-best-price-calculation.md)  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

