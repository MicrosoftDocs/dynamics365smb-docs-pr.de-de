---
title: Erstellen Sie eine Einkaufsanfrage, um ein Angebot von Ihrem Lieferanten anzufordern | Microsoft Docs
description: Beschreibt, wie Verkaufsangebote oder eine Anforderung erstellt wird, um Ihr Angebot zu erfassen, um unter bestimmten Bedingungen einem Debitoren zu verkaufen.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: a243df7928e6468cc3490966331b325134f6cc37
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "798921"
---
# <a name="request-quotes"></a><span data-ttu-id="64d36-103">Angebotsanforderungen</span><span class="sxs-lookup"><span data-stu-id="64d36-103">Request Quotes</span></span>
<span data-ttu-id="64d36-104">Eine Einkaufsanfrage kann als erster Entwurf für eine Bestellung verwendet werden. Die Bestellung kann dann in eine Rechnung oder einen Auftrag umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="64d36-104">A purchase quote can be used as a preliminary draft for a purchase order, and the order can then be converted to a purchase invoice or an order.</span></span>


## <a name="to-create-a-purchase-quote"></a><span data-ttu-id="64d36-105">So erstellen Sie eine Einkaufsanfrage</span><span class="sxs-lookup"><span data-stu-id="64d36-105">To create a purchase quote</span></span>
1. <span data-ttu-id="64d36-106">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kaufangebote** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="64d36-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Quotes**, and then choose the related link.</span></span>
2. <span data-ttu-id="64d36-107">Erstellen eines neuen Belegs, so wie Sie eine Bestellung erstellen.</span><span class="sxs-lookup"><span data-stu-id="64d36-107">Create a new document, in the same way as you make a purchase order.</span></span> <span data-ttu-id="64d36-108">Weitere Informationen finden Sie unter [Erfassen eines Einkaufs](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="64d36-108">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a><span data-ttu-id="64d36-109">So konvertieren Sie eine Einkaufsanfrage in eine Einkaufsbestellung</span><span class="sxs-lookup"><span data-stu-id="64d36-109">To convert a purchase quote to a purchase order</span></span>
<span data-ttu-id="64d36-110">Wenn Sie das Angebot akzeptiert haben, können Sie diese mit einer Einkaufsrechnung oder einem Auftrag umwandeln, um den Einkauf zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="64d36-110">When you have accepted the vendor's quote, you can convert it to a purchase invoice or order to process the purchase.</span></span>

1. <span data-ttu-id="64d36-111">Öffnen Sie eine Einkaufsanfrage, die bereit ist zum umzuwandeln, und wählen Sie die **Bestellung erst.** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="64d36-111">Open a purchase quote that is ready to convert, and then choose the **Make Order** action.</span></span>

<span data-ttu-id="64d36-112">Das Verkaufsangebot wird aus der Datenbank entfernt.</span><span class="sxs-lookup"><span data-stu-id="64d36-112">The purchase quote is removed from the database.</span></span> <span data-ttu-id="64d36-113">Eine Verkaufsrechnung oder ein Verkaufsauftrag wird auf der Basis der Informationen im Verkaufsangebot erstellt, in dem Sie den Verkauf verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="64d36-113">A purchase invoice or a purchase order is created based on the information in the purchase quote in which you can process the purchase.</span></span> <span data-ttu-id="64d36-114">In der erstellten Verkaufsrechnung gibt das Feld **Angebotsnr.** die Nummer des Verkaufsauftrags oder der Rechnung  n, aus dem sie erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="64d36-114">In the **Quote No.** field on the purchase invoice or purchase order, you can see the number of the purchase quote that it was made from.</span></span>

## <a name="see-also"></a><span data-ttu-id="64d36-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64d36-115">See Also</span></span>
[<span data-ttu-id="64d36-116">Einkauf</span><span class="sxs-lookup"><span data-stu-id="64d36-116">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="64d36-117">Einkaufeinrichten</span><span class="sxs-lookup"><span data-stu-id="64d36-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="64d36-118">Senden von Belegen über E-Mail</span><span class="sxs-lookup"><span data-stu-id="64d36-118">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="64d36-119">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="64d36-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
