---
title: "Kunden für überfälligen Zahlungen erinnern oder mit einem Zuschlag belegen| Microsoft Docs"
description: "Beschreibt, wie eine Mahnung zu einem Debitoren zu einer Zahlung, welche und Gebühren hinzuzufügen fällig ist, oder Gebühren mit der Zahlung aufgrund von Verzögerung sendet."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge, reminder
ms.date: 03/16/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 8f4cb1b2fdd55275fc1a3cba494d1ea4b583b5ed
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="collect-outstanding-balances"></a>Einziehen von Restbeträgen
Im Rahmen der Debitorenverwaltung muss auch geprüft werden, ob fällige Beträge pünktlich bezahlt werden. Wenn Debitoren überfällige Zahlungen haben, können Sie den Debitoren-Abrechnungsbericht als Mahnung senden. Sie können auch Mahnungen ausgeben.

Mithilfe von Mahnungen können Debitoren auf überfällige Beträge aufmerksam gemacht werden. Darüber hinaus können Mahnungen zum Berechnen von Zinsen oder Zuschlägen verwendet werden, die dann in die Mahnung aufgenommen werden. Verwenden Sie Zinsrechnungen, wenn Sie Debitoren Zinsen oder Zuschläge berechnen möchten, ohne die überfälligen Beträge anzumahnen.

## <a name="reminders"></a>Mahnungen
Bevor Sie Mahnungen erstellen können, müssen zunächst Mahnmethoden eingerichtet und den Debitoren zugeordnet werden. Jeder Mahnmethodencode enthält vordefinierte Mahnstufen. Jede Mahnstufe enthält Regeln darüber, wann die Mahnung ausgegeben wird, zum Beispiel wie viele Tage nach der Fälligkeit der Rechnung oder nach der vorherigen Mahnung. Die Inhalte des Fensters **Zinskonditionen** legen fest, ob auf der Mahnung Zinsen berechnet werden.  

Der Batchauftrag **Mahnungen erstellen** kann in regelmäßigen Abständen ausgeführt werden, um Mahnungen für alle Debitoren mit überfälligem Saldo zu erstellen. Alternativ können Sie eine Mahnung für einen bestimmten Debitor manuell erstellen und die Zeilen automatisch berechnen und ausfüllen lassen.  

Erstellte Mahnungen können geändert werden. Der Text, der am Anfang und am Ende einer Mahnung erscheint, ist abhängig von den Bedingungen für die Mahnstufe und wird in der Spalte **Beschreibung** angezeigt. Wurde in den Vor- oder Nachtext automatisch ein berechneter Betrag eingefügt, wird der Text beim Löschen von Zeilen nicht angepasst. Verwenden Sie in diesem Fall die Funktion **Mahnungstext aktualisieren**.  

Durch Debitorenposten, bei denen das Feld **Abwarten** ausgefüllt ist, wird keine Mahnungserstellung veranlasst. Wird jedoch eine Mahnung auf der Grundlage eines anderen Postens erstellt, wird auch ein überfälliger Posten, der mit "Abwarten" markiert ist, in die Mahnung einbezogen. Für Zeilen mit diesen Posten werden keine Zinsen berechnet.

Nach dem Erstellen von Mahnungen und dem Vornehmen von möglicherweise erforderlichen Änderungen können Sie entweder Testberichte drucken oder die Mahnungen registrieren.

## <a name="finance-charges"></a>Finanzierungskosten
Hat ein Debitor nicht bis zum Fälligkeitsdatum gezahlt, können automatisch Zuschläge berechnet und zu den überfälligen Beträgen auf dem Debitorkonto addiert werden. Verwenden Sie Zinsrechnungen, um Debitoren über die Zuschläge zu informieren.  

> [!NOTE]  
> Mithilfe von Zinsrechnungen werden Zinsen und Zuschläge berechnet und Debitoren über die Zinsen und Zuschläge informiert, ohne die überfälligen Beträge anzumahnen. Alternativ können Zinsen auf überfällige Zahlungen auch bei der Mahnungserstellung berechnet werden.  

