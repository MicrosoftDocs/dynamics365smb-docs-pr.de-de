---
title: Erfassen, Regulieren und Umbuchen von Lagerbestand| Microsoft Docs
description: Beschreibt, wie eine physische Zählung ausgeführt wir, negative oder Zugängen gemacht werden und wie Informationen wie Lagerort oder Chargennummer in Artikelposten und Lagerplatzposten geändert werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: adjustment, negative, positive, increase, decrease
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8909e4428aa97190ea6ccb5b83997657f29ea96f
ms.sourcegitcommit: fe6943d410f5dca4e8b2986f95501009ae982d98
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "4827093"
---
# <a name="count-adjust-and-reclassify-inventory-using-journals"></a>Erfassen, Regulieren und Umbuchen von Lagerbestand mithilfe von Buch.-Blättern
Mindestens einmal im Geschäftsjahr muss eine Inventur durchgeführt werden, d. h. alle Artikel im Lager müssen gezählt werden, um festzustellen, ob die in der Datenbank geführten Mengen denen entsprechen, die tatsächlich physisch im Lager vorhanden sind. Ist die tatsächliche physische Menge bekannt, wird diese im Hauptbuch als Teil der Lagerbewertung am Ende eines Zeitraums gebucht.

Obwohl Sie alle Artikel am Lager mindestens einmal im Jahr zählen, haben Sie sich möglicherweise entschieden, manche Artikel häufiger zu zählen, vielleicht, weil sie wertvoller sind oder weil sie häufig umgesetzt werden und einen großen Teil Ihres Umsatzes darstellen. Zu diesem Zweck können Sie spezielle Inventurhäufigkeiten den Artikeln zuweisen. Weitere Informationen finden Sie unter [Durchführen zyklischer Inventuren](inventory-how-count-adjust-reclassify.md#to-perform-cycle-counting).

Falls Sie erfasste Lagerbestandsmengen im Zusammenhang mit einer Inventur oder zu anderen Zwecken anpassen müssen, können Sie ein Artikel Buch.-Blatt verwenden, um die Inventurposten direkt ohne Buchen von Geschäftstransaktionen zu ändern. Alternativ können Sie einen einzelnen Artikel der Artikelkarte anpassen.

Wenn Sie Attribute und Mengen im Artikelposten ändern müssen, können Sie das Artikel Umlag. Buch.-Blatt verwenden. Typische Attribute zur Reklassifizierung umfassen Dimensionen und Verkaufskampagnecodes. Sie führen aber auch "Systemübertragungen" durch, indem Lagerplatz und Lagerortcodes umgebucht werden. Spezielle Schritte treffen zu, wenn Sie Serien- oder Chargennummern und deren Ablaufdatum umbuchen möchten. Weitere Informationen finden Sie unter [Arbeiten mit Serien- und Chargennummern](inventory-how-work-item-tracking.md).

> [!NOTE]
> In erweiterten Lagerkonfigurationen werden Artikel in Lagerplätzen als Lagerplatzposten, nicht als Artikelposten erfasst. Daher führen Sie die Zählmengen aus und buchen in bestimmten Logistik Buch.-Blättern, um die Lagerplätze zu unterstützen. Dann verwenden Sie spezielle Funktionen, um die neuen oder geänderten Lagerplatzposten mit den entsprechenden Artikelposten zu synchronisieren, um die Änderungen in den Lagerbestandsmengen in den Werten zu aktualisieren. Dies wird in einem spezifischen Verfahren unten beschrieben, wo dies relevant ist.

## <a name="to-perform-a-physical-inventory"></a>Eine physische Inventur durchzuführen:
Sie müssen am Ende des Geschäftsjahres – wenn nicht sogar noch häufiger – eine Inventur durchführen (d. h., die tatsächlich verfügbaren Artikel zählen), um zu prüfen, ob die vermerkte Menge dieselbe ist wie die Menge im Lager. Wenn es Differenzen gibt, müssen Sie diese verbuchen, bevor Sie eine Lagerbewertung durchführen können.

> [!NOTE]
> Dieses Verfahren beschriebt, wie eine Inventur unter Verwendung eines Buch.-Blatts, die Seite **Physisches Bestandjournal** ausgeführt wird. Sie können diese Aufgabe auch mithilfe von Belegen, den Seiten **Inventurauftrag** und **Inventurerfassung** durchführen, die mehr Kontrolle bieten und die Verteilung der Erfassung auf mehrere Mitarbeiter unterstützen. Weitere Informationen finden Sie unter [Inventurerfassung mithilfe von Belegen](inventory-how-count-inventory-with-documents.md).<br /><br />
> Beachten Sie, dass belegbasierte Funktionalität nicht verwendet werden kann, um Artikel in Lagerplätzen, Lagerplatzposten zu erfassen.

Neben der physischen Zählaufgabe umfasst der gesamte Vorgang die folgenden drei Aufgaben:

- Berechnen des erwarteten Lagerbestands.
- Drucken des Berichts, der beim Zählen verwendet werden soll.
- Eingeben und Buchen des tatsächlichen gezählten Lagerbestands.

Sie können eine physische Inventur, abhängig von Ihren Lagereinstellungen, nach einer der folgenden Methoden durchführen. Weitere Informationen finden Sie unter [Lagerortverwaltung einrichten](warehouse-setup-warehouse.md).  

-   Wenn Ihr Lagerort keine gesteuerte Einlagerung und Kommissionierung nutzt, verwenden Sie das **Inventur Buch.-Blatt** im Menü **Lager** und das Vorgehen ist fast dasselbe, als wenn Sie eine Inventur ohne zyklische Zählung durchführen.  
-   Wenn Ihr Lagerort die gesteuerte Einlagerung und Kommissionierung nutzt (erweiterte Lagerortkonfiguration) verwenden Sie zunächst das Fenster **Logistik Inventur Buch.-Blatt** und dann das Fenster **Artikel Buch.-Blatt**, um die Funktion **Ausgleich berechnen** auszuführen.

### <a name="to-calculate-the-expected-inventory-in-basic-warehouse-configurations"></a>Um den erwarteten Lagerbestand in den Basislagerkonfigurationen zu berechnen
1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Physisches Bestandjournale** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Lager berechnen** aus.
3. Geben Sie auf der Seite **Lagerbestand berechnen** im Inforegister Optionen die Bedingungen an, die zum Erstellen der Buch.-Blattzeilen verwendet werden sollen, wie z. B. ob Artikel mit einem Lagerbestand von null zu berücksichtigen sind.
4. Setzen Sie Filter, wenn Sie nur den Lagerbestand bestimmter Artikel, Lagerplätze, Lagerorte oder Dimensionen berechnen möchten.
5. Wählen Sie die Schaltfläche **OK** aus.

> [!NOTE]  
>   Die Artikelposten werden gemäß den von Ihnen angegebenen Informationen verarbeitet, und im Inventur Buch.-Blatt werden Zeilen erstellt. Beachten Sie, dass das Feld **Inventurmenge** automatisch mit der gleichen Menge wie das Feld **Menge (berechnet)** ausgefüllt wird. Bei dieser Funktion ist es für Sie nicht erforderlich, den gezählten verfügbaren Lagerbestand für Artikel einzugeben, die der berechneten Menge entsprechen. Wenn jedoch die gezählte Menge von der Eingabe im Feld **Menge (Berechnet)** abweicht, müssen Sie diese mit der tatsächlich gezählten Menge überschreiben.

### <a name="to-print-the-report-to-be-used-when-counting"></a>Drucken des Berichts, der beim Zählen verwendet werden soll
1. Auf der Seite **Physisches Bestandjournal**, das den berechneten erwarteten Lagerbestand enthält, wählen Sie auf der Registerkarte Aktionen in der Gruppe Allgemein die Option **Drucken** aus.
2. Geben Sie auf der Seite **Inventurliste** im Inforegister Optionen an, ob der Bericht die berechnete Mengen ausweisen soll und ob der Bericht Lagerartikel nach Serien-/Chargennummern aufführen soll.
3. Setzen Sie Filter, wenn Sie nur den Bericht für bestimmte Artikel, Lagerplätze, Lagerorte oder Dimensionen berechnen möchten.
4. Wählen Sie die Schaltfläche **Drucken** aus.

Mitarbeiter können nun mit dem Zählen des Lagerbestands fortfahren und alle Abweichungen in dem gedruckten Bericht erfassen.

> [!NOTE]
> Es kann mehrere Tage dauern, bis gedruckte Berichte zur endgültigen Verarbeitung und Veröffentlichung zurückkehren. Wenn Sie den tatsächlichen gezählten Lagerbestand angeben und buchen, passt das System den Lagerbestand an, um die Differenz zwischen dem erwarteten und dem tatsächlich gezählten Lagerbestand widerzuspiegeln. Sie müssen die ursprünglich berechneten Buch.-Blattzeilen beibehalten und den erwarteten Bestand nicht neu berechnen, da sich der erwartete Lagerbestand ändern und zu falschen Lagerebenen führen kann. Wenn Sie mehrere Berichte erstellen müssen, z. B. für verschiedene Standorte oder Artikelgruppen, müssen Sie separate Buch.-Blattnamen erstellen und beibehalten.

### <a name="to-enter-and-post-the-actual-counted-inventory-in-basic-warehouse-configurations"></a>Um den tatsächlichen gezählten Lagerbestands in den Basislagerkonfigurationen einzugeben und zu buchen
1. In jeder Zeile auf der Seite **Physischer Lagerbestant** in der der tatsächliche verfügbare Lagerbestand, wie durch die physische Zählung ermittelt, von der berechneten Menge abweicht, geben Sie den tatsächlichen verfügbaren **Lagerbestand** im Feld Inventurmenge ein.

    Die verknüpften Felder werden entsprechend aktualisiert.

    > [!NOTE]  
    >   Wenn die Zählung zeigt, dass Differenzen bestehen, die durch Artikel mit fehlerhaften Lagerortcodes verursacht wurden, geben Sie die Differenzen nicht in das Inventurbuch ein. Verwenden Sie stattdessen das Umlagerungs Buch.-Blatt oder einen Umlagerungsauftrag, um die Artikel zu den richtigen Lagerorten umzuleiten. Weitere Informationen finden Sie unter Umlagerung Buch.-Blatt oder Umlagerungsaufträge erstellen.

2. Um die berechneten Mengen an die tatsächlichen gezählten Mengen anzupassen, wählen Sie auf der Registerkarte Aktionen in der Gruppe Buchen die Option **Buchen** aus.

    Sowohl Artikelposten als auch Inventurposten werden erstellt. Öffnen Sie die Artikelkarte, um die resultierenden Inventurposten anzuzeigen.

3. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Artikel** ein, und wählen Sie dann den entsprechenden Link.
4. Öffnen Sie die betreffende Artikelkarte, und wählen Sie dann auf der Registerkarte Navigieren in der Gruppe Artikel die Option **Inventurposten** aus.

### <a name="to-calculate-the-expected-inventory-in-advanced-warehouse-configurations"></a>Um den erwarteten Lagerbestand in den erweiterten Basislagerkonfigurationen zu berechnen
Synchronisieren Artikelposten und Lager, bevor Sie die Inventur für das Lager ausführen. Wenn Sie dies nicht tun, werden die Ergebnisse, die Sie im zweiten Teil des Prozesses im Inventur-Buch.-Blatt und als Artikelposten buchen, die mit anderen Logistikanpassungen der gezählten Artikel kombinierten Inventurergebnisse sein. Weitere Informationen finden Sie unter [Mengen in den Artikelposten und im Lager synchronisieren](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries)

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), und geben Sie **Logistik Inventur Buch.-Blatt** ein, und wählen Sie den entsprechenden Link.  
2. Wählen Sie die Aktion **Lager berechnen** aus. Die Batchauftrags-Anforderungfsseite **Logistik Lagerbestand berech.** wird geöffnet.  
3. Legen Sie Filter fest, um die Artikel zu begrenzen, die im Buch.-Blatt gezählt werden sollen, und wählen Sie die Schaltfläche **OK**.

    Die Anwendung erstellt für jeden Lagerplatz, der die Filtervorgaben erfüllt, eine Zeile. Sie können zu diesem Zeitpunkt noch einige der Zeilen löschen. Wenn Sie die Ergebnisse aber als Inventur buchen möchten, müssen Sie den Artikel an allen Lagerplätzen zählen, an denen er vorhanden ist.  

     Wenn Sie nur Zeit haben, den Artikel in einigen Lagerplätzen zu zählen und in anderen nicht, können Sie Differenzen feststellen, diese registrieren und sie später mit der Funktion **Ausgleich berechnen** berechnen.  


