---
title: Besondere-E-Mail-Dokumente einrichten | Microsoft Docs
description: Sie können Inhalt definieren, um in den Text eine E-Mail beispielsweise ein Paypal-Link einzufügen. Bestellanforderungen können auch Dokumente an eine E-Mail-Nachricht angehängt werden.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365, cover, body, PayPal, layout
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: fcae17577b448b4271adee299874cf5cad9da79f
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2019
ms.locfileid: "938203"
---
# <a name="send-documents-by-email"></a>Senden von Belegen über E-Mail
Um die Inhalte von Geschäftsbelegen Ihren Geschäftspartnern rasch zu kommunizieren, wie beispielsweise Zahlungsinformationen auf Verkaufsbelegen an Debitoren, können Sie die Berichtslayoutfunktion verwenden, um dokumentspezifischen Inhalt zu definieren, der automatisch in E-Mail-Texte eingefügt wird. Weitere Informationen finden Sie unter [Berichte- und Dokumentenlayouts verwalten](ui-manage-report-layouts.md).

Um E-Mails aus [!INCLUDE[d365fin](includes/d365fin_md.md)] zu aktivieren starten Sie den Leitfaden zur unterstützten Einrichtung **E-Mail einrichten** im Rollencenter.

Sie können praktisch alle Belegarten als Dateianhänge in E-Mails direkt auf der Seite senden, das den Beleg anzeigt. Zusätzlich zum Dateianhang können Sie dokumentspezifische E-Mail-Texte mit Kerninformationen aus dem Beleg einrichten, der vom Standardtext gefolgt wird, der den E-Mail-Empfänger grüßt und den fraglichen Beleg vorstellt. Um Ihren Debitoren anzubieten, für Verkäufe unter Verwendung eines Zahlungsservice wie Paypal elektronisch zu bezahlen, können Sie die Paypal-Informationen und -Links auch in den E-Mail-Text einfügen.

Von allen unterstützten Belegen initiieren Sie das Übermitteln per E-Mail, indem Sie **Senden** auf gebuchten Belegen oder **Buchen und Senden** auf nicht-gebuchten Belegen auswählen.

Wenn das Feld **E-Mail** auf der Seite **Dokument senden an** auf **JA festgelegt wurde (Aufforderung für Einstellungen)**, dann wird die Seite **Senden per E-Mail** geöffnet und mit der Kontaktperson im Feld **Zu** ergänzt und das Dokument als PDF-Datei angehängt. Geben Sie im Feld **Text** entweder den Text manuell ein oder Sie können definieren, dass das Feld mit einem dokumentspezifischen E-Mail-Text ausgefüllt wird, den Sie eingerichtet haben.

Nachfolgend wird beschrieben, wie der Bericht **Verkaufsrechnung** für dokumentspezifische E-Mail-Texte verwendet wird, wenn Sie gebuchte Verkaufsrechnungen senden.

## <a name="to-set-up-a-document-specific-email-body-for-sales-invoices"></a>Einen dokumentspezifischen E-Mail-Text für Verkaufsrechnungen einrichten
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Berichtsauswahl Verkauf** ein, und wählen dann den zugehörigen Link aus.
2. Auf der Seite **Berichts-Auswahl - Verkauf** unter **Verwendung** wählen Sie **Rechnung**.
3. In einer neuen Zeile im Feld **Berichts-ID** wählen Sie beispielsweise Standardbericht 1306.
4. Wählen Sie das Kontrollkästchen **Für E-Mail-Text verwenden**.
5. Wählen Sie das Feld **E-Mail-Text-Layout-Code** und wählen Sie ein Layout aus der Liste aus.

    Berichtslayouts definieren das Format und den Inhalt des E-Mail-Texts, einschließlich den Standardtext, der den Kernbeleginformationen im E-Mail-Text vorangeht. Sie können alle verfügbaren Berichtslayouts sehen, wenn Sie die Schaltfläche **Aus vollständiger Liste auswählen** in der Liste auswählen.
