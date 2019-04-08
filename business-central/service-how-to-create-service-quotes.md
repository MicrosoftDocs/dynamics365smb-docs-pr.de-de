---
title: So erstellen Sie Serviceangebote | Microsoft Docs
description: Sie können die Seite **Serviceangebot** verwenden, um Belege zu erstellen, in die Sie Informationen über den Service (Reparatur und Wartung) von Serviceartikeln auf Debitorenanfrage eingeben. Serviceangebote können als Vorentwürfe von Serviceaufträgen betrachtet werden, die dann vom Angebot in einen Auftrag umgewandelt werden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 1486be71b0b848aa48996f4161f8987322a09e32
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "797938"
---
# <a name="create-service-quotes"></a><span data-ttu-id="2b752-104">Serviceangebote erstellen</span><span class="sxs-lookup"><span data-stu-id="2b752-104">Create Service Quotes</span></span>
<span data-ttu-id="2b752-105">Sie können an Serviceangebote als Basis für Serviceaufträge denken.</span><span class="sxs-lookup"><span data-stu-id="2b752-105">You can think of service quotes as the basis for service orders.</span></span> <span data-ttu-id="2b752-106">Tatsächlich sind sie fast identisch.</span><span class="sxs-lookup"><span data-stu-id="2b752-106">In fact, they are almost identical.</span></span> <span data-ttu-id="2b752-107">Sie enthalten sowohl die Serviceartikelbeschreibung, wie der Debitor, die Art des Auftrags, den Artikel, für den Service, Gebührenzählung und benötigte Versandinformationen, und die Informationen über die tatsächliche Dienstarbeit.</span><span class="sxs-lookup"><span data-stu-id="2b752-107">They both contain information such as who the customer is, the type of order, the item that needs service, billing and shipping information, and information about the actual service work.</span></span>
 
<span data-ttu-id="2b752-108">Serviceangebote können als Vorentwürfe von Serviceaufträgen betrachtet werden, die dann vom Angebot in einen Auftrag umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="2b752-108">You can use a service quote as a preliminary draft for a service order, and then convert the quote to a service order.</span></span>  
  
## <a name="to-create-a-service-quote"></a><span data-ttu-id="2b752-109">So erstellen Sie ein Serviceangebot</span><span class="sxs-lookup"><span data-stu-id="2b752-109">To create a service quote</span></span>  
1. <span data-ttu-id="2b752-110">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Serviceangebote** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="2b752-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Quotes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2b752-111">Erstellen Sie ein neues Serviceangebot.</span><span class="sxs-lookup"><span data-stu-id="2b752-111">Create a new service quote.</span></span>  
3. <span data-ttu-id="2b752-112">Geben Sie im Feld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="2b752-112">In the **No.**</span></span> <span data-ttu-id="2b752-113">eine Nummer für das Serviceangebot ein.</span><span class="sxs-lookup"><span data-stu-id="2b752-113">field, enter a number for the service quote.</span></span> <span data-ttu-id="2b752-114">Wenn Sie Nummernserien für Serviceangebote auf der Seite **Service Einrichtung** definiert haben, drücken Sie die Eingabetaste, um die nächste verfügbare Serviceangebotsnummer auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="2b752-114">Alternatively, if you have set up a number series for service quotes on the **Service Mgt. Setup** page, you can press Enter to select the next available service quote number.</span></span>  
4. <span data-ttu-id="2b752-115">Klicken Sie im Feld **Debitorennr.**</span><span class="sxs-lookup"><span data-stu-id="2b752-115">In the **Customer No.**</span></span>  <span data-ttu-id="2b752-116">Feld wählen Sie den relevanten Debitoren aus der Liste.</span><span class="sxs-lookup"><span data-stu-id="2b752-116">field, select the relevant customer from the list.</span></span>  

  > [!Note]  
  >  <span data-ttu-id="2b752-117">Die Debitorenfelder werden automatisch mit Informationen aus der Karte **Debitor** gefüllt.</span><span class="sxs-lookup"><span data-stu-id="2b752-117">The customer fields are filled in automatically with information from the **Customer** card.</span></span> <span data-ttu-id="2b752-118">Wenn keine **Debitor**-Karte für den Debitor vorhanden ist und Sie eine Debitorenvorlage eingerichtet haben, können Sie aus dem Serviceangebot heraus einen Debitor erstellen.</span><span class="sxs-lookup"><span data-stu-id="2b752-118">If a **Customer** card does not exist for the customer, and you have set up a customer template, you can create the customer from the service quote.</span></span> <span data-ttu-id="2b752-119">Füllen Sie die relevanten Felder aus, und wählen Sie dann die Schaltfläche **Debitor erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="2b752-119">Fill in the relevant fields, and then choose the **Create Customer** action.</span></span>  
  
5. <span data-ttu-id="2b752-120">Abhängig von den Einstellungen auf dem Inforegister **Pflichtfelder** auf der Seite **Service Einrichtung** muss das Feld **Serviceauftragsart** auf dem Inforegister **Verkäufercode** ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="2b752-120">Depending on the settings on the **Mandatory Fields** FastTab on the **Service Mgt. Setup** page, you may need to fill in the **Service Order Type** field and the **Salesperson Code** field.</span></span>  
6. <span data-ttu-id="2b752-121">Füllen Sie die Serviceartikelzeilen aus.</span><span class="sxs-lookup"><span data-stu-id="2b752-121">Fill in the service item lines.</span></span>  
7. <span data-ttu-id="2b752-122">Erfassen Sie die geschätzten Kosten in den Servicezeilen.</span><span class="sxs-lookup"><span data-stu-id="2b752-122">Register estimated costs on the service lines.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2b752-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b752-123">See Also</span></span>  
[<span data-ttu-id="2b752-124">Erstellen von Serviceaufträgen</span><span class="sxs-lookup"><span data-stu-id="2b752-124">Create Service Orders</span></span>](service-how-to-create-service-orders.md)  
[<span data-ttu-id="2b752-125">Mit Serviceaufgaben arbeiten</span><span class="sxs-lookup"><span data-stu-id="2b752-125">Work on Service tasks</span></span>](service-how-to-work-on-service-tasks.md)  

 