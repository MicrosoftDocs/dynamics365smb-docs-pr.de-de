---
title: Einen Verkaufsauftrag erstellen und Produkte verkaufen
description: 'Beschreibt, wie Sie einen Verkaufsauftrag erstellen, einen Vertrag mit einem Debitoren erfassen, Produkte unter bestimmten Bedingungen verkaufen oder kaufen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'trade, partial deliveries, customer sales order, shipping advice, partial shipments,'
ms.search.form: '42, 48, 9305'
ms.date: 09/02/2022
ms.author: edupont
---
# <a name="sell-products-with-a-customer-sales-order" />Produkte mit einem Debitorenauftrag verkaufen

Dieser Artikel bietet Hilfestellungen dazu, wann ein Debitorenauftrag zusätzlich zu einer Rechnung verwendet werden sollte. Wenn der Verkaufsprozess erfordert, dass Sie nur Teile einer Bestellmenge liefern, weil beispielsweise die vollständige Menge nicht sofort verfügbar ist, müssen Sie diesen Verkauf mittels eines Verkaufsauftrags verarbeiten.

Sie müssen auch Verkaufsaufträge verwenden, wenn Sie Artikel als Direktlieferung verkaufen, indem Sie direkt von Ihrem Kreditor an Ihren Debitor versenden. Erfahren Sie mehr unter [Direktlieferungen machen](sales-how-drop-shipment.md). In allen anderen Aspekten ist das Vorgehen bei Verkaufsaufträgen gleich wie bei Verkaufsrechnungen. Erfahren Sie mehr unter [Fakturieren eines Verkaufs](sales-how-invoice-sales.md).

Wenn Sie die Produkte teilweise oder gesamthaft liefern, buchen Sie die Verkaufsrechnung oder den Verkaufsauftrag als geliefert oder als geliefert und fakturiert, um den zugehörigen Artikel und die Debitorenposten im System zu erfassen. Wenn Sie den Verkaufsauftrag, können Sie ihn als PDF-Dateianhang auch senden. Sie können den E-Mail-Text mit einer Zusammenfassung des Auftrags und der Zahlungsinformationen, wie ein Link zu PayPal automatisch ausfüllen lassen. Erfahren Sie mehr unter [Artikel versenden](warehouse-how-ship-items.md) und [Dokumente per E-Mail versenden](ui-how-send-documents-email.md).

In Geschäftsumgebungen, wo Debitoren sofort bezahlen, beispielswiese mit PayPal oder Bargeld, wenn eine Zahlung sofort erfasst wird, wenn Sie die Verkaufsrechnung buchen, das heißt die gebuchte Verkaufsrechnung. wird geschlossen als vollständig ausgeglichen. Wählen Sie im Inforegister Zahlungen im Feld **Zahlungsformcode** den entsprechenden Code aus. Siehe dazu auch Schritt 5 unten. Für elektronischen Zahlungsverkehr wie PayPal müssen Sie das Feld **Zahlungsverkehr** ausfüllen. Erfahren Sie mehr unter [Aktivieren von Debitoren-Zahlungen durch Zahlungsverkehr](sales-how-enable-payment-service-extensions.md).

Sie können direkt gezahlte Rechnungen für nicht-registrierte Debitoren auch erstellen, indem Sie eine Bargelddebitoren-Karte einrichten, auf der Sie auf die Verkaufsrechnung hinweisen. Erfahren Sie mehr unter [Bardebitoren einrichten](finance-how-to-set-up-cash-customers.md).

## <a name="create-a-sales-order" />Einen Verkaufsauftrag erstellen

> [!NOTE]  
> Beim nachfolgenden Verfahren wird davon ausgegangen aus, dass der Debitor bereits eingerichtet ist. Anweisungen dazu finden Sie unter [Neue Debitoren registrieren](sales-how-register-new-customers.md).

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie **Neu** aus, um einen neuen Eintrag zu erstellen.
3. Geben Sie im Feld **Debitor** den Namen eines vorhandenen Debitors ein.

    Andere Felder auf der Seite **Verkaufsangebot** werden nun mit den Standardinformationen zum ausgewählten Debitor ausgefüllt.  

