---
title: "Gewusst wie: Einrichten von Berichten für MwSt. und Intrastat"
description: "In Finance and Operations, Business edition können Sie festlegen, welche Berichte verwendet werden sollen, um die Dokumente zu erstellen, die Sie an die Behörden, wie beispielsweise die MwSt.-Abrechnung und das Intrastat-Formular übermitteln müssen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: dcbd0891515c1447a7d9f417ac2576835136ef55
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-reports-for-vat-and-intrastat"></a><span data-ttu-id="34c6b-103">Richten Sie Berichte für MwSt ein.</span><span class="sxs-lookup"><span data-stu-id="34c6b-103">Set Up Reports for VAT and Intrastat</span></span>
<span data-ttu-id="34c6b-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] können Sie festlegen, welche Berichte verwendet werden sollen, um die Dokumente zu erstellen, die Sie an die Behörden, wie beispielsweise die MwSt.-Abrechnung und das Intrastat-Formular übermitteln müssen.</span><span class="sxs-lookup"><span data-stu-id="34c6b-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can specify which reports to use to create the documents that you must submit to the authorities, such as the VAT statement and the Intrastat form.</span></span>  

### <a name="to-set-up-reports-for-vat"></a><span data-ttu-id="34c6b-105">Richten Sie MwSt.-Berichte ein.</span><span class="sxs-lookup"><span data-stu-id="34c6b-105">To set up reports for VAT</span></span>  

1.  <span data-ttu-id="34c6b-106">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "")Nach Seite oder Bericht suchen und geben **Berichtauswahl MwSt** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="34c6b-106">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Selections VAT**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="34c6b-107">Im Fenster **Berichtsauswahl - MwSt.** im Feld **Verbrauch**, wählen Sie die Art des Belegs aus, für die Sie Berichte festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="34c6b-107">In the **Report Selection – VAT** window, in the **Usage** field, select the type of document that you want to specify reports for.</span></span> <span data-ttu-id="34c6b-108">Dieses umfasst die MwSt.-Abrechnung und den MwSt.-Abrechnungsplan.</span><span class="sxs-lookup"><span data-stu-id="34c6b-108">This includes the VAT statement and the VAT statement schedule.</span></span>  

3.  <span data-ttu-id="34c6b-109">Geben Sie den Bericht oder den Batchauftrag an, die ausgeführt werden müssen, wenn ein Benutzer die Aktivität für die Belegart startet, die Sie im Feld **Verbrauch** angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="34c6b-109">Specify the report or batch job that must run when a user starts the activity for the document type that you specified in the **Usage** field.</span></span> <span data-ttu-id="34c6b-110">Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="34c6b-110">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="34c6b-111">Feld</span><span class="sxs-lookup"><span data-stu-id="34c6b-111">Field</span></span>|<span data-ttu-id="34c6b-112">Description</span><span class="sxs-lookup"><span data-stu-id="34c6b-112">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="34c6b-113">**Reihenfolge**</span><span class="sxs-lookup"><span data-stu-id="34c6b-113">**Sequence**</span></span>|<span data-ttu-id="34c6b-114">Gibt an, wo in der Druckreihenfolge ein Bericht steht.</span><span class="sxs-lookup"><span data-stu-id="34c6b-114">Specifies where a report is in the printing order.</span></span>|  
    |<span data-ttu-id="34c6b-115">**Berichts-ID**</span><span class="sxs-lookup"><span data-stu-id="34c6b-115">**Report ID**</span></span>|<span data-ttu-id="34c6b-116">Gibt die ID des Berichts an, der für diese Belegart gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="34c6b-116">Specifies the ID of the report that prints for this document type.</span></span>|  
    |<span data-ttu-id="34c6b-117">**Berichtsname**</span><span class="sxs-lookup"><span data-stu-id="34c6b-117">**Report Name**</span></span>|<span data-ttu-id="34c6b-118">Gibt den Namen des Berichts an, der für diese Belegart gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="34c6b-118">Specifies the name of the report that prints for this document type.</span></span> <span data-ttu-id="34c6b-119">Die **Berichtsname** Feldupdates auf Grundlage der Auswahl im **Berichts-ID**.</span><span class="sxs-lookup"><span data-stu-id="34c6b-119">The **Report Name** field updates based on the selection in the **Report ID** field.</span></span>|  

4.  <span data-ttu-id="34c6b-120">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="34c6b-120">Choose the **OK** button.</span></span>  

