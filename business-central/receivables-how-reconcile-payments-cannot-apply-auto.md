---
title: Verwenden der Funktion „Differenz auf Konto übertragen“ zum Abgleichen von Zahlungen
description: 'Beschreibt die Verarbeitung von Zahlungen, die einem Dokument nicht zugeordnet werden können, z. B. wenn aufgrund eines Wechselkurses die Beträge abweichen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, cash receipts'
ms.search.form: '1290, 1294, 1287'
ms.date: 07/08/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Abgleichen von Zahlungen, die nicht automatisch angewendet werden können
Möglicherweise müssen Sie gelegentlich Zahlungen auf Ihr Bankkonto abwickeln, die keinem zugehörigen offenen Debitoren-, Kreditoren- oder Bankkontoposten zugeordnet werden können. Gründe hierfür können sein, dass kein Dokument vorhanden ist, dem die Zahlung zugeordnet werden kann, oder dass das zugehörige Dokument einen anderen Betrag aufweist als der Transaktionsbetrag, beispielsweise aufgrund einer Währungsumrechnung. [!INCLUDE[prod_short](includes/prod_short.md)]  [!INCLUDE[prod_short](includes/prod_short.md)]  Auf der Seite  **Zahlungsabstimmungsjournal**  werden alle Transaktionsbeträge für Zahlungen, die noch nicht angewendet wurden, im Feld  **Differenz**  angezeigt, einschließlich der Beträge, die aus Gründen wie den oben genannten nicht angewendet werden können.

Die Methoden zur Lösung dieser Arten von nicht beantragten Zahlungen:
* Manuell ausgleichen
* Text-zu-Konto-Zuordnung verwenden
* Übertragen Sie einen überschüssigen Betrag in eine Journalzeile, um den erforderlichen Eintrag zu erstellen und zu buchen, z. B. eine Rückerstattung einer Überzahlung.

Zahlungen, die nicht angewendet werden können, können in den Zahlungsabstimmungserfassungszeilen auf folgende Arten angezeigt werden:

* Der Wert im Feld **Differenz** entspricht dem Wert im Feld **Transaktions-Betrag**, das angibt, dass kein Teil der Zahlung mit einem zugehörigen offenen Debitor, Kreditor oder einem Bankposten ausgeglichen werden kann.
* Der Wert im Feld **Differenz** ist tiefer als der Wert im Feld **Transaktions-Betrag**, das angibt, dass ein Teil der Zahlung mit einem zugehörigen offenen Debitor, Kreditor oder einem Bankposten ausgeglichen werden kann. Der verbleibende Teil der Zahlung kann nicht angewendet werden und muss manuell oder durch direkte Buchung auf ein Konto abgeglichen werden.

Um solche Zahlungen abzustimmen, können Sie die Aktion **Übergangsdifferenz zur Konto** auswählen und dann definieren, auf welches Konto im Feld **Differenz** er gebucht wird wenn Sie das Zahlungsabstimmungsbuch.-Blatt buchen. Sie können dies entweder über die Seite **Zahlungsabstimmungsbuch.-Blatt** oder über die Seite **Überprüfung des Zahlungsantrags** tun, die Sie öffnen, indem Sie den Wert im Feld **Übereinstimmungsgenauigkeit** oder durch Auswahl des Felds **Unterschied** auswählen.

> [!TIP]  
>   Ähnliche Funktionen sind vorhanden, um automatische Abstimmung von wiederkehrenden Zahlungen einzurichten, die mit keinem zugehörigen offenen Debitor, Kreditor oder die Bankposten ausgeglichen werden können. Weitere Informationen finden Sie unter [Zuordnen von sich wiederholenden Zahlungen an Konten bei der automatischen Abstimmung](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)

## So gleichen Sie Zahlungen ab, die nicht automatisch angewendet werden können
1. Wählen Sie das ![Glühbirne, die das „Sie wünschen ...“-Feature öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Zahlungsausgangs Buch.-Blätter** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie ein Zahlungsabstimmungsbuch.-Blatt. Weitere Informationen finden Sie unter [Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-auto-application.md).
3. Wählen Sie **Differenz auf Konto buchen**. Die Seite **Differenz auf Konto buchen** öffnet sich.
4. Im Feld **Kontoart** definieren Sie die Kontoart, auf die der Zahlungsbetrag gebucht werden soll.
5. Im Feld **Kontonr.** definieren Sie die Kontoart, auf die der Zahlungsbetrag gebucht werden soll.
6. Geben Sie im Feld **Beschreibung** den Text an, der diese direkte Zahlungsbuchung beschreibt. Standardmäßig wird der Text im Feld **Transaktionstext** auf der Zahlungsabstimmungsbuch.-Blattzeile eingefügt.
7. Wählen Sie die Schaltfläche **OK** aus.

Wenn der Wert im Feld **Differenz** dem Wert im Feld **Transaktions-Betrag** entspricht, wenn Sie das Zahlungsabstimmungsbuch.-Blatt buchen, werden alle Zahlungen der Buch.-Blattzeile direkt auf das angegebene Gegenkonto gebucht.

Wenn der Wert im Feld **Differenz** kleiner ist als der Wert im Feld **Transaktions-Betrag** wird eine zusätzliche Buch.-Blattzeile mit dem gleichen Text und Datum und mit der Differenz erstellt, die im Feld **Transaktions-Betrag** eingefügt wird. In der ursprünglichen Buch.-Blattzeile wird die Differenz vom Wert im Feld **Transaktions-Betrag** abgezogen und die Zahlung muss dem entsprechenden Debitor, Kreditor oder Bankposteneintrag zugewiesen werden. Wenn Sie im Zahlungsabstimmungsbuch.-Blatt buchen, wird ein Teil der Zahlung als zugewiesene Zahlung gebucht. Der andere Teil der Zahlung wird direkt auf das angegebene Konto gebucht.

## Siehe auch
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]