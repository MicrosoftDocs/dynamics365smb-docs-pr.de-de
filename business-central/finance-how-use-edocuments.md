---
title: E-Belege bei Verkäufen und Einkäufen verwenden
description: 'Erfahren Sie, wie Sie die E-Belege-Funktionalität im Zusammenhang mit Verkaufs- und Einkaufsrechnungen nutzen.'
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, sales, purchase'
ms.search.form: '42, 43, 51, 6103, 6133, 6121, 9301, 9305, 9308'
ms.date: 10/03/2023
ms.author: altotovi
---

# <a name="use-e-documents-in-sales-and-purchases"></a>E-Belege bei Verkäufen und Einkäufen verwenden

Sie können konfigurierte elektronische Belege (E-Belege) mit Verkaufs- und Einkaufsbelegen verwenden.

Sie können die folgenden Belege mit der E-Belege-Funktionalität verwenden:  

- Verkauf: 
    - Verkaufsrechnungen
    - Verkaufsaufträge
    - Verkaufsgutschriften
    - Servicerechnungen
    - Servicegutschriften
    - Zinsrechnungen
    - Mahnungen
- Einkauf: 
    - Einkaufsrechnungen
    - Bestellungen (nur neuen Beleg erstellen)
    - Einkaufsgutschriften
    - Fibu Buch.-Blätter

> [!NOTE]
> Derzeit kann eine Bestellung nur verwendet werden, wenn Sie den Beleg aus dem E-Beleg Ihres Kreditors erstellen. Sie können den vorhandenen Beleg jedoch nicht mit Zeilen aktualisieren, die Sie von Ihrem Kreditor erhalten haben.  

## <a name="e-documents-in-sales"></a>E-Belege im Verkauf

Um eine E-Rechnung zu erstellen und an einen Debitor zu senden, müssen Sie die Verkaufsrechnung erstellen und buchen. Weitere Informationen zum Standardprozess finden Sie unter [Fakturierung eines Verkaufs](sales-how-invoice-sales.md).

Nachdem Sie den Verkaufsbeleg gebucht haben, öffnen Sie die Seite **Gebuchte Verkaufsrechnung**, um auf die zugehörige Seite **E-Beleg** zuzugreifen.

### <a name="view-e-documents"></a>E-Belege aufrufen

Gehen Sie wie folgt vor, um vorhandene E-Belege anzuzeigen.

1. Wählen Sie auf der Seite **Gebuchte Verkaufsrechnung** **E-Beleg** \> **E-Beleg öffnen**.
2. Auf der Seite **E-Beleg** können Sie in der Kopfzeile grundlegende Informationen zur gebuchten Rechnung einsehen.
3. Das Feld **Datensatz** enthält die Belegnummer der gebuchten Verkaufsrechnung. Wählen Sie den Link aus, um den Beleg zu öffnen.
4. Im Feld **Status des elektronischen Belegs** können Sie den Echtzeitstatus des Belegs und seine Position in der Verarbeitungspipeline anzeigen. Wenn der Beleg gebucht ist, lautet der Status **Verarbeitet**.

### <a name="e-document-statuses-and-logs"></a>E-Beleg-Status und -Protokolle

Einzelheiten zum Dienststatus Ihres E-Belegs finden Sie im Inforegister **E-Beleg – Dienststatus**. Das System zeigt in den Zeilen einen oder mehrere Dienste an, die der Beleg verwendet hat. Im häufigsten Szenario verwendet jeder Beleg nur einen Dienst. Ein Beleg kann jedoch mehrere Dienste nutzen.

- Sehen Sie im Feld **E-Beleg – Dienstcode** heraus, welcher Dienst verwendet wurde.
- Entnehmen Sie dem Feld **Status des E-Belegs** den aktuellen Dienststatus für diesen Beleg.
- Wenn Sie weitere Details wünschen, wählen Sie das Feld **Protokolle** für den Dienst auf der Seite **E-Beleg-Protokolle** aus. Es wird eine chronologische Übersicht über die verschiedenen Status des Belegs angezeigt.
- Sehen Sie sich die Felder **Postennr.** und **Erstellt am** und andere Informationen auf der Seite **E-Beleg-Protokolle** an. Der erste Status im Feld **Status des E-Belegs** lautet **Exportiert**, was anzeigt, dass die E-Belegsdatei erstellt wurde. Der nächste Status ist **Gesendet**, was angibt, dass der Beleg an den Dienstanbieter gesendet wurde, sofern einer konfiguriert wurde.

