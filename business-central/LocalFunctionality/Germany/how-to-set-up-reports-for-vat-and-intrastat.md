---
title: 'Gewusst wie: Einrichten von Berichten für MwSt. und Intrastat'
description: In Business Central können Sie festlegen, welche Berichte verwendet werden sollen, um die Dokumente zu erstellen, die Sie an die Behörden, wie beispielsweise die MwSt.-Abrechnung und das Intrastat-Formular übermitteln müssen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 76db929eeab84d089967fa6c007718563b71b3b4
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "922206"
---
# <a name="set-up-reports-for-vat-and-intrastat"></a><span data-ttu-id="79983-103">Richten Sie Berichte für MwSt ein.</span><span class="sxs-lookup"><span data-stu-id="79983-103">Set Up Reports for VAT and Intrastat</span></span>
<span data-ttu-id="79983-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] können Sie festlegen, welche Berichte verwendet werden sollen, um die Dokumente zu erstellen, die Sie an die Behörden, wie beispielsweise die MwSt.-Abrechnung und das Intrastat-Formular übermitteln müssen.</span><span class="sxs-lookup"><span data-stu-id="79983-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can specify which reports to use to create the documents that you must submit to the authorities, such as the VAT statement and the Intrastat form.</span></span>  

### <a name="to-set-up-reports-for-vat"></a><span data-ttu-id="79983-105">Richten Sie MwSt.-Berichte ein.</span><span class="sxs-lookup"><span data-stu-id="79983-105">To set up reports for VAT</span></span>  

1.  <span data-ttu-id="79983-106">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen")Nach Seite oder Bericht suchen und geben **Berichtauswahl MwSt** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="79983-106">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Selections VAT**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="79983-107">Auf der Seite **Berichtsauswahl - MwSt.** im Feld **Verbrauch**, wählen Sie die Art des Belegs aus, für die Sie Berichte festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="79983-107">On the **Report Selection – VAT** page, in the **Usage** field, select the type of document that you want to specify reports for.</span></span> <span data-ttu-id="79983-108">Dieses umfasst die MwSt.-Abrechnung und den MwSt.-Abrechnungsplan.</span><span class="sxs-lookup"><span data-stu-id="79983-108">This includes the VAT statement and the VAT statement schedule.</span></span>  

3.  <span data-ttu-id="79983-109">Geben Sie den Bericht oder den Batchauftrag an, die ausgeführt werden müssen, wenn ein Benutzer die Aktivität für die Belegart startet, die Sie im Feld **Verbrauch** angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="79983-109">Specify the report or batch job that must run when a user starts the activity for the document type that you specified in the **Usage** field.</span></span> <span data-ttu-id="79983-110">Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="79983-110">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="79983-111">Feld</span><span class="sxs-lookup"><span data-stu-id="79983-111">Field</span></span>|<span data-ttu-id="79983-112">Description</span><span class="sxs-lookup"><span data-stu-id="79983-112">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="79983-113">**Reihenfolge**</span><span class="sxs-lookup"><span data-stu-id="79983-113">**Sequence**</span></span>|<span data-ttu-id="79983-114">Gibt an, wo in der Druckreihenfolge ein Bericht steht.</span><span class="sxs-lookup"><span data-stu-id="79983-114">Specifies where a report is in the printing order.</span></span>|  
    |<span data-ttu-id="79983-115">**Berichts-ID**</span><span class="sxs-lookup"><span data-stu-id="79983-115">**Report ID**</span></span>|<span data-ttu-id="79983-116">Gibt die ID des Berichts an, der für diese Belegart gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="79983-116">Specifies the ID of the report that prints for this document type.</span></span>|  
    |<span data-ttu-id="79983-117">**Berichtsname**</span><span class="sxs-lookup"><span data-stu-id="79983-117">**Report Name**</span></span>|<span data-ttu-id="79983-118">Gibt den Namen des Berichts an, der für diese Belegart gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="79983-118">Specifies the name of the report that prints for this document type.</span></span> <span data-ttu-id="79983-119">Die **Berichtsname** Feldupdates auf Grundlage der Auswahl im **Berichts-ID**.</span><span class="sxs-lookup"><span data-stu-id="79983-119">The **Report Name** field updates based on the selection in the **Report ID** field.</span></span>|  

