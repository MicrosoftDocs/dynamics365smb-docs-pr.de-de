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
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 772052fc88e0b8be7ec5276600b0c237e2d2f8b2
ms.sourcegitcommit: a76475f124e79440a5bba20577b335c4d50a2d83
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025808"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a><span data-ttu-id="3e4fd-103">Aktualisieren einer Integration mit Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="3e4fd-103">Upgrading an Integration with Dynamics 365 Sales</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="3e4fd-104">lässt sich mit der [!INCLUDE[prod_short](includes/cds_long_md.md)] integrieren, was die Verbindung und Synchronisierung von Daten mit anderen Dynamics 365-Anwendungen wie [!INCLUDE[crm_md](includes/crm_md.md)] oder sogar selbst erstellten Anwendungen erleichtert.</span><span class="sxs-lookup"><span data-stu-id="3e4fd-104">integrates with [!INCLUDE[prod_short](includes/cds_long_md.md)], which makes it easy to connect and synchronize data with other Dynamics 365 applications, such as [!INCLUDE[crm_md](includes/crm_md.md)], or even apps that you build yourself.</span></span> <span data-ttu-id="3e4fd-105">Wenn Sie zum ersten Mal integrieren, empfehlen wir Ihnen, dies über [!INCLUDE[prod_short](includes/cds_long_md.md)] zu tun.</span><span class="sxs-lookup"><span data-stu-id="3e4fd-105">If you are integrating for the first time, we recommend that you do so through [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span> <span data-ttu-id="3e4fd-106">Weitere Informationen finden Sie unter [Integration mit Dataverse](admin-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="3e4fd-106">For more information, see [Integration with Dataverse](admin-common-data-service.md).</span></span>

