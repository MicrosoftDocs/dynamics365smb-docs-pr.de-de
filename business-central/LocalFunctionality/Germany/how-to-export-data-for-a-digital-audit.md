---
title: "Wie Sie Daten für eine Digital-Überwachung exportieren"
description: "Sie können Finanz- und Steuerdaten exportieren entsprechend dem Prozess für Datenzugriff und Testbarkeit von digitalen Dokumenten (GDPdU), der auf deutschen Steuergesetzen basiert. Zudem können verschiedene Optionen in eine XML-Datei eingeschlossen werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 12931d738bf85947f12f7e565bfb93311f50083b
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="export-data-for-a-digital-audit"></a><span data-ttu-id="49a5b-104">Wie Sie Daten für eine Digital-Überwachung exportieren</span><span class="sxs-lookup"><span data-stu-id="49a5b-104">Export Data for a Digital Audit</span></span>
<span data-ttu-id="49a5b-105">Sie können Finanz- und Steuerdaten exportieren entsprechend dem Prozess für Datenzugriff und Testbarkeit von digitalen Dokumenten (GDPdU), der auf deutschen Steuergesetzen basiert.</span><span class="sxs-lookup"><span data-stu-id="49a5b-105">You can export financial data and tax data according to the process for digital audits (GoBD/GDPdU).</span></span> <span data-ttu-id="49a5b-106">Zudem können verschiedene Optionen in eine XML-Datei eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="49a5b-106">You can also select various options to be included in an XML file.</span></span>  

<span data-ttu-id="49a5b-107">Falls es keine Daten zum Exportieren gibt, erstellt [!INCLUDE[d365fin](../../includes/d365fin_md.md)] leere Dateien.</span><span class="sxs-lookup"><span data-stu-id="49a5b-107">If there is no data to export, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] creates empty files.</span></span>  

### <a name="to-export-data-for-a-digital-audit"></a><span data-ttu-id="49a5b-108">Wie Sie Daten für eine Digital-Überwachung exportieren</span><span class="sxs-lookup"><span data-stu-id="49a5b-108">To export data for a digital audit</span></span>

1.  <span data-ttu-id="49a5b-109">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen")und geben **Geschäftsdaten exportieren** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="49a5b-109">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Export Business Data**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="49a5b-110">Füllen Sie im Stapelverarbeitungsauftrag **Datenexport** im Inforegister **Optionen** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="49a5b-110">In the **Data Export** window, on the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="49a5b-111">Option</span><span class="sxs-lookup"><span data-stu-id="49a5b-111">Option</span></span>|<span data-ttu-id="49a5b-112">Description</span><span class="sxs-lookup"><span data-stu-id="49a5b-112">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="49a5b-113">**Startdatum**</span><span class="sxs-lookup"><span data-stu-id="49a5b-113">**Starting Date**</span></span>|<span data-ttu-id="49a5b-114">Gibt das Startdatum des Berichts für den Datenexport an.</span><span class="sxs-lookup"><span data-stu-id="49a5b-114">Specifies the start date for the data export.</span></span><br /><br /> <span data-ttu-id="49a5b-115">**HINWEIS:** Wenn die Datenenexportquell Periodenfelder einschließt, wird das Startdatum und das Enddatum als Filterwert für die Periodenfelder verwendet.</span><span class="sxs-lookup"><span data-stu-id="49a5b-115">**NOTE:** If the data export source includes period fields, the start date and the end date are used as filter values for the period fields.</span></span>|  
    |<span data-ttu-id="49a5b-116">**Enddatum**</span><span class="sxs-lookup"><span data-stu-id="49a5b-116">**Ending Date**</span></span>|<span data-ttu-id="49a5b-117">Gibt das Enddatum des Berichts für den Datenexport an.</span><span class="sxs-lookup"><span data-stu-id="49a5b-117">Specifies the end date for the data export.</span></span>|  
    |<span data-ttu-id="49a5b-118">**Abschlussdatum einschließen**</span><span class="sxs-lookup"><span data-stu-id="49a5b-118">**Include Closing Date**</span></span>|<span data-ttu-id="49a5b-119">Gibt an, ob der Datenexport das Ultimodatum der Periode enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="49a5b-119">Specifies if the data export must include the closing date for the period.</span></span>|  

3.  <span data-ttu-id="49a5b-120">Wählen Sie im Inforegister **Datenexport - Datensatzdefinition** die entsprechenden Filter aus, um den Datenexport zu identifizieren und Daten exportieren Datensatztyp.</span><span class="sxs-lookup"><span data-stu-id="49a5b-120">On the **Data Export Record Definition** FastTab, select the appropriate filters to identify the data export and data export record type.</span></span> <span data-ttu-id="49a5b-121">Weitere Informationen finden Sie unter [Prozess für Digital-Überwachung (/GoBD GDPdU)](process-for-digital-audits.md).</span><span class="sxs-lookup"><span data-stu-id="49a5b-121">For more information, see [Process for Digital Audits (GoBD/GDPdU)](process-for-digital-audits.md).</span></span>  

4.  <span data-ttu-id="49a5b-122">Um Daten zu exportieren, wählen Sie die Schaltfläche **OK**, um den Export zu starten.</span><span class="sxs-lookup"><span data-stu-id="49a5b-122">To export the data, choose the **OK** button.</span></span>  

    > [!WARNING]  
    >  <span data-ttu-id="49a5b-123">Während des Exports werden alle vorhandenen Dateien, einschließlich der Protokolldatei, überschrieben.</span><span class="sxs-lookup"><span data-stu-id="49a5b-123">During the export, any existing files, including the log file, will be overwritten.</span></span> <span data-ttu-id="49a5b-124">Wenn Sie identische Daten mehrfach exportieren, werden die Dateien aus dem ersten Export überschrieben</span><span class="sxs-lookup"><span data-stu-id="49a5b-124">If you export the same data twice, the files from the first export are overwritten</span></span>  

 <span data-ttu-id="49a5b-125">Sie werden informiert, wenn der Export abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="49a5b-125">You will be notified when the export completes.</span></span> <span data-ttu-id="49a5b-126">Wenn Sie den Export abbrechen oder das Fenster schließen, werden Sie informiert, dass der Export abgeschlossen ist, aber der Protokollordner bleibt leer.</span><span class="sxs-lookup"><span data-stu-id="49a5b-126">If you cancel the export, or if you close the window, you will also be notified that the export has completed, but the log folder will be empty.</span></span> <span data-ttu-id="49a5b-127">Abhängig von Ihrer Konfiguration, wurden eventuell einige Dateien exportiert, aber der Export ist möglicherweise noch nicht abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="49a5b-127">However, depending on your configuration, some files may have been exported, but the export might not be complete.</span></span>  

## <a name="see-also"></a><span data-ttu-id="49a5b-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49a5b-128">See Also</span></span>  
[<span data-ttu-id="49a5b-129">Prozess für Digital-Überwachung (/GoBD GDPdU)</span><span class="sxs-lookup"><span data-stu-id="49a5b-129">Process for Digital Audits (GoBD/GDPdU)</span></span>](process-for-digital-audits.md)

