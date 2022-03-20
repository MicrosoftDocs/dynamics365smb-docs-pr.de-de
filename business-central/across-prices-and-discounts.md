---
title: Preise und Rabatte einrichten
description: Beschreibt, wie Standard- und Sonderpreis- und Rabattvereinbarungen für Verkäufe und Einkäufe definiert werden.
author: brentholtorf
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: price, pricing, discount, discounting, rebate, sale, purchase, invoice
ms.search.form: 459, 460, 7001, 7011, 7015, 7016, 7017, 7018
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 3a6d6b680ebfb89c376872d2dcd5cb6fb535d4a3
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2022
ms.locfileid: "8383295"
---
# <a name="set-up-prices-and-discounts"></a>Preise und Rabatte einrichten
> [!NOTE]
> In Veröffentlichungszyklus 2 von 2020 haben wir optimierte Prozesse zum Einrichten und Verwalten von Preisen und Rabatten veröffentlicht. Wenn Sie ein neuer Kunde mit dieser Version sind, nutzen Sie die neue Erfahrung. Wenn Sie bereits Kunde sind, hängt es davon ab, ob Sie die neue Erfahrung verwenden, ob Ihr Administrator die Funktionsaktualisierung **Neues Verkaufspreiserlebnis** auf der Seite **Funktionsverwaltung** akualisiert hat. Weitere Informationen finden Sie unter [Bevorstehende Funktionen im Voraus aktivieren](/dynamics365/business-central/dev-itpro/administration/feature-management).

Preis- und Rabattstrategien für den Kauf und Verkauf von Artikeln und Dienstleistungen sind grundlegende Instrumente für erfolgreiche Unternehmen. Nachdem Sie die Artikel und Dienstleistungen eingerichtet haben, die Ihr Unternehmen kauft und verkauft, können Sie festlegen, was Sie dafür bezahlen oder berechnen. Diese Beträge werden automatisch zu den Verkaufs- und Kaufdokumenten hinzugefügt. 

## <a name="setting-up-prices-and-discounts"></a>Preise und Rabatte einrichten
Bevor Sie Preislisten erstellen, müssen Sie Ihre Preis- und Rabattstrategien auf den Seiten **Debitoren & Verkauf Einr.** und **Kreditoren & Einkauf Einr.** definieren.

Sie könne zwei Arten von Rabatten einrichten und verwenden:

| Rabattart | Beschreibung |
| --- | --- |
| **Zeilenrabatt** |Ein Rabattbetrag, der für Zeilen in Verkaufs- und Kaufbelegen angegeben wird. In der Regel basieren Zeilenrabatte auf einer Kombination aus Kunde, Artikel, Mindestmenge, Maßeinheit oder Zeitraum, die Sie für Verkäufe und Einkäufe auf den Seiten **Debitoren & Verkauf Einr.** und **Kreditoren & Einkauf Einr.** definieren.|
| **Rechnungsrabatt** |Ein Rabattprozentsatz, der von der Gesamtsumme des Verkaufs- und Einkaufsbelegs abgezogen wird, wenn die Summe aller Zeilen des Belegs einen bestimmten Mindestwert übersteigt. |

Da Verkaufszeilenrabatte und Verkaufspreise auf einer Kombination aus Artikel und Debitor bestehen, können Sie diese Konfiguration auch auf der Artikelseite des Artikels eingerichtet werden, für den die Regeln und Werte gelten.

> [!TIP]  
> Wenn ein Artikel nie mit einem Rabatt verkauft werden sollte, lassen Sie die Skontofelder auf der Artikelseite leer und schließen Sie den Artikel nicht in einer Zeilenrabatteinrichtung ein.

## <a name="about-price-lists"></a>Über Preislisten
Preislisten sind flexibel und ermöglichen es Ihnen, den Geschäftspartner oder die Aktivität anzugeben, für die sie gelten. Sie können beispielsweise eine Preisliste erstellen, die für alle Anbieter und Kunden gilt, oder für jeden Geschäftspartner Sonderpreise oder Rabatte anbieten, möglicherweise basierend auf einer Mindestmenge bei Kauf- oder Kundenaufträgen oder einer bestimmten Kombination von Kunden, Artikeln, Mindestmenge, Maßeinheit oder Zeiträume. Die von Ihnen definierten Preise und Rabatte werden automatisch auf Kauf- und Verkaufsbelege angewendet. 

