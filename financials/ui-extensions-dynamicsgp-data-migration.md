---
title: Migrieren von Daten von Dynamics GP mit der Datenmigrations-Erweiterung | Microsoft Docs
description: Verwenden Sie die GP-Datenmigrationserweiterung, um Debitoren, Kreditoren, Artikel und Konten von Dynamics GP auf Finance and Operations, Business edition zu migrieren.
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
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: bfd3ca3e28b6eb3efa2a16cc131b508db6bd1590
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="the-dynamics-gp-data-migration-extension-for-finance-and-operations-business-edition"></a>Die Dynamics GP-Datenmigrations-Erweiterung für Finance and Operations, Business edition 
Diese Erweiterung macht es einfach, Debitoren, Kreditoren und Artikel aus Dynamics GP in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu migrieren. Wenn Ihr Geschäft Dynamics GP heute verwendet, können Sie die Daten exportieren und dann eine unterstützte Einrichtungsanleitung öffnen, um die Daten hochzuladen und in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu migrieren. Weitere Informationen finden Sie unter [Geschäftsdaten aus anderen Finanzsystemen importieren](upload-data.md).

## <a name="exporting-data-from-dynamics-gp"></a>Exportieren von Daten aus Dynamics GP
Sie müssen Ihre bestehenden Debitoren, Kreditoren, Artikel und Konten mit der Exportdatenenfunktionalität in Dynamics GP exportiert haben. Zum Zweck des [!INCLUDE[d365fin](includes/d365fin_md.md)] können Sie die folgenden Datentypen exportieren:

* Konto  
* Debitor  
* Option  
* Kreditor  

Die Dynamics GP-Datenmigrationserweiterung ordnet automatisch die exportierten Daten zu, so dass Sie Ihre bestehenden Daten rasch im [!INCLUDE[d365fin](includes/d365fin_md.md)] Unternehmen bereitstehen. Während des Prozesses werden unterstützende Einrichtungsinformationen wie z. B. Buchungsgruppen erstellt. Lagerartikel werden im System mit FIFO als die Bewertungsmethode mit Kosten angezeigt. Konten werden als das Hauptkontosegment von Dynamics GP mit Dimensionen eingerichtet, da sie keine [!INCLUDE[d365fin](includes/d365fin_long_md.md)] Kontensegmente haben.

## <a name="see-also"></a>Siehe auch
[Geschäftsdaten aus anderen Finanzsystemen importieren](upload-data.md)  
[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)  

