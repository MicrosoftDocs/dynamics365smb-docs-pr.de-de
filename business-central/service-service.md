---
title: Service | Microsoft Docs
description: Informationen zur Verwendung der Funktion für die Unterstützung der Arbeitsgänge Werkstatt und Service.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 06f2f8d56d16ef1177bf49e30795cf41af69b8bd
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "798417"
---
# <a name="service-management"></a><span data-ttu-id="ab657-103">Service</span><span class="sxs-lookup"><span data-stu-id="ab657-103">Service Management</span></span>
> [!NOTE]
> <span data-ttu-id="ab657-104">Die Funktionalität, die in diesem Thema und in Vorthemen beschrieben, handelt in der Benutzeroberfläche nur angezeigt, wenn Sie die **Premium** haben.</span><span class="sxs-lookup"><span data-stu-id="ab657-104">Functionality described in this topic and sub topics is only visible in the user interface if you have the **Premium** experience.</span></span> <span data-ttu-id="ab657-105">Weitere Informationen finden Sie unter [Ändern, welche Funktionen angezeigt werden](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="ab657-105">For more information, see [Changing Which Features are Displayed](ui-experiences.md).</span></span>

<span data-ttu-id="ab657-106">Debitoren einen zuverlässigen Service zu bieten, ist ein wesentlicher Bestandteil der Arbeit jedes Unternehmens und eine Grundlage für Debitorenzufriedenheit und Loyalität, zusätzlich zu den Einnahmen.</span><span class="sxs-lookup"><span data-stu-id="ab657-106">Providing ongoing service to customers is an important part of any business and one that can be a source of customer satisfaction and loyalty, in addition to revenue.</span></span> <span data-ttu-id="ab657-107">Die Planung und Steuerung des Service ist jedoch nicht immer einfach. Daher bietet [!INCLUDE[d365fin](includes/d365fin_md.md)] eine Reihe von Tools zur Vereinfachung dieser Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="ab657-107">However, managing and tracking service is not always easy, and [!INCLUDE[d365fin](includes/d365fin_md.md)] provides a set of tools to help.</span></span> <span data-ttu-id="ab657-108">Diese Tools dienen zur Unterstützung der Abläufe in Werkstatt und Außendienst und können in Geschäftsszenarien wie komplexen Debitorendienst- vertriebssystemen, Industrieserviceumgebungen mit Stücklisten und beim umfassenden Einsatz von Servicetechnikern mit Anforderungen für Ersatzteilmanagement verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab657-108">These tools are designed to support repair shop and field service operations, and can be used in business scenarios such as complex customer service distribution systems, industrial service environments with bills of materials, and high volume dispatching of service technicians with requirements for spare parts management.</span></span>  

 <span data-ttu-id="ab657-109">Mit diesen Tools können Sie Folgendes durchführen:</span><span class="sxs-lookup"><span data-stu-id="ab657-109">With these tools you can accomplish the following:</span></span>  

* <span data-ttu-id="ab657-110">Planen von Serviceanrufen und Einrichten von Serviceaufträgen.</span><span class="sxs-lookup"><span data-stu-id="ab657-110">Schedule service calls and set up service orders.</span></span>  
* <span data-ttu-id="ab657-111">Verfolgen von Ersatzteilen und Betriebsstoffen.</span><span class="sxs-lookup"><span data-stu-id="ab657-111">Track repair parts and supplies.</span></span>  
* <span data-ttu-id="ab657-112">Zuweisen von Servicepersonal auf Basis von Qualifikation und Verfügbarkeit.</span><span class="sxs-lookup"><span data-stu-id="ab657-112">Assign service personnel based on skill and availability.</span></span>  
* <span data-ttu-id="ab657-113">Bereitstellen von Serviceschätzungen und Servicerechnungen.</span><span class="sxs-lookup"><span data-stu-id="ab657-113">Provide service estimates and service invoices.</span></span>  

<span data-ttu-id="ab657-114">Zudem können Sie Codierung standardisieren, Verträge einrichten, eine Rabattrichtlinie implementieren und Routenpläne für Servicemitarbeiter erstellen.</span><span class="sxs-lookup"><span data-stu-id="ab657-114">In addition, you can standardize coding, set up contracts, implement a discounting policy, and create route maps for service employees.</span></span>  

<span data-ttu-id="ab657-115">Im Allgemeinen sind beim Servicemanagement zwei Aspekte zu beachten: Konfigurieren und Einrichten des Systems und seine Verwendung für Preisgestaltung, Verträge, Aufträge, Einsatz des Servicepersonals und Projektplaner.</span><span class="sxs-lookup"><span data-stu-id="ab657-115">In general, there are two aspects to service management: configuring and setting up your system, and using it for pricing, contracts, orders, service personnel dispatch, and job scheduler.</span></span>  

<span data-ttu-id="ab657-116">In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.</span><span class="sxs-lookup"><span data-stu-id="ab657-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="ab657-117">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="ab657-117">**To**</span></span>|<span data-ttu-id="ab657-118">**Siehe**</span><span class="sxs-lookup"><span data-stu-id="ab657-118">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="ab657-119">Einrichten von Servicemanagement, einschließlich Fehlercodes, Richtlinien, Standard- dokumenten und -vorlagen.</span><span class="sxs-lookup"><span data-stu-id="ab657-119">Set up Service Management, including fault codes, policies, default documents and templates.</span></span>|[<span data-ttu-id="ab657-120">Einrichten der Serviceverwaltung</span><span class="sxs-lookup"><span data-stu-id="ab657-120">Setting Up Service Management</span></span>](service-setup-service.md)|  
|<span data-ttu-id="ab657-121">Verwalten von Servicepreis, Serviceartikel erstellen und verstehen, wie der Status überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="ab657-121">Manage service pricing, create service items, and understand how to monitor progress.</span></span>|[<span data-ttu-id="ab657-122">Planungsservice</span><span class="sxs-lookup"><span data-stu-id="ab657-122">Planning Service</span></span>](service-plan-service.md)|  
|<span data-ttu-id="ab657-123">Erstellen und Verwalten vertragliche Vereinbarungen zwischen Ihnen und den Debitoren bestehen.</span><span class="sxs-lookup"><span data-stu-id="ab657-123">Create and manage contractual agreements between you and your customers.</span></span>|[<span data-ttu-id="ab657-124">Erfüllen von Serviceverträgen</span><span class="sxs-lookup"><span data-stu-id="ab657-124">Fulfilling Service Contracts</span></span>](service-fulfill-service-contracts.md)|  
|<span data-ttu-id="ab657-125">Bereitstellen von Service, Debitoren und Fakturieren von Serviceaufträgen.</span><span class="sxs-lookup"><span data-stu-id="ab657-125">Provide service to customers, and invoice service orders.</span></span>|[<span data-ttu-id="ab657-126">Bereitstellen von Service</span><span class="sxs-lookup"><span data-stu-id="ab657-126">Delivering Service</span></span>](service-deliver-service.md)|  

## <a name="see-also"></a><span data-ttu-id="ab657-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab657-127">See Also</span></span>  
<span data-ttu-id="ab657-128">[Debitoren verwalten](receivables-manage-receivables.md) </span><span class="sxs-lookup"><span data-stu-id="ab657-128">[Managing Receivables](receivables-manage-receivables.md) </span></span>  
<span data-ttu-id="ab657-129">[Projekte](projects-how-create-jobs.md) </span><span class="sxs-lookup"><span data-stu-id="ab657-129">[Jobs](projects-how-create-jobs.md) </span></span>  
<span data-ttu-id="ab657-130">[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="ab657-130">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] ](index.md)</span></span>

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
