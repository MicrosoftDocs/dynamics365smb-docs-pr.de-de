---
title: Microsoft Dynamics GP-Datenmigration| Microsoft Docs
description: "Enthält Informationen über die Dynamics GP-Datenmigrationserweiterung bereit"
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
ms.openlocfilehash: a94afbd0ee689f6bd9157d0b441959f252230f08
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# Die Dynamics GP-Datenmigrations-Erweiterung für Dynamics 365 for Financials
<a id="the-dynamics-gp-data-migration-extension-for-dynamics-365-for-financials" class="xliff"></a>
Diese Erweiterung macht es einfach, Debitoren, Kreditoren und Artikel aus Dynamics GP in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu migrieren. Wenn Ihr Geschäft Dynamics GP heute verwendet, können Sie die Daten exportieren und dann eine unterstützte Einrichtungsanleitung öffnen, um die Daten hochzuladen und in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu migrieren. Weitere Informationen finden Sie unter [Geschäftsdaten aus anderen Finanzsystemen migrieren](upload-data.md).

## Exportieren von Daten aus Dynamics GP
<a id="exporting-data-from-dynamics-gp" class="xliff"></a>
Sie müssen Ihre bestehenden Debitoren, Kreditoren, Artikel und Konten mit der Exportdatenenfunktionalität in Dynamics GP exportiert haben. Zum Zweck des [!INCLUDE[d365fin](includes/d365fin_md.md)] können Sie die folgenden Datentypen exportieren:

* Konto  
* Debitor  
* Option  
* Kreditor  

Die Dynamics GP-Datenmigrationserweiterung ordnet automatisch die exportierten Daten zu, so dass Sie Ihre bestehenden Daten rasch im [!INCLUDE[d365fin](includes/d365fin_md.md)] Unternehmen bereitstehen. Während des Prozesses werden unterstützende Einrichtungsinformationen wie z. B. Buchungsgruppen erstellt. Lagerartikel werden im System mit FIFO als die Bewertungsmethode mit Kosten angezeigt. Konten werden als das Hauptkontosegment von Dynamics GP mit Dimensionen eingerichtet, da sie keine [!INCLUDE[d365fin](includes/d365fin_long_md.md)] Kontensegmente haben.

## Siehe auch
<a id="see-also" class="xliff"></a>
[Geschäftsdaten aus anderen Finanzsystemen migrieren](upload-data.md)  
[Anpassen von [!INCLUDE[d365fin](includes/d365fin_md.md)] mithilfe der Erweiterungen] (ui-extensions.md)  

