---
title: Designdetails - Bestandkosten | Microsoft Docs
description: Diese Dokumentation stellt einen detaillierten technischen Einblick in die Konzepte und Prinzipien bereit, die in den Lagerkostenfunktionen in Business Central verwendet werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, costing
ms.date: 11/25/2019
ms.author: sgroespe
ms.openlocfilehash: 667adfcc9c470a9d4dbf26923fe5e6edfc7ed85a
ms.sourcegitcommit: e97e1df1f5d7b1d8af477580960a8737fcea4d16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832191"
---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="5f6f9-103">Designdetails: Lagerkostenberechnung</span><span class="sxs-lookup"><span data-stu-id="5f6f9-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="5f6f9-104">Diese Dokumentation stellt einen detaillierten technischen Einblick in die Konzepte und Prinzipien bereit, die in den Lagerkostenfunktionen in [!INCLUDE[d365fin](includes/d365fin_md.md)] verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f6f9-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="5f6f9-105">Die Kostenverwaltung, die auch als "Lagerabgang" bezeichnet wird, dient zum Erfassen und Melden der Betriebskosten eines Unternehmens.</span><span class="sxs-lookup"><span data-stu-id="5f6f9-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="5f6f9-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="5f6f9-106">In This Section</span></span>  
[<span data-ttu-id="5f6f9-107">Designdetails: Kostenberechnungsmethoden</span><span class="sxs-lookup"><span data-stu-id="5f6f9-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="5f6f9-108">Designdetails: Artikelausgleich</span><span class="sxs-lookup"><span data-stu-id="5f6f9-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="5f6f9-109">Designdetails: Bekannte Artikelanwendungsprobleme</span><span class="sxs-lookup"><span data-stu-id="5f6f9-109">Design Details: Known Item Application Issue</span></span>](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[<span data-ttu-id="5f6f9-110">Designdetails: Kostenregulierung</span><span class="sxs-lookup"><span data-stu-id="5f6f9-110">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="5f6f9-111">Designdetails: Buchungsdatum auf Ausgleichs-Wertposten</span><span class="sxs-lookup"><span data-stu-id="5f6f9-111">Design Details: Posting Date on Adjustment Value Entry</span></span>](design-details-inventory-adjustment-value-entry-posting-date.md)  
[<span data-ttu-id="5f6f9-112">Designdetails: Soll-Kosten-Buchen</span><span class="sxs-lookup"><span data-stu-id="5f6f9-112">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="5f6f9-113">Designdetails: Durchschnittskosten</span><span class="sxs-lookup"><span data-stu-id="5f6f9-113">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="5f6f9-114">Designdetails: Abweichung</span><span class="sxs-lookup"><span data-stu-id="5f6f9-114">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="5f6f9-115">Designdetails: Rundung</span><span class="sxs-lookup"><span data-stu-id="5f6f9-115">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="5f6f9-116">Designdetails: Kostenkomponenten</span><span class="sxs-lookup"><span data-stu-id="5f6f9-116">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="5f6f9-117">Designdetails: Bestandsperioden</span><span class="sxs-lookup"><span data-stu-id="5f6f9-117">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="5f6f9-118">Designdetails: Bestandsbuchung</span><span class="sxs-lookup"><span data-stu-id="5f6f9-118">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="5f6f9-119">Designdetails: Fertigungsauftragsbuchung</span><span class="sxs-lookup"><span data-stu-id="5f6f9-119">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="5f6f9-120">Designdetails: Montageauftragsbuchung</span><span class="sxs-lookup"><span data-stu-id="5f6f9-120">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="5f6f9-121">Designdetails: Abgleich mit der Finanzbuchhaltung</span><span class="sxs-lookup"><span data-stu-id="5f6f9-121">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="5f6f9-122">Designdetails: Konten in der Finanzbuchhaltung</span><span class="sxs-lookup"><span data-stu-id="5f6f9-122">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="5f6f9-123">Designdetails: Bestandsbewertung</span><span class="sxs-lookup"><span data-stu-id="5f6f9-123">Design Details: Inventory Valuation</span></span>](design-details-inventory-valuation.md)  
[<span data-ttu-id="5f6f9-124">Designdetails: Neubewertung</span><span class="sxs-lookup"><span data-stu-id="5f6f9-124">Design Details: Revaluation</span></span>](design-details-revaluation.md)
