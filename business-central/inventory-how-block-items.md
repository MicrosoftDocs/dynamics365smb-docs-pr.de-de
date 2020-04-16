---
title: So sperren Sie Artikel vom Verkauf oder Einkauf
description: In Business Central kann ein Artikel für den Verkauf, den Einkauf oder alle Zwecke gesperrt werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: c453a10f30d2a45f6d4641bda8b24ee3659b1a32
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182300"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="4a52e-103">Artikel vom Verkauf oder Einkauf sperren</span><span class="sxs-lookup"><span data-stu-id="4a52e-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="4a52e-104">Sie können einen Artikel sperren, damit er nicht auf Verkaufs- oder Einkaufszeilen eingetragen werden kann, und Sie können ihn sperren, damit er nicht in einer Transaktion gebucht werden kann.</span><span class="sxs-lookup"><span data-stu-id="4a52e-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="4a52e-105">In der folgenden Tabelle wird dargestellt, was geschieht, wenn Artikel gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="4a52e-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="4a52e-106">Option</span><span class="sxs-lookup"><span data-stu-id="4a52e-106">Option</span></span>|<span data-ttu-id="4a52e-107">Description</span><span class="sxs-lookup"><span data-stu-id="4a52e-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="4a52e-108">**Vertrieb gesperrt**</span><span class="sxs-lookup"><span data-stu-id="4a52e-108">**Sales Blocked**</span></span>|<span data-ttu-id="4a52e-109">Sie können den Artikel nicht in ein Verkaufs- oder Verkaufsartikelbuch.-Blatt eingeben.</span><span class="sxs-lookup"><span data-stu-id="4a52e-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="4a52e-110">**Einkauf gesperrt**</span><span class="sxs-lookup"><span data-stu-id="4a52e-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="4a52e-111">Sie können den Artikel nicht in ein Einkaufsdokument, in einem Einkaufsartikel Buch.-Blatt oder in Einkaufsplanungsvorgänge eingeben.</span><span class="sxs-lookup"><span data-stu-id="4a52e-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="4a52e-112">**Gesperrt**</span><span class="sxs-lookup"><span data-stu-id="4a52e-112">**Blocked**</span></span>|<span data-ttu-id="4a52e-113">Sie können diesen Artikel nicht für Artikeltransaktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="4a52e-113">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="4a52e-114">Blockierte Artikel können zurückgesendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a52e-114">Blocked items can be returned.</span></span> <span data-ttu-id="4a52e-115">Das bedeutet, dass keine der obigen Einstellungen gilt, wenn der Artikel für Reklamationen und Gutschriften verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4a52e-115">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

<span data-ttu-id="4a52e-116">Wenn Sie die Funktion **Aus Dokument kopieren** verwenden, um neue Dokumente auf der Grundlage vorhandener Dokumente zu erstellen, werden Sie benachrichtigt, wenn Positionen in den Zeilen des Quelldokuments blockiert sind.</span><span class="sxs-lookup"><span data-stu-id="4a52e-116">When you use the **Copy from Document** function to create new documents based on existing documents, you are notified if any items on the source document lines are blocked.</span></span> <span data-ttu-id="4a52e-117">Die gesperrten Belegzeilen werden vom neuen Beleg ausgeschlossen, und eine Benachrichtigung zeigt eine Übersicht aller Belegzeilen, die im Quellbeleg gesperrt sind.</span><span class="sxs-lookup"><span data-stu-id="4a52e-117">The blocked document lines are excluded from the new document, and a notification shows an overview of all document lines that are blocked in the source document.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="4a52e-118">So sperren Sie einen Artikel vom Eintrag auf Verkaufszeilen</span><span class="sxs-lookup"><span data-stu-id="4a52e-118">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="4a52e-119">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Elemente** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="4a52e-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="4a52e-120">Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Verkauf gesperrt** aus.</span><span class="sxs-lookup"><span data-stu-id="4a52e-120">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="4a52e-121">Wenn Sie versuchen, den Artikel in ein Verkaufsdokument oder eine Buch.-Blattzeile einzutragen erhalten Sie jetzt eine Fehlermeldung, dass der Artikel gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="4a52e-121">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="4a52e-122">So sperren Sie einen Artikel vom Eintrag auf Einkaufszeilen</span><span class="sxs-lookup"><span data-stu-id="4a52e-122">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="4a52e-123">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Elemente** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="4a52e-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="4a52e-124">Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Einkauf gesperrt** aus.</span><span class="sxs-lookup"><span data-stu-id="4a52e-124">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="4a52e-125">Wenn Sie versuchen, den Artikel in ein Einkaufsdokument oder eine Buch.-Blattzeile einzutragen erhalten Sie jetzt eine Fehlermeldung, dass der Artikel gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="4a52e-125">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="4a52e-126">So sperren Sie einen Artikel vor der Buchung</span><span class="sxs-lookup"><span data-stu-id="4a52e-126">To block an item from being posted</span></span>
1. <span data-ttu-id="4a52e-127">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Elemente** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="4a52e-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="4a52e-128">Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Gesperrt** aus.</span><span class="sxs-lookup"><span data-stu-id="4a52e-128">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="4a52e-129">Wenn Sie versuchen, irgendeine Transaktion für den Artikel zu buchen, erhalten Sie jetzt eine Fehlermeldung, dass der Artikel gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="4a52e-129">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="4a52e-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a52e-130">See Also</span></span>  
[<span data-ttu-id="4a52e-131">Neue Artikel registrieren</span><span class="sxs-lookup"><span data-stu-id="4a52e-131">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="4a52e-132">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="4a52e-132">Inventory</span></span>](inventory-manage-inventory.md)  
