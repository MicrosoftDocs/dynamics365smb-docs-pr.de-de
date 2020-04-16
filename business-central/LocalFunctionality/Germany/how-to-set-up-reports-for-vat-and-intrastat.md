---
title: 'Gewusst wie: Einrichten von Berichten für MwSt. und Intrastat'
description: Sie können festlegen, welche Berichte verwendet werden sollen, um die Dokumente zu erstellen, die Sie an die Behörden, wie beispielsweise die MwSt.-Abrechnung und das Intrastat-Formular übermitteln müssen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: dcc44164f6273558c88999f5f342bcb8da591677
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181155"
---
# <a name="set-up-reports-for-vat-and-intrastat"></a><span data-ttu-id="a7248-103">Richten Sie Berichte für MwSt ein.</span><span class="sxs-lookup"><span data-stu-id="a7248-103">Set Up Reports for VAT and Intrastat</span></span>
<span data-ttu-id="a7248-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] können Sie festlegen, welche Berichte verwendet werden sollen, um die Dokumente zu erstellen, die Sie an die Behörden, wie beispielsweise die MwSt.-Abrechnung und das Intrastat-Formular übermitteln müssen.</span><span class="sxs-lookup"><span data-stu-id="a7248-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can specify which reports to use to create the documents that you must submit to the authorities, such as the VAT statement and the Intrastat form.</span></span>  

### <a name="to-set-up-reports-for-vat"></a><span data-ttu-id="a7248-105">Richten Sie MwSt.-Berichte ein.</span><span class="sxs-lookup"><span data-stu-id="a7248-105">To set up reports for VAT</span></span>  

1.  <span data-ttu-id="a7248-106">Wählen Sie das Symbol ![Suche nach Seite oder Bericht](../../media/ui-search/search_small.png "Symbol „Suche nach Seite oder Bericht“"), geben Sie **Berichtsauswahl - MwSt.** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="a7248-106">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Selections VAT**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="a7248-107">Auf der Seite **Berichtsauswahl - MwSt.** im Feld **Verbrauch**, wählen Sie die Art des Belegs aus, für die Sie Berichte festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="a7248-107">On the **Report Selection – VAT** page, in the **Usage** field, select the type of document that you want to specify reports for.</span></span> <span data-ttu-id="a7248-108">Dieses umfasst die MwSt.-Abrechnung und den MwSt.-Abrechnungsplan.</span><span class="sxs-lookup"><span data-stu-id="a7248-108">This includes the VAT statement and the VAT statement schedule.</span></span>  

3.  <span data-ttu-id="a7248-109">Geben Sie den Bericht oder den Batchauftrag an, die ausgeführt werden müssen, wenn ein Benutzer die Aktivität für die Belegart startet, die Sie im Feld **Verbrauch** angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="a7248-109">Specify the report or batch job that must run when a user starts the activity for the document type that you specified in the **Usage** field.</span></span> <span data-ttu-id="a7248-110">Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="a7248-110">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="a7248-111">Feld</span><span class="sxs-lookup"><span data-stu-id="a7248-111">Field</span></span>|<span data-ttu-id="a7248-112">Description</span><span class="sxs-lookup"><span data-stu-id="a7248-112">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="a7248-113">**Reihenfolge**</span><span class="sxs-lookup"><span data-stu-id="a7248-113">**Sequence**</span></span>|<span data-ttu-id="a7248-114">Gibt an, wo in der Druckreihenfolge ein Bericht steht.</span><span class="sxs-lookup"><span data-stu-id="a7248-114">Specifies where a report is in the printing order.</span></span>|  
    |<span data-ttu-id="a7248-115">**Berichts-ID**</span><span class="sxs-lookup"><span data-stu-id="a7248-115">**Report ID**</span></span>|<span data-ttu-id="a7248-116">Gibt die ID des Berichts an, der für diese Belegart gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="a7248-116">Specifies the ID of the report that prints for this document type.</span></span>|  
    |<span data-ttu-id="a7248-117">**Berichtsname**</span><span class="sxs-lookup"><span data-stu-id="a7248-117">**Report Name**</span></span>|<span data-ttu-id="a7248-118">Gibt den Namen des Berichts an, der für diese Belegart gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="a7248-118">Specifies the name of the report that prints for this document type.</span></span> <span data-ttu-id="a7248-119">Die **Berichtsname** Feldupdates auf Grundlage der Auswahl im **Berichts-ID**.</span><span class="sxs-lookup"><span data-stu-id="a7248-119">The **Report Name** field updates based on the selection in the **Report ID** field.</span></span>|  

4.  <span data-ttu-id="a7248-120">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="a7248-120">Choose the **OK** button.</span></span>  

