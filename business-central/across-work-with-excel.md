---
title: Anzeigen und Arbeit in Excel aus Business Central
description: Mehr erfahren, wie Sie die Finanzaufstellungen in Microsoft Excel von  Business Central für eine Analyse der Daten öffnen können.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 11/06/2020
ms.author: jswymer
ms.openlocfilehash: 5e585d4bc7d9f7ce159671c10298f734fd5a09d5
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378823"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="918c8-103">Anzeigen und Arbeit in Excel aus Business Central</span><span class="sxs-lookup"><span data-stu-id="918c8-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="918c8-104">Mit Seiten, die eine Liste der Datensätze in den Zeilen und Spalten anzeigen, wie eine Liste von Debitoren von Verkaufsaufträgen oder Rechnungen können Sie die Daten mithilfe von Microsoft Excel anzeigen.</span><span class="sxs-lookup"><span data-stu-id="918c8-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="918c8-105">Dazu haben Sie zwei Optionen.</span><span class="sxs-lookup"><span data-stu-id="918c8-105">To do this, you have two options.</span></span> <span data-ttu-id="918c8-106">Sie können entweder die **In Excel öffnen** Aktion oder die **Bearbeiten Sie in Excel** Aktion dieser Seite auswählen.</span><span class="sxs-lookup"><span data-stu-id="918c8-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="918c8-107">Der Unterschied zwischen den beiden Methoden ist wie folgt::</span><span class="sxs-lookup"><span data-stu-id="918c8-107">The differences between the two actions are as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="918c8-108">In Excel öffnen</span><span class="sxs-lookup"><span data-stu-id="918c8-108">Open in Excel</span></span>

- <span data-ttu-id="918c8-109">Mit dieser Aktion respektiert Excel alle Filter auf der Seite, die die angezeigten Datensätze einschränken.</span><span class="sxs-lookup"><span data-stu-id="918c8-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="918c8-110">Das Excel-Arbeitsblatt enthält die gleichen Zeilen und Spalten, die auf der Seite in [!INCLUDE[prod_short](includes/prod_short.md)] erscheinen.</span><span class="sxs-lookup"><span data-stu-id="918c8-110">The Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

- <span data-ttu-id="918c8-111">Sie können Änderungen mit Datensätzen in Excel vornehmen, aber Sie können die Änderungen nicht auf  [!INCLUDE[prod_short](includes/prod_short.md)] veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="918c8-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="918c8-112">Sie können die Änderungen in die Excel-Datei nur auf dem Computer speichern.</span><span class="sxs-lookup"><span data-stu-id="918c8-112">You can only save the changes to Excel file on your computer.</span></span>

