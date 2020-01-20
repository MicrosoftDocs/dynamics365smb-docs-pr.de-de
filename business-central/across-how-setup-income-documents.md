---
title: Einrichten von eingehenden Belegen| Microsoft Docs
description: Verwenden Sie die Funktion der eingehenden Belege, um elektronische Belege zu erstellen, verwalten Sie OCRaufgaben, importieren Sie Rechnungen und wandeln Sie Bilddateien um.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 12/09/2019
ms.author: sgroespe
ms.openlocfilehash: e67ca1c0b26d7e4a81e53854ca31efc64a366c3f
ms.sourcegitcommit: 3d128a00358668b3fdd105ebf4604ca4e2b6743c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2910492"
---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="5cccf-103">Einrichten von eingehenden Belegen</span><span class="sxs-lookup"><span data-stu-id="5cccf-103">Set Up Incoming Documents</span></span>
<span data-ttu-id="5cccf-104">Wenn Sie Fibu Buch.-Blattzeilen für eingehende Belege erstellen, müssen Sie auf der Seite **Einrichtung für eingehende Belege** angeben, welche Buch.-Blattvorlage und welches Buch.-Blatt verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5cccf-104">If you create general journal lines from incoming document records, you must specify on the **Incoming Documents Setup** page which journal template and batch to use.</span></span>

<span data-ttu-id="5cccf-105">Wenn Sie möchten, dass Benutzer Rechnungen oder Journalzeilen anhand von Eingangsbelegen nur dann erstellen können, wenn diese genehmigt sind, müssen Sie Workflow-Genehmiger einrichten.</span><span class="sxs-lookup"><span data-stu-id="5cccf-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up workflow approvers.</span></span>

<span data-ttu-id="5cccf-106">Um PDF und Bilddateien in elektronische Dokumente umzuwandeln, die in Dokumentdatensätze in Project [!INCLUDE[d365fin](includes/d365fin_md.md)] konvertiert werden, müssen Sie die OCR-Funktion einrichten und den Dienst aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5cccf-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span>

<span data-ttu-id="5cccf-107">Wenn die Funktion für eingehende Belege eingerichtet ist, können Sie verschiedene Funktionen zum Überprüfen von Ausgabenbelegen, Verwalten von OCR-Aufgaben und Konvertieren von eingehenden Belegen, manuell oder automatisch, in den entsprechenden Belegen oder Buch.-Blattzeilen verwenden.</span><span class="sxs-lookup"><span data-stu-id="5cccf-107">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="5cccf-108">Die externen Dateien können jeder Prozessphase zugeordnet werden, auch gebuchten Belegen und den resultierenden Kreditoren-, Debitoren- und Sachposten.</span><span class="sxs-lookup"><span data-stu-id="5cccf-108">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="5cccf-109">Weitere Informationen finden Sie unter [Eingehende Belege verarbeiten](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="5cccf-109">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="5cccf-110">So richten Sie die Funktion für eingehende Belege ein</span><span class="sxs-lookup"><span data-stu-id="5cccf-110">To set up the Incoming Documents feature</span></span>
1. <span data-ttu-id="5cccf-111">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Eingehenden Beleg einrichten** ein, und wählen Sie dann den zugehörigen Link.</span><span class="sxs-lookup"><span data-stu-id="5cccf-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="5cccf-112">Füllen Sie die Felder bei Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="5cccf-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="5cccf-113">So richten Sie Genehmiger für eingehende Belege ein</span><span class="sxs-lookup"><span data-stu-id="5cccf-113">To set up approvers of incoming document records</span></span>
<span data-ttu-id="5cccf-114">Genehmiger von eingehenden Belegen müssen als Genehmigungsworkflow-Benutzer eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="5cccf-114">Approvers of incoming documents must be set up as approval workflow users.</span></span>

<span data-ttu-id="5cccf-115">Bevor Sie Workflows erstellen können, die Genehmigungsschritte betreffen, müssen Sie die Workflowbenutzer einrichten, die von den Genehmigungsprozessen betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="5cccf-115">Before you can create workflows that involve approval steps, you must set up the workflow users who are involved in approval processes.</span></span> <span data-ttu-id="5cccf-116">Auf der Seite **Genehmigungsbenutzereinrichtung** müssen Sie zusätzlich Grenzbeträge für bestimmte Arten von Anforderungen festlegen und Ersatzgenehmiger definieren, an die Genehmigungsanforderungen delegiert werden, wenn der ursprüngliche Genehmiger abwesend ist.</span><span class="sxs-lookup"><span data-stu-id="5cccf-116">On the **Approval User Setup** page, you also set amount limits for specific types of requests and define substitute approvers to whom approval requests are delegated when the original approver is absent.</span></span> <span data-ttu-id="5cccf-117">Weitere Informationen finden Sie unter [Einrichten von Genehmigungsbenutzern.](across-how-to-set-up-approval-users.md)</span><span class="sxs-lookup"><span data-stu-id="5cccf-117">For more information, see [Set Up Approval Users](across-how-to-set-up-approval-users.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="5cccf-118">So richten Sie einen OCR-Service ein</span><span class="sxs-lookup"><span data-stu-id="5cccf-118">To set up an OCR service</span></span>
1. <span data-ttu-id="5cccf-119">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **OCR-Serviceeinrichtung** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="5cccf-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="5cccf-120">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="5cccf-120">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="5cccf-121">Sie informieren Daten werden verschlüsselt automatisch an.</span><span class="sxs-lookup"><span data-stu-id="5cccf-121">You login data is automatically encrypted.</span></span>

## <a name="see-also"></a><span data-ttu-id="5cccf-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5cccf-122">See Also</span></span>
[<span data-ttu-id="5cccf-123">Eingehende Belege verarbeiten</span><span class="sxs-lookup"><span data-stu-id="5cccf-123">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="5cccf-124">Eingehende Belege</span><span class="sxs-lookup"><span data-stu-id="5cccf-124">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="5cccf-125">Einkauf</span><span class="sxs-lookup"><span data-stu-id="5cccf-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="5cccf-126">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5cccf-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
