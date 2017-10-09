---
title: "Gschäftsrelevante Ausgaben der Beschäftigten aufzeichnen und zurückzahlen | Microsoft Docs"
description: "Buchen Sie die Kosten der Mitarbeiter mit dem Fibu Buch.-Blatt zu dem Konto und buchen Sie später die Zahlung an das Bankkonto des Mitarbeiters, dem die geschäftsverwandten Ausgaben zurückzuerstatten sind."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 8674fcc050e11c9ecb1c423fc5048c1ef630e1ac
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-record-and-reimburse-employees-expenses"></a>Vorgehensweise: Geschäftsverwandte Ausgaben der Beschäftigten aufzeichnen und zurückzahlen
[!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt Transaktionen für Mitarbeiter auf ähnliche Weise wie für Kreditoren. Entsprechend bestehen Mitarbeiterbuchungsgruppen, um sicherzustellen, dass Mitarbeiterposten auf den entsprechenden Konten in der Finanzbuchhaltung gebucht werden.

> [!NOTE]  
> Mitarbeitertransaktionen können nur in der lokalen Währung gebucht werden. Vergütungszahlungen für Mitarbeiter unterstützen keine Skonti und Zahlungstoleranzen.

Wenn die Mitarbeiter ihr eigenes Geld für die Geschäftsaktivitäten ausgeben, können Sie die Kosten auf das Konto des Mitarbeiters buchen. Dann können Sie die Kosten den Mitarbeiter zurückerstatten, indem Sie eine Zahlung auf das  Bankkonto des Mitarbeiters leisten, ähnlich wie Sie Kreditoren bezahlen.

## <a name="to-record-an-employees-expense"></a>Um die Ausgaben eines Mitarbeiters tz erfassen
Sie buchen die Ausgaben der Mitarbeiter im Fenster **Fibu Buch.-Blatt**.
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Fibu Buch.-Blatt** ein. Wählen Sie dann den zugehörigen Link aus.
2. Öffnet das entsprechende Fibu Buch.-Blatt Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)
3. Füllen Sie die Felder in einer neuen Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    
4. Wiederholen Sie Schritt 3 für alle Ausgaben, die der Beschäftigte hatte.

    > [!TIP]  
    > Wenn Sie Zeilen mit mehreren Transaktion über eine Gegenkontozeile, beispielsweise für das Bankkonto des Mitarbeiters eingeben möchten, wählen Sie das Kontrollkästchen **Ausgleichsbetrag vorschlagen** in der Zeile für Ihren Stapel im **Fibu Buch.-Blattnamen** aus. Dann werden das Feld **Betrag** auf der Gegenkontozeile automatisch mit dem Wert ausgefüllt, der erforderlich ist, um Transaktionen auszugleichen.
5. Wählen Sie die **Buchen** Aktion aus, um die Ausgaben des Kontos des Mitarbeiters zu erfassen.

## <a name="to-reimburse-an-employee"></a>Rückerstattung für Mitarbeiter
Sie zahlen die Kosten dem Mitarbeiter zurück, indem Sie Zahlungen zu dem Bankkonto im Fenster **Zahlungsausgangs Buch.-Blatt** buchen.
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Zahlungs-Buchblatt** ein und wählen den zugehörenden Link aus.
2. Öffnet das entsprechende Zahlungs-Fibu Buch.-Blatt Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)
3. Füllen Sie die Felder je nach Bedarf aus. Weitere Informationen finden Sie unter [Zahlungen durchführen](payables-make-payments.md).
4. Wählen Sie alternativ die **Mitarbeiter-Zahlung vorschlagen** Aktion aus, um automatisch Buch.-Blattzeilen für offene Mitarbeitervergütungen einzufügen.
5. Wählen Sie die Aktion **Buchen**, um die Rückerstattung zu erfassen.  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a>Um Vergütungen mit Mitarbeiterposten ausgleichen
Sie gleichen Mitarbeiterzahlungen in den entsprechenden offenen Mitarbeiterposten gleich aus, wie Sie dies für Kreditorenzahlungen tun, zum Beispiel im Fenster **Zahlungsabstimmungsbuch.-Blatt** in den entsprechenden Bankkontoauszugsposten. Weitere Informationen finden Sie unter [Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md). Alternativ können Sie im Fenster **Mitarbeiter-Posten** den Eintrag manuell eingeben. Weitere Informationen finden Sie unter [Vorgehensweise: Manuelle Abstimmung von Zahlungen](payables-how-apply-purchase-transactions-manually.md).  

## <a name="see-also"></a>Siehe auch
[Vorgehensweise: Transaktionen direkt in die Finanzbuchhaltung buchen](finance-how-post-transactions-directly.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[So geht's: Buchungen stornieren](finance-how-reverse-journal-posting.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

