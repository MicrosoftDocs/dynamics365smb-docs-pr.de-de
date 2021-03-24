---
title: 'Designdetails: Ausgleich von Bedarf und Vorrat | Microsoft Docs'
description: Um zu erkennen, wie das Planungssystem funktioniert, ist es erforderlich, die priorisierten Ziele des Planungssystems zu kennen. Die wichtigsten davon sind, sicherzustellen, dass jeglicher Bedarf durch genügenden Vorrat befriedigt wird und jeder Vorrat einem Zweck dient.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f8f09c843397c7b3fa0a24bc90f5799a157fa883
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388724"
---
# <a name="design-details-balancing-demand-and-supply"></a>Designdetails: Ausgleich von Bedarf und Vorrat
Um zu erkennen wie das Planungssystem funktioniert, ist es notwendig, die priorisierten Ziele des Planungssystems zu kennen, von denen die wichtigsten sind, Folgendes sicherzustellen:  

- Jeder Bedarf wird durch ausreichenden Vorrat abgedeckt.  
- Jeder Vorrat dient einem Zweck.  

 Im Allgemeinen werden diese Ziele durch den Augleich von Bedarf und Vorrat erzielt.  

## <a name="demand-and-supply"></a>Bedarf und Vorrat
 Bedarf ist der Oberbegriff, der für jede Art Brutto-Bedarf verwendet wird, beispielsweise für Verkaufsauftrags und Komponentenbedarf aus einem Fertigungsauftrag. Darüber hinaus ermöglicht die Anwendung noch weitere technische Bedarfsarten, wie z.B. negative Lagerbestände und Einkaufsreklamationen.  

  Vorrat ist der allgemeine Begriff für jede Art von positiver oder eingehender Menge, wie etwa Bestands-, Einkauf-, Montage-, Fertigungs- oder eingehende Umlagerungen. Darüber hinaus stellt möglicherweise eine Verkaufsreklamation ebenfalls einen Vorrat dar.  

  Um die vielen Quellen von Nachfrage und Angebot zu sortieren, organisiert das Planungssystem sie auf zwei Zeitachsen, die Bestandsprofile genannt werden. Das eine Profil enthält Bedarfsereignisse und das andere enthält die entsprechenden Zubehörereignisse. Jedes Ereignis repräsentiert eine Auftragsnetzwerkeinheit, wie etwa eine Verkaufsauftragszeile, einen Artikelposten oder eine Fertigungsauftragszeile.  

  Wenn Bestandsprofile geladen werden, werden die verschiedenen BBedarf-Vorrat-Sätze ausgeglichen, um einen Beschaffungsplan auszustellen, der die aufgeführten Ziele erfüllt.  

  Planungsparameter und Lagerbestände sind andere Arten von Bedarf und Vorrat bzw. sind einem integrierten Ausgleich unterworfen, um den Lagerbestand wieder aufzufüllen. Weitere Informationen finden Sie unter [Designdetails: Behandlungs-Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md).

## <a name="the-concept-of-balancing-in-brief"></a>Das Ausgleichskonzept in Kürze
  Die Nachfrage wird von den Debitoren eines Unternehmens gestellt. Der Vorrat ist das, was das Unternehmen erstellen oder entfernen kann, um Saldi auszugleichen. Die Planungssystem beginnt mit dem unabhängigen Bedarf und verfolgt ihn rückwärts zum Vorrat.  

   Die Bestandsprofile werden verwendet, um Informationen über die Bedarfe und Vorräte sowie über Mengen und Timing zu enthalten. Diese Profile bilden im Wesentlichen die zwei Seiten der Ausgleichsskala.  

   Die Zielsetzung des Planungsmechanismus ist, den Bedarf und den Vorrat eines Artikels zu balancieren, um sicherzustellen, dass der Vorrat den Bedarf in einer durchführbaren Art deckt, wie durch die Planungsparameter und Regeln definiert.  

   ![Überblick über den Ausgleich zwischen Angebot und Nachfrage](media/nav_app_supply_planning_2_balancing.png "Überblick über den Ausgleich zwischen Angebot und Nachfrage")

## <a name="dealing-with-orders-before-the-planning-starting-date"></a>Umgang mit Aufträgen vor dem Planungs-Startdatum
Um zu vermeiden, dass ein Beschaffungsplan unmöglichen und daher unbrauchbare Vorschläge anzeigt, berücksichtigt das Planungssystem die Periode bis zum Startdatum als fixierte Zone, für die nichts geplant wird. Die folgende Regel gilt für die fixierte Zone:  

Alle Vorräte und Bedarfe vor dem Startdatum der Planungsperiode gelten als Teil des Lagerbestands oder als geliefert.  

Entsprechend schlägt das Planungssystem, mit wenigen Ausnahmen, keine Änderungen an Beschaffungsaufträgen in der fixierten Zone vor, und keine Auftragsnachverfolgungsverknüpfungen werden für diese Periode erstellt oder gespeichert.  

