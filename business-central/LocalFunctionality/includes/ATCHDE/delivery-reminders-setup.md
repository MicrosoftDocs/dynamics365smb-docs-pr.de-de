---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 34d9ddd0c3afc97beb19c6c4c9441770656ef6e9
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771506"
---
<span data-ttu-id="a1e37-101">In [!INCLUDE[prod_short](../../../includes/prod_short.md)] können Sie Lieferbenachrichtigungen nutzen, um Verkäufer über verspätete Lieferungen zu mahnen.</span><span class="sxs-lookup"><span data-stu-id="a1e37-101">In [!INCLUDE[prod_short](../../../includes/prod_short.md)], you can use purchase delivery reminders to remind vendors about overdue deliveries.</span></span> <span data-ttu-id="a1e37-102">Um Lieferanmahnungen für Kreditoren zu erstellen, müssen Sie die Stammdaten für die Erstellung von Lieferanmahnungen sowie die Nummernserien für die Lieferanmahnungen auf der Seite Fenster **Kreditoren & Einkauf einrichten** einrichten.</span><span class="sxs-lookup"><span data-stu-id="a1e37-102">To create delivery reminders for vendors, you must set up base data for delivery reminder creation and number series for the delivery reminders on the **Purchases & Payables Setup** page.</span></span>  

## <a name="to-set-up-delivery-reminders"></a><span data-ttu-id="a1e37-103">Gewusst wie: Einrichten von Lieferbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="a1e37-103">To set up delivery reminders</span></span>  

1. <span data-ttu-id="a1e37-104">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](../../../media/ui-search/search_small.png "Tell me-Funktion"), geben Sie **Einrichten von Einkäufen und Verbindlichkeiten** ein, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="a1e37-104">Choose the ![Lightbulb that opens the Tell Me feature](../../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="a1e37-105">Legen Sie im Feld **Standard ENTF. Abbau, AfA** eine der in der folgenden Tabelle beschriebenen Optionen fest.</span><span class="sxs-lookup"><span data-stu-id="a1e37-105">In the **Default Del. Rem. Date Field** field, specify one of the options described in the following table.</span></span>  

    |<span data-ttu-id="a1e37-106">Option</span><span class="sxs-lookup"><span data-stu-id="a1e37-106">Option</span></span>|<span data-ttu-id="a1e37-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1e37-107">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="a1e37-108">**Gewünschtes Wareneingangsdatum**</span><span class="sxs-lookup"><span data-stu-id="a1e37-108">**Requested Receipt Date**</span></span>|<span data-ttu-id="a1e37-109">Legt fest, dass der Datumswert im Feld **Gewünschtes Wareneingangsdatum** in der Bestellzeile als Standarddatum für die Erstellung von Lieferanmahnungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a1e37-109">Specifies that the date value in the **Requested Receipt Date** field on the purchase order line will be used as the default date for creating delivery reminders.</span></span>|  
    |<span data-ttu-id="a1e37-110">**Zugesagtes Wareneingangsdatum**</span><span class="sxs-lookup"><span data-stu-id="a1e37-110">**Promised Receipt Date**</span></span>|<span data-ttu-id="a1e37-111">Legt fest, dass der Datumswert im Feld **Zugesagtes Wareneingangsdatum** in der Bestellzeile als Standarddatum für die Erstellung von Lieferanmahnungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a1e37-111">Specifies that the date value in the **Promised Receipt Date** field on the purchase order line will be used as the default date for creating delivery reminders.</span></span>|  
    |<span data-ttu-id="a1e37-112">**Erwartetes Wareneingangsdatum**</span><span class="sxs-lookup"><span data-stu-id="a1e37-112">**Expected Receipt Date**</span></span>|<span data-ttu-id="a1e37-113">Legt fest, dass der Datumswert im Feld **Erwartetes Wareneingangsdatum** in der Bestellzeile als Standarddatum für die Erstellung von Lieferanmahnungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a1e37-113">Specifies that the date value in the **Expected Receipt Date** field on the purchase order line will be used as the default date for creating delivery reminders.</span></span>|  

3. <span data-ttu-id="a1e37-114">Füllen Sie zusätzliche Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="a1e37-114">Fill in additional fields as described in the following table.</span></span>  

    |<span data-ttu-id="a1e37-115">Feld</span><span class="sxs-lookup"><span data-stu-id="a1e37-115">Field</span></span>|<span data-ttu-id="a1e37-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1e37-116">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="a1e37-117">**Lieferbenachrichtigungsnummern**</span><span class="sxs-lookup"><span data-stu-id="a1e37-117">**Delivery Reminder Nos.**</span></span>|<span data-ttu-id="a1e37-118">Der Nummernseriencode für Lieferanmahnungen.</span><span class="sxs-lookup"><span data-stu-id="a1e37-118">The number series code for delivery reminders.</span></span>|  
    |<span data-ttu-id="a1e37-119">**Reg. Lieferbenachrichtigungsnummern**</span><span class="sxs-lookup"><span data-stu-id="a1e37-119">**Issued Delivery Reminder Nos.**</span></span>|<span data-ttu-id="a1e37-120">Der Nummernseriencode für ausgegebene Lieferanmahnungen.</span><span class="sxs-lookup"><span data-stu-id="a1e37-120">The number series code for issued delivery reminders.</span></span>|  

4. <span data-ttu-id="a1e37-121">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="a1e37-121">Choose the **OK** button.</span></span>  
