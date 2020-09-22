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
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: c97673ceda1765033877318b46d63652ec318ae9
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3789425"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a><span data-ttu-id="dde81-103">Die Envestnet Yodlee Bank Feeds-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="dde81-103">The Envestnet Yodlee Bank Feeds Extension</span></span>
<span data-ttu-id="dde81-104">Um die Zahlungen schnell abzustimmen, die an Ihre Bankkonten getätigt werden, kann der Envestnet Yodlee Bank Feeds Service Ihre Systembankkonten mit Ihrem Online Bankkonto verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="dde81-104">To quickly reconcile payments made to your bank accounts, the Envestnet Yodlee Bank Feeds service allows you to link your system bank account to your online bank account.</span></span> <span data-ttu-id="dde81-105">Das bedeutet, dass der letzte Bankkontoauszug automatisch oder manuell in Ihr Abstimmungsbuch.-Blatt gespeist wird und stellt sicher, dass immer die aktuelle Zahlungen mit minimalem Fehlerrisiko verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="dde81-105">This means that the latest bank statement is automatically or manually fed into your reconciliation journal, ensuring that you are always processing the latest payments with minimal risk of errors.</span></span>

<span data-ttu-id="dde81-106">Der Envestnet Yodlee Bank Feeds-Service wird nur in den Vereinigten Staaten und Kanada unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dde81-106">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>

> [!NOTE]
> <span data-ttu-id="dde81-107">Der Envestnet Yodlee Bank Feeds Service wird nur in der Online-Version von Business Central unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dde81-107">The Envestnet Yodlee Bank Feeds service is only supported in the online version of Business Central.</span></span> <span data-ttu-id="dde81-108">Um diese Funktionalität lokal nutzen zu können, müssen Sie ein Co-Brand-Konto von Envestnet Yodlee erhalten.</span><span class="sxs-lookup"><span data-stu-id="dde81-108">To use this functionality on-premises, you must obtain a cobrand account from Envestnet Yodlee.</span></span><br /><br />
> <span data-ttu-id="dde81-109">Der Envestnet Yodlee Bank Feeds-Service wird nur in den Vereinigten Staaten und Kanada unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dde81-109">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>
> <span data-ttu-id="dde81-110">Es werden nur Banken mit Wohnsitz in diesen Ländern unterstützt, auch wenn Banken aus anderen Ländern im Bankenauswahlfenster Envestnet Yodlee Bank Feeds unter [!INCLUDE[d365fin](includes/d365fin_md.md)] erscheinen können.</span><span class="sxs-lookup"><span data-stu-id="dde81-110">Only banks residing in these countries are supported, even though banks from other countries may appear in the Envestnet Yodlee Bank Feeds bank selection window in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dde81-111">Aufgrund der neuen Zahlungsdiensterichtlinie in Europa (PSD2) können Sie nach dem 14. September 2019 nicht mehr automatisch Kontoauszüge von Banken in Großbritannien importieren in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="dde81-111">Due to the new Payment Services Directive in Europe (PSD2), after September 14, 2019, you will no longer be able to automatically import bank statements from banks in the United Kingdom into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="dde81-112">Wir prüfen, ob wir dieses Funktion in Zukunft wieder anbieten können.</span><span class="sxs-lookup"><span data-stu-id="dde81-112">We are looking into the possibility of offering this feature again in the future.</span></span>

<span data-ttu-id="dde81-113">Der Envestnet Yodlee Bank Feeds Service bietet die folgenden Vorteile:</span><span class="sxs-lookup"><span data-stu-id="dde81-113">The Envestnet Yodlee Bank Feeds service provides the following benefits:</span></span>

* <span data-ttu-id="dde81-114">Entfernt die Anforderung zur manuellen Eingabe.</span><span class="sxs-lookup"><span data-stu-id="dde81-114">Removes the need for manual entry.</span></span>
* <span data-ttu-id="dde81-115">Verbessert Effektivität und die Genauigkeit, wenn die Zahlungsabstimmung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="dde81-115">Improves efficiency and accuracy when doing payment reconciliation.</span></span>
* <span data-ttu-id="dde81-116">Unterstützt viele Banken.</span><span class="sxs-lookup"><span data-stu-id="dde81-116">Supports a large number of banks.</span></span>
* <span data-ttu-id="dde81-117">Hier aktuelle Informationen über Banktransaktionen in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="dde81-117">Allows up-to-date information about bank transactions from within [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
* <span data-ttu-id="dde81-118">Unterstützt manuelle sowie automatische Bankfeeds.</span><span class="sxs-lookup"><span data-stu-id="dde81-118">Supports manual as well as automatic bank feeds.</span></span>
* <span data-ttu-id="dde81-119">Aktiviert das Outsourcing der Zahlungsabstimmung zu einem Buchhalter, indem das Bieten des Lagerzugang zu den Bankkontoauszügen bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="dde81-119">Enables outsourcing of payment reconciliation to an accountant by providing access to bank statements.</span></span>

## <a name="available-bank-feeds"></a><span data-ttu-id="dde81-120">Verfügbare Bankfeeds</span><span class="sxs-lookup"><span data-stu-id="dde81-120">Available Bank Feeds</span></span>
<span data-ttu-id="dde81-121">Sie können prüfen, ob eine Bank unterstützt wird, indem Sie den Dienst Envestnet Yodlee Bank Feeds einrichten und sich mit ihm verbinden.</span><span class="sxs-lookup"><span data-stu-id="dde81-121">You can check whether a bank is supported by setting up and connecting to the Envestnet Yodlee Bank Feeds service.</span></span> <span data-ttu-id="dde81-122">Die Bank wird in der Liste angezeigt, wenn sie von Envestnet Yodlee unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="dde81-122">The bank will appear on the list if it is supported by Envestnet Yodlee.</span></span>

<span data-ttu-id="dde81-123">Weitere Informationen finden Sie unter [Den Envestnet Yodlee Bank Feeds Service einrichten](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="dde81-123">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="dde81-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dde81-124">See Also</span></span>
<span data-ttu-id="dde81-125">[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="dde81-125">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
[<span data-ttu-id="dde81-126">Zahlungen automatisch vornehmen und Bankkonten abstimmen</span><span class="sxs-lookup"><span data-stu-id="dde81-126">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
<span data-ttu-id="dde81-127">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dde81-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
