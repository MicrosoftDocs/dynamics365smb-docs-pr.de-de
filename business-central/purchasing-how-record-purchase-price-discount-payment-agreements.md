---
title: "Einrichtung spezieller und alternativer Preise und Rabatte für Kreditoren | Microsoft Docs"
description: Die unterschiedlichen oder alternativen Preise und Rabattvereinbarungen festlegen und sie zu Einkaufsbelegen zuweisen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 07/03/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 021eac95fe22cfb37a6eaf851a5da11fd3ce9d30
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="record-special-purchase-prices-and-discounts"></a>Besondere Verkaufspreise und Rabatte aufzeichnen
Definieren Sie die verschiedenen Preis- und Rabattvereinbarungen, die beim Artikeleinkauf von unterschiedlichen Kreditoren gelten, damit die vereinbarten Regeln und Werte auf die für den Kreditor erstellten Einkaufsbelege angewendet werden.

Falls Sie spezielle Preise und Zeilenrabatte für Verkäufe und Einkäufe erfasst haben, stellt [!INCLUDE[d365fin](includes/d365fin_md.md)] sicher, dass der Deckungsbeitrag im Artikelhandel immer optimal ist, indem er die besten Preise automatisch in Einkaufs- und Verkaufsbelegen und auf Projekt und Artikel Buch.-Blattzeilen berechnet. Weitere Informationen finden Sie im Abschnitt "Beste Preise berechnen".

Für die Preise können Sie besondere auf den Einkaufszeilen verschiedene Einkaufspreise einfügen, wenn eine bestimmte Kombination aus Kreditor, Artikel, Mindestmenge, Einheit oder des Start-/Enddatum vorhanden ist.

Für die Rabatte können Sie zwei Arten von Einkaufsrabatten einrichten und verwenden:

| Rabattart | Beschreibung |
| --- | --- |
| **Einkaufszeilenrabatt** |Ein Betrag mit Rabatt wird auf den Einkaufszeilen eingefügt, wenn eine bestimmte Kombination aus Kreditor, Artikel, Mindestmenge, Einheit oder des Start-/Enddatum vorhanden ist. Diese Funktionalität gilt auf gleiche Weise für Einkaufsbelege. |
| **Rechnungsrabatt** |Ein prozentualer Rabatt, der gewährt wird, wenn der Wertbetrag aller Zeilen eines Einkaufsbelegs einen bestimmten Mindestwert übersteigt. |

Da Einkaufszeilenrabatte und Einkaufspreise auf einer Kombination aus Artikel und Kreditor basieren, kann diese Konfiguration auch auf der Artikelkarte erfolgen, auf der die Regeln und Werte definiert sind. Weitere Informationen finden Sie unter [Neue Artikel registrieren](inventory-how-register-new-items.md).

## <a name="to-set-up-a-special-purchase-price-for-a-vendor"></a>Einen Speziellen Einkaufspreis für einen Kreditor einrichten
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Bankkonten** ein. Wählen Sie dann den zugehörigen Link aus.
2. Öffnen Sie die relevante Kreditorenkarte, und klicken Sie dann auf die Aktion **Preise**.

    Das **Einkaufstyp**-Feld ist mit **Kreditor** vorausgefüllt und das Feld **Einkaufscode** ist mit der Kreditorennummer vorausgefüllt.
3. Füllen Sie die Felder in der Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Füllen Sie eine Zeile für jede Kombination aus, für die Sie dem Kreditor einen Einkaufszeilenrabatt gewähren.

## <a name="to-set-up-a-line-discount-for-a-vendor"></a>Um einen Zeilenrabatt für einen Kreditor einzurichten
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Bankkonten** ein. Wählen Sie dann den zugehörigen Link aus.
2. Öffnen Sie die relevante Kreditorenkarte, und klicken Sie dann auf die Aktion **Zeilenrabatte**.

    Das **Einkaufstyp**-Feld ist mit **Kreditor** vorausgefüllt und das Feld **Einkaufscode** ist mit der Kreditorennummer vorausgefüllt.
3. Füllen Sie die Felder in der Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Füllen Sie eine Zeile für jede Kombination aus, für die Sie dem Kreditor einen Einkaufszeilenrabatt gewähren.

