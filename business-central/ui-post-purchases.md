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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 687a63e1d53db4c120070de0a353b3501a335d27
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914935"
---
# <a name="posting-purchases"></a>Einkäufe buchen
Bei einem Kaufbeleg können Sie zwischen den folgenden Buchungsaktionen wählen:

* **Veröffentlichen**
* **Buchungsvorschau**
* **Buchen und Drucken**
* **Testbericht**
* **Stapelbuchung**

Wenn ein Einkaufsbeleg gebucht wird, werden das Kreditorenkonto, das Hauptbuch, die Einträge im Artikel-Sachkonto und die Einträge im Ressourcen-Sachkonto aktualisiert.

Für jeden Einkaufsbeleg wird ein Einkaufseintrag in der Tabelle **Sachposten** angelegt. Darüber hinaus wird ein Posten in der Tabelle **Kreditorenposten** erzeugt und ein Sachposten im entsprechenden Einkaufskonto. Darüber hinaus kann die Buchung des Einkaufs zu einer Umsatzsteuerbuchung und einer Sachkontenbuchung für den Rabattbetrag führen. Ob ein Posten für Rabatt gebucht wird, hängt von den Einstellungen im Feld **Rabattbuchung** auf der Seite **Kreditoren & Einkauf Einrichtung** ab.

Für jede Einkaufszeile werden die folgenden Einträge erstellt:
- Ein Eintrag in der Tabelle **Buch.-Blatt-Position-Eingabe**, wenn die Einkaufszeile vom Typ **Position** ist.
- Ein Eintrag in der Tabelle **Buch.-Blatt-Eintrag**, wenn die Einkaufszeilen vom Typ **Buch.-Blatt-Konto** sind
- Ein Eintrag in der Tabelle **Ressourcen-Buch.-Blatt-Eingabe**, wenn die Einkaufszeile vom Typ **Ressourcen** ist.

Darüber hinaus werden Einkaufsbelege immer im Feld **Einkaufslieferkopf** und **Einkaufsrechnungskopf** Tabellen erfasst.

Bevor Sie buchen, können Sie einen Testbericht ausdrucken, der alle Daten der Einkaufsbestellung und etwaige Fehler enthält. Um den Bericht zu drucken, wählen Sie **Buchen** und wählen **Testbericht** aus.

> [!IMPORTANT]  
>   Wenn Sie eine Bestellung für Artikel buchen, können Sie sowohl einen Beleg als auch eine Rechnung erstellen. Dies kann gleichzeitig oder unabhängig voneinander durchgeführt werden. Sie können auch eine Teillieferung und eine Teilrechnung erzeugen, indem Sie die Felder **Menge zu liefern** und/oder **Zu fakturieren** in den jeweiligen Zeilen des Verkaufsauftrags ausfüllen, bevor Sie buchen. Beachten Sie, dass Sie keine Rechnung für Mengen erstellen können, die noch nicht geliefert wurden. Das bedeutet, dass Sie vor der Fakturierung einen Wareneingang gebucht haben müssen, oder Sie müssen "Liefern und Fakturieren" wählen.

Sie können entweder buchen oder buchen und drucken. Wenn Sie sich entscheiden, zu buchen und zu drucken, wird ein Bericht gedruckt, wenn der Auftrag gebucht wird. Sie können auch die Funktion **Stapelbuchen** wählen, mit der Sie mehrere Aufträge gleichzeitig buchen können. Weitere Informationen finden Sie unter [Mehrere Belege gleichzeitig buchen](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Anzeigen von Posten
Wenn die Buchung vollständig ist, werden die gebuchten Einkaufszeilen aus der Bestellung entfernt. Eine Meldung erscheint, die Ihnen mitteilt, dass die Buchung vollständig ist. Danach können Sie die gebuchten Buchungen auf den verschiedenen Seiten sehen, die gebuchte Buchungen enthalten, wie z.B. die Seiten **Kreditorenbuch-Einträge**, **Buch.-Blatt-Einträge**, **Buch.-Blatt-Buch-Einträge**, **Ressourcen-Buch.-Blatt-Einträge**, **Einkaufsbelege** und **Gebuchte Einkaufsrechnungen**.

In den meisten Fällen können Sie Posten von der betroffenen Karte oder dem betroffenen Beleg aus öffnen. Auf der Seite **Kreditorenkarte** wählen Sie beispielsweise die Aktion **Einträge** aus.

## <a name="editing-ledger-entries"></a>Bearbeiten von Posten
Sie können bestimmte Felder in gebuchten Einkaufsbelegen bearbeiten, z. B. das Feld **Zahlungsreferenz**. Weitere Informationen finden Sie unter [Gebuchte Belege bearbeiten](across-edit-posted-document.md). Bei kritischeren Feldern, die sich auf den Überwachungspfad auswirken, müssen Sie die Buchung stornieren oder rückgängig machen. Weitere Informationen finden Sie unter [Buchungen stornieren und Belege/Lieferungen rückgängig machen](finance-how-reverse-journal-posting.md).

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/receive-invoice-dynamics-d365-business-central/index)

## <a name="see-also"></a>Siehe auch
[Gebuchte Belege bearbeiten](across-edit-posted-document.md)  
[Mehrere Dokumente gleichzeitig buchen](ui-batch-posting.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Journale und Dokumente buchen](ui-post-documents-journals.md)  
[Ändern oder Löschen einer unbezahlten Einkaufsrechnung](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Suchen von Seiten und Informationen mit Wie möchten Sie weiter verfahren](ui-search.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
