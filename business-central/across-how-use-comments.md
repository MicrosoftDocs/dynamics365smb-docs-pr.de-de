---
title: Hinzufügen von Bemerkungen zu Karten und Belegen| Microsoft Docs
description: Fügen Sie zusätzlichen Informationen zu Konten, Debitorenkarten oder Verkaufsaufträgen, Verträge, wie eine Sonderpreis- oder Zustellungsmethode, mit anderen Benutzern mitzuteilen hinzu.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: tasks, work
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3f84b6d7d03bd8766bfd485870cef8401a3e3382
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754567"
---
# <a name="add-comments-to-cards-and-documents"></a><span data-ttu-id="cdb68-103">Hinzufügen von Bemerkungen zu Karten und Belegen</span><span class="sxs-lookup"><span data-stu-id="cdb68-103">Add Comments to Cards and Documents</span></span>
<span data-ttu-id="cdb68-104">Fügen Sie zusätzlichen Informationen zu Konten, Debitorenkarten oder Verkaufsaufträgen, Verträge, wie eine Sonderpreis- oder Zustellungsmethode, mit anderen Benutzern mitzuteilen hinzu.</span><span class="sxs-lookup"><span data-stu-id="cdb68-104">You can add extra information to G/L accounts, customers cards, or sales orders to communicate exceptions or special agreements to other users.</span></span>
<span data-ttu-id="cdb68-105">Nahezu alle Karten und Beleg haben eine **Bemerkungen** Aktion, die die Seite **Bemerkungen** öffnen, in der Sie Bemerkungen verfassen oder lesen können.</span><span class="sxs-lookup"><span data-stu-id="cdb68-105">Practically all cards and document have a **Comments** action, which opens the **Comment Sheet** page where you can write or read comments.</span></span> <span data-ttu-id="cdb68-106">In Belege können Sie Bemerkungen einzelnen Zeilen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="cdb68-106">On documents, you can also add comments to individual lines.</span></span>

<span data-ttu-id="cdb68-107">Bemerkungen in laufenden Belegen werden für den entsprechenden gebuchten Beleg übertragen.</span><span class="sxs-lookup"><span data-stu-id="cdb68-107">Comments on ongoing documents are transferred to the related posted document.</span></span> <span data-ttu-id="cdb68-108">Beispielsweise wird eine Bemerkung für einen Auftrag mit einer gebuchten, daraus resultierenden Verkaufslieferung übertragen.</span><span class="sxs-lookup"><span data-stu-id="cdb68-108">For example, a comment on a sales order is transferred to a resulting posted sales shipment.</span></span>

<span data-ttu-id="cdb68-109">Außerdem können Sie definieren, welche Bemerkungen von einer Art Beleg auf eine andere Art Beleg übertragen werden sollen, wie von einem Verkaufsauftrag auf eine Verkaufsrechnung.</span><span class="sxs-lookup"><span data-stu-id="cdb68-109">In addition, you can specify if you want comments to be transferred from one type of document to another resulting type of document, such as from a sales order to a sales invoice.</span></span> <span data-ttu-id="cdb68-110">Sie können dies in **Debitoren & Verkauf** und der Seiten **Kreditoren & Einkauf** festlegen.</span><span class="sxs-lookup"><span data-stu-id="cdb68-110">You do this in the **Sales & Receivables** and the **Purchases & Payables** pages respectively.</span></span>

> [!NOTE]
> <span data-ttu-id="cdb68-111">Bemerkungen werden nicht auf Berichten oder externen Erfassungsbelegen gedruckt.</span><span class="sxs-lookup"><span data-stu-id="cdb68-111">Comments are not printed or output to reports or externally-facing documents.</span></span>

<span data-ttu-id="cdb68-112">Nachfolgend wird erläutert, wie einer Bemerkung einer Artikelkarte hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="cdb68-112">The following describes how to add a comment to an item card.</span></span> <span data-ttu-id="cdb68-113">Die Schritte sind für alle anderen Karten ähnlich und Dokumente, außer in Belegzeilen, die **Bemerkungen** Aktion wird auf ein Zeilenaktionsmenü platziert.</span><span class="sxs-lookup"><span data-stu-id="cdb68-113">The steps are similar for all other cards and documents, except on document lines, the **Comments** action is placed on a lines action menu.</span></span>

## <a name="to-add-a-comments-to-an-item-card"></a><span data-ttu-id="cdb68-114">Um Bemerkungen einer Artikelkarte hinzuzufügen</span><span class="sxs-lookup"><span data-stu-id="cdb68-114">To add a comments to an item card</span></span>
1. <span data-ttu-id="cdb68-115">Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Artikel** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="cdb68-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="cdb68-116">Öffnen Sie die entsprechende Artikelkarte.</span><span class="sxs-lookup"><span data-stu-id="cdb68-116">Open the relevant item card.</span></span>
3. <span data-ttu-id="cdb68-117">Wählen Sie die Aktion **Kommentare** aus.</span><span class="sxs-lookup"><span data-stu-id="cdb68-117">Choose the **Comments** action.</span></span>
4. <span data-ttu-id="cdb68-118">Auf der Seite **Bemerkungen** können Sie beliebigen Text in das Feld eingeben und dann **ok** klicken.</span><span class="sxs-lookup"><span data-stu-id="cdb68-118">On the **Comment Sheet** page, enter any text, and then choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="cdb68-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cdb68-119">See Also</span></span>
<span data-ttu-id="cdb68-120">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cdb68-120">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="cdb68-121">Allgemeine Geschäftsfunktionen</span><span class="sxs-lookup"><span data-stu-id="cdb68-121">General Business Functionality</span></span>](ui-across-business-areas.md)
