---
title: 'Erfassen, Regulieren und Umbuchen von Lagerbestand'
description: 'Erfahren Sie, wie Sie physisch zählen und Anpassungen und Neuklassifizierungen vornehmen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/20/2022
ms.custom: bap-template
---
# Erfassen, Regulieren und Umbuchen von Lagerbestand mithilfe von Buch.-Blättern

Führen Sie eine Inventur aller Artikel im Bestand durch, um sicherzustellen, dass Ihre Mengen korrekt sind. Einige Unternehmen führen eine jährliche Inventur durch, andere zählen alle oder nur einige Artikel häufiger. Nachdem Sie die Artikel gezählt haben, verwenden Sie Journale, um die tatsächlichen Mengen in das Hauptbuch zu buchen. Zum Beispiel, wenn Sie den Bestand am Ende einer Periode bewerten.

Um einige Artikel öfter zu zählen als andere, vielleicht wegen ihres Wertes, verwenden Sie Zykluszählungen. Weisen Sie den Artikeln für Zykluszählungen spezielle Inventurhäufigkeiten zu. Weitere Informationen finden Sie unter [Zykluszählung durchführen](inventory-how-count-adjust-reclassify.md#to-do-cycle-counting).

Um Mengen nach einer Inventur oder aus anderen Gründen anzupassen, verwenden Sie eine Artikelerfassung, um die Lagerposten zu ändern, ohne Transaktionen zu buchen. Sie können auch die Menge eines einzelnen Artikels der einer Artikelkarte anpassen.

Um Attribute und Mengen im Artikelposten zu ändern, verwenden Sie ein Artikel Umlag. Buch.-Blatt. Zu den typischen neu zu klassifizierenden Attributen gehören Dimensionen und Verkaufskampagnencodes. Neuklassifizierungserfassungen können auch für Umbuchungen verwendet werden, indem Lagerplatz- und Lagerplatzcodes neu klassifiziert werden. Spezielle Schritte treffen zu, wenn Sie Serien- oder Chargennummern und deren Ablaufdatum umbuchen möchten. Weitere Informationen finden Sie unter [Arbeiten mit Serien- und Chargennummern](inventory-how-work-item-tracking.md).

> [!NOTE]
> In Vorgängen mit mehreren Schritten werden Artikel in Lagerplätzen als Lagerplatzposten, nicht als Artikelposten erfasst. Daher führen Sie die Zählmengen aus und buchen in Logistik Buch.-Blättern, um die Lagerplätze zu unterstützen. Dann synchronisieren Sie die neuen oder geänderten Lagerplatzposten mit den entsprechenden Artikelposten, um die Änderungen in den Lagerbestandsmengen in den Werten zu aktualisieren.

[!INCLUDE [edit-in-excel](includes/edit-in-excel.md)]

## So führen Sie eine Inventur durch

Eine Inventur durchzuführen bedeutet, die tatsächlich verfügbaren Artikel zu zählen, um zu prüfen, ob die vermerkte Menge dieselbe ist wie die Menge im Lager. In der Regel findet die Inventur am Ende eines Geschäftsjahres statt, manchmal jedoch häufiger. Bei Differenzen buchen Sie die tatsächlichen Mengen auf die Artikelkonten, <!--accounts, or ledger?--> bevor Sie die Bestandsbewertung durchführen.

> [!NOTE]
> Dieses Verfahren beschriebt, wie eine Inventur unter Verwendung eines Buch.-Blatts, die Seite **Physisches Bestandjournal** ausgeführt wird. Sie können Dokumente auf den Seiten **Inventurauftrag** und **Inventurerfassung** verwenden. Diese Dokumente bieten mehr Kontrolle und Unterstützung bei der Verteilung der Zählarbeit auf mehrere Mitarbeiter. Weitere Informationen finden Sie unter [Erfassung und Regulierung des Lagerbestand mithilfe von Belegen](inventory-how-count-inventory-with-documents.md).<br /><br />
> Beachten Sie, dass Sie belegbasierte Funktionalität nicht verwenden können, um Artikel in Lagerplätzen oder Lagerplatzposten zu erfassen.

Der Zählprozess beinhaltet auch die folgenden Aufgaben:

- Berechnen des erwarteten Lagerbestands.
- Drucken des Berichts, der beim Zählen verwendet werden soll.
- Eingeben und Buchen der tatsächlichen Mengen.

Führen Sie eine Inventur abhängig von Ihren Lagereinstellungen, auf eine der folgenden Methoden durch. Weitere Informationen finden Sie unter [Lagerortverwaltung einrichten](warehouse-setup-warehouse.md).  

- Wenn Ihr Lagerort keine gerichtete Einlagerung und Kommissionierung verwendet, verwenden Sie die Seite **Phys. Lagererfassung Buch.-Blatt**. Das Verfahren ähnelt der Inventur ohne Zykluszählung.  
- Wenn Ihr Lagerort gerichtete Einlagerung und Kommissionierung verwendet, verwenden Sie die Seite **Logistik Inventur Buch.-Blatt**. Verwenden Sie dann die Seite **Artikel Buch.-Blätter** , um die Aktion **Ausgleich berechnen** auszuführen. <!--We should say what to do on each of these pages.-->

### So berechnen Sie den erwarteten Lagerbestand in den Basislagerkonfigurationen

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Geben Sie **Physische Lagererfassungen Buch.-Blätter** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Lager berechnen** aus.
3. Geben Sie auf der Seite **Lagerbestand berechnen** im Inforegister Optionen die Bedingungen an, die zum Erstellen der Buch.-Blattzeilen verwendet werden sollen, wie z. B. ob Artikel mit einem Lagerbestand von null zu berücksichtigen sind.
4. Setzen Sie Filter, wenn Sie nur den Lagerbestand bestimmter Artikel, Lagerplätze, Lagerorte oder Dimensionen berechnen möchten.
5. Wählen Sie die Schaltfläche **OK**.

> [!NOTE]  
> Artikelposten werden gemäß den von Ihnen angegebenen Informationen verarbeitet, und im Inventur Buch.-Blatt werden Zeilen erstellt. Beachten Sie, dass das Feld **Inventurmenge** die gleiche Menge wie das Feld **Menge (berechnet)** hat. Für Artikel, bei denen diese Werte übereinstimmen, müssen Sie die gezählte Menge nicht eingeben. Wenn die gezählte Menge jedoch abweicht, geben Sie die gezählte Menge ein.

### Drucken des Berichts, der beim Zählen verwendet werden soll

1. Auf der Seite **Inventur Buch.-Blatt**, das den berechneten erwarteten Lagerbestand enthält, wählen Sie auf der Registerkarte Aktionen in der Gruppe Allgemein die Option **Drucken** aus.
2. Geben Sie auf der Seite **Inventurliste Lager** im Inforegister Optionen an, ob der Bericht die berechnete Mengen und Lagerartikel nach Serien- und Chargennummern aufführt.
3. Setzen Sie Filter, wenn Sie nur den Bericht für bestimmte Artikel, Lagerplätze, Lagerorte oder Dimensionen berechnen möchten.
4. Wählen Sie **Drucken** aus.

Lagermitarbeiter können nun den Lagerbestand zählen und alle Unterschiede in dem gedruckten Bericht erfassen.

> [!NOTE]
> Es kann mehrere Tage dauern, bis gedruckte Berichte zur endgültigen Verarbeitung und Veröffentlichung zurückkehren. Wenn Sie den tatsächlichen gezählten Lagerbestand angeben und buchen, passt das System den Lagerbestand an, um die Differenz zwischen dem erwarteten und dem tatsächlich gezählten Lagerbestand widerzuspiegeln. Sie müssen die ursprünglich berechneten Buch.-Blattzeilen beibehalten und den erwarteten Bestand nicht neu berechnen, da sich der erwartete Lagerbestand ändern und zu falschen Lagerebenen führen kann. Wenn Sie mehrere Berichte erstellen müssen, z. B. für verschiedene Standorte oder Artikelgruppen, müssen Sie separate Buch.-Blattnamen erstellen und beibehalten.

### Um den tatsächlichen gezählten Lagerbestands in den Basislagerkonfigurationen einzugeben und zu buchen

1. In jeder Zeile auf der Seite **Inventur Buch.-Blatt** in der der tatsächliche verfügbare Lagerbestand, wie durch die physische Zählung ermittelt, von der berechneten Menge abweicht, geben Sie den tatsächlichen verfügbaren **Lagerbestand** im Feld Inventurmenge ein.
  
  > [!NOTE]  
  > Wenn die Zählung zeigt, dass Differenzen bestehen, die durch Artikel mit fehlerhaften Lagerorten verursacht wurden, geben Sie die Differenzen nicht in das Inventurbuch ein. Verwenden Sie stattdessen ein Umlagerungs Buch.-Blatt oder einen Umlagerungsauftrag, um die Artikel zu den richtigen Lagerorten umzuleiten. 

2. Um die berechneten Mengen an die tatsächlichen gezählten Mengen anzupassen, wählen Sie auf der Registerkarte Aktionen in der Gruppe Buchen die Option **Buchen** aus.

    Die Buchung erstellt Artikelposten als auch Inventurposten. Öffnen Sie die Seite Artikelkarte für den Artikel, um die Inventurposten zu finden. <!--Where are they shown on an item?-->

3. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol einrichten möchten, geben Sie **Artikel** ein und wählen dann den entsprechenden Link.
4. Öffnen Sie die Seite Artikelkarte für den Artikel, und wählen Sie die Aktion **Inventurposten** aus, um die Zahl zu bestätigen <!--I don't see this action -->

### Um den erwarteten Lagerbestand in den erweiterten Basislagerkonfigurationen zu berechnen

Artikelbuch und Lager synchronisieren <!--warehouse what?--> bevor Sue die Inventur durchführen. Andernfalls buchen Sie die Inventurergebnisse kombiniert mit anderen Lagerortanpassungen für die Artikel in die Inventurerfassung und das Artikelbuch. Weitere Informationen finden Sie unter [Mengen in den Artikelposten und im Lager synchronisieren](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Geben Sie **Logistik Inventur Buch.-Blatt** ein und wählen Sie den zugehörigen Link.  
2. Wählen Sie die **Lager berechnen** Aktion aus, um die Seite **Logistik Lagerbestand berech.** zu öffnen.  
3. Legen Sie Filter fest, um die Artikel anzugeben, die im Buch.-Blatt gezählt werden sollen, und wählen Sie **OK**.

   [!INCLUDE [prod_short](includes/prod_short.md)] erzeugt eine Zeile für jeden Lagerplatz, der die Filtervorgaben erfüllt. Sie können Zeilen löschen. Wenn Sie die Ergebnisse aber als Inventur buchen möchten, zählen Sie den Artikel an allen Lagerplätzen, an denen er vorhanden ist.  

   Wenn Sie nur ein Artikel in einigen Lagerplätzen zu zählen, aber nicht an anderen, können Sie Differenzen eingeben und sie später mit der Aktion **Ausgleich berechnen** buchen. <!--I don't see this action-->  

### Um den tatsächlichen gezählten Lagerbestands in den erweiterten Lagerkonfigurationen einzugeben und zu buchen

1. Geben Sie auf der Seite **Logistik Inventur Buch.-Blatt** die tatsächlichen Mengen in das Feld **Inventurmenge** ein.  

    > [!NOTE]  
    >  Das Feld **Menge (Berechnet)** wird basierend auf Lagerplatzdatensätzen ausgefüllt. Diese Menge wird in jeder Zeile in das Feld **Menge (Physisch)** kopiert. Wenn die Mengen in diesen Feldern nicht übereinstimmen, geben Sie die tatsächliche Menge ein.  

2. Nachdem Sie alle tatsächlichen Mengen eingegeben haben, wählen Sie die Aktion **Erfassen**.  

    Wenn Sie das Buch.-Blatt registrieren, erstellt [!INCLUDE [prod_short](includes/prod_short.md)] zwei Lagerplatzposten im Logistikjournal für jede Zeile, die gezählt und registriert wurde:  

    - Wenn die berechneten und die tatsächlichen Mengen nicht übereinstimmen, wird eine negative oder positive Menge für den Lagerplatz registriert und eine Ausgleichsmenge wird auf den Ausgleichslagerplatz des Lagerorts gebucht.  
    - Wenn die berechnete Menge der gezählten entspricht, registriert [!INCLUDE [prod_short](includes/prod_short.md)] **0** für den Lagerplatz und den Ausgleichslagerplatz. 

Wenn Sie den physischen Bestand registrieren, buchen Sie nicht auf den Artikel, den physischen Bestand oder die Wertbücher. Die Aufzeichnungen stehen jedoch bei Bedarf zum Abgleich zur Verfügung. Um die Mengen genau zu halten, buchen Sie die Ergebnisse, nachdem Sie die Artikel in allen Lagerplätzen gezählt haben, als physische Inventur <!--physical inventory journal-->. Weitere Informationen finden Sie unter [Mengen in den Artikelposten und im Lager synchronisieren](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).

## So führen Sie zyklischer Inventuren durch

Sie können Artikel so oft zählen, wie Sie möchten. Zum Beispiel, weil sie wertvoller sind oder weil sie sich schnell bewegen und einen großen Teil Ihres Geschäfts ausmachen. Legen Sie die Zählhäufigkeit fest, indem Sie den Artikeln spezielle Zählzeiträume zuweisen.

Je nach Ihrer Lagereinrichtung können Sie eine Zyklusinventur auf folgende Weise durchführen. Weitere Informationen finden Sie unter [Einrichten von Warehouse Management](warehouse-setup-warehouse.md).  

- Wenn Ihr Lagerort keine gerichtete Einlagerung und Kommissionierungen verwendet, verwenden Sie die Seite **Inventur Buch.-Blatt**. Das Schritte ähnelt der Inventur ohne Zykluszählung.  
- Wenn Ihr Lagerort gerichtete Einlagerung und Kommissionierung verwendet, verwenden Sie die Seite **Logistik Inventur Buch.-Blatt**. Verwenden Sie dann die Seite **Artikel Buch.-Blätter** , um die Aktion **Ausgleich berechnen** auszuführen. <!--we should say what to do on each of these pages-->  

### So richten Sie Inventurhäufigkeiten ein:

Eine Inventur ist normalerweise eine wiederkehrende Aufgabe, z. B. monatlich, vierteljährlich oder jährlich. Sie können die Inventurhäufigkeiten einrichten, die Sie benötigen, und dann jedem Artikel eine davon zuweisen. Danach verwenden Sie die Aktion **Inventurdatum berechnen** auf der Seite **Inventur Buch.-Blatt**, um automatisch Zeilen für die Artikel zu erstellen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Inventurhäufigkeit** ein, und wählen Sie den zugehörigen Link.  
2. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### Um einem Artikel oder Lagerhaltungsdaten eine Inventurhäufigkeit zuzuordnen:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Elemente** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie den Artikel aus, dem Sie eine Inventurhäufigkeit zuweisen möchten.  
3. Geben Sie im Feld **Inventurhäufigkeitscode** die Inventurhäufigkeit aus.  

> [!NOTE]
> Wenn Sie den Zählzeitraum ändern, zeigt eine Meldung Informationen zu den Ergebnissen der Änderung an. Wählen Sie **Ja** aus, um den Code zu ändern und das erste Inventurdatum für den Artikel zu berechnen. Wenn Sie das nächste Mal die Berechnung einer Inventurhäufigkeit im Logistik Inventur Buch.-Blatt auswählen, erscheint der Artikel als Zeile auf der Seite **Inventurartikelauswahl**. Sie können den Artikel dann periodisch zählen.

### Eine Zählung auf Grundlage der Zählperioden in den Basislagerkonfigurationen starten

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Inventur Buch.-Blatt** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Inventurdatum berechnen**.

    Die Seite **Inventurartikelauswahl** zeigt Artikel, die entsprechend ihren Inventurhäufigkeiten gezählt werden müssen.
3. Führen Sie eine Inventur durch. Weitere Informationen finden Sie unter [So führen Sie eine Inventur durch](inventory-how-count-adjust-reclassify.md#to-count-physical-inventory).

### Eine Zählung auf Grundlage der Zählperioden in den erweiterten Lagerkonfigurationen starten

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Geben Sie **Logistik Inventur Buch.-Blatt** ein und wählen Sie den zugehörigen Link.  
2. Wählen Sie die Aktion **Inventurdatum berechnen**.

    Die Seite **Inventurartikelauswahl** zeigt Artikel, die entsprechend ihren Inventurhäufigkeiten gezählt werden müssen.
3. Führen Sie eine Inventur durch. Weitere Informationen finden Sie unter [So führen Sie eine Inventur durch](inventory-how-count-adjust-reclassify.md#to-count-physical-inventory).  

   > [!NOTE]  
   > Zählen Sie den Artikel an allen Lagerplätzen, die ihn enthalten. Wenn Sie Lagerplatzzeilen löschen, die auf der Seite **Lagerplatzumlagerungsbestand** zum Zählen abgerufen wurden, ist die Zählung falsch, wenn Sie sie in eine Inventarerfassung buchen.  

## So passen Sie die Menge eines Artikels an

Nachdem Sie eine Inventur eines Artikels vorgenommen haben, nutzen Sie die Aktion **Lager regulieren**, um die Menge des aktuellen Lagerstatus zu erfassen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Elemente** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Artikel, für den Sie den Lagerbestand anpassen möchten, und wählen Sie dann die Aktion **Lager regulieren** aus.
3. Geben Sie im Feld **Neuer Bestand** für den Lagerort das Ergebnis der Zählung ein.
4. Wählen Sie die Schaltfläche **OK**.

<!-- I don't see a "Quantity on Hand" field on the Item Card page. Should this point to the options for viewing availability?

The item’s inventory is adjusted. The new quantity is shown in the **Quantity on Hand** field on the **Item Card** page.-->

Sie können auch die Aktion **Bestand anpassen** als eine einfache Methode verwenden, gekaufte Artikel dem Bestand hinzuzufügen, wenn Sie keine Einkaufsrechnungen oder Bestellungen verwenden, um Ihre Einkäufe zu erfassen. Erfahren Sie mehr unter [Einkäufe aufzeichnen](purchasing-how-record-purchases.md).

> [!NOTE]  
> Nachdem Sie den Bestand angepasst haben, aktualisieren Sie seinen aktuellen Wert. Weitere Informationen finden Sie unter [Neubewerten von Lagerbestand](inventory-how-revalue-inventory.md).

### So passen Sie die Mengen mehrerer Artikel in den Basislagerkonfigurationen an

Auf der Seite **Artikel Buch.-Blatt** können Sie Artikelbuchungen direkt buchen, um Bestand für Einkäufe, Verkäufe und positive oder negative Änderungen direkt buchen, ohne Dokumente zu buchen.

Wenn Sie das Artikel Buch.-Blatt häufig zum Buchen der gleichen oder ähnlicher Buch.-Blattzeilen verwenden, z. B.für Materialverbrauch, kann die Seite **Standard Artikel Buch.-Blatt** diese wiederkehrenden Arbeiten vereinfachen. Weitere Informationen finden Sie unter [Arbeiten mit Standard-Buchblättern](ui-work-general-journals.md#work-with-standard-journals).

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Element Buch.-Blätter** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Wählen Sie die Aktion **Buchen** aus, um die Mengen anzupassen.

### Die Lagerplatzmengen in erweiterten Lagerkonfigurationen anpassen

Wenn Ihr Standort gezielte Einlagerung und Kommissionierung verwendet, verwenden Sie die Seite **Lagerartikeljournal** , um ungeplante positive und negative Mengenänderungen zu buchen. Zum Beispiel für als fehlend gebuchte Artikel, die unerwartet auftauchen, oder für Verluste durch Bruch.  

Lagerartikeljournale bieten Ihnen mehr Anpassungsebenen, um Ihre Mengen genauer zu machen. Das Lager weiß, wie viele Artikel vorrätig sind und wo sie gelagert werden, aber jede Anpassung wird nicht im Artikelbuch gebucht. Mit der Mengenanpassung erfolgt eine Gut- oder Lastschrift auf den realen Lagerplatz. An einem Ausgleichslagerplatz wird eine Ausgleichsbuchung vorgenommen. Der Anpassungslagerplatz ist ein virtueller Lagerplatz ohne reale Artikel. Sie geben den virtuellen Lagerplatz im Feld **Lagerplatzcode Anpassung** für Anpassungen auf den Seiten **Lagerortkarte** an.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Logistik Artikel Buch.-Blatt** ein und wählen Sie dann den zugehörigen Link.  
2. Tragen Sie die erforderlichen Informationen in den Kopf ein.  
3. Wählen Sie im Feld **Artikelnr.** in der Zeile den Artikel aus.  
4. Geben Sie den Lagerplatz ein, in den Sie die zusätzlichen Artikel einlagern möchten oder in dem Sie festgestellt haben, dass Artikel fehlen.  
5. Geben Sie im Feld **Menge** eine positive Menge ein, wenn Sie zusätzliche Artikel gefunden haben. Wenn Artikel fehlen, geben Sie eine negative Menge ein.  
6. Wählen Sie die Aktion **Registrieren** aus.

## Um die korrigierten Lagerplatzposten mit den entsprechenden Artikelposten zu synchronisieren

Buchen Sie die Anpassungslagerplatzdatensätze im Artikelbuch für die von Ihnen definierten Perioden. Einige Unternehmen buchen tägliche Anpassungen im Artikelbuch, während andere seltener abgleichen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Element Buch.-Blatt** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder jeder Buch.-Blattzeile aus.  
3. Wählen Sie die Aktion **Lagerausgleich berechnen**, und fügen Sie dann Filter auf der Seite **Lagerausgleich berechnen** hinzu. Anpassungen werden nur für die Posten im Ausgleichslagerplatz berechnet, die den Filteranforderungen entsprechen.  
4. Füllen Sie im Inforegister **Optionen** das Feld **Belegnr.** mit einer Nummer, die Sie manuell eingeben. Da für diese Stapelverarbeitung keine Nummernserie eingerichtet wurde, sollten Sie entweder das vom Lager verwendete Nummernschema verwenden oder das Datum, gefolgt von Ihren Initialen eingeben.  
5. Wählen Sie **OK** aus. Die positiven und negativen Anpassungen werden für alle Artikel summiert und im Artikel Buch.-Blatt werden Zeilen erstellt.  
6. Buchen Sie die Buch.-Blattzeilen, um die Mengenabweichungen als Artikelposten zu buchen. Die Bestände an den Lagerplätzen und im Artikelbuch stimmen jetzt überein.  

## Siehe auch

[Erfassung des Lagerbestand mithilfe von Belegen](inventory-how-count-inventory-with-documents.md)  
[Bestand](inventory-manage-inventory.md)  
[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)  
[Verkauf](sales-manage-sales.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
