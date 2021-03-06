---
title: Verkaufsangebote für einen Kunden erstellen
description: Beschreibt, wie Verkaufsangebote oder eine Anforderung erstellt wird, um Ihr Angebot zu erfassen, um unter bestimmten Bedingungen einem Debitoren zu verkaufen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: a538b7099521b10227bf5aeaefad0a9c60971068
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115540"
---
# <a name="make-sales-quotes"></a>Verkaufsangebote machen

Sie erstellen eine Angebotsrechnung, um Ihr Angebot für den Debitor zu erfassen, um bestimmte Produkte unter speziellen Lieferungs- und Zahlungsbedingungen zu verkaufen. Sie können das Verkaufsangebot an den Debitor senden, um das Angebot mitzuteilen. Sie können den Beleg als PDF-Dateianhang senden. Sie können den E-Mail-Text auch, der mit einer Zusammenfassung des Angebots vorab ausgefüllt wurde. Weitere Informationen finden Sie unter [Senden von Dkumenten über E-Mail](ui-how-send-documents-email.md).

Während Sie mit dem Debitor verhandeln, können Sie das Verkaufsangebot ändern wie benötigt und erneut versenden. Wenn der Debitor das Angebot annimmt, wandeln Sie das Verkaufsangebot in eine Verkaufsrechnung, in der Sie den Verkauf verarbeiten. Weitere Informationen finden Sie unter [Fakturieren eines Verkaufs](sales-how-invoice-sales.md) und [Neue Produkte verkaufen](sales-how-sell-products.md).

Sie können die oberen Infoboxen des Verkaufsangebotes auf zwei Arten ausfüllen, abhängig davon, ob der Debitor bereits registriert ist oder nicht. Siehe Schritt 2 und 3 im folgenden Verfahren.

## <a name="to-create-a-sales-quote"></a>So erstellen Sie Verkaufsangebote:

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Angebote** ein, und wählen Sie dann den entsprechenden Link aus.
2. Geben Sie im Feld **Debitor** den Namen eines vorhandenen Debitors ein.

   Andere Felder auf der Seite **Verkaufsangebot** werden nun mit den Standardinformationen vom ausgewählten Debitor ausgefüllt.  

    [!INCLUDE [sales-create-customer](includes/sales-create-customer.md)]

    Felder im Verkaufsangebot werden mit den Informationen, die Sie festgelegt haben, in der neuen Debitorenkarte ausgefüllt.  
3. Füllen Sie auf der Seite **Verkaufsangebot** die Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Sie können nun die Verkaufsauftragszeilen für Produkte füllen, die Sie an den Debitoren oder für jede mögliche Transaktion mit dem Debitoren verkaufen, den Sie im Sachkonto buchen möchten.  

    Wenn Sie wiederkehrende Verkaufszeilen für den Debitor wie einen Monatsersatzauftrag, eingerichtet haben, können Sie diese Zeilen auf der Rechnung durch Auswählen der Schaltfläche **Wiederkehrende Verkaufszeilen holen** einfügen.  

4. Wählen Sie im Inforegister **Zeilen** im Feld **Art** aus, welche Art des Produkts, der Kosten oder der Transaktion Sie für den Debitor mit der Verkaufszeile buchen werden.
5. Geben Sie im Feld **Nr.** Feld, einen Datensatz auswählen, um entsprechend dem Wert im Feld **Art** zu buchen.

    Sie lassen das **Nr.** Feld ist in folgenden Fällen leer:
    - Wenn die Zeile für einen Kommentar ist. Die Bemerkung im Feld **Beschreibung** enthalten ist.
    - Wenn die Zeile für einen Katalogartikel ist. Wählen Sie die Aktion **Katalogartikel auswählen**. Weitere Informationen finden Sie unter [Arbeiten mit Katalogelementen](inventory-how-work-nonstock-items.md).

