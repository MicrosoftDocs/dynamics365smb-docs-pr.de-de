---
title: Schließen Sie GuV-Berichte | Microsoft Docs
description: Am Jahresende beispielsweise müssen Sie die Stapelverarbeitung "GuV-Konten Nullstellung" laufen lassen, um die Buchhaltungsperioden zu schließen, aus der sich das Geschäftsjahr zusammensetzt.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2019
ms.author: jswymer
ms.openlocfilehash: fd811a1a472efe53fe1c16bd5c301925d424f274
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2313928"
---
# <a name="close-income-statement-accounts"></a>Schließen Sie GuV-Konten
Wenn ein Geschäftsjahr vorbei ist, müssen die Perioden, aus denen es besteht, geschlossen werden. Verwenden Sie dazu den Stapelverarbeitungsjob **GuV-Konten Nullstellung**. Dieser Job überträgt die Ergebnisse des Jahrs auf ein Bilanzkonto und führt die GuV-Kontennullstellung durch. Hierfür erstellen Sie Zeilen in einem Buch.-Blatt, die Sie dann buchen können.

## <a name="to-run-the-close-income-statement-batch-job"></a>Verwenden Sie dazu den Stapelverarbeitungsjob GuV-Konten Nullstellung.
1. Schließen Sie das Geschäftsjahr ab. Das Geschäftsjahr muss geschlossen werden, bevor die Stapelverarbeitung aufgerufen werden kann. Weitere Informationen finden Sie unter [Abschließen von Buchhaltungsperioden](year-close-account-periods.md).
2. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **GuV Konten Nullstellung** ein, und wählen dann den zugehörigen Link aus.
3. Wählen Sie die Schaltfläche **OK**, um den Batchauftrag zu starten.

## <a name="about-the-close-income-statement-batch-job"></a>Mehr Informationen zum Stapelverarbeitungsjob GuV-Konten Nullstellung.
Mithilfe dieses Batchauftrags werden alle Sachkonten der Art "GuV" bearbeitet und Buchungszeilen erzeugt, die eine Nullstellung ihrer Salden bewirken. Anders ausgedrückt,entspricht jeder Posten der Summe aller Sachposten auf dem Konto im Geschäftsjahr. Diese neuen Posten werden in ein Buch.-Blatt eingefügt, in dem Sie ein Gegenkonto und ein Abschlusskonto GuV in der Bilanz angeben müssen, bevor diese gebucht werden. Wenn Sie das Buch.-Blatt buchen, wird ein Posten auf jedes GuV-Konto gebucht, sodass der Saldo des Kontos Null ist und gleichzeitig das Jahresergebnis in die Bilanz übertragen wird.

Sie müssen das Buch.-Blatt manuell buchen. Durch den Batchauftrag erfolgt keine automatische Buchung der Posten, es sei denn, es wird eine Berichtswährung verwendet. Wenn eine zusätzliche Berichtswährung verwendet wird, bucht die Stapelverarbeitung die Posten direkt in die Finanzbuchhaltung.

Das Datum, das von dem Batchauftrag in die Zeilen eingefügt wird, ist stets das Ultimodatum des Geschäftsjahrs. Das Ultimodatum ist ein fiktives Datum zwischen dem letzten Tag des alten und dem ersten Tag des neuen Geschäftsjahres. Der Vorteil des Buchens zu einem Ultimodatum liegt darin, dass die Salden des Geschäftsjahres mit normalen Datumsangaben erhalten bleiben.

Die Stapelverarbeitung **GuV Konten-Nullstellung** kann mehrmals aufgerufen werden. Sie können im vorigen Geschäftsjahr buchen, selbst wenn die GuV Konten Nullstellung bereits vorgenommen wurde, sofern Sie die Stapelverarbeitung erneut ausführen.

## <a name="see-also"></a>Siehe auch
[Schließen der Bücher](year-close-books.md)  
[So buchen Sie den Jahresabschlussposten](year-how-post-year-end-close-entry.md)  
[Ein neues Geschäftsjahres eröffnen](finance-how-open-new-fiscal-year.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