Die Ausnahmen dieser Regel sind die folgenden:  

   * Wenn der voraussichtlich verfügbare Lagerbestand, einschließlich die Summe von Bedarf und Vorrat in der fixierten Zone, geringer als Null ist.  
   * Wenn Serien-/Chargennummern auf den zurückdatierten Aufträgen erforderlich sind.  
   * Wenn der Vorrat-Bedarf-Satz durch eine Auftrag-zu-Auftrag-Richtlinie verknüpft ist.  

Wenn der anfänglich verfügbare Lagerbestand geringer als Null ist, schlägt das Planungssystem einen Notfallbeschaffungsauftrag am Tag vor der Planperiode vor, um die fehlende Menge zu decken. Deshalb ist der voraussichtliche und der verfügbare Lagerbestand immer mindestens Null, wenn die Planung für die zukünftige Periode beginnt. Die Planungszeile für diesen Beschaffungsauftrag zeigt ein Notwarnsymbol an , und zusätzliche Informationen werden beim Lookup angezeigt.  

### <a name="seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone"></a>Serien-/Chargennummern und Auftrag-zu-Auftrag-Links sind von der fixierten Zone ausgenommen  
   Wenn Serien-/Chargennummern erforderlich sind, oder ein Auftrag-zu-Auftrag-Link vorhanden ist, beachtet das Planungssystem die fixierte Zone nicht und berücksichtigt solche Mengen, die vom dem Startdatum zurückdatiert sind und möglicherweise Korrekturmaßnahmen erfordern, wenn bedarf und Vorrat nicht synchronisiert sind. Der Geschäftsgrund für dieses Prinzip ist, dass solche bestimmten bedarf-Vorrat-Sätze übereinstimmen müssen, um sicherzustellen, dass dieser bestimmte Bedarf erfüllt wird.

## <a name="loading-the-inventory-profiles"></a>Bestand Laden von Profilen
Um die vielen Quellen von Nachfrage und Angebot zu sortieren, organisiert das Planungssystem sie auf zwei Zeitachsen, die Bestandsprofile genannt werden.  

