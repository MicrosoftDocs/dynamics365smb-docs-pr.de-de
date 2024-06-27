---
title: Festlegen des Berichtslayouts
description: 'Erfahren Sie, wie Sie das Layout festlegen, das beim Anzeigen und Drucken eines Berichts verwendet wird.'
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9652, 9650'
ms.date: 06/13/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# Die von einem Bericht verwendeten Layouts festlegen

> **GILT FÜR:** Business Central Online, Business Central lokal 2022 Veröffentlichungzyklus 1 und höher. Informationen zu früheren Versionen finden Sie [hier](ui-how-change-layout-currently-used-report.md).

Ein Berichtslayout bestimmt das Aussehen eines Berichts. Es steuert, welche Datenfelder eines Berichtsdatensatzes angezeigt werden, wie sie angeordnet, formatiert sind und mehr. Ein Bericht kann mehr als ein Layout haben, die bei Bedarf ausgewechselt werden können.

Wenn die Anwendung mehrere Unternehmen enthält, werden die Layouts pro Unternehmen festgelegt. Derselbe Bericht in einem Unternehmen kann also in einem anderen Unternehmen ein anderes Layout haben.

## Erste Schritte

Es gibt einige Möglichkeiten festzulegen, welches Layout ein Bericht verwendet. Jeder Weg hat Vorteile, je nachdem, was Sie tun möchten: 

- Von der Berichtsanforderungsseite

  Beim Einrichten eines auszuführenden Berichts enthält die Berichtsanforderungsseite das Feld **Berichtslayout**, das das aktuelle Standardlayout anzeigt, das vom Bericht verwendet wird. Sie können dieses Feld verwenden, um vorübergehend zu einem anderen verfügbaren Layout des von Ihnen ausgeführten Berichts zu wechseln. Nachdem Sie den Bericht ausgeführt haben, wird das Layout wieder auf das Standardlayout zurückgesetzt. Weitere Informationen finden Sie unter [Berichte ausführen und drucken](ui-work-report.md#switch-the-report-layout).

- Von der Seite **Berichtslayout-Auswahl**

  Die Seite **Auswahl des Berichtslayouts** zeigt eine Liste aller Berichte an. Diese Seite zeigt das aktuelle Standardlayout für einen Bericht an. Damit können Sie Layouts in verschiedenen Unternehmen festlegen, ohne das Unternehmen wechseln zu müssen, mit dem Sie arbeiten.

- Die **Berichtslayout**-Seite zeigt alle verfügbaren **Berichtslayouts** für jeden Bericht im aktuellen Unternehmen an. Es wird auch verwendet, um das Standardlayout für Berichte anzugeben. Es ist einfach, ein bestimmtes Layout zu finden, indem Sie die Liste sortieren oder filtern. Sobald Sie das Layout gefunden haben, können Sie es mit einer einzigen Auswahl für einen Bericht festlegen.

  > [!NOTE]
  > Sie können die Seite **Berichtslayouts** nicht für Word- und RDLC-Layouts verwenden, die mit der der **Benutzerdefinierte Layouts**-Funktion einer Vorgängerversion erstellt wurden. Tatsächlich werden diese benutzerdefinierten Layouts nicht einmal auf der Seite **Berichtslayouts** aufgelistet. Sie können diese Layouts nur über die **Auswahl des Berichtslayouts**-Seite festlegen.

## Das Layout aus der Berichtslayouts-Seite festlegen

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Suchen Sie das Layout in der Liste, wählen Sie es aus, und wählen Sie dann die **Standard festlegen**-Aktion oben auf der Seite aus.

## Das Layout aus der Auswahl des Berichtslayouts-Seite festlegen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?"). Symbol. Geben Sie **Auswahl des Berichtslayouts** ein und wählen Sie dann den entsprechenden Link.
  
   Auf der Seite sind alle Berichte aufgelistet, die für das Unternehmen verfügbar sind, das im Feld **Unternehmen** oben auf der Seite verfügbar ist. Das Feld **Layoutbeschreibung** gibt das Layout an, das in dem Bericht aktuell verwendet wird.
2. Legen Sie das Feld **Unternehmen** oben auf das Unternehmen fest, das den Bericht umfasst.
3. Suchen Sie den Bericht in der Liste und wählen Sie ihn aus. Führen Sie dann einen der folgenden Schritte aus:

   - Wenn das Layout, zu dem Sie wechseln möchten, ein anderer Typ als das aktuelle Layout ist, wählen Sie das **Layouttyp**-Feld und dann den Typ des Layouts aus, den Sie für den Bericht festlegen möchten. 
   - Wenn das Layout, zu dem Sie wechseln möchten, den gleichen Typ wie das aktuelle Layout hat, wählen Sie die **Layout auswählen**-Aktion ganz oben.

4. Auf der **Berichtslayouts**-Seite wählen Sie das Layout und dann **OK** aus.

## Das ursprüngliche Standardlayout wiederherstellen

Berichte sind so konzipiert, dass sie standardmäßig ein Layout verwenden. Sie können auf der **Auswahl des Berichtslayouts**-Seite wieder zum ursprünglichen Standardlayout wechseln. Wählen Sie einfach den Bericht und dann die **Standardauswahl wiederherstellen**-Aktion oben auf der Seite aus.

## Siehe auch

[Verwalten von Berichtslayouts](ui-manage-report-layouts.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
