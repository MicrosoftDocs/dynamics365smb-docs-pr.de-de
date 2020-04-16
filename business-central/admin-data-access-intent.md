---
title: Verwalten der Datenbank-Zugriffsabsicht in Business Central | Microsoft Docs
description: Ändern Sie die Datenbank-Zugriffsabsicht für Berichte, API-Seiten und Abfragen.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 33b5a3ff604b0ddf7525b89d7a8a82bcfdd7f653
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196381"
---
# <a name="managing-database-access-intent"></a><span data-ttu-id="3e7a6-103">Verwaltung der Datenbank-Zugriffsabsicht</span><span class="sxs-lookup"><span data-stu-id="3e7a6-103">Managing Database Access Intent</span></span> 

<span data-ttu-id="3e7a6-104">Als Superuser oder Administrator können Sie die Datenbankzugriffsabsicht auf Berichte, Seiten vom Typ API und Abfragen ändern, um die Leistung des Dienstes zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="3e7a6-104">As a super user or administrator, you can change the database access intent on reports, pages of the type API, and queries to improve performance of the service.</span></span>

## <a name="overview"></a><span data-ttu-id="3e7a6-105">Matrix</span><span class="sxs-lookup"><span data-stu-id="3e7a6-105">Overview</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="3e7a6-106">kann so eingerichtet werden, dass schreibgeschützte Replikate der primären Datenbank (Lesen und Schreiben) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3e7a6-106">can be set up to use read-only replicas of the primary (read-write) database.</span></span> <span data-ttu-id="3e7a6-107">Die Verwendung der Datenbankreplik reduziert die Belastung der primären Datenbank.</span><span class="sxs-lookup"><span data-stu-id="3e7a6-107">Using the database replica reduces the load on the primary database.</span></span> <span data-ttu-id="3e7a6-108">In einigen Fällen wird dadurch auch die Leistung beim Anzeigen von Daten im Client verbessert.</span><span class="sxs-lookup"><span data-stu-id="3e7a6-108">In some cases, it will also improve the performance when viewing data in the client.</span></span> <span data-ttu-id="3e7a6-109">Replikate sind vorteilhaft für Objekte wie Berichte, Abfragen und API-Seiten, die nur zur Anzeige von Daten, nicht zur Änderung von Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3e7a6-109">Replicas are beneficial for objects, like reports, queries, and API pages, that are used for viewing data only, not modifying data.</span></span>

<span data-ttu-id="3e7a6-110">Wenn Objekte ausgeführt werden, bestimmt die Datenbank-Zugriffsabsicht, ob eine schreibgeschützte Replik, falls vorhanden, oder die primäre Datenbank verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3e7a6-110">When objects run, the database access intent determines whether to use a read-only replica, if one is available, or the primary database.</span></span> <span data-ttu-id="3e7a6-111">Berichte, API-Seiten und Abfragen werden mit einer vordefinierten Datenbank-Zugriffsabsicht entwickelt (siehe [DatabaseAccessIntent-Eigenschaft](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).</span><span class="sxs-lookup"><span data-stu-id="3e7a6-111">Reports, API pages, and queries are developed with a predefined database access intent (see [DatabaseAccessIntent property](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).</span></span>

<span data-ttu-id="3e7a6-112">Auf der Seite **Datenbank-Zugriffsabsichtsliste** können Sie die vordefinierte Datenbank-Zugriffsabsicht für Objekte außer Kraft setzen, wenn sie ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3e7a6-112">The **Database Access Intent List** page lets you override the predefined database access intent for objects when they're run.</span></span>

