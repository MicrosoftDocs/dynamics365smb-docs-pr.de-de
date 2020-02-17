---
title: Verstehen, wie Einkaufsbelege gebucht werden | Microsoft Docs
description: Erfahren Sie mehr über die verschiedenen Buchungsfunktionen zum Buchen von Einkaufsbelegen und wie Sie gebuchte Belege aktualisieren können.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 01/17/2020
ms.author: sgroespe
ms.openlocfilehash: 2565133adfab4fb5f6febeeccb69c4f3d6f59e71
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2020
ms.locfileid: "2991880"
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

Für jede Einkaufsbestellung wird ein Einkaufsposten in der Tabelle **Sachposten** erstellt. Darüber hinaus wird ein Posten in der Tabelle **Kreditorenposten** erzeugt und ein Sachposten im entsprechenden Einkaufskonto. Zusätzlich kann das Buchen in einem MwSt.-Posten und einem Sachposten für den Rabattbetrag resultieren. Ob ein Posten für Rabatt gebucht wird, hängt von den Einstellungen im Feld **Rabattbuchung** auf der Seite **Kreditoren & Einkauf Einrichtung** ab.

Für jede Einkaufsbestellungszeile wird ein Artikelposten in der Tabelle **Artikelposten** erstellt (wenn die Einkaufszeilen Artikelnummern enthalten) oder es wird ein Sachposten in der Tabelle **Sachposten** erstellt (wenn die Einkaufszeilen eine Sachkontonummer enthalten). Zusätzlich werden Einkaufsbestellungen immer in den Tabellen **Einkaufslieferkopf** und **Einkaufsrechnungskopf** erfasst.

Bevor Sie buchen, können Sie einen Testbericht ausdrucken, der alle Daten der Einkaufsbestellung und etwaige Fehler enthält. Um den Bericht zu drucken, wählen Sie **Buchen** und wählen **Testbericht** aus.

> [!IMPORTANT]  
>   Wenn Sie eine Bestellung buchen, können Sie sowohl eine Lieferung als auch eine Rechnung erstellen. Dies kann gleichzeitig oder unabhängig voneinander durchgeführt werden. Sie können auch eine Teillieferung und eine Teilrechnung erzeugen, indem Sie die Felder **Menge zu liefern** und/oder **Zu fakturieren** in den jeweiligen Zeilen des Verkaufsauftrags ausfüllen, bevor Sie buchen. Beachten Sie, dass Sie keine Rechnung für Mengen erstellen können, die noch nicht geliefert wurden. Das bedeutet, dass Sie vor der Fakturierung einen Wareneingang gebucht haben müssen, oder Sie müssen "Liefern und Fakturieren" wählen.

Sie können entweder buchen oder buchen und drucken. Wenn Sie sich entscheiden, zu buchen und zu drucken, wird ein Bericht gedruckt, wenn der Auftrag gebucht wird. Sie können auch die Funktion **Stapelbuchen** wählen, mit der Sie mehrere Aufträge gleichzeitig buchen können. Weitere Informationen finden Sie unter [Mehrere Dokumente gleichzeitig bereitstellen](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Anzeigen von Posten
Wenn die Buchung vollständig ist, werden die gebuchten Einkaufszeilen aus der Bestellung entfernt. Eine Meldung erscheint, die Ihnen mitteilt, dass die Buchung vollständig ist. Im Anschluss können Sie die gebuchten Posten auf den verschiedenen Seiten einsehen, die gebuchte Posten enthalten **Kreditorenposten**, **Sachposten**, **Artikelposten**, **Lagerplatzposten**, **Einkaufsrechnung**.

In den meisten Fällen können Sie Posten von der betroffenen Karte oder dem betroffenen Beleg aus öffnen. Auf der Seite **Kreditorenkarte** wählen Sie beispielsweise die Aktion **Einträge** aus.

## <a name="editing-ledger-entries"></a>Bearbeiten von Posten
Sie können bestimmte Felder in gebuchten Einkaufsbelegen bearbeiten, z. B. das Feld **Zahlungsreferenz**. Weitere Informationen finden Sie unter [Gebuchte Belege bearbeiten](across-edit-posted-document.md). Bei kritischeren Feldern, die sich auf den Überwachungspfad auswirken, müssen Sie die Buchung stornieren oder rückgängig machen. Weitere Informationen finden Sie unter [Buchungen stornieren und Belege/Lieferungen rückgängig machen](finance-how-reverse-journal-posting.md). 

## <a name="see-related-training-at-microsoft-learnlearnmodulesreceive-invoice-dynamics-d365-business-centralindex"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/receive-invoice-dynamics-d365-business-central/index)

## <a name="see-also"></a>Siehe auch
[Gebuchte Belege bearbeiten](across-edit-posted-document.md)  
[Mehrere Dokumente gleichzeitig buchen](ui-batch-posting.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Journale und Dokumente buchen](ui-post-documents-journals.md)  
[Ändern oder Löschen einer unbezahlten Einkaufsrechnung](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Suchen von Seiten und Informationen mit Wie möchten Sie weiter verfahren](ui-search.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
