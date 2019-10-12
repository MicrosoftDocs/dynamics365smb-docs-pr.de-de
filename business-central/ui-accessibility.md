---
title: Assistive Funktionen
description: Tastenkombinationen und andere assistive Funktionen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: cb898a459bdf5d0b4ced3baadd2a245cd23b8f38
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2311452"
---
# <a name="accessibility-and-keyboard-shortcuts"></a><span data-ttu-id="861e0-103">Eingabehilfe und Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="861e0-103">Accessibility and Keyboard Shortcuts</span></span>
<span data-ttu-id="861e0-104">Dieses Thema enthält Informationen zu den Funktionen, die [!INCLUDE[d365fin](includes/d365fin_md.md)] einfach verfügbar machen für die Personen mit Behinderungen.</span><span class="sxs-lookup"><span data-stu-id="861e0-104">This topic provides information about the features that make [!INCLUDE[d365fin](includes/d365fin_md.md)] readily available to people with disabilities.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="861e0-105">unterstützt die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="861e0-105">supports the following accessibility features:</span></span>  

-   <span data-ttu-id="861e0-106">Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="861e0-106">Keyboard shortcuts</span></span>

    <span data-ttu-id="861e0-107">Weitere Informationen finden Sie unter [Einrichten von Tastenkombinationen](keyboard-shortcuts.md)</span><span class="sxs-lookup"><span data-stu-id="861e0-107">For more information, see [Keyboard Shortcuts](keyboard-shortcuts.md)</span></span>

-   <span data-ttu-id="861e0-108">Navigation</span><span class="sxs-lookup"><span data-stu-id="861e0-108">Navigation</span></span>  

-   <span data-ttu-id="861e0-109">Überschrift</span><span class="sxs-lookup"><span data-stu-id="861e0-109">Headings</span></span>  

-   <span data-ttu-id="861e0-110">Alternativer Text für Bilder und Links</span><span class="sxs-lookup"><span data-stu-id="861e0-110">Alternative text for images and links</span></span>  

-   <span data-ttu-id="861e0-111">Unterstützung für allgemeine assistive Technologien</span><span class="sxs-lookup"><span data-stu-id="861e0-111">Support for common assistive technologies</span></span>  

<!-- moved to separate article
##  <a name="Keyboard"></a> Keyboard Shortcuts in the browser
 [!INCLUDE[d365fin](includes/d365fin_md.md)] supports the keyboard shortcuts that are supported by most web browsers. The keyboard shortcuts described here refer to the U.S. keyboard layout. The layout of the keys on other keyboards may not correspond exactly to the keys on a U.S. keyboard.  

|To do this|Press|  
|----------------|-----------|  
|To move focus to the next or previous control or element on a page, such as buttons, fields, or items in a list.|Tab, Shift+Tab|  
|To enable or access the element or control that is in focus.|Enter|  
|To scroll items up and down in a list.|Up Arrow, Down Arrow|  
|To scroll columns of an item left and right in a list.|Left Arrow, Right Arrow|  
|To open a drop-down list or look up a value for a field.|Alt+Down Arrow|  
|To move focus to the next element outside the list.|Ctrl + Enter|  
|To see the transactions that resulted in a calculated value in a field.|Alt+Right Arrow|  

-->

##  <a name="Navigation"></a> <span data-ttu-id="861e0-112">Navigation</span><span class="sxs-lookup"><span data-stu-id="861e0-112">Navigation</span></span>  
 <span data-ttu-id="861e0-113">Sie können zwischen den Registerkarten sowie den Aktionen im Menüband, den Elementen im Navigationsbereich und anderen Steuerelementen auf Seiten [!INCLUDE[d365fin](includes/d365fin_md.md)] und Berichte anhand der Tastatur navigieren.</span><span class="sxs-lookup"><span data-stu-id="861e0-113">You can navigate between the tabs and actions in the ribbon, elements in the navigation bar, and other controls on [!INCLUDE[d365fin](includes/d365fin_md.md)] pages and reports using the keyboard.</span></span> <span data-ttu-id="861e0-114">Um den Fokus einer Registerkarte, einer Aktion oder Steuerung zu verschieben, klicken Sie die TAB-TASTE um Vorwärts zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="861e0-114">To move the focus from one tab, action, or control to another, press the Tab key to move forward.</span></span> <span data-ttu-id="861e0-115">Drücken Sie UMSCHALT+TAB zum zurückgehen.</span><span class="sxs-lookup"><span data-stu-id="861e0-115">Press Shift+Tab to move backward.</span></span>  

 <span data-ttu-id="861e0-116">Durch die Verwendung der Aktivierreihenfolge können Sie zwischen der Hauptbrowserseite und den Dialogfeldern wechseln, die Bestätigung erfordern, beispielsweise die Seite Fenster "Anmeldungen".</span><span class="sxs-lookup"><span data-stu-id="861e0-116">By using the tab order, you can also switch between the main browser page and dialog boxes that request confirmation, for example, or the login page.</span></span>  