<span data-ttu-id="3e7a6-113">In Bezug auf die Datenbank wird diese Funktion allgemein als *Lesen Scale-out* bezeichnet. Weitere Informationen über die Ausleseskalierung und die Datenzugriffsabsicht in [!INCLUDE[d365fin](includes/d365fin_md.md)] finden Sie unter [Ausnutzung der Ausleseskalierung für eine bessere Leistung](https://review.docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview?branch=tfs337368-readscaleout) in der Hilfe für Entwickler und IT-Profis unter [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="3e7a6-113">In database terms, this feature is commonly known as *read scale-out*. For more information about read-scale out and data access intent in [!INCLUDE[d365fin](includes/d365fin_md.md)], see [Utilizing Read Scale-Out for Better Performance](https://review.docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview?branch=tfs337368-readscaleout) in the [!INCLUDE[d365fin](includes/d365fin_md.md)] Developer and IT Pro help.</span></span>

## <a name="to-change-the-database-access-intent"></a><span data-ttu-id="3e7a6-114">So ändern Sie die Datenbank-Zugriffsabsicht</span><span class="sxs-lookup"><span data-stu-id="3e7a6-114">To change the database access intent</span></span>

1. <span data-ttu-id="3e7a6-115">Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Datenbankzugriffsabsichtsliste** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="3e7a6-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Database Access Intent List**, and then choose the related link.</span></span>

    <span data-ttu-id="3e7a6-116">Die Seite listet alle Berichte, Seiten und Abfragen auf.</span><span class="sxs-lookup"><span data-stu-id="3e7a6-116">The page lists all reports, pages, and queries.</span></span> <span data-ttu-id="3e7a6-117">Die Spalte **Zugriffsabsicht** enthält einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="3e7a6-117">The **Access Intent** column includes one of the following values:</span></span>

    |<span data-ttu-id="3e7a6-118">**Einstellung**</span><span class="sxs-lookup"><span data-stu-id="3e7a6-118">**Setting**</span></span>|<span data-ttu-id="3e7a6-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3e7a6-119">**Description**</span></span>|  
    |------------|-------------|  
    |<span data-ttu-id="3e7a6-120">**Standard**</span><span class="sxs-lookup"><span data-stu-id="3e7a6-120">**Default**</span></span>|<span data-ttu-id="3e7a6-121">Zeigt an, dass das Objekt die vordefinierte Datenbankzugriffsabsicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3e7a6-121">Indicates that the object uses the predefined database access intent.</span></span>|
    |<span data-ttu-id="3e7a6-122">**Schreiben erlauben**</span><span class="sxs-lookup"><span data-stu-id="3e7a6-122">**Allow Write**</span></span>|<span data-ttu-id="3e7a6-123">Legt das Objekt so fest, dass es die primäre Datenbank verwendet, was bedeutet, dass der Benutzer Daten ändern kann.</span><span class="sxs-lookup"><span data-stu-id="3e7a6-123">Sets the object to use the primary database, allowing the user to modify data.</span></span>|
    |<span data-ttu-id="3e7a6-124">**Nur lesen**</span><span class="sxs-lookup"><span data-stu-id="3e7a6-124">**Read Only**</span></span>|<span data-ttu-id="3e7a6-125">Legen Sie das Objekt so fest, dass die Datenbankreplik verwendet wird, d.h. der Benutzer kann die Daten nur anzeigen und nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="3e7a6-125">Sets the object to use the database replica, which means that the user can only view data, not change data.</span></span>|

2. <span data-ttu-id="3e7a6-126">Wählen Sie die Aktion **Liste bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="3e7a6-126">Choose the **Edit List** action.</span></span>

3. <span data-ttu-id="3e7a6-127">Ändern Sie auf der Seite **Bearbeiten - Datenbank-Zugriffsabsichtsliste** das Feld **Zugriffsabsicht** für die Objekte.</span><span class="sxs-lookup"><span data-stu-id="3e7a6-127">On the **Edit - Database Access Intent List** page, change the **Access Intent** field for the objects.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3e7a6-128">Wenn ein editierbares Objekt, wie die Debitorenkarte, auf **Nur lesen** gesetzt ist, wird die primäre Datenbank unabhängig von der Zugriffsabsicht weiterhin verwendet, so dass die Benutzer wie gewohnt Änderungen vornehmen können.</span><span class="sxs-lookup"><span data-stu-id="3e7a6-128">If an object that is editable, like the Customer Card, is set to **Read Only**, the primary database will still be used, regardless of the access intent, allowing users to make changes as normal.</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="3e7a6-129">Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="3e7a6-129">See Related Training at [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="3e7a6-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e7a6-130">See Also</span></span>
[<span data-ttu-id="3e7a6-131">Geschäftsfunktionen</span><span class="sxs-lookup"><span data-stu-id="3e7a6-131">Business Functionality</span></span>](across-business-functionality.md)  
[<span data-ttu-id="3e7a6-132">Allgemeine Geschäftsfunktionen</span><span class="sxs-lookup"><span data-stu-id="3e7a6-132">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="3e7a6-133">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3e7a6-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="3e7a6-134">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="3e7a6-134">Getting Started</span></span>](product-get-started.md)    

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
