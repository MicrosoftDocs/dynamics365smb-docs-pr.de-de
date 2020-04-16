---
title: Verkaufsangebote erstellen| Microsoft Docs
description: Beschreibt, wie Sie einen Verkaufsauftrag erstellen, einen Vertrag mit einem Debitoren erfassen, Produkte unter bestimmten Bedingungen verkaufen oder kaufen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bill, sale, invoice, order
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 9e485f2051cb045db6f106377521973a45546ad7
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3193659"
---
# <a name="invoice-sales"></a>Fakturieren eines Verkaufs
Sie erstellen eine Verkaufsrechnung oder eine Bestellung, um Ihre Vereinbarung mit dem Debitoren zu erfassen, um bestimmte Produkte unter speziellen Liefer- und Zahlungsbedingungen zu verkaufen.  

Es gibt mehrere Szenarien, in dem Sie einen Verkaufsauftrag anstelle einer Verkaufsrechnung verwenden müssen:  

* Wenn Sie nur einen Teil einer Bestellmenge liefern müssen, da z. B. die gesamte Menge nicht verfügbar ist.  
* Wenn Sie Artikel verkaufen, die Ihr Kreditor direkt an den Debitor liefert, d. h. bei einer sogenannten Direktlieferung. Weitere Informationen finden Sie unter [Direktlieferungen erstellen](sales-how-drop-shipment.md)  

In allen anderen Aspekten ist das Vorgehen bei Verkaufsaufträgen gleich wie bei Verkaufsrechnungen. Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)

Sie können mit dem Debitor verhandeln, indem Sie zuerst ein Verkaufsangebot erstellen, das Sie in eine Verkaufsrechnung umwandeln können, wenn Sie dem Verkauf zustimmen. Weitere Informationen finden Sie unter [Verkaufsangebote machen](sales-how-make-offers.md).

