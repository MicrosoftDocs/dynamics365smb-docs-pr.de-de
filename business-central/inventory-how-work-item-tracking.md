---
title: 'Verfolgen Sie Artikel mit Serien-, Chargen‑ und Paketnummern'
description: 'Sie können Serien‑, Chargen‑ und Paketnummern zu beliebigen ausgehenden oder eingehenden Belegen hinzufügen, und die gebuchte Artikelverfolgung wird in den entsprechenden Buchungsposten angezeigt.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.forms: '6503, 6515, 6513, 6512, 6502, 6506, 6501, 6510, 6507, 6500, 6505, 6508, 9126, 6526, 6516, 6511, 6504, 6509, 163, 6550,'
ms.date: 03/13/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="track-items-with-serial-lot-and-package-numbers"></a>Artikel mit Serien-, Chargen- und Paketnummern verfolgen

Sie können Serien‑, Chargen‑ und Paketnummern zu beliebigen ausgehenden oder eingehenden Belegen zuordnen, und die gebuchte Artikelverfolgung wird in den entsprechenden Buchungsposten angezeigt. Sie verfolgen Artikel auf der Seite **Artikelverfolgungszeilen** aus, die Sie über eingehende und ausgehende Belege öffnen können.

Die Mengenfelder im Kopf der Seite **Artikelnachverfolgungszeile** zeigt dynamisch die Mengen und die Summen der Artikelverfolgungsnummern an, die Sie auf den Zeilen des Fensters eingegeben werden. Die Mengen müssen denen in den Belegzeilen entsprechen, was durch eine 0 in den Feldern **Undefiniert** angezeigt wird.

[!INCLUDE [prod_short](includes/prod_short.md)] aktualisiert die Verfügbarkeitsinformationen auf der Seite **Artikelverfolgungszeilen**, wenn Sie die Seite öffnen. Die Informationen werden nicht aktualisiert, während Sie die Seite geöffnet haben, und zwar auch dann nicht, wenn in dieser Zeit Änderungen am Lagerbestand oder an anderen Belegen vorgenommen werden.

> [!NOTE]  
> Damit die in diesem Artikel beschriebenen Features funktionieren, müssen Sie zuerst die Artikelverfolgung einrichten. Weitere Informationen finden Sie unter [Artikelverfolgung mit Serien-, Chargen- und Paketnummern einrichten](inventory-how-setup-item-tracking.md).

## <a name="item-tracking-availability"></a>Verfügbarkeit der Artikelverfolgung

Wenn Sie mit Chargen‑, Serien‑ und Paketnummern arbeiten, berechnet [!INCLUDE[prod_short](includes/prod_short.md)] die Verfügbarkeitsinformationen und zeigt sie in den verschiedenen Artikelverfolgungsseiten an. Es wird angezeigt, welche Chargen-, Paket‑ oder Seriennummer auf anderen Belegen verwendet wird. Diese Informationen helfen, Fehler und Unsicherheiten aufgrund von Doppelzuordnungen zu verringern.

Auf der Seite **Artikelverfolgungszeilen** wird in den Feldern **Verfügbarkeit, Chargennr.** oder **Verfügbarkeit, Seriennr.** eventuell aus folgenden Gründen ein Warnsymbol angezeigt:

* Wenn ein Teil oder die gesamte von Ihnen ausgewählte Menge bereits in anderen Belegen verwendet wird.
* Wenn die Chargen- oder Seriennummer nicht verfügbar ist.

Die Seiten **Chargennr./Seriennr.-Informationsliste**, **Chargennr./Seriennr. Verfügbarkeit** und **Artikelverfolgung – Posten auswählen** enthalten Informationen über die verwendete Menge eines Artikels. In der folgenden Tabelle sind die relevanten Felder aufgeführt.

