---
title: QuickBooks-Migrations-Erweiterung verwenden | Microsoft Docs
description: Beschreibt, wie die Erweiterung verwendet wird, um Debitoren, Kreditoren, Artikel und Konten aus QuickBooks-Desktop auf Dynamics 365 for Financials zu importieren.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 37d90316ea0be5489fb5abe33645de3fe0d3cf90
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2017

---
# <a name="the-quickbooks-data-migration-extension-for-dynamics-365-for-financials"></a><span data-ttu-id="779b4-103">Die QuickBooks-Datenmigrations-Erweiterung für Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="779b4-103">The QuickBooks Data Migration Extension for Dynamics 365 for Financials</span></span>
<span data-ttu-id="779b4-104">Diese Erweiterung macht es einfach, Debitoren, Kreditoren und Artikel aus QuickBooks in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="779b4-104">This extension makes it easy to migrate customers, vendors, items, and accounts from QuickBooks to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="779b4-105">Wenn Ihr Geschäft QuickBooks heute verwendet, können Sie die Daten exportieren und dann eine unterstützte Einrichtungsanleitung öffnen, um die Daten hochzuladen und in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="779b4-105">If your business uses QuickBooks today, you can export the relevant information and then open an assisted setup guide to upload the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
<span data-ttu-id="779b4-106">Weitere Informationen finden Sie unter [Geschäftsdaten aus anderen Finanzsystemen zu importieren](upload-data.md).</span><span class="sxs-lookup"><span data-stu-id="779b4-106">For more information, see [Importing Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-quickbooks"></a><span data-ttu-id="779b4-107">Exportieren von Daten aus QuickBooks</span><span class="sxs-lookup"><span data-stu-id="779b4-107">Exporting Data from QuickBooks</span></span>
<span data-ttu-id="779b4-108">Sie müssen einige oder alle Ihrer bestehenden Debitoren, Kreditoren, Lagerartikel und anderen Konten in ein Intuit-Austausch-Format (IIF) exportiert haben.</span><span class="sxs-lookup"><span data-stu-id="779b4-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to an Intuit Interchange Format (IIF) file.</span></span> <span data-ttu-id="779b4-109">Die QuickBooks-Datenmigrationserweiterung umfasst eine Standardzuordnung von QuickBooks-Daten, sodass Sie Ihre bestehenden Daten verwenden können, um Ihre neue [!INCLUDE[d365fin](includes/d365fin_md.md)] Unternehmung zu testen.</span><span class="sxs-lookup"><span data-stu-id="779b4-109">The QuickBooks Data Migration extension includes a default mapping of QuickBooks data so that you can use your existing data to test your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="779b4-110">Die Standardzuordnung ist in den meisten Fällen ausreichend, aber Sie können die Zuordnung in der unterstützten Einrichtung ändern.</span><span class="sxs-lookup"><span data-stu-id="779b4-110">The default mapping will be sufficient in the vast majority of cases, but you can change the mapping in the assisted setup guide.</span></span>  
<span data-ttu-id="779b4-111">In QuickBooks umfasst das Dateimenü ein Hilfsprogramm zu den Exporttarifen.</span><span class="sxs-lookup"><span data-stu-id="779b4-111">In QuickBooks, the File menu includes a utility to export lists.</span></span> <span data-ttu-id="779b4-112">Zum Zweck des [!INCLUDE[d365fin](includes/d365fin_md.md)] können Sie die folgenden Listen exportieren:</span><span class="sxs-lookup"><span data-stu-id="779b4-112">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following lists:</span></span>

* <span data-ttu-id="779b4-113">Debitorenübersicht</span><span class="sxs-lookup"><span data-stu-id="779b4-113">Customer List</span></span>  
* <span data-ttu-id="779b4-114">Kreditorenübersicht</span><span class="sxs-lookup"><span data-stu-id="779b4-114">Vendor List</span></span>  
* <span data-ttu-id="779b4-115">Artikelübersicht</span><span class="sxs-lookup"><span data-stu-id="779b4-115">Item List</span></span>  
* <span data-ttu-id="779b4-116">Kontenübersicht</span><span class="sxs-lookup"><span data-stu-id="779b4-116">Account List</span></span>  

<span data-ttu-id="779b4-117">Die exportierten Daten werden IIF-Datei gespeichert, die Sie in [!INCLUDE[d365fin](includes/d365fin_md.md)] hochladen können.</span><span class="sxs-lookup"><span data-stu-id="779b4-117">The exported data is saved as an IIF file that you can then upload to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="779b4-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="779b4-118">See Also</span></span>
[<span data-ttu-id="779b4-119">Geschäftsdaten aus anderen Finanzsystemen migrieren</span><span class="sxs-lookup"><span data-stu-id="779b4-119">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="779b4-120">[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="779b4-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

