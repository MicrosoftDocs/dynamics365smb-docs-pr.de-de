---
title: Zusätzliche Währungen einrichten
description: 'Ihre Finanzbuchhaltung wird in der lokalen Wählrung (LW) eingerichtet. Sie können eine weitere Währung einrichten, der Sie einen aktuellen Wechselkurs zuweisen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'multiple currencies, foreign exchange rates'
ms.search.form: '5, 16,118, 483, 495'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# <a name="set-up-an-additional-reporting-currency"></a>Berichtswährung einrichten

Da die Anzahl der Länder, in denen Unternehmen Geschäftsbeziehungen unterhalten, ständig wächst, wird es immer wichtiger, dass Finanzdaten in mehreren Währungen erfasst und angezeigt werden können.

> [!NOTE]  
> Wenn Sie in [!INCLUDE[prod_short](includes/prod_short.md)] nach Echtzeitinformationen zu Wechselkursen (FX) oder älteren Kursen suchen, werden diese als Währung bezeichnet. Siehe neben diesem Artikel auch [Währungswechselkurse aktualisieren](finance-how-update-currencies.md).

In der Anwendung wird die Finanzbuchhaltung in der Mandantenwährung (MW) eingerichtet. Eine weitere Währung, der ein aktueller Wechselkurs zugewiesen ist, wird als zusätzliche Währung eingerichtet. Wenn Sie eine zweite Währung als Berichtswährung (BW) festlegen, erfasst [!INCLUDE[prod_short](includes/prod_short.md)] automatisch Beträge sowohl in MW als auch in BW bei jedem Sachposten und anderen Buchungen, z. B. bei der Mehrwertsteuer.

> [!Warning]
> Sie sollten die BW-Funktion nicht als Grundlage für die Umrechnung von Finanzauswertungen verwenden, es sei denn, Sie sind sich ihrer Einschränkungen bewusst. Es kann keine Finanzauswertungen von ausländischen Niederlassungen im Rahmen einer Unternehmenskonsolidierung durchführen. Die BW kann nur verwendet werden, um Berichte in einer anderen Währung zu erstellen, so als ob diese Währung die LW des Unternehmens wäre.
>
> Sie haben z.B. eine große Menge an Debitoren in Britischen Pfund (GBP) und Sie haben Ihre zusätzliche BW auf GBP festgelegt. In diesem Szenario werden die Beträge in den Debitoren, die GBP verwenden, nicht um Wechselkursgewinne/-verluste im ACY bereinigt, sondern nur die Beträge in den Debitoren, die in anderen Währungen sind. Das bedeutet, dass, wenn Sie ACY verwenden, um Ihren Jahresabschluss zu erstellen, dies zu unter- oder überbewerteten ausstehenden Salden der Debitoren führen kann.

## <a name="displaying-reports-and-amounts-in-acy"></a>Berichte und Beträge in BW anzeigen

Eine BW kann in folgenden Fällen für das Berichtswesen eines Unternehmens hilfreich sein:

- Unternehmen in nicht-EU-Ländern/-Regionen mit einem hohen Anteil von Transaktionen mit Unternehmen in EU-Ländern/-Regionen. In diesem Fall möchte das Nicht-EU-Unternehmen seine Berichte möglicherweise ebenfalls in Euro erstellen, damit diese für die Handelspartner in der EU besser nutzbar sind.
- Unternehmen, die Berichte in einer international gehandelten Währung anzeigen möchte, wenn dies auf deren Landeswährung nicht zutrifft.

Einige Finanzberichte basieren auf Sachposten. Um die Finanzdaten in dem Bericht in der BW anzuzeigen, wählen Sie das Kontrollkästchen **Beträge in Berichtswährung ausgeben** im Inforegister **Optionen** für den entsprechenden Finanzbuchhaltungsbericht.

## <a name="adjusting-exchange-rates"></a>Wechselkurse regulieren

Da sich Wechselkurse ständig ändern, müssen weitere BW-Entsprechungen im System in regelmäßigen Abständen reguliert werden. Werden diese Regulierungen nicht durchgeführt, sind Beträge, die aus Fremdwährungen (oder Berichtswährungen) umgerechnet und in der LW in der Finanzbuchhaltung gebucht wurden, möglicherweise irreführend. Darüber hinaus müssen Tagesposten, die vor der Eingabe eines Tageswechelkurses in der Anwendung gebucht werden, aktualisiert werden, nachdem der Tageswechselkurs eingegeben wurde. Der Batchauftrag **Wechselkurse** dient zur Regulierung der Wechselkurse gebuchter Kreditoren-, Debitoren- und Bankkontoposten. BW-Beträge in Sachposten können hiermit ebenfalls aktualisiert werden. Weitere Informationen finden Sie unter [Stapelverarbeitungsauftrag "Wechselkurse regulieren"](finance-how-update-currencies.md).

## <a name="setting-up-an-acy"></a>BW einrichten

Führen Sie die folgenden Schritte aus, um eine BW einzurichten:

- Legen Sie Sachkonten für die Buchung von Kursregulierungen fest.  
- Legen Sie Kursregulierungsart für alle Sachkonten fest.  
- Legen Sie die Kursregulierungsmethode für MwSt.-Posten fest.  
- Aktivieren Sie die BW.  

