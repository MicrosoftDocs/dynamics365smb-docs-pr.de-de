---
title: Fehlerbehebung bei Synchronisationsfehlern | Microsoft Docs
description: Bietet eine Anleitung zum Erkennen und Beheben von Synchronisationsfehlern.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 729a767c0cb4bb330a463e14c7eb6a4f8fd7d909
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304255"
---
# <a name="troubleshooting-synchronization-errors"></a><span data-ttu-id="f7268-103">Fehlerbehebung bei Synchronisationsfehlern</span><span class="sxs-lookup"><span data-stu-id="f7268-103">Troubleshooting Synchronization Errors</span></span>
<span data-ttu-id="f7268-104">Bei der Integration von [!INCLUDE[d365fin](includes/d365fin_md.md)] mit [!INCLUDE[crm_md](includes/crm_md.md)] sind viele bewegliche Teile beteiligt und manchmal laufen die Dinge schief.</span><span class="sxs-lookup"><span data-stu-id="f7268-104">There are lots of moving parts involved in integrating [!INCLUDE[d365fin](includes/d365fin_md.md)] with [!INCLUDE[crm_md](includes/crm_md.md)], and sometimes things go wrong.</span></span> <span data-ttu-id="f7268-105">In diesem Thema werden einige der typischen Fehler aufgeführt, die auftreten, und es werden einige Hinweise zu deren Behebung gegeben.</span><span class="sxs-lookup"><span data-stu-id="f7268-105">This topic points out some of the typical errors that occur and gives some pointers for how to fix them.</span></span>

<span data-ttu-id="f7268-106">Fehler treten häufig auf, wenn ein Benutzer gekoppelte Datensätze bearbeitet hat oder wenn ein Fehler bei der Einrichtung der Integration aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="f7268-106">Errors often occur either because of something that a user has done to coupled records or something is wrong with how the integration is set up.</span></span> <span data-ttu-id="f7268-107">Bei Fehlern im Zusammenhang mit gekoppelten Datensätzen können Benutzer diese selbst beheben.</span><span class="sxs-lookup"><span data-stu-id="f7268-107">For errors related to coupled records, users can resolve those themselves.</span></span> <span data-ttu-id="f7268-108">Diese Fehler werden durch Aktionen verursacht, z. B. Löschen eines Datensatzes in einer, jedoch nicht in beiden Geschäftsanwendungen und anschließendes Synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="f7268-108">These errors are caused by actions such as deleting a record in one, but not both, business apps and then synchronizing.</span></span> <span data-ttu-id="f7268-109">Weitere Informationen finden Sie unter [Den Status einer Synchronisierung anzeigen](admin-how-to-view-synchronization-status.md).</span><span class="sxs-lookup"><span data-stu-id="f7268-109">For more information, see [View the Status of a Synchronization](admin-how-to-view-synchronization-status.md).</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

<span data-ttu-id="f7268-110">Fehler im Zusammenhang mit der Einrichtung der Integration erfordern in der Regel die Aufmerksamkeit eines Administrators.</span><span class="sxs-lookup"><span data-stu-id="f7268-110">Errors that are related to how the integration is set up typically require an administrator's attention.</span></span> <span data-ttu-id="f7268-111">Sie können diese Fehler auf der Seite **Integration von Synchronisationsfehlern** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="f7268-111">You can view these errors on the **Integration Synchronization Errors** page.</span></span> <span data-ttu-id="f7268-112">Beispiele für typische Probleme sind:</span><span class="sxs-lookup"><span data-stu-id="f7268-112">Examples of some typical issues include:</span></span>  
  
* <span data-ttu-id="f7268-113">Die den Benutzern zugewiesenen Berechtigungen und Rollen sind nicht korrekt.</span><span class="sxs-lookup"><span data-stu-id="f7268-113">The permissions and roles assigned to users are not correct.</span></span>  
* <span data-ttu-id="f7268-114">Das Administratorkonto wurde als Integrationsbenutzer angegeben.</span><span class="sxs-lookup"><span data-stu-id="f7268-114">The administrator account was specified as the integration user.</span></span>  
* <span data-ttu-id="f7268-115">Das Kennwort des Integrationsbenutzers erfordert eine Änderung, wenn sich der Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="f7268-115">The integration user’s password is set to require a change when the user signs in.</span></span>  
* <span data-ttu-id="f7268-116">Die Wechselkurse für Währungen sind in der einen oder anderen App nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="f7268-116">The exchange rates for currencies are not specified in one or the other app.</span></span>  
  
<span data-ttu-id="f7268-117">Sie müssen die Fehler manuell beheben. Es gibt jedoch einige Möglichkeiten, wie die Seite Ihnen helfen kann.</span><span class="sxs-lookup"><span data-stu-id="f7268-117">You must manually resolve the errors, but there are a few ways in which the page helps you.</span></span> <span data-ttu-id="f7268-118">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="f7268-118">For example:</span></span>  

* <span data-ttu-id="f7268-119">Die Felder **Quelle**und **Ziel** können Links zu dem Datensatz enthalten, in dem der Fehler gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="f7268-119">The **Source** and **Destination** fields may contain links to the record where the error was found.</span></span> <span data-ttu-id="f7268-120">Klicken Sie auf den Link, um den Datensatz zu öffnen und den Fehler zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="f7268-120">Click the link to open the record and investigate the error.</span></span>  
* <span data-ttu-id="f7268-121">Die Aktion **Einträge löschen, die älter als 7 Tage sind**und die Aktion **Alle Einträge löschen** wird die Liste bereinigen.</span><span class="sxs-lookup"><span data-stu-id="f7268-121">The **Delete Entries Older than 7 Days** and the **Delete All Entries** actions will clean up the list.</span></span> <span data-ttu-id="f7268-122">In der Regel verwenden Sie diese Aktionen, nachdem Sie die Ursache eines Fehlers behoben haben, der viele Datensätze betrifft.</span><span class="sxs-lookup"><span data-stu-id="f7268-122">Typically, you use these actions after you have resolved the cause of an error that affects many records.</span></span> <span data-ttu-id="f7268-123">Vorsicht walten lassen.</span><span class="sxs-lookup"><span data-stu-id="f7268-123">Use caution, however.</span></span> <span data-ttu-id="f7268-124">Durch diese Aktionen werden möglicherweise noch relevante Fehler gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f7268-124">These actions might delete errors that are still relevant.</span></span>

## <a name="see-also"></a><span data-ttu-id="f7268-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7268-125">See Also</span></span>
<span data-ttu-id="f7268-126">[Integrieren in [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)</span><span class="sxs-lookup"><span data-stu-id="f7268-126">[Integrating with [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)</span></span>  
<span data-ttu-id="f7268-127">[Einrichten des Benutzerkontos für die Integration in [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)</span><span class="sxs-lookup"><span data-stu-id="f7268-127">[Setting Up User Accounts for Integrating with [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)</span></span>  
<span data-ttu-id="f7268-128">[Richten Sie eine Verbindung mit [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md) ein</span><span class="sxs-lookup"><span data-stu-id="f7268-128">[Set Up a Connection to [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)</span></span>  
[<span data-ttu-id="f7268-129">Datensätze manuell koppeln und synchronisieren</span><span class="sxs-lookup"><span data-stu-id="f7268-129">Couple and Synchronize Records Manually</span></span>](admin-how-to-couple-and-synchronize-records-manually.md)  
[<span data-ttu-id="f7268-130">Den Status einer Synchronisierung anzeigen</span><span class="sxs-lookup"><span data-stu-id="f7268-130">View the Status of a Synchronization</span></span>](admin-how-to-view-synchronization-status.md)  