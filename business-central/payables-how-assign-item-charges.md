---
title: Artikelzu-/abschläge zu Verkäufen und Käufen zuordnen (enthält Video)
description: 'Weisen Sie Artikelgebühren zu, wenn Sie Lagerartikel benötigen, um zusätzliche Kosten wie Fracht und physische Handhabung zu tragen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'transportation, added cost, landed cost'
ms.search.form: '5709, 5800, 5805, 5814'
ms.date: 06/22/2021
ms.author: bholtorf
---
# <a name="use-item-charges-to-account-for-additional-trade-costs"></a>Verwenden von Artikelzuschlägen für zusätzliche Kosten

Um eine korrekte Bewertung sicherzustellen, müssen Ihre Lagerartikel Kosten wie Fracht, Versicherung, Umlagerung und Transport enthalten, die beim Kauf oder Verkauf entstehen. Die Kosten eines eingekauften Artikels bestehen aus dem Einkaufspreis des Kreditors und allen zusätzlichen Artikelzuschlägen, die einzelnen Wareneingängen oder Rücklieferungen zugewiesen werden können. Die Frachtkosten der verkauften Artikel zu kennen, kann für Ihr Unternehmen genauso wichtig sein wie die Einkaufspreise der eingekauften Artikel zu kennen.

Zusätzlich zum Aufzeichnen der hinzugefügten Kosten zu Ihrem Lagerwert, können Sie die Funktion Artikelzuschlag wie folgt verwenden:

* Die Identifizierung der Gesamtkosten eines Artikels, um bessere Entscheidungen bezüglich der Optimierung des Vertriebsnetzes zu treffen.
* Die Analyse der Zusammensetzung eines Verkaufspreises/Einstandspreises eines Artikels.
* Lassen Sie Kaufzuschläge in die Kalkulation der Einheit und Verkaufszuschläge in den Einheitspreis einfließen.

Bevor Sie Artikelzuschläge zuweisen können, müssen Sie Artikelzuschlagsnummern für die verschiedenen Arten von Artikelzuschlägen einrichten. Die Zahlen beinhalten, auf welche Sachkonten Kosten im Zusammenhang mit Verkäufen, Einkäufen und Bestandsanpassungen gebucht werden sollen. Eine Artikelzuschlagsnummer enthält eine Kombination von Produktbuchungsgruppe, Steuergruppencode, MwSt.-Produktbuchungsgruppe und Artikelzuschlag. Wenn Sie die Artikelbelastungsnummer auf einem Einkaufs- oder Verkaufsbeleg eingeben, wird das Sachkonto abgerufen. Das abgerufene Konto wird basierend auf der Einrichtung der Artikelbelastungsnummer und den Informationen auf dem Dokument ausgewählt.

Für Bestellungen und Verkaufsbelege können Artikelzuschläge auf zwei Arten zugeordnet werden:

* Auf dem Beleg, auf dem der Artikel aufgeführt ist, auf den sich der Artikelzuschlag bezieht. Dies ist in der Regel für Belege der Fall, die noch nicht vollständig gebucht sind.
* Auf einer getrennten Rechnung, indem Sie den Artikelzuschhlag mit einem gebuchten Beleg oder einer Lieferung verknüpfen, in denen der Artikel vorkommt, zu dem der Artikelzuschlag gehört.

> [!NOTE]  
> Sie können Artikelzuschläge in Bestellungen, Rechnungen und Gutschriften für Verkaufs- und Einkaufsberichte zuweisen. Die folgenden Verfahren beschreiben, wie man mit Artikelzuschlägen für eine Einkaufsrechnung arbeitet. Die Schritte sind für alle anderen Einkaufs- und Verkaufsbelege ähnlich.

## <a name="example"></a>Beispiel

In diesem Video wird gezeigt, wie Sie im Rahmen der Lagerkostenberechnung mit zusätzlichen Lieferkosten umgehen.
<br><br>  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4b0SB?rel=0]

## <a name="to-set-up-item-charge-numbers"></a>Vorgehensweise: Eine Artikelzu-/-abschlagsnummer einrichten

Sie können die Artikel Zu-/Abschlagsnummern verwenden, um die verschiedenen Arten von Artikel Zu-/Abschlägen, die in Ihrem Unternehmen verwendet werden, zu verwalten.

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Artikel Zu-/Abschläge** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie auf der Seite **Artikel-Gebühren** die Aktion **Neu** aus, um eine neue Zeile für eine zu erstellen.
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-an-item-charge-directly-to-the-purchase-invoice-for-the-item"></a>Um einen Artikel Zu-/Abschlag in die Einkaufsrechnung für den Artikel zuordnen