<span data-ttu-id="3e4fd-107">Wenn Sie bereits [!INCLUDE[crm_md](includes/crm_md.md)] mit [!INCLUDE[prod_short](includes/prod_short.md)] integriert haben, können Sie die Datensynchronisation mit Ihrem Setup fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="3e4fd-107">If you have already integrated [!INCLUDE[crm_md](includes/crm_md.md)] with [!INCLUDE[prod_short](includes/prod_short.md)], you can continue to synchronize data using your setup.</span></span> <span data-ttu-id="3e4fd-108">Wenn Sie jedoch [!INCLUDE[prod_short](includes/prod_short.md)] aktualisieren oder Ihre [!INCLUDE[crm_md](includes/crm_md.md)]-Integration ausschalten, müssen Sie sich über [!INCLUDE[prod_short](includes/cds_long_md.md)] verbinden, um sie wieder einzuschalten.</span><span class="sxs-lookup"><span data-stu-id="3e4fd-108">However, if you upgrade [!INCLUDE[prod_short](includes/prod_short.md)], or turn off your [!INCLUDE[crm_md](includes/crm_md.md)] integration, to turn it on again you must connect through [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span> 

> [!NOTE]
> <span data-ttu-id="3e4fd-109">Eine erneute Verbindung über [!INCLUDE[prod_short](includes/cds_long_md.md)] wendet die Standard-Synchronisationseinstellungen an und überschreibt alle Ihre Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="3e4fd-109">Reconnecting through [!INCLUDE[prod_short](includes/cds_long_md.md)] will apply default synchronization settings, and will overwrite any configurations you have.</span></span> <span data-ttu-id="3e4fd-110">Es werden zum Beispiel die Standard-Tabellenzuordnungen angewendet.</span><span class="sxs-lookup"><span data-stu-id="3e4fd-110">For example, the default table mappings will be applied.</span></span>

## <a name="to-upgrade-your-connection-to-use-dataverse"></a><span data-ttu-id="3e4fd-111">So rüsten Sie Ihre Verbindung auf die Verwendung von Dataverse auf</span><span class="sxs-lookup"><span data-stu-id="3e4fd-111">To upgrade your connection to use Dataverse</span></span>
1. <span data-ttu-id="3e4fd-112">Öffnen Sie die Seite **Microsoft Dynamics 365 Verbindungseinrichtung**, und wählen Sie den Schalter **Aktivieren**, um die Verbindung von [!INCLUDE[crm_md](includes/crm_md.md)] einzuschalten.</span><span class="sxs-lookup"><span data-stu-id="3e4fd-112">Open the **Microsoft Dynamics 365 Connection Setup** page, and then turn off the **Enabled** toggle to disconnect from [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
2. <span data-ttu-id="3e4fd-113">Öffnen Sie die Seite **Dataverse Verbindungseinrichtung**, und wählen Sie den Schalter **Aktivieren**, um die Verbindung mit [!INCLUDE[prod_short](includes/cds_long_md.md)] zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3e4fd-113">Open the **Dataverse Connection Setup** page, and choose the **Enabled** toggle to turn on the connection to [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span>
  
   > [!NOTE]
   > <span data-ttu-id="3e4fd-114">Nachdem Sie die Verbindung aktiviert haben, wird die Business Central CDS Base Integration Solution auf Dataverse bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="3e4fd-114">After you enable the connection, the Business Central Integration Solution is deployed to Dataverse.</span></span>
3. <span data-ttu-id="3e4fd-115">Wählen Sie **Integrationslösung neu bereitstellen**, um die aktualisierte Business Central Integration Solution neu zu installieren und zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="3e4fd-115">Choose **Redeploy Integration Solution** to reinstall the Business Central Integration Solution.</span></span>
4. <span data-ttu-id="3e4fd-116">Aktivieren Sie auf der Seite **Microsoft Dynamics 365 Verbindungseinrichtung** das Kontrollkästchen **Aktiviert**, um eine Verbindung zu [!INCLUDE[crm_md](includes/crm_md.md)] erneut herzustellen.</span><span class="sxs-lookup"><span data-stu-id="3e4fd-116">On the **Microsoft Dynamics 365 Connection Setup** page, turn on the **Enabled** toggle to reconnect to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
  
   > [!NOTE]
   > <span data-ttu-id="3e4fd-117">Nachdem Sie die Verbindung aktiviert haben, wird die Business Central CDS Base Integration Solution auf [!INCLUDE[prod_short](includes/prod_short.md)] bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="3e4fd-117">After you enable the connection, the Business Central Integration Solution is deployed to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="3e4fd-118">Dies ermöglicht die Integration mit Tabellen, die spezifisch für [!INCLUDE[crm_md](includes/crm_md.md)] sind, wie z.B. Debitorenaufträge, Angebote und Rechnungen.</span><span class="sxs-lookup"><span data-stu-id="3e4fd-118">This enables integration with tables that are specific to [!INCLUDE[crm_md](includes/crm_md.md)], such as sales orders, quotes, and invoices.</span></span>
5. <span data-ttu-id="3e4fd-119">Wählen Sie **Integrationslösung neu bereitstellen**, um die aktualisierte Business Central Integration Solution neu zu installieren und zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="3e4fd-119">Choose **Redeploy Integration Solution** to reinstall the Business Central Integration Solution.</span></span>
6. <span data-ttu-id="3e4fd-120">Wählen Sie auf der Seite **Sales-Verbindungseinrichtung** die Aktion **Standardsynchronisationseinrichtung verwenden**, um die Integrationstabellenzuordnungen für [!INCLUDE[crm_md](includes/crm_md.md)] zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="3e4fd-120">On the **Sales Connection Setup** page, choose **Use Default Synchronization Setup** to initialize the integration table mappings for [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="3e4fd-121">Wenn Sie die Aktion **Standard-Synchronisation einrichten** verwenden, werden die Standard-Zuordnungen der Integrationstabellen übernommen.</span><span class="sxs-lookup"><span data-stu-id="3e4fd-121">Using the **Use Default Synchronization Setup** action will apply the default integration table mappings.</span></span> <span data-ttu-id="3e4fd-122">Alle angepassten Zuordnungen werden überschrieben.</span><span class="sxs-lookup"><span data-stu-id="3e4fd-122">All custom mappings will be overwritten.</span></span> <span data-ttu-id="3e4fd-123">Wenn Sie angepasste Zuordnungen haben, die Sie behalten möchten, empfehlen wir Ihnen, diese nach Excel zu exportieren oder mit Ihrem Microsoft-Partner über andere Möglichkeiten zu sprechen, Ihre angepassten Zuordnungen zu behalten.</span><span class="sxs-lookup"><span data-stu-id="3e4fd-123">If you have custom mappings that you want to keep, we recommend that you export them to Excel or talk to your Microsoft partner about other ways to keep your custom mappings.</span></span>    

## <a name="see-also"></a><span data-ttu-id="3e4fd-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e4fd-124">See Also</span></span>
[<span data-ttu-id="3e4fd-125">Integration mit Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="3e4fd-125">Integrating with Dynamics 365 Sales</span></span>](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[<span data-ttu-id="3e4fd-126">Integrieren in Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="3e4fd-126">Integrating with Microsoft Dataverse</span></span>](admin-common-data-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]