Um mehr zu erfahren, wählen Sie den Posten mit dem Status **Exportiert** aus und führen Sie dann eine der folgenden Aktionen aus:

- **Zuordnungsprotokolle öffnen**: Erhalten Sie einen Überblick über alle aus den Quelltabellen im Feld **Ursprünglicher Wert** exportierten Felder. Wenn Sie beim Export Transformationsregeln verwendet haben, können Sie den Endwert auch im Feld **Neuer Wert** abrufen.
- **Exportdatei**: Exportieren Sie die XML-Datei zur manuellen Überprüfung.

Um die Kommunikation zwischen Ihnen und dem Dienst anzuzeigen, an den Sie Ihr Beleg senden, verwenden Sie das Feld **Kommunikationsprotokolle**. Öffnen Sie die Seite **Kommunikationsprotokolle für E-Belege**, um Details über die Anfrage und die Gründe für die Nachricht mit diesem Dienst anzuzeigen.

Wenn es ein Problem mit dem Dienstanbieter gibt und der Beleg nicht gesendet werden kann, achten Sie auf die folgenden Indikatoren auf der Seite **E-Beleg**:

- Das Feld **Status des elektronischen Belegs** in der Kopfzeile zeigt den Status **Fehler**.
- Das Feld **Status des E-Belegs** auf dem Inforegister **E-Beleg – Dienststatus** zeigt den Status **Fehler beim Senden**.
- Das Inforegister **Fehler und Warnungen** enthält eine oder mehrere Meldungen, die die Ursache des Problems angeben.

Nachdem das Problem behoben ist, führen Sie die Aktionen **Beleg senden** manuell aus. Wenn Sie verschiedene Aktionen benötigen, z. B. **Beleg neu erstellt**, **Beleg stornieren** oder **Genehmigung erhalten**, können Sie sie ausführen.

## <a name="e-documents-in-purchases"></a>E-Belege im Einkauf

Der Eingang elektronischer Einkaufsrechnungen in Dynamics 365 Business Central kann als Stapelverarbeitung oder manuell durchgeführt werden.

### <a name="run-the-batch-job"></a>Stapelverarbeitung ausführen

> [!NOTE]
> Diese Stapelverarbeitung dient der automatisierten Erfassung Ihrer eingehenden Rechnungen. Sie funktioniert nur in einem Land oder einer Region, in der die Funktionalität vorhanden ist.

Jedes Mal, wenn eine Aufgabenwarteschlange ausgeführt wird und der externe Dienst über eingehende Rechnungen verfügt, die von Ihrem Kreditor gesendet wurden, sammelt und importiert das System diese Rechnungen. Gehen Sie wie folgt vor, um den Vorgang abzuschließen.

1. Nachdem die Ausführung der Stapelverarbeitung abgeschlossen ist, werden die neu importierten Rechnungen zusammen mit ihren grundlegenden detaillierten Informationen auf der Seite **E-Beleg** aufgelistet.
2. Um weitere Details anzuzeigen, öffnen Sie einen bestimmten E-Beleg.
3. Wenn im E-Beleg und seiner Zuordnung keine Fehler oder Probleme aufgetreten sind, wird im Feld **Datensatz** die Belegnummer der Einkaufsrechnung angezeigt, die das System automatisch erstellt hat. Wählen Sie den Link aus, um den Beleg zu öffnen. Dieser vom System erstellte Beleg ist nicht der gebuchte Beleg.
4. Um direkt zum Einkaufsbeleg zu gelangen, wählen Sie das Feld **Datensatz** aus. Nachdem Sie die Seite **Einkaufsrechnung** geöffnet haben, überprüfen Sie den Beleg. Wenn dann alles korrekt ist, buchen Sie den Beleg.
5. Wenn Sie den Einkaufsbeleg buchen, wird das Feld **Datensatz** auf dem **E-Beleg** von **Rechnung** auf **Einkaufsrechnung** aktualisiert und die Nummer des gebuchten Einkaufsbelegs ist verfügbar. Sie können die Nummer auswählen, um die gebuchte Einkaufsrechnung zu öffnen.

