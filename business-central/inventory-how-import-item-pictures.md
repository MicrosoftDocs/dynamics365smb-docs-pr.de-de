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
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: fa859d3e350cedb845df47521ee58ba8d2e4aade
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "940167"
---
# <a name="import-multiple-item-pictures"></a>Mehrere Artikelbilder importieren
Sie können mehrere Artikelbilder in einem Durchgang importieren. Benennen Sie einfach Ihre Bilddateien mit Namen entsprechend zu Ihren Artikelnummern, komprimieren Sie sie in einer ZIP-Datei und verwenden Sie dann die Seite **Artikelbilder importieren**, um zu verwalten, welche Artikel importiert werden sollen.

Alle gängigen Dateiformate werden unterstützt.

## <a name="to-name-picture-files-by-the-item-names-and-prepare-the-zip-file"></a>So benennen Sie Bilddateien anhand des Artikelnamens und bereiten die ZIP-Datei vor:
1. Gehen Sie zu dem Ort, an dem Ihre Artikelbilder gespeichert sind, und benennen Sie die einzelnen Dateien entsprechend der Nummer des zugehörigen Artikels. Beispiel:

    |Artikelnr.|Dateiname|
    |-|-|
    |1000|1000.bmp|
    |1001|1001.bmp|
    |1002|1002.bmp|

2. Sammeln Sie alle Dateien in einer ZIP-Datei. Wählen Sie zum Beispiel in Windows Explorer die Dateien und dann **Senden an**, **Komprimierter (gezippter) Ordner** aus.     

## <a name="to-import-item-pictures"></a>So importieren Sie Artikelbilder
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Lagereinrichtung** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Artikelbilder importieren** aus.
3. Wählen Sie im Feld **ZIP-Datei auswählen** den relevanten ZIP-Ordner und dann die Schaltfläche **Öffnen** aus.

    Eine Zeile für jeden Artikel und jedes Bild wurde auf der Seite **Artikelbilder importieren** erstellt.

    > [!NOTE]
    > Für Artikelkarten, die bereits ein Bild haben, wird das Kontrollkästchen **Bild bereits vorhanden** aktiviert. Wenn keine vorhandenen Bilder ersetzt werden sollen, entfernen Sie das Häkchen aus dem Kontrollkästchen **Bilder ersetzen**. Wenn einzelne vorhandene Bilder nicht ersetzt werden sollen, löschen Sie die entsprechenden Zeilen.

3. Wählen Sie die Aktion **Bilder importieren** aus.

Das Feld **Importstatus** wird aktualisiert, um anzuzeigen, ob der Bildimport übersprungen oder abgeschlossen wurde.       

## <a name="see-also"></a>Siehe auch
[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Erstellen von Nummernkreisen](ui-create-number-series.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
