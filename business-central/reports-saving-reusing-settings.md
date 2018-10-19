---
title: "Ausgleichen und ändern Sie Einstellungen in gespeicherten Berichten | Microsoft Docs"
description: Beschreibt vordefinierte Optionen und filtert, um einen Bericht anzupassen und die richtigen Daten zu generieren.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 6027ba17868aca0a6571e059c9d157c542d12823
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="managing-saved-settings-on-reports"></a><span data-ttu-id="0b589-103">Gespeicherte Einstellungen in Berichtenn verwalten</span><span class="sxs-lookup"><span data-stu-id="0b589-103">Managing Saved Settings on Reports</span></span>
<span data-ttu-id="0b589-104">Abhängig vom ausgeführten Bericht, erhalten Benutzer in der Regel eine Seite, für die Sie bestimmte Optionen festlegen und filtern können, um Daten zu ändern, die im erstellten Bericht enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="0b589-104">When running a reports, users are typically presented with a page that lets them set certain options and filters for changing the data that is included in the generated report.</span></span> <span data-ttu-id="0b589-105">Diese Seite ist die Berichtanfordearungsseite.</span><span class="sxs-lookup"><span data-stu-id="0b589-105">This page is called the report request page.</span></span> <span data-ttu-id="0b589-106">Ein Bericht kann eine oder mehrere *Gespeicherte Einstellungen* enthalten, die Benutzer auf den Bericht von der Anforderungsseite anwenden können.</span><span class="sxs-lookup"><span data-stu-id="0b589-106">A report can include one or more *saved settings* that users can apply to the report from the request page.</span></span> <span data-ttu-id="0b589-107">*Gespeicherte Einstellungen* sind grundsätzlich vordefinierte Optionen und Filter.</span><span class="sxs-lookup"><span data-stu-id="0b589-107">*Saved settings* are basically predefined options and filters.</span></span> <span data-ttu-id="0b589-108">Die Verwendung von gespeicherten Einstellungen ist eine schnelle und zuverlässige Art, Berichte zu erstellen, die die richtigen Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="0b589-108">Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data.</span></span> <span data-ttu-id="0b589-109">Weitere Informationen darüber, wie gespeicherte Einstellungen verwendet werden können, erfahren Sie unter [Gespeicherte Einstellungen nutzen](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="0b589-109">For more information about how saved settings are used, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

<span data-ttu-id="0b589-110">Wenn Sie die richtigen Berechtigungen haben, können Sie die gespeicherten Einstellungen für alle Berichte für alle Benutzer im Unternehmen anzeigen, erstellen und bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="0b589-110">If you have the proper permissions, you can view, create, and modify the saved settings for all reports for all users in company.</span></span> <span data-ttu-id="0b589-111">Sie können gespeicherte Einstellungen für einen Bericht den einzelnen Benutzern oder allen Benutzern im Unternehmen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="0b589-111">You can assign saved settings for a report to individual users or all users in the company.</span></span>

<!-- 
## Apply saved settings to a report
1. Open the report.

   The report request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="create-and-modify-saved-settings-for-all-users"></a><span data-ttu-id="0b589-112">Erstellen und Ändern gespeicherter Einstellungen für alle Benutzer</span><span class="sxs-lookup"><span data-stu-id="0b589-112">Create and modify saved settings for all users</span></span>
<span data-ttu-id="0b589-113">Sie können gespeicherte Einstellungen der Seite **1560 Berichteinstellungen** verwalten.</span><span class="sxs-lookup"><span data-stu-id="0b589-113">You manage saved settings from page **1560 Reports Settings**.</span></span> <span data-ttu-id="0b589-114">Es gibt zwei Möglichkeiten, dies Seite zu öffnen:</span><span class="sxs-lookup"><span data-stu-id="0b589-114">There are two ways to open this page:</span></span>
-   <span data-ttu-id="0b589-115">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Berichtseinstellungen** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="0b589-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Settings**, and then choose the related link.</span></span>
-   <span data-ttu-id="0b589-116">Öffnen Sie einen Bericht, wählen die Suche neben dem Feld **Verwendete Standardwerte aus:** aus, wählen Sie **Aus vollständiger Liste auswählen** aus.</span><span class="sxs-lookup"><span data-stu-id="0b589-116">Open a report, choose the lookup next to the **Used default values from:** box, choose **Select from full list**.</span></span>

<span data-ttu-id="0b589-117">Die Seitendarstellungen zeigt alle vorhandenen Abwehreinstellungsposten für alle Anwender an.</span><span class="sxs-lookup"><span data-stu-id="0b589-117">The page displays all the existing save settings entries for all users.</span></span> <span data-ttu-id="0b589-118">Wenn es einen Benutzernamen in der Spalte **Zugewiesen zu** hat, kann nur der Benutzer die gespeicherten Einstellungen für den entsprechenden Bericht verwenden.</span><span class="sxs-lookup"><span data-stu-id="0b589-118">If there is a user name in the **Assigned to** column, only that user can use the saved settings for the associated report.</span></span> <span data-ttu-id="0b589-119">Wenn sich ein Häkchen im Feld **Anteil mit allen Benutzern** befindet, können alle Benutzer die  gespeicherten Einstellungen für den Bericht verwenden.</span><span class="sxs-lookup"><span data-stu-id="0b589-119">If there is a check mark in the **Share with all users** column, all users can use the saved settings for the report.</span></span>

<span data-ttu-id="0b589-120">Von der Seite **Berichts-Einstellungen** können Sie:</span><span class="sxs-lookup"><span data-stu-id="0b589-120">From the **Report Settings** window, you can:</span></span>
-   <span data-ttu-id="0b589-121">**Neu** auswählen, um neue gespeicherte Einstellungen von Grund auf neu zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0b589-121">Choose **New** to create a new saved settings entry from scratch.</span></span>
-   <span data-ttu-id="0b589-122">Wählen Sie einen Einstellungsposten aus der Liste aus, und wählen Sie **Kopieren**, um eine Kopie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0b589-122">Select a saved settings entry from the list, and choose **Copy** to create a copy.</span></span>
-   <span data-ttu-id="0b589-123">Wählen Sie einen Einstellungsposten aus der Liste aus, und wählen Sie **Bearbeiten**, um einen gespeicherten Einstellungsposten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="0b589-123">Select a saved settings entry from the list, and choose **Edit** to modify a saved settings entry.</span></span>


> [!Important]
> <span data-ttu-id="0b589-124">Berücksichtigt den Namen, den Sie einem gespeicherten Einstellungsposten geben.</span><span class="sxs-lookup"><span data-stu-id="0b589-124">Consider the name that you give a saved settings entry.</span></span> <span data-ttu-id="0b589-125">Wenn Sie einen gespeicherten Einstellungsartikel für alle Benutzer erstellen und er denselben Namen wie bestehende gespeicherte Einstellungen für einen bestimmten Benutzer hat, ist dieser Benutzer nicht dazu in der Lage, die gespeicherten Einstellungen zu verwenden, die jedem zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0b589-125">If you create a saved settings entry for all users, and you give it the same name as an existing saved settings entry that is assigned to a specific user only, then that user will not be able to use the saved settings entry that is assigned to everyone.</span></span>  <span data-ttu-id="0b589-126">Im Feld **Gespeicherte Einstellungen** auf der Berichtsanforderungsseite werden dem Benutzer auch zwei Optionen gespeicherter Einstellungen mit demselben Namen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0b589-126">Under **Saved Settings** on the report request page, the user will see two saved settings entries with the same name.</span></span> <span data-ttu-id="0b589-127">Jedoch gleichgültig welche Option er auswählt, werden die benutzerspezifischen gespeicherten Einstellungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="0b589-127">However, no matter which option he chooses, the user-specific saved settings entry will be used.</span></span>

> [!NOTE]
> <span data-ttu-id="0b589-128">Die gespeicherte Einstellungsfunktion in Berichten ist nur relevant, wenn die [SaveValues-Eigenschaft](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property) der Anforderungsseite mit `Yes` festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0b589-128">The saved settings feature is available only on reports where the [SaveValues property](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property) of the report's request page is set to `Yes`.</span></span> <span data-ttu-id="0b589-129">Die **SaveValues**-Eigenschaft wird in der Entwicklungsumgebung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0b589-129">The **SaveValues** property is set in the development environment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0b589-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b589-130">See Also</span></span>
[<span data-ttu-id="0b589-131">Arbeiten mit Berichten</span><span class="sxs-lookup"><span data-stu-id="0b589-131">Working with Reports</span></span>](ui-work-report.md)  

