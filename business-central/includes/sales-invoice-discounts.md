---
author: edupont04
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ed62e60d3b5b1af2158d8adc6c411884ea4c12aa
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8133576"
---
Wenn alle Artikel in den Verkaufszeilen eingegeben wurden, kann der Rechnungsrabatt für den gesamten Verkaufsbeleg berechnet werden, indem Sie auf Aktionen und dann auf die Aktion **Rechnungsrabatt berechnen** klicken.

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
