---
title: 'Vorgehensweise: Erstellen benutzerdefinierter Unternehmenskonfigurationspakete | Microsoft Docs'
description: Während Ihr Unternehmen wächst, werden Sie sich wahrscheinlich mit der Zeit auf einen Satz von Mandantentypen festlegen, den Sie auf die meisten Ihrer Debitoren anwenden können. Sie können Ihren Implementierungsprozess rationalisieren, indem Sie diese Arten zu Konfigurationspaketen verarbeiten, die für die Wiederverwendung verfügbar sind.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e6781b01a80acfd3431fc000069dd2c8b96dffc5
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779907"
---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="84c55-104">Vorgehensweise: Erstellen benutzerdefinierter Unternehmenskonfigurationspakete</span><span class="sxs-lookup"><span data-stu-id="84c55-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="84c55-105">Während Ihr Unternehmen wächst, werden Sie sich wahrscheinlich mit der Zeit auf einen Satz von Mandantentypen festlegen, den Sie auf die meisten Ihrer Debitoren anwenden können.</span><span class="sxs-lookup"><span data-stu-id="84c55-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="84c55-106">Sie können Ihren Implementierungsprozess rationalisieren, indem Sie diese Arten zu Konfigurationspaketen verarbeiten, die für die Wiederverwendung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="84c55-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="84c55-107">Im Allgemeinen erstellen Sie ein Konfigurationspaket pro Funktionsbereich, zum Beispiel ein Paket für Ihre Fertigungsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="84c55-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="84c55-108">Dadurch können Sie nach Bedarf neue Bereiche in einem Mandanten anwenden und einrichten.</span><span class="sxs-lookup"><span data-stu-id="84c55-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="84c55-109">Ein anderer Ansatz wäre die Erstellung eines Pakets, das die Tabellen enthält, die die Einrichtung definieren, etwa wie folgt:</span><span class="sxs-lookup"><span data-stu-id="84c55-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="84c55-110">Anlagen Einrichtung</span><span class="sxs-lookup"><span data-stu-id="84c55-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="84c55-111">Finanzbuchhaltungs-Einrichtung:</span><span class="sxs-lookup"><span data-stu-id="84c55-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="84c55-112">Lager Einrichtung</span><span class="sxs-lookup"><span data-stu-id="84c55-112">Inventory Setup</span></span>  
-   <span data-ttu-id="84c55-113">Produktion Einrichtung</span><span class="sxs-lookup"><span data-stu-id="84c55-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="84c55-114">Kreditoren und Einkauf Einr.</span><span class="sxs-lookup"><span data-stu-id="84c55-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="84c55-115">Marketing & Vertrieb Einr.</span><span class="sxs-lookup"><span data-stu-id="84c55-115">Marketing Setup</span></span>  
-   <span data-ttu-id="84c55-116">Service Einrichtung</span><span class="sxs-lookup"><span data-stu-id="84c55-116">Service Setup</span></span>  
-   <span data-ttu-id="84c55-117">Debitoren und Verkauf Einr.</span><span class="sxs-lookup"><span data-stu-id="84c55-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="84c55-118">Logistik Einrichtung</span><span class="sxs-lookup"><span data-stu-id="84c55-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="84c55-119">Buchungsmatrix Einrichtung</span><span class="sxs-lookup"><span data-stu-id="84c55-119">General Posting Setup</span></span>  
-   <span data-ttu-id="84c55-120">MwSt.-Buchungsmatrix</span><span class="sxs-lookup"><span data-stu-id="84c55-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="84c55-121">Lagerbuchungseinrichtung</span><span class="sxs-lookup"><span data-stu-id="84c55-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="84c55-122">Um eine vollständige Liste von Einrichtungstabellen zu sehen, wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Sie wünschen“ geöffnet wird](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Manuelle Einrichtung** ein und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="84c55-122">To see a complete list of setup tables, Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Manual Setup**, and then choose the related link.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="84c55-123">Seien Sie vorsichtig, wenn Sie Tabellen oder Felder auswählen, die denselben zeitlichen Namen haben, sich jedoch durch Sonderzeichen wie %, &, <,>, (, und) unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="84c55-123">Use caution if you choose tables or fields that have the same temporal name but are differentiated by special characters, such as %, &, <, >, (, and ).</span></span> <span data-ttu-id="84c55-124">Beispielsweise kann die Tabelle „XYZ“ die Felder „Feld 1“ und „Feld 1%“ enthalten.</span><span class="sxs-lookup"><span data-stu-id="84c55-124">For example, table "XYZ" might contain the "Field 1" and "Field 1%" fields.</span></span>
>
> <span data-ttu-id="84c55-125">Der XML-Prozessor akzeptiert nur einige Sonderzeichen und entfernt diejenigen, die er nicht akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="84c55-125">The XML processor accepts only some special characters, and will remove those it does not.</span></span> <span data-ttu-id="84c55-126">Wenn das Entfernen eines Sonderzeichens, wie z. B. des %-Zeichens in „Feld 1 %“, zu zwei oder mehr Tabellen oder Feldern mit demselben Namen führt, tritt beim Exportieren oder Importieren eines Konfigurationspakets ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="84c55-126">If removing a special character, such as the % sign in "Field 1%," results in two or more tables or fields with the same name an error will occur when you export or import a configuration package.</span></span>

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="84c55-127">Vorgehensweise: Erstellen benutzerdefinierter Unternehmenskonfigurationspakete</span><span class="sxs-lookup"><span data-stu-id="84c55-127">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="84c55-128">Erstellen eines neuen Mandanten.</span><span class="sxs-lookup"><span data-stu-id="84c55-128">Create a new company.</span></span> <span data-ttu-id="84c55-129">Weitere Informationen finden Sie unter [Neue Mandanten erstellen in Business Central](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="84c55-129">For more information, see [Creating New Companies in Business Central](about-new-company.md).</span></span>  
3.  <span data-ttu-id="84c55-130">Richten Sie den neuen Mandanten so ein, wie Sie ihn benötigen.</span><span class="sxs-lookup"><span data-stu-id="84c55-130">Set up the new company in the way you need.</span></span> <span data-ttu-id="84c55-131">Füllen Sie alle erforderlichen Einrichtungstabellen aus.</span><span class="sxs-lookup"><span data-stu-id="84c55-131">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="84c55-132">Öffnen des neuen Mandanten</span><span class="sxs-lookup"><span data-stu-id="84c55-132">Open the new company.</span></span>
5. <span data-ttu-id="84c55-133">Öffnen Sie das Fenster **Konfigurationsarbeitsblatt**.</span><span class="sxs-lookup"><span data-stu-id="84c55-133">Open the **Configuration Worksheet** page.</span></span>  
6.  <span data-ttu-id="84c55-134">Fügen Sie die Tabellen hinzu, die Sie zu einem anderen Mandanten auf dem Arbeitsblatt übertragen möchten.</span><span class="sxs-lookup"><span data-stu-id="84c55-134">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="84c55-135">Weisen Sie die Arbeitsblattzeilen dem Paket zu.</span><span class="sxs-lookup"><span data-stu-id="84c55-135">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="84c55-136">Erstellen Sie einen Fragebogen für die am häufigsten verwendeten Einrichtungstabellen.</span><span class="sxs-lookup"><span data-stu-id="84c55-136">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="84c55-137">Erstellen Sie Konfigurationsvorlagen, um es zu erleichtern, Stammdaten, beispielsweise Debitoren oder Artikel, zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="84c55-137">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="84c55-138">Exportieren Sie Ihr Paket als eine .rapidstart-Datei.</span><span class="sxs-lookup"><span data-stu-id="84c55-138">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="84c55-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84c55-139">See Also</span></span>  
[<span data-ttu-id="84c55-140">Einrichten eines Unternehmens mit RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="84c55-140">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="84c55-141">Verwaltung</span><span class="sxs-lookup"><span data-stu-id="84c55-141">Administration</span></span>](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]