---
title: Feld-Zuordnung beim Importieren von SEPA CAMT-Dateien | Microsoft Docs
description: "In den europäischen Märkten können Sie Bankkontoauszugsdateien in den regionalen SEPA-Standards  (einzelner Eurozahlungs-Bereich) importieren."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/18/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 95d4104be55bcaf77dffd47e1bec0afcbe95a1da
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="field-mapping-when-importing-sepa-camt-files"></a>Feld-Zuordnung beim Importieren von SEPA CAMT-Dateien
[!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt den regionalen SEPA-Standard (Single Euro Payments Area) für das Importieren von SEPA-Bankkontoauszügen (CAMT-Format). Für weitere Informationen, siehe [Gewusst wie: Einrichten des Bankdatenkonvertierungsservice](bank-how-setup-bank-data-conversion-service.md).  

 Der SEPA CAMT-Standard selbst verfügt über lokale Variationen. Daher müssen Sie möglicherweise die generische Datenaustauschdefinition ändern (angezeigt durch den **SEPA CAMT-Code** im Fenster **Exchange-Definitionen** ändern, um ihn einer lokalen Variation des Standards anzupassen. Die folgenden Tabellen zeigen die Element-zu-Feld-Zuordnung für die Tabellen 81, 273 und 274 in der SEPA CAMT-Implementierung in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

 Informationen zum Erstellen oder die Stapelverarbeitung eine Datenaustauschdefinition, siehe [Vorgehensweise: Einrichtungsdaten-Exchange-Definitionen](across-how-to-set-up-data-exchange-definitions.md).  

## <a name="camt-data-mapping-to-fields-in-the-general-journal-table-81"></a>CAMT-Datenzuordnung zu den Feldern in der Fibu Buch.-Blatt-Tabelle (81)  

|Element-Pfad|Meldungs-Element|Datentyp|Beschreibung|Kennzeichen mit negativem Zeichen|Feldnr.|Feldname|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/Ntry/Amt|Betrag|Dezimal|Der Geldbetrag im Bargeldposten||13|Betrag|  
|Stmt/Ntry/CdtDbtInd|CreditDebitIndicator|Text|Gibt an, ob der Posten ein Habenbetrag oder ein Sollposten ist|DBIT|13|Betrag|  
|Stmt/Ntry/BookgDt/Dt|Datum|Datum|Das Datum der Buchung eines Postens auf einem Konto oder in den Büchern des Buchhaltungsservices.||5|Buchungsdatum|  
|Stmt/Ntry/BookgDt/DtTm|DateTime|DateTime|Das Datum und die Uhrzeit der Buchung eines Postens auf einem Konto oder in den Büchern des Buchhaltungsservices.||5|Buchungsdatum|  
|Stmt/Ntry/NtryDtls/TxDtls/RltdPties/Dbtr/Nm|Name|Text|Der Name der Partei, die einen Geldbetrag an das (wesentlichen) schuldet können||1221|Informationen Zahlender|  
|Stmt/Ntry/NtryDtls/TxDtls/RmtInf/Ustrd|Unstrukturiert|Text|Informationen, die angegeben werden, um Abgleichen/Abstimmung eines Postens mit den Artikeln zu aktivieren, die die Zahlung abgleichen soll, wie etwa Handelsrechnungen in einem Debitorensystem, in unstrukturierter Form.||8|Beschreibung|  
|Stmt/Ntry/AddtlNtryInf|ZusätzlicheEingabeInformationen|Text|Zusätzliche Informationen zu der Eingabe||1222|Transaktionsinformationen|  

## <a name="camt-data-mapping-to-fields-in-the-bank-acc-reconciliation-table-273"></a>CAMT-Datenzuordnung zu den Feldern in der Bankkonto-Abstimmungstabelle (273)  

|Element-Pfad|Meldungs-Element|Datentyp|Beschreibung|Kennzeichen mit negativem Zeichen|Feldnr.|Feldname|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/CreDtTm|CreationDateTime|Datum|Das Datum und die Uhrzeit der Erstellung der Nachricht.||3|Auszugsdatum|  
|Stmt/Bal/Amt|Betrag|Dezimal|Der Betrag, der aus den Nettobeträgen für alle Soll- und Habenposten resultiert||4|Auszug Schluss-Saldo|  

## <a name="camt-data-mapping-to-fields-in-the-bank-acc-reconciliation-line-table-274"></a>CAMT-Datenzuordnung zu den Feldern in der Bankkonto-Abstimmungszeilentabelle (274)  

|Element-Pfad|Meldungs-Element|Datentyp|Beschreibung|Kennzeichen mit negativem Zeichen|Feldnr.|Feldname|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/Ntry/Amt|Betrag|Dezimal|Der Geldbetrag im Bargeldposten||7|Auszugsbetrag|  
|Stmt/Ntry/CdtDbtInd|CreditDebitIndicator|Text|Gibt an, ob der Posten ein Habenbetrag oder ein Sollposten ist|DBIT|7|Auszugsbetrag|  
|Stmt/Ntry/BookgDt/Dt|Datum|Datum|Das Datum der Buchung eines Postens auf einem Konto oder in den Büchern des Buchhaltungsservices.||5|Transaktionsdatum|  
|Stmt/Ntry/BookgDt/DtTm|DateTime|DateTime|Das Datum und die Uhrzeit der Buchung eines Postens auf einem Konto oder in den Büchern des Buchhaltungsservices.||5|Transaktionsdatum|  
|Stmt/Ntry/ValDt/Dt|Datum|Datum|Das Datum, an dem Anlagen für den Kontobesitzer im Falle eines Habenpostens verfügbar sind oder oder im Falle eines Sollpostens nicht mehr verfügbar sind.||12|Valutadatum|  
|Stmt/Ntry/ValDt/DtTm|DateTime|DateTime|Das Datum und die Uhrzeit, wenn Anlagen für den Kontobesitzer im Falle eines Habenpostens verfügbar sind oder oder im Falle eines Sollpostens nicht mehr verfügbar sind.||12|Valutadatum|  
|Stmt/Ntry/NtryDtls/TxDtls/RltdPties/Dbtr/Nm|Name|Text|Der Name der Partei, die einen Geldbetrag an das (wesentlichen) schuldet können||15|Informationen Zahlender|  
|Stmt/Ntry/NtryDtls/TxDtls/RmtInf/Ustrd|Unstrukturiert|Text|Informationen, die angegeben werden, um Abgleichen/Abstimmung eines Postens mit den Artikeln zu aktivieren, die die Zahlung abgleichen soll, wie etwa Handelsrechnungen in einem Debitorensystem, in unstrukturierter Form.||6|Beschreibung|  
|Stmt/Ntry/AddtlNtryInf|ZusätzlicheEingabeInformationen|Text|Zusätzliche Informationen zu der Eingabe||16|Transaktionsinformationen|  

 Elemente im **Ntry**-Knoten, die in [!INCLUDE[d365fin](includes/d365fin_md.md)] importiert, aber nicht mit einem Feld verknüpft werden, werden in der **Exch.Spaltendefinition buchen**-Tabelle gespeichert. Benutzer können diese Elemente **Zahlungsabstimmungsbuch.-Blatt**, **Zahlungsausgleich** und **Bankkonto Abstimmen** Fenstern anzeigen, indem sie die **Details zur Bankauszugsposition** Aktion auswählen. Weitere Informationen finden Sie unter [So gehts: Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-auto-application.md).  
## <a name="see-also"></a>Siehe auch  
[Einrichten eines Datenaustauschs](across-set-up-data-exchange.md)  
[Datenaustausch als Elektronische Dokumente ](across-data-exchange.md)  
[Gewusst wie: Einrichten des Bankdatenkonvertierungsservice](bank-how-setup-bank-data-conversion-service.md)   
[Gewusst wie: Verwenden von XML-Schemata zur Vorbereitung von Datenaustauschdefinitionen](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Vorgehensweise: Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-auto-application.md)  

