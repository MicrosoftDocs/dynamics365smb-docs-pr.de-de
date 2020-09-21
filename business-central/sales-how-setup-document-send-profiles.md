---
title: Bevorzugte Methoden der Übermittlung von Verkaufsbelegen einrichten | Microsoft Docs
description: Beschreibt, wie Sie für jeden Debitor die bevorzugte Methode zum Versenden von Verkaufsdokumenten, z.B. E-Mail, PDF, elektronisches Dokument usw., einrichten.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: email, PDF, electronic document
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 528ee49dda35055872c7ebe2d241456383028434
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3780810"
---
# <a name="set-up-document-sending-profiles"></a><span data-ttu-id="bc2b1-103">Belegsendeprofile einrichten</span><span class="sxs-lookup"><span data-stu-id="bc2b1-103">Set Up Document Sending Profiles</span></span>
<span data-ttu-id="bc2b1-104">Sie können jeden Debitor mit einer bevorzugten Methode der Übermittlung von Verkaufsbelegen einrichten, sodass Sie nicht jedes Mal eine Sendeoptionen auswählen müssen, wenn Sie die Schaltfläche **Buchen und senden** auswählen.</span><span class="sxs-lookup"><span data-stu-id="bc2b1-104">You can set each customer up with a preferred method of sending sales documents, so that you do not have to select a sending option every time you choose the **Post and Send** action.</span></span>

<span data-ttu-id="bc2b1-105">Auf der Seite **Belegsendeprofile** richten Sie verschiedene **Dokumente-Sendeprofile** ein, die Sie aus dem Feld von einer Debitorenkarte auswählen können.</span><span class="sxs-lookup"><span data-stu-id="bc2b1-105">On the **Document Sending Profiles** page, you set up different sending profiles that you can select from in the **Document Sending Profile** field on a customer card.</span></span> <span data-ttu-id="bc2b1-106">Im Kontrollkästchen **Standard** geben Sie an, dass das Belegsendprofil das Standardprofil für alle Debitoren gilt, außer Debitoren, bei denen das Feld **Dokument-Sendeprofil** mit einem anderen Sendeprofil ausgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="bc2b1-106">You can select the **Default** check box to specify that the document sending profile is the default profile for all customers, except for customers where the **Document Sending Profile** field is filled with another sending profile.</span></span>

<span data-ttu-id="bc2b1-107">Wenn Sie die Schaltfläche **Buchen und senden** für einen Verkaufsbeleg auswählen, wird im Dialogfeld **Buchungs- und Sendebestätigung** das verwendete Sendeprofil angezeigt. Dabei handelt es sich entweder um das für den Debitor eingerichtete oder um Standardprofil für alle Debitoren.</span><span class="sxs-lookup"><span data-stu-id="bc2b1-107">When you choose the **Post and Send** action on a sales document, the **Post and Send Confirmation** dialog box shows the sending profile used, either the one set up for the customer or the default for all customers.</span></span> <span data-ttu-id="bc2b1-108">In diesem Dialogfeld können Sie das Sendeprofil für den Verkaufsbeleg ändern.</span><span class="sxs-lookup"><span data-stu-id="bc2b1-108">In the dialog box, you can change the sending profile for the sales document.</span></span> <span data-ttu-id="bc2b1-109">Weitere Informationen finden Sie unter [Fakturieren eines Verkaufs](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="bc2b1-109">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span>
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4jzHH?rel=0]

## <a name="to-set-up-a-document-sending-profile"></a><span data-ttu-id="bc2b1-110">Einrichten von Belegsendeprofilen</span><span class="sxs-lookup"><span data-stu-id="bc2b1-110">To set up a document sending profile</span></span>
1. <span data-ttu-id="bc2b1-111">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Belegsendeprofil** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="bc2b1-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Document Sending Profiles**, and then choose the related link.</span></span>
2. <span data-ttu-id="bc2b1-112">Auf der Seite **Dokumentsendeprofile** wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="bc2b1-112">On the **Document Sending Profiles** page, choose the **New** action.</span></span>
3. <span data-ttu-id="bc2b1-113">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="bc2b1-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-specify-a-sending-profile-on-a-customer-card"></a><span data-ttu-id="bc2b1-114">Sendeprofil für eine Debitorenkarte festlegen</span><span class="sxs-lookup"><span data-stu-id="bc2b1-114">To specify a sending profile on a customer card</span></span>
1. <span data-ttu-id="bc2b1-115">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link.</span><span class="sxs-lookup"><span data-stu-id="bc2b1-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="bc2b1-116">Öffnen Sie die Karte des Debitors, für den ein Sendeprofil eingerichtet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bc2b1-116">Open the card of the customer who you want to set up a sending profile for.</span></span>
3. <span data-ttu-id="bc2b1-117">Wählen Sie im Inforegister **Belegsendeprofil** ein Profil aus, das sie eingerichtet haben wie im vorigen Verfahren beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bc2b1-117">In the **Document Sending Profile** field, select a profile that you have set up as described in the previous procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="bc2b1-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc2b1-118">See Also</span></span>
[<span data-ttu-id="bc2b1-119">Einrichten von Verkäufen</span><span class="sxs-lookup"><span data-stu-id="bc2b1-119">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="bc2b1-120">Verkauf</span><span class="sxs-lookup"><span data-stu-id="bc2b1-120">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="bc2b1-121">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bc2b1-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
