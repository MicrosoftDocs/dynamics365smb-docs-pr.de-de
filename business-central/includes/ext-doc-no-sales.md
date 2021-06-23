---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: 50b4b331f00bdcdf030bac2332ffb5dafdfd2de6
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115961"
---
Auf Verkaufsbelegen und Buch.-Blättern können Sie eine Belegnummer angeben, die auf das Nummerierungssystem des Debitors verweist. <!--You can enter a maximum of ten characters, both numbers and letters.--> Verwenden Sie dieses Feld, um die Nummer zu erfassen, die der Debitor der Bestellung, Rechnung oder Gutschrift zugewiesen hat. Sie können die Nummer dann später verwenden, wenn Sie aus irgendeinem Grund den gebuchten Posten anhand dieser Nummer suchen müssen.  

Das Feld **Ext. Belegnr. erforderlich** auf der Seite **Debitoren & Verkauf Einr.** gibt an, ob die Eingabe einer externen Belegnummer im Feld **Externe Belegnr.** in einem Verkaufskopf und das Feld **Externe Belegnr.** in einer Fibu Buch.-Blattzeile erforderlich ist.

Wenn Sie dieses Feld auswählen, ist es nicht möglich, eine Rechnung oder eine Fibu Buch.-Blattzeile ohne externe Belegnummer zu buchen.

Die externe Belegnummer ist in gebuchten Belegen enthalten, in denen Sie nach der entsprechenden Nummer suchen können. Sie können bei der Navigation zu Debitorenposten auch über die externe Belegnummer suchen.

Eine andere Möglichkeit, externe Belegnummern zu handhaben, ist die Verwendung des Feldes **Ihre Referenz**. Wenn Sie das Feld **Ihre Referenz** verwenden, wird die Nummer in gebuchte Belege aufgenommen und Sie können danach wie nach Werten aus den Feldern **Externe Belegnr.** suchen. Das Feld ist jedoch in Buchungsblattzeile nicht verfügbar.