Details zu Protokollen sind die gleichen wie im Verkaufsprozess für E-Belege.

Da Fehler im Verkaufsprozess meist mit der Verfügbarkeit des Dienstes zusammenhängen, kann der eingehende Beleg mehrere Ursachen enthalten. Der häufigste Grund für einen Fehler ist, dass das System die Zeilen im E-Beleg, den Sie von Ihrem Kreditor erhalten haben, nicht erkennen kann. Daher können keine Zeilen in Ihre Einkaufsrechnung eingegeben werden.

Es gibt zwei häufige Fehler:

- Wenn Sie diese bestimmte Zeile aus Ihrer Kreditorenrechnung verwenden möchten, die direkt auf das Hauptbuchkonto (Sachkonto) gebucht wurde, müssen Sie den Wert **Zuordnungstext** korrekt konfiguriert haben. Um diesen Fehler zu umgehen, wenn Sie Sachkonten verwenden möchten, wählen Sie **Text zu Konto zuordnen** aus, um eine spezifische Zuordnung des Werts **Zuordnungstext** mit dem Wert **Sollkontonr.** zu erstellen, die Sie verwenden möchten.
- Wenn Sie den Lagerbestand verfolgen und Zeilen aus Ihrer Kreditorenrechnung zum Ausfüllen von Artikeln in Ihren Belegzeilen verwenden möchten, müssen Sie den Wert **Artikelreferenz-Nr.** korrekt konfiguriert haben. Um diesen Fehler zu umgehen, ordnen Sie den externen Artikel mithilfe der Artikelreferenzliste Ihren Artikelnummern zu. Weitere Informationen finden Sie unter [Artikelreferenzen verwenden](inventory-how-use-item-cross-refs.md).

Nachdem Sie die Fehler und Warnungen behoben haben, können Sie manuell festlegen, wann das System basierend auf Ihren Einstellungen eine Einkaufsrechnung erstellen soll, indem Sie **Beleg erstellen** auswählen.

### <a name="manually-import-invoices"></a>Rechnungen manuell importieren

Um externe E-Belege manuell zu importieren, gehen Sie wie folgt vor.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol aus. Geben Sie **E-Beleg – Dienst** ein und wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie auf der Seite **E-Beleg – Dienst** den aktiven Dienst aus. 
3. Wählen Sie **Eingang** und laden Sie die E-Beleg-Datei hoch, die Sie vom Kreditor erhalten haben.
4. Wenn eine Fehlermeldung auftritt, öffnen Sie den E-Beleg, um die Probleme zu beheben.
5. Wenn Sie mit der Behebung der Probleme fertig sind, wählen Sie in der Gruppe **Manuell importieren** die Option **Beleg erstellen** aus.
6. Nachdem der Beleg in Business Central erstellt wurde, können Sie ihn genauso anzeigen wie bei der Verwendung einer Stapelverarbeitung.

## <a name="overview-of-e-document-statuses"></a>Übersicht über die Status von E-Belegen

Um einen besseren Überblick über alle E-Belege im Unternehmen zu erhalten, können Sie das **Buchhalter**-Rollencenter auswählen, in dem die Status des E-Belegs vorhanden sind. Dort finden Sie E-Beleg-Aktivitäten mit folgenden Status:

- **Ausgehende E-Belege:**

    - Verarbeitet
    - In Bearbeitung
    - Fehler

- **Eingehende E-Belege:**

    - Verarbeitet
    - In Bearbeitung
    - Fehler

## <a name="see-also"></a>Siehe auch

[E-Belege in Business Central einrichten](finance-how-setup-edocuments.md)  
[E-Belege in Business Central erweitern](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Finanzmanagement](finance.md)  
[Verkäufe fakturieren](sales-how-invoice-sales.md)  
[Käufe mit Einkaufsrechnungen und Aufträgen erfassen](purchasing-how-record-purchases.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
