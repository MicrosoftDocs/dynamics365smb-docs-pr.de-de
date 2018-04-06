---
title: 'Gewusst wie: Lieferbenachrichtigungen manuell erstellen'
description: "Mahnt Ihre Debitoren wegen überfälliger Lieferung."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 828145173d6e98e9c88b3d4189d37ef952567729
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="create-delivery-reminders-manually"></a><span data-ttu-id="e17ee-103">So erstellen Sie Lieferanmahnungen manuell</span><span class="sxs-lookup"><span data-stu-id="e17ee-103">Create Delivery Reminders Manually</span></span>
<span data-ttu-id="e17ee-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], können Sie Lieferbenachrichtigungen erstellen, wenn eine Bestellung nicht wie erwartet geliefert wurde.</span><span class="sxs-lookup"><span data-stu-id="e17ee-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can create delivery reminders when a purchase has not been delivered as expected.</span></span> <span data-ttu-id="e17ee-105">Sie können eine einzelne Lieferbenachrichtigung manuell erstellen oder Sie können Lieferbenachrichtigungen für alle überfälligen Lieferungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="e17ee-105">You can create a single delivery reminder manually, or you can generate delivery reminders for all overdue deliveries.</span></span> <span data-ttu-id="e17ee-106">Weitere Informationen finden Sie unter [Lieferbenachrichtigungen erstellen](how-to-generate-delivery-reminders.md).</span><span class="sxs-lookup"><span data-stu-id="e17ee-106">For more information, see [Generate Delivery Reminders](how-to-generate-delivery-reminders.md).</span></span>

> [!NOTE]
> <span data-ttu-id="e17ee-107">Um Lieferanmahnungen zu erstellen, müssen Sie die Lieferanmahnungseigenschaften einrichten.</span><span class="sxs-lookup"><span data-stu-id="e17ee-107">To create delivery reminders, you must set up the delivery reminder properties.</span></span> <span data-ttu-id="e17ee-108">Weitere Informationen finden Sie unter [Lieferbenachrichtigungen erstellen](how-to-set-up-delivery-reminders.md).</span><span class="sxs-lookup"><span data-stu-id="e17ee-108">For more information, see [Set Up Delivery Reminders](how-to-set-up-delivery-reminders.md).</span></span>

## <a name="to-create-a-delivery-reminder-manually"></a><span data-ttu-id="e17ee-109">So erstellen Sie Lieferantenbenachrichtigungen manuell</span><span class="sxs-lookup"><span data-stu-id="e17ee-109">To create a delivery reminder manually</span></span>  

