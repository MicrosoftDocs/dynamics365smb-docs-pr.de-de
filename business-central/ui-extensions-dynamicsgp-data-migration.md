---
title: Daten von Dynamics GP vor 15.3 migrieren | Microsoft Docs
description: Vor dem Update 15.3 konnten Sie die Dynamics GP-Datenmigrationserweiterung verwenden, um Debitoren, Kreditoren, Lagerartikel, Sachkonten, Transaktionen zu offenen Verbindlichkeiten und Forderungen von Dynamics GP nach Business Central zu migrieren.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 10/01/2020
ms.author: edupont
ROBOTS: NOINDEX
ms.openlocfilehash: a8f6c35d031cdbe6376ed57ea9ba2e9ce79188b4
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757267"
---
# <a name="the-dynamics-gp-data-migration-extension"></a><span data-ttu-id="a7e41-103">Die Dynamics GP-Datenmigrations-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="a7e41-103">The Dynamics GP Data Migration Extension</span></span>

> [!NOTE]
> <span data-ttu-id="a7e41-104">Diese Erweiterung ist im 15.3-Update veraltet.</span><span class="sxs-lookup"><span data-stu-id="a7e41-104">This extension is deprecated in the 15.3 update.</span></span> <span data-ttu-id="a7e41-105">Es wird empfohlen, dass Benutzer, die von Dynamics GP migrieren möchten, stattdessen ab jetzt den **Cloudmigration**-Assistenten verwenden.</span><span class="sxs-lookup"><span data-stu-id="a7e41-105">We recommend that users who want to migrate from Dynamics GP start using the **Cloud Migration** wizard instead.</span></span> <span data-ttu-id="a7e41-106">Die Erweiterung **Cloudmigration** hat robustere Funktionen und bring mehr Daten von Dynamics GP nach Business Central.</span><span class="sxs-lookup"><span data-stu-id="a7e41-106">The **Cloud Migration** extension has more robust functionality and brings more data into Business Central from Dynamics GP.</span></span> <span data-ttu-id="a7e41-107">Weitere Informationen finden Sie unter [Von Dynamics GP zu Business Central Online migrieren](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp) im Verwaltungsinhalt für [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="a7e41-107">For more information, see [Migrate to Business Central Online from Dynamics GP](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp) in the administration content for [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="a7e41-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7e41-108">See Also</span></span>

[<span data-ttu-id="a7e41-109">Intelligente Cloud-Erweiterungen für die Cloudmigration</span><span class="sxs-lookup"><span data-stu-id="a7e41-109">Intelligent Cloud Extensions for Cloud Migration</span></span>](ui-extensions-data-replication.md)  
[<span data-ttu-id="a7e41-110">Importieren von Geschäftsdaten aus anderen Finanzsystemen</span><span class="sxs-lookup"><span data-stu-id="a7e41-110">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="a7e41-111">[Anpassen [!INCLUDE[prod_short](includes/prod_short.md)] Erweiterungen nutzen ](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="a7e41-111">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)</span></span>  
[<span data-ttu-id="a7e41-112">Von Dynamics GP zu Business Central Online migrieren</span><span class="sxs-lookup"><span data-stu-id="a7e41-112">Migrate to Business Central Online from Dynamics GP</span></span>](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp)  
