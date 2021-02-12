---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/20/2021
ms.author: edupont
ms.openlocfilehash: 718845561c1a18701d20b93ebdc8339308ce7ac8
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035785"
---
Wenn alle Artikel in den Verkaufsauftragszeilen eingegeben wurden, kann der Rechnungsrabatt für den gesamten Verkaufsbeleg berechnet werden, indem Sie auf Aktionen und dann auf die Aktion **Rechnungsrabatt berechnen** klicken.

Wenn das Feld **Rechnungsrabatt berechnen** im Fenster **Verkäufe und Debitoren einrichten** ausgewählt wird, dann wird der Rechnungsrabatt automatisch berechnet, wenn Sie eine der folgenden Aktionen auf einem Verkaufsbeleg ausführen:

* Statistik anzeigen
* Anzeigen eines Testberichts
* Drucken
* Buchung

Der Rabatt wird über alle Zeilen des Verkaufsbelegs verteilt, jedoch nur für Artikel, bei denen das Feld **Rech.-Rabatt zulassen** in der Verkaufsauftragszeile die Option **Ja** enthält. Dies ist die Standardeinstellung für Artikel.

Zum Berechnen des Rechnungsrabatts werden die auf der Seite **Debitorenrechnungsrabatt** berechneten Rechnungsrabatte definiert. Anhand des Währungscodes im Verkaufsbeleg werden die Rechnungsrabattbedingungen der entsprechenden Währung ermittelt.

Wenn keine Rechnungsrabatte für Fremdwährungen definiert wurden, verwendet die Anwendung die Rechnungsrabattbedingungen in Mandantenwährung, die in der Tabelle **Debitorenrechnungsrabatt** festgelegt wurden und den Wechselkurs zum Buchungsdatum des Verkaufsbelegs, um den Rechnungsrabatt in der Fremdwährung zu berechnen.
