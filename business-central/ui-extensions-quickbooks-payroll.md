---
title: Nutzung der Quickbooks-Gehaltsabrechnungsdatei-Importerweiterung| Microsoft Docs
description: Beschreibt, wie die Erweiterung verwendet wird, um Gehalts- und Lohntransaktionen aus dem Quickbooks-Gehaltsabrechnungsdienst zu importieren.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: eae93ea8cf81a2fad6af2c3810f94d5292eef93f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757092"
---
# <a name="the-quickbooks-payroll-file-import-extension"></a><span data-ttu-id="8cae0-103">Die Quickbooks-Gehaltsabrechnungsdatei-Importerweiterung</span><span class="sxs-lookup"><span data-stu-id="8cae0-103">The QuickBooks Payroll File Import Extension</span></span>
<span data-ttu-id="8cae0-104">Verwenden Sie die QuickBooks-Gehaltsabrechnungsdatei-Importerweiterung, um Gehaltsabrechnungstransaktionen von QuickBooks mit den Sachkonten in [!INCLUDE[prod_short](includes/prod_short.md)] zu importieren.</span><span class="sxs-lookup"><span data-stu-id="8cae0-104">Use the QuickBooks Payroll File Import extension to import payroll transactions from QuickBooks to general ledger accounts in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="8cae0-105">Dies ist beispielsweise dann nützlich, wenn Sie von QuickBooks zu [!INCLUDE[prod_short](includes/prod_short.md)] wechseln oder, dass Sie Löhne auslagern aber diese in [!INCLUDE[prod_short](includes/prod_short.md)] nachverfolgen möchten.</span><span class="sxs-lookup"><span data-stu-id="8cae0-105">For example, this is useful when you are transitioning from QuickBooks to [!INCLUDE[prod_short](includes/prod_short.md)], or if you outsource your payroll but also want to keep track of it in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

## <a name="steps-to-import-payroll-data"></a><span data-ttu-id="8cae0-106">So importieren Sie Lohndaten</span><span class="sxs-lookup"><span data-stu-id="8cae0-106">Steps to Import Payroll Data</span></span>
<span data-ttu-id="8cae0-107">Der erste Schritt für Sie oder IHren Buchhalter ist es, die Exportfunktionen in QuickBook zu verwenden, um die Lohndaten in eine .IIF Datei zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="8cae0-107">The first step is for you, or maybe your accountant, to use the export features in QuickBooks to export the payroll data to an .IIF file.</span></span> <span data-ttu-id="8cae0-108">Der zweite Schritt ist es, die **Fibu Buch.-Blätter** in [!INCLUDE[prod_short](includes/prod_short.md)] zu öffnen und die **Lohntransaktionen importieren** Aktion zu verwenden, um die Datei zu importieren.</span><span class="sxs-lookup"><span data-stu-id="8cae0-108">The second step is to open the **General Journals** page in [!INCLUDE[prod_short](includes/prod_short.md)] and use the **Import Payroll Transactions** action to import the file.</span></span> <span data-ttu-id="8cae0-109">Während des Importvorgangs ordnen Sie Sachkonten aus QuickBooks auf den entsprechenden Konten in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="8cae0-109">During the import process you map the general ledger accounts from QuickBooks to corresponding accounts in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="8cae0-110">Zuletzt buchen Sie die Gehaltsabrechnungstransaktionen in [!INCLUDE[prod_short](includes/prod_short.md)]mentsprechend der Kontozuordnung.</span><span class="sxs-lookup"><span data-stu-id="8cae0-110">The final step is to post the payroll transactions in [!INCLUDE[prod_short](includes/prod_short.md)] according to the account mapping.</span></span> 

<span data-ttu-id="8cae0-111">Weitere Informationen finden Sie unter [Gehaltsabrechnungstransaktionen importieren](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="8cae0-111">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8cae0-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8cae0-112">See Also</span></span>
<span data-ttu-id="8cae0-113">[Anpassen [!INCLUDE[prod_short](includes/prod_short.md)] Erweiterungen nutzen](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="8cae0-113">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="8cae0-114">[Finanzen](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="8cae0-114">[Finance](finance.md)  </span></span>  
<span data-ttu-id="8cae0-115">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8cae0-115">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
