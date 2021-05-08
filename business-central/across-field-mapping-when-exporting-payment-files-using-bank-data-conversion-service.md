---
title: Feldzuordnung für den Export von Bankzahlungsdateien | Microsoft Docs
description: Wenn Sie Zahlungsdateien mit der AMC Banking 365 Fundamentals-Erweiterung exportieren, werden die von Ihnen exportierten Daten dem Dienstanbieter zugänglich gemacht.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 52632b540c2795b0e46cbae12037aa2e1ee8c743
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776122"
---
# <a name="field-mapping-when-exporting-payment-files-using-the-amc-banking-365-fundamentals-extension"></a>Feldzuordnung beim Export von Zahlungsdateien mit der AMC Banking 365 Fundamentals-Erweiterung
Wenn Sie Zahlungsdateien mit der AMC Banking 365 Fundamentals-Erweiterung exportieren, werden die von Ihnen exportierten Daten dem Dienstanbieter zugänglich gemacht. Der Dienstanbieter ist für den Schutz dieser Daten verantwortlich. Weitere Informationen zur AMC Banking 365 Fundamentals-Erweiterung finden Sie unter [Verwenden der AMC Banking 365 Fundamentals-Erweiterung](ui-extensions-amc-banking.md).  

> [!CAUTION]  
>  Wenn Sie Zahlungsdateien mit der AMC Banking 365 Fundamentals-Erweiterung exportieren, werden einige Ihrer Geschäftsdaten dem Anbieter des Dienstes zugänglich gemacht. Der Dienstanbieter, AMC Consult A/S, ist für den Schutz dieser Daten verantwortlich. Weitere Informationen finden Sie unter [AMC-Datenschutzrichtlinie](https://go.microsoft.com/fwlink/?LinkId=510158).  

Die folgende Tabelle listet die Felder in [!INCLUDE[prod_short](includes/prod_short.md)] auf, aus denen Sie Daten exportieren können.  

|Zugeordnetes Feld|Feld in Tabelle|Tisch|Beschreibung|  
|------------------|--------------------|-----------|---------------------------------------|  
|Gläubiger-Identifikationsnummer|Gläubiger-Identifikationsnummer|Bankkonto|Die Identifikationsnummer, die Ihrem Unternehmen von Ihrer Bank zugeordnet wurde, um Zahlungen zu erfassen|  
|Bankkontonr. des Absenders|Bankkontonummer/IBAN|Bankkonto|Die Bankkontonummer (IBAN oder sonstige) Ihres Unternehmens, die auf der Bankkontokarte angegeben ist|  
|Absenderbank-Clearing-Standard|Bank-Clearing-Standard|Bankkonto|Das Nationale Register der Banknamen für das Bankkonto des Absenders|  
|Clearing-Code Absenderbank|Bank-Clearing-Code|Bankkonto|Die Identifikationsnummer Bank des Absenders in Bezug auf das Bankadressenregister, das verwendet wird|  
|BIC Absenderbank|SWIFT-Code|Bankkonto|Die SWIFT-Kennung des Absenderbankkontos.|  
|Kontowährung der Absenderbank|Währungscode|Bankkonto|Der Währungscode der Absenderbank|  
|Belegnr.|Belegnr.|Fibu Buch.-Blattzeile|Die Belegnummer der Zahlungszeile|  
|Ausgleich ext. Belegnr.|Ausgleich ext. Belegnr.|Fibu Buch.-Blattzeile|Die Nummer des externen Belegs, der Rechnung oder Gutschrift, mit der die Zahlungszeile ausgeglichen werden soll.|  
|Empfänger-ID|Kontonummer|Fibu Buch.-Blattzeile|Die Nummer des Debitors oder Kreditors, die auf der Zahlungszeile angegeben ist|  
|Zahlungsart|Zahlungstyp Bankdatenkonvertierung|Zahlungsform|Die Art des Banktransfers, wie Inland oder International|  
|Zahlungsreferenz|Zahlungsreferenz|Fibu Buch.-Blattzeile|Die Zahlungsreferenz der Zahlungszeile|  
|Adresse des Empfängers|Adresse|Debitor/Kreditor|Die Empfängeradresse, die auf der Debitoren- oder Kreditorenkarte angegeben ist|  
|Ort des Empfängers|Ort|Debitor/Kreditor|Die Stadt, die auf der Debitoren- oder Kreditorenkarte angegeben ist|  
|Name des Empfängers|Name|Debitor/Kreditor|Die Empfängername, der auf der Debitoren- oder Kreditorenkarte angegeben ist|  
|Landes-/Regionscode Empfänger|Länder-/Regionscode|Debitor/Kreditor|Der Länder-/Regionencode des Bankkontos des Empfängers, der auf der Debitoren- oder auf der Bankkontokarte angegeben ist|  
|PLZ-Code Empfänger|PLZ-Code|Debitor/Kreditor|Die Postleitzahl des Empfängers, die auf der Debitoren- oder auf der Bankkontokarte angegeben ist|  
|Bankkontonr. Empfänger|Bankkontonummer/IBAN|Debitorenbankkonto/Kreditorenbankkonto|Die Nummer (IBAN oder sonstige) des Bankkontos des Empfängers, die auf der Debitoren- oder auf der Bankkontokarte angegeben ist|  
|Clearing-Code Empfängerbank|Bank-Clearing-Standard|Debitorenbankkonto/Kreditorenbankkonto|Das Nationale Register der Banknamen für das Bankkonto des Empfängers|  
|Clearing-Standard Empfängerbank|Bank-Clearing-Code|Debitorenbankkonto/Kreditorenbankkonto|Die Identifikationsnummer des Empfänger-Bankkontos in Bezug auf das Bankadressenregister, das verwendet wird|  
|E-Mail-Adresse Empfänger|E-Mail|Debitor/Kreditor|Die E-Mail-Adresse des Empfängers.|  
|Nachricht an Empfänger 1|Nachricht an Empfänger|Fibu Buch.-Blattzeile|Die Meldung an den Empfänger, die in der Zahlungszeile angegeben ist|  
|Betrag|Betrag|Fibu Buch.-Blattzeile|Der Betrag auf der Zahlungszeile|  
|Währungscode|Währungscode|Fibu Buch.-Blattzeile|Der Währungscode auf der Zahlungszeile.|  
|Lastschriftdatum|Buchungsdatum|Fibu Buch.-Blattzeile|Das Buchungsdatum der Zahlungsposition.|  
|Rechnungsbetrag|Ursprungsbetrag|Debitoren-/Kreditorenposten|Der Betrag in dem Eintrag, auf den die Zahlung angewendet wird.|  
|Rechnungsdatum|Belegdatum|Debitoren-/Kreditorenposten|Der Rechnungsbetrag in dem Eintrag, auf den die Zahlung angewendet wird.|  
|Adresse Empfängerbank|Adresse|Debitorenbankkonto/Kreditorenbankkonto|Die Bankkontoadresse des Empfängers, die auf der Debitoren- oder auf der Bankkontokarte angegeben ist|  
|Die Bankkontoadresse des Empfängers, die auf der Debitoren- oder auf der Bankkontokarte angegeben ist|Ort|Debitorenbankkonto/Kreditorenbankkonto|Die Stadt des Bankkontos des Empfängers, die auf der Debitoren- oder auf der Bankkontokarte angegeben ist|  
|Name Empfängerbank|Name|Debitorenbankkonto/Kreditorenbankkonto|Der Name des Bankkontos des Empfängers, der auf der Debitoren- oder auf der Bankkontokarte angegeben ist|  
|Land/Region Empfängerbank|Länder-/Regionscode|Debitorenbankkonto/Kreditorenbankkonto|Das Land/Die Region des Bankkontos des Empfängers, das auf der Debitoren- oder auf der Bankkontokarte angegeben ist|  
|PLZ-Code Empfängerbank|PLZ-Code|Debitorenbankkonto/Kreditorenbankkonto|Die Postleitzahl des Bankkontos des Empfängers, die auf der Debitoren- oder auf der Bankkontokarte angegeben ist|  
|Adresse Absenderbank|Adresse|Bankkonto|Die Absenderbankkontoadresse, die auf der Bankkontokarte angegeben ist|  
|Ort Absenderbank|Ort|Bankkonto|Die Absenderbankkontostadt, die auf der Bankkontokarte angegeben ist|  
|Name der Absenderbank|Name|Bankkonto|Der Absenderbankkontoname, der auf der Bankkontokarte angegeben ist|  
|Land/Region Absenderbank|Länder-/Regionscode|Bankkonto|Das Land/Die Region des Absenderbankkontos, das/die auf der Bankkontokarte angegeben ist|  
|PLZ-Code Absenderbank|PLZ-Code|Bankkonto|Der Absenderbankkonto-PLZ-Code, der auf der Bankkontokarte angegeben ist|  
|Fibu Buch.-Blattvorlage|Buch.-Blattvorlagenname|Fibu Buch.-Blattzeile|Die Fibu Buch.-Blattvorlage, die für die Zahlungszeile verwendet wird|  
|Fibu Buch.-Blattname|Buch.-Blattname|Fibu Buch.-Blattzeile|Der Fibu Buch.-Blatt-Buch.-Blatt, das für die Zahlungszeile verwendet wird|  
|Name der Absenderbank – Datenkonvertierung|Bankname – Datenkonv.|Bankkonto|Der Name des Absenderbankkontos, der von der AMC Banking 365 Fundamentals-Erweiterung angefordert und auf der Bankkarte angegeben wird.|  

## <a name="see-also"></a>Siehe auch  
[Datenaustausch einrichten](across-set-up-data-exchange.md)  
[Daten elektronisch austauschen](across-data-exchange.md)
[Verwenden der AMC Banking 365 Fundamentals-Erweiterung](ui-extensions-amc-banking.md)   
[Zahlungen mit der AMC Banking 365 Fundamentals-Erweiterung oder per SEPA-Überweisung vornehmen](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]