Die normalen Typen von Bedarf und Vorrat mit Fälligkeitsdaten auf oder nach dem Planungsstartdatum werden in die Bestandsprofile geladen. Wenn sie geladen werden, werden die verschiedenen Bedarf- und Vorrattypen entsprechend allgemeinen Prioritäten, wie Fälligkeitsdatum, Stücklistenebenen, Lagerort und Variante sortiert. Darüber hinaus werden Auftragsprioritäten auf verschiedene Arten angewendet, um sicherzustellen, dass der wichtigste Bedarf zuerst erfüllt wird. Weitere Informationen finden Sie unter [Priorisieren von Aufträgen](design-details-balancing-demand-and-supply.md#prioritizing-orders).  

Wie bereits erwähnt, kann Bedarf auch negativ sein. Das bedeutet, dass es als Vorrat behandelt werden sollte, jedoch anders als die normalen Vorratstypen, gilt negativer Bedarf als fester Vorrat. Das Planungssystem kann dies berücksichtigen, schlägt aber keine Änderungen dafür vor.  

Im Allgemeinen berücksichtigt das Planungssystem alle Beschaffungsaufträge nach dem Startdatum als änderbar, um den Bedarf zu erfüllen. Sobald eine Menge von einem Beschaffungsauftrag gebucht wurde, kann sie jedoch vom Planungssystem nicht mehr geändert werden. Entsprechend können die folgenden verschiedenen Aufträge nicht neu geplant werden:  

- Freigegebene Fertigungsaufträge, bei denen Verbrauch oder Ausgabe gebucht wurde.  
- Montageaufträge, bei denen Verbrauch oder Ausgabe gebucht wurde.  
- Umlagerungsaufträge, in denen Lieferung gebucht wurde.  
- Einkaufsbestellungen, in denen der Wareneingang gebucht wurde.  

Abgesehen vom Laden von Bedarf- und Vorrattypen werden bestimmte Typen im Hinblick auf besondere Regeln und Abhängigkeiten geladen, die nachfolgend beschrieben werden.  

### <a name="item-dimensions-are-separated"></a>Artikeldimensionen sind aufgeteilt  
Der Beschaffungsplan muss pro Kombination der Artikeldimensionen, wie Variante und Lagerort berechnet werden. Es gibt jedoch keinen Grund, eine theoretische Kombination zu berechnen. Nur jene Kombinationen, die einen Bedarf ausführen und/oder Bedarfsposten müssen berechnet werden.  

Das Planungssystem steuert dies, indem es das Bestandsprofil durchläuft. Wenn eine neue Kombination gefunden wird, erstellt die Anwendung einen internen Steuerdatensatz, der nun die tatsächlichen Kombinationsinformationen enthält. Die Anwendung fügt die SKU als Steuerdatensatz oder externe Schleife ein. Als Ergebnis werden die richtigen Planungsparameters entsprechend einer Kombination aus Variante und Lagerort gesetzt, und die Anwendung kann dann an die inneren Schleife übergehen.  

> [!NOTE]  
>  Die Anwendung verlangt nicht, dass der Benutzer einen SKU-Datensatz eingibt, wenn ein Bedarf und/oder ein Vorrat für eine bestimmte Kombination von Variante und Lagerort eingegeben wird. Wenn die Lagerhaltungsdaten für eine angegebene Kombination nicht vorhanden sind, erstellt die Anwendung einen eigenen temporären Lagerhaltungsdatendatensatz basierend auf den Artikelkartendaten. Wenn „Lagerort erforderlich“ in der Bestandseinrichtungsseite auf „Ja“ gesetzt ist, muss entweder eine SKU erstellt werden, oder „Komponenten am Lagerort“ muss auf „Ja“ gesetzt werden. Weitere Informationen finden Sie unter [Designdetails: Bedarf an leerem Lagerort](design-details-demand-at-blank-location.md)  

### <a name="seriallot-numbers-are-loaded-by-specification-level"></a>Serien-/Chargennummern werden durch die Spezifikations-Ebene geladen  
Attribute in Form von Serien-/Chargennummern werden in die Bestandsprofile zusammen mit dem Bedarf und dem Vorrat geladen, denen sie zugeordnet sind.  

Bedarfs- und Vorratsattribute werden nach Auftragspriorität sowie nach Spezifikationsebene angeordnet. Da Serien-/Chargennummernübereinstimmungen die Ebene der Spezifikation widerspiegeln, gilt: Der spezifischere Bestand, wie etwa eine Chargennummer, die speziell nach Verkaufszeile ausgewählt wurde, sucht eine Übereinstimmung vor einem weniger spezifischen Bestand, etwa einem Verkauf aus einer beliebigen ausgewählten Chargennummer.  

> [!NOTE]  
>  Es gibt keine dedizierten Prioritisierungsregeln für serien-/chargennummerierten Bedarf und Vorrat, außer den Ebenen der Spezifikation, die durch ihre Kombinationen von Serien- und der Chargennummern und die Artikelverfolgungseinrichtung der einbezogenen Artikel definiert sind.  

Während des Ausgleichs betrachtet das Planungssystem Vorrat mit Serien-/Chargennummern als nicht flexibel und versucht nicht, diese Beschaffungsaufträge zu erhöhen oder umzuplanen (sofern sie nicht in einer Auftrag-zu-Auftrag-Beziehung verwendet werden). Vgl. Auftrag-zu-Auftrags-Link werden nie unterbrochen). Diese schützt das Vorrat davor, mehrere und möglicherweise widersprüchliche Ereignismeldungen zu erhalten, wenn eine Bedarfssicherung unterschiedliche Attribute hat, etwa eine Sammlung verschiedener Seriennummern.  

Ein weiterer Grund dafür, dass Serien-/Chargen-nummerierter Vorrat unflexibel ist, besteht darin, dass Serien-/Chargennummern allgemein so spät im Prozess zugewiesen werden, dass Änderungsvorschläge verwirrend wären.  

Der Ausgleich von Serien-/Losnummern respektiert nicht die Aktion *Fixierte Zone*. Wenn Bedarf und Vorrat nicht synchronisiert sind, schlägt das Planungssystem Änderungen vor oder neue Aufträge, unabhängig vom Startdatum der Planung.  

### <a name="order-to-order-links-are-never-broken"></a>Auftrag-zu-Auftrag-Links werden nie unterbrochen.  
Wenn ein Auftrag-zu-Auftrag-Artikel geplant wird, darf der verknüpfte Vorrat nicht für einen anderen Bedarf verwendet werden, als den, für den er ursprünglich gedacht war. Der verknüpfte Bedarf sollte nicht durch einen anderen zufälligen Vorrat abgedeckt werden, selbst wenn er in der derzeitigen Situation nach Zeit und Menge verfügbar ist. Beispielsweise kann ein Montageauftrag, der mit einem Verkaufsauftrag in einem Auftragsfertigungsszenario verknüpft ist, nicht verwendet werden, um anderen Bedarf zu decken.  

Auftrag-zu-Auftrag-Bedarfe und Angebot müssen sich genau ausgleichen. Das Planungssystem stellt den Vorrat unter allen Umständen sicher, ohne Auftragsdimensionierungsparameter, -modifizierer oder Mengen im Bestand (ausgenommen Mengen im Zusammenhang mit den verknüpften Aufträgen) zu berücksichtigen. Aus dem gleichen Grund schlägt das System die Minderung überschüssigen Vorrats vor, wenn der verknüpfte Bedarf vermindert wird.  

