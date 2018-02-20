---
title: "Weisen Sie einem Kreditor eine Prioritätsstufe zu| Microsoft Docs"
description: "Sie können sowohl Zahlen Ihren Kreditoren oder Lieferanten zuweisen, um sie zu priorisieren und Zahlungsvorschläge in Finance and Operations, Business edition zu erleichtern."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d44e06f4dd33332e8d96e712e93ed05c7f0a920b
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="prioritize-vendors"></a><span data-ttu-id="2d414-103">Kreditoren priorisieren</span><span class="sxs-lookup"><span data-stu-id="2d414-103">Prioritize Vendors</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="2d414-104"> kann verschiedene Zahlungen an Kreditoren vorschlagen. Dies können z. B. Zahlungen sein, die in Kürze fällig sind, oder Zahlungen, bei denen Sie einen Rabatt erhalten können.</span><span class="sxs-lookup"><span data-stu-id="2d414-104">can suggest various payments to vendors, for example, payments that will be due soon or payments where a discount is available.</span></span> <span data-ttu-id="2d414-105">Weitere Informationen finden Sie unter [Erstellen von Zahlungsvorschlägen für Kreditoren](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="2d414-105">For more information, see [Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span>

<span data-ttu-id="2d414-106">Zuerst müssen Sie den Kreditoren priorisieren, indem Sie ihm Nummern zuweisen.</span><span class="sxs-lookup"><span data-stu-id="2d414-106">First, you must prioritize your vendors by assigning numbers to them.</span></span>

## <a name="to-prioritize-vendors"></a><span data-ttu-id="2d414-107">So priorisieren Sie Kreditoren</span><span class="sxs-lookup"><span data-stu-id="2d414-107">To prioritize vendors</span></span>
1. <span data-ttu-id="2d414-108">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Bankkonten** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="2d414-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendors**, and then choose the related link.</span></span>
2. <span data-ttu-id="2d414-109">Wählen Sie die entsprechende Kreditor, und klicken Sie dann auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="2d414-109">Select the relevant vendor, and then choose **Edit**.</span></span>
3. <span data-ttu-id="2d414-110">Geben Sie im Feld **Priorität** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="2d414-110">In the **Priority** field, enter a number.</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="2d414-111"> geht davon aus, dass die niedrigsten Nummern (außer 0) die höchste Priorität haben.</span><span class="sxs-lookup"><span data-stu-id="2d414-111">considers the lowest number, except 0, to have the highest priority.</span></span> <span data-ttu-id="2d414-112">Wenn Sie also z. B. 1, 2 und 3 verwenden, erhält 1 die höchste Priorität.</span><span class="sxs-lookup"><span data-stu-id="2d414-112">So, for example, if you use 1, 2, and 3, then 1 will have the highest priority.</span></span>

<span data-ttu-id="2d414-113">Falls Sie einem Kreditor keine Priorität zuweisen wollen, lassen Sie das Feld **Priorität** leer.</span><span class="sxs-lookup"><span data-stu-id="2d414-113">If you do not want to prioritize a vendor, leave the **Priority** field blank.</span></span> <span data-ttu-id="2d414-114">Wenn Sie dann die Funktion "Zahlungsvorschlag" verwenden, wird dieser Kreditor nach den Kreditoren aufgeführt, die eine Priorität haben.</span><span class="sxs-lookup"><span data-stu-id="2d414-114">Then, if you use the payment suggestion feature, the vendor will be listed after all the vendors that have a priority number.</span></span> <span data-ttu-id="2d414-115">Sie können so viele Prioritäten einrichten wie Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="2d414-115">You can enter as many priority levels as necessary.</span></span>

## <a name="see-also"></a><span data-ttu-id="2d414-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d414-116">See Also</span></span>
[<span data-ttu-id="2d414-117">Einkaufeinrichten</span><span class="sxs-lookup"><span data-stu-id="2d414-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="2d414-118">Verwalten von Verbindlichkeiten</span><span class="sxs-lookup"><span data-stu-id="2d414-118">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="2d414-119">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2d414-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

