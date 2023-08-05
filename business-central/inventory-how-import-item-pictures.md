---
title: Importieren vieler Artikelbilder über eine ZIP-Datei
description: 'Um mehrere Artikelbilder zu importieren, geben Sie den Bilddateien Namen, die den Artikelnummern entsprechen, komprimieren Sie sie in eine ZIP-Datei und verwenden Sie die Seite Artikelbilder importieren.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'product, image'
ms.search.form: '30, 461'
ms.date: 06/16/2021
ms.author: edupont
---
# Mehrere Artikelbilder importieren
Sie können mehrere Artikelbilder in einem Durchgang importieren. Benennen Sie einfach Ihre Bilddateien mit Namen entsprechend zu Ihren Artikelnummern, komprimieren Sie sie in einer ZIP-Datei und verwenden Sie dann die Seite „Artikelbilder importieren”, um zu verwalten, welche Artikel importiert werden sollen.

Alle gängigen Dateiformate werden unterstützt.

## So benennen Sie Bilddateien anhand des Artikelnamens und bereiten die ZIP-Datei vor:
1. Gehen Sie zu dem Ort, an dem Ihre Artikelbilder gespeichert sind, und benennen Sie die einzelnen Dateien entsprechend der Nummer des zugehörigen Artikels. Beispiel:

    |Artikelnr.|Dateiname|
    |-|-|
    |1000|1000.bmp|
    |1001|1001.bmp|
    |1002|1002.bmp|

2. Sammeln Sie alle Dateien in einer ZIP-Datei. Wählen Sie zum Beispiel in Windows Explorer die Dateien und dann **Senden an**, **Komprimierter (gezippter) Ordner** aus.     

## So importieren Sie Artikelbilder
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Lagerbestandseinrichtung** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Artikelbilder importieren** aus.
3. Wählen Sie im Feld **ZIP-Datei auswählen** den relevanten ZIP-Ordner und dann die Schaltfläche **Öffnen** aus.

    Eine Zeile für jeden Artikel und jedes Bild wurde auf der Seite **Artikelbilder importieren** erstellt.

    > [!NOTE]
    > Für Artikelkarten, die bereits ein Bild haben, wird das Kontrollkästchen **Bild bereits vorhanden** aktiviert. Wenn keine vorhandenen Bilder ersetzt werden sollen, entfernen Sie das Häkchen aus dem Kontrollkästchen **Bilder ersetzen**. Wenn einzelne vorhandene Bilder nicht ersetzt werden sollen, löschen Sie die entsprechenden Zeilen.

3. Wählen Sie die Aktion **Bilder importieren** aus.

Das Feld **Importstatus** wird aktualisiert, um anzuzeigen, ob der Bildimport übersprungen oder abgeschlossen wurde.       

## Siehe auch
[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Erstellen von Nummernkreisen](ui-create-number-series.md)  
[Bestand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]