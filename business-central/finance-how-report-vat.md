---
title: Senden Sie Umsatzsteuerberichte an die Steuerbehörden
description: 'Erfahren Sie, wie Sie Berichte erstellen, in denen die Mehrwertsteuer aus Verkäufen während eines Zeitraums oder aus Verkäufen und Käufen aufgeführt ist, und wie Sie den Bericht an eine Steuerbehörde übermitteln.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'VAT, tax, report, EC sales list, statement'
ms.search.form: '321, 322, 323, 474, 475, 739, 740, 741, 742, 743, 744, 745, 746, 747, 748, 9401'
ms.date: 08/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="report-vat-to-tax-authorities"></a>Melden Sie die Umsatzsteuer an die Steuerbehörden

In diesem Artikel werden die Berichte beschrieben, mit denen Sie Informationen zu Mehrwertsteuerbeträgen (MwSt.) für Verkäufe und Käufe an die Steuerbehörden Ihrer Region übermitteln können. [!INCLUDE[prod_short](includes/prod_short.md)]  Je nach Land/Region enthalten die Berichte möglicherweise spezifische Informationen oder es müssen zusätzliche Berichte übermittelt werden. Überprüfen Sie die Artikel für Ihr Land/Ihre Region im Abschnitt [Lokale Funktionen](about-localization.md).  

Es können die folgenden integrierten Berichte verwendet werden:

* Der **„EU-Verkaufsübersicht“**-Bericht  

    Der „EU-Verkaufsübersicht“-Bericht führt MwSt.-Beträge der Europäischen Union (EU) auf, die Sie für Verkäufe an für MwSt. registrierte Debitoren in den Ländern/Regionen der EU eingetrieben haben.  
* Der Bericht **MwSt.-Rückgabe**  

    Der Bericht „MwSt.-Rückgabe“ enthält die MwSt. für Verkäufe und Einkäufe an Debitoren und von Kreditoren in allen Ländern/Regionen, die MwSt. verwenden.  

In beiden Fällen wird die Mehrwertsteuer (wie in anderen MwSt.-bezogenen Berichte) auf der Grundlage der MwSt.-Buchungseinrichtung und der MwSt.-Buchungsgruppen, die Sie festgelegt haben, berechnet. [!INCLUDE[prod_short](includes/prod_short.md)] zeigt MwSt.-Posten immer auf Basis ihres **MwSt.-Datum** als primäres Meldungsdatum.  

> [!NOTE]
> Alle MwSt-bezogene Berichte werden jetzt mit dem **MwSt.-Datum** ausgeführt, um relevante Datensätze zu filtern. Auch wenn Sie **Verwendung des MwSt.-Datums** auf **Die MwSt.-Datum-Funktion nicht verwenden** festgelegt haben, blendet [!INCLUDE[prod_short](includes/prod_short.md)] alle Instanzen von **MwSt.-Datum** über die Anwendung aus. Allerdings wird das **MwSt.-Datum** weiterhin in allen Berichten verwendet und das **Buchungsdatum** wird automatisch eingetragen.

Wenn Sie den gesamten Verlauf von MwSt.-Posten anzeigen möchten, erstellt jede Buchung, die Mehrwertsteuer beinhaltet, einen Posten auf der Seite **MwSt.-Posten**. Diese Posten werden verwendet, um Ihren MwSt.-Abrechnungsbetrag (Ihrer Zahlung oder Erstattung) für eine bestimmte Periode zu berechnen. Um MwSt.-Posten einzusehen, wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **MwSt.-Posten** ein und wählen Sie dann den entsprechenden Link.

> [!NOTE]
> Jede [!INCLUDE[prod_short](includes/prod_short.md)]-Umgebung soll die gesetzlich vorgeschriebene Berichterstellung in einem einzigen Land bzw. einer einzigen Region handhaben. Die niederländische Version von [!INCLUDE[prod_short](includes/prod_short.md)] handhabt MwSt-Berichterstellung beispielsweise in den Niederlanden, jedoch nicht in anderen Ländern/Regionen. In ähnlicher Weise handhabt die US-Version von [!INCLUDE[prod_short](includes/prod_short.md)] Steuererklärungen (US 1099) in den USA und unterstützt nicht die Geltendmachung von MwSt-Berichten in anderen Ländern/Regionen, es sei denn, sie wird durch eine von unserem Partner-Ökosystem gelieferte Erweiterung oder eine kundenspezifische Code-Modifikation eingeführt.

