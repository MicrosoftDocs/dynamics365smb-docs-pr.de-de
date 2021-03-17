---
title: Design Details - Buchungsschnittstellenstruktur | Microsoft Docs
description: Dieses Thema enthält einen Überblick zu den globalen Verfahren in der Buchungsschnittstellenstruktur.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4815e2d4b69095ff61e92d750963879f93dda875
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5390774"
---
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="bb823-103">Designdetails: Buchungs-Schnittstellenstruktur</span><span class="sxs-lookup"><span data-stu-id="bb823-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="bb823-104">In [!INCLUDE[prod_short](includes/prod_short.md)]-Buchungsschnittstellenstruktur gibt es mehrere globale Verfahren, die dieselbe Struktur verwenden:</span><span class="sxs-lookup"><span data-stu-id="bb823-104">In the [!INCLUDE[prod_short](includes/prod_short.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="bb823-105">Anrufprozedurcode RunWithCheck und RunWithoutCheck - generische Buchungsschnittstelle für Gen.</span><span class="sxs-lookup"><span data-stu-id="bb823-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen.</span></span> <span data-ttu-id="bb823-106">Buch.-Blattzeile.</span><span class="sxs-lookup"><span data-stu-id="bb823-106">Jnl Line.</span></span>  
* <span data-ttu-id="bb823-107">CustPostApplyCustLedgEntry - Debitoren-Anwendung buchen, aufgerufen aus Codeunit 226 CustEntry-Gebuchte Posten übernehmen.</span><span class="sxs-lookup"><span data-stu-id="bb823-107">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="bb823-108">VendPostApplyVendLedgEntry - Buchen von Kreditoren-Anwendung, aufgerufen aus Codeunit 227 VendEntry-Gebuchte Posten übernehmen.</span><span class="sxs-lookup"><span data-stu-id="bb823-108">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="bb823-109">UnapplyCustLedgEntry - Buchen von Debitoren-Anwendung rückgängig machen, aufgerufen aus Codeunit 226 CustEntry-Gebuchte Posten übernehmen.</span><span class="sxs-lookup"><span data-stu-id="bb823-109">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="bb823-110">UnapplyVendLedgEntry - Buchen von Kreditoren-Anwendung rückgängig machen, aufgerufen aus Codeunit 227 VendEntry-Gebuchte Posten übernehmen.</span><span class="sxs-lookup"><span data-stu-id="bb823-110">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bb823-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb823-111">See Also</span></span>  
[<span data-ttu-id="bb823-112">Designdetails: Buchungs-Modul-Struktur</span><span class="sxs-lookup"><span data-stu-id="bb823-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]