---
title: E-Belege im Verkauf verwenden
description: 'Erfahren Sie, wie Sie die E-Belege-Funktionalität im Zusammenhang mit Verkäufen verwenden.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, sales, deliver'
ms.search.form: '42, 43, 132, 6103, 6133, 6121, 9301, 9305'
ms.date: 04/10/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="use-e-documents-in-the-sales-process"></a>E-Belege im Verkaufsprozess verwenden

Sie können konfigurierte elektronische Belege (E-Belege) mit Verkaufsbelegen verwenden.

Sie können die folgenden Verkaufsbelegen mit der E-Belege-Funktionalität verwenden:  

- Verkaufsrechnungen
- Verkaufsaufträge
- Verkaufsgutschriften
- Servicerechnungen
- Servicegutschriften
- Zinsrechnungen
- Mahnungen

## <a name="e-documents-in-sales"></a>E-Belege im Verkauf

Um eine E-Rechnung zu erstellen und an einen Debitor zu senden, müssen Sie die Verkaufsrechnung erstellen und buchen. Weitere Informationen zum Standardprozess finden Sie unter [Fakturierung eines Verkaufs](sales-how-invoice-sales.md).

Nachdem Sie den Verkaufsbeleg gebucht haben, öffnen Sie die Seite **Gebuchte Verkaufsrechnungen**, um auf die zugehörige Seite **E-Belege** zuzugreifen.

### <a name="view-e-documents"></a>E-Belege aufrufen

Gehen Sie wie folgt vor, um vorhandene E-Belege anzuzeigen.

1. Wählen Sie auf der Seite **Gebuchte Verkaufsrechnungen** **E-Belege** und dann **E-Beleg öffnen**.
2. Auf der Seite **E-Belege** können Sie in der Kopfzeile grundlegende Informationen zur gebuchten Rechnung einsehen.
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

Wenn es ein Problem mit dem Dienstanbieter gibt und der Beleg nicht gesendet werden kann, achten Sie auf die folgenden Indikatoren auf der Seite **E-Belege**:

- Das Feld **Status des elektronischen Belegs** in der Kopfzeile zeigt den Status **Fehler**.
- Das Feld **Status des E-Belegs** auf dem Inforegister **E-Beleg – Dienststatus** zeigt den Status **Fehler beim Senden**.
- Das Inforegister **Fehler und Warnungen** enthält eine oder mehrere Meldungen, die die Ursache des Problems angeben.

Nachdem das Problem behoben ist, führen Sie die Aktionen **Beleg senden** manuell aus. Wenn Sie verschiedene Aktionen benötigen, z. B. **Beleg neu erstellt**, **Beleg stornieren** oder **Genehmigung erhalten**, können Sie sie ausführen.

## <a name="overview-of-e-document-statuses"></a>Übersicht über die Status von E-Belegen

Um einen besseren Überblick über alle E-Belege im Unternehmen zu erhalten, können Sie das **Buchhalter**-Rollencenter auswählen, in dem die Status des E-Belegs vorhanden sind. Dort finden Sie E-Beleg-Aktivitäten mit folgenden Status:

- **Ausgehende E-Belege:**

    - Verarbeitet
    - In Bearbeitung
    - Fehler


## <a name="see-also"></a>Siehe auch

[E-Belege in [!INCLUDE[prod_short](includes/prod_short.md)] einrichten](finance-how-setup-edocuments.md)    
[E-Belege im Einkauf verwenden](finance-how-use-edocuments-purchase.md)  
[E-Belege in [!INCLUDE[prod_short](includes/prod_short.md)] erweitern](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)    
[Finanzmanagement](finance.md)    
[Fakturieren eines Verkaufs](sales-how-invoice-sales.md)    
[Käufe mit Einkaufsrechnungen und Aufträgen erfassen](purchasing-how-record-purchases.md)    
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
