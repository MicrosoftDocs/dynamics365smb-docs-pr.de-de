---
title: Kaufbelege buchen
description: Lernen Sie die verschiedenen Buchungsfunktionen für Belege kennen, mit denen Sie Kaufbelege buchen können, und erfahren Sie, wie Sie gebuchte Belege aktualisieren können.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.form: ''
ms.date: 08/08/2022
ms.author: edupont
ms.openlocfilehash: 2f306fee236fda2bae4863e0e793239c2168f125
ms.sourcegitcommit: 8b95e1700a9d1e5be16cbfe94fdf7b660f1cd5d7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2022
ms.locfileid: "9461102"
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

Für jede Einkaufszeile werden, falls anwendbar. die folgenden Einträge erstellt:

* in der Tabelle **Buch.-Blatt-Position-Eingabe**, wenn die Einkaufszeile vom Typ **Artikel** ist.
* in der Tabelle **Buch.-Blatt-Eintrag**, wenn die Einkaufszeilen vom Typ **Buch.-Blatt-Konto** sind
* in der Tabelle **Ressourcen-Buch.-Blatt-Eingabe**, wenn die Einkaufszeile vom Typ **Ressourcen** ist.

Darüber hinaus werden Einkaufsbelege immer im Feld **Einkaufslieferkopf** und **Einkaufsrechnungskopf** Tabellen erfasst.

Bevor Sie buchen, können Sie einen Testbericht ausdrucken, der alle Daten der Einkaufsbestellung und etwaige Fehler enthält. Um den Bericht zu drucken, wählen Sie **Buchen** und wählen **Testbericht** aus.

> [!IMPORTANT]  
> Wenn Sie eine Bestellung für Artikel buchen, können Sie sowohl einen Beleg als auch eine Rechnung erstellen. Dies kann gleichzeitig oder unabhängig voneinander durchgeführt werden. Sie können auch eine Teillieferung und eine Teilrechnung erzeugen, indem Sie die Felder **Menge zu liefern** und/oder **Zu fakturieren** in den jeweiligen Zeilen des Verkaufsauftrags ausfüllen, bevor Sie buchen. Beachten Sie, dass Sie keine Einkaufsrechnung aus einer Bestellung für Produkte oder Dienstleistungen erstellen können, die nicht erhalten wurden. Das bedeutet, dass Sie vor der Fakturierung einen Wareneingang gebucht haben müssen, oder Sie müssen "Liefern und Fakturieren" wählen.
>
> Zum Buchen einer Einkaufsrechnung, ohne einen Kaufbeleg in [!INCLUDE[prod_short](includes/prod_short.md)]zu erfassen, erstellen Sie das Dokument auf der Seite **Einkaufsrechnungen**. Erfahren Sie mehr unter [Einkäufe mit Einkaufsrechnungen erfassen](purchasing-how-record-purchases.md).

Sie können entweder buchen oder buchen und drucken. Wenn Sie sich entscheiden, zu buchen und zu drucken, wird ein Bericht gedruckt, wenn der Auftrag gebucht wird. Sie können auch **Stapelbuchen** wählen, mit der Sie mehrere Aufträge gleichzeitig buchen können. Erfahren Sie mehr unter [Mehrere Dokumente gleichzeitig buchen](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Anzeigen von Posten

Wenn die Buchung vollständig ist, werden die gebuchten Einkaufszeilen aus der Bestellung entfernt. Eine Meldung erscheint, die Ihnen mitteilt, dass die Buchung vollständig ist. Danach können Sie die gebuchten Buchungen auf den verschiedenen Seiten sehen, die gebuchte Buchungen enthalten, wie z.B. die Seiten **Kreditorenbuch-Einträge**, **Buch.-Blatt-Einträge**, **Buch.-Blatt-Buch-Einträge**, **Ressourcen-Buch.-Blatt-Einträge**, **Einkaufsbelege** und **Gebuchte Einkaufsrechnungen**.

In den meisten Fällen können Sie Posten von der betroffenen Karte oder dem betroffenen Beleg aus öffnen. Auf der Seite **Kreditorenkarte** wählen Sie beispielsweise die Aktion **Einträge** aus.

## <a name="editing-ledger-entries"></a>Bearbeiten von Posten

Sie können bestimmte Felder in gebuchten Einkaufsbelegen bearbeiten, z. B. das Feld **Zahlungsreferenz**. Erfahren Sie mehr unter [Gebuchte Belege bearbeiten](across-edit-posted-document.md). Bei kritischeren Feldern, die sich auf den Überwachungspfad auswirken, müssen Sie die Buchung stornieren oder rückgängig machen. Erfahren Sie mehr unter [Buch.-Blatt-Buchungen stornieren und Rückgängigmachung von Eingängen/Versendungen](finance-how-reverse-journal-posting.md).

## <a name="see-related-training-at-microsoft-learn"></a>Siehe verwandte Schulungen unter [Microsoft Learn](/learn/modules/receive-invoice-dynamics-d365-business-central/index).

## <a name="see-also"></a>Siehe auch

[Gebuchte Belege bearbeiten](across-edit-posted-document.md)  
[Mehrere Dokumente gleichzeitig buchen](ui-batch-posting.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Journale und Dokumente buchen](ui-post-documents-journals.md)  
[Ändern oder Löschen einer unbezahlten Einkaufsrechnung](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Suche nach Seiten und Informationen mit „Sie wünschen...“](ui-search.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
