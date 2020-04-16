---
title: Datenbank-Sperren anzeigen
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 1153ffc97d0f22c889ff23c5a27a8c0446b17018
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196380"
---
# <a name="viewing-database-locks"></a><span data-ttu-id="e0219-102">Anzeigen von Datenbank-Sperren</span><span class="sxs-lookup"><span data-stu-id="e0219-102">Viewing Database Locks</span></span>

## <a name="about-locks"></a><span data-ttu-id="e0219-103">Über Sperren</span><span class="sxs-lookup"><span data-stu-id="e0219-103">About Locks</span></span>

<span data-ttu-id="e0219-104">Die Datenbanksperre steuert den gleichzeitigen Zugriff mehrerer Benutzer auf dieselben Daten.</span><span class="sxs-lookup"><span data-stu-id="e0219-104">Database locking controls access by multiple users to the same data at the same time.</span></span> <span data-ttu-id="e0219-105">Um eine Transaktion gegen andere Transaktionen zu schützen, die dieselben Daten ändern, sperrt die erste Transaktion die Daten.</span><span class="sxs-lookup"><span data-stu-id="e0219-105">To protect a transaction against other transactions modifying the same data, the first transaction puts a lock on the data.</span></span> <span data-ttu-id="e0219-106">Die Sperre bleibt bestehen, bis die Transaktion abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="e0219-106">The lock remains until the transaction's done.</span></span>

<span data-ttu-id="e0219-107">Benutzer können für den Abschluss von Transaktionen mit den gesperrten Daten gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="e0219-107">Users may be blocked from completing transactions on the locked data.</span></span> <span data-ttu-id="e0219-108">Sie erhalten in der Regel eine Meldung, die den Sperrzustand anzeigt.</span><span class="sxs-lookup"><span data-stu-id="e0219-108">They'll typically get a message that indicates the lock condition.</span></span>

## <a name="to-view-database-locks"></a><span data-ttu-id="e0219-109">So zeigen Sie Datenbanksperren an</span><span class="sxs-lookup"><span data-stu-id="e0219-109">To view database locks</span></span>

<span data-ttu-id="e0219-110">Wählen Sie das Symbol ![Seite suchen oder Bericht](media/ui-search/search_small.png "Suchen Sie nach dem Symbol Seite oder Bericht"), geben Sie **Datenbanksperren** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="e0219-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Database Locks**, and then choose the related link.</span></span>

<span data-ttu-id="e0219-111">Die Seite **Datenbanksperren** zeigt eine Momentaufnahme aller aktuellen Datenbanksperren.</span><span class="sxs-lookup"><span data-stu-id="e0219-111">The **Database Locks** page gives snapshot of all current database locks.</span></span>

<span data-ttu-id="e0219-112">Weitere Informationen über Datenbanksperren finden Sie unter [Überwachung von Datenbanksperren](/dynamics365/business-central/a/dev-itpro/administration/monitor-database-locks) in der Hilfe für Business Central Entwickler und IT Pro.</span><span class="sxs-lookup"><span data-stu-id="e0219-112">For more information about database locking, see [Monitoring Database Locks](/dynamics365/business-central/a/dev-itpro/administration/monitor-database-locks) in the Business Central Developer and IT Pro help.</span></span>

## <a name="see-also"></a><span data-ttu-id="e0219-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0219-113">See Also</span></span>

[<span data-ttu-id="e0219-114">Datenbanksperren überwachen</span><span class="sxs-lookup"><span data-stu-id="e0219-114">Monitor Database Locks</span></span>](/dynamics365/business-central/a/dev-itpro/administration/monitor-database-locks) 
