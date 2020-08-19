---
title: 'Gewusst wie: Einrichten des Senden und Empfangen von elektronischen Bele | Microsoft Docsgen'
description: Als Alternative zu E-Mail-Dateianhängen können Sie Geschäftsbelegen elektronisch versenden und empfangen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/21/2020
ms.author: sgroespe
ms.openlocfilehash: ed2af108abd0ef23dac82b7e798a58bc8c494f89
ms.sourcegitcommit: bdb6d18d512aa76d8d4f477d73ccfb284b0047fc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/21/2020
ms.locfileid: "3611559"
---
# <a name="set-up-electronic-document-sending-and-receiving"></a>Einrichten des Senden und Empfangen von elektronischen Belegen

Als Alternative zu E-Mail-Dateianhängen können Sie Geschäftsbelegen elektronisch versenden und empfangen. Ein elektronischer Beleg ist eine normgerechte \-, die ein Geschäftsdokument darstellt (zum Beispiel eine Rechnung von einem Kreditor), die empfangen und in [!INCLUDE[d365fin](includes/d365fin_md.md)] in eine Einkaufsrechnung konvertieren kann. Der Austausch von elektronischen Belegen zwischen zwei Handelspartnern erfolgt über einen externen Anbieter eines Belegaustauschdiensts. Die allgemeine Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt das Senden und Empfangen von elektronischen Rechnungen und Gutschriften im PEPPOL-Format, das von den größten Anbietern von Belegaustauschdiensten unterstützt wird. Ein wichtiger Anbieter eines Belegaustauschdienstes ist vorkonfiguriert und kann für Ihren Mandanten eingerichtet werden.  

Mithilfe eines externen OCR-Dienstes (optische Zeichenerkennung) können Sie aus PDF- oder Bilddateien, die die eingehenden Belege darstellen, elektronische Belege erstellen, die Sie dann in [!INCLUDE[d365fin](includes/d365fin_md.md)] in Belegdatensätze konvertieren können, wie Sie es für elektronische PEPPOL-Belege tun. Wenn Sie beispielsweise eine Rechnung in PDF-Format von Ihrem Kreditor erhalten, können Sie diese über die Seiter **Eingehende Belege** zum OCR-Dienst senden. Nach einigen Sekunden erhalten Sie die Datei als elektronische Rechnung zurück, die zu einer Einkaufsrechnung für den Kreditor umgewandelt werden kann. Wenn Sie die Datei per E-Mail an den OCR-Service senden, wird automatisch ein neuer Datensatz für einen eingehenden Beleg erstellt, wenn Sie den elektronischen Belegs zurückerhalten.  

Das elektronische Belegformat **PEPPOL** ist vorkonfiguriert, sodass Sie elektronische Rechnungen und Gutschriften im PEPPOL-Format senden können. Zuerst müssen Sie verschiedene Stammdaten einrichten, zum Beispiel Mandantendaten, Debitoren, Artikel und Maßeinheiten. Diese werden verwendet, um Geschäftspartner und Artikel zu identifizieren, wenn Daten in Feldern in [!INCLUDE[d365fin](includes/d365fin_md.md)] in Elemente in der ausgehenden Dokumentdatei konvertiert werden. Abschließend müssen Sie auf der Seite **Elektronisches Dokumentenformat** das Format für jeden Debitor auswählen, an den Sie elektronische PEPPOL-Belege senden. Weitere Informationen finden Sie unter [Senden von elektronischen Dokumenten](sales-how-to-send-electronic-documents.md).  

Die Datenaustauschdefinition **PEPPOL - Rechnung** und **PEPPOL – Gutschrift** sind vorkonfiguriert, sodass Sie elektronische Rechnungen und Gutschriften im PEPPOL-Format empfangen können. Zuerst müssen Sie verschiedene Stammdaten einrichten, zum Beispiel Mandantendaten, Kreditoren, Artikel und Maßeinheiten. Diese werden verwendet, um Geschäftspartner und Artikel zu identifizieren, wenn Daten in Elementen im eingehenden Beleg zu Feldern in [!INCLUDE[d365fin](includes/d365fin_md.md)] konvertiert werden. Abschließend müssen Sie auf der Seite **Eingehende Belege** die Datenaustauschdefinition für jeden eingehenden elektronischen Beleg auswählen, der in einen Einkaufsbeleg in [!INCLUDE[d365fin](includes/d365fin_md.md)] umgewandelt werden soll.  