Wenn der Debitor entscheidet zu kaufen, senden Sie die Verkaufsrechnung, um die entsprechende Menge und die Wertposten zu erstellen. Wenn Sie die Verkaufsrechnung buchen, können Sie das Dokument als PDF-Dateianhang auch senden. Sie können den E-Mail-Text haben, der mit einer Zusammenfassung der Rechnung und der Zahlungsinformationen, wie ein Link zu Paypal, vorab ausgefüllt wurde. Weitere Informationen finden Sie unter [Senden von Dkumenten über E-Mail](ui-how-send-documents-email.md). Wenn der Debitor die Rechnung gezahlt hat, können Sie die Zahlung auf verschiedene Arten ausführen, abhängig von der Größe und dem gewünschten Workflow der Organisation. Weitere Informationen finden Sie im Abschnitt [Zahlungen erfassen](#registering-payments).  


Sie können eine gebuchte Verkaufsrechnung einfach korrigieren oder stornieren, bevor sie bezahlt wird. Dies ist nützlich, wenn Sie einen Tippfehler korrigieren möchten, oder wenn der Debitor eine Änderung früh im Bestellvorgang anfordert. Weitere Informationen finden Sie unter [Ändern oder löschen von unbezahlten Verkaufsrechnungen](sales-how-correct-cancel-sales-invoice.md). Wenn die gebuchte Verkaufsrechnung bezahlt ist, müssen Sie eine Verkaufsgutschrift erstellen, um den Verkauf zu stornieren. Weitere Informationen finden Sie unter [Retouren verarbeiten oder Stornieren](sales-how-process-sales-returns-cancellations.md).

Gibt an, ob die Artikelkarte einen **Bestand**, **Service** und **Nicht-Bestand** ist, wenn die Einheit eine physische Einheit ist, die nicht im Lagerbestand verfolgt wird. Weitere Informationen finden Sie unter [Neue Artikel registrieren](inventory-how-register-new-items.md). Der Verkaufsrechnungsprozess ist derselbe für alle drei Artikeltypen.

Sie können die oberen Infoboxen des Verkaufsangebotes auf zwei Arten ausfüllen, abhängig davon, ob der Debitor bereits registriert ist. Siehe Schritt 2 und 3 im folgenden Verfahren.

## <a name="to-create-a-sales-invoice"></a>So erstellen Sie eine Verkaufsrechnung
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Verkaufsrechnungen** ein und wählen Sie dann den entsprechenden Link.  
2. Geben Sie im Feld **Debitor** den Namen eines vorhandenen Debitors ein.

   Andere Felder auf der Seite **Verkaufsrechnung** werden nun mit den Standardinformationen vom ausgewählten Debitor ausgefüllt. Wenn der Debitor noch nicht erfasst wurde, dann führen Sie die folgenden Schritte durch:
3. Geben Sie im Feld **Debitor** den Namen eines neuen Debitors ein.
4. Klicken Sie im Dialogfeld auf die Schaltfläche **Ja**, um die Übertragung zu bestätigen.
5. Auf der Seite **Eine Vorlage für einen neuen Debitor auswählen** wählen Sie eine Vorlage, auf der die neue Debitorenkarte basieren soll, und dann wählen Sie die Schaltfläche **OK**.
6. Eine neue Debitorenkarte wird geöffnet, vorausgefüllt mit Informationen auf der ausgewählten Debitorenvorlage. Füllen Sie die restlichen Felder aus. Weitere Informationen finden Sie unter [Neue Debitoren registrieren](sales-how-register-new-customers.md).  
7. Wenn Sie die Debitorenkarte abgeschlossen haben, wählen Sie die Schaltfläche **OK**, um zur Seite **Verkaufsrechnung** zurückzugehen.

   Felder im Verkaufsrechnungskopf werden mit den Informationen, die Sie festgelegt haben, in der neuen Debitorenkarte ausgefüllt.  
8. Füllen Sie auf der Seite **Verkaufsrechnung** die Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Wenn Sie dem Debitor ermöglichen, sofort in bar oder durch Paypal zu bezahlen, dann füllen Sie das Feld **Zahlungsformcode** aus. Die Zahlung wird dann erfasst, sobald Sie die Verkaufsrechnung buchen. Wenn Sie KASSE auswählen, wird die Zahlung in einem angegebenen Gegenkonto erfasst.

    Sie können nun die Verkaufsrechnungszeilen für Produkte füllen, die Sie an den Debitoren oder für jede mögliche Transaktion mit dem Debitoren verkaufen, den Sie im Sachkonto buchen möchten.   

    Wenn Sie wiederkehrende Verkaufszeilen für den Debitor wie einen Monatsersatzauftrag, eingerichtet haben, können Sie diese Zeilen auf der Rechnung durch Auswählen der Schaltfläche **Wiederkehrende Verkaufszeilen holen** einfügen.  
9. Wählen Sie im Inforegister **Zeilen** im Feld **Art** aus, welche Art des Produkts, der Kosten oder der Transaktion Sie für den Debitor mit der Verkaufszeile buchen werden.
10. Geben Sie im Feld **Nr.** Feld, einen Datensatz auswählen, um entsprechend dem Wert im Feld **Art** zu buchen.

    Sie lassen das **Nr.** Feld ist in folgenden Fällen leer:

    * Wenn die Zeile für einen Kommentar ist. Die Bemerkung im Feld **Beschreibung** enthalten ist.
    * Wenn die Zeile für einen Katalogartikel ist. Wählen Sie die Aktion **Katalogartikel auswählen**. Weitere Informationen finden Sie unter [Arbeiten mit Katalogelementen](inventory-how-work-nonstock-items.md).

11. Geben Sie im Feld **Menge** ein, wie viele Einheiten des Produkts, der Kosten oder der Transaktion, in der Zeile des Debitors gespeichert werden soll.  

    > [!NOTE]  
    > Wenn Artikel vom Typ **Service** sind, oder das **Typ**-Feld **Ressource** enthält, ist die Menge eine Zeiteinheit wie Stunden, wie im Feld **Einheit des Messcodes** der Zeile angegeben. Weitere Informationen finden Sie unter [Einrichten von Einheiten](inventory-how-setup-units-of-measure.md)

    Der Wert im Feld **Zeilenbetrag** Feld wird als *VK-Preis* x *Menge* berechnet.  

    Der Preis und der Zeilenbetrag auf den Verkaufsrechnungszeilen werden mit oder ohne MwSt. angezeigt je nachdem, was Sie im Feld **Preis inklusive Mehrwertsteuer** auf der Debitorenkarte ausgewählt haben.  
12. Wenn Sie Skonto gewähren möchten, geben Sie einen Prozentsatz im Feld **Zeilenrabatt %** ein. Der Wert im Feld **Zeilenbetrag** wird entsprechend aktualisiert.  

    Wenn Sie bestimmte Artikelpreise für den Debitor auf dem Inforegister **Verkaufspreise und Verkaufspreis-Zeilenrabatte** eingerichtet haben, werden der Preis und der Betrag auf der Rechnungszeile automatisch aktualisiert, wenn die vereinbarten Preiskriterien erfüllt sind. Weitere Informationen finden Sie unter [Erfassen von Verkaufspreisen, Rabatt und Zahlungsvereinbarungen](sales-how-record-sales-price-discount-payment-agreements.md)  
13. Wiederholen Sie die Schritte 9 bis 12 für jedes Produkt oder jede Gebühr, die Sie an den Debitoren verkaufen möchten.  

    Die Summenfelder unter den Positionen werden automatisch aktualisiert, wenn Sie Positionen erstellen oder ändern, um die Beträge anzuzeigen, die auf die Sachkonten gebucht werden.

    > [!NOTE]
    > In sehr seltenen Fällen können die gebuchten Beträge von den in den Summenfeldern angezeigten Beträgen abweichen. Dies ist in der Regel auf Rundungsrechnungen in Bezug auf Mehrwertsteuer oder Verkaufssteuer zurückzuführen.<br /><br />Um die tatsächlich gebuchten Beträge zu überprüfen, können Sie die **Statistiken**-Seite verwenden, die die Rundungsberechnungen berücksichtigt. Auch wenn Sie die Aktion **Freigabe** auswählen, werden die Summenfelder aktualisiert, sodass sie die Rundungsberechnungen enthalten.
14. Geben Sie im Feld **Rabattbetrag in Rechnung stellen** einen Betrag ein, der vom Wert abgezogen werden soll, der im Feld **Total inklusive Mehrwertsteuer** im unteren Bereich der Rechnung angezeigt wird.

    Wenn Sie Rechnungsrabatte für den Debitor eingerichtet haben, wird der angegebene Prozentwert automatisch in das Feld **Rechnungsrabatt in Prozent** eingetragen, sobald die Kriterien erfüllt sein, und der entsprechende Betrag wird im Feld **Rechnungsbetrag mit Rabatt ohne Mehrwertsteuer** eingefügt. Weitere Informationen finden Sie unter [Erfassen von Verkaufspreisen, Rabatt und Zahlungsvereinbarungen](sales-how-record-sales-price-discount-payment-agreements.md)  
15. Wenn die Verkaufsrechnungszeilen ausgeführt werden, wählen Sie die Aktion **Buchen und Senden** aus.  

Das Dialogfeld **Buchungs- und Sendebestätigung** zeigt die gewünschte Methode des Debitors das Empfangen von Belegen an. Sie können die Sendemethode ändern, indem Sie die Schaltfläche vom Feld **Beleg senden an** auswählen. Weitere Informationen finden Sie unter [Einrichten von Sendeprofilen](sales-how-setup-document-send-profiles.md).

Der zugehörige Artikel und die Debitorenposten werden nun im System erfasst erstellt, und die Verkaufsrechnung wird als PDF-Dokument ausgegeben. Die Verkaufsrechnung wird in der Liste der gebuchten Verkaufsrechnungen entfernt und durch einen neuen Beleg in der Liste der gebuchten Verkaufsrechnungen ersetzt.  

## <a name="registering-payments"></a>Zahlungen registrieren

Abhängig von den Unternehmensanforderungen können Sie bezahlt werden und die Zahlung auf unterschiedliche Arten erfassen: automatisch und durch Zahlungsverkehr.  

Sie können Zahlungen direkt auf der Debitorenkarte verarbeiten. Verwenden Sie die Aktion **Debitorenzahlungen registrieren**, um eine Übersicht nicht geleisteten Rechnungen für diesen Debitor zu erhalten. Dann markieren Sie die Rechnung, als teilweise oder vollständig bezahlt. Verarbeitet die Zahlungen Ihrer Debitoren, indem die auf Ihrem Konto eingegangenen Beträge den entsprechenden unbezahlten Verkaufsrechnungen zugeordnet und anschließend die Zahlungen gebucht werden. Weitere Informationen finden Sie unter [Zahlungen individuell abstimmen](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-register-customer-payments-individually).  

Im Geschäftsumgebungen, in denen der Debitor einige Zeit nach der Lieferung bezahlt entsprechend der Zahlungsbedingung, verbleibt eine offene (unbezahlte) Verkaufsrechnung bis die Debitorenabteilung überprüft, dass die Zahlung erfolgt ist und die Zahlung der gebuchten Verkaufsrechnung ausgeglichen ist. Der Text kann manuell oder automatisch eingefügt werden. Weitere Informationen finden Sie unter [Abstimmen von Debitoren-Zahlungen mit dem Zahlungseingangs Buch.-Blatt oder von Debitorenposten](receivables-how-apply-sales-transactions-manually.md) und [Zahlungen mit automatischem Ausgleich abstimmen](receivables-how-reconcile-payments-auto-application.md).  

In Geschäftsumgebungen, wo Debitoren sofort bezahlen, beispielswiese mit Paypal oder Bargeld, wenn eine Zahlung sofort erfasst wird, wenn Sie die Verkaufsrechnung buchen, das heißt die gebuchte Verkaufsrechnung. wird geschlossen als vollständig ausgeglichen. Wählen Sie im Inforegister Zahlungen im Feld **Zahlungsformcode** den entsprechenden Code aus. Siehe dazu auch Schritt 8 unten. Für elektronischen Zahlungsverkehr wie Paypal müssen Sie das Feld **Zahlungsverkehr** ausfüllen. Weitere Informationen finden Sie unter [Aktivieren Sie Zahlungen durch Zahlungsverkehr](sales-how-enable-payment-service-extensions.md)  

Sie können direkt gezahlte Rechnungen für nicht-registrierte Debitoren auch erstellen, indem Sie eine Bargelddebitoren-Karte einrichten, auf der Sie auf die Verkaufsrechnung hinweisen. Weitere Informationen finden Sie unter [Einrichten von BargeldDebitoren](finance-how-to-set-up-cash-customers.md).  

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/invoicing-customers-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch
[Verkauf](sales-manage-sales.md)  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Senden von Belegen über E-Mail](ui-how-send-documents-email.md)  
[Massenrechnungsstellung von Microsoft Bookings in Business Central](finance-bookings.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
