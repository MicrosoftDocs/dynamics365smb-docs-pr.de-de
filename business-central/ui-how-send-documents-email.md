---
title: Besondere-E-Mail-Dokumente einrichten | Microsoft Docs
description: Sie können Inhalt definieren, um in den Text eine E-Mail beispielsweise ein Paypal-Link einzufügen. Bestellanforderungen können auch Dokumente an eine E-Mail-Nachricht angehängt werden.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.workload: na
ms.search.keywords: SMTP, mail, Microsoft 365, cover, body, PayPal, layout
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 72ed1cba131e76eba2020e4cca9c900b9b2ed45c
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923420"
---
# <a name="send-documents-by-email"></a>Senden von Belegen über E-Mail

Um die Inhalte von Geschäftsbelegen Ihren Geschäftspartnern rasch zu kommunizieren, wie beispielsweise Zahlungsinformationen auf Verkaufsbelegen an Debitoren, können Sie die Berichtslayoutfunktion verwenden, um dokumentspezifischen Inhalt zu definieren, der automatisch in E-Mail-Texte eingefügt wird. Weitere Informationen finden Sie unter [Berichte- und Dokumentenlayouts verwalten](ui-manage-report-layouts.md).

Um E-Mails aus [!INCLUDE[d365fin](includes/d365fin_md.md)] zu aktivieren starten Sie den Leitfaden zur unterstützten Einrichtung **E-Mail einrichten** im Rollencenter.

Sie können praktisch alle Belegarten als Dateianhänge in E-Mails direkt auf der Seite senden, das den Beleg anzeigt. Zusätzlich zum Dateianhang können Sie dokumentspezifische E-Mail-Texte mit Kerninformationen aus dem Beleg einrichten, der vom Standardtext gefolgt wird, der den E-Mail-Empfänger grüßt und den fraglichen Beleg vorstellt. Um Ihren Debitoren anzubieten, für Verkäufe unter Verwendung eines Zahlungsservice wie Paypal elektronisch zu bezahlen, können Sie die Paypal-Informationen und -Links auch in den E-Mail-Text einfügen.

Von allen unterstützten Belegen initiieren Sie das Übermitteln per E-Mail, indem Sie **Senden** auf gebuchten Belegen oder **Buchen und Senden** auf nicht-gebuchten Belegen auswählen.

Wenn das Feld **E-Mail** auf der Seite **Dokument senden an** auf **JA festgelegt wurde (Aufforderung für Einstellungen)** , dann wird die Seite **Senden per E-Mail** geöffnet und mit der Kontaktperson im Feld **Zu** ergänzt und das Dokument als PDF-Datei angehängt. Geben Sie im Feld **Text** entweder den Text manuell ein oder Sie können definieren, dass das Feld mit einem dokumentspezifischen E-Mail-Text ausgefüllt wird, den Sie eingerichtet haben.

Nachfolgend wird beschrieben, wie der Bericht **Verkaufsrechnung** für dokumentspezifische E-Mail-Texte verwendet wird, wenn Sie gebuchte Verkaufsrechnungen senden.

## <a name="to-set-up-a-document-specific-email-body-for-sales-invoices"></a>Einen dokumentspezifischen E-Mail-Text für Verkaufsrechnungen einrichten

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Berichtsauswahl Verkäufe** ein und wählen Sie dann den entsprechenden Link.
2. Auf der Seite **Berichts-Auswahl - Verkauf** unter **Verwendung** wählen Sie **Rechnung** .
3. In einer neuen Zeile im Feld **Berichts-ID** wählen Sie beispielsweise Standardbericht 1306.
4. Wählen Sie das Kontrollkästchen **Für E-Mail-Text verwenden** .
5. Wählen Sie das Feld **E-Mail-Text-Layout-Code** und wählen Sie ein Layout aus der Liste aus.

    Berichtslayouts definieren das Format und den Inhalt des E-Mail-Texts, einschließlich den Standardtext, der den Kernbeleginformationen im E-Mail-Text vorangeht. Sie können alle verfügbaren Berichtslayouts sehen, wenn Sie die Schaltfläche **Aus vollständiger Liste auswählen** in der Liste auswählen.
6. Um das Layout anzusehen oder zu bearbeiten, auf dem der E-Mail-Text basiert, gehen Sie zur Seite **Benutzerdefinierte Berichtslayouts** und wählen die Aktion **Layout bearbeiten** aus.
7. Um Ihren Debitoren anzubieten, für Verkäufe unter Verwendung eines Zahlungsservice wie Paypal elektronisch zu bezahlen, können Sie die Paypal-Informationen und -Links auch in den E-Mail-Text einfügen. Weitere Informationen finden Sie unter [Aktivieren Sie Debitoren-Zahlung durch Paypal](sales-how-enable-payment-service-extensions.md)
8. Wählen Sie die Schaltfläche **OK** aus.

