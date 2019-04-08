---
title: Verstehen, wie Verkaufsbelege gebucht werden | Microsoft Docs
description: Mehr zu den unterschiedlichen Buchungsfunktionen erfahren, um Verkaufsbelege zu buchen.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: solsen
ms.openlocfilehash: 7ada688f7946d7f857dc6d4a6518b8bcb4e5c707
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "798525"
---
# <a name="posting-sales"></a>Verkäufe buchen
Wenn Sie die Schaltfläche **Gruppe Buchen** in einem Verkaufsbeleg auswählen, können Sie zwischen den folgenden Buchungsfunktionen auswählen:

* **Veröffentlichen**
* **Testbericht**
* **Buchen und senden**
* **Buchen und Drucken**
* **Buchen und per E-Mail senden**
* **Stapelbuchung**
* **Buchungsvorschau**

Wenn Sie alle Zeilen ausgefüllt und alle Daten des Verkaufsauftrags eingegeben haben, können Sie ihn buchen. Dies erstellt eine Lieferung und eine Rechnung.

Wenn eine Verkaufsbestellung gebucht wird, wird das Debitorenkonto, die Finanzbuchhaltung und die Artikelposten aktualisiert.

Für jeden Verkaufsauftrag wird ein Verkaufsposten in der Tabelle **Sachposten** erstellt. Darüber hinaus wird ein Posten in der Tabelle **Kreditorenposten** erzeugt und ein Sachposten im entsprechenden Einkaufskonto. Zusätzlich kann das Buchen in einem MwSt.-Posten und einem Sachposten für den Rabattbetrag resultieren. Ob ein Posten für Rabatt gebucht wird, hängt von den Einstellungen im Feld **Rabattbuchung** auf der Seite **Debitoren & Verkauf Einr.** ab.

Für jede Zeile des Verkaufsauftrags wird ein Artikelposten in der Tabelle **Artikelposten** erzeugt (wenn die Verkaufszeilen Artikelnummern enthalten) oder es wird ein Sachposten in der Tabelle **Sachposten** erzeugt (wenn die Verkaufszeilen Sachkonten enthalten). Zusätzlich dazu werden Verkaufsaufträge immer in den Tabellen **Verkaufslieferkopf** und **Verkaufsrechnungskopf** gespeichert.

> [!IMPORTANT]  
>   Wenn Sie einen Auftrag buchen, können Sie sowohl einen Lieferschein als auch eine Rechnung erzeugen. Dies kann gleichzeitig oder unabhängig voneinander getan werden. Sie können auch eine Teillieferung und eine Teilrechnung erzeugen, indem Sie die Felder **Menge zu liefern** und/oder **Menge zu fakturieren** in den jeweiligen Zeilen des Verkaufsauftrags ausfüllen, bevor Sie buchen. Beachten Sie, dass Sie keine Rechnung ausstellen können, solange die entsprechende Lieferung nicht erfolgt ist. Bevor Sie also die Fakturierung durchführen können, müssen Sie einen Lieferschein erstellt oder die Funktion zur gleichzeitigen Lieferung und Fakturierung gewählt haben.

Wenn die Buchung vollständig ist, werden die gebuchten Verkaufszeilen aus der Bestellung entfernt. Eine Meldung erscheint, die Ihnen mitteilt, dass die Buchung vollständig ist. Im Anschluss können Sie die gebuchten Posten auf den verschiedenen Seiten einsehen, die gebuchte Posten enthalten, einschließlich **Debitorenposten**, **Sachposten**, **Artikelposten**, **Lagerplatzposten**, **Geb. Verkaufsrechnung**.

## <a name="see-also"></a>Siehe auch
[Verkauf](sales-manage-sales.md)  
[Senden von Belegen über E-Mail](ui-how-send-documents-email.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

