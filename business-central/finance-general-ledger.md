---
title: Erhalten von Informationen zu Finanzbuchhaltung und Kontoplan| Microsoft Docs
description: Beschreibt die Finanzbuchhaltung, den Kontenplan und die Kontokategorien.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 05/12/2020
ms.author: edupont
ms.openlocfilehash: 098317d09a5ad8c3792de48e5332b4c247eff0e0
ms.sourcegitcommit: b9264b4ed650feca18776892ec23f2aa7ec43e20
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2020
ms.locfileid: "3372543"
---
# <a name="understanding-the-general-ledger-and-the-coa"></a><span data-ttu-id="e6d0d-103">Verständis der Fibu und des Kontoplans</span><span class="sxs-lookup"><span data-stu-id="e6d0d-103">Understanding the General Ledger and the COA</span></span>

<span data-ttu-id="e6d0d-104">Die Finanzbuchhaltung speichert Finanzdaten, und der Kontenplan zeigt die Konten, auf die alle Sachposten gebucht werden, an.</span><span class="sxs-lookup"><span data-stu-id="e6d0d-104">The general ledger stores your financial data, and the chart of accounts shows the accounts that all general ledger entries are posted to.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="e6d0d-105">umfasst einen Standardkontenplan, der zur Unterstützung Ihres Unternehmens bereit steht.</span><span class="sxs-lookup"><span data-stu-id="e6d0d-105">includes a standard chart of accounts that is ready to support your business.</span></span>

## <a name="general-ledger-setup-and-general-posting-setup"></a><span data-ttu-id="e6d0d-106">Finanzbuchhaltungs-Einrichtung: und Buchungsmatrix Einrichtung</span><span class="sxs-lookup"><span data-stu-id="e6d0d-106">General Ledger Setup and General Posting Setup</span></span>

<span data-ttu-id="e6d0d-107">Die Einrichtung der Finanzbuchhaltung ist das Kernstück der Finanzvorgängen, da sie definieren, wie Sie Daten buchen.</span><span class="sxs-lookup"><span data-stu-id="e6d0d-107">The setup of the general ledger is at the core of financial processes because it defines how you post data.</span></span>  

<span data-ttu-id="e6d0d-108">Auf der Seite **Finanzbuchhaltung einrichten** geben Sie an, wie bestimmte finanzbuchhalterische Sachverhalte in Ihrem Unternehmen gehandhabt werden sollen, wie beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="e6d0d-108">On the **General Ledger Setup** page, you specify how to handle certain accounting issues in your company, such as:</span></span>  

* <span data-ttu-id="e6d0d-109">Rechnungsrundungskontodetails</span><span class="sxs-lookup"><span data-stu-id="e6d0d-109">Invoice rounding details</span></span>  
* <span data-ttu-id="e6d0d-110">Adressformate</span><span class="sxs-lookup"><span data-stu-id="e6d0d-110">Address formats</span></span>  
* <span data-ttu-id="e6d0d-111">Finanzberichterstellung</span><span class="sxs-lookup"><span data-stu-id="e6d0d-111">Financial reporting</span></span>  

<span data-ttu-id="e6d0d-112">Ebenso geben Sie auf der Seite **Buchungsmatrix Einrichtung** an, wie Sie Kombinationen aus Geschäftsbuchungsgruppen und Produktbuchungsgruppen einrichten wollen.</span><span class="sxs-lookup"><span data-stu-id="e6d0d-112">Similarly, on the **General Posting Setup** page, you specify how you want to set up combinations of general business and general product posting groups.</span></span> <span data-ttu-id="e6d0d-113">Buchungsgruppenzuordnungseinheiten nach Debitoren, Kreditoren, Artikel, Ressourcen und Einkaufs- und Verkaufsbelegen mit Sachkonten.</span><span class="sxs-lookup"><span data-stu-id="e6d0d-113">Posting groups map entities like customers, vendors, items, resources, and sales and purchase documents to general ledger accounts.</span></span> <span data-ttu-id="e6d0d-114">Für jede Kombination aus Geschäftsbuchungsgruppe und Produktbuchungsgruppe geben Sie eine Zeile ein.</span><span class="sxs-lookup"><span data-stu-id="e6d0d-114">You fill in a line for each combination of business posting group and product posting group.</span></span> <span data-ttu-id="e6d0d-115">Weitere Informationen finden Sie unter [Gruppenbuchungen einrichten](finance-posting-groups.md).</span><span class="sxs-lookup"><span data-stu-id="e6d0d-115">For more information, see [Posting Group Setups](finance-posting-groups.md).</span></span>  

