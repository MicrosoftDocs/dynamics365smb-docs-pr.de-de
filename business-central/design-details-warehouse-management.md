---
title: Designdetails - Lagerhausverwaltung | Microsoft Docs
description: Diese Dokumentation gibt einen Überblick über Konzepte und Prinzipien, die in den Logistikfunktionen in  Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 2f6a84e015ccfd625f3b902281bd8ec59150540f
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1246288"
---
# <a name="design-details-warehouse-management"></a><span data-ttu-id="b06e8-103">Designdetails: Lagerverwaltung</span><span class="sxs-lookup"><span data-stu-id="b06e8-103">Design Details: Warehouse Management</span></span>
<span data-ttu-id="b06e8-104">Diese Dokumentation gibt einen Überblick über Konzepte und Prinzipien, die in den Logistikfunktionen in [!INCLUDE[d365fin](includes/d365fin_md.md)] verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b06e8-104">This documentation gives an overview of the concepts and principles that are used in the Warehouse Management features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="b06e8-105">Erläutert das Design hinter den Zentrallagerfunktionen und wie die Einlagerung mit anderen Lieferkettenfunktionen integriert ist.</span><span class="sxs-lookup"><span data-stu-id="b06e8-105">It explains the design behind central warehouse features and how warehousing integrates with other supply chain features.</span></span>  

<span data-ttu-id="b06e8-106">Um die verschiedenen Komplexitätsniveaus der Lagerhaltung zu unterscheiden, ist diese Dokumentation in zwei allgemeine Gruppen, grundlegende und erweiterte Lagerhaltung aufgeteilt, angegeben durch Abteilungstitel.</span><span class="sxs-lookup"><span data-stu-id="b06e8-106">To differentiate the different complexity levels of the warehousing, this documentation is divided into two general groups, Basic and Advanced warehouse configurations, indicated by section titles.</span></span> <span data-ttu-id="b06e8-107">Diese einfache Unterscheidung umfasst verschiedene Komplexitätsebenen, die durch definierte Produktdetails und Lagerorteinrichtung definiert sind.</span><span class="sxs-lookup"><span data-stu-id="b06e8-107">This simple differentiation covers different complexity levels as defined by product granules and location setup.</span></span> <span data-ttu-id="b06e8-108">Weitere Informationen finden Sie unter [Designdetails: Lagerhaus einrichten](design-details-warehouse-setup.md).</span><span class="sxs-lookup"><span data-stu-id="b06e8-108">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="b06e8-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="b06e8-109">In This Section</span></span>  
[<span data-ttu-id="b06e8-110">Designdetails: Lagerübersicht</span><span class="sxs-lookup"><span data-stu-id="b06e8-110">Design Details: Warehouse Overview</span></span>](design-details-warehouse-overview.md)  
[<span data-ttu-id="b06e8-111">Designdetails: Lagereinrichtung</span><span class="sxs-lookup"><span data-stu-id="b06e8-111">Design Details: Warehouse Setup</span></span>](design-details-warehouse-setup.md)  
[<span data-ttu-id="b06e8-112">Designdetails: Eingehender Lagerfluss</span><span class="sxs-lookup"><span data-stu-id="b06e8-112">Design Details: Inbound Warehouse Flow</span></span>](design-details-inbound-warehouse-flow.md)  
[<span data-ttu-id="b06e8-113">Designdetails: Interner Lagerfluss</span><span class="sxs-lookup"><span data-stu-id="b06e8-113">Design Details: Internal Warehouse Flows</span></span>](design-details-internal-warehouse-flows.md)  
[<span data-ttu-id="b06e8-114">Designdetails: Verfügbarkeit im Lager</span><span class="sxs-lookup"><span data-stu-id="b06e8-114">Design Details: Availability in the Warehouse</span></span>](design-details-availability-in-the-warehouse.md)  
[<span data-ttu-id="b06e8-115">Designdetails: Ausgehender Lagerfluss</span><span class="sxs-lookup"><span data-stu-id="b06e8-115">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="b06e8-116">Designdetails: Integration mit dem Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="b06e8-116">Design Details: Integration with Inventory</span></span>](design-details-integration-with-inventory.md)