Dieser Ausgleich beeinflusst auch die zeitliche Steuerung. Der begrenzte Zeitraum, der durch den Zeitrahmen gewährt wird, wird nicht berücksichtigt; der Vorrat wird neu geplant, wenn die zeitliche Steuerung des Bedarfs geändert wurde. Es wird jedoch die Toleranzzeit berücksichtigt und Auftrag-zu-Auftrag-Vorrat wird nicht ausgeplant, ausgenommen interner Vorrat eines mehrstufigen Fertigungsauftrags (Projektauftrag).  

> [!NOTE]  
>  Serien-/Chargennummern können auch auf Auftrag-zu-Auftrag-Bedarfen angegeben werden. In diesem Fall gilt der Vorrat nicht standardmäßig als inflexibel, wie dies normalerweise der Fall ist für Serien-/Chargennummern. In diesem Fall erhöht/mindert das System gemäß den Änderungen des Bedarfs. Darüber hinaus gilt: Wenn ein Bedarf variierende Serien-/Chargennummern enthält (etwa mehr als eine Chargennummer), wird ein Beschaffungsauftrag pro Charge vorgeschlagen.  

> [!NOTE]  
>  Planungen sollten nicht dazu führen, dass Beschaffungsaufträge erstellt werden, die durch eine Auftrag-zu-Auftrag-Verknüpfung gebunden sind. Wenn der Plan verwendet wird, sollte er nur als Generator des abhängigen Bedarfs in einer Produktionsumgebung verwendet werden.  

### <a name="component-need-is-loaded-according-to-production-order-changes"></a>Der Komponentenbedarf wird gemäß den Fertigungsauftragsänderungen geladen  
Wenn es Fertigungsaufträge bearbeitet, muss das Planungssystem die benötigten Komponenten überwachen, bevor es sie in das Anforderungsprofil lädt. Komponentenzeilen, die aus einem ergänzten Fertigungsauftrag resultieren, ersetzen die des ursprünglichen Auftrags. Dadurch ist sichergestellt, dass das Planungssystem festlegt, dass Planungszeilen für Komponentenbedarf nicht dupliziert werden.  

###  <a name="safety-stock-may-be-consumed"></a><a name="BKMK_SafetyStockMayBeConsumed"></a> Sicherheitsbestand kann verbraucht werden  
Der Sicherheitsbestand ist hauptsächlich ein Bedarfstyp und wird daher am Planungsstartdatum in das Bestandsprofil geladen.  

Der Sicherheitsbestand ist eine Bestandsmenge, die beiseite gelegt wird, um Ungewissheiten beim Bedarf während der Beschaffungszeit zu kompensieren. Jedoch kann er verbraucht werden, wenn es erforderlich ist, ihn zur Deckung eines Bedarfs zu verwenden. In diesem Fall wird durch das Planungssystem sichergestellt, dass der Sicherheitsbestand schnell ersetzt wird, indem am Datum des Verbrauchs ein Ausnahmebeschaffungsauftrag zum Auffüllen des Sicherheitsbestands vorgeschlagen wird. In dieser Planungszeile wird das Symbol für eine Ausnahmewarnung angezeigt, durch das der Planer darauf aufmerksam gemacht wird, dass der Sicherheitsbestand teilweise oder vollständig aufgrund eines Ausnahmeauftrags für die Fehlteile verbraucht wurde.  

### <a name="forecast-demand-is-reduced-by-sales-orders"></a>Planungsbedarf wird durch Verkaufsaufträge reduziert  
Der Produktionsplan drückt den erwarteten künftigen Bedarf aus. Während der Eingabe des tatsächlichen Bedarfs, üblicherweise als Verkaufsaufträge für Fertigungsartikel, verbraucht er die Planung.  

Die Planung selbst wird durch Verkaufsaufträge nicht reduziert; sie bleibt unverändert. Jedoch werden die geplanten Mengen, die in der Planungsberechnung verwendet werden, reduziert (über die Verkaufsauftragsmengen), bevor die eventuelle Restmenge in das Bedarfsbestandsprofil eingeht. Wenn das Planungssystem tatsächliche Verkäufe für eine Periode prüft, schließt dies sowohl Verkaufsaufträge als auch Artikelposten von gelieferten Verkäufen ein, es sei denn, sie ergeben sich aus einem Rahmenauftrag.  

Ein Benutzer muss eine gültige Planungsperiode definieren. Das Datum auf der Planungsmenge definiert den Anfang der Periode, und das Datum auf der nächsten Planung definiert das Ende der Periode.  

Die Planung für Zeiträume vor der Planungsperiode wird nicht verwendet, unabhängig davon, ob sie verbraucht wurde oder nicht. Die erste interessante Planungszahl ist entweder das Datum auf oder möglichst nahe vor dem Planungsstartdatum.  

Die Planung kann für unabhängigen Bedarf, wie etwa Verkaufsaufträge, oder abhängigen Bedarf, wie etwa FA-Komponenten (Modul Planung) gelten. Ein Artikel kann beide Planungsarten haben. Während der Planung findet der Verbrauch separat statt, zuerst für unabhängigen Bedarf und dann für abhängigen Bedarf.  