## <a name="about-the-ec-sales-list-report"></a><a name="ecsaleslist"></a>Info über den „EU-Verkaufsübersicht“-Bericht

In der Europäischen Union (EU) und im Vereinigten Königreich müssen alle Unternehmen, die Waren und Dienstleistungen an mehrwertsteuerlich registrierte Debitoren verkaufen, einschließlich Debitoren in anderen Ländern/Regionen der Europäischen Union (EU), eine elektronische Version der EU-Verkaufsübersicht an ihre Zoll- und Steuerbehörden senden. Der **EU-Verkaufsübersicht**-Bericht funktioniert nur für Länder/Regionen in der EU.

Der Bericht enthält eine Zeile für jede Art Transaktion mit dem Debitor und zeigt den Gesamtbetrag für jede Art von Transaktionen an. Es gibt drei Arten von Transaktionen, die der Bericht enthalten kann:  

* B2B-Waren  
* B2B-Dienste  
* Triangulierte Waren B2Bs  

*B2B* Waren und Dienstleistungen geben an, ob Sie eine Ware oder eine Dienstleistung verkauft haben, und werden über die Einstellung **EU Service** in der MwSt.-Buchungseinrichtung festgelegt. *B2B-Dreieckswaren* zeigen an, ob Sie mit einer dritten Partei Handel getrieben haben, und werden durch die Einstellung **EU 3-Parteien-Handel** auf Verkaufsbelegen wie Verkaufsaufträgen, Rechnungen, Gutschriften usw. festgelegt.  

Nachdem die Steuerbehörde Ihren Bericht geprüft hat, sendet sie eine E-Mail an die Kontaktperson Ihres Unternehmens. In [!INCLUDE[prod_short](includes/prod_short.md)], wird die Kontaktperson auf der Seite **Firmendaten** angegeben. Bevor Sie den Bericht senden, prüfen Sie, ob eine Kontaktperson ausgewählt ist.  

### <a name="submit-an-ec-sales-list-report"></a>Einen „EU-Verkaufsübersicht“-Bericht übermitteln

[!INCLUDE [finance-ecsaleslist](includes/finance-ecsaleslist.md)]

## <a name="about-the-vat-return-report"></a><a name="vatreturn"></a>Informationen zum MwSt.-Rückgabebericht

Verwenden Sie diesen Bericht, um MwSt. für Einkaufs- und Verkaufsbelege zu senden, wie Bestellungen und Verkaufsaufträge, Rechnungen und Gutschriften. Die Informationen dieses Berichts haben dabei dasselbe Format wie die Formulare der Finanz- und Steuerbehörden.  

Für die Mehrwertsteuerrückgabe können Sie die Posten angeben, die berücksichtigt werden sollen:

* Buchen Sie nur offene Transaktionen oder geöffnete und geschlossene. Dies ist beispielsweise dann nützlich, wenn Sie die abschließende jährliche Mehrwertsteuerrückgabe vorbereiten.
* Buchen Sie nur Posten aus den angegebenen Zeiträumen, oder aktualisieren Sie auch Posten aus den vorherigen Perioden. Dies dient zum Aktualisieren der Mehrwertsteuerrückgabe, die Sie bereits gebucht haben, wenn zum Beispiel ein Kreditor eine verspätete Rechnung sendet.    

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Um sich mit der Webdienst Ihrer Steuerbehörde zu verbinden
[!INCLUDE[prod_short](includes/prod_short.md)] stellt die Dienst-Verbindungen für Steuerbehördenwebsites bereit. Wenn Sie beispielsweise im Vereinigten Königreich sind, können Sie die **GovTalk**-Dienst-Verbindung ausführen, um die EU-Verkaufsübersicht und MwSt.-Rückgabeberichte elektronisch zu senden. Wenn Sie die Meldung manuell abgeben möchten, etwa indem Sie Ihre Daten auf der Internetseite des Finanzamts eingeben, ist dies nicht erforderlich.   

