---
title: Importieren Sie Ihre Stammdaten in Financials | Microsoft Docs
description: "Sie können Daten für Debitoren, Kreditoren und Lager zum Beispiel aus Excel oder QuickBooks Dynamics GP, in Financials migrieren."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migrate, initialize, implement
ms.date: 07/05/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2a38dc36cb9ff609c5582acd489841b20013d4bc
ms.openlocfilehash: dd6eb5a6b19bf4c8fd92674a48e8cd29ce912eee
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="importing-business-data-from-other-finance-systems"></a>Geschäftsdaten aus anderen Finanzsystemen importieren
Wenn Sie sich bei [!INCLUDE[d365fin](includes/d365fin_md.md)] anmelden, können Sie auswählen, einen leeren Mandanten zu erstellen, sodass Sie Ihre eigenen Daten hochladen und den neuen Projektmandanten in [!INCLUDE[d365fin](includes/d365fin_md.md)] testen können. Abhängig von der Finanzlösung, die Ihr Unternehmen heute verwendet, können Sie Informationen zu Debitoren, Kreditoren, Lagerbestand und Bankkonten vornehmen.  

Vom Startbildschirm aus können Sie eine unterstützte Einrichtung vornehmen, mit der Sie die Daten einer Exceldatei oder aus anderen Formaten übertragen können. Die Art der Dateien, die Sie hochladen können, hängt von den Erweiterungen ab, die verfügbar sind. Beispielsweise können Sie Daten aus QuickBooks hochladen, da [!INCLUDE[d365fin](includes/d365fin_md.md)] eine Erweiterung umfasst, die die Umwandlung von QuickBooks behandelt. Wenn Sie Daten aus anderen Finanzlösungen migrieren möchten, müssen Sie überprüfen, ob eine Erweiterung für diese Lösung verfügbar ist oder sie aus Excel importieren.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] umfasst Vorlagen für Debitoren, Kreditoren und Lagerartikel, die Sie zum Anwenden wählen können, wenn Sie Ihre Daten importieren.  

## <a name="importing-data-from-quickbooks-or-dynamics-gp"></a>Importieren von Daten aus QuickBooks oder von Dynamics GP
Wenn Ihr Geschäft heute QuickBooks oder Dynamics GP verwendet, können Sie die relevanten Daten in eine Datei exportieren. Sie können dann die unterstütze Einrichtung öffnen, um die Daten zu übertragen.
Wenn beispielsweise Ihre Datei Debitoren und Kreditoren umfasst, können Sie wählen, nur die Debitorendaten umzulagern. Sie können die restlichen Daten dann später übertragen.  

Die unterstützte Einrichtung umfasst eine Option, die Vorgabe Konfiguration der Übertragung zu ändern. Wir empfehlen aber, dass nur dieses erweiterte Einrichtung eingeben wird, wenn Sie mit Datenbanktabellen vertraut sind. In der überwiegenden Mehrheit von Geschäften überträgt die Standardzuordnung von QuickBook oder Dynamics GP die Informationen zu [!INCLUDE[d365fin](includes/d365fin_md.md)], die Sie möchten.  

Weitere Informationen finden Sie unter [QuickBooks-Datenmigration](ui-extensions-quickbooks-data-migration.md) oder [Dynamics GP-Datenmigration](ui-extensions-dynamicsgp-data-migration.md).

## <a name="importing-data-from-configuration-packages"></a>Importieren von Daten aus den Konfigurations-Paketen
[!INCLUDE[d365fin](includes/d365fin_md.md)] umfasst ein Konfigurationspaket, das Sie dann in Excel exportieren und dort die Daten einrichten können. Anschließend können die wieder von Excel importiert werden. Das Paket besteht aus 27 Tabellen, einschließlich Masterdaten wie Debitoren, Kreditoren, Artikel und Konten, andere grundsätzliche Einrichtungstabellen wie Versandarten und Transaktionstabellen wie Versandkopf und Zeilen.  

> [!NOTE]  
>   Das Arbeiten mit Konfigurationspaketen ist eine erweiterte Funktionalität und wir empfehlen, dass Sie sich an Ihren Administrator wenden. [Importieren von Daten aus der Vorgänger-Buchhaltungs-Software unter Verwendung eines Konfigurations-Pakets](across-import-data-configuration-packages.md)  

## <a name="see-also"></a>Siehe auch
[Finanzen](finance.md)  
[Importieren von Daten aus der Vorgänger-Buchhaltungs-Software unter Verwendung eines Konfigurations-Pakets.](across-import-data-configuration-packages.md)  
[QuickBooks Datenmigration](ui-extensions-quickbooks-data-migration.md)  
[Dynamics GP Datenmigration](ui-extensions-dynamicsgp-data-migration.md)  
[Anpassen[!INCLUDE[d365fin](includes/d365fin_md.md)]Erweiterungen nutzen ](ui-extensions.md)   
[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

