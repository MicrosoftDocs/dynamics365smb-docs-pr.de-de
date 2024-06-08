---
title: 'Datenaustausch festlegen, um Dateien zu senden und zu empfangen'
description: 'Legen Sie das Framework für den Datenaustausch fest, um Daten mit externen Dateien auszutauschen; um elektronische Belege zu senden und zu empfangen oder Bankdateien zu importieren und zu exportieren.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/11/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="setting-up-data-exchange"></a>Einrichten eines Datenaustauschs

Bevor Sie elektronische Belege senden und empfangen oder Bankdateien importieren und exportieren können, müssen Sie das Daten-Exchange-Framework einrichten, um die entsprechenden Dateien zu verarbeiten. Darüber hinaus müssen Sie verwandte Bereiche einrichten, wie z. B. die Kunden, an die Sie elektronische Rechnungen senden, oder die AMC Banking 365 Fundamentals-Erweiterung, wenn Sie den externen Dienstleister zur Konvertierung Ihrer Bankdateien nutzen. Weitere Informationen finden Sie unter [Daten elektronisch austauschen](across-data-exchange.md).  

 Wenn [!INCLUDE[prod_short](includes/prod_short.md)] für den Datenaustausch mit externen Dateien eingerichtet wurde, können Benutzer die Einrichtung in allgemeinen Geschäftsaufgaben, wie Senden und Empfangen von elektronischen Belegen und Importieren und Exportieren von Bankdateien, verwenden.  

 Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Themen, die sie beschreiben..  

|**Aufgabe**|**Informationen**|  
|------------|-------------|  
|Richten Sie den vorkonfigurierten Belegaustauschdienst für den Versand und den Empfang elektronischer Belege in [!INCLUDE[prod_short](includes/prod_short.md)] ein.|[So richten Sie einen Belegaustauschdienst ein](across-how-to-set-up-a-document-exchange-service.md)|  
|Richten Sie den vorkonfigurierten OCR-Dienst so ein, dass PDF- oder Bilddateien in elektronische Belege umgewandelt werden, die in [!INCLUDE[prod_short](includes/prod_short.md)] in Belegdatensätze konvertiert werden können.|[Einrichten von eingehenden Belegen](across-how-setup-income-documents.md)|  
|Richten Sie einen der beiden vorkonfigurierten Dienste für aktualisierte Wechselkurse so ein, dass auf der Seite **Währungswechselkurse** angezeigt werden.|[Währungswechselkurse aktualisieren](finance-how-update-currencies.md)|  
|Zuerst müssen Sie verschiedene Stammdaten einrichten, zum Beispiel Mandantendaten, Debitoren, Artikel und Einheiten, die auf die Zuordnungsdaten in [!INCLUDE[prod_short](includes/prod_short.md)] Bezug nehmen|[Einrichten des Senden und Empfangen von elektronischen Belegen](across-how-to-set-up-electronic-document-sending-and-receiving.md)|  
|Richten Sie ein Bankkonto, einen Lieferanten und ein Zahlungsbuch für SEPA-Banküberweisung ein.|[Einrichten von SEPA-Kreditübertragung](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#setting-up-sepa-credit-transfer)|  
|Bereiten Sie Bankkonto-Formate, Zahlungsformen und Kundenvereinbarungen für das Lastschriftverfahren SEPA vor.|[Erfassen von Zahlungen per Lastschriftverfahren SEPA](finance-collect-payments-with-sepa-direct-debit.md)|  
|Richten sie die Benutzerauthentifizierung und die URL der AMC Banking 365 Fundamentals-Erweiterung ein, die erforderlich sind, um Bankdateien in das Format Ihrer Bank zu konvertieren.|[AMC Banking 365 Fundamentals-Erweiterung verwenden](ui-extensions-amc-banking.md)|  
|Richten Sie einen externen Dienst ein, der es Ihnen ermöglicht, Bankauszüge als Bankfeeds für Zahlungsausgleich und Bankabstimmung zu importieren.|[Einrichten des Bankauszugservice](bank-how-setup-bank-statement-service.md)|  
|Nachdem der Bankkontoauszugsdienst aktiviert ist, verknüpfen Sie Bankkonten in [!INCLUDE[prod_short](includes/prod_short.md)]|[Bankkonten einrichten](bank-how-setup-bank-accounts.md)|  
|Richten Sie Datenexport für Intrastat-Berichte in [!INCLUDE[prod_short](includes/prod_short.md)] ein.|[Intrastat-Berichte festlegen](finance-how-setup-report-intrastat.md)|
|Bereiten Sie die Einrichtung einer neuen Datenaustauschdefinition für Datendateien oder Datenströme vor, indem Sie das Inforegister **Spaltendefinitionen** auf der Seite **Exchange-Definitinen buchen** mit dem XML-Schema der Datei vorab ausfüllen.|[Verwenden von XML-Schemata zur Vorbereitung der Datenaustauschdefinitionen](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)|  
|Richten Sie das Datenaustauschframework so ein, dass Benutzer ein neues Einkaufsbelegformat empfangen, ein neues Verkaufsbelegformat senden, eine neue Bankdatei importieren oder andere Daten austauschen können.|[Datenaustauschdefinitionen einrichten](across-how-to-set-up-data-exchange-definitions.md)|  

## <a name="see-also"></a>Siehe auch

[Daten elektronisch austauschen](across-data-exchange.md)  
[Eingehende Belege](across-income-documents.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