### <a name="blanket-order-demand-is-reduced-by-sales-orders"></a>Der Rahmenauftragsbedarf wird durch Verkaufsaufträge reduziert  
Die Planung wird durch den Rahmenauftrag als Mittel zur Angabe des zukünftigen Bedarfs von einem bestimmten Debitoren ergänzt. Wie mit dem (unspezifizierten) Plan sollte der tatsächliche Verkauf den voraussichtlichen Bedarf verbrauchen, und die restliche Menge sollte in das Bedarfsbestandsprofil eingehen. Wieder reduziert der Verbrauch nicht tatsächlich den Rahmenauftrag.  

Die Planungsberechnung berücksichtigt offene Verkaufsaufträge, die mit dieser bestimmten Rahmenauftragszeile verbunden sind, nicht jedoch Gültigkeitszeiträume. Es berücksichtigt auch nicht gebuchte Aufträge, da das Buchungsverfahren bereits die ausstehende Rahmenauftragsmenge reduziert hat.

## <a name="prioritizing-orders"></a>Aufträge mit Priorität
In bestimmten Lagerhaltungsdaten zeigt das angeforderte oder verfügbare Datum die höchste Priorität an; mit dem Bedarf des heutigen Tages soll vor dem Bedarf der nächsten Woche verfahren werden. Zusätzlich zu dieser allgemeinen Priorität schlägt das Planungssystem jedoch auch vor, welche Art von Bedarf vor anderen Bedarfen erfüllt werden soll. Ebenso empfiehlt es eine auszugleichende Versorgungsquelle vor anderen Versorgungsquellen. Dieses wird gemäß Auftragsprioritäten durchgeführt.  

Geladener Bedarf und Vorrat tragen zu einem Profil für den voraussichtlichen Lagerbestand entsprechend den folgenden Prioritäten bei:  

### <a name="priorities-on-the-demand-side"></a>Prioritäten der Bedarfs-Seite  
1. Bereits geliefert: Artikelposten  
2. Einkaufsreklamation  
3. Verkaufsauftrag  
4. Serviceauftrag  
5. Bedarf an Produktionskomponenten  
6. Montageauftragszeile  
7. Ausgehender Umlagerungsauftrag.  
8. Rahmenauftrag (der nicht bereits durch zugehörige Verkaufsaufträge verbraucht wurde)  
9. Planung (die nicht bereits durch andere Verkaufsaufträge verbraucht wurde)  

> [!NOTE]  
>  Einkaufsreklamationen sind normalerweise nicht Teil der Absatzplanung; sie sollten stets in der Charge reserviert sein, die zurückgegeben wird. Falls nicht reserviert, spielen Einkaufsreklamationen eine Rolle bei der Verfügbarkeit und werden hoch priorisiert, um zu vermeiden, dass das Planungssystem einen Beschaffungsauftrag vorschlägt, nur um eine Einkaufsreklamation zu erfüllen.  

### <a name="priorities-on-the-supply-side"></a>Prioritäten der Bedarfs-Seite  
1. Bereits im Bestand: Artikelposten (Planungs-Flexibilität = keine)  
2. Verkaufsreklamation (Planungs-Flexibilität = keine)  
3. Ausgehende Umlagerungsaufträge  
4. Fertigungsauftrag  
5. Montageauftrag  
6. Bestellung  

### <a name="priority-related-to-the-state-of-demand-and-supply"></a>Priorität in Bezug auf Status des Bedarfs und des Angebotes  
Abgesehen von den Prioritäten, die von dem Typ des Bedarfs oder des Vorrats vorgegeben werden, definiert der aktuelle Zustand der Aufträge im Ausführungsprozess ebenfalls eine Priorität. Beispielsweise haben Lageraktivitäten Auswirkungen, und der Status von Verkaufs-, Einkaufs-, Umlagerungs-, Montage- und Fertigunksaufträgen wird berücksichtigt:  

1. Teilweise bearbeitet (Planungs-Flexibilität = Nein)  
2. Bereits in Bearbeitung im Lager (Planungs-Flexibilität = keine)  
3. Freigegeben - alle Auftragsarten (Planungs-Flexibilität = unbegrenzt)  
4. Fest geplanter Fertigungsauftrag (Planungs-Flexibilität = unbegrenzt)  
5. Geplant/Offen – alle Ordnertypen (Planungs-Flexibilität = unbegrenzt)

## <a name="balancing-supply-with-demand"></a>Bedarf und Vorrat ausgleichen
Das Kernstück des Planungssystems beinhaltet den Ausgleich von Bedarf und Vorrat durch das Vorschlagen von Benutzeraktionen zur Überarbeitung der Beschaffungsaufträge bei Diskrepanz. Dieses findet pro Kombination von Variante und Lagerort statt.  