### <a name="to-specify-general-ledger-accounts-for-posting-exchange-rate-adjustments"></a>Sachkonten für die Buchung von Kursregulierungen festlegen:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Währungen** ein, und wählen Sie dann den entsprechenden Link.  
2. Auf der Seite **Währungen** geben Sie die folgenden Felder für die BW an.  

|Feld|Description|  
|---------------------------------|---------------------------------------|  
|**Sachkto. Kursgewinn real. Kto**|Das Finanzbuchhaltungskonto, auf das Wechselkursgewinne aus Wechselkursregulierungen zwischen der LW und der BW gebucht werden.|  
|**Sachkto. Kursverlust real. Kto**|Das Sachkonto, auf das Wechselkursgewinne aus Wechselkursregulierungen zwischen der LW und der BW gebucht werden.|  
|**Differenzkonto Gewinn**|Das Sachkonto, auf das Rundungsgewinne gebucht werden, wenn Sie im Anwendungsbereich „Finanzbuchhaltung“ sowohl in der LW als auch in einer BW buchen.|  
|**Differenzkonto Verlust**|Das Sachkonto, auf das Rundungsverluste gebucht werden, wenn Sie im Anwendungsbereich „Finanzbuchhaltung“ sowohl in der LW als auch in einer BW buchen.|

> [!NOTE]  
> Rundungsbeträge können entstehen, wenn [!INCLUDE[prod_short](includes/prod_short.md)] Soll- und Habenbeträge rundet, die aus der Mandantenwährung in eine BW umgerechnet wurden.  

Für jedes Finanzbuchhaltungskonto müssen Sie angeben, wie Beträge für dieses Konto hinsichtlich der Wechselkursschwankungen zwischen der LW und der BW reguliert werden.  

### <a name="to-specify-the-exchange-rate-adjustment-method-for-all-general-ledger-accounts"></a>So geben Sie die Kursregulierungsmethode für alle Sachkonten an

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Kontenplan** ein, und wählen Sie dann den zugehörigen Link.  
2. Auf der Seite **Kontenplan** wählen Sie das gewünschte Konto aus, und wählen Sie die **Bearbeiten** Aktion aus.  
3. Wählen Sie auf der Seite **Berichtswesen** die richtige Methode im Feld **Kursregulierung** aus.  

    Wenn Sie Buchungen in einer BW durchführen, geben Sie im Feld **Wechselkursregulierung** an, wie dieses Sachkonto bei Wechselkursschwankungen zwischen der LW und der BW ausgeglichen wird. Die Optionen werden in der folgenden Tabelle beschrieben.  

    |Feld|Description|  
    |----------------------------------|---------------------------------------|  
    |**Keine Regulierung**|Es wird keine Wechselkursregulierung auf das Sachkonto gebucht. Diese Einstellung ist die Standardoption.<br /><br /> **HINWEIS:** Wählen Sie diese Option, wenn der Wechselkurs zwischen der LW und der BW immer fest ist.|  
    |**Betrag regulieren**|Der MW-Betrag wird gemäß der Wechselkursgewinne oder -verluste reguliert. Wechselkursgewinne oder -verluste werden auf das Sachkonto im Feld **Betrag** gebucht und auf die Konten, die Sie für Gewinne oder Verluste in den Feldern **Sachkto. Kursgewinn real. Kto.** und **Sachkto. Kursverlust real. Kto.** im Fenster **Währungen** festgelegt haben.|  
    |**Zusätzlichen Währungsbetrag regulieren**|Der BW-Betrag wird gemäß der Wechselkursgewinne oder -verluste reguliert. Wechselkursgewinne oder -verluste werden auf das Sachkonto im Feld **Betrag (BW)** gebucht und auf die Konten, die Sie für Gewinne oder Verluste in den Feldern **Sachkto. Kursgewinn real. Kto.** und **Sachkto. Kursverlust real. Kto.** im Fenster **Währungen** festgelegt haben.|  

    Wechselkursgewinne und -verluste werden erstmals bei Ausführung der Stapelverarbeitung **Wechselkurse regulieren** gebucht. In diesem Batchauftrag wird der regulierte Wechselkurs auf der Seite **Währungswechselkurse** gefunden, und die Beträge in den Feldern **Betrag** und **Betrag (BW)** des Sachpostens verglichen, um zu ermitteln, ob ein Wechselkursgewinn oder -verlust vorliegt. Im Batchauftrag wird mithilfe der im Feld **Kursregulierung** ausgewählten Option bestimmt, ob Wechselkursgewinne oder -verluste für Sachkonten berechnet und gebucht werden.  

4.  Schließen Sie die Seite **Sachkontokarte**.  