|Feld|Description|
|-----|-----------|  
|**Gesamtmenge**|Die Gesamtmenge eines Artikels, die momentan im Lagerbestand vorhanden ist.|
|**Total angeforderte Menge**|Die Gesamtanzahl des Artikels, die zur Verwendung auf diesem Beleg sowie auf anderen Belegen angefordert ist.|
|**Aktuell ausstehende Menge**|Die Anzahl der angeforderten Artikel, die auf dem aktuellen Beleg angefordert, aber nicht gebucht ist.|
|**Aktuell angeforderte Menge**|Die Anzahl der angeforderten Artikel, die auf dem aktuellen Beleg verwendet wird|
|**Total verfügbare Menge**|Die Gesamtanzahl des Artikels im Lagerbestand minus der Menge des Artikels, die zur Verwendung auf diesem sowie auf anderen Belegen angefordert ist (Total angeforderte Menge) und minus der Menge, die für diesen Beleg angefordert ist, aber noch nicht für den Beleg gebucht wurde (Aktuell angeforderte Menge).|

Wenn Sie längere Zeit auf der Seite **Artikelverfolgungszeilen** arbeiten und wenn es viele Aktivitäten für den Artikel gibt, mit dem Sie arbeiten, können Sie die Verfügbarkeitsinformationen durch Auswahl der Aktion **Verfügbarkeit aktualisieren** aktualisieren. Wenn Sie die Seite schließen, wird die Verfügbarkeit des Artikels also automatisch neu überprüft, um zu bestätigen, dass es keine Verfügbarkeitsprobleme gibt.

## <a name="to-assign-serial-or-lot-numbers-during-an-inbound-transaction"></a>Serien- oder Chargennummern während einer eingehenden Transaktion zuzuordnen:

Vielleicht möchten Sie Artikel sofort ab dem Eingang verfolgen. In diesem Fall ist häufig die Bestellung der entscheidende Beleg. Sie können die Artikelverfolgung jedoch von jedem eingehenden Beleg vornehmen, und die gebuchten Posten werden in den entsprechenden Artikelposten angezeigt.

Die Verfolgungsnummern werden automatisch auf alle ausgehenden Lageraktivitäten übertragen.

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Einkaufsbestellungen** ein, und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie entweder eine vorhandene Bestellung, oder erstellen Sie eine neue.
3. Wählen Sie die Belegzeile und im Inforegister **Zeilen** die Aktion **Zeile** und anschließend die Aktion **Artikelverfolgungszeilen** aus, um die Seite **Bearbeiten – Artikelverfolgungszeilen** zu öffnen.  

   Zum Zuweisen von Serien- oder Chargennummern gibt es folgende Möglichkeiten:  
   * Automatisch, indem Sie **Verarbeiten** und dann **Seriennr. zuweisen** oder **Chargennr. zuweisen** wählen, damit Serien-/Chargennummern aus vordefinierten Nummernserien zugeordnet werden.  
   * Automatisch, indem Sie **Verarbeiten** und dann **Benutzerdef. Seriennr. erstellen** auswählen, damit Serien-/Chargennummern basierend auf Nummernserien zugeordnet werden, die Sie speziell für die angekommenen Artikel festlegen.  
   * Manuell, indem Sie Serien- oder Chargennummern direkt eingeben, z. B. die Nummern des Kreditors.  
   * Manuell, indem Sie jeder Artikeleinheit eine bestimmte Nummer zuweisen.  

4. Um automatisch zuzuweisen, wählen Sie die **Benutzerdef. Seriennr. erstellen** Aktion.  
5. Im Feld **Benutzerdef. Seriennr.** geben Sie die Startnummer einer Nummernserie für Seriennummern ein. Zum Beispiel **S/N-Vend0001**.  
6. Im Feld **Erhöhung** geben Sie "1" ein, um festzulegen, dass jede folgende Nummer um 1 höher sein soll als die vorige.  

    Das Feld **Menge zu erstellen** enthält standardmäßig die Menge aus der Zeile, Sie können diese Menge jedoch ändern.  

