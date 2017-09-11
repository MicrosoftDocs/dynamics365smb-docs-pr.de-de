---
title: Einrichten von Berichten, um auf bestimmte Druckern zu drucken | Microsoft Docs
description: "Weitere Informationen zum Definieren eines Druckers für eine Bericht und zur Nutzung des Druckerauswahlfensters."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 106ad2acf2703e8182033a43a39c693a8b060d8f
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2017

---
# <a name="specify-printer-selection-for-reports"></a><span data-ttu-id="0e2e0-103">Angeben der Druckerauswahl für Berichte</span><span class="sxs-lookup"><span data-stu-id="0e2e0-103">Specify Printer Selection for Reports</span></span>
<span data-ttu-id="0e2e0-104">Diese Seite ist leer, da Sie bestimmte Drucker für bestimmte Berichte noch nicht einrichten können.</span><span class="sxs-lookup"><span data-stu-id="0e2e0-104">This page is empty because you cannot yet set up specific printers for specific reports.</span></span> <span data-ttu-id="0e2e0-105">Wir arbeiten an der Lösung des Problems.</span><span class="sxs-lookup"><span data-stu-id="0e2e0-105">We are working on solving this.</span></span>

<span data-ttu-id="0e2e0-106">Wenn Sie einen Bericht drucken möchten, müssen Sie den Bericht als PDF-Dokument zuerst herunterladen, indem Sie die Schaltfläche **Senden an** auswählen.</span><span class="sxs-lookup"><span data-stu-id="0e2e0-106">In the meantime, when you want to print a report you have to download the report as a PDF document first by choosing the **Send to** button.</span></span> <span data-ttu-id="0e2e0-107">Dann wählen Sie die Art der Datei aus, um den Bericht herunterzuladen und wählen Sie **PDF-Dokument** aus.</span><span class="sxs-lookup"><span data-stu-id="0e2e0-107">Then you select the type of file to download the report as, and here you should pick **PDF Document**.</span></span> <span data-ttu-id="0e2e0-108">Jetzt können Sie entweder das PDF-Dokument sofort öffnen und es drucken, oder speichern Sie es, um später zu drucken.</span><span class="sxs-lookup"><span data-stu-id="0e2e0-108">Now, you can either open the PDF document right-away and print it, or save it and print it later.</span></span>

<!--

You can set up reports so that they must be printed on a specific printer. The following are some uses of printer selection:

- You can print reports on special company letterhead.
- You can print reports on different paper sizes.
- You can print reports on the default printer of a specified employee.

You use the **Printer Selections** window to set different values to obtain different output. If you set a specific printer selection, then it takes precedence over a more general printer selection. For example, you can set a printer selection that has values in the **User ID**, **Report ID**, and **Printer Name** fields. This printer selection takes precedence over a printer selection that has blank entries in the **User ID** or **Report ID** fields.

The following table describes the combination of values to specify when you set up printer selections for a report.

|To                                                 |Set the following values                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Print a report to a specific printer for all users |Specify values in the **Report ID** and **Printer Name** fields and leave the **User ID** field blank.|
|Print all reports to a specific printer for a specific user|Specify values in the **User ID** and **Printer Name** fields and leave the **Report ID** field blank.|
|Set the default printer for all reports|Specify a value in the **Printer Name** field and leave the **User ID** and **Report ID** fields blank.|
|Print a specific report to the user’s default printer|Specify a value in the **Report ID** field and leave the **Printer Name** and **User ID** fields blank.|
|Print a specific report to a specific printer for a specific user|Specify values in all three fields.|
-->

## <a name="see-also"></a><span data-ttu-id="0e2e0-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e2e0-109">See Also</span></span>
<span data-ttu-id="0e2e0-110">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0e2e0-110">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="0e2e0-111">Vorgehensweise: Ausführen von Stapelverarbeitungen</span><span class="sxs-lookup"><span data-stu-id="0e2e0-111">How to: Run Batch Jobs</span></span>](ui-how-run-batch-jobs.md)  
[<span data-ttu-id="0e2e0-112">Gewusst wie: Senden von Belegen über E-Mail</span><span class="sxs-lookup"><span data-stu-id="0e2e0-112">How to: Send Documents by Email</span></span>](ui-how-send-documents-email.md)  

