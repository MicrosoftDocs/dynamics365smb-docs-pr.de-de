---
title: Designdetailsl- Artikelausgleich | Microsoft Docs
description: In diesem Thema wird beschrieben, wie Artikelausgleich passiert, wenn Sie eine Lagertransaktion buchen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, item ledger, costing
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: ddb2cd65abc96e27486782a1e9c9937858920f7c
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "916420"
---
# <a name="design-details-item-application"></a>Designdetails: Artikelausgleich
Wenn Sie eine Lagertransaktion buchen, wird die Mengenbuchung in den Artikelposten, die Wertbuchungen in den Wertposten erfasst. Weitere Informationen finden Sie unter [Designdetails: Planungsbuchung](design-details-inventory-posting.md).  
  
Darüber hinaus wird ein Artikelausgleich erstellt, um den Kostenempfänger mit seiner Kostenquelle zu verknüpfen, damit eine Kostenweiterleitung entsprechend der Kostenmethode erfolgen kann. Weitere Informationen finden Sie unter [Designdetails: Lagerabgangsmethoden".](design-details-costing-methods.md)  
  
[!INCLUDE[d365fin](includes/d365fin_md.md)] nimmt zwei Arten von Artikelausgleich vor.  
  
|Anwendungstyp|Description|  
|----------------------|---------------------------------------|  
|Mengenausgleich|Erstellt für alle Bestandstransaktionen|  
|Ausgleich Lagerwert reguliert|Erstellt für eingehende Posten zusammen mit einem Mengenausgleich als Folge eines Benutzereingriffs in speziellen Prozessen.|  
  
Artikelausgleiche können folgendermaßen vorgenommen werden.  
  
|Methode|Description|Anwendungstyp|  
|------------|---------------------------------------|----------------------|  
|Automatisch|Tritt als allgemeine Kosten entsprechend der Lagerabgangsmethode auf|Mengenausgleich|  
|Fixiert|Durch den Benutzer erstellt, wenn:<br /><br /> -   Verarbeiten von Rücklieferungen<br />-   Buchungskorrekturen<br />-   Um Warenausgänge rückgängig zu machen<br />-   Direktlieferung erstellen **Hinweis**  Der feste Ausgleich kann entweder manuell durch Eingabe einer Postennummer im Feld **Ausgegl. von Artikelposten** oder mithilfe einer Formel durchgeführt werden, wie etwa **Zu stornierende gebuchte Belegzeilen abrufen**.|Mengenausgleich<br /><br /> Kostenanwendung **Hinweis:** Der Kostenausgleich tritt nur in eingehenden Transaktionen auf, bei denen das Feld **Ausgegl. von Artikelposten** ausgefüllt ist, um einen festen Ausgleich zu erstellen. Siehe die folgende Tabelle.|  
  
Ob Mengen-Anwendungen oder Kostenanträge gemacht werden, hängt von der Richtung der Lagertransaktion und auch davon ab, ob der Artikelausgleich in Verbindung mit Systemprozessen automatisch gesetzt oder korrigiert wird.  
  
Die nachstehende Tabelle zeigt, basierend auf den zentralen Ausgleichsfeldern auf Lagertransaktionzeilen, wie die Kosten je nach Transaktionsrichtung fließen. Gibt auch an, wann und warum der Artikelausgleich den Typ Menge oder Kosten hat.  
  
||Ausgleich mit Artikelpostenfeld|Ausgegl. von Artikelpostenfeld|  
|-|--------------------------------|----------------------------------|  
|Anwendung für ausgehenden Posten|Der ausgehende Posten ruft die Kosten aus dem offenen eingehenden Posten ab.<br /><br /> **Mengenausgleich**|Nicht unterstützt|  
|Anwendung für eingehenden Posten|Der eingehende Posten verschiebt die Kosten in den offenen ausgehenden Posten.<br /><br /> Der eingehende Posten ist die Kostenquelle.<br /><br /> **Mengenausgleich**|Der eingehende Posten ruft die Kosten aus dem ausgehenden Posten ab. **Hinweis:**  Wenn dieser festen Ausgleich vorgenommen wird, wird die eingehende Transaktion als Verkaufsreklamation verarbeitet. Daher bleibt der ausgeglichene ausgehende Posten offen. <br /><br /> Der eingehende Posten ist NICHT die Kostenquelle.<br /><br /> **Ausgleich Lagerwert reguliert**|  
  
> [!IMPORTANT]  
>  Eine Verkaufsreklamation gilt NICHT als Kostenquelle, wenn "Fest" angewendet wird.  
>   
>  Der Verkaufsposten bleibt offen, bis die tatsächliche Herkunft gebucht wird.  
  
In einem Artikelausgleichsposten werden folgende Informationen erfasst.  
  
|Feld|Description|  
|---------------------------------|---------------------------------------|  
|**Artikelposten Lfd. Nr.**|Die Nummer des Artikelpostens für die Transaktion, für die dieser Ausgleichsposten erstellt wird|  
|**Eingeh. Artikelposten Lfd. Nr.**|Ausgeh. Artikelposten Lfd. Nr.: Die Artikelpostennummer des Lagereingangs, mit dem die Transaktion verknüpft werden soll (sofern möglich).|  
|**Ausgeh. Artikelposten Lfd. Nr.**|Ausgeh. Artikelposten Lfd. Nr.: Die Artikelpostennummer des Lagerabgangs, mit dem die Transaktion verknüpft werden soll (sofern möglich).|  
|**Menge**|Die zu erfassende Menge|  
|**Buchungsdatum**|Das Buchungsdatum der Transaktion|  
  
## <a name="inventory-increase"></a>Lagerzugänge  
Wenn Sie einen Lagerzugang buchen, wird ein einfacher Artikelausgleichsposten erfasst, ohne dass ein Ausgleich für einen ausgehenden Posten vorgenommen wird.  
  
### <a name="example"></a>Beispiel  
Die folgende Tabelle zeigt den Artikelausgleichsposten, der erstellt wird, wenn Sie eine Einkaufslieferung mit 10 Stück buchen.  
  
|Buchungsdatum|Eingeh. Artikelposten Lfd. Nr.|Ausgeh. Artikelposten Lfd. Nr.|Menge|Artikelposten Lfd. Nr.|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|01-01-20|1|0|10|1|  
  
## <a name="inventory-decrease"></a>Lagerabgänge  
Wenn Sie einen Lagerabgang buchen, wird ein Artikelausgleichsposten erfasst, der den Lagerbagang mit einem Lagerzugang verknüpft. Diese verknüpfung wird erstellt, indem die Lagerabgangsmethode des Artikels verwendet wird. Für Artikel mit den Kostenberechnungsmethoden FIFO, Standard und Durchschnitt basiert die Verknüpfung auf dem FIFO-Prinzip. Die Bestandsminderung wird auf die Bestandserhöhung mit dem frühesten Buchungsdatum angewendet. Für Artikel mit der Kostenberechnungsmethode LIFO basiert die Verknüpfung auf dem LIFO-Prinzip. Die Bestandsminderung wird auf die Bestandserhöhung mit dem neuesten Buchungsdatum angewendet.  
  
In der Tabelle **Artikelposten** enthält das Feld **Restmenge die Menge**, für die es noch keine Verknüpfung gibt. Wenn die Restmenge größer als 0 ist, wird das Kontrollkästchen **Offen** aktiviert.  
  
### <a name="example"></a>Beispiel  
Das folgende Beispiel zeigt einen Artikelausgleichsposten, der erstellt wird, wenn Sie eine Verkaufslieferung buchen, die 5 Einheiten der Artikel umfasst, die im vorherigen Beispiel eingegangen sind. Der erste Artikelausgleichsposten ist der Einkaufseingang. Der zweite Ausgleichsposten ist die Verkaufslieferung.  
  
Die folgende Tabelle zeigt die beiden Artikelausgleichsposten, die aus der Bestandserhöhung und der Bestandsminderung resultieren.  
  
|Buchungsdatum|Eingeh. Artikelposten Lfd. Nr.|Ausgeh. Artikelposten Lfd. Nr.|Menge|Artikelposten Lfd. Nr.|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|01-01-20|1|0|10|1|  
|01-03-20|1|2|-5|2|  
  
## <a name="fixed-application"></a>fester Ausgleich  
Sie können einen festen Ausgleich vornehmen, wenn Sie angeben, dass die Kosten eines Lagerzugangs einem bestimmten Lagerabgang (oder umgekehrt) zugeordnet werden sollen. Der feste Ausgleich betrifft die verbleibenden Mengen der Posten , er kehrt aber auch die exakten Kosten des ursprünglichen Postens um, zu oder von dem Sie den Ausgleich durchführen.  
  
Für einen festen Ausgleich verwenden Sie das Feld **Ausgleich mit Lfd. Nr**. oder **Ausgegl. von Posten in den Belegzeilen**, um den Artikelposten anzugeben, der mit der Transaktionszeile (oder ab dieser) verknüpft werden soll. Beispielsweise könnten Sie einen festen Ausgleich vornehmen, wenn Sie einen Kostenausgleich erstellen möchten, mit dem eine Verkaufsreklamation mit einer bestimmten Verkaufslieferung verknüpft werden soll, damit die Kosten der Verkaufslieferung exakt storniert werden. In diesem Fall ignoriert [!INCLUDE[d365fin](includes/d365fin_md.md)] die Lagerabgangsmethode ignoriert und der Lagerabgang (oder Lagerzugang, wenn es sich um eine Verkaufsreklamation handelt) mit dem von Ihnen angegebenen Artikelposten verknüpft. Das Vornehmen eines festen Ausgleichs hat den Vorteil, dass die Kosten der ursprünglichen Transaktion an die neue Transaktion übergeben werden können.  
  
### <a name="example--fixed-application-in-purchase-return"></a>Beispiel – Fester Ausgleich in der Einkaufsreklamation  
Das folgende Beispiel, das die Auswirkungen des festen Ausgleichs einer Einkaufsreklamation eines Artikels zeigt, der die FIFO-Kostenbewertungsmethode verwendet, basiert auf dem folgenden Szenario:  
  
1. In Postennummer 1 bucht der Benutzer einen Einkauf zu den Kosten von MW 10,00.  
2. In Postennummer 2 bucht der Benutzer einen Einkauf an Kosten MW 20,00.  
3. In Postennummer 3 bucht der Benutzer eine Einkaufsreklamation. Der Benutzer erstellt einen festen Ausgleich für den zweiten Verkauf, indem er die Artikelpostennummer im Feld **Anwendung für Artikeleintrag**in der Reklamationszeile eingibt.  
  
Die folgende Tabelle zeigt Artikelposten an, die aus dem Szenario resultieren.  
  
|**Buchungsdatum**|**Artikelpostenart**|**Menge**|**Einstandsbetrag (tatsächl.)**|**Artikelposten Lfd. Nr.**|  
|----------------------|---------------------------------------------------|------------------|----------------------------------------------------|---------------------------------------------------|  
|01-04-20|Einkauf|10|10.00|1|  
|01-05-20|Einkauf|10|20.00|2|  
|01-06-20|Einkauf (Reklamation)|-10|-20.00|3|  
  
Da ein fester Ausgleich aus der Einkaufsreklamation für den zweiten Einkaufsposten durchgeführt wird, werden die Artikel mit den richtigen Kosten zurückgegeben. Wenn der Benutzer nicht den festen Ausgleich ausgeführt hätte, dann wäre der zurückgegebene Artikel falsch mit MW 10,00 bewertet worden, da die Rückgabe gemäß dem FIFO-Prinzip auf den ersten Einkaufsposten angewendet worden wäre.  
  
Die folgende Tabelle zeigt den Artikelausgleichsposten, der aus dem festen Ausgleich resultiert.  
  
|Buchungsdatum|Eingeh. Artikelposten Lfd. Nr.|Ausgeh. Artikelposten Lfd. Nr.|Menge|Artikelposten Lfd. Nr.|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|01-06-20|1|3|10|3|  
  
Der Einstandsbetrag wird dann LCY 20.00, richtig mit der Einkaufsreklamation verknüpft.  
  
### <a name="example--fixed-application-with-average-cost"></a>Beispiel – Fester Ausgleich mit Durchschnittskosten  
Das folgende Beispiel, das die Auswirkungen des festen Ausgleichs einer Einkaufsreklamation, basiert auf dem folgenden Szenario eines Artikels mit der Durchschnittskostenbewertungsmethode:  
  
1. In Postennummer 1 und 2 bucht der Benutzer zwei Einkaufsrechnungen. Die zweite Rechnung hat den falschen EK-Preis von MW 1000,00.  
2. In Postennummer3 bucht der Benutzer eine Einkaufsgutschrift mit einem festen Ausgleich für den Einkaufsposten mit den falschen direkten Einheitskosten. Die Summe des Feldes **Kostenbetrag (Ist)** für die zwei fest ausgeglichenen Wertposten wird 0,00  
3. In Postennummer 4 bucht der Benutzer eine andere Einkaufsrechnung mit dem korrekten Direkteinheitspreis von MW 100,00  
4. In Postennummer 5 bucht der Benutzer eine Verkaufsrechnung.  
5. Die Bestandsmenge ist 0, und der Bestandwert ist ebenfalls 0,00.  
  
Die folgende Tabelle zeigt das Ergebnis des Szenarios auf die Wertposten des Artikels an.  
  
|Buchungsdatum|Artikelpostenart|Bewertete Menge|Einstandsbetrag (tatsächl.)|Ausgleich mit Artikelposten|Bew. z. Einst.-Pr. (durchschn.)|Artikelposten Lfd. Nr.|Postennr.|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|--------------------------------------------|-------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Einkauf|1|200.00||Nr.|1|1|  
|01-01-20|Einkauf|1|1000.00||Nein|2|2|  
|01-01-20|Einkauf|-1|-1000|2|Nein|3|3|  
|01-01-20|Einkauf|1|100.00||Nein|4|4|  
|01-01-20|Verkauf|-2|-300.00||Ja|5|5|  
  
Wenn der Benutzer nicht den festen Ausgleich zwischen der Einkaufsgutschrift und dem Einkauf mit dem falschen EK-Preis (Schritt 2 im vorherigen Szenario) eingerichtet hätte, dann würden die Kosten anders reguliert worden sein.  
  
Die folgende Tabelle zeigt die Auswirkung auf die Wertposten des Artikels an, wenn Schritt 2 im vorherigen Szenario ohne einen festen Ausgleich ausgeführt wird.  
  
|Buchungsdatum|Artikelpostenart|Bewertete Menge|Einstandsbetrag (tatsächl.)|Ausgleich mit Artikelposten|Bew. z. Einst.-Pr. (durchschn.)|Artikelposten Lfd. Nr.|Postennr.|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|--------------------------------------------|-------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Einkauf|1|200.00||Nr.|1|1|  
|01-01-20|Einkauf|1|1000.00||Nein|2|2|  
|01-01-20|Einkauf|-1|433,33||Ja|3|3|  
|01-01-20|Einkauf|1|100.00||Nein|4|4|  
|01-01-20|Verkauf|-2|866,67||Ja|5|5|  
  
In Postennummer 3 wird der Wert im Feld **Kostenbetrag (Ist)** durch die Methode „Durchschnitt“ bewertet und enthält daher die fehlerhafte Buchung von 1000,00. Entsprechend ergibt sich -433,33, d.h. ein überhöhter Kostenbetrag. Die Berechnung lautet: 1300 / 3 = .-433,33.  
  
In Postennummer 5 ist der Wert des -Felds **Kostenbetrag (Ist)** für diesen Posten aus dem gleichen Grund ebenfalls falsch.  
  
> [!NOTE]  
>  Wenn Sie einen festen Ausgleich für einen Lagerabgang eines Artikels erstellen, für den die Lagerabgangsmethode "Durchschnitt" festgelegt ist, wird dem Abgang nicht wie üblich der durchschnittliche Einstandspreis, sondern der von Ihnen angegebene Einstandspreis des Lagerzugangs zugeordnet. Dieser Lagerabgang wird damit nicht länger in die Berechnung des durchschnittlichen Einstandspreises einbezogen.  
  
### <a name="example--fixed-application-in-sales-return"></a>Beispiel – Fester Ausgleich in der Verkaufsreklamation  
Feste Ausgleiche sind ebenfalls sehr gut dafür geeignet, Kosten exakt umzukehren, etwa bei Verkaufsreklamationen.  
  
Das folgende Beispiel, das zeigt, wie ein fester Ausgleich die genaue Kostenumkehrung sicherstellt, basiert auf dem folgenden Szenario:  
  
1. Der Benutzer bucht eine Einkaufsrechnung.  
2. Der Benutzer bucht eine Verkaufsrechnung.  
3. Der Benutzer bucht eine Verkaufsgutschrift für den zurückgesendeten Artikel, der für den Verkaufsposten gilt, um die Kosten korrekt zu stornieren.  
4. Frachtkosten, die mit der zuvor gebuchten Einkaufsbestellung verbunden sind, gehen ein. Der Benutzer bucht dies als Artikel Zu-/Abschlag.  
  
Die folgende Tabelle zeigt das Ergebnis der Szenarioschritte 1 bis 3 für die Wertposten des Artikels an.  
  
|Buchungsdatum|Artikelpostenart|Bewertete Menge|Einstandsbetrag (tatsächl.)|Ausgegl. von Artikelposten|Artikelposten Lfd. Nr.|Postennr.|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Einkauf|1|1000.00||1|1|  
|02-01-20|Verkauf|-1|1000.00||2|2|  
|03-01-20|Verkaufs&gutschrift|1|1000|2|3|3|  
  
Die folgende Tabelle enthält den Wertposten,der aus Szenarioschritt 4, Buchung der Artikelkosten, resultiert.  
  
|Buchungsdatum|Artikelpostenart|Bewertete Menge|Einstandsbetrag (tatsächl.)|Ausgegl. von Artikelposten|Artikelposten Lfd. Nr.|Postennr.|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|04-01-20|(Artikel &Zu-/Abschlag)|1|100.00||1|4|  
  
Die folgende Tabelle zeigt die Auswirkung der exakten Kostenumkehrung der Wertposten des Artikels an.  
  
|Buchungsdatum|Artikelpostenart|Bewertete Menge|Einstandsbetrag (tatsächl.)|Ausgegl. von Artikelposten|Artikelposten Lfd. Nr.|Postennr.|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Einkauf|1|1000.00||1|1|  
|02-01-20|Verkauf|-1|1100.00||2|2|  
|03-01-20|Verkaufs&gutschrift|1|1100.00|2|3|3|  
|04-01-20|(Artikel &Zu-/Abschlag)|1|100.00||1|4|  
  
Wenn Sie die Stapelverarbeitung **Kostenanpassung Artikeleinträge** ausführen, werden die erhöhten Kosten des Einkaufspostens aufgrund des Zu-/Abschlags (Artikelnummer) zum Verkaufsposten weitergeleitet (Postennummer 2). Der Verkaufsposten übergibt dann diese erhöhten Kosten an den Verkaufsgutschriftposten weiter (Postennummer 3). Das Endergebnis ist, dass die Kosten korrekt umgekehrt werden.  
  
> [!NOTE]  
>  Wenn Sie mit Reklamationen oder Gutschriften arbeiten und im Feld **Einst.-Pr.-Rückverfolg. notw.** entweder die Seite **Kreditoren und Einkauf Einr** oder in **Debitoren und Verkauf Einr.** entsprechend Ihren Gegebenheiten Einstandspreisrückverfolgung eingerichtet haben, dann werden [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisch ausgefüllt, wenn Sie die Funktion **Beleg kopieren** verwenden. Wenn Sie die Funktion **Zu stornierende gebuchte Belegzeilen abrufen** verwenden, werden diese Felder immer automatsich ausgefüllt.  
  
> [!NOTE]  
>  Wenn Sie eine Transaktion mit einem festen Ausgleich buchen und der Artikelposten, zu dem Sie verknüpfen, ist geschlossen (d. h. die Restmenge ist gleich 0), wird automatisch der alte Ausgleich zurückgenommen und erneut mit dem Artikelposten ausgeglichen, wobei der von Ihnen angegebene feste Ausgleich verwendet wird.  
  
## <a name="transfer-application"></a>Umlagerungs-Anwendung  
Wenn ein Artikel von einem Lagerort zu einem anderen innerhalb des Lagerbestands übertragen wird, wird eine Anwendung zwischen den beiden Übergangsposten erstellt. Die Bewertung eines Übergangspostens hängt von der Lagerabgangsmethode ab. Für Artikel mit der Kostenberechnungsmethode Durchschnitt wird Bewertung mithilfe der durchschnittlichen Kosten in der Durchschnittskostenperiode erstellt, in der das Bewertungsdatum der Übertragung auftritt. Für Artikel mit anderen Kostenbewertungsmethoden wird die Bewertung durch Rückverfolgung zu den Kosten der ursprünglichen Bestandszunahme durchgeführt.  
  
### <a name="example--average-costing-method"></a>Beispiel - Durchschnittskostenberechnungsmethode  
Das folgende Beispiel, das zeigt, wie Übergangsposten ausgeglichen werden, basiert auf dem folgenden Szenario für einen Artikel mit der Durchschnittskostenbewertungsmethode und der Durchschnittskostenperiode Tag.  
  
1. Der Benutzer kauft den Artikel zu einem Preis von MW 10,00 ein.  
2. Der Benutzer kauft den Artikel erneut zu einem Preis von MW 20,00 ein.  
3. Der Benutzer lagert den Artikel von Lagerort BLAU zu ROT um.  
  
Die folgende Tabelle zeigt die Auswirkung der Umlagerung auf die Wertposten des Artikels an.  
  
|Buchungsdatum|Artikelpostenart|Lagerortcode|Bewertete Menge|Einstandsbetrag (tatsächl.)|Postennr.|  
|-------------------------------------|-----------------------------------------------|--------------------------------------|-----------------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|Einkauf|BLAU|1|10.00|1|  
|01-01-20|Einkauf|BLAU|1|20.00|2|  
|02-01-20|Umlagerung|BLAU|-1|15.00|3|  
|02-01-20|Umlagerung|ROT|1|15.00|4|  
  
### <a name="example--standard-costing-method"></a>Beispiel - Lagerabgangsmethode  
Das folgende Beispiel, das zeigt, wie Übergangsposten ausgeglichen werden, basiert auf dem folgenden Szenario für einen Artikel mit der Standardkostenbewertungsmethode und der Durchschnittskostenperiode Tag.  
  
1. Der Benutzer kauft den Artikel zu einem Standardpreis von MW 10,00 ein.  
2. Der Benutzer überträgt den Artikel aus Lagerort BLAU zu ROT zu einem Einstandspreis (fest) von MW 12,00.  
  
Die folgende Tabelle zeigt die Auswirkung der Umlagerung auf die Wertposten des Artikels an.  
  
|Buchungsdatum|Artikelpostenart|Lagerortcode|Bewertete Menge|Einstandsbetrag (tatsächl.)|Postennr.|  
|-------------------------------------|-----------------------------------------------|--------------------------------------|-----------------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|Einkauf|BLAU|1|10.00|1|  
|02-01-20|Transfer|BLAU|-1|10,00|2|  
|02-01-20|Umlagerung|ROT|1|10,00|3|  
  
Da der Wert des ursprünglichen Bestandszunahme MW 10,00 ist, wird die Übertragung zu diesen Kosten bewertet, nicht mit MW 12,00.  
  
## <a name="reapplication"></a>Erneuter Ausgleich  
Wegen der Art, in der Einstandspreise berechnet werden, kann ein fehlerhafter Artikelausgleich zu falschen durchschnittlichen Einstandspreisen und zu falschen Einstandspreisen führen. Der folgenden Szenarien verursachen möglicherweise falsche Artikelausgleiche, was erfordert, dass Sie Artikelausgleiche annullieren und Artikelposten erneut ausgleichen:  
  
* Sie haben vergessen, einen festen Ausgleich vorzunehmen.  
* Sie haben einen fehlerhaften festen Ausgleich vorgenommen.  
* Sie möchten die erstellte Anwendung automatisch beim Buchen überschreiben, entsprechend der Lagerabgangsmethode des Artikels.  
* Sie müssen einen Artikel zurückliefern, für den bereits ein Verkauf manuell angewendet wurde, ohne die Funktion **Zu stornierende Belegzeilen abrufen** zu verwenden und daher die Anwendung annullieren.  
  
[!INCLUDE[d365fin](includes/d365fin_md.md)] bietet eine Funktion zum Analysieren und Korrigieren der Artikelausgleiche. Dieser Vorgang wird auf der Seite **Arbeitsblatt anwenden** ausgeführt.  
  
## <a name="see-also"></a>Siehe auch  
[Designdetails: Lagerkostenberechnung](design-details-inventory-costing.md)  
[Designdetails: Kostenberechnungsmethoden](design-details-costing-methods.md)  
[Designdetails: Durchschnittskosten](design-details-average-cost.md)  
[Designdetails: Kostenregulierung](design-details-cost-adjustment.md)  
