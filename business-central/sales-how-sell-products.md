---
title: Erstellen Sie einen Verkaufsauftrag und verkaufen Sie Produkte| Microsoft Docs
description: Beschreibt, wie Sie einen Verkaufsauftrag erstellen, einen Vertrag mit einem Kunden erfassen, Produkte unter bestimmten Bedingungen verkaufen oder kaufen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade
ms.date: 01/12/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 3a5dc2085e5d7b7bfad591e0f70f7f6e8f9cc43f
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="sell-products"></a>Produkte verkaufen
Sie erstellen eine Verkaufsrechnung oder eine Bestellung, um Ihre Vereinbarung mit dem Kunden zu erfassen, um bestimmte Produkte unter speziellen Liefer- und Zahlungsbedingungen zu verkaufen.

> [!NOTE]  
>   Sie müssen Verkaufsaufträge verwenden, wenn der Verkaufsprozess dies erfordert, so dass Sie Teile einer Bestellmenge liefern können, weil beispielsweise die vollständige Menge nicht sofort verfügbar ist. Wenn Sie Artikel als Direktlieferung verkaufen, indem Sie direkt von Ihrem Kreditor an Ihren Debitor versenden, müssen Sie ebenfalls Verkaufsaufträge verwenden. Weitere Informationen finden Sie unter [Direktlieferungen erstellen](sales-how-drop-shipment.md) In allen anderen Aspekten ist das Vorgehen bei Verkaufsaufträgen gleich wie bei Verkaufsrechnungen. Weitere Informationen finden Sie unter [Verkaufsrechnungen](sales-how-invoice-sales.md).

Sie können mit dem Debitor verhandeln, indem Sie zuerst ein Verkaufsangebot erstellen, das Sie in eine Verkaufsrechnung umwandeln können, wenn Sie dem Verkauf zustimmen. Weitere Informationen finden Sie unter  [Angebot erstellen](sales-how-make-offers.md).

Nachdem der Debitor die Vereinbarung bestätigt hat, beispielsweise nach dem Angebotsprozess, können Sie eine Auftragsbestätigung senden, um Ihre Verpflichtung zu erfassen, die Produkte wie vereinbart zu liefern.

Wenn Sie die Produkte teilweise oder gesamthaft liefern, buchen Sie die Verkaufsrechnung oder den Verkaufsauftrag als geliefert oder als geliefert und fakturiert, um den zugehörigen Artikel und die Debitorenposten im System zu erfassen. Wenn Sie den Verkaufsauftrag buchen, können Sie das Dokument auch als PDF-Dateianhang senden. Sie können den E-Mail-Text mit einer Zusammenfassung des Auftrags und der Zahlungsinformationen, wie ein Link zu Paypal automatisch ausfüllen lassen. Weitere Informationen finden Sie unter [Senden von Dkumenten über E-Mail](ui-how-send-documents-email.md).

Im betrieblichen Umfeld, in dem der Debitor bezahlen muss, bevor Produkte, wie in der Einzelhandelsbranche, geliefert werden, müssen Sie den Zahlungseingang für die Produkte abwarten, bevor Sie die Produkte liefern. In den meisten Fällen verarbeiten Sie eingehende Zahlungen einige Wochen nach Lieferung, indem Sie die Zahlungen in ihre entsprechenden gebuchten, unbezahlten Verkaufsrechnungen übernehmen. Weitere Informationen finden Sie unter [Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-auto-application.md).

Sie können eine gebuchte Verkaufsrechnung aus einen Verkaufsauftrag einfach korrigieren oder stornieren, bevor sie bezahlt wird. Dies ist nützlich, wenn Sie einen Tippfehler korrigieren möchten, oder wenn der Debitor eine Änderung früh im Bestellvorgang anfordert. Weitere Informationen finden Sie unter [Ändern oder löschen von unbezahlten Verkaufsrechnungen](sales-how-correct-cancel-sales-invoice.md). Wenn die gebuchte Verkaufsrechnung bezahlt ist, müssen Sie eine Verkaufsgutschrift erstellen, um den Verkauf zu stornieren. Weitere Informationen finden Sie unter [Retouren verarbeiten oder Stornieren](sales-how-process-sales-returns-cancellations.md).

