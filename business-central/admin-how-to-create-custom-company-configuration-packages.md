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
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 868972e4d53d858834ba5985a3de3ffa1d4dcc6b
ms.contentlocale: de-de
ms.lasthandoff: 11/22/2018

---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="534a6-104">Vorgehensweise: Erstellen benutzerdefinierter Unternehmenskonfigurationspakete</span><span class="sxs-lookup"><span data-stu-id="534a6-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="534a6-105">Während Ihr Unternehmen wächst, werden Sie sich wahrscheinlich mit der Zeit auf einen Satz von Mandantentypen festlegen, den Sie auf die meisten Ihrer Debitoren anwenden können.</span><span class="sxs-lookup"><span data-stu-id="534a6-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="534a6-106">Sie können Ihren Implementierungsprozess rationalisieren, indem Sie diese Arten zu Konfigurationspaketen verarbeiten, die für die Wiederverwendung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="534a6-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="534a6-107">Im Allgemeinen erstellen Sie ein Konfigurationspaket pro Funktionsbereich, zum Beispiel ein Paket für Ihre Fertigungsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="534a6-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="534a6-108">Dadurch können Sie nach Bedarf neue Bereiche in einem Mandanten anwenden und einrichten.</span><span class="sxs-lookup"><span data-stu-id="534a6-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="534a6-109">Ein anderer Ansatz wäre die Erstellung eines Pakets, das die Tabellen enthält, die die Einrichtung definieren, etwa wie folgt:</span><span class="sxs-lookup"><span data-stu-id="534a6-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="534a6-110">Anlagen Einrichtung</span><span class="sxs-lookup"><span data-stu-id="534a6-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="534a6-111">Finanzbuchhaltungs-Einrichtung:</span><span class="sxs-lookup"><span data-stu-id="534a6-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="534a6-112">Lager Einrichtung</span><span class="sxs-lookup"><span data-stu-id="534a6-112">Inventory Setup</span></span>  
-   <span data-ttu-id="534a6-113">Produktion Einrichtung</span><span class="sxs-lookup"><span data-stu-id="534a6-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="534a6-114">Kreditoren und Einkauf Einr.</span><span class="sxs-lookup"><span data-stu-id="534a6-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="534a6-115">Marketing & Vertrieb Einr.</span><span class="sxs-lookup"><span data-stu-id="534a6-115">Marketing Setup</span></span>  
-   <span data-ttu-id="534a6-116">Service Einrichtung</span><span class="sxs-lookup"><span data-stu-id="534a6-116">Service Setup</span></span>  
-   <span data-ttu-id="534a6-117">Debitoren und Verkauf Einr.</span><span class="sxs-lookup"><span data-stu-id="534a6-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="534a6-118">Logistik Einrichtung</span><span class="sxs-lookup"><span data-stu-id="534a6-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="534a6-119">Buchungsmatrix Einrichtung</span><span class="sxs-lookup"><span data-stu-id="534a6-119">General Posting Setup</span></span>  
-   <span data-ttu-id="534a6-120">MwSt.-Buchungsmatrix</span><span class="sxs-lookup"><span data-stu-id="534a6-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="534a6-121">Lagerbuchungseinrichtung</span><span class="sxs-lookup"><span data-stu-id="534a6-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="534a6-122">Um eine vollständige Liste von Tabellen-Einrichtungen zu sehen, wählen Sie das Symbol ![Glühlampe, mit der die Funktion Wie möchten Sie weiter verfahren geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") und geben Sie **Einrichtung** ein und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="534a6-122">To see a complete list of setup tables, Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Setup**, and then choose the related link.</span></span>  

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="534a6-123">Vorgehensweise: Erstellen benutzerdefinierter Unternehmenskonfigurationspakete</span><span class="sxs-lookup"><span data-stu-id="534a6-123">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="534a6-124">Erstellen Sie in der Liste eine neue [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="534a6-124">Create a new [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="534a6-125">***NICHT MÖGLICHER Link, um für das Erstellen eines neuen Tenants" zu helfen***.</span><span class="sxs-lookup"><span data-stu-id="534a6-125">***NOT POSSIBLE Link to help for "Creating a New Tenant"***.</span></span>   
2.  <span data-ttu-id="534a6-126">Erstellen Sie einen neuen Mandanten für die Branchen- oder die Lösungsvorlage.</span><span class="sxs-lookup"><span data-stu-id="534a6-126">Create a new company for the industry or solution template.</span></span> <span data-ttu-id="534a6-127">Weitere Informationen zum Erstellen einer Vorlage finden Sie unter [Vorgehensweise: Ein neues Unternehmen  erstellen](admin-how-to-create-a-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="534a6-127">For more information, see [Create a New Company](admin-how-to-create-a-new-company.md).</span></span>  
3.  <span data-ttu-id="534a6-128">Richten Sie den neuen Mandanten so ein, wie Sie ihn benötigen.</span><span class="sxs-lookup"><span data-stu-id="534a6-128">Setup the new company in the way you need.</span></span> <span data-ttu-id="534a6-129">Füllen Sie alle erforderlichen Einrichtungstabellen aus.</span><span class="sxs-lookup"><span data-stu-id="534a6-129">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="534a6-130">Öffnen des neuen Mandanten</span><span class="sxs-lookup"><span data-stu-id="534a6-130">Open the new company.</span></span>
5. <span data-ttu-id="534a6-131">Öffnen Sie das Fenster **Konfigurationsvorschlag**.</span><span class="sxs-lookup"><span data-stu-id="534a6-131">Open the **Configuration Worksheet** page.</span></span>  
6.  <span data-ttu-id="534a6-132">Fügen Sie die Tabellen hinzu, die Sie zu einem anderen Mandanten auf dem Arbeitsblatt übertragen möchten.</span><span class="sxs-lookup"><span data-stu-id="534a6-132">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="534a6-133">Weisen Sie die Arbeitsblattzeilen dem Paket zu.</span><span class="sxs-lookup"><span data-stu-id="534a6-133">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="534a6-134">Erstellen Sie einen Fragebogen für die am häufigsten verwendeten Einrichtungstabellen.</span><span class="sxs-lookup"><span data-stu-id="534a6-134">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="534a6-135">Erstellen Sie Konfigurationsvorlagen, um es zu erleichtern, Stammdaten, beispielsweise Debitoren oder Artikel, zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="534a6-135">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="534a6-136">Exportieren Sie Ihr Paket als eine .rapidstart-Datei.</span><span class="sxs-lookup"><span data-stu-id="534a6-136">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="534a6-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="534a6-137">See Also</span></span>  
[<span data-ttu-id="534a6-138">Einrichten von Mandanten mit RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="534a6-138">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="534a6-139">Verwaltung</span><span class="sxs-lookup"><span data-stu-id="534a6-139">Administration</span></span>](admin-setup-and-administration.md)

