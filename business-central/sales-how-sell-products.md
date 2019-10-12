---
title: Erstellen Sie einen Verkaufsauftrag und verkaufen Sie Produkte| Microsoft Docs
description: Beschreibt, wie Sie einen Verkaufsauftrag erstellen, einen Vertrag mit einem Debitoren erfassen, Produkte unter bestimmten Bedingungen verkaufen oder kaufen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 76fc6081cf1dd27cc1e8f6c3611e60cb0ef7d37f
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2312100"
---
# <a name="sell-products"></a>Produkte verkaufen
Sie erstellen eine Verkaufsrechnung oder eine Bestellung, um Ihre Vereinbarung mit dem Debitoren zu erfassen, um bestimmte Produkte unter speziellen Liefer- und Zahlungsbedingungen zu verkaufen.

> [!NOTE]  
>   Sie müssen Verkaufsaufträge verwenden, wenn der Verkaufsprozess dies erfordert, so dass Sie Teile einer Bestellmenge liefern können, weil beispielsweise die vollständige Menge nicht sofort verfügbar ist. Wenn Sie Artikel als Direktlieferung verkaufen, indem Sie direkt von Ihrem Kreditor an Ihren Debitor versenden, müssen Sie ebenfalls Verkaufsaufträge verwenden. Weitere Informationen finden Sie unter [Direktlieferungen erstellen](sales-how-drop-shipment.md) In allen anderen Aspekten ist das Vorgehen bei Verkaufsaufträgen gleich wie bei Verkaufsrechnungen. Weitere Informationen finden Sie unter [Fakturieren eines Verkaufs](sales-how-invoice-sales.md).

Sie können mit dem Debitor verhandeln, indem Sie zuerst ein Verkaufsangebot erstellen, das Sie in eine Verkaufsrechnung umwandeln können, wenn Sie dem Verkauf zustimmen. Weitere Informationen finden Sie unter [Verkaufsangebote machen](sales-how-make-offers.md).

Nachdem der Debitor die Vereinbarung bestätigt hat, beispielsweise nach dem Angebotsprozess, können Sie eine Auftragsbestätigung senden, um Ihre Verpflichtung zu erfassen, die Produkte wie vereinbart zu liefern.

Wenn Sie die Produkte teilweise oder gesamthaft liefern, buchen Sie die Verkaufsrechnung oder den Verkaufsauftrag als geliefert oder als geliefert und fakturiert, um den zugehörigen Artikel und die Debitorenposten im System zu erfassen. Wenn Sie den Verkaufsauftrag buchen, können Sie das Dokument auch als PDF-Dateianhang senden. Sie können den E-Mail-Text mit einer Zusammenfassung des Auftrags und der Zahlungsinformationen, wie ein Link zu Paypal automatisch ausfüllen lassen. Weitere Informationen finden Sie unter [Senden von Dkumenten über E-Mail](ui-how-send-documents-email.md).

Im Geschäftsumgebungen, in denen der Debitor einige Zeit nach der Lieferung bezahlt entsprechend der Zahlungsbedingung, verbleibt eine offene (unbezahlte) Verkaufsrechnung bis die Debitorenabteilung überprüft, dass die Zahlung erfolgt ist und die Zahlung der gebuchten Verkaufsrechnung ausgeglichen ist. Weitere Informationen finden Sie unter [Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-auto-application.md).

In Geschäftsumgebungen, wo Debitoren sofort bezahlen, beispielswiese mit Paypal oder Bargeld, wenn eine Zahlung sofort erfasst wird, wenn Sie die Verkaufsrechnung buchen, das heißt die gebuchte Verkaufsrechnung. wird geschlossen als vollständig ausgeglichen. Wählen Sie im Inforegister Zahlungen im Feld **Zahlungsformcode** den entsprechenden Code aus. Siehe dazu auch Schritt 8 unten. Für elektronischen Zahlungsverkehr wie Paypal müssen Sie das Feld **Zahlungsverkehr** ausfüllen. Weitere Informationen finden Sie unter [Aktivieren Sie Zahlungen durch Zahlungsverkehr](sales-how-enable-payment-service-extensions.md)

Sie können direkt gezahlte Rechnungen für nicht-registrierte Debitoren auch erstellen, indem Sie eine Bargelddebitoren-Karte einrichten, auf der Sie auf die Verkaufsrechnung hinweisen. Weitere Informationen finden Sie unter [Einrichten von BargeldDebitoren](finance-how-to-set-up-cash-customers.md).

