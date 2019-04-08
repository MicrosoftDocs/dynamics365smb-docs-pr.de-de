---
title: Vorbereiten zur Einrichtung von Geschäftsbeziehungscodes für Kontakte | Microsoft Docs
description: Geschäftsbeziehungen in Business Central werden verwendet, um das Marketing zu erleichtern und um die Geschäftsbeziehung anzuzeigen, die Sie mit Ihren Interessenten, Debitoren und Debitoren haben, wie z. B. Bank oder Dienstleister.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 10/01/2018
ms.author: jswymer
redirect_url: marketing-create-contact-companies
ms.openlocfilehash: cb600ea688a856f481d84604d6966231fe7f536d
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "798718"
---
# <a name="setting-up-business-relations-on-contacts"></a><span data-ttu-id="f774d-103">Einrichten von Geschäftsbeziehungen für Kontakte</span><span class="sxs-lookup"><span data-stu-id="f774d-103">Setting Up Business Relations on Contacts</span></span>
<span data-ttu-id="f774d-104">Sie können Geschäftsbeziehungen verwenden, um die Geschäftsbeziehung anzuzeigen, die Sie mit Ihren Kontakten haben wie z. B. Interessent, Bank, Berater und Dienstleister usw. pflegen.</span><span class="sxs-lookup"><span data-stu-id="f774d-104">You can use business relations to indicate the business relationship you have with your contacts, for example, a prospect, bank, consultant, service supplier, and so on.</span></span>

<span data-ttu-id="f774d-105">Die Nutzung von Geschäftsbeziehungen zu Kontakten ist ein zwei Schritte umfassender Prozess.</span><span class="sxs-lookup"><span data-stu-id="f774d-105">Using business relations on contacts is a two-step process.</span></span> <span data-ttu-id="f774d-106">Zuerst definieren Sie den Geschäftsbeziehungscode.</span><span class="sxs-lookup"><span data-stu-id="f774d-106">First, you define the business relation code.</span></span> <span data-ttu-id="f774d-107">Sie müssen diesen Schritt nur einmal für jede Geschäftsbeziehung ausführen.</span><span class="sxs-lookup"><span data-stu-id="f774d-107">You only have to perform this step one time for each business relation.</span></span> <span data-ttu-id="f774d-108">Sobald Sie einen Geschäftsbeziehungscode haben, können Sie den Code zu den Kontaktunternehmen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="f774d-108">Once you have a business relation code, you can start to assign the code to contact companies.</span></span>

> [!NOTE]  
>   <span data-ttu-id="f774d-109">Wenn Sie planen, Ihre Kontakte mit Debitoren, Kreditoren oder Bankkonten in anderen Teilen der Anwendung zu synchronisieren, können Sie für sie eine Geschäftsbeziehung erstellen.</span><span class="sxs-lookup"><span data-stu-id="f774d-109">If you plan to synchronize your contacts with vendors, customers, or bank accounts in other parts of the application, you may want to set up a business relation for them.</span></span>

## <a name="to-define-a-business-relation-code"></a><span data-ttu-id="f774d-110">Definieren eines Geschäftsbeziehungscodes</span><span class="sxs-lookup"><span data-stu-id="f774d-110">To define a business relation code</span></span>
<span data-ttu-id="f774d-111">Der Geschäftsbeziehungscode definiert eine Kategorie oder einen Typ von Geschäftsbeziehung wie BANK oder Gesetz.</span><span class="sxs-lookup"><span data-stu-id="f774d-111">The business relation code defines a category or type of the business relationship, such as BANK or Law.</span></span> <span data-ttu-id="f774d-112">Sie können mehrere Geschäftsbeziehungscodes haben.</span><span class="sxs-lookup"><span data-stu-id="f774d-112">You can have several business relation codes.</span></span> <span data-ttu-id="f774d-113">Um die Geschäftsbeziehung zu definieren, verwenden Sie die Seite **Geschäftsbeziehungen**.</span><span class="sxs-lookup"><span data-stu-id="f774d-113">To define the business relation, you use the **Business Relations** page.</span></span>

1. <span data-ttu-id="f774d-114">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Geschäftsbeziehung** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="f774d-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Business Relations**, and then choose the related link.</span></span>
2. <span data-ttu-id="f774d-115">Wählen Sie die Aktion **Neu** aus, und geben Sie einen Code und eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="f774d-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="f774d-116">Der Code kann maximal 11 Zeichen, sowohl Ziffern als auch Buchstaben, umfassen.</span><span class="sxs-lookup"><span data-stu-id="f774d-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <span data-ttu-id="f774d-117"><a name="AssignBusRelContact">Um Kontakten Geschäftsbeziehungen zuzuordnen:</a></span><span class="sxs-lookup"><span data-stu-id="f774d-117"><a name="AssignBusRelContact"></a> To assign business relations to a contact</span></span>
<span data-ttu-id="f774d-118">Sie können Geschäftsbeziehungen nicht zu Personen zuordnen – nur zu Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="f774d-118">You cannot assign business relations to a contact person - only companies.</span></span>

1. <span data-ttu-id="f774d-119">Öffnen Sie den Kontakt.</span><span class="sxs-lookup"><span data-stu-id="f774d-119">Open the contact.</span></span>
2. <span data-ttu-id="f774d-120">Wählen Sie die Aktion **Unternehmen** und dann die **Geschäftsbeziehungen**-Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="f774d-120">Choose the **Company** action, and then the **Business Relations** action.</span></span>

    <span data-ttu-id="f774d-121">Die Seite **Kontakt Geschäftsbeziehungen** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f774d-121">The **Contact Business Relations** page opens.</span></span>
3. <span data-ttu-id="f774d-122">Wählen Sie im Feld **Geschäftsbeziehungscode** die Geschäftsbeziehung aus, die Sie zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="f774d-122">In the **Business Relation Code** field, select the business relation you want to assign.</span></span>

<span data-ttu-id="f774d-123">Wiederholen Sie diese Schritte, um beliebig viele Geschäftsbeziehungen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="f774d-123">Repeat these steps to assign as many business relations as you want.</span></span> <span data-ttu-id="f774d-124">Außerdem können Sie Geschäftsbeziehungen auf die gleiche Art in dem Fenster Kontaktübersicht zuordnen.</span><span class="sxs-lookup"><span data-stu-id="f774d-124">You can also assign business relations from the contact list by following the same procedure.</span></span>

<span data-ttu-id="f774d-125">Die Anzahl der Geschäftsbeziehungen, die Sie dem Kontakt auf der Kontaktkarte zugeordnet haben, wird im Feld **Anzahl Geschäftsbeziehungen** im Abschnitt **Segmentierung** auf der Seite **Kontakt** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f774d-125">The number of business relations you have assigned to the contact is displayed in the **No. of Business Relations** field in the **Segmentation** section on the **Contact** page.</span></span>

<span data-ttu-id="f774d-126">Nachdem Sie Ihren Kontakten Geschäftsbeziehungen zugeordnet haben, können Sie diese Informationen verwenden, um Kontakte für Ihre Segmente auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="f774d-126">After you have assigned business relations to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="f774d-127">Weitere Informationen finden Sie unter [Hinzufügen von Kontakten zu Segmenten](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="f774d-127">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="f774d-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f774d-128">See Also</span></span>
<span data-ttu-id="f774d-129">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f774d-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
