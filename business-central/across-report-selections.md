---
title: Berichtsauswahl in Business Central
description: Erfahren Sie, wie Sie die Berichte einrichten, mit denen Sie verschiedene Arten von Dokumenten in Business Central drucken.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: setup, reporting
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ba15a65317ebf52579c285c93dd59eba1b65ae1b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787107"
---
# <a name="report-selection-in-business-central"></a><span data-ttu-id="cce03-103">Berichtsauswahl in Business Central</span><span class="sxs-lookup"><span data-stu-id="cce03-103">Report Selection in Business Central</span></span>

<span data-ttu-id="cce03-104">Sie können Standardbereichte einrichten, die verwendet werden, um sie bei der Arbeit mit verschiedenen Einkaufs- und Verkaufsbelegen, wie Bestellungen, Angebote, Rechnungen und Gutschriften, drucken zu können.</span><span class="sxs-lookup"><span data-stu-id="cce03-104">You can set up default reports that will be used to print the various documents for sales and purchases, such as orders, quotes, invoices, and credit memos.</span></span> <span data-ttu-id="cce03-105">Wenn Sie beispielsweise ein bestimmtes Layout für Verkaufsrechnungen haben, können Sie diesen Bericht auf der Seite **Berichtsauswahl – Verkauf** definieren, damit sie zum Senden oder Drucken von Verkaufsrechnungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cce03-105">For example, if you have a specific layout for sales invoices, you can specify that report in the **Report Selections - Sales** page so that it will be used to send or print sales invoices.</span></span>  

<span data-ttu-id="cce03-106">Die Seiten **Berichtsauswahl** geben an, welcher Bericht in verschiedenen Situationen gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="cce03-106">The **Report Selections** pages specify which report will be printed in different situations.</span></span> <span data-ttu-id="cce03-107">[!INCLUDE [prod_short](includes/prod_short.md)] enthält Standardkonfigurationen, aber Sie können diese Standardeinstellungen natürlich ändern.</span><span class="sxs-lookup"><span data-stu-id="cce03-107">[!INCLUDE [prod_short](includes/prod_short.md)] includes default configurations, but of course you can change these defaults.</span></span> <span data-ttu-id="cce03-108">Zudem lassen sich auch weitere Berichte in das Fenster **Berichtsauswahl** aufnehmen, um gleichzeitig mehrere Berichte zu einer Belegart auszudrucken.</span><span class="sxs-lookup"><span data-stu-id="cce03-108">You can also add reports to the **Report Selection** pages if you want to print more than one report per document type, for example.</span></span>  

## <a name="available-report-selections"></a><span data-ttu-id="cce03-109">Verfügbare Berichtsauswahl</span><span class="sxs-lookup"><span data-stu-id="cce03-109">Available report selections</span></span>

<span data-ttu-id="cce03-110">[!INCLUDE [prod_short](includes/prod_short.md)] beinhaltet verschiedene **Berichtsauswahl** Seiten für verschiedene Bereiche.</span><span class="sxs-lookup"><span data-stu-id="cce03-110">[!INCLUDE [prod_short](includes/prod_short.md)] includes different **Report Selection** pages for different areas.</span></span> <span data-ttu-id="cce03-111">In den folgenden Tabellen wird beschrieben, wo Sie Informationen zu den verschiedenen Seiten finden.</span><span class="sxs-lookup"><span data-stu-id="cce03-111">The following tables describes where you can find information about the different pages.</span></span>  

