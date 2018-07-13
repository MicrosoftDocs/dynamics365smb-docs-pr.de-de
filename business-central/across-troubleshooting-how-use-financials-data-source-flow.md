---
title: Problembehandlung Integration mit Microsoft Flow| Microsoft Docs
description: "Problemlösung beim Bereitstellen von Business Central als Datenquelle und eine OData-URL Ihrer Webdienste festlegen, um eine Geschäfts-App mithilfe einem automatisierten Workflow zu erstellen."
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: e3917573a912a4e51416c4e926443c87513728fe
ms.openlocfilehash: 80bc35f6ea8c4264c2cd8960be3370e5966b88e3
ms.contentlocale: de-de
ms.lasthandoff: 06/01/2018

---
# <a name="troubleshooting-integration-with-microsoft-flow---request-url-too-long"></a><span data-ttu-id="383c5-103">Problembehandlung bei der Integration mit Microsoft Flow - angeforderte URL zu lang</span><span class="sxs-lookup"><span data-stu-id="383c5-103">Troubleshooting Integration with Microsoft Flow - Request URL Too Long</span></span>
<span data-ttu-id="383c5-104">Sie können die Daten in [!INCLUDE[d365fin](includes/d365fin_md.md)] als Teil eines Workflows in Microsoft Flow verwenden.</span><span class="sxs-lookup"><span data-stu-id="383c5-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="383c5-105">Sie müssen ein gültiges Konto mit [!INCLUDE[d365fin](includes/d365fin_md.md)] und Flow haben.</span><span class="sxs-lookup"><span data-stu-id="383c5-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

<span data-ttu-id="383c5-106">Wenn Sie einen Microsoft Flow mithilfe des [!INCLUDE[d365fin](includes/d365fin_md.md)] Connectors erstellen, erhalten Sie möglicherweise eine Fehlermeldung, dass die angeforderte URL zu lang ist, nachdem der Flow erstellt wurde, wie beispielsweise **RequestUriTooLong**.</span><span class="sxs-lookup"><span data-stu-id="383c5-106">If you are creating a Microsoft Flow using the [!INCLUDE[d365fin](includes/d365fin_md.md)] connector, you may receive an error message stating that the requsted URL is too long after creating the flow, such as the following: **RequestUriTooLong**.</span></span>

## <a name="cause"></a><span data-ttu-id="383c5-107">Grund</span><span class="sxs-lookup"><span data-stu-id="383c5-107">Cause</span></span>
<span data-ttu-id="383c5-108">Um einen Flow auszulösen, sucht er Änderungen in Ihren Daten.</span><span class="sxs-lookup"><span data-stu-id="383c5-108">For a flow to trigger, it looks for changes in your data.</span></span> <span data-ttu-id="383c5-109">Bei der Festlegung, ob sich Ihre Daten verändert haben, vergleichen die Connectors die zwischengespeicherten Daten mit den neuen Daten, die von der Quelle angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="383c5-109">When determining if your data has changed, the connectors compare the cached data to the new data requested from the source.</span></span>  

<span data-ttu-id="383c5-110">Wenn die Datenenanforderung eine URL erstellt, die zu lang, schlägt sie fehl.</span><span class="sxs-lookup"><span data-stu-id="383c5-110">If the data request creates a URL that is too long, it will fail.</span></span> <span data-ttu-id="383c5-111">Gemeinsame Ursachen können sein:</span><span class="sxs-lookup"><span data-stu-id="383c5-111">Common causes may include:</span></span>
- <span data-ttu-id="383c5-112">Grundsätzlich jede Quelltabelle mit über 250 Zeilen</span><span class="sxs-lookup"><span data-stu-id="383c5-112">Generally, any source table with over 250 rows</span></span>
- <span data-ttu-id="383c5-113">Quelltabellen, die mehrere Tausend Datensätze enthalten</span><span class="sxs-lookup"><span data-stu-id="383c5-113">Source tables containing multiple thousands of records</span></span>

## <a name="workaround"></a><span data-ttu-id="383c5-114">Problemumgehung</span><span class="sxs-lookup"><span data-stu-id="383c5-114">Workaround</span></span>
<span data-ttu-id="383c5-115">Folgen Sie diesen Schritten als Problemumgehung.</span><span class="sxs-lookup"><span data-stu-id="383c5-115">Follow these steps as a workaround.</span></span>
1. <span data-ttu-id="383c5-116">Bearbeiten Sie den Flow, der fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="383c5-116">Choose to edit the flow that is failing.</span></span>
2. <span data-ttu-id="383c5-117">Erweitern Sie **Zeigen Sie erweiterte Optionen an** im Flowauslöser.</span><span class="sxs-lookup"><span data-stu-id="383c5-117">Expand the **Show advanced options** on the flow trigger.</span></span>
3. <span data-ttu-id="383c5-118">Geben Sie im Feld **Zählung überspringen** die Anzahl Datensätze ein, die übersprungen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="383c5-118">In the **Skip Count** field, enter the number of records to skip.</span></span>  
<span data-ttu-id="383c5-119">Wenn die Tabelle beispielsweise, die Sie als Datenquelle verwenden, 4.000 Datensätze hat, geben Sie 4.000 als die Anzahl der Datensätze ein, die übersprungen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="383c5-119">For example, if the table that you are using as a data source has 4,000 records, enter 4,000 as the number of records to skip.</span></span>
4. <span data-ttu-id="383c5-120">Aktualisieren Sie den Flow.</span><span class="sxs-lookup"><span data-stu-id="383c5-120">Update your flow.</span></span>

> [!NOTE]  
> <span data-ttu-id="383c5-121">Der Connector ist derzeit in Beta-Vesion.</span><span class="sxs-lookup"><span data-stu-id="383c5-121">The connector is currently in Beta.</span></span> <span data-ttu-id="383c5-122">Aktualisierungen, wie Datenänderungen behandelt werden, sind für eine spätere Freigabe geplant.</span><span class="sxs-lookup"><span data-stu-id="383c5-122">Updates to how data changes are targeted for a future release.</span></span>


## <a name="see-also"></a><span data-ttu-id="383c5-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="383c5-123">See Also</span></span>
<span data-ttu-id="383c5-124">[Nutzung von [!INCLUDE[d365fin](includes/d365fin_md.md)] in einem automatisierten Workflow](across-how-use-financials-data-source-flow.md)</span><span class="sxs-lookup"><span data-stu-id="383c5-124">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow](across-how-use-financials-data-source-flow.md)</span></span>  
[<span data-ttu-id="383c5-125">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="383c5-125">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="383c5-126">Geschäftsdaten aus anderen Finanzsystemen importieren</span><span class="sxs-lookup"><span data-stu-id="383c5-126">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="383c5-127">[Benutzer und ihre Berechtigungen verwalten.](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="383c5-127">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="383c5-128">[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="383c5-128">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="383c5-129">Finanzen</span><span class="sxs-lookup"><span data-stu-id="383c5-129">Finance</span></span>](finance.md)  

