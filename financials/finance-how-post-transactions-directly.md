---
title: Erfassen von Aufwendungen oder Umsatz direkt in der Finanzbuchhaltung| Microsoft Docs
description: "Für Geschäftsaktivitäten, die nicht in einem Beleg festgehlaten sind, wie kleinere Aufwendungen oder Zahlungseingänge, können Sie die entsprechenden Transaktionen erstellen, indem Sie die Buch.-Blattzeilen im Fibu Buch.-Blatt buchen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 06/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7fa0d6b604a60e000208287546d831690a914931
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-post-transactions-directly-to-the-general-ledger"></a>Vorgehensweise: Transaktionen direkt in die Finanzbuchhaltung buchen
Die meisten Finanztransaktionen werden in der Finanzbuchhaltung von Geschäftsbelegen wie Einkaufsrechnungen und Verkaufsaufträge gebucht. Für Geschäftsaktivitäten, die nicht in einem Beleg in[!INCLUDE[d365fin](includes/d365fin_md.md)] festgehlaten sind, wie kleinere Aufwendungen oder Zahlungseingänge, können Sie die entsprechenden Transaktionen erstellen, indem Sie die Buch.-Blattzeilen im **Fibu Buch.-Blatt** buchen.

Fibu Buch.-Blätter dienen zum Buchen auf Sachkonten sowie auf andere Konten wie Bank-, Debitoren-, Kreditoren- oder Anlagekonten. Bei der Buchung mit einem Fibu Buch.-Blatt werden immer Posten für Sachkonten erstellt. Dies gilt auch, wenn beispielsweise eine Buch.-Blattzeile auf ein Debitorenkonto gebucht wird, da ein Posten im Rahmen einer Buchungsgruppe auf ein Fibu-Debitorenkonto gebucht wird. Sie können Ihre Version eines Fibu Buch.-Blattes anpassen, indem Sie einen Buch.-Blattnamen oder eine Vorlage einrichten. Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)

Anders als für Posten, die mit Belegen gebucht werden, die einen Gutschriftsvorgang benötigen, können Sie Posten ordnungsgemäß stornieren, die mit dem Buch.-Blatt gebucht werden. Weitere Informationen finden Sie unter [Stornieren von Buch.-Blattbuchungen](finance-how-reverse-journal-posting.md).

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a>Transaktionen direkt in die Finanzbuchhaltung buchen
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Fibu Buch.-Blatt** ein. Wählen Sie dann den zugehörigen Link aus.
2. Öffnet das entsprechende Fibu Buch.-Blatt Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)
3. Füllen Sie die Felder in einer neuen Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    
4. Wiederholen Sie Schritt 3 für jede separate Transaktion, die Sie buchen möchten.

    > [!TIP]  
    > Wenn Sie Zeilen mit mehreren Transaktion über eine Gegenkontozeile, beispielsweise für das Bankkonto eingeben möchten, wählen Sie das Kontrollkästchen **Ausgleichsbetrag vorschlagen** in der Zeile für Ihren Stapel im **Fibu Buch.-Blattnamen** aus. Dann werden das Feld **Betrag** auf der Gegenkontozeile automatisch mit dem Wert ausgefüllt, der erforderlich ist, um Transaktionen auszugleichen.
5. Wählen Sie die **Buchen** Aktion aus, um die Transaktionen in den angegebenen Sachkonten zu erfassen.

## <a name="see-also"></a>Siehe auch
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[So geht's: Buch.-Blatt-Buchungen stornieren](finance-how-reverse-journal-posting.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

