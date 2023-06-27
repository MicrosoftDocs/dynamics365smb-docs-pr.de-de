---
title: Besondere Verkaufspreise und Rabatte aufzeichnen
description: Die unterschiedlichen oder alternativen Preise und Rabattvereinbarungen festlegen und sie zu Einkaufsbelegen zuweisen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'special price, alternate price, pricing'
ms.search.form: '26, 1346, 7012, 7014, 7017, 7018, 7189, 7190, 9307'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="record-special-purchase-prices-and-discounts" />Besondere Verkaufspreise und Rabatte aufzeichnen

> [!NOTE]
> In Veröffentlichungszyklus 2 von 2020 haben wir optimierte Prozesse zum Einrichten und Verwalten von Preisen und Rabatten veröffentlicht. Wenn Sie ein neuer Kunde mit dieser Version sind, nutzen Sie die neue Erfahrung. Wenn Sie bereits Kunde sind, hängt es davon ab, ob Sie die neue Erfahrung verwenden, ob Ihr Administrator die Funktionsaktualisierung **Neues Verkaufspreiserlebnis** in **Funktionsverwaltung** akualisiert hat. Weitere Informationen finden Sie unter [Bevorstehende Funktionen im Voraus aktivieren](/dynamics365/business-central/dev-itpro/administration/feature-management).

Definieren Sie die verschiedenen Preis- und Rabattvereinbarungen, die beim Artikeleinkauf von unterschiedlichen Kreditoren gelten, damit die vereinbarten Regeln und Werte auf die für den Kreditor erstellten Einkaufsbelege angewendet werden.

