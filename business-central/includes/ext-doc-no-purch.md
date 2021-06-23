---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: 59376b96dcd6f755040b07784ceca53e157bcf14
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115958"
---
Auf Einkaufsbelegen und Buch.-Blättern können Sie eine Belegnummer angeben, die auf das Nummerierungssystem des Kreditors verweist. Verwenden Sie dieses Feld, um die Nummer zu erfassen, die der Kreditor der Bestellung, Rechnung oder Gutschrift zugewiesen hat. Sie können die Nummer dann später verwenden, wenn Sie aus irgendeinem Grund den gebuchten Posten anhand dieser Nummer suchen müssen.

Das Feld **Ext. Belegnr. erforderlich** auf der Seite **Kreditoren & Einkauf Einr.** gibt an, ob in folgenden Situationen die Eingabe einer externen Belegnummer obligatorisch ist:

* Im Feld **Kred.-Rechnungsnr.**, im Feld **Lieferanten-Bestell-Nr.** oder im Feld **Kred.-Gutschriftsnr.** in einem Einkaufskopf.

* Im Feld **Externe Belegnummer** in der Buch.-Blattzeile, wenn das Feld **Belegart** auf *Rechnung*, *Gutschrift* oder *Zinsrechnung* und das Feld **Kontoart** auf *Kreditor* festgelegt ist.

Wenn Sie dieses Feld aktivieren, ist es nicht möglich, eine Rechnung, Gutschrift oder Buch.-Blattzeile ohne die Angabe einer externen Belegnummer zu buchen.

Die externe Belegnummer ist in gebuchten Belegen enthalten, in denen Sie nach der entsprechenden Nummer suchen können. Sie können bei der Navigation zu Kreditorenposten auch über die externe Belegnummer suchen.

Eine andere Möglichkeit, externe Belegnummern zu handhaben, ist die Verwendung des Feldes **Ihre Referenz**. Wenn Sie das Feld **Ihre Referenz** verwenden, wird die Nummer in gebuchte Belege aufgenommen und Sie können danach wie nach Werten aus den Feldern **Externe Belegnr.** suchen. Das Feld ist jedoch in Buchungsblattzeile nicht verfügbar.