### <a name="to-print-the-report-to-be-used-when-counting"></a>Drucken des Berichts, der beim Zählen verwendet werden soll
1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Lagerinventurliste** ein und wählen Sie dann den entsprechenden Link.  
2. Öffnen Sie die Berichtsanforderungsseite und drucken Sie die Listen, in denen Mitarbeiter die Menge an Artikeln erfassen können, die an jedem Lagerplatz gezählt wird.  

Mitarbeiter können nun mit dem Zählen des Lagerbestands fortfahren und alle Abweichungen in dem gedruckten Bericht erfassen.

### <a name="to-enter-and-post-the-actual-counted-inventory-in-advanced-warehouse-configurations"></a>Um den tatsächlichen gezählten Lagerbestands in den erweiterten Lagerkonfigurationen einzugeben und zu buchen
1. Wenn die Zählung abgeschlossen ist, geben Sie die gezählten Mengen in das Feld **Inventurmenge** des Logistik Inventur Buch.-Blattes ein.  

    > [!NOTE]  
    >  Im Logistik Inventur Buch.-Blatt wird automatisch das Feld **Menge (berechnet)** auf der Basis der Lagerplatzposten ausgefüllt, und diese Mengen werden in das Feld **Inventurmenge** jeder Zeile kopiert. Wenn die vom Lagermitarbeiter gezählte Menge von der Menge abweicht, die die Anwendung in das Feld "Inventurmenge" eingetragen hat, müssen Sie die tatsächlich gezählte Menge eintragen.  