Falls Sie spezielle Preise und Zeilenrabatte für Verkäufe und Einkäufe erfasst haben, stellt [!INCLUDE[prod_short](includes/prod_short.md)] sicher, dass der Deckungsbeitrag im Artikelhandel immer optimal ist, indem er die besten Preise automatisch in Einkaufs- und Verkaufsbelegen und auf Projekt und Artikel Buch.-Blattzeilen berechnet. Weitere Informationen finden Sie unter [Beste Preisberechnung](purchasing-how-record-purchase-price-discount-payment-agreements.md#best-price-calculation).

Für die Preise können Sie besondere auf den Einkaufszeilen verschiedene Einkaufspreise einfügen, wenn eine bestimmte Kombination aus Kreditor, Artikel, Mindestmenge, Einheit oder des Start-/Enddatum vorhanden ist.

Für die Rabatte können Sie zwei Arten von Einkaufsrabatten einrichten und verwenden:

| Rabattart | Beschreibung |
| --- | --- |
| **Einkaufszeilenrabatt** |Ein Betrag mit Rabatt wird auf den Einkaufszeilen eingefügt, wenn eine bestimmte Kombination aus Kreditor, Artikel, Mindestmenge, Einheit oder des Start-/Enddatum vorhanden ist. Dieser Typ gilt auf gleiche Weise für Einkaufspreise. |
| **Rechnungsrabatt** |Ein prozentualer Rabatt, der gewährt wird, wenn der Wertbetrag aller Zeilen eines Einkaufsbelegs einen bestimmten Mindestwert übersteigt. |

Da Einkaufszeilenrabatte und Einkaufspreise auf einer Kombination aus Artikel und Kreditor basieren, kann diese Konfiguration auch auf der Artikelkarte erfolgen, auf der die Regeln und Werte definiert sind. Weitere Informationen finden Sie unter [Neue Artikel registrieren](inventory-how-register-new-items.md).

## <a name="to-set-up-a-special-purchase-price-for-a-vendor" />Einen Speziellen Einkaufspreis für einen Kreditor einrichten

#### [Aktuelle Erfahrung](#tab/current-experience)

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Kreditoren** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die relevante Kreditorenkarte, und klicken Sie dann auf die Aktion **Preise**.
3. Füllen Sie die Felder in der Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Füllen Sie eine Zeile für jede Kombination aus, für die Sie dem Kreditor einen Einkaufszeilenrabatt gewähren.

#### [Neue Erfahrung](#tab/new-experience)

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Kreditoren** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Kreditor und wählen Sie dann die Aktion **Verkaufspreislisten**.
3. Wählen Sie **Neu**, um eine neue Kaufpreisliste zu erstellen.
4. Füllen Sie bei Bedarf die Felder in den Inforegistern **Allgemein** und **Steuern** aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Führen Sie einen der folgenden Schritte aus, um Elemente zur Liste hinzuzufügen:
   * Um viele Elemente hinzuzufügen, wählen Sie **Linien vorschlagen**. Geben Sie anschließend Filterkriterien ein, um die hinzuzufügenden Elementtypen anzugeben. Optional können Sie auch einige zusätzliche Einstellungen für die Artikel eingeben, die für die Preisliste spezifisch sind. Bei Bedarf können Sie diese später ändern.
   * Um Artikel aus einer anderen Preisliste zu kopieren, wählen Sie **Zeilen kopieren** und wählen Sie dann die zu kopierende Preisliste aus.
   * Um Elemente manuell hinzuzufügen, wählen Sie im Raster im Feld **Produkt-Typ** den Produkttyp aus, für den die Preisliste bestimmt ist. Füllen Sie je nach Auswahl die restlichen Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Um die Preisliste zu verwenden, klicken Sie auf das Feld **Status** und wählen Sie **Aktiv**.

---

## <a name="to-set-up-a-line-discount-for-a-vendor" />Um einen Zeilenrabatt für einen Kreditor einzurichten

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Kreditoren** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die relevante Kreditorenkarte, und klicken Sie dann auf die Aktion **Zeilenrabatte**.

   Das Feld **Kreditorennr.** ist mit der Nummer des Kreditors ausgefüllt.
3. Füllen Sie die Felder in der Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Füllen Sie eine Zeile für jede Kombination aus, für die Sie dem Kreditor einen Einkaufszeilenrabatt gewähren.

## <a name="to-set-up-an-invoice-discount-for-a-vendor" />Um einen Rechnungsrabatt für einen Kreditor einzurichten

Wenn Ihre Kreditoren Sie informiert haben, welche Rechnungsrabatte sie gewähren, können Sie den Rechnungsrabattcode auf den Kreditorenkarten eingeben und Bedingungen für jeden Code einrichten.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Kreditoren** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die Kreditorenkarte für einen Kreditor, der für Rechnungsrabatte in Frage kommt.
3. Geben Sie im Feld **Rechnungsrabattcode** einen Code für die jeweilige Rechnungsrabattbedingungen ein, die zur Berechnung der Rabatte für den Kreditor verwendet werden sollen.

    > [!NOTE]  
    > Rechnungsrabattcodes werden durch vorhandene Kreditorenkarten dargestellt. Dies ermöglicht es Ihnen, Rechnungsrabattbedingungen schnell einem Kreditor zuzuweisen, indem es den Namen eines anderen Kreditors mit den selben Konditionen auswählt.

    Fahren Sie fort, um neue Einkaufssrechnungsrabatt-Bedingungen einzurichten.
4. Auf der Seite **Kreditorenkarte** wählen Sie die Aktion **Rechnungsrabatt** aus. Die Seite **Kreditorenrechnungsrabatte** wird geöffnet.
5. Geben Sie in dem Feld **Währungscode** den Code für die Währung ein, für die die Rechnungsrabattkonditionen gelten sollen. Wenn Sie Rechnungsrabattbedingungen in EUR einrichten möchten, dann lassen Sie das Feld leer.
6. Geben Sie im Feld **Minimalbetrag** den Mindestbetrag ein, den eine Rechnung aufweisen muss, um für einen Rabatt in Frage zu kommen.
7. Geben Sie im Feld **Rabatt** den Rechnungsrabatt als Prozentsatz des Rechnungsbetrages ein.
8. Wiederholen Sie die Schritte 5 bis 7 für jede Währung, für die der Kreditor einen Rechnungsrabatt erhält.

Der Rechnungsrabatt wird jetzt eingerichtet und dem fraglichen Kreditor zugewiesen. Wenn Sie den Kreditorencode im Feld **Rechnungs-Rabattcode** für andere Kreditorenkarten auswählen, wird derselbe Rechnungsrabatt diesen Kreditoren zugewiesen.

## <a name="to-choose-a-principle-for-posting-purchase-discounts" />So wählen Sie ein Prinzip für die Buchung von Einkaufsrabatten aus

Wenn Sie eine Einkaufsrechnung buchen, die einen oder mehrere Rabatte enthält, können Sie zwischen zwei Prinzipien für die Buchung von Rabattbeträgen wählen. Sie können die Rabattbeträge separat buchen oder diese von den Rechnungsbeträgen abziehen.  

Bevor Sie dies tun können, müssen Sie zuvor die notwendigen Konten für die Buchung von Rabattbeträgen im Kontenplan eingerichtet haben. Sie müssen auch überprüfen, ob Sie die richtigen Kontonummern in der Buchungsmatrix-Einrichtung in den Feldern **Eink.-Zeilenrabattkonto** und **Eink.-Rechnungsrabattkonto** eingegeben haben.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Kredite und Einkauf Einr. ein** und wählen Sie dann den entsprechenden Link.
2. Klicken Sie in das Feld  **Rabattbuchung**, um ein Prinzip für die Buchung von Rabatten auszuwählen.

|**Rabattbuchungsprinzip**|**Rechnungsrabatt**|**Zeilenrabatt**|  
|------------------------------------|--------------------------|-----------------------|  
|**Alle Rabatte**|Separat Buchen|Separat Buchen|  
|**Rechnungsrabatte**|Separat Buchen|Abziehen|  
|**Zeilenrabatte**|Abziehen|Separat Buchen|  
|**Keine Rabatte**|Abziehen|Abziehen|  

## <a name="purchase-invoice-discounts-and-service-charges" />Einkaufsrechnungsrabatte und Servicegebühren

Wenn Sie feste Konditionen für Rechnungsrabatte mit einzelnen Kreditoren haben, können Sie diese für die einzelnen Kreditoren einrichten. Der Rabatt wird berechnet, wenn Sie eine Einkaufsrechnung erstellen.  

Bevor Sie die Rechnungsrabatte für Einkäufe verwenden können, müssen Sie die Kreditoren angeben, die Ihnen Rabatte anbieten.  

Sie verknüpfen Rabattprozentsätze mit bestimmten Rechnungsbeträgen auf den Seiten **Kreditorenrechnungsrabatte**. Sie können eine beliebige Anzahl von Prozentsätzen auf jeder Seite eingeben. Jeder Kreditor kann eine eigene Seite haben, oder Sie können verschiedene Kreditoren mit der gleichen Seite verknüpfen.  

Zusätzlich zu einem Rabattprozentsatz können Sie eine Servicegebühr mit einem bestimmten Rechnungsbetrag verknüpfen.  

Sie können die Bedingungen für Rechnungsrabatte für inländische Kreditoren in MW angeben und für ausländische Kreditoren in Fremdwährung.  

Sie können wählen, ob [!INCLUDE[prod_short](includes/prod_short.md)] automatisch die Rechnungsrabatte für Anfragen, Rahmenbestellungen, Bestellungen, Rechnungen oder Gutschriften berechnen soll.  

> [!TIP]  
> Bevor Sie diese Informationen eingeben, ist es sinnvoll, eine Skizze der Rabattstruktur vorzubereiten, die Sie verwenden möchten. Daraus ist leichter zu ersehen, welche Kreditoren mit der gleichen Rechnungsrabattseite verknüpft werden können. Wenn Sie weniger Seiten einrichten müssen, können Sie die Basisinformationen schneller eingeben.

## <a name="best-price-calculation" />Berechnung des besten Preises

Falls Sie spezielle Preise und Zeilenrabatte für Verkäufe und Einkäufe erfasst haben, stellt [!INCLUDE[prod_short](includes/prod_short.md)] sicher, dass der Deckungsbeitrag im Artikelhandel immer optimal ist, indem er die besten Preise automatisch in Einkaufs- und Verkaufsbelegen und auf Projekt und Artikel Buch.-Blattzeilen berechnet.

Der beste Preis ist der niedrigste mögliche Preis mit dem höchsten möglichen Zeilenrabatt an einem bestimmten Datum. [!INCLUDE[prod_short](includes/prod_short.md)] berechnet diesen Preis, wenn Sie den Verkaufspreis und den prozentualen Zeilenrabatt für Artikel auf neuen Beleg und Buch.-Blattzeilen eingefügt haben.

> [!NOTE]  
> Nachfolgend wird erläutert, wie die besten Preise für Verkäufe berechnet werden. Die Berechnung ist die gleiche wie für Einkäufe.

1. [!INCLUDE[prod_short](includes/prod_short.md)] prüft die Kombination aus Rechnungsempfänger und Artikel und wählt den entsprechenden Verkaufspreis/Rabatt unter Verwendung der folgenden Kriterien:

    - Hat dieser Debitor eine spezielle Vereinbarung für Preise oder Zeilenrabatte oder gehört der Debitor zu einer Gruppe, die solche Vereinbarungen hat?
    - Ist der Artikel oder die Artikelrabattgruppe in der Zeile in einer dieser Prei-/Rabattvereinbarungen enthalten?
    - Liegt das Auftragsdatum (oder das Buchungsdatum für die Rechnung und Gutschrift) innerhalb des Start- und Enddatums der Preis-/Zeilenrabatt-Vereinbarung?
    - Wurde ein Einheitencode angegeben? Falls dies der Fall ist, prüft [!INCLUDE[prod_short](includes/prod_short.md)] Preise/Rabatte mit dem gleichen Einheitencode und die Preise und Rabatte, bei denen kein Einheitencode angegeben wurde.

2. [!INCLUDE[prod_short](includes/prod_short.md)] überprüft, ob Preis-/Rabattvereinbarungen für Informationen für die Beleg- oder die Buch.-Blattzeile gilt und fügt dann den gültigen VK-Preis und den prozentualen Zeilenrabatt, unter Verwendung der folgenden Kriterien ein:

    - Gibt es eine Mindestanzahl in der Preis-/Rabattvereinbarung, die erfüllt ist?
    - Gibt es eine Währungsanforderung in der Preis-/Rabattvereinbarung, die erfüllt ist? In diesem Fall werden der niedrigste Preis und der höchsten Zeilenrabatt für diese Währung eingefügt, selbst wenn MW einen besseren Preis liefern würde. Falls es für den angegebenen Währungscode keine Preis-/Zeilenrabatte gibt, verwendet [!INCLUDE[prod_short](includes/prod_short.md)] den niedrigsten Preis und den höchsten Zeilenrabatt in MW.

Wenn keine Spezialpreise für die Artikel in der Zeile gefunden werden, werden entweder die letzten direkten Kosten oder der VK-Preis von der Artikelkarte oder der Lagerhaltungsdatenkarte verwendet.

## <a name="see-related-microsoft-training" />Siehe verwandte [Microsoft Schulungen](/training/modules/set-up-prices-discounts-dynamics-365-business-central/index)

## <a name="see-also" />Siehe auch

[Einkaufeinrichten](purchasing-setup-purchasing.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
