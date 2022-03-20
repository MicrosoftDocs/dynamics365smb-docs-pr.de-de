---
title: Verkaufspreise und Rabatte für Debitoren einrichten | Microsoft Docs
description: Beschreibt das Einrichten und Anwenden von Preis- und Rabattvereinbarungen für Verkaufsbelege.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.search.form: 1345, 7002, 7007, 7015, 7016, 7023
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: acba6dc39b57788541a36540f443d02a25bc610c
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2022
ms.locfileid: "8384176"
---
# <a name="record-sales-prices-and-discounts"></a>Verkaufspreise und Rabatte aufzeichnen
> [!NOTE]
> In Veröffentlichungszyklus 2 von 2020 haben wir optimierte Prozesse zum Einrichten und Verwalten von Preisen und Rabatten veröffentlicht. Wenn Sie ein neuer Kunde mit dieser Version sind, nutzen Sie die neue Erfahrung. Wenn Sie bereits Kunde sind, hängt es davon ab, ob Sie die neue Erfahrung verwenden, ob Ihr Administrator die Funktionsaktualisierung **Neues Verkaufspreiserlebnis** in **Funktionsverwaltung** akualisiert hat. Weitere Informationen finden Sie unter [Bevorstehende Funktionen im Voraus aktivieren](/dynamics365/business-central/dev-itpro/administration/feature-management).

[!INCLUDE[prod_short](includes/prod_short.md)] unterstützt verschiedene Preisstrategien, angefangen von One-Price-Fits-All-Modellen, bei denen ein Artikel immer zum gleichen Preis verkauft wird, bis hin zu speziellen Preisvereinbarungen mit bestimmten Debitoren, Debitorengruppen oder Sonderangeboten bei der Durchführung einer Verkaufsaktion. Sie können beispielsweise unter den folgenden Bedingungen einen Sonderpreis für einen Bestellungsauftrag anbieten:

* Wenn es um eine Mindestmenge geht
* Es ist für eine bestimmte Art von Artikel  
* Wenn es während eines bestimmten Zeitraums erstellt wurde

Um ein einfaches Preismodell zu verwenden, müssen Sie nur einen Einheitspreis für einen Artikel oder eine Ressource angeben. Dieser Preis wird immer für Verkaufsbelege verwendet. Bei fortgeschritteneren Modellen, zum Beispiel, wenn Sie eine Verkaufsaktion durchführen und Sonderpreise anbieten möchten, können Sie die Kriterien dafür auf der Seite **Verkaufspreise** angeben. Sie können Sonderpreise anbieten, die auf folgenden Kombinationen basieren: 

* Debitor
* Artikel
* Einheit
* Mindestmenge
* Zeiträume, die definieren, wann die Preise gültig sind

Nachdem Sie Sonderpreise eingerichtet haben, kann [!INCLUDE[prod_short](includes/prod_short.md)] automatisch den besten Preis für Verkaufs- und Einkaufsbelege sowie für Auftrags- und Artikelerfassungszeilen berechnen. Weitere Informationen finden Sie unter [Beste Preisberechnung](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).  

Für die Verkaufsrabatte können Sie folgende Arten einrichten und verwenden:

| Rabattart | Beschreibung |
| --- | --- |
| **Verkaufszeilenrabatt** |Ein Betrag mit Rabatt wird auf den Verkaufszeilen eingefügt, wenn eine bestimmte Kombination aus Debitor, Artikel, Mindestmenge, Einheit oder des Start- und Enddatums vorhanden ist. Diese Kombinationen gelten auf gleiche Weise für Verkaufsbelege. |
| **Rechnungsrabatt** |Ein Rabattprozentsatz, der von der Gesamtsumme des Verkaufsbelegs abgezogen wird, wenn die Summe aller Zeilen des Belegs einen bestimmten Mindestwert übersteigt. |

> [!TIP]  
> Wenn ein Artikel nie mit einem Rabatt verkauft werden sollte, lassen Sie die Skontofelder auf der Artikelseite leer und schließen Sie den Artikel nicht in einer Zeilenrabatteinrichtung ein.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Um Verkaufspreise für einen Debitor zu erstellen:

Diese Schritte unterscheiden sich je nachdem, ob Ihr Administrator das Feature-Update **Neues Verkaufspreiserlebnis** aktiviert hat. Wenn das Funktionsupdate nicht aktiviert ist, befolgen Sie die Schritte auf der Registerkarte "Aktuelle Erfahrung". 

