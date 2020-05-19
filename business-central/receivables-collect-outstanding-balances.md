---
title: Debitoren für überfälligen Zahlungen erinnern oder mit einem Zuschlag belegen| Microsoft Docs
description: Beschreibt, wie eine Mahnung zu einem Debitoren zu einer Zahlung, welche und Gebühren hinzuzufügen fällig ist, oder Gebühren mit der Zahlung aufgrund von Verzögerung sendet.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge, reminder
ms.date: 04/02/2020
ms.author: sgroespe
ms.openlocfilehash: 0b7c1ad6a19869c5d79f7da34e89e25b2b9456aa
ms.sourcegitcommit: 8a4e66f7fc8f9ef8bdf34595e0d3983df4749376
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/15/2020
ms.locfileid: "3262118"
---
# <a name="collect-outstanding-balances"></a>Einziehen von Restbeträgen
Im Rahmen der Debitorenverwaltung muss auch geprüft werden, ob fällige Beträge pünktlich bezahlt werden. Wenn Debitoren überfällige Zahlungen haben, können Sie den Debitoren-Abrechnungsbericht als Mahnung senden. Sie können auch Mahnungen ausgeben.

Mithilfe von Mahnungen können Debitoren auf überfällige Beträge aufmerksam gemacht werden. Darüber hinaus können Mahnungen zum Berechnen von Zinsen oder Zuschlägen verwendet werden, die dann in die Mahnung aufgenommen werden. Verwenden Sie Zinsrechnungen, wenn Sie Debitoren Zinsen oder Zuschläge berechnen möchten, ohne die überfälligen Beträge anzumahnen.

## <a name="reminders"></a>Mahnungen
Bevor Sie Mahnungen erstellen können, müssen zunächst Mahnmethoden eingerichtet und den Debitoren zugeordnet werden. Jeder Mahnmethodencode enthält vordefinierte Mahnstufen. Jede Mahnstufe enthält Regeln darüber, wann die Mahnung ausgegeben wird, zum Beispiel wie viele Tage nach der Fälligkeit der Rechnung oder nach der vorherigen Mahnung. Die Inhalte der Seite **Zinskonditionen** legen fest, ob auf der Mahnung Zinsen berechnet werden.  

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
Wenn Sie Zinskonditionen und Mahnmethoden für verspätete Zahlungen einrichten, können Sie mehrere Zinssätzen angeben, damit die Strafgebühr aus verschiedenen Zinssätzen in verschiedenen Perioden berechnet wird. Sind mehrere Zinssätze nicht eingerichtet, dann wird der Zinssatz und die Periode, die auf den Seiten **Zinskonditionen** und **Mahnmethode** für der gesamten Periode der Berechnung definiert ist, verwendet. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten verschiedener Zinssätze](finance-how-to-set-up-multiple-interest-rates.md).  

## <a name="to-send-the-customer-statement-report"></a>Um den Kontoauszugsbericht zu senden
1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Kontoauszug** ein, und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Unter **Ausgabeoptionen** wählen Sie aus, wie der Bericht an den Debitoren gesendet wird.

> [!NOTE]  
>   Wenn Sie mehrere Währungen verwenden, wird der Debitoren-Abrechnungsbericht immer in der Währung des Debitors gedruckt. Das Datum einer Abrechnungsperiode dient auch als Abrechnungsdatum und als Fälligkeitsdatum, wenn die Fälligkeit enthalten ist.

## <a name="to-set-up-reminder-terms"></a>So richten Sie Mahnmethoden ein:
Bei Debitoren mit überfälligen Zahlungen muss entschieden werden, wann und auf welche Weise eine Mahnung gesendet wird. Darüber hinaus können ggf. Gebühren oder Zinsen erhoben werden. Sie können eine beliebige Anzahl an Lieferanmahnungsmethoden einrichten. Für jeden Lieferanmahnungsmethodencode können beliebig viele Lieferanmahnungsstufen definiert werden.

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Mahnmethoden** ein und wählen Sie dann den entsprechenden Link.  
2. Füllen Sie die Felder je nach Bedarf aus.  
3. Um mehr als eine Kombination von Mahnmethoden zu verwenden, richten Sie einen Code für jede ein.

