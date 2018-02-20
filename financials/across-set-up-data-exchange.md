---
title: Datenaustausch einrichten | Microsoft Docs
description: Richten Sie das Datenenaustauschframework in Finance and Operations, Business edition ein.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: a043ad387455cf93182689b0c58025be7186c0cd
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="setting-up-data-exchange"></a>Einrichten eines Datenaustauschs
Bevor Sie elektronische Belege senden und empfangen oder Bankdateien importieren und exportieren können, müssen Sie das Daten-Exchange-Framework einrichten, um die entsprechenden Dateien zu verarbeiten. Außerdem müssen Sie zugehörige Bereiche einrichten, z. B. Stammdaten für Debitoren, an die Sie elektronische Rechnungen senden, oder den Bankdaten-Konvertierungsdienst, falls Sie den externen Dienstleister mit der Konvertierung Ihrer Bankdateien beauftragen. Weitere Informationen finden Sie unter [Daten elektronisch austauschen](across-data-exchange.md).  

 Wenn [!INCLUDE[d365fin](includes/d365fin_md.md)] für den Datenaustausch mit externen Dateien eingerichtet wurde, können Benutzer die Einrichtung in allgemeinen Geschäftsaufgaben, wie Senden und Empfangen von elektronischen Belegen und Importieren und Exportieren von Bankdateien, verwenden.  

 Die folgende Tabelle enthält eine Abfolge von Aufgaben sowie Links zu den entsprechenden Themen, in denen diese Aufgaben erläutert werden.  

|**Aufgabe**|**Informationen**|  
|------------|-------------|  
|Richten Sie den vorkonfigurierten Belegaustauschdienst für den Versand und den Empfang elektronischer Belege in [!INCLUDE[d365fin](includes/d365fin_md.md)] ein.|[So richten Sie einen Belegaustauschdienst ein](across-how-to-set-up-a-document-exchange-service.md)|  
|Richten Sie den vorkonfigurierten OCR-Dienst so ein, dass PDF- oder Bilddateien in elektronische Belege umgewandelt werden, die in  in Belegdatensätze konvertiert werden können. [!INCLUDE[d365fin](includes/d365fin_md.md)]|[Einrichten von eingehenden Belegen](across-how-setup-income-documents.md)|  
|Richten Sie einen der beiden vorkonfigurierten Dienste für aktualisierte Wechselkurse so ein, dass im Fenster **Währungswechselkurse** angezeigt werden.|[Währungswechselkurse aktualisieren](finance-how-update-currencies.md)|  
|Zuerst müssen Sie verschiedene Stammdaten einrichten, zum Beispiel Mandantendaten, Debitoren, Artikel und Maßeinheiten, die auf die Zuordnungsdaten in  Bezug nehmen [!INCLUDE[d365fin](includes/d365fin_md.md)]|[Einrichten des Senden und Empfangen von elektronischen Belegen](across-how-to-set-up-electronic-document-sending-and-receiving.md)|  
|Richten Sie ein Bankkonto, einen Lieferanten und ein Zahlungsbuch für SEPA-Banküberweisung ein.|[Einrichten von SEPA-Kreditübertragung](finance-how-to-set-up-sepa-credit-transfer.md)|  
|Bereiten Sie Bankkonto-Formate, Zahlungsmethoden und Kundenvereinbarungen für das Lastschriftverfahren SEPA vor.|[Einrichten von SEPA-Lastschriften](finance-how-to-set-up-sepa-direct-debit.md)|  
|Einrichten von Benutzerauthentifizierung und URL des Bankdatenkonvertierungsdienstanbieters, die erforderlich sind, um Bankdateien in das Format Ihrer Bank zu konvertieren.|[Einrichten des Bankdaten-Konvertierungsdienst](bank-how-setup-bank-data-conversion-service.md)|  
|Richten Sie einen externen Dienst ein, der es Ihnen ermöglicht, Bankauszüge als Bankfeeds für Zahlungsausgleich und Bankabstimmung zu importieren.|[Einrichten des Bankauszugservice](bank-how-setup-bank-statement-service.md)|  
|Nachdem der Bankkontoauszugsdienst aktiviert ist, verknüpfen Sie Bankkonten in  [!INCLUDE[d365fin](includes/d365fin_md.md)]|[Bankkonten einrichten](bank-how-setup-bank-accounts.md)|  
|Bereiten Sie die Einrichtung einer neuen Datenaustauschdefinition für Datendateien oder Datenströme vor, indem Sie das Inforegister **Spaltendefinitionen** im Fenster **Exchange-Definitinen buchen** mit dem XML-Schema der Datei vorab ausfüllen.|[Verwenden von XML-Schemata zur Vorbereitung der Datenaustauschdefinitionen](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)|  
|Richten Sie das Datenaustauschframework so ein, dass Benutzer ein neues Einkaufsbelegformat empfangen, ein neues Verkaufsbelegformat senden, eine neue Bankdatei importieren oder andere Daten austauschen können.|[Richten Sie Datenaustauschdefinitionen ein.](across-how-to-set-up-data-exchange-definitions.md)|  

## <a name="see-also"></a>Siehe auch  
[Daten elektronisch austauschen](across-data-exchange.md)  
[Austausch von Daten](across-exchange-data.md)   
[Eingehende Belege](across-income-documents.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  