2. Eenn Sie alle gezählten Mengen eingegeben haben wählen Sie die Aktion **Erfassen**.  

    Wenn Sie das Buch.-Blatt registrieren, erstellt die Anwendung zwei Lagerplatzposten im Logistikjournal für jede Zeile, die gezählt und registriert wurde:  

    -   Wenn die berechneten und die gezählten Mengen nicht übereinstimmen, wird eine negative oder positive Menge für den Lagerplatz registriert und eine Ausgleichsmenge wird auf den Ausgleichslagerplatz des Lagerorts gebucht.  
    -   Wenn die berechnete Menge mit der gezählten übereinstimmt, registriert die Anwendung einen Posten der Menge 0 und zwar sowohl für den Lagerplatz als auch für den Ausgleichslagerplatz. Diese Posten zeigen an, dass am Registrierungsdatum eine Logistik Inventur durchgeführt wurde und es keine Differenzen in den Lagerbeständen des Artikels gab.  

Wenn Sie die Logistik Inventur registrieren, erzeugen Sie keine Artikelposten, Inventurposten oder Wertposten, die Datensätze stehen jedoch jederzeit für eine Abstimmung zur Verfügung. Wenn Sie jedoch ganz genau nachvollziehen möchten, was im Lager passiert, und Sie alle Lagerplätze gezählt haben, in denen die Artikel registriert waren, sollten Sie die Logistikergebnisse sofort als Inventur im Modul "Lager" buchen. Weitere Informationen finden Sie unter [Mengen in den Artikelposten und im Lager synchronisieren](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).


