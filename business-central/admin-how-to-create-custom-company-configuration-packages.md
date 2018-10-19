---
title: 'Vorgehensweise: Erstellen benutzerdefinierter Unternehmenskonfigurationspakete | Microsoft Docs'
description: "Während Ihr Unternehmen wächst, werden Sie sich wahrscheinlich mit der Zeit auf einen Satz von Mandantentypen festlegen, den Sie auf die meisten Ihrer Debitoren anwenden können. Sie können Ihren Implementierungsprozess rationalisieren, indem Sie diese Arten zu Konfigurationspaketen verarbeiten, die für die Wiederverwendung verfügbar sind."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e26174fcf723e13ef5a9ed0b386006c0439e1c7a
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="3f09d-104">Vorgehensweise: Erstellen benutzerdefinierter Unternehmenskonfigurationspakete</span><span class="sxs-lookup"><span data-stu-id="3f09d-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="3f09d-105">Während Ihr Unternehmen wächst, werden Sie sich wahrscheinlich mit der Zeit auf einen Satz von Mandantentypen festlegen, den Sie auf die meisten Ihrer Debitoren anwenden können.</span><span class="sxs-lookup"><span data-stu-id="3f09d-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="3f09d-106">Sie können Ihren Implementierungsprozess rationalisieren, indem Sie diese Arten zu Konfigurationspaketen verarbeiten, die für die Wiederverwendung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="3f09d-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="3f09d-107">Im Allgemeinen erstellen Sie ein Konfigurationspaket pro Funktionsbereich, zum Beispiel ein Paket für Ihre Fertigungsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="3f09d-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="3f09d-108">Dadurch können Sie nach Bedarf neue Bereiche in einem Mandanten anwenden und einrichten.</span><span class="sxs-lookup"><span data-stu-id="3f09d-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="3f09d-109">Ein anderer Ansatz wäre die Erstellung eines Pakets, das die Tabellen enthält, die die Einrichtung definieren, etwa wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3f09d-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="3f09d-110">Anlagen Einrichtung</span><span class="sxs-lookup"><span data-stu-id="3f09d-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="3f09d-111">Finanzbuchhaltungs-Einrichtung:</span><span class="sxs-lookup"><span data-stu-id="3f09d-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="3f09d-112">Lager Einrichtung</span><span class="sxs-lookup"><span data-stu-id="3f09d-112">Inventory Setup</span></span>  
-   <span data-ttu-id="3f09d-113">Produktion Einrichtung</span><span class="sxs-lookup"><span data-stu-id="3f09d-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="3f09d-114">Kreditoren und Einkauf Einr.</span><span class="sxs-lookup"><span data-stu-id="3f09d-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="3f09d-115">Marketing & Vertrieb Einr.</span><span class="sxs-lookup"><span data-stu-id="3f09d-115">Marketing Setup</span></span>  
-   <span data-ttu-id="3f09d-116">Service Einrichtung</span><span class="sxs-lookup"><span data-stu-id="3f09d-116">Service Setup</span></span>  
-   <span data-ttu-id="3f09d-117">Debitoren und Verkauf Einr.</span><span class="sxs-lookup"><span data-stu-id="3f09d-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="3f09d-118">Logistik Einrichtung</span><span class="sxs-lookup"><span data-stu-id="3f09d-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="3f09d-119">Buchungsmatrix Einrichtung</span><span class="sxs-lookup"><span data-stu-id="3f09d-119">General Posting Setup</span></span>  
-   <span data-ttu-id="3f09d-120">MwSt.-Buchungsmatrix</span><span class="sxs-lookup"><span data-stu-id="3f09d-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="3f09d-121">Lagerbuchungseinrichtung</span><span class="sxs-lookup"><span data-stu-id="3f09d-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="3f09d-122">Um eine vollständige Liste von Tabellen-Einrichtungen zu sehen, wählen Sie das Symbol ![Glühlampe, mit der die Funktion Wie möchten Sie weiter verfahren geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") und geben Sie **Einrichtung** ein und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="3f09d-122">To see a complete list of setup tables, Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Setup**, and then choose the related link.</span></span>  

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="3f09d-123">Vorgehensweise: Erstellen benutzerdefinierter Unternehmenskonfigurationspakete</span><span class="sxs-lookup"><span data-stu-id="3f09d-123">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="3f09d-124">Erstellen Sie in der Liste eine neue [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="3f09d-124">Create a new [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="3f09d-125">***NICHT MÖGLICHER Link, um für das Erstellen eines neuen Tenants" zu helfen***.</span><span class="sxs-lookup"><span data-stu-id="3f09d-125">***NOT POSSIBLE Link to help for "Creating a New Tenant"***.</span></span>   
2.  <span data-ttu-id="3f09d-126">Erstellen Sie einen neuen Mandanten für die Branchen- oder die Lösungsvorlage.</span><span class="sxs-lookup"><span data-stu-id="3f09d-126">Create a new company for the industry or solution template.</span></span> <span data-ttu-id="3f09d-127">Weitere Informationen zum Erstellen einer Vorlage finden Sie unter [Vorgehensweise: Ein neues Unternehmen  erstellen](admin-how-to-create-a-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="3f09d-127">For more information, see [Create a New Company](admin-how-to-create-a-new-company.md).</span></span>  
3.  <span data-ttu-id="3f09d-128">Richten Sie den neuen Mandanten so ein, wie Sie ihn benötigen.</span><span class="sxs-lookup"><span data-stu-id="3f09d-128">Setup the new company in the way you need.</span></span> <span data-ttu-id="3f09d-129">Füllen Sie alle erforderlichen Einrichtungstabellen aus.</span><span class="sxs-lookup"><span data-stu-id="3f09d-129">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="3f09d-130">Öffnen des neuen Mandanten</span><span class="sxs-lookup"><span data-stu-id="3f09d-130">Open the new company.</span></span>
5. <span data-ttu-id="3f09d-131">Öffnen Sie das Fenster **Konfigurationsvorschlag**.</span><span class="sxs-lookup"><span data-stu-id="3f09d-131">Open the **Configuration Worksheet** window.</span></span>  
6.  <span data-ttu-id="3f09d-132">Fügen Sie die Tabellen hinzu, die Sie zu einem anderen Mandanten auf dem Arbeitsblatt übertragen möchten.</span><span class="sxs-lookup"><span data-stu-id="3f09d-132">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="3f09d-133">Weisen Sie die Arbeitsblattzeilen dem Paket zu.</span><span class="sxs-lookup"><span data-stu-id="3f09d-133">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="3f09d-134">Erstellen Sie einen Fragebogen für die am häufigsten verwendeten Einrichtungstabellen.</span><span class="sxs-lookup"><span data-stu-id="3f09d-134">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="3f09d-135">Erstellen Sie Konfigurationsvorlagen, um es zu erleichtern, Stammdaten, beispielsweise Debitoren oder Artikel, zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3f09d-135">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="3f09d-136">Exportieren Sie Ihr Paket als eine .rapidstart-Datei.</span><span class="sxs-lookup"><span data-stu-id="3f09d-136">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3f09d-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f09d-137">See Also</span></span>  
[<span data-ttu-id="3f09d-138">Einrichten von Mandanten mit RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="3f09d-138">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="3f09d-139">Verwaltung</span><span class="sxs-lookup"><span data-stu-id="3f09d-139">Administration</span></span>](admin-setup-and-administration.md)