## <a name="current-experience"></a>[Aktuelle Erfahrung](#tab/current-experience)

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Debitoren** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Debitor und dann die Aktion **Preise**.
3. Füllen Sie die Felder in der Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Füllen Sie eine Zeile für jede Kombination aus, die dem Debitor einen besonderen Preis gewährt.

## <a name="new-experience"></a>[Neue Erfahrung](#tab/new-experience)  
Standardmäßig lautet der Status neuer Preislisten Entwurf. Preislistenentwürfe gehen nicht in die Preiskalkulation ein. Wenn Sie mit dem Hinzufügen von Zeilen fertig sind und die Preise verwenden möchten, können Sie den Status in Aktiv ändern.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Debitoren** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Debitor und dann die Aktion **Verkaufspreislisten**. 
3. Wählen Sie **Neu**, um eine neue Verkaufspreisliste zu erstellen.
4. Füllen Sie bei Bedarf die Felder in den Inforegistern **Allgemein** und **Steuern** aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Sie haben folgende Möglichkeiten, um Artikel der Liste hinzuzufügen:
   * Um viele Elemente hinzuzufügen, wählen Sie **Linien vorschlagen**. Geben Sie anschließend Filterkriterien ein, um die hinzuzufügenden Elementtypen anzugeben. Optional können Sie weitere Einstellungen für die Artikel vornehmen. Diese Einstellungen sind preislistenspezifisch. Bei Bedarf können Sie diese später ändern.
   * Um Artikel aus einer anderen Preisliste zu kopieren, wählen Sie **Zeilen kopieren** und wählen Sie dann die zu kopierende Preisliste aus.
   * Um Elemente manuell hinzuzufügen, wählen Sie im Feld einer Zeile **Produkt-Typ** den Produkttyp aus, für den die Preisliste bestimmt ist. Füllen Sie je nach Auswahl die restlichen Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Um die Preisliste zu verwenden, klicken Sie auf das Feld **Status** und wählen Sie **Aktiv**.  

---

## <a name="using-sales-and-purchase-price-lists"></a>Verwenden von Verkaufs- und Einkaufspreislisten
> [!NOTE]
> Die Verwendung von Preislisten erfordert, dass Ihr Administrator das Funktionsupdate **Neue Verkaufspreis-Erfahrung** in der **Funktionsverwaltung** aktiviert. Weitere Informationen finden Sie unter [Bevorstehende Funktionen im Voraus aktivieren](/dynamics365/business-central/dev-itpro/administration/feature-management).

Die **Ausgleich mit Typ** und **Ausgleich mit Nummer** In den Feldern können Sie auswählen, für was eine Preisliste gelten soll, z. B. Debitor oder Debitorenpreisgruppe. Mit **Spalten anzeigen für** können Sie Spalten anzeigen, die nur für Preise, Rabatte oder Preise und Rabatte relevant sind.

### <a name="converting-existing-prices-when-you-turn-on-the-pricing-feature-update"></a>Konvertieren vorhandener Preise, wenn Sie die Aktualisierung der Preisfunktion aktivieren
Wenn Sie das Funktionsupdate **Neue Verkaufspreis-Erfahrung** auf der Seite **Funktionsverwaltung** aktivieren, wird die Anleitung **Funktionsdatenupdate** geöffnet. Verwenden Sie den Umschalter **Standardpreise verwenden** wie folgt:

* Wenn Sie mit allen Preisen auf einer einzigen Seite arbeiten möchten, aktivieren Sie sie. Vorhandene Preise werden für jeden der folgenden Punkte in eine Standardpreisliste umgewandelt:

    * Verkauf
    * Einkauf
    * Projektumsätze
    * Projekteinkäufe 

    Anschließend können Sie alle Preise für diese Bereiche auf der Seite **Preise Arbeitsblatt** bearbeiten. Die Standardpreislisten werden auf den Seiten **Einrichtung von Verkäufen und Forderungen**, **Einrichtung von Käufen und Verbindlichkeiten** und **Projekteinrichtung** festgelegt. 

    > [!NOTE]
    > Wenn Preise nur für Artikel- oder Ressourcenkarten festgelegt sind, werden die Standardpreislisten während der Datenaktualisierung nicht mit diesen Preisen ausgefüllt. Sie können jedoch jede der Standardpreislisten oder die Seite Preisarbeitsblatt öffnen und die Aktion **Zeilen vorschlagen** nutzen, um die auf Artikel- oder Ressourcenkarten festgelegten Preise hinzuzufügen. 