Sie können eine gebuchte Verkaufsrechnung aus einen Verkaufsauftrag einfach korrigieren oder stornieren, bevor sie bezahlt wird. Dies ist nützlich, wenn Sie einen Tippfehler korrigieren möchten, oder wenn der Debitor eine Änderung früh im Bestellvorgang anfordert. Weitere Informationen finden Sie unter [Ändern oder löschen von unbezahlten Verkaufsrechnungen](sales-how-correct-cancel-sales-invoice.md). Wenn die gebuchte Verkaufsrechnung bezahlt ist, müssen Sie eine Verkaufsgutschrift erstellen, um den Verkauf zu stornieren. Weitere Informationen finden Sie unter [Retouren verarbeiten oder Stornieren](sales-how-process-sales-returns-cancellations.md).

Gibt an, ob die Artikelkarte einen **Bestand**, **Service** und **Nicht-Bestand** ist, wenn die Einheit eine physische Einheit ist, die nicht im Lagerbestand verfolgt wird. Weitere Informationen finden Sie unter [Neue Artikel registrieren](inventory-how-register-new-items.md). Der Verkaufsangebotsprozess ist derselbe für alle dre Artikeltypen.

Sie können die Debitorenfelder des Verkaufsangebotes auf zwei Arten ausfüllen, abhängig davon, ob der Debitor bereits registriert ist oder nicht. Siehe Schritt 2 und 3 im folgenden Verfahren.

## <a name="to-create-a-sales-order"></a>So erstellen Sie einen Verkaufsauftrag
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Aufträge** ein, und wählen dann den zugehörigen Link aus.
2. Geben Sie im Feld **Debitor** den Namen eines vorhandenen Debitors ein.

    Andere Felder auf der Seite **Verkaufsangebot** werden nun mit den Standardinformationen vom ausgewählten Debitor ausgefüllt. Wenn der Debitor noch nicht erfasst wurde, dann führen Sie die folgenden Schritte durch:
3. Geben Sie im Feld **Debitor** den Namen eines neuen Debitors ein.
4. Klicken Sie im Dialogfeld auf die Schaltfläche **Ja**, um die Übertragung zu bestätigen.
5. Auf der Seite **Eine Vorlage für einen neuen Debitor auswählen** wählen Sie eine Vorlage, auf der die neue Debitorenkarte basieren soll, und dann wählen Sie die Schaltfläche **OK**.

    Eine neue Debitorenkarte wird geöffnet, vorausgefüllt mit Informationen auf der ausgewählten Debitorenvorlage. Das Feld **Name** wird mit dem neuen Namen des Debitors vorab ausgefüllt, den Sie im Verkaufsauftrag eingegeben haben.
6. Fahren Sie fort, die restlichen Felder auf der Debitorenkarte auszufüllen. Weitere Informationen finden Sie unter [Neue Debitoren registrieren](sales-how-register-new-customers.md).  
7. Wenn Sie die Debitorenkarte abgeschlossen haben, wählen Sie die Schaltfläche **OK**, um zur Seite **Verkaufsauftrag** zurückzugehen.

    Felder im Verkaufsangebot werden mit den Informationen, die Sie festgelegt haben, in der neuen Debitorenkarte ausgefüllt.
8. Füllen Sie auf der Seite **Verkaufsauftrag** die Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Wenn Sie dem Debitor ermöglichen, sofort mit Kreditkarte oder Paypal zu bezahlen, dann füllen Sie das Feld **Zahlungsformcode** aus. Die Zahlung wird dann erfasst, sobald Sie die Verkaufsrechnung buchen. Wenn Sie KASSE auswählen, wird die Zahlung in einem angegebenen Gegenkonto erfasst.

    Sie sind nun bereit, die Verkaufsangebotszeilen mit Lagerartikeln oder Services auszufüllen, die Sie an den Debitoren verkaufen möchten.

    Wenn Sie wiederkehrende Verkaufszeilen für den Debitor wie einen Monatsersatzauftrag, eingerichtet haben, können Sie diese Zeilen auf der Rechnung durch Auswählen der Schaltfläche **Wiederkehrende Verkaufszeilen holen** einfügen.
