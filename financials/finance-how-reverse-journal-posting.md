---
title: "Eine Buch.-Blatt-Buchung rückgängig machen, indem ein Rückbuchung gemacht wird| Microsoft Docs"
description: "Wenn Sie fehlerhafte Buchungen im Fibu Buch.-Blatt vorgenommen haben, können Sie die Funktion verwenden, um die korrekte Buchung mit einem Protokoll zu stornieren."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 06/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 8126a53d59e72276eb1558fd65fe3c0cd53600cc
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-reverse-journal-posting"></a>So geht's: Buch.-Blatt-Buchungen stornieren
Zum Stornieren (Rückgängig machen) fehlerhafter Buch.-Blattbuchungen wählen Sie einen Posten und erstellen einen Korrekturposten (ein Posten, die mit dem ursprünglichen Posten identisch ist, jedoch im Betragsfeld ein umgekehrtes Vorzeichen aufweist) mit derselben Belegnummer und demselben Belegdatum wie der ursprüngliche Posten. Nachdem Sie einen Posten storniert haben, müssen Sie den Korrekturposten erstellen.

Storniert werden können nur Posten, die in eine Zeile eines Fibu Buch.-Blattes gebucht wurden. Ein Posten kann nur einmal storniert werden.

Weitere Informationen zum Buchen eines Fibu Buch.-Blatt, siehe [Vorgehensweise: Beitrags-Transaktionen in die Finanzbuchhaltung](finance-how-post-transactions-directly.md).

Posten können in allen **Posten** storniert werden. Das folgende Verfahren basiert auf dem **Sachposten** Fenster.

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a>Um die Buch.-Blatt-Buchung eines Sachpostens zu stornieren
1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Finanzbuchhaltung einrichten** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie den Posten, den Sie stornieren möchten, und wählen die **Transaktion stornieren** Aktion aus. Beachten Sie, das sie aus einer Buch.-Blatt-Buchung stammen muss.
3. Im Fenster **Transaktionsposten stornieren** wählen Sie den entsprechenden Posten, und wählen die **Stornieren** Aktion aus.
4. Klicken Sie auf die Schaltfläche **Ja** auf der Bestätigungsnachricht.

## <a name="see-also"></a>Siehe auch
[Vorgehensweise: Transaktionen direkt in die Finanzbuchhaltung buchen](finance-how-post-transactions-directly.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

