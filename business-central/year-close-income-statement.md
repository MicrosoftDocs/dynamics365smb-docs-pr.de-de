---
title: Schließen Sie GuV-Konten
description: 'Am Jahresende beispielsweise müssen Sie die Stapelverarbeitung "GuV-Konten Nullstellung" laufen lassen, um die Buchhaltungsperioden zu schließen, aus der sich das Geschäftsjahr zusammensetzt.'
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'year closing, close accounting period, close fiscal year, bank account detailed trial balance'
ms.date: 06/25/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="closing-income-statement-accounts"></a>GuV-Konten Nullstellung
Wenn ein Geschäftsjahr zu Ende ist, müssen Sie die Perioden, aus denen es besteht, abschließen. Verwenden Sie dazu den Stapelverarbeitungsjob **GuV-Konten Nullstellung**. Dieser Job überträgt die Ergebnisse des Jahrs auf ein Bilanzkonto und führt die GuV-Kontennullstellung durch. Hierfür erstellen Sie Zeilen in einem Buch.-Blatt, die Sie dann buchen können.

## <a name="to-run-the-close-income-statement-batch-job"></a>Verwenden Sie dazu den Stapelverarbeitungsjob GuV-Konten Nullstellung.
1. Schließen Sie das Geschäftsjahr ab. Das Geschäftsjahr muss geschlossen werden, bevor die Stapelverarbeitung aufgerufen werden kann. Weitere Informationen finden Sie unter [Abschließen von Buchhaltungsperioden](year-close-account-periods.md).
2. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Gewinn- und Verlustrechnung Nullstellung abschließen** ein, und wählen Sie dann den zugehörigen Link.
3. Wählen Sie die Schaltfläche **OK**, um den Batchauftrag zu starten.

## <a name="about-the-close-income-statement-batch-job"></a>Mehr Informationen zum Stapelverarbeitungsjob GuV-Konten Nullstellung.
Mithilfe dieses Batchauftrags werden alle Sachkonten der Art "GuV" bearbeitet und Buchungszeilen erzeugt, die eine Nullstellung ihrer Salden bewirken. Anders ausgedrückt,entspricht jeder Posten der Summe aller Sachposten auf dem Konto im Geschäftsjahr. Diese neuen Posten werden in ein Buch.-Blatt eingefügt, in dem Sie ein Gegenkonto und ein Abschlusskonto GuV in der Bilanz angeben müssen, bevor diese gebucht werden. Wenn Sie das Buch.-Blatt buchen, wird ein Posten auf jedes GuV-Konto gebucht, sodass der Saldo des Kontos Null ist und gleichzeitig das Jahresergebnis in die Bilanz übertragen wird.

Sie müssen das Buch.-Blatt manuell buchen. Durch den Batchauftrag erfolgt keine automatische Buchung der Posten, es sei denn, es wird eine Berichtswährung verwendet. Wenn eine zusätzliche Berichtswährung verwendet wird, bucht die Stapelverarbeitung die Posten direkt in die Finanzbuchhaltung.

Das Datum, das von dem Batchauftrag in die Zeilen eingefügt wird, ist stets das Ultimodatum des Geschäftsjahrs. Das Ultimodatum ist ein fiktives Datum zwischen dem letzten Tag des alten und dem ersten Tag des neuen Geschäftsjahres. Der Vorteil des Buchens zu einem Ultimodatum liegt darin, dass die Salden des Geschäftsjahres mit normalen Datumsangaben erhalten bleiben.

Die Stapelverarbeitung **GuV Konten-Nullstellung** kann mehrmals aufgerufen werden. Sie können im vorigen Geschäftsjahr buchen, selbst wenn die GuV Konten Nullstellung bereits vorgenommen wurde, sofern Sie die Stapelverarbeitung erneut ausführen.

## <a name="see-also"></a>Siehe auch

[Schließen der Bücher](year-close-books.md)  
[Jahresabschlussbuchung buchen](year-how-post-year-end-close-entry.md)  
[Arbeiten mit Buchhaltungsperioden und Geschäftsjahren](finance-accounting-periods-and-fiscal-years.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
