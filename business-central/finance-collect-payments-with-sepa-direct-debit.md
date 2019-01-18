---
title: SEPA Direkbelastung in Business Central | Microsoft Docs
description: "Mit Zustimmung Ihres Kunden können Sie Zahlungen direkt vom Bankkonto des Kunden gemäß dem SEPA-Format einziehen."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/15/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: c732702808f807396702cef9ef0a1a22354ead15
ms.contentlocale: de-de
ms.lasthandoff: 11/26/2018

---
# <a name="collecting-payments-with-sepa-direct-debit"></a>Einziehen von Zahlungen per Lastschriftverfahren SEPA
Mit Zustimmung Ihres Kunden können Sie Zahlungen direkt vom Bankkonto des Kunden gemäß dem SEPA-Format einziehen.  

 Richten Sie zuerst das Exportformat der Bankdatei ein, die Ihrer Bank aufträgt, eine Lastschrift durchführen. Richten Sie dann die Zahlungsmethode des Debitors ein. Richten Sie schließlich das Lastschrift-Mandat ein, die Ihrer Übereinkunft mit dem Kunden zum Einzug seiner Zahlungen in einem bestimmten Zeitraum entspricht.  

 Um die Bank anzuweisen, den Zahlungsbetrag vom Bankkonto des Debitors auf das Bankkonto Ihres Unternehmens zu überweisen, erstellen Sie einen Lastschrifteinzugposten mit Informationen zu Bankkonten, den betroffenen Verkaufsrechnungen und dem Lastschrift-Mandat. Anschließend exportieren Sie eine XML-Datei, die auf dem Einzugseintrag basiert, und senden Sie zur Verarbeitung an Ihre Bank. Alle Zahlungen, die nicht verarbeitet werden konnten, werden Ihnen von Ihrer Bank mitgeteilt, und Sie müssen dann die jeweiligen Lastschrifteinzugsposten manuell ablehnen.  

 Sie können Standarddebitorverkaufscodes mit Informationen zum Lastschrifteinzug und zu Einzugsermächtigungen einrichten. Anschließend können Sie mit der **Standard-Debitorenrechnung erstellen**-Stapelverarbeitung mehrere Verkaufsrechnungen erstellen, die bereits vorab die Einzugsinformationen enthalten. Dies kann manuell oder automatisch durchgeführt werden, je nach dem Zahlungsfälligkeitsdatum.  

 Wenn Ihre Bank Ihnen mitteilt, dass Zahlungen erfolgreich verarbeitet wurden, können Sie die Zahlungseingänge direkt aus der Seite **Lastschriftenposten** buchen, oder indem Sie die Zahlungszeilen in das Buch verschieben, in dem Sie Zahlungseingänge buchen, etwa das Fenster **Zahlungseingangs Buch.-Blatt**. Je nach Ihrem Cash-Management-Prozess können Sie auch warten und die Zahlungen lediglich als Teil der Bankabstimmung anwenden.  

> [!NOTE]  
>  Um Zahlungen mithilfe von SEPA-Lastschrift zu erfassen, muss die Währung der Verkaufsrechnung EURO sein.  