Um MwSt an eine Steuerbehörden zu übermitteln, müssen Sie den [!INCLUDE[prod_short](includes/prod_short.md)] mit der Steuerbehörde verbinden. Dazu ist es erforderlich, dass Sie ein Konto mit Ihrer Steuerbehörden einrichten. Wenn Sie ein Konto haben, können Sie eine Dienst-Verbindung ausführen, die wir in [!INCLUDE[prod_short](includes/prod_short.md)] voraussetzen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 2.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Dienstverbindungen** ein und wählen Sie dann den entsprechenden Link.
2. Füllen Sie die entsprechenden Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > Es ist empfehlenswert, die Verbindung zu testen. Aktivieren Sie dazu das Kontrollkästchen **Testmodus** und senden Sie Ihren MwSt.-Bericht wie im Abschnitt [So erstellen und senden Sie einen MwSt.-Bericht](#to-prepare-and-submit-a-vat-report) beschrieben. Im Testmodus testet der Dienst, ob die Steuerbehörden den Bericht erhalten, und der Status des Berichts gibt an, ob die Testübermittlung erfolgreich war. Denken Sie daran, dass dies keine tatsächliche Datenübermittlung ist. Um den tatsächlichen Bericht zu senden, müssen Sie das Feld **Testmodus** deaktivieren und dann den Übermittlungsvorgang wiederholen.

## <a name="to-set-up-vat-reports-in-"></a>Einrichten von MwSt.-Berichten in [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE [vat-report-setup](includes/vat-report-setup.md)]

### <a name="to-set-up-vat-return-periods"></a>So legen Sie die Perioden für die Umsatzsteuererklärung fest

Wenn Ihr Unternehmen nicht im Vereinigten Königreich ansässig ist, können Sie optional die Seite  **Umsatzsteuererklärungszeiträume**  verwenden, um geplante Umsatzsteuererklärungen einzurichten. Wenn Ihr Unternehmen im Vereinigten Königreich ansässig ist, lesen Sie  [Making Tax Digital in the United Kingdom](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md).  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Mehrwertsteuer-Rückgabeperioden** ein und wählen Sie dann den zugehörigen Link.  
2. Auf der Seite **Mehrwertsteuer-Rückgabeperioden** füllen Sie die Felder aus, um die erste Periode festzulegen. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)].  
3. Wiederholen Sie Schritt 2 für alle weiteren Perioden, die Sie hinzufügen möchten.  

Wenn es nun an der Zeit ist, einen MwSt.-Bericht für einen MwSt.-Berichtszeitraum zu senden, wählen Sie den Zeitraum auf der Seite **MwSt.-Rückgabezeiträume** aus und wählen Sie dann die Aktion **MwSt.-Bericht erstellen**. Wählen Sie dann auf der Karteikarte **Mehrwertsteuerrückerstattung** die Aktion **Zeilen vorschlagen**, wie in Schritt 3 des folgenden Verfahrens beschrieben.  

## <a name="to-prepare-and-submit-a-vat-report"></a>Vorbereiten und Übermitteln eines MwSt.-Berichts

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 3.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie  **EG-Verkaufsliste**  oder  **Mehrwertsteuererklärungen** ein und wählen Sie dann das zugehörige verknüpfen aus.  
2. Wählen Sie Aktion **Neu** aus, und füllen Sie die relevanten Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Um den Inhalt des Berichts zu erstellen, wählen Sie die **Vorschlagszeilen** Aktion.  

    > [!NOTE]  
    >  Für den EU-Verkaufsübersicht-Bericht können Sie Transaktionen überprüfen, die in den Berichtszeilen enthalten sind, bevor Sie den Bericht senden. Wählen Sie die Zeile mit der Verteilung, und wählen Sie dann die Aktion **MwSt-Einträge anzeigen** aus.  

