---
title: 'Gewusst wie: Einrichten von Lieferbenachrichtigungen'
description: In Business Central können Sie Lieferbenachrichtigungen nutzen, um Verkäufer über verspätete Lieferungen zu mahnen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/23/2020
ms.author: sgroespe
ms.openlocfilehash: 3fe1a3dca9a5ab1d561ff0ad9c1b4f2ab45dc990
ms.sourcegitcommit: 007b331b6974983ee614db0406f00777da359ecb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/10/2020
ms.locfileid: "3676550"
---
# <a name="set-up-delivery-reminders"></a><span data-ttu-id="c3d56-103">Gewusst wie: Einrichten von Lieferbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="c3d56-103">Set Up Delivery Reminders</span></span>

<span data-ttu-id="c3d56-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] können Sie Lieferbenachrichtigungen nutzen, um Verkäufer über verspätete Lieferungen zu mahnen.</span><span class="sxs-lookup"><span data-stu-id="c3d56-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can use purchase delivery reminders to remind vendors about overdue deliveries.</span></span> <span data-ttu-id="c3d56-105">Um Lieferanmahnungen für Kreditoren zu erstellen, müssen Sie die Stammdaten für die Erstellung von Lieferanmahnungen sowie die Nummernserien für die Lieferanmahnungen auf der Seite Fenster **Kreditoren & Einkauf einrichten** einrichten.</span><span class="sxs-lookup"><span data-stu-id="c3d56-105">To create delivery reminders for vendors, you must set up base data for delivery reminder creation and number series for the delivery reminders on the **Purchases & Payables Setup** page.</span></span>  

## <a name="to-set-up-delivery-reminders"></a><span data-ttu-id="c3d56-106">Gewusst wie: Einrichten von Lieferbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="c3d56-106">To set up delivery reminders</span></span>  

1. <span data-ttu-id="c3d56-107">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](../../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Einrichten von Einkäufen und Verbindlichkeiten** ein, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="c3d56-107">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c3d56-108">Wählen Sie im Inforegister **Allgemein** im Feld **Standard ENTF. Abbau, AfA**, geben Sie eine der folgenden Optionen an, wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c3d56-108">On the **General** FastTab, in the **Default Del. Rem. Date Field** field, specify one of the following options as described in the following table.</span></span>  

    |<span data-ttu-id="c3d56-109">Option</span><span class="sxs-lookup"><span data-stu-id="c3d56-109">Option</span></span>|<span data-ttu-id="c3d56-110">Description</span><span class="sxs-lookup"><span data-stu-id="c3d56-110">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="c3d56-111">**Gewünschtes Wareneingangsdatum**</span><span class="sxs-lookup"><span data-stu-id="c3d56-111">**Requested Receipt Date**</span></span>|<span data-ttu-id="c3d56-112">Um anzugeben, dass der Datumswert im Feld **Gewünschtes Wareneingangsdatum** in der Bestellzeile als Standarddatum für die Erstellung von Lieferanmahnungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3d56-112">To specify that the date value in the **Requested Receipt Date** field on the purchase order line will be used as the default date for creating delivery reminders.</span></span>|  
    |<span data-ttu-id="c3d56-113">**Zugesagtes Wareneingangsdatum**</span><span class="sxs-lookup"><span data-stu-id="c3d56-113">**Promised Receipt Date**</span></span>|<span data-ttu-id="c3d56-114">Um anzugeben, dass der Datumswert im Feld **Gewünschtes Wareneingangsdatum** in der Bestellzeile als Standarddatum für die Erstellung von Lieferanmahnungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3d56-114">To specify that the date value in the **Promised Receipt Date** field on the purchase order line will be used as the default date for creating delivery reminders.</span></span>|  
    |<span data-ttu-id="c3d56-115">**Erwartetes Wareneingangsdatum**</span><span class="sxs-lookup"><span data-stu-id="c3d56-115">**Expected Receipt Date**</span></span>|<span data-ttu-id="c3d56-116">Um anzugeben, dass der Datumswert im Feld **Erwartetes Wareneingangsdatum** in der Bestellzeile als Standarddatum für die Erstellung von Lieferanmahnungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3d56-116">To specify that the date value in the **Expected Receipt Date** field on the purchase order line will be used as the default date for creating delivery reminders.</span></span>|  

3. <span data-ttu-id="c3d56-117">Füllen Sie im Inforegister **Nummerierung** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="c3d56-117">On the **Numbering** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="c3d56-118">Feld</span><span class="sxs-lookup"><span data-stu-id="c3d56-118">Field</span></span>|<span data-ttu-id="c3d56-119">Description</span><span class="sxs-lookup"><span data-stu-id="c3d56-119">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="c3d56-120">**Lieferbenachrichtigungsnummern**</span><span class="sxs-lookup"><span data-stu-id="c3d56-120">**Delivery Reminder Nos.**</span></span>|<span data-ttu-id="c3d56-121">Der Nummernseriencode für Lieferanmahnungen.</span><span class="sxs-lookup"><span data-stu-id="c3d56-121">The number series code for delivery reminders.</span></span>|  
    |<span data-ttu-id="c3d56-122">**Reg. Lieferbenachrichtigungsnummern**</span><span class="sxs-lookup"><span data-stu-id="c3d56-122">**Issued Delivery Reminder Nos.**</span></span>|<span data-ttu-id="c3d56-123">Der Nummernseriencode für ausgegebene Lieferanmahnungen.</span><span class="sxs-lookup"><span data-stu-id="c3d56-123">The number series code for issued delivery reminders.</span></span>|  

4. <span data-ttu-id="c3d56-124">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="c3d56-124">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c3d56-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3d56-125">See Also</span></span>

[<span data-ttu-id="c3d56-126">Lieferbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="c3d56-126">Delivery Reminders</span></span>](delivery-reminders.md)  
[<span data-ttu-id="c3d56-127">Einrichten von Lieferbenachrichtigungsbestimmungen, Stufen und Text</span><span class="sxs-lookup"><span data-stu-id="c3d56-127">Set Up Delivery Reminder Terms, Levels, and Text</span></span>](how-to-set-up-delivery-reminder-terms-levels-and-text.md)  
[<span data-ttu-id="c3d56-128">So werden Lieferbenachrichtigungscodes zu Kreditoren zugewiesen</span><span class="sxs-lookup"><span data-stu-id="c3d56-128">Assign Delivery Reminder Codes to Vendors</span></span>](how-to-assign-delivery-reminder-codes-to-vendors.md)  
[<span data-ttu-id="c3d56-129">So erstellen Sie Lieferbenachrichtungen manuell</span><span class="sxs-lookup"><span data-stu-id="c3d56-129">Create Delivery Reminders Manually</span></span>](how-to-create-delivery-reminders-manually.md)
