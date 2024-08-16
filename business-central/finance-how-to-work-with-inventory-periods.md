---
title: Arbeiten mit Bestandsperioden
description: 'Sie können den Zeitrahmen steuern, auf den Mitarbeiter Beitragsänderungen des Lagerbestandes buchen können, indem Sie Lagerbuchungsperioden definieren.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'inventory, periods'
ms.search.form: 5828
ms.date: 07/29/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="work-with-inventory-periods"></a>Arbeiten mit Bestandsperioden

Eine Lagerbuchungsperiode definiert eine Zeitspanne, in der Sie Änderungen des Lagerbestandes buchen können. Eine Lagerbuchungsperiode ist durch das Datum definiert, an dem sie endet (wird auch als Enddatum bezeichnet). Wenn Sie eine Lagerperiode schließen, können Sie vor diesem Enddatum keine erwarteten oder in Rechnung gestellten Lageränderungen buchen. Vor dem Enddatum können Sie keine neuen Werte ins Inventar eintragen. Wenn Sie in der geschlossenen Periode offene Posten haben, also positive Mengen, die noch nicht auf ausgehende Transaktionen angewendet wurden, können Sie diesen Posten auch dann noch ausgehende Mengen hinzufügen, wenn die Periode geschlossen ist.  

In den folgenden Abschnitten werden diese Schritte beschrieben:

* Lagerbuchungsperioden erstellen.  
* Lagerbuchungsperioden schließen.  
* Lagerbuchungsperioden erneut öffnen.  

## <a name="to-create-an-inventory-period"></a>Eine Lagerbuchungsperiode erstellen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Lagerbuchungsperioden** ein und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie eine neue Zeile.  
3. Geben Sie in das Feld **Enddatum** das letzte Datum der Lagerbuchungsperiode ein, die Sie definieren möchten. Wenn die Periode geschlossen ist, können Sie vor diesem Datum keine Bestandsänderungen mehr buchen.  
4. Geben Sie im Feld **Name** einen beschreibenden Namen ein. Wählen Sie die Schaltfläche **OK**.  

## <a name="to-close-inventory-periods"></a>So schließen Sie Lagerbuchungen

Das Feld **Abgeschlossen** gibt an, ob die Lagerbuchungsperiode hinsichtlich Änderungen der Lagerbestandswerte geschlossen ist. Sie können dieses Feld nicht bearbeiten.  

Sie können jede Inventurperiode schließen, wenn Folgendes zutrifft:  

* In dieser Periode gibt es keine offenen ausgehenden Artikelposten (d. h., es gibt keinen negativen Lagerbestand).  
* Die Preise aller Artikel wurden mit dem Batchauftrag **Lagerreg. fakt. Einst. Preise** angepasst.  

Das heißt, dass alle ausgehenden Transaktionsmengen (z. B. von Verkaufsaufträgen, ausgehenden Umlagerungen, Verkaufsrechnungen, Einkaufsreklamationen oder Einkaufsgutschriften) mit der im Lagerbestand vorhandenen Menge ausgeglichen werden müssen.  

### <a name="to-close-an-inventory-period"></a>Eine Lagerbuchungsperiode schließen

1. Bevor Sie eine Bestandsperiode abschließen, wählen Sie die Aktion **Kosten anpassen - Artikelbuchungen**, um sicherzustellen, dass alle Kostenanpassungen gebucht werden.

    Führen Sie den Bericht  **Inventarperiode schließen – Test**  aus, um zu ermitteln, ob innerhalb der Inventurperiode offene ausgehende Artikeleinträge oder Artikel vorhanden sind, deren Kosten noch nicht angepasst wurden.  
2. Wählen Sie die **Bericht testen** Aktion aus.  

    Führen Sie den Batchauftrag **Lagerregulierung buchen** aus, damit sichergestellt ist, dass alle Preise in der Finanzbuchhaltung gebucht werden.  
3. Wählen Sie die Aktion **Lager auf Sachkonten buchen** aus.  
4. Wählen Sie im Fenster **Lagerbuchungsperioden** die Lagerbuchungsperiode aus, die geschlossen werden soll.  
5. Wählen Sie die Aktion **Periode schließen**. Nach Abschluss der Inventurperiode können Sie vor dem Enddatum keine Bestandsänderungen mehr buchen. Die Preise aller Artikel müssen mit der Stapelverarbeitung **Kosten anpassen - Artikelposten** reguliert sein, bevor Sie die Lagerbuchungsperiode schließen.  
6. Wählen Sie die Schaltfläche **Ja**, wenn Sie bestätigen möchten, dass die Periode geschlossen werden soll, oder wählen Sie die Schaltfläche **Nein**, wenn Sie das Schließen abbrechen möchten.  
7. Der Inventurzeitraum wird geschlossen und nach Abschluss wird eine Bestätigungsmeldung angezeigt.  

## <a name="reopening-inventory-periods"></a>Wiedereröffnung von Inventurperioden
Nachdem Sie die Inventurperiode geschlossen haben, können Sie sie nicht mehr löschen. Sie können sie aber erneut öffnen, wenn Sie Buchungen vor dem Enddatum der Lagerbuchungsperiode zulassen möchten. Ein erneutes Öffnen einer Periode bewirkt, dass auch jede Lagerbuchungsperiode geöffnet wird, deren Enddatum hinter dem Enddatum der Periode liegt, die Sie erneut öffnen.  

### <a name="to-reopen-an-inventory-period"></a>So öffnen Sie eine Lagerbuchungsperiode erneut
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Lagerbuchungsperioden** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Lagerbuchungsperiode aus, die erneut geöffnet werden soll.  
3. Wählen Sie die Aktion **Periode erneut öffnen**. Bestätigen Sie, dass Sie die Periode erneut öffnen möchten.  
4. Alle Lagerbuchungsperioden, deren Enddatum nach der von Ihnen ausgewählten Periode liegt, werden erneut geöffnet.  

## <a name="see-also"></a>Siehe auch
[Designdetails: Lagerperioden](design-details-inventory-periods.md)    
[Finanzen](finance.md)    
[Lagerbest](inventory-manage-inventory.md)    
[Arbeiten mit Financials](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
