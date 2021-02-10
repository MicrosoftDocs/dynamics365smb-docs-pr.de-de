---
title: Zusätzliche Zeilen hinzufügen, um Zusatztext für Beschreibungen zu definieren
description: Sie können zusätzliche Zeilen hinzufügen, um den Standardtext zu erweitern, der einen Artikel, ein Sachkonto oder andere Daten beschreibt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9e443a44135bbdaf75f6a064370983592797b10b
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756917"
---
# <a name="add-extended-text"></a><span data-ttu-id="d1d74-103">Textbaustein hinzufügen</span><span class="sxs-lookup"><span data-stu-id="d1d74-103">Add Extended Text</span></span>

<span data-ttu-id="d1d74-104">Sie können die Beschreibung für Artikel, Lagerhaltungsdaten, Sachkonten und Ressourcen erweitern, indem Sie zusätzliche Zeilen als Textbaustein hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d1d74-104">You can extend the description for items, stock-keeping units, general ledger accounts, and resources by adding extra lines as extended text.</span></span> <span data-ttu-id="d1d74-105">Sie können auch Bedingungen für die Verwendung der zusätzlichen Zeilen festlegen.</span><span class="sxs-lookup"><span data-stu-id="d1d74-105">You can also set up conditions for use of the extra lines.</span></span>  

<span data-ttu-id="d1d74-106">Im folgenden Abschnitt wird beschrieben, wie Sie einer Beschreibung eines Elements einen Textbaustein hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d1d74-106">The following section describes how to add extended text to a description of an item.</span></span> <span data-ttu-id="d1d74-107">Die gleichen Schritte gelten jedoch für Lagerhaltungsdaten, Sachkonten und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="d1d74-107">But the same steps apply to stock-keeping units, general ledger accounts, and resources.</span></span>  

## <a name="to-define-extended-text-for-an-description"></a><span data-ttu-id="d1d74-108">So definieren Sie Textbausteine für eine Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1d74-108">To define extended text for an description</span></span>

1. <span data-ttu-id="d1d74-109">Öffnen Sie die Karte eines Artikels, dem Sie den zusätzlichen Text hinzufügen möchten, und wählen Sie dann die Aktion **Textbaustein** aus.</span><span class="sxs-lookup"><span data-stu-id="d1d74-109">Open the card for an item that you want to add extended text to, and then choose the **Extended Text** action.</span></span>
2. <span data-ttu-id="d1d74-110">Füllen Sie die Felder **Code** und **Beschreibung** aus.</span><span class="sxs-lookup"><span data-stu-id="d1d74-110">Fill in the **Code** and **Description** fields.</span></span>
3. <span data-ttu-id="d1d74-111">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="d1d74-111">Choose the **New**.</span></span>
4. <span data-ttu-id="d1d74-112">Füllen Sie das Feld **Sprachcode** oder das Kontrollkästchen **Alle Sprachcodes** aus, wenn Sie mit Sprachcodes arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d1d74-112">Fill in the **Language Code** field or select the **All Language Codes** check box if you use language codes.</span></span>
5. <span data-ttu-id="d1d74-113">Füllen Sie die Felder **Startdatum** und/oder **Enddatum** aus, wenn Sie die Verwendung des Textbausteins zeitlich einschränken möchten.</span><span class="sxs-lookup"><span data-stu-id="d1d74-113">Fill in the **Starting Date** and **Ending Date** fields if you want to limit the dates on which the extended text is used.</span></span>
6. <span data-ttu-id="d1d74-114">Geben Sie im Feld **Text** den erweiterten Text ein.</span><span class="sxs-lookup"><span data-stu-id="d1d74-114">In the **Text** field, write the extended text.</span></span>
7. <span data-ttu-id="d1d74-115">Wählen Sie die entsprechenden Kontrollkästchen für die Belegarten, für die die Textbausteine gedruckt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d1d74-115">Select relevant check boxes for the document types where you want the extended text printed.</span></span>
8. <span data-ttu-id="d1d74-116">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d1d74-116">Close the page.</span></span>

<span data-ttu-id="d1d74-117">Sie können diesen Textbaustein jetzt Dokumenten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d1d74-117">You can now add this extended text to documents.</span></span> <span data-ttu-id="d1d74-118">Im folgenden Verfahren wird erläutert, wie Sie einem Verkaufsauftrag einen Textbaustein hinzufügen. Die gleichen Schritte gelten jedoch auch für alle anderen Dokumente, die Sie für den Textbaustein angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="d1d74-118">The following procedure explains how to add extended text to a sales order, but the same steps apply to any other document that you specified for the extended text.</span></span>  

## <a name="to-add-an-extended-item-text-on-a-sales-order-line"></a><span data-ttu-id="d1d74-119">Einen erweiterten Elementtext in einer Verkaufsauftragszeile hinzufügen</span><span class="sxs-lookup"><span data-stu-id="d1d74-119">To add an extended item text on a sales order line</span></span>

1. <span data-ttu-id="d1d74-120">Öffnen Sie einen Verkaufsauftrag mit einer Verkaufszeile für einen Artikel, die den Textbaustein definiert hat.</span><span class="sxs-lookup"><span data-stu-id="d1d74-120">Open a sales order with a sales line for an item that has extended text defined.</span></span> <span data-ttu-id="d1d74-121">Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)</span><span class="sxs-lookup"><span data-stu-id="d1d74-121">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="d1d74-122">Wählen Sie die betreffende Zeile aus, und wählen Sie die **Textbaustein einfügen** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="d1d74-122">Select the line in question, and then choose the **Insert Ext. Text** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="d1d74-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1d74-123">See Also</span></span>

[<span data-ttu-id="d1d74-124">Bestand einrichten</span><span class="sxs-lookup"><span data-stu-id="d1d74-124">Setting Up Inventory</span></span>](inventory-setup-inventory.md)  
<span data-ttu-id="d1d74-125">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d1d74-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
