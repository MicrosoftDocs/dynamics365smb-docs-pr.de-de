---
title: 'Gewusst wie: Einrichten von Lieferbenachrichtigungsbedingungen, -stufen und -text'
description: "Um Lieferbenachrichtigungen zu erstellen, müssen Sie bestimmte Einrichtungen festlegen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: a5230e066c072744dcd5a472c94bc661b49943cd
ms.contentlocale: de-de
ms.lasthandoff: 11/26/2018

---
# <a name="set-up-delivery-reminder-terms-levels-and-text"></a><span data-ttu-id="1dfde-103">Einrichten von Lieferbenachrichtigungsbestimmungen, Stufen und Text</span><span class="sxs-lookup"><span data-stu-id="1dfde-103">Set Up Delivery Reminder Terms, Levels, and Text</span></span>
<span data-ttu-id="1dfde-104">Um Lieferbenachrichtigung zu erstellen, müssen Sie Folgendes einrichten:</span><span class="sxs-lookup"><span data-stu-id="1dfde-104">To create delivery reminders, you must set up the following:</span></span>  

- <span data-ttu-id="1dfde-105">Lieferbenachrichtigungsbestimmungen</span><span class="sxs-lookup"><span data-stu-id="1dfde-105">Delivery reminder terms</span></span>  
- <span data-ttu-id="1dfde-106">Lieferbenachrichtigungsstufen</span><span class="sxs-lookup"><span data-stu-id="1dfde-106">Delivery reminder levels</span></span>  
- <span data-ttu-id="1dfde-107">Lieferbenachrichtigungstextnachrichten</span><span class="sxs-lookup"><span data-stu-id="1dfde-107">Delivery reminder text messages</span></span>  

<span data-ttu-id="1dfde-108">Jede Lieferbenachrichtigungsmethode verfügt über eigene Lieferbenachrichtigungsstufen, und Sie können für jede der Lieferbenachrichtigungsstufe spezielle Lieferbenachrichtigungstexte definieren.</span><span class="sxs-lookup"><span data-stu-id="1dfde-108">Each delivery reminder term has two or more delivery reminder levels, and for each delivery reminder level, you can specify text that will be part of the delivery reminder.</span></span>  

<span data-ttu-id="1dfde-109">Weitere Informationen finden Sie unter [Lieferbenachrichtigungen](delivery-reminders.md).</span><span class="sxs-lookup"><span data-stu-id="1dfde-109">For more information, see [Delivery Reminders](delivery-reminders.md).</span></span>  

## <a name="to-set-up-delivery-reminder-terms"></a><span data-ttu-id="1dfde-110">Einrichten von Lieferbenachrichtigungsmethoden</span><span class="sxs-lookup"><span data-stu-id="1dfde-110">To set up delivery reminder terms</span></span>  

