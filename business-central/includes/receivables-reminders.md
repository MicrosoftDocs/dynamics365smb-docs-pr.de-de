---
author: edupont04
ms.topic: include
ms.date: 02/09/2022
ms.author: edupont
ms.openlocfilehash: fc1788acfb1b11a90327ac72ce83d7fa4981e602
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8143348"
---
Mithilfe von Mahnungen können Debitoren auf überfällige Beträge aufmerksam gemacht werden. Sie können auch Mahnungen verwenden, um finanzielle Belastungen wie Zinsen oder Gebühren zu berechnen und sie in die Mahnung aufzunehmen.

Bevor Sie Mahnungen erstellen können, müssen zunächst Mahnmethoden eingerichtet und den Debitoren zugeordnet werden. Weitere Informationen finden Sie unter [Mahnmethoden und Stufen festlegen](../finance-setup-reminders.md). [!INCLUDE [reminder-terms](reminder-terms.md)] Der Inhalt der Seite **Zinskonditionen für Finance** bestimmt, ob für die Mahnung Zinsen berechnet werden.  

Der Batchauftrag **Mahnungen erstellen** kann in regelmäßigen Abständen ausgeführt werden, um Mahnungen für alle Debitoren mit überfälligem Saldo zu erstellen. Alternativ können Sie eine Mahnung für einen bestimmten Debitor manuell erstellen und die Zeilen automatisch berechnen und ausfüllen lassen.  

Erstellte Mahnungen können geändert werden. Der Text, der am Anfang und am Ende einer Mahnung erscheint, ist abhängig von den Bedingungen für die Mahnstufe und wird in der Spalte **Beschreibung** angezeigt. Wurde in den Vor- oder Nachtext automatisch ein berechneter Betrag eingefügt, wird der Text beim Löschen von Zeilen nicht angepasst. Verwenden Sie in diesem Fall die Funktion **Mahnungstext aktualisieren**.  

Durch Debitorenposten, bei denen das Feld **Abwarten** ausgefüllt ist, wird keine Mahnungserstellung veranlasst. Wird jedoch eine Mahnung auf der Grundlage eines anderen Postens erstellt, wird auch ein überfälliger Posten, der mit "Abwarten" markiert ist, in die Mahnung einbezogen. Für Zeilen mit diesen Posten werden keine Zinsen berechnet.

Nach dem Erstellen von Mahnungen und dem Vornehmen von möglicherweise erforderlichen Änderungen können Sie entweder Testberichte drucken oder die Mahnungen registrieren.

### <a name="to-create-a-reminder-automatically"></a>So erstellen Sie Mahnungen automatisch:

