---
title: 'Gewusst wie: Vorauszahlungsrechnungen erstellen | Microsoft Docs'
description: Erfahren Sie, wie Sie Situationen bearbeiten, in denen Vorauszahlung gefordert wird, oder Ihr Kreditor dies fordert.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 04d7703df0c1b5e4da8996f00b5f1eed293cbf56
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-prepayment-invoices"></a>Vorgehensweise: Erstellen von Vorauszahlungsrechnungen
Wenn Sie von Ihren Kunden erwarten, dass diese vor der Lieferung eines Auftrags eine Vorauszahlung leisten oder wenn der Lieferant von Ihnen eine Vorauszahlung vor Lieferung erwartet, können Sie die Funktion "Vorauszahlung" verwenden.  

Nachdem Sie einen Auftrag oder eine Bestellung angelegt haben, können Sie eine Vorauszahlungsrechnung erstellen. Sie können für Verkaufs- oder Einkaufszeile die Standardprozentsätze verwenden, oder Sie können den Betrag den Anforderungen entsprechend anpassen. So können Sie beispielsweise den Gesamtbetrag für den gesamten Auftrag angeben.  

Im Folgenden wird beschrieben, wie eine Vorauszahlung für einen Auftrag fakturiert wird. Die Schritte sind für eine Bestellung ähnlich.  

## <a name="to-create-a-prepayment-invoice"></a>So erstellen Sie eine Vorauszahlungsrechnung  
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Verkaufsaufträge** ein und wählen dann den zugehörigen Link aus.  
2. Erstellen Sie einen neuen Verkaufsauftrag. Weitere Informationen finden Sie unter [So geht's: Produkte verkaufen](sales-how-sell-products.md)  

    Im Inforegister **Vorauszahlung** wird das Feld **Vorauszahlung %** automatisch ausgefüllt, wenn auf der Debitorenkarte ein standardmäßiger Vorauszahlungsprozentsatz angegeben ist. Sie können den Inhalt des Felds ändern. Der Vorauszahlungsprozentsatz wird aus dem Kopf nur in die Zeilen kopiert, in die nicht der standardmäßige Vorauszahlungsprozentsatz des Artikels kopiert wird.  

    Ein Häkchen im Feld **Vorauszahlung komprimieren** bedeutet, dass die Zeilen auf der Rechnung zusammengefasst werden, wenn folgende Bedingungen zutreffen:  
    - Es wird das gleiche Sachkonto für Vorauszahlungen verwendet, wie unter "Buchungsmatrix Einrichtung" festgelegt.  
    - Es werden die gleichen Dimensionen verwendet.  

    Lassen Sie das Feld leer, wenn Sie eine Vorauszahlungsrechnung angeben möchten, die für jede Auftragszeile mit einem Vorauszahlungsprozentsatz eine Zeile enthält.  

3. Füllen Sie die Verkaufszeilen aus.  

    Wenn für Artikel Vorauszahlungsprozentsätze eingerichtet wurden, wird der Standard automatisch in das Feld  der Zeile **Vorauszahlung %** kopiert. Andernfalls wird der Vorauszahlungsprozentsatz aus dem Kopf kopiert. Sie können den Inhalt des Felds  in der Zeile **Vorauszahlung %** ändern.  
4. Wenn Sie einen Vorauszahlungsprozentsatz für den gesamten Auftrag verwenden möchten, ändern Sie den Wert im Feld **Vorauszahlung** im Auftragskopf, nachdem die Zeilen ausgefüllt wurden.  
5. Um den gesamten Vorauszahlungsbetrag anzuzeigen, wählen Sie die Aktion **Statistik**.

    Wenn Sie den gesamten Vorauszahlungsbetrag für den Auftrag anpassen möchten, können Sie den Inhalt des Feldes **Vorauszahlungsbetrag** im Fenster **Verkaufsauftragsstatistik** ändern.  

    Wenn das Feld **Preise inkl. MwSt** aktiviert ist, kann das Feld **Vorauszahlungsbetrag einschl. MwSt**. geändert werden.  

    Wenn Sie den Inhalt des Felds **Vorauszahlungsbetrag** ändern, wird der Betrag proportional auf alle Zeilen aufgeteilt, mit Ausnahme der Felder, bei denen im Feld **Vorauszahlung** der Wert **0** angegeben ist.  
6. Wählen Sie zum Drucken eines Testberichtes vor der Buchung der Vorauszahlungsrechnung die Aktion **Vorauszahlung** und dann die Aktion **Vorauszahlungstestbericht**.  
7. Wählen Sie zum Buchen der Vorauszahlungsrechnung die Aktion **Vorauszahlung**, und dann die Aktion **Vorauszahlungsrechnung**.  

    Klicken Sie zum Buchen und Drucken der Vorauszahlungsrechnung die Aktion **Vorauszahlungsrechnung buchen und drucken**.  

Es können weitere Vorauszahlungsrechnungen für den Auftrag ausgegeben werden. Erhöhen Sie hierzu den Vorauszahlungsbetrag für eine oder mehrere Zeilen, passen Sie im Bedarfsfall das Belegdatum an, und buchen Sie die Vorauszahlungsrechnung. Für die Differenz zwischen den bisher fakturierten Vorauszahlungsbeträgen und dem neuen Vorauszahlungsbetrag wird eine neue Rechnung erstellt.  

> [!NOTE]  
>  Wenn Sie in Nordamerika sind, können Sie den Prozentsatz nicht ändern, nachdem die Vorauszahlungsrechnung gebucht wurde. Dieses wird in der nordamerikanischen Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] verhindert, da die Berechnung der Verkaufssteuer ansonsten falsch ist.  

 Wenn Sie bereit zum Buchen des verbleibenden Rechnungsbetrags sind, buchen Sie diesen auf die gleiche Weise, wie Sie jede andere Rechnung buchen. Der Vorauszahlungsbetrag wird automatisch vom fälligen Betrag abgezogen.  

## <a name="see-also"></a>Siehe auch  
[Fakturieren von Vorauszahlungen](finance-invoice-prepayments.md)  
[Exemplarische Vorgehensweise: Einrichten und Fakturieren von Verkaufsvorauszahlungen](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