7. Wählen Sie das Kontrollkästchen **Neue Chargennr. erstellen** aus, um der neuen Seriennummern eine eigene Chargennummer zuzuteilen.  
8. Wählen Sie die Schaltfläche **OK**.  

[!INCLUDE [prod_short](includes/prod_short.md)] erstellt eine Chargennummer mit einzelnen Seriennummern gemäß der Artikelmenge in der Belegzeile. Der Nummer wird der Wert vorangestellt, den Sie im Feld **Benutzerdef. Seriennr.** eingegeben haben. Zum Beispiel beginnend mit **S/N-Vend0001**.  

Die Mengenfelder im Kopf auf der Seite zeigt dynamisch die Mengen und die Summen der Artikelverfolgungsnummern an, die Sie auf der Seite einrichten. Die Mengen müssen denen in den Belegzeilen entsprechen, was durch eine **0** im Feld **Undefiniert** angezeigt wird.  

Wenn die Belegzeile gebucht wird, werden die Artikelverfolgungposten auf die Artikelposten übertragen.

### <a name="to-handle-serial-and-lot-numbers-when-getting-receipt-lines-from-a-purchase-invoice"></a>So verwenden Sie Serien- und Chargennummern beim Abrufen von Einkaufslieferzielen aus einer Einkaufsrechnung

Wenn Sie gebuchte Einkaufslieferzeilen oder Lieferzeilen aus den zugehörigen Rechnungen oder Gutschriften abrufen, werden alle Artikelverfolgungszeilen in den Logistikbelegen automatisch übertragen. Sie werden jedoch auf besondere Weise verarbeitet.

Die Funktionen unterstützen die folgenden eingehenden Prozesse:  

* **Wareneingangszeilen holen** – von einer Einkaufsrechnung aus.  
* **Rücklieferzeilen holen** – von einer Einkaufsgutschrift aus.  

Die Funktionen unterstützen die folgenden ausgehenden Prozesse:  

* **Lieferzeilen holen** – von einer Verkaufsrechnung oder einem kombinierten Versand aus.  
* **Rücksendungszeilen holen** – von einer Verkaufsgutschrift aus.  

In diesen Fällen werden die Artikelverfolgungszeilen an die Rechnung oder Gutschrift übertragen, die Seite **Artikelverfolgungszeilen** lässt allerdings keine Änderung der Serien- oder Chargennummer zu. Sie können nur die Menge ändern.  

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Einkaufsrechnungen** ein, und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie eine Einkaufsrechnung für Artikel, die mit Serien- oder Chargennummern eingekauft werden.  
3. Wählen Sie in der Einkaufsrechnungszeile im Inforegister **Zeilen** die Option Funktion aus, und wählen Sie dann **Wareneingangszeilen holen** aus.  
4. Wählen Sie auf der Seite **Wareneingangszeile holen** eine Wareneingangszeile aus, die Artikelverfolgungszeilen hat, und klicken Sie anschließend auf **OK**.  

    Der Herkunftsbeleg wird in die Bestellrechnung als neue Zeile kopiert und dessen Artikelverfolgungszeilen werden in das darunter liegende Fenster **Artikelverfolgungszeilen** kopiert.  

5. Wählen Sie auf der Einkaufsrechnung die übertragene Wareneingangszeile aus.  
6. Wählen Sie im Inforegister **Zeilen** **Zeile** und dann **Artikelverfolgungszeile**, um die übertragenen Artikelverfolgungszeilen aufzurufen.  

Sie können die Felder **Seriennr.** und **Chargennr.** nicht ändern. Sie können allerdings ganze Zeilen löschen oder die Mengen verändern, um Änderungen in der Herkunftszeile auszugleichen.  

## <a name="to-assign-a-serial-or-lot-number-during-an-outbound-transaction"></a>Serien- oder Chargennummern bei ausgehenden Vorgängen zuordnen

