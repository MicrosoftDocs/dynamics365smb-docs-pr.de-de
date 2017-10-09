---
title: QuickBooks-Migrations-Erweiterung verwenden | Microsoft Docs
description: Beschreibt, wie die Erweiterung verwendet wird, um Debitoren, Kreditoren, Artikel und Konten aus QuickBooks Desktop auf Dynamics 365 for Financials zu importieren.
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 4775c945a7721b8f4e52a187840a585396611e47
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="the-quickbooks-data-migration-extension-for-dynamics-365-for-financials"></a>Die QuickBooks-Datenmigrations-Erweiterung für Dynamics 365 for Financials
Diese Erweiterung macht es einfach, Debitoren, Kreditoren und Artikel aus QuickBooks Desktop in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu migrieren. Wenn Ihr Geschäft QuickBooks heute verwendet, können Sie die Daten exportieren und dann eine unterstützte Einrichtungsanleitung öffnen, um die Daten hochzuladen und in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu migrieren.  
Weitere Informationen finden Sie unter [Geschäftsdaten aus anderen Finanzsystemen zu importieren](upload-data.md).

## <a name="exporting-data-from-quickbooks-desktop"></a>Exportieren von Daten aus QuickBooks Desktop
Sie müssen einige oder alle Ihrer bestehenden Debitoren, Kreditoren, Lagerartikel und anderen Konten in ein Intuit-Austausch-Format (IIF) exportiert haben. Die QuickBooks-Datenmigrationserweiterung umfasst eine Standardzuordnung von QuickBooks-Daten, sodass Sie Ihre bestehenden Daten verwenden können, um Ihre neue [!INCLUDE[d365fin](includes/d365fin_md.md)] Unternehmung zu testen. Die Standardzuordnung ist in den meisten Fällen ausreichend, aber Sie können die Zuordnung in der unterstützten Einrichtung ändern.  
In QuickBooks umfasst das Dateimenü ein Hilfsprogramm zu den Exporttarifen. Zum Zweck des [!INCLUDE[d365fin](includes/d365fin_md.md)] können Sie die folgenden Listen exportieren:

* Debitorenübersicht  
* Kreditorenübersicht  
* Artikelübersicht  
* Kontenübersicht  

Die exportierten Daten werden IIF-Datei gespeichert, die Sie in [!INCLUDE[d365fin](includes/d365fin_md.md)] hochladen können.

## <a name="finding-the-quickbooks-data-migration-extension"></a>Die QuickBooks-Datenmigrations-Erweiterung suchen
Die QuickBooks-Datenmigrationserweiterung ist eingerichtet und vorbereitet, um als integrierter Teil des unterstützten Setups bei der Datenmigration zu helfen. Wenn Sie bereit sind jetzt anzufangen, und die Daten aus QuickBooks exportiert haben, wähen Sie ![Seite oder Bericht suchen](media/ui-search/search_small.png "Seiten- oder Berichtssymbol suchen") und geben **Unterstützte Einrichtung** ein und wählen dann den zugehörigen Link aus. Wählen Sie **Migrieren von Geschäftsdaten** und anschließend führen Sie die Schritte im Handbuch aus.  

## <a name="see-also"></a>Siehe auch
[Geschäftsdaten aus anderen Finanzsystemen importieren](upload-data.md)  
[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)  

