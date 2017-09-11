---
title: Verkaufssteuer in Kanada | Microsoft Docs
description: "Mehr über Verkaufssteuer sowie Steuern auf Waren und Dienstleistungen in Kanada erfahren."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales tax, local
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 571b11f4f18ffd194bdfe1d1d412bca87df4b868
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2017

---
# <a name="reporting-sales-tax-and-goodsservices-tax-in-canada"></a><span data-ttu-id="34dcc-103">Verkaufssteuern sowie Steuern auf Waren und Dienstleistungen in Kanada berichten</span><span class="sxs-lookup"><span data-stu-id="34dcc-103">Reporting Sales Tax and Goods/Services Tax in Canada</span></span>
<span data-ttu-id="34dcc-104">Wenn ein Kreditor in Kanada keine Geschäftspräsenz in der Provinz hat, in der die Einkäufe getätigt werden, berechnet der Kreditor nur Steuern auf Waren und Dienstleistungen (Goods and Services Tax, GST) oder Harmonised Sales Tax (HST).</span><span class="sxs-lookup"><span data-stu-id="34dcc-104">In Canada, when a vendor does not have a business presence in the province in which purchases are made, the vendor will charge the Goods and Services Tax (GST) or Harmonized Sales Tax (HST) only.</span></span> <span data-ttu-id="34dcc-105">Wenn jedoch die Provinz eine Provincial Sales Tax (PST) erhebt, dann muß der Einkäufer noch die PST berechnen und sie direkt an die Provinz bezahlen.</span><span class="sxs-lookup"><span data-stu-id="34dcc-105">However, if the province has a Provincial Sales Tax (PST), then the purchaser must still calculate the PST and pay it directly to the province.</span></span> <span data-ttu-id="34dcc-106">Wenn ein Steuergebietscode für Provinzen aktiviert ist, verwendet [!INCLUDE[d365fin](includes/d365fin_md.md)] diesen, um die PST zu berechnen und zu buchen, sodass sowohl im Sachkonto als auch in den Steuerpostendatensätzen Steuerverbindlichkeiten vermerkt sind.</span><span class="sxs-lookup"><span data-stu-id="34dcc-106">When a Provincial Tax Area Code is selected, [!INCLUDE[d365fin](includes/d365fin_md.md)] uses it to calculate the PST and post it so that there is a tax liability in both the general ledger and the tax entry records.</span></span> <span data-ttu-id="34dcc-107">Daher sollte der Steuergebietscode, der hier aktiviert ist, nur die PST enthalten, nicht die GST.</span><span class="sxs-lookup"><span data-stu-id="34dcc-107">Therefore, the tax area code selected here should be one where only the PST is included, not the GST.</span></span>  

<span data-ttu-id="34dcc-108">Weitere Informationen zur Verkaufssteuer, finden Sie unter [Verkaufssteuer sowie Steuergruppen in den USA und in Kanada](us-finance-sales-tax.md).</span><span class="sxs-lookup"><span data-stu-id="34dcc-108">For more information about sales tax, see [Sales Tax and Tax Groups in the US and Canada](us-finance-sales-tax.md).</span></span>  

## <a name="submitting-the-gsthst-file"></a><span data-ttu-id="34dcc-109">Übermitteln der GST-/HST-Datei</span><span class="sxs-lookup"><span data-stu-id="34dcc-109">Submitting the GST/HST File</span></span>
<span data-ttu-id="34dcc-110">Die Steuerdaten in Einkaufsbelegen werden verwendet, um eine GST/HST-Online-Dateiübertragung (GIFT) zu generieren, die Sie dem Finanzamt bereitstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="34dcc-110">The tax information in purchase documents is used to generate a GST/HST online file transfer that you must provide to the tax authorities.</span></span> <span data-ttu-id="34dcc-111">Diese Datei umfasst Steuern auf Waren und Dienstleistungen (GST) und die Harmonised Sales Tax (HST).</span><span class="sxs-lookup"><span data-stu-id="34dcc-111">This file includes goods and services tax (GST) and harmonized sales tax (HST).</span></span> <span data-ttu-id="34dcc-112">Die Datei wird in einem .tax-Dateiformat erstellt, das online übertragen werden kann.</span><span class="sxs-lookup"><span data-stu-id="34dcc-112">The file is created in a .tax file format, which can be transferred online.</span></span>  

## <a name="see-also"></a><span data-ttu-id="34dcc-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34dcc-113">See Also</span></span>
[<span data-ttu-id="34dcc-114">Finanzen</span><span class="sxs-lookup"><span data-stu-id="34dcc-114">Finance</span></span>](finance.md)  
[<span data-ttu-id="34dcc-115">Finance einrichten</span><span class="sxs-lookup"><span data-stu-id="34dcc-115">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="34dcc-116">Finance einrichten</span><span class="sxs-lookup"><span data-stu-id="34dcc-116">Sales Tax and Tax Groups in the US and Canada</span></span>](us-finance-sales-tax.md)  
<span data-ttu-id="34dcc-117">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="34dcc-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

