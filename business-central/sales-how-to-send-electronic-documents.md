---
title: Elektronische Belege senden
description: Erfahren Sie, wie man Rechnungen elektronisch sendet.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d547f031d9d33c0d7cd5f8b20398fd7b6dbe0393
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383000"
---
# <a name="send-electronic-documents"></a><span data-ttu-id="4b2ac-103">Elektronische Belege senden</span><span class="sxs-lookup"><span data-stu-id="4b2ac-103">Send Electronic Documents</span></span>

<span data-ttu-id="4b2ac-104">Die allgemeine Version von [!INCLUDE[prod_short](includes/prod_short.md)] unterstützt das Senden von elektronischen Rechnungen und Gutschriften im PEPPOL-Format, einem Format, das von den größten Anbietern von Belegaustauschdiensten unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-104">The generic version of [!INCLUDE[prod_short](includes/prod_short.md)] supports sending electronic invoices and credit memos in the PEPPOL format, a format that the largest document exchange service providers support.</span></span> <span data-ttu-id="4b2ac-105">Ein Anbieter von Belegaustauschdiensten leitet elektronische Belege zwischen Handelspartnern weiter.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-105">A document exchange service provider dispatches electronic documents between trading partners.</span></span> <span data-ttu-id="4b2ac-106">Um Unterstützung für andere elektronische Belegformate zu bieten, verwenden Sie das Datenaustauschframework.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-106">To provide support for other electronic document formats, you use the data exchange framework.</span></span>  

 <span data-ttu-id="4b2ac-107">In der allgemeinen Version von [!INCLUDE[prod_short](includes/prod_short.md)] ist ein vorkonfigurierter Belegaustauschdienst enthalten, der für Ihren Mandanten eingerichtet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-107">In the generic version of [!INCLUDE[prod_short](includes/prod_short.md)], a document exchange service is preconfigured and ready to be set up for your company.</span></span> <span data-ttu-id="4b2ac-108">Weitere Informationen finden Sie unter [Belegaustausch-Dienst](across-how-to-set-up-a-document-exchange-service.md).</span><span class="sxs-lookup"><span data-stu-id="4b2ac-108">For more information, see [Set Up a Document Exchange Service](across-how-to-set-up-a-document-exchange-service.md).</span></span> <span data-ttu-id="4b2ac-109">In einigen Fällen müssen Sie jedoch eine App installieren.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-109">However, in some cases, you must install an app.</span></span> <span data-ttu-id="4b2ac-110">Weitere Informationen finden Sie unter [Elektronische Rechnung FAQ](faq-electronic-invoicing.yml).</span><span class="sxs-lookup"><span data-stu-id="4b2ac-110">For more information, see [Electronic Invoicing FAQ](faq-electronic-invoicing.yml).</span></span>  

 <span data-ttu-id="4b2ac-111">Um beispielsweise Verkaufsrechnungen als elektronischen PEPPOL-Beleg zu senden, wählen Sie die Option **Elektronisches Dokument** im **Buchen und senden**-Dialogfeld aus.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-111">To send a sales invoice as an electronic PEPPOL document, you select the **Electronic Document** option in the **Post and Send** dialog box.</span></span> <span data-ttu-id="4b2ac-112">Dort können Sie außerdem das standardmäßige Belegsendeprofil für den Kunden vom Dialogfeld einrichten.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-112">You can also set up the customer's default document sending profile from that dialog box.</span></span> <span data-ttu-id="4b2ac-113">Zuerst müssen Sie verschiedene Stammdaten einrichten, zum Beispiel Mandantendaten, Debitoren, Artikel und Maßeinheiten.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-113">First, you must set up various master data, such as company information, customers, items, and units of measure.</span></span> <span data-ttu-id="4b2ac-114">Diese werden verwendet, um Geschäftspartner und Artikel zu identifizieren, wenn Daten in Feldern in [Einrichten von Senden und Empfangen von elektronischen Dokumenten](across-how-to-set-up-electronic-document-sending-and-receiving.md)in Elemente in der ausgehenden Dokumentdatei konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-114">These are used to identify the business partners and items when converting data in fields in [Set Up Electronic Document Sending and Receiving](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span></span>  

### <a name="to-send-an-electronic-sales-invoice"></a><span data-ttu-id="4b2ac-115">So senden Sie eine elektronische Verkaufsrechnung</span><span class="sxs-lookup"><span data-stu-id="4b2ac-115">To send an electronic sales invoice</span></span>

1. <span data-ttu-id="4b2ac-116">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun") aus, geben Sie **Verkaufsrechnungen** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  

2. <span data-ttu-id="4b2ac-117">Erstellen Sie eine neue Verkaufsrechnung.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-117">Create a new sales invoice.</span></span>  

