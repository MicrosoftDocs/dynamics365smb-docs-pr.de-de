---
title: 'Vorgehensweise: Erstellen benutzerdefinierter Unternehmenskonfigurationspakete | Microsoft Docs'
description: Während Ihr Unternehmen wächst, werden Sie sich wahrscheinlich mit der Zeit auf einen Satz von Mandantentypen festlegen, den Sie auf die meisten Ihrer Debitoren anwenden können. Sie können Ihren Implementierungsprozess rationalisieren, indem Sie diese Arten zu Konfigurationspaketen verarbeiten, die für die Wiederverwendung verfügbar sind.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 8bbd9b07976dc4d54f8bee9f5eb8c23270c5a10c
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187172"
---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="67f70-104">Vorgehensweise: Erstellen benutzerdefinierter Unternehmenskonfigurationspakete</span><span class="sxs-lookup"><span data-stu-id="67f70-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="67f70-105">Während Ihr Unternehmen wächst, werden Sie sich wahrscheinlich mit der Zeit auf einen Satz von Mandantentypen festlegen, den Sie auf die meisten Ihrer Debitoren anwenden können.</span><span class="sxs-lookup"><span data-stu-id="67f70-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="67f70-106">Sie können Ihren Implementierungsprozess rationalisieren, indem Sie diese Arten zu Konfigurationspaketen verarbeiten, die für die Wiederverwendung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="67f70-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="67f70-107">Im Allgemeinen erstellen Sie ein Konfigurationspaket pro Funktionsbereich, zum Beispiel ein Paket für Ihre Fertigungsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="67f70-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="67f70-108">Dadurch können Sie nach Bedarf neue Bereiche in einem Mandanten anwenden und einrichten.</span><span class="sxs-lookup"><span data-stu-id="67f70-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="67f70-109">Ein anderer Ansatz wäre die Erstellung eines Pakets, das die Tabellen enthält, die die Einrichtung definieren, etwa wie folgt:</span><span class="sxs-lookup"><span data-stu-id="67f70-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="67f70-110">Anlagen Einrichtung</span><span class="sxs-lookup"><span data-stu-id="67f70-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="67f70-111">Finanzbuchhaltungs-Einrichtung:</span><span class="sxs-lookup"><span data-stu-id="67f70-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="67f70-112">Lager Einrichtung</span><span class="sxs-lookup"><span data-stu-id="67f70-112">Inventory Setup</span></span>  
-   <span data-ttu-id="67f70-113">Produktion Einrichtung</span><span class="sxs-lookup"><span data-stu-id="67f70-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="67f70-114">Kreditoren und Einkauf Einr.</span><span class="sxs-lookup"><span data-stu-id="67f70-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="67f70-115">Marketing & Vertrieb Einr.</span><span class="sxs-lookup"><span data-stu-id="67f70-115">Marketing Setup</span></span>  
-   <span data-ttu-id="67f70-116">Service Einrichtung</span><span class="sxs-lookup"><span data-stu-id="67f70-116">Service Setup</span></span>  
-   <span data-ttu-id="67f70-117">Debitoren und Verkauf Einr.</span><span class="sxs-lookup"><span data-stu-id="67f70-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="67f70-118">Logistik Einrichtung</span><span class="sxs-lookup"><span data-stu-id="67f70-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="67f70-119">Buchungsmatrix Einrichtung</span><span class="sxs-lookup"><span data-stu-id="67f70-119">General Posting Setup</span></span>  
-   <span data-ttu-id="67f70-120">MwSt.-Buchungsmatrix</span><span class="sxs-lookup"><span data-stu-id="67f70-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="67f70-121">Lagerbuchungseinrichtung</span><span class="sxs-lookup"><span data-stu-id="67f70-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="67f70-122">Um eine vollständige Liste von Einrichtungstabellen zu sehen, wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Sie wünschen“ geöffnet wird](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Manuelle Einrichtung** ein und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="67f70-122">To see a complete list of setup tables, Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Manual Setup**, and then choose the related link.</span></span>  

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="67f70-123">Vorgehensweise: Erstellen benutzerdefinierter Unternehmenskonfigurationspakete</span><span class="sxs-lookup"><span data-stu-id="67f70-123">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="67f70-124">Erstellen eines neuen Mandanten.</span><span class="sxs-lookup"><span data-stu-id="67f70-124">Create a new company.</span></span> <span data-ttu-id="67f70-125">Weitere Informationen finden Sie unter [Neue Mandanten erstellen in Business Central](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="67f70-125">For more information, see [Creating New Companies in Business Central](about-new-company.md).</span></span>  
3.  <span data-ttu-id="67f70-126">Richten Sie den neuen Mandanten so ein, wie Sie ihn benötigen.</span><span class="sxs-lookup"><span data-stu-id="67f70-126">Set up the new company in the way you need.</span></span> <span data-ttu-id="67f70-127">Füllen Sie alle erforderlichen Einrichtungstabellen aus.</span><span class="sxs-lookup"><span data-stu-id="67f70-127">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="67f70-128">Öffnen des neuen Mandanten</span><span class="sxs-lookup"><span data-stu-id="67f70-128">Open the new company.</span></span>
5. <span data-ttu-id="67f70-129">Öffnen Sie das Fenster **Konfigurationsvorschlag**.</span><span class="sxs-lookup"><span data-stu-id="67f70-129">Open the **Configuration Worksheet** page.</span></span>  
6.  <span data-ttu-id="67f70-130">Fügen Sie die Tabellen hinzu, die Sie zu einem anderen Mandanten auf dem Arbeitsblatt übertragen möchten.</span><span class="sxs-lookup"><span data-stu-id="67f70-130">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="67f70-131">Weisen Sie die Arbeitsblattzeilen dem Paket zu.</span><span class="sxs-lookup"><span data-stu-id="67f70-131">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="67f70-132">Erstellen Sie einen Fragebogen für die am häufigsten verwendeten Einrichtungstabellen.</span><span class="sxs-lookup"><span data-stu-id="67f70-132">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="67f70-133">Erstellen Sie Konfigurationsvorlagen, um es zu erleichtern, Stammdaten, beispielsweise Debitoren oder Artikel, zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="67f70-133">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="67f70-134">Exportieren Sie Ihr Paket als eine .rapidstart-Datei.</span><span class="sxs-lookup"><span data-stu-id="67f70-134">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="67f70-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67f70-135">See Also</span></span>  
[<span data-ttu-id="67f70-136">Einrichten eines Unternehmens mit RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="67f70-136">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="67f70-137">Verwaltung</span><span class="sxs-lookup"><span data-stu-id="67f70-137">Administration</span></span>](admin-setup-and-administration.md)
