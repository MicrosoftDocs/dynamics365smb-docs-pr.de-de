---
title: Zahlungen mit nicht geleisteten Verkaufsbelegen ausgleichen
description: 'Sie gleichen die Beträge aus, die von den Debitoren mit Bezug auf den entsprechenden Verkaufsbeleg bezahlt werden und buchen die Zahlungen, um den Debitor, die Finanzbuchhaltung und die Bankposten zu aktualisieren.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment process, cash receipts, customer payment'
ms.search.form: '1290, 1294, 1287'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="reconcile-customer-payments-from-a-list-of-unpaid-sales-documents"></a>Debitoren-Zahlungen aus einer Liste mit unbezahlten Verkaufsbelegen abstimmen

Nachdem Kunden elektronische Zahlungen auf Ihr Bankkonto getätigt haben, müssen Sie die folgenden Maßnahmen ergreifen:

* Wenden Sie jede Zahlung auf den entsprechenden gebuchten Verkaufsbeleg an
* Buchen Sie Zahlungseingänge, um die Debitoren-, Sachposten- und Bankposten zu aktualisieren. 

Abhängig von den Unternehmensanforderungen können Sie bezahlt werden und die Zahlung auf unterschiedliche Arten erfassen: automatisch und durch Zahlungsverkehr.  

> [!NOTE]  
> Sie können die selben Aufgaben einschließlich Debitorenzahlungen auf der Seite **Zahlungsabstimmungsbuch.-Blatt** mithilfe von Funktionalitäten für den Bankkontoauszugsimport ausführen, die automatische Anwendung und die Bankkontoabstimmung verwenden. Weitere Informationen finden Sie unter [Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-auto-application.md).

Verwenden Sie die Seite **Registrieren Sie Kundenzahlungen**, um interne Konten ausgleichen, indem tatsächliche Kassenzahlen verwendet werden, um sicherzustellen, dass Zahlungen eingezogen werden. Sie können Einzel- oder Pauschalzahlungen schnell prüfen und buchen, Skontozahlungen verarbeiten und unbezahlte Dokumente finden.

Zahlungen für verschiedene Debitoren, die verschiedene Fälligkeitsdaten haben, müssen als einzelne Zahlungen gebucht werden. Zahlungen für denselben Debitor, der das gleiche Fälligkeitsdatum hat, können als Pauschalzahlung gebucht werden. Pauschalzahlungen sind beispielsweise dann nützlich, wenn ein Debitor eine einzelne Zahlung getätigt hat, die mehrere Verkaufsrechnungen umfasst.

## <a name="to-set-up-the-payment-registration-journal"></a>Zahlungsregistrierungsbuch.-Blatt einrichten
Da Sie verschiedene Zahlungsarten auf verschiedene Gegenkonten buchen können, müssen Sie ein Gegenkonto auf der Seite **Zahlungsanmeldungs-Einrichtung** auswählen, bevor Sie die Bearbeitung von Debitorenzahlungen starten. Wenn Sie immer auf das gleiche Gegenkonto buchen, können Sie dieses Konto als Standardwert festlegen und diesen Schritt jedes Mal vermeiden, wenn Sie die Seite **Debitorenzahlung erfassen** öffnen.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Einrichtung der Zahlungsregistrierung** ein und wählen Sie dann den zugehörigen Link. Sie können auch auf der Seite **Debitorenzahlung erfassen** die Aktion **Einrichten** auswählen.
2. Füllen Sie die Felder auf der Seite **Zahlungserfassungseinrichtung** aus. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)] Wählen Sie ein Feld aus, um eine kurze Beschreibung des Feldes zu lesen oder einen Link für weitere Informationen zu öffnen.  

> [!TIP]
> Um später Buchungen, die über das Journal gebucht wurden, leichter identifizieren zu können, können Sie dem Journal eine bestimmte Nummernserie zuweisen. Dies ist hilfreich, wenn Sie Zahlungsabstimmungsjournale verwenden, um Zahlungen zu registrieren und anzuwenden.

## <a name="to-register-customer-payments-individually"></a>Um Debitorenzahlungen einzeln zu erfassen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Debitoren-Zahlungen registrieren** ein und wählen Sie dann den zugehörigen Link.  

    Die Seite **Debitorenzahlungen registrieren** werden alle gebuchten Belege angezeigt, für die eine Zahlung erfasst werden kann. Dieselbe Seite kann auch aus der Seite **Debitoren** und der **Debitorenkarte** geöffnet werden , in der sie automatisch für den angegebenen Debitoren gefiltert wird.  
