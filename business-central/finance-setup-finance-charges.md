---
title: Zinskonditionen einrichten
description: Erfahren Sie, wie Sie Business Central einrichten, damit Sie Debitoren über zusätzliche Gebühren informieren können, indem Sie Memos zu Finanzierungskosten senden.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 08a2443f94efbc9920145109b4b7499a3a4e05b3
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783622"
---
# <a name="set-up-finance-charge-terms"></a><span data-ttu-id="b36eb-103">Zinskonditionen einrichten</span><span class="sxs-lookup"><span data-stu-id="b36eb-103">Set Up Finance Charge Terms</span></span>

<span data-ttu-id="b36eb-104">Hat ein Debitor nicht bis zum Fälligkeitsdatum gezahlt, können automatisch Zuschläge berechnet und zu den überfälligen Beträgen auf dem Debitorkonto addiert werden.</span><span class="sxs-lookup"><span data-stu-id="b36eb-104">When a customer does not pay by the due date, you can have finance charges calculated automatically and add them to the overdue amounts on the customer's account.</span></span> <span data-ttu-id="b36eb-105">Verwenden Sie Zinsrechnungen, um Debitoren über die Zuschläge zu informieren.</span><span class="sxs-lookup"><span data-stu-id="b36eb-105">You can inform customers of the added charges by sending finance charge memos.</span></span> <span data-ttu-id="b36eb-106">Zuerst müssen Sie für jede Zinskondition einen eigenen Code einrichten.</span><span class="sxs-lookup"><span data-stu-id="b36eb-106">But first, you must set up a code that represents each finance charge calculation.</span></span> <span data-ttu-id="b36eb-107">Danach können Sie den Code in das Feld Zinskonditionencode auf Debitorenkarten eingeben.</span><span class="sxs-lookup"><span data-stu-id="b36eb-107">Then you can enter this code in the Fin. Charge Terms Code field on customer cards.</span></span>  

## <a name="finance-charge-terms"></a><span data-ttu-id="b36eb-108">Zinskonditionbestimmung</span><span class="sxs-lookup"><span data-stu-id="b36eb-108">Finance charge terms</span></span>

<span data-ttu-id="b36eb-109">Sie müssen für jede Berechnung der Finanzierungskosten Finanzierungskostenbedingungen festlegen und diese dann dem Kunden im Feld **Gebührenbedingungen Code** auf der Seite **Debitor** zuweisen.</span><span class="sxs-lookup"><span data-stu-id="b36eb-109">You must set up finance charge terms for each finance charge calculation, and then assign the terms to the customer in the **Fin. Charge Terms Code** field on the **Customer** page.</span></span>

<span data-ttu-id="b36eb-110">Zinsrechnungen können entweder auf der Grundlage des Tagessaldos oder des fälligen Saldos berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="b36eb-110">Finance charges can be calculated using either the average daily balance or the balance due methods.</span></span>

* <span data-ttu-id="b36eb-111">Durchschnittlicher Tagessaldo</span><span class="sxs-lookup"><span data-stu-id="b36eb-111">Average daily balance</span></span>  
  
  <span data-ttu-id="b36eb-112">Die Anzahl der Tage, die die Zahlung überfällig ist, wird berücksichtigt:</span><span class="sxs-lookup"><span data-stu-id="b36eb-112">The number of days the payment is overdue is taken into account:</span></span>  
  <span data-ttu-id="b36eb-113">*Durchschnittlicher Tagessaldo* - *Belastung* = *Überfälliger Betrag* x *(Überfälliger Betrag / Zinsperiodeo)* x *(Zinssatz/100)*</span><span class="sxs-lookup"><span data-stu-id="b36eb-113">*Average Daily Balance method* - *Finance Charge* = *Overdue Amount* x *(Days Overdue / Interest Period)* x *(Interest Rate/100)*</span></span>

* <span data-ttu-id="b36eb-114">Fälliger Saldo</span><span class="sxs-lookup"><span data-stu-id="b36eb-114">Balance due</span></span>  
  
  <span data-ttu-id="b36eb-115">Bei der Methode Fälliger Saldo stellt die Zinsberechnung einfach einen Prozentsatz des überfälligen Betrags dar:</span><span class="sxs-lookup"><span data-stu-id="b36eb-115">The finance charge is a percentage of the overdue amount:</span></span>  
  <span data-ttu-id="b36eb-116">*Methode fälliger Saldo* - *Belastung* = *Überfälliger Betrag* x *(Zinssatz Rate / 100)*</span><span class="sxs-lookup"><span data-stu-id="b36eb-116">*Balance Due method* - *Finance Charge* = *Overdue Amount* x *(Interest Rate / 100)*</span></span>

