---
title: Beispiel - Inventurauftragszeile mit Nachverfolgungszeilen
description: 'Eine Inventurauftragszeile muss die folgenden bestimmten Daten enthalten:'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: ../../inventory-how-count-inventory-with-documents
ms.openlocfilehash: 8d663849e34f0e5a6a69cf19b17e8cd9d3ab89c7
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2301334"
---
# <a name="example---inventory-order-line-with-tracking-lines"></a>Beispiel - Inventurauftragszeile mit Nachverfolgungszeilen
Eine Inventurauftragszeile enthält die folgenden buchungsrelevanten Daten:  

- Artikelnr.: 80216-V  
- Lagerortcode: BLAU  
- Die Felder "Variantencode" und "Lagerplatzcode" sind beide leer.  

Das Kontrollkästchen Verfolgungszeilen verwenden der Inventurauftragszeile wurde aktiviert, und der Artikel 80216-V wird entsprechend seines Artikelverfolgungscodes stets unter Angabe der Chargennummern gebucht.  

Das Buchungsdatum des Inventurauftragskopfes ist der 31.12.2002.  

Die erwartete Menge des Artikels 80216-V am Lagerort BLAU zum 31.12.2001 beträgt 120 Stück.  

Der Lagerbestand setzt sich aus den folgenden Chargen zusammen:  

## <a name="the-expected-item-tracking-lines"></a>Die erwarteten Artikelverfolgungszeilen:  

|**Chargennr.**|**Menge**|  
|-----------------|------------------|  
|CH1001|80|  
|CH1003|30|  
|CH1006|10|  
|**Summe**|**120**|  

Es wurden folgende Inventurerfassungszeilen für Artikel 80216-V, Lagerortcode BLAU, erfasst:  

## <a name="recorded-lot-nos-on-the-physical-inventory-recording-lines"></a>Erfasste Chargennummern in den Inventurerfassungszeilen:  

|**Chargennr.**|**Menge**|  
|-----------------|------------------|  
|CH1001|80|  
|CH1002|12|  
|CH1003|20|  
|**Summe**|**112**|  

Bei Abschluss des Inventurauftrags berechnet die Anwendung für den Artikel 80216-V am Lagerort BLAU einen zu buchenden Abgang von 8 Stück und erstellt folgende Posten  

## <a name="item-tracking-lines-to-post"></a>Zu buchende Artikelverfolgungszeilen:  

|**Chargennr.**|**Erwartete Menge**|**Erfasste Menge**|**Zu buchende Menge**|  
|-----------------|---------------------------|---------------------------|--------------------------|  
|CH1001|80|80|0|  
|CH1002|0|12|+12|  
|CH1003|30|20|-10|  
|CH1006|10|0|-10|  
|**Summe**|**120**|**112**|**-8**|  

## <a name="see-also"></a>Siehe auch  
 [Inventurauftragszeilen mit Artikelverfolgungszeilen](physical-inventory-order-lines-with-item-tracking-lines.md)  
 [Arbeiten mit Chargennummern und Seriennummern](../../inventory-how-work-item-tracking.md)
