---
title: Ausgleichen und ändern Sie Einstellungen in gespeicherten Berichten | Microsoft Docs
description: Beschreibt vordefinierte Optionen und filtert, um einen Bericht anzupassen und die richtigen Daten zu generieren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: a9bb72a85fb49b4316af2160e5823fbf77a18cbf
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2881401"
---
# <a name="manage-saved-settings-for-reports-and-batch-jobs"></a><span data-ttu-id="3e22a-103">Gespeicherte Einstellungen für Berichte und Stapelaufträge verwalten</span><span class="sxs-lookup"><span data-stu-id="3e22a-103">Manage Saved Settings for Reports and Batch jobs</span></span>
<span data-ttu-id="3e22a-104">Abhängig vom ausgeführten Bericht, erhalten Benutzer in der Regel eine Seite, für die Sie bestimmte Optionen wählen und Filter festlegen können, um Daten zu ändern, die im erstellten Bericht enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="3e22a-104">When running reports, users are typically presented with a page that lets them select options and set filters to change the data that is included in the generated report.</span></span> <span data-ttu-id="3e22a-105">Dies ist die Berichtanfordearungsseite.</span><span class="sxs-lookup"><span data-stu-id="3e22a-105">This page is called the request page.</span></span> <span data-ttu-id="3e22a-106">Ein Bericht kann eine oder mehrere *Gespeicherte Einstellungen* enthalten, die Benutzer auf den Bericht von der Anforderungsseite anwenden können.</span><span class="sxs-lookup"><span data-stu-id="3e22a-106">A report can include one or more *saved settings* that users can apply to the report from the request page.</span></span> <span data-ttu-id="3e22a-107">*Gespeicherte Einstellungen* sind grundsätzlich vordefinierte Optionen und Filter.</span><span class="sxs-lookup"><span data-stu-id="3e22a-107">*Saved settings* are basically predefined options and filters.</span></span> <span data-ttu-id="3e22a-108">Die Verwendung von gespeicherten Einstellungen ist eine schnelle und zuverlässige Art, Berichte zu erstellen, die die richtigen Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="3e22a-108">Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data.</span></span> <span data-ttu-id="3e22a-109">Weitere Informationen finden Sie unter [Gespeicherte Einstellungen verwenden](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="3e22a-109">For more information, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

> [!NOTE]
> <span data-ttu-id="3e22a-110">Dieses Thema bezieht sich hauptsächlich auf "Bericht", aber die gleichen Informationen gelten für Stapelverarbeitungen.</span><span class="sxs-lookup"><span data-stu-id="3e22a-110">This topic refers mainly to "report", but similar information applies to batch jobs.</span></span>

<span data-ttu-id="3e22a-111">Wenn Sie die richtigen Berechtigungen haben, können Sie die gespeicherten Einstellungen für alle Berichte für alle Benutzer in einem Unternehmen anzeigen, erstellen und bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="3e22a-111">If you have the proper permissions, you can view, create, and modify the saved settings for all reports for all users in a company.</span></span> <span data-ttu-id="3e22a-112">Sie können gespeicherte Einstellungen für einen Bericht entweder den einzelnen Benutzern oder allen Benutzern im Unternehmen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="3e22a-112">You can assign saved settings for a report to individual users or to all users in the company.</span></span>

<!--
## Apply saved settings to a report
1. Open the report.

   The request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="to-create-and-modify-saved-settings-for-all-users"></a><span data-ttu-id="3e22a-113">Um gespeicherter Einstellungen für alle Benutzer zu erstellen oder zu ändern</span><span class="sxs-lookup"><span data-stu-id="3e22a-113">To create and modify saved settings for all users</span></span>
<span data-ttu-id="3e22a-114">Sie können gespeicherte Einstellungen auf der Seite **Berichteinstellungen** verwalten.</span><span class="sxs-lookup"><span data-stu-id="3e22a-114">You manage saved settings on the **Reports Settings** page.</span></span> <span data-ttu-id="3e22a-115">Es gibt zwei Möglichkeiten, dies Seite zu öffnen:</span><span class="sxs-lookup"><span data-stu-id="3e22a-115">There are two ways to open this page:</span></span>
-   <span data-ttu-id="3e22a-116">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Berichtseinstellungen** ein, und wählen Sie dann den zugehörigen Link.</span><span class="sxs-lookup"><span data-stu-id="3e22a-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Settings**, and then choose the related link.</span></span>
-   <span data-ttu-id="3e22a-117">Öffnen Sie einen Bericht, wählen die Suche neben dem Feld **Verwendete Standardwerte verwenden aus** aus und wählen Sie **Aus vollständiger Liste auswählen** aus.</span><span class="sxs-lookup"><span data-stu-id="3e22a-117">Open a report, choose the lookup in the **Use default values from** field, and then choose the **Select from full list** action.</span></span>

<span data-ttu-id="3e22a-118">Die Seitendarstellungen zeigt alle gespeicherten Einstellungseingaben für alle Anwender an.</span><span class="sxs-lookup"><span data-stu-id="3e22a-118">The page displays all the existing saved settings entries for all users.</span></span> <span data-ttu-id="3e22a-119">Wenn es einen Benutzernamen im Feld **Zugewiesen zu** hat, kann nur der Benutzer die gespeicherten Einstellungen für den entsprechenden Bericht verwenden.</span><span class="sxs-lookup"><span data-stu-id="3e22a-119">If there is a user name in the **Assigned to** field, only that user can use the saved settings for the associated report.</span></span> <span data-ttu-id="3e22a-120">Wenn sich ein Häkchen im Feld **Mit allen Benutzern teilen** befindet, können alle Benutzer die gespeicherten Einstellungen für den Bericht verwenden.</span><span class="sxs-lookup"><span data-stu-id="3e22a-120">If there is a check mark in the **Share with all users** field, all users can use the saved settings for the report.</span></span>

<span data-ttu-id="3e22a-121">Von der Seite **Berichts-Einstellungen** können Sie:</span><span class="sxs-lookup"><span data-stu-id="3e22a-121">From the **Report Settings** page, you can:</span></span>
-   <span data-ttu-id="3e22a-122">Die Aktion **Neu** auswählen, um neue gespeicherte Einstellungen von Grund auf neu zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3e22a-122">Choose the **New** action to create a new saved settings entry from scratch.</span></span>
-   <span data-ttu-id="3e22a-123">Wählen Sie einen Einstellungsposten aus der Liste aus, und wählen Sie die Aktion **Kopieren**, um eine Kopie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3e22a-123">Select a saved settings entry from the list, and choose the **Copy** action to create a copy.</span></span>
-   <span data-ttu-id="3e22a-124">Wählen Sie einen Einstellungsposten aus der Liste aus, und wählen Sie die Aktion **Bearbeiten**, um einen gespeicherten Einstellungsposten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="3e22a-124">Select a saved settings entry from the list, and choose the **Edit** action to modify a saved settings entry.</span></span>

> [!Important]
> <span data-ttu-id="3e22a-125">Berücksichtigt den Namen, den Sie einem gespeicherten Einstellungsposten geben.</span><span class="sxs-lookup"><span data-stu-id="3e22a-125">Consider the name that you give a saved settings entry.</span></span> <span data-ttu-id="3e22a-126">Wenn Sie einen gespeicherten Einstellungsartikel für alle Benutzer erstellen und er denselben Namen wie bestehende gespeicherte Einstellungen für einen bestimmten Benutzer hat, ist dieser Benutzer nicht dazu in der Lage, die gespeicherten Einstellungen zu verwenden, die jedem zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3e22a-126">If you create a saved settings entry for all users, and you give it the same name as an existing saved settings entry that is assigned to a specific user only, then that user will not be able to use the saved settings entry that is assigned to everyone.</span></span>  <span data-ttu-id="3e22a-127">Im Abschnitt **Gespeicherte Einstellungen** auf der Berichtsanforderungsseite werden dem Benutzer auch zwei Optionen gespeicherter Einstellungen mit demselben Namen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3e22a-127">In the **Saved Settings** section on the request page, the user will see two saved settings entries with the same name.</span></span> <span data-ttu-id="3e22a-128">Jedoch gleichgültig welche Option sie auswählen, werden die benutzerspezifischen gespeicherten Einstellungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="3e22a-128">However, no matter which option they choose, the user-specific saved settings entry will be used.</span></span>

> [!NOTE]
> <span data-ttu-id="3e22a-129">Die gespeicherte Einstellungsfunktion in Berichten ist nur relevant, wenn die [SaveValues-Eigenschaft](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) der Anforderungsseite mit **Ja** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3e22a-129">The Saved Settings feature is available only on reports where the [SaveValues property](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) of the report's request page is set to **Yes**.</span></span> <span data-ttu-id="3e22a-130">Die **SaveValues**-Eigenschaft wird in der Entwicklungsumgebung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3e22a-130">The **SaveValues** property is set in the development environment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3e22a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e22a-131">See Also</span></span>
[<span data-ttu-id="3e22a-132">Arbeiten mit Berichten, Batchaufträgen und XMLports</span><span class="sxs-lookup"><span data-stu-id="3e22a-132">Working with Reports, Batch Jobs, and XMLports</span></span>](ui-work-report.md)  
