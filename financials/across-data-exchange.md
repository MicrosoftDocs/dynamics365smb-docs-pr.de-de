---
title: Elektronische Dokumente in Dynamics 365 Business edition  | Microsoft Docs
description: "Einführung zum Senden und Empfang von elektronischen Dokumenten in Dynamics 365."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/19/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: dca451d2555641dc1c1fc134b19380b3ede2690b
ms.contentlocale: de-de
ms.lasthandoff: 12/14/2017

---

# <a name="exchanging-data-electronically"></a>Daten elektronisch austauschen
Sie können das Datenaustauschframework verwenden, um Geschäftsbelege, Bankdateien, Währungswechselkurse und andere Datendateien mit Ihren Geschäftspartnern auszutauschen.

## <a name="electronic-documents"></a>Elektronische Belege
Als Alternative zu E-Mail-Dateianhängen können Sie Geschäftsbelegen elektronisch versenden und empfangen. Mit elektronischem Beleg ist eine normgerechte Datei gemeint, die ein Geschäftsdokument darstellt, zum Beispiel eine Rechnung von einem Kreditor, die Sie in [!INCLUDE[d365fin](includes/d365fin_md.md)] empfangen und in eine Einkaufsrechnung konvertieren können. Der Austausch von elektronischen Belegen zwischen zwei Handelspartnern erfolgt über einen externen Anbieter eines Belegaustauschdiensts. Die allgemeine Version von [!INCLUDE[d365fin](includes/d365fin_md.md)]  unterstützt das Senden und Empfangen von elektronischen Rechnungen und Gutschriften im PEPPOL-Format, das von den größten Anbietern von Belegaustauschdiensten unterstützt wird. Ein wichtiger Anbieter eines Belegaustauschdienstes ist vorkonfiguriert und kann für Ihren Mandanten eingerichtet werden. Um Unterstützung für andere elektronische Belegformate zu bieten, müssen Sie mithilfe des Datenaustauschframework neue Datenaustauschdefinitionen erstellen.  

Mithilfe eines externen OCR-Dienstes (optische Zeichenerkennung) können Sie aus PDF- oder Bilddateien, die die Eingangsbelege darstellen, elektronische Belege erstellen, die Sie dann in [!INCLUDE[d365fin](includes/d365fin_md.md)] in Belegdatensätze konvertieren können, wie Sie es für elektronische PEPPOL-Belege tun. Wenn Sie beispielsweise eine Rechnung in PDF-Format von Ihrem Kreditor erhalten, können Sie diese über das Fenster **Eingehende Belege** zum OCR-Dienst senden. Nach einigen Sekunden erhalten Sie die Datei als elektronische Rechnung zurück, die zu einer Einkaufsrechnung für den Kreditor umgewandelt werden kann. Wenn Sie die Datei per E-Mail an den OCR-Service senden, wird automatisch ein neuer Datensatz für einen eingehenden elektronischen Beleg erstellt, wenn Sie den elektronischen Belegs zurückerhalten.  

Um beispielsweise Verkaufsrechnungen als elektronischer PEPPOL-Beleg zu senden, wählen Sie die Option **Elektronisches Dokument** im **Buchen und senden**-Dialogfeld aus. Dort können Sie außerdem das standardmäßige Belegsendeprofil für den Debitor einrichten. Zuerst müssen Sie verschiedene Stammdaten einrichten, zum Beispiel Mandantendaten, Debitoren, Artikel und Maßeinheiten. Diese werden verwendet, um Geschäftspartner und Artikel beim Konvertieren von Daten in Feldern in [!INCLUDE[d365fin](includes/d365fin_md.md)] in Elemente der ausgehenden Dokumentdatei zu identifizieren. Die Datenkonvertierung und das Senden der PEPPOL-Verkaufsrechnung werden durch dedizierte Codeunits und XMLports ausgeführt, die im elektronischen Belegformat **PEPPOL** dargestellt werden.  

Um beispielsweise eine Rechnung von einem Kreditor in Form eines elektronischen PEPPOL-Belegs zu erhalten, verarbeiten Sie den Beleg im Fenster **Eingehende Dokumente**, um ihn in eine Einkaufsrechnung in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu konvertieren. Sie können entweder die Auftragswarteschlange zur regelmäßigen Verarbeitung solcher Dateien einrichten, oder Sie können den Vorgang manuell starten. Zuerst müssen Sie verschiedene Stammdaten einrichten, zum Beispiel Mandantendaten, Kreditoren, Artikel und Maßeinheiten. Diese werden verwendet, um Geschäftspartner und Artikel zu identifizieren, wenn Daten in Elementen im Eingangsbeleg zu Feldern in [!INCLUDE[d365fin](includes/d365fin_md.md)] konvertiert werden. Der Empfang und die Datenkonvertierung von PEPPOL-Rechnungen erfolgen über das Datenaustauschframework, das durch die Datenaustauschdefinition **PEPPOL - Rechnung** dargestellt wird.  

 Um zum Beispiel eine Rechnung als elektronischer OCR-Beleg zu empfangen, verarbeiten Sie diese genauso wie beim Empfang eines elektronischen PEPPOL-Belegs. Der Empfang und die Konvertierung von elektronischen Belegen von OCR wird über das Datenaustauschframework durchgeführt, das durch die Datenaustauschdefinition **OCR - Rechnung** dargestellt wird.  