## <a name="to-perform-cycle-counting"></a>Durchführen zyklischer Inventuren
Obwohl Sie alle Artikel am Lager mindestens einmal im Jahr zählen, haben Sie sich möglicherweise entschieden, manche Artikel häufiger zu zählen, vielleicht, weil sie wertvoller sind oder weil sie häufig umgesetzt werden und einen großen Teil Ihres Umsatzes darstellen. Zu diesem Zweck können Sie spezielle Inventurhäufigkeiten den Artikeln zuweisen.

Sie können eine zyklische Inventur, abhängig von Ihren Lagereinstellungen, nach einer der folgenden Methoden durchführen. Weitere Informationen finden Sie unter [Lagerortverwaltung einrichten](warehouse-setup-warehouse.md).  

-   Wenn Ihr Lagerort keine gesteuerte Einlagerung und Kommissionierung nutzt, verwenden Sie das **Inventur Buch.-Blatt** im Menü **Lager** und das Vorgehen ist fast dasselbe, als wenn Sie eine Inventur ohne zyklische Zählung durchführen.  
-   Wenn Ihr Lagerort die gesteuerte Einlagerung und Kommissionierung nutzt (erweiterte Lagerortkonfiguration) verwenden Sie zunächst das Fenster **Logistik Inventur Buch.-Blatt** und dann das Fenster **Artikel Buch.-Blatt**, um die Funktion **Ausgleich berechnen** auszuführen.  

