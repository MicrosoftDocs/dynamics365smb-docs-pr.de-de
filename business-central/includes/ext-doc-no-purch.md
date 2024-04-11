---
author: brentholtorf
ms.topic: include
ms.date: 03/20/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

Auf Einkaufsbelegen und Buch.-Blättern können Sie eine Belegnummer angeben, die auf das Nummerierungssystem des Kreditors verweist. Verwenden Sie dieses Feld, um die Nummer zu erfassen, die der Kreditor der Bestellung, Rechnung oder Gutschrift zugewiesen hat. Sie können die Nummer dann später verwenden, wenn Sie aus irgendeinem Grund den gebuchten Posten anhand dieser Nummer suchen müssen.

Das Feld **Ext. Belegnr. erforderlich** auf der Seite **Kreditoren & Einkauf Einr.** gibt an, ob in folgenden Situationen die Eingabe einer externen Belegnummer obligatorisch ist:

* Im Feld **Kred.-Rechnungsnr.**, im Feld **Lieferanten-Bestell-Nr.** oder im Feld **Kred.-Gutschriftsnr.** in einem Einkaufskopf.

* Im Feld **Externe Belegnummer** in der Buch.-Blattzeile, wenn das Feld **Belegart** auf *Rechnung*, *Gutschrift* oder *Zinsrechnung* und das Feld **Kontoart** auf *Kreditor* festgelegt ist.

Wenn Sie dieses Feld aktivieren, ist es nicht möglich, eine Rechnung, Gutschrift oder Buch.-Blattzeile ohne die Angabe einer externen Belegnummer zu buchen.

Die externe Belegnummer ist in gebuchten Belegen enthalten, in denen Sie nach der entsprechenden Nummer suchen können. Sie können bei der Navigation zu Kreditorenposten auch über die externe Belegnummer suchen.

Eine andere Möglichkeit, externe Belegnummern zu handhaben, ist die Verwendung des Feldes **Ihre Referenz**. Wenn Sie das Feld **Ihre Referenz** verwenden, wird die Nummer in gebuchte Belege aufgenommen und Sie können danach wie nach Werten aus den Feldern **Externe Belegnr.** suchen. Das Feld ist jedoch in Buchungsblattzeilen nicht verfügbar.
