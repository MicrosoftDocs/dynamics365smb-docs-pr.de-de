---
title: Design-Details – Struktur der Buchungsschnittstelle
description: Dieses Thema bietet einen Überblick über die globalen Prozeduren und Design-Details in der Struktur der Buchungsschnittstelle.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'posting, interface, design'
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="design-details-posting-interface-structure"></a>Designdetails: Buchungs-Schnittstellenstruktur
In [!INCLUDE[prod_short](includes/prod_short.md)]-Buchungsschnittstellenstruktur gibt es mehrere globale Verfahren, die dieselbe Struktur verwenden:  
  
* Anrufprozedurcode RunWithCheck und RunWithoutCheck - generische Buchungsschnittstelle für Gen. Buch.-Blattzeile.  
* CustPostApplyCustLedgEntry - Debitoren-Anwendung buchen, aufgerufen aus Codeunit 226 CustEntry-Gebuchte Posten übernehmen.  
* VendPostApplyVendLedgEntry - Buchen von Kreditoren-Anwendung, aufgerufen aus Codeunit 227 VendEntry-Gebuchte Posten übernehmen.  
* UnapplyCustLedgEntry - Buchen von Debitoren-Anwendung rückgängig machen, aufgerufen aus Codeunit 226 CustEntry-Gebuchte Posten übernehmen.  
* UnapplyVendLedgEntry - Buchen von Kreditoren-Anwendung rückgängig machen, aufgerufen aus Codeunit 227 VendEntry-Gebuchte Posten übernehmen.  
  
## <a name="see-also"></a>Siehe auch
[Designdetails: Buchungs-Modul-Struktur](design-details-posting-engine-structure.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