## <a name="to-set-up-an-invoice-discount-for-a-vendor"></a>Um einen Rechnungsrabatt für einen Kreditor einzurichten
Wenn Ihre Kreditoren Sie informiert haben, welche Rechnungsrabatte sie gewähren, können Sie den Rechnungsrabattcode auf den Kreditorenkarten eingeben und Bedingungen für jeden Code einrichten.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Bankkonten** ein. Wählen Sie dann den zugehörigen Link aus.
2. Öffnen Sie die Kreditorenkarte für einen Kreditor, der für Rechnungsrabatte in Frage kommt.
3. Geben Sie im Feld **Rechnungsrabattcode** einen Code für die jeweilige Rechnungsrabattbedingungen ein, die zur Berechnung der Rabatte für den Kreditor verwendet werden sollen.

    > [!NOTE]  
    >   Rechnungsrabattcodes werden durch vorhandene Kreditorenkarten dargestellt. Dies ermöglicht es Ihnen, Rechnungsrabattbedingungen schnell einem Kreditor zuzuweisen, indem es den Namen eines anderen Kreditors mit den selben Konditionen auswählt.

    Fahren Sie fort, um neue Einkaufssrechnungsrabatt-Bedingungen einzurichten.
4. Im Fenster **Kreditorenkarte** wählen Sie die Aktion **Rechnungsrabatt** aus. Das Fenster **Kreditorenrechnungsrabatte** wird geöffnet.
5. Geben Sie in dem Feld **Währungscode** den Code für die Währung ein, für die die Rechnungsrabattkonditionen gelten sollen. Wenn Sie Rechnungsrabattbedingungen in EUR einrichten möchten, dann lassen Sie das Feld leer.
6. Geben Sie im Feld **Minimalbetrag** den Mindestbetrag ein, den eine Rechnung aufweisen muss, um für einen Rabatt in Frage zu kommen.
7. Geben Sie im Feld **Rabatt** den Rechnungsrabatt als Prozentsatz des Rechnungsbetrages ein.
8. Wiederholen Sie die Schritte 5 bis 7 für jede Währung, für die der Kreditor einen Rechnungsrabatt erhält.

Der Rechnungsrabatt wird jetzt eingerichtet und dem fraglichen Kreditor zugewiesen. Wenn Sie den Kreditorencode im Feld **Rechnungs-Rabattcode** für andere Kreditorenkarten auswählen, wird derselbe Rechnungsrabatt diesen Kreditor zugewiesen.

## <a name="to-choose-a-principle-for-posting-purchase-discounts"></a>So wählen Sie ein Prinzip für die Buchung von Einkaufsrabatten aus  
Wenn Sie eine Einkaufsrechnung buchen, die einen oder mehrere Rabatte enthält, können Sie zwischen zwei Prinzipien für die Buchung von Rabattbeträgen wählen. Sie können die Rabattbeträge separat buchen oder diese von den Rechnungsbeträgen abziehen.  

Bevor Sie dies tun können, müssen Sie zuvor die notwendigen Konten für die Buchung von Rabattbeträgen im Kontenplan eingerichtet haben. Sie müssen auch überprüfen, ob Sie die richtigen Kontonummern in der Buchungsmatrix-Einrichtung in den Feldern **Eink.-Zeilenrabattkonto** und **Eink.-Rechnungsrabattkonto** eingegeben haben.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht  suchen") und geben **Kreditoren- und Debitoren-Einrichtung** ein. Wählen Sie dann den zugehörigen Link aus.
2. Klicken Sie in das Feld  **Rabattbuchung**, um ein Prinzip für die Buchung von Rabatten auszuwählen.

|**Rabattbuchungsprinzip**|**Rechnungsrabatt**|**Zeilenrabatt**|  
|------------------------------------|--------------------------|-----------------------|  
|**Alle Rabatte**|Separat Buchen|Separat Buchen|  
|**Rechnungsrabatte**|Separat Buchen|Abziehen|  
|**Zeilenrabatte**|Abziehen|Separat Buchen|  
|**Keine Rabatte**|Abziehen|Abziehen|  

