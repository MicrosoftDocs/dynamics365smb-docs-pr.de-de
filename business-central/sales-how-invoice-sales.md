---
title: Fakturieren eines Verkaufs
description: 'Beschreibt, wie Sie einen Verkaufsauftrag erstellen, einen Vertrag mit einem Debitoren erfassen, Produkte unter bestimmten Bedingungen verkaufen oder kaufen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bill, sale, invoice, order'
ms.search.form: '43, 48, 9301'
ms.date: 09/01/2022
ms.author: bholtorf
---
# Fakturieren eines Verkaufs

Sie erstellen entweder eine Verkaufsrechnung oder eine Bestellung, um Ihre Vereinbarung mit dem Debitoren zu erfassen, um bestimmte Produkte unter speziellen Liefer- und Zahlungsbedingungen zu verkaufen.  

Sie müssen jedoch einen Verkaufsauftrag anstelle einer Verkaufsrechnung verwenden, wenn Sie:  

* Nur einen Teil einer Bestellmenge liefern müssen, da z. B. die gesamte Menge nicht verfügbar ist.  
* Produkte versenden, nachdem Sie die entsprechenden Verkaufsrechnungen gebucht haben.
* Artikel verkaufen, die Ihr Kreditor direkt an den Debitor liefert, d. h. bei einer sogenannten Direktlieferung. Erfahren Sie mehr unter [Direktlieferungen machen](sales-how-drop-shipment.md).  

In allen anderen Situationen ist das Vorgehen bei Verkaufsaufträgen gleich wie bei Verkaufsrechnungen. Weitere Informationen zum Verwenden von Verkaufsaufträgen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md).

Sie können mit dem Debitor verhandeln, indem Sie zuerst ein Verkaufsangebot erstellen, das Sie in eine Verkaufsrechnung oder einen Verkaufsauftrag umwandeln können, wenn Sie dem Verkauf zustimmen. Weitere Informationen unter [Verkaufsangebote erstellen](sales-how-make-offers.md)

## Verkaufsrechnung erstellen

