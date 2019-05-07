---
title: Häufig gestellte Fragen zu „Wie möchten Sie weiter verfahren“ | Microsoft Docs
description: Dieser Artikel bietet Antworten zu den häufig von unseren Partner und Debitoren über „Wie möchten Sie weiter verfahren“ gestellten Fragen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: d04f78b31b9fb0403201cb9e5cb1f98f1ef935e1
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "937581"
---
# <a name="tell-me-faq"></a><span data-ttu-id="cdc10-103">Häufig gestellte Fragen zu „Wie möchten Sie weiter verfahren“</span><span class="sxs-lookup"><span data-stu-id="cdc10-103">Tell Me FAQ</span></span>
<span data-ttu-id="cdc10-104">In diesem Thema werden Fragen beantwortet, die unsere fortgeschrittenen Benutzer häufig zur Funktion „Wie möchten Sie weiter verfahren“ stellen. Diese Funktion hat die vorherige Seitensuchfunktion ersetzt, die als **Seiten und Bereichte finden** bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="cdc10-104">This topic answers questions that our advanced users often ask about the new Tell Me feature, which has replaced the previous Page Search feature known as **Find Pages and Reports**.</span></span>

### <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a><span data-ttu-id="cdc10-105">Werden alle Aktionen meiner aktuellen Seite von „Wie möchten Sie weiter verfahren“ abgedeckt?</span><span class="sxs-lookup"><span data-stu-id="cdc10-105">Are all actions from my current page discoverable in Tell Me?</span></span>
<span data-ttu-id="cdc10-106">Nein.</span><span class="sxs-lookup"><span data-stu-id="cdc10-106">No.</span></span> <span data-ttu-id="cdc10-107">Aktionen in Zeilen, z. B. der insgesamt, Verkaufszeilen-Teil der FactBoxes werden in „Wie möchten Sie weiter verfahren“ nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cdc10-107">Actions in parts, such as the Sales Lines part or FactBoxes, are not displayed in Tell Me.</span></span>

### <a name="are-the-results-in-tell-me-filtered-by-permissions"></a><span data-ttu-id="cdc10-108">Werden die Ergebnisse in „Wie möchten Sie weiter verfahren“ nach Berechtigungen gefiltert?</span><span class="sxs-lookup"><span data-stu-id="cdc10-108">Are the results in Tell Me filtered by permissions?</span></span>
<span data-ttu-id="cdc10-109">Wenn der Benutzer nicht über AccessByPermissions verfügt, werden keine Aktionen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cdc10-109">If the user does not have AccessByPermissions then actions are not displayed.</span></span> <span data-ttu-id="cdc10-110">Allerdings werden Seiten und Berichte in den Ergebnissen angezeigt. Der Benutzer benötigt jedoch die Berechtigungen, auf sie zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="cdc10-110">However, pages and reports appear in the results but require that the user has permission to access them.</span></span> <span data-ttu-id="cdc10-111">Es wird eine Meldung angezeigt, wenn der Benutzer, nicht über die Berechtigungen zum Anzeigen des Objekts verfügt.</span><span class="sxs-lookup"><span data-stu-id="cdc10-111">A message will display if the user does not have permission to view the object.</span></span>

### <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a><span data-ttu-id="cdc10-112">Zeigt „Wie möchten Sie weiter verfahren“ Inhalt von meinen Anpassungen oder installierten Drittanbietererweiterungen an?</span><span class="sxs-lookup"><span data-stu-id="cdc10-112">Does Tell Me display content from my customizations or installed third-party extensions?</span></span>
<span data-ttu-id="cdc10-113">Aktionen, Seiten und Berichte, die aus Erweiterungen stammen, werden von „Wie möchten Sie weiter verfahren“ erkannt, angepasste Hilfedokumente allerdings nicht.</span><span class="sxs-lookup"><span data-stu-id="cdc10-113">Actions, pages, and reports that originate from extensions are picked up by Tell Me, but custom help documentation is not.</span></span> <span data-ttu-id="cdc10-114">Technische Informationen darüber, wie benutzerdefinierte Seiten und Berichte feststellbar gemacht werden, finden Sie unter [Hinzufügen von Seiten und Berichten zur Suche](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).</span><span class="sxs-lookup"><span data-stu-id="cdc10-114">For technical information about how to make custom pages and reports discoverable, see [Adding Pages and Reports to Search](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).</span></span>