4. Füllen Sie auf der Seite **Verkaufsauftrag** die Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Wenn Sie dem Debitor ermöglichen, sofort mit Kreditkarte oder PayPal zu bezahlen, dann füllen Sie das Feld **Zahlungsformcode** aus. Die Zahlung wird dann erfasst, sobald Sie die Verkaufsrechnung buchen. Wenn Sie *Kasse* auswählen, wird die Zahlung in einem angegebenen Gegenkonto erfasst.

    Sie sind nun bereit, die Verkaufsangebotszeilen mit Lagerartikeln oder Services auszufüllen, die Sie an den Debitoren verkaufen möchten.

    Wenn Sie wiederkehrende Verkaufszeilen für den Debitor wie einen Monatsersatzauftrag, eingerichtet haben, können Sie diese Zeilen auf der Rechnung durch Auswählen der Schaltfläche **Wiederkehrende Verkaufszeilen holen** einfügen.
5. Wählen Sie auf dem Inforegister **Zeilen** im Feld **Typ** aus, welche Art von Produkt, Gebühr oder Transaktion Sie für den Kunden mit der Verkaufszeile buchen möchten.

6. Geben Sie im Feld **Nr.** die Nummer eines Lagerartikels oder Dienstes ein.

    Sie lassen das **Nr.** Feld leer, wenn die Zeile für Folgendes ist:

    * Kommentar. Die Bemerkung im Feld **Beschreibung** enthalten ist.
    * Katalogartikel. Wählen Sie die Aktion **Katalogartikel auswählen**. Erfahren Sie mehr unter [Mit Katalogelementen arbeiten ](inventory-how-work-nonstock-items.md).
7. Geben Sie in dem Feld **Menge** die Anzahl des Artikels an, der verkauft werden soll.

    > [!NOTE]  
    > Für Artikel des Typs *Ressource* oder *Service* ist die Menge eine Zeiteinheit wie Stunden, wie im Feld **Einheitencode** der Zeile angegeben. Weitere Informationen finden Sie unter [Einrichten von Einheiten](inventory-how-setup-units-of-measure.md).

    Das Feld **Zeilenmenge** wird aktualisiert, um den Wert im Feld **VK-Preis** multipliziert ist mit dem Zahl im Feld **Menge** anzuzeigen.

    Der Preis und der Zeilenbetrag auf den Verkaufsrechnungszeilen werden mit oder ohne MwSt. angezeigt je nachdem, was Sie im Feld **Preis inklusive Mehrwertsteuer** auf der Debitorenkarte ausgewählt haben.
8. Geben Sie im Feld **Zeilenrabatt in Prozent** einen Prozentsatz ein, wenn Sie dem Debitor einen Rabatt auf das Produkt gewähren möchten. Der Wert im Feld **Zeilenbetrag** wird entsprechend aktualisiert.

    Wenn Sie bestimmte Artikelpreise für den Debitor auf dem Inforegister **Verkaufspreise und Verkaufspreis-Zeilenrabatte** eingerichtet haben, werden der Preis und der Betrag auf der Rechnungszeile automatisch aktualisiert, wenn die vereinbarten Preiskriterien erfüllt sind. Erfahren Sie mehr unter [Erfassen von Verkaufspreisen, Skonti und Zahlungsvereinbarungen](sales-how-record-sales-price-discount-payment-agreements.md).
9. Um einen Kommentar zur Bestellzeile hinzuzufügen, den der Debitor auf dem gedruckten Verkaufsauftrag sehen kann, schreiben Sie einen Kommentar in die leere Zeile im Feld **Beschreibung**.  
10. Wiederholen Sie die Schritte 5 bis 9 für jedes Element, das Sie an den Kunden verkaufen möchten.

    Die Summenfelder unter den Positionen werden automatisch aktualisiert, wenn Sie Positionen erstellen oder ändern, um die Beträge anzuzeigen, die auf die Sachkonten gebucht werden.

    > [!NOTE]
    > In sehr seltenen Fällen können die gebuchten Beträge von den in den Summenfeldern angezeigten Beträgen abweichen. Dies ist in der Regel auf Rundungsrechnungen in Bezug auf Mehrwertsteuer oder Verkaufssteuer zurückzuführen.
    >
    > Verwenden Sie zum Übeprüfen der tatsächlich gebuchten Beträge die Seite **Statistiken**, die die Rundungsberechnungen berücksichtigt. Auch wenn Sie die Aktion **Freigabe** auswählen, werden die Summenfelder aktualisiert, sodass sie die Rundungsberechnungen enthalten.  