> [!TIP]
> <span data-ttu-id="e6d0d-116">Die Seite **Finanzbuchhaltung Einrichtung** enthält allgemeine Felder sowie Felder, die für Ihr Land oder Ihre Region spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="e6d0d-116">The **General Ledger Setup** page includes generic fields and fields that are particular to your country or region.</span></span> <span data-ttu-id="e6d0d-117">Wenn Sie nicht sicher sind, welche Bedeutung ein Feld hat, empfehlen wir Ihnen, mit Ihrem Buchhalter zusammenzuarbeiten, um zu ermitteln, ob es für Ihre Organisation relevant ist.</span><span class="sxs-lookup"><span data-stu-id="e6d0d-117">If you are not sure of the meaning of a field, we suggest you work with your accountant to determine whether it is of relevance to your organization.</span></span>  

## <a name="the-chart-of-accounts"></a><span data-ttu-id="e6d0d-118">Kontenplan</span><span class="sxs-lookup"><span data-stu-id="e6d0d-118">The Chart of Accounts</span></span>

<span data-ttu-id="e6d0d-119">Der Kontenplan zeigt alle Sachkonten an.</span><span class="sxs-lookup"><span data-stu-id="e6d0d-119">The chart of accounts shows all general ledger accounts.</span></span> <span data-ttu-id="e6d0d-120">Vom Kontenplan aus können Sie Dinge tun wie:</span><span class="sxs-lookup"><span data-stu-id="e6d0d-120">From the chart of accounts, you can do things like:</span></span>  

* <span data-ttu-id="e6d0d-121">Berichte ansehen, die die Sachkonteneinträge und -Salden zeigen.</span><span class="sxs-lookup"><span data-stu-id="e6d0d-121">View reports that show general ledger entries and balances.</span></span>  
* <span data-ttu-id="e6d0d-122">GuV-Kontennullstellung.</span><span class="sxs-lookup"><span data-stu-id="e6d0d-122">Close your income statement.</span></span>  
* <span data-ttu-id="e6d0d-123">Öffnen der Sachkontokarte, um Einstellungen hinzuzufügen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e6d0d-123">Open the G/L account card to add or change settings.</span></span>  
* <span data-ttu-id="e6d0d-124">Sie können außerdem eine Liste von Buchungsgruppen anzeigen, die auf dieses Konto buchen.</span><span class="sxs-lookup"><span data-stu-id="e6d0d-124">See a list of posting groups that post to that account.</span></span>
* <span data-ttu-id="e6d0d-125">Ansicht der Soll- und Habensalden von einzelnen Sachkonten</span><span class="sxs-lookup"><span data-stu-id="e6d0d-125">View separate debit and credit balances for a single account</span></span>  

<span data-ttu-id="e6d0d-126">Sie können Sachkonten hinzufügen, ändern oder löschen.</span><span class="sxs-lookup"><span data-stu-id="e6d0d-126">You can add, change, or delete general ledger accounts.</span></span> <span data-ttu-id="e6d0d-127">Um jedoch Differenzen zu verhindern, können Sie ein Sachkonto nicht löschen, wenn Daten im Kontenplan verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6d0d-127">However, to prevent discrepancies, you can't delete a general ledger account if it's data is used in the chart of accounts.</span></span>  

## <a name="account-categories"></a><span data-ttu-id="e6d0d-128">Kontokategorien</span><span class="sxs-lookup"><span data-stu-id="e6d0d-128">Account Categories</span></span>

<span data-ttu-id="e6d0d-129">Sie können die Struktur der Finanzberichte personalisieren, indem Sie Sachkonten den Kontenkategorien hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e6d0d-129">You can personalize the structure of your financial statements by mapping general ledger accounts to account categories.</span></span>  

<span data-ttu-id="e6d0d-130">Die Seite **Sachkontokategorien** zeigt Ihre vorhandenen Haupt- und Unterkategorien und die Sachkonten an, die Sie jeder Kategorie zugeordnet haben.</span><span class="sxs-lookup"><span data-stu-id="e6d0d-130">The **G/L Account Categories** page shows your categories and subcategories, and the G/L accounts that are assigned to them.</span></span> <span data-ttu-id="e6d0d-131">Sie können neue Unterkategorien erstellen und diese bestehenden Konten zuweisen.</span><span class="sxs-lookup"><span data-stu-id="e6d0d-131">You can create new subcategories and assign those categories to existing accounts.</span></span>  

