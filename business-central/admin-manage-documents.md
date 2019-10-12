---
title: Verwalten, löschen oder komprimieren von Belegen | Microsoft Docs
description: Speichern Sie die historischen Daten oder löschen Sie sie.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: e2ef5daf60bd9b2a3b7200001170c2c5e570b674
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304396"
---
# <a name="manage-documents"></a><span data-ttu-id="d1e1d-103">Verwalten von Belegen</span><span class="sxs-lookup"><span data-stu-id="d1e1d-103">Manage Documents</span></span>
<span data-ttu-id="d1e1d-104">Ein Benutzer mit einer zentralen Rolle, z. B. der Anwendungsadministrator, muss sich regelmäßig um die angesammelten historischen Belege kümmern, indem er diese löscht oder komprimiert.</span><span class="sxs-lookup"><span data-stu-id="d1e1d-104">A central role, such as the application administrator, must regularly deal with accumulating historic documents by deleting or compressing them.</span></span>  

## <a name="delete-documents"></a><span data-ttu-id="d1e1d-105">Belege löschen</span><span class="sxs-lookup"><span data-stu-id="d1e1d-105">Delete Documents</span></span>
<span data-ttu-id="d1e1d-106">Es kann gelegentlich erforderlich sein, erledigte Einkaufsbestellungen zu löschen, die noch nicht gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="d1e1d-106">In certain situations, you may need to delete invoiced purchase orders that have not been deleted.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="d1e1d-107">überprüft, ob Sie die gelöschten Bestellungen vollständig fakturiert haben.</span><span class="sxs-lookup"><span data-stu-id="d1e1d-107">checks that you have fully invoiced the deleted purchase orders.</span></span> <span data-ttu-id="d1e1d-108">Sie können keine Bestellungen löschen, die noch nicht vollständig geliefert und fakturiert wurden.</span><span class="sxs-lookup"><span data-stu-id="d1e1d-108">You cannot delete orders that you have not fully invoiced and received.</span></span>  

<span data-ttu-id="d1e1d-109">Reklamationen werden üblicherweise gelöscht, nachdem sie fakturiert wurden.</span><span class="sxs-lookup"><span data-stu-id="d1e1d-109">Return orders are usually deleted after they are invoiced.</span></span> <span data-ttu-id="d1e1d-110">Wenn Sie eine Rechnung buchen, wird sie auf die Seite **Geb. Einkaufsgutschrift** übertragen.</span><span class="sxs-lookup"><span data-stu-id="d1e1d-110">When you post an invoice, it is transferred to the **Posted Purchase Credit Memo** page.</span></span> <span data-ttu-id="d1e1d-111">Ist das Kontrollkästchen **Rücklieferung bei Gutschrift** im Fenster **Kreditoren & Einkauf Einr.** aktiviert, wird sie auch auf die Seite **Gebuchte Rücklieferung** übertragen.</span><span class="sxs-lookup"><span data-stu-id="d1e1d-111">If you selected the **Return Shipment on Credit Memo** check box on the **Purchases & Payable Setup** page, then the invoice is transferred to the **Posted Return Shipment** page.</span></span> <span data-ttu-id="d1e1d-112">Sie können die Belege mithilfe der Stapelverarbeitung **Erledigte Eink.-Rekl. löschen** löschen.</span><span class="sxs-lookup"><span data-stu-id="d1e1d-112">You can delete the documents using the **Delete Invd Purch. Ret. Orders** batch job.</span></span> <span data-ttu-id="d1e1d-113">Vor dem Löschen prüft die Stapelverarbeitung, ob die Einkaufsreklamationen vollständig geliefert und fakturiert wurden.</span><span class="sxs-lookup"><span data-stu-id="d1e1d-113">Before deleting, the batch job checks if the purchase return orders are fully shipped and invoiced.</span></span>  

<span data-ttu-id="d1e1d-114">Rahmenbestellungen werden nicht gelöscht, nachdem Sie alle zugehörigen Bestellungen verarbeitet und fakturiert haben.</span><span class="sxs-lookup"><span data-stu-id="d1e1d-114">Blanket purchase orders are not deleted after you have processed and invoiced all the related purchase orders.</span></span> <span data-ttu-id="d1e1d-115">Sie können erledigte Rahmenbestellungen mit Hilfe der Stapelverarbeitung **Erledigte Rahmenbestellungen löschen** löschen.</span><span class="sxs-lookup"><span data-stu-id="d1e1d-115">You can delete blanket orders with the **Delete Invoiced Blanket Purchase Orders** batch job.</span></span>  

<span data-ttu-id="d1e1d-116">Verrechnete Serviceaufträge werden automatisch gelöscht, nachdem diese vollständig fakturiert wurden.</span><span class="sxs-lookup"><span data-stu-id="d1e1d-116">Invoiced service orders are usually deleted automatically after having been fully invoiced.</span></span> <span data-ttu-id="d1e1d-117">Beim Buchen einer Rechnung wird ein entsprechender Posten auf der Seite **Gebuchte Servicerechnungen** erstellt.</span><span class="sxs-lookup"><span data-stu-id="d1e1d-117">When an invoice is posted, a corresponding entry is created on the **Posted Service Invoices** page.</span></span> <span data-ttu-id="d1e1d-118">Der gebuchte Beleg kann auf der Seite **Gebuchte Servicerechnung** angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d1e1d-118">The posted document can be viewed on the **Posted Service Invoice** page.</span></span>  

<span data-ttu-id="d1e1d-119">Serviceaufträge werden aber nicht automatisch gelöscht, wenn die Gesamtmenge des Auftrags nicht aus dem eigentlichen Serviceauftrag, sondern von der Seite **Servicerechnung** gebucht wurde.</span><span class="sxs-lookup"><span data-stu-id="d1e1d-119">Service orders are not deleted automatically, however, if the total quantity on the order has been posted not from the service order itself, but from the **Service Invoice** page.</span></span> <span data-ttu-id="d1e1d-120">In diesem Fall müssen Sie fakturierte Aufträge, die nicht gelöscht wurden, manuell löschen.</span><span class="sxs-lookup"><span data-stu-id="d1e1d-120">Then you may need to delete invoiced orders that were not deleted.</span></span> <span data-ttu-id="d1e1d-121">Dazu führen Sie die Stapelverarbeitung **Fakturierte Serviceaufträge löschen** aus.</span><span class="sxs-lookup"><span data-stu-id="d1e1d-121">You can do this by running the **Delete Invoiced Service Orders** batch job.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d1e1d-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1e1d-122">See Also</span></span>  
[<span data-ttu-id="d1e1d-123">Verwaltung</span><span class="sxs-lookup"><span data-stu-id="d1e1d-123">Administration</span></span>](admin-setup-and-administration.md)  