1.  <span data-ttu-id="e17ee-110">Wählen Sie in der rechten oberen Ecke ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen") und geben **Lieferbenachrichtigungen** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="e17ee-110">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delivery Reminder**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e17ee-111">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="e17ee-111">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="e17ee-112">Füllen Sie im Fenster **Lieferbenachrichtigung** im Inforegister **Allgemein** die erforderlichen Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="e17ee-112">In the **Delivery Reminder** window, on the **General** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="e17ee-113">Feld</span><span class="sxs-lookup"><span data-stu-id="e17ee-113">Field</span></span>|<span data-ttu-id="e17ee-114">Description</span><span class="sxs-lookup"><span data-stu-id="e17ee-114">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="e17ee-115">**Nr.**</span><span class="sxs-lookup"><span data-stu-id="e17ee-115">**No.**</span></span>|<span data-ttu-id="e17ee-116">Die eindeutige Kennnummer für die Lieferbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="e17ee-116">The unique identification number for the delivery reminder.</span></span>|  
    |<span data-ttu-id="e17ee-117">**Kreditorennr**</span><span class="sxs-lookup"><span data-stu-id="e17ee-117">**Vendor No.**</span></span>|<span data-ttu-id="e17ee-118">Gibt die Nummer des Kreditors an, für den Sie eine Lieferbenachrichtigung buchen möchten.</span><span class="sxs-lookup"><span data-stu-id="e17ee-118">The number of the vendor for whom you want to post the delivery reminder.</span></span><br /><br /> <span data-ttu-id="e17ee-119">Wenn Sie die Kreditorennummer auswählen, werden **Name**, **Adresse**, **PLZ Code/Ort** und **Kontakt** Felder automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="e17ee-119">When you select the vendor number, the **Name**, **Address**, **Post Code/City**, and **Contact** fields are filled in automatically.</span></span>|  
    |<span data-ttu-id="e17ee-120">**Buchungsdatum**</span><span class="sxs-lookup"><span data-stu-id="e17ee-120">**Posting Date**</span></span>|<span data-ttu-id="e17ee-121">Gibt das Buchungsdatum der Lieferbenachrichtigung an.</span><span class="sxs-lookup"><span data-stu-id="e17ee-121">The posting date for the delivery reminder.</span></span> <span data-ttu-id="e17ee-122">Dieses Datum wird in alle Lieferbenachrichtigung kopiert.</span><span class="sxs-lookup"><span data-stu-id="e17ee-122">This date is copied to all of the delivery reminder ledger entries.</span></span>|  
    |<span data-ttu-id="e17ee-123">**Belegdatum**</span><span class="sxs-lookup"><span data-stu-id="e17ee-123">**Document Date**</span></span>|<span data-ttu-id="e17ee-124">Gibt das Dokumentdatum der Lieferbenachrichtigung an.</span><span class="sxs-lookup"><span data-stu-id="e17ee-124">The document date for the delivery reminder.</span></span> <span data-ttu-id="e17ee-125">Dieses Datum wird auch verwendet, um das Fälligkeitsdatum der Lieferbenachrichtigung zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="e17ee-125">This date is also used to calculate the due date for the delivery reminder.</span></span> <span data-ttu-id="e17ee-126">Sie können das Buchungsdatum bei Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="e17ee-126">You can modify the posting date if required.</span></span>|  
    |<span data-ttu-id="e17ee-127">**Mahnstufe**</span><span class="sxs-lookup"><span data-stu-id="e17ee-127">**Reminder Level**</span></span>|<span data-ttu-id="e17ee-128">Lieferbenachrichtigungsstufe.</span><span class="sxs-lookup"><span data-stu-id="e17ee-128">The delivery reminder level.</span></span> <span data-ttu-id="e17ee-129">Dieser Wert basiert auf der Anzahl von Lieferbenachrichtigung, die bereits gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="e17ee-129">This value is based on the number of delivery reminders that have already been sent.</span></span> <span data-ttu-id="e17ee-130">Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Lieferbenachrichtigungen](how-to-set-up-delivery-reminder-terms-levels-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="e17ee-130">For more information, see [Set Up Delivery Reminder Terms, Levels, and Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md).</span></span>|  
    |<span data-ttu-id="e17ee-131">**Mahnmethodencode**</span><span class="sxs-lookup"><span data-stu-id="e17ee-131">**Reminder Terms Code**</span></span>|<span data-ttu-id="e17ee-132">Gibt den Lieferbenachrichtigungscode für den Kreditor an.</span><span class="sxs-lookup"><span data-stu-id="e17ee-132">Specify the delivery reminder terms code that is set up for the vendor.</span></span>|  
    |<span data-ttu-id="e17ee-133">**Fälligkeitsdatum**</span><span class="sxs-lookup"><span data-stu-id="e17ee-133">**Due Date**</span></span>|<span data-ttu-id="e17ee-134">Gibt das Fälligkeitsdatum der Lieferbenachrichtigung an.</span><span class="sxs-lookup"><span data-stu-id="e17ee-134">The due date for the delivery reminder.</span></span>|  

4.  <span data-ttu-id="e17ee-135">Wählen Sie die Aktion **Mahnungszeile vorschlagen**.</span><span class="sxs-lookup"><span data-stu-id="e17ee-135">Choose the **Suggest Reminder Lines** action</span></span>  

    <span data-ttu-id="e17ee-136">Wenn es überfällige Lieferungen vom angegebenen Kreditor gibt, werden diese der Lieferbenachrichtigung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e17ee-136">If there are overdue deliveries from the specified vendor, these are added to the deliver reminder.</span></span>  

5.  <span data-ttu-id="e17ee-137">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="e17ee-137">Choose the **OK** button.</span></span>  

    <span data-ttu-id="e17ee-138">Lieferbenachrichtigung wurde erstellt.</span><span class="sxs-lookup"><span data-stu-id="e17ee-138">The delivery reminder is created.</span></span> <span data-ttu-id="e17ee-139">So können die Lieferbenachrichtigungen ausgeben und erstellen.</span><span class="sxs-lookup"><span data-stu-id="e17ee-139">You can now issue and print the delivery reminder.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e17ee-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e17ee-140">See Also</span></span>  
 <span data-ttu-id="e17ee-141">[Lieferbenachrichtigungen](delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="e17ee-141">[Delivery Reminders](delivery-reminders.md) </span></span>  
 <span data-ttu-id="e17ee-142">[So erstellen Sie Lieferanmahnungen](how-to-generate-delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="e17ee-142">[Generate Delivery Reminders](how-to-generate-delivery-reminders.md) </span></span>  
 <span data-ttu-id="e17ee-143">[Gewusst wie: Einrichten von Lieferbenachrichtigungen](how-to-set-up-delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="e17ee-143">[Set Up Delivery Reminders](how-to-set-up-delivery-reminders.md) </span></span>  
 <span data-ttu-id="e17ee-144">[Einrichten von Lieferbenachrichtigungsbestimmungen, Stufen und Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md) </span><span class="sxs-lookup"><span data-stu-id="e17ee-144">[Set Up Delivery Reminder Terms, Levels, and Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md) </span></span>  
 <span data-ttu-id="e17ee-145">[So werden Lieferbenachrichtigungscodes zu Kreditoren zugewiesen](how-to-assign-delivery-reminder-codes-to-vendors.md) </span><span class="sxs-lookup"><span data-stu-id="e17ee-145">[Assign Delivery Reminder Codes to Vendors](how-to-assign-delivery-reminder-codes-to-vendors.md) </span></span>  
 <span data-ttu-id="e17ee-146">[Lieferbenachrichtigung registrieren](how-to-issue-delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="e17ee-146">[Issue Delivery Reminders](how-to-issue-delivery-reminders.md) </span></span>  
 [<span data-ttu-id="e17ee-147">So drucken Sie Testberichte vor dem Registrieren von Lieferanmahnungen</span><span class="sxs-lookup"><span data-stu-id="e17ee-147">Print Test Reports for Delivery Reminders</span></span>](how-to-print-test-reports-for-delivery-reminders.md)

