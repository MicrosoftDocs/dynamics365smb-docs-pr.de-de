---
title: Abstimmen der Lagerkosten mit der Finanzbuchhaltung
description: 'Am Ende der Buchhaltungsperioden muss eine Sequenz von Steuerelementen und Prüfungsaufgaben durchgeführt werden, um einen korrekten und ausgeglichenen Bestandswert auszuweisen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'warehouse, stock'
ms.search.form: 9297
ms.date: 06/16/2021
ms.author: edupont
---
# Abstimmen der Lagerkosten mit der Finanzbuchhaltung

Wenn Sie Lagertransaktionen buchen, z. B. Verkaufslieferungen, Einkaufsrechnungen oder Lagerregulierungen, werden die veränderten Artikelkosten in den Artikelwerteinträgen aufgezeichnet. Um diese Änderung des Lagerwerts in Ihren Finanzbüchern wiederzugeben, werden die Lagerkosten automatisch zu den entsprechenden Lagerkonten in der Finanzbuchhaltung gebucht. Für jede Lagertransaktion, die Sie buchen, werden die entsprechenden Werte in der Hauptbuchhaltung im Lagerkonto, im Korrekturkonto und im Lagerverbrauchskonto gebucht.

Die automatische Lagerbuchung wird durch das Feld **Automatische Lagerbuchung** auf der Seite **Lagereinrichtung** definiert.

Selbst wenn Lagerkosten automatisch in die Finanzbuchhaltung gebucht werden, ist es immer noch notwendig sicherzustellen, dass die Kosten für Waren zur zugehörigen ausgehenden Transaktion weitergeleitet werden, insbesondere in Situationen, in denen Sie Waren verkaufen, bevor Sie den Kauf dieser Waren in Rechnung stellen. Dies wird als Kostenanpassung bezeichnet. Artikelkosten werden automatisch angepasst, wenn Sie Artikeltransaktionen buchen, Sie können jedoch auch Artikelpreise manuell anpassen. Weitere Informationen finden Sie unter [Artikelkosten anpassen](inventory-how-adjust-item-costs.md).

## Lagerkosten manuell buchen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Lagerkosten ins Hauptbuch buchen** ein, und wählen Sie dann den zugehörigen Link.
2. Sie buchen eine Lagerkosten manuell in der Hauptbuchhaltung, indem Sie den Batchauftrag ausführen. Wenn Sie diesen Batchauftrag ausführen, werden auf Basis der Wertposten Hauptbuchungsposten erstellt. Sie können die Posten so buchen, dass sie pro Buchungsgruppe zusammengefasst werden.

> [!NOTE]  
> Beim Ausführen dieses Batchauftrages könnten Sie auf Fehler treffen, die ihre Ursache in fehlender Einrichtung oder nicht kompatibler Dimensionseinrichtung haben. Wenn die Stapelverarbeitung auf Fehler in der Dimensionseinrichtung stößt, setzt sie diese Fehler außer Kraft und verwendet die Dimensionen des Wertpostens. Bei allen anderen Fehlern überspringt der Batchauftrag das Buchen der Wertposten und listet sie am Ende des Berichts im Abschnitt “Übersprungene Artikel” auf. Solen diese Artikel gebucht werden, müssen Sie die Fehler beheben.

Wenn Sie eine Liste der Fehler anzeigen möchten, bevor Sie den Batchauftrag ausführen, führen Sie den Bericht **Lagereinstandspreise buchen - Test** aus. In dem Testbericht werden alle gefundenen Fehler aufgelistet, die während der Testbuchung aufgetreten sind. Sie können die Fehler dann beheben und die Stapelverarbeitung zum Buchen der Lagerregulierung ausführen, ohne dass Posten übersprungen werden.

Wenn Sie sich nur einen Überblick verschaffen möchten, welche Werte in der Finanzbuchhaltung gebucht werden können, das Buchen selbst aber nicht vornehmen möchten, können Sie die Stapelverarbeitung **Lagerregulierung buchen** ausführen, ohne dass die Werte tatsächlich in der Finanzbuchhaltung gebucht werden. Dazu müssen Sie auf der Anforderungsseite das Häkchen im Feld **Buchen** entfernen. In diesem Fall wird, wenn Sie der Batchauftrag ausführen, nur der Bericht erzeugt, der die Werte enthält, die in der Hauptbuchhaltung bereit stehen, aber nicht gebucht sind.

## Überprüfen der Abstimmung zwischen den Lagerposten und der Finanzbuchhaltung
Die Seite **Lager – Sachpostenabstimmung** ermöglicht Folgendes:

- Gibt Aufschluss über Abstimmungsdifferenzen. Hierzu werden die in der Finanzbuchhaltung erfassten Werte mit den in den Inventurposten erfassten Werten verglichen.
- Zeigt nicht abgestimmte Einstandsbeträge in den Wertposten der Inventurposten so an, als seien sie entsprechenden lagerbezogenen Konten in der Finanzbuchhaltung zugeordnet, und vergleicht sie mit den tatsächlich erfassten Summen auf den gleichen Konten in der Finanzbuchhaltung.
- Spiegelt die Struktur der doppelten Buchführung aus der Finanzbuchhaltung wider, indem die Daten entsprechend dargestellt werden. So besitzt beispielsweise ein Lagerverbrauchsposten einen entsprechenden Lagerposten.
- Ermöglicht das Anzeigen der zugrunde liegenden Einstandsbeträge mittels Drilldown-Navigation.
- Beinhaltet Filter zum Eingrenzen der Analyse anhand von Datum, Artikel und Lagerort.
- Gibt Aufschluss über die Gründe für Abstimmungsdifferenzen in Form von Informationsmeldungen.


