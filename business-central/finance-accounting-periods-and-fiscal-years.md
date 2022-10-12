---
title: Mit Buchhaltungsperioden und Geschäftsjahren arbeiten
description: Erfahren Sie, wie Sie mit Buchhaltungsperioden arbeiten, um festzulegen, wann Ihr Unternehmen über Finanzleistung berichtet.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 100
ms.date: 08/25/2022
ms.author: bholtorf
ms.openlocfilehash: 93dcf334d65bda2859f8fcd91c976c3d85e6b18f
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605650"
---
# <a name="work-with-accounting-periods-and-fiscal-years"></a>Arbeiten mit Buchhaltungsperioden und Geschäftsjahren

Buchhaltungsperioden, auch Berichtsperioden genannt, sind Zeiträume, für die eine Firma oder Organisation über ihre finanzielle Leistung berichtet, indem sie z.B. ihre Gewinn- und Verlustrechnung oder ihre Bilanz erstellt. Normalerweise beziehen sich Buchhaltungsperioden auf das Geschäftsjahr der Konzernmandanten, die mehrere Buchhaltungsperioden enthalten. wie Monate oder Quartale.

Bei vielen Firmen stimmt das Geschäftsjahr nicht mit dem Kalenderjahr überein, zum Beispiel wenn das Geschäftsjahr am 30. Juni und nicht am 31. Dezember endet. Für neu erstellte Firmen kann das Geschäftsjahr sogar länger als 12 Monate sein.  

[!INCLUDE[prod_short](includes/prod_short.md)] benötigt Buchhaltungsperioden nur, wenn Sie eine Gewinn- und Verlustrechnung abschließen oder Datenkomprimierungsaufgaben ausführen möchten.

Sie können Buchhaltungsperioden in der Berichterstattung verwenden, z.B. wenn Sie Buchungen auf der Seite **Bilanz/Budget** überprüfen, auf der das Berichtsintervall angegeben ist. Eine der Optionen, die Sie angeben können, ist die Berichterstattung nach Buchhaltungsperioden. Sie können auch einen Finanzbericht erstellen, der die Ergebnisse für verschiedene Buchhaltungsperioden vergleicht.

## <a name="creating-a-new-fiscal-year"></a>Ein neues Geschäftsjahres eröffnen

Sie können Buchhaltungsperioden in großen Mengen erstellen, indem Sie den Batchauftrag **Geschäftsjahr erstellen** verwenden, oder dies manuell tun.

### <a name="how-to-create-accounting-periods-in-bulk"></a>So erstellen Sie Buchhaltungsperioden im Batch

Verwenden Sie die Stapelverarbeitung **Geschäftsjahr eröffnen**, um ein Geschäftsjahr in Perioden derselben Länge zu unterteilen.  

1. Wählen Sie das ![Suchen Sie nach Seite oder Bericht.](media/ui-search/search_small.png "Nach dem Symbol für „Seite“ oder „Bericht“ suchen") Symbol, geben Sie **Buchhaltungsperioden** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Jahr erstellen** aus.
3. Geben Sie im Feld **Startdatum** das Datum ein, an dem das Geschäftsjahr beginnt.  
4. Im Feld **Anzahl Perioden** geben Sie die Anzahl der Buchhaltungsperioden ein, in die sich das Geschäftsjahr gliedert. Es kann bis zu 365 Perioden in einem Jahr geben.  
5. In dem Feld **Periodenlänge** geben Sie eine Zeitspanne für die einzelnen Perioden ein. Die Bezeichnungen der Perioden sind 1M für einen Monat, 1Q für ein Quartal und 1Y für ein Jahr.  
6. Wählen Sie **OK** aus.  

### <a name="how-to-create-accounting-periods-manually"></a>So erstellen Sie Buchhaltungsperioden in einer Massenoperation manuell

Wenn die Buchhaltungsperioden in Ihrem Geschäftsjahr unterschiedliche Laufzeiten haben, wie z.B. der im Einzelhandel verwendete 4-4-5-Kalender, können Sie dies manuell festlegen.  
  
1. Wählen Sie die ![Suche nach Seite oder Bericht.](media/ui-search/search_small.png "Suche nach dem Symbol für Seite oder Bericht") Symbol, geben Sie **Buchhaltungsperioden** ein und wählen Sie dann den entsprechenden Link.  
2. Geben Sie im Feld **Startdatum** das Datum ein, an dem das Geschäftsjahr beginnt. Geben Sie in dem Feld **Name** den Namen des Monats ein.  
3. Wählen Sie das Kontrollkästchen **Neues Geschäftsjahr**, um anzugeben, dass dies die erste Periode im Jahr ist. [!INCLUDE[prod_short](includes/prod_short.md)] verwendet diese Periode, um zu ermitteln, welche Periode am Ende des Geschäftsjahres zu schließen ist.
4. Wiederholen Sie Schritt 2 und 3 für jede verbleibende Periode.  

## <a name="closing-a-fiscal-year"></a>Abschließen eines Geschäftsjahres

Das Geschäftsjahr abzuschließen ist eine der Aufgaben für das Schließen der Bücher. Nachdem Sie das Geschäftsjahr abgeschlossen haben, sind die Felder **Abgeschlossen** und **Datum gesperrt** für alle Perioden des Jahres aktiviert. Sie können ein Jahr nicht erneut öffnen oder die Kontrollkästchen deaktivieren.

> [!NOTE]  
> Sie müssen immer mindestens ein offenen Geschäftsjahres haben. Wenn Sie ein Jahr abschließen, überprüfen Sie, dass ein neues Jahr erstellt wurde. Beachten Sie, dass Sie nach dem Abschluss eines Geschäftsjahres das Startdatum des folgenden Geschäftsjahres nicht mehr ändern können.

1. Wählen Sie das ![Suchen Sie nach Seite oder Bericht.](media/ui-search/search_small.png "Symbol „Suche nach Seite oder Bericht“") Symbol. Geben Sie **Buchhaltungsperioden** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Jahr beenden** aus.  

## <a name="posting-entries-to-a-closed-fiscal-year"></a>Buchungen für ein abgeschlossenes Geschäftsjahr

Auch wenn ein Geschäftsjahr abgeschlossen wurde, können hierfür noch Sachposten gebucht werden. In diesen Fällen wird in den Posten vermerkt, dass die Buchung in einem abgeschlossenen Geschäftsjahr erfolgte, d. h., das Feld **Nachbuchung** wird mit einem Häkchen versehen. Standardmäßig wird das Kontrollkästchen auf der Seite nicht angezeigt, aber Sie können es hinzufügen. Als nächsten Schritt schließen Sie die GuV-Konten und übertragen das Jahresergebnis an ein Konto in der Bilanz. Dies müssen Sie jedes Mal wiederholen, wenn Sie in ein abgeschlossenes Geschäftsjahr gebucht haben.

## <a name="see-also"></a>Siehe auch

[Bucher schließen](year-close-books.md)  
[Jahre und Perioden abschließen](year-close-years-periods.md)  
[Wie Sie mit Financial Reports arbeiten](bi-how-work-account-schedule.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