## <a name="setting-up-sepa-direct-debit"></a>Einrichten von SEPA-Lastschriften
Auf der Seite **Lastschriften** können Sie Anweisungen in Ihre elektronische Bank exportieren, um eine Lastschrift vom Bankkonto des Debitors auf Ihr Bankkonto durchzuführen. [!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt das Abbuchungsformat SEPA, aber in Ihrem Land/die Region, sind möglicherweise andere Formate für den elektronischen Zahlungsverkehr verfügbar.  

Um das Exportieren von Bankdateiformaten zu aktivieren, die nicht durch die allgemeine oder lokale Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt werden, können Sie eine Datenaustauschdefinition einrichten, indem Sie das Datenaustauschframework verwenden. Für weitere Informationen, siehe [Einrichten der Datenaustauschdefinition](across-how-to-set-up-data-exchange-definitions.md).  

Bevor Sie Debitorenzahlungen elektronisch durch den Export von Lastschriften im SEPA-Lastschriftformat verarbeiten können, müssen Sie die folgenden Einrichtungsschritte ausführen:  

* Richten Sie zunächst das Exportformat der Bankdatei ein, wodurch Ihre Bank beauftragt wird, eine Lastschrift vom Bankkonto des Debitors auf Ihr Bankkonto durchzuführen.  
* Richten Sie die Zahlungsmethode des Debitors ein.  
* Richten Sie das Lastschriftmandat ein, das Ihrer Übereinkunft mit dem Debitor zum Einzug seiner Zahlungen in einem bestimmten Zeitraum entspricht.  

### <a name="to-set-up-your-bank-account-for-sepa-direct-debit"></a>Einrichten Ihres Bankkontos für die SEPA-Lastschrift  
1. Geben Sie im Feld **Suchen** **Bankkonten** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Öffnen Sie das Konto, das Sie für das Lastschriftverfahren verwenden möchten.  
3. Wählen Sie im Inforegister **Umlagerung**, im Feld **SEPA-Lastschrift Exportformat** SEPA Lastschrift.  

### <a name="to-set-up-the-customers-payment-method-for-sepa-direct-debit"></a>Einrichten der Zahlungsmethode des Debitors für die SEPA-Lastschrift  
1. Geben Sie im Feld **Suchen** einen Wert für **Zahlungsformen** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Neu** aus.  
3. Richten Sie eine Zahlungsmethode ein. Füllen Sie die auf den Lastschrifteinzug bezüglichen Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Lastschrift**|Geben Sie an, ob die Zahlungsmethode für den SEPA-Lastschrifteinzug gilt.|  
    |**Zahlungsbedingungscode Lastschrift**|Geben Sie die Zahlungsbedingungen an, wie etwa NICHT ZAHLEN, die auf Verkaufsrechnungen angezeigt werden, die per SEPA-Lastschrift bezahlt werden, um den Debitor darauf hinzuweisen, dass die Zahlung automatisch eingezogen wird. Als Alternative können Sie das Feld leer lassen.|  

    > [!NOTE]  
    >  Geben Sie hier keinen Wert in **Bal. Kontonr.** ein  

4. Wählen Sie die Schaltfläche **OK** aus, um die Seite **Genehmigungskommentare** zu schließen.  
5. Geben Sie im Feld **Suchen** **Debitoren** ein, und wählen Sie dann den zugehörigen Link aus.  
6. Öffnen Sie die Debitorenkarte für den Debitor, der für die SEPA-Lastschriften eingerichtet werden soll.  
7. Wählen Sie das Feld , und wählen Sie dann den **Zahlungsformcode**, den Sie in Schritt 3 angegeben haben.  
8. Wiederholen Sie die Schritte 6 und 7 für alle Debitoren, die Sie für SEPA-Lastschriften einrichten wollen.  

#### <a name="to-set-up-the-direct-debit-mandate-that-represents-the-customer-agreement"></a>Einrichten des Lastschrift-Mandats, entsprechend der Vereinbarung mit dem Debitor  
1. Geben Sie im Feld **Suchen** **Debitoren** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Öffnen Sie die Karte für den Debitor, der für die SEPA-Lastschriften eingerichtet werden soll.  
3. Wählen Sie die **Bankkonten** Aktion aus.  
4. Wählen Sie auf der Seite **Debitor-Bankkontenübersicht** das Debitorenbankkonto, das Lastschriften verwenden wird, und wählen Sie dann auf der Registerkarte **Start**, in der Gruppe **Prozess**, **Lastschrift-Mandat**.  
5. Füllen Sie auf der Seite **SEPA-Felder** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Debitor Bankkontocode**|Gibt das Bankkonto an, aus dem Lastschrifteinzüge abgebucht werden. Dieses Feld wird automatisch ausgefüllt.|  
    |**Gültig ab**|Geben Sie das Datum an, an dem das Lastschrift-Mandat beginnt.|  
    |**Gültig bis**|Geben Sie das Datum an, an dem das Lastschrift-Mandat endet.|  
    |**Datum der Unterschrift**|Geben Sie das Datum an, an dem der Kunde das Lastschrift-Mandat unterzeichnet hat.|  
    |**Zahlungstyp**|Geben Sie an, ob die Übereinkunft mehrere (**Wiederkehrende**) oder einen einzelnen (**Einmalig**) Lastschrifteinzug abdeckt.|  
    |**Erwartete Anzahl Sollbeträge**|Geben Sie an, wie viele Lastschrifteinzüge Sie zu tätigen erwarten. Dieses Feld ist nur relevant, wenn Sie **Wiederkehrend** im Feld **Sequenzart** ausgewählt haben.|  
    |**Sollzähler**|Gibt an, wie viele Lastschrift-Einzüge mit diesem Lastschrift-Mandat durchgeführt wurden. Dieses Feld wird automatisch aktualisiert.|  
    |**Gesperrt**|Geben Sie an, dass Lastschrifteinzüge mit diesem Lastschrift-Mandat nicht durchgeführt werden können.|  

6.  Wiederholen Sie die Schritte 1 bis 5 für alle Debitoren, die für die SEPA-Lastschriften eingerichtet werden sollen.  

 Das Lastschrift-Mandat wird automatisch in das Feld **Lastschrift-Mandat-ID** eingegeben, wenn Sie eine Verkaufsrechnung für den Debitor erstellen, den Sie in Schritt 2 ausgewählt haben. Weitere Informationen finden Sie unter [Erstellen Sie wiederkehrende Verkaufs- und Einkaufszeilen](sales-how-work-standard-lines.md).

## <a name="creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file"></a>SEPA-Lastschrifteinzugsposten erstellen und in eine Bankdatei exportieren
 Um die Bank anzuweisen, den Zahlungsbetrag vom Bankkonto des Debitors auf das Bankkonto Ihres Unternehmens zu überweisen, erstellen Sie einen Lastschrifteinzug mit Informationen zum Bankkonto des Debitors, den betroffenen Verkaufsrechnungen und dem Lastschrift-Mandat. Aus dem resultierenden Lastschrifteinzugsposten können Sie dann eine XML-Datei exportieren, die Sie dann zur Verarbeitung an Ihre elektronische Bank senden oder hochladen. Alle Zahlungen, die von der Bank nicht verarbeitet werden konnten, werden Ihnen von Ihrer Bank mitgeteilt, und Sie müssen dann die jeweiligen Lastschrifteinzugsposten manuell ablehnen.  

 > [!NOTE]  
 >  Um Zahlungen mithilfe von SEPA-Lastschrift zu erfassen, muss die Währung der Verkaufsrechnung EURO sein.  

### <a name="to-create-a-direct-debit-collection"></a>Erstellen eines Lastschrifteinzugs  

 1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Lastschriften** ein, und wählen dann den zugehörigen Link aus.  
 2. Wählen Sie auf der Seite **Lastschriften** auf der Registerkarte **Start** in der Gruppe **Neu** die Option **Lastschrifteinzug erstellen** aus.  
 3. Füllen Sie auf der Seite **Lastschrift erstellen** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

     |Feld|Beschreibung|  
     |---------------------------------|---------------------------------------|  
     |**Ab Fälligkeitsdatum**|Geben Sie das früheste Zahlungsfälligkeitsdatum auf Verkaufsrechnungen an, für das Sie einen Lastschrifteinzug erstellen wollen.|  
     |**Bis Fälligkeitsdatum**|Geben Sie das späteste Zahlungsfälligkeitsdatum auf Verkaufsrechnungen an, für das Sie einen Lastschrifteinzug erstellen wollen.|  
     |**Partnerart**|Geben Sie an, ob der Lastschrifteinzug für Debitoren des Typs **Unternehmen** oder **Person** erfolgt.|  
     |**Nur Debitoren mit gültiger Einzugsermächtigung**|Geben Sie an, ob ein Lastschrifteinzug für Debitoren erstellt wird, die über ein gültiges Lastschrift-Mandat verfügen. **Hinweis:** Eine Lastschrift wird auch erstellt, wenn das Feld **Lastschrift-Unternehmens-ID** auf der Vertriebsrechnung nicht ausgefüllt ist.|  
     |**Nur Rechnungen mit gültigem Lastschrift-Mandat**|Legt fest, ob ein Lastschrifteinzug nur dann für Verkaufsrechnungen erstellt wird, wenn im Feld **Lastschrift-Mandat-ID** auf der Verkaufsrechnung ein gültiges Lastschrift-Mandat ausgewählt ist.|  
     |**Bankkontonr.**|Geben Sie an, auf welches der Bankkonten Ihres Unternehmens die Eingangszahlung vom Bankkonto des Debitors überwiesen werden soll.|  
     |**Bankkontoname**|Gibt den Namen des Bankkontos an, das Sie im Feld **Bankkontonr.** auswählen. Dieses Feld wird automatisch ausgefüllt.|  

 4. Wählen Sie die Schaltfläche **OK** aus.  

      Eine Einzugserfassung wird der **Lastschrift**-Seite hinzugefügt, und ein oder mehrere Lastschrifteinzugsposten werden erstellt.  

### <a name="to-export-a-direct-debit-collection-entry-to-a-bank-file"></a>Export eines Lastschrifteinzugpostens in eine Bankdatei  
 1. Wählen Sie auf der Seite **Lastschriften** auf der Registerkarte **Start** in der Gruppe **Verarbeiten** die Option **Lastschrifteinzug-Eintrag erstellen** aus.  
 2. Wählen Sie auf der Seite **Lastschrifteinzug-Eintrag** den Eintrag aus, den Sie exportieren möchten, und wählen Sie dann auf der Registerkarte **Start**, in der Gruppe **Verarbeiten**, **Lastschrift erstellen** aus.  
 3. Speichern Sie die Exportdatei an dem Speicherort, von dem aus Sie sie an Ihre elektronische Bank senden oder hochladen.  

      auf der Seite **Lastschrifteinzug-Eintrag** wird das Feld **Status Lastschrift** zur erstellten Datei geändert. auf der Seite **SEPA-Lastschrift-Mandate** wird das Feld **Sollzähler** mit einer Anzahl aktualisiert.  

 Wenn die exportierte Datei nicht verarbeitet werden kann, etwa weil der Debitor nicht mehr zahlungsfähig ist, können Sie den Lastschrifteinzugsposten ablehnen. Wenn die exportierte Datei von der Bank erfolgreich verarbeitet wird, werden die fälligen Zahlungen der beteiligten Verkaufsrechnungen von den beteiligten Debitoren automatisch eingezogen. In diesem Fall können Sie die Erfassung schließen.  

### <a name="to-reject-a-direct-debit-collection-entry"></a>Ablehnen eines Lastschrifteinzugpostens  

 * Wählen Sie auf der Seite **Lastschrifteinzug-Eintrag** den Eintrag aus, der nicht erfolgreich verarbeitet wurde, und wählen Sie dann auf der Registerkarte **Start**, in der Gruppe **Verarbeiten**, **Eintrag ablehnen** aus.  

      Der Wert im Feld **Status** auf der Seite **Lastschrifteinzug-Eintrag** wird auf **zurückgewiesen** geändert.  

### <a name="to-close-a-direct-debit-collection"></a>Schließen eines Lastschrifteinzugs  
 *  Wählen Sie auf der Seite **Lastschrifteinzug-Eintrag** den Eintrag aus, der nicht erfolgreich verarbeitet wurde, und wählen Sie dann auf der Registerkarte **Start**, in der Gruppe **Verarbeiten**, **Lastschrift beenden** aus.  

      Der zugehörige Lastschrifteinzug wird geschlossen.  

 Sie können jetzt Zahlungseingänge für die betreffenden Verkaufsrechnungen buchen. Sie können dies tun, wie Sie normalerweise Zahlungseingänge buchen, etwa auf der Seite **Zahlungserfassung** oder Sie können die zugehörigen Zahlungseingänge direkt aus dem Fenster **Lastschrifteinzug-Eintrag** buchen. Weitere Informationen finden Sie unter [SEPA-Lastschrifteinzug-Zahlungseingänge buchen](finance-how-to-post-sepa-direct-debit-payment-receipts.md).

## <a name="posting-sepa-direct-debit-payment-receipts"></a>SEPA-Lastschrifteinzug-Zahlungseingänge buchen
 Wenn ein Lastschrifteinzug von Ihrer Bank erfolgreich verarbeitet wird, können Sie den Eingang der Zahlungen für die betreffenden Verkaufsrechnungen buchen. Weitere Informationen finden Sie unter [SEPA-Lastschrifteinzugsposten erstellen und in eine Bankdatei exportieren](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)  

 Sie können der Zahlungseingang direkt aus dem **Lastschriften** oder im **Direct Debit Collect. Posten** buchen. Sie können auch die Arbeit an einen anderen Benutzer übertragen, indem Sie die zugehörigen Buch.-Blattzeilen vorbereiten.  

### <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-page"></a>Buchen eines Lastschrifteingangs aus der Lastschrift-Einzugsseite  
 1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren?“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Lastschriften** ein, und wählen dann den zugehörigen Link aus.  
 2. Wählen Sie eine Zeile für die Lastschrift-Einzugserfassung, die in eine Bankdatei exportiert und von der Bank erfolgreich verarbeitet wurde. Weitere Informationen finden Sie unter [SEPA-Lastschrifteinzugsposten erstellen und in eine Bankdatei exportieren](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)  
 3. Wählen Sie die Aktion **Zahlungseingang buchen** aus.  
 4. Füllen Sie auf der Seite **Lastschrift buchen** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

     |Feld|Beschreibung|  
     |---------------------------------|---------------------------------------|  
     |**Lastschriftnr.**|Geben Sie den Lastschrifteinzug an, für den Sie den Zahlungseingang buchen wollen.|  
     |**Fibu Buch.-Blattvorlage**|Geben Sie an, welche Fibu Buch.-Blattvorlage zum Buchen des Zahlungseingangs verwendet werden soll, etwa die Vorlage für Bareingänge.|  
     |**Fibu Buch.-Blattname**|Geben Sie an, welcher Fibu Buch.-Blattname für die Buchung des Zahlungseingangs verwendet werden soll.|  
     |**Nur Buch.-Blatt erstellen**|Markieren Sie dieses Kontrollkästchen, wenn Sie den Zahlungseingang nicht buchen wollen, wenn Sie die Schaltfläche **OK** wählen. Der Zahlungseingang wird in dem angegebenen Buch vorbereitet und erst gebucht, wenn jemand die fraglichen Buch.-Blatt-Zeilen bucht.|  

 5. Wählen Sie die Schaltfläche **OK** aus.

## <a name="see-also"></a>Siehe auch  
[Verwalten von Forderungen](receivables-manage-receivables.md)

