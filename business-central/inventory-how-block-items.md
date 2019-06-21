---
title: So sperren Sie Artikel vom Verkauf oder Einkauf
description: In Business Central kann ein Artikel für den Verkauf, den Einkauf oder alle Zwecke gesperrt werden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8c98e4b893783c795a49e05ab04dc70b03161c6a
ms.sourcegitcommit: bf5f89dfaf5ad9f8f9902941cf3dac3e9f3553e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/22/2019
ms.locfileid: "1594250"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="d8527-103">Artikel vom Verkauf oder Einkauf sperren</span><span class="sxs-lookup"><span data-stu-id="d8527-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="d8527-104">Sie können einen Artikel sperren, damit er nicht auf Verkaufs- oder Einkaufszeilen eingetragen werden kann, und Sie können ihn sperren, damit er nicht in einer Transaktion gebucht werden kann.</span><span class="sxs-lookup"><span data-stu-id="d8527-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="d8527-105">In der folgenden Tabelle wird dargestellt, was geschieht, wenn Artikel gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="d8527-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="d8527-106">Option</span><span class="sxs-lookup"><span data-stu-id="d8527-106">Option</span></span>|<span data-ttu-id="d8527-107">Description</span><span class="sxs-lookup"><span data-stu-id="d8527-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="d8527-108">**Vertrieb gesperrt**</span><span class="sxs-lookup"><span data-stu-id="d8527-108">**Sales Blocked**</span></span>|<span data-ttu-id="d8527-109">Sie können den Artikel nicht in ein Verkaufs- oder Verkaufsartikelbuch.-Blatt eingeben.</span><span class="sxs-lookup"><span data-stu-id="d8527-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="d8527-110">**Einkauf gesperrt**</span><span class="sxs-lookup"><span data-stu-id="d8527-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="d8527-111">Sie können den Artikel nicht in ein Einkaufsdokument, in einem Einkaufsartikel Buch.-Blatt oder in Einkaufsplanungsvorgänge eingeben.</span><span class="sxs-lookup"><span data-stu-id="d8527-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="d8527-112">**Gesperrt**</span><span class="sxs-lookup"><span data-stu-id="d8527-112">**Blocked**</span></span>|<span data-ttu-id="d8527-113">Sie können diesen Artikel nicht für Artikeltransaktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="d8527-113">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="d8527-114">Blockierte Artikel können zurückgesendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8527-114">Blocked items can be returned.</span></span> <span data-ttu-id="d8527-115">Das bedeutet, dass keine der obigen Einstellungen gilt, wenn der Artikel für Reklamationen und Gutschriften verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d8527-115">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="d8527-116">So sperren Sie einen Artikel vom Eintrag auf Verkaufszeilen</span><span class="sxs-lookup"><span data-stu-id="d8527-116">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="d8527-117">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren?“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Katalogartikel** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="d8527-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d8527-118">Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Verkauf gesperrt** aus.</span><span class="sxs-lookup"><span data-stu-id="d8527-118">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="d8527-119">Wenn Sie versuchen, den Artikel in ein Verkaufsdokument oder eine Buch.-Blattzeile einzutragen erhalten Sie jetzt eine Fehlermeldung, dass der Artikel gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="d8527-119">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="d8527-120">So sperren Sie einen Artikel vom Eintrag auf Einkaufszeilen</span><span class="sxs-lookup"><span data-stu-id="d8527-120">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="d8527-121">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Katalogartikel** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="d8527-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d8527-122">Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Einkauf gesperrt** aus.</span><span class="sxs-lookup"><span data-stu-id="d8527-122">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="d8527-123">Wenn Sie versuchen, den Artikel in ein Einkaufsdokument oder eine Buch.-Blattzeile einzutragen erhalten Sie jetzt eine Fehlermeldung, dass der Artikel gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="d8527-123">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="d8527-124">So sperren Sie einen Artikel vor der Buchung</span><span class="sxs-lookup"><span data-stu-id="d8527-124">To block an item from being posted</span></span>
1. <span data-ttu-id="d8527-125">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Katalogartikel** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="d8527-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="d8527-126">Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Gesperrt** aus.</span><span class="sxs-lookup"><span data-stu-id="d8527-126">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="d8527-127">Wenn Sie versuchen, irgendeine Transaktion für den Artikel zu buchen, erhalten Sie jetzt eine Fehlermeldung, dass der Artikel gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="d8527-127">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="d8527-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8527-128">See Also</span></span>  
[<span data-ttu-id="d8527-129">Neue Artikel registrieren</span><span class="sxs-lookup"><span data-stu-id="d8527-129">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="d8527-130">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="d8527-130">Inventory</span></span>](inventory-manage-inventory.md)  
