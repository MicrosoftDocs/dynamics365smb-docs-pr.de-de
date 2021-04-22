---
title: 'Gewusst wie: Einrichten von Berichten für MwSt. und Intrastat'
description: Sie können festlegen, welche Berichte verwendet werden sollen, um die Dokumente zu erstellen, die Sie an die Behörden, wie beispielsweise die MwSt.-Abrechnung und das Intrastat-Formular übermitteln müssen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: a50fb3cbf3264cd0820a6e8312d6a510d0c96360
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5773256"
---
# <a name="set-up-reports-for-vat-and-intrastat"></a><span data-ttu-id="66d25-103">Richten Sie Berichte für MwSt ein.</span><span class="sxs-lookup"><span data-stu-id="66d25-103">Set Up Reports for VAT and Intrastat</span></span>
<span data-ttu-id="66d25-104">In [!INCLUDE[prod_short](../../includes/prod_short.md)] können Sie festlegen, welche Berichte verwendet werden sollen, um die Dokumente zu erstellen, die Sie an die Behörden, wie beispielsweise die MwSt.-Abrechnung und das Intrastat-Formular übermitteln müssen.</span><span class="sxs-lookup"><span data-stu-id="66d25-104">In [!INCLUDE[prod_short](../../includes/prod_short.md)], you can specify which reports to use to create the documents that you must submit to the authorities, such as the VAT statement and the Intrastat form.</span></span>  

### <a name="to-set-up-reports-for-vat"></a><span data-ttu-id="66d25-105">Richten Sie MwSt.-Berichte ein.</span><span class="sxs-lookup"><span data-stu-id="66d25-105">To set up reports for VAT</span></span>  