9. Geben Sie im Inforegister **Zeilen** im Feld **Artikel** die Nummer eines Lagerartikels oder Service ein.  
10. Geben Sie in dem Feld **Menge** die Anzahl des Artikels an, der verkauft werden soll.

    > [!NOTE]  
    >   Für Artikel des Typs Service ist die Menge eine Zeiteinheit wie Stunden, wie im Feld **Einheit des Messcodes** der Zeile angegeben.

    Das Feld **Zeilenmenge** wird aktualisiert, um den Wert im Feld **VK-Preis** multipliziert ist mit dem Wert im Feld **Menge** anzuzeigen.

    Der Preis und der Zeilenbetrag auf den Verkaufsrechnungszeilen werden mit oder ohne MwSt. angezeigt je nachdem, was Sie im Feld **Preis inklusive Mehrwertsteuer** auf der Debitorenkarte ausgewählt haben.
11. Geben Sie im Feld **Zeilenrabatt in Prozent** einen Prozentsatz ein, wenn Sie dem Debitor einen Rabatt auf das Produkt gewähren möchten. Der Wert im Feld **Zeilenbetrag** wird entsprechend aktualisiert.

    Wenn Sie bestimmte Artikelpreise für den Debitor auf dem Inforegister **Verkaufspreise und Verkaufspreis-Zeilenrabatte** eingerichtet haben, werden der Preis und der Betrag auf der Rechnungszeile automatisch aktualisiert, wenn die vereinbarten Preiskriterien erfüllt sind. Weitere Informationen finden Sie unter [Erfassen von Verkaufspreisen, Rabatt und Zahlungsvereinbarungen](sales-how-record-sales-price-discount-payment-agreements.md)
12. Um eine Bemerkung über die Angebotszeile hinzuzufügen, die der Debitor auf dem gedruckten Angebot anzeigen kann, schreiben Sie einen Text im Feld **Beschreibung**-in einer leeren Zeile.  
13. Wiederholen Sie die Schritte 9 bis 12 für jeden Artikel, den Sie an den Debitoren verkaufen möchten.

    Die Summen unter den Zeilen werden berechnet, während Sie Zeilen erstellen oder ändern.
14. Eine neue Debitorenkarte wird geöffnet, vorausgefüllt mit Informationen auf der ausgewählten Debitorenvorlage. Füllen Sie die restlichen Felder aus. Weitere Informationen finden Sie unter [Neue Debitoren registrieren](sales-how-register-new-customers.md).  
15. Wenn Sie die Debitorenkarte abgeschlossen haben, wählen Sie die Schaltfläche **OK**, um zur Seite **Verkaufsauftrag** zurückzugehen.

    Felder im Verkaufsangebot werden mit den Informationen, die Sie festgelegt haben, in der neuen Debitorenkarte ausgefüllt.
16. Füllen Sie auf der Seite **Verkaufsauftrag** die Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Sie können nun die Verkaufsauftragszeilen für Produkte füllen, die Sie an den Debitoren oder für jede mögliche Transaktion mit dem Debitoren verkaufen, den Sie im Sachkonto buchen möchten.   

    Wenn Sie wiederkehrende Verkaufszeilen für den Debitor wie einen Monatsersatzauftrag, eingerichtet haben, können Sie diese Zeilen auf der Rechnung durch Auswählen der Schaltfläche **Wiederkehrende Verkaufszeilen holen** einfügen.  
17. Wählen Sie im Inforegister **Zeilen** im Feld **Art** aus, welche Art des Produkts, der Kosten oder der Transaktion Sie für den Debitor mit der Verkaufszeile buchen werden.

18. Geben Sie im Feld **Nr.** Feld, einen Datensatz auswählen, um entsprechend dem Wert im Feld **Art** zu buchen.

    Sie lassen das **Nr.** Feld ist in folgenden Fällen leer:

    * Wenn die Zeile für einen Kommentar ist. Die Bemerkung im Feld **Beschreibung** enthalten ist.
    * Wenn die Zeile für einen Katalogartikel ist. Wählen Sie die Aktion **Katalogartikel auswählen**. Weitere Informationen finden Sie unter [Arbeiten mit Katalogelementen](inventory-how-work-nonstock-items.md).

19. Geben Sie im Feld **Menge** ein, wie viele Einheiten des Produkts, der Kosten oder der Transaktion, in der Zeile des Debitors gespeichert werden soll.  

    > [!NOTE]  
    > Wenn Artikel vom Typ **Service** sind, oder das **Typ**-Feld **Ressource** enthält, ist die Menge eine Zeiteinheit wie Stunden, wie im Feld **Einheit des Messcodes** der Zeile angegeben. Weitere Informationen finden Sie unter [Einrichten von Einheiten](inventory-how-setup-units-of-measure.md).

    Der Wert im Feld **Zeilenbetrag** Feld wird als *VK-Preis* x *Menge* berechnet.  

    Der Preis und der Zeilenbetrag auf den Verkaufsrechnungszeilen werden mit oder ohne MwSt. angezeigt je nachdem, was Sie im Feld **Preis inklusive Mehrwertsteuer** auf der Debitorenkarte ausgewählt haben.  