### <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a><span data-ttu-id="cdc10-115">Worin unterschiedet sich dies von der vorherigen Funktion, die als Seitensuche bekannt war?</span><span class="sxs-lookup"><span data-stu-id="cdc10-115">What makes this different from what was previously known as Page Search?</span></span>
<span data-ttu-id="cdc10-116">Die Seitensuche wurde zu „Wie möchten Sie weiter verfahren“ weiterentwickelt, damit Sie schneller arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="cdc10-116">Page Search has evolved into Tell Me to help you get work done quickly.</span></span> <span data-ttu-id="cdc10-117">Die Seitensuche konnte Ihnen nur bei der Navigation in Seiten oder Berichten helfen.</span><span class="sxs-lookup"><span data-stu-id="cdc10-117">Page Search could only help you navigate to pages or reports.</span></span> <span data-ttu-id="cdc10-118">Auf technischer Ebene basiert „Wie möchten Sie weiter verfahren“ nicht mehr auf dem vorherigen MenuSuite-Konzept.</span><span class="sxs-lookup"><span data-stu-id="cdc10-118">At a technical level, Tell Me is no longer based on the legacy MenuSuite concept.</span></span>

### <a name="i-use-on-premises-included365finincludesd365finmdmd-does-that-include-tell-me"></a><span data-ttu-id="cdc10-119">Ich verwende [!INCLUDE[d365fin](includes/d365fin_md.md)] lokal.</span><span class="sxs-lookup"><span data-stu-id="cdc10-119">I use on-premises [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="cdc10-120">Schließt das „Wie möchten Sie weiter verfahren“ ein?</span><span class="sxs-lookup"><span data-stu-id="cdc10-120">Does that include Tell Me?</span></span>
<span data-ttu-id="cdc10-121">Sie können „Wie möchten Sie weiter verfahren“ mit dem lokalen Webclient verwenden, um nach Aktionen, Seiten und Berichten zu suchen, aber nicht nach Dokumentation oder Apps und Beratungsdiensten auf AppSource.</span><span class="sxs-lookup"><span data-stu-id="cdc10-121">You can use Tell Me in the on-premises Web Client to find actions, pages, and reports, but not documentation, or apps and consulting services on AppSource.</span></span> <span data-ttu-id="cdc10-122">Benutzer, die vom Dynamics NAV-Client eine Verbindung mit [!INCLUDE[d365fin](includes/d365fin_md.md)] herstellen, nutzen weiterhin die Seitensuche.</span><span class="sxs-lookup"><span data-stu-id="cdc10-122">Users connecting to [!INCLUDE[d365fin](includes/d365fin_md.md)] from the Dynamics NAV client continue to use Page Search.</span></span>

### <a name="is-tell-me-available-for-all-form-factors"></a><span data-ttu-id="cdc10-123">Ist „Wie möchten Sie weiter verfahren“ für alle Formularfaktoren verfügbar?</span><span class="sxs-lookup"><span data-stu-id="cdc10-123">Is Tell Me available for all form factors?</span></span>
<span data-ttu-id="cdc10-124">„Wie möchten Sie weiter verfahren“ ist nur im Webclient oder der Windows-Desktop-App verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cdc10-124">Tell Me is only available in the Web Client or Windows desktop app.</span></span>

### <a name="are-the-documentation-results-available-in-any-language"></a><span data-ttu-id="cdc10-125">Sind die Dokumentationsergebnisse in jeder Sprache verfügbar?</span><span class="sxs-lookup"><span data-stu-id="cdc10-125">Are the documentation results available in any language?</span></span>
<span data-ttu-id="cdc10-126">Die Hilfeartikelanzeige werden in der Sprache angezeigt, die Sie in **Meine Einstellungen** angegeben haben, sofern die Hilfe in diese Sprache verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="cdc10-126">The help articles display in the language you have specified in **My Settings**, if help is available in that language.</span></span>

## <a name="see-also"></a><span data-ttu-id="cdc10-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cdc10-127">See Also</span></span>  
[<span data-ttu-id="cdc10-128">Suchen von Funktionen und Informationen</span><span class="sxs-lookup"><span data-stu-id="cdc10-128">Finding Features and Information</span></span>](ui-search.md)
