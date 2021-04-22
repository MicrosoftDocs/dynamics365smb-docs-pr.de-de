---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7cab5533c038dda6082a0455bf480779f143854e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777573"
---
<span data-ttu-id="6d322-101">Nachdem Sie Lieferbenachrichtigungen erstellt haben, müssen Sie sie registrieren und ausdrucken, sodass Sie Mahnungen an Kreditoren verschicken können.</span><span class="sxs-lookup"><span data-stu-id="6d322-101">After you have created delivery reminders, you must issue and print them so that you can send reminders to vendors.</span></span> <span data-ttu-id="6d322-102">Vor dem Ausstellen von Lieferanmahnnungen können Sie einen Testbericht drucken.</span><span class="sxs-lookup"><span data-stu-id="6d322-102">Before you issue the delivery reminders, you can print a test report.</span></span>  

<span data-ttu-id="6d322-103">Beim Registrieren der Lieferantenbenachrichtigungen erzeugt die Anwendung Lieferantenbenachrichtigungsposten.</span><span class="sxs-lookup"><span data-stu-id="6d322-103">When you issue the delivery reminders, delivery reminder ledger entries are created.</span></span> <span data-ttu-id="6d322-104">Die erstellten Posten können Sie dann auf der Seite **Registrierten Lieferbenachrichtigungskopfes** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="6d322-104">You can view the created ledger entries on the **Deliv. Reminder Ledger Entries** page.</span></span>  

## <a name="to-issue-delivery-reminders"></a><span data-ttu-id="6d322-105">So registrieren Sie Lieferbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="6d322-105">To issue delivery reminders</span></span>  

1. <span data-ttu-id="6d322-106">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“](../../../media/ui-search/search_small.png "Tell me-Funktion") öffnet, geben Sie **Lieferbenachrichtigung** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="6d322-106">Choose the ![Lightbulb that opens the Tell Me feature](../../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delivery Reminder**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6d322-107">Auf der Seite **Lieferbenachrichtigungen** wählen Sie die Lieferbenachrichtigungen aus, die Sie registrieren möchten, und wählen die **Bearbeiten** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="6d322-107">On the **Delivery Reminder** page, select the delivery reminder that you want to issue, and then choose the **Edit** action.</span></span>  
3. <span data-ttu-id="6d322-108">Wählen Sie die Aktion **Ausgeben** aus.</span><span class="sxs-lookup"><span data-stu-id="6d322-108">Choose the **Issue** action.</span></span>  
4. <span data-ttu-id="6d322-109">Füllen Sie die Felder auf der Seite **Lieferanmahnung registrieren** gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="6d322-109">On the **Issue Delivery Reminder** page, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="6d322-110">Feld</span><span class="sxs-lookup"><span data-stu-id="6d322-110">Field</span></span>|<span data-ttu-id="6d322-111">Description</span><span class="sxs-lookup"><span data-stu-id="6d322-111">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="6d322-112">**Drucken**</span><span class="sxs-lookup"><span data-stu-id="6d322-112">**Print**</span></span>|<span data-ttu-id="6d322-113">Wählen Sie diese Option aus, um die Lieferbenachrichtigungen zu drucken, wenn sie registriert werden.</span><span class="sxs-lookup"><span data-stu-id="6d322-113">Select to print the delivery reminders when they are issued.</span></span>|  
    |<span data-ttu-id="6d322-114">**Buchungsdatum ersetzen**</span><span class="sxs-lookup"><span data-stu-id="6d322-114">**Replace Posting Date**</span></span>|<span data-ttu-id="6d322-115">Wählen Sie diese Option aus, um das vorhandene Buchungsdatum für die Lieferbenachrichtigungen zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="6d322-115">Select to replace the existing posting date for the delivery reminder.</span></span>|  
    |<span data-ttu-id="6d322-116">**Buchungsdatum**</span><span class="sxs-lookup"><span data-stu-id="6d322-116">**Posting Date**</span></span>|<span data-ttu-id="6d322-117">Gibt das Buchungsdatum der Lieferbenachrichtigung an.</span><span class="sxs-lookup"><span data-stu-id="6d322-117">The posting date for the delivery reminder.</span></span><br /><br /> <span data-ttu-id="6d322-118">Dieses Buchungsdatum wird für alle Lieferbenachrichtigungen verwendet, wenn Sie das Kontrollkästchen **Buchungsdatum ersetzen** aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="6d322-118">This posting date is used for all delivery reminders if you have selected the **Replace Posting Date** check box.</span></span> <span data-ttu-id="6d322-119">Wenn das Kontrollkästchen **Buchungsdatum ersetzen** deaktiviert ist, wird dieses Datum nur für diejenigen Lieferbenachrichtigungen verwendet, für die kein Buchungsdatum verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6d322-119">If the **Replace Posting Date** check box is cleared, this date will be used for only those delivery reminders for which a posting date is not available.</span></span>|  

5. <span data-ttu-id="6d322-120">Optional wählen Sie im Inforegister **Lieferbenachrichtigungen Kopfzeile** die entsprechenden Filter aus.</span><span class="sxs-lookup"><span data-stu-id="6d322-120">Optionally, on the **Delivery Reminder Header** FastTab, select the appropriate filters.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="6d322-121">Sie können Filter entfernen und allen Lieferbenachrichtigungen gleichzeitig registrieren.</span><span class="sxs-lookup"><span data-stu-id="6d322-121">You can remove filters and issue all delivery reminders at the same time.</span></span>  

6. <span data-ttu-id="6d322-122">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="6d322-122">Choose the **OK** button.</span></span>  

<span data-ttu-id="6d322-123">Sie können das Fenster registrierte Mahnungen anzeigen auf der Seite **Registrierte Lieferbenachrichtigungen**.</span><span class="sxs-lookup"><span data-stu-id="6d322-123">You can view the issued reminders on the **Issued Delivery Reminder** page.</span></span> <span data-ttu-id="6d322-124">Optional können Sie jetzt eine Lieferbenachrichtigung drucken.</span><span class="sxs-lookup"><span data-stu-id="6d322-124">Optionally, you can now print a delivery reminder.</span></span>  

## <a name="to-view-delivery-reminder-ledger-entries"></a><span data-ttu-id="6d322-125">Um sich detaillierte Lieferbenachrichtigungen anzeigen zu lassen:</span><span class="sxs-lookup"><span data-stu-id="6d322-125">To view delivery reminder ledger entries</span></span>  

1. <span data-ttu-id="6d322-126">Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](../../../media/ui-search/search_small.png "Tell me-Funktion"), geben Sie **Einkaufsaufträge** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="6d322-126">Choose the ![Lightbulb that opens the Tell Me feature](../../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6d322-127">Wählen Sie die Bestellung, für die Sie den Mahnungsstatus anzeigen möchten, und wählen die Aktion **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="6d322-127">Select the purchase order for which you want to view the reminder status, and then choose the **Edit** action.</span></span>  
3. <span data-ttu-id="6d322-128">Wählen Sie die Aktion **Lieferbenachrichtigungs-Einträge** aus.</span><span class="sxs-lookup"><span data-stu-id="6d322-128">Choose the **Deliv. Reminder Ledger Entries** action.</span></span>  

<span data-ttu-id="6d322-129">Auf der Seite **Lieferanmahnungsposten** können Sie sich die Lieferanmahnungsposten der ausgewählten Bestellung anzeigen lassen.</span><span class="sxs-lookup"><span data-stu-id="6d322-129">On the **Deliv. Reminder Ledger Entries** page, you can view the delivery reminder ledger entries for the selected purchase order.</span></span>  
