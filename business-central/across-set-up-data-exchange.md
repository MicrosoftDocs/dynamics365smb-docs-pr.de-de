---
title: Datenaustausch einrichten | Microsoft Docs
description: Richten Sie das Datenaustauschframework in Business Central ein.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 70672fcab8c2614de58bd152288ba3543fe6955a
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787082"
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
|Zuerst müssen Sie verschiedene Stammdaten einrichten, zum Beispiel Mandantendaten, Debitoren, Artikel und Maßeinheiten, die auf die Zuordnungsdaten in [!INCLUDE[prod_short](includes/prod_short.md)] Bezug nehmen|[Einrichten des Senden und Empfangen von elektronischen Belegen](across-how-to-set-up-electronic-document-sending-and-receiving.md)|  
|Richten Sie ein Bankkonto, einen Lieferanten und ein Zahlungsbuch für SEPA-Banküberweisung ein.|[Einrichten von SEPA-Kreditübertragung](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#setting-up-sepa-credit-transfer)|  
|Bereiten Sie Bankkonto-Formate, Zahlungsformen und Kundenvereinbarungen für das Lastschriftverfahren SEPA vor.|[Erfassen von Zahlungen per Lastschriftverfahren SEPA](finance-collect-payments-with-sepa-direct-debit.md)|  
|Richten sie die Benutzerauthentifizierung und die URL der AMC Banking 365 Fundamentals-Erweiterung ein, die erforderlich sind, um Bankdateien in das Format Ihrer Bank zu konvertieren.|[Verwenden der AMC Banking 365 Fundamentals-Erweiterung](ui-extensions-amc-banking.md)|  
|Richten Sie einen externen Dienst ein, der es Ihnen ermöglicht, Bankauszüge als Bankfeeds für Zahlungsausgleich und Bankabstimmung zu importieren.|[Einrichten des Bankauszugservice](bank-how-setup-bank-statement-service.md)|  
|Nachdem der Bankkontoauszugsdienst aktiviert ist, verknüpfen Sie Bankkonten in [!INCLUDE[prod_short](includes/prod_short.md)]|[Bankkonten einrichten](bank-how-setup-bank-accounts.md)|  
|Bereiten Sie die Einrichtung einer neuen Datenaustauschdefinition für Datendateien oder Datenströme vor, indem Sie das Inforegister **Spaltendefinitionen** auf der Seite **Exchange-Definitinen buchen** mit dem XML-Schema der Datei vorab ausfüllen.|[Verwenden von XML-Schemata zur Vorbereitung der Datenaustauschdefinitionen](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)|  
|Richten Sie das Datenaustauschframework so ein, dass Benutzer ein neues Einkaufsbelegformat empfangen, ein neues Verkaufsbelegformat senden, eine neue Bankdatei importieren oder andere Daten austauschen können.|[Richten Sie Datenaustauschdefinitionen ein](across-how-to-set-up-data-exchange-definitions.md)|  

## <a name="see-also"></a>Siehe auch  
[Daten elektronisch austauschen](across-data-exchange.md)  
[Eingehende Belege](across-income-documents.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]