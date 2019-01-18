---
title: Invoicing und Business Central verwenden | Microsoft Docs
description: Problemumgehung zum Aufrufen von Microsoft Invoicing, wenn Sie sich auf Dynamics 365 Business Central
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 3e2357766d514f30e42869a4f10ede1e66a6fec1
ms.contentlocale: de-de
ms.lasthandoff: 11/26/2018

---
# <a name="using-the-same-office-365-account-in-included365finincludesd365finlongmdmd-and-microsoft-invoicing"></a><span data-ttu-id="ab9af-103">Mithilfe des gleichen Office 365 Kontos in [!INCLUDE[d365fin](includes/d365fin_long_md.md)] und Microsoft Invoicing</span><span class="sxs-lookup"><span data-stu-id="ab9af-103">Using the same Office 365 Account in [!INCLUDE[d365fin](includes/d365fin_long_md.md)] and Microsoft Invoicing</span></span>
<span data-ttu-id="ab9af-104">Wenn Sie sich für eine Testversion anmelden [!INCLUDE[d365fin](includes/d365fin_md.md)], können das Programm 30-Tage lang testen, Sie können ein Abonnement abschließen oder Sie können die Verwendung von [!INCLUDE[d365fin](includes/d365fin_md.md)] beenden.</span><span class="sxs-lookup"><span data-stu-id="ab9af-104">When you sign up for a trial with [!INCLUDE[d365fin](includes/d365fin_md.md)], you can move to a 30-day evaluation phase, you can start a subscription, or you can stop using [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="ab9af-105">In allen Fällen sehen Sie bei der Anmeldung in das Office-Portal eine Kachel **Geschäftszentrum** und klicken darauf.</span><span class="sxs-lookup"><span data-stu-id="ab9af-105">In all cases, if you log into the Office Portal, you might see a tile called **Business center** and click it.</span></span> <span data-ttu-id="ab9af-106">Dieses ist ein Teil des Office 365 Business Premium Abonnements, deshalb sieht nicht jeder die Kachel im Office-Portal.</span><span class="sxs-lookup"><span data-stu-id="ab9af-106">This is part of the Office 365 Business Premium subscription, so not everyone will see that tile in the Office Portal.</span></span>  

<span data-ttu-id="ab9af-107">Wenn Sie auf das Geschäftszentrum zugreifen, sehen Sie ein Abschnitt, der **Fakturierung** genannt wird.</span><span class="sxs-lookup"><span data-stu-id="ab9af-107">If you do access the Business center, you will see a section called **Invoicing**.</span></span> <span data-ttu-id="ab9af-108">Wenn Sie auf diesen Abschnitt zugreifen, sehen Sie eine Meldung, dass Sie nicht auf Microsoft Invoicing zugreifen können, da Ihr Konto verwendet wird in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ab9af-108">If you access that section, you will see a message that you cannot access Microsoft Invoicing because your account is used in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="ab9af-109">Sie sehen eine ähnliche Meldung, wenn Sie die mobile App für die Fakturierung einrichten.</span><span class="sxs-lookup"><span data-stu-id="ab9af-109">You see a similar message if you install the mobile app for Invoicing.</span></span>  

## <a name="workaround"></a><span data-ttu-id="ab9af-110">Problemumgehung</span><span class="sxs-lookup"><span data-stu-id="ab9af-110">Workaround</span></span>
<span data-ttu-id="ab9af-111">Invoicing und [!INCLUDE[d365fin](includes/d365fin_md.md)] haben eine freigegebene Plattform.</span><span class="sxs-lookup"><span data-stu-id="ab9af-111">Invoicing and [!INCLUDE[d365fin](includes/d365fin_md.md)] have a shared platform.</span></span> <span data-ttu-id="ab9af-112">Das bedeutet, dass Sie als bestehender Benutzer von [!INCLUDE[d365fin](includes/d365fin_md.md)] erkannt werden, wenn Sie auf Rechnungsstellung im Geschäftszentrum klicken.</span><span class="sxs-lookup"><span data-stu-id="ab9af-112">That means that you are recognized as an existing user of [!INCLUDE[d365fin](includes/d365fin_md.md)] when you click Invoicing in the Business center.</span></span> <span data-ttu-id="ab9af-113">Der Grund ist, dass das Invoicing nicht das gleiche Unternehmen als [!INCLUDE[d365fin](includes/d365fin_md.md)] verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="ab9af-113">The reason is that Invoicing cannot use the same company as [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="ab9af-114">Daher müssen Sie sich bei [!INCLUDE[d365fin](includes/d365fin_md.md)] anmelden und Ihr bestehendes Unternehmen umbenennen und dann ein neues Unternehmen erstellen, dass Sie dann in Invoicing verwenden können.</span><span class="sxs-lookup"><span data-stu-id="ab9af-114">So you will have to log into [!INCLUDE[d365fin](includes/d365fin_md.md)] and rename your existing company, and then create a new company that you can then use in Invoicing.</span></span> <span data-ttu-id="ab9af-115">Keine Daten werden bei dieser Problemumgehung überschrieben oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="ab9af-115">No data is moved or overwritten during this workaround.</span></span>

### <a name="to-rename-your-company"></a><span data-ttu-id="ab9af-116">Ihr Unternehmen umbenennen</span><span class="sxs-lookup"><span data-stu-id="ab9af-116">To rename your company</span></span>
1.  <span data-ttu-id="ab9af-117">Anmelden bei [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ab9af-117">Sign in to your [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
2.  <span data-ttu-id="ab9af-118">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Unternehmen** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="ab9af-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Companies**, and then choose the related link.</span></span>  
3.  <span data-ttu-id="ab9af-119">Im Fenster **Unternehmen** wählen Sie die Schaltfläche **Liste bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="ab9af-119">On the **Companies** page, choose the **Edit List** button.</span></span>  
4.  <span data-ttu-id="ab9af-120">Ändern den Namen des Postens *Mein Unternehmen* in etwas anderes.</span><span class="sxs-lookup"><span data-stu-id="ab9af-120">Change the name of the *My Company* entry to something else.</span></span>  

    <span data-ttu-id="ab9af-121">Warten Sie mehrere Minuten.</span><span class="sxs-lookup"><span data-stu-id="ab9af-121">Wait a number of minutes.</span></span> <span data-ttu-id="ab9af-122">Wir machen einige Änderungen in der zugrunde liegenden Datenbank und das kann eine Weile dauern.</span><span class="sxs-lookup"><span data-stu-id="ab9af-122">We’ll be making a number of changes in the underlying database, and that takes a while.</span></span>
5.  <span data-ttu-id="ab9af-123">Wenn die Anwendung wieder bereit steht, wählen Sie die Schaltfläche **Neues Unternehmen erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="ab9af-123">When the system is ready again, choose the **Create New Company** button.</span></span>  
6.  <span data-ttu-id="ab9af-124">Im Dialogfeld, das erscheint, geben Sie den Namen als *Mein Unternehmen* an, und wählen Sie die Option **Suiten-Produktion – nur Einrichtungsdaten** aus.</span><span class="sxs-lookup"><span data-stu-id="ab9af-124">In the dialog that appears, specify the name as *My Company*, and choose the **Production – Setup Data Only** option.</span></span>  

<span data-ttu-id="ab9af-125">Dies kann wieder mehrere Minuten dauern.</span><span class="sxs-lookup"><span data-stu-id="ab9af-125">This again takes a number of minutes.</span></span> <span data-ttu-id="ab9af-126">Wenn der Vorgang abgeschlossen ist, sind Sie in der Lage, auf Invoicing als Teil IhrerOffice 365 Business Premium Erfahrung zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="ab9af-126">When the process completes, you will be able to access Invoicing as part of your Office 365 Business Premium experience.</span></span>  

### <a name="what-about-my-data"></a><span data-ttu-id="ab9af-127">Informationen zu Ihren Daten.</span><span class="sxs-lookup"><span data-stu-id="ab9af-127">What about my data?</span></span>
<span data-ttu-id="ab9af-128">Wenn Sie die Vorlage Meine Mandanten umbenennen auswählen, werden die Datenbanktabellen, die Ihre bestehenden [!INCLUDE[d365fin](includes/d365fin_md.md)] Daten speichern, umbenennte, aber die Daten selber werden nicht berührt</span><span class="sxs-lookup"><span data-stu-id="ab9af-128">When you rename the original My Company, the database tables that store your existing [!INCLUDE[d365fin](includes/d365fin_md.md)] data are renamed, but the data itself is not touched.</span></span>  

<span data-ttu-id="ab9af-129">Wenn Sie "Invoicing" und [!INCLUDE[d365fin](includes/d365fin_md.md)] verwenden, werden die Daten in zwei verschiedenen Containern gespeichert (die zwei Unternehmen).</span><span class="sxs-lookup"><span data-stu-id="ab9af-129">If you use both Invoicing and [!INCLUDE[d365fin](includes/d365fin_md.md)], the data is stored in two different containers (the two companies).</span></span> <span data-ttu-id="ab9af-130">Nichts wird freigegebent, daher müssen Sie Debitoren und Artikel in beiden Unternehmen verwalten.</span><span class="sxs-lookup"><span data-stu-id="ab9af-130">Nothing is shared, so you'll have to manage customers and items in both companies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ab9af-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab9af-131">See Also</span></span>
[<span data-ttu-id="ab9af-132">Häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="ab9af-132">Frequently Asked Questions</span></span>](across-faq.md)  
[<span data-ttu-id="ab9af-133">Verwaltung</span><span class="sxs-lookup"><span data-stu-id="ab9af-133">Administration</span></span>](admin-setup-and-administration.md)  

