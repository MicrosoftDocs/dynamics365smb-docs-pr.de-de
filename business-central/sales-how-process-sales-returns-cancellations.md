---
title: Retouren oder Stornierungen verarbeiten
description: 'Hier wird beschrieben, wie Sie eine Verkaufsgutschrift erstellen, um eine Rückgabe, Stornierung oder Rückerstattung für Artikel oder Dienstleistungen zu verarbeiten, für die Sie eine Zahlung erhalten haben.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'undo, credit memo, return'
ms.search.form: '44, 134, 143, 6629, 6630, 6633, 6662, 9302, 9304, Report_6646'
ms.date: 02/26/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="process-sales-returns-or-cancellations"></a>Retouren oder Stornierungen verarbeiten

Wenn Ihr Debitor Artikel zurückschicken oder Dienstleistungen löschen will, die Sie verkauft haben, können Sie eine Einkaufsgutschrift erstellen und buchen, die die angeforderte Änderung im Hinblick auf die ursprünglichen Einkaufsrechnung angibt. Um die korrekten Informationen der Verkaufsrechnungen einzubeziehen, können Sie folgende Aufgaben ausführen:  

- Erzeugen Sie die Verkaufsgutschrift direkt aus der gebuchten Verkaufsrechnung.
- Erstellen Sie eine neue Verkaufsgutschrift mit kopierten Rechnungsinformationen.

Wenn Sie mehr Steuerelemente für den Rücklieferungsprozess benötigen, z.B. Lagerbelege für die Artikelabwicklung oder eine bessere Übersicht beim Empfang von Artikeln aus mehreren Verkaufsbelegen mit einer Rücklieferung, dann können Sie Verkaufsreklamationen erstellen. Eine Verkaufsreklamation löst automatisch die zugehörige Verkaufsgutschrift sowie andere Dokumente wie Verkaufsauftrag für Ersatzlieferungen aus, sofern erforderlich. Weitere Informationen finden Sie unter [Verkaufsretourenaufträge verarbeiten](sales-how-process-sales-returns-orders.md).

> [!NOTE]  
> Wenn eine gebuchte Verkaufsrechnung noch nicht bezahlt wurde, können Sie die Funktionen **Korrigieren** oder **Abbrechen** auf der gebuchten Verkaufsrechnung verwenden, um die entsprechenden Transaktionen automatisch zu stornieren. Diese Funktionen arbeiten nur für nicht geleistete Rechnungen, und sie unterstützen nicht Teil-Reklamationen oder Kündigungen. Weitere Informationen finden Sie unter [Ändern oder löschen von unbezahlten Verkaufsrechnungen](sales-how-correct-cancel-sales-invoice.md).

Eine Rücklieferungs- oder eine Vergütung kann sich nur auf einige der Artikel oder der Services in der ursprünglichen Verkaufsrechnung beziehen. In diesem Fall müssen Sie Informationen in den Zeilen der Verkaufsgutschrift oder der Verkaufsreklamation bearbeiten. Wenn Sie die Verkaufsgutschrift oder Verkaufsreklamationen buchen, werden die Verkaufsbelege, die von Änderungen betroffen sind rückgängig gemacht und eine Rückerstattung für den Debitor wird erstellt. Weitere Informationen finden Sie unter [Zahlungen durchführen](payables-make-payments.md).  

Die Gutschriftsbuchung stellt auch jegliche Artikel Zu-/Abschläge wieder her, die dem gebuchten Beleg zugewiesen wurden, sodass die Wertposten des Artikels wieder identisch sind, wie bevor der Artikel Zu-/Abschlag zugewiesen wurde.

> [!NOTE]
> Die Buchhaltungsaspekte von Retouren, wie z. B. die Zahlungen an Debitoren als Rückerstattung, wird als Buchhaltungsarbeit betrachtet und hier nicht beschrieben. Weitere Informationen finden Sie unter [Kreditoren verwalten](payables-manage-payables.md).

## <a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a>Erstellt eine neue Verkaufsgutschrift, um eine gebuchte Verkaufsrechnung zurückzusetzen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Gebuchte Verkaufsrechnungen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Gebuchte Verkaufsrechnungen** die gebuchte Verkaufsrechnung aus, die Sie stornieren möchten, wählen Sie die Aktion **Stornieren** und wählen Sie dann die Aktion **Korrekturgutschrift erstellen**.

    Der Verkaufsgutschriftskopf enthält einige Informationen aus der gebuchten Verkaufsrechnung. Sie können alle Felder bearbeiten, zum Beispiel mit neuen Daten, die die Rückholvereinbarung wiedergeben.  
