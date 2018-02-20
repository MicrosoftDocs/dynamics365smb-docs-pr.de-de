---
title: "Definieren, welche eingehenden Dokumente Sie sehen möchten| Microsoft Docs"
description: "Regulieren der Standardansicht aus eingehenden Belege, wie Erechnungen, um die Übersicht verarbeiteten und nicht verarbeiteten Datensätzen zu verbessern."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2016
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 65f3c14b29a5fcf7f855d7ea183445cf2fc1bd95
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="manage-many-incoming-document-records"></a><span data-ttu-id="bcad4-103">Mehrere eingehende Belegdatensätze verwalten</span><span class="sxs-lookup"><span data-stu-id="bcad4-103">Manage Many Incoming Document Records</span></span>
<span data-ttu-id="bcad4-104">Wenn Sie eingehende Belegdatensätze verarbeiten, erhöht sich die Anzahl der Zeilen im Fenster **Eingehende Dokumente** möglicherweise so, dass Sie die Übersicht verlieren.</span><span class="sxs-lookup"><span data-stu-id="bcad4-104">As you create or process incoming document records, the number of lines in the **Incoming Documents** window may grow to an extent where you lose overview.</span></span> <span data-ttu-id="bcad4-105">Daher können Sie eingehende Belegdatensätze auf "Verarbeitet" festlegen, um sie aus der Standardansicht zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="bcad4-105">Therefore, you can set incoming document records to Processed to remove them from the default view.</span></span> <span data-ttu-id="bcad4-106">Wenn Sie die Aktion **Alle anzeigen** auswählen, können Sie sowohl verarbeitete als auch nicht verarbeitete Datensätze anzeigen.</span><span class="sxs-lookup"><span data-stu-id="bcad4-106">When you choose the **Show All** action, you can view both processed and unprocessed records.</span></span>

> [!NOTE]  
>   <span data-ttu-id="bcad4-107">Sie können in eingehenden Belegdatensätzen, die auf "Verarbeitet" gesetzt wurden, keine Informationen bearbeiten, Dateien hinzufügen oder andere Prozesse ausführen.</span><span class="sxs-lookup"><span data-stu-id="bcad4-107">You cannot edit information, attach files, or perform other processes on incoming document records that are set to Processed.</span></span> <span data-ttu-id="bcad4-108">Sie müssen sie zuerst auf "Nicht verarbeitet" festlegen.</span><span class="sxs-lookup"><span data-stu-id="bcad4-108">You must first set it to Unprocessed.</span></span>

<span data-ttu-id="bcad4-109">Das Kontrollkästchen **Verarbeitet** ist automatisch bei eingehenden Belegdatensätzen aktiviert, die verarbeitet wurden, aber Sie können das Kontrollkästchen auch manuell aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="bcad4-109">The **Processed** check box is automatically selected on incoming document records that have been processed, but you can also select or deselect the check box manually.</span></span> <span data-ttu-id="bcad4-110">Abhängig von Ihrem Geschäftsprozess wird ein Datensatz möglicherweise verarbeitet, wenn ein zugehöriger Beleg dafür erstellt oder eine Datei angehängt wurde.</span><span class="sxs-lookup"><span data-stu-id="bcad4-110">Depending on your business process, an incoming document record may be processed when a related document has been created for it or a file has been attached.</span></span>

> [!NOTE]  
>   <span data-ttu-id="bcad4-111">Wenn Sie das Fenster **Eingehende Dokumente** innerhalb der Aktion **Meine eingehenden Dokumente** im Rollencenter öffnen, werden nur nicht verarbeitete Belege standardmäßig angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bcad4-111">When you open the **Incoming Documents** window with the **My Incoming Documents** action on the Role Center, only unprocessed incoming document records are shown by default.</span></span> <span data-ttu-id="bcad4-112">Dies wird in diesem Thema als "Standardansicht" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="bcad4-112">This is referred to in this topic as "the default view".</span></span>

