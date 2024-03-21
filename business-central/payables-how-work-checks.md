---
title: 'Schecks ausstellen, drucken, stornieren und annullieren'
description: 'Beschreibt, wie Schecks mithilfe des Zahlungsausgangs Buch.-Blattes, ausgegeben, gedruckt oder annulliert werden oder wie Check-Sachposteneinträge in Business Central angezeigt werden.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment journal, print check, vendor payment, creditor, debt, balance due, AP'
ms.search.form: '256, 404,'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Zahlung per Scheck machen

Sie können elektronischerund und manuelle Schecks ausgeben in [!INCLUDE[prod_short](includes/prod_short.md)]. Bei beiden Verfahren erfolgt die Ausstellung von Schecks an Kreditoren über das Zahlungsausgangs-Buch.-Blatt. Sie können auch Schecks annullieren und Scheckposten anzeigen.

Der folgende Ablauf zeigt, wie ein Kreditor mit Computer-Schecks bezahlt wird, indem die Zahlung für die zu bezahlende Rechnung erfolgt, der Scheck gedruckt und die Zahlung als bezahlt gebucht wird. Dadurch ergibt sich positiver Kreditorenposten, der auf einen negativen Bankpostens angewendet wurd und der physische Check von der Bank verarbeitet wird.

Sie können mit zwei Arten von Schecks bezahlen Für beide Arten müssen **Bal. Kontoart** oder **Kontoart** das Feld **Bankkonto** enthalten.

- **Computer Scheck**: Wählen Sie diese Option, wenn Sie einen Scheck über den in der Buch.-Blattzeile angezeigten Betrag drucken wollen. Sie müssen die Schecks drucken, bevor Sie die Buch.-Blattzeilen buchen können.
- **Manueller Scheck**: Wählen Sie diese Option, wenn Sie einen Scheck manuell ausstellen und einen entsprechenden Scheckposten über diesen Betrag anlegen möchten. Mit dieser Option ist das automatische Drucken von Schecks nicht möglich.

> [!NOTE]  
> Um sicherzustellen, dass Ihre Bank nur Schecks und Beträge freigibt, können Sie ihr eine Datei senden, die die Daten für Kreditoren, Schecks und Zahlungsinformationen enthält. Weitere Informationen finden Sie unter [Datei Positive Pay exportieren](finance-how-positive-pay.md).

> [!IMPORTANT]
> Der Drucker muss für den Ausdruck von Scheckformularen eingerichtet werden, und Sie müssen festlegen welches Layout verwendet werden soll. Weitere Informationen finden Sie unter [Scheck-Layout auswählen](finance-how-define-check-layouts.md). Alternativ können Sie den Scheck beispielsweise als PDF-Datei senden.  

Sie können bis 10 Rechnungen auf einer Seite für einen Scheckabschnitt drucken. Wenn ein Häkchen in mehr als 10 Rechnungen angewendet wird, wenn Sie den Abschnitt drucken, stornieren wir den Scheck auf der ersten Seite und drucken den Begriff UNGÜLTIG auf den Scheck. Wir drucken dann die restlichen Rechnungen und den gesamten Scheckbetrags auf der zweiten Seite.

## Um Kreditorenrechnungen mit einem Computer Scheck zu bezahlen

Nachfolgend wird erläutert, wie Sie einen Kreditor mit Schecks bezahlen. Die Schritte sind ähnlich wie bei der Rückerstattung eines Debitors per Scheck.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Zahlungsausgangs Buch.-Blätter** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die Zalungszeilen ein. Weitere Informationen finden Sie unter [Zahlungen und Rückerstattungen aufzeichnen](payables-how-post-payments-refunds.md)
3. Wählen Sie im Feld die **Zahlungsform** aus und wählen Sie **Check**.
4. Wählen Sie im Feld **Bankkontozahlungsart** die Option **Computer Scheck** aus.
5. Wählen Sie die Aktion **Check Drucken** aus.
6. Füllen Sie auf der Seite **Scheck** die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Wenn Ihr Drucker zum Drucken von Schecks eingerichtet ist, wählen Sie die Schaltfläche **Drucken** aus. Andernfalls wählen Sie die Schaltfläche **Senden an**, die Option **PDF-Dokument** und dann die Schaltfläche **OK** aus, und drucken Sie anschließend das PDF-Dokument.

    Die physischen Schecks können jetzt zur Bearbeitung an die Kreditoren gesendet werden. Fahren Sie fort, um die Zahlung für den Kreditor und im System als bezahlt zu buchen.
8. Wählen Sie die Aktion **Buchen** aus.

Völlig ausgeglichene Kreditorenposten und Bankposten werden erstellt.

> [!NOTE]  
> Wenn Sie Schecks in mehreren Währungen von mehreren Bankkonten aus ausdrucken und bezahlen möchten, muss die Stapelverarbeitung **Scheck drucken** für jede einzelne Währung ausgeführt und das entsprechende Bankkonto muss angegeben werden.

## Um gedruckte Scheck die nicht gebucht wurden zu stornieren

Sie können nicht gebuchte Schecks stornieren, nachdem sie gedruckt wurden, indem Sie die Aktion **Scheck annullieren** auf der Seite **Zahlungsausgangs Buch.-Blatt** verwenden.

1. Wählen Sie auf der Seite **Zahlungsausgangs Buch.-Blatt** **Scheck annullieren** aus, und wählen Sie aus, welche Prüfungen durchgeführt zum stornieren mit den Schecks durchgeführt werden.

## Annullieren von Schecks

Wenn Scheckzahlung gebucht wurden, können Sie Schecks aus den resultierenden Bankposten nur stornieren (annulieren).

> [!IMPORTANT]
> Wenn der Scheck auf eine Rechnung angewendet wird, heben Sie den Scheck zuerst auf, damit die Rechnung zurückgezahlt werden kann, und stornieren Sie dann den Scheck. Wenn der Scheck gedruckt und keine Rechnung damit bezahlt wurde, wählen Sie **Scheck nur annullieren** aus, wie in diesem Abschnitt beschrieben.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Bankkonten** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie das entsprechende Bankkonto aus, wählen Sie die **Bearbeiten**-Aktion aus, und wählen Sie dann die **Scheckposten**-Aktion aus.
3. Auf der Seite **Scheckposten** wählen Sie die **Scheck annullieren**-Aktion aus.
4. Wählen das Kontrollkästchen **Scheck nur annullieren**.
5. Wählen Sie die Schaltfläche **OK** aus.

## Um eine Zusammenfassung der gebuchten Schecks anzuzeigen

Wenn Sie gebuchte Schecks überprüfen möchten, zum Beispiel, um Mehrfachverbindungsschecks für einen Kreditor zu überprüfen, können Sie **Bankkonto - Scheckdetails** verwenden.
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Bankkonto – Scheckdetails** ein, und wählen Sie dann den zugehörigen Link.
2. Legen Sie Filter fest und wählen Sie dann die Schaltfläche **Vorschau** aus.

## Siehe auch

[Zahlungen vornehmen](payables-make-payments.md)  
[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Einrichten von Banken](bank-setup-banking.md)  
[Um eine Positive Pay-Datei zu exportieren](finance-how-positive-pay.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
