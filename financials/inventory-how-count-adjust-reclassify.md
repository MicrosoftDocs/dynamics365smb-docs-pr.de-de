---
title: Erfassen, Regulieren und Umbuchen von Lagerbestand| Microsoft Docs
description: "Beschreibt, wie eine physische Zählung ausgeführt wir, negative oder Zugängen gemacht werden und wie Informationen wie Lagerort oder Chargennummer in Artikelposten und Lagerplatzposten geändert werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: adjustment, negative, positive, increase, decrease
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: db79c257585fe89237ef4e8d61fa49ce46ec682f
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-count-adjust-and-reclassify-inventory"></a>Vorgehensweise. Erfassen, Regulieren und Umbuchen von Lagerbestand
Mindestens einmal im Geschäftsjahr muss eine Inventur durchgeführt werden, d. h. alle Artikel im Lager müssen gezählt werden, um festzustellen, ob die in der Datenbank geführten Mengen denen entsprechen, die tatsächlich physisch im Lager vorhanden sind. Ist die tatsächliche physische Menge bekannt, wird diese im Hauptbuch als Teil der Lagerbewertung am Ende eines Zeitraums gebucht.

Obwohl Sie alle Artikel am Lager mindestens einmal im Jahr zählen, haben Sie sich möglicherweise entschieden, manche Artikel häufiger zu zählen, vielleicht, weil sie wertvoller sind oder weil sie häufig umgesetzt werden und einen großen Teil Ihres Umsatzes darstellen. Zu diesem Zweck können Sie spezielle Inventurhäufigkeiten den Artikeln zuweisen. Weitere Informationen finden Sie im Abschnitt "Zyklische Inventur durchführen".

Falls Sie erfasste Lagerbestandsmengen im Zusammenhang mit einer Inventur oder zu anderen Zwecken anpassen müssen, können Sie ein Artikel Buch.-Blatt verwenden, um die Inventurposten direkt ohne Buchen von Geschäftstransaktionen zu ändern. Alternativ können Sie einen einzelnen Artikel der Artikelkarte anpassen.

Wenn Sie Attribute und Mengen im Artikelposten ändern müssen, können Sie das Artikel Umlag. Buch.-Blatt verwenden. Typische Attribute für die Umbuchung sind Serien-/Chargennummern, Ablaufdaten und Dimensionen.

## <a name="to-perform-a-physical-inventory"></a>Eine physische Inventur durchzuführen:
Sie müssen am Ende des Geschäftsjahres – wenn nicht sogar noch häufiger – eine Inventur durchführen (d. h., die tatsächlich verfügbaren Artikel zählen), um zu prüfen, ob die vermerkte Menge dieselbe ist wie die Menge im Lager. Wenn es Differenzen gibt, müssen Sie diese verbuchen, bevor Sie eine Lagerbewertung durchführen können.

Neben der physischen Zählaufgabe umfasst der gesamte Vorgang die folgenden drei Aufgaben:

- Berechnen des erwarteten Lagerbestands.
- Drucken des Berichts, der beim Zählen verwendet werden soll.
- Eingeben und Buchen des tatsächlichen gezählten Lagerbestands.

### <a name="to-calculate-the-expected-inventory"></a>So berechnen Sie den erwarteten Lagerbestand
1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Physische Inventur durchführen** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Lager berechnen** aus.
3. Geben Sie im Fenster **Lagerbestand berechnen** im Inforegister Optionen die Bedingungen an, die zum Erstellen der Buch.-Blattzeilen verwendet werden sollen, wie z. B. ob Artikel mit einem Lagerbestand von null zu berücksichtigen sind.
4. Setzen Sie Filter, wenn Sie nur den Lagerbestand bestimmter Artikel, Lagerplätze, Lagerorte oder Dimensionen berechnen möchten.
5. Wählen Sie die Schaltfläche **OK** aus.

> [!NOTE]  
>   Die Artikelposten werden gemäß den von Ihnen angegebenen Informationen verarbeitet, und im Inventur Buch.-Blatt werden Zeilen erstellt. Beachten Sie, dass das Feld **Inventurmenge** automatisch mit der gleichen Menge wie das Feld **Menge (berechnet)** ausgefüllt wird. Bei dieser Funktion ist es für Sie nicht erforderlich, den gezählten verfügbaren Lagerbestand für Artikel einzugeben, die der berechneten Menge entsprechen. Wenn jedoch die gezählte Menge von der Eingabe im Feld **Menge (Berechnet)** abweicht, müssen Sie diese mit der tatsächlich gezählten Menge überschreiben.