2. Wählen Sie das Kontrollkästchen **Zahlung erfolgt** in der Zeile, die den gebuchten Beleg darstellt, für den eine Zahlung geleistet wurde.

    Wenn das Kontrollkästchen **Automatische Datumseingabe** auf der Seite **Einrichtung der Zahlungserfassung** aktiviert ist, wird das Arbeitsdatum in Feld **Empfangsdatum** eingegeben.  
3. Geben Sie im Feld **Empfangsdatum** das Datum ein, an dem die Zahlung gemacht wurde. Dieses Datum kann vom Arbeitsdatum abweichen.  
4. In dem Feld **Betrag erhalten** geben Sie den Betrag ein, der bezahlt worden ist.

    Für gesamte Zahlungen ist dies der gleiche Betrag wie der Betrag im Feld **Verbleibender Betrag** in der Zeile. Für Teilzahlungen ist dieser Betrag niedriger als der Betrag im Feld **Verbleibender Betrag** in der Zeile.
5. Wiederholen Sie die Schritte 2-4 für andere Zeilen, die gebuchte Belege darstellen, für die Zahlungen getätigt wurden.  
6. Wählen Sie die Aktion **Zahlung buchen** aus.  

Die eingegebene Zahlungsinformation ist für Belege gebucht, die durch Zeilen dargestellt werden, in denen das Kontrollkästchen **Zahlung erhalten** aktiviert ist.  

Zahlungsposten werden in der Finanzbuchhaltung, Bank und in Debitorenkonten gebucht. Jede Zahlung wird für den entsprechenden gebuchten Verkaufsbeleg angewandt.  

## <a name="to-reconcile-lump-sum-payments"></a>Pauschalzahlungen verarbeiten
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Zahlungsregistrierung** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie das Kontrollkästchen **Zahlung erfolgt** in der Zeile, die die gebuchten Belege für denselben Debitor darstellen, für den eine Pauschalzahlung gemacht wurde.  

    > [!NOTE]  
    >   Der Debitor im Feld **Name** muss der Gleiche in allen Zeilen sein, die als Pauschalzahlung gebucht werden.  

    Wenn das Kontrollkästchen **Automatische Datumseingabe** auf der Seite **Einrichtung der Zahlungserfassung** aktiviert ist, wird das Arbeitsdatum im Feld **Empfangsdatum** ausgefüllt.  
3. Geben Sie im Feld **Empfangsdatum** das Datum ein, an dem die Zahlung gemacht wurde. Dieses Datum kann vom Arbeitsdatum abweichen.  

    > [!NOTE]  
    >   Dieses Datum muss das gleiche in allen Zeilen sein, die als Pauschalzahlung gebucht werden.  
4. Geben Sie im Feld **Betrag erhalten** die Beträge in mehreren Zeilen ein, die den einmaligen Zahlungsbetrag zusammenfassen.  

    > [!TIP]  
    > Versuchen Sie, mit dem Pauschalbetrag so viele volle Zahlungen wie möglich zu buchen. Geben Sie Beträge auf so viele Zeilen wie möglich ein, die dieselben sind, wie der Betrag im Feld **Verbleibender Betrag**.  
5. Wiederholen Sie die Schritte 2-4 für andere Zeilen, die für gebuchte Belege für denselben Debitor stehen, für den eine Pauschalzahlung geleistet wurde.  
6. Wählen Sie die Aktion **Als einmalige Zahlung buchen** aus. Die eingegebene Zahlungsinformation ist für Belege gebucht, die durch Zeilen dargestellt werden, in denen das Kontrollkästchen **Zahlung getätigt** aktiviert ist.  

Zahlungseingänge werden in Finanzbuchhaltung, Bank und in Debitorenkonten gebucht. Jede Zahlung wird für den entsprechenden gebuchten Verkaufsbeleg angewandt.  

