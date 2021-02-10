---
title: 'Vorgehensweise: Vorauszahlungen korrigieren | Microsoft Docs'
description: Sie können eine Korrektur an einem Auftrag vornehmen, nachdem Sie eine Vorauszahlungsrechnung für den Auftrag gebucht haben. Sie können einem Auftrag auch nach dem Versand einer Vorauszahlungsrechnung noch weitere Zeilen hinzufügen, und Sie können dann eine weitere Vorauszahlungsrechnung buchen, Sie können jedoch keine Zeile mehr aus einem Auftrag löschen, nachdem für die Zeile eine Vorauszahlung fakturiert wurde.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1be1ba8d59567fdf9ba2adfeceeaa23c9cf63778
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750730"
---
# <a name="correct-prepayments"></a>So korrigieren Sie Vorauszahlungen

Sie können eine Korrektur an einem Auftrag vornehmen, nachdem Sie eine Vorauszahlungsrechnung für den Auftrag gebucht haben. Sie können einem Auftrag auch nach dem Versand einer Vorauszahlungsrechnung noch weitere Zeilen hinzufügen, und Sie können dann eine weitere Vorauszahlungsrechnung buchen, Sie können jedoch keine Zeile mehr aus einem Auftrag löschen, nachdem für die Zeile eine Vorauszahlung fakturiert wurde.  

> [!TIP]
> Wenn Sie eine Vorauszahlungsrechnung für eine Verkaufsrechnung gebucht haben, die Sie dann korrigieren oder stornieren, müssen Sie auch die Vorauszahlung korrigieren oder stornieren.

## <a name="to-correct-a-prepayment"></a>So korrigieren Sie eine Vorauszahlung

Das folgende Verfahren zeigt, wie Sie eine Vorauszahlungsgutschrift ausstellen, um alle fakturierten Vorauszahlungen für einen Auftrag zu stornieren.  

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Verkaufsaufträge** ein und wählen Sie dann den entsprechenden Link.  
2. Öffnen Sie den entsprechenden Verkaufsauftrag.
3. Wählen Sie die Aktion **Vorauszahlung**, und dann die Aktion **Vorauszahlungsgutschrift buchen** oder **Vorauszahlungsgutschrift buchen und drucken**.  
4. Korrigieren Sie auf der Seite **Verkaufsgutschrift** alle relevanten Positionen für alle Verkaufsgutschriften. Weitere Informationen finden Sie unter [Retouren verarbeiten oder Stornieren](sales-how-process-sales-returns-cancellations.md).  

    > [!NOTE]  
    > Um den Betrag im Feld **Positionsbetrag** zu reduzieren, müssen Sie zuerst den Vorauszahlungsprozentsatz in der Zeile erhöhen, damit der Wert im Feld **Vorauszahlungszeilenbetrag** nicht unter den Wert im Feld **Fakt. Vorauszahlungsbetrag** fällt.

5. Um eine Vorauszahlungsrechnung für neuen Zeilen in der Vorauszahlungsgutschrift zu erstellen, wählen Sie die Aktion **Vorauszahlung**, und dann die Aktion **Vorauszahlungsrechnung buchen** oder **Vorauszahlungsrechnung buchen und drucken**.  
6. Um eine zusätzliche Vorauszahlungsrechnung zu erstellen, erhöhen Sie den Vorauszahlungsbetrag in einer oder mehreren Zeilen, und buchen die Vorauszahlungsrechnung. Für die Differenz zwischen dem fakturierten Vorauszahlungsbetrag und den neuen Vorauszahlungsbeträgen wird eine neue Rechnung erstellt.  

## <a name="see-also"></a>Siehe auch

[Fakturieren von Vorauszahlungen](finance-invoice-prepayments.md)  
[Exemplarische Vorgehensweise: Einrichten und Fakturieren von Verkaufsvorauszahlungen](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
