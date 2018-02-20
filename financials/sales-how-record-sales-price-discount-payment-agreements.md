---
title: Besondere Verkaufspreise und Rabatte aufzeichnen| Microsoft Docs
description: Beschreibt, wie Preise die alternative und Rabattvereinbarungen definiert, die Sie zu Verkaufsbelegen beim Verkauf an verschiedene Debitoren gelten sollen.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: bfb0a5b68768c3fe5e0fcf2874752b55bd96708e
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="record-special-sales-prices-and-discounts"></a>Spezielle Verkaufspreise und Rabatte aufzeichnen
Die unterschiedlichen Preis- und Zahlungsrichtlinien, die beim Verkauf an verschiedene Debitoren gelten, müssen so definiert werden, dass die vereinbarten Regeln und Werte für Verkaufsbelege übernommen werden, die für den Debitor erstellt werden.

Falls Sie spezielle Preise und Zeilenrabatte für Verkäufe und Einkäufe erfasst haben, stellt [!INCLUDE[d365fin](includes/d365fin_md.md)] sicher, dass der Deckungsbeitrag im Artikelhandel immer optimal ist, indem er die besten Preise automatisch in Einkaufs- und Verkaufsbelegen und auf Projekt und Artikel Buch.-Blattzeilen berechnet. Weitere Informationen finden Sie im Abschnitt "Beste Preise berechnen".

Für die Preise können Sie besondere auf den Verkaufszeilen verschiedene Verkaufspreise einfügen, wenn eine bestimmte Kombination aus Debitor, Artikel, Mindestmenge, Einheit oder des Start-/Enddatum vorhanden ist.

Für die Rabatte können Sie zwei Arten von Verkaufsrabatten einrichten und verwenden:

| Rabattart | Beschreibung |
| --- | --- |
| **Verkaufszeilenrabatt** |Ein Betrag mit Rabatt wird auf den Verkaufszeilen eingefügt, wenn eine bestimmte Kombination aus Debitor, Artikel, Mindestmenge, Einheit oder des Start-/Enddatum vorhanden ist. Diese Funktionalität gilt auf gleiche Weise für Verkaufsbelege. |
| **Rechnungsrabatt** |Ein prozentualer Rabatt, der gewährt wird, wenn der Wertbetrag aller Zeilen eines Einkaufsbelegs einen bestimmten Mindestwert übersteigt. |

Da Verkaufszeilenrabatte und Verkaufspreise auf einer Kombination aus Artikel und Debitor bestehen, können Sie diese Konfiguration auch auf der Artikelkarte des Artikels eingerichtet werden, für den die Regeln und Werte gelten.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Um Verkaufspreise für einen Debitor zu erstellen:
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Kunden** ein. Wählen Sie dann den zugehörigen Link aus.
2. Öffnen Sie die entsprechende Debitorenkarte und klicken dann auf **Preise**.

    Das Feld **Verkaufsart** ist mit dem Code **Debitor** ausgefüllt und das Feld **Verkaufscode** enthält die Nummer des Debitoren.
3. Füllen Sie die Felder in der Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Füllen Sie eine Zeile für jede Kombination aus, die dem Debitor einen besonderen Preis gewährt.

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>So erstellen Sie Verkaufszeilenrabatte für einen Debitor:
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Kunden** ein. Wählen Sie dann den zugehörigen Link aus.
2. Öffnen Sie die entsprechende Debitorenkarte und klicken dann auf **Zeilenpreise**.

    Das Feld **Verkaufsart** ist mit dem Code **Debitor** ausgefüllt und das Feld **Verkaufscode** enthält die Nummer des Debitoren.
3. Füllen Sie die Felder in der Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Füllen Sie eine Zeile für jede Kombination aus, die dem Debitor einen besonderen Preis gewährt.

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Um Rechnungsrabattkonditionen für Einkäufe einzurichten:
Nachdem Sie sich entschieden haben, welche Debitoren für Rechnungsrabatte in Frage kommen, geben Sie die Rechnungsrabattcodes auf den Debitorenkarten ein, und richten Sie die Bedingungen für die einzelnen Codes ein.

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Kunden** ein. Wählen Sie dann den zugehörigen Link aus.
2. Öffnen Sie die Debitorenkarte für einen Debitor, der für Rechnungsrabatte in Frage kommt.
3. Geben Sie im Feld **Rechnungsrabattcode** einen Code für das jeweilige Rechnungsrabattfenster ein, das die Anwendung verwenden soll, um Rechnungsrabatte für den Debitor zu berechnen.

    > [!NOTE]  