Artikel können Artikel und Dienstleistungen sein, gekennzeichnet als **Artikel - Lager** und **Artikel - Service** auf den Verkaufszeilen. Der Verkaufsangebotsprozess ist derselbe für beide Artikeltypen. Weitere Informationen finden Sie unter [Neue Artikel registrieren](inventory-how-register-new-items.md).

Sie können die Debitorenfelder des Verkaufsangebotes auf zwei Arten ausfüllen, abhängig davon, ob der Debitor bereits registriert ist oder nicht. Siehe Schritt 2 und 3 im folgenden Verfahren.

## <a name="to-create-a-sales-order"></a>So erstellen Sie einen Verkaufsauftrag
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Verkaufsauftrag** ein, und wählen Sie dann den zugehörigen Link aus.
2. Geben Sie im Feld **Debitor** den Namen eines vorhandenen Debitors ein.

    Andere Felder im Fenster **Verkaufsangebot** werden nun mit den Standardinformationen vom ausgewählten Debitor ausgefüllt. Wenn der Debitor noch nicht erfasst wurde, dann führen Sie die folgenden Schritte durch:
3. Geben Sie im Feld **Debitor** den Namen eines neuen Debitors ein.
4. Klicken Sie im Dialogfeld auf die Schaltfläche **Ja**, um die Übertragung zu bestätigen.
5. Im Fenster **Vorlage für neuen Debitor wählen** wählen Sie eine Vorlage, auf der die neue Debitorenkarte basieren soll, und dann wählen Sie die Schaltfläche **OK**.

    Eine neue Debitorenkarte wird geöffnet, vorausgefüllt mit Informationen auf der ausgewählten Debitorenvorlage. Das Feld **Name** wird mit dem neuen Namen des Debitors vorab ausgefüllt, den Sie im Verkaufsauftrag eingegeben haben.
6. Fahren Sie fort, die restlichen Felder auf der Debitorenkarte auszufüllen. Weitere Informationen finden Sie unter [Neue Kunden registrieren](sales-how-register-new-customers.md).  
7. Wenn Sie die Debitorenkarte abgeschlossen haben, wählen Sie die Schaltfläche **OK**, um zum Fenster **Verkaufsangebot** zurückzugehen.

    Felder im Verkaufsangebot werden mit den Informationen, die Sie festgelegt haben, in der neuen Debitorenkarte ausgefüllt.
8. Füllen Sie im Fenster **Verkaufsangebot** die Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Sie sind nun bereit, die Verkaufsangebotszeilen mit Lagerartikeln oder Services auszufüllen, die Sie an den Kunden verkaufen möchten.

    Wenn Sie wiederkehrende Verkaufszeilen für den Debitor wie einen Monatsersatzauftrag, eingerichtet haben, können Sie diese Zeilen auf der Rechnung durch Auswählen der Schaltfläche **Wiederkehrende Verkaufszeilen holen** einfügen.
9. Geben Sie im Inforegister **Zeilen** im Feld **Artikel** die Nummer eines Lagerartikels oder Service ein.  
10. Geben Sie in dem Feld **Menge** die Anzahl des Artikels an, der verkauft werden soll.

    > [!NOTE]  
    >   Für Artikel des Typs Service ist die Menge eine Zeiteinheit wie Stunden, wie im Feld **Einheit des Messcodes** der Zeile angegeben.

    Das Feld **Zeilenmenge** wird aktualisiert, um den Wert im Feld **Einheitspreis** multipliziert ist mit dem Wert im Feld **Menge** anzuzeigen.

    Der Preis und der Zeilenbetrag auf den Verkaufsrechnungszeilen werden mit oder ohne MwSt. angezeigt je nachdem, was Sie im Feld **Preis inklusive Mehrwertsteuer** auf der Debitorenkarte ausgewählt haben.