## <a name="to-remove-incoming-document-records-from-the-default-view"></a><span data-ttu-id="bcad4-113">So entfernen Sie eingehende Belegdatensätze aus der Standardansicht</span><span class="sxs-lookup"><span data-stu-id="bcad4-113">To remove incoming document records from the default view</span></span>
1. <span data-ttu-id="bcad4-114">Im Fenster **Eingehende Dokumente** wählen Sie eine oder mehrere Zeilen für eingehende Datensätze, die Sie von der Standardansicht entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="bcad4-114">In the **Incoming Documents** window, select one or more lines for incoming document records that you want to remove from the default view.</span></span>
2. <span data-ttu-id="bcad4-115">Wählen Sie die Aktion **Auf "Verarbeitet" setzen** aus.</span><span class="sxs-lookup"><span data-stu-id="bcad4-115">Choose the **Set to Processed** action.</span></span>

    <span data-ttu-id="bcad4-116">Die eingehenden Belegdatensätze werden aus der Standardansicht entfernt, und das Kontrollkästchen **Verarbeitet** wird in den Zeilen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="bcad4-116">The incoming document records are removed from the default view, and the **Processed** check box is selected on the lines.</span></span>

> [!NOTE]  
>   <span data-ttu-id="bcad4-117">Sie können diese Aktion für einzelne Datensätze im Fenster **Eingehende Belegkarte** durchführen.</span><span class="sxs-lookup"><span data-stu-id="bcad4-117">You can also perform this action for the individual record in the **Incoming Document Card** window.</span></span>

## <a name="to-view-all-incoming-document-records"></a><span data-ttu-id="bcad4-118">So zeigen Sie alle eingehende Belegdatensätze an</span><span class="sxs-lookup"><span data-stu-id="bcad4-118">To view all incoming document records</span></span>
1. <span data-ttu-id="bcad4-119">Wählen Sie im Fenster **Eingehende Dokumente** die Aktion **Alle anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="bcad4-119">In the **Incoming Documents** window, choose the **Show All** action.</span></span>

<span data-ttu-id="bcad4-120">Alle eingehenden Belegdatensätze einschließlich derer, bei denen das Kontrollkästchen **Verarbeitet** nicht aktiviert ist, werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bcad4-120">All incoming document records are displayed, including those where the **Processed** check box is not selected.</span></span>

## <a name="to-add-incoming-document-records-to-the-default-view"></a><span data-ttu-id="bcad4-121">So fügen Sie eingehende Belegdatensätze der Standardansicht hinzu</span><span class="sxs-lookup"><span data-stu-id="bcad4-121">To add incoming document records to the default view</span></span>
1. <span data-ttu-id="bcad4-122">Wählen Sie im Fenster **Eingehende Dokumente** die Aktion **Alle anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="bcad4-122">In the **Incoming Documents** window, choose the **Show All** action.</span></span>
2. <span data-ttu-id="bcad4-123">Wählen Sie eine oder mehrere Zeilen für eingehende Belegdatensätzeaus, die in der Standardansicht angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bcad4-123">Select one or more lines for incoming document records that you want to appear in the default view.</span></span>
3. <span data-ttu-id="bcad4-124">Wählen Sie die Aktion **Auf "Nicht verarbeitet" setzen** aus.</span><span class="sxs-lookup"><span data-stu-id="bcad4-124">Choose the **Set to Unprocessed** action.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="bcad4-125">Sie können diese Aktion für einzelne Datensätze im Fenster **Eingehende Belegkarte** durchführen.</span><span class="sxs-lookup"><span data-stu-id="bcad4-125">You can also perform this action for the individual record in the **Incoming Document Card** window.</span></span>

## <a name="see-also"></a><span data-ttu-id="bcad4-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bcad4-126">See Also</span></span>
[<span data-ttu-id="bcad4-127">Eingehende Dokumente verarbeiten</span><span class="sxs-lookup"><span data-stu-id="bcad4-127">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="bcad4-128">Eingehende Belege</span><span class="sxs-lookup"><span data-stu-id="bcad4-128">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="bcad4-129">Einkauf</span><span class="sxs-lookup"><span data-stu-id="bcad4-129">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="bcad4-130">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bcad4-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

