---
title: Aktualisieren einer Integration mit Dynamics 365 Sales
description: Erfahren Sie, wie Sie Ihre Dynamics 365 Business Central-Integration mit Dynamics 365 Sales auf die neueste Version aktualisieren.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 69ffe6cea05cc28d1950481a07b064a3365f404e
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386699"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a><span data-ttu-id="93688-103">Aktualisieren einer Integration mit Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="93688-103">Upgrading an Integration with Dynamics 365 Sales</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="93688-104">lässt sich mit der [!INCLUDE[prod_short](includes/cds_long_md.md)] integrieren, was die Verbindung und Synchronisierung von Daten mit anderen Dynamics 365-Anwendungen wie [!INCLUDE[crm_md](includes/crm_md.md)] oder sogar selbst erstellten Anwendungen erleichtert.</span><span class="sxs-lookup"><span data-stu-id="93688-104">integrates with [!INCLUDE[prod_short](includes/cds_long_md.md)], which makes it easy to connect and synchronize data with other Dynamics 365 applications, such as [!INCLUDE[crm_md](includes/crm_md.md)], or even apps that you build yourself.</span></span> <span data-ttu-id="93688-105">Wenn Sie zum ersten Mal integrieren, empfehlen wir Ihnen, dies über [!INCLUDE[prod_short](includes/cds_long_md.md)] zu tun.</span><span class="sxs-lookup"><span data-stu-id="93688-105">If you are integrating for the first time, we recommend that you do so through [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span> <span data-ttu-id="93688-106">Weitere Informationen finden Sie unter [Integration mit Dataverse](admin-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="93688-106">For more information, see [Integration with Dataverse](admin-common-data-service.md).</span></span>

<span data-ttu-id="93688-107">Wenn Sie bereits [!INCLUDE[crm_md](includes/crm_md.md)] mit [!INCLUDE[prod_short](includes/prod_short.md)] integriert haben, können Sie die Datensynchronisation mit Ihrem Setup fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="93688-107">If you have already integrated [!INCLUDE[crm_md](includes/crm_md.md)] with [!INCLUDE[prod_short](includes/prod_short.md)], you can continue to synchronize data using your setup.</span></span> <span data-ttu-id="93688-108">Wenn Sie jedoch [!INCLUDE[prod_short](includes/prod_short.md)] aktualisieren oder Ihre [!INCLUDE[crm_md](includes/crm_md.md)]-Integration ausschalten, müssen Sie sich über [!INCLUDE[prod_short](includes/cds_long_md.md)] verbinden, um sie wieder einzuschalten.</span><span class="sxs-lookup"><span data-stu-id="93688-108">However, if you upgrade [!INCLUDE[prod_short](includes/prod_short.md)], or turn off your [!INCLUDE[crm_md](includes/crm_md.md)] integration, to turn it on again you must connect through [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span> 

> [!NOTE]
> <span data-ttu-id="93688-109">Eine erneute Verbindung über [!INCLUDE[prod_short](includes/cds_long_md.md)] wendet die Standard-Synchronisationseinstellungen an und überschreibt alle Ihre Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="93688-109">Reconnecting through [!INCLUDE[prod_short](includes/cds_long_md.md)] will apply default synchronization settings, and will overwrite any configurations you have.</span></span> <span data-ttu-id="93688-110">Es werden zum Beispiel die Standard-Tabellenzuordnungen angewendet.</span><span class="sxs-lookup"><span data-stu-id="93688-110">For example, the default table mappings will be applied.</span></span>

## <a name="to-upgrade-your-connection-to-use-dataverse"></a><span data-ttu-id="93688-111">So rüsten Sie Ihre Verbindung auf die Verwendung von Dataverse auf</span><span class="sxs-lookup"><span data-stu-id="93688-111">To upgrade your connection to use Dataverse</span></span>
1. <span data-ttu-id="93688-112">Öffnen Sie die Seite **Microsoft Dynamics 365 Verbindungseinrichtung**, und wählen Sie den Schalter **Aktivieren**, um die Verbindung von [!INCLUDE[crm_md](includes/crm_md.md)] einzuschalten.</span><span class="sxs-lookup"><span data-stu-id="93688-112">Open the **Microsoft Dynamics 365 Connection Setup** page, and then turn off the **Enabled** toggle to disconnect from [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
2. <span data-ttu-id="93688-113">Öffnen Sie die Seite **Dataverse Verbindungseinrichtung**, und wählen Sie den Schalter **Aktivieren**, um die Verbindung mit [!INCLUDE[prod_short](includes/cds_long_md.md)] zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="93688-113">Open the **Dataverse Connection Setup** page, and choose the **Enabled** toggle to turn on the connection to [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span>
  
   > [!NOTE]
   > <span data-ttu-id="93688-114">Nachdem Sie die Verbindung aktiviert haben, wird die Business Central CDS Base Integration Solution auf Dataverse bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="93688-114">After you enable the connection, the Business Central Integration Solution is deployed to Dataverse.</span></span>
3. <span data-ttu-id="93688-115">Wählen Sie **Integrationslösung neu bereitstellen**, um die aktualisierte Business Central Integration Solution neu zu installieren und zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="93688-115">Choose **Redeploy Integration Solution** to reinstall the Business Central Integration Solution.</span></span>
4. <span data-ttu-id="93688-116">Aktivieren Sie auf der Seite **Microsoft Dynamics 365 Verbindungseinrichtung** das Kontrollkästchen **Aktiviert**, um eine Verbindung zu [!INCLUDE[crm_md](includes/crm_md.md)] erneut herzustellen.</span><span class="sxs-lookup"><span data-stu-id="93688-116">On the **Microsoft Dynamics 365 Connection Setup** page, turn on the **Enabled** toggle to reconnect to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
  
   > [!NOTE]
   > <span data-ttu-id="93688-117">Nachdem Sie die Verbindung aktiviert haben, wird die Business Central CDS Base Integration Solution auf [!INCLUDE[prod_short](includes/prod_short.md)] bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="93688-117">After you enable the connection, the Business Central Integration Solution is deployed to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="93688-118">Dies ermöglicht die Integration mit Tabellen, die spezifisch für [!INCLUDE[crm_md](includes/crm_md.md)] sind, wie z.B. Debitorenaufträge, Angebote und Rechnungen.</span><span class="sxs-lookup"><span data-stu-id="93688-118">This enables integration with tables that are specific to [!INCLUDE[crm_md](includes/crm_md.md)], such as sales orders, quotes, and invoices.</span></span>
5. <span data-ttu-id="93688-119">Wählen Sie **Integrationslösung neu bereitstellen**, um die aktualisierte Business Central Integration Solution neu zu installieren und zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="93688-119">Choose **Redeploy Integration Solution** to reinstall the Business Central Integration Solution.</span></span>
6. <span data-ttu-id="93688-120">Wählen Sie auf der Seite **Sales-Verbindungseinrichtung** die Aktion **Standardsynchronisationseinrichtung verwenden**, um die Integrationstabellenzuordnungen für [!INCLUDE[crm_md](includes/crm_md.md)] zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="93688-120">On the **Sales Connection Setup** page, choose **Use Default Synchronization Setup** to initialize the integration table mappings for [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="93688-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93688-121">See Also</span></span>
[<span data-ttu-id="93688-122">Integration mit Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="93688-122">Integrating with Dynamics 365 Sales</span></span>](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[<span data-ttu-id="93688-123">Integration in Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="93688-123">Integrating with Microsoft Dataverse</span></span>](admin-common-data-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]