## <a name="bank-files"></a>Bankdateien  
 Die Formate der Dateien für den Austausch von Bankdaten mit ERP-Systemen variieren abhängig vom Lieferanten der Datei und vom jeweiligen Land oder der Region. Die allgemeine Version von [!INCLUDE[d365fin](includes/d365fin_md.md)]  unterstützt den Import und Export von SEPA-Bankdateien (Single Euro Payments Area; einheitlicher Euro-Zahlungsverkehrsraum) und einen Bankdaten-Konvertierungsdienst, der vom externen Anbieter AMC Consult bereitgestellt wird. Um Unterstützung für andere elektronische Belegformate zu bieten, verwenden Sie das Datenaustauschframework.  

Um SEPA-Gutschriftübertragungen zu exportieren, wählen Sie die Schaltfläche **Zahlungen in Datei exportieren** im Fenster **Zahlungs-Buch-Blatt.** aus und laden die Datei dann hoch, um die Zahlungen bei Ihrer Bank in Auftrag zu geben. Zuerst müssen Sie verschiedene Stammdaten einrichten, wie Bankkonto, Kreditoren und Zahlungsformen. Die Datenkonvertierung und der Export von SEPA-Bankdaten werden durch dedizierte Codeunits und XMLports ausgeführt, die durch das Bankexport-/-importsetup **SEPA Kreditübertragung** dargestellt werden. Alternativ können Sie den Bankdaten-Konvertierungsdienst so einrichten, dass er den Export ausführt. Dies wird durch die Datenaustauschdefinition **Bankdaten-Konvertierungsdienst - Kreditübertragung** dargestellt.  

Um SEPA-Lastschriften zu exportieren, wählen Sie die Schaltfläche **Lastschriftdatei exportieren** im Fenster **Lastschrift** aus und senden die Datei dann zu Ihrer Bank, damit die entsprechenden Debitorenzahlungen automatisch erfasst werden. Zuerst müssen Sie Bankkonten, Debitoren, Lastschrift-Mandage und Zahlungsformen einrichten. Die Datenkonvertierung und der Export von SEPA-Bankdaten werden durch dedizierte Codeunits und XMLports ausgeführt, die durch das **SEPA-Lastschrift** Bankexport-/-importsetup dargestellt werden.  

Um SEPA-Bankauszüge zu importieren, wählen Sie die Schaltfläche "Bankauszug importieren" in den Fenstern **Zahlungsabstimmungsbuch.-Blatt** und **Bankkonto-Abstimmung** aus. Gleichen Sie dann die einzelnen Bankkontoauszugsposten manuell oder automatisch mit Zahlungen der Bankposten aus. Zuerst müssen Sie Bankkonten einrichten. Der Import und die Datenkonvertierung von SEPA-Bankdaten erfolgen über das Datenaustauschframework, das durch die Datenaustauschdefinition **SEPA CAMT** dargestellt wird. Alternativ können Sie den Bankdaten-Konvertierungsdienst so einrichten, dass er den Import ausführt. Dies wird durch die Datenaustauschdefinition **Bankdaten-Konvertierungsdienst – Bankauszug** dargestellt.  

 Darüber hinaus unterstützen die lokalen Versionen von [!INCLUDE[d365fin](includes/d365fin_md.md)] verschiedene andere Dateiformate für den Import und Export von Bankdaten, Lohntransaktionen und anderen Daten. Weitere Informationen finden Sie im Abschnitt „Lokale Funktion“ in der Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] für Ihr Land.  

## <a name="currency-exchange-rates"></a>Währungswechselkurse  
Sie können einen externen Service einrichten, um Ihre Währungswechselkurses auf dem neuesten Stand zu halten. Der Service, der aktualisierte Währungswechselkurses bereitstellt, wird durch eine Datenaustauschdefinition aktiviert. Entsprechend wird das **Wechselkursaktualisierungskarte einrichten** Fenster eine verkürzte Darstellungsform des Fensters **Datenaustauschdefinition** für die entsprechenden Datenaustauschdefinition.  

Für den gesamten Austausch von Daten in XML-Dateien können Sie die Einrichtung des Datenaustausches vorbereiten, indem Sie die zugehörige **XML-Schemadatei** im Fenster laden. Hier wählen Sie die Datenelemente aus, die Sie mit [!INCLUDE[d365fin](includes/d365fin_md.md)] austauschen möchten, und dann initialisieren Sie entweder eine Datenaustauschdefinition oder generieren einen XMLport.  

Die folgende Tabelle enthält eine Abfolge von Aufgaben sowie Links zu den entsprechenden Themen, in denen diese Aufgaben erläutert werden.  

|Aufgabe|Siehe|  
|--------|---------|  
|Erfahren Sie, wie das Daten-Exchange-Framework arbeitet.|[Über das Datenaustauschframework](across-about-the-data-exchange-framework.md)|  
|Bereiten Sie den Datenaustausch per Datei vor, indem Sie das XML-Schema der Datei verwenden. Richten Sie Datenaustauschdefinitionen ein. Richten Sie Stammdaten für das Senden von elektronischen Belegen ein. Richten Sie verschiedene Felder für den Bankimport und -export ein.|[Einrichten eines Datenaustauschs](across-set-up-data-exchange.md)|  
|Auf der Grundlage von Datenaustauschdefinitionen senden und empfangen Sie PEPPOL-Rechnungen, importieren Bankauszüge und exportieren Bankzahlungsdateien.|[Austausch von Daten](across-exchange-data.md)|  

## <a name="see-also"></a>Siehe auch  
[Über das Datenaustauschframework](across-about-the-data-exchange-framework.md)  
[Gewusst wie: Verwenden von XML-Schemata zur Vorbereitung von Datenaustauschdefinitionen](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Einrichten eines Datenaustauschs](across-set-up-data-exchange.md)  
[Austausch von Daten](across-exchange-data.md)  
[Eingehende Belege](across-income-documents.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)