Eine Mahnung ähnelt einer Rechnung. Beim Erstellen einer Lieferanmahnung müssen sowohl der Lieferanmahnungskopf als auch eine oder mehrere Lieferanmahnungszeilen ausgefüllt werden. Sie können eine Funktion verwenden, um Mahnungen für alle Debitoren automatisch zu erstellen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 0.](../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Mahnungen** ein und wählen Sie dann den zugehörigen Link.
2. Klicken Sie auf der Seite **Mahnung** auf die Aktion **Mahnung erstellen**.
3. Auf der Seite **Mahnungen erstellen** füllen Sie die Felder aus, um festzulegen wie und an Mahnungen erstellt werden.
4. Wählen Sie die Schaltfläche **OK** aus.

### <a name="to-create-a-reminder-manually"></a>So werden Mahnungen manuell erstellt:

Auf der Seite **Mahnung** können Sie das Inforegister **Allgemein** manuell ausfüllen und dann die Zeilen automatisch ausfüllen dann lassen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion erneut öffnet 2.](../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Mahnungen** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Neu**.
3. Füllen Sie im Inforegister **Allgemein** die notwendigen Felder aus.
4. Wählen Sie die Aktion **Mahnungszeile vorschlagen**.
5. In der Stapelverarbeitung **Mahnungszeile vorschlagen** füllen Sie die Felder aus, um festzulegen wie und an wen Mahnungen erstellt werden.
6. Wählen Sie im Inforegister das Kontrollkästchen **Posten auf Abwarten einschließen**, wenn Sie möchten, dass die Mahnungen überfällige Posten enthalten, die auf „Abwarten” gesetzt sind.
7. Aktivieren Sie das Kontrollkästchen **Nur Posten mit fälligen Beträgen**, wenn die Mahnungen nur überfällige offene Posten enthalten sollen. Es werden nur Rechnungen und Zahlungen angezeigt, da dies die Einträge sind, für die die Zahlungen Ihrer Kunden möglicherweise überfällig sind.

    > [!Important]
    > Offene Posten, die auf „Abwarten” gesetzt sind, werden eingefügt, ungeachtet der Einstellung des Kontrollkästchens **Nur Posten mit fälligen Beträgen**.

8. Wählen Sie die Schaltfläche **OK** aus.

### <a name="to-replace-reminder-texts"></a>So ersetzen Sie Mahnungstexte:

Es gibt verschiedene Arten, wie Sie den Text, der auf der ausgedruckten Mahnung erscheinen soll, festlegen können. In manchen Fällen möchten Sie möglicherweise die Vor- und Nachtexte, die für die aktuelle Stufe festgelegt wurden, durch die einer anderen Stufe ersetzen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion noch einmal öffnet 3.](../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Mahnungen** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die relevante Mahnung, und wählen Sie die Aktion **Mahnungstext aktualisieren** aus.
3. Geben Sie auf der Seite **Mahnungstext aktualisieren** im Feld **Mahnstufe** die gewünschte Stufe ein.
4. Wählen Sie die Schaltfläche **OK**, um den Vortext und den Nachtext zu aktualisieren.

### <a name="to-issue-a-reminder"></a>Um eine Mahnung auszugeben

Nach dem Erstellen von Mahnungen und dem Vornehmen von möglicherweise erforderlichen Änderungen können Sie entweder Testberichte drucken oder die Mahnungen registrieren.

Durch Registrieren einer Mahnung werden die Daten auf eine separate Seite für registrierte Mahnungen übertragen. Gleichzeitig werden die Mahnungsposten gebucht. Wurden Zinsen oder Gebühren berechnet, werden zudem Debitorenposten sowie Fibu-Posten gebucht.

Wenn eine Mahnung registriert wird, werden die Posten entsprechend Ihren Angaben auf der Seite **Mahnmethode** gebucht.. Diese Spezifikation legt fest, ob Zinsen und/oder Gebühren für den Debitor und in die Finanzbuchhaltung gebucht werden sollen. Die Seite **Debitorenbuchungsgruppen** bestimmt, auf welche Konten gebucht wird.

Für jeden Debitorenposten in der Zinsrechnung wird ein Posten auf der Seite **Mahnungs-/Zinsrechnungsposten** erzeugt.

Wenn das Kontrollkästchen **Zins buchen** oder **Zusätzliche Gebühren buchen** auf der Seite **Mahnungsbedingungen** aktiviert ist, werden außerdem die folgenden Posten erstellt:

- Ein Posten auf der Seite **Debitorenposten**
- Ein Forderungsposten auf dem jeweiligen Sachkonto
- Ein Zins- und/oder Gebührenposten auf dem jeweiligen Sachkonto

Zusätzlich kann das Registrieren der Mahnung zu MwSt.-Posten führen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion auch hier öffnet 4.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Mahnungen** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die entsprechenden Mahung aus und wählen Sie die Aktion **Ausgeben** aus.
3. Füllen Sie auf der Seite **Mahnungen ausgeben** die Felder nach Bedarf aus.
4. Wählen Sie die Schaltfläche **OK** aus.

Die Mahnung wird entweder gedruckt oder an eine festgelegte E-Mail als PDF-Dateianhang gesendet.

### <a name="to-cancel-an-issued-reminder"></a>Zum Stornieren der registrierten Mahnung.

Wenn fälschlicherweise Erinnerungen ausgegeben wurden, können Sie diese vor dem Versenden stornieren. Sie können dies entweder einzeln oder als Stapel ausführen.

1. Auf der Seite **Profilanpassungen** wählen Sie mindestens eine Zeile für die Seitenanpassungen aus, die Sie löschen möchten, und wählen Sie danach die Aktion **Löschen** aus.
2. Auf der Seite **Ausgestellte Manung stornieren** geben Sie die Felder wie nötig ein, und wählen Sie dann die Schaltfläche **OK**.