|<span data-ttu-id="cce03-112">Bereich oder Aufgabe</span><span class="sxs-lookup"><span data-stu-id="cce03-112">Area or task</span></span>  |<span data-ttu-id="cce03-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cce03-113">Learn more</span></span>|
|--------------|----------|
|<span data-ttu-id="cce03-114">Beispiel für die Funktionsweise der Berichtsauswahl (Vertrieb)</span><span class="sxs-lookup"><span data-stu-id="cce03-114">Example of how report selection works (Sales)</span></span>|[<span data-ttu-id="cce03-115">Berichtsauswahl für Verkaufsbelege</span><span class="sxs-lookup"><span data-stu-id="cce03-115">Report selection for sales documents</span></span>](#example-report-selection-for-sales-documents)|
|<span data-ttu-id="cce03-116">Standardlayout für E-Mails mit Verkaufs- und Kaufdokumenten</span><span class="sxs-lookup"><span data-stu-id="cce03-116">Default layout for emails with sales and purchase documents</span></span>  |[<span data-ttu-id="cce03-117">Richten Sie wiederverwendbare E-Mail-Texte und Layouts für Verkaufs- und Einkaufsbelege ein</span><span class="sxs-lookup"><span data-stu-id="cce03-117">Set Up Reusable Email Texts and Layouts for Sales and Purchase Documents</span></span>](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents) |
|<span data-ttu-id="cce03-118">Schecklayouts definieren</span><span class="sxs-lookup"><span data-stu-id="cce03-118">Define check layouts</span></span>     |[<span data-ttu-id="cce03-119">Ein Prüflayout auswählen</span><span class="sxs-lookup"><span data-stu-id="cce03-119">Select a Check Layout</span></span>](finance-how-define-check-layouts.md) |
|<span data-ttu-id="cce03-120">Berichte für die Mehrwertsteuerberichterstattung definieren (Deutschland)</span><span class="sxs-lookup"><span data-stu-id="cce03-120">Define reports for VAT reporting (Germany)</span></span>|[<span data-ttu-id="cce03-121">Richten Sie Berichte für MwSt ein</span><span class="sxs-lookup"><span data-stu-id="cce03-121">Set Up Reports for VAT and Intrastat</span></span>](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> <span data-ttu-id="cce03-122">Ihr [!INCLUDE [prod_short](includes/prod_short.md)] kann zusätzliche Seiten **Berichtsauswahl** enthalten, abhängig von Ihrem Standort und Ihrer Branche.</span><span class="sxs-lookup"><span data-stu-id="cce03-122">Your [!INCLUDE [prod_short](includes/prod_short.md)] can include additional **Report Selection** pages, depending on your location and industry, for example.</span></span> <span data-ttu-id="cce03-123">Sie können Ihre Einrichtung jederzeit überprüfen, indem Sie das Symbol ![Glühbirne, die die Funktion Wie möchten Sie weiter verfahren öffnet](media/ui-search/search_small.png "Was möchten Sie tun") auswählen und dann **Berichtsauswahl** eingeben und den entsprechenden Link auswählen.</span><span class="sxs-lookup"><span data-stu-id="cce03-123">You can always check your setup by choosing the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, entering **Report Selections**, and then choose the relevant link.</span></span>

<span data-ttu-id="cce03-124">Die Standardversion von [!INCLUDE [prod_short](includes/prod_short.md)] beinhaltet die folgende Seite **Berichtsabschnitt**:</span><span class="sxs-lookup"><span data-stu-id="cce03-124">The default version of [!INCLUDE [prod_short](includes/prod_short.md)] includes the following **Report Section** pages:</span></span>

* <span data-ttu-id="cce03-125">**Berichtsauswahl - Verkauf**</span><span class="sxs-lookup"><span data-stu-id="cce03-125">**Report Selection - Sales**</span></span>  
* <span data-ttu-id="cce03-126">**Berichtsauswahl - Einkauf**</span><span class="sxs-lookup"><span data-stu-id="cce03-126">**Report Selection - Purchase**</span></span>  
* <span data-ttu-id="cce03-127">**Berichtsauswahl - Lager**</span><span class="sxs-lookup"><span data-stu-id="cce03-127">**Report Selection - Inventory**</span></span>  
* <span data-ttu-id="cce03-128">**Berichtsauswahl - Cashflow**</span><span class="sxs-lookup"><span data-stu-id="cce03-128">**Report Selection - Cash Flow**</span></span>  
* <span data-ttu-id="cce03-129">**Berichtsauswahl – Lager**</span><span class="sxs-lookup"><span data-stu-id="cce03-129">**Report Selection - Warehouse**</span></span>  
* <span data-ttu-id="cce03-130">**Berichtsauswahl - Bankkonto**</span><span class="sxs-lookup"><span data-stu-id="cce03-130">**Report Selection - Bank Account**</span></span>  
* <span data-ttu-id="cce03-131">**Berichtsauswahlen - Mahnung/Zinsrechnung**</span><span class="sxs-lookup"><span data-stu-id="cce03-131">**Report Selections Reminder/Finance Charge**</span></span>  

## <a name="example-report-selection-for-sales-documents"></a><span data-ttu-id="cce03-132">Beispiel: Berichtsauswahl für Verkaufsbelege</span><span class="sxs-lookup"><span data-stu-id="cce03-132">Example: Report selection for sales documents</span></span>

<span data-ttu-id="cce03-133">Die Seite **Berichtsauswahl – Verkauf** definiert die Standardberichte, die in verschiedenen Szenarien für jeden zugehörigen Dokumenttyp verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cce03-133">The **Report Selection - Sales** page defines the default reports to use in different scenarios for each related document type.</span></span> <span data-ttu-id="cce03-134">Wählen Sie einen Dokumenttyp im Feld **Verwendung** und fügen Sie dann die Berichtsauswahl hinzu oder überprüfen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="cce03-134">Choose a document type in the **Usage** field, and then add or review the report selection.</span></span> <span data-ttu-id="cce03-135">Sie können mehr als einen Bericht und die Reihenfolge festlegen, in der die Berichte gesendet oder gedruckt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="cce03-135">You can set up more than one report and the order of sequence that the reports must be sent or printed in.</span></span>  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="cce03-136">Einige Dokumenttypen können als E-Mail-Anhänge gesendet werden, andere nicht.</span><span class="sxs-lookup"><span data-stu-id="cce03-136">Some types of document can be sent as email attachments, and others cannot.</span></span> <span data-ttu-id="cce03-137">Jede Seite **Berichtsauswahl** zeigt zusätzliche Felder an, wenn der Typ unterstützende E-Mail nicht sofort verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="cce03-137">Each **Report Selection** page shows additional fields if the type support email out of the box.</span></span>  

<span data-ttu-id="cce03-138">Zum Beispiel helfen Ihnen die Seiten **Berichtsauswahl – Verkauf** und **Berichtsauswahl – Kauf** die folgenden Felder für die E-Mails einzurichten:</span><span class="sxs-lookup"><span data-stu-id="cce03-138">For example, in the **Report Selection - Sales** and **Report Selection - Purchase** pages, the following fields help you set up emailing:</span></span>

|<span data-ttu-id="cce03-139">Name des Felds</span><span class="sxs-lookup"><span data-stu-id="cce03-139">Field name</span></span> |<span data-ttu-id="cce03-140">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cce03-140">Description</span></span>  |
|-----------|-------------|
|<span data-ttu-id="cce03-141">**Für E-Mail-Text verwenden**</span><span class="sxs-lookup"><span data-stu-id="cce03-141">**Use for Email Body**</span></span>| <span data-ttu-id="cce03-142">Gibt an, dass zusammengefasste Informationen, z. B. Rechnungsnummer, Fälligkeitsdatum und Zahlungsservicelink, in den Text der gesendeten E-Mail eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="cce03-142">Specifies that summarized information, such as invoice number, due date, and payment service link, will be inserted in the body of the email that you send.</span></span>        |
|<span data-ttu-id="cce03-143">**Für E-Mail-Anhang verwenden**</span><span class="sxs-lookup"><span data-stu-id="cce03-143">**Use for Email Attachment**</span></span>| <span data-ttu-id="cce03-144">Legt fest, dass der zugehörige Beleg an die E-Mail angehängt wird.</span><span class="sxs-lookup"><span data-stu-id="cce03-144">Specifies that the related document will be attached to the email.</span></span>|
|<span data-ttu-id="cce03-145">**Layout-Beschreibung E-Mail-Text**</span><span class="sxs-lookup"><span data-stu-id="cce03-145">**Email Body Layout Description**</span></span>|<span data-ttu-id="cce03-146">Gibt das verwendete E-Mail-Textlayout an, normalerweise ein benutzerdefiniertes Berichtslayout.</span><span class="sxs-lookup"><span data-stu-id="cce03-146">Specifies the email body layout that is used, typically a custom report layout.</span></span> |

## <a name="see-also"></a><span data-ttu-id="cce03-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cce03-147">See also</span></span>

[<span data-ttu-id="cce03-148">Richten Sie wiederverwendbare E-Mail-Texte und Layouts für Verkaufs- und Einkaufsbelege ein</span><span class="sxs-lookup"><span data-stu-id="cce03-148">Set Up Reusable Email Texts and Layouts for Sales and Purchase Documents</span></span>](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents)  
[<span data-ttu-id="cce03-149">Ein Prüflayout auswählen</span><span class="sxs-lookup"><span data-stu-id="cce03-149">Select a Check Layout</span></span>](finance-how-define-check-layouts.md)  
[<span data-ttu-id="cce03-150">Einrichten von Berichten für MwSt. und Intrastat (Deutschland)</span><span class="sxs-lookup"><span data-stu-id="cce03-150">Set Up Reports for VAT and Intrastat (Germany)</span></span>](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[<span data-ttu-id="cce03-151">Verwaltung von Berichts- und Dokumentlayouts</span><span class="sxs-lookup"><span data-stu-id="cce03-151">Managing Report and Document Layouts</span></span>](ui-manage-report-layouts.md)  
[<span data-ttu-id="cce03-152">Beleglayouts für Debitoren und Kreditoren definieren</span><span class="sxs-lookup"><span data-stu-id="cce03-152">Define Document Layouts for Customers and Vendors</span></span>](ui-define-customer-vendor-document-layouts.md)  
[<span data-ttu-id="cce03-153">Drucker einrichten</span><span class="sxs-lookup"><span data-stu-id="cce03-153">Set Up Printers</span></span>](ui-specify-printer-selection-reports.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]