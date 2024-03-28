---
title: Arbeiten mit Eingehenden Belegen
description: 'Sie können eingehende externe Unternehmensbelege, wie Zahlungseingänge oder PDF-Dateien verwalten, OCR-Aufgaben verwalten und Dateien in elektronische Belege und Datensätze umwandeln.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Eingehende Belege

Externe Geschäftsdokumente können als E-Mail-Anhang oder als Papierkopie, die Sie zur Ablage einscannen, in Ihre Firma kommen. Dieses Szenario ist typisch für Einkäufe, bei denen solche eingehenden Dokumentdateien Zahlungsbelege für Ausgaben oder kleine Einkäufe darstellen.

Auf der Seite **Eingehende Belege** können Sie verschiedene Funktionen zum Überprüfen von Ausgabenbelegen, Verwalten von OCR-Aufgaben und Konvertieren eingehender Belege, manuell oder automatisch, in den entsprechenden Belegen oder Buch.-Blattzeilen verwenden. Die externen Dateien können jeder Prozessphase zugeordnet werden, auch gebuchten Belegen und den resultierenden Kreditoren-, Debitoren- und Sachposten.

## Anwendungsszenario

Sie können Dateien oder Papierkopien, die Sie von Ihren Handelspartnern erhalten haben, in [!INCLUDE[prod_short](includes/prod_short.md)] registrieren und einen Datensatz für ein Dokument erstellen. Zum Beispiel eine Einkaufs- oder Verkaufsrechnung, eine Gutschrift oder eine Buchungsblattzeile.

Laden Sie die empfangenen Dateien hoch – oder verwenden Sie die Kamera des Geräts, um ein Foto zu machen – und erstellen Sie Einträge, um die externen Dokumente darzustellen. Optional können Sie mit PDF- oder Bilddateien von einem externen OCR-Dienst (Optical Character Recognition) elektronische Belege generieren lassen, die dann in Datensätze in [!INCLUDE[prod_short](includes/prod_short.md)] umgewandelt werden können.

> [!NOTE]
> Die OCR Funktion wird von externen Anbietern bereitgestellt. Wählen Sie ein Servicepaket, das für Ihre Organisation und/oder Ihr Land/Ihre Region geeignet ist. Dienste, die mit [!INCLUDE[prod_short](includes/prod_short.md)] kompatibel sind, und Details zu den verfügbaren Funktionen finden Sie unter [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).

Wenn Sie beispielsweise eine Rechnung in PDF-Format von Ihrem Kreditor erhalten, können Sie diese über die Seiter **Eingehende Belege** zum OCR-Dienst senden. Alternativ bieten einige OCR-Anbieter die Möglichkeit, Dateien zu verarbeiten, die an eine spezielle E-Mail-Adresse weitergeleitet werden, die dann automatisch einen entsprechenden Datensatz für eingehende Dokumente erstellt. Nach einigen Sekunden erhalten Sie die Datei vom OCR-Dienst als elektronische Rechnung zurück, die zu einer Einkaufsrechnung für den Kreditor umgewandelt werden kann.

> [!TIP]
> Erstellen Sie Datensätze für eingehende Dokumente in [!INCLUDE[prod_short](includes/prod_short.md)] direkt aus den von den Lieferanten gesendeten E-Mails mit Hilfe des Outlook Add-Ins. Weitere Informationen finden Sie unter [Benutzen Sie Business Central als Ihren Posteingang in Outlook](work-outlook-addin.md).

## Funktionen für Eingehende Belege

Die Verarbeitung von eingehenden Belegen kann aus den folgenden Hauptaktivitäten bestehen:

* Erfassen Sie die externen Belege in Project '[!INCLUDE[prod_short](includes/prod_short.md)]', indem Sie mithilfe einer der folgenden Methoden Zeilen auf der Seite **Eingehende Belege** anlegen:
  * Manuell, entweder von einem PC oder von einem mobilen Gerät aus, auf eine der folgenden Arten:
    * Verwenden Sie die Schaltfläche **Aus Datei erstellen**, laden Sie eine Datei hoch und füllen Sie dann die entsprechenden Felder auf der Seite **Eingehendes Dokument** aus.
    * Verwenden Sie die Schaltfläche **Neu**, füllen Sie die entsprechenden Felder auf der Seite **Eingehendes Dokument** aus und hängen Sie die entsprechende Datei manuell an.
    * Verwenden Sie von einem Tablet oder Telefon aus die Schaltfläche **Von Kamera erstellen**, um einen neuen Datensatz für eingehende Dokumente mit der integrierten Kamera des Geräts zu erstellen.
  * Automatisch, indem Sie das Dokument vom OCR-Dienst als elektronischen Beleg erhalten, nachdem Sie die zugehörige PDF- oder Bilddatei hochgeladen oder per E-Mail an einen OCR-Dienst gesendet haben. Das Inforegister **Finanzinformationen** wird automatisch auf der Seite **Eingehender Beleg** ausgefüllt.