3. Bearbeiten Sie Informationen über die Zeilen entsprechend der Vereinbarung, wie die Anzahl der zurückzuerstattenden Artikel oder der gutzuschreibende Betrag.
4. Wählen Sie die Aktion **Vorbereiten** und wählen Sie dann die Aktion **Buchungen anwenden**.
5. Auf der Seite **Debitorenposten zuweisen** wählen Sie die Zeile mit dem gebuchten Verkaufsbeleg, die Sie der Verkaufsgutschrift zuordnen möchten, und wählen Sie dann **Zuweisungs-ID festlegen** aus.

    Die Kennzeichnung der Verkaufsgutschrift wird im Feld **Zuweisungs-ID** angezeigt.
6. Geben Sie in jeder Zeile im Feld **Anzuwendender Betrag** den Betrag ein, den Sie ausgleichen möchten, wenn dieser kleiner ist als der ursprüngliche Betrag.  

    Im unteren Bereich der Seite **Debitorenposten zuweisen** können Sie den Gesamtbetrag sehen, um alle beteiligten Posten zu stornieren, nämlich wenn der Wert im Feld **Saldo** Null ist.
7. Wählen Sie die Schaltfläche **OK** aus. Wenn Sie die Verkaufsgutschrift buchen, wird sie für die angegebenen gebuchten Verkaufsrechnungen angewandt.

    Nachdem Sie die erforderlichen Verkaufsgutschriftszeilen erstellt ober bearbeitet haben, und der Ausgleich einzelner oder mehrerer Posten angegeben wird, können Sie fortfahren, die Verkaufsgutschrift zu buchen.  
8. Wählen Sie die Aktion **Buchen** und dann die Aktion **Buchen und Senden**.  

Das Dialogfeld **Buchungs- und Sendebestätigung** wird geöffnet und zeigt die bevorzugte Sendemethode für den Debitor an. Sie können die Sendemethode ändern, indem Sie die Schaltfläche vom Feld **Beleg senden an** auswählen. Weitere Informationen finden Sie unter [Einrichten von Sendeprofilen](sales-how-setup-document-send-profiles.md).  

Die gebuchten Verkaufsdokumente für die entsprechende Gutschrift werden nun storniert und eine Erstattung der Zahlung kann für den Debitor erstellt werden. Die Verkaufsgutschrift wird entfernt und durch einen neuen Beleg in der Liste der gebuchten Verkaufsgutschriften ersetzt.

## <a name="to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice"></a>Erstellt eine neue Verkaufsgutschrift, um eine gebuchte Verkaufsrechnung zurückzusetzen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Verkaufsgutschriften** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie **Neu**, um eine neue leere Verkaufsgutschrift zu öffnen.
3. Geben Sie in das Feld **Kundenname** den Namen eines bestehenden Kunden ein.
4. Wählen Sie die Aktion **Vorbereiten** und dann die Aktion **Dokument kopieren**.
5. Wählen Sie auf der Seite **Verkaufsbeleg kopieren** im Feld **Dokumenttyp** **Rechnung buchen** aus.
6. Wählen Sie das Feld **Belegnummer**, um die Seite **Gebuchte Verkaufsrechnungen** zu öffnen, und wählen Sie dann den Datensatz der gebuchten Verkaufsrechnungen aus, der Zeilen enthält, die Sie stornieren möchten.
7. Wählen Sie das Kontrollkästchen **Zeilen neu berechnen**, wenn die kopierten gebuchten Verkaufsrechnungszeilen, mit einzelnen Änderungen im Artikelpreis und im Einstandspreis, aktualisiert werden sollen, da die Rechnung gebucht wurde.
8. Wählen Sie die Schaltfläche **OK** aus. Die kopierten Rechnungszeilen werden in die Verkaufsgutschrift eingefügt.
9. Schließen Sie die Verkaufsgutschrift ab, so wie dies unter [Erstellt eine neue Verkaufsgutschrift, um eine gebuchte Verkaufsrechnung zurückzusetzen](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-from-a-posted-sales-invoice) erklärt ist.

