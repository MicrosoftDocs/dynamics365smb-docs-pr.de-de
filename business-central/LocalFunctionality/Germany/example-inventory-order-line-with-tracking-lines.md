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
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 91a6436cf9539c3808d80de80bf97b9b03d0ebea
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "826737"
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