>   Rechnungsrabattcodes werden durch Bestandskundenkarten dargestellt. Dies ermöglicht es Ihnen, Rechnungsrabattbedingungen schnell einem Debitor zuzuweisen, indem es den Namen eines anderen Debitors mit den selben Konditionen auswählt.

    Fahren Sie fort, um neue Verkaufsrechnungsrabatt-Bedingungen einzurichten.
4. Im Fenster **Debitorenkarte** wählen Sie die Aktion **Rechnungsrabatt** aus. Das Fenster **Debitorenrechnungsrabatte** wird geöffnet.
5. Geben Sie in dem Feld **Währungscode** den Code für die Währung ein, für die die Rechnungsrabattkonditionen gelten sollen. Wenn Sie Rechnungsrabattbedingungen in EUR einrichten möchten, dann lassen Sie das Feld leer.
6. Geben Sie im Feld **Minimalbetrag** den Mindestbetrag ein, den eine Rechnung aufweisen muss, um für einen Rabatt in Frage zu kommen.
7. Geben Sie im Feld **Rabatt** den Rechnungsrabatt als Prozentsatz des Rechnungsbetrages ein.
8. Wiederholen Sie die Schritte 5 bis 7 für jede Währung, für die der Debitor einen Rechnungsrabatt erhält.

Der Rechnungsrabatt wird jetzt eingerichtet und dem fraglichen Debitor zugewiesen. Wenn Sie den Debitorencode im Feld **Rechnungs-Rabattcode** für andere Debitorenkarten auswählen, wird derselbe Rechnungsrabatt diesen Kunden zugewiesen.

## <a name="to-work-with-sales-invoice-discounts-and-service-charges"></a>Arbeiten mit Verkaufsrechnungsrabatten und Servicegebühren
Wenn Sie Rechnungsrabatte verwenden, bestimmt die Höhe des Rechnungsbetrages die Höhe des Rabattes, der gewährt wird.  

In dem Fenster **Debitorenrechnungsrabatte** können Sie eine Servicegebühr für Rechnungen über einem bestimmten Betrag einrichten.  

Bevor Sie Rechnungsrabatte mit Verkäufen verwenden können, müssen Sie einige Informationen in der Anwendung einrichten. Sie müssen festlegen:  

- welchen Debitoren diese Art von Rabatt gewährt wird.  
- welche Rabattprozentsätze Sie verwenden möchten.  

Wenn die Anwendung Rechnungsrabatte automatisch berechnen soll, können Sie dies in dem Fenster **Debitoren & Verkauf Einr.** einrichten.  

Sie können für jeden Debitor angeben, ob Sie Rechnungsrabatte gewähren möchten, wenn die Anforderungen erfüllt sind (d. h. der Rechnungsbetrag groß genug ist). Sie können die Bedingungen für Rechnungsrabatte für inländische Debitoren in der Mandantenwährung und für ausländische Debitoren in Fremdwährung festlegen.  

Sie verknüpfen Rabattprozentsätze mit bestimmten Rechnungsbeträgen in den **Debitorenrechnungsrabattfenstern**. Sie können eine beliebige Anzahl von Prozentsätzen in jedem Fenster eingeben. Jeder Debitor kann ein eigenes Fenster haben, oder Sie können verschiedene Debitoren mit dem gleichen Fenster verknüpfen.  

Zusätzlich (oder anstatt) eines Rabattprozentsatzes können Sie eine Servicegebühr mit einem bestimmten Rechnungsbetrag verknüpfen.  

> [!TIP]  
>  Bevor Sie diese Informationen in der Anwendung eingeben, ist es sinnvoll, eine Skizze der Rabattstruktur vorzubereiten, die Sie verwenden möchten. Dadurch wird es Ihnen erleichtert, zu erkennen, welche Debitoren mit demselben Rechnungsrabattfenster verknüpft werden können. Wenn Sie weniger Fenster einrichten müssen, können Sie die Basisinformationen schneller eingeben.  

## <a name="best-price-calculation"></a>Beste Preisberechnung
Falls Sie spezielle Preise und Zeilenrabatte für Verkäufe und Einkäufe erfasst haben, stellt [!INCLUDE[d365fin](includes/d365fin_md.md)] sicher, dass der Deckungsbeitrag im Artikelhandel immer optimal ist, indem er die besten Preise automatisch in Einkaufs- und Verkaufsbelegen und auf Projekt und Artikel Buch.-Blattzeilen berechnet.

Der beste Preis ist der niedrigste mögliche Preis mit dem höchsten möglichen Zeilenrabatt an einem bestimmten Datum. [!INCLUDE[d365fin](includes/d365fin_md.md)] berechnet diesen, wenn Sie den Verkaufspreis und den prozentualen Zeilenrabatt für Artikel auf neuen Beleg und Buch.-Blattzeilen eingefügt haben.

