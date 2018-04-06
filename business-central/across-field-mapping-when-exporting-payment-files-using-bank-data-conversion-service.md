---
title: "Feldzuordnung für den Export von Bankzahlungsdateien | Microsoft Docs"
description: "Wenn Sie Zahlungsdateien exportieren, indem Sie die Bankdaten-Konvertierungsdienst-Funktion verwenden, werden die Daten, die Sie exportieren, dem Anbieter des Bankdaten-Konvertierungsdienstes zur Verfügung gestellt."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/18/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 6f30a7c08db374b7f5571b8e48d4b91a2bb7ddc2
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="field-mapping-when-exporting-payment-files-using-bank-data-conversion-service"></a>Feld-Zuordnung beim Exportieren von Zahlungsdateien unter Verwendung von Bankdaten-Konvertierungsdienst
Wenn Sie Zahlungsdateien exportieren, indem Sie die Bankdaten-Konvertierungsdienst-Funktion verwenden, werden die Daten, die Sie exportieren, dem Anbieter des Bankdaten-Konvertierungsdienstes zur Verfügung gestellt. Der Dienstanbieter ist für den Schutz dieser Daten verantwortlich. Weitere Informationen darüber, wie die Bankdaten-Konvertierungsdienst-Funktion arbeitet, finden Sie unter [Datenaustausch-Framework](across-about-the-data-exchange-framework.md).  

> [!CAUTION]  
>  Wenn Sie Zahlungsdateien exportieren, indem Sie die Bankdaten-Konvertierungsdienst-Funktion verwenden, werden einige Ihrer Daten dem Anbieter des Services zur Verfügung gestellt. Der Dienstanbieter, AMC Consult A/S, ist für den Schutz dieser Daten verantwortlich. Weitere Informationen finden Sie unter [AMC-Datenschutzrichtlinie.](http://go.microsoft.com/fwlink/?LinkId=510158)  

In der folgenden Tabelle sind die Felder in [!INCLUDE[d365fin](includes/d365fin_md.md)] ausgefüllt, aus denen Daten zu dem Dienstanbieter exportiert werden können.  

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
|Name der Absenderbank – Datenkonvertierung|Bankname – Datenkonv.|Bankkonto|Der Absenderbankkontoname, der avom Bankdatenkonvertierungs-Service angefordert wird und auf der Bankkontokarte angegeben ist|  

## <a name="see-also"></a>Siehe auch  
[Einrichten eines Datenaustauschs](across-set-up-data-exchange.md)  
[Daten elektronisch austauschen](across-data-exchange.md)
[Richten Sie den Bankdaten-Konvertierungsdienst ein](bank-how-setup-bank-data-conversion-service.md)   
[Nehmen Sie Zahlungen mit dem Bank-Datenkonvertierungs-Service- oder einer SEPA-Banküberweisung vor](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)   