Wenn Sie jetzt beispielsweise die Aktion **Senden** auf der Seite **Gebuchte Verkaufsrechnung** auswählen, enthält der E-Mail-Text die Beleginformationen 1306 des Berichts, der vom formatierten Standardtext entsprechend dem Berichtslayout stammt, das Sie in Schritt 5 ausgewählt haben.

Nachfolgend wird beschrieben, wie eine gebuchte Verkaufsrechnung als E-Mail mit dem Beleg gesendet wird, der als PDF-Datei angehängt ist und einen dokumentspezifischen E-Mail-Text enthält.

## <a name="to-send-documents-by-email"></a>Senden von Belegen über E-Mail

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Gebuchte Verkaufsrechnungen** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die relevante gebuchte Verkaufsrechnung aus und wählen Sie die Aktion **Senden** . Die Seite **Dokument senden an** wird geöffnet.
3. Wählen Sie im Feld **E-Mail** **Ja (Aufforderung für Einstellung)** aus. Weitere Informationen finden Sie unter [Einrichten von Sendeprofilen](sales-how-setup-document-send-profiles.md).
4. Wählen Sie die Schaltfläche **OK** aus. Die Seite **E-Mails senden** wird geöffnet.
5. Im Feld **Zu** geben Sie eine gültige E-Mail-Adresse ein. Der Standardwert ist die E-Mail-Adresse des Debitors.
6. Geben Sie im Feld **Betreff** einen beschreibenden Betreff ein. Der Standardwert ist der Debitorennamen und die Rechnungsnummer.
7. Im Feld **Anhang** wird die generierte Rechnung standardmäßig als PDF\_Datei angehängt.
8. Geben Sie im **Nachrichtentext** -Feld eine kurze Mitteilung an den Empfänger ein.

    Wenn ein belegspezifischer E-Mail-Text auf der Seite **Berichts-Auswahl - Verkauf** eingerichtet wird, wird das Feld **Text** automatisch ausgefüllt. Weitere Informationen finden Sie unter [Einrichten eines dokumentspezifischen E-Mail-Texts für Verkaufsrechnungen](ui-how-send-documents-email.md#to-set-up-a-document-specific-email-body-for-sales-invoices).
9. Wählen Sie die Schaltfläche **OK** , um die E-Mail zu senden.

> [!NOTE]  
> Wenn Sie die E-Mail-Einstellungen nicht jedes Mal ändern wollen, wenn Sie ein Dokument per E-Mail senden, können Sie die Option **Ja** (Standardeinstellungen verwenden) im Feld **E-Mail** auf der Seite **Dokument senden** an auswählen. In diesem Fall wird die Seite **E-Mail senden** nicht geöffnet. Siehe dazu auch Schritt 4. Weitere Informationen finden Sie unter [Einrichten von Sendeprofilen](sales-how-setup-document-send-profiles.md).  

## <a name="documents-marked-as-printed-when-they-are-sent"></a>Belege, die beim Senden als gedruckt markiert sind

Einige Belege in [!INCLUDE[prodshort](includes/prodshort.md)] verfügen über ein Feld, das angibt, wie oft der Beleg gedruckt wurde. Das Feld wird auch aktualisiert, wenn Sie den Beleg nicht drucken, sondern stattdessen per E-Mail senden. Das Feld wird selbst dann aktualisiert, wenn Sie den Beleg überhaupt nicht senden, z. B. wenn Ihr Unternehmen keine E-Mail eingerichtet hat oder wenn für den Kontakt, an den Sie den Beleg senden möchten, keine E-Mail-Adresse angegeben ist. Für alle Szenarien, soweit [!INCLUDE[prodshort](includes/prodshort.md)] betroffen ist, wird der Beleg gedruckt, weil eine PDF-Datei generiert wird.  

Der Benutzer sieht diese generierte Datei möglicherweise nicht, was auch der Grund ist, warum das Feld aktualisiert wird.

## <a name="see-also"></a>Siehe auch

[Verwaltung von Berichts- und Dokumentlayouts](ui-manage-report-layouts.md)  
[E-Mail einrichten](admin-how-setup-email.md)  
[Fakturieren eines Verkaufs](sales-how-invoice-sales.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
