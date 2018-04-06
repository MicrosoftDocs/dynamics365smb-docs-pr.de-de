---
title: 'Gewusst wie: Einrichten von Lieferbenachrichtigungen'
description: "In [Finance and Operations, Business edition können Sie Lieferbenachrichtigungen nutzen, um Verkäufer über verspätete Lieferungen zu mahnen."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 449668d5ba5b16036318d815524e1849ce51348c
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-delivery-reminders"></a><span data-ttu-id="5f169-103">Gewusst wie: Einrichten von Lieferbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="5f169-103">Set Up Delivery Reminders</span></span>
<span data-ttu-id="5f169-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] können Sie Lieferbenachrichtigungen nutzen, um Verkäufer über verspätete Lieferungen zu mahnen.</span><span class="sxs-lookup"><span data-stu-id="5f169-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can use purchase delivery reminders to remind vendors about overdue deliveries.</span></span> <span data-ttu-id="5f169-105">Um Lieferanmahnungen für Kreditoren zu erstellen, müssen Sie die Stammdaten für die Erstellung von Lieferanmahnungen sowie die Nummernserien für die Lieferanmahnungen in dem Fenster **Kreditoren & Einkauf einrichten** einrichten.</span><span class="sxs-lookup"><span data-stu-id="5f169-105">To create delivery reminders for vendors, you must set up base data for delivery reminder creation and number series for the delivery reminders in the **Purchases & Payables Setup** window.</span></span>  

## <a name="to-set-up-delivery-reminders"></a><span data-ttu-id="5f169-106">Gewusst wie: Einrichten von Lieferbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="5f169-106">To set up delivery reminders</span></span>  

1.  <span data-ttu-id="5f169-107">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht  suchen")und geben **Kreditoren- und Debitoren-Einrichtung** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="5f169-107">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5f169-108">Wählen Sie im Inforegister **Allgemein** im Feld **Standard ENTF. Abbau, AfA**, geben Sie eine der folgenden Optionen an, wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5f169-108">On the **General** FastTab, in the **Default Del. Rem. Date Field** field, specify one of the following options as described in the following table.</span></span>  

    |<span data-ttu-id="5f169-109">Option</span><span class="sxs-lookup"><span data-stu-id="5f169-109">Option</span></span>|<span data-ttu-id="5f169-110">Description</span><span class="sxs-lookup"><span data-stu-id="5f169-110">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="5f169-111">**Gewünschtes Wareneingangsdatum**</span><span class="sxs-lookup"><span data-stu-id="5f169-111">**Requested Receipt Date**</span></span>|<span data-ttu-id="5f169-112">Um anzugeben, dass der Datumswert im Feld **Gewünschtes Wareneingangsdatum** in der Bestellzeile als Standarddatum für die Erstellung von Lieferanmahnungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5f169-112">To specify that the date value in the **Requested Receipt Date** field on the purchase order line will be used as the default date for creating delivery reminders.</span></span>|  
    |<span data-ttu-id="5f169-113">**Zugesagtes Wareneingangsdatum**</span><span class="sxs-lookup"><span data-stu-id="5f169-113">**Promised Receipt Date**</span></span>|<span data-ttu-id="5f169-114">Um anzugeben, dass der Datumswert im Feld **Gewünschtes Wareneingangsdatum** in der Bestellzeile als Standarddatum für die Erstellung von Lieferanmahnungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5f169-114">To specify that the date value in the **Promised Receipt Date** field on the purchase order line will be used as the default date for creating delivery reminders.</span></span>|  
    |<span data-ttu-id="5f169-115">**Erwartetes Wareneingangsdatum**</span><span class="sxs-lookup"><span data-stu-id="5f169-115">**Expected Receipt Date**</span></span>|<span data-ttu-id="5f169-116">Um anzugeben, dass der Datumswert im Feld **Erwartetes Wareneingangsdatum** in der Bestellzeile als Standarddatum für die Erstellung von Lieferanmahnungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5f169-116">To specify that the date value in the **Expected Receipt Date** field on the purchase order line will be used as the default date for creating delivery reminders.</span></span>|  

3.  <span data-ttu-id="5f169-117">Füllen Sie im Inforegister **Nummerierung** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="5f169-117">On the **Numbering** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="5f169-118">Feld</span><span class="sxs-lookup"><span data-stu-id="5f169-118">Field</span></span>|<span data-ttu-id="5f169-119">Description</span><span class="sxs-lookup"><span data-stu-id="5f169-119">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="5f169-120">**Lieferbenachrichtigungsnummern**</span><span class="sxs-lookup"><span data-stu-id="5f169-120">**Delivery Reminder Nos.**</span></span>|<span data-ttu-id="5f169-121">Der Nummernseriencode für Lieferanmahnungen.</span><span class="sxs-lookup"><span data-stu-id="5f169-121">The number series code for delivery reminders.</span></span>|  
    |<span data-ttu-id="5f169-122">**Reg. Lieferbenachrichtigungsnummern**</span><span class="sxs-lookup"><span data-stu-id="5f169-122">**Issued Delivery Reminder Nos.**</span></span>|<span data-ttu-id="5f169-123">Der Nummernseriencode für ausgegebene Lieferanmahnungen.</span><span class="sxs-lookup"><span data-stu-id="5f169-123">The number series code for issued delivery reminders.</span></span>|  

4.  <span data-ttu-id="5f169-124">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="5f169-124">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5f169-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f169-125">See Also</span></span>  
 <span data-ttu-id="5f169-126">[Lieferbenachrichtigungen](delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="5f169-126">[Delivery Reminders](delivery-reminders.md) </span></span>  
 <span data-ttu-id="5f169-127">[Einrichten von Lieferbenachrichtigungsbestimmungen, Stufen und Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md) </span><span class="sxs-lookup"><span data-stu-id="5f169-127">[Set Up Delivery Reminder Terms, Levels, and Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md) </span></span>  
 <span data-ttu-id="5f169-128">[So werden Lieferbenachrichtigungscodes zu Kreditoren zugewiesen](how-to-assign-delivery-reminder-codes-to-vendors.md) </span><span class="sxs-lookup"><span data-stu-id="5f169-128">[Assign Delivery Reminder Codes to Vendors](how-to-assign-delivery-reminder-codes-to-vendors.md) </span></span>  
 [<span data-ttu-id="5f169-129">So erstellen Sie Lieferanmahnungen manuell</span><span class="sxs-lookup"><span data-stu-id="5f169-129">Create Delivery Reminders Manually</span></span>](how-to-create-delivery-reminders-manually.md)