### <a name="to-print-the-report-used-when-counting"></a>So drucken Sie den Bericht, der beim Zählen verwendet wird
1. Im Fenster **Physisches Bestandjournal**, das den berechneten erwarteten Lagerbestand enthält, wählen Sie auf der Registerkarte Aktionen in der Gruppe Allgemein die Option **Drucken** aus.
2. Geben Sie im Fenster **Inventurliste** im Inforegister Optionen an, ob der Bericht die berechnete Mengen ausweisen soll und ob der Bericht Lagerartikel nach Serien-/Chargennummern aufführen soll.
3. Setzen Sie Filter, wenn Sie nur den Bericht für bestimmte Artikel, Lagerplätze, Lagerorte oder Dimensionen berechnen möchten.
4. Wählen Sie die Schaltfläche **Drucken** aus.

Mitarbeiter können nun mit dem Zählen des Lagerbestands fortfahren und alle Abweichungen in dem gedruckten Bericht erfassen.

### <a name="to-enter-and-post-the-actual-counted-inventory"></a>So erfassen und buchen Sie den tatsächlichen gezählten Lagerbestand
1. In jeder Zeile im Fenster **Physischer Lagerbestant**in der der tatsächliche verfügbare Lagerbestand, wie durch die physische Zählung ermittelt, von der berechneten Menge abweicht, geben Sie den tatsächlichen verfügbaren **Lagerbestand** im Feld Inventurmenge ein.

    Die verknüpften Felder werden entsprechend aktualisiert.

    > [!NOTE]  
>   Wenn die Zählung zeigt, dass Differenzen bestehen, die durch Artikel mit fehlerhaften Lagerortcodes verursacht wurden, geben Sie die Differenzen nicht in das Inventurbuch ein. Verwenden Sie stattdessen das Umlagerungs Buch.-Blatt oder einen Umlagerungsauftrag, um die Artikel zu den richtigen Lagerorten umzuleiten. Weitere Informationen finden Sie unter Artikel neu klassieren. So wird's gemacht: Umlagerungsaufträge anlegen.

2. Um die berechneten Mengen an die tatsächlichen gezählten Mengen anzupassen, wählen Sie auf der Registerkarte Aktionen in der Gruppe Buchen die Option **Buchen** aus.

    Sowohl Artikelposten als auch Inventurposten werden erstellt. Öffnen Sie die Artikelkarte, um die resultierenden Inventurposten anzuzeigen.

3. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen")aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.
4. Öffnen Sie die betreffende Artikelkarte, und wählen Sie dann auf der Registerkarte Navigieren in der Gruppe Artikel die Option **Inventurposten** aus.

# <a name="to-perform-cycle-counting"></a>Durchführen zyklischer Inventuren
Obwohl Sie alle Artikel am Lager mindestens einmal im Jahr zählen, haben Sie sich möglicherweise entschieden, manche Artikel häufiger zu zählen, vielleicht, weil sie wertvoller sind oder weil sie häufig umgesetzt werden und einen großen Teil Ihres Umsatzes darstellen. Zu diesem Zweck können Sie spezielle Inventurhäufigkeiten den Artikeln zuweisen.

> [!NOTE]  
>   Wenn Ihr Lagerort die gesteuerte Einlagerung und Kommissionierung nutzt, verwenden Sie zunächst das Fenster **Logistik Inventur Buch.-Blatt** und dann das Fenster **Artikel Buch.-Blatt**, um die Funktion **Ausgleich berechnen** auszuführen.

## <a name="to-set-up-counting-periods"></a>So richten Sie Inventurhäufigkeiten ein:
Eine Inventur wird normalerweise in regelmäßigen Intervallen durchgeführt, z. B. monatlich, vierteljährlich oder jährlich. Sie können die benötigten Inventurhäufigkeiten einrichten.

Sie richten die Inventurhäufigkeiten ein, die Sie verwenden möchten, und ordnen dann allen Lagerhaltungsdaten und/oder Artikeln eine von ihnen zu. Wenn Sie eine Inventur durchführen und **Inventurhäufigkeit berechnen** im Inventur-Buch.-Blatt nutzen, werden Zeilen für die Artikel automatisch erstellt.

1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Physische Inventurperioden** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-a-counting-period-to-an-item"></a>Um einem Artikel oder Lagerhaltungsdaten eine Inventurhäufigkeit zuzuordnen:  
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen")aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie den Artikel aus, dem Sie eine Inventurhäufigkeit zuweisen möchten.  
3. Geben Sie im Feld **Inventurhäufigkeitscode** die passende Inventurhäufigkeit aus.  
4. Wählen Sie die Schaltfläche **Ja** aus, um den Code zu ändern und das erste Inventurdatum für den Artikel zu berechnen. Wenn Sie das nächste Mal die Berechnung einer Inventurhäufigkeit im Logistik Inventur Buch.-Blatt auswählen, erscheint der Artikel als Zeile im Fenster **Inventurartikelauswahl**. Sie können jetzt beginnen, den Artikel in regelmäßigen Abständen zu zählen.

