---
title: 'Vorgehensweise: Einrichten von Barkunden | Microsoft Docs'
description: Dieses Thema beschreibt die Schritte, um Kunden einzurichten, der in bar bezahlt.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/11/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 93c28879417b12bc142c84c38c054828b380cc53
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-cash-customers"></a><span data-ttu-id="3ad42-103">Barkunden einrichten</span><span class="sxs-lookup"><span data-stu-id="3ad42-103">Set Up Cash Customers</span></span>
<span data-ttu-id="3ad42-104">Sie können keine Rechnung ohne Debitorennummer erstellen.</span><span class="sxs-lookup"><span data-stu-id="3ad42-104">You cannot create an invoice without a customer number.</span></span> <span data-ttu-id="3ad42-105">Dies trifft auch zu, wenn Sie einen Barverkauf tätigen und kein Debitorenkonto aktualisieren müssen.</span><span class="sxs-lookup"><span data-stu-id="3ad42-105">This is true, even if you make a cash sale and do not have anything to record in a customer account.</span></span>  

## <a name="to-set-up-a-cash-customer"></a><span data-ttu-id="3ad42-106">So richten Sie Bargelddebitoren ein:</span><span class="sxs-lookup"><span data-stu-id="3ad42-106">To set up a cash customer</span></span>  
1.  <span data-ttu-id="3ad42-107">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Kunde** ein und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="3ad42-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customer**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="3ad42-108">Erstellen Sie eine neue Karte **Debitor**.</span><span class="sxs-lookup"><span data-stu-id="3ad42-108">Create a new **Customer** card.</span></span> <span data-ttu-id="3ad42-109">Weitere Informationen finden Sie unter [Neue Kunden registrieren](sales-how-register-new-customers.md).</span><span class="sxs-lookup"><span data-stu-id="3ad42-109">For more information, see [Register New Customers](sales-how-register-new-customers.md).</span></span>
3.  <span data-ttu-id="3ad42-110">Geben Sie im Feld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="3ad42-110">In the **No.**</span></span> <span data-ttu-id="3ad42-111">Geben Sie beispielsweise **Bar** ein.</span><span class="sxs-lookup"><span data-stu-id="3ad42-111">field, enter **Cash**, for example.</span></span>  
4.  <span data-ttu-id="3ad42-112">Geben Sie in dem Feld **Name** z. B. **BARVERKAUF** ein.</span><span class="sxs-lookup"><span data-stu-id="3ad42-112">In the **Name** field, enter **Cash Sale**, for example.</span></span>  
5.  <span data-ttu-id="3ad42-113">Füllen Sie auf dem Inforegister **Fakturierung** die Felder **Debitorenbuchungsgruppe** und **Geschäftsbuchungsgruppe** aus.</span><span class="sxs-lookup"><span data-stu-id="3ad42-113">On the **Invoicing** FastTab, fill in the **Customer Posting Group** and the **Gen. Bus. Posting Group** fields.</span></span>  

 <span data-ttu-id="3ad42-114">Sie haben jetzt einen neuen Debitor und die notwendigen Informationen für die Fakturierung eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="3ad42-114">Now you have set up a customer that contains sufficient information for invoicing.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="3ad42-115">Es kann sein, dass Sie eine Buchungsgruppe gewählt haben, die auch für inländische Kreditverkäufe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3ad42-115">You may have chosen a posting group that is also used for domestic credit sales.</span></span> <span data-ttu-id="3ad42-116">Falls Sie gesonderte Daten für Barverkäufe benötigen, z. B. mit einem Verkaufs- oder Sammelkonto, können Sie zu diesem Zweck eine gesonderte Buchungsgruppe einrichten.</span><span class="sxs-lookup"><span data-stu-id="3ad42-116">If you want to maintain separate data on cash sales, for example, with a special sales or receivables account, you can set up an extra posting group for this purpose.</span></span>  
>   
>  <span data-ttu-id="3ad42-117">Sie müssen in dieser Buchungsgruppe die Nummer für ein Sammelkonto angeben, obwohl der Saldo auf diesem Konto immer 0 sein wird, nachdem Sie die Rechnung gebucht haben.</span><span class="sxs-lookup"><span data-stu-id="3ad42-117">You must enter a number for a receivables account for the posting group, even though the balance in this account will always be 0 after you post an invoice.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3ad42-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ad42-118">See Also</span></span>
[<span data-ttu-id="3ad42-119">Verwalten von Forderungen</span><span class="sxs-lookup"><span data-stu-id="3ad42-119">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="3ad42-120">[Registriert einen neuen Debitor](sales-how-register-new-customers.md)  </span><span class="sxs-lookup"><span data-stu-id="3ad42-120">[Register New Customers](sales-how-register-new-customers.md)  </span></span>  
[<span data-ttu-id="3ad42-121">Finanzen</span><span class="sxs-lookup"><span data-stu-id="3ad42-121">Finance</span></span>](finance.md)  