* Um Verkaufspreislisten zu verwenden, deaktivieren Sie sie. Bestehende Preise werden für jede Kombination aus Debitor, Debitorengruppe oder Kampagne sowie Start- und Enddatum und Währung in eine neue Preisliste umgewandelt. Wenn Sie viele Kombinationen haben, haben Sie viele Preislisten.

Wenn Sie die neue Preisgestaltung bereits aktiviert haben, können Sie Standardpreislisten manuell erstellen oder eine vorhandene Preisliste als Standard angeben. Um eine vorhandene Preisliste als Standard festzulegen, aktivieren Sie den Schalter **Aktualisieren von Standardeinstellungen zulassen** auf der Preisliste. Setzen Sie dann auf den Seiten **Einrichtung von Verkäufen und Forderungen**, **Einrichtung von Käufen und Verbindlichkeiten** und **Projekteinrichtung** die Preisliste als standardmäßig.

## <a name="editing-active-price-lists"></a>Bearbeiten der aktiven Preislisten
Damit Bearbeiter Preise in aktiven Preislisten für Artikel, Ressourcen, Debitoren, Kreditoren und andere Entitäten, die Preise verwenden, bearbeiten können, aktivieren Sie den Umschalter **Bearbeiten des aktiven Preises zulassen** auf den Seiten **Einrichtung von Verkäufen und Forderungen** und **Einrichtung von Käufen und Verbindlichkeiten**. 

Wenn der Umschalter **Bearbeiten des aktiven Preises zulassen** deaktiviert ist, müssen Sie, um Preise in einer Preisliste zu aktualisieren, den Status der Preisliste in **Entwurf** ändern, Ihre Änderung vornehmen und die Preisliste erneut aktivieren.

Die **Preisübersicht** Seite bietet eine Übersicht über alle Preise in Preislisten. Sie können Filter festlegen, um die Liste einzugrenzen. Nachdem Sie die Preise geändert haben, verwenden Sie die Aktion **Zeilen überprüfen**, um die Preise mit anderen Preislistenzeilen zu vergleichen. Die Überprüfung der Preise hilft beispielsweise, doppelte oder widersprüchliche Preise zu vermeiden. 

> [!NOTE]
> Wenn Sie eine Zeile in einer aktiven Preisliste bearbeiten, wird der Status der Zeile Entwurf und die Zeile wird erst in die Preisberechnung einbezogen, bis Sie die Aktion **Zeilen überprüfen** verwenden. Nachdem Sie den Preis überprüft haben, wird der Status der Position Aktiv und in Preisberechnungen verwendet.

Um neue Preise hinzuzufügen, verwenden Sie auf der Seite **Preisübersicht** die Aktion **Neue Zeilen hinzufügen**. Die Seite **Preise Arbeitsblatt** wird geöffnet, auf der Sie wie folgt Preiszeilen hinzufügen:

* Indem Sie sie anhand von Kriterien vorschlagen
* Kopieren von anderen Preislisten
* Geben Sie sie manuell ein. 

Danach können Sie die Aktion **Preisänderung implementieren** verwenden, um die neuen Preise mit anderen Preislisten zu vergleichen, um Dubletten zu vermeiden.

## <a name="to-copy-sales-prices"></a>Verkaufspreise kopieren
Diese Schritte unterscheiden sich je nachdem, ob Ihr Administrator das Feature-Update **Neues Verkaufspreiserlebnis** aktiviert hat. Wenn das Funktionsupdate nicht aktiviert ist, befolgen Sie die Schritte auf der Registerkarte "Aktuelle Erfahrung".

## <a name="current-experience"></a>[Aktuelle Erfahrung](#tab/current-experience)  

