---
title: Exchange-Daten | Microsoft Docs
description: "Sie können Daten zwischen Business Central und externen Dateien oder Streams in Bezug auf allgemeine Geschäftsaufgaben (z. B. Senden und Empfangen von elektronischen Belegen und Importieren und Exportieren von Bankdateien) austauschen."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 678b15b8d15dba477ac09c2651964525f4afe26a
ms.contentlocale: de-de
ms.lasthandoff: 11/22/2018

---
# <a name="exchanging-data"></a>Austausch von Daten
Sie können Daten zwischen [!INCLUDE[d365fin](includes/d365fin_md.md)] und externen Dateien oder Streams in Bezug auf allgemeine Geschäftsaufgaben (z. B. Senden und Empfangen von elektronischen Belegen und Importieren und Exportieren von Bankdateien) austauschen.  

Bevor Sie elektronische Belege senden und empfangen oder Bankdateien importieren und exportieren können, müssen Sie das Datenaustauschframework einrichten, um die entsprechenden Dateien oder Streams zu verarbeiten. Darüber hinaus müssen Sie zugehörige Bereiche einrichten. Dazu gehören Stammdaten für Debitoren, an die Sie elektronische Rechnungen senden, und der Bankdaten-Konvertierungsdienst, falls Sie Bankdateikonvertierungen an einen externen Dienstleister vergeben. Weitere Informationen finden Sie unter [Datenaustausch einrichten](across-set-up-data-exchange.md)  

 In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.  

|**Aufgabe**|**Informationen**|  
|------------|-------------|  
|Wandeln Sie Verkaufsbelege in [!INCLUDE[d365fin](includes/d365fin_md.md)] in ein standardisiertes Format um, und senden Sie sie als elektronische Belege, die Ihre Debitoren in ihrem System empfangen können.|[Elektronische Belege senden](sales-how-to-send-electronic-documents.md)|  
|Senden Sie PDF- oder Bilddateien an einen Anbieter von OCR-Dienstleistungen, um sie in Form von elektronischen Belegen zurückzuerhalten, die in [!INCLUDE[d365fin](includes/d365fin_md.md)] in Belegdatensätze konvertiert werden können.|[Verwenden von OCR, um PDF und Bilddateien in elektronische Belege umzuwandeln](across-how-use-ocr-pdf-images-files.md)|  
|Empfangen Sie elektronische Belege, entweder aus dem OCR-Dienst oder aus dem Beleg-Austauschdienst, in einem standardisierten Format, das sie in die relevanten Belegdatensätze in [!INCLUDE[d365fin](includes/d365fin_md.md)] konvertieren.|[Vorgehensweise: Elektronische Belege empfangen und konvertieren](purchasing-how-to-receive-and-convert-electronic-documents.md)|  
|Bereiten Sie das Importieren einer Bankauszugsdatei in das Fenster **Zahlungsabstimmungsbuch.-Blatt** als ersten Schritt zur Abstimmung von Zahlungen oder auf die Seite **Bankonto-Abstimmung** als ersten Schritt zur Abstimmung von Bankkonten vor|[Einrichten des Envestnet Yodlee Bank-Feed-Service](bank-how-setup-bank-statement-service.md)|  
|Exportierten Sie Zahlungen aus der Seite **Zahlung Buch.-Blatt** in eine Bankdatei, die Sie auf Ihr elektronisches Bankkonto zur Verarbeitung hochladen.|[Zahlungen in eine Bankdatei exportieren](payables-how-export-payments-bank-file.md)|
|Erstellen von elektronischen Zahlungen entsprechend dem Banküberweisungsstandard EU SEPA.|[Nehmen Sie Zahlungen mit dem Bank-Datenkonvertierungs-Service- oder einer SEPA-Banküberweisung vor](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|  
|Weisen Sie Ihre Bank an, Zahlungsbeträge von den Bankkonten Ihrer Kunden auf das Konto Ihres Unternehmens gemäß Ihrer SEPA-Lastschrift-Einstellung zu überweisen.|[SEPA-Lastschrifteinzugsposten erstellen und in eine Bankdatei exportieren](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)|  
|Verwenden Sie einen Dienstanbieter für Währungswechselkursen, um die Seite **Währungen** zu aktualisieren.|[Währungswechselkurse aktualisieren](finance-how-update-currencies.md)|  
|Zeigen Sie an, welche Dateielemente mit Feldern in [!INCLUDE[d365fin](includes/d365fin_md.md)] verknüpft sind, wenn Sie SEPA CAMT-Bankkontoauszugsdateien importieren.|[Feld-Zuordnung beim Importieren von SEPA CAMT-Dateien](across-field-mapping-when-importing-sepa-camt-files.md)|  
|Zeigen Sie an, welche Felder in [!INCLUDE[d365fin](includes/d365fin_md.md)] Dateielementen zugeordnet sind, wenn Sie Zahlungsdateien mithilfe der Bankdaten-Konvertierungsdienst-Funktion exportieren.|[Feld-Zuordnung beim Exportieren von Zahlungsdateien unter Verwendung von Bankdaten-Konvertierungsdienst](across-field-mapping-when-exporting-payment-files-using-bank-data-conversion-service.md)|  

## <a name="see-also"></a>Siehe auch  
[Einrichten eines Datenaustauschs](across-set-up-data-exchange.md)  
[Daten elektronisch austauschen](across-data-exchange.md)  
[Fakturieren eines Verkaufs](sales-how-invoice-sales.md)   
[Erfassen eines Einkaufs](purchasing-how-record-purchases.md)  
[Eingehende Belege](across-income-documents.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  