##  <a name="Headings"></a> <span data-ttu-id="861e0-117">Überschrift</span><span class="sxs-lookup"><span data-stu-id="861e0-117">Headings</span></span>  
 <span data-ttu-id="861e0-118">Die HTML-Quelle für den [!INCLUDE[d365fin](includes/d365fin_md.md)] Inhalt verwendet Tags, um Benutzern der assistive Technologie zu helfen, die Struktur und den Inhalt der Seite zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="861e0-118">The HTML source for [!INCLUDE[d365fin](includes/d365fin_md.md)] content uses tags to help users of assistive technology to understand the structure and content of the page.</span></span> <span data-ttu-id="861e0-119">So werden beispielsweise für Listenseiten die Spalten in den Spaltenüberschriften und die Kategorien festgelegt und werden mit TITEL-Aattribut innerhalb des Tags festgelegt.</span><span class="sxs-lookup"><span data-stu-id="861e0-119">For example, on list pages, the columns are defined in TH tags and the column headings are set with TITLE attribute inside the tag.</span></span> <span data-ttu-id="861e0-120">Caption für Elementen wie Felder, Infoboxen und Inforegister sind in den Überschriftstags enthalten (H1, H2, H3 und H4).</span><span class="sxs-lookup"><span data-stu-id="861e0-120">Captions for elements, such as FastTabs, FactBoxes, and fields are included in heading tags (H1, H2, H3, and H4).</span></span>  

##  <a name="Images"></a> <span data-ttu-id="861e0-121">Bild und Links</span><span class="sxs-lookup"><span data-stu-id="861e0-121">Image and Links</span></span>  
 <span data-ttu-id="861e0-122">Ein Text für Bilder wird mit dem ALT-Attribut innerhalb des IMG-Tags festgelegt.</span><span class="sxs-lookup"><span data-stu-id="861e0-122">A descriptive text for images is set with the ALT attribute inside the IMG tag.</span></span> <span data-ttu-id="861e0-123">Ein beschreibender Text für Hyperlinks wird mit dem Titelattribut innerhalb des A-Tags festgelegt.</span><span class="sxs-lookup"><span data-stu-id="861e0-123">A descriptive text for hyperlinks is set with the title attribute inside the A tag.</span></span>  

##  <a name="AssistiveTech"></a> <span data-ttu-id="861e0-124">Assistive Technologien</span><span class="sxs-lookup"><span data-stu-id="861e0-124">Assistive Technologies</span></span>  
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="861e0-125">unterstützt verschiedene assistive Technologien, wie kontrastreiches, Sprachausgaben und Spracherkennungs-Software.</span><span class="sxs-lookup"><span data-stu-id="861e0-125">supports various assistive technologies, such as high contrast, screen readers, and voice recognition software.</span></span> <span data-ttu-id="861e0-126">Einige assistive Technologien funktionieren möglicherweise nicht mit bestimmten Elementen«» [!INCLUDE[d365fin](includes/d365fin_md.md)] in Seiten.</span><span class="sxs-lookup"><span data-stu-id="861e0-126">Some assistive technologies may not work well with certain elements in [!INCLUDE[d365fin](includes/d365fin_md.md)] pages.</span></span>  

## <a name="for-more-accessibility-information"></a><span data-ttu-id="861e0-127">Weitere Zugriffsinformationen</span><span class="sxs-lookup"><span data-stu-id="861e0-127">For more accessibility information</span></span>  
<span data-ttu-id="861e0-128">Sie können zusätzliche Informationen über Eingabehilfen mit Microsoft-Produkten und assistiven Technologien der Site [Microsoft-Eingabehilfe](https://go.microsoft.com/fwlink/?LinkId=262160) finden.</span><span class="sxs-lookup"><span data-stu-id="861e0-128">You can find additional information about accessibility with Microsoft products and assistive technologies on the [Microsoft Accessibility](https://go.microsoft.com/fwlink/?LinkId=262160) site.</span></span>

## <a name="see-also"></a><span data-ttu-id="861e0-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="861e0-129">See Also</span></span>
[<span data-ttu-id="861e0-130">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="861e0-130">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="861e0-131">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="861e0-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="861e0-132">Häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="861e0-132">Frequently Asked Questions</span></span>](across-faq.md)  
