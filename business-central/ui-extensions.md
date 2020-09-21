---
title: Erweiterungen installieren um Business Central anzupassen | Microsoft Docs
description: Informationen zum Hinzufügen von Funktionalität und Anpassungen für Business Central durch die Installation von Erweiterungen.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 08/12/2020
ms.author: edupont
ms.openlocfilehash: 2011728e8e036442418c6a2d8b51477b45b02d1e
ms.sourcegitcommit: 43284728c34b72ad1984a516273dc80e4cdc99ab
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/04/2020
ms.locfileid: "3765921"
---
# <a name="customizing-business-central-using-extensions"></a><span data-ttu-id="cb24b-103">Anpassen von Business Central mithilfe der Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="cb24b-103">Customizing Business Central Using Extensions</span></span>

<span data-ttu-id="cb24b-104">Sie können [!INCLUDE[d365fin](includes/d365fin_md.md)] ändern, indem Sie beispielsweise Erweiterungen installieren, die Funktionalität hinzufügen, das Verhalten ändern oder Zugriff auf die neuen Onlinediensten geben.</span><span class="sxs-lookup"><span data-stu-id="cb24b-104">You can change [!INCLUDE[d365fin](includes/d365fin_md.md)] by installing extensions that add functionality, changes behavior, or gives you access to new online services, for example.</span></span>

> [!NOTE]
> <span data-ttu-id="cb24b-105">Um Erweiterungen von AppSource zu installieren oder Erweiterungen pro Mandanten hinzuzufügen, müssen Sie über die richtigen Berechtigungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="cb24b-105">To install extensions from AppSource or add per-tenant extensions, you must have the right permissions.</span></span> <span data-ttu-id="cb24b-106">Sie müssen entweder Mitglied der Benutzergruppe D365 EXTENSION MGMT sein oder über den Berechtigungssatz D365 EXTENSION MGMT verfügen.</span><span class="sxs-lookup"><span data-stu-id="cb24b-106">You must either be a member of the D365 EXTENSION MGMT user group or you must have the D365 EXTENSION MGMT permission set.</span></span> <span data-ttu-id="cb24b-107">Als Administrator können Sie anderen Benutzern in Ihrem Unternehmen Benutzergruppen und Berechtigungen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="cb24b-107">If you are an administrator, you can assign user groups and permissions to other users in your company.</span></span><br /><br />
<span data-ttu-id="cb24b-108">Um die Funktionen einer Erweiterung nutzen zu können, z. B. Seiten öffnen, Berichte ausführen, Aktionen auswählen usw., müssen Sie den Berechtigungssätzen zugewiesen sein, die als Teil der Erweiterung installiert werden.</span><span class="sxs-lookup"><span data-stu-id="cb24b-108">To use the functionality that is provided by an extension, such as opening pages, running reports, selecting actions, and so on, you must be assigned the permission sets that are installed as part of the extension.</span></span>

> [!IMPORTANT]  
> <span data-ttu-id="cb24b-109">Das Hochladen von Tenant-Erweiterungen und die Installation von AppSource-Erweiterungen werden über die Seite **Erweiterungsverwaltung** für lokale Installationen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cb24b-109">The upload of per-tenant extensions and the installation of AppSource extensions is not supported through the **Extension Management** page for on-premise installations.</span></span>

<span data-ttu-id="cb24b-110">Wenn Sie das [!INCLUDE[d365fin](includes/d365fin_md.md)] zuerst starten, werden bestimmte Erweiterungen bereits eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="cb24b-110">When you first launch [!INCLUDE[d365fin](includes/d365fin_md.md)], some extensions are already installed for you.</span></span> <span data-ttu-id="cb24b-111">Im Zeitverlauf werden mehr Erweiterungen für Sie zugänglich und Sie können auswählen, ob Sie die Erweiterung verwenden möchten oder nicht.</span><span class="sxs-lookup"><span data-stu-id="cb24b-111">Over time, more extensions will be made available to you, and you can then choose if you want to use the extension or not.</span></span>

<span data-ttu-id="cb24b-112">Beispielsweise bietet Microsoft eine Erweiterung an, die die Integration mit PayPal Payments Standard ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="cb24b-112">For example, Microsoft provides an extension that provides integration with PayPal Payments Standard.</span></span> <span data-ttu-id="cb24b-113">Diese Erweiterung wird standardmäßig eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="cb24b-113">This extension is installed by default.</span></span>
<span data-ttu-id="cb24b-114">Wenn aber keine andere Erweiterung bereitgestellt wird, die die Integration mit einem anderen Zahlungsservice anbietet, können Sie die neue Erweiterung einrichten und dann auswählen, welcher der beiden Services verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cb24b-114">But if another extension is made available that offers integration with another payment service, you can install the new extension and then choose which of the two services to use.</span></span>  

