---
title: Geben Sie Farbindikatoren an, um visuelle Signale über eine Farbaktivität anzupassen | Microsoft Docs
description: Einrichten eines Farbindikator in einer Stapelkachel, um ein personalisiertes visuelles Signal der Farb-Aktivität zu erhalten.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personalize, customize
ms.date: 04/01/2019
ms.author: solsen
redirect_url: admin-how-set-up-colored-indicator-on-cues
ms.openlocfilehash: f79f1a65ee17d8ca46a8ecf1cd9d49c5246bef63
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "923438"
---
# <a name="set-up-a-colored-indicator-on-cues"></a><span data-ttu-id="26627-103">Einrichten eines farbigen Indikators auf Stapeln des Rollencenters</span><span class="sxs-lookup"><span data-stu-id="26627-103">Set Up a Colored Indicator on Cues</span></span>
<span data-ttu-id="26627-104">Sie können Stapel einrichten, die im Rollencenter mit einem Indikator angezeigt werden, dessen Farbe sich basierend auf den Datenwerten in den Stapeln ändert.</span><span class="sxs-lookup"><span data-stu-id="26627-104">You can set up Cues that appear on the Role Center to include an indicator that changes color based on the data values in the Cues.</span></span>

<span data-ttu-id="26627-105">Der Indikator erscheint als farbige Leiste an der oberen Kante der Stapelfläche.</span><span class="sxs-lookup"><span data-stu-id="26627-105">The indicator appears as a colored bar along the top border of the Cue tile.</span></span> <span data-ttu-id="26627-106">Es wird ein optisches Signal zu dem Status der Aktivität des Stapels angezeigt, dss Bedingungen (vorteilhaft oder ungünstig) angeben kann, und den Benutzer auffordern kann, Maßnahmen zu ergreifen.</span><span class="sxs-lookup"><span data-stu-id="26627-106">It provides a visual signal of the status of the Cue's activity, which can indicate favorable or unfavorable conditions to prompt the user to take action.</span></span> <span data-ttu-id="26627-107">Wenn beispielsweise ein Stapel laufende Verkaufsrechnungen angezeigt, können Sie die Markierung so einrichten, dass sie grün (vorteilhaft) angezeigt wird, wenn die Gesamtanzahl laufender Verkaufsrechnungen unter 10 ist, und in Rot (ungünstig), wenn die Anzahl größer als 20 ist.</span><span class="sxs-lookup"><span data-stu-id="26627-107">For example, if a Cue displays ongoing sales invoices, you can set up the indicator to appear green (favorable) when total number of ongoing sales invoices is below 10, and appears red (unfavorable) when the total is greater than 20.</span></span>

<span data-ttu-id="26627-108">Auf der Seite **Stapel einrichten** können Sie Indikatoren für alle Stapel einrichten, die in der Unternehmensdatenbank verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="26627-108">From the **Cue Setup** page, you set up indicators for all the Cues that are available in the company database.</span></span>

<span data-ttu-id="26627-109">Um den Indikator einzurichten, geben Sie bis zu zwei Schwellenwerte an, die drei Bereiche von Datenwerten definieren (niedrig, mittel und hoch), die Sie jeweils mit einer anderen Farbe (oder einem anderen Format) anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="26627-109">To set up the indicator, you specify up to two threshold values that define three ranges of data values (low, middle, and high) to which you can apply a different color (or style).</span></span>

## <a name="to-set-up-colored-indicators-on-cues"></a><span data-ttu-id="26627-110">So richten Sie farbige Indikatoren auf Stapeln ein.</span><span class="sxs-lookup"><span data-stu-id="26627-110">To set up colored indicators on Cues</span></span>
1. <span data-ttu-id="26627-111">Unter **Aktivitäten** auf Ihrer Rollencenter wählen Sie **Stapel einrichten** aus.</span><span class="sxs-lookup"><span data-stu-id="26627-111">Under **Activities** on your Role Center, choose **Set Up Cues**.</span></span>  
   <span data-ttu-id="26627-112">Die Seite **Stapel einrichten** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="26627-112">The **Cue Setup** page appears.</span></span> <span data-ttu-id="26627-113">Die Seite listet die Indikatoren auf, die derzeit in Stapeln für den Mandanten eingerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="26627-113">The page lists the indicators that are currently setup up on Cues.</span></span>
2. <span data-ttu-id="26627-114">Um einen Indikator zu ändern, bearbeiten Sie die Felder und ändern Sie beispielsweise die Werte für die verschiedenen Schwellenwerte.</span><span class="sxs-lookup"><span data-stu-id="26627-114">To modify an indicator, edit the fields and modify, for example, the values for the different thresholds.</span></span>  

<span data-ttu-id="26627-115">Die folgende Tabelle enthält die Farben, die den Optionen der **Format des unteren Bereichs**, **Format des mittleren Bereichs** und **Format des oberen Bereichs** entsprechen.</span><span class="sxs-lookup"><span data-stu-id="26627-115">The following table lists the colors that correspond to the options of the **Low Range Style**, **Middle Range Style**, and **High Range Style** fields.</span></span>

| <span data-ttu-id="26627-116">Option</span><span class="sxs-lookup"><span data-stu-id="26627-116">Option</span></span> | <span data-ttu-id="26627-117">Farbe</span><span class="sxs-lookup"><span data-stu-id="26627-117">Color</span></span> |
| --- | --- |
| <span data-ttu-id="26627-118">**Keine**</span><span class="sxs-lookup"><span data-stu-id="26627-118">**None**</span></span> |<span data-ttu-id="26627-119">Keine Farbe (dieselbe Farbe wie die Stapelfläche)</span><span class="sxs-lookup"><span data-stu-id="26627-119">No color (same color as the Cue tile)</span></span>|
| <span data-ttu-id="26627-120">**Vorteilhaft**</span><span class="sxs-lookup"><span data-stu-id="26627-120">**Favorable**</span></span> |<span data-ttu-id="26627-121">Grün</span><span class="sxs-lookup"><span data-stu-id="26627-121">Green</span></span> |
| <span data-ttu-id="26627-122">**Ungünstig**</span><span class="sxs-lookup"><span data-stu-id="26627-122">**Unfavorable**</span></span> |<span data-ttu-id="26627-123">Rot</span><span class="sxs-lookup"><span data-stu-id="26627-123">Red</span></span> |
| <span data-ttu-id="26627-124">**Mehrdeutig**</span><span class="sxs-lookup"><span data-stu-id="26627-124">**Ambiguous**</span></span> |<span data-ttu-id="26627-125">Gelb</span><span class="sxs-lookup"><span data-stu-id="26627-125">Yellow</span></span> |
| <span data-ttu-id="26627-126">**Untergeordnet**</span><span class="sxs-lookup"><span data-stu-id="26627-126">**Subordinate**</span></span> |<span data-ttu-id="26627-127">Grau</span><span class="sxs-lookup"><span data-stu-id="26627-127">Gray</span></span> |

## <a name="see-also"></a><span data-ttu-id="26627-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26627-128">See Also</span></span>
<span data-ttu-id="26627-129">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="26627-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