Sie können eine Zinsrechnung für einen bestimmten Debitor manuell erstellen und die Zeilen automatisch ausfüllen. Alternativ können Sie die Funktion **Zinsrechnungen erstellen** verwenden, um Zinsrechnungen für alle oder ausgewählte Debitoren mit überfälligem Saldo zu erstellen.  

Erstellte Zinsrechnungen können geändert werden. Der Text, der am Anfang und am Ende der Zinsrechnung erscheint, ist abhängig von den Zinskonditionen und wird in der jeweiligen Zeile in der Spalte **Beschreibung** angezeigt. Wurde in den Vor- oder Nachtext automatisch ein berechneter Betrag eingefügt, wird der Text beim Löschen von Zeilen nicht angepasst. Verwenden Sie in diesem Fall die Funktion **Zinsrech. Text aktualisieren**.  

Nach dem Erstellen von Zinsrechnungen und dem Vornehmen von möglicherweise erforderlichen Änderungen können Sie entweder Testberichte drucken oder die Zinsrechnungen versenden, in der Regel als E-Mail.

## <a name="multiple-interest-rates"></a>Verschiedene Zinssätze
Wenn Sie Zinskonditionen und Mahnmethoden für verspätete Zahlungen einrichten, können Sie mehrere Zinssätzen angeben, damit die Strafgebühr aus verschiedenen Zinssätzen in verschiedenen Perioden berechnet wird. Sind mehrere Zinssätze nicht eingerichtet, dann wird der Zinssatz und die Periode, die in den Fenstern **Zinskonditionen** und **Mahnmethode** für der gesamten Periode der Berechnung definiert ist, verwendet. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten verschiedener Zinssätze](finance-how-to-set-up-multiple-interest-rates.md).  

## <a name="to-send-the-customer-statement-report"></a>Um den Kontoauszugsbericht zu senden
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Kundenauszug** ein. Wählen Sie dann den zugehörigen Link aus.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Unter **Ausgabeoptionen** wählen Sie aus, wie der Bericht an den Kunden gesendet wird.

> [!NOTE]  
>   Wenn Sie mehrere Währungen verwenden, wird der Debitoren-Abrechnungsbericht immer in der Währung des Debitors gedruckt. Das Datum einer Abrechnungsperiode dient auch als Abrechnungsdatum und als Fälligkeitsdatum, wenn die Fälligkeit enthalten ist.

## <a name="to-set-up-reminder-terms"></a>So richten Sie Mahnmethoden ein:
Bei Debitoren mit überfälligen Zahlungen muss entschieden werden, wann und auf welche Weise eine Mahnung gesendet wird. Darüber hinaus können ggf. Gebühren oder Zinsen erhoben werden. Sie können eine beliebige Anzahl an Lieferanmahnungsmethoden einrichten. Für jeden Lieferanmahnungsmethodencode können beliebig viele Lieferanmahnungsstufen definiert werden.

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Mahnungsbestimmungen** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus.  
3. Um mehr als eine Kombination von Mahnmethoden zu verwenden, richten Sie einen Code für jede ein.

## <a name="to-set-up-reminder-levels"></a>So richten Sie Mahnstufen ein:
Bei der ersten Erstellung einer Mahnung für einen Debitor werden die Einstellungen der Stufe 1 verwendet. Beim Registrieren der Mahnung wird die Stufennummer in den erstellten Mahnposten erfasst und mit den jeweiligen Debitorenposten verknüpft. Ist eine erneute Mahnung erforderlich, werden alle Mahnposten überprüft, die mit offenen Debitorenposten verknüpft sind, um die höchste Stufennummer zu ermitteln. In der neuen Mahnung werden dann die Bedingungen für die nächsthöhere Stufennummer verwendet.

