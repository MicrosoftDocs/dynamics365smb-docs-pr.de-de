---
title: Mahnmethoden und Mahnstufen einrichten
description: 'Richten Sie Business Central so ein, dass Sie Mahnungen wegen Zahlungen versenden und Verzugsgebühren oder -aufschläge hinzufügen können.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment due, debt, overdue, fee, charge, reminder'
ms.search.form: '431, 432, 436, 478'
ms.date: 03/12/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Mahnmethoden und Mahnstufen einrichten

Mithilfe von Mahnungen können Debitoren über überfällige Beträge informiert und die Zahlung angefordert werden. [!INCLUDE [reminder-terms](includes/reminder-terms.md)]

> [!TIP]
> Nachdem Sie Mahnbedingungen und -stufen eingerichtet haben, können Sie diese in automatisierte Prozesse zum Erstellen, Ausgeben und Senden von Mahnungen einbeziehen. Weitere Informationen zum automatisierten Prozess finden Sie unter [Erinnerungen in Sammlungen automatisieren](finance-automate-reminders.md).

## Mahnbestimmungen

Bei Debitoren mit überfälligen Zahlungen muss entschieden werden, wann und auf welche Weise ihnen eine Mahnung gesendet werden soll. Darüber hinaus können ggf. Gebühren oder Zinsen erhoben werden. Sie können eine beliebige Anzahl an Lieferanmahnungsmethoden einrichten.  

