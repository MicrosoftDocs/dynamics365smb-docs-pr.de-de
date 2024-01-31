---
title: Nutzung der Erweiterung zum Importieren der Quickbooks-Lohnbuchhaltungsdatei | Microsoft-Dokumentation
description: 'Dieser Artikel beschreibt, wie die Erweiterung verwendet wird, um Gehalts- und Lohntransaktionen aus Quickbooks zu importieren.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms. search.keywords: 'app, add-in, manifest, customize, salary, wage'
ms.date: 12/07/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Die Erweiterung zum Importieren der Quickbooks-Lohnbuchhaltung
Verwenden Sie die QuickBooks-Gehaltsabrechnungsdatei-Importerweiterung, um Gehaltsabrechnungstransaktionen von QuickBooks mit den Sachkonten in [!INCLUDE[prod_short](includes/prod_short.md)] zu importieren. Dies ist beispielsweise dann nützlich, wenn Sie von QuickBooks zu [!INCLUDE[prod_short](includes/prod_short.md)] wechseln oder, dass Sie Ihre Lohnbuchhaltung auslagern, diese aber in [!INCLUDE[prod_short](includes/prod_short.md)] nachverfolgen möchten.

## So importieren Sie Lohnbuchhaltungsdaten
Der erste Schritt für Sie oder IHren Buchhalter ist es, die Exportfunktionen in QuickBook zu verwenden, um die Lohndaten in eine .IIF Datei zu exportieren. Der zweite Schritt ist es, die **Fibu Buch.-Blätter** in [!INCLUDE[prod_short](includes/prod_short.md)] zu öffnen und die **Lohntransaktionen importieren** Aktion zu verwenden, um die Datei zu importieren. Während des Importvorgangs ordnen Sie Sachkonten aus QuickBooks den entsprechenden Konten in [!INCLUDE[prod_short](includes/prod_short.md)] zu. Zuletzt buchen Sie die Gehaltsabrechnungstransaktionen in [!INCLUDE[prod_short](includes/prod_short.md)] entsprechend der Kontozuordnung. 

Weitere Informationen finden Sie unter [Gehaltsabrechnungstransaktionen importieren](finance-how-import-payroll-transactions.md).

## Siehe auch
[Anpassen [!INCLUDE[prod_short](includes/prod_short.md)] Erweiterungen nutzen](ui-extensions.md)    
[Finanzen](finance.md)    
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]