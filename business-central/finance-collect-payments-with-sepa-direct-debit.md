---
title: SEPA-Lastschrift in Business Central
description: Mit dem Einverständnis Ihres Debitors können Sie Zahlungen nach dem SEPA-Format direkt vom Bankkonto des Debitors einziehen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.form: '371, 423, 424, 427, 1208, 1207, 1230'
ms.date: 07/17/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="collect-payments-with-sepa-direct-debit"></a>Zahlungen per SEPA-Lastschrift einziehen

Mit dem Einverständnis Ihres Debitors können Sie Zahlungen nach dem SEPA-Format direkt vom Bankkonto des Debitors einziehen.  

Richten Sie zuerst das Exportformat der Bankdatei ein, die Ihrer Bank aufträgt, eine Lastschrift durchführen. Dann richten Sie die Zahlungsmethode des Debitors ein. Richten Sie schließlich das Lastschrift-Mandat ein, die Ihrer Übereinkunft mit dem Kunden zum Einzug seiner Zahlungen in einem bestimmten Zeitraum entspricht.  

Um die Bank anzuweisen, den Zahlungsbetrag vom Bankkonto des Debitors auf das Konto Ihres Unternehmens zu überweisen, erstellen Sie eine Lastschrifteinzugsbuchung, die Informationen über Bankkonten, die betroffenen Verkaufsrechnungen und die Lastschriftanweisung enthält. Anschließend exportieren Sie eine XML-Datei, die auf dem Einzugseintrag basiert, und senden Sie zur Verarbeitung an Ihre Bank. Über etwaige nicht verbuchte Zahlungen wirst Du durch Deine Bank informiert und musst die entsprechenden Lastschrifteinzüge dann manuell ablehnen.  

Sie können Standarddebitorverkaufscodes mit Informationen zum Lastschrifteinzug und zu Einzugsermächtigungen einrichten. Anschließend können Sie mit der **Standard-Debitorenrechnung erstellen**-Stapelverarbeitung mehrere Verkaufsrechnungen erstellen, die bereits vorab die Einzugsinformationen enthalten. Dies kann manuell oder automatisch durchgeführt werden, je nach dem Zahlungsfälligkeitsdatum.  

Wenn die Zahlungen wie von Ihrer Bank mitgeteilt erfolgreich verarbeitet wurden, können Sie die Zahlungseingänge entweder direkt von der Seite  **Lastschrifteinzugseinträge**  aus buchen oder indem Sie die Zahlungszeilen in das Journal verschieben, in dem Sie Zahlungseingänge buchen, z. B. auf die Seite  **Barzahlungseingangsjournale** . Je nach Ihrem Cash-Management-Prozess können Sie auch warten und die Zahlungen lediglich als Teil der Bankabstimmung anwenden.  

> [!NOTE]  
> Um Zahlungen mithilfe von SEPA-Lastschrift zu erfassen, muss die Währung der Verkaufsrechnung EURO sein.  

## <a name="how-to-set-up-sepa-direct-debit"></a>So richten Sie das SEPA-Lastschriftverfahren ein

Von der Seite **Lastschrifteinzüge** aus können Sie Anweisungen an Ihre elektronische Bank exportieren, um einen Lastschrifteinzug vom Bankkonto des Debitors auf Ihr Bankkonto gemäss dem SEPA-Lastschriftformat durchzuführen.

> [!NOTE]
> Die globale Version von [!INCLUDE[prod_short](includes/prod_short.md)] unterstützt nur das SEPA-Lastschriftformat. Die Version für Ihr Land/Ihre Region unterstützt möglicherweise andere Formate für die elektronische Zahlung. Siehe unter **Lokale Funktionalität** im Inhaltsverzeichnis.  

Um den Export eines Bankdateiformats zu ermöglichen, das in  [!INCLUDE[prod_short](includes/prod_short.md)] nicht standardmäßig unterstützt wird, können Sie mithilfe des Datenaustauschframeworks eine Datenaustauschdefinition einrichten. Für weitere Informationen, siehe [Einrichten der Datenaustauschdefinition](across-how-to-set-up-data-exchange-definitions.md).  

Bevor Sie Debitorenzahlungen elektronisch durch den Export von Lastschriften im SEPA-Lastschriftformat verarbeiten können, müssen Sie die folgenden Einrichtungsschritte ausführen:  

* Richten Sie das Exportformat der Bankdatei ein, mit der Ihre Bank angewiesen wird, einen Bankeinzug vom Bankkonto des Debitors auf Ihr Bankkonto durchzuführen.  
* Richten Sie die Zahlungsmethode des Debitors ein.  
* Richten Sie das Lastschriftmandat ein, das Ihrer Übereinkunft mit dem Debitor zum Einzug seiner Zahlungen in einem bestimmten Zeitraum entspricht.  