## <a name="to-set-up-reminder-levels"></a>So richten Sie Mahnstufen ein:
Bei der ersten Erstellung einer Mahnung für einen Debitor werden die Einstellungen der Stufe 1 verwendet. Beim Registrieren der Mahnung wird die Stufennummer in den erstellten Mahnposten erfasst und mit den jeweiligen Debitorenposten verknüpft. Ist eine erneute Mahnung erforderlich, werden alle Mahnposten überprüft, die mit offenen Debitorenposten verknüpft sind, um die höchste Stufennummer zu ermitteln. In der neuen Mahnung werden dann die Bedingungen für die nächsthöhere Stufennummer verwendet.

Werden mehr Mahnungen erstellt als definierte Stufen vorhanden sind, werden die Bedingungen der höchsten Stufe verwendet. Die Anzahl der erstellbaren Mahnungen wird in den Mahnmethoden durch das Feld **Max. Anzahl Mahnungen** begrenzt.

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Mahnmethoden** ein und wählen Sie dann den entsprechenden Link.  
2. Klicken Sie auf der Seite **Mahnmethoden** in die Zeile mit der Methode, für die Sie Stufen anlegen möchten, und wählen Sie dann die Aktion **Stufen**.  
3. Füllen Sie die Felder je nach Bedarf aus.  

    Für jede Mahnstufe können Sie individuelle Bedingungen angeben, die zusätzliche Gebühren in Landes- oder Fremdwährung enthalten können. Sie können mehrere Gebühren in Fremdwährungen für jeden Code auf der Seite **Mahnstufen** einrichten.
4. Wählen Sie die Aktion **Währungen** aus.
5. Auf der Seite **Währungen für Mahnstufen festlegen** können Sie für jeden Mahnstufencode und die dazugehörende Mahnstufe Fremdwährungsinformationen hinterlegen, die aus einem Währungscode und einer Gebühr bestehen.

    > [!NOTE]  
    > Wenn Sie Mahnungen in Fremdwährungen erstellen, verwendet die Anwendung die Bedingungen für Fremdwährungen, die Sie in dieser Tabelle eingerichtet haben, um Mahnungen zu erstellen. Falls keine Mahnkonditionen für Fremdwährungen eingerichtet wurden, verwendet die Anwendung die Mahnkonditionen für die Mandantenwährung auf der Seite **Mahnstufe** und rechnet diese in die entsprechende Währung um.

    Jede Mahnstufe kann mit Text versehen werden, der entweder vor (**Vortext**) oder nach (**Nachtext**) den Mahnposten gedruckt wird.

6. Wählen Sie die Aktionen **Vortext** oder **Nachtext** entsprechend aus und füllen Sie die Seite **Mahntext** aus.
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

Wenn Sie beispielsweise schreiben **%9 %7 fällig am %2.**, dann enthält die Mahnung den folgenden Text: **Sie schulden 1.200,50 MW, fällig am 02-02-2014**.

