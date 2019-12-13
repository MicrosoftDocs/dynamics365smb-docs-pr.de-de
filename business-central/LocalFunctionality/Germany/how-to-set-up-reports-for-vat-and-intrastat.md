---
title: 'Gewusst wie: Einrichten von Berichten für MwSt. und Intrastat'
description: In Business Central können Sie festlegen, welche Berichte verwendet werden sollen, um die Dokumente zu erstellen, die Sie an die Behörden, wie beispielsweise die MwSt.-Abrechnung und das Intrastat-Formular übermitteln müssen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: f681c2c36360daee5e5ccbdd711e26d8de203aeb
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2878918"
---
# <a name="set-up-reports-for-vat-and-intrastat"></a><span data-ttu-id="94dda-103">Richten Sie Berichte für MwSt ein.</span><span class="sxs-lookup"><span data-stu-id="94dda-103">Set Up Reports for VAT and Intrastat</span></span>
<span data-ttu-id="94dda-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] können Sie festlegen, welche Berichte verwendet werden sollen, um die Dokumente zu erstellen, die Sie an die Behörden, wie beispielsweise die MwSt.-Abrechnung und das Intrastat-Formular übermitteln müssen.</span><span class="sxs-lookup"><span data-stu-id="94dda-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can specify which reports to use to create the documents that you must submit to the authorities, such as the VAT statement and the Intrastat form.</span></span>  

### <a name="to-set-up-reports-for-vat"></a><span data-ttu-id="94dda-105">Richten Sie MwSt.-Berichte ein.</span><span class="sxs-lookup"><span data-stu-id="94dda-105">To set up reports for VAT</span></span>  

1.  <span data-ttu-id="94dda-106">Wählen Sie das Symbol ![Suche nach Seite oder Bericht](../../media/ui-search/search_small.png "Symbol „Suche nach Seite oder Bericht“"), geben Sie **Berichtsauswahl - MwSt.** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="94dda-106">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Selections VAT**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="94dda-107">Auf der Seite **Berichtsauswahl - MwSt.** im Feld **Verbrauch**, wählen Sie die Art des Belegs aus, für die Sie Berichte festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="94dda-107">On the **Report Selection – VAT** page, in the **Usage** field, select the type of document that you want to specify reports for.</span></span> <span data-ttu-id="94dda-108">Dieses umfasst die MwSt.-Abrechnung und den MwSt.-Abrechnungsplan.</span><span class="sxs-lookup"><span data-stu-id="94dda-108">This includes the VAT statement and the VAT statement schedule.</span></span>  

3.  <span data-ttu-id="94dda-109">Geben Sie den Bericht oder den Batchauftrag an, die ausgeführt werden müssen, wenn ein Benutzer die Aktivität für die Belegart startet, die Sie im Feld **Verbrauch** angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="94dda-109">Specify the report or batch job that must run when a user starts the activity for the document type that you specified in the **Usage** field.</span></span> <span data-ttu-id="94dda-110">Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="94dda-110">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="94dda-111">Feld</span><span class="sxs-lookup"><span data-stu-id="94dda-111">Field</span></span>|<span data-ttu-id="94dda-112">Description</span><span class="sxs-lookup"><span data-stu-id="94dda-112">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="94dda-113">**Reihenfolge**</span><span class="sxs-lookup"><span data-stu-id="94dda-113">**Sequence**</span></span>|<span data-ttu-id="94dda-114">Gibt an, wo in der Druckreihenfolge ein Bericht steht.</span><span class="sxs-lookup"><span data-stu-id="94dda-114">Specifies where a report is in the printing order.</span></span>|  
    |<span data-ttu-id="94dda-115">**Berichts-ID**</span><span class="sxs-lookup"><span data-stu-id="94dda-115">**Report ID**</span></span>|<span data-ttu-id="94dda-116">Gibt die ID des Berichts an, der für diese Belegart gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="94dda-116">Specifies the ID of the report that prints for this document type.</span></span>|  
    |<span data-ttu-id="94dda-117">**Berichtsname**</span><span class="sxs-lookup"><span data-stu-id="94dda-117">**Report Name**</span></span>|<span data-ttu-id="94dda-118">Gibt den Namen des Berichts an, der für diese Belegart gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="94dda-118">Specifies the name of the report that prints for this document type.</span></span> <span data-ttu-id="94dda-119">Die **Berichtsname** Feldupdates auf Grundlage der Auswahl im **Berichts-ID**.</span><span class="sxs-lookup"><span data-stu-id="94dda-119">The **Report Name** field updates based on the selection in the **Report ID** field.</span></span>|  