## <a name="to-create-a-sales-allowance"></a>So erstellen Sie einen Verkaufsrabatt
Sie können einem Debitoren eine Gutschrift mit einem Preisnachlass ausstellen, wenn der Debitor leicht beschädigte Artikel erhalten hat oder die Artikel zu spät geliefert wurden.  
Sie können diesen herabgesetzten Preis als Zu-/Abschlag (Artikel) in einer Gutschrift oder einer Reklamation buchen und ihn der gebuchten Lieferung zuordnen. Nachfolgend wird es für eine Verkaufsreklamation erläutert, aber dieselben Schritte gelten für eine Verkaufsgutschrift.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Verkaufsgutschriften** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie **Neu**, um eine neue leere Verkaufsgutschrift zu öffnen.
3. Füllen Sie den Kopf der Gutschrift mit den entsprechenden Informationen über den Debitor aus, dem Sie den Verkaufsrabatt gewähren möchten.  
4. Wählen Sie auf dem Inforegister **Zeilen** im Feld **Art** die Option **Zu-/Abschlag (Artikel)**.  
5. Geben Sie im Feld **Nr.** den entsprechenden Chargenwert ein.  
     Vielleicht möchten Sie eine spezielle Artikel Zu-/Abschlagsnummer erstellen, um Verkaufsrabatte abzudecken.  
6. Geben Sie im Feld **Menge** den Wert **1** ein.  
7. Geben Sie in das Feld **Einheitspreis ohne MwSt.** den Betrag für den Verkaufsrabatt ein.  
8. Den Verkaufsrabatt können Sie als Zu-/Abschlag (Artikel) den Artikeln in der gebuchten Lieferung zuweisen. Weitere Informationen finden Sie untert [Verwenden von Artikelzuschlägen für zusätzliche Kosten](payables-how-assign-item-charges.md). Kehren Sie zur Seite **Gutschrift** zurück.  

Wenn Sie die Verkaufsreklamation buchen, wird die Wiedereinlagerungsgebühr zu dem entsprechenden Betrag des Verkaufspostens addiert. Auf diese Art können Sie genaue Bestandbewertung führen.

## <a name="to-combine-return-receipts"></a>Sammelgutschrift für Reklamationen kombinieren
Sie können Rücksendungen zusammenfassen, wenn Ihr Debitor mehrere Artikel zurücksendet, die durch mehrere Verkaufsreklamationen abgedeckt werden.  

Wenn Sie die Artikel in Ihrem Lager erhalten, buchen Sie die entsprechende Verkaufsreklamation als geliefert. Dadurch erzeugen Sie gebuchte Rücksendungen. Dies erstellt gebuchte Rücksendungen.  

Wenn Sie bereit sind, an den Debitoren zu fakturieren, können Sie eine Verkaufsgutschrift anlegen und die gebuchten Rücksendungszeilen automatisch in diesen Beleg kopieren, anstatt jede Verkaufsreklamation einzeln zu fakturieren. Dann können Sie die Verkaufsgutschrift buchen und einfach alle offenen Verkaufsreklamationen auf einmal fakturieren.  

Um Rücksendungen zusammenzufassen, muss das Kontrollkästchen **Sammelversand** auf der Seite **Debitorenkarte** aktiviert sein.  

### <a name="to-manually-combine-return-receipts"></a>So werden Rücksendungen manuell zusammengefasst:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Verkaufsgutschriften** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu**.
3. Füllen Sie im Inforegister **Allgemein** die notwendigen Felder aus.  
4. Wählen Sie die **Rücklieferzeilen abrufen** Aktion aus.  
5. Wählen Sie die Rücksendungszeilen aus, die Sie in die Gutschrift einschließen möchten:  

    - Um alle Zeilen einzufügen, wählen Sie alle Zeilen aus, und wählen Sie die Schaltfläche **OK**.  

    - Um spezifische Zeilen einzufügen, wählen Sie die Zeilen aus, und wählen Sie die Schaltfläche **OK**.  
6.  Wenn Sie eine falsche Lieferzeile ausgewählt haben oder von vorn beginnen möchten, können Sie einfach die Zeilen in der Gutschrift löschen und die Funktion **Rücksendungszeilen holen** erneut ausführen.  
7.  Buchen Sie die Rechnung.  

