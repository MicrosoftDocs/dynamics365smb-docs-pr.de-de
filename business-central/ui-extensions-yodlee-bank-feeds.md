---
title: Zahlungs-Abstimmung mit der Bank Envestnet Yodlee Erweiterung | Microsoft Docs
description: Beschreibt die Bank-Feederweiterung Envestnet, Yodlee den Verknüpfungen für Bankkonten sodass Sie schnell und Zahlungen zu entschädigen können.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 02/26/2019
ms.author: sgroespe
ms.openlocfilehash: 36400b3265517c29f68f7eb59d17d968334e0fb1
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "799294"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a><span data-ttu-id="c3caa-103">Die Envestnet Yodlee Bank-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="c3caa-103">The Envestnet Yodlee Bank Feeds Extension</span></span>
<span data-ttu-id="c3caa-104">Um die Zahlungen schnell abzustimmen, die an Ihre Bankkonten getätigt werden, kann die Bank-Feed-Service Envestnet Yodlee Ihre Systembankkonten mit Ihrem Online Bankkonto verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="c3caa-104">To quickly reconcile payments made to your bank accounts, the Envestnet Yodlee Bank Feeds service allows you to link your system bank account to your online bank account.</span></span> <span data-ttu-id="c3caa-105">Das bedeutet, dass der letzte Bankkontoauszug automatisch oder manuell in Ihr Abstimmungsbuch.-Blatt gespeist wird und stellt sicher, dass immer die aktuelle Zahlungen mit minimalem Fehlerrisiko verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="c3caa-105">This means that the latest bank statement is automatically or manually fed into your reconciliation journal, ensuring that you are always processing the latest payments with minimal risk of errors.</span></span>

> [!NOTE]
> <span data-ttu-id="c3caa-106">Diese Funktion wird nur in der Online-Version von Business Central unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c3caa-106">This functionality is only supported in the online version of Business Central.</span></span> <span data-ttu-id="c3caa-107">Um diese Funktionalität lokal nutzen zu können, müssen Sie ein Co-Brand-Konto von Envestnet Yodlee erhalten.</span><span class="sxs-lookup"><span data-stu-id="c3caa-107">To use this functionality on-premise, you must obtain a cobrand account from Envestnet Yodlee.</span></span>

<span data-ttu-id="c3caa-108">Der Bank-Feed-Service Envestnet Yodlee stellt die folgenden Vorteile bereit:</span><span class="sxs-lookup"><span data-stu-id="c3caa-108">The Envestnet Yodlee Bank Feeds service provides the following benefits:</span></span>

* <span data-ttu-id="c3caa-109">Entfernt die Anforderung zur manuellen Eingabe.</span><span class="sxs-lookup"><span data-stu-id="c3caa-109">Removes the need for manual entry.</span></span>
* <span data-ttu-id="c3caa-110">Verbessert Effektivität und die Genauigkeit, wenn die Zahlungsabstimmung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="c3caa-110">Improves efficiency and accuracy when doing payment reconciliation.</span></span>
* <span data-ttu-id="c3caa-111">Unterstützt viele Banken.</span><span class="sxs-lookup"><span data-stu-id="c3caa-111">Supports a large number of banks.</span></span>
* <span data-ttu-id="c3caa-112">Hier aktuelle Informationen über Banktransaktionen in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="c3caa-112">Allows up-to-date information about bank transactions from within [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
* <span data-ttu-id="c3caa-113">Unterstützt manuelle sowie automatische Bankfeeds.</span><span class="sxs-lookup"><span data-stu-id="c3caa-113">Supports manual as well as automatic bank feeds.</span></span>
* <span data-ttu-id="c3caa-114">Aktiviert das Outsourcing der Zahlungsabstimmung zu einem Buchhalter, indem das Bieten des Lagerzugang zu den Bankkontoauszügen bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c3caa-114">Enables outsourcing of payment reconciliation to an accountant by providing access to bank statements.</span></span>

<span data-ttu-id="c3caa-115">Für weitere Informationen, siehe [Einrichten des Envestnet Yodlee Bank-Feed-Service](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="c3caa-115">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c3caa-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3caa-116">See Also</span></span>
<span data-ttu-id="c3caa-117">[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="c3caa-117">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
[<span data-ttu-id="c3caa-118">Zahlungen automatisch vornehmen und Bankkonten abstimmen</span><span class="sxs-lookup"><span data-stu-id="c3caa-118">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
<span data-ttu-id="c3caa-119">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c3caa-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
