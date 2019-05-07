---
title: Einrichten von unrealisierter Mehrwertsteuer | Microsoft Docs
description: Wenn Sie Einnahmen- und Ausgabenrechnung verwenden, können Sie angeben, wie Sie unrealisierte MwSt. für Verkäufe und Einkäufe behandeln möchten.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cash, VAT, unrealized, cash-based
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 69e4d4f4e924edd7eea45da73a3b0b5f71dd8cc0
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "928793"
---
# <a name="set-up-unrealized-vat-for-cash-based-accounting"></a>Einrichten unrealisierter MwSt. für Einnahmen- und Ausgabenrechnung
Wenn Sie Einnahmen- und Ausgabenrechnungs-Methoden ausgleichen, können Sie in [!INCLUDE[d365fin](includes/d365fin_md.md)] festlegen, wie unrealisierte MwSt. zu behandeln ist.

## <a name="to-use-general-ledger-accounts-for-unrealized-vat"></a>Verwenden von Sachkonten für unrealisierte MwSt.
Sie können festlegen, dass MwSt.-Beträge beim Buchen einer Rechnung berechnet und auf ein temporäres Sachkonto gebucht werden und dass die Beträge erst dann auf das korrekte Sachkonto gebucht und in die MwSt.-Abrechnungen einbezogen werden sollen, wenn die eigentliche Zahlung der Rechnung gebucht wird. Bevor Sie dies tun können, müssen Sie die MwSt.-Buchungsmatrix ausfüllen.

Um die Konten für unrealisierte MwSt. zu verwenden, führen Sie diese Schritte aus:
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Finanzbuchhaltung einrichten** ein, und wählen dann den zugehörigen Link aus.
2. Auf der Seite **Finanzbuchhaltung Einrichtung** wählen Sie das Kontrollkästchen **Unrealisierte MwSt.**.
3. Wählen Sie das Symbol **Nach Seite oder Bericht suchen** ![Glühlampe, mit der die Funktion "Wie möchten Sie weiter verfahren"](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") geöffnet wird und geben Sie **MwSt Buchung** einrichten ein.
4. Auf der Seite **MwSt.-Buchung einrichten** wählen Sie die MwSt.-Buchungsgruppe aus, und wählen Sie dann **Bearbeiten** aus.
5. Im Feld **Unrealisierte MwSt-Art** wählen Sie eine Option aus, um zu bestimmen, wie Zahlungen auf dem Rechnungsbetrag (ohne MwSt.) und den MwSt.-Betrag selbst aufgeteilt wird und wie MwSt.-Beträge vom Konto "Unreal. MwSt." auf das realisierte MwSt.-Konto gebucht werden. Die Optionen werden in der folgenden Tabelle beschrieben.

| Option | Beschreibung |
| --- | --- |
| Leer | Wählen Sie diese Option, wenn Sie die Funktion "Unrealisierte MwSt." nicht verwenden möchten. |
| Prozent | Zahlungen decken sowohl MwSt und den Rechnungsbetrag im Verhältnis zur prozentualen Zahlung des zu begleichenden Gesamtbetrags. Der gezahlte Steuerbetrag wird vom unrealisierten MwSt-Konto auf das realisierte MwSt-Konto gebucht. |
| Erster | Zahlungen decken zuerst die MwSt und dann den Rechnungsbetrag. In diesem Fall entspricht der vom Konto für die unrealisierte Mehrwertsteuer auf das Konto für die realisierte Mehrwertsteuer transferierte Betrag dem Zahlungsbetrag (bis die Mehrwertsteuer vollständig beglichen ist). |
| Letzter | Zahlungen decken zuerst den Rechnungsbetrag und dann die MwSt. In diesem Fall wird erst dann ein Betrag vom Konto für die unrealisierte Mehrwertsteuer auf das Konto für die realisierte Mehrwertsteuer transferiert, wenn der Zahlungsbetrag (ohne Mehrwertsteuer) vollständig beglichen ist. |
| Erste (ganz bezahlt) | Zahlungen decken zuerst die MwSt. (wie die _Erste_ Option), aber es werden erst dann Beträge auf das Steuerkonto transferiert, wenn die MwSt. vollständig gezahlt wurde. |
| Letzte (ganz bezahlt) | Zahlungen decken zuerst den Rechnungsbetrag (wie unter der Option _Letzte_), aber es werden erst dann Beträge auf das Steuerkonto transferiert, wenn die MwSt. vollständig beglichen wurde. |

6. Geben Sie im Feld **Unreal. Umsatzsteuerkonto** die entsprechende unrealisierte MwSt ein.

    > [!NOTE]  
    > Der MwSt-Betrag wird auf dieses Steuerkonto gebucht, wo er verbleibt, bis die Zahlung des Debitors gebucht wird. Der Betrag wird dann auf das Sachkonto für Umsatzsteuer transferiert.
7. Geben Sie im Feld **Unreal. Vorsteuerkonto** die entsprechende Sachkontonummer ein.

> [!NOTE]  
> Der MwSt-Betrag wird auf dieses Steuerkonto gebucht, wo er verbleibt, bis die Zahlung des Debitors gebucht wird. Der Betrag wird dann auf das Sachkonto für Mehrwertsteuerkäufe transferiert.

## <a name="see-also"></a>Siehe auch
[Mehrwertsteuer einrichten](finance-setup-vat.md)
