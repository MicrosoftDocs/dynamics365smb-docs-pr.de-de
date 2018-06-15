---
title: Migrieren von Daten von Dynamics GP mit der Datenmigrations-Erweiterung | Microsoft Docs
description: Verwenden Sie die GP-Datenmigrationserweiterung, um Debitoren, Kreditoren, Artikel und Konten von Dynamics GP auf Business Central zu migrieren.
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 3761bdb0d6b9a51ed309ac4189ff263de76f4679
ms.contentlocale: de-de
ms.lasthandoff: 05/17/2018

---
# <a name="the-dynamics-gp-data-migration-extension-for-business-central"></a><span data-ttu-id="adad4-103">Die Dynamics GP Datenmigrations-Erweiterung für Business Central</span><span class="sxs-lookup"><span data-stu-id="adad4-103">The Dynamics GP Data Migration Extension for Business Central</span></span> 
<span data-ttu-id="adad4-104">Diese Erweiterung macht es einfach, Debitoren, Kreditoren und Artikel aus Dynamics GP in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="adad4-104">This extension makes it easy to migrate customers, vendors, inventory items, and accounts from Dynamics GP to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="adad4-105">Wenn Ihr Geschäft Dynamics GP heute verwendet, können Sie die Daten exportieren und dann eine unterstützte Einrichtungsanleitung öffnen, um die Daten hochzuladen und in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="adad4-105">If your business uses Dynamics GP today, you can export the relevant master records and then open an assisted setup guide to add the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="adad4-106">Weitere Informationen finden Sie unter [Geschäftsdaten aus anderen Finanzsystemen zu importieren](across-import-data-configuration-packages.md).</span><span class="sxs-lookup"><span data-stu-id="adad4-106">For more information, see [Importing Business Data from Other Finance Systems](across-import-data-configuration-packages.md).</span></span>

## <a name="exporting-data-from-dynamics-gp"></a><span data-ttu-id="adad4-107">Exportieren von Daten aus Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="adad4-107">Exporting Data from Dynamics GP</span></span>
<span data-ttu-id="adad4-108">Sie müssen Ihre bestehenden Debitoren, Kreditoren, Artikel und Konten mit der Exportdatenenfunktionalität in Dynamics GP exportiert haben.</span><span class="sxs-lookup"><span data-stu-id="adad4-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to a file, using the Dynamics GP functionality for data export.</span></span> <span data-ttu-id="adad4-109">Zum Zweck des [!INCLUDE[d365fin](includes/d365fin_md.md)] können Sie die folgenden Datentypen exportieren:</span><span class="sxs-lookup"><span data-stu-id="adad4-109">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following types of data:</span></span>

* <span data-ttu-id="adad4-110">Konto</span><span class="sxs-lookup"><span data-stu-id="adad4-110">Account</span></span>  
* <span data-ttu-id="adad4-111">Debitor</span><span class="sxs-lookup"><span data-stu-id="adad4-111">Customer</span></span>  
* <span data-ttu-id="adad4-112">Option</span><span class="sxs-lookup"><span data-stu-id="adad4-112">Item</span></span>  
* <span data-ttu-id="adad4-113">Kreditor</span><span class="sxs-lookup"><span data-stu-id="adad4-113">Vendor</span></span>  

<span data-ttu-id="adad4-114">Die Dynamics GP-Datenmigrationserweiterung ordnet automatisch die exportierten Daten zu, so dass Sie Ihre bestehenden Daten rasch im [!INCLUDE[d365fin](includes/d365fin_md.md)] Unternehmen bereitstehen.</span><span class="sxs-lookup"><span data-stu-id="adad4-114">The Dynamics GP Data Migration extension automatically maps the exported data so that your data is quickly available to you in your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="adad4-115">Während des Prozesses werden unterstützende Einrichtungsinformationen wie z. B. Buchungsgruppen erstellt.</span><span class="sxs-lookup"><span data-stu-id="adad4-115">During the process, supporting setup information is created, such as posting groups.</span></span> <span data-ttu-id="adad4-116">Lagerartikel werden im System mit FIFO als die Bewertungsmethode mit Kosten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="adad4-116">Inventory items will be brought into the system with FIFO as the cost valuation method.</span></span> <span data-ttu-id="adad4-117">Konten werden als das Hauptkontosegment von Dynamics GP mit Dimensionen eingerichtet, da sie keine [!INCLUDE[d365fin](includes/d365fin_long_md.md)] Kontensegmente haben.</span><span class="sxs-lookup"><span data-stu-id="adad4-117">Accounts will be set up as the main account segment from Dynamics GP with dimensions, because [!INCLUDE[d365fin](includes/d365fin_long_md.md)] does not have account segments.</span></span>

## <a name="see-also"></a><span data-ttu-id="adad4-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="adad4-118">See Also</span></span>
[<span data-ttu-id="adad4-119">Geschäftsdaten aus anderen Finanzsystemen importieren</span><span class="sxs-lookup"><span data-stu-id="adad4-119">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="adad4-120">[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="adad4-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