Werden mehr Mahnungen erstellt als definierte Stufen vorhanden sind, werden die Bedingungen der höchsten Stufe verwendet. Die Anzahl der erstellbaren Mahnungen wird in den Mahnmethoden durch das Feld **Max. Anzahl Mahnungen** begrenzt.

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Mahnungsbestimmungen** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Klicken Sie im Fenster **Mahnmethoden** in die Zeile mit der Methode, für die Sie Stufen anlegen möchten, und wählen Sie dann Aktione **Stufen**.  
3. Füllen Sie die Felder je nach Bedarf aus.  

    Für jede Mahnstufe können Sie individuelle Bedingungen angeben, die zusätzliche Gebühren in Landes- oder Fremdwährung enthalten können. Sie können mehrere Gebühren in Fremdwährungen für jeden Code im Fenster **Mahnstufen** einrichten.
4. Wählen Sie die Aktion **Währungen** aus.
5. Im Fenstert **Währungen für Mahnstufen festlegen** können Sie für jeden Mahnstufencode und die dazugehörende Mahnstufe Fremdwährungsinformationen hinterlegen, die aus einem Währungscode und einer Gebühr bestehen.

    > [!NOTE]  
    > Wenn Sie Mahnungen in Fremdwährungen erstellen, verwendet die Anwendung die Bedingungen für Fremdwährungen, die Sie in dieser Tabelle eingerichtet haben, um  Mahnungen zu erstellen. Falls keine Mahnkonditionen für Fremdwährungen eingerichtet wurden, verwendet die Anwendung die Mahnkonditionen für die Mandantenwährung in der Tabelle **Mahnstufe** und rechnet diese in die entsprechende Währung um.

    Jede Mahnstufe kann mit Text versehen werden, der entweder vor ( **Vortext**) oder nach ( **Nachtext**) den Mahnposten gedruckt wird.

6. Wählen Sie die Aktionen **Vortext** oder **Nachtext** entsprechend aus und füllen Sie das Fenster **Mahntext** aus.
7. Um zugehörige Werte in das resultierende Mahntext automatisch einzusetzen, geben -Sie die folgenden Platzhaltern im Feld **Text** Feld ein.  

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

Wenn Sie beispielsweise schreiben **%9 %7 fällig am %2.**, dann enthält die Mahnung den folgenden Text: **Sie schulden 1,200,50 MW, fällig am 02-02-2014.**

Geben Sie nach der Einrichtung der Mahnmethoden (mit zusätzlichen Stufen und Text) auf jeder Debitorenkarte einen der Codes ein. Weitere Informationen finden Sie unter [Neue Kunden registrieren](sales-how-register-new-customers.md).

## <a name="to-create-a-reminder-automatically"></a>So erstellen Sie Mahnungen automatisch:
Eine Mahnung ähnelt einer Rechnung. Beim Erstellen einer Lieferanmahnung müssen sowohl der Lieferanmahnungskopf als auch eine oder mehrere Lieferanmahnungszeilen ausgefüllt werden. Sie können eine Funktion verwenden, um Mahnungen für alle Debitoren automatisch zu erstellen.

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Mahnung** ein. Wählen Sie dann den zugehörigen Link aus.
2. Klicken Sie im Fenster **Mahnung** auf die Aktion **Mahnung erstellen**.
3. Im Fenster **Mahnungen erstellen** füllen Sie die Felder aus, um festzulegen wie und an Mahnungen erstellt werden.
4. Wählen Sie die Schaltfläche **OK** aus.

## <a name="to-create-a-reminder-manually"></a>So werden Mahnungen manuell erstellt:
Im Fenster **Mahnung** können Sie das Inforegister **Allgemein** manuell ausfüllen und dann die Zeilen automatisch ausfüllen dann lassen.

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Mahnung** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie im Inforegister **Allgemein** die notwendigen Felder aus.
4. Wählen Sie die Aktion **Mahnungszeile vorschlagen**.
5. In der Stapelverarbeitung **Mahnungszeile vorschlagen** füllen Sie die Felder aus, um festzulegen wie und an wen Mahnungen erstellt werden.
6. Wählen Sie im Inforegister das Kontrollkästchen **Posten auf Abwarten einschließen**, wenn Sie möchten, dass die Mahnungen überfällige Posten enthalten, die auf „Abwarten” gesetzt sind.

    > [!Important]
    > Offene Posten, die auf „Abwarten” gesetzt sind, werden eingefügt, ungeachtet der Einstellung des Kontrollkästchens Nur Posten mit fälligen Beträgen.

