---
title: Zahlungsabstimmung mit der Envestnet Yodlee Bank Feeds Erweiterung | Microsoft Docs
description: Beschreibt die Envestnet Yodlee Bank Feeds Erweierung, die die Bankkonten verknüpft, sodass Sie schnell Zahlungen abgleichen können.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: d79ef7c076ec3a529aeb0c679b8b61658ef65af5
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315348"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a><span data-ttu-id="82294-103">Die Envestnet Yodlee Bank Feeds-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="82294-103">The Envestnet Yodlee Bank Feeds Extension</span></span>
<span data-ttu-id="82294-104">Um die Zahlungen schnell abzustimmen, die an Ihre Bankkonten getätigt werden, kann der Envestnet Yodlee Bank Feeds Service Ihre Systembankkonten mit Ihrem Online Bankkonto verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="82294-104">To quickly reconcile payments made to your bank accounts, the Envestnet Yodlee Bank Feeds service allows you to link your system bank account to your online bank account.</span></span> <span data-ttu-id="82294-105">Das bedeutet, dass der letzte Bankkontoauszug automatisch oder manuell in Ihr Abstimmungsbuch.-Blatt gespeist wird und stellt sicher, dass immer die aktuelle Zahlungen mit minimalem Fehlerrisiko verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="82294-105">This means that the latest bank statement is automatically or manually fed into your reconciliation journal, ensuring that you are always processing the latest payments with minimal risk of errors.</span></span>

<span data-ttu-id="82294-106">Der Envestnet Yodlee Bank Feeds Service wird nur in den USA und in Kanada unterstützt.</span><span class="sxs-lookup"><span data-stu-id="82294-106">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>

> [!NOTE]
> <span data-ttu-id="82294-107">Diese Funktion wird nur in der Online-Version von Business Central unterstützt.</span><span class="sxs-lookup"><span data-stu-id="82294-107">This functionality is only supported in the online version of Business Central.</span></span> <span data-ttu-id="82294-108">Um diese Funktionalität lokal nutzen zu können, müssen Sie ein Co-Brand-Konto von Envestnet Yodlee erhalten.</span><span class="sxs-lookup"><span data-stu-id="82294-108">To use this functionality on-premise, you must obtain a cobrand account from Envestnet Yodlee.</span></span><br /><br />

> [!IMPORTANT]
> <span data-ttu-id="82294-109">Aufgrund der neuen Zahlungsdiensterichtlinie in Europa (PSD2) können Sie nach dem 14. September 2019 nicht mehr automatisch Kontoauszüge von Banken in Großbritannien importieren in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="82294-109">Due to the new Payment Services Directive in Europe (PSD2), after September 14, 2019, you will no longer be able to automatically import bank statements from banks in the United Kingdom into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="82294-110">Wir prüfen, ob wir dieses Funktion in Zukunft wieder anbieten können.</span><span class="sxs-lookup"><span data-stu-id="82294-110">We are looking into the possibility of offering this feature again in the future.</span></span>

<span data-ttu-id="82294-111">Der Envestnet Yodlee Bank Feeds Service bietet die folgenden Vorteile:</span><span class="sxs-lookup"><span data-stu-id="82294-111">The Envestnet Yodlee Bank Feeds service provides the following benefits:</span></span>

* <span data-ttu-id="82294-112">Entfernt die Anforderung zur manuellen Eingabe.</span><span class="sxs-lookup"><span data-stu-id="82294-112">Removes the need for manual entry.</span></span>
* <span data-ttu-id="82294-113">Verbessert Effektivität und die Genauigkeit, wenn die Zahlungsabstimmung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="82294-113">Improves efficiency and accuracy when doing payment reconciliation.</span></span>
* <span data-ttu-id="82294-114">Unterstützt viele Banken.</span><span class="sxs-lookup"><span data-stu-id="82294-114">Supports a large number of banks.</span></span>
* <span data-ttu-id="82294-115">Hier aktuelle Informationen über Banktransaktionen in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="82294-115">Allows up-to-date information about bank transactions from within [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
* <span data-ttu-id="82294-116">Unterstützt manuelle sowie automatische Bankfeeds.</span><span class="sxs-lookup"><span data-stu-id="82294-116">Supports manual as well as automatic bank feeds.</span></span>
* <span data-ttu-id="82294-117">Aktiviert das Outsourcing der Zahlungsabstimmung zu einem Buchhalter, indem das Bieten des Lagerzugang zu den Bankkontoauszügen bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="82294-117">Enables outsourcing of payment reconciliation to an accountant by providing access to bank statements.</span></span>

<span data-ttu-id="82294-118">Weitere Informationen finden Sie unter [Den Envestnet Yodlee Bank Feeds Service einrichten](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="82294-118">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="82294-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82294-119">See Also</span></span>
<span data-ttu-id="82294-120">[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="82294-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
[<span data-ttu-id="82294-121">Zahlungen automatisch vornehmen und Bankkonten abstimmen</span><span class="sxs-lookup"><span data-stu-id="82294-121">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
<span data-ttu-id="82294-122">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="82294-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
