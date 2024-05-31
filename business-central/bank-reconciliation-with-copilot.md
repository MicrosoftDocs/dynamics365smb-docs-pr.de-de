---
title: Bankkontoabstimmung mit der Unterstützung bei Bankkontoabstimmung
description: 'Erfahren Sie, wie Sie Copilot verwenden, um Bankkonten in Business Central abzustimmen.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 04/15/2024
ms.custom: bap-template
---

# <a name="reconcile-bank-accounts-with-copilot-preview"></a>Bankkontoabstimmung mit Copilot (Vorschauversion)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

In diesem Artikel wird erläutert, wie Sie die Unterstützung bei Bankkontoabstimmung verwenden, um Banktransaktionen mit Sachbucheinträgen in Business Central abzugleichen.

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="about-bank-account-reconciliation-assist"></a>Über die Unterstützung bei Bankkontoabstimmung

Bei der Unterstützung bei Bankkontoabstimmung handelt es sich um eine Reihe von KI-gestützten Features, die Sie bei der Abstimmung von Bankkonten unterstützen. Die Unterstützung bei der Bankkontoabstimmung bietet Ihnen über Copilot zwei unterschiedliche Aufgaben:

- Verbesserte Zuordnung von Transaktionen mit Sachbucheinträgen

   Vielleicht sind Sie ja bereits mit der Aktion **Automatisch abgleichen** auf der Seite **Bankkontoabstimmung** vertraut, welche die meisten Banktransaktionen automatisch Sachbucheinträgen zuordnet. Wir bezeichnen diesen Vorgang als *automatische Zuordnung*. Obwohl die automatische Zuordnung gut funktioniert, können die verwendeten Algorithmen manchmal zu vielen nicht zugeordneten Transaktionen führen. Copilot nutzt KI-Technologie, um verbleibende Transaktionen zu überprüfen und anhand der Daten, Beträge und Beschreibungen weitere Übereinstimmungen zu identifizieren. Wenn beispielsweise mehrere Rechnungen von einem Kunden als Abschlag bezahlt wurden, gleicht Copilot die einzelne Kontoauszugspositionen mit den Sachbucheinträgen für die Rechnung ab.

   Gehen Sie zu [Bankkontoabstimmung mit Copilot](#reconcile-bank-accounts-with-copilot).

- Vorgeschlagene Sachkonten

  Für verbleibende Banktransaktionen, die keinem Sachbucheintrag zugeordnet werden können, vergleicht Copilot die Transaktionsbeschreibung mit Sachkontonamen und schlägt das wahrscheinlichste Sachkonto vor, auf das gebucht werden soll. Beispielsweise könnte Copilot vorschlagen, Transaktionen mit der Meldung „Tanken 24“ auf das Konto „Beförderung“ zu buchen.
  
   Gehen Sie zu [Nicht zugeordnete Banktransaktionen auf die vorgeschlagenen Sachbuchkonten buchen](#post-unmatched-bank-transaction-amounts-to-suggested-general-ledger-accounts).

## <a name="prerequisites"></a>Voraussetzungen

- Die Unterstützung bei Bankkontoabstimmung ist aktiviert. Diese Aufgabe wird von Administrierenden ausgeführt. [Erfahren Sie mehr über das Konfigurieren von Copilot- und KI-Funktionen](enable-ai.md).
- Bankkonten in Business Central, die Sie abstimmen möchten, sind mit einem Onlinebankkonto verknüpft oder mit einem -Format für den Kontoauszugsimport eingerichtet. 
- Sie sind mit der Bankkontenabstimmung in Business Central vertraut, wie unter [Bankkonten abstimmen](bank-how-reconcile-bank-accounts-separately.md) beschrieben. 

<!--H2s. Required. A how-to article explains how to do a task. The bulk of each H2 should be a procedure.-->
## <a name="reconcile-bank-accounts-with-copilot"></a>Bankkontoabstimmung mit Copilot

<!-- Similar to the **Match Automatically** capability on the **Bank Acc. Reconciliation** page, Bank account reconciliation assist can also automatically matches transactions in banks statements with bank entries. The difference is that **Match Automatically** uses a native rules-based algorithm, while Bank account reconciliation assist is based AI technology though Copilot. Bank account reconciliation assist is intended to supplement the **Match Automatically** capability. While **Match Automatically** is fairly successful at matching transactions, there are some instances where it can't&mdash;which is where Bank account reconciliation assist comes. By using the **Reconcile with Copilot** action on **Bank Acc. Reconciliation** page, you can find even more matches.-->

Copilot soll bei der Bankkontoabstimmung als Ergänzung zur automatischen Zuordnung eingesetzt werden. Aus diesem Grund wird bei Verwendung von Copilot zuerst die automatische Zuordnung ausgeführt, um die ersten Zuordnungen vorzunehmen. Anschließend wird Copilot ausgeführt, um zu versuchen, Transaktionen zuzuordnen, welche die automatische Zuordnung nicht verarbeitet hat.   

Es gibt zwei Ansätze, Bankkonten mit Copilot abzustimmen. Sie können Copilot verwenden, um direkt von dort aus eine neue Abstimmung für ein Bankkonto direkt von der Liste **Bankkontoabstimmung** zu starten, oder Sie können Copilot für eine neue oder bestehende Abstimmung auf der Karte **Bankkontoabstimmung** verwenden.

# [Von der Liste „Bankkontoabstimmungen“](#tab/fromlist) 

Bei diesem Ansatz erstellen und stimmen Sie eine neue Bankkontenabstimmung von Grund auf ab. Bei diesem Ansatz müssen Sie das Bankkonto auswählen und die Kontoauszugsdatei importieren, wenn das Bankkonto nicht mit einem Onlinekonto verknüpft ist.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Bankkontoabstimmungen** ein, und wählen Sie dann den zugehörigen Link. 
1. Wählen Sie die Aktion **Mit Copilot abstimmen** aus, um das Fenster **Mit Copilot abstimmen** zu öffnen.
1. Legen Sie das Feld **Abstimmung für dieses Bankkonto durchführen** auf das Bankkonto fest, das Sie abstimmen möchten.

   ![Zeigt das Fenster „Mit Copilot abstimmen“ für die Abstimmung von Grund auf an](media/reconcile-bank-accounts-new-copilot.svg) 
 
1. Wenn das ausgewählte Bankkonto nicht mit einem Onlinebankkonto verknüpft ist, müssen Sie die Kontoauszugsdatei importieren. Um die Datei zu importieren, wählen Sie entweder den Wert im Feld **Transaktionsdaten verwenden aus** oder die Büroklammer-Schaltfläche neben der Schaltfläche **Generieren** aus. Dann verwenden Sie **Wählen Sie die zu importierende Datei aus.**, um die Kontoauszugsdatei zu importieren, indem Sie sie entweder von Ihrem Gerät hineinziehen oder Ihr Gerät nach ihr durchsuchen.
1. Für die Abstimmung mit Copilot wählen Sie **Generieren**.

   Copilot beginnt mit der Generierung vorgeschlagener Zuordnungen. Wenn der Vorgang abgeschlossen ist, werden im Fenster „Mit Copilot abstimmen“ die Ergebnisse der Zuordnung angezeigt.

1. Überprüfen Sie wie im folgenden Abschnitt beschrieben die vorgeschlagenen Zuordnungen.

# [Von einer Bankkontoabstimmungskarte](#tab/fromcard) 

Bei diesem Ansatz verwenden Sie Copilot entweder für eine neue Bankkontoabstimmung, die Sie manuell oder durch Bearbeiten einer vorhandenen Abstimmung erstellen. 


1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Bankkontoabstimmungen** ein, und wählen Sie dann den zugehörigen Link. 
1. Führen Sie einen der folgenden Schritte aus:

   - Wählen Sie **Neu**, um eine neue Abstimmung zu starten. 
   - Wählen Sie eine vorhandene Abstimmung aus der Liste aus und öffnen Sie sie.
1. Wählen Sie auf der Karte **Bankkontoabstimmung** **Mit Copilot abstimmen** aus

   ![Zeigt die Aktion „Mit Copilot abstimmen“ auf der Karte „Bankkontoabstimmung“](media/bank-reconciliation-copilot-card.svg) 

   Copilot beginnt mit der Generierung vorgeschlagener Zuordnungen. Wenn der Vorgang abgeschlossen ist, werden im Fenster **Mit Copilot abstimmen** die Ergebnisse der Zuordnung angezeigt. 

1. Überprüfen Sie wie im folgenden Abschnitt beschrieben die vorgeschlagenen Zuordnungen. 
---

### <a name="review-save-or-discard-proposed-matches"></a>Vorgeschlagene Übereinstimmungen überprüfen, speichern oder verwerfen

Nachdem Sie Copilot ausgeführt haben, werden im Fenster **Mit Copilot abstimmen** die detaillierten Ergebnisse angezeigt, einschließlich aller vorgeschlagenen Zuordnungen. Zu diesem Zeitpunkt wurden keine von Copilot vorgeschlagenen Zuordnungen gespeichert, sodass Sie die Vorschläge überprüfen und nach Belieben speichern oder verwerfen können.

![Zeigt das Fenster „Mit Copilot abstimmen“ mit vorgeschlagenen Zuordnungen an](media/bank-reconciliation-copilot-window.png) 

Das Copilot-Fenster ist in zwei Abschnitte unterteilt. Der obere Abschnitt enthält einige allgemeine Details zum Ergebnis, wie in der folgenden Tabelle beschrieben.  Im unteren Abschnitt **Zugeordnete Vorschläge** sind die von Copilot vorgeschlagenen Zuordnungen aufgeführt.

|Feld|Beschreibung|
|-|-|
|Automatisch abgeglichen|Gibt an, wie viele Posten auf dem Bankauszug durch die automatische Zuordnung zugeordnet werden können. Wählen Sie den Wert aus, um die Abstimmungskarte anzuzeigen.  |
|Copilot-Übereinstimmung|Gibt an, für wie viele Posten auf dem Bankauszug Zuordnungen durch Copilot vorgeschlagen wurden. Einzelheiten zu den Übereinstimmungen finden Sie im Abschnitt **Vorgeschlagene Zuordnungen**.|
|Auszug Schluss-Saldo|Gibt den Schlusssaldo des Bankkontoauszugs an, mit dem Sie die Abstimmung vornehmen|
|Buchen, wenn vollständig angewendet|Aktivieren Sie diesen Umschalter, wenn Sie die Bankkontoabstimmung automatisch buchen möchten, wenn alle Positionen (100 %) zugeordnet sind und Sie **Behalten** ausgewählt haben.|

#### <a name="save-or-discard-proposed-matches"></a>Vorgeschlagene Übereinstimmungen speichern oder verwerfen

Überprüfen Sie im Abschnitt **Zugeordnete Vorschläge** Position für Position die vorgeschlagenen Zuordnungen und ergreifen Sie dann die entsprechenden Maßnahmen:

- Um eine einzelne vorgeschlagene Zuordnung zu verwerfen, wählen Sie sie in der Liste und dann die Aktion **Position löschen** aus.

- Um alle vorgeschlagenen Zuordnungen zu verwerfen und das Copilot-Fenster zu schließen, klicken Sie auf die Schaltfläche „Verwerfen“ (Papierkorb). ![Zeigt das Papierkorbsymbol zum Löschen aller Copilot-Vorschläge für die Bankkontoabstimmung](media/copilot-delete-trash-can.png) neben der **Behalten**-Schaltfläche unten am Fenster.

- Um die vollständig abgeglichene Abstimmung beim Speichern automatisch zu buchen, aktivieren Sie den Umschalter **Buchen, wenn vollständig angewendet**.  
- Um die aktuell im Copilot-Fenster angezeigten Übereinstimmungen zu speichern, wählen Sie **Behalten**.

## <a name="post-unmatched-bank-transaction-amounts-to-suggested-general-ledger-accounts"></a>Nicht zugeordnete Banktransaktionen auf die vorgeschlagenen Sachbuchkonten buchen

In diesem Abschnitt erfahren Sie, wie Sie mit Copilot nicht abgestimmte (im Feld **Differenz** angegebene) Kontoauszugspositionen auf ein Sachkonto buchen. Diese Aufgabe kann nur aus einer bestehenden Abstimmung heraus durchgeführt werden.

1. Gehen Sie zur Liste **Bankkontenabstimmungen** und öffnen Sie die vorhandene Abstimmung, die die nicht abgestimmten Positionen enthält.

   Beginnen Sie mit der Eröffnung einer bestehenden Bankkontoabstimmung. Dieser Schritt bietet Ihnen einen klaren Überblick über alle nicht abgestimmten Kontoauszugspositionen, die auf das Sachkonto übertragen werden müssen.

1. Identifizieren Sie im Bereich **Kontoauszugspositionen** nicht abgeglichenen Kontoauszugspositionen und wählen Sie eine oder mehrere Positionen aus, die Sie abstimmen möchten.

   Diese Positionen sind die Kontoauszugspositionen, auf die sich Copilot bei der Buchung neuer Zahlungen auf das Sachkonto konzentriert.

1. Wählen Sie **Differenz auf Sachkonto buchen**, um den Vorgang zu starten.

   ![Zeigt die Aktion zur Übertragung an Sachkonto mit Copilot auf der Karte „Bankkontoabstimmung“](media/bank-reconciliation-transfer-gl-copilot-card.png) 

   Dadurch beginnt Copilot mit der Generierung von Vorschlägen für die Buchung neuer Zahlungen.

1. Sobald Copilot die Generierung von Vorschlägen abgeschlossen hat, wird das Fenster **Copilot-Vorschläge für das Buchen von Differenzbeträgen auf Sachkonten** geöffnet.

   In diesem Fenster werden die Vorschläge im Abschnitt **Zugeordneter Vorschlag** angezeigt. Die Erfahrung ist ähnlich wie bei Copilot.

   ![Zeigt die Seite „Übertragung an Sachkonto mit vorgeschlagenen Copilot-Zuordnungen“ für die Bankkontoabstimmung an](media/bank-reconciliation-gl-transfer-proposed-matches.png) 

1. Überprüfen Sie jeden Vorschlag Position für Position, um sicherzustellen, dass die zur Buchung vorgeschlagenen Zahlungen richtig sind.

   - Wenn Sie einen Drilldown für den Vorschlag durchführen, indem Sie ihn in der Liste auswählen, gelangen Sie zu einer Liste mit Konten. Von hier aus können Sie ein anderes Konto auswählen. Diese Art der manuellen Korrektur ist nur bei Verwendung des Flows **Differenz auf Sachkonto buchen** möglich, nicht im Zuordnungs-Flow. 
   - Wenn Sie **Speichern ...** neben einem Vorschlag auswählen, können Sie die Zuordnung der Seite **Text zu Konto zuordnen** hinzufügen, sodass, wenn dieser Text das nächste Mal bei der Abstimmung erscheint, er dem vorgeschlagenen Konto zugeordnet wird.

1. Verwerfen oder speichern Sie Vorschläge.

   - Wenn Sie eine bestimmte Zuordnung verwerfen möchten, wählen Sie sie in der Liste und dann **Position löschen** aus. Um alle Zuordnungen zu verwerfen und Copilot zu schließen, klicken Sie auf die Schaltfläche „Verwerfen“ (Papierkorb). ![Zeigt das Papierkorbsymbol zum Löschen aller Copilot-Vorschläge für die Bankkontoabstimmung](media/copilot-delete-trash-can.png) neben der **Behalten**-Schaltfläche unten am Fenster.

   - Wenn die Vorschläge Ihren Anforderungen entsprechen und Sie sie speichern möchten, wählen Sie **Behalten**.

      Dieser Schritt bestätigt die Übertragung der aktuell ausgewählten Vorschläge vom Bankkonto auf das Sachkonto. Es bucht neue Zahlungen auf die vorgeschlagenen Sachkonten und wendet entsprechende Zeilen auf die resultierenden Bankkontoeinträge an.

## <a name="next-steps"></a>Nächste Schritte

[Ihrer Bankkontoabstimmung validieren](bank-how-reconcile-bank-accounts-separately.md#validate-your-bank-reconciliation)  

## <a name="see-also"></a>Siehe auch
[Probleme mit Copilot- und KI-Funktionen behandeln](ai-copilot-troubleshooting.md)  
[Häufig gestellte Fragen zur verantwortungsbewussten KI bei Unterstützung bei Bankkontoabstimmung](faqs-bank-reconciliation.md)  
[Einrichten von Banken](bank-setup-banking.md)  
[Bankkonten abstimmen](bank-how-reconcile-bank-accounts-separately.md)  
[Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md) 
