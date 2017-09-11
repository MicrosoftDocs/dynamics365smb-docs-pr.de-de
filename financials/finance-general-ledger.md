---
title: Erhalten von Informationen zu Finanzbuchhaltung und COA| Microsoft Docs
description: Beschreibt die Finanzbuchhaltung, den Kontenplan und die Kontokategorien.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 06becfd7e54803fea925e8364719576bef0a8bab
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2017

---
# <a name="understanding-the-general-ledger-and-the-coa"></a><span data-ttu-id="33fd0-103">Verständnis der Fibu und des COA</span><span class="sxs-lookup"><span data-stu-id="33fd0-103">Understanding the General Ledger and the COA</span></span>
<span data-ttu-id="33fd0-104">Die Finanzbuchhaltung speichert Ihre Finanzdaten, und der Kontenplan zeigt die Konten, auf die alle Sachposten gebucht werden, an.</span><span class="sxs-lookup"><span data-stu-id="33fd0-104">The general ledger stores your financial data, and the chart of accounts shows the accounts that all general ledger entries are posted to.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="33fd0-105"> umfasst einen Standardkontenplan, der zur Unterstützung Ihres Unternehmens bereit steht.</span><span class="sxs-lookup"><span data-stu-id="33fd0-105"> includes a standard chart of accounts that is ready to support your business.</span></span>

## <a name="general-ledger-setup-and-general-posting-setup"></a><span data-ttu-id="33fd0-106">Finanzbuchhaltung Einrichtung und Buchungsmatrix Einrichtung</span><span class="sxs-lookup"><span data-stu-id="33fd0-106">General Ledger Setup and General Posting Setup</span></span>
<span data-ttu-id="33fd0-107">Die Einrichtung der Finanzbuchhaltung ist das Kernstück der Finanzvorgängen, da sie definieren, wie Sie Daten buchen.</span><span class="sxs-lookup"><span data-stu-id="33fd0-107">The setup of the general ledger is at the core of financial processes because it defines how you post data.</span></span>  

<span data-ttu-id="33fd0-108">Im Fenster **Finanzbuchhaltung einrichten** geben Sie an, wie bestimmte finanzbuchhalterische Sachverhalte in Ihrem Unternehmen gehandhabt werden sollen, wie beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="33fd0-108">In the **General Ledger Setup** window, you specify how to handle certain accounting issues in your company, such as:</span></span>  

* <span data-ttu-id="33fd0-109">Rechnungsrundungskontodetails</span><span class="sxs-lookup"><span data-stu-id="33fd0-109">Invoice rounding details</span></span>  
* <span data-ttu-id="33fd0-110">Adressformate</span><span class="sxs-lookup"><span data-stu-id="33fd0-110">Address formats</span></span>  
* <span data-ttu-id="33fd0-111">Finanzberichterstellung</span><span class="sxs-lookup"><span data-stu-id="33fd0-111">Financial reporting</span></span>  

<span data-ttu-id="33fd0-112">Ebenso geben Sie im Fenster **Buchungsmatrix Einrichtung** an, wie Sie Kombinationen aus Geschäftsbuchungsgruppen und Produktbuchungsgruppen einrichten wollen.</span><span class="sxs-lookup"><span data-stu-id="33fd0-112">Similarly, in the **General Posting Setup** window, you specify how you want to set up combinations of general business and general product posting groups.</span></span> <span data-ttu-id="33fd0-113">Buchungsgruppenzuordnungseinheiten nach Debitoren, Kreditoren, Artikel, Ressourcen und Einkaufs- und Verkaufsbelegen mit Sachkonten.</span><span class="sxs-lookup"><span data-stu-id="33fd0-113">Posting groups map entities like customers, vendors, items, resources, and sales and purchase documents to general ledger accounts.</span></span> <span data-ttu-id="33fd0-114">Für jede Kombination aus Geschäftsbuchungsgruppe und Produktbuchungsgruppe geben Sie eine Zeile ein.</span><span class="sxs-lookup"><span data-stu-id="33fd0-114">You fill in a line for each combination of business posting group and product posting group.</span></span> <span data-ttu-id="33fd0-115">Weitere Informationen finden Sie unter [Einrichten von Gruppenbuchungen](finance-posting-groups.md)</span><span class="sxs-lookup"><span data-stu-id="33fd0-115">For more information, see [Posting Group Setups](finance-posting-groups.md)</span></span>  

