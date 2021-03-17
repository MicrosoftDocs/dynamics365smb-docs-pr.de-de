---
title: Häufig gestellte Fragen zu „Wie möchten Sie weiter verfahren“ | Microsoft Docs
description: Dieser Artikel bietet Antworten zu den häufig von unseren Partner und Debitoren über „Wie möchten Sie weiter verfahren“ gestellten Fragen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: ad9aa62555a6296ec03cc93d8488855ab1e46d88
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5380738"
---
# <a name="tell-me-faq"></a><span data-ttu-id="a157b-103">Häufig gestellte Fragen zu „Wie möchten Sie weiter verfahren“</span><span class="sxs-lookup"><span data-stu-id="a157b-103">Tell Me FAQ</span></span>
<span data-ttu-id="a157b-104">In diesem Thema werden Fragen beantwortet, die unsere erfahrenen Benutzer häufig zu der Funktion "Wie möchten Sie weiter verfahren" stellen.</span><span class="sxs-lookup"><span data-stu-id="a157b-104">This topic answers questions that our advanced users often ask about the Tell Me feature.</span></span>

### <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a><span data-ttu-id="a157b-105">Werden alle Aktionen meiner aktuellen Seite von „Wie möchten Sie weiter verfahren“ abgedeckt?</span><span class="sxs-lookup"><span data-stu-id="a157b-105">Are all actions from my current page discoverable in Tell Me?</span></span>
<span data-ttu-id="a157b-106">Nein.</span><span class="sxs-lookup"><span data-stu-id="a157b-106">No.</span></span> <span data-ttu-id="a157b-107">Aktionen in Zeilen, z. B. der insgesamt, Verkaufszeilen-Teil der FactBoxes werden in „Wie möchten Sie weiter verfahren“ nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a157b-107">Actions in parts, such as the Sales Lines part or FactBoxes, are not displayed in Tell Me.</span></span>

### <a name="are-the-results-in-tell-me-filtered-by-permissions"></a><span data-ttu-id="a157b-108">Werden die Ergebnisse in „Wie möchten Sie weiter verfahren“ nach Berechtigungen gefiltert?</span><span class="sxs-lookup"><span data-stu-id="a157b-108">Are the results in Tell Me filtered by permissions?</span></span>
<span data-ttu-id="a157b-109">Wenn der Benutzer nicht über AccessByPermissions verfügt, werden keine Aktionen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a157b-109">If the user does not have AccessByPermissions then actions are not displayed.</span></span> <span data-ttu-id="a157b-110">Allerdings werden Seiten und Berichte in den Ergebnissen angezeigt. Der Benutzer benötigt jedoch die Berechtigungen, auf sie zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="a157b-110">However, pages and reports appear in the results but require that the user has permission to access them.</span></span> <span data-ttu-id="a157b-111">Es wird eine Meldung angezeigt, wenn der Benutzer, nicht über die Berechtigungen zum Anzeigen des Objekts verfügt.</span><span class="sxs-lookup"><span data-stu-id="a157b-111">A message will display if the user does not have permission to view the object.</span></span>

### <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a><span data-ttu-id="a157b-112">Zeigt „Wie möchten Sie weiter verfahren“ Inhalt von meinen Anpassungen oder installierten Drittanbietererweiterungen an?</span><span class="sxs-lookup"><span data-stu-id="a157b-112">Does Tell Me display content from my customizations or installed third-party extensions?</span></span>
<span data-ttu-id="a157b-113">Aktionen, Seiten und Berichte, die aus Erweiterungen stammen, werden von „Wie möchten Sie weiter verfahren“ erkannt, angepasste Hilfedokumente allerdings nicht.</span><span class="sxs-lookup"><span data-stu-id="a157b-113">Actions, pages, and reports that originate from extensions are picked up by Tell Me, but custom help documentation is not.</span></span> <span data-ttu-id="a157b-114">Technische Informationen darüber, wie benutzerdefinierte Seiten und Berichte feststellbar gemacht werden, finden Sie unter [Hinzufügen von Seiten und Berichten zur Suche](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).</span><span class="sxs-lookup"><span data-stu-id="a157b-114">For technical information about how to make custom pages and reports discoverable, see [Adding Pages and Reports to Search](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).</span></span>

