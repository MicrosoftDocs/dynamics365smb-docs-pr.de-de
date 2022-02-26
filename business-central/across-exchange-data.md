---
title: Austausch von Daten
description: Tauschen Sie elektronische Belege, z.B. Bankdateien, zwischen Business Central und externen Parteien aus.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: exchange data, external files, electronic documents, AMC Banking, OCT, SEPA
ms.date: 06/10/2021
ms.author: edupont
ms.openlocfilehash: 85f8a69d05366585bd11d651a6c093a4388433d9
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "6319640"
---
# <a name="exchanging-data"></a>Austausch von Daten
Sie können Daten zwischen [!INCLUDE[prod_short](includes/prod_short.md)] und externen Dateien oder Streams in Bezug auf allgemeine Geschäftsaufgaben (z. B. Senden und Empfangen von elektronischen Belegen und Importieren und Exportieren von Bankdateien) austauschen.  

Bevor Sie elektronische Dokumente senden und empfangen oder Bankdateien importieren und exportieren können, müssen Sie das Datenaustausch-Framework für die Verarbeitung der Datendateien oder Streams einrichten. Darüber hinaus müssen Sie verwandte Bereiche einrichten, wie z. B. die Kunden, an die Sie elektronische Rechnungen senden, und die AMC Banking 365 Fundamentals-Erweiterung, wenn Sie Bankdateikonvertierungen an einen externen Dienstanbieter verteilen. Weitere Informationen finden Sie unter [Datenaustausch einrichten](across-set-up-data-exchange.md)  

 Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Themen, die sie beschreiben..  

|**Aufgabe**|**Informationen**|  
|------------|-------------|  
|Wandeln Sie Verkaufsbelege in [!INCLUDE[prod_short](includes/prod_short.md)] in ein standardisiertes Format um, und senden Sie sie als elektronische Belege, die Ihre Debitoren in ihrem System empfangen können.|[Elektronische Belege senden](sales-how-to-send-electronic-documents.md)|  
|Senden Sie PDF- oder Bilddateien an einen Anbieter von OCR-Dienstleistungen, um sie in Form von elektronischen Belegen zurückzuerhalten, die in [!INCLUDE[prod_short](includes/prod_short.md)] in Belegdatensätze konvertiert werden können.|[Verwenden von OCR, um PDF und Bilddateien in elektronische Belege umzuwandeln](across-how-use-ocr-pdf-images-files.md)|  
|Empfangen Sie elektronische Belege, entweder aus dem OCR-Dienst oder aus dem Beleg-Austauschdienst, in einem standardisierten Format, das sie in die relevanten Belegdatensätze in [!INCLUDE[prod_short](includes/prod_short.md)] konvertieren.|[Vorgehensweise: Elektronische Belege empfangen und konvertieren](purchasing-how-to-receive-and-convert-electronic-documents.md)|  
|Bereiten Sie das Importieren einer Bankauszugsdatei in das Fenster **Zahlungsabstimmungsbuch.-Blatt** als ersten Schritt zur Abstimmung von Zahlungen oder auf die Seite **Bankonto-Abstimmung** als ersten Schritt zur Abstimmung von Bankkonten vor|[Den Envestnet Yodlee Bank Feeds Service einrichten](bank-how-setup-bank-statement-service.md)|  
|Exportierten Sie Zahlungen aus der Seite **Zahlung Buch.-Blatt** in eine Bankdatei, die Sie auf Ihr elektronisches Bankkonto zur Verarbeitung hochladen.|[Zahlungen in eine Bankdatei exportieren](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)|
|Erstellen von elektronischen Zahlungen entsprechend dem Banküberweisungsstandard EU SEPA.|[Zahlungen mit der AMC Banking 365 Fundamentals-Erweiterung oder per SEPA-Überweisung vornehmen](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|  
|Weisen Sie Ihre Bank an, Zahlungsbeträge von den Bankkonten Ihrer Kunden auf das Konto Ihres Unternehmens gemäß Ihrer SEPA-Lastschrift-Einstellung zu überweisen.|[SEPA-Lastschrifteinzugsposten erstellen und in eine Bankdatei exportieren](finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file)|  
|Verwenden Sie einen Dienstanbieter für Währungswechselkursen, um die Seite **Währungen** zu aktualisieren.|[Währungswechselkurse aktualisieren](finance-how-update-currencies.md)|  
|Zeigen Sie an, welche Dateielemente mit Feldern in [!INCLUDE[prod_short](includes/prod_short.md)] verknüpft sind, wenn Sie SEPA CAMT-Bankkontoauszugsdateien importieren.|[Feld-Zuordnung beim Importieren von SEPA CAMT-Dateien](across-field-mapping-when-importing-sepa-camt-files.md)|  
|Zeigen Sie an, welche Felder in [!INCLUDE[prod_short](includes/prod_short.md)] beim Export von Zahlungsdateien mit der AMC Banking 365 Fundamentals-Erweiterung auf Dateielemente abgebildet werden.|[Feldzuordnung beim Export von Zahlungsdateien mit der AMC Banking 365 Fundamentals-Erweiterung](across-field-mapping-when-exporting-payment-files-using-bank-data-conversion-service.md)|  

## <a name="see-also"></a>Siehe auch  
[Datenaustausch einrichten](across-set-up-data-exchange.md)  
[Daten elektronisch austauschen](across-data-exchange.md)  
[Fakturieren eines Verkaufs](sales-how-invoice-sales.md)   
[Erfassen eines Einkaufs](purchasing-how-record-purchases.md)  
[Eingehende Belege](across-income-documents.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]