Wenn eine Zahlung in der Bank nicht durch Zeile auf der Seite **Zahlungserfassung** angegeben wird, kann dies sein, da der zugehörige Beleg noch nicht gebucht wurde. In diesem Fall können Sie eine Suchfunktion verwenden, um den Beleg zu buchen und schnell zu suchen, um die Zahlung zu verarbeiten. Weitere Informationen finden Sie unter [Bestimmten Verkaufsbeleg suchen, der nicht vollständig fakturiert wurde](#to-find-a-specific-sales-document-that-isnt-fully-invoiced).  

Wenn eine Zahlung in der Bank nicht durch einen Beleg in [!INCLUDE[prod_short](includes/prod_short.md)] angegeben wird, dann können Sie eine Fibu Buch.-Blattzeile aus der Seite **Zahlungserfassung** öffnen, um die Zahlung direkt auf das Hauptkonto zu buchen, ohne die Zahlung auf einen Beleg anzuwenden. Alternativ können Sie die Zahlung im Buch.-Blatt buchen, bis der Ursprung der Zahlung gelöst wurde. Weitere Informationen finden Sie im Abschnitt [Zahlung ohne zugehörigen Beleg erfassen oder buchen](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-record-or-post-a-payment-without-a-related-document).  

## <a name="to-process-customer-payments-with-discounts-manually"></a>Vorgehensweise: Manuelle Verarbeitung von Zahlungen mit Rabatten
Wenn Sie ein Skonto mit dem Debitor vereinbart haben, können die Zahlungsbeträge niedriger als die fakturierten Beträge sein, wenn die Zahlung vor dem vereinbarten Skontodatum auftritt.  

Dieses Thema erläutert vier verschiedene Verfahren zum Buchen von verbilligten Zahlungen auf der Seite **Zahlungserfassung**.  

* Der Zahlungsbetrag entspricht dem diskontierten Betrag und dessen Zahlungsdatum liegt vor dem Skontodatum. Sie buchen die Zahlung, wie sie ist.  
* Der Zahlungsbetrag entspricht dem diskontierten Betrag, aber dessen Zahlungsdatum liegt nach dem Skontodatum. Sie buchen die Zahlung als Teilzahlung. Der Beleg bleibt offen, um den Restbetrag einzufordern/zu bezahlen. Sie können das Skontodatum später festlegen, um die vollständige Bezahlung zu ermöglichen.  
* Die Zahlungssumme ist niedriger als der verbleibende diskontierte Betrag. Sie buchen die Zahlung als Teilzahlung. Der Beleg bleibt offen, um den Restbetrag einzufordern/zu bezahlen.  
* Die Zahlungssumme ist höher als der verbleibende diskontierte Betrag. Sie buchen die Zahlungen, wie sie sind. Nur der Restbetrag wird gebucht. Der extra Betrag wird dem Debitor gutgeschrieben.  

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-and-where-the-payment-date-is-before-the-discount-date"></a>Zahlungsbetrag verarbeiten, der dem diskontierten Betrag entspricht und dessen Zahlungsdatum vor dem Skontodatum liegt
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Zahlungsregistrierung** ein und wählen Sie dann den zugehörigen Link.  
2. Geben Sie den Zahlungsbetrag im Feld **Betrag erhalten** ein. Der Betrag ist gleich wie der Betrag im Feld **Restbetrag nach Rabatt**.

    Das Kontrollkästchen **Zahlung erfolgt** wird automatisch aktiviert, und das Feld **Empfangsdatum** wird mit dem Arbeitsdatum ausgefüllt.    
3. Geben Sie im Feld **Datum erhalten** das Zahlungsdatum ein. Das Datum steht vor dem Datum im Feld **Skontodatum**.
4. Vergewissern Sie sich, dass das Feld **Restbetrag** den Wert Null (0) enthält.  
5. Wählen Sie auf der Registerkarte **Zahlung buchen**, um den Gesamtbetrag auf Sach-, Bank- und Debitorenkonten zu buchen.

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-but-where-the-payment-date-is-after-the-discount-date"></a>Zahlungsbetrag verarbeiten, der dem diskontierten Betrag entspricht, dessen Zahlungsdatum jedoch nach dem Skontodatum liegt
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Zahlungsregistrierung** ein und wählen Sie dann den zugehörigen Link.  
2. Geben Sie den Zahlungsbetrag im Feld **Betrag erhalten** ein. Der Betrag ist gleich wie der Betrag im Feld **Restbetrag nach Rabatt**.

    Das Kontrollkästchen **Zahlung erfolgt** wird automatisch aktiviert, und das Feld **Empfangsdatum** wird mit dem Arbeitsdatum ausgefüllt.
3. Geben Sie im Feld **Eingangsdatum** ein Zahlungsdatum an, das nach dem Datum im Feld **Skontodatum** liegt. Datumsfelder ändern zu roter Schrift, und eine Fehlermeldung wird unten auf der Seite angezeigt.

    > [!TIP]  
    >   Wenn Sie eine Ausnahme erstellen möchten und den Rabatt gewähren, selbst wenn die Zahlung spät ist, dann führen Sie die folgenden Schritte durch:
4. Wählen Sie die Aktion **Details** aus.  
5. Geben Sie auf der Seite **Zahlungserfassungsdatum** im Feld **Skontodatum** im Inforegister **Skonto** ein Datum ein, das nach dem **Empfangsdatum** im Feld **Zahlungserfassung** liegt.  

    Die Fehlermeldung und die rote Schriftart verschwinden, und Sie können fortfahren, die verbilligte Zahlung zu bearbeiten.    
6. Vergewissern Sie sich, dass das Feld **Restbetrag** den Betrag enthält, der verbleibt, um den vollständigen Rechnungsbetrag zu bezahlen.  
7. Wählen Sie die Aktion **Zahlung buchen**, um den Teilbetrag auf Sach-, Bank- und Debitorenkonten zu buchen.  

Der zugehörige Beleg bleibt offen.

### <a name="to-process-a-payment-that-is-lower-than-the-remaining-discounted-amount"></a>Zahlung verarbeiten, die niedriger als der verbleibende diskontierte Betrag ist
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Zahlungsregistrierung** ein und wählen Sie dann den zugehörigen Link.  
2. Geben Sie den Zahlungsbetrag im Feld **Betrag erhalten** ein. Der Betrag ist kleiner als der Betrag im Feld **Restbetrag nach Rabatt**.

    Das Kontrollkästchen **Zahlung erfolgt** wird automatisch aktiviert, und das Feld **Empfangsdatum** wird mit dem Arbeitsdatum ausgefüllt.  
3. Geben Sie im Feld **Datum erhalten** das Zahlungsdatum ein. Das Datum steht vor dem Datum im Feld **Skontodatum**.
4. Vergewissern Sie sich, dass das Feld **Restbetrag** den Betrag enthält, der verbleibt, um den rabattierten Rechnungsbetrag zu bezahlen.  
5. Wählen Sie die Aktion **Zahlung buchen**, um den Teilbetrag auf Sach-, Bank- und Debitorenkonten zu buchen.  

Der zugehörige Beleg bleibt offen.

### <a name="to-process-a-payment-that-is-more-than-the-remaining-discounted-amount"></a>Zahlung verarbeiten, die höher als der verbleibende diskontierte Betrag ist
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Zahlungsregistrierung** ein und wählen Sie dann den zugehörigen Link.  
2. Geben Sie den Zahlungsbetrag im Feld **Betrag erhalten** ein. Der Betrag ist grösser als der Betrag im Feld **Restbetrag nach Rabatt**.  

    Das Kontrollkästchen **Zahlung erfolgt** wird automatisch aktiviert, und das Feld **Empfangsdatum** wird mit dem Arbeitsdatum ausgefüllt.    
3. Geben Sie im Feld **Datum erhalten** das Zahlungsdatum ein. Das Datum steht vor dem Datum im Feld **Skontodatum**.
4. Vergewissern Sie sich, dass das Feld **Restbetrag** den Wert Null (0) enthält.  
5. Wählen Sie auf der Registerkarte **Zahlung buchen**, um den Gesamtbetrag auf Sach-, Bank- und Debitorenkonten zu buchen.  

Der zugehörige Beleg ist abgeschlossen, und dem Debitor wird der Überzahlungsbetrag gutgeschrieben.  

## <a name="to-find-a-specific-sales-document-that-isnt-fully-invoiced"></a>Bestimmten Verkaufsbeleg suchen, der nicht vollständig fakturiert wurde
Die Seite **Zahlungserfassungs** unterstützt Sie bei Aufgaben, die interne Konten mit tatsächlichen Bargeldabbildungen ausgleichen müssen, um die effektive Sammlung von Debitoren sicher zu stellen. Es zeigt ausstehende eingehende Zahlungen als Zeilen an, welche Verkaufsbelege darstellen, in denen ein Betrag zur Zahlung fällig ist.  

Wenn eine Zahlung erfolgt ist, auf der Bank oder anderweitig verzeichnet wurde, wird normalerweise der zugehörige Verkaufs- oder Einkaufsbeleg als Zeile auf der Seite **Zahlungserfassung** dargestellt, da für den betreffenden Beleg die Zahlung noch für den ausstehenden Betrag gebucht werden muss. Manchmal wird jedoch eine Zahlung, die geleistet wurde, nicht durch eine Zeile auf der Seite **Zahlungserfassung** dargestellt, da der jeweilige Beleg üblicherweise nicht vollständig fakturiert wurde.

Auf der Seite **Dokument suchen** können Sie aus Belegen suchen, die nicht vollständig fakturiert wurden. Sie können basierend auf einer oder mehrerer der folgenden Kriterien suchen:  

* Belegnummer  
* Betrag oder Betragsbereich  

Nachfolgend wird erklärt, wie man einen bestimmten Beleg findet, indem man beide Suchkriterien verwendet.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Zahlungsregistrierung** ein und wählen Sie dann den zugehörigen Link.
2. Zeigen Sie mit dem Mauszeiger auf eine beliebige Zeile und wählen Sie **Dokument suchen**.
3. Auf der Seite **Dokumentsuche** geben Sie einen Suchwert im Feld **Dokumentennummer** ein.  

    > [!NOTE]  
    >   Der Wert, den Sie hier eingeben, ist in den ausgeblendeten Platzhalterzeichen enthalten. Das bedeutet, dass die Funktion in allen Belegnummern sucht, die den eingegebenen Wert enthalten.    
4. Geben Sie in dem Feld **Betrag** den entsprechenden Betrag ein, der auf dem Beleg vorhanden ist, den Sie finden möchten.  
5. Geben Sie im Feld **Betragsabwicklung in %** einen Prozentwert ein, um den Bereich von Beträgen zu definieren, die Sie sehen möchten, um den offenen Beleg zu finden.  

    Wenn Sie 10 eingeben, dann sucht die Funktion nach Beträgen in einem Bereich zwischen zehn Prozent unter und zehn Prozent über dem Feld **Betrag**.    
6. Wählen Sie die Aktion **Suchen** aus.  

Die Suchfunktion sucht unter Belegen, die nicht vollständig fakturiert sind basierend auf den angegebenen Kriterien.  

Wenn einer oder mehrere Belege mit den Suchkriterien im Feld **Ergebnis Dokumentsuche** übereinstimmen, dann öffnet sich die Seite, um Zeilen anzuzeigen, die diese Dokumente darstellen. Jede Zeile enthält eine Belegnummer, eine Beschreibung und einen Betrag. Diese Informationen erleichtern das Auffinden eines bestimmten Dokuments.

Wenn eine Zahlung in der Bank nicht durch einen Beleg in [!INCLUDE[prod_short](includes/prod_short.md)] angegeben wird, dann können Sie eine Fibu Buch.-Blattzeile aus der Seite **Zahlungserfassung** öffnen, um die Zahlung direkt auf das Hauptkonto zu buchen, ohne die Zahlung auf einen Beleg anzuwenden. Alternativ können Sie die Zahlung im Buch.-Blatt buchen, bis der Ursprung der Zahlung gelöst wurde.  

## <a name="to-record-or-post-a-payment-without-a-related-document"></a>Zahlung ohne zugehörigen Beleg erfassen oder buchen
Wenn eine Zahlung in der Bank nicht durch einen Beleg in [!INCLUDE[prod_short](includes/prod_short.md)] angegeben wird, dann können Sie eine Fibu Buch.-Blattzeile aus der Seite **Zahlungserfassung** öffnen, um die Zahlung direkt auf das Hauptkonto zu buchen, ohne die Zahlung auf einen Beleg anzuwenden. Alternativ können Sie die Zahlung im Buch.-Blatt buchen, bis der Ursprung der Zahlung geklärt wurde.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Zahlungsregistrierung** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Fibu Buch.-Blatt** aus.  

    Die Seite **Fibu Buch.-Blatt** wird mit einer Zeile geöffnet, die das Saldokonto des Buch.-Blatts enthält, das auf der Seite **Zahlungserfassungs-Einrichtung** festgelegt ist.  
3. Füllen Sie die übrigen Felder jeder Fibu Buch.-Blattzeile aus. Geben Sie beispielsweise den Betrag, die Debitorennummer oder Informationen aus dem Kontoauszug an. Weitere Informationen finden Sie unter [Transaktionen direkt in der Finanzbuchhaltung buchen](finance-how-post-transactions-directly.md).  

Sie können die Buch.-Blattzeile buchen, um die Summe in dem Gegenkonto zu aktualisieren. Alternativ können Sie die Buch.-Blattzeile ungebucht lassen und fügen ggf. mit einer Notiz an, dass die Zahlung mehr Analyse benötigt.  

Wenn Sie die Buch.-Blattzeile nicht buchen lassen, wird der Wert im Feld **Ungebuchter Saldo** am unteren Rand der Seite **Zahlungserfassung** hinzugefügt.  

## <a name="see-also"></a>Weitere Informationen
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