### <a name="to-set-up-counting-periods"></a>So richten Sie Inventurhäufigkeiten ein:
Eine Inventur wird normalerweise in regelmäßigen Intervallen durchgeführt, z. B. monatlich, vierteljährlich oder jährlich. Sie können die benötigten Inventurhäufigkeiten einrichten.

Sie richten die Inventurhäufigkeiten ein, die Sie verwenden möchten, und ordnen dann allen Lagerhaltungsdaten und/oder Artikeln eine von ihnen zu. Wenn Sie eine Inventur durchführen und **Inventurhäufigkeit berechnen** im Inventur-Buch.-Blatt nutzen, werden Zeilen für die Artikel automatisch erstellt.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Physische Inventurperioden** ein, und wählen Sie dann den entsprechenden Link.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-assign-a-counting-period-to-an-item"></a>Um einem Artikel oder Lagerhaltungsdaten eine Inventurhäufigkeit zuzuordnen:  
1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Artikel** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie den Artikel aus, dem Sie eine Inventurhäufigkeit zuweisen möchten.  
3. Geben Sie im Feld **Inventurhäufigkeitscode** die passende Inventurhäufigkeit aus.  
4. Wählen Sie die Schaltfläche **Ja** aus, um den Code zu ändern und das erste Inventurdatum für den Artikel zu berechnen. Wenn Sie das nächste Mal die Berechnung einer Inventurhäufigkeit im Logistik Inventur Buch.-Blatt auswählen, erscheint der Artikel als Zeile auf der Seite **Inventurartikelauswahl**. Sie können jetzt beginnen, den Artikel in regelmäßigen Abständen zu zählen.

### <a name="to-initiate-a-count-based-on-counting-periods-in-basic-warehouse-configurations"></a>Eine Zählung auf Grundlage der Zählperioden in den Basislagerkonfigurationen initiieren
1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Physisches Bestandjournal** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Inventurdatum berechnen**.

    Die Seite **Inventurartikelauswahl** wird geöffnet, das die Artikel enthält, für die Inventurhäufigkeiten eingerichtet wurden, die gezählt werden müssen, entsprechend ihren Inventurhäufigkeiten.
3. Eine physische Inventur durchzuführen. Weitere Informationen finden Sie unter [Eine physische Inventur durchzuführen](inventory-how-count-adjust-reclassify.md#to-perform-a-physical-inventory).

### <a name="to-initiate-a-count-based-on-counting-periods-in-advanced-warehouse-configurations"></a>Eine Zählung auf Grundlage der Zählperioden in den erweiterten Lagerkonfigurationen initiieren
1.  Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), und geben Sie **Logistik Inventur Buch.-Blatt** ein, und wählen Sie den entsprechenden Link.  
2. Wählen Sie die Aktion **Inventurdatum berechnen**.

    Die Seite **Inventurartikelauswahl** wird geöffnet, das die Artikel enthält, für die Inventurhäufigkeiten eingerichtet wurden, die gezählt werden müssen, entsprechend ihren Inventurhäufigkeiten.
