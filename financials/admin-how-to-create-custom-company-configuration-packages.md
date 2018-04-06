---
title: 'Vorgehensweise: Erstellen benutzerdefinierter Unternehmenskonfigurationspakete | Microsoft Docs'
description: "Während Ihr Unternehmen wächst, werden Sie sich wahrscheinlich mit der Zeit auf einen Satz von Mandantentypen festlegen, den Sie auf die meisten Ihrer Debitoren anwenden können. Sie können Ihren Implementierungsprozess rationalisieren, indem Sie diese Arten zu Konfigurationspaketen verarbeiten, die für die Wiederverwendung verfügbar sind."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/05/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 37fe7a482b88626adff1ef16496a785399d19a8d
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="c5988-104">Vorgehensweise: Erstellen benutzerdefinierter Unternehmenskonfigurationspakete</span><span class="sxs-lookup"><span data-stu-id="c5988-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="c5988-105">Während Ihr Unternehmen wächst, werden Sie sich wahrscheinlich mit der Zeit auf einen Satz von Mandantentypen festlegen, den Sie auf die meisten Ihrer Debitoren anwenden können.</span><span class="sxs-lookup"><span data-stu-id="c5988-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="c5988-106">Sie können Ihren Implementierungsprozess rationalisieren, indem Sie diese Arten zu Konfigurationspaketen verarbeiten, die für die Wiederverwendung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c5988-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="c5988-107">Im Allgemeinen erstellen Sie ein Konfigurationspaket pro Funktionsbereich, zum Beispiel ein Paket für Ihre Fertigungsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="c5988-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="c5988-108">Dadurch können Sie nach Bedarf neue Bereiche in einem Mandanten anwenden und einrichten.</span><span class="sxs-lookup"><span data-stu-id="c5988-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="c5988-109">Ein anderer Ansatz wäre die Erstellung eines Pakets, das die Tabellen enthält, die die Einrichtung definieren, etwa wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c5988-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="c5988-110">Anlagen Einrichtung</span><span class="sxs-lookup"><span data-stu-id="c5988-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="c5988-111">Finanzbuchhaltungs-Einrichtung:</span><span class="sxs-lookup"><span data-stu-id="c5988-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="c5988-112">Lager Einrichtung</span><span class="sxs-lookup"><span data-stu-id="c5988-112">Inventory Setup</span></span>  
-   <span data-ttu-id="c5988-113">Produktion Einrichtung</span><span class="sxs-lookup"><span data-stu-id="c5988-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="c5988-114">Kreditoren und Einkauf Einr.</span><span class="sxs-lookup"><span data-stu-id="c5988-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="c5988-115">Marketing & Vertrieb Einr.</span><span class="sxs-lookup"><span data-stu-id="c5988-115">Marketing Setup</span></span>  
-   <span data-ttu-id="c5988-116">Service Einrichtung</span><span class="sxs-lookup"><span data-stu-id="c5988-116">Service Setup</span></span>  
-   <span data-ttu-id="c5988-117">Debitoren und Verkauf Einr.</span><span class="sxs-lookup"><span data-stu-id="c5988-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="c5988-118">Logistik Einrichtung</span><span class="sxs-lookup"><span data-stu-id="c5988-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="c5988-119">Buchungsmatrix Einrichtung</span><span class="sxs-lookup"><span data-stu-id="c5988-119">General Posting Setup</span></span>  
-   <span data-ttu-id="c5988-120">MwSt.-Buchungsmatrix</span><span class="sxs-lookup"><span data-stu-id="c5988-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="c5988-121">Lagerbuchungseinrichtung</span><span class="sxs-lookup"><span data-stu-id="c5988-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="c5988-122">Um eine vollständige Liste der Einrichtungstabellen zu sehen, wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Einrichten** ein. Wählen Sie dann den betreffenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="c5988-122">To see a complete list of setup tables, Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Setup**, and then choose the related link.</span></span>  

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="c5988-123">Vorgehensweise: Erstellen benutzerdefinierter Unternehmenskonfigurationspakete</span><span class="sxs-lookup"><span data-stu-id="c5988-123">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="c5988-124">Erstellen Sie in der Liste eine neue [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="c5988-124">Create a new [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="c5988-125">***NICHT MÖGLICHER Link, um für das Erstellen eines neuen Tenants" zu helfen***.</span><span class="sxs-lookup"><span data-stu-id="c5988-125">***NOT POSSIBLE Link to help for "Creating a New Tenant"***.</span></span>   
2.  <span data-ttu-id="c5988-126">Erstellen Sie einen neuen Mandanten für die Branchen- oder die Lösungsvorlage.</span><span class="sxs-lookup"><span data-stu-id="c5988-126">Create a new company for the industry or solution template.</span></span> <span data-ttu-id="c5988-127">Weitere Informationen zum Erstellen einer Vorlage finden Sie unter [Vorgehensweise: Ein neues Unternehmen  erstellen](admin-how-to-create-a-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="c5988-127">For more information, see [Create a New Company](admin-how-to-create-a-new-company.md).</span></span>  
3.  <span data-ttu-id="c5988-128">Richten Sie den neuen Mandanten so ein, wie Sie ihn benötigen.</span><span class="sxs-lookup"><span data-stu-id="c5988-128">Setup the new company in the way you need.</span></span> <span data-ttu-id="c5988-129">Füllen Sie alle erforderlichen Einrichtungstabellen aus.</span><span class="sxs-lookup"><span data-stu-id="c5988-129">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="c5988-130">Öffnen des neuen Mandanten</span><span class="sxs-lookup"><span data-stu-id="c5988-130">Open the new company.</span></span>
5. <span data-ttu-id="c5988-131">Öffnen Sie das Fenster **Konfigurationsvorschlag**.</span><span class="sxs-lookup"><span data-stu-id="c5988-131">Open the **Configuration Worksheet** window.</span></span>  
6.  <span data-ttu-id="c5988-132">Fügen Sie die Tabellen hinzu, die Sie zu einem anderen Mandanten auf dem Arbeitsblatt übertragen möchten.</span><span class="sxs-lookup"><span data-stu-id="c5988-132">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="c5988-133">Weisen Sie die Arbeitsblattzeilen dem Paket zu.</span><span class="sxs-lookup"><span data-stu-id="c5988-133">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="c5988-134">Erstellen Sie einen Fragebogen für die am häufigsten verwendeten Einrichtungstabellen.</span><span class="sxs-lookup"><span data-stu-id="c5988-134">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="c5988-135">Erstellen Sie Konfigurationsvorlagen, um es zu erleichtern, Stammdaten, beispielsweise Debitoren oder Artikel, zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c5988-135">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="c5988-136">Exportieren Sie Ihr Paket als eine .rapidstart-Datei.</span><span class="sxs-lookup"><span data-stu-id="c5988-136">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c5988-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5988-137">See Also</span></span>  
[<span data-ttu-id="c5988-138">Einrichten von Mandanten mit RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="c5988-138">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="c5988-139">Verwaltung</span><span class="sxs-lookup"><span data-stu-id="c5988-139">Administration</span></span>](admin-setup-and-administration.md)