11. Geben Sie im Feld **Zeilenrabatt in Prozent** einen Prozentsatz ein, wenn Sie dem Debitor einen Rabatt auf das Produkt gewähren möchten. Der Wert im Feld **Zeilenbetrag** wird entsprechend aktualisiert.

    Wenn Sie bestimmte Artikelpreise für den Debitor auf dem Inforegister **Verkaufspreise und Verkaufspreis-Zeilenrabatte** eingerichtet haben, werden der Preis und der Betrag auf der Rechnungszeile automatisch aktualisiert, wenn die vereinbarten Preiskriterien erfüllt sind. Weitere Informationen finden Sie unter [Erfassen von Verkaufspreisen, Skonti und Zahlungsvereinbarungen](sales-how-record-sales-price-discount-payment-agreements.md)
12. Um eine Bemerkung über die Angebotszeile hinzuzufügen, die der Debitor auf dem gedruckten Angebot anzeigen kann, schreiben Sie einen Text im Feld **Beschreibung**-in einer leeren Zeile.  
13. Wiederholen Sie die Schritte 9 bis 12 für jeden Artikel, den Sie an den Kunden verkaufen möchten.

    Die Summen unter den Zeilen werden berechnet, während Sie Zeilen erstellen oder ändern.
14. Eine neue Debitorenkarte wird geöffnet, vorausgefüllt mit Informationen auf der ausgewählten Debitorenvorlage. Füllen Sie die restlichen Felder aus. Weitere Informationen finden Sie unter [Neue Kunden registrieren](sales-how-register-new-customers.md).  
15. Wenn Sie die Debitorenkarte abgeschlossen haben, wählen Sie die Schaltfläche **OK**, um zum Fenster **Verkaufsangebot** zurückzugehen.

   Felder im Verkaufsauftrag werden mit den Informationen, die Sie festgelegt haben, in der neuen Debitorenkarte ausgefüllt.  
16. Füllen Sie im Fenster **Verkaufsangebot** die Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

   Sie können nun die Verkaufsauftragszeilen für Produkte füllen, die Sie an den Kunden oder für jede mögliche Transaktion mit dem Kunden verkaufen, den Sie im Sachkonto buchen möchten.   

   Wenn Sie wiederkehrende Verkaufszeilen für den Debitor wie einen Monatsersatzauftrag, eingerichtet haben, können Sie diese Zeilen auf der Rechnung durch Auswählen der Schaltfläche **Wiederkehrende Verkaufszeilen holen** einfügen.  
17. Wählen Sie im Inforegister **Zeilen** im Feld **Art** aus, welche Art des Produkts, der Kosten oder der Transaktion Sie für den Debitor mit der Verkaufszeile buchen werden.
18. Geben Sie im Feld **Nr.** Feld, einen Datensatz auswählen, um entsprechend dem Wert im Feld **Art** zu buchen.

    Sie lassen das **Nr.** Feld leer in folgenden Fällen: - Wenn die Zeile für eine Bemerkung ist. Die Bemerkung im Feld **Beschreibung** enthalten ist.
    - Wenn die Zeile für einen Katalogartikel ist. Wählen Sie die Aktion **Nicht-Katalogartikel auswählen**. Weitere Informationen finden Sie unter [Arbeiten mit nicht im Bestand vorhandenen Artikeln](inventory-how-work-nonstock-items.md).