7. Wählen Sie die Schaltfläche **OK** aus.

## <a name="to-replace-reminder-texts"></a>So ersetzen Sie Mahnungstexte:  
Es gibt verschiedene Arten, wie Sie den Text, der auf der ausgedruckten Mahnung erscheinen soll, festlegen können. In manchen Fällen möchten Sie möglicherweise die Vor- und Nachtexte, die für die aktuelle Stufe festgelegt wurden, durch die einer anderen Stufe ersetzen.

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Mahnung** ein. Wählen Sie dann den zugehörigen Link aus.
2. Öffnen Sie die relevante Mahnung, und wählen Sie die Aktion **Mahnungstext aktualisieren** aus.
3. Geben Sie im Fenster **Mahnungstext aktualisieren** im Feld **Mahnstufe** die gewünschte Stufe ein.
3. Wählen Sie die Schaltfläche **OK**, um den Vortext und den Nachtext zu aktualisieren.

## <a name="to-issue-a-reminder"></a>Um eine Mahnung auszugeben
Nach dem Erstellen von Mahnungen und dem Vornehmen von möglicherweise erforderlichen Änderungen können Sie entweder Testberichte drucken oder die Mahnungen registrieren.

Durch Registrieren einer Mahnung werden die Daten in einem separaten Fenster für registrierte Mahnungen übertragen. Gleichzeitig werden die Mahnungsposten gebucht. Wurden Zinsen oder Gebühren berechnet, werden zudem Debitorenposten sowie Fibu-Posten gebucht.

Wenn eine Mahnung registriert wird, werden die Posten entsprechend Ihren Angaben in der Tabelle **Mahnmethode** gebucht.. Diese Spezifikation legt fest, ob Zinsen und/oder Gebühren für den Debitor und in die Finanzbuchhaltung gebucht werden sollen. Das Fenster **Debitorenbuchungsgruppen** bestimmt, auf welche Konten gebucht wird.

Für jeden Debitorenposten in der Zinsrechnung wird ein Posten in der Tabelle **Mahnungs-/Zinsrechnungsposten** erzeugt.

Wenn das Kontrollkästchen **Zins buchen** oder **Zusätzliche Gebühren buchen** im Fenster **Mahnungsbedingungen** aktiviert ist, werden außerdem die folgenden Posten erstellt:

- Ein Posten im Fenster **Debitorenposten**
- Ein Forderungsposten auf dem jeweiligen Sachkonto
- Ein Zins- und/oder Gebührenposten auf dem jeweiligen Sachkonto

Zusätzlich kann das Registrieren der Mahnung zu MwSt.-Posten führen.

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Mahnung** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die entsprechenden Mahung aus und wählen Sie die Aktion **Ausgeben** aus.
3. Füllen Sie im Fenster **Mahnungen ausgeben** die Felder nach Bedarf aus.
4. Wählen Sie die Schaltfläche **OK** aus.

Die Mahnung wird entweder gedruckt oder an eine festgelegte E-Mail als PDF-Dateianhang gesendet.

## <a name="to-set-up-finance-charge-terms"></a>Um Bedingungen für Gebühren festzulegen
Sie müssen für jede Zinskondition einen eigenen Code einrichten. Danach können Sie den Code in das Feld **Zinskonditionencode** auf den Debitorenkarten eingeben.

Zinsen können entweder auf der Grundlage des Tagessaldos oder des fälligen Saldos berechnet werden.

* Methode "Fälliger Saldo":

    Bei der Methode "Fälliger Saldo" stellt der Zins einfach einen Prozentsatz des überfälligen Betrags dar:  
    *Methode fälliger Saldo* - *Belastung* = *Überfälliger Betrag* x *(Zinssatz Rate / 100)*

