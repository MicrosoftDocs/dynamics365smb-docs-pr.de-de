---
title: Daten mithilfe von Flow verbinden| Microsoft Docs
description: "Sie können Financials als Datenquelle zur Verfügung stellen und eine OData-URL Ihrer Webdienste festlegen, um eine Geschäfts-App mithilfe einem automatisierten Workflow erstellen."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ef4d841723b6bb0af37695a8c3ed1d805319be78
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a><span data-ttu-id="c2f41-103">[!INCLUDE[d365fin](includes/d365fin_md.md)]in einem automatisierten Workflow nutzen</span><span class="sxs-lookup"><span data-stu-id="c2f41-103">Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow</span></span>
<span data-ttu-id="c2f41-104">Sie können die Daten in [!INCLUDE[d365fin](includes/d365fin_md.md)] als Teil eines Workflows in Microsoft Flow verwenden.</span><span class="sxs-lookup"><span data-stu-id="c2f41-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="c2f41-105">Sie müssen ein gültiges Konto mit [!INCLUDE[d365fin](includes/d365fin_md.md)] und Flow haben.</span><span class="sxs-lookup"><span data-stu-id="c2f41-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a><span data-ttu-id="c2f41-106">Um [!INCLUDE[d365fin](includes/d365fin_md.md)] als Datenquelle in Flow hinzufügen</span><span class="sxs-lookup"><span data-stu-id="c2f41-106">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in Flow</span></span>
1. <span data-ttu-id="c2f41-107">In Ihrem Browser navigieren Sie zu [flow.microsoft.com](https://flow.microsoft.com/en-us/) und melden sich dann an.</span><span class="sxs-lookup"><span data-stu-id="c2f41-107">In your browser, navigate to [flow.microsoft.com](https://flow.microsoft.com/en-us/), and then sign in.</span></span>
2. <span data-ttu-id="c2f41-108">Wählen Sie **My Flows** im Menüband oben auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="c2f41-108">Choose **My Flows** from the ribbon at the top of the page.</span></span>
3. <span data-ttu-id="c2f41-109">Im Fenster **My Flows** wählen Sie die Option **Aus Leer erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="c2f41-109">In the **My Flows** window, choose the **Create from blank** option.</span></span>
4. <span data-ttu-id="c2f41-110">Aus der Liste der verfügbaren Triggern, wählen Sie einen der [!INCLUDE[d365fin](includes/d365fin_md.md)] verfügbaren Trigger aus:</span><span class="sxs-lookup"><span data-stu-id="c2f41-110">From the list of available triggers, select one of the [!INCLUDE[d365fin](includes/d365fin_md.md)] triggers available:</span></span>  
    <span data-ttu-id="c2f41-111">,*Wenn ein Datensatz erstellt wird*</span><span class="sxs-lookup"><span data-stu-id="c2f41-111">*When a record is created*,</span></span>  
    <span data-ttu-id="c2f41-112">,*Wenn ein Datensatz gelöscht wird*</span><span class="sxs-lookup"><span data-stu-id="c2f41-112">*When a record is deleted*,</span></span>  
    <span data-ttu-id="c2f41-113">,*Wenn ein Datensatz geändert wird*</span><span class="sxs-lookup"><span data-stu-id="c2f41-113">*When a record is modified*,</span></span>  
    <span data-ttu-id="c2f41-114">*Die Genehmigung für einen Debitor wird angefordert*,</span><span class="sxs-lookup"><span data-stu-id="c2f41-114">*When a customer approval is requested*,</span></span>  
    <span data-ttu-id="c2f41-115">*Genehmigung von Fibu Buch.-Blattname wird angefordert*,</span><span class="sxs-lookup"><span data-stu-id="c2f41-115">*When a general journal batch approval is requested*,</span></span>  
    <span data-ttu-id="c2f41-116">*Genehmigung von Fibu Buch.-Blattzeile wird angefordert*,</span><span class="sxs-lookup"><span data-stu-id="c2f41-116">*When a general journal line approval is requested*,</span></span>  
    <span data-ttu-id="c2f41-117">*Die Genehmigung für einen Artikel wird angefordert*,</span><span class="sxs-lookup"><span data-stu-id="c2f41-117">*When an item approval is requested*,</span></span>  
    <span data-ttu-id="c2f41-118">*Die Genehmigung für einen Einkaufsbeleg wird angefordert*,</span><span class="sxs-lookup"><span data-stu-id="c2f41-118">*When a purchase document approval is requested*,</span></span>  
    <span data-ttu-id="c2f41-119">*Die Genehmigung für einen Verkaufsbeleg wird angefordert* oder</span><span class="sxs-lookup"><span data-stu-id="c2f41-119">*When a sales document approval is requested*, or</span></span>  
    <span data-ttu-id="c2f41-120">*Die Genehmigung für einen Kreditor wird angefordert*.</span><span class="sxs-lookup"><span data-stu-id="c2f41-120">*When a vendor aproval is requested*.</span></span>
5. <span data-ttu-id="c2f41-121">Flow fordert Sie zur Eingabe der Informationen auf, die benötigt werden, um sich mit Ihren [!INCLUDE[d365fin](includes/d365fin_md.md)] Daten zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="c2f41-121">Flow will prompt you for the information that is required to connect to your [!INCLUDE[d365fin](includes/d365fin_md.md)] data.</span></span> <span data-ttu-id="c2f41-122">Wenn Sie eine der folgenden Trigger gewählt haben: *Wenn ein Datensatz erstellt wird*, *Wenn ein Datensatz geändert wird* oder *Wenn ein Datensatz gelöscht wird*, müssen Sie einen Namen und einen Tabellennamen auswählen.</span><span class="sxs-lookup"><span data-stu-id="c2f41-122">If you selected one of the following triggers: *When a record is created*, *When a record is modified*, or *When a record is deleted*, you must select a company name and table name.</span></span> <span data-ttu-id="c2f41-123">Mit jedem anderen Trigger wird nur der Name der Unternehmung benötigt, um zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="c2f41-123">With any other trigger, only the company name is required to connect.</span></span>

   <span data-ttu-id="c2f41-124">Flow zeigt eine Liste der Unternehmungen und Tabellen an, die in [!INCLUDE[d365fin](includes/d365fin_md.md)]verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c2f41-124">Flow will show a list of companies and tables that are available from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="c2f41-125">Diese Tabellen oder Endpunkte stehen für alle Webdienste, die Sie von [!INCLUDE[d365fin](includes/d365fin_md.md)] veröffentlicht haben.</span><span class="sxs-lookup"><span data-stu-id="c2f41-125">These tables, or end points, represent all the web services that you have published from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

   <span data-ttu-id="c2f41-126">Sie können einen neuen Webdienst URL in [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellen, indem Sie die **Erstellen Dataset** Aktion der Seite **Webdienste** nutzen, indem Sie die unterstütze Hilfe **Bericht einrichten** verwenden oder die Aktion **Bearbeiten in Excel** in einer beliebigen Liste wählen.</span><span class="sxs-lookup"><span data-stu-id="c2f41-126">Alternatively, create a new web service URL in [!INCLUDE[d365fin](includes/d365fin_md.md)] by using the **Create Data Set** action in the **Web Services** page, using the **Set Up Reporting** Assisted Setup guide, or by choosing the **Edit in Excel** action in any lists.</span></span>

<span data-ttu-id="c2f41-127">Zu diesem Zeitpunkt haben Sie erfolgreich Ihre Finance and Operations, Business edition-Daten verbunden und sind bereit, Ihren Flow zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c2f41-127">At this point, you have successfully connected to your Finance and Operations, Business edition data and are ready to begin building your flow.</span></span> <span data-ttu-id="c2f41-128">Weitere Informationen finden Sie in der [Flow Dokumentation](https://flow.microsoft.com/documentation/getting-started/).</span><span class="sxs-lookup"><span data-stu-id="c2f41-128">For more information, see the [Flow documentation](https://flow.microsoft.com/documentation/getting-started/).</span></span>

<span data-ttu-id="c2f41-129">Bei Problemen mit Microsoft Flow siehe [Problembehandlung Integration mit Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="c2f41-129">For troubleshooting your Microsoft Flow, see [Troubleshooting Integration with Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c2f41-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2f41-130">See Also</span></span>
<span data-ttu-id="c2f41-131">[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="c2f41-131">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="c2f41-132">Geschäftsdaten aus anderen Finanzsystemen importieren</span><span class="sxs-lookup"><span data-stu-id="c2f41-132">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="c2f41-133">[Benutzer und ihre Berechtigungen verwalten.](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="c2f41-133">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="c2f41-134">[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="c2f41-134">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="c2f41-135">Finanzen</span><span class="sxs-lookup"><span data-stu-id="c2f41-135">Finance</span></span>](finance.md)  