## <a name="set-up-prices"></a>Preise einrichten

Diese Schritte unterscheiden sich je nachdem, ob Ihr Administrator das Feature-Update **Neues Verkaufspreiserlebnis** aktiviert hat. 

#### <a name="current-experience"></a>[Aktuelle Erfahrung](#tab/current-experience)  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Debitoren** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Debitor und dann die Aktion **Preise**.
3. Füllen Sie die Felder in der Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Füllen Sie eine Zeile für jede Kombination aus, die dem Debitor einen besonderen Preis gewährt.

#### <a name="new-experience"></a>[Neue Erfahrung](#tab/new-experience)  
Sie können Elemente und Dienste für jede Zeile manuell hinzufügen oder die Aktion **Zeilen vorschlagen** zum Erstellen neuer Preise für ausgewählte Artikel, Artikelrabattgruppen, Ressourcen und andere Produkttypen verwenden. Wenn Sie **Zeilen vorschlagen**, auf der Seite **Preiszeilen – Neu erstellen** wählen, können Sie mithilfe von Filtern die Artikel oder Dienstleistungen auswählen, die in die Preisliste aufgenommen werden sollen. Sie können auch angeben, ob bei der Preisberechnung eine Mindestmenge berücksichtigt werden soll, der Anpassungsfaktor für neue Preislistenzeilen und die Rundungsmethode für Preise. 

Standardmäßig lautet der Status neuer Preislisten **Entwurf**. Wenn Sie bereit sind, die Liste zu verwenden, können Sie den Status in **Aktiv** ändern.

Um Preislisten und Preise zu überprüfen, die für bestimmte Kunden oder Lieferanten gelten, klicken Sie auf den Seiten **Kunde** oder **Verkäufer** entweder auf die Aktion **Verkaufspreislisten** oder **Kaufpreislisten**. Für Artikel und Ressourcen können Sie Preislistenzeilen anzeigen, indem Sie **Verkaufspreise** oder **Kaufpreise** auf den Seiten **Artikel** und **Ressource**.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Debitor** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Debitor und dann die Aktion **Verkaufspreislisten**. 
3. Wählen Sie **Neu**, um eine neue Verkaufspreisliste zu erstellen.
4. Füllen Sie bei Bedarf die Felder in den Inforegistern **Allgemein** und **Steuern** aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Führen Sie einen der folgenden Schritte aus, um Elemente zur Liste hinzuzufügen:
   * Um viele Elemente hinzuzufügen, wählen Sie **Linien vorschlagen**. Geben Sie anschließend Filterkriterien ein, um die hinzuzufügenden Elementtypen anzugeben. Optional können Sie auch einige zusätzliche Einstellungen für die Artikel eingeben, die für die Preisliste spezifisch sind. Bei Bedarf können Sie diese später ändern.
   * Um Artikel aus einer anderen Preisliste zu kopieren, wählen Sie **Zeilen kopieren** und wählen Sie dann die zu kopierende Preisliste aus.
   * Um Elemente manuell hinzuzufügen, wählen Sie im Feld **Produkt-Typ** den Produkttyp aus, für den die Preisliste bestimmt ist. Füllen Sie je nach Auswahl die restlichen Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Um die Preisliste zu verwenden, klicken Sie auf das Feld **Status** und wählen Sie **Aktiv**.  

---

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

---

## <a name="working-with-invoice-discounts-and-service-charges"></a>Arbeiten mit Rechnungsrabatten und Servicegebühren
Wenn Sie Rechnungsrabatte verwenden, bestimmt die Höhe des Rechnungsbetrages die Höhe des Rabattes, der gewährt wird. Auf der Seite **Rechnungsrabatte** können Sie eine Servicegebühr für Rechnungen über einem bestimmten Betrag einrichten.  <!--The Invoice Discounts page is hard to find.-->

Bevor Sie Rechnungsrabatte mit Verkäufen verwenden können, müssen Sie einige Informationen in der Anwendung eingeben. Sie müssen entscheiden, welchen Kunden diese Art von Rabatt gewährt wird und welche Rabattprozentsätze Sie verwenden.  

Wenn die Anwendung Rechnungsrabatte automatisch berechnen soll, können Sie dies auf der Seite **Debitoren & Verkauf Einr.** einrichten.  

