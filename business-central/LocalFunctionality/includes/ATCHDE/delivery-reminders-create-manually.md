---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 923162f06045d13e37c80d31c27c8771eccf2f04
ms.sourcegitcommit: 428f180604e5afcf94fa0e92a0615f58c88e13cd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/02/2020
ms.locfileid: "3959622"
---
<span data-ttu-id="41db0-101">In [!INCLUDE[d365fin](../../../includes/d365fin_md.md)], können Sie Lieferanmahnungen erstellen, wenn eine Bestellung nicht wie erwartet geliefert wurde.</span><span class="sxs-lookup"><span data-stu-id="41db0-101">In [!INCLUDE[d365fin](../../../includes/d365fin_md.md)], you can create delivery reminders when a purchase has not been delivered as expected.</span></span> <span data-ttu-id="41db0-102">Sie können eine einzelne Lieferbenachrichtigung manuell erstellen oder Sie können Lieferbenachrichtigungen für alle überfälligen Lieferungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="41db0-102">You can create a single delivery reminder manually, or you can generate delivery reminders for all overdue deliveries.</span></span>  

> [!NOTE]
> <span data-ttu-id="41db0-103">Um Lieferanmahnungen zu erstellen, müssen Sie die Lieferanmahnungsbestimmungen, -stufen und -texte eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="41db0-103">To create delivery reminders, you must have set up the delivery reminder terms, levels, and texts.</span></span>

## <a name="to-create-a-delivery-reminder-manually"></a><span data-ttu-id="41db0-104">So erstellen Sie Lieferantenbenachrichtigungen manuell</span><span class="sxs-lookup"><span data-stu-id="41db0-104">To create a delivery reminder manually</span></span>  

