---
title: Verstehen, wie Einkaufsbelege gebucht werden | Microsoft Docs
description: Mehr zu den unterschiedlichen Buchungsfunktionen erfahren, um Einkaufsbelege zu buchen.
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/12/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 06c22658518d504c80a5a379d579cf7f7e8a0757
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="posting-purchases"></a>Einkäufe buchen
Wenn Sie die Schaltfläche **Gruppe Buchen** in einem Einkaufsbeleg auswählen, können Sie zwischen den folgenden Buchungsfunktionen auswählen:

* **Veröffentlichen**
* **Buchungsvorschau**
* **Buchen und Drucken**
* **Testbericht**
* **Stapelbuchung**

Wenn Sie die Zeilen der Einkaufsbestellung ausgefüllt haben, können Sie sie buchen, d. h., eine Lieferung und eine Rechnung erzeugen.

Wenn eine Einkaufsbestellung gebucht wird, wird das Kreditorenkonto, die Finanzbuchhaltung und die Artikelposten aktualisiert.

Für jede Einkaufsbestellung wird ein Einkaufsposten in der Tabelle **Sachposten** erstellt. Darüber hinaus wird ein Posten in der Tabelle **Kreditorenposten** erzeugt und ein Sachposten im entsprechenden Einkaufskonto. Zusätzlich kann das Buchen in einem MwSt.-Posten und einem Sachposten für den Rabattbetrag resultieren. Ob ein Posten für Rabatt gebucht wird, hängt von den Einstellungen im Feld **Rabattbuchung** im Fenster **Kreditoren & Einkauf einrichten** ab.

Für jede Einkaufsbestellungszeile wird ein Artikelposten in der Tabelle **Artikelposten** erstellt (wenn die Einkaufszeilen Artikelnummern enthalten) oder es wird ein Sachposten in der Tabelle **Sachposten** erstellt (wenn die Einkaufszeilen eine Sachkontonummer enthalten). Zusätzlich werden Einkaufsbestellungen immer in den Tabellen **Einkaufslieferkopf** und **Einkaufsrechnungskopf** erfasst.

Bevor Sie buchen, können Sie einen Testbericht ausdrucken, der alle Daten der Einkaufsbestellung und etwaige Fehler enthält. Um den Bericht zu drucken, wählen Sie **Buchen** und wählen **Testbericht** aus.

> [!IMPORTANT]  
>   Wenn Sie eine Bestellung buchen, können Sie sowohl eine Lieferung als auch eine Rechnung erstellen. Dies kann gleichzeitig oder unabhängig voneinander durchgeführt werden. Sie können auch eine Teillieferung und eine Teilrechnung erzeugen, indem Sie die Felder **Menge zu liefern** und/oder **Zu fakturieren** in den jeweiligen Zeilen des Verkaufsauftrags ausfüllen, bevor Sie buchen. Beachten Sie, dass Sie keine Rechnung für Mengen erstellen können, die noch nicht geliefert wurden. Das bedeutet, dass Sie vor der Fakturierung einen Wareneingang gebucht haben müssen, oder Sie müssen "Liefern und Fakturieren" wählen.

Sie können entweder buchen oder buchen und drucken. Wenn Sie sich entscheiden, zu buchen und zu drucken, wird ein Bericht gedruckt, wenn der Auftrag gebucht wird. Sie können auch die Funktion **Stapelbuchen** wählen, mit der Sie mehrere Aufträge gleichzeitig buchen können.

Wenn die Buchung vollständig ist, werden die gebuchten Einkaufszeilen aus der Bestellung entfernt. Eine Meldung erscheint, die Ihnen mitteilt, dass die Buchung vollständig ist. Im Anschluss können Sie die gebuchten Posten in den verschiedenen Fenstern einsehen, die gebuchte Posten enthalten (**Kreditorenposten**, **Sachposten**, **Artikelposten**, **Lagerplatzposten**, **Einkaufsrechnung**).

## <a name="see-also"></a>Siehe auch
[Einkauf](purchasing-manage-purchasing.md)  
[Journale und Dokumente buchen](ui-post-documents-journals.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


