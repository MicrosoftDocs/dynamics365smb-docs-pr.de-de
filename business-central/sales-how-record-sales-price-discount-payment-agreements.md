---
title: Besondere Verkaufspreise und Rabatte aufzeichnen| Microsoft Docs
description: Beschreibt, wie Preise die alternative und Rabattvereinbarungen definiert, die Sie zu Verkaufsbelegen beim Verkauf an verschiedene Debitoren gelten sollen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 6d358afec4689a3543245295427d5fae992dd680
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6436776"
---
# <a name="record-special-sales-prices-and-discounts"></a>Spezielle Verkaufspreise und Rabatte aufzeichnen
> [!NOTE]
> In Veröffentlichungszyklus 2 von 2020 haben wir optimierte Prozesse zum Einrichten und Verwalten von Preisen und Rabatten veröffentlicht. Wenn Sie ein neuer Kunde mit dieser Version sind, nutzen Sie die neue Erfahrung. Wenn Sie bereits Kunde sind, hängt es davon ab, ob Sie die neue Erfahrung verwenden, ob Ihr Administrator die Funktionsaktualisierung **Neues Verkaufspreiserlebnis** in **Funktionsverwaltung** akualisiert hat. Weitere Informationen finden Sie unter [Bevorstehende Funktionen im Voraus aktivieren](/dynamics365/business-central/dev-itpro/administration/feature-management).

Die Preis- und Zahlungsrichtlinien, die beim Verkauf an Debitoren gelten, müssen so definiert werden, dass die vereinbarten Regeln und Werte für Verkaufsbelege übernommen werden.

