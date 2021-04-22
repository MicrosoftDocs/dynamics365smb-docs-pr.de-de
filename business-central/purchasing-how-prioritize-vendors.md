---
title: Weisen Sie einem Kreditor eine Prioritätsstufe zu| Microsoft Docs
description: Sie können sowohl Zahlen Ihren Kreditoren oder Lieferanten zuweisen, um sie zu priorisieren und Zahlungsvorschläge in  Business Central zu erleichtern.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1604113b255a585532677ccb47d7e68d1cc64059
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772779"
---
# <a name="prioritize-vendors"></a><span data-ttu-id="53dae-103">Kreditoren priorisieren</span><span class="sxs-lookup"><span data-stu-id="53dae-103">Prioritize Vendors</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="53dae-104">kann verschiedene Zahlungen an Kreditoren vorschlagen. Dies können z. B. Zahlungen sein, die in Kürze fällig sind, oder Zahlungen, bei denen Sie einen Rabatt erhalten können.</span><span class="sxs-lookup"><span data-stu-id="53dae-104">can suggest various payments to vendors, for example, payments that will be due soon or payments where a discount is available.</span></span> <span data-ttu-id="53dae-105">Weitere Informationen finden Sie unter [Erstellen von Zahlungsvorschlägen für Kreditoren](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="53dae-105">For more information, see [Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span>

<span data-ttu-id="53dae-106">Zuerst müssen Sie den Kreditoren priorisieren, indem Sie ihm Nummern zuweisen.</span><span class="sxs-lookup"><span data-stu-id="53dae-106">First, you must prioritize your vendors by assigning numbers to them.</span></span>
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE3PRGa?rel=0]

## <a name="to-prioritize-vendors"></a><span data-ttu-id="53dae-107">So priorisieren Sie Kreditoren</span><span class="sxs-lookup"><span data-stu-id="53dae-107">To prioritize vendors</span></span>
1. <span data-ttu-id="53dae-108">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Anbieter** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="53dae-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>
2. <span data-ttu-id="53dae-109">Wählen Sie die entsprechende Kreditor, und klicken Sie dann auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="53dae-109">Select the relevant vendor, and then choose **Edit**.</span></span>
3. <span data-ttu-id="53dae-110">Geben Sie im Feld **Priorität** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="53dae-110">In the **Priority** field, enter a number.</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="53dae-111">geht davon aus, dass die niedrigsten Nummern (außer 0) die höchste Priorität haben.</span><span class="sxs-lookup"><span data-stu-id="53dae-111">considers the lowest number, except 0, to have the highest priority.</span></span> <span data-ttu-id="53dae-112">Wenn Sie also z. B. 1, 2 und 3 verwenden, erhält 1 die höchste Priorität.</span><span class="sxs-lookup"><span data-stu-id="53dae-112">So, for example, if you use 1, 2, and 3, then 1 will have the highest priority.</span></span>

<span data-ttu-id="53dae-113">Falls Sie einem Kreditor keine Priorität zuweisen wollen, lassen Sie das Feld **Priorität** leer.</span><span class="sxs-lookup"><span data-stu-id="53dae-113">If you do not want to prioritize a vendor, leave the **Priority** field blank.</span></span> <span data-ttu-id="53dae-114">Wenn Sie dann die Funktion "Zahlungsvorschlag" verwenden, wird dieser Kreditor nach den Kreditoren aufgeführt, die eine Priorität haben.</span><span class="sxs-lookup"><span data-stu-id="53dae-114">Then, if you use the payment suggestion feature, the vendor will be listed after all the vendors that have a priority number.</span></span> <span data-ttu-id="53dae-115">Sie können so viele Prioritäten einrichten wie Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="53dae-115">You can enter as many priority levels as necessary.</span></span>

## <a name="see-also"></a><span data-ttu-id="53dae-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53dae-116">See Also</span></span>
[<span data-ttu-id="53dae-117">Einkaufeinrichten</span><span class="sxs-lookup"><span data-stu-id="53dae-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="53dae-118">Verwalten von Verbindlichkeiten</span><span class="sxs-lookup"><span data-stu-id="53dae-118">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="53dae-119">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="53dae-119">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]