4.  <span data-ttu-id="79983-120">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="79983-120">Choose the **OK** button.</span></span>  

### <a name="to-set-up-reports-for-intrastat"></a><span data-ttu-id="79983-121">Richten Sie Intrastat-Berichte ein.</span><span class="sxs-lookup"><span data-stu-id="79983-121">To set up reports for Intrastat</span></span>  

1.  <span data-ttu-id="79983-122">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen")und geben **Berichtauswahl** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="79983-122">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Selection**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="79983-123">Auf der Seite **Berichtsauswahl - Intrastat** im Feld **Verbrauch**, wählen Sie die Art des Belegs aus, für die Sie Berichte festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="79983-123">On the **Report Selection – Intrastat** page, in the **Usage** field, select the type of document that you want to specify reports for.</span></span> <span data-ttu-id="79983-124">Dieses umfasst die Intrastat-Checkliste und das Intrastat-Formular.</span><span class="sxs-lookup"><span data-stu-id="79983-124">This includes the Intrastat checklist and Intrastat form.</span></span>  

3.  <span data-ttu-id="79983-125">Geben Sie den Bericht oder den Batchauftrag an, die ausgeführt werden müssen, wenn ein Benutzer die Aktivität für die Belegart startet, die Sie im Feld **Verbrauch** angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="79983-125">Specify the report or batch job that must run when a user starts the activity for the document type that you specified in the **Usage** field.</span></span> <span data-ttu-id="79983-126">Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="79983-126">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="79983-127">Feld</span><span class="sxs-lookup"><span data-stu-id="79983-127">Field</span></span>|<span data-ttu-id="79983-128">Description</span><span class="sxs-lookup"><span data-stu-id="79983-128">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="79983-129">**Reihenfolge**</span><span class="sxs-lookup"><span data-stu-id="79983-129">**Sequence**</span></span>|<span data-ttu-id="79983-130">Gibt an, wo in der Druckreihenfolge ein Bericht steht.</span><span class="sxs-lookup"><span data-stu-id="79983-130">Specifies where a report is in the printing order.</span></span>|  
    |<span data-ttu-id="79983-131">**Berichts-ID**</span><span class="sxs-lookup"><span data-stu-id="79983-131">**Report ID**</span></span>|<span data-ttu-id="79983-132">Gibt die ID des Berichts an, der für diese Belegart gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="79983-132">Specifies the ID of the report that prints for this document type.</span></span>|  
    |<span data-ttu-id="79983-133">**Berichtsname**</span><span class="sxs-lookup"><span data-stu-id="79983-133">**Report Name**</span></span>|<span data-ttu-id="79983-134">Gibt den Namen des Berichts an, der für diese Belegart gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="79983-134">Specifies the name of the report that prints for this document type.</span></span> <span data-ttu-id="79983-135">Die **Berichtsname** Feldupdates auf Grundlage der Auswahl im **Berichts-ID**.</span><span class="sxs-lookup"><span data-stu-id="79983-135">The **Report Name** field updates based on the selection in the **Report ID** field.</span></span>|  

4.  <span data-ttu-id="79983-136">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="79983-136">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="79983-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79983-137">See Also</span></span>  
[<span data-ttu-id="79983-138">Exportieren und Drucken von Intrastat-Berichten</span><span class="sxs-lookup"><span data-stu-id="79983-138">Export and Print Intrastat Reports</span></span>](how-to-export-and-print-intrastat-reports.md)  
[<span data-ttu-id="79983-139">MwSt.-Abrechnung</span><span class="sxs-lookup"><span data-stu-id="79983-139">VAT Reporting</span></span>](vat-reporting.md)