- <span data-ttu-id="918c8-113">Diese Aktion geht auf Windows und Mac Os.</span><span class="sxs-lookup"><span data-stu-id="918c8-113">This action works on both on Windows and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="918c8-114">Für [!INCLUDE[prod_short](includes/prod_short.md)] lokal ist die Aktion **In Excel öffnen** standardmäßig verfügbar.</span><span class="sxs-lookup"><span data-stu-id="918c8-114">For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="918c8-115">Wenn Sie jedoch [!INCLUDE[prod_short](includes/prod_short.md)] lokal für die Bearbeitung von Daten in Excel einrichten, wird die Aktion **In Excel öffnen** durch die Aktion **In Excel bearbeiten** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="918c8-115">However, if you set up [!INCLUDE[prod_short](includes/prod_short.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="918c8-116">In Excel bearbeiten</span><span class="sxs-lookup"><span data-stu-id="918c8-116">Edit in Excel</span></span>

- <span data-ttu-id="918c8-117">Mit dieser Aktion berücksichtigt Excel die meisten Filter auf der Seite, die die angezeigten Datensätze einschränken, sodass das Excel-Arbeitsblatt fast dieselben Datensätze und Spalten enthält.</span><span class="sxs-lookup"><span data-stu-id="918c8-117">With this action, Excel respects most filters on the page that limit the records shown, so the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="918c8-118">Der Vorteil der **Bearbeiten Sie in Excel** Aktion ist, dass es Sie Änderungen mit Datensätzen in Excel vornimmt und die Änderungen zurück in [!INCLUDE[prod_short](includes/prod_short.md)] veröffentlichen können,</span><span class="sxs-lookup"><span data-stu-id="918c8-118">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

- <span data-ttu-id="918c8-119">Das geht nur auf Windows; nicht Mac Os.</span><span class="sxs-lookup"><span data-stu-id="918c8-119">It only works on Windows; not macOS.</span></span>

- <span data-ttu-id="918c8-120">Sie können das Unternehmen, mit dem Sie zusammenarbeiten, wechseln.</span><span class="sxs-lookup"><span data-stu-id="918c8-120">You can switch the company that you are working with.</span></span> <span data-ttu-id="918c8-121">Um das Unternehmen zu wechseln, wählen Sie dazu im Excel-Add-In-Fensterbereich das Symbol **Optionen** ![Excel-Add-In-Optionen](media/cogwheel.png "Excel-Add-In-Optionen") und wählen Sie dann das Unternehmen aus dem Feld **Unternehmen**.</span><span class="sxs-lookup"><span data-stu-id="918c8-121">To switch company, select the **Options** icon ![Excel add-in options](media/cogwheel.png "Excel add-in options") in the Excel Add-in pane, then select the company from the **Company** field.</span></span>  

    > [!IMPORTANT]
    > <span data-ttu-id="918c8-122">Wenn Sie das Unternehmen ändern, stellen Sie sicher, dass das Feld **Umgebung** nicht leer ist.</span><span class="sxs-lookup"><span data-stu-id="918c8-122">When changing the company, make sure that the **Environment** field is not empty.</span></span> <span data-ttu-id="918c8-123">Wenn dies der Fall ist, dann stellen Sie sie auf eine der verfügbaren Optionen ein; andernfalls wird das Add-In nicht korrekt funktionieren.</span><span class="sxs-lookup"><span data-stu-id="918c8-123">If it is, then set it to one of the available options; otherwise, the add-in will not work correctly.</span></span>  

<span data-ttu-id="918c8-124">Wenn Sie Änderungen am Add-In vornehmen, müssen Sie es neu laden, um die Verbindung zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="918c8-124">If you make changes to the add-in, you must reload it to update the connection.</span></span> <span data-ttu-id="918c8-125">Verwenden Sie zum Neuladen das ![Excel-Add-In-Menü](media/excel-addin-menu.png "Excel-Add-In-Menü") in der oberen rechten Ecke des Add-Ins.</span><span class="sxs-lookup"><span data-stu-id="918c8-125">To reload, use the ![Excel add-in menu](media/excel-addin-menu.png "Excel add-in menu") menu in the top-right corner of the add-in.</span></span> <span data-ttu-id="918c8-126">Wenn Sie das Add-In nicht laden können, wenden Sie sich an Ihren Administrator.</span><span class="sxs-lookup"><span data-stu-id="918c8-126">If you cannot load the add-in, talk to your administrator.</span></span> <span data-ttu-id="918c8-127">Wenn Sie der Administrator sind, lesen Sie [Einrichten des Excel-Add-Ins zum Bearbeiten von Business Central-Daten](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="918c8-127">If you are the administrator, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

> [!NOTE]
> <span data-ttu-id="918c8-128">Für [!INCLUDE[prod_short](includes/prod_short.md)] vor Ort ist die Aktion **In Excel bearbeiten** nur verfügbar, wenn das Excel-Add-In von Ihrem Administrator konfiguriert wurde, und nur für den Web-Client verfügbar.</span><span class="sxs-lookup"><span data-stu-id="918c8-128">For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator, and only available for the Web client.</span></span> <span data-ttu-id="918c8-129">Wenn Sie als Administrator erfahren möchten, wie Sie das Excel-Add-In installieren, lesen Sie [Einrichtung des Excel-Add-Ins zur Bearbeitung von Business Central Daten](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="918c8-129">For administrators, if you want to learn how to install the Excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="918c8-130">Sehen Sie sich die Unterschiede zwischen den Optionen an</span><span class="sxs-lookup"><span data-stu-id="918c8-130">See the differences between the options</span></span>
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="918c8-131">Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="918c8-131">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="918c8-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="918c8-132">See Also</span></span>

[<span data-ttu-id="918c8-133">Finanzauswertungen analysieren in Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="918c8-133">Analyzing Financial Statements in Microsoft Excel</span></span>](finance-analyze-excel.md)  
[<span data-ttu-id="918c8-134">Arbeiten mit Business Central</span><span class="sxs-lookup"><span data-stu-id="918c8-134">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="918c8-135">Verbesserungen der Excel-Integration in der Veröffentlichungswelle 2 von 2019</span><span class="sxs-lookup"><span data-stu-id="918c8-135">Enhancements to Excel integration in 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]