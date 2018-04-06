---
title: 'Vorgehensweise: Konfigurieren neuer Unternehmen per Cmdlet | Microsoft Docs'
description: "In einigen Szenarien können Sie ein Konfigurationspaket laden und importieren, ohne Ihre Benutzer mit einzubeziehen oder die RapidStart Services-Benutzeroberfläche zu verwenden. Dies können Sie tun, indem Sie ein Windows PowerShell cmdlet  verwenden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 8b91c3b91e07f5ad96dcfc65152062054fc13c01
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="configure-new-companies-using-a-cmdlet"></a><span data-ttu-id="876d5-104">Vorgehensweise: Konfigurieren neuer Unternehmen per Cmdlet</span><span class="sxs-lookup"><span data-stu-id="876d5-104">Configure New Companies using a Cmdlet</span></span>
<span data-ttu-id="876d5-105">In einigen Szenarien können Sie ein Konfigurationspaket laden und importieren, ohne Ihre Benutzer mit einzubeziehen oder die RapidStart Services-Benutzeroberfläche zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="876d5-105">In a number of scenarios, you may want to load and import a configuration package without involving your users or using the RapidStart Services user interface.</span></span> <span data-ttu-id="876d5-106">Dies können Sie tun, indem Sie ein Windows PowerShell cmdlet  verwenden.</span><span class="sxs-lookup"><span data-stu-id="876d5-106">You can do so by using a Windows PowerShell cmdlet.</span></span> <span data-ttu-id="876d5-107">Szenarien, in denen dies hilfreich sein kann, sind etwa:</span><span class="sxs-lookup"><span data-stu-id="876d5-107">Scenarios where this may be useful include:</span></span>  

- <span data-ttu-id="876d5-108">Ausführen des Dateniports in mehre  [!INCLUDE[d365fin](includes/d365fin_md.md)] Installationsarbeiten.</span><span class="sxs-lookup"><span data-stu-id="876d5-108">Performing data import across multiple [!INCLUDE[d365fin](includes/d365fin_md.md)] installations.</span></span>
- <span data-ttu-id="876d5-109">Konfigurieren von zusätzlichen Anwendungsbereichen für mehrere Kunden.</span><span class="sxs-lookup"><span data-stu-id="876d5-109">Configuring additional application areas for multiple customers.</span></span>  

## <a name="to-deploy-a-configuration-package-using-a-cmdlet"></a><span data-ttu-id="876d5-110">Ein Konfigurationspaket unter Verwendung eines Cmdlets bereitstellen</span><span class="sxs-lookup"><span data-stu-id="876d5-110">To deploy a configuration package using a cmdlet</span></span>  

1. <span data-ttu-id="876d5-111">Bereiten Sie ein RapidStart-Dienstepaket vor.</span><span class="sxs-lookup"><span data-stu-id="876d5-111">Prepare a RapidStart Services package.</span></span> <span data-ttu-id="876d5-112">Beispielsweise können Sie ein Paket erstellen, um bestimmte Werte und Namen der Tabelle und der Felder zu importieren und diese Werte einzufügen.</span><span class="sxs-lookup"><span data-stu-id="876d5-112">For example, you can create a package to import certain values and the names of the table and the fields to insert these values into.</span></span>  
2. <span data-ttu-id="876d5-113">Setzen Sie das Paket auf einen Computer, auf dem Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="876d5-113">Place the package on a computer where you will run the cmdlet.</span></span>  
3. <span data-ttu-id="876d5-114">[!INCLUDE[d365fin](includes/d365fin_md.md)] Verwaltungsshell öffnen.</span><span class="sxs-lookup"><span data-stu-id="876d5-114">Open the [!INCLUDE[d365fin](includes/d365fin_md.md)] administration shell.</span></span>  
4. <span data-ttu-id="876d5-115">Geben Sie **Invoke-NAVCodeUnit** ein, und geben Sie Daten wie im folgenden Beispiel an.</span><span class="sxs-lookup"><span data-stu-id="876d5-115">Enter **Invoke-NAVCodeUnit**, and specify information similar to the following example.</span></span>  
    ```  
    Invoke-NAVCodeunit -Tenant Default -CompanyName "CRONUS International Ltd." -CodeunitId 8620 -MethodName ImportRapidStartPackage -Argument "C:TEMPRS_CONFIG.rapidstart" -ServerInstance DynamicsNAV71  

    ```
<span data-ttu-id="876d5-116">Das Cmdlet importiert das Paket in jedes Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="876d5-116">The cmdlet imports the package into each company.</span></span> <span data-ttu-id="876d5-117">Benutzer können sofort beginnen, eine neue Funktionalität zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="876d5-117">Users can start to use the new functionality immediately.</span></span>  

## <a name="see-also"></a><span data-ttu-id="876d5-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="876d5-118">See Also</span></span>  
[<span data-ttu-id="876d5-119">So konfigurieren Sie einen neuen Mandanten.</span><span class="sxs-lookup"><span data-stu-id="876d5-119">Configure New Companies</span></span>](admin-how-to-configure-new-companies.md)  
[<span data-ttu-id="876d5-120">Übernehmen von Konfiguration in neue Mandanten</span><span class="sxs-lookup"><span data-stu-id="876d5-120">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="876d5-121">Einrichten von Mandanten mit RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="876d5-121">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="876d5-122">Verwaltung</span><span class="sxs-lookup"><span data-stu-id="876d5-122">Administration</span></span>](admin-setup-and-administration.md)  
[<span data-ttu-id="876d5-123">Microsoft Dynamics NAV Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="876d5-123">Microsoft Dynamics NAV Windows PowerShell Cmdlets</span></span>](/dynamics-nav/microsoft-dynamics-nav-windows-powershell-cmdlets)