Sie können für jeden Debitor angeben, ob Sie Rechnungsrabatte gewähren möchten, wenn die Anforderungen erfüllt sind (d. h. der Rechnungsbetrag groß genug ist). Sie können die Bedingungen für Rechnungsrabatte für inländische Debitoren in der Mandantenwährung und für ausländische Debitoren in Fremdwährung festlegen.  

Sie verknüpfen Rabattprozentsätze mit bestimmten Rechnungsbeträgen auf der Seite **Rechnungsrabatte**. Sie können so viele Prozentsätze wie notwendig eingeben. Jeder Debitor kann eine eigene Seite haben, oder Sie können verschiedene Debitoren mit der gleichen Seite verknüpfen.  

Zusätzlich (oder anstatt) eines Rabattprozentsatzes können Sie eine Servicegebühr mit einem bestimmten Rechnungsbetrag verknüpfen.  

> [!TIP]  
> Bevor Sie mit der Eingabe dieser Informationen beginnen, sollten Sie Ihre Rabattstruktur im Voraus vorbereiten, damit Sie leichter erkennen können, welche Kunden auf dieselbe Rechnungsrabatt-Seite verlinken sollen. Weitere Informationen zu Rabatten bei Verkäufen finden Sie unter [Einrichten von Rabatten für Ihre Kunden](/learn/modules/customer-discounts-dynamics-365-business-central/index) unter Microsoft Learn.  

### <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Um Rechnungsrabattkonditionen für Einkäufe einzurichten
Wenn Sie sich entschieden haben, welche Debitoren für Rechnungsrabatte in Frage kommen, geben Sie die Rechnungsrabattcodes auf den Debitorenkarten ein, und richten Sie die Bedingungen für die einzelnen Codes ein.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Debitor** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Kundenseite für einen Debitor, der für Rechnungsrabatte in Frage kommt.
3. Geben Sie im Feld **Rechnungsrabattcode** einen Code für das jeweilige Rechnungsrabattfenster ein, das die Anwendung verwenden soll, um Rechnungsrabatte für den Debitor zu berechnen. <!--Looks like I can only choose customers in this list-->

> [!NOTE]  
> Rechnungsrabattcodes werden durch BestandsDebitorenkarten dargestellt. Dies ermöglicht es Ihnen, Rechnungsrabattbedingungen schnell einem Debitor zuzuweisen, indem es den Namen eines anderen Debitors mit den selben Konditionen auswählt.

Fahren Sie fort, um neue Verkaufsrechnungsrabatt-Bedingungen einzurichten.

1. Auf der Seite **Debitoren** wählen Sie die Aktion **Rechnungsrabatt** aus. Die Seite **Debitorenrechnungsrabatte** wird geöffnet.
2. Geben Sie in dem Feld **Währungscode** den Code für die Währung ein, für die die Rechnungsrabattkonditionen gelten sollen. Wenn Sie Rechnungsrabattbedingungen in EUR einrichten möchten, dann lassen Sie das Feld leer.
3. Geben Sie im Feld **Minimalbetrag** den Mindestbetrag ein, den eine Rechnung aufweisen muss, um für einen Rabatt in Frage zu kommen.
4. Geben Sie im Feld **Rabatt** den Rechnungsrabatt als Prozentsatz des Rechnungsbetrages ein.
5. Wiederholen Sie die Schritte 5 bis 7 für jede Währung, für die der Debitor einen Rechnungsrabatt erhält.

Der Rechnungsrabatt wird jetzt eingerichtet und dem fraglichen Debitor zugewiesen. Wenn Sie den Debitorencode im Feld **Rechnungs-Rabattcode** für andere Debitorenkarten auswählen, wird derselbe Rechnungsrabatt diesen Debitoren zugewiesen.

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

## <a name="calculating-the-best-price"></a>Den besten Preis berechnen
Falls Sie spezielle Preise und Zeilenrabatte für Verkäufe und Einkäufe erfasst haben, stellt [!INCLUDE[d365fin](includes/d365fin_md.md)] sicher, dass der Deckungsbeitrag im Artikelhandel immer optimal ist, indem er die besten Preise automatisch in Einkaufs- und Verkaufsbelegen und auf Projekt und Artikel Buch.-Blattzeilen berechnet. Weitere Informationen finden Sie unter [Beste Preisberechnung](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

## <a name="see-also"></a>Siehe auch
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
