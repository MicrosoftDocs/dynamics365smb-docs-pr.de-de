---
title: Verkaufsangebote machen
description: 'Lesen Sie, wie Sie ein Verkaufsangebot oder einen Beleg für eine Angebotsanfrage (RFQ) erstellen, um Ihr Angebot an einen Debitor oder Interessenten zum Verkauf von Produkten zu bestimmten Bedingungen zu erstellen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.search.form: '41, 9300'
ms.date: 07/12/2021
ms.author: edupont
---
# <a name="make-sales-quotes"></a>Verkaufsangebote machen

Sie erstellen ein Verkaufsangebot, um Ihren Datensatz an einen Debitor oder Interessenten zu erstellen, um bestimmte Produkte zu bestimmten Liefer- und Zahlungsbedingungen zu verkaufen. Sie können das Verkaufsangebot an den Debitor senden, um das Angebot mitzuteilen. Sie können den Beleg als PDF-Dateianhang senden. Sie können den E-Mail-Text auch, der mit einer Zusammenfassung des Angebots vorab ausgefüllt wurde. Weitere Informationen finden Sie unter [Senden von Dkumenten über E-Mail](ui-how-send-documents-email.md).

Während Sie mit dem Kunden oder Interessenten verhandeln, können Sie das Verkaufsangebot so oft wie nötig ändern und erneut versenden. Wenn der Debitor das Angebot annimmt, wandeln Sie das Verkaufsangebot in eine Verkaufsrechnung, in der Sie den Verkauf verarbeiten. Weitere Informationen finden Sie unter [Fakturieren eines Verkaufs](sales-how-invoice-sales.md) und [Neue Produkte verkaufen](sales-how-sell-products.md).

In den meisten Fällen senden Sie Verkaufsangebote an potenzielle Kunden. Sie haben oft einen Ansprechpartner, mit dem Sie verhandeln. Wenn dieser dann Ihr Angebot annimmt, wandeln Sie das Verkaufsangebot in einen Auftrag um und registrieren den Interessenten als Kunden in [!INCLUDE [prod_short](includes/prod_short.md)]. Im folgenden Verfahren konzentrieren wir uns auf Kontakte, aber Sie können auch Angebote an bestehende Kunden senden.  

## <a name="to-create-a-sales-quote"></a>So erstellen Sie Verkaufsangebote:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Verkaufsangebote** ein, und wählen Sie dann den entsprechenden Link.
2. Geben Sie den Kontakt oder Debitor an, an den Sie das Verkaufsangebot senden möchten.

    - Wenn es sich um ein Verkaufsangebot für einen bestehenden Kontakt handelt, geben Sie den Namen im Feld **Kontaktnr.** an. Feld eingetragen.  

        Wenn das Verkaufsangebot für einen bestehenden Kunden bestimmt ist, geben Sie den Debitor im Feld **Kunde** an.
    - Wenn der Kontakt nicht registriert ist, gehen Sie wie folgt vor:

        1. Wählen Sie im Feld **Kontaktnr.** Feld, wählen Sie die Schaltfläche :::image type="icon" source="media/assist-edit-icon.png" border="false"::: bearbeiten.
        2. Wählen Sie im Dialogfenster zur Auswahl des Kontakts die Aktion **Neu** und füllen Sie dann die entsprechenden Felder aus. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] Für weitere Informationen siehe [Kontakte erstellen](marketing-create-contact-companies.md).  
        3. Wenn Sie die Kontaktkarte ausgefüllt haben, wählen Sie den neu erstellten Kontakt in der Liste der Kontakte aus und wählen dann die Schaltfläche OK, um zum Verkaufsangebot zurückzukehren.

        Mehrere Felder des Verkaufsangebots sind nun mit den Informationen gefüllt, die Sie auf der neuen Kontaktkarte angegeben haben.

        > [!NOTE]
        > Um Steuern und Preise für ein Angebot korrekt zu berechnen, müssen Sie die entsprechende Kundenvorlage im Feld **Kundenvorlagencode** auswählen. Die Vorlage wird verwendet, um den Kontakt in einen Debitor umzuwandeln, sobald das Angebot in einen Verkaufsauftrag oder eine Rechnung umgewandelt wird.
    -  Wenn es sich um ein Angebot für einen neuen Kunden handelt, müssen Sie den Kunden hinzufügen. Weitere Informationen finden Sie unter [Neue Debitoren registrieren](sales-how-register-new-customers.md).  

