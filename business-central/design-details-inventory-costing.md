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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 97aa9dc23397403b74fc8f1c65d302733ab3301c
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751480"
---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="38028-103">Designdetails: Lagerkostenberechnung</span><span class="sxs-lookup"><span data-stu-id="38028-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="38028-104">Diese Dokumentation stellt einen detaillierten technischen Einblick in die Konzepte und Prinzipien bereit, die in den Lagerkostenfunktionen in [!INCLUDE[prod_short](includes/prod_short.md)] verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="38028-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

<span data-ttu-id="38028-105">Die Kostenverwaltung, die auch als "Lagerabgang" bezeichnet wird, dient zum Erfassen und Melden der Betriebskosten eines Unternehmens.</span><span class="sxs-lookup"><span data-stu-id="38028-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="38028-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="38028-106">In This Section</span></span>  
[<span data-ttu-id="38028-107">Designdetails: Kostenberechnungsmethoden</span><span class="sxs-lookup"><span data-stu-id="38028-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="38028-108">Designdetails: Artikelausgleich</span><span class="sxs-lookup"><span data-stu-id="38028-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="38028-109">Designdetails: Bekannte Artikelanwendungsprobleme</span><span class="sxs-lookup"><span data-stu-id="38028-109">Design Details: Known Item Application Issue</span></span>](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[<span data-ttu-id="38028-110">Designdetails: Kostenregulierung</span><span class="sxs-lookup"><span data-stu-id="38028-110">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="38028-111">Designdetails: Buchungsdatum auf Ausgleichs-Wertposten</span><span class="sxs-lookup"><span data-stu-id="38028-111">Design Details: Posting Date on Adjustment Value Entry</span></span>](design-details-inventory-adjustment-value-entry-posting-date.md)  
[<span data-ttu-id="38028-112">Designdetails: Soll-Kosten-Buchen</span><span class="sxs-lookup"><span data-stu-id="38028-112">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="38028-113">Designdetails: Durchschnittskosten</span><span class="sxs-lookup"><span data-stu-id="38028-113">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="38028-114">Designdetails: Abweichung</span><span class="sxs-lookup"><span data-stu-id="38028-114">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="38028-115">Designdetails: Rundung</span><span class="sxs-lookup"><span data-stu-id="38028-115">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="38028-116">Designdetails: Kostenkomponenten</span><span class="sxs-lookup"><span data-stu-id="38028-116">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="38028-117">Designdetails: Bestandsperioden</span><span class="sxs-lookup"><span data-stu-id="38028-117">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="38028-118">Designdetails: Bestandsbuchung</span><span class="sxs-lookup"><span data-stu-id="38028-118">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="38028-119">Designdetails: Fertigungsauftragsbuchung</span><span class="sxs-lookup"><span data-stu-id="38028-119">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="38028-120">Designdetails: Montageauftragsbuchung</span><span class="sxs-lookup"><span data-stu-id="38028-120">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="38028-121">Designdetails: Abgleich mit der Finanzbuchhaltung</span><span class="sxs-lookup"><span data-stu-id="38028-121">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="38028-122">Designdetails: Konten in der Finanzbuchhaltung</span><span class="sxs-lookup"><span data-stu-id="38028-122">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="38028-123">Designdetails: Bestandsbewertung</span><span class="sxs-lookup"><span data-stu-id="38028-123">Design Details: Inventory Valuation</span></span>](design-details-inventory-valuation.md)  
[<span data-ttu-id="38028-124">Designdetails: Neubewertung</span><span class="sxs-lookup"><span data-stu-id="38028-124">Design Details: Revaluation</span></span>](design-details-revaluation.md)
