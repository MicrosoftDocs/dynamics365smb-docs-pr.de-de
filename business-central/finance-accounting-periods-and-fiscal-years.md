---
title: Mit Buchhaltungsperioden und Geschäftsjahren arbeiten | Microsoft Docs
description: Erfahren Sie, wie Sie mit Buchhaltungsperioden arbeiten, um festzulegen, wann Ihr Unternehmen über Finanzleistung berichtet.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/13/2018
ms.author: bholtorf
ms.openlocfilehash: 6f760f546ea02fbc19473c70eb26d8b4c47c0987
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "799354"
---
# <a name="working-with-accounting-periods-and-fiscal-years"></a>Mit Buchhaltungsperioden und Geschäftsjahren arbeiten
Buchhaltungsperioden, die auch als Meldezeiträume betragen, geben für die Zeiträume Mandanten- oder Organisationsberichtsfinanzleistung - beispielsweise durch das Generieren eines GuV-Kontos oder eines Bilanzkontos. Normalerweise beziehen sich Buchhaltungsperioden auf das Geschäftsjahr der Konzernmandanten, die mehrere Buchhaltungsperioden enthalten. wie Monate oder Quartale.

Für viele Unternehmen stimmt das Geschäftsjahr nicht mit dem Kalenderjahr überein. Beispielsweise kann das Geschäftsjahr am 30. Juni anstatt am 31. Dezember enden. Bei neu erstellten Mandanten kann das Steuerjahr tatsächlich länger als 12 Monate  sein. 

[!INCLUDE[d365fin](includes/d365fin_md.md)] erfordert nur Buchhaltungsperioden, wenn Sie nur einen GuV schließen möchten, oder Datenkomprimierungsaufgaben ausführen. 

Sie können die Buchhaltungsperioden für Meldungen verwenden. Wenn Sie gebuchte Posten auf der Seite **Saldo/Budget** überprüfen, in der die bestimmte Berichtsintervalle definiert werden können. Eine der Optionen, die Sie möglicherweise benötigen, um nach Buchhaltungsperiode zu melden. Sie können ein Kontenschema auch erstellen, um die Ergebnisse für verschiedene Perioden zu vergleichen.

## <a name="creating-a-new-fiscal-year"></a>Ein neues Geschäftsjahres eröffnen
Sie können Buchhaltungsperioden in einer Massenoperation erstellen, indem Sie die Stapelverarbeitung **Geschäftsjahr eröffnen** verwenden oder dies manuell tun.

### <a name="how-to-create-accounting-periods-in-bulk"></a>So erstellen Sie Buchhaltungsperioden in einer Massenoperation
Verwenden Sie die Stapelverarbeitung **Geschäftsjahr eröffnen**, um ein Geschäftsjahr in Perioden derselben Länge zu unterteilen.  

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Buchhaltungsperioden** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Jahr erstellen** aus.  <!--What about the Scheduling option? Should we mention that? There's also the Report Output Type field...-->
3. Geben Sie im Feld **Startdatum** das Datum ein, an dem das Geschäftsjahr beginnt.  
4. Im Feld **Anzahl Perioden** geben Sie die Anzahl der Buchhaltungsperioden ein, in die sich das Geschäftsjahr gliedert. Es kann bis zu 365 Perioden in einem Jahr geben.  
5. In dem Feld **Periodenlänge** geben Sie eine Zeitspanne für die einzelnen Perioden ein. Beispielsweise 1M für einen Monat, 1Q für ein Quartal und 1J für ein Jahr.  
6. Wählen Sie **OK** aus.  

### <a name="how-to-create-accounting-periods-manually"></a>So erstellen Sie Buchhaltungsperioden in einer Massenoperation manuell
Wenn die Buchhaltungsperioden in dem Geschäftsjahr verschiedene Dauern aufweisen, wie der Kalender 4-4-5, der im Einzelhandel verwendet wird, können Sie ihn manuell einrichten.  
  
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Buchhaltungsperioden** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Geben Sie im Feld **Startdatum** das Datum ein, an dem das Geschäftsjahr beginnt. Geben Sie in dem Feld **Name** den Namen des Monats ein.  
3. Wählen Sie das Kontrollkästchen **Neues Geschäftsjahr**, um anzugeben, dass dies die erste Periode im Jahr ist. [!INCLUDE[d365fin](includes/d365fin_md.md)] verwendet diese Periode, um zu ermitteln, welche  Periode am Ende des Geschäftsjahres zu schließen ist.
4. Wiederholen Sie Schritt 2 und 3 für jede verbleibende Periode.  

## <a name="closing-a-fiscal-year"></a>Geschäftsjahr beenden
Das Geschäftsjahr abzuschließen ist eine der Aufgaben für das Schließen der Bücher. Nachdem Sie das Geschäftsjahr abgeschlossen haben, sind die Felder **Abgeschlossen** und **Datum gesperrt** für alle Perioden des Jahres aktiviert. Sie können ein Jahr nicht erneut öffnen oder die Kontrollkästchen deaktivieren.

> [!NOTE]  
>  Sie müssen immer mindestens ein offenen Geschäftsjahres haben. Wenn Sie ein Jahr abschließen, überprüfen Sie, dass ein neues Jahr erstellt wurde. Beachten Sie, dass Sie nach dem Abschluss eines Geschäftsjahres das Startdatum des folgenden Geschäftsjahres nicht mehr ändern können.

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Buchhaltungsperioden** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Jahr beenden** aus.  

## <a name="posting-entries-to-a-closed-fiscal-year"></a>Posten in einem abgeschlossenen Geschäftsjahr buchen
Auch wenn ein Geschäftsjahr abgeschlossen wurde, können hierfür noch Sachposten gebucht werden. In diesen Fällen wird in den Posten vermerkt, dass die Buchung in einem abgeschlossenen Geschäftsjahr erfolgte, d. h., das Feld **Nachbuchung** wird mit einem Häkchen versehen. Standardmäßig wird das Kontrollkästchen auf der Seite nicht angezeigt, aber Sie können es hinzufügen. Als nächsten Schritt schließen Sie die GuV-Konten und übertragen das Jahresergebnis an ein Konto in der Bilanz. Dies müssen Sie jedes Mal wiederholen, wenn Sie in ein abgeschlossenes Geschäftsjahr gebucht haben.

## <a name="see-also"></a>Siehe auch
[Bucher schließen](year-close-books.md)  
[Beenden von Jahresabschluss und Perioden](year-close-years-periods.md)  
[Vorgehensweise: Arbeiten mit Kontenschemata](bi-how-work-account-schedule.md)  
  





