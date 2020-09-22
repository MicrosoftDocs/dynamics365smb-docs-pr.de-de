---
title: Zusätzliche Zeilen hinzufügen, um Zusatztext für Beschreibungen zu definieren
description: Sie können zusätzliche Zeilen hinzufügen, um den Standardtext zu erweitern, der einen Artikel, ein Sachkonto oder andere Daten beschreibt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 07/08/2020
ms.author: edupont
ms.openlocfilehash: cf0418f4182e9d66da88af9262dd807a34dd3572
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3782318"
---
# <a name="add-extended-text"></a><span data-ttu-id="31d48-103">Textbaustein hinzufügen</span><span class="sxs-lookup"><span data-stu-id="31d48-103">Add Extended Text</span></span>

<span data-ttu-id="31d48-104">Sie können die Beschreibung für Artikel, Lagerhaltungsdaten, Sachkonten und Ressourcen erweitern, indem Sie zusätzliche Zeilen als Textbaustein hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="31d48-104">You can extend the description for items, stock-keeping units, general ledger accounts, and resources by adding extra lines as extended text.</span></span> <span data-ttu-id="31d48-105">Sie können auch Bedingungen für die Verwendung der zusätzlichen Zeilen festlegen.</span><span class="sxs-lookup"><span data-stu-id="31d48-105">You can also set up conditions for use of the extra lines.</span></span>  

<span data-ttu-id="31d48-106">Im folgenden Abschnitt wird beschrieben, wie Sie einer Beschreibung eines Elements einen Textbaustein hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="31d48-106">The following section describes how to add extended text to a description of an item.</span></span> <span data-ttu-id="31d48-107">Die gleichen Schritte gelten jedoch für Lagerhaltungsdaten, Sachkonten und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="31d48-107">But the same steps apply to stock-keeping units, general ledger accounts, and resources.</span></span>  

## <a name="to-define-extended-text-for-an-description"></a><span data-ttu-id="31d48-108">So definieren Sie Textbausteine für eine Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31d48-108">To define extended text for an description</span></span>

1. <span data-ttu-id="31d48-109">Öffnen Sie die Karte eines Artikels, dem Sie den zusätzlichen Text hinzufügen möchten, und wählen Sie dann die Aktion **Textbaustein** aus.</span><span class="sxs-lookup"><span data-stu-id="31d48-109">Open the card for an item that you want to add extended text to, and then choose the **Extended Text** action.</span></span>
2. <span data-ttu-id="31d48-110">Füllen Sie die Felder **Code** und **Beschreibung** aus.</span><span class="sxs-lookup"><span data-stu-id="31d48-110">Fill in the **Code** and **Description** fields.</span></span>
3. <span data-ttu-id="31d48-111">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="31d48-111">Choose the **New**.</span></span>
4. <span data-ttu-id="31d48-112">Füllen Sie das Feld **Sprachcode** oder das Kontrollkästchen **Alle Sprachcodes** aus, wenn Sie mit Sprachcodes arbeiten.</span><span class="sxs-lookup"><span data-stu-id="31d48-112">Fill in the **Language Code** field or select the **All Language Codes** check box if you use language codes.</span></span>
5. <span data-ttu-id="31d48-113">Füllen Sie die Felder **Startdatum** und/oder **Enddatum** aus, wenn Sie die Verwendung des Textbausteins zeitlich einschränken möchten.</span><span class="sxs-lookup"><span data-stu-id="31d48-113">Fill in the **Starting Date** and **Ending Date** fields if you want to limit the dates on which the extended text is used.</span></span>
6. <span data-ttu-id="31d48-114">Geben Sie im Feld **Text** den erweiterten Text ein.</span><span class="sxs-lookup"><span data-stu-id="31d48-114">In the **Text** field, write the extended text.</span></span>
7. <span data-ttu-id="31d48-115">Wählen Sie die entsprechenden Kontrollkästchen für die Belegarten, für die die Textbausteine gedruckt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="31d48-115">Select relevant check boxes for the document types where you want the extended text printed.</span></span>
8. <span data-ttu-id="31d48-116">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="31d48-116">Close the page.</span></span>

<span data-ttu-id="31d48-117">Sie können diesen Textbaustein jetzt Dokumenten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="31d48-117">You can now add this extended text to documents.</span></span> <span data-ttu-id="31d48-118">Im folgenden Verfahren wird erläutert, wie Sie einem Verkaufsauftrag einen Textbaustein hinzufügen. Die gleichen Schritte gelten jedoch auch für alle anderen Dokumente, die Sie für den Textbaustein angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="31d48-118">The following procedure explains how to add extended text to a sales order, but the same steps apply to any other document that you specified for the extended text.</span></span>  

## <a name="to-add-an-extended-item-text-on-a-sales-order-line"></a><span data-ttu-id="31d48-119">Einen erweiterten Elementtext in einer Verkaufsauftragszeile hinzufügen</span><span class="sxs-lookup"><span data-stu-id="31d48-119">To add an extended item text on a sales order line</span></span>

1. <span data-ttu-id="31d48-120">Öffnen Sie einen Verkaufsauftrag mit einer Verkaufszeile für einen Artikel, die den Textbaustein definiert hat.</span><span class="sxs-lookup"><span data-stu-id="31d48-120">Open a sales order with a sales line for an item that has extended text defined.</span></span> <span data-ttu-id="31d48-121">Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)</span><span class="sxs-lookup"><span data-stu-id="31d48-121">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="31d48-122">Wählen Sie die betreffende Zeile aus, und wählen Sie die **Textbaustein einfügen** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="31d48-122">Select the line in question, and then choose the **Insert Ext. Text** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="31d48-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31d48-123">See Also</span></span>

[<span data-ttu-id="31d48-124">Bestand einrichten</span><span class="sxs-lookup"><span data-stu-id="31d48-124">Setting Up Inventory</span></span>](inventory-setup-inventory.md)  
<span data-ttu-id="31d48-125">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="31d48-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