### <a name="to-set-up-your-bank-account-for-sepa-direct-debit"></a>So richten Sie Ihr Bankkonto für das SEPA-Lastschriftverfahren ein

1. Wählen Sie das ![Glühbirne, die das „Sie wünschen ...“-Feature öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Bankkonten** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie das Konto, das Sie für das Lastschriftverfahren verwenden möchten.  
3. Wählen Sie auf der Registerkarte  **Allgemeines**  im Feld  **SEPA-Lastschrift-Ablaufformat**  die Option für SEPA-Lastschrift aus.  

### <a name="to-set-up-the-customers-payment-method-for-sepa-direct-debit"></a>So richten Sie die Zahlungsmethode des Debitors für das SEPA-Lastschriftverfahren ein

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Zahlungsformen** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu**.  
3. Richten Sie eine Zahlungsform ein. Füllen Sie die auf den Lastschrifteinzug\-spezifischen Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Lastschrift**|Geben Sie an, ob die Zahlungsmethode für den SEPA-Lastschrifteinzug vorgesehen ist.|  
    |**Zahlungsbedingungscode Lastschrift**|Geben Sie die Zahlungsbedingungen (z. B. „NICHT ZAHLEN“) an, die auf Verkaufsrechnungen angezeigt werden, die mit SEPA-Lastschrift bezahlt werden, um dem Kunden mitzuteilen, dass die Zahlung automatisch eingezogen wird. Als Alternative können Sie das Feld leer lassen.|  

    > [!NOTE]  
    >  Geben Sie hier keinen Wert in **Bal. Kontonr.** ein  

4. Wählen Sie die Schaltfläche **OK** aus, um die Seite **Zahlungsformen** zu schließen.  
5. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Debitor** ein und wählen Sie dann den entsprechenden Link.  
6. Öffnen Sie den Kunden Karte für den Kunden, den Sie für den SEPA-Lastschrifteinzug einrichten möchten.  
7. Wählen Sie das Feld , und wählen Sie dann den **Zahlungsformcode**, den Sie in Schritt 3 angegeben haben.  
8. Wiederholen Sie die Schritte 6 und 7 für alle Kunden, die Sie für den SEPA-Lastschrifteinzug einrichten möchten.  

#### <a name="to-set-up-the-direct-debit-mandate-that-represents-the-customer-agreement"></a>Einrichten des Lastschrift-Mandats, entsprechend der Vereinbarung mit dem Debitor

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Debitor** ein und wählen Sie dann den entsprechenden Link.  
2. Öffnen Sie Karte für den Kunden, den Sie für SEPA-Lastschriften einrichten möchten.  
3. Wählen Sie die **Bankkonten** Aktion aus.  
4. Auswählen Sie auf der Seite  **Kundenbankkontoliste**  das Kundenbankkonto, das Lastschriften nutzen soll, und wählen Sie dann die Aktion  **Lastschriftmandate**  unter  **Neu** aus.  
5. Füllen Sie auf der Seite **SEPA-Felder** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Debitor Bankkontocode**|Gibt das Bankkonto an, aus dem Lastschrifteinzüge\-direkt abgebucht werden. Dieses Feld wird automatisch ausgefüllt.|  
    |**Gültig ab**|Geben Sie das Datum an, an dem das Lastschrift\-Mandat beginnt.|  
    |**Gültig bis**|Geben Sie das Datum an, an dem das Lastschrift\-Mandat endet.|  
    |**Datum der Unterschrift**|Geben Sie das Datum an, an dem der Kunde das Lastschrift\-Mandat unterzeichnet hat.|  
    |**Zahlungsart**|Geben Sie an, ob die Übereinkunft mehrere (**Wiederkehrende**) oder einen einzelnen (**Einmalig**) Lastschrifteinzug abdeckt.|  
    |**Erwartete Anzahl Sollbeträge**|Geben Sie an, wie viele Lastschrifteinzüge Sie zu tätigen erwarten. Dieses Feld ist nur relevant, wenn Sie **Wiederkehrend** im Feld **Sequenzart** ausgewählt haben.|  
    |**Sollzähler**|Gibt an, wie viele Lastschrift-Einzüge mit diesem Lastschrift\-Mandat durchgeführt wurden. Dieses Feld wird automatisch aktualisiert.|  
    |**Gesperrt**|Geben Sie an, dass mit diesem Lastschriftmandat keine Lastschrifteinzüge durchgeführt werden können.\-|  

6. Wiederholen Sie die Schritte 1 bis 5 für alle Kunden, die Sie für SEPA-Lastschriften einrichten möchten.  

 Das Lastschrift-Mandat wird automatisch in das Feld **Lastschrift-Mandat-ID** eingegeben, wenn Sie eine Verkaufsrechnung für den Debitor erstellen, den Sie in Schritt 2 ausgewählt haben. Weitere Informationen finden Sie unter [Erstellen Sie wiederkehrende Verkaufs- und Einkaufszeilen](sales-how-work-standard-lines.md).

## <a name="creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file"></a>SEPA-Lastschrifteinzugsposten erstellen und in eine Bankdatei exportieren

Um die Bank anzuweisen, den Zahlungsbetrag vom Bankkonto des Debitors auf das Konto Ihres Unternehmens zu überweisen, erstellen Sie eine Lastschrifteinzugsbuchung, die Informationen über das Bankkonto des Debitors, die betroffenen Verkaufsrechnungen und die Einzugsermächtigung enthält. Aus dem resultierenden Lastschrifteinzugsposten können Sie dann eine XML-Datei exportieren, die Sie dann zur Verarbeitung an Ihre elektronische Bank senden oder hochladen. Konnten Zahlungen von der Bank nicht verarbeitet werden, werden Sie von Ihrer Bank darüber informiert und müssen den entsprechenden Lastschrifteinzug manuell ablehnen.  

 > [!NOTE]  
 > Um Zahlungen mithilfe von SEPA-Lastschrift zu erfassen, muss die Währung der Verkaufsrechnung EURO sein.  

### <a name="to-create-a-direct-debit-collection"></a>Erstellen eines Lastschrifteinzugs

 1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Lastschriften-Sammlungen** ein, und wählen Sie dann den entsprechenden Link.  
 2. Wählen Sie auf der Seite **Lastschrifteneinzug** die Aktion **Lastschrift anlegen**.  
 3. Füllen Sie auf der Seite **Lastschrift erstellen** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Ab Fälligkeitsdatum**|Geben Sie das früheste Zahlungsfälligkeitsdatum auf Verkaufsrechnungen an, für das Sie einen Lastschrifteinzug erstellen wollen.|  
    |**Bis Fälligkeitsdatum**|Geben Sie das späteste Zahlungsfälligkeitsdatum auf Verkaufsrechnungen an, für das Sie einen Lastschrifteinzug erstellen wollen.|  
    |**Partnerart**|Geben Sie an, ob der Lastschrifteinzug für Debitoren des Typs **Unternehmen** oder **Person** erfolgt.|  
    |**Nur Debitoren mit gültiger Einzugsermächtigung**|Geben Sie an, ob ein Lastschrifteinzug für Debitoren erstellt wird, die über ein gültiges Lastschrift-Mandat verfügen. **Hinweis:**  Ein Lastschrifteinzug wird erstellt, auch wenn das Feld  **Lastschriftmandats-ID**  auf der Verkaufsrechnung nicht ausgefüllt ist.|  
    |**Nur Rechnungen mit gültigem Lastschrift-Mandat**|Legt fest, ob ein Lastschrifteinzug nur dann für Verkaufsrechnungen erstellt wird, wenn im Feld **Lastschrift-Mandat-ID** auf der Verkaufsrechnung ein gültiges Lastschrift-Mandat ausgewählt ist.|  
    |**Bankkontonr.**|Geben Sie an, auf welches der Bankkonten Ihres Unternehmens die eingezogene Zahlung vom Bankkonto des Debitors überwiesen werden soll.|  
    |**Bankkontoname**|Gibt den Namen des Bankkontos an, das Sie im Feld **Bankkontonr.** auswählen. Dieses Feld wird automatisch ausgefüllt.|  

 4. Wählen Sie die Schaltfläche **OK** aus.  

Eine Einzugserfassung wird der **Lastschrift**-Seite hinzugefügt, und ein oder mehrere Lastschrifteinzugsposten werden erstellt.  

### <a name="to-export-a-direct-debit-collection-entry-to-a-bank-file"></a>Export eines Lastschrifteinzugpostens in eine Bankdatei

 1. Wählen Sie auf der Seite **Direktinkasso** die Option **Direktinkasso. Einträge** Aktion.  
 2. Auf der Seite **Direct Debit Inkasso. Einträge**, wählen Sie den Eintrag, den Sie exportieren möchten, und wählen Sie dann die Aktion **Lastschriftdatei erstellen**.  
 3. Speichern Sie die Exportdatei an dem Speicherort, von dem aus Sie sie an Ihre elektronische Bank senden oder hochladen.  

      auf der Seite **Lastschrifteinzug-Eintrag** wird das Feld **Status Lastschrift** zur erstellten Datei geändert. auf der Seite **SEPA-Lastschrift-Mandate** wird das Feld **Sollzähler** mit einer Anzahl aktualisiert.  

 Kann die exportierte Datei nicht verarbeitet werden, beispielsweise weil der Kunde insolvent ist, können Sie die Lastschrifteinzugsbuchung ablehnen. Wenn die exportierte Datei von der Bank erfolgreich verarbeitet wird, werden die fälligen Zahlungen der beteiligten Verkaufsrechnungen von den beteiligten Debitoren automatisch eingezogen. In diesem Fall können Sie die Erfassung schließen.  

### <a name="to-reject-a-direct-debit-collection-entry"></a>Ablehnen eines Lastschrifteinzugpostens

* Markieren Sie auf der Seite  **Lastschrifteinzüge**  den Eintrag, der nicht erfolgreich verarbeitet wurde, und wählen Sie dann die Aktion  **Eintrag ablehnen** .  

    Der Wert im Feld **Status** auf der Seite **Lastschrifteinzug-Eintrag** wird auf **zurückgewiesen** geändert.  

### <a name="to-close-a-direct-debit-collection"></a>Schließen eines Lastschrifteinzugs

* Auf der Seite **Lastschrifteinzug-Eintrag** Seite, wählen Sie den Eintrag, der erfolgreich bearbeitet wurde, und wählen Sie dann die Aktion **Sammlung schließen**.  

    Der zugehörige Lastschrifteinzug wird geschlossen.  

 Sie können jetzt Zahlungseingänge für die betreffenden Verkaufsrechnungen buchen. Sie können dies tun, wie Sie normalerweise Zahlungseingänge buchen, etwa auf der Seite **Zahlungserfassung** oder Sie können die zugehörigen Zahlungseingänge direkt aus dem Fenster **Lastschrifteinzug-Eintrag** buchen. Weitere Informationen finden Sie unter [Einziehen von Zahlungen mit Abbuchung SEPA](finance-collect-payments-with-sepa-direct-debit.md).

## <a name="posting-sepa-direct-debit-payment-receipts"></a>SEPA-Lastschrifteinzug-Zahlungseingänge buchen

Wenn ein Lastschrifteinzug von Ihrer Bank erfolgreich verarbeitet wird, können Sie den Eingang der Zahlungen für die betreffenden Verkaufsrechnungen buchen. Weitere Informationen finden Sie unter [SEPA-Lastschrifteinzugsposten erstellen und in eine Bankdatei exportieren](finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file)  

Sie können der Zahlungseingang direkt aus dem **Lastschriften** oder im **Direct Debit Collect. Posten** buchen. Sie können auch die Arbeit an einen anderen Benutzer übertragen, indem Sie die zugehörigen Buch.-Blattzeilen vorbereiten.  

### <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-page"></a>Buchen eines Lastschrifteingangs aus der Lastschrift-Einzugsseite

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Lastschriften-Sammlungen** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie eine Zeile für die Lastschrift-Einzugserfassung, die in eine Bankdatei exportiert und von der Bank erfolgreich verarbeitet wurde.
3. Wählen Sie die Aktion **Zahlungseingang buchen** aus.  
4. Füllen Sie auf der Seite **Lastschrift buchen** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Lastschriftnr.**|Geben Sie den Lastschrifteinzug an, für den Sie den Zahlungseingang buchen wollen.|  
    |**Fibu Buch.-Blattvorlage**|Geben Sie an, welche Fibu Buch.-Blattvorlage zum Buchen des Zahlungseingangs verwendet werden soll, etwa die Vorlage für Bareingänge.|  
    |**Fibu Buch.-Blattname**|Geben Sie an, welcher Fibu Buch.-Blattname für die Buchung des Zahlungseingangs verwendet werden soll.|  
    |**Nur Buch.-Blatt erstellen**|Auswählen Aktivieren Sie dieses Kontrollkästchen, wenn Sie den Zahlungsbeleg nicht buchen möchten, wenn Sie die Schaltfläche  **OK**  auswählen. Der Zahlungsbeleg wird im angegebenen Journal vorbereitet und erst gebucht, wenn jemand die betreffenden Journalzeilen bucht.|  

5. Wählen Sie die Schaltfläche **OK**.

## <a name="see-also"></a>Siehe auch

[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Serviceverwaltung](service-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
