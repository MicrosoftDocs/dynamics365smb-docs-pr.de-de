---
title: Datenaustausch einrichten | Microsoft Docs
description: Richten Sie das Datenenaustauschframework in Dynamics 365 for Financials ein.
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5c0fcfd6ef178c5917a4a07ba81a9bef9b4522aa
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-data-exchange"></a>Einrichten eines Datenaustauschs
Bevor Sie elektronische Belege senden und empfangen oder Bankdateien importieren und exportieren können, müssen Sie das Daten-Exchange-Framework einrichten, um die entsprechenden Dateien zu verarbeiten. Außerdem müssen Sie zugehörige Bereiche einrichten, z. B. Stammdaten für Debitoren, an die Sie elektronische Rechnungen senden, oder den Bankdaten-Konvertierungsdienst, falls Sie den externen Dienstleister mit der Konvertierung Ihrer Bankdateien beauftragen. Weitere Informationen finden Sie unter [Daten als elektronische Dokumente austauschebn](across-data-exchange.md).  

 Wenn [!INCLUDE[d365fin](includes/d365fin_md.md)] für den Datenaustausch mit externen Dateien eingerichtet wurde, können Benutzer die Einrichtung in allgemeinen Geschäftsaufgaben, wie Senden und Empfangen von elektronischen Belegen und Importieren und Exportieren von Bankdateien, verwenden.  

 Die folgende Tabelle enthält eine Abfolge von Aufgaben sowie Links zu den entsprechenden Themen, in denen diese Aufgaben erläutert werden.  

|**Aufgabe**|**Informationen**|  
|------------|-------------|  
|Richten Sie den vorkonfigurierten Belegaustauschdienst für den Versand und den Empfang elektronischer Belege in [!INCLUDE[d365fin](includes/d365fin_md.md)] ein.|[Gewusst wie: Einrichten eine Belegaustauschdienstes](across-how-to-set-up-a-document-exchange-service.md)|  
|Richten Sie den vorkonfigurierten OCR-Dienst so ein, dass PDF- oder Bilddateien in elektronische Belege umgewandelt werden, die in [!INCLUDE[d365fin](includes/d365fin_md.md)] in Belegdatensätze konvertiert werden können.|[Gewusst wie: Eingehende Dokumente einrichten](across-how-setup-income-documents.md)|  
|Richten Sie einen der beiden vorkonfigurierten Dienste für aktualisierte Wechselkurse so ein, dass im Fenster  **Währungswechselkurse** angezeigt werden.|[Vorgehensweise: Aktualisieren von Währungswechselkursen](finance-how-update-currencies.md)|  
|Zuerst müssen Sie verschiedene Stammdaten einrichten, zum Beispiel Mandantendaten, Debitoren, Artikel und Maßeinheiten, die auf die Zuordnungsdaten in [!INCLUDE[d365fin](includes/d365fin_md.md)] Bezug nehmen|[Gewusst wie: Einrichten des Senden und Empfangen von elektronischen Belegen](across-how-to-set-up-electronic-document-sending-and-receiving.md)|  
|Richten Sie ein Bankkonto, einen Lieferanten und ein Zahlungsbuch für SEPA-Banküberweisung ein.|[So wird's gemacht: SEPA-Kreditübertragungen einrichten](finance-how-to-set-up-sepa-credit-transfer.md)|  
|Bereiten Sie Bankkonto-Formate, Zahlungsmethoden und Kundenvereinbarungen für das Lastschriftverfahren SEPA vor.|[Vorgehensweise: Einrichten von SEPA-Lastschriften](finance-how-to-set-up-sepa-direct-debit.md)|  
|Einrichten von Benutzerauthentifizierung und URL des Bankdatenkonvertierungsdienstanbieters, die erforderlich sind, um Bankdateien in das Format Ihrer Bank zu konvertieren.|[Gewusst wie: Einrichten des Bankdatenkonvertierungsservice](bank-how-setup-bank-data-conversion-service.md)|  
|Richten Sie einen externen Dienst ein, der es Ihnen ermöglicht, Bankauszüge als Bankfeeds für Zahlungsausgleich und Bankabstimmung zu importieren.|[Gewusst wie: Einrichten des Bankauszugservice](bank-how-setup-bank-statement-service.md)|  
|Nachdem der Bankkontoauszugsdienst aktiviert ist, verknüpfen Sie Bankkonten in [!INCLUDE[d365fin](includes/d365fin_md.md)]|[So geht's: Bankkonten einrichten](bank-how-setup-bank-accounts.md)|  
|Bereiten Sie die Einrichtung einer neuen Datenaustauschdefinition für Datendateien oder Datenströme vor, indem Sie das Inforegister **Spaltendefinitionen** im Fenster **Exchange-Definitinen buchen**mit dem XML-Schema der Datei vorab ausfüllen.|[Gewusst wie: Verwenden von XML-Schemata zur Vorbereitung von Datenaustauschdefinitionen](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)|  
|Richten Sie das Datenaustauschframework so ein, dass Benutzer ein neues Einkaufsbelegformat empfangen, ein neues Verkaufsbelegformat senden, eine neue Bankdatei importieren oder andere Daten austauschen können.|[Vorgehensweise: Richten Sie Datenaustauschdefinitionen ein.](across-how-to-set-up-data-exchange-definitions.md)|  

## <a name="see-also"></a>Siehe auch  
[Datenaustausch als Elektronische Dokumente ](across-data-exchange.md)  
[Austauschdaten](across-exchange-data.md)   
[Eingehende Belege](across-income-documents.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  

