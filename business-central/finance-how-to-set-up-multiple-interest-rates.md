---
title: Dient zum Einrichten mehrerer Zinssätze.
description: Sie können Zinsrechnungen mit mehreren Zinssätzen für eine bestimmte Periode berechnen. Die Zinsberechnung ist für alle finanziellen Belastungen, nur mit Veränderung des Zinssatzes für eine bestimmte Periode ähnlich.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 3311747fb6bf6482b708948c3a99c9baf91557f8
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239674"
---
# <a name="set-up-multiple-interest-rates"></a><span data-ttu-id="e763f-104">Dient zum Einrichten mehrerer Zinssätze.</span><span class="sxs-lookup"><span data-stu-id="e763f-104">Set Up Multiple Interest Rates</span></span>
<span data-ttu-id="e763f-105">Mehrere Zinssätze werden für verschiedene Perioden für gestundete Zahlungen in den Geschäftstransaktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="e763f-105">Multiple interest rates are used for different periods for delayed payments in trade transactions.</span></span> <span data-ttu-id="e763f-106">Beispielsweise zeigt eine Regierung den maximalen Zinsen, der für einen Verbraucher erhoben wird.</span><span class="sxs-lookup"><span data-stu-id="e763f-106">For example, a government specifies the maximum interest to be levied for a consumer.</span></span> <span data-ttu-id="e763f-107">Dieser Zinssatz kann zweimal jährlich geändert werden am 1. Januar und 1. Juli.</span><span class="sxs-lookup"><span data-stu-id="e763f-107">This interest rate can be changed twice a year on 01 January and 01 July.</span></span> <span data-ttu-id="e763f-108">Der Zinssatz zwischen Unternehmen (B2B) wird von beiden Parteien vereinbart und dort ist keine Begrenzung zu dieser Debitorengruppe.</span><span class="sxs-lookup"><span data-stu-id="e763f-108">The interest rate between businesses (B2B) is agreed by the parties and there is no limit to that customer group.</span></span> <span data-ttu-id="e763f-109">Der angekündigte Kurs ist normalerweise vier Prozent mehr als die normalen Bankzinsen.</span><span class="sxs-lookup"><span data-stu-id="e763f-109">The announced rate is usually four percent more than the normal bank interest.</span></span>

<span data-ttu-id="e763f-110">Wenn Sie Zinskonditionen und Mahnmethoden für verspätete Zahlungen einrichten, können Sie mehrere Zinssätzen angeben, damit die Strafgebühr aus verschiedenen Zinssätzen in verschiedenen Perioden berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="e763f-110">When you create finance charge terms and reminder terms, for delayed payment penalty, you can specify multiple interest rates so that the penalty fee is calculated from different interest rates in different periods.</span></span> <span data-ttu-id="e763f-111">Weitere Informationen finden Sie unter [Offene Salden eintreiben](receivables-collect-outstanding-balances.md)</span><span class="sxs-lookup"><span data-stu-id="e763f-111">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>

## <a name="to-set-up-multiple-interest-rates"></a><span data-ttu-id="e763f-112">Einrichten mehrerer Zinssätze.</span><span class="sxs-lookup"><span data-stu-id="e763f-112">To set up multiple interest rates</span></span>  
1.  <span data-ttu-id="e763f-113">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Finanzbelastungs-Bestimmungen** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="e763f-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Finance Charge Terms**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e763f-114">Auf der Seite **Zinskonditionen** wählen Sie den gewünschten Finanzausdruck, und wählen die Aktion **Zinssätze**.</span><span class="sxs-lookup"><span data-stu-id="e763f-114">On the **Finance Charge Terms** page, select the required finance term, and then choose the **Interest Rates** action.</span></span>  
3.  <span data-ttu-id="e763f-115">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="e763f-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  <span data-ttu-id="e763f-116">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="e763f-116">Choose the **OK** button.</span></span>  
5.  <span data-ttu-id="e763f-117">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Erinnerungsbestimmungen** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="e763f-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Reminder Terms**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="e763f-118">Auf der Seite **Mahnbestimmungen** wählen Sie die gewünschte Mahnbestimmung und wählen die Aktion **Stufen** aus.</span><span class="sxs-lookup"><span data-stu-id="e763f-118">On the **Reminder Terms** page, select the required reminder term, and then choose the **Levels** action.</span></span>  
7.  <span data-ttu-id="e763f-119">Auf der Seite **Mahnstufen** wählen Sie das Feld **Zins berechnen** aus.</span><span class="sxs-lookup"><span data-stu-id="e763f-119">On the **Reminder Levels** page, select the **Calculate Interest** field.</span></span>  

<span data-ttu-id="e763f-120">Wenn Sie eine Zinsrechnung registrieren, wird deren Registrierung die Zinsrechnungen mit mehreren Zinssätzen während eines bestimmten Zeitraums anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e763f-120">When you issue a finance charge memo, the memo shows the finance charges with multiple interest rates for a specific time period.</span></span> <span data-ttu-id="e763f-121">Die Mahnung enthält außerdem die Kontaktdetails des Debitors, des Unternehmens, das die Mahnung ausgibt, den Zusatzbetrag und den Gesamtbetrag.</span><span class="sxs-lookup"><span data-stu-id="e763f-121">The memo also contains the contact details of the customer, the company issuing the memo, the additional amount, and the total amount.</span></span> <span data-ttu-id="e763f-122">Der Eröffnungsposten der Zinsrechnung wird fett angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e763f-122">The opening entry on the memo is displayed in bold.</span></span> <span data-ttu-id="e763f-123">Die Zinsrechnungen werden mit verschiedenen Zinssätzen für eine bestimmte Periode berechnet und werden nach dem Eröffnungsposten der Mahnung gedruckt.</span><span class="sxs-lookup"><span data-stu-id="e763f-123">The finance charges are calculated with multiple interest rates for a specific time period and are printed after the opening entry of the memo.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e763f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e763f-124">See Also</span></span>  
[<span data-ttu-id="e763f-125">Einziehen von Restbeträgen</span><span class="sxs-lookup"><span data-stu-id="e763f-125">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="e763f-126">Finanzen einrichten</span><span class="sxs-lookup"><span data-stu-id="e763f-126">Setting Up Finance</span></span>](finance-setup-finance.md)
