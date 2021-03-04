---
title: Design Details - Buchungsschnittstellenstruktur | Microsoft Docs
description: Dieses Thema enthält einen Überblick zu den globalen Verfahren in der Buchungsschnittstellenstruktur.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e306b0caeb58bfe7bd04f93ac64d8b593f70f695
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751255"
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