<span data-ttu-id="b36eb-117">Zusätzlich ist jede Bestimmung in der Tabelle Zinskondition mit einer Untertabelle, der Tabelle Zinsrechnungstext verbunden.</span><span class="sxs-lookup"><span data-stu-id="b36eb-117">Additionally, each term in the Finance Charge Terms table is linked to a subtable, the Finance Charge Text table.</span></span> <span data-ttu-id="b36eb-118">Für jeden Zinskonditionencode kann hier ein Vor- und/oder Nachtext hinterlegt werden, der dann auf dem Zinsrechnungsbeleg erscheint.</span><span class="sxs-lookup"><span data-stu-id="b36eb-118">For each set of finance charge terms, you can define a beginning and/or an ending text to include on the finance charge memo.</span></span>

### <a name="to-set-up-finance-charge-terms"></a><span data-ttu-id="b36eb-119">Um Bedingungen für Gebühren festzulegen</span><span class="sxs-lookup"><span data-stu-id="b36eb-119">To set up finance charge terms</span></span>

1. <span data-ttu-id="b36eb-120">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Zinskonditionen** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="b36eb-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Finance Charge Terms**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b36eb-121">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="b36eb-121">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="b36eb-122">Um mehr als eine Kombination von Mahnmethoden zu verwenden, richten Sie einen Code für jede ein.</span><span class="sxs-lookup"><span data-stu-id="b36eb-122">To use more than one combination of finance charge terms, set up a code for each one.</span></span>

    <span data-ttu-id="b36eb-123">Für jede Zinskondition können Sie individuelle Bedingungen angeben, die zusätzliche Gebühren in Landes- oder Fremdwährung enthalten können.</span><span class="sxs-lookup"><span data-stu-id="b36eb-123">For each finance charge term, you can specify individual conditions that can include additional fees in both LCY and in foreign currency.</span></span> <span data-ttu-id="b36eb-124">Sie können mehrere Gebühren in Fremdwährungen für jede Bestimmung auf der Seite **Zinskonditionen** einrichten.</span><span class="sxs-lookup"><span data-stu-id="b36eb-124">You can define additional fees in foreign currencies for each term on the **Finance Charge Terms** page.</span></span>
4. <span data-ttu-id="b36eb-125">Wählen Sie die Aktion **Währungen** aus.</span><span class="sxs-lookup"><span data-stu-id="b36eb-125">Choose the **Currencies** action.</span></span>
5. <span data-ttu-id="b36eb-126">Auf der Seite **Währungen für Zinskonditionen** können Sie für jeden Begriff einen Währungscode und Gebühren definieren.</span><span class="sxs-lookup"><span data-stu-id="b36eb-126">On the **Currencies for Fin. Chrg. Terms** page, define for each term a currency code and an additional fee.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="b36eb-127">Wenn Sie Zinsrechnungen in Fremdwährungen erstellen, verwendet die Anwendung die Bedingungen für Fremdwährungen, die Sie in dieser Tabelle eingerichtet haben, um Zinsrechnungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b36eb-127">When you create finance charges in a foreign currency, the foreign currency conditions that you set up here will be used to create finance charge memos.</span></span> <span data-ttu-id="b36eb-128">Falls es keine Zinskonditionen für Fremdwährungen gibt, verwendet die Anwendung die MW-Zinskonditionen für die Mandantenwährung auf der Seite **Zinskondition** und rechnet diese in die entsprechende Währung um.</span><span class="sxs-lookup"><span data-stu-id="b36eb-128">If there are no foreign currency finance charge conditions set up, the LCY finance charge conditions specified on the **Finance Charge Terms** page will be used and then converted to the relevant currency.</span></span>

    <span data-ttu-id="b36eb-129">Für jeden Zinskonditionencode können Sie Texte festlegen, die vor (**Vortext**) oder nach (**Nachtext**) den Posten in der Zinsrechnung ausgedruckt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b36eb-129">For each finance charge term, you can specify text that will be printed before (**Beginning Text**) or after (**Ending Text**) on the entries on the finance charge memo.</span></span>  
6. <span data-ttu-id="b36eb-130">Wählen Sie die Aktionen **Vortext** oder **Nachtext** entsprechend aus und füllen Sie die Seite **Zinsgebühr** aus.</span><span class="sxs-lookup"><span data-stu-id="b36eb-130">Choose the **Beginning Text** or **Ending Text** actions respectively, and fill on the **Finance Charge Text** page.</span></span>
7. <span data-ttu-id="b36eb-131">Um zugehörige Werte in das resultierende Zinsgebühr automatisch einzusetzen, geben -Sie die folgenden Platzhaltern im Feld **Text** Feld ein.</span><span class="sxs-lookup"><span data-stu-id="b36eb-131">To automatically insert related values in the resulting finance charge text, enter the following placeholders in the **Text** field.</span></span>

