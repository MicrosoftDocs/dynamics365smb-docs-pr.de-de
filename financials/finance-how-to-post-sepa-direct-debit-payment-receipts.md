---
title: SEPA Lastschriftzahlungen | Microsoft Docs
description: "Wenn ein Lastschrifteinzug von Ihrer Bank erfolgreich verarbeitet wird, können Sie den Eingang der Zahlungen für die betreffenden Verkaufsrechnungen buchen."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5beb5f6795bd7f4943a6ed9d8b691c05fc5ecb63
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-post-sepa-direct-debit-payment-receipts"></a>Vorgehensweise: SEPA-Lastschrifteinzug-Zahlungseingänge buchen
Wenn ein Lastschrifteinzug von Ihrer Bank erfolgreich verarbeitet wird, können Sie den Eingang der Zahlungen für die betreffenden Verkaufsrechnungen buchen. Weitere Informationen finden Sie unter [Vorgehensweise: SEPA-Lastschrifteinzugsposten erstellen und in eine Bankdatei exportieren](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)  

Sie können der Zahlungseingang direkt aus dem **Lastschriften** oder im **Direct Debit Collect. Posten** buchen. Sie können auch die Arbeit an einen anderen Benutzer übertragen, indem Sie die zugehörigen Buch.-Blattzeilen vorbereiten.  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-window"></a>Buchen eines Lastschrifteingangs aus dem Lastschrift-Einzugsfenster  
1. Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Berichtsymbol suchen") und geben **Lastschriften** ein und wählen dann den zugehörigen Link aus.  
2. Wählen Sie eine Zeile für die Lastschrift-Einzugserfassung, die in eine Bankdatei exportiert und von der Bank erfolgreich verarbeitet wurde. Weitere Informationen finden Sie unter [Vorgehensweise: SEPA-Lastschrifteinzugsposten erstellen und in eine Bankdatei exportieren](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)  
3. Wählen Sie die Aktion **Zahlungseingang buchen** aus.  
4. Füllen Sie im Fenster **Lastschrift erstellen** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Lastschriftnr.**|Geben Sie den Lastschrifteinzug an, für den Sie den Zahlungseingang buchen wollen.|  
    |**Fibu Buch.-Blattvorlage**|Geben Sie an, welche Fibu Buch.-Blattvorlage zum Buchen des Zahlungseingangs verwendet werden soll, etwa die Vorlage für Bareingänge.|  
    |**Fibu Buch.-Blattname**|Geben Sie an, welcher Fibu Buch.-Blattname für die Buchung des Zahlungseingangs verwendet werden soll.|  
    |**Nur Buch.-Blatt erstellen**|Markieren Sie dieses Kontrollkästchen, wenn Sie den Zahlungseingang nicht buchen wollen, wenn Sie die Schaltfläche **OK** wählen. Der Zahlungseingang wird in dem angegebenen Buch vorbereitet und erst gebucht, wenn jemand die fraglichen Buch.-Blatt-Zeilen bucht.|  

5. Wählen Sie die Schaltfläche **OK** aus.  

## <a name="see-also"></a>Siehe auch  
 [Erfassen von Zahlungen per Lastschriftverfahren SEPA](finance-collect-payments-with-sepa-direct-debit.md)   
 [Verkauf](sales-manage-sales.md)

