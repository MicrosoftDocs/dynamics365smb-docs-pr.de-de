---
title: Suche nach Belegen ohne Dateianhänge| Microsoft Docs
Description: Sie können nach Sachposten für gebuchte Einkaufs- und Verkaufsbelege suchen, die keine eingehenden elektronische Belege haben, wie importierte Rechnungen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: eecce08613d553a0abbe45c6653a0719c15c6910
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2301684"
---
# <a name="find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="e38c0-103">So finden Sie gebuchte Belege ohne zugehörige eingehende Belege</span><span class="sxs-lookup"><span data-stu-id="e38c0-103">Find Posted Documents without Incoming Document Records</span></span>
<span data-ttu-id="e38c0-104">Auf der Seiten **Kontenplan** und **Sachposten** können Sie eine Suchfunktion verwenden, um Sachposten für gebuchte Einkaufs- und Verkaufsbelege zu finden, für die keine eingehende Belege vorhanden sind, und dann zentral eine Verknüpfung zu vorhandenen Datensätzen herstellen oder neue mit angefügten Belegdateien erstellen.</span><span class="sxs-lookup"><span data-stu-id="e38c0-104">From the **Chart of Accounts** and **General Ledger Entries** pages, you can use a search function to find general ledger entries for posted purchase and sales documents that do not have incoming document records and then centrally link to existing records or create new ones with attached document files.</span></span>

## <a name="to-find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="e38c0-105">So finden Sie gebuchte Belege ohne zugehörige eingehende Belege</span><span class="sxs-lookup"><span data-stu-id="e38c0-105">To find posted documents without incoming document records</span></span>
1. <span data-ttu-id="e38c0-106">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontenplan** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="e38c0-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="e38c0-107">Wählen Sie eine Zeile für ein Sachkonto aus, für dessen Sachposten Sie gebuchte Einkaufs- und Verkaufsbelege abrufen möchten, zu denen keine eingehenden Belege vorhanden sind, und wählen Sie dann die Aktion **Gebuchte Belege ohne eingehenden Beleg**.</span><span class="sxs-lookup"><span data-stu-id="e38c0-107">Select a line for a G/L account for whose general ledger entries you want to see posted purchase and sales documents without incoming document records, and then choose the **Posted Documents without Incoming Document** action.</span></span>
3. <span data-ttu-id="e38c0-108">Wählen Sie die Aktion **Posten** aus.</span><span class="sxs-lookup"><span data-stu-id="e38c0-108">Alternatively, choose the **Ledger Entries** action.</span></span>
4. <span data-ttu-id="e38c0-109">Wählen Sie auf der Seite **Sachposten** die Aktion **Gebuchte Belege ohne eingehende Belege** aus.</span><span class="sxs-lookup"><span data-stu-id="e38c0-109">On the **General Ledger Entries** page, choose the **Posted Documents without Incoming Documents** action.</span></span>

<span data-ttu-id="e38c0-110">Daraufhin wird die Seite **Gebuchte Belege ohne eingehenden Beleg** geöffnet, das die gebuchten Einkaufs- und Verkaufsbelege ohne zugehörige eingehende Belege enthält, die von Sachposten auf dem Sachkonto dargestellt werden, für das Sie das Fenster geöffnet haben.</span><span class="sxs-lookup"><span data-stu-id="e38c0-110">The **Posted Documents without Incoming Document** page opens showing posted purchase and sales documents without incoming document records represented by general ledger entries on the G/L account that you opened the page for.</span></span> <span data-ttu-id="e38c0-111">Die Seite kann maximal 1000 Zeilen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e38c0-111">The page can show a maximum of 1000 lines.</span></span> <span data-ttu-id="e38c0-112">Standardmäßig enthält das Feld **Datumsfilter** daher einen Filter, der die Anzeige auf Einträge beschränkt, deren Buchungsdatum zwischen dem Beginn der Buchhaltungsperiode und dem Arbeitsdatum liegt.</span><span class="sxs-lookup"><span data-stu-id="e38c0-112">By default, the **Date Filter** field therefore contains a filter that limits the lines to entries with posting dates from the beginning of the accounting period to the work date.</span></span>

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a><span data-ttu-id="e38c0-113">So verknüpfen Sie gefundene Dokumente mit vorhandenen eingehenden Belegen</span><span class="sxs-lookup"><span data-stu-id="e38c0-113">To connect found documents to existing incoming document records</span></span>
1. <span data-ttu-id="e38c0-114">Wählen Sie auf der Seite **Gebuchte Belege ohne eingehenden Beleg** die Zeile für einen gebuchten Beleg aus, den Sie mit einem vorhandenen eingehenden Beleg verknüpfen möchten, und wählen Sie dann die Aktion **Eingehenden Beleg auswählen** aus.</span><span class="sxs-lookup"><span data-stu-id="e38c0-114">On the **Posted Documents without Incoming Document** page, select the line for a posted document that you want to connect to an existing incoming document record, and then choose the **Select Incoming Document** action.</span></span>
2. <span data-ttu-id="e38c0-115">Wählen Sie auf der Seite **Eingehende Belege** den eingehenden Beleg aus, den Sie der gefundenen Buchung zuordnen möchten, und klicken Sie anschließend auf die Schaltfläche **OK**.</span><span class="sxs-lookup"><span data-stu-id="e38c0-115">On the **Incoming Documents** page, select the incoming document record that you want to connect to posted document found, and then choose the **OK** button.</span></span>
3. <span data-ttu-id="e38c0-116">Auf der Seite **Gebuchte Belege ohne eingehenden Beleg** wird der gewählte eingehende Beleg nun mit dem gebuchten Beleg verknüpft und in der Infobox **Eingehender Beleg** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e38c0-116">On the **Posted Documents without Incoming Document** page, the selected incoming document record is now connected to the posted document, as you can see in the **Incoming Document Files** FactBox.</span></span>

<span data-ttu-id="e38c0-117">Wenn die Seite **Eingehende Belege** keinen relevanten eingehenden Beleg, können Sie einen erstellen.</span><span class="sxs-lookup"><span data-stu-id="e38c0-117">If a relevant incoming document record does not exist on the **Incoming Documents** page, then you can create it.</span></span> <span data-ttu-id="e38c0-118">Weitere Informationen finden Sie unter [So geht's: Eingehende Belege erstellen](across-how-create-income-document-records.md).</span><span class="sxs-lookup"><span data-stu-id="e38c0-118">For more information, see [Create Incoming Document Records](across-how-create-income-document-records.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e38c0-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e38c0-119">See Also</span></span>
[<span data-ttu-id="e38c0-120">Eingehende Belege verarbeiten</span><span class="sxs-lookup"><span data-stu-id="e38c0-120">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="e38c0-121">Eingehende Belege</span><span class="sxs-lookup"><span data-stu-id="e38c0-121">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="e38c0-122">Einkauf</span><span class="sxs-lookup"><span data-stu-id="e38c0-122">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="e38c0-123">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e38c0-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
