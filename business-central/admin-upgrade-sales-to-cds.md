---
title: Aktualisieren einer Integration mit Dynamics 365 Sales| Microsoft Docs
description: Erfahren Sie, wie Sie Dynamics 365 Business Central für die Integration mit Dynamics 365 Sales vorbereiten.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 2a5f58ac904ea05f4410ac9e1b804df1cb01c609
ms.sourcegitcommit: 4545bb597dd9dc4c563b30af762977ee1d815497
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410668"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a><span data-ttu-id="d85aa-103">Aktualisieren einer Integration mit Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="d85aa-103">Upgrading an Integration with Dynamics 365 Sales</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="d85aa-104">lässt sich mit der [!INCLUDE[d365fin](includes/cds_long_md.md)] integrieren, was die Verbindung und Synchronisierung von Daten mit anderen Dynamics 365-Anwendungen wie [!INCLUDE[crm_md](includes/crm_md.md)] oder sogar selbst erstellten Anwendungen erleichtert.</span><span class="sxs-lookup"><span data-stu-id="d85aa-104">integrates with [!INCLUDE[d365fin](includes/cds_long_md.md)], which makes it easy to connect and synchronize data with other Dynamics 365 applications, such as [!INCLUDE[crm_md](includes/crm_md.md)], or even apps that you build yourself.</span></span> <span data-ttu-id="d85aa-105">Wenn Sie zum ersten Mal integrieren, empfehlen wir Ihnen, dies über [!INCLUDE[d365fin](includes/cds_long_md.md)] zu tun.</span><span class="sxs-lookup"><span data-stu-id="d85aa-105">If you are integrating for the first time, we recommend that you do so through [!INCLUDE[d365fin](includes/cds_long_md.md)].</span></span> <span data-ttu-id="d85aa-106">Weitere Informationen finden Sie unter [Integration mit Common Data Service](admin-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="d85aa-106">For more information, see [Integration with Common Data Service](admin-common-data-service.md).</span></span>

<span data-ttu-id="d85aa-107">Wenn Sie bereits [!INCLUDE[crm_md](includes/crm_md.md)] mit [!INCLUDE[d365fin](includes/d365fin_md.md)] integriert haben, können Sie die Datensynchronisation mit Ihrem Setup fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="d85aa-107">If you have already integrated [!INCLUDE[crm_md](includes/crm_md.md)] with [!INCLUDE[d365fin](includes/d365fin_md.md)], you can continue to synchronize data using your setup.</span></span> <span data-ttu-id="d85aa-108">Wenn Sie jedoch [!INCLUDE[d365fin](includes/d365fin_md.md)] aktualisieren oder Ihre [!INCLUDE[crm_md](includes/crm_md.md)]-Integration ausschalten, müssen Sie sich über [!INCLUDE[d365fin](includes/cds_long_md.md)] verbinden, um sie wieder einzuschalten.</span><span class="sxs-lookup"><span data-stu-id="d85aa-108">However, if you upgrade [!INCLUDE[d365fin](includes/d365fin_md.md)], or turn off your [!INCLUDE[crm_md](includes/crm_md.md)] integration, to turn it on again you must connect through [!INCLUDE[d365fin](includes/cds_long_md.md)].</span></span> 

> [!NOTE]
> <span data-ttu-id="d85aa-109">Eine erneute Verbindung über [!INCLUDE[d365fin](includes/cds_long_md.md)] wendet die Standard-Synchronisationseinstellungen an und überschreibt alle Ihre Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="d85aa-109">Reconnecting through [!INCLUDE[d365fin](includes/cds_long_md.md)] will apply default synchronization settings, and will overwrite any configurations you have.</span></span> <span data-ttu-id="d85aa-110">Es werden zum Beispiel die Standard-Tabellenzuordnungen angewendet.</span><span class="sxs-lookup"><span data-stu-id="d85aa-110">For example, the default table mappings will be applied.</span></span>