### <a name="to-specify-exchange-rate-adjustment-method-for-vat-entries"></a>Die Kursregulierungsmethode für MwSt.-Posten festlegen:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Hauptbuchhaltung Einrichtung** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Berichtswesen einrichten** die richtige Methode im Feld **Kursregulierung** aus.  
3. Wenn Sie die Buchung in einer BW durchführen, können Sie im Feld **Kursregulierung** festlegen, wie die auf der Seite **MwSt.-Buchungsmatrix Einr.** für die Buchung der MwSt. eingerichteten Konten bei Wechselkursschwankungen zwischen der LW und der BW reguliert werden.  

    Wenn Sie den Batchauftrag **Wechselkurse regulieren** aufrufen, wird auf der Seite **Währungswechselkurs** der regulierte Wechselkurs gefunden, und die Beträge in den Feldern **Betrag** und **Betrag (BW)** in dem MwSt.-Posten werden verglichen, um zu ermitteln, ob ein Wechselkursgewinn oder -verlust vorliegt. Der Batchauftrag verwendet die von Ihnen gewählte Option zur Buchung von Wechselkursgewinnen oder -verlusten für MwSt.-Konten.  

    Ihnen stehen dieselben Optionen wie bei Sachposten zur Verfügung. Bei den regulierten Posten handelt es sich jedoch um MwSt.-Posten. Die Optionen werden in der folgenden Tabelle beschrieben.

    |Feld|Description|  
    |----------------------------------|---------------------------------------|  
    |**Keine Regulierung**|Es wird keine Wechselkursregulierung auf das Sachkonto gebucht. Diese Einstellung ist die Standardoption.|  
    |**Betrag regulieren**|Der MW-Betrag wird gemäß der Wechselkursgewinne oder -verluste reguliert. Wechselkursgewinne oder -verluste werden auf das Sachkonto im Feld **Betrag** gebucht und auf die Konten, die Sie für Gewinne oder Verluste in den Feldern **Sachkto. Kursgewinn real. Kto.** und **Sachkto. Kursverlust real. Kto.** im Fenster **Währungen** festgelegt haben.|  
    |**Zusätzlichen Währungsbetrag regulieren**|Der BW-Betrag wird gemäß der Wechselkursgewinne oder -verluste reguliert. Wechselkursgewinne oder -verluste werden auf das Sachkonto im Feld **Betrag (BW)** gebucht und auf die Konten, die Sie für Gewinne oder Verluste in den Feldern **Sachkto. Kursgewinn real. Kto.** und **Sachkto. Kursverlust real. Kto.** im Fenster **Währungen** festgelegt haben.|  

### <a name="to-activate-the-acy"></a>So aktivieren Sie die BW

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Hauptbuchhaltung Einrichtung** ein und wählen Sie dann den zugehörigen Link.  
2. Auf der Seite **Finanzbuchhaltung Einrichtung** wählen Sie im Feld **Berichtswährung** die zusätzliche Währung aus, in der Sie Daten erfassen möchten.  
3. Beim Verlassen des Felds zeigt [!INCLUDE[prod_short](includes/prod_short.md)] eine Bestätigungsmeldung an, die Sie über die Auswirkungen der Aktivierung der BW informiert.  
4. Wählen Sie die Schaltfläche **Ja** aus, um zu bestätigen, dass Sie die Währung aktivieren möchten.  
5. Der Batchauftrag **Berichtswährung regulieren** wird geöffnet.

    Mithilfe dieser Stapelverarbeitung werden MW-Beträge in vorhandenen Posten in die BW umgerechnet. Der Stapelverarbeitungsauftrag verwendet einen Standardwechselkurs, der am Arbeitsdatum entsprechend der Seite **Währungswechselkurse** gültig ist. Rundungsbeträge, die bei der Umrechnung der Mandantenwährung in die BW entstehen, werden auf der Seite **Währungen** angegebenen Differenzkonten für Gewinne und Verluste gebucht. Das Buchungsdatum und die Belegnummer dieser Posten ist mit denen des ursprünglichen Sachpostens identisch. Nachdem Sie sämtliche Rundungsposten gebucht haben, wird bei der Stapelverarbeitung ein Rundungsposten am Ultimodatum jedes abgeschlossenen Jahres auf das Abschlusskonto für die GuV gebucht. Durch diese Buchung wird sichergestellt, dass der Endsaldo der GuV-Konten für alle abgeschlossenen Jahre in der LW und der BW 0 ist.
6. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]      
7. Wählen Sie die Schaltfläche **OK**, um den Batchauftrag zu starten.  

Nachdem Sie die Stapelverarbeitung ausgeführt haben, werden die Beträge der folgenden vorhandenen Posten sowohl in der LW und in der BW angegeben:  

- Sachposten-Einträge  
- Artikelausgleichsposten  
- MwSt.-Posten  
- Projektposten  
- Wertposten  
- Fertigungsauftragszeilen  
- Fertigungsauftragsposten  

Darüber hinaus werden die Beträge für alle zukünftigen Posten desselben Typs sowohl in der LW als auch in der BW erfasst.  

> [!NOTE]  
> Das Feld **Berichtswährung** wird erst aktiviert, nachdem Sie im Batchauftrag **Berichtswährung regulieren** die Schaltfläche **OK** gewählt haben.  

## <a name="see-also"></a>Siehe auch

[Währungswechselkurse aktualisieren](finance-how-update-currencies.md)  
[Jahres- und Periodenabschlüsse](year-close-years-periods.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