3. Eine physische Inventur durchzuführen. Weitere Informationen finden Sie unter [Eine physische Inventur durchzuführen](inventory-how-count-adjust-reclassify.md#to-perform-a-physical-inventory).  

    > [!NOTE]  
    >  Sie müssen den Artikel an allen Lagerplätzen zählen, die ihn enthalten. Wenn Sie einige der Lagerplatzzeilen löschen, die die Anwendung für die Zählung auf der Seite **Lagerplatzumlagerungsbestand** abgerufen hat, werden Sie nicht alle Artikel im Lager zählen. Wenn Sie solche unvollständigen Ergebnisse später im Fenster "Inventur Buch.-Blatt" buchen, sind die gebuchten Zahlen falsch.  

## <a name="to-adjust-the-inventory-of-one-item"></a>Um die Lager von einem Artikel zu korrigieren
Nachdem Sie eine Inventur eines Artikels in Ihrem Lagerbereich vorgenommen haben, können Sie die Funktion **Lager regulieren** verwenden, um die Menge des aktuellen Lagerstatus zu erfassen.

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Artikel** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Artikel, für den Sie den Lagerbestand anpassen möchten, und wählen Sie dann die Aktion **Lager regulieren** aus.
3. Geben Sie im Feld **Neuer Bestand** die Bestandsmenge ein, die Sie für den Artikel übernehmen möchten.
4. Wählen Sie die Schaltfläche **OK** aus.

Der Bestand des Artikels ist jetzt reguliert. Die neue Menge wird im Feld **Vorhandene Menge** auf der Seite **Artikelkarte** angezeigt.

Sie können auch die Funtion **Bestand anpassen** als einfachen Weg verwenden, gekaufte Artikel in den Lagerbestand aufzunehmen, wenn Sie nicht Einkaufsrechnungen oder Bestellungen verwenden, um Ihre Einkäufe zu erfassen. Weitere Informationen finden Sie unter [Erfassen eines Einkaufs](purchasing-how-record-purchases.md).

> [!NOTE]  
>   Nachdem Sie den Lagerbestand angepasst haben, müssen Sie diese mit dem aktuellen, berechneten Wert aktualisiert werden. Weitere Informationen finden Sie unter [Neubewerten von Lagerbestand](inventory-how-revalue-inventory.md).

### <a name="to-adjust-the-inventory-quantity-of-multiple-items-in-basic-warehouse-configurations"></a>Die Reservierung der Lagermenge mehrerer Artikel in den Basislagerkonfigurationen anpassen
Im **Artikel Buch.-Blatt** können Sie Veränderungen des Lagerbestands im Zusammenhang mit Einkäufen, Verkäufen und der Produktion von Stücklisten sowie Zugänge und Abgänge buchen.

Wenn Sie das Artikel Buch.-Blatt häufig zum Buchen der gleichen oder ähnlicher Buch.-Blattzeilen verwenden, z. B. im Zusammenhang mit Materialverbrauch, können Sie das **Standard Artikel Buch.-Blatt** verwenden, um diese wiederkehrenden Arbeiten zu vereinfachen. Weitere Informationen finden Sie unter [Arbeiten mit Standard-Buchblättern](ui-work-general-journals.md#working-with-standard-journals)

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Artikel Buch.-Blätter** ein und wählen Sie dann den entsprechenden Link.
2. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Wählen Sie die **Buchen** Aktion aus, die Lagerregulierungen vorzunehmen.

### <a name="to-adjust-bin-quantities-in-advanced-warehouse-configurations"></a>Die Lagerplatzmengen in erweiterten Lagerkonfigurationen anpassen  
Wenn Ihr Lagerort die gesteuerte Einlagerung und Kommissionierung nutzt, verwenden Sie **Logistik Artikel Buch.-Blatt** zum Buchen aller Zugänge und Abgänge außerhalb des Kontexts des physischen Inventars, von denen Sie wissen, dass sie wirkliche Gewinne (z. B. Artikel, die vorher als verloren gebucht wurden und die dann unerwartet wieder auftauchen) oder wirkliche Verluste (z. B. beschädigte Artikel) darstellen.  

Im Unterschied zum Buchen der Anpassungen im Artikel Buch.-Blatt bietet die Verwendung des Logistik Artikel Buch.-Blatts eine zusätzliche Anpassungsebene, die Ihre erfassten Mengen zu jeder Zeit noch genauer macht. Die Logistik hat daher immer eine vollständige Aufstellung darüber, wie viele Artikel verfügbar sind und wo diese gelagert sind. Es wird jedoch nicht jeder registrierte Ausgleich sofort als Artikelposten gebucht. Während des Registrierungsprozesses werden die positiven oder negativen Mengenanpassungen für den tatsächlichen Lagerplatz erzeugt, und ein Gegenposten wird im Ausgleichslagerplatz erzeugt, einem virtuellen Lagerplatz ohne richtige Artikel. Dieser Lagerplatz wird in **Lagerplatzcode Anpassung** auf der Lagerortkarte festgelegt.

1.  Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), und geben Sie **Logistik Artikel Buch.-Blatt** ein, und wählen Sie dann den entsprechenden Link.  
2.  Tragen Sie die erforderlichen Informationen in den Kopf ein.  
3.  Füllen Sie das Feld **Artikelnr.** in der Zeile aus.  
4.  Geben Sie den Lagerplatz ein, in den Sie die zusätzlichen Artikel einlagern möchten oder in dem Sie festgestellt haben, dass Artikel fehlen.  
5.  Geben Sie die Menge, die Sie als Differenz festgestellt haben, in das Feld **Menge** ein. Wenn Sie zusätzliche Artikel gefunden haben, geben Sie eine positive Menge ein. Wenn Artikel fehlen, geben Sie eine negative Menge ein.  
6.  Wählen Sie die Aktion **Registrieren** aus.

## <a name="to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries"></a>Um die korrigierten Lagerplatzposten mit den entsprechenden Artikelposten zu synchronisieren
Sie müssen in geeigneten Intervallen, die von der Firmenpolitik bestimmt werden, die Datensätze in den Ausgleichslagerplätzen in Artikelposten buchen. Einige Unternehmen möchten die Anpassungen jeden Tag ins Lager buchen, wohingegen es anderen ausreicht, dies weniger häufig vorzunehmen.

1.  Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Positions-Buch-Blatt** ein und wählen Sie dann den entsprechenden Link.  
2.  Füllen Sie die Felder jeder Buch.-Blattzeile aus.  
3.  Wählen Sie auf der Registerkarte Aktionen in der Gruppe Funktion die Option **Ausgleich berechnen** aus, und geben Sie im Anforderungsfenster für den Batchauftrag die gewünschten Filter ein. Die Änderungen werden nur für die Posten im Ausgleichslagerplatz berechnet, die den Filteranforderungen entsprechen.  
4.  Füllen Sie im Inforegister **Optionen** das Feld **Belegnr.** mit einer Nummer, die Sie manuell eingeben. Da für diese Stapelverarbeitung keine Nummernserie eingerichtet wurde, sollten Sie entweder das vom Lager verwendete Nummernschema verwenden oder das Datum, gefolgt von Ihren Initialen eingeben.  
5.  Wählen Sie die Schaltfläche **OK** aus. Die positiven und negativen Anpassungen werden für alle Artikel summiert und im Artikel Buch.-Blatt werden für alle Artikel Zeilen erstellt, deren Summe eine positive oder negative Menge ist.  
6.  Buchen Sie die Buch.-Blattzeilen, um die Mengenabweichungen als Artikelposten zu buchen. Der Lagerbestand in den Lagerplätzen entspricht jetzt genau dem Lagerbestand in den Artikelposten.  

## <a name="to-reclassify-an-items-lot-number"></a>Um die Chargennummer des Artikels neu zu klassieren
Wenn Sie Attribute und Mengen im Artikelposten ändern müssen, können Sie das Artikel Umlag. Buch.-Blatt verwenden. Typische Attribute zur Reklassifizierung umfassen Dimensionen und Verkaufskampagnecodes. Sie führen aber auch "Systemübertragungen" durch, indem Lagerplatz und Lagerortcodes umgebucht werden.

Spezielle Schritte treffen zu, wenn Sie Serien- oder Chargennummern und deren Ablaufdatum umbuchen möchten. Weitere Informationen finden Sie unter [Arbeiten mit Serien- und Chargennummern](inventory-how-work-item-tracking.md).

Das folgende Beispiel basiert auf einen Lagerortcode. Die Schritte sind für andere Arten von Artikelattribute gleich.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), und geben Sie **Umlagerung Buch.-Blatt** ein und wählen Sie dann den entsprechenden Link.
2. Füllen Sie auf der Seite **Umlagerungs Buch.-Blatt** die notwendigen Felder aus.
3. Geben Sie im **Lagerortcode** Feld den aktuellen Lagerortcode des Artikels ein.
4. Geben Sie im **Neuer Lagerortcode** Feld den neuen Lagerortcode des Artikels ein.
5. Wählen Sie die Aktion **Buchen** aus.

Weitere Informationen zum Übertragen von Artikeln mit Kontrolle der gelieferten und eingegangenen Mengen, siehe [Übertragen Sie Lagerbestand zwischen Lagerorten](inventory-how-transfer-between-locations.md).

## <a name="see-also"></a>Siehe auch
[Erfassung des Lagerbestand mithilfe von Belegen](inventory-how-count-inventory-with-documents.md)  
[Bestands](inventory-manage-inventory.md)
[Lagerortverwaltung](warehouse-manage-warehouse.md)    
[Verkauf](sales-manage-sales.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
