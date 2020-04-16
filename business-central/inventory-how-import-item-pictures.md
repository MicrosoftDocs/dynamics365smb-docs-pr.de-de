---
title: Importieren vieler Artikelbilder über eine ZIP-Datei | Microsoft Docs
description: Sie können mehrere Artikelbilder in einem Durchgang importieren. Benennen Sie einfach Ihre Bilddateien mit Namen entsprechend zu Ihren Artikelnummern, komprimieren Sie sie in einer ZIP-Datei und verwenden Sie dann die Seite „Artikelbilder importieren”, um zu verwalten, welche Artikel importiert werden sollen.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: product, image
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 8478a6fc2a4860f2cd5a2b5a01d6680fbaea3130
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182180"
---
# <a name="import-multiple-item-pictures"></a><span data-ttu-id="a2745-104">Mehrere Artikelbilder importieren</span><span class="sxs-lookup"><span data-stu-id="a2745-104">Import Multiple Item Pictures</span></span>
<span data-ttu-id="a2745-105">Sie können mehrere Artikelbilder in einem Durchgang importieren.</span><span class="sxs-lookup"><span data-stu-id="a2745-105">You can import multiple item pictures in one go.</span></span> <span data-ttu-id="a2745-106">Benennen Sie einfach Ihre Bilddateien mit Namen entsprechend zu Ihren Artikelnummern, komprimieren Sie sie in einer ZIP-Datei und verwenden Sie dann die Seite **Artikelbilder importieren**, um zu verwalten, welche Artikel importiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a2745-106">Simply name your picture files with names corresponding to your item numbers, compress them to a ZIP file, and then use the **Import Item Pictures** page to manage which item pictures to import.</span></span>

<span data-ttu-id="a2745-107">Alle gängigen Dateiformate werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a2745-107">All common file formats are supported.</span></span>

## <a name="to-name-picture-files-by-the-item-names-and-prepare-the-zip-file"></a><span data-ttu-id="a2745-108">So benennen Sie Bilddateien anhand des Artikelnamens und bereiten die ZIP-Datei vor:</span><span class="sxs-lookup"><span data-stu-id="a2745-108">To name picture files by the item names and prepare the ZIP file</span></span>
1. <span data-ttu-id="a2745-109">Gehen Sie zu dem Ort, an dem Ihre Artikelbilder gespeichert sind, und benennen Sie die einzelnen Dateien entsprechend der Nummer des zugehörigen Artikels.</span><span class="sxs-lookup"><span data-stu-id="a2745-109">At the location where your item pictures are stored, name each files according to the number of the related item.</span></span> <span data-ttu-id="a2745-110">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="a2745-110">For example:</span></span>

    |<span data-ttu-id="a2745-111">Artikelnr.</span><span class="sxs-lookup"><span data-stu-id="a2745-111">Item No.</span></span>|<span data-ttu-id="a2745-112">Dateiname</span><span class="sxs-lookup"><span data-stu-id="a2745-112">File Name</span></span>|
    |-|-|
    |<span data-ttu-id="a2745-113">1000</span><span class="sxs-lookup"><span data-stu-id="a2745-113">1000</span></span>|<span data-ttu-id="a2745-114">1000.bmp</span><span class="sxs-lookup"><span data-stu-id="a2745-114">1000.bmp</span></span>|
    |<span data-ttu-id="a2745-115">1001</span><span class="sxs-lookup"><span data-stu-id="a2745-115">1001</span></span>|<span data-ttu-id="a2745-116">1001.bmp</span><span class="sxs-lookup"><span data-stu-id="a2745-116">1001.bmp</span></span>|
    |<span data-ttu-id="a2745-117">1002</span><span class="sxs-lookup"><span data-stu-id="a2745-117">1002</span></span>|<span data-ttu-id="a2745-118">1002.bmp</span><span class="sxs-lookup"><span data-stu-id="a2745-118">1002.bmp</span></span>|

2. <span data-ttu-id="a2745-119">Sammeln Sie alle Dateien in einer ZIP-Datei.</span><span class="sxs-lookup"><span data-stu-id="a2745-119">Collect all the files in a ZIP file.</span></span> <span data-ttu-id="a2745-120">Wählen Sie zum Beispiel in Windows Explorer die Dateien und dann **Senden an**, **Komprimierter (gezippter) Ordner** aus.</span><span class="sxs-lookup"><span data-stu-id="a2745-120">For example, in Windows Explorer, select the files, and then choose **Send to**, **Compressed (zipped) folder**.</span></span>     

## <a name="to-import-item-pictures"></a><span data-ttu-id="a2745-121">So importieren Sie Artikelbilder</span><span class="sxs-lookup"><span data-stu-id="a2745-121">To import item pictures</span></span>
1. <span data-ttu-id="a2745-122">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") Symbol öffnet, geben Sie **Bestandseinrichtung** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="a2745-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="a2745-123">Wählen Sie die Aktion **Artikelbilder importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="a2745-123">Choose the **Import Item Pictures** action.</span></span>
3. <span data-ttu-id="a2745-124">Wählen Sie im Feld **ZIP-Datei auswählen** den relevanten ZIP-Ordner und dann die Schaltfläche **Öffnen** aus.</span><span class="sxs-lookup"><span data-stu-id="a2745-124">In the **Select a ZIP file** field, select the relevant ZIP folder, and then choose the **Open** button.</span></span>

    <span data-ttu-id="a2745-125">Eine Zeile für jeden Artikel und jedes Bild wurde auf der Seite **Artikelbilder importieren** erstellt.</span><span class="sxs-lookup"><span data-stu-id="a2745-125">A line for each item and picture is created on the **Import Item Pictures** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a2745-126">Für Artikelkarten, die bereits ein Bild haben, wird das Kontrollkästchen **Bild bereits vorhanden** aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a2745-126">For item cards that already have a picture, the **Picture Already Exists** check box is selected.</span></span> <span data-ttu-id="a2745-127">Wenn keine vorhandenen Bilder ersetzt werden sollen, entfernen Sie das Häkchen aus dem Kontrollkästchen **Bilder ersetzen**.</span><span class="sxs-lookup"><span data-stu-id="a2745-127">If you do not want any existing pictures to be replaced, deselect the **Replace Pictures** check box.</span></span> <span data-ttu-id="a2745-128">Wenn einzelne vorhandene Bilder nicht ersetzt werden sollen, löschen Sie die entsprechenden Zeilen.</span><span class="sxs-lookup"><span data-stu-id="a2745-128">If you do not want individual existing pictures to be replaced, delete the lines in question.</span></span>

3. <span data-ttu-id="a2745-129">Wählen Sie die Aktion **Bilder importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="a2745-129">Choose the **Import Pictures** action.</span></span>

<span data-ttu-id="a2745-130">Das Feld **Importstatus** wird aktualisiert, um anzuzeigen, ob der Bildimport übersprungen oder abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="a2745-130">The **Import Status** field is updated to show if the picture import was skipped or completed.</span></span>       

## <a name="see-also"></a><span data-ttu-id="a2745-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2745-131">See Also</span></span>
[<span data-ttu-id="a2745-132">Neue Artikel registrieren</span><span class="sxs-lookup"><span data-stu-id="a2745-132">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="a2745-133">Erstellen von Nummernkreisen</span><span class="sxs-lookup"><span data-stu-id="a2745-133">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="a2745-134">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="a2745-134">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="a2745-135">Einkauf</span><span class="sxs-lookup"><span data-stu-id="a2745-135">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="a2745-136">Verkauf</span><span class="sxs-lookup"><span data-stu-id="a2745-136">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="a2745-137">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a2745-137">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