|<span data-ttu-id="b36eb-132">Platzhalter</span><span class="sxs-lookup"><span data-stu-id="b36eb-132">Placeholder</span></span>|<span data-ttu-id="b36eb-133">Wert</span><span class="sxs-lookup"><span data-stu-id="b36eb-133">Value</span></span>|  
|-----------------|-----------|  
|<span data-ttu-id="b36eb-134">%1</span><span class="sxs-lookup"><span data-stu-id="b36eb-134">%1</span></span>|<span data-ttu-id="b36eb-135">Inhalt des Felds **Belegdatum** des Zinsgebührkopfs</span><span class="sxs-lookup"><span data-stu-id="b36eb-135">Content of the **Document Date** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="b36eb-136">%2</span><span class="sxs-lookup"><span data-stu-id="b36eb-136">%2</span></span>|<span data-ttu-id="b36eb-137">Inhalt des Felds **Fälligkeitsdatum** des Zinsgebührkopfs</span><span class="sxs-lookup"><span data-stu-id="b36eb-137">Content of the **Due Date** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="b36eb-138">%3</span><span class="sxs-lookup"><span data-stu-id="b36eb-138">%3</span></span>|<span data-ttu-id="b36eb-139">Inhalt des Felds **Zinssatz** im verknüpften Zinskonditionen</span><span class="sxs-lookup"><span data-stu-id="b36eb-139">Content of the **Interest Rate** field on the related finance charge terms</span></span>|  
|<span data-ttu-id="b36eb-140">%4</span><span class="sxs-lookup"><span data-stu-id="b36eb-140">%4</span></span>|<span data-ttu-id="b36eb-141">Inhalt des Felds **Restbetrag** des Zinsgebührkopfs</span><span class="sxs-lookup"><span data-stu-id="b36eb-141">Content of the **Remaining Amount** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="b36eb-142">%5</span><span class="sxs-lookup"><span data-stu-id="b36eb-142">%5</span></span>|<span data-ttu-id="b36eb-143">Inhalt des Felds **Zinsbetrag** des Zinsgebührkopfs</span><span class="sxs-lookup"><span data-stu-id="b36eb-143">Content of the **Interest Amount** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="b36eb-144">%6</span><span class="sxs-lookup"><span data-stu-id="b36eb-144">%6</span></span>|<span data-ttu-id="b36eb-145">Inhalt des Felds **Zusatzgebühr** des Zinsgebührkopfs</span><span class="sxs-lookup"><span data-stu-id="b36eb-145">Content of the **Additional Fee** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="b36eb-146">%7</span><span class="sxs-lookup"><span data-stu-id="b36eb-146">%7</span></span>|<span data-ttu-id="b36eb-147">Der Gesamtbetrag der Mahnung</span><span class="sxs-lookup"><span data-stu-id="b36eb-147">The total amount of the reminder</span></span>|  
|<span data-ttu-id="b36eb-148">%8</span><span class="sxs-lookup"><span data-stu-id="b36eb-148">%8</span></span>|<span data-ttu-id="b36eb-149">Inhalt des Felds **Währungscode** des Zinsgebührkopfs</span><span class="sxs-lookup"><span data-stu-id="b36eb-149">Content of the **Currency Code** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="b36eb-150">%9</span><span class="sxs-lookup"><span data-stu-id="b36eb-150">%9</span></span>|<span data-ttu-id="b36eb-151">Inhalt des Felds **Buchungsdatum** des Zinsgebührkopfs</span><span class="sxs-lookup"><span data-stu-id="b36eb-151">Content of the **Posting Date** field on the finance charge memo header</span></span>|  

## <a name="see-also"></a><span data-ttu-id="b36eb-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b36eb-152">See also</span></span>

[<span data-ttu-id="b36eb-153">Einziehen von Restbeträgen</span><span class="sxs-lookup"><span data-stu-id="b36eb-153">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="b36eb-154">Einrichten von Mahnmethoden, Bestimmungen und Mahntext</span><span class="sxs-lookup"><span data-stu-id="b36eb-154">Set Up Reminder Terms and Levels</span></span>](finance-setup-reminders.md)  
[<span data-ttu-id="b36eb-155">Finanzen einrichten</span><span class="sxs-lookup"><span data-stu-id="b36eb-155">Setting Up Finance</span></span>](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]