4. Um einen Bericht für die Übermittlung zu überprüfen und vorzubereiten, wählen Sie die **Freigabe**-Aktion.  

    > [!NOTE]  
    > [!INCLUDE[prod_short](includes/prod_short.md)] prüft, ob der Bericht korrekt eingerichtet ist. Wenn die Prüfung fehlschlägt, werden die Fehler im Fenster **Fehler und Warnungen** angezeigt, sodass Sie entsprechende Änderungen vornehmen können. Wenn die Meldung zu einer fehlenden Einstellung in [!INCLUDE[prod_short](includes/prod_short.md)] erfolgt, können Sie auf die Nachricht klicken, um die Seite zu öffnen, die die Informationen zur Korrektur enthält.  
5. Um den Bericht zu buchen, wählen Sie die **Übermitteln** Aktion.  

Nachdem Sie den Bericht gesendet haben, überwacht [!INCLUDE[prod_short](includes/prod_short.md)] den Service und bewahrt einen Datensatz Ihrer Kommunikation auf. Das Feld **Status** gibt an, wo der Bericht in Bearbeitung ist. Beispielsweise wenn die Behörden Ihren Bericht verarbeiten, ändert sich der Status des Berichts auf **Erfolgreich**. Wenn die Steuerbehörde Fehler im Bericht finden, erhält der Bericht den Status **Fehler**. Sie können die Fehler unter **Fehler und Warnungen** anzeigen, korrigieren und den Bericht erneut senden. Um eine Liste Ihrer EU-Verkaufsübersichts-Berichte anzuzeigen, wechseln Sie zur Seite **EU-Verkaufsübersichts-Berichte**.  

### <a name="vat-return-statuses"></a>MwSt.-Rückgabestatus

MwSt.-Rückgaben können, wie in der folgenden Tabelle beschrieben, unterschiedliche Status haben.

| Status | Beschreibung |
|------------|-------------------------|
| Öffnen | Wenn Sie eine neue MwSt.-Rückgabe erstellen. Sie können die Aktion **Zeilen vorschlagen** ausführen. Wenn Sie Werte korrigieren müssen, können Sie die Aktion **Zeilen vorschlagen** wieder ausführen. Sie können keine MwSt.-Rückgabe mit diesem Status einreichen. |
| Freigegeben | Der Status wird geändert, wenn Sie die Aktion **Freigeben** verwenden. [!INCLUDE[prod_short](includes/prod_short.md)] zeigt das Inforegister **Fehler und Warnungen** an. Sie können keine Änderungen vornehmen oder die Aktion **Zeilen vorschlagen** verwenden. Um Änderungen vorzunehmen, müssen Sie die MwSt.-Rückgabe erneut öffnen. |
| Abgelehnt | Wenn Ihre Übermittlung nicht erfolgreich war (z. B. wenn die Authentifizierung fehlgeschlagen ist), ändert sich der Status in  **Abgelehnt**. Sie können eine MwSt.-Rückgabe mit diesem Status nicht erneut öffnen. |
| Übermittelt | Die MwSt.-Rückgabe wird mit der Aktion **Einreichen** eingereicht oder es wird mithilfe der Aktion **Als „Übermittelt“ markieren** als übermittelt markiert. |
| Angenommen | Die Umsatzsteuererklärung hat diesen Status, wenn der Bericht mit der Aktion  **Als akzeptiert markieren**  als akzeptiert markiert wird. Wenn der Bericht **MwSt.-Rückgabe** als **Angenommen** markiert wird, können Sie die Aktion **MwSt. abrechnen und buchen** ausführen. |

## <a name="viewing-communications-with-your-tax-authority"></a>Zeigt den Verlauf der Kommunikation mit der Steuerbehörde an

In einigen Ländern/Regionen tauschen Sie Meldungen mit Steuerbehörden aus, wenn Sie Berichte senden. Sie können die erste und letzte Meldung anzeigen, die Sie gebucht oder erhalten haben, indem Sie die Aktionen **Übermittlungsnachricht herunterladen** und **Antwornachricht herunterladen** gewählt haben.  

## <a name="submitting-vat-reports-manually"></a>Manuelles Senden von MwSt.-Berichten
Wenn Sie eine andere Methode verwenden, um den Bericht zu buchen, indem Sie beispielsweise die XML exportieren und sie in eine Steuerbehördenwebsite, können Sie sie danach **als übermittet markieren**, um den Berichtszeitraum zu schließen. Wenn Sie den Bericht als freigegeben kennzeichnen, ist er nicht mehr editierbar. Wenn Sie die Erklärung ändern müssen, nachdem Sie sie als freigegeben gekennzeichnet haben, müssen Sie sie zuerst erneut öffnen.

