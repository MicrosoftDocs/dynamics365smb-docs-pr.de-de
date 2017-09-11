---
title: "Aktualisieren von Währungswechselkursen | Microsoft Docs"
description: "Um mehrere Währungen in Ihrem Unternehmen zu verwenden, können Sie einen Code für jede Währung einrichten und einen externen Wechselkursdienst, wie Yahoo verwenden."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, Yahoo
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: cc60569091b3aa37d17e981f1fae8f46c4a004df
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-update-currency-exchange-rates"></a><span data-ttu-id="08845-103">Vorgehensweise: Aktualisieren von Währungswechselkursen</span><span class="sxs-lookup"><span data-stu-id="08845-103">How to: Update Currency Exchange Rates</span></span>
<span data-ttu-id="08845-104">Sie müssen für jede Währung, die Sie verwenden, einen Währungscode einrichten, wenn Sie in anderen Währungen als Ihrer Mandantenwährung verkaufen oder einkaufen, Forderungen oder Verbindlichkeiten haben oder in unterschiedlichen Währungen buchen.</span><span class="sxs-lookup"><span data-stu-id="08845-104">You must set up a code for each currency you use if you buy or sell in currencies other than your local currency, have receivables or payables in other currencies, or record G/L transactions in different currencies.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="08845-105">Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="08845-105">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="08845-106">Weitere Informationen finden Sie unter [Anpassen Ihrer [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)Experience.</span><span class="sxs-lookup"><span data-stu-id="08845-106">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

<span data-ttu-id="08845-107">Sie können einen externen Service verwenden, um Ihre Währungswechselkurses auf dem neuesten Stand zu halten.</span><span class="sxs-lookup"><span data-stu-id="08845-107">You can use an external service to keep your currency exchange rates up to date.</span></span> <span data-ttu-id="08845-108">Der Service wird vorinstalliert und Yahoo Currency Exchange Rates ist vorbereitet und muss lediglich noch aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="08845-108">The Yahoo Currency Exchange Rates service is preinstalled and ready to enable.</span></span>

## <a name="to-set-up-a-currency-exchange-rate-service"></a><span data-ttu-id="08845-109">So richten Sie einen Währungswechselkurs-Service ein</span><span class="sxs-lookup"><span data-stu-id="08845-109">To set up a currency exchange rate service</span></span>
1. <span data-ttu-id="08845-110">Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") ein und wählen **Währungswechselkurs-Dienste** und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="08845-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Currency Exchange Rate Services**, and then choose the related link.</span></span>
2. <span data-ttu-id="08845-111">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="08845-111">Choose the **New** action.</span></span>
3. <span data-ttu-id="08845-112">Füllen Sie im Fenster **Währungswechselkurs-Service** die Felder nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="08845-112">In the **Currency Exchange Rate Service** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="08845-113">Wählen Sie das Kontrollkästchen **Aktiviert**, um den Service zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="08845-113">Choose the **Enabled** check box to enable the service.</span></span>

## <a name="to-update-currency-exchange-rates-through-a-service"></a><span data-ttu-id="08845-114">Um Währungswechselkurse über einen Service zu aktualisieren</span><span class="sxs-lookup"><span data-stu-id="08845-114">To update currency exchange rates through a service</span></span>
1. <span data-ttu-id="08845-115">Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") ein und wählen **Währungswechselkurs-Dienste** und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="08845-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Currencies**, and then choose the related link.</span></span>
2. <span data-ttu-id="08845-116">Wählen Sie die **Aktualisieren von Wechselkursen** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="08845-116">Choose the **Update Exchange Rates** action.</span></span>

<span data-ttu-id="08845-117">Der Wert im Feld **Wechselkurs** wird im Fenster **Währung** mit dem aktuellen Währungswechselkurs aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="08845-117">The value in the **Exchange Rate** field in the **Currencies** window is updated with the latest currency exchange rate.</span></span>

## <a name="see-also"></a><span data-ttu-id="08845-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08845-118">See Also</span></span>
[<span data-ttu-id="08845-119">Beenden von Jahresabschluss und Perioden</span><span class="sxs-lookup"><span data-stu-id="08845-119">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="08845-120">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="08845-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

