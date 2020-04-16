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
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: bae0ddeb2a3b22d4f29c04628a54754f4d608ec9
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3191019"
---
# <a name="request-quotes"></a><span data-ttu-id="65a28-103">Angebotsanforderungen</span><span class="sxs-lookup"><span data-stu-id="65a28-103">Request Quotes</span></span>
<span data-ttu-id="65a28-104">Eine Einkaufsanfrage kann als erster Entwurf für eine Bestellung verwendet werden. Die Bestellung kann dann in eine Rechnung oder einen Auftrag umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="65a28-104">A purchase quote can be used as a preliminary draft for a purchase order, and the order can then be converted to a purchase invoice or an order.</span></span>


## <a name="to-create-a-purchase-quote"></a><span data-ttu-id="65a28-105">So erstellen Sie eine Einkaufsanfrage</span><span class="sxs-lookup"><span data-stu-id="65a28-105">To create a purchase quote</span></span>
1. <span data-ttu-id="65a28-106">Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Einkaufsanfragen** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="65a28-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Quotes**, and then choose the related link.</span></span>
2. <span data-ttu-id="65a28-107">Erstellen eines neuen Belegs, so wie Sie eine Bestellung erstellen.</span><span class="sxs-lookup"><span data-stu-id="65a28-107">Create a new document, in the same way as you make a purchase order.</span></span> <span data-ttu-id="65a28-108">Weitere Informationen finden Sie unter [Erfassen eines Einkaufs](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="65a28-108">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a><span data-ttu-id="65a28-109">So konvertieren Sie eine Einkaufsanfrage in eine Einkaufsbestellung</span><span class="sxs-lookup"><span data-stu-id="65a28-109">To convert a purchase quote to a purchase order</span></span>
<span data-ttu-id="65a28-110">Wenn Sie das Angebot akzeptiert haben, können Sie diese mit einer Einkaufsrechnung oder einem Auftrag umwandeln, um den Einkauf zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="65a28-110">When you have accepted the vendor's quote, you can convert it to a purchase invoice or order to process the purchase.</span></span>

1. <span data-ttu-id="65a28-111">Öffnen Sie eine Einkaufsanfrage, die bereit ist zum umzuwandeln, und wählen Sie die **Bestellung erst.** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="65a28-111">Open a purchase quote that is ready to convert, and then choose the **Make Order** action.</span></span>

<span data-ttu-id="65a28-112">Das Verkaufsangebot wird aus der Datenbank entfernt.</span><span class="sxs-lookup"><span data-stu-id="65a28-112">The purchase quote is removed from the database.</span></span> <span data-ttu-id="65a28-113">Eine Verkaufsrechnung oder ein Verkaufsauftrag wird auf der Basis der Informationen im Verkaufsangebot erstellt, in dem Sie den Verkauf verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="65a28-113">A purchase invoice or a purchase order is created based on the information in the purchase quote in which you can process the purchase.</span></span> <span data-ttu-id="65a28-114">In der erstellten Verkaufsrechnung gibt das Feld **Angebotsnr.** die Nummer des Verkaufsauftrags oder der Rechnung  n, aus dem sie erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="65a28-114">In the **Quote No.** field on the purchase invoice or purchase order, you can see the number of the purchase quote that it was made from.</span></span>

## <a name="see-also"></a><span data-ttu-id="65a28-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65a28-115">See Also</span></span>
[<span data-ttu-id="65a28-116">Einkauf</span><span class="sxs-lookup"><span data-stu-id="65a28-116">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="65a28-117">Einkaufeinrichten</span><span class="sxs-lookup"><span data-stu-id="65a28-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="65a28-118">Dokumente per E-Mail versenden</span><span class="sxs-lookup"><span data-stu-id="65a28-118">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="65a28-119">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="65a28-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