Die **OCR - Rechnung**-Datenaustauschdefinition ist vorkonfiguriert. Sie ermöglicht Ihnen dem Empfang von um elektronischen Belege die vom OCR-Service generiert werden. Um zum Beispiel eine Rechnung als elektronischen OCR-Beleg zu empfangen, richten Sie das Masterdatum ein und verarbeitet den Beleg dann so wie einen elektronischen PEPPOL-Beleg. Weitere Informationen finden Sie unter [Verwenden von OCR, um PDF und Bilddateien in elektronische Belege umzuwandeln](across-how-use-ocr-pdf-images-files.md).  

Die vorkonfigurierten Services für den Belegaustausch und für OCR müssen vor dem Senden und Empfangen aktiviert werden. Weitere Informationen finden Sie unter [Belegaustausch-Dienst](across-how-to-set-up-a-document-exchange-service.md).  

In diesem Thema werden die folgenden Prozeduren beschrieben:  

* Einrichten des Mandanten zum Senden und Empfangen von elektronischen Belegen  
* Einrichten der MwSt.-Buchung zum Senden und Empfangen von elektronischen Belegen  
* Einrichten von Ländern/Regionen zum Senden und Empfangen von elektronischen Belegen  
* Einrichten von Artikeln zum Senden und Empfangen von elektronischen Belegen  
* Einrichten von Maßeinheiten zum Senden und Empfangen von elektronischen Belegen  
* Einrichten von Debitoren zum Senden von elektronischen Belegen  
* Auswählen des elektronischen Belegformats **PEPPOL** zum Senden von elektronischen Belegen  
* Einrichten von Kreditoren für den Empfang von elektronischen Belegen  
* Auswählen der Datenaustauschdefinition **PEPPOL - Rechnung** für den Empfang von elektronischen Belegen  
* Einrichten des Sachkontos zur Verwendung bei neuen Einkaufsrechnungszeilen für nicht \-identifizierbare Artikel und Nicht\-Artikel  

### <a name="to-set-up-the-company-for-electronic-document-sending-and-receiving"></a>Einrichten des Mandanten zum Senden und Empfangen von elektronischen Belegen

1. Geben Sie im Feld **Suchen** **Firmendaten** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Füllen Sie im Inforegister **Allgemein** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Identifizieren Sie Ihren Mandanten.<br /><br /> Wenn Sie beispielsweise elektronische Rechnungen im PEPPOL-Format senden, wird der Wert in diesem Feld verwendet, um das **EndPointID**-Element unter dem **AccountingSupplierParty**-Knoten zu füllen. Die Nummer basiert auf dem GS1-Standard, der mit ISO 6523 konform ist.|  
    |**USt-ID**|Geben Sie die USt-IdNr. Ihres Unternehmens an.|  
    |**Zuständigkeitseinheitencode**|Wenn Ihr Unternehmen mit einer Zuständigkeitseinheit eingerichtet ist, dann stellen Sie sicher, dass das Feld **Land-/Regionencode** ausgefüllt ist.|  

### <a name="to-set-up-vat-posting-for-electronic-document-sending-and-receiving"></a>Einrichten der MwSt.-Buchung zum Senden und Empfangen von elektronischen Belegen