6. Geben Sie im Feld **Menge** ein, wie viele Einheiten des Produkts, der Kosten oder der Transaktion, in der Zeile des Debitors gespeichert werden soll.

    > [!NOTE]  
    >  Wenn Artikel vom Typ **Service** sind, oder das **Typ**-Feld **Ressource** enthält, ist die Menge eine Zeiteinheit wie Stunden, wie im Feld **Einheit des Messcodes** der Zeile angegeben. Weitere Informationen finden Sie unter [Einrichten von Einheiten](inventory-how-setup-units-of-measure.md)

    Der Wert im Feld **Zeilenbetrag** Feld wird als *VK-Preis* x *Menge* berechnet.  

    Der Preis und der Zeilenbetrag auf den Verkaufsrechnungszeilen werden mit oder ohne MwSt. angezeigt je nachdem, was Sie im Feld **Preis inklusive Mehrwertsteuer** auf der Debitorenkarte ausgewählt haben.  
7. Wenn Sie Skonto gewähren möchten, geben Sie einen Prozentsatz im Feld **Zeilenrabatt %** ein. Der Wert im Feld **Zeilenbetrag** wird entsprechend aktualisiert.  

    Wenn Sie bestimmte Artikelpreise für den Debitor auf dem Inforegister **Verkaufspreise und Verkaufspreis-Zeilenrabatte** eingerichtet haben, werden der Preis und der Betrag auf der Rechnungszeile automatisch aktualisiert, wenn die vereinbarten Preiskriterien erfüllt sind. Weitere Informationen finden Sie unter [Erfassen von Verkaufspreisen, Rabatt und Zahlungsvereinbarungen](sales-how-record-sales-price-discount-payment-agreements.md)  
8. Wiederholen Sie die Schritte 4 bis 7 für jedes Produkt, das Sie an den Debitoren verkaufen möchten.

    Die Summen unter den Zeilen werden berechnet, während Sie Zeilen erstellen oder ändern.  
9. Geben Sie im Feld **Rabattbetrag in Rechnung stellen** einen Betrag ein, der vom Wert abgezogen werden soll, der im Feld **Total inklusive Mehrwertsteuer** im unteren Bereich der Rechnung angezeigt wird.

    Wenn Sie Rechnungsrabatte für den Debitor eingerichtet haben, wird der angegebene Prozentwert automatisch in das Feld **Rechnungsrabatt in Prozent** eingetragen, sobald die Kriterien erfüllt sein, und der entsprechende Betrag wird im Feld **Rechnungsbetrag mit Rabatt ohne Mehrwertsteuer** eingefügt. Weitere Informationen finden Sie unter [Erfassen von Verkaufspreisen, Rabatt und Zahlungsvereinbarungen](sales-how-record-sales-price-discount-payment-agreements.md)

    > [!TIP]
    > Um **Angebot gültig bis Datum** haben, die automatisch mit einigen Tage nach Angebotserstellung ausgefüllt ist, können Sie das **Angebots-Gültigkeits-Berechnung** auf der Seite **Debitoren & Verkauf** ausfüllen.

10. Wenn die Verkaufsangebotszeilen ausgeführt werden, wählen Sie die Aktion **Per E-Mail senden** aus.
11. Auf der Seite **E-Mail senden** füllen Sie die restlichen Felder aus und überprüfen Sie das eingebettete Verkaufsangebot. Weitere Informationen finden Sie unter [Senden von Dkumenten über E-Mail](ui-how-send-documents-email.md).
12. Wenn der Debitor das Angebot annimmt, wählen Sie **Rechnung erstellen** oder **Auftrag vornehmen** aus.

Das Verkaufsangebot wird aus der Datenbank entfernt. Eine Verkaufsrechnung oder ein Verkaufsauftrag wird auf der Basis der Informationen im Verkaufsangebot erstellt, in dem Sie den Verkauf verarbeiten können. In der erstellten Verkaufsrechnung gibt das Feld **Angebotsnr.** die Nummer des Verkaufsauftrags oder der Rechnung  n, aus dem sie erstellt wurde. Weitere Informationen finden Sie unter [Fakturieren eines Verkaufs](sales-how-invoice-sales.md) und [Neue Produkte verkaufen](sales-how-sell-products.md).  

## <a name="external-document-number"></a>Externe Belegnummer

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-also"></a>Siehe auch

[Verkauf](sales-manage-sales.md)  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Dokumente per E-Mail versenden](ui-how-send-documents-email.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]