## <a name="the-chart-of-accounts"></a><span data-ttu-id="33fd0-116">Kontenplan</span><span class="sxs-lookup"><span data-stu-id="33fd0-116">The Chart of Accounts</span></span>
<span data-ttu-id="33fd0-117">Der Kontenplan zeigt alle Sachkonten an.</span><span class="sxs-lookup"><span data-stu-id="33fd0-117">The chart of accounts shows all general ledger accounts.</span></span> <span data-ttu-id="33fd0-118">Vom Kontenplan aus können Sie Dinge tun wie:</span><span class="sxs-lookup"><span data-stu-id="33fd0-118">From the chart of accounts, you can do things like:</span></span>  

* <span data-ttu-id="33fd0-119">Berichte ansehen, die die Sachkonteneinträge und -Salden zeigen.</span><span class="sxs-lookup"><span data-stu-id="33fd0-119">View reports that show general ledger entries and balances.</span></span>  
* <span data-ttu-id="33fd0-120">GuV-Kontennullstellung.</span><span class="sxs-lookup"><span data-stu-id="33fd0-120">Close your income statement.</span></span>  
* <span data-ttu-id="33fd0-121">Öffnen der Sachkontokarte, um Einstellungen hinzuzufügen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="33fd0-121">Open the G/L account card to add or change settings.</span></span>  
* <span data-ttu-id="33fd0-122">Sie können außerdem eine Liste von Buchungsgruppen anzeigen, die auf dieses Konto buchen.</span><span class="sxs-lookup"><span data-stu-id="33fd0-122">See a list of posting groups that post to that account.</span></span>  

<span data-ttu-id="33fd0-123">Sie können Sachkonten hinzufügen, ändern oder löschen.</span><span class="sxs-lookup"><span data-stu-id="33fd0-123">You can add, change, or delete general ledger accounts.</span></span> <span data-ttu-id="33fd0-124">Um jedoch Differenzen zu verhindern, können Sie ein Sachkonto nicht löschen, wenn Daten im Kontenplan verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="33fd0-124">However, to prevent discrepancies, you can't delete a general ledger account if it's data is used in the chart of accounts.</span></span>  

## <a name="account-categories"></a><span data-ttu-id="33fd0-125">Kontokategorien</span><span class="sxs-lookup"><span data-stu-id="33fd0-125">Account Categories</span></span>
<span data-ttu-id="33fd0-126">Sie können die Struktur der Finanzberichte personalisieren, indem Sie Sachkonten den Kontenkategorien hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="33fd0-126">You can personalize the structure of your financial statements by mapping general ledger accounts to account categories.</span></span>  

<span data-ttu-id="33fd0-127">Das Fenster **Sachkontokategorien** zeigt Ihre vorhandenen Haupt- und Unterkategorien und die Sachkonten an, die Sie jeder Kategorie zugeordnet haben.</span><span class="sxs-lookup"><span data-stu-id="33fd0-127">The **G/L Account Categories** window shows your categories and subcategories, and the G/L accounts that are assigned to them.</span></span> <span data-ttu-id="33fd0-128">Sie können neue Unterkategorien erstellen und diese bestehenden Konten zuweisen.</span><span class="sxs-lookup"><span data-stu-id="33fd0-128">You can create new subcategories and assign those categories to existing accounts.</span></span>  