<span data-ttu-id="cb24b-115">Sie verwalten die Erweiterung auf der **Erweiterungs-Verwaltungs**-Seite.</span><span class="sxs-lookup"><span data-stu-id="cb24b-115">You manage the extensions on the **Extension Management** page.</span></span> <span data-ttu-id="cb24b-116">Sie können vom Startbildschirm auf diese Seite zugreifen.</span><span class="sxs-lookup"><span data-stu-id="cb24b-116">You can access this page from Home.</span></span> <span data-ttu-id="cb24b-117">Wählen Sie alternativ das Symbol **Nach Seite oder Bericht suchen** aus ![Glühlampe, mit der die Funktion „Sie wünschen“ geöffnet wird](media/ui-search/search_small.png "Was möchten Sie tun?") in der oberen rechter Ecke, geben Sie **Erweiterung** ein, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="cb24b-117">Alternatively, choose the **Search for Page or Report** icon ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") in the top right corner, enter **Extension**, and then choose the related link.</span></span> <span data-ttu-id="cb24b-118">Weitere Informationen finden Sie unter [Installieren und Deinstallieren von Erweiterungen](ui-extensions-install-uninstall.md).</span><span class="sxs-lookup"><span data-stu-id="cb24b-118">For more information, see [Installing and Uninstalling Extensions](ui-extensions-install-uninstall.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="cb24b-119">Wenn Sie der Meinung sind, Sie sollten Zugriff zu einer Erweiterung haben, können die Funktionalität aber nicht finden, überprüfen Sie die Seite **Erweiterungsverwaltung**, wenn die Erweiterung dort nicht aufgeführt wird, können Sie sie einrichten, wie im folgenden Abschnitt erläutert.</span><span class="sxs-lookup"><span data-stu-id="cb24b-119">If you think you should have access to an extension but you cannot find its functionality, check the **Extension Management** page - if the extension is not listed there, you can install it as described in the following section.</span></span>  

> [!NOTE]  
> <span data-ttu-id="cb24b-120">Neue Erweiterungen sind nicht direkt in AppSource verfügbar, nachdem ein Update angekündigt wurde.</span><span class="sxs-lookup"><span data-stu-id="cb24b-120">New extensions are not available in AppSource immediately after we announce an update.</span></span> <span data-ttu-id="cb24b-121">Halten Sie unter [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646) Ausschau nach den Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="cb24b-121">You can keep an eye out for the extensions at  [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).</span></span>

## <a name="see-also"></a><span data-ttu-id="cb24b-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb24b-122">See Also</span></span>

[<span data-ttu-id="cb24b-123">Erweitern von Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="cb24b-123">Extending Dynamics 365 Business Central</span></span>](about-develop-extensions.md)  
[<span data-ttu-id="cb24b-124">Business Central-Erweiterungen von anderen Anbietern</span><span class="sxs-lookup"><span data-stu-id="cb24b-124">Business Central Extensions by Other Providers</span></span>](ui-extensions-other.md)  
[<span data-ttu-id="cb24b-125">Den Envestnet Yodlee Bank Feeds Service einrichten</span><span class="sxs-lookup"><span data-stu-id="cb24b-125">Set Up the Envestnet Yodlee Bank Feeds Service</span></span>](bank-how-setup-bank-statement-service.md)  
[<span data-ttu-id="cb24b-126">Aktivieren von Debitoren-Zahlungen durch Paypal</span><span class="sxs-lookup"><span data-stu-id="cb24b-126">Enable Customer Payment Through PayPal</span></span>](sales-how-enable-payment-service-extensions.md)  
[<span data-ttu-id="cb24b-127">Geschäftsdaten aus anderen Finanzsystemen migrieren</span><span class="sxs-lookup"><span data-stu-id="cb24b-127">Migrating Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="cb24b-128">Einrichten der britischen Postleitzahlerweiterung GetAddress.io</span><span class="sxs-lookup"><span data-stu-id="cb24b-128">Setting Up the GetAddress.io UK Postal Code extension</span></span>](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
<span data-ttu-id="cb24b-129">[[!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen für andere Anbieter](ui-extensions-other.md)</span><span class="sxs-lookup"><span data-stu-id="cb24b-129">[[!INCLUDE[d365fin](includes/d365fin_md.md)] Extensions by Other Providers](ui-extensions-other.md)</span></span>  
[<span data-ttu-id="cb24b-130">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="cb24b-130">Getting Started</span></span>](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
