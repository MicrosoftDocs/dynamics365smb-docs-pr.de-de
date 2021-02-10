---
title: 'Designdetails: Artikelverfolgungsdesign | Microsoft Docs'
description: Dieses Thema zeigt eine Übersicht über Entwurfsdetails für Artikelverfolgung.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 50ae6f2f3538269cc7c82dd2d84644a1a31d7f56
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751355"
---
# <a name="design-details-item-tracking"></a><span data-ttu-id="a216d-103">Designdetails: Artikelnachverfolgung</span><span class="sxs-lookup"><span data-stu-id="a216d-103">Design Details: Item Tracking</span></span>
<span data-ttu-id="a216d-104">Da der Warenfluss in heutigen Lieferketten immer komplexer wird, wird die Möglichkeit, Artikel nachzuverfolgen für die involvierten Unternehmen immer wichtiger.</span><span class="sxs-lookup"><span data-stu-id="a216d-104">As the flow of goods in today’s supply chain becomes more and more complex, the ability to keep track of items is increasingly important to the companies involved.</span></span> <span data-ttu-id="a216d-105">Den Transaktionsfluss eines Artikels zu überwachen ist eine gesetzlich vorgeschriebenes Erfordernis in Bezug auf medizinische und chemische Vorräte, andere Sektoren haben Produkte mit Garantien oder Ablaufdatumsangaben für Kundenservicegründe zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="a216d-105">Monitoring an item’s transaction flow is a legal requirement in the business of medical and chemical supply, but other businesses may want to monitor products with warranties or expiration dates for customer service reasons.</span></span>  

<span data-ttu-id="a216d-106">Ein Artikelverfolgungssystem sollte für eine einfache Handhabung der Serien- und Chargennummern bieten, unter Berücksichtigung, dass jeder Artikel eine eindeutige Ware darstellt, Empfang und Eingang, Lagerord und Verkaufsdatum anzeigt.</span><span class="sxs-lookup"><span data-stu-id="a216d-106">An item tracking system should provide a company with easy handling of serial and lot numbers, considering each unique piece of merchandise: when and where received, where stored, when and where sold.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="a216d-107">hat schrittweise seine Abdeckung dieser Geschäftsanforderung erweitert und stellt heute eine breite Funktionalität und festes Kernstück in den Erweiterungen bereit.einen widerrufen Kernstück bereitstellt, in denen Erweiterungen definieren.</span><span class="sxs-lookup"><span data-stu-id="a216d-107">has gradually expanded its coverage of this business requirement and today provides application-wide functionality and a solid core on which to develop extensions.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="a216d-108">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a216d-108">In This Section</span></span>  
[<span data-ttu-id="a216d-109">Designdetails: Artikelverfolgungsdesign</span><span class="sxs-lookup"><span data-stu-id="a216d-109">Design Details: Item Tracking Design</span></span>](design-details-item-tracking-design.md)  
[<span data-ttu-id="a216d-110">Designdetails: Artikelverfolgungs-Buchungsstruktur</span><span class="sxs-lookup"><span data-stu-id="a216d-110">Design Details: Item Tracking Posting Structure</span></span>](design-details-item-tracking-posting-structure.md)  
[<span data-ttu-id="a216d-111">Designdetails: Aktive vs. historische Artikelverfolgungsposten</span><span class="sxs-lookup"><span data-stu-id="a216d-111">Design Details: Active versus Historic Item Tracking Entries</span></span>](design-details-active-versus-historic-item-tracking-entries.md)  
[<span data-ttu-id="a216d-112">Designdetails – Artikelverfolgungszeilenfenster-Seite</span><span class="sxs-lookup"><span data-stu-id="a216d-112">Design Details: Item Tracking Lines Page</span></span>](design-details-item-tracking-lines-window.md)  
[<span data-ttu-id="a216d-113">Designdetails: Artikelverfolgungsverfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="a216d-113">Design Details: Item Tracking Availability</span></span>](design-details-item-tracking-availability.md)  
[<span data-ttu-id="a216d-114">Designdetails: Artikelverfolgung und Planung</span><span class="sxs-lookup"><span data-stu-id="a216d-114">Design Details: Item Tracking and Planning</span></span>](design-details-item-tracking-and-planning.md)  
[<span data-ttu-id="a216d-115">Designdetails: Artikelverfolgung und Reservierungen</span><span class="sxs-lookup"><span data-stu-id="a216d-115">Design Details: Item Tracking and Reservations</span></span>](design-details-item-tracking-and-reservations.md)  
[<span data-ttu-id="a216d-116">Designdetails: Artikelverfolgung im Lager</span><span class="sxs-lookup"><span data-stu-id="a216d-116">Design Details: Item Tracking in the Warehouse</span></span>](design-details-item-tracking-in-the-warehouse.md)
