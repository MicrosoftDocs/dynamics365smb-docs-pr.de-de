---
title: Ausgabe, Drucken, Stornieren und Annullieren von Schecks| Microsoft Docs
description: "Beschreibt, wie Schecks mithilfe des Zahlungsausgangs Buch.-Blattes, ausgegeben, gedruckt oder annulliert werden oder wie Check-Sachposteneinträge in Business Central angezeigt werden."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 0c1b37616b4aafc9535f2d3fbf60b915c490dd0b
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-checks"></a>Arbeiten mit Checks
Sie können elektronischerund und manuelle Schecks ausgeben in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Bei beiden Verfahren erfolgt die Ausstellung von Schecks an Kreditoren über das Zahlungsausgangs-Buch.-Blatt. Sie können auch Schecks annullieren und Scheckposten anzeigen.

Bei dem Verfahren zum Ausstellen von Schecks werden Zahlungsvorschläge gemacht, Scheckposten erstellt und die Computerschecks gedruckt.

> [!NOTE]  
>   Um sicherzustellen, dass Ihre Bank nur Schecks und Beträge freigibt, können Sie ihr eine Datei senden, die die Daten für Kreditoren, Schecks und Zahlungsinformationen enthält. Weitere Informationen finden Sie unter [Datei Positive Pay exportieren](finance-how-positive-pay.md).

Der Drucker muss für den Ausdruck von Scheckformularen eingerichtet werden, und Sie müssen festlegen welches Layout verwendet werden soll. Weitere Informationen zum Definieren von Attributen finden Sie unter [Definieren von Scheck-Layouts](finance-how-define-check-layouts.md).

## <a name="to-issue-checks"></a>Um Schecks auszustellen
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Zahlungs-Buchblatt** ein und wählen den zugehörenden Link aus.
2. Füllen Sie das Buch.-Blatt mit den entsprechenden Zahlungen aus, z. B. indem Sie die Zahlungsvorschläge verwenden. Weitere Informationen finden Sie unter [Erstellen von Zahlungsvorschlägen für Kreditoren](payables-how-suggest-vendor-payments.md).
3. Im Feld **Bankkontozahlungsart** der Buch.-Blattzeilen zur Zahlung, die Sie mit Schecks vornehmen möchten, wählen Sie eine der folgenden Optionen:

   * **Computer Scheck**: Wählen Sie diese Option, wenn Sie einen Scheck über den in der Buch.-Blattzeile angezeigten Betrag drucken wollen. Sie müssen die Schecks drucken, bevor Sie die Buch.-Blattzeilen buchen können. Sie können **Computer Scheck** nur auswählen, wenn **Gegenkontoart** oder **Kontoart** den Wert **Bankkonto** hat.
   * **Manueller Scheck**: Wählen Sie diese Option, wenn Sie einen Scheck manuell ausstellen und einen entsprechenden Scheckposten über diesen Betrag anlegen möchten. Mit dieser Option ist das automatische Drucken von Schecks in [!INCLUDE[d365fin](includes/d365fin_md.md)]nicht möglich. Sie können **Manueller Scheck** nur auswählen, wenn **Gegenkontoart** oder **Kontoart** den Wert **Bankkonto** hat.

     > [!NOTE]  
     >   Sie müssen die Computer Schecks drucken, bevor Sie die entsprechenden Buch.-Blattzeilen buchen können.
4. Im Falle von Computer Schecks wählen Sie **Scheck drucken** aus.
5. Füllen Sie im Fenster **Check** die Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Wählen Sie die Schaltfläche **Drucken** aus.

> [!NOTE]  
>   Wenn Sie Schecks in mehreren Währungen von mehreren Bankkonten aus ausdrucken möchten, muss der Batchauftrag **Scheck drucken** für jede einzelne Währung ausgeführt und das entsprechende Bankkonto angegeben werden.

## <a name="to-cancel-printed-checks-that-are-not-posted"></a>Um gedruckte Scheck die nicht gebucht wurden zu stornieren
Sie können nicht gebuchte Schecks stornieren, nachdem sie gedruckt wurden, indem Sie die Aktion **Scheck annullieren** im Fenster **Zahlungsausgangs Buch.-Blatt** verwenden.

1. Wählen Sie im Fenster **Zahlungsausgangs Buch.-Blatt** **Scheck annullieren** aus, und wählen Sie aus, welche Prüfungen durchgeführt zum stornieren mit den Schecks durchgeführt werden.

## <a name="to-void-checks"></a>Annullieren von Schecks
Wenn Scheckzahlung gebucht wurden, können Sie Schecks aus den resultierenden Bankposten nur stornieren (annulieren).

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Bankkonten** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie das entsprechende Bankkonto aus, wählen Sie die **Bearbeiten**-Aktion aus, und wählen Sie dann die **Scheckposten**-Aktion aus.
3. Im **Scheckposten**-Fenster wählen Sie die **Scheck annullieren**-Aktion aus.
4. Wählen das Kontrollkästchen **Scheck nur annullieren**.
5. Wählen Sie die Schaltfläche **OK** aus.

## <a name="see-also"></a>Siehe auch
[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Einrichten von Banken](bank-setup-banking.md)  
[Um eine Positive Pay-Datei zu exportieren](finance-how-positive-pay.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