## <a name="to-initiate-a-count-based-on-counting-periods"></a>Eine Grundlage basierend auf den  Inventurhäufigkeiten initiieren
1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Physische Inventur Buchblatt** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Inventurdatum berechnen**.

    Das Fenster **Inventurartikelauswahl** wird geöffnet, das die Artikel enthält, für die Inventurhäufigkeiten eingerichtet wurden, die gezählt werden müssen, entsprechend ihren Inventurhäufigkeiten.
3. Eine physische Inventur durchzuführen. Weitere Informationen finden Sie unter Vorgehensweise: Führen Sie physische Inventuren aus.

## <a name="to-adjust-the-inventory-of-one-item"></a>Um die Lager von einem Artikel zu korrigieren
Nachdem Sie eine Inventur eines Artikels in Ihrem Lagerbereich vorgenommen haben, können Sie die Funktion **Lager regulieren** verwenden, um die Menge des aktuellen Lagerstatus zu erfassen.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen")aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie den Artikel, für den Sie den Lagerbestand anpassen möchten, und wählen Sie dann die Aktion **Lager regulieren** aus.
3. Geben Sie im Feld **Neuer Bestand** die Bestandsmenge ein, die Sie für den Artikel übernehmen möchten.
4. Wählen Sie die Schaltfläche **OK** aus.

Der Bestand des Artikels ist jetzt reguliert. Die neue Menge wird im Feld **Aktueller Lagerbestand** im Fenster **Lager regulieren** und im Feld **Lagerbest.** im Fenster **Artikelkarte** angezeigt.

Sie können auch die Funtion **Bestand anpassen** als einfachen Weg verwenden, gekaufte Artikel in den Lagerbestand aufzunehmen, wenn Sie nicht Einkaufsrechnungen oder Bestellungen verwenden, um Ihre Einkäufe zu erfassen. Weitere Informationen finden Sie unter [So gehts: Erfassen eines Einkaufs](purchasing-how-record-purchases.md).

> [!NOTE]  
>   Nachdem Sie den Lagerbestand angepasst haben, müssen Sie diese mit dem aktuellen, berechneten Wert aktualisiert werden. Weitere Informationen finden Sie unter [So geht's: Bestand anpassen](inventory-how-revalue-inventory.md).

## <a name="to-adjust-the-inventory-quantity-of-one-or-more-items"></a>Um die Reservierung der Lagermenge eines oder mehrerer Artikel korrigieren
Im **Artikel Buch.-Blatt** können Sie Veränderungen des Lagerbestands im Zusammenhang mit Einkäufen, Verkäufen und der Produktion von Stücklisten sowie Zugänge und Abgänge buchen.

Wenn Sie das Artikel Buch.-Blatt häufig zum Buchen der gleichen oder ähnlicher Buch.-Blattzeilen verwenden, z. B. im Zusammenhang mit Materialverbrauch, können Sie das **Standard Artikel Buch.-Blatt** verwenden, um diese wiederkehrenden Arbeiten zu vereinfachen. Weitere Informationen zum Arbeiten mit Fibu Buch.-Blättern, finden Sie unter [Arbeiten mit Fibu Buch.-Blätter](ui-work-general-journals.md)

1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Fibu Buchblatt** ein und wählen den zugehörenden Link aus.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Wählen Sie die **Buchen** Aktion aus, die Lagerregulierungen vorzunehmen.

> [!NOTE]  
>   Nachdem Sie den Lagerbestand angepasst haben, müssen Sie diese mit dem aktuellen, berechneten Wert aktualisiert werden. Weitere Informationen finden Sie unter [So geht's: Bestand anpassen](inventory-how-revalue-inventory.md).

## <a name="to-reclassify-an-items-lot-number"></a>Um die Chargennummer des Artikels neu zu klassieren
1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Artikel Buchblatt neu klassieren** ein und wählen den zugehörenden Link aus.
2. Füllen Sie im Fenster **Umlagerungs Buch.-Blatt** die notwendigen Felder aus.
3. Wählen Sie das Feld **Chargennummer** Feld, geben die Artikelstromchargennummer ein.
4. Wählen Sie das Feld **Neue Chargennummer** Feld, geben die neue Artikelchargennummer ein.
5. Wählen Sie die Aktion **Buchen** aus.

## <a name="see-also"></a>Siehe auch
[Lagerbest](inventory-manage-inventory.md)  
[Verkauf](sales-manage-sales.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