> [!NOTE]  
>   Nachfolgend wird erläutert, wie die besten Preise für Verkäufe berechnet werden. Die Berechnung ist die gleiche wie für Einkäufe.

1. [!INCLUDE[d365fin](includes/d365fin_md.md)]  prüft die Kombination aus Rechnungsempfänger und Artikel und wählt den entsprechenden Preis/Rabatt unter Verwendung der folgenden Kriterien:

    - Hat dieser Debitor eine spezielle Vereinbarung für Preise oder Zeilenrabatte oder gehört der Debitor zu einer Gruppe, die solche Vereinbarungen hat?
    - Ist der Artikel oder die Artikelrabattgruppe in der Zeile in einer dieser Vereinbarungen enthalten?
    - Liegt das Auftragsdatum (oder das Buchungsdatum für die Rechnung und Gutschrift) innerhalb des Start- und Enddatums der Preis-/Zeilenrabatt-Vereinbarung?
    - Wurde ein Einheitencode angegeben? Falls dies der Fall ist, prüft [!INCLUDE[d365fin](includes/d365fin_md.md)] Preise/Rabatte mit dem gleichen Einheitencode und die Preise und Rabatte, bei denen kein Einheitencode angegeben wurde.

2. [!INCLUDE[d365fin](includes/d365fin_md.md)]  überprüft, ob Preis-/Rabattvereinbarungen für Informationen für die Beleg- oder die Buch.-Blattzeile gilt und fügt dann den gültigen Einheitspreis und den prozentualen Zeilenrabatt, unter Verwendung der folgenden Kriterien ein:

    - Gibt es eine Mindestanzahl in der Preis-/Rabattvereinbarung, die erfüllt ist?
    - Gibt es eine Währungsanforderung in der Preis-/Rabattvereinbarung, die erfüllt ist? In diesem Fall werden der niedrigste Preis und der höchsten Zeilenrabatt für diese Währung eingefügt, selbst wenn lokale Währung einen besseren Preis liefern würde. Falls es für den angegebenen Währungscode keine Preis-/Zeilenrabatte gibt, verwendet [!INCLUDE[d365fin](includes/d365fin_md.md)] den niedrigsten Preis und den höchsten Zeilenrabatt in Ihrer lokalen Währung.

Wenn keine Spezialpreise für die Artikel in der Zeile gefunden werden, werden entweder die letzten direkten Kosten oder der Einheitspreis von der Artikelkarte oder der Lagerhaltungsdatenkarte verwendet.

## <a name="to-copy-sales-prices"></a>Verkaufspreise kopieren  
Falls Sie Verkaufspreise kopieren möchten, wie z. B. den Preis eines einzelnen Debitors, um ihn in einer Debitorengruppe zu verwenden, müssen Sie die Stapelverarbeitung **VK-Preis vorschlagen** ausführen.  Batchauftrag. Sie finden diese Stapelverarbeitung in dem Fenster **VK-Preisvorschläge**.    

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Verkaufsabrechungszusammenfassung** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie den **Vorgeschlagenen Verkaufspreis auf dem Arbeitsblatt.** Aktion  
3.  Füllen Sie im Inforegister **Verkaufspreis** die Felder mit der **Verkaufsart** und dem **Verkaufscode** der ursprünglichen Preise aus, die Sie kopieren möchten.  
4.  Füllen Sie im oberen Bereich des Anforderungsfensters die Felder **Verkaufsart** und **Verkaufscode** mit der Art und dem Namen aus, in die Sie die Verkaufspreise kopieren möchten.  
5.  Wenn Sie mit dem Batchauftrag neue Preise erstellen wollen, wählen Sie in das Feld **Neue Preise generieren**.  
6.  Wählen Sie die Schaltfläche **OK** , um die Zeilen in dem Fenster **VK-Preisvorschläge** mit den neuen Preisvorschlägen auszufüllen, und geben Sie an, dass diese für die gewählte **Verkaufsart** gültig sind.  

> [!NOTE]  
>  Die Stapelverarbeitung erzeugt nur Vorschläge, implementiert die vorgeschlagenen Änderungen aber nicht. Wenn Sie mit den Vorschlägen zufrieden sind und sie annehmen möchten, d. h. sie in die Tabelle **VK-Preise** übernehmen möchten, können Sie den Batchauftrag **Preisvorschlag übernehmen** verwenden, den Sie im Register **Aktionen**, in der Gruppe **Funktionen** im Fenster **VK-Preisformular** finden.

## <a name="see-also"></a>Siehe auch
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