Stellen Sie sich vor, dass jedes Lagerprofil eine Zeichenfolge aus den Bedarfsereignissen (sortiert nach Datum und Priorität) und eine entsprechende Zeichenfolge von Vorratsereignissen enthält. Jedes Ereignis verweist zurück auf seinen Herkunftsartstyp und seine Identifizierung. Die Regeln für den Ausgleich des Artikels sind einfach. Zu jedem Zeitpunkt des Vorgangs können vier Instanzen des Abgleichs von Bedarf und Vorrat auftreten:  

1. Kein Bedarf oder Vorrat für den Artikel => die Planung ist abgeschlossen (oder soll nicht beginnen).  
2. Bedarf existiert, aber es ist kein Vorrat vorhanden=> Vorrat soll vorgeschlagen werden.  
3. Vorrat existiert, aber es ist kein Bedarf vorhanden=> Vorrat soll storniert werden.  
4. Bedarf und Vorrat sind vorhanden => Fragen sollten gestellt und beantwortet werden, bevor das System sicherstellen kann, dass der Bedarf befriedigt wird und der Vorrat ausreicht.  

    Wenn das Timing des Vorrats nicht geeignet ist, kann der Vorrat möglicherweise wie folgt umgeplant werden:  

    1.  Wenn der Vorrat vor dem Bedarf platziert wird, kann der Vorrat vielleicht umgeplant werden, so dass der Bestand so niedrig wie möglich ist.  
    2.  Wenn das Angebot später gesetzt wird, kann das Angebot möglicherweise umgeplant werden. Andernfalls schlägt das System einen neuen Vorrat vor.  
    3.  Wenn der Vorrat den Bedarf an dem Datum erfüllt, kann das Planungssystem fortfahren, zu untersuchen, ob die Menge des Vorrats den bedarf decken kann.  

    Sobald die Zeitplanung erfolgt ist, kann die entsprechende bereitzustellende Menge wie folgt berechnet werden:  

    1.  Wenn die Vorratsmenge kleiner als der Bedarf ist, ist es möglich, dass die Vorratsmenge erhöht werden kann (oder nicht, wenn Sie durch eine Höchstmengenrichtlinie begrenzt ist).  
    2.  Wenn die Vorratsmenge größer als der Bedarf ist, ist es möglich, dass die Vorratsmenge reduziert werden kann (oder nicht, wenn Sie durch eine Mindestmengenrichtlinie begrenzt ist).  

    An dieser Stelle besteht eine von zwei Situationen:  

    1.  Der aktuelle Bedarf kann abgedeckt werden, in welchem Fall er geschlossen werden kann und die Planung für den folgenden Bedarf begonnen werden kann.  
    2.  Das Vorrat hat sein Maximum erreicht, ein Teil der Bedarfsmenge wurde nicht abgedeckt. In diesem Fall kann das Planungssystem den aktuellen Vorrat schließen und mit dem nächsten fortfahren.  

 Der Vorgang beginnt von vorn mit dem folgenden Bedarf und dem folgenden Vorrat oder umgekehrt. Der aktuelle Vorrat kann möglicherweise auch diesen nächsten Bedarf abdecken, oder der aktuelle Bedarf wurde noch nicht vollständig abgedeckt.  

### <a name="rules-concerning-actions-for-supply-events"></a>Regeln im Hinblick auf Aktionen für Vorratsereignisse  
Wenn das Planungssystem eine top-down Berechnung ausführt, in der der Vorrat den Bedarf erfüllen muss, gilt der Bedarf als entnommen, d.h. es liegt außerhalb des Steuererung des Planungssystems. Jedoch kann die Vorratsseite verwaltet werden. Daher wird vom Planungssystem vorgeschlagen, neue Beschaffungsaufträge zu erstellen, bestehenden neu zu planen und/oder die Bestellmenge zu ändern. Wenn ein vorhandener Beschaffungsauftrag überflüssig wird, schlägt das System dem Benutzer vor, ihn zu stornieren.  

Wenn der Benutzer einen vorhandenen Beschaffungsauftrag aus den Planungsvorschlägen ausschließen möchte, kann er angeben, dass keine Planungsflexibilität besteht (Planungsflexibilität = Keine). Dann wird überschüssiger Vorrat aus diesem Auftrag verwendet, um Bedarf zu decken, aber keine Aktion wird vorgeschlagen.  

Im Allgemeinen haben alle Vorräte eine Planungsflexibilität, die durch den Zustand der einzelnen vorgeschlagenen Aktionen eingeschränkt ist.  

