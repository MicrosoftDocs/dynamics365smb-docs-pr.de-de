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
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 1e80b905d96fc2204b61b03c0970257755b9e105
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3787346"
---
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="45d03-103">Designdetails: Buchungs-Schnittstellenstruktur</span><span class="sxs-lookup"><span data-stu-id="45d03-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="45d03-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)]-Buchungsschnittstellenstruktur gibt es mehrere globale Verfahren, die dieselbe Struktur verwenden:</span><span class="sxs-lookup"><span data-stu-id="45d03-104">In the [!INCLUDE[d365fin](includes/d365fin_md.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="45d03-105">Anrufprozedurcode RunWithCheck und RunWithoutCheck - generische Buchungsschnittstelle für Gen.</span><span class="sxs-lookup"><span data-stu-id="45d03-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen.</span></span> <span data-ttu-id="45d03-106">Buch.-Blattzeile.</span><span class="sxs-lookup"><span data-stu-id="45d03-106">Jnl Line.</span></span>  
* <span data-ttu-id="45d03-107">CustPostApplyCustLedgEntry - Debitoren-Anwendung buchen, aufgerufen aus Codeunit 226 CustEntry-Gebuchte Posten übernehmen.</span><span class="sxs-lookup"><span data-stu-id="45d03-107">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="45d03-108">VendPostApplyVendLedgEntry - Buchen von Kreditoren-Anwendung, aufgerufen aus Codeunit 227 VendEntry-Gebuchte Posten übernehmen.</span><span class="sxs-lookup"><span data-stu-id="45d03-108">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="45d03-109">UnapplyCustLedgEntry - Buchen von Debitoren-Anwendung rückgängig machen, aufgerufen aus Codeunit 226 CustEntry-Gebuchte Posten übernehmen.</span><span class="sxs-lookup"><span data-stu-id="45d03-109">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="45d03-110">UnapplyVendLedgEntry - Buchen von Kreditoren-Anwendung rückgängig machen, aufgerufen aus Codeunit 227 VendEntry-Gebuchte Posten übernehmen.</span><span class="sxs-lookup"><span data-stu-id="45d03-110">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="45d03-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45d03-111">See Also</span></span>  
[<span data-ttu-id="45d03-112">Designdetails: Buchungs-Modul-Struktur</span><span class="sxs-lookup"><span data-stu-id="45d03-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)