Falls Sie Verkaufspreise kopieren möchten, wie z. B. den Preis eines einzelnen Debitors, um ihn in einer Debitorengruppe zu verwenden, müssen Sie die Stapelverarbeitung **VK-Preis vorschlagen** ausführen. Batchauftrag auf der Seite **Verkaufspreisarbeitsblatt**.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Verkaufspreisarbeitsblatt** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie den **Vorgeschlagenen Verkaufspreis auf dem Arbeitsblatt.** Aktion  
3. Füllen Sie im Inforegister **Verkaufspreise** die Felder mit der **Verkaufsart** und dem **Verkaufscode** der ursprünglichen Preise aus, die Sie kopieren möchten.  
4. Füllen Sie im oberen Bereich der Anforderungsseite die Felder **Verkaufsart** und **Verkaufscode** mit der Art und dem Namen aus, in die Sie die Verkaufspreise kopieren möchten.  
5. Wenn Sie mit dem Batchauftrag neue Preise erstellen wollen, wählen Sie in das Feld **Neue Preise generieren**.  
6. Wählen Sie die Schaltfläche **OK**, um die Zeilen auf der Seite **VK-Preisarbeitsblatt** mit den neuen Preisvorschlägen auszufüllen, und geben Sie an, dass diese für die gewählte Verkaufsart gültig sind.  

   > [!NOTE]  
   > Die Stapelverarbeitung erzeugt nur Vorschläge, implementiert die vorgeschlagenen Änderungen aber nicht. Falls Sie die Vorschläge annehmen möchten, d. h. sie auf die Seite **VK-Preise** übernehmen möchten, können Sie die Aktion **Preisvorschlag übernehmen** verwenden, die Sie …auf der Seite **VK-Preisarbeitsblatt** finden.

## <a name="new-experience"></a>[Neue Erfahrung](#tab/new-experience)  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Verkaufspreislisten** ein und wählen Sie dann den zugehörigen Link. 
2. Wählen Sie die zu kopierende Preisliste aus und wählen Sie dann **Zeilen kopieren**.
3. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Sie können nicht zwei Zeilen mit denselben Einstellungen, aber unterschiedlichen Preisen verwenden. In diesem Fall wird eine Meldung angezeigt, wenn Sie eine Preisliste aktivieren. Sie können den zu verwendenden Preis auswählen, indem Sie die Liste öffnen und den falschen Preis löschen.  
  
---

## <a name="to-bulk-update-item-prices"></a>So aktualisieren Sie Debitorenartikelpreise auf einmal
Diese Schritte unterscheiden sich je nachdem, ob Ihr Administrator das Feature-Update **Neues Verkaufspreiserlebnis** aktiviert hat. Wenn das Funktionsupdate nicht aktiviert ist, befolgen Sie die Schritte auf der Registerkarte "Aktuelle Erfahrung".

### <a name="current-experience"></a>[Aktuelle Erfahrung](#tab/current-experience)

Wenn Sie Artikelpreise, wie alle Lagerzugangs-Artikelpreise durch einen Prozentsatz auf einmal aktualisieren möchten, müssen Sie **Verkaufspreisarbeitsblatt** mithilfe der folgenden Batchvorgänge ausfüllen:

* **Artikelpreis auf dem Arbeitsblatt vorschlagen** schlägt Änderungen vor, indem ein Anpassungsfaktor auf vorhandene Verkaufspreise angewendet oder vorhandene Verkaufspreisvereinbarungen auf andere Debitoren, Debitorpreisgruppen oder Verkaufsaktionen kopieren.
* **Artikelpreis auf dem Arbeitsblatt vorschlagen** Schlägt Änderungen vor, indem ein Anpassungsfaktor auf vorhandene Einheitspreise auf Artikelkarten angewendet wird oder indem Preise für neue Kombinationen von Währungen, Maßeinheiten usw. vorgeschlagen werden. Die Einheitspreise der Artikel werden nicht geändert.    

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Verkaufspreisarbeitsblatt** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Artikelpreis auf dem Arbeitsblatt vorschlagen** aus.  
3. Füllen Sie im Inforegister **Artikel** die **Nr.** oder **Bestand-Buchungsgruppe** oder andere Felder mit den ursprünglichen Artikelpreisen aus, die Sie aktualisieren möchten ein.  
4. Füllen Sie im oberen Bereich der Anforderungsseite die Felder **Verkaufsart** und **Verkaufscode** mit der Art und dem Namen aus, in die Sie die Verkaufspreise kopieren möchten.
5. Wenn Sie möchten, dass die Stapelverarbeitung automatisch eingegeben wird, geben Sie Anpassung ein im Feld **Korrekturfaktor**. Beispielsweise geben Sie entsprechend **1.15** unter **Korrekturfaktor** für die Preiserhöhung für den Artikelpreis um **15%** ein.  
6. Wenn Sie mit dem Batchauftrag neue Preise erstellen wollen, aktivieren Sie den Schalter **Neue Preise generieren**.  
7. Wählen Sie **OK**, um die Zeilen auf der Seite **Verkaufspreisarbeitsblatt** mit den vorgeschlagenen neuen Preisen auszufüllen.
8. Um die Vorschläge umzusetzen, verwenden Sie die Aktion **Preisänderungen implementieren**. Der Batch-Job erstellt Vorschläge, setzt diese jedoch nicht um.