1. Geben Sie im Feld **Suchen** einen Wert für **MwSt.-Buchungsmatrix Einr.**, und wählen Sie dann den zugehörigen Link aus.  
2. Für jede MwSt.-Buchungsmatrixzeile, die Sie für elektronische Belege verwenden, müssen Sie das Feld wie in der folgenden Tabelle beschrieben ausfüllen.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Steuerkategorie**|Geben Sie die MwSt.-Kategorie an.<br /><br /> Wenn Sie beispielsweise elektronische Rechnungen im PEPPOL-Format senden, wird der Wert in diesem Feld verwendet, um das **TaxApplied**-Element unter dem **AccountingSupplierParty**-Knoten zu füllen. Die Nummer basiert auf dem UNCL5305-Standard.|  

### <a name="to-set-up-countriesregions-for-electronic-document-sending-and-receiving"></a>Einrichten von Ländern/Regionen zum Senden und Empfangen von elektronischen Belegen

1. Geben Sie im Feld **Suchen** die Option **Länder/Regionen** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Für alle Länder/Regionen, mit denen Sie elektronische Belege austauschen, müssen Sie das Feld wie in der folgenden Tabelle beschrieben ausfüllen.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**MwSt.-Schema**|Identifizieren Sie die nationale Behörde, die die MwSt-IdNr. für die Länder\/Regionen ausgibt, an die elektronische Beleg gesendet werden.<br /><br /> Wenn Sie beispielsweise elektronische Rechnungen im PEPPOL-Format senden, wird der Wert in diesem Feld verwendet, um das **SchemeID**-Attribut für das **EndPointID**-Element unter den Knoten **AccountingSupplierParty** und **AccountingCustomerParty** in der Datei zu füllen.<br /><br /> Das Feld **MwSt-Schema** wird nur verwendet, wenn das Feld **GLN** auf der Seite **Unternehmen** nicht ausgefüllt ist. **Hinweis:** Der Wert im Feld **Code** auf der Seite **Länder\/Regionen** muss dem Standard ISO 3166\-1:Alpha2 entsprechen.|  

### <a name="to-set-up-items-for-electronic-document-sending-and-receiving"></a>Einrichten von Artikeln zum Senden und Empfangen von elektronischen Belegen

1. Geben Sie im Feld **Suchen** **Artikel** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Für jeden Artikel, den Sie unter Verwendung von elektronischen Belegen kaufen oder verkaufen, müssen Sie das Feld wie in der folgenden Tabelle beschrieben ausfüllen.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**GTIN**|Identifiziert das Element in Verbindung mit dem elektronischen Senden und Empfangen von Dokumenten. Für das PEPPOL-Format wird das Feld wie folgt verwendet:<br /><br /> Wenn für das Element **StandardItemIdentification\/ID** das Attribut **SchemeID** auf den Wert **GTIN** festgelegt ist, wird das Element dem Feld **GTIN** auf der Artikelkarte zugeordnet.|  

### <a name="to-set-up-units-of-measure-for-electronic-document-sending-and-receiving"></a>Einrichten von Maßeinheiten zum Senden und Empfangen von elektronischen Belegen

