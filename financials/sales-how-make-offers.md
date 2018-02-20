---
title: "Verkaufsangebote für einen Kunden erstellen| Microsoft Docs"
description: Beschreibt, wie Verkaufsangebote oder eine Anforderung erstellt wird, um Ihr Angebot zu erfassen, um unter bestimmten Bedingungen einem Kunden zu verkaufen.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 08/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 552fbf283a9149c430ea1ed94bcea4bd22e43fea
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="make-offers"></a>Aufträge erstellen
Sie erstellen eine Angebotsrechnung, um Ihr Angebot für den Debitor zu erfassen, um bestimmte Produkte unter speziellen Lieferungs- und Zahlungsbedingungen zu verkaufen. Sie können das Verkaufsangebot an den Debitor senden, um das Angebot mitzuteilen. Sie können den Beleg als PDF-Dateianhang senden. Sie können den E-Mail-Text auch, der mit einer Zusammenfassung des Angebots vorab ausgefüllt wurde. Weitere Informationen finden Sie unter [Senden von Dkumenten über E-Mail](ui-how-send-documents-email.md).

Während Sie mit dem Debitor verhandeln, können Sie das Verkaufsangebot ändern wie benötigt und erneut versenden. Wenn der Kunde das Angebot annimmt, wandeln Sie das Verkaufsangebot in eine Verkaufsrechnung, in der Sie den Verkauf verarbeiten. Weitere Informationen finden Sie unter [Fakturieren von Verkäufen](sales-how-invoice-sales.md) und [Neue Produkte verkaufen](sales-how-sell-products.md).

Sie können die oberen Infoboxen des Verkaufsangebotes auf zwei Arten ausfüllen, abhängig davon, ob der Debitor bereits registriert ist oder nicht. Siehe Schritt 2 und 3 im folgenden Verfahren.

## <a name="to-create-a-sales-quote"></a>So erstellen Sie Verkaufsangebote:
Auf der Seite Homepage wählen Sie die Aktion **Verkaufsangebote** aus.  
2. Geben Sie im Feld **Debitor** den Namen eines vorhandenen Debitors ein.

   Andere Felder im Fenster **Verkaufsangebot** werden nun mit den Standardinformationen vom ausgewählten Debitor ausgefüllt. Wenn der Debitor noch nicht erfasst wurde, dann führen Sie die folgenden Schritte durch:
3. Geben Sie im Feld **Debitor** den Namen eines neuen Debitors ein.
4. Klicken Sie im Dialogfeld auf die Schaltfläche **Ja**, um die Übertragung zu bestätigen.
5. Im Fenster **Vorlage für neuen Debitor wählen** wählen Sie eine Vorlage, auf der die neue Debitorenkarte basieren soll, und dann wählen Sie die Schaltfläche **OK**.
6. Eine neue Debitorenkarte wird geöffnet, vorausgefüllt mit Informationen auf der ausgewählten Debitorenvorlage. Füllen Sie die restlichen Felder aus. Weitere Informationen finden Sie unter [Neue Kunden registrieren](sales-how-register-new-customers.md).  
7. Wenn Sie die Debitorenkarte abgeschlossen haben, wählen Sie die Schaltfläche **OK**, um zum Fenster **Verkaufsangebot** zurückzugehen.

   Felder im Verkaufsangebot werden mit den Informationen, die Sie festgelegt haben, in der neuen Debitorenkarte ausgefüllt.  
8. Füllen Sie im Fenster **Verkaufsangebot** die Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Sie können nun die Verkaufsauftragszeilen für Produkte füllen, die Sie an den Kunden oder für jede mögliche Transaktion mit dem Kunden verkaufen, den Sie im Sachkonto buchen möchten.   

Wenn Sie wiederkehrende Verkaufszeilen für den Debitor wie einen Monatsersatzauftrag, eingerichtet haben, können Sie diese Zeilen auf der Rechnung durch Auswählen der Schaltfläche **Wiederkehrende Verkaufszeilen holen** einfügen.  
9. Wählen Sie im Inforegister **Zeilen** im Feld **Art** aus, welche Art des Produkts, der Kosten oder der Transaktion Sie für den Debitor mit der Verkaufszeile buchen werden.
10. Geben Sie im Feld **Nr.** Feld, einen Datensatz auswählen, um entsprechend dem Wert im Feld **Art** zu buchen.

 Sie lassen das **Nr.** Feld leer in folgenden Fällen: - Wenn die Zeile für eine Bemerkung ist. Die Bemerkung im Feld **Beschreibung** enthalten ist.
 - Wenn die Zeile für einen Katalogartikel ist. Wählen Sie die Aktion **Nicht-Katalogartikel auswählen**. Weitere Informationen finden Sie unter [Arbeiten mit nicht im Bestand vorhandenen Artikeln](inventory-how-work-nonstock-items.md).