## <a name="purchase-invoice-discounts-and-service-charges"></a>Einkaufsrechnungsrabatte und Servicegebühren
Wenn Sie feste Konditionen für Rechnungsrabatte mit einzelnen Kreditoren haben, können Sie diese für die einzelnen Kreditoren einrichten. Der Rabatt wird berechnet, wenn Sie eine Einkaufsrechnung erstellen.  

 Bevor Sie die Rechnungsrabatte für Einkäufe verwenden können, müssen Sie die Kreditoren angeben, die Ihnen Rabatte anbieten.  

 Sie verknüpfen Rabattprozentsätze mit bestimmten Rechnungsbeträgen im Fenster **Kreditorenrechnungsrabatte** windows. Sie können eine beliebige Anzahl von Prozentsätzen in jedem Fenster eingeben. Jeder Kreditor kann ein eigenes Fenster haben, oder Sie können verschiedene Kreditoren mit dem gleichen Fenster verknüpfen.  

 Zusätzlich zu einem Rabattprozentsatz können Sie eine Servicegebühr mit einem bestimmten Rechnungsbetrag verknüpfen.  

 Sie können die Bedingungen für Rechnungsrabatte für inländische Kreditoren in MW angeben und für ausländische Kreditoren in Fremdwährung.  

 Sie können wählen, ob [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisch die Rechnungsrabatte für Anfragen, Rahmenbestellungen, Bestellungen, Rechnungen oder Gutschriften berechnen soll.  

> [!TIP]  
>  Bevor Sie diese Informationen eingeben, ist es sinnvoll, eine Skizze der Rabattstruktur vorzubereiten, die Sie verwenden möchten. Daraus ist leichter zu ersehen, welche Kreditoren mit dem gleichen Rechnungsrabattfenster verknüpft werden können. Wenn Sie weniger Fenster einrichten müssen, können Sie die Basisinformationen schneller eingeben.

## <a name="best-price-calculation"></a>Beste Preisberechnung
Falls Sie spezielle Preise und Zeilenrabatte für Verkäufe und Einkäufe erfasst haben, stellt [!INCLUDE[d365fin](includes/d365fin_md.md)] sicher, dass der Deckungsbeitrag im Artikelhandel immer optimal ist, indem er die besten Preise automatisch in Einkaufs- und Verkaufsbelegen und auf Projekt und Artikel Buch.-Blattzeilen berechnet.

Der beste Preis ist der niedrigste mögliche Preis mit dem höchsten möglichen Zeilenrabatt an einem bestimmten Datum. [!INCLUDE[d365fin](includes/d365fin_md.md)] berechnet diesen, wenn Sie den Verkaufspreis und den prozentualen Zeilenrabatt für Artikel auf neuen Beleg und Buch.-Blattzeilen eingefügt haben.

> [!NOTE]  
>   Nachfolgend wird erläutert, wie die besten Preise für Verkäufe berechnet werden. Die Berechnung ist die gleiche wie für Einkäufe.

1. [!INCLUDE[d365fin](includes/d365fin_md.md)] prüft die Kombination aus Rechnungsempfänger und Artikel und wählt den entsprechenden Preis/Rabatt unter Verwendung der folgenden Kriterien:

    - Hat dieser Debitor eine spezielle Vereinbarung für Preise oder Zeilenrabatte oder gehört der Debitor zu einer Gruppe, die solche Vereinbarungen hat?
    - Ist der Artikel oder die Artikelrabattgruppe in der Zeile in einer dieser Vereinbarungen enthalten?
    - Liegt das Auftragsdatum (oder das Buchungsdatum für die Rechnung und Gutschrift) innerhalb des Start- und Enddatums der Preis-/Zeilenrabatt-Vereinbarung?
    - Wurde ein Einheitencode angegeben? Falls dies der Fall ist, prüft [!INCLUDE[d365fin](includes/d365fin_md.md)] Preise/Rabatte mit dem gleichen Einheitencode und die Preise und Rabatte, bei denen kein Einheitencode angegeben wurde.

2. [!INCLUDE[d365fin](includes/d365fin_md.md)] überprüft, ob Preis-/Rabattvereinbarungen für Informationen für die Beleg- oder die Buch.-Blattzeile gilt und fügt dann den gültigen Einheitspreis und den prozentualen Zeilenrabatt, unter Verwendung der folgenden Kriterien ein:

    - Gibt es eine Mindestanzahl in der Preis-/Rabattvereinbarung, die erfüllt ist?
    - Gibt es eine Währungsanforderung in der Preis-/Rabattvereinbarung, die erfüllt ist? In diesem Fall werden der niedrigste Preis und der höchsten Zeilenrabatt für diese Währung eingefügt, selbst wenn MW einen besseren Preis liefern würde. Falls es für den angegebenen Währungscode keine Preis-/Zeilenrabatte gibt, verwendet [!INCLUDE[d365fin](includes/d365fin_md.md)] den niedrigsten Preis und den höchsten Zeilenrabatt in MW.

Wenn keine Spezialpreise für die Artikel in der Zeile gefunden werden, werden entweder die letzten direkten Kosten oder der Einheitspreis von der Artikelkarte oder der Lagerhaltungsdatenkarte verwendet.

## <a name="see-also"></a>Siehe auch
[Einkaufeinrichten](purchasing-setup-purchasing.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