-   **Neuplanung Aus**: Das Datum eines vorhandenen Beschaffungsauftrags kann ausgeplant werden, um das Fälligkeitsdatum des Bedarfs zu erfüllen, es sei denn:  

    -   Es stellt den Lagerbestand dar (immer mit Tag Null).  
    -   Es enthält einen Auftrag-zu-Auftrag-Link zu einem anderen Bedarf.  
    -   Es liegt außerhalb der durch den Zeitrahmen definierten, neu geplanten Seite.  
    -   Es gibt einen näheren Bestand, der verwendet werden könnte.  
    -   Andererseits entscheidet sich der Benutzer möglicherweise zu einer Neuplanung, weil  
    -   Der Beschaffungsauftrag wurde bereits an einem früheren Datum mit einem anderen Bedarf verbunden.  
    -   Das erforderliche Neuplanung ist so minimal, dass der Benutzer sie als geringfügig ansehen wird.  

-   **Neuplanung Ein**: Das Datum eines vorhandenen Beschaffungsauftrags kann eingeplant werden, ausgenommen unter den folgenden Bedingungen:  

    -   Es wird direkt mit einem anderen Bedarf verknüpft.  
    -   Es liegt außerhalb der durch den Zeitrahmen definierten, neu geplanten Seite.  

> [!NOTE]  
>  Wenn ein Artikel unter Verwendung eines Minimalbestands geplant wird, kann der Beschaffungsauftrag immer bei Bedarf geplant werden. Dies ist häufig in den vorwärtsgeplanten Beschaffungsaufträgen, die durch einen Minimalbestand gestartet werden.  

-   **Zugangs-Menge**: Die Menge eines vorhandenen Beschaffungsauftrags kann erhöht werden, damit der Bedarf erfüllt werden kann, es sei denn, der Beschaffungsauftrag ist direkt mit einem Bedarf durch einen Auftrag-zu-Auftrag-Link verknüpft.  

> [!NOTE]  
>  Obwohl es möglich ist, den Beschaffungsauftrag zu erhöhen, kann dies durch eine maximale Auftragsgröße eingeschränkt sein.  

-   **Menge reduzieren**: Ein vorhandener Beschaffungsauftrag mit einem Überschuss im Vergleich zu einem vorhandenen Bedarf kann reduziert werden, damit der Bedarf erfüllt werden kann.  

> [!NOTE]  
>  Obwohl die Menge verringert werden kann, ist möglicherweise immer noch Überschuss im Vergleich zum Bedarf vorhanden, und zwar aufgrund einer Mindestauftragsmenge oder eines Auftragsvielfachen.  

-   **Abbrechen**: Als spezieller Vorfall der Mengenverminderungsaktion könnte der Beschaffungsauftrag storniert werden, wenn er bis auf Null verringert wurde.  
-   **Neu**: Wenn kein Beschaffungsauftrag existiert oder jedoch ein existierender, der nicht geändert werden kann, um der erforderlichen Menge im angeforderten Fälligkeitsdatum zu genügen, wird ein neuer Beschaffungsauftrag vorgeschlagen.  

### <a name="determining-the-supply-quantity"></a>Bestimmen der Vorratsmenge  
Durch den Benutzer definierte Planungsparameter steuern die vorgeschlagene Menge eines jeden Beschaffungsauftrags.  

Wenn das Planungssystem die Menge eines neuen Beschaffungsauftrags oder die Mengenänderung in bestehenden Aufträgen berechnet, kann sich die vorgeschlagene Menge von der tatsächlich benötigten unterscheiden.  

Wenn ein Maximalbestand oder eine feste Auftragsmenge ausgewählt werden, wird die vorgeschlagene Menge erhöht, um diese feste Menge oder den Maximalbestand zu erfüllen. Wenn ein Wiederbeschaffungsverfahren einen Minimalbestand verwendet, wird die Menge mindestens so erhöht, dass der Minimalbestand erreicht wird.  

 Die vorgeschlagene Menge kann in dieser Sequenz geändert werden:  

1. Bis zur maximalen Auftragsmenge (falls vorhanden).  
2. Aufwärts bis zur Mindestbestellmenge.  
3. Aufwärts bis zum nächsten Losgrößenrundungsfaktor. (Im Falle fehlerhafter Einstellungen verstößt dies möglicherweise gegen die maximale Auftragsmenge.)  

### <a name="order-tracking-links-during-planning"></a>Bedarfsverursacherverknüpfungen bei der Planung  
Hinsichtlich des Auftragsnachverfolgung während der Planung ist es wichtig zu erwähnen, dass das Planungssystem die dynamisch erstellten Auftragsnachverfolgungsverknüpfungen für die Artikel-/Varianten-/Lagerortkombinationen neu anordnet.  

Hierfür gibt es zwei Gründe:  

-   Das Planungssystem muss in der Lage sein, seine Vorschläge zu begründen; dass der Gesamtbedarf gedeckt wurde und dass keine Beschaffungsaufträge überflüssig sind.  
-   Dynamisch erstellte Auftragsnachverfolgungslinks müssen regelmäßig nachjustiert werden.  

Im Laufe der Zeit geraten dynamische Bedarfsverursacherverknüpfungen aus der Balance, da das gesamte Bedarfsverursachernetzwerk erst dann wiederhergestellt wird, wenn ein Bedarf- oder Vorratsereignis tatsächlich geschlossen ist.  

