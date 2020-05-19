---
title: Buchen Sie Zahlungsanzeige-Erweiterung | Microsoft Docs
description: Beschreibt das Senden der Zahlungsanzeigeerweiterung, die das Buchen und das Neuversenden der Zahlungsanzeige aus dem Zahlungsausgangs Buch.-Blatt und den Kreditorenposten zulassen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, remittance, advice
ms.date: 05/05/2020
ms.author: edupont
ms.openlocfilehash: 236cb83e99c2385edc09622255037a152bf41e6e
ms.sourcegitcommit: 57e31a8b92feeaf8c6c63eba147f36b38eee7679
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/06/2020
ms.locfileid: "3339922"
---
# <a name="send-remittance-advice"></a><span data-ttu-id="90667-103">Rimesseavis senden</span><span class="sxs-lookup"><span data-stu-id="90667-103">Send Remittance Advice</span></span>

<span data-ttu-id="90667-104">Wenn Zahlungsanzeigen verwendet werden, um Kreditoren über die Zahlungen zu benachrichtigen, die erstellt werden, können Sie Zahlungsanzeige als Massenvorgang aus dem Zahlungsausgangs Buch.-Blatt buchen und erneut senden, nachdem die Zahlungen von Kreditorenposten getätigt werden, indem Sie Belegsendeprofile verwenden….</span><span class="sxs-lookup"><span data-stu-id="90667-104">Where remittance advice is used to notify vendors of payments being made, you can now email remittance advice in bulk from the payment journal as well as resend after payments are made from vendor ledger entries by using document sending profiles.</span></span>

> [!NOTE]
> <span data-ttu-id="90667-105">Diese Funktionalität wird nur in Business Central online und lokal in folgenden Ländern unterstützt: Großbritannien, USA, Kanada, Australien Neuseeland, und Südafrika.</span><span class="sxs-lookup"><span data-stu-id="90667-105">This functionality is only supported in Business Central online and on-premises in following countries: United Kingdom, United States, Canada, Australia, New Zealand, and South Africa.</span></span>  

<span data-ttu-id="90667-106">Sie können Zahlungsanzeigen auf zwei verschiedene Arten senden:</span><span class="sxs-lookup"><span data-stu-id="90667-106">You can send remittance advice in two different ways:</span></span>

* <span data-ttu-id="90667-107">Auf der Seite **Zahlungsausgangs Buch.-Blatt** wählen Sie **Navigieren**, **Zahlungen**, **Senden der Zahlungsanzeige**, um die Zahlungsanzeige für eine oder mehrere Buch.-Blattzeilen zu buchen</span><span class="sxs-lookup"><span data-stu-id="90667-107">In the **Payment Journal** page, choose **Navigate**, **Payments**, **Send Remittance Advice** to email remittance advice for one or multiple payment journal lines</span></span>
* <span data-ttu-id="90667-108">Wählen Sie auf der Seite **Kreditorenposten** **Aktionen**, **Funktionen**, **Überweisungsbescheid senden** aus, um einen Überweisungsbescheid per E-Mail zu senden, nachdem die Kreditorenzahlungen für einen von mehreren Kreditorenposten gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="90667-108">In the **Vendor Ledger Entries** page, choose **Actions**, **Functions**, **Send Remittance Advice** to email remittance advice after posting of vendor payments, for one or multiple vendor ledger entries</span></span>

## <a name="see-also"></a><span data-ttu-id="90667-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90667-109">See Also</span></span>

[<span data-ttu-id="90667-110">Zahlungsvorschlag</span><span class="sxs-lookup"><span data-stu-id="90667-110">Suggest Vendor Payments</span></span>](payables-how-suggest-vendor-payments.md)  
<span data-ttu-id="90667-111">[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="90667-111">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  
<span data-ttu-id="90667-112">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="90667-112">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="90667-113">Dokumente per E-Mail versenden</span><span class="sxs-lookup"><span data-stu-id="90667-113">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
