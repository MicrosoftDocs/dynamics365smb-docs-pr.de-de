---
title: Importieren der Gehalts-Daten mithilfe der Ceridian-Gehaltsabrechnungserweiterung | Microsoft Docs
description: Mit der Ceridian-Gehaltsabrechnungserweiterung können Sie die Importgehaltsabrechnungstransaktionen Services Ceridian HR/Payroll (USA) und Ceridian PowerPay (Kanada) importieren.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 5c90555b71fd3991d6a3c2e4e8a44c687b4299bb
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3785371"
---
# <a name="the-ceridian-payroll-extension"></a><span data-ttu-id="a13a4-103">Die Ceridian-Gehaltsabrechnungserweiterung</span><span class="sxs-lookup"><span data-stu-id="a13a4-103">The Ceridian Payroll Extension</span></span>
<span data-ttu-id="a13a4-104">Um Gehaltszahlungen und verwandte Transaktionen zu berücksichtigen, müssen Sie die Gehaltstransaktionen importieren und finanzielle Transaktionen buchen, die durch Ihr Gehaltsabrechnungsanbieter in die Finanzbuchhaltung gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="a13a4-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span>

<span data-ttu-id="a13a4-105">Dazu importieren Sie zuerst eine Datei, die Sie vom Gehaltsabrechnungsanbieter erhalten in die Seite **Fibur Buch.Blatt**.</span><span class="sxs-lookup"><span data-stu-id="a13a4-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** page.</span></span> <span data-ttu-id="a13a4-106">Anschließend ordnen Sie die externen Konten in der Gehaltsabrechnungsdatei den jeweiligen Sachkonten zu.</span><span class="sxs-lookup"><span data-stu-id="a13a4-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="a13a4-107">Zuletzt buchen Sie die Gehaltsabrechnungstransaktionen entsprechend der Kontozuordnung.</span><span class="sxs-lookup"><span data-stu-id="a13a4-107">Lastly, you post the payroll transactions according to the account mapping.</span></span> <span data-ttu-id="a13a4-108">Weitere Informationen finden Sie unter [Gehaltsabrechnungstransaktionen importieren](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="a13a4-108">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

<span data-ttu-id="a13a4-109">Mit der Ceridian-Gehaltsabrechnungserweiterung können Sie die Importgehaltsabrechnungstransaktionen Services Ceridian HR/Payroll (USA) und Ceridian PowerPay (Kanada) importieren.</span><span class="sxs-lookup"><span data-stu-id="a13a4-109">The Ceridian Payroll extension allows you to import payroll transactions from the Ceridian HR/Payroll (US) and Ceridian PowerPay (Canada) services.</span></span>

## <a name="see-also"></a><span data-ttu-id="a13a4-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a13a4-110">See Also</span></span>
<span data-ttu-id="a13a4-111">[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="a13a4-111">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="a13a4-112">[Finanzen](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="a13a4-112">[Finance](finance.md)  </span></span>  
<span data-ttu-id="a13a4-113">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a13a4-113">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