1.  <span data-ttu-id="1dfde-111">Wählen Sie in der rechten oberen Ecke ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen") und geben **Lieferbenachrichtigungsmethoden** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="1dfde-111">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delivery Reminder Terms**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1dfde-112">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="1dfde-112">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="1dfde-113">Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="1dfde-113">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="1dfde-114">Feld</span><span class="sxs-lookup"><span data-stu-id="1dfde-114">Field</span></span>|<span data-ttu-id="1dfde-115">Description</span><span class="sxs-lookup"><span data-stu-id="1dfde-115">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="1dfde-116">**Code**</span><span class="sxs-lookup"><span data-stu-id="1dfde-116">**Code**</span></span>|<span data-ttu-id="1dfde-117">Der Code für das Fälligkeitsdatum der Lieferbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="1dfde-117">The code for the delivery reminder term.</span></span> <span data-ttu-id="1dfde-118">Sie können maximal 10 alphanumerische Zeichen eingeben.</span><span class="sxs-lookup"><span data-stu-id="1dfde-118">You can enter a maximum of 10 alphanumeric characters.</span></span>|  
    |<span data-ttu-id="1dfde-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1dfde-119">**Description**</span></span>|<span data-ttu-id="1dfde-120">Die Beschreibung für die Lieferbenachrichtigungsmethode.</span><span class="sxs-lookup"><span data-stu-id="1dfde-120">The description for the delivery reminder term.</span></span> <span data-ttu-id="1dfde-121">Sie können maximal 30 alphanumerische Zeichen eingeben.</span><span class="sxs-lookup"><span data-stu-id="1dfde-121">You can enter a maximum of 30 alphanumeric characters.</span></span>|  
    |<span data-ttu-id="1dfde-122">**Max. Anzahl Lieferbenachrichtigungen**</span><span class="sxs-lookup"><span data-stu-id="1dfde-122">**Max. No. of Delivery Reminders**</span></span>|<span data-ttu-id="1dfde-123">Gibt die maximale Anzahl von Lieferbenachrichtigungen an, die für eine Bestellung erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1dfde-123">The maximum number of delivery reminders that can be created for an order.</span></span><br /><br /> <span data-ttu-id="1dfde-124">**HINWEIS:** Dies ist die maximale Anzahl über alle Mahnstufen hinweg für diese Anmahnungsmethode.</span><span class="sxs-lookup"><span data-stu-id="1dfde-124">**NOTE:** This is the maximum number across all reminder levels for this reminder term.</span></span> <span data-ttu-id="1dfde-125">Wenn Sie beispielsweise drei Stufen eingerichtet haben, und Sie **Max. Anzahl Lieferbenachrichtigungen** auf 5 festlegen, wird die erste Mahnung mit Stufe 1, die zweite mit Stufe 2 und die letzten drei mit Stufe 3 erstellt.</span><span class="sxs-lookup"><span data-stu-id="1dfde-125">For example, if you have set up three levels, and you set **Max. No. of Delivery Reminders** to 5, the first reminder is created at level 1, the second at level 2, and the last three at level 3.</span></span>|  

4.  <span data-ttu-id="1dfde-126">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="1dfde-126">Choose the **OK** button.</span></span>  

## <a name="to-add-delivery-reminder-levels-to-a-delivery-reminder-term"></a><span data-ttu-id="1dfde-127">So richten Sie Lieferanmahnungsstufen für Lieferanmahnungsmethoden ein</span><span class="sxs-lookup"><span data-stu-id="1dfde-127">To add delivery reminder levels to a delivery reminder term</span></span>  

1.  <span data-ttu-id="1dfde-128">Klicken Sie auf der Seite **Lieferbenachrichtigungsbestimmungen** in die Zeile mit der Methode, für die Sie Stufen anlegen möchten, und wählen Sie dann die Aktion **Stufen**.</span><span class="sxs-lookup"><span data-stu-id="1dfde-128">On the **Delivery Reminder Terms** page, select the delivery reminder term for which you want to set up levels, and then choose the **Levels** action.</span></span>  
2.  <span data-ttu-id="1dfde-129">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="1dfde-129">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="1dfde-130">Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="1dfde-130">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="1dfde-131">Feld</span><span class="sxs-lookup"><span data-stu-id="1dfde-131">Field</span></span>|<span data-ttu-id="1dfde-132">Description</span><span class="sxs-lookup"><span data-stu-id="1dfde-132">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="1dfde-133">**Nr.**</span><span class="sxs-lookup"><span data-stu-id="1dfde-133">**No.**</span></span>|<span data-ttu-id="1dfde-134">Lieferbenachrichtigungsstufenzahl.</span><span class="sxs-lookup"><span data-stu-id="1dfde-134">The delivery reminder level number.</span></span> <span data-ttu-id="1dfde-135">Dieses Feld wird automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="1dfde-135">This field is filled in automatically.</span></span>|  
    |<span data-ttu-id="1dfde-136">**Berechnung Fälligkeitsdatum**</span><span class="sxs-lookup"><span data-stu-id="1dfde-136">**Due Date Calculation**</span></span>|<span data-ttu-id="1dfde-137">Die Formel für die Berechnung des Fälligkeitsdatums für die Lieferbenachrichtigung</span><span class="sxs-lookup"><span data-stu-id="1dfde-137">The formula for the due date calculation for the delivery reminder.</span></span> <span data-ttu-id="1dfde-138">Sie können eine Kombination von Nummern zwischen 0 und 9999 sowie Datumscodes eingeben (D für Tag, TW für Wochentag, W für Woche, M für Monat, Q für Quartal oder J für Jahr).</span><span class="sxs-lookup"><span data-stu-id="1dfde-138">You can enter a combination of numbers from 0 to 9999, and date codes (D for day, WD for weekday, W for week, M for month, Q for quarter, or Y for year).</span></span> <span data-ttu-id="1dfde-139">Die Formel für die Berechnung des Datencodes für das Fälligkeitsdatum für die Lieferbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="1dfde-139">The date codes denote the calculation for the delivery reminder due date.</span></span> <span data-ttu-id="1dfde-140">Die Datumsberechnungsformel für das Fälligkeitsdatum kann maximal 20 Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="1dfde-140">You can enter a maximum of 20 characters for the due date calculation formula.</span></span>|  

