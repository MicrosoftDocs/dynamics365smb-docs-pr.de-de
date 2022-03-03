---
title: Design-Details – Struktur der Buchungsschnittstelle
description: Dieses Thema bietet einen Überblick über die globalen Prozeduren und Design-Details in der Struktur der Buchungsschnittstelle.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 06/15/2021
ms.author: edupont
ms.openlocfilehash: ed590455c9edbe5b8727988d4300172223bd2056
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8131925"
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