Vor dem Ausgleich des Vorrats nach Bedarf löscht die Anwendung alle vorhandenen Auftragsnachverfolgungslinks. Dann während des Ausgleichsvorgangs, wenn ein Bedarfs- oder Zubehörereignis abgeschlossen wird, werden neue Bedarfsverursacherverknüpfungen zwischen Bedarf und Angebot erstellt.  

> [!NOTE]  
>  Selbst wenn der Artikel nicht für die dynamische Auftragsnachverfolgung eingerichtet wurde, erstellt das Planungssystem Auftragsverfolgungslinks wie oben erläutert.
## <a name="closing-demand-and-supply"></a>Bedarf und Vorrat beenden
Wenn die Zubehör-Ausgleichsverfahren ausgeführt wurden, gibt es drei mögliche Schlusssituationen:  

* Die benötigte Menge und das Datum der Bedarfsereignisse wurden erfüllt, und die Planung für den Artikel kann geschlossen werden. Das Vorratsereignis ist noch offen und kann möglicherweise den nächsten Bedarf decken, der Ausgleichsvorgang kann daher erneut mit dem aktuellen Vorratsereignis und dem nächsten Bedarf starten.  
* Der Beschaffungsauftrag kann nicht geändert werden, um den gesamten Bedarf zu decken. Das Bedarfsereignis ist noch offen, mit einigen nicht abgedeckten Mengen, die möglicherweise vom nächsten Bedarfsereignis abgedeckt werden. Daher wird das aktuelle Vorratsereignis geschlossen, sodass der Ausgleichsvorgang mit dem aktuellen Bedarfs- und dem nächsten Vorratsereignis erneut beginnen kann.  
* Der gesamte Bedarf ist abgedeckt; es gibt keinen folgenden Bedarf (oder es gab überhaupt keinen Bedarf). Wenn überschüssiger Vorrat vorhanden ist, kann dieser vermindert (oder storniert) und dann geschlossen werden. Es ist möglich, dass zusätzliche Zubehörereignisse weiter entlang der Kette vorhanden sind, und diese sollten ebenfalls annulliert werden.  

Schließlich erstellt das Planungssystem ein Auftragsnachverfolgungslink zwischen dem Vorrat und dem Bedarf.  

### <a name="creating-the-planning-line-suggested-action"></a>Die Planungszeile (vorgeschlagene Aktion) erstellen  
Wenn eine Aktion – Neu, Menge ändern, Neuplanen, Neuplanen und Menge ändern oder Stornieren – für die Revision des Beschaffungsauftrags vorgeschlagen wird, erstellt das Planungssystem, eine Planung auf dem Planungsarbeitsblatt. Aufgrund der Auftragsnachverfolgung wird die Planungszeile nicht nur erstellt, wenn das Vorratsereignis geschlossen wird, sondern auch, wenn das Nachfrageereignis geschlossen wird, auch wenn das Vorratsereignis möglicherweise noch offen und abhängig von zusätzlichen Änderungen ist, wenn das nächste Nachfrageereignis verarbeitet wird. Dies bedeutet, dass die Planungszeile, wenn sie zuerst erstellt wird, möglicherweise erneut geändert wird.  

Um Datenbankzugriff zu minimieren, wenn Sie Fertigungsaufträge bearbeiten, können Sie die Planungszeile in drei Ebenen verwalten, mit dem Ziel, das am wenigsten anspruchsvolle Bestanderhaltungsniveau auszuführen:  

* Erstellen Sie nur die Planungszeile mit dem aktuellen Fälligkeitsdatum und der Menge, aber ohne Arbeitsplan und Komponenten.  
* Arbeitsplan einschließen: Der geplante Arbeitsplan wird einschließlich Berechnung des Start- und Enddatum und -Zeiten ausgebreitet. Dieses ist anspruchvoll in Bezug auf Datenbankzugriffe. Um das End- und die Fälligkeitsdatum zu bestimmen, kann es notwendig sein, dies zu berechnen, auch wenn das Vorratsereignis nicht abgeschlossen wurde (im Fall der Vorwärtsterminierung).  
* Strukturstückliste einschließen: Dies kann warten bis kurz vor dem Abschluss des Vorratsereignisses.  

Damit sind die Beschreibungen dazu, wie Bedarf und Vorrat vom Planungssystem geladen, priorisiert und ausgeglichen werden, abgeschlossen. In der Integration mit dieser Beschaffungsplanungsaktivität muss das System sicherstellen, dass der erforderliche Lagerbestand jedes geplanten Artikels entsprechend den jeweiligen Wiederbeschaffungsverfahren verwaltet wird.

## <a name="see-also"></a>Siehe auch  
 [Designdetails: Zentrale Konzepte des Planungssystems](design-details-central-concepts-of-the-planning-system.md)   
 [Designdetails: Umgang mit Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md)   
 [Designdetails: Vorratsplanung](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]