1. <span data-ttu-id="41db0-105">Wählen Sie das Symbol ![Glühbirne, das die Tell me Funktion](../../../media/ui-search/search_small.png "Tell me-Funktion") öffnet, geben Sie **Lieferanmahnung** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="41db0-105">Choose the ![The lightbulb icon that opens the Tell Me feature](../../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delivery Reminder**, and then choose the related link.</span></span>  
2. <span data-ttu-id="41db0-106">Wählen Sie die Aktion **Neu**.</span><span class="sxs-lookup"><span data-stu-id="41db0-106">Choose the **New** action.</span></span>  
3. <span data-ttu-id="41db0-107">Füllen Sie die Felder auf der Seite **Lieferanmahnung** gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="41db0-107">On the **Delivery Reminder** page, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="41db0-108">Feld</span><span class="sxs-lookup"><span data-stu-id="41db0-108">Field</span></span>|<span data-ttu-id="41db0-109">Description</span><span class="sxs-lookup"><span data-stu-id="41db0-109">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="41db0-110">**Nr.**</span><span class="sxs-lookup"><span data-stu-id="41db0-110">**No.**</span></span>|<span data-ttu-id="41db0-111">Die eindeutige Kennnummer für die Lieferbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="41db0-111">The unique identification number for the delivery reminder.</span></span>|  
    |<span data-ttu-id="41db0-112">**Kreditorennr**</span><span class="sxs-lookup"><span data-stu-id="41db0-112">**Vendor No.**</span></span>|<span data-ttu-id="41db0-113">Gibt die Nummer des Kreditors an, für den Sie eine Lieferbenachrichtigung buchen möchten.</span><span class="sxs-lookup"><span data-stu-id="41db0-113">The number of the vendor for whom you want to post the delivery reminder.</span></span><br /><br /> <span data-ttu-id="41db0-114">Wenn Sie die Kreditorennummer auswählen, werden **Name**, **Adresse**, **PLZ Code/Ort** und **Kontakt** Felder automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="41db0-114">When you select the vendor number, the **Name**, **Address**, **Post Code/City**, and **Contact** fields are filled in automatically.</span></span>|  
    |<span data-ttu-id="41db0-115">**Buchungsdatum**</span><span class="sxs-lookup"><span data-stu-id="41db0-115">**Posting Date**</span></span>|<span data-ttu-id="41db0-116">Gibt das Buchungsdatum der Lieferbenachrichtigung an.</span><span class="sxs-lookup"><span data-stu-id="41db0-116">The posting date for the delivery reminder.</span></span> <span data-ttu-id="41db0-117">Dieses Datum wird in alle Lieferbenachrichtigung kopiert.</span><span class="sxs-lookup"><span data-stu-id="41db0-117">This date is copied to all of the delivery reminder ledger entries.</span></span>|  
    |<span data-ttu-id="41db0-118">**Belegdatum**</span><span class="sxs-lookup"><span data-stu-id="41db0-118">**Document Date**</span></span>|<span data-ttu-id="41db0-119">Gibt das Dokumentdatum der Lieferbenachrichtigung an.</span><span class="sxs-lookup"><span data-stu-id="41db0-119">The document date for the delivery reminder.</span></span> <span data-ttu-id="41db0-120">Dieses Datum wird auch verwendet, um das Fälligkeitsdatum der Lieferbenachrichtigung zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="41db0-120">This date is also used to calculate the due date for the delivery reminder.</span></span> <span data-ttu-id="41db0-121">Sie können das Buchungsdatum bei Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="41db0-121">You can modify the posting date if required.</span></span>|  
    |<span data-ttu-id="41db0-122">**Mahnstufe**</span><span class="sxs-lookup"><span data-stu-id="41db0-122">**Reminder Level**</span></span>|<span data-ttu-id="41db0-123">Lieferbenachrichtigungsstufe.</span><span class="sxs-lookup"><span data-stu-id="41db0-123">The delivery reminder level.</span></span> <span data-ttu-id="41db0-124">Dieser Wert basiert auf der Anzahl von Lieferbenachrichtigung, die bereits gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="41db0-124">This value is based on the number of delivery reminders that have already been sent.</span></span>|  
    |<span data-ttu-id="41db0-125">**Mahnmethodencode**</span><span class="sxs-lookup"><span data-stu-id="41db0-125">**Reminder Terms Code**</span></span>|<span data-ttu-id="41db0-126">Gibt den Lieferbenachrichtigungscode für den Kreditor an.</span><span class="sxs-lookup"><span data-stu-id="41db0-126">Specify the delivery reminder terms code that is set up for the vendor.</span></span>|  
    |<span data-ttu-id="41db0-127">**Fälligkeitsdatum**</span><span class="sxs-lookup"><span data-stu-id="41db0-127">**Due Date**</span></span>|<span data-ttu-id="41db0-128">Gibt das Fälligkeitsdatum der Lieferbenachrichtigung an.</span><span class="sxs-lookup"><span data-stu-id="41db0-128">The due date for the delivery reminder.</span></span>|  

4. <span data-ttu-id="41db0-129">Wählen Sie die Aktion **Mahnungszeile vorschlagen**.</span><span class="sxs-lookup"><span data-stu-id="41db0-129">Choose the **Suggest Reminder Lines** action.</span></span>  

    <span data-ttu-id="41db0-130">Wenn es überfällige Lieferungen vom angegebenen Kreditor gibt, werden diese der Lieferanmahnung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="41db0-130">If there are overdue deliveries from the specified vendor, these are added to the delivery reminder.</span></span>  

5. <span data-ttu-id="41db0-131">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="41db0-131">Choose the **OK** button.</span></span>  

    <span data-ttu-id="41db0-132">Lieferbenachrichtigung wurde erstellt.</span><span class="sxs-lookup"><span data-stu-id="41db0-132">The delivery reminder is created.</span></span> <span data-ttu-id="41db0-133">So können die Lieferbenachrichtigungen ausgeben und erstellen.</span><span class="sxs-lookup"><span data-stu-id="41db0-133">You can now issue and print the delivery reminder.</span></span>  