Wenn Sie den Artikel-Zu-/Abschlag kennen, und den Zeitpunkt, der eine Einkaufsrechnung für den Artikel betrifft, gehen Sie folgendermaßen vor.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Einkaufsrechnungen** ein, und wählen Sie dann den zugehörigen Link.
2. Eine neue Einkaufsrechnung erstellen. Weitere Informationen finden Sie unter [Erfassen eines Einkaufs](purchasing-how-record-purchases.md).
3. Stellen Sie sicher, dass die Einkaufsrechnung eine oder mehrere Zeilen vom Artikeltyp hat.
4. Geben Sie eine neue Zeile ein, und wählen Sie **Zu-/Abschlag (Artikel)** im Feld **Art**.
5. Geben Sie in dem Feld **Menge** die Anzahl der Einheiten dieses Artikel Zu-/Abschlages ein, für die Sie eine Rechnung erhalten haben.
6. Geben Sie in dem Feld **EK-Preis** den Betrag der Artikelgebühr an.
7. Füllen Sie die verbleibenden Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Folgen sie diesen Schritten, um die aktuelle Zuordnung vorzunehmen. Bis die Artikelgebühr vollständig zugewiesen wird, wird der Wert im Feld **Menge zuordnen** in roter Schrift angezeigt..
8. Klicken Sie auf dem Inforegister **Zeilen** auf Aktionen **Artikelgebühr-Zuweisung**.

    Die Seite **Artikel Zu-/Abschlagszuweisung** öffnet sich und zeigt eine Zeile für jede Zeile der Art in der Einkaufsrechnung. Um den Artikel Zu-/Abschlag in einen oder mehreren Verkaufsrechnungszeilen zuzuweisen, können Sie eine Funktion verwenden die es für Sie zugewiesen und verteilt oder Sie das **Menge. zuordnen** Feld manuell ausfüllen können. Die folgenden Schritte beschreiben, wie Vorschlagungs-ArtikelZu-/Abschlags-Zuweisungsfunktion verwendet.

9. Auf der Seite **Artikel Zu-/Abschlagszuweisung** wählen Sie die **Artikel Zu-/Abschlagszuweisung vorschlagen** Aktion aus.
10. Wenn es mehr Rechnungszeilen als eine Art des Artikels gibt, wählen Sie eine der vier Verteilungsoptionen aus.  

Bis die Artikelgebühr vollständig zugewiesen wird, wird der Wert im Feld **Menge zuordnen** in roter Schrift angezeigt..

Der Artikelzuschlag wird nun der Einkaufsrechnung zugeordnet. Wenn Sie den Wareneingang der Einkaufsrechnung buchen, werden die Lagerwerte der Artikel mit den Kosten für Artikelzu-/-abschläge aktualisiert.  

## <a name="to-assign-an-item-charge-from-a-separate-invoice-to-the-purchase-invoice-for-the-item"></a>Um einen Artikel Zu-/Abschlag in die Einkaufsrechnung für den Artikel zuordnen

Wenn Sie eine Rechnung für die Zu-/Abschläge erhalten, nachdem Sie den Wareneingang der ursprünglichen Einkaufsrechnung wurde, gehen Sie folgendermaßen vor.

1. Wiederholen Sie die Schritte 1 bis 8 unter [Um einen Artikel Zu-/Abschlag in die Einkaufsrechnung für den Artikel zuordnen](payables-how-assign-item-charges.md#to-assign-an-item-charge-directly-to-the-purchase-invoice-for-the-item).
2. Klicken Sie auf der Seite **Artikel Zu-/Abschlagszuweisung** auf die Aktion **Rücksendungszeilen holen**.
3. Auf der Seite **Einkauf Lieferzeilen** wählen Sie die Zeile Geb. Einkaufslieferung für den Artikel, dem Sie den Artikel Zu-/Abschlag zuordnen möchten, und wählen Sie dann die Schaltfläche **OK** aus.
4. Wählen Sie die **Artikel Zu-/Abschlagszuweisung vorschlagen** Aktion aus.

Artikelzu-/Abschläge der separaten Einkaufsrechnung wird jetzt dem Artikel in der gebuchten Einkaufslieferung zugeordnet, d aktualisiert der Lagerwert des Artikels mit den Kosten für Artikelzu-/-abschläge.

## <a name="handle-item-charges-for-partial-receipts"></a>Behandeln Sie Artikelgebühren für Teilquittungen

Sehen wir uns ein Beispiel an, wie Artikelgebühren für einen Teilbeleg gehandhabt werden.

Sie haben eine Bestellung mit drei Zeilen:

* Zwei Zeilen sind für Artikel.
* Eine Zeile erfasst Artikelgebühren, die den Artikeln nach Betrag zugeordnet sind.

Wenn die Artikel geliefert werden, stellen Sie fest, dass einer der Artikel fehlt, sodass Sie diese Zeile nicht als erhalten markieren können. Sie können die Einkaufsrechnung nur für den zweiten Artikel empfangen und buchen und sich später um den fehlenden Artikel kümmern.

Um die Artikelkosten für den Teilzugang zu bearbeiten, geben Sie auf der **Artikelbelastungszuordnung**-Seite **0** im Feld **Zu handhabende Menge** in der Zeile für das fehlende Element ein. Kopieren Sie dann den Wert aus dem Feld **zu handhabendenArtikelgebühr Menge** ind das Feld **Rechnungsmenge** in den Bestellpositionen.

Wenn Sie bereit sind, das fehlende Element zu handhaben, aktualisieren Sie das Feld **Zu handhabende Menge** und buchen Sie die Bestellung.

## <a name="see-also"></a>Siehe auch

[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Einkäufe erfassen](purchasing-how-record-purchases.md)  
[Verkäufe fakturieren](sales-how-invoice-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