Wenn der Debitor entscheidet zu kaufen, senden Sie die Verkaufsrechnung, um die entsprechende Menge und die Wertposten zu erstellen. Wenn Sie die Verkaufsrechnung buchen, können Sie sie als PDF-Dateianhang auch senden. Sie können den E-Mail-Text haben, der mit einer Zusammenfassung der Rechnung und der Zahlungsinformationen, wie ein Link zu PayPal, vorab ausgefüllt wurde. Erfahren Sie mehr unter [Artikel versenden und Dokumente per E-Mail versenden](ui-how-send-documents-email.md). Wenn der Debitor die Rechnung gezahlt hat, können Sie die Zahlung auf verschiedene Arten ausführen, abhängig von der Größe und dem gewünschten Workflow der Organisation. Erfahren Sie mehr unter [Registrierung von Zahlungen](#registering-payments) Sektion.  

Artikelkarten können einen **Bestand**, **Service** und **Nicht-Bestand** haben, wenn die Einheit eine physische Einheit ist, die nicht im Lagerbestand verfolgt wird, Erfahren Sie mehr unter [Registrieren Sie neue Artikel](inventory-how-register-new-items.md). Der Verkaufsrechnungsprozess ist derselbe für alle drei Artikeltypen.

Sie können die oberen Infoboxen des Verkaufsangebotes auf zwei Arten ausfüllen, abhängig davon, ob der Debitor bereits registriert ist. Siehe Schritt 2 im folgenden Verfahren.

### So erstellen Sie eine Verkaufsrechnung

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Verkaufsrechnungen** ein und wählen Sie dann den zugehörigen Link.  
2. Geben Sie im Feld **Debitor** den Namen eines vorhandenen Debitors ein. Wenn der Kunde jedoch neu und daher nicht registriert ist, befolgen Sie diese Schritte, um die Standardkundeninformationen auf der Seote **Verkaufsrechnung** auszufüllen:

    1. Geben Sie im Feld **Debitorname** den Namen eines neuen Debitors ein.
    2. Klicken Sie im Dialogfeld auf **Ja**, um die Übertragung zu bestätigen.
    3. Auf der Seite **Eine Vorlage für einen neuen Debitor auswählen** wählen Sie eine Vorlage, auf der die neue Debitorenkarte basieren soll, und dann wählen Sie **OK**.
    4. Eine neue Debitorenkarte wird geöffnet, vorausgefüllt mit Informationen auf der ausgewählten Debitorenvorlage. Füllen Sie die restlichen Felder aus. Erfahren Sie mehr unter [Registrieren Sie neue Debitoren](sales-how-register-new-customers.md).  
    5. Wenn Sie die Debitorenkarte abgeschlossen haben, wählen Sie die Schaltfläche **Schließen**, um zur Seite **Verkaufsrechnung** zurückzugehen.

   Felder im Verkaufsrechnungskopf werden mit den Informationen, die Sie festgelegt haben, in der neuen Debitorenkarte ausgefüllt.  
3. Füllen Sie auf der Seite **Verkaufsrechnung** die Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Wenn Sie dem Debitor ermöglichen, sofort in bar oder durch PayPal zu bezahlen, dann füllen Sie das Feld **Zahlungsformcode** aus. Die Zahlung wird dann erfasst, sobald Sie die Verkaufsrechnung buchen. Wenn Sie *Kasse* auswählen, wird die Zahlung in einem angegebenen Gegenkonto erfasst.

    Sie können nun das Inforegister **Zeilen** für Produkte füllen, die Sie an den Debitoren oder für jede mögliche Transaktion mit dem Debitoren verkaufen, den Sie im Sachkonto buchen möchten.

4. Wählen Sie auf dem Inforegister **Zeilen** im Feld **Typ** aus, welche Art von Produkt, Gebühr oder Transaktion Sie für den Debitor mit der Verkaufszeile buchen möchten.
   * Wenn Sie wiederkehrende Verkaufszeilen für den Debitor wie einen Monatsersatzauftrag, eingerichtet haben, können Sie dies durch Auswählen der Schaltfläche **Wiederkehrende Verkaufszeilen holen** reflektieren.
5. Geben Sie im Feld **Nr.** Feld, einen Datensatz auswählen, um entsprechend dem Wert im Feld **Art** zu buchen.

    Sie lassen das **Nr.** Feld in folgenden Fällen leer:

    * Wenn die Zeile für einen Kommentar ist. Die Bemerkung im Feld **Beschreibung** enthalten ist.
    * Wenn die Zeile für einen Katalogartikel ist. Wählen Sie die Aktion **Katalogartikel auswählen**. Erfahren Sie mehr unter [Mit Katalogelementen arbeiten ](inventory-how-work-nonstock-items.md).

6. Geben Sie im Feld **Menge** ein, wie viele Einheiten des Produkts, der Kosten oder der Transaktion, in der Zeile des Debitors gespeichert werden soll.  

    > [!NOTE]  
    > Wenn Artikel vom Typ **Service** sind, oder das **Typ**-Feld **Ressource** enthält, ist die Menge eine Zeiteinheit wie Stunden, wie im Feld **Einheit des Messcodes** der Zeile angegeben. Weitere Informationen finden Sie unter [Einrichten von Einheiten](inventory-how-setup-units-of-measure.md)

    Der Wert im Feld **Zeilenbetrag** Feld wird als *VK-Preis* x *Menge* berechnet.  

    Der Preis und der Zeilenbetrag auf den Verkaufsrechnungszeilen werden mit oder ohne MwSt. angezeigt je nachdem, was Sie im Feld **Preis inklusive Mehrwertsteuer** auf der Debitorenkarte ausgewählt haben.  
7. Wenn Sie Skonto gewähren möchten, geben Sie einen Prozentsatz im Feld **Zeilenrabatt %** ein. Der Wert im Feld **Zeilenbetrag** wird entsprechend aktualisiert.  

    Wenn Sie bestimmte Artikelpreise für den Debitor auf dem Inforegister **Verkaufspreise und Verkaufspreis-Zeilenrabatte** eingerichtet haben, werden der Preis und der Betrag auf der Rechnungszeile automatisch aktualisiert, wenn die vereinbarten Preiskriterien erfüllt sind. Erfahren Sie mehr unter [Erfassen von Verkaufspreisen, Skonti und Zahlungsvereinbarungen](sales-how-record-sales-price-discount-payment-agreements.md).  
8. Wiederholen Sie die Schritte 4 bis 7 für jedes Produkt oder jede Gebühr, die Sie an den Debitoren verkaufen möchten.

    Die Summenfelder unter den Positionen werden automatisch aktualisiert, wenn Sie Positionen erstellen oder ändern, um die Beträge anzuzeigen, die auf die Sachkonten gebucht werden.

    > [!NOTE]
    > In sehr seltenen Fällen können die gebuchten Beträge von den in den Summenfeldern angezeigten Beträgen abweichen. Dies ist in der Regel auf Rundungsrechnungen in Bezug auf Mehrwertsteuer oder Verkaufssteuer zurückzuführen.<br /><br />Um die tatsächlich gebuchten Beträge zu überprüfen, können Sie die **Statistiken**-Seite verwenden, die die Rundungsberechnungen berücksichtigt. Auch wenn Sie die Aktion **Freigabe** auswählen, werden die Summenfelder aktualisiert, sodass sie die Rundungsberechnungen enthalten.
9. Geben Sie im Feld **Rechnungsbetrag mit Rabatt ohne Mehrwertsteuer** einen Betrag ein, der vom Wert abgezogen werden soll, der im Feld **Total inklusive Mehrwertsteuer** im unteren Bereich der Rechnung angezeigt wird.

    Wenn Sie Rechnungsrabatte für den Debitor eingerichtet haben, wird der angegebene Prozentwert automatisch in das Feld **Rechnungsrabatt in Prozent** eingetragen, sobald die Rabattkriterien erfüllt sein, und der entsprechende Betrag wird im Feld **Rechnungsbetrag mit Rabatt ohne Mehrwertsteuer** eingefügt. Erfahren Sie mehr unter [Erfassen von Verkaufspreisen, Skonti und Zahlungsvereinbarungen](sales-how-record-sales-price-discount-payment-agreements.md).

10. Wenn die Verkaufsrechnungszeilen ausgeführt werden, wählen Sie die Aktion **Buchen und Senden** aus.  

Das Dialogfeld **Buchungs- und Sendebestätigung** zeigt die gewünschte Methode des Debitors das Empfangen von Belegen an. Sie können die Sendemethode ändern, indem Sie die Schaltfläche vom Feld **Beleg senden an** auswählen. Erfahren Sie mehr unte r[Belegsendeprofile einrichten](sales-how-setup-document-send-profiles.md)

Der zugehörige Artikel und die Debitorenposten werden nun im System erfasst erstellt, und die Verkaufsrechnung wird als PDF-Dokument ausgegeben. Die Verkaufsrechnung wird in der Liste der gebuchten Verkaufsrechnungen entfernt und durch einen neuen Beleg in der Liste der gebuchten Verkaufsrechnungen ersetzt.  

### Rechnungsrabatte bei Verkäufen berechnen

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## Gebuchte Rechnungen

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Sie können eine gebuchte Verkaufsrechnung einfach korrigieren oder stornieren, bevor sie bezahlt wird. Dies ist nützlich, wenn Sie einen Tippfehler korrigieren möchten, oder wenn der Debitor eine Änderung früh im Bestellvorgang anfordert. Weitere Informationen finden Sie unter [Ändern oder Löschen einer unbezahlten Verkaufsrechnung](sales-how-correct-cancel-sales-invoice.md). Wenn die gebuchte Verkaufsrechnung bezahlt ist, müssen Sie eine Verkaufsgutschrift erstellen, um den Verkauf zu stornieren. Weitere Informationen finden Sie unter [Verarbeiten einer Verkaufsrücklieferung oder von Stornierungen](sales-how-process-sales-returns-cancellations.md).  

[Die Liste **Gebuchte Verkaufsrechnungen** öffnen](https://businesscentral.dynamics.com/?page=143) in [!INCLUDE [prod_short](includes/prod_short.md)].

## Zahlungen registrieren

Abhängig von den Unternehmensanforderungen können Sie bezahlt werden und die Zahlung auf unterschiedliche Arten erfassen: automatisch und durch Zahlungsverkehr.  

Sie können Zahlungen direkt auf der Debitorenkarte verarbeiten. Verwenden Sie die Aktion **Debitorenzahlungen registrieren**, um eine Übersicht nicht geleisteten Rechnungen für diesen Debitor zu erhalten. Dann markieren Sie die Rechnung, als teilweise oder vollständig bezahlt. Verarbeitet die Zahlungen Ihrer Debitoren, indem die auf Ihrem Konto eingegangenen Beträge den entsprechenden unbezahlten Verkaufsrechnungen zugeordnet und anschließend die Zahlungen gebucht werden. Weitere Informationen finden Sie unter [Zahlungen individuell abstimmen](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-register-customer-payments-individually).  

Im Geschäftsumgebungen, in denen der Debitor einige Zeit nach der Lieferung bezahlt entsprechend der Zahlungsbedingungen, verbleibt eine offene (unbezahlte) Verkaufsrechnung bis die Debitorenabteilung überprüft, dass die Zahlung erfolgt ist und die Zahlung der gebuchten Verkaufsrechnung ausgeglichen ist. Der Text kann manuell oder automatisch eingefügt werden. Weitere Informationen finden Sie unter [Abstimmen von Debitoren-Zahlungen mit dem Zahlungseingangs Buch.-Blatt oder von Debitorenposten](receivables-how-apply-sales-transactions-manually.md) und [Zahlungen mit automatischem Ausgleich abstimmen](receivables-how-reconcile-payments-auto-application.md).  

In Geschäftsumgebungen, wo Debitoren sofort bezahlen, beispielswiese mit PayPal oder Bargeld, wenn eine Zahlung sofort erfasst wird, wenn Sie die Verkaufsrechnung buchen, das heißt die gebuchte Verkaufsrechnung. wird geschlossen als vollständig ausgeglichen. Wählen Sie im Inforegister Zahlungen im Feld **Zahlungsformcode** den entsprechenden Code aus. Für elektronischen Zahlungsverkehr wie PayPal müssen Sie das Feld **Zahlungsverkehr** ausfüllen. Erfahren Sie mehr unter [Aktivieren von Debitoren-Zahlungen durch Zahlungsverkehr](sales-how-enable-payment-service-extensions.md).

Sie können direkt gezahlte Rechnungen für nicht-registrierte Debitoren auch erstellen, indem Sie eine Bargelddebitoren-Karte für sie einrichten, auf der Sie auf die Verkaufsrechnung hinweisen. Erfahren Sie mehr unter [Bardebitoren einrichten](finance-how-to-set-up-cash-customers.md).  

> [!TIP]
> Wenn Sie Ihren Kunden Erinnerungen an überfällige Zahlungen senden möchten, müssen Sie Erinnerungsstufen und -bedingungen einrichten. Weitere Informationen finden Sie unter [Einrichten von Mahnmethoden, Bestimmungen und Mahntext](finance-setup-reminders.md)  

## Externe Belegnummern

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## Siehe auch

[Verkauf](sales-manage-sales.md)  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Kommissionierliste drucken](sales-how-print-picking-list.md)  
[Bestand](inventory-manage-inventory.md)  
[Dokumente per E-Mail versenden](ui-how-send-documents-email.md)  
[Einziehen von Restbeträgen](receivables-collect-outstanding-balances.md)  
[Massenrechnungsstellung von Microsoft Bookings in Business Central](finance-bookings.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
