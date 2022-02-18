---
title: Importieren vieler Artikelbilder über eine ZIP-Datei
description: Um mehrere Artikelbilder zu importieren, geben Sie den Bilddateien Namen, die den Artikelnummern entsprechen, komprimieren Sie sie in eine ZIP-Datei und verwenden Sie die Seite Artikelbilder importieren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: product, image
ms.search.form: 30, 461
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 5a43d696eab27a72c9f9b3c224d08feb9e99ccf4
ms.sourcegitcommit: 189bf08d7ddf6c8b7ef2c09058c6847aa6e590d3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8059674"
---
# <a name="import-multiple-item-pictures"></a>Mehrere Artikelbilder importieren
Sie können mehrere Artikelbilder in einem Durchgang importieren. Benennen Sie einfach Ihre Bilddateien mit Namen entsprechend zu Ihren Artikelnummern, komprimieren Sie sie in einer ZIP-Datei und verwenden Sie dann die Seite „Artikelbilder importieren”, um zu verwalten, welche Artikel importiert werden sollen.

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
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Lagerbestandseinrichtung** ein und wählen Sie dann den zugehörigen Link.
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
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]