<span data-ttu-id="33fd0-129">Sie erstellen eine Kategoriengruppe, indem Sie weitere Unterkategorien unter einer Zeile im Fenster **Sachkontokategorien** einrücken.</span><span class="sxs-lookup"><span data-stu-id="33fd0-129">You create a category group by indenting other subcategories under a line in the **G/L Account Categories** window.</span></span> <span data-ttu-id="33fd0-130">Dieses erleichtert Ihnen den Überblick, da jede Gruppierung einen Gesamtsaldo anzeigt.</span><span class="sxs-lookup"><span data-stu-id="33fd0-130">This makes it easy for you to get an overview, because each grouping shows a total balance.</span></span> <span data-ttu-id="33fd0-131">Beispielsweise können Sie Unterkategorien für unterschiedliche Arten von Anlagen erstellen und dann Kategoriengruppen für Anlagen gegenüber Umlaufvermögen erstellen.</span><span class="sxs-lookup"><span data-stu-id="33fd0-131">For example, you can create subcategories for different types of assets, and then create category groups for fixed assets versus current assets.</span></span>  

<span data-ttu-id="33fd0-132">Für jede Unterkategorie können Sie festlegen, ob Konten dieser Kategorie in bestimmte Arten von Finanzberichten enthalten sein müssen.</span><span class="sxs-lookup"><span data-stu-id="33fd0-132">You can specify whether the accounts in each subcategory must be included in specific types of reports.</span></span> <span data-ttu-id="33fd0-133">Die Kontengruppen helfen Ihnen dabei, das Layout Ihrer Finanzberichte zu definieren.</span><span class="sxs-lookup"><span data-stu-id="33fd0-133">The account categories help define the layout of your financial statements.</span></span>  

<span data-ttu-id="33fd0-134">Beispielsweise gibt es in der Standardsaldoabrechnung eine einzige Unterkategorie für Zahlungen unter Anlagen.</span><span class="sxs-lookup"><span data-stu-id="33fd0-134">For example, the default balance statement has a subcategory for Cash under Current Assets.</span></span> <span data-ttu-id="33fd0-135">Wenn Sie möchten, dass die Saldoabrechnung Handgeld und Giro berücksichtigt, können Sie:</span><span class="sxs-lookup"><span data-stu-id="33fd0-135">If you want the balance statement consider petty cash and checking, you can:</span></span>  

1. <span data-ttu-id="33fd0-136">Zwei neue Unterkategorien hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="33fd0-136">Add two new subcategories.</span></span> <span data-ttu-id="33fd0-137">Eine für Handgeld und eine für Ihr Girokonto.</span><span class="sxs-lookup"><span data-stu-id="33fd0-137">One for petty cash, and one for your checking account.</span></span>  
2. <span data-ttu-id="33fd0-138">Geben Sie die zusätzlichen Berichtsdefinition **Bargeldkonten** für diese Unterkategorien an.</span><span class="sxs-lookup"><span data-stu-id="33fd0-138">Specify the additional report definition **Cash Accounts** for these subcategories.</span></span>  
3. <span data-ttu-id="33fd0-139">Fassen Sie diese in der Unterkategorie **Bar** zusammen.</span><span class="sxs-lookup"><span data-stu-id="33fd0-139">Indent them under the **Cash** subcategory.</span></span>  

<span data-ttu-id="33fd0-140">Wenn Sie das nächste Mal ein Kontenschemata auf Grundlage Ihre Änderungen erstellt haben, wird die nächste Saldoabrechnung ein Gesamtsaldo für Zahlungen und zwei Zeilen mit Salden für Handgeld und das Girokonto anzeigen.</span><span class="sxs-lookup"><span data-stu-id="33fd0-140">The next time you generate account schedules your balance statement will show a total balance for cash and two lines with balances for petty cash and the checking account.</span></span>  

## <a name="see-also"></a><span data-ttu-id="33fd0-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33fd0-141">See Also</span></span>
[<span data-ttu-id="33fd0-142">Finanzen</span><span class="sxs-lookup"><span data-stu-id="33fd0-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="33fd0-143">Einrichten oder Ändern des Kontenplans</span><span class="sxs-lookup"><span data-stu-id="33fd0-143">Setting Up or Changing the Chart of Accounts</span></span>](finance-setup-chart-accounts.md)  
[<span data-ttu-id="33fd0-144">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="33fd0-144">Business Intelligence</span></span>](bi.md)  