### <a name="to-set-up-reports-for-intrastat"></a><span data-ttu-id="a7248-121">Richten Sie Intrastat-Berichte ein.</span><span class="sxs-lookup"><span data-stu-id="a7248-121">To set up reports for Intrastat</span></span>  
> [!NOTE]
> <span data-ttu-id="a7248-122">Intrastat-Berichte können entweder das XML- oder das ASCII-Format verwenden.</span><span class="sxs-lookup"><span data-stu-id="a7248-122">Intrastat reports can use either the XML or ASCII formats.</span></span> <span data-ttu-id="a7248-123">Geben Sie je nach verwendetem Format die Materialnummer in eines der folgenden Felder auf der Seite **Unternehmensinformationen** ein.</span><span class="sxs-lookup"><span data-stu-id="a7248-123">Depending on the format you use, enter the material number in one of the following fields on the **Company  Information** page.</span></span>  
> 
> |<span data-ttu-id="a7248-124">Format</span><span class="sxs-lookup"><span data-stu-id="a7248-124">Format</span></span>|<span data-ttu-id="a7248-125">Felder</span><span class="sxs-lookup"><span data-stu-id="a7248-125">Fields</span></span>|
> |---------|---------|
> |<span data-ttu-id="a7248-126">XML</span><span class="sxs-lookup"><span data-stu-id="a7248-126">XML</span></span>|<span data-ttu-id="a7248-127">Unternehmensnummer</span><span class="sxs-lookup"><span data-stu-id="a7248-127">Company No.</span></span>|
> |<span data-ttu-id="a7248-128">ASCII</span><span class="sxs-lookup"><span data-stu-id="a7248-128">ASCII</span></span>|<span data-ttu-id="a7248-129">Verkaufsmaterial-Nr., Einkaufsmaterial-Nr.</span><span class="sxs-lookup"><span data-stu-id="a7248-129">Sales Material No., Purchase Material No.</span></span>|

1.  <span data-ttu-id="a7248-130">Wählen Sie das Symbol ![Suche nach Seite oder Bericht](../../media/ui-search/search_small.png "Symbol „Suche nach Seite oder Bericht“"), geben Sie **Berichtsauswahl** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="a7248-130">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Selection**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="a7248-131">Auf der Seite **Berichtsauswahl - Intrastat** im Feld **Verbrauch**, wählen Sie die Art des Belegs aus, für die Sie Berichte festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="a7248-131">On the **Report Selection – Intrastat** page, in the **Usage** field, select the type of document that you want to specify reports for.</span></span> <span data-ttu-id="a7248-132">Dieses umfasst die Intrastat-Checkliste und das Intrastat-Formular.</span><span class="sxs-lookup"><span data-stu-id="a7248-132">This includes the Intrastat checklist and Intrastat form.</span></span>  

3.  <span data-ttu-id="a7248-133">Geben Sie den Bericht oder den Batchauftrag an, die ausgeführt werden müssen, wenn ein Benutzer die Aktivität für die Belegart startet, die Sie im Feld **Verbrauch** angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="a7248-133">Specify the report or batch job that must run when a user starts the activity for the document type that you specified in the **Usage** field.</span></span> <span data-ttu-id="a7248-134">Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="a7248-134">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="a7248-135">Feld</span><span class="sxs-lookup"><span data-stu-id="a7248-135">Field</span></span>|<span data-ttu-id="a7248-136">Description</span><span class="sxs-lookup"><span data-stu-id="a7248-136">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="a7248-137">**Reihenfolge**</span><span class="sxs-lookup"><span data-stu-id="a7248-137">**Sequence**</span></span>|<span data-ttu-id="a7248-138">Gibt an, wo in der Druckreihenfolge ein Bericht steht.</span><span class="sxs-lookup"><span data-stu-id="a7248-138">Specifies where a report is in the printing order.</span></span>|  
    |<span data-ttu-id="a7248-139">**Berichts-ID**</span><span class="sxs-lookup"><span data-stu-id="a7248-139">**Report ID**</span></span>|<span data-ttu-id="a7248-140">Gibt die ID des Berichts an, der für diese Belegart gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="a7248-140">Specifies the ID of the report that prints for this document type.</span></span>|  
    |<span data-ttu-id="a7248-141">**Berichtsname**</span><span class="sxs-lookup"><span data-stu-id="a7248-141">**Report Name**</span></span>|<span data-ttu-id="a7248-142">Gibt den Namen des Berichts an, der für diese Belegart gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="a7248-142">Specifies the name of the report that prints for this document type.</span></span> <span data-ttu-id="a7248-143">Die **Berichtsname** Feldupdates auf Grundlage der Auswahl im **Berichts-ID**.</span><span class="sxs-lookup"><span data-stu-id="a7248-143">The **Report Name** field updates based on the selection in the **Report ID** field.</span></span>|  

4.  <span data-ttu-id="a7248-144">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="a7248-144">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a7248-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7248-145">See Also</span></span>  
[<span data-ttu-id="a7248-146">Exportieren und Drucken von Intrastat-Berichten</span><span class="sxs-lookup"><span data-stu-id="a7248-146">Export and Print Intrastat Reports</span></span>](how-to-export-and-print-intrastat-reports.md)  
[<span data-ttu-id="a7248-147">MwSt.-Abrechnung</span><span class="sxs-lookup"><span data-stu-id="a7248-147">VAT Reporting</span></span>](vat-reporting.md)
