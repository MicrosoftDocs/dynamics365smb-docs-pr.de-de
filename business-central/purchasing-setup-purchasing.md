---
title: Überblick der Aufgaben zum Einrichten von Einkauf einzurichten | Microsoft Docs
description: Beschreibt die Aufgaben, um die Beschaffungsrichtlinien Ihres Mandanten festzulegen und Ihre Einkaufsprozesse einzurichten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement, supply, vendor order
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 219c1fcf1d4929a548f9a8d5849dde77f1c0b24a
ms.sourcegitcommit: 32bfc2acaaf3693afc9aeb86feea505fd328caa1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/19/2021
ms.locfileid: "5024587"
---
# <a name="setting-up-purchasing"></a><span data-ttu-id="31924-103">Einkauf einrichten</span><span class="sxs-lookup"><span data-stu-id="31924-103">Setting Up Purchasing</span></span>
<span data-ttu-id="31924-104">Bevor Sie Einkaufsprozesse verwalten können, müssen die Regeln und Werte konfiguriert werden, die die Einkaufsrichtlinien des Mandanten definieren.</span><span class="sxs-lookup"><span data-stu-id="31924-104">Before you can manage purchase processes, you must configure the rules and values that define the company's purchase policies.</span></span>

<span data-ttu-id="31924-105">Definieren Sie zunächst die allgemeinen Einstellungen wie die erforderlichen Belege und die gewünschte Buchung der entsprechenden Werte.</span><span class="sxs-lookup"><span data-stu-id="31924-105">You must define the general setup, such as which purchase documents are required and how their values are posted.</span></span> <span data-ttu-id="31924-106">Diese allgemeine Einrichtung erfolgt in der Regel einmal bei der anfänglichen Implementierung.</span><span class="sxs-lookup"><span data-stu-id="31924-106">This general setup is typically performed once during the initial implementation.</span></span>

<span data-ttu-id="31924-107">Eine separate Reihe von Aufgaben, die mit der Erfassung neuer Kreditoren im Zusammenhang stehen, dient dazu, alle Sonderpreis oder Rabattvereinbarungen zu speichern, die Sie mit einzelnen Kreditoren haben.</span><span class="sxs-lookup"><span data-stu-id="31924-107">A separate series of tasks related to registering new vendors is to record any special price or discount agreements that you have with each vendor.</span></span>

<span data-ttu-id="31924-108">Einrichten von finanzbezogenen Einkäufen wie Zahlungsformen und Währungen werden im Finanzsetupabschnitt behandelt.</span><span class="sxs-lookup"><span data-stu-id="31924-108">Finance-related purchase setup, such as payment methods and currencies, are covered in the Finance Setup section.</span></span> <span data-ttu-id="31924-109">Weitere Informationen finden Sie unter [Einrichten von Finanzen](finance-setup-finance.md).</span><span class="sxs-lookup"><span data-stu-id="31924-109">For more information, see [Setting Up Finance](finance-setup-finance.md).</span></span>

| <span data-ttu-id="31924-110">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="31924-110">To</span></span> | <span data-ttu-id="31924-111">Siehe</span><span class="sxs-lookup"><span data-stu-id="31924-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="31924-112">Erstellen Sie eine Kreditorenkarte für jeden Kreditor, von dem Sie einkaufen.</span><span class="sxs-lookup"><span data-stu-id="31924-112">Create a vendor card for each vendor that you purchase from</span></span>|[<span data-ttu-id="31924-113">Registriert einen neuen Kreditor</span><span class="sxs-lookup"><span data-stu-id="31924-113">Register New Vendors</span></span>](purchasing-how-register-new-vendors.md) |
| <span data-ttu-id="31924-114">Eingeben der unterschiedlichen Rabatte und alternativen Preise, die vom Kreditor in Abhängigkeit des Artikels, der Menge und/oder des Datums gewährt werden</span><span class="sxs-lookup"><span data-stu-id="31924-114">Enter the different discounts and special prices that vendors grant you depending on item, quantities, and/or date</span></span> |[<span data-ttu-id="31924-115">Erfassen von Einkaufspreisen, Skonti und Zahlungsvereinbarungen</span><span class="sxs-lookup"><span data-stu-id="31924-115">Record Purchase Price, Discount, and Payment Agreements</span></span>](purchasing-how-record-purchase-price-discount-payment-agreements.md) |
| <span data-ttu-id="31924-116">Kreditoren priorisieren</span><span class="sxs-lookup"><span data-stu-id="31924-116">Prioritize vendors</span></span> |[<span data-ttu-id="31924-117">Kreditoren priorisieren</span><span class="sxs-lookup"><span data-stu-id="31924-117">Prioritize Vendors</span></span>](purchasing-how-prioritize-vendors.md) |
| <span data-ttu-id="31924-118">Einkäufer einrichten</span><span class="sxs-lookup"><span data-stu-id="31924-118">Set up purchasers</span></span> |[<span data-ttu-id="31924-119">Einkäufer einrichten</span><span class="sxs-lookup"><span data-stu-id="31924-119">Set Up Purchasers</span></span>](purchasing-how-setup-purchasers.md) |
|<span data-ttu-id="31924-120">Geben Sie Standardberichte an, die für verschiedene Dokumenttypen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="31924-120">Specify default reports to be used for different document types.</span></span>|[<span data-ttu-id="31924-121">Berichtsauswahl in Business Central</span><span class="sxs-lookup"><span data-stu-id="31924-121">Report Selection in Business Central</span></span>](across-report-selections.md)|

> [!TIP]
> <span data-ttu-id="31924-122">Abhängig von Ihrem geografischen Standort können einige Seiten Felder enthalten, die in den hier aufgeführten Artikeln nicht beschrieben sind, da sie für lokale Funktionen oder Anpassungen gelten.</span><span class="sxs-lookup"><span data-stu-id="31924-122">Depending on your geographical location, some pages can contain fields that are not described in the articles that are listed here because they apply to local functionality or customizations.</span></span> [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="31924-123">Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="31924-123">See Related Training at [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="31924-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31924-124">See Also</span></span>

[<span data-ttu-id="31924-125">Einkauf</span><span class="sxs-lookup"><span data-stu-id="31924-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="31924-126">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="31924-126">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