> [!NOTE]
> Wenn Sie Zinsen auf überfällige Zahlungen berechnen möchten, können Sie das auch bei der Mahnungserstellung. Möchten Sie die Zinsen dagegen nur berechnen und Ihre Debitoren darüber in Kenntnis setzen, ohne eine Mahnung zu senden, verwenden Sie eine [Zinsrechnung](finance-setup-finance-charges.md). Weitere Informationen finden Sie unter [Mahnungen](receivables-collect-outstanding-balances.md#reminders) oder [Finanzierungskosten](receivables-collect-outstanding-balances.md#finance-charges).

### Richten Sie Anhänge und E-Mail-Texte für die Kommunikation ein

Auf der Seite **Mahnfristen einrichten** können Sie Anhangstexte und Standard-E-Mail-Nachrichten einrichten, die entweder für alle Mahnstufen verwendet werden, oder für jede Stufe spezifische Nachrichten erstellen. Beispielsweise kann die Nachricht, die Sie für die erste Erinnerungsstufe senden, einen anderen Ton oder Inhalt haben als die Nachricht für die zweite oder dritte. Um Anhang- und E-Mail-Nachrichtentexte für alle Ebenen zu erstellen, wählen Sie oben auf der Seite **Debitorenkommunikation** aus. Um Nachrichten für bestimmte Zeilen zu erstellen, wählen Sie auf dem Inforegister **Mahnstufe** eine Zeile und anschließend die Aktion **Debitorenkommunikation** aus.

Standardmäßig verwenden Anhänge und E-Mail-Texte Ihre Spracheinstellung. Wenn Sie jedoch Ihre Kundschaft in anderen Ländern mahnen, möchten Sie möglicherweise in anderen Sprachen kommunizieren. Sie können mit der Aktion **Text für Sprache hinzufügen** Texte für jede von [!INCLUDE [prod_short](includes/prod_short.md)] unterstützte Sprache erstellen. Stellen Sie in diesem Fall sicher, dass die Sprachen für Anhangstexte und E-Mail-Texte identisch sind. Wenn sie nicht übereinstimmen und die Mahnfrist mehr als eine Ebene hat, kann es sein, dass die Automatisierung die Nachricht für eine oder mehrere Ebenen nicht anpassen kann. Um die Übereinstimmung der Sprachen zu prüfen, nutzen Sie die Aktion **Mitteilungsübersicht** und vergleichen Sie die Mitteilungen mit den Texten.

Wenn Sie eine E-Mail senden, ist die Erinnerung ein Bericht, den Sie an die E-Mail anhängen. Sie definieren den Bericht, der die Mahnung generiert, auf der Seite **Berichtsauswahlen – Mahnung/Zinsrechnung**, auf der Sie auch den Bericht auswählen, der den E-Mail-Text im Feld **Name des E-Mail-Textlayouts** enthält. Wenn Sie E-Mails an Ihre Kundschaft senden, werden die Texte im Inforegister **E-Mail-Text** in den im Feld **Name des E-Mail-Textlayouts** ausgewählten Bericht eingefügt. Für diesen Text ist im Standardbericht ein Textfeld vorhanden. Wenn Sie möchten, können Sie diesen Bericht bearbeiten, um beispielsweise Inhalte hinzuzufügen oder zu entfernen. Bearbeiten Sie das Layout dieser Berichte auf der Seite **Berichtslayouts**. Weitere Informationen zu Berichtslayouts finden Sie unter [Erste Schritte beim Erstellen von Berichtslayouts](ui-get-started-layouts.md).

> [!NOTE]
> Für die direkte Kommunikation per E-Mail von [!INCLUDE [prod_short](includes/prod_short.md)] müssen Sie über die entsprechende Einrichtung verfügen. Weitere Informationen zum Verbinden von E-Mail-Konten mit [!INCLUDE [prod_short](includes/prod_short.md)] finden Sie unter [E-Mail einrichten](admin-how-setup-email.md).

### Mahnmethoden einrichten

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun") Symbol. Geben Sie **Mahnmethoden** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
3. Um mehr als eine Kombination von Mahnmethoden zu verwenden, richten Sie einen Code für jede ein.

## Mahnstufen

Für jede Mahnmethode können Sie eine unbegrenzte Anzahl von Mahnstufen definieren, obwohl die meisten Unternehmen nur zwei oder drei Stufen verwenden. Bei der ersten Erstellung einer Mahnung für einen Debitor werden die Einstellungen der Stufe 1 verwendet. Beim Registrieren der Mahnung wird die Stufennummer in den erstellten Mahnposten erfasst und mit den jeweiligen Debitorenposten verknüpft. Ist eine erneute Mahnung erforderlich, werden alle Mahnposten überprüft, die mit offenen Debitorenposten verknüpft sind, um die höchste Stufennummer zu ermitteln. In der neuen Mahnung werden dann die Bedingungen für die nächsthöhere Stufennummer verwendet.

Werden mehr Mahnungen erstellt als Stufen festgelegt sind, werden die Bedingungen der höchsten Stufe verwendet. Die Anzahl der erstellbaren Mahnungen wird in den Mahnmethoden durch das Feld **Max. Anzahl Mahnungen** begrenzt.

### So richten Sie Mahnstufen ein:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun") Symbol. Geben Sie **Mahnmethoden** ein und wählen Sie dann den zugehörigen Link.  
2. Klicken Sie auf der Seite **Mahnmethoden** in die Zeile mit der Methode, für die Sie Stufen anlegen möchten, und wählen Sie dann die Aktion **Stufen**.  
3. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

    > [!TIP]
    > Die Einstellung des Felds **Zinsen berechnen** legt fest, ob bei der Erinnerung Zinsen für die Erinnerung angezeigt werden. Das Feld **Zinsen buchen** auf der Seite **Erinnerungsbestimmungen** bestimmen, ob die berechneten Zinsen auf Sachkonten und Debitorenkonten gebucht werden müssen.
    >
    > Um anzuzeigen, dass Zinsen berechnet werden sollen, wählen Sie das Feld **Zinsen berechnen**.

    Geben Sie optional für jede Mahnstufe zusätzliche Gebühren sowohl in lokaler als auch Fremdwährung an. Sie können mehrere zusätzliche Gebühren in Fremdwährungen für jeden Code auf der Seite **Mahnstufen** einrichten.  

    Die zusätzlichen Gebühren können auf drei verschiedene Arten berechnet werden, die durch den Wert des Feld **Berechnungstyp zusätzliche Gebühr** definiert werden.  

    - **Fixiert**

        Die Gebühren werden auf der Grundlage der Werte der Felder **Zusätzliche Gebühr** in der Zeile für die Erinnerungsebene selbst berechnet.  
    - **Single Dynamic**

        Die Gebühren werden auf der Grundlage der Werte der Felder **Zusätzliche Gebühr einrichten** in der Zeile für die Erinnerungsebene selbst berechnet.
    - **Akkumulierte Dynamik**

        Die Gebühren werden auf der Grundlage der Werte der Felder **Zusätzliche Gebühr einrichten** in der kombinierten Zeile für die Erinnerungsebene selbst berechnet.

4. Wählen Sie die Aktion **Währungen** aus.
5. Auf der Seite **Währungen für Mahnstufen festlegen** können Sie für jeden Mahnstufencode und die dazugehörende Mahnstufe Fremdwährungsinformationen hinterlegen, die aus einem Währungscode und einer zusätzlichen Gebühr bestehen.

    > [!NOTE]  
    > Wenn Sie Mahnungen in Fremdwährungen erstellen, verwendet die Anwendung die Bedingungen für Fremdwährungen, die Sie in dieser Tabelle eingerichtet haben, um Mahnungen zu erstellen. Falls keine Mahnkonditionen für Fremdwährungen eingerichtet wurden, verwendet die Anwendung die Mahnkonditionen für die Mandantenwährung auf der Seite **Mahnstufe** und rechnet diese in die entsprechende Währung um.

    Jede Mahnstufe kann mit Text versehen werden, der entweder vor (**Vortext**) oder nach (**Nachtext**) den Mahnposten gedruckt wird.

6. Wählen Sie die Aktionen **Anfangstext** oder **Endtext** entsprechend aus und füllen Sie die Seite **Mahntext** aus.
7. Um zugehörige Werte in das resultierende Mahntext automatisch einzusetzen, geben Sie die folgenden Platzhaltern im Feld **Text** ein.  

    |Platzhalter|Wert|  
    |-----------------|-----------|  
    |%1|Inhalt des Felds **Belegdatum** des Mahnungskopfs|  
    |%2|Inhalt des Felds **Fälligkeitsdatum** des Mahnungskopfs|  
    |%3|Inhalt des Felds **Zinssatz** im verknüpften Zinskonditionen|  
    |%4|Inhalt des Felds **Restbetrag** des Mahnungskopfs|  
    |%5|Inhalt des Felds **Zinsbetrag** des Mahnungskopfs|  
    |%6|Inhalt des Felds **Zusatzgebühr** des Mahnungskopfs|  
    |%7|Der Gesamtbetrag der Mahnung|  
    |%8|Inhalt des Felds **Mahnstufe** des Mahnungskopfs|  
    |%9|Inhalt des Felds **Währungscode** des Mahnungskopfs|  
    |%10|Inhalt des Felds **Buchungsdatum** des Mahnungskopfs|  
    |%11|Der Unternehmensname.|  
    |%12|Inhalt des Felds **Zusatzgebühr pro Zeile** des Mahnungskopfs|  

    Wenn Sie beispielsweise schreiben **%9 %7 fällig am %2.**, dann enthält die Mahnung den folgenden Text: **Sie schulden 1.200,50 MW, fällig am 02-02-2024**.

    > [!NOTE]
    > [!INCLUDE [prod_short](includes/prod_short.md)] berechnet das Fälligkeitsdatum entsprechend der von Ihnen eingegebenen Datumsformel. Weitere Informationen zu finden Sie unter [Verwenden von Datumsformeln](ui-enter-date-ranges.md#use-date-formulas).

8. Um die Sprache für eine E-Mail-Nachricht festzulegen, wählen Sie die Aktion **Text für Sprache hinzufügen**. Das Feld **Sprachcode** wird aktualisiert, um Ihre Auswahl anzuzeigen. Geben Sie im Inforegister **E-Mail-Text** den Inhalt der Nachricht in der ausgewählten Sprache ein.

Nachdem Sie die Mahnbedingungen eingerichtet haben, können Sie diese auf den Debitorenkartenseiten der Kundschaft zuweisen. Weitere Informationen finden Sie unter [Neue Debitoren registrieren](sales-how-register-new-customers.md).  

## Siehe auch

[Einziehen von Restbeträgen](receivables-collect-outstanding-balances.md)  
[Mahnungen für ausstehende Salden versenden](receivables-send-reminders.md)  
[Konditionen für Finance-Belastungen festlegen](finance-setup-finance-charges.md)  
[Finanzen einrichten](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