### <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a><span data-ttu-id="a157b-115">Worin unterschiedet sich dies von der vorherigen Funktion, die als Seitensuche bekannt war?</span><span class="sxs-lookup"><span data-stu-id="a157b-115">What makes this different from what was previously known as Page Search?</span></span>
<span data-ttu-id="a157b-116">Die Seitensuche wurde zu „Wie möchten Sie weiter verfahren“ weiterentwickelt, damit Sie schneller arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="a157b-116">Page Search has evolved into Tell Me to help you get work done quickly.</span></span> <span data-ttu-id="a157b-117">Die Seitensuche konnte Ihnen nur bei der Navigation in Seiten oder Berichten helfen.</span><span class="sxs-lookup"><span data-stu-id="a157b-117">Page Search could only help you navigate to pages or reports.</span></span> <span data-ttu-id="a157b-118">Auf technischer Ebene basiert „Wie möchten Sie weiter verfahren“ nicht mehr auf dem vorherigen MenuSuite-Konzept.</span><span class="sxs-lookup"><span data-stu-id="a157b-118">At a technical level, Tell Me is no longer based on the legacy MenuSuite concept.</span></span>

### <a name="i-use-on-premises-prod_short-does-that-include-tell-me"></a><span data-ttu-id="a157b-119">Ich verwende [!INCLUDE[prod_short](includes/prod_short.md)] lokal.</span><span class="sxs-lookup"><span data-stu-id="a157b-119">I use on-premises [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="a157b-120">Schließt das „Wie möchten Sie weiter verfahren“ ein?</span><span class="sxs-lookup"><span data-stu-id="a157b-120">Does that include Tell Me?</span></span>
<span data-ttu-id="a157b-121">Sie können „Wie möchten Sie weiter verfahren“ mit dem lokalen Webclient verwenden, um nach Aktionen, Seiten und Berichten zu suchen, aber nicht nach Dokumentation oder Apps und Beratungsdiensten auf AppSource.</span><span class="sxs-lookup"><span data-stu-id="a157b-121">You can use Tell Me in the on-premises Web Client to find actions, pages, and reports, but not documentation, or apps and consulting services on AppSource.</span></span>

### <a name="is-tell-me-available-for-all-form-factors"></a><span data-ttu-id="a157b-122">Ist „Wie möchten Sie weiter verfahren“ für alle Formularfaktoren verfügbar?</span><span class="sxs-lookup"><span data-stu-id="a157b-122">Is Tell Me available for all form factors?</span></span>
<span data-ttu-id="a157b-123">„Wie möchten Sie weiter verfahren“ ist nur im Webclient oder der Windows-Desktop-App verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a157b-123">Tell Me is only available in the Web Client or Windows desktop app.</span></span>

### <a name="are-the-documentation-results-available-in-any-language"></a><span data-ttu-id="a157b-124">Sind die Dokumentationsergebnisse in jeder Sprache verfügbar?</span><span class="sxs-lookup"><span data-stu-id="a157b-124">Are the documentation results available in any language?</span></span>
<span data-ttu-id="a157b-125">Die Hilfeartikelanzeige werden in der Sprache angezeigt, die Sie in **Meine Einstellungen** angegeben haben, sofern die Hilfe in diese Sprache verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a157b-125">The help articles display in the language you have specified in **My Settings**, if help is available in that language.</span></span>

### <a name="why-dont-i-see-a-bookmark-icon-for-my-search-results"></a><span data-ttu-id="a157b-126">Warum sehe ich kein Lesezeichensymbol für meine Suchergebnisse?</span><span class="sxs-lookup"><span data-stu-id="a157b-126">Why don't I see a bookmark icon for my search results?</span></span>
<span data-ttu-id="a157b-127">Das Lesezeichensymbol wird im Benachrichtigungsfenster nicht angezeigt, wenn die Personalisierung für eine Benutzerrolle deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a157b-127">The bookmark icon is not displayed in the Tell Me window when personalization is disabled for a user role.</span></span>


## <a name="see-also"></a><span data-ttu-id="a157b-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a157b-128">See Also</span></span>  
[<span data-ttu-id="a157b-129">Speichern und personalisieren Sie Listenansichten</span><span class="sxs-lookup"><span data-stu-id="a157b-129">Save and Personalize List Views</span></span>](ui-views.md)  
[<span data-ttu-id="a157b-130">Suche nach Seiten und Informationen mit Tell Me</span><span class="sxs-lookup"><span data-stu-id="a157b-130">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
[<span data-ttu-id="a157b-131">Suche nach Seiten mit dem Rollen-Explorer</span><span class="sxs-lookup"><span data-stu-id="a157b-131">Finding Pages with the Role Explorer</span></span>](ui-role-explorer.md)  
[<span data-ttu-id="a157b-132">Erstellen eines Lesezeichens für eine Seite oder einen Bericht im Rollencenter</span><span class="sxs-lookup"><span data-stu-id="a157b-132">Bookmark a Page or Report on Your Role Center</span></span>](ui-bookmarks.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]