4.  <span data-ttu-id="94dda-120">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="94dda-120">Choose the **OK** button.</span></span>  

### <a name="to-set-up-reports-for-intrastat"></a><span data-ttu-id="94dda-121">Richten Sie Intrastat-Berichte ein.</span><span class="sxs-lookup"><span data-stu-id="94dda-121">To set up reports for Intrastat</span></span>  

1.  <span data-ttu-id="94dda-122">Wählen Sie das Symbol ![Suche nach Seite oder Bericht](../../media/ui-search/search_small.png "Symbol „Suche nach Seite oder Bericht“"), geben Sie **Berichtsauswahl** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="94dda-122">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Selection**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="94dda-123">Auf der Seite **Berichtsauswahl - Intrastat** im Feld **Verbrauch**, wählen Sie die Art des Belegs aus, für die Sie Berichte festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="94dda-123">On the **Report Selection – Intrastat** page, in the **Usage** field, select the type of document that you want to specify reports for.</span></span> <span data-ttu-id="94dda-124">Dieses umfasst die Intrastat-Checkliste und das Intrastat-Formular.</span><span class="sxs-lookup"><span data-stu-id="94dda-124">This includes the Intrastat checklist and Intrastat form.</span></span>  

3.  <span data-ttu-id="94dda-125">Geben Sie den Bericht oder den Batchauftrag an, die ausgeführt werden müssen, wenn ein Benutzer die Aktivität für die Belegart startet, die Sie im Feld **Verbrauch** angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="94dda-125">Specify the report or batch job that must run when a user starts the activity for the document type that you specified in the **Usage** field.</span></span> <span data-ttu-id="94dda-126">Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="94dda-126">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="94dda-127">Feld</span><span class="sxs-lookup"><span data-stu-id="94dda-127">Field</span></span>|<span data-ttu-id="94dda-128">Description</span><span class="sxs-lookup"><span data-stu-id="94dda-128">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="94dda-129">**Reihenfolge**</span><span class="sxs-lookup"><span data-stu-id="94dda-129">**Sequence**</span></span>|<span data-ttu-id="94dda-130">Gibt an, wo in der Druckreihenfolge ein Bericht steht.</span><span class="sxs-lookup"><span data-stu-id="94dda-130">Specifies where a report is in the printing order.</span></span>|  
    |<span data-ttu-id="94dda-131">**Berichts-ID**</span><span class="sxs-lookup"><span data-stu-id="94dda-131">**Report ID**</span></span>|<span data-ttu-id="94dda-132">Gibt die ID des Berichts an, der für diese Belegart gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="94dda-132">Specifies the ID of the report that prints for this document type.</span></span>|  
    |<span data-ttu-id="94dda-133">**Berichtsname**</span><span class="sxs-lookup"><span data-stu-id="94dda-133">**Report Name**</span></span>|<span data-ttu-id="94dda-134">Gibt den Namen des Berichts an, der für diese Belegart gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="94dda-134">Specifies the name of the report that prints for this document type.</span></span> <span data-ttu-id="94dda-135">Die **Berichtsname** Feldupdates auf Grundlage der Auswahl im **Berichts-ID**.</span><span class="sxs-lookup"><span data-stu-id="94dda-135">The **Report Name** field updates based on the selection in the **Report ID** field.</span></span>|  

4.  <span data-ttu-id="94dda-136">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="94dda-136">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="94dda-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94dda-137">See Also</span></span>  
[<span data-ttu-id="94dda-138">Exportieren und Drucken von Intrastat-Berichten</span><span class="sxs-lookup"><span data-stu-id="94dda-138">Export and Print Intrastat Reports</span></span>](how-to-export-and-print-intrastat-reports.md)  
[<span data-ttu-id="94dda-139">MwSt.-Abrechnung</span><span class="sxs-lookup"><span data-stu-id="94dda-139">VAT Reporting</span></span>](vat-reporting.md)