Falls Sie spezielle Preise und Zeilenrabatte für Verkäufe und Einkäufe erfasst haben, stellt [!INCLUDE[prod_short](includes/prod_short.md)] sicher, dass der Deckungsbeitrag im Artikelhandel immer optimal ist, indem er die besten Preise automatisch in Einkaufs- und Verkaufsbelegen und auf Projekt und Artikel Buch.-Blattzeilen berechnet. Weitere Informationen finden Sie unter [Beste Preisberechnung](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

Für die Preise können Sie besondere auf den Verkaufszeilen verschiedene Verkaufspreise einfügen, wenn eine bestimmte Kombination aus Debitor, Artikel, Mindestmenge, Einheit oder des Start-/Enddatum vorhanden ist. Weitere Informationen finden Sie unter [So legen Sie einen Verkaufspreis für einen Kunden fest](#to-set-up-a-sales-price-for-a-customer) und [Beste Preisberechnung](#best-price-calculation).  

Für die Rabatte können Sie zwei Arten von Verkaufsrabatten einrichten und verwenden:

| Rabattart | Beschreibung |
| --- | --- |
| **Verkaufszeilenrabatt** |Ein Betrag mit Rabatt wird auf den Verkaufszeilen eingefügt, wenn eine bestimmte Kombination aus Debitor, Artikel, Mindestmenge, Einheit oder des Start-/Enddatum vorhanden ist. Diese Funktionalität gilt auf gleiche Weise für Verkaufsbelege. |
| **Rechnungsrabatt** |Ein Rabattprozentsatz, der von der Gesamtsumme des Verkaufsbelegs abgezogen wird, wenn die Summe aller Zeilen des Belegs einen bestimmten Mindestwert übersteigt. |

Da Verkaufszeilenrabatte und Verkaufspreise auf einer Kombination aus Artikel und Debitor bestehen, können Sie diese Konfiguration auch auf der Artikelseite des Artikels eingerichtet werden, für den die Regeln und Werte gelten.

> [!TIP]  
> Wenn ein Artikel nie mit einem Rabatt verkauft werden sollte, lassen Sie die Skontofelder auf der Artikelseite leer und schließen Sie den Artikel nicht in einer Zeilenrabatteinrichtung ein.

Die **Ausgleich mit Typ** und **Ausgleich mit Nummer** In den Feldern können Sie auswählen, für was diese Preisliste gelten soll, z. B. Kunde oder Kundenpreisgruppe. Mit **Spalten anzeigen für** können Sie Spalten ein- oder ausblenden, die für das Festlegen von Preisen, Rabatten oder Preisen und Rabatten relevant sind.

Sie können Preislistenzeilen für jede Zeile manuell hinzufügen oder beispielsweise die Aktion **Zeilen vorschlagen** zum Erstellen neuer Preise für ausgewählte Artikel, Artikelrabattgruppen, Ressourcen und andere Produkttypen verwenden. Wenn Sie „Zeilen vorschlagen“ auswählen, können Sie auf der Seite „Preislinien – Neu erstellen“ Filter festlegen, um Produkte auszuwählen, für die Sie neue Preislistenlinien erstellen möchten. Sie können auch angeben, ob bei der Preisberechnung eine Mindestmenge berücksichtigt werden soll, der Anpassungsfaktor für neue Preislistenzeilen und die Rundungsmethode für Preise. Mit dieser Aktion **Zeilen kopieren** können Sie vorhandene Preislistenzeilen zwischen Preislisten kopieren.

Standardmäßig lautet der Status neuer Preislisten Entwurf. Wenn Sie mit dem Hinzufügen von Zeilen fertig sind und möchten, dass die Preisberechnungs-Engine diese enthält, können Sie den Status in Aktiv ändern.

Um Preislisten und Preise zu überprüfen, die für bestimmte Kunden oder Lieferanten gelten, klicken Sie auf der Seite **Kunde** **Verkaufspreislisten** oder auf der Seite **Verkäufer** **Kaufpreislisten**. Sie können Preislistenzeilen in unterschiedlichen Preislisten anzeigen, indem Sie **Verkaufspreise** oder **Kaufpreise** aus den Seiten **Artikel** und **Ressource** auswählen.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Um Verkaufspreise für einen Debitor zu erstellen:

Diese Schritte unterscheiden sich je nachdem, ob Ihr Administrator das Feature-Update **Neues Verkaufspreiserlebnis** aktiviert hat.  

#### <a name="current-experience"></a>[Aktuelle Erfahrung](#tab/current-experience/)

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Debitor** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Debitor und dann die Aktion **Preise**.
3. Füllen Sie die Felder in der Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Füllen Sie eine Zeile für jede Kombination aus, die dem Debitor einen besonderen Preis gewährt.

#### <a name="new-experience"></a>[Neue Erfahrung](#tab/new-experience/)  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Debitor** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Debitor und dann die Aktion **Verkaufspreislisten**. 
3. Wählen Sie **Neu**, um eine neue Verkaufspreisliste zu erstellen.
4. Füllen Sie bei Bedarf die Felder in den Inforegistern **Allgemein** und **Steuern** aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Führen Sie einen der folgenden Schritte aus, um Elemente zur Liste hinzuzufügen:
   * Um viele Elemente hinzuzufügen, wählen Sie **Linien vorschlagen**. Geben Sie anschließend Filterkriterien ein, um die hinzuzufügenden Elementtypen anzugeben. Optional können Sie auch einige zusätzliche Einstellungen für die Artikel eingeben, die für die Preisliste spezifisch sind. Bei Bedarf können Sie diese später ändern.
   * Um Artikel aus einer anderen Preisliste zu kopieren, wählen Sie **Zeilen kopieren** und wählen Sie dann die zu kopierende Preisliste aus.
   * Um Elemente manuell hinzuzufügen, wählen Sie im Raster im Feld **Produkt-Typ** den Produkttyp aus, für den die Preisliste bestimmt ist. Füllen Sie je nach Auswahl die restlichen Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Um die Preisliste zu verwenden, klicken Sie auf das Feld **Status** und wählen Sie **Aktiv**.  

---

## <a name="sales-invoice-discounts-and-service-charges"></a>Verkaufsrechnungsrabatte und Servicegebühren
Wenn Sie Rechnungsrabatte verwenden, bestimmt der Gesamtbetrag des Rechnungsbetrages die Höhe des Rabattes, der gewährt wird. Auf der Seite **Debitorenrechnungsrabatte** können Sie eine Servicegebühr für Rechnungen über einem bestimmten Betrag einrichten.  

Bevor Sie Rechnungsrabatte mit Verkäufen verwenden können, müssen Sie einige Informationen in der Anwendung definieren. Sie müssen Folgendes entscheiden:  

- Welchen Debitoren diese Art von Rabatt gewährt wird  
- Welche Rabattprozentsätze Sie verwenden möchten  

Wenn Sie Rechnungsrabatte automatisch berechnen möchten, können Sie dies auf der Seite **Debitoren und Verkauf einrichten** tun.  

Sie können für jeden Debitor angeben, ob Sie Rechnungsrabatte gewähren möchten, wenn die Anforderungen erfüllt sind (d. h. der Rechnungsbetrag groß genug ist). Sie können die Bedingungen für Rechnungsrabatte für inländische Debitoren in der Mandantenwährung und für ausländische Debitoren in Fremdwährung festlegen.  

Sie verknüpfen Rabattprozentsätze mit bestimmten Rechnungsbeträgen auf den Seiten **Debitorenrechnungsrabatte** für jeden Debitor. Sie können eine beliebige Anzahl von Prozentsätzen auf jeder Seite eingeben. Jeder Debitor kann eine eigene Seite haben, oder Sie können verschiedene Debitoren mit der gleichen Seite verknüpfen.  

Zusätzlich (oder anstatt) eines Rabattprozentsatzes können Sie eine Servicegebühr mit einem bestimmten Rechnungsbetrag verknüpfen.  

> [!TIP]  
> Bevor Sie diese Informationen eingeben, ist es sinnvoll, eine Skizze der Rabattstruktur vorzubereiten, die Sie verwenden möchten. Dadurch wird es Ihnen erleichtert, zu erkennen, welche Debitoren mit derselben Rechnungsrabattseite verknüpft werden können. Wenn Sie weniger Seiten einrichten müssen, können Sie die Basisinformationen schneller eingeben.

Weitere Informationen zur Schulung für Rabatte bei Verkäufen finden Sie unter [Einrichten von Rabatten für Ihre Kunden](/learn/modules/customer-discounts-dynamics-365-business-central/index) unter Microsoft Learn.  

### <a name="calculating-invoice-discounts-on-sales"></a>Rechnungsrabatte bei Verkäufen berechnen

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>So erstellen Sie Verkaufszeilenrabatte für einen Debitor:
Diese Schritte unterscheiden sich je nachdem, ob Ihr Administrator das Feature-Update **Neues Verkaufspreiserlebnis** aktiviert hat. 

#### <a name="current-experience"></a>[Aktuelle Erfahrung](#tab/current-experience/)  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Debitor** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die entsprechende Kundenkarte und wählen Sie dann die Aktion **Zeilen-Rabatte**.
3. Füllen Sie die Felder in der Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Füllen Sie eine Zeile für jede Kombination aus, die dem Debitor einen besonderen Verkaufszeilenrabatt gewährt.

> [!Note]
> Wenn Sie die Seiten **Verkaufspreise** und **Verkaufszeilenrabatte** von einem bestimmten Debitoren öffnen, werden die Felder **Verkaufsartfilter** und **Verkaufscodefilter** für den Debitor festgelegt und können nicht geändert oder entfernt werden.
>
> Um Preise oder Zeilenrabatte für alle Debitoren, eine Debitorenpreisgruppe oder Kampagne einzurichten, müssen Sie die Seiten von einer Artikelkarte aus öffnen. Verwenden Sie alternativ für Verkaufspreise die Seite **VK-Preisarbeitsblatt**. Weitere Informationen finden Sie unter [So führen Sie eine Sammelaktualisierung von Artikelpreisen durch](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

#### <a name="new-experience"></a>[Neue Erfahrung](#tab/new-experience/)  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Debitor** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Debitor und dann die Aktion **Verkaufspreislisten**.
3. Öffnen Sie die Preisliste, für die der Zeilenrabatt angegeben werden soll.
4. Aktivieren Sie den Schalter **Zeilenrabatt zulassen**.
5. Erstellen Sie eine neue Zeile oder wählen Sie eine vorhandene Zeile aus und füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Wählen Sie im Feld **Definiert** entweder **Preis und Rabatt** oder einfach **Rabatt**. 
7. Legen Sie im Feld **Zeilenrabatt %** den Rabattprozentsatz fest.

    > [!TIP]
    > Wenn Sie eine vorhandene Zeile bearbeiten, können Sie die Zeilen filtern, indem Sie die entsprechende Option im Feld **Spalten anzeigen für** auswählen.

    > [!NOTE]  
    > Rechnungsrabattcodes werden durch BestandsDebitorenkarten dargestellt. Dies ermöglicht es Ihnen, Rechnungsrabattbedingungen schnell einem Debitor zuzuweisen, indem es den Namen eines anderen Debitors mit den selben Konditionen auswählt. Um kundenspezifische Rechnungsrabattbedingungen einzurichten, setzen Sie das Feld **Rechnungs-Rabatt-Code** auf den Kundencode des Kunden und fahren Sie dann mit dem nächsten Schritt fort.

8. Auf der Seite **Debitorenkarte** wählen Sie die Aktion **Rechnungsrabatt** aus. Die Seite **Debitorenrechnungsrabatte** wird geöffnet.
9. Geben Sie in dem Feld **Währungscode** den Code für die Währung ein, für die die Rechnungsrabattkonditionen gelten sollen. Wenn Sie Rechnungsrabattbedingungen in Ihrer Mandantenwährung einrichten möchten, dann lassen Sie das Feld leer.
10. Optional geben Sie im Feld **Minimalbetrag** den Mindestbetrag ein, den eine Rechnung aufweisen muss, um für einen Rabatt in Frage zu kommen.
11. Geben Sie im Feld **Rabatt** den Rechnungsrabatt als Prozentsatz des Rechnungsbetrages ein.
12. Wiederholen Sie die Schritte 5 bis 7 für jede Währung, für die der Debitor einen Rechnungsrabatt erhält.

Der Rechnungsrabatt wird jetzt eingerichtet und dem Debitor zugewiesen. Wenn Sie den Debitorencode im Feld **Rechnungs-Rabattcode** für andere Debitorenkarten auswählen, wird derselbe Rechnungsrabatt diesen Debitoren zugewiesen.

---

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Um Rechnungsrabattkonditionen für Einkäufe einzurichten:
Nachdem Sie sich entschieden haben, welche Debitoren für Rechnungsrabatte in Frage kommen, geben Sie die Rechnungsrabattcodes auf den Debitorenkarten ein, und richten Sie die Bedingungen für die einzelnen Codes ein.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Debitor** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Kundenseite für einen Debitor, der für Rechnungsrabatte in Frage kommt.
3. Geben Sie im Feld **Rechnungsrabattcode** einen Code für das jeweilige Rechnungsrabattfenster ein, das die Anwendung verwenden soll, um Rechnungsrabatte für den Debitor zu berechnen. <!--Looks like I can only choose customers in this list-->

> [!NOTE]  
> Rechnungsrabattcodes werden durch BestandsDebitorenkarten dargestellt. Dies ermöglicht es Ihnen, Rechnungsrabattbedingungen schnell einem Debitor zuzuweisen, indem es den Namen eines anderen Debitors mit den selben Konditionen auswählt.

Fahren Sie fort, um neue Verkaufsrechnungsrabatt-Bedingungen einzurichten.

1. Auf der Seite **Debitoren** wählen Sie die Aktion **Rechnungsrabatt** aus. Die Seite **Debitorenrechnungsrabatte** wird geöffnet.
2. Geben Sie in dem Feld **Währungscode** den Code für die Währung ein, für die die Rechnungsrabattkonditionen gelten sollen. Wenn Sie Rechnungsrabattbedingungen in Ihrer Mandantenwährung einrichten möchten, dann lassen Sie das Feld leer.
3. Geben Sie im Feld **Minimalbetrag** den Mindestbetrag ein, den eine Rechnung aufweisen muss, um für einen Rabatt in Frage zu kommen.
4. Geben Sie im Feld **Rabatt** den Rechnungsrabatt als Prozentsatz des Rechnungsbetrages ein.
5. Wiederholen Sie die Schritte 5 bis 7 für jede Währung, für die der Debitor einen Rechnungsrabatt erhält.

## <a name="to-copy-sales-prices"></a>Verkaufspreise kopieren
Diese Schritte unterscheiden sich je nachdem, ob Ihr Administrator das Feature-Update **Neues Verkaufspreiserlebnis** aktiviert hat. 

#### <a name="current-experience"></a>[Aktuelle Erfahrung](#tab/current-experience/)  

Falls Sie Verkaufspreise kopieren möchten, wie z. B. den Preis eines einzelnen Debitors, um ihn in einer Debitorengruppe zu verwenden, müssen Sie die Stapelverarbeitung **VK-Preis vorschlagen** ausführen. Batchauftrag auf der Seite **Verkaufspreisarbeitsblatt**.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Verkaufspreisarbeitsblatt** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie den **Vorgeschlagenen Verkaufspreis auf dem Arbeitsblatt.** Aktion  
3. Füllen Sie im Inforegister **Verkaufspreise** die Felder mit der **Verkaufsart** und dem **Verkaufscode** der ursprünglichen Preise aus, die Sie kopieren möchten.  
4. Füllen Sie im oberen Bereich der Anforderungsseite die Felder **Verkaufsart** und **Verkaufscode** mit der Art und dem Namen aus, in die Sie die Verkaufspreise kopieren möchten.  
5. Wenn Sie mit dem Batchauftrag neue Preise erstellen wollen, wählen Sie in das Feld **Neue Preise generieren**.  
6. Wählen Sie die Schaltfläche **OK**, um die Zeilen auf der Seite **VK-Preisarbeitsblatt** mit den neuen Preisvorschlägen auszufüllen, und geben Sie an, dass diese für die gewählte Verkaufsart gültig sind.  

   > [!NOTE]  
   > Die Stapelverarbeitung erzeugt nur Vorschläge, implementiert die vorgeschlagenen Änderungen aber nicht. Falls Sie die Vorschläge annehmen möchten, d. h. sie auf die Seite **VK-Preise** übernehmen möchten, können Sie die Aktion **Preisvorschlag übernehmen** verwenden, die Sie …auf der Seite **VK-Preisarbeitsblatt** finden.

#### <a name="new-experience"></a>[Neue Erfahrung](#tab/new-experience/)  

Der Status der Preisliste muss **Entwurf** sein. 

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Verkaufspreislisten** ein und wählen Sie dann den zugehörigen Link. 
2. Wählen Sie die zu kopierende Preisliste aus und wählen Sie dann **Zeilen kopieren**.
3. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Sie können nicht zwei Zeilen mit denselben Einstellungen, aber unterschiedlichen Preisen verwenden. In diesem Fall wird eine Meldung angezeigt, wenn Sie eine Preisliste aktivieren. Sie können den zu verwendenden Preis auswählen, indem Sie die Liste öffnen und den falschen Preis löschen.  
  
---

## <a name="to-bulk-update-item-prices"></a>So aktualisieren Sie Debitorenartikelpreise auf einmal
Diese Schritte unterscheiden sich je nachdem, ob Ihr Administrator das Feature-Update **Neues Verkaufspreiserlebnis** aktiviert hat. 

#### <a name="current-experience"></a>[Aktuelle Erfahrung](#tab/current-experience/)

Wenn Sie Artikelpreise, wie alle Lagerzugangs-Artikelpreise durch einen Prozentsatz auf einmal aktualisieren möchten, müssen Sie **Artikelpreis vorschlagen** auswählen. Batchauftrag. Einen Link zu dem Batchauftrag finden Sie auf der Seite **Verkaufspreisarbeitsblatt**.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Verkaufspreisarbeitsblatt** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Artikelpreis auf dem Arbeitsblatt vorschlagen** aus.  
3. Füllen Sie im Inforegister **Artikel** die **Nr.** oder **Bestand-Buchungsgruppe** oder andere Felder mit den ursprünglichen Artikelpreisen aus, die Sie aktualisieren möchten ein.  
4. Füllen Sie im oberen Bereich der Anforderungsseite die Felder **Verkaufsart** und **Verkaufscode** mit der Art und dem Namen aus, in die Sie die Verkaufspreise kopieren möchten.
5. Wenn Sie möchten, dass die Stapelverarbeitung automatisch eingegeben wird, geben Sie Artikelpreise anpassen ein im Feld **Korrekturfaktor**. Beispielsweise geben Sie entsprechend 1.15 unter **Korrekturfaktor** für die Preiserhöhung für den Artikelpreis um 15% ein.  
6. Wenn Sie mit dem Batchauftrag neue Preise erstellen wollen, wählen Sie in das Feld **Neue Preise generieren**.  
7. Wählen Sie die Schaltfläche **OK**, um die Zeilen auf der Seite **VK-Preisarbeitsblatt** mit den neuen Preisvorschlägen auszufüllen, und geben Sie an, dass diese für die gewählte **Verkaufsart** gültig sind.  

> [!NOTE]
> Die Stapelverarbeitung erzeugt nur Vorschläge, implementiert die vorgeschlagenen Änderungen aber nicht. Wenn Sie mit den Vorschlägen zufrieden sind und sie annehmen möchten, d. h. sie in die Tabelle **Verkaufspreise** übernehmen möchten, können Sie den Batchauftrag **Preisvorschlag übernehmen** verwenden, den Sie im Register **Aktionen**, in der Gruppe **Funktionen** auf der Seite **VK-Preisarbeitsblatt** finden.

#### <a name="new-experience"></a>[Neue Erfahrung](#tab/new-experience/)

Um die Preise für mehrere Artikel zu aktualisieren, müssen Sie eine neue Preisliste erstellen und dann die Zeilen aus einer vorhandenen Preisliste kopieren. Wenn Sie die Zeilen kopieren, können Sie mithilfe von Filtern angeben, was kopiert werden soll, und Sie können eine Ganzzahl oder eine Dezimalzahl im Feld **Anpassungsfaktor** zum Erhöhen oder Verringern der Preise angeben. Die Preisliste muss sich im Status **Entwurf** befinden. Bei Bedarf können Sie dann die alte Preisliste deaktivieren.

> [!NOTE]
> Sie können nicht zwei Zeilen mit denselben Einstellungen, aber unterschiedlichen Preisen verwenden. In diesem Fall wird eine Meldung angezeigt, wenn Sie eine Preisliste aktivieren. Sie können den zu verwendenden Preis auswählen, indem Sie die Liste öffnen und den falschen Preis löschen.  

---

## <a name="best-price-calculation"></a>Beste Preisberechnung
Falls Sie spezielle Preise und Zeilenrabatte für Verkäufe und Einkäufe erfasst haben, stellt [!INCLUDE[d365fin](includes/d365fin_md.md)] sicher, dass der Deckungsbeitrag im Artikelhandel immer optimal ist, indem er die besten Preise automatisch in Einkaufs- und Verkaufsbelegen und auf Projekt und Artikel Buch.-Blattzeilen berechnet.

Der beste Preis ist der niedrigste mögliche Preis mit dem höchsten möglichen Zeilenrabatt an einem bestimmten Datum. [!INCLUDE[d365fin](includes/d365fin_md.md)] berechnet diesen, wenn Sie den Verkaufspreis und den prozentualen Zeilenrabatt für Artikel auf neuen Beleg und Buch.-Blattzeilen eingefügt haben.

> [!NOTE]  
> Nachfolgend wird erläutert, wie die besten Preise für Verkäufe berechnet werden. Die Berechnung ist die gleiche wie für Einkäufe.

1. [!INCLUDE[d365fin](includes/d365fin_md.md)] prüft die Kombination aus Rechnungsempfänger und Artikel und wählt den entsprechenden Verkaufspreis/Rabatt unter Verwendung der folgenden Kriterien:

    - Hat dieser Debitor eine spezielle Vereinbarung für Preise oder Zeilenrabatte oder gehört der Debitor zu einer Gruppe, die solche Vereinbarungen hat?
    - Ist der Artikel oder die Artikelrabattgruppe in der Zeile in einer dieser Prei-/Rabattvereinbarungen enthalten?
    - Liegt das Auftragsdatum (oder das Buchungsdatum für die Rechnung und Gutschrift) innerhalb des Start- und Enddatums der Preis-/Zeilenrabatt-Vereinbarung?
    - Wurde ein Einheitencode angegeben? Falls dies der Fall ist, prüft [!INCLUDE[d365fin](includes/d365fin_md.md)] Preise/Rabatte mit dem gleichen Einheitencode und die Preise und Rabatte, bei denen kein Einheitencode angegeben wurde.

2. [!INCLUDE[d365fin](includes/d365fin_md.md)] überprüft, ob Preis-/Rabattvereinbarungen für Informationen für die Beleg- oder die Buch.-Blattzeile gilt und fügt dann den gültigen VK-Preis und den prozentualen Zeilenrabatt, unter Verwendung der folgenden Kriterien ein:

    - Gibt es eine Mindestanzahl in der Preis-/Rabattvereinbarung, die erfüllt ist?
    - Gibt es eine Währungsanforderung in der Preis-/Rabattvereinbarung, die erfüllt ist? In diesem Fall werden der niedrigste Preis und der höchsten Zeilenrabatt für diese Währung eingefügt, selbst wenn lokale Währung einen besseren Preis liefern würde. Falls es für den angegebenen Währungscode keine Preis-/Zeilenrabatte gibt, verwendet [!INCLUDE[d365fin](includes/d365fin_md.md)] den niedrigsten Preis und den höchsten Zeilenrabatt in Ihrer lokalen Währung.

Wenn keine Spezialpreise für die Artikel in der Zeile gefunden werden, werden entweder die letzten direkten Kosten oder der VK-Preis von der Artikelkarte oder der Lagerhaltungsdatenkarte verwendet.

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/manage-sales-prices-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Einrichten von Verkäufen](sales-setup-sales.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]