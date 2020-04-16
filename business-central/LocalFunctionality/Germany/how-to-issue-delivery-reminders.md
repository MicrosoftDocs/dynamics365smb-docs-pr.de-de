---
title: 'Gewusst wie: Lieferbenachrichtigungen ausstellen'
description: Nachdem Sie Lieferbenachrichtigungen erstellt haben, müssen Sie sie registrieren und ausdrucken, sodass Sie Mahnungen an Kreditoren verschicken können. Vor dem Ausstellen von Lieferbenachrichtigungen können Sie einen Testbericht drucken.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 2ebbc76f17c4a42cfc845d2d2b2a8e0488a06d6c
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181164"
---
# <a name="issue-delivery-reminders"></a><span data-ttu-id="a6c9a-104">Lieferbenachrichtigung registrieren</span><span class="sxs-lookup"><span data-stu-id="a6c9a-104">Issue Delivery Reminders</span></span>
<span data-ttu-id="a6c9a-105">Nachdem Sie Lieferbenachrichtigungen erstellt haben, müssen Sie sie registrieren und ausdrucken, sodass Sie Mahnungen an Kreditoren verschicken können.</span><span class="sxs-lookup"><span data-stu-id="a6c9a-105">After you have created delivery reminders, you must issue and print them so that you can send reminders to vendors.</span></span> <span data-ttu-id="a6c9a-106">Vor dem Ausstellen von Lieferbenachrichtigungen können Sie einen Testbericht drucken.</span><span class="sxs-lookup"><span data-stu-id="a6c9a-106">Before you issue the delivery reminders, you can print a test report.</span></span> <span data-ttu-id="a6c9a-107">Weitere Informationen finden Sie unter [Vorgehensweise: Drucken von Testberichten für Lieferbenachrichtigungen](how-to-print-test-reports-for-delivery-reminders.md).</span><span class="sxs-lookup"><span data-stu-id="a6c9a-107">For more information, see [Print Test Reports for Delivery Reminders](how-to-print-test-reports-for-delivery-reminders.md).</span></span>  

<span data-ttu-id="a6c9a-108">Beim Registrieren der Lieferantenbenachrichtigungen erzeugt die Anwendung Lieferantenbenachrichtigungsposten.</span><span class="sxs-lookup"><span data-stu-id="a6c9a-108">When you issue the delivery reminders, delivery reminder ledger entries are created.</span></span> <span data-ttu-id="a6c9a-109">Die erstellten Posten können Sie dann auf der Seite **Registrierten Lieferbenachrichtigungskopfes** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a6c9a-109">You can view the created ledger entries on the **Deliv. Reminder Ledger Entries** page.</span></span>  

## <a name="to-issue-delivery-reminders"></a><span data-ttu-id="a6c9a-110">So registrieren Sie Lieferbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="a6c9a-110">To issue delivery reminders</span></span>  

1.  <span data-ttu-id="a6c9a-111">Wählen Sie das Symbol ![Suche nach Seite oder Bericht](../../media/ui-search/search_small.png "Symbol „Suche nach Seite oder Bericht“") aus, geben Sie **Lieferanmahnung** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="a6c9a-111">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delivery Reminder**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a6c9a-112">Auf der Seite **Lieferbenachrichtigungen** wählen Sie die Lieferbenachrichtigungen aus, die Sie registrieren möchten, und wählen die **Bearbeiten** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="a6c9a-112">On the **Delivery Reminder** page, select the delivery reminder that you want to issue, and then choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="a6c9a-113">Wählen Sie die Aktion **Ausgeben** aus.</span><span class="sxs-lookup"><span data-stu-id="a6c9a-113">Choose the **Issue** action.</span></span>  
4.  <span data-ttu-id="a6c9a-114">Füllen Sie auf der Seite **Lieferbenachrichtigung** im Inforegister **Option** die erforderlichen Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="a6c9a-114">On the **Issue Delivery Reminder** page, on the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="a6c9a-115">Feld</span><span class="sxs-lookup"><span data-stu-id="a6c9a-115">Field</span></span>|<span data-ttu-id="a6c9a-116">Description</span><span class="sxs-lookup"><span data-stu-id="a6c9a-116">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="a6c9a-117">**Drucken**</span><span class="sxs-lookup"><span data-stu-id="a6c9a-117">**Print**</span></span>|<span data-ttu-id="a6c9a-118">Wählen Sie diese Option aus, um die Lieferbenachrichtigungen zu drucken, wenn sie registriert werden.</span><span class="sxs-lookup"><span data-stu-id="a6c9a-118">Select to print the delivery reminders when they are issued.</span></span>|  
    |<span data-ttu-id="a6c9a-119">**Buchungsdatum ersetzen**</span><span class="sxs-lookup"><span data-stu-id="a6c9a-119">**Replace Posting Date**</span></span>|<span data-ttu-id="a6c9a-120">Wählen Sie diese Option aus, um das vorhandene Buchungsdatum für die Lieferbenachrichtigungen zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="a6c9a-120">Select to replace the existing posting date for the delivery reminder.</span></span>|  
    |<span data-ttu-id="a6c9a-121">**Buchungsdatum**</span><span class="sxs-lookup"><span data-stu-id="a6c9a-121">**Posting Date**</span></span>|<span data-ttu-id="a6c9a-122">Gibt das Buchungsdatum der Lieferbenachrichtigung an.</span><span class="sxs-lookup"><span data-stu-id="a6c9a-122">The posting date for the delivery reminder.</span></span><br /><br /> <span data-ttu-id="a6c9a-123">Dieses Buchungsdatum wird für alle Lieferbenachrichtigungen verwendet, wenn Sie das Kontrollkästchen **Buchungsdatum ersetzen** aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="a6c9a-123">This posting date is used for all delivery reminders if you have selected the **Replace Posting Date** check box.</span></span> <span data-ttu-id="a6c9a-124">Wenn das Kontrollkästchen **Buchungsdatum ersetzen** deaktiviert ist, wird dieses Datum nur für diejenigen Lieferbenachrichtigungen verwendet, für die kein Buchungsdatum verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a6c9a-124">If the **Replace Posting Date** check box is cleared, this date will be used for only those delivery reminders for which a posting date is not available.</span></span>|  

