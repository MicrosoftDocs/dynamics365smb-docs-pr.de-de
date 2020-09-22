---
title: Senden Sie elektronische Belege | Microsoft Docs
description: Erfahren Sie, wie man Rechnungen elektronisch sendet.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: b89724725f5929e0ebea79a94bcdb3e87069c75d
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788900"
---
# <a name="send-electronic-documents"></a><span data-ttu-id="8eed4-103">Elektronische Belege senden</span><span class="sxs-lookup"><span data-stu-id="8eed4-103">Send Electronic Documents</span></span>
<span data-ttu-id="8eed4-104">Die allgemeine Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt das Senden von elektronischen Rechnungen und Gutschriften im PEPPOL-Format, das von den größten Anbietern von Belegaustauschdiensten unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="8eed4-104">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] supports sending electronic invoices and credit memos in the PEPPOL format, which is supported by the largest document exchange service providers.</span></span> <span data-ttu-id="8eed4-105">Ein Anbieter von Belegaustauschdiensten leitet elektronische Belege zwischen Handelspartnern weiter.</span><span class="sxs-lookup"><span data-stu-id="8eed4-105">A document exchange service provider dispatches electronic documents between trading partners.</span></span> <span data-ttu-id="8eed4-106">Um Unterstützung für andere elektronische Belegformate zu bieten, verwenden Sie das Datenaustauschframework.</span><span class="sxs-lookup"><span data-stu-id="8eed4-106">To provide support for other electronic document formats, you use the data exchange framework.</span></span>  

 <span data-ttu-id="8eed4-107">In der allgemeinen Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] ist ein vorkonfigurierter Belegaustauschdienst enthalten, der für Ihren Mandanten eingerichtet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8eed4-107">In the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)], a document exchange service is preconfigured and ready to be set up for your company.</span></span> <span data-ttu-id="8eed4-108">Weitere Informationen finden Sie unter [Belegaustausch-Dienst](across-how-to-set-up-a-document-exchange-service.md).</span><span class="sxs-lookup"><span data-stu-id="8eed4-108">For more information, see [Set Up a Document Exchange Service](across-how-to-set-up-a-document-exchange-service.md).</span></span>  

 <span data-ttu-id="8eed4-109">Um eine Verkaufsrechnung als elektronischen PEPPOL-Beleg zu senden, wählen Sie die Option **Elektronischer Beleg** im Dialogfeld **Buchen und Senden** aus. Hier können Sie auch das standardmäßige Belegsendeprofil für den Debitor einrichten.</span><span class="sxs-lookup"><span data-stu-id="8eed4-109">To send a sales invoice as an electronic PEPPOL document, you select the **Electronic Document** option in the **Post and Send** dialog box from where you can also set up the customer’s default document sending profile.</span></span> <span data-ttu-id="8eed4-110">Zuerst müssen Sie verschiedene Stammdaten einrichten, zum Beispiel Mandantendaten, Debitoren, Artikel und Maßeinheiten.</span><span class="sxs-lookup"><span data-stu-id="8eed4-110">First, you must set up various master data, such as company information, customers, items, and units of measure.</span></span> <span data-ttu-id="8eed4-111">Diese werden verwendet, um Geschäftspartner und Artikel zu identifizieren, wenn Daten in Feldern in [Einrichten von Senden und Empfangen von elektronischen Dokumenten](across-how-to-set-up-electronic-document-sending-and-receiving.md)in Elemente in der ausgehenden Dokumentdatei konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="8eed4-111">These are used to identify the business partners and items when converting data in fields in [Set Up Electronic Document Sending and Receiving](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span></span>  

### <a name="to-send-an-electronic-sales-invoice"></a><span data-ttu-id="8eed4-112">So senden Sie eine elektronische Verkaufsrechnung</span><span class="sxs-lookup"><span data-stu-id="8eed4-112">To send an electronic sales invoice</span></span>  

1.  <span data-ttu-id="8eed4-113">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Verkaufsrechnungen** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="8eed4-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="8eed4-114">Erstellen Sie eine neue Verkaufsrechnung.</span><span class="sxs-lookup"><span data-stu-id="8eed4-114">Create a new sales invoice.</span></span>  

3.  <span data-ttu-id="8eed4-115">Wenn die Verkaufsrechnung fakturierbar ist, wählen Sie die Aktion **Buchen und Senden**.</span><span class="sxs-lookup"><span data-stu-id="8eed4-115">When the sales invoice is ready to be invoiced, choose the **Post and Send** action.</span></span>  

     <span data-ttu-id="8eed4-116">Wenn das Standardsendeprofil des Debitors **Elektronischer Beleg** lautet, wird es im Dialogfeld **Buchungs- und Sendebestätigung** angezeigt, und Sie müssen nur die Schaltfläche **Ja** auswählen, um die Rechnung im ausgewählten Format elektronisch zu buchen und zu senden.</span><span class="sxs-lookup"><span data-stu-id="8eed4-116">If the customer’s default sending profile is **Electronic Document**, then it will be shown in the **Post and Send Confirmation** dialog box and you just have to choose the **Yes** button to post and send the invoice electronically in the selected format.</span></span>  

4.  <span data-ttu-id="8eed4-117">Wählen Sie im Dialogfeld **Buchungs- und Sendebestätigung** die AssistEdit-Schaltfläche rechts vom Feld **Beleg senden an** aus.</span><span class="sxs-lookup"><span data-stu-id="8eed4-117">In the **Post and Send Confirmation** dialog box, choose the AssistEdit button to the right of the **Send Document to** field.</span></span>  

5.  <span data-ttu-id="8eed4-118">Wählen Sie im Dialgofeld **Beleg senden an** im Feld **Elektronischer Beleg** die Option **Über Belegaustauschdienst** aus.</span><span class="sxs-lookup"><span data-stu-id="8eed4-118">In the **Send Document to** dialog box, in the **Electronic Document** field, choose **Through Document Exchange Service**.</span></span>  

6.  <span data-ttu-id="8eed4-119">Wählen Sie im Feld **Format** die Option **PEPPOL** aus.</span><span class="sxs-lookup"><span data-stu-id="8eed4-119">In the **Format** field, choose **PEPPOL**.</span></span>  

7.  <span data-ttu-id="8eed4-120">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="8eed4-120">Choose the **OK** button.</span></span> <span data-ttu-id="8eed4-121">Das Dialogfeld **Buchungs- und Sendebestätigung** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8eed4-121">The **Post and Send Confirmation** dialog box appears.</span></span> <span data-ttu-id="8eed4-122">**Elektronischer Beleg (PEPPOL)** wird im Feld **Beleg senden an** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8eed4-122">**Electronic Document (PEPPOL)** is added to the **Send Document to** field.</span></span>  

8.  <span data-ttu-id="8eed4-123">Wählen Sie die Schaltfläche **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="8eed4-123">Choose the **Yes** button.</span></span>  

     <span data-ttu-id="8eed4-124">Die Verkaufsrechnung wird gebucht und als elektronischer Beleg im PEPPOL-Format an den Debitor gesendet.</span><span class="sxs-lookup"><span data-stu-id="8eed4-124">The sales invoice is posted and sent to the customer as an electronic document in the PEPPOL format.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="8eed4-125">Sie können auch eine gebuchte Verkaufsrechnung als elektronischen Beleg senden.</span><span class="sxs-lookup"><span data-stu-id="8eed4-125">You can also send a posted sales invoice as an electronic document.</span></span> <span data-ttu-id="8eed4-126">Dieser Vorgang ist derselbe wie im Thema für nicht gebuchte Verkaufsbelege beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8eed4-126">The procedure is the same as described in this topic for non-posted sales documents.</span></span> <span data-ttu-id="8eed4-127">Wählen Sie auf der Seite **gebuchte Verkaufsrechnung** die Aktion **Aktivitätsprotokoll**, um den Status des elektronischen Dokuments anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8eed4-127">On the **Posted Sales Invoice** page, choose the **Activity Log** action to view the status of the electronic document.</span></span> <span data-ttu-id="8eed4-128">Weitere Informationen finden Sie unter **Aktivitätsprotokoll**</span><span class="sxs-lookup"><span data-stu-id="8eed4-128">For more information, see **Activity Log**.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="8eed4-129">Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="8eed4-129">See Related Training at [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="8eed4-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8eed4-130">See Also</span></span>  
[<span data-ttu-id="8eed4-131">Fakturieren eines Verkaufs</span><span class="sxs-lookup"><span data-stu-id="8eed4-131">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="8eed4-132">Belegsendeprofile einrichten</span><span class="sxs-lookup"><span data-stu-id="8eed4-132">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md)  
[<span data-ttu-id="8eed4-133">Einrichten des Senden und Empfangen von elektronischen Belegen</span><span class="sxs-lookup"><span data-stu-id="8eed4-133">Set Up Electronic Document Sending and Receiving</span></span>](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[<span data-ttu-id="8eed4-134">So richten Sie einen Belegaustauschdienst ein</span><span class="sxs-lookup"><span data-stu-id="8eed4-134">Set Up a Document Exchange Service</span></span>](across-how-to-set-up-a-document-exchange-service.md)  
[<span data-ttu-id="8eed4-135">Richten Sie Datenaustauschdefinitionen ein.</span><span class="sxs-lookup"><span data-stu-id="8eed4-135">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="8eed4-136">Daten elektronisch austauschen</span><span class="sxs-lookup"><span data-stu-id="8eed4-136">Exchanging Data Electronically</span></span>](across-data-exchange.md)  
[<span data-ttu-id="8eed4-137">Allgemeine Geschäftsfunktionen</span><span class="sxs-lookup"><span data-stu-id="8eed4-137">General Business Functionality</span></span>](ui-across-business-areas.md)  
