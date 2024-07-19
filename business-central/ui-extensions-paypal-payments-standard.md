---
title: Verwendung der PayPal-Zahlungen-Standarderweiterung
description: 'In diesem Artikel wird beschrieben, wie Sie die Standarderweiterung verwenden, damit Debitoren Zahlungen mit PayPal vornehmen können.'
author: brentholtorf
ms.author: bholtorf
ms.topic: conceptual
ms.search.keywords: 'app, add-in, manifest, customize'
ms.search.form: '1070, 1071, 1073, 1074'
ms.date: 07/09/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="the-paypal-payments-standard-extension"></a>Die Erweiterung „PayPal Payments Standard“

Mit der Erweiterung „PayPal Payments Standard“ können Sie Ihren Kundenservice verbessern, indem Sie Ihren Kunden die Bezahlung ihrer Rechnungen erleichtern.

Alternativ zur Zahlung per Banküberweisung oder Kreditkarte Karten können Kunden auch über ihr PayPal-Konto bezahlen. Wenn Sie eine Verkaufsrechnung per E-Mail versenden, hat es einen PayPal-Link im E-Mail-Text und im angefügten PDF-Dokument. Wählt der Kunde den Code verknüpfen, öffnet sich die Serviceseite seines PayPal-Kontos und zeigt die Zahlungsdetails an. Der Debitor kann die Rechnung wie jede andere PayPal-Zahlung bezahlen.

Der PayPal Payments Standard-Service hat folgende Vorteile:

* Debitorenzahlungen sind schneller auf Ihrem Bankkonto.
* Debitoren haben mehr Arten, Rechnungen zu bezahlen.
* PayPal bietet einen vertrauenswürdigen Zahlungsservice an, den Debitoren gegenüber der Eingabe von Kreditkarteninformationen auf der Websites bevorzugen.
* PayPal bietet mehrere Arten zur Zahlungsabwicklung an, einschließlich Kreditkartenverarbeitung, PayPal-Konten und andere Quellen.
* Der PayPal-Link kann automatisch allen Verkaufsdokumenten oder manuell vom Benutzer hinzugefügt werden.
* Der „PayPal Payments Standard“-Service kostet keine Monatsgebühren oder Gebühren für die Einrichtung.
* Da dies eine Erweiterung ist, können Sie den „Paypal Payments Standard“-Service einfach aktivieren wenn und wenn Ihr Geschäft sie benötigt.  

Weitere Informationen zum Einrichten der Erweiterung finden Sie unter  [Kundenzahlung über PayPal aktivieren](sales-how-enable-payment-service-extensions.md).

## <a name="register-payments-automatically-for-business-accounts"></a>Zahlungen für Geschäftskonten automatisch erfassen

[!INCLUDE [prod_short](includes/prod_short.md)] können Zahlungen automatisch registrieren, wenn Sie über ein Business-Merchant-Konto für die PayPal Commerce Platform verfügen. Wenn Ihre Kunden eine Rechnung über PayPal verknüpfen bezahlen, [!INCLUDE [prod_short](includes/prod_short.md)] bucht es die Buchungen und schließt den Beleg.

Um diese Funktion zu nutzen, aktivieren Sie auf der Seite  **Einrichtung der Zahlungsregistrierung**  [!INCLUDE [prod_short](includes/prod_short.md)] die Option  **Zahlungen automatisch registrieren**  und bestätigen Sie die Konten, die Sie für die Zahlungen verwenden möchten. Wenn Sie die automatische Zahlungserfassung doch nicht wünschen, können Sie diese Funktion wieder deaktivieren.

> [!TIP]
> Entwickler können Sandbox-Konten verwenden, um das Setup zu testen. Ändern Sie dazu die PayPal-URL in  **sandbox.PayPal.com**. [!INCLUDE [prod_short](includes/prod_short.md)] verwendet die Instant Payment Notification (IPN) von PayPal über notify_url.

## <a name="see-also"></a>Siehe auch

[Anpassen von [!INCLUDE[prod_short](includes/prod_short.md)] mithilfe von Erweiterungen](ui-extensions.md)  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