In der Spalte **Name** (am äußerst linken Rand des Gitters) werden die verschiedenen Sachkontoarten angezeigt, die mit Lagerbestand verknüpft sind.

Die Spalten **Lagerbestand**, **Lager (Interim)** und **Aktiviert Lager** enthalten die fakturierten, nicht fakturierten und WIP-Summen jeder Sachkontoart. Diese werden aus Wertposten berechnet, d.h., sie werden auf die Sachkontoarten übertragen, auf denen sie sich nach dem Buchen in die Finanzbuchhaltung befinden.

Die Spalte **Gesamt** enthält die (fett formatierte) Summe der Wertpostenbeträge in den drei Lagerbestandsspalten.

Die Spalte **Fibu gesamt** enthält die (fett formatierten) Beträge für die einzelnen, in der Finanzbuchhaltung vorhandenen Sachkontoarten. Diese Werte werden auf der Grundlage von Sachposten berechnet, stellen also die Lagerkosten dar, die bereits in die Finanzbuchhaltung gebucht wurden.

Die Spalte **Differenz** enthält die Differenz zwischen **Fibu gesamt** und **Gesamt**.

Am oberen Rand der Seite **Lager - Sachpostenabstimmung** können Sie mithilfe von Filtern beispielsweise die Periode eingrenzen, für die Sie Informationen ermitteln möchten.

Wenn Sie ein Häkchen im Kontrollkästchen **Warnung anzeigen** setzen und wenn es Abweichungen zwischen den Lagerbestandssummen und den Werten in der Fibu gesamt gibt, werden im Feld **Warnung** des Gitters Meldungen angezeigt, in denen die jeweilige Abweichung beschrieben wird. Wenn Sie das Feld "Warnung" auswählen, gibt die Anwendung weitere Informationen zum Inhalt der Warnung.

Wenn Sie alle entsprechenden Filter eingegeben haben, wählhen Sie die Aktion **Matrix anzeigen**. Die Daten werden berechnet, und die Matrixseite wird geöffnet.

In der äußerst linken Spalte des Gitters werden die verschiedenen Kontoarten der Finanzbuchhaltung angezeigt, die mit dem Lagerbestand verknüpft sind. Für jede dieser Kontoarten werden im Gitter die fakturierten, nicht fakturierten (Interims-) und WIP-Lagerbestandssummen angezeigt. Diese Summen wurden aus den Wertposten berechnet.

In den nächsten Spalten werden für dieselben Kontoarten die Summen angezeigt, die aus den Sachposten berechnet wurden.

Wählen Sie in einem der Summenfelder den Betrag, damit die Lagerberichtsposten angezeigt werden, mit denen die Summen berechnet wurden. Für Lagerbestandssummen sind die Lagerberichtsposten die Summen der Wertposten für die Artikel. Für die Werte in Fibu gesamt sind die Lagerberichtsposten die Summen aus den Sachposten.

## Melden von Kosten und Abstimmen mit der Finanzbuchhaltung
Weitere Berichte, Rückverfolgungsfunktionen und ein spezielles Abstimmungsinstrument stehen dem Prüfer oder Controller zur Verfügung, der für die Meldung eines korrekten und ausgewogenen Bestandswerts an die Finanzabteilung verantwortlich ist.

Die Werte werden in der folgenden Tabelle beschrieben.    

|**Prozess**|**Siehe**|  
|------------|-------------|  
|Anzeigen des Lagerwerts ausgewählter Artikel, einschließlich Informationen zu Mengen und Werten bei Erhöhung oder Verringerung des Lagerbestands innerhalb eines bestimmten Zeitraums|Bericht **Aktuellen Lagerwert ermitteln**|  
|Anzeigen des Lagerwerts ausgewählter Fertigungsaufträge in "Aktiviert Lager", beispielsweise der Mengen und Werte für Verbrauch, Kapazitätsauslastung und Ausgabe in laufenden Fertigungsaufträgen|Bericht **Lagerbewertung - Aktiviert**|  
|Anzeigen des Lagerwerts ausgewählter Artikel, einschließlich der tatsächlichen Kosten und der Soll-Kosten zum angegebenen Datum|Bericht **Lagerbew.-Einst.-Pr.-Ermittl.**|  
|Verwenden eines Berichts zum Analysieren der Ursachen für Kostenschwankungen oder zum Verschaffen eines Überblicks über den Kostenanteil verkaufter Artikel (Lagerverbrauch)|Bericht **Kostenanteilsanalyse**|  

## Weitere Informationen  
[Verwalten der Bestandsregulierung](finance-manage-inventory-costs.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verkauf](sales-manage-sales.md)    
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]