## <a name="new-experience"></a>[Neue Erfahrung](#tab/new-experience)

Um die Preise für mehrere Artikel zu aktualisieren, müssen Sie eine neue Preisliste erstellen und dann die Zeilen aus einer vorhandenen Preisliste kopieren. Wenn Sie die Zeilen kopieren, können Sie mithilfe von Filtern angeben, was kopiert werden soll, und Sie können eine Ganzzahl oder eine Dezimalzahl im Feld **Anpassungsfaktor** zum Erhöhen oder Verringern der Preise angeben. Die Preisliste muss sich im Status **Entwurf** befinden. Bei Bedarf können Sie dann die alte Preisliste deaktivieren.

> [!NOTE]
> Sie können nicht zwei Zeilen mit denselben Einstellungen, aber unterschiedlichen Preisen verwenden. In diesem Fall wird eine Meldung angezeigt, wenn Sie eine Preisliste aktivieren. Sie können den zu verwendenden Preis auswählen, indem Sie die Liste öffnen und den falschen Preis löschen.  

---

## <a name="sales-invoice-discounts-and-service-charges"></a>Verkaufsrechnungsrabatte und Servicegebühren
Wenn Sie Rechnungsrabatte verwenden, bestimmt der Gesamtbetrag des Rechnungsbetrages die Höhe des Rabattes, der gewährt wird. Auf der Seite **Debitorenrechnungsrabatte** können Sie eine Servicegebühr für Rechnungen über einem bestimmten Betrag einrichten.  

Wenn Sie Rechnungsrabatte automatisch berechnen möchten, aktivieren Sie auf der Seite **Debitoren & Verkauf Einr.** den Umschalter für **Rechnungsrabatt berechnen**.  

Für jeden Debitor können Sie angeben, ob Sie Rechnungsrabatte anbieten, wenn die Kriterien erfüllt sind. Zum Beispiel, wenn der Rechnungsbetrag groß genug ist. Sie können die Bedingungen für Rechnungsrabatte für inländische Debitoren in der Mandantenwährung und für ausländische Debitoren in Fremdwährung festlegen.  

Sie verknüpfen Rabattprozentsätze mit bestimmten Rechnungsbeträgen auf den Seiten **Debitorenrechnungsrabatte** für jeden Debitor. Sie können eine beliebige Anzahl von Prozentsätzen auf jeder Seite eingeben. Jeder Debitor kann eine eigene Seite haben, oder Sie können verschiedene Debitoren mit der gleichen Seite verknüpfen.  

Zusätzlich (oder anstatt) eines Rabattprozentsatzes können Sie eine Servicegebühr mit einem bestimmten Rechnungsbetrag verknüpfen.  

Weitere Informationen zur Schulung für Rabatte bei Verkäufen finden Sie unter [Einrichten von Rabatten für Ihre Debitoren](/learn/modules/customer-discounts-dynamics-365-business-central/index) unter Microsoft Learn.  

### <a name="calculating-invoice-discounts-on-sales"></a>Rechnungsrabatte bei Verkäufen berechnen

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>So erstellen Sie Verkaufszeilenrabatte für einen Debitor:
Diese Schritte unterscheiden sich je nachdem, ob Ihr Administrator das Feature-Update **Neues Verkaufspreiserlebnis** aktiviert hat. Wenn das Funktionsupdate nicht aktiviert ist, befolgen Sie die Schritte auf der Registerkarte "Aktuelle Erfahrung".

