---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/25/2021
ms.author: edupont
ms.openlocfilehash: 539ee2eb2c9e4a71eacfb78d95320870128fb1d9
ms.sourcegitcommit: cb06aa973f5c767df774b0e1e199c6fbe0e85b88
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470287"
---
Wenn alle Artikel in den Verkaufszeilen eingegeben wurden, kann der Rechnungsrabatt für den gesamten Beleg berechnet werden, indem Sie auf Aktionen und dann auf die Aktion **Rechnungsrabatt berechnen** klicken.

Der Rabatt wird basierend auf allen Zeilen des Verkaufsbelegs berechnet, jedoch nur für Artikel, bei denen das Feld **Rech.-Rabatt zulassen** in der Verkaufsauftragszeile die Option **Ja** enthält. Dies ist die Standardeinstellung für Artikel. Beispielsweise werden Zeilen mit Artikelgebühren nicht in die Berechnung des Rechnungsrabattes einbezogen. Wenn Sie einen Rabatt auf solche Zeilen gewähren möchten, müssen Sie das Feld **Zeilenrabatt %** in den entsprechenden Zeilen festlegen.  

> [!TIP]
> Wenn das Feld **Rechnungsrabatt berechnen** auf der Seite **Verkäufe und Debitoren einrichten** ausgewählt wird, dann wird der Rechnungsrabatt automatisch berechnet, wenn Sie eine der folgenden Aktionen auf einem Verkaufsbeleg ausführen:
>
> * Statistik anzeigen
> * Anzeigen eines Testberichts
> * Drucken
> * Buchung

Zum Berechnen des Rechnungsrabatts für einen Debitor werden auf der Seite **Debitorenrechnungsrabatt** für den Debitor definiert. Anhand des Währungscodes im Verkaufsbeleg werden die Rechnungsrabattbedingungen der entsprechenden Währung ermittelt.

Wenn keine Rechnungsrabatte für Fremdwährungen definiert wurden, verwendet die Anwendung die Rechnungsrabattbedingungen in Mandantenwährung, die in der Tabelle **Debitorenrechnungsrabatt** festgelegt wurden und den Wechselkurs zum Buchungsdatum des Verkaufsbelegs, um den Rechnungsrabatt in der Fremdwährung zu berechnen.
