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
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b852d6e5d7f96cfba64de219ca414de60cea3a31
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777600"
---
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="0c3aa-103">Designdetails: Buchungs-Schnittstellenstruktur</span><span class="sxs-lookup"><span data-stu-id="0c3aa-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="0c3aa-104">In [!INCLUDE[prod_short](includes/prod_short.md)]-Buchungsschnittstellenstruktur gibt es mehrere globale Verfahren, die dieselbe Struktur verwenden:</span><span class="sxs-lookup"><span data-stu-id="0c3aa-104">In the [!INCLUDE[prod_short](includes/prod_short.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="0c3aa-105">Anrufprozedurcode RunWithCheck und RunWithoutCheck - generische Buchungsschnittstelle für Gen.</span><span class="sxs-lookup"><span data-stu-id="0c3aa-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen.</span></span> <span data-ttu-id="0c3aa-106">Buch.-Blattzeile.</span><span class="sxs-lookup"><span data-stu-id="0c3aa-106">Jnl Line.</span></span>  
* <span data-ttu-id="0c3aa-107">CustPostApplyCustLedgEntry - Debitoren-Anwendung buchen, aufgerufen aus Codeunit 226 CustEntry-Gebuchte Posten übernehmen.</span><span class="sxs-lookup"><span data-stu-id="0c3aa-107">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="0c3aa-108">VendPostApplyVendLedgEntry - Buchen von Kreditoren-Anwendung, aufgerufen aus Codeunit 227 VendEntry-Gebuchte Posten übernehmen.</span><span class="sxs-lookup"><span data-stu-id="0c3aa-108">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="0c3aa-109">UnapplyCustLedgEntry - Buchen von Debitoren-Anwendung rückgängig machen, aufgerufen aus Codeunit 226 CustEntry-Gebuchte Posten übernehmen.</span><span class="sxs-lookup"><span data-stu-id="0c3aa-109">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="0c3aa-110">UnapplyVendLedgEntry - Buchen von Kreditoren-Anwendung rückgängig machen, aufgerufen aus Codeunit 227 VendEntry-Gebuchte Posten übernehmen.</span><span class="sxs-lookup"><span data-stu-id="0c3aa-110">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0c3aa-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c3aa-111">See Also</span></span>  
[<span data-ttu-id="0c3aa-112">Designdetails: Buchungs-Modul-Struktur</span><span class="sxs-lookup"><span data-stu-id="0c3aa-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]