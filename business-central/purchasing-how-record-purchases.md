---
title: Einkäufe mit Einkaufsrechnungen erfassen (enthält Video)
description: 'Beschreibt, wie Sie Bestand, Nicht-Bestandsartikel oder Ressourcen erwerben, indem Sie Einkaufsrechnungen oder Bestellungen erstellen und buchen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: procurement
ms.search.form: '50 ,51, 53, 56, 146, 147, 9307, 9309, 9306, 9308, 9310'
ms.date: 03/21/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="record-purchases-with-purchase-invoices-and-orders"></a>Einkäufe mit Einkaufsrechnungen und Aufträgen erfassen

Sie erstellen eine Einkaufsrechnung oder Einkaufsbestellung, um die Kosten der Einkäufe zu erfassen und Kreditoren zu verfolgen. Einkaufsrechnungen und Einkaufsbestellungen werden auch verwendet, um Lagerbestände dynamisch zu aktualisieren, sodass Sie Ihre Lagerbestandskosten minimieren und besseren Debitorenservice bereitstellen können. Die Einkaufskosten, einschließlich Servicekosten und Bestandswerte, die aus der Buchung von Einkaufsrechnungen resultieren, tragen zu den Gewinnzahlen und Key Performance Indicators (KPIs) in Ihrem Rollencenter bei.

## <a name="record-purchases-with-purchase-invoices"></a>Einkäufe mit Einkaufsrechnungen erfassen

Wenn Sie die Bestandsartikel erhalten oder wenn die gekaufte Dienstleistung abgeschlossen ist, buchen Sie die Rechnung, um die Bestands- und Finanzdaten zu aktualisieren und die Zahlung an den Lieferanten gemäß den Zahlungsbedingungen zu aktivieren. [Zahlungen vornehmen](payables-make-payments.md).

> [!CAUTION]  
> Buchen Sie die physischen Artikel einer Einkaufsrechnung erst dann, wenn Sie die Artikel erhalten und die endgültigen Kosten des Kaufs, einschließlich aller zusätzlichen Kosten, kennen. Andernfalls werden Ihr Lagerwert und DB-Zahlen möglicherweise falsch sein.

### <a name="create-and-post-a-purchase-invoice"></a>Eine Verkaufsrechnung erstellen und buchen

Im folgenden Schritt wird beschrieben, wie Sie eine Einkaufsrechnung erstellen. Die Schritte für die Erstellung einer Bestellung sind ähnlich. Der Hauptunterschied besteht darin, dass Bestellungen einige zusätzliche Felder und Aktionen für die physische Handhabung von Artikeln haben.

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Einkaufsrechnungen** ein, und wählen Sie dann den zugehörigen Link.  
2. Geben Sie in das Feld **Kreditorenname** den Namen eines vorhandenen Kreditors ein.

    Andere Felder auf der Seite **Einkaufsrechnung** werden nun mit den Standardinformationen für den ausgewählten Kreditor ausgefüllt. Wenn der Kreditor noch nicht erfasst wurde, dann führen Sie die folgenden Schritte durch:

    1. Geben Sie im Feld **Kreditorenname** den Namen eines neuen Kreditors ein.
    2. Klicken Sie im Dialogfeld auf **Ja**, um den neuen Kreditor zu bestätigen.
    3. Weitere Informationen zum Ausfüllen der Kreditorenkarte finden Sie unter [Neue Kreditoren registrieren](purchasing-how-register-new-vendors.md).  
    4. Wenn Sie die Kreditorenkarte abgeschlossen haben, wählen Sie **OK**, um zur Seite **Einkaufsrechnung** zurückzugehen.

3. Füllen Sie auf der Seite **Einkaufsrechnung** die Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Sie sind nun bereit, die Einkaufsrechnungszeilen mit vom Kreditor gekauften Artikeln oder Ressourcen auszufüllen.

    > [!NOTE]  
    > Wenn Sie wiederkehrende Einkaufszeilen für den Debitor, wie einen monatlichen Ersatzauftrag, eingerichtet haben, können Sie diese Zeilen auf der Rechnung durch Auswählen der Aktion **Wiederkehrende Einkaufszeilen** abrufen einfügen.
