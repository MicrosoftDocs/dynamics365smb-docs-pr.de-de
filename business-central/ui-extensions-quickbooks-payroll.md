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
ms.date: 01/09/2019
ms.author: bholtorf
ms.openlocfilehash: ac68f8a4d67224ad55b1c34ff9b2e4ffa2c372aa
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "798384"
---
# <a name="the-quickbooks-payroll-file-import-extension"></a><span data-ttu-id="ed0d1-103">Die Quickbooks-Gehaltsabrechnungsdatei-Importerweiterung</span><span class="sxs-lookup"><span data-stu-id="ed0d1-103">The QuickBooks Payroll File Import Extension</span></span>
<span data-ttu-id="ed0d1-104">Verwenden Sie die QuickBooks-Gehaltsabrechnungsdatei-Importerweiterung, um Gehaltsabrechnungstransaktionen von QuickBooks mit den Sachkonten in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu importieren.</span><span class="sxs-lookup"><span data-stu-id="ed0d1-104">Use the QuickBooks Payroll File Import extension to import payroll transactions from QuickBooks to general ledger accounts in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="ed0d1-105">Dies ist beispielsweise dann nützlich, wenn Sie von QuickBooks zu [!INCLUDE[d365fin](includes/d365fin_md.md)] wechseln oder, dass Sie Löhne auslagern aber diese in [!INCLUDE[d365fin](includes/d365fin_md.md)] nachverfolgen möchten.</span><span class="sxs-lookup"><span data-stu-id="ed0d1-105">For example, this is useful when you are transitioning from QuickBooks to [!INCLUDE[d365fin](includes/d365fin_md.md)], or if you outsource your payroll but also want to keep track of it in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="steps-to-import-payroll-data"></a><span data-ttu-id="ed0d1-106">So importieren Sie Lohndaten</span><span class="sxs-lookup"><span data-stu-id="ed0d1-106">Steps to Import Payroll Data</span></span>
<span data-ttu-id="ed0d1-107">Der erste Schritt für Sie oder IHren Buchhalter ist es, die Exportfunktionen in QuickBook zu verwenden, um die Lohndaten in eine .IIF Datei zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="ed0d1-107">The first step is for you, or maybe your accountant, to use the export features in QuickBooks to export the payroll data to an .IIF file.</span></span> <span data-ttu-id="ed0d1-108">Der zweite Schritt ist es, die **Fibu Buch.-Blätter** in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu öffnen und die **Lohntransaktionen importieren** Aktion zu verwenden, um die Datei zu importieren.</span><span class="sxs-lookup"><span data-stu-id="ed0d1-108">The second step is to open the **General Journals** page in [!INCLUDE[d365fin](includes/d365fin_md.md)] and use the **Import Payroll Transactions** action to import the file.</span></span> <span data-ttu-id="ed0d1-109">Während des Importvorgangs ordnen Sie Sachkonten aus QuickBooks auf den entsprechenden Konten in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ed0d1-109">During the import process you map the general ledger accounts from QuickBooks to corresponding accounts in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="ed0d1-110">Zuletzt buchen Sie die Gehaltsabrechnungstransaktionen in [!INCLUDE[d365fin](includes/d365fin_md.md)]mentsprechend der Kontozuordnung.</span><span class="sxs-lookup"><span data-stu-id="ed0d1-110">The final step is to post the payroll transactions in [!INCLUDE[d365fin](includes/d365fin_md.md)] according to the account mapping.</span></span> 

<span data-ttu-id="ed0d1-111">Weitere Informationen finden Sie unter [Gehaltsabrechnungstransaktionen importieren](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="ed0d1-111">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ed0d1-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed0d1-112">See Also</span></span>
<span data-ttu-id="ed0d1-113">[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="ed0d1-113">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="ed0d1-114">[Finanzen](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="ed0d1-114">[Finance](finance.md)  </span></span>  
<span data-ttu-id="ed0d1-115">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ed0d1-115">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
