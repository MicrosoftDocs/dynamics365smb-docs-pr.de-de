---
title: "Einrichten von Branchengruppen für Kontaktunternehmen| Microsoft Docs"
description: Beschreibt, wie eine Branche definiert und diese einem Kontaktunternehmen, beispielsweise Einzelhandelsbranche, oder der Automobilindustrie zuweist.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: d2e331536de615b5a3ad84db526f86c79e56774c
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-industry-groups-for-contact-companies"></a><span data-ttu-id="bcfc8-103">Einrichten von Branchen für Kontaktunternehmen</span><span class="sxs-lookup"><span data-stu-id="bcfc8-103">Set Up Industry Groups for Contact Companies</span></span>
<span data-ttu-id="bcfc8-104">Branchen werden verwendet, um die Branche anzugeben, zu der Ihre Kontakte gehören z. B. die Einzelhandelsbranche und die Automobilbranche.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-104">You use industry groups to indicate the type of industry to which your contacts belong, for example, the retail industry or the automobile industry.</span></span>

<span data-ttu-id="bcfc8-105">Die Nutzung von Branchen zu Kontakten ist ein zwei Schritte umfassender Prozess.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-105">Using industry groups on contacts is a two-step process.</span></span> <span data-ttu-id="bcfc8-106">Zuerst definieren Sie den Branchenscode.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-106">First, you define the industry group code.</span></span> <span data-ttu-id="bcfc8-107">Sie müssen diesen Schritt nur einmal für jede Branche ausführen.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-107">You only have to perform this step one time for each industry group.</span></span> <span data-ttu-id="bcfc8-108">Sobald Sie einen Branchencode haben, können Sie den Code zu den Kontaktunternehmen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-108">Once you have an industry group code, you can start to assign the code to contact companies.</span></span>

> [!NOTE]  
>   <span data-ttu-id="bcfc8-109">Wenn Sie planen, Ihre Kontakte mit Debitoren, Kreditoren oder Bankkonten in anderen Teilen der Anwendung zu synchronisieren, können Sie für sie eine Geschäftsbeziehung erstellen.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-109">If you plan to synchronize your contacts with vendors, customers, or bank accounts in other parts of the application, you may want to set up a business relation for them.</span></span>

## <a name="to-define-an-industry-group-code"></a><span data-ttu-id="bcfc8-110">Branchengruppencode definieren</span><span class="sxs-lookup"><span data-stu-id="bcfc8-110">To define an industry group code</span></span>
<span data-ttu-id="bcfc8-111">Der Branchencode definiert die Art oder die Kategorie der Gruppe, z. B. WERBUNG für Werbung oder PRESSE für TV und Radio.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-111">The industry group code defines the type or category of the group, such as ADVERT for advertising, or PRESS, for TV and radio.</span></span> <span data-ttu-id="bcfc8-112">Sie können mehrere Branchencodes haben.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-112">You can have several industry group codes.</span></span> <span data-ttu-id="bcfc8-113">Um die Branchen zu definieren, verwenden Sie das **Branchen**-Fenster.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-113">To define the industry groups, you use the **Industry Groups** window.</span></span>

1. <span data-ttu-id="bcfc8-114">Wählen Sie das Symbol![ Nach Seite oder Bericht suchen ](media/ui-search/search_small.png "Nach Seite oder Bericht suchen")und geben **Branchen** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Industry Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="bcfc8-115">Wählen Sie die Aktion **Neu** aus, und geben Sie einen Code und eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="bcfc8-116">Der Code kann maximal 11 Zeichen, sowohl Ziffern als auch Buchstaben, umfassen.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <span data-ttu-id="bcfc8-117"><a name="AssignIndustryGroupContact">Um einem Kontakt eine Branche zuzuordnen:</a></span><span class="sxs-lookup"><span data-stu-id="bcfc8-117"><a name="AssignIndustryGroupContact"></a> To assign industry groups to a contact</span></span>
<span data-ttu-id="bcfc8-118">Sie können Branchen nicht zu Personen zuordnen – nur zu Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-118">You cannot assign industry groups to a contact person - only companies.</span></span>

1. <span data-ttu-id="bcfc8-119">Öffnen Sie den Kontakt.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-119">Open the contact.</span></span>
2. <span data-ttu-id="bcfc8-120">Wählen Sie die Aktion **Unternehmen** und dann die **Branchen**-Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-120">Choose the **Company** action, and then the **Industry Groups** action.</span></span> <span data-ttu-id="bcfc8-121">Das Fenster **Kontakt Branchen** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-121">The **Contact Industry Groups** window opens.</span></span>
3. <span data-ttu-id="bcfc8-122">Wählen Sie im Feld **Branchencode** die Branchen aus, die Sie zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-122">In the **Industry Groups Code** field, select the industry groups you want to assign.</span></span>

<span data-ttu-id="bcfc8-123">Wiederholen Sie diese Schritte, um beliebig viele Branchen einzurichten.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-123">Repeat these steps to assign as many industry groups as you want.</span></span> <span data-ttu-id="bcfc8-124">Sie können in dem Fenster Kontaktübersicht ebenfalls Branchen zuordnen, indem Sie denselben Schritten folgen.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-124">You can also assign industry groups from the contact list by following the same procedure.</span></span>

<span data-ttu-id="bcfc8-125">Die Anzahl der Branchen, die Sie dem Kontakt zugeordnet haben, wird im Feld **Anzahl Branchen** im Inforegister **Segmentierung** im Fenster **Kontakt** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-125">The number of industry groups that you have assigned to the contact is displayed in the **No. of Industry Groups** field in the **Segmentation** section in the **Contact** window.</span></span>

<span data-ttu-id="bcfc8-126">Nachdem Sie Ihren Kontakten Branchen zugeordnet haben, können Sie diese Informationen verwenden, um Kontakte für Ihre Segmente auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="bcfc8-126">After you have assigned industry groups to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="bcfc8-127">Weitere Informationen finden Sie unter [Hinzufügen von Kontakten zu Segmenten](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="bcfc8-127">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="bcfc8-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bcfc8-128">See Also</span></span>
[<span data-ttu-id="bcfc8-129">Kontaktunternehmenerstellen</span><span class="sxs-lookup"><span data-stu-id="bcfc8-129">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="bcfc8-130">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bcfc8-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