20. Wenn Sie Skonto gewähren möchten, geben Sie einen Prozentsatz im Feld **Zeilenrabatt %** ein. Der Wert im Feld **Zeilenbetrag** wird entsprechend aktualisiert.  

    Wenn Sie bestimmte Artikelpreise für den Debitor auf dem Inforegister **Verkaufspreise und Verkaufspreis-Zeilenrabatte** eingerichtet haben, werden der Preis und der Betrag auf der Rechnungszeile automatisch aktualisiert, wenn die vereinbarten Preiskriterien erfüllt sind. Weitere Informationen finden Sie unter [Erfassen von Verkaufspreisen, Rabatt und Zahlungsvereinbarungen](sales-how-record-sales-price-discount-payment-agreements.md)  
21. Wiederholen Sie die Schritte 9 bis 12 für jedes Produkt oder jede Gebühr, die Sie an den Debitoren verkaufen möchten.  

    Die Summenfelder unter den Positionen werden automatisch aktualisiert, wenn Sie Positionen erstellen oder ändern, um die Beträge anzuzeigen, die auf die Sachkonten gebucht werden.

    > [!NOTE]
    > In sehr seltenen Fällen können die gebuchten Beträge von den in den Summenfeldern angezeigten Beträgen abweichen. Dies ist in der Regel auf Rundungsrechnungen in Bezug auf Mehrwertsteuer oder Verkaufssteuer zurückzuführen.<br /><br />Um die tatsächlich gebuchten Beträge zu überprüfen, können Sie die **Statistiken**-Seite verwenden, die die Rundungsberechnungen berücksichtigt. Auch wenn Sie die Aktion **Freigabe** auswählen, werden die Summenfelder aktualisiert, sodass sie die Rundungsberechnungen enthalten.  
22. Geben Sie im Feld **Rabattbetrag in Rechnung stellen** einen Betrag ein, der vom Wert abgezogen werden soll, der im Feld **Total inklusive Mehrwertsteuer** im unteren Bereich der Rechnung angezeigt wird.

    Wenn Sie Rechnungsrabatte für den Debitor eingerichtet haben, wird der angegebene Prozentwert automatisch in das Feld **Rechnungsrabatt in Prozent** eingetragen, sobald die Kriterien erfüllt sein, und der entsprechende Betrag wird im Feld **Rechnungsbetrag mit Rabatt ohne Mehrwertsteuer** eingefügt. Weitere Informationen finden Sie unter [Erfassen von Verkaufspreisen, Rabatt und Zahlungsvereinbarungen](sales-how-record-sales-price-discount-payment-agreements.md)
23. Um nur einen Teil der Auftragsmenge zu liefern, geben Sie die Menge im Feld **Menge für Versand** ein. Der Wert wird in das Feld **Zu fakturierende Menge** kopiert.
24. Um nur einen Teil der Auftragsmenge zu fakturieren, geben Sie die Menge im Feld **Menge für Fakturierung** ein. Die zu fakturierende Menge kann nicht größer sein, als der Wert im Feld **Menge geliefert**.   
25. Wenn die Verkaufsangebotszeilen ausgeführt werden, wählen Sie die Aktion **Buchen und Senden** aus.

Das Dialogfeld **Buchungs- und Sendebestätigung** zeigt die gewünschte Methode des Debitors das Empfangen von Belegen an. Sie können die Sendemethode ändern, indem Sie die Schaltfläche vom Feld **Beleg senden an** auswählen. Weitere Informationen finden Sie unter [Einrichten von Sendeprofilen](sales-how-setup-document-send-profiles.md).

Der zugehörige Artikel und die Debitorenposten werden nun im System erfasst erstellt, und das Verkaufsangebot wird als PDF-Dokument ausgegeben. Wenn der Auftrag vollständig gebucht wird, wird er aus der Liste von Verkaufsaufträgen entfernt und durch neue Belege in der Übersicht der gebuchten Verkaufsrechnungen und in der Liste gebuchter Auftragslieferungen ersetzt.

## <a name="see-also"></a>Siehe auch
[Verkauf](sales-manage-sales.md)  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Senden von Belegen über E-Mail](ui-how-send-documents-email.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
