---
title: SEPA Lastschriftzahlungen | Microsoft Docs
description: Wenn ein Lastschrifteinzug von Ihrer Bank erfolgreich verarbeitet wird, können Sie den Eingang der Zahlungen für die betreffenden Verkaufsrechnungen buchen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-collect-payments-with-sepa-direct-debit
ms.openlocfilehash: 6c646575ba803358aa00309ce02742423bcc7de8
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "930754"
---
# <a name="post-sepa-direct-debit-payment-receipts"></a>SEPA-Lastschrifteinzug-Zahlungseingänge buchen
Wenn ein Lastschrifteinzug von Ihrer Bank erfolgreich verarbeitet wird, können Sie den Eingang der Zahlungen für die betreffenden Verkaufsrechnungen buchen. Weitere Informationen finden Sie unter [SEPA-Lastschrifteinzugsposten erstellen und in eine Bankdatei exportieren](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)  

Sie können der Zahlungseingang direkt aus dem **Lastschriften** oder im **Direct Debit Collect. Posten** buchen. Sie können auch die Arbeit an einen anderen Benutzer übertragen, indem Sie die zugehörigen Buch.-Blattzeilen vorbereiten.  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-page"></a>Buchen eines Lastschrifteingangs aus der Lastschrift-Einzugsseite  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren?“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Lastschriften** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie eine Zeile für die Lastschrift-Einzugserfassung, die in eine Bankdatei exportiert und von der Bank erfolgreich verarbeitet wurde. Weitere Informationen finden Sie unter [SEPA-Lastschrifteinzugsposten erstellen und in eine Bankdatei exportieren](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)  
3. Wählen Sie die Aktion **Zahlungseingang buchen** aus.  
4. Füllen Sie auf der Seite **Lastschrift buchen** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Lastschriftnr.**|Geben Sie den Lastschrifteinzug an, für den Sie den Zahlungseingang buchen wollen.|  
    |**Fibu Buch.-Blattvorlage**|Geben Sie an, welche Fibu Buch.-Blattvorlage zum Buchen des Zahlungseingangs verwendet werden soll, etwa die Vorlage für Bareingänge.|  
    |**Fibu Buch.-Blattname**|Geben Sie an, welcher Fibu Buch.-Blattname für die Buchung des Zahlungseingangs verwendet werden soll.|  
    |**Nur Buch.-Blatt erstellen**|Markieren Sie dieses Kontrollkästchen, wenn Sie den Zahlungseingang nicht buchen wollen, wenn Sie die Schaltfläche **OK** wählen. Der Zahlungseingang wird in dem angegebenen Buch vorbereitet und erst gebucht, wenn jemand die fraglichen Buch.-Blatt-Zeilen bucht.|  

5. Wählen Sie die Schaltfläche **OK** aus.  

## <a name="see-also"></a>Siehe auch  
 [Erfassen von Zahlungen per Lastschriftverfahren SEPA](finance-collect-payments-with-sepa-direct-debit.md)   
 [Verkauf](sales-manage-sales.md)
