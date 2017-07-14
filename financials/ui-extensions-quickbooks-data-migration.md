---
title: QuickBooks-Datenmigration | Microsoft Docs
description: "Enthält Informationen über die QuickBooks-Datenmigrationserweiterung bereit"
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 860ee6b26071e8264deb68bec3b039f384c7be0f
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# Die QuickBooks-Datenmigrations-Erweiterung für Dynamics 365 for Financials
<a id="the-quickbooks-data-migration-extension-for-dynamics-365-for-financials" class="xliff"></a>
Diese Erweiterung macht es einfach, Debitoren, Kreditoren und Artikel aus QuickBooks in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu migrieren. Wenn Ihr Geschäft QuickBooks heute verwendet, können Sie die Daten exportieren und dann eine unterstützte Einrichtungsanleitung öffnen, um die Daten hochzuladen und in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu migrieren.  
Weitere Informationen finden Sie unter [Geschäftsdaten aus anderen Finanzsystemen zu importieren](upload-data.md).

## Exportieren von Daten aus QuickBooks
<a id="exporting-data-from-quickbooks" class="xliff"></a>
Sie müssen einige oder alle Ihrer bestehenden Debitoren, Kreditoren, Lagerartikel und anderen Konten in ein Intuit-Austausch-Format (IIF) exportiert haben. Die QuickBooks-Datenmigrationserweiterung umfasst eine Standardzuordnung von QuickBooks-Daten, sodass Sie Ihre bestehenden Daten verwenden können, um Ihre neue [!INCLUDE[d365fin](includes/d365fin_md.md)] Unternehmung zu testen. Die Standardzuordnung ist in den meisten Fällen ausreichend, aber Sie können die Zuordnung in der unterstützten Einrichtung ändern.  
In QuickBooks umfasst das Dateimenü ein Hilfsprogramm zu den Exporttarifen. Zum Zweck des [!INCLUDE[d365fin](includes/d365fin_md.md)] können Sie die folgenden Listen exportieren:

* Debitorenübersicht  
* Kreditorenübersicht  
* Artikelübersicht  
* Kontenübersicht  

Die exportierten Daten werden IIF-Datei gespeichert, die Sie in [!INCLUDE[d365fin](includes/d365fin_md.md)] hochladen können.

## Siehe auch
<a id="see-also" class="xliff"></a>
[Geschäftsdaten aus anderen Finanzsystemen migrieren](upload-data.md)  
[Anpassen von [!INCLUDE[d365fin](includes/d365fin_md.md)] mithilfe der Erweiterungen] (ui-extensions.md)  

