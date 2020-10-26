---
title: Daten kopieren und einfügen
description: Kopieren Sie Felder und Zeilen von Business Central-Seiten und fügen Sie sie an anderer Stelle ein
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accessibility, shortcuts, keyboarding
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d53932be1597a96ced906ed7546ce8ff011639e3
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912621"
---
# <a name="copy-and-paste-faq"></a>Kopieren und einfügen FAQ
Sie können eine oder mehrere Zeilen (Datensätze) aus einer Liste oder einem einzelnen Feld auf einer Seite kopieren und die kopierten Daten dann auf der gleichen Seite, einer andere Seite oder einem externen Dokument (wie Microsoft Excel und Outlook-E-Mail) einfügen. Kurz gesagt, zum Kopieren drücken Sie STRG+C (cmd+C in Mac Os) auf Ihrer Tastatur. Zum Einfügen drücken Sie STRG+V (cmd+V in Mac Os).

Es gibt mehrere andere Tastenkombinationen zum Kopieren und Einfügen, mit denen Sie Zeit sparen, wenn Sie Daten eingeben. Weitere Informationen dazu finden Sie unter [Tastenkombinationen](keyboard-shortcuts.md#CopyRows).

In diesem Artikel finden Sie Antworten auf allgemeine Fragen, die Sie möglicherweise über das Kopieren und Einfügen haben.  

## <a name="what-can-i-copy-and-paste"></a>Was kann ich kopieren und einfügen?
- Kopieren Sie mindestens eine Zeile in [!INCLUDE[d365fin](includes/d365fin_md.md)] in die gleiche Liste oder in eine Liste mit identischen Spalten.
- Kopieren Sie mindestens eine Zeile in [!INCLUDE[d365fin](includes/d365fin_md.md)] und fügen Sie sie in Excel oder in anderen Programmen ein.
- Kopieren Sie mindestens eine Zeile in Excel und fügen Sie sie in eine [!INCLUDE[d365fin](includes/d365fin_md.md)]-Liste ein.
- Kopieren Sie den Wert eines individuellen Felds in [!INCLUDE[d365fin](includes/d365fin_md.md)] und fügen Sie ihn überall ein.

## <a name="does-copy-and-paste-work-with-tiles"></a>Funktioniert Kopieren und Einfügen bei Kacheln?
Ja, aber nur für eine einzelne ausgewählte Kachel.

## <a name="how-do-i-copy-a-row"></a>Wie kopiere ich eine Zeile?
Um eine einzelne Zeile zu kopieren, wählen Sie diese aus und drücken Sie STRG+C.

Wenn Sie weitere Zeilen kopieren möchten, können Sie Folgendes tun:
- Drücken Sie STRG und klicken Sie auf eine andere Zeile oder drücken Sie UMSCHALT und Klicken Sie, um die Zeile und alle dazwischen zu markieren. Weitere Informationen zu Maus- und Tastenkombinationen zur Auswahl von Zeilen finden Sie unter [Tastenkombinationen](keyboard-shortcuts.md#CopyRows).
- Wählen Sie ![Weitere Optionen anzeigen](media/show-more-options-icon.png "Symbol „Weitere Optionen anzeigen“") in der ersten Spalte einer Zeile, wählen Sie **Weitere auswählen** aus, aktivieren Sie das Kontrollkästchen neben jeder Zeile, die Sie kopieren möchten, und drücken dann STRG+C.

## <a name="how-do-i-paste-rows"></a>Wie füge ich Zeilen ein?
Wählen Sie eine leere Zeile mit Fokus in einer beliebigen Zelle aus und drücken Sie STRG+V.

Wenn Sie vorhandene Zeilen ersetzen möchten, wählen Sie die Zeilen aus und drücken dann STRG+V. In diesem Fall können Sie nur dieselbe Anzahl an Zeilen einfügen, die Sie ausgewählt haben.

> [!NOTE]
> Die Liste, in die Sie einfügen, muss bearbeitbar sein.

<!-- Rows are pasted directly where your cursor is located. If you paste into an empty line, any existing subsequent lines will be moved after the pasted lines. If you paste into an existing line or lines, this will be overwritten.-->

## <a name="can-i-paste-rows-into-an-outlook-email"></a>Kann ich Zeilen in eine Outlook-E-Mail einfügen?
Ja. Dies wird als eine formatierte Tabelle eingefügt, bei der die Einrückung, die numerische Ausrichtung und die Farben so erhalten bleiben, wie sie in [!INCLUDE[d365fin](includes/d365fin_md.md)] angezeigt werden würden.

## <a name="in-which-lists-can-i-copy-and-paste-rows"></a>In welche Listen kann ich Zeilen kopieren und einfügen?
Sie können Zeilen in jede Art von Liste kopieren, einschließlich Arbeitsblättern, Infoboxen oder Liste, die auf einer Seite eingebettet sind (z. B. Zeilen eines Verkaufsauftrags). Zum Einfügen müssen Zeilen jedoch editierbar sein.

Auf einigen Seiten kann der Anwendungsentwurf verhindern, dass Sie Zeilen einfügen. Wenden Sie sich an Ihren Administrator oder an den Anwendungsentwickler, um die [Eigenschaft "Editierbar"](/dynamics365/business-central/dev-itpro/developer/properties/devenv-editable-property) auf der Seite oder die [Eigenschaft "PasteIsValid"](/dynamics365/business-central/dev-itpro/developer/properties/devenv-pasteisvalid-property) in der Quelltabelle zu ändern.

## <a name="on-which-clients-is-copy-and-paste-available"></a>Auf welchen Clients ist das Kopieren und Einfügen verfügbar?
Kopieren und Einfügen sind im Browser oder der [!INCLUDE[d365fin](includes/d365fin_md.md)]-App für Windows 10 verfügbar.

## <a name="what-is-the-maximum-number-of-rows-that-can-be-copied"></a>Was ist die maximale Anzahl an Zeilen, die kopiert werden können?
Sie können so viele Zeilen kopieren, wie auf dem Bildschirm angezeigt werden. Wenn Sie beispielsweise alle 1000 Zeilen auf einer Seite kopieren möchten, müssen Sie zunächst zum unteren Rand scrollen und warten, bis die Zeilen angezeigt werden, bevor Sie diese kopieren. Die maximale Anzahl der Zeilen, die Sie kopieren können, ist nur durch den Speicherplatz Ihres Geräts begrenzt.

## <a name="must-i-have-the-exact-same-number-of-columns-when-pasting-rows"></a>Muss ich die exakte Anzahl an Spalten haben, wenn ich Zeilen einfüge?
Ja. Egal, ob Sie aus [!INCLUDE[d365fin](includes/d365fin_md.md)], aus Excel oder aus einer anderen Tabellenquelle kopieren, die Zeilen, die Sie in [!INCLUDE[d365fin](includes/d365fin_md.md)] einfügen, müssen genau die entsprechenden Spalten haben, nicht mehr, nicht weniger.

## <a name="why-do-i-get-errors-when-pasting-rows"></a>Warum erhalte ich Fehler, wenn ich Zeilen einfüge?
Beim Einfügen in [!INCLUDE[d365fin](includes/d365fin_md.md)] wird jede Zeile geprüft, um sicherzustellen, dass die Werte in jeder Spalte gültig sind. Wenn eine Spalte einen ungültigen Wert enthält, wird das Einfügen beendet, und eine Fehlermeldung wird angezeigt. Um dies zu verhindern, überprüfen Sie, dass die Spalten über gültige Werte verfügen, bevor Sie sie einfügen.


## <a name="see-also"></a>Siehe auch
[Assistive Funktionen](ui-accessibility.md)  
[Erste Schritte](product-get-started.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Häufig gestellte Fragen](across-faq.md)  
