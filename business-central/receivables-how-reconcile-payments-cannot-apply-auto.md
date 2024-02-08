---
title: Mithilfe der Übergangsdifferenz zu Kontenfunktion Zahlungen abzustimmen
description: 'Beschreibt, wie Zahlungen verarbeitet werden, die nicht mit einem Beleg ausgeglichen werden können - beispielsweise wenn ein Wechselkurs Beträge bucht, die sich unterscheiden.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, cash receipts'
ms.search.form: '1290, 1294, 1287'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Zahlungen abstimmen, die nicht automatisch ausgeglichen werden können
Gelegentlich müssen Sie Zahlungen an Ihr Bankkonto bearbeiten, die nicht mit einem zugehörigen offenen Debitor, Kreditor oder einem Bankposten ausgeglichen werden kann. Gründe können sein, dass kein Beleg im [!INCLUDE[prod_short](includes/prod_short.md)] vorhanden ist, damit die Zahlung ausgeglichen werden kann oder dass der zugehörige Beleg im [!INCLUDE[prod_short](includes/prod_short.md)] einen anderen Betrag aufweist als der Transaktionsbetrag, zum Beispiel aufgrund von "Währungswechselkursen". Auf der Seite **Zahlungs-Abstimmungs-Buch** erscheinen alle Transaktion für Zahlungen, die noch nicht ausgeführt wurden im Feld **Differenz**, einschließlich Beträge, die aufgrund der Gründe wie oben nicht ausgeglichen werden können.

Die Methoden zur Lösung dieser Arten von nicht beantragten Zahlungen:
* Manuell ausgleichen
* Text-zu-Konto-Zuordnung verwenden
* Übertragen Sie einen überschüssigen Betrag in eine Journalzeile, um den erforderlichen Eintrag zu erstellen und zu buchen, z. B. eine Rückerstattung einer Überzahlung.

Zahlungen, die nicht angewendet werden können, können in Zahlungsabstimmungsbuch.-Blattzeilen auf die folgenden Arten erscheinen:

* Der Wert im Feld **Differenz** entspricht dem Wert im Feld **Transaktions-Betrag**, das angibt, dass kein Teil der Zahlung mit einem zugehörigen offenen Debitor, Kreditor oder einem Bankposten ausgeglichen werden kann.
* Der Wert im Feld **Differenz** ist tiefer als der Wert im Feld **Transaktions-Betrag**, das angibt, dass ein Teil der Zahlung mit einem zugehörigen offenen Debitor, Kreditor oder einem Bankposten ausgeglichen werden kann. Der restliche Teil der Zahlung kann nicht angewendet und muss manuell oder durch direktes Buchen auf ein Konto erfolgen.

Um solche Zahlungen abzustimmen, können Sie die Aktion **Übergangsdifferenz zur Konto** auswählen und dann definieren, auf welches Konto im Feld **Differenz** er gebucht wird wenn Sie das Zahlungsabstimmungsbuch.-Blatt buchen. Sie können dies entweder über die Seite **Zahlungsabstimmungsbuch.-Blatt** oder über die Seite **Überprüfung des Zahlungsantrags** tun, die Sie öffnen, indem Sie den Wert im Feld **Übereinstimmungsgenauigkeit** oder durch Auswahl des Felds **Unterschied** auswählen.

> [!TIP]  
>   Ähnliche Funktionen sind vorhanden, um automatische Abstimmung von wiederkehrenden Zahlungen einzurichten, die mit keinem zugehörigen offenen Debitor, Kreditor oder die Bankposten ausgeglichen werden können. Weitere Informationen finden Sie unter [Zuordnen von sich wiederholenden Zahlungen an Konten bei der automatischen Abstimmung](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)

## Abstimmen von Zahlungen, die nicht automatisch übernommen werden können
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Zahlungsausgangs Buch.-Blätter** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie ein Zahlungsabstimmungsbuch.-Blatt. Weitere Informationen finden Sie unter [Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-auto-application.md).
3. Wählen Sie **Differenz auf Konto buchen**. Die Seite **Differenz auf Konto buchen** öffnet sich.
4. Im Feld **Kontoart** definieren Sie die Kontoart, auf die der Zahlungsbetrag gebucht werden soll.
5. Im Feld **Kontonr.** definieren Sie die Kontoart, auf die der Zahlungsbetrag gebucht werden soll.
6. Geben Sie im Feld **Beschreibung** den Text an, der diese direkte Zahlungsbuchung beschreibt. Standardmäßig wird der Text im Feld **Transaktionstext** auf der Zahlungsabstimmungsbuch.-Blattzeile eingefügt.
7. Wählen Sie die Schaltfläche **OK** aus.

Wenn der Wert im Feld **Differenz** dem Wert im Feld **Transaktions-Betrag** entspricht, wenn Sie das Zahlungsabstimmungsbuch.-Blatt buchen, werden alle Zahlungen der Buch.-Blattzeile direkt auf das angegebene Gegenkonto gebucht.

Wenn der Wert im Feld **Differenz** kleiner ist als der Wert im Feld **Transaktions-Betrag** wird eine zusätzliche Buch.-Blattzeile mit dem gleichen Text und Datum und mit der Differenz erstellt, die im Feld **Transaktions-Betrag** eingefügt wird. In der ursprünglichen Buch.-Blattzeile wird die Differenz vom Wert im Feld **Transaktions-Betrag** abgezogen und die Zahlung muss dem entsprechenden Debitor, Kreditor oder Bankposteneintrag zugewiesen werden. Wenn Sie im Zahlungsabstimmungsbuch.-Blatt buchen, wird ein Teil der Zahlung als zugewiesene Zahlung gebucht. Der andere Teil der Zahlung wird direkt auf das angegebene Konto gebucht.

## Weitere Informationen
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]