11. Optional geben Sie im Feld **Rabattbetrag in Rechnung stellen** einen Betrag ein, der vom Wert abgezogen werden soll, der im Feld **Total inklusive Mehrwertsteuer** im unteren Bereich der Rechnung angezeigt wird.

    Wenn Sie Rechnungsrabatte für den Debitor eingerichtet haben, wird der angegebene Prozentwert automatisch in das Feld **Rechnungsrabatt in Prozent** eingetragen, sobald die Kriterien erfüllt sein, und der entsprechende Betrag wird im Feld **Rechnungsbetrag mit Rabatt ohne Mehrwertsteuer** eingefügt. Erfahren Sie mehr unter [Erfassen von Verkaufspreisen, Skonti und Zahlungsvereinbarungen](sales-how-record-sales-price-discount-payment-agreements.md).
12. Um nur einen Teil der Auftragsmenge zu liefern, geben Sie die Menge im Feld **Menge für Versand** ein. Der Wert wird in das Feld **Zu fakturierende Menge** automatisch kopiert.

    > [!NOTE]
    > Wenn das Feld **Versandhinweis** auf **Vollständig** im Inforegister **Versand und Rechnungsstellung** gesetzt ist, können Sie keine Teillieferungen buchen. Erfahren Sie mehr unter [Teillieferungen verarbeiten](sales-how-send-partial-shipments.md).
13. Um nur einen Teil der Auftragsmenge zu fakturieren, geben Sie die Menge im Feld **Menge für Fakturierung** ein. Die zu fakturierende Menge kann nicht größer sein, als der Wert im Feld **Menge geliefert**.  
14. Wenn die Verkaufsangebotszeilen ausgeführt werden, wählen Sie die Aktion **Buchen und Senden** aus.

[!INCLUDE [order-ship-invoice](includes/order-ship-invoice.md)]

Das Dialogfeld **Buchungs- und Sendebestätigung** zeigt die gewünschte Methode des Debitors das Empfangen von Belegen an. Sie können die Sendemethode ändern, indem Sie die Schaltfläche vom Feld **Beleg senden an** auswählen. Erfahren Sie mehr unte r[Belegsendeprofile einrichten](sales-how-setup-document-send-profiles.md)

Der zugehörige Artikel und die Debitorenposten werden nun im System erfasst erstellt, und das Verkaufsangebot wird als PDF-Dokument ausgegeben. Wenn der Auftrag vollständig gebucht wird, wird er aus der Liste von Verkaufsaufträgen entfernt und durch neue Belege in der Übersicht der gebuchten Verkaufsrechnungen und in der Liste gebuchter Auftragslieferungen ersetzt.  

## <a name="external-document-number" />Externe Belegnummer

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-related-microsoft-training" />Siehe verwandte [Microsoft Schulungen](/training/modules/create-sales-documents-dynamics-365-business-central/)

## <a name="see-also" />Siehe auch

[Fakturieren eines Verkaufs](sales-how-invoice-sales.md)  
[Verkäufe buchen](ui-post-sales.md)  
[Versenden von Artikeln](warehouse-how-ship-items.md)  
[Direktlieferungen machen](sales-how-drop-shipment.md)  
[Verkauf](sales-manage-sales.md)  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Kommissionierliste drucken](sales-how-print-picking-list.md)  
[Teillieferungen verarbeiten](sales-how-send-partial-shipments.md)  
[Bestand](inventory-manage-inventory.md)  
[Dokumente per E-Mail versenden](ui-how-send-documents-email.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