4.  <span data-ttu-id="1dfde-141">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="1dfde-141">Choose the **OK** button.</span></span>  

<span data-ttu-id="1dfde-142">Für jede Lieferbenachrichtigungsstufe kann eine Textnachricht definiert werden, der in die Lieferbenachrichtigung aufgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="1dfde-142">For each delivery reminder level, you can define text messages that are added to the delivery reminder.</span></span> <span data-ttu-id="1dfde-143">Sie können Vortext definieren, der vor der Beschreibung der überfälligen Bestellung hinzugefügt wird, und Nachtext, der nach der Beschreibung der überfälligen Bestellung hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="1dfde-143">You can define beginning text that is added before the description of the overdue purchase order, and ending text that is added after the description of the overdue purchase order.</span></span>  

<span data-ttu-id="1dfde-144">Nachfolgend wird beschrieben, wie Vortextnachrichten eingerichtet werde. Aber dieselben Schritte gelten auch für das Einrichten von Nachtextnachrichten.</span><span class="sxs-lookup"><span data-stu-id="1dfde-144">The following procedure describes how to set up beginning text messages, but the same steps apply for setting up ending text messages.</span></span>  

## <a name="to-set-up-delivery-reminder-text-messages"></a><span data-ttu-id="1dfde-145">Lieferbenachrichtigungstextnachrichten einrichten</span><span class="sxs-lookup"><span data-stu-id="1dfde-145">To set up delivery reminder text messages</span></span>  

1.  <span data-ttu-id="1dfde-146">Auf der Seite **Lieferbenachrichtigungsstufen** wählen Sie eine Ebene, und wählen die Aktion **Vortext** aus.</span><span class="sxs-lookup"><span data-stu-id="1dfde-146">On the **Delivery Reminder Levels** page, select a level, and then choose the **Beginning Text** action.</span></span>  
2.  <span data-ttu-id="1dfde-147">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="1dfde-147">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="1dfde-148">Geben Sie im Feld **Beschreibung** die Vortextnachricht für die Lieferbenachrichtigung ein.</span><span class="sxs-lookup"><span data-stu-id="1dfde-148">In the **Description** field, enter the beginning text message for the delivery reminder.</span></span>  
4.  <span data-ttu-id="1dfde-149">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="1dfde-149">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1dfde-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1dfde-150">See Also</span></span>  
 <span data-ttu-id="1dfde-151">[Lieferbenachrichtigungen](delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="1dfde-151">[Delivery Reminders](delivery-reminders.md) </span></span>  
 <span data-ttu-id="1dfde-152">[Gewusst wie: Einrichten von Lieferbenachrichtigungen](how-to-set-up-delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="1dfde-152">[Set Up Delivery Reminders](how-to-set-up-delivery-reminders.md) </span></span>  
 <span data-ttu-id="1dfde-153">[So werden Lieferbenachrichtigungscodes zu Kreditoren zugewiesen](how-to-assign-delivery-reminder-codes-to-vendors.md) </span><span class="sxs-lookup"><span data-stu-id="1dfde-153">[Assign Delivery Reminder Codes to Vendors](how-to-assign-delivery-reminder-codes-to-vendors.md) </span></span>  
 <span data-ttu-id="1dfde-154">[So erstellen Sie Lieferanmahnungen manuell](how-to-create-delivery-reminders-manually.md) </span><span class="sxs-lookup"><span data-stu-id="1dfde-154">[Create Delivery Reminders Manually](how-to-create-delivery-reminders-manually.md) </span></span>  
 [<span data-ttu-id="1dfde-155">Lieferbenachrichtigung registrieren</span><span class="sxs-lookup"><span data-stu-id="1dfde-155">Issue Delivery Reminders</span></span>](how-to-issue-delivery-reminders.md)

