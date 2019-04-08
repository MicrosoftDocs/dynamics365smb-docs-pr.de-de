---
title: Ausgabe, Drucken, Stornieren und Annullieren von Schecks| Microsoft Docs
description: Beschreibt, wie Schecks mithilfe des Zahlungsausgangs Buch.-Blattes, ausgegeben, gedruckt oder annulliert werden oder wie Check-Sachposteneinträge in Business Central angezeigt werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 4dd8f50f4d7767cb70b53a16009b86f135a5f5c6
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "797970"
---
# <a name="make-check-payments"></a>Zahlung per Scheck machen
Sie können elektronischerund und manuelle Schecks ausgeben in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Bei beiden Verfahren erfolgt die Ausstellung von Schecks an Kreditoren über das Zahlungsausgangs-Buch.-Blatt. Sie können auch Schecks annullieren und Scheckposten anzeigen.

Der folgende Ablauf zeigt, wie ein Kreditor mit Computer-Schecks bezahlt wird, indem die Zahlung für die zu bezahlende Rechnung erfolgt, der Scheck gedruckt und die Zahlung als bezahlt gebucht wird. Dadurch ergibt sich positiver Kreditorenposten, der auf einen negativen Bankpostens angewendet wurd und der physische Check von der Bank verarbeitet wird.

Sie können mit zwei Arten von Schecks bezahlen Für beide Arten müssen **Bal. Kontoart** oder **Kontoart** das Feld **Bankkonto** enthalten.

- **Computer Scheck**: Wählen Sie diese Option, wenn Sie einen Scheck über den in der Buch.-Blattzeile angezeigten Betrag drucken wollen. Sie müssen die Schecks drucken, bevor Sie die Buch.-Blattzeilen buchen können. Sie können nur **Computer Scheck** wenn
- **Manueller Scheck**: Wählen Sie diese Option, wenn Sie einen Scheck manuell ausstellen und einen entsprechenden Scheckposten über diesen Betrag anlegen möchten. Mit dieser Option ist das automatische Drucken von Schecks nicht möglich.

> [!NOTE]  
> Um sicherzustellen, dass Ihre Bank nur Schecks und Beträge freigibt, können Sie ihr eine Datei senden, die die Daten für Kreditoren, Schecks und Zahlungsinformationen enthält. Weitere Informationen finden Sie unter [Datei Positive Pay exportieren](finance-how-positive-pay.md).

Der Drucker muss für den Ausdruck von Scheckformularen eingerichtet werden, und Sie müssen festlegen welches Layout verwendet werden soll. Weitere Informationen zum Definieren von Attributen finden Sie unter [Definieren von Scheck-Layouts](finance-how-define-check-layouts.md).

Sie können bis 10 Rechnungen auf einer Seite für einen Scheckabschnitt drucken. Wenn ein Häkchen in mehr als 10 Rechnungen angewendet wird, wenn Sie den Abschnitt drucken, stornieren wir den Scheck auf der ersten Seite und drucken den Begriff UNGÜLTIG auf den Scheck. Wir drucken dann die restlichen Rechnungen und den gesamten Scheckbetrags auf der zweiten Seite. 

## <a name="to-pay-a-vendor-invoice-with-a-computer-check"></a>Um Kreditorenrechnungen mit einem Computer Scheck zu bezahlen
Nachfolgend wird erläutert, wie Sie einen Kreditor mit Schecks bezahlen. Die Schritte sind ähnlich, wie wenn sie Ihren Debitoren Scheck zurückerstatten.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Zahlungs-Buch.-Blätter** ein, und wählen dann den zugehörigen Link aus.
2. Füllen Sie die Zalungszeilen ein. Weitere Informationen finden Sie unter [Zahlungen und Rückerstattungen aufzeichnen](payables-how-post-payments-refunds.md)
3. Wählen Sie im Feld die **Zahlungsform** aus und wählen Sie **Check**.
4. Wählen Sie im Feld **Bankkontozahlungsart** die Option **Computer Scheck** aus.
5. Wählen Sie die Aktion **Check Drucken** aus.
6. Füllen Sie auf der Seite **Scheck** die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Wählen Sie die Schaltfläche **Senden an** aus, wählen Sie die Option **PDF-Dokument**, und wählen Sie dann die Schaltfläche **OK** aus.

    Die Warenkontrollen können jetzt bereitgestellt werden für die Bank für die Bearbeitung. Fahren Sie fort, um die Zahlung für den Kreditor und im System als bezahlt zu buchen.
8. Wählen Sie die Aktion **Buchen** aus.

Völlig ausgeglichene Kreditorenposten und Bankposten werden erstellt.

> [!NOTE]  
> Wenn Sie Schecks in mehreren Währungen von mehreren Bankkonten aus ausdrucken und bezahlen möchten, muss die Stapelverarbeitung **Scheck drucken** für jede einzelne Währung ausgeführt und das entsprechende Bankkonto muss angegeben werden.

## <a name="to-cancel-printed-checks-that-are-not-posted"></a>Um gedruckte Scheck die nicht gebucht wurden zu stornieren
Sie können nicht gebuchte Schecks stornieren, nachdem sie gedruckt wurden, indem Sie die Aktion **Scheck annullieren** auf der Seite **Zahlungsausgangs Buch.-Blatt** verwenden.

1. Wählen Sie auf der Seite **Zahlungsausgangs Buch.-Blatt** **Scheck annullieren** aus, und wählen Sie aus, welche Prüfungen durchgeführt zum stornieren mit den Schecks durchgeführt werden.

## <a name="to-void-checks"></a>Annullieren von Schecks
Wenn Scheckzahlung gebucht wurden, können Sie Schecks aus den resultierenden Bankposten nur stornieren (annulieren).

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Bankkonten** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie das entsprechende Bankkonto aus, wählen Sie die **Bearbeiten**-Aktion aus, und wählen Sie dann die **Scheckposten**-Aktion aus.
3. Auf der Seite **Scheckposten** wählen Sie die **Scheck annullieren**-Aktion aus.
4. Wählen das Kontrollkästchen **Scheck nur annullieren**.
5. Wählen Sie die Schaltfläche **OK** aus.

## <a name="to-view-a-summary-of-posted-checks"></a>Um eine Zusammenfassung der gebuchten Schecks anzuzeigen
Wenn Sie gebuchte Schecks überprüfen möchten, zum Beispiel, um Mehrfachverbindungsschecks für einen Kreditor zu überprüfen, können Sie **Bankkonto - Scheckdetails** verwenden.
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Bankkonto - Details prüfen** ein, und wählen dann den zugehörigen Link aus.
2. Legen Sie Filter fest und wählen Sie dann die Schaltfläche **Vorschau** aus.

## <a name="see-also"></a>Siehe auch
[Zahlungen vornehmen](payables-make-payments.md)  
[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Einrichten von Banken](bank-setup-banking.md)  
[Um eine Positive Pay-Datei zu exportieren](finance-how-positive-pay.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