### <a name="to-set-up-reports-for-intrastat"></a><span data-ttu-id="34c6b-121">Richten Sie Intrastat-Berichte ein.</span><span class="sxs-lookup"><span data-stu-id="34c6b-121">To set up reports for Intrastat</span></span>  

1.  <span data-ttu-id="34c6b-122">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen")und geben **Berichtauswahl** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="34c6b-122">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Selection**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="34c6b-123">Im Fenster **Berichtsauswahl - Intrastat** im Feld **Verbrauch**, wählen Sie die Art des Belegs aus, für die Sie Berichte festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="34c6b-123">In the **Report Selection – Intrastat** window, in the **Usage** field, select the type of document that you want to specify reports for.</span></span> <span data-ttu-id="34c6b-124">Dieses umfasst die Intrastat-Checkliste und das Intrastat-Formular.</span><span class="sxs-lookup"><span data-stu-id="34c6b-124">This includes the Intrastat checklist and Intrastat form.</span></span>  

3.  <span data-ttu-id="34c6b-125">Geben Sie den Bericht oder den Batchauftrag an, die ausgeführt werden müssen, wenn ein Benutzer die Aktivität für die Belegart startet, die Sie im Feld **Verbrauch** angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="34c6b-125">Specify the report or batch job that must run when a user starts the activity for the document type that you specified in the **Usage** field.</span></span> <span data-ttu-id="34c6b-126">Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="34c6b-126">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="34c6b-127">Feld</span><span class="sxs-lookup"><span data-stu-id="34c6b-127">Field</span></span>|<span data-ttu-id="34c6b-128">Description</span><span class="sxs-lookup"><span data-stu-id="34c6b-128">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="34c6b-129">**Reihenfolge**</span><span class="sxs-lookup"><span data-stu-id="34c6b-129">**Sequence**</span></span>|<span data-ttu-id="34c6b-130">Gibt an, wo in der Druckreihenfolge ein Bericht steht.</span><span class="sxs-lookup"><span data-stu-id="34c6b-130">Specifies where a report is in the printing order.</span></span>|  
    |<span data-ttu-id="34c6b-131">**Berichts-ID**</span><span class="sxs-lookup"><span data-stu-id="34c6b-131">**Report ID**</span></span>|<span data-ttu-id="34c6b-132">Gibt die ID des Berichts an, der für diese Belegart gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="34c6b-132">Specifies the ID of the report that prints for this document type.</span></span>|  
    |<span data-ttu-id="34c6b-133">**Berichtsname**</span><span class="sxs-lookup"><span data-stu-id="34c6b-133">**Report Name**</span></span>|<span data-ttu-id="34c6b-134">Gibt den Namen des Berichts an, der für diese Belegart gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="34c6b-134">Specifies the name of the report that prints for this document type.</span></span> <span data-ttu-id="34c6b-135">Die **Berichtsname** Feldupdates auf Grundlage der Auswahl im **Berichts-ID**.</span><span class="sxs-lookup"><span data-stu-id="34c6b-135">The **Report Name** field updates based on the selection in the **Report ID** field.</span></span>|  

4.  <span data-ttu-id="34c6b-136">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="34c6b-136">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="34c6b-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34c6b-137">See Also</span></span>  
<span data-ttu-id="34c6b-138"><<<<<<< KOPF: Finanzverhältnisse/LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md [Export- und des Druck-Intrastat Berichte](how-to-export-and-print-intrastat-reports.md)</span><span class="sxs-lookup"><span data-stu-id="34c6b-138"><<<<<<< HEAD:financials/LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md [Export and Print Intrastat Reports](how-to-export-and-print-intrastat-reports.md)</span></span>  
<span data-ttu-id="34c6b-139">[MwSt Berichte](vat-reporting.md)
=======
[Gewusst wie: Exportieren und Drucken von Intrastat-Berichten](how-to-export-and-print-intrastat-reports.md)</span><span class="sxs-lookup"><span data-stu-id="34c6b-139">[VAT Reporting](vat-reporting.md)
=======
[Export and Print Intrastat Reports](how-to-export-and-print-intrastat-reports.md)</span></span>  
[<span data-ttu-id="34c6b-140">MwSt.-Abrechnung</span><span class="sxs-lookup"><span data-stu-id="34c6b-140">VAT Reporting</span></span>](vat-reporting.md)
>>>>>>> <span data-ttu-id="34c6b-141">refs/remotes/origin/Update13:archive/LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md</span><span class="sxs-lookup"><span data-stu-id="34c6b-141">refs/remotes/origin/Update13:archive/LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md</span></span>