5.  <span data-ttu-id="a6c9a-125">Optional wählen Sie im Inforegister **Lieferbenachrichtigungen Kopfzeile** die entsprechenden Filter aus.</span><span class="sxs-lookup"><span data-stu-id="a6c9a-125">Optionally, on the **Delivery Reminder Header** FastTab, select the appropriate filters.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="a6c9a-126">Sie können Filter entfernen und allen Lieferbenachrichtigungen gleichzeitig registrieren.</span><span class="sxs-lookup"><span data-stu-id="a6c9a-126">You can remove filters and issue all delivery reminders at the same time.</span></span>  

6.  <span data-ttu-id="a6c9a-127">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="a6c9a-127">Choose the **OK** button.</span></span>  

<span data-ttu-id="a6c9a-128">Sie können das Fenster registrierte Mahnungen anzeigen auf der Seite **Registrierte Lieferbenachrichtigungen**.</span><span class="sxs-lookup"><span data-stu-id="a6c9a-128">You can view the issued reminders on the **Issued Delivery Reminder** page.</span></span> <span data-ttu-id="a6c9a-129">Optional können Sie jetzt eine Lieferbenachrichtigung drucken.</span><span class="sxs-lookup"><span data-stu-id="a6c9a-129">Optionally, you can now print a delivery reminder.</span></span>  

## <a name="to-view-delivery-reminder-ledger-entries"></a><span data-ttu-id="a6c9a-130">Um sich detaillierte Lieferbenachrichtigungen anzeigen zu lassen:</span><span class="sxs-lookup"><span data-stu-id="a6c9a-130">To view delivery reminder ledger entries</span></span>  

1.  <span data-ttu-id="a6c9a-131">Wählen Sie das Symbol ![Suche nach Seite oder Bericht](../../media/ui-search/search_small.png "Symbol „Suche nach Seite oder Bericht“"), geben Sie **Einkaufsbestellungen** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="a6c9a-131">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a6c9a-132">Wählen Sie die Bestellung, für die Sie den Mahnungsstatus anzeigen möchten, und wählen die Aktion **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="a6c9a-132">Select the purchase order for which you want to view the reminder status, and then choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="a6c9a-133">Wählen Sie die Aktion **Lieferbenachrichtigungs-Einträge** aus.</span><span class="sxs-lookup"><span data-stu-id="a6c9a-133">Choose the **Deliv. Reminder Ledger Entries** action.</span></span>  

<span data-ttu-id="a6c9a-134">Auf der Seite registrierter Lieferbenachrichtigungskopf können Sie die Lieferbenachrichtigungsposten der ausgewählten Bestellung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a6c9a-134">In the Deliv. Reminder Ledger Entries page, you can view the delivery reminder ledger entries for the selected purchase order.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a6c9a-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6c9a-135">See Also</span></span>  
 <span data-ttu-id="a6c9a-136">[Lieferbenachrichtigungen](delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="a6c9a-136">[Delivery Reminders](delivery-reminders.md) </span></span>  
 <span data-ttu-id="a6c9a-137">[So erstellen Sie Lieferanmahnungen](how-to-generate-delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="a6c9a-137">[Generate Delivery Reminders](how-to-generate-delivery-reminders.md) </span></span>  
 [<span data-ttu-id="a6c9a-138">So erstellen Sie Lieferanmahnungen manuell</span><span class="sxs-lookup"><span data-stu-id="a6c9a-138">Create Delivery Reminders Manually</span></span>](how-to-create-delivery-reminders-manually.md)
