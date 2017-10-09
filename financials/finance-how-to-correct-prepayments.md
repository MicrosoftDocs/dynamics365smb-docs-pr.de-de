---
title: 'Vorgehensweise: Vorauszahlungen korrigieren | Microsoft Docs'
description: "Sie können eine Korrektur an einem Auftrag vornehmen, nachdem Sie eine Vorauszahlungsrechnung für den Auftrag gebucht haben. Sie können einem Auftrag nach der Leistung einer Vorauszahlungsrechnung weitere Zeilen hinzufügen und dann eine weitere Vorauszahlungsrechnung buchen. Sie können jedoch keine Zeile mehr aus einem Auftrag löschen, nachdem für die Zeile eine Vorauszahlung fakturiert wurde."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b51fba1ee8c9a040836ac24c51f39a036f3c0e23
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-correct-prepayments"></a>Vorgehensweise: Vorauszahlungen korrigieren
Sie können eine Korrektur an einem Auftrag vornehmen, nachdem Sie eine Vorauszahlungsrechnung für den Auftrag gebucht haben. Sie können einem Auftrag auch nach dem Versand einer Vorauszahlungsrechnung noch weitere Zeilen hinzufügen, und Sie können dann eine weitere Vorauszahlungsrechnung buchen, Sie können jedoch keine Zeile mehr aus einem Auftrag löschen, nachdem für die Zeile eine Vorauszahlung fakturiert wurde.  

## <a name="to-correct-a-prepayment"></a>So korrigieren Sie eine Vorauszahlung
Das folgende Verfahren zeigt, wie Sie eine Vorauszahlungsgutschrift ausstellen, um alle fakturierten Vorauszahlungen für einen Auftrag zu stornieren.  
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Verkaufsaufträge** ein und wählen dann den zugehörigen Link aus.  
2. Öffnen Sie den entsprechenden Verkaufsauftrag.
3. Wählen Sie die Aktion **Vorauszahlung**, und dann die Aktion **Vorauszahlungsgutschrift buchen** oder **Vorauszahlungsgutschrift buchen und drucken**.  
4. Korrigieren Sie im Fenster **Verkaufsgutschrift** alle relevanten Positionen für alle Verkaufsgutschriften. Weitere Informationen finden Sie unter [Vorgehensweise: Retouren verarbeiten oder Stornieren](sales-how-process-sales-returns-cancellations.md).     

    > [!NOTE]  
    > Um den Betrag im Feld **Positionsbetrag** zu reduzieren, müssen Sie zuerst den Vorauszahlungsprozentsatz in der Zeile erhöhen, damit der Wert im Feld **Vorauszahlungszeilenbetrag** nicht unter den Wert im Feld **Fakt. Vorauszahlungsbetrag** fällt.

5. Um eine Vorauszahlungsrechnung für neuen Zeilen in der Vorauszahlungsgutschrift zu erstellen, wählen Sie die Aktion **Vorauszahlung**, und dann die Aktion **Vorauszahlungsrechnung buchen** oder **Vorauszahlungsrechnung buchen und drucken**.  
6. Um eine zusätzliche Vorauszahlungsrechnung zu erstellen, erhöhen Sie den Vorauszahlungsbetrag in einer oder mehreren Zeilen, und buchen die Vorauszahlungsrechnung. Für die Differenz zwischen dem fakturierten Vorauszahlungsbetrag und den neuen Vorauszahlungsbeträgen wird eine neue Rechnung erstellt.  

## <a name="see-also"></a>Siehe auch  
[Fakturieren von Vorauszahlungen](finance-invoice-prepayments.md)  
[Exemplarische Vorgehensweise: Einrichten und Fakturieren von Verkaufsvorauszahlungen](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