3. <span data-ttu-id="4b2ac-118">Wenn die Verkaufsrechnung fakturierbar ist, wählen Sie die Aktion **Buchen und Senden**.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-118">When the sales invoice is ready to be invoiced, choose the **Post and Send** action.</span></span>  

     <span data-ttu-id="4b2ac-119">Wenn das Standard-Sendeprofil des Kunden lautet **Elektronisches Dokument**, dann wird es im Dialogfeld **Bestätigung buchen und senden** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-119">If the customer's default sending profile is **Electronic Document**, then it will be shown in the **Post and Send Confirmation** dialog box.</span></span> <span data-ttu-id="4b2ac-120">Auf diese Weise müssen Sie nur die Schaltfläche **Ja** zum Buchen und Versenden der Rechnung elektronisch im ausgewählten Format auswählen.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-120">This way, you just have to choose the **Yes** button to post and send the invoice electronically in the selected format.</span></span>  

4. <span data-ttu-id="4b2ac-121">Wählen Sie im Dialogfeld **Buchungs- und Sendebestätigung** die AssistEdit-Schaltfläche rechts vom Feld **Beleg senden an** aus.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-121">In the **Post and Send Confirmation** dialog box, choose the AssistEdit button to the right of the **Send Document to** field.</span></span>  

5. <span data-ttu-id="4b2ac-122">Wählen Sie im Dialgofeld **Beleg senden an** im Feld **Elektronischer Beleg** die Option **Über Belegaustauschdienst** aus.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-122">In the **Send Document to** dialog box, in the **Electronic Document** field, choose **Through Document Exchange Service**.</span></span>  

6. <span data-ttu-id="4b2ac-123">Wählen Sie im Feld **Format** die Option **PEPPOL** aus.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-123">In the **Format** field, choose **PEPPOL**.</span></span>  

7. <span data-ttu-id="4b2ac-124">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-124">Choose the **OK** button.</span></span> <span data-ttu-id="4b2ac-125">Das Dialogfeld **Buchungs- und Sendebestätigung** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-125">The **Post and Send Confirmation** dialog box appears.</span></span> <span data-ttu-id="4b2ac-126">**Elektronischer Beleg (PEPPOL)** wird im Feld **Beleg senden an** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-126">**Electronic Document (PEPPOL)** is added to the **Send Document to** field.</span></span>  

8. <span data-ttu-id="4b2ac-127">Wählen Sie die Schaltfläche **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-127">Choose the **Yes** button.</span></span>  

     <span data-ttu-id="4b2ac-128">Die Verkaufsrechnung wird gebucht und als elektronischer Beleg im PEPPOL-Format an den Debitor gesendet.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-128">The sales invoice is posted and sent to the customer in the PEPPOL format.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="4b2ac-129">Sie können auch eine gebuchte Verkaufsrechnung als elektronischen Beleg senden.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-129">You can also send a posted sales invoice as an electronic document.</span></span> <span data-ttu-id="4b2ac-130">Dieser Vorgang ist derselbe wie im Thema für nicht gebuchte Verkaufsbelege beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-130">The procedure is the same as described in this topic for non-posted sales documents.</span></span> <span data-ttu-id="4b2ac-131">Wählen Sie auf der Seite **gebuchte Verkaufsrechnung** die Aktion **Aktivitätsprotokoll**, um den Status des elektronischen Dokuments anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-131">On the **Posted Sales Invoice** page, choose the **Activity Log** action to view the status of the electronic document.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="4b2ac-132">Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="4b2ac-132">See Related Training at [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="4b2ac-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b2ac-133">See Also</span></span>

[<span data-ttu-id="4b2ac-134">Fakturieren eines Verkaufs</span><span class="sxs-lookup"><span data-stu-id="4b2ac-134">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="4b2ac-135">Belegsendeprofile einrichten</span><span class="sxs-lookup"><span data-stu-id="4b2ac-135">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md)  
[<span data-ttu-id="4b2ac-136">Einrichten des Senden und Empfangen von elektronischen Belegen</span><span class="sxs-lookup"><span data-stu-id="4b2ac-136">Set Up Electronic Document Sending and Receiving</span></span>](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[<span data-ttu-id="4b2ac-137">So richten Sie einen Belegaustauschdienst ein</span><span class="sxs-lookup"><span data-stu-id="4b2ac-137">Set Up a Document Exchange Service</span></span>](across-how-to-set-up-a-document-exchange-service.md)  
[<span data-ttu-id="4b2ac-138">Richten Sie Datenaustauschdefinitionen ein.</span><span class="sxs-lookup"><span data-stu-id="4b2ac-138">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="4b2ac-139">Daten elektronisch austauschen</span><span class="sxs-lookup"><span data-stu-id="4b2ac-139">Exchanging Data Electronically</span></span>](across-data-exchange.md)  
[<span data-ttu-id="4b2ac-140">Elektronische Rechnungsstellung FAQ</span><span class="sxs-lookup"><span data-stu-id="4b2ac-140">Electronic Invoicing FAQ</span></span>](faq-electronic-invoicing.yml)  
[<span data-ttu-id="4b2ac-141">Allgemeine Geschäftsfunktionen</span><span class="sxs-lookup"><span data-stu-id="4b2ac-141">General Business Functionality</span></span>](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]