## <a name="to-upgrade-your-connection-to-use-common-data-service"></a><span data-ttu-id="d85aa-111">So rüsten Sie Ihre Verbindung auf die Verwendung von Common Data Service auf</span><span class="sxs-lookup"><span data-stu-id="d85aa-111">To upgrade your connection to use Common Data Service</span></span>
1. <span data-ttu-id="d85aa-112">Öffnen Sie die Seite **Microsoft Dynamics 365 Verbindungseinrichtung**, wählen Sie den Schalter **Aktivieren**, um Ihre bestehende Verbindung auf [!INCLUDE[crm_md](includes/crm_md.md)] auszuschalten.</span><span class="sxs-lookup"><span data-stu-id="d85aa-112">Open the **Microsoft Dynamics 365 Connection Setup** page, choose the **Enable** toggle to turn off your existing connection to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
2. <span data-ttu-id="d85aa-113">Öffnen Sie die Seite **Common Data Service Verbindungseinrichtung**, und wählen Sie den Schalter **Freigeben**, um die Verbindung einzuschalten.</span><span class="sxs-lookup"><span data-stu-id="d85aa-113">Open the **Common Data Service Connection Setup** page, and choose the **Enable** toggle to turn on the connection.</span></span>
  
   <span data-ttu-id="d85aa-114">Nachdem Sie die CDS-Verbindung aktiviert haben, wird die Business Central CDS Base Integration Solution auf Common Data Service bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d85aa-114">After you enable the CDS connection, the Business Central CDS Base Integration Solution is deployed to Common Data Service.</span></span>
3. <span data-ttu-id="d85aa-115">Deinstallieren Sie die Integrationslösung Microsoft Dynamics 365 Business Central aus Dynamics 365 Sales, indem Sie wie im Thema [Deinstallieren oder Löschen einer Lösung](/powerapps/developer/common-data-service/uninstall-delete-solution) beschrieben vorgehen.</span><span class="sxs-lookup"><span data-stu-id="d85aa-115">Uninstall the Microsoft Dynamics 365 Business Central Integration solution from your Dynamics 365 Sales following [Uninstall or delete a solution topic](/powerapps/developer/common-data-service/uninstall-delete-solution)</span></span> 

4. <span data-ttu-id="d85aa-116">Wählen Sie auf der Seite Microsoft Dynamics 365 Verbindungseinrichtung den Schalter Aktivieren, um die Verbindung für [!INCLUDE[crm_md](includes/crm_md.md)] einzuschalten.</span><span class="sxs-lookup"><span data-stu-id="d85aa-116">On the Microsoft Dynamics 365 Connection Setup page, choose the Enable toggle to turn on the connection to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
  
   <span data-ttu-id="d85aa-117">Nachdem Sie die Verbindung mit Sales aktiviert haben, wird die Lösung für die Business Central Integration in Sales bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d85aa-117">After you enable the Sales connection, the Business Central Integration Solution is deployed to Sales.</span></span> <span data-ttu-id="d85aa-118">Dies ermöglicht die Integration mit Entitäten, die spezifisch für [!INCLUDE[crm_md](includes/crm_md.md)] sind, wie z.B. Debitorenaufträge, Angebote und Rechnungen.</span><span class="sxs-lookup"><span data-stu-id="d85aa-118">This enables integration with entities that are specific to [!INCLUDE[crm_md](includes/crm_md.md)], such as sales orders, quotes, and invoices.</span></span>
5. <span data-ttu-id="d85aa-119">Wählen Sie **Integrationslösung neu bereitstellen**, um die aktualisierte Business Central Integration Solution zu installieren und zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d85aa-119">Choose **Redeploy Integration Solution** to install and configure the upgraded Business Central Integration Solution.</span></span>
6. <span data-ttu-id="d85aa-120">Wählen Sie auf der Seite **Sales-Verbindungseinrichtung** die Aktion **Standardsynchronisationseinrichtung verwenden**, um die Integrationstabellenzuordnungen für [!INCLUDE[crm_md](includes/crm_md.md)] zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="d85aa-120">On the **Sales Connection Setup** page, choose **Use Default Synchronization Setup** to initialize the integration table mappings for [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="d85aa-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d85aa-121">See Also</span></span>
[<span data-ttu-id="d85aa-122">Integration mit Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="d85aa-122">Integrating with Dynamics 365 Sales</span></span>](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[<span data-ttu-id="d85aa-123">Integrieren in Common Data Service</span><span class="sxs-lookup"><span data-stu-id="d85aa-123">Integrating with Common Data Service</span></span>](admin-common-data-service.md)