6. Um das Layout anzusehen oder zu bearbeiten, auf dem der E-Mail-Text basiert, gehen Sie zur Seite **Benutzerdefinierte Berichtslayouts** und wählen die Aktion **Layout bearbeiten** aus.
7. Um Ihren Debitoren anzubieten, für Verkäufe unter Verwendung eines Zahlungsservice wie Paypal elektronisch zu bezahlen, können Sie die Paypal-Informationen und -Links auch in den E-Mail-Text einfügen. Weitere Informationen finden Sie unter [Aktivieren Sie Debitoren-Zahlung durch Paypal](sales-how-enable-payment-service-extensions.md)
8. Wählen Sie die Schaltfläche **OK** aus.

Wenn Sie jetzt beispielsweise die Aktion **Senden** auf der Seite **Gebuchte Verkaufsrechnung** auswählen, enthält der E-Mail-Text die Beleginformationen 1306 des Berichts, der vom formatierten Standardtext entsprechend dem Berichtslayout stammt, das Sie in Schritt 5 ausgewählt haben.

Nachfolgend wird beschrieben, wie eine gebuchte Verkaufsrechnung als E-Mail mit dem Beleg gesendet wird, der als PDF-Datei angehängt ist und einen dokumentspezifischen E-Mail-Text enthält.

## <a name="to-send-documents-by-email"></a>Senden von Belegen über E-Mail
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Gebuchte Verkaufsrechnungen** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die relevante gebuchte Verkaufsrechnung aus und wählen Sie die Aktion **Senden**. Die Seite **Dokument senden an** wird geöffnet.
3. Wählen Sie im Feld **E-Mail** **Ja (Aufforderung für Einstellung)** aus. Weitere Informationen finden Sie unter [Einrichten von Sendeprofilen](sales-how-setup-document-send-profiles.md).
4. Wählen Sie die Schaltfläche **OK** aus. Die Seite **E-Mails senden** wird geöffnet.
5. Im Feld **Zu** geben Sie eine gültige E-Mail-Adresse ein. Der Standardwert ist die E-Mail-Adresse des Debitors.
6. Geben Sie im Feld **Betreff** einen beschreibenden Betreff ein. Der Standardwert ist der Debitorennamen und die Rechnungsnummer.
7. Im Feld **Anhang** wird die generierte Rechnung standardmäßig als PDF\_Datei angehängt. Wählen Sie die Suchschaltfläche, um die Datei zu öffnen oder eine andere Datei anzufügen.
8. Geben Sie im **Nachrichtentext**-Feld eine kurze Mitteilung an den Empfänger ein.

    Wenn ein belegspezifischer E-Mail-Text auf der Seite **Berichts-Auswahl - Verkauf** eingerichtet wird, wird das Feld **Text** automatisch ausgefüllt. Weitere Informationen finden Sie unter [Einrichten eines dokumentspezifischen E-Mail-Texts für Verkaufsrechnungen](ui-how-send-documents-email.md#to-set-up-a-document-specific-email-body-for-sales-invoices).
9. Wählen Sie die Schaltfläche **OK**, um die E-Mail zu senden.

> [!NOTE]  
>   Wenn Sie die E-Mail-Einstellungen nicht jedes Mal ändern wollen, wenn Sie ein Dokument per E-Mail senden, können Sie die Option **Ja** (Standardeinstellungen verwenden) im Feld **E-Mail** auf der Seite **Dokument senden** an auswählen. In diesem Fall wird die Seite **E-Mail senden** nicht geöffnet. Siehe dazu auch Schritt 4. Weitere Informationen finden Sie unter [Einrichten von Sendeprofilen](sales-how-setup-document-send-profiles.md).

## <a name="see-also"></a>Siehe auch
[Verwaltung von Berichts- und Beleg-Layouts](ui-manage-report-layouts.md)  
[E-Mail einrichten](admin-how-setup-email.md)  
[Fakturieren eines Verkaufs](sales-how-invoice-sales.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
