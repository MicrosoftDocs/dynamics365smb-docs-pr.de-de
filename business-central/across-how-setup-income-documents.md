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
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7e99f4b33767a1bdea7b942d1b183edbacc829ac
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "932741"
---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="7cc6e-103">Einrichten von eingehenden Belegen</span><span class="sxs-lookup"><span data-stu-id="7cc6e-103">Set Up Incoming Documents</span></span>
<span data-ttu-id="7cc6e-104">Wenn Sie Fibu Buch.-Blattzeilen für eingehende Belegdatensätze erstellen, müssen Sie auf der Seite **Einrichtung für eingehende Belege** angeben, welche Buch.-Blattvorlage und welches Buch.-Blatt verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7cc6e-104">If you create general journal lines from incoming document records, you must specify on the **Incoming Documents Setup** page which journal template and batch to use.</span></span>

<span data-ttu-id="7cc6e-105">Wenn Sie nicht möchten, dass Benutzer Rechnungen oder Fibu Buch.-Blattzeilen anhand von eingehende Belegdatensätzen erstellen können, ausser, wenn diese genehmigt sind, müssen Sie Genehmiger auf der Seite **Genehmiger für eingehendes Dokument** einrichten.</span><span class="sxs-lookup"><span data-stu-id="7cc6e-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up approvers on the **Incoming Document Approvers** page.</span></span>

<span data-ttu-id="7cc6e-106">Um PDF und Bilddateien in elektronische Dokumente umzuwandeln, die in Dokumentdatensätze in Project [!INCLUDE[d365fin](includes/d365fin_md.md)] konvertiert werden, müssen Sie die OCR-Funktion einrichten und den Dienst aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7cc6e-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span>

<span data-ttu-id="7cc6e-107">Wenn die Funktion für Eingangsbelege eingerichtet ist, können Sie verschiedene Funktionen zum Überprüfen von Ausgabenbelegen, Verwalten von OCR-Aufgaben und Konvertieren von Eingangsbelegen, manuell oder automatisch, in den entsprechenden Belegen oder Buch.-Blattzeilen verwenden.</span><span class="sxs-lookup"><span data-stu-id="7cc6e-107">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="7cc6e-108">Die externen Dateien können jeder Prozessphase zugeordnet werden, auch gebuchten Belegen und den resultierenden Kreditoren-, Debitoren- und Sachposten.</span><span class="sxs-lookup"><span data-stu-id="7cc6e-108">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="7cc6e-109">Weitere Informationen finden Sie unter [Eingehende Belege verarbeiten](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="7cc6e-109">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="7cc6e-110">So richten Sie die Funktion für Eingangsbelege ein</span><span class="sxs-lookup"><span data-stu-id="7cc6e-110">To set up the Incoming Documents feature</span></span>
1. <span data-ttu-id="7cc6e-111">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Eingehende Belegeinrichtung** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="7cc6e-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="7cc6e-112">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="7cc6e-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="7cc6e-113">So richten Sie Genehmiger für Eingangsbelege ein</span><span class="sxs-lookup"><span data-stu-id="7cc6e-113">To set up approvers of incoming document records</span></span>
1. <span data-ttu-id="7cc6e-114">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Eingehende Belegeinrichtung** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="7cc6e-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7cc6e-115">Wählen Sie auf der Seite **Einrichtung für eingehende Belege** die Aktion **Genehmiger** aus.</span><span class="sxs-lookup"><span data-stu-id="7cc6e-115">On the **Incoming Documents Setup** page, choose the **Approvers** action.</span></span>

    <span data-ttu-id="7cc6e-116">Auf der Seite **Genehmiger für eingehende Belege** werden alle Benutzer, die in Ihrem Project [!INCLUDE[d365fin](includes/d365fin_md.md)] eingerichtet sind, angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7cc6e-116">The **Incoming Document Approvers** page shows all users that are set up in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
3. <span data-ttu-id="7cc6e-117">Wählen Sie mindestens einen Benutzer aus, der einen eingehenden Beleg genehmigen kann, bevor eine zugehörige Beleg- oder Buch.-Blattzeile erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7cc6e-117">Select one or more users that can approve an incoming document before a related document or journal line can be created.</span></span>

<span data-ttu-id="7cc6e-118">Nachdem Sie Genehmiger auf der Seite **Genehmiger für eingehendes Dokument** eingerichtet haben, können nur diese Benutzer ein eingehendes Dokument genehmigen, wenn auf der Seite **Einrichtung für eingehende Belege** das Kontrollkästchen **Genehmigung zum Erstellen anfordern** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7cc6e-118">When approvers have been set up on the **Incoming Document Approvers** page, only those users can approve an incoming document if the **Require Approval To Create** check box on the **Incoming Documents Setup** page is selected.</span></span>

> [!NOTE]  
>   <span data-ttu-id="7cc6e-119">Diese Genehmigungseinrichtung ist nicht mit den Genehmigungsworkflows verknüpft.</span><span class="sxs-lookup"><span data-stu-id="7cc6e-119">This approval setup is not related to approval workflows.</span></span> <span data-ttu-id="7cc6e-120">Weitere Informationen erhalten Sie unter [Genehmigungsworkflow verwenden](across-how-use-approval-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="7cc6e-120">For more information, see [Use Approval Workflows](across-how-use-approval-workflows.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="7cc6e-121">So richten Sie einen OCR-Service ein</span><span class="sxs-lookup"><span data-stu-id="7cc6e-121">To set up an OCR service</span></span>
1. <span data-ttu-id="7cc6e-122">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **OCR Service einrichten** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="7cc6e-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="7cc6e-123">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="7cc6e-123">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="7cc6e-124">Sie informieren Daten werden verschlüsselt automatisch an.</span><span class="sxs-lookup"><span data-stu-id="7cc6e-124">You login data is automatically encrypted.</span></span>

## <a name="see-also"></a><span data-ttu-id="7cc6e-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7cc6e-125">See Also</span></span>
[<span data-ttu-id="7cc6e-126">Eingehende Belege verarbeiten</span><span class="sxs-lookup"><span data-stu-id="7cc6e-126">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="7cc6e-127">Eingehende Belege</span><span class="sxs-lookup"><span data-stu-id="7cc6e-127">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="7cc6e-128">Einkauf</span><span class="sxs-lookup"><span data-stu-id="7cc6e-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="7cc6e-129">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7cc6e-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