* Verwenden Sie einen externen OCR-Dienst, um PDF- oder Bilddateien in elektronische Belege umzuwandeln, die in Datensätze in [!INCLUDE[prod_short](includes/prod_short.md)] umgewandelt werden können.
* Erstellen Sie neue Belege oder eine Fibu Buch.-Blattzeilen aus einem eingehenden Belegdatensatz, indem sie die Informationen so eingeben, wie sie in den eingehenden Belegen stehen.
* Fügen Sie eingehender Belege zu Einkaufs- und Verkaufsbelegen jeden möglichen Status hinzu, einschließlich der resultierenden Kreditor, Debitor- und Sachposten, die aus dem Buchen resultieren.
* Zeigen Sie eingehende Belege und deren Anhänge aus Einkaufs- und Verkaufsbelegen oder Posten an, oder finden Sie alle Sachposten ohne eingehende Belege auf der Seite **Kontenplan**.

> [!NOTE]
> Dateien, die an Karten und Dokumente auf der Registerkarte **Anhänge** angehängt sind, werden auf der Seite **Eingehende Belege** nicht berücksichtigt. Weitere Informationen finden Sie unter [Verwalten von Anhängen, Links und Notizen zu Karten und Dokumenten](ui-how-add-link-to-record.md).

| Bis | Siehe |
| --- | --- |
| Legen Sie die Funktion **Eingehende Belege** fest und richten Sie den OCR-Dienst ein. |[Einrichten von eingehenden Belegen](across-how-setup-income-documents.md) |
| Erstellen Sie eingehende Belege manuell oder automatisch, indem Sie zum Beispiel ein Foto eines Papierbelegs erstellen. |[Erstellen von eingehenden Belegen](across-how-create-income-document-records.md) |
| Verwenden Sie einen OCR-Dienst, um PDF und Bilddateien zu elektronische Belege umzuwandeln, die beispielsweise zu Einkaufsrechnungen im [!INCLUDE[prod_short](includes/prod_short.md)] konvertiert werden können. Schulen Sie den OCR-Dienst, Fehler zu vermeiden,wenn er das nächste Mal ähnliche Daten verarbeitet. |[Verwenden von OCR, um PDF und Bilddateien in elektronische Belege umzuwandeln](across-how-use-ocr-pdf-images-files.md) |
| Verbinden oder entfernen Sie einen eingehenden Beleg mit einem beliebigem nicht gebuchten Verkaufs- oder Einkaufsbeleg, sowie mit jedem Debitor-, Kreditor- oder Sachposten in dem Beleg oder Posten. |[Erstellen und Verknüpfen von eingehenden Belegen aus Dokumenten und Posten](across-how-connect-disconnect-income-document-records.md) |
| Auf den Seiten **Kontenplan** und **Hauptbucheinträge** können Sie mit Hilfe einer Suchfunktion Hauptbuchhaltungsposten für gebuchte Belege suchen, für die es keine Datensätze für eingehende Belege gibt, und diese dann zentral mit bestehenden Datensätzen verknüpfen oder neue Datensätze mit angehängten Belegdateien erstellen. |[So finden Sie gebuchte Belege ohne zugehörige eingehende Belege](across-how-find-posted-documents-without-income-document-records.md) |
| Verschaffen Sie sich einen besseren Überblick, indem Sie die Datensätze für eingehende Dokumente auf *Verarbeitet* festlegen und aus der Standardansicht entfernen. |[Mehrere eingehende Belegdatensätze verwalten](across-how-manage-many-income-document-records.md) |

## Siehe auch

[Einkauf](purchasing-manage-purchasing.md)  
[Bearbeiten von geposteten Dokumenten](across-edit-posted-document.md)  
[Daten elektronisch austauschen](across-data-exchange.md)  
[Business Central und OneDrive für Business Integration](across-onedrive-overview.md)  
[Benutzen Sie Business Central als Posteingang in Outlook](work-outlook-addin.md)  
[Dokumente und E-Mails versenden](ui-how-send-documents-email.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