Die Verarbeitung von ausgehenden Serien- oder Chargennummern ist eine häufige Aktivität, die in vielen verschiedenen Lagerprozessen verwendet wird. Es gibt zwei Möglichkeiten, um ausgehenden Transaktionen Serien- und Chargennummern hinzuzufügen:  

- Treffen Sie Ihre Auswahl aus bestehenden Serien- oder Chargennummern. Dies trifft zu, wenn Artikelverfolgungsnummern bereits bei einem eingehenden Vorgang zugeordnet werden.
- Ordnen Sie neue Serien- oder Chargennummern bei ausgehenden Vorgängen zu. Dies trifft zu, wenn Artikelverfolgungsnummern Artikeln erst zugewiesen werden, wenn diese verkauft und lieferbereit sind.

### <a name="to-select-from-existing-serial-or-lot-numbers"></a>Aus bestehenden Serien- oder Chargennummern auswählen

Wenn Sie mit Artikeln arbeiten, für die Artikelverfolgung erforderlich ist, und Sie ausgehende Transaktionen erstellen, müssen Sie üblicherweise die Chargen- oder Seriennummern von Artikeln verwenden, die es bereits existieren.

1. Wählen Sie in einem beliebigen ausgehenden Beleg die Zeile aus, für die Sie Serien- oder Chargennummern auswählen möchten.  
2. Wählen Sie im Inforegister **Zeilen** die Aktion **Zeile**, dann **Zugehörige Informationen** und anschließend die Option **Artikelverfolgungszeilen** aus.  
3. Auf der Seite **Artikelverfolgungszeilen** gibt es drei Möglichkeiten zum Angeben der Chargen- oder Seriennummer:  

   * Wählen Sie das Feld **Seriennr.** und dann eine Nummer auf der Seite **Seriennummernliste** aus.
   * Wählen Sie das Feld **Chargennr.** und dann eine Nummer auf der Seite **Chargennummernliste** aus. Wählen Sie dann das Feld **Seriennr.** und eine Nummer auf der Seite **Seriennummernliste** aus.
   * Wählen Sie die Aktion **Verarbeiten** und dann **Einträge auswählen** aus. Auf der Seite **Einträge auswählen** werden alle Chargen- und Seriennummern sowie die Verfügbarkeitsinformationen angezeigt.

4. Geben Sie in das Feld **Ausgewählte Menge** für jede Chargen- oder Seriennummer die Menge ein.
5. Wählen Sie die Schaltfläche **OK**. Die Artikelverfolgungsinformationen werden auf die Seite **Artikelverfolgungszeilen** übertragen.  

Die Mengenfelder im Kopf auf der Seite zeigt dynamisch die Mengen und die Summen der Artikelverfolgungsnummern an, die Sie auf der Seite einrichten. Die Mengen müssen denen in der Belegzeile entsprechen, was durch eine **0** im Feld **Undefiniert** angezeigt wird.  

Wenn die Belegzeile gebucht wird, werden die Artikelverfolgungsinformationen auf die zugehörigen Artikelposten übertragen.

### <a name="to-assign-new-serial-or-lot-numbers"></a>So weisen Sie neue Chargen- oder Seriennummern zu

Dieser Prozess wird angewendet, wenn Artikel keine Serien- oder Chargennummern haben, während sie sich im Lagerbestand befinden. Stattdessen weisen Sie die Artikelverfolgungsnummern Artikeln zu, wenn diese verkauft und lieferbereit sind. In diesem Fall weisen Sie die Nummern in der Regel über eine vordefinierte Nummernserie zu.