1. Geben Sie im Feld **Suchen** die Option **Einheiten** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Für jede Maßeinheit, die Sie für Artikel auf elektronischen Belegen verwenden, müssen Sie das Feld wie in der folgenden Tabelle beschrieben ausfüllen.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Internationaler Standardcode**|Geben Sie den Einheitencode an, der gemäß dem Standard UNECERec20 in Verbindung mit dem Senden von elektronischen Belegen verwendet wird.<br /><br /> Wenn Sie beispielsweise elektronische Rechnungen im PEPPOL-Format senden, wird der Wert in diesem Feld verwendet, um das **unitCode**-Attribut für das **InvoicedQuantity**-Element unter dem **InvoiceLine**-Knoten zu füllen. **Hinweis:** Wenn das Feld **Maßeinheit** in der Verkaufszeile leer ist, wird der UNECERe20-Standardwert für „Stück“ \(H87\) standardmäßig eingefügt. Weitere Informationen und eine Liste von gültigen Maßeinheitscodes finden Sie unter [Empfehlungen Nr. 20\-Verwendete Maßeinheiten im internationalen Handel](https://www.unece.org/fileadmin/DAM/cefact/recommendations/rec20/rec20_rev3_Annex2e.pdf).|  

### <a name="to-set-up-customers-for-electronic-document-sending"></a>Einrichten von Debitoren zum Senden von elektronischen Belegen

1. Geben Sie im Feld **Suchen** **Debitoren** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Für jeden Debitor, an den Sie elektronische Belege senden, müssen Sie die Felder in der folgenden Tabelle ausfüllen.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Identifizieren Sie den Debitor.<br /><br /> Wenn Sie beispielsweise elektronische Rechnungen im PEPPOL-Format senden, wird der Wert in diesem Feld verwendet, um das **EndPointID**-Element unter dem **AccountingCustomerParty**-Knoten zu füllen. Die Nummer basiert auf dem GS1-Standard, der mit ISO 6523 konform ist.<br /><br /> Wenn das Feld **GLN**leer ist, wird der Wert im **MwSt Registrationsnr.**-Feld verwendet.|  
    |**USt-ID**|Geben Sie die Umsatzsteuer-Identifikationsnummer des Debitors an. **Hinweis:** Wählen Sie in unterstützten lokalisierten Versionen die DrillDown-Schaltfläche aus, um den Webdienst zu verwenden, der prüft, ob die Nummer im nationalen Handelsregister vorhanden ist.|  
    |**Zuständigkeitseinheitencode**|Wenn Ihr Unternehmen mit einer Zuständigkeitseinheit eingerichtet ist, dann stellen Sie sicher, dass das Feld **Land-/Regionencode** ausgefüllt ist.|  

    Sie können für jeden Debitor eine bevorzugte Methode der Übermittlung von Geschäftsbelegen einrichten, sodass Sie nicht jedes Mal eine Sendeoption auswählen müssen, wenn Sie einen Beleg an den Debitor senden. Weitere Informationen finden Sie unter [Einrichten von Sendeprofilen](sales-how-setup-document-send-profiles.md).  

### <a name="to-select-the-peppol-electronic-document-format-for-electronic-document-sending"></a>Auswählen des elektronischen Belegformats PEPPOL zum Senden von elektronischen Belegen  
1. Geben Sie im Feld **Suchen** den Text **Belegsendeprofile** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Öffnen Sie ein vorhandenes Sendeprofil für Belege, oder erstellen Sie ein neues. Weitere Informationen finden Sie unter [Einrichten von Sendeprofilen](sales-how-setup-document-send-profiles.md).  
3. Die Seite **Belegsendeprofil** kann jetzt im **Elektronisches Format**-Feld in der Zeile für PEPPOL ausgewählt werden. Wählen Sie dann die Schaltfläche **OK**.  
4. Wählen Sie im Feld **Elektronisches Do,ument** die Option **Ja (über Belegaustauschdienst)** aus.  

    > [!NOTE]  
    >  [!INCLUDE[d365fin](includes/d365fin_md.md)] erkennt automatisch, ob es sich bei dem Beleg um eine Rechnung oder eine Gutschrift handelt, und passt das PEPPOL-Format entsprechend an.  

5. Damit dieses Belegsendeprofil auf alle Debitoren angewendet wird, aktivieren Sie das Kontrollkästchen **Standard** im Inforegister **Allgemein**. Damit das Profil nur für bestimmte Debitoren gilt, füllen Sie das Feld **Belegsendeprofil** auf den jeweiligen Debitorenkarten aus. Weitere Informationen finden Sie unter [Einrichten von Sendeprofilen](sales-how-setup-document-send-profiles.md).  

    Nun können Sie den elektronischen Beleg mit den konvertierten Daten senden. Weitere Informationen finden Sie unter [Senden von elektronischen Dokumenten](sales-how-to-send-electronic-documents.md).  

### <a name="to-set-up-vendors-for-electronic-document-receiving"></a>Einrichten von Kreditoren für den Empfang von elektronischen Belegen  
1. Geben Sie im Feld **Suchen** **Kreditoren** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Für jeden Kreditor, von dem Sie elektronische Belege empfangen, müssen Sie die Felder wie in der folgenden Tabelle beschrieben ausfüllen.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Identifizieren Sie den Kreditor.<br /><br /> Wenn Sie beispielsweise elektronische Rechnungen im PEPPOL-Format emfpangen, wird der Wert in diesem Feld verwendet, um das **EndPointID**-Element unter dem **AccountingSupplierParty**-Knoten zu füllen. Die Nummer basiert auf dem GS1-Standard, der mit ISO 6523 konform ist.<br /><br /> Wenn das Feld **GLN**leer ist, wird der Wert im **MwSt Registrationsnr.**-Feld verwendet.|  
    |**USt-ID**|Geben Sie die Umsatzsteuer-Identifikationsnummer des Kreditors an. **Hinweis:** Wählen Sie in unterstützten lokalisierten Versionen die DrillDown-Schaltfläche aus, um den Webdienst zu verwenden, der prüft, ob die Nummer im nationalen Handelsregister vorhanden ist.|  
    |**Zuständigkeitseinheitencode**|Wenn Ihr Unternehmen mit einer Zuständigkeitseinheit eingerichtet ist, dann stellen Sie sicher, dass das Feld **Land-/Regionencode** ausgefüllt ist.|  

### <a name="to-select-the-peppol---invoice-data-exchange-definition-for-electronic-document-receiving"></a>Auswählen der Datenaustauschdefinition „PEPPOL - Rechnung“ für den Empfang von elektronischen Belegen  
1. Geben Sie im Feld **Suchen** einen Wert für **Eingehende Belege** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie in der Zeile für den elektronischen Beleg, der empfangen und konvertiert werden soll, das Feld **Datenaustasuchtyp** und dann **PEPPOL-Rechnung** aus.  

     Wenn der zu empfangen Beleg eine Gutschrift ist, wählen Sie **PEPPOLCREDITMEMO** aus.  

    Nun können Sie den elektronischen Beleg empfangen, indem Sie den Datenkonvertierungsprozess auf der Seite **Eingehende Belege** starten. Weitere Informationen finden Sie unter [Elektronische Belege empfangen und konvertieren](purchasing-how-to-receive-and-convert-electronic-documents.md).  

### <a name="to-set-up-the-gl-account-to-use-on-new-purchase-invoice-lines-for-non-identifiable-items-and-non-items"></a>Einrichten des Sachkontos zur Verwendung bei neuen Einkaufsrechnungszeilen für nicht identifizierbare Artikel und Nicht-Artikel  
1. Geben Sie im Feld **Suchen** **Kreditoren & Einkauf einrichten** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Füllen Sie im Inforegister **Kontenschemata** das Feld gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Standardsollkonto für Nicht-Artikel-Positionen**|Gibt das Sachkonto an, das automatisch in Verkaufszeilen eingefügt wird, die aus elektronischen Dokumenten erstellt werden, wenn die Zeile des eingehenden Beleges keinen identifizierbaren Artikel enthält. Irgendeine Zeile des eingehenden Beleges, die kein GTIN hat, oder die Artikelnummer des Kreditors auf eine Einkaufszeile des Typs **Sachkonto** und **Nr.** Feld der Einkaufsbestellzeile enthält das Konto, das Sie in dem Feld **Sachkonto für Nicht-Artikel-Zeilen** auswählen.<br /><br /> Wenn Sie das **Sachkonteo für Nicht-Artikel-Positionen**-Feld leer lassen und der eingehende Beleg Zeilen ohne identifizierbare Artikel hat, wird der Einkaufsbeleg nicht erstellt. Eine Fehlermeldung weist Sie an, das **Sachkonto Nicht-Artikel-Zeilen**-Feld auszufüllen, bevor Sie die Aufgabe ausführen können.|  

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch  
[Daten elektronisch austauschen](across-data-exchange.md)   
[Fakturieren eines Verkaufs](sales-how-invoice-sales.md)   
[Erfassen eines Einkaufs](purchasing-how-record-purchases.md)
