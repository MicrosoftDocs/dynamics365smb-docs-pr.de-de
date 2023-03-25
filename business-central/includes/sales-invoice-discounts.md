---
author: brentholtorf
ms.topic: include
ms.date: 10/05/2022
ms.author: bholtorf
---
Nachdem Sie alle Artikel in den Verkaufszeilen hinzugefügt haben, kann der Rechnungsrabatt für den gesamten Verkaufsbeleg berechnet werden, indem Sie auf Aktionen und dann auf die Aktion **Rechnungsrabatt berechnen** klicken.

Der Rabatt wird auf der Grundlage aller Zeilen auf dem Verkaufsbeleg berechnet, in denen **Rechnungsdatenträger zulassen** ausgewählt ist. Standardmäßig sind Rechnungsrabatte erlaubt. Jedoch werden Zeilen mit Artikelgebühren nicht in die Berechnung des Rechnungsrabattes einbezogen. Um einen Rabatt auf solche Zeilen zu gewähren, müssen Sie einen Wert im Feld **Zeilenrabatt %** in den Zeilen eingeben.  

> [!NOTE]
> Standardmäßig sind die Felder **Rech.-Rabatt zulassen** und**Zeilenrabattbetrag** für die Zeilen ausgeblendet. Wenn die Felder nicht verfügbar sind, können Sie sie hinzufügen, indem Sie die Seite personalisieren. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](../ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

> [!TIP]
> Wenn das Feld **Rechnungsrab. berechnen** auf der Seite **Debitoren und Verkauf Einr.** aktiviert ist, wird der Rechnungsrabatt automatisch berechnet. Wann die Berechnung erfolgt, hängt von der Art des verwendeten Verkaufsbelegs ab.
>
> Wenn Sie einen Verkaufsauftrag verwenden, wird der Rabatt berechnet, wenn Sie eine Position hinzufügen. Für alle anderen Verkaufsbelege, z. B. Verkaufsrechnungen, wird der Rabatt berechnet, wenn Sie eine der folgenden Aktionen ausführen:
>
> * Statistik anzeigen
> * Anzeigen eines Testberichts
> * Drucken
> * Postverkehr

Sie definieren die Rechnungsrabattbedingungen für einen Debitor auf der Seite **Debitorenrechnungsrabatt**. Anhand des Währungscodes im Verkaufsbeleg werden die Rechnungsrabattbedingungen der entsprechenden Währung ermittelt.

Wenn Sie keine Rechnungsrabatte für Fremdwährungen definiert haben, gelten die Rabattbedingungen auf der Seite **Debitorenrechnungsrabattei**, um den Rabatt zu berechnen. Für die Berechnung wird Ihre Hauswährung und der am Buchungsdatum des Belegs gültige Wechselkurs verwendet.