4. Geben Sie auf der Seite **Zeilen** Inforegister in das Feld **Positionsnummer** die Nummer eines Bestandsartikels oder einer Dienstleistung ein.
5. Geben Sie in dem Feld **Menge** die Anzahl des Artikels an, der eingekauft wird.

    Das Feld **Zeilenmenge** wird aktualisiert, um den Wert im Feld **EK-Preis** multipliziert ist mit dem Wert im Feld **Menge** anzuzeigen.

    Der Preis und der Zeilenbetrag auf den Verkaufsrechnungszeilen werden mit oder ohne MwSt. angezeigt, je nachdem, was Sie im Feld **Preis inklusive Mehrwertsteuer** auf der Kreditorenkarte ausgewählt haben.

    Die Summenfelder unter den Positionen werden automatisch aktualisiert, wenn Sie Positionen erstellen oder ändern, um die Beträge anzuzeigen, die auf die Sachkonten gebucht werden.

6. Geben Sie im Feld **Rabattbetrag in Rechnung stellen** einen Betrag ein, der vom Wert abgezogen werden soll, der im Feld **Total inklusive Mehrwertsteuer** im unteren Bereich der Rechnung angezeigt wird.

    > [!NOTE]  
    > Wenn Sie Rechnungsrabatte für den Kreditor eingerichtet haben, wird der angegebene Prozentwert automatisch in das Feld **Kreditorenrechnungsrabatt %** eingetragen, sobald die Kriterien erfüllt sein, und der entsprechende Betrag wird im Feld eingefügt. Der zugeordnete Betrag wird dann im Feld **Rechnungsrabattbetrag** eingefügt.
7. Wenn Sie die gekauften Artikel oder Dienstleistungen erhalten, wählen Sie **Buchen**.

