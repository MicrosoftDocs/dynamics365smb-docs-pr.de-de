---
title: Buchhalter-Portal nutzen| Microsoft Docs
description: "Enthält Informationen über die  Buchhalter-Portalserweiterung."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, accountant
ms.date: 09/05/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 84b2331f14b8c7e8d73921189e2df33fa709626e
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="accountant-portal-for-dynamics-365-for-financials"></a><span data-ttu-id="4e9c5-103">Accountant Hub für Dynamics 365 for Financials.</span><span class="sxs-lookup"><span data-stu-id="4e9c5-103">Accountant Portal for Dynamics 365 for Financials</span></span>
<span data-ttu-id="4e9c5-104">Diese Anwendung bietet ein Portal mit Zusammenfassungsdaten für jeden Client eines Buchhalters.</span><span class="sxs-lookup"><span data-stu-id="4e9c5-104">This application provides a dashboard with summary data for each client of an accountant.</span></span> <span data-ttu-id="4e9c5-105">Das Portal zeigt Finanz-KPIs sowie eine direkte Verknüpfung der Finanz-Anwendung des Clients an.</span><span class="sxs-lookup"><span data-stu-id="4e9c5-105">The portal displays financial KPIs as well as a direct link to the client’s financial application.</span></span>  

<span data-ttu-id="4e9c5-106">Das Portal umfasst ein spezialisiertes Rollencenter, das als Dashboard für einen besseren Überblick über Ihre Clients dient.</span><span class="sxs-lookup"><span data-stu-id="4e9c5-106">The dashboard is a highly specialized Role Center for a better overview of your clients.</span></span>  
<span data-ttu-id="4e9c5-107">[![Buchhaltungsportal](./media/ui-extensions-accportal/accountant-portal.png)](https://go.microsoft.com/fwlink/?linkid=851257)</span><span class="sxs-lookup"><span data-stu-id="4e9c5-107">[![Accountant Portal](./media/ui-extensions-accportal/accountant-portal.png)](https://go.microsoft.com/fwlink/?linkid=851257)</span></span>

<span data-ttu-id="4e9c5-108">Wenn Sie zuerst die Erweiterung einrichten, hilft ein Beispielmandant Ihnen dabei.</span><span class="sxs-lookup"><span data-stu-id="4e9c5-108">When you first install the extension, a sample company helps you get started.</span></span> <span data-ttu-id="4e9c5-109">Sie können den Beispielmandanten jederzeit löschen.</span><span class="sxs-lookup"><span data-stu-id="4e9c5-109">You can delete the sample company at any time.</span></span>  

## <a name="installing-the-extension"></a><span data-ttu-id="4e9c5-110">Erweiterung wird installiert</span><span class="sxs-lookup"><span data-stu-id="4e9c5-110">Installing the Extension</span></span>
<span data-ttu-id="4e9c5-111">Wenn Sie die Erweiterung in Ihrem [!INCLUDE[d365fin](includes/d365fin_md.md)] einrichten, werden Sie gefragt, ob Sie es jetzt verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="4e9c5-111">When you install the extension in your [!INCLUDE[d365fin](includes/d365fin_md.md)], you will be asked if you want to use it now.</span></span> <span data-ttu-id="4e9c5-112">Wenn Sie dies tun, müssen Sie sich abmelden und wieder anmelden, da die Erweiterung Ihr aktuelles Rollencenter ersetzt und Berechtigungen Ihrem Benutzerprofil hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="4e9c5-112">If you do, then you must sign out and sign in again, because the extension replaces your current Role Center and adds permissions to your user profile.</span></span>  

<span data-ttu-id="4e9c5-113">Weitere Informationen finden Sie unter [Buchhaltungs-Erfahrung in Dynamics 365 for Financials](finance-accounting.md).</span><span class="sxs-lookup"><span data-stu-id="4e9c5-113">For more information, see [Accountant Experiences in Dynamics 365 for Financials](finance-accounting.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="4e9c5-114">Die aktuelle Version der Erweiterung erfordert,  dass Ihre Client nutzt. [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="4e9c5-114">The current version of the extension requires that your clients use [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="using-the-extension"></a><span data-ttu-id="4e9c5-115">Erweiterung nutzen</span><span class="sxs-lookup"><span data-stu-id="4e9c5-115">Using the extension</span></span>
<span data-ttu-id="4e9c5-116">Diese Erweiterung wird verwendet, wenn Sie sich an anmeldencro bei [Financials for Accountants bei Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants). Wenn Sie die Erweiterung in Ihrem [!INCLUDE[d365fin](includes/d365fin_md.md)] eirnichten, ersetzt das Ihr aktuelles Rollencenter.</span><span class="sxs-lookup"><span data-stu-id="4e9c5-116">This extension is used when you sign up at [Financials for Accountants on Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants). If you install the extension in your [!INCLUDE[d365fin](includes/d365fin_md.md)], it will replace your current Role Center.</span></span> <span data-ttu-id="4e9c5-117">Wenn Sie dann zum anderen Rollencenter zurückkehren möchten, dann können Sie das in " Meine Einstellungen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="4e9c5-117">If you then want to return to the other Role Center, then you can do that in My Settings.</span></span> <span data-ttu-id="4e9c5-118">Weitere Informationen finden Sie unter [Vorgehensweise: Rollencenter ändern](change-role.md).</span><span class="sxs-lookup"><span data-stu-id="4e9c5-118">For more information, see [How to: Change the Role Center](change-role.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="4e9c5-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e9c5-119">See Also</span></span>
[<span data-ttu-id="4e9c5-120">Buchhalter Experiences in Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="4e9c5-120">Accountant Experiences in Dynamics 365 for Financials</span></span>](finance-accounting.md)  
[<span data-ttu-id="4e9c5-121">Finanzen</span><span class="sxs-lookup"><span data-stu-id="4e9c5-121">Finance</span></span>](finance.md)  

