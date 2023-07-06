---
title: Nutzung der Quickbooks-Gehaltsabrechnungsdatei-Importerweiterung| Microsoft Docs
description: 'Beschreibt, wie die Erweiterung verwendet wird, um Gehalts- und Lohntransaktionen aus dem Quickbooks-Gehaltsabrechnungsdienst zu importieren.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: 'app, add-in, manifest, customize, salary, wage'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="the-quickbooks-payroll-file-import-extension"></a><a name="the-quickbooks-payroll-file-import-extension"></a><a name="the-quickbooks-payroll-file-import-extension"></a>Die Quickbooks-Gehaltsabrechnungsdatei-Importerweiterung
Verwenden Sie die QuickBooks-Gehaltsabrechnungsdatei-Importerweiterung, um Gehaltsabrechnungstransaktionen von QuickBooks mit den Sachkonten in [!INCLUDE[prod_short](includes/prod_short.md)] zu importieren. Dies ist beispielsweise dann nützlich, wenn Sie von QuickBooks zu [!INCLUDE[prod_short](includes/prod_short.md)] wechseln oder, dass Sie Löhne auslagern aber diese in [!INCLUDE[prod_short](includes/prod_short.md)] nachverfolgen möchten.

## <a name="steps-to-import-payroll-data"></a><a name="steps-to-import-payroll-data"></a><a name="steps-to-import-payroll-data"></a>So importieren Sie Lohndaten
Der erste Schritt für Sie oder IHren Buchhalter ist es, die Exportfunktionen in QuickBook zu verwenden, um die Lohndaten in eine .IIF Datei zu exportieren. Der zweite Schritt ist es, die **Fibu Buch.-Blätter** in [!INCLUDE[prod_short](includes/prod_short.md)] zu öffnen und die **Lohntransaktionen importieren** Aktion zu verwenden, um die Datei zu importieren. Während des Importvorgangs ordnen Sie Sachkonten aus QuickBooks auf den entsprechenden Konten in [!INCLUDE[prod_short](includes/prod_short.md)]. Zuletzt buchen Sie die Gehaltsabrechnungstransaktionen in [!INCLUDE[prod_short](includes/prod_short.md)]mentsprechend der Kontozuordnung. 

Weitere Informationen finden Sie unter [Gehaltsabrechnungstransaktionen importieren](finance-how-import-payroll-transactions.md).

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Weitere Informationen
[Anpassen [!INCLUDE[prod_short](includes/prod_short.md)] Erweiterungen nutzen](ui-extensions.md)    
[Finanzen](finance.md)    
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