<span data-ttu-id="e6d0d-132">Sie erstellen eine Kategoriengruppe, indem Sie weitere Unterkategorien unter einer Zeile auf der Seite **Sachkontokategorien** einrücken.</span><span class="sxs-lookup"><span data-stu-id="e6d0d-132">You create a category group by indenting other subcategories under a line on the **G/L Account Categories** page.</span></span> <span data-ttu-id="e6d0d-133">Dieses erleichtert Ihnen den Überblick, da jede Gruppierung einen Gesamtsaldo anzeigt.</span><span class="sxs-lookup"><span data-stu-id="e6d0d-133">This makes it easy for you to get an overview, because each grouping shows a total balance.</span></span> <span data-ttu-id="e6d0d-134">Beispielsweise können Sie Unterkategorien für unterschiedliche Arten von Anlagen erstellen und dann Kategoriengruppen für Anlagen gegenüber Umlaufvermögen erstellen.</span><span class="sxs-lookup"><span data-stu-id="e6d0d-134">For example, you can create subcategories for different types of assets, and then create category groups for fixed assets versus current assets.</span></span>  

<span data-ttu-id="e6d0d-135">Für jede Unterkategorie können Sie festlegen, ob Konten dieser Kategorie in bestimmte Arten von Finanzberichten enthalten sein müssen.</span><span class="sxs-lookup"><span data-stu-id="e6d0d-135">You can specify whether the accounts in each subcategory must be included in specific types of reports.</span></span> <span data-ttu-id="e6d0d-136">Die Kontengruppen helfen Ihnen dabei, das Layout Ihrer Finanzberichte zu definieren.</span><span class="sxs-lookup"><span data-stu-id="e6d0d-136">The account categories help define the layout of your financial statements.</span></span>  

<span data-ttu-id="e6d0d-137">Beispielsweise gibt es in der Standardsaldoabrechnung eine einzige Unterkategorie für Zahlungen unter Anlagen.</span><span class="sxs-lookup"><span data-stu-id="e6d0d-137">For example, the default balance statement has a subcategory for Cash under Current Assets.</span></span> <span data-ttu-id="e6d0d-138">Wenn Sie möchten, dass die Saldoabrechnung Handgeld und Giro berücksichtigt, können Sie:</span><span class="sxs-lookup"><span data-stu-id="e6d0d-138">If you want the balance statement consider petty cash and checking, you can:</span></span>  

1. <span data-ttu-id="e6d0d-139">Zwei neue Unterkategorien hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e6d0d-139">Add two new subcategories.</span></span> <span data-ttu-id="e6d0d-140">Eine für Handgeld und eine für Ihr Girokonto.</span><span class="sxs-lookup"><span data-stu-id="e6d0d-140">One for petty cash, and one for your checking account.</span></span>  
2. <span data-ttu-id="e6d0d-141">Geben Sie die zusätzlichen Berichtsdefinition **Bargeldkonten** für diese Unterkategorien an.</span><span class="sxs-lookup"><span data-stu-id="e6d0d-141">Specify the additional report definition **Cash Accounts** for these subcategories.</span></span>  
3. <span data-ttu-id="e6d0d-142">Fassen Sie diese in der Unterkategorie **Bar** zusammen.</span><span class="sxs-lookup"><span data-stu-id="e6d0d-142">Indent them under the **Cash** subcategory.</span></span>  

<span data-ttu-id="e6d0d-143">Wenn Sie das nächste Mal ein Kontenschemata auf Grundlage Ihre Änderungen erstellt haben, wird die nächste Saldoabrechnung ein Gesamtsaldo für Zahlungen und zwei Zeilen mit Salden für Handgeld und das Girokonto anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e6d0d-143">The next time you generate account schedules your balance statement will show a total balance for cash and two lines with balances for petty cash and the checking account.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e6d0d-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6d0d-144">See Also</span></span>

[<span data-ttu-id="e6d0d-145">Finanzen</span><span class="sxs-lookup"><span data-stu-id="e6d0d-145">Finance</span></span>](finance.md)  
[<span data-ttu-id="e6d0d-146">Einrichten oder Ändern des Kontenplans</span><span class="sxs-lookup"><span data-stu-id="e6d0d-146">Setting Up or Changing the Chart of Accounts</span></span>](finance-setup-chart-accounts.md)  
[<span data-ttu-id="e6d0d-147">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="e6d0d-147">Business Intelligence</span></span>](bi.md)  