### <a name="to-automatically-combine-return-receipts"></a>So werden Rücksendungen automatisch zusammengefasst

Sie können Rücksendungen automatisch zusammenfassen und haben zudem die Möglichkeit, Gutschriften automatisch zu buchen, indem Sie die Stapelverarbeitung **Sammelgutschrift für Rekl.** verwenden.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Sammelgutschrift für Rekl.** ein und wählen Sie den zugehörigen Link.
2. Auf der Seite **Sammelgutschrift für Rekl.** füllen Sie die Felder aus, um die relevanten Rücksendungen auszuwählen.
3. Wählen Sie das Feld **Gutschriften buchen** aus. Wenn nicht, müssen Sie die ausgefüllten Einkaufsgutschriften manuell buchen.
4. Wählen Sie die Schaltfläche **OK** aus.  

### <a name="to-remove-a-received-and-invoiced-return-order"></a>So werden eingegangene und fakturierte Reklamationen entfernt:

Wenn Rücksendungen auf diese Weise fakturiert werden, bleiben die Rücksendungsaufträge, von denen ausgehend die Rücksendungen gebucht werden, weiterhin bestehen, auch wenn sie vollständig geliefert und fakturiert wurden.  

Wenn Rücksendungen in einer Gutschrift zusammengefasst und gebucht werden, wird für die gutgeschriebenen Zeilen eine gebuchte Verkaufsgutschrift erstellt. Das Feld **Menge fakturiert** auf der entstehenden Verkaufsreklamation wird ausgehend von der fakturierten Menge aktualisiert.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Erledigte Verkaufsaufträge löschen** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie im Feld **Kontonummer** Filterfeld an, welche Verkaufsaufträge zu löschen sind.  
3. Wählen Sie die Schaltfläche **OK** aus.  

Sie können die einzelnen Verkaufsaufträge auch manuell löschen.  

## <a name="inventory-costing"></a>Bestandskosten

Um die korrekte Lagerbewertung beizubehalten, möchten Sie üblicherweise zurückgegebene Artikel im Lager zum Einstandspreis, zum dem sie verkauft wurden und nicht mit dem aktuellen Einstandspreis einlagern. Dies wird als Einstandspreisrückverfolgung bezeichnet.

Es gibt zwei Funktionen, mit denen Sie automatisch eine exakte Kalkulation vornehmen können:  

|Funktion|Beschreibung|  
|------------------|---------------------------------------|  
|Funktion **Zu stornierende gebuchte Belegzeilen abrufen** auf der Seite **Verkaufsreklamation**|Kopiert Zeilen einer oder mehrerer gebuchter Verkaufsbelegzeilen, um den ursprünglichen Auftrag zu stornieren. Weitere Informationen finden Sie unter [Erstellen eines Verkaufsreklamationsauftrags auf der Grundlage eines oder mehrerer gebuchter Belege](sales-how-process-sales-returns-orders.md#create-a-sales-return-order-based-on-one-or-more-posted-sales-documents).|  
|Funktion **Beleg kopieren** auf den Seiten **Verkaufsgutschrift** und **Verkaufsreklamation**|Kopiert den Kopf und die Zeilen aus einem gebuchten Beleg, der storniert werden soll.<br /><br /> Erfordert, dass das Kontrollkästchen **Einst.-Pr.-Rückverfolg. notw.** auf der Seite **Debitoren und Verkauf Einr.** ausgewählt ist.|

Um exakte Einstandspreisstornierung manuell zuzuordnen, müssen Sie das Feld **Ausgegl. von Artikelposten** für alle Rückholbelegzeile Art wählen und dann die Nummer des ursprünglichen Verkaufspostens. Dies verknüpft die Verkaufsgutschrift oder Verkaufsreklamation mit dem ursprünglichen Verkaufsposten und stellt sicher, dass der Artikel mit dem ursprünglichen Einstandspreis bewertet wird.

Weitere Informationen finden Sie unter [Designdetails: Bestandskosten](design-details-inventory-costing.md).

## <a name="see-also"></a>Siehe auch

[Verkauf](sales-manage-sales.md)  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Belege per E-Mail senden](ui-how-send-documents-email.md)  
[Verarbeiten einer Einkaufsrücklieferung oder von Stornierungen](purchasing-how-process-purchase-returns-cancellations.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