> [!NOTE]
> Das Fälligkeitsdatum wird entsprechend der von Ihnen eingegebenen Datumsformel berechnet. Weitere Informationen zu finden Sie unter [Verwenden von Datumsformeln](ui-enter-date-ranges.md#using-date-formulas).

Geben Sie nach der Einrichtung der Mahnmethoden (mit zusätzlichen Stufen und Text) auf jeder Debitorenkarte einen der Codes ein. Weitere Informationen finden Sie unter [Neue Debitoren registrieren](sales-how-register-new-customers.md).

## <a name="to-create-a-reminder-automatically"></a>So erstellen Sie Mahnungen automatisch:
Eine Mahnung ähnelt einer Rechnung. Beim Erstellen einer Lieferanmahnung müssen sowohl der Lieferanmahnungskopf als auch eine oder mehrere Lieferanmahnungszeilen ausgefüllt werden. Sie können eine Funktion verwenden, um Mahnungen für alle Debitoren automatisch zu erstellen.

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Erinnerungen** ein und wählen Sie dann den entsprechenden Link.
2. Klicken Sie auf der Seite **Mahnung** auf die Aktion **Mahnung erstellen**.
3. Auf der Seite **Mahnungen erstellen** füllen Sie die Felder aus, um festzulegen wie und an Mahnungen erstellt werden.
4. Wählen Sie die Schaltfläche **OK** aus.

## <a name="to-create-a-reminder-manually"></a>So werden Mahnungen manuell erstellt:
Auf der Seite **Mahnung** können Sie das Inforegister **Allgemein** manuell ausfüllen und dann die Zeilen automatisch ausfüllen dann lassen.

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Erinnerungen** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Neu**.
3. Füllen Sie im Inforegister **Allgemein** die notwendigen Felder aus.
4. Wählen Sie die Aktion **Mahnungszeile vorschlagen**.
5. In der Stapelverarbeitung **Mahnungszeile vorschlagen** füllen Sie die Felder aus, um festzulegen wie und an wen Mahnungen erstellt werden.
6. Wählen Sie im Inforegister das Kontrollkästchen **Posten auf Abwarten einschließen**, wenn Sie möchten, dass die Mahnungen überfällige Posten enthalten, die auf „Abwarten” gesetzt sind.
7. Aktivieren Sie das Kontrollkästchen **Nur Posten mit fälligen Beträgen**, wenn die Mahnungen nur überfällige offene Posten enthalten sollen. Es werden nur Rechnungen und Zahlungen angezeigt, da dies die Einträge sind, für die die Zahlungen Ihrer Kunden möglicherweise überfällig sind.

    > [!Important]
    > Offene Posten, die auf „Abwarten” gesetzt sind, werden eingefügt, ungeachtet der Einstellung des Kontrollkästchens **Nur Posten mit fälligen Beträgen**.

8. Wählen Sie die Schaltfläche **OK** aus.

## <a name="to-replace-reminder-texts"></a>So ersetzen Sie Mahnungstexte:  
Es gibt verschiedene Arten, wie Sie den Text, der auf der ausgedruckten Mahnung erscheinen soll, festlegen können. In manchen Fällen möchten Sie möglicherweise die Vor- und Nachtexte, die für die aktuelle Stufe festgelegt wurden, durch die einer anderen Stufe ersetzen.

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Erinnerungen** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die relevante Mahnung, und wählen Sie die Aktion **Mahnungstext aktualisieren** aus.
3. Geben Sie auf der Seite **Mahnungstext aktualisieren** im Feld **Mahnstufe** die gewünschte Stufe ein.
3. Wählen Sie die Schaltfläche **OK**, um den Vortext und den Nachtext zu aktualisieren.

## <a name="to-issue-a-reminder"></a>Um eine Mahnung auszugeben
Nach dem Erstellen von Mahnungen und dem Vornehmen von möglicherweise erforderlichen Änderungen können Sie entweder Testberichte drucken oder die Mahnungen registrieren.

Durch Registrieren einer Mahnung werden die Daten auf eine separate Seite für registrierte Mahnungen übertragen. Gleichzeitig werden die Mahnungsposten gebucht. Wurden Zinsen oder Gebühren berechnet, werden zudem Debitorenposten sowie Fibu-Posten gebucht.

Wenn eine Mahnung registriert wird, werden die Posten entsprechend Ihren Angaben auf der Seite **Mahnmethode** gebucht.. Diese Spezifikation legt fest, ob Zinsen und/oder Gebühren für den Debitor und in die Finanzbuchhaltung gebucht werden sollen. Die Seite **Debitorenbuchungsgruppen** bestimmt, auf welche Konten gebucht wird.

Für jeden Debitorenposten in der Zinsrechnung wird ein Posten auf der Seite **Mahnungs-/Zinsrechnungsposten** erzeugt.

Wenn das Kontrollkästchen **Zins buchen** oder **Zusätzliche Gebühren buchen** auf der Seite **Mahnungsbedingungen** aktiviert ist, werden außerdem die folgenden Posten erstellt:

- Ein Posten auf der Seite **Debitorenposten**
- Ein Forderungsposten auf dem jeweiligen Sachkonto
- Ein Zins- und/oder Gebührenposten auf dem jeweiligen Sachkonto

Zusätzlich kann das Registrieren der Mahnung zu MwSt.-Posten führen.

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Erinnerungen** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die entsprechenden Mahung aus und wählen Sie die Aktion **Ausgeben** aus.
3. Füllen Sie auf der Seite **Mahnungen ausgeben** die Felder nach Bedarf aus.
4. Wählen Sie die Schaltfläche **OK** aus.

Die Mahnung wird entweder gedruckt oder an eine festgelegte E-Mail als PDF-Dateianhang gesendet.

### <a name="to-cancel-an-issued-reminder"></a>Zum Stornieren der registrierten Mahnung.
Wenn fälschlicherweise Erinnerungen ausgegeben wurden, können Sie diese vor dem Versenden stornieren. Sie können dies entweder einzeln oder als Stapel ausführen.
1. Auf der Seite **Profilanpassungen** wählen Sie mindestens eine Zeile für die Seitenanpassungen aus, die Sie löschen möchten, und wählen Sie danach die Aktion **Löschen** aus.
2. Auf der Seite **Ausgestellte Manung stornieren** geben Sie die Felder wie nötig ein, und wählen Sie dann die Schaltfläche **OK**.

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

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Zinskonditionen** ein, und wählen Sie dann den entsprechenden Link.  
2. Füllen Sie die Felder je nach Bedarf aus.
3. Um mehr als eine Kombination von Mahnmethoden zu verwenden, richten Sie einen Code für jede ein.

    Für jede Mahnstufe können Sie individuelle Bedingungen angeben, die zusätzliche Gebühren in Landes- oder Fremdwährung enthalten können. Sie können mehrere Gebühren in Fremdwährungen für jeden Code auf der Seite **Zinskonditionen** einrichten.
4. Wählen Sie die Aktion **Währungen** aus.
5. Auf der Seite **Währungen für Zinskonditionen** können Sie für jeden Begriff einen Währungscode und Gebühren definieren.

    > [!NOTE]  
    > Wenn Sie Zinsrechnungen in Fremdwährungen erstellen, verwendet die Anwendung die Bedingungen für Fremdwährungen, die Sie in dieser Tabelle eingerichtet haben, um Zinsrechnungen zu erstellen. Falls es keine Zinskonditionen für Fremdwährungen gibt, verwendet die Anwendung die Zinskonditionen für die Mandantenwährung auf der Seite **Zinskondition** und rechnet diese in die entsprechende Währung um.

    Für jeden Zinskonditionencode können Sie Texte festlegen, die vor (**Vortext**) oder nach (**Nachtext**) den Posten in der Zinsrechnung ausgedruckt werden sollen.  
6. Wählen Sie die Aktionen **Vortext** oder **Nachtext** entsprechend aus und füllen Sie die Seite **Zinsgebühr** aus.
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

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Zinsrechnungen** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu** aus, und füllen Sie die Felder nach Bedarf aus.  
3. Wählen Sie **Zinsgebührmemo-Zeilen** vorschlagen.
4. Auf der Seite **Zinsrechnungszeile vorschlagen** setzen Sie auf dem Inforegister **Debitorenposten** einen Filter, wenn Sie nur für bestimmte Posten Zinsrechnungen erstellen möchten.

    > [!NOTE]
    > Obwohl sie aufgelistet sind, hat die Auswahl von **Zahlung** und **Gutschrift** als **Belegart**-Filter keine Wirkung, da die Funktion **Zinsrechnung** nur positive Beträge verarbeitet.
5.  Klicken Sie auf die Schaltfläche **OK**, um den Batchauftrag zu starten.  

## <a name="to-update-finance-charge-memo-texts"></a>So aktualisieren Sie Zinsrechnungstexte:  
In manchen Fällen möchten Sie möglicherweise den Vor- und Nachtext ändern, den Sie für die Zinskonditionen eingerichtet haben. Wenn Sie dies zu einem Zeitpunkt tun, an dem Sie Zinsrechnungen angelegt, aber noch nicht registriert haben, können Sie die Anwendung dazu veranlassen, die Zinsrechnungen mit den geänderten Texten zu aktualisieren.

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Zinsrechnung** ein, und wählen Sie dann den entsprechenden Link.  
2. Öffnen Sie das Fenster, in dem Sie Text ändern möchten und wählen Sie die **Zinsrech. Text aktualisieren** Aktion aus.
3. Auf der Seite **Zinsrechnungskopf aktualisieren** können Sie einen Filter festlegen, wenn Sie mehrere Zinsrechnungen aktualisieren möchten.
4. Wählen Sie die Schaltfläche **OK**, um den Vortext und den Nachtext zu aktualisieren.  

## <a name="to-issue-finance-charge-memos"></a>Um Zinsrechnungen zu registrieren
Nach dem Erstellen von Zinsrechnungen und dem Vornehmen von möglicherweise erforderlichen Änderungen können Sie entweder Testberichte drucken oder die Zinsrechnungen registrieren.

Wenn eine Mahnung registriert wird, werden die Posten entsprechend Ihren Angaben auf der Seite **Zinsgebühr** gebucht. Diese Spezifikation legt fest, ob Zinsen und/oder Gebühren für den Debitor und in die Finanzbuchhaltung gebucht werden sollen. Die Seite **Debitorenbuchungsgruppen** bestimmt, auf welche Konten gebucht wird.

Für jeden Debitorenposten in der Zinsrechnung wird ein Posten auf der Seite **Mahnungs-/Zinsrechnungsposten** erzeugt.

Wenn das Kontrollkästchen **Zins buchen** oder **Zusätzliche Gebühren buchen** auf der Seite **Zinsgebührbedingungen** aktiviert ist, werden außerdem die folgenden Posten erstellt:

- Ein Posten auf der Seite **Debitorenposten**
- Ein Forderungsposten auf dem jeweiligen Sachkonto
- Ein Zins- und/oder Gebührenposten auf dem jeweiligen Sachkonto

Zusätzlich kann das Registrieren der Mahnung zu MwSt.-Posten führen.

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Zinsrechnungen** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie das entsprechenden Memo aus und wählen Sie die Aktion **Ausgeben** aus.
3. Füllen Sie auf der Seite **Zinsgebührmemo ausgeben** die Felder nach Bedarf aus.
4. Wählen Sie die Schaltfläche **OK** aus.

Das Zinsgebührenmemo wird entweder gedruckt oder an eine festgelegte E-Mail als PDF-Dateianhang gesendet.

### <a name="to-cancel-an-issued-finance-charge-memo"></a>Um die ausgestellte Zinsrechnung zu stornieren
Wenn fälschlicherweise Zinsrechnungen ausgegeben wurden, können Sie diese vor dem Versenden stornieren. Sie können dies entweder einzeln oder als Stapel ausführen.
1. Auf der Seite **Ausgestellte Zinsrechnung** wählen Sie mindestens eine Zeile für die Seitenanpassungen aus, die Sie löschen möchten, und wählen Sie danach die Aktion **Löschen** aus.
2. Auf der Seite **Ausgestellte Zinsrechnungs-Memos stornieren** geben Sie die Felder wie nötig ein, und wählen Sie dann die Schaltfläche **OK**.

## <a name="to-view-reminder-and-finance-charge-entries"></a>So zeigen Sie Mahnungs- und Zinsrechnungsposten an:  
Wenn Sie eine Mahnung registrieren, wird für jede Mahnungszeile, die einen Debitorenposten enthält, ein Mahnungsposten auf der Seite **Mahnung/Zinsrechnung Posten** erstellt. Sie können sich einen Überblick über die erstellten Mahnungsposten für einen bestimmten Debitor anzeigen lassen.    
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie die entsprechende Debitorenkarte und klicken dann auf **Buchblatteinträge**.
3. Klicken Sie auf die Seite auf **Buch-Blatteinträge** und wählen Sie die Zeilen, die Sie anzeigen möchten, und klicken Sie dann auf **Posten, Mahnungs-/Zinsrechnungseinträge**.

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/paths/process-financial-periodic-activities-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
