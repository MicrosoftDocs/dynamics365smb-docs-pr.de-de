---
title: Erfassen von Aufwendungen oder Umsatz direkt in der Finanzbuchhaltung| Microsoft Docs
description: Für Geschäftsaktivitäten, die nicht in einem Beleg festgehlaten sind, wie kleinere Aufwendungen oder Zahlungseingänge, können Sie die entsprechenden Transaktionen erstellen, indem Sie die Buch.-Blattzeilen im Fibu Buch.-Blatt buchen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 11/27/2018
ms.author: sgroespe
ms.openlocfilehash: a1e7137cdc08fb558b6a6d423ce9524fa47eec16
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "798316"
---
# <a name="post-transactions-directly-to-the-general-ledger"></a>Buchen von Transaktionen direkt in der Finanzbuchhaltung

Fibu Buch.-Blätter dienen zum Buchen auf Sachkonten sowie auf andere Konten wie Bank-, Debitoren-, Debitoren- oder Mitarbeiterkonten.  

Eine typische Verwendung des Fibu Buch.-Blatt gehört die Buchung der Kosten der Mitarbeiter während  Geschäftsaktivitäten zur späteren Rückvergütung. Weitere Informationen finden Sie unter [Erstatten Sie die Ausgaben der Mitarbeiter zurück](finance-how-record-reimburse-employee-expenses.md).

Fibu Buch.-Blätter dienen zum Buchen auf Sachkonten sowie auf andere Konten wie Bank-, Debitoren-, Kreditoren- oder Mitarbeiterkonten. Bei der Buchung mit einem Fibu Buch.-Blatt werden immer Posten für Sachkonten erstellt. Dies gilt auch, wenn beispielsweise eine Buch.-Blattzeile auf ein Debitorenkonto gebucht wird, da ein Posten im Rahmen einer Buchungsgruppe auf ein Fibu-Debitorenkonto gebucht wird. Sie können Ihre Version eines Fibu Buch.-Blattes anpassen, indem Sie einen Buch.-Blattnamen oder eine Vorlage einrichten. Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)

Anders als für Posten, die mit Belegen gebucht werden, die einen Gutschriftsvorgang benötigen, können Sie Posten ordnungsgemäß stornieren, die mit dem Buch.-Blatt gebucht werden. Weitere Informationen finden Sie unter [Gewusst wie: Buchungen rückgängig machen](finance-how-reverse-journal-posting.md).

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a>Transaktionen direkt in die Finanzbuchhaltung buchen

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Allgemeine Buch.-Blätter** ein, und wählen dann den zugehörigen Link aus.
2. Öffnet das entsprechende Fibu Buch.-Blatt Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)
3. Füllen Sie die Felder in einer neuen Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. Wiederholen Sie Schritt 3 für jede separate Transaktion, die Sie buchen möchten.

    > [!TIP]  
    > Wenn Sie Zeilen mit mehreren Transaktion über eine Gegenkontozeile, beispielsweise für das Bankkonto eingeben möchten, wählen Sie das Kontrollkästchen **Ausgleichsbetrag vorschlagen** in der Zeile für Ihren Stapel im **Fibu Buch.-Blattnamen** aus. Dann werden das Feld **Betrag** auf der Gegenkontozeile automatisch mit dem Wert ausgefüllt, der erforderlich ist, um Transaktionen auszugleichen.
5. Wählen Sie die **Buchen** Aktion aus, um die Transaktionen in den angegebenen Sachkonten zu erfassen.

## <a name="see-also"></a>Siehe auch

[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[Geschäftsverwandte Ausgaben der Beschäftigten aufzeichnen und zurückzahlen](finance-how-record-reimburse-employee-expenses.md)  
[Buchungen stornieren](finance-how-reverse-journal-posting.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