## <a name="current-experience"></a>[Aktuelle Erfahrung](#tab/current-experience)  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die entsprechende Debitorenkarte und klicken dann auf **Zeilenrabatte**.
3. Füllen Sie die Felder in der Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Füllen Sie eine Zeile für jede Kombination aus, die dem Debitor einen besonderen Verkaufszeilenrabatt gewährt.

> [!Note]
> Wenn Sie die Seiten **Verkaufspreise** und **Verkaufszeilenrabatte** von einem bestimmten Debitoren öffnen, werden die Felder **Verkaufsartfilter** und **Verkaufscodefilter** für den Debitor festgelegt und können nicht geändert oder entfernt werden.
>
> Um Preise oder Zeilenrabatte für alle Debitoren, eine Debitorenpreisgruppe oder Kampagne einzurichten, müssen Sie die Seiten von einer Artikelkarte aus öffnen. Verwenden Sie alternativ für Verkaufspreise die Seite **VK-Preisarbeitsblatt**. Weitere Informationen finden Sie unter [So führen Sie eine Sammelaktualisierung von Artikelpreisen durch](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

## <a name="new-experience"></a>[Neue Erfahrung](#tab/new-experience)  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Debitor und dann die Aktion **Verkaufspreislisten**.
3. Öffnen Sie die Preisliste, für die der Zeilenrabatt angegeben werden soll.
4. Erstellen Sie eine neue Zeile oder wählen Sie eine vorhandene Zeile aus und füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Wählen Sie im Feld **Definiert** entweder **Preis und Rabatt** oder einfach **Rabatt**. 
6. Legen Sie im Feld **Zeilenrabatt %** den Rabattprozentsatz fest.

   > [!TIP]
   > Sie können die Zeilen filtern, indem Sie die entsprechende Option im Feld **Spalten anzeigen für** auswählen.   
  
   > [!NOTE]
   > Rechnungsrabattcodes werden durch BestandsDebitorenkarten dargestellt. Das Verwenden von Debitorennamen als Codes ermöglicht es Ihnen, Rechnungsrabattbedingungen schnell einem Debitor zuzuweisen, indem es den Namen eines anderen Debitors mit den selben Konditionen auswählt. Um debitorenspezifische Rechnungsrabattbedingungen einzurichten, setzen Sie das Feld **Rechnungs-Rabatt-Code** auf den Debitorencode des Debitoren und fahren Sie dann mit dem nächsten Schritt fort.

---

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Um Rechnungsrabattkonditionen für Einkäufe einzurichten
Nachdem Sie sich entschieden haben, welche Debitoren für Rechnungsrabatte in Frage kommen, geben Sie die Rechnungsrabattcodes auf den Debitorenkarten ein, und richten Sie die Bedingungen für die einzelnen Codes ein.

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die Debitorenseite für einen Debitor, der für Rechnungsrabatte in Frage kommt.
3. Geben Sie im Feld **Rechnungsrabattcode** einen Code für das jeweilige Rechnungsrabattfenster ein, das die Anwendung verwenden soll, um Rechnungsrabatte für den Debitor zu berechnen. 

> [!NOTE]  
> Rechnungsrabattcodes werden durch BestandsDebitorenkarten dargestellt. Das Verwenden von Debitorennamen als Codes ermöglicht es Ihnen, Rechnungsrabattbedingungen schnell einem Debitor zuzuweisen, indem es den Namen eines anderen Debitors mit den selben Konditionen auswählt.

Nun fahren Sie fort, um neue Verkaufsrechnungsrabatt-Bedingungen einzurichten.

1. Auf der Seite **Debitoren** wählen Sie die Aktion **Rechnungsrabatt** aus. Die Seite **Debitorenrechnungsrabatte** wird geöffnet.
2. Geben Sie in dem Feld **Währungscode** den Code für die Währung ein, für die die Rechnungsrabattkonditionen gelten sollen. Wenn Sie Rechnungsrabattbedingungen in EUR einrichten möchten, dann lassen Sie das Feld leer.
3. Geben Sie im Feld **Minimalbetrag** den Mindestbetrag ein, den eine Rechnung aufweisen muss, um für einen Rabatt in Frage zu kommen.
4. Geben Sie im Feld **Rabatt** den Rechnungsrabatt als Prozentsatz des Rechnungsbetrages ein.
5. Wiederholen Sie die Schritte 5 bis 7 für jede Währung, für die der Debitor einen Rechnungsrabatt erhält.

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