Der Kauf wird nun im Bestand, in den Ressourcen-Sachkonten und in den Finanzdokument widergespiegelt, und die Kreditorenzahlung wird aktiviert. Die Einkaufsrechnung wird in der Liste der gebuchten Einkaufsrechnungen entfernt und durch einen neuen Beleg in der Liste der gebuchten Einkaufsrechnungen ersetzt. Weitere Informationen dazu, was passiert, wenn Sie Einkaufbelege buchen, finden Sie unter [Einkäufe buchen](purchasing-how-record-purchases.md#posting-purchases).

> [!NOTE]
> In seltenen Fällen können die gebuchten Beträge von dem abweichen, was in den Summenfeldern angezeigt wird. Dies ist in der Regel auf Rundungsrechnungen in Bezug auf Mehrwertsteuer oder Verkaufssteuer zurückzuführen.
>
> Verwenden Sie zum Übeprüfen der tatsächlich gebuchten Beträge die Seite **Statistiken**, die die Rundungsberechnungen berücksichtigt. Auch wenn Sie die Aktion **Freigabe** auswählen, werden die Summenfelder aktualisiert, sodass sie die Rundungsberechnungen enthalten.

## <a name="posted-invoices"></a>Gebuchte Rechnungen

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Sie können eine gebuchte Einkaufsrechnung einfach korrigieren oder stornieren, bevor Sie den Kreditor bezahlen. Zum Beispiel, wenn Sie einen Tippfehler korrigieren möchten oder den Kauf früh im Bestellvorgang ändern möchten. Weitere Informationen finden Sie unter [Ändern oder Löschen einer unbezahlten Bestellungsrechnung](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Um den Kauf eines Artikels oder Services auf einer gebuchten Einkaufsrechnung, für welche die Zahlung verarbeitet wird, rückgängig zu machen, erstellen Sie eine Einkaufsgutschrift. Weitere Informationen finden Sie unter [Verarbeiten einer Bestellungsrücklieferung oder von Stornierungen](purchasing-how-process-purchase-returns-cancellations.md).

[Die Liste **Gebuchte Einkaufsrechnungen** öffnen](https://businesscentral.dynamics.com/?page=146) in [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="purchasing-noninventory-items"></a>Nicht-Bestandsartikel kaufen

Die Zeilen auf einer Einkaufsrechnung können vom Typ **Ressource** oder **Artikel** sein. Artikelkarten können als **Bestand**, **Service** oder **Nicht-Bestand** klassifiziert werden, wenn die Einheit eine physische Einheit ist, eine Arbeitszeiteinheit (auch anwendbar auf Ressourcen) oder eine physische Einheit, die nicht auf Lager ist. Erfahren Sie mehr unter [Registrieren Sie neue Artikel](inventory-how-register-new-items.md). Der Kaufsrechnungsprozess ist derselbe für alle erwähnten Artikeltypen.

> [!NOTE]
> Mit dem Zeilentyp **Ressource** Bestellzeile können Sie auch externe Ressourcen einkaufen, z.B. um einem Kreditor die gelieferte Arbeit in Rechnung zu stellen. Erfahren Sie mehr unter [Ressourcen einrichten](projects-how-setup-resources.md).
>
> Um eine gekaufte Ressource zu verwenden, müssen Sie möglicherweise die Kapazität der Ressource festlegen und sie manuell einem Projekt zuweisen. Durch den Kauf einer Ressource wird ein Ressourcenposten erstellt, jedoch werden die Ressourcen-Sachkonto-Einträge nicht nach Menge und Wert verfolgt, wie dies z.B. bei Artikeln der Fall ist. Wenn eine Mengen- und Wertverfolgung erforderlich ist, sollten Sie die Verwendung anderer Positionsarten in Betracht ziehen.

## <a name="when-to-use-purchase-orders"></a>Verwendung von Bestellungen

Verwenden Sie Bestellungen, wenn Sie Teillieferungen einer Bestellmenge erfassen müssen. Zum Beispiel, weil der Kreditor nicht die vollständige Menge vorrätig hat. Wenn Sie verkaufte Artikel liefern, indem Sie direkt von Ihrem Kreditor an Ihren Debitor versenden, müssen Sie ebenfalls Einkaufsbestellungen verwenden. Erfahren Sie mehr unter [Direktlieferungen machen](sales-how-drop-shipment.md).

In allen anderen Aspekten ist das Vorgehen bei Einkaufsbestellungen genau wie bei Einkaufsrechnungen. Das folgende Verfahren basiert auf einer Einkaufsrechnung. Bei einer Bestellung sind die Schritte ähnlich.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

## <a name="receive-items-with-a-purchase-order"></a>Empfangen Sie Artikel mit einer Einkaufsbestellung

Der folgende Schritt beschreibt, wie Artikel mit einer Bestellung empfangen werden. 

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Einkaufsbestellungen** ein, und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie eine bestehende Bestellung, oder erstellen Sie eine neue.
3. Geben Sie in dem Feld **Menge akt. Lieferung** die empfangene Menge an.

   > [!NOTE]
   > Wenn die eingegangene Menge mehr ist als die Menge in der Bestellung ist und der Kreditor so eingestellt ist, dass er einen Eingangsüberschuss zulässt, dann verwenden Sie das Feld **Eingangsüberschussmenge**, um die überschüssige Menge zu behandeln. Weitere Informationen finden Sie im Abschnitt [Um mehr Artikel als bestellt zu erhalten](purchasing-how-record-purchases.md#receive-more-items-than-you-ordered).
4. Wählen Sie die Aktion **Buchen**.

  Der Wert im Feld **Bereits gelief. Menge** wird aktualisiert. Wenn es sich dabei um eine Teillieferung handelt, ist der Wert niedriger als der Wert im Feld **Menge**.

> [!NOTE]
> Wenn Sie eine Lagerdurchlaufzeit verwenden, können Sie nicht die Aktion **Buchen** auf die Bestellung anwenden, um den Eingang zu erfassen. Deshalb hat ein Lagerarbeiter die Bestellmenge bereits als eingegangen gebucht. Weitere Informationen finden Sie unter [Designdetails - Eingehender Lagerfluss](design-details-inbound-warehouse-flow.md).

## <a name="receive-more-items-than-you-ordered"></a>Mehr Artikel als bestellt erhalten

Wenn mehr Waren ankommen, als bestellt waren, möchten Sie diese möglicherweise erhalten, anstatt den Beleg zu stornieren. Beispielsweise kann es billiger sein, die überschüssigen Artikel Ihres Inventars zu behalten, als sie zurückzugeben, oder Ihr Kreditor bietet Ihnen möglicherweise einen Skonto an, wenn Sie sie behalten.

Im nachfolgenden Video wird der Umgang mit Übereingängen veranschaulicht.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RW1l2PE]

<!--move the over-receipt setup info to an article about purchasing. Keep the concept info here and link to the steps-->
### <a name="set-up-over-receipts"></a>Richten Sie Übereingänge ein

Erstellen Sie Eingangsüberschusscodes, um einen Prozentsatz zu definieren, um den eine erhaltene Menge die bestellte Menge überschreiten darf. Geben Sie den Prozentsatz im Feld **Übereingangtoleranz %** an. Sie weisen dann den Code auf den Seiten Artikelkarte oder Kreditorenkarte für Artikel und Kreditoren zu.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Geben Sie **Eingangsüberschusscodes** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="assign-the-over-receipt-code-to-an-item"></a>Den Eingangsüberschusscode einem Artikel zuweisen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Posten** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Seite **Artikelkarte** des zugehörigen Artikels.
3. Wählen Sie im Feld **Eingangsüberschusscode** den Code aus, der den Prozentsatz enthält, den Sie für Übereingänge zulassen möchten.

Der Übereingangscode wird dem Artikel zugewiesen. Einkaufsbestellungen oder Wareneingänge für den Artikel erlauben Ihnen nun den Empfang von mehr als der bestellten Menge innerhalb des Prozentsatzes der Überzugstoleranz.

> [!NOTE]
> Sie können einen Genehmigungs-Workflow einrichten, um zu verlangen, dass überzählige Belege genehmigt werden müssen, bevor sie bearbeitet werden können. Aktivieren Sie das Kontrollkästchen **Genehmigung erforderlich** auf der Seite **Eingangsüberschuss-Code**. Erfahren Sie mehr unter [Workflows erstellen](across-how-to-create-workflows.md).

### <a name="over-receive-an-order"></a>Übereingang eines Auftrags

In Einkaufs- und Lagerzugangszeilen wird das Feld **Über-Empfangsmenge** dazu verwendet, überzählige Mengen zu erfassen, d.h. Mengen, die den Wert im Feld **Menge**, die bestellte Menge, überschreiten.

Wenn Sie einen Übereingang bearbeiten, können Sie entweder den Wert im Feld **Zu erhaltende Menge** auf die erhaltene Menge erhöhen. Das Feld **Übereingangsmenge** wird aktualisiert, um die Überschussmenge anzuzeigen. Alternativ können Sie die überschüssige Menge in das Feld **Übereingangsmenge** eingeben. Das Feld **Zu erhaltende Menge** wird aktualisiert, um die bestellte Menge plus die überschüssige Menge anzuzeigen. Das folgende Verfahren beschreibt, wie das Feld **Zu empfangende Menge** auszufüllen ist.  

1. Geben Sie bei einer Bestellung oder einem Lagerzugangsbeleg, bei dem die eingegangene Menge höher als die bestellte Menge ist, die eingegangene Menge in das Feld **Zu erhaltende Menge** ein.

    Wenn die Erhöhung innerhalb der durch einen zugeordneten Eingangsüberschusscode festgelegten Toleranz liegt, wird das Feld **Eingangsüberschussmenge** aktualisiert, um die Menge anzuzeigen, um die der Wert im Feld **Menge** überschritten wird.

    Wenn die Erhöhung über der Toleranz liegt, ist der Eingangsüberschuss nicht zulässig. Untersuchen Sie, ob ein anderer Eingangsüberschusscode dies zulässt. Andernfalls kann nur die bestellte Menge empfangen werden, und die überschüssige Menge muss anderweitig behandelt werden, z.B. durch Rücksendung an den Lieferanten.

2. Buchen Sie den Eingang wie jeden anderen Eingang.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] behandelt nicht automatisch die finanziellen Aspekte von Übereingängen. Dies müssen Sie in Absprache mit dem Kreditor manuell regeln, z.B. indem der Lieferant eine neue oder aktualisierte Rechnung weiterleitet.

## <a name="external-document-number"></a>Externe Belegnummer

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="posting-purchases"></a>Einkäufe buchen

Bei einem Kaufbeleg können Sie zwischen den folgenden Buchungsaktionen wählen:

* **Veröffentlichen**
* **Buchungsvorschau**
* **Buchen und Drucken**
<!--* **Test Report**-->
* **Stapelbuchung**

Wenn ein Einkaufsbeleg gebucht wird, werden das Kreditorenkonto, das Hauptbuch, die Einträge im Artikel-Sachkonto und die Einträge im Ressourcen-Sachkonto aktualisiert.

Für jeden Einkaufsbeleg wird ein Einkaufseintrag in der Tabelle **Sachposten** angelegt. Darüber hinaus wird ein Posten in der Tabelle **Kreditorenposten** erzeugt und ein Sachposten im entsprechenden Einkaufskonto. Darüber hinaus kann die Buchung des Einkaufs zu einer Mehrwertsteuerbuchung (MwSt.) und einem Sachposten für den Rabattbetrag führen. Ob ein Posten für Rabatt gebucht wird, hängt von den Einstellungen im Feld **Rabattbuchung** auf der Seite **Kreditoren & Einkauf Einrichtung** ab.

Für jede Einkaufszeile werden, falls anwendbar. die folgenden Einträge erstellt:

* in der Tabelle **Buch.-Blatt-Position-Eingabe**, wenn die Einkaufszeile vom Typ **Artikel** ist.
* in der Tabelle **Buch.-Blatt-Eintrag**, wenn die Einkaufszeilen vom Typ **Buch.-Blatt-Konto** sind
* in der Tabelle **Ressourcen-Buch.-Blatt-Eingabe**, wenn die Einkaufszeile vom Typ **Ressourcen** ist.

Darüber hinaus werden Einkaufsbelege immer im Feld **Einkaufslieferkopf** und **Einkaufsrechnungskopf** Tabellen erfasst.

Sie können jederzeit verschiedene Hauptbucheinträge überprüfen, die als Ergebnis von Buchungen erstellt werden. Wählen Sie **Buchungsvorschau**, um den Beleg zu validieren und die erwarteten Hauptbucheinträge zu prüfen.


> [!IMPORTANT]  
> Wenn Sie eine Bestellung für Artikel buchen, können Sie sowohl einen Beleg als auch eine Rechnung erstellen. Dies kann gleichzeitig oder unabhängig voneinander durchgeführt werden. Sie können auch eine Teillieferung und eine Teilrechnung erzeugen, indem Sie die Felder **Menge zu liefern** und/oder **Zu fakturieren** in den jeweiligen Zeilen des Verkaufsauftrags ausfüllen, bevor Sie buchen. Beachten Sie, dass Sie keine Einkaufsrechnung aus einer Bestellung für Produkte oder Dienstleistungen erstellen können, die nicht erhalten wurden. Das bedeutet, dass Sie vor der Fakturierung einen Wareneingang gebucht haben müssen, oder Sie müssen "Liefern und Fakturieren" wählen.

Sie können entweder buchen oder buchen und drucken. Wenn Sie sich entscheiden, zu buchen und zu drucken, wird ein Bericht gedruckt, wenn der Auftrag gebucht wird. Sie können auch **Stapelbuchen** wählen, mit der Sie mehrere Aufträge gleichzeitig buchen können. Erfahren Sie mehr unter [Mehrere Dokumente gleichzeitig buchen](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Anzeigen von Posten

Wenn die Buchung vollständig ist, werden die gebuchten Einkaufszeilen aus der Bestellung entfernt. Eine Meldung erscheint, die Ihnen mitteilt, dass die Buchung vollständig ist. Danach stehen die gebuchten Posten auf den verschiedenen Seiten zur Verfügung, darunter auf den Seiten **Kreditorenbuch-Einträge**, **Buch.-Blatt-Einträge**, **Buch.-Blatt-Buch-Einträge**, **Ressourcen-Buch.-Blatt-Einträge**, **Einkaufsbelege** und **Gebuchte Einkaufsrechnungen**.

In den meisten Fällen können Sie Posten von der betroffenen Karte oder dem betroffenen Beleg aus öffnen. Auf der Seite **Kreditorenkarte** wählen Sie beispielsweise die Aktion **Einträge** aus.

## <a name="editing-ledger-entries"></a>Bearbeiten von Posten

Sie können bestimmte Felder in gebuchten Einkaufsbelegen bearbeiten, z. B. das Feld **Zahlungsreferenz**. Erfahren Sie mehr unter [Gebuchte Belege bearbeiten](across-edit-posted-document.md). Bei kritischeren Feldern, die sich auf den Überwachungspfad auswirken, müssen Sie die Buchung stornieren oder rückgängig machen. Erfahren Sie mehr unter [Buch.-Blatt-Buchungen stornieren und Rückgängigmachung von Eingängen/Versendungen](finance-how-reverse-journal-posting.md).

## <a name="see-also"></a>Siehe auch

[Angebote anfordern](purchasing-how-request-quotes.md)  
[Artikel für einen Verkauf einkaufen](purchasing-how-purchase-products-sale.md)  
[Direktlieferungen vorbereiten](sales-how-drop-shipment.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Einkaufeinrichten](purchasing-setup-purchasing.md)  
[Ressourcen einrichten](projects-how-setup-resources.md)  
[Registriert einen neuen Kreditor](purchasing-how-register-new-vendors.md)  
[Gebuchte Belege bearbeiten](across-edit-posted-document.md)  
[Mehrere Dokumente gleichzeitig buchen](ui-batch-posting.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Journale und Dokumente buchen](ui-post-documents-journals.md)  
[Ändern oder Löschen einer unbezahlten Einkaufsrechnung](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Suche nach Seiten und Informationen mit „Sie wünschen...“](ui-search.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