11. Geben Sie im Feld **Menge** ein, wie viele Einheiten des Produkts, der Kosten oder der Transaktion, in der Zeile des Debitors gespeichert werden soll.

    > [!NOTE]  
>   Für Artikel des Typs **Artikel - Service** oder **Ressource** ist die Menge eine Zeiteinheit wie Stunden, wie im Feld **Einheit des Messcodes** der Zeile angegeben.  

    Der Wert im Feld **Zeilenbetrag** Feld wird als *VK-Preis* x *Menge* berechnet.  

    Der Preis und der Zeilenbetrag auf den Verkaufsrechnungszeilen werden mit oder ohne MwSt. angezeigt je nachdem, was Sie im Feld **Preis inklusive Mehrwertsteuer** auf der Debitorenkarte ausgewählt haben.  
12. Wenn Sie Skonto gewähren möchten, geben Sie einen Prozentsatz im Feld **Zeilenrabatt %** ein. Der Wert im Feld **Zeilenbetrag** wird entsprechend aktualisiert.  

    Wenn Sie bestimmte Artikelpreise für den Debitor auf dem Inforegister **Verkaufspreise und Verkaufspreis-Zeilenrabatte** eingerichtet haben, werden der Preis und der Betrag auf der Rechnungszeile automatisch aktualisiert, wenn die vereinbarten Preiskriterien erfüllt sind. Weitere Informationen finden Sie unter [Erfassen von Verkaufspreisen, Skonti und Zahlungsvereinbarungen](sales-how-record-sales-price-discount-payment-agreements.md)  
13. Wiederholen Sie die Schritte 9 bis 12 für jedes Produkt, das Sie an den Kunden verkaufen möchten.  

    Die Summen unter den Zeilen werden berechnet, während Sie Zeilen erstellen oder ändern.  
14. Geben Sie im Feld **Rabattbetrag in Rechnung stellen** einen Betrag ein, der vom Wert abgezogen werden soll, der im Feld **Total inklusive Mehrwertsteuer** im unteren Bereich der Rechnung angezeigt wird.

    Wenn Sie Rechnungsrabatte für den Debitor eingerichtet haben, wird der angegebene Prozentwert automatisch in das Feld **Rechnungsrabatt in Prozent** eingetragen, sobald die Kriterien erfüllt sein, und der entsprechende Betrag wird im Feld **Rechnungsbetrag mit Rabatt ohne Mehrwertsteuer** eingefügt. Weitere Informationen finden Sie unter [Erfassen von Verkaufspreisen, Skonti und Zahlungsvereinbarungen](sales-how-record-sales-price-discount-payment-agreements.md)
15. Wenn die Verkaufsangebotszeilen ausgeführt werden, wählen Sie die Aktion **Per E-Mail senden** aus.
16. Im Fenster **E-Mail senden** füllen Sie die restlichen Felder aus und überprüfen Sie das eingebettete Verkaufsangebot. Weitere Informationen finden Sie unter [Senden von Dkumenten über E-Mail](ui-how-send-documents-email.md).
17. Wenn der Kunde das Angebot annimmt, wählen Sie **Rechnung erstellen** oder **Auftrag vornehmen** aus.

Das Verkaufsangebot wird aus der Datenbank entfernt. Eine Verkaufsrechnung oder ein Verkaufsauftrag wird auf der Basis der Informationen im Verkaufsangebot erstellt, in dem Sie den Verkauf verarbeiten können. In der erstellten Verkaufsrechnung gibt das Feld **Angebotsnr.** die Nummer des Verkaufsauftrags oder der Rechnung  n, aus dem sie erstellt wurde. Weitere Informationen finden Sie unter [Fakturieren von Verkäufen](sales-how-invoice-sales.md) und [Neue Produkte verkaufen](sales-how-sell-products.md).

## <a name="see-also"></a>Siehe auch
[Verkauf](sales-manage-sales.md)  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Senden von Belegen über E-Mail](ui-how-send-documents-email.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