19. Geben Sie im Feld **Menge** ein, wie viele Einheiten des Produkts, der Kosten oder der Transaktion, in der Zeile des Debitors gespeichert werden soll.  

    > [!NOTE]  
    >   Für Artikel des Typs **Artikel - Service** oder **Ressource** ist die Menge eine Zeiteinheit wie Stunden, wie im Feld **Einheit des Messcodes** der Zeile angegeben. Weitere Informationen finden Sie unter [Einrichten von Einheiten](inventory-how-setup-units-of-measure.md).

    Der Wert im Feld **Zeilenbetrag** Feld wird als *VK-Preis* x *Menge* berechnet.  

    Der Preis und der Zeilenbetrag auf den Verkaufsrechnungszeilen werden mit oder ohne MwSt. angezeigt je nachdem, was Sie im Feld **Preis inklusive Mehrwertsteuer** auf der Debitorenkarte ausgewählt haben.  
20. Wenn Sie Skonto gewähren möchten, geben Sie einen Prozentsatz im Feld **Zeilenrabatt %** ein. Der Wert im Feld **Zeilenbetrag** wird entsprechend aktualisiert.  

    Wenn Sie bestimmte Artikelpreise für den Debitor auf dem Inforegister **Verkaufspreise und Verkaufspreis-Zeilenrabatte** eingerichtet haben, werden der Preis und der Betrag auf der Rechnungszeile automatisch aktualisiert, wenn die vereinbarten Preiskriterien erfüllt sind. Weitere Informationen finden Sie unter [Erfassen von Verkaufspreisen, Skonti und Zahlungsvereinbarungen](sales-how-record-sales-price-discount-payment-agreements.md)  
21. Wiederholen Sie die Schritte 9 bis 12 für jedes Produkt oder jede Gebühr, die Sie an den Kunden verkaufen möchten.  

    Die Summen unter den Zeilen werden berechnet, während Sie Zeilen erstellen oder ändern.  
22. Geben Sie im Feld **Rabattbetrag in Rechnung stellen** einen Betrag ein, der vom Wert abgezogen werden soll, der im Feld **Total inklusive Mehrwertsteuer** im unteren Bereich der Rechnung angezeigt wird.

    Wenn Sie Rechnungsrabatte für den Debitor eingerichtet haben, wird der angegebene Prozentwert automatisch in das Feld **Rechnungsrabatt in Prozent** eingetragen, sobald die Kriterien erfüllt sein, und der entsprechende Betrag wird im Feld **Rechnungsbetrag mit Rabatt ohne Mehrwertsteuer** eingefügt. Weitere Informationen finden Sie unter [Erfassen von Verkaufspreisen, Skonti und Zahlungsvereinbarungen](sales-how-record-sales-price-discount-payment-agreements.md)
23. Um nur einen Teil der Auftragsmenge zu liefern, geben Sie die Menge im Feld **Menge für Versand** ein. Der Wert wird in das Feld **Zu fakturierende Menge** kopiert.
24. Um nur einen Teil der Auftragsmenge zu fakturieren, geben Sie die Menge im Feld **Menge für Fakturierung** ein. Die zu fakturierende Menge kann nicht größer sein, als der Wert im Feld **Menge geliefert**.   
25. Wenn die Verkaufsangebotszeilen ausgeführt werden, wählen Sie die Aktion **Buchen und Senden** aus.

Das Dialogfeld **Buchungs- und Sendebestätigung** zeigt die gewünschte Methode des Debitors das Empfangen von Belegen an. Sie können die Sendemethode ändern, indem Sie die Schaltfläche vom Feld **Beleg senden an** auswählen. Weitere Informationen finden Sie unter [Einrichten von Sendeprofilen](sales-how-setup-document-send-profiles.md).

Der zugehörige Artikel und die Debitorenposten werden nun im System erfasst erstellt, und das Verkaufsangebot wird als PDF-Dokument ausgegeben. Wenn der Auftrag vollständig gebucht wird, wird er aus der Liste von Verkaufsaufträgen entfernt und durch neue Belege in der Übersicht der gebuchten Verkaufsrechnungen und in der Liste gebuchter Auftragslieferungen ersetzt.

## <a name="see-also"></a>Siehe auch
[Verkauf](sales-manage-sales.md)  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Lagerbest](inventory-manage-inventory.md)  
[Senden von Belegen über E-Mail](ui-how-send-documents-email.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