*   Methode "Tagessaldo":

    Die Anzahl der Tage, die die Zahlung überfällig ist, wird berücksichtigt:  
    *Durchschnittlicher Tagessaldo* - *Belastung* = *Überfälliger Betrag* x *(Überfälliger Betrag / Zinsperiodeo)* x *(Zinssatz/100)*

Zusätzlich ist jeder Code in der Tabelle "Zinskondition" mit einer Untertabelle, der Tabelle Zinsrechnungstext verbunden. Für jeden Zinskonditionencode kann hier ein Vor- und/oder Nachtext hinterlegt werden, der dann auf dem Zinsrechnungsbeleg erscheint.

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Mahnungsbestimmungen** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus.  
3. Um mehr als eine Kombination von Mahnmethoden zu verwenden, richten Sie einen Code für jede ein.

    Für jede Mahnstufe können Sie individuelle Bedingungen angeben, die zusätzliche Gebühren in Landes- oder Fremdwährung enthalten können. Sie können mehrere Gebühren in Fremdwährungen für jeden Code im Fenster **Zinskonditionen** einrichten.
4. Wählen Sie die Aktion **Währungen** aus.
5. Im Fenster **Währungen für Zinskonditionen** können Sie für jeden Begriff einen Währungscode und Gebühren definieren.

    > [!NOTE]  
    > Wenn Sie Zinsrechnungen in Fremdwährungen erstellen, verwendet die Anwendung die Bedingungen für Fremdwährungen, die Sie in dieser Tabelle eingerichtet haben, um  Zinsrechnungen zu erstellen. Falls es keine Zinskonditionen für Fremdwährungen gibt, verwendet die Anwendung die Zinskonditionen für die Mandantenwährung in der Tabelle **Zinskondition** und rechnet diese in die entsprechende Währung um.

    Für jeden Zinskonditionencode können Sie Texte festlegen, die vor (**Vortext**) oder nach (**Nachtext)** den Posten in der Zinsrechnung ausgedruckt werden sollen.  
6. Wählen Sie die Aktionen **Vortext** oder **Nachtext** entsprechend aus und füllen Sie das Fenster **Zinsgebühr** aus.
7. Um zugehörige Werte in das resultierende Zinsgebühr automatisch einzusetzen, geben -Sie die folgenden Platzhaltern im Feld **Text** Feld ein.

|Platzhalter|Wert|  
|-----------------|-----------|  
|%1|Inhalt des Felds **Belegdatum** des Zinsgebührkopfs|  
|%2|Inhalt des Felds **Fälligkeitsdatum** des Zinsgebührkopfs|  
|%3|Inhalt des Felds **Zinssatz** im verknüpften Zinskonditionen|  
|%4|Inhalt des Felds **Restbetrag** des Zinsgebührkopfs|  
|%5|Inhalt des Felds **Zinsbetrag** des Zinsgebührkopfs|  
|%6|Inhalt des Felds **Zusatzgebühr** des Zinsgebührkopfs|  
|%7|Der Gesamtbetrag der Mahnung|  
|%8|Inhalt des Felds **Währungscode** des Zinsgebührkopfs|  
|%9|Inhalt des Felds **Buchungsdatum** des Zinsgebührkopfs|  

## <a name="to-create-a-finance-charge-memo-manually"></a>So erstellen Sie eine Zinsrechnung manuell  
Eine Zinsrechnung ist ähnlich wie eine Rechnung. Sie können den Kopf manuell ausfüllen und die Zeilen ausfüllen lassen, oder Sie können Zinsrechnungen für alle Debitoren automatisch erstellen lassen.

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Zinsgebührmemo** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Neu** aus, und füllen Sie die Felder nach Bedarf aus.  
3. Wählen Sie **Zinsgebührmemo-Zeilen** vorschlagen.
4. Im Fenster **Zinsrechnungszeile vorschlagen**Setzen Sie auf dem Inforegister **Debitorenposten** einen Filter, wenn Sie nur für bestimmte Posten Zinsrechnungen erstellen möchten.  
5.  Klicken Sie auf die Schaltfläche **OK**, um den Batchauftrag zu starten.  