## <a name="vat-settlement"></a>MwSt.-Abrechnung
Die Netto-MwSt. muss in regelmäßigen Abständen an die Steuerbehörden überwiesen werden. Bei häufigen MwSt.-Abrechnungen können Sie die Stapelverarbeitung **MwSt. abrechnen und buchen** ausführen, um die offenen MwSt.-Posten abzuschließen und die MwSt.-Beträge für Einkäufe und Verkäufe an das MwSt.-Abrechnungskonto zu übertragen.

Die Übertragung von MwSt.-Beträgen auf Abrechnungskonten bedeutet, dass das Vorsteuerkonto im Haben und das Umsatzsteuerkonto im Soll mit den für die angegebene Abrechnungsperiode berechneten Beträge bebucht wird. Der Nettobetrag wird als Haben auf das MwSt.-Ausgleichskonto gebucht (oder als Soll, wenn der Einkaufs-MwSt.-Betrag größer ist). Sie können die Abrechnung unmittelbar buchen oder erst einen Testbericht ausdrucken.  

> [!Note]
> Wenn Sie die Stapelverarbeitung **MwSt. abrechnen und buchen** verwenden und keine **MwSt.-Geschäftsbuchungsgruppe** und **MwSt.-Produktbuchungsgruppe** angeben, werden Posten mit den Geschäftsbuchungsgruppen und Produktbuchungsgruppencodes einbezogen.

## <a name="configuring-your-own-vat-reports"></a>MwSt-Bericht konfigurieren

Sie können den **EU-Verkaufsübersicht**-Bericht ohne Änderungen nutzen. Sie können jedoch auch eigene Berichte erstellen, wenn Sie über eine Entwicklungslizenz verfügen, mit der Sie Codeunits erstellen können. Wenn Sie Hilfe benötigen, wenden Sie sich an einen Microsoft Partner.  

Die folgende Tabelle beschreibt Codeunits, die Sie für den Bericht erstellen müssen.  

| Codeunit | Was sie tun müssen |
|----|-----|
|Vorschlagszeilen| Holen Sie Informationen aus der Tabelle **MwSt.-Posten** und zeigen Sie sie in Zeilen auf dem MwSt.-Bericht an.|
|Inhalt | Kontollieren Sie das Format des Berichts. Beispielsweise, ob es XML oder JSON ist. Das Format, das zu verwenden ist, hängt von den Anforderungen des Webdiensts Ihrer Steuerbehörden ab. |
|Übermittlung | Steuern Sie, wie und wann Sie den Bericht basierend auf den Anforderungen Ihrer Steuerbehörden senden. |
|Antwort-Handler | Bearbeit die Antwort der Steuerbehörden. Beispielsweise sendet sie eine E-Mail an die Kontaktperson Ihres Mandanten. |
|Abbrechen | Senden Sie eine Stornierung eines MwSt-Berichts, der zuvor zu Ihrer Steuerbehörden gesendet wurde. |  

> [!Note]
> Wenn Sie Codeunits für den Bericht erstellen, achten Sie auf den Wert im Feld **Version des MwSt.-Berichts**. Dieses Feld muss der Version des Berichts entsprechen, der von der Steuerbehörde verlangt wurde oder verlangt wird. Beispielsweise können Sie **2021** in dieses Feld eingeben, um anzugeben, dass der Bericht der Anforderungen entspricht, die im letzten Jahr verlangt wurden. Um die aktuellen Version zu finden, setzen Sie sich mit den Steuerbehörden in Verbindung.  

## <a name="see-also"></a>Siehe auch

[Berechnungen und Buchungsmethoden für die Mehrwertsteuer einrichten](finance-setup-vat.md)    
[Arbeiten mit MwSt im Verkauf und Einkauf](finance-work-with-vat.md)    
[Verkauf einrichten](sales-setup-sales.md)    
[Fakturieren eines Verkaufs](sales-how-invoice-sales.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]