3. Füllen Sie auf der Seite **Verkaufsangebot** die Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Jetzt können Sie die Verkaufszeilen für die Produkte, die Sie verkaufen, oder für jede Transaktion mit dem Kunden oder Interessenten, die Sie in einem Sachkonto aufzeichnen wollen, ausfüllen.  

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
8. Wiederholen Sie die Schritte 4 bis 7 für jedes Produkt, das Sie dem Kontakt anbieten wollen.

    Die Summen unter den Zeilen werden berechnet, während Sie Zeilen erstellen oder ändern.  
9. Geben Sie im Feld **Rabattbetrag in Rechnung stellen** einen Betrag ein, der vom Wert abgezogen werden soll, der im Feld **Total inklusive Mehrwertsteuer** im unteren Bereich der Rechnung angezeigt wird.

    Wenn Sie Rechnungsrabatte für den Debitor eingerichtet haben, wird der angegebene Prozentwert automatisch in das Feld **Rechnungsrabatt in Prozent** eingetragen, sobald die Kriterien erfüllt sein, und der entsprechende Betrag wird im Feld **Rechnungsbetrag mit Rabatt ohne Mehrwertsteuer** eingefügt. Weitere Informationen finden Sie unter [Erfassen von Verkaufspreisen, Rabatt und Zahlungsvereinbarungen](sales-how-record-sales-price-discount-payment-agreements.md)

    > [!TIP]
    > Um **Angebot gültig bis Datum** haben, die automatisch mit einigen Tage nach Angebotserstellung ausgefüllt ist, können Sie das **Angebots-Gültigkeits-Berechnung** auf der Seite **Debitoren & Verkauf** ausfüllen.

10. Wenn die Verkaufsangebotszeilen ausgeführt werden, wählen Sie die Aktion **Per E-Mail senden** aus.
11. Auf der Seite **E-Mail senden** füllen Sie die restlichen Felder aus und überprüfen Sie das eingebettete Verkaufsangebot. Weitere Informationen finden Sie unter [Dokumente per E-Mail versenden](ui-how-send-documents-email.md).
12. Wenn der Kontakt das Angebot annimmt, wählen Sie die Aktion **Bestellung vornehmen**.  

    Alternativ, wenn Ihr Unternehmen diesen Prozess bevorzugt, wählen Sie die Aktion **Rechnung erstellen**.  
    > [!NOTE]
    > Wenn Sie in Schritt 2 einen Debitor hinzugefügt haben, werden Sie aufgefordert, die Umwandlung des Angebots in eine Bestellung zu bestätigen.  
    >
    > Wenn Sie in Schritt 2 einen Kontakt von einem Interessenten hinzugefügt haben, werden Sie aufgefordert, die folgenden Schritte auszuführen:
    >
    >  - Konvertieren Sie den Kontakt oder Interessenten in einen Debitor, indem Sie eine der Kontaktkonvertierungsvorlagen auswählen. Weitere Informationen finden Sie unter [So erstellen Sie einen Kontakt als Debitor, Kreditor , Mitarbeiter oder Bankkonto von einem Kontakt](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  
    > - Bestätigen Sie die Umwandlung des Angebots in einen Auftrag.

Durch die Umwandlung wird das Verkaufsangebot aus der Datenbank entfernt. Eine Verkaufsrechnung oder ein Verkaufsauftrag wird auf der Basis der Informationen im Verkaufsangebot erstellt, damit Sie den Verkauf verarbeiten können. In der erstellten Verkaufsrechnung gibt das Feld **Angebotsnr.** die Nummer des Verkaufsauftrags oder der Rechnung  n, aus dem sie erstellt wurde. Weitere Informationen finden Sie unter [Fakturieren eines Verkaufs](sales-how-invoice-sales.md) und [Neue Produkte verkaufen](sales-how-sell-products.md).  

## <a name="external-document-number"></a>Externe Belegnummer

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/create-sales-documents-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch

[Verkauf](sales-manage-sales.md)  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Dokumente per E-Mail versenden](ui-how-send-documents-email.md)  
[Beleg archivieren](across-how-to-archive-documents.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