1.  <span data-ttu-id="66d25-106">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](../../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Berichtsauswahl MwSt.** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="66d25-106">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Selections VAT**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="66d25-107">Auf der Seite **Berichtsauswahl - MwSt.** im Feld **Verbrauch**, wählen Sie die Art des Belegs aus, für die Sie Berichte festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="66d25-107">On the **Report Selection – VAT** page, in the **Usage** field, select the type of document that you want to specify reports for.</span></span> <span data-ttu-id="66d25-108">Dieses umfasst die MwSt.-Abrechnung und den MwSt.-Abrechnungsplan.</span><span class="sxs-lookup"><span data-stu-id="66d25-108">This includes the VAT statement and the VAT statement schedule.</span></span>  

3.  <span data-ttu-id="66d25-109">Geben Sie den Bericht oder den Batchauftrag an, die ausgeführt werden müssen, wenn ein Benutzer die Aktivität für die Belegart startet, die Sie im Feld **Verbrauch** angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="66d25-109">Specify the report or batch job that must run when a user starts the activity for the document type that you specified in the **Usage** field.</span></span> <span data-ttu-id="66d25-110">Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="66d25-110">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="66d25-111">Feld</span><span class="sxs-lookup"><span data-stu-id="66d25-111">Field</span></span>|<span data-ttu-id="66d25-112">Description</span><span class="sxs-lookup"><span data-stu-id="66d25-112">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="66d25-113">**Reihenfolge**</span><span class="sxs-lookup"><span data-stu-id="66d25-113">**Sequence**</span></span>|<span data-ttu-id="66d25-114">Gibt an, wo in der Druckreihenfolge ein Bericht steht.</span><span class="sxs-lookup"><span data-stu-id="66d25-114">Specifies where a report is in the printing order.</span></span>|  
    |<span data-ttu-id="66d25-115">**Berichts-ID**</span><span class="sxs-lookup"><span data-stu-id="66d25-115">**Report ID**</span></span>|<span data-ttu-id="66d25-116">Gibt die ID des Berichts an, der für diese Belegart gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="66d25-116">Specifies the ID of the report that prints for this document type.</span></span>|  
    |<span data-ttu-id="66d25-117">**Berichtsname**</span><span class="sxs-lookup"><span data-stu-id="66d25-117">**Report Name**</span></span>|<span data-ttu-id="66d25-118">Gibt den Namen des Berichts an, der für diese Belegart gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="66d25-118">Specifies the name of the report that prints for this document type.</span></span> <span data-ttu-id="66d25-119">Die **Berichtsname** Feldupdates auf Grundlage der Auswahl im **Berichts-ID**.</span><span class="sxs-lookup"><span data-stu-id="66d25-119">The **Report Name** field updates based on the selection in the **Report ID** field.</span></span>|  

4.  <span data-ttu-id="66d25-120">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="66d25-120">Choose the **OK** button.</span></span>  

### <a name="to-set-up-reports-for-intrastat"></a><span data-ttu-id="66d25-121">Richten Sie Intrastat-Berichte ein.</span><span class="sxs-lookup"><span data-stu-id="66d25-121">To set up reports for Intrastat</span></span>  
> [!NOTE]
> <span data-ttu-id="66d25-122">Intrastat-Berichte können entweder das XML- oder das ASCII-Format verwenden.</span><span class="sxs-lookup"><span data-stu-id="66d25-122">Intrastat reports can use either the XML or ASCII formats.</span></span> <span data-ttu-id="66d25-123">Geben Sie je nach verwendetem Format die Materialnummer in eines der folgenden Felder auf der Seite **Unternehmensinformationen** ein.</span><span class="sxs-lookup"><span data-stu-id="66d25-123">Depending on the format you use, enter the material number in one of the following fields on the **Company  Information** page.</span></span>  
> 
> |<span data-ttu-id="66d25-124">Format</span><span class="sxs-lookup"><span data-stu-id="66d25-124">Format</span></span>|<span data-ttu-id="66d25-125">Felder</span><span class="sxs-lookup"><span data-stu-id="66d25-125">Fields</span></span>|
> |---------|---------|
> |<span data-ttu-id="66d25-126">XML</span><span class="sxs-lookup"><span data-stu-id="66d25-126">XML</span></span>|<span data-ttu-id="66d25-127">Unternehmensnummer</span><span class="sxs-lookup"><span data-stu-id="66d25-127">Company No.</span></span>|
> |<span data-ttu-id="66d25-128">ASCII</span><span class="sxs-lookup"><span data-stu-id="66d25-128">ASCII</span></span>|<span data-ttu-id="66d25-129">Verkaufsmaterial-Nr., Einkaufsmaterial-Nr.</span><span class="sxs-lookup"><span data-stu-id="66d25-129">Sales Material No., Purchase Material No.</span></span>|

1.  <span data-ttu-id="66d25-130">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](../../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Berichtsauswahl** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="66d25-130">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Selection**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="66d25-131">Auf der Seite **Berichtsauswahl - Intrastat** im Feld **Verbrauch**, wählen Sie die Art des Belegs aus, für die Sie Berichte festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="66d25-131">On the **Report Selection – Intrastat** page, in the **Usage** field, select the type of document that you want to specify reports for.</span></span> <span data-ttu-id="66d25-132">Dieses umfasst die Intrastat-Checkliste und das Intrastat-Formular.</span><span class="sxs-lookup"><span data-stu-id="66d25-132">This includes the Intrastat checklist and Intrastat form.</span></span>  

3.  <span data-ttu-id="66d25-133">Geben Sie den Bericht oder den Batchauftrag an, die ausgeführt werden müssen, wenn ein Benutzer die Aktivität für die Belegart startet, die Sie im Feld **Verbrauch** angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="66d25-133">Specify the report or batch job that must run when a user starts the activity for the document type that you specified in the **Usage** field.</span></span> <span data-ttu-id="66d25-134">Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="66d25-134">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="66d25-135">Feld</span><span class="sxs-lookup"><span data-stu-id="66d25-135">Field</span></span>|<span data-ttu-id="66d25-136">Description</span><span class="sxs-lookup"><span data-stu-id="66d25-136">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="66d25-137">**Reihenfolge**</span><span class="sxs-lookup"><span data-stu-id="66d25-137">**Sequence**</span></span>|<span data-ttu-id="66d25-138">Gibt an, wo in der Druckreihenfolge ein Bericht steht.</span><span class="sxs-lookup"><span data-stu-id="66d25-138">Specifies where a report is in the printing order.</span></span>|  
    |<span data-ttu-id="66d25-139">**Berichts-ID**</span><span class="sxs-lookup"><span data-stu-id="66d25-139">**Report ID**</span></span>|<span data-ttu-id="66d25-140">Gibt die ID des Berichts an, der für diese Belegart gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="66d25-140">Specifies the ID of the report that prints for this document type.</span></span>|  
    |<span data-ttu-id="66d25-141">**Berichtsname**</span><span class="sxs-lookup"><span data-stu-id="66d25-141">**Report Name**</span></span>|<span data-ttu-id="66d25-142">Gibt den Namen des Berichts an, der für diese Belegart gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="66d25-142">Specifies the name of the report that prints for this document type.</span></span> <span data-ttu-id="66d25-143">Die **Berichtsname** Feldupdates auf Grundlage der Auswahl im **Berichts-ID**.</span><span class="sxs-lookup"><span data-stu-id="66d25-143">The **Report Name** field updates based on the selection in the **Report ID** field.</span></span>|  

4.  <span data-ttu-id="66d25-144">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="66d25-144">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="66d25-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66d25-145">See Also</span></span>  
[<span data-ttu-id="66d25-146">Exportieren und Drucken von Intrastat-Berichten</span><span class="sxs-lookup"><span data-stu-id="66d25-146">Export and Print Intrastat Reports</span></span>](how-to-export-and-print-intrastat-reports.md)  
[<span data-ttu-id="66d25-147">MwSt.-Abrechnung</span><span class="sxs-lookup"><span data-stu-id="66d25-147">VAT Reporting</span></span>](vat-reporting.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]