1. Wählen Sie das entsprechende Dokument, zum Beispiel eine Verkaufsrechnung oder einen Verkaufsauftrag, und im Inforegister **Zeilen** die Aktion **Zeile**, dann **Zugehörige Informationen** und anschließend die Aktion **Artikelverfolgungszeilen** aus.  

    Sie können auf folgende Arten Artikelverfolgungsnummern zuordnen:  
    * Automatisch aus einer vordefinierten Nummernserie: Wählen Sie die Aktion **Seriennr. zuweisen** oder **Chargennr. zuweisen** aus.  
    * Automatisch auf Basis von Parametern, die Sie speziell für den ausgehenden Artikel definieren: Klicken Sie auf der Registerkarte Aktionen in der Gruppe Funktionen auf Benutzerdef. **Seriennr. erstellen**.  
    * Manuell, indem Sie Serien- oder Chargennummern ohne Verwendung von Nummernserien eingeben.  

2. Für diesen Vorgang weisen Sie eine Seriennummer automatisch zu, indem Sie **Seriennr. zuweisen** auswählen.  

    Das Feld **Menge zu erstellen** enthält standardmäßig die Menge aus der Zeile. Sie können diese Menge jedoch ändern.  
3. Wählen Sie das Feld **Neue Chargennr. erstellen**, um der neuen Seriennummern eine eigene Chargennummer zuzuteilen.  
4. Wählen Sie die Schaltfläche **OK**, um eine Chargennummer und neue individuelle Seriennummern entsprechend der Menge in der Belegzeile zu erzeugen.  

Die Mengenfelder im Kopf des Fensters zeigt dynamisch die Mengen und die Summen der Artikelverfolgungsnummern an, die Sie auf der Seite einrichten. Die Mengen müssen denen in der Belegzeile entsprechen, was durch eine **0** im Feld **Undefiniert** angezeigt wird.  

Wenn die Belegzeile gebucht wird, werden die Artikelverfolgungposten auf die Artikelposten übertragen.

### <a name="assign-tracking-numbers-on-source-documents"></a>Verfolgungsnummern in Quelldokumenten zuweisen

Einige Unternehmen legen bestimmte Serien- oder Chargennummern in Herkunftsbelegen fest, z. B. Verkaufsaufträge. Zum Beispiel, wenn Kundschaft eine bestimmte Charge anfordert. Wenn Sie Lagerkommissionierungs- oder Kommissionierungsbelege aus einem ausgehenden Herkunftsbeleg erstellen, in dem bereits Artikelverfolgungsnummern definiert sind, können Sie keine Felder auf der Seite **Artikelverfolgungszeile** unter der Lagerkommissionierung ändern. Die einzige Ausnahme ist das Feld **Bewegungsmge.** Die Lagerkommissionierzeilen legen die Artikelverfolgungsnummern der individuellen Zeilen für Lagerentnahme/Einlagerung fest. Die Menge wurde bereits in einzelne Serien- oder Chargennummer-Kombinationen aufgeteilt, da der Verkaufsauftrag die zu liefernden Artikelverfolgungsnummern enthalten hat.

## <a name="to-handle-serial-and-lot-numbers-on-transfer-orders"></a>Um Serien-/Chargennummern in Umlagerungsaufträgen zu verarbeiten:

Die Vorgehensweise zur Verarbeitung von Serien- und Chargennummern, die zwischen Lagerorten umgelagert werden, ist ähnlich der beim Einkauf und Verkauf von Artikeln.  

Die Umlagerungsaufträge sind allerdings insofern etwas Besonderes, als der Warenausgang und -eingang von derselben Umlagerungszeile aus erfolgen und sie daher die gleiche Instanz der Seite **Artikelverfolgungszeilen** verwenden. Artikelverfolgungsnummern, die von dem einen Lagerort aus geliefert werden, müssen unverändert an dem anderen Ort ankommen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Umlagerungsaufträge** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie den Umlagerungsauftrag, die Sie bearbeiten möchten. Wählen Sie im Inforegister **Zeilen** die Aktion **Zeile**, die Aktion **Artikelverfolgungszeilen** und dann die Aktion **Lieferung** aus.  
3. Auf der Seite **Artikelverfolgungszeilen** weisen Sie eine Serien-/Chargennummer zu oder wählen eine aus, wie für jede andere ausgehende Artikeltransaktion.  

    Wenn Sie Serien-/Chargennummern für Umlagerungsartikel verarbeiten, sind normalerweise bereits Nummern zugeordnet. Daher wählen Sie häufig aus vorhandenen Serien- oder Chargennummern aus.  

4. Buchen Sie den Umlagerungsauftrag (zuerst Warenausgang und dann Wareneingang), um festzuhalten, dass die Artikel mit ihren jeweiligen Artikelverfolgungsposten umgelagert werden.  

Während der Umlagerung können Sie die Werte auf der Seite **Artikelverfolgungszeilen** nicht ändern.  

## <a name="to-record-additional-serial-or-lot-number-information"></a>So zeichnen Sie zusätzliche Serien- oder Chargennummerinformationen auf

Falls Sie spezielle Informationen mit einer Artikelverfolgungsnummer verknüpfen müssen, z. B. für die Qualitätssicherung, können Sie dies in einer Serien- oder Chargennummer-Informationskarte vornehmen.

1. Öffnen eines Belegs, der die Serien- oder Chargennummern ist, die zugeordnet werden.
2. Öffnen Sie die Seite **Artikelverfolgungszeilen** Seite für den Artikel, für den Sie Informationen eingeben möchten.
3. Wählen Sie die Aktion **Zeile** und dann zum Beispiel die Aktion **Seriennr.-Informationskarte** aus.  
4. Wählen das Pluszeichen **(+)** oben in der Liste aus, um einen neuen Eintrag zu erstellen. Die Felder **Seriennr.** und **Chargennr.** werden aus der Artikelverfolgungszeile vorab ausgefüllt.
5. Geben Sie im Feld **Beschreibung** eine kurze Beschreibung ein, zum Beispiel über den Zustand des Artikels.  
6. Wählen Sie die Aktion **Zugehörig**, die Aktion **Seriennr.** und dann die Aktion **Kommentar**, um einen separaten Kommentardatensatz zu erstellen.  
7. Wählen Sie das Feld **Gesperrt** aus, um die Serien- oder Chargennummer von sämtlichen Transaktionen auszuschließen.  

<!--If you create serial numbers in bulk by using the **Create Customized SN** or **Assign Serial No.** actions, you can enable **Create SN Information** and an information card will be created for each tracking line.

Alternatively, you can create an information card when you post journals or documents. On the **Item Tracking Code** page, turn on the **Create SN Info. on posting** or **Create SN Info. on posting** toggles. -->

Sie können Serien- oder Losinformationskarten später ändern.

## <a name="to-modify-existing-serial-or-lot-number-information"></a>Bestehende Serien- oder Chargennummerinformationen ändern

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Elemente** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie einen Artikel, der einen Artikelverfolgungscode hat und Serien- oder Chargennummerinformationen hat.
3. Auf der Seite **Artikelkarte** wählen Sie die **Posten** Aktion aus, und wählen Sie dann **Posten** aus.
4. Wählen Sie das Feld **Chargennr.** oder **Seriennr.** aus. Wenn es für die Artikelverfolgungsnummer Informationen gibt, dann wird die Seite **Chargennr.-Informationsliste** oder **Seriennr.-Informationsliste** geöffnet.  
5. Wählen Sie eine Karte aus, und wählen Sie die **Chargennr./Seriennummer Informationskarte** Aktion aus.  
6. Ändern Sie den Kurzbeschreibungstext, den Bemerkungsdatensatz oder das Feld **Gesperrt**.  

Sie können die Serien- oder Chargennummern oder Mengen nicht ändern. Um dies zu tun, müssen Sie den Artikelposten umbuchen. Weitere Informationen zur Umbuchung finden Sie unter [Chargen- und Seriennummern umbuchen](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).

## <a name="to-reclassify-serial-or-lot-numbers"></a>Chargen- oder Seriennummern umbuchen

Ein Umbuchen der Artikelverfolgung für einen Artikel bedeutet, dass eine Chargen- oder Seriennummer in eine neue Chargen- oder Seriennummer oder das Ablaufdatum in ein neues Ablaufdatum geändert wird. Wenn Sie mit Chargen arbeiten, können Sie außerdem mehrere Chargen zu einer Charge vereinigen. Verwenden Sie ein Artikel Umlagerungs Buch.-Blatt., um diese Aufgaben zu erledigen.

> [!NOTE]
> [!INCLUDE [prod_short](includes/prod_short.md)] überprüft, ob jede Zeile eine einzigartige Kombination aus Serien-, Los- und/oder Paketnummern hat. Wenn Sie eine Charge, ein Paket oder ein Los und ein Paket in mehrere Lose oder Pakete aufteilen möchten, müssen Sie mehrere Buch.-Blattzeilen verwenden.

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Element umklassifizieren. Erfassungen** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Zeile mit den relevanten Informationen aus. Weitere Informationen finden Sie unter [Lagerbestand anhand der Belege erfassen](inventory-how-count-inventory-with-documents.md) oder [Erfassen, Regulieren und Umbuchen von Lagerbestand mithilfe von Buch.-Blättern](inventory-how-count-adjust-reclassify.md).
3. Wählen Sie die **Artikelverfolgungszeilen** Aktion aus.  
4. Wählen Sie im Feld **Seriennr.** oder **Chargennr.** die aktuelle Serien- oder Chargennummer aus.  
5. Wenn Sie eine Einen neuen Artikelverfolgungsnummer eingeben möchten, geben Sie diese in das Feld **Neue Seriennr.** oder **Neue Chargennr.** ein. Bei Bedarf können Sie ein oder mehrere Chargen in einer oder mehreren neuen Chargen zusammenführen.  

    > [!NOTE]  
    > Wenn Sie Ablaufdatumsangaben umbuchen, werden die Artikel mit den frühesten Ablaufdatumsangaben für ausgehende Transaktionen zuerst vorgeschlagen. Um mehr zu erfahren, gehen Sie zu [Kommissionierung nach FEFO](warehouse-picking-by-fefo.md).  

6. Um ein neues Ablaufdatum für eine Serien- oder Chargennummer einzugeben, geben Sie dieses in das Feld **Neues Ablaufdatum** ein.  

    > [!IMPORTANT]  
    > * Wenn Sie eine Charge auf die gleiche Chargennummer, aber mit einem anderen Ablaufdatum umbuchen möchten, müssen Sie die gesamte Charge in einer Zeile des Artikel Umlagerungs Buch.-Blatts umbuchen.
    > * Wenn Sie mehrere Chargennummern zu einer neuen Chargennummer zusammenführen möchten (wenn also mehrere Chargen zu einer neuen Charge zusammengeführt werden), müssen Sie für alle Chargen das gleiche Ablaufdatum eingeben. 
    > * Wenn Sie eine vorhandene Charge in eine andere vorhandene Charge umbuchen, die ein anderes Ablaufdatum besitzt, müssen Sie das Ablaufdatum der zweiten Charge verwenden. 
    > * Wenn Sie das Feld **Neues Ablaufdatum** leer lassen, wird die Chargen- oder Seriennummer ohne Ablaufdatum umgebucht.  

7. Wenn Sie Informationen zu der alten Serien- oder Chargennummer haben, können Sie diese Informationen für die neue Serien- oder Chargennummer kopieren.  

    1. Klicken Sie auf der Seite **Artikelverfolgungszeilen** auf **Neue Seriennummerinformation** oder **Neuze Chargennummerninformation**  
    2. Wenn Sie Informationen aus der alten Chargen- oder Seriennummer kopieren möchten, klicken Sie auf **Info kopieren**.  
    3. Wählen Sie auf der Seite "Informationsliste" die Chargen- oder Seriennummer aus, von der Sie kopieren möchten, und wählen Sie **OK**.  

