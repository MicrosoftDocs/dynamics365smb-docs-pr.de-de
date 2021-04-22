---
title: Über das Datenaustauschframework | Microsoft Docs
description: Das Format von Dateien zum Austausch von Daten in den Bankdateien, die elektronischen Belegen, die Währungsumrechnungsraten und anderen mit ERP-Systemen variieren abhängig vom Anbieter der Datendatei oder des Streams und dem Land/der Region.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 6ae76aa8f8522b7d93dd442d6d8cc748f1d2dac4
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776322"
---
# <a name="about-the-data-exchange-framework"></a>Über das Datenaustauschframework

Sie können das Datenaustauschframework verwenden, um den Austausch von Geschäftsbelegen, Bankdateien, Währungswechselkursen und sämtlichen anderen Datendateien mit Ihren Geschäftspartnern zu verwalten.

Als Administrator oder Microsoft-Partner können Sie das Framework in neuen Integrationsfunktionen verwenden, indem Sie festlegen, welche Daten ausgetauscht werden sollen und wie. Beispielsweise das Format von Dateien zum Austausch von Daten in den Bankdateien, von elektronischen Dokumenten, von Währungswechselkursen und anderen mit ERP-Systemen variieren abhängig vom Anbieter der Datendatei oder des Streams und von Land/Region. [!INCLUDE[prod_short](includes/prod_short.md)] unterstützt verschiedene Bankdateiformate und Datendienststandards. Um Unterstützung für andere elektronische Belegformate zu bieten, verwenden Sie das Datenaustauschframework.

 Die folgenden Diagramme zeigen die Architektur des Daten-Exchange-Frameworks an.  

 ![Import von Datenaustauschframework &#45;](media/across-data-exchange/dataexchangeframework_import.png)  

 ![Export von Datenaustauschframework &#45;](media/across-data-exchange/dataexchangeframework_export.png)  

## <a name="electronic-documents"></a>Elektronische Belege

Als Alternative zu E-Mail-Dateianhängen können Sie Geschäftsbelegen elektronisch versenden und empfangen. Mit elektronischem Beleg ist eine normgerechte Datei gemeint, die ein Geschäftsdokument darstellt, zum Beispiel eine Rechnung von einem Kreditor, die Sie in [!INCLUDE[prod_short](includes/prod_short.md)] empfangen und in eine Einkaufsrechnung konvertieren können. Der Austausch von elektronischen Belegen zwischen zwei Handelspartnern erfolgt über einen externen Anbieter eines Belegaustauschdiensts. Die allgemeine Version von [!INCLUDE[prod_short](includes/prod_short.md)]  unterstützt das Senden und Empfangen von elektronischen Rechnungen und Gutschriften im PEPPOL-Format, das von den größten Anbietern von Belegaustauschdiensten unterstützt wird. Ein wichtiger Anbieter eines Belegaustauschdienstes ist vorkonfiguriert und kann für Ihren Mandanten eingerichtet werden. Um Unterstützung für andere elektronische Belegformate zu bieten, müssen Sie mithilfe des Datenaustauschframework neue Datenaustauschdefinitionen erstellen.  

 Mithilfe eines externen OCR-Dienstes (optische Zeichenerkennung) können Sie aus PDF- oder Bilddateien, die die eingehenden Belege darstellen, elektronische Belege erstellen, die Sie dann in [!INCLUDE[prod_short](includes/prod_short.md)] in Belegdatensätze konvertieren können, wie Sie es für elektronische PEPPOL-Belege tun. Wenn Sie beispielsweise eine Rechnung in PDF-Format von Ihrem Kreditor erhalten, können Sie diese über die Seiter **Eingehende Belege** zum OCR-Dienst senden. Nach einigen Sekunden erhalten Sie die Datei als elektronische Rechnung zurück, die zu einer Einkaufsrechnung für den Kreditor umgewandelt werden kann. Wenn Sie die Datei per E-Mail an den OCR-Service senden, wird automatisch ein neuer eingehender Beleg erstellt, wenn Sie den elektronischen Belegs zurückerhalten.  

 Um beispielsweise Verkaufsrechnungen als elektronischer PEPPOL-Beleg zu senden, wählen Sie die Option **Elektronisches Dokument** im **Buchen und senden**-Dialogfeld aus. Dort können Sie außerdem das standardmäßige Belegsendeprofil für den Kunden einrichten. Zuerst müssen Sie verschiedene Stammdaten einrichten, zum Beispiel Mandantendaten, Debitoren, Artikel und Maßeinheiten. Diese werden verwendet, um Geschäftspartner und Artikel beim Konvertieren von Daten in Feldern in [!INCLUDE[prod_short](includes/prod_short.md)] in Elemente der ausgehenden Dokumentdatei zu identifizieren. Die Datenkonvertierung und das Senden der PEPPOL-Verkaufsrechnung werden durch dedizierte Codeunits und XMLports ausgeführt, die im elektronischen Belegformat **PEPPOL** dargestellt werden.  

 Um beispielsweise eine Rechnung von einem Kreditor in Form eines elektronischen PEPPOL-Belegs zu erhalten, verarbeiten Sie den Beleg auf der Seite **Eingehende Belege**, um ihn in eine Einkaufsrechnung in [!INCLUDE[prod_short](includes/prod_short.md)] zu konvertieren. Sie können entweder die Auftragswarteschlange zur regelmäßigen Verarbeitung solcher Dateien einrichten, oder Sie können den Vorgang manuell starten. Zuerst müssen Sie verschiedene Stammdaten einrichten, zum Beispiel Mandantendaten, Kreditoren, Artikel und Maßeinheiten. Diese werden verwendet, um Geschäftspartner und Artikel zu identifizieren, wenn Daten in Elementen im eingehenden Beleg zu Feldern in [!INCLUDE[prod_short](includes/prod_short.md)] konvertiert werden. Der Empfang und die Datenkonvertierung von PEPPOL-Rechnungen erfolgen über das Datenaustauschframework, das durch die Datenaustauschdefinition **PEPPOL - Rechnung** dargestellt wird.  

  Um zum Beispiel eine Rechnung als elektronischer OCR-Beleg zu empfangen, verarbeiten Sie diese genauso wie beim Empfang eines elektronischen PEPPOL-Belegs. Der Empfang und die Konvertierung von elektronischen Belegen von OCR wird über das Datenaustauschframework durchgeführt, das durch die Datenaustauschdefinition **OCR - Rechnung** dargestellt wird.  

## <a name="bank-files"></a>Bankdateien

Die Formate der Dateien für den Austausch von Bankdaten mit ERP-Systemen variieren je nach Anbieter der Datei und Land oder Region. [!INCLUDE[prod_short](includes/prod_short.md)] unterstützt den Import und Export von SEPA-Bankdateien (Single Euro Payments Area) und die AMC Banking 365 Fundamentals-Erweiterung ermöglicht die Verbindung zu einer AMC Banking 365 Fundamentals-Erweiterung des externen Anbieters AMC Consult. Um Unterstützung für andere elektronische Belegformate zu bieten, verwenden Sie das Datenaustauschframework.  

Um SEPA-Gutschriftübertragungen zu exportieren, wählen Sie die Schaltfläche **Zahlungen in Datei exportieren** auf der Seite **Zahlungs-Buch-Blatt.** aus und laden die Datei dann hoch, um die Zahlungen bei Ihrer Bank in Auftrag zu geben. Zuerst müssen Sie verschiedene Stammdaten einrichten, wie Bankkonto, Kreditoren und Zahlungsformen. Die Datenkonvertierung und der Export von SEPA-Bankdaten erfolgen durch eine dedizierte Codeunit und XMLport, die durch das Bank-Export-/Import-Setup **SEPA-Kreditübertragung** dargestellt werden. Alternativ können Sie die AMC Banking 365 Fundamentals-Erweiterung für den Export einrichten, dargestellt durch die **AMC Banking 365 Fundamentals-Erweiterung – Kreditübertragung** Datenaustauschdefinition.  

 Um SEPA-Lastschriften zu exportieren, wählen Sie die Schaltfläche **Lastschriftdatei exportieren** auf der Seite **Lastschrift** aus und senden die Datei dann zu Ihrer Bank, damit die entsprechenden Debitorenzahlungen automatisch erfasst werden. Zuerst müssen Sie Bankkonten, Debitoren, Lastschrift-Mandage und Zahlungsformen einrichten. Die Datenkonvertierung und der Export von SEPA-Bankdaten erfolgt durch eine dedizierte Codeunit und XMLport, die durch das Bank-Export-/Import-Setup **SEPA-Lastschrift** dargestellt werden.  

 Um SEPA-Bankauszüge zu importieren, wählen Sie die Schaltfläche "Bankauszug importieren" in den Fenstern **Zahlungsabstimmungsbuch.-Blatt** und **Bankkonto-Abstimmung** aus. Gleichen Sie dann die einzelnen Bankkontoauszugsposten manuell oder automatisch mit Zahlungen der Bankposten aus. Zuerst müssen Sie Bankkonten einrichten. Der Import und die Datenkonvertierung von SEPA-Bankdaten erfolgen über das Datenaustauschframework, das durch die Datenaustauschdefinition **SEPA CAMT** dargestellt wird. Alternativ können Sie die AMC Banking 365 Fundamentals-Erweiterung für den Import einrichten, dargestellt durch die **AMC Banking 365 Fundamentals-Erweiterung – Bankauszug** Datenaustauschdefinition.  

 Darüber hinaus unterstützen die lokalen Versionen von [!INCLUDE[prod_short](includes/prod_short.md)] verschiedene andere Dateiformate für den Import und Export von Bankdaten, Lohnabrechnungen und anderen Daten. Weitere Informationen finden Sie auf der Landing Page [Lokale Funktionalität](about-localization.md) für Ihr Land/Ihre Region in der Hilfe.  

## <a name="currency-exchange-rates"></a>Währungswechselkurse

Sie können einen externen Service einrichten, um Ihre Währungswechselkurses auf dem neuesten Stand zu halten. Der Service, der aktualisierte Währungswechselkurses bereitstellt, wird durch eine Datenaustauschdefinition aktiviert. Entsprechend wird die **Wechselkursaktualisierungskarte einrichten** Seite eine verkürzte Darstellungsform des Fensters **Datenaustauschdefinition** für die entsprechenden Datenaustauschdefinition.  

Für den gesamten Austausch von Daten in XML-Dateien können Sie die Einrichtung des Datenaustausches vorbereiten, indem Sie die zugehörige **XML-Schemadatei** auf die Seite laden. Hier wählen Sie die Datenelemente aus, die Sie mit [!INCLUDE[prod_short](includes/prod_short.md)] austauschen möchten, und dann initialisieren Sie entweder eine Datenaustauschdefinition oder generieren einen XMLport.

## <a name="see-also"></a>Siehe auch

[Daten elektronisch austauschen](across-data-exchange.md)  
[Verwenden von XML-Schemas, um Datenaustauschdefinitionen vorzubereiten](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Datenaustausch einrichten](across-set-up-data-exchange.md)  
[Eingehende Belege](across-income-documents.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]