---
title: Einrichten von unrealisierter Mehrwertsteuer
description: 'Wenn Sie Einnahmen- und Ausgabenrechnung verwenden, können Sie angeben, wie Sie unrealisierte MwSt. für Verkäufe und Einkäufe behandeln möchten.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'cash, VAT, unrealized, cash-based'
ms.search.form: '118, 472, 473'
ms.date: 04/01/2021
ms.author: bholtorf
---

# <a name="set-up-unrealized-vat-for-cash-based-accounting"></a><a name="set-up-unrealized-vat-for-cash-based-accounting"></a><a name="set-up-unrealized-vat-for-cash-based-accounting"></a>Einrichten unrealisierter MwSt. für Einnahmen- und Ausgabenrechnung

Wenn Sie Einnahmen- und Ausgabenrechnungs-Methoden ausgleichen, können Sie in [!INCLUDE[prod_short](includes/prod_short.md)] festlegen, wie unrealisierte MwSt. zu behandeln ist.

## <a name="to-use-general-ledger-accounts-for-unrealized-vat"></a><a name="to-use-general-ledger-accounts-for-unrealized-vat"></a><a name="to-use-general-ledger-accounts-for-unrealized-vat"></a>Verwenden von Sachkonten für unrealisierte MwSt.

Sie können festlegen, dass MwSt.-Beträge beim Buchen einer Rechnung berechnet und auf ein temporäres Sachkonto gebucht werden und dass die Beträge erst dann auf das korrekte Sachkonto gebucht und in die MwSt.-Abrechnungen einbezogen werden sollen, wenn die eigentliche Zahlung der Rechnung gebucht wird. Bevor Sie dies tun können, müssen Sie die [MwSt.-Buchungsmatrix](finance-setup-vat.md) ausfüllen.

Um die Konten für unrealisierte MwSt. zu verwenden, führen Sie diese Schritte aus:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, und geben Sie **Hauptbuchhaltung Einrichtung** ein.
2. Auf der Seite **Finanzbuchhaltung Einrichtung** wählen Sie das Kontrollkästchen **Unrealisierte MwSt.**.
3. Wählen Sie das Symbol **Seite oder Bericht suchen** ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?"), und geben Sie **MWR-Buchungseinrichtung** ein.
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

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Siehe auch
[Berechnungen einrichten und Buchungsmethoden für Mehrwertsteuer](finance-setup-vat.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