8. Wenn Sie die vorhandenen Informationen für eine Chargen- oder Seriennummer ändern möchten, können Sie die Chargen- oder Serieninformationen aufzeichnen.  
9. Buchen Sie das Buch.-Blatt, um die neuen Artikelverfolgungsnummern oder Ablaufdatumsangaben mit den entsprechenden Artikelposten zu verknüpfen.

## <a name="scan-barcodes-with-the-business-central-mobile-app"></a>Barcodes mit der mobilen Business Central-App scannen

[!INCLUDE [barcode-mobile-app](includes/barcode-mobile-app.md)]

Wenn Sie mehrere Serien-, Chargen- oder Paketbarcodes scannen möchten, können Sie auf der Seite **Artikelverfolgungszeilen** die Aktion **Mehrere scannen** verwenden. Nachdem Sie einen Barcode gescannt haben, wird sein Wert in das Feld auf der Seite eingegeben und das nächste Schnelleingabefeld wird verfügbar. Sie können auch das Barcodescannersymbol verwenden, um ein bestimmtes Feld auszufüllen.

In den folgenden Tabellen sind die Seiten aufgeführt, die das Scannen von Barcodes zur Artikelverfolgung über die mobile App [!INCLUDE [prod_short](includes/prod_short.md)] unterstützen.

|Seite  |Feldwerte, die Sie scannen können  |
|---------|---------|
|Artikelverfolgungszeilen     |* Seriennr.<br><br>* Neue Seriennr.<br><br>* Chargennr.<br><br>* Neue Chargennr.<br><br>* Paketnr.<br><br>* Neue Paketnr.|
|Logistik Umlag. Artikelverfolgungszeilen     |* Seriennr.<br><br>* Neue Seriennr.<br><br>* Chargennr.<br><br>* Neue Chargennr.<br><br>* Paketnr.<br><br>* Neue Paketnr.|
|Artikelablaufverfolgung     |* Seriennr. Filter<br><br>* Chargennr. Filter<br><br>* Paketnr. Filtern |
|Artikel Buch.-Blatt     |* Seriennr.<br><br>* Chargennr.<br><br>* Paketnr.     |
|Lageraktivitätszeile     |* Seriennr.<br><br>* Chargennr.<br><br>* Paketnr.<br><br>**Hinweis**: Die folgenden Seiten verwenden die Seite „Lageraktivitätszeile“:<br><br>* Seite 5780 „Lager Entnahme Unterformular“<br><br>* Seite 7378 „Lagerbestand Entnahme Unterformular“<br><br>* Seite 5771 „Lager Einlagerung Unterformular“<br><br>* Seite 7316 „Lagerplatzumlagerung Unterformular“<br><br>* Seite 7376 „Lagerbestand Einlagerung Unterformular“<br><br>* Seite 7383 „Lagerplatzumlagerung Unterformular“        |
|Logistik Umlag. Inventur Buch.-Blatt     |* Seriennr.<br><br>* Chargennr.<br><br>* Paketnr.         |

## <a name="see-also"></a>Siehe auch

[Artikelverfolgung mit Serien-, Chargen- und Paketnummern einrichten](inventory-how-setup-item-tracking.md)  
[Verfolgen von Artikeln mit Artikelverfolgung](inventory-how-to-trace-item-tracked-items.md)  
[Bestand](inventory-manage-inventory.md)  
[Designdetails: Artikelverfolgung](design-details-item-tracking.md)  
[Designdetails – Artikelverfolgung und Reservierungen](design-details-item-tracking-and-reservations.md)  
[Artikel reservieren](inventory-how-to-reserve-items.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