## <a name="to-update-finance-charge-memo-texts"></a>So aktualisieren Sie Zinsrechnungstexte:  
In manchen Fällen möchten Sie möglicherweise den Vor- und Nachtext ändern, den Sie für die Zinskonditionen eingerichtet haben. Wenn Sie dies zu einem Zeitpunkt tun, an dem Sie Zinsrechnungen angelegt, aber noch nicht registriert haben, können Sie die Anwendung dazu veranlassen, die Zinsrechnungen mit den geänderten Texten zu aktualisieren.

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Zinsgebührmemo** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Öffnen Sie das Fenster, in dem Sie Text ändern möchten und wählen Sie die **Zinsrech. Text aktualisieren** Aktion aus.
3. Auf dem Inforegister **Zinsrechnungskopf aktualisieren** können Sie einen Filter festlegen, wenn Sie mehrere Zinsrechnungen aktualisieren möchten.
4. Wählen Sie die Schaltfläche **OK**, um den Vortext und den Nachtext zu aktualisieren.  

## <a name="to-issue-finance-charge-memos"></a>Um Zinsrechnungen zu registrieren
Nach dem Erstellen von Zinsrechnungen und dem Vornehmen von möglicherweise erforderlichen Änderungen können Sie entweder Testberichte drucken oder die Zinsrechnungen registrieren.

Wenn eine Mahnung registriert wird, werden die Posten entsprechend Ihren Angaben in der Tabelle **Zinsgebühr** gebucht. Diese Spezifikation legt fest, ob Zinsen und/oder Gebühren für den Debitor und in die Finanzbuchhaltung gebucht werden sollen. Das Fenster **Debitorenbuchungsgruppen** bestimmt, auf welche Konten gebucht wird.

Für jeden Debitorenposten in der Zinsrechnung wird ein Posten in der Tabelle **Mahnungs-/Zinsrechnungsposten** erzeugt.

Wenn das Kontrollkästchen **Zins buchen** oder **Zusätzliche Gebühren buchen** im Fenster **Zinsgebührbedingungen** aktiviert ist, werden außerdem die folgenden Posten erstellt:

- Ein Posten im Fenster **Debitorenposten**
- Ein Forderungsposten auf dem jeweiligen Sachkonto
- Ein Zins- und/oder Gebührenposten auf dem jeweiligen Sachkonto

Zusätzlich kann das Registrieren der Mahnung zu MwSt.-Posten führen.

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Zinsgebührmemo** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie das entsprechenden Memo aus und wählen Sie die Aktion **Ausgeben** aus.
3. Füllen Sie im Fenster **Zinsgebührmemo ausgeben** die Felder nach Bedarf aus.
4. Wählen Sie die Schaltfläche **OK** aus.

Das Zinsgebührenmemo wird entweder gedruckt oder an eine festgelegte E-Mail als PDF-Dateianhang gesendet.

## <a name="to-view-reminder-and-finance-charge-entries"></a>So zeigen Sie Mahnungs- und Zinsrechnungsposten an:  
Wenn Sie eine Mahnung registrieren, wird für jede Mahnungszeile, die einen Debitorenposten enthält, ein Mahnungsposten in der Tabelle **Mahnung/Zinsrechnung Posten** erstellt. Sie können sich einen Überblick über die erstellten Mahnungsposten für einen bestimmten Debitor anzeigen lassen.    
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Kunden** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Öffnen Sie die entsprechende Debitorenkarte und klicken dann auf **Buchblatteinträge**.
3. Klicken Sie in die Zeile **Buch-Blatteinträge** und wählen Sie die Zeilen, die Sie anzeigen möchten, und klicken Sie dann auf  **Posten,  Mahnungs-/Zinsrechnungseinträge**.

## <a name="see-also"></a>Siehe auch
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

