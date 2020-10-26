---
title: Business Central Intelligente Cloud-Erweiterungen für Cloudmigration | Microsoft-Dokumentation
description: Verwenden Sie die Cloudmigrationserweiterungen, um Ihre lokalen Daten zu Business Central online zu migrieren. Diese Erweiterungen verschieben Ihre lokalen Daten in die Cloud, sodass Sie Business Central online mit Ihren vorhandenen Daten verwenden können.
author: jenolson
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: jenolson
ms.openlocfilehash: dde6797139f383948d72c52ca1d05298a280087b
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915210"
---
# <a name="intelligent-cloud-extensions-for-cloud-migration"></a><span data-ttu-id="988ab-104">Intelligente Cloud-Erweiterungen für die Cloudmigration</span><span class="sxs-lookup"><span data-stu-id="988ab-104">Intelligent Cloud Extensions for Cloud Migration</span></span>

<span data-ttu-id="988ab-105">Abhängig von Ihrer Lösung vor Ort müssen Sie verschiedene Erweiterungen verwenden, um Ihre Daten mit [!INCLUDE[prodshort](includes/prodshort.md)] online zu verbinden, um Ihre Lösung in die Cloud zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="988ab-105">Depending on your on-premises solution, you must use different extensions to connect your data with [!INCLUDE[prodshort](includes/prodshort.md)] online for purposes of migrating your solution to the cloud.</span></span>  

<span data-ttu-id="988ab-106">Wenn Sie eines der unterstützten lokalen Produkte verwenden, können Sie Ihre Cloudumgebung auf Basis einer produktspezifische Erweiterung konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="988ab-106">If you are using one of the supported on-premises products, you can configure your cloud environment based on a product-specific extension.</span></span><span data-ttu-id="988ab-107"> Sobald Ihre Cloudumgebung konfiguriert ist, haben Sie die Möglichkeit, Daten von Ihrer lokalen Lösung nach [!INCLUDE[prodshort](includes/prodshort.md)] zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="988ab-107"> Once your cloud environment is configured, you will be able to migrate data from your on-premises solution to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="988ab-108">Dadurch können Sie die Möglichkeiten, die die Cloud Ihrem Unternehmen zu bieten hat, in vollen Umfang nutzen, z. B. , erhöhte Einblicke in Ihr Unternehmen, künstliche Intelligenz mehrfacher Gerätzugriff und Zugriff überall und jederzeit.</span><span class="sxs-lookup"><span data-stu-id="988ab-108">This will enable you to take full advantage of what the cloud has to offer your business such as, enhanced insights into your business, artificial intelligence, multiple device access, and anytime, anywhere access.</span></span>  

<span data-ttu-id="988ab-109">Weitere Informationen finden Sie unter [Migrieren lokaler Daten zu Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) im Verwaltungsinhalt für [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="988ab-109">For more information, see [Migrating On-Premises Data to Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) in the administration content for [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>  

## <a name="business-central-on-premises"></a><span data-ttu-id="988ab-110">Lokales Business Central</span><span class="sxs-lookup"><span data-stu-id="988ab-110">Business Central on-premises</span></span>

<span data-ttu-id="988ab-111">Wenn Sie eine lokale Bereitstellung von [!INCLUDE[prodshort](includes/prodshort.md)] verwenden, rufen Sie die Erweiterung **Intelligente Cloud Basis** und die Erweiterung **Business Central intelligente Cloud** ab, und führen Sie dann den Anleitung für die unterstützte Einrichtung von **Cloudmigrationseinrichtung** durch.</span><span class="sxs-lookup"><span data-stu-id="988ab-111">If you are using an on-premises deployment of [!INCLUDE[prodshort](includes/prodshort.md)], get the **Intelligent Cloud Base** extension and the **Business Central Intelligent Cloud** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

## <a name="dynamics-gp"></a><span data-ttu-id="988ab-112">Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="988ab-112">Dynamics GP</span></span>

<span data-ttu-id="988ab-113">Wenn Sie Dynamics GP verwenden, holen Sie sich die Erweiterung **Intelligente Cloud Basis-Erweiterung** und die Erweiterung **Dynamics GP Intelligente Cloud** , und führen Sie dann die Anleitung für die unterstützte Einrichtung der **Cloudmigrationseinrichtung** aus.</span><span class="sxs-lookup"><span data-stu-id="988ab-113">If you are using Dynamics GP,  get the **Intelligent Cloud Base Extension** extension and the **Dynamics GP Intelligent Cloud** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="988ab-114">Die Migration von Dynamics GP mit dem unterstützten Einrichtungsleitfaden **Cloudmigrationseinrichtung** wird derzeit nur für die folgenden Märkte unterstützt: USA, Kanada, Vereinigtes Königreich.</span><span class="sxs-lookup"><span data-stu-id="988ab-114">Migrating from Dynamics GP using the **Cloud Migration Setup** assisted setup guide is currently only supported for the following markets: United States, Canada, United Kingdom.</span></span>

## <a name="dynamics-sl"></a><span data-ttu-id="988ab-115">Dynamics SL</span><span class="sxs-lookup"><span data-stu-id="988ab-115">Dynamics SL</span></span>

<span data-ttu-id="988ab-116">Wenn Sie Dynamics SL verwenden, holen Sie sich die Erweiterung **Intelligente Cloud-Basis** -Erweiterung, die Erweiterung **Microsoft Dynamics SL Intelligente Cloud** und die Erweiterung **Microsoft Dynamics SL-Verlauf-SmartLists** , und führen Sie dann die Anleitung für die unterstützte Einrichtung der **Cloudmigrationseinrichtung** aus.</span><span class="sxs-lookup"><span data-stu-id="988ab-116">If you are using Dynamics SL, get the **Intelligent Cloud Base** extension, the **Microsoft Dynamics SL Intelligent Cloud** extension and the **Microsoft Dynamics SL History SmartLists** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

## <a name="see-also"></a><span data-ttu-id="988ab-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="988ab-117">See Also</span></span>

[<span data-ttu-id="988ab-118">Intelligente Einblicke</span><span class="sxs-lookup"><span data-stu-id="988ab-118">Intelligent Insights</span></span>](about-intelligent-cloud.md)  
[<span data-ttu-id="988ab-119">Intelligente Cloud Base-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="988ab-119">Intelligent Cloud Base Extension</span></span>](ui